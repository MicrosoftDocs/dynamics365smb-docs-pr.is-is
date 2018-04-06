---
title: "Hönnunarupplýsingar: Virk móti sögulegum vörurakningarfærslum | Microsoft Docs"
description: "Þegar hlutar skjalslínumagns eru bókaðir eraðeins þessi tiltekna magn flutt í birgðahöfuðbókarfærslur og vörurakningarnúmer þess. Hins vegar viltu fá aðgang að öllum viðeigandi vörurakningarupplýsingum beint úr virku skjalalínunni. Það er, ekki aðeins verður þú vilt sjá færslur sem tengjast eftirstandandi magni, þú munt einnig vilja upplýsingar um einingar sem hafa verið bókaðar. Þegar þú skoðar eða breytir glugganum **Vörurakningarlínur** er samtals innihald töflunnar**Vörurakningarlýsing** (T336) og töflunnar**Frátekningarfærsla** (T337) are sett fram í tímabundinni útgáfu af T336. Þetta tryggir heildaraðgang að fyrri og virkum vörurakningargögnum."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 34654f907759bc0bdfcb2fb2f1265a74cdcdce4f
ms.contentlocale: is-is
ms.lasthandoff: 03/22/2018

---
# <a name="design-details-active-versus-historic-item-tracking-entries"></a>Hönnunarupplýsingar: Virk móti sögulegum vörurakningarfærslum
Þegar hlutar skjalslínumagns eru bókaðir eraðeins þessi tiltekna magn flutt í birgðahöfuðbókarfærslur og vörurakningarnúmer þess. Hins vegar viltu fá aðgang að öllum viðeigandi vörurakningarupplýsingum beint úr virku skjalalínunni. Það er, ekki aðeins verður þú vilt sjá færslur sem tengjast eftirstandandi magni, þú munt einnig vilja upplýsingar um einingar sem hafa verið bókaðar. Þegar þú skoðar eða breytir glugganum **Vörurakningarlínur** er samtals innihald töflunnar**Vörurakningarlýsing** (T336) og töflunnar**Frátekningarfærsla** (T337) are sett fram í tímabundinni útgáfu af T336. Þetta tryggir heildaraðgang að fyrri og virkum vörurakningargögnum.  

 Eftirfarandi tafla sýnir hvernig T336 og T337 eru notuð í kaupatburðarás. Feitletruðu tölurnar tákna gildi sem notandinn færir handvirkt í gluggann **Vörurakningarlínur**.  

 Skref 1: Búa innkaupapöntunarlínu með sjö stykkjum með  vörurakningarnúmerum.  

||**Magn (stofn)**|**Magn til afgreiðslu**|**Magn til reikningsf. (stofn)**|**Afgreitt magn (stofn)**|**Reikningsfært magn (stofn)**|  
|-|----------------------------------------------|--------------------------------------------|------------------------------------------------------|-------------------------------------------------------|--------------------------------------------------------|  
|**T337**|7|0|0|0|0|  
|**T336**|0|0|0|0|0|  

 Skref 2: Fá fjögur stykki.  

||**Magn (stofn)**|**Magn til afgreiðslu**|**Magn til reikningsf. (stofn)**|**Afgreitt magn (stofn)**|**Reikningsfært magn (stofn)**|  
|-|----------------------------------------------|--------------------------------------------|------------------------------------------------------|-------------------------------------------------------|--------------------------------------------------------|  
|**Vörurakningarlínur** gluggi|7|**4**|**0**|0|0|  
|**T337**|3|0|0|0|0|  
|**T336**|4|0|0|4|0|  

 Skref 3: Fá tvö stykki og reikningsfæra tvö stykki.  

||**Magn (stofn)**|**Magn til afgreiðslu**|**Magn til reikningsf. (stofn)**|**Afgreitt magn (stofn)**|**Reikningsfært magn (stofn)**|  
|-|----------------------------------------------|--------------------------------------------|------------------------------------------------------|-------------------------------------------------------|--------------------------------------------------------|  
|**Vörurakningarlínur** gluggi|7|**2**|**2**|4|0|  
|**T337**|1|0|0|0|0|  
|**T336**|6|0|0|6|2|  

 Skref 4: Fá eitt stykki.  

||**Magn (stofn)**|**Magn til afgreiðslu**|**Magn til reikningsf. (stofn)**|**Afgreitt magn (stofn)**|**Reikningsfært magn (stofn)**|  
|-|----------------------------------------------|--------------------------------------------|------------------------------------------------------|-------------------------------------------------------|--------------------------------------------------------|  
|**Vörurakningarlínur** gluggi|7|**1**|**0**|6|2|  
|**T336**|7|0|0|7|2|  

 Reikningsfæra 5 stykki.  

||**Magn (stofn)**|**Magn til afgreiðslu**|**Magn til reikningsf. (stofn)**|**Afgreitt magn (stofn)**|**Reikningsfært magn (stofn)**|  
|-|----------------------------------------------|--------------------------------------------|------------------------------------------------------|-------------------------------------------------------|--------------------------------------------------------|  
|**Vörurakningarlínur** gluggi|7|0|**5**|7|2|  
|**T336**|7|0|0|7|7|  

## <a name="see-also"></a>Sjá einnig  
 [Hönnunarupplýsingar: vörurakning](design-details-item-tracking.md)   
 [Hönnunarupplýsingar: vörurakningarlínur gluggi](design-details-item-tracking-lines-window.md)

