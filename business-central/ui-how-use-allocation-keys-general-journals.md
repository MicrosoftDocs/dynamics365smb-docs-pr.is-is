---
title: Nota úthlutunarlykla í færslubókum | Microsoft Docs
description: Lærðu hvernig þú getur notað úthlutunarlykla í færslubókum.
services: project-madeira
documentationcenter: ''
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: cost accounting
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 408dfeaeb56f271a2b9b3d5cf515e41abeaf78e8
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2020
ms.locfileid: "3195556"
---
# <a name="use-allocation-keys-in-general-journals"></a><span data-ttu-id="ef0b9-103">Nota úthlutunarlykla í færslubókum</span><span class="sxs-lookup"><span data-stu-id="ef0b9-103">Use Allocation Keys in General Journals</span></span>
<span data-ttu-id="ef0b9-104">Hægt er að úthluta færslu úr færslubók til nokkurra reikninga þegar færslubókin er bókuð.</span><span class="sxs-lookup"><span data-stu-id="ef0b9-104">You can allocate an entry in a general journal to several different accounts when you post the journal.</span></span> <span data-ttu-id="ef0b9-105">Úthlutunin getur verið í magni, prósentu eða upphæð.</span><span class="sxs-lookup"><span data-stu-id="ef0b9-105">The allocation can be made by quantity, percentage, or amount.</span></span>

## <a name="to-set-up-allocation-keys"></a><span data-ttu-id="ef0b9-106">setja upp úthlutunarlykla</span><span class="sxs-lookup"><span data-stu-id="ef0b9-106">To set up allocation keys</span></span>
1. <span data-ttu-id="ef0b9-107">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Ítrekunarfærslubók** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="ef0b9-107">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Recurring General Journal**, and then choose the related link.</span></span>
2. <span data-ttu-id="ef0b9-108">Veldu reitinn **Runuheiti** til að opna síðuna **Færslubókarkeyrslur**.</span><span class="sxs-lookup"><span data-stu-id="ef0b9-108">Choose the **Batch Name** field to open the **General Journal Batches** page.</span></span>
3. <span data-ttu-id="ef0b9-109">Þú getur annað hvort breytt úthlutunum á fyrirliggjandi runu í listanum eða stofnað nýja runu með úthlutunum.</span><span class="sxs-lookup"><span data-stu-id="ef0b9-109">You can either modify allocations on an existing batch in the list or create a new batch with allocations.</span></span>
   * <span data-ttu-id="ef0b9-110">Til að stofna nýja runu, velja **Nýtt** aðgerð og farið á næsta skref.</span><span class="sxs-lookup"><span data-stu-id="ef0b9-110">To create a new batch, choose the **New** action, and go to the next step.</span></span>
   * <span data-ttu-id="ef0b9-111">Til að breyta úthlutunum fyrir núverandi færslubók, veldu færslubók og farðu í skref 7.</span><span class="sxs-lookup"><span data-stu-id="ef0b9-111">To change the allocations of an existing journal, select the journal and go to step 7.</span></span>    
