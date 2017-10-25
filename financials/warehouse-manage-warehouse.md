---
title: "Vöruhúsaaðgerðir | Microsoft Docs"
description: "Eftir að tekið hefur verið á móti vörum og áður en vörur eru afhentar, fer röð vöruhúsaaðgerða fram til þess að tryggja að flæði gegnum vöruhúsið sé skilvirkt og til að skipuleggja og viðhalda birgðum fyrirtækisins."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/15/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: c1ea1c4a5ea4b917243d60981ec35050895f82a7
ms.contentlocale: is-is
ms.lasthandoff: 09/22/2017

---
# <a name="warehouse-management"></a><span data-ttu-id="da70f-103">Vöruhúsastjórnun</span><span class="sxs-lookup"><span data-stu-id="da70f-103">Warehouse Management</span></span>
<span data-ttu-id="da70f-104">Eftir að tekið hefur verið á móti vörum og áður en vörur eru afhentar, fer röð vöruhúsaaðgerða fram til þess að tryggja að flæði gegnum vöruhúsið sé skilvirkt og til að skipuleggja og viðhalda birgðum fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="da70f-104">After goods are received and before goods are shipped, a series of internal warehouse activities take place to ensure an effective flow through the warehouse and to organize and maintain company inventories.</span></span>

<span data-ttu-id="da70f-105">Dæmigerðar vöruhúsaaðgerðir felast í frágangi vöru, færslu á vörum inni í eða milli vöruhúsa og tínslu á vörum fyrir samsetningu, framleiðslu eða afhendingu.</span><span class="sxs-lookup"><span data-stu-id="da70f-105">Typical warehouse activities include putting items away, moving items inside or between warehouses, and picking items for assembly, production, or shipment.</span></span> <span data-ttu-id="da70f-106">Vörusamsetning fyrir sölu eða birgðir geta einnig talist til vöruhúsaðgerða, en um það er fjallað annarsstaðar.</span><span class="sxs-lookup"><span data-stu-id="da70f-106">Assembling items for sale or inventory may also be considered warehouse activities, but these are covered elsewhere.</span></span> <span data-ttu-id="da70f-107">Nánari upplýsingar, sjá [Samsetningarstjórnun](assembly-assemble-items.md).</span><span class="sxs-lookup"><span data-stu-id="da70f-107">For more information, see [Assembly Management](assembly-assemble-items.md).</span></span>  

<span data-ttu-id="da70f-108">Í stórum vöruhúsum er hægt að aðskilja mismunandi meðhöndlunarverk með deildum og samhæfingu sem stjórnað er með stýrðu verkflæði.</span><span class="sxs-lookup"><span data-stu-id="da70f-108">In large warehouses, these different handling tasks can be separated by departments and the integration managed by a directed workflow.</span></span> <span data-ttu-id="da70f-109">Í einfaldari uppsetningum er flæðið ekki jafn formfast og vöruhúsaaðgerðir eru framkvæmdar með svokölluðum birgðafrágangi og -tínslu.</span><span class="sxs-lookup"><span data-stu-id="da70f-109">In simpler installations, the flow is less formalized and the warehouse activities are performed with so-called inventory put-aways and inventory picks.</span></span> <span data-ttu-id="da70f-110">Nánari upplýsingar um mismunandi vöruhúsaflækjustig, einfalt og ítarlegt, eru í [Hönnunarupplýsingar: Vöruhúsayfirlit](design-details-warehouse-overview.md).</span><span class="sxs-lookup"><span data-stu-id="da70f-110">For more information about basic versus advanced warehouse configurations, see [Design Details: Warehouse Overview](design-details-warehouse-overview.md).</span></span>

<span data-ttu-id="da70f-111">Áður en þú framkvæmir vöruhúsaaðgerðir, er nauðsynlegt að setja kerfið upp fyrir viðeigandi flækjustig vöruhúsaferla.</span><span class="sxs-lookup"><span data-stu-id="da70f-111">Before you can perform warehouse activities, you must set the system up for the relevant complexity of warehouse processing.</span></span> <span data-ttu-id="da70f-112">Nánari upplýsingar er að finna í [Uppsetning vöruhúsastjórnunar](warehouse-setup-warehouse.md).</span><span class="sxs-lookup"><span data-stu-id="da70f-112">For more information, see [Setting Up Warehouse Management](warehouse-setup-warehouse.md).</span></span>

 <span data-ttu-id="da70f-113">Eftirfarandi tafla lýsir röð verkefna með tenglum í efnisatriði þar sem þeim er lýst.</span><span class="sxs-lookup"><span data-stu-id="da70f-113">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>   

