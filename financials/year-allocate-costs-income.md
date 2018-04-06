---
title: "Yfirlit yfir verkhluta úthlutunar á kostnaði og tekjum | Microsoft Docs"
description: "Útskýrir verkhluta sem felur í sér að úthluta færslu úr færslubók til nokkurra reikninga þegar færslubókin er bókuð."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 06/07/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 3f2a1f762f9380f3cd272e78c4c2f269e9960f38
ms.contentlocale: is-is
ms.lasthandoff: 03/22/2018

---
# <a name="allocate-costs-and-income"></a><span data-ttu-id="76877-103">Úthluta kostnaði og tekjum</span><span class="sxs-lookup"><span data-stu-id="76877-103">Allocate Costs and Income</span></span>
<span data-ttu-id="76877-104">Hægt er að úthluta færslu úr færslubók til nokkurra reikninga þegar færslubókin er bókuð.</span><span class="sxs-lookup"><span data-stu-id="76877-104">You can allocate an entry in a general journal to several different accounts when you post the journal.</span></span> <span data-ttu-id="76877-105">Framkvæma má úthlutunina miðað við þrjú atriði:</span><span class="sxs-lookup"><span data-stu-id="76877-105">The allocation can be made by three different methods:</span></span>

* <span data-ttu-id="76877-106">Magn</span><span class="sxs-lookup"><span data-stu-id="76877-106">Quantity</span></span>
* <span data-ttu-id="76877-107">Prósentuhlutfall (%)</span><span class="sxs-lookup"><span data-stu-id="76877-107">Percentage (%)</span></span>
* <span data-ttu-id="76877-108">Upphæð</span><span class="sxs-lookup"><span data-stu-id="76877-108">Amount</span></span>

<span data-ttu-id="76877-109">Nota má úthlutunareiginleika með ítrekunarfærslubókum og eignabókum.</span><span class="sxs-lookup"><span data-stu-id="76877-109">The allocation features can be used with recurring general journals and in fixed assets journals.</span></span>
<!--You can also distribute the cost or revenue of a line to an intercompany partner when you post a sales or purchase document. When you post the document, a line will be posted in your general journal, and a corresponding line will be created in the intercompany outbox.-->

<span data-ttu-id="76877-110">Eftirfarandi ferli lýsa því hvernig skal búa sig undir það að úthluta kostnaði í ítrekunarfærslubók með því að skilgreina úthlutunarlykla.</span><span class="sxs-lookup"><span data-stu-id="76877-110">The following procedures describe how to prepare to allocate costs in a recurring general journal by defining allocation keys.</span></span> <span data-ttu-id="76877-111">Þegar úthlutunarlyklar eru skilgreindir, er færslubókin kláruð og bókuð eins og hver önnur ítrekunarfærslubók.</span><span class="sxs-lookup"><span data-stu-id="76877-111">When allocation keys are defined, you complete and post the journal like any other recurring general journal.</span></span> <span data-ttu-id="76877-112">Frekari upplýsingar, sjá [Vinna með almennar færslubækur](ui-work-general-journals.md).</span><span class="sxs-lookup"><span data-stu-id="76877-112">For more information, see [Working with General Journals](ui-work-general-journals.md).</span></span>

## <a name="to-set-up-allocation-keys"></a><span data-ttu-id="76877-113">setja upp úthlutunarlykla</span><span class="sxs-lookup"><span data-stu-id="76877-113">To set up allocation keys</span></span>
<span data-ttu-id="76877-114">Hægt er að úthluta færslu úr ítrekunarfærslubók til nokkurra reikninga þegar færslubókin er bókuð.</span><span class="sxs-lookup"><span data-stu-id="76877-114">You can allocate an entry in a recurring general journal to several different accounts when you post the journal.</span></span> <span data-ttu-id="76877-115">Úthlutunin getur verið í magni, prósentu eða upphæð.</span><span class="sxs-lookup"><span data-stu-id="76877-115">The allocation can be made by quantity, percentage, or amount.</span></span>
1. <span data-ttu-id="76877-116">Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Ítrekunarfærslubók** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="76877-116">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Recurring General Journal**, and then choose the related link.</span></span>
2. <span data-ttu-id="76877-117">Veldu **runuheiti** reitinn til að opna **færslubókarkeyrslu** gluggann.</span><span class="sxs-lookup"><span data-stu-id="76877-117">Choose the **Batch Name** field to open the **General Journal Batches** window.</span></span>
3. <span data-ttu-id="76877-118">Þú getur annað hvort breytt úthlutunum á fyrirliggjandi runu í listanum eða stofna nýja runu með úthlutunum.</span><span class="sxs-lookup"><span data-stu-id="76877-118">You can either modify allocations on an existing batch in the list or create a new batch with allocations.</span></span>
   * <span data-ttu-id="76877-119">Til að stofna nýja runu, velja **Nýtt** aðgerð og farið á næsta skref.</span><span class="sxs-lookup"><span data-stu-id="76877-119">To create a new batch, choose the **New** action, and go to the next step.</span></span>
   * <span data-ttu-id="76877-120">Til að breyta úthlutunum fyrir núverandi færslubók, veldu færslubók og farðu í skref 7.</span><span class="sxs-lookup"><span data-stu-id="76877-120">To change the allocations of an existing journal, select the journal and go to step 7.</span></span>    
