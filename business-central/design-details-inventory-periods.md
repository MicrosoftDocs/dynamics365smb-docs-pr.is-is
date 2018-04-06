---
title: "Hönnunarupplýsingar - Birgðahaldstími | Microsoft Docs"
description: "Bakfærð færsla eða kostnaðarleiðréttingar hafa oft áhrif á stöðu og birgðaverðmat fyrri reikningstímabil sem teljast lokjuð. Þetta getur haft öfug áhrif á nákvæma skýrslugerð, sérstaklega hjá alþjóðlegum fyrirtækjum. Búnaður birgðahaldstíma má nota til að forðast slíka vandamál, með því að opna eða loka birgðahaldstímum til að takmarka bókanir á tilteknu tímabili."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 99aa0cacdbe6933c5ba16443297d1838b8bfd3ac
ms.contentlocale: is-is
ms.lasthandoff: 03/22/2018

---
# <a name="design-details-inventory-periods"></a>Hönnunarupplýsingar: birgðahaldstími
Bakfærð færsla eða kostnaðarleiðréttingar hafa oft áhrif á stöðu og birgðaverðmat fyrri reikningstímabil sem teljast lokjuð. Þetta getur haft öfug áhrif á nákvæma skýrslugerð, sérstaklega hjá alþjóðlegum fyrirtækjum. Búnaður birgðahaldstíma má nota til að forðast slíka vandamál, með því að opna eða loka birgðahaldstímum til að takmarka bókanir á tilteknu tímabili.  

 Birgðatímabil er tímabil, skilgreint með lokadagsetningu, sem birgðafærslur eru bókaðar innan. Þegar þú lokar birgðahaldstíma er ekki hægt að bóka neinar gildisbreytingar á lokaða tímabilinu. Þetta inniheldur nýjar gildisbókanir, væntanlegar eða reikningsfærðar færslur, breytingar á núverandi gildi og kostnaðarleiðréttingu. Hins vegar getur þú samt notað það á opna birgðafærslu sem lendir á lokaða tímabilinu. Nánari upplýsingar eru í [Upplýsingar um hönnun: Vörujöfnun](design-details-item-application.md).  

 Til að ganga úr skugga um að allar viðskiptifærslur í lokuðu tímabili eru endanlegar, skulu eftirfarandi skilyrði vera uppfyllt áður en birgðahaldstími getur lokað:  

-   Allar birgðahöfuðbókarfærslur á útleið á tímabilinu þurfa að vera lokaðar (ekki neikvæð birgðastaða).  
-   Leiðrétta þarf allan vörukostnað á tímabilinu.  
-   Allar losaðar og loknar framleiðslupantanir á tímabilinu þurfa að vera kostnaðarjafnaðar.  

 Þegar þú lokar birgðahaldstíma er stofnuð birgðahaldstímafærsla með þv´að nota númer síðustu vöruskráningar sem fellur undir birgðahaldstímann. Að auki, er tími, dagsetning, og notandakóði notandans sem lokar tímabilinu eru færðar í birgðahaldstímifærslu. Með því að nota þessar upplýsingar með síðasta skráðri vöru fyrra tímabili, getur þú séð hvaða birgðafærslur voru bókaðar á birgðahaldstími. Það er líka hægt að enduropna birgðahaldstíma ef þú þarft að bóka í lokuðum tímabili. Þegar þú enduropnar birgðahaldstíma er stofnuð birgðahaldstímafærsla.  

## <a name="see-also"></a>Sjá einnig  
 [Hönnunarupplýsingar: Birgðakostnaður](design-details-inventory-costing.md) [Stjórna birgðakostnaði](finance-manage-inventory-costs.md) [Fjármál](finance.md)  
 [Unnið með Financials](ui-work-product.md)

