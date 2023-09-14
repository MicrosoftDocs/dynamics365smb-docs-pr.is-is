---
title: 'Hönnunarupplýsingar: Aðferð kostn.útreiknings'
description: Í þessu efnisatriði er því lýst hvernig aðferð við kostnaðarútreikning hefur áhrif á það hvort raunverulegt og áætlað virði nýtist og sé notað við kostnaðarútreikning.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 05/12/2023
ms.author: bholtorf
---
# Hönnunarupplýsingar: Aðferð kostn.útreiknings

Það veltur á aðferð við kostnaðarútreikning hvort raunverulegt eða áætlað virði nýtist og sé notað við kostnaðarútreikning. Kostnaðaraðferðin hefur líka áhrif á það hvernig kostnaðarflæðið er skráð, ásamt bókunardagsetningu og lotu.

> [!NOTE]
> Ekki er hægt að breyta aðferð kostnaðarútreiknings fyrir vöru ef birgðabókarfærslur eru til fyrir vöruna. Frekari upplýsingar er að finna í [Hönnunarupplýsingar: Breyta kostnaðarútreikningi fyrir vörur](design-details-changing-costing-methods.md).

Eftirfarandi aðferðir eru studdar í [!INCLUDE[prod_short](includes/prod_short.md)]:  

