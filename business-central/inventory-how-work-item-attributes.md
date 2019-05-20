---
title: Setja upp vörueigindir og úthluta þeim á vörur| Microsoft Docs
description: Lýsir því hvernig á að setja upp gildi vörueiginda, til dæmis sem hægt er nota sem leitarorð, og úthluta þeim á vörur og vöruflokka.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: categories, search words, facets
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 7d35f7c91792d9fe8eea87a4c63f8fd637a94fd1
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/29/2019
ms.locfileid: "1243964"
---
# <a name="work-with-item-attributes"></a>Vinna með vörueigindir
Þegar viðskiptamaður gerir fyrirspurn um vöru, annað hvort í beinum samskiptum eða í innbyggðri vefverslun getur hann spurt um vöruna eða leitað samkvæmt eiginleikum, t.d. hæð og árgerð. Til að veita þessa þjónustu við viðskiptamanninn er hægt að úthluta vörum mismunandi eigindargildum sem er svo hægt að nota við leit að vörum.

Einnig er hægt að úthluta vörueigindum á vöruflokka, sem síðan eiga við um vörur sem nota vöruflokka. Frekari upplýsingar eru í [Flokka vöru](inventory-how-categorize-items.md).

> [!Tip]  
> Ef þú setur myndir í viðhengi vöru, getur Myndgreiningaviðbótin greint eigindir á myndinni og lagt til eigindirnar svo þú getir ákveðið hvort eigi að úthluta þeim eður ei. Viðbótin er tilbúin til notkunar. Þú þarft bara að virkja hana. Nánari upplýsingar er að finna í [myndgreiningarviðbótinni](ui-extensions-image-analyzer.md).

## <a name="to-create-item-attributes"></a>Að búa til vörueigind
1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Vörueigindir** og veldu síðan tengda tengilinn.
2. Á síðunni **Vörueigindir** skal velja **Nýtt**.
3. Á síðunni **vörueigind** þarf að fylla reitina út eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
>   Athugasemd: Ef valið er **Kostur** á svæðinu **Tegund** er hægt að velja aðgerðina **Eigindargildi vöru** til að stofna gildi fyrir vörueigindina. Nánari upplýsingar eru í [Að stofna gildi fyrir vörueigindir af gerðinni valkostur](inventory-how-work-item-attributes.md#to-create-values-for-item-attributes-of-type-option).  

## <a name="to-create-values-for-item-attributes-of-type-option"></a>Stofna gildi fyrir vörueigindir af gerðinni valkostur.
1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Vörueigindir** og veldu síðan tengda tengilinn.
2. Á síðunni **Vörueigindir** er valin vörueigind af gerðinni **Valkostur** sem á að stofna gildi fyrir og veljið síðan aðgerðina **Eigindargildi vöru**.
3. Á síðunni **vörueigindagildi** þarf að fylla reitina út eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-assign-item-attributes-to-items"></a>Að úthluta vörueigindum á vörur
1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Vörur** og veldu síðan tengda hlekkinn.
2. Á síðunni **Vörur** skal velja vöruna sem á að úthluta vörueigindum á og velja síðan aðgerðina **Eigindir**.
3. Á síðunni **vörueigindagildi** skal velja aðgerðina **Nýtt**.
4. Veldu leitarhnappinn í reitnum **Eigind** og veldu fyrirliggjandi vörueigind. Einnig má velja **Nýtt** aðgerðina til að stofna fyrst nýja vörueigind eins og útskýrt er í [Stofna vörueigind](inventory-how-work-item-attributes.md#to-create-item-attributes).
5. Í reitnum **Gildi** er fært inn vörueigindagildi, s.s. „2010“ fyrir gildið **Árgerð**.
6. Fyrir vörueigind af gerðinni **Valkostur**, veldu hnappinn uppfletting í reitnum **Gildi** og veldu vörueigindargildi. Einnig má velja á **Nýtt** aðgerð til að stofna fyrst nýtt vörueigindargildi eins og útskýrt er í [Stofna gildi fyrir vörueigindir af gerðinni valkostur](inventory-how-work-item-attributes.md#to-assign-item-attributes-to-items).
7. Liðir 4-6 eru endurteknir fyrir allar vörueigindir sem á að úthluta á vöru.

## <a name="to-assign-item-attributes-to-item-categories"></a>Að úthluta vörueigindum á vöruflokka
1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Vöruflokkar** og veldu síðan tengda tengilinn.
2. Á síðunni **vöruflokkar** skal velja vöruflokk sem á að úthluta vörueigindum á og velja síðan aðgerðina **breyta**.
3. Á síðunni **vöruflokkaspjald** á flýtiflipanum **eigind** skal velja aðgerðina **Nýtt**.
4. Veldu hnappinn AssistEdit í reitnum **eigind** og veldu fyrirliggjandi vörueigind. Einnig má velja **Nýtt** aðgerðina til að stofna fyrst nýja vörueigind eins og útskýrt er í [Stofna vörueigind](inventory-how-work-item-attributes.md#to-create-item-attributes).
5. Í reitnum **Sjálfgefið gildi** skal velja hnappinn uppfletting og velja vörueigindargildi.
6. Liðir 4-5 eru endurteknir fyrir allar vörueigindir sem á að úthluta á vöruflokk.

> [!NOTE]  
>   Vörueigindum fyrir vöruflokka yfirvöru verður afritaður á vöruflokka undireiningar. Þetta er tilgreint með reitnum **afritað Úr** í **Eigindum** Flýtiflipa. Frekari upplýsingar eru í [Flokka vörur](inventory-how-categorize-items.md).

## <a name="to-filter-by-item-attributes"></a>Afmarka eftir vörueigind
1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Vörur** og veldu síðan tengda hlekkinn.
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
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
