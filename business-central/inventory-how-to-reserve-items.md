---
title: Hvernig á að taka frá vörur
description: Hægt er að taka vörur frá fyrir sölu-, innkaupa- og framleiðslupantanir. Hægt er að taka frá vörur í birgðum eða á innleið í opnum skjalalínum.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.search.forms: 498, 497
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 385003db0d0fe8b121e6512257f0ed448596225e
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2022
ms.locfileid: "8519701"
---
# <a name="reserve-items"></a>Taka frá vörur
Hægt er að taka vörur frá fyrir sölu-, innkaupa-, þjónustu, samsetningar- og framleiðslupantanir. Hægt er að taka frá vörur í birgðum eða á innleið í opnum skjalalínum eða færslubókarlínum. Þú framkvæmir vinnuna á síðunni **Frátekning**.

Hver lína á síðunni **Frátekning**, sem þú opnar til að taka frá vörur, sýnir upplýsingar um eina tegund línu (sölu-, innkaupa-, bókar-) eða birgðafærslu. Línurnar lýsa því hver margar vörur er hægt að taka frá fyrir hverja tegund línu eða færslu.

## <a name="to-reserve-items-for-sales"></a>Vörur teknar frá fyrir sölu
Eftirfarandi lýsir því hvernig skal taka frá vörur frá sölupöntun. Skrefin eru svipuð fyrir innkaupa-, þjónustu og samsetningarpöntun.  
1.  Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, færa inn **Sölupantanir** og velja síðan viðkomandi tengil.  
2.  Í sölupöntun í flýtiflipanum **Línur** veljið aðgerðina **Taka frá**. Síðan **Frátekning** opnast.  
3. Smellt er á línuna þar sem taka á vörurnar frá.  
4. Ein af eftirfarandi aðgerðum er valinn.  

    |**Virkni**|**Lýsing**|
    |------------------|---------------------|  
    |**Sjálfvirk frátekning**|Vörur teknar sjálfkrafa frá á síðunni **Frátekning**.|  
    |**Taka frá í gildandi línu**|Vörur teknar frá úr skjalinu á línunni sem hefur verið valin.|  
    |**Hætta við frátekningu í gildandi línu**|Hætt við að taka vörur frá úr skjalinu á línunni sem hefur verið valin.|

