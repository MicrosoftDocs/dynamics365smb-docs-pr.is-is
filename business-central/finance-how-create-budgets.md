---
title: "Stofna fjárhagsáætlanir| Microsoft Docs"
description: "Lýsir því hvernig stofna skal fjárhagsáætlanir til að spá fyrir um mismunandi fjármálaaðgerðir og úthluta víddum fyrir viðskiptaupplýsingar."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: postpone
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: caf7cf5afe370af0c4294c794c0ff9bc8ff4c31c
ms.openlocfilehash: 4cf8738c7bab09f7bcf900baae54731b6772e7e9
ms.contentlocale: is-is
ms.lasthandoff: 11/22/2018

---
# <a name="create-gl-budgets"></a><span data-ttu-id="b9c2d-103">Stofna fjárhagsáætlunum</span><span class="sxs-lookup"><span data-stu-id="b9c2d-103">Create G/L Budgets</span></span>
<span data-ttu-id="b9c2d-104">Hægt er að útbúa margar áætlanir fyrir sömu tímabil með því að stofna áætlanir undir aðskildum heitum.</span><span class="sxs-lookup"><span data-stu-id="b9c2d-104">You can have multiple budgets for identical time periods by creating budgets with separate names.</span></span> <span data-ttu-id="b9c2d-105">Fyrst er heiti áætlunar sett upp og áætlunarupphæðir færðar inn.</span><span class="sxs-lookup"><span data-stu-id="b9c2d-105">First, you set up the budget name and enter the budget figures.</span></span> <span data-ttu-id="b9c2d-106">Þá er heiti áætlunarinnar haft með við allar áætlunarfærslur sem stofnaðar eru.</span><span class="sxs-lookup"><span data-stu-id="b9c2d-106">The budget name is then included on all the budget entries you create.</span></span>  

 <span data-ttu-id="b9c2d-107">Þegar áætlun er stofnuð er hægt að skilgreina fjórar víddir fyrir hverja áætlun.</span><span class="sxs-lookup"><span data-stu-id="b9c2d-107">When you create a budget, you can define four dimensions for each budget.</span></span> <span data-ttu-id="b9c2d-108">Þessar áætlanatengdu víddir kallast áætlanavíddir.</span><span class="sxs-lookup"><span data-stu-id="b9c2d-108">These budget-specific dimensions are called budget dimensions.</span></span> <span data-ttu-id="b9c2d-109">Hægt er að velja áætlanavíddir fyrir hverja áætlun úr víddunum sem þegar hafa verið settar upp.</span><span class="sxs-lookup"><span data-stu-id="b9c2d-109">You select the budget dimensions for each budget from among the dimensions you have already set up.</span></span> <span data-ttu-id="b9c2d-110">Hægt er að nota áætlanavíddir til að afmarka áætlanir og til að bæta víddaupplýsingum við áætlanafærslur.</span><span class="sxs-lookup"><span data-stu-id="b9c2d-110">Budget dimensions can be used to set filters on a budget and to add dimension information to budget entries.</span></span> <span data-ttu-id="b9c2d-111">Frekari upplýsingar er að finna í [Unnið með víddir](finance-dimensions.md).</span><span class="sxs-lookup"><span data-stu-id="b9c2d-111">For more information, see [Working with Dimensions](finance-dimensions.md).</span></span>

 <span data-ttu-id="b9c2d-112">Fjárhagsáætlanir spila stórt hlutverk þegar kemur að viðskiptaupplýsingum, eins og í fjárhagsskýrslu sem byggir á fjárhagsskema sem innihalda fjárhagsáætlanafærslur eða þegar verið er að greina áætlaðar og raunverulegar upphæðir í bókhaldslyklunum.</span><span class="sxs-lookup"><span data-stu-id="b9c2d-112">Budgets play an important role in business intelligence, such as in financial statement based on account schedules that include budget entries or when analyzing budgeted versus actual amounts in the chart of accounts.</span></span> <span data-ttu-id="b9c2d-113">Frekari upplýsingar eru í [Viðskiptaupplýsingar](bi.md).</span><span class="sxs-lookup"><span data-stu-id="b9c2d-113">For more information, see [Business Intelligence](bi.md).</span></span>

 <span data-ttu-id="b9c2d-114">Fjárhagsáætlanir spila stórt hlutverk þegar kemur að viðskiptaupplýsingum, eins og í fjárhagsskýrslu sem byggir á fjárhagsskema sem innihalda fjárhagsáætlanafærslur eða þegar verið er að greina áætlaðar og raunverulegar upphæðir í bókhaldslyklunum.</span><span class="sxs-lookup"><span data-stu-id="b9c2d-114">Budgets play an important role in business intelligence, such as in financial statement based on account schedules that include budget entries or when analyzing budgeted versus actual amounts in the chart of accounts.</span></span> <span data-ttu-id="b9c2d-115">Frekari upplýsingar eru í [Viðskiptaupplýsingar](bi.md).</span><span class="sxs-lookup"><span data-stu-id="b9c2d-115">For more information, see [Business Intelligence](bi.md).</span></span>

