---
title: "Hvernig ska virkja tínslu eftir FEFO | Microsoft Docs"
description: "Fyrst-fyrnt-fyrst-út (FEFO) er röðunaraðferð sem tryggir að elstu vörurnar, sem hafa elstu lokadagsetningarnar, eru tíndar fyrst."
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
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 34d6e46146f3072da49cd28e4b4bf1b0f00d1369
ms.contentlocale: is-is
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-enable-picking-items-by-fefo"></a>Hvernig skal: Virkja Vörutínsla eftir FEFO
Fyrst-fyrnt-fyrst-út (FEFO) er röðunaraðferð sem tryggir að elstu vörurnar, sem hafa elstu lokadagsetningarnar, eru tíndar fyrst.  

 Þessi aðgerð virkar aðeins ef eftirfarandi skilyrði eru uppfyllt:  

-   Varan verður að hafa rað-/lotunúmer.  
-   Í vörurakningarkótauppsetningu vörunnar verður að velja reitinn **Vöruhúsarakning bundin við raðnúmer** eða reitinn **Vöruhúsarakning bundin við lotnúmer**.  
-   Vöruna þarf að bóka á birgðir með lokadegi.  
-   Á birgðageymsluspjaldinu verður reiturinn **Krefjast tínslu** að vera valinn.  
-   Á birgðageymsluspjaldinu verður gátreiturinn **Tína eftir FEFO** að vera valinn.  
-   Á birgðageymsluspjaldinu þarf að velja gátreitinn **Hólf áskilið**.  

 Þegar öll skilyrðin eru uppfyllt er rað-/lotunúmerum til tínslu raðað með þá elstu fyrst í öllum tínslum og hreyfingum, fyrir utan vörur sem nota raðnúmers- eða lotubundna rakningu.  

> [!NOTE]  
>  Ef einhverjar vörur með rað-/lotunúmerum nota sértæka rakningu er fyrst tekið tillit til þeirra og undir þeim birtast eftirstandandi ósértak rað-/lotunúmer eftir FEFO.  

 Ef tvær vörur með rað-/lotunúmeri hafa sömu fyrningadagsetningu velur kerfið vöruna með lægsta lotu- eða raðnúmerið. Ef rað- eða lotunúmerin eru þær sömu þá velur forritið þá vöru sem fyrst var skráð.  

> [!NOTE]  
>  -   Þegar vörur með rað-/lotunúmeri eru tíndar í birgðageymslum sem settar eru upp fyrir beinan frágang og tínslu er einungis magn í hólfum af tegundinni *Tínsla* tínt samkvæmt FEFO.  
> -   Til að virkja hreyfingar samkvæmt FEFO, annaðhvort í glugganum **Birgðahreyfing** eða **Vinnublað hreyfingar** verður að skilja reitinn **Frá-hólf** eftir auðan.  
> -   Ef reiturinn **Ströng lokasöludagsetning** er valinn. munu aðeins vörur sem ekki eru útrunnar verða teknar með í tínslunni. Þetta gildir jafnvel þó Tínsla sé ekki notuð samkvæmt FEFO.  

## <a name="see-also"></a>Sjá einnig  
[Vörutínsla](warehouse-pick-items.md)   
[Hvernig á að tína vörur fyrir vöruhúsaafhendingu](warehouse-how-to-pick-items-for-warehouse-shipment.md)   
[Hvernig á að: Tína vörur með birgðatínslu](warehouse-how-to-pick-items-with-inventory-picks.md)   
[Hönnunarupplýsingar vöruhúsakerfi](design-details-warehouse-management.md)  
[Birgðir](inventory-manage-inventory.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

