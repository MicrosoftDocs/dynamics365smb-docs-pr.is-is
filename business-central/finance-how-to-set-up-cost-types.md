---
title: Hvernig á að setja upp myndrit yfir kostnaðartegundir | Microsoft Docs
description: Myndrit kostnaðartegunda eru svipuð bókhaldslyklum í fjárhag.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: cost types, general ledger, accounts
ms.date: 04/01/2019
ms.author: sgroespe
redirect_url: finance-set-up-cost-accounting
ms.openlocfilehash: e0bf6a8c7595155785949ed51c765fef0524173b
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2019
ms.locfileid: "922113"
---
# <a name="set-up-cost-types"></a><span data-ttu-id="94694-103">Uppsetning kostnaðargerða</span><span class="sxs-lookup"><span data-stu-id="94694-103">Set Up Cost Types</span></span>
<span data-ttu-id="94694-104">Myndrit kostnaðartegunda eru svipuð bókhaldslyklum í fjárhag.</span><span class="sxs-lookup"><span data-stu-id="94694-104">The chart of cost types is similar to the chart of accounts in the general ledger.</span></span> <span data-ttu-id="94694-105">Hægt er að setja upp myndritið yfir kostnaðartegundir á eftirfarandi hátt:</span><span class="sxs-lookup"><span data-stu-id="94694-105">You can set up the chart of cost types in the following ways:</span></span>  

-   <span data-ttu-id="94694-106">Skipulag kostnaðargerða milli fyrirtækja svipað og á reikningum rekstrarreiknings á fjárhagsbókhaldslyklinum.</span><span class="sxs-lookup"><span data-stu-id="94694-106">Structure the chart of cost types similar to the income statement accounts in the general ledger chart of accounts.</span></span> <span data-ttu-id="94694-107">Síðan er hægt að flytja bókhaldslykil fjárhags yfir í kostnaðargerðir.</span><span class="sxs-lookup"><span data-stu-id="94694-107">Then, you can transfer the general ledger chart of accounts to the chart of cost types.</span></span> <span data-ttu-id="94694-108">Hægt er að gera allar nauðsynlegar leiðréttingar eftir flutninginn.</span><span class="sxs-lookup"><span data-stu-id="94694-108">You can make any necessary adjustments after the transfer.</span></span>  
-   <span data-ttu-id="94694-109">Stofna nýja kostnaðartegund eða bæta nýjum kostnaðartegundum við fyrirliggjandi kostnaðartegund.</span><span class="sxs-lookup"><span data-stu-id="94694-109">Create new chart of cost types or add new cost types to existing chart of cost types.</span></span> <span data-ttu-id="94694-110">Stofna þarf hverja nýja kostnaðartegund sérstaklega.</span><span class="sxs-lookup"><span data-stu-id="94694-110">You must create each new cost type individually.</span></span>  

