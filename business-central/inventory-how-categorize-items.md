---
title: Skipuleggja vörur í flokkum
description: 'Til að fá hjálp við að leita að og finna vörur, er hægt að úthluta eiginleikum vöru og skipuleggja vörur í flokkum.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'category, search, attribute, facet'
ms.search.form: '5730, 5733, 5401'
ms.date: 06/10/2024
ms.service: dynamics-365-business-central
---
# <a name="categorize-items"></a>Flokka vörur

Til að viðhalda yfirliti yfir vörurnar og hjálpa til við að raða og finna vörur er gagnlegt að skipuleggja vörur í vöruflokkum.

Til að finna vörur eftir eiginleika er hægt að úthluta vörueigindum á vörur og einnig vöruflokka. Frekari upplýsingar eru í [Vinna með vörueigindir](inventory-how-work-item-attributes.md).
<br><br>  

> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4j4mo?rel=0]

## <a name="to-create-an-item-category"></a>Að búa til vöruflokka
1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Vöruflokkar** og velja síðan viðkomandi tengil.
2. Á síðunni **vöruflokkar** skal velja aðgerðina **Nýtt**.
3. Á síðunni **vöruflokkaspjald**, á flipanum **Almennt**, eru eftirfarandi reitir fylltir út. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Í **eigindir** Flýtiflipanum skal tilgreina hvers kyns vörueigindum fyrir vöruflokk. Nánari upplýsingar [eru í Til að úthluta vörueigindum á vöruflokka](inventory-how-work-item-attributes.md#assign-item-attributes-to-item-categories).

> [!NOTE]  
> Hafi vöruflokkur yfirvöruflokk eins og gefið er til kynna með reitnum **yfirtegund** þá eru allar vörueigindir sem eru úthlutaðar á þann yfirflokk vöru forútfylltar á flýtiflipanum **eigindir**.

> [!NOTE]  
> Vörueigindir sem á að úthluta á vöruflokk mun sjálfkrafa gilda um vöruna sem vöruflokknum er úthlutað á.

Ef þú skiptir um skoðun varðandi vöruflokk, getur þú eytt honum. Ef tegundinni er hins vegar úthlutað á vöru verður að fjarlægja þá úthlutun fyrirfram.

## <a name="to-assign-an-item-category-to-an-item"></a>Að úthluta vöruflokki á vöru.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Vörur** og velja síðan viðkomandi tengil.
2. Opna skal birgðaspjaldið fyrir vöruna sem á að úthluta á vöruflokk.
3. Veldu leitarhnappinn í reitnum **Vöruflokkskóði** og veldu fyrirliggjandi vöruflokk. Einnig má velja á **Nýtt** aðgerð til að stofna fyrst nýjan vöruflokk eins og útskýrt er í [Stofna vöruflokk](inventory-how-categorize-items.md#to-create-an-item-category).

## <a name="categories-attributes-and-variants"></a>Flokkar, eigindir og afbrigði

[!INCLUDE[inventory_variant](includes/inventory_variant.md)]

## <a name="see-also"></a>Sjá einnig .

[Vinna með vörueigindir](inventory-how-work-item-attributes.md)  
[Stjórna afurðarafbrigðum](inventory-item-variants.md)  
[Skrá nýjar vörur](inventory-how-register-new-items.md)  
[Birgðir](inventory-manage-inventory.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
