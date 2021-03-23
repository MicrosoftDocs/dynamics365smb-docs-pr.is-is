---
title: Hönnunarupplýsingar - Meðalkostnaður | Microsoft Docs
description: Meðalkostnaður vöru er reiknaður með reglubundnu vegnu meðaltali, miðað við meðalkostnaðartímabil sem er sett upp í Business Central.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 70b0f4c5a858b73cb0f872bb1bfb92ebc56ded42
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5380707"
---
# <a name="design-details-average-cost"></a>Hönnunarupplýsingar: Meðalkostnaður
Meðalkostnaður vöru er reiknaður með reglubundnu vegnu meðaltali, miðað við meðalkostnaðartímabil sem er sett upp í [!INCLUDE[prod_short](includes/prod_short.md)].  

 Virðisdagsetningin er valin sjálfkrafa.  

## <a name="setting-up-average-cost-calculation"></a>Setja upp meðalkostnaðrverðútreikning  
 Eftirfarandi tafla lýsir tveimur reitum á síðunni **Uppsetning birgða** sem verður að fylla út til að gera meðalkostnaðarútreikning virkan.  

|Svæði|Lýsing|  
|---------------------------------|---------------------------------------|  
|**Tímabil meðalinnk.verðs**|Tilgreinir á hvaða tímabili meðalkostnaður er reiknaður í. Eftirfarandi möguleikar eru til staðar:<br /><br /> -   **Dagur**<br />-   **Vika**<br />-   **Mánuður**<br />-   **Reikningstímabil**<br /><br /> Öll birgðaminnkun sem var bókuð innan tímabils meðalinnkaupsverðs fær meðalinnkaupsverðið sem reiknað er fyrir þetta tímabil.|  
|**Meðalinnk.verð Teg. útreikn.**|Tilgreinir hvernig meðalkostnaður er reiknaður. Eftirfarandi möguleikar eru til staðar:<br /><br /> -   **Vara**<br />-   **Vörur, afbrigði og staðsetning**<br />     Ef þessi kostur er valinn reiknar kerfið út meðalinnkaupsverð á vöru fyrir hverja birgðageymslu og fyrir hvert afbrigði vörunnar í fyrirtækinu. Þetta þýðir að meðalinnkaupsverð þessarar vöru veltur á því hvar hún er geymd og hvaða afbrigði vörunnar (til dæmis litur) var valið.|  

> [!NOTE]  
>  Aðeins er hægt að nota meðalkostnaðartímabil og eina gerð útreikninga meðaltalskostnaðará hverju fjárhagsári.  
>   
>  **Fjárhagstímabil** síðan sýnir hvaða meðalkostnaðartímabil og meðalkostnaðarútreikningsgerð er í gildi á því tímabili, fyrir hvert fjárhagstímabil.  

## <a name="calculating-average-cost"></a>Meðalkostnaður reiknaður  
 Þegar viðskipti eru bókuð fyrir vöru sem notar kostnaðarútreikningsaðferðina Meðaltal stofnar forritið færslu í töflunni **Upphafspunktur Meðalkostnaðarleiðréttingar**. Þessi færsla inniheldur vörunúmer, afbrigðakóða og birgðageymslukóða færslunnar. Færslan inniheldur einnig reitinn **Dagsetning virðismats**, sem tilgreinir síðustu dagsetningu meðalkostnaðartímabilsins sem færslan var bókuð á.  

> [!NOTE]  
>  Ekki ætti að rugla þessum reit saman við **Dagsetning virðismats** reitinn í **Virðisfærsla** töflunni, sem sýnir dagsetninguna þegar gildið tekur gildi og er notaður til að ákvarða meðalkostnaðartímabilið sem gildisfærslan tilheyrir.  

 Meðalkostnaður færslu er reiknaður þegar vörukostnaður er leiðréttur. Nánari upplýsingar, sjá [Upplýsingar um hönnun: Kostnaðarleiðrétting](design-details-cost-adjustment.md) Kostnaðarleiðrétting notar færslur í **Upphafsstaður Meðalkostnaðarleiðrétting** töflunni til að auðkenna fyrir hvaða vöru eða vörur, staðsetningu, og afbrigði skal reikna meðalkostnað fyrir. Fyrir hverja færslu með kostnað sem hefur ekki verið jöfnuð notar kostnaðarleiðrétting eftirfarandi til að ákvarða meðalkostnað:  

