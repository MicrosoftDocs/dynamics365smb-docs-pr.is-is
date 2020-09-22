---
title: Hvernig á að búa til standandi samsetningarpantanir | Microsoft Docs
description: Búa til standandi sölupantanir fyrir sérsniðnar samsetningaríhluti áður en gerðar eru reglulegar eiginlegar sölupantanir í samræmi við standandi pöntunarsamninginn.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: kit, kitting
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 9a0f3c81aad31eb51d282479e56acbfc935bf1dd
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/09/2020
ms.locfileid: "3786072"
---
# <a name="create-blanket-assembly-orders"></a>Búa til standandi samsetningarpantanir
Hægt er að nota samsetningarstjórnun til að sérsníða samsetningaríhlut eftir beiðni viðskiptavinar á meðan söluferlinu stendur. Frekari upplýsingar eru í [Selja hluti sem eru settir saman í pöntun](assembly-how-to-sell-items-assembled-to-order.md).  

 Eins og fyrir aðrar tegundir vöru, er einnig hægt að stofna standandi sölupantanir fyrir sérsniðnar samsetningarvörur áður en gerðar eru reglulegar eiginlegar sölupantanir í samræmi við standandi pöntunarsamninginn. Þetta ferli felur í sér nokkur aukaskref í samanburði við stofnun venjulegrar standandi sölupöntunar, og notar afbrigði tengdrar samsetningarpöntunar, sem er standandi samsetningarpöntun.

> [!NOTE]  
>  Eins og allar standandi pantanir er magn í standandi samsetningarpöntunum aðeins spár og er ekki tilbúið fyrr en þeim er breytt í raunverulegar samsetningarpantanir. Þess vegna eru pöntunaraðgerðir, eins og útreikningur á tiltæku magni, frátektir og vörurakning, ekki virkar á standandi samsetningarpöntunum.  

## <a name="to-create-a-blanket-assembly-order-for-an-assemble-to-order-item"></a>Til að stofna standandi samsetningarpöntun fyrir samsetningu\-í\-vörupöntun  
1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Standandi sölupantanir** og veldu síðan tengda tengilinn.  
2. Stofna nýja standandi sölupöntun með eina línu fyrir samsetningu vöru. Frekari upplýsingar eru í [Stofna standandi sölupantanir](sales-how-to-create-blanket-sales-orders.md).  
3. Í reitnum **Magn sem setja á saman í pöntun** í standandi samsetningarpöntunarlínu skal slá inn heildarmagn.

    > [!NOTE]  
    >  Ekki ætti að stofna samninga fyrir standandi pöntun fyrir hlutamagn. Því verður að færa inn sama magn og fært var inn í reitinn **Magn** í línu standandi sölupöntunar.  

4. Veldu aðgerðina **Setja saman í pöntun** og veldu síðan aðgerðina **Setja saman í pöntunarlínu**. Að öðrum kosti skal velja reitinn **Magn til samsetningar til pöntunar** í línunni.  
5. Á síðunni **Setja saman í pöntunarlínu** endurskoðið og breytið samsetningu pöntunalína samkvæmt samningi standandi pöntunar sem hefur verið gerður við viðskiptamanninn. Ef þú vilt skoða fleiri upplýsingar skaltu velja aðgerðina **Sýna skjal** til að opna alla standandi samsetningarpöntunina. Ekki er hægt að breyta innihaldi i flestum reitum, og ekki er hægt að bóka.  
6. Þegar búið er að leiðrétta samsetningarpöntunarlínur samkvæmt standandi pöntunarsamningnum skal loka síðunni **Sameina-í-pöntun línur** til að fara aftur á síðuna **Standandi sölupöntun**.  
7. Þegar viðskiptamaður biður um að fá að búa til sölupöntun sem byggir á standandi sölupöntuninni sem fallist var á skal búa til sölupöntun fyrir umsamdar samsetningarvöru eða vörur. Frekari upplýsingar eru í [Stofna standandi sölupantanir](sales-how-to-create-blanket-sales-orders.md).

Tengd standandi samsetningartilboð og allar sérstillingar tengjast við þessa nýju sölupöntun til undirbúnings á samsetningu vöru eða vörum sem á að selja.  

## <a name="see-also"></a>Sjá einnig
[Reikningsfærðar standandi sölupantanir búnar til](sales-how-to-create-blanket-sales-orders.md)  
[Samsetningardeild](assembly-assemble-items.md)  
[Vinna með uppskriftir](inventory-how-work-BOMs.md)  
[Birgðir](inventory-manage-inventory.md)  
[Hönnunarupplýsingar vöruhúsakerfi](design-details-warehouse-management.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
