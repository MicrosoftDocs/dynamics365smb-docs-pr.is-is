---
title: "Keyra framleiðslu | Microsoft Docs"
description: "Þegar eftirspurn hefur verið áætluð og efnið sent út samkvæmt framleiðsluuppskriftum, geta raunverulegar framleiðsluaðgerðir hafist og verið framkvæmdar í þeirri röð sem skilgreind er af framleiðslupöntunarleiðinni."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/26/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: b34f276a764f0e828fbc1f015429df9852242a4c
ms.openlocfilehash: e358e505977e2229ad7f7338fb22e0d8075b0aa9
ms.contentlocale: is-is
ms.lasthandoff: 03/22/2018

---
# <a name="manufacturing"></a><span data-ttu-id="8dccf-103">Framleiðsla</span><span class="sxs-lookup"><span data-stu-id="8dccf-103">Manufacturing</span></span>
<span data-ttu-id="8dccf-104">Þegar eftirspurn hefur verið áætluð og efnið sent út samkvæmt framleiðsluuppskriftum, geta raunverulegar framleiðsluaðgerðir hafist og verið framkvæmdar í þeirri röð sem skilgreind er af framleiðslupöntunarleiðinni.</span><span class="sxs-lookup"><span data-stu-id="8dccf-104">When demand is planned for and the materials have been issued according to production BOMs, then the actual production operations can start and be executed in the sequence defined by the production order routing.</span></span>  

<span data-ttu-id="8dccf-105">Mikilvægur hluti af framleiðslunni, hvað kerfið varðar, er að bóka frálag framleiðslu í gagnagrunninn til að sýna framvindu áætlunarinnar og uppfæra birgðir með fullbúnum vörum.</span><span class="sxs-lookup"><span data-stu-id="8dccf-105">An important part of executing production, from a system point of view, is to post production output to the database to report progress and to update inventory with the finished items.</span></span> <span data-ttu-id="8dccf-106">Hægt er að bóka frálag á handvirkan hátt með því að fylla út og bóka færslulínur eftir framleiðsluaðgerðir.</span><span class="sxs-lookup"><span data-stu-id="8dccf-106">Output posting can be done manually, by filling and posting journal lines after production operations.</span></span> <span data-ttu-id="8dccf-107">Einnig er hægt að bóka á sjálfvirkan hátt með því að nota afturvirka birgðaskráningu.</span><span class="sxs-lookup"><span data-stu-id="8dccf-107">Or, it can be done automatically with the use of backward flushing.</span></span> <span data-ttu-id="8dccf-108">Í slíkum tilvikum er efnisnotkun bókuð sjálfkrafa ásamt frálagi þegar lokið er við framleiðslupöntunina.</span><span class="sxs-lookup"><span data-stu-id="8dccf-108">In that case material consumption is automatically posted along with output when the production order changes to finished.</span></span>  

<span data-ttu-id="8dccf-109">Í stað þess að nota runubók til að bóka frálag margra framleiðslupantana má nota gluggann **Framleiðslubók** til að bóka notkun og/eða frálag fyrir tiltekna framleiðslupöntunarlínu.</span><span class="sxs-lookup"><span data-stu-id="8dccf-109">As an alternative to the batch journal for output posting for multiple production orders, you can use the **Production Journal** window to post consumption and/or output for one production order line.</span></span>

<span data-ttu-id="8dccf-110">Áður en þú getur byrjað að framleiða vöru, er nauðsynlegt að búa til ýmsar uppsetningar, eins og vinnustöðvar, leiðir og framleiðsluuppskriftir.</span><span class="sxs-lookup"><span data-stu-id="8dccf-110">Before you can begin to produce items, you must make various setup, such as work centers, routings, and production BOMs.</span></span> <span data-ttu-id="8dccf-111">Nánari upplýsingar er að finna í [Uppsetning framleiðslu](production-configure-production-processes.md).</span><span class="sxs-lookup"><span data-stu-id="8dccf-111">For more information, see [Setting Up Manufacturing](production-configure-production-processes.md).</span></span>

<span data-ttu-id="8dccf-112">Eftirfarandi tafla lýsir röð verkefna með tenglum í efnisatriði þar sem þeim er lýst.</span><span class="sxs-lookup"><span data-stu-id="8dccf-112">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>   

