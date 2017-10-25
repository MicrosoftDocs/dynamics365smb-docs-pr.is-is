---
title: "Hvernig á að taka frá vörur | Microsoft Docs"
description: "Hægt er að taka vörur frá fyrir sölu-, innkaupa- og framleiðslupantanir. Hægt er að taka frá vörur í birgðum eða á innleið í opnum skjalalínum."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/14/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: b03209b5681c264f7d788d3d731d32b60f1709b6
ms.contentlocale: is-is
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-reserve-items"></a>Hvernig skal: Taka frá vörur
Hægt er að taka vörur frá fyrir sölu-, innkaupa-, þjónustu, samsetningar- og framleiðslupantanir. Hægt er að taka frá vörur í birgðum eða á innleið í opnum skjalalínum eða færslubókarlínum. Þú framkvæmir vinnuna í **Frátekning** glugganum.

Hver lína í glugganum **Frátekning**, sem þú opnar til að taka frá vörur, sýnir upplýsingar um eina tegund línu (sölu-, innkaupa-, bókar-) eða birgðafærslu. Línurnar lýsa því hver margar vörur er hægt að taka frá fyrir hverja tegund línu eða færslu.

## <a name="to-reserve-items-for-sales"></a>Vörur teknar frá fyrir sölu
Eftirfarandi lýsir því hvernig skal taka frá vörur frá sölupöntun. Skrefin eru svipuð fyrir innkaupa-, þjónustu og samsetningarpöntun.  
1.  Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn  **Sölupantanir** og velja svo viðeigandi tengil.  
2.  Í sölupöntun í flýtiflipanum **Línur** veljið aðgerðina **Taka frá**. Glugginn **Frátekning** opnast.  
3. Smellt er á línuna þar sem taka á vörurnar frá.  
4. Ein af eftirfarandi aðgerðum er valinn.  

    |**Virkni**|**Lýsing**|
    |------------------|---------------------|  
    |**Sjálfvirk frátekning**|Vörur teknar sjálfkrafa frá í glugganum **Frátekning**.|  
    |**Taka frá í gildandi línu**|Vörur teknar frá úr skjalinu á línunni sem hefur verið valin.|  
    |**Hætta við frátekningu í gildandi línu**|Hætt við að taka vörur frá úr skjalinu á línunni sem hefur verið valin.|

> [!NOTE]  
>  Ef vörurakningarlínur eru til vegna sölupöntunarinnar leiðir frátekningarkerfið notandann í gegnum nokkrar séraðgerðir. Frekari upplýsingar, sjá hlutann „Til að taka frá tiltekið rað- eða lotunúmer“.  

## <a name="to-reserve-an-item-for-a-production-order-line"></a>Vörur teknar frá fyrir framleiðslupöntunarlínur  
Hægt er að taka vörur frá fyrir framleiðslupantanir. Greina þarf á milli framleiðslupöntunarlína, það er yfirvaran, og framleiðslupöntunaríhluta.

Eftirfarandi aðferð sýnir hvernig fastáætluð framl.pöntun er notuð.   
1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn  **Fastáætluð framleiðslupöntun** og velja svo viðeigandi tengil.  
2. Opna fastáætluðu framleiðslupöntunina sem taka á frá yfirvörur fyrir.  
3. Viðkomandi framleiðslupöntunarlína er valin.  
4. Á flýtiflipanum **Línur** veljið aðgerðina **Taka frá**.
5. Í glugganum **Frátekning** er valin línan **Sölulína, Pöntun** og síðan smellt á aðgerðina **Taka frá af gildandi línu**.  

Magnið sem fært var inn í fastáætluðu framleiðslupöntunarlínuna hefur verið frátekið.

## <a name="to-reserve-items-for-production-order-components"></a>Vörur teknar frá fyrir framleiðslupöntunaríhluti  
Hægt er að taka vörur frá fyrir framleiðslupantanir. Greina þarf á milli framleiðslupöntunarlína, það er yfirvaran, og framleiðslupöntunaríhluta.

Eftirfarandi aðferð sýnir hvernig fastáætluð framl.pöntun er notuð.    
1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn  **Fastáætluð framleiðslupöntun** og velja svo viðeigandi tengil.  
2. Opna fastáætluðu framleiðslupöntunina sem taka á frá íhlutavörur fyrir.  
3. Viðkomandi framleiðslupöntunarlína er valin.  
4. Á flýtiflipanum **Línur** skal velja **Lína** og velja svo **Íhlutir**.  
5. Viðeigandi íhlutarlínu er valin.  
6. Á flýtiflipanum **Línur** veljið aðgerðina **Taka frá**.  
7. Í glugganum **Frátekning** er valin línan og síðan smellt á aðgerðina **Taka frá af gildandi línu**.  

