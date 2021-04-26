---
title: Skipuleggja hluti í flokkum| Microsoft Docs
description: Til að fá hjálp við að leita að og finna vörur, er hægt að úthluta eiginleikum vöru og skipuleggja vörur í flokkum.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: category, search, attribute, facet
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 55196b8026e5efc5a79ce1a547e2ff594fae231c
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5786024"
---
# <a name="categorize-items"></a>Flokka vörur

Til að hafa yfirlit yfir vörur og til að hjálpa til við röðun og leit í vörum er gagnlegt að skipuleggja vörur í vöruflokka.

Til að finna vörur eftir eiginleika er hægt að úthluta vörueigindum á vörur og einnig vöruflokka. Frekari upplýsingar eru í [Vinna með vörueigindir](inventory-how-work-item-attributes.md).
<br><br>  

> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4j4mo?rel=0]

## <a name="to-create-an-item-category"></a>Að búa til vöruflokka
1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Vöruflokkar** og veldu síðan tengda tengilinn.
2. Á síðunni **vöruflokkar** skal velja aðgerðina **Nýtt**.
3. Á síðunni **vöruflokkaspjald**, á flipanum **Almennt**, eru eftirfarandi reitir fylltir út. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Í **eigindir** Flýtiflipanum skal tilgreina hvers kyns vörueigindum fyrir vöruflokk. Frekari upplýsingar er að finna í [Að úthluta vörueigindum á vöruflokka](inventory-how-work-item-attributes.md#to-assign-item-attributes-to-item-categories).

> [!NOTE]  
> Hafi vöruflokkur yfirvöruflokk eins og gefið er til kynna með reitnum **yfirtegund** þá eru allar vörueigindir sem eru úthlutaðar á þann yfirflokk vöru forútfylltar á flýtiflipanum **eigindir**.

> [!NOTE]  
> Vörueigindir sem á að úthluta á vöruflokk mun sjálfkrafa gilda um vöruna sem vöruflokknum er úthlutað á.

Ef þú skiptir um skoðun varðandi vöruflokk, getur þú eytt honum. Ef honum hefur hinsvegar verið úthlutað á vöru þarf að fjarlægja þá úthlutun áður en vöruflokknum er eytt.

## <a name="to-assign-an-item-category-to-an-item"></a>Að úthluta vöruflokki á vöru.

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Vara** og veldu síðan tengda tengilinn.
2. Opna skal birgðaspjaldið fyrir vöruna sem á að úthluta á vöruflokk.
3. Veldu leitarhnappinn í reitnum **Vöruflokkskóði** og veldu fyrirliggjandi vöruflokk. Einnig má velja á **Nýtt** aðgerð til að stofna fyrst nýjan vöruflokk eins og útskýrt er í [Stofna vöruflokk](inventory-how-categorize-items.md#to-create-an-item-category).

## <a name="categories-attributes-and-variants"></a>Flokkar, eigindir og afbrigði

[!INCLUDE[inventory_variant](includes/inventory_variant.md)]

## <a name="see-also"></a>Sjá einnig

[Vinna með vörueigindir](inventory-how-work-item-attributes.md)  
[Skrá nýjar vörur](inventory-how-register-new-items.md)  
[Birgðir](inventory-manage-inventory.md)  
[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]