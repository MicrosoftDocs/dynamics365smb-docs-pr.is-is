---
title: Skrá og endurgreiða útgjöld starfsmanna í viðskiptaerindum | Microsoft Docs
description: Bóka útgjöld starfsmanna með færslubók á reikning starfsmanns og bóka síðar greiðslu á bankareikning starfsmanns til að endurgreiða útgjöld í viðskiptaerindum.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reimbursement
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: edef774738233890af240b20622cc40585d79116
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5783823"
---
# <a name="record-and-reimburse-employees-expenses"></a><span data-ttu-id="dc884-103">Skrá og endurgreiða starfsmannaútgjöld</span><span class="sxs-lookup"><span data-stu-id="dc884-103">Record and Reimburse Employees' Expenses</span></span>

[!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="dc884-104">styður færslur fyrir starfsmann á svipaðan hátt og fyrir lánardrottna.</span><span class="sxs-lookup"><span data-stu-id="dc884-104">supports transactions for employee in a similar way as for vendors.</span></span> <span data-ttu-id="dc884-105">Til eru bókunarflokkar starfsmanna, sem eiga að tryggja að fjárhagsfærslur starfsmanna séu bókaðar á viðeigandi reikninga í færslubókinni.</span><span class="sxs-lookup"><span data-stu-id="dc884-105">Accordingly, employee posting groups exist to make sure that employee ledger entries are posted to the relevant accounts in the general ledger.</span></span>

> [!NOTE]  
> <span data-ttu-id="dc884-106">Starfsmannafærslur er eingöngu hægt að bóka í staðbundna gjaldmiðlinum.</span><span class="sxs-lookup"><span data-stu-id="dc884-106">Employee transactions can be posted in the local currency only.</span></span> <span data-ttu-id="dc884-107">Endurgreiðslur til starfsmanna styðja ekki aflsætti og greiðsluvikmörk.</span><span class="sxs-lookup"><span data-stu-id="dc884-107">Reimbursement payments to employees do not support discounts and payment tolerances.</span></span>

<span data-ttu-id="dc884-108">Ef starfsmenn eyða sínum eigin peningum í viðskiptaerindum, er hægt að bóka útgjöldin á reikning starfsmanns.</span><span class="sxs-lookup"><span data-stu-id="dc884-108">If employees spend their own money during business activities, you can post the expense to the employee's account.</span></span> <span data-ttu-id="dc884-109">Þá geturðu endurgreitt starfsmanninum með því að framkvæma greiðslu inn á bankareikning starfsmannsins, á svipaðan hátt og þú borgar lánardrottnum.</span><span class="sxs-lookup"><span data-stu-id="dc884-109">Then you can reimburse the employee by making a payment to the employee's bank account, similarly to how you pay vendors.</span></span>  

> [!TIP]
> <span data-ttu-id="dc884-110">Þessi grein útskýrir hvernig á að skrá kostnaðinn í bókunum og hvernig á að endurgreiða starfsmanninum.</span><span class="sxs-lookup"><span data-stu-id="dc884-110">This article explains how to record the expense in the books and how to reimburse the employee.</span></span> <span data-ttu-id="dc884-111">Fyrirtækið kann að vera með gátt eða forrit þar sem starfsmenn geta sent inn kostnaðarskýrslur.</span><span class="sxs-lookup"><span data-stu-id="dc884-111">Your organization may have a portal or app where employees can submit their expense reports.</span></span>

## <a name="to-record-an-employees-expense"></a><span data-ttu-id="dc884-112">Skrá útgjöld starfsmanns</span><span class="sxs-lookup"><span data-stu-id="dc884-112">To record an employee's expense</span></span>
<span data-ttu-id="dc884-113">Útgjöld starfsmanna eru bókuð á síðunni **Færslubók**.</span><span class="sxs-lookup"><span data-stu-id="dc884-113">You post employees' expenses on the **General Journal** page.</span></span>
1. <span data-ttu-id="dc884-114">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Færslubækur** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="dc884-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **General Journals**, and then choose the related link.</span></span>
2. <span data-ttu-id="dc884-115">Viðeigandi færslubók keyrsla er opnaður.</span><span class="sxs-lookup"><span data-stu-id="dc884-115">Open the relevant general journal batch.</span></span> <span data-ttu-id="dc884-116">Frekari upplýsingar, sjá [Vinna með almennar færslubækur](ui-work-general-journals.md).</span><span class="sxs-lookup"><span data-stu-id="dc884-116">For more information, see [Working with General Journals](ui-work-general-journals.md).</span></span>
3. <span data-ttu-id="dc884-117">Fyllið í reitina eftir þörfum í nýrri færslubókarlínu.</span><span class="sxs-lookup"><span data-stu-id="dc884-117">On a new journal line, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]    

    > [!NOTE]
    > [!INCLUDE[journal-showhide-columns-inline-tip](includes/journal-showhide-columns-inline-tip.md)]