-   Ákvarðar kostnað vöru Í upphafi meðalkostnaðartímabil.  
-   Bæta við summu kostnaðar á innleið sem voru bókaðir á meðalkostnaðartímabil. Það inniheldur innkaup, söluvöruskil, jákvæða leiðréttingu, og vöru og samsetningarúttak.  
-   Dregur frá summu kostnaðar útleiðarfærslna sem voru fastjafnaðar við móttöku í meðalkostnaðartímabili. Yfirleitt inniheldur þetta innkaupaskil og neikvætt frálag.  
-   Deilir með heildarfjölda birgða fyrir lok meðalkostnaðartímabils, að undanskildum birgðarminnkun sem eru metin.  

 Reiknaður meðalkostnaður er svo jafnaður við birgðaminnkun vörunnar ( eða vöru, birgðageymslu og afbrigði) með bókunardagsetningum í meðalkostnaðartímabilinu. Ef einhverjar birgðaaukningar eru fyrir hendi sem voru notaðar fast á birgðaminnkun á meðalkostnaðartímabilinu er útreiknaður meðalkostnaður framsendur úr aukningu í minnkun.  

### <a name="example-average-cost-period--day"></a>Dæmi Tímabil meðalinnk.verðs = Dagur  
 Þetta dæmi sýnir hvaða áhrif það hefur að reikna meðalkostnað samkvæmt meðalkostnaðartímabili eins dags. Reiturinn **Útreikningsgerð meðalkostnaðar** á síðunni **Uppsetning birgða** er stilltur á **Vara**.  

 Eftirfarandi tafla sýnir hlut birgðahöfuðbókarfærslur fyrir sýnishorn meðalkostnaðarvöru, VARA1, áður en runuvinnslan **Leiðrétta kostnað - Birgðafærslur** hefur verið keyrð.  

|**Bókunardags.**|**Tegund birgðafærslu**|**Magn**|**Kostnaðarupphæð (raunverul.)**|**Færslunr.**|  
|---------------------------------------|---------------------------------------------------|------------------------------------|----------------------------------------------------|------------------------------------|  
|01-01-20|Innkaup|1|20.00|1|  
|01-01-20|Innkaup|1|40.00|2|  
|01-01-20|Sala|-1|-20,00|3|  
|02-01-20|Sala|-1|-40,00|4|  
|02-02-20|Innkaup|1|100,00|5|  
|02-03-20|Sala|-1|-100,00|6|  

> [!NOTE]  
>  Vegna þess að kostnaðarleiðrétting hefur ekki átt sér stað ennþá, mun reiturinn í **Kostnaðarupphæð Raunveruleg** birgðaminnkun samsvara birgðaaukningu sem hann er jafnaður við.  

 Eftirfarandi tafla sýnir færslur í töflunni **Upphafspunktur Meðalkostnaðarleiðrétting** sem gilda um virðisfærslur vegna birgðahöfuðbókarfærsla í undanfarandi töflu.  

|**Vörunr.**|**Afbrigðiskóði**|**Staðsetningarkóði**|**Dagsetning virðismats**|**Kostnaður er leiðréttur**|  
|-------------------------------------|-----------------------------------------|------------------------------------------|-------------------------------------------|---------------------------------------------|  
|VARA1||BLÁTT|01-01-20|Nei|  
|VARA1||BLÁTT|02-01-20|Nei|  
|VARA1||BLÁTT|02-02-20|Nei|  
|VARA1||BLÁTT|02-03-20|Nei|  

 Eftirfarandi tafla sýnir sömu birgðahöfuðbókarfærslur eftir að runuvinnslan **Leiðrétta kostnað Birgðafærslur** hefur verið keyrð. Meðalkostnaður á dag er reiknaður og jafnaður við birgðaminnkun.  

