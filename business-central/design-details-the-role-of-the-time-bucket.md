---
title: Hönnunarupplýsingar - Hlutverk tímarammi | Microsoft Docs
description: Tilgangurinn með tímarammanum er að safna saman eftirspurnartilvikum innan tímasíðunnar til að útbúa sameiginlega birgðapöntun.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
redirect_url: design-details-handling-reordering-policies
ms.openlocfilehash: 54d4a4aed94b562b82d94d6a5a75a3050c054fc3
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/29/2019
ms.locfileid: "1239315"
---
# <a name="design-details-the-role-of-the-time-bucket"></a><span data-ttu-id="eab7f-103">Hönnunarupplýsingar: Hlutverk tímaramma</span><span class="sxs-lookup"><span data-stu-id="eab7f-103">Design Details: The Role of the Time Bucket</span></span>
<span data-ttu-id="eab7f-104">Tilgangurinn með tímarammanum er að safna saman eftirspurnartilvikum innan tímasíðunnar til að útbúa sameiginlega birgðapöntun.</span><span class="sxs-lookup"><span data-stu-id="eab7f-104">The purpose of the time bucket is to collect demand events within the time page in order to make a joint supply order.</span></span>  

 <span data-ttu-id="eab7f-105">Fyrir endurpöntunarstefnur sem nota endurpöntunarmark er hægt að skilgreina tímaramma.</span><span class="sxs-lookup"><span data-stu-id="eab7f-105">For reordering policies that use a reorder point, you can define a time bucket.</span></span> <span data-ttu-id="eab7f-106">Þetta tryggir að eftirspurn innan sama tímabils sé safnað upp áður en áhrifin á áætlaðar birgðir eru könnuð, og hvort endurpöntunarmarki hafi verið náð.</span><span class="sxs-lookup"><span data-stu-id="eab7f-106">This ensures that demand within the same time period is accumulated before checking the impact on the projected inventory and whether the reorder point has been passed.</span></span> <span data-ttu-id="eab7f-107">Ef farið er yfir endurpöntunarmarkið er ný birgðapöntun áætluð framvirkt frá lokum tímabilsins sem skilgreint er í tímarammanum.</span><span class="sxs-lookup"><span data-stu-id="eab7f-107">If the reorder point is passed, a new supply order is scheduled forward from the end of the period defined by the time bucket.</span></span> <span data-ttu-id="eab7f-108">Tímaramminn hefst á upphafsdagsetningu áætlunar.</span><span class="sxs-lookup"><span data-stu-id="eab7f-108">The time buckets begin on the planning starting date.</span></span>  

 <span data-ttu-id="eab7f-109">Tímaramminn endurspeglar það handvirka ferli að kanna birgðastigið oft fremur en fyrir hverja færslu.</span><span class="sxs-lookup"><span data-stu-id="eab7f-109">The time-bucketed concept reflects the manual process of checking the inventory level on a frequent basis rather than for each transaction.</span></span> <span data-ttu-id="eab7f-110">Notandinn verður að tilgreina tíðnina (tímarammann).</span><span class="sxs-lookup"><span data-stu-id="eab7f-110">The user needs to define the frequency (the time bucket).</span></span> <span data-ttu-id="eab7f-111">Til dæmis safnar notandinn saman öllum vöruþörfum frá einum lánardrottni til að leggja inn vikulega pöntun.</span><span class="sxs-lookup"><span data-stu-id="eab7f-111">For example, the user gathers all item needs from one vendor to place a weekly order.</span></span>  

 <span data-ttu-id="eab7f-112">![Dæmi um tímaramma í skipulagningu](media/nav_app_supply_planning_2_reorder_cycle.png "Dæmi um tímaramma í skipulagningu")</span><span class="sxs-lookup"><span data-stu-id="eab7f-112">![Example of time bucket in planning](media/nav_app_supply_planning_2_reorder_cycle.png "Example of time bucket in planning")</span></span>  

 <span data-ttu-id="eab7f-113">Tímaramminn er vanalega notaður til að forðast keðjuverkun.</span><span class="sxs-lookup"><span data-stu-id="eab7f-113">The time bucket is generally used to avoid a cascade effect.</span></span> <span data-ttu-id="eab7f-114">Til dæmis jöfn lína framboðs og eftirspurnar þar sem fyrri eftirspurn er afturkölluð eða ný búin til.</span><span class="sxs-lookup"><span data-stu-id="eab7f-114">For example, a balanced row of demand and supply where an early demand is canceled, or a new one is created.</span></span> <span data-ttu-id="eab7f-115">Niðurstaðan ætti að vera sú að framboðspöntunin (nema sú síðasta) er enduráætluð.</span><span class="sxs-lookup"><span data-stu-id="eab7f-115">The result would be that every supply order (except the last one) is rescheduled.</span></span>  

## <a name="see-also"></a><span data-ttu-id="eab7f-116">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="eab7f-116">See Also</span></span>  
 <span data-ttu-id="eab7f-117">[Hönnunarupplýsingar: Endurpöntunarstefnur](design-details-reordering-policies.md) </span><span class="sxs-lookup"><span data-stu-id="eab7f-117">[Design Details: Reordering Policies](design-details-reordering-policies.md) </span></span>  
 <span data-ttu-id="eab7f-118">[Hönnunarupplýsingar: áætlunarfæribreyta](design-details-planning-parameters.md) </span><span class="sxs-lookup"><span data-stu-id="eab7f-118">[Design Details: Planning Parameters](design-details-planning-parameters.md) </span></span>  
 <span data-ttu-id="eab7f-119">[Hönnunarupplýsingar: Meðhöndlun endurpöntunarstefna](design-details-handling-reordering-policies.md) </span><span class="sxs-lookup"><span data-stu-id="eab7f-119">[Design Details: Handling Reordering Policies](design-details-handling-reordering-policies.md) </span></span>  
 [<span data-ttu-id="eab7f-120">Hönnunarupplýsingar: framboðsáætlun</span><span class="sxs-lookup"><span data-stu-id="eab7f-120">Design Details: Supply Planning</span></span>](design-details-supply-planning.md)
