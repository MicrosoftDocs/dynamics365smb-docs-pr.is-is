---
title: Hönnunarupplýsingar - Væntanleg kostnaðarfærsla
description: Áætlaður kostnaður stendur til dæmis fyrir kostnað keyptrar vöru sem skráð var áður en reikningur fyrir vörunni var móttekinn.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 07/20/2021
ms.author: edupont
ms.openlocfilehash: c2c3e7cd0e9f5ae88e63bd305927a20341e7559b
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2022
ms.locfileid: "8513097"
---
# <a name="design-details-expected-cost-posting"></a>Hönnunarupplýsingar: Væntanlegur kostnaðarfærsla
Áætlaður kostnaður stendur til dæmis fyrir kostnað keyptrar vöru sem skráð var áður en reikningur fyrir vörunni var móttekinn.  

 Hægt er að bóka áætlaðan kostnað á birgðir og í fjárhag. Þegar þú bóakr magn sem er aðeins móttekið eða sent en ekki reikningsfært er stofnuð viðrisfærsla með ætluðum kostnaði. Þessi áætlaði kostnaður hefur áhrif á birgðavirðið, en bókast ekki í fjárhag nema kerfið sé sett þannig upp.  

> [!NOTE]  
>  Áætlaður kostnaður er aðeins stýrður fyrir vörufærslur. Áætlaður kostnaður er ekki fyrir óáþreifanlegar færslugerðir á borð við afköst og kostnaðarauka.  

 Ef einungis magnhluti birgðaaukningar hefur verið bókaður breytist birgðavirðið í fjárhag ekki nema gátreiturinn **Væntanleg kostnaðarbókun í fjárhag** hafi verið valinn á síðunni **Uppsetning birgða**. Í því tilviki er áætlaður kostnaður bókaður á bráðabirgðareikninga við móttöku. Eftir að móttaka hefur að fullu verið reikningsfærð eru bráðabirgðareikningarnir mótbókaðir og raunverulegur kostnaður bókaður í birgðareikninginn.  

 Til að styðja afstemmingu og rekjanleika vinnu, reikningsfært virðisfærsla sýnir áætlaðan kostnaðarupphæð sem hefur verið sendur til að jafnvægi á bráðabirgðareikningum.  

## <a name="prerequisites-for-posting-expected-costs"></a>Skilyrði fyrir bókun væntanlegs kostnaðar

Til að gera mögulegt að bóka væntanlegan kostnað þarftu að gera eftirfarandi:
1. Á síðunni **Uppsetning birgða** skal velja **Sjálfvirka kostnaðarbókun** og gátreitinn **Væntanleg kostnaðarbókun í fjárhag**.
2. Setja upp hvaða bráðabirgðareikninga þú átt að nota fyrir bókunarferli væntanlegs kostnaðar.  

  Á síðunni **Uppsetning birgðabókunar** skaltu staðfesta reitina **Birgðareikningur** og **Birgðareikningur (bráðabirgða)** fyrir **Staðsetningarkóða og kóða birgðabókunarflokks** fyrir vöruna sem á að kaupa. Til að fá nánari upplýsingar um þessa reikninga skal fara í [Hönnunarupplýsingar - reikningar í fjárhag](design-details-accounts-in-the-general-ledger.md).
3. Á síðunni **Almennur bókunargrunnur** skal staðfesta reitinn **Uppsöfnunarreikningur birgða (bráðabirgða)** fyrir **Almennan viðskiptabókunarflokk** og **Almennan vörubókunarflokk** sem ætlunin er að nota.
4. Þegar þú stofnar innkaupapöntun er sjálfgefið að reiturinn **Reikningsnr. lánardrottins** sé áskilinn. Þú þarft að slökkva á því á síðunni **Uppsetning innkaupagrunns** með því að afvelja reitinn **Nr. utanaðk. skjals áskilið**.

## <a name="example"></a>Dæmi  

> [!NOTE]  
> Reikningsnúmerin sem notuð eru í þessu dæmi eru aðeins til viðmiðunar og verða önnur í kerfinu. Settu þau upp samkvæmt leiðbeiningum í skilyrðum hér að ofan.

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

|Bókunardagsetning|Fjárhagur|Lykilnr. (eingöngu dæmi!)|Upphæð|Færslunr.|  
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
 [Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
