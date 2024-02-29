---
title: Hönnunarupplýsingar - Reikningar í fjárhagnum | Microsoft Docs
description: Til að afstemma birgðir og afkastahöfuðbókarfærslur við fjárhag eru tengdar virðisfærslur bókaðar á mismunandi reikninga í fjárhag.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bnielse
ms.topic: conceptual
ms.search.keywords: null
ms.date: 02/20/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# <a name="design-details-accounts-in-the-general-ledger"></a>Hönnunarupplýsingar: reikningar í fjárhag

Til að afstemma birgðir og afkastahöfuðbókarfærslur við fjárhag eru tengdar virðisfærslur bókaðar á mismunandi reikninga í fjárhag. Frekari upplýsingar, sjá [Hönnunarupplýsingar: afstemming við fjárhaginn](design-details-reconciliation-with-the-general-ledger.md)  

## <a name="from-the-inventory-ledger"></a>Úr fjárhag birgða

Eftirfarandi tafla sýnir sambandið milli mismunandi gerða birgðavirðisfærsla og reikninga og mótreikninga í fjárhag.  

|**Tegund birgðafærslu**|**Tegund virðisfærslu**|**Tegund fráviks**|**Væntanl. kostnaður**|**Reikningur**|**Mótreikningur**|  
|--------------------------------|--------------------------|-----------------------|-----------------------|-----------------|---------------------------|  
|Innkaup|Beinn kostnaður||Já|Birgðir (bráðab.)|Birgðaleiðr.reikn. (bráðab.)|  
|Innkaup|Beinn kostnaður||Nr.|Birgðir|Beinn kostnaður jafnaður|  
|Innkaup|Óbeinn kostnaður||Nr.|Birgðir|Sameiginl. kostnaður jafnaður|  
|Innkaup|Frávik|Innkaup|Nr.|Birgðir|Frávik í innkaupum|  
|Innkaup|Endurmat||Nr.|Birgðir|Birgðaleiðr.|  
|Innkaup|Sléttun||Nr.|Birgðir|Birgðaleiðr.|  
|Sala|Beinn kostnaður||Já|Birgðir (bráðab.)|KSV (bráðab.)|  
|Sala|Beinn kostnaður||Nr.|Birgðir|KSV|  
|Sala|Endurmat||Nr.|Birgðir|Birgðaleiðr.|  
|Sala|Sléttun||Nr.|Birgðir|Birgðaleiðr.|  
|Aukning, minnkun, millifærsla|Beinn kostnaður||Nr.|Birgðir|Birgðaleiðr.|  
|Aukning, minnkun, millifærsla|Endurmat||Nr.|Birgðir|Birgðaleiðr.|  
|Aukning, minnkun, millifærsla|Sléttun||Nr.|Birgðir|Birgðaleiðr.|  
|(Framleiðsla) Notkun|Beinn kostnaður||Nr.|Birgðir|VÍV|  
|(Framleiðsla) Notkun|Endurmat||Nr.|Birgðir|Birgðaleiðr.|  
|(Framleiðsla) Notkun|Sléttun||Nr.|Birgðir|Birgðaleiðr.|  
|Samsetningarnotkun|Beinn kostnaður||Nr.|Birgðir|Birgðaleiðr.|  
|Samsetningarnotkun|Beinn kostnaður||Nr.|Beinn kostnaður jafnaður|Birgðaleiðr.|  
|Samsetningarnotkun|Óbeinn kostnaður||Nr.|Sameiginl. kostnaður jafnaður|Birgðaleiðr.|  
|(Framleiðslu)frálag|Beinn kostnaður||Já|Birgðir (bráðab.)|VÍV|  
|(Framleiðslu)frálag|Beinn kostnaður||Nr.|Birgðir|VÍV|  
|(Framleiðslu)frálag|Óbeinn kostnaður||Nr.|Birgðir|Sameiginl. kostnaður jafnaður|  
|(Framleiðslu)frálag|Frávik|Efni|Nr.|Birgðir|Hráefnisfrávik|  
|(Framleiðslu)frálag|Frávik|Geta|Nr.|Birgðir|Getufrávik|  
|(Framleiðslu)frálag|Frávik|Undirverktaka|Nr.|Birgðir|Frávik undirverktaka|  
|(Framleiðslu)frálag|Frávik|Sameiginlegur kostnaður afkastagetu|Nr.|Birgðir|Frávik í sam. kostn.|  
|(Framleiðslu)frálag|Frávik|Sameiginl. kostn. framleiðslu|Nr.|Birgðir|Sam. frl.kostn. frávik|  
|(Framleiðslu)frálag|Endurmat||Nr.|Birgðir|Birgðaleiðr.|  
|(Framleiðslu)frálag|Sléttun||Nr.|Birgðir|Birgðaleiðr.|  
|Samsetningarfrálag|Beinn kostnaður||Nr.|Birgðir|Birgðaleiðr.|  
|Samsetningarfrálag|Endurmat||Nr.|Birgðir|Birgðaleiðr.|  
|Samsetningarfrálag|Óbeinn kostnaður||Nr.|Birgðir|Sameiginl. kostnaður jafnaður|  
|Samsetningarfrálag|Frávik|Efni|Nr.|Birgðir|Hráefnisfrávik|  
|Samsetningarfrálag|Frávik|Geta|Nr.|Birgðir|Getufrávik|  
|Samsetningarfrálag|Frávik|Sameiginlegur kostnaður afkastagetu|Nr.|Birgðir|Frávik í sam. kostn.|  
|Samsetningarfrálag|Frávik|Sameiginl. kostn. framleiðslu|Nr.|Birgðir|Sam. frl.kostn. frávik|  
|Samsetningarfrálag|Sléttun||Nr.|Birgðir|Birgðaleiðr.|  

