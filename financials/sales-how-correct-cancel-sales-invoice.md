---
title: "Leiðrétta eða hætta við bókaðan sölureikning | Microsoft Docs"
description: "Lýsir því hvernig skal leiðrétta, afturkalla eða hætta við bókaðan sölureikning og jafna sölukreditreikning."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: undo, credit memo, return
ms.date: 08/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: e8e5a4762564d036ac8c0e7bdaf9e13b448d37f4
ms.contentlocale: is-is
ms.lasthandoff: 03/22/2018

---
# <a name="correct-or-cancel-unpaid-sales-invoices"></a><span data-ttu-id="0f5ff-103">Ógreiddir sölureikningar leiðréttir eða afturkallaðir</span><span class="sxs-lookup"><span data-stu-id="0f5ff-103">Correct or Cancel Unpaid Sales Invoices</span></span>
<span data-ttu-id="0f5ff-104">Hægt er að leiðrétta eða afturkalla bókaðann sölureikning.</span><span class="sxs-lookup"><span data-stu-id="0f5ff-104">You can correct or cancel a posted sales invoice.</span></span> <span data-ttu-id="0f5ff-105">Þetta er gagnlegt þegar mistök eiga sér stað eða ef viðskiptamaðurinn biður um breytingu.</span><span class="sxs-lookup"><span data-stu-id="0f5ff-105">This is useful if you make a mistake or if the customer requests a change.</span></span>

> [!NOTE]  
>   <span data-ttu-id="0f5ff-106">Þegar bókaðaður sölureikningur hefur verið greiddur að hluta til eða að fullu, er ekki hægt að leiðrétta eða hætta við hann í bókaða sölureikningnum sjálfum.</span><span class="sxs-lookup"><span data-stu-id="0f5ff-106">After a posted sales invoice has been partially or fully paid, you cannot correct or cancel it from the posted sales invoice itself.</span></span> <span data-ttu-id="0f5ff-107">Þess i stað þarf að stofna sölukreditreikning handvirkt til að ógilda söluna og endurgreiða viðskiptamanninum, valfrjálst stjórnað með söluvöruskilapöntun.</span><span class="sxs-lookup"><span data-stu-id="0f5ff-107">Instead, you must manually create a sales credit memo to void the sale and reimburse the customer, optionally managed with a sales return order.</span></span> <span data-ttu-id="0f5ff-108">Fyrir frekar upplýsingar, sjá [Meðhöndlun söluvöruskila eða afturkallana](sales-how-process-sales-returns-cancellations.md).</span><span class="sxs-lookup"><span data-stu-id="0f5ff-108">For more information, see [Process Sales Returns or Cancellations](sales-how-process-sales-returns-cancellations.md).</span></span>

<span data-ttu-id="0f5ff-109">Í glugganum **Bókaður sölureikningur** er hægt að velja aðgerðina **Leiðrétting** eða aðgerina **Hætta við** til að framkvæma aðgerðirnar sem lýst er í eftirfarandi töflu.</span><span class="sxs-lookup"><span data-stu-id="0f5ff-109">In the **Posted Sales Invoice** window, you can choose the **Correct** action or the **Cancel** action to perform the actions that are described in the following table.</span></span>

