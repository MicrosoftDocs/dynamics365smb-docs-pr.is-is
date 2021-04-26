---
title: Hvernig á að rekja tengsl milli eftirspurnar og framboðs | Microsoft Docs
description: Frá hverju framboðs- eða eftirspurnarskjali í hinu svokallaða pöntunarneti, geturðu rakið pöntunareftirspurn (rakið magn), spá, standandi sölupöntun eða áætlunarfæribreytu (órakið magn) sem á við umrædda áætlunarlínu.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 8ff7653ec28e70c13842f9b66bff91b7d8b48f98
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5787628"
---
# <a name="track-relations-between-demand-and-supply"></a>Rekja tengsl milli eftirspurnar og framboðs
Frá hverju framboðs- eða eftirspurnarskjali í hinu svokallaða pöntunarneti, geturðu rakið pöntunareftirspurn (rakið magn), spá, standandi sölupöntun eða áætlunarfæribreytu (órakið magn) sem á við umrædda áætlunarlínu.

Áætlunarvinnublöðin bjóða einnig hjálplegar áætlunarupplýsingar um ópantaðar einingar, til að aðstoða skipuleggjandann við að búa til fullkomna framboðsáætlun. Frekari upplýsingar er að finna í [Óraktar áætlunareiningar](production-how-track-demand-supply.md#untracked-planning-elements).

## <a name="to-track-linked-items"></a>Rekja tengdar vörur
Pöntunarrakningin sýnir hvernig sölupantanir, framleiðslupantanir og innkaupapantanir tengjast aðalframleiðslupöntuninni í gegnum áætlanir og frátekningarkerfi.

Eftirfarandi lýsir hvernig rekja skal tengdar vörur í fastáætlunarpöntun. Skrefin eru svipuð fyrir allar aðrar tegundir af pöntunum, og frá áætlunarvinnublaðslínum.

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Fastáætluð framl.pöntun** og veldu síðan tengda tengilinn.
2. Viðeigandi fastáætluð framleiðslupöntun er opnuð úr listanum.
3. Á flýtiflipanum **Línur** skal velja aðgerðina **Aðgerðir**, og velja svo aðgerðina **Pöntunarrakning**.

Línurnar í glugganum **Pöntunarrakning** sýna fylgiskjölin sem tengjast gildandi framleiðslupöntunarlínunni.

## <a name="untracked-planning-elements"></a>Órakin áætlunaratriði
Síðan **Óraktar áætlunareiningar** opnast þegar þú velur **Órakið magn** reitinn í **Pantanaáætlun** glugginn. Það þjónar tvenns konar tilgangi:

1. Að geyma upplýsingar um órakið magn sem birtist þegar notandi flettir upp á síðunni Rakning pöntunar til að sjá órakið magn.
2. Að geyma viðvörunarboð sem birtast þegar notandi smellir á **Viðvörun** tákn á síðunni **Áætlunarvinnublað**.

Síðan inniheldur færslur sem standa fyrir órakið umframmagn í pöntunarrakningarkerfi. Þessar færslur eru stofnaðar við áætlunarkeyrslu og útskýra hvaðan órakta umframmagnið í rakningarlínunum kom. Þetta órakta umframmagn kom frá:

- Framleiðsluspá
- Standandi pantanir
- Magn í öryggisbirgðum
- Endurpöntunarmark
- Hámarksbirgðir
- Pöntunarmagn
- Hámarksmagn pöntunar
- Lágmarksmagn pöntunar
- Fjöldapanta
- Hömlur (% af lotustærð)

## <a name="see-also"></a>Sjá einnig  
[Áætlun](production-planning.md)   
[Uppsetning framleiðslu](production-configure-production-processes.md)  
[Framleiðsla](production-manage-manufacturing.md)    
[Birgðir](inventory-manage-inventory.md)  
[Innkaup](purchasing-manage-purchasing.md)  
[Hönnunarupplýsingar: Frátekning, rakning og aðgerðarboð](design-details-reservation-order-tracking-and-action-messaging.md)  
[Hönnunarupplýsingar: framboðsáætlun](design-details-supply-planning.md)   
[Uppsetning bestu venja: Framboðsáætlun](setup-best-practices-supply-planning.md)  
[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]