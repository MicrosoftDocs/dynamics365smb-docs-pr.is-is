---
title: Hvernig á að rekja vöruraktar vörur | Microsoft Docs
description: Hægt er að sjá hvar vörurakin vara var notuð, þar á meðal hvernig og hvenær hún var fengin eða framleidd, millifærð, seld, notuð eða henni skilað. Einnig er hægt að finna öll núverandi tilvik af tilteknu rað- eða lotunúmeri í gagnagrunninum. Það er gert með því að nota Vörurakningu og Færsluleit.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 0e48b98d42a38035de68349677b9e77586c8de2f
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2019
ms.locfileid: "931362"
---
# <a name="trace-item-tracked-items"></a>Rekja vöruraktar vörur
Hægt er að sjá hvar vörurakin vara var notuð, þar á meðal hvernig og hvenær hún var fengin eða framleidd, millifærð, seld, notuð eða henni skilað. Einnig er hægt að finna öll núverandi tilvik af tilteknu rað- eða lotunúmeri í gagnagrunninum. Það er gert með því að nota Vörurakningu og Færsluleit.  

 Þessar aðgerðir geta verið sérstaklega nothæfar við gæðastjórnun þegar komast þarf að því hvaða viðskiptavinir fengu vörur með sérstöku lotunúmeri eða þegar komast þarf að því úr hvaða lotu gallaður íhlutur kom.  

 Á síðunni **Vörurakning** er hægt að rekja áfram og afturábak í röð bókaðra birgðafærslna fyrir rað- eða lotunúmer.  

 Á síðunni **Færsluleit** er ekki hægt að skoða röð færslna en þar sjást allar færslur rað- eða lotunúmers, bæði bókaðar og opnar.  

 Aðgerðirnar tvær má nota í samsetningu með því að flytja inn rakið rað- eða lotunúmer á síðuna **Færsluleit** til að ljúka rakningaraðgerð. Frekari upplýsingar eru í [Kynning: Rekja rað- og lotunúmer](walkthrough-tracing-serial-lot-numbers.md).  

## <a name="to-trace-item-tracked-items"></a>að rekja vöruraktar vörur  

1.  Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **vörurakning** og veldu síðan tengda tengilinn.  
2.  Í afmörkunarreitunum efst á síðunni skal færa inn tiltekið vörunúmer eða afmörkun á vörunúmerum sem á að rekja.  
3.  Í reitnum **Sýna íhluti** er valið hvort ætlunin sé einnig að sjá hvaðan íhlutirnir fyrir vörurnar komu. Valkostirnir í reitnum eru sem hér segir.  

    |Svæði|Description|  
    |----------------------------------|---------------------------------------|  
    |**Nr**|Þessi valkostur er valinn ef ætlunin er ekki að sjá neina íhluti.|  
    |**Vara-eingöngu rakin**|Þessi valkostur er valinn ef ætlunin er að sjá eingöngu þá íhluti sem hafa lotu- eða raðnúmer.|  
    |**ALLT**|Þessi valkostur er valinn ef ætlunin er að sjá alla íhlutina.|  

4.  Í reitnum **Rakningaraðferð** er valin sú aðferð sem nota á til að rekja vöruna. Valkostirnir eru eftirfarandi  

    |Svæði|Description|  
    |----------------------------------|---------------------------------------|  
    |**Notkun->Uppruni**|Þessi aðferð rekur vöruna frá því hvar hún var notuð til þess hvaðan hún kom. Til dæmis, ef framleidd vara var seld til viðskiptavinar, sýnir síðan **Vörurakning** þetta fyrst með söluafhendingarlínunni sem er síðan hægt að stækka til að sjá frá hvaða framleiðslupöntun hún kom.|  
    |**Uppruni->Notkun**|Þessi aðferð rekur vöruna frá því hvar hún kom inn í birgðir til þess hvar hún var notuð. Til dæmis, ef framleidd vara var seld til viðskiptavinar, sýnir síðan **Vörurakning** þetta fyrst með tilbúinni framleiðslupöntun, sem er síðan hægt að stækka til að sjá söluafhendingarlínur þar sem varan var notuð.|  

5.  Velja skal **Rekja** aðgerðina til að keyra rakninguna.  

> [!NOTE]  
>  Ef sama lota er móttekin í fleiri en einni færslu sýnir síðan **Vörurakning** hugsanlega ekki allar færslurnar. Aðeins notaðar færslur eru sýndar.  

> [!NOTE]  
>  Ef lína fyrir ofan vörurakningarlínu hefur þegar rekið færsluferil er gátreiturinn **Þegar verið rakið** valinn. Til að veita einfaldara yfirlit eru slíkar undirliggjandi línur ekki sýndar.  
>   
>  Til að finna vörurakningarlínur þar sem færsluferill hefur þegar verið rakinn skal velja hnappinn **Fara í það sem hefur verið rakið**. Viðkomandi vörurakningarlína er valin og allar undirliggjandi línur eru stækkaðar.  

## <a name="to-find-item-tracked-items-with-navigate"></a>Til að finna vöruraktar vörur með Færsluleit  

1.  Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **skoða** og veldu síðan tengda tengilinn.  
2.  Á flýtiflipanum **Vörurakning**, í reitunum **Raðnúmer** og **Lotunr.**, skal færa inn vörurakningarnúmer sem ætlunin er að rekja.  
3.  Velja skal aðgerðina **Finna** til að finna öll tilvik um rað- eða lotunúmerið í gagnagrunninum.  

## <a name="see-also"></a>Sjá einnig  
[Birgðir](inventory-manage-inventory.md)  
[Hönnunarupplýsingar: vörurakning](design-details-item-tracking.md)
[Hönnunarupplýsingar - vörurakning og frátekning](design-details-item-tracking-and-reservations.md)  
[Taka frá vörur](inventory-how-to-reserve-items.md)  
[Vinna með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
[Kynning: Rekja rað- og lotunúmer](walkthrough-tracing-serial-lot-numbers.md).
