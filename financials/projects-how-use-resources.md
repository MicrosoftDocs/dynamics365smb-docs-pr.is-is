---
title: "Hvernig á að: Notaðu tilföng fyrir verk | Microsoft Docs"
description: "Lýsir því hvernig á að nota vinnuskýrslur til að stjórna verkefnum."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project management, capacity, staff
ms.date: 03/28/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 34d8b133a11324e1821780e3988158bb0989349b
ms.contentlocale: is-is
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-use-resources-for-jobs"></a>Hvernig á að: Nota forða fyrir verk
Notkun forða er skráð í verkbókina til að fylgjast með kostnaði, verði og þeim verktegundum sem tengdar eru við verk. Nánari upplýsingar eru í [Hvernig á að: Skrá notkun vegna verka](projects-how-record-job-usage.md).

Einnig er hægt að bóka notkun forða í forðabók. Færslur sem bókaðar eru í forðabók hafa engin áhrif á fjárhag.

**Athugið**: Þessi virkni krefst að upplifun þín er stilltur á **Pakki**. Nánari upplýsingar, sjá [Sérstilli þína [!INCLUDE[d365fin](includes/d365fin_md.md)]upplifun](ui-experiences.md).

## <a name="to-assign-resources-to-jobs"></a>Forða úthlutað á verk
Forða er úthlutað á verk með því að búa til verkáætlunarlínur fyrir verkið. Nánari upplýsingar eru í [Hvernig á að: Stofna verk](projects-how-create-jobs.md).

## <a name="to-record-resource-usage-for-a-job"></a>Til að skrá notkun forða fyrir verk
1. Efst í hægra horni skal velja **Leita að síðu eða skýrslu** táknið ![Leita að síðu eða skýrslu](media/ui-search/search_small.png "Leita að síðu eða skýrslu táknið"), færa **Verk - færslubækur**, og velja síðan viðeigandi tengil.
2. Opnið viðeigandi verkbókarfærslu og fyllið út reitina eins og þörf krefur. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Þegar færslubókin er tilbúin skal velja aðgerðina **Bóka**.

## <a name="to-adjust-resource-prices"></a>Til að leiðrétta forðaverð
Ef breyta á kostnaði eða verði á mörgum tegundum forða er hægt að nota keyrslu.  

1. Efst í hægra horni skal velja **Leita að síðu eða skýrslu** táknið ![Leita að síðu eða skýrslu](media/ui-search/search_small.png "Leita að síðu eða skýrslu táknið"), færa **Leiðr. forðakostnað/verð**, og velja síðan viðeigandi tengil.
2. Fyllið út reitina í línu eins og þörf krefur og veljið svo hnappinn **Í lagi**.

**Til athugunar**: Þessi keyrsla stofnar hvorki né leiðréttir annan kostnað eða verð forða. Hún breytir aðeins innihaldi reitsins á forðaspjaldinu fyrir reitinn **Leiðr. reit** sem var valinn í keyrslunni. Leiðréttingarnar taka strax gildi í forðanum svo að rétt er að ganga úr skugga um að leiðréttingarstuðullinn sé réttur áður en keyrslan er notuð.

## <a name="to-get-resource-price-change-suggestions-based-on-existing-alternate-prices"></a>Til að fá verðbreytingatillögur forða út frá fyrirliggjandi öðru verði
Ef þegar er búið að setja upp annað verð fyrir hluta af forðanum er hægt að nota keyrslu til að setja upp fleiri önnur forðaverð.

1. Efst í hægra horni skal velja **Leita að síðu eða skýrslu** táknið ![Leita að síðu eða skýrslu](media/ui-search/search_small.png "Leita að síðu eða skýrslu táknið"), færa **Verðbreytingar forða**, og velja síðan viðeigandi tengil.
2. Veljið aðgerðina **Tillaga forðaverðbr. (verð)** og fyllið svo út reitina eins og þörf krefur.
3. Velja hnappinn **Í lagi**.  
4. Þegar keyrslunni lýkur má sjá niðurstöður keyrslunnar í glugganum **Verðbreytingar forða**.

## <a name="to-get-resource-price-change-suggestions-based-on-standard-prices"></a>Búa til verðbreytingatillögur forða út frá stöðluðu verði:
Ef setja á upp fleiri en eitt annað verð á forða út frá stöðluðu verði á forðaspjöldunum er hægt að nota keyrslu.  

1. Efst í hægra horni skal velja **Leita að síðu eða skýrslu** táknið ![Leita að síðu eða skýrslu](media/ui-search/search_small.png "Leita að síðu eða skýrslu táknið"), færa **Verðbreytingar forða**, og velja síðan viðeigandi tengil.
2. Veljið aðgerðina **Tillaga forðaverðbr. (forði)** og fyllið svo út reitina eins og þörf krefur.  
3. Velja hnappinn **Í lagi**.  
4. Þegar keyrslunni lýkur er glugginn **Verðbreytingar forða** opnaður til að sjá niðurstöður keyrslunnar.

## <a name="to-get-resource-price-change-suggestions-based-on-alternate-prices"></a>Til að fá verðbreytingatillögur forða út frá öðru verði
Ef þegar er búið að setja upp annað verð fyrir hluta af forðanum er hægt að nota keyrslu til að setja upp fleiri önnur forðaverð.

1. Í reitnum **Leit** skal færa inn **Tillaga forðaverðbr. (verð)** og velja síðan viðkomandi tengil.  
2. Fyllið inn í svæðin eftir þörfum.
3. Velja hnappinn **Í lagi**.  
4. Þegar keyrslunni lýkur er glugginn **Verðbreytingar forða** opnaður til að sjá niðurstöður keyrslunnar.

## <a name="see-also"></a>Sjá einnig
[Verkefnastjórnun](projects-manage-projects.md)  
[Fjármál](finance.md)  
[Innkaup](purchasing-manage-purchasing.md)         
[Sala](sales-manage-sales.md)     
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

