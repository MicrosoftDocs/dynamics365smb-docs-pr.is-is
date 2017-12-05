---
title: "Stjórna bankareikningum| Microsoft Docs"
description: "Með reglulegu millibili þarf að afstemma bankafjárahagsfærslur í Financials við viðkomandi bankafærslur á bankareikningunum þínum."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reconcile
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: daa014eaa78caa7a317b05ca92ff27c1d1530c06
ms.openlocfilehash: 2e8314c6da4da73712787a40204a964922f153f4
ms.contentlocale: is-is
ms.lasthandoff: 10/17/2017

---
# <a name="managing-bank-accounts"></a><span data-ttu-id="73639-103">Stjórnun bankareikninga</span><span class="sxs-lookup"><span data-stu-id="73639-103">Managing Bank Accounts</span></span>
<span data-ttu-id="73639-104">Með reglulegu millibili þarf að stemma bankareikningsfærslur í [!INCLUDE[d365fin](includes/d365fin_md.md)] við viðkomandi bankafærslur í bankareikningum í bankanum þínum, og bóka svo stöðuna á þinn bankareikning.</span><span class="sxs-lookup"><span data-stu-id="73639-104">At regular intervals, you must reconcile your bank ledger entries in [!INCLUDE[d365fin](includes/d365fin_md.md)] with the related bank transactions in bank accounts at your bank, and then post the balance to your bank account.</span></span> <span data-ttu-id="73639-105">Hægt er að framkvæma þetta verk, annað hvort sem hluta af vinnslu á greiðslum sem koma fram á bankayfirliti í **greiðsluafstemmingarbók**.</span><span class="sxs-lookup"><span data-stu-id="73639-105">You can perform this task either as part of processing the payments represented on a bank statement in the **Payment Reconciliation Journal**.</span></span> <span data-ttu-id="73639-106">Einnig er hægt að framkvæma verkið sérstaklega úr greiðsluvinnslu, í glugganum **Afstemming bankareiknings** sem styður tékkafærslur.</span><span class="sxs-lookup"><span data-stu-id="73639-106">Alternatively, you can perform the task separately from payment processing, in the **Bank Acc. Reconciliation** window, which supports check ledger entries.</span></span> <span data-ttu-id="73639-107">Í báðum tilvikum er fyllt í gluggann með innflutningi á bankayfirlitið í [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="73639-107">In both cases, you fill in the windows by importing the bank statement into [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

<span data-ttu-id="73639-108">Stundum þarf að færa upphæðir milli bankareikninga í [!INCLUDE[d365fin](includes/d365fin_md.md)] til að endurspegla millifærslur í bankanum þínum.</span><span class="sxs-lookup"><span data-stu-id="73639-108">Sometimes, you need to transfer amounts between bank account in [!INCLUDE[d365fin](includes/d365fin_md.md)] to reflect transfers at your bank.</span></span> <span data-ttu-id="73639-109">Þú framkvæmir þetta verk í flugganum **almenn Færslubók** með mismunandi hætti eftir gjaldmiðli sjóðanna.</span><span class="sxs-lookup"><span data-stu-id="73639-109">You perform this task in the **General Journal** window, in different ways depending on the currency of the funds.</span></span>

<span data-ttu-id="73639-110">Áður en hægt er að stjórna bankareikningum verður að stofna sérhvern bankareikning sem bankareikningsspjald.</span><span class="sxs-lookup"><span data-stu-id="73639-110">Before you can manage bank accounts, you must set each bank account up as a bank account card.</span></span> <span data-ttu-id="73639-111">Þar að auki þarf að setja upp rafrænar þjónustu sem má nota fyrir innflutning bankayfirlits og útflutning greiðsluskrár.</span><span class="sxs-lookup"><span data-stu-id="73639-111">In addition, you must set up electronic services that you may use for bank statement import and payment file export.</span></span> <span data-ttu-id="73639-112">Nánari upplýsingar um það eru í [Setja upp bankareikninga](bank-setup-banking.md).</span><span class="sxs-lookup"><span data-stu-id="73639-112">For more information, see [Set Up Bank Accounts](bank-setup-banking.md).</span></span>

<span data-ttu-id="73639-113">Eftirfarandi tafla lýsir röð verkefna með tenglum í efnisatriði þar sem þeim er lýst.</span><span class="sxs-lookup"><span data-stu-id="73639-113">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>

| <span data-ttu-id="73639-114">Til</span><span class="sxs-lookup"><span data-stu-id="73639-114">To</span></span> | <span data-ttu-id="73639-115">Sjá</span><span class="sxs-lookup"><span data-stu-id="73639-115">See</span></span> |
| --- | --- |
| <span data-ttu-id="73639-116">Afstemma bankareikninga í tengslum við greiðsluvinnslu í glugganum **greiðsluafstemmingarbók**</span><span class="sxs-lookup"><span data-stu-id="73639-116">Reconcile bank accounts in connection with payment processing in the **Payment Reconciliation Journal** window.</span></span> |[<span data-ttu-id="73639-117">Jafna greiðslur sjálfkrafa og afstemma bankareikninga</span><span class="sxs-lookup"><span data-stu-id="73639-117">Applying Payments Automatically and Reconciling Bank Accounts</span></span>](receivables-apply-payments-auto-reconcile-bank-accounts.md) |
| <span data-ttu-id="73639-118">Afstemma bankareikninga sem sérstakt verk í reitinn **afstemming bankareiknings** glugganum, þar með talið tékkafærslur.</span><span class="sxs-lookup"><span data-stu-id="73639-118">Reconcile bank accounts, including check ledger entries, as a separate task in the **Bank Acc. Reconciliation** window.</span></span> |[<span data-ttu-id="73639-119">Hvernig á að: Afstemma bankareikninga hvern fyrir sig</span><span class="sxs-lookup"><span data-stu-id="73639-119">How to: Reconcile Bank Accounts Separately</span></span>](bank-how-reconcile-bank-accounts-separately.md) |
| <span data-ttu-id="73639-120">Bóka færslur milli bankareikninga í sama gjaldmiðli eða í öðrum gjaldmiðlum.</span><span class="sxs-lookup"><span data-stu-id="73639-120">Post transfers between bank accounts in the same currency or in different currencies.</span></span> |[<span data-ttu-id="73639-121">Hvernig á að: Flytja bankainnistæður</span><span class="sxs-lookup"><span data-stu-id="73639-121">How to: Transfer Bank Funds</span></span>](bank-how-transfer-bank-funds.md) |

## <a name="see-also"></a><span data-ttu-id="73639-122">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="73639-122">See Also</span></span>
[<span data-ttu-id="73639-123">Uppsetning bankaþjónustu</span><span class="sxs-lookup"><span data-stu-id="73639-123">Setting Up Banking</span></span>](bank-setup-banking.md)  
[<span data-ttu-id="73639-124">Stjórnun skulda</span><span class="sxs-lookup"><span data-stu-id="73639-124">Managing Receivables</span></span>](receivables-manage-receivables.md)  
<span data-ttu-id="73639-125">[Stjórna skuldum](payables-manage-payables.md)  </span><span class="sxs-lookup"><span data-stu-id="73639-125">[Managing Payables](payables-manage-payables.md)  </span></span>  
<span data-ttu-id="73639-126">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="73639-126">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="73639-127">Almenn viðskiptavirkni</span><span class="sxs-lookup"><span data-stu-id="73639-127">General Business Functionality</span></span>](ui-across-business-areas.md)  

