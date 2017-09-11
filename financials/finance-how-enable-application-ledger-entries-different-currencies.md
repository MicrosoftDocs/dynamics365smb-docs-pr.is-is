---
title: "Jafna færslur í mismunandi gjaldmiðlum| Microsoft Docs"
description: "Ef viðskiptamaður selur t.d. í einum gjaldmiðli og fær greitt í öðrum er hægt að jafna fjárhagsfærsluna í mismunandi gjaldmiðlum."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: multiple currencies, payment, reconcile
ms.date: 06/02/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 035f4c0e98e3b7ba308319c2017568de832e26c5
ms.contentlocale: is-is
ms.lasthandoff: 09/11/2017

---
# <a name="how-to-enable-application-of-ledger-entries-in-different-currencies"></a><span data-ttu-id="47c61-103">Hvernig á að: Leyfa jöfnun fjárhagsfærslna í mismunandi gjaldmiðlum</span><span class="sxs-lookup"><span data-stu-id="47c61-103">How to: Enable Application of Ledger Entries in Different Currencies</span></span>
<span data-ttu-id="47c61-104">Ef keypt er af lánardrottni í einum gjaldmiðli og greitt í öðrum gjaldmiðli er hægt að jafna greiðsluna innkaupunum.</span><span class="sxs-lookup"><span data-stu-id="47c61-104">If you purchase from a vendor in one currency and submit payment in another currency, you can apply the payment to the purchase.</span></span>

<span data-ttu-id="47c61-105">Á sama hátt, kaupi viðskiptamaður í einum gjaldmiðli og greiði í öðrum er hægt að jafna greiðsluna við sölureikninginn.</span><span class="sxs-lookup"><span data-stu-id="47c61-105">Likewise, if you sell to a customer in one currency and receive payment in another currency, you can apply the payment to the sales invoice.</span></span>

<span data-ttu-id="47c61-106">Eftirfarandi ferli sýnir hvernig á að setja þetta upp fyrir lánardrottnafærslur í glugganum **Uppsetning innkaupa og viðskiptaskulda**.</span><span class="sxs-lookup"><span data-stu-id="47c61-106">The following procedure describes how to set this up for vendor ledger entries in the **Purchases & Payables Setup** window.</span></span> <span data-ttu-id="47c61-107">Uppsetningin er svipuð og færslur í viðskiptamannabók í glugganum **Uppsetning sölu og viðskiptakrafna**.</span><span class="sxs-lookup"><span data-stu-id="47c61-107">The setup is similar for customer ledger entries in the **Sales & Receivables Setup** window.</span></span>

> [!NOTE]  
>   <span data-ttu-id="47c61-108">Þessi virkni krefst þess að upplifun þín sé stillt á **Pakki**.</span><span class="sxs-lookup"><span data-stu-id="47c61-108">This functionality requires that your experience is set to **Suite**.</span></span> <span data-ttu-id="47c61-109">Nánari upplýsingar, sjá [Sérstilla þína [!INCLUDE[d365fin](includes/d365fin_md.md)] upplifun](ui-experiences.md).</span><span class="sxs-lookup"><span data-stu-id="47c61-109">For more information, see [Customizing Your [!INCLUDE[d365fin](includes/d365fin_md.md)] Experience](ui-experiences.md).</span></span>

## <a name="to-enable-application-of-vendor-ledger-entries-in-different-currencies"></a><span data-ttu-id="47c61-110">Til að virkja jöfnun lánardrottnafærslna í mismunandi gjaldmiðlum</span><span class="sxs-lookup"><span data-stu-id="47c61-110">To enable application of vendor ledger entries in different currencies</span></span>
1. <span data-ttu-id="47c61-111">Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Uppsetning innkaupa og viðskiptaskulda** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="47c61-111">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Purchases & Payables Setup**, and then choose the related link.</span></span>
2. <span data-ttu-id="47c61-112">Í reitnum **Jöfnun milli gjaldmiðla** skal velja einn eftirtalinna valkosta.</span><span class="sxs-lookup"><span data-stu-id="47c61-112">In the **Appln. between Currencies** field, select one of the following options.</span></span>

| <span data-ttu-id="47c61-113">Valkostur</span><span class="sxs-lookup"><span data-stu-id="47c61-113">Option</span></span> | <span data-ttu-id="47c61-114">Lýsing</span><span class="sxs-lookup"><span data-stu-id="47c61-114">Description</span></span> |
| --- | --- |
| <span data-ttu-id="47c61-115">Engin</span><span class="sxs-lookup"><span data-stu-id="47c61-115">None</span></span> |<span data-ttu-id="47c61-116">Jöfnun milli gjaldmiðla er ekki leyfð.</span><span class="sxs-lookup"><span data-stu-id="47c61-116">Application between currencies is not allowed.</span></span> |
| <span data-ttu-id="47c61-117">EMU</span><span class="sxs-lookup"><span data-stu-id="47c61-117">EMU</span></span> |<span data-ttu-id="47c61-118">Jöfnun milli EMU-gjaldmiðla er leyfð.</span><span class="sxs-lookup"><span data-stu-id="47c61-118">Application between EMU currencies is allowed.</span></span> |
| <span data-ttu-id="47c61-119">Allt</span><span class="sxs-lookup"><span data-stu-id="47c61-119">All</span></span> |<span data-ttu-id="47c61-120">Jöfnun milli allra gjaldmiðla er leyfð.</span><span class="sxs-lookup"><span data-stu-id="47c61-120">Application between all currencies is allowed.</span></span> |

## <a name="see-also"></a><span data-ttu-id="47c61-121">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="47c61-121">See Also</span></span>
[<span data-ttu-id="47c61-122">Stjórna skuldum</span><span class="sxs-lookup"><span data-stu-id="47c61-122">Managing Payables</span></span>](payables-manage-payables.md)  
[<span data-ttu-id="47c61-123">Stjórnun skulda</span><span class="sxs-lookup"><span data-stu-id="47c61-123">Managing Receivables</span></span>](receivables-manage-receivables.md)  
<span data-ttu-id="47c61-124">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="47c61-124">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

