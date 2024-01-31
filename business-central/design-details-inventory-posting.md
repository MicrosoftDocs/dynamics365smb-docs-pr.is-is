---
title: Hönnunarupplýsingar - Birgðabókun | Microsoft Docs
description: 'Hver birgðafærsla, svo sem innkaupakvittun eða sölusending bókar tvær færslur af mismunandi gerðum.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/08/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Hönnunarupplýsingar: birgðabókun

Hver birgðafærsla, svo sem innkaupakvittun eða sölusending bókar tvær færslur af mismunandi gerðum.  

|Tegund færslu|Description|  
|----------|-----------|  
|Magn|Endurspeglar breytingu á magni í birgðum. Þessar upplýsingar eru geymdar í birgðafærslum.<br /><br /> Með birgðajöfnunarfærslum.|  
|Gildi|Endurspeglar breytingu á birgðavirði. Þessar upplýsingar eru geymdar í virðisfærslum.<br /><br /> Ein virðisfærsla eða fleiri eru til fyrir hverja birgðafærslu eða afkastahöfuðbókarfærslu.<br /><br /> Upplýsingar um afkastagildisfærslur sem tengjast notkun framleiðslu- eða samsetningartilfanga eru í [Hönnunarupplýsingar: Bókun framleiðslupöntunar](design-details-production-order-posting.md).|  

 Hvað varðar magnbókun eru til vörujöfnunarfærslur til að tengja birgðaaukningu við birgðaminnkun. Þetta gerir kostnaðarforritinu kleift að framsenda kostnað frá aukningu á tengda minnkun, og öfugt. Nánari upplýsingar eru í [Upplýsingar um hönnun: Vörujöfnun](design-details-item-application.md).  

 Birgðahöfuðbókarfærslur, virðisfærslur og vörujöfnunarfærslur eru stofnaðar vegna bókunar í birgðabókarlínu, annað óbeint með bókun í pöntunarlínu eða beint á síðunni Birgðabók.  

 Með reglulegu millibili virðisfærslur sem eru stofna í birgðarfjárhag eru eru bókaðar í fjárhagur til að afstemma fjárhagur vegna fjárhagsástæðna Frekari upplýsingar, sjá [Hönnunarupplýsingar: afstemming við fjárhaginn](design-details-reconciliation-with-the-general-ledger.md)  

 ![Færsluflæði þegar birgðir eru stemmdar af við fjárhag.](media/design_details_inventory_costing_1_entry_flow.png "Færsluflæði þegar sætt er saman við fjárhag")  

## Dæmi

Eftirfarandi dæmi sýnir hvernig vörubókarfærslur, virðisfærslur og vörujöfnunarfærslur mynda fjárhagsfærslur.  

 Innkaupapöntun er bókuð sem móttekin og reikningsfærð fyrir 10 vörur með beinum einingarkostnaði sem nemur SGM 7 og sameiginlegum kostnaði sem nemur SGM 1. Bókunardagsetningin er 01-01-20. Eftirfarandi færslur eru stofnaðar.  

### Birgðafærslur (1)

|Bókunardagsetning|Tegund færslu|Kostnaðarupphæð (raunverul.)|Magn|Færslunr.|  
|------------|----------|--------------------|--------|---------|  
|01-01-20|Innkaup|80,00|10|1|  

### Virðisfærslur (1)

|Bókunardagsetning|Tegund færslu|Kostnaðarupphæð (raunverul.)|Birgðafærsla nr.|Færslunr.|  
|------------|----------|--------------------|---------------------|---------|  
|01-01-20|Beinn kostnaður|70,00|1|1|  
|01-01-20|Óbeinn kostnaður|10,00|1|2|  

### Birgðajöfnunarfærslur (1)

|Færslunr.|Birgðafærsla nr.|Birgðafærslunr. vöru á innleið|Birgðafærslunr. vöru á útleið|Magn|  
|---------|---------------------|----------------------|-----------------------|--------|  
|1|1|1|0|10|  

 Næst er bókuð sala 10 eininga vörunnar með bókunardagsetningunni 01-15-20.  

### Birgðafærslur (2)

|Bókunardagsetning|Tegund færslu|Kostnaðarupphæð (raunverul.)|Magn|Færslunr.|  
|------------|----------|--------------------|--------|---------|  
|01-15-20|Sala|-80,00|-10|2|  

