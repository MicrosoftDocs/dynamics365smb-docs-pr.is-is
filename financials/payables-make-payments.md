---
title: "Yfirlit yfir umsjónarverkhluta greiðslna til lánardrottna| Microsoft Docs"
description: "Útskýrir verkhluta sem fela í sér stjórnun greiðslna til lánardrottna, eins og að bóka greiðslulínur og sækja yfirlit fyrir gjaldfallna stöðu."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: print check, vendor payment, creditor, debt, balance due, AP
ms.date: 06/06/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: d0b9020596484a8910db2f5720adfe159ad96fe7
ms.contentlocale: is-is
ms.lasthandoff: 07/07/2017


---
# <a name="make-payments"></a><span data-ttu-id="da3b0-103">Framkvæma greiðslur</span><span class="sxs-lookup"><span data-stu-id="da3b0-103">Make Payments</span></span>
<span data-ttu-id="da3b0-104">Þegar greiðslur til lánardrottna eru framkvæmdar eru tengdar greiðslulínur bókaðar í glugganum **Greiðslubók**.</span><span class="sxs-lookup"><span data-stu-id="da3b0-104">When you make payments to vendors, you post the related payment lines in the **Payment Journal** window.</span></span> <span data-ttu-id="da3b0-105">Hægt er að nota aðgerðina **Greiðslutillögur til lánardrottna** til að finna greiðslur sem komnar eru á gjalddaga.</span><span class="sxs-lookup"><span data-stu-id="da3b0-105">You can use the **Suggest Vendor Payments** function to find payments that are due.</span></span> <span data-ttu-id="da3b0-106">Einnig er hægt að nota skýrsluna **Lánardrottinn - aldursgreind staða** til að fá yfirlit yfir greiðslur sem komnar eru á gjalddaga.</span><span class="sxs-lookup"><span data-stu-id="da3b0-106">You can also use the **Vendor - Summary Aging** report to get an overview of due payments.</span></span>

<span data-ttu-id="da3b0-107">Úr greiðslubókinni er hægt að prenta vélfærða tékka eða skrá þegar tékkar eru skrifaðir.</span><span class="sxs-lookup"><span data-stu-id="da3b0-107">From the payment journal, you can print computer checks or record when checks are written.</span></span> <span data-ttu-id="da3b0-108">Þegar **Vélfærður tékki** er valinn í reitnum **Tegund bankagreiðslu** verður að prenta allar línur sem tákna tékka áður en hægt er að bóka greiðslubókina.</span><span class="sxs-lookup"><span data-stu-id="da3b0-108">If you select **Computer Check** in the **Bank Payment Type** field, then any lines representing checks must be printed before the payment journal can be posted.</span></span>

<span data-ttu-id="da3b0-109">Þegar greiðslurnar eru bókaðar eru þær fluttar í bankaskrá til að hlaða þær upp í banka til meðhöndlunar.</span><span class="sxs-lookup"><span data-stu-id="da3b0-109">When the payments are posted, you can export them to a bank file for upload to your bank for processing.</span></span>

<span data-ttu-id="da3b0-110">Þegar búið er að framkvæma greiðslur til banka, þarf að jafna þær við tengdar opnar lánardrottnafærslur.</span><span class="sxs-lookup"><span data-stu-id="da3b0-110">After the payments are made at your bank, you must apply them to their related open vendor ledger entries.</span></span> <span data-ttu-id="da3b0-111">Hægt er að gera það handvirkt eða með því að flytja inn bankayfirlitsskrá og jafna greiðslur sjálfkrafa.</span><span class="sxs-lookup"><span data-stu-id="da3b0-111">You can do this manually or by importing a bank statement file and applying the payments automatically.</span></span> <span data-ttu-id="da3b0-112">Nánari upplýsingar er að finna í [Jafna greiðslur sjálfkrafa og stemma af bankareikninga](receivables-apply-payments-auto-reconcile-bank-accounts.md).</span><span class="sxs-lookup"><span data-stu-id="da3b0-112">For more information, see [Apply Payments Automatically and Reconcile Bank Accounts](receivables-apply-payments-auto-reconcile-bank-accounts.md).</span></span>

