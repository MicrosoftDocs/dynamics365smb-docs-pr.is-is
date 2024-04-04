---
title: 'Hönnunarupplýsingar: Pöntun, pöntunarrakning og stöðuboð | Microsoft Docs'
description: Frátekningarkerfið er ítarlegt og nær yfir samtengda og samliggjandi eiginleika pöntunarrakningar og aðgerðaboða.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'design, replenishment, reordering'
ms.date: 06/08/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Hönnunarupplýsingar: Pöntun, pöntunarrakning og stöðuboð
Frátekningarkerfið er ítarlegt og nær yfir samtengda og samliggjandi eiginleika pöntunarrakningar og aðgerðaboða.  

 Kjarni frátekningarkerfisins er tenging eftirspurnarfærslu og samsvarandi framboðsfærslu, annað hvort með frátekningu eða rakningu pöntunar. Frátekning er tengill sem notandi myndar og pöntunarrakningarfærsla er tengill sem kerfi myndar. Vörumagn sem fært er í frátekningarkerfið er annað hvort frátekið eða pöntunarrakið, ekki bæði í einu. Hvernig kerfin meðhöndla vöru fer eftir því hvernig varan er uppsett.  

 Frátekningarkerfið vinnur með áætlanakerfinu með því að búa til aðgerðaboð á áætlunarlínum í áætlunarkeyrslu. Aðgerðarboð geta talist viðbót við skráningu pöntunarrakningar. Aðgerðaboð, hvort sem þau eru stofnuð kvikt í pöntunarrakningu eða við áætlunarkeyrslu, bjóða upp á hentugt verkfærui fyrir skilvirka framboðsáætlun.  

