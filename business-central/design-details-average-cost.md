---
title: Hönnunarupplýsingar - Meðalkostnaður
description: Meðalkostnaður á vöru er reiknaður með reglubundnu vegnu meðaltali.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.search.form: '8645,'
ms.date: 06/06/2023
ms.author: bholtorf
---
# <a name="design-details-average-cost"></a>Hönnunarupplýsingar: Meðalkostnaður

Meðalkostnaður á vöru er reiknaður með reglubundnu vegnu meðaltali. Meðaltalið er miðað við meðalkostnaðartímabilið sem sett er upp í [!INCLUDE[prod_short](includes/prod_short.md)].  

Virðisdagsetningin er valin sjálfkrafa.  

## <a name="setting-up-average-cost-calculation"></a>Setja upp meðalkostnaðrverðútreikning

Eftirfarandi tafla lýsir tveimur reitum á síðunni **Uppsetning birgða** sem verður að fylla út til að gera meðalkostnaðarútreikning virkan.  

|Svæði|Lýsing|  
|---------------------------------|---------------------------------------|  
|**Tímabil meðalinnk.verðs**|Tilgreinir á hvaða tímabili meðalkostnaður er reiknaður í. Eftirfarandi möguleikar eru til staðar:<br /><br /> - **Dag**<br />- **Viku**<br />- **Mánuði**<br />- **Bókhaldstímabil**<br /><br /> Minnkun birgða sem bókaðar eru á meðalkostnaðartímabilinu fá meðalinnkaupsverð reiknað fyrir það tímabil.|  
|**Meðalinnk.verð Teg. útreikn.**|Tilgreinir hvernig meðalkostnaður er reiknaður. Eftirfarandi möguleikar eru til staðar:<br /><br /> - **Vöru**<br />- **Vara, afbrigði og staðsetning**<br /> Ef þessi kostur er valinn reiknar kerfið út meðalinnkaupsverð á vöru fyrir hverja birgðageymslu og fyrir hvert afbrigði vörunnar í fyrirtækinu. Meðalkostnaður þessarar vöru veltur á því hvar hann er geymdur og afbrigðinu sem er valið, t.d. lit.|  

> [!NOTE]  
> Aðeins er hægt að nota meðalkostnaðartímabil og eina gerð útreikninga meðaltalskostnaðará hverju fjárhagsári.  
>
> **Fjárhagstímabil** síðan sýnir hvaða meðalkostnaðartímabil og meðalkostnaðarútreikningsgerð er í gildi á því tímabili, fyrir hvert fjárhagstímabil.  

## <a name="calculating-average-cost"></a>Meðalkostnaður reiknaður

 Þegar viðskipti eru bókuð fyrir vöru sem notar kostnaðarútreikningsaðferðina Meðaltal stofnar forritið færslu í töflunni **Upphafspunktur Meðalkostnaðarleiðréttingar**. Þessi færsla inniheldur vörunúmer, afbrigðakóða og birgðageymslukóða færslunnar. Færslan inniheldur einnig reitinn **Dagsetning virðismats**, sem tilgreinir síðustu dagsetningu meðalkostnaðartímabilsins sem færslan var bókuð á.  

> [!NOTE]  
> Ekki ætti að rugla þessum reit saman við **Dagsetning virðismats** reitinn í **Virðisfærsla** töflunni, sem sýnir dagsetninguna þegar gildið tekur gildi og er notaður til að ákvarða meðalkostnaðartímabilið sem gildisfærslan tilheyrir.  

 Meðalkostnaður færslu er reiknaður þegar vörukostnaður er leiðréttur. Nánari upplýsingar, sjá [Upplýsingar um hönnun: Kostnaðarleiðrétting](design-details-cost-adjustment.md) Kostnaðarleiðrétting notar færslur í **Upphafsstaður Meðalkostnaðarleiðrétting** töflunni til að auðkenna fyrir hvaða vöru eða vörur, staðsetningu, og afbrigði skal reikna meðalkostnað fyrir. Fyrir hverja færslu með kostnað sem hefur ekki verið jöfnuð notar kostnaðarleiðrétting eftirfarandi til að ákvarða meðalkostnað:  

