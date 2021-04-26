---
title: Bóka milli-fyrirtækjaskjöl og færslubækur | Microsoft Docs
description: Notaðu milli-fyrirtækjaskjöl til að bóka viðskipti við MF-félaga.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: IC, group, consolidation, affiliate, subsidiary
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: febd0eec1e5a66354538964d5495e4409c4042f0
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5786174"
---
# <a name="work-with-intercompany-documents-and-journals"></a><span data-ttu-id="bc5a2-103">Unnið með samstæðuskjöl og færslubækur</span><span class="sxs-lookup"><span data-stu-id="bc5a2-103">Work with Intercompany Documents and Journals</span></span>
<span data-ttu-id="bc5a2-104">Milli-fyrirtækjaskjöl eru notuð til að bóka viðskipti við milli-fyrirtækjafélaga.</span><span class="sxs-lookup"><span data-stu-id="bc5a2-104">You use intercompany documents or journals to post transactions with your intercompany partners.</span></span> <span data-ttu-id="bc5a2-105">Þegar milli-fyrirtækjaskjöl eða færslubókarlína eru bókuð í fyrirtækinu er samsvarandi fylgiskjal eða færslubókarlína stofnuð í MF-úthólfinu sem hægt er að flytja til félagans.</span><span class="sxs-lookup"><span data-stu-id="bc5a2-105">When you post an intercompany document or journal line in your company, a corresponding document or journal line is created in your intercompany outbox that you can transfer to your partner.</span></span> <span data-ttu-id="bc5a2-106">Félaginn getur síðan bókað samsvarandi færslu í sínu fyrirtæki án þess að færa gögnin inn aftur.</span><span class="sxs-lookup"><span data-stu-id="bc5a2-106">Your partner can then post the corresponding transaction in their company, without having to re-enter the data.</span></span>

<span data-ttu-id="bc5a2-107">Fyrir sölu- og innkaupskjöl, mun MF-félagakóði tilheyrandi viðskiptamanns eða lánardrottins tryggja að allar pantanir og reikningar sem eiga við færslur til eða frá þessum félögum stofna þaðan í frá samsvarandi skjöl hjá fyrirtækjafélögum svo að staða reikninganna verði rétt.</span><span class="sxs-lookup"><span data-stu-id="bc5a2-107">For sales and purchase documents, the intercompany partner code on the involved customer or vendor ensures that all orders and invoices generated pertaining to transactions with these companies will produce corresponding documents in the partner company, resulting in correct balancing of the accounts.</span></span>

<span data-ttu-id="bc5a2-108">Fyrir MF-færslubókarlínu, þarf ekki að tilgreina reikningana fyrir stök söfn bóka, heldur þarf aðeins að gefa upp kenni samstarfsfyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="bc5a2-108">For intercompany general journal lines, you do not need to specify the accounts for an individual set of books, but simply give the identification of the partner company.</span></span> <span data-ttu-id="bc5a2-109">Samsvarandi MF-færslubókarlínur eru síðan stofnaðar í félagafyrirtækinu sem veldur afstemmingu bóka beggja fyrirtækja sem taka þátt í færslunni.</span><span class="sxs-lookup"><span data-stu-id="bc5a2-109">Corresponding intercompany general journal lines are then created in the partner company that result in the balancing of the books of both companies involved in a transaction.</span></span>

## <a name="to-fill-in-and-send-an-intercompany-sales-order"></a><span data-ttu-id="bc5a2-110">MF-sölupöntun fyllt út og send:</span><span class="sxs-lookup"><span data-stu-id="bc5a2-110">To fill in and send an intercompany sales order</span></span>
<span data-ttu-id="bc5a2-111">Hægt er að senda sölu- og innkaupapantanir og vöruskilapantanir áður en bókað er.</span><span class="sxs-lookup"><span data-stu-id="bc5a2-111">You can send sales and purchase orders and return orders before posting.</span></span> <span data-ttu-id="bc5a2-112">Ekki er hægt að senda reikninga og kreditreikninga fyrr en þeir hafa verið bókaðir.</span><span class="sxs-lookup"><span data-stu-id="bc5a2-112">Invoices and credit memos cannot be sent until they are posted.</span></span>

