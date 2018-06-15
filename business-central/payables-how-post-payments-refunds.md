---
title: "Jafna greiðslur við tengd fylgiskjöl og bóka þær| Microsoft Docs"
description: "Lýsir því hvernig á að skrá greiðslur sem þú greiðir lánardrottnum og endurgreiðslur sem þú greiðir viðskiptavinum."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment journal, print check, vendor payment, customer refund, creditor, debt, balance due, AP
ms.date: 04/30/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 75501b9402bb1c14fcfeb2fc6e61f055a2247493
ms.openlocfilehash: 3cad699234d95a849bf48f04c8462afa968789f6
ms.contentlocale: is-is
ms.lasthandoff: 05/15/2018

---
# <a name="record-payments-and-refunds"></a>Skrá greiðslur og endurgreiðslur
Í glugganum **Greiðslubók** skráir þú greiðslur sem þú greiðir lánardrottnum og endurgreiðslur sem þú greiðir viðskiptavinum. Þegar þú bókar greiðslubókarlínu er greidda upphæðin skráð í tilgreindan bankareikning kerfisins. Þú verður þá að gera ráðstafanir til að framkvæma raunverulegu peningamillifærslu af tengdum bankareikningi.

Ef þú fyllir út reitinn **Jöfnunarskjalsnúmer** með reikningnum eða kreditreikningnum sem þarf að greiða eða endurgreiða, þá er skjalið sem um ræðir sett til greiðslu þegar þú bókar færslubókina. Þetta kallast að vera „jafnað“. Í stað þess að framkvæma jöfnun við bókun á greiðslu geturðu notað gluggann **Jafna lánardr.færslur** og **Jafna viðskm.færslur** eftir að þú hefur framkvæmt bókun á greiðslu. Nánari upplýsingar má til dæmis finna í [Afstemma greiðslur lánardrottna handvirkt](payables-how-apply-purchase-transactions-manually.md).

Aðgerðin **Greiðslutillögur til lánardrottna** getur hjálpað þér að fylla út í greiðslubókarlínur sjálfvirkt samkvæmt forgangsröðun lánardrottins og gjalddögum. Frekari upplýsingar er að finna í [Greiðslutillögur til lánardrottna](payables-how-suggest-vendor-payments.md). Með þessari aðgerð er reiturinn **Jöfnunarskjalsnúmer** alltaf fylltur út.

Til viðbótar við að skrá þig að greiðslan er hafi verið gerð, geturðu einnig notað gluggann **Greiðslubók** til að gera greiðsluna móttækilega fyrir frekari vinnslu hjá bankanum þínum. Frekari upplýsingar eru að finna í [Greiða greiðslu með ávísun](payables-how-work-checks.md) og [Greiða rafrænar greiðslur](payables-how-export-payments-bank-file.md).  

1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **greiðslubækur** og velja svo viðeigandi tengil.
2. Opnaðu bókarkeyrsluna sem er notuð fyrir greiðslur.
3. Ef þú veist hverjum á að borga eða endurgreiða skaltu fylla inn reitina handvirkt. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Til að einnig jafna greiðsluna við tengdan reikning eða kreditreikning skaltu velja **Jöfnunarskjalsnúmer**. reitinn í glugganum **Jafna lánardr.færslur**, velja viðeigandi reikning eða kreditreikning og síðan velja hnappinn **Í lagi**.

    Margir reitir, svo sem reitirnir **Upphæð** og **Gjalddagi** eru nú fylltir inn með upplýsingum úr valda skjalinu.
5. Annar valkostur er að nota aðgerðina **Greiðslutillögur til lánardrottna**. Allar jöfnunarupplýsingar og upphæðir eru síðan einnig færðar inn í færslubókarlínur. Frekari upplýsingar er að finna í [Greiðslutillögur til lánardrottna](payables-how-suggest-vendor-payments.md).

    Skilaboð munu leiðbeina þér í að fylla út nauðsynlega reiti á réttan hátt.
6.  Þegar öllum greiðslubókarlínum er lokið skal velja aðgerðina **Bóka**.

## <a name="see-also"></a>Sjá einnig
[Framkvæma ávísanagreiðslur](payables-how-work-checks.md)  
[Framkvæma rafrænar greiðslur](payables-how-export-payments-bank-file.md)  
[Stjórna skuldum](payables-manage-payables.md)  
[Uppsetning bankaþjónustu](bank-setup-banking.md)  
[Flytja út jákvæða greiðsluskrá](finance-how-positive-pay.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

