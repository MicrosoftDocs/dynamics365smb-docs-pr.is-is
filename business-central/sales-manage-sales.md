---
title: Yfirlit yfir verk sem stjórna á sölu
description: 'Lestu allt um hvernig á að nota þjónustu Business Central til að hafa umsjón með söluaðgerðum viðskiptamanna í sölureikningum, pöntunum, tilboðum og fleiru.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: overview
ms.search.keywords: 'trade, sell'
ms.search.form: '253,'
ms.date: 01/25/2024
ms.custom: bap-template
ms.service: dynamics-365-business-central
---

# Sölur

Búinn er til sölureikningur eða sölupöntun til að skrá samkomulag við viðskiptamann um að selja tilteknar vörur með tilteknum afhendingar- og greiðsluskilmálum.

Nota verður sölupantanir ef söluferlið krefst þess að varahlutir í pöntunarmagni séu afhentir, til dæmis vegna þess að allt magnið er ekki tiltækt strax. Ef vara er seld með því að afhenda beint frá lánardrottni til viðskiptamanns, sem bein sending þarf að einnig nota sölupantanir. Frá öllum sjónarhornum séð virka sölupantanir á sama hátt og sölureikningar. Með sölupöntunum, geturðu líka notað aðgerðina Pöntun lofað til að koma til skila ákveðnum afhendingardagsetningum til viðskiptamanna þinna.  

Hægt er að semja við viðskiptamanninn með því að gera fyrst sölutilboð, sem hægt er að breyta í sölureikning eða sölupöntun þegar samkomulag hefur náðst um söluna. Þegar viðskiptamaðurinn staðfestir samkomulagið er hægt að senda pöntunarstaðfestingu til að skrá skyldu þína til að afhenda vörurnar eins og samið hefur verið um.

Auðvelt er að leiðrétta eða hætta við bókaðan sölureikning áður en viðskiptamaður greiðir hann. Til dæmis til að leiðrétta mistök við innslætti eða ef viðskiptamaðurinn biður um breytingu snemma í pantanaferlinu. Ef bókaður sölureikningur er greiddur, verður að búa til sölukreditreikning eða söluvöruskilapöntun til að afturkalla söluna.

Góðar sölu- og markaðssetningaraðferðir snúast um að taka réttar ákvarðanir á réttum tíma. Markaðsvirknin í [!INCLUDE[prod_short](includes/prod_short.md)] veitir nákvæma og tímabæra yfirsýn yfir upplýsingar um tengiliði þína svo að þú getir þjónað væntanlegum viðskiptavinum þínum á skilvirkan hátt og aukið ánægju viðskiptavina. Frekari upplýsingar eru í [Tengslastjórnun](marketing-relationship-management.md).

Ef 365 Sala er notuð Microsoft Dynamics fyrir þátttöku viðskiptavina er hægt að njóta óaðfinnanlegrar samþættingar í ferlinu sem leiðir til sjóðs með því að nota [!INCLUDE [prod_short](includes/prod_short.md)] fyrir bakendaaðgerðir. Til dæmis til að vinna pantanir, vinna með birgðir og vinna úr fjármálum. Fræðast meira um notkun [Dynamics 365 Sales frá Business Central](marketing-integrate-dynamicscrm.md).

Í viðskiptaumhverfi þar sem viðskiptamaðurinn verður að greiða áður en vörur eru afhentar, til dæmis í smásölu, verður að bíða eftir greiðslukvittun fyrir vörunum áður en þær eru afhentar. Í flestum tilfellum er valið að vinna  greiðslur á innleið nokkrum vikum eftir afhendingu með því að jafna greiðslurnar við viðkomandi bókaða, ógreidda sölureikninga. Frekari upplýsingar eru í [Afstemma greiðslur með sjálfvirkri jöfnun](receivables-how-reconcile-payments-auto-application.md).

Hægt er að senda söluskjöl sem PDF skrár tengdar við tölvupóst. Meginmál tölvupóstsins inniheldur útdrátt úr söluskjalinu, svo sem vörur, heildarupphæð og tengil á PayPal síðuna. Frekari upplýsingar eru í [Senda skjöl í tölvupósti](ui-how-send-documents-email.md).

Í öllum söluferlum er hægt að fella samþykktarverkflæði inn. Til dæmis getur samþykktarverkflæði krafist þess að yfirmaður samþykki stóra sölu tiltekinna viðskiptamanna. Frekari upplýsingar má finna á [Nota verkflæði](across-use-workflows.md).

Eftirfarandi hlutar lýsa röð verka, með tenglum á greinar sem ná yfir þá.

## Hafist handa við sölugetu

Áður en selja á er tilgreint hvernig eigi að stýra söluferlum fyrirtækisins.

|Til...| Sjá |
|---|---|
| Stofnaðu viðskiptamannaspjald fyrir hvern viðskiptamann sem selt er til.|[Skrá nýja viðskiptamenn](sales-how-register-new-customers.md) |
| Setja upp hvernig sala er framkvæmd, t.d. verð og afsláttur, verð og afsláttarflokkar viðskiptamanna, sölumenn, afhendingarmátar og umboðsmenn. | [Uppsetning sölu](sales-setup-sales.md) |

## Greiningar á sölu

Í þessum hluta er lýst þeim greiningartólum sem hægt er að nota til að fá innsýn í sölugögnin.

| Til... | Sjá |
| --- | --- |
| Fræðast um getu til að greina sölugögn. | [Sölugreiningaryfirlit](sales-analytics-overview.md) |
| Gera tilfalallu greiningu á sölugögnum beint á listasíðum og fyrirspurnum. | [Búa til sölugreiningskýrslur](bi-how-create-analysis-views-reports.md) |
| Skoða innbyggðar söluskýrslur. | [Innbyggðar söluskýrslur](sales-reports.md) |

