---
title: Nota vörutilvísanir
description: Setjið upp tilvísanir á milli lýsinganna sem þú og lánardrottinn notið fyrir vöru til að setja inn vörulýsingu lánardrottins í innkaupaskjölum.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: item reference, cross reference, inventory
ms.date: 06/16/2021
ms.author: edupont
ms.openlocfilehash: 4eed6fce594b0b6835020fcdddb7275489b4d160
ms.sourcegitcommit: 6ad0a834fc225cc27dfdbee4a83cf06bbbcbc1c9
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/01/2021
ms.locfileid: "7588602"
---
# <a name="use-item-references"></a>Nota vörutilvísanir
Ef sett er upp tilvísun milli vörulýsingar sem er notuð fyrir vöru og lýsingu sem lánardrottinn þessarar vöru notar, þá er vörulýsing lánardrottins sjálfkrafa færð inn fyrir innkaupaskjöl lánardrottins þegar **Vöruvísunarnr.** er fyllt út. . Sama virknin gildir um númer viðskiptavina í söluskjölum.

Eftirfarandi ferli sýna hvernig á að nota vörutilvísanir innkaupamegin. Skrefin eru svipuð sölumegin.

> [!NOTE]
> Ekki öll fyrirtæki nota vörutilvísanir og til þess að lágmarka óreiðu á síðum höfum við falið tengda reiti og aðgerðir. Ef þú ákveður að nota það geturðu kveikt á **Nota vörutilvísanir** á síðunni **Birgðauppsetning**. Eftir að þú hefur virkjað vörutilvísanir verða reitir og aðgerðir í boði á birgðaspjaldinu, lánardrottnaspjaldinu og viðskiptamannspjaldinu og í sölu- og innkaupaskjölum.

## <a name="to-start-using-item-references"></a>Að byrja að nota vörutilvísanir
1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Uppsetning birgða** og velja síðan viðkomandi tengil.
2. Kveiktu á **Nota vörutilvísanir**.

## <a name="to-set-up-an-item-reference-to-a-vendors-item-description"></a>Að setja upp tilvísun vöru í vörulýsingu lánardrottins

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Vörur** og velja síðan viðkomandi tengil.
2. Opnaðu spjaldið fyrir vöru þar sem á að búa til tilvísun á vörulýsingu sem lánardrottinn notar fyrir þessa vöru.
3. Veldu aðgerðina **Vörutilvísanir**.

     Ef ekki er hægt að finna aðgerðina **Vörutilvísanir** skal velja til að skoða fleiri valkosti og finna hana síðan undir **Tengd** > **Vara**.
  
4. Í nýrri línu á síðunni **Færslur fyrir tilvísun vöru** skal fylla í reitina eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].

## <a name="to-enter-a-vendors-item-description-on-a-purchase-order"></a>Að færa vörulýsingu lánardrottins inn á innkaupapöntun

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Innkaupapantanir** og velja síðan viðkomandi tengil.
2. Stofnaðu innkaupapöntun fyrir lánardrottin sem þú setur upp tilvísun vöru fyrir í ferlinu hér á undan.
3. Stofnaðu innkaupalínu fyrir vöruna sem þú setur upp tilvísun vöru fyrir í ferlinu hér á undan.
4. Í **Vörutilvísunarnúmer** reitnum skal velja tilvísun vörunnar sem þú stofnaðir og velja síðan hnappinn **Í lagi**.

Skrifað er yfir reitinn **Lýsing** í línunni með vörulýsingu lánardrottins eins og er uppsett í færslu fyrir tilvísun vörunnar.

## <a name="see-also"></a>Sjá einnig
[Skrá nýjar vörur](inventory-how-register-new-items.md)  
[Birgðir](inventory-manage-inventory.md)  
[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]