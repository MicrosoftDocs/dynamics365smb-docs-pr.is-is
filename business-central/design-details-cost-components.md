---
title: Hönnunarupplýsingar - kostnaðaríhlutir | Microsoft Docs
description: Kostnaðarþættir eru mismunandi gerðir af kostnaði sem mynda virði birgðaaukningar eða birgðaminnkunar.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/08/2021
ms.author: edupont
ms.openlocfilehash: 1c1dd2eafb648a7c6053406ea3c931d6e7cecb76
ms.sourcegitcommit: 0953171d39e1232a7c126142d68cac858234a20e
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/09/2021
ms.locfileid: "6215359"
---
# <a name="design-details-cost-components"></a>Hönnunarupplýsingar: kostnaðaríhlutur
Kostnaðarþættir eru mismunandi gerðir af kostnaði sem mynda virði birgðaaukningar eða birgðaminnkunar.  

 Eftirfarandi tafla sýnir mismunandi kostnaðarþætti og allan þann undirkostnaðarþætti sem þeir samanstanda af.  

|Kostnaðaríhlutur|Víkjandi kostnaður íhlutar|Description|  
|--------------------|--------------------------------|---------------------------------------|  
|Beinn kostnaður|Kostnaðarverð (beint kaupverð)|Kostnaður sem rekja má til kostnaðarhlutar.|  
|Beinn kostnaður|Farmgjald (Kostnaðarauki)|Kostnaður sem rekja má til kostnaðarhlutar.|  
|Beinn kostnaður|Tryggingakostnaður (Kostnaðarauki)|Kostnaður sem rekja má til kostnaðarhlutar.|  
|Óbeinn kostnaður||Kostnaður sem ekki má rekja beint til kostnaðarhlutar.|  
|Frávik|Frávik í innkaupum|Munurinn á raunkostnaði og stöðluðu kostnaðarverði sem aðeins er bókað vegna vöru þar sem aðferð **Staðlaðs** kostnaðarverðs er beitt.|  
|Frávik|Efnisfrávik|Munurinn á raunkostnaði og stöðluðu kostnaðarverði sem aðeins er bókað vegna vöru þar sem aðferð **Staðlaðs** kostnaðarverðs er beitt.|  
|Frávik|Getufrávik|Munurinn á raunkostnaði og stöðluðu kostnaðarverði sem aðeins er bókað vegna vöru þar sem aðferð **Staðlaðs** kostnaðarverðs er beitt.|  
|Frávik|Frávik undirverktaka|Munurinn á raunkostnaði og stöðluðu kostnaðarverði sem aðeins er bókað vegna vöru þar sem aðferð **Staðlaðs** kostnaðarverðs er beitt.|  
|Frávik|Fráv. sameiginl. kost. afk.getu|Munurinn á raunkostnaði og stöðluðu kostnaðarverði sem aðeins er bókað vegna vöru þar sem aðferð **Staðlaðs** kostnaðarverðs er beitt.|  
|Frávik|Sameiginl. kostn.frávik framleiðslu|Munurinn á raunkostnaði og stöðluðu kostnaðarverði sem aðeins er bókað vegna vöru þar sem aðferð **Staðlaðs** kostnaðarverðs er beitt.|  
|Endurmat||Afskrift eða uppfærsla miðað við núgildandi birgðavirði.|  
|Sléttun||Endurnýta viðmótssérstillingu fyrir pantanavinnsluforstillingu í aðra gagnagrunna|  

> [!NOTE]  
>  Farm- og vátryggingakostnaður eru kostnaðarauki sem hægt er að bæta við kostnað vöru hvenær sem er. Þegar runuvinnslan **Kostnaðarleiðrétting - Birgðafærslur** er keyrð er virði allrar tengdrar birgðarminnkunar uppfærð í samræmi við það.  

## <a name="see-also"></a>Sjá einnig  
 [Hönnunarupplýsingar: Birgðakostnaður](design-details-inventory-costing.md)   
 [Hönnunarupplýsingar: Frávik](design-details-variance.md) [Birgðakostnaði stjórnað](finance-manage-inventory-costs.md)  
 [Fjármál](finance.md)  
 [Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]