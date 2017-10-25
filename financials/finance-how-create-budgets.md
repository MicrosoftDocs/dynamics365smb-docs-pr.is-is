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
ms.date: 06/16/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: cda69d70ece090a149a13e5e1f4ed02fa70c49f7
ms.contentlocale: is-is
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-create--budgets"></a><span data-ttu-id="4cc8f-103">Hvernig á að: stofna fjárhagsáætlanir</span><span class="sxs-lookup"><span data-stu-id="4cc8f-103">How to: Create  Budgets</span></span>
<span data-ttu-id="4cc8f-104">Hægt er að útbúa margar áætlanir fyrir sömu tímabil með því að stofna áætlanir undir aðskildum heitum.</span><span class="sxs-lookup"><span data-stu-id="4cc8f-104">You can have multiple budgets for identical time periods by creating budgets with separate names.</span></span> <span data-ttu-id="4cc8f-105">Fyrst er heiti áætlunar sett upp og áætlunarupphæðir færðar inn.</span><span class="sxs-lookup"><span data-stu-id="4cc8f-105">First, you set up the budget name and enter the budget figures.</span></span> <span data-ttu-id="4cc8f-106">Þá er heiti áætlunarinnar haft með við allar áætlunarfærslur sem stofnaðar eru.</span><span class="sxs-lookup"><span data-stu-id="4cc8f-106">The budget name is then included on all the budget entries you create.</span></span>  

 <span data-ttu-id="4cc8f-107">Þegar áætlun er stofnuð er hægt að skilgreina fjórar víddir fyrir hverja áætlun.</span><span class="sxs-lookup"><span data-stu-id="4cc8f-107">When you create a budget, you can define four dimensions for each budget.</span></span> <span data-ttu-id="4cc8f-108">Þessar áætlanatengdu víddir kallast áætlanavíddir.</span><span class="sxs-lookup"><span data-stu-id="4cc8f-108">These budget-specific dimensions are called budget dimensions.</span></span> <span data-ttu-id="4cc8f-109">Hægt er að velja áætlanavíddir fyrir hverja áætlun úr víddunum sem þegar hafa verið settar upp.</span><span class="sxs-lookup"><span data-stu-id="4cc8f-109">You select the budget dimensions for each budget from among the dimensions you have already set up.</span></span> <span data-ttu-id="4cc8f-110">Hægt er að nota áætlanavíddir til að afmarka áætlanir og til að bæta víddaupplýsingum við áætlanafærslur.</span><span class="sxs-lookup"><span data-stu-id="4cc8f-110">Budget dimensions can be used to set filters on a budget and to add dimension information to budget entries.</span></span> <span data-ttu-id="4cc8f-111">Frekari upplýsingar er að finna í [Unnið með víddir](finance-dimensions.md).</span><span class="sxs-lookup"><span data-stu-id="4cc8f-111">For more information, see [Working with Dimensions](finance-dimensions.md).</span></span>

 <span data-ttu-id="4cc8f-112">Fjárhagsáætlanir spila stórt hlutverk þegar kemur að viðskiptaupplýsingum, eins og í fjárhagsskýrslu sem byggir á fjárhagsskema sem innihalda fjárhagsáætlanafærslur eða þegar verið er að greina áætlaðar og raunverulegar upphæðir í bókhaldslyklunum.</span><span class="sxs-lookup"><span data-stu-id="4cc8f-112">Budgets play an important role in business intelligence, such as in financial statement based on account schedules that include budget entries or when analyzing budgeted versus actual amounts in the chart of accounts.</span></span> <span data-ttu-id="4cc8f-113">Frekari upplýsingar eru í [Viðskiptaupplýsingar](bi.md).</span><span class="sxs-lookup"><span data-stu-id="4cc8f-113">For more information, see [Business Intelligence](bi.md).</span></span>

 <span data-ttu-id="4cc8f-114">Fjárhagsáætlanir spila stórt hlutverk þegar kemur að viðskiptaupplýsingum, eins og í fjárhagsskýrslu sem byggir á fjárhagsskema sem innihalda fjárhagsáætlanafærslur eða þegar verið er að greina áætlaðar og raunverulegar upphæðir í bókhaldslyklunum.</span><span class="sxs-lookup"><span data-stu-id="4cc8f-114">Budgets play an important role in business intelligence, such as in financial statement based on account schedules that include budget entries or when analyzing budgeted versus actual amounts in the chart of accounts.</span></span> <span data-ttu-id="4cc8f-115">Frekari upplýsingar eru í [Viðskiptaupplýsingar](bi.md).</span><span class="sxs-lookup"><span data-stu-id="4cc8f-115">For more information, see [Business Intelligence](bi.md).</span></span>

<span data-ttu-id="4cc8f-116">Í kostnaðarbókhaldi vinnurðu með kostnaðaráætlun á svipaðan hátt.</span><span class="sxs-lookup"><span data-stu-id="4cc8f-116">In cost accounting, you work with cost budgets in a similar way.</span></span> <span data-ttu-id="4cc8f-117">Frekari upplýsingar eru í [Stofna kostnaðaráætlun](finance-create-cost-budgets.md).</span><span class="sxs-lookup"><span data-stu-id="4cc8f-117">For more information, see [Creating Cost Budgets](finance-create-cost-budgets.md).</span></span>    

 > [!NOTE]  
