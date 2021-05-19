---
title: Flytja bankainnstæður
description: Þú getur millifært upphæðir frá einum bankareikningi til annars, meðal annars í ólíkum gjaldmiðlum, með því að bóka millifærsluna í færslubókina.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bank account transfer, multiple currencies
ms.date: 04/29/2021
ms.author: edupont
ms.openlocfilehash: da9c8711751040cecb267a3b2209bad2534b618b
ms.sourcegitcommit: 08ca5798cf3f04fc3ea38fff40c1860196a70adf
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/06/2021
ms.locfileid: "5985388"
---
# <a name="transfer-bank-funds"></a><span data-ttu-id="d8599-103">Flytja bankainnstæður</span><span class="sxs-lookup"><span data-stu-id="d8599-103">Transfer Bank Funds</span></span>

<span data-ttu-id="d8599-104">Stundum þarf að millifæra upphæð af einum bankareikningi í [!INCLUDE[prod_short](includes/prod_short.md)] yfir á annan.</span><span class="sxs-lookup"><span data-stu-id="d8599-104">You may sometimes need to transfer an amount from one bank account in [!INCLUDE[prod_short](includes/prod_short.md)] to another.</span></span> <span data-ttu-id="d8599-105">Til að gera þetta verður að bóka færsluna á síðunni **Færslubók**.</span><span class="sxs-lookup"><span data-stu-id="d8599-105">To do this, you must post the transaction on the **General Journal** page.</span></span> <span data-ttu-id="d8599-106">Verkið er misjafnt eftir því hvort bankareikningarnir nota sama gjaldmiðil eða mismunandi gjaldmiðla.</span><span class="sxs-lookup"><span data-stu-id="d8599-106">The task varies depending on whether the bank accounts use the same currency or different currencies.</span></span>

## <a name="to-post-a-transfer-between-bank-accounts-with-the-same-currency-code"></a><span data-ttu-id="d8599-107">Millifærslur af einum bankareikningi á annan með sama gjaldmiðilskóða</span><span class="sxs-lookup"><span data-stu-id="d8599-107">To post a transfer between bank accounts with the same currency code</span></span>

1. <span data-ttu-id="d8599-108">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Færslubók** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="d8599-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **General Journal**, and then choose the related link.</span></span>
2. <span data-ttu-id="d8599-109">Reitirnir **Bókunardagsetning** og **Númer fylgiskjals** eru fylltir út í færslubókarlínu.</span><span class="sxs-lookup"><span data-stu-id="d8599-109">On a journal line, fill in the **Posting Date** and **Document No.** fields.</span></span>
3. <span data-ttu-id="d8599-110">Í reitnum **Tegund reiknings** er valinn **Bankareikningur**.</span><span class="sxs-lookup"><span data-stu-id="d8599-110">In the **Account Type** field, select **Bank Account**.</span></span>
4. <span data-ttu-id="d8599-111">Í reitnum **Reikningur númer** skal velja bankann sem flytja á bankainnistæðuna frá.</span><span class="sxs-lookup"><span data-stu-id="d8599-111">In the **Account No.** field, select the bank from which you want to transfer the funds.</span></span>
5. <span data-ttu-id="d8599-112">Heildarupphæðin sem á að úthluta í reitinn  **Upphæð** er færð inn.</span><span class="sxs-lookup"><span data-stu-id="d8599-112">In the **Amount** field, enter the amount to be transferred.</span></span>

    <span data-ttu-id="d8599-113">Næst þarf að tilgreina mótreikninginn.</span><span class="sxs-lookup"><span data-stu-id="d8599-113">Next, you must specify the balancing account.</span></span> <span data-ttu-id="d8599-114">Ef þú sérð ekki viðkomandi svæði skaltu velja aðgerðina **Sýna fleiri dálka** til að skoða öll tiltæk svæði.</span><span class="sxs-lookup"><span data-stu-id="d8599-114">If you can't see the relevant fields, then choose the **Show More Columns** action to view all available fields.</span></span>
