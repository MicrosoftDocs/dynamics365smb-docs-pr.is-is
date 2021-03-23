---
title: Jafna færslur í mismunandi gjaldmiðlum| Microsoft Docs
description: Ef viðskiptamaður selur t.d. í einum gjaldmiðli og fær greitt í öðrum er hægt að jafna fjárhagsfærsluna í mismunandi gjaldmiðlum.
services: project-madeira
documentationcenter: ''
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: multiple currencies, payment, reconcile
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 83b054b09f1015b988aed55acf9e75d93ab99f4e
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5386475"
---
# <a name="enable-application-of-ledger-entries-in-different-currencies"></a><span data-ttu-id="e522f-103">Leyfa jöfnun fjárhagsfærslna í mismunandi gjaldmiðlum</span><span class="sxs-lookup"><span data-stu-id="e522f-103">Enable Application of Ledger Entries in Different Currencies</span></span>
<span data-ttu-id="e522f-104">Ef keypt er af lánardrottni í einum gjaldmiðli og greitt í öðrum gjaldmiðli er hægt að jafna greiðsluna innkaupunum.</span><span class="sxs-lookup"><span data-stu-id="e522f-104">If you purchase from a vendor in one currency and submit payment in another currency, you can apply the payment to the purchase.</span></span>

<span data-ttu-id="e522f-105">Á sama hátt, kaupi viðskiptamaður í einum gjaldmiðli og greiði í öðrum er hægt að jafna greiðsluna við sölureikninginn.</span><span class="sxs-lookup"><span data-stu-id="e522f-105">Likewise, if you sell to a customer in one currency and receive payment in another currency, you can apply the payment to the sales invoice.</span></span>

<span data-ttu-id="e522f-106">Eftirfarandi ferli sýnir hvernig á að setja þetta upp fyrir lánardrottnafærslur á síðunni **Uppsetning innkaupa og viðskiptaskulda**.</span><span class="sxs-lookup"><span data-stu-id="e522f-106">The following procedure describes how to set this up for vendor ledger entries on the **Purchases & Payables Setup** page.</span></span> <span data-ttu-id="e522f-107">Uppsetningin er svipuð og færslur viðskiptamannabókar á síðunni **Uppsetning sölu og viðskiptakrafna**.</span><span class="sxs-lookup"><span data-stu-id="e522f-107">The setup is similar for customer ledger entries on the **Sales & Receivables Setup** page.</span></span>

## <a name="to-enable-application-of-vendor-ledger-entries-in-different-currencies"></a><span data-ttu-id="e522f-108">Til að virkja jöfnun lánardrottnafærslna í mismunandi gjaldmiðlum</span><span class="sxs-lookup"><span data-stu-id="e522f-108">To enable application of vendor ledger entries in different currencies</span></span>
1. <span data-ttu-id="e522f-109">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Uppsetning innkaupagrunns** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="e522f-109">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Purchases & Payables Setup**, and then choose the related link.</span></span>
2. <span data-ttu-id="e522f-110">Í reitnum **Jöfnun milli gjaldmiðla** skal velja einn eftirtalinna valkosta.</span><span class="sxs-lookup"><span data-stu-id="e522f-110">In the **Appln. between Currencies** field, select one of the following options.</span></span>

| <span data-ttu-id="e522f-111">Valkostur</span><span class="sxs-lookup"><span data-stu-id="e522f-111">Option</span></span> | <span data-ttu-id="e522f-112">Lýsing</span><span class="sxs-lookup"><span data-stu-id="e522f-112">Description</span></span> |
| --- | --- |
| <span data-ttu-id="e522f-113">Engin</span><span class="sxs-lookup"><span data-stu-id="e522f-113">None</span></span> |<span data-ttu-id="e522f-114">Jöfnun milli gjaldmiðla er ekki leyfð.</span><span class="sxs-lookup"><span data-stu-id="e522f-114">Application between currencies is not allowed.</span></span> |
| <span data-ttu-id="e522f-115">EMU</span><span class="sxs-lookup"><span data-stu-id="e522f-115">EMU</span></span> |<span data-ttu-id="e522f-116">Jöfnun milli EMU-gjaldmiðla er leyfð.</span><span class="sxs-lookup"><span data-stu-id="e522f-116">Application between EMU currencies is allowed.</span></span> |
| <span data-ttu-id="e522f-117">Allt</span><span class="sxs-lookup"><span data-stu-id="e522f-117">All</span></span> |<span data-ttu-id="e522f-118">Jöfnun milli allra gjaldmiðla er leyfð.</span><span class="sxs-lookup"><span data-stu-id="e522f-118">Application between all currencies is allowed.</span></span> |

