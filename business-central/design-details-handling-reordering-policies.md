---
title: Hönnunarupplýsingar - Meðhöndlun endurpöntunarstefnu | Microsoft Docs
description: Yfirlit yfir verkhluta sem taka til skilgreininga á endurpöntunarstefnu í framboðsáætlun.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: f7d207d0f6e4730d900ce4214d7faa8c809ae8bd
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2020
ms.locfileid: "3185397"
---
# <a name="design-details-handling-reordering-policies"></a>Hönnunarupplýsingar: Meðhöndlun endurpöntunarstefnur
Til þess að vara geti tekið þátt í birgðaáætlunargerð verður að tilgreina endurpöntunarstefnu. Eftirfarandi fjórar endurpöntunarstefnur eru til:  

* Fast endurpöntunarmagn  
* Hámarksmagn  
* Röð  
* Lotu-fyrir-lotu  

Stefnur um fast endurpöntunarmagn og hámarksmagn tengjast birgðaáætlunargerð. Þó birgðaáætlanagerð sé tæknilega einfaldari en mótbókunaraðferð eru þessar stefnur báðar til með nákvæmri mótbókun framboðs og pöntunarrakningu. Til að stjórna samþættingu milli tveggja, og að veita sýnileika í þátt áætlanagerð rökfræði, strangar reglur gilda hversu endurröðun reglur eru meðhöndlaðar.  

## <a name="the-role-of-the-reorder-point"></a>Hlutverk endurpöntunarmarks
Í viðbót við almenna jafnvægi á framboð og eftirspurn, áætlanagerð kerfi verður einnig fylgjast birgðastigum fyrir viðkomandi vöru að virða skilgreind endurröðun stefnu.  

Endurpöntunarmark stendur fyrir eftirspurn á afhendingartíma. Þegar áætlaðar birgðir fara undir birgðastigið sem endurpöntunarmark skilgreinir er kominn tími til að panta meira magn. Á meðan eiga birgðir smám saman að minnka og mögulega ná núlli (eða öryggisbirgðastigi), þar til fyllt er á.  

Í samræmi mun áætlunarkerfið stinga upp á framboðspöntun sem er dagsett í framtíðinni á þeim tíma þegar áætlaðar birgðir fara undir endurpöntunarmark.  

Endurpöntunarmarkið endurspeglar tiltekið birgðastig. Hins vegar geta birgðastig hreyfst töluvert innan tímarammans og þess vegna verður áætlanakerfið að fylgjast stöðugt með áætluðum tiltækum birgðum.

## <a name="monitoring-the-projected-inventory-level-and-the-reorder-point"></a>Vöktun áætlaðs birgðastigs og endurpöntunarmarks
Birgðir eru tegund af framboði, en fyrir birgðaáætlanagerð, greinir áætlanakerfið milli tveggja birgðastiga:  

* Áætlaðar birgðir  
* Áætlaðar tiltækar birgðir  

### <a name="projected-inventory"></a>Áætlaðar birgðir  
Upphaflega áætlað birgðir er magn af vergri birgðum, þ.mt framboð og eftirspurn í fortíðinni, jafnvel þótt ekki bókað, þegar áætlanagerð er ræst. Í framtíðinni, verður þetta færanlegar áætlaðar birgðastig sem er viðhaldið af vergu magni frá síðara framboð og eftirspurn vegna þess að þeir eru kynnt eftir tímalínu (hvort sem er fráteknar eða öðrum hætti úthlutað).  

Áætlaðar birgðir skal nota af áætlanakerfinu þegar eftirlit er haft með endurpöntunarmarki og til að ákvarða endurpöntunarmang þegar endurpöntunarstefnan Hámarksmagn er notuð.  

### <a name="projected-available-inventory"></a>Áætlaðar tiltækar birgðir  
Áætlaðar tiltækar birgðir eru hluti af áætluðum birgðum sem eru tiltækar á einhverjum tilteknum tíma til að mæta eftirspurn. Áætlaðar tiltækar birgðir skal nota af áætlanakerfinu þegar eftirlit er haft með öryggisbirgðum.  

