---
title: "Hvernig á að rekja tengsl milli eftirspurnar og framboðs | Microsoft Docs"
description: "Frá hverju framboðs- eða eftirspurnarskjali í hinu svokallaða pöntunarneti, geturðu rakið pöntunareftirspurn (rakið magn), spá, standandi sölupöntun eða áætlunarfæribreytu (órakið magn) sem á við umrædda áætlunarlínu."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 8c53878418592daf9179d6864da4447ca8ad1262
ms.contentlocale: is-is
ms.lasthandoff: 03/22/2018

---
# <a name="track-relations-between-demand-and-supply"></a>Rekja tengsl milli eftirspurnar og framboðs
Frá hverju framboðs- eða eftirspurnarskjali í hinu svokallaða pöntunarneti, geturðu rakið pöntunareftirspurn (rakið magn), spá, standandi sölupöntun eða áætlunarfæribreytu (órakið magn) sem á við umrædda áætlunarlínu.

Áætlunarvinnublöðin bjóða einnig hjálplegar áætlunarupplýsingar um ópantaðar einingar, til að aðstoða skipuleggjandann við að búa til fullkomna framboðsáætlun. Sjá hlutann „Óraktar áætlunareiningar“ fyrir frekari upplýsingar.

## <a name="to-track-linked-items"></a>Rekja tengdar vörur
Pöntunarrakningin sýnir hvernig sölupantanir, framleiðslupantanir og innkaupapantanir tengjast aðalframleiðslupöntuninni í gegnum áætlanir og frátekningarkerfi.

Eftirfarandi lýsir hvernig rekja skal tengdar vörur í fastáætlunarpöntun. Skrefin eru svipuð fyrir allar aðrar tegundir af pöntunum, og frá áætlunarvinnublaðslínum.

1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn  **Fastáætluð framleiðslupöntun** og velja svo viðeigandi tengil.
2. Viðeigandi fastáætluð framleiðslupöntun er opnuð úr listanum.
3. Á flýtiflipanum **Línur** skal velja aðgerðina **Aðgerðir**, og velja svo aðgerðina **Pöntunarrakning**.

Línurnar í glugganum **Pöntunarrakning** sýna fylgiskjölin sem tengjast gildandi framleiðslupöntunarlínunni.

## <a name="untracked-planning-elements"></a>Órakin áætlunaratriði
Glugginn **Óraktar áætlunareiningar** opnast þegar þú velur **Órakið magn** reitinn í **Pantanaáætlun** glugginn. Það þjónar tvenns konar tilgangi:

1. Að geyma upplýsingar um órakið magn sem birtist þegar notandi flettir upp í glugganum Rakning pöntunar til að sjá órakið magn.
2. Að geyma viðvörunarboð sem birtast þegar notandi smellir á **Viðvörun** tákn á **áætlunarvinnublaði** glugganum.

Glugginn inniheldur færslur sem standa fyrir órakið umframmagn í pöntunarrakningarkerfi. Þessar færslur eru stofnaðar við áætlunarkeyrslu og útskýra hvaðan órakta umframmagnið í rakningarlínunum kom. Þetta órakta umframmagn kom frá:

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
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

