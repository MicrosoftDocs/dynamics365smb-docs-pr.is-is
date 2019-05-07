---
title: Stjórna bankareikningum| Microsoft Docs
description: Með reglulegu millibili þarf að afstemma bankafjárhagsfærslur við viðkomandi bankafærslur á bankareikningunum þínum.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reconcile
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 25e1242541e98cc47e2fcc4f016a860ad08c635d
ms.sourcegitcommit: addfb47612cc2e4e98dfd7e338b6f41cde405d5c
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/16/2019
ms.locfileid: "939130"
---
# <a name="managing-bank-accounts"></a><span data-ttu-id="d17a9-103">Stjórnun bankareikninga</span><span class="sxs-lookup"><span data-stu-id="d17a9-103">Managing Bank Accounts</span></span>
<span data-ttu-id="d17a9-104">Með reglulegu millibili þarf að stemma bankareikningsfærslur í [!INCLUDE[d365fin](includes/d365fin_md.md)] við viðkomandi bankafærslur í bankareikningum í bankanum þínum, og bóka svo stöðuna á þinn bankareikning.</span><span class="sxs-lookup"><span data-stu-id="d17a9-104">At regular intervals, you must reconcile your bank ledger entries in [!INCLUDE[d365fin](includes/d365fin_md.md)] with the related bank transactions in bank accounts at your bank, and then post the balance to your bank account.</span></span> <span data-ttu-id="d17a9-105">Hægt er að framkvæma þetta verk, annað hvort sem hluta af vinnslu á greiðslum sem koma fram á bankayfirliti í **greiðsluafstemmingarbók**.</span><span class="sxs-lookup"><span data-stu-id="d17a9-105">You can perform this task either as part of processing the payments represented on a bank statement in the **Payment Reconciliation Journal**.</span></span> <span data-ttu-id="d17a9-106">Einnig er hægt að framkvæma verkið aðskilið úr greiðsluvinnslu á síðunni **Afstemming bankareiknings** þar sem þú jafnar (afstemmir) bankayfirlitslínur í vinstri rúðunni við innri færslur í höfuðbók bankareikningsins þíns í hægri rúðunni.</span><span class="sxs-lookup"><span data-stu-id="d17a9-106">Alternatively, you can perform the task separately from payment processing, on the **Bank Acc. Reconciliation** page where you match (reconcile) bank statement lines in the left-hand pane with your internal bank account ledger entries in the right-hand pane.</span></span> <span data-ttu-id="d17a9-107">Á báðum síðunum geturðu fyllt út upplýsingar um bankayfirlit með því að flytja inn skrá eða straum og þú getur notað sjálfvirkar jöfnunarráðleggingar.</span><span class="sxs-lookup"><span data-stu-id="d17a9-107">In both pages, you can fill in the bank statement information by importing a file or feed and you can use automatic matching suggestions.</span></span>

> [!NOTE]  
> <span data-ttu-id="d17a9-108">Í norður-amerískum útgáfum getur þú einnig framkvæmt bankaafstemmingu á síðunni **Vinnublað bankaafstemmingar** sem er hentar betur fyrir ávísanir og innborganir en býður ekki upp á innflutning á bankayfirlitsskrám.</span><span class="sxs-lookup"><span data-stu-id="d17a9-108">In North American versions, you can also perform bank reconciliation on the **Bank Rec. Worksheet** page, which is better suited for checks and deposits but does not offer import of bank statement files.</span></span> <span data-ttu-id="d17a9-109">Til að nota þennan glugga í staðinn fyrir gluggann **Afstemming bankareikninga** skaltu afvelja reitinn **Bankareikn.afstemming með sjálfvirkri jöfnun** á síðunni **Fjárhagsgrunnur**.</span><span class="sxs-lookup"><span data-stu-id="d17a9-109">To use this page instead of the **Bank Acc. Reconciliation** page, deselect the **Bank Recon. with Auto. Match** field on the **General Ledger Setup** page.</span></span> <span data-ttu-id="d17a9-110">Frekari upplýsingar er hægt að finna í hlutanum „Afstemma bankareikninga“ sem heyrir undir staðbundnar aðgerðir Bandaríkjanna.</span><span class="sxs-lookup"><span data-stu-id="d17a9-110">For more information, see the "Reconcile Bank Accounts" section under United States Local Functionality.</span></span>

<span data-ttu-id="d17a9-111">Stundum þarf að færa upphæðir milli bankareikninga í [!INCLUDE[d365fin](includes/d365fin_md.md)] til að endurspegla millifærslur í bankanum þínum.</span><span class="sxs-lookup"><span data-stu-id="d17a9-111">Sometimes, you need to transfer amounts between bank account in [!INCLUDE[d365fin](includes/d365fin_md.md)] to reflect transfers at your bank.</span></span> <span data-ttu-id="d17a9-112">Þú framkvæmir þetta verk á síðunni **almenn Færslubók** með mismunandi hætti eftir gjaldmiðli sjóðanna.</span><span class="sxs-lookup"><span data-stu-id="d17a9-112">You perform this task on the **General Journal** page, in different ways depending on the currency of the funds.</span></span>