Áætlaðar tiltækar birgðir skal nota af áætlanakerfinu þegar eftirlit er haft með öryggisbirgðum, þar sem öryggisbirgðir þurfa alltaf að vera tiltækar til að mæta óvæntri eftirspurn.  

### <a name="time-buckets"></a>Tímarammar  
Góð stjórna á áætluðum birgðum er lykilatriði þegar greina á hvenær endurpöntunarmarki er náð og farið er yfir það og til að ákvarða rétt endurpöntunarmagn þegar endurpöntunarstefnan Hámarksmagn er notuð.  

Eins og fyrr segir er áætlað birgðastig reiknað í upphafi áætlunartímabilsins. Það er brúttó stig sem tekur ekki tillit til frátekninga og svipa‘ðra úthlutun. Til að fylgjast með þessu birgðastig á áætlunarröð, kerfið fylgist uppsöfnuðum breytingar yfir a tímabil , tímarammi. Kerfið tryggir að tímaramminn sé a.m.k. einn dagur þar sem það er nákvæmasta tímaeiningin fyrir birgðir eða eftirspurn.  

### <a name="determining-the-projected-inventory-level"></a>Ákvarða áætlaðar birgðir  
Eftirfarandi röð lýsir því hvernig áætlað birgðastig er ákvarðað:  

* Þegar framboðstilvik, svo sem innkaupapöntun, hefur verið algerlega skipulögð, mun það auka áætlaðar birgðir á skiladegi.  
* Þegar eftirspurnartilvik hefur verið að fullu uppfyllt, mun það ekki minnka áætlaðar birgðir strax. Í staðinn, bókar það minnkunaráminningu, sem er innri skrá sem geymir dagsetningu og magn af framlagi þess til áætlaðra birgða.  
* Þegar síðara framboðstilvik er skipulögð og sett á tímalínu, eru bókaðar minnkunaráminningar rannsakaðar eitt af öðru fram til fyrirhuguðum degi framboðs meðan áætlaðar birgðir eru uppfærðar. Á meðan á þessu ferli getur endurpöntunarmarki innri aukningaráminningar verið náð eða farið yfir það.  
* Ef ný birgðapöntun er innleidd athugar kerfið hvort hún sé færð inn á undan núverandi birgðum. Ef svo er verður nýja framboðið núverandi framboð og mótreikningsaðferðin hefst upp á nýtt.  

Eftirfarandi sýnir mynd af þessari meginreglu:  

![Ákvarða áætlaðar birgðir](media/nav_app_supply_planning_2_projected_inventory.png "Ákvarða áætlaðar birgðir")  

1. Framboð **Sa** af 4 (fast) lokar Eftirspurn **Da** af -3.  
2. CloseDemand: Búa til lækkunaráminningu -3 (ekki sýnt).  
3. Framboð **Sa** er lokað með afgangi upp á 1 (engin frekari eftirspurn er til).  

     Þetta eykur áætlað birgðastig í +4, á sama tíma og áætlaðar tiltækar birgðir **í boði** verða -1.  

4. Næsta eftirspurn **Sb** af 2 (önnur pöntun) hefur þegar verið sett á tímalínuna.  
5. Kerfið athugar hvort það sé einhver minnkunaráminning á undan **Sb** (það er ekki, þannig að ekki er gripið til aðgerða).  
6. Kerfið lokar framboði **Sb** (ekki fleiri eftirspurn) -annað hvort A: með því að minnka það til 0 hætta við eða B: með því að skilja eftir eins og er.  

     Þetta eykur áætlað birgðastig (A: +0 => +4 eða B: +2 = +6).  

7. Kerfið gerir endanlega athugum: Er einhver minnkunaráminning? Já, það er eitt á dagsetningunni **Da**.  
8. Kerfi bætir við minnkunaráminningu -3 við áætlað birgðastig, annað hvort A: +4 -3 = 1 eða B: +6 -3 = +3.  
9. Í tilviki A býr kerfið til framvirkt áætlaða pöntun sem hefst á degi **Da**  

     Í tilviki B er pöntunarmarki náð og ný pöntun er stofnuð.