- Ákvarðar kostnað vöru Í upphafi meðalkostnaðartímabil.  
- Bæta við summu kostnaðar á innleið sem voru bókaðir á meðalkostnaðartímabil. Það inniheldur innkaup, söluvöruskil, jákvæða leiðréttingu, og vöru og samsetningarúttak.  
- Dregur frá summu kostnaðar útleiðarfærslna sem voru fastjafnaðar við móttöku í meðalkostnaðartímabili. Yfirleitt inniheldur þetta innkaupaskil og neikvætt frálag.  
- Arður af heildarbirgðamagni fyrir lok tímabils meðalkostnaðarins. Minnkar birgðatíð sem verið er að meta.  

 Reiknaður meðalkostnaður er svo jafnaður við birgðaminnkun vörunnar ( eða vöru, birgðageymslu og afbrigði) með bókunardagsetningum í meðalkostnaðartímabilinu. Fyrir birgðahækkanir sem eru fastar jafnaðar við minnkun birgða á meðalkostnaðartímabilinu,  [!INCLUDE [prod_short](includes/prod_short.md)]  Framsendir útreiknaðan meðalkostnað frá aukningu til lækkunar.  

### <a name="example-average-cost-period--day"></a>Dæmi Tímabil meðalinnk.verðs = Dagur

Eftirfarandi dæmi sýnir áhrif þess að reikna meðalkostnað miðað við meðalkostnaðartímabil einn dag. Reiturinn **Útreikningsgerð meðalkostnaðar** á síðunni **Uppsetning birgða** er stilltur á **Vara**.  

Eftirfarandi tafla sýnir hlut birgðahöfuðbókarfærslur fyrir sýnishorn meðalkostnaðarvöru, VARA1, áður en runuvinnslan **Leiðrétta kostnað - Birgðafærslur** hefur verið keyrð.  

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

 Eftirfarandi tafla sýnir færslurnar í  **reitnum AV. kostnaðarleiðr. Færslunapunkta**  sem gilda um virðisfærslur sem verða til við birgðafærslurnar í fyrri töflunni.  

| **Vörunr.** | **Afbrigðiskóði** | **Staðsetningarkóði** | **Dagsetning virðismats** | **Kostnaður er leiðréttur** |
|--|--|--|--|--|
| VARA1 |  | BLÁTT | 01-01-23 |   Nr. |
| VARA1 |  | BLÁTT | 02-01-23 |   Nr. |
| VARA1 |  | BLÁTT | 02-02-23 |   Nr. |
| VARA1 |  | BLÁTT | 02-03-23 |   Nr. |

 Eftirfarandi tafla sýnir sömu birgðahöfuðbókarfærslur eftir að runuvinnslan **Leiðrétta kostnað Birgðafærslur** hefur verið keyrð. Meðalkostnaður á dag er reiknaður og jafnaður við birgðaminnkun.  

| **Bókunardags.** | **Tegund birgðafærslu** | **Magn** | **Kostnaðarupphæð (raunverul.)** | **Færslunr.** |
|--|--|--|--|--|--|
| 01-01-23 |   Innkaup | 1 | 20.00 | 1 |
| 01-01-23 |   Innkaup | 1 | 40.00 | 2 |
| 01-01-23 |   Útsala | -1 | -30,00 | 3 |
| 02-01-23 |   Útsala | -1 | -30,00 | 4 |
| 02-02-23 |   Innkaup | 1 | 100.00 | 5 |
| 02-03-23 |   Útsala | -1 | -100,00 | 6 |

### <a name="example-average-cost-period--month"></a>Dæmi Tímabil meðalinnk.verðs = mánuður

 Þetta dæmi sýnir áhrif þess að reikna meðalkostnað miðað við tímabil meðalkostnaðar á einum mánuði. Reiturinn **Útreikningsgerð meðalkostnaðar** á síðunni **Uppsetning birgða** er stilltur á **Vara**.  

 Ef meðalkostnaðartímabilið er einn mánuður,  [!INCLUDE [prod_short](includes/prod_short.md)]  stofnast ein færsla fyrir hverja samsetningu vörunúmera, afbrigðiskóta, birgðageymslukóta og dagsetningu matsdagsetningar.  

 Eftirfarandi tafla sýnir hlut birgðahöfuðbókarfærslur fyrir sýnishorn meðalkostnaðarvöru, VARA1, áður en runuvinnslan **Leiðrétta kostnað - Birgðafærslur** hefur verið keyrð.  

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

