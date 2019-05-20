---
title: Skipuleggja hluti í flokkum| Microsoft Docs
description: Til að fá hjálp við að leita að og finna vörur, er hægt að úthluta eiginleikum vöru og skipuleggja vörur í flokkum.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: category, search, attribute, facet
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: dd5ca3a3e109f565448d0c5698a6e1ee6dce331c
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/29/2019
ms.locfileid: "1240134"
---
# <a name="categorize-items"></a>Flokka vörur
Til að hafa yfirlit yfir vörur og til að hjálpa til við röðun og leit í vörum er gagnlegt að skipuleggja vörur í vöruflokka.

Til að finna vörur eftir eiginleika er hægt að úthluta vörueigindum á vörur og einnig vöruflokka. Frekari upplýsingar eru í [Vinna með vörueigindir](inventory-how-work-item-attributes.md).

## <a name="to-create-an-item-category"></a>Að búa til vöruflokka
1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Vöruflokkar** og veldu síðan tengda tengilinn.
2. Á síðunni **vöruflokkar** skal velja aðgerðina **Nýtt**.
3. Á síðunni **vöruflokkaspjald**, á flipanum **Almennt**, eru eftirfarandi reitir fylltir út. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Í **eigindir** Flýtiflipanum skal tilgreina hvers kyns vörueigindum fyrir vöruflokk. Frekari upplýsingar er að finna í [Að úthluta vörueigindum á vöruflokka](inventory-how-work-item-attributes.md#to-assign-item-attributes-to-item-categories).

> [!NOTE]  
>   Hafi vöruflokkur yfirvöruflokk eins og gefið er til kynna með reitnum **yfirtegund** þá eru allar vörueigindir sem eru úthlutaðar á þann yfirflokk vöru forútfylltar á flýtiflipanum **eigindir**.

> [!NOTE]  
>   Vörueigindir sem á að úthluta á vöruflokk mun sjálfkrafa gilda um vöruna sem vöruflokknum er úthlutað á.

## <a name="to-assign-an-item-category-to-an-item"></a>Að úthluta vöruflokki á vöru.
1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Vörur** og veldu síðan tengda hlekkinn.
2. Opna skal birgðaspjaldið fyrir vöruna sem á að úthluta á vöruflokk.
3. Veldu leitarhnappinn í reitnum **Vöruflokkskóði** og veldu fyrirliggjandi vöruflokk. Einnig má velja á **Nýtt** aðgerð til að stofna fyrst nýjan vöruflokk eins og útskýrt er í [Stofna vöruflokk](inventory-how-categorize-items.md#to-create-an-item-category).

## <a name="see-also"></a>Sjá einnig
[Vinna með vörueigindir](inventory-how-work-item-attributes.md)  
[Skrá nýjar vörur](inventory-how-register-new-items.md)  
[Birgðir](inventory-manage-inventory.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
