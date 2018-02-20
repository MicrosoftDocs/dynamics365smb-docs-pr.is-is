---
title: "Hönnunarupplýsingar - Meðhöndlun endurpöntunarstefnu | Microsoft Docs"
description: "Yfirlit yfir verkhluta sem taka til skilgreininga á endurpöntunarstefnu í framboðsáætlun."
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
ms.openlocfilehash: 2a6658508f8e12a11989d54da6d6c8e3a36631cc
ms.contentlocale: is-is
ms.lasthandoff: 12/14/2017

---
# <a name="design-details-handling-reordering-policies"></a>Hönnunarupplýsingar: Meðhöndlun endurpöntunarstefnur
Til þess að vara geti tekið þátt í birgðaáætlunargerð verður að tilgreina endurpöntunarstefnu. Eftirfarandi fjórar endurpöntunarstefnur eru til:  
  
* Fast endurpöntunarmagn  
* Hámarksmagn  
* Röð  
* Lotu-fyrir-lotu  
  
Stefnur um fast endurpöntunarmagn og hámarksmagn tengjast birgðaáætlunargerð. Þó birgðaáætlanagerð sé tæknilega einfaldari en mótbókunaraðferð eru þessar stefnur báðar til með nákvæmri mótbókun framboðs og pöntunarrakningu. Til að stjórna samþættingu milli tveggja, og að veita sýnileika í þátt áætlanagerð rökfræði, strangar reglur gilda hversu endurröðun reglur eru meðhöndlaðar.  
  
## <a name="in-this-section"></a>Í þessum hluta  
[Hönnunarupplýsingar: Hlutverk endurpöntunarmarks](design-details-the-role-of-the-reorder-point.md)  
[Hönnunarupplýsingar Vöktun áætlaðar birgðastigs og endurpöntunarmark](design-details-monitoring-the-projected-inventory-level-and-the-reorder-point.md)  
[Hönnunarupplýsingar: Hlutverk tímaramma](design-details-the-role-of-the-time-bucket.md)  
[Hönnunarupplýsingar: undir yfirflæðisstigi](design-details-staying-under-the-overflow-level.md)  
[Hönnunarupplýsingar: Meðhöndlun Áætlaðrar Neikvæðra birgða](design-details-handling-projected-negative-inventory.md)  
[Hönnunarupplýsingar: Endurpöntunarstefnur](design-details-reordering-policies.md)  
  
## <a name="see-also"></a>Sjá einnig  
[Hönnunarupplýsingar: áætlunarfæribreyta](design-details-planning-parameters.md)   
[Hönnunarupplýsingar: áætlunartafla](design-details-planning-assignment-table.md)   
[Hönnunarupplýsingar: Miðlægar hugmyndir áætlanakerfisins](design-details-central-concepts-of-the-planning-system.md)   
[Hönnunarupplýsingar: Jöfnun eftirspurnar og framboðs](design-details-balancing-demand-and-supply.md)   
[Hönnunarupplýsingar: framboðsáætlun](design-details-supply-planning.md)
