---
title: "Yfirlit yfir umsjónarverkhluta viðskiptaskulda| Microsoft Docs"
description: "Útskýrir verkhluta sem felur í sér stjórnun viðskiptaskulda, til dæmis að borga skuldareiganda eða úthluta greiðslum á útleið á fjárhagsfærslur til að loka reikningum eða kreditreikningum."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: vendor payment, creditor, debt, balance due, AP
ms.date: 06/06/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 9684a91268927a4f1f4d249fef019c8f6ac00325
ms.contentlocale: is-is
ms.lasthandoff: 07/07/2017


---
# <a name="managing-payables"></a><span data-ttu-id="76db3-103">Stjórna skuldum</span><span class="sxs-lookup"><span data-stu-id="76db3-103">Managing Payables</span></span>
<span data-ttu-id="76db3-104">Stór hluti af stjórnun viðskiptaskulda er að borga lánardrottnum þínum.</span><span class="sxs-lookup"><span data-stu-id="76db3-104">A big part of managing accounts payable is paying your vendors.</span></span> <span data-ttu-id="76db3-105">Þú getur notað aðgerðir til að bæta við greiðslumörkum fyrir innkaupakvittanir sem eiga að eiga sér stað í **Greiðslubókinni**.</span><span class="sxs-lookup"><span data-stu-id="76db3-105">You can use functions to add payments lines for purchase invoices that are due in the **Payment Journal** window.</span></span> <span data-ttu-id="76db3-106">Til að senda viðskipti í bankann þinn, getur þú flutt margar greiðslubókalínur í skrá og síðan hlaðið skránum inn í bankann þinn.</span><span class="sxs-lookup"><span data-stu-id="76db3-106">To send transactions to your bank, you can export multiple payment journal lines to a file, and then upload the file to your bank.</span></span> <span data-ttu-id="76db3-107">Einnig er hægt að framkvæma greiðslur með tékka, þar með talið senda tékka sem rafræn greiðsla</span><span class="sxs-lookup"><span data-stu-id="76db3-107">You can also make payments by check, including transmitting checks as electronic payments.</span></span>

<span data-ttu-id="76db3-108">Annar dæmigerður verkefni er að beita útgjöldum til tengdra söluaðilanna, til þess að loka innkaupakostningum eða kaupa lánshæfiseinkunnir sem greiddar eru.</span><span class="sxs-lookup"><span data-stu-id="76db3-108">Another typical task is to apply outgoing payments to their related vendor ledger entries in order to close purchase invoices or purchase credit memos as paid.</span></span> <span data-ttu-id="76db3-109">Þú getur gert þetta í glugganum **Greiðsluafstemmingarbók** með því að flytja inn bankareikningsskrá til að skrá greiðslur.</span><span class="sxs-lookup"><span data-stu-id="76db3-109">You can do this in the **Payment Reconciliation Journal** window by importing a bank statement file to register the payments.</span></span> <span data-ttu-id="76db3-110">Greiðslur eru beittar til að opna seljanda eða viðskiptavinarbókarfærslur með því að passa greiðslu texta og færsluupplýsingar.</span><span class="sxs-lookup"><span data-stu-id="76db3-110">The payments are applied to open vendor or customer ledger entries by matching payment text and entry information.</span></span> <span data-ttu-id="76db3-111">Það eru ýmsar leiðir til að skoða og breyta leikjunum áður en þú sendir dagbókina.</span><span class="sxs-lookup"><span data-stu-id="76db3-111">There are various ways to review and change the matches before you post the journal.</span></span> <span data-ttu-id="76db3-112">Þú getur valið að loka öllum opnum bankareikningsfærslum sem tengjast jöfnuðu fjárhagsfærslunum þegar þú bókar færslubókina.</span><span class="sxs-lookup"><span data-stu-id="76db3-112">You can choose to close any open bank account ledger entries related to the applied ledger entries when you post the journal.</span></span> <span data-ttu-id="76db3-113">Bankareikningurinn er sjálfkrafa sáttur þegar allar greiðslur eru sóttar.</span><span class="sxs-lookup"><span data-stu-id="76db3-113">The bank account is automatically reconciled when all payments are applied.</span></span>

<span data-ttu-id="76db3-114">Einnig er hægt að jafna greiðslur á útleið handvirkt í glugganum **greiðslubók**  eða úr tengdum lánardrottnafærslur.</span><span class="sxs-lookup"><span data-stu-id="76db3-114">Alternatively, you can apply outgoing payments manually in the **Payment Journal** window or from the related vendor ledger entries.</span></span>