### Virðisfærslur (2)

|Bókunardagsetning|Tegund færslu|Kostnaðarupphæð (raunverul.)|Birgðafærsla nr.|Færslunr.|  
|------------|----------|--------------------|---------------------|---------|  
|01-15-20|Beinn kostnaður|-80,00|2|3|  

### Birgðajöfnunarfærslur (2)

|Færslunr.|Birgðafærsla nr.|Birgðafærslunr. vöru á innleið.|Birgðafærslunr. vöru á útleið.|Magn|  
|---------|---------------------|----------------------|-----------------------|--------|  
|2|2|1|2|-10|  

Að lokum bókhaldstímabils, skaltu keyra runuvinnslurnar **Bóka birgðakostnað í fjárhag** til að afstemma þessar birgðafærslur við fjárhaginn.  

 Frekari upplýsingar, sjá [Hönnunarupplýsingar: reikningar í fjárhagur](design-details-accounts-in-the-general-ledger.md)  

 Eftirfarandi töflur sýna niðurstöður afstemmingar birgðafærsla í þessu dæmi við fjárhag.  

### Virðisfærslur (3)  

|Bókunardagsetning|Tegund færslu|Kostnaðarupphæð (raunverul.)|Kostnaður bókaður í fjárhag|Birgðafærslunr.|Færslunr.|  
|------------|----------|--------------------|------------------|---------------------|---------|  
|01-01-20|Beinn kostnaður|70,00|70,00|1|1|  
|01-01-20|Óbeinn kostnaður|10,00|10,00|1|2|  
|01-15-20|Beinn kostnaður|-80,00|-80,00|2|3|  

### Fjárhagsfærslur (3)

|Bókunardagsetning|Fjárhagur|Reikningur nr. (En-US sýnishorn)|Upphæð|Færslunr.|  
|------------|-----------|------------------------|------|---------|  
|01-01-20|[Reikningur birgða]|2130|70,00|1|  
|01-01-20|[Jöfnunareikn. beins kostnaðar]|7291|-70,00|2|  
|01-01-20|[Reikningur birgða]|2130|10,00|3|  
|01-01-07|[Jöfnunarreikn. sam. kostn.]|7292|-10,00|4|  
|01-15-20|[Reikningur birgða]|2130|-80,00|5|  
|01-15-20|[Kostnaður seldra vara]|7290|80,00|6|  

> [!NOTE]  
> Bókunardagsetning fjárhagsfærslnanna er sú sama og fyrir tengdar virðisfærslur.  
> 
> Reiturinn **Bókaður kostnaður í fjárhag** í töflunni **Virðisfærsla** er útfylltur.  

 Tengslin milli virðisfærslna og fjárhagsfærslna eru geymd í töflunni **Fjárhagur - Birgðahöfuðbók tengls**.  

### Tengslafærslur í fjárhag - tengslatafla fjárhagsbirgðabókar (3)

|Fjárhagsfærslunr.|Virðisfærslunr.|Fjárhagsdagbók nr.|  
|-------------|---------------|----------------|  
|1|1|1|  
|2|1|1|  
|3|2|1|  
|4|2|1|  
|5|3|1|  
|6|3|1|  

## Samsetning og framleiðslubókun

Afkasta- og forðafærslur endurspegla tímann sem er bókaður sem notaður í vöru eða samsetningu. Þessi framleiðslukostnaður er bókaður sem virðisfærslur í fjárhag ásamt tengdum efniskostnaði í svipaðri uppsetningu og lýst er fyrir færslur í birgðahöfuðbók í þessu efnisatriði.  

Frekari upplýsingar, sjá [Hönnunarupplýsingar: bókun samsetningarpöntunar](design-details-assembly-order-posting.md).  

## Sjá einnig

 [Hönnunarupplýsingar: Birgðakostnaður](design-details-inventory-costing.md)  
 [Hönnunarupplýsingar: reikningar í fjárhagur](design-details-accounts-in-the-general-ledger.md)  
 [Hönnunarupplýsingar: kostnaðaríhlutir](design-details-cost-components.md) [Stjórna birgðakostnaði](finance-manage-inventory-costs.md)  
 [Fjármál](finance.md)  
 [Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]