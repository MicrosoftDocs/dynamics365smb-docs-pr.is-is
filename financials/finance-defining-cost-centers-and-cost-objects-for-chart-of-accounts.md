---
title: "Skilgreining kostnaðarstaði og kostnaðarhluti fyrir bókhaldslykil | Microsoft Docs"
description: "Hægt er að flytja útgjalda- og tekjufærslur sjálfkrafa úr fjárhag í kostnaðarbókhald, annað hvort fyrir hverja fjarhagsfærslu eða með keyrslu. Þegar flutningurinn er framkvæmdur flytur kerfið aðeins færslur sem þegar eru tengdar við kostnaðarstað eða kostnaðarhlut. Til að búa til merkingarbæran flutning þarf að tryggja að kostnaðarstaðir og kostnaðarhlutir séu rétt skilgreindir."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 0a3b89e2d2a59aa3434e747976437f24860be408
ms.contentlocale: is-is
ms.lasthandoff: 09/22/2017

---
# <a name="defining-cost-centers-and-cost-objects-for-chart-of-accounts"></a>Skilgreining kostnaðarstaði og kostnaðarhluti fyrir bókhaldslykil
Hægt er að flytja útgjalda- og tekjufærslur sjálfkrafa úr fjárhag í kostnaðarbókhald, annað hvort fyrir hverja fjarhagsfærslu eða með keyrslu. Þegar flutningurinn er framkvæmdur flytur [!INCLUDE[d365fin](includes/d365fin_md.md)] aðeins færslur sem þegar eru tengdar við kostnaðarstað eða kostnaðarhlut. Til að búa til merkingarbæran flutning þarf að tryggja að kostnaðarstaðir og kostnaðarhlutir séu rétt skilgreindir.  

## <a name="defining-default-dimension-values-for-general-ledger-accounts"></a>Skilgreining sjálfgefin víddargildi fyrir fjárhagslykla  
Fyrir hvern fjárhagsreikning er hægt að skilgreina sjálfgefið víddargildi í töflunni **Sjálfgefið víddargildi**. Eftirfarandi dæmi sýnir hvernig eigi að skilgreina að það ætti alltaf að vera kostnaðarstaður DEILDAR, en aldrei kostnaðarhlutur VERKEFNIS þegar bókað er á almennan fjárhagslykil.  

|**Víddarkóti**|**Virðisbókun**|  
|------------------------------------------|-----------------------------------------|  
|Deild|Kóti tilskilinn|  
|Verkefni|Enginn kóti|  

## <a name="defining-dimension-values-for-overhead-costs-and-direct-costs"></a>Skilgreining á víddargildi fyrir sameiginlegan kostnað og beinan kostnað  
 Hægt er að flytja rekstrarkostnað í kostnaðarstað og beinan kostnað í kostnaðaríhlut. Eftirfarandi tafla sýnir bestu samsetningu uppsetningargilda vídda.  

|Flytja í|Bókun kostnaðarstaðar|Bókun kostnaðarhlutar|  
|-----------------|-------------------------|-------------------------|  
|Kostnaðarstaður|Kóti tilskilinn|Enginn kóti|  
|Kostnaðarhlutur|Enginn kóti|Kóti tilskilinn|  

> [!NOTE]  
>  Til að ganga úr skugga um að fyrirfram skilgreindur kostnaðarstaður og kostnaðarhlutur sem eru sett upp í fjárhag séu sjálfkrafa færðar yfir í kostnaðarbókhald skal velja gátreitinn **Athuga fjárhagsbókanir** í glugganum.Uppsetning kostnaðarbókhalds  

## <a name="see-also"></a>Sjá einnig  
[Kostnaðarreikningur](finance-manage-cost-accounting.md)  
[Hvernig á að setja upp Kostnaðarstaði](finance-how-to-set-up-cost-centers.md)   
[Hvernig á að setja upp kostnaðarhluti](finance-how-to-set-up-cost-objects.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