Eftirfarandi tafla sýnir færslurnar í  **reitnum AV. kostnaðarleiðr.** Færslutöflu sem á við þær virðisfærslur sem verða vegna birgðafærslna í töflunni hér á undan.  

| **Vörunr.** | **Afbrigðiskóði** | **Staðsetningarkóði** | **Dagsetning virðismats** | **Kostnaður er leiðréttur** |
|--|--|--|--|--|
| VARA1 |  | BLÁTT | 01-31-23 |   Nr. |
| VARA1 |  | BLÁTT | 02-28-23 |   Nr. |

> [!NOTE]  
> Virðisdagsetningin er stillt á síðasta dag meðalkostnaðartímabils, sem í þessu tilviki er síðasti dagur mánaðarins.  

Eftirfarandi tafla sýnir sömu birgðahöfuðbókarfærslur eftir að runuvinnslan **Leiðrétta kostnað Birgðafærslur** hefur verið keyrð. Meðalkostnaður á mánuði er reiknaður og jafnaður við birgðaminnkun.  

|**Bókunardags.** | **Tegund birgðafærslu** | **Magn** | **Kostnaðarupphæð (raunverul.)** | **Færslunr.** |
|--|--|--|--|--|
| 01-01-23 | Innkaup | 1 | 20.00 | 1 |
| 01-01-23 | Innkaup | 1 | 40.00 | 2 |
| 01-01-23 | Útsala | -1 | -30,00 | 3 |
| 02-01-23 | Útsala | -1 | -65,00 | 4 |
| 02-02-23 | Innkaup | 1 | 100.00 | 5 |
| 02-03-23 | Útsala | -1 | -65,00 | 6 |

Meðalkostnaður við færslu númer 3 er reiknaður út í meðalkostnaðartímabili fyrir Janúar. Meðalkostnaður vegna færslna 4 og 6 er reiknaður út frá meðalkostnaðartímabili fyrir febrúar.  

Til að fá meðalkostnaðinn fyrir febrúar,  [!INCLUDE [prod_short](includes/prod_short.md)] bætir Meðalkostnaðurinn við vöruna sem fékkst í birgðum (100,00) við meðalkostnaðinn í upphafi tímabilsins (30,00). Samtala (130,00) er síðan deilt með heildarmagni í birgðum (2). Þessi Útreikningur gefur sem fyrr meðalkostnað á vöruna í febrúar-tímabilinu (65,00). Meðalkostnaðinum er úthlutað á birgðaminnkunina í tímabilinu (færslur 4 og 6).  

## <a name="setting-the-valuation-date"></a>Dagsetning virðismats ákveðin

  **Reiturinn Dagsetning**  verðmætasköpunar í  **töflunni Virðisfærsla**  ákvarðar meðaltímabilið sem birgðalækkunarfærsla tilheyrir. Þessi stilling á einnig við um birgðastöðu í vinnslu (VÍV).  

 Eftirfarandi tafla sýnir skilyrði sem eru notuð til að stilla matsdagsetninguna.  

| Aðstæður | Bókunardagsetning | Virt magn | Endurmat | Dagsetning virðismats |
|--|--|--|--|--|
| 1 |  | Jákvæð | Nei | Bókunardagsetning birgðafærslu |
| 2 | Síðar en síðasta matsdagsetning jafnaðra virðisfærslna | Neikvætt | Nei | Bókunardagsetning birgðafærslu |
| 3 | Fyrr en síðasta matsdagsetning jafnaðra virðisfærslna | Jákvætt | Nei | Síðasta matsdagsetning jafnaðra virðisfærslna |
| 4 |  | Neikvætt | Já | Bókunardagsetning virðisfærslu endurmats |

### <a name="example"></a>Dæmi

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

Ef magn birgða er minna en núll eftir að birgðaminnkun er bókuð er matsdagsetningin stillt á bókunardagsetningu birgðaminnkunar. Hægt er að breyta þessari dagsetningu þegar birgðaauka er beitt, samkvæmt reglum sem lýst er í athugasemd fyrr í þessum kafla.  

## <a name="recalculating-average-cost"></a>Meðalkostnaður reiknaður

Verðmæti birgða minnkar eftir því sem vegið meðaltal yrði einfalt í nokkrum tilvikum:

