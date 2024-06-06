---
title: Tilfalengd greining á birgðagögnum
description: Fræðast um hvernig gagnagreiningarstillingin er notuð til að greina birgðagögn.
author: kennienp
ms.author: kepontop
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'bi, power BI, analysis, KPI'
ms.search.form: '516, 9300, 5119, 9301, 9305'
ms.date: 05/03/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# Tilfalengd greining á birgðagögnum

Þessi grein útskýrir hvernig á að nota aðgerðina **Gagnagreining** til að greina birgðagögn beint frá listasíðum og fyrirspurnum. Ekki þarf að keyra skýrslu eða skipta yfir í annað forrit, t.d. Excel. Eiginleikinn býður upp á gagnvirka og fjölhæfa leið til að reikna út, taka saman og skoða gögn. Í stað þess að keyra skýrslur með valkostum og afmörkunum er hægt að bæta við mörgum flipum sem tákna mismunandi verk eða yfirlit á gögnunum. Sum dæmi eru "útrunnin lager" eða "sölumenn" eða önnur sjónarmið sem hægt er að ímynda sér. Til að fræðast meira um notkun aðgerðarinnar **Gagnagreining** er farið í [Greiningarlista og fyrirspurnargögn með greiningarstillingu](analysis-mode.md).

Nota eftirfarandi listasíður til að tilfalja greiningu á birgðaferlum:

- [Birgðafærslur](https://businesscentral.dynamics.com/?page=38)

## Tilfalvarnar birgðagreiningar

Aðgerðin **Gagnagreining** er notuð til að gera skyndiathugun og tilfalalengdar greiningar:

- Ef ekki á að keyra skýrslu.
- Ef skýrsla vegna sérstakra þarfa er ekki til.
- Ef þú vilt ítreka á fljótlegan hátt til að fá góða yfirsýn yfir hluta af fyrirtækinu þínu.

Eftirfarandi hlutar gefa dæmi um birgðaaðstæður [!INCLUDE [prod_short](includes/prod_short.md)].

| Svæðarit | Til... | Opna þessa síðu í greiningarstillingu | Þessir reitir notaðir |
| ---- | ----- | ------------------------------- |------------------- |
| [Lagerbirgðir](#example-inventory-on-hand) | Fá yfirlit yfir vörur sem eru tiltækar í birgðaskrá. | [Birgðafærslur](https://businesscentral.dynamics.com/?page=38) | **Vörunr.**, **Eftirstöðvar (magn)** |
|[Dæmi: rekja útrunnið eða gamlar birgðir](#example-track-expiring-or-old-stock) | Fá yfirlit yfir vörur í birgðum sem hafa verið á lager í langan tíma og eru ekki að selja vel. | [Birgðafærslur](https://businesscentral.dynamics.com/?page=38) | **Bókunardags.ár,Bókunardags.mánuður,Vörunr** **·** **.**, **Bókunardagsetning,Tegund** **færslu**, **Magn** og **Eftirstöðvar (magn)** |
| [Skilavörur eftir ástæðu skila](#example-returned-items-by-return-reason) | Fá yfirlit yfir vörur sem viðskiptamenn skila, flokkaðar eftir ástæðu skila. Nota þetta til greiningar fyrir gæðaeftirlit. | [Birgðafærslur](https://businesscentral.dynamics.com/?page=38) | **Ástæðukóti** vöruskila,Bókunardags.mánuður,Magn,Kostnaðarupphæð,Bókunardagsetning,Tegund **·** **·**  **·** **·** **fylgiskjals**,Vörunr.og **·**  **Númer**  fylgiskjals. |
| Afkastageta birgða | Fá yfirlit yfir innkaup og sölu í birgðum eftir mánuðum eða ársfjórðungi. | [Birgðafærslur](https://businesscentral.dynamics.com/?page=38) | **Bókunardags.ár,Bókunardags.mánuður,Vörunr** **·** **.**, **Magn**, **Upphæð sölu,Kostnaðarupphæð** **(raunverul.)** og **Mánuður bókunardagsetningar** |
| [Birgðahreyfingar] | Fá yfirlit yfir hvernig vörur í birgðahreyfingum milli birgðageymslna eru færðar. | [Birgðafærslur](https://businesscentral.dynamics.com/?page=38) | **Kóti** birgðageymslu,Magn,Bókunardags **·** **.**, **Vörunr.** |

## Dæmi: lagerbirgðir

Til að greina vörur í birgðum sem eru til á lager skal fylgja eftirfarandi skrefum:

1. Opna listann [Birgðafærslur](https://businesscentral.dynamics.com/?page=38) listann og veldu :::image type="content" source="media/analysis-mode-icon.png" alt-text="Opna greiningarstillingu."::: Til að kveikja á greiningarstillingu.
1. Farið er í valmyndina **Dálkar** og allir dálkar fjarlægðir (reiturinn næst leitarreitnum **er** valinn).
1. Reiturinn Vörunr. er dreginn til að **skoða reitinn Vörun** til **línuflokkasvæðisins** . Reitirnir eru dregnir í þeirri röð.
1. Reiturinn **Eftirstöðvar (magn**) er dreginn í **gildin** .
1. Stilla ójafn afmörkun **á** 0 **á** Eftirstöðvar (**magn)** Ef neikvæð birgðastig eru ekki leyfð er sett **hærra en** afmörkun á **0**.
1. Einnig er hægt að bæta öðrum reitum við greininguna og hugsanlega velti í birgðageymslu eða öðrum reitum.
1. Endurnefna greiningarflipa fyrir Birgðir á **lager** eða eitthvað sem lýsir þessari greiningu.

Eftirfarandi mynd sýnir niðurstöður þessara skrefa.

:::image type="content" source="media/data-analysis-inventory-on-hand.png" alt-text="Dæmi um hvernig gera á greiningu á birgðum á lagerbirgðum." lightbox="media/data-analysis-inventory-on-hand.png":::

## Dæmi: rekja útrunnið eða gamlar birgðir

Til að greina vörur í birgðum sem hafa verið á lager í langan tíma og eru ekki að selja vel skal fylgja eftirfarandi skrefum:

1. Opnaðu [Fjárhagsfærslur](https://businesscentral.dynamics.com/?page=38) listann og veldu :::image type="content" source="media/analysis-mode-icon.png" alt-text="Opna greiningarstillingu."::: Til að kveikja á greiningarstillingu.
1. Farið er í valmyndina **Dálkar** og allir dálkar fjarlægðir (reiturinn er valinn við hliðina **á leitarreitnum** til hægri).
1. Draga skal reitina **Bókunardags.ár,Bókunardags.mánuður** **·**  og **Vörunr.**  **að línuflokkasvæðinu** . Reitirnir eru dregnir í þeirri röð.
1. Í reitnum **Dálkar eru reitirnir** Bókunardags **.,** Færslutegund **·**, **Magn** og **Eftirstöðvar (magn**) valið.
1. Stilla skal **Lægra en** afmörkun á **bókunardagsetningu** til að tilgreina hvað er átt við með "gömlum".
1. Endurnefna greiningarflipa fyrir Gamlar **birgðir** eða eitthvað sem lýsir þessari greiningu.

Eftirfarandi mynd sýnir niðurstöður þessara skrefa.

:::image type="content" source="media/data-analysis-inventory-dead-stock.png" alt-text="Dæmi um hvernig á að gera greiningu á dauðri birgðagagnagreiningu á síðunni Birgðafærslur." lightbox="media/data-analysis-inventory-dead-stock.png":::

## Dæmi: skilavörur eftir ástæðu skila

Til að greina skilavöru sem raðað er eftir ástæðum fyrir vöruskilum er eftirfarandi skrefum fylgt:

1. Listinn Birgðafærslur er [opnaður](https://businesscentral.dynamics.com/?page=38) .
1. Reitnum **Ástæðukóti** vöruskila er bætt við með því að sérsníða síðuna. Í valmyndinni **Stillingar** er valið **Sérstilla**.
1. Loka sérstillingarstillingu.
1. Velja skal :::image type="content" source="media/analysis-mode-icon.png" alt-text="Færa inn greiningarham."::: Til að kveikja á greiningarstillingu.
1. Farið er í valmyndina **Dálkar** og allir dálkar fjarlægðir (reiturinn er valinn við hliðina **á leitarreitnum** til hægri).
1. Reitirnir **Ástæðukóti** skila og **Bókunardags. mánaðar** eru dregnir í **línuflokkasvæðið** . Reitirnir eru dregnir í þeirri röð.
1. Reitirnir  **Magn** og **Kostnaðarupphæð** eru dregnir að **gildasvæðinu** .
1. Bæta skal við öðrum reitum sem eiga að vera í greiningunni og virkja þá í **dálkasvæðinu** . Til dæmis er hægt að bæta við **bókunardagsetningu**, **tegund** fylgiskjals,Vörunr **.** og  **Númer fylgiskjals.** Svæði.
1. Endurnefna greiningarflipa til skilavara **eftir ástæðu** skila eða eitthvað sem lýsir þessari greiningu.  

## Dæmi: gegnumstætt birgðir

1. Opna listann [Fjárhagsfærslur](https://businesscentral.dynamics.com/?page=38) listann og veldu :::image type="content" source="media/analysis-mode-icon.png" alt-text="Opna greiningarstillingu."::: Til að kveikja á greiningarstillingu.
1. Farið er í valmyndina **Dálkar** og allir dálkar fjarlægðir (reiturinn er valinn við hliðina **á leitarreitnum** til hægri).
1. Kveikja á **veltihamsvíkkuninni** (sem staðsett er fyrir ofan **leitarreitinn** hægra megin).
1. Draga skal reitina **Bókunardags.ár,Bókunardags.mánuður** **og** **Vörunr.**  **að línuflokkasvæðinu** .
1. Reitirnir **Magn**, **Upphæð** sölu og **Kostnaðarupphæð (raunverul.)** eru dregnir **í reitina** Virði.
1. Reiturinn **Bókunardags.mánuður** er dreginn í **svæðið Dálkflokkar** .
1. Endurnefna greiningarflipa fyrir **Birgðir troughput eftir mánuði** eða eitthvað sem lýsir þessari greiningu.  

## Birgðahreyfingar

Til að rekja birgðahreyfingar milli birgðageymslna skal fylgja eftirfarandi skrefum:

1. Opnaðu [Fjárhagsfærslur](https://businesscentral.dynamics.com/?page=38) listann og veldu :::image type="content" source="media/analysis-mode-icon.png" alt-text="Opna greiningarstillingu."::: Til að kveikja á greiningarstillingu.
1. Farið er í valmyndina **Dálkar** og allir dálkar fjarlægðir (reiturinn er valinn við hliðina **á leitarreitnum** til hægri).
1. Reiturinn **Kóti** birgðageymslu er dreginn að **svæðinu Línuflokkar** .
1. Reiturinn **Magn er** dreginn að **gildasvæðinu** .
1. Bæta skal við öðrum reitum sem eiga að vera í greiningunni og virkja þá í **dálkasvæðinu** . Til dæmis er hægt að bæta við vörunr **.** Ef reiturinn er auður er
1. Endurnefna greiningarflipa fyrir **hreyfingar** í birgðum eða eitthvað sem lýsir þessari greiningu.  

   > [!TIP]
   > Ef reitnum Bókunardagsetning er bætt við er einnig hægt að rekja hreyfingar með tímanum.

## Gagnagrunnur fyrir tilfalvarna greiningu á birgðum

Þegar sölupöntun er bókuð uppfærist [!INCLUDE [prod_short](includes/prod_short.md)]  reikningur viðskiptamanns, fjárhags og birgðafærslna.

- Birgðafærsla er stofnuð í **töflunni Birgðafærsla** fyrir hverja sölupöntunarlínu (ef vörunúmer eru í sölulínunum). Þar að auki eru sölupantanir alltaf skráðar í töflunum **Haus** söluafhendingar og **Sölureikningshaus** . Nánari upplýsingar um bókun sölu fást með því að fara [í Bókun sölu](ui-post-sales.md).

Við bókun innkaupaskjals uppfærist [!INCLUDE [prod_short](includes/prod_short.md)]  reikningur lánardrottins, fjárhagur (fjárhagur), birgðafærslur og forðafærslur.

- Færslur eru búnar til í **töflunni Birgðafærsla** fyrir hverja innkaupalínu (ef innkaupalínan er af tegundinni Vara). Þar að auki eru innkaupaskjöl alltaf skráð í töflunum **Innk.móttökuhaus** og **Innk.reikningshaus**. Nánari upplýsingar eru notaðar [til að](purchasing-how-record-purchases.md#posting-purchases) bóka innkaup.

## Sjá einnig .

[Greina lista og fyrirspurnargögn með greiningarstillingu](analysis-mode.md)  
[Birgðagreiningaryfirlit](inventory-analytics-overview.md)  
[Yfirlit yfir greiningar, viðskiptagreind og skýrslur](reports-bi-reporting.md)  
[Yfirlit yfir birgðir](inventory-manage-inventory.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  

[!INCLUDE[footer-include](includes/footer-banner.md)]