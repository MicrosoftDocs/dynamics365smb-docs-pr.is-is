---
title: "Stjórna bankareikningum| Microsoft Docs"
description: "Með reglulegu millibili þarf að afstemma bankafjárhagsfærslur við viðkomandi bankafærslur á bankareikningunum þínum."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reconcile
ms.date: 05/15/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2286b728a464943841b192031cfea13644441013
ms.openlocfilehash: 319faa64adc93c9e54cf792325daeb6a5a8e0b80
ms.contentlocale: is-is
ms.lasthandoff: 06/28/2018

---
# <a name="managing-bank-accounts"></a><span data-ttu-id="85e71-103">Stjórnun bankareikninga</span><span class="sxs-lookup"><span data-stu-id="85e71-103">Managing Bank Accounts</span></span>
<span data-ttu-id="85e71-104">Með reglulegu millibili þarf að stemma bankareikningsfærslur í [!INCLUDE[d365fin](includes/d365fin_md.md)] við viðkomandi bankafærslur í bankareikningum í bankanum þínum, og bóka svo stöðuna á þinn bankareikning.</span><span class="sxs-lookup"><span data-stu-id="85e71-104">At regular intervals, you must reconcile your bank ledger entries in [!INCLUDE[d365fin](includes/d365fin_md.md)] with the related bank transactions in bank accounts at your bank, and then post the balance to your bank account.</span></span> <span data-ttu-id="85e71-105">Hægt er að framkvæma þetta verk, annað hvort sem hluta af vinnslu á greiðslum sem koma fram á bankayfirliti í **greiðsluafstemmingarbók**.</span><span class="sxs-lookup"><span data-stu-id="85e71-105">You can perform this task either as part of processing the payments represented on a bank statement in the **Payment Reconciliation Journal**.</span></span> <span data-ttu-id="85e71-106">Einnig er hægt að framkvæma verkið aðskilið úr greiðsluvinnslu í glugganum **Afstemming bankareiknings** þar sem þú jafnar (afstemmir) bankayfirlitslínur í vinstri rúðunni við innri færslur í höfuðbók bankareikningsins þíns í hægri rúðunni.</span><span class="sxs-lookup"><span data-stu-id="85e71-106">Alternatively, you can perform the task separately from payment processing, in the **Bank Acc. Reconciliation** window where you match (reconcile) bank statement lines in the left-hand pane with your internal bank account ledger entries in the right-hand pane.</span></span> <span data-ttu-id="85e71-107">Í báðum gluggum geturðu fyllt út upplýsingar um bankayfirlit með því að flytja inn skrá eða straum og þú getur notað sjálfvirkar jöfnunarráðleggingar.</span><span class="sxs-lookup"><span data-stu-id="85e71-107">In both windows, you can fill in the bank statement information by importing a file or feed and you can use automatic matching suggestions.</span></span>

> [!NOTE]  
> <span data-ttu-id="85e71-108">Í norður-amerískum útgáfum getur þú einnig framkvæmt bankaafstemmingu í glugganum **Vinnublað bankaafstemmingar** sem er hentar betur fyrir ávísanir og innborganir en býður ekki upp á innflutning á bankayfirlitsskrám.</span><span class="sxs-lookup"><span data-stu-id="85e71-108">In North American versions, you can also perform bank reconciliation in the **Bank Rec. Worksheet** window, which is better suited for checks and deposits but does not offer import of bank statement files.</span></span> <span data-ttu-id="85e71-109">Til að nota þennan glugga í staðinn fyrir gluggann **Afstemming bankareikninga** skaltu afvelja reitinn **Bankareikn.afstemming með sjálfvirkri jöfnun** í glugganum **Fjárhagsgrunnur**.</span><span class="sxs-lookup"><span data-stu-id="85e71-109">To use this window instead of the **Bank Acc. Reconciliation** window, deselect the **Bank Recon. with Auto. Match** field in the **General Ledger Setup** window.</span></span> <span data-ttu-id="85e71-110">Frekari upplýsingar er hægt að finna í hlutanum „Afstemma bankareikninga“ sem heyrir undir staðbundnar aðgerðir Bandaríkjanna.</span><span class="sxs-lookup"><span data-stu-id="85e71-110">For more information, see the "Reconcile Bank Accounts" section under United States Local Functionality.</span></span>

<span data-ttu-id="85e71-111">Stundum þarf að færa upphæðir milli bankareikninga í [!INCLUDE[d365fin](includes/d365fin_md.md)] til að endurspegla millifærslur í bankanum þínum.</span><span class="sxs-lookup"><span data-stu-id="85e71-111">Sometimes, you need to transfer amounts between bank account in [!INCLUDE[d365fin](includes/d365fin_md.md)] to reflect transfers at your bank.</span></span> <span data-ttu-id="85e71-112">Þú framkvæmir þetta verk í flugganum **almenn Færslubók** með mismunandi hætti eftir gjaldmiðli sjóðanna.</span><span class="sxs-lookup"><span data-stu-id="85e71-112">You perform this task in the **General Journal** window, in different ways depending on the currency of the funds.</span></span>