## <a name="the-role-of-the-time-bucket"></a>Hlutverk tímaramma
Tilgangurinn með tímarammanum er að safna saman eftirspurnartilvikum innan tímasíðunnar til að útbúa sameiginlega birgðapöntun.  

Fyrir endurpöntunarstefnur sem nota endurpöntunarmark er hægt að skilgreina tímaramma. Þetta tryggir að eftirspurn innan sama tímabils sé safnað upp áður en áhrifin á áætlaðar birgðir eru könnuð, og hvort endurpöntunarmarki hafi verið náð. Ef farið er yfir endurpöntunarmarkið er ný birgðapöntun áætluð framvirkt frá lokum tímabilsins sem skilgreint er í tímarammanum. Tímaramminn hefst á upphafsdagsetningu áætlunar.  

Tímaramminn endurspeglar það handvirka ferli að kanna birgðastigið oft fremur en fyrir hverja færslu. Notandinn verður að tilgreina tíðnina (tímarammann). Til dæmis safnar notandinn saman öllum vöruþörfum frá einum lánardrottni til að leggja inn vikulega pöntun.  

![Dæmi um tímaramma í skipulagningu](media/nav_app_supply_planning_2_reorder_cycle.png "Dæmi um tímaramma í skipulagningu")  

Tímaramminn er vanalega notaður til að forðast keðjuverkun. Til dæmis jöfn lína framboðs og eftirspurnar þar sem fyrri eftirspurn er afturkölluð eða ný búin til. Niðurstaðan ætti að vera sú að framboðspöntunin (nema sú síðasta) er enduráætluð.

## <a name="staying-under-the-overflow-level"></a>Að vera undir yfirflæðisstigi
Þegar reglur um hámarksmagn og fast endurpöntunarmagn eru notaðar einblínir áætlanakerfið aðeins á ætlaðar birgðir í tilgreindum tímaramma. Þetta þýðir að áætlanakerfið geta stinga upp á óþarfa framboð þegar neikvæð eftirspurn eða jákvæðar breytingar á framboð koma fram utan ákveðins tímaramma. Ef, af þessum sökum, umframframboð er stungið upp á, reiknar áætlanagerðarkerfið hvaða magn framboðið skal minnka í (eða eytt) til að forðast umframframboð. Þetta magn er kallað „yfirflæðisstig“. Yfirflæðið er miðlað sem áætlanalína með **Breyta magni (Lækkun)** eða **Hætta við** aðgerð og eftirfarandi viðvörun skilaboð:  

*Athugið: Áætlaðar birgðir [xx] er hærra en yfirflæðisstig [xx] á gjalddaga [xx].*  

![Yfirflæðisstig birgða](media/supplyplanning_2_overflow1_new.png "Yfirflæðisstig birgða")  

###  <a name="calculating-the-overflow-level"></a>Reiknar yfirflæðisstig  
Yfirflæðisstigið er reiknað út á mismunandi hátt, allt eftir uppsetningu áætlana.  

#### <a name="maximum-qty-reordering-policy"></a>Endurpöntunarstefna fyrir Hámarksmagn  
Yfirflæðisstig = Hámarksbirgðir  

> [!NOTE]  
>  Ef lágmarkspöntunarmagn er til, þá verður því bætt við eins og hér segir: Yfirflæðisstig = Hámarksbirgðir + lágmarkspöntunarmagn.  

#### <a name="fixed-reorder-qty-reordering-policy"></a>Endurpöntunarstefna fasts endurpöntunarmagn  
Yfirflæðisstig = Endurpöntunarmagn + Endurpöntunarmark  

> [!NOTE]  
>  Ef lágmarkspöntunarmagn er yfir endurpöntunarmarkinu er því skipt út eins og hér segir: Yfirflæðisstig = Endurpöntunarmagn + lágmarkspöntunarmagn  

#### <a name="order-multiple"></a>Margföld pöntun  
Ef margföld pöntun er til mun hún leiðrétta yfirflæðisstigið fyrir endurpöntunarstefnurnar fyrir bæði hámarksmagn og fast endurpöntunarmagn.  

