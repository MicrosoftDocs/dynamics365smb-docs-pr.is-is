---
title: Hönnunarupplýsingar - Væntanleg kostnaðarfærsla
description: Áætlaður kostnaður stendur til dæmis fyrir kostnað keyptrar vöru sem skráð var áður en reikningur fyrir vörunni var móttekinn.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 07/20/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# Hönnunarupplýsingar: Væntanlegur kostnaðarfærsla
Áætlaður kostnaður stendur til dæmis fyrir kostnað keyptrar vöru sem skráð var áður en reikningur fyrir vörunni var móttekinn.  

 Hægt er að bóka áætlaðan kostnað á birgðir og í fjárhag. Þegar þú bóakr magn sem er aðeins móttekið eða sent en ekki reikningsfært er stofnuð viðrisfærsla með ætluðum kostnaði. Þessi áætlaði kostnaður hefur áhrif á birgðavirðið, en bókast ekki í fjárhag nema kerfið sé sett þannig upp.  

> [!NOTE]  
>  Áætlaður kostnaður er aðeins stýrður fyrir vörufærslur. Áætlaður kostnaður er ekki fyrir óáþreifanlegar færslugerðir á borð við afköst og kostnaðarauka.  

 Ef einungis magnhluti birgðaaukningar hefur verið bókaður breytist birgðavirðið í fjárhag ekki nema gátreiturinn **Væntanleg kostnaðarbókun í fjárhag** hafi verið valinn á síðunni **Uppsetning birgða**. Í því tilviki er áætlaður kostnaður bókaður á bráðabirgðareikninga við móttöku. Eftir að móttaka hefur að fullu verið reikningsfærð eru bráðabirgðareikningarnir mótbókaðir og raunverulegur kostnaður bókaður í birgðareikninginn.  

 Til að styðja afstemmingu og rekjanleika vinnu, reikningsfært virðisfærsla sýnir áætlaðan kostnaðarupphæð sem hefur verið sendur til að jafnvægi á bráðabirgðareikningum.  

## Skilyrði fyrir bókun væntanlegs kostnaðar

Til að gera mögulegt að bóka væntanlegan kostnað þarftu að gera eftirfarandi:
1. Á síðunni **Uppsetning birgða** skal velja **Sjálfvirka kostnaðarbókun** og gátreitinn **Væntanleg kostnaðarbókun í fjárhag**.
2. Setja upp hvaða bráðabirgðareikninga þú átt að nota fyrir bókunarferli væntanlegs kostnaðar.  

  Á síðunni **Uppsetning birgðabókunar** skaltu staðfesta reitina **Birgðareikningur** og **Birgðareikningur (bráðabirgða)** fyrir **Staðsetningarkóða og kóða birgðabókunarflokks** fyrir vöruna sem á að kaupa. Til að fá nánari upplýsingar um þessa reikninga skal fara í [Hönnunarupplýsingar - reikningar í fjárhag](design-details-accounts-in-the-general-ledger.md).
3. Á síðunni **Almennur bókunargrunnur** skal staðfesta reitinn **Uppsöfnunarreikningur birgða (bráðabirgða)** fyrir **Almennan viðskiptabókunarflokk** og **Almennan vörubókunarflokk** sem ætlunin er að nota.
4. Þegar þú stofnar innkaupapöntun er sjálfgefið að reiturinn **Reikningsnr. lánardrottins** sé áskilinn. Þú þarft að slökkva á því á síðunni **Uppsetning innkaupagrunns** með því að afvelja reitinn **Nr. utanaðk. skjals áskilið**.

## Dæmi  

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

## Sjá einnig
 [Hönnunarupplýsingar: Birgðakostnaður](design-details-inventory-costing.md)   
 [Hönnunarupplýsingar: Kostnaðarleiðrétting](design-details-cost-adjustment.md)   
 [Hönnunarupplýsingar: afstemming í fjárhagur](design-details-reconciliation-with-the-general-ledger.md)   
 [Hönnunarupplýsingar: Birgðabókun](design-details-inventory-posting.md)   
 [Hönnunarupplýsingar Frávik](design-details-variance.md)  
 [Birgðakostnaði stjórnað](finance-manage-inventory-costs.md)  
 [Fjármál](finance.md)  
 [Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
