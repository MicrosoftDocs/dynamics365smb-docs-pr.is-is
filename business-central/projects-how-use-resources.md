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
# <a name="use-resources-for-jobs"></a><span data-ttu-id="1b5df-103">Nota tilföng fyrir verk</span><span class="sxs-lookup"><span data-stu-id="1b5df-103">Use Resources for Jobs</span></span>
<span data-ttu-id="1b5df-104">Notkun forða er skráð í verkbókina til að fylgjast með kostnaði, verði og þeim verktegundum sem tengdar eru við verk.</span><span class="sxs-lookup"><span data-stu-id="1b5df-104">You record the usage of resources in the job journal to keep track of costs, prices, and the work types that are linked to jobs.</span></span> <span data-ttu-id="1b5df-105">Frekari upplýsingar eru í [Skrá notkun fyrir verk](projects-how-record-job-usage.md).</span><span class="sxs-lookup"><span data-stu-id="1b5df-105">For more information, see [Record Usage for Jobs](projects-how-record-job-usage.md).</span></span>

> [!NOTE]
> <span data-ttu-id="1b5df-106">Einnig er hægt að kaupa ytri forða, t.d. til að senda reikning á lánardrottin fyrir afhenta vinnu.</span><span class="sxs-lookup"><span data-stu-id="1b5df-106">You can also purchase external resources, for example, to invoice a vendor for work delivered.</span></span> <span data-ttu-id="1b5df-107">Nánari upplýsingar eru í reitnum [Skrá innkaup](purchasing-how-record-purchases.md).</span><span class="sxs-lookup"><span data-stu-id="1b5df-107">For more information, see [Record Purchases](purchasing-how-record-purchases.md).</span></span>

<span data-ttu-id="1b5df-108">Einnig er hægt að bóka notkun forða í forðabók.</span><span class="sxs-lookup"><span data-stu-id="1b5df-108">You can also post the usage of a resource in a resource journal.</span></span> <span data-ttu-id="1b5df-109">Færslur sem bókaðar eru í forðabók hafa engin áhrif á fjárhag.</span><span class="sxs-lookup"><span data-stu-id="1b5df-109">Entries posted in a resource journal have no effect on the general ledger.</span></span>

## <a name="to-assign-resources-to-jobs"></a><span data-ttu-id="1b5df-110">Forða úthlutað á verk</span><span class="sxs-lookup"><span data-stu-id="1b5df-110">To assign resources to jobs</span></span>
<span data-ttu-id="1b5df-111">Forða er úthlutað á verk með því að búa til verkáætlunarlínur fyrir verkið.</span><span class="sxs-lookup"><span data-stu-id="1b5df-111">You assign resources to jobs by creating job planning lines for the job.</span></span> <span data-ttu-id="1b5df-112">Frekari upplýsingar eru í [Stofna verk](projects-how-create-jobs.md).</span><span class="sxs-lookup"><span data-stu-id="1b5df-112">For more information, see [Create Jobs](projects-how-create-jobs.md).</span></span>

## <a name="to-record-resource-usage-for-a-job"></a><span data-ttu-id="1b5df-113">Til að skrá notkun forða fyrir verk</span><span class="sxs-lookup"><span data-stu-id="1b5df-113">To record resource usage for a job</span></span>
1. <span data-ttu-id="1b5df-114">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Verkbækur** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="1b5df-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Job Journals**, and then choose the related link.</span></span>
2. <span data-ttu-id="1b5df-115">Opnið viðeigandi verkbókarfærslu og fyllið út reitina eins og þörf krefur.</span><span class="sxs-lookup"><span data-stu-id="1b5df-115">Open a relevant job journal batch, and then fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="1b5df-116">Þegar færslubókin er tilbúin skal velja aðgerðina **Bóka**.</span><span class="sxs-lookup"><span data-stu-id="1b5df-116">When the journal is complete, choose the **Post** action.</span></span>

