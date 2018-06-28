---
title: "Yfirlit yfir umsjónarverkhluta viðskiptaskulda| Microsoft Docs"
description: "Útskýrir verkhluta sem felur í sér stjórnun viðskiptaskulda, til dæmis að borga skuldareiganda eða úthluta greiðslum á útleið á fjárhagsfærslur til að loka reikningum eða kreditreikningum."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: vendor payment, creditor, debt, balance due, AP
ms.date: 06/28/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2286b728a464943841b192031cfea13644441013
ms.openlocfilehash: 730596534df93b7aa16f7975b5c5b1307a7f571a
ms.contentlocale: is-is
ms.lasthandoff: 06/28/2018

---
# <a name="managing-payables"></a><span data-ttu-id="e0aec-103">Stjórna skuldum</span><span class="sxs-lookup"><span data-stu-id="e0aec-103">Managing Payables</span></span>
<span data-ttu-id="e0aec-104">Stór hluti af stjórnun viðskiptaskulda er að borga lánardrottnum þínum eða endurgreiða starfsmönnum útgjöld.</span><span class="sxs-lookup"><span data-stu-id="e0aec-104">A big part of managing accounts payable is paying your vendors, or reimbursing your employees for expenses.</span></span> <span data-ttu-id="e0aec-105">Þú getur notað aðgerðir til að bæta við greiðslumörkum fyrir innkaupakvittanir sem eiga að eiga sér stað í **Greiðslubókinni**.</span><span class="sxs-lookup"><span data-stu-id="e0aec-105">You can use functions to add payments lines for purchase invoices that are due in the **Payment Journal** window.</span></span> <span data-ttu-id="e0aec-106">Til að senda viðskipti í bankann þinn, getur þú flutt margar greiðslubókalínur í skrá og síðan hlaðið skránum inn í bankann þinn.</span><span class="sxs-lookup"><span data-stu-id="e0aec-106">To send transactions to your bank, you can export multiple payment journal lines to a file, and then upload the file to your bank.</span></span> <span data-ttu-id="e0aec-107">Einnig er hægt að framkvæma greiðslur með tékka, þar með talið senda tékka sem rafræn greiðsla</span><span class="sxs-lookup"><span data-stu-id="e0aec-107">You can also make payments by check, including transmitting checks as electronic payments.</span></span>

<span data-ttu-id="e0aec-108">Annar dæmigerður verkefni er að jafna útgjöld við tengdar fjárhagsfærslur lánardrottna og starfsmanna, til þess að loka innkaupareikningum, innkaupakreditreikningum eða starfsmannareikningnum sem greiddir.</span><span class="sxs-lookup"><span data-stu-id="e0aec-108">Another typical task is to apply outgoing payments to their related vendor or employee ledger entries in order to close purchase invoices, purchase credit memos, or employee accounts as paid.</span></span> <span data-ttu-id="e0aec-109">Þú getur gert þetta í glugganum **Greiðsluafstemmingarbók** með því að flytja inn bankareikningsskrá til að skrá greiðslur.</span><span class="sxs-lookup"><span data-stu-id="e0aec-109">You can do this in the **Payment Reconciliation Journal** window by importing a bank statement file to register the payments.</span></span> <span data-ttu-id="e0aec-110">Greiðslurnar eru jafnaðar við opinn lánardrottinn, viðskiptamann eða starfsmanna fjárhagsfærslur með því að láta greiðslu texta og færsluupplýsingar passa saman.</span><span class="sxs-lookup"><span data-stu-id="e0aec-110">The payments are applied to open vendor, customer, or employee ledger entries by matching payment text and entry information.</span></span> <span data-ttu-id="e0aec-111">Það eru ýmsar leiðir til að skoða og breyta leikjunum áður en þú sendir dagbókina.</span><span class="sxs-lookup"><span data-stu-id="e0aec-111">There are various ways to review and change the matches before you post the journal.</span></span> <span data-ttu-id="e0aec-112">Þú getur valið að loka öllum opnum bankareikningsfærslum sem tengjast jöfnuðu fjárhagsfærslunum þegar þú bókar færslubókina.</span><span class="sxs-lookup"><span data-stu-id="e0aec-112">You can choose to close any open bank account ledger entries related to the applied ledger entries when you post the journal.</span></span> <span data-ttu-id="e0aec-113">Bankareikningurinn er sjálfkrafa sáttur þegar allar greiðslur eru sóttar.</span><span class="sxs-lookup"><span data-stu-id="e0aec-113">The bank account is automatically reconciled when all payments are applied.</span></span>

