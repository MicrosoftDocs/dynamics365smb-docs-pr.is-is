---
title: "Hönnunarupplýsingar - Meðhöndlun endurpöntunarstefnu | Microsoft Docs"
description: "Yfirlit yfir verkhluta sem taka til skilgreininga á endurpöntunarstefnu í framboðsáætlun."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 2a6658508f8e12a11989d54da6d6c8e3a36631cc
ms.contentlocale: is-is
ms.lasthandoff: 09/22/2017

---
# <a name="design-details-handling-reordering-policies"></a><span data-ttu-id="f1bd7-103">Hönnunarupplýsingar: Meðhöndlun endurpöntunarstefnur</span><span class="sxs-lookup"><span data-stu-id="f1bd7-103">Design Details: Handling Reordering Policies</span></span>
<span data-ttu-id="f1bd7-104">Til þess að vara geti tekið þátt í birgðaáætlunargerð verður að tilgreina endurpöntunarstefnu.</span><span class="sxs-lookup"><span data-stu-id="f1bd7-104">For an item to participate in supply planning, a reorder policy must be defined.</span></span> <span data-ttu-id="f1bd7-105">Eftirfarandi fjórar endurpöntunarstefnur eru til:</span><span class="sxs-lookup"><span data-stu-id="f1bd7-105">The following four reordering policies exist:</span></span>  
  
* <span data-ttu-id="f1bd7-106">Fast endurpöntunarmagn</span><span class="sxs-lookup"><span data-stu-id="f1bd7-106">Fixed Reorder Qty.</span></span>  
* <span data-ttu-id="f1bd7-107">Hámarksmagn</span><span class="sxs-lookup"><span data-stu-id="f1bd7-107">Maximum Qty.</span></span>  
* <span data-ttu-id="f1bd7-108">Röð</span><span class="sxs-lookup"><span data-stu-id="f1bd7-108">Order</span></span>  
* <span data-ttu-id="f1bd7-109">Lotu-fyrir-lotu</span><span class="sxs-lookup"><span data-stu-id="f1bd7-109">Lot-for-Lot</span></span>  
  
<span data-ttu-id="f1bd7-110">Stefnur um fast endurpöntunarmagn og hámarksmagn tengjast birgðaáætlunargerð.</span><span class="sxs-lookup"><span data-stu-id="f1bd7-110">Fixed Reorder Qty. and Maximum Qty. policies relate to inventory planning.</span></span> <span data-ttu-id="f1bd7-111">Þó birgðaáætlanagerð sé tæknilega einfaldari en mótbókunaraðferð eru þessar stefnur báðar til með nákvæmri mótbókun framboðs og pöntunarrakningu.</span><span class="sxs-lookup"><span data-stu-id="f1bd7-111">Although inventory planning is technically simpler than the balancing procedure, these policies must coexist with the step-by-step balancing of supply and order tracking.</span></span> <span data-ttu-id="f1bd7-112">Til að stjórna samþættingu milli tveggja, og að veita sýnileika í þátt áætlanagerð rökfræði, strangar reglur gilda hversu endurröðun reglur eru meðhöndlaðar.</span><span class="sxs-lookup"><span data-stu-id="f1bd7-112">To control the integration between the two, and to provide visibility into the involved planning logic, strict principles govern how reordering policies are handled.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="f1bd7-113">Í þessum hluta</span><span class="sxs-lookup"><span data-stu-id="f1bd7-113">In This Section</span></span>  
[<span data-ttu-id="f1bd7-114">Hönnunarupplýsingar: Hlutverk endurpöntunarmarks</span><span class="sxs-lookup"><span data-stu-id="f1bd7-114">Design Details: The Role of the Reorder Point</span></span>](design-details-the-role-of-the-reorder-point.md)  
[<span data-ttu-id="f1bd7-115">Hönnunarupplýsingar Vöktun áætlaðar birgðastigs og endurpöntunarmark</span><span class="sxs-lookup"><span data-stu-id="f1bd7-115">Design Details: Monitoring the Projected Inventory Level and the Reorder Point</span></span>](design-details-monitoring-the-projected-inventory-level-and-the-reorder-point.md)  
[<span data-ttu-id="f1bd7-116">Hönnunarupplýsingar: Hlutverk tímaramma</span><span class="sxs-lookup"><span data-stu-id="f1bd7-116">Design Details: The Role of the Time Bucket</span></span>](design-details-the-role-of-the-time-bucket.md)  
[<span data-ttu-id="f1bd7-117">Hönnunarupplýsingar: undir yfirflæðisstigi</span><span class="sxs-lookup"><span data-stu-id="f1bd7-117">Design Details: Staying under the Overflow Level</span></span>](design-details-staying-under-the-overflow-level.md)  
[<span data-ttu-id="f1bd7-118">Hönnunarupplýsingar: Meðhöndlun Áætlaðrar Neikvæðra birgða</span><span class="sxs-lookup"><span data-stu-id="f1bd7-118">Design Details: Handling Projected Negative Inventory</span></span>](design-details-handling-projected-negative-inventory.md)  
[<span data-ttu-id="f1bd7-119">Hönnunarupplýsingar: Endurpöntunarstefnur</span><span class="sxs-lookup"><span data-stu-id="f1bd7-119">Design Details: Reordering Policies</span></span>](design-details-reordering-policies.md)  
  
## <a name="see-also"></a><span data-ttu-id="f1bd7-120">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="f1bd7-120">See Also</span></span>  
<span data-ttu-id="f1bd7-121">[Hönnunarupplýsingar: áætlunarfæribreyta](design-details-planning-parameters.md) </span><span class="sxs-lookup"><span data-stu-id="f1bd7-121">[Design Details: Planning Parameters](design-details-planning-parameters.md) </span></span>  
<span data-ttu-id="f1bd7-122">[Hönnunarupplýsingar: áætlunartafla](design-details-planning-assignment-table.md) </span><span class="sxs-lookup"><span data-stu-id="f1bd7-122">[Design Details: Planning Assignment Table](design-details-planning-assignment-table.md) </span></span>  
<span data-ttu-id="f1bd7-123">[Hönnunarupplýsingar: Miðlægar hugmyndir áætlanakerfisins](design-details-central-concepts-of-the-planning-system.md) </span><span class="sxs-lookup"><span data-stu-id="f1bd7-123">[Design Details: Central Concepts of the Planning System](design-details-central-concepts-of-the-planning-system.md) </span></span>  
<span data-ttu-id="f1bd7-124">[Hönnunarupplýsingar: Jöfnun eftirspurnar og framboðs](design-details-balancing-demand-and-supply.md) </span><span class="sxs-lookup"><span data-stu-id="f1bd7-124">[Design Details: Balancing Demand and Supply](design-details-balancing-demand-and-supply.md) </span></span>  
[<span data-ttu-id="f1bd7-125">Hönnunarupplýsingar: framboðsáætlun</span><span class="sxs-lookup"><span data-stu-id="f1bd7-125">Design Details: Supply Planning</span></span>](design-details-supply-planning.md)
