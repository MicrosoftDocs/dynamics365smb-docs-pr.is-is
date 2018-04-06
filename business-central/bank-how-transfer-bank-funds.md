---
title: "Flytja bankasjóði| Microsoft Docs"
description: "Þú getur millifært upphæðir frá einum bankareikningi til annars, meðal annars í ólíkum gjaldmiðlum, með því að bóka millifærsluna í færslubókina."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bank account transfer, multiple currencies
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 54e8a7bf7ca8761d6317b57d45e64f9ee628f4b8
ms.contentlocale: is-is
ms.lasthandoff: 03/22/2018

---
# <a name="transfer-bank-funds"></a><span data-ttu-id="f97b2-103">Flytja bankainnstæður</span><span class="sxs-lookup"><span data-stu-id="f97b2-103">Transfer Bank Funds</span></span>
<span data-ttu-id="f97b2-104">Stundum þarf að bóka millifærslu á upphæðum af einum bankareikningi yfir á annan.</span><span class="sxs-lookup"><span data-stu-id="f97b2-104">You may sometimes need to transfer an amount from one bank account to another.</span></span> <span data-ttu-id="f97b2-105">Til að gera þetta verður að bóka á færslu í færslubók.</span><span class="sxs-lookup"><span data-stu-id="f97b2-105">To do this, you must post the a transaction in the general journal.</span></span> <span data-ttu-id="f97b2-106">Verkið er misjafnt eftir því hvort bankareikningarnir nota sama gjaldmiðil eða mismunandi gjaldmiðla.</span><span class="sxs-lookup"><span data-stu-id="f97b2-106">The task varies depending on whether the bank accounts use the same currency or different currencies.</span></span>

## <a name="to-post-a-transfer-between-bank-accounts-with-the-same-currency-code"></a><span data-ttu-id="f97b2-107">Millifærslur af einum bankareikningi á annan með sama gjaldmiðilskóða</span><span class="sxs-lookup"><span data-stu-id="f97b2-107">To post a transfer between bank accounts with the same currency code</span></span>
1. <span data-ttu-id="f97b2-108">Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **færslubók** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="f97b2-108">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **General Journal**, and then choose the related link.</span></span>
2. <span data-ttu-id="f97b2-109">Reitirnir **Bókunardagsetning** og **Númer fylgiskjals** eru fylltir út í færslubókarlínu.</span><span class="sxs-lookup"><span data-stu-id="f97b2-109">On a journal line, fill in the **Posting Date** and **Document No.** fields.</span></span>
3. <span data-ttu-id="f97b2-110">Í reitnum **Tegund reiknings** er valinn **Bankareikningur**.</span><span class="sxs-lookup"><span data-stu-id="f97b2-110">In the **Account Type** field, select **Bank Account**.</span></span>
4. <span data-ttu-id="f97b2-111">Í reitnum **Reikningur númer** skal velja bankann sem flytja á bankainnistæðuna frá.</span><span class="sxs-lookup"><span data-stu-id="f97b2-111">In the **Account No.** field, select the bank from which you want to transfer the funds.</span></span>
5. <span data-ttu-id="f97b2-112">Heildarupphæðin sem á að úthluta í reitinn  **Upphæð** er færð inn.</span><span class="sxs-lookup"><span data-stu-id="f97b2-112">In the **Amount** field, enter the amount to be transferred.</span></span>
6. <span data-ttu-id="f97b2-113">Í reitnum **Tegund mótreiknings** er **Bankareikningur** valinn.</span><span class="sxs-lookup"><span data-stu-id="f97b2-113">In the **Bal. Account Type** field, select **Bank Account**.</span></span>
7. <span data-ttu-id="f97b2-114">Í reitnum **Mótreikningur númer** skal velja bankareikninginn sem flytja á bankainnistæðuna til.</span><span class="sxs-lookup"><span data-stu-id="f97b2-114">In the **Bal. Account No.** field, select the bank account to which you want to transfer the funds.</span></span>
8. <span data-ttu-id="f97b2-115">Bóka skal færslubókina.</span><span class="sxs-lookup"><span data-stu-id="f97b2-115">Post the journal.</span></span>

