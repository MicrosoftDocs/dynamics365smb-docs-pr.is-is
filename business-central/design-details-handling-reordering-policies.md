---
title: Hönnunarupplýsingar - Meðhöndlun endurpöntunarstefnur
description: Þessi grein gefur yfirlit yfir endurpöntunarefnin sem nota má í áætlun framboðs.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: conceptual
ms.date: 02/24/2023
ms.custom: bap-template
---
# Hönnunarupplýsingar: Meðhöndlun endurpöntunarstefnur

Til að taka með vöru með í birgðaáætlanagerð þarf að tilgreina endurpöntunarstefnu fyrir hana á  **síðunni birgðaspjald** . Eftirfarandi endurpöntunarstefnur eru tiltækar:  

* Fast endurpöntunarmagn  
* Hámarksmagn  
* Pöntun  
* Lotu-fyrir-lotu  

 **Fast Endurpöntunarmagn.**  og  **Hámarksmagn**  stefnur tengjast birgðaáætlanagerð. Þessar stefnur eru með skref-fyrir-skref-jöfnun framboðs og pöntunar.  

## Hlutverk endurpöntunarpoint

Endurpöntunarmark stendur fyrir eftirspurn á afhendingartíma. Þegar birgðir eru áætlaðar til að fara yfir stigið sem er skilgreint af endurpöntunarefninu er kominn tími til að panta meira. Birgðir minnka smám saman þar til Áfylling kemur. Það gæti náð núlli eða öryggisbirgðastigi. Áætlunarkerfið stingur upp á fyrirfram röðuðu framboðinu á punktinn þegar birgðirnar fara fyrir neðan endurpöntunarpunktinn.  

Birgðastig geta farið verulega í tímarammanum. Þess vegna fylgist áætlanakerfið stöðugt að tiltækum birgðum.

## Vöktun áætlaðra birgðastita og endurpöntunarsjónarmiða

Birgðir eru tegund af framboði, en fyrir birgðaáætlanagerð, greinir áætlanakerfið milli tveggja birgðastiga:  

* Áætlaðar birgðir  
* Áætlaðar tiltækar birgðir  

### Áætlaðar birgðir  

Í upphafi áætlunarferlis eru áætlaðar birgðir brúttó magn birgða. Brúttómagnið inniheldur bókað og sent framboð og eftirspurn í fortíðinni. Þetta magn verður áætlað birgðastig sem brúttómagn frá framtíðar framboði og þörfum er viðhaldið. Framtíðarframboð og eftirspurn eru kynnt meðfram tímalínunni, hvort sem er frátekið eða úthlutað með öðrum hætti.  

Áætlanakerfið notar áætlaðar birgðir til að fylgjast með endurpöntunarefninu og ákvarða pöntunarmagnið með því að nota  **Hámarksmagn.**  endurpöntunarstefnu.  

### Áætlaðar tiltækar birgðir  

Áætlaðar tiltækar birgðir eru birgðir sem eru tiltækar til að uppfylla eftirspurn á tilteknum tímapunkti. Áætlanakerfið notar áætlaðar tiltækar birgðir þegar verið er að vakta öryggisbirgðastig. Öryggisbirgðir verða ávallt að vera tiltækar fyrir óvænta eftirspurn.  

### Tímafötur  

Áætlaðar birgðir eru mikilvægar uppgötvun þegar pöntunarpunkti er náð eða yfir og til að reikna rétt pöntunarmagn þegar notað er  **Hámarksmagn.**  endurpöntunarstefnu.  

