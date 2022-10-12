---
title: Yfirlit yfir verkefni sem setja á upp innkaup
description: Lýsir verkhlutanum sem felur í sér skilgreiningu á innkaupastefnu fyrirtækisins og uppsetningu innkaupaferla.
author: SorenGP
ms.topic: overview
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: procurement, supply, vendor order
ms.search.form: 175, 176, 177, 178, 456, 460, 5727, 5729
ms.date: 08/30/2022
ms.author: edupont
ms.openlocfilehash: 82083beeb1779455fbd4b8a6083663b5559129eb
ms.sourcegitcommit: 8ad79e0ec6e625796af298f756a142624f514cf3
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/30/2022
ms.locfileid: "9606614"
---
# <a name="setting-up-purchasing"></a>Uppsetning innkaupa

Áður en hægt er að hefjast handa við að stýra kaupferlum þarf að grunnstilla reglur og gildi sem ráða kaupreglum fyrirtækisins.

Skilgreina verður almenna uppsetningu á **uppsetningarsíðu** innkaupa & lánardrottna sem vanalega er gert einu sinni við upphaflegu innleiðinguna. Frekari upplýsingar er að fá í eftirfarandi hluta, [uppsetningu innkaupa og greiðslu](#purchases-and-payables-setup).

Aðskilin röð verkefna sem tengjast skráningu nýrra lánardrottna er að skrá allar sérstakar verð-eða afsláttarsamninga við hvern lánardrottinn.

Fjármögnunargrunnur sem tengist innkaupum, s.s. greiðsluaðferðum og gjaldmiðlum, er fjallað um í hlutanum fjármálauppsetning. Frekari upplýsingar er að setja upp í [fjármálum](finance-setup-finance.md). Á sama hátt er hægt að finna birgðatengda innkaupauppsetningu eins og mælieiningar og vörurakningarkóta í [hlutanum birgðauppsetning](inventory-setup-inventory.md).

## <a name="purchases-and-payables-setup"></a>Uppsetning innkaupa og skulda

Tilgreinið á **uppsetningarsíðu** innkaupa & lánardrottna hvernig innkaupavirði er bókað og númeraröðin sem er notuð í lánardrottnum og innkaupaskjölum, áður en unnið er með innkaup og skuldir.

### <a name="general-settings"></a>Almennar stillingar

**Á flipanum Almennt** eru tilgreindir Valkostir eins og hvernig á að reikna út og bóka afslátt og hvort slétta eigi reikninga. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].