## <a name="to-post-a-transfer-between-bank-accounts-with-different-currency-codes"></a><span data-ttu-id="f97b2-116">Færslur milli bankareikninga bókaðar með gjaldmiðilskótum</span><span class="sxs-lookup"><span data-stu-id="f97b2-116">To post a transfer between bank accounts with different currency codes</span></span>
<span data-ttu-id="f97b2-117">Til að færa fjármuni milli bankareikninga sem nota mismunandi gjaldmiðla, verður að bóka tvær færslubókarlínur.</span><span class="sxs-lookup"><span data-stu-id="f97b2-117">To transfer funds between bank accounts that use different currencies, you must post two general journal lines.</span></span>

1. <span data-ttu-id="f97b2-118">Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **færslubók** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="f97b2-118">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **General Journal**, and then choose the related link.</span></span>
2. <span data-ttu-id="f97b2-119">Búið til tvær færslubókarlínur og fyllið út reitina **Bókunardagsetning** og **Númer fylgiskjals**.</span><span class="sxs-lookup"><span data-stu-id="f97b2-119">Create two journal lines, and fill in the **Posting Date** and **Document No.** fields.</span></span>
3. <span data-ttu-id="f97b2-120">Í fyrstu færslubókarlínunni skal færa inn **Bankareikningur** í reitnum **Tegund reiknings**.</span><span class="sxs-lookup"><span data-stu-id="f97b2-120">On the first journal line, in the **Type** field, select **Bank Account**.</span></span>
4. <span data-ttu-id="f97b2-121">Í reitnum **Reikningur númer** skal velja bankann sem flytja á bankainnistæðuna frá.</span><span class="sxs-lookup"><span data-stu-id="f97b2-121">In the **Account No.** field, select the bank account from which you want to transfer the funds.</span></span>
5. <span data-ttu-id="f97b2-122">Í reitnum **Upphæð** er rituð upphæðin sem er í gjaldmiðli bankareiknings.</span><span class="sxs-lookup"><span data-stu-id="f97b2-122">In the **Amount** field, enter the amount in the currency of the bank account.</span></span> <span data-ttu-id="f97b2-123">Færið inn kreditáætlunarupphæð með neikvæðu formerki.</span><span class="sxs-lookup"><span data-stu-id="f97b2-123">Enter credit amounts with a minus sign.</span></span> <span data-ttu-id="f97b2-124">Færið inn debetáætlunarupphæð með neikvæðu formerki.</span><span class="sxs-lookup"><span data-stu-id="f97b2-124">Enter debit amounts without a minus sign.</span></span>
6. <span data-ttu-id="f97b2-125">Í reitnum **Tegund mótreiknings** er **Bankareikningur** valinn.</span><span class="sxs-lookup"><span data-stu-id="f97b2-125">In the **Bal. Account Type** field, select **Bank Account**.</span></span>
7. <span data-ttu-id="f97b2-126">Í reitnum **Mótreikningur númer** skal velja bankareikninginn sem flytja á bankainnistæðuna til.</span><span class="sxs-lookup"><span data-stu-id="f97b2-126">In the **Bal. Account No.** field, select the bank account to which you want to transfer the funds.</span></span>
8. <span data-ttu-id="f97b2-127">Í seinni færslubókarlínunni skal færa inn **Bankareikningur** í reitnum **Tegund reiknings**.</span><span class="sxs-lookup"><span data-stu-id="f97b2-127">On the second journal line, in the **Type** field, select **Bank Account**.</span></span>
9. <span data-ttu-id="f97b2-128">Í reitnum **Reikningur númer** skal velja bankareikninginn sem flytja á bankainnistæðuna til.</span><span class="sxs-lookup"><span data-stu-id="f97b2-128">In the **Account No.** field, select the bank account to which you want to transfer the funds.</span></span>
10. <span data-ttu-id="f97b2-129">Í reitnum **Upphæð** er rituð upphæðin sem er í gjaldmiðli bankareiknings.</span><span class="sxs-lookup"><span data-stu-id="f97b2-129">In the **Amount** field, enter the amount in the currency of the bank account.</span></span> <span data-ttu-id="f97b2-130">Færið inn kreditáætlunarupphæð með neikvæðu formerki.</span><span class="sxs-lookup"><span data-stu-id="f97b2-130">Enter credit amounts with a minus sign.</span></span> <span data-ttu-id="f97b2-131">Færið inn debetáætlunarupphæð með neikvæðu formerki.</span><span class="sxs-lookup"><span data-stu-id="f97b2-131">Enter debit amounts without a minus sign.</span></span>
11. <span data-ttu-id="f97b2-132">Í reitnum **Tegund mótreiknings** er **Bankareikningur** valinn.</span><span class="sxs-lookup"><span data-stu-id="f97b2-132">In the **Bal. Account Type** field, select **Bank Account**.</span></span>  
12. <span data-ttu-id="f97b2-133">Í reitnum **Mótreikningur númer** skal velja bankareikninginn sem flytja á bankainnistæðuna frá.</span><span class="sxs-lookup"><span data-stu-id="f97b2-133">In the **Bal. Account No.** field, select the bank account from which you want to transfer the funds.</span></span>

    > [!NOTE]  