<span data-ttu-id="b9c2d-116">Í kostnaðarbókhaldi vinnurðu með kostnaðaráætlun á svipaðan hátt.</span><span class="sxs-lookup"><span data-stu-id="b9c2d-116">In cost accounting, you work with cost budgets in a similar way.</span></span> <span data-ttu-id="b9c2d-117">Frekari upplýsingar eru í [Stofna kostnaðaráætlun](finance-create-cost-budgets.md).</span><span class="sxs-lookup"><span data-stu-id="b9c2d-117">For more information, see [Creating Cost Budgets](finance-create-cost-budgets.md).</span></span>    

## <a name="to-create-a-new-gl-budget"></a><span data-ttu-id="b9c2d-118">Að búa til nýja fjárhagsáætlun</span><span class="sxs-lookup"><span data-stu-id="b9c2d-118">To create a new G/L budget</span></span>  
1. <span data-ttu-id="b9c2d-119">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Fjárhagsáætlun** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="b9c2d-119">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **G/L Budgets**, and then choose the related link.</span></span>  
2. <span data-ttu-id="b9c2d-120">Veljið aðgerðina **Breyta lista** og fyllið svo út reitina eins og þörf krefur.</span><span class="sxs-lookup"><span data-stu-id="b9c2d-120">Choose the **Edit List** action, and then fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. <span data-ttu-id="b9c2d-121">Velja skal aðgerðina **Breyta fjárhagsáætlun**.</span><span class="sxs-lookup"><span data-stu-id="b9c2d-121">Choose the **Edit Budget** action.</span></span>
4. <span data-ttu-id="b9c2d-122">Efst á síðunni **Fjárhagsáætlun** skal fylla inn í reitina eins og þörf krefur, til að skilgreina hvað birtist.</span><span class="sxs-lookup"><span data-stu-id="b9c2d-122">At the top of the **Budget** page, fill in the fields as necessary to define what is displayed.</span></span>  

    <span data-ttu-id="b9c2d-123">Aðeins færslur sem innihalda heiti áætlunar sem þú færðir inn í reitinn **Heiti áætlunar** eru sýndar.</span><span class="sxs-lookup"><span data-stu-id="b9c2d-123">Only entries that contain the budget name that you entered in the **budget Name** field are shown.</span></span> <span data-ttu-id="b9c2d-124">Þar sem heiti áætlunar er nýstofnað eiga engar áætlanir við afmörkunina.</span><span class="sxs-lookup"><span data-stu-id="b9c2d-124">Because the budget name has just been created, there are no entries that match the filter.</span></span> <span data-ttu-id="b9c2d-125">Síðan er þar af leiðandi tóm.</span><span class="sxs-lookup"><span data-stu-id="b9c2d-125">Therefore, the page is empty.</span></span>  
5. <span data-ttu-id="b9c2d-126">Til að færa inn rétta upphæð er smellt á viðeigandi reit í fylkinu.</span><span class="sxs-lookup"><span data-stu-id="b9c2d-126">To enter an amount, choose the relevant cell in the matrix.</span></span> <span data-ttu-id="b9c2d-127">Síðan **Fjárhagsáætl.færslur** opnast.</span><span class="sxs-lookup"><span data-stu-id="b9c2d-127">The **G/L Budget Entries** page opens.</span></span>  
6. <span data-ttu-id="b9c2d-128">Ný lína er búin til og reiturinn **Upphæð** fylltur út.</span><span class="sxs-lookup"><span data-stu-id="b9c2d-128">Create a new line and fill in the **Amount** field.</span></span> <span data-ttu-id="b9c2d-129">Loka síðunni **Fjárhagsáætlunarfærslur**.</span><span class="sxs-lookup"><span data-stu-id="b9c2d-129">Close the **G/L Budget Entries** page.</span></span>  
7. <span data-ttu-id="b9c2d-130">Skref 5 og 6 eru endurtekin þar til allar áætlaðar upphæðir eru færðar inn.</span><span class="sxs-lookup"><span data-stu-id="b9c2d-130">Repeat steps 5 and 6 until you have entered all of the budget amounts.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="b9c2d-131">Á flýtiflipanum **Afmarkanir** geturðu afmarkað upplýsingar um fjárhagsáætlun með áætlunarvíddum, sem hafa verið settar upp undir heiti áætlunar.</span><span class="sxs-lookup"><span data-stu-id="b9c2d-131">On the **Filters** FastTab, you can filter the budget information by budget dimensions you have set up under the budget name.</span></span>   

## <a name="see-also"></a><span data-ttu-id="b9c2d-132">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="b9c2d-132">See Also</span></span>
[<span data-ttu-id="b9c2d-133">Fjármál</span><span class="sxs-lookup"><span data-stu-id="b9c2d-133">Finance</span></span>](finance.md)  
[<span data-ttu-id="b9c2d-134">Viðskiptaupplýsingar</span><span class="sxs-lookup"><span data-stu-id="b9c2d-134">Business Intelligence</span></span>](bi.md)  
[<span data-ttu-id="b9c2d-135">Uppsetning Fjármála</span><span class="sxs-lookup"><span data-stu-id="b9c2d-135">Setting Up Finance</span></span>](finance-setup-finance.md)  
[<span data-ttu-id="b9c2d-136">Fjárhagur og bókhaldslyklar</span><span class="sxs-lookup"><span data-stu-id="b9c2d-136">The General Ledger and the Chart of Accounts</span></span>](finance-general-ledger.md)  
<span data-ttu-id="b9c2d-137">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="b9c2d-137">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