###  <a name="creating-the-planning-line-with-overflow-warning"></a>Stofna áætlunarlínu með yfirfallsviðvörun  
Þegar núverandi framboð veldur því að áætlaðar birgðir eru meiri en yfirflæðisstigið við lok tímaramma er búin til áætlunarlína. Til að vara við hugsanlega óþarft framboð, er áætlunarlínan með viðvörunarboð, **Samþykkja aðgerðaboð** reiturinn er ekki valinn, og aðgerðaboð eru annaðhvort Hætta við eða Breyta Magni.  

#### <a name="calculating-the-planning-line-quantity"></a>Reiknar magn áætlunarlínu  
Magn áætlunarlínu = Núverandi framboðsmagn – (Áætlaðar birgðir – Yfirflæðisstig)  

> [!NOTE]  
>  Eins og í öllum viðvörunarlínum verður hámarks-/lágmarkspöntunarmagn eða endurtekin pöntun hundsuð.  

#### <a name="defining-the-action-message-type"></a>Skilgreina tegund aðgerðaboða  

-   Ef magn áætlunarlínu er meira en 0 eru aðgerðaboðin Breyta magni.  
-   Ef magn áætlunarlínu er jafnt og eða minna en 0 eru aðgerðaboðin Hætta við.  

#### <a name="composing-the-warning-message"></a>Semja viðvörunarmerkið  
Í tilviki yfirflæðis birtir síðan **Óraktar áætlunareiningar** viðvörunarskilaboð með eftirfarandi upplýsingum:  

-   Áætlað birgðastig sem setti af stað viðvörunina.  
-   Reiknaða yfirflæðisstigið  
-   Lokadagur framboðstilviks.  

Dæmi Áætlaðar birgðir 120 eru meiri en yfirflæðisstigið 60 á 28-01-11  

### <a name="scenario"></a>Aðstæður  
Í þessari atburðarás, breytir viðskiptamaður sölupöntun frá 70 í 40 stykki milli tveggja áætlunarkeyrslna. Yfirflæðisbúnaðurinn grípur inn í til að draga úr innkaupunum sem lögð voru til fyrir upphaflega sölumagnið.  

#### <a name="item-setup"></a>Vöruuppsetning  

|Endurpöntunarstefna|Hámarksmagn|  
|-----------------------|------------------|  
|Hámarksmagn pöntunar|100|  
|Endurpöntunarmark|50|  
|Birgðir|80|  

#### <a name="situation-before-sales-decrease"></a>Staða fyrir söluminnkun  

|Atburður|Breyta magni|Áætlaðar birgðir|  
|-----------|-----------------|-------------------------|  
|Dagur eitt|Engin|80|  
|Sala|-70|10|  
|Lok tímaramma|Engin|10|  
|Leggja til nýja innkaupapöntun|+90|100|  

#### <a name="situation-after-sales-ddecrease"></a>Staða eftir söluminnkun  

|Breyting|Breyta magni|Áætlaðar birgðir|  
|------------|-----------------|-------------------------|  
|Dagur eitt|Engin|80|  
|Sala|-40|40|  
|Innkaup|+90|130|  
|Lok tímaramma|Ekkert|130|  
|Stinga upp á að minnka innkaup<br /><br /> panta frá 90 til 60|-30|100%|  

#### <a name="resulting-planning-lines"></a>Áætlunarlínur  
 Ein áætlunarlína (viðvörun) er stofnuð til að draga úr innkaupum um 30 úr 90 í 60 til að halda áætluðum birgðum í 100 samkvæmt yfirflæðisstiginu.  

![Áætla samkvæmt yfirflæðisstigi](media/nav_app_supply_planning_2_overflow2.png "Áætla samkvæmt yfirflæðisstigi")  

> [!NOTE]  
>  Ef búnaðurinn Yfirfall er ekki til staðar er ekki stofnuð nein viðvörun ef áætlaðar birgðir eru meiri en hámarksbirgðir. Þetta kann að valda óþörfu framboði upp á 30.

