---
title: Búa til standandi samsetningarpantanir
description: Búa til standandi sölupantanir fyrir sérsniðnar samsetningaríhluti áður en gerðar eru reglulegar eiginlegar sölupantanir í samræmi við standandi pöntunarsamninginn.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'kit, kitting'
ms.search.form: '900, 901, 902, 903, 904, 907, 910, 916, 920, 921, 922, 923, 940, 941, 942, 930, 931, 932, 914, 915, 905'
ms.date: 04/01/2021
ms.author: edupont
---
# <a name="create-blanket-assembly-orders"></a><a name="create-blanket-assembly-orders"></a>Búa til standandi samsetningarpantanir

Hægt er að nota samsetningarstjórnun til að sérsníða samsetningaríhlut eftir beiðni viðskiptavinar á meðan söluferlinu stendur. Frekari upplýsingar eru í [Selja hluti sem eru settir saman í pöntun](assembly-how-to-sell-items-assembled-to-order.md).  

 Eins og fyrir aðrar tegundir vöru, er einnig hægt að stofna standandi sölupantanir fyrir sérsniðnar samsetningarvörur áður en gerðar eru reglulegar eiginlegar sölupantanir í samræmi við standandi pöntunarsamninginn. Þetta ferli felur í sér nokkur aukaskref í samanburði við stofnun venjulegrar standandi sölupöntunar, og notar afbrigði tengdrar samsetningarpöntunar, sem er standandi samsetningarpöntun.

> [!NOTE]  
>  Eins og allar standandi pantanir er magn í standandi samsetningarpöntunum aðeins spár og er ekki tilbúið fyrr en þeim er breytt í raunverulegar samsetningarpantanir. Þess vegna eru pöntunaraðgerðir, eins og útreikningur á tiltæku magni, frátektir og vörurakning, ekki virkar á standandi samsetningarpöntunum.  

## <a name="to-create-a-blanket-assembly-order-for-an-assemble-to-order-item"></a><a name="to-create-a-blanket-assembly-order-for-an-assemble-to-order-item"></a>Til að stofna standandi samsetningarpöntun fyrir samsetningu\-í\-vörupöntun

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Standandi sölupantanir** og velja síðan viðkomandi tengil.  
2. Stofna nýja standandi sölupöntun með eina línu fyrir samsetningu vöru. Frekari upplýsingar eru í [Stofna standandi sölupantanir](sales-how-to-create-blanket-sales-orders.md).  
3. Í reitnum **Magn sem setja á saman í pöntun** í standandi samsetningarpöntunarlínu skal slá inn heildarmagn.

    > [!NOTE]  
    >  Ekki ætti að stofna samninga fyrir standandi pöntun fyrir hlutamagn. Því verður að færa inn sama magn og fært var inn í reitinn **Magn** í línu standandi sölupöntunar.  

4. Veldu aðgerðina **Setja saman í pöntun** og veldu síðan aðgerðina **Setja saman í pöntunarlínu**. Að öðrum kosti skal velja reitinn **Magn til samsetningar til pöntunar** í línunni.  
5. Á síðunni **Setja saman í pöntunarlínu** endurskoðið og breytið samsetningu pöntunalína samkvæmt samningi standandi pöntunar sem hefur verið gerður við viðskiptamanninn. Ef þú vilt skoða fleiri upplýsingar skaltu velja aðgerðina **Sýna skjal** til að opna alla standandi samsetningarpöntunina. Ekki er hægt að breyta innihaldi i flestum reitum, og ekki er hægt að bóka.  
6. Þegar búið er að leiðrétta samsetningarpöntunarlínur samkvæmt standandi pöntunarsamningnum skal loka síðunni **Sameina-í-pöntun línur** til að fara aftur á síðuna **Standandi sölupöntun**.  
7. Þegar viðskiptamaður biður um að fá að búa til sölupöntun sem byggir á standandi sölupöntuninni sem fallist var á skal búa til sölupöntun fyrir umsamdar samsetningarvöru eða vörur. Frekari upplýsingar eru í [Stofna standandi sölupantanir](sales-how-to-create-blanket-sales-orders.md).

Tengd standandi samsetningartilboð og allar sérstillingar tengjast við þessa nýju sölupöntun til undirbúnings á samsetningu vöru eða vörum sem á að selja.  

## <a name="see-also"></a><a name="see-also"></a>Sjá einnig .

[Reikningsfærðar standandi sölupantanir búnar til](sales-how-to-create-blanket-sales-orders.md)  
[Samsetningardeild](assembly-assemble-items.md)  
[Vinna með samsetningaruppskriftir](assembly-how-work-assembly-boms.md)  
[Birgðir](inventory-manage-inventory.md)  
[Yfirlit yfir](design-details-warehouse-management.md)
[vöruhúsastjórnun vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
