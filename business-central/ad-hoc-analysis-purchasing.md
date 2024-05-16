---
title: Ad-hoc greiningar í innkaupum
description: Fræðast um hvernig gagnagreiningarstillingin er notuð til að greina gögn í innkaupum.
author: kennienp
ms.author: kepontop
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'bi, power BI, analysis, KPI'
ms.search.form: '9306, 9307, 518, 29'
ms.date: 04/29/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# Ad-hoc greiningar í innkaupum

Þessi grein útskýrir hvernig á að greina innkaup gagna af listasíðum og fyrirspurnum með aðgerðinni **Gagnagreining** . Eiginleikinn gerir kleift að greina gögn beint frá síðunni án þess að þurfa að keyra skýrslu eða opna annað forrit, t.d. Excel. Gagnagreining býður upp á gagnvirka og fjölhæfa leið til að reikna út, taka saman og skoða gögn. Í stað þess að keyra skýrslur með valkostum og afmörkunum er hægt að bæta við mörgum flipum sem tákna mismunandi verk eða yfirlit á gögnunum. Nokkur dæmi eru "Lánardrottnar mínir" eða "Innkaupatölur" eða öll önnur dæmi sem hægt er að ímynda sér. Til að fræðast meira um notkun aðgerðarinnar **Gagnagreining** er farið í [Greiningarlista og fyrirspurnargögn með greiningarstillingu](analysis-mode.md).

Eftirfarandi listasíður eru notaðar til að tilfalja greiningu á innkaupaferlum:

