---
title: "Birgðakostnaði stjórnað | Microsoft Docs"
description: "Kostnaðarstýring snýst um að skrá og tilkynna kostnað við starfsemi fyrirtækisins. Það felur í sér skráningu framleiðslukostnaðar og vörukostnaðar, það er, virði vara."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/29/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: e2443552440cae8a0d90753d9a56fdc82006a197
ms.contentlocale: is-is
ms.lasthandoff: 01/30/2018

---
# <a name="managing-inventory-costs"></a><span data-ttu-id="905a9-104">Birgðakostnaði stjórnað</span><span class="sxs-lookup"><span data-stu-id="905a9-104">Managing Inventory Costs</span></span>
<span data-ttu-id="905a9-105">Kostnaðarstýring snýst um að skrá og tilkynna kostnað við starfsemi fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="905a9-105">Cost management, also referred to as “costing”, is concerned with recording and reporting business operating costs.</span></span> <span data-ttu-id="905a9-106">Það felur í sér skráningu framleiðslukostnaðar og vörukostnaðar, það er, virði vara.</span><span class="sxs-lookup"><span data-stu-id="905a9-106">It includes the reporting of manufacturing costs and inventory costs, that is, the value of items.</span></span>   

<span data-ttu-id="905a9-107">Grundvallaratriðin sem öðlast þarf skilning á eru að kostnaðaraðferðir skilgreina hvernig virði vara er metið þegar þær eru teknar úr birgðum, að kostnaðarbreyting uppfærir kostnað við seldar vörur með tengdum innkaupakostnaði sem bókaður er eftir söluna og að birgðavirði þarf að bóka í sérstaka fjárhagsreikninga með reglulegu millibili.</span><span class="sxs-lookup"><span data-stu-id="905a9-107">Central principles to understand are that costing methods define how items are valued when they leave inventory, that cost adjustment updates the cost of goods sold with related purchase costs posted after the sale, and that inventory values must be posted to dedicated G/L accounts at regular intervals.</span></span>

<span data-ttu-id="905a9-108">Eftirfarandi tafla lýsir röð verkefna með tenglum í efnisatriði þar sem þeim er lýst.</span><span class="sxs-lookup"><span data-stu-id="905a9-108">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>

