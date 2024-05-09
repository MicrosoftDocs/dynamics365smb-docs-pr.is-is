---
title: Upplýsingar um hönnun - meðalinnkaupaverð
description: Meðalinnkaupaverð vöru er reiknað út með reglubundnu vegnu meðaltali.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: null
ms.search.form: '8645,'
ms.date: 04/26/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# Upplýsingar um hönnun: meðalinnkaupaverð

Meðalinnkaupaverð vöru er reiknað út með reglubundnu vegnu meðaltali. Meðaltalið byggist á meðalinnkaupaverðstímabilinu sem tilgreint var í [!INCLUDE[prod_short](includes/prod_short.md)].  

Virðisdagsetningin er valin sjálfkrafa.  

## Uppsetning útreiknings á meðalinnkaupaverði

Eftirfarandi tafla lýsir tveimur reitum á síðunni **Uppsetning birgða** sem verður að fylla út til að gera meðalkostnaðarútreikning virkan.  

|Svæði|Lýsing|  
|---------------------------------|---------------------------------------|  
|**Tímabil meðalinnk.verðs**|Tilgreinir á hvaða tímabili meðalkostnaður er reiknaður í. Eftirfarandi möguleikar eru til staðar:<br /><br /> - **Dag**<br />- **Viku**<br />- **Mánuði**<br />- **Reikningstímabil**<br /><br /> Birgðaminnkanir sem eru bókaðar í meðalinnkaupaverðstímabilið fá meðalinnkaupaverðið reiknað út fyrir það tímabil.|  
|**Meðalinnk.verð Teg. útreikn.**|Tilgreinir hvernig meðalkostnaður er reiknaður. Eftirfarandi möguleikar eru til staðar:<br /><br /> - **Vöru**<br />- **Vara, Afbrigði og Birgðageymsla**<br /> Ef þessi kostur er valinn reiknar kerfið út meðalinnkaupsverð á vöru fyrir hverja birgðageymslu og fyrir hvert afbrigði vörunnar í fyrirtækinu. Meðalinnkaupaverð þessarar vöru veltur á því hvar hún er geymd og afbrigðið sem valið er, t.d. lit.|  

> [!NOTE]  
> Aðeins er hægt að nota meðalkostnaðartímabil og eina gerð útreikninga meðaltalskostnaðará hverju fjárhagsári.  
>
> **Fjárhagstímabil** síðan sýnir hvaða meðalkostnaðartímabil og meðalkostnaðarútreikningsgerð er í gildi á því tímabili, fyrir hvert fjárhagstímabil.  

## Útreikningur meðalinnkaupaverðs

 Þegar viðskipti eru bókuð fyrir vöru sem notar kostnaðarútreikningsaðferðina Meðaltal stofnar forritið færslu í töflunni **Upphafspunktur Meðalkostnaðarleiðréttingar**. Þessi færsla inniheldur vörunúmer, afbrigðakóða og birgðageymslukóða færslunnar. Færslan inniheldur einnig reitinn **Dagsetning virðismats**, sem tilgreinir síðustu dagsetningu meðalkostnaðartímabilsins sem færslan var bókuð á.  

> [!NOTE]  
> Ekki ætti að rugla þessum reit saman við **Dagsetning virðismats** reitinn í **Virðisfærsla** töflunni, sem sýnir dagsetninguna þegar gildið tekur gildi og er notaður til að ákvarða meðalkostnaðartímabilið sem gildisfærslan tilheyrir.  

 Meðalkostnaður færslu er reiknaður þegar vörukostnaður er leiðréttur. Nánari upplýsingar, sjá [Upplýsingar um hönnun: Kostnaðarleiðrétting](design-details-cost-adjustment.md) Kostnaðarleiðrétting notar færslur í **Upphafsstaður Meðalkostnaðarleiðrétting** töflunni til að auðkenna fyrir hvaða vöru eða vörur, staðsetningu, og afbrigði skal reikna meðalkostnað fyrir. Fyrir hverja færslu með kostnaði sem ekki hefur verið leiðréttur notar kostnaðarleiðréttingin eftirfarandi til að ákvarða meðalinnkaupaverðið:  

