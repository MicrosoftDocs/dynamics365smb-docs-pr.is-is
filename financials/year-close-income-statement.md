---
title: Loka rekstrarreikningum | Microsoft Docs
description: "Við lok árs, er nauðsynlegt að keyra runuvinnsluna Loka rekstrarreikningi til að loka reikningstímabilunum sem mynda fjárhagsárið."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: year closing, close accounting period, close fiscal year, bank account detailed trial balance
ms.date: 06/02/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 237c03e2ba6408bde65aba5f652468a3b700fa0a
ms.contentlocale: is-is
ms.lasthandoff: 03/22/2018

---
# <a name="close-income-statement-accounts"></a><span data-ttu-id="f5e71-103">Loka rekstrarreikningi</span><span class="sxs-lookup"><span data-stu-id="f5e71-103">Close Income Statement Accounts</span></span>
<span data-ttu-id="f5e71-104">Þegar reikningsári er lokið þarf að loka tímabilunum sem það skiptist í.</span><span class="sxs-lookup"><span data-stu-id="f5e71-104">When a fiscal year is over, you must close the periods that comprise it.</span></span> <span data-ttu-id="f5e71-105">Til að gera þetta skal keyra Runuvinnslan **Loka rekstrarreikningi**</span><span class="sxs-lookup"><span data-stu-id="f5e71-105">To do this, you run the **Close Income Statement** batch job.</span></span> <span data-ttu-id="f5e71-106">Þetta verk flytur niðurstöðutölur ársins yfir á efnahagsreikning og loka rekstrarreikningum.</span><span class="sxs-lookup"><span data-stu-id="f5e71-106">This job transfers the year's result to an account in the balance sheet and closes the income statement accounts.</span></span> <span data-ttu-id="f5e71-107">Það er gert með því að stofna línur í færslubók sem síðan er hægt að bóka.</span><span class="sxs-lookup"><span data-stu-id="f5e71-107">You do this by creating lines in a journal, which you then can post.</span></span>

## <a name="to-run-the-close-income-statement-batch-job"></a><span data-ttu-id="f5e71-108">Til að keyra Runuvinnslan Loka rekstrarreikningi</span><span class="sxs-lookup"><span data-stu-id="f5e71-108">To run the Close Income Statement batch job</span></span>
1. <span data-ttu-id="f5e71-109">Loka reikningsári</span><span class="sxs-lookup"><span data-stu-id="f5e71-109">Close the fiscal year.</span></span> <span data-ttu-id="f5e71-110">Reikningsárinu þarf að loka áður en hægt er að setja keyrsluna í gang.</span><span class="sxs-lookup"><span data-stu-id="f5e71-110">The fiscal year must closed before the batch job can be run.</span></span> <span data-ttu-id="f5e71-111">Nánari upplýsingar sjá [Loka fjárhagstímabilum](year-close-account-periods.md).</span><span class="sxs-lookup"><span data-stu-id="f5e71-111">For more information, see [Close Accounting Periods](year-close-account-periods.md).</span></span>
2. <span data-ttu-id="f5e71-112">Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Loka rekstrarreikningi** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="f5e71-112">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Close Income Statement**, and then choose the related link.</span></span>
3. <span data-ttu-id="f5e71-113">Veldu hnappinn **Í lagi** til að ræsa keyrsluna.</span><span class="sxs-lookup"><span data-stu-id="f5e71-113">Choose the **OK** button to run the batch job.</span></span>

