---
title: Setja upp Vörueigindi og úthluta þeim á vörur
description: Lýsir því hvernig á að setja upp gildi vörueiginda, til dæmis sem hægt er nota sem leitarorð, og úthluta þeim á vörur og vöruflokka.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: categories, search words, facets
ms.search.forms: 7507, 7509, 7506, 7505, 7503, 7502, 7510, 7504, 7501, 7500, 9110, 5734, 7508
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: cb907b4574126c23292e4b164505606a5ac404dd
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2022
ms.locfileid: "8516188"
---
# <a name="work-with-item-attributes"></a>Vinna með vörueigindir
Þegar viðskiptamaður gerir fyrirspurn um vöru, annað hvort í beinum samskiptum eða í innbyggðri vefverslun getur hann spurt um vöruna eða leitað samkvæmt eiginleikum, t.d. hæð og árgerð. Til að veita þessa þjónustu við viðskiptamanninn er hægt að úthluta vörum mismunandi eigindargildum sem er svo hægt að nota við leit að vörum.

Einnig er hægt að úthluta vörueigindum á vöruflokka, sem síðan eiga við um vörur sem nota vöruflokka. Frekari upplýsingar eru í [Flokka vöru](inventory-how-categorize-items.md).

> [!Tip]  
> Ef þú setur myndir í viðhengi vöru, getur Myndgreiningaviðbótin greint eigindir á myndinni og lagt til eigindirnar svo þú getir ákveðið hvort eigi að úthluta þeim eður ei. Viðbótin er tilbúin til notkunar. Þú þarft bara að virkja hana. Nánari upplýsingar er að finna í [myndgreiningarviðbótinni](ui-extensions-image-analyzer.md).

## <a name="to-create-item-attributes"></a>Að búa til vörueigind
1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Vörueigindir** og veldu síðan tengda tengilinn.
2. Á síðunni **Vörueigindir** skal velja **Nýtt**.
3. Á síðunni **vörueigind** þarf að fylla reitina út eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
>   Ef valið **er** í **reitnum Tegund** er hægt að velja **aðgerðina eigind gildi** vörunnar til að stofna gildi fyrir eigindina vara. Nánari upplýsingar eru í [Að stofna gildi fyrir vörueigindir af gerðinni valkostur](inventory-how-work-item-attributes.md#to-create-values-for-item-attributes-of-type-option).  

## <a name="to-create-values-for-item-attributes-of-type-option"></a>Stofna gildi fyrir vörueigindir af gerðinni valkostur.
1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Vörueigindir** og veldu síðan tengda tengilinn.
2. Á síðunni **Vörueigindir** er valin vörueigind af gerðinni **Valkostur** sem á að stofna gildi fyrir og veljið síðan aðgerðina **Eigindargildi vöru**.
3. Á síðunni **vörueigindagildi** þarf að fylla reitina út eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-assign-item-attributes-to-items"></a>Að úthluta vörueigindum á vörur
1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Vörur** og velja síðan viðkomandi tengil.
2. Á síðunni **Vörur** skal velja vöruna sem á að úthluta vörueigindum á og velja síðan aðgerðina **Eigindir**.
3. Á síðunni **vörueigindagildi** skal velja aðgerðina **Nýtt**.
4. Veldu leitarhnappinn í reitnum **Eigind** og veldu fyrirliggjandi vörueigind. Einnig má velja **Nýtt** aðgerðina til að stofna fyrst nýja vörueigind eins og útskýrt er í [Stofna vörueigind](inventory-how-work-item-attributes.md#to-create-item-attributes).
5. Í reitnum **Gildi** er fært inn vörueigindagildi, s.s. „2010“ fyrir gildið **Árgerð**.
6. Fyrir vörueigind af gerðinni **Valkostur**, veldu hnappinn uppfletting í reitnum **Gildi** og veldu vörueigindargildi. Einnig má velja á **Nýtt** aðgerð til að stofna fyrst nýtt vörueigindargildi eins og útskýrt er í [Stofna gildi fyrir vörueigindir af gerðinni valkostur](inventory-how-work-item-attributes.md#to-assign-item-attributes-to-items).
7. Liðir 4-6 eru endurteknir fyrir allar vörueigindir sem á að úthluta á vöru.

## <a name="to-assign-item-attributes-to-item-categories"></a>Að úthluta vörueigindum á vöruflokka
1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Vöruflokkar** og velja síðan viðkomandi tengil.
2. Á síðunni **vöruflokkar** skal velja vöruflokk sem á að úthluta vörueigindum á og velja síðan aðgerðina **breyta**.
3. Á síðunni **vöruflokkaspjald** á flýtiflipanum **eigind** skal velja aðgerðina **Nýtt**.
4. Veldu hnappinn AssistEdit í reitnum **eigind** og veldu fyrirliggjandi vörueigind. Einnig má velja **Nýtt** aðgerðina til að stofna fyrst nýja vörueigind eins og útskýrt er í [Stofna vörueigind](inventory-how-work-item-attributes.md#to-create-item-attributes).
5. Í reitnum **Sjálfgefið gildi** skal velja hnappinn uppfletting og velja vörueigindargildi.
6. Liðir 4-5 eru endurteknir fyrir allar vörueigindir sem á að úthluta á vöruflokk.

> [!NOTE]  
>   Vörueigindum fyrir vöruflokka yfirvöru verður afritaður á vöruflokka undireiningar. Þetta er tilgreint með reitnum **afritað Úr** í **Eigindum** Flýtiflipa. Frekari upplýsingar eru í [Flokka vörur](inventory-how-categorize-items.md).

## <a name="to-filter-by-item-attributes"></a>Afmarka eftir vörueigind
1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Vörur** og velja síðan viðkomandi tengil.
2. Á síðunni **Vörur** skal velja aðgerðina **Afmarka eftir eigindum**.
3. Á síðunni **Afmarka vöru eftir eigind** skal velja uppflettihnappinn á svæðinu **Eigind** og velja síðan vörueigind.
4. Í reitnum **Gildi** skal velja hnappinn uppfletting og velja eigindargildi til að afmarka vörur eftir.

    > [!NOTE]  
    >   Aðeins er hægt að velja gildi beint fyrir vörueigindir sem hafa föst gildi, til dæmis lit. Fyrir vörueigindir sem hafa breytileg gildi, til dæmis breidd, verður að tilgreina eigindargildi vöru eftir fyrsta val á skilyrði. Sjá skref 5.
5. Í reitnum **Gildi** fyrir breytilega vörueigind skal velja hnappinn uppfletting.
6. Á síðunni **Tilgreina afmörkunargildi** á svæðinu **Skilyrði** skal velja felliörina og velja skilyrði.
7. Í reitnum **Virði** skal færa eigindargildi til að afmarka vörur með.

    **Dæmi**: Til að afmarka vörur þar sem efnislýsing hefst með "blátt", skal fylla inn í reitina sem hér segir: Reiturinn **Eigind**: Efnislýsing, reiturinn **Skilyrði**: Hefst með, reiturinn **Virði**: Blátt.
8. Velja hnappinn **Í lagi**.   

Vörur á síðunni **Vörur** eru afmarkaðar eftir tilgreindum eigindagildum vörunnar.

## <a name="see-also"></a>Sjá einnig
[Flokka vörur](inventory-how-categorize-items.md)    
[Skrá nýjar vörur](inventory-how-register-new-items.md)  
[Birgðir](inventory-manage-inventory.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]