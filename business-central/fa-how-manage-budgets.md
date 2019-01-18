---
title: "Umsjón fjárhagsáætlana fyrir eignir| Microsoft Docs"
description: "Til að hjálpa til við undirbúning fjárhagsáætlana og forspáa, eru settar upp upplýsingar um fjárfestingar, afskráningar og afskriftir eigna í framtíðinni."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: forecast
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: 12833530e37ed092cec5f410afdf7f4f52cd46b1
ms.contentlocale: is-is
ms.lasthandoff: 11/26/2018

---
# <a name="manage-budgets-for-fixed-assets"></a><span data-ttu-id="4d573-103">Umsjón fjárhagsáætlana fyrir eignir</span><span class="sxs-lookup"><span data-stu-id="4d573-103">Manage Budgets for Fixed Assets</span></span>
<span data-ttu-id="4d573-104">Hægt er að setja upp áætlaðar eignir.</span><span class="sxs-lookup"><span data-stu-id="4d573-104">You can set up budgeted fixed assets.</span></span> <span data-ttu-id="4d573-105">Til dæmis leyfir þetta þér að taka með áætluð kaup og sölu í skýrslum.</span><span class="sxs-lookup"><span data-stu-id="4d573-105">For example, this lets you include anticipated acquisitions and sales in reports.</span></span>  

<span data-ttu-id="4d573-106">Við gerð áætlaðs rekstrarreiknings, efnahagsreiknings og sjóðstreymis þarf upplýsingar um fjárfestingar, afskráningar og afskriftir eigna í framtíðinni.</span><span class="sxs-lookup"><span data-stu-id="4d573-106">To prepare your budgeted income statement, budgeted balance sheet, and cash budget, you need information about future investments, disposals and depreciation of fixed assets.</span></span> <span data-ttu-id="4d573-107">Hægt er að fá þessar upplýsingar í skýrslunni **Eignir - Áætlað virði**.</span><span class="sxs-lookup"><span data-stu-id="4d573-107">You can get this information from the **Fixed Asset - Projected Value** report.</span></span> <span data-ttu-id="4d573-108">Áður en skýrslan er prentuð þarf að taka saman fjárhagsáætlunina.</span><span class="sxs-lookup"><span data-stu-id="4d573-108">Before you print this report, you must prepare the budget.</span></span>  

## <a name="to-budget-the-acquisition-cost-of-a-fixed-asset"></a><span data-ttu-id="4d573-109">Setja kaupverð eignar í fjárhagsáætlun</span><span class="sxs-lookup"><span data-stu-id="4d573-109">To budget the acquisition cost of a fixed asset</span></span>
<span data-ttu-id="4d573-110">Til undirbúnings fjárhagsáætlunar verður að stofna eignaspjöld fyrir þær eignir sem ætlunin er að kaupa í framtíðinni.</span><span class="sxs-lookup"><span data-stu-id="4d573-110">To prepare a budget, you have to set up fixed asset cards for fixed assets that you intend to buy in the future.</span></span> <span data-ttu-id="4d573-111">Eignir á fjárhagsáætlun eru settar upp eins og venjulegar eignir, en það verður að setja þær upp þannig að þær bókist ekki í fjárhag.</span><span class="sxs-lookup"><span data-stu-id="4d573-111">The budget fixed assets are set up as ordinary fixed assets, but it must be set up to not post to the general ledger.</span></span>

<span data-ttu-id="4d573-112">Þegar kaupverð er bókað er færður inn fjöldi áætlaðra eigna í reitnum **Áætlað eignanr.**.</span><span class="sxs-lookup"><span data-stu-id="4d573-112">When you post the acquisition cost, you enter the number of the budgeted fixed asset in the **Budgeted FA No.** field.</span></span> <span data-ttu-id="4d573-113">Þetta veldur því að forritið bókar stofnkostnað með gagnstæðu formerki á áætluðu eigninni.</span><span class="sxs-lookup"><span data-stu-id="4d573-113">This will post an acquisition cost with an opposite sign for the budgeted asset.</span></span> <span data-ttu-id="4d573-114">Heildarstofnkostnaður áætluðu eignarinnar er þá mismunurinn milli áætlaðs og raunverulegs stofnkostnaðar.</span><span class="sxs-lookup"><span data-stu-id="4d573-114">This means that the total acquisition cost on the budgeted asset is the difference between the budgeted and the actual acquisition cost.</span></span>

