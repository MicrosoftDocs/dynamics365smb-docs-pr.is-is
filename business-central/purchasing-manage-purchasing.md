---
title: Yfirlit yfir verk sem stjórna á innkaupum
description: 'Útskýrir verkhluta sem felur í sér umsjón innkaupa þinna og innkaupaferla, þar með talið hvernig innkaupareikningar og innkaupapantanir virka.'
author: brentholtorf
ms.topic: overview
ms.devlang: al
ms.search.keywords: 'procurement, supply, vendor order'
ms.search.form: '460, 9307'
ms.date: 03/21/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# <a name="purchasing"></a>Innkaup

Innkaupareikningur eða innkaupapöntun er stofnaður til að skrá kostnaðarverð keyptra vara og til að rekja viðskiptaskuldir. Ef stjórna þarf birgðum eru innkaupareikningar líka notaðir til að uppfæra birgðastig gagnvirkt svo að hægt sé að lágmarka birgðakostnað og veita betri þjónustu við viðskiptavini. Innkaupakostnaður, að þjónustukostnaði meðtöldum, og birgðavirði sem leiðir af bókun innkaupareikninga verða hluti af framlegðartölum og öðrum fjárhagslegum afkastavísum í Mitt hlutverk.

Nota verður innkaupapantanir ef innkaupaferlið krefst þess að skráðar séu hlutamóttökur af pöntunarmagni, til dæmis vegna þess að allt magnið var ekki tiltækt hjá lánardrottni. Ef vara er seld með því að afhenda beint frá lánardrottni til viðskiptamanns, sem bein sending þarf að einnig nota innkaupapantanir. Frekari upplýsingar eru í [Beinar sendingar](sales-how-drop-shipment.md). Frá öllum sjónarhornum séð virka innkaupapantanir á sama hátt og innkaupareikningar.

Hægt er að láta innkaupareikninga stofnaðast sjálfkrafa með því að nota OCR þjónustu (stafakennsl, Optical Character Recognition) til að breyta PDF reikninga frá lánardrottnum í rafræn skjöl, sem síðan er breytt í innkaupareikninga með verkflæði. Til að nota þessa aðgerð verður fyrst að skrá sig fyrir OCR-þjónustuna og framkvæma síðan ýmsar uppsetningar. Frekari upplýsingar eru í [Skjöl á innleið](across-income-documents.md).

Framleiðsluvörur geta bæði verið birgðavörur og þjónusta. Nánari upplýsingar eru í [Skrá nýjar vörur](inventory-how-register-new-items.md).

Fyrir öll innkaupaferli er hægt að setja inn verkflæði samþykktar, til dæmis þannig að krafist sé þess að stór innkaup þurfi samþykki aðalbókara. Frekari upplýsingar eru í [Nota verkflæði samþykktar](across-how-use-approval-workflows.md).

Eftirfarandi hlutar lýsa röð verka, með tenglum á greinar sem ná yfir þá.

## <a name="get-started-with-purchase-capabilities"></a>Hafist handa við innkaupagetu

Áður en vörur eru keyptar þarf að tilgreina hvernig stjórna eigi innkaupaferlum fyrirtækisins.

|Til...| Sjá |
|---|---|
| Grunnstilla reglur og gildi sem skilgreina innkaupastefnu fyrirtækisins. | [Setja upp innkaup](purchasing-setup-purchasing.md) |
| Skrá skal hvern lánardrottinn sem keypt er af með lánardrottnaspjaldi. | [Skrá nýja lánardrottna](purchasing-how-register-new-vendors.md) |

## <a name="purchase-analytics"></a>Innkaupagreiningar

Í þessum hluta er lýst þeim greiningartólum sem hægt er að nota til að fá innsýn í innkaupaferlið.

| Til... | Sjá |
| --- | --- |
| Fræðast um getu til að greina innkaupagögn. | [Greiningaryfirlit innkaupa](purchasing-analytics-overview.md) |
| Gera tilfalallu greiningu á innkaupagögnum beint á listasíðum og fyrirspurnum. | [Sérstök greining á innkaupagögnum](ad-hoc-analysis-purchasing.md) |
| Skoða innbyggðar innkaupaskýrslur. | [Innbyggðar innkaupaskýrslur](purchase-reports.md) |

## <a name="quote-to-order-to-purchase-invoice"></a>Tilboð til pöntunar á innkaupareikning

