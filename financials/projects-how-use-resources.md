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
ms.date: 01/25/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: acef03f32124c5983846bc6ed0c4d332c9c8b347
ms.openlocfilehash: 5c6a83acd120d86d568a140f002189f9af180bb4
ms.contentlocale: is-is
ms.lasthandoff: 04/16/2018

---
# <a name="use-resources-for-jobs"></a><span data-ttu-id="060ae-103">Nota tilföng fyrir verk</span><span class="sxs-lookup"><span data-stu-id="060ae-103">Use Resources for Jobs</span></span>
<span data-ttu-id="060ae-104">Notkun forða er skráð í verkbókina til að fylgjast með kostnaði, verði og þeim verktegundum sem tengdar eru við verk.</span><span class="sxs-lookup"><span data-stu-id="060ae-104">You record the usage of resources in the job journal to keep track of costs, prices, and the work types that are linked to jobs.</span></span> <span data-ttu-id="060ae-105">Frekari upplýsingar eru í [Skrá notkun fyrir verk](projects-how-record-job-usage.md).</span><span class="sxs-lookup"><span data-stu-id="060ae-105">For more information, see [Record Usage for Jobs](projects-how-record-job-usage.md).</span></span>

<span data-ttu-id="060ae-106">Einnig er hægt að bóka notkun forða í forðabók.</span><span class="sxs-lookup"><span data-stu-id="060ae-106">You can also post the usage of a resource in a resource journal.</span></span> <span data-ttu-id="060ae-107">Færslur sem bókaðar eru í forðabók hafa engin áhrif á fjárhag.</span><span class="sxs-lookup"><span data-stu-id="060ae-107">Entries posted in a resource journal have no effect on the general ledger.</span></span>

## <a name="to-assign-resources-to-jobs"></a><span data-ttu-id="060ae-108">Forða úthlutað á verk</span><span class="sxs-lookup"><span data-stu-id="060ae-108">To assign resources to jobs</span></span>
<span data-ttu-id="060ae-109">Forða er úthlutað á verk með því að búa til verkáætlunarlínur fyrir verkið.</span><span class="sxs-lookup"><span data-stu-id="060ae-109">You assign resources to jobs by creating job planning lines for the job.</span></span> <span data-ttu-id="060ae-110">Frekari upplýsingar eru í [Stofna verk](projects-how-create-jobs.md).</span><span class="sxs-lookup"><span data-stu-id="060ae-110">For more information, see [Create Jobs](projects-how-create-jobs.md).</span></span>