1. <span data-ttu-id="4d573-115">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Eignir** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="4d573-115">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Fixed Assets**, and then choose the related link.</span></span>
2. <span data-ttu-id="4d573-116">Veldu aðgerðina **Nýtt** til að stofna nýtt eignaspjald fyrir áætluðu eignina.</span><span class="sxs-lookup"><span data-stu-id="4d573-116">Choose the **New** action to create a new fixed asset card for the budgeted fixed asset.</span></span>
3. <span data-ttu-id="4d573-117">Velja reitnum **Áætluð Eign** gátreitinn til að hindra bókun í fjárhag.</span><span class="sxs-lookup"><span data-stu-id="4d573-117">Select the **Budgeted Asset** check box to prevent posting to the general ledger.</span></span>
4. <span data-ttu-id="4d573-118">Hinir reitirnir eru fylltir út, úthluta afskriftabók og bóka síðan fyrsta kaupverð með áætluðu eigninni sem er færð inn í reitinn **Áætlað Eignanr.** á færslubókarlínunni.</span><span class="sxs-lookup"><span data-stu-id="4d573-118">Fill in the remaining fields, assign a depreciation book, and then post the first acquisition cost with the budgeted fixed asset entered in the **Budgeted FA No.** field on the journal line.</span></span> <span data-ttu-id="4d573-119">Nánari upplýsingar eru í [Komast yfir eignir](fa-how-acquire.md).</span><span class="sxs-lookup"><span data-stu-id="4d573-119">For more information, see [Acquire Fixed Assets](fa-how-acquire.md).</span></span>

## <a name="to-budget-the-disposal-of-a-fixed-asset"></a><span data-ttu-id="4d573-120">Setja afskráningu eignar í fjárhagsáætlun</span><span class="sxs-lookup"><span data-stu-id="4d573-120">To budget the disposal of a fixed asset</span></span>
<span data-ttu-id="4d573-121">Eigi að selja eignir á áætlunartímabilinu er hægt að færa inn upplýsingar um söluverð og söludagsetningu.</span><span class="sxs-lookup"><span data-stu-id="4d573-121">If you plan to sell assets within the budget period, you can enter information about sales price and sales date.</span></span>

1. <span data-ttu-id="4d573-122">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Eignir** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="4d573-122">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Fixed Assets**, and then choose the related link.</span></span>
2. <span data-ttu-id="4d573-123">Valin er eignin sem á að afskrá, og velja síðan **Afskriftabækur** aðgerð.</span><span class="sxs-lookup"><span data-stu-id="4d573-123">Select the fixed asset to be disposed of, and then choose the **Depreciation Books** action.</span></span>
3. <span data-ttu-id="4d573-124">Á síðunni **Eignaafskriftabækur** er fært inn í reitina **Áætluð afskráningardags.** og **Áætlaður afrakstur undir reitnum Afskráning**.</span><span class="sxs-lookup"><span data-stu-id="4d573-124">On the **FA Depreciation Books** page, fill in the **Projected Disposal Date** and **Projected Proceeds on Disposal** fields.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-view-projected-disposal-values"></a><span data-ttu-id="4d573-125">Skoðun á áætluðu virði afskráninga:</span><span class="sxs-lookup"><span data-stu-id="4d573-125">To view projected disposal values</span></span>
<span data-ttu-id="4d573-126">Keyra má skýrsluna **Eignir - Áætlað virði** til að skoða áætlað afskráningarvirði og reikna hagnað/tap.</span><span class="sxs-lookup"><span data-stu-id="4d573-126">To see the projected disposal values and have the gain and loss calculated, you can use the **FA Projected Value** report.</span></span>