<span data-ttu-id="bc5a2-113">Eftirfarandi aðferð lýsir því hvernig eigi að fylla út og senda sölupöntun milli fyrirtækja.</span><span class="sxs-lookup"><span data-stu-id="bc5a2-113">The following procedure describes how to fill in and send an intercompany sales order.</span></span> <span data-ttu-id="bc5a2-114">Sömu skref eiga við um sölu- og vöruskilapantanir millifyrirtækis, og bókaða millifyrirtækjareikninga og kreditreikninga.</span><span class="sxs-lookup"><span data-stu-id="bc5a2-114">The same steps apply to intercompany purchase orders and return orders, and to posted intercompany invoices and credit memos.</span></span>  

1. <span data-ttu-id="bc5a2-115">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Sölupantanir** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="bc5a2-115">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Orders**, and then choose the related link.</span></span>  
2. <span data-ttu-id="bc5a2-116">Veljið **Nýtt** til að stofna nýja sölupöntun.</span><span class="sxs-lookup"><span data-stu-id="bc5a2-116">Choose **New** to create a new sales order.</span></span> <span data-ttu-id="bc5a2-117">Frekari upplýsingar eru í [Selja vörur](sales-how-sell-products.md).</span><span class="sxs-lookup"><span data-stu-id="bc5a2-117">For more information, see [Sell Products](sales-how-sell-products.md).</span></span>  
3. <span data-ttu-id="bc5a2-118">Fyllið inn í reitina eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="bc5a2-118">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. <span data-ttu-id="bc5a2-119">Gangið úr skugga um að viðskiptamaðurinn sé milli-fyrirtækjafélagi.</span><span class="sxs-lookup"><span data-stu-id="bc5a2-119">Make sure the customer is an intercompany partner.</span></span>
5. <span data-ttu-id="bc5a2-120">Til að senda sölupöntunina áður en hún er bókuð er valin aðgerðin **Senda MF-sölupöntun**.</span><span class="sxs-lookup"><span data-stu-id="bc5a2-120">To send the sales order before you post it, choose the **Send IC Sales Order** action.</span></span>

> [!NOTE]
> <span data-ttu-id="bc5a2-121">Ef þú framkvæmir skref 4, mun sölupöntunin verða færð yfir til úthólfs millifyrirtækisins þar sem þú getur sent hana síðar.</span><span class="sxs-lookup"><span data-stu-id="bc5a2-121">If you do perform step 4, then the sales order will be moved to your intercompany outbox where you can send it later.</span></span> <span data-ttu-id="bc5a2-122">Frekari upplýsingar er að finna í [Stjórna millifyrirtækja innhólfsfærslur og úthólfsfærslur](intercompany-how-manage-intercompany-inbox.md).</span><span class="sxs-lookup"><span data-stu-id="bc5a2-122">For more information, see [Manage the Intercompany Inbox and Outbox](intercompany-how-manage-intercompany-inbox.md).</span></span>

## <a name="to-fill-in-and-post-an-intercompany-journal"></a><span data-ttu-id="bc5a2-123">Fært í milli-fyrirtækjabækur og bókað</span><span class="sxs-lookup"><span data-stu-id="bc5a2-123">To fill in and post an intercompany journal</span></span>
<span data-ttu-id="bc5a2-124">Þegar bókuð er almenn færslubókarlína í fyrirtækinu, er samsvarandi færslubókarlína stofunuð í MF-úthólfinu sem hægt er að flytja til félagans.</span><span class="sxs-lookup"><span data-stu-id="bc5a2-124">When you post an intercompany general journal line in your company, a corresponding journal line is created in your intercompany outbox that you can transfer to your partner.</span></span> <span data-ttu-id="bc5a2-125">Félaginn getur síðan bókað samsvarandi færslu í sínu fyrirtæki án þess að færa gögnin inn aftur.</span><span class="sxs-lookup"><span data-stu-id="bc5a2-125">Your partner can then post the corresponding transaction in their company, without having to re-enter the data.</span></span>

