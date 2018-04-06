---
title: "Hvernig á að færa vörur með ítarlegum vöruhúsaaðgerðum | Microsoft Docs"
description: "Í ítarlegri vöruhúsagrunnstillingu, þ.e. birgðageymslum sem nota beinan frágang og tínslu, sér reyndur starfsmaður um hreyfingar milli hólfa og útbýr hreyfingar í hreyfingavinnublaðinu og stofnar síðan hreyfingar sem starfsmenn vöruhússins framkvæma."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/23/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 709246afc4eef211a7f168741e7b05d40461a41b
ms.contentlocale: is-is
ms.lasthandoff: 03/22/2018

---
# <a name="move-items-in-advanced-warehouse-configurations"></a>Færa vörur með ítarlegum vöruhúsaaðgerðum
Í ítarlegri vöruhúsagrunnstillingu, þ.e. birgðageymslum sem nota beinan frágang og tínslu, sér reyndur starfsmaður um hreyfingar milli hólfa og útbýr hreyfingar í hreyfingavinnublaðinu og stofnar síðan hreyfingar sem starfsmenn vöruhússins framkvæma.  

## <a name="to-move-items-with-the-warehouse-movement-worksheet"></a>Til að færa vörur með vöruhúsahreyfingarvinnublaðinu
Glugginn **Vinnublað hreyfingar** hefur tvær aðgerðir sem hjálpa til við að fylla út línurnar sjálfvirkt. Önnur er aðgerðin **Reikna út áfyllingu hólfs**. Aðgerðin notar hólfaflokkun til að leggja til áfyllingu hærra flokkaðra hólfa úr lægra flokkuðum. Hin er aðgerðin **Sækja innihald hólfs** sem fyllir út vinnublaðslínurnar með öllu innihaldi hólfsins eða hólfanna sem eru tilgreind.

1.  Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Hreyfingarvinnublað** og velja svo viðeigandi tengil.  
2.  Færið inn upplýsingar um vöruhúsahreyfingar í vinnublaðslínurnar eins og við á.  
3. Veljið aðgerðina **Stofna hreyfingu** til að stofna vöruhúsahreyfingarskjal sem síðan er hægt að skrá þegar vöruhúsahreyfingunni er lokið.  

### <a name="to-register-the-warehouse-movement"></a>Vöruhúsahreyfingin skráð  
1.  Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Hreyfingar** og velja svo viðeigandi tengil.  
2.  Opnar vöruhúsahreyfingu sem á að vinna með.  
3.  Á línum aðgerðartegundar **Staðsetja** skal tilgreina hvar, sem og, hvenær eigi að færa viðkomandi vöru með því að breyta svæðunum **Svæðiskóti**, **Hólfkóti**, **Magn til afgreiðslu**, eða **Gjalddagi**.  

    Hafi vöruhúsið verið sett þannig upp að hólfakótarnir fylgi eiginlegu skipulagi vöruhússins er hægt að taka ákveðnar vörur úr samfelldum magnhólfum og setja þær síðan í framtíðartínsluhólf sem gætu verið nálægt hvert öðru.  
4.  Í línum aðgerðegundir **Taka**, tilgreinið í reitnum **Magn til afgreiðslu** íhlutamagn innihalds hólfs sem á að færa. Allir aðrir reitir á línum af aðgerðtegundinni **Taka** eru skrifvarðir.  
5.  Til að færa allt ráðlagt magn eins og tilgreint er í reitnum **Magn** skal velja **Fylla sjálfvirkt inn magn til afgr.** aðgerðina.  
6. Velja aðgerðina **Skrá**.  

> [!NOTE]  
>  Þegar birgðageymslan notar beinan frágang og tínslu og hólfategundir þá er ekki hægt að færa vörur handvirkt inn og út úr hólfum því vörur sem eru í hólfi af þeirri gerð verður að skrá sem frágengnar áður en þær verða hluti af tiltækum birgðum.

## <a name="to-register-the-movement-of-an-item-that-has-already-occurred"></a>Flutningur á vörum sem þegar hefur átt sér stað skráður  
Ef birgðageymslan notar beinan frágang og tínslu og það þarf að færa vörurnar í önnur hólf án þess að fyrir sé vöruhúsafrágangur, tínsla eða hreyfing er hægt að skrá rétta staðinn fyrir vörurnar í vöruhúsinu með því að nota **vöruhússendurflokkunarbók**.

1.  Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Endurflokkunarbók vöruhúss** og velja svo viðeigandi tengil.  
2.  Reitirnir **Vörunr.**, **, Frá-svæðiskóti**, **Kóti frá-hólfs**, **Til-svæðiskóti**, and **Kóti til-hólfse** eru fylltir út.  
3.  Velja aðgerðina **Skrá**.  

## <a name="see-also"></a>Sjá einnig  
[Vöruhúsastjórnun](warehouse-manage-warehouse.md)  
[Birgðir](inventory-manage-inventory.md)  
[Vöruhúsastjórnun sett upp](warehouse-setup-warehouse.md)     
[Samsetningardeild](assembly-assemble-items.md)    
[Hönnunarupplýsingar vöruhúsakerfi](design-details-warehouse-management.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

