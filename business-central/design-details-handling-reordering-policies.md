---
title: Hönnunarupplýsingar - Meðhöndlun endurpöntunarstefnur
description: Í þessari grein er yfirlit yfir endurpöntunarstefnuna sem hægt er að nota í framboðsáætlun.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.date: 02/24/2023
ms.custom: bap-template
ms.service: dynamics-365-business-central
---
# <a name="design-details-handling-reordering-policies"></a>Hönnunarupplýsingar: Meðhöndlun endurpöntunarstefnur

Ef taka á vöru með í birgðaáætlun þarf að tilgreina endurpöntunarstefnu fyrir hana á **birgðaspjaldssíðunni** . Eftirfarandi endurpöntunarstefnur eru tiltækar:  

* Fast endurpöntunarmagn  
* Hámarksmagn  
* Röð  
* Lota fyrir lotu  

Fast **endurpöntunarmagn** og **Hámarksmagn** reglur tengjast birgðaáætlun. Þessi stefna fylgir skref fyrir skref mótun framboðs og pöntunarrakningar.  

## <a name="the-role-of-the-reorder-point"></a>Hlutverk endurpöntunarmarksins

Endurpöntunarmark stendur fyrir eftirspurn á afhendingartíma. Þegar birgðir eru áætlaðar fyrir neðan stigið sem skilgreint er af endurpöntunarmarki er kominn tími til að panta meira. Birgðir minnka smám saman þar til áfyllingin berst. Það gæti náð núlli eða öryggisbirgðastigi. Áætlunarkerfið leggur til framvirka birgðapöntun þegar birgðir fara niður fyrir endurpöntunarmark.  

Birgðastig geta hreyft verulega meðan á tímarammanum stendur. Þess vegna fylgist áætlunarkerfið stöðugt með tiltækum birgðum.

## <a name="monitoring-the-projected-inventory-level-and-the-reorder-point"></a>Eftirlit með áætluðu birgðastigi og endurpöntunarmarki

Birgðir eru tegund af framboði, en fyrir birgðaáætlanagerð, greinir áætlanakerfið milli tveggja birgðastiga:  

* Áætlaðar birgðir  
* Áætlaðar tiltækar birgðir  

### <a name="projected-inventory"></a>Áætlaðar birgðir

Í upphafi áætlunarferlisins eru áætlaðar birgðir brúttómagn birgða. Brúttómagnið felur í sér bókað og óbókað framboð og eftirspurn í fortíðinni. Þetta magn verður áætlað birgðastig sem brúttómagn úr framboði og eftirspurn viðhalda. Framboð og eftirspurn eru kynnt meðfram tímalínunni, hvort sem er frátekið eða úthlutað með öðrum hætti.  

Áætlunarkerfið notar áætlaðar birgðir til að fylgjast með endurpöntunarmarkinu og ákvarða endurpöntunarmagnið með reitnum **Hámarksmagn.** endurpöntunarstefnunni.  

### <a name="projected-available-inventory"></a>Áætlaðar tiltækar birgðir

Áætlaðar birgðir til ráðstöfunar eru birgðir sem eru tiltækar til að uppfylla eftirspurn á tilteknum tímapunkti. Áætlunarkerfið notar áætlaðar birgðir til ráðstöfunar þegar fylgst er með öryggisbirgðastiginu. Öryggisbirgðir verða alltaf að vera tiltækar fyrir óvænta eftirspurn.  

### <a name="time-buckets"></a>Tímafötur

Mikilvægt er að greina áætluð birgðir þegar komið er á endurpöntunarmark og að reikna út rétt pöntunarmagn þegar **notað er Hámarksmagn.** endurpöntunarstefnunni.  