4. <span data-ttu-id="dc884-118">Endurtakið skref 3 fyrir öll útgjöld sem starfsmaður hefur stofnað til.</span><span class="sxs-lookup"><span data-stu-id="dc884-118">Repeat step 3 for all the expenses that the employee has incurred.</span></span>

    > [!TIP]  
    > <span data-ttu-id="dc884-119">Ef þú vilt færa inn fleiri kostnaðarlínur fyrir ofan eina mótreikningslínu fyrir bankareikning starfsmanns, skaltu velja gátreitinn **Leggja til afstemmingarupphæð** á línunni fyrir þína keyrslu á síðunni **færslubókakeyrslur**.</span><span class="sxs-lookup"><span data-stu-id="dc884-119">If you want to enter multiple expense lines above one balance-account line for the employee's bank account, then select the **Suggest Balancing Amount** check box on the line for your batch on the **General Journal Batches** page.</span></span> <span data-ttu-id="dc884-120">Þá verður reiturinn **Upphæð** á mótreikningslínunni sjálfkrafa fylltur út með gildinu sem er nauðsynlegt til að jafna útgjöldin.</span><span class="sxs-lookup"><span data-stu-id="dc884-120">Then the **Amount** field on the balance-account line is automatically prefilled with the value that is required to balance the expenses.</span></span>
5. <span data-ttu-id="dc884-121">Veljið **Bóka** aðgerðina til að skrá útgjöldin á reikning starfsmanns.</span><span class="sxs-lookup"><span data-stu-id="dc884-121">Choose the **Post** action to record the expenses on the employee's account.</span></span>

## <a name="to-reimburse-an-employee"></a><span data-ttu-id="dc884-122">Endurgreiða starfsmanni</span><span class="sxs-lookup"><span data-stu-id="dc884-122">To reimburse an employee</span></span>
<span data-ttu-id="dc884-123">Þú endurgreiðir starfsmanni með því að bóka greiðslur á bankareikning hans á síðunni **greiðslubók**.</span><span class="sxs-lookup"><span data-stu-id="dc884-123">You reimburse employees by posting payments to their bank account on the **Payment Journal** page.</span></span>
1. <span data-ttu-id="dc884-124">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Greiðslubækur** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="dc884-124">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Payment Journals**, and then choose the related link.</span></span>
2. <span data-ttu-id="dc884-125">Viðeigandi greiðslubók keyrsla er opnaður.</span><span class="sxs-lookup"><span data-stu-id="dc884-125">Open the relevant payment journal batch.</span></span> <span data-ttu-id="dc884-126">Frekari upplýsingar, sjá [Vinna með almennar færslubækur](ui-work-general-journals.md).</span><span class="sxs-lookup"><span data-stu-id="dc884-126">For more information, see [Working with General Journals](ui-work-general-journals.md).</span></span>
3. <span data-ttu-id="dc884-127">Fyllið inn í reitina eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="dc884-127">Fill in the fields as necessary.</span></span> <span data-ttu-id="dc884-128">Frekari upplýsingar eru í [Greiðslur framkvæmdar](payables-make-payments.md).</span><span class="sxs-lookup"><span data-stu-id="dc884-128">For more information, see [Making Payments](payables-make-payments.md).</span></span>
4. <span data-ttu-id="dc884-129">Að öðrum kosti skal velja **Leggja til starfsmannagreiðslu** aðgerðina til að setja sjálfvirkt inn færslubókarlínu fyrir endurgreiðslu í bið til starfsmanns.</span><span class="sxs-lookup"><span data-stu-id="dc884-129">Alternatively, choose the **Suggest Employee Payment** action to automatically insert journal lines for pending employee reimbursements.</span></span>
5. <span data-ttu-id="dc884-130">Valið er **bóka** aðgerð til að skrá endurgreiðsluna.</span><span class="sxs-lookup"><span data-stu-id="dc884-130">Choose the **Post** action to register the reimbursement.</span></span>  