> [!NOTE]  
>  Ef vörurakningarlínur eru til vegna sölupöntunarinnar leiðir frátekningarkerfið notandann í gegnum nokkrar séraðgerðir. Frekari upplýsingar er að finna í [Til að taka frá tiltekið rað- eða lotunúmer](inventory-how-to-reserve-items.md#to-reserve-a-specific-serial-or-lot-number).  

## <a name="to-reserve-an-item-for-a-production-order-line"></a>Vörur teknar frá fyrir framleiðslupöntunarlínur  
Hægt er að taka vörur frá fyrir framleiðslupantanir. Greina þarf á milli framleiðslupöntunarlína, það er yfirvaran, og framleiðslupöntunaríhluta.

Eftirfarandi aðferð sýnir hvernig fastáætluð framl.pöntun er notuð.   
1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Fastáætluð framl.pöntun** og velja síðan viðkomandi tengil.  
2. Opna fastáætluðu framleiðslupöntunina sem taka á frá yfirvörur fyrir.  
3. Viðkomandi framleiðslupöntunarlína er valin.  
4. Á flýtiflipanum **Línur** veljið aðgerðina **Taka frá**.
5. Á síðunni **Frátekning** er valin línan **Sölulína, Pöntun** og síðan smellt á aðgerðina **Taka frá af gildandi línu**.  

Magnið sem fært var inn í fastáætluðu framleiðslupöntunarlínuna hefur verið frátekið.

## <a name="to-reserve-items-for-production-order-components"></a>Vörur teknar frá fyrir framleiðslupöntunaríhluti  
Hægt er að taka vörur frá fyrir framleiðslupantanir. Greina þarf á milli framleiðslupöntunarlína, það er yfirvaran, og framleiðslupöntunaríhluta.

Eftirfarandi aðferð sýnir hvernig fastáætluð framl.pöntun er notuð.    
1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Fastáætluð framl.pöntun** og velja síðan viðkomandi tengil.  
2. Opna fastáætluðu framleiðslupöntunina sem taka á frá íhlutavörur fyrir.  
3. Viðkomandi framleiðslupöntunarlína er valin.  
4. Á flýtiflipanum **Línur** skal velja **Lína** og velja svo **Íhlutir**.  
5. Viðeigandi íhlutarlínu er valin.  
6. Á flýtiflipanum **Línur** veljið aðgerðina **Taka frá**.  
7. Á síðunni **Frátekning** er valin línan og síðan smellt á aðgerðina **Taka frá af gildandi línu**.  

Magnið sem fært var inn í fastáætluðu framleiðsluíhlutalínuna hefur verið frátekið.

## <a name="to-change-a-reservation"></a>Frátekningu breytt:  
Stundum er þörf á að breyta frátekningu á vöru.   
1. Á skjalalínunni sem frátekningin beindist að, á flýtiflipanum **Línur** veljið aðgerðina **Taka frá**.  
2. Á síðunni **Frátekning** skal velja aðgerðina **Frátekningarfærslur**.
3. Síðan **Frátekningarfærslur**, uppfærðu reitinn **Magn** í línunni sem á að breyta.
4. Staðfesta eftirfarandi skilaboð með því að velja hnappinn **Í lagi**.

## <a name="to-cancel-a-reservation"></a>Hætt við frátekningu á vörum  
Stundum er þörf á að hætta við frátekningu á vöru.   
1. Úr fylgiskjalslínunni þar sem á að hætta við frátekningu, á flýtiflipanum **Línur** skal velja aðgerðina **Taka frá**.  
2. Á síðunni **Frátekning** skal velja **Frátekningarfærslur** aðgerðina.  
3.  Á síðunni **Frátekningarfærslur** er valin aðgerðin **Hætta við frátekningu**.  
4.  Staðfesta eftirfarandi skilaboð með því að velja hnappinn **Í lagi**.  

## <a name="to-reserve-a-specific-serial-or-lot-number"></a>Til að taka frá tiltekið rað- eða lotunúmer  
Hægt að taka frá tiltekin raðnúmer eða lotunúmer í útleiðarskjölum fyrir vörur með línurakningu, svo sem sölupantanir eða framleiðsluíhlutalista. Þetta getur til dæmis átt við ef þörf er fyrir framleiðsluíhlutina úr tiltekinni lotu til að tryggja samræmi við fyrri framleiðslukeyrslur eða vegna þess að viðskiptavinur hefur beðið um ákveðið raðnúmer. Frekari upplýsingar, sjá [Vinna með rað- og lotunúmer](inventory-how-work-item-tracking.md).

Þetta er kallað sértæk frátekning, þar sem tekið er frá magni Vöru X sem tilheyrir Lotu X. Ef einfaldlega er tekið frá úr magni Vöru X er það venjuleg, ósértæk frátekning. Nánari upplýsingar eru í [Upplýsingar um hönnun - Vörurakning og frátekningar](design-details-item-tracking-and-reservations.md).

Eftirfarandi ferli byggist á sölupöntun.    
1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Sölupantanir** og velja síðan viðkomandi tengil.  
2. Stofna sölupöntunarlínu fyrir vörurakta vöru.  
3. Úthluta rað- og lotunúmerum í sölupöntunarlínuna. Frekari upplýsingar, sjá [Vinna með rað- og lotunúmer](inventory-how-work-item-tracking.md).
4. Velja **Taka frá** aðgerðina í sölupöntunarlínunni.  
5. Velja hnappinn **Já** til að taka frá tiltekin rað- eða lotunúmer.  
6. Á síðunni **Vörurakningarlisti** skal velja þá samsetningu rað- og lotunúmers sem var verið að úthluta.  
7. Veldu hnappinn **Í lagi** til að opna síðuna **Frátekning** sem sýnir aðeins framboð með tiltekna vörurakningarnúmerinu. Ef ósértækar frátekningar eru í vörurakningarnúmeri sem tilgreint hefur verið fyrir þessa línu er tilkynnt um hve mikið magn hefur þegar verið frátekið.  
8. Veljið annað hvort **Sjálfvirk frátekning** eða **Taka frá í gildandi línu** aðgerð til að stofna frátekninguna á tilgreindu vörurakningarnúmerunum.

## <a name="see-also"></a>Sjá einnig
[Birgðir](inventory-manage-inventory.md)  
[Hönnunarupplýsingar: Pöntun, pöntunarrakning og stöðuboð](design-details-reservation-order-tracking-and-action-messaging.md)  
[Hönnunarupplýsingar - vörurakning og frátekningar](design-details-item-tracking-and-reservations.md)  
[Vinna með rað- og lotunúmer](inventory-how-work-item-tracking.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]