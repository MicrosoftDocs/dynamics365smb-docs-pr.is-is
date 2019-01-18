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
ms.date: 11/18/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: 486196d228d9a19d6fbba1e171e138bd5693ac94
ms.contentlocale: is-is
ms.lasthandoff: 11/26/2018

---
# <a name="transfer-bank-funds"></a><span data-ttu-id="14adc-103">Flytja bankainnstæður</span><span class="sxs-lookup"><span data-stu-id="14adc-103">Transfer Bank Funds</span></span>
<span data-ttu-id="14adc-104">Stundum þarf að bóka millifærslu á upphæðum af einum bankareikningi yfir á annan.</span><span class="sxs-lookup"><span data-stu-id="14adc-104">You may sometimes need to transfer an amount from one bank account to another.</span></span> <span data-ttu-id="14adc-105">Til að gera þetta verður að bóka á færslu í færslubók.</span><span class="sxs-lookup"><span data-stu-id="14adc-105">To do this, you must post the a transaction in the general journal.</span></span> <span data-ttu-id="14adc-106">Verkið er misjafnt eftir því hvort bankareikningarnir nota sama gjaldmiðil eða mismunandi gjaldmiðla.</span><span class="sxs-lookup"><span data-stu-id="14adc-106">The task varies depending on whether the bank accounts use the same currency or different currencies.</span></span>

## <a name="to-post-a-transfer-between-bank-accounts-with-the-same-currency-code"></a><span data-ttu-id="14adc-107">Millifærslur af einum bankareikningi á annan með sama gjaldmiðilskóða</span><span class="sxs-lookup"><span data-stu-id="14adc-107">To post a transfer between bank accounts with the same currency code</span></span>
1. <span data-ttu-id="14adc-108">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **færslubók** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="14adc-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **General Journal**, and then choose the related link.</span></span>
2. <span data-ttu-id="14adc-109">Reitirnir **Bókunardagsetning** og **Númer fylgiskjals** eru fylltir út í færslubókarlínu.</span><span class="sxs-lookup"><span data-stu-id="14adc-109">On a journal line, fill in the **Posting Date** and **Document No.** fields.</span></span>
3. <span data-ttu-id="14adc-110">Í reitnum **Tegund reiknings** er valinn **Bankareikningur**.</span><span class="sxs-lookup"><span data-stu-id="14adc-110">In the **Account Type** field, select **Bank Account**.</span></span>
4. <span data-ttu-id="14adc-111">Í reitnum **Reikningur númer** skal velja bankann sem flytja á bankainnistæðuna frá.</span><span class="sxs-lookup"><span data-stu-id="14adc-111">In the **Account No.** field, select the bank from which you want to transfer the funds.</span></span>
5. <span data-ttu-id="14adc-112">Heildarupphæðin sem á að úthluta í reitinn  **Upphæð** er færð inn.</span><span class="sxs-lookup"><span data-stu-id="14adc-112">In the **Amount** field, enter the amount to be transferred.</span></span>
6. <span data-ttu-id="14adc-113">Veljið aðgerðina **Sýna fleiri dálka** til að skoða alla tiltæka reiti.</span><span class="sxs-lookup"><span data-stu-id="14adc-113">Choose the **Show More Columns** action to view all available fields.</span></span>
7. <span data-ttu-id="14adc-114">Í reitnum **Tegund mótreiknings** er **Bankareikningur** valinn.</span><span class="sxs-lookup"><span data-stu-id="14adc-114">In the **Bal. Account Type** field, select **Bank Account**.</span></span>
8. <span data-ttu-id="14adc-115">Í reitnum **Mótreikningur númer** skal velja bankareikninginn sem flytja á bankainnistæðuna til.</span><span class="sxs-lookup"><span data-stu-id="14adc-115">In the **Bal. Account No.** field, select the bank account to which you want to transfer the funds.</span></span>
9. <span data-ttu-id="14adc-116">Bóka skal færslubókina.</span><span class="sxs-lookup"><span data-stu-id="14adc-116">Post the journal.</span></span>

