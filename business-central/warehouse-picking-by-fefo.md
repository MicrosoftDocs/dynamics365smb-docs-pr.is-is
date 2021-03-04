---
title: Hvernig ska virkja tínslu eftir FEFO | Microsoft Docs
description: Fyrst-fyrnt-fyrst-út (FEFO) er röðunaraðferð sem tryggir að elstu vörurnar, sem hafa elstu lokadagsetningarnar, eru tíndar fyrst.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 1c7896988545d6f1b8269ead90dff7350bc6f320
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/17/2020
ms.locfileid: "4755828"
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