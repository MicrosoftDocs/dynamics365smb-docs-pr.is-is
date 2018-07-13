---
title: "Yfirlit yfir umsjónarverkhluta sölu | Microsoft Docs"
description: "Lýsir því hvernig sölurverkþættir er stjórnað."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: trade, sell
ms.date: 09/08/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 046a42582dc66368fded90a4bb45add71a95d979
ms.openlocfilehash: 6351f2b8a79afa201192addc4960bda6d59448eb
ms.contentlocale: is-is
ms.lasthandoff: 07/02/2018

---
# <a name="sales"></a>Sala
Búinn er til sölureikningur eða sölupöntun til að skrá samkomulag við viðskiptamann um að selja tilteknar vörur með tilteknum afhendingar- og greiðsluskilmálum.

Sölupantanir þarf að nota ef söluferlið krefst þess að hægt að afhenda hluta magns pöntunar, til dæmis þar sem allt magnið er ekki tiltækt í einu. Ef vara er seld með því að afhenda beint frá lánardrottni til viðskiptamanns, sem bein sending þarf að einnig nota sölupantanir. Frá öllum sjónarhornum séð virka sölupantanir á sama hátt og sölureikningar. Með sölupöntunum, geturðu líka notað aðgerðina Pöntun lofað til að koma til skila ákveðnum afhendingardagsetningum til viðskiptamanna þinna.  

Hægt er að semja við viðskiptamanninn með því að gera fyrst sölutilboð, sem hægt er að breyta í sölureikning eða sölupöntun þegar samkomulag hefur náðst um söluna. Þegar viðskiptamaðurinn hefur staðfest samninginn, geturðu sent staðfestingu pöntunar til að skrá afhendingarskyldu vörunnar, eins og um var samið.

Auðvelt er að leiðrétta eða afturkalla bókaðann sölureikning áður en hann er greiddur. Þetta er gagnlegt þegar leiðrétta á mistök eða þegar viðskiptamaðurinn biður um breytingu snemma í pöntunarferlinu. Ef bókaður sölureikningur er greiddur, verður að búa til sölukreditreikning eða söluvöruskilapöntun til að afturkalla söluna.

Góðar sölu- og markaðssetningaraðferðir snúast um að taka réttar ákvarðanir á réttum tíma. Markaðsvirknin í [!INCLUDE[d365fin](includes/d365fin_md.md)] veitir nákvæma og tímabæra yfirsýn yfir upplýsingar um tengiliði þína svo að þú getir þjónað væntanlegum viðskiptavinum þínum á skilvirkan hátt og aukið ánægju viðskiptavina. Nánari upplýsingar eru í [Tengslastjórnun](marketing-relationship-management.md).

Í viðskiptaumhverfi þar sem viðskiptamaðurinn verður að greiða áður en vörur eru afhentar, til dæmis í smásölu, verður að bíða eftir greiðslukvittun fyrir vörunum áður en þær eru afhentar. Í flestum tilfellum er valið að vinna  greiðslur á innleið nokkrum vikum eftir afhendingu með því að jafna greiðslurnar við viðkomandi bókaða, ógreidda sölureikninga. Frekari upplýsingar eru í [afstemma greiðslur með því að nota sjálfvirk jöfnun](receivables-how-reconcile-payments-auto-application.md)

Hægt er að senda söluskjöl sem PDF skrár tengdar við tölvupóst. Meginmál tölvupóstins mun innihalda útdrátt úr söluskjalinu, svo sem vörur, heildarupphæð og tengil á vefsvæði PayPal. Frekari upplýsingar eru í [Senda skjöl í tölvupósti](ui-how-send-documents-email.md).

Fyrir öll söluferli er hægt að setja inn verkflæði samþykktar, til dæmis þannig að krafist sé þess að stórar sölur til ákveðinna viðskiptamanna þurfi samþykki aðalbókara. Frekari upplýsingar eru í [Nota verkflæði](across-use-workflows.md).

Eftirfarandi tafla lýsir röð verkefna með tenglum í efnisatriði þar sem þeim er lýst.

| Til | Sjá |
| --- | --- |
| Stofna sölutilboð þar sem boðið er upp á vörur með umsemjanlegum skilmálum áður en tilboðinu er breytt í sölureikning. |[Gera sölutilboð](sales-how-make-offers.md) |
| Stofna sölureikning til að skrá samkomulag við viðskiptamann um að selja vörur með tilteknum afhendingar- og greiðsluskilmálum. |[Reikningsfæra sölur](sales-how-invoice-sales.md) |
| Vinna sölupöntun sem felur í sér sendingu eða beina sendingu. |[Selja vörur](sales-how-sell-products.md) |
|Setja upp staðlaðar innkaupa- og sölulínur sem þú getur fært á fljótlegan hátt inn í skjöl, til dæmis fyrir endurteknar áfyllingapantanir.|[Stofna ítrekaðar sölu- og innkaupalínur](sales-how-work-standard-lines.md)|  
| Tengja sölupöntun við innkaupapöntun til að selja vöru beinnar afhendingar vara sem verður afhent beint frá lánardrottni til viðskiptamanns þíns. |[Beinar sendingar](sales-how-drop-shipment.md) |
|Láttu lánardrottinn afgreiða til þín utanbirgðavöru í vöruhúsið svo þú getir afgreitt vöruna til viðskiptamannsins.|[Sérstakar pantanir stofnaðar](sales-how-to-create-special-orders.md)|
| Notið aðgerð á ógreiddum bókuðum sölureikningi til að stofna sjálfvirkt kreditreikningsferli og annaðhvort afturkalla sölureikninginn eða endurskapa hann til að gera leiðréttingar. |[Ógreiddir sölureikningar leiðréttir eða afturkallaðir](sales-how-correct-cancel-sales-invoice.md) |
| Stofna sölukreditreikning til þess að bakfæra tiltekinn bókaðan sölureikning til að endurspegla hvaða vörur viðskiptamaðurinn skilar og hvað upphæð þarf að endurgreiða. |[Vinna söluskil eða afturkallanir](sales-how-process-sales-returns-cancellations.md) |
|Stjórnaðu ráðstöfun viðskiptamanns til að kaupa inn mikið magn sem er afhent í nokkrum sendingum yfir tímabil.|[Vinna með standandi sölupantanir](sales-how-to-create-blanket-sales-orders.md)|
|Selja samsetningarsett sem ekki eru tiltæk með því að búa til tengda samsetningarpöntun til að veita fullt magn eða hluta af magni sölupöntunar.|[Selja hluti sem eru settir saman í pöntun](assembly-how-to-sell-items-assembled-to-order.md)|
|Senda viðskiptamanni einn reikning fyrir margar afhendingar með því að sameina afhendingarnar í einn reikning.|[Sameina afhendingar einn reikning](sales-how-to-combine-shipments-on-a-single-invoice.md)|
|Upplýsa viðskiptamenn þína um afhendingardag pöntunar með því að reikna út annað hvort hægt að lofa eða tiltækt að lofa dasetninguna.|[Reikna dagsetningar pöntunarloforða](sales-how-to-calculate-order-promising-dates.md)|

## <a name="see-also"></a>Sjá einnig
[Uppsetning sölu](sales-setup-sales.md)  
[Skrá nýja viðskiptamenn](sales-how-register-new-customers.md)  
[Stjórnun skulda](receivables-manage-receivables.md)  
[Stjórna skuldum](payables-manage-payables.md)  
[Verkefnastjórnun](projects-manage-projects.md)    
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Almenn viðskiptavirkni](ui-across-business-areas.md)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
 

