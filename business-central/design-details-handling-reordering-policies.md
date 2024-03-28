---
title: Hönnunarupplýsingar - Meðhöndlun endurpöntunarstefnur
description: Þessi grein gefur yfirlit yfir endurpöntunarstefnur sem hægt er að nota í framboðsáætlun.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.date: 02/24/2023
ms.custom: bap-template
ms.service: dynamics-365-business-central
---
# Hönnunarupplýsingar: Meðhöndlun endurpöntunarstefnur

Til að hafa vöru með í birgðaáætlun verður að tilgreina endurpöntunarstefnu fyrir hana á **síðunni Birgðaspjald** . Eftirfarandi endurpöntunarreglur eru tiltækar:  

* Fast endurpöntunarmagn  
* Hámarksmagn  
* Röð  
* Lota fyrir lotu  

Fast **endurpöntunarmagn** og **hámarksmagn.** Reglur tengjast birgðaáætlun. Þessar reglur eru samhliða skref-fyrir-skref jafnvægi á framboði og pöntunarrakningu.  

## Hlutverk endurpöntunarmarks

Endurpöntunarmark stendur fyrir eftirspurn á afhendingartíma. Þegar áætlað er að birgðir fari niður fyrir það stig sem endurpöntunarmarkið skilgreinir er kominn tími til að panta meira. Birgðir minnka smám saman þar til áfylling berst. Það gæti náð núlli eða öryggisbirgðum. Áætlunarkerfið stingur upp á framáætlaðri framboðspöntun á þeim tímapunkti þegar birgðir fara yfir fyrir endurpöntunarmark.  

Birgðastig geta færst verulega í tímarammanum. Þess vegna fylgist áætlunarkerfið stöðugt með tiltækum birgðum.

## Eftirlit með áætluðu birgðastigi og endurpöntunarmarki

Birgðir eru tegund af framboði, en fyrir birgðaáætlanagerð, greinir áætlanakerfið milli tveggja birgðastiga:  

* Áætlaðar birgðir  
* Áætlaðar tiltækar birgðir  

### Áætlaðar birgðir  

Í upphafi áætlunarferlisins eru áætlaðar birgðir brúttómagn birgða. Brúttómagnið inniheldur bókað og óbókað framboð og eftirspurn í fortíðinni. Þetta magn verður áætlað birgðastig sem brúttómagn úr framtíðarframboði og eftirspurn viðhalda. Framtíðarframboð og eftirspurn eru kynnt á tímalínunni, hvort sem þau eru frátekin eða úthlutað á annan hátt.  

Áætlunarkerfið notar áætlaðar birgðir til að vakta endurpöntunarmarkið og ákvarða endurpöntunarmagnið með því að nota reitinn **Hámarksmagn.** endurröðun stefnu.  

### Áætlaðar tiltækar birgðir  

Áætlaðar tiltækar birgðir eru birgðir sem eru tiltækar til að uppfylla eftirspurn á tilteknum tímapunkti. Áætlunarkerfið notar áætlaðar tiltækar birgðir við eftirlit með öryggisbirgðastigi. Öryggisbirgðir verða alltaf að vera tiltækar fyrir óvænta eftirspurn.  

### Tímarammar  

Varpaðar birgðir eru mikilvægar til að greina hvenær endurpöntunarmarki er náð eða farið yfir hann og til að reikna út rétt pöntunarmagn þegar Hámarksmagn er notað **.** endurröðun stefnu.  