| <span data-ttu-id="0f5ff-110">Aðgerð</span><span class="sxs-lookup"><span data-stu-id="0f5ff-110">Action</span></span> | <span data-ttu-id="0f5ff-111">Lýsing</span><span class="sxs-lookup"><span data-stu-id="0f5ff-111">Description</span></span> |
| --- | --- |
| <span data-ttu-id="0f5ff-112">**Leiðrétta**</span><span class="sxs-lookup"><span data-stu-id="0f5ff-112">**Correct**</span></span> |<span data-ttu-id="0f5ff-113">Bókaði sölureikningurinn er afturkallaður.</span><span class="sxs-lookup"><span data-stu-id="0f5ff-113">The posted sales invoice is canceled.</span></span> <span data-ttu-id="0f5ff-114">Nýr sölureikingur með sömu upplýsingum er stofnaður.</span><span class="sxs-lookup"><span data-stu-id="0f5ff-114">A new sales invoice with the same information is created.</span></span> <span data-ttu-id="0f5ff-115">Hægt er að leiðrétta og halda svo áfram söluferlinu.</span><span class="sxs-lookup"><span data-stu-id="0f5ff-115">You can make the correction and then continue the sales process.</span></span> <span data-ttu-id="0f5ff-116">Nýi sölureikningurinn hefur annað númer en upprunalegi sölureikningurinn.</span><span class="sxs-lookup"><span data-stu-id="0f5ff-116">The new sales invoice has a different number than the initial sales invoice.</span></span> <span data-ttu-id="0f5ff-117">Leiðréttur sölukreditreikningur er búinn til sjálfkrafa og bókaður til að ógilda upphaflega bókaða sölureikninginn.</span><span class="sxs-lookup"><span data-stu-id="0f5ff-117">A corrective sales credit memo is automatically created and posted to void the initial posted sales invoice.</span></span> <span data-ttu-id="0f5ff-118">Á upphaflega bókuðum sölureikningi eru gátreitirnir  hætt við og  greitt valdir.</span><span class="sxs-lookup"><span data-stu-id="0f5ff-118">On the initial posted sales invoice, the Canceled and Paid check boxes are selected.</span></span> |
| <span data-ttu-id="0f5ff-119">**Hætta við**</span><span class="sxs-lookup"><span data-stu-id="0f5ff-119">**Cancel**</span></span> |<span data-ttu-id="0f5ff-120">Bókaði sölureikningurinn er afturkallaður.</span><span class="sxs-lookup"><span data-stu-id="0f5ff-120">The posted sales invoice is canceled.</span></span> <span data-ttu-id="0f5ff-121">Leiðréttur sölukreditreikningur er búinn til sjálfkrafa og bókaður til að ógilda upphaflega bókaða sölureikninginn.</span><span class="sxs-lookup"><span data-stu-id="0f5ff-121">A corrective sales credit memo is automatically created and posted to void the initial posted sales invoice.</span></span> <span data-ttu-id="0f5ff-122">Á upphaflega bókuðum sölureikningi eru gátreitirnir  hætt við og  greitt valdir.</span><span class="sxs-lookup"><span data-stu-id="0f5ff-122">On the initial posted sales invoice, the Canceled and Paid check boxes are selected.</span></span> |

<span data-ttu-id="0f5ff-123">Þegar hinn bókaður sölureikningur er leiðréttur eða afturkallaður, er hann jafnaður við allar fjárhags- og raunbirgðafærslur sem búnar voru til við bókun hins upphaflega sölureiknings.</span><span class="sxs-lookup"><span data-stu-id="0f5ff-123">When you correct or cancel a posted sales invoice, the corrective sales credit memo is applied to all general ledger and inventory ledger entries that were created when the initial sales invoice was posted.</span></span> <span data-ttu-id="0f5ff-124">Þetta bakfærir hinn bókaða sölureikning í fjárhagslegum færslum og lætur hina leiðréttu bókaða sölukreditreikninga í endurskoðunarrakninguna.</span><span class="sxs-lookup"><span data-stu-id="0f5ff-124">This reverses the posted sales invoice in your financial records and leaves the corrective posted sales credit memo for your audit trail.</span></span>

## <a name="to-correct-a-posted-sales-invoice"></a><span data-ttu-id="0f5ff-125">Bókaður sölureikningur leiðréttur</span><span class="sxs-lookup"><span data-stu-id="0f5ff-125">To correct a posted sales invoice</span></span>
1. <span data-ttu-id="0f5ff-126">Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Bókaðir sölureikningar** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="0f5ff-126">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Posted Sales Invoices**, and then choose the related link.</span></span>  
2. <span data-ttu-id="0f5ff-127">Veljið bókaða sölureikninginn sem á að leiðrétta.</span><span class="sxs-lookup"><span data-stu-id="0f5ff-127">Select the posted sales invoice that you want to correct.</span></span>

    > [!NOTE]  
>   <span data-ttu-id="0f5ff-128">Ef gátreiturinn **hætt við** er valinn, er ekki hægt að leiðrétta þennan bókaða sölureikning þar sem hann hefur þegar verið leiðréttur eða hætt var við hann.</span><span class="sxs-lookup"><span data-stu-id="0f5ff-128">If the **Canceled** check box is selected, then you cannot correct the posted sales invoice because it has already been corrected or canceled.</span></span>
3. <span data-ttu-id="0f5ff-129">Í reitnum **Bókaður Sölureikningur** er valið **leiðrétta** aðgerð.</span><span class="sxs-lookup"><span data-stu-id="0f5ff-129">In the **Posted Sales Invoice** window, choose the **Correct** action.</span></span>  
4. <span data-ttu-id="0f5ff-130">Nýr sölureikningur með sömu upplýsingum er stofnaður þar sem hægt er að gera leiðréttinguna.</span><span class="sxs-lookup"><span data-stu-id="0f5ff-130">A new sales invoice with the same information is created where you can make the correction.</span></span> <span data-ttu-id="0f5ff-131">Reiturinn **hætt við** á hinum upphaflega bókaða sölureikningi er breytt í **Já**.</span><span class="sxs-lookup"><span data-stu-id="0f5ff-131">The **Canceled** field on the initial posted sales invoice is changed to **Yes**.</span></span>

    <span data-ttu-id="0f5ff-132">Sölukreditreikningur er búinn til sjálfkrafa og bókaður til að ógilda upphaflega bókaða sölureikninginn.</span><span class="sxs-lookup"><span data-stu-id="0f5ff-132">A sales credit memo is automatically created and posted to void the initial posted sales invoice.</span></span>