> [!NOTE]  
>  Áskilinn magn er hunsað af áætlunarkerfi, það er, harði tengilinn sem er á milli framboðs og eftirspurnar er ekki hægt að breyta í gegnum áætlanagerð.  

 Frátekningarkerfið myndar einnig skipulagsgrunn fyrir vörurakningarkerfið. Nánari upplýsingar eru í [Upplýsingar um hönnun: Vörurakning](design-details-item-tracking.md).  

 <!--For more detailed information about how the reservation system works, see the _Reservation Entry Table_ white paper on [PartnerSource](https://go.microsoft.com/fwlink/?LinkId=258348).  -->

> [!NOTE]
> [!INCLUDE [locations-cronus](includes/locations-cronus.md)]

## Frátekning  
 Frátekning er fastur tengill sem tengir sérstaka eftirspurn og sérstakt framboð. Þessi tengill hefur beint áhrif á síðari birgðafærslu og tryggir rétta notkun vörufærsla vegna kostnaðar. Frátekning hnekkir sjálfgefinni aðferð kostnaðarútreiknings fyrir vöru. Nánari upplýsingar eru í [Upplýsingar um hönnun: Vörurakning](design-details-item-tracking.md).  

 Síðan **Frátekning** er aðgengileg af öllum pöntunarlínum af gerðinni eftirspurn og framboð. Á þessari síðu getur notandinn skilgreint hvaða eftirspurn eða framboð færslu til að búa til frátekningartengil á. Frátekning samanstendur af færslupörum með sama færslunúmer. Ein færsla er með neikvætt formerki og vísar á eftirspurn. Hin færslan er með jákvæðu merki og vísar á framboðið. Þessar færslur eru vistaðar í töflunni **Frátekningarfærsla** með stöðugildinu **Frátekning**. Notandinn getur skoðað allar frátekningarnar á síðunni **Frátekningarfærslur**.  

### Mótbókun í frátekningu  
 Frátekningar eru gerðar gegn tiltæku vörumagni. Vara til ráðstöfunar er reiknuð út í undirstöðuatriðum á eftirfarandi hátt:  

 tiltækt magn = birgðir + tímasettar móttökur - brúttóþarfir  

 Eftirfarandi tafla sýnir upplýsingar um pöntunarneteiningar sem eru hluti af framboðsútreikningi.  

||Reitur í T27|Upprunatafla|Töfluafmörkun|Upprunareitur|  
|-|------------------|------------------|------------------|------------------|  
|**Birgðir**|Birgðir|Birgðafærsla|Á ekki við|Magn|  
|**Tímasettar móttökur**|Mótt. afgr. framl.pönt. (magn)|Framl.pöntunarlína|Áætlað|Eftirstöðvar (stofn)|  
|**Tímasettar móttökur**|Mótt. útg. pöntunar (magn)|Framl.pöntunarlína|=Útgefið|Eftirstöðvar (stofn)|  
|**Tímasettar móttökur**|Magn í samsetningarpöntun|Yfirskrift samsetningar|Pantanir|Eftirstöðvar (stofn)|  
|**Tímasettar móttökur**|Magn í innk.pöntun|Innkaupalína|Pantanir|Óafgreitt magn (stofn)|  
|**Tímasettar móttökur**|Mótt. millif. pönt. (Magn)|Millifærslulína|Á ekki við|Útistandandi magn|  
|**Brúttóþörf**|Magn í sölupöntun|Sölulína|Pantanir|Óafgreitt magn (stofn)|  
|**Brúttóþörf**|Tímasett þörf (magn)|Framl.pöntunaríhlutur|<>Hermd|Eftirstöðvar (stofn)|  
|**Brúttóþörf**|Magn í sams.íhlut|Samsetningarlína|Pantanir|Eftirstöðvar (stofn)|  
|**Brúttóþörf**|Afh. millif. pönt. (magn)|Millifærslulína|Á ekki við|Útistandandi magn|  

 Nánari upplýsingar eru í [Upplýsingar um hönnun: Til ráðstöfunar í vöruhúsi](design-details-availability-in-the-warehouse.md).  

### Handvirk frátekning  
 Þegar notandi býr viljandi til frátekningu fær notandinn fullt eignarhald og ábyrgð á þessum vörum. Þetta þýðir að notandinn þarf einnig handvirkt breyta eða hætta við frátekningu. Slíkar handvirkar breytingar geta valdið sjálfvirka breytingu á frátekningum  

 Eftirfarandi tafla sýnir hvenær og hvaða breytingar gætu átt sér stað:  

|Aðgerð notanda|Kerfisviðbrögð|  
|-----------------|---------------------|  
|Minnka frátekið magn|Tengdir magnreitir eru uppfærðir.|  
|Breyting dagsetningarreita|Tengdir dagsetningarreitir eru uppfærðir.<br /><br /> **Athugið:** Ef gjalddaga eftirspurnar er breytt til að hann komi á undan afhendingardegi eða gjalddaga framboðsins er hætt við frátekninguna.|  
|Eyða pöntuninni|Hætt við frátekningu.|  
|Breyting staðsetninga, hólfa, afbrigða, raðnúmers, eða lotunúmers.|Hætt við frátekningu.|  

> [!NOTE]  
>  Aðgerðin fyrir bindingu á eftir áætlun getur einnig breytt fyrirvörum án þess að notandi sé upplýstur, með þvi´að endurraða ótilgreindum fyrirvörum rað- eða lotunúmera. Nánari upplýsingar eru í „Upplýsingar um hönnun: Vörurakning og frátekningar“.  

### Sjálfvirkar frátekningar  
 Birgðaspjaldið má stilla þannig að það sé alltaf með sjálfkrafa frátekt úr eftirspurn, svo sem sölupantanir. Þá er gerð frátekning á birgðum, innkaupapöntunum og samsetningarpöntunum og framleiðslupöntunum. Viðvörun er birt ef framboð er ónógt.  

 Að auki eru vörur sjálfkrafa áskilin með ýmsum aðgerðum að skipuleggja að halda eftirspurn tengd við ákveðinn framboðs. Pöntunarrakningarfærslur fyrir slíka áætlanatengla innihalda **Frátekning** í reitnum **Frátekningarstaða** í töflunni **Frátekningarfærsla**. Sjálfvirkar frátekningar eru búnar til í eftirtöldum tilvikum:  

-   Framleiðslupöntun í mörgum stigum þar sem reiturinn **Framleiðslustefna** viðkomandi yfir- og undirvöru er stilltur á **Eftir pöntun**. Áætlanakerfið býr til frátekningar á milli yfirframleiðslupöntun og undirliggjandi framleiðslupöntunum til að tryggja að pantanirnar verði unnar samtímis. Slíka frátekningarbinding hnekkir sjálfgefnum kostnaði og jöfnunaraðferð vöru.  

-   Framleiðsla, samsetning eða innkaupapöntun þar sem reiturinn **Framleiðslustefna** viðkomandi vöru er stilltur á **Pöntun**. Áætlanakerfið býr til frátekningar á milli eftirspurnar og ætlaðs framboð til að tryggja að tilgreint framboð verði búið til. Nánari upplýsingar eru í [Pöntun](design-details-handling-reordering-policies.md#order).  

-   Framleiðslupöntun sem stofnuð er með eiginleikanum **Sölupantanaáætlun** er tengd við sölupöntun með sjálfvirkri frátekningu.  

-   Samsetningarpöntun sem er mynduð sjálfkrafa fyrir sölupöntunarlínu til að uppfylla magnið í reitnum **($ T_37_900 Qty. to Assemble to Order $)**. Þessi sjálfvirka frátekning tengir sölueftirspurn og framboðssamsetningu þannig að þeir sem sjá um sölupantanir geti stillt og lofað samsetningarvörunni beint við viðskiptamanninn. Að auki, frátekning tengir samsetningarfrálag við sölupöntunarlínu í gegnum afhendingaraðgerðir sem uppfyllir pantanir viðskiptavini þess.  

 Ef um er að ræða framboð eða eftirspurn sem er ekki úthlutað, úthlutar áætlanakerfið sjálfkrafa pöntunarstöðu af tegund **Afgangur** Þetta gæti leitt til eftirspurnar sem er vegna fyrirsjáanlegs magns eða áætlunarfæribreyta sem slegnar hafa verið inn. Þetta er gildur afgangur, sem kerfið ber kennsl á, og gefur ekki tilefni til aðgerðaboða. Umframbirgðir, eins og í þessu tilfelli, endurspeglar umframframboð eða eftirspurn sem helst órakin. Þetta gefur til kynna ójafnvægi í pöntunarnetinu sem veldur því að kerfið gefi út aðgerðaboð. Hafið í huga að aðgerðaboð sem leggur til breytingu á magni á alltaf við gerðina **Umframbirgðir** Frekari upplýsingar eru í „Dæmi: Pöntunarrakning í sölu, framleiðsla og flutningur“ í þessu efnisatriði.  

 Sjálfvirkar frátekningar sem eru búnar til á áætlunarkeyrslu eru meðhöndlaðar á eftirfarandi hátt:  

-   Þær eru jafnaðar á móti vörumagni sem eru hluti af framboðsútreikningi, sem og handvirkar frátekningar. Nánari upplýsingar eru í hlutanum „Sjálfvirkar frátekningar“ í þessu efnisatriði.  

-   Þær eru innfaldar og hugsanlega breytt í síðari áætlunarkeyrslum, borið saman við handvirkt fráteknar vörur.  

## Rakning pöntunar  
 Pöntunarrakning hjálpar til við viðhalda gildri framboðsáætlun með því að bjóða upp á yfirlit yfir mótbókun á milli eftirspurnar og framboðs í pöntunarnetinu. Pöntunarrakningarfærslan er undirstaða fyrir gangvirk aðgerðaboð og tilögur um áætlanalínur á meðan áætlun er í keyrslu.  

> [!NOTE]  
>  Pöntunarrakningarkerfið jafnar tiltækar birgðir um leið og pantanir eru færðar inn í pöntunarnetið. Þetta gefur til kynna að kerfið setji ekki í forgang pantanir sem kunna að vera meiri áríðandi vegna skiladags. Því er það undir rökum áætlanakerfis eða skynsemi áætlanagerðarmanns komið að raða þessum forgangsverkefnum á skynsamlegan hátt.  

> [!NOTE]  
>  Pöntunarrakningarregla og aðgerðin Sækja aðgerðaboð eru ekki samþættar við Vinnslu. Þetta merkir að eftirspurn tengd verki er ekki rakin sjálfkrafa. Þar sem það er ekki rakið getur það valdið því að önnur áfylling með öðrum verkupplýsingum sé rakin fyrir aðra eftirspurn, t.d. sölupöntun. Einnig getur komið upp sú aðstaða þar sem upplýsingar um tiltækar birgðir eru ekki samstilltar.  

### Pöntunarnetið  
 Pöntunarrakningarkerfið er byggt á þeirri meginreglu að pöntunarnetið verði alltaf að vera í jafnvægi, þar sem öll eftirspurn sem skráð er í kerfið samsvari framboði, og öfugt. Kerfið nær þessu með því að bera kennsl á röklæga tengla milli allra eftirspurnar og birgðafærslna í pöntunarnetinu.  

 Þessi meginregla felur í sér að breyting á eftirspurn leiðir til samsvarandi ójafnvægi á framboðshlið pöntunarnets. Hins vegar leiðir birgðabreyting til samsvarandi ójafnvægis á eftirspurnarhlið pantanakerfisins. Í raun er pöntunarnetið í síbreytilegu flæði því notendur slá inn, breyta og eyða pöntunum. Pöntunarrakning vinnur pantanir kvikt, bregst við öllum breytingum á þeim tíma sem þær eru færðar inn í kerfið og verða hluti af pöntunarnetinu. Um leið og ný pöntunarrakning er stofnuð er pöntunarnetið í jafnvægi, en aðeins þangað til að næsta breyting á sér stað.  

 Til að auka gagnsæi útreikninga í áætlanakerfi sýnir síðan **Óraktar áætlunareiningar** órekið magn sem lýsir mismun á magni milli þekktan eftirspurn og leiðbeinandi framboð. Hver lína á síðunni vísar til orsakar af umframmagni, svo sem **Standandi pöntun**, **Öryggisbirgðastig**, **Fast endurpöntunarmagn**, **Lágmarks pöntunarmagn**, **Sléttun** eða **Hömlur**.  

### Mótbókun í pöntunarrakningu  
 Ólíkt frátekningum, sem getur aðeins verið gert gegn fyrirliggjandi vörumagni, er pantanarakning möguleg fyrir allar pöntunarnetseiningar sem eru hluti af netpantanaútreikningi áætlanakerfisins. Nettókröfur eru reiknaðar út með eftirfarandi hætti:  

 nettókröfur = brúttókröfur + endurpöntunarmark - tímasettar móttökur - áætlaðar móttökur - áætluð fyrirliggjandi staða  

> [!NOTE]  
>  Eftirspurn sem er tengt við spár eða skipulags þáttum er ekki raktir eftir pöntun.  

### Dæmi: Pöntunarrakning í sölu, framleiðsla og flutningur  
 Eftirfarandi atburðarás sýnir hvaða pöntunarrakningarfærslur eru búnar til í töflunni **Frátekningarfærsla** vegna ýmissa breytinga í pöntunarneti.  

 Gera skal ráð fyrir eftirfarandi gögnum fyrir tvær vörur sem eru uppsettar fyrir pöntunarrakningu.  

|Vara 1|Name|""|
|-|-|-|
||Til ráðstöfunar|100 einingar í VESTUR birgðageymslu<br /><br />- 30 einingar af LOTA<br />- 70 einingar af LOTB|  
|Vara 2|Name|„Framleidd vara“|
||Framl.uppskr.|1 magn á „íhlut“|  
||Eftirspurn|Sala á 100 einingar á AUSTUR stað|  
||Framboð|Útgefin framleiðslupöntun (búin til með **VÁætlun sölupöntunar** eiginleikanum fyrir sölu á 100 hlutum)|  

Á síðunni **Framleiðsluuppsetning** er reiturinn **Íhlutir á staðnum** stilltur á **RED**.

 Eftirfarandi pöntunarrakningarfærslur eru til staðar í töflunni **Frátekningarfærsla** samkvæmt gögnunum í töflunni.  

 ![Fysta dæmi um pöntunarrakningarfærslur í frátekningarfærslutöflu.](media/supply_planning_RTAM_1.png "supply_planning_RTAM_1")  

### Færslunúmer 8 og 9  
 Fyrir íhlutaþörf fyrir LOTA annarsvegar og LOTB hinsvegar eru tenglar pöntunarrakningar stofnaðir úr eftirspurninni í töflu 5407, **Framl.pöntunaríhlutur**, til framboðsins í töflu 32, **Birgðafærsla**. **Pöntunarstaða** reitur inniheldur **Rakning** til að sýna að þessar færslur eru breytilegir pöntunarrakningartenglar á milli framboðs og eftirspurnar.  

> [!NOTE]  
>  Reiturinn**lotunr.** er auður á eftirspurnarlínum vegna þess að ekki eru tilgreind lotunúmer í íhlutalínum losaðrar framleiðslupöntunar.  

### Færslunúmer 10  
 Úr sölueftirspurn í töflu 37, **Sölulína**, er pöntunarrakningartengill stofnaður fyrir framboðið í töflu 5406, **Framl.pöntunarlína**. **pöntunarstaða** reitur inniheldur **frátekningu** og **binding** reitur inniheldur **pöntun-í-pöntun**. Þetta er vegna þess að útgefin framleiðslupöntun var stofnuð sérstaklega fyrir sölupöntunina og verður að vera tengd, öfugt við pöntunarrakningartenglum með frátekningarstöðuna **Rakning**, sem eru stofnaðir og breytt gagnvirkt. Nánari upplýsingar eru í hlutanum „Sjálfvirkar frátekningar“ í þessu efnisatriði.  

 Á þessum tímapunkti , eru 100 einingar í LOTA og LOTB flutt til EAST með flutningspöntun.  

> [!NOTE]  
>  Aðeins afhending millifærslupöntunar er bókuð á þessum tímapunkti, ekki móttaka.  

 Eftirfarandi röð pöntunarrakningarfærslna til staðar í töflunni **Frátekningarfærsla**.  

 ![Annað dæmi um pöntunarrakningarfærslur í frátekningarfærslutöflu.](media/supply_planning_RTAM_2.png "supply_planning_RTAM_2")  

### Færslunúmer 8 og 9  
 Pöntunarrakningarfærslum fyrir tvær lotur íhlutarins sem endurspegla eftirspurn í töflu 5407 er breytt úr frátekningarstöðunni **Raknings** í **Umframbirgðir**. Ástæðan er að birgðirnar sem greiðslan var tengd við áður, í töflu 32, hafa verið notaðar af sendingu á millifærslupöntuninni.  

 Raunverulegur afgangur, eins og í þessu tilfelli, endurspeglar umframframboð eða eftirspurn sem helst órakin. Það er til marks um ójafnvægi í pöntunarneti, sem mun búa til aðgerðaboð af áætlanakerfinu  nema það sé leyst virk.  

### Færslunúmer 12 til 16  
 Vegna þess að tvær lotur af íhlutanum eru bókaðar á flutningspöntunina sem sendar en ekki mótteknar, eru allar tengdar jákvæðar pöntunarrakningngarfærslur af gerðinni frátekning **Afgangur**, sem gefur til kynna að þeir eru ekki úthlutað neinum kröfum. Fyrur hvert lotunúmer gentist ein færsla töflu 5741, **Millifærslulína**, og ein færsla tengist birgðafærslunni í flutningsstaðsetningunni þar sem vörurnar eru núna.  

 Á þessum tímapunkti er flutningspöntunin íhluta frá AUSTUR til VESTUR bókað sem móttekin.  

 Eftirfarandi röð pöntunarrakningarfærslna til staðar í töflunni **Frátekningarfærsla**.  

 ![Þriðja dæmi um pöntunarrakningarfærslur í frátekningarfærslutöflu.](media/supply_planning_RTAM_3.png "supply_planning_RTAM_3")  

 Pöntunarrakningarfærslurnar eru nú áþekkar því sem var á fyrsta stigi aðstæðnanna, áður en flutningspöntunin var bókuð sem aðeins send, nema að færslur fyrir íhlutinn eru nú með frátektarstöðuna **Afgangur**. Þetta er vegna þess að þörf fyrir íhlutinn er ennþá á staðsetningunni VESTUR, sem endurspeglar að reiturinn **Staðsetningarkóði** á íhlutarlínu framleiðslupöntunarinnar innihaldi **VESTUR** líkt og sett er upp í uppsetningarreitnum **Íhlutir á staðnum**. Birgðir sem var úthlutað á þessa eftirspurn áður hafa verið færðar á AUSTUR staðsetningu og eru að fullu rekjanlegar nema ef íhlutarþörf á framleiðslupöntunarlínu sé breytt í EAST staðsetningu.  

 Á þessum tímapunkti er **Staðsetningarkóði** á framleiðslupöntunarlínu stilltur á **AUSTUR**. Að auki, á síðunni **vörurakningarlína** eru 30 vörur af LOTA og 70 vörur af LOTB settar á framleiðslupöntunarlínu.  

 Eftirfarandi röð pöntunarrakningarfærslna til staðar í töflunni **Frátekningarfærsla**.  

 ![Fyrsta dæmi um pöntunarrakningarfærslur í frátekningarfærslutöflu.](media/supply_planning_RTAM_4.png "supply_planning_RTAM_4")  

### Færslunúmer 21 og 22  
 Þar sem íhluturinn þarf að hafa verið breytt í AUSTUR staðsetningu og framboðið er tiltækt sem birgðahöfuðbókarfærslur á AUSTUR staðsetningu eru allar pöntunarrakningarfærslur fyrir tvö lotunúmer nú að fullu raktar, gefið til kynna með frátekningarstöðu **Rakning**.  

 Reiturinn **lotunr.** er nú útfylltur í pöntunarrakningarfærslunni fyrir töflu 5407 vegna þess að lotunúmerunum var úthlutað á íhlutalínur framleiðslupöntunar.  

 Nákvæmar upplýsingar um hvernig frátekningarkerfið virkar í töflunni **Frátekningarfærsla** eru á hvítblaðinu „Taflan Frátekningarfærsla“ í [PartnerSource](https://go.microsoft.com/fwlink/?LinkId=258348) (innskráning er nauðsynleg).

## Aðgerðarboð  
 Þegar pöntunarrakningarkerfi greinir ójafnvægi í pöntunarnetinu stofnar það sjálfkrafa aðgerðaboð til að tilkynna notanda um það. Aðgerðaboð eru kerfismynduð köll fyrir notanda aðgerðar sem tilgreina upplýsingar um ójafnvægi og tillögur um hvernig á að endurheimta jafnvægi í pöntunarneti. Þær birtast sem áætlunarlínur á síðunni **Áætlunarvinnublað** þegar **Sækja aðgerðaboð** er valið. Að auki eru aðgerðaskilaboð birt á áætlanagerðarlínur sem eru búnir til með áætlunarkeyrslu til að endurspegla tillögur skipulagningu kerfisins snýst um hvernig á að endurheimta jafnvægi við pantanakerfið. Í báðum tilvikum eru tillögur keyrðar á pöntunarnet, þegar þú velur **Framkvæma aðgerðaboð**  

 Aðgerðarboð nær yfir eitt uppskriftarstig í einu. Ef notandinn samþykkir aðgerðaboðin getur það leitt til viðbótaraðgerðaboða á næsta uppskriftarstigi.  

 Eftirfarandi tafla sýnir aðgerðaboð sem eru fyrir hendi.  

|Aðgerðarboð|Description|  
|--------------------|---------------------------------------|  
|**Breyta magni**|Breytir magn á núverandi birgðapöntun til að standa straum að breytingum eða nýja eftirspurn.|  
|**Endurtímasetja**|Endurtímasetja skiladag fyrirliggjandi pöntunar.|  
|**Endurtímas. og br. magni**|Endurtímasetur skiladag og breytir magninu í fyrirliggjandi pöntun.|  
|**Nýtt**|Stofnar nýja pöntun ef ekki er hægt að mæta eftirspurn með öðrum af fyrri aðgerðaskilaboðum.|  
|**Hætta við**|Hætta við fyrirliggjandi pöntun.|  

 Pöntunarrakningarkerfið reynir alltaf að leysa úr ójafnvægi í fyrirliggjandi pöntunarneti. Ef þetta er ekki mögulegt eru send aðgerðaboð um að búa til nýja pöntun. Hér á eftir er forgangsraðaður listi sem pöntunarrakningakerfið notar þegar það greinir hvernig á að enrudheimta stöðu. Ef viðbótareftirspurn hefur komið inn í pöntunarnetið leitast kerfið við að rekja pantanir gegnum eftirfarandi athuganir:  

1.  Stöðva allt umfram framboð á núverandi pöntunarrakningarfærslu fyrir þessa eftirspurn.  
2.  Athuga áætlaðar og tímasettar móttökur í röð dagsetningu móttöku. Nýjasta mögulega dagsetning er valin.  
3.  Athuga tiltækar birgðir.  
4.  Athuga hvort birgðapöntun er til staðar í núverandi pöntunarrakningarfærslu. Ef svo er sendir kerfið út aðgerðaboð af gerðinni **Breyting** til að stækka pöntunina.  
5.  Athuga að engin birgðapöntun sé til staðar í núverandi pöntunarrakningarfærslu. Ef svo er sendir kerfið út aðgerðaboð af gerðinni **Nýtt** til að búa til nýja pöntun.  

 Opin eftirspurn fer í gegnum listann og mótfærir tiltækt framboð við hvern punkt. Eftirstandandi eftirspurn er einnig uppfyllt í athugun 4 eða athugun 5.  

 Ef minnkun í eftirspurnarmagni á sér stað reynir pöntunarrakningarkerfið að leysa úr ójafnvæginu með því að gera fyrrnefndar athuganir í öfugri röð. Þetta þýðir að eldri aðgerðaboð gætu verið breytt eða jafnvel eytt, ef nauðsyn krefur. Pöntunarrakningarkerfið sýnir notandanum alltaf hreina útkomu útreikninga sinna.  

## Rakning pöntunar og áætlun  
 Þegar áætlanakerfi er keyrt eyðir það öllum fyrirliggjandi rakningarfærslum og aðgerðaboðafærslum og endurstofnar þær sem tillgöur að áætlunarlínum í samræmi við framboð/eftirspurn pör og forgangsverkefni. Þegar áætlunarkeyrslu er lokið er pöntunarkerfið í jafnvægi.  

### Áætlunarkerfi samanborið við Pöntunarrakningu og Aðgerðarboð  
 Eftirfarandi samanburður sýnir muninn á aðferðum sem eru notaðar við skipulagningu kerfisins til að búa til áætlanagerðarlínutillögur og þeim aðferðum sem eru notaðar með pöntunarrakningarkerfinu til að búa til pöntunarrakningarfærslur og aðgerðaskilaboð.  

-   Áætlanakerfið tekur á öllu mynstri framboðs og eftirspurnar varðandi tiltekna vöru en pantanarakning tekur á pöntuninni sem virkjaði það.  

-   Áætlanakerfið tekur á öllum stigum uppskriftarstigveldisins en pöntunarrakning tekur aðeins og einu stigi í einu.  

-   Áætlanakerfið kemur á tengslum á milli eftirspurnar og framboðs samkvæmt forgangsröðuðum gjalddaga. Pöntunarrakning býr til tengingar á milli eftirspurnar og framboðs samkvæmt pöntunarfærsluröðinni.  

-   Áætlanakerfið tekur áætlanafæribreytur til greina, en það gerir pöntunarrakning ekki.  

-   Áætlanakerfið býr til tengla í notandavirkjaðri runustillingu þegar það jafnar eftirspurn og framboð, en pantanarakning býr tenglana til sjálfkrafa og gagnvirkt um leið og notandinn færir inn pantanir.  

## Sjá einnig  
[Hönnunarupplýsingar: Miðlægar hugmyndir áætlanakerfisins](design-details-central-concepts-of-the-planning-system.md)   
[Hönnunarupplýsingar: framboðsáætlun](design-details-supply-planning.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