| Aðferð kostn.útreiknings | Description | Hvenær skal nota |
|--|--|--|
| FIFO | Kostnaðarverð vöru er raunvirði sérhverrar innhreyfingar vörunnar, valið samkvæmt FIFO-reglunni.<br /><br /> Fyrir verðmat birgða, er gert ráð fyrir að vörur sem settar voru fyrst í birgðir seljist fyrst. | Í umhverfi fyrirtækja þar sem vörukostnaður er stöðugt.<br /><br /> (Þegar verð hækkar sýnir efnahagsreikningurinn hærra virði. Þetta þýðir að skattaskuldir aukast, en möguleikar til að fá lánsfé aukast.<br /><br /> Notið með vörum með takmarkaðan endingartíma, þar sem elstu vörurnar þarf að selja áður en þær fara fram yfir síðasta söludag. |
| LIFO | Kostnaðarverð vöru er raunvirði sérhverrar innhreyfingar vörunnar, valin samkvæmt LIFO-reglunni.<br /><br /> Fyrir verðmat birgða, er gert ráð fyrir að vörur sem settar voru síðast í birgðir seljist fyrst. | Óheimilt í mörgum löndum, þar sem það getur verið notað til að minnka hagnað.<br /><br /> (Þegar verð hækkar, lækkar virðið á rekstarreikningnum. Þetta þýðir að skattaskuldir minnka, en möguleikar til að fá lánsfé rýrna. |
| Meðaltal | Kostnaðarverð vöru er reiknað sem meðaleiningaverð vara á hverjum tímapunkti eftir innkaup.<br /><br /> Fyrir verðmat birgða er gert ráð fyrir að allar birgðir séu seldar samtímis. | Í umhverfi fyrirtækja þar sem vörukostnaður er óstöðugur.<br /><br /> Þar sem birgðum er raðað eða blandað saman og er ekki hægt að aðskilja, til dæmis kemísk efni. |
| Sérstakt | Kostnaðarverð vöru er nákvæmur kostnaður þegar tekið var við vörunni. | Í framleiðslu eða viðskiptum með vörur sem auðvelt er að bera kennsl á og hafa frekar hátt kostnaðarverð.<br /><br /> Notist fyrir vörur sem falla undir reglugerð.<br /><br /> Notið fyrir vörur með raðnúmer. |
| Staðlað | Kostnaðarverð vöru er forstillt samkvæmt áætlun.<br /><br /> Þegar raunkostnaður er innleystur síðar, verður að breyta staðlaða kostnaðarverðinu í raunkostnaðinn, í gegnum fráviksgildi. | Þar sem kostnaðarstýring er mikilvæg.<br /><br /> Í endurtekingaframleiðslu, til að meta kostnaðinn á beinu efni, beinni framleiðslu og sameiginlegs kostnaðar.<br /><br /> Í öguðu umhverfi og þar sem starfsfólkið viðheldur gæðastaðli. |

Á meðfylgjandi mynd sést kostnaðarflæði gegnum birgðir fyrir hverja kostnaðarmatsaðferð.  

![Myndræn framsetning kostnaðarútreiknings.](media/design_details_inventory_costing_7_costing_methods.png "Myndræn framsetning kostnaðarútreikninga")  

Aðferð kostnaðarútreiknings eru mismunandi í því hvernig þeir meta birgðaminnkun og hvort þær nota raunkostnað eða staðalkostnað vörubirgðir sem grunn matsins. Eftirfarandi tafla útskýrir mismunandi einkenni. (LIFO-aðferðin er útilokuð þar sem hún er mjög svipuð FIFO-aðferðinni.)  
<!--Old  table
|Category|FIFO|Average|Standard|Specific|  
|-|----------|-------------|--------------|--------------|  
|General characteristic|Easy to understand|Based on period options: **Day**/**Week**/**Month**/**Quarter**/**Accounting Period**.<br /><br /> Can be calculated per item or per item/location/variant.|Easy to use, but requires qualified maintenance.|Requires item tracking on both inbound and outbound transaction.<br /><br /> Typically used for serialized items.|  
|Application/Adjustment|Application keeps track of **the remaining quantity**.<br /><br /> Adjustment forwards costs according to quantity application.|Application keeps track of the **remaining quantity**.<br /><br /> Costs are calculated and forwarded per the **valuation date**.|Application keeps track of the **remaining quantity**.<br /><br /> Application is based on FIFO.|All applications are fixed.|  
|Revaluation|Revalues invoiced quantity only.<br /><br /> Can be done per item or per item ledger entry.<br /><br /> Can be done backward in time.|Revalues invoiced quantity only.<br /><br /> Can be done per item only.<br /><br /> Can be done backward in time.|Revalues invoiced and un-invoiced quantities.<br /><br /> Can be done per item or per item ledger entry.<br /><br /> Can be done backward in time.|Revalues invoiced quantity only.<br /><br /> Can be done per item or per item ledger entry.<br /><br /> Can be done backward in time.|  
|Miscellaneous|If you back-date an inventory decrease, then existing entries are NOT reapplied to provide a correct FIFO cost flow.|If you back-date an inventory increase or decrease, then the average cost is recalculated, and all affected entries are adjusted.<br /><br /> If you change the period or calculation type, then all affected entries must be adjusted.|Use the **Standard Worksheet** page to periodically update and roll up standard costs.<br /><br /> Is NOT supported per SKU.<br /><br /> No historic records exist for standard costs.|You can use specific item tracking without using the Specific costing method. Then the cost will NOT follow the lot number, but the cost assumption of the selected costing method.|  
-->
<!--Table flipped for slightly better readability -->

||Almennir eiginleikar|Jöfnun/Leiðrétting |Endurmat|Blandað |
|-|---------|---------|---------|---------|
|**FIFO**     |Auðskilið|Jöfnun rekur **eftirstandandi magn**.<br /><br /> Leiðrétting framsendir kostnað í samræmi við jöfnun magns. |Uppreiknar reikningsfært magn eingöngu.<br /><br /> Er hægt að reikna út á vöru eða birgðafærslu.<br /><br /> Er hægt að gera aftur á bak í tíma.|Ef birgðaminnkun er endurdagsett eru færslur sem fyrir eru EKKI endurjafnaðar til að setja fram rétt FIFO-kostnaðarflæði.|
|**Meðaltal**     |Byggt á tímabilsvalkostum: **Dagur**/**/Vika/**/**Mánuður**/**/Ársfjórðungur/**/**Reikningstímabil**.<br /><br /> Hægt að reikna út á vöru , eða á vörueiningu/staðsetningu/afbrigði.|Jöfnun rekur **eftirstandandi magn**.<br /><br /> Kostnaður er reiknaður og sendur á **dagsetningu mats** |Uppreiknar reikningsfært magn eingöngu.<br /><br /> Er hægt að gera á vöru eingöngu.<br /><br /> Er hægt að gera aftur á bak í tíma. |Ef birgðaaukning eða -minnkun er endurdagsett er meðalkostnaðurinn endurreiknaður og allar færslur sem verða fyrir áhrifum eru leiðréttar.<br /><br /> Ef tímabili eða gerð útreikninga er breytt verður að leiðrétta allar færslur sem verða fyrir áhrifum.|
|**Staðlað**     |Einfalt í notkun en þarf gott viðhald.|Jöfnun rekur **eftirstandandi magn**.<br /><br /> Jöfnun byggist á FIFO.|Uppreiknar innheimt og óreikningsfærðan magn.<br /><br /> Er hægt að reikna út á vöru eða birgðafærslu.<br /><br /> Er hægt að gera aftur á bak í tíma.|Notaðu síðuna **Staðlað vinnublað** til að uppfæra reglulega og taka saman staðalkostnaði.<br /><br /> Er EKKI studd á birgðahaldseiningu.<br /><br /> Engar sögulegar færslur eru til staðar fyrir staðlaðan kostnað.|
|**Sérstakt**     |Krefst vörurakningar á bæði færslur á innleið og útleið.<br /><br /> Venjulega notað fyrir vörur með raðnúmer.|Allar jafnanir eru fastar.|Uppreiknar reikningsfært magn eingöngu.<br /><br /> Er hægt að reikna út á vöru eða birgðafærslu.<br /><br /> Er hægt að gera aftur á bak í tíma.|Hægt er að nota sértæka vörurakninguán þess að nota Tilgreinda aðferð kostnaðarútreiknings. Kostnaðurinn mun þá EKKI fylgja lotunúmerinu, heldur kostnaðaráætlun valinnar aðferðar kostnaðarútreiknings.|

## Dæmi

Þessi hluti gefur dæmi um hvernig mismunandi kostnaðaraðferðir hafa áhrif birgðavirði.  

Eftirfarandi tafla sýnir birgðaaukningu og -minnkun sem dæmin eru byggð á.  

|Bókunardags.|Magn|Færslunr.|  
|------------------|--------------|---------------|  
|01-01-20|1|1|  
|01-01-20|1|2|  
|01-01-20|1|3|  
|02-01-20|-1|4|  
|03-01-20|-1|5|  
|04-01-20|-1|6|  

> [!NOTE]  
> Magn í birgðaeiningum verður núll. Þar af leiðandi verður birgðavirði einnig að vera núll, hver sem aðferð kostnaðarútreiknings er.  

### Áhrif aðferða við kostnaðarútreikning til að meta birgðaminnkun  

Fyrir vörur með kostnaðarútreikninga sem nota raunverulegan kostnað sem grunn fyrir verðmat (**FIFO (fyrst inn - fyrst út)**, **LIFO (síðast inn - fyrst út)**, **Meðaltal** eða **Tilgreint**), er birgðaaukning metin á kaupverði vörunnar.  

- **Staðlað**  

    Þegar notuð er kostnaðaraðferðin **Staðlað** er birgðaaukning metin á því staðalverði vörunnar sem er í gildi.  

#### Staðlað  

Þegar notuð er kostnaðaraðferðin **Staðlað** er birgðaaukning metin á því staðalverði vörunnar sem er í gildi.  

### Áhrif aðferða við kostnaðarútreikning til að meta birgðaminnkun

- **FIFO**  

    Fyrir vörur sem nota aðferðina **FIFO (fyrst inn - fyrst út)** við kostnaðarútreikning eru vörurnar sem eru keyptar fyrst alltaf seldar fyrst (færsla númer 3, 2 og 1 í þessu dæmi). Í samræmi er birgðaminnkun verðmetin með því að nota virði fyrstu birgðaaukningarinnar.  

     Kostnaður seldra vara er reiknuð með virði fyrstu birgðakaupa.  

     Eftirfarandi tafla sýnir hvernig birgðir sem minnka eru metnar fyrir kostnaðarmatsaðferðina **FIFO (fyrst inn - fyrst út)**.  

    |Bókunardags.|Magn|Kostnaðarupphæð (raunverul.)|Færslunr.|  
    |------------------|--------------|----------------------------|---------------|  
    |02-01-20|-1|-10,00|4|  
    |03-01-20|-1|-20,00|5|  
    |04-01-20|-1|-30,00|6|  

- **LIFO**  

    Fyrir vörur sem nota aðferðina **LIFO (síðast inn - fyrst út)** við kostnaðarútreikning eru vörurnar sem eru keyptar síðast alltaf seldar fyrst (færsla númer 3, 2 og 1 í þessu dæmi). Í samræmi er birgðaminnkun verðmetin með því að nota virði síðustu birgðaaukningarinnar.  

     Kostnaður seldra vara er reiknuð með virði síðustu birgðakaupa.  

     Eftirfarandi tafla sýnir hvernig birgðir sem minnka eru metnar fyrir kostnaðarmatsaðferðina **LIFO (fyrst inn - fyrst út)**.  

    |Bókunardags.|Magn|Kostnaðarupphæð (raunverul.)|Færslunr.|  
    |------------|--------|--------------------|---------|  
    |02-01-20|-1|-30,00|4|  
    |03-01-20|-1|-20,00|5|  
    |04-01-20|-1|-10,00|6|  

- **Meðaltal**  

    Aðferð við útreikning meðalkostnaðari **Meðaltal**metur birgðaminnkun með því að reikna út vegið meðaltal eftirstandandi birgða á síðasta degi meðalkostnaðartímabils þar sem birgðaminnkun var bókuð. Nánari upplýsingar eru í [Upplýsingar um hönnun: Meðalkostnaður](design-details-average-cost.md).  

     Eftirfarandi tafla sýnir hvernig birgðir sem minnka eru metnar fyrir kostnaðarmatsaðferðina **Meðaltal**.  

    | Bókunardags. | Magn | Kostnaðarupphæð (raunverul.) | Færslunr. |
    |--|--|--|--|
    | 02-01-20 | -1 | -20,00 | 4 |
    | 03-01-20 | -1 | -20,00 | 5 |
    | 04-01-20 | -1 | -20,00 | 6 |

- **Staðlað**  

    Fyrir vörur sem nota aðferðina **Staðlað** til kostnaðarútreiknings er birgðaminnkun metin svipað og í kostnaðarútreikningnum **FIFO (fyrst inn - fyrst út)** nema að verðmat er byggt á staðalkostnaði, ekki raunverulegur kostnaður.  

    Eftirfarandi tafla sýnir hvernig birgðir sem minnka eru metnar fyrir kostnaðarmatsaðferðina **Staðlað**.  

    |Bókunardags.|Magn|Kostnaðarupphæð (raunverul.)|Færslunr.|  
    |------------------|--------------|----------------------------|---------------|  
    |02-01-20|-1|-15,00|4|  
    |03-01-20|-1|-15,00|5|  
    |04-01-20|-1|-15,00|6|  

- **Sérstakt**  

    Aðferð kostnaðarútreiknings áæltar konstaðarflæði úr birgðaaukningu í birgðaminnkun. Hins vegar, ef nákvæmari upplýsingar um kostnaðarverðflæði eru til, þá er hægt að hnekkja þessari forsendu með því að skapa fasta jöfnun milli færslna. Föst jöfnun stofnar tengil á milli birgðaminnkunar og tiltekinnar birgðaaukningar og beinir kostnaðarflæði í samræmi við það.  

    Fyrir vörur sem nota aðferðina **Tilgreint** við kostnaðarútreikning er birgðaminnkun metin á grunni birgðaaukningarinnar sem er tengt í með föstu jöfnuninni.  

    Eftirfarandi tafla sýnir hvernig birgðir sem minnka eru metnar fyrir kostnaðarmatsaðferðina **Sérstakt**.  

    |Bókunardags.|Magn|Kostnaðarupphæð (raunverul.)|Jafna færslu|Færslunr.|
    |------------|--------|--------------------|----------------|---------|  
    |02-01-20|-1|-20,00|**2**|4|  
    |03-01-20|-1|-10,00|**1**|5|  
    |04-01-20|-1|-30,00|**3**|6|  

## Sjá einnig

[Hönnunarupplýsingar: Birgðakostnaður](design-details-inventory-costing.md)  
[Hönnunarupplýsingar Frávik](design-details-variance.md)  
[Hönnunarupplýsingar: Meðalkostnaður](design-details-average-cost.md)  
[Hönnunarupplýsingar: Umsókn vöru](design-details-item-application.md)  
[Birgðakostnaði stjórnað](finance-manage-inventory-costs.md)  
[Fjármál](finance.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Orðalisti yfir hugtök í Dynamics 365 viðskiptaferlar](/dynamics365/guidance/business-processes/glossary)  
[Skilgreina Yfirlit fyrir kostnað vöru og þjónustu](/dynamics365/guidance/business-processes/product-service-define-cost-overview)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
