---
title: Skilgreining kostnaðarstaði og kostnaðarhluti fyrir bókhaldslykil | Microsoft Docs
description: Hægt er að flytja útgjalda- og tekjufærslur sjálfkrafa úr fjárhag í kostnaðarbókhald, annað hvort fyrir hverja fjarhagsfærslu eða með keyrslu. Þegar flutningurinn er framkvæmdur flytur kerfið aðeins færslur sem þegar eru tengdar við kostnaðarstað eða kostnaðarhlut. Til að búa til merkingarbæran flutning þarf að tryggja að kostnaðarstaðir og kostnaðarhlutir séu rétt skilgreindir.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
redirect_url: finance-set-up-cost-accounting
ms.openlocfilehash: 00c0ac4a37476c2ab21ddc850e80e7abeb5eda18
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/29/2019
ms.locfileid: "1242055"
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
>  Til að ganga úr skugga um að fyrirfram skilgreindur kostnaðarstaður og kostnaðarhlutur sem eru sett upp í fjárhag séu sjálfkrafa færðar yfir í kostnaðarbókhald skal velja gátreitinn **Athuga fjárhagsbókanir** á síðunni Uppsetning kostnaðarbókhalds  

## <a name="see-also"></a>Sjá einnig  
[Kostnaðarreikningur](finance-manage-cost-accounting.md)  
[Uppsetning kostnaðarbókhalds](finance-set-up-cost-accounting.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