<span data-ttu-id="e0aec-114">Einnig er hægt að jafna greiðslur á útleið handvirkt í glugganum **greiðslubók** eða úr tengdum lánardrottna- eða starfsmanna fjárhagsfærslur.</span><span class="sxs-lookup"><span data-stu-id="e0aec-114">Alternatively, you can apply outgoing payments manually in the **Payment Journal** window or from the related vendor or employee ledger entries.</span></span>

<span data-ttu-id="e0aec-115">Í eftirfarandi töflu er lýsing á röð verka  innan viðskiptaskulda með tenglum í efnisatriðin sem lýsa þeim.</span><span class="sxs-lookup"><span data-stu-id="e0aec-115">The following table describes a sequence of tasks within accounts payable, with links to the topics that describe them.</span></span>

| <span data-ttu-id="e0aec-116">Til</span><span class="sxs-lookup"><span data-stu-id="e0aec-116">To</span></span> | <span data-ttu-id="e0aec-117">Sjá</span><span class="sxs-lookup"><span data-stu-id="e0aec-117">See</span></span> |
| --- | --- |
| <span data-ttu-id="e0aec-118">Mynda lánardrottnagreiðslur komnar á gjalddaga eða endurgreiðslur til starfsmanna, undirbúa ávísanagreiðslur og flytja út greiðslur á bankaskrá við bókun.</span><span class="sxs-lookup"><span data-stu-id="e0aec-118">Generate due vendor payments or employee reimbursements, prepare check payments, and export payments to a bank file when posting.</span></span> |[<span data-ttu-id="e0aec-119">Framkvæma greiðslur</span><span class="sxs-lookup"><span data-stu-id="e0aec-119">Making Payments</span></span>](payables-make-payments.md) |
| <span data-ttu-id="e0aec-120">Jafna greiðslur lánardrottna sjálfkrafa við ógreidda innkaupareikninga með því að flytja inn bankayfirlitsskrá.</span><span class="sxs-lookup"><span data-stu-id="e0aec-120">Apply vendor payments automatically to unpaid purchase invoices by importing a bank statement file.</span></span> |[<span data-ttu-id="e0aec-121">Jafna greiðslur sjálfkrafa og afstemma bankareikninga</span><span class="sxs-lookup"><span data-stu-id="e0aec-121">Applying Payments Automatically and Reconciling Bank Accounts</span></span>](receivables-apply-payments-auto-reconcile-bank-accounts.md) |
| <span data-ttu-id="e0aec-122">Jafna greiðslur lánardrottna handvirkt við ógreidda innkaupareikninga.</span><span class="sxs-lookup"><span data-stu-id="e0aec-122">Apply vendor payments to unpaid purchase invoices manually.</span></span> |[<span data-ttu-id="e0aec-123">Afstemma greiðslur lánardrottna handvirkt</span><span class="sxs-lookup"><span data-stu-id="e0aec-123">Reconcile Vendor Payments Manually</span></span>](payables-how-apply-purchase-transactions-manually.md) |
|<span data-ttu-id="e0aec-124">Tryggðu rétt birgðamat með því að úthluta viðbótar vörukostnaði, eins og farmur, efnisleg meðhöndlun, tryggingar og flutningar sem viðskipti þín með vörurnar hafa í för með sér.</span><span class="sxs-lookup"><span data-stu-id="e0aec-124">Ensure correct inventory valuation by assigning added item costs, such as freight, physical handling, insurance, and transportation that you incur when purchasing.</span></span>|[<span data-ttu-id="e0aec-125">Nota kostnaðarauka til að gera grein fyrir viðbótar viðskiptakostnaði</span><span class="sxs-lookup"><span data-stu-id="e0aec-125">Use Item Charges to Account for Additional Trade Costs</span></span>](payables-how-assign-item-charges.md)|

## <a name="see-also"></a><span data-ttu-id="e0aec-126">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="e0aec-126">See Also</span></span>
[<span data-ttu-id="e0aec-127">Innkaup</span><span class="sxs-lookup"><span data-stu-id="e0aec-127">Purchasing</span></span>](purchasing-manage-purchasing.md)  
[<span data-ttu-id="e0aec-128">Stjórnun skulda</span><span class="sxs-lookup"><span data-stu-id="e0aec-128">Managing Receivables</span></span>](receivables-manage-receivables.md)  
[<span data-ttu-id="e0aec-129">Nota kostnaðarauka til að gera grein fyrir viðbótar viðskiptakostnaði</span><span class="sxs-lookup"><span data-stu-id="e0aec-129">Use Item Charges to Account for Additional Trade Costs</span></span>](payables-how-assign-item-charges.md)  
[<span data-ttu-id="e0aec-130">Almenn viðskiptavirkni</span><span class="sxs-lookup"><span data-stu-id="e0aec-130">General Business Functionality</span></span>](ui-across-business-areas.md)  
<span data-ttu-id="e0aec-131">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="e0aec-131">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
 

