---
title: "Skrá og endurgreiða útgjöld starfsmanna í viðskiptaerindum | Microsoft Docs"
description: "Bóka útgjöld starfsmanna með færslubók á reikning starfsmanns og bóka síðar greiðslu á bankareikning starfsmanns til að endurgreiða útgjöld í viðskiptaerindum."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reimbursement
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 75e2615dfd7af8ec6269affb0a61f75adf1c6d97
ms.contentlocale: is-is
ms.lasthandoff: 09/28/2018

---
# <a name="record-and-reimburse-employees-expenses"></a><span data-ttu-id="71064-103">Skrá og endurgreiða starfsmannaútgjöld</span><span class="sxs-lookup"><span data-stu-id="71064-103">Record and Reimburse Employees' Expenses</span></span>
[!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="71064-104">styður færslur fyrir starfsmann á svipaðan hátt og fyrir lánardrottna.</span><span class="sxs-lookup"><span data-stu-id="71064-104">supports transactions for employee in a similar way as for vendors.</span></span> <span data-ttu-id="71064-105">Til eru bókunarflokkar starfsmanna, sem eiga að tryggja að fjárhagsfærslur starfsmanna séu bókaðar á viðeigandi reikninga í færslubókinni.</span><span class="sxs-lookup"><span data-stu-id="71064-105">Accordingly, employee posting groups exist to make sure that employee ledger entries are posted to the relevant accounts in the general ledger.</span></span>

> [!NOTE]  
> <span data-ttu-id="71064-106">Starfsmannafærslur er eingöngu hægt að bóka í staðbundna gjaldmiðlinum.</span><span class="sxs-lookup"><span data-stu-id="71064-106">Employee transactions can be posted in the local currency only.</span></span> <span data-ttu-id="71064-107">Endurgreiðslur til starfsmanna styðja ekki aflsætti og greiðsluvikmörk.</span><span class="sxs-lookup"><span data-stu-id="71064-107">Reimbursement payments to employees do not support discounts and payment tolerances.</span></span>

<span data-ttu-id="71064-108">Ef starfsmenn eyða sínum eigin peningum í viðskiptaerindum, er hægt að bóka útgjöldin á reikning starfsmanns.</span><span class="sxs-lookup"><span data-stu-id="71064-108">If employees spend their own money during business activities, you can post the expense to the employee's account.</span></span> <span data-ttu-id="71064-109">Þá geturðu endurgreitt starfsmanninum með því að framkvæma greiðslu inn á bankareikning starfsmannsins, á svipaðan hátt og þú borgar lánardrottnum.</span><span class="sxs-lookup"><span data-stu-id="71064-109">Then you can reimburse the employee by making a payment to the employee's bank account, similarly to how you pay vendors.</span></span>

## <a name="to-record-an-employees-expense"></a><span data-ttu-id="71064-110">Skrá útgjöld starfsmanns</span><span class="sxs-lookup"><span data-stu-id="71064-110">To record an employee's expense</span></span>
<span data-ttu-id="71064-111">Útgjöld starfsmanna eru bókuð í **Færslubók** glugga</span><span class="sxs-lookup"><span data-stu-id="71064-111">You post employees' expenses in the **General Journal** window.</span></span>
1. <span data-ttu-id="71064-112">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Færslubækur** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="71064-112">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **General Journals**, and then choose the related link.</span></span>
2. <span data-ttu-id="71064-113">Viðeigandi færslubók keyrsla er opnaður.</span><span class="sxs-lookup"><span data-stu-id="71064-113">Open the relevant general journal batch.</span></span> <span data-ttu-id="71064-114">Frekari upplýsingar, sjá [Vinna með almennar færslubækur](ui-work-general-journals.md).</span><span class="sxs-lookup"><span data-stu-id="71064-114">For more information, see [Working with General Journals](ui-work-general-journals.md).</span></span>
3. <span data-ttu-id="71064-115">Fyllið í reitina eftir þörfum í nýrri færslubókarlínu.</span><span class="sxs-lookup"><span data-stu-id="71064-115">On a new journal line, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]    
4. <span data-ttu-id="71064-116">Endurtakið skref 3 fyrir öll útgjöld sem starfsmaður hefur stofnað til.</span><span class="sxs-lookup"><span data-stu-id="71064-116">Repeat step 3 for all the expenses that the employee has incurred.</span></span>

    > [!TIP]  
    > <span data-ttu-id="71064-117">Ef þú vilt færa inn fleiri kostnaðarlínur fyrir ofan eina mótreikningslínu fyrir bankareikning starfsmanns, skaltu velja gátreitinn **Leggja til afstemmingarupphæð** á línunni fyrir þína keyrslu í glugganum **færslubókakeyrslur**.</span><span class="sxs-lookup"><span data-stu-id="71064-117">If you want to enter multiple expense lines above one balance-account line for the employee's bank account, then select the **Suggest Balancing Amount** check box on the line for your batch in the **General Journal Batches** window.</span></span> <span data-ttu-id="71064-118">Þá verður reiturinn **Upphæð** á mótreikningslínunni sjálfkrafa fylltur út með gildinu sem er nauðsynlegt til að jafna útgjöldin.</span><span class="sxs-lookup"><span data-stu-id="71064-118">Then the **Amount** field on the balance-account line is automatically prefilled with the value that is required to balance the expenses.</span></span>
