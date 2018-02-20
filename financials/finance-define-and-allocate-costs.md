---
title: "Skilgreina og úthluta kostnaði | Microsoft Docs"
description: "Kostnaðarúthlutun færir kostnað og tekjur milli kostnaðargerða, kostnaðarstaða og kostnaðhluta. Hægt er að tilgreina eins margar línur og þörf krefur."
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
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 04e5a95b7a926528cc26c254390d08e3bce6ad8a
ms.contentlocale: is-is
ms.lasthandoff: 01/30/2018

---
# <a name="defining-and-allocating-costs"></a><span data-ttu-id="a8740-104">Skilgreina og úthluta kostnaði</span><span class="sxs-lookup"><span data-stu-id="a8740-104">Defining and Allocating Costs</span></span>
<span data-ttu-id="a8740-105">Kostnaðarúthlutun færir kostnað og tekjur milli kostnaðargerða, kostnaðarstaða og kostnaðhluta.</span><span class="sxs-lookup"><span data-stu-id="a8740-105">Cost allocations move costs and revenues between cost types, cost centers, and cost objects.</span></span> <span data-ttu-id="a8740-106">Hægt er að tilgreina eins margar línur og þörf krefur.</span><span class="sxs-lookup"><span data-stu-id="a8740-106">You can define as many allocations as you need.</span></span> <span data-ttu-id="a8740-107">Hver úthlutun samanstendur af:</span><span class="sxs-lookup"><span data-stu-id="a8740-107">Each allocation consists of:</span></span>  

-   <span data-ttu-id="a8740-108">Úthlutunaruppruni.</span><span class="sxs-lookup"><span data-stu-id="a8740-108">An allocation source.</span></span>  
-   <span data-ttu-id="a8740-109">Eitt eða fleiri úthlutunarmörk.</span><span class="sxs-lookup"><span data-stu-id="a8740-109">One or more allocation targets.</span></span>  

<span data-ttu-id="a8740-110">Úthlutunaruppruninn kveður á um hvaða kostnaði verður að úthluta, og úthlutunarmörk skilgreina hvert kostnaðinum skuli úthlutað.</span><span class="sxs-lookup"><span data-stu-id="a8740-110">The allocation source establishes which costs must be allocated, and the allocation targets determine where the costs must be allocated.</span></span> <span data-ttu-id="a8740-111">Til dæmis getur úthlutunaruppruninn verið kostnaðurinn fyrir kostnaðartegundina Rafmagn og hiti.</span><span class="sxs-lookup"><span data-stu-id="a8740-111">For example, an allocation source can be the costs for the Electricity and Heating cost type.</span></span> <span data-ttu-id="a8740-112">Öllum rafmagns- og hitakostnaði er úthlutað á þrjá kostnaðarstaði: Verkstæði, Framleiðslu og Sölu.</span><span class="sxs-lookup"><span data-stu-id="a8740-112">You allocate all electricity and heating costs to three cost centers: Workshop, Production, and Sales.</span></span> <span data-ttu-id="a8740-113">Þessir kostnaðarstaðir eru það sem úthluta skal á.</span><span class="sxs-lookup"><span data-stu-id="a8740-113">These cost centers are your allocation targets.</span></span>  

<span data-ttu-id="a8740-114">Fyrir hvern úthlutunaruppruna skilgreinir notandi úthlutunarstig, gildistímabil og afbrigði sem flokkunarkenni.</span><span class="sxs-lookup"><span data-stu-id="a8740-114">For each allocation source, you define an allocation level, a validity period, and a variant as grouping identifier.</span></span> <span data-ttu-id="a8740-115">Hægt er að nota keyrslu til að setja afmarkanir til að velja úthlutunarskilgreiningar og keyra síðan kostnaðarúthlutun . sjálfkrafa.</span><span class="sxs-lookup"><span data-stu-id="a8740-115">You can use a batch job to set filters to select allocation definitions and then run cost allocations automatically.</span></span>  

<span data-ttu-id="a8740-116">Fyrir hvert úthlutunarmarki skilgreinir notandi úthlutunarstofninn.</span><span class="sxs-lookup"><span data-stu-id="a8740-116">For each allocation target, you define an allocation base.</span></span> <span data-ttu-id="a8740-117">Úthlutunarstofn getur annað hvort verið fastur eða kvikur.</span><span class="sxs-lookup"><span data-stu-id="a8740-117">The allocation base can be either static or dynamic.</span></span>  

