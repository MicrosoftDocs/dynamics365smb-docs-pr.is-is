---
title: "Greina raunverulegar og áætlaðar upphæðir| Microsoft Docs"
description: "Lýsir því hvernig greina skal raunverulegar upphæðir annars vegar og áætlaðar upphæðir hins vegar."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bi, power BI, analysis, KPI
ms.date: 06/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 126c8da9b9ef80e954510fa8e5089906d7dd6f01
ms.contentlocale: is-is
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-analyze-actual-amounts-versus-budgeted-amounts"></a><span data-ttu-id="1ec09-103">Hvernig skal: Greina raunverulegar og áætlaðar upphæðir</span><span class="sxs-lookup"><span data-stu-id="1ec09-103">How to: Analyze Actual Amounts Versus Budgeted Amounts</span></span>
<span data-ttu-id="1ec09-104">Hluti af því að safna saman, greina og deila upplýsingum fyrirtækis, er að skoða raunverulegar upphæðir í samanburði við áætlaðar upphæðir fyrir alla reikninga og nokkur tímabil.</span><span class="sxs-lookup"><span data-stu-id="1ec09-104">As a part of gathering, analyzing, and sharing your company data, you view actual amounts compared to budgeted amounts for all accounts and for several periods.</span></span>

<span data-ttu-id="1ec09-105">Til að greina áætlaðar upphæðir, verður fyrst að búa til fjárhagsáætlun.</span><span class="sxs-lookup"><span data-stu-id="1ec09-105">To analyze budgeted amounts, you must first create budgets.</span></span> <span data-ttu-id="1ec09-106">Nánari upplýsingar eru í [Hvernig á að: Búa til fjárhagsáætlanir](finance-how-create-budgets.md).</span><span class="sxs-lookup"><span data-stu-id="1ec09-106">For more information, see [How to: Create Budgets](finance-how-create-budgets.md).</span></span>

> [!NOTE]  
>   <span data-ttu-id="1ec09-107">Þessi virkni krefst þess að upplifun þín sé stillt á **Suite**.</span><span class="sxs-lookup"><span data-stu-id="1ec09-107">This functionality requires that your experience is set to **Suite**.</span></span> <span data-ttu-id="1ec09-108">Nánari upplýsingar, sjá [Sérstilla þína [!INCLUDE[d365fin](includes/d365fin_md.md)] upplifun](ui-experiences.md).</span><span class="sxs-lookup"><span data-stu-id="1ec09-108">For more information, see [Customizing Your [!INCLUDE[d365fin](includes/d365fin_md.md)] Experience](ui-experiences.md).</span></span>

## <a name="to-view-a-budget"></a><span data-ttu-id="1ec09-109">Að skoða áætlun</span><span class="sxs-lookup"><span data-stu-id="1ec09-109">To view a budget</span></span>
<span data-ttu-id="1ec09-110">Í áætlun með víddum er hægt að setja afmarkanir á færslurnar og sjá tilteknar áætlanir.</span><span class="sxs-lookup"><span data-stu-id="1ec09-110">In a budget with dimensions, you can filter the entries and see specific budgets.</span></span>

1. <span data-ttu-id="1ec09-111">Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Fjárhagsáætlanir** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="1ec09-111">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **G/L Budgets**, and then choose the related link.</span></span>
2. <span data-ttu-id="1ec09-112">Í glugganum **Fjárhagsáætlanir** skal velja þá áætlun sem á að skoða.</span><span class="sxs-lookup"><span data-stu-id="1ec09-112">In the **G/L Budgets** window, open the budget that you want to view.</span></span>  
3. <span data-ttu-id="1ec09-113">Efst í glugganum skal fylla inn í reitina eins og þörf krefur, til að skilgreina hvað birtist.</span><span class="sxs-lookup"><span data-stu-id="1ec09-113">At the top of the window, fill in the fields as necessary to define what is shown.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
>   <span data-ttu-id="1ec09-114">Ef valið var **Tímabil** annað hvort í reitnum **Sýna sem línur** eða **Sýna sem dálka** þarf að fylla út reitinn **Skoða eftir**.</span><span class="sxs-lookup"><span data-stu-id="1ec09-114">If you have selected **Period** in either the **Show as Lines** or the **Show as Columns** field, then you must fill in the **View by** field.</span></span> <span data-ttu-id="1ec09-115">Ef ekki hefur verið valið **Tímabil**, hvorki í reitnum **Sýna sem línur** né **Sýna sem dálka**, skal slá inn viðeigandi tímabil í reitnum **Dags.afmörkun**.</span><span class="sxs-lookup"><span data-stu-id="1ec09-115">If you have not selected **Period** in either the **Show as Lines** or **Show as Columns** field, then enter the appropriate period in **Date Filter** field.</span></span>  

