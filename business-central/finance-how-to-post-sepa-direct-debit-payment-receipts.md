---
title: Bóka SEPA-beingreiðslur | Microsoft Docs
description: Þegar innheimta beingreiðslu er meðhöndluð af bankanum er hægt að bóka kvittanir greiðslunnar fyrir sölureikninganna.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
redirect_url: finance-collect-payments-with-sepa-direct-debit
ms.openlocfilehash: c75f68ddc4112c5956b175162687737464454c45
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/01/2019
ms.locfileid: "2302074"
---
# <a name="post-sepa-direct-debit-payment-receipts"></a>Bóka SEPA-greiðslukvittanir beingreiðslna
Þegar innheimta beingreiðslu er meðhöndluð af bankanum er hægt að bóka kvittanir greiðslunnar fyrir sölureikninganna. Frekari upplýsingar, sjá [Stofna SEPA-innheimtufærslur fyrir beingreiðslur og flytja út í bankaskrá](finance-how-create-sepa-direct-debit-collection-entries-export-bank-file.md).  

Hægt að bóka greiðslukvittunina beint af síðunni **Innheimta fyrir beingreiðslur** eða af síðunni **Innheimtufærslur fyrir beingreiðslur**. Einnig er hægt að færa verkið á annan notanda með því að undirbúa tengdar færslubókarlínur.  

## <a name="to-post-a-direct-debit-payment-receipt-from-the-direct-debit-collections-page"></a>Bóka greiðslukvittun beingreiðslu af síðunni Innheimta beingreiðslur  
1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **innheimta beingreiðslu** og veldu síðan tengda tengilinn.  
2. Veljið línu fyrir innheimtu beingreiðslu sem hefur verið flutt út í bankaskrá og meðhöndluð af bankanum. Frekari upplýsingar, sjá [Stofna SEPA-innheimtufærslur fyrir beingreiðslur og flytja út í bankaskrá](finance-how-create-sepa-direct-debit-collection-entries-export-bank-file.md).  
3. Valið er **bóka greiðslukvittanir** aðgerð.  
4. Á síðunni **bóka innheimtu beingreiðslu** þarf að fylla reitina út eins og lýst er í eftirfarandi töflu.  

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
