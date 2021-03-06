---
title: Nota millivísanir vöru
description: Setjið upp tilvísanir á milli lýsinganna sem þú og lánardrottinn notið fyrir vöru þannig að hægt sé að setja inn vörulýsingu lánardrottins í innkaupaskjölum.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: item reference, cross reference, inventory
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 0a9f84522598344435ad9c1263fe8cdea2e2a1e0
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5785649"
---
# <a name="use-item-cross-references"></a>Nota millivísanir vöru
Ef sett er upp millivísun milli vörulýsingar sem er notuð fyrir vöru og lýsingu sem lánardrottinn þessarar vöru notar, þá er vörulýsing lánardrottins sjálfkrafa færð inn fyrir innkaupaskjöl lánardrottins þegar **Millivísunarnr.** er fyllt út. . Sama virknin gildir um númer viðskiptavina í söluskjölum.

Eftirfarandi ferli sýna hvernig á að nota millivísanir vöru innkaupamegin. Skrefin eru svipuð sölumegin.

> [!NOTE]
> Það er að verða algengara að vörukenni á borð við GTIN eða GUID innihaldi 30 eða fleiri stafi, sem er meira en núverandi eiginleiki fyrir millivísanir á vörum getur ráðið við. Ef nauðsynlegt er að nota tilvísanir sem innihalda fleiri en 30 stafi getur stjórnandinn kveikt á eiginleikanum **Skrifa lengri vörutilvísun** á síðunni [Eiginleikastjórnun](https://businesscentral.dynamics.com/?page=2610) (tengillinn krefst þess að þú sért með [!INCLUDE[prod_short](includes/prod_short.md)]-leigjanda). Hvernig tilvísanir eru notaðar breytist ekki en heiti hluta eins og síður og hnappar gera það. Til dæmis verður síðan **Millitilvísanafærslur vöru** að síðunni **Vörutilvísanafærslur**.

## <a name="to-set-up-an-item-cross-reference-to-a-vendors-item-description"></a>Að setja upp millivísun vöru í vörulýsingu lánardrottins

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Vara** og veldu síðan tengda tengilinn.
2. Opnaðu spjaldið fyrir vöru þar sem á að búa til millivísun á vörulýsingu sem lánardrottinn notar fyrir þessa vöru.
3. Veldu aðgerðina **Millivísanir**.

     Ef ekki er hægt að finna aðgerðina **Millivísanir** skal velja til að skoða fleiri valkosti og finna hana síðan undir **Tengd** > **Vara**.
  
4. Í nýrri línu á síðunni **Færslur fyrir millivísun vöru** skal fylla í reitina eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].

## <a name="to-enter-a-vendors-item-description-on-a-purchase-order"></a>Að færa vörulýsingu lánardrottins inn á innkaupapöntun

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Innkaupapantanir** og veldu síðan tengda tengilinn.
2. Stofnaðu innkaupapöntun fyrir lánardrottin sem þú setur upp millivísun vöru fyrir í ferlinu hér á undan.
3. Stofnaðu innkaupalínu fyrir vöruna sem þú setur upp millivísun vöru fyrir í ferlinu hér á undan.
4. Í **Millivísunarnr.** reitnum skal velja millivísun vörunnar sem þú stofnaðir og velja síðan hnappinn **Í lagi**.

Skrifað er yfir reitinn **Lýsing** í línunni með vörulýsingu lánardrottins eins og er uppsett í færslu fyrir millivísun vörunnar.

## <a name="see-also"></a>Sjá einnig
[Skrá nýjar vörur](inventory-how-register-new-items.md)  
[Birgðir](inventory-manage-inventory.md)  
[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]