## <a name="handling-projected-negative-inventory"></a>Að takast á við áætlaða neikvæða birgðastöðu
Endurpöntunarmarkið endurspeglar ætlaða eftirspurn á afhendingartíma vörunnar. Þegar farið er yfir endurpöntunarmark er kominn tími til að panta meira magn. En áætlaðar birgðir verður að vera nógu stórt til að hylja eftirspurn þar til ný pöntun er móttekin. Á meðan ættu öryggisbirgðir að uppfylla sveiflur í eftirspurn að áætluðu þjónustustigi.  

 Þar af leiðandi lítur áætlanakerfi á það sem neyðarástand ef framtíðareftirspurn er ekki hægt að mæta úr áætlaðar birgðir eða m.ö.o. ef áætlaðar birgðir verða neikvæðar. Kerfið meðhöndlar þannig frávik með því að leggja til nýja birgðapöntun til að uppfylla þann hluta eftirspurnarinnar sem birgðir eða önnur eftirspurn getur ekki uppfyllt. Stærð pöntunar í nýju birgðapöntuninni mun ekki taka tillit til hámarksbirgða eða pöntunarmagns, né heldur til pantanabreytinganna Hámarksmagn pöntunar, Lágmarksmagn pöntunar eða Margföld pöntun. Í Staðinn, mun það endurspegla nákvæmlega skort.  

 Áætlunarlína fyrir þessa gerð birgðapöntunar birtir viðvörunartákn og viðbótarupplýsingar birtast við uppflettingu, til að upplýsa notandann um stöðu mála.  

 Í eftirfarandi dæmi, framboð D táknar neyðarpöntun til að leiðrétta fyrir neikvæðum birgðum.  

 ![Viðbragðsáætlun til að koma í veg fyrir neikvæða birgðastöðu](media/nav_app_supply_planning_2_negative_inventory.png "Viðbragðsáætlun til að koma í veg fyrir neikvæða birgðastöðu")  

1.  Framboð **A**, fyrstu áætlaðar birgðir, er undir pöntunarmark.  
2.  Nýtt framsendingaráætlað framboð er stofnað (**C**).  

     (Magn = Hámarksbirgðir – Áætlað birgðastig)  
3.  Framboð **A** er lokað með eftirspurn **B**, sem er ekki að öllu leyti annað.  

     (Eftirspurn **B** gæti reynt að áætla framboð C en það gerist ekki samkvæmt tímaramma.)  
4.  Nýtt framboð (**D**) er stofnað til að uppfylla eftirstandandi magn eftirspurnar **B**  
5.  Eftirspurn **B** er lokað (búa til áminningu fyrir áætluðum birgðum).  
6.  Nýjar birgðir **D** eru lokaðar.  
7.  Áætlaðar birgðir er athugaðar. Endurpöntunarmarki hefur ekki verið náð.  
8.  Framboð **C** er lokað (ekki meiri eftirspurn til staðar).  
9. Lokaathugun: Engin útistandandi birgðastigsinnheimtubréf eru eftir.  

> [!NOTE]  
>  Skref 4 endurspeglar hvernig kerfið bregst við í útgáfum fyrr en Microsoft Dynamics NAV 2009 SP1.  

Þetta lýkur lýsingu miðlægra reglna sem tengjast birgðaáætlunargerð sem byggir á reglum um endurpöntun. Í eftirfarandi kafla er fjallað um einkenni fjögurra studdra endurpöntunarstefna.

## <a name="reordering-policies"></a>Endurpöntunarstefnur
Endurpöntunarstefnur skilgreina hversu mikið þarf að panta þegar vara þarf að vera fyllt á. Fjórir mismunandi endurröðunarstefnur eru til.  

### <a name="fixed-reorder-qty"></a>Fast endurpöntunarmagn
Stefnan Fast endurpöntunarmagn tengist birgðaáætlanagerð á dæmigerðum C-vörum (lágur birgðakostnaður, lítil hætta á úreldingu og / eða mörgum vörum). Þessi stefna er yfirleitt notað í tengslum við pöntunarmark endurspeglar fyrirsjáanlegs eftirspurn meðan á afhendingartími vörunanr stendur.  

