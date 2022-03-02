---
title: Hvernig á að stofna Þjónustuvörur
description: Lestu um mismunandi leiðir sem hægt er að fara til að búa til þjónustuvörur í Business Central, til dæmis innan þjónustupöntunar eða við sendingu á vörum.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/23/2021
ms.author: edupont
ms.openlocfilehash: 74af60caaf286b9993402228b050e3717fb847a6
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2022
ms.locfileid: "8136906"
---
# <a name="create-service-items"></a>Stofna þjónustuatriði
Í [!INCLUDE[prod_short](includes/prod_short.md)] vísar hugtakið „þjónustuvara“ til búnaðar eða vöru þarfnast þjónustu. Þegar þú stofnar þjónustupöntun, tilgreinirðu vöruna sem þarfnast þjónustu. Í pöntuninni geturðu tengt þjónustuvöru við vöru í birgðum eða þjónustuvöruflokk.    

Þegar tekið er við vöru sem þarfnast þjónustu má skrá hana sem þjónustuvöru. Hægt er gera það á nokkra vegu: Þú getur t.d. stofnað þjónustuvöru á **Þjónustuvörur** síðunni, eða sem hluta af öðru ferli, eins og þegar þú vinnur með þjónustupöntun.   

## <a name="to-create-a-service-item"></a>Þjónustuvörur stofnaðar:  
1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Þjónustuvörur** og svo velja viðeigandi tengil.
2. Fyllið inn í reitina eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-create-service-items-within-a-service-order"></a>Þjónustuvörur stofnaðar út frá þjónustupöntunum  
Þegar tekið er við vöru til þjónustu og þarf að skrá hana sem þjónustuvöru er hægt að stofna þjónustuvöru á síðunum **Þjónustupöntun** eða **Þjónustutilboð**.  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Þjónustupantanir** og svo velja viðeigandi tengil.  
2. Fyllið inn í reitina eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. Veljið aðgerðina **Stofna þjónustuvara**.  

    Númeri er sjálfkrafa úthlutað til þjónustuvörunnar og þjónustuvöruspjald er stofnað. Reiturinn **Nr. þjónustuvöru** er fylltur út með númeri nýju þjónustuvörunnar.

## <a name="to-create-a-service-item-when-shipping-items"></a>Þjónustuvörur stofnaðar þegar vörur eru sendar:  
Þegar vörur eru sendar, annaðhvort með því að bóka sölupantanir eða sölureikninga eru sendu vörurnar sjálfkrafa skráðar sem þjónustuvörur að uppfylltum eftirfarandi skilyrðum. Varan verður að tilheyra þjónustuvöruflokki með gátmerki í reitnum **Stofna þjónustuvöru**. Ef vörurnar eru með raðnúmer skráð á síðunni **Vörurakningarlínur** eru þessar upplýsingar afritaðar sjálfvirkt í reitinn Raðnr. á þjónustuvöruspjaldinu þegar þjónustuvörur eru stofnaðar.  

Eftirfarandi aðferð sýnir hvernig stofna má þjónustuvöru þegar sölupöntunarvara er send.  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, færa inn **Sölupantanir** og velja síðan viðkomandi tengil.  
2. Viðeigandi sölupöntun er opnuð.  
3. Veljið aðgerðina **bóka** eða **Bóka og prenta**.  
4. Velja **Afhenda** eða **Afhenda og reikningsfæra** aðgerðina.  
5. Þjónustuvörur eru stofnaðar sjálfkrafa fyrir vörurnar í pöntuninni svo fremi að þær tilheyri þjónustuvöruflokki sem settur hefur verið upp til að stofna þjónustuvörur. Ef sérstök raðnúmer eru skráð á síðunni **Vörurakningarlínur** verður þeim úthlutað til þessum þjónustuvörum eins og við á.  

> [!NOTE]  
>  Ef vara er uppskrift og búið er að opna uppskriftina eru vörurnar meðhöndlaðar eins og um venjulegar vörur væri að ræða. Kerfið stofnar þjónustuvörur eftir skilyrðinu um þjónustuvöruflokk, og ef vill, raðnúmer. Ef þjónustuvara er aukinheldur stofnuð fyrir opna uppskrift sem er samsett úr öðrum uppskriftaríhlutum eru vörur sem þjónustuvöruíhluti stofnaðar fyrir opna uppskriftarþjónustuvöru.  
>   
>  Ef vara er uppskrift og ekki búið að opna uppskriftina eru þjónustuvörur stofnaðar fyrir hana eftir skilyrðinu um þjónustuvöruflokk, og ef vill, raðnúmer.  

## <a name="to-insert-a-starting-fee-for-a-service-item"></a>Upphafsgjald vegna þjónustuvöru sett inn:
1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Þjónustuverk** og svo velja viðeigandi tengil.
2. Velja aðgerðina **Vöruvinnublað**.
3. Velja þjónustulínuna og síðan **Aðgerðir**, velja **Aðgerðir** og síðan velja **Setja inn upphafsgjald** aðgerðina.  

    Kerfið setur inn þjónustulínu af gerðinni **Kostnaður** með upphafsgjaldinu. Upphafsgjaldið á við þá þjónustuvöru sem valin var.

## <a name="see-also"></a>Sjá einnig  
[Setja upp þjónustuvörur og íhluti þjónustuvara](service-how-setup-service-items.md)  
[Þjónustustýring sett upp](service-setup-service.md)  
[Þjónustukerfi](service-service.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]