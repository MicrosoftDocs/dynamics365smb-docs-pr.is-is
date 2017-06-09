---
title: "Hvernig á að: Meðhöndla innkaupaskil eða afturkallanir| Microsoft Docs"
description: "Meðhöndlun innkaupaskila eða afturkallana"
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: cancel, undo, correct
ms.date: 03/29/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: f87b51ac746c6586e4ebb3b09aaa8d5ee7ac391d
ms.contentlocale: is-is
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-process-purchase-returns-or-cancellations"></a>Meðhöndlun innkaupaskila eða afturkallana
Ef skila á vörum til lánardrottins eða afturkalla þjónustu sem hefur verið keypt, er hægt að búa til og bóka kreditreikning sem tilgreinir breytingarnar sem óskað er eftir vegna hins upphaflega innkaupareiknings. Til að taka réttar innkaupareikningsupplýsingar með, er hægt að stofna innkaupakreditreikning úr bókaða innkaupareikningnum eða nota afritunaraðgerð

**Athugaðu**: Ef bókaður innkaupareikningur hefur ekki verið greiddur er hægt að nota aðgerðirnar **Leiðrétta** eða **Afturkalla** á bókuðu innkaupareikningnum til að afturkalla umræddar færslur sjálfkrafa. Þessir eiginleikar virka aðeins fyrir ógreidda reikninga og styðja ekki vöruskil að hluta eða afturkallanir. Nánari upplýsingar er að finna [hvernig á að: ógreiddir innkaupareikningar leiðréttir eða afturkallaðir](purchasing-how-correct-cancel-unpaid-purchase-invoices.md)

Venjulega, getur þú búið til innkaupakreditreikning sem svar við kreditreikningur sem lánardrottinn sendir þér, Innkaupakreditreikningurinn virkar eins og innra fylgiskjal fyrir bókahaldið um kreditreikningsferlið.

Breytingin gæti tengst öllum vörunum á hinum upphaflega innkaupareikningi eða aðeins sumum varanna. Hægt er að skila mótteknum vörum að hluta, eða fara fram á endurgreiðslu að hluta af móttekinni þjónustu. Í því tilviki, verður að breyta hinum afrituðu innkaupareikningsupplýsingum.

Auk upprunalega bókaðan innkaupareikning, er hægt að jafna innkaupakreditreikning við öðrum innkaupaskjölum, t.d. aðra bókaður innkaupareikningur, Því þú ert einnig að skila vörum sem voru afhentar með viðkomandi reikningur.

## <a name="to-create-a-purchase-credit-memo-from-a-posted-purchase-invoice"></a>Stofna nýjan innkaupakreditreikning úr bókaðan innkaupareikningur.
1. Efst í hægra horni skal velja reitinn **Leita að síðu eða skýrslu** táknið ![Leita að síðu eða skýrslu](media/ui-search/search_small.png "Leita að síðu eða skýrslu táknið"), færa **Innkaupakreditreikningar**, og velja síðan viðeigandi tengil.  
2. Í gluggann **Bókaðir innkaupareikningar** og veldu bókaða innkaupareikninginn sem á að bakfæra og veldu svo stofna aðgerðina **stofna leiðréttandi kkreditreikning**

    Flestir reitir á innkaupakreditreikningshausnum eru nú fylltir út með upplýsingum úr bókaður innkaupareikningur Hægt er að breyta allir reitir, til dæmis með nýjar upplýsingar sem endurspegla endursenda samkomulagið.
3. Breyta upplýsingum í línunum í samræmi við samninginn, eins og fjöldi þeirra vara sem skilað er eða upphæð sem á að endurgreiða.
4. Valið er **Jafna Færslur** aðgerð.
5. Í **Jafna Lánardr.færslur** glugganum, velja línan með bókaða innkaupaskjalið sem á að jafna við innkaup sölukreditreikning innkaupakreditreikning á og velja síðan aðgerðina **Jöfnunarkenni**. Númer innkaupakreditreikningsins er sett í reitinn **jöfnunarkenni**
6. Í reitnum  **Upphæð til jöfnunar** er rituð upphæðin sem á að jafna ef hún er lægri en upprunalega upphæðin.

    Neðst á **Jafna Lánardr.færslur** glugganum, er hægt að skoða heildarupphæðin sem á að nota til að bakfæra allar viðkomandi færslur, nefnilega þegar gildið í **Stöðu** reitnum er núll.
7. Velja hnappinn **Í lagi**. Þegar innkaupakreditreikningurinn er bókaður, verður hann jafnaður við tilgreinda bókaða innkaupaskjölin

    Þegar stofnaðar eða breyttar hafa verið línur fyrir innkaupakreditreikninga og ein eða fleiri jöfnun hefur verið tilgreind, er hægt að fara í að bóka innkaupakreditreikninginn.
8. Valið er **bóka ** aðgerð.

Bókuðu innkaupareikningarnir sem jafnaðir eru við kreditreikninginn eru nú bakfærðir. Ef þegar upprunalegi reikningurinn hefur þegar verið greiddur ætti lánardrottinn nú að endurgreiða greiðsluna. Ef kreditreikningurinn er aðeins fyrir hluta afurðarinnar á upprunalega reikningnum geturðu aðeins greitt eftirstandandi upphæð á upprunalega innkaupareikningnum til að loka honum.

Innkaupakreditreikningurinn er fjarlægður og skipt út fyrir nýtt fylgiskjal á lista bókaðra innkaupakreditreikninga.

## <a name="to-create-a-purchase-credit-memo-from-scratch"></a>Innkaupakreditreikningur búinn til frá byrjun.
1. Efst í hægra horni skal velja **Leita að síðu eða skýrslu** táknið ![Leita að síðu eða skýrslu](media/ui-search/search_small.png "Leita að síðu eða skýrslu táknið"), færa **Bókaðir innkaupareikningar**, og velja síðan viðeigandi tengil.
2. Valið er **Nýtt** aðgerð til að opna ný auður innkaupakreditreikningur.
3. Í reitnum **lánardrottins** er fært inn nafn núverandi lánardrottins.
4. Valið er **Afrita fylgiskjal** aðgerð.
5. Í glugganum **afrita innkaupaskjal** í **Gerð fylgiskjals** velurðu **Bókaður reikningur**.
6. Veljið **skjalanúmer** reitinn til að opna gluggann **Bókaðir innkaupareikningar** og síðan bókaða innkaupareikninginn sem inniheldur línur sem á að bakfæra.
7. Veljið gátreitinn **Endurreikna línur**, ef bókaða innkaupakreditreikningslínan sem var afrituð á að uppfærast með breytingum á vöruverði og kostnaðarverði síðan reikningurinn var bókaður.
8. Velja hnappinn **Í lagi**. Afrituðu reikningslínurnar eru settar inn í innkaupakreditreikninginn.
9. Ljúktu Innkaupakreditreikningur eins og útskýrt er í reitnum "Stofna nýjan innkaupakreditreikning úr bókaðan innkaupareikningur" hlutanum í þessu efnisatriði.

## <a name="see-also"></a>Sjá einnig
[Innkaup](purchasing-manage-purchasing.md)  
[Hvernig á að skrá kaup](purchasing-how-record-purchases.md)  
[Hvernig á að: Hvernig á að: Leiðrétta eða afturkalla ógreidda innkaupareikninga](purchasing-how-correct-cancel-unpaid-purchase-invoices.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

