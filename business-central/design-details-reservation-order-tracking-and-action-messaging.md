---
title: 'Upplýsingar um hönnun - frátekning, pantanarakning og aðgerðaboð | Microsoft-skjöl'
description: Frátekningarkerfið er yfirgripsmikið og felur í sér samtengda og samhliða eiginleika Rakningar pöntunar og aðgerðaboða.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'design, replenishment, reordering'
ms.date: 08/06/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

# Hönnunarupplýsingar: frátekning, pöntunarrakning og aðgerðaboð

Alhliða frátekningarkerfið felur í sér samtengda og samhliða eiginleika Rakningar pöntunar og Aðgerðaboða.  

Í kjarna frátekningarkerfisins er tenging eftirspurnarfærslu og samsvarandi framboðsfærslu, annaðhvort með frátekningu eða pöntunarrakningu. Frátekning er tengill sem notandi myndar og pöntunarrakningarfærsla er tengill sem kerfi myndar. Vörumagn sem fært er inn í frátekningarkerfið er annaðhvort frátekið eða pöntun rakið, en ekki bæði á sama tíma. Hvernig kerfið meðhöndlar vöru veltur á því hvernig varan er sett upp.  

Frátekningarkerfið vinnur með áætlanakerfinu með því að búa til aðgerðaboð á áætlunarlínum í áætlunarkeyrslu. Aðgerðarboð geta talist viðbót við skráningu pöntunarrakningar. Aðgerðaboð, hvort sem þau eru stofnuð kvikt í pöntunarrakningu eða við áætlunarkeyrslu, bjóða upp á hentugt verkfærui fyrir skilvirka framboðsáætlun.  

