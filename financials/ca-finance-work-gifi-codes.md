---
title: "GIFI kóðar í Kanada| Microsoft Docs"
Description: "Í Kanada er hægt að setja upp kóða fyrir Almenna atriðaskrá um fjárhagsupplýsingar (GIFI) og úthluta þeim til bókunarreikninga."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: local
ms.date: 06/02/2017
ms.author: SorenGP
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: d5211f5c8265e572ff1d1a809b1046ce89f8c1e6
ms.contentlocale: is-is
ms.lasthandoff: 09/11/2017

---
# <a name="how-to-work-with-gifi-codes-in-canada"></a><span data-ttu-id="7d75c-103">Hvernig á að: Vinna með GIFI kóða í Kanada</span><span class="sxs-lookup"><span data-stu-id="7d75c-103">How to: Work With GIFI Codes in Canada</span></span>
<span data-ttu-id="7d75c-104">Fjárhagsupplýsingar geta innihaldið fjárhagsreikninga, skýrslur, rekstrarreikninga, efnahagsreikninga og yfirlit yfir óráðstafað eigið fé.</span><span class="sxs-lookup"><span data-stu-id="7d75c-104">Fiscal information can include general ledger accounts, reports, income statements, balance sheets, and statements of retained earnings.</span></span> <span data-ttu-id="7d75c-105">Fjárhagsupplýsingar eru flokkaðar með kóðum.</span><span class="sxs-lookup"><span data-stu-id="7d75c-105">Fiscal information is classified using codes.</span></span> <span data-ttu-id="7d75c-106">Notkun kóða hjálpar hinu opinbera að vinna upplýsingar, undirbúa rafræn skattskil og staðfesta upplýsingar um skatta rafrænt.</span><span class="sxs-lookup"><span data-stu-id="7d75c-106">The use of codes helps the government to process information, prepare for electronic filing, and validate tax information electronically.</span></span> <span data-ttu-id="7d75c-107">Notkun kóða auðveldar einnig hagstofum og slíkum stofnunum vinnuna, þar sem fjárhagsupplýsingar eru aðgengilegri.</span><span class="sxs-lookup"><span data-stu-id="7d75c-107">The use of codes also helps statistical organizations to work more efficiently, as financial information is more readily available.</span></span> <span data-ttu-id="7d75c-108">Nánari upplýsingar eru á vefsíðu [Tekjuskrifstofu Kanada](http://www.cra-arc.gc.ca/).</span><span class="sxs-lookup"><span data-stu-id="7d75c-108">For more information, see the [Canada Revenue Agency website](http://www.cra-arc.gc.ca/).</span></span>

<span data-ttu-id="7d75c-109">Tekjuskrifstofa Kanada notar kóða úr Almennri atriðaskrá um fjárhagsupplýsingar (General Index of Financial Information, GIFI) til að safna saman, sannprófa, og vinna ársreikninga og vsk-upplýsingar rafrænt.</span><span class="sxs-lookup"><span data-stu-id="7d75c-109">The Canada Revenue Agency uses General Index of Financial Information (GIFI) codes to collect, validate, and process financial and tax information electronically.</span></span> <span data-ttu-id="7d75c-110">Það er best að úthluta GIFI kóðum aðeins á bókunarreikninga, til þess að allar samtölur séu gerðar af hugbúnaðinum sem notaður er fyrir undirbúning vsk-skatts.</span><span class="sxs-lookup"><span data-stu-id="7d75c-110">It is a best practice to assign GIFI codes only to posting accounts, so that all totaling is done by your tax preparation software.</span></span>

<span data-ttu-id="7d75c-111">Þegar reikningur er tengdur GIFI kóða er hann skráður í tekjuskrifstofunni undir þeim kóða.</span><span class="sxs-lookup"><span data-stu-id="7d75c-111">When an account is associated with a GIFI code, it is reported to the revenue agency under that code.</span></span> <span data-ttu-id="7d75c-112">Margir sameinaðir reikningar geta haft sama GIFI kóða, en hver reikningur getur aðeins haft einn GIFI kóða.</span><span class="sxs-lookup"><span data-stu-id="7d75c-112">Multiple accounts can all have the same GIFI code, but each account can have only one GIFI code.</span></span>

<span data-ttu-id="7d75c-113">Hægt er að flytja út upplýsingar um stöðu eftir GIFI kóða og vista útfluttu skrána í Excel, sem er gagnlegt við að flytja upplýsingar til hugbúnaðarins sem notaður er fyrir undirbúning vsk-skatts.</span><span class="sxs-lookup"><span data-stu-id="7d75c-113">You can export balance information by GIFI code and save the exported file in Excel, which is useful for transferring information to your tax preparation software.</span></span>

## <a name="to-set-up-gifi-codes"></a><span data-ttu-id="7d75c-114">Uppsetning GIFI kóða</span><span class="sxs-lookup"><span data-stu-id="7d75c-114">To set up GIFI codes</span></span>
<span data-ttu-id="7d75c-115">Í Dynamics NAV þarf að setja upp GIFI kóða fyrir fjárhagsreikninga, skýrslur, efnahagsreikninga, tekjureikninga og yfirlit yfir óráðstafað eigið fé.</span><span class="sxs-lookup"><span data-stu-id="7d75c-115">In Dynamics NAV, you must set up GIFI codes for general ledger accounts, reports, balance sheets, income sheets, and statements of retained earnings.</span></span>

1. <span data-ttu-id="7d75c-116">Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **GIFI-kóðar** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="7d75c-116">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **GIFI Codes**, and then choose the related link.</span></span>
2. <span data-ttu-id="7d75c-117">Í glugganum **GIFI kóðar** skal velja aðgerðina **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="7d75c-117">In the **GIFI Codes** window, choose the **New** action.</span></span>
3. <span data-ttu-id="7d75c-118">Setjið upp GIFI kóða með því að fylla í reitina.</span><span class="sxs-lookup"><span data-stu-id="7d75c-118">Set up GIFI codes by filling the fields.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-associate-gifi-codes-with-gl-accounts"></a><span data-ttu-id="7d75c-119">Til að tengja GIFI kóða við fjárhagsreikninga</span><span class="sxs-lookup"><span data-stu-id="7d75c-119">To associate GIFI codes with G/L accounts</span></span>
<span data-ttu-id="7d75c-120">Til að tilkynna fjárhagslegar upplýsingar eftir GIFI kóða þarf hver GIFI kóði að vera tengdur við viðeigandi reikninga í bókhaldslyklinum.</span><span class="sxs-lookup"><span data-stu-id="7d75c-120">To report financial information by GIFI code, each GIFI code must be associated with the appropriate accounts in the chart of accounts.</span></span>

1. <span data-ttu-id="7d75c-121">Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **bókhaldslykill** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="7d75c-121">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Chart of Accounts**, and then choose the related link.</span></span>
2. <span data-ttu-id="7d75c-122">Veljið viðeigandi fjárhagsreikning og veljið svo aðgerðina **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="7d75c-122">Select a relevant general ledger account, and then choose the **Edit** action.</span></span>
3. <span data-ttu-id="7d75c-123">Í flýtiflipanum **Kostnaðarbókhald** í svæðinu **GIFI kóði** er viðeigandi GIFI kóði valinn.</span><span class="sxs-lookup"><span data-stu-id="7d75c-123">On the **Cost Accounting** FastTab, in the **GIFI Code** field, select an appropriate GIFI code.</span></span>

## <a name="to-view-account-balances-using-the-gifi-code-report"></a><span data-ttu-id="7d75c-124">Til að skoða reikningsstöður með GIFI kóða skýrslunni.</span><span class="sxs-lookup"><span data-stu-id="7d75c-124">To view account balances using the GIFI code report</span></span>
<span data-ttu-id="7d75c-125">Hægt er að skoða stöðu reikninga eftir GIFI kóða með því að nota skýrsluna **Staða reikninga eftir GIFI kóða**.</span><span class="sxs-lookup"><span data-stu-id="7d75c-125">You can review your account balances by GIFI code by using the **Account Balances by GIFI Code** report.</span></span>

1. <span data-ttu-id="7d75c-126">Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Reikningsstaða eftir GIFI-kóðum** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="7d75c-126">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Account Balances by GIFI Code**, and then choose the related link.</span></span>
2. <span data-ttu-id="7d75c-127">Tilgreina þarf hvað eigi að taka með í skýrslunni með því að fylla í reitina.</span><span class="sxs-lookup"><span data-stu-id="7d75c-127">Specify what to include in the report by filling the fields.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="7d75c-128">Veljið hnappinn **Prenta** eða **Forskoðun**.</span><span class="sxs-lookup"><span data-stu-id="7d75c-128">Choose the **Print** or the **Preview** button.</span></span>

## <a name="to-export-balance-information-using-gifi-codes"></a><span data-ttu-id="7d75c-129">Til að flytja út reikningsupplýsingar með því að nota GIFI kóða</span><span class="sxs-lookup"><span data-stu-id="7d75c-129">To export balance information using GIFI codes</span></span>
<span data-ttu-id="7d75c-130">Hægt er að flytja út reikningsupplýsingar með því að nota GIFI kóða og vista útfluttu skrána í Excel.</span><span class="sxs-lookup"><span data-stu-id="7d75c-130">You can export balance information using GIFI codes and save the exported file in Excel.</span></span> <span data-ttu-id="7d75c-131">Hægt er að breyta, vista eða eyða skrám.</span><span class="sxs-lookup"><span data-stu-id="7d75c-131">You can modify, save, or delete the file.</span></span> <span data-ttu-id="7d75c-132">Skrána má nota til að flytja upplýsingar til hugbúnaðarins sem notaður er fyrir undirbúning vsk-skatts.</span><span class="sxs-lookup"><span data-stu-id="7d75c-132">You can use the file to transfer information to your tax preparation software.</span></span>

1. <span data-ttu-id="7d75c-133">Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Flytja GIFI upplýsingar í Excel** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="7d75c-133">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Export GIFI Info. to Excel**, and then choose the related link.</span></span>
2. <span data-ttu-id="7d75c-134">Skilgreina þarf hvað eigi að flytja út í Excel með því að fylla í reitina.</span><span class="sxs-lookup"><span data-stu-id="7d75c-134">Specify what to export to Excel by filling the fields.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="7d75c-135">Velja hnappinn **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="7d75c-135">Choose the **OK** button.</span></span>

> [!NOTE]  
>   <span data-ttu-id="7d75c-136">Excel-skráin hefur eftirfarandi eiginleika:</span><span class="sxs-lookup"><span data-stu-id="7d75c-136">The Excel file has the following characteristics:</span></span>

* <span data-ttu-id="7d75c-137">Staðan er sléttuð í næstu prósentu en gildi reitsins viðheldur sömu prósentu og í fjárhag.</span><span class="sxs-lookup"><span data-stu-id="7d75c-137">The balance is rounded to the nearest percentage, but the cell value maintains the same percentage as it does in the general ledger.</span></span>
* <span data-ttu-id="7d75c-138">Neikvæð númer eru sýnd sem jákvæð númer í svigum.</span><span class="sxs-lookup"><span data-stu-id="7d75c-138">Negative numbers are represented as positive number in brackets.</span></span> <span data-ttu-id="7d75c-139">Í samræmi við það er talan -123 sýnd sem (123).</span><span class="sxs-lookup"><span data-stu-id="7d75c-139">Accordingly, -123 is represented as (123).</span></span>

## <a name="see-also"></a><span data-ttu-id="7d75c-140">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="7d75c-140">See Also</span></span>
<span data-ttu-id="7d75c-141">[Fjármál](finance.md) </span><span class="sxs-lookup"><span data-stu-id="7d75c-141">[Finance](finance.md) </span></span>  
[<span data-ttu-id="7d75c-142">Uppsetning Fjármála</span><span class="sxs-lookup"><span data-stu-id="7d75c-142">Setting Up Finance</span></span>](finance-setup-finance.md)

