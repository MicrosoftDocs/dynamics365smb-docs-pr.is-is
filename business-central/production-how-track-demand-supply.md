---
title: "Hvernig á að rekja tengsl milli eftirspurnar og framboðs | Microsoft Docs"
description: "Frá hverju framboðs- eða eftirspurnarskjali í hinu svokallaða pöntunarneti, geturðu rakið pöntunareftirspurn (rakið magn), spá, standandi sölupöntun eða áætlunarfæribreytu (órakið magn) sem á við umrædda áætlunarlínu."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 2300cc6e3f4c429cd73a17939420a44b846a3b13
ms.contentlocale: is-is
ms.lasthandoff: 09/28/2018

---
# <a name="track-relations-between-demand-and-supply"></a><span data-ttu-id="a9af1-103">Rekja tengsl milli eftirspurnar og framboðs</span><span class="sxs-lookup"><span data-stu-id="a9af1-103">Track Relations Between Demand and Supply</span></span>
<span data-ttu-id="a9af1-104">Frá hverju framboðs- eða eftirspurnarskjali í hinu svokallaða pöntunarneti, geturðu rakið pöntunareftirspurn (rakið magn), spá, standandi sölupöntun eða áætlunarfæribreytu (órakið magn) sem á við umrædda áætlunarlínu.</span><span class="sxs-lookup"><span data-stu-id="a9af1-104">From any supply or demand document in the so-called order network, you can track the order demand (tracked quantity), forecast, blanket sales order, or planning parameter (untracked quantity) that has given rise to the planning line in question.</span></span>

<span data-ttu-id="a9af1-105">Áætlunarvinnublöðin bjóða einnig hjálplegar áætlunarupplýsingar um ópantaðar einingar, til að aðstoða skipuleggjandann við að búa til fullkomna framboðsáætlun.</span><span class="sxs-lookup"><span data-stu-id="a9af1-105">The planning worksheets also offers supporting planning information about non-order entities to help the planner obtain an optimal supply plan.</span></span> <span data-ttu-id="a9af1-106">Sjá hlutann „Óraktar áætlunareiningar“ fyrir frekari upplýsingar.</span><span class="sxs-lookup"><span data-stu-id="a9af1-106">For more information, see the "Untracked Planning Elements" section.</span></span>

## <a name="to-track-linked-items"></a><span data-ttu-id="a9af1-107">Rekja tengdar vörur</span><span class="sxs-lookup"><span data-stu-id="a9af1-107">To track linked items</span></span>
<span data-ttu-id="a9af1-108">Pöntunarrakningin sýnir hvernig sölupantanir, framleiðslupantanir og innkaupapantanir tengjast aðalframleiðslupöntuninni í gegnum áætlanir og frátekningarkerfi.</span><span class="sxs-lookup"><span data-stu-id="a9af1-108">Order tracking shows how sales orders, production orders, and purchase orders are related to the manufacturing order through the planning and reservation systems.</span></span>

<span data-ttu-id="a9af1-109">Eftirfarandi lýsir hvernig rekja skal tengdar vörur í fastáætlunarpöntun.</span><span class="sxs-lookup"><span data-stu-id="a9af1-109">The following describes how to track linked items on a firm planned production order.</span></span> <span data-ttu-id="a9af1-110">Skrefin eru svipuð fyrir allar aðrar tegundir af pöntunum, og frá áætlunarvinnublaðslínum.</span><span class="sxs-lookup"><span data-stu-id="a9af1-110">The steps are similar for all other order types, and from planning worksheet lines.</span></span>

1. <span data-ttu-id="a9af1-111">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Fastáætluð framl.pöntun** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="a9af1-111">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Firm Planned Prod. Order**, and then choose the related link.</span></span>
2. <span data-ttu-id="a9af1-112">Viðeigandi fastáætluð framleiðslupöntun er opnuð úr listanum.</span><span class="sxs-lookup"><span data-stu-id="a9af1-112">Open the relevant firm planned production order from the list.</span></span>
3. <span data-ttu-id="a9af1-113">Á flýtiflipanum **Línur** skal velja aðgerðina **Aðgerðir**, og velja svo aðgerðina **Pöntunarrakning**.</span><span class="sxs-lookup"><span data-stu-id="a9af1-113">On the **Lines** FastTab, choose the **Functions** action, and then choose the **Order Tracking** action.</span></span>

<span data-ttu-id="a9af1-114">Línurnar í glugganum **Pöntunarrakning** sýna fylgiskjölin sem tengjast gildandi framleiðslupöntunarlínunni.</span><span class="sxs-lookup"><span data-stu-id="a9af1-114">The lines in the **Order Tracking** display the documents that are related to the current production order line.</span></span>

## <a name="untracked-planning-elements"></a><span data-ttu-id="a9af1-115">Órakin áætlunaratriði</span><span class="sxs-lookup"><span data-stu-id="a9af1-115">Untracked Planning Elements</span></span>
<span data-ttu-id="a9af1-116">Glugginn **Óraktar áætlunareiningar** opnast þegar þú velur **Órakið magn** reitinn í **Pantanaáætlun** glugginn.</span><span class="sxs-lookup"><span data-stu-id="a9af1-116">The **Untracked Planning Elements** window opens when you choose the **Untracked Qty.** field in the **order Planning** window.</span></span> <span data-ttu-id="a9af1-117">Það þjónar tvenns konar tilgangi:</span><span class="sxs-lookup"><span data-stu-id="a9af1-117">It serves two purposes:</span></span>

