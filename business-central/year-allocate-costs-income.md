---
title: Yfirlit yfir verkhluta úthlutunar á kostnaði og tekjum | Microsoft Docs
description: Útskýrir verkhluta sem felur í sér að úthluta færslu úr færslubók til nokkurra reikninga þegar færslubókin er bókuð.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: 0c761db3f76d1fff05dd75a08a586f52386b5b88
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/08/2019
ms.locfileid: "799959"
---
# <a name="allocate-costs-and-income"></a><span data-ttu-id="acfa1-103">Úthluta kostnaði og tekjum</span><span class="sxs-lookup"><span data-stu-id="acfa1-103">Allocate Costs and Income</span></span>
<span data-ttu-id="acfa1-104">Hægt er að úthluta færslu úr færslubók til nokkurra reikninga þegar færslubókin er bókuð.</span><span class="sxs-lookup"><span data-stu-id="acfa1-104">You can allocate an entry in a general journal to several different accounts when you post the journal.</span></span> <span data-ttu-id="acfa1-105">Framkvæma má úthlutunina miðað við þrjú atriði:</span><span class="sxs-lookup"><span data-stu-id="acfa1-105">The allocation can be made by three different methods:</span></span>

* <span data-ttu-id="acfa1-106">Magn</span><span class="sxs-lookup"><span data-stu-id="acfa1-106">Quantity</span></span>
* <span data-ttu-id="acfa1-107">Prósentuhlutfall (%)</span><span class="sxs-lookup"><span data-stu-id="acfa1-107">Percentage (%)</span></span>
* <span data-ttu-id="acfa1-108">Upphæð</span><span class="sxs-lookup"><span data-stu-id="acfa1-108">Amount</span></span>

<span data-ttu-id="acfa1-109">Nota má úthlutunareiginleika með ítrekunarfærslubókum og eignabókum.</span><span class="sxs-lookup"><span data-stu-id="acfa1-109">The allocation features can be used with recurring general journals and in fixed assets journals.</span></span>
<!--You can also distribute the cost or revenue of a line to an intercompany partner when you post a sales or purchase document. When you post the document, a line will be posted in your general journal, and a corresponding line will be created in the intercompany outbox.-->

<span data-ttu-id="acfa1-110">Eftirfarandi ferli lýsa því hvernig skal búa sig undir það að úthluta kostnaði í ítrekunarfærslubók með því að skilgreina úthlutunarlykla.</span><span class="sxs-lookup"><span data-stu-id="acfa1-110">The following procedures describe how to prepare to allocate costs in a recurring general journal by defining allocation keys.</span></span> <span data-ttu-id="acfa1-111">Þegar úthlutunarlyklar eru skilgreindir, er færslubókin kláruð og bókuð eins og hver önnur ítrekunarfærslubók.</span><span class="sxs-lookup"><span data-stu-id="acfa1-111">When allocation keys are defined, you complete and post the journal like any other recurring general journal.</span></span> <span data-ttu-id="acfa1-112">Frekari upplýsingar, sjá [Vinna með almennar færslubækur](ui-work-general-journals.md).</span><span class="sxs-lookup"><span data-stu-id="acfa1-112">For more information, see [Working with General Journals](ui-work-general-journals.md).</span></span>

## <a name="to-set-up-allocation-keys"></a><span data-ttu-id="acfa1-113">setja upp úthlutunarlykla</span><span class="sxs-lookup"><span data-stu-id="acfa1-113">To set up allocation keys</span></span>
<span data-ttu-id="acfa1-114">Hægt er að úthluta færslu úr ítrekunarfærslubók til nokkurra reikninga þegar færslubókin er bókuð.</span><span class="sxs-lookup"><span data-stu-id="acfa1-114">You can allocate an entry in a recurring general journal to several different accounts when you post the journal.</span></span> <span data-ttu-id="acfa1-115">Úthlutunin getur verið í magni, prósentu eða upphæð.</span><span class="sxs-lookup"><span data-stu-id="acfa1-115">The allocation can be made by quantity, percentage, or amount.</span></span>
1. <span data-ttu-id="acfa1-116">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Ítrekunarfærslubók** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="acfa1-116">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Recurring General Journal**, and then choose the related link.</span></span>
2. <span data-ttu-id="acfa1-117">Veldu reitinn **Runuheiti** til að opna síðuna **Færslubókarkeyrslur**.</span><span class="sxs-lookup"><span data-stu-id="acfa1-117">Choose the **Batch Name** field to open the **General Journal Batches** page.</span></span>
3. <span data-ttu-id="acfa1-118">Þú getur annað hvort breytt úthlutunum á fyrirliggjandi runu í listanum eða stofnað nýja runu með úthlutunum.</span><span class="sxs-lookup"><span data-stu-id="acfa1-118">You can either modify allocations on an existing batch in the list or create a new batch with allocations.</span></span>
   * <span data-ttu-id="acfa1-119">Til að stofna nýja runu, velja **Nýtt** aðgerð og farið á næsta skref.</span><span class="sxs-lookup"><span data-stu-id="acfa1-119">To create a new batch, choose the **New** action, and go to the next step.</span></span>
   * <span data-ttu-id="acfa1-120">Til að breyta úthlutunum fyrir núverandi færslubók, veldu færslubók og farðu í skref 7.</span><span class="sxs-lookup"><span data-stu-id="acfa1-120">To change the allocations of an existing journal, select the journal and go to step 7.</span></span>    
