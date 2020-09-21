---
title: Skrá og leiðrétta forðanotkun og verð| Microsoft Docs
description: Lýsir því hvernig þú getur skráð forðanotkunina eða neysluna í tengslum við verk, til að fylgjast með og stjórna kostnaði, verði, og vinnutegund.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project management, capacity, staff
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: ac15e8f84efba5a46e3d5fc3d0d07f9dceed666a
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/09/2020
ms.locfileid: "3778840"
---
# <a name="use-resources-for-jobs"></a>Nota tilföng fyrir verk
Notkun forða er skráð í verkbókina til að fylgjast með kostnaði, verði og þeim verktegundum sem tengdar eru við verk. Frekari upplýsingar eru í [Skrá notkun fyrir verk](projects-how-record-job-usage.md).

> [!NOTE]
> Einnig er hægt að kaupa ytri forða, t.d. til að senda reikning á lánardrottin fyrir afhenta vinnu. Nánari upplýsingar eru í reitnum [Skrá innkaup](purchasing-how-record-purchases.md).

Einnig er hægt að bóka notkun forða í forðabók. Færslur sem bókaðar eru í forðabók hafa engin áhrif á fjárhag.

## <a name="to-assign-resources-to-jobs"></a>Forða úthlutað á verk
Forða er úthlutað á verk með því að búa til verkáætlunarlínur fyrir verkið. Frekari upplýsingar eru í [Stofna verk](projects-how-create-jobs.md).

## <a name="to-record-resource-usage-for-a-job"></a>Til að skrá notkun forða fyrir verk
1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Verkbækur** og veldu síðan tengda tengilinn.
2. Opnið viðeigandi verkbókarfærslu og fyllið út reitina eins og þörf krefur. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Þegar færslubókin er tilbúin skal velja aðgerðina **Bóka**.

## <a name="to-adjust-resource-prices"></a>Til að leiðrétta forðaverð
Ef breyta á kostnaði eða verði á mörgum tegundum forða er hægt að nota keyrslu.  

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Leiðrétta forðakostnað/verð** og veldu síðan tengda tengilinn.
2. Fyllið út reitina í línu eins og þörf krefur og veljið svo hnappinn **Í lagi**.

> [!NOTE]  
>   Þessi keyrsla stofnar hvorki né leiðréttir annan kostnað eða verð forða. Hún breytir aðeins innihaldi reitsins á forðaspjaldinu fyrir reitinn **Leiðr. reit** sem var valinn í keyrslunni. Leiðréttingarnar taka strax gildi í forðanum svo að rétt er að ganga úr skugga um að leiðréttingarstuðullinn sé réttur áður en keyrslan er notuð.

## <a name="to-get-resource-price-change-suggestions-based-on-existing-alternate-prices"></a>Til að fá verðbreytingatillögur forða út frá fyrirliggjandi öðru verði
Ef þegar er búið að setja upp annað verð fyrir hluta af forðanum er hægt að nota keyrslu til að setja upp fleiri önnur forðaverð.

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Verðbreytingar forða** og veldu síðan tengda tengilinn.
2. Veljið aðgerðina **Tillaga forðaverðbr. (verð)** og fyllið svo út reitina eins og þörf krefur.
3. Velja hnappinn **Í lagi**.  
4. Þegar runuvinnslunni lýkur sýnir síðan **Verðbreytingar forða** niðurstöður runuvinnslunnar.

## <a name="to-get-resource-price-change-suggestions-based-on-standard-prices"></a>Búa til verðbreytingatillögur forða út frá stöðluðu verði:
Ef setja á upp fleiri en eitt annað verð á forða út frá stöðluðu verði á forðaspjöldunum er hægt að nota keyrslu.  

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Verðbreytingar forða** og veldu síðan tengda tengilinn.
2. Veljið aðgerðina **Tillaga forðaverðbr. (forði)** og fyllið svo út reitina eins og þörf krefur.  
3. Velja hnappinn **Í lagi**.  
4. Þegar runuvinnslunni lýkur er síðan **Verðbreytingar forða** opnuð til að sjá niðurstöður runuvinnslunnar.

## <a name="to-get-resource-price-change-suggestions-based-on-alternate-prices"></a>Til að fá verðbreytingatillögur forða út frá öðru verði
Ef þegar er búið að setja upp annað verð fyrir hluta af forðanum er hægt að nota keyrslu til að setja upp fleiri önnur forðaverð.

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Tillögur um verðbreytingar forða** og veldu síðan tengda tengilinn.  
2. Fyllið inn í svæðin eftir þörfum.
3. Velja hnappinn **Í lagi**.  
4. Þegar runuvinnslunni lýkur er síðan **Verðbreytingar forða** opnuð til að sjá niðurstöður runuvinnslunnar.

## <a name="see-also"></a>Sjá einnig
[Verkefnastjórnun](projects-manage-projects.md)  
[Fjármál](finance.md)  
[Innkaup](purchasing-manage-purchasing.md)         
[Sala](sales-manage-sales.md)     
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