## <a name="from-the-capacity-ledger"></a>Úr Afkastabók

 Eftirfarandi tafla sýnir sambandið milli mismunandi gerða afkastavirðisfærsla og reikninga og mótreikninga í fjárhag. Færslur í afkastahöfuðbók tákna vinnuafl neytt í samsetningu eða framleiðslu.  

|**Tegund vinnu**|**Afkastagetufærslugerð**|**Tegund virðisfærslu**|**Reikningur**|**Mótreikningur**|  
|-------------------|------------------------------------|--------------------------|-----------------|---------------------------|  
|Samsetning|Forði|Beinn kostnaður|Beinn kostnaður jafnaður|Birgðaleiðr.|  
|Samsetning|Forði|Óbeinn kostnaður|Sameiginl. kostnaður jafnaður|Birgðaleiðr.|  
|Framleiðsla|Vélastöð/vinnustöð|Beinn kostnaður|Reikningur VÍV|Beinn kostnaður jafnaður|  
|Framleiðsla|Vélastöð/vinnustöð|Óbeinn kostnaður|Reikningur VÍV|Sameiginl. kostnaður jafnaður|  

## <a name="assembly-costs-are-always-actual"></a>Samsetningarkostnaður er alltaf raunverulegur

 Eins og sést í töflunni hér að ofan eru samsetningarbókanir ekki sýndar í bráðabirgðareikningum. Þetta er vegna þess að hugtakið um verk í vinnslu (VÍV) gildir ekki um bókun samsetningarúttaks, sem er frábrugðið bókun framleiðsluúttaks. Samsetningarkostnaður er aðeins bókaður sem raunverulegur kostnaður, aldrei áætlaður kostnaður.  

 Frekari upplýsingar, sjá [Hönnunarupplýsingar: bókun samsetningarpöntunar](design-details-assembly-order-posting.md).  

## <a name="calculating-the-amount-to-post-to-the-general-ledger"></a>Útreikningur upphæðar sem á að bóka í fjárhag

 Eftirfarandi reitir í töflunni **Gildisfærsla** eru notaðir til að reikna áætlaða kostnaðarupphæð sem er bókuð í fjárhag:  

- Kostnaðarupphæð (raunverul.)  
- Kostnaður bókaður í fjárhag  
- Kostnaðarupphæð (væntanl.)  
- Væntanl. kostn. bók. í fjárhag  

Eftirfarandi tafla sýnir hvernig upphæðirnar sem á að bóka í fjárhag eru reiknaðar fyrir tvær mismunandi kostnaðargerðir.  

|Tegund kostnaðar|Útreikningur|  
|---------------|-----------------|  
|Raunkostnaður|Kostnaðarupphæð (raunverul.). – kostnaður bókaður í fjárhag.|  
|Væntanl. kostnaður|Kostnaðarupphæð (væntanleg)  - Væntanlegur kostnaður bókaður í fjárh.|  

## <a name="see-also"></a>Sjá einnig .

[Hönnunarupplýsingar: Birgðakostnaður](design-details-inventory-costing.md)  
[Hönnunarupplýsingar: birgðabókun](design-details-inventory-posting.md)  
[Hönnunarupplýsingar: Væntanleg kostnaðarfærsla](design-details-expected-cost-posting.md)  
[Birgðakostnaði stjórnað](finance-manage-inventory-costs.md)  
[Fjármál](finance.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
