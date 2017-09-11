---
title: "Valfrjálsar aðgerðir fyrir lokun tímabila | Microsoft Docs"
description: "Þetta efnisatriði útskýrir valfrjáls ferli og aðgerðir fyrir lokun fjárhagstímabila í Financials."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: year closing, close accounting period, close fiscal year, aging, creditor payments, vendor payments
ms.date: 06/02/2017
ms.author: jswymer
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 678cebc065594ed0ed6fea897676f109ff2c1dce
ms.contentlocale: is-is
ms.lasthandoff: 07/07/2017


---
# <a name="overview-of-tasks-to-close-accounting-periods"></a><span data-ttu-id="11dfb-103">Yfirlit yfir verkhluta sem felur í sér lokun fjárhagstímabila</span><span class="sxs-lookup"><span data-stu-id="11dfb-103">Overview of Tasks to Close Accounting Periods</span></span>
[!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="11dfb-104"> þvingar þig ekki til að loka tímabilum, en það eru margar aðgerðir í lokunartíma (lok mánaðar) sem þú getur gert.</span><span class="sxs-lookup"><span data-stu-id="11dfb-104"> does not force you to close periods, however, there are many period-end (month-end) activities that you can do.</span></span> <span data-ttu-id="11dfb-105">Þetta efni gefur yfirlit yfir valfrjáls ferli og starfsemi fyrir lokunartímabil.</span><span class="sxs-lookup"><span data-stu-id="11dfb-105">This topic provides an overview of optional processes and activities for closing periods.</span></span>  

## <a name="general-ledger"></a><span data-ttu-id="11dfb-106">Fjárhagur</span><span class="sxs-lookup"><span data-stu-id="11dfb-106">General Ledger</span></span>
* <span data-ttu-id="11dfb-107">Tilgreindu kerfisbundið og notendasértækt bókunartímabil.</span><span class="sxs-lookup"><span data-stu-id="11dfb-107">Specify system-wide and user-specific posting periods.</span></span>  

    <span data-ttu-id="11dfb-108">Þetta tilgreinir dagsetningar þar sem hægt er að bóka.</span><span class="sxs-lookup"><span data-stu-id="11dfb-108">This specifies the dates between which you allow posting.</span></span> <span data-ttu-id="11dfb-109">Þú gætir viljað leyfa bókun í byrjun tímabilsins eða í lok tímabilsins, allt eftir fyrirtækinu.</span><span class="sxs-lookup"><span data-stu-id="11dfb-109">Depending on your business, you may want to allow posting at the start of the period, or toward the end.</span></span> <span data-ttu-id="11dfb-110">Nánari upplýsingar eru í [Hvernig á að tilgreina bókunartímabil](finance-how-specify-posting-periods.md).</span><span class="sxs-lookup"><span data-stu-id="11dfb-110">For more information, see [How to: Specify Posting Periods](finance-how-specify-posting-periods.md).</span></span>  
* <span data-ttu-id="11dfb-111">Allar nauðsynlegar fjárhagsleiðréttingar eru framkvæmdar.</span><span class="sxs-lookup"><span data-stu-id="11dfb-111">Make all necessary G/L adjustments.</span></span>  
* <span data-ttu-id="11dfb-112">Ítrekunarbækur eru uppfærðar og bókaðar.</span><span class="sxs-lookup"><span data-stu-id="11dfb-112">Update and post Recurring Journals.</span></span>  
  <!--* Process Consolidations-->
* <span data-ttu-id="11dfb-113">Fjárhagsskema keyrt sem hér segir:</span><span class="sxs-lookup"><span data-stu-id="11dfb-113">Run account schedules as follows:</span></span>  
  * <span data-ttu-id="11dfb-114">Glugginn **Fjárhagsskema** er opnaður og smellt á aðgerðina **Prenta**.</span><span class="sxs-lookup"><span data-stu-id="11dfb-114">Open the **Account Schedule** window, and then choose the **Print** action.</span></span>  

## <a name="sales-and-receivables"></a><span data-ttu-id="11dfb-115">Sala and útistandandi</span><span class="sxs-lookup"><span data-stu-id="11dfb-115">Sales and Receivables</span></span>
* <span data-ttu-id="11dfb-116">Allar sölupantanir, reikningar, kreditreikningar og vöruskilapantanir eru bókaðar.</span><span class="sxs-lookup"><span data-stu-id="11dfb-116">Post all sales orders, invoices, credit memos, and return orders.</span></span>  
* <span data-ttu-id="11dfb-117">Inngreiðslubókin er bókuð.</span><span class="sxs-lookup"><span data-stu-id="11dfb-117">Post all cash receipt journals.</span></span>  
* <span data-ttu-id="11dfb-118">Uppfæra og birta bækur tímarit sem tengjast sölu og útistandandi.</span><span class="sxs-lookup"><span data-stu-id="11dfb-118">Update and post recurring journals that are related to sales and receivables.</span></span>  
* <span data-ttu-id="11dfb-119">Afstemma viðskiptakröfur við færslubók.</span><span class="sxs-lookup"><span data-stu-id="11dfb-119">Reconcile accounts receivable to the general ledger.</span></span>  
* <span data-ttu-id="11dfb-120">Runuvinnslan **Eyða reikningsf. sölupöntunum** er keyrð.</span><span class="sxs-lookup"><span data-stu-id="11dfb-120">Run the **Delete Invoiced Sales Orders** batch job.</span></span>  

## <a name="purchases-and-payables"></a><span data-ttu-id="11dfb-121">Innkaup og viðskiptaskuldir</span><span class="sxs-lookup"><span data-stu-id="11dfb-121">Purchases and Payables</span></span>
* <span data-ttu-id="11dfb-122">Allar pantanir, reikningar, kreditreikningar og vöruskilapantanir eru bókaðar.</span><span class="sxs-lookup"><span data-stu-id="11dfb-122">Post all purchase orders, invoices, credit memos, and return orders.</span></span>  
* <span data-ttu-id="11dfb-123">Allar greiðslubækur eru bókaðar.</span><span class="sxs-lookup"><span data-stu-id="11dfb-123">Post all payment journals.</span></span>  
* <span data-ttu-id="11dfb-124">Ítrekunarfærslubækur tengdar innkaupum og viðskiptaskuldum eru uppfærðar og bókaðar.</span><span class="sxs-lookup"><span data-stu-id="11dfb-124">Update and post recurring journals that are related to purchases & payables.</span></span>  
* <span data-ttu-id="11dfb-125">Skýrslan **Aldursgreindar skuldir** er keyrð og skuldir stemmdar af við fjárhaginn.</span><span class="sxs-lookup"><span data-stu-id="11dfb-125">Run the **Aged Accounts Payable** report and reconcile accounts payable to the general ledger.</span></span>  
* <span data-ttu-id="11dfb-126">Runuvinnslan **Eyða reikningsf. innk.pöntunum** er keyrð.</span><span class="sxs-lookup"><span data-stu-id="11dfb-126">Run the **Delete Invoiced Purchase Orders** batch job.</span></span>  

<!-- ### Fixed Assets
* Post all maintenance costs have been posted through the fixed asset journals or invoices.
* Post adjustments.
* Post appreciation.
* Post depreciation.
* Update and post the recurring fixed asset journal.-->

<!--### Intercompany
* Process Intercompany Postings.-->

## <a name="calculate-and-process-sales-tax"></a><span data-ttu-id="11dfb-127">VSK er reiknaður og unninn</span><span class="sxs-lookup"><span data-stu-id="11dfb-127">Calculate and Process Sales Tax</span></span>
* <span data-ttu-id="11dfb-128">Lokið er við skattyfirlit.</span><span class="sxs-lookup"><span data-stu-id="11dfb-128">Complete Tax Statements.</span></span>  

## <a name="see-also"></a><span data-ttu-id="11dfb-129">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="11dfb-129">See Also</span></span>
[<span data-ttu-id="11dfb-130">Lokaár og Tímabil</span><span class="sxs-lookup"><span data-stu-id="11dfb-130">Closing Years and Periods</span></span>](year-close-years-periods.md)  
[<span data-ttu-id="11dfb-131">Bókum lokað</span><span class="sxs-lookup"><span data-stu-id="11dfb-131">Closing Books</span></span>](year-close-books.md)  
<span data-ttu-id="11dfb-132">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="11dfb-132">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