## <a name="to-post-a-transfer-between-bank-accounts-with-different-currency-codes"></a><span data-ttu-id="14adc-117">Færslur milli bankareikninga bókaðar með gjaldmiðilskótum</span><span class="sxs-lookup"><span data-stu-id="14adc-117">To post a transfer between bank accounts with different currency codes</span></span>
<span data-ttu-id="14adc-118">Til að færa fjármuni milli bankareikninga sem nota mismunandi gjaldmiðla, verður að bóka tvær færslubókarlínur.</span><span class="sxs-lookup"><span data-stu-id="14adc-118">To transfer funds between bank accounts that use different currencies, you must post two general journal lines.</span></span>

1. <span data-ttu-id="14adc-119">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **færslubók** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="14adc-119">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **General Journal**, and then choose the related link.</span></span>
2. <span data-ttu-id="14adc-120">Búið til tvær færslubókarlínur og fyllið út reitina **Bókunardagsetning** og **Númer fylgiskjals**.</span><span class="sxs-lookup"><span data-stu-id="14adc-120">Create two journal lines, and fill in the **Posting Date** and **Document No.** fields.</span></span>
3. <span data-ttu-id="14adc-121">Í fyrstu færslubókarlínunni skal færa inn **Bankareikningur** í reitnum **Tegund reiknings**.</span><span class="sxs-lookup"><span data-stu-id="14adc-121">On the first journal line, in the **Type** field, select **Bank Account**.</span></span>
4. <span data-ttu-id="14adc-122">Í reitnum **Reikningur númer** skal velja bankann sem flytja á bankainnistæðuna frá.</span><span class="sxs-lookup"><span data-stu-id="14adc-122">In the **Account No.** field, select the bank account from which you want to transfer the funds.</span></span>
5. <span data-ttu-id="14adc-123">Í reitnum **Upphæð** er rituð upphæðin sem er í gjaldmiðli bankareiknings.</span><span class="sxs-lookup"><span data-stu-id="14adc-123">In the **Amount** field, enter the amount in the currency of the bank account.</span></span> <span data-ttu-id="14adc-124">Færið inn kreditáætlunarupphæð með neikvæðu formerki.</span><span class="sxs-lookup"><span data-stu-id="14adc-124">Enter credit amounts with a minus sign.</span></span> <span data-ttu-id="14adc-125">Færið inn debetáætlunarupphæð með neikvæðu formerki.</span><span class="sxs-lookup"><span data-stu-id="14adc-125">Enter debit amounts without a minus sign.</span></span>
6. <span data-ttu-id="14adc-126">Í reitnum **Tegund mótreiknings** er **Bankareikningur** valinn.</span><span class="sxs-lookup"><span data-stu-id="14adc-126">In the **Bal. Account Type** field, select **Bank Account**.</span></span>
7. <span data-ttu-id="14adc-127">Í reitnum **Mótreikningur númer** skal velja bankareikninginn sem flytja á bankainnistæðuna til.</span><span class="sxs-lookup"><span data-stu-id="14adc-127">In the **Bal. Account No.** field, select the bank account to which you want to transfer the funds.</span></span>
8. <span data-ttu-id="14adc-128">Í seinni færslubókarlínunni skal færa inn **Bankareikningur** í reitnum **Tegund reiknings**.</span><span class="sxs-lookup"><span data-stu-id="14adc-128">On the second journal line, in the **Type** field, select **Bank Account**.</span></span>
9. <span data-ttu-id="14adc-129">Í reitnum **Reikningur númer** skal velja bankareikninginn sem flytja á bankainnistæðuna til.</span><span class="sxs-lookup"><span data-stu-id="14adc-129">In the **Account No.** field, select the bank account to which you want to transfer the funds.</span></span>
10. <span data-ttu-id="14adc-130">Í reitnum **Upphæð** er rituð upphæðin sem er í gjaldmiðli bankareiknings.</span><span class="sxs-lookup"><span data-stu-id="14adc-130">In the **Amount** field, enter the amount in the currency of the bank account.</span></span> <span data-ttu-id="14adc-131">Færið inn kreditáætlunarupphæð með neikvæðu formerki.</span><span class="sxs-lookup"><span data-stu-id="14adc-131">Enter credit amounts with a minus sign.</span></span> <span data-ttu-id="14adc-132">Færið inn debetáætlunarupphæð með neikvæðu formerki.</span><span class="sxs-lookup"><span data-stu-id="14adc-132">Enter debit amounts without a minus sign.</span></span>
11. <span data-ttu-id="14adc-133">Í reitnum **Tegund mótreiknings** er **Bankareikningur** valinn.</span><span class="sxs-lookup"><span data-stu-id="14adc-133">In the **Bal. Account Type** field, select **Bank Account**.</span></span>  
12. <span data-ttu-id="14adc-134">Í reitnum **Mótreikningur númer** skal velja bankareikninginn sem flytja á bankainnistæðuna frá.</span><span class="sxs-lookup"><span data-stu-id="14adc-134">In the **Bal. Account No.** field, select the bank account from which you want to transfer the funds.</span></span>

    > [!NOTE]  
    > <span data-ttu-id="14adc-135">Ef gengið sem notað er í færslunni er annað en gengið á síðunni **Gengi gjaldmiðils** þarf að bæta inn þriðju línunni fyrir gengishagnað eða -tap.</span><span class="sxs-lookup"><span data-stu-id="14adc-135">If the exchange rates used in the journal are different than the exchange rates on the **Currency Exchange Rates** page, enter a third line for the exchange rate gain or loss.</span></span> <span data-ttu-id="14adc-136">Færið inn **Fjárhagsreikning** í reitnum **Tegund reiknings**.</span><span class="sxs-lookup"><span data-stu-id="14adc-136">Enter **G/L Account** in the **Account Type** field.</span></span> <span data-ttu-id="14adc-137">Færið inn fjárhagsreikningsnúmer fyrir gengishagnað eða -tap í reitinn **Reikningur nr.**.</span><span class="sxs-lookup"><span data-stu-id="14adc-137">Enter the G/L account number for exchange rate gain or loss in the **Account No.** field.</span></span> <span data-ttu-id="14adc-138">Færa inn gengishagnað eða -tap í reitinn **Upphæð** með eða án neikvæðs formerkis, eftir því hvort um er að ræða kreditupphæð eða debetupphæð.</span><span class="sxs-lookup"><span data-stu-id="14adc-138">Enter the exchange rate gain or loss in the **Amount** field with or without a minus sign for credits and debits respectively.</span></span>
13. <span data-ttu-id="14adc-139">Bóka skal færslubókina.</span><span class="sxs-lookup"><span data-stu-id="14adc-139">Post the journal.</span></span>

## <a name="see-also"></a><span data-ttu-id="14adc-140">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="14adc-140">See Also</span></span>
[<span data-ttu-id="14adc-141">Stjórna bankareikningum</span><span class="sxs-lookup"><span data-stu-id="14adc-141">Managing Bank Accounts</span></span>](bank-manage-bank-accounts.md)  
[<span data-ttu-id="14adc-142">Uppsetning bankaþjónustu</span><span class="sxs-lookup"><span data-stu-id="14adc-142">Setting Up Banking</span></span>](bank-setup-banking.md)  
[<span data-ttu-id="14adc-143">Vinna í færslubókum</span><span class="sxs-lookup"><span data-stu-id="14adc-143">Working with General Journals</span></span>](ui-work-general-journals.md)  
<span data-ttu-id="14adc-144">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="14adc-144">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

