---
title: Tilfallukkagreining á sjálfbærnigögnum
description: Fræðast um hvernig á að nota gagnagreiningarhaminn til að greina sjálfbærnigögn.
author: brentholtorf
ms.author: kepontop
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'bi, power BI, analysis, KPI, sustainability, ESG'
ms.search.form: '6220,'
ms.date: 06/12/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# Tilfallukkagreining á sjálfbærnigögnum

Þessi grein útskýrir hvernig á að nota aðgerðina **Gagnagreining** til að greina sjálfbærnigögn beint frá listasíðum og fyrirspurnum. Ekki þarf að keyra skýrslu eða skipta yfir í annað forrit, t.d. Excel. Eiginleikinn býður upp á gagnvirka og fjölhæfa leið til að reikna út, taka saman og skoða gögn. Í stað þess að keyra skýrslur með valkostum og afmörkunum er hægt að bæta við mörgum flipum sem tákna mismunandi verk eða yfirlit á gögnunum. Sum dæmi eru "Útblástursyfirlit" eða "Útblástur eftir umfangi" eða öll önnur sjónarmið sem hægt er að ímynda sér. Til að fræðast meira um notkun aðgerðarinnar **Gagnagreining** er farið í [Greiningarlista og fyrirspurnargögn með greiningarstillingu](analysis-mode.md).

Eftirfarandi listasíður eru notaðar til að gera tilfalvarar greiningar á gögnum um sjálfbærni:

- [Sjálfbærnifærslur](https://businesscentral.dynamics.com/?page=6220)

## Tilföng til sjálfbærni greiningar

Aðgerðin **Gagnagreining** er notuð til að gera skyndiathugun og tilfalalengdar greiningar:

- Ef ekki á að keyra skýrslu.
- Ef skýrsla vegna sérstakra þarfa er ekki til.
- Ef þú vilt ítreka á fljótlegan hátt til að fá góða yfirsýn yfir hluta af fyrirtækinu þínu.

Í eftirfarandi köflum eru dæmi um sjálfbærni í [!INCLUDE [prod_short](includes/prod_short.md)].

| Svæðarit | Til... | Opna þessa síðu í greiningarstillingu | Þessir reitir notaðir |
| ---- | ----- | ------------------------------- |------------------- |
| [Útblástursyfirlit (samtala eftir tegund)](#example-emission-overview-sum-by-category) | Greina útblástur eftir flokki. | [Sjálfbærnifærslur](https://businesscentral.dynamics.com/?page=6220) | **Reikningsflokkur**, **Reikningsheiti**, **Útblástur NH4**, **Útblástur CO2** og **Útblástur N2O**.|
| [Meðalútstreymi eftir tegundum](#example-average-emissions-by-category) | Greina meðallosun eftir flokki. | [Sjálfbærnifærslur](https://businesscentral.dynamics.com/?page=6220) | **Reikningsflokkur**, **Reikningsheiti**, **Útblástur NH4**, **Útblástur CO2** og **Útblástur N2O**.|
| [Losun eftir umfangi](#example-emissions-by-scope) | Greina útblástur eftir umfangi. | [Sjálfbærnifærslur](https://businesscentral.dynamics.com/?page=6220) | **Útblásturssvið**, **Reikningsflokkur**, **Útblástur NH4**, **Útblástur CO2** og **Útblástur N2O**.|

## Dæmi: Útblástursyfirlit (summa eftir tegund)

Til að greina losun eftir flokki skal fylgja eftirfarandi skrefum:

1. Opna síðuna [Sjálfbærnifærslur](https://businesscentral.dynamics.com/?page=6220) og kveikja á greiningarstillingu.
1. Farið er í valmyndina **Dálkar** og allir dálkar fjarlægðir (reiturinn næst leitarreitnum **er** valinn).
1. Kveikja á **veltistillingu** (staðsett beint fyrir ofan **leitarreitinn**).
1. Reitirnir **Tegund reiknings** og **Heiti** reiknings eru dregnir í **línuflokkasvæðið** . Reitirnir eru dregnir í þeirri röð.
1. Dragðu reitina Útblástur NH4, Útblástur CO2 **og** Losun N2O **til gildi svæðisins** **.**  **·** 
1. Endurnefna greiningarflipa til yfirlits **losunar (summu)** eða eitthvað sem lýsir þessari greiningu.

Eftirfarandi mynd sýnir niðurstöður þessara skrefa.

:::image type="content" source="media/data-analysis-sustainability-entries.png" alt-text="Dæmi 1 um gagnagreiningu á síðunni Sjálfbærnifærslur." lightbox="media/data-analysis-sustainability-entries.png":::

## Dæmi: Meðalútstreymi eftir tegundum

Til að greina meðalútstreymi eftir flokki skal fylgja eftirfarandi skrefum:

1. Opna síðuna [Sjálfbærnifærslur](https://businesscentral.dynamics.com/?page=6220) og kveikja á greiningarstillingu.
1. Farið er í valmyndina **Dálkar** og allir dálkar fjarlægðir (reiturinn næst leitarreitnum **er** valinn).
1. Kveikja á **veltistillingu** (staðsett beint fyrir ofan **leitarreitinn**).
1. Reitirnir **Tegund reiknings** og **Heiti** reiknings eru dregnir í **línuflokkasvæðið** . Reitirnir eru dregnir í þeirri röð.
1. Dragðu reitina Útblástur NH4, Útblástur CO2 **og** Losun N2O **til gildi svæðisins** **.**  **·** 
1. Fyrir hvern reit á **svæðinu Gildi** skal velja þá og breyta uppsöfnunaraðgerðinni í `Average`.
1. Endurnefna greiningarflipa til **yfirlits útblásturs (avg)** eða eitthvað sem lýsir þessari greiningu.

Eftirfarandi mynd sýnir niðurstöður þessara skrefa.

:::image type="content" source="media/data-analysis-sustainability-entries-avg.png" alt-text="Dæmi 2 um gagnagreiningu á síðunni Sjálfbærnifærslur." lightbox="media/data-analysis-sustainability-entries-avg.png":::

## Dæmi: Losun eftir umfangi

Til að greina losun eftir umfangi skal fylgja eftirfarandi skrefum:

1. Opna síðuna [Sjálfbærnifærslur](https://businesscentral.dynamics.com/?page=6220) og kveikja á greiningarstillingu.
1. Farið er í valmyndina **Dálkar** og allir dálkar fjarlægðir (reiturinn næst leitarreitnum **er** valinn).
1. Kveikja á **veltistillingu** (staðsett beint fyrir ofan **leitarreitinn**).
1. Reitirnir Útblásturssvið **og** Reikningsflokkur **eru dregnir í** svæðið **Línuflokkar** . Reitirnir eru dregnir í þeirri röð.
1. Dragðu reitina Útblástur NH4, Útblástur CO2 **og** Losun N2O **til gildi svæðisins** **.**  **·** 
1. Endurnefna greiningarflipa til yfirlits **um losun eftir umfangi** eða einhverju sem lýsir þessari greiningu.

Eftirfarandi mynd sýnir niðurstöður þessara skrefa.

:::image type="content" source="media/data-analysis-sustainability-entries-scope.png" alt-text="Dæmi 3 um gagnagreiningu á síðunni Sjálfbærnifærslur." lightbox="media/data-analysis-sustainability-entries-scope.png":::

## Gagnagrunnur fyrir tilfalvarna greiningu á sjálfbærni

Upplýsingarnar sem færðar eru inn í sjálfbærnibók eru til bráðabirgða og hægt er að breyta þeim meðan það er í bókinni. Þegar sjálfbærnibók er bókuð eru upplýsingarnar fluttar í sjálfbærnibókarfærslur um einstaka sjálfbærnireikninga þar sem ekki er hægt að breyta henni. Hins vegar er hægt að bóka bakfærslu eða leiðréttingu færslna. Listasíðan [Sjálfbærnibókarfærslur](https://businesscentral.dynamics.com/?page=6220) er helsti gagnagjafi til augljósrar greiningar á sjálfbærnigögnum.

Til að fræðast meira um bókun sjálfbærnifærslna er farið í [Skrá sjálfbærnifærslur](finance-sustainability-journal.md).

## Sjá einnig .

[Skrá sjálfbærnifærslur](finance-sustainability-journal.md)  
[Innbyggðar sjálfbærniskýrslur](sustainability-reports.md)   
[Yfirlit yfir greiningar, viðskiptagreind og skýrslur](reports-bi-reporting.md)  
[Yfirlit yfir sjálfbærnistjórnun](finance-manage-sustainability.md)   
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  

[!INCLUDE[footer-include](includes/footer-banner.md)]
