---
title: Hönnunarupplýsingar - Meðhöndlun endurpöntunarstefnur
description: Þessi grein gefur yfirlit yfir endurpöntunarstefnur sem hægt er að nota í framboðsáætlun.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: conceptual
ms.date: 02/24/2023
ms.custom: bap-template
---
# <a name="design-details-handling-reordering-policies"></a><a name="design-details-handling-reordering-policies"></a>Hönnunarupplýsingar: Meðhöndlun endurpöntunarstefnur

Til að hafa vöru með í framboðsáætlun þarf að tilgreina endurpöntunarreglu fyrir hana á **síðunni Birgðaspjald.**  Eftirfarandi endurpöntunarstefnur eru tiltækar:  

* Fast endurpöntunarmagn  
* Hámarksmagn  
* Röð  
* Lota fyrir lotu  

Fasta endurpöntunarmagnið **.**  og **Hámarks magn**  Reglur tengjast birgðaáætlun. Þessar stefnur eru samhliða jöfnun framboðs og pöntunarrakningar skref fyrir skref.  

## <a name="the-role-of-the-reorder-point"></a><a name="the-role-of-the-reorder-point"></a>Hlutverk endurpöntunarmarks

Endurpöntunarmark stendur fyrir eftirspurn á afhendingartíma. Þegar áætlað er að birgðir fari undir það stig sem endurpöntunarmarkið skilgreinir, er kominn tími til að panta meira. Birgðum fækkar smám saman þar til áfyllingin kemur. Það gæti náð núlli eða öryggisbirgðastigi. Áætlanakerfið leggur til framvirka birgðapöntun á þeim stað þegar birgðir fara undir endurpöntunarmark.  

Birgðastig getur færst verulega innan tímarammans. Þess vegna fylgist áætlanakerfið stöðugt með tiltækum birgðum.

## <a name="monitoring-the-projected-inventory-level-and-the-reorder-point"></a><a name="monitoring-the-projected-inventory-level-and-the-reorder-point"></a>Eftirlit með áætluðu birgðastigi og endurpöntunarmarki

Birgðir eru tegund af framboði, en fyrir birgðaáætlanagerð, greinir áætlanakerfið milli tveggja birgðastiga:  

* Áætlaðar birgðir  
* Áætlaðar tiltækar birgðir  

### <a name="projected-inventory"></a><a name="projected-inventory"></a>Áætlaðar birgðir

Við upphaf áætlunarferlisins eru áætlaðar birgðir vergt magn birgða. Verga magnið felur í sér áður bókað og óbókað framboð og eftirspurn. Þetta magn verður áætlað birgðastig sem vergt magn úr framtíðarframboði og eftirspurn viðhalda. Framtíðarframboð og eftirspurn eru kynnt eftir tímalínunni, hvort sem þau eru frátekin eða þeim úthlutað á annan hátt.  

Áætlanakerfið notar áætlaðar birgðir til að fylgjast með endurpöntunarmarki og ákvarða endurpöntunarmagn með því að nota hámarksmagn. **·**  endurpöntunarstefna.  

### <a name="projected-available-inventory"></a><a name="projected-available-inventory"></a>Áætlaðar tiltækar birgðir

Áætlaðar tiltækar birgðir eru birgðir sem eru tiltækar til að uppfylla eftirspurn á tilteknum tímapunkti. Áætlanakerfið notar áætlaðar tiltækar birgðir þegar fylgst er með öryggisbirgðastigi. Öryggisbirgðir verða alltaf að vera tiltækar fyrir óvænta eftirspurn.  

### <a name="time-buckets"></a><a name="time-buckets"></a>Tímarammar

Mikilvægt er að finna áætlaðar birgðir þegar endurpöntunarmarki er náð eða farið yfir það og reikna út rétt pöntunarmagn þegar hámarksmagn **er notað.**  endurpöntunarstefna.  