4. <span data-ttu-id="76877-121">Í reitnum **Heiti** er fært inn heiti fyrir keyrsluna, eins og Þrif.</span><span class="sxs-lookup"><span data-stu-id="76877-121">In the **Name** field, enter a name for the batch, such as CLEANING.</span></span> <span data-ttu-id="76877-122">Í reitnum **Lýsing** færið inn lýsingu, eins og Hreinsa kostnaðarbók.</span><span class="sxs-lookup"><span data-stu-id="76877-122">In the **Description** field, enter a description, such as Cleaning Expenses Journal.</span></span>
5. <span data-ttu-id="76877-123">Lokið glugganum þegar þessu er lokið.</span><span class="sxs-lookup"><span data-stu-id="76877-123">When you are done, close the window.</span></span> <span data-ttu-id="76877-124">Ný, auð ítrekunarbók opnast.</span><span class="sxs-lookup"><span data-stu-id="76877-124">A new, empty recurring journal opens.</span></span>
6. <span data-ttu-id="76877-125">Reitirnir í línunni eru fylltir út.</span><span class="sxs-lookup"><span data-stu-id="76877-125">Fill in the fields on the line.</span></span>
7. <span data-ttu-id="76877-126">Valið er **úthluta** aðgerð.</span><span class="sxs-lookup"><span data-stu-id="76877-126">Choose the **Allocations** action.</span></span>
8. <span data-ttu-id="76877-127">Lína er bætt við fyrir hverja úthlutun.</span><span class="sxs-lookup"><span data-stu-id="76877-127">Add a line for each allocation.</span></span> <span data-ttu-id="76877-128">Annaðhvort þarf að fylla út reitinn **Úthlutun %**, **Úthlutunarmagn** eða **Upphæð**.</span><span class="sxs-lookup"><span data-stu-id="76877-128">You must fill in either the **Allocation %**, **Allocation Quantity**, or **Amount** field.</span></span> <span data-ttu-id="76877-129">Einnig þarf að fylla út reitinn **Reikningsnr.** og í reitina í altækum víddum ef færslan á að fara í altækar víddir.</span><span class="sxs-lookup"><span data-stu-id="76877-129">You must also fill in the **Account No.** field and, if you are allocating the transaction among global dimensions, the global dimension fields.</span></span>
9. <span data-ttu-id="76877-130">Þegar prósenta er færð í línu reiknast upphæðin í reitnum **Upphæð** sjálfkrafa.</span><span class="sxs-lookup"><span data-stu-id="76877-130">If you enter a percentage on a line, the amount in the **Amount** field is calculated automatically.</span></span> <span data-ttu-id="76877-131">Þessar upphæðir verða að hafa andstætt merki við það sem heildarupphæðin í reitnum **Upphæð** er með í ítrekunarbókinni.</span><span class="sxs-lookup"><span data-stu-id="76877-131">These amounts have the opposite sign from the total amount in the **Amount** field in the recurring journal.</span></span>
10. <span data-ttu-id="76877-132">Eftir að hafa fært inn úthlutunarlínurnar skal velja **Í lagi** til að fara aftur í gluggann **endurteknar færslubækur**.</span><span class="sxs-lookup"><span data-stu-id="76877-132">After entering the allocations lines, choose **OK** to return to the **Recurring General Journal** window.</span></span> <span data-ttu-id="76877-133">Svæðið **Úthlutuð upphæð (USD)** er fyllt út og er eins og svæðið **Upphæð**.</span><span class="sxs-lookup"><span data-stu-id="76877-133">The **Allocated Amt. (USD)** field is filled in and matches the **Amount** field.</span></span>
11. <span data-ttu-id="76877-134">Bóka skal færslubókina.</span><span class="sxs-lookup"><span data-stu-id="76877-134">Post the journal.</span></span>

## <a name="to-change-an-allocation-key-that-has-already-been-set-up"></a><span data-ttu-id="76877-135">Breyta uppsettum úthlutunarlykli.</span><span class="sxs-lookup"><span data-stu-id="76877-135">To change an allocation key that has already been set up</span></span>
1. <span data-ttu-id="76877-136">Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Ítrekunarfærslubók** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="76877-136">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Recurring General Journal**, and then choose the related link.</span></span>
2. <span data-ttu-id="76877-137">Í glugganum**Ítrekunarfærslubók** er færslubók með úthlutun valin.</span><span class="sxs-lookup"><span data-stu-id="76877-137">In the **Recurring General Journal** window, select the journal with the allocation.</span></span>
3. <span data-ttu-id="76877-138">Velja línu með úthlutuninni og velja síðan **úthlutanir**.</span><span class="sxs-lookup"><span data-stu-id="76877-138">Choose the line with the allocation, and then choose **Allocations** action.</span></span>
4. <span data-ttu-id="76877-139">Breyta viðeigandi reitum, og velja svo hnappinn **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="76877-139">Change the relevant fields, and then choose the **OK** button.</span></span>

## <a name="see-also"></a><span data-ttu-id="76877-140">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="76877-140">See Also</span></span>
[<span data-ttu-id="76877-141">Lokaár og Tímabil</span><span class="sxs-lookup"><span data-stu-id="76877-141">Closing Years and Periods</span></span>](year-close-years-periods.md)  
<span data-ttu-id="76877-142">[Vinna í færslubókum](ui-work-general-journals.md)  </span><span class="sxs-lookup"><span data-stu-id="76877-142">[Working with General Journals](ui-work-general-journals.md)  </span></span>  
<span data-ttu-id="76877-143">[Að bóka skjöl og færslubækur](ui-post-documents-journals.md)  </span><span class="sxs-lookup"><span data-stu-id="76877-143">[Posting Documents and Journals](ui-post-documents-journals.md)  </span></span>  
<span data-ttu-id="76877-144">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="76877-144">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