#### <a name="calculated-per-time-bucket"></a>Reiknuð fyrir hvern tímaramma  
Ef áætlanakerfið greinir að endurpöntunarmarkinu hafi verið náð eða farið yfir það innan tiltekins tímaramma (endurpöntunarferli) – yfir eða við endurpöntunarmarkið í upphafi tímabilsins og undir því eða við það í lokin – leggur það til stofnun nýrrar birgðapöntunar á tilgreinda endurpöntunarmagninu og áætlar það áfram frá fyrstu dagsetningunni eftir lok tímarammans.  

Hugtakið um hólfað endurpöntunarmark dregur úr fjölda framboðstillaga. Þetta endurspeglar handvirkt ferli af því að fara oft inn á lager til að athuga raunverulegt innihald í hinum ýmsu hólfum.  

#### <a name="creates-only-necessary-supply"></a>Stofanr aðeins nauðsynlegar birgðir  
Áður en ný birgðapöntun er lögð til til að mæta endurpöntunarmarki, kannar áætlanakerfið hvort framboð hafi verið pantað eða móttekið innan afhendingartíma vörunnar. Ef núverandi birgðapöntun leysir vandamálið með því að færa áætlaðar birgðir að eða yfir endurpöntunarmarkið innan afhendingartímans leggur kerfið ekki til nýja birgðapöntun.  

Birgðapantanri sem eru búnar til sérstaklega til að mæta pöntunarmark er útilokuð frá venjulegum framboðsjöfnun, og mun ekki á nokkurn hátt hægt að breyta eftirá. Þar af leiðandi, ef á að áfangaskipta út vöru með endurpöntunarmarki (ekki endurnýja) er ráðlegt að endurskoða útistandandi birgðapantanir handvirkt eða breyta endurpöntunarstefnu í Lotu fyrir lotu, þannig að kerfið dragi úr eða afturkalli umframbirgðir.  

#### <a name="combines-with-order-modifiers"></a>Samsett við Breytingalykla  
Pantanabreytingarnar, Lágmarksmagn pöntunar, Hámarksmagn pöntunar og Margföld pöntun, ættu ekki að gegna stóru hlutverki þegar notuð er stefnan um fast pöntunarmagn. Hins vegar reiknar áætlanakerfið enn með þessum breytingalyklum og minnkar magnið í tilgreint hámarkspöntunarmagn (og býr til tvær eða fleiri birgðir til að ná heildarpöntunarmagninu), eykur pöntunina í tilgreint lágmarkspöntunarmagn, eða námundar pöntunarmagnið upp til að ná tiltekinni margfaldri pöntun.  

#### <a name="combines-with-calendars"></a>Sameinast dagbók  
Áður en ný birgðapöntun er lögð til að mæta endurpöntunarmarki, kannar áætlanakerfið hvort pöntunin sé áætluð á frídegi, samkvæmt öllum dagatölum sem eru skilgreind í **Grunndagatalskóði** reitnum á síðunni **Fyrirtækjaupplýsingar** og **Birgðageymslukort**.  

Ef fyrirhuguð dagsetning er frídagur, færir áætlanakerfið pöntunina áfram á næsta virka dag. Þetta getur orsakað pöntun sem uppfyllir endurpöntunarmark en uppfyllir ekki einhverja tiltekna eftirspurn. Fyrir svona ójafna eftirspurn, býr áætlanakerfið til auka framboð.  

#### <a name="should-not-be-used-with-forecast"></a>Ætti ekki að nota við spá  
Þar sem væntalega eftirspurn er þegar lýst í endurpöntunarmarki er ekki nauðsynlegt að spá í að skipuleggja hlut með endurpöntunarmarki. Ef það er viðeigandi að byggja áætlun á spá skal nota stefnuna lotu-fyrir-lotu.  

