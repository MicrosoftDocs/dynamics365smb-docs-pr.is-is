---
title: "Bóka SEPA-beingreiðslur | Microsoft Docs"
description: "Þegar innheimta beingreiðslu er meðhöndluð af bankanum er hægt að bóka kvittanir greiðslunnar fyrir sölureikninganna."
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/21/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 0031017c96172dca76b50542e52c6a437c01427a
ms.contentlocale: is-is
ms.lasthandoff: 03/22/2018

---
# <a name="post-sepa-direct-debit-payment-receipts"></a>Bóka SEPA-greiðslukvittanir beingreiðslna
Þegar innheimta beingreiðslu er meðhöndluð af bankanum er hægt að bóka kvittanir greiðslunnar fyrir sölureikninganna. Frekari upplýsingar, sjá [Stofna SEPA-innheimtufærslur fyrir beingreiðslur og flytja út í bankaskrá](finance-how-create-sepa-direct-debit-collection-entries-export-bank-file.md).  

Hægt að bóka greiðslukvittunina beint úr **Innheimta fyrir beingreiðslur** glugganum, eða **Innheimtufærslur fyrir beingreiðslur** glugganum. Einnig er hægt að færa verkið á annan notanda með því að undirbúa tengdar færslubókarlínur.  

## <a name="to-post-a-direct-debit-payment-receipt-from-the-direct-debit-collections-window"></a>Bóka greiðslukvittun beingreiðslu úr glugganum Innheimta beingreiðslur  
1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Bein skuldfærsla** og velja svo viðeigandi tengil.  
2. Veljið línu fyrir innheimtu beingreiðslu sem hefur verið flutt út í bankaskrá og meðhöndluð af bankanum. Frekari upplýsingar, sjá [Stofna SEPA-innheimtufærslur fyrir beingreiðslur og flytja út í bankaskrá](finance-how-create-sepa-direct-debit-collection-entries-export-bank-file.md).  
3. Valið er **bóka greiðslukvittanir** aðgerð.  
4. Í glugganum **bóka innheimtu beingreiðslu** þarf að fylla reitina út eins og lýst er í eftirfarandi töflu.  

    |Svæði|Description|  
    |---------------------------------|---------------------------------------|  
    |**Númer innheimtu með beinni skuldfærslu**|Tilgreina innheimtu beingreiðslu sem á að bóka greiðslukvittun fyrir.|  
    |**Sniðmát almennrar færslubókar**|Tilgreina hvaða sniðmát almennrar færslubókar á að nota til að bóka greiðslukvittun, svo sem sniðmát fyrir inngreiðslur.|  
    |**Heiti færslubókarkeyrslu**|Tilgreina hvaða færslubókarkeyrslu á að nota til að bóka greiðslukvittun.|  
    |**Stofna aðeins færslubók**|Veljið þennan gátreit ef ekki á að bóka greiðslukvittunina þegar **Í lagi** hnappurinn er valinn. Greiðslukvittunin verður undirbúin í tilgreindri færslubók og mun ekki vera bókuð fyrr en einhver bókar færslubókarlínurnar sem um ræðir.|  

5. Velja hnappinn **Í lagi**.  

## <a name="see-also"></a>Sjá einnig  
 [Innheimta greiðslur með SEPA-beingreiðslum](finance-collect-payments-with-sepa-direct-debit.md)   
 [Sala](sales-manage-sales.md)