> [!NOTE]  
> Áskilinn magn er hunsað af áætlunarkerfi, það er, harði tengilinn sem er á milli framboðs og eftirspurnar er ekki hægt að breyta í gegnum áætlanagerð.  

 Frátekningarkerfið myndar einnig skipulagsgrunn fyrir vörurakningarkerfið. Nánari upplýsingar eru í [Hönnunarupplýsingar: Vörurakning](design-details-item-tracking.md).  

 <!--For more detailed information about how the reservation system works, see the _Reservation Entry Table_ white paper on [PartnerSource](https://go.microsoft.com/fwlink/?LinkId=258348).  -->
<!--
> [!NOTE]
> [!INCLUDE [locations-cronus](includes/locations-cronus.md)]
-->

## Frátekning  

 Frátekning er fastur tengill sem tengir sérstaka eftirspurn og sérstakt framboð. Þessi tengill hefur beint áhrif á síðari birgðafærslu og tryggir rétta notkun vörufærsla vegna kostnaðar. Frátekning hnekkir sjálfgefinni aðferð kostnaðarútreiknings fyrir vöru. Nánari upplýsingar eru í [Hönnunarupplýsingar: Vörurakning](design-details-item-tracking.md).  

 Síðan **Frátekning** er aðgengileg úr öllum pöntunarlínum af bæði eftirspurn og framboðstegundum. Á þessari síðu getur notandinn tilgreint hvaða eftirspurn eða framboðsfærsla á að stofna frátekningu tengja í átt til. Frátekning samanstendur af færslupörum með sama færslunúmer. Ein færsla er með neikvætt formerki og vísar á eftirspurn. Hin færslan er með jákvæðu merki og vísar á framboðið. Þessar færslur eru vistaðar í *töflunni Frátekningarfærsla með stöðugildinu* Frátekning *·*. Notandinn getur skoðað allar frátekningarnar á síðunni **Frátekningarfærslur**.  

### Mótbókun í frátekningum  

 Frátekningar eru gerðar gegn tiltæku vörumagni. Vara til ráðstöfunar er reiknuð út í undirstöðuatriðum á eftirfarandi hátt:  

 `available quantity = inventory + scheduled receipts - gross requirements`

 Eftirfarandi tafla sýnir upplýsingar um pöntunarneteiningar sem eru hluti af framboðsútreikningi.  

||Reitur í T27 vöru|Upprunatafla|Töfluafmörkun|Upprunareitur|  
|-|------------------|------------------|------------------|------------------|  
|**Birgðir**|Birgðir|Birgðafærsla|Á ekki við|Magn|  
|**Tímasettar móttökur**|Mótt. afgr. framl.pönt. (magn)|Framl.pöntunarlína|Áætlað|Eftirstöðvar (stofn)|  
|**Tímasettar móttökur**|Mótt. útg. pöntunar (magn)|Framl.pöntunarlína|=Útgefið|Eftirstöðvar (stofn)|  
|**Tímasettar móttökur**|Magn í samsetningarpöntun|Yfirskrift samsetningar|Pantanir|Eftirstöðvar (stofn)|  
|**Tímasettar móttökur**|Magn í innk.pöntun|Innkaupalína|Pantanir|Óafgreitt magn (stofn)|  
|**Tímasettar móttökur**|Mótt. millif. pönt. (Magn)|Millifærslulína|Á ekki við|Útistandandi magn|  
|**Brúttóþörf**|Magn í sölupöntun|Sölulína|Pantanir|Óafgreitt magn (stofn)|  
|**Brúttóþörf**|Tímasett þörf (magn)|Framl.pöntunaríhlutur|<> Hermdar|Eftirstöðvar (stofn)|  
|**Brúttóþörf**|Magn í sams.íhlutum|Samsetningarlína|Pantanir|Eftirstöðvar (stofn)|  
|**Brúttóþörf**|Afh. millif. pönt. (magn)|Millifærslulína|Á ekki við|Útistandandi magn|  

 Nánari upplýsingar eru í [Hönnunarupplýsingar: Til ráðstöfunar í vöruhúsinu](design-details-availability-in-the-warehouse.md).  

### Handvirk frátekning  

Þegar notandi býr viljandi til frátekningu fær notandinn fullt eignarhald og ábyrgð á þessum vörum. Þetta þýðir að notandinn þarf einnig handvirkt breyta eða hætta við frátekningu. Slíkar handvirkar breytingar geta valdið sjálfvirkri breytingu á viðkomandi frátekningum.  

Eftirfarandi tafla sýnir hvenær og hvaða breytingar geta orðið:  

|Aðgerð notanda|Kerfisviðbrögð|  
|-----------------|---------------------|  
|Minnka frátekið magn|Tengdir magnreitir eru uppfærðir.|  
|Breyting dagsetningarreita|Tengdir dagsetningarreitir eru uppfærðir.<br /><br /> **Athugið:** Ef gjalddaga eftirspurnar er breytt til að hann komi á undan afhendingardegi eða gjalddaga framboðsins er hætt við frátekninguna.|  
|Eyða pöntuninni|Hætt við frátekningu.|  
|Breyting staðsetninga, hólfa, afbrigða, raðnúmers, eða lotunúmers.|Hætt við frátekningu.|  

> [!NOTE]  
> Aðgerðin fyrir bindingu á eftir áætlun getur einnig breytt fyrirvörum án þess að notandi sé upplýstur, með þvi´að endurraða ótilgreindum fyrirvörum rað- eða lotunúmera. Nánari upplýsingar eru í [Hönnunarupplýsingar: Vörurakning og frátekningar](design-details-item-tracking-and-reservations.md).  

### Sjálfvirk frátekning  

Hægt er að setja birgðaspjaldið þannig upp að vörur séu sjálfkrafa teknar frá samkvæmt eftirspurn, t.d. sölupöntunum. Þá er gerð frátekning á birgðum, innkaupapöntunum og samsetningarpöntunum og framleiðslupöntunum. Viðvörun er gefin út ef birgðir eru ekki nægilegar.  

Þar að auki taka ýmsar áætlunaraðgerðir sjálfkrafa frá vörum til að halda eftirspurn sem tengist tilteknu framboði. Í pöntunarrakningarfærslum fyrir slíka áætlunartengla eru **Frátekning** í reitnum **Staða** frátekningar í töflunni *Frátekningarfærsla* . Sjálfvirkar frátekningar eru búnar til í eftirtöldum tilvikum:  

- Framleiðslupöntun í mörgum stigum þar sem reiturinn **Framleiðslustefna** viðkomandi yfir- og undirvöru er stilltur á **Eftir pöntun**. Áætlunarkerfið stofnar frátekningar milli framleiðslupöntunar yfireining og undirliggjandi framleiðslupöntunar til að tryggja að það vinnist saman. Þessi frátekningarbinding hnekkir sjálfgefnum kostnaði og jöfnunaraðferð vörunnar.  

- Framleiðsla, samsetning eða innkaupapöntun þar sem reiturinn **Framleiðslustefna** viðkomandi vöru er stilltur á **Pöntun**. Áætlanakerfið býr til frátekningar á milli eftirspurnar og ætlaðs framboð til að tryggja að tilgreint framboð verði búið til. Nánari upplýsingar eru í [Pöntun](design-details-handling-reordering-policies.md#order).  

- Framleiðslupöntun sem stofnuð er með eiginleikanum **Sölupantanaáætlun** er tengd við sölupöntun með sjálfvirkri frátekningu.  

- Samsetningarpöntun stofnuð sjálfvirkt fyrir sölupöntunarlínu til að uppfylla magnið í reitnum **Magn til samsetningar í pöntun** . Þessi sjálfvirka frátekning tengir sölueftirspurn og framboðssamsetningu þannig að þeir sem sjá um sölupantanir geti stillt og lofað samsetningarvörunni beint við viðskiptamanninn. Að auki, frátekning tengir samsetningarfrálag við sölupöntunarlínu í gegnum afhendingaraðgerðir sem uppfyllir pantanir viðskiptavini þess.  

Áætlunarkerfið úthlutar sjálfkrafa frátekningarstöðunni **Umframmagn** fyrir framboð eða eftirspurn sem ekki er úthlutað. Þetta gæti leitt til eftirspurnar sem er vegna fyrirsjáanlegs magns eða áætlunarfæribreyta sem slegnar hafa verið inn. Þetta er lögmæt umframbirgðatal sem kerfið þekkir og gefur ekki tilefni til aðgerðaboða. Umframbirgðir geta einnig verið ósviknar, umframbirgðir eða eftirspurn sem er órakin. Þetta gefur til kynna ójafnvægi í pöntunarnetinu sem veldur því að kerfið gefi út aðgerðaboð. Hafið í huga að aðgerðaboð sem leggur til breytingu á magni á alltaf við gerðina **Umframbirgðir** Nánari upplýsingar eru í [Dæmi: Rakning pöntunar í sölu, framleiðslu og millifærslum](#example-order-tracking-in-sales-production-and-transfers) í þessari grein.  

Sjálfvirkar frátekningar sem stofnaðar eru við áætlaða keyrslu eru meðhöndlaðar á eftirfarandi hátt:  

- Þær eiga við vörumagn sem er innifalið í útreikningum á til ráðstöfunar, rétt eins og handvirkar frátekningar. Nánari upplýsingar eru í hlutanum "Mótfært í frátekningu" í þessari grein.  

- Þær eru teknar með og hugsanlega breytt í áætlunarkeyrslum sem á eftir koma, ólíkt fráteknum vörum sem eru handvirkt fráteknar.  

## Rakning pöntunar  

Pöntunarrakning hjálpar til við viðhalda gildri framboðsáætlun með því að bjóða upp á yfirlit yfir mótbókun á milli eftirspurnar og framboðs í pöntunarnetinu. Pöntunarrakningarfærslan er undirstaða fyrir gangvirk aðgerðaboð og tilögur um áætlanalínur á meðan áætlun er í keyrslu.  

> [!NOTE]  
> Pöntunarrakningarkerfið jafnar tiltækar birgðir um leið og pantanir eru færðar inn í pöntunarnetið. Þetta gefur til kynna að kerfið setji ekki í forgang pantanir sem kunna að vera meiri áríðandi vegna skiladags. Því er það undir rökum áætlanakerfis eða skynsemi áætlanagerðarmanns komið að raða þessum forgangsverkefnum á skynsamlegan hátt.  

> [!NOTE]  
> Rakningarstefna pöntunar og aðgerðin Sækja aðgerðarboð eru ekki samþætt verkefnum. Það þýðir að eftirspurn sem tengist verki er ekki rakin sjálfkrafa. Þar sem hún er ekki rakin gæti það valdið því að notkun fyrirliggjandi áfyllingar með verkupplýsingum er rakin til annarrar eftirspurnar, til dæmis sölupöntunar. Þar af leiðandi gæti komið upp staða þar sem upplýsingar um tiltækar birgðir eru ekki samstilltar.  

### Pöntunarnetið  

Pöntunarrakningarkerfið byggir á þeirri meginreglu að pöntunarnetið verði alltaf að halda jafnvægi og tryggja að allar eftirspurnir sem koma inn í kerfið séu mótfærðar með samsvarandi framboði og öfugt. Kerfið nær þessu með því að bera kennsl á röklæga tengla milli allra eftirspurnar og birgðafærslna í pöntunarnetinu.  

Þessi meginregla felur í sér að breyting á eftirspurn leiðir til samsvarandi ójafnvægi á framboðshlið pöntunarnets. Hins vegar leiðir birgðabreyting til samsvarandi ójafnvægis á eftirspurnarhlið pantanakerfisins. Í raun er pöntunarnetið í síbreytilegu flæði því notendur slá inn, breyta og eyða pöntunum. Pöntunarrakning vinnur pantanir kvikt, bregst við öllum breytingum á þeim tíma sem þær eru færðar inn í kerfið og verða hluti af pöntunarnetinu. Um leið og ný pöntunarrakning er stofnuð er pöntunarnetið í jafnvægi, en aðeins þangað til að næsta breyting á sér stað.  

Til að auka gagnsæi útreikninga í áætlanakerfi sýnir síðan **Óraktar áætlunareiningar** órekið magn sem lýsir mismun á magni milli þekktan eftirspurn og leiðbeinandi framboð. Hver lína á síðunni vísar til orsakar af umframmagni, svo sem **Standandi pöntun**, **Öryggisbirgðastig**, **Fast endurpöntunarmagn**, **Lágmarks pöntunarmagn**, **Sléttun** eða **Hömlur**.  

### Mótfærslu í pöntunarrakningu  

Ólíkt frátekningum, sem getur aðeins verið gert gegn fyrirliggjandi vörumagni, er pantanarakning möguleg fyrir allar pöntunarnetseiningar sem eru hluti af netpantanaútreikningi áætlanakerfisins. Nettókröfur eru reiknaðar út með eftirfarandi hætti:  

`net requirements = gross requirements + reorder point - scheduled receipts - planned receipts - projected available balance`  

> [!NOTE]  
> Eftirspurn sem er tengt við spár eða skipulags þáttum er ekki raktir eftir pöntun.  

### Dæmi: Rakning pöntunar í sölu, framleiðslu og millifærslum  

Eftirfarandi dæmi sýnir hvaða pöntunarrakningarfærslur eru stofnaðar í *töflunni Frátekningarfærsla* sem niðurstöður ýmissa breytinga á pöntunarneti.  

Gera skal ráð fyrir eftirfarandi gögnum fyrir tvær vörur sem eru uppsettar fyrir pöntunarrakningu.  

|Atriði|Mæliþáttur|Upplýsingar|
|-|-|-|
|Vara 1|Nafn|Íhlutur|
||Til ráðstöfunar|100 einingar á Austurlandi<br /><br />- 30 einingar af LOTA<br />- 70 einingar af LOTB|  
|Vara 2|Nafn|Framleidd vara|
||Framleiðsluuppskrift|1 magn á íhlut|  
||Eftirspurn|Sala fyrir 100 einingar á WEST staðsetningu|  
||Framboð|Útgefin framleiðslupöntun (mynduð með aðgerðinni *Sölupöntunaráætlun* fyrir sölu 100 einingar)|  

Á síðunni **Uppsetning** framleiðslu er reiturinn **Íhlutir á staðnum stilltur** á *Austur.*

Eftirfarandi rakningarfærslur pöntunar eru til í *töflunni Frátekningarfærsla* samkvæmt gögnum í töflunni.  

<!--![First example of order tracking entries in Reservation Entry table.](media/supply_planning_RTAM_1.png "supply_planning_RTAM_1")  -->
**Frátekningarfærslur**

|Færslunr.|Jákvætt|Vörunr.|Kóði birgðageymslu|Magn|Frátekningarstaða|Heimildasamstæða|Lotunúmer|Upprunagerð|Upprunakenni|Binding|  
|--------|--------|--------|-------------|--------|------------------|-----------|-------|-----------|---------|-------| 
|8|-|ÞÁTTUR|AUSTUR|-70|Rakning|Íhlutur|-|5407|101004|-|
|8|Já|ÞÁTTUR|AUSTUR|70|Rakning|Íhlutur|LOTAB|32|-|-| 
|9|-|ÞÁTTUR|AUSTUR|-30|Rakning|Íhlutur|-|5407|1001004|-| 
|9|Já|ÞÁTTUR|AUSTUR|30|Rakning|Íhlutur|LOTA|32|-|-| 
|10|-|FRAMLEIDD VARA|VESTUR|-100|Frátekning|Framleidd vara|-|37|1001|Pöntun-fyrir-pöntun|
|10|Já|FRAMLEIDD VARA|VESTUR|100|Frátekning|Framleidd vara|-|5406|101004|Pöntun-fyrir-pöntun|


#### Færslunúmer 8 og 9  

Fyrir íhlutaþörfina fyrir LOTA og LOTA eru rakningartenglar pantana stofnaðir úr eftirspurninni í töflu 5407, *Framl.pöntunaríhlutur*, til framboðsins í töflu 32, *Birgðafærsla*.  **Í reitnum Staða** frátekningar er *Rakning* til að gefa til kynna að þessar færslur séu kvikar rakningartengingar pöntunar milli framboðs og eftirspurnar.  

> [!NOTE]  
> Reiturinn **Lotunr.** reiturinn er auður í eftirspurnarlínunum vegna þess að lotunúmerin eru ekki tilgreind í íhlutalínum útgefnu framleiðslupöntunarinnar.  

#### Færslunúmer 10  

Úr sölueftirspurninni í töflu 37,Sölulínur *er* rakning pöntunar tengja stofnuð fyrir framboðið í töflu 5406, *Framl.pöntunarlína*.  **Í reitnum Staða** frátekningar er *Frátekning* og í reitnum **Binding** er *Pöntun-eftir pöntun*. Það er vegna þess að útgefna framleiðslupöntunin var mynduð sérstaklega fyrir sölupöntunina og verður að vera tengd, ólíkt rakningartenglum pöntunar með frátekningarstöðuna Rakning, sem er búin til og breytt. Nánari upplýsingar eru í hlutanum [Sjálfvirkar frátekningar](#automatic-reservations) í þessari grein.  

 Á þessum tímapunkti , eru 100 einingar í LOTA og LOTB flutt til WEST með flutningspöntun.  

> [!NOTE]  
> Aðeins afhending millifærslupöntunar er bókuð á þessum tímapunkti, ekki móttaka.  

 Nú eru eftirfarandi rakningarfærslur pöntunar til í *töflunni Frátekningarfærsla* .  

<!-- ![Second example of order tracking entries in Reservation Entry table.](media/supply_planning_RTAM_2.png "supply_planning_RTAM_2")  -->
**Frátekningarfærslur**

|Færslunr.|Jákvætt|Vörunr.|Kóði birgðageymslu|Magn|Frátekningarstaða|Heimildasamstæða|Lotunúmer|Upprunagerð|Upprunakenni|Binding|  
|---------|--------|--------|-------------|--------|------------------|-----------|-------|-----------|---------|-------| 
|9|-|ÞÁTTUR|AUSTUR|-30|Umframbirgðir|Íhlutur|-|5407|1001004|-| 
|10|-|FRAMLEIDD VARA|VESTUR|-100|Frátekning|Framleidd vara|-|37|1001|Pöntun-fyrir-pöntun|
|10|Já|FRAMLEIDD VARA|VESTUR|100|Frátekning|Framleidd vara|-|5406|101004|Pöntun-fyrir-pöntun|
|12|Já|ÞÁTTUR|VESTUR|70|Umframbirgðir|Íhlutur|LOTAB|5741|1011|-| 
|14|Já|ÞÁTTUR|VESTUR|30|Umframbirgðir|Íhlutur|LOTA|5741|1011|-| 
|15|Já|ÞÁTTUR|ÚT. TRJÁBOLUR.|70|Umframbirgðir|Íhlutur|LOTAB|32|-|-| 
|16|Já|ÞÁTTUR|ÚT. TRJÁBOLUR.|30|Umframbirgðir|Íhlutur|LOTA|32|-|-| 

#### Færslunúmer 8 og 9  

Rakningarfærslur pantana fyrir loturnar tvær íhlutsins sem endurspegla eftirspurn í töflu 5407 er breytt úr frátekningarstöðu Rakningar í *Umframmagn* . *·* Ástæðan er sú að birgðir sem tengdar voru áður, í töflu 32, eru notaðar við afhendingu millifærslupöntunarinnar.  

Raunverulegur afgangur, eins og í þessu tilfelli, endurspeglar umframframboð eða eftirspurn sem helst órakin. Það er vísbending um ójafnvægi í pöntunarnetinu, sem býr til aðgerðarboð af áætlunarkerfinu nema það sé leyst gagnvirkt.  

#### Færslunúmer 12 til 16  

Þar sem tvær lotur íhlutarins eru bókaðar í millifærslupöntunina sem afhentar en ekki mótteknar eru allar tengdar jákvæðar rakningarfærslur pöntunar af frátekningartegundinni *Umframmagn* sem gefur til kynna að þeim sé ekki úthlutað á neina eftirspurn. Ein færsla tengist töflu 5741,Millifærslulínu *fyrir* hvert lotunúmer og eina færslu tengist birgðafærslunni í millifærslustaðnum þar sem vörurnar eru nú til.  

Á þessum tímapunkti í dæminu er millifærslupöntun íhluta frá *AUSTUR* til *WEST* bókuð sem móttekin.  

Nú eru eftirfarandi rakningarfærslur pöntunar til í *töflunni Frátekningarfærsla* .  

<!-- ![Third example of order tracking entries in Reservation Entry table.](media/supply_planning_RTAM_3.png "supply_planning_RTAM_3") -->
 **Frátekningarfærslur**

|Færslunr.|Jákvætt|Vörunr.|Kóði birgðageymslu|Magn|Frátekningarstaða|Heimildasamstæða|Lotunúmer|Upprunagerð|Upprunakenni|Binding|  
|---------|--------|--------|-------------|--------|------------------|-----------|-------|-----------|---------|-------| 
|8|-|ÞÁTTUR|AUSTUR|-70|Umframbirgðir|Íhlutur|-|5407|101004|-| 
|9|-|ÞÁTTUR|AUSTUR|-30|Umframbirgðir|Íhlutur|-|5407|1001004|-|
|10|-|FRAMLEIDD VARA|VESTUR|-100|Frátekning|Framleidd vara|-|37|1001|Pöntun-fyrir-pöntun|
|10|Já|FRAMLEIDD VARA|VESTUR|100|Frátekning|Framleidd vara|-|5406|101004|Pöntun-fyrir-pöntun|
|17|Já|ÞÁTTUR|VESTUR|70|Umframbirgðir|Íhlutur|LOTAB|32|-|-| 
|18|Já|ÞÁTTUR|VESTUR|30|Umframbirgðir|Íhlutur|LOTA|32|-|-| 

Pöntunarrakningarfærslurnar eru nú svipaðar og fyrsti punkturinn í dæminu áður en millifærslupöntunin var bókuð sem afhent eingöngu, nema færslur fyrir íhlutinn eru nú umframmagn *frátekningar*. Það er vegna þess að íhlutaþörfin er enn í *austur* birgðageymslunni sem sýnir að **reiturinn Kóti** birgðageymslu á íhlutalínunni framleiðslupöntun hefur *AUSTUR* sem uppsetningu í reitnum **Íhlutir á staðnum** . Framboðið sem var úthlutað á þessa eftirspurn áður var flutt í birgðageymsluna WEST *og er ekki hægt að rekja að* fullu nema íhlutaþörfinni á framleiðslupöntunarlínunni sé breytt *í birgðageymsluna WEST* .  

Á þessum tímapunkti í dæminu **er Kóti** birgðageymslu í íhlutalínunni framleiðslupöntun stilltur á *WEST*. Auk þess er á síðunni **Vörurakningarlínur**, 30 einingar LOTA og 70 eininga LOTA úthlutað á íhlutalínu framleiðslupöntunarinnar.  

Nú eru eftirfarandi rakningarfærslur pöntunar til í *töflunni Frátekningarfærsla* .  

<!-- ![Fourth example of order tracking entries in Reservation Entry table.](media/supply_planning_RTAM_4.png "supply_planning_RTAM_4")   -->
 **Frátekningarfærslur**

|Færslunr.|Jákvætt|Vörunr.|Kóði birgðageymslu|Magn|Frátekningarstaða|Heimildasamstæða|Lotunúmer|Upprunagerð|Upprunakenni|Binding|  
|---------|--------|--------|-------------|--------|------------------|-----------|-------|-----------|---------|-------| 
|10|-|FRAMLEIDD VARA|VESTUR|-100|Frátekning|Framleidd vara|-|37|1001|Pöntun-fyrir-pöntun|
|10|Já|FRAMLEIDD VARA|VESTUR|100|Frátekning|Framleidd vara|-|5406|101004|Pöntun-fyrir-pöntun|
|21|-|ÞÁTTUR|VESTUR|-70|Rakning|Íhlutur|LOTAB|5407|101004|-| 
|21|Já|ÞÁTTUR|VESTUR|70|Rakning|Íhlutur|LOTAB|32|-|-| 
|22|-|ÞÁTTUR|VESTUR|-30|Rakning|Íhlutur|LOTA|5407|1001004|-| 
|22|Já|ÞÁTTUR|VESTUR|30|Rakning|Íhlutur|LOTA|32|-|-| 

#### Færslunúmer 21 og 22  

Þar sem íhluturinn þarf að breytast í *staðsetningu WEST* og framboðið er tiltækt sem birgðafærslur í birgðageymslunni *WEST* eru allar pöntunarrakningarfærslur fyrir lotunúmerin tvö nú að fullu raktar, gefið til kynna með frátekningarstöðu *rakningar*.  

Reiturinn **Lotunr.** Nú er reiturinn fylltur út í pöntunarrakningarfærslunni fyrir töflu 5407 vegna þess að lotunúmerin voru tengd í íhlutalínur framleiðslupöntunarinnar.  

## Aðgerðaboð  

Þegar pöntunarrakningarkerfi greinir ójafnvægi í pöntunarnetinu stofnar það sjálfkrafa aðgerðaboð til að tilkynna notanda um það. Aðgerðarboð eru köll sem kalla á notandaaðgerðir sem tilgreina upplýsingar um ójafnvægið og tillögur um hvernig eigi að endurheimta jafnvægi á pöntunarnetið. Þeir birtast sem áætlunarlínur á síðunni **Áætlunarvinnublöð** þegar aðgerðin Sækja aðgerðarboð **er valin** . Þar að auki eru aðgerðarboð í áætlunarlínum mynduð við áætlunarkeyrslan til að endurspegla tillögur áætlunarkerfisins um að endurheimta stöðu á pöntunarnetið. Í báðum tilvikum eru tillögurnar keyrðar á pöntunarnetinu þegar aðgerðin Framkvæma aðgerðarboð **er valin** .  

Aðgerðarboð nær yfir eitt uppskriftarstig í einu. Ef notandinn samþykkir aðgerðarboðin gæti það gefið viðbótaraðgerðarboð á næsta uppskriftarstigi.  

Eftirfarandi tafla sýnir aðgerðaboð sem eru fyrir hendi.  

|Aðgerðarboð|Description|  
|--------------------|---------------------------------------|  
|**Breyta magni**|Breytir magn á núverandi birgðapöntun til að standa straum að breytingum eða nýja eftirspurn.|  
|**Endurtímasetja**|Endurtímasetja skiladag fyrirliggjandi pöntunar.|  
|**Endurtímas. og br. magni**|Endurtímasetur skiladag og breytir magninu í fyrirliggjandi pöntun.|  
|**Nýtt**|Stofnar nýja pöntun ef ekki er hægt að uppfylla eftirspurn með fyrri aðgerðarboðum.|  
|**Hætta við**|Hætta við fyrirliggjandi pöntun.|  

Pöntunarrakningarkerfið reynir alltaf að leysa úr ójafnvægi í fyrirliggjandi pöntunarneti. Ef það er ekki mögulegt birtast aðgerðarboð til að stofna nýja pöntun. Hér á eftir er forgangsraðaður listi sem pöntunarrakningakerfið notar þegar það greinir hvernig á að enrudheimta stöðu. Ef viðbótareftirspurn kemur inn á pöntunarnetið leitar kerfið að pöntunarrakningu með eftirfarandi tékkum:  

1. Stöðva allt umfram framboð á núverandi pöntunarrakningarfærslu fyrir þessa eftirspurn.  
1. Athuga áætlaðar og tímasettar móttökur í röð dagsetningu móttöku. Nýjasta mögulega dagsetning er valin.  
1. Athuga tiltækar birgðir.  
1. Athuga hvort birgðapöntun er til staðar í núverandi pöntunarrakningarfærslu. Ef svo er gefur kerfið út aðgerðarboð af gerðinni *Breyta* til að auka pöntunina.  
1. Athuga að engin birgðapöntun sé til staðar í núverandi pöntunarrakningarfærslu. Ef svo er gefur kerfið út aðgerðarboð af gerðinni *Nýtt* til að stofna nýja pöntun.  

Opin eftirspurn fer í gegnum listann og mótfærir tiltækt framboð við hvern punkt. Eftirstandandi eftirspurn er einnig uppfyllt í athugun 4 eða athugun 5.  

Ef minnkun í eftirspurnarmagni á sér stað reynir pöntunarrakningarkerfið að leysa úr ójafnvæginu með því að gera fyrrnefndar athuganir í öfugri röð. Þetta þýðir að eldri aðgerðaboð gætu verið breytt eða jafnvel eytt, ef nauðsyn krefur. Pöntunarrakningarkerfið sýnir notandanum alltaf hreina útkomu útreikninga sinna.  

## Rakning og áætlun pöntunar  

Þegar áætlanakerfi er keyrt eyðir það öllum fyrirliggjandi rakningarfærslum og aðgerðaboðafærslum og endurstofnar þær sem tillgöur að áætlunarlínum í samræmi við framboð/eftirspurn pör og forgangsverkefni. Þegar áætlunarkeyrslan lýkur er pöntunarnetið í stöðu.  

### Áætlunarkerfi samanborið við rakningu pöntunar og aðgerðaboð  

 Eftirfarandi samanburður sýnir muninn á aðferðum sem eru notaðar við skipulagningu kerfisins til að búa til áætlanagerðarlínutillögur og þeim aðferðum sem eru notaðar með pöntunarrakningarkerfinu til að búa til pöntunarrakningarfærslur og aðgerðaskilaboð.  

- Áætlanakerfið tekur á öllu mynstri framboðs og eftirspurnar varðandi tiltekna vöru en pantanarakning tekur á pöntuninni sem virkjaði það.  

- Áætlanakerfið tekur á öllum stigum uppskriftarstigveldisins en pöntunarrakning tekur aðeins og einu stigi í einu.  

- Áætlanakerfið kemur á tengslum á milli eftirspurnar og framboðs samkvæmt forgangsröðuðum gjalddaga. Pöntunarrakning býr til tengingar á milli eftirspurnar og framboðs samkvæmt pöntunarfærsluröðinni.  

- Áætlunarkerfið tekur áætlunarfæribreytur með í reikninginn en rakning pöntunar ekki.  

- Áætlanakerfið býr til tengla í notandavirkjaðri runustillingu þegar það jafnar eftirspurn og framboð, en pantanarakning býr tenglana til sjálfkrafa og gagnvirkt um leið og notandinn færir inn pantanir.  

## Sjá einnig .  

[Hönnunarupplýsingar: Miðlægar hugmyndir áætlanakerfisins](design-details-central-concepts-of-the-planning-system.md)  
[Hönnunarupplýsingar: framboðsáætlun](design-details-supply-planning.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
