---
title: "Umsjón fjárhagsáætlana fyrir eignir| Microsoft Docs"
description: "Til að hjálpa til við undirbúning fjárhagsáætlana og forspáa, eru settar upp upplýsingar um fjárfestingar, afskráningar og afskriftir eigna í framtíðinni."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: forecast
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 2185a1fc40ddae772e20994f6531b02d7e703e17
ms.contentlocale: is-is
ms.lasthandoff: 09/11/2017


---
# <a name="how-to-manage-budgets-for-fixed-assets"></a><span data-ttu-id="3eafe-103">Hvernig á að: Umsjón fjárhagsáætlana fyrir eignir</span><span class="sxs-lookup"><span data-stu-id="3eafe-103">How to: Manage Budgets for Fixed Assets</span></span>
<span data-ttu-id="3eafe-104">Hægt er að setja upp áætlaðar eignir.</span><span class="sxs-lookup"><span data-stu-id="3eafe-104">You can set up budgeted fixed assets.</span></span> <span data-ttu-id="3eafe-105">Til dæmis leyfir þetta þér að taka með áætluð kaup og sölu í skýrslum.</span><span class="sxs-lookup"><span data-stu-id="3eafe-105">For example, this lets you include anticipated acquisitions and sales in reports.</span></span>  

<span data-ttu-id="3eafe-106">Við gerð áætlaðs rekstrarreiknings, efnahagsreiknings og sjóðstreymis þarf upplýsingar um fjárfestingar, afskráningar og afskriftir eigna í framtíðinni.</span><span class="sxs-lookup"><span data-stu-id="3eafe-106">To prepare your budgeted income statement, budgeted balance sheet, and cash budget, you need information about future investments, disposals and depreciation of fixed assets.</span></span> <span data-ttu-id="3eafe-107">Hægt er að fá þessar upplýsingar í skýrslunni **Eignir - Áætlað virði**.</span><span class="sxs-lookup"><span data-stu-id="3eafe-107">You can get this information from the **Fixed Asset - Projected Value** report.</span></span> <span data-ttu-id="3eafe-108">Áður en skýrslan er prentuð þarf að taka saman fjárhagsáætlunina.</span><span class="sxs-lookup"><span data-stu-id="3eafe-108">Before you print this report, you must prepare the budget.</span></span>  

> [!NOTE]  
>   <span data-ttu-id="3eafe-109">Þessi virkni krefst þess að upplifun þín sé stillt á **Pakki**.</span><span class="sxs-lookup"><span data-stu-id="3eafe-109">This functionality requires that your experience is set to **Suite**.</span></span> <span data-ttu-id="3eafe-110">Nánari upplýsingar, sjá [Sérstilla þína [!INCLUDE[d365fin](includes/d365fin_md.md)] upplifun](ui-experiences.md).</span><span class="sxs-lookup"><span data-stu-id="3eafe-110">For more information, see [Customizing Your [!INCLUDE[d365fin](includes/d365fin_md.md)] Experience](ui-experiences.md).</span></span>

## <a name="to-budget-the-acquisition-cost-of-a-fixed-asset"></a><span data-ttu-id="3eafe-111">Setja kaupverð eignar í fjárhagsáætlun</span><span class="sxs-lookup"><span data-stu-id="3eafe-111">To budget the acquisition cost of a fixed asset</span></span>
<span data-ttu-id="3eafe-112">Til undirbúnings fjárhagsáætlunar verður að stofna eignaspjöld fyrir þær eignir sem ætlunin er að kaupa í framtíðinni.</span><span class="sxs-lookup"><span data-stu-id="3eafe-112">To prepare a budget, you have to set up fixed asset cards for fixed assets that you intend to buy in the future.</span></span> <span data-ttu-id="3eafe-113">Eignir á fjárhagsáætlun eru settar upp eins og venjulegar eignir, en það verður að setja þær upp þannig að þær bókist ekki í fjárhag.</span><span class="sxs-lookup"><span data-stu-id="3eafe-113">The budget fixed assets are set up as ordinary fixed assets, but it must be set up to not post to the general ledger.</span></span>