|<span data-ttu-id="da70f-114">**Til að**</span><span class="sxs-lookup"><span data-stu-id="da70f-114">**To**</span></span>|<span data-ttu-id="da70f-115">**Sjá**</span><span class="sxs-lookup"><span data-stu-id="da70f-115">**See**</span></span>|  
|------------|-------------|  
|<span data-ttu-id="da70f-116">Skrá móttöku vara í vöruhúsabirgðageymslum, annað hvort með innkaupapöntun eingöngu, í einfaldri birgðageymsluuppsetningu, eða með vöruhúsamóttöku, ef skyldi vera sjálfvirkt vöruhúsaferli, að hluta eða í heild, í birgðageymslunni.</span><span class="sxs-lookup"><span data-stu-id="da70f-116">Record the receipt of items at warehouse locations, either with a purchase order only, in simple location setups, or with a warehouse receipt, in case of semi or fully automated warehouse processing at the location.</span></span>|[<span data-ttu-id="da70f-117">Hvernig á að: Taka á við vörum</span><span class="sxs-lookup"><span data-stu-id="da70f-117">How to: Receive Items</span></span>](warehouse-how-receive-items.md)|
|<span data-ttu-id="da70f-118">Tengja framhjá frágangs- og tínsluferlinu til að flýta vöru beint frá móttöku eða framleiðslu yfir í afhendingu.</span><span class="sxs-lookup"><span data-stu-id="da70f-118">Bypass the put-away and pick processes to expedite an item straight from receiving or production to shipping.</span></span>|[<span data-ttu-id="da70f-119">Hvernig á að: Hjáskipa vörur</span><span class="sxs-lookup"><span data-stu-id="da70f-119">How to: Cross-Dock Items</span></span>](warehouse-how-to-cross-dock-items.md)|    
|<span data-ttu-id="da70f-120">Ganga frá vörum sem eru mótteknar vegna innkaupa, söluvöruskila, flutnings eða framleiðslufrálagi samkvæmt tilgreindu aðgerðaflæði vöruhúss.</span><span class="sxs-lookup"><span data-stu-id="da70f-120">Put away items received from purchases, sales returns, transfers, or production output according to the configured warehouse process.</span></span>|[<span data-ttu-id="da70f-121">Gengið frá vörum</span><span class="sxs-lookup"><span data-stu-id="da70f-121">Putting Items Away</span></span>](warehouse-put-away-items.md)|
|<span data-ttu-id="da70f-122">Færa vörur milli hólfa í vöruhúsinu.</span><span class="sxs-lookup"><span data-stu-id="da70f-122">Move items between bins in the warehouse.</span></span>|[<span data-ttu-id="da70f-123">Færa vörur</span><span class="sxs-lookup"><span data-stu-id="da70f-123">Moving Items</span></span>](warehouse-move-items.md)|
|<span data-ttu-id="da70f-124">Tína til vörur fyrir afhendingu, flutning eða til notkunar í framleiðslu eða samsetningu, samkvæmt tilgreindu aðgerðaflæði vöruhúss.</span><span class="sxs-lookup"><span data-stu-id="da70f-124">Pick items to be shipped, transferred, or consumed in assembly or production, according to the configured warehouse process.</span></span>|[<span data-ttu-id="da70f-125">Tína vörur</span><span class="sxs-lookup"><span data-stu-id="da70f-125">Picking Items</span></span>](warehouse-pick-items.md)|
|<span data-ttu-id="da70f-126">Skrá afhendingu vara frá vöruhúsabirgðageymslum, annað hvort með sölupöntun eingöngu, í einfaldri birgðageymsluuppsetningu, eða með vöruhúsaafhendingu, ef skyldi vera sjálfvirkt vöruhúsaferli, að hluta eða í heild, í birgðageymslunni.</span><span class="sxs-lookup"><span data-stu-id="da70f-126">Record the shipment of items from warehouse locations, either with a sales order only, in simple location setups, or with a warehouse shipment, in case of semi or fully automated warehouse processes at the location.</span></span>|[<span data-ttu-id="da70f-127">Hvernig á að: Afgreiða vörur</span><span class="sxs-lookup"><span data-stu-id="da70f-127">How to: Ship Items</span></span>](warehouse-how-ship-items.md)|  

## <a name="see-also"></a><span data-ttu-id="da70f-128">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="da70f-128">See Also</span></span>  
 [<span data-ttu-id="da70f-129">Birgðir</span><span class="sxs-lookup"><span data-stu-id="da70f-129">Inventory</span></span>](inventory-manage-inventory.md)  
 <span data-ttu-id="da70f-130">[Vöruhúsastjórnun sett upp](warehouse-setup-warehouse.md)   </span><span class="sxs-lookup"><span data-stu-id="da70f-130">[Setting Up Warehouse Management](warehouse-setup-warehouse.md)   </span></span>  
 <span data-ttu-id="da70f-131">[Samsetningardeild](assembly-assemble-items.md)  </span><span class="sxs-lookup"><span data-stu-id="da70f-131">[Assembly Management](assembly-assemble-items.md)  </span></span>  
[<span data-ttu-id="da70f-132">Hönnunarupplýsingar vöruhúsakerfi</span><span class="sxs-lookup"><span data-stu-id="da70f-132">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
 <span data-ttu-id="da70f-133">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="da70f-133">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

