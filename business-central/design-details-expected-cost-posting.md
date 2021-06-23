---
title: Hönnunarupplýsingar - Væntanleg kostnaðarbókun | Microsoft Docs
description: Áætlaður kostnaður stendur til dæmis fyrir kostnað keyptrar vöru sem skráð var áður en reikningur fyrir vörunni var móttekinn.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/08/2021
ms.author: edupont
ms.openlocfilehash: 181b0168dc73aba7bb4d09b7cda7a2ce7028e142
ms.sourcegitcommit: 0953171d39e1232a7c126142d68cac858234a20e
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/09/2021
ms.locfileid: "6215279"
---
# <a name="design-details-expected-cost-posting"></a>Hönnunarupplýsingar: Væntanlegur kostnaðarfærsla
Áætlaður kostnaður stendur til dæmis fyrir kostnað keyptrar vöru sem skráð var áður en reikningur fyrir vörunni var móttekinn.  

 Hægt er að bóka áætlaðan kostnað á birgðir og í fjárhag. Þegar þú bóakr magn sem er aðeins móttekið eða sent en ekki reikningsfært er stofnuð viðrisfærsla með ætluðum kostnaði. Þessi áætlaði kostnaður hefur áhrif á birgðavirðið, en bókast ekki í fjárhag nema kerfið sé sett þannig upp.  

> [!NOTE]  
>  Áætlaður kostnaður er aðeins stýrður fyrir vörufærslur. Áætlaður kostnaður er ekki fyrir óáþreifanlegar færslugerðir á borð við afköst og kostnaðarauka.  

 Ef einungis magnhluti birgðaaukningar hefur verið bókaður breytist birgðavirðið í fjárhag ekki nema gátreiturinn **Væntanleg kostnaðarbókun í fjárhag** hafi verið valinn á síðunni **Uppsetning birgða**. Í því tilviki er áætlaður kostnaður bókaður á bráðabirgðareikninga við móttöku. Eftir að móttaka hefur að fullu verið reikningsfærð eru bráðabirgðareikningarnir mótbókaðir og raunverulegur kostnaður bókaður í birgðareikninginn.  

 Til að styðja afstemmingu og rekjanleika vinnu, reikningsfært virðisfærsla sýnir áætlaðan kostnaðarupphæð sem hefur verið sendur til að jafnvægi á bráðabirgðareikningum.  

## <a name="example"></a>Dæmi  
 Eftirfarandi dæmi sýnir væntanlegan kostnað ef gátreiturinn **Sjálfvirk kostnaðarbókun** og gátreiturinn **Væntanleg kostnaðarbókun í fjárhag** eru valdir á síðunni **Birgðagrunnur**.  

 Innkaupapöntun er bókuð sem móttekin Áætlaður kostnaður er 95,00 SGM.  

 **Virðisfærslur**  

|Bókunardags.|Tegund færslu|Kostnaðarupphæð (væntanl.)|Væntanl. kostn. bók. í fjárhag|Væntanl. kostnaður|Birgðafærslunr.|Færslunr.|  
|------------------|----------------|------------------------------|----------------------------------|-------------------|---------------------------|---------------|  
|01-01-20|Beinn kostnaður|95,00|95,00|Já|1|1|  

 **TengslaFærslur í  tengslatöflu fjárhagsbirgðabók**  

|Fjárhagsfærslunr.|Virðisfærslunr.|Fjárhagsdagbók nr.|  
|--------------------|---------------------|-----------------------|  
|1|1|1|  
|2|1|1|  

 **Fjárhagsfærslur**  

|Bókunardags.|Fjárhagsreikningur|Reikningur nr. (En-US sýnishorn)|Upphæð|Færslunr.|  
|------------------|------------------|---------------------------------|------------|---------------|  
|01-01-20|Reikningur áfallinna gjalda birgða (tímab.)|5530|-95,00|2|  
|01-01-20|Reikningur birgða  (bráðab.)|2131|95,00|1|  

 Notandinn bókar innkaupapöntunina á síðari degi samkvæmt reikningi. Reikningsfærður kostnaður er SGM 100,00.  

 **Virðisfærslur**  

|Bókunardags.|Kostnaðarupphæð (raunverul.)|Kostnaðarupphæð (væntanl.)|Kostnaður bókaður í fjárhag|Væntanl. kostnaður|Birgðafærslunr.|Færslunr.|  
|------------------|----------------------------|------------------------------|-------------------------|-------------------|---------------------------|---------------|  
|01-15-20|100,00|-95,00|100,00|Nei|1|2|  

 **TengslaFærslur í  tengslatöflu fjárhagsbirgðabók**  

|Fjárhagsfærslunr.|Virðisfærslunr.|Fjárhagsdagbók nr.|  
|--------------------|---------------------|-----------------------|  
|3|2|2|  
|4|2|2|  
|5|2|2|  
|6|2|2|  

 **Fjárhagsfærslur**  

|Bókunardags.|Fjárhagsreikningur|Reikningur nr. (En-US sýnishorn)|Upphæð|Færslunr.|  
|------------------|------------------|---------------------------------|------------|---------------|  
|01-15-20|Reikningur áfallinna gjalda birgða (tímab.)|5530|95,00|4|  
|01-15-20|Reikningur birgða  (bráðab.)|2131|-95,00|3|  
|01-15-20|Jöfnunareikn. beins kostnaðar|7291|-100|6|  
|01-15-20|Reikningur birgða|2130|100|5|  

## <a name="see-also"></a>Sjá einnig
 [Hönnunarupplýsingar: Birgðakostnaður](design-details-inventory-costing.md)   
 [Hönnunarupplýsingar: Kostnaðarleiðrétting](design-details-cost-adjustment.md)   
 [Hönnunarupplýsingar: afstemming í fjárhagur](design-details-reconciliation-with-the-general-ledger.md)   
 [Hönnunarupplýsingar: Birgðabókun](design-details-inventory-posting.md)   
 [Hönnunarupplýsingar Frávik](design-details-variance.md)  
 [Birgðakostnaði stjórnað](finance-manage-inventory-costs.md)  
 [Fjármál](finance.md)  
 [Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]