Áætlað birgðastig er reiknað við upphaf áætlunartímabilsins. Það er brúttóstigi sem telur ekki til frátekningar eða annarra úthlutana. Til að fylgjast með þessu birgðastigi við áætlunarröðina fylgist áætlanakerfið eftir uppsöfnuðum breytingum yfir tímabil. Það tímabil kallast  *tímarammi*. Til að fræðast meira um tímafötur er farið í  [tímafötur](#time-buckets). Áætlanakerfið tryggir að tímarammi sé a.m.k. einn dagur. Einn dagur er lágmarkseiningaeining vegna eftirspurnar-eða framboðsatvika.  

### Ákvarða áætlað birgðastig  

Eftirfarandi röð lýsir því hvernig áætlanakerfið ákvarðar áætlað birgðastig:  

* Þegar framboðsatburður er að fullu Áætlaður, eins og innkaupapöntun, eykur það áætlaðar birgðir á gjalddaga viðburðarins.  
* Þegar eftirspurnartilvik er fullkomlega fullnægjandi minnkar það áætlaðar birgðir strax. Þess í stað bókar hún minnkaða áminningu, sem er innri færsla sem inniheldur dagsetningu og magn viðbóta við áætlaðar birgðir.  
* Þegar seinna framboðsatvik er áætlað og bætt við tímalínu kannar kerfið bókaðar minnkun áminningar um einn til áætlaðrar dagsetningar framboðins. Meðan á þessu ferli stendur gæti endurpöntunarstig innri aukningar áminningarinnar náð til eða farið yfir þau.  
* Ef ný framboðsathugun er kynnt athugar hún hvort hún sé slegin inn á undan núverandi framboði. Ef svo er, verður nýja framboðið núverandi framboð og Jöfnunaraðferðin endurræst.  

Eftirfarandi mynd sýnir þessa meginreglu.  

![Ákvarða áætlaðar birgðir.](media/nav_app_supply_planning_2_projected_inventory.png "Ákvarða áætlaðar birgðir")  

1. Framboð **Sa** af 4 (fast) lokar Eftirspurn **Da** af -3.  
2. CloseDemand: Búa til lækkunaráminningu -3 (ekki sýnt).  
3. Framboði  **SA**  er lokað með umfjallanir um 1 (það er ekki meiri eftirspurn).  

     Áætlað birgðastig hækkar í + 4 á meðan áætlaðar  **tiltækar**  Birgðir verða-1.  

4. Næsta eftirspurn **Sb** af 2 (önnur pöntun) hefur þegar verið sett á tímalínuna.  
5. Áætlunarkerfið leitar að minnkum áminningum áður en  **sb**  (í þessu dæmi er ekki svo að engin aðgerð sé tekin).  
6. Áætlanakerfið lokar framboði  **sb**  (ekki er þörf á meiri eftirspurn) við annað hvort A, draga frá það á 0 (hætta við) eða B, með því að fara eftir því eins og er.  

     Áætlað birgðastig hækkar (A: + 0 = > + 4 eða B: + 2 = + 6).  

7. Áætlanakerfið gerir lokaathugun. Er einhver lækkun áminning? Já, það er eitt á dagsetningunni **Da**.  
8. Áætlanakerfið bætir minnkaðri áminningu um-3 áminningu á áætluðu birgðastigi, annaðhvort A: + 4 -3 = 1 eða B: + 6 -3 = + 3.  
9. Fyrir A stofnar áætlanakerfið framáætlaða pöntun sem er ræst á degi  **da**. Fyrir B er endurpöntunarpunkti náð og ný pöntun er stofnuð.

## Hlutverk tímarammans

Tilgangurinn með tímarammanum er að safna saman eftirspurnartilvikum innan tímasíðunnar til að útbúa sameiginlega birgðapöntun.  

Fyrir endurpöntunarstefnur sem nota endurpöntunarmark er hægt að skilgreina tímaramma. Tímafötur hjálpa til við að tryggja að kröfuhafar innan sama tímabils séu uppsafnaðra. Kerfið athugaði síðan áhrifin á áætlaðar birgðir og hvort endurpöntunarpunktur hafi verið liðinn.

Ef komið er framhjá endurpöntunarpunkti raðar kerfið nýrri framboðapöntun úr lok tímarammans. Tímaskeið í fötum byrja á upphafsdegi áætlunar.  

Hugtak tímarammans endurspeglar handvirka ferlið við að athuga birgðastig á tíddum grunni frekar en fyrir hverja færslu. Tíðnin er skilgreind (tímarammans). Til dæmis væri hægt að safna öllum vöruþörfum frá lánardrottni til að setja vikulega pöntun.  

![Dæmi um tímaramma í skipulagningu.](media/nav_app_supply_planning_2_reorder_cycle.png "Dæmi um tímaramma í skipulagningu")  

Tímafötur eru oft notaðar til að forðast Cascade áhrif. Til dæmis jöfn lína framboðs og eftirspurnar þar sem fyrri eftirspurn er afturkölluð eða ný búin til. Niðurstaðan ætti að vera sú að framboðspöntunin (nema sú síðasta) er enduráætluð.

## Vera undir yfirstigi

Þegar Hámarksmagn er  **notað.**  og  **Fast Endurpöntunarmagn.**  endurpöntunarstefnu, leggur áætlanakerfið áherslu á áætlaðar birgðir í uppgefin tímafötu eingöngu. Það gæti stungið upp á auka framboði þegar neikvæð eftirspurn eða jákvæð framboð breytinga gerast utan tímarammans. Fyrir auka framboð reiknar áætlanakerfið magnið með því að lækka framboðið. Þetta magn er kallað „yfirflæðisstig“. Yfirflæði er tiltækt sem áætlunarlína með  **Breytingarmagni (minnkun)**  eða  **Hætta**  við aðgerð og eftirfarandi viðvörunarskilaboðum:  

* Takið eftir: áætlaðar birgðir [XX] eru hærri en yfirstraumstigið [XX] á gjalddaga [XX]. *  

![Yfirflæðisstig birgða.](media/supplyplanning_2_overflow1_new.png "Yfirflæðisstig birgða")  

### Útreikningur á yfirstraumstigi  

Yfirstraumstigið er reiknað með mismunandi hætti eftir endurpöntunarstefnunni.  

#### Hámarksmagn

Frárennslisstig = Hámarksbirgðir  

> [!NOTE]  
> Ef lágmarks pöntunarmagn er notað er því bætt við á eftirfarandi hátt:
>
> Frárennslisstig = Hámarksbirgðir + lágmarks pöntunarmagn.  

#### Fast endurpöntunarmagn  

Yfirstraumsmagn = endurskipuleggja magn + endurpöntunarstig  

> [!NOTE]  
> Ef lágmarks pöntunarmagn er hærra en endurpöntunarstig er því skipt út á eftirfarandi hátt:
>
> Frárennslisstig = Endurpöntunarmagn + lágmarksmagn pöntunar  

#### Fjöldapanta  

Ef pöntunarmargfeldi er til, leiðréttir það yfirstraumshæð fyrir bæði Hámarksmagn og fast magn endurpöntunarmagns.  

### Stofnun áætlunarlínunnar með viðvörun um straumleysi  

Áætlunarlína er stofnuð þegar framboð veldur því að áætlaðar birgðir verða hærri en yfirstraumstigið við lok tímaramma. Til að vara við auka framboði hefur áætlunarlínan viðvörunarboð,  **reiturinn Samþykkja aðgerðaboð**  hefur ekki verið valinn og aðgerðaboð eru annað hvort  **hætt við**  eða  **skipt um magn.**  

#### Reiknar út magn áætlunarlínu  

Magnið í áætlunarlínu er reiknað út á eftirfarandi hátt:

Magn áætlunarlínu = núverandi framboðsmagn – (áætlað birgðir – yfirrennslisstig)  

> [!NOTE]  
> Fyrir sAs með allar viðvörunarlínur er hámarks-og lágmarkspöntun magnið hunsað.  

#### Skilgreining gerðar aðgerðabota  

* Ef áætlunarlínumagnið er hærra en 0, er  **aðgerðaboðinn breyta magni.**  
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
|Stinga upp á að minnka innkaup<br><br> panta frá 90 til 60|-30|100%|  

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

### Lotu-fyrir-lotu

Lotu-fyrir-lotu-stefnu er sveigjanlegasta því kerfið bregst aðeins við raunverulegri eftirspurn. Það virkar á áætlaða eftirspurn frá spá og standandi pöntunum og jafnar síðan pöntunarmagnið á grundvelli eftirspurnar. Stefnan er ætluð fyrir vörur þar sem hægt er að samþykkja birgðir en það ætti að forðast.  

Að sumu leyti er Lotun-fyrir-Lotunstefnunni líkt við Pöntunarstefnuna en hún hefur almenna nálgun að atriðum. Það getur tekið við magni í birgðum og það bútað eftirspurn og framboði í tímans fötum sem þú skilgreinir.  

Tímarammanum er tilgreindur í  **reitnum tímarammi**  á  **síðunni birgðaspjald** . Lágmarksstærð tímaramma er einn dagur því það er Minnsti Tímamælieining á eftirspurn og framboðstilvikum í [!INCLUDE [prod_short](includes/prod_short.md)].  

Tímaramminn takmarkar einnig það hvenær eigi að endurraða framboðinu til að mæta tiltekinni eftirspurn. Framboðs innan tímarammans er endurraðað í eða úr til að mæta eftirspurninni. Fyrri birgðir munu valda aukbirgðum og það ætti að hætta við. Fyrir framboð sem síðar er búin til ný framboðapöntun.  

Með þessari stefnu er hægt að tilgreina öryggisbirgðir til að bæta fyrir breytingar í framboði eða til að mæta skyndilegri eftirspurn.  

Þar sem magn framboðanna er byggt á raunverulegri eftirspurn getur það haft vit á að nota pöntunarbreytin:

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