>   <span data-ttu-id="4cc8f-118">Þessi virkni krefst þess að upplifun þín sé stillt á **Suite**.</span><span class="sxs-lookup"><span data-stu-id="4cc8f-118">This functionality requires that your experience is set to **Suite**.</span></span> <span data-ttu-id="4cc8f-119">Nánari upplýsingar, sjá [Sérstilla þína [!INCLUDE[d365fin](includes/d365fin_md.md)] upplifun](ui-experiences.md).</span><span class="sxs-lookup"><span data-stu-id="4cc8f-119">For more information, see [Customizing Your [!INCLUDE[d365fin](includes/d365fin_md.md)] Experience](ui-experiences.md).</span></span>  

### <a name="to-create-a-new-budget"></a><span data-ttu-id="4cc8f-120">Að búa til nýja fjárhagsáætlun.</span><span class="sxs-lookup"><span data-stu-id="4cc8f-120">To create a new budget</span></span>  

1. <span data-ttu-id="4cc8f-121">Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Fjárhagsáætlanir** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="4cc8f-121">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **G/L Budgets**, and then choose the related link.</span></span>  
2. <span data-ttu-id="4cc8f-122">Veljið aðgerðina **Breyta lista** og fyllið svo út reitina eins og þörf krefur.</span><span class="sxs-lookup"><span data-stu-id="4cc8f-122">Choose the **Edit List** action, and then fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. <span data-ttu-id="4cc8f-123">Velja skal aðgerðina **Breyta fjárhagsáætlun**.</span><span class="sxs-lookup"><span data-stu-id="4cc8f-123">Choose the **Edit Budget** action.</span></span>
4. <span data-ttu-id="4cc8f-124">Efst í glugganum **Fjárhagsáætlun** skal fylla inn í reitina eins og þörf krefur, til að skilgreina hvað birtist.</span><span class="sxs-lookup"><span data-stu-id="4cc8f-124">At the top of the **Budget** window, fill in the fields as necessary to define what is displayed.</span></span>  

    <span data-ttu-id="4cc8f-125">Aðeins færslur sem innihalda heiti áætlunar sem þú færðir inn í reitinn **Heiti áætlunar** eru sýndar.</span><span class="sxs-lookup"><span data-stu-id="4cc8f-125">Only entries that contain the budget name that you entered in the **budget Name** field are shown.</span></span> <span data-ttu-id="4cc8f-126">Þar sem heiti áætlunar er nýstofnað eiga engar áætlanir við afmörkunina.</span><span class="sxs-lookup"><span data-stu-id="4cc8f-126">Because the budget name has just been created, there are no entries that match the filter.</span></span> <span data-ttu-id="4cc8f-127">Þess vegna er glugginn auður.</span><span class="sxs-lookup"><span data-stu-id="4cc8f-127">Therefore, the window is empty.</span></span>  
5. <span data-ttu-id="4cc8f-128">Til að færa inn rétta upphæð er smellt á viðeigandi reit í fylkinu.</span><span class="sxs-lookup"><span data-stu-id="4cc8f-128">To enter an amount, choose the relevant cell in the matrix.</span></span> <span data-ttu-id="4cc8f-129">Glugginn **Fjárhagsáætl.færslur** opnast.</span><span class="sxs-lookup"><span data-stu-id="4cc8f-129">The **G/L Budget Entries** window opens.</span></span>  
6. <span data-ttu-id="4cc8f-130">Ný lína er búin til og reiturinn **Upphæð** fylltur út.</span><span class="sxs-lookup"><span data-stu-id="4cc8f-130">Create a new line and fill in the **Amount** field.</span></span> <span data-ttu-id="4cc8f-131">Glugganum **Fjárhagsáætl.færslur** er lokað.</span><span class="sxs-lookup"><span data-stu-id="4cc8f-131">Close the **G/L Budget Entries** window.</span></span>  
7. <span data-ttu-id="4cc8f-132">Skref 5 og 6 eru endurtekin þar til allar áætlaðar upphæðir eru færðar inn.</span><span class="sxs-lookup"><span data-stu-id="4cc8f-132">Repeat steps 5 and 6 until you have entered all of the budget amounts.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="4cc8f-133">Á flýtiflipanum **Afmarkanir** geturðu afmarkað upplýsingar um fjárhagsáætlun með áætlunarvíddum, sem hafa verið settar upp undir heiti áætlunar.</span><span class="sxs-lookup"><span data-stu-id="4cc8f-133">On the **Filters** FastTab, you can filter the budget information by budget dimensions you have set up under the budget name.</span></span>   

## <a name="see-also"></a><span data-ttu-id="4cc8f-134">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="4cc8f-134">See Also</span></span>
[<span data-ttu-id="4cc8f-135">Fjármál</span><span class="sxs-lookup"><span data-stu-id="4cc8f-135">Finance</span></span>](finance.md)  
[<span data-ttu-id="4cc8f-136">Viðskiptaupplýsingar</span><span class="sxs-lookup"><span data-stu-id="4cc8f-136">Business Intelligence</span></span>](bi.md)  
[<span data-ttu-id="4cc8f-137">Uppsetning Fjármála</span><span class="sxs-lookup"><span data-stu-id="4cc8f-137">Setting Up Finance</span></span>](finance-setup-finance.md)  
[<span data-ttu-id="4cc8f-138">Fjárhagur og bókhaldslyklar</span><span class="sxs-lookup"><span data-stu-id="4cc8f-138">The General Ledger and the Chart of Accounts</span></span>](finance-general-ledger.md)  
<span data-ttu-id="4cc8f-139">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="4cc8f-139">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

