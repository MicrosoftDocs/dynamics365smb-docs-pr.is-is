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
ms.date: 01/10/2020
ms.author: sgroespe
ms.openlocfilehash: 0d1a38468f5d07a1170027bc728ba16996f2b782
ms.sourcegitcommit: 2f741f442226b8be74586e355f283f365e43220f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/10/2020
ms.locfileid: "2947238"
---
# <a name="reconciling-bank-accounts"></a><span data-ttu-id="5fda4-103">Afstemming bankareikninga</span><span class="sxs-lookup"><span data-stu-id="5fda4-103">Reconciling Bank Accounts</span></span>
<span data-ttu-id="5fda4-104">Ljúka ætti bankaafstemmingu með reglulegu millibili fyrir alla bankareikninga til að tryggja að peningafærslur fyrirtækisins séu réttar.</span><span class="sxs-lookup"><span data-stu-id="5fda4-104">A bank reconciliation should be completed at regular intervals for all your bank accounts to ensure that the company's cash records are correct.</span></span> <span data-ttu-id="5fda4-105">Þetta er gert með því að bera saman og jafna færslur á innri bankareikningum við bankafærslur í bankanum þínum og síðan bóka stöðurnar á innri bankareikningana svo að samtölur verði í boði fyrir fjármálastjóra.</span><span class="sxs-lookup"><span data-stu-id="5fda4-105">You do this by comparing and matching entries in your internal bank accounts with bank transactions at your bank, and then posting the balances to your internal bank accounts to make totals available to finance managers.</span></span> <span data-ttu-id="5fda4-106">Bankaafstemming er einnig hagkvæm leið til að uppgötva og leysa úr greiðslum sem vantar upp á og bókhaldsvillum.</span><span class="sxs-lookup"><span data-stu-id="5fda4-106">Bank reconciliation is also a practical way to discover and resolve missing payments and bookkeeping errors.</span></span>

<span data-ttu-id="5fda4-107">Hægt er að framkvæma verkið á síðunni **Afstemming bankareiknings** þar sem þú jafnar (afstemmir) bankayfirlitslínur í vinstri rúðunni við innri fjárhagsfærslur bankareikningsins þíns í hægri rúðunni.</span><span class="sxs-lookup"><span data-stu-id="5fda4-107">You can perform the task on the **Bank Acc. Reconciliation** page where you match (reconcile) bank statement lines in the left-hand pane with your internal bank account ledger entries in the right-hand pane.</span></span> <span data-ttu-id="5fda4-108">Annars er hægt að framkvæma þetta verk á síðunni **Greiðsluafstemmingarbók** sem hluti af úrvinnslu greiðslnanna sem koma fram á bankayfirliti.</span><span class="sxs-lookup"><span data-stu-id="5fda4-108">Alternatively, you can perform this task on the **Payment Reconciliation Journal** page as part of processing the payments that are represented on a bank statement.</span></span> <span data-ttu-id="5fda4-109">Á báðum síðunum geturðu fyllt út upplýsingar um bankayfirlit með því að flytja inn skrá eða straum og þú getur notað sjálfvirkar jöfnunarráðleggingar.</span><span class="sxs-lookup"><span data-stu-id="5fda4-109">On both pages, you can fill in the bank statement information by importing a file or feed and you can use automatic matching suggestions.</span></span>

> [!NOTE]  
> <span data-ttu-id="5fda4-110">Í norður-amerískum útgáfum getur þú einnig framkvæmt bankaafstemmingu á síðunni **Vinnublað bankaafstemmingar** sem er hentar betur fyrir ávísanir og innborganir en býður ekki upp á innflutning á bankayfirlitsskrám.</span><span class="sxs-lookup"><span data-stu-id="5fda4-110">In North American versions, you can also perform bank reconciliation on the **Bank Rec. Worksheet** page, which is better suited for checks and deposits but does not offer import of bank statement files.</span></span> <span data-ttu-id="5fda4-111">Til að nota þennan glugga í staðinn fyrir gluggann **Afstemming bankareikninga** skaltu afvelja reitinn **Bankareikn.afstemming með sjálfvirkri jöfnun** á síðunni **Fjárhagsgrunnur**.</span><span class="sxs-lookup"><span data-stu-id="5fda4-111">To use this page instead of the **Bank Acc. Reconciliation** page, deselect the **Bank Recon. with Auto. Match** field on the **General Ledger Setup** page.</span></span> <span data-ttu-id="5fda4-112">Frekari upplýsingar er hægt að finna í hlutanum „Afstemma bankareikninga“ sem heyrir undir staðbundnar aðgerðir Bandaríkjanna.</span><span class="sxs-lookup"><span data-stu-id="5fda4-112">For more information, see the "Reconcile Bank Accounts" section under United States Local Functionality.</span></span>