5. <span data-ttu-id="0f5ff-133">velja **sýna leiðréttan kreditreikning** aðgerðina til að skoða bókaða sölukreditreikninginn sem ógildir upphaflega bókaða sölureikninginn.</span><span class="sxs-lookup"><span data-stu-id="0f5ff-133">Choose the **Show Corrective Credit Memo** action to view the posted sales credit memo that voids the initial posted sales invoice.</span></span>

## <a name="to-cancel-a-posted-sales-invoice"></a><span data-ttu-id="0f5ff-134">Bókaður sölureikningur afturkallaður</span><span class="sxs-lookup"><span data-stu-id="0f5ff-134">To cancel a posted sales invoice</span></span>
1. <span data-ttu-id="0f5ff-135">Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Bókaðir sölureikningar** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="0f5ff-135">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Posted Sales Invoices**, and then choose the related link.</span></span>  
2. <span data-ttu-id="0f5ff-136">Veljið bókaða sölureikninginn sem á að afturkalla.</span><span class="sxs-lookup"><span data-stu-id="0f5ff-136">Select the posted sales invoice that you want to cancel.</span></span>

    > [!NOTE]  
>   <span data-ttu-id="0f5ff-137">Ef gátreiturinn **hætt við** er valinn, er ekki hægt að hætta við þennan bókaða sölureikning þar sem þegar hefur verið hætt við hann eða hann leiðréttur.</span><span class="sxs-lookup"><span data-stu-id="0f5ff-137">If the **Canceled** check box is selected, then you cannot cancel the posted sales invoice because it has already been canceled or corrected.</span></span>
3. <span data-ttu-id="0f5ff-138">Í reitnum **Bókaður Sölureikningur** er valið **hætta við** aðgerð.</span><span class="sxs-lookup"><span data-stu-id="0f5ff-138">In the **Posted Sales Invoice** window, choose the **Cancel** action.</span></span>

    <span data-ttu-id="0f5ff-139">Sölukreditreikningur er búinn til sjálfkrafa og bókaður til að ógilda upphaflega bókaða sölureikninginn.</span><span class="sxs-lookup"><span data-stu-id="0f5ff-139">A sales credit memo is automatically created and posted to void the initial posted sales invoice.</span></span> <span data-ttu-id="0f5ff-140">Reiturinn **hætt við** á hinum upphaflega bókaða sölureikningi er breytt í **Já**.</span><span class="sxs-lookup"><span data-stu-id="0f5ff-140">The **Canceled** field on the initial posted sales invoice is changed to **Yes**.</span></span>
4. <span data-ttu-id="0f5ff-141">Velja **sýna leiðréttan kreditreikning** til að skoða bókaða sölukreditreikninginn sem ógildir upphaflega bókaða sölureikninginn.</span><span class="sxs-lookup"><span data-stu-id="0f5ff-141">Choose **Show Corrective Credit Memo** to view the posted sales credit memo that voids the initial posted sales invoice.</span></span>

## <a name="see-also"></a><span data-ttu-id="0f5ff-142">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="0f5ff-142">See Also</span></span>
[<span data-ttu-id="0f5ff-143">Sala</span><span class="sxs-lookup"><span data-stu-id="0f5ff-143">Sales</span></span>](sales-manage-sales.md)  
[<span data-ttu-id="0f5ff-144">Uppsetning sölu</span><span class="sxs-lookup"><span data-stu-id="0f5ff-144">Setting Up Sales</span></span>](sales-setup-sales.md)  
[<span data-ttu-id="0f5ff-145">Senda skjöl í tölvupósti</span><span class="sxs-lookup"><span data-stu-id="0f5ff-145">Send Documents by Email</span></span>](ui-how-send-documents-email.md)  
<span data-ttu-id="0f5ff-146">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="0f5ff-146">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

