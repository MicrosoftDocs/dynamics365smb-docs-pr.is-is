---
title: Tilfallandi greining á fjárhagsgögnum
description: Fræðast um hvernig gagnagreiningarstillingin er notuð til að greina fjárhagsgögn.
author: kennienp
ms.author: kepontop
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'bi, power BI, analysis, KPI'
ms.search.form: '516, 9300, 5119, 9301, 9305'
ms.date: 05/02/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# Tilfallandi greining á fjárhagsgögnum

Þessi grein útskýrir hvernig á að nota aðgerðina **Gagnagreining** til að greina fjárhagsgögn beint frá listasíðum og fyrirspurnum. Ekki þarf að keyra skýrslu eða skipta yfir í annað forrit, t.d. Excel. Eiginleikinn býður upp á gagnvirka og fjölhæfa leið til að reikna út, taka saman og skoða gögn. Í stað þess að keyra skýrslur með valkostum og afmörkunum er hægt að bæta við mörgum flipum sem tákna mismunandi verk eða yfirlit á gögnunum. Nokkur dæmi eru "Heildareignir með tímanum", "Útistandandi skuldir", "Útistandandi skuldir" eða annað sem hægt er að ímynda sér. Til að fræðast meira um notkun aðgerðarinnar **Gagnagreining** er farið í [Greiningarlista og fyrirspurnargögn með greiningarstillingu](analysis-mode.md).

Eftirfarandi listasíður eru notaðar til að hefja tilfallandi greiningu á fjárhagsferlum:

- [Fjárhagsfærslur](https://businesscentral.dynamics.com/?page=20)
- [Viðskm.færslur](https://businesscentral.dynamics.com/?page=25)
- [Lánardr.færslur](https://businesscentral.dynamics.com/?page=29)

## Tilfallandi greiningardæmi í fjármálum

Aðgerðin **Gagnagreining** er notuð til að gera skyndiathugun og tilfalalengdar greiningar:

- Ef ekki á að keyra skýrslu.
- Ef skýrsla vegna sérstakra þarfa er ekki til.
- Ef þú vilt ítreka á fljótlegan hátt til að fá góða yfirsýn yfir hluta af fyrirtækinu þínu.

Eftirfarandi hlutar gefa dæmi um fjármálaaðstæður. [!INCLUDE [prod_short](includes/prod_short.md)]

| Svæðarit | Til... | Opna þessa síðu í greiningarstillingu | Þessir reitir notaðir |
| ---- | ----- | ------------------------------- |------------------- |
| [Vaxtareikningur (Útistandandi reikn.)](#example-finance-accounts-receivables) | Sjá hverju viðskiptamennirnir skulda, til dæmis, skipt niður í tímabil þegar upphæðir eru gjaldfallnar. | [Viðskm.færslur](https://businesscentral.dynamics.com/?page=25) | **Nafn viðskiptamanns**, **Gjalddagi** og **Eftirstöðvar** |
| [Vaxtareikningur (Safnreikningur)](#example-finance-accounts-payable) | Sjá hvað lánardrottnarnir skulda, kannski skipt niður í tímabil þegar upphæðir eru gjaldfaldar. | [Lánardr.færslur](https://businesscentral.dynamics.com/?page=29) | **Heiti lánardrottins, Tegund** fylgiskjals,Númer **fylgiskjals**, **Gjalddagaár**, **Gjalddaga mánuður** og **Eftirstöðvar**. **·** |
| [Fjármál (Rekstrarreikningur)](#example-finance-income-statement) | Sjá tekjur yfir tekjureikningana í bókhaldslyklinum, til dæmis, raðað niður í tímabil þegar upphæðir voru bókaðar. | [Fjárhagsfærslur](https://businesscentral.dynamics.com/?page=20) | **Fjárhagsreikn.nr.**, **Bókunardagsetning** og **Upphæð**. |
| [Fjármál (heildareignir)](#example-finance-total-assets) | Skoða eignir yfir eignareikningana í bókhaldslyklinum, til dæmis, skipt niður í tímabil þegar upphæðir voru bókaðar. | [Fjárhagsfærslur](https://businesscentral.dynamics.com/?page=20) | **Fjárhagsreikn.nr.**, **Bókunardagsetning** og **Upphæð**. |

### Dæmi: Fjárhagur (Útistandandi safnreikningur)

Til að sjá hvað viðskiptamenn skulda þér er kannski raðað niður í tímabil þegar upphæðir eru gjaldfallnar skal fylgja eftirfarandi skrefum:

1. Listinn [Viðskm.færslur](https://businesscentral.dynamics.com/?page=25) er opnaður og Færa inn greiningarstillingu valið :::image type="content" source="media/analysis-mode-icon.png" alt-text="."::: Til að kveikja á greiningarstillingu.
1. Farið er í valmyndina **Dálkar** og allir dálkar fjarlægðir (reiturinn er valinn við hliðina *á leitarreitnum* til hægri).
1. Kveikja á veltistillingu **·*** ví6 (staðsett fyrir ofan **leitarreitinn** hægra megin).
1. Reiturinn **Nafn** viðskiptamanns er dreginn á **svæðið Línuflokkar** og eftirstöðvar **dregnar** yfir í **svæðið Virði** .
1. Reiturinn **Gjalddagamánuður** er dreginn yfir í **svæðið Dálkmerki** .
1. Hægt er að gera greiningu á tilteknu ári eða ársfjórðungi með því að nota afmörkun í valmyndinni **Greiningarafmarkanir** (sem er undir valmyndinni **Dálkar** hægra megin).
1. Endurnefna greiningarflipann á **aldursgreiningarreikninga eftir mánuðum** eða eitthvað sem lýsir þessari greiningu.

### Dæmi: Fjárhagur (Safnreikningur)

Til að sjá hvað lánardrottnarnir skulda er kannski skipt niður í tímabil þegar upphæðir eru komnar á gjalddaga er eftirfarandi skrefum fylgt:

1.  [Opna skal listasíðuna Lánardr.færslur](https://businesscentral.dynamics.com/?page=29) og velja :::image type="content" source="media/analysis-mode-icon.png" alt-text="Færa inn greiningarham."::: Til að kveikja á greiningarstillingu.
1. Farið er í valmyndina **Dálkar** og allir dálkar fjarlægðir (reiturinn næst leitarreitnum **er** valinn).
1. Kveikja á **veltihamsvíkkuninni** (sem staðsett er fyrir ofan **leitarreitinn** hægra megin).
1. Draga skal reitinn Heiti lánardrottins **,** Tegund fylgiskjals **og** Númer fylgiskjals. **að** línuflokkasvæðinu **og** draga síðan reitinn **Eftirstöðvar** yfir í **svæðið Virði** .
1. Reitirnir Gjalddagaár **og** **Gjalddagamánuður** eru dregnir **í** svæðið Dálkmerki. Reitirnir eru dregnir í þeirri röð.
1. Hægt er að gera greiningu á tilteknu ári eða ársfjórðungi með því að nota afmörkun í valmyndinni **Greiningarafmarkanir** (sem er undir valmyndinni **Dálkar** hægra megin).
1. Endurnefna greiningarflipann á **Aldursgreiningarreikninga fyrir mánuð** eða eitthvað sem lýsir þessari greiningu.

Eftirfarandi mynd sýnir niðurstöður þessara skrefa.

:::image type="content" source="media/data-analysis-vendor-ledger-entries.png" alt-text="Dæmi um gagnagreiningu á síðunni Viðskm.færslur." lightbox="media/data-analysis-vendor-ledger-entries.png":::

### Dæmi: Fjármál (Rekstrarreikningur)

Til að skoða tekjur yfir tekjureikningana í bókhaldslyklinum er skipt niður í tímabil fyrir það hvenær upphæðir voru bókaðar er eftirfarandi skrefum fylgt:

1. Opnaðu [Fjárhagsfærslur](https://businesscentral.dynamics.com/?page=20) listann og veldu :::image type="content" source="media/analysis-mode-icon.png" alt-text="Opna greiningarstillingu."::: Til að kveikja á greiningarstillingu.
1. Farið er í valmyndina **Dálkar** og allir dálkar fjarlægðir (reiturinn næst leitarreitnum **er** valinn).
1. Kveikja á **veltihamsvíkkuninni** (sem staðsett er fyrir ofan **leitarreitinn** hægra megin).
1. Reiturinn Fjárhagsreikn.nr. er dreginn **.** yfir í línuflokkasvæðið **og upphæð** dregin **í** svæðið Virði **.** 
1. Reiturinn **Bókunardags.mánuður** er dreginn á **svæðið Dálklímmiðar** .
1. Afmarka skal reikningana sem notaðir eru fyrir rekstrarreikninginn.  [!INCLUDE [prod_short](includes/prod_short.md)] Í sýnigögnunum byrja þessir reikningar á "4" en bókhaldslykillinn gæti verið öðruvísi. Setja afmörkun á reikningana í valmyndinni **Greiningarafmarkanir** (sem er staðsettur fyrir neðan valmyndina **Dálkar** hægra megin).

   > [!TIP]
   > Til að sjá hvaða reikningar eru notaðir í uppsetningunni er skýrslan [Prófjöfnuður keyrður eftir tímabilum](https://businesscentral.dynamics.com/?report=38) .

1. Endurnefna greiningarflipa fyrir **Tekjur eftir mánuðum** eða eitthvað sem lýsir þessari greiningu.

### Dæmi: Fjármál (heildareignir)

Til að skoða eignir yfir eignareikningana í bókhaldslyklinum er skipt niður í tímabil þegar upphæðir voru bókaðar er gert á eftirfarandi hátt:

1. Opnaðu [Fjárhagsfærslur](https://businesscentral.dynamics.com/?page=20) listann og veldu :::image type="content" source="media/analysis-mode-icon.png" alt-text="Opna greiningarstillingu."::: Til að kveikja á greiningarstillingu.
1. Farið er í valmyndina **Dálkar** og allir dálkar fjarlægðir (reiturinn er valinn við hliðina **á leitarreitnum** til hægri).
1. Kveikja á **veltihamsvíkkuninni** (sem staðsett er fyrir ofan **leitarreitinn** hægra megin).
1. Reiturinn Fjárhagsreikn.nr. er dreginn **.** yfir í línuflokkasvæðið **og upphæð** dregin **í** svæðið Virði **.** 
1. Reiturinn **Bókunardags.mánuður** er dreginn á **svæðið Dálklímmiðar** .
1. Afmörkun á reikningum sem notaðir eru á yfirliti yfir heildareignir.  [!INCLUDE [prod_short](includes/prod_short.md)] Í sýnigögnunum byrja þessir reikningar á "10" en bókhaldslykillinn gæti verið öðruvísi. Setja afmörkun á viðeigandi reikninga í valmyndinni **Viðbótarafmarkanir** (sem er staðsett neðan valmyndarinnar **Dálkar** hægra megin).

   > [!TIP]
   > Til að sjá hvaða reikningar eru notaðir í uppsetningunni er skýrslan [Prófjöfnuður keyrður eftir tímabilum](https://businesscentral.dynamics.com/?report=38) .

1. Endurnefna greiningarflipa fyrir **Tekjur eftir mánuðum** eða eitthvað sem lýsir þessari greiningu.

## Gagnagrunnur fyrir tilfallandi greiningu á fjármálum

Við bókun færslubóka stofnar [!INCLUDE [prod_short](includes/prod_short.md)]  notandi færslur í **töflunni Fjárhagsfærsla** . Þess vegna er tilfallandi greining á almennum fjármálum yfirleitt unnin á síðunni [Fjárhagsfærslur](https://businesscentral.dynamics.com/?page=20) . Fyrir útistandandi og gjaldfallna reikninga er hægt að greina [viðskiptamannafærslur](https://businesscentral.dynamics.com/?page=25) og [lánardr.færslur](https://businesscentral.dynamics.com/?page=29).

Til að fá nánari upplýsingar er farið í eftirfarandi greinar:

- [Gagnagrunnur fyrir tilfalvarna greiningu á sölu](ad-hoc-analysis-sales.md#data-foundation-for-ad-hoc-analysis-on-sales)
- [Gagnagrunnur fyrir tilfallandi greiningu á innkaupum](ad-hoc-analysis-purchasing.md#data-foundation-for-ad-hoc-analysis-on-purchasing)

## Sjá einnig .

[Greina lista og fyrirspurnargögn með greiningarstillingu](analysis-mode.md)  
[Yfirlit fjárhagsgreininga](bi.md)  
[Yfirlit yfir greiningar, viðskiptagreind og skýrslur](reports-bi-reporting.md)  
[Fjárhagsyfirlit](finance.md)   
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  

[!INCLUDE[footer-include](includes/footer-banner.md)]