4. <span data-ttu-id="ef0b9-112">Í reitnum **Heiti** er fært inn heiti fyrir keyrsluna, eins og Þrif.</span><span class="sxs-lookup"><span data-stu-id="ef0b9-112">In the **Name** field, enter a name for the batch, such as CLEANING.</span></span> <span data-ttu-id="ef0b9-113">Í reitnum **Lýsing** skal færa inn lýsingu, eins og Hreinsa kostnaðarbók.</span><span class="sxs-lookup"><span data-stu-id="ef0b9-113">In the **Description** field, enter a description, such as Cleaning Expenses Journal.</span></span>
5. <span data-ttu-id="ef0b9-114">Að því loknu er síðunni lokað.</span><span class="sxs-lookup"><span data-stu-id="ef0b9-114">When you are done, close the page.</span></span> <span data-ttu-id="ef0b9-115">Ný, auð ítrekunarbók opnast.</span><span class="sxs-lookup"><span data-stu-id="ef0b9-115">A new, empty recurring journal opens.</span></span>
6. <span data-ttu-id="ef0b9-116">Reitirnir í línunni eru fylltir út.</span><span class="sxs-lookup"><span data-stu-id="ef0b9-116">Fill in the fields on the line.</span></span>
7. <span data-ttu-id="ef0b9-117">Valið er **úthluta** aðgerð.</span><span class="sxs-lookup"><span data-stu-id="ef0b9-117">Choose the **Allocations** action.</span></span>
8. <span data-ttu-id="ef0b9-118">Lína er bætt við fyrir hverja úthlutun.</span><span class="sxs-lookup"><span data-stu-id="ef0b9-118">Add a line for each allocation.</span></span> <span data-ttu-id="ef0b9-119">Annaðhvort þarf að fylla út reitinn **Úthlutun %**, **Úthlutunarmagn** eða **Upphæð**.</span><span class="sxs-lookup"><span data-stu-id="ef0b9-119">You must fill in either the **Allocation %**, **Allocation Quantity**, or **Amount** field.</span></span> <span data-ttu-id="ef0b9-120">Einnig þarf að fylla út reitinn **Reikningsnr.** og í reitina í altækum víddum ef færslan á að fara í altækar víddir.</span><span class="sxs-lookup"><span data-stu-id="ef0b9-120">You must also fill in the **Account No.** field and, if you are allocating the transaction among global dimensions, the global dimension fields.</span></span>
9. <span data-ttu-id="ef0b9-121">Þegar prósenta er færð í línu reiknast upphæðin í reitnum **Upphæð** sjálfkrafa.</span><span class="sxs-lookup"><span data-stu-id="ef0b9-121">If you enter a percentage on a line, the amount in the **Amount** field is calculated automatically.</span></span> <span data-ttu-id="ef0b9-122">Þessar upphæðir verða að hafa andstætt merki við það sem heildarupphæðin í reitnum **Upphæð** er með í ítrekunarbókinni.</span><span class="sxs-lookup"><span data-stu-id="ef0b9-122">These amounts have the opposite sign from the total amount in the **Amount** field in the recurring journal.</span></span>
10. <span data-ttu-id="ef0b9-123">Eftir að hafa fært inn úthlutunarlínurnar skal velja **Í lagi** til að fara aftur á síðuna **endurteknar færslubækur**.</span><span class="sxs-lookup"><span data-stu-id="ef0b9-123">After entering the allocations lines, choose **OK** to return to the **Recurring General Journal** page.</span></span> <span data-ttu-id="ef0b9-124">Svæðið **Úthlutuð upphæð (USD)** er fyllt út og er eins og svæðið **Upphæð**.</span><span class="sxs-lookup"><span data-stu-id="ef0b9-124">The **Allocated Amt. (USD)** field is filled in and matches the **Amount** field.</span></span>
11. <span data-ttu-id="ef0b9-125">Bóka skal færslubókina.</span><span class="sxs-lookup"><span data-stu-id="ef0b9-125">Post the journal.</span></span>

## <a name="to-change-an-allocation-key-that-has-already-been-set-up"></a><span data-ttu-id="ef0b9-126">Til að breyta uppsettum úthlutunarlykli</span><span class="sxs-lookup"><span data-stu-id="ef0b9-126">To change an allocation key that has already been set up</span></span>
1. <span data-ttu-id="ef0b9-127">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Ítrekunarfærslubók** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="ef0b9-127">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Recurring General Journal**, and then choose the related link.</span></span>
2. <span data-ttu-id="ef0b9-128">Á síðunni **Ítrekunarfærslubók** er færslubók með úthlutun valin.</span><span class="sxs-lookup"><span data-stu-id="ef0b9-128">On the **Recurring General Journal** page, select the journal with the allocation.</span></span>
3. <span data-ttu-id="ef0b9-129">Velja línu með úthlutuninni og velja síðan **úthlutanir**.</span><span class="sxs-lookup"><span data-stu-id="ef0b9-129">Choose the line with the allocation, and then choose **Allocations** action.</span></span>
4. <span data-ttu-id="ef0b9-130">Breyta viðeigandi reitum, og velja svo hnappinn **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="ef0b9-130">Change the relevant fields, and then choose the **OK** button.</span></span>

## <a name="see-also"></a><span data-ttu-id="ef0b9-131">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="ef0b9-131">See Also</span></span>
[<span data-ttu-id="ef0b9-132">Vinna í færslubókum</span><span class="sxs-lookup"><span data-stu-id="ef0b9-132">Working with General Journals</span></span>](ui-work-general-journals.md)  
[<span data-ttu-id="ef0b9-133">Bókun skjala og færslubóka</span><span class="sxs-lookup"><span data-stu-id="ef0b9-133">Posting Documents and Journals</span></span>](ui-post-documents-journals.md)  
<span data-ttu-id="ef0b9-134">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="ef0b9-134">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