- Ákvarðar kostnað vöru Í upphafi meðalkostnaðartímabil.  
- Bæta við summu kostnaðar á innleið sem voru bókaðir á meðalkostnaðartímabil. Það inniheldur innkaup, söluvöruskil, jákvæða leiðréttingu, og vöru og samsetningarúttak.  
- Dregur frá summu kostnaðar útleiðarfærslna sem voru fastjafnaðar við móttöku í meðalkostnaðartímabili. Yfirleitt inniheldur þetta innkaupaskil og neikvætt frálag.  
- Deilir með heildarbirgðamagni fyrir lok meðalinnkaupaverðstímabilsins. Útilokar birgðaminnkun sem verið er að meta.  

 Reiknaður meðalkostnaður er svo jafnaður við birgðaminnkun vörunnar ( eða vöru, birgðageymslu og afbrigði) með bókunardagsetningum í meðalkostnaðartímabilinu. Fyrir birgðaaukningar sem eru fast jafnaðar við birgðaminnkanir á meðalinnkaupaverðstímabilinu áframsendir [!INCLUDE [prod_short](includes/prod_short.md)]  reiknað meðalinnkaupaverð frá aukningunni til minnkunarinnar.  

### Dæmi: meðalinnkaupaverðstímabil = dagur

Eftirfarandi dæmi sýnir áhrif þess að reikna út meðalinnkaupsverð á grundvelli meðalinnkaupaverðstímabils sem er einn dagur. Reiturinn **Útreikningsgerð meðalkostnaðar** á síðunni **Uppsetning birgða** er stilltur á **Vara**.  

Eftirfarandi tafla sýnir birgðafærslur fyrir sýnishorn af meðalkostnaðarvöru, VÖRU1, áður en **keyrslan** Leiðr. kostnað - Birgðafærslur er keyrð.  

| **Bókunardags.** | **Tegund birgðafærslu** | **Magn** | **Kostnaðarupphæð (raunverul.)** | **Færslunr.** |
|--|--|--|--|--|
| 01-01-23 |   Innkaup | 1 | 20.00 | 1 |
| 01-01-23 |   Innkaup | 1 | 40.00 | 2 |
| 01-01-23 |   Útsala | -1 | -20,00 | 3 |
| 02-01-23 |   Útsala | -1 | -40,00 | 4 |
| 02-02-23 |   Innkaup | 1 | 100.00 | 5 |
| 02-03-23 |   Útsala | -1 | -100,00 | 6 |

> [!NOTE]  
> Vegna þess að kostnaðarleiðrétting hefur ekki átt sér stað ennþá, mun reiturinn í **Kostnaðarupphæð Raunveruleg** birgðaminnkun samsvara birgðaaukningu sem hann er jafnaður við.  

 Eftirfarandi tafla sýnir færslurnar í reitnum **Meðalinnk.verðleiðr. Taflan Komustaður** sem á við virðisfærslurnar sem eru afleiðingar birgðafærslna í síðustu töflu.  

| **Vörunr.** | **Afbrigðiskóði** | **Staðsetningarkóði** | **Dagsetning virðismats** | **Kostnaður er leiðréttur** |
|--|--|--|--|--|
| VARA1 |  | BLÁTT | 01-01-23 |   Nr. |
| VARA1 |  | BLÁTT | 02-01-23 |   Nr. |
| VARA1 |  | BLÁTT | 02-02-23 |   Nr. |
| VARA1 |  | BLÁTT | 02-03-23 |   Nr. |

 Eftirfarandi tafla sýnir sömu birgðafærslur eftir að keyrslan **Leiðr. kostnað - Birgðafærslur hefur verið keyrð** . Meðalkostnaður á dag er reiknaður og jafnaður við birgðaminnkun.  

| **Bókunardags.** | **Tegund birgðafærslu** | **Magn** | **Kostnaðarupphæð (raunverul.)** | **Færslunr.** |
|--|--|--|--|--|--|
| 01-01-23 |   Innkaup | 1 | 20.00 | 1 |
| 01-01-23 |   Innkaup | 1 | 40.00 | 2 |
| 01-01-23 |   Útsala | -1 | -30,00 | 3 |
| 02-01-23 |   Útsala | -1 | -30,00 | 4 |
| 02-02-23 |   Innkaup | 1 | 100.00 | 5 |
| 02-03-23 |   Útsala | -1 | -100,00 | 6 |