Áætlað birgðastig er reiknað í upphafi áætlunartímabilsins. Það er brúttóstig sem tekur ekki tillit til bókana eða annarra úthlutana. Til að fylgjast með þessu birgðastigi í áætlunarröðinni fylgist áætlunarkerfið með uppsöfnuðum breytingum yfir tímabil. Það tímabil er kallað *tímafötu*. Til að læra meira um tímafötu, farðu í [Hlutverk tímarammans](#the-role-of-the-time-bucket). Áætlunarkerfið tryggir að tímaramminn sé að minnsta kosti einn dagur. Einn dagur er lágmarks tímaeining fyrir eftirspurnar- eða framboðstilvik.  

### Ákvörðun áætlaðs birgðastigs  

Eftirfarandi röð lýsir því hvernig áætlunarkerfið ákvarðar áætlað birgðastig:  

* Þegar birgðatilvik er fyllilega áætlað, eins og innkaupapöntun, eykur það áætlaðar birgðir á gjalddaga tilviksins.  
* Þegar eftirspurnartilvik er að fullu uppfyllt minnkar það ekki áætlaðar birgðir strax. Þess í stað bókar það minnkunaráminningu, sem er innri færsla sem inniheldur dagsetningu og magn viðbótarinnar við áætlaðar birgðir.  
* Þegar seinna birgðatilvik er áætlað og bætt við tímalínuna, rannsakar kerfið bókaðar áminningar um lækkun, eina af annarri til áætlaðrar dagsetningar framboðs. Á meðan á þessu ferli stendur gæti endurpöntunarmarki innri áminningar um aukningu verið náð eða það strikað yfir.  
* Ef ný framboðspöntun er kynnt, athugar hún hvort hún er færð inn á undan gildandi framboði. Ef svo er verður nýja framboðið núverandi framboð og jöfnunarferlið hefst á ný.  

Eftirfarandi mynd sýnir þessa meginreglu.  

![Ákvarða áætlaðar birgðir.](media/nav_app_supply_planning_2_projected_inventory.png "Ákvarða áætlaðar birgðir")  

1. Framboð **Sa** af 4 (fast) lokar Eftirspurn **Da** af -3.  
2. CloseDemand: Búa til lækkunaráminningu -3 (ekki sýnt).  
3. Framboð **Sa** er lokað með afgangi upp á 1 (það er ekki meiri eftirspurn).  

     Áætlað birgðastig eykst í +4 á meðan áætlaðar **tiltækar** birgðir verða -1.  

4. Næsta eftirspurn **Sb** af 2 (önnur pöntun) hefur þegar verið sett á tímalínuna.  
5. Áætlunarkerfið leitar að minnkunaráminningu á undan **Sb(** í þessu dæmi er það ekki, svo ekkert er gert).  
6. Áætlunarkerfið lokar framboði **Sb**  (ekki meiri eftirspurn er til staðar) með A, minnkar það í 0 (hætta við) eða B, með því að hafa það eins og það er.  

     Áætlað birgðastig eykst (A: +0 => +4 eða B: +2 = +6).  

7. Áætlunarkerfið gerir lokaathugun. Er einhver áminning um lækkun? Já, það er eitt á dagsetningunni **Da**.  
8. Áætlunarkerfið bætir minnkunaráminningu um -3 við áætlað birgðastig, annað hvort A: +4 -3 = 1 eða B: +6 -3 = +3.  
9. Fyrir A stofnar áætlunarkerfið framtímasetta pöntun sem hefst á dagsetningunni **Da**. Fyrir B er endurpöntunarmarki náð og ný pöntun stofnuð.

## Hlutverk tímarammans

Tilgangur tímarammans er að safna saman eftirspurnartilvikum innan tímabils til að gera sameiginlega framboðspöntun.  

Fyrir endurpöntunarstefnur sem nota endurpöntunarmark er hægt að skilgreina tímaramma. Tímarammar hjálpa til við að tryggja að kröfur innan sama tímabils safnist upp. Kerfið athugar síðan áhrifin á áætlaðar birgðir og hvort endurpöntunarmark hefur verið sent.

Ef farið er framhjá endurpöntunarmarki raðar kerfið áfram nýrri framboðspöntun frá lokum tímarammans. Tímarammar byrja á upphafsdagsetningu áætlunarinnar.  

Hugtakið tímarammi endurspeglar það handvirka ferli að athuga birgðastigið oft frekar en fyrir hverja færslu. Þú skilgreinir tíðnina (tímarammann). Til dæmis gætirðu safnað saman öllum vöruþörfum frá lánardrottni til að leggja inn vikulega pöntun.  

![Dæmi um tímaramma í skipulagningu.](media/nav_app_supply_planning_2_reorder_cycle.png "Dæmi um tímaramma í skipulagningu")  

Tímarammar eru oft notaðir til að forðast keðjuverkun. Til dæmis jöfn lína framboðs og eftirspurnar þar sem fyrri eftirspurn er afturkölluð eða ný búin til. Niðurstaðan ætti að vera sú að framboðspöntunin (nema sú síðasta) er enduráætluð.

## Halda sig undir yfirfallsmörkum

Þegar Hámarksmagn er notað. **og** **Fast endurpöntunarmagn.** Endurpöntunarstefna, áætlanakerfið einblínir aðeins á áætlaðar birgðir í tilteknum tímaramma. Það gæti stungið upp á auknu framboði þegar neikvæð eftirspurn eða jákvæðar framboðsbreytingar eiga sér stað utan tímarammans. Fyrir aukið framboð reiknar áætlunarkerfið magnið sem minnka ætti framboð um. Þetta magn er kallað „yfirflæðisstig“. Yfirflæðið er tiltækt sem áætlunarlína með aðgerðinni **Breyta magni (Minnka)**  eða **Hætta við** og eftirfarandi viðvörunarskilaboðum:  

* Athugið: Áætlaðar birgðir [xx] eru hærri en yfirfallsstigið [xx] á gjalddaga [xx].*  

![Yfirflæðisstig birgða.](media/supplyplanning_2_overflow1_new.png "Yfirflæðisstig birgða")  

### Útreikningur yfirflæðisstigs  

Yfirflæðisstigið er reiknað út á mismunandi vegu eftir endurpöntunarstefnunni.  

#### Hámarksmagn

Yfirflæðisstig = hámarksbirgðir  

> [!NOTE]  
> Ef notað er lágmarkspöntunarmagn er því bætt við á eftirfarandi hátt:
>
> Yfirflæðisstig = hámarksbirgðir + lágmarksmagn pöntunar.  

#### Fast endurpöntunarmagn  

Yfirflæðisstig = endurpöntunarmagn + endurpöntunarmark  

> [!NOTE]  
> Ef lágmarkspöntunarmagn er meira en endurpöntunarmark er honum skipt út á eftirfarandi hátt:
>
> Yfirflæðisstig = endurpöntunarmagn + lágmarksmagn pöntunar  

#### Fjöldapanta  

Ef pöntunarmargfeldi er til leiðréttir hún yfirflæðisstigið fyrir bæði hámarksmagn og endurpöntunarstefnu fasts endurpöntunarmagns.  

### Áætlunarlínan stofnuð með yfirflæðisviðvörun  

Áætlunarlína er stofnuð þegar framboð veldur því að áætlaðar birgðir verða hærri en yfirflæðisstigið við lok tímarammans. Til að vara við auknu framboði fær áætlunarlínan viðvörunarboð, reiturinn **Samþykkja aðgerðaboð** er ekki valinn og aðgerðaboðin eru annað hvort **Hætta við** eða **Breyta magni.**  

#### Magn áætlunarlínunnar reiknað  

Magnið í áætlunarlínu er reiknað á eftirfarandi hátt:

Magn áætlunarlínu = núverandi framboðsmagn – (áætlaðar birgðir – yfirflæðisstig)  

> [!NOTE]  
> Fyrir sEins og með allar viðvörunarlínur er hámarks- og lágmarkspöntunarmagn og pöntunarmargfeldi hunsað.  

#### Skilgreining á gerð aðgerðaboða  

* Ef magnið í áætlunarlínunni er meira en 0 eru **aðgerðaboðin Breyta magni.**  
* Ef áætlunarlínumagnið er jafnt eða minna en 0 er  **hætt við að aðgerðaboðinn**  

#### Semja viðvörunarskilaboðin  

Ef frárennslislagnir eru í  **verði birtir óbirtar Áætlunareiningar**  með viðvörunarboðum með eftirfarandi upplýsingum:  

* Áætlað birgðastig sem setti af stað viðvörunina.  
* Reiknaða yfirflæðisstigið  
* Gjalddagi framboðsatvika  

Dæmi Áætlaðar birgðir 120 eru meiri en yfirflæðisstigið 60 á 01-28-23  

### Dæmi um atburðarás  

Í þessari atburðarás, breytir viðskiptamaður sölupöntun frá 70 í 40 stykki milli tveggja áætlunarkeyrslna. Yfirstraumsmöguleika dregur úr innkaupum sem var stungið upp á upphaflegu sölumagni.  

#### Vöruuppsetning  

|Endurpöntunarstefna|Hámarksmagn|  
|-----------------------|------------------|  
|Hámarksmagn pöntunar|100%|  
|Endurpöntunarmark|50|  
|Birgðir|80|  

#### Staða fyrir söluminnkun  

|Atburður|Breyta magni|Áætlaðar birgðir|  
|-----------|-----------------|-------------------------|  
|Dagur eitt|Ekkert|80|  
|Sala|-70|10|  
|Lok tímaramma|Ekkert|10|  
|Leggja til nýja innkaupapöntun|+90|100%|  

#### Staða eftir söluminnkun  

|Breyting|Breyta magni|Áætlaðar birgðir|  
|------------|-----------------|-------------------------|  
|Dagur eitt|Ekkert|80|  
|Sala|-40|40|  
|Innkaup|+90|130|  
|Lok tímaramma|Ekkert|130|  
|Stinga upp á að minnka innkaup<br><br> panta frá 90 til 60|-30|100|  

#### Áætlunarlínur sem leiða  

Kerfið stofnar viðvörunaráætlunarlínu til að minnka innkaupin um 30, úr 90 í 60, til að halda áætluðum birgðum á 100 í samræmi við yfirstraumskerfið.  

![Áætla samkvæmt yfirflæðisstigi.](media/nav_app_supply_planning_2_overflow2.png "Áætla samkvæmt yfirflæðisstigi")  

> [!NOTE]  
> Án yfirstraumseiginleikinn er engin viðvörun stofnuð ef áætluð birgðastig eru umfram hámarkið sem gæti valdið því að auka framboðið um 30.

## Meðhöndlun áætlaðra neikvæðra birgða

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

## Endurpöntunarstefnur

Endurpöntunarstefnur skilgreina hversu mikið þarf að panta þegar vara þarf að vera fyllt á. Fjórir mismunandi endurröðunarstefnur eru til.  

### Fast Endurpöntunarmagn

Regla um fast Endurpöntunarmagn er vanalega notuð við birgðaáætlanagerð fyrir vörur með eftirfarandi eiginleikum:

* Lágur birgðakostnaður
* Lítil hætta á Herta-
* Lítils fjölda atriða

Að jafnaði skal nota þessa reglu með endurpöntunarpunkti sem endurspeglar áætlaða eftirspurn á afhendingartíma vörunnar.  

#### Reiknaður fyrir hvern tímaramma  

Ef þú nærð í eða kropir á endurpöntunarpunkt í tímaramma (endurpöntunarhringrás) stingur kerfið upp á tveimur aðgerðum:

* Búa til nýja framboðapöntun fyrir endurpöntunarmagnið
* Áfram tímasett pöntunin frá fyrsta degi eftir lok tímarammans  

Í tímastillaði endurpöntunarpunkti fækkar fjölda framboðstillagna. Það endurspeglar ferli til að leita handvirkt að raunverulegu innihaldi hólfa í vöruhúsinu.  

#### Skapar aðeins nauðsynlegt framboð  

Áður en hann leggur fram nýtt framboðskerfi til að mæta endurpöntunaratriði athugar áætlanakerfið eftirfarandi framboð:

* Hvort framboð er þegar pantað
* Hvort gert sé ráð fyrir að fá framboðið innan afgreiðslutíma vörunnar

Kerfið stingur ekki upp á nýrri framboðapöntun ef framboð mun skila áætluðum birgðum á endurpöntunarstað innan afhendingartíma.  

Framboðspantanir sem eru stofnaðar sérstaklega til að mæta endurpöntunarpunkti eru undanskildar framboðsjöfnun og verða ekki breyttar. Ef óskað er eftir að verkfæra vöru sem hefur endurpöntunarpunkt er farið yfir útistandandi framboðspantanir handvirkt eða breytingu endurreisnarstefnunnar yfir í  **Lotu-fyrir-lotu**. Kerfið dregur úr eða hættir við auka framboð.  

#### Sameinar með pöntunarbreyti  

Lágmarks pöntunarmagn, magn Hámarkspöntunarinnar og röð margra pöntunarbreytta ætti ekki að gegna veigamiklu hlutverki þegar notað er fast pöntunarmagn. Áætlanakerfið tekur þó mið af því:

* Minnkið magnið í tilgreint Hámarksmagn pöntunarmagns (og stofnið tvær eða fleiri birgðir til að ná í heildarmagn pöntunar)
* Hækka skal pöntunina í tilgreint lágmarkspöntun magn
* Slétta pöntunarmagnið til að uppfylla tilgreinda pöntunarmargfeldi  

#### Sameinar við dagatöl  

Áður en ný framboðsathugun er gerð til að mæta endurpöntunarsjónarmiði athugar áætlanakerfið hvort pöntunin er áætluð fyrir hvern dag sem ekki er vinnudagur. Hann notar dagatölin sem tilgreind eru í  **reitnum kóti**  grunndagatals á  **upplýsingum**  og  **birgðageymsluspjaldinu**  fyrirtæki.  

Ef Áætluð dagsetning er ekki vinnudagur, færist áætlunarkerfið pöntunin fram á næsta vinnudag. Flutningur á dagsetningunni gæti orðið til í pöntun sem uppfyllir endurpöntunarstig en uppfyllir ekki ákveðna eftirspurn. Fyrir svona ójafna eftirspurn, býr áætlanakerfið til auka framboð.  

#### Ætti ekki að nota með spám  

Þar sem áætluð eftirspurn er þegar gefin upp í stigi endurpöntunarstigs er ekki nauðsynlegt að taka spá með í áætlanagerð. Ef það skiptir máli að byggja áætlunina á spá er notaður  **Lotu-fyrir-lotustefnuna** .  

#### Má ekki nota með frátekningum  

Ef magn hefur verið tekið frá, til dæmis magn í birgðum, vegna fjarlægrar eftirspurnar, gæti Skipulagsstofnun raskað. Jafnvel þótt áætlað birgðastig sé leyfilegt með tilliti til endurpöntunarmarks, má magnið ekki vera til staðar vegna frátekningarinnar. Kerfið gæti reynt að bæta úr því að stofna undantekningarpantanir. Hins vegar er mælt með því að  **reiturinn frátektir**  sé stilltur  **á aldrei**  á vörur sem eru áætlaðar með því að nota endurpöntunarpunkt.

### Hámarksmagn

Reglan um hámarksmag er ein leið til að viðhalda birgðum með því að nota endurpöntunarmark.  

Allt sem gildir um stefnu endurpöntunarmagns gildir einnig um þessa stefnu. Eini munurinn er magnið sem lagt er til sem framboð. Þegar Hámarksmagn er notað verður Endurpöntunarmagn skilgreint breytilegt eftir áætluðu birgðastigi. Því er yfirleitt mismunandi eftir röð að panta.  

#### Reikna á tímaramma

Þegar komið er til eða yfir endurpöntunarstað ákvarðar kerfið endurpöntunarmagnið við lok tímaramma. Það mælir bilið á milli núverandi áætlaðrar birgðastöðu og tilgreindra hámarksbirgða til að ákvarða magnið sem á að panta. Kerfið athugar þá:

* Hvort framboð er þegar pantað
* Hvort gert sé ráð fyrir að fá framboðið innan afgreiðslutíma vörunnar

Ef svo er minnkar kerfið magnið í nýju framboðapöntuninni með því magni sem þegar er pantað.  

Ef ekki er tilgreint hámarks birgðamagn, getur áætlanakerfið tryggt að áætlaðar birgðir ná endurpöntunarmagni.

#### Sameina við pöntunarbreyti

Eftir uppsetningu gæti verið best að sameina Hámarksmagn reglu með pöntunarbreyti: 

* Til að tryggja lágmarks pöntunarmagn
* Slétta magnið í heiltölu innkaupamæmælieininga
* Skipta magninu í lotur eins og það er skilgreint með Hámarksmagn pöntunar  

### Sameina við dagatöl

Áður en ný framboðsathugun er gerð til að mæta endurpöntunarsjónarmiði athugar áætlanakerfið hvort pöntunin er áætluð fyrir hvern dag sem ekki er vinnudagur. Það notar dagatölin sem tilgreind eru í  **reitnum kóti**  grunndagatals á  **upplýsingum**  og  **birgðageymsluspjaldinu**  fyrirtæki.  

Ef Áætluð dagsetning er ekki vinnudagur, færist áætlunarkerfið pöntunin fram á næsta vinnudag. Flutningur á dagsetningunni gæti orðið til í pöntun sem uppfyllir endurpöntunarstig en uppfyllir ekki ákveðna eftirspurn. Fyrir svona ójafna eftirspurn, býr áætlanakerfið til auka framboð.

### Pöntun

Í Make-up-pöntunarumhverfi er vara keypt eða framleidd til að ná fram ákveðinni eftirspurn. Algengast er að Endurpöntunarstefna pöntunar sé notuð fyrir vörur með eftirfarandi eiginleikum

* Eftirspurn er ótíð
* Afhendingartíminn er óverulegur
* Nauðsynlegar eigindir eru breytilegar  

[!INCLUDE [prod_short](includes/prod_short.md)] stofnar pöntunartengingu sem virkar eins og bráðabirgðartenging milli framboðs (framboðapöntun eða birgða) og eftirspurnar. Hægt er að sækja um pöntunartengingu á meðan á áætlanagerð stendur á eftirfarandi hátt:  

* Þegar notuð er framleiðslustefnu til pöntunar til að stofna fjölstig eða gerð framleiðslupantana (framleiða íhluti í sömu framleiðslupöntun)  
* Þegar sölupöntunaráætlun er notuð til að stofna framleiðslupöntun úr sölupöntun  

> [!TIP]
> Ef vörumerseigindir hafa ekki verið breytilegir er kannski best að nota reglu mikið-fyrir-lotu endurpöntunarstefnu. Þar af leiðandi notar kerfið óáætlaðar birgðir og safnar aðeins saman sölupöntunum með sömu afhendingardagsetningu eða innan skilgreindra tímaramma.  

#### Tenglar til pöntunartengla og eldri Gjalddagar

Ólíkt flestum framboð-eftirspurn settum eru tengdar pantanir með skiladag á undan upphafsdagsetningu áætlunar áætlaðar að fullu af kerfinu. Ástæðan fyrir þessari undantekningu er sú að samstilla þarf ákveðin eftirspurnarframboðstilstæður. Til að fræðast meira um frosksvæðið sem á við um flestar eftirspurnargerðir er farið í að  [vinna pantanir á undan upphafsdagsetningunni](design-details-balancing-demand-and-supply.md#process-orders-before-the-planning-start-date) áætlunar.

### Lota fyrir lotu

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

## Sjá einnig  

[Hönnunarupplýsingar: áætlunarfæribreyta](design-details-planning-parameters.md)  
[Hönnunarupplýsingar: áætlunartafla](design-details-planning-assignment-table.md)  
[Hönnunarupplýsingar: Miðlægar hugmyndir áætlanakerfisins](design-details-central-concepts-of-the-planning-system.md)  
[Hönnunarupplýsingar: Jöfnun eftirspurn og framboð](design-details-balancing-demand-and-supply.md)  
[Hönnunarupplýsingar: framboðsáætlun](design-details-supply-planning.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]