1. <span data-ttu-id="bc5a2-126">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **MF-færslubækur** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="bc5a2-126">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Intercompany General Journals**, and then choose the related link.</span></span>  
2. <span data-ttu-id="bc5a2-127">Viðeigandi færslubókarkeyrsla er opnaður.</span><span class="sxs-lookup"><span data-stu-id="bc5a2-127">Open the relevant journal batch.</span></span> <span data-ttu-id="bc5a2-128">Frekari upplýsingar, sjá [Vinna með almennar færslubækur](ui-work-general-journals.md).</span><span class="sxs-lookup"><span data-stu-id="bc5a2-128">For more information, see [Working with General Journals](ui-work-general-journals.md).</span></span>
3. <span data-ttu-id="bc5a2-129">Fyllið inn í reitina eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="bc5a2-129">Fill in the fields as necessary.</span></span>
4. <span data-ttu-id="bc5a2-130">Í reitinn **MF félagi fjárhagsreikningur nr.** færið inn MF fjárhagsreikninginn sem upphæðin verður bókuð á í fyrirtæki félagans.</span><span class="sxs-lookup"><span data-stu-id="bc5a2-130">In the **IC Partner G/L Acc. No.** field, enter the intercompany general ledger account that the amount will be posted to in your partner's company.</span></span>

    > [!NOTE]
    > <span data-ttu-id="bc5a2-131">Þennan reit verður að fylla út í línu með bankareikningi eða fjárhagsreikningi annað hvort í reitnum **Reikningsnúmer** eða reitnum **Mótreikningsnúmer**.</span><span class="sxs-lookup"><span data-stu-id="bc5a2-131">This field must be filled in on a line with a bank account or general ledger account in either the **Account No.** field or the **Bal. Account No.** field.</span></span>  
5. <span data-ttu-id="bc5a2-132">Valið er **Bóka** aðgerðin.</span><span class="sxs-lookup"><span data-stu-id="bc5a2-132">Choose the **Post** action.</span></span>

<span data-ttu-id="bc5a2-133">Færslurnar sem þessu tengjast eru bókaðar í þínu fyrirtæki og færslubók með samsvarandi færslum er stofnuð í úthólfi millifyrirtækisins þar sem þú getur sent þær til fyrirtæki félagans.</span><span class="sxs-lookup"><span data-stu-id="bc5a2-133">The involved entries are posted in your company and a journal with the corresponding entries are created in your intercompany outbox that you can send to your partner company.</span></span> <span data-ttu-id="bc5a2-134">Frekari upplýsingar er að finna í [Stjórna millifyrirtækja innhólfsfærslur og úthólfsfærslur](intercompany-how-manage-intercompany-inbox.md).</span><span class="sxs-lookup"><span data-stu-id="bc5a2-134">For more information, see [Manage the Intercompany Inbox and Outbox](intercompany-how-manage-intercompany-inbox.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="bc5a2-135">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="bc5a2-135">See Also</span></span>
[<span data-ttu-id="bc5a2-136">Vinna með millifyrirtækjafærslur</span><span class="sxs-lookup"><span data-stu-id="bc5a2-136">Managing Intercompany Transactions</span></span>](intercompany-manage.md)  
[<span data-ttu-id="bc5a2-137">Fjármál</span><span class="sxs-lookup"><span data-stu-id="bc5a2-137">Finance</span></span>](finance.md)  
[<span data-ttu-id="bc5a2-138">Uppsetning Fjármála</span><span class="sxs-lookup"><span data-stu-id="bc5a2-138">Setting Up Finance</span></span>](finance-setup-finance.md)  
[<span data-ttu-id="bc5a2-139">Vinna í færslubókum</span><span class="sxs-lookup"><span data-stu-id="bc5a2-139">Working with General Journals</span></span>](ui-work-general-journals.md)  
<span data-ttu-id="bc5a2-140">[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="bc5a2-140">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]