Áætlað birgðastig er reiknað í upphafi áætlunartímabilsins. Það er brúttóstig sem tekur ekki tillit til frátekninga eða annarra úthlutana. Til að fylgjast með þessu birgðastigi í áætlunarröðinni fylgist áætlunarkerfið með uppsöfnuðum breytingum á tilteknu tímabili. Það tímabil nefnist *tímarammi*. Til að [fræðast meira um tímafötur er farið í Hlutverk tímarammans](#the-role-of-the-time-bucket). Áætlunarkerfið tryggir að vinnutíminn sé að minnsta kosti einn dagur. Einn dagur er lágmarkstími fyrir eftirspurn eða framboðsviðburði.  

### <a name="determining-the-projected-inventory-level"></a>Ákvörðun á áætluðu birgðastigi

Eftirfarandi röð lýsir því hvernig áætlunarkerfið ákvarðar áætlað birgðastig:  

* Þegar framboðstilvik er að fullu áætlað, t.d. innkaupapöntun, eykur það áætlaðar birgðir á skiladegi tilviksins.  
* Þegar eftirspurnaratvik er fullnægt minnkar það ekki áætlaðar birgðir strax. Þess í stað bókar það minnkunaráminningu sem er innri færsla sem geymir dagsetningu og magn til viðbótar við áætlaðar birgðir.  
* Þegar síðari framboðstilvik eru áætluð og bætt við tímalínuna rannsakar kerfið bókaðar minnkunaráminningar, hver fyrir sig og eina á áætlaðan dag framboðsins. Í þessu ferli er hægt að ná eða fara yfir endurpöntunarmark innheimtubréfs innanhúss.  
* Ef ný framboðspöntun er kynnt kannar hún hvort hún er færð inn á undan núverandi framboði. Ef svo er verður nýja framboðið núgildandi og jöfnunarferlið endurræsist.  

Eftirfarandi mynd sýnir þessa reglu.  

![Ákvarða áætlaðar birgðir.](media/nav_app_supply_planning_2_projected_inventory.png "Ákvarða áætlaðar birgðir")  

1. Framboð **Sa** af 4 (fast) lokar Eftirspurn **Da** af -3.  
2. CloseDemand: Búa til lækkunaráminningu -3 (ekki sýnt).  
3. Framboð **Sa** er lokað með umframmagni 1 (það er ekki meiri eftirspurn).  

     Áætluð birgðastig hækkar í +4, en áætlaðar birgðir til ráðstöfunar **verða** -1.  

4. Næsta eftirspurn **Sb** af 2 (önnur pöntun) hefur þegar verið sett á tímalínuna.  
5. Áætlunarkerfið leitar að minnkunaráminningu á undan **Sb**  (í þessu dæmi er það ekki svo ekki sé framkvæmd aðgerð).  
6. Áætlunarkerfið lokar **framboðsbirgðum**  (ekki meiri eftirspurn er til) með því að minnka það í 0 (hætta við) eða B, með því að skilja hana eftir eins og hún er.  

     Áætluð birgðastigsaukning (A: +0 => +4 eða B: +2 = +6).  

7. Áætlunarkerfið gerir lokaathugun. Er einhver minnkunaráminning? Já, það er eitt á dagsetningunni **Da**.  
8. Áætlunarkerfið bætir minnkunaráminningunni -3 áminningu við áætlað birgðastig, annaðhvort A: +4 -3 = 1 eða B: +6 -3 = +3.  
9. Fyrir A býr áætlunarkerfið til framvirka tímasetta pöntun sem hefst á degi **da**. Fyrir B er náð í endurpöntunarmarkið og ný pöntun er stofnuð.

## <a name="the-role-of-the-time-bucket"></a>Hlutverk tímarammans

Tilgangur tímarammans er að innheimta eftirspurnarviðburði innan tímabils til að gera sameiginlega framboðspöntun.  

Fyrir endurpöntunarstefnur sem nota endurpöntunarmark er hægt að skilgreina tímaramma. Tímarammar tryggja að eftirspurn innan sama tímabils sé safnað saman. Kerfið kannar síðan áhrifin á áætlaðar birgðir og hvort endurpöntunarmarkið hafi verið sent.

Ef endurpöntunarmarkið er sent tímasetur kerfið nýja framboðspöntun frá lokum tímarammans. Tímaramar byrja á upphafsdagsetningu áætlunarinnar.  

Hugtakið tímarammi sýnir handvirka athugun á birgðastiginu í staðinn fyrir hverja færslu. Tíðnin er skilgreind (tímaraminn). Til dæmis er hægt að safna saman öllum vöruþörfum frá lánardrottni til að setja vikulega pöntun.  

![Dæmi um tímaramma í skipulagningu.](media/nav_app_supply_planning_2_reorder_cycle.png "Dæmi um tímaramma í skipulagningu")  

Tímaföt eru oft notuð til að forðast áhrif cascade. Til dæmis jöfn lína framboðs og eftirspurnar þar sem fyrri eftirspurn er afturkölluð eða ný búin til. Niðurstaðan ætti að vera sú að framboðspöntunin (nema sú síðasta) er enduráætluð.

## <a name="stay-below-the-overflow-level"></a>Halda sig undir yfirflæði

Þegar reiturinn Hámarksmagn **er notaður** og **Fast endurpöntunarmagn** endurpöntunarstefnur, áætlunarkerfið einbeitir sér aðeins að áætluðum birgðum á tilteknum tímafötum. Það gæti stungið upp á aukabirgðum þegar neikvæð eftirspurn eða jákvæðar framboðsbreytingar gerast utan tímarammanns. Áætlunarkerfið reiknar út magnið sem minnka ætti framboðið um til viðbótar. Þetta magn er kallað „yfirflæðisstig“. Yfirflæðið er tiltækt sem áætlunarlína með **aðgerðinni Breyta magni (minnkun)** eða **Hætta við** og eftirfarandi viðvörunarboð:  

* Takið eftir: Áætlaðar birgðir [xx] eru hærri en yfirflæðisstigið [xx] á skiladeginum [xx].*  

![Yfirflæðisstig birgða.](media/supplyplanning_2_overflow1_new.png "Yfirflæðisstig birgða")  

### <a name="calculating-the-overflow-level"></a>Útreikningur á yfirflæðisstigi

Yfirflæðisstigið er reiknað á mismunandi hátt eftir endurpöntunarstefnunni.  

#### <a name="maximum-qty"></a>Hámarksmagn

Yfirflæðisstig = hámarksbirgðir  

> [!NOTE]  
> Ef notað er lágmarksmagn pöntunar er því bætt við á eftirfarandi hátt:
>
> Yfirflæðisstig = hámarksbirgðir + lágmarksmagn pöntunar.  

#### <a name="fixed-reorder-qty"></a>Fast endurpöntunarmagn

Yfirflæðisstig = endurpöntunarmagn + endurpöntunarmark  

> [!NOTE]  
> Ef lágmarksmagn pöntunar er hærra en endurpöntunarmarkið er því skipt út á eftirfarandi hátt:
>
> Yfirflæðisstig = endurpöntunarmagn + lágmarksmagn pöntunar  

#### <a name="order-multiple"></a>Fjöldapanta

Ef margfeldi pöntunar er til leiðréttir það yfirflæðisstigið fyrir bæði Hámarksmagn og Fast endurpöntunarmagn endurpöntunarstefnu.  

### <a name="creating-the-planning-line-with-an-overflow-warning"></a>Áætlunarlínan búin til með yfirflæðisviðvörun

Áætlunarlína er stofnuð þegar framboð veldur því að áætlaðar birgðir eru hærri en yfirflæðisstigið í lok tímarammanns. Áætlunarlínan varar við viðbótarbirgðum, reiturinn **Samþykkja aðgerðarboð er ekki valinn og aðgerðarboðin** eru annaðhvort **Hætta við** eða **Breyta magni.**  

#### <a name="calculating-the-planning-line-quantity"></a>Útreikningur á magni áætlunarlínu

Magnið í áætlunarlínu er reiknað á eftirfarandi hátt:

áætlunarlínumagn = núgildandi framboðsmagn – (áætlaðar birgðir – yfirflæðisstig)  

> [!NOTE]  
> Fyrir sAs með allar viðvörunarlínur er hunsað hámarks- og lágmarksmagn pöntunar og margfeldi pöntunar.  

#### <a name="defining-the-action-message-type"></a>Skilgreining gerðar aðgerðaboða

* Ef magn áætlunarlínunnar er hærra en 0 eru **aðgerðarboðin Breyta magni.**  
* Ef magn áætlunarlínunnar er jafnt og eða lægra en 0 eru **aðgerðarboðin Hætta við**  

#### <a name="composing-the-warning-message"></a>Viðvörunarboð samin

Ef yfirflæði er á síðunni **Óraknar áætlunareiningar** birtar viðvörunarboð með eftirfarandi upplýsingum:  

* Áætlað birgðastig sem setti af stað viðvörunina.  
* Reiknaða yfirflæðisstigið  
* Skiladagur birgðavikunnar  

Dæmi Áætlaðar birgðir 120 eru meiri en yfirflæðisstigið 60 á 01-28-23  

### <a name="example-scenario"></a>Dæmi dæmi

Í þessari atburðarás, breytir viðskiptamaður sölupöntun frá 70 í 40 stykki milli tveggja áætlunarkeyrslna. Yfirflæðisaðgerðin dregur úr innkaupunum sem lögð var til fyrir upphaflegt sölumagn.  

#### <a name="item-setup"></a>Vöruuppsetning

|Endurpöntunarstefna|Hámarksmagn|  
|-----------------------|------------------|  
|Hámarksmagn pöntunar|100%|  
|Endurpöntunarmark|50|  
|Birgðir|80|  

#### <a name="situation-before-sales-decrease"></a>Staða fyrir söluminnkun

|Atburður|Breyta magni|Áætlaðar birgðir|  
|-----------|-----------------|-------------------------|  
|Dagur eitt|Ekkert|80|  
|Sala|-70|10|  
|Lok tímaramma|Ekkert|10|  
|Leggja til nýja innkaupapöntun|+90|100%|  

#### <a name="situation-after-sales-decrease"></a>Staða eftir söluminnkun

|Breyting|Breyta magni|Áætlaðar birgðir|  
|------------|-----------------|-------------------------|  
|Dagur eitt|Ekkert|80|  
|Sala|-40|40|  
|Innkaup|+90|130|  
|Lok tímaramma|Ekkert|130|  
|Stinga upp á að minnka innkaup<br><br> panta frá 90 til 60|-30|100|  

#### <a name="resulting-planning-lines"></a>Áætlunarlínur sem leiða af sér

Kerfið stofnar viðvörunaráætlunarlínu til að minnka innkaupin um 30, úr 90 í 60, til að halda áætluðum birgðum í 100 í samræmi við yfirflæðisstigið.  

![Áætla samkvæmt yfirflæðisstigi.](media/nav_app_supply_planning_2_overflow2.png "Áætla samkvæmt yfirflæðisstigi")  

> [!NOTE]  
> Án yfirflæðisaðgerðarinnar er engin viðvörun stofnuð ef áætluð birgðastig er yfir hámarkinu sem gæti valdið 30 aukabirgðum.

## <a name="handling-projected-negative-inventory"></a>Meðhöndlun áætlaðra neikvæðra birgða

Endurpöntunarmarkið endurspeglar ætlaða eftirspurn á afhendingartíma vörunnar. Áætlaðar birgðir verða að vera nógu stórar til að standa undir eftirspurninni þar til nýja pöntunin er móttekin. Á meðan ættu öryggisbirgðir að uppfylla sveiflur í eftirspurn að áætluðu þjónustustigi.  

Áætlunarkerfið tekur það tillit til neyðar ef ekki er hægt að bera framtíðareftirspurn úr áætluðum birgðum. Einnig er gefið upp á annan hátt að áætluð birgðir fari neikvæðar. Kerfið leggur til að ný framboðspöntun sé stofnuð til að standa undir ómetnum hluta eftirspurnarinnar. Stærð nýju framboðspöntunarinnar mun hvorki taka tillit til hámarksbirgða né endurpöntunarmagns né eftirfarandi breytinga á pöntunum:

* Hámarksmagn pöntunar
* Lágmarksmagn pöntunar
* Fjöldapanta 

Þess í stað endurspeglar það nákvæmlega skort.  

Áætlunarlínan fyrir þessa tegund framboðspöntunar birtir **viðvörunartákn neyðarviðvörunar** veita viðbótarupplýsingar um aðstæðurnar.  

Í eftirfarandi mynd stendur framboð D fyrir neyðarpöntun til að leiðrétta fyrir neikvæðar birgðir.  

![Viðbragðsáætlun til að koma í veg fyrir neikvæða birgðastöðu.](media/nav_app_supply_planning_2_negative_inventory.png "Viðbragðsáætlun til að koma í veg fyrir neikvæða birgðastöðu")  

1. Framboð **A**, fyrstu áætlaðar birgðir, er undir pöntunarmark.  
2. Nýtt framsendingaráætlað framboð er stofnað (**C**).  

     (magn = hámarksbirgðir – áætlað birgðastig)  
3. Framboð **A** er lokað með eftirspurn **B**, sem er ekki að öllu leyti annað.  

     (Eftirspurn **B** gæti reynt að tímasetja framboð C en tímarammann kemur í veg fyrir það.)  
4. Nýtt framboð (**D**) er stofnað til að uppfylla eftirstandandi magn eftirspurnar **B**  
5. Eftirspurn **B** er lokað (búa til áminningu fyrir áætluðum birgðum).  
6. Nýjar birgðir **D** eru lokaðar.  
7. Merkt er við áætlaðar birgðir. Endurpöntunarmarkið hefur ekki verið farið yfir.  
8. Framboð **C** er lokað (eftirspurn er ekki meiri).  
9. Lokaathugun. Engar áminningar á birgðastigi eru útistandandi.  

Í eftirfarandi kafla er fjallað um einkenni fjögurra studdra endurpöntunarstefna.

## <a name="reordering-policies"></a>Endurpöntunarstefnur

Endurpöntunarstefnur skilgreina hversu mikið þarf að panta þegar vara þarf að vera fyllt á. Fjórir mismunandi endurröðunarstefnur eru til.  

### <a name="fixed-reorder-quantity"></a>Fast endurpöntunarmagn

Reglan Fast endurpöntunarmagn er gjarnan notuð fyrir birgðaáætlun fyrir vörur með eftirfarandi eiginleika:

* Lágur birgðakostnaður
* Lítil hætta á þráhyggju
* Lítill fjöldi vara

Venja er að nota þessa stefnu með endurpöntunarmarki sem endurspeglar áætlaða eftirspurn á afgreiðslutíma vörunnar.  

#### <a name="calculated-per-time-bucket"></a>Reiknað eftir tímaramu

Ef náð er í eða farið yfir endurpöntunarmarkið í tímaramma (endurpöntunarferli) leggur kerfið til tvær aðgerðir:

* Stofna nýja framboðspöntun fyrir endurpöntunarmagnið
* Tímasetja pöntunina áfram frá fyrstu dagsetningu eftir lok tímarammans  

Endurpöntunarmark tímanna minnkar fjölda birgðatillagna. Hann endurspeglar ferli prófunar handvirkt í raunverulegt innihald hólfa í vöruhúsinu.  

#### <a name="creates-only-necessary-supply"></a>Stofnar aðeins nauðsynlegt framboð

Áður en það leggur til nýja framboðspöntun til að uppfylla endurpöntunarmark athugar áætlunarkerfið eftirfarandi framboð:

* Hvort framboð hefur þegar verið pantað
* Hvort búist er við því að fá birgðir innan afhendingartíma vörunnar

Kerfið stingur ekki upp á nýrri framboðspöntun ef framboð færir áætlaðar birgðir til endurpöntunarmarks innan afgreiðslutíma.  

Framboðspantanir sem eru stofnaðar sérstaklega til að uppfylla endurpöntunarmark eru undanskildar frá birgðajöfnun og verður ekki breytt. Ef fara á út vöru sem er með endurpöntunarmark skal fara yfir útistandandi framboðspantanir handvirkt eða breyta endurpöntunarstefnunni **í Lotu-fyrir-lotu**. Kerfið dregur úr eða hættir við aukabirgðir.  

#### <a name="combines-with-order-modifiers"></a>Sameinar pöntunarbreyti

Lágmarksmagn pöntunar, Hámarksmagn pöntunar og Margfeldi pöntunarbreyta ættu ekki að gegna mikilvægu hlutverki þegar reglan Fast endurpöntunarmagn er notuð. Hins vegar tekur áætlunarkerfið það með í reikninginn:

* Minnka magnið í tiltekið hámarksmagn pöntunar (og stofna tvær eða fleiri birgðir til að ná heildarmagni pöntunar)
* Auka pöntunina í tiltekið lágmarksmagn pöntunar
* Slétta upp pöntunarmagnið til að uppfylla tiltekna pöntunarmargfeldi  

#### <a name="combines-with-calendars"></a>Sameinar dagatöl

Áður en ný framboðspöntun er lögð til að uppfylla endurpöntunarmark athugar áætlunarkerfið hvort pöntunin sé áætluð fyrir daginn sem er ekki virkur. Það notar dagatölin sem tilgreind eru í reitnum **Kóti** grunndagatals á síðunum **Stofngögn** og **Birgðageymsluspjald** .  

Ef áætluð dagsetning er ekki virkur dagur færir áætlunarkerfið pöntunina áfram á næsta vinnudag. Ef dagsetningin er færð getur það leitt til pöntunar sem uppfyllir endurpöntunarmark en uppfyllir ekki sérstaka eftirspurn. Fyrir svona ójafna eftirspurn, býr áætlanakerfið til auka framboð.  

#### <a name="shouldnt-be-used-with-forecasts"></a>Ætti ekki að nota með spám

Þar sem áætluð eftirspurn er þegar sýnd á stigi endurpöntunarmarks er ekki nauðsynlegt að taka spá með í áætluninni. Ef það á við til að byggja áætlunina á spá skal nota stefnuna **Lota fyrir lotu** .  

#### <a name="must-not-be-used-with-reservations"></a>Ekki má nota með frátekningum

Ef magn hefur verið frátekið, til dæmis magn í birgðum, fyrir fjarlæga eftirspurn gæti verið hægt að trufla áætlunargrunninn. Jafnvel þótt áætlað birgðastig sé leyfilegt með tilliti til endurpöntunarmarks, má magnið ekki vera til staðar vegna frátekningarinnar. Kerfið gæti reynt að bæta upp með því að stofna frávikspantanir. Hins vegar er mælt með því að reiturinn **Frátekið** sé stilltur **á Aldrei** á vörum sem áætlað er að nota endurpöntunarmark.

### <a name="maximum-quantity"></a>Hámarksmagn

Reglan um hámarksmag er ein leið til að viðhalda birgðum með því að nota endurpöntunarmark.  

Allt sem gildir um stefnu endurpöntunarmagns gildir einnig um þessa stefnu. Eini munurinn er magnið sem lagt er til sem framboð. Þegar hámarksmagnsstefnan er notuð er endurpöntunarmagnið skilgreint á kvikan hátt byggt á áætluðu birgðastigi. Þess vegna er það yfirleitt frábrugðið pöntun.  

#### <a name="calculate-per-time-bucket"></a>Reikna eftir tímafötu

Þegar farið er yfir endurpöntunarmarkið ákvarðar kerfið endurpöntunarmagnið í lok tímaramma. Hann mælir bilið milli núverandi áætlaðs birgðastigs og tilgreindra hámarksbirgða til að ákvarða magnið sem á að panta. Kerfið athugar síðan:

* Hvort framboð hefur þegar verið pantað
* Hvort búist er við því að fá birgðir innan afhendingartíma vörunnar

Ef svo er minnkar kerfið magn nýju framboðspöntunarinnar um magnið sem þegar hefur verið pantað.  

Ef hámarksbirgðamagn er ekki tilgreint tryggir áætlunarkerfið að áætlaðar birgðir nái endurpöntunarmagninu.

#### <a name="combine-with-order-modifiers"></a>Sameina pantanabreytingar

Það fer eftir uppsetningunni hvort best er að sameina stefnu hámarksmagns og breyta pöntunum: 

* Til að tryggja lágmarksmagn pöntunar
* Slétta magnið að heiltölufjölda innkaupamælieininga
* Skipta magninu í lotur eins og skilgreint er af hámarksmagni pöntunar  

### <a name="combine-with-calendars"></a>Sameina dagatöl

Áður en ný framboðspöntun er lögð til að uppfylla endurpöntunarmark athugar áætlunarkerfið hvort pöntunin sé áætluð fyrir daginn sem er ekki virkur. Það notar dagatölin sem tilgreind eru í reitnum **Kóti** grunndagatals á síðunum **Stofngögn** og **Birgðageymsluspjald** .  

Ef áætluð dagsetning er ekki virkur dagur færir áætlunarkerfið pöntunina áfram á næsta vinnudag. Ef dagsetningin er færð getur það leitt til pöntunar sem uppfyllir endurpöntunarmark en uppfyllir ekki sérstaka eftirspurn. Fyrir svona ójafna eftirspurn, býr áætlanakerfið til auka framboð.

### <a name="order"></a>Pöntun

Í umhverfi sem er eftir pöntun er vara keypt eða framleidd til að standa undir sérstakri eftirspurn. Yfirleitt er pöntunarendurpöntunarstefnan notuð fyrir vörur með eftirfarandi eiginleika

* Eftirspurn er óáreiðanleg
* Afgreiðslutíminn er ómarktækur
* Nauðsynlegar eigindir eru breytilegar  

[!INCLUDE [prod_short](includes/prod_short.md)] stofnar pöntun-í-pöntun tengil sem virkar sem bráðabirgðatenging milli framboðs (framboðspöntun eða birgðir) og eftirspurnarinnar. Hægt er að nota tengilinn pöntun-til-pöntun við áætlun á eftirfarandi hátt:  

* Þegar framleiðslustefnan Framleiðsla eftir pöntun er notuð til að stofna framleiðslupantanir af mörgum stigum eða framleiðslupantanir af verki (framleiða nauðsynlega íhluti á sömu framleiðslupöntun)  
* Þegar sölupöntunaráætlun er notuð til að stofna framleiðslupöntun úr sölupöntun  

> [!TIP]
> Ef vörueigindir eru ekki breytilegar gæti verið best að nota Lotu-fyrir-lotuendurpöntunarstefnuna. Þar af leiðandi notar kerfið óáætlaðar birgðir og safnar aðeins saman sölupöntunum með sömu afhendingardagsetningu eða innan tilgreinds tímaramma.  

#### <a name="order-to-order-links-and-past-due-dates"></a>Tenglar fyrir pöntun og gjalddaga sem komnir eru fram yfir

Ólíkt flestum framboð-eftirspurn settum eru tengdar pantanir með skiladag á undan upphafsdagsetningu áætlunar áætlaðar að fullu af kerfinu. Ástæðan fyrir þessari undantekningu er sú að samstilla verður tiltekin framboðssett eftirspurnar. Nánari upplýsingar um frysta svæðið sem á við um flestar tegundir framboðs eftirspurnar er farið í [Vinnslupantanir fyrir upphafsdagsetningu](design-details-balancing-demand-and-supply.md#process-orders-before-the-planning-start-date) áætlunarinnar.

### <a name="lot-for-lot"></a>Lota fyrir lotu

Lotu-fyrir-lotustefnuna er sveigjanlegasta vegna þess að kerfið bregst aðeins við raunverulegri eftirspurn. Hún vinnur með ráðgerða eftirspurn úr spá og standandi pöntunum og jafnar svo pöntunarmagnið samkvæmt eftirspurninni. Stefnan er ætluð fyrir vörur þar sem hægt er að samþykkja birgðir en ætti að forðast það.  

Að sumu leyti er lotu-fyrir-lotustefnunni svipað og pöntunarstefnan. Hún getur tekið við magni í birgðum og hún búnar til eftirspurn og framboð í tímaramunum sem notandinn skilgreinir.

Tímaraminn er tilgreindur í reitnum **Tímarauður** á **birgðaspjaldssíðunni** . Lágmarkstími fötu er einn dagur því það er minnsta tímamælieiningin í eftirspurn og framboðsviðburðum í [!INCLUDE [prod_short](includes/prod_short.md)].  

Tímarammann takmarkar einnig hvenær á að endurtímasetja framboðspöntun til að mæta tiltekinni eftirspurn. Framboð innan tímarammanns er endurtímasett inn og út til að mæta eftirspurninni. Fyrra framboð veldur viðbótarbirgðum og hætta ætti við það. Stofna skal nýja framboðspöntun fyrir framboð sem síðar.  

Með þessari stefnu er hægt að tilgreina öryggisbirgðir til að bæta fyrir breytingar á framboði eða til að mæta skyndilegri eftirspurn. Lotu-fyrir-lotustefnuna getur einnig falið í sér hömlunartímabil og hömlunarmagn til að draga úr pöntunaráætlun.  

Reiturinn **Lotusöfnunartímabil** stuðlar að því að skilgreina endurpöntunarferlið ásamt reitnum **Endurtímasetningartímabil** . Frá dagsetningu fyrstu eftirspurnar er öll eftirspurn safnað saman á næsta lotusafnunartímabili í eina framboðspöntun á degi fyrstu eftirspurnarinnar. Eftirspurn sem er utan lotusöfnunartímabilsins nær ekki yfir framboðspöntunina.

Þar sem magn framboðspöntunar er byggt á raunverulegri eftirspurn getur verið skynsamlegt að nota pöntunarbreytingar:

* Slétta upp pöntunarmagnið til að uppfylla margfeldi pöntunar (eða innkaupamælieiningu)
* Auka pöntunina í tiltekið lágmarksmagn pöntunar
* Minnka magnið í tiltekið hámarksmagn (og stofna þannig tvær eða fleiri birgðir til að ná heildarmagni sem þarf)

## <a name="see-also"></a>Sjá einnig

[Hönnunarupplýsingar: áætlunarfæribreyta](design-details-planning-parameters.md)  
[Hönnunarupplýsingar: áætlunartafla](design-details-planning-assignment-table.md)  
[Hönnunarupplýsingar: Miðlægar hugmyndir áætlanakerfisins](design-details-central-concepts-of-the-planning-system.md)  
[Hönnunarupplýsingar: Jöfnun eftirspurn og framboð](design-details-balancing-demand-and-supply.md)  
[Hönnunarupplýsingar: framboðsáætlun](design-details-supply-planning.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