<span data-ttu-id="76db3-115">Í eftirfarandi töflu er lýsing á röð verka  innan viðskiptaskulda með tenglum í efnisatriðin sem lýsa þeim.</span><span class="sxs-lookup"><span data-stu-id="76db3-115">The following table describes a sequence of tasks within accounts payable, with links to the topics that describe them.</span></span>

| <span data-ttu-id="76db3-116">Til</span><span class="sxs-lookup"><span data-stu-id="76db3-116">To</span></span> | <span data-ttu-id="76db3-117">Sjá</span><span class="sxs-lookup"><span data-stu-id="76db3-117">See</span></span> |
| --- | --- |
| <span data-ttu-id="76db3-118">Mynda gjaldfallnar greiðslur lánardrottna með forgangsröðun samkvæmt greiðsluafslætti og vanræksluálags.</span><span class="sxs-lookup"><span data-stu-id="76db3-118">Generate due vendor payments prioritized according to payment discounts and overdue penalties.</span></span> <span data-ttu-id="76db3-119">Valkvæt er að flytja út greiðslur í bankaskrá við bókun.</span><span class="sxs-lookup"><span data-stu-id="76db3-119">Optionally, export the payments to a bank file when posting.</span></span> |[<span data-ttu-id="76db3-120">Framkvæma greiðslur</span><span class="sxs-lookup"><span data-stu-id="76db3-120">Make Payments</span></span>](payables-make-payments.md) |
| <span data-ttu-id="76db3-121">Jafna greiðslur lánardrottna sjálfkrafa við ógreidda innkaupareikninga með því að flytja inn bankayfirlitsskrá.</span><span class="sxs-lookup"><span data-stu-id="76db3-121">Apply vendor payments automatically to unpaid purchase invoices by importing a bank statement file.</span></span> |[<span data-ttu-id="76db3-122">Jafna greiðslur sjálfkrafa og afstemma bankareikninga</span><span class="sxs-lookup"><span data-stu-id="76db3-122">Apply Payments Automatically and Reconcile Bank Accounts</span></span>](receivables-apply-payments-auto-reconcile-bank-accounts.md) |
| <span data-ttu-id="76db3-123">Jafna greiðslur lánardrottna handvirkt við ógreidda innkaupareikninga.</span><span class="sxs-lookup"><span data-stu-id="76db3-123">Apply vendor payments to unpaid purchase invoices manually.</span></span> |[<span data-ttu-id="76db3-124">Hvernig á að: Afstemma greiðslur á lánardrottna handvirkt</span><span class="sxs-lookup"><span data-stu-id="76db3-124">How to: Reconcile Vendor Payments Manually</span></span>](payables-how-apply-purchase-transactions-manually.md) |
|<span data-ttu-id="76db3-125">Tryggðu rétt birgðamat með því að úthluta viðbótar vörukostnaði, eins og farmur, efnisleg meðhöndlun, tryggingar og flutningar sem viðskipti þín með vörurnar hafa í för með sér.</span><span class="sxs-lookup"><span data-stu-id="76db3-125">Ensure correct inventory valuation by assigning added item costs, such as freight, physical handling, insurance, and transportation that you incur when purchasing.</span></span>|[<span data-ttu-id="76db3-126">Hvernig skal: Nota kostnaðarauka til að gera grein fyrir viðbótar viðskiptakostnaði</span><span class="sxs-lookup"><span data-stu-id="76db3-126">How to: Use Item Charges to Account for Additional Trade Costs</span></span>](payables-how-assign-item-charges.md)|

## <a name="see-also"></a><span data-ttu-id="76db3-127">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="76db3-127">See Also</span></span>
[<span data-ttu-id="76db3-128">Innkaup</span><span class="sxs-lookup"><span data-stu-id="76db3-128">Purchasing</span></span>](purchasing-manage-purchasing.md)  
[<span data-ttu-id="76db3-129">Stjórnun skulda</span><span class="sxs-lookup"><span data-stu-id="76db3-129">Managing Receivables</span></span>](receivables-manage-receivables.md)  
[<span data-ttu-id="76db3-130">Hvernig skal: Nota kostnaðarauka til að gera grein fyrir viðbótar viðskiptakostnaði</span><span class="sxs-lookup"><span data-stu-id="76db3-130">How to: Use Item Charges to Account for Additional Trade Costs</span></span>](payables-how-assign-item-charges.md)  
[<span data-ttu-id="76db3-131">Almenn viðskiptavirkni</span><span class="sxs-lookup"><span data-stu-id="76db3-131">General Business Functionality</span></span>](ui-across-business-areas.md)  
<span data-ttu-id="76db3-132">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="76db3-132">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