- [Innkaupapantanir](https://businesscentral.dynamics.com/?page=9307)
- [Innkaupalínur](https://businesscentral.dynamics.com/?page=518)
- [Bókaðir innkaupareikningar](https://businesscentral.dynamics.com/?page=146)
- [Lánardr.færslur](https://businesscentral.dynamics.com/?page=29)
- [Fjárhagsfærslur](https://businesscentral.dynamics.com/?page=20)

## Tilfallandi greiningardæmi fyrir innkaup

Aðgerðin **Gagnagreining** er notuð til að gera skyndiathugun og tilfalalengdar greiningar:

- Ef ekki á að keyra skýrslu
- Ef ekki er til skýrsla að sérþörfum þínum
- Ef þú vilt ítreka á fljótlegan hátt til að fá góða yfirsýn yfir hluta af fyrirtækinu þínu.

Eftirfarandi hlutar gefa dæmi um innkaup [!INCLUDE [prod_short](includes/prod_short.md)].

| Svæðarit | Til... | Opna þessa síðu í greiningarstillingu | Þessir reitir notaðir |
| ---- | ----- | ------------------------------- |------------------- |
| [YFIRLIT GRNI](#example-goods-received-not-invoiced-grni-overview) | Fá yfirlit yfir mótteknar vörur, ekki reikningsfærðar (GRNI) þvert á lánardrottna. | [Innkaupalínur](https://businesscentral.dynamics.com/?page=518) | **Tegund,Afh.upph** **. Ekki reikningsfært (SGM)** (afmörkun á þessum reitum), **Nr.** lánardrottins, **Númer fylgiskjals,** Nr **.**, og **Upph. Óreikn. reikningsfært (SGM)** <br><br> **ATH:** Sérstilla verður síðuna til að bæta þessum reitum við. Nánari upplýsingar eru notaðar til að sérstilla [vinnusvæðið](ui-personalization-user.md). | 
| [Vaxtareikningur (Safnreikningur)](#example-finance-accounts-payable) | Sjá hvað lánardrottnarnir skulda, kannski skipt niður í tímabil þegar upphæðir eru gjaldfaldar. | [Lánardr.færslur](https://businesscentral.dynamics.com/?page=29) | **Heiti lánardrottins, Tegund** fylgiskjals,Númer **fylgiskjals**, **Gjalddagaár**, **Gjalddaga mánuður** og **Eftirstöðvar**. **·** |

## Dæmi: vörur mótteknar, ekki reikningsfærðar (GRNI) yfirlit

Til að búa til yfirlit yfir mótteknar vörur sem ekki hafa verið reikningsfærðar (GRNI) yfir lánardrottna skal fylgja eftirfarandi skrefum:

1. Listasíða Innkaupalína er [opnuð](https://businesscentral.dynamics.com/?page=518).
1. Sérstilla síðuna til að bæta reitnum **Móttekin upphæð óreikningsfærð** . Til að sérstilla síðuna skal velja **Stillingar** og sérstilla **síðan.**
1. Velja skal :::image type="content" source="media/analysis-mode-icon.png" alt-text="Færa inn greiningarham."::: Til að kveikja á greiningarstillingu.
1. Farið er í valmyndina **Dálkar** og allir dálkar fjarlægðir (reiturinn er valinn við hliðina **á leitarreitnum** til hægri).
1. Í valmyndinni **Viðbótarafmarkanir** (sem er staðsettur fyrir neðan valmyndina **Dálkar** til hægri) eru eftirfarandi afmarkanir stilltar:
    - **Tegund = Vara**
    - **Upphæð upph. > 0**, óreikn.reiknf. (SGM) 
1. Draga skal reitinn **Nr.** lánardrottins, **Númer** fylgiskjals og **Nr.**  **að línuflokkasvæðinu** . Reitirnir eru dregnir í þeirri röð.
1. Reitnum Afh.upph.upph. er **bætt við Reiturinn Óreikningsfært (SGM)** til að taka hann með í yfirlitinu.
1. Afmörkun er notuð í valmyndinni **Greiningarafmarkanir til að gera greiningu fyrir tiltekið ár eða ársfjórðung** . Valmyndin er hægra megin við síðuna, rétt fyrir neðan **dálkavalmyndina** .
1. Endurnefna greiningarflipann á **Mótteknar vörur, Ekki reikningsfært (GRNI)** eða eitthvað sem lýsir þessari greiningu.

## Dæmi: Fjárhagur (útistandi skuldir)

Til að sjá hvað lánardrottnarnir skulda er kannski skipt niður í tímabil þegar upphæðir eru komnar á gjalddaga er eftirfarandi skrefum fylgt:

1.  [Opna skal listasíðuna Lánardr.færslur](https://businesscentral.dynamics.com/?page=29) og kveikja á greiningarstillingu.
1. Farið er í valmyndina **Dálkar** og allir dálkar fjarlægðir (reiturinn er valinn við hliðina **á leitarreitnum** til hægri).
1. Kveikja á **veltihamsvíkkuninni** (sem staðsett er fyrir ofan **leitarreitinn** hægra megin).
1. Draga skal reitinn Heiti lánardrottins **,** Tegund fylgiskjals **og** Númer fylgiskjals. **að** línuflokkasvæðinu **og** draga síðan reitinn **Eftirstöðvar** yfir í **svæðið Virði** .
1. Reitirnir Gjalddagaár **og** **Gjalddagamánuður** eru dregnir **í** svæðið Dálkmerki. Reitirnir eru dregnir í þeirri röð.
1. Hægt er að gera greiningu á tilteknu ári eða ársfjórðungi með því að nota afmörkun í valmyndinni **Greiningarafmarkanir** (sem er undir valmyndinni **Dálkar** hægra megin).
1. Endurnefna greiningarflipann á **Aldursgreiningarreikninga fyrir mánuð** eða eitthvað sem lýsir þessari greiningu.

Eftirfarandi mynd sýnir niðurstöður þessara skrefa.

:::image type="content" source="media/data-analysis-vendor-ledger-entries.png" alt-text="Dæmi um gagnagreiningu á síðunni Viðskm.færslur." lightbox="media/data-analysis-vendor-ledger-entries.png":::

## Gagnagrunnur fyrir tilfallandi greiningu á innkaupum

Þegar innkaupaskjal er bókað uppfærist [!INCLUDE [prod_short](includes/prod_short.md)]  reikningur lánardrottins, fjárhagur (fjárhagur), birgðafærslur og forðafærslur:

- Fyrir hvert innkaupaskjal er innkaupafærsla stofnuð í töflunni **Fjárhagsfærsla**. Færsla er einnig stofnuð í lánardrottnareikningi **í töflunni Birgjafærsla** og fjárhagsfærsla er stofnuð í viðeigandi safnreikningi lánardrottna. Auk þess getur bókun innkaupanna leitt til virðisaukaskattsfærslu (VSK) og fjárhagsfærslu vegna afsláttarupphæðarinnar.

- Fyrir hverja innkaupalínu, eftir því sem við á, eru færslur stofnaðar í:
  - **Birgðafærsla** ef innkaupalínan er af tegundinni Vara.
  - **Ef innkaupalínan er af tegundinni Fjárhagsreikningur er taflan Fjárhagsfærsla** .
  - **Ef innkaupalínan er af tegundinni Forði er taflan Forðafærsla** .
- Þar að auki eru innkaupaskjöl alltaf skráð í töflunum **Innk.móttökuhaus** og **Innk.reikningshaus**.

Nánari upplýsingar eru notaðar [til að](purchasing-how-record-purchases.md#posting-purchases) bóka innkaup.

## Sjá einnig .

[Bókun innkaupa](purchasing-how-record-purchases.md#posting-purchases)  
[Greina lista og fyrirspurnargögn með greiningarstillingu](analysis-mode.md)  
[Yfirlit yfir greiningar, viðskiptagreind og skýrslur](reports-bi-reporting.md)  
[Yfirlit yfir innkaup](purchasing-manage-purchasing.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  

[!INCLUDE[footer-include](includes/footer-banner.md)]