<span data-ttu-id="3eafe-114">Þegar kaupverð er bókað er færður inn fjöldi áætlaðra eigna í reitnum **Áætlað eignanr.**.</span><span class="sxs-lookup"><span data-stu-id="3eafe-114">When you post the acquisition cost, you enter the number of the budgeted fixed asset in the **Budgeted FA No.**</span></span> <span data-ttu-id="3eafe-115">.</span><span class="sxs-lookup"><span data-stu-id="3eafe-115">field.</span></span> <span data-ttu-id="3eafe-116">Þetta veldur því að forritið bókar stofnkostnað með gagnstæðu formerki á áætluðu eigninni.</span><span class="sxs-lookup"><span data-stu-id="3eafe-116">This will post an acquisition cost with an opposite sign for the budgeted asset.</span></span> <span data-ttu-id="3eafe-117">Heildarstofnkostnaður áætluðu eignarinnar er þá mismunurinn milli áætlaðs og raunverulegs stofnkostnaðar.</span><span class="sxs-lookup"><span data-stu-id="3eafe-117">This means that the total acquisition cost on the budgeted asset is the difference between the budgeted and the actual acquisition cost.</span></span>

1. <span data-ttu-id="3eafe-118">Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **eignir** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="3eafe-118">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Fixed Assets**, and then choose the related link.</span></span>
2. <span data-ttu-id="3eafe-119">Veldu aðgerðina **Nýtt** til að stofna nýtt eignaspjald fyrir áætluðu eignina.</span><span class="sxs-lookup"><span data-stu-id="3eafe-119">Choose the **New** action to create a new fixed asset card for the budgeted fixed asset.</span></span>
3. <span data-ttu-id="3eafe-120">Velja reitnum **Áætluð Eign** gátreitinn til að hindra bókun í fjárhag.</span><span class="sxs-lookup"><span data-stu-id="3eafe-120">Select the **Budgeted Asset** check box to prevent posting to the general ledger.</span></span>
4. <span data-ttu-id="3eafe-121">Hinir reitirnir eru fylltir út, úthluta afskriftabók og bóka síðan fyrsta kaupverð með áætluðu eigninni sem er færð inn í reitinn **Áætlað Eignanr.**</span><span class="sxs-lookup"><span data-stu-id="3eafe-121">Fill in the remaining fields, assign a depreciation book, and then post the first acquisition cost with the budgeted fixed asset entered in the **Budgeted FA No.**</span></span> <span data-ttu-id="3eafe-122">á færslubókarlínunni.</span><span class="sxs-lookup"><span data-stu-id="3eafe-122">field on the journal line.</span></span> <span data-ttu-id="3eafe-123">Nánari upplýsingar eru í [Hvernig á að: komast ufir eignir](fa-how-acquire.md).</span><span class="sxs-lookup"><span data-stu-id="3eafe-123">For more information, see [How to: Acquire Fixed Assets](fa-how-acquire.md).</span></span>

## <a name="to-budget-the-disposal-of-a-fixed-asset"></a><span data-ttu-id="3eafe-124">Setja afskráningu eignar í fjárhagsáætlun</span><span class="sxs-lookup"><span data-stu-id="3eafe-124">To budget the disposal of a fixed asset</span></span>
<span data-ttu-id="3eafe-125">Eigi að selja eignir á áætlunartímabilinu er hægt að færa inn upplýsingar um söluverð og söludagsetningu.</span><span class="sxs-lookup"><span data-stu-id="3eafe-125">If you plan to sell assets within the budget period, you can enter information about sales price and sales date.</span></span>

1. <span data-ttu-id="3eafe-126">Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **eignir** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="3eafe-126">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Fixed Assets**, and then choose the related link.</span></span>
2. <span data-ttu-id="3eafe-127">Valin er eignin sem á að afskrá, og velja síðan **Afskriftabækur** aðgerð.</span><span class="sxs-lookup"><span data-stu-id="3eafe-127">Select the fixed asset to be disposed of, and then choose the **Depreciation Books** action.</span></span>
3. <span data-ttu-id="3eafe-128">Í glugganum **Eignaafskriftabækur** er fært inn í reitina **Áætluð afskráningardags.** og **Áætlaður afrakstur undir reitnum Afskráning**.</span><span class="sxs-lookup"><span data-stu-id="3eafe-128">In the **FA Depreciation Books** window, fill in the **Projected Disposal Date** and **Projected Proceeds on Disposal** fields.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-view-projected-disposal-values"></a><span data-ttu-id="3eafe-129">Skoðun á áætluðu virði afskráninga:</span><span class="sxs-lookup"><span data-stu-id="3eafe-129">To view projected disposal values</span></span>
<span data-ttu-id="3eafe-130">Keyra má skýrsluna **Eignir - Áætlað virði** til að skoða áætlað afskráningarvirði og reikna hagnað/tap.</span><span class="sxs-lookup"><span data-stu-id="3eafe-130">To see the projected disposal values and have the gain and loss calculated, you can use the **FA Projected Value** report.</span></span>