## <a name="to-reconcile-reimbursements-with-employee-ledger-entries"></a><span data-ttu-id="dc884-131">Afstemma endurgreiðslur við fjárhagsfærslur starfsmanns</span><span class="sxs-lookup"><span data-stu-id="dc884-131">To reconcile reimbursements with employee ledger entries</span></span>
<span data-ttu-id="dc884-132">Þú jafnar greiðslu til starfsmanns við tengdar og opnar fjárhagsfærslur starfsmanns á sama hátt og greiðslur til lánardrottins, til dæmis á síðunni **Greiðsluafstemmingarbók**, byggt á tengdum bankayfirlitsfærslum.</span><span class="sxs-lookup"><span data-stu-id="dc884-132">You apply employee payments to their related open employee ledger entries in the same way as you do for vendor payments, for example on the **Payment Reconciliation Journal** page, based on the related bank statement entries.</span></span> <span data-ttu-id="dc884-133">Nánari upplýsingar er að finna í [Jafna greiðslur sjálfkrafa og afstemma bankareikninga](receivables-apply-payments-auto-reconcile-bank-accounts.md).</span><span class="sxs-lookup"><span data-stu-id="dc884-133">For more information, see [Applying Payments Automatically and Reconciling Bank Accounts](receivables-apply-payments-auto-reconcile-bank-accounts.md).</span></span> <span data-ttu-id="dc884-134">Einnig er hægt að jafna handvirkt á síðunni **Fjárhagsfærslur starfsmanna**.</span><span class="sxs-lookup"><span data-stu-id="dc884-134">Alternatively, you can apply manually on the **Employee Ledger Entries** page.</span></span> <span data-ttu-id="dc884-135">Frekari upplýsingar er að finna í [Afstemma greiðslu lánardrottins með greiðslubók eða úr færslum í lánardrottnabók](payables-how-apply-purchase-transactions-manually.md).</span><span class="sxs-lookup"><span data-stu-id="dc884-135">For more information, see the related [Reconcile Vendor Payments with the Payment Journal or from Vendor Ledger Entries](payables-how-apply-purchase-transactions-manually.md).</span></span>  

## <a name="see-also"></a><span data-ttu-id="dc884-136">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="dc884-136">See Also</span></span>
[<span data-ttu-id="dc884-137">Bóka færslu beint í Fjárhag</span><span class="sxs-lookup"><span data-stu-id="dc884-137">Post Transactions Directly to the General Ledger</span></span>](finance-how-post-transactions-directly.md)  
[<span data-ttu-id="dc884-138">Vinna í færslubókum</span><span class="sxs-lookup"><span data-stu-id="dc884-138">Working with General Journals</span></span>](ui-work-general-journals.md)  
[<span data-ttu-id="dc884-139">Bakfæra bókanir í færslubók og afturkalla kvittanir/sendingar</span><span class="sxs-lookup"><span data-stu-id="dc884-139">Reverse Journal Postings and Undo Receipts/Shipments</span></span>](finance-how-reverse-journal-posting.md)  
[<span data-ttu-id="dc884-140">Fjármál</span><span class="sxs-lookup"><span data-stu-id="dc884-140">Finance</span></span>](finance.md)  
<span data-ttu-id="dc884-141">[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="dc884-141">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  


[!INCLUDE[footer-include](includes/footer-banner.md)]