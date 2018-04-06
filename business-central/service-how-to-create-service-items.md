---
title: "Hvernig á að stofna Þjónustuvörur | Microsoft Docs"
description: "Þegar tekið er við óskráðri vöru vegna þjónustu má skrá hana sem þjónustuvöru."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/08/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: b7a125335d0e0420bd65a45051f625c9e753b522
ms.contentlocale: is-is
ms.lasthandoff: 03/22/2018

---
# <a name="create-service-items"></a>Stofna þjónustuatriði
Í [!INCLUDE[d365fin](includes/d365fin_md.md)] vísar hugtakið „þjónustuvara“ til búnaðar eða vöru þarfnast þjónustu. Þegar þú stofnar þjónustupöntun, tilgreinirðu vöruna sem þarfnast þjónustu. Í pöntuninni geturðu tengt þjónustuvöru við vöru í birgðum eða þjónustuvöruflokk.    

Þegar tekið er við vöru sem þarfnast þjónustu má skrá hana sem þjónustuvöru. Hægt er gera það á nokkra vegu: Þú getur t.d. stofnað þjónustuvöru á **Þjónustuvörur** síðunni, eða sem hluta af öðru ferli, eins og þegar þú vinnur með þjónustupöntun.   

## <a name="to-create-a-service-item"></a>Þjónustuvörur stofnaðar:  
1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Þjónustuvörur** og velja svo viðeigandi tengil.
2. Fyllið inn í reitina eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-create-service-items-within-a-service-order"></a>Þjónustuvörur stofnaðar út frá þjónustupöntunum  
Þegar tekið er við vöru til þjónustu og þarf að skrá hana sem þjónustuvöru er hægt að stofna þjónustuvöru í gluggunum **Þjónustupöntun** eða **Þjónustutilboð**.  

1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn  **Þjónustupantanir** og velja svo viðeigandi tengil.  
2. Fyllið inn í reitina eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. Veljið aðgerðina **Stofna þjónustuvara**.  

    Númeri er sjálfkrafa úthlutað til þjónustuvörunnar og þjónustuvöruspjald er stofnað. Reiturinn **Nr. þjónustuvöru** er fylltur út með númeri nýju þjónustuvörunnar.

## <a name="to-create-a-service-item-when-shipping-items"></a>Þjónustuvörur stofnaðar þegar vörur eru sendar:  
Þegar vörur eru sendar, annaðhvort með því að bóka þjónustupantanir eða þjónustureikninga eru sendu vörurnar sjálfkrafa skráðar sem þjónustuvörur að uppfylltum eftirfarandi skilyrðum: Varan verður að tilheyra þjónustuvöruflokki með gátmerki í reitnum **Stofna þjónustuvöru**. Ef vörurnar eru með raðnúmer skráð í glugganum **Vörurakningarlínur** eru þessar upplýsingar afritaðar sjálfvirkt í reitinn Raðnr. á þjónustuvöruspjaldinu þegar þjónustuvörur eru stofnaðar.  

Eftirfarandi aðferð sýnir hvernig stofna má þjónustuvöru þegar þjónustupöntun er send.  

1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn  **Þjónustupantanir** og velja svo viðeigandi tengil.  
2. Opna skal viðeigandi þjónustupöntun.  
3. Veljið aðgerðina **bóka** eða **Bóka og prenta**.  
4. Velja **Afhenda** eða **Afhenda og reikningsfæra** aðgerðina.  
5. Þjónustuvörur eru stofnaðar sjálfkrafa fyrir vörurnar í pöntuninni svo fremi að þær tilheyri þjónustuvöruflokki sem settur hefur verið upp til að stofna þjónustuvörur. Ef sérstök raðnúmer eru skráð í glugganum **Vörurakningarlínur** verður þeim úthlutað til þessum þjónustuvörum eins og við á.  

> [!NOTE]  
>  Ef vara er uppskrift og búið er að opna uppskriftina eru vörurnar meðhöndlaðar eins og um venjulegar vörur væri að ræða. Kerfið stofnar þjónustuvörur eftir skilyrðinu um þjónustuvöruflokk, og ef vill, raðnúmer. Ef þjónustuvara er aukinheldur stofnuð fyrir opna uppskrift sem er samsett úr öðrum uppskriftaríhlutum eru vörur sem þjónustuvöruíhluti stofnaðar fyrir opna uppskriftarþjónustuvöru.  
>   
>  Ef vara er uppskrift og ekki búið að opna uppskriftina eru þjónustuvörur stofnaðar fyrir hana eftir skilyrðinu um þjónustuvöruflokk, og ef vill, raðnúmer.  

## <a name="to-insert-a-starting-fee-for-a-service-item"></a>Upphafsgjald vegna þjónustuvöru sett inn:
1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Þjónustuverkhlutar** og velja svo viðeigandi tengil.
2. Velja aðgerðina **Vöruvinnublað**.
3. Velja þjónustulínuna og síðan **Aðgerðir**, velja **Aðgerðir** og síðan velja **Setja inn upphafsgjald** aðgerðina.  

    Kerfið setur inn þjónustulínu af gerðinni **Kostnaður** með upphafsgjaldinu. Upphafsgjaldið á við þá þjónustuvöru sem valin var.

## <a name="see-also"></a>Sjá einnig  
[Setja upp þjónustuvörur og íhluti þjónustuvara](service-how-setup-service-items.md)  
[Þjónustustýring sett upp](service-setup-service.md)  
[Þjónustukerfi](service-service.md)  

