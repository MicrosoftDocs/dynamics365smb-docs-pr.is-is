---
title: Jafna greiðslur við tengd fylgiskjöl og bóka þær| Microsoft Docs
description: Lýsir því hvernig á að skrá greiðslur sem þú greiðir lánardrottnum og endurgreiðslur sem þú greiðir viðskiptavinum.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment journal, print check, vendor payment, customer refund, creditor, debt, balance due, AP
ms.date: 10/01/2018
ms.author: edupont
ms.openlocfilehash: 7b3065dd0528588fec4c05e4e9c391a3beb1cc9a
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/08/2019
ms.locfileid: "800439"
---
# <a name="record-payments-and-refunds-in-the-payment-journal"></a>Skrá greiðslur og endurgreiðslur í greiðslubókina

Á síðunni **Greiðslubók** skráir þú greiðslur sem þú greiðir lánardrottnum og endurgreiðslur sem þú greiðir viðskiptavinum. Þegar þú bókar greiðslubókarlínu er greidda upphæðin skráð í tilgreindan bankareikning kerfisins. Þú verður þá að gera ráðstafanir til að framkvæma raunverulegu peningamillifærslu af tengdum bankareikningi.  

Greiðslubókin er færslubók sem er fínstillt til að framkvæma greiðlsur. Þú getur bætt við línum með skjótum hætti handvirkt, þú getur látið [!INCLUDE[d365fin](includes/d365fin_md.md)] stinga upp á lánardrottnagreiðslur, og þú getur jafnað greiðsluna á bókuð skjöl. Jafnvel þótt þú greiðir greiðslur, þá færirðu inn jákvæð upphæð í **Skjalaupphæð** reitinn. Það fer eftir gerð skjala fyrir færslubókarlínuna, þá er þetta upphæð breytt í neikvæð upphæð í undirliggjandi færslum. Þannig ertu fljótari að bæta við færslubókarlínum handvirkt. Ef þú vilt heldur færa inn neikvæðum upphæðum, getur þú sérsniðið greiðslubókina til að sýna **Upphæð** reitinn í staðinn.  

- Jafna greiðslur á reikninga eða kreditreikninga

    Ef þú fyllir út reitinn **Jöfnunarskjalsnúmer** með reikningnum eða kreditreikningnum sem þarf að greiða eða endurgreiða, þá er skjalið sem um ræðir sett til greiðslu þegar þú bókar færslubókina. Þetta kallast að vera „jafnað“. Í stað þess að framkvæma jöfnun við bókun á greiðslu geturðu notað síðuna **Jafna lánardr.færslur** og **Jafna viðskm.færslur** eftir að þú hefur framkvæmt bókun á greiðslu. Nánari upplýsingar má til dæmis finna í [Afstemma greiðslur lánardrottins við greiðslubók eða úr færslum í lánardrottnabók](payables-how-apply-purchase-transactions-manually.md).  

- Fáðu tillögur um greiðslur til lánardrottna eða starfsmanna

    The **Greiðslutillögur til lánardrottna** og **Greiðslutillögur til starfsmanna** aðgerðir geta hjálpað þér að fylla greiðslubókarlínur sjálfkrafa í samræmi við forgangsröðun lánardrottna og gjalddaga. Frekari upplýsingar er að finna í [Greiðslutillögur til lánardrottna](payables-how-suggest-vendor-payments.md). Með þessari aðgerð er reiturinn **Jöfnunarskjalsnúmer** alltaf fylltur út.  

- Prenta ávísanir og senda greiðslur rafrænt til bankans

    Til viðbótar við að skrá þig að greiðslan er hafi verið gerð, geturðu einnig notað síðuna **Greiðslubók** til að gera greiðsluna móttækilega fyrir frekari vinnslu hjá bankanum þínum. Frekari upplýsingar eru að finna í [Greiða greiðslu með ávísun](payables-how-work-checks.md) og [Greiða rafrænar greiðslur](payables-how-export-payments-bank-file.md).  

## <a name="to-make-payments-in-the-payment-journal"></a>Til að greiða í greiðslubók

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **greiðslubók** og veldu síðan tengda tengilinn.
2. Opnaðu bókarkeyrsluna sem er notuð fyrir greiðslur.
3. Ef þú veist hverjum á að borga eða endurgreiða skaltu fylla inn reitina handvirkt. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Til að einnig jafna greiðsluna við tengdan reikning eða kreditreikning skaltu velja **Jöfnunarskjalsnúmer**. reitinn á síðunni **Jafna lánardr.færslur**, velja viðeigandi reikning eða kreditreikning og síðan velja hnappinn **Í lagi**.

    Mörg reiti, svo sem **Skjalaupphæð** og **Gjalddagi** reitir, eru nú fylltir inn með upplýsingum úr völdu skjalinu.
5. Annar valkostur er að nota aðgerðina **Greiðslutillögur til lánardrottna**. Allar jöfnunarupplýsingar og upphæðir eru síðan einnig færðar inn í færslubókarlínur. Frekari upplýsingar er að finna í [Greiðslutillögur til lánardrottna](payables-how-suggest-vendor-payments.md).

    Skilaboð munu leiðbeina þér í að fylla út nauðsynlega reiti á réttan hátt.
6.  Þegar öllum greiðslubókarlínum er lokið skal velja aðgerðina **Bóka**.

## <a name="see-also"></a>Sjá einnig
[Framkvæma ávísanagreiðslur](payables-how-work-checks.md)  
[Framkvæma rafrænar greiðslur](payables-how-export-payments-bank-file.md)  
[Stjórna skuldum](payables-manage-payables.md)  
[Uppsetning bankaþjónustu](bank-setup-banking.md)  
[Flytja út jákvæða greiðsluskrá](finance-how-positive-pay.md)  
[Vinna í færslubókum](ui-work-general-journals.md)  
[Sérstillingar verksvæðis](ui-personalization-user.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
