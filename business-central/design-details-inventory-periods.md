---
title: Hönnunarupplýsingar - birgðahaldstími
description: Birgðahaldstíma má nota til að forðast vandamál varðandi stöður og birgðaverðmat með því að opna eða loka birgðahaldstímum til að takmarka bókanir á tilteknu tímabili.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 06/15/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
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

[Hönnunarupplýsingar: Birgðakostnaður](design-details-inventory-costing.md)  
[Birgðakostnaði stjórnað](finance-manage-inventory-costs.md)  
[Fjármál](finance.md)  
[Unnið með Business Central](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
