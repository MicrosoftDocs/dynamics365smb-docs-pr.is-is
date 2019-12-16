---
title: Hvernig á að loka á vörur í sölum eða innkaupum
description: Í Business Central getur vara verið merkt sem lokuð fyrir sölu, lokuð fyrir innkaupum eða lokuð fyrir allt.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 12/04/2019
ms.author: sgroespe
ms.openlocfilehash: 0218cf1b4982b9e8c5b5c2817590bc5ebd8f1941
ms.sourcegitcommit: b6e506a45a1cd632294bafa1c959746cc3a144f6
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/06/2019
ms.locfileid: "2896062"
---
# <a name="block-items-from-sales-or-purchasing"></a>Loka á vörur í sölum eða innkaupum
Hægt er að loka fyrir vöru svo hún verði ekki slegin inn í sölu- eða innkaupalínur og hægt er að loka á að hún verði bókuð í færslu.  

Eftirfarandi tafla sýnir hvað gerist þegar vörum er lokað.  

|Valkostur|Description|  
|--------------------|------------|  
|**Lokað fyrir sölu**|Ekki er hægt að slá vöruna inn í söluskjal eða færslubók söluvöru.|  
|**Lokað fyrir innkaup**|Ekki er hægt að slá vöruna inn í innkaupaskjal eða færslubók innkaupavöru, eða í innkaupaáætlunarferli.|  
|**Lokað**|Ekki er hægt að nota vöruna fyrir vörufærslu.|  

> [!NOTE]
> Hægt er að skila útilokuðum vörum. Þetta þýðir að engar ofangreindra stillinga gilda þegar varan er notuð fyrir skilapantanir og kreditreikninga.

Þegar þú notar aðgerðina **Afrita fylgiskjal** til að búa til ný skjöl sem byggjast á fyrirliggjandi skjölum færðu tilkynningu ef einhver atriði í upprunaskjalslínum eru lokuð. Útilokaðar fylgiskjalslínur eru ekki í nýja skjalinu og tilkynning sýnir yfirlit yfir allar fylgiskjalalínur sem eru útilokaðar í upprunaskjalinu.

## <a name="to-block-an-item-from-being-entered-on-sales-lines"></a>Til að loka á vöru svo hún verði ekki slegin inn í sölulínur  

1.  Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Vara** og veldu síðan tengda tengilinn.  
2.  Velja skal vöruna sem á að loka á og síðan velja gátreitinn **Sölur lokaðar**.  

Nú munu villuboð koma upp sem segja að lokað sé fyrir vöruna ef reynt er að slá hana inn í söluskjal eða færslubókarlínu.

## <a name="to-block-an-item-from-being-entered-on-purchase-lines"></a>Til að loka á vöru svo hún verði ekki slegin inn í innkaupalínur  

1.  Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Vara** og veldu síðan tengda tengilinn.  
2.  Velja skal vöruna sem á að loka á og síðan velja gátreitinn **innkaup lokuð**.  

Nú munu villuboð koma upp sem segja að lokað sé fyrir vöruna ef reynt er að slá hana inn í innkaupaskjal eða færslubókarlínu.

## <a name="to-block-an-item-from-being-posted"></a>Til að loka á vöru svo hún verði ekki bókuð
1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Vara** og veldu síðan tengda tengilinn.
2. Velja skal vöruna sem á að loka á og síðan velja gátreitinn **lokað**.

Nú munu villuboð koma upp sem segja að lokað sé fyrir vöruna ef reynt er að bóka einhverja færslu fyrir hana.

## <a name="see-also"></a>Sjá einnig  
[Skrá nýjar vörur](inventory-how-register-new-items.md)  
[Birgðir](inventory-manage-inventory.md)  