<span data-ttu-id="85e71-113">Áður en hægt er að stjórna bankareikningum verður að stofna sérhvern bankareikning sem bankareikningsspjald.</span><span class="sxs-lookup"><span data-stu-id="85e71-113">Before you can manage bank accounts, you must set each bank account up as a bank account card.</span></span> <span data-ttu-id="85e71-114">Þar að auki þarf að setja upp rafrænar þjónustu sem má nota fyrir innflutning bankayfirlits og útflutning greiðsluskrár.</span><span class="sxs-lookup"><span data-stu-id="85e71-114">In addition, you must set up electronic services that you may use for bank statement import and payment file export.</span></span> <span data-ttu-id="85e71-115">Nánari upplýsingar um það eru í [Setja upp bankareikninga](bank-setup-banking.md).</span><span class="sxs-lookup"><span data-stu-id="85e71-115">For more information, see [Set Up Bank Accounts](bank-setup-banking.md).</span></span>

<span data-ttu-id="85e71-116">Eftirfarandi tafla lýsir röð verkefna með tenglum í efnisatriði þar sem þeim er lýst.</span><span class="sxs-lookup"><span data-stu-id="85e71-116">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>

| <span data-ttu-id="85e71-117">Til</span><span class="sxs-lookup"><span data-stu-id="85e71-117">To</span></span> | <span data-ttu-id="85e71-118">Sjá</span><span class="sxs-lookup"><span data-stu-id="85e71-118">See</span></span> |
| --- | --- |
| <span data-ttu-id="85e71-119">Afstemma bankareikninga í tengslum við greiðsluvinnslu í glugganum **greiðsluafstemmingarbók**</span><span class="sxs-lookup"><span data-stu-id="85e71-119">Reconcile bank accounts in connection with payment processing in the **Payment Reconciliation Journal** window.</span></span> |[<span data-ttu-id="85e71-120">Jafna greiðslur sjálfkrafa og afstemma bankareikninga</span><span class="sxs-lookup"><span data-stu-id="85e71-120">Applying Payments Automatically and Reconciling Bank Accounts</span></span>](receivables-apply-payments-auto-reconcile-bank-accounts.md) |
| <span data-ttu-id="85e71-121">Afstemma bankareikninga sem sérstakt verk í reitinn **afstemming bankareiknings** glugganum, þar með talið tékkafærslur.</span><span class="sxs-lookup"><span data-stu-id="85e71-121">Reconcile bank accounts, including check ledger entries, as a separate task in the **Bank Acc. Reconciliation** window.</span></span> |[<span data-ttu-id="85e71-122">Afstemma bankareikninga hvern fyrir sig</span><span class="sxs-lookup"><span data-stu-id="85e71-122">Reconcile Bank Accounts Separately</span></span>](bank-how-reconcile-bank-accounts-separately.md) |
| <span data-ttu-id="85e71-123">Bóka færslur milli bankareikninga í sama gjaldmiðli eða í öðrum gjaldmiðlum.</span><span class="sxs-lookup"><span data-stu-id="85e71-123">Post transfers between bank accounts in the same currency or in different currencies.</span></span> |[<span data-ttu-id="85e71-124">Flytja bankainnstæður</span><span class="sxs-lookup"><span data-stu-id="85e71-124">Transfer Bank Funds</span></span>](bank-how-transfer-bank-funds.md) |

## <a name="see-also"></a><span data-ttu-id="85e71-125">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="85e71-125">See Also</span></span>
[<span data-ttu-id="85e71-126">Uppsetning bankaþjónustu</span><span class="sxs-lookup"><span data-stu-id="85e71-126">Setting Up Banking</span></span>](bank-setup-banking.md)  
[<span data-ttu-id="85e71-127">Stjórnun skulda</span><span class="sxs-lookup"><span data-stu-id="85e71-127">Managing Receivables</span></span>](receivables-manage-receivables.md)  
<span data-ttu-id="85e71-128">[Stjórna skuldum](payables-manage-payables.md)  </span><span class="sxs-lookup"><span data-stu-id="85e71-128">[Managing Payables](payables-manage-payables.md)  </span></span>  
<span data-ttu-id="85e71-129">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="85e71-129">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="85e71-130">Almenn viðskiptavirkni</span><span class="sxs-lookup"><span data-stu-id="85e71-130">General Business Functionality</span></span>](ui-across-business-areas.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
 