>   <span data-ttu-id="f97b2-134">Ef gengið sem notað er í færslunni er annað en gengið í glugganum **Gengi gjaldmiðils** þarf að bæta inn þriðju línunni fyrir gengishagnað eða -tap.</span><span class="sxs-lookup"><span data-stu-id="f97b2-134">If the exchange rates used in the journal are different than the exchange rates in the **Currency Exchange Rates** window, enter a third line for the exchange rate gain or loss.</span></span> <span data-ttu-id="f97b2-135">Færið inn **Fjárhagsreikning** í reitnum **Tegund reiknings**.</span><span class="sxs-lookup"><span data-stu-id="f97b2-135">Enter **G/L Account** in the **Account Type** field.</span></span> <span data-ttu-id="f97b2-136">Færið inn fjárhagsreikningsnúmer fyrir gengishagnað eða -tap í reitinn **Reikningur nr.**.</span><span class="sxs-lookup"><span data-stu-id="f97b2-136">Enter the G/L account number for exchange rate gain or loss in the **Account No.** field.</span></span> <span data-ttu-id="f97b2-137">Færa inn gengishagnað eða -tap í reitinn **Upphæð** með eða án neikvæðs formerkis, eftir því hvort um er að ræða kreditupphæð eða debetupphæð.</span><span class="sxs-lookup"><span data-stu-id="f97b2-137">Enter the exchange rate gain or loss in the **Amount** field with or without a minus sign for credits and debits respectively.</span></span>
13. <span data-ttu-id="f97b2-138">Bóka skal færslubókina.</span><span class="sxs-lookup"><span data-stu-id="f97b2-138">Post the journal.</span></span>

## <a name="see-also"></a><span data-ttu-id="f97b2-139">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="f97b2-139">See Also</span></span>
[<span data-ttu-id="f97b2-140">Stjórna bankareikningum</span><span class="sxs-lookup"><span data-stu-id="f97b2-140">Managing Bank Accounts</span></span>](bank-manage-bank-accounts.md)  
[<span data-ttu-id="f97b2-141">Uppsetning bankaþjónustu</span><span class="sxs-lookup"><span data-stu-id="f97b2-141">Setting Up Banking</span></span>](bank-setup-banking.md)  
[<span data-ttu-id="f97b2-142">Vinna í færslubókum</span><span class="sxs-lookup"><span data-stu-id="f97b2-142">Working with General Journals</span></span>](ui-work-general-journals.md)  
<span data-ttu-id="f97b2-143">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="f97b2-143">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