|<span data-ttu-id="8dccf-113">**Til að**</span><span class="sxs-lookup"><span data-stu-id="8dccf-113">**To**</span></span>|<span data-ttu-id="8dccf-114">**Sjá**</span><span class="sxs-lookup"><span data-stu-id="8dccf-114">**See**</span></span>|  
|------------|-------------|  
|<span data-ttu-id="8dccf-115">Skilja hvernig framleiðsla gengur fyrir sig.</span><span class="sxs-lookup"><span data-stu-id="8dccf-115">Understand how production orders work.</span></span>|[<span data-ttu-id="8dccf-116">Um framleiðslupantanir</span><span class="sxs-lookup"><span data-stu-id="8dccf-116">About Production Orders</span></span>](production-about-production-orders.md)|
|<span data-ttu-id="8dccf-117">Stofnun framleiðslupantana handvirkt</span><span class="sxs-lookup"><span data-stu-id="8dccf-117">Create production orders manually.</span></span>|[<span data-ttu-id="8dccf-118">Stofnun framleiðslupantana</span><span class="sxs-lookup"><span data-stu-id="8dccf-118">Create Production Orders</span></span>](production-how-to-create-production-orders.md)|
|<span data-ttu-id="8dccf-119">Útvista öllum eða völdum aðgerðum í framleiðslupöntun til undirverktaka.</span><span class="sxs-lookup"><span data-stu-id="8dccf-119">Outsource all or selected operations in a production order to a subcontractor.</span></span>|[<span data-ttu-id="8dccf-120">Úthýsa framleiðslu til undirverktaka</span><span class="sxs-lookup"><span data-stu-id="8dccf-120">Subcontract Manufacturing</span></span>](production-how-to-subcontract-manufacturing.md)|
|<span data-ttu-id="8dccf-121">Skrá og bóka frálag framleiðslu ásamt efnis- og tímanotkun fyrir eina útgefna framleiðslupöntunarlínu.</span><span class="sxs-lookup"><span data-stu-id="8dccf-121">Record and post production output along with material and time consumption for a single released production order line.</span></span>|[<span data-ttu-id="8dccf-122">Bóka notkun og frálag fyrir eina útgefna framleiðslupöntunarlínu</span><span class="sxs-lookup"><span data-stu-id="8dccf-122">Post Consumption and Output for One Released Production Order Line</span></span>](production-how-to-register-consumption-and-output.md)|  
|<span data-ttu-id="8dccf-123">Fjöldabóka magn íhluta notað á aðgerð, í færslubók sem getur unnið fjölda áætlaðra framleiðslupantana.</span><span class="sxs-lookup"><span data-stu-id="8dccf-123">Batch post the quantity of components used per operation in a journal that can processes multiple planned production orders.</span></span>|[<span data-ttu-id="8dccf-124">Fjöldabóka notkun</span><span class="sxs-lookup"><span data-stu-id="8dccf-124">Batch Post Consumption</span></span>](production-how-to-post-consumption.md)|
|<span data-ttu-id="8dccf-125">Bóka magn tilbúinna vara og tíma eytt á aðgerð, í færslubók sem getur unnið fjölda útgefinna framleiðslupantana.</span><span class="sxs-lookup"><span data-stu-id="8dccf-125">Post the quantity of finished items and the time spent per operation in a journal that can processes multiple released production orders.</span></span>|[<span data-ttu-id="8dccf-126">Fjöldabóka frálag og keyrslutíma</span><span class="sxs-lookup"><span data-stu-id="8dccf-126">Batch Post Output and Run Times</span></span>](production-how-to-post-output-quantity.md)|  
|<span data-ttu-id="8dccf-127">Bóka fjölda vara sem framleiddar eru í hverri lokinni aðgerð sem ekki teljast til tilbúinnar vöru heldur sem úrkast.</span><span class="sxs-lookup"><span data-stu-id="8dccf-127">Post the number of items produced in each finished operation which do not qualify as finished output, but as scrapped material.</span></span>|[<span data-ttu-id="8dccf-128">Bóka úrkast</span><span class="sxs-lookup"><span data-stu-id="8dccf-128">Post Scrap</span></span>](production-how-to-post-scrap.md)|
|<span data-ttu-id="8dccf-129">Skoða álag á vinnusal sem afleiðingu útgefinna og afgreiddra framleiðslupantana.</span><span class="sxs-lookup"><span data-stu-id="8dccf-129">View the shop floor load as a result of planned and released production orders.</span></span>|[<span data-ttu-id="8dccf-130">Skoða álag á vinnu- og vélastöðvar</span><span class="sxs-lookup"><span data-stu-id="8dccf-130">View the Load in Work and Machine Centers</span></span>](production-how-to-view-the-load-on-work-centers.md)|      
|<span data-ttu-id="8dccf-131">Nota gluggann **Afkastagetubók** til að bóka notaða afkastagetu sem ekki er úthlutað á framleiðslupöntun, líkt og viðhaldsvinna.</span><span class="sxs-lookup"><span data-stu-id="8dccf-131">Use the **Capacity Journal** window to post consumed capacities that are not assigned to a production order, such as maintenance work.</span></span>|[<span data-ttu-id="8dccf-132">Bóka afkastagetu</span><span class="sxs-lookup"><span data-stu-id="8dccf-132">Post Capacities</span></span>](production-how-to-post-capacities.md)|  
|<span data-ttu-id="8dccf-133">Reikna út og jafna kostnað við tilbúnar framleiðsluvörur og íhluti sem notaðir voru til afstemmingar.</span><span class="sxs-lookup"><span data-stu-id="8dccf-133">Calculate and adjust the cost of finished production items and consumed components for financial reconciliation.</span></span>|[<span data-ttu-id="8dccf-134">Um lokinn framleiðslupantanakostnað</span><span class="sxs-lookup"><span data-stu-id="8dccf-134">About Finished Production Order Costs</span></span>](finance-about-finished-production-order-costs.md)|  

## <a name="see-also"></a><span data-ttu-id="8dccf-135">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="8dccf-135">See Also</span></span>  
[<span data-ttu-id="8dccf-136">Uppsetning framleiðslu</span><span class="sxs-lookup"><span data-stu-id="8dccf-136">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="8dccf-137">[Áætlun](production-planning.md)    </span><span class="sxs-lookup"><span data-stu-id="8dccf-137">[Planning](production-planning.md)    </span></span>  
[<span data-ttu-id="8dccf-138">Birgðir</span><span class="sxs-lookup"><span data-stu-id="8dccf-138">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="8dccf-139">Innkaup</span><span class="sxs-lookup"><span data-stu-id="8dccf-139">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="8dccf-140">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="8dccf-140">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
## [!INCLUDE[d365fin](includes/training_link_md.md)]

