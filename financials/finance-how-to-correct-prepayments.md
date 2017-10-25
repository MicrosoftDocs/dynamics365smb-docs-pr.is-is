---
title: "Hvernig á að leiðrétta fyrirframgreiðslu | Microsoft Docs"
description: "Hægt er að gera leiðréttingu á pöntun eftir að búið er að bóka fyrirframgreiðslureikning fyrir pöntunina. Hægt er að bæta nýjum línum við pöntun eftir að búið er að senda fyrirframgreiðslu og bóka síðan annan fyrirframgreiddan reikning en ekki er unnt að eyða línu í pöntun eftir fyrirframgreiðsla hefur verið reikningsfærð fyrir línu."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/04/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: b51fba1ee8c9a040836ac24c51f39a036f3c0e23
ms.contentlocale: is-is
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-correct-prepayments"></a>Hvernig á að leiðrétta fyrirframgreiðslu
Hægt er að gera leiðréttingu á pöntun eftir að búið er að bóka fyrirframgreiðslureikning fyrir pöntunina. Hægt er að bæta nýjum línum við pöntun eftir að búið er að senda fyrirframgreiðslu og bóka síðan annan fyrirframgreiddan reikning en ekki er unnt að eyða línu í pöntun eftir fyrirframgreiðsla hefur verið reikningsfærð fyrir línu.  

## <a name="to-correct-a-prepayment"></a>Til að leiðrétta fyrirframgreiðslu:
Eftirfarandi ferli sýnir hvernig gefa skal út kreditreikning fyrirframgreiðslu til að afturkalla allar reikningsfærðar fyrirframgreiðslur fyrir sölupöntun.  
1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn  **Sölupantanir** og velja svo viðeigandi tengil.  
2. Viðeigandi sölupöntun er opnuð.
3. Veljið aðgerðina **Fyrirframgreiðsla** og síðan aðgerðina **Bóka kreditreikning fyrirframgreiðslu** eða **Bóka og prenta kr.reikn. fyrirframgr.** aðgerðina.  
4. Í glugganum **Kreditreikningur sölu** skal farið í leiðréttingu viðeigandi færslna, sem og alla kreditreikninga sölu. Fyrir frekar upplýsingar, sjá [hvernig á að: Meðhöndlun söluvöruskila eða afturkallana](sales-how-process-sales-returns-cancellations.md)     

    > [!NOTE]  
    > Til að lækka upphæðina í reitnum **Upphæð línu**, verður fyrst að auka fyrirframgreiðsluprósentuna í línunni svo gildið í reitnum **fyrirfrgr. línuupphæð** sé ekki lækkuð niður fyrir gildið í reitnum **fyrirfrg. reikningsupphæð**.

5. Til að gera fyrirframgreiðslureikning fyrir nýjar línur í sölukreditreikningi, veljið aðgerðina **Fyrirframgreiðsla** og síðan aðgerðina **Bóka reikning fyrirframgreiðslu** eða **Bóka og prenta reikn. fyrirframgr.** aðgerðina.  
6. Til að gefa út auka fyrirframgreiðslureikning, skal hækka upphæð fyrirframgreiðslu í einni eða fleiri línum og bóka fyrirframgreiðslureikninginn. Nýr reikningur er stofnaður fyrir mismuninn á milli reikningsfærðra upphæða fyrirframgreiðslu og nýju fyrirframgreiðsluupphæðanna.  

## <a name="see-also"></a>Sjá einnig  
[Reikningsfærsla fyrirframgreiðslna](finance-invoice-prepayments.md)  
[Kynning: Uppsetning og reikningsfærsla fyrirframgreiðslna fyrir sölu](walkthrough-setting-up-and-invoicing-sales-prepayments.md)  
[Fjármál](finance.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

