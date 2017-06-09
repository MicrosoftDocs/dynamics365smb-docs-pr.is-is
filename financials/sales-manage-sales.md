---
title: Sala | Microsoft Docs
description: "Lýsir því hvernig sölurverkþættir er stjórnað."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: trade, sell
ms.date: 04/27/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: d8b73dcf1ee000bd13aec200c82275eb3c0f9d1d
ms.contentlocale: is-is
ms.lasthandoff: 05/04/2017


---
# <a name="sales"></a>Sala
Búinn er til sölureikningur eða sölupöntun til að skrá samkomulag við viðskiptamann um að selja tilteknar vörur með tilteknum afhendingar- og greiðsluskilmálum.

Sölupantanir þarf að nota ef söluferlið krefst þess að hægt að afhenda hluta magns pöntunar, til dæmis þar sem allt magnið er ekki tiltækt í einu. Ef vara er seld með því að afhenda beint frá lánardrottni til viðskiptamanns, sem bein sending þarf að einnig nota sölupantanir. Frá öllum sjónarhornum séð virka sölupantanir á sama hátt og sölureikningar.

Góðar sölu- og markaðssetningaraðferðir snúast um að taka réttar ákvarðanir á réttum tíma. Markaðsvirknin í [!INCLUDE[d365fin](includes/d365fin_md.md)] veitir nákvæma og tímabæra yfirsýn yfir upplýsingar um tengiliði þína svo að þú getir þjónað væntanlegum viðskiptavinum þínum á skilvirkan hátt og aukið ánægju viðskiptavina. Nánari upplýsingar eru í [Tengslastjórnun](marketing-relationship-management.md).

Hægt er að semja við viðskiptamanninn með því að gera fyrst sölutilboð, sem hægt er að breyta í sölureikning þegar samkomulag hefur náðst um söluna. Þegar viðskiptamaðurinn hefur staðfest samninginn, til dæmis eftir tilboðsferli, geturðu sent staðfestingu pöntunar til að skrá afhendindingarskyldu vörunnar, eins og um var samið.

Þegar vörur eru afhentar, að fullu eða hluta, er sölureikningurinn eða sölupöntunin bókuð sem afhentar eða sem afhentar og reikningsfærðar til að stofna tengdar færslur vöru- og viðskiptamannabókar í kerfinu.

Í viðskiptaumhverfi þar sem viðskiptamaðurinn verður að greiða áður en vörur eru afhentar, til dæmis í smásölu, verður að bíða eftir greiðslukvittun fyrir vörunum áður en þær eru afhentar. Í flestum tilfellum er valið að vinna  greiðslur á innleið nokkrum vikum eftir afhendingu með því að jafna greiðslurnar við viðkomandi bókaða, ógreidda sölureikninga. Frekari upplýsingar eru í [hvernig á að afstemma greiðslur með því að nota sjálfvirka jöfnun](receivables-how-reconcile-payments-auto-application.md)

Auðvelt er að leiðrétta eða afturkalla bókaðann sölureikning áður en hann er greiddur. Þetta er gagnlegt þegar leiðrétta á mistök eða þegar viðskiptamaðurinn biður um breytingu snemma í pöntunarferlinu. Ef bókaður sölureikningur er greiddur, verður að búa til sölukreditreikning til að afturkalla söluna.

Hægt er að senda söluskjöl sem PDF skrár tengdar við tölvupóst. Meginmál tölvupóstins mun innihalda útdrátt úr söluskjalinu, svo sem vörur, heildarupphæð og tengil á vefsvæði PayPal. Nánari upplýsingar sjá [Hvernig á að: Senda Skjöl með Tölvupóst](ui-how-send-documents-email.md).

Fyrir öll söluferli er hægt að setja inn verkflæði samþykktar, til dæmis þannig að krafist sé þess að stórar sölur til ákveðinna viðskiptamanna þurfi samþykki aðalbókara. Nánari upplýsingar sjá [nota samþykktarverkflæði](across-how-use-approval-workflows.md).

Eftirfarandi tafla lýsir röð verkefna með tenglum í efnisatriði þar sem þeim er lýst.

| Til | Sjá |
| --- | --- |
| Stofna sölutilboð þar sem boðið er upp á vörur með umsemjanlegum skilmálum áður en tilboðinu er breytt í sölureikning. |[Hvernig á að: Gera tilboð](sales-how-make-offers.md) |
| Stofna sölureikning til að skrá samkomulag við viðskiptamann um að selja vörur með tilteknum afhendingar- og greiðsluskilmálum. |[Hvernig er reikningsfært](sales-how-invoice-sales.md) |
| Vinna sölupöntun sem felur í sér sendingu eða beina sendingu. |[Hvernig á að: Selja vörur](sales-how-sell-products.md) |
| Tengja sölupöntun við innkaupapöntun til að selja vöru beinnar afhendingar vara sem verður afhent beint frá lánardrottni til viðskiptamanns þíns. |[Hvernig á að: Gera beinar afhendingar](sales-how-drop-shipment.md) |
| Notið aðgerð á ógreiddum bókuðum sölureikningi til að stofna sjálfvirkt kreditreikningsferli og annaðhvort afturkalla sölureikninginn eða endurskapa hann til að gera leiðréttingar. |[Ógreiddir sölureikningar leiðréttir eða afturkallaðir](sales-how-correct-cancel-sales-invoice.md) |
| Stofna sölukreditreikning til þess að bakfæra tiltekinn bókaðan sölureikning til að endurspegla hvaða vörur viðskiptamaðurinn skilar og hvað upphæð þarf að endurgreiða. |[Meðhöndlun söluvöruskila eða afturkallana](sales-how-process-sales-returns-cancellations.md) |
| Stofna viðskiptamannaspjald fyrir alla viðskiptamenn sem selt er til. |[Hvernig á að Skrá nýja viðskiptamenn](sales-how-register-new-customers.md) |

## <a name="see-also"></a>Sjá einnig
[Uppsetning sölu](sales-setup-sales.md)  
[Stjórnun skulda](receivables-manage-receivables.md)  
[Stjórna skuldum](payables-manage-payables.MD)  
[Verkefnastjórnun](projects-manage-projects.md)    
[Aðfangakeðja](madeira-supply-chain.md)      
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Almenn viðskiptavirkni](ui-across-business-areas.md)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]