## <a name="to-transfer-the-general-ledger-chart-of-accounts-to-the-chart-of-cost-types"></a><span data-ttu-id="94694-111">Til að flytja bókhaldslykil fjárhags yfir í kostnaðargerðir.</span><span class="sxs-lookup"><span data-stu-id="94694-111">To transfer the general ledger chart of accounts to the chart of cost types</span></span>  
1.  <span data-ttu-id="94694-112">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Myndrit yfir kostnaðargerðir** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="94694-112">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Chart of Cost Types**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="94694-113">Velja skal aðgerðina **Sækja kostnaðargerðir úr bókhaldslykli**.</span><span class="sxs-lookup"><span data-stu-id="94694-113">Choose the **Get Cost Types from Chart of Accounts** action.</span></span> <span data-ttu-id="94694-114">Í svarglugganum er valið hnappinn **Já** til að staðfesta flutninginn.</span><span class="sxs-lookup"><span data-stu-id="94694-114">In the dialog box, choose the **Yes** button to confirm the transfer.</span></span> <span data-ttu-id="94694-115">Aðgerðin notar bókhaldslykla til að stofna myndrit af kostnaðartegundum.</span><span class="sxs-lookup"><span data-stu-id="94694-115">The function uses the chart of accounts to create a chart of cost types.</span></span>  

    <span data-ttu-id="94694-116">Myndrit kostnaðargerða inniheldur nú alla rekstrarreikninga í fjárhag og inniheldur fyrirsagnir og samtölur.</span><span class="sxs-lookup"><span data-stu-id="94694-116">The chart of cost types now contain all income statement accounts in the general ledger and include headings and subtotals.</span></span> <span data-ttu-id="94694-117">Hægt er að breyta myndriti yfir kostnaðartegundir, eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="94694-117">You can change the chart of cost types, as necessary.</span></span> <span data-ttu-id="94694-118">Til dæmis er hægt að eyða tvíteknum fyrirliggjandi kostnaðartegundum.</span><span class="sxs-lookup"><span data-stu-id="94694-118">For example, you can delete duplicate existing cost types.</span></span>  

    > [!IMPORTANT]  
    >  <span data-ttu-id="94694-119">Aðgerðin **Skrá kostnaðargerðir í bókhaldslyklinum** uppfærir samband milli bókhaldslykils og bókhaldslykils fyrir kostnaðartegundir.</span><span class="sxs-lookup"><span data-stu-id="94694-119">The **Register Cost Types in Chart of Accounts** function updates the relationship between the chart of accounts and the chart of cost types.</span></span> <span data-ttu-id="94694-120">**númer**</span><span class="sxs-lookup"><span data-stu-id="94694-120">The **No.**</span></span> <span data-ttu-id="94694-121"> svæðið er fyllt og staðfest til að tryggja að hver almennur fjárhagsreikningur tengist aðeins einni tegund kostnaðar.</span><span class="sxs-lookup"><span data-stu-id="94694-121">field is filled and verified to make sure that each general ledger account is related to only one cost type.</span></span> <span data-ttu-id="94694-122">Aðgerðin keyrir sjálfkrafa áður en fjárhagsfærslur eru færðar í kostnaðarbókhald.</span><span class="sxs-lookup"><span data-stu-id="94694-122">The function runs automatically before transferring general ledger entries to cost accounting.</span></span>  

## <a name="to-set-up-new-cost-types-in-the-chart-of-cost-types-page"></a><span data-ttu-id="94694-123">Til að setja upp nýjar kostnaðargerðir á síðunni Myndrit fyrir kostnaðargerðir</span><span class="sxs-lookup"><span data-stu-id="94694-123">To set up new cost types in the Chart of Cost Types page</span></span>  
1.  <span data-ttu-id="94694-124">Opnaðu síðuna **Myndrit yfir kostnaðargerðir** í breytingarstillingu.</span><span class="sxs-lookup"><span data-stu-id="94694-124">Open the **Chart of Cost Types** page in edit mode.</span></span>  
2.  <span data-ttu-id="94694-125">Fyllið inn í reitina eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="94694-125">Fill in the fields as described as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
    >  <span data-ttu-id="94694-126">Hægt er að setja upp og viðhalda kostnaðargerðum á síðunni **Kostnaðargerð spjald** eða á síðunni **Myndrit yfir kostnaðargerðir**.</span><span class="sxs-lookup"><span data-stu-id="94694-126">You can set up and maintain cost types in either the **Cost Type Card** page or on the **Chart of Cost Types** page.</span></span> <span data-ttu-id="94694-127">Í þessu ferli eru settar upp kostnaðartegundir á síðunni **Myndrit yfir kostnaðargerðir**.</span><span class="sxs-lookup"><span data-stu-id="94694-127">In this procedure, you set up cost types on the **Chart of Cost Types** page.</span></span>

3.  <span data-ttu-id="94694-128">Þegar búið er að stofna öll kostnaðargerðir, skal velja aðgerðina **Draga inn kostnaðargerðir**.</span><span class="sxs-lookup"><span data-stu-id="94694-128">After you have created all cost types, choose the **Indent Cost Types** action.</span></span> <span data-ttu-id="94694-129">Í svarglugganum, veljið hnappinn **Já**.</span><span class="sxs-lookup"><span data-stu-id="94694-129">In the dialog box, choose the **Yes** button.</span></span>  
4.  <span data-ttu-id="94694-130">Tengja nýju tegund kostnaðar í samsvarandi almennan fjárhagslykil.</span><span class="sxs-lookup"><span data-stu-id="94694-130">Link the new cost type to the corresponding general ledger account.</span></span>  

    > [!IMPORTANT]  
    >  <span data-ttu-id="94694-131">Ef skilgreiningar hafa verið færðar í **Samtala** reitina fyrir línutegundina **Loka-upphæð** áður en aðgerðin **Inndráttur kostnaðargerða** er framkvæmd þarf að færa skilgreiningarnar inn aftur því að aðgerðin skrifar yfir gildin í öllum **Loka-Upphæð**-reitum.</span><span class="sxs-lookup"><span data-stu-id="94694-131">If you have entered definitions in the **Totaling** fields for the line type of **End-Total** before you run the **Indent Cost Types** function, then you must enter the definitions again because the function overwrites the values in all **End-Total** fields.</span></span>  

