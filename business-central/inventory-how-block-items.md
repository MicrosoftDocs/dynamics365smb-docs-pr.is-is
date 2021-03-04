---
title: Hvernig á að loka á vörur í sölum eða innkaupum
description: Hægt er að koma í veg fyrir að vara sé notuð, t.d. í sölu- eða innkaupaskjölum.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: f958600a47daa12a665975d6c41e214fca7cf5ad
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/01/2020
ms.locfileid: "3914091"
---
# <a name="block-items-from-sales-or-purchasing"></a>Loka á vörur í sölum eða innkaupum
Hægt er að loka á vöru svo hún verði ekki slegin inn í línur í innkaupa- eða söluskjölum og hægt er að loka á að hún verði bókuð í færslu. Til dæmis er þetta gagnlegt þegar vara er með þekktan galla. Ef einhver velur lokaða vöru á sölu- eða innkaupaskjali birtast skilaboð um að varan sé læst.

Eftirfarandi tafla sýnir hvað gerist þegar vörum er lokað.  

|Valkostur|Description|  
|--------------------|------------|  
|**Lokað fyrir sölu**|Ekki er hægt að slá vöruna inn í söluskjal eða færslubók söluvöru.|  
|**Lokað fyrir innkaup**|Ekki er hægt að slá vöruna inn í innkaupaskjal eða færslubók innkaupavöru, eða í innkaupaáætlunarferli.|  
|**Lokað**|Ekki er hægt að nota vöruna fyrir vörufærslu.|  

> [!NOTE]
> Hægt er að skila útilokuðum vörum. Þetta þýðir að engar ofangreindra stillinga gilda þegar varan er notuð fyrir skilapantanir og kreditreikninga.

Þegar þú notar aðgerðina **Afrita úr fylgiskjali** til að búa til ný skjöl sem byggjast á fyrirliggjandi skjölum færðu tilkynningu ef einhver atriði í upprunaskjalslínum eru lokuð. Útilokaðar fylgiskjalslínur eru ekki í nýja skjalinu og tilkynning sýnir yfirlit yfir allar fylgiskjalalínur sem eru útilokaðar í upprunaskjalinu.

## <a name="to-block-an-item-from-being-entered-on-sales-lines"></a>Til að loka á vöru svo hún verði ekki slegin inn í sölulínur  
1.  Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Vara** og veldu síðan tengda tengilinn.  
2.  Velja skal vöruna sem á að loka á og síðan velja gátreitinn **Sölur lokaðar** .  

## <a name="to-block-an-item-from-being-entered-on-purchase-lines"></a>Til að loka á vöru svo hún verði ekki slegin inn í innkaupalínur  
1.  Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Vara** og veldu síðan tengda tengilinn.  
2.  Velja skal vöruna sem á að loka á og síðan velja gátreitinn **innkaup lokuð** .  

## <a name="to-block-an-item-from-being-posted"></a>Til að loka á vöru svo hún verði ekki bókuð
1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Vara** og veldu síðan tengda tengilinn.
2. Velja skal vöruna sem á að loka á og síðan velja gátreitinn **lokað** .

## <a name="see-also"></a>Sjá einnig  
[Skrá nýjar vörur](inventory-how-register-new-items.md)  
[Birgðir](inventory-manage-inventory.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]