1. <span data-ttu-id="3eafe-131">Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Áætlað virði eigna** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="3eafe-131">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **FA Projected Value**, and then choose the related link.</span></span>
2. <span data-ttu-id="3eafe-132">Fyllið inn í svæðin eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="3eafe-132">Fill in the fields as necessary.</span></span>
3. <span data-ttu-id="3eafe-133">Veljið hnappinn **Prenta** eða **Forskoðun**.</span><span class="sxs-lookup"><span data-stu-id="3eafe-133">Choose the **Print** or **Preview** button.</span></span>

## <a name="to-budget-depreciation"></a><span data-ttu-id="3eafe-134">Áætlun afskrifta:</span><span class="sxs-lookup"><span data-stu-id="3eafe-134">To budget depreciation</span></span>
<span data-ttu-id="3eafe-135">Þú getur notað **Eignir – Áætlað virði** skýrsluna til að reikna afskrift í framtíðinni.</span><span class="sxs-lookup"><span data-stu-id="3eafe-135">You can use the **Fixed Asset - Projected Value** report to calculate future depreciation.</span></span> <span data-ttu-id="3eafe-136">Í skýrslunni er hægt að skoða bókfært virði og uppsafnaðar afskriftir við upphaf valins tímabils, breytingar sem á tímabilinu og bókfært virði og uppsafnaðar afskriftir i lok tímabilsins.</span><span class="sxs-lookup"><span data-stu-id="3eafe-136">The report shows the book value and accumulated depreciation at the start of the selected period, changes during the period, and the book value and accumulated depreciation at the end of the selected period.</span></span>

1. <span data-ttu-id="3eafe-137">Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Áætlað virði eigna** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="3eafe-137">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **FA Projected Value**, and then choose the related link.</span></span>
2. <span data-ttu-id="3eafe-138">Fyllið inn í svæðin eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="3eafe-138">Fill in the fields as necessary.</span></span>
3. <span data-ttu-id="3eafe-139">Til að skoða heildarvirði allra eigna skal hreinsa gátreitinn **Prenta á Eign**.</span><span class="sxs-lookup"><span data-stu-id="3eafe-139">To see total values for all assets, clear the **Print per Fixed Asset** check box.</span></span>
4. <span data-ttu-id="3eafe-140">Flýtiflipinn **Eignir** er hafður auður ef taka á allar eignir með.</span><span class="sxs-lookup"><span data-stu-id="3eafe-140">Leave the **Fixed Asset** FastTab blank to have all assets included.</span></span> <span data-ttu-id="3eafe-141">Ritaðu **Nei** í reitinn **Áætluð eign** til að undanskilja áætlaðar eignir eða **Já** til að skoða einungis áætlaðar eignir.</span><span class="sxs-lookup"><span data-stu-id="3eafe-141">In the **Budgeted Asset** field, enter **No** to exclude budgeted assets or **Yes** to see budgeted assets only.</span></span>
5. <span data-ttu-id="3eafe-142">Veljið hnappinn **Prenta** eða **Forskoðun**.</span><span class="sxs-lookup"><span data-stu-id="3eafe-142">Choose the **Print** or **Preview** button.</span></span>

## <a name="see-also"></a><span data-ttu-id="3eafe-143">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="3eafe-143">See Also</span></span>
[<span data-ttu-id="3eafe-144">Eignir</span><span class="sxs-lookup"><span data-stu-id="3eafe-144">Fixed Assets</span></span>](fa-manage.md)  
[<span data-ttu-id="3eafe-145">Uppsetning eigna</span><span class="sxs-lookup"><span data-stu-id="3eafe-145">Setting Up Fixed Assets</span></span>](fa-setup.md)  
[<span data-ttu-id="3eafe-146">Fjármál</span><span class="sxs-lookup"><span data-stu-id="3eafe-146">Finance</span></span>](finance.md)  
<span data-ttu-id="3eafe-147">[Velkomin(n) í [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)</span><span class="sxs-lookup"><span data-stu-id="3eafe-147">[Welcome to [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)</span></span>  
<span data-ttu-id="3eafe-148">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="3eafe-148">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