#### <a name="must-not-be-used-with-reservations"></a>Má ekki nota með frátekningu  
Ef notandi hefur tekið frá magn, til dæmis magn í birgðum fyrir einhverja fjarlæga eftirspurn, truflar það forsendur áætlunarinnar. Jafnvel þótt áætlað birgðastig sé leyfilegt með tilliti til endurpöntunarmarks, má magnið ekki vera til staðar vegna frátekningarinnar. Kerfið kann að reyna að bæta það upp með því að stofna frávikspantanir. Þó er mælt með því að reiturinn Taka frá sé stilltur á Aldrei fyrir vörur sem eru planaðar með endurpöntunarmarki.

### <a name="maximum-qty"></a>Hámarksmagn
Reglan um hámarksmag er ein leið til að viðhalda birgðum með því að nota endurpöntunarmark.  

Allt sem gildir um stefnu endurpöntunarmagns gildir einnig um þessa stefnu. Eini munurinn er magnið sem lagt er til sem framboð. Þegar reglan um hámarksmagn rer notuð verður endurpöntunarmagnið skilgrein á virkan hátt samkvæmt ætluðu birgðastigi og verður því yfirleitt mismunandi eftir pöntunum.  

#### <a name="calculated-per-time-bucket"></a>Reiknuð fyrir hvern tímaramma  
Endurpöntunarmarkið er ákvarðað á þeim tímapunkti (við lok tímaramma) þegar áætlanakerfið greinir að farið hefur verið yfir endurpöntunarmark. Á þessum tíma mælir kerfið bilið frá núverandi áætlaðar birgðum upp að tilteknum hámarksbirgðum. Þetta stendur fyrir magnið sem þarf að endurpanta. Kerfið kannar þá hvort birgðir hafi þegar verið pantaðar annars staðar þannig að þær berist innan afhendingartímans og, ef svo er, minnkar magn nýju birgðapöntunarinnar í samræmi við það magn sem þegar hefur verið pantað.  

Kerfið tryggir að áætlaðar birgðir nái a.m.k. endurpöntunarmarkinu - ef vera skyldi að notandinn hafi gleymt að tilgreina hámarksbirgðagildi.  

#### <a name="combines-with-order-modifiers"></a>Samsett við Breytingalykla  
Það fer eftir uppsetningu, getur það verið best að sameina það hámarksmagn stefnu með breytingalyklum til að tryggja lágmarksupphæð þess magn eða sléttun innkaupaeiningar, eða kljúfa það í fleiri lotur samkvæmt skilgreiningu hámarksmagns.  

### <a name="combines-with-calendars"></a>Sameinast dagbók  
Áður en ný birgðapöntun er lögð til að mæta endurpöntunarmarki, kannar áætlanakerfið hvort pöntunin sé áætluð á frídegi, samkvæmt öllum dagatölum sem eru skilgreind í **Grunndagatalskóði** reitnum á síðunni **Fyrirtækjaupplýsingar** og **Birgðageymslukort**.  

Ef fyrirhuguð dagsetning er frídagur, færir áætlanakerfið pöntunina áfram á næsta virka dag. Þetta getur orsakað pöntun sem uppfyllir endurpöntunarmark en uppfyllir ekki einhverja tiltekna eftirspurn. Fyrir svona ójafna eftirspurn, býr áætlanakerfið til auka framboð.

### <a name="order"></a>Pöntun
Í framleiða eftir pöntun umhverfi, er vara keypt eða framleidd til eingöngu ná ákveðna eftirspurn. Venjulega tekur hún til A-vara og ástæða fyrir að velja Endurpöntunarstefnu pöntunar getur verið að eftirspurn er hverfandi, sem afhendingartími er óveruleg, eða nauðsynlegar eigindir mismunandi.  

Forritið stofnar pöntun-við-pöntun tengsl sem virka sem undirbúningstengsl milli framboðsins, birgðapöntunar eða birgða og eftirspurnarinnar sem henni er ætlað að mæta.  

Burtséð frá notkun pöntunarstefnu er hægt að nota tengil á milli pantana í áætlun með eftirfarandi hætti:  

* Þegar reglan framleiðsla eftir pöntun er notuð til að stofna margþrepa framleiðslupöntun eða framleiðslupöntun af gerðinni verk (nauðsynlegir íhlutir framleiddir samkv. sömu framleiðslupöntun).  
* Þegar búnaðurinn Sölupantanaáætlun er notaður til að stofna framleiðslupöntun úr sölupöntun.  

