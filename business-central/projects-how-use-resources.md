---
title: Skrá og leiðrétta forðanotkun og verð
description: 'Lýsir því hvernig hægt er að skrá forðanotkun eða notkun sem tengist verkefni, fylgjast með og stýra kostnaði, verði og tegundum vinnu.'
author: brentholtorf
ms.topic: how-to
ms.search.keywords: 'project management, capacity, staff'
ms.search.form: '201,206, 207, 271, 493'
ms.date: 02/22/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.custom: bap-template
ms.reviewer: bholtorf
---
# <a name="use-resources-for-projects"></a>Nota forða fyrir verkefni

Notkun forða er skráð í verkbókina til að fylgjast með kostnaði, verði og þeim tegundum vinnu sem tengjast verkefnum. Nánari upplýsingar eru í [Skrá notkun vegna verkefna](projects-how-record-job-usage.md).

> [!NOTE]
> Einnig er hægt að kaupa ytri forða, t.d. til að senda reikning á lánardrottin fyrir afhenta vinnu. Nánari upplýsingar eru í reitnum [Skrá innkaup](purchasing-how-record-purchases.md).

Einnig er hægt að bóka notkun forða í forðabók. Færslur sem bókaðar eru í forðabók hafa engin áhrif á fjárhag.

## <a name="to-assign-resources-to-projects"></a>Forða úthlutað til verkefna

Forða er úthlutað til verkefna með því að stofna verkáætlunarlínur fyrir verkið. Nánari upplýsingar eru í [Stofna verkefni](projects-how-create-jobs.md).

## <a name="to-record-resource-usage-for-a-project"></a>Til að skrá forðanotkun fyrir verk

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, færa inn **verkbækur** og velja síðan viðeigandi tengil.
2. Viðeigandi verkbókarkeyrsla er opnuð og reitirnir fylltir út eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Þegar færslubókin er tilbúin skal velja aðgerðina **Bóka**.

    [!INCLUDE [preview-posting-inventory](includes/preview-posting-inventory.md)]

## <a name="to-adjust-resource-prices"></a>Til að leiðrétta forðaverð

Ef breyta á kostnaði eða verði á mörgum tegundum forða er hægt að nota keyrslu.  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Leiðrétta kostnað/verð tilfangs** og veldu síðan tengda tengilinn.
2. Fyllið út reitina í línu eins og þörf krefur og veljið svo hnappinn **Í lagi**.

> [!NOTE]  
> Þessi keyrsla stofnar hvorki né leiðréttir annan kostnað eða verð forða. Hún breytir aðeins innihaldi reitsins á forðaspjaldinu fyrir reitinn **Leiðr. reit** sem var valinn í keyrslunni. Leiðréttingarnar taka strax gildi í forðanum svo að rétt er að ganga úr skugga um að leiðréttingarstuðullinn sé réttur áður en keyrslan er notuð.

## <a name="to-get-resource-price-change-suggestions-based-on-existing-alternate-prices"></a>Til að fá verðbreytingatillögur forða út frá fyrirliggjandi öðru verði

Ef þegar er búið að setja upp annað verð fyrir hluta af forðanum er hægt að nota keyrslu til að setja upp fleiri önnur forðaverð.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Verðbreytingar forða** og velja síðan viðkomandi tengil.
2. Veljið aðgerðina **Tillaga forðaverðbr. (verð)** og fyllið svo út reitina eins og þörf krefur.
3. Velja hnappinn **Í lagi**.  
4. Þegar runuvinnslunni lýkur sýnir síðan **Verðbreytingar forða** niðurstöður runuvinnslunnar.

## <a name="to-get-resource-price-change-suggestions-based-on-standard-prices"></a>Búa til verðbreytingatillögur forða út frá stöðluðu verði:

Ef setja á upp fleiri en eitt annað verð á forða út frá stöðluðu verði á forðaspjöldunum er hægt að nota keyrslu.  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Verðbreytingar forða** og velja síðan viðkomandi tengil.
2. Veljið aðgerðina **Tillaga forðaverðbr. (forði)** og fyllið svo út reitina eins og þörf krefur.  
3. Velja hnappinn **Í lagi**.  
4. Þegar runuvinnslunni lýkur er síðan **Verðbreytingar forða** opnuð til að sjá niðurstöður runuvinnslunnar.

## <a name="to-get-resource-price-change-suggestions-based-on-alternate-prices"></a>Til að fá verðbreytingatillögur forða út frá öðru verði

Ef þegar er búið að setja upp annað verð fyrir hluta af forðanum er hægt að nota keyrslu til að setja upp fleiri önnur forðaverð.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Tillaga um verðbreytingu forða (verð)** og velja síðan viðkomandi tengil.  
2. Fyllið inn í svæðin eftir þörfum.
3. Velja hnappinn **Í lagi**.  
4. Þegar runuvinnslunni lýkur er síðan **Verðbreytingar forða** opnuð til að sjá niðurstöður runuvinnslunnar.

## <a name="see-also"></a>Sjá einnig

[Verkefnastjórnun](projects-manage-projects.md)  
[Fjármál](finance.md)  
[Innkaup](purchasing-manage-purchasing.md)         
[Sala](sales-manage-sales.md)     
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
