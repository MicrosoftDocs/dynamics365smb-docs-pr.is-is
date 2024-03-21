---
title: Yfirlit yfir verkhluta uppsetningu innkaupa
description: Lýsir verkhlutanum sem felur í sér skilgreiningu á innkaupastefnu fyrirtækisins og uppsetningu innkaupaferla.
author: brentholtorf
ms.topic: overview
ms.devlang: al
ms.search.keywords: 'procurement, supply, vendor order'
ms.search.form: '175, 176, 177, 178, 456, 460, 5727, 5729'
ms.date: 08/30/2022
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Uppsetning innkaupa

Áður en hægt er að hefjast handa við að stýra kaupferlum þarf að grunnstilla reglur og gildi sem ráða kaupreglum fyrirtækisins.

Þú verður að skilgreina almenna uppsetningu á síðunni **Uppsetning innkaupagrunns** sem er yfirleitt gert í eitt skipti við fyrstu innleiðingu. Frekari upplýsingar er að finna í [Uppsetning innkaupagrunns](#purchases-and-payables-setup).

Sérstakar raðir verkefna sem tengjast skráningu nýrra lánardrottna er að skrá öll sérstök verð eða afsláttarsamninga sem þú hefur með hverjum lánardrottni.

Farið er nánar yfir uppsetningu kaupa sem tengjast fjármunum, svo sem greiðsluaðferðir og gjaldmiðlar í hlutanum uppsetning fjárhags. Frekari upplýsingar má finna á [Uppsetning Fjármála](finance-setup-finance.md). Á sama hátt er hægt að finna birgðatengda uppsetningu innkaupa, svo sem mælieiningar og rakningarkóða atriða, í hlutanum [Birgðagrunnur](inventory-setup-inventory.md).

## Innkaupagrunnur

Áður en unnið er með innkaup og viðskiptaskuldir skal tilgreina á síðunni **Innkaupagrunnur** hvernig innkaupavirði er bókað og númeraröðin sem notuð er fyrir lánardrottna- og innkaupaskjöl.

### Almennar stillingar

Á flýtiflipanum **Almennt** eru tilgreindir valkostir, eins og hvernig á að reikna og bóka afslátt og hvort slétta eigi reikninga, tilgreindir hér. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].