> [!NOTE]  
>   <span data-ttu-id="1ec09-116">Aðeins færslur úr fjárhagsáætlun með afmörkunarkótum sem færðir eru inn á flýtiflipanum **Afmarkanir** eru teknar með í útreikninginn.</span><span class="sxs-lookup"><span data-stu-id="1ec09-116">Only entries from the general ledger budget with the filter codes that you enter on the **Filters** FastTab are included in the calculation.</span></span> <span data-ttu-id="1ec09-117">Áætlunarfærslur með aðra afmörkunarkóta eða án nokkurra afmörkunarkóta teljast ekki með.</span><span class="sxs-lookup"><span data-stu-id="1ec09-117">Budget entries with other filter codes or without any filter codes are not included.</span></span> <span data-ttu-id="1ec09-118">Á meðan afmörkunin er stillt á gluggann sýnir áætlunin aðeins áætlunarfærslur með þessum afmörkunarkótum.</span><span class="sxs-lookup"><span data-stu-id="1ec09-118">As long as the filter remains on the window, the budget only displays the budget entries with these filter codes.</span></span>  

> [!TIP]  
>   <span data-ttu-id="1ec09-119">Ef þörf er á að breyta áætlun, er hægt að breyta áætlunarfærslunum.</span><span class="sxs-lookup"><span data-stu-id="1ec09-119">If you want to modify the budget, you can modify the budget entries.</span></span> <span data-ttu-id="1ec09-120">Velja upphæð til að skoða undirliggjandi fjárhagsáætlunarfærslur.</span><span class="sxs-lookup"><span data-stu-id="1ec09-120">Choose an amount to view the underlying general ledger budget entries.</span></span>