Magnið sem fært var inn í fastáætluðu framleiðsluíhlutalínuna hefur verið frátekið.

## <a name="to-change-a-reservation"></a>Frátekningu breytt:  
Stundum er þörf á að breyta frátekningu á vöru.   
1. Á skjalalínunni sem frátekningin beindist að, á flýtiflipanum **Línur** veljið aðgerðina **Taka frá**.  
2. Í glugganum **Frátekning** skal velja aðgerðina **Frátekningarfærslur**.
3. Glugginn **Frátekningarfærslur**, uppfærðu reitinn **Magn** í línunni sem á að breyta.
4. Staðfesta eftirfarandi skilaboð með því að velja hnappinn **Í lagi**.

## <a name="to-cancel-a-reservation"></a>Hætt við frátekningu á vörum  
Stundum er þörf á að hætta við frátekningu á vöru.   
1. Úr fylgiskjalslínunni þar sem á að hætta við frátekningu, á flýtiflipanum **Línur** skal velja aðgerðina **Taka frá**.  
2. Í glugganum **Frátekning** skal velja aðgerðina **Frátekningarfærslur**.  
3.  Í reitnum **Frátekningarfærslur** er valið **hætta við frátekningu** aðgerð.  
4.  Staðfesta eftirfarandi skilaboð með því að velja hnappinn **Í lagi**.  

## <a name="to-reserve-a-specific-serial-or-lot-number"></a>Til að taka frá tiltekið rað- eða lotunúmer  
Hægt að taka frá tiltekin raðnúmer eða lotunúmer í útleiðarskjölum fyrir vörur með línurakningu, svo sem sölupantanir eða framleiðsluíhlutalista. Þetta getur til dæmis átt við ef þörf er fyrir framleiðsluíhlutina úr tiltekinni lotu til að tryggja samræmi við fyrri framleiðslukeyrslur eða vegna þess að viðskiptavinur hefur beðið um ákveðið raðnúmer. Frekari upplýsingar, sjá [Hvernig á að: vinna með rað- og lotunúmer](inventory-how-work-item-tracking.md).

Þetta er kallað sértæk frátekning, þar sem tekið er frá magni Vöru X sem tilheyrir Lotu X. Ef einfaldlega er tekið frá úr magni Vöru X er það venjuleg, ósértæk frátekning. Nánari upplýsingar eru í [Upplýsingar um hönnun - Vörurakning og frátekningar](design-details-item-tracking-and-reservations.md).

Eftirfarandi ferli byggist á sölupöntun.    
1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Sölupantanir** og velja svo viðeigandi tengil.  
2. Stofna sölupöntunarlínu fyrir vörurakta vöru.  
3. Úthluta rað- og lotunúmerum í sölupöntunarlínuna. Frekari upplýsingar, sjá [Hvernig á að: vinna með rað- og lotunúmer](inventory-how-work-item-tracking.md).
4. Velja **Taka frá** aðgerðina í sölupöntunarlínunni.  
5. Velja hnappinn **Já** til að taka frá tiltekin rað- eða lotunúmer.  
6. Í glugganum **Vörurakningarlisti** skal velja þá samsetningu rað- og lotunúmers sem var verið að úthluta.  
7. Veldu hnappinn **Í lagi** til að opna gluggann **Frátekning** sem sýnir aðeins framboð með tiltekna vörurakningarnúmerinu. Ef ósértækar frátekningar eru í vörurakningarnúmeri sem tilgreint hefur verið fyrir þessa línu er tilkynnt um hve mikið magn hefur þegar verið frátekið.  
8. Veljið annað hvort **Sjálfvirk frátekning** eða **Taka frá í gildandi línu** aðgerð til að stofna frátekninguna á tilgreindu vörurakningarnúmerunum.

## <a name="see-also"></a>Sjá einnig
[Birgðir](inventory-manage-inventory.md)  
[Hönnunarupplýsingar: Pöntun, pöntunarrakning og stöðuboð](design-details-reservation-order-tracking-and-action-messaging.md)  
[Hönnunarupplýsingar - vörurakning og frátekningar](design-details-item-tracking-and-reservations.md)  
[Hvernig á að: vinna með rað- og lotunúmer](inventory-how-work-item-tracking.md).  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

