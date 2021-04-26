---
title: Yfirlit yfir umsjónarverkhluta innkaupa | Microsoft Docs
description: Útskýrir verkhluta sem felur í sér umsjón innkaupa þinna og innkaupaferla, þar með talið hvernig innkaupareikningar og innkaupapantanir virka.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: procurement, supply, vendor order
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 0cc508d75aaf64a631de47af5c241cab2be3f334
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5772530"
---
# <a name="purchasing"></a>Innkaup
Innkaupareikningur eða innkaupapöntun er stofnaður til að skrá kostnaðarverð keyptra vara og til að rekja viðskiptaskuldir. Ef stjórna þarf birgðum eru innkaupareikningar líka notaðir til að uppfæra birgðastig gagnvirkt svo að hægt sé að lágmarka birgðakostnað og veita betri þjónustu við viðskiptavini. Innkaupakostnaður, að þjónustukostnaði meðtöldum, og birgðavirði sem leiðir af bókun innkaupareikninga verða hluti af framlegðartölum og öðrum fjárhagslegum afkastavísum í Mitt hlutverk.

Verður Að nota innkaupapantanir ef innkaupaferlið krefst þess að hægt sé að skrá hlutamóttökur pöntunarmagns , til dæmis þar sem allt magnið var ekki tiltæk í hjá lánardrottinn. Ef vara er seld með því að afhenda beint frá lánardrottni til viðskiptamanns, sem bein sending þarf að einnig nota innkaupapantanir. Frekari upplýsingar eru í [Beinar sendingar](sales-how-drop-shipment.md). Frá öllum sjónarhornum séð virka innkaupapantanir á sama hátt og innkaupareikningar.

Hægt er að láta innkaupareikninga stofnaðast sjálfkrafa með því að nota OCR þjónustu (stafakennsl, Optical Character Recognition) til að breyta PDF reikninga frá lánardrottnum í rafræn skjöl, sem síðan er breytt í innkaupareikninga með verkflæði. Til að nota þessa aðgerð, þarf fyrst að nýskrá sig í OCR þjónustu, og síðan framkvæma ýmiskonar uppsetningu. Nánari upplýsingar er að finna í [vinna skjöl á innleið](across-process-income-documents.md).      

Framleiðsluvörur geta bæði verið birgðavörur og þjónusta. Nánari upplýsingar eru í [Skrá nýjar vörur](inventory-how-register-new-items.md).

Fyrir öll innkaupaferli er hægt að setja inn verkflæði samþykktar, til dæmis þannig að krafist sé þess að stór innkaup þurfi samþykki aðalbókara. Nánari upplýsingar sjá [nota samþykktarverkflæði](across-how-use-approval-workflows.md).

Eftirfarandi tafla lýsir röð verkefna með tenglum í efnisatriði þar sem þeim er lýst.

| Til | Sjá |
| --- | --- |
| Stofna innkaupareikning til að skrá samkomulag við lánardrottinn um að kaupa vörur með tilteknum afhendingar- og greiðsluskilmálum. |[Skrá innkaup](purchasing-how-record-purchases.md) |
|Stofna innkaupabeiðni til að spegla beiðni um tilboð frá lánardrottni, sem þú getur síðar breytt yfir í innkaupapöntun.|[Biðja um tilboð](purchasing-how-request-quotes.md)|
| Stofna innkaupareikning fyrir allar eða valdar línur á sölureikningi. |[Kaupa vörur fyrir sölu](purchasing-how-purchase-products-sale.md) |
|Það sem gerist þegar innkaupaskjöl eru bókuð.|[Bókun innkaupa](ui-post-purchases.md)|
| Notið aðgerð á ógreiddum bókuðum innkaupareikningi til að stofna sjálfvirkt kreditreikningsferli og annaðhvort afturkalla innkaupareikninginn eða endurskapa hann til að gera leiðréttingar. |[Ógreiddir sölureikningar leiðréttir eða afturkallaðir](purchasing-how-correct-cancel-unpaid-purchase-invoices.md) |
| Stofna innkaupakreiditreikning til þess að bakfæra tiltekinn bókaðan innkaupareikning til að endurspegla hvaða vörum er skilað til lánardrottins og hvað greiðsluupphæð fæst. |[Meðhöndlun innkaupaskila eða afturkallana](purchasing-how-register-new-vendors.md) |
|Undirbúðu þig fyrir að reikningsfæra fjölda móttökukvittana frá sama lánardrottni með því að sameina móttökukvittanirnar á einn reikning.|[Sameina móttökur í einn reikning](purchasing-how-to-combine-receipts.md)|
|Umbreyttu til dæmis rafrænum reikningum frá lánardrottnum þínum í innkaupareikninga í Business Central.|[Taka við og umbreyta rafræn skjölum](purchasing-how-to-receive-and-convert-electronic-documents.md)|
| Læra hvernig [!INCLUDE[prod_short](includes/prod_short.md)] reiknar hvenær verður að panta vöru til að geta fengið hana á tilteknum degi.|[Dagsetning útreiknings fyrir kaup.](purchasing-date-calculation-for-purchases.md)|
|Leysa úr misskilningi þegar tvær eða fleiri færslur eru til fyrir sama lánardrottinn.|[Sameina tvítekin atriði](sales-how-merge-duplicate-records.md)|
|Stjórnaðu skuldbindingum þínum til lánardrottins til að kaupa inn mikið magn sem er afhent í nokkrum sendingum yfir tímabil.|[Vinna með standandi innkaupapantanir](sales-how-to-create-blanket-sales-orders.md)|

## <a name="see-related-training-at-microsoft-learn"></a>Sjá tengda þjálfun á [Microsoft Learn](/learn/paths/purchase-items-services-dynamics-365-business-central/)

## <a name="see-also"></a>Sjá einnig
[Uppsetning innkaupa](purchasing-setup-purchasing.md)  
[Skráning nýrra lánardrottna](purchasing-how-register-new-vendors.md)  
[Stjórna skuldum](payables-manage-payables.md)  
[Stjórna verkum](projects-manage-projects.md)    
[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Almenn viðskiptavirkni](ui-across-business-areas.md)

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]