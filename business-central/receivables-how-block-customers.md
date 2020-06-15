---
title: Hvernig á að loka fyrir sölu til viðskiptamanna
description: Ef þörf er á er hægt að útiloka að viðskiptavinur sé hafður með í söluskjölum og öðrum sölufærslum.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 7cc82ab0aaf28b355117571d0d2cc5869141693f
ms.sourcegitcommit: 4545bb597dd9dc4c563b30af762977ee1d815497
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/29/2020
ms.locfileid: "3410717"
---
# <a name="block-customers"></a>Loka á viðskiptamenn
Hægt er að loka á viðskiptamann, til dæmis vegna gjaldþrota, svo að ekki sé hægt að bæta viðskiptamanninum við söluskjöl eða svo að ekki sé hægt að bóka færslur fyrir viðskiptamanninn.

Auk þess að loka á viðskitamenn er hægt að stilla viðskiptakröfur fyrir viðskiptamanninn í bið í tengslum við áminningar. Nánari upplýsingar er að finna í [Innheimta útistandandi skuldir](receivables-collect-outstanding-balances.md).   

Eftirfarandi tafla lýsir valkostunum fyrir lokun á viðskiptavini.  

|Valkostur|Description|  
|--------------------|------------|  
|**Autt**|Viðskipti eru leyfð fyrir þennan viðskiptamann.|
|**Afhenda**|Ekki er hægt að stofna nýjar pantanir og nýjar afhendingar fyrir þennan viðskiptamann. Hægt er að reikningsfæra fyrirliggjandi óreikningsfærðar afhendingar.|  
|**Reikningsfæra**|Ekki er hægt að stofna nýjar pantanir, nýjar afhendingar og nýja reikninga fyrir þennan viðskiptamann. Ekki er hægt að reikningsfæra fyrirliggjandi óreikningsfærðar afhendingar. Enn er hægt að senda innheimtubréf og vaxtareikninga til viðskiptavinarins.|  
|**Allt**|Engar færslur eru leyfðar fyrir þennan viðskiptamann, þ.m.t. greiðslur.|  

## <a name="to-block-a-customer"></a>Til að loka á viðskiptamann  
1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Viðskiptamenn** og veldu síðan tengda tengilinn.
2. Veldu viðskiptamann og síðan aðgerðina **Breyta**.
3. Í reitnum **Lokað** skal velja hverju á að loka, eins og lýst er í töflunni hér að ofan.

## <a name="see-also"></a>Sjá einnig  
[Skrá nýja viðskiptamenn](sales-how-register-new-customers.md)  
[Innheimta útistandandi skuldir](receivables-collect-outstanding-balances.md)  
[Stjórnun skulda](receivables-manage-receivables.md)  