1. <span data-ttu-id="a9af1-118">Að geyma upplýsingar um órakið magn sem birtist þegar notandi flettir upp í glugganum Rakning pöntunar til að sjá órakið magn.</span><span class="sxs-lookup"><span data-stu-id="a9af1-118">To hold information about untracked quantities displayed when the user looks up from the Order Tracking window to see untracked quantities.</span></span>
2. <span data-ttu-id="a9af1-119">Að geyma viðvörunarboð sem birtast þegar notandi smellir á **Viðvörun** tákn á **áætlunarvinnublaði** glugganum.</span><span class="sxs-lookup"><span data-stu-id="a9af1-119">To hold warning messages displayed when the user chooses the **Warning** icon in the **Planning Worksheet** window.</span></span>

<span data-ttu-id="a9af1-120">Glugginn inniheldur færslur sem standa fyrir órakið umframmagn í pöntunarrakningarkerfi.</span><span class="sxs-lookup"><span data-stu-id="a9af1-120">The window contains entries which account for an untracked surplus quantity in order tracking network.</span></span> <span data-ttu-id="a9af1-121">Þessar færslur eru stofnaðar við áætlunarkeyrslu og útskýra hvaðan órakta umframmagnið í rakningarlínunum kom.</span><span class="sxs-lookup"><span data-stu-id="a9af1-121">These entries are generated during the planning run and explain where the untracked surplus quantity in the order tracking lines came from.</span></span> <span data-ttu-id="a9af1-122">Þetta órakta umframmagn kom frá:</span><span class="sxs-lookup"><span data-stu-id="a9af1-122">This untracked surplus can come from:</span></span>

- <span data-ttu-id="a9af1-123">Framleiðsluspá</span><span class="sxs-lookup"><span data-stu-id="a9af1-123">Production forecast</span></span>
- <span data-ttu-id="a9af1-124">Standandi pantanir</span><span class="sxs-lookup"><span data-stu-id="a9af1-124">Blanket orders</span></span>
- <span data-ttu-id="a9af1-125">Magn í öryggisbirgðum</span><span class="sxs-lookup"><span data-stu-id="a9af1-125">Safety stock quantity</span></span>
- <span data-ttu-id="a9af1-126">Endurpöntunarmark</span><span class="sxs-lookup"><span data-stu-id="a9af1-126">Reorder point</span></span>
- <span data-ttu-id="a9af1-127">Hámarksbirgðir</span><span class="sxs-lookup"><span data-stu-id="a9af1-127">Maximum inventory</span></span>
- <span data-ttu-id="a9af1-128">Pöntunarmagn</span><span class="sxs-lookup"><span data-stu-id="a9af1-128">Reorder quantity</span></span>
- <span data-ttu-id="a9af1-129">Hámarksmagn pöntunar</span><span class="sxs-lookup"><span data-stu-id="a9af1-129">Maximum order quantity</span></span>
- <span data-ttu-id="a9af1-130">Lágmarksmagn pöntunar</span><span class="sxs-lookup"><span data-stu-id="a9af1-130">Minimum order quantity</span></span>
- <span data-ttu-id="a9af1-131">Fjöldapanta</span><span class="sxs-lookup"><span data-stu-id="a9af1-131">Order multiple</span></span>
- <span data-ttu-id="a9af1-132">Hömlur (% af lotustærð)</span><span class="sxs-lookup"><span data-stu-id="a9af1-132">Dampener (% of lot size)</span></span>

## <a name="see-also"></a><span data-ttu-id="a9af1-133">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="a9af1-133">See Also</span></span>  
<span data-ttu-id="a9af1-134">[Áætlun](production-planning.md) </span><span class="sxs-lookup"><span data-stu-id="a9af1-134">[Planning](production-planning.md) </span></span>  
[<span data-ttu-id="a9af1-135">Uppsetning framleiðslu</span><span class="sxs-lookup"><span data-stu-id="a9af1-135">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="a9af1-136">[Framleiðsla](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="a9af1-136">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
[<span data-ttu-id="a9af1-137">Birgðir</span><span class="sxs-lookup"><span data-stu-id="a9af1-137">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="a9af1-138">Innkaup</span><span class="sxs-lookup"><span data-stu-id="a9af1-138">Purchasing</span></span>](purchasing-manage-purchasing.md)  
[<span data-ttu-id="a9af1-139">Hönnunarupplýsingar: Frátekning, rakning og aðgerðarboð</span><span class="sxs-lookup"><span data-stu-id="a9af1-139">Design Details: Reservation, Tracking, and Action Messaging</span></span>](design-details-reservation-order-tracking-and-action-messaging.md)  
<span data-ttu-id="a9af1-140">[Hönnunarupplýsingar: framboðsáætlun](design-details-supply-planning.md) </span><span class="sxs-lookup"><span data-stu-id="a9af1-140">[Design Details: Supply Planning](design-details-supply-planning.md) </span></span>  
[<span data-ttu-id="a9af1-141">Uppsetning bestu venja: Framboðsáætlun</span><span class="sxs-lookup"><span data-stu-id="a9af1-141">Setup Best Practices: Supply Planning</span></span>](setup-best-practices-supply-planning.md)  
<span data-ttu-id="a9af1-142">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="a9af1-142">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

