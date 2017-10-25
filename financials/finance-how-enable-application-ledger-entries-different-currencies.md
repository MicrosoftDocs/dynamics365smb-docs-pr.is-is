---
title: "Jafna færslur í mismunandi gjaldmiðlum| Microsoft Docs"
description: "Ef viðskiptamaður selur t.d. í einum gjaldmiðli og fær greitt í öðrum er hægt að jafna fjárhagsfærsluna í mismunandi gjaldmiðlum."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: multiple currencies, payment, reconcile
ms.date: 06/02/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 6379aea58ab7943b117e5b19b22f71193290c2cb
ms.contentlocale: is-is
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-enable-application-of-ledger-entries-in-different-currencies"></a>Hvernig á að: Leyfa jöfnun fjárhagsfærslna í mismunandi gjaldmiðlum
Ef keypt er af lánardrottni í einum gjaldmiðli og greitt í öðrum gjaldmiðli er hægt að jafna greiðsluna innkaupunum.

Á sama hátt, kaupi viðskiptamaður í einum gjaldmiðli og greiði í öðrum er hægt að jafna greiðsluna við sölureikninginn.

Eftirfarandi ferli sýnir hvernig á að setja þetta upp fyrir lánardrottnafærslur í glugganum **Uppsetning innkaupa og viðskiptaskulda**. Uppsetningin er svipuð og færslur í viðskiptamannabók í glugganum **Uppsetning sölu og viðskiptakrafna**.

> [!NOTE]  
>   Þessi virkni krefst þess að upplifun þín sé stillt á **Suite**. Nánari upplýsingar, sjá [Sérstilla þína [!INCLUDE[d365fin](includes/d365fin_md.md)] upplifun](ui-experiences.md).

## <a name="to-enable-application-of-vendor-ledger-entries-in-different-currencies"></a>Til að virkja jöfnun lánardrottnafærslna í mismunandi gjaldmiðlum
1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Uppsetning innkaupa og viðskiptaskulda** og velja svo viðeigandi tengil.
2. Í reitnum **Jöfnun milli gjaldmiðla** skal velja einn eftirtalinna valkosta.

| Valkostur | Lýsing |
| --- | --- |
| Engin |Jöfnun milli gjaldmiðla er ekki leyfð. |
| EMU |Jöfnun milli EMU-gjaldmiðla er leyfð. |
| Allt |Jöfnun milli allra gjaldmiðla er leyfð. |

## <a name="to-set-up-gl-accounts-for-currency-application-rounding-differences"></a>Uppsetning fjárhagsreikninga fyrir gjaldmiðilsaðgerð sléttunarmismunar  
Eigi að jafna færslur í mismunandi gjaldmiðlum þarf að setja upp fjárhagsreikninga þar sem á að bóka sléttunarmismun.  
  
> [!NOTE]  
>  Setja verður upp fjárhagsreikningana áður en lokið er við verkið. Frekari upplýsingar er að finna í [Að skilja fjárhag og bókhaldslykla](finance-general-ledger.md). 
  
1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn  **Bókunarflokkar viðskiptamanns** og velja svo viðeigandi tengil.  
2. Í reitunum **Debet gjaldm.jöfn.slétt.reikn** og **Kreditreikn. gjaldeyrisjöfn.** er fært inn viðkomandi fjárhagsreikningsnúmer til að bóka sléttunarmismun.  
3. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn  **Bókunarflokkar lánardrottna** og velja svo viðeigandi tengil.  
4. Í reitunum **Debet gjaldm.jöfn.slétt.reikn** og **Kreditreikn. gjaldeyrisjöfn.** er fært inn viðkomandi fjárhagsreikningsnúmer til að bóka sléttunarmismun.  

## <a name="see-also"></a>Sjá einnig
[Stjórna skuldum](payables-manage-payables.md)  
[Stjórnun skulda](receivables-manage-receivables.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