6. <span data-ttu-id="d8599-115">Í reitnum **Tegund mótreiknings** er **Bankareikningur** valinn.</span><span class="sxs-lookup"><span data-stu-id="d8599-115">In the **Bal. Account Type** field, select **Bank Account**.</span></span>
7. <span data-ttu-id="d8599-116">Í reitnum **Mótreikningur númer** skal velja bankareikninginn sem flytja á bankainnistæðuna til.</span><span class="sxs-lookup"><span data-stu-id="d8599-116">In the **Bal. Account No.** field, select the bank account to which you want to transfer the funds.</span></span>
8. <span data-ttu-id="d8599-117">Bóka skal færslubókina.</span><span class="sxs-lookup"><span data-stu-id="d8599-117">Post the journal.</span></span>

## <a name="to-post-a-transfer-between-bank-accounts-with-different-currency-codes"></a><span data-ttu-id="d8599-118">Færslur milli bankareikninga bókaðar með gjaldmiðilskótum</span><span class="sxs-lookup"><span data-stu-id="d8599-118">To post a transfer between bank accounts with different currency codes</span></span>

<span data-ttu-id="d8599-119">Til að færa fjármuni milli bankareikninga sem nota mismunandi gjaldmiðla, verður að bóka tvær færslubókarlínur.</span><span class="sxs-lookup"><span data-stu-id="d8599-119">To transfer funds between bank accounts that use different currencies, you must post two general journal lines.</span></span>

1. <span data-ttu-id="d8599-120">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Færslubók** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="d8599-120">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **General Journal**, and then choose the related link.</span></span>
2. <span data-ttu-id="d8599-121">Búið til tvær færslubókarlínur og fyllið út reitina **Bókunardagsetning** og **Númer fylgiskjals**.</span><span class="sxs-lookup"><span data-stu-id="d8599-121">Create two journal lines, and fill in the **Posting Date** and **Document No.** fields.</span></span>
3. <span data-ttu-id="d8599-122">Í fyrstu færslubókarlínunni skal færa inn **Bankareikningur** í reitnum **Tegund reiknings**.</span><span class="sxs-lookup"><span data-stu-id="d8599-122">On the first journal line, in the **Type** field, select **Bank Account**.</span></span>
4. <span data-ttu-id="d8599-123">Í reitnum **Reikningur númer** skal velja bankann sem flytja á bankainnistæðuna frá.</span><span class="sxs-lookup"><span data-stu-id="d8599-123">In the **Account No.** field, select the bank account from which you want to transfer the funds.</span></span>
5. <span data-ttu-id="d8599-124">Upphæðin er færð í reitinn **Upphæð** í gjaldmiðli bankareikningsins með eða án mínusmerkis.</span><span class="sxs-lookup"><span data-stu-id="d8599-124">In the **Amount** field, enter the amount in the currency of the bank account with or without a minus sign.</span></span>

    > [!TIP]
    > <span data-ttu-id="d8599-125">Upphæð með engu merki er debet og upphæð með mínusmerki er kreditupphæð.</span><span class="sxs-lookup"><span data-stu-id="d8599-125">An amount without a sign is a debit, and an amount with a minus sign is a credit.</span></span>

    > [!NOTE]
    > <span data-ttu-id="d8599-126">Sum fyrirtæki kjósa frekar að færa milli reikninga til að aðskilja færslubókarlínur.</span><span class="sxs-lookup"><span data-stu-id="d8599-126">Some companies prefer to transfer between accounts on separate journal lines.</span></span> <span data-ttu-id="d8599-127">Önnur fyrirtæki kjósa að bóka allt á einni færslubókarlínu með því að nota mótreikning.</span><span class="sxs-lookup"><span data-stu-id="d8599-127">Other companies prefer to post everything on one journal line by using a balancing account.</span></span> <span data-ttu-id="d8599-128">Hafðu samband við sérfræðing á staðnum ef þú ert ekki viss um hvað á að gera.</span><span class="sxs-lookup"><span data-stu-id="d8599-128">Check with your local expert if you're not sure what to do.</span></span>
    >
    > <span data-ttu-id="d8599-129">Ef fyrirtækið þitt kýs að nota mótreikning skaltu stilla reitinn **Tegund mótreiknings** á **Bankareikningur** og stilla **Númer mótreiknings** á bankareikninginn sem færa á fjármunina yfir á.</span><span class="sxs-lookup"><span data-stu-id="d8599-129">If your company prefers to use a balancing account, then set the **Bal. Account Type** field to **Bank Account**, and set the **Bal. Account No.** field to the bank account to which you want to transfer the funds.</span></span> <span data-ttu-id="d8599-130">Haltu síðan áfram í skref 9 eða 10.</span><span class="sxs-lookup"><span data-stu-id="d8599-130">Then proceed to step 9 or 10.</span></span>
    >
    > <span data-ttu-id="d8599-131">Ef fyrirtækið þitt kýs að nota aðskilda færslubókarlínu skaltu fara í næsta skref.</span><span class="sxs-lookup"><span data-stu-id="d8599-131">If your company prefers to use a separate journal line, then move on to the next step.</span></span>