### Dæmi: meðalinnkaupaverðstímabil = mánuður

 Þetta dæmi sýnir áhrif þess að reikna út meðalinnkaupsverð á grundvelli meðalinnkaupsverðstímabils sem er einn mánuður. Reiturinn **Útreikningsgerð meðalkostnaðar** á síðunni **Uppsetning birgða** er stilltur á **Vara**.  

 Ef meðalinnkaupaverðstímabilið er einn mánuður [!INCLUDE [prod_short](includes/prod_short.md)]  stofnar ein færsla fyrir hverja samsetningu vörunúmers, afbrigðiskóta, birgðageymslukóta og matsdagsetningar.  

 Eftirfarandi tafla sýnir birgðafærslur fyrir sýnishorn af meðalkostnaðarvöru, VÖRU1, áður en **keyrslan** Leiðr. kostnað - Birgðafærslur er keyrð.  

| **Bókunardags.** | **Tegund birgðafærslu** | **Magn** | **Kostnaðarupphæð (raunverul.)** | **Færslunr.** |
|--|--|--|--|--|
| 01-01-23 |   Innkaup | 1 | 20.00 | 1 |
| 01-01-23 |   Innkaup | 1 | 40.00 | 2 |
| 01-01-23 |   Útsala | -1 | -20,00 | 3 |
| 02-01-23 |   Útsala | -1 | -40,00 | 4 |
| 02-02-23 |   Innkaup | 1 | 100.00 | 5 |
| 02-03-23 |   Útsala | -1 | -100,00 | 6 |

> [!NOTE]  
> Vegna þess að kostnaðarleiðrétting hefur ekki átt sér stað ennþá, mun reiturinn í **Kostnaðarupphæð Raunveruleg** birgðaminnkun samsvara birgðaaukningu sem hann er jafnaður við.  

Eftirfarandi tafla sýnir færslurnar í reitnum **Meðalinnk.verðleiðr. Taflan Komustaður** sem á við virðisfærslurnar sem eru afleiðingar birgðafærslna í síðustu töflu.  

| **Vörunr.** | **Afbrigðiskóði** | **Staðsetningarkóði** | **Dagsetning virðismats** | **Kostnaður er leiðréttur** |
|--|--|--|--|--|
| VARA1 |  | BLÁTT | 01-31-23 |   Nr. |
| VARA1 |  | BLÁTT | 02-28-23 |   Nr. |

> [!NOTE]  
> Virðisdagsetningin er stillt á síðasta dag meðalkostnaðartímabils, sem í þessu tilviki er síðasti dagur mánaðarins.  

Eftirfarandi tafla sýnir sömu birgðafærslur eftir að keyrslan **Leiðr. kostnað - Birgðafærslur hefur verið keyrð** . Meðalkostnaður á mánuði er reiknaður og jafnaður við birgðaminnkun.  

|**Bókunardags.** | **Tegund birgðafærslu** | **Magn** | **Kostnaðarupphæð (raunverul.)** | **Færslunr.** |
|--|--|--|--|--|
| 01-01-23 | Innkaup | 1 | 20.00 | 1 |
| 01-01-23 | Innkaup | 1 | 40.00 | 2 |
| 01-01-23 | Útsala | -1 | -30,00 | 3 |
| 02-01-23 | Útsala | -1 | -65,00 | 4 |
| 02-02-23 | Innkaup | 1 | 100.00 | 5 |
| 02-03-23 | Útsala | -1 | -65,00 | 6 |

Meðalinnkaupaverð færslunúmers 3 er reiknað í meðalinnkaupaverðstímabilinu í janúar. Meðalinnkaupaverð færslna 4 og 6 er reiknað í meðalinnkaupaverðstímabilinu í febrúar.  

Til að fá meðalinnkaupsverð fyrir febrúar [!INCLUDE [prod_short](includes/prod_short.md)]  er meðalinnkaupaverð þeirrar vöru sem var móttekin í birgðum (100,00) bætt við meðalinnkaupsverð í upphafi tímabilsins (30,00). Samtalan (130,00) er síðan deilt með heildarmagni í birgðum (2). Þessi útreikningur gefur út meðalinnkaupsverð vörunnar í febrúartímabilinu (65,00). Meðalkostnaðinum er úthlutað á birgðaminnkunina í tímabilinu (færslur 4 og 6).  

