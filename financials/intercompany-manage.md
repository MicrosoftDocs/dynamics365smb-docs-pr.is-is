---
title: "Færslur á milli dótturfyrirtækja innan sama fyrirtækis | Microsoft Docs"
description: "Með milli-fyrirtækjavirkninni getur einfaldað fyrirtækjaferli og færslur á milli dótturfyrirtækja innan sama fyrirtækis."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: IC, group, consolidation, affiliate, subsidiary
ms.date: 06/20/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: b34f276a764f0e828fbc1f015429df9852242a4c
ms.openlocfilehash: 0537940a323ff102552551a95d99cc9da8c6da52
ms.contentlocale: is-is
ms.lasthandoff: 03/22/2018

---
# <a name="managing-intercompany-transactions"></a><span data-ttu-id="73d1a-103">Vinna með millifyrirtækjafærslur</span><span class="sxs-lookup"><span data-stu-id="73d1a-103">Managing Intercompany Transactions</span></span>
<span data-ttu-id="73d1a-104">Fyrirtækið gæti verið samansett úr mörgum dótturfyrirtækum án þess að hafa sama fjölda bókahalds- og stjórnunarteyma.</span><span class="sxs-lookup"><span data-stu-id="73d1a-104">Your organization may consist of several companies, but might not have the equivalent number of accounting and administrative teams.</span></span> <span data-ttu-id="73d1a-105">Milli-fyrirtækjavirknin gerir þér kleift að stunda viðskipti við dóttur- og félagafyrirtæki á sama hátt og þú átt við ytri lánardrottna og viðskiptamenn.</span><span class="sxs-lookup"><span data-stu-id="73d1a-105">The Intercompany functionality lets you do business with your subsidiary and internal partner organizations in the same way as you engage with your external vendors and customers.</span></span> <span data-ttu-id="73d1a-106">Færslur milli fyrirtækja eru aðeins færðar einu sinni í viðeigandi skjal.</span><span class="sxs-lookup"><span data-stu-id="73d1a-106">You enter intercompany transaction information only once in the appropriate documents.</span></span> <span data-ttu-id="73d1a-107">Notandinn getur notað þær aðgerðir sem hann er vanur, til dæmis stjórnun á útgjöldum og gjaldfærðum skuldum.</span><span class="sxs-lookup"><span data-stu-id="73d1a-107">You can use the functionality you are already familiar with, such as receivables and payables management.</span></span> <span data-ttu-id="73d1a-108">Vörpunaraðgerðir fyrir bókhaldslykla og víddir tryggja að upplýsingarnar birtist á réttum stað.</span><span class="sxs-lookup"><span data-stu-id="73d1a-108">Mapping facilities for the chart of accounts and dimensions help ensure that information appears in the right places.</span></span>  

<span data-ttu-id="73d1a-109">Fjórir helstu kostir milli fyrirtækjavirkninnar eru:</span><span class="sxs-lookup"><span data-stu-id="73d1a-109">There are four main benefits to the Intercompany functionality:</span></span>  

- <span data-ttu-id="73d1a-110">Tímasparnaður og einfaldari færslur auka afköst</span><span class="sxs-lookup"><span data-stu-id="73d1a-110">Increased productivity as a result of time saved and simplified transactions</span></span>  
- <span data-ttu-id="73d1a-111">Minni hætta á villum - færslur aðeins færðar inn í eitt skipti og sjálfvirkar uppfærslur á heildarkerfinu</span><span class="sxs-lookup"><span data-stu-id="73d1a-111">Minimized error potential with one-time entry of information and system-wide, automated updates</span></span>  
- <span data-ttu-id="73d1a-112">Fullt eftirlit með ferli endurskoðana, viðskipta og færslna</span><span class="sxs-lookup"><span data-stu-id="73d1a-112">Complete audit trail and full visibility into business activities and transaction histories</span></span>  
- <span data-ttu-id="73d1a-113">Skilvirkar og hagkvæmar færslur í samskiptum við hlutdeildarfélög eða dótturfyrirtæki</span><span class="sxs-lookup"><span data-stu-id="73d1a-113">Efficient, cost-effective transactions with affiliate and subsidiary companies</span></span>  

<span data-ttu-id="73d1a-114">Færsluskjölum má stjórna algjörlega.</span><span class="sxs-lookup"><span data-stu-id="73d1a-114">You are in full control of all transaction documents.</span></span> <span data-ttu-id="73d1a-115">Til dæmis er hægt að hafna fylgiskjali sem sent hafa verið og, með þessum hætti, bakfæra bókanir sem voru rangar.</span><span class="sxs-lookup"><span data-stu-id="73d1a-115">For example, you can reject a document sent to you and, in this way, reverse postings that were incorrect.</span></span> <span data-ttu-id="73d1a-116">Einnig er hægt að uppfæra innkaupapöntun þegar keypt er frá félaga eða hlutdeildarfyrirtæki, svo lengi sem sölufyrirtækið hefur ekki afhent vörur.</span><span class="sxs-lookup"><span data-stu-id="73d1a-116">Or, when making a purchase from a partner or subsidiary company, you can update the purchase order as long as the selling company has not shipped any goods.</span></span>  