1. <span data-ttu-id="4d573-127">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Áætlað virði eigna** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="4d573-127">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **FA Projected Value**, and then choose the related link.</span></span>
2. <span data-ttu-id="4d573-128">Fyllið inn í svæðin eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="4d573-128">Fill in the fields as necessary.</span></span>
3. <span data-ttu-id="4d573-129">Veljið hnappinn **Prenta** eða **Forskoðun**.</span><span class="sxs-lookup"><span data-stu-id="4d573-129">Choose the **Print** or **Preview** button.</span></span>

## <a name="to-budget-depreciation"></a><span data-ttu-id="4d573-130">Áætlun afskrifta:</span><span class="sxs-lookup"><span data-stu-id="4d573-130">To budget depreciation</span></span>
<span data-ttu-id="4d573-131">Þú getur notað **Eignir – Áætlað virði** skýrsluna til að reikna afskrift í framtíðinni.</span><span class="sxs-lookup"><span data-stu-id="4d573-131">You can use the **Fixed Asset - Projected Value** report to calculate future depreciation.</span></span> <span data-ttu-id="4d573-132">Í skýrslunni er hægt að skoða bókfært virði og uppsafnaðar afskriftir við upphaf valins tímabils, breytingar sem á tímabilinu og bókfært virði og uppsafnaðar afskriftir i lok tímabilsins.</span><span class="sxs-lookup"><span data-stu-id="4d573-132">The report shows the book value and accumulated depreciation at the start of the selected period, changes during the period, and the book value and accumulated depreciation at the end of the selected period.</span></span>

1. <span data-ttu-id="4d573-133">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Áætlað virði eigna** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="4d573-133">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **FA Projected Value**, and then choose the related link.</span></span>
2. <span data-ttu-id="4d573-134">Fyllið inn í svæðin eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="4d573-134">Fill in the fields as necessary.</span></span>
3. <span data-ttu-id="4d573-135">Til að skoða heildarvirði allra eigna skal hreinsa gátreitinn **Prenta á Eign**.</span><span class="sxs-lookup"><span data-stu-id="4d573-135">To see total values for all assets, clear the **Print per Fixed Asset** check box.</span></span>
4. <span data-ttu-id="4d573-136">Flýtiflipinn **Eignir** er hafður auður ef taka á allar eignir með.</span><span class="sxs-lookup"><span data-stu-id="4d573-136">Leave the **Fixed Asset** FastTab blank to have all assets included.</span></span> <span data-ttu-id="4d573-137">Ritaðu **Nei** í reitinn **Áætluð eign** til að undanskilja áætlaðar eignir eða **Já** til að skoða einungis áætlaðar eignir.</span><span class="sxs-lookup"><span data-stu-id="4d573-137">In the **Budgeted Asset** field, enter **No** to exclude budgeted assets or **Yes** to see budgeted assets only.</span></span>
5. <span data-ttu-id="4d573-138">Veljið hnappinn **Prenta** eða **Forskoðun**.</span><span class="sxs-lookup"><span data-stu-id="4d573-138">Choose the **Print** or **Preview** button.</span></span>

## <a name="see-also"></a><span data-ttu-id="4d573-139">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="4d573-139">See Also</span></span>
[<span data-ttu-id="4d573-140">Eignir</span><span class="sxs-lookup"><span data-stu-id="4d573-140">Fixed Assets</span></span>](fa-manage.md)  
[<span data-ttu-id="4d573-141">Uppsetning eigna</span><span class="sxs-lookup"><span data-stu-id="4d573-141">Setting Up Fixed Assets</span></span>](fa-setup.md)  
[<span data-ttu-id="4d573-142">Fjármál</span><span class="sxs-lookup"><span data-stu-id="4d573-142">Finance</span></span>](finance.md)  
[<span data-ttu-id="4d573-143">Hafist handa</span><span class="sxs-lookup"><span data-stu-id="4d573-143">Getting Started</span></span>](product-get-started.md)  
<span data-ttu-id="4d573-144">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="4d573-144">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