5. <span data-ttu-id="71064-119">Veljið **Bóka** aðgerðina til að skrá útgjöldin á reikning starfsmanns.</span><span class="sxs-lookup"><span data-stu-id="71064-119">Choose the **Post** action to record the expenses on the employee's account.</span></span>

## <a name="to-reimburse-an-employee"></a><span data-ttu-id="71064-120">Endurgreiða starfsmanni</span><span class="sxs-lookup"><span data-stu-id="71064-120">To reimburse an employee</span></span>
<span data-ttu-id="71064-121">Þú endurgreiðir starfsmanni með því að bóka greiðslur á bankareikning hans í glugganum **greiðslubók**.</span><span class="sxs-lookup"><span data-stu-id="71064-121">You reimburse employees by posting payments to their bank account in the **Payment Journal** window.</span></span>
1. <span data-ttu-id="71064-122">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **greiðslubók** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="71064-122">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Payment Journals**, and then choose the related link.</span></span>
2. <span data-ttu-id="71064-123">Viðeigandi greiðslubók keyrsla er opnaður.</span><span class="sxs-lookup"><span data-stu-id="71064-123">Open the relevant payment journal batch.</span></span> <span data-ttu-id="71064-124">Frekari upplýsingar, sjá [Vinna með almennar færslubækur](ui-work-general-journals.md).</span><span class="sxs-lookup"><span data-stu-id="71064-124">For more information, see [Working with General Journals](ui-work-general-journals.md).</span></span>
3. <span data-ttu-id="71064-125">Fyllið inn í reitina eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="71064-125">Fill in the fields as necessary.</span></span> <span data-ttu-id="71064-126">Frekari upplýsingar eru í [Greiðslur framkvæmdar](payables-make-payments.md).</span><span class="sxs-lookup"><span data-stu-id="71064-126">For more information, see [Making Payments](payables-make-payments.md).</span></span>
4. <span data-ttu-id="71064-127">Að öðrum kosti skal velja **Leggja til starfsmannagreiðslu** aðgerðina til að setja sjálfvirkt inn færslubókarlínu fyrir endurgreiðslu í bið til starfsmanns.</span><span class="sxs-lookup"><span data-stu-id="71064-127">Alternatively, choose the **Suggest Employee Payment** action to automatically insert journal lines for pending employee reimbursements.</span></span>
5. <span data-ttu-id="71064-128">Valið er **bóka** aðgerð til að skrá endurgreiðsluna.</span><span class="sxs-lookup"><span data-stu-id="71064-128">Choose the **Post** action to register the reimbursement.</span></span>  

## <a name="to-reconcile-reimbursements-with-employee-ledger-entries"></a><span data-ttu-id="71064-129">Afstemma endurgreiðslur við fjárhagsfærslur starfsmanns</span><span class="sxs-lookup"><span data-stu-id="71064-129">To reconcile reimbursements with employee ledger entries</span></span>
<span data-ttu-id="71064-130">Þú jafnar greiðslu til starfsmanns við tengdar og opnar fjárhagsfærslur starfsmanns á sama hátt og greiðslur til lánardrottins, til dæmis í glugganum **Greiðsluafstemmingarbók**, byggt á tengdum bankayfirlitsfærslum.</span><span class="sxs-lookup"><span data-stu-id="71064-130">You apply employee payments to their related open employee ledger entries in the same way as you do for vendor payments, for example in the **Payment Reconciliation Journal** window, based on the related bank statement entries.</span></span> <span data-ttu-id="71064-131">Nánari upplýsingar er að finna í [Jafna greiðslur sjálfkrafa og afstemma bankareikninga](receivables-apply-payments-auto-reconcile-bank-accounts.md).</span><span class="sxs-lookup"><span data-stu-id="71064-131">For more information, see [Applying Payments Automatically and Reconciling Bank Accounts](receivables-apply-payments-auto-reconcile-bank-accounts.md).</span></span> <span data-ttu-id="71064-132">Einnig er hægt að jafna handvirkt í glugganum **Fjárhagsfærslur starfsmanna**.</span><span class="sxs-lookup"><span data-stu-id="71064-132">Alternatively, you can apply manually in the **Employee Ledger Entries** window.</span></span> <span data-ttu-id="71064-133">Frekari upplýsingar, sjá [Afstemma greiðslu lánardrottinss handvirkt](payables-how-apply-purchase-transactions-manually.md).</span><span class="sxs-lookup"><span data-stu-id="71064-133">For more information, see the related [Reconcile Vendor Payments Manually](payables-how-apply-purchase-transactions-manually.md).</span></span>  

## <a name="see-also"></a><span data-ttu-id="71064-134">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="71064-134">See Also</span></span>
[<span data-ttu-id="71064-135">Bóka færslu beint í Fjárhag</span><span class="sxs-lookup"><span data-stu-id="71064-135">Post Transactions Directly to the General Ledger</span></span>](finance-how-post-transactions-directly.md)  
[<span data-ttu-id="71064-136">Vinna í færslubókum</span><span class="sxs-lookup"><span data-stu-id="71064-136">Working with General Journals</span></span>](ui-work-general-journals.md)  
[<span data-ttu-id="71064-137">Bakfæra bókanir</span><span class="sxs-lookup"><span data-stu-id="71064-137">Reverse Postings</span></span>](finance-how-reverse-journal-posting.md)  
[<span data-ttu-id="71064-138">Fjármál</span><span class="sxs-lookup"><span data-stu-id="71064-138">Finance</span></span>](finance.md)  
<span data-ttu-id="71064-139">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="71064-139">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