## <a name="to-update-cost-types"></a><span data-ttu-id="94694-132">Til að uppfæra kostnaðargerðir</span><span class="sxs-lookup"><span data-stu-id="94694-132">To update cost types</span></span>  
1.  <span data-ttu-id="94694-133">Á síðunni **Uppsetning kostnaðarbókhalds** skal velja hvort uppfæra eigi myndrit yfir kostnaðartegundir sjálfkrafa þegar bókhaldslykillinn breytist.</span><span class="sxs-lookup"><span data-stu-id="94694-133">On the **Cost Accounting Setup** page, select if you want the chart of cost types to be automatically updated when the chart of accounts is changed.</span></span>  
2.  <span data-ttu-id="94694-134">Í reitnum **Stilla fjárhagsreikning** er hægt að velja úr eftirfarandi valkostum.</span><span class="sxs-lookup"><span data-stu-id="94694-134">In the **Align G/L Account** field, you can choose from the following options.</span></span>  

- <span data-ttu-id="94694-135">**Engin jöfnun** - Það er engin samsvarandi breyting á kostnaðartegundum þegar bókhaldslyklinum er breytt.</span><span class="sxs-lookup"><span data-stu-id="94694-135">**No Alignment** - There is no corresponding change in the chart of cost types when you change the chart of accounts.</span></span>  
- <span data-ttu-id="94694-136">**Sjálfvirkt** - Samsvarandi breyting er gerð á kostnaðartegundalyklinum þegar bókhaldslyklinum er breytt.</span><span class="sxs-lookup"><span data-stu-id="94694-136">**Automatic** - A corresponding change is made in the chart of cost types when you change the chart of accounts.</span></span>  
- <span data-ttu-id="94694-137">**Kvaðning** - Skilaboð birtast þar sem spurt er hvort gera eigi samsvarandi breytingu á myndriti kostnaðartegunda þegar bókhaldslykli er breytt.</span><span class="sxs-lookup"><span data-stu-id="94694-137">**Prompt** - A message is displayed asking if you want to make a corresponding change in the chart of cost types when you change the chart of accounts.</span></span>  

## <a name="see-also"></a><span data-ttu-id="94694-138">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="94694-138">See Also</span></span>  
[<span data-ttu-id="94694-139">Kostnaðarreikningur</span><span class="sxs-lookup"><span data-stu-id="94694-139">Accounting for Costs</span></span>](finance-manage-cost-accounting.md)  
<span data-ttu-id="94694-140">[Skilgreining kostnaðarstaði og kostnaðarhluti fyrir bókhaldslykil](finance-defining-cost-centers-and-cost-objects-for-chart-of-accounts.md) </span><span class="sxs-lookup"><span data-stu-id="94694-140">[Defining Cost Centers and Cost Objects for Chart of Accounts](finance-defining-cost-centers-and-cost-objects-for-chart-of-accounts.md) </span></span>  
<span data-ttu-id="94694-141">[Stöður milli kostnaðartegundar, kostnaðarstaðar og kostnaðarliðar](finance-balances-between-cost-type-cost-center-and-cost-object.md) </span><span class="sxs-lookup"><span data-stu-id="94694-141">[Balances Between Cost Type, Cost Center, and Cost Object](finance-balances-between-cost-type-cost-center-and-cost-object.md) </span></span>  
<span data-ttu-id="94694-142">[Uppsetning kostnaðarbókhalds](finance-set-up-cost-accounting.md) </span><span class="sxs-lookup"><span data-stu-id="94694-142">[Setting Up Cost Accounting](finance-set-up-cost-accounting.md) </span></span>  
<span data-ttu-id="94694-143">[Orðalisti í kostnaðarbókhaldi](finance-terminology-in-cost-accounting.md) </span><span class="sxs-lookup"><span data-stu-id="94694-143">[Terminology in Cost Accounting](finance-terminology-in-cost-accounting.md) </span></span>  
[<span data-ttu-id="94694-144">Um kostnaðarbókhald</span><span class="sxs-lookup"><span data-stu-id="94694-144">About Cost Accounting</span></span>](finance-about-cost-accounting.md)  
<span data-ttu-id="94694-145">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="94694-145">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
