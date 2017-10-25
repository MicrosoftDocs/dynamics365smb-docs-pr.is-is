---
title: "Skrá og leiðrétta forðanotkun og verð| Microsoft Docs"
description: "Lýsir því hvernig þú getur skráð forðanotkunina eða neysluna í tengslum við verk, til að fylgjast með og stjórna kostnaði, verði, og vinnutegund."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project management, capacity, staff
ms.date: 06/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: eea34afbee429d14ab150894729cb4ea3843bb2b
ms.openlocfilehash: f110f4cc342f5284e3da2641d56dc13f67c3773a
ms.contentlocale: is-is
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-use-resources-for-jobs"></a><span data-ttu-id="e579a-103">Hvernig á að: Nota forða fyrir verk</span><span class="sxs-lookup"><span data-stu-id="e579a-103">How to: Use Resources for Jobs</span></span>
<span data-ttu-id="e579a-104">Notkun forða er skráð í verkbókina til að fylgjast með kostnaði, verði og þeim verktegundum sem tengdar eru við verk.</span><span class="sxs-lookup"><span data-stu-id="e579a-104">You record the usage of resources in the job journal to keep track of costs, prices, and the work types that are linked to jobs.</span></span> <span data-ttu-id="e579a-105">Nánari upplýsingar eru í [Hvernig á að: Skrá notkun vegna verka](projects-how-record-job-usage.md).</span><span class="sxs-lookup"><span data-stu-id="e579a-105">For more information, see [How to: Record Usage for Jobs](projects-how-record-job-usage.md).</span></span>

<span data-ttu-id="e579a-106">Einnig er hægt að bóka notkun forða í forðabók.</span><span class="sxs-lookup"><span data-stu-id="e579a-106">You can also post the usage of a resource in a resource journal.</span></span> <span data-ttu-id="e579a-107">Færslur sem bókaðar eru í forðabók hafa engin áhrif á fjárhag.</span><span class="sxs-lookup"><span data-stu-id="e579a-107">Entries posted in a resource journal have no effect on the general ledger.</span></span>

> [!NOTE]  
>   <span data-ttu-id="e579a-108">Þessi virkni krefst þess að upplifun þín sé stillt á **Suite**.</span><span class="sxs-lookup"><span data-stu-id="e579a-108">This functionality requires that your experience is set to **Suite**.</span></span> <span data-ttu-id="e579a-109">Nánari upplýsingar, sjá [Sérstilla þína [!INCLUDE[d365fin](includes/d365fin_md.md)] upplifun](ui-experiences.md).</span><span class="sxs-lookup"><span data-stu-id="e579a-109">For more information, see [Customizing Your [!INCLUDE[d365fin](includes/d365fin_md.md)] Experience](ui-experiences.md).</span></span>

## <a name="to-assign-resources-to-jobs"></a><span data-ttu-id="e579a-110">Forða úthlutað á verk</span><span class="sxs-lookup"><span data-stu-id="e579a-110">To assign resources to jobs</span></span>
<span data-ttu-id="e579a-111">Forða er úthlutað á verk með því að búa til verkáætlunarlínur fyrir verkið.</span><span class="sxs-lookup"><span data-stu-id="e579a-111">You assign resources to jobs by creating job planning lines for the job.</span></span> <span data-ttu-id="e579a-112">Nánari upplýsingar eru í [Hvernig á að: Stofna verk](projects-how-create-jobs.md).</span><span class="sxs-lookup"><span data-stu-id="e579a-112">For more information, see [How to: Create Jobs](projects-how-create-jobs.md).</span></span>

## <a name="to-record-resource-usage-for-a-job"></a><span data-ttu-id="e579a-113">Til að skrá notkun forða fyrir verk</span><span class="sxs-lookup"><span data-stu-id="e579a-113">To record resource usage for a job</span></span>
1. <span data-ttu-id="e579a-114">Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Verkbækur** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="e579a-114">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Job Journals**, and then choose the related link.</span></span>
2. <span data-ttu-id="e579a-115">Opnið viðeigandi verkbókarfærslu og fyllið út reitina eins og þörf krefur.</span><span class="sxs-lookup"><span data-stu-id="e579a-115">Open a relevant job journal batch, and then fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="e579a-116">Þegar færslubókin er tilbúin skal velja aðgerðina **Bóka**.</span><span class="sxs-lookup"><span data-stu-id="e579a-116">When the journal is complete, choose the **Post** action.</span></span>