|**Bókunardags.**|**Tegund birgðafærslu**|**Magn**|**Kostnaðarupphæð (raunverul.)**|**Færslunr.**|  
|---------------------------------------|---------------------------------------------------|------------------------------------|----------------------------------------------------|------------------------------------|  
|01-01-20|Innkaup|1|20.00|1|  
|01-01-20|Innkaup|1|40.00|2|  
|01-01-20|Sala|-1|-30,00|3|  
|02-01-20|Sala|-1|-30,00|4|  
|02-02-20|Innkaup|1|100,00|5|  
|02-03-20|Sala|-1|-100,00|6|  

### <a name="example-average-cost-period--month"></a>Dæmi Tímabil meðalinnk.verðs = mánuður  
 Þetta dæmi sýnir hvaða áhrif það hefur að reikna meðalkostnað samkvæmt meðalkostnaðartímabili eins mánaðar. Reiturinn **Útreikningsgerð meðalkostnaðar** á síðunni **Uppsetning birgða** er stilltur á **Vara**.  

 Ef meðalkostnaðartímabilið er einn mánuður er aðeins ein færsla búin til fyrir hverja samsetningu vörunúmers, afbrigðiskóða, staðsetningarkóða og endurmatsdagsetningar.  

 Eftirfarandi tafla sýnir hlut birgðahöfuðbókarfærslur fyrir sýnishorn meðalkostnaðarvöru, VARA1, áður en runuvinnslan **Leiðrétta kostnað - Birgðafærslur** hefur verið keyrð.  

|**Bókunardags.**|**Tegund birgðafærslu**|**Magn**|**Kostnaðarupphæð (raunverul.)**|**Færslunr.**|  
|---------------------------------------|---------------------------------------------------|------------------------------------|----------------------------------------------------|------------------------------------|  
|01-01-20|Innkaup|1|20.00|1|  
|01-01-20|Innkaup|1|40.00|2|  
|01-01-20|Sala|-1|-20,00|3|  
|02-01-20|Sala|-1|-40,00|4|  
|02-02-20|Innkaup|1|100,00|5|  
|02-03-20|Sala|-1|-100,00|6|  

> [!NOTE]  
>  Vegna þess að kostnaðarleiðrétting hefur ekki átt sér stað ennþá, mun reiturinn í **Kostnaðarupphæð Raunveruleg** birgðaminnkun samsvara birgðaaukningu sem hann er jafnaður við.  

 Eftirfarandi tafla sýnir færslur í töflunni **Upphafspunktur Meðalkostnaðarleiðrétting** sem gilda um virðisfærslur vegna birgðahöfuðbókarfærsla í undanfarandi töflu.  

|**Vörunr.**|**Afbrigðiskóði**|**Staðsetningarkóði**|**Dagsetning virðismats**|**Kostnaður er leiðréttur**|  
|-------------------------------------|-----------------------------------------|------------------------------------------|-------------------------------------------|---------------------------------------------|  
|VARA1||BLÁTT|01-31-20|Nei|  
|VARA1||BLÁTT|02-28-20|Nei|  

> [!NOTE]  
>  Virðisdagsetningin er stillt á síðasta dag meðalkostnaðartímabils, sem í þessu tilviki er síðasti dagur mánaðarins.  

 Eftirfarandi tafla sýnir sömu birgðahöfuðbókarfærslur eftir að runuvinnslan **Leiðrétta kostnað Birgðafærslur** hefur verið keyrð. Meðalkostnaður á mánuði er reiknaður og jafnaður við birgðaminnkun.  

|**Bókunardags.**|**Tegund birgðafærslu**|**Magn**|**Kostnaðarupphæð (raunverul.)**|**Færslunr.**|  
|---------------------------------------|---------------------------------------------------|------------------------------------|----------------------------------------------------|------------------------------------|  
|01-01-20|Innkaup|1|20.00|1|  
|01-01-20|Innkaup|1|40.00|2|  
|01-01-20|Sala|-1|-30,00|3|  
|02-01-20|Sala|-1|-65,00|4|  
|02-02-20|Innkaup|1|100,00|5|  
|02-03-20|Sala|-1|-65,00|6|  

 Meðalkostnaður færslunúmers 3 er reiknað út á meðalkostnaðartímabili fyrir janúar og meðalkostnaður fyrir færslur 4 og 6 er reiknaður út á meðalkostnaðartímabili fyrir febrúar.  

 Til að fá meðalkostnað febrúar, meðalkostnaður hlutarins fékk í birgðum (100.00), er bætt við á meðalkostnaði í upphafi tímabils (30,00). Svo er deilt í summu þessara tveggja (130,00) með heildarmagni í birgðum (2). Við það fæst meðalkostnaður vörunnar í febrúar (65,00). Meðalkostnaðinum er úthlutað á birgðaminnkunina í tímabilinu (færslur 4 og 6).  

