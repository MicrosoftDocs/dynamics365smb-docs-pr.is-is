---
title: Hvernig á að leiðrétta fyrirframgreiðslu | Microsoft Docs
description: Hægt er að gera leiðréttingu á pöntun eftir að búið er að bóka fyrirframgreiðslureikning fyrir pöntunina. Hægt er að bæta nýjum línum við pöntun eftir að búið er að senda fyrirframgreiðslu og bóka síðan annan fyrirframgreiddan reikning en ekki er unnt að eyða línu í pöntun eftir fyrirframgreiðsla hefur verið reikningsfærð fyrir línu.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 0ed9bed71ca73e25197869f1f670251ae523648c
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5783535"
---
# <a name="correct-prepayments"></a>Leiðrétta fyrirframgreiðslur

Hægt er að gera leiðréttingu á pöntun eftir að búið er að bóka fyrirframgreiðslureikning fyrir pöntunina. Hægt er að bæta nýjum línum við pöntun eftir að búið er að senda fyrirframgreiðslu og bóka síðan annan fyrirframgreiddan reikning en ekki er unnt að eyða línu í pöntun eftir fyrirframgreiðsla hefur verið reikningsfærð fyrir línu.  

> [!TIP]
> Ef búið er að bóka fyrirframgreiðslureikning fyrir sölureikning sem þá þú leiðréttir svo eða hættir við verður einnig að leiðrétta eða hætta við fyrirframgreiðsluna.

## <a name="to-correct-a-prepayment"></a>Til að leiðrétta fyrirframgreiðslu:

Eftirfarandi ferli sýnir hvernig gefa skal út kreditreikning fyrirframgreiðslu til að afturkalla allar reikningsfærðar fyrirframgreiðslur fyrir sölupöntun.  

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Sölupantanir** og veldu síðan tengda tengilinn.  
2. Viðeigandi sölupöntun er opnuð.
3. Veljið aðgerðina **Fyrirframgreiðsla** og síðan aðgerðina **Bóka kreditreikning fyrirframgreiðslu** eða **Bóka og prenta kr.reikn. fyrirframgr.** aðgerðina.  
4. Á síðunni **Kreditreikningur sölu** skal farið í leiðréttingu viðeigandi færslna, sem og alla kreditreikninga sölu. Fyrir frekar upplýsingar, sjá [Meðhöndlun söluvöruskila eða afturkallana](sales-how-process-sales-returns-cancellations.md).  

    > [!NOTE]  
    > Til að lækka upphæðina í reitnum **Upphæð línu**, verður fyrst að auka fyrirframgreiðsluprósentuna í línunni svo gildið í reitnum **fyrirfrgr. línuupphæð** sé ekki lækkuð niður fyrir gildið í reitnum **fyrirfrg. reikningsupphæð**.

5. Til að gera fyrirframgreiðslureikning fyrir nýjar línur í sölukreditreikningi, veljið aðgerðina **Fyrirframgreiðsla** og síðan aðgerðina **Bóka reikning fyrirframgreiðslu** eða **Bóka og prenta reikn. fyrirframgr.** aðgerðina.  
6. Til að gefa út auka fyrirframgreiðslureikning, skal hækka upphæð fyrirframgreiðslu í einni eða fleiri línum og bóka fyrirframgreiðslureikninginn. Nýr reikningur er stofnaður fyrir mismuninn á milli reikningsfærðra upphæða fyrirframgreiðslu og nýju fyrirframgreiðsluupphæðanna.  

## <a name="see-also"></a>Sjá einnig

[Reikningsfærsla fyrirframgreiðslna](finance-invoice-prepayments.md)  
[Kynning: Uppsetning og reikningsfærsla fyrirframgreiðslna fyrir sölu](walkthrough-setting-up-and-invoicing-sales-prepayments.md)  
[Fjármál](finance.md)  
[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]