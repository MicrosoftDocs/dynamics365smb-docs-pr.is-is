---
title: "Setja upp vörueigindir og úthluta þeim á vörur| Microsoft Docs"
description: "Lýsir því hvernig á að setja upp gildi vörueiginda, til dæmis sem hægt er nota sem leitarorð, og úthluta þeim á vörur og vöruflokka."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: categories, search words, facets
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: be7d4df5614de4c9726dea7fab8e1bdbc5c333b6
ms.contentlocale: is-is
ms.lasthandoff: 03/22/2018

---
# <a name="work-with-item-attributes"></a>Vinna með vörueigindir
Þegar viðskiptamaður gerir fyrirspurn um vöru, annað hvort í beinum samskiptum eða í innbyggðri vefverslun getur hann spurt um vöruna eða leitað samkvæmt eiginleikum, t.d. hæð og árgerð. Til að veita þessa þjónustu við viðskiptamanninn er hægt að úthluta vörum mismunandi eigindargildum sem er svo hægt að nota við leit að vörum.

Einnig er hægt að úthluta vörueigindum á vöruflokka, sem síðan eiga við um vörur sem nota vöruflokka. Frekari upplýsingar eru í [Flokka vöru](inventory-how-categorize-items.md).

> [!Tip]  
> Ef þú setur myndir í viðhengi vöru, getur Myndgreiningaviðbótin greint eigindir á myndinni og lagt til eigindirnar svo þú getir ákveðið hvort eigi að úthluta þeim eður ei. Viðbótin er tilbúin til notkunar. Þú þarft bara að virkja hana. Nánari upplýsingar eru í [Myndgreiningarviðbót fyrir Microsoft Business Central](ui-extensions-image-analyzer.md).

## <a name="to-create-item-attributes"></a>Að búa til vörueigind
1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Vörueigindir** og velja svo viðeigandi tengil.
2. Í glugganum **Vörueigindir** skal velja **Nýtt**.
3. Í glugganum **vörueigind** þarf að fylla reitina út eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
>   Athugasemd: Ef valið er **Kostur** á svæðinu **Tegund** er hægt að velja aðgerðina **Eigindargildi vöru** til að stofna gildi fyrir vörueigindina. Nánari upplýsingar eru í hlutanum "Stofna gildi fyrir vörueigindir af gerðinni valkostur".  

## <a name="to-create-values-for-item-attributes-of-type-option"></a>Stofna gildi fyrir vörueigindir af gerðinni valkostur.
1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Vörueigindir** og velja svo viðeigandi tengil.
2. Í **Vörueigindir** glugganum er valin vörueigind af gerðinni **Valkostir** sem þú vilt búa til gildi fyrir og svo velja **Eigindargildi** aðgerðina.
3. Í glugganum **vörueigindagildi** þarf að fylla reitina út eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-assign-item-attributes-to-items"></a>Að úthluta vörueigindum á vörur
1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Vörur** og velja svo viðeigandi tengil.
2. Í glugganum **Vörur** skal velja vöruna sem á að úthluta vörueigindum á og velja síðan aðgerðina **Eigindir**.
3. Í glugganum **vörueigindagildi** skal velja aðgerðina **Nýtt**.
4. Veldu leitarhnappinn í reitnum **Eigind** og veldu fyrirliggjandi vörueigind. Einnig má velja **Nýtt** aðgerðina til að stofna fyrst nýjan vörueigind eins og útskýrt er í "Stofna vörueigind" hlutanum.
5. Í reitnum **Gildi** er fært inn vörueigindagildi, s.s. „2010“ fyrir gildið **Árgerð**.
6. Fyrir vörueigind af gerðinni **Valkostur**, veldu hnappinn uppfletting í reitnum **Gildi** og veldu vörueigindargildi. Einnig má velja á **Nýtt** aðgerð til að stofna fyrst nýjan vörueigindargildi eins og útskýrt er í "Stofna gildi fyrir vörueigindir af gerðinni valkostur" hlutanum.
7. Liðir 4-6 eru endurteknir fyrir allar vörueigindir sem á að úthluta á vöru.

## <a name="to-assign-item-attributes-to-item-categories"></a>Að úthluta vörueigindum á vöruflokka
1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Vörurflokkar** og velja svo viðeigandi tengil.
2. Í glugganum **vöruflokkar** skal velja vöruflokk sem á að úthluta vörueigindum á og velja síðan aðgerðina **breyta**.
3. Í glugganum **vöruflokkaspjald** á flýtiflipanum **eigind** skal velja aðgerðina **Nýtt**.
4. Veldu leitarhnappinn í reitnum **Eigind** og veldu fyrirliggjandi vörueigind. Einnig má velja á **Nýtt** aðgerð til að stofna fyrst nýjan vörueigind eins og útskýrt er í "Stofna vörueigind" hlutanum.
5. Í reitnum **Sjálfgefið gildi** skal velja hnappinn uppfletting og velja vörueigindargildi.
6. Liðir 4-5 eru endurteknir fyrir allar vörueigindir sem á að úthluta á vöruflokk.

> [!NOTE]  
>   Vörueigindum fyrir vöruflokka yfirvöru verður afritaður á vöruflokka undireiningar. Þetta er tilgreint með reitnum **afritað Úr** í **Eigindum** Flýtiflipa. Frekari upplýsingar eru í [Flokka vörur](inventory-how-categorize-items.md).

## <a name="to-filter-by-item-attributes"></a>Afmarka eftir vörueigind
1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Vörur** og velja svo viðeigandi tengil.
2. Í glugganum **Vörur** skal velja aðgerðina **Afmarka eftir eigindum**.
3. Í glugganum **Afmarka vöru eftir eigind** skal velja uppflettihnappinn á svæðinu **Eigind** og velja síðan vörueigind.
4. Í reitnum **Gildi** skal velja hnappinn uppfletting og velja eigindargildi til að afmarka vörur eftir.

    > [!NOTE]  
    >   Aðeins er hægt að velja gildi beint fyrir vörueigindir sem hafa föst gildi, til dæmis lit. Fyrir vörueigindir sem hafa breytileg gildi, til dæmis breidd, verður að tilgreina eigindargildi vöru eftir fyrsta val á skilyrði. Sjá skref 5.
5. Í reitnum **Gildi** fyrir breytilega vörueigind skal velja hnappinn uppfletting.
6. Í glugganum **Tilgreina afmörkunargildi** á svæðinu **Skilyrði** skal velja felliörina og velja skilyrði.
7. Í reitnum **Virði** skal færa eigindargildi til að afmarka vörur með.

    **Dæmi**: Til að afmarka vörur þar sem efnislýsing hefst með "blátt", skal fylla inn í reitina sem hér segir: Reiturinn **Eigind**: Efnislýsing, reiturinn **Skilyrði**: Hefst með, reiturinn **Virði**: Blátt.
8. Velja hnappinn **Í lagi**.   

Vörur í glugganum **Vörur** eru afmarkaðar eftir tilgreindum eigindagildum vörunnar.

## <a name="see-also"></a>Sjá einnig
[Flokka vörur](inventory-how-categorize-items.md)    
[Skrá nýjar vörur](inventory-how-register-new-items.md)  
[Birgðir](inventory-manage-inventory.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