Sum svæði þarfnast sérstakrar athygli, til dæmis í **reitnum Reikna reikn. afsl. fyrir HVERN VSK/skattkenni**, sem tilgreinir hvort reikningsafsláttur sé reiknaður samkvæmt skattkenni eða samtölu reiknings. Frekari upplýsingar eru í að [tengja VSK-bókunarflokka í uppsetningar](finance-setup-vat.md#combine-vat-posting-groups-in-vat-posting-setups) VSK-bókunar.

**Á sama hátt getur reiturinn frammistaðan milli gjaldmiðla** valdið litlum sléttunarmismun þegar færslur í mismunandi gjaldmiðlum eru jafnaðar hver annarri. [Frekari upplýsingar eru virkar með því að virkja jöfnun færslna í mismunandi gjaldmiðlum](finance-how-enable-application-ledger-entries-different-currencies.md).

Einnig breyta sumir reitir hegðun sinni eða fara eftir því hvernig önnur svæði eru sett. Til dæmis **hefur aðgerðin fyrirframbókun** þegar áhrif **á aðgerðina. Sjálfvirk Uppfærslusvæði** er stillt til að leita að fyrirframgreiðslum í bið.

Lesa upplýsingar um [**EXT-Doc. nr. Skyldubundin**](#external-document-number) og [**nákvæm bakáskyldusvæði**](#exact-cost-reversing) að neðan.

### <a name="number-series-settings"></a>Stillingar númeraraðar

**Í númeraröðinni** fastanum þarf að tilgreina einkvæman auðkenniskóða sem verða notaðir fyrir lánardrottna, reikninga og önnur innkaupaskjöl. Tölusetning er mikilvæg ekki aðeins fyrir innri ferla heldur getur einnig þurft að fylgja staðbundnum reglugerðum. Svo það gæti verið þess virði miðað við að setja allar raðirnar í **Nr. Raða** síðu fyrirfram í stað þess að stofna nýjar úr **uppsetningu** Innkaup&. Frekari upplýsingar í [stofna númeraröð](ui-create-number-series.md).

## <a name="external-document-number"></a>Númer ytra skjals

[!INCLUDE [ext-doc-no-purch](includes/ext-doc-no-purch.md)]

## <a name="exact-cost-reversing"></a>Nákvæm bakkostnaðaráætlun

Skylduaðgerð **fyrir** nákvæma kostnaðarbakgerð hjálpar til við að tryggja að skilagreinar séu metnar á sama kostnað og þegar þær voru upphaflega teknar úr birgðum, með fastri umsókn í stað meðaltals-eða fyrsta útfærslukostnaðar (FIFO) kostnaðarútreiknings. Frekari upplýsingar í [Hönnunarupplýsingum: fastur kerfishluta](design-details-item-application.md#fixed-application). Ef viðbótarkostnaði er síðar bætt við upphaflegu innkaupin uppfærir kerfið gildið í viðkomandi innkaupaskilum.

Með aðgerðinni virkt er aðeins hægt að bóka endursölufærslu með því að tilgreina færslunúmer birgðafærslu í **reitnum Jafna** birgðafærslu í pöntunarlínu innkaupaskilapöntunar. Sjálfgefið er að svæðið sé ekki birt **í fastflipanum línur**. Lærðu að bæta reitum á síður í [hlutanum sérsníða vinnusvæði](ui-personalization-user.md#to-start-personalizing-a-page-through-the-personalizing-banner).

[!INCLUDE[local-functionality](includes/local-functionality.md)]

## <a name="more-purchasing-setups"></a>Fleiri innkaupauppsetningar

| Til | Sjá |
| --- | --- |
| Stofnið lánardrottinsspjald fyrir hvern lánardrottinn sem er keypt úr. |[Skráning nýrra lánardrottna](purchasing-how-register-new-vendors.md) |
| Forgangsraða lánardrottnum. |[Forgangsraða lánardrottnum](purchasing-how-prioritize-vendors.md) |
| Færið inn bankareiknings upplýsingar &mdash;, þar á meðal alþjóðlegt bankanúmer (IBAN) og SWIFT-kóða &mdash; á spjald lánardrottins. | [Setja upp bankareikninga lánardrottins](purchasing-how-set-up-vendors-bank-accounts.md) |
| Setja upp innkaupaaðila, úthluta þeim lánardrottnum og kóðum til að rekja talnagögn. |[Setja upp kaupendur](purchasing-how-setup-purchasers.md) |
| Færa inn mismunandi afslætti og sérverð birgja sem þú styrkir eftir vöru, magni og/eða dagsetningu. |[Skráning innkaupaverðs, afsláttar og greiðslusamkomulags](purchasing-how-record-purchase-price-discount-payment-agreements.md) |
| Skilgreinið hvað greitt er fyrir vörur og þjónustu sem fyrirtækið kaupir.  | [Setja upp verð og afslætti](across-prices-and-discounts.md) |
| Stofna staðlaðar línur til að setja inn í ítrekunarinnkaupaskjöl. | [Setja upp endurteknar innkaupalínur](purchasing-how-work-recurring-purchase-lines.md) |
| Stofna röð verka til að tengja vinnslur sem framkvæmdar eru af mismunandi notendum, svo sem að biðja um og samþykkja innkaupapantanir. | [Setja upp verkflæði fyrir Innkaupasamþykkt](across-set-up-workflows.md) |
| Stjórna samskiptum fyrirtækja við lánardrottna, flytja inn móttekin reikningsskjöl og skrá nýja birgja með Outlook email biðlara. | [Setja upp Viðskiptaaðalinnbót í Outlook](admin-outlook.md) |
| Fara yfir kostnaðarinnhreyfingar, umbreyta pappír og rafræn skjöl í færslubókarlínur og digitalize pappírsreikninga frá lánardrottnum. | [Setja upp skjöl á innleið](across-how-setup-income-documents.md) |
| Tilgreina sjálfgefnar skýrslur sem á að nota fyrir mismunandi skjalagerðir. |[Skýrsluval í Business Central](across-report-selections.md)|

## <a name="see-related-training-at-microsoft-learn"></a>Sjá tengdar þjálfun kl [Microsoft Learn](/learn/paths/trade-get-started-dynamics-365-business-central/).

## <a name="see-also"></a>Sjá einnig .

[Innkaup](purchasing-manage-purchasing.md)  
[Setja upp Yfirlit](setup.md)  
[Vinna með[!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
