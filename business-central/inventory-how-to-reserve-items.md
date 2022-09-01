---
title: Hvernig á að taka frá vörur
description: Hægt er að taka vörur frá fyrir sölu-, innkaupa- og framleiðslupantanir. Einnig er hægt að taka frá vörur í birgðum eða á innleið í opnum fylgiskjalslínum.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.search.forms: 498, 497
ms.date: 08/11/2022
ms.author: edupont
ms.openlocfilehash: d727242c772d1eba2959747c2fcd151a7a330009
ms.sourcegitcommit: 38b1272947f64a473de910fe81ad97db5213e6c3
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/29/2022
ms.locfileid: "9361664"
---
# <a name="reserve-items"></a>Taka frá vörur

Hægt er að taka frá vörur fyrir sölupantanir, innkaupapantanir, þjónustupantanir, samsetningarpantanir, flutningspantanir og framleiðslupantanir. Einnig er hægt að taka frá vörur í birgðum eða á innleið í opnum skjala-eða færslubókarlínum. Þetta er gert á **síðunni frátekt**.

Hver lína sem opnuð er til að taka frá vörur á **síðunni frátekningar** Birtir upplýsingar um eina tegund línu (sala, innkaup eða færslubók) eða birgðafærslu. Línurnar lýsa því hver margar vörur er hægt að taka frá fyrir hverja tegund línu eða færslu.

## <a name="reserve-items-for-sales"></a>Taka frá vörur fyrir sölu

Eftirfarandi ferli lýsir því hvernig á að taka frá vörur úr sölupöntun. Skrefin eru svipuð fyrir innkaup, þjónustu, flutning og samsetningarpantanir.
  
1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Teikn, færa inn **sölupantanir** og velja síðan tengda tengilinn.  
2. Velja sölupöntunina.
3. Á flýtiflipanum **Línur** veljið aðgerðina **Taka frá**. Síðan **Frátekning** opnast.  
4. Línan sem taka á vörurnar úr er valin.  
5. Ein af eftirfarandi aðgerðum er valinn.  

    |**Virkni**|**Lýsing**|
    |------------------|---------------------|  
    |**Sjálfvirk frátekning**|Vörur teknar sjálfkrafa frá á síðunni **Frátekning**.|  
    |**Taka frá í gildandi línu**|Vörur teknar frá úr skjalinu á línunni sem hefur verið valin.|  
    |**Hætta við frátekningu í gildandi línu**|Til að hætta við frátekningar varanna í skjalinu í línunni sem þú valdir.|

