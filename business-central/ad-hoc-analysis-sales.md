---
title: Tilfalalengd greining á sölugögnum
description: Fræðast um hvernig gagnagreiningarstillingin er notuð til að greina sölugögn.
author: brentholtorf
ms.author: kepontop
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'bi, power BI, analysis, KPI'
ms.search.form: '516, 9300, 5119, 9301, 9305'
ms.date: 04/28/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# <a name="ad-hoc-analysis-of-sales-data"></a>Tilfalalengd greining á sölugögnum

Þessi grein útskýrir hvernig á að nota aðgerðina **Gagnagreining** til að greina sölugögn beint frá listasíðum og fyrirspurnum. Ekki þarf að keyra skýrslu eða skipta yfir í annað forrit, t.d. Excel. Eiginleikinn býður upp á gagnvirka og fjölhæfa leið til að reikna út, taka saman og skoða gögn. Í stað þess að keyra skýrslur með valkostum og afmörkunum er hægt að bæta við mörgum flipum sem tákna mismunandi verk eða yfirlit á gögnunum. Nokkur dæmi eru "Viðskiptamenn mínir" eða "Söluupplýsingar" eða hvaða önnur yfirlit sem hægt er að ímynda sér. Til að fræðast meira um notkun aðgerðarinnar **Gagnagreining** er farið í [Greiningarlista og fyrirspurnargögn með greiningarstillingu](analysis-mode.md).

Eftirfarandi listasíður eru notaðar til að gera augljósa greiningu á söluferlum:

- [Sölupantanir](https://businesscentral.dynamics.com/?page=9305)
- Fjárhagsfærslur
- [Viðskm.færslur](https://businesscentral.dynamics.com/?page=25)
- Vörubókafærslur
- Bókaðir sölureikningar
- Söluvöruskilapantanir

## <a name="sales-ad-hoc-analysis-scenarios"></a>Söluaðstæður í tilfalengdum greiningardæmum

Aðgerðin **Gagnagreining** er notuð til að gera skyndiathugun og tilfalalengdar greiningar:

- Ef ekki á að keyra skýrslu.
- Ef skýrsla vegna sérstakra þarfa er ekki til.
- Ef þú vilt ítreka á fljótlegan hátt til að fá góða yfirsýn yfir hluta af fyrirtækinu þínu.

Eftirfarandi hlutar gefa dæmi um söluaðstæður í [!INCLUDE [prod_short](includes/prod_short.md)].

| Svæðarit | Til... | Opna þessa síðu í greiningarstillingu | Þessir reitir notaðir |
| ---- | ----- | ------------------------------- |------------------- |
| [Sala (væntanlegt sölumagn)](#example-sales-expected-sales-volume) | Greining á áætluðu sölumagni. | [Sölupantanir](https://businesscentral.dynamics.com/?page=9305) | **Selt-til nafn** viðskm., **Selt-til viðskm.nr.**, **Nr.** , **Upphæð**, **Dags.ár** fylgiskjals og **Dags.mánuður** fylgiskjals. |
| [Sala (Sala viðskiptamanns eftir rúmmáli)](#example-sales-customer-sales-by-volume) | Fá yfirlit yfir þá viðskiptamenn sem kaupa mest inn eða sem skulda mest. | [Viðskm.færslur](https://businesscentral.dynamics.com/?page=25) | **Nafn viðskiptamanns, Númer** fylgiskjals, **Upphæð** og **Eftirstöðvar**. **·** |
| [Vaxtareikningur (Útistandandi safnreikningur)](#example-finance-accounts-receivables) | Sjá hverju viðskiptamennirnir skulda, til dæmis, skipt niður í tímabil þegar upphæðir eru gjaldfallnar. | [Viðskm.færslur](https://businesscentral.dynamics.com/?page=25) | **Nafn viðskiptamanns**, **Gjalddagi** og **Eftirstöðvar**. |

## <a name="example-sales-expected-sales-volume"></a>Dæmi: Sala (væntanlegt sölumagn)

Til að greina áætlað sölumagn og söluupphæðir óskráðra pantana fyrir hvern viðskiptamann fyrir ár eða mánuð skal fylgja eftirfarandi skrefum:

1. Listinn Sölupantanir [er opnaður](https://businesscentral.dynamics.com/?page=9305) og kveikt á greiningarstillingu.
1. Farið er í valmyndina **Dálkar** og allir dálkar fjarlægðir (reiturinn næst leitarreitnum **er** valinn).
1. Kveikja á **veltistillingu** (staðsett beint fyrir ofan **leitarreitinn**).
1.  **Selt-til nafn** viðskm., **Selt-til viðskm.nr.** og **Nr.**  **að línuflokkasvæðinu** . Reitirnir eru dregnir í þeirri röð.
1. Reiturinn **Upphæð** er dreginn í reitinn **Virðissvæði** .
1. Reitirnir **Dags.ár** fylgiskjals og **Dags.mánuður** fylgiskjals eru dregnir í svæði **dálkalímmiða** . Reitirnir eru dregnir í þeirri röð.
1. Afmörkun er notuð í valmyndinni **Viðbótarafmarkanir til að gera greiningu fyrir tiltekið ár eða ársfjórðung** . Valmyndin er hægra megin við síðuna, rétt fyrir neðan **dálkavalmyndina** .
1. Endurnefna greiningarflipa á **væntanlegt sölumagn** eða eitthvað sem lýsir þessari greiningu.

## <a name="example-sales-customer-sales-by-volume"></a>Dæmi: Sala (Sala viðskiptamanns eftir rúmmáli)

Til að framleiða yfirlit yfir viðskiptamenn sem kaupa mest inn eða sem skulda mest er eftirfarandi skrefum fylgt:

1. Listinn [Viðskm.færslur](https://businesscentral.dynamics.com/?page=25) er opnaður og kveikt á greiningarstillingu.
1. Farið er í valmyndina **Dálkar** og allir dálkar fjarlægðir (reiturinn næst leitarreitnum **er** valinn).
1. Reiturinn **Nafn** viðskiptamanns er dreginn inn í **línuflokkasvæðið** og reitinn **Númer fylgiskjals.** fyrir neðan hann.
1. Reitirnir **Upphæð**  **og** Eftirstöðvar eru velja.
1. Afmörkun er notuð í valmyndinni **Viðbótarafmarkanir til að gera greiningu fyrir tiltekið ár eða ársfjórðung** . Valmyndin er hægra megin við síðuna, rétt fyrir neðan **dálkavalmyndina** .
1. Endurnefna greiningarflipann á **Viðskiptamann eftir sölumagni** eða einhverju sem lýsir þessari greiningu.

Eftirfarandi mynd sýnir niðurstöður þessara skrefa.

:::image type="content" source="media/data-analysis-customer-ledger-entries.png" alt-text="Dæmi um gagnagreiningu á síðunni Viðskm.færslur." lightbox="media/data-analysis-customer-ledger-entries.png":::

## <a name="example-finance-accounts-receivables"></a>Dæmi: Fjárhagur (Útistandandi safnreikningur)

Til að sjá hvað viðskiptamenn skulda þér er kannski raðað niður í tímabil þegar upphæðir eru gjaldfallnar skal fylgja eftirfarandi skrefum:

1. Listinn [Viðskm.færslur er](https://businesscentral.dynamics.com/?page=25) opnaður og kveikt á greiningarstillingu.
1. Í valmyndinni **Dálkar** eru allir dálkar fjarlægðir (reiturinn við hliðina á leitarreitnum **er** valinn).
1. Kveikja á **veltistillingu** (staðsett beint fyrir ofan **leitarreitinn**).
1. Reiturinn **Nafn** viðskiptamanns er dreginn **á svæðið Línuflokkar** og reiturinn **Eftirstöðvar** dreginn yfir á **svæðið Virði** .
1. Reiturinn **Gjalddagamánuður** er dreginn yfir í **svæðið Dálkmerki** .
1. Afmörkun er notuð í valmyndinni **Viðbótarafmarkanir til að gera greiningu fyrir tiltekið ár eða ársfjórðung** . Valmyndin er hægra megin við síðuna, rétt fyrir neðan **dálkavalmyndina** .
1. Endurnefna greiningarflipann á **aldursgreiningarreikninga eftir mánuðum** eða eitthvað sem lýsir þessari greiningu.

## <a name="data-foundation-for-ad-hoc-analysis-on-sales"></a>Gagnagrunnur fyrir tilfalvarna greiningu á sölu

Þegar upplýsingar hafa verið færðar inn á sölupöntun og öllum sölupöntunarlínum bætt við er hægt að bóka pöntunina. Bókun stofnar afhendingu og reikning. [!INCLUDE [prod_short](includes/prod_short.md)] uppfærir reikning viðskiptamanns, fjárhag og birgðafærslur:

- Sölufærsla er stofnuð í **töflunni Fjárhagsfærsla** fyrir hverja sölupöntun. Færsla er einnig stofnuð í reikningi viðskiptamanns í töflunni **sérsniðin fjárhagsfærsla** og fjárhagsfærsla er stofnuð í viðeigandi safnreikningi viðskiptamanns. Auk þess getur bókun pöntunarinnar leitt til VSK-færslu og fjárhagsfærslu vegna afsláttarupphæðarinnar.
- Birgðafærsla er stofnuð í **töflunni Birgðafærsla** fyrir hverja sölupöntunarlínu (ef sölulínurnar eru með vörunúmerum) eða fjárhagsfærsla er stofnuð í **töflunni Fjárhagsfærsla** (ef fjárhagsreikningur er í sölulínunum). Þar að auki eru sölupantanir alltaf skráðar í töflunum **Haus** söluafhendingar og **Sölureikningshaus** .

Nánari upplýsingar um bókun sölu fást með því að fara [í Bókun sölu](ui-post-sales.md).

## <a name="see-also"></a>Sjá einnig .

[Bókun sölu](ui-post-sales.md)  
[Greina lista og fyrirspurnargögn með greiningarstillingu](analysis-mode.md)  
[Sölugreiningaryfirlit](sales-analytics-overview.md)  
[Yfirlit yfir greiningar, viðskiptagreind og skýrslur](reports-bi-reporting.md)  
[Söluyfirlit](sales-manage-sales.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  

[!INCLUDE[footer-include](includes/footer-banner.md)]