## <a name="setting-the-valuation-date"></a>Dagsetning virðismats ákveðin  
 Reiturinn **Dagsetning virðismats** í töflunni **Virðisfærsla** er notaður til að ákvarða í hvaða meðalkostnaðartímabili minnkunarfærsla í birgðum á heima. Þetta gildir einnig um birgðir verka í vinnslu (VÍV).  

 Eftirfarandi tafla sýnir skilyrði sem eru notuð til að stilla matsdagsetninguna.  

|Aðstæður|Bókunardagsetning|Virt magn|Endurmat|Dagsetning virðismats|  
|--------------|-------------------------------------|-----------------------------------------|-----------------|-----------------------------------------|  
|1||Jákvæð|Nei|Bókunardagsetning birgðafærslu|  
|2|Síðar en síðasta matsdagsetning jafnaðra virðisfærslna|Neikvætt|Nei|Bókunardagsetning birgðafærslu|  
|3|Fyrr en síðasta matsdagsetning jafnaðra virðisfærslna|Jákvætt|Nei|Síðasta matsdagsetning jafnaðra virðisfærslna|  
|4||Neikvætt|Já|Bókunardagsetning virðisfærslu endurmats|  

### <a name="example"></a>Dæmi  
 Eftirfarandi tafla með virðisfærslur sýnir mismunandi aðstæður.  

|Aðstæður|Bókunardagsetning|Tegund birgðafærslu|Dagsetning virðismats|Virt magn|Kostnaðarupphæð (raunverul.)|Birgðafærslunr.|Færslunr.|  
|--------------|-------------------------------------|-----------------------------------------------|-----------------------------------------|-----------------------------------------|------------------------------------------------|-----------------------------------------------|----------------------------------|  
|1|01-01-20|Innkaup|01-01-20|2|20.00|1|1|  
|2|01-15-20|(Kostnaðarauki)|01-01-20|2|8,00|1|2|  
|3|02-01-20|Sala|02-01-20|-1|-14,00|2|3|  
|4|03-01-20|(Endurmat)|03-01-20|1|-.4.00|1|4|  
|5|02-01-20|Sala|03-01-20|-1|-10,00|3|5|  

> [!NOTE]  
>  Í færslu númer 5 í töflunni á undann, notandinn hefur sett inn sölupöntun með bókunardagsetningu (02-01-20) sem kemur á undan nýjustu verðmatsdagsetningu jafnaðra virðisfærslna (03-01-20). Ef samsvarandi gildi í reitnum **Kostnaðarupphæð Raunveruleg** fyrir þessa dagsetningu (02-01-20) væri notað fyrir þessa færslu væri það 14.00. Þetta myndi gefa aðstæður þar sem magn á lager er núll, en birgðavirði er -4,00.  
>   
>  Til að forðast slíkt misræmi á magni og virði er verðmatsdagsetningin sett til að jafna nýjasta verðmats dagsetningu jafnaðra virðisfærslna (03-01-20). Gildið í **Kostnaðarupphæð Raunveruleg** reitnum verður 10.00 eftir endurmat, sem merkir að magn birgða er núll og gildi birgða er einnig núll.  

> [!CAUTION]  
>  Þar sem skýrsla um **Birgðavirði** byggir á bókunardagsetningu, mun skýrslan endurspegla allt misræmi í magni-verðmæti eins og í dæminu hér að ofan. Nánari upplýsingar, sjá [Upplýsingar um hönnun: Birgðavirði](design-details-inventory-valuation.md)  

 Ef magn í birgðum er minna en núll eftir bókun á birgðaminnkun er matsdagsetningin fyrst stillt á bókunardagsetningu birgðaminnkunarinnar. Hægt er að breyta þessari dagsetningu síðar, samkvæmt reglunum sem lýst er í athugasemdinni áður í þessum hluta, þegar birgðaaukningin er notuð.  

