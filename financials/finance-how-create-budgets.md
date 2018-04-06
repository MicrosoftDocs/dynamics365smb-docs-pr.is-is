---
title: "Stofna fjárhagsáætlanir| Microsoft Docs"
description: "Lýsir því hvernig stofna skal fjárhagsáætlanir til að spá fyrir um mismunandi fjármálaaðgerðir og úthluta víddum fyrir viðskiptaupplýsingar."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: postpone
ms.date: 01/25/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: f6969d05cfde9ba7ce5767a961d4af1c7b3bd983
ms.contentlocale: is-is
ms.lasthandoff: 03/22/2018

---
# <a name="create-gl-budgets"></a><span data-ttu-id="e5882-103">Stofna fjárhagsáætlunum</span><span class="sxs-lookup"><span data-stu-id="e5882-103">Create G/L Budgets</span></span>
<span data-ttu-id="e5882-104">Hægt er að útbúa margar áætlanir fyrir sömu tímabil með því að stofna áætlanir undir aðskildum heitum.</span><span class="sxs-lookup"><span data-stu-id="e5882-104">You can have multiple budgets for identical time periods by creating budgets with separate names.</span></span> <span data-ttu-id="e5882-105">Fyrst er heiti áætlunar sett upp og áætlunarupphæðir færðar inn.</span><span class="sxs-lookup"><span data-stu-id="e5882-105">First, you set up the budget name and enter the budget figures.</span></span> <span data-ttu-id="e5882-106">Þá er heiti áætlunarinnar haft með við allar áætlunarfærslur sem stofnaðar eru.</span><span class="sxs-lookup"><span data-stu-id="e5882-106">The budget name is then included on all the budget entries you create.</span></span>  

 <span data-ttu-id="e5882-107">Þegar áætlun er stofnuð er hægt að skilgreina fjórar víddir fyrir hverja áætlun.</span><span class="sxs-lookup"><span data-stu-id="e5882-107">When you create a budget, you can define four dimensions for each budget.</span></span> <span data-ttu-id="e5882-108">Þessar áætlanatengdu víddir kallast áætlanavíddir.</span><span class="sxs-lookup"><span data-stu-id="e5882-108">These budget-specific dimensions are called budget dimensions.</span></span> <span data-ttu-id="e5882-109">Hægt er að velja áætlanavíddir fyrir hverja áætlun úr víddunum sem þegar hafa verið settar upp.</span><span class="sxs-lookup"><span data-stu-id="e5882-109">You select the budget dimensions for each budget from among the dimensions you have already set up.</span></span> <span data-ttu-id="e5882-110">Hægt er að nota áætlanavíddir til að afmarka áætlanir og til að bæta víddaupplýsingum við áætlanafærslur.</span><span class="sxs-lookup"><span data-stu-id="e5882-110">Budget dimensions can be used to set filters on a budget and to add dimension information to budget entries.</span></span> <span data-ttu-id="e5882-111">Frekari upplýsingar er að finna í [Unnið með víddir](finance-dimensions.md).</span><span class="sxs-lookup"><span data-stu-id="e5882-111">For more information, see [Working with Dimensions](finance-dimensions.md).</span></span>

 <span data-ttu-id="e5882-112">Fjárhagsáætlanir spila stórt hlutverk þegar kemur að viðskiptaupplýsingum, eins og í fjárhagsskýrslu sem byggir á fjárhagsskema sem innihalda fjárhagsáætlanafærslur eða þegar verið er að greina áætlaðar og raunverulegar upphæðir í bókhaldslyklunum.</span><span class="sxs-lookup"><span data-stu-id="e5882-112">Budgets play an important role in business intelligence, such as in financial statement based on account schedules that include budget entries or when analyzing budgeted versus actual amounts in the chart of accounts.</span></span> <span data-ttu-id="e5882-113">Frekari upplýsingar eru í [Viðskiptaupplýsingar](bi.md).</span><span class="sxs-lookup"><span data-stu-id="e5882-113">For more information, see [Business Intelligence](bi.md).</span></span>

 <span data-ttu-id="e5882-114">Fjárhagsáætlanir spila stórt hlutverk þegar kemur að viðskiptaupplýsingum, eins og í fjárhagsskýrslu sem byggir á fjárhagsskema sem innihalda fjárhagsáætlanafærslur eða þegar verið er að greina áætlaðar og raunverulegar upphæðir í bókhaldslyklunum.</span><span class="sxs-lookup"><span data-stu-id="e5882-114">Budgets play an important role in business intelligence, such as in financial statement based on account schedules that include budget entries or when analyzing budgeted versus actual amounts in the chart of accounts.</span></span> <span data-ttu-id="e5882-115">Frekari upplýsingar eru í [Viðskiptaupplýsingar](bi.md).</span><span class="sxs-lookup"><span data-stu-id="e5882-115">For more information, see [Business Intelligence](bi.md).</span></span>