- Innkaup eru alltaf reikningsfærð fyrir sölu.
- Bókanir eru aldrei afturkræfari.
- Þú gerðir aldrei mistök.

Raunveruleikinn er hins vegar ólíkur.  

Eins og Dæmin í þessari grein sýna þá er matsdagsetningin skilgreind sem dagsetningin sem virðisfærslan er innifalin í útreikningi á meðalkostnaði. Þessi stilling gerir kleift að gera nokkra hluti fyrir vörur með Meðalkostnaðarútreikningsaðferðinni:  

- Reikningsfæra sölu á vöru áður en innkaup hennar eru reikningsgerð.  
- Bakfæra bókun.  
- Endurheimta ranga bókun.  

> [!NOTE]  
> Önnur ástæða fyrir þessum sveigjanleika er föst jöfnun. Frekari upplýsingar um fastar jafnanir eru í [Hönnunarupplýsingar: Birgðajöfnun](design-details-item-application.md).  

Vegna þessa sveigjanleika gæti þurft að endurreikna meðalkostnaðinn eftir bókun. Ef til dæmis er bókað fyrir aukningu birgða eða lækkun með matsdegi sem er á undan birgðalækkun. Endurreikningur meðalkostnaðar gerist sjálfkrafa þegar þú keyrir **Kostnaðarleiðrétting Birgðafærslur** runuvinnsluna, handvirkt eða sjálfvirkt.  

Hægt er að breyta birgðagildrunni innan reikningstímabils með því að breyta gildum í  **reitum meðalkostnaðartímabils**  og  **Tegund**  meðalkostnaðar. Við mælum hins vegar með að gæta varúðar og ráðfæra sig við endurskoðanda.  

### <a name="example-of-recalculated-average-cost"></a>Dæmi um Endurútgefið meðalinnkaupsverð

Þetta dæmi sýnir hvernig  [!INCLUDE [prod_short](includes/prod_short.md)]  endurreiknar meðalinnkaupsverð þegar bókað er á dagsetningu sem er á undan birgðalækkun. Dæmi um meðalkostnaðartímabil í **Dagur**.  

Eftirfarandi tafla sýnir virðisfærslur fyrir vöruna áður en bókað er.  

| Dagsetning virðismats | Magn | Kostnaðarupphæð (raunverul.) | Færslunr. |
|--|--|--|--|
| 01-01-20 | 1 | 10.00 | 1 |
| 01-02-20 | 1 | 20.00 | 2 |
| 02-15-20 | -1 | -15,00 | 3 |
| 02-16-20 | -1 | -15,00 | 4 |

Notandinn bókar birgðasaukninguna (færslunúmer 5) með matsdagsetningunni (01-03-20) en minnkun á birgðum. Til að jafna birgðir, verður meðaltals kostnaður skal endurreiknaður og leiðrétt til 17,00.  

Eftirfarandi tafla sýnir virðisfærslur fyrir vöruna eftir að færslunúmer 5 kemur til.  

| Dagsetning virðismats | Magn | Kostnaðarupphæð (raunverul.) | Færslunr. |
|--|--|--|--|
| 01-01-20 | 1 | 10.00 | 1 |
| 01-02-20 | 1 | 20.00 | 2 |
| 01-03-20 | 1 | 21.00 | 5 |
| 02-15-20 | -1 | -17,00 | 3 |
| 02-16-20 | -1 | -17,00 | 4 |

## <a name="see-also"></a>Sjá einnig

[Hönnunarupplýsingar: Birgðakostnaður](design-details-inventory-costing.md)  
[Hönnunarupplýsingar: Aðferð kostnaðarútreiknings](design-details-costing-methods.md)  
[Hönnunarupplýsingar: kostnaðarleiðrétting](design-details-cost-adjustment.md)  
[Hönnunarupplýsingar: Umsókn vöru](design-details-item-application.md)  
[Birgðakostnaði stjórnað](finance-manage-inventory-costs.md)  
[Fjármál](finance.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Orðalisti yfir hugtök í Dynamics 365 viðskiptaferlar](/dynamics365/guidance/business-processes/glossary)  
[Skilgreina Yfirlit fyrir kostnað vöru og þjónustu](/dynamics365/guidance/business-processes/product-service-define-cost-overview)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