## Tilboð til pöntunar á sölureikning

Eftirfarandi tafla lýsir því hvernig á að nota einfalda söluferli.

|Til...| Sjá |
|---|---|
| Stofnaðu sölutilboð til að bjóða upp á vörur með umsemjanlegum skilmálum áður en tilboðinu er breytt í sölureikning. |[Gera sölutilboð](sales-how-make-offers.md) |
| Vinna sölupöntun (kannski með hlutaafhendingu eða með beinni afhendingu.) |[Selja vörur](sales-how-sell-products.md) |
| Búðu til sölureikning til að skrá samkomulag við viðskiptamann um að selja þeim tilteknar vörur með tilteknum afhendingar- og greiðsluskilmálum. |[Reikningsfæra sölur](sales-how-invoice-sales.md) |
|Það sem gerist þegar söluskjöl eru bókuð.|[Sölubókun](ui-post-sales.md)|

Ef þörf er á flóknari söluferlum birtast í eftirfarandi töflu greinar sem útskýra hvað er hægt að gera við [!INCLUDE[prod_short](includes/prod_short.md)].

|Til...| Sjá |
|---|---|
| Uppfylltu sölupöntun með mörgum hlutaafhendingum. | [Vinna úr hlutaafhendingum](sales-how-send-partial-shipments.md) |
| Setja upp staðlaðar innkaupa- og sölulínur sem þú getur fært á fljótlegan hátt inn í skjöl, til dæmis fyrir endurteknar áfyllingapantanir.|[Stofna ítrekaðar sölu- og innkaupalínur](sales-how-work-standard-lines.md)|  
|Stjórnaðu ráðstöfun viðskiptamanns til að kaupa inn mikið magn sem er afhent í nokkrum sendingum yfir tímabil.|[Vinna með standandi sölupantanir](sales-how-to-create-blanket-sales-orders.md)|
|Senda viðskiptamanni einn reikning fyrir margar afhendingar með því að sameina afhendingarnar í einn reikning.|[Sameina afhendingar einn reikning](sales-how-to-combine-shipments-on-a-single-invoice.md)|
|Selja samsetningarvörur sem eru ekki tiltækar eins og er með því að búa til tengda samsetningarpöntun. Samsetningarpöntunin getur útvegað fullt eða að hluta magn á sölupöntuninni.|[Selja hluti sem eru settir saman í pöntun](assembly-how-to-sell-items-assembled-to-order.md)|

## Tína og senda

Eftirfarandi tafla lýsir því hvernig á að tína vörur í sölupöntun og senda þær viðskiptamanni.

| Til | Sjá |
| --- | --- |
|Búðu þig undir að tína til vörur fyrir sendingu.|[Prenta tiltektarlistann](sales-how-print-picking-list.md)|
| Tengja sölupöntun við innkaupapöntun til að selja vöru beinnar afhendingar vara sem verður afhent beint frá lánardrottni til viðskiptamanns þíns. |[Beinar sendingar](sales-how-drop-shipment.md) |
|Láttu lánardrottinn afgreiða til þín vörulistaatriði í vöruhúsið svo þú getir afgreitt vöruna til viðskiptamannsins.|[Sérstakar pantanir stofnaðar](sales-how-to-create-special-orders.md)|
|Upplýsa viðskiptamenn þína um afhendingardag pöntunar með því að reikna út annað hvort hægt að lofa eða tiltækt að lofa dasetninguna.|[Reikna dagsetningar pöntunarloforða](sales-how-to-calculate-order-promising-dates.md)|
| Fræðast um hvernig rekja má sendingu frá bókuðum söluafhendingum. | [Finna sendingar](sales-how-track-packages.md) |

## Afturkallaðar pantanir, endurgreiðslur og skil

Eftirfarandi tafla lýsir því hvernig á að takast á við ógiltar pantanir, endurgreiðslur og vöruskil.

| Til | Sjá |
| --- | --- |
| Notið aðgerð á ógreiddum bókuðum sölureikningi til að stofna sjálfvirkt kreditreikningsferli og annaðhvort afturkalla sölureikninginn eða endurskapa hann til að gera leiðréttingar. |[Ógreiddir sölureikningar leiðréttir eða afturkallaðir](sales-how-correct-cancel-sales-invoice.md) |
| Stofna sölukreditreikning til að bakfæra tiltekinn bókaðan sölureikning til að endurspegla vörurnar sem viðskiptamaðurinn skilar og endurgreiðsluupphæðinni. |[Vinna söluskil eða afturkallanir](sales-how-process-sales-returns-cancellations.md) |

## Önnur ferli í sölu

Eftirfarandi tafla lýsir því hvernig á að takast á við önnur söluferli.

| Til | Sjá |
| --- | --- |
|Leysa úr misskilningi þegar tvær eða fleiri færslur eru til fyrir sama viðskiptamann.|[Sameina tvítekin atriði](sales-how-merge-duplicate-records.md)|

## Sjá einnig .

[Uppsetning sölu](sales-setup-sales.md)  
[Skrá nýja viðskiptamenn](sales-how-register-new-customers.md)  
[Yfirlit yfir sölugreiningar](sales-analytics-overview.md)   
[Stjórnun skulda](receivables-manage-receivables.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Almenn viðskiptavirkni](ui-across-business-areas.md)

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  

[!INCLUDE[footer-include](includes/footer-banner.md)]