Jafnvel þótt framleiðslufyrirtæki álíti sig framleiða eftir pöntun geur verið best að nota endurpöntunarstefnuna lota fyrir lotu ef vörurnar eru staðlaðar án afbrigða í eigindum. Niðurstaðan er að kerfið mun nota óáætlaðar birgðir og safna aðeins sölupöntunum með sömu afhendingardagsetningu eða innan tilgreinds tímaramma.  

#### <a name="order-to-order-links-and-past-due-dates"></a>Tenglar á milli pantana og liðnir skiladagar  
Ólíkt flestum framboð-eftirspurn settum eru tengdar pantanir með skiladag á undan upphafsdagsetningu áætlunar áætlaðar að fullu af kerfinu. Viðskiptaástæðan fyrir þessa undanþágu er að tiltekin pör eftirspurnar og framboðs þurfa að vera samstillt fram að framkvæmdinni. Nánari upplýsingar um frosna svæðið sem eiga við um flestar gerðir framboðs og eftirspurnar eru í [Takast á við pantanir fyrir upphafsdagsetningu áætlunar](design-details-balancing-demand-and-supply.md#dealing-with-orders-before-the-planning-starting-date).

### <a name="lot-for-lot"></a>Lotu-fyrir-lotu
Lota-fyrir-lotu reglan er sveigjanlegust vegna þess að kerfið bregst bara við raunverulegri eftirspurn og bregst auk þess við væntanlegri eftirspurn samkvæmt spám og standandi pöntunum og ákvarðar svo magn pantanan á grundvelli eftirspurnarinnar. Lota-fyrir-lotu reglan beinist að A- og B-vörum þar sem hægt er að samþykkja birgðir en ætti helst að forðast það.  

Að sumu leyti er lota fyrir lotu stefnan eins og pantanastefnan en er með almenna nálgun á vörur; það getur samþykkt magn í birgðum, og það flokkareftirspurn og samsvarandi framboð í tímarömmum skilgreindum af notanda.  

Tímaramminn er skilgreindum í reitnum **Tímarammi**. Kerfið vinnur með lágmarks tímaramma upp á einn dag, þar sem það er minnsta tímamælieining fyrir birgðir og eftirspurn í kerfin (þó svo að í raun geti tímamælieining á framleiðslupöntunum og íhlutaþörfum verið sekúndur).  

Tímaramminn setur einnig takmörkun á það hvenær birgðapöntun er enduráætluð til að mæta tiltekinni eftirspurn. Ef framboð er innan tímarammans verður það enduráætlað inn eða út til að svara eftirspurninni. Annars, ef það liggur fyrr, mun það valda óþarfa uppsöfnun birgða og ætti að afturkalla. Ef það er síðar verður nýtt framboð stofnað í staðinn.  

Með þessari reglu er einnig mögulegt að skilgreina öryggisbirgðir til að bæta upp hugsanlegar sveiflur á birgðum eða til að mæta skyndilegri eftirspurn.  

Þar sem birgðapöntunarmagn byggir á raunveruleg eftirspurn getur það borgað sig að nota raðabreytur: slétta pöntunarmagn til að það passi við tiltekna pöntunarstuðul (eða innkaupamælieiningu), auka pöntuina upp í tiltekið magn, eða minnka magnið í hámarksmagn (og því búa til tvær eða fleiri birgðir til að uppfylla allt magnið).

## <a name="see-also"></a>Sjá einnig  
[Hönnunarupplýsingar: Áætlunarfæribreytur](design-details-planning-parameters.md)   
[Hönnunarupplýsingar: áætlunartafla](design-details-planning-assignment-table.md)   
[Hönnunarupplýsingar: Miðlægar hugmyndir áætlanakerfisins](design-details-central-concepts-of-the-planning-system.md)   
[Hönnunarupplýsingar: Jöfnun eftirspurnar og framboðs](design-details-balancing-demand-and-supply.md)   
[Hönnunarupplýsingar: framboðsáætlun](design-details-supply-planning.md)