## <a name="to-record-resource-usage-for-a-job"></a><span data-ttu-id="060ae-111">Til að skrá notkun forða fyrir verk</span><span class="sxs-lookup"><span data-stu-id="060ae-111">To record resource usage for a job</span></span>
1. <span data-ttu-id="060ae-112">Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Verkbækur** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="060ae-112">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Job Journals**, and then choose the related link.</span></span>
2. <span data-ttu-id="060ae-113">Opnið viðeigandi verkbókarfærslu og fyllið út reitina eins og þörf krefur.</span><span class="sxs-lookup"><span data-stu-id="060ae-113">Open a relevant job journal batch, and then fill in the fields as necessary.</span></span> [!INCLUDE [tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="060ae-114">Þegar færslubókin er tilbúin skal velja aðgerðina **Bóka**.</span><span class="sxs-lookup"><span data-stu-id="060ae-114">When the journal is complete, choose the **Post** action.</span></span>

## <a name="to-adjust-resource-prices"></a><span data-ttu-id="060ae-115">Til að leiðrétta forðaverð</span><span class="sxs-lookup"><span data-stu-id="060ae-115">To adjust resource prices</span></span>
<span data-ttu-id="060ae-116">Ef breyta á kostnaði eða verði á mörgum tegundum forða er hægt að nota keyrslu.</span><span class="sxs-lookup"><span data-stu-id="060ae-116">If you want to change costs or prices for a large number of resources, you can use a batch job.</span></span>  

1. <span data-ttu-id="060ae-117">Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Leiðrétta forðakostnað/verð** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="060ae-117">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Adjust Resource Costs/Prices**, and then choose the related link.</span></span>
2. <span data-ttu-id="060ae-118">Fyllið út reitina í línu eins og þörf krefur og veljið svo hnappinn **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="060ae-118">Fill in the fields on a line as necessary, and then choose the **OK** button.</span></span>

> [!NOTE]  
>   <span data-ttu-id="060ae-119">Þessi keyrsla stofnar hvorki né leiðréttir annan kostnað eða verð forða.</span><span class="sxs-lookup"><span data-stu-id="060ae-119">This batch job does not create or adjust alternate costs or prices for resources.</span></span> <span data-ttu-id="060ae-120">Hún breytir aðeins innihaldi reitsins á forðaspjaldinu fyrir reitinn **Leiðr. reit** sem var valinn í keyrslunni.</span><span class="sxs-lookup"><span data-stu-id="060ae-120">It only changes the contents of the field on the resource card for the **Adjust Field** field that you selected in the batch job.</span></span> <span data-ttu-id="060ae-121">Leiðréttingarnar taka strax gildi í forðanum svo að rétt er að ganga úr skugga um að leiðréttingarstuðullinn sé réttur áður en keyrslan er notuð.</span><span class="sxs-lookup"><span data-stu-id="060ae-121">The adjustment will take effect immediately for resources, so check your adjustment factors before you run the batch job.</span></span>

## <a name="to-get-resource-price-change-suggestions-based-on-existing-alternate-prices"></a><span data-ttu-id="060ae-122">Til að fá verðbreytingatillögur forða út frá fyrirliggjandi öðru verði</span><span class="sxs-lookup"><span data-stu-id="060ae-122">To get resource price change suggestions based on existing alternate prices</span></span>
<span data-ttu-id="060ae-123">Ef þegar er búið að setja upp annað verð fyrir hluta af forðanum er hægt að nota keyrslu til að setja upp fleiri önnur forðaverð.</span><span class="sxs-lookup"><span data-stu-id="060ae-123">If you have already set up alternate resource price for some resources, you can use a batch job to set up multiple alternate resource prices.</span></span>

1. <span data-ttu-id="060ae-124">Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Breytingar á forðaverði** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="060ae-124">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Resource Price Changes**, and then choose the related link.</span></span>
2. <span data-ttu-id="060ae-125">Veljið aðgerðina **Tillaga forðaverðbr. (verð)** og fyllið svo út reitina eins og þörf krefur.</span><span class="sxs-lookup"><span data-stu-id="060ae-125">Choose the **Suggest Res. Price Chg. (Price)** action, and then fill in the fields as necessary.</span></span>
3. <span data-ttu-id="060ae-126">Velja hnappinn **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="060ae-126">Choose the **OK** button.</span></span>  
4. <span data-ttu-id="060ae-127">Þegar keyrslunni lýkur má sjá niðurstöður keyrslunnar í glugganum **Verðbreytingar forða**.</span><span class="sxs-lookup"><span data-stu-id="060ae-127">When the batch job is finished, the **Resource Price Changes** window shows the results of the batch job.</span></span>

## <a name="to-get-resource-price-change-suggestions-based-on-standard-prices"></a><span data-ttu-id="060ae-128">Búa til verðbreytingatillögur forða út frá stöðluðu verði:</span><span class="sxs-lookup"><span data-stu-id="060ae-128">To get resource price change suggestions based on standard prices</span></span>
<span data-ttu-id="060ae-129">Ef setja á upp fleiri en eitt annað verð á forða út frá stöðluðu verði á forðaspjöldunum er hægt að nota keyrslu.</span><span class="sxs-lookup"><span data-stu-id="060ae-129">If you want to set up multiple alternate resource prices based on the standard prices on the resource cards, you can use a batch job.</span></span>  

1. <span data-ttu-id="060ae-130">Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Breytingar á forðaverði** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="060ae-130">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Resource Price Changes**, and then choose the related link.</span></span>
2. <span data-ttu-id="060ae-131">Veljið aðgerðina **Tillaga forðaverðbr. (forði)** og fyllið svo út reitina eins og þörf krefur.</span><span class="sxs-lookup"><span data-stu-id="060ae-131">Choose the **Suggest Res. Price Chg. (Res.)** action, and then fill in the fields as necessary.</span></span>  
3. <span data-ttu-id="060ae-132">Velja hnappinn **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="060ae-132">Choose the **OK** button.</span></span>  
4. <span data-ttu-id="060ae-133">Þegar keyrslunni lýkur er glugginn **Verðbreytingar forða** opnaður til að sjá niðurstöður keyrslunnar.</span><span class="sxs-lookup"><span data-stu-id="060ae-133">When the batch job is finished, open the **Resource Price Changes** window to see the results of the batch job.</span></span>

## <a name="to-get-resource-price-change-suggestions-based-on-alternate-prices"></a><span data-ttu-id="060ae-134">Til að fá verðbreytingatillögur forða út frá öðru verði</span><span class="sxs-lookup"><span data-stu-id="060ae-134">To get resource price change suggestions based on alternate prices</span></span>
<span data-ttu-id="060ae-135">Ef þegar er búið að setja upp annað verð fyrir hluta af forðanum er hægt að nota keyrslu til að setja upp fleiri önnur forðaverð.</span><span class="sxs-lookup"><span data-stu-id="060ae-135">If you have already set up alternate resource price for some resources, you can use a batch job to set up multiple alternate resource prices.</span></span>

1. <span data-ttu-id="060ae-136">Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Tillaga forðaverðbr. (Verð)** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="060ae-136">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Suggest Res. Price Chg. (Price)**, and then choose the related link.</span></span>  
2. <span data-ttu-id="060ae-137">Fyllið inn í svæðin eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="060ae-137">Fill in the fields as necessary.</span></span>
3. <span data-ttu-id="060ae-138">Velja hnappinn **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="060ae-138">Choose the **OK** button.</span></span>  
4. <span data-ttu-id="060ae-139">Þegar keyrslunni lýkur er glugginn **Verðbreytingar forða** opnaður til að sjá niðurstöður keyrslunnar.</span><span class="sxs-lookup"><span data-stu-id="060ae-139">When the batch job is finished, open the **Resource Price Changes** window to see the results of the batch job.</span></span>

## <a name="see-also"></a><span data-ttu-id="060ae-140">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="060ae-140">See Also</span></span>
[<span data-ttu-id="060ae-141">Verkefnastjórnun</span><span class="sxs-lookup"><span data-stu-id="060ae-141">Project Management</span></span>](projects-manage-projects.md)  
[<span data-ttu-id="060ae-142">Fjármál</span><span class="sxs-lookup"><span data-stu-id="060ae-142">Finance</span></span>](finance.md)  
<span data-ttu-id="060ae-143">[Innkaup](purchasing-manage-purchasing.md)       </span><span class="sxs-lookup"><span data-stu-id="060ae-143">[Purchasing](purchasing-manage-purchasing.md)       </span></span>  
<span data-ttu-id="060ae-144">[Sala](sales-manage-sales.md)   </span><span class="sxs-lookup"><span data-stu-id="060ae-144">[Sales](sales-manage-sales.md)   </span></span>  
<span data-ttu-id="060ae-145">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="060ae-145">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