<span data-ttu-id="d17a9-113">Áður en hægt er að stjórna bankareikningum verður að stofna sérhvern bankareikning sem bankareikningsspjald.</span><span class="sxs-lookup"><span data-stu-id="d17a9-113">Before you can manage bank accounts, you must set each bank account up as a bank account card.</span></span> <span data-ttu-id="d17a9-114">Þar að auki þarf að setja upp rafrænar þjónustu sem má nota fyrir innflutning bankayfirlits og útflutning greiðsluskrár.</span><span class="sxs-lookup"><span data-stu-id="d17a9-114">In addition, you must set up electronic services that you may use for bank statement import and payment file export.</span></span> <span data-ttu-id="d17a9-115">Nánari upplýsingar um það eru í [Setja upp bankareikninga](bank-setup-banking.md).</span><span class="sxs-lookup"><span data-stu-id="d17a9-115">For more information, see [Set Up Bank Accounts](bank-setup-banking.md).</span></span>

<span data-ttu-id="d17a9-116">Eftirfarandi tafla lýsir röð verkefna með tenglum í efnisatriði þar sem þeim er lýst.</span><span class="sxs-lookup"><span data-stu-id="d17a9-116">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>

| <span data-ttu-id="d17a9-117">Til</span><span class="sxs-lookup"><span data-stu-id="d17a9-117">To</span></span> | <span data-ttu-id="d17a9-118">Sjá</span><span class="sxs-lookup"><span data-stu-id="d17a9-118">See</span></span> |
| --- | --- |
| <span data-ttu-id="d17a9-119">Afstemma bankareikninga í tengslum við greiðsluvinnslu á síðunni **Greiðsluafstemmingarbók**.</span><span class="sxs-lookup"><span data-stu-id="d17a9-119">Reconcile bank accounts in connection with payment processing on the **Payment Reconciliation Journal** page.</span></span> |[<span data-ttu-id="d17a9-120">Jafna greiðslur sjálfkrafa og afstemma bankareikninga</span><span class="sxs-lookup"><span data-stu-id="d17a9-120">Applying Payments Automatically and Reconciling Bank Accounts</span></span>](receivables-apply-payments-auto-reconcile-bank-accounts.md) |
| <span data-ttu-id="d17a9-121">Afstemma bankareikninga sem sérstakt verk á síðunni **Afstemming bankareiknings**, þar með talið tékkafærslur.</span><span class="sxs-lookup"><span data-stu-id="d17a9-121">Reconcile bank accounts, including check ledger entries, as a separate task on the **Bank Acc. Reconciliation** page.</span></span> |[<span data-ttu-id="d17a9-122">Afstemma bankareikninga hvern fyrir sig</span><span class="sxs-lookup"><span data-stu-id="d17a9-122">Reconcile Bank Accounts Separately</span></span>](bank-how-reconcile-bank-accounts-separately.md) |
| <span data-ttu-id="d17a9-123">Bóka færslur milli bankareikninga í sama gjaldmiðli eða í öðrum gjaldmiðlum.</span><span class="sxs-lookup"><span data-stu-id="d17a9-123">Post transfers between bank accounts in the same currency or in different currencies.</span></span> |[<span data-ttu-id="d17a9-124">Flytja bankainnstæður</span><span class="sxs-lookup"><span data-stu-id="d17a9-124">Transfer Bank Funds</span></span>](bank-how-transfer-bank-funds.md) |

## <a name="see-also"></a><span data-ttu-id="d17a9-125">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="d17a9-125">See Also</span></span>
[<span data-ttu-id="d17a9-126">Uppsetning bankaþjónustu</span><span class="sxs-lookup"><span data-stu-id="d17a9-126">Setting Up Banking</span></span>](bank-setup-banking.md)  
[<span data-ttu-id="d17a9-127">Stjórnun skulda</span><span class="sxs-lookup"><span data-stu-id="d17a9-127">Managing Receivables</span></span>](receivables-manage-receivables.md)  
<span data-ttu-id="d17a9-128">[Stjórna skuldum](payables-manage-payables.md)  </span><span class="sxs-lookup"><span data-stu-id="d17a9-128">[Managing Payables](payables-manage-payables.md)  </span></span>  
<span data-ttu-id="d17a9-129">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="d17a9-129">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="d17a9-130">Almenn viðskiptavirkni</span><span class="sxs-lookup"><span data-stu-id="d17a9-130">General Business Functionality</span></span>](ui-across-business-areas.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
 