<span data-ttu-id="73d1a-117">Þegar færsla er færð inn þarf ekki að tilgreina reikningana fyrir stök söfn bóka, heldur þarf aðeins að gefa upp kenni samstarfsfyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="73d1a-117">When you enter a transaction, you do not need to specify the accounts for an individual set of books, but simply give the identification of the partner company.</span></span> <span data-ttu-id="73d1a-118">Milli-fyrirtækjavirknin býr til færslubókarlínur sem leiða til réttrar stöðu reikninga beggja fyrirtækjanna sem eiga hlut að færslu.</span><span class="sxs-lookup"><span data-stu-id="73d1a-118">The Intercompany functionality creates general journal lines that result in the balancing of the books of both companies involved in a transaction.</span></span> <span data-ttu-id="73d1a-119">Í Útistandandi og viðskiptaskuldir er MF-félagakóta úthlutað á hvaða viðskiptamann eða lánardrottin sem er.</span><span class="sxs-lookup"><span data-stu-id="73d1a-119">In receivables and payables, you assign an intercompany partner code to any customer or vendor.</span></span> <span data-ttu-id="73d1a-120">Pantanir og reikningar sem eiga við færslur til eða frá þessum félögum stofna þaðan í frá samsvarandi skjöl hjá fyrirtækjafélögum svo að staða reikninganna verði rétt.</span><span class="sxs-lookup"><span data-stu-id="73d1a-120">From that moment on, all orders and invoices generated pertaining to transactions with these companies will produce corresponding documents in the partner company, resulting in correct balancing of the accounts.</span></span>  

 <span data-ttu-id="73d1a-121">Eftir að samstarfsaðilar hafa verið settir upp sem viðskiptamenn og lánardrottnar í kerfinu og þeim úthlutað MF-félagakóta er hægt að deila innkaupa- og söluskjölum milli fyrirtækja, þar á meðal vörum og vörugjöldum.</span><span class="sxs-lookup"><span data-stu-id="73d1a-121">After you set up business partners as customers and vendors in the system, and assign them intercompany partner codes, it is possible to exchange intercompany purchase and sales documents, including items and item charges.</span></span> <span data-ttu-id="73d1a-122">Milli fyrirtækjavirknin leyfir færslur milli fyrirtækja úr mörgum gagnagrunnum, til dæmis í ólíkum löndum/svæðum, í ólíkum gjaldmiðlum, bókhaldslyklum, víddum og vörunúmerum.</span><span class="sxs-lookup"><span data-stu-id="73d1a-122">The Intercompany functionality allows intercompany transactions between multiple databases, for example, in different countries/regions, as well as multiple currencies, different charts of accounts, different dimensions, and different item numbering.</span></span>  

<span data-ttu-id="73d1a-123">Eftirfarandi tafla lýsir röð verkefna með tenglum í efnisatriði þar sem þeim er lýst.</span><span class="sxs-lookup"><span data-stu-id="73d1a-123">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>

 |<span data-ttu-id="73d1a-124">Til</span><span class="sxs-lookup"><span data-stu-id="73d1a-124">To</span></span> |<span data-ttu-id="73d1a-125">Sjá</span><span class="sxs-lookup"><span data-stu-id="73d1a-125">See</span></span>|
 |---|---|
 |<span data-ttu-id="73d1a-126">Stofna lánardrottna og viðskiptamenn millifyrirtækis sem svokallaða millifyrirtækjafélaga, og setja upp bókhaldslykil millifyrirtækis.</span><span class="sxs-lookup"><span data-stu-id="73d1a-126">Create your intercompany vendors and customers as so-called intercompany partners, and set up an intercompany chart of accounts.</span></span>|[<span data-ttu-id="73d1a-127">Uppsetning milli fyrirtækja</span><span class="sxs-lookup"><span data-stu-id="73d1a-127">Set Up Intercompany</span></span>](intercompany-how-setup.md)|
 |<span data-ttu-id="73d1a-128">Milli-fyrirtækjaskjöl eða færslubækur eru notuð til að bóka viðskipti við milli-fyrirtækjafélaga.</span><span class="sxs-lookup"><span data-stu-id="73d1a-128">Use intercompany documents or journals to post transactions with your intercompany partners.</span></span>|[<span data-ttu-id="73d1a-129">Unnið með samstæðuskjöl og færslubækur</span><span class="sxs-lookup"><span data-stu-id="73d1a-129">Work with Intercompany Documents and Journals</span></span>](intercompany-how-work-documents-journals.md)|
 |<span data-ttu-id="73d1a-130">Skipuleggja og vinna færslur á inn- og útleið sem þú og millifyrirtækjafélagar þínir sendið ykkar á milli.</span><span class="sxs-lookup"><span data-stu-id="73d1a-130">Organize and process incoming and outgoing transactions that you exchange with your intercompany partners.</span></span>|[<span data-ttu-id="73d1a-131">Stjórna millifyrirtækja innhólfsfærslur og úthólfsfærslur</span><span class="sxs-lookup"><span data-stu-id="73d1a-131">Manage the Intercompany Inbox and Outbox</span></span>](intercompany-how-manage-intercompany-inbox.md)|

## <a name="see-also"></a><span data-ttu-id="73d1a-132">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="73d1a-132">See Also</span></span>
[<span data-ttu-id="73d1a-133">Fjármál</span><span class="sxs-lookup"><span data-stu-id="73d1a-133">Finance</span></span>](finance.md)  
[<span data-ttu-id="73d1a-134">Uppsetning Fjármála</span><span class="sxs-lookup"><span data-stu-id="73d1a-134">Setting Up Finance</span></span>](finance-setup-finance.md)  
[<span data-ttu-id="73d1a-135">Vinna í færslubókum</span><span class="sxs-lookup"><span data-stu-id="73d1a-135">Working with General Journals</span></span>](ui-work-general-journals.md)  
<span data-ttu-id="73d1a-136">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="73d1a-136">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
## [!INCLUDE[d365fin](includes/training_link_md.md)]