## <a name="to-adjust-resource-prices"></a><span data-ttu-id="1b5df-117">Til að leiðrétta forðaverð</span><span class="sxs-lookup"><span data-stu-id="1b5df-117">To adjust resource prices</span></span>
<span data-ttu-id="1b5df-118">Ef breyta á kostnaði eða verði á mörgum tegundum forða er hægt að nota keyrslu.</span><span class="sxs-lookup"><span data-stu-id="1b5df-118">If you want to change costs or prices for a large number of resources, you can use a batch job.</span></span>  

1. <span data-ttu-id="1b5df-119">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Leiðrétta forðakostnað/verð** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="1b5df-119">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Adjust Resource Costs/Prices**, and then choose the related link.</span></span>
2. <span data-ttu-id="1b5df-120">Fyllið út reitina í línu eins og þörf krefur og veljið svo hnappinn **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="1b5df-120">Fill in the fields on a line as necessary, and then choose the **OK** button.</span></span>

> [!NOTE]  
>   <span data-ttu-id="1b5df-121">Þessi keyrsla stofnar hvorki né leiðréttir annan kostnað eða verð forða.</span><span class="sxs-lookup"><span data-stu-id="1b5df-121">This batch job does not create or adjust alternate costs or prices for resources.</span></span> <span data-ttu-id="1b5df-122">Hún breytir aðeins innihaldi reitsins á forðaspjaldinu fyrir reitinn **Leiðr. reit** sem var valinn í keyrslunni.</span><span class="sxs-lookup"><span data-stu-id="1b5df-122">It only changes the contents of the field on the resource card for the **Adjust Field** field that you selected in the batch job.</span></span> <span data-ttu-id="1b5df-123">Leiðréttingarnar taka strax gildi í forðanum svo að rétt er að ganga úr skugga um að leiðréttingarstuðullinn sé réttur áður en keyrslan er notuð.</span><span class="sxs-lookup"><span data-stu-id="1b5df-123">The adjustment will take effect immediately for resources, so check your adjustment factors before you run the batch job.</span></span>

## <a name="to-get-resource-price-change-suggestions-based-on-existing-alternate-prices"></a><span data-ttu-id="1b5df-124">Til að fá verðbreytingatillögur forða út frá fyrirliggjandi öðru verði</span><span class="sxs-lookup"><span data-stu-id="1b5df-124">To get resource price change suggestions based on existing alternate prices</span></span>
<span data-ttu-id="1b5df-125">Ef þegar er búið að setja upp annað verð fyrir hluta af forðanum er hægt að nota keyrslu til að setja upp fleiri önnur forðaverð.</span><span class="sxs-lookup"><span data-stu-id="1b5df-125">If you have already set up alternate resource price for some resources, you can use a batch job to set up multiple alternate resource prices.</span></span>

1. <span data-ttu-id="1b5df-126">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Verðbreytingar forða** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="1b5df-126">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Resource Price Changes**, and then choose the related link.</span></span>
2. <span data-ttu-id="1b5df-127">Veljið aðgerðina **Tillaga forðaverðbr. (verð)** og fyllið svo út reitina eins og þörf krefur.</span><span class="sxs-lookup"><span data-stu-id="1b5df-127">Choose the **Suggest Res. Price Chg. (Price)** action, and then fill in the fields as necessary.</span></span>
3. <span data-ttu-id="1b5df-128">Velja hnappinn **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="1b5df-128">Choose the **OK** button.</span></span>  
4. <span data-ttu-id="1b5df-129">Þegar runuvinnslunni lýkur sýnir síðan **Verðbreytingar forða** niðurstöður runuvinnslunnar.</span><span class="sxs-lookup"><span data-stu-id="1b5df-129">When the batch job is finished, the **Resource Price Changes** page shows the results of the batch job.</span></span>

