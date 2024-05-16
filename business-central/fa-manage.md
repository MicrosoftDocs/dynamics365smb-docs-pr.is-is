---
title: Stjórna eignum (myndband)
description: Kynntu þér virkni eigna og fáðu yfirsýn yfir það hvernig skuli vinna með og stjórna eignum.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'machinery, buildings'
ms.search.form: '5604, 5606, 5664, 5601, 5602, 5658, 5603, 5671, 5641, 5629, 5633, 5634, 5649, 5622, 5650'
ms.date: 05/06/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# Vinna með eignir

Með aðgerðinni Eignir í [!INCLUDE[prod_short](includes/prod_short.md)] fæst yfirlit yfir eignir notanda og hjálpar til við að tryggja að afskriftir þeirra séu réttar. Einnig er hægt að rekja viðhaldskostnað, stjórna vátryggingarskilmálum, bóka eignafærslur og búa til ýmsar skýrslur og upplýsingar.

## Myndbandsyfirlit

Eftirfarandi myndband fjallar um grunnatriði eigna:

> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4AegS?rel=0]

## Upphafleg uppsetning eigna

Áður en hægt er að stjórna eignum þarf að fylla út eftirfarandi uppsetningar:

- Sjálfgildi
- Eignabókhald
- Bókunarflokkar og tegundir
- Úthlutunarlyklar
- Eignabækur

Nánari upplýsingar eru í [Uppsetning eigna](fa-setup.md).

## Greiningar á eignum

Í þessum hluta er lýst þeim greiningartólum sem hægt er að nota til að fá innsýn í gögn um eignir.