-   <span data-ttu-id="a8740-118">Fastir úthlutunargrunnar eru byggðir á tilteknu gildi, s.s. ferfetum eða skilgreindu úthlutunarhlutfalli, s.s. 5:2:4.</span><span class="sxs-lookup"><span data-stu-id="a8740-118">Static allocation bases are based on a definite value, such as square footage or an established allocation ratio, such as 5:2:4.</span></span>  
-   <span data-ttu-id="a8740-119">Kvik úthlutun fer eftir breytanlegum gildum, eins og fjölda starfsmanna í kostnaðarstöð eða sölutekjum kostnaðarliðar á tilteknu tímabili.</span><span class="sxs-lookup"><span data-stu-id="a8740-119">Dynamic allocation bases depend on changeable values, such as the number of employees in a cost center or sales revenue of a cost object throughout a certain time period.</span></span>  

<span data-ttu-id="a8740-120">Eftirfarandi tafla lýsir röð verkefna með tenglum í efnisatriði þar sem þeim er lýst.</span><span class="sxs-lookup"><span data-stu-id="a8740-120">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>

|<span data-ttu-id="a8740-121">Til</span><span class="sxs-lookup"><span data-stu-id="a8740-121">To</span></span>|<span data-ttu-id="a8740-122">Sjá</span><span class="sxs-lookup"><span data-stu-id="a8740-122">See</span></span>|  
|--------|---------|  
|<span data-ttu-id="a8740-123">Uppsetning úthlutunaruppruna og úthlutunarmarka hans.</span><span class="sxs-lookup"><span data-stu-id="a8740-123">Set up allocation source and its targets.</span></span>|[<span data-ttu-id="a8740-124">Setja upp uppruna og markhópa úthlutanna</span><span class="sxs-lookup"><span data-stu-id="a8740-124">Set Up Allocation Source and Targets</span></span>](finance-how-to-set-up-allocation-source-and-targets.md)|  
|<span data-ttu-id="a8740-125">Setja upp margvíslegar afmarkanir fyrir kvik úthlutunargrunna.</span><span class="sxs-lookup"><span data-stu-id="a8740-125">Set up various filters for dynamic allocation bases.</span></span>|[<span data-ttu-id="a8740-126">Uppsetning afmarkanir fyrir Kvik úthlutunargrunnar.</span><span class="sxs-lookup"><span data-stu-id="a8740-126">Setting Filters for Dynamic Allocation Bases</span></span>](finance-setting-filters-for-dynamic-allocation-bases.md)|  
|<span data-ttu-id="a8740-127">Sjá dæmi um hvernig á að skilgreina fasta úthlutun.</span><span class="sxs-lookup"><span data-stu-id="a8740-127">See an example of how to define a static allocation.</span></span>|[<span data-ttu-id="a8740-128">Dæmi: Skilgreining fastrar úthlutunar á grundvelli úthlutunarhlutfalls</span><span class="sxs-lookup"><span data-stu-id="a8740-128">Scenario Example: Defining Static Allocations Based on Allocation Ratio</span></span>](finance-scenario-example-defining-static-allocations-based-on-allocation-ratio.md)|  
|<span data-ttu-id="a8740-129">Sjá dæmi um hvernig á að skilgreina kvika úthlutun.</span><span class="sxs-lookup"><span data-stu-id="a8740-129">See an example of how to define a dynamic allocation.</span></span>|[<span data-ttu-id="a8740-130">Dæmi: Skilgreining kvikrar úthlutunar á grundvelli seldra vara</span><span class="sxs-lookup"><span data-stu-id="a8740-130">Scenario Example: Defining Dynamic Allocations Based on Items Sold</span></span>](finance-scenario-example-defining-dynamic-allocations-based-on-items-sold.md)|  

## <a name="see-also"></a><span data-ttu-id="a8740-131">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="a8740-131">See Also</span></span>  
 <span data-ttu-id="a8740-132">[Uppsetning kostnaðarbókhalds](finance-set-up-cost-accounting.md) </span><span class="sxs-lookup"><span data-stu-id="a8740-132">[Setting Up Cost Accounting](finance-set-up-cost-accounting.md) </span></span>  
 <span data-ttu-id="a8740-133">[Flytja og bóka kostnaðarfærslur](finance-transfer-and-post-cost-entries.md) </span><span class="sxs-lookup"><span data-stu-id="a8740-133">[Transferring and Posting Cost Entries](finance-transfer-and-post-cost-entries.md) </span></span>  
 <span data-ttu-id="a8740-134">[Kostnaðarreikningur](finance-manage-cost-accounting.md) </span><span class="sxs-lookup"><span data-stu-id="a8740-134">[Accounting for Costs](finance-manage-cost-accounting.md) </span></span>  
 <span data-ttu-id="a8740-135">[Orðalisti í kostnaðarbókhaldi](finance-terminology-in-cost-accounting.md) </span><span class="sxs-lookup"><span data-stu-id="a8740-135">[Terminology in Cost Accounting](finance-terminology-in-cost-accounting.md) </span></span>  
 [<span data-ttu-id="a8740-136">Um kostnaðarbókhald</span><span class="sxs-lookup"><span data-stu-id="a8740-136">About Cost Accounting</span></span>](finance-about-cost-accounting.md)