## <a name="about-the-close-income-statement-batch-job"></a><span data-ttu-id="f5e71-114">Um Runuvinnslan Loka rekstrarreikningi</span><span class="sxs-lookup"><span data-stu-id="f5e71-114">About the Close Income Statement Batch Job</span></span>
<span data-ttu-id="f5e71-115">Keyrslan vinnur úr öllum fjárhagsreikningum af gerðinni rekstrarreikningar og býr til færslur sem jafna út stöðu þeirra.</span><span class="sxs-lookup"><span data-stu-id="f5e71-115">The batch job processes all general accounts of the income statement type and creates entries that cancel out their respective balances.</span></span> <span data-ttu-id="f5e71-116">Þ.e. hver færsla er samtala allra almennra fjárhagsfærslna á reikningnum á reikningsárinu.</span><span class="sxs-lookup"><span data-stu-id="f5e71-116">That is, each entry is the sum of all the general ledger entries on the account in the fiscal year.</span></span> <span data-ttu-id="f5e71-117">Þessar nýju færslur eru færðar inn í færslubók þar sem þarf að tilgreina mótreikning og framlegðarreikning í efnahagsreikningi áður en bókað er.</span><span class="sxs-lookup"><span data-stu-id="f5e71-117">These new entries are placed in a journal in which you must specify a balancing account and retained earnings account in the balance sheet before you post.</span></span> <span data-ttu-id="f5e71-118">Þegar færslubók er bókuð er færsla bókuð á alla rekstrarreikninga til að staðan verði núll og um leið er útkoma ársins færð á efnahagsreikning.</span><span class="sxs-lookup"><span data-stu-id="f5e71-118">When you post the journal, an entry is posted to each income statement account so that its balance becomes zero and at the same time the year's result is transferred to the balance sheet.</span></span>

<span data-ttu-id="f5e71-119">Notandi þarf að bóka þarf bókina sjálfur.</span><span class="sxs-lookup"><span data-stu-id="f5e71-119">You must post the journal yourself.</span></span> <span data-ttu-id="f5e71-120">Keyrslan bókar færslurnar ekki sjálfkrafa, nema þegar annar skýrslugjaldmiðill er notaður.</span><span class="sxs-lookup"><span data-stu-id="f5e71-120">The batch job does not post the entries automatically, except when an additional reporting currency is being used.</span></span> <span data-ttu-id="f5e71-121">Þegar annar skýrslugjaldmiðill er notaður, bókar keyrslan beint í færslubókina.</span><span class="sxs-lookup"><span data-stu-id="f5e71-121">When an additional reporting currency is being used, the batch job posts entries directly to the general ledger.</span></span>

<span data-ttu-id="f5e71-122">Dagsetningin í línunum sem bætast í færslubókina í keyrslunni verður alltaf lokadagsetning reikningsársins.</span><span class="sxs-lookup"><span data-stu-id="f5e71-122">The date on the lines that the batch job inserts in the journal is always a closing date for the fiscal year.</span></span> <span data-ttu-id="f5e71-123">Lokadagsetningin er hugsuð dagsetning milli síðustu dagsetningar reikningsársins og fyrstu dagsetningar á nýju ári.</span><span class="sxs-lookup"><span data-stu-id="f5e71-123">The closing date is a fictitious date between the last day of the old fiscal year and the first day of the new year.</span></span> <span data-ttu-id="f5e71-124">Kosturinn við að bóka á lokadagsetningu er sá að þá helst rétt staða fyrir venjulegar dagsetningar reikningsársins.</span><span class="sxs-lookup"><span data-stu-id="f5e71-124">The advantage of posting on a closing date is that you maintain the correct balances for the ordinary dates of the fiscal year.</span></span>

<span data-ttu-id="f5e71-125">Keyrsluna **Loka rekstrareikningi** má nota mörgum sinnum.</span><span class="sxs-lookup"><span data-stu-id="f5e71-125">The **Close Income Statement** batch job can be used several times.</span></span> <span data-ttu-id="f5e71-126">Hægt er að bóka á fyrra reikningsár jafnvel eftir lokun rekstrarreiknings ef keyrslan er keyrð aftur.</span><span class="sxs-lookup"><span data-stu-id="f5e71-126">You can post in a previous fiscal year, even after the income statement accounts have been closed, if you run the batch job again.</span></span>

## <a name="see-also"></a><span data-ttu-id="f5e71-127">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="f5e71-127">See Also</span></span>
[<span data-ttu-id="f5e71-128">Bókum lokað</span><span class="sxs-lookup"><span data-stu-id="f5e71-128">Closing Books</span></span>](year-close-books.md)  
[<span data-ttu-id="f5e71-129">Bóka lokafærslu ársloka</span><span class="sxs-lookup"><span data-stu-id="f5e71-129">Post the Year-End Closing Entry</span></span>](year-how-post-year-end-close-entry.md)  
[<span data-ttu-id="f5e71-130">Opna nýtt reikningsár</span><span class="sxs-lookup"><span data-stu-id="f5e71-130">Open a New Fiscal Year</span></span>](finance-how-open-new-fiscal-year.md)  
<span data-ttu-id="f5e71-131">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="f5e71-131">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

