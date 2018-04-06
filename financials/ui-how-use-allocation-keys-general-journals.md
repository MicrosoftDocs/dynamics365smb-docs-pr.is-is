---
title: "Nota úthlutunarlykla í færslubókum | Microsoft Docs"
description: "Lærðu hvernig þú getur notað úthlutunarlykla í færslubókum."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: cost accounting
ms.date: 03/29/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 6ee3e0f325623666eb720e3cc2656cfd1f6332eb
ms.contentlocale: is-is
ms.lasthandoff: 03/22/2018

---
# <a name="use-allocation-keys-in-general-journals"></a><span data-ttu-id="18dda-103">Nota úthlutunarlykla í færslubókum</span><span class="sxs-lookup"><span data-stu-id="18dda-103">Use Allocation Keys in General Journals</span></span>
<span data-ttu-id="18dda-104">Hægt er að úthluta færslu úr færslubók til nokkurra reikninga þegar færslubókin er bókuð.</span><span class="sxs-lookup"><span data-stu-id="18dda-104">You can allocate an entry in a general journal to several different accounts when you post the journal.</span></span> <span data-ttu-id="18dda-105">Úthlutunin getur verið í magni, prósentu eða upphæð.</span><span class="sxs-lookup"><span data-stu-id="18dda-105">The allocation can be made by quantity, percentage, or amount.</span></span>

## <a name="to-set-up-allocation-keys"></a><span data-ttu-id="18dda-106">setja upp úthlutunarlykla</span><span class="sxs-lookup"><span data-stu-id="18dda-106">To set up allocation keys</span></span>
1. <span data-ttu-id="18dda-107">Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Ítrekunarfærslubók** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="18dda-107">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Recurring General Journal**, and then choose the related link.</span></span>
2. <span data-ttu-id="18dda-108">Veldu **runuheiti** reitinn til að opna **færslubókarkeyrslu** gluggann.</span><span class="sxs-lookup"><span data-stu-id="18dda-108">Choose the **Batch Name** field to open the **General Journal Batches** window.</span></span>
3. <span data-ttu-id="18dda-109">Þú getur annað hvort breytt úthlutunum á fyrirliggjandi runu í listanum eða stofna nýja runu með úthlutunum.</span><span class="sxs-lookup"><span data-stu-id="18dda-109">You can either modify allocations on an existing batch in the list or create a new batch with allocations.</span></span>
   * <span data-ttu-id="18dda-110">Til að stofna nýja runu, velja **Nýtt** aðgerð og farið á næsta skref.</span><span class="sxs-lookup"><span data-stu-id="18dda-110">To create a new batch, choose the **New** action, and go to the next step.</span></span>
   * <span data-ttu-id="18dda-111">Til að breyta úthlutunum fyrir núverandi færslubók, veldu færslubók og farðu í skref 7.</span><span class="sxs-lookup"><span data-stu-id="18dda-111">To change the allocations of an existing journal, select the journal and go to step 7.</span></span>    
