---
title: Tilfalengin greining á gögnum um eignir
description: Fræðast um notkun gagnagreiningarmáta til að greina eignagögn.
author: kennienp
ms.author: kepontop
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'bi, power BI, analysis, KPI'
ms.search.form: '5604, 20'
ms.date: 05/02/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# <a name="ad-hoc-analysis-of-fixed-assets-data"></a>Tilfalengin greining á gögnum um eignir

Þessi grein útskýrir hvernig á að nota aðgerðina **Gagnagreining** til að greina eignagögn beint frá listasíðum og fyrirspurnum. Ekki þarf að keyra skýrslu eða skipta yfir í annað forrit, t.d. Excel. Eiginleikinn býður upp á gagnvirka og fjölhæfa leið til að reikna út, taka saman og skoða gögn. Í stað þess að keyra skýrslur með valkostum og afmörkunum er hægt að bæta við mörgum flipum sem tákna mismunandi verk eða yfirlit á gögnunum. Sum dæmi eru "Heildareignir" "Afskriftir með tímanum" eða annað sem hægt er að ímynda sér. Til að fræðast meira um notkun aðgerðarinnar **Gagnagreining** er farið í [Greiningarlista og fyrirspurnargögn með greiningarstillingu](analysis-mode.md).

Eftirfarandi listasíður eru notaðar til að hefja greiningu á ferlum eigna:

- [Eignafærslur](https://businesscentral.dynamics.com/?page=5604)
- [Fjárhagsfærslur](https://businesscentral.dynamics.com/?page=20)

## <a name="fixed-assets-ad-hoc-analysis-scenarios"></a>Tilfalengdar greiningaraðstæður eigna

Aðgerðin **Gagnagreining** er notuð til að gera skyndiathugun og tilfalalengdar greiningar:

- Ef ekki á að keyra skýrslu.
- Ef skýrsla vegna sérstakra þarfa er ekki til.
- Ef þú vilt ítreka á fljótlegan hátt til að fá góða yfirsýn yfir hluta af fyrirtækinu þínu.

Eftirfarandi hlutar gefa dæmi um aðstæður eigna í [!INCLUDE [prod_short](includes/prod_short.md)].

| Svæðarit | Til... | Opna þessa síðu í greiningarstillingu | Þessir reitir notaðir |
| ---- | ----- | ------------------------------- |------------------- |
| [Eignir (gildandi virði)](#example-fixed-assets-current-value) | Rekja eignavirði, bæði á öllum eignum og á einni eign. | [Eignafærslur](https://businesscentral.dynamics.com/?page=5604) | **Afskriftabók,Eignanr** **.,** Eignabókunardags **.**, **Eignabókunartegund** og **Upphæð** |
| [Virði eignar breytist með tímanum](#example-asset-value-changes-over-time) | Rekja virði eignar breytist með tímanum. | [Eignafærslur](https://businesscentral.dynamics.com/?page=5604) | **Eignabókunartegund**, **Eignabókunardags.** og **Upphæð** |
|[Eignaafskriftir með tímanum](#example-fixed-asset-depreciations-over-time) | Rekja afskriftir með tímanum, bæði á öllum eignum og einni eign. | [Eignafærslur](https://businesscentral.dynamics.com/?page=5604) | **Afskriftabók**, **Eignanr.**, **Eignabókunarár**, **Eignabókunarmánuður**, **Upphæð** og **Eignabókunartegund** |

### <a name="example-fixed-assets-current-value"></a>Dæmi: núgildandi virði eigna

Til að rekja virði einnar eða fleiri eigna skal fylgja eftirfarandi skrefum:

1. Listinn [Eignafærslur](https://businesscentral.dynamics.com/?page=5604) er opnaður og Færa inn greiningarham valið :::image type="content" source="media/analysis-mode-icon.png" alt-text="."::: Til að kveikja á greiningarstillingu.
1. Farið er í valmyndina **Dálkar** og allir dálkar fjarlægðir (reiturinn er valinn við hliðina **á leitarreitnum** til hægri).
1. Draga á reitina **Afskriftabók** og **Eignanr.**  **að línuflokkasvæðinu** .
1. Velja skal reitina **Eignabókunardags** . og **Eignabókunartegund** .
1. Reiturinn **Upphæð** er dreginn á **svæðið Virði** .
1. Endurnefna greiningarflipa í **yfirlit eigna - virði** eða eitthvað sem lýsir þessari greiningu.

Eftirfarandi mynd sýnir niðurstöður þessara skrefa.

:::image type="content" source="media/data-analysis-fa-ledger-entries-asset-overview-current-value.png" alt-text="Dæmi um hvernig á að gera gagnagreiningu á síðunni Eignafærslur til að sjá virði eignar." lightbox="media/data-analysis-fa-ledger-entries-asset-overview-current-value.png":::

### <a name="example-asset-value-changes-over-time"></a>Dæmi: eignavirði breytist með tímanum

Til að rekja breytingar á virði eigna með tímanum skal fylgja eftirfarandi skrefum:

1. Listinn [Eignafærslur](https://businesscentral.dynamics.com/?page=5604) er opnaður og Færa inn greiningarham valið :::image type="content" source="media/analysis-mode-icon.png" alt-text="."::: Til að kveikja á greiningarstillingu.
1. Farið er í valmyndina **Dálkar** og allir dálkar fjarlægðir (reiturinn er valinn við hliðina **á leitarreitnum** til hægri).
1. Kveikja á **veltihamsvíkkuninni** (sem staðsett er fyrir ofan **leitarreitinn** hægra megin).
1. Reiturinn **Eignabókunartegund** er dreginn að reitnum **Línuflokkar** .
1. Reitirnir Eignabókunarár og Eignabókunarmánuður **eru dregnir í reitina Dálklímmiðar** . **·**  **·** 
1. Reiturinn **Upphæð** er dreginn á **svæðið Virði** .
1. Endurnefna greiningarflipann við **virði eigna breytist með tímanum** eða eitthvað sem lýsir þessari greiningu.

Eftirfarandi mynd sýnir niðurstöður þessara skrefa.

:::image type="content" source="media/data-analysis-fa-ledger-entries-asset-changes-over-time.png" alt-text="Dæmi um hvernig á að gera gagnagreiningu á síðunni Eignafærslur til að sjá virðisbreytingar eigna með tímanum." lightbox="media/data-analysis-fa-ledger-entries-asset-changes-over-time.png":::

### <a name="example-fixed-asset-depreciations-over-time"></a>Dæmi: eignaafskriftir með tímanum

Til að rekja afskriftir fyrir eina eða fleiri eignir skal fylgja eftirfarandi skrefum:

1. Listinn [Eignafærslur](https://businesscentral.dynamics.com/?page=5604) er opnaður og Færa inn greiningarham valið :::image type="content" source="media/analysis-mode-icon.png" alt-text="."::: Til að kveikja á greiningarstillingu.
1. Farið er í valmyndina **Dálkar** og allir dálkar fjarlægðir (reiturinn er valinn við hliðina **á leitarreitnum** til hægri).
1. Kveikja á **veltihamsvíkkuninni** (sem staðsett er fyrir ofan **leitarreitinn** hægra megin).
1. Draga á reitina **Afskriftabók** og **Eignanr.**  **að línuflokkasvæðinu** .
1. Reitirnir Eignabókunarár og Eignabókunarmánuður **eru dregnir í reitina Dálklímmiðar** . **·**  **·** 
1. Reiturinn **Upphæð** er dreginn á **svæðið Virði** .
1. Í reitnum **Eignabókunartegund** er valið **Afskrift**.
1. Endurnefna greiningarflipann við **Afskriftir með tímanum** eða eitthvað sem lýsir þessari greiningu.

Eftirfarandi mynd sýnir niðurstöður þessara skrefa.

:::image type="content" source="media/data-analysis-fa-ledger-entries-depreciation-by-asset.png" alt-text="Dæmi um hvernig á að gera greiningu á gögnum á síðunni Eignafærslur til að sjá afskriftir með tímanum." lightbox="media/data-analysis-fa-ledger-entries-depreciation-by-asset.png":::

## <a name="data-foundation-for-ad-hoc-analysis-on-fixed-assets"></a>Gagnagrunnur fyrir tilfalvarna greiningu á eignum

Þegar eignabækur eru bókaðar [!INCLUDE [prod_short](includes/prod_short.md)]  stofnar notandi færslur í **töflunni Eignafærsla** . Þess vegna er tilfalvarleg greining á eignum gjarnan gerð á síðunni [Eignafærslur](https://businesscentral.dynamics.com/?page=5604) .

## <a name="contributors"></a>Stuðlar

*Microsoft viðheldur þessari grein. Varahlutir dæmisins voru upphaflega skrifaðir af eftirfarandi þátttakanda.*

* [Aldona Stec](https://www.linkedin.com/in/aldona-stec-25283bb1) | [!INCLUDE[prod_short](includes/prod_short.md)] ráðgjafi

## <a name="see-also"></a>Sjá einnig .

[Greina lista og fyrirspurnargögn með greiningarstillingu](analysis-mode.md)  
[Yfirlit yfir greiningar á eignum](fa-analytics-overview.md)  
[Yfirlit yfir greiningar, viðskiptagreind og skýrslur](reports-bi-reporting.md)  
[Yfirlit yfir eignir](fa-manage.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  

[!INCLUDE[footer-include](includes/footer-banner.md)]
