---
title: "Yfirlit yfir umsjónarverkhluta innkaupa | Microsoft Docs"
description: "Útskýrir verkhluta sem felur í sér umsjón innkaupa þinna og innkaupaferla, þar með talið hvernig innkaupareikningar og innkaupapantanir virka."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: procurement, supply, vendor order
ms.date: 11/15/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 67400e424305cc705db5c1bd52a8e4de17ecc5a9
ms.openlocfilehash: 87e3d134abe82e0f55acf4d3680b84fbc2c0c14b
ms.contentlocale: is-is
ms.lasthandoff: 11/20/2018

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
| Notið aðgerð á ógreiddum bókuðum innkaupareikningi til að stofna sjálfvirkt kreditreikningsferli og annaðhvort afturkalla innkaupareikninginn eða endurskapa hann til að gera leiðréttingar. |[Ógreiddir sölureikningar leiðréttir eða afturkallaðir](purchasing-how-correct-cancel-unpaid-purchase-invoices.md) |
| Stofna innkaupakreiditreikning til þess að bakfæra tiltekinn bókaðan innkaupareikning til að endurspegla hvaða vörum er skilað til lánardrottins og hvað greiðsluupphæð fæst. |[Meðhöndlun innkaupaskila eða afturkallana](purchasing-how-register-new-vendors.md) |
|Undirbúðu þig fyrir að reikningsfæra fjölda móttökukvittana frá sama lánardrottni með því að sameina móttökukvittanirnar á einn reikning.|[Sameina móttökur í einn reikning](purchasing-how-to-combine-receipts.md)|
|Umbreyttu til dæmis rafrænum reikningum frá lánardrottnum þínum í innkaupareikninga í Business Central.|[Taka við og umbreyta rafræn skjölum](purchasing-how-to-receive-and-convert-electronic-documents.md)|
| Læra hvernig [!INCLUDE[d365fin](includes/d365fin_md.md)] reiknar hvenær verður að panta vöru til að geta fengið hana á tilteknum degi.|[Dagsetning útreiknings fyrir kaup.](purchasing-date-calculation-for-purchases.md)|

## <a name="see-also"></a>Sjá einnig
[Uppsetning innkaupa](purchasing-setup-purchasing.md)  
[Skráning nýrra lánardrottna](purchasing-how-register-new-vendors.md)  
[Stjórna skuldum](payables-manage-payables.md)  
[Stjórna verkum](projects-manage-projects.md)    
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Almenn viðskiptavirkni](ui-across-business-areas.md)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  