<span data-ttu-id="da3b0-113">Eftirfarandi tafla lýsir röð verkefna með tenglum í efnisatriði þar sem þeim er lýst.</span><span class="sxs-lookup"><span data-stu-id="da3b0-113">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>

| <span data-ttu-id="da3b0-114">Til</span><span class="sxs-lookup"><span data-stu-id="da3b0-114">To</span></span> | <span data-ttu-id="da3b0-115">Sjá</span><span class="sxs-lookup"><span data-stu-id="da3b0-115">See</span></span> |
| --- | --- |
| <span data-ttu-id="da3b0-116">Nota skal aðgerð til að leggja til lánardrottnagreiðslur samkvæmt völdum skilyrðum, eins og gjalddaga, afsláttarskilyrði og greiðslugetu þína.</span><span class="sxs-lookup"><span data-stu-id="da3b0-116">Use a function to suggest vendor payments according to selected criteria, such as due date, discount eligibility, and your liquidity.</span></span> |[<span data-ttu-id="da3b0-117">Hvernig á að leggja til greiðslutillögur til lánardrottna</span><span class="sxs-lookup"><span data-stu-id="da3b0-117">How to: Suggest Vendor Payments</span></span>](payables-how-suggest-vendor-payments.md) |
| <span data-ttu-id="da3b0-118">Gefið út tékka vegna greiðslna, annað hvort útprentaða eða sem vélfærða tékka.</span><span class="sxs-lookup"><span data-stu-id="da3b0-118">Issue checks for payments, either as print-outs or as computer checks.</span></span> <span data-ttu-id="da3b0-119">Ógilda tékka fyrir eða eftir bókun.</span><span class="sxs-lookup"><span data-stu-id="da3b0-119">Void checks before or after posting.</span></span> |[<span data-ttu-id="da3b0-120">Hvernig á að: vinna með tékka</span><span class="sxs-lookup"><span data-stu-id="da3b0-120">How to: Work with Checks</span></span>](payables-how-work-checks.md) |
| <span data-ttu-id="da3b0-121">Gakktu úr skugga um að bankinn þinn eingöngu hreinsar staðfestar athuganir og magn með því að senda þeim skrá sem inniheldur seljanda, athugun og greiðsluupplýsingar.</span><span class="sxs-lookup"><span data-stu-id="da3b0-121">Make sure that your bank only clears validated checks and amounts by sending them a file that contains vendor, check, and payment information.</span></span> |[<span data-ttu-id="da3b0-122">Hvernig á að: flytja út jákvæða greiðsluskrá</span><span class="sxs-lookup"><span data-stu-id="da3b0-122">How to: Export a Positive Pay file</span></span>](finance-how-positive-pay.md) |
|<span data-ttu-id="da3b0-123">Flytja greiðslur úr glugganum **Greiðslubók** í bankaskrá sem þú hleður inn í bankann til vinnslu, þar með talið EFT (rafræn sjóðurflutningur) í Norður-Ameríku.</span><span class="sxs-lookup"><span data-stu-id="da3b0-123">Export payments from the **Payment Journal** window to a bank file that you upload to your bank for processing, including EFT (electronic funds transfer) in North America.</span></span> |[<span data-ttu-id="da3b0-124">Hvernig á að: Flytja út greiðslur í bankaskrá</span><span class="sxs-lookup"><span data-stu-id="da3b0-124">How to: Export Payments to a Bank File</span></span>](payables-how-export-payments-bank-file.md)|  

## <a name="see-also"></a><span data-ttu-id="da3b0-125">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="da3b0-125">See Also</span></span>
[<span data-ttu-id="da3b0-126">Stjórna skuldum</span><span class="sxs-lookup"><span data-stu-id="da3b0-126">Managing Payables</span></span>](payables-manage-payables.md)  
[<span data-ttu-id="da3b0-127">Innkaup</span><span class="sxs-lookup"><span data-stu-id="da3b0-127">Purchasing</span></span>](purchasing-manage-purchasing.md)  
[<span data-ttu-id="da3b0-128">Stjórnun skulda</span><span class="sxs-lookup"><span data-stu-id="da3b0-128">Managing Receivables</span></span>](receivables-manage-receivables.md)  
<span data-ttu-id="da3b0-129">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="da3b0-129">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