Áætlað birgðastig er reiknað við upphaf áætlunartímabilsins. Það er brúttóstig sem tekur ekki tillit til fyrirvara eða annarra úthlutana. Til að fylgjast með þessu birgðastigi í áætlunarröðinni fylgist áætlanakerfið með samanlögðum breytingum yfir tímabil. Það tímabil er kallað *tímarammi*. Til að læra meira um tímaramma skaltu fara í [Tímafötur](#time-buckets). Áætlanakerfið tryggir að tímaramminn sé að minnsta kosti einn dagur. Einn dagur er lágmarks tímaeining fyrir eftirspurn eða framboðstilvik.  

### <a name="determining-the-projected-inventory-level"></a><a name="determining-the-projected-inventory-level"></a>Ákvarða áætlað birgðastig

Eftirfarandi röð lýsir því hvernig áætlanakerfið ákvarðar áætlað birgðastig:  

* Þegar birgðatilvik er að fullu áætlað, eins og innkaupapöntun, eykur það áætlaðar birgðir á gjalddaga tilviksins.  
* Þegar eftirspurnartilvik er að fullu uppfyllt mun það ekki minnka áætlaðar birgðir strax. Þess í stað bókar það minnkunaráminningu, sem er innri færsla sem geymir dagsetningu og magn viðbótarinnar við áætlaðar birgðir.  
* Þegar seinna framboðstilvik er áætlað og bætt við tímalínuna rannsakar kerfið bókaðar minnkunaráminningar, eina af annarri að áætlaðri dagsetningu framboðsins. Meðan á þessu ferli stendur gæti endurpöntunarmarki innri aukningaráminningar verið náð eða farið yfir það.  
* Ef ný birgðapöntun er sett inn athugar hún hvort hún hafi verið færð inn á undan núverandi framboði. Ef svo er, verður nýja framboðið núverandi framboð og jafnvægisferlið endurræsir.  

Eftirfarandi mynd sýnir þessa meginreglu.  

![Ákvarða áætlaðar birgðir.](media/nav_app_supply_planning_2_projected_inventory.png "Ákvarða áætlaðar birgðir")  

1. Framboð **Sa** af 4 (fast) lokar Eftirspurn **Da** af -3.  
2. CloseDemand: Búa til lækkunaráminningu -3 (ekki sýnt).  
3. Framboð **Sa** er lokað með afgangi upp á 1 (það er ekki meiri eftirspurn).  

     Áætlað birgðastig hækkar í +4, á meðan áætlaðar **tiltækar** birgðir verða -1.  

4. Næsta eftirspurn **Sb** af 2 (önnur pöntun) hefur þegar verið sett á tímalínuna.  
5. Áætlanakerfið leitar að minnkunaráminningu áður en **Sb(** í þessu dæmi er það ekki, þannig að ekki er gripið til aðgerða).  
6. Áætlanakerfið lokar framboði **Sb** (ekki meiri eftirspurn er til) með því að annaðhvort A, minnka það í 0 (hætta við) eða B, með því að láta það vera eins og það er.  

     Áætlað birgðastig hækkar (A: +0 => +4 eða B: +2 = +6).  

7. Áætlanakerfið gerir lokaathugun. Er einhver áminning um lækkun? Já, það er eitt á dagsetningunni **Da**.  
8. Áætlanakerfið bætir minnkunaráminningu upp á -3 við áætlað birgðastig, annað hvort A: +4 -3 = 1 eða B: +6 -3 = +3.  
9. Fyrir A býr áætlanakerfið til framvirka áætlaða pöntun sem hefst á dagsetningu **Da**. Fyrir B er endurpöntunarmarki náð og ný pöntun stofnuð.

## <a name="the-role-of-the-time-bucket"></a><a name="the-role-of-the-time-bucket"></a>Hlutverk tímarammans

Tilgangurinn með tímarammanum er að safna saman eftirspurnartilvikum innan tímasíðunnar til að útbúa sameiginlega birgðapöntun.  

Fyrir endurpöntunarstefnur sem nota endurpöntunarmark er hægt að skilgreina tímaramma. Tímarammar hjálpa til við að tryggja að kröfur innan sama tímabils safnist upp. Kerfið athugar síðan áhrifin á áætlaðar birgðir og hvort endurpöntunarmark hafi verið náð.

Ef þú nærð endurpöntunarmarkinu tímasetur kerfið áfram nýja birgðapöntun frá lokum tímarammans. Tímarammar hefjast á upphafsdagsetningu áætlunar.  

Tímarammahugtakið endurspeglar handvirkt ferli við að athuga birgðastig oft frekar en fyrir hverja færslu. Tíðnin er skilgreind (tímaramminn). Til dæmis er hægt að safna saman öllum vöruþörfum frá lánardrottni til að leggja fram vikulega pöntun.  

![Dæmi um tímaramma í skipulagningu.](media/nav_app_supply_planning_2_reorder_cycle.png "Dæmi um tímaramma í skipulagningu")  

Tímarammar eru oft notaðir til að forðast keðjuverkun. Til dæmis jöfn lína framboðs og eftirspurnar þar sem fyrri eftirspurn er afturkölluð eða ný búin til. Niðurstaðan ætti að vera sú að framboðspöntunin (nema sú síðasta) er enduráætluð.

## <a name="stay-below-the-overflow-level"></a><a name="stay-below-the-overflow-level"></a>Vertu undir yfirfallsmörkum

Þegar hámarksmagn er **notað.**  og **fastur endurpöntunarmagn.**  Endurpöntunarstefnur, áætlanakerfið einbeitir sér að áætluðum birgðum aðeins innan tiltekins tímaramma. Það gæti bent til aukins framboðs þegar neikvæð eftirspurn eða jákvæðar breytingar á framboði eiga sér stað utan tímarammans. Fyrir auka framboð reiknar áætlanakerfið út magnið sem þú ættir að minnka framboð eftir. Þetta magn er kallað „yfirflæðisstig“. Yfirflæðið er tiltækt sem áætlunarlína með Breyta **magni (lækkun)**  eða **Hætta við** aðgerð og eftirfarandi viðvörunarskilaboð:  

* Athugið: Áætlaðar birgðir [xx] eru hærri en yfirflæðisstigið [xx] á gjalddaga [xx].*  

![Yfirflæðisstig birgða.](media/supplyplanning_2_overflow1_new.png "Yfirflæðisstig birgða")  

### <a name="calculating-the-overflow-level"></a><a name="calculating-the-overflow-level"></a>Útreikningur á yfirflæðisstigi

Yfirflæðisstigið er reiknað á mismunandi vegu eftir endurpöntunarstefnu.  

#### <a name="maximum-qty"></a><a name="maximum-qty"></a>Hámarksmagn

Yfirflæðisstig = hámarksbirgðir  

> [!NOTE]  
> Ef þú notar lágmarkspöntunarmagn er því bætt við sem hér segir:
>
> Yfirflæðisstig = hámarksbirgðir + lágmarkspöntunarmagn.  

#### <a name="fixed-reorder-qty"></a><a name="fixed-reorder-qty"></a>Fast endurpöntunarmagn

Yfirflæðisstig = endurpöntunarmagn + endurpöntunarmark  

> [!NOTE]  
> Ef lágmarkspöntunarmagn er hærra en endurpöntunarmarkið er því skipt út sem hér segir:
>
> Yfirflæðisstig = endurpöntunarmagn + lágmarkspöntunarmagn  

#### <a name="order-multiple"></a><a name="order-multiple"></a>Fjöldapanta

Ef margfeldi pöntunar er til staðar leiðréttir það yfirflæðisstig fyrir bæði Hámarksmagn og Fast endurpöntunarmagn endurpöntunarstefnu.  

### <a name="creating-the-planning-line-with-an-overflow-warning"></a><a name="creating-the-planning-line-with-an-overflow-warning"></a>Stofna áætlunarlínu með viðvörun um yfirflæði

Áætlunarlína er stofnuð þegar framboð veldur því að áætlaðar birgðir eru hærri en yfirflæðisstig í lok tímaramma. Til að vara við aukaframboðinu er áætlunarlínan með viðvörunarboð, reiturinn **Samþykkja aðgerðarboð** er ekki valinn og aðgerðaboðin eru annað hvort **Hætta** við eða **Breyta magni**.  

#### <a name="calculating-the-planning-line-quantity"></a><a name="calculating-the-planning-line-quantity"></a>Útreikningur á magni áætlunarlínu

Magn á áætlunarlínu er reiknað á eftirfarandi hátt:

Áætlunarlínumagn = Magn gildandi framboðs – (áætlaðar birgðir – yfirflæðisstig)  

> [!NOTE]  
> Fyrir sAs með öllum viðvörunarlínum er hámark og lágmark pöntunarmagns og margra pantana hunsuð.  

#### <a name="defining-the-action-message-type"></a><a name="defining-the-action-message-type"></a>Skilgreina tegund aðgerðaboða

* Ef magn áætlunarlínu er meira en 0 eru **aðgerðaboðin Breyta magni**.  
* Ef magn áætlunarlínu er jafnt og eða minna en 0 eru aðgerðaboðin **Hætta við**  

#### <a name="composing-the-warning-message"></a><a name="composing-the-warning-message"></a>Að búa til viðvörunarskilaboð

Ef frárennslislagnir eru í  **verði birtir óbirtar Áætlunareiningar**  með viðvörunarboðum með eftirfarandi upplýsingum:  

* Áætlað birgðastig sem setti af stað viðvörunina.  
* Reiknaða yfirflæðisstigið  
* Gjalddagi framboðsatvika  

Dæmi Áætlaðar birgðir 120 eru meiri en yfirflæðisstigið 60 á 01-28-23  

### <a name="example-scenario"></a><a name="example-scenario"></a>Dæmi um atburðarás

Í þessari atburðarás, breytir viðskiptamaður sölupöntun frá 70 í 40 stykki milli tveggja áætlunarkeyrslna. Yfirstraumsmöguleika dregur úr innkaupum sem var stungið upp á upphaflegu sölumagni.  

#### <a name="item-setup"></a><a name="item-setup"></a>Vöruuppsetning

|Endurpöntunarstefna|Hámarksmagn|  
|-----------------------|------------------|  
|Hámarksmagn pöntunar|100%|  
|Endurpöntunarmark|50|  
|Birgðir|80|  

#### <a name="situation-before-sales-decrease"></a><a name="situation-before-sales-decrease"></a>Staða fyrir söluminnkun

|Atburður|Breyta magni|Áætlaðar birgðir|  
|-----------|-----------------|-------------------------|  
|Dagur eitt|Ekkert|80|  
|Sala|-70|10|  
|Lok tímaramma|Ekkert|10|  
|Leggja til nýja innkaupapöntun|+90|100%|  

#### <a name="situation-after-sales-decrease"></a><a name="situation-after-sales-decrease"></a>Staða eftir söluminnkun

|Breyting|Breyta magni|Áætlaðar birgðir|  
|------------|-----------------|-------------------------|  
|Dagur eitt|Ekkert|80|  
|Sala|-40|40|  
|Innkaup|+90|130|  
|Lok tímaramma|Ekkert|130|  
|Stinga upp á að minnka innkaup<br><br> panta frá 90 til 60|-30|100|  

#### <a name="resulting-planning-lines"></a><a name="resulting-planning-lines"></a>Áætlunarlínur sem leiða

Kerfið stofnar viðvörunaráætlunarlínu til að minnka innkaupin um 30, úr 90 í 60, til að halda áætluðum birgðum á 100 í samræmi við yfirstraumskerfið.  

![Áætla samkvæmt yfirflæðisstigi.](media/nav_app_supply_planning_2_overflow2.png "Áætla samkvæmt yfirflæðisstigi")  

> [!NOTE]  
> Án yfirstraumseiginleikinn er engin viðvörun stofnuð ef áætluð birgðastig eru umfram hámarkið sem gæti valdið því að auka framboðið um 30.

## <a name="handling-projected-negative-inventory"></a><a name="handling-projected-negative-inventory"></a>Meðhöndlun áætlaðra neikvæðra birgða

Endurpöntunarmarkið endurspeglar ætlaða eftirspurn á afhendingartíma vörunnar. Áætlaðar birgðir verða að vera nógu stórar til að ná eftirspurninni þangað til ný pöntun berst. Á meðan ættu öryggisbirgðir að uppfylla sveiflur í eftirspurn að áætluðu þjónustustigi.  

Áætlunarkerfið telur það neyðartilvik ef ekki er hægt að bera framtíðareftirspurn fram úr áætluðum birgðum. Eða tilgreint á annan hátt, að áætlaðar birgðir fari neikvæðar úr. Kerfið bendir á að stofnuð hafi verið ný framboðtil að ná yfir óuppfyllta hluta eftirspurnarinnar. Stærð nýja framboðshurðarinnar mun ekki íhuga Hámarksbirgðir eða pöntunarmagn né breytir eftirfarandi pöntunarbreyti:

* Hámarksmagn pöntunar
* Lágmarksmagn pöntunar
* Fjöldapanta 

Þess í stað endurspeglar það nákvæman skort.  

Áætlunarlínan fyrir þessa gerð framboðapöntun mun birta  **neyðarviðvörunarteikn**  til að fá frekari upplýsingar um ástandið.  

Í eftirfarandi mynd er framboð D táknar neyðarlínu til að leiðrétta neikvæðar birgðir.  

![Viðbragðsáætlun til að koma í veg fyrir neikvæða birgðastöðu.](media/nav_app_supply_planning_2_negative_inventory.png "Viðbragðsáætlun til að koma í veg fyrir neikvæða birgðastöðu")  

1. Framboð **A**, fyrstu áætlaðar birgðir, er undir pöntunarmark.  
2. Nýtt framsendingaráætlað framboð er stofnað (**C**).  

     (magn = Hámarksbirgðir – áætlað birgðastig)  
3. Framboð **A** er lokað með eftirspurn **B**, sem er ekki að öllu leyti annað.  

     (Krafa  **B**  gæti reynt að áætla framboð C í, en tíma-Bucket hindrar það.)  
4. Nýtt framboð (**D**) er stofnað til að uppfylla eftirstandandi magn eftirspurnar **B**  
5. Eftirspurn **B** er lokað (búa til áminningu fyrir áætluðum birgðum).  
6. Nýjar birgðir **D** eru lokaðar.  
7. Áætlaðar birgðir eru kannaðar. Ekki var farið yfir endurpöntunarpunktinn.  
8. Viðauka  **C**  er lokað (það er ekki meiri eftirspurn).  
9. Endanlegrar athugunar. Það eru engar útistandandi birgðastigáminningar.  

Í eftirfarandi kafla er fjallað um einkenni fjögurra studdra endurpöntunarstefna.

## <a name="reordering-policies"></a><a name="reordering-policies"></a>Endurpöntunarstefnur

Endurpöntunarstefnur skilgreina hversu mikið þarf að panta þegar vara þarf að vera fyllt á. Fjórir mismunandi endurröðunarstefnur eru til.  

### <a name="fixed-reorder-quantity"></a><a name="fixed-reorder-quantity"></a>Fast Endurpöntunarmagn

Regla um fast Endurpöntunarmagn er vanalega notuð við birgðaáætlanagerð fyrir vörur með eftirfarandi eiginleikum:

* Lágur birgðakostnaður
* Lítil hætta á Herta-
* Lítils fjölda atriða

Að jafnaði skal nota þessa reglu með endurpöntunarpunkti sem endurspeglar áætlaða eftirspurn á afhendingartíma vörunnar.  

#### <a name="calculated-per-time-bucket"></a><a name="calculated-per-time-bucket"></a>Reiknaður fyrir hvern tímaramma

Ef þú nærð í eða kropir á endurpöntunarpunkt í tímaramma (endurpöntunarhringrás) stingur kerfið upp á tveimur aðgerðum:

* Búa til nýja framboðapöntun fyrir endurpöntunarmagnið
* Áfram tímasett pöntunin frá fyrsta degi eftir lok tímarammans  

Í tímastillaði endurpöntunarpunkti fækkar fjölda framboðstillagna. Það endurspeglar ferli til að leita handvirkt að raunverulegu innihaldi hólfa í vöruhúsinu.  

#### <a name="creates-only-necessary-supply"></a><a name="creates-only-necessary-supply"></a>Skapar aðeins nauðsynlegt framboð

Áður en hann leggur fram nýtt framboðskerfi til að mæta endurpöntunaratriði athugar áætlanakerfið eftirfarandi framboð:

* Hvort framboð er þegar pantað
* Hvort gert sé ráð fyrir að fá framboðið innan afgreiðslutíma vörunnar

Kerfið stingur ekki upp á nýrri framboðapöntun ef framboð mun skila áætluðum birgðum á endurpöntunarstað innan afhendingartíma.  

Framboðspantanir sem eru stofnaðar sérstaklega til að mæta endurpöntunarpunkti eru undanskildar framboðsjöfnun og verða ekki breyttar. Ef óskað er eftir að verkfæra vöru sem hefur endurpöntunarpunkt er farið yfir útistandandi framboðspantanir handvirkt eða breytingu endurreisnarstefnunnar yfir í  **Lotu-fyrir-lotu**. Kerfið dregur úr eða hættir við auka framboð.  

#### <a name="combines-with-order-modifiers"></a><a name="combines-with-order-modifiers"></a>Sameinar með pöntunarbreyti

Lágmarks pöntunarmagn, magn Hámarkspöntunarinnar og röð margra pöntunarbreytta ætti ekki að gegna veigamiklu hlutverki þegar notað er fast pöntunarmagn. Áætlanakerfið tekur þó mið af því:

* Minnkið magnið í tilgreint Hámarksmagn pöntunarmagns (og stofnið tvær eða fleiri birgðir til að ná í heildarmagn pöntunar)
* Hækka skal pöntunina í tilgreint lágmarkspöntun magn
* Slétta pöntunarmagnið til að uppfylla tilgreinda pöntunarmargfeldi  

#### <a name="combines-with-calendars"></a><a name="combines-with-calendars"></a>Sameinar við dagatöl

Áður en ný framboðsathugun er gerð til að mæta endurpöntunarsjónarmiði athugar áætlanakerfið hvort pöntunin er áætluð fyrir hvern dag sem ekki er vinnudagur. Hann notar dagatölin sem tilgreind eru í  **reitnum kóti**  grunndagatals á  **upplýsingum**  og  **birgðageymsluspjaldinu**  fyrirtæki.  

Ef Áætluð dagsetning er ekki vinnudagur, færist áætlunarkerfið pöntunin fram á næsta vinnudag. Flutningur á dagsetningunni gæti orðið til í pöntun sem uppfyllir endurpöntunarstig en uppfyllir ekki ákveðna eftirspurn. Fyrir svona ójafna eftirspurn, býr áætlanakerfið til auka framboð.  

#### <a name="shouldnt-be-used-with-forecasts"></a><a name="shouldnt-be-used-with-forecasts"></a>Ætti ekki að nota með spám

Þar sem áætluð eftirspurn er þegar gefin upp í stigi endurpöntunarstigs er ekki nauðsynlegt að taka spá með í áætlanagerð. Ef það skiptir máli að byggja áætlunina á spá er notaður  **Lotu-fyrir-lotustefnuna** .  

#### <a name="must-not-be-used-with-reservations"></a><a name="must-not-be-used-with-reservations"></a>Má ekki nota með frátekningum

Ef magn hefur verið tekið frá, til dæmis magn í birgðum, vegna fjarlægrar eftirspurnar, gæti Skipulagsstofnun raskað. Jafnvel þótt áætlað birgðastig sé leyfilegt með tilliti til endurpöntunarmarks, má magnið ekki vera til staðar vegna frátekningarinnar. Kerfið gæti reynt að bæta úr því að stofna undantekningarpantanir. Hins vegar er mælt með því að  **reiturinn frátektir**  sé stilltur  **á aldrei**  á vörur sem eru áætlaðar með því að nota endurpöntunarpunkt.

### <a name="maximum-quantity"></a><a name="maximum-quantity"></a>Hámarksmagn

Reglan um hámarksmag er ein leið til að viðhalda birgðum með því að nota endurpöntunarmark.  

Allt sem gildir um stefnu endurpöntunarmagns gildir einnig um þessa stefnu. Eini munurinn er magnið sem lagt er til sem framboð. Þegar Hámarksmagn er notað verður Endurpöntunarmagn skilgreint breytilegt eftir áætluðu birgðastigi. Því er yfirleitt mismunandi eftir röð að panta.  

#### <a name="calculate-per-time-bucket"></a><a name="calculate-per-time-bucket"></a>Reikna á tímaramma

Þegar komið er til eða yfir endurpöntunarstað ákvarðar kerfið endurpöntunarmagnið við lok tímaramma. Það mælir bilið á milli núverandi áætlaðrar birgðastöðu og tilgreindra hámarksbirgða til að ákvarða magnið sem á að panta. Kerfið athugar þá:

* Hvort framboð er þegar pantað
* Hvort gert sé ráð fyrir að fá framboðið innan afgreiðslutíma vörunnar

Ef svo er minnkar kerfið magnið í nýju framboðapöntuninni með því magni sem þegar er pantað.  

Ef ekki er tilgreint hámarks birgðamagn, getur áætlanakerfið tryggt að áætlaðar birgðir ná endurpöntunarmagni.

#### <a name="combine-with-order-modifiers"></a><a name="combine-with-order-modifiers"></a>Sameina við pöntunarbreyti

Eftir uppsetningu gæti verið best að sameina Hámarksmagn reglu með pöntunarbreyti: 

* Til að tryggja lágmarks pöntunarmagn
* Slétta magnið í heiltölu innkaupamæmælieininga
* Skipta magninu í lotur eins og það er skilgreint með Hámarksmagn pöntunar  

### <a name="combine-with-calendars"></a><a name="combine-with-calendars"></a>Sameina við dagatöl

Áður en ný framboðsathugun er gerð til að mæta endurpöntunarsjónarmiði athugar áætlanakerfið hvort pöntunin er áætluð fyrir hvern dag sem ekki er vinnudagur. Það notar dagatölin sem tilgreind eru í  **reitnum kóti**  grunndagatals á  **upplýsingum**  og  **birgðageymsluspjaldinu**  fyrirtæki.  

Ef Áætluð dagsetning er ekki vinnudagur, færist áætlunarkerfið pöntunin fram á næsta vinnudag. Flutningur á dagsetningunni gæti orðið til í pöntun sem uppfyllir endurpöntunarstig en uppfyllir ekki ákveðna eftirspurn. Fyrir svona ójafna eftirspurn, býr áætlanakerfið til auka framboð.

### <a name="order"></a><a name="order"></a>Pöntun

Í Make-up-pöntunarumhverfi er vara keypt eða framleidd til að ná fram ákveðinni eftirspurn. Algengast er að Endurpöntunarstefna pöntunar sé notuð fyrir vörur með eftirfarandi eiginleikum

* Eftirspurn er ótíð
* Afhendingartíminn er óverulegur
* Nauðsynlegar eigindir eru breytilegar  

[!INCLUDE [prod_short](includes/prod_short.md)] stofnar pöntunartengingu sem virkar eins og bráðabirgðartenging milli framboðs (framboðapöntun eða birgða) og eftirspurnar. Hægt er að sækja um pöntunartengingu á meðan á áætlanagerð stendur á eftirfarandi hátt:  

* Þegar notuð er framleiðslustefnu til pöntunar til að stofna fjölstig eða gerð framleiðslupantana (framleiða íhluti í sömu framleiðslupöntun)  
* Þegar sölupöntunaráætlun er notuð til að stofna framleiðslupöntun úr sölupöntun  

> [!TIP]
> Ef vörumerseigindir hafa ekki verið breytilegir er kannski best að nota reglu mikið-fyrir-lotu endurpöntunarstefnu. Þar af leiðandi notar kerfið óáætlaðar birgðir og safnar aðeins saman sölupöntunum með sömu afhendingardagsetningu eða innan skilgreindra tímaramma.  

#### <a name="order-to-order-links-and-past-due-dates"></a><a name="order-to-order-links-and-past-due-dates"></a>Tenglar til pöntunartengla og eldri Gjalddagar

Ólíkt flestum framboð-eftirspurn settum eru tengdar pantanir með skiladag á undan upphafsdagsetningu áætlunar áætlaðar að fullu af kerfinu. Ástæðan fyrir þessari undantekningu er sú að samstilla þarf ákveðin eftirspurnarframboðstilstæður. Til að fræðast meira um frosksvæðið sem á við um flestar eftirspurnargerðir er farið í að  [vinna pantanir á undan upphafsdagsetningunni](design-details-balancing-demand-and-supply.md#process-orders-before-the-planning-start-date) áætlunar.

### <a name="lot-for-lot"></a><a name="lot-for-lot"></a>Lota fyrir lotu

Lotu-fyrir-lotu-stefnu er sveigjanlegasta því kerfið bregst aðeins við raunverulegri eftirspurn. Það virkar á áætlaða eftirspurn frá spá og standandi pöntunum og jafnar síðan pöntunarmagnið á grundvelli eftirspurnar. Stefnan er ætluð fyrir vörur þar sem hægt er að samþykkja birgðir en það ætti að forðast.  

Að sumu leyti er regla um lotu-fyrir-lotu líkt við Pöntunarstefnuna. Það getur tekið við magni í birgðum og það bútað eftirspurn og framboði í tímans fötum sem þú skilgreinir.

Tímarammanum er tilgreindur í  **reitnum tímarammi**  á  **síðunni birgðaspjald** . Lágmarksstærð tímaramma er einn dagur því það er Minnsti Tímamælieining á eftirspurn og framboðstilvikum í [!INCLUDE [prod_short](includes/prod_short.md)].  

Tímaramminn takmarkar einnig það hvenær eigi að endurraða framboðinu til að mæta tiltekinni eftirspurn. Framboðs innan tímarammans er endurraðað í eða úr til að mæta eftirspurninni. Fyrri birgðir munu valda aukbirgðum og það ætti að hætta við. Fyrir framboð sem síðar er búin til ný framboðapöntun.  

Með þessari stefnu er hægt að tilgreina öryggisbirgðir til að bæta fyrir breytingar í framboði eða til að mæta skyndilegri eftirspurn. Lotu-fyrir-lotustefnuna getur einnig verið hömlulaus tímabil og magn til að stytta röðun pöntunar.  

 **Í reitnum endurröðunartímabil**  er reiturinn lota uppsöfnuð  **,**  sem stuðlar að því að skilgreina endurpöntunarferlið. Frá dagsetningu fyrstu eftirspurnar safnast allar kröfur í næsta lotu uppsöfnuð tímabil í eina framboðsuppröð á dagsetningu fyrstu eftirspurnar. Eftirspurn sem er utan lotuuppsöfnunartímabilsins nær ekki yfir framboðsuppröð.

Þar sem magn framboðs er byggt á raunverulegri eftirspurn getur það haft vit á að nota pöntunarbreyti:

* Slétta pöntunarmagnið til að uppfylla pöntunarmargfeldi pöntunar (eða innkaupamælieiningu)
* Hækka pöntun í ákveðið lágmarkspöntun
* Minnkaðu magnið í tilgreint Hámarksmagn (og Búðu þannig til tvær eða fleiri birgðir til að ná í heildarmagn sem þarf)

## <a name="see-also"></a><a name="see-also"></a>Sjá einnig

[Hönnunarupplýsingar: áætlunarfæribreyta](design-details-planning-parameters.md)  
[Hönnunarupplýsingar: áætlunartafla](design-details-planning-assignment-table.md)  
[Hönnunarupplýsingar: Miðlægar hugmyndir áætlanakerfisins](design-details-central-concepts-of-the-planning-system.md)  
[Hönnunarupplýsingar: Jöfnun eftirspurn og framboð](design-details-balancing-demand-and-supply.md)  
[Hönnunarupplýsingar: framboðsáætlun](design-details-supply-planning.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
