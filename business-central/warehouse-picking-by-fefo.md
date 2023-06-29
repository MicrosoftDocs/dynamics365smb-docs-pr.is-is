---
title: Hvernig ska virkja tínslu eftir FEFO | Microsoft Docs
description: 'Fyrst-fyrnt-fyrst-út (FEFO) er röðunaraðferð sem tryggir að elstu vörurnar, sem hafa elstu lokadagsetningarnar, eru tíndar fyrst.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 04/01/2021
ms.author: edupont
---
# <a name="enable-picking-items-by-fefo"></a><a name="enable-picking-items-by-fefo"></a>Virkja Vörutínsla eftir FEFO
Fyrst-fyrnt-fyrst-út (FEFO) er röðunaraðferð sem tryggir að elstu vörurnar, sem hafa elstu lokadagsetningarnar, eru tíndar fyrst.  

 Þessi aðgerð virkar aðeins ef eftirfarandi skilyrði eru uppfyllt:  

-   Varan verður að hafa rað-/lotunúmer.  
-   Í vörurakningarkóðauppsetningu vörunnar verður að velja reitinn **Vöruhúsarakning bundin við raðnúmer** eða reitinn **Vöruhúsarakning bundin við lotnúmer**.  
-   Vöruna þarf að bóka á birgðir með lokadegi.  
-   Á staðsetningunni verður að vera kveikt á **Krefjast tínslu**, **Tína samkvæmt FEFO** og **Hólf áskilið**.  

 Þegar öll skilyrðin eru uppfyllt er rað-/lotunúmerum til tínslu raðað með þá elstu fyrst í öllum tínslum og hreyfingum, fyrir utan vörur sem nota raðnúmers- eða lotubundna rakningu.  

> [!NOTE]  
> Ef einhverjar vörur með rað- eða lotunúmerum nota sértæka rakningu er fyrst tekið tillit til þeirra og undir þeim birtast eftirstandandi ósértak rað-/lotunúmer eftir FEFO.
<br /><br />
Ef tvær vörur með rað- eða lotunúmeri hafa sömu fyrningadagsetningu velur kerfið vöruna með lægsta lotu- eða raðnúmerið.
<br /><br />
Þegar vörur með rað- eða lotunúmeri eru tíndar í birgðageymslum sem settar eru upp fyrir beinan frágang og tínslu er einungis magn í hólfum af tegundinni *Tínsla* tínt samkvæmt FEFO.  
<br /><br />
Til að virkja hreyfingar samkvæmt FEFO skal skilja reitinn **Frá hólfi** eftir auðan á síðunni **Birgðahreyfing** eða síðunni **Vinnublað hreyfingar**.  
<br /><br />
Ef reiturinn **Ströng lokasöludagsetning** er valinn á **Vörurakningarkóðaspjaldinu** verða aðeins vörur sem ekki eru útrunnar hafar með í tínslunni og línunum er raðað samkvæmt FEFO.

## <a name="see-also"></a><a name="see-also"></a>Sjá einnig
[Tína vörur fyrir vöruhúsaafhendingu](warehouse-how-to-pick-items-for-warehouse-shipment.md)   
[Vörur tíndar með birgðatínslu](warehouse-how-to-pick-items-with-inventory-picks.md)   
[Yfirlit](design-details-warehouse-management.md)
[vöruhúsakerstjórnunar birgðir](inventory-manage-inventory.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