## <a name="to-set-up-gl-accounts-for-currency-application-rounding-differences"></a><span data-ttu-id="e522f-119">Uppsetning fjárhagsreikninga fyrir gjaldmiðilsaðgerð sléttunarmismunar</span><span class="sxs-lookup"><span data-stu-id="e522f-119">To set up G/L accounts for currency application rounding differences</span></span>  
<span data-ttu-id="e522f-120">Eigi að jafna færslur í mismunandi gjaldmiðlum þarf að setja upp fjárhagsreikninga þar sem á að bóka sléttunarmismun.</span><span class="sxs-lookup"><span data-stu-id="e522f-120">If you apply entries in different currencies, you must set up the general ledger accounts to which you want to post rounding differences.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="e522f-121">Setja verður upp fjárhagsreikningana áður en lokið er við verkið.</span><span class="sxs-lookup"><span data-stu-id="e522f-121">You must set up the general ledger accounts before you complete the task.</span></span> <span data-ttu-id="e522f-122">Frekari upplýsingar er að finna í [Að skilja fjárhag og bókhaldslykla](finance-general-ledger.md).</span><span class="sxs-lookup"><span data-stu-id="e522f-122">For more information, see [Understanding the General Ledger and the Chart of Accounts](finance-general-ledger.md).</span></span>

1. <span data-ttu-id="e522f-123">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Bókunarflokkar viðskiptamanns** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="e522f-123">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Customer Posting Groups**, and then choose the related link.</span></span>  
2. <span data-ttu-id="e522f-124">Í reitunum **Debet gjaldm.jöfn.slétt.reikn** og **Kreditreikn. gjaldeyrisjöfn.** er fært inn viðkomandi fjárhagsreikningsnúmer til að bóka sléttunarmismun.</span><span class="sxs-lookup"><span data-stu-id="e522f-124">In the **Debit Curr. Appln. Rndg. Acc.** and **Credit Curr. Appln. Rndg. Acc.** fields, enter the relevant general ledger accounts to post rounding differences.</span></span>  
3. <span data-ttu-id="e522f-125">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Bókunarflokkar lánardrottins** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="e522f-125">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Vendor Posting Groups**, and then choose the related link.</span></span>  
4. <span data-ttu-id="e522f-126">Í reitunum **Debet gjaldm.jöfn.slétt.reikn** og **Kreditreikn. gjaldeyrisjöfn.** er fært inn viðkomandi fjárhagsreikningsnúmer til að bóka sléttunarmismun.</span><span class="sxs-lookup"><span data-stu-id="e522f-126">In the **Debit Curr. Appln. Rndg. Acc.** and **Credit Curr. Appln. Rndg. Acc.** fields, enter the relevant general ledger accounts to post rounding differences.</span></span>  

## <a name="see-also"></a><span data-ttu-id="e522f-127">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="e522f-127">See Also</span></span>
[<span data-ttu-id="e522f-128">Stjórna skuldum</span><span class="sxs-lookup"><span data-stu-id="e522f-128">Managing Payables</span></span>](payables-manage-payables.md)  
[<span data-ttu-id="e522f-129">Stjórnun skulda</span><span class="sxs-lookup"><span data-stu-id="e522f-129">Managing Receivables</span></span>](receivables-manage-receivables.md)  
<span data-ttu-id="e522f-130">[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="e522f-130">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]