<span data-ttu-id="5fda4-113">Áður en hægt er að stjórna bankareikningum innan [!INCLUDE[d365fin](includes/d365fin_md.md)] verður að setja upp sérhvern bankareikning sem bankareikningsspjald.</span><span class="sxs-lookup"><span data-stu-id="5fda4-113">Before you can manage your bank accounts within [!INCLUDE[d365fin](includes/d365fin_md.md)], you must set each bank account up as a bank account card.</span></span> <span data-ttu-id="5fda4-114">Þar að auki þarf að setja upp rafrænar þjónustu sem má nota fyrir innflutning bankayfirlits og útflutning greiðsluskrár.</span><span class="sxs-lookup"><span data-stu-id="5fda4-114">In addition, you must set up electronic services that you may use for bank statement import and payment file export.</span></span> <span data-ttu-id="5fda4-115">Nánari upplýsingar um það eru í [Setja upp bankareikninga](bank-setup-banking.md).</span><span class="sxs-lookup"><span data-stu-id="5fda4-115">For more information, see [Set Up Bank Accounts](bank-setup-banking.md).</span></span>

<span data-ttu-id="5fda4-116">Eftirfarandi tafla lýsir röð verkefna með tenglum í efnisatriði þar sem þeim er lýst.</span><span class="sxs-lookup"><span data-stu-id="5fda4-116">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>

| <span data-ttu-id="5fda4-117">Til að</span><span class="sxs-lookup"><span data-stu-id="5fda4-117">To</span></span> | <span data-ttu-id="5fda4-118">Sjá</span><span class="sxs-lookup"><span data-stu-id="5fda4-118">See</span></span> |
| --- | --- |
| <span data-ttu-id="5fda4-119">Afstemmið bankareikninga sem sérstakt verk á síðunni **Afstemming bankareiknings**.</span><span class="sxs-lookup"><span data-stu-id="5fda4-119">Reconcile bank accounts as a separate task on the **Bank Acc. Reconciliation** page.</span></span> |[<span data-ttu-id="5fda4-120">Afstemma bankareikninga</span><span class="sxs-lookup"><span data-stu-id="5fda4-120">Reconcile Bank Accounts</span></span>](bank-how-reconcile-bank-accounts-separately.md) |
| <span data-ttu-id="5fda4-121">Afstemma bankareikninga í tengslum við greiðsluvinnslu á síðunni **Greiðsluafstemmingarbók**.</span><span class="sxs-lookup"><span data-stu-id="5fda4-121">Reconcile bank accounts in connection with payment processing on the **Payment Reconciliation Journal** page.</span></span> |[<span data-ttu-id="5fda4-122">Jafna greiðslur sjálfkrafa og afstemma bankareikninga</span><span class="sxs-lookup"><span data-stu-id="5fda4-122">Applying Payments Automatically and Reconciling Bank Accounts</span></span>](receivables-apply-payments-auto-reconcile-bank-accounts.md) |

## <a name="see-related-training-at-microsoft-learnlearnpathsreconcile-bank-accounts-dynamics-365-business-central"></a><span data-ttu-id="5fda4-123">Sjá tengda þjálfun á [Microsoft Learn](/learn/paths/reconcile-bank-accounts-dynamics-365-business-central/)</span><span class="sxs-lookup"><span data-stu-id="5fda4-123">See Related Training at [Microsoft Learn](/learn/paths/reconcile-bank-accounts-dynamics-365-business-central/)</span></span>

## <a name="see-also"></a><span data-ttu-id="5fda4-124">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="5fda4-124">See Also</span></span>
[<span data-ttu-id="5fda4-125">Uppsetning bankaþjónustu</span><span class="sxs-lookup"><span data-stu-id="5fda4-125">Setting Up Banking</span></span>](bank-setup-banking.md)  
[<span data-ttu-id="5fda4-126">Flytja bankainnstæður</span><span class="sxs-lookup"><span data-stu-id="5fda4-126">Transfer Bank Funds</span></span>](bank-how-transfer-bank-funds.md)  
[<span data-ttu-id="5fda4-127">Stjórnun skulda</span><span class="sxs-lookup"><span data-stu-id="5fda4-127">Managing Receivables</span></span>](receivables-manage-receivables.md)  
<span data-ttu-id="5fda4-128">[Stjórna skuldum](payables-manage-payables.md)  </span><span class="sxs-lookup"><span data-stu-id="5fda4-128">[Managing Payables](payables-manage-payables.md)  </span></span>  
<span data-ttu-id="5fda4-129">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="5fda4-129">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="5fda4-130">Almenn viðskiptavirkni</span><span class="sxs-lookup"><span data-stu-id="5fda4-130">General Business Functionality</span></span>](ui-across-business-areas.md)