6. <span data-ttu-id="d8599-132">Í seinni færslubókarlínunni skal færa inn **Bankareikningur** í reitnum **Tegund reiknings**.</span><span class="sxs-lookup"><span data-stu-id="d8599-132">On the second journal line, in the **Type** field, select **Bank Account**.</span></span>
7. <span data-ttu-id="d8599-133">Í reitnum **Reikningur númer** skal velja bankareikninginn sem flytja á bankainnistæðuna til.</span><span class="sxs-lookup"><span data-stu-id="d8599-133">In the **Account No.** field, select the bank account to which you want to transfer the funds.</span></span>
8. <span data-ttu-id="d8599-134">Upphæðin er færð í reitinn **Upphæð** í gjaldmiðli bankareikningsins með eða án mínusmerkis.</span><span class="sxs-lookup"><span data-stu-id="d8599-134">In the **Amount** field, enter the amount in the currency of the bank account with or without a minus sign.</span></span>

    > [!TIP]
    > <span data-ttu-id="d8599-135">Upphæð með engu merki er debet og upphæð með mínusmerki er kreditupphæð.</span><span class="sxs-lookup"><span data-stu-id="d8599-135">An amount without a sign is a debit, and an amount with a minus sign is a credit.</span></span>
9. <span data-ttu-id="d8599-136">Ef gengið sem notað er í færslunni er annað en gengið á síðunni **Gengi gjaldmiðils** þarf að bæta inn nýrri færslubókarlínu fyrir gengishagnað eða -tap.</span><span class="sxs-lookup"><span data-stu-id="d8599-136">If the exchange rates used in the journal are different than the exchange rates on the **Currency Exchange Rates** page, enter a new journal line for the exchange rate gain or loss.</span></span>  

    1. <span data-ttu-id="d8599-137">Færið inn **Fjárhagsreikning** í reitnum **Tegund reiknings**.</span><span class="sxs-lookup"><span data-stu-id="d8599-137">Enter **G/L Account** in the **Account Type** field.</span></span>  

    2. <span data-ttu-id="d8599-138">Færið inn fjárhagsreikningsnúmer fyrir gengishagnað eða -tap í reitinn **Reikningur nr.**.</span><span class="sxs-lookup"><span data-stu-id="d8599-138">Enter the G/L account number for exchange rate gain or loss in the **Account No.** field.</span></span>  

    3. <span data-ttu-id="d8599-139">Færið inn gengishagnað eða -tap í reitinn **Upphæð** með eða án mínusmerkis.</span><span class="sxs-lookup"><span data-stu-id="d8599-139">Enter the exchange rate gain or loss in the **Amount** field with or without a minus sign.</span></span>

    > [!TIP]
    > <span data-ttu-id="d8599-140">Upphæð með engu merki er debet og upphæð með mínusmerki er kreditupphæð.</span><span class="sxs-lookup"><span data-stu-id="d8599-140">An amount without a sign is a debit, and an amount with a minus sign is a credit.</span></span>
10. <span data-ttu-id="d8599-141">Bóka skal færslubókina.</span><span class="sxs-lookup"><span data-stu-id="d8599-141">Post the journal.</span></span>

## <a name="see-also"></a><span data-ttu-id="d8599-142">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="d8599-142">See Also</span></span>

[<span data-ttu-id="d8599-143">Afstemming bankareikninga</span><span class="sxs-lookup"><span data-stu-id="d8599-143">Reconciling Bank Accounts</span></span>](bank-manage-bank-accounts.md)  
[<span data-ttu-id="d8599-144">Uppsetning bankaþjónustu</span><span class="sxs-lookup"><span data-stu-id="d8599-144">Setting Up Banking</span></span>](bank-setup-banking.md)  
[<span data-ttu-id="d8599-145">Vinna í færslubókum</span><span class="sxs-lookup"><span data-stu-id="d8599-145">Working with General Journals</span></span>](ui-work-general-journals.md)  
<span data-ttu-id="d8599-146">[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="d8599-146">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]