## Dagsetning mats stillt

 Reiturinn **Matsdagsetning** í **töflunni Virðisfærsla** ákvarðar það meðalinnkaupaverðstímabil sem birgðaminnkunarfærsla tilheyrir. Þessi stilling á einnig við um birgðir í vinnslu (VÍV).  

 Eftirfarandi tafla sýnir skilyrði sem eru notuð til að stilla matsdagsetninguna.  

| Aðstæður | Bókunardagsetning | Virt magn | Endurmat | Dagsetning virðismats |
|--|--|--|--|--|
| 1 |  | Jákvæð | Nei | Bókunardagsetning birgðafærslu |
| 2 | Síðar en síðasta matsdagsetning jafnaðra virðisfærslna | Neikvætt | Nei | Bókunardagsetning birgðafærslu |
| 3 | Fyrr en síðasta matsdagsetning jafnaðra virðisfærslna | Jákvætt | Nei | Síðasta matsdagsetning jafnaðra virðisfærslna |
| 4 |  | Neikvætt | Já | Bókunardagsetning virðisfærslu endurmats |

### Dæmi

Eftirfarandi tafla með virðisfærslur sýnir mismunandi aðstæður.  

| Aðstæður | Bókunardagsetning | Tegund birgðafærslu | Dagsetning virðismats | Virt magn | Kostnaðarupphæð (raunverul.) | Birgðafærslunr. | Færslunr. |
|--|--|--|--|--|--|--|--|
| 1 | 01-01-20 | Innkaup | 01-01-20 | 2 | 20.00 | 1 | 1 |
| 2 | 01-15-20 | (Kostnaðarauki) | 01-01-20 | 2 | 8,00 | 1 | 2 |
| 3 | 02-01-20 | Sala | 02-01-20 | -1 | -14,00 | 2 | 3 |
| 4 | 03-01-20 | (Endurmat) | 03-01-20 | 1 | -.4.00 | 1 | 4 |
| 5 | 02-01-20 | Sala | 03-01-20 | -1 | -10,00 | 3 | 5 |

> [!NOTE]  
> Í færslu númer 5 í töflunni á undann, notandinn hefur sett inn sölupöntun með bókunardagsetningu (02-01-20) sem kemur á undan nýjustu verðmatsdagsetningu jafnaðra virðisfærslna (03-01-20). Ef samsvarandi gildi í reitnum **Kostnaðarupphæð Raunveruleg** fyrir þessa dagsetningu (02-01-20) væri notað fyrir þessa færslu væri það 14.00. Þetta myndi gefa aðstæður þar sem magn á lager er núll, en birgðavirði er -4,00.  
>
> Til að forðast slíkt misræmi á magni og virði er verðmatsdagsetningin sett til að jafna nýjasta verðmats dagsetningu jafnaðra virðisfærslna (03-01-20). Gildið í **Kostnaðarupphæð Raunveruleg** reitnum verður 10.00 eftir endurmat, sem merkir að magn birgða er núll og gildi birgða er einnig núll.  

> [!CAUTION]  
> Þar sem skýrsla um **Birgðavirði** byggir á bókunardagsetningu, mun skýrslan endurspegla allt misræmi í magni-verðmæti eins og í dæminu hér að ofan. Nánari upplýsingar, sjá [Upplýsingar um hönnun: Birgðavirði](design-details-inventory-valuation.md)  

Ef birgðamagnið er lægra en núll eftir bókun birgðaminnkunarinnar er matsdagsetningin stillt á bókunardagsetningu birgðaminnkunarinnar. Hægt er að breyta þessari dagsetningu þegar birgðaaukningu er beitt samkvæmt reglunum sem lýst er í athugasemdinni fyrr í þessum hluta.  

## Endurreikna meðalinnkaupaverð

Mat á birgðaminnkun sem vegið meðaltal væri einfalt í nokkrum tilvikum:

- Innkaup eru alltaf reikningsfærð fyrir sölu.
- Bókanir eru aldrei bakfærðar.
- Þú gerðir aldrei mistök.

Raunveruleikinn er hins vegar öðruvísi.  

Sem dæmi í þessari grein er matsdagsetningin skilgreind sem dagsetningin sem virðisfærslan er tekin með í útreikningi á meðalinnkaupsverði. Með þessari stillingu er hægt að gera marga hluti fyrir vörur með meðalkostnaðarútreikningsaðferðina:  

- Reikningsfæra sölu vöru áður en hún er reikningsfærð.  
- Bakfæra bókun.  
- Endurheimta ranga bókun.  

> [!NOTE]  
> Önnur ástæða fyrir þessum sveigjanleika er föst jöfnun. Frekari upplýsingar um fastar jafnanir eru í [Hönnunarupplýsingar: Birgðajöfnun](design-details-item-application.md).  

Vegna þessa sveigjanleika þarf hugsanlega að endurreikna meðalinnkaupsverð eftir bókun. Ef t.d. birgðaaukning eða minnkun er bókuð með matsdagsetningu sem er á undan birgðaminnkun. Endurreiknun á meðalinnkaupaverði á sér sjálfkrafa stað þegar keyrslan Leiðr. kostnað - Birgðafærslur **er keyrð** sjálfvirkt eða handvirkt.  

Hægt er að breyta birgðamatsgrunni innan reikningstímabils með því að breyta gildunum í reitunum **Meðalinnkaupaverðstímabil** og **Útreikn.teg** . meðalinnkaupsverðs. Hins vegar er mælt með því að gát sé notuð og ráðfært sig við endurskoðandann.  

### Dæmi um endurreiknaðan meðalinnkaupaverð

Þetta dæmi sýnir hvernig [!INCLUDE [prod_short](includes/prod_short.md)] meðalinnkaupsverðið er endurreiknað þegar bókað er á degi sem er á undan birgðaminnkun. Dæmi um meðalkostnaðartímabil í **Dagur**.  

Eftirfarandi tafla sýnir virðisfærslur fyrir vöruna áður en bókað er.  

| Dagsetning virðismats | Magn | Kostnaðarupphæð (raunverul.) | Færslunr. |
|--|--|--|--|
| 01-01-20 | 1 | 10.00 | 1 |
| 01-02-20 | 1 | 20.00 | 2 |
| 02-15-20 | -1 | -15,00 | 3 |
| 02-16-20 | -1 | -15,00 | 4 |

Notandinn bókar birgðaaukningu (færslunúmer 5) með matsdagsetningu (01-03-20) sem er á undan birgðaminnkun. Til að jafna birgðir, verður meðaltals kostnaður skal endurreiknaður og leiðrétt til 17,00.  

Eftirfarandi tafla sýnir virðisfærslur fyrir vöruna eftir að færslunúmer 5 kemur til.  

| Dagsetning virðismats | Magn | Kostnaðarupphæð (raunverul.) | Færslunr. |
|--|--|--|--|
| 01-01-20 | 1 | 10.00 | 1 |
| 01-02-20 | 1 | 20.00 | 2 |
| 01-03-20 | 1 | 21.00 | 5 |
| 02-15-20 | -1 | -17,00 | 3 |
| 02-16-20 | -1 | -17,00 | 4 |

## Sjá einnig

[Hönnunarupplýsingar: Birgðakostnaður](design-details-inventory-costing.md)  
[Hönnunarupplýsingar: Aðferð kostnaðarútreiknings](design-details-costing-methods.md)  
[Hönnunarupplýsingar: kostnaðarleiðrétting](design-details-cost-adjustment.md)  
[Hönnunarupplýsingar: Umsókn vöru](design-details-item-application.md)  
[Birgðakostnaði stjórnað](finance-manage-inventory-costs.md)  
[Fjármál](finance.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Orðalisti í viðskiptaferlum Dynamics 365](/dynamics365/guidance/business-processes/glossary)  
[Viðskiptaferli fyrir kostnaðarúttekt afurða og hvernig það tengist öðrum ferlum með Dynamics 365](/dynamics365/guidance/business-processes/design-to-retire-define-product-costing-overview)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