4. <span data-ttu-id="18dda-112">Í reitnum **Heiti** er fært inn heiti fyrir keyrsluna, eins og Þrif.</span><span class="sxs-lookup"><span data-stu-id="18dda-112">In the **Name** field, enter a name for the batch, such as CLEANING.</span></span> <span data-ttu-id="18dda-113">Í reitnum **Lýsing** færið inn lýsingu, eins og Hreinsa kostnaðarbók.</span><span class="sxs-lookup"><span data-stu-id="18dda-113">In the **Description** field, enter a description, such as Cleaning Expenses Journal.</span></span>
5. <span data-ttu-id="18dda-114">Lokið glugganum þegar þessu er lokið.</span><span class="sxs-lookup"><span data-stu-id="18dda-114">When you are done, close the window.</span></span> <span data-ttu-id="18dda-115">Ný, auð ítrekunarbók opnast.</span><span class="sxs-lookup"><span data-stu-id="18dda-115">A new, empty recurring journal opens.</span></span>
6. <span data-ttu-id="18dda-116">Reitirnir í línunni eru fylltir út.</span><span class="sxs-lookup"><span data-stu-id="18dda-116">Fill in the fields on the line.</span></span>
7. <span data-ttu-id="18dda-117">Valið er **úthluta** aðgerð.</span><span class="sxs-lookup"><span data-stu-id="18dda-117">Choose the **Allocations** action.</span></span>
8. <span data-ttu-id="18dda-118">Lína er bætt við fyrir hverja úthlutun.</span><span class="sxs-lookup"><span data-stu-id="18dda-118">Add a line for each allocation.</span></span> <span data-ttu-id="18dda-119">Annaðhvort þarf að fylla út reitinn **Úthlutun %**, **Úthlutunarmagn** eða **Upphæð**.</span><span class="sxs-lookup"><span data-stu-id="18dda-119">You must fill in either the **Allocation %**, **Allocation Quantity**, or **Amount** field.</span></span> <span data-ttu-id="18dda-120">Einnig þarf að fylla út reitinn **Reikningsnr.** og í reitina í altækum víddum ef færslan á að fara í altækar víddir.</span><span class="sxs-lookup"><span data-stu-id="18dda-120">You must also fill in the **Account No.** field and, if you are allocating the transaction among global dimensions, the global dimension fields.</span></span>
9. <span data-ttu-id="18dda-121">Þegar prósenta er færð í línu reiknast upphæðin í reitnum **Upphæð** sjálfkrafa.</span><span class="sxs-lookup"><span data-stu-id="18dda-121">If you enter a percentage on a line, the amount in the **Amount** field is calculated automatically.</span></span> <span data-ttu-id="18dda-122">Þessar upphæðir verða að hafa andstætt merki við það sem heildarupphæðin í reitnum **Upphæð** er með í ítrekunarbókinni.</span><span class="sxs-lookup"><span data-stu-id="18dda-122">These amounts have the opposite sign from the total amount in the **Amount** field in the recurring journal.</span></span>
10. <span data-ttu-id="18dda-123">Eftir að hafa fært inn úthlutunarlínurnar skal velja **Í lagi** til að fara aftur í gluggann **endurteknar færslubækur**.</span><span class="sxs-lookup"><span data-stu-id="18dda-123">After entering the allocations lines, choose **OK** to return to the **Recurring General Journal** window.</span></span> <span data-ttu-id="18dda-124">Svæðið **Úthlutuð upphæð (USD)** er fyllt út og er eins og svæðið **Upphæð**.</span><span class="sxs-lookup"><span data-stu-id="18dda-124">The **Allocated Amt. (USD)** field is filled in and matches the **Amount** field.</span></span>
11. <span data-ttu-id="18dda-125">Bóka skal færslubókina.</span><span class="sxs-lookup"><span data-stu-id="18dda-125">Post the journal.</span></span>

## <a name="to-change-an-allocation-key-that-has-already-been-set-up"></a><span data-ttu-id="18dda-126">Breyta uppsettum úthlutunarlykli.</span><span class="sxs-lookup"><span data-stu-id="18dda-126">To change an allocation key that has already been set up</span></span>
1. <span data-ttu-id="18dda-127">Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Ítrekunarfærslubók** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="18dda-127">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Recurring General Journal**, and then choose the related link.</span></span>
2. <span data-ttu-id="18dda-128">Í glugganum**Ítrekunarfærslubók** er færslubók með úthlutun valin.</span><span class="sxs-lookup"><span data-stu-id="18dda-128">In the **Recurring General Journal** window, select the journal with the allocation.</span></span>
3. <span data-ttu-id="18dda-129">Velja línu með úthlutuninni og velja síðan **úthlutanir**.</span><span class="sxs-lookup"><span data-stu-id="18dda-129">Choose the line with the allocation, and then choose **Allocations** action.</span></span>
4. <span data-ttu-id="18dda-130">Breyta viðeigandi reitum, og velja svo hnappinn **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="18dda-130">Change the relevant fields, and then choose the **OK** button.</span></span>

## <a name="see-also"></a><span data-ttu-id="18dda-131">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="18dda-131">See Also</span></span>
[<span data-ttu-id="18dda-132">Vinna í færslubókum</span><span class="sxs-lookup"><span data-stu-id="18dda-132">Working with General Journals</span></span>](ui-work-general-journals.md)  
[<span data-ttu-id="18dda-133">Að bóka skjöl og færslubækur</span><span class="sxs-lookup"><span data-stu-id="18dda-133">Posting Documents and Journals</span></span>](ui-post-documents-journals.md)  
<span data-ttu-id="18dda-134">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="18dda-134">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