Sumir reitir þurfa sérstaka athygli, eins og reiturinn **Reikna reikn.afsl. e. VSK/skattnr.** sem tilgreinir hvort reikningsafslátturinn sé reiknaður samkvæmt skattauðkenninu eða heildarupphæð reiknings. Frekari upplýsingar má finn í [Sameina VSK-bókunarflokka og VSK-bókunaruppsetningar](finance-setup-vat.md#combine-vat-posting-groups-in-vat-posting-setups).

Reiturinn **Jöfnun milli gjaldmiðla** getur einnig leitt til smá sléttunarmismunar þegar færslur eru jafnaðar í mismunandi gjaldmiðlum. Frekari upplýsingar má finna í [Leyfa jöfnun fjárhagsfærslna í mismunandi gjaldmiðlum](finance-how-enable-application-ledger-entries-different-currencies.md).

Einnig geta sumir reitir breytt hegðun sinni eða farið eftir því hvernig aðrir reitir eru stilltir. Til dæmis verður eiginleikinn **Athuga fyrirframgr. við bókun** fyrir áhrifum þegar **Sjálfvirk uppfærsla fyrirframgr.** er stilltur á að athuga fyrirframgreiðslur í bið.

Lestu upplýsingar um reitina [**Nr. utanaðk. skjals áskilið**](#external-document-number) og [**Nákvæmar kostnaðarbakfærslur áskildar**](#exact-cost-reversing) hér að neðan.

### Stillingar númeraraðar

Í flýtiflipanum **Númeraraðir** þarf að tilgreina einkvæman auðkenniskóða sem verður notaður fyrir lánardrottna, reikninga og önnur innkaupaskjöl. Tölusetning er mikilvæg ekki bara fyrir innri ferla heldur gæti einnig þurft að fylgja staðbundnum reglugerðum. Svo það gæti verið þess virði að íhuga að setja upp allar raðirnar á síðunni **Númeraraðir** á undan í staðinn fyrir að búa til nýjar í **Uppsetning innkaupagrunns**. Frekari upplýsingar er að finna í [Búa til númeraraðir](ui-create-number-series.md).

## Númer ytra skjals

[!INCLUDE [ext-doc-no-purch](includes/ext-doc-no-purch.md)]

## Nákvæm bakfærsla kostnaðar

Aðgerðina **Nákvæmar kostnaðarbakfærslur áskildar** tryggir að skilavörur séu metnar á sama kostnaði og þegar þær voru teknar úr birgðum með því að nota fasta jöfnun í staðinn fyrir að fylgja meðaltali eða fyrst inn, fyrst út (FIFO) kostnaðarútreikningi. Frekari upplýsingar er að finna í hlutanum [Hönnunarupplýsingar: Föst jöfnun](design-details-item-application.md#fixed-application). Ef viðbótarkostnaði er síðar bætt við upphaflegu innkaupin er virði innkaupaskilanna uppfært til samræmis.

Með eiginleikann virkan getur skilafærsla aðeins verið bókuð með því að tilgreina birgðafærslunúmerið í reitinn **Jafna í birgðafærslu** í vöruskilapöntunarlínu innkaupa. Reiturinn er ekki sjálfgefið sýndur í flýtiflipanum **Línur**. Lærðu að bæta reitum á síður í  [hlutanum sérsníða vinnusvæði](ui-personalization-user.md#start-personalizing-by-using-the-personalization-mode) .

[!INCLUDE[local-functionality](includes/local-functionality.md)]

## Fleiri innkaupauppsetningar

| Til | Sjá |
| --- | --- |
| Stofna lánardrottnaspjald fyrir alla lánardrottna keypt er af |[Skráning nýrra lánardrottna](purchasing-how-register-new-vendors.md) |
| Lánardrottnum forgangsraðað. |[Forgangsraða lánardrottnum](purchasing-how-prioritize-vendors.md) |
| Færðu inn bankareikningsupplýsingar&mdash;þ.m.t. alþjóðlegt bankareikningsnúmer (IBAN) og SWIFT-kóða&mdash;á lánardrottnaspjaldi. | [Uppsetning lánardrottnabankareikninga](purchasing-how-set-up-vendors-bank-accounts.md) |
| Settu upp kaupendur, úthlutaðu þeim lánardrottnum og kóða til að rekja tölfræði. |[Setja upp kaupendur](purchasing-how-setup-purchasers.md) |
| Skráið inn mismunandi afslætti og sérverð sem lánardrottinn veitir, sem fer eftir vörum, magni og/eða dagsetningum. |[Skráning innkaupaverðs, afsláttar og greiðslusamkomulags](purchasing-how-record-purchase-price-discount-payment-agreements.md) |
| Skilgreindu hvað þú greiðir fyrir vörur og þjónustu sem fyrirtækið þitt greiðir.  | [Setja upp verð og afslætti](across-prices-and-discounts.md) |
| Stofnaðu staðlaðar línur sem á að setja inn í endurtekin innkaupaskjöl. | [Setja upp endurteknar innkaupalínur](purchasing-how-work-recurring-purchase-lines.md) |
| Búðu til raðir af verkum til að tengja ferla sem mismunandi notendur framkvæma, eins og beiðni um eða samþykkt innkaupapantana. | [Setja upp samþykktarverkflæði innkaupa](across-set-up-workflows.md) |
| Stjórnaðu samskiptum í viðskiptum við lánardrottna, flyttu inn móttekin reikningsskjöl og skráðu nýja birgja með Outlook-tölvupóstforritinu. | [Setja upp innbót Business Central fyrir Outlook](admin-outlook.md) |
| Farðu yfir kostnaðarkvittanir, breyttu pappírsskjölum og rafrænum skjölum í færslubókarlínur og komdu pappírsreikningum frá lánardrottnum yfir á tölvutækt form. | [Setja upp skjöl á innleið](across-how-setup-income-documents.md) |
| Tilgreina sjálfgefnar skýrslur sem á að nota fyrir mismunandi skjalagerðir. |[Skýrsluval í Business Central](across-report-selections.md)|
|Tilgreinið hvort notendur eigi að fá bókun innkaupareikninga og hvort þeir verði að bóka þá ásamt sendingu. |[Skilgreina bókunarreglu reiknings fyrir notendur](admin-setup-invoice-posting-policy.md)|

## Sjá einnig .

[Innkaup](purchasing-manage-purchasing.md)  
[Setja upp yfirlit](setup.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
