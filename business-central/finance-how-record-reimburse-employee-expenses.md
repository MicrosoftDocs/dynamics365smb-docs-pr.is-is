---
title: Skrá og endurgreiða útgjöld starfsmanna í viðskiptaerindum
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
ms.openlocfilehash: dd4ce755e3414f19ae501c1d437f3e1d78d565a1
ms.sourcegitcommit: 1aab52477956bf1aa7376fc7fb984644bc398c61
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/04/2021
ms.locfileid: "6184400"
---
# <a name="record-and-reimburse-employees-expenses"></a><span data-ttu-id="91686-103">Skrá og endurgreiða starfsmannaútgjöld</span><span class="sxs-lookup"><span data-stu-id="91686-103">Record and Reimburse Employees' Expenses</span></span>

[!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="91686-104">styður færslur fyrir starfsmenn á svipaðan hátt og fyrir lánardrottna.</span><span class="sxs-lookup"><span data-stu-id="91686-104">supports transactions for employees in a similar way as for vendors.</span></span> <span data-ttu-id="91686-105">Til eru bókunarflokkar starfsmanna, sem eiga að tryggja að fjárhagsfærslur starfsmanna séu bókaðar á viðeigandi reikninga í færslubókinni.</span><span class="sxs-lookup"><span data-stu-id="91686-105">Accordingly, employee posting groups exist to make sure that employee ledger entries are posted to the relevant accounts in the general ledger.</span></span>

> [!NOTE]  
> <span data-ttu-id="91686-106">Starfsmannafærslur er eingöngu hægt að bóka í staðbundna gjaldmiðlinum.</span><span class="sxs-lookup"><span data-stu-id="91686-106">Employee transactions can be posted in the local currency only.</span></span> <span data-ttu-id="91686-107">Endurgreiðslur til starfsmanna styðja ekki aflsætti og greiðsluvikmörk.</span><span class="sxs-lookup"><span data-stu-id="91686-107">Reimbursement payments to employees do not support discounts and payment tolerances.</span></span>

<span data-ttu-id="91686-108">Ef starfsmenn eyða sínum eigin peningum í viðskiptaerindum, er hægt að bóka útgjöldin á reikning starfsmanns.</span><span class="sxs-lookup"><span data-stu-id="91686-108">If employees spend their own money during business activities, you can post the expense to the employee's account.</span></span> <span data-ttu-id="91686-109">Þá geturðu endurgreitt starfsmanninum með því að framkvæma greiðslu inn á bankareikning starfsmannsins, á svipaðan hátt og þú borgar lánardrottnum.</span><span class="sxs-lookup"><span data-stu-id="91686-109">Then you can reimburse the employee by making a payment to the employee's bank account, similarly to how you pay vendors.</span></span>  

> [!TIP]
> <span data-ttu-id="91686-110">Þessi grein útskýrir hvernig á að skrá kostnaðinn í bókunum og hvernig á að endurgreiða starfsmanninum.</span><span class="sxs-lookup"><span data-stu-id="91686-110">This article explains how to record the expense in the books and how to reimburse the employee.</span></span> <span data-ttu-id="91686-111">Fyrirtækið kann að vera með gátt eða forrit þar sem starfsmenn geta sent inn kostnaðarskýrslur.</span><span class="sxs-lookup"><span data-stu-id="91686-111">Your organization may have a portal or app where employees can submit their expense reports.</span></span>

<span data-ttu-id="91686-112">[!INCLUDE [prod_short](includes/prod_short.md)] er nógu sveigjanlegt til að henta mörgum mismunandi leiðum.</span><span class="sxs-lookup"><span data-stu-id="91686-112">[!INCLUDE [prod_short](includes/prod_short.md)] is flexible enough to suit many different practices.</span></span> <span data-ttu-id="91686-113">Nákvæm reikningsnúmer sem nota á fara eftir stillingum og ferlum fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="91686-113">The exact account numbers to use depends on your organization's configuration and processes.</span></span>  

## <a name="to-record-an-employees-expense"></a><span data-ttu-id="91686-114">Skrá útgjöld starfsmanns</span><span class="sxs-lookup"><span data-stu-id="91686-114">To record an employee's expense</span></span>

<span data-ttu-id="91686-115">Útgjöld starfsmanna eru bókuð á síðunni **Færslubók**.</span><span class="sxs-lookup"><span data-stu-id="91686-115">You post employees' expenses on the **General Journal** page.</span></span>

1. <span data-ttu-id="91686-116">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Færslubækur** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="91686-116">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **General Journals**, and then choose the related link.</span></span>  
2. <span data-ttu-id="91686-117">Viðeigandi færslubók keyrsla er opnaður.</span><span class="sxs-lookup"><span data-stu-id="91686-117">Open the relevant general journal batch.</span></span> <span data-ttu-id="91686-118">Frekari upplýsingar, sjá [Vinna með almennar færslubækur](ui-work-general-journals.md).</span><span class="sxs-lookup"><span data-stu-id="91686-118">For more information, see [Working with General Journals](ui-work-general-journals.md).</span></span>
3. <span data-ttu-id="91686-119">Fyllið í reitina eftir þörfum í nýrri færslubókarlínu.</span><span class="sxs-lookup"><span data-stu-id="91686-119">On a new journal line, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    > [!NOTE]
    > [!INCLUDE[journal-showhide-columns-inline-tip](includes/journal-showhide-columns-inline-tip.md)]
4. <span data-ttu-id="91686-120">Endurtakið skref 3 fyrir öll útgjöld sem starfsmaður hefur stofnað til.</span><span class="sxs-lookup"><span data-stu-id="91686-120">Repeat step 3 for all the expenses that the employee has incurred.</span></span>

    > [!TIP]  
    > <span data-ttu-id="91686-121">Ef þú vilt færa inn fleiri kostnaðarlínur fyrir ofan eina mótreikningslínu fyrir bankareikning starfsmanns, skaltu velja gátreitinn **Leggja til afstemmingarupphæð** á línunni fyrir þína keyrslu á síðunni **færslubókakeyrslur**.</span><span class="sxs-lookup"><span data-stu-id="91686-121">If you want to enter multiple expense lines above one balance-account line for the employee's bank account, then select the **Suggest Balancing Amount** check box on the line for your batch on the **General Journal Batches** page.</span></span> <span data-ttu-id="91686-122">Þá verður reiturinn **Upphæð** á mótreikningslínunni sjálfkrafa fylltur út með gildinu sem er nauðsynlegt til að jafna útgjöldin.</span><span class="sxs-lookup"><span data-stu-id="91686-122">Then the **Amount** field on the balance-account line is automatically prefilled with the value that is required to balance the expenses.</span></span>
5. <span data-ttu-id="91686-123">Veljið **Bóka** aðgerðina til að skrá útgjöldin á reikning starfsmanns.</span><span class="sxs-lookup"><span data-stu-id="91686-123">Choose the **Post** action to record the expenses on the employee's account.</span></span>

## <a name="to-reimburse-an-employee"></a><span data-ttu-id="91686-124">Endurgreiða starfsmanni</span><span class="sxs-lookup"><span data-stu-id="91686-124">To reimburse an employee</span></span>

<span data-ttu-id="91686-125">Þú endurgreiðir starfsmanni með því að bóka greiðslur á bankareikning hans á síðunni **greiðslubók**.</span><span class="sxs-lookup"><span data-stu-id="91686-125">You reimburse employees by posting payments to their bank account on the **Payment Journal** page.</span></span>  

1. <span data-ttu-id="91686-126">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Greiðslubækur** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="91686-126">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Payment Journals**, and then choose the related link.</span></span>
2. <span data-ttu-id="91686-127">Viðeigandi greiðslubók keyrsla er opnaður.</span><span class="sxs-lookup"><span data-stu-id="91686-127">Open the relevant payment journal batch.</span></span> <span data-ttu-id="91686-128">Frekari upplýsingar, sjá [Vinna með almennar færslubækur](ui-work-general-journals.md).</span><span class="sxs-lookup"><span data-stu-id="91686-128">For more information, see [Working with General Journals](ui-work-general-journals.md).</span></span>
3. <span data-ttu-id="91686-129">Fyllið inn í reitina eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="91686-129">Fill in the fields as necessary.</span></span> <span data-ttu-id="91686-130">Frekari upplýsingar eru í [Greiðslur framkvæmdar](payables-make-payments.md).</span><span class="sxs-lookup"><span data-stu-id="91686-130">For more information, see [Making Payments](payables-make-payments.md).</span></span>
4. <span data-ttu-id="91686-131">Að öðrum kosti skal velja **Leggja til starfsmannagreiðslu** aðgerðina til að setja sjálfvirkt inn færslubókarlínu fyrir endurgreiðslu í bið til starfsmanns.</span><span class="sxs-lookup"><span data-stu-id="91686-131">Alternatively, choose the **Suggest Employee Payment** action to automatically insert journal lines for pending employee reimbursements.</span></span>
5. <span data-ttu-id="91686-132">Valið er **bóka** aðgerð til að skrá endurgreiðsluna.</span><span class="sxs-lookup"><span data-stu-id="91686-132">Choose the **Post** action to register the reimbursement.</span></span>  

## <a name="to-reconcile-reimbursements-with-employee-ledger-entries"></a><span data-ttu-id="91686-133">Afstemma endurgreiðslur við fjárhagsfærslur starfsmanns</span><span class="sxs-lookup"><span data-stu-id="91686-133">To reconcile reimbursements with employee ledger entries</span></span>

<span data-ttu-id="91686-134">Þú jafnar greiðslu til starfsmanns við tengdar og opnar fjárhagsfærslur starfsmanns á sama hátt og greiðslur til lánardrottins, til dæmis á síðunni **Greiðsluafstemmingarbók**, byggt á tengdum bankayfirlitsfærslum.</span><span class="sxs-lookup"><span data-stu-id="91686-134">You apply employee payments to their related open employee ledger entries in the same way as you do for vendor payments, for example on the **Payment Reconciliation Journal** page, based on the related bank statement entries.</span></span> <span data-ttu-id="91686-135">Nánari upplýsingar er að finna í [Jafna greiðslur sjálfkrafa og afstemma bankareikninga](receivables-apply-payments-auto-reconcile-bank-accounts.md).</span><span class="sxs-lookup"><span data-stu-id="91686-135">For more information, see [Applying Payments Automatically and Reconciling Bank Accounts](receivables-apply-payments-auto-reconcile-bank-accounts.md).</span></span> <span data-ttu-id="91686-136">Einnig er hægt að jafna handvirkt á síðunni **Fjárhagsfærslur starfsmanna**.</span><span class="sxs-lookup"><span data-stu-id="91686-136">Alternatively, you can apply manually on the **Employee Ledger Entries** page.</span></span> <span data-ttu-id="91686-137">Frekari upplýsingar er að finna í [Afstemma greiðslu lánardrottins með greiðslubók eða úr færslum í lánardrottnabók](payables-how-apply-purchase-transactions-manually.md).</span><span class="sxs-lookup"><span data-stu-id="91686-137">For more information, see the related [Reconcile Vendor Payments with the Payment Journal or from Vendor Ledger Entries](payables-how-apply-purchase-transactions-manually.md).</span></span>  

## <a name="see-also"></a><span data-ttu-id="91686-138">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="91686-138">See Also</span></span>

[<span data-ttu-id="91686-139">Bóka færslu beint í Fjárhag</span><span class="sxs-lookup"><span data-stu-id="91686-139">Post Transactions Directly to the General Ledger</span></span>](finance-how-post-transactions-directly.md)  
[<span data-ttu-id="91686-140">Vinna í færslubókum</span><span class="sxs-lookup"><span data-stu-id="91686-140">Working with General Journals</span></span>](ui-work-general-journals.md)  
[<span data-ttu-id="91686-141">Bakfæra bókanir í færslubók og afturkalla kvittanir/sendingar</span><span class="sxs-lookup"><span data-stu-id="91686-141">Reverse Journal Postings and Undo Receipts/Shipments</span></span>](finance-how-reverse-journal-posting.md)  
[<span data-ttu-id="91686-142">Fjármál</span><span class="sxs-lookup"><span data-stu-id="91686-142">Finance</span></span>](finance.md)  
<span data-ttu-id="91686-143">[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="91686-143">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  


[!INCLUDE[footer-include](includes/footer-banner.md)]