4. <span data-ttu-id="acfa1-121">Í reitnum **Heiti** er fært inn heiti fyrir keyrsluna, eins og Þrif.</span><span class="sxs-lookup"><span data-stu-id="acfa1-121">In the **Name** field, enter a name for the batch, such as CLEANING.</span></span> <span data-ttu-id="acfa1-122">Í reitnum **Lýsing** skal færa inn lýsingu, eins og Hreinsa kostnaðarbók.</span><span class="sxs-lookup"><span data-stu-id="acfa1-122">In the **Description** field, enter a description, such as Cleaning Expenses Journal.</span></span>
5. <span data-ttu-id="acfa1-123">Að því loknu er síðunni lokað.</span><span class="sxs-lookup"><span data-stu-id="acfa1-123">When you are done, close the page.</span></span> <span data-ttu-id="acfa1-124">Ný, auð ítrekunarbók opnast.</span><span class="sxs-lookup"><span data-stu-id="acfa1-124">A new, empty recurring journal opens.</span></span>
6. <span data-ttu-id="acfa1-125">Reitirnir í línunni eru fylltir út.</span><span class="sxs-lookup"><span data-stu-id="acfa1-125">Fill in the fields on the line.</span></span>
7. <span data-ttu-id="acfa1-126">Valið er **úthluta** aðgerð.</span><span class="sxs-lookup"><span data-stu-id="acfa1-126">Choose the **Allocations** action.</span></span>
8. <span data-ttu-id="acfa1-127">Lína er bætt við fyrir hverja úthlutun.</span><span class="sxs-lookup"><span data-stu-id="acfa1-127">Add a line for each allocation.</span></span> <span data-ttu-id="acfa1-128">Annaðhvort þarf að fylla út reitinn **Úthlutun %**, **Úthlutunarmagn** eða **Upphæð**.</span><span class="sxs-lookup"><span data-stu-id="acfa1-128">You must fill in either the **Allocation %**, **Allocation Quantity**, or **Amount** field.</span></span> <span data-ttu-id="acfa1-129">Einnig þarf að fylla út reitinn **Reikningsnr.** og í reitina í altækum víddum ef færslan á að fara í altækar víddir.</span><span class="sxs-lookup"><span data-stu-id="acfa1-129">You must also fill in the **Account No.** field and, if you are allocating the transaction among global dimensions, the global dimension fields.</span></span>
9. <span data-ttu-id="acfa1-130">Þegar prósenta er færð í línu reiknast upphæðin í reitnum **Upphæð** sjálfkrafa.</span><span class="sxs-lookup"><span data-stu-id="acfa1-130">If you enter a percentage on a line, the amount in the **Amount** field is calculated automatically.</span></span> <span data-ttu-id="acfa1-131">Þessar upphæðir verða að hafa andstætt merki við það sem heildarupphæðin í reitnum **Upphæð** er með í ítrekunarbókinni.</span><span class="sxs-lookup"><span data-stu-id="acfa1-131">These amounts have the opposite sign from the total amount in the **Amount** field in the recurring journal.</span></span>
10. <span data-ttu-id="acfa1-132">Eftir að hafa fært inn úthlutunarlínurnar skal velja **Í lagi** til að fara aftur á síðuna **endurteknar færslubækur**.</span><span class="sxs-lookup"><span data-stu-id="acfa1-132">After entering the allocations lines, choose **OK** to return to the **Recurring General Journal** page.</span></span> <span data-ttu-id="acfa1-133">Svæðið **Úthlutuð upphæð (USD)** er fyllt út og er eins og svæðið **Upphæð**.</span><span class="sxs-lookup"><span data-stu-id="acfa1-133">The **Allocated Amt. (USD)** field is filled in and matches the **Amount** field.</span></span>
11. <span data-ttu-id="acfa1-134">Bóka skal færslubókina.</span><span class="sxs-lookup"><span data-stu-id="acfa1-134">Post the journal.</span></span>

## <a name="to-change-an-allocation-key-that-has-already-been-set-up"></a><span data-ttu-id="acfa1-135">Til að breyta uppsettum úthlutunarlykli</span><span class="sxs-lookup"><span data-stu-id="acfa1-135">To change an allocation key that has already been set up</span></span>
1. <span data-ttu-id="acfa1-136">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Ítrekunarfærslubók** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="acfa1-136">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Recurring General Journal**, and then choose the related link.</span></span>
2. <span data-ttu-id="acfa1-137">Á síðunni **Ítrekunarfærslubók** er færslubók með úthlutun valin.</span><span class="sxs-lookup"><span data-stu-id="acfa1-137">On the **Recurring General Journal** page, select the journal with the allocation.</span></span>
3. <span data-ttu-id="acfa1-138">Velja línu með úthlutuninni og velja síðan **úthlutanir**.</span><span class="sxs-lookup"><span data-stu-id="acfa1-138">Choose the line with the allocation, and then choose **Allocations** action.</span></span>
4. <span data-ttu-id="acfa1-139">Breyta viðeigandi reitum, og velja svo hnappinn **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="acfa1-139">Change the relevant fields, and then choose the **OK** button.</span></span>

## <a name="see-also"></a><span data-ttu-id="acfa1-140">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="acfa1-140">See Also</span></span>
[<span data-ttu-id="acfa1-141">Lokaár og Tímabil</span><span class="sxs-lookup"><span data-stu-id="acfa1-141">Closing Years and Periods</span></span>](year-close-years-periods.md)  
<span data-ttu-id="acfa1-142">[Vinna í færslubókum](ui-work-general-journals.md)  </span><span class="sxs-lookup"><span data-stu-id="acfa1-142">[Working with General Journals](ui-work-general-journals.md)  </span></span>  
<span data-ttu-id="acfa1-143">[Að bóka skjöl og færslubækur](ui-post-documents-journals.md)  </span><span class="sxs-lookup"><span data-stu-id="acfa1-143">[Posting Documents and Journals](ui-post-documents-journals.md)  </span></span>  
<span data-ttu-id="acfa1-144">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="acfa1-144">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