## <a name="to-adjust-resource-prices"></a><span data-ttu-id="e579a-117">Til að leiðrétta forðaverð</span><span class="sxs-lookup"><span data-stu-id="e579a-117">To adjust resource prices</span></span>
<span data-ttu-id="e579a-118">Ef breyta á kostnaði eða verði á mörgum tegundum forða er hægt að nota keyrslu.</span><span class="sxs-lookup"><span data-stu-id="e579a-118">If you want to change costs or prices for a large number of resources, you can use a batch job.</span></span>  

1. <span data-ttu-id="e579a-119">Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Leiðrétta forðakostnað/verð** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="e579a-119">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Adjust Resource Costs/Prices**, and then choose the related link.</span></span>
2. <span data-ttu-id="e579a-120">Fyllið út reitina í línu eins og þörf krefur og veljið svo hnappinn **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="e579a-120">Fill in the fields on a line as necessary, and then choose the **OK** button.</span></span>

> [!NOTE]  
>   <span data-ttu-id="e579a-121">Þessi keyrsla stofnar hvorki né leiðréttir annan kostnað eða verð forða.</span><span class="sxs-lookup"><span data-stu-id="e579a-121">This batch job does not create or adjust alternate costs or prices for resources.</span></span> <span data-ttu-id="e579a-122">Hún breytir aðeins innihaldi reitsins á forðaspjaldinu fyrir reitinn **Leiðr. reit** sem var valinn í keyrslunni.</span><span class="sxs-lookup"><span data-stu-id="e579a-122">It only changes the contents of the field on the resource card for the **Adjust Field** field that you selected in the batch job.</span></span> <span data-ttu-id="e579a-123">Leiðréttingarnar taka strax gildi í forðanum svo að rétt er að ganga úr skugga um að leiðréttingarstuðullinn sé réttur áður en keyrslan er notuð.</span><span class="sxs-lookup"><span data-stu-id="e579a-123">The adjustment will take effect immediately for resources, so check your adjustment factors before you run the batch job.</span></span>

## <a name="to-get-resource-price-change-suggestions-based-on-existing-alternate-prices"></a><span data-ttu-id="e579a-124">Til að fá verðbreytingatillögur forða út frá fyrirliggjandi öðru verði</span><span class="sxs-lookup"><span data-stu-id="e579a-124">To get resource price change suggestions based on existing alternate prices</span></span>
<span data-ttu-id="e579a-125">Ef þegar er búið að setja upp annað verð fyrir hluta af forðanum er hægt að nota keyrslu til að setja upp fleiri önnur forðaverð.</span><span class="sxs-lookup"><span data-stu-id="e579a-125">If you have already set up alternate resource price for some resources, you can use a batch job to set up multiple alternate resource prices.</span></span>

1. <span data-ttu-id="e579a-126">Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Breytingar á forðaverði** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="e579a-126">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Resource Price Changes**, and then choose the related link.</span></span>
2. <span data-ttu-id="e579a-127">Veljið aðgerðina **Tillaga forðaverðbr. (verð)** og fyllið svo út reitina eins og þörf krefur.</span><span class="sxs-lookup"><span data-stu-id="e579a-127">Choose the **Suggest Res. Price Chg. (Price)** action, and then fill in the fields as necessary.</span></span>
3. <span data-ttu-id="e579a-128">Velja hnappinn **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="e579a-128">Choose the **OK** button.</span></span>  
4. <span data-ttu-id="e579a-129">Þegar keyrslunni lýkur má sjá niðurstöður keyrslunnar í glugganum **Verðbreytingar forða**.</span><span class="sxs-lookup"><span data-stu-id="e579a-129">When the batch job is finished, the **Resource Price Changes** window shows the results of the batch job.</span></span>