| Til... | Sjá |
| --- | --- |
| Fræðast um getu til að greina gögn um eignir. | [Yfirlit yfir greiningar á eignum](fa-analytics-overview.md) |
| Gera tilfallanda greiningu eignagagna beint á listasíðum og fyrirspurnum. | [Tilfalengin greining á gögnum um eignir](ad-hoc-analysis-fa.md) |
| Skoða innbyggðar skýrslur fyrir eignir. | [Innbyggðar eignaskýrslur](fa-reports.md) |
| Fylgjast með viðhaldskostnaði. | [Fylgjast með viðhaldskostnaði](fa-how-maintain.md#to-monitor-maintenance-costs)|
| Fylgjast með vátryggingasviði. | [Eftirlit með vátryggingasviði](fa-how-insure.md#to-monitor-insurance-coverage) |
| Skoða afskráningarbókarfærslur. | [Skoða afskráningarbókarfærslur](fa-how-dispose-retire.md#to-view-disposal-ledger-entries) |
| Skoða áætluð afskráningargildi. | [Skoða áætlað virði afskráninga](fa-how-manage-budgets.md#to-view-projected-disposal-values) |

## Skrá eignir

Setja verður upp spjald fyrir hverja eign með upplýsingum um þær. Til dæmis er hægt að setja byggingar eða framleiðslubúnað upp sem aðaleignir með íhlutalista. Hægt er að flokka eignir á ýmsa vegu, svo sem eftir flokki, deild eða staðsetningu. Síðan er hægt að eignast, viðhalda og selja eignirnar. Hægt er einnig að setja upp áætlaðar eignir. Með fjárhagsáætlun er hægt að taka með fyrirsjáanlega kaup og sölu í skýrslum.

| Til  | Sjá |
| --- | --- |
| Stjórna fjárhagsáætlana eigna, áætlun stofnkostnaðar, áætlun afskráninga eigna og áætlun afskrifta. |[Umsjón fjárhagsáætlana fyrir eignir](fa-how-manage-budgets.md) |
| Stofna eignir, úthluta afskriftaaðferðum, bóka eignakaup, hrakvirði og prenta eignalista. |[Komast yfir eignir](fa-how-acquire.md) |

## Setja upp afskriftir fyrir eignir

Til að rekja eignaafskriftir og aðrar fjárhagslegar færslur fyrir eignir er sett upp ein eða fleiri afskriftabækur fyrir hverja þeirra. Nokkur þrep eru til að afskrifa eignir:

1. Keyra skýrslu til að reikna tímabilsafskriftir.
1. Færslurnar sem leiða til eru færðar inn í færslubókina.
1. Bóka skal færslubókina.

[!INCLUDE[prod_short](includes/prod_short.md)] styður nokkrar afskriftaraðferðir. Nánari upplýsingar eru notaðar með því að [fara í Afskriftaaðferðir](fa-depreciation-methods.md). Hægt er að setja upp margar afskriftabækur fyrir hverja eign í mismunandi tilgangi, svo sem eina fyrir skattskýrslugerð og aðra fyrir innri skýrslugerð.

| Til  | Sjá |
| --- | --- |
| Læra um mismunandi Aðferðir við afskriftir eigna |[Afskriftaaðferðir](fa-depreciation-methods.md) |
| Reikna afskriftir, bóka afskriftir og greina afskriftir í eignaskýrslum. |[Afskrifa eða greiða af eignum](fa-how-depreciate-amortize.md) |
| Skoða breytt virði afskriftabókar. | [Skoða breytt afskriftabókargildi](fa-how-trans-split-combine.md#to-view-changed-depreciation-book-values-due-to-fixed-asset-reclassification) |
| Skrá handvirkt eignafærslur á síðunni **Eignafjárhagsbók** eða á **síðunni Eignabók** eftir því hvort færslurnar eru fyrir fjárhagslega skýrslugerð eða fyrir innri stjórnun. | [Setja upp eignaafskriftir](fa-how-setup-depreciation.md) |

## Eignaviðhald og tryggingar

Hægt er að skrá viðhaldskostnað og næstu þjónustudagsetningu fyrir hverja eign. Rakning viðhaldskostnaðar getur skipt máli vegna fjárhagsáætlunar og ákveðið hvort skipta skuli um eign. Hægt er að tengja hverja eign einum eða fleiri vátryggingarskilmálum og sannreyna að iðgjöld vegna iðgjalda séu samræmd verðmæti eignanna.

| Til  | Sjá |
| --- | --- |
| Skrá þjónustuheimsóknir, bókun viðhaldskostnaðar og fylgjast með viðhaldskostnaði. |[Umsjón eigna](fa-how-maintain.md) |
| Fylgjast með viðhaldskostnaði. | [Fylgjast með viðhaldskostnaði](fa-how-maintain.md#to-monitor-maintenance-costs)|
| Uppfæra vátryggingarupplýsingar, bóka stofnkostnað á vátryggingarskilmála, breyta vátryggingasviði, skoða vátryggingaupplýsingar og gera lista yfir vátryggingaskírteini. |[Tryggja eignir](fa-how-insure.md) |
| Fylgjast með vátryggingasviði. | [Eftirlit með vátryggingasviði](fa-how-insure.md#to-monitor-insurance-coverage) |

## Endurflokka, flytja, skipta upp/sameina, leiðrétta virði, niðurfærslu og afskrá eignir

| Til  | Sjá |
| --- | --- |
| Endurflokka eignir, flytja eignir á aðra staði, skipta upp eignum eða sameina þær. |[Flytja, skipta upp eða sameina eignir](fa-how-trans-split-combine.md) |
| Leiðrétta verð eigna, bóka afskriftir og bóka niðurfærslur. |[Endurmeta eignir](fa-how-revalue.md) |
| Bóka afskráningarfærslur, skoða afskráningarbókarfærslur og bóka afskráningar að hluta. |[Afskrá eða innkalla eignir](fa-how-dispose-retire.md) |
| Skoða afskráningarbókarfærslur. | [Skoða afskráningarbókarfærslur](fa-how-dispose-retire.md#to-view-disposal-ledger-entries) |
| Skoða áætluð afskráningargildi. | [Skoða áætlað virði afskráninga](fa-how-manage-budgets.md#to-view-projected-disposal-values) |

## Sjá einnig .

[Uppsetning eigna](fa-setup.md)  
[Yfirlit yfir greiningar á eignum](fa-analytics-overview.md)  
[Yfirlit yfir Fjármál](finance.md)  
[Undirbúðu þig fyrir að gera viðskipti](ui-get-ready-business.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Breyta því hvaða eiginleikar eru sýndir](ui-experiences.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  

[!INCLUDE[footer-include](includes/footer-banner.md)]