|<span data-ttu-id="905a9-109">**Til að**</span><span class="sxs-lookup"><span data-stu-id="905a9-109">**To**</span></span>|<span data-ttu-id="905a9-110">**Sjá**</span><span class="sxs-lookup"><span data-stu-id="905a9-110">**See**</span></span>|  
|------------|-------------|  
|<span data-ttu-id="905a9-111">Gott er að lesa margvíslegar upplýsingar um hugtök til að skilja forsendur og skilgreiningar sem stýra reikningskostnaðarhluta [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="905a9-111">Read various conceptual information to understand the principles and definitions that govern the inventory costing accounting functionality in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>|[<span data-ttu-id="905a9-112">Um birgðakostnað</span><span class="sxs-lookup"><span data-stu-id="905a9-112">About Inventory Costing</span></span>](finance-learn-about-costing.md)|  
|<span data-ttu-id="905a9-113">Uppsetning birgðatímabil, kostnaðaraðferðir og sléttunaraðferðir.</span><span class="sxs-lookup"><span data-stu-id="905a9-113">Set up inventory periods, costing methods, and rounding methods.</span></span>|[<span data-ttu-id="905a9-114">Uppsetning birgðaverðmats og kostnaðar</span><span class="sxs-lookup"><span data-stu-id="905a9-114">Setting Up Inventory Valuation and Costing</span></span>](finance-set-up-inventory-valuation-and-costing.md)|
|<span data-ttu-id="905a9-115">Hækka eða lækka virði einnar eða fleiri vara í birgðaskrá með því að bóka núverandi, útreiknað virði þeirra.</span><span class="sxs-lookup"><span data-stu-id="905a9-115">Appreciate or depreciate the value of one or more items in inventory by posting their current, calculated value.</span></span>|[<span data-ttu-id="905a9-116">Endurmat birgða</span><span class="sxs-lookup"><span data-stu-id="905a9-116">Revalue Inventory</span></span>](inventory-how-revalue-inventory.md)|
|<span data-ttu-id="905a9-117">Leiðrétta kostnað vöru, annaðhvort sjálfvirkt eða handvirkt til að áframsenda kostnaðarbreytingar úr færslum á innleið í tengdar færslur á útleið.</span><span class="sxs-lookup"><span data-stu-id="905a9-117">Adjust item costs, either automatically or manually, to forward cost changes from inbound entries to their related outbound entries.</span></span>|[<span data-ttu-id="905a9-118">Leiðr. kostnað vara</span><span class="sxs-lookup"><span data-stu-id="905a9-118">Adjust Item Costs</span></span>](inventory-how-adjust-item-costs.md)|
|<span data-ttu-id="905a9-119">Nota aðgerðir sérstaks kostnaðar fyrir hversdagslegar vörufærslur í vöruaðgerðum.</span><span class="sxs-lookup"><span data-stu-id="905a9-119">Use special costing functions for every-day item transactions in the item operations.</span></span>|[<span data-ttu-id="905a9-120">Meðhöndla birgða- og framleiðslukostnað</span><span class="sxs-lookup"><span data-stu-id="905a9-120">Handling Inventory and Manufacturing Costs</span></span>](finance-handle-inventory-and-manufacturing-costs.md)|  
|<span data-ttu-id="905a9-121">Reglulega verður að uppfæra staðlað kostnaðarverð íhluta, í samsetningu eða framleiðsluuppskrift, og leggja nýja kostnaðinn saman við yfirvöruna.</span><span class="sxs-lookup"><span data-stu-id="905a9-121">Periodically update the standard costs of components, in assembly or production BOMs, and roll the new costs up to the parent item.</span></span>|[<span data-ttu-id="905a9-122">Uppfæra staðlaðan kostnað</span><span class="sxs-lookup"><span data-stu-id="905a9-122">Update Standard Costs</span></span>](finance-how-to-update-standard-costs.md)|
|<span data-ttu-id="905a9-123">Stjórna framkvæmd í lok tímabils og búa til skýrslur um verk, t.d. að reikna út virði birgða og bóka kostnað í færslubók.</span><span class="sxs-lookup"><span data-stu-id="905a9-123">Perform period-end control and reporting tasks, such calculate the value of inventory and post costs to the general ledger.</span></span>|[<span data-ttu-id="905a9-124">Tilkynna kostnað og afstemma við fjárhag</span><span class="sxs-lookup"><span data-stu-id="905a9-124">Reporting Costs and Reconciling with the General Ledger</span></span>](finance-report-costs-and-reconcile-with-the-general-ledger.md)|  
|<span data-ttu-id="905a9-125">Læra um allt gangverk í kostnaðarkerfinu.</span><span class="sxs-lookup"><span data-stu-id="905a9-125">Learn about all mechanisms in the costing system.</span></span>|[<span data-ttu-id="905a9-126">Hönnunarupplýsingar: Birgðakostnaður</span><span class="sxs-lookup"><span data-stu-id="905a9-126">Design Details: Inventory Costing</span></span>](design-details-inventory-costing.md)|  

## <a name="see-also"></a><span data-ttu-id="905a9-127">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="905a9-127">See Also</span></span>  
 [<span data-ttu-id="905a9-128">Fjármál</span><span class="sxs-lookup"><span data-stu-id="905a9-128">Finance</span></span>](finance.md)  
 <span data-ttu-id="905a9-129">[Birgðir](inventory-manage-inventory.md) </span><span class="sxs-lookup"><span data-stu-id="905a9-129">[Inventory](inventory-manage-inventory.md) </span></span>  
 <span data-ttu-id="905a9-130">[Sala](sales-manage-sales.md) </span><span class="sxs-lookup"><span data-stu-id="905a9-130">[Sales](sales-manage-sales.md) </span></span>  
 [<span data-ttu-id="905a9-131">Innkaup</span><span class="sxs-lookup"><span data-stu-id="905a9-131">Purchasing</span></span>](purchasing-manage-purchasing.md)  
 <span data-ttu-id="905a9-132">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="905a9-132">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

