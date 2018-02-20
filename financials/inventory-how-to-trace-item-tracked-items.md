---
title: "Hvernig á að rekja vöruraktar vörur | Microsoft Docs"
description: "Hægt er að sjá hvar vörurakin vara var notuð, þar á meðal hvernig og hvenær hún var fengin eða framleidd, millifærð, seld, notuð eða henni skilað. Einnig er hægt að finna öll núverandi tilvik af tilteknu rað- eða lotunúmeri í gagnagrunninum. Það er gert með því að nota Vörurakningu og Færsluleit."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: cc24989d2cf770cd88bbde23d483e3859ff4a68a
ms.contentlocale: is-is
ms.lasthandoff: 01/30/2018

---
# <a name="trace-item-tracked-items"></a>Rekja vöruraktar vörur
Hægt er að sjá hvar vörurakin vara var notuð, þar á meðal hvernig og hvenær hún var fengin eða framleidd, millifærð, seld, notuð eða henni skilað. Einnig er hægt að finna öll núverandi tilvik af tilteknu rað- eða lotunúmeri í gagnagrunninum. Það er gert með því að nota Vörurakningu og Færsluleit.  

 Þessar aðgerðir geta verið sérstaklega nothæfar við gæðastjórnun þegar komast þarf að því hvaða viðskiptavinir fengu vörur með sérstöku lotunúmeri eða þegar komast þarf að því úr hvaða lotu gallaður íhlutur kom.  

 Í glugganum **Vörurakning** er hægt að rekja áfram og afturábak í röð bókaðra birgðafærslna fyrir rað- eða lotunúmer.  

 Í glugganum **Færsluleit** er ekki hægt að skoða röð færslna en þar sjást allar færslur rað- eða lotunúmers, bæði bókaðar og opnar.  

 Aðgerðirnar tvær má nota í samsetningu með því að flytja inn rakið rað- eða lotunúmer í gluggann **Færsluleit** til að ljúka rakningaraðgerð. Frekari upplýsingar eru í [Kynning: Rekja rað- og lotunúmer](walkthrough-tracing-serial-lot-numbers.md).  

## <a name="to-trace-item-tracked-items"></a>að rekja vöruraktar vörur  

1.  Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Vörurakning** og velja svo viðeigandi tengil.  
2.  Í afmörkunarreitina efst í glugganum eru slegin inn tilteknu vörunúmerin eða afmörkun á þau vörunúmer sem ætlunin er að rekja.  
3.  Í reitnum **Sýna íhluti** er valið hvort ætlunin sé einnig að sjá hvaðan íhlutirnir fyrir vörurnar komu. Valkostirnir í reitnum eru sem hér segir.  

    |Svæði|Description|  
    |----------------------------------|---------------------------------------|  
    |**Nr**|Þessi valkostur er valinn ef ætlunin er ekki að sjá neina íhluti.|  
    |**Vara-eingöngu rakin**|Þessi valkostur er valinn ef ætlunin er að sjá eingöngu þá íhluti sem hafa lotu- eða raðnúmer.|  
    |**ALLT**|Þessi valkostur er valinn ef ætlunin er að sjá alla íhlutina.|  

4.  Í reitnum **Rakningaraðferð** er valin sú aðferð sem nota á til að rekja vöruna. Valkostirnir eru eftirfarandi  

    |Svæði|Description|  
    |----------------------------------|---------------------------------------|  
    |**Notkun->Uppruni**|Þessi aðferð rekur vöruna frá því hvar hún var notuð til þess hvaðan hún kom. Ef framleidd vara var til dæmis seld viðskiptavini sýnir glugginn **Vörurakning** þetta fyrst með söluafhendingarlínunni og svo er hægt að víkka út til að sjá úr hvaða framleiðslupöntun hún kom.|  
    |**Uppruni->Notkun**|Þessi aðferð rekur vöruna frá því hvar hún kom inn í birgðir til þess hvar hún var notuð. Ef framleidd vara var til dæmis seld viðskiptavini sýnir glugginn **Vörurakning** þetta fyrst með fullunnu framleiðslupöntuninni, sem svo er hægt að víkka út til að sjá söluafhendingarlínur þar sem varan var notuð.|  

5.  Velja skal **Rekja** aðgerðina til að keyra rakninguna.  

> [!NOTE]  
>  Ef sama lota er móttekin í fleiri en einni færslu sýnir glugginn **Vörurakning** hugsanlega ekki allar færslurnar. Aðeins notaðar færslur eru sýndar.  

> [!NOTE]  
>  Ef lína fyrir ofan vörurakningarlínu hefur þegar rekið færsluferil er gátreiturinn **Þegar verið rakið** valinn. Til að veita einfaldara yfirlit eru slíkar undirliggjandi línur ekki sýndar.  
>   
>  Til að finna vörurakningarlínur þar sem færsluferill hefur þegar verið rakinn skal velja hnappinn **Fara í það sem hefur verið rakið**. Viðkomandi vörurakningarlína er valin og allar undirliggjandi línur eru stækkaðar.  

## <a name="to-find-item-tracked-items-with-navigate"></a>Til að finna vöruraktar vörur með Færsluleit  

1.  Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Færsluleit** og velja svo viðeigandi tengil.  
2.  Á flýtiflipanum **Vörurakning**, í reitunum **Raðnúmer** og **Lotunr.**, skal færa inn vörurakningarnúmer sem ætlunin er að rekja.  
3.  Velja skal aðgerðina **Finna** til að finna öll tilvik um rað- eða lotunúmerið í gagnagrunninum.  

## <a name="see-also"></a>Sjá einnig  
[Birgðir](inventory-manage-inventory.md)  
[Hönnunarupplýsingar: vörurakning](design-details-item-tracking.md)
[Hönnunarupplýsingar - vörurakning og frátekning](design-details-item-tracking-and-reservations.md)  
[Taka frá vörur](inventory-how-to-reserve-items.md)  
[Vinna með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
[Kynning: Rekja rað- og lotunúmer](walkthrough-tracing-serial-lot-numbers.md).