## <a name="recalculating-average-cost"></a>Meðalkostnaður reiknaður  
 Að meta birgðaminnkun sem vegið meðaltal væri einfalt ef kaup væru alltaf reikningsfærð áður en sala er reikningsfærði, bókanir væru aldrei bakfærðar og aldrei væru gerð nein mistök. Hins vegar er veruleikinn er nokkuð frábrugðinn þessari hugmynd.  

 Eins og sýnt er í dæmunum í þessu umfjöllunarefni er matsdagsetningin skilgreind sem dagsetningin sem virðisfærsla er tekin með í meðalkostnaðarútreikinginn. Þetta gefur sveigjanleikann til að gera eftirfarandi fyrir vörur með Meðaltal kostnaðarútreiknings.  

-   Reikningsfæra sölu á vöru áður en kaup á vörunni hefur verið reikningsfærð.  
-   Bakfæra bókun.  
-   Endurheimta ranga bókun.  

> [!NOTE]  
>  Önnur ástæða fyrir þessum sveigjanleika er föst jöfnun. Frekari upplýsingar um fastar jafnanir eru í [Hönnunarupplýsingar: Birgðajöfnun](design-details-item-application.md).  

 Vegna þessa sveigjanleika, getur þú þurft að endurreikna meðalkostnað eftir tengda bókun. Til dæmis ef notandi bókar birgðaaukningu eða birgðaminnkun með virðisdagsetningu sem er fyrir eina eða fleiri birgðaminnkun. Endurreikningur meðalkostnaðar gerist sjálfkrafa þegar þú keyrir **Kostnaðarleiðrétting Birgðafærslur** runuvinnsluna, handvirkt eða sjálfvirkt.  

 Hægt er að breyta birgðamatsgrunni innan reikningstímabils með því að breyta reitnum **Meðalkostnaðartímabil** og reitnum **Meðalinnk.verð - Teg. útreikn.**. Hins vegar ætti þetta að vera gert með varúð og í samráði við endurskoðanda.  

### <a name="example"></a>Dæmi  
 Eftirfarandi dæmi sýnir hvernig meðalkostnaður er endurreiknuð þegar seint bókun er kynnt á dagsetningu sem kemur áður en ein eða fleiri birgðir minnka. Dæmi um meðalkostnaðartímabil í **Dagur**.  

 Eftirfarandi tafla sýnir virðisfærslur fyrir vöruna áður en bókað er.  

|Dagsetning virðismats|Magn|Kostnaðarupphæð (raunverul.)|Færslunr.|  
|-----------------------------------------|--------------------------------|------------------------------------------------|----------------------------------|  
|01-01-20|1|10.00|1|  
|01-02-20|1|20.00|2|  
|02-15-20|-1|-15,00|3|  
|02-16-20|-1|-15,00|4|  

 Notandinn bókar birgðaaukningu (færsla númer 5) með virðisdagsetningu (01-03-20) sem er fyrir eina eða fleiri birgðaaukningu. Til að jafna birgðir, verður meðaltals kostnaður skal endurreiknaður og leiðrétt til 17,00.  

 Eftirfarandi tafla sýnir virðisfærslur fyrir vöruna eftir að færslunúmer 5 kemur til.  

|Dagsetning virðismats|Magn|Kostnaðarupphæð (raunverul.)|Færslunr.|  
|-----------------------------------------|--------------------------------|------------------------------------------------|----------------------------------|  
|01-01-20|1|10.00|1|  
|01-02-20|1|20.00|2|  
|01-03-20|1|21.00|5|  
|02-15-20|-1|-17,00|3|  
|02-16-20|-1|-17,00|4|  

## <a name="see-also"></a>Sjá einnig  
 [Hönnunarupplýsingar: Birgðakostnaður](design-details-inventory-costing.md)   
 [Hönnunarupplýsingar: Aðferð kostn.útreiknings](design-details-costing-methods.md)   
 [Hönnunarupplýsingar: Kostnaðarleiðrétting](design-details-cost-adjustment.md)   
 [Hönnunarupplýsingar: Birgðajöfnun](design-details-item-application.md)  
 [Birgðakostnaði stjórnað](finance-manage-inventory-costs.md)  
 [Fjármál](finance.md)  
 [Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]