Eftirfarandi tafla lýsir því hvernig á að nota einfalda innkaupavinnslu.

| Til | Sjá |
| --- | --- |
|Stofna innkaupabeiðni til að spegla beiðni um tilboð frá lánardrottni, sem þú getur síðar breytt yfir í innkaupapöntun.|[Biðja um tilboð](purchasing-how-request-quotes.md)|
| Stofna innkaupareikning fyrir allar eða valdar línur á sölureikningi. |[Kaupa vörur fyrir sölu](purchasing-how-purchase-products-sale.md) |
| Stofna innkaupareikning til að skrá samkomulag við lánardrottinn um að kaupa vörur með tilteknum afhendingar- og greiðsluskilmálum. |[Skrá innkaup](purchasing-how-record-purchases.md) |
| Læra hvernig [!INCLUDE[prod_short](includes/prod_short.md)] reiknar hvenær verður að panta vöru til að geta fengið hana á tilteknum degi.|[Dagsetning útreiknings fyrir kaup](purchasing-date-calculation-for-purchases.md)|
|Það sem gerist þegar innkaupaskjöl eru bókuð.|[Bókun innkaupa](ui-post-purchases.md)|

Ef þörf er á flóknari innkaupaferlum birtir eftirfarandi tafla greinar sem útskýra hvað er hægt að gera við [!INCLUDE[prod_short](includes/prod_short.md)].

| Til | Sjá |
| --- | --- |
| Notið aðgerð á ógreiddum bókuðum innkaupareikningi til að stofna sjálfvirkt kreditreikningsferli og annaðhvort afturkalla innkaupareikninginn eða endurskapa hann til að gera leiðréttingar. |[Ógreiddir sölureikningar leiðréttir eða afturkallaðir](purchasing-how-correct-cancel-unpaid-purchase-invoices.md) |
| Búa til innkaupakreditreikning til að bakfæra tiltekinn bókaðan innkaupareikning til að endurspegla hvaða vörur þú ert að skila til lánardrottins og hvaða greiðsluupphæð þú innheimtir. |[Meðhöndlun innkaupaskila eða afturkallana](purchasing-how-process-purchase-returns-cancellations.md) |
|Stjórnaðu skuldbindingum þínum til lánardrottins til að kaupa inn mikið magn sem er afhent í nokkrum sendingum yfir tímabil.|[Vinna með standandi innkaupapantanir](sales-how-to-create-blanket-sales-orders.md)|


## <a name="canceled-orders-refunds-and-returns"></a>Afturkallaðar pantanir, endurgreiðslur og skil

Eftirfarandi tafla lýsir því hvernig á að takast á við ógiltar pantanir, endurgreiðslur og vöruskil sem keyptar eru.

| Til | Sjá |
| --- | --- |
|Undirbúðu þig fyrir að reikningsfæra fjölda móttökukvittana frá sama lánardrottni með því að sameina móttökukvittanirnar á einn reikning.|[Sameina móttökur í einn reikning](purchasing-how-to-combine-receipts.md)|
|Umbreyttu til dæmis rafrænum reikningum frá lánardrottnum þínum í innkaupareikninga í Business Central.|[Taka við og umbreyta rafræn skjölum](purchasing-how-to-receive-and-convert-electronic-documents.md)|


## <a name="other-processes-in-sales"></a>Önnur ferli í sölu

Eftirfarandi tafla lýsir því hvernig á að takast á við önnur innkaupaferli.

| Til | Sjá |
| --- | --- |
|Leysa úr misskilningi þegar tvær eða fleiri færslur eru til fyrir sama lánardrottinn.|[Sameina tvítekin atriði](sales-how-merge-duplicate-records.md)|


## <a name="external-document-numbers"></a>Númer ytri skjala

[!INCLUDE [ext-doc-no-purch](includes/ext-doc-no-purch.md)]

## <a name="see-also"></a>Sjá einnig .

[Uppsetning innkaupa](purchasing-setup-purchasing.md)  
[Skrá nýja lánardrottna](purchasing-how-register-new-vendors.md)  
[Yfirlit yfir innkaup greiningar](purchasing-analytics-overview.md)   
[Stjórna skuldum](payables-manage-payables.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Almenn viðskiptavirkni](ui-across-business-areas.md)

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]