## <a name="to-view-actual-and-budgeted-amounts-for-all-accounts"></a><span data-ttu-id="1ec09-121">Að skoða raunverulegar og áætlaðar upphæðir fyrir alla reikninga</span><span class="sxs-lookup"><span data-stu-id="1ec09-121">To view actual and budgeted amounts for all accounts</span></span>  
<span data-ttu-id="1ec09-122">Hægt er að skoða fjárhagsáætlanir og bera þær saman við raunverulegar upphæðir í mörgum svæðum í [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="1ec09-122">You can view general ledger budgets and compare them with actual figures in several areas of [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

1. <span data-ttu-id="1ec09-123">Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **bókhaldslykill** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="1ec09-123">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Chart of Accounts**, and then choose the related link.</span></span>  
2. <span data-ttu-id="1ec09-124">Í glugganum **Bókhaldslykill**, skal velja aðgerðina **Fjárhagur staða/áætlun**.</span><span class="sxs-lookup"><span data-stu-id="1ec09-124">In the **Chart of Accounts** window, choose the **G/L Balance/Budget** action.</span></span>
3. <span data-ttu-id="1ec09-125">Efst í glugganum skal fylla inn í reitina eins og þörf krefur, til að skilgreina hvað birtist.</span><span class="sxs-lookup"><span data-stu-id="1ec09-125">At the top of the window, fill in the fields as necessary to define what is shown.</span></span>  
4. <span data-ttu-id="1ec09-126">Til að sjá tilgreininguna sem birt upphæð samanstendur af skal velja reitinn.</span><span class="sxs-lookup"><span data-stu-id="1ec09-126">To see a specification that makes up the amount shown, choose the field.</span></span>  

> [!NOTE]  
>   <span data-ttu-id="1ec09-127">Afmarkanir sem settar eru í gluggahausinn verða notaðar í fjárhagsfærslum og áætlunarfærslum.</span><span class="sxs-lookup"><span data-stu-id="1ec09-127">The filters you set in the window header will be applied to general ledger entries and also budget entries.</span></span>

<span data-ttu-id="1ec09-128">Bókhaldslykillinn er í dálkunum til vinstri.</span><span class="sxs-lookup"><span data-stu-id="1ec09-128">The leftmost columns contain the chart of accounts.</span></span> <span data-ttu-id="1ec09-129">Af dálkunum fimm lengst til hægri sýna fjórir þeir fyrstu raunverulegar og áætlaðar debet- og kreditfærslur á hverjum reikningi.</span><span class="sxs-lookup"><span data-stu-id="1ec09-129">Of the five columns on the rightmost side, the first four columns show actual and budgeted debit and credit amounts for each account.</span></span> <span data-ttu-id="1ec09-130">Fimmti dálkurinn sýnir hlutfallsleg tengsl raunverulegra og áætlaðra upphæða á fjárhagsreikningnum.</span><span class="sxs-lookup"><span data-stu-id="1ec09-130">The fifth column shows the proportional relationship between the actual and the budgeted amounts on the general ledger account.</span></span>  

> [!TIP]  
>   <span data-ttu-id="1ec09-131">Reiturinn **Skoða eftir** í glugganum **Fjárhagur - Staða/áætlun** er notaður til að velja lengd tímabils.</span><span class="sxs-lookup"><span data-stu-id="1ec09-131">Use the **View by** field in the **G/L Balance/Budget** window to select the period length.</span></span> <span data-ttu-id="1ec09-132">Smellt er á reitinn  **Skoða sem** til að velja hvernig upphæðir eru reiknaðar (**Hreyfing** eða **Staða til dags**).</span><span class="sxs-lookup"><span data-stu-id="1ec09-132">Use the **View as** field to select the way the amounts will be calculated, **Net Change** or **Balance at Date**.</span></span> <span data-ttu-id="1ec09-133">Veljið aðgerðina **Fyrra tímabil** eða **Næsta tímabil** til að breyta tímabilinu.</span><span class="sxs-lookup"><span data-stu-id="1ec09-133">Choose the **Previous Period** or **Next Period** action to change the period.</span></span>  

## <a name="to-view-actual-and-budgeted-amounts-for-several-periods"></a><span data-ttu-id="1ec09-134">Að skoða raunverulegar og áætlaðar upphæðir fyrir nokkur tímabil</span><span class="sxs-lookup"><span data-stu-id="1ec09-134">To view actual and budgeted amounts for several periods</span></span>  
<span data-ttu-id="1ec09-135">Í stað þess að skoða raunverulegar og áætlaðar upphæðir á öllum reikningum innan ákveðins tímabils er hægt að skoða fjölda tímabila á stökum reikningi.</span><span class="sxs-lookup"><span data-stu-id="1ec09-135">Instead of viewing the actual and budgeted amounts for all accounts within a single period, you can view a number of periods for a single account.</span></span>  

1. <span data-ttu-id="1ec09-136">Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **bókhaldslykill** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="1ec09-136">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Chart of Accounts**, and then choose the related link.</span></span>  
2. <span data-ttu-id="1ec09-137">Í glugganum **Bókhaldslykill** veljið viðeigandi fjárhagsreikning, og veljið síðan aðgerðina **Fjárhagsreikningur staða/áætlun**.</span><span class="sxs-lookup"><span data-stu-id="1ec09-137">In the **Chart of Accounts** window, select the relevant general ledger account, and then choose the **G/L Account Balance/Budget** action.</span></span>  
3. <span data-ttu-id="1ec09-138">Efst í glugganum skal fylla inn í reitina eins og þörf krefur, til að skilgreina hvað birtist.</span><span class="sxs-lookup"><span data-stu-id="1ec09-138">At the top of the window, fill in the fields as necessary to define what is shown.</span></span>   
4. <span data-ttu-id="1ec09-139">Til að sjá tilgreiningu á birtri upphæð skal velja reitinn.</span><span class="sxs-lookup"><span data-stu-id="1ec09-139">To see a specification of an amount shown, choose the field.</span></span>  

## <a name="see-also"></a><span data-ttu-id="1ec09-140">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="1ec09-140">See Also</span></span>
<span data-ttu-id="1ec09-141">[Viðskiptaupplýsingar](bi.md)
[Hvernig skal: Vinna með fjárhagsskemu](bi-how-work-account-schedule.md)</span><span class="sxs-lookup"><span data-stu-id="1ec09-141">[Business Intelligence](bi.md)
[How to: Work with Account Schedules](bi-how-work-account-schedule.md)</span></span>  
[<span data-ttu-id="1ec09-142">Fjármál</span><span class="sxs-lookup"><span data-stu-id="1ec09-142">Finance</span></span>](finance.md)  
[<span data-ttu-id="1ec09-143">Uppsetning Fjármála</span><span class="sxs-lookup"><span data-stu-id="1ec09-143">Setting Up Finance</span></span>](finance-setup-finance.md)  
[<span data-ttu-id="1ec09-144">Fjárhagur og bókhaldslyklar</span><span class="sxs-lookup"><span data-stu-id="1ec09-144">The General Ledger and the Chart of Accounts</span></span>](finance-general-ledger.md)  
<span data-ttu-id="1ec09-145">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="1ec09-145">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

