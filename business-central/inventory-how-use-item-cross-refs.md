---
title: Nota millivísanir vöru | Microsoft Docs
description: Ef sett er upp millivísun milli vörulýsingar sem er notuð fyrir vöru og lýsingu sem lánardrottinn þessarar vöru notar, þá er vörulýsing lánardrottins sjálfkrafa færð inn fyrir innkaupaskjöl lánardrottins þegar **Millivísunarnr.** er fyllt út. .
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 89a99080723ee57270583ee2f277250d767b8dde
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2020
ms.locfileid: "3181941"
---
# <a name="use-item-cross-references"></a>Nota millivísanir vöru
Ef sett er upp millivísun milli vörulýsingar sem er notuð fyrir vöru og lýsingu sem lánardrottinn þessarar vöru notar, þá er vörulýsing lánardrottins sjálfkrafa færð inn fyrir innkaupaskjöl lánardrottins þegar **Millivísunarnr.** er fyllt út. . Sama virknin gildir um númer viðskiptavina í söluskjölum.

Eftirfarandi ferli sýna hvernig á að nota millivísanir vöru innkaupamegin. Skrefin eru svipuð sölumegin.

## <a name="to-set-up-an-item-cross-reference-to-a-vendors-item-description"></a>Að setja upp millivísun vöru í vörulýsingu lánardrottins
1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Vara** og veldu síðan tengda tengilinn.
2. Opnaðu spjaldið fyrir vöru þar sem á að búa til millivísun á vörulýsingu sem lánardrottinn notar fyrir þessa vöru.
3. Veldu aðgerðina **Millivísanir**.
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
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