> [!NOTE]  
> Ef vörurakningarlínur eru til vegna sölupöntunarinnar leiðir frátekningarkerfið notandann í gegnum nokkrar séraðgerðir. Frekari upplýsingar eru [í til að taka frá ákveðinn hluta rað-eða lotunúmera](inventory-how-to-reserve-items.md#reserve-a-specific-serial-or-lot-number).  

## <a name="reserve-an-item-for-a-production-order-line"></a>Taka frá vöru fyrir framleiðslupöntunarlínu

Hægt er að taka vörur frá fyrir framleiðslupantanir. Greina þarf á milli framleiðslupöntunarlína, það er yfirvaran, og framleiðslupöntunaríhluta.

Eftirfarandi aðferð sýnir hvernig fastáætluð framl.pöntun er notuð.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknið, færa inn **Fastáætluð framl. pöntun** og velja síðan tengdan tengil.  
2. Opna fastáætluðu framleiðslupöntunina sem taka á frá yfirvörur fyrir.  
3. Viðkomandi framleiðslupöntunarlína er valin.  
4. Á flýtiflipanum **Línur** veljið aðgerðina **Taka frá**.
5. **Á síðunni frátekning** skal velja **sölulínuna, pöntunarlínuna** og velja **síðan frátekningu úr núverandi Línuaðgerð**.  

Magnið sem fært var inn í fastáætluðu framleiðslupöntunarlínuna hefur verið frátekið.

## <a name="reserve-items-for-production-order-components"></a>Taka frá vörur fyrir íhluti framleiðslupantana

Hægt er að taka vörur frá fyrir framleiðslupantanir. Greina þarf á milli framleiðslupöntunarlína, það er yfirvaran, og framleiðslupöntunaríhluta.

Eftirfarandi aðferð sýnir hvernig fastáætluð framl.pöntun er notuð.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknið, færa inn **Fastáætluð framl. pöntun** og velja síðan tengdan tengil.  
2. Opna fastáætluðu framleiðslupöntunina sem taka á frá íhlutavörur fyrir.  
3. Viðkomandi framleiðslupöntunarlína er valin.  
4. **Á vöruflipanum línur** er valin **lína** og síðan valið **Íhlutir**.  
5. Viðeigandi íhlutarlínu er valin.  
6. Á flýtiflipanum **Línur** veljið aðgerðina **Taka frá**.  
7. **Á síðunni frátekning** er valin lína og síðan er **valið frátekið úr núverandi Línuaðgerð**.  

Magnið sem fært var inn í fastáætluðu framleiðsluíhlutalínuna hefur verið frátekið.

## <a name="change-a-reservation"></a>Breyta frátekningu

Stundum er þörf á að breyta frátekningu á vöru.

1. Úr fylgiskjalslínunni sem frátekningin var gerð úr, á **fastflipanum línur**, veljið þá **varaaðgerðina**.  
2. Á síðunni **Frátekning** skal velja aðgerðina **Frátekningarfærslur**.
3. **Á síðunni frátekningarfærslur** skal uppfæra **magnið** í línunni sem á að breyta.
4. Síðari skilaboðin eru staðfest með því að velja hnappinn í **lagi**.

## <a name="cancel-a-reservation"></a>Hætta við frátekningu

Stundum er þörf á að hætta við frátekningu á vöru.

1. Úr fylgiskjalslínunni sem á að hætta við frátekningu fyrir í fastflipanum á **línunum** er varaaðgerðin valin. **·**  
2. Á síðunni **Frátekning** skal velja aðgerðina **Frátekningarfærslur**.  
3. Á síðunni **Frátekningarfærslur** er valin aðgerðin **Hætta við frátekningu**.  
4. Eftirfarandi boð eru staðfest með því að **velja Já** -hnappinn.  

## <a name="reserve-a-specific-serial-or-lot-number"></a>Taka skal fram sérstakt rað-eða lotunúmer

Hægt að taka frá tiltekin raðnúmer eða lotunúmer í útleiðarskjölum fyrir vörur með línurakningu, svo sem sölupantanir eða framleiðsluíhlutalista. Þetta getur til dæmis átt við ef þörf er fyrir framleiðsluíhlutina úr tiltekinni lotu til að tryggja samræmi við fyrri framleiðslukeyrslur eða vegna þess að viðskiptavinur hefur beðið um ákveðið raðnúmer. Lærðu meira í [vinnu með rað-og lotunúmer](inventory-how-work-item-tracking.md).

Í þessari framkvæmd er vísað til sérstakrar frátekningar þar sem Frátekning á magni vöru X sem tilheyrir lotu X er frátengd. Ef aðeins er tekið frá magn af vöru X, er það einfaldlega venjuleg, Óákveðin, frátekning. Frekari upplýsingar í [Hönnunarupplýsingum-vörurakningar og frátekningar](design-details-item-tracking-and-reservations.md).

Eftirfarandi ferli byggist á sölupöntun.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Sölupantanir** og velja síðan viðkomandi tengil.  
2. Stofna sölupöntunarlínu fyrir vörurakta vöru.  
3. Úthluta rað- og lotunúmerum í sölupöntunarlínuna. Lærðu meira í [vinnu með rað-og lotunúmer](inventory-how-work-item-tracking.md).
4. Velja **Taka frá** aðgerðina í sölupöntunarlínunni.  
5. Velja hnappinn **Já** til að taka frá tiltekin rað- eða lotunúmer.  
6. **Á listasíðunni** Vörurakning er valið rað-og lotunúmerasamsetninguna sem úthlutað hefur verið.  
7. Veldu hnappinn **Í lagi** til að opna síðuna **Frátekning** sem sýnir aðeins framboð með tiltekna vörurakningarnúmerinu. Ef ekki eru til neinar sérstakar frátekningar á vörurakningarnúmerin sem hafa verið tilgreind fyrir þessa línu er hægt að upplýsa magnið sem þegar hefur verið frátekið.  
8. Veljið annað hvort **Auto Reserve** eða **Reserve frá núverandi Línuaðgerð** til að stofna frátekningu á tilteknum vörurakningarnúmerum.

## <a name="see-related-training-at-microsoft-learn"></a>Sjá tengdar þjálfun hjá [Microsoft Learn](/learn/modules/manage-outbound-serial-lot-numbers/)

## <a name="see-also"></a>Sjá einnig .

[Birgðir](inventory-manage-inventory.md)  
[Hönnunarupplýsingar: Pöntun, pöntunarrakning og stöðuboð](design-details-reservation-order-tracking-and-action-messaging.md)  
[Hönnunarupplýsingar: vörurakning og frátekningar](design-details-item-tracking-and-reservations.md)  
[Vinna með rað- og lotunúmer](inventory-how-work-item-tracking.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
