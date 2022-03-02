---
title: Rekja vöruraktar vörur
description: Hægt er að sjá hvar vörurakin vara var notuð, þar á meðal hvernig og hvenær hún var móttekin, framleidd eða skilað með eiginleikum vörurakningar og færsluleit.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.search.forms: 6520,
ms.date: 06/16/2021
ms.author: edupont
ms.openlocfilehash: 6592172331b92c1e0b6623c36c5531b4a32b5088
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2022
ms.locfileid: "8148527"
---
# <a name="trace-item-tracked-items"></a>Rekja vöruraktar vörur
Hægt er að sjá hvar vörurakin vara var notuð, þar á meðal hvernig og hvenær hún var fengin eða framleidd, millifærð, seld, notuð eða henni skilað. Einnig er hægt að finna öll núverandi tilvik af tilteknu rað- eða lotunúmeri í gagnagrunninum. Þetta er gert með því að nota vörurakningu og eiginleikann [Finna færslur](ui-find-entries.md).  

Þessar aðgerðir geta verið sérstaklega nothæfar við gæðastjórnun þegar komast þarf að því hvaða viðskiptavinir fengu vörur með sérstöku lotunúmeri eða þegar komast þarf að því úr hvaða lotu gallaður íhlutur kom.  

 Á síðunni **Vörurakning** er hægt að rekja áfram og afturábak í röð bókaðra birgðafærslna fyrir rað- eða lotunúmer.  

 Á síðunni **Færsluleit** er ekki hægt að skoða röð færslna en þar sjást allar færslur rað- eða lotunúmers, bæði bókaðar og opnar færslur.  

 Aðgerðirnar tvær má nota saman með því að flytja inn rakið rað- eða lotunúmer yfir á síðuna **Finna færslur** til að ljúka ítarlegri rakningaraðgerð. <!-- For more information, see [Walkthrough: Tracing Serial-Lot Numbers](walkthrough-tracing-serial-lot-numbers.md).   -->

## <a name="to-trace-item-tracked-items"></a>að rekja vöruraktar vörur  

1.  Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Vörurakning** og velja síðan viðkomandi tengil.  
2.  Í afmörkunarreitunum efst á síðunni skal færa inn tiltekið vörunúmer eða afmörkun á vörunúmerum sem á að rekja.  
3.  Í reitnum **Sýna íhluti** er valið hvort einnig eigi að sjá hvaðan íhlutirnir fyrir vörurnar komu. Eftirfarandi tafla lýsir valkostunum.  

    |Svæði|Description|  
    |----------------------------------|---------------------------------------|  
    |**Nr**|Ekki sýna íhluti.|  
    |**Vara-eingöngu rakin**|Sýna aðeins íhluti sem hafa lotu- eða raðnúmer.|  
    |**Allt**|Sýna alla íhluti.|  

4.  Í reitnum **Rakningaraðferð** skal velja aðferðina sem nota á til að rekja vöruna. Eftirfarandi tafla lýsir valkostunum.  

    |Svæði|Description|  
    |----------------------------------|---------------------------------------|  
    |**Notkun->Uppruni**|Rekja atriðið þaðan sem það var notað til hvaðan það kom. Til dæmis, ef framleidd vara var seld til viðskiptavinar, sýnir síðan **Vörurakning** þetta fyrst með söluafhendingarlínunni sem er síðan hægt að stækka til að sjá frá hvaða framleiðslupöntun hún kom.|  
    |**Uppruni->Notkun**|Rekja vöruna þaðan sem hún kom í birgðir til þess hvar hún var notuð. Ef framleidd vara var til dæmis seld viðskiptamanni **sýnir síðan Vörurakning** þetta fyrst með loknu framleiðslupöntuninni sem síðan er hægt að stækka til að sjá söluafhendingarlínurnar þar sem varan var notuð.|  

5.  Velja skal **Rekja** aðgerðina til að keyra rakninguna.  

> [!NOTE]  
>  Aðeins notaðar færslur eru sýndar. Ef sama lotan hefur borist í mörgum færslum **sýnir ekki allar færslur á síðunni Vörurakning**.   

> [!NOTE]  
>  Ef lína fyrir ofan vörurakningarlínu hefur þegar rekið færsluferil er gátreiturinn **Þegar verið rakið** valinn. Til að veita einfaldara yfirlit eru slíkar undirliggjandi línur ekki sýndar.  
>   
>  Til að finna vörurakningarlínur þar sem færsluferill hefur þegar verið rakinn skal velja hnappinn **Fara í það sem hefur verið rakið**. Viðkomandi vörurakningarlína er valin og allar undirliggjandi línur eru stækkaðar.  

## <a name="to-find-item-tracked-items-with-find-entries"></a>Til að finna vöruraktar vörur með Finna færslur  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Finna færslur** og velja síðan viðkomandi tengil.  
2. Veljið **Aðgerðir** > **Leita eftir** > **Leita eftir vörutilvísun**.
3. Í reitina **Raðnúmer** og **Lotunúmer** skal færa inn vörurakningarnúmer sem ætlunin er að rekja.  
4. Velja skal aðgerðina **Finna** til að finna öll tilvik um rað- eða lotunúmerið í gagnagrunninum.  

## <a name="see-also"></a>Sjá einnig

[Birgðir](inventory-manage-inventory.md)  
[Vinna með raðnúmer, lotu og pakkanúmer](inventory-how-work-item-tracking.md)  
[Hönnunarupplýsingar: Vörurakning](design-details-item-tracking.md)  
[Hönnunarupplýsingar - vörurakning og frátekningar](design-details-item-tracking-and-reservations.md)  
[Taka frá vörur](inventory-how-to-reserve-items.md)  
[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
<!-- [Walkthrough: Tracing Serial-Lot Numbers](walkthrough-tracing-serial-lot-numbers.md)   -->
[Finna færslur](ui-find-entries.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]