<span data-ttu-id="e5882-116">Í kostnaðarbókhaldi vinnurðu með kostnaðaráætlun á svipaðan hátt.</span><span class="sxs-lookup"><span data-stu-id="e5882-116">In cost accounting, you work with cost budgets in a similar way.</span></span> <span data-ttu-id="e5882-117">Frekari upplýsingar eru í [Stofna kostnaðaráætlun](finance-create-cost-budgets.md).</span><span class="sxs-lookup"><span data-stu-id="e5882-117">For more information, see [Creating Cost Budgets](finance-create-cost-budgets.md).</span></span>    

## <a name="to-create-a-new-gl-budget"></a><span data-ttu-id="e5882-118">Að búa til nýja fjárhagsáætlun</span><span class="sxs-lookup"><span data-stu-id="e5882-118">To create a new G/L budget</span></span>  
1. <span data-ttu-id="e5882-119">Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Fjárhagsáætlanir** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="e5882-119">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **G/L Budgets**, and then choose the related link.</span></span>  
2. <span data-ttu-id="e5882-120">Veljið aðgerðina **Breyta lista** og fyllið svo út reitina eins og þörf krefur.</span><span class="sxs-lookup"><span data-stu-id="e5882-120">Choose the **Edit List** action, and then fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. <span data-ttu-id="e5882-121">Velja skal aðgerðina **Breyta fjárhagsáætlun**.</span><span class="sxs-lookup"><span data-stu-id="e5882-121">Choose the **Edit Budget** action.</span></span>
4. <span data-ttu-id="e5882-122">Efst í glugganum **Fjárhagsáætlun** skal fylla inn í reitina eins og þörf krefur, til að skilgreina hvað birtist.</span><span class="sxs-lookup"><span data-stu-id="e5882-122">At the top of the **Budget** window, fill in the fields as necessary to define what is displayed.</span></span>  

    <span data-ttu-id="e5882-123">Aðeins færslur sem innihalda heiti áætlunar sem þú færðir inn í reitinn **Heiti áætlunar** eru sýndar.</span><span class="sxs-lookup"><span data-stu-id="e5882-123">Only entries that contain the budget name that you entered in the **budget Name** field are shown.</span></span> <span data-ttu-id="e5882-124">Þar sem heiti áætlunar er nýstofnað eiga engar áætlanir við afmörkunina.</span><span class="sxs-lookup"><span data-stu-id="e5882-124">Because the budget name has just been created, there are no entries that match the filter.</span></span> <span data-ttu-id="e5882-125">Þess vegna er glugginn auður.</span><span class="sxs-lookup"><span data-stu-id="e5882-125">Therefore, the window is empty.</span></span>  
5. <span data-ttu-id="e5882-126">Til að færa inn rétta upphæð er smellt á viðeigandi reit í fylkinu.</span><span class="sxs-lookup"><span data-stu-id="e5882-126">To enter an amount, choose the relevant cell in the matrix.</span></span> <span data-ttu-id="e5882-127">Glugginn **Fjárhagsáætl.færslur** opnast.</span><span class="sxs-lookup"><span data-stu-id="e5882-127">The **G/L Budget Entries** window opens.</span></span>  
6. <span data-ttu-id="e5882-128">Ný lína er búin til og reiturinn **Upphæð** fylltur út.</span><span class="sxs-lookup"><span data-stu-id="e5882-128">Create a new line and fill in the **Amount** field.</span></span> <span data-ttu-id="e5882-129">Glugganum **Fjárhagsáætl.færslur** er lokað.</span><span class="sxs-lookup"><span data-stu-id="e5882-129">Close the **G/L Budget Entries** window.</span></span>  
7. <span data-ttu-id="e5882-130">Skref 5 og 6 eru endurtekin þar til allar áætlaðar upphæðir eru færðar inn.</span><span class="sxs-lookup"><span data-stu-id="e5882-130">Repeat steps 5 and 6 until you have entered all of the budget amounts.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="e5882-131">Á flýtiflipanum **Afmarkanir** geturðu afmarkað upplýsingar um fjárhagsáætlun með áætlunarvíddum, sem hafa verið settar upp undir heiti áætlunar.</span><span class="sxs-lookup"><span data-stu-id="e5882-131">On the **Filters** FastTab, you can filter the budget information by budget dimensions you have set up under the budget name.</span></span>   

## <a name="see-also"></a><span data-ttu-id="e5882-132">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="e5882-132">See Also</span></span>
[<span data-ttu-id="e5882-133">Fjármál</span><span class="sxs-lookup"><span data-stu-id="e5882-133">Finance</span></span>](finance.md)  
[<span data-ttu-id="e5882-134">Viðskiptaupplýsingar</span><span class="sxs-lookup"><span data-stu-id="e5882-134">Business Intelligence</span></span>](bi.md)  
[<span data-ttu-id="e5882-135">Uppsetning Fjármála</span><span class="sxs-lookup"><span data-stu-id="e5882-135">Setting Up Finance</span></span>](finance-setup-finance.md)  
[<span data-ttu-id="e5882-136">Fjárhagur og bókhaldslyklar</span><span class="sxs-lookup"><span data-stu-id="e5882-136">The General Ledger and the Chart of Accounts</span></span>](finance-general-ledger.md)  
<span data-ttu-id="e5882-137">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="e5882-137">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