## <a name="to-get-resource-price-change-suggestions-based-on-standard-prices"></a><span data-ttu-id="1b5df-130">Búa til verðbreytingatillögur forða út frá stöðluðu verði:</span><span class="sxs-lookup"><span data-stu-id="1b5df-130">To get resource price change suggestions based on standard prices</span></span>
<span data-ttu-id="1b5df-131">Ef setja á upp fleiri en eitt annað verð á forða út frá stöðluðu verði á forðaspjöldunum er hægt að nota keyrslu.</span><span class="sxs-lookup"><span data-stu-id="1b5df-131">If you want to set up multiple alternate resource prices based on the standard prices on the resource cards, you can use a batch job.</span></span>  

1. <span data-ttu-id="1b5df-132">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Verðbreytingar forða** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="1b5df-132">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Resource Price Changes**, and then choose the related link.</span></span>
2. <span data-ttu-id="1b5df-133">Veljið aðgerðina **Tillaga forðaverðbr. (forði)** og fyllið svo út reitina eins og þörf krefur.</span><span class="sxs-lookup"><span data-stu-id="1b5df-133">Choose the **Suggest Res. Price Chg. (Res.)** action, and then fill in the fields as necessary.</span></span>  
3. <span data-ttu-id="1b5df-134">Velja hnappinn **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="1b5df-134">Choose the **OK** button.</span></span>  
4. <span data-ttu-id="1b5df-135">Þegar runuvinnslunni lýkur er síðan **Verðbreytingar forða** opnuð til að sjá niðurstöður runuvinnslunnar.</span><span class="sxs-lookup"><span data-stu-id="1b5df-135">When the batch job is finished, open the **Resource Price Changes** page to see the results of the batch job.</span></span>

## <a name="to-get-resource-price-change-suggestions-based-on-alternate-prices"></a><span data-ttu-id="1b5df-136">Til að fá verðbreytingatillögur forða út frá öðru verði</span><span class="sxs-lookup"><span data-stu-id="1b5df-136">To get resource price change suggestions based on alternate prices</span></span>
<span data-ttu-id="1b5df-137">Ef þegar er búið að setja upp annað verð fyrir hluta af forðanum er hægt að nota keyrslu til að setja upp fleiri önnur forðaverð.</span><span class="sxs-lookup"><span data-stu-id="1b5df-137">If you have already set up alternate resource price for some resources, you can use a batch job to set up multiple alternate resource prices.</span></span>

1. <span data-ttu-id="1b5df-138">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Tillögur um verðbreytingar forða** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="1b5df-138">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Suggest Res. Price Chg. (Price)**, and then choose the related link.</span></span>  
2. <span data-ttu-id="1b5df-139">Fyllið inn í svæðin eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="1b5df-139">Fill in the fields as necessary.</span></span>
3. <span data-ttu-id="1b5df-140">Velja hnappinn **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="1b5df-140">Choose the **OK** button.</span></span>  
4. <span data-ttu-id="1b5df-141">Þegar runuvinnslunni lýkur er síðan **Verðbreytingar forða** opnuð til að sjá niðurstöður runuvinnslunnar.</span><span class="sxs-lookup"><span data-stu-id="1b5df-141">When the batch job is finished, open the **Resource Price Changes** page to see the results of the batch job.</span></span>

## <a name="see-also"></a><span data-ttu-id="1b5df-142">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="1b5df-142">See Also</span></span>
[<span data-ttu-id="1b5df-143">Verkefnastjórnun</span><span class="sxs-lookup"><span data-stu-id="1b5df-143">Project Management</span></span>](projects-manage-projects.md)  
[<span data-ttu-id="1b5df-144">Fjármál</span><span class="sxs-lookup"><span data-stu-id="1b5df-144">Finance</span></span>](finance.md)  
<span data-ttu-id="1b5df-145">[Innkaup](purchasing-manage-purchasing.md)       </span><span class="sxs-lookup"><span data-stu-id="1b5df-145">[Purchasing](purchasing-manage-purchasing.md)       </span></span>  
<span data-ttu-id="1b5df-146">[Sala](sales-manage-sales.md)   </span><span class="sxs-lookup"><span data-stu-id="1b5df-146">[Sales](sales-manage-sales.md)   </span></span>  
<span data-ttu-id="1b5df-147">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="1b5df-147">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
