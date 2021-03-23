---
title: Hvernig ska virkja tínslu eftir FEFO | Microsoft Docs
description: Fyrst-fyrnt-fyrst-út (FEFO) er röðunaraðferð sem tryggir að elstu vörurnar, sem hafa elstu lokadagsetningarnar, eru tíndar fyrst.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: ae07bc4f1d9f348f08f591e5e4341938ec4b5f16
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5382205"
---
# <a name="enable-picking-items-by-fefo"></a>Virkja Vörutínsla eftir FEFO
Fyrst-fyrnt-fyrst-út (FEFO) er röðunaraðferð sem tryggir að elstu vörurnar, sem hafa elstu lokadagsetningarnar, eru tíndar fyrst.  

 Þessi aðgerð virkar aðeins ef eftirfarandi skilyrði eru uppfyllt:  

-   Varan verður að hafa rað-/lotunúmer.  
-   Í vörurakningarkóðauppsetningu vörunnar verður að velja reitinn **Vöruhúsarakning bundin við raðnúmer** eða reitinn **Vöruhúsarakning bundin við lotnúmer**.  
-   Vöruna þarf að bóka á birgðir með lokadegi.  
-   Á birgðageymsluspjaldinu verður reiturinn **Krefjast tínslu** að vera valinn.  
-   Á birgðageymsluspjaldinu verður gátreiturinn **Tína eftir FEFO** að vera valinn.  
-   Á birgðageymsluspjaldinu þarf að velja gátreitinn **Hólf áskilið**.  

 Þegar öll skilyrðin eru uppfyllt er rað-/lotunúmerum til tínslu raðað með þá elstu fyrst í öllum tínslum og hreyfingum, fyrir utan vörur sem nota raðnúmers- eða lotubundna rakningu.  

> [!NOTE]  
> Ef einhverjar vörur með rað-/lotunúmerum nota sértæka rakningu er fyrst tekið tillit til þeirra og undir þeim birtast eftirstandandi ósértak rað-/lotunúmer eftir FEFO.
<br /><br />
Ef tvær vörur með rað-/lotunúmeri hafa sömu fyrningadagsetningu velur forritið vöruna með lægsta lotu- eða raðnúmerið.
<br /><br />
Þegar vörur með rað-/lotunúmeri eru tíndar í birgðageymslum sem settar eru upp fyrir beinan frágang og tínslu er einungis magn í hólfum af tegundinni *Tínsla* tínt samkvæmt FEFO.  
<br /><br />
Til að virkja hreyfingar samkvæmt FEFO, annaðhvort á síðunni **Birgðahreyfing** eða **Vinnublað hreyfingar** verður að skilja reitinn **Frá-hólf** eftir auðan.  
<br /><br />
Ef reiturinn **Ströng lokasöludagsetning** er valinn. munu aðeins vörur sem ekki eru útrunnar verða teknar með í tínslunni. Þetta gildir jafnvel þó Tínsla sé ekki notuð samkvæmt FEFO.

## <a name="see-also"></a>Sjá einnig  
[Vörutínsla](warehouse-pick-items.md)   
[Tína vörur fyrir vöruhúsaafhendingu](warehouse-how-to-pick-items-for-warehouse-shipment.md)   
[Vörur tíndar með birgðatínslu](warehouse-how-to-pick-items-with-inventory-picks.md)   
[Hönnunarupplýsingar vöruhúsakerfi](design-details-warehouse-management.md)  
[Birgðir](inventory-manage-inventory.md)  
[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]