## <a name="to-get-resource-price-change-suggestions-based-on-standard-prices"></a><span data-ttu-id="e579a-130">Búa til verðbreytingatillögur forða út frá stöðluðu verði:</span><span class="sxs-lookup"><span data-stu-id="e579a-130">To get resource price change suggestions based on standard prices</span></span>
<span data-ttu-id="e579a-131">Ef setja á upp fleiri en eitt annað verð á forða út frá stöðluðu verði á forðaspjöldunum er hægt að nota keyrslu.</span><span class="sxs-lookup"><span data-stu-id="e579a-131">If you want to set up multiple alternate resource prices based on the standard prices on the resource cards, you can use a batch job.</span></span>  

1. <span data-ttu-id="e579a-132">Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Breytingar á forðaverði** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="e579a-132">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Resource Price Changes**, and then choose the related link.</span></span>
2. <span data-ttu-id="e579a-133">Veljið aðgerðina **Tillaga forðaverðbr. (forði)** og fyllið svo út reitina eins og þörf krefur.</span><span class="sxs-lookup"><span data-stu-id="e579a-133">Choose the **Suggest Res. Price Chg. (Res.)** action, and then fill in the fields as necessary.</span></span>  
3. <span data-ttu-id="e579a-134">Velja hnappinn **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="e579a-134">Choose the **OK** button.</span></span>  
4. <span data-ttu-id="e579a-135">Þegar keyrslunni lýkur er glugginn **Verðbreytingar forða** opnaður til að sjá niðurstöður keyrslunnar.</span><span class="sxs-lookup"><span data-stu-id="e579a-135">When the batch job is finished, open the **Resource Price Changes** window to see the results of the batch job.</span></span>

## <a name="to-get-resource-price-change-suggestions-based-on-alternate-prices"></a><span data-ttu-id="e579a-136">Til að fá verðbreytingatillögur forða út frá öðru verði</span><span class="sxs-lookup"><span data-stu-id="e579a-136">To get resource price change suggestions based on alternate prices</span></span>
<span data-ttu-id="e579a-137">Ef þegar er búið að setja upp annað verð fyrir hluta af forðanum er hægt að nota keyrslu til að setja upp fleiri önnur forðaverð.</span><span class="sxs-lookup"><span data-stu-id="e579a-137">If you have already set up alternate resource price for some resources, you can use a batch job to set up multiple alternate resource prices.</span></span>

1. <span data-ttu-id="e579a-138">Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Tillaga forðaverðbr. (Verð)** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="e579a-138">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Suggest Res. Price Chg. (Price)**, and then choose the related link.</span></span>  
2. <span data-ttu-id="e579a-139">Fyllið inn í svæðin eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="e579a-139">Fill in the fields as necessary.</span></span>
3. <span data-ttu-id="e579a-140">Velja hnappinn **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="e579a-140">Choose the **OK** button.</span></span>  
4. <span data-ttu-id="e579a-141">Þegar keyrslunni lýkur er glugginn **Verðbreytingar forða** opnaður til að sjá niðurstöður keyrslunnar.</span><span class="sxs-lookup"><span data-stu-id="e579a-141">When the batch job is finished, open the **Resource Price Changes** window to see the results of the batch job.</span></span>

## <a name="see-also"></a><span data-ttu-id="e579a-142">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="e579a-142">See Also</span></span>
[<span data-ttu-id="e579a-143">Verkefnastjórnun</span><span class="sxs-lookup"><span data-stu-id="e579a-143">Project Management</span></span>](projects-manage-projects.md)  
[<span data-ttu-id="e579a-144">Fjármál</span><span class="sxs-lookup"><span data-stu-id="e579a-144">Finance</span></span>](finance.md)  
<span data-ttu-id="e579a-145">[Innkaup](purchasing-manage-purchasing.md)       </span><span class="sxs-lookup"><span data-stu-id="e579a-145">[Purchasing](purchasing-manage-purchasing.md)       </span></span>  
<span data-ttu-id="e579a-146">[Sala](sales-manage-sales.md)   </span><span class="sxs-lookup"><span data-stu-id="e579a-146">[Sales](sales-manage-sales.md)   </span></span>  
<span data-ttu-id="e579a-147">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="e579a-147">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

