---
title: Uppsetning birgða | Microsoft Docs
description: Lýsir því hvernig á að setja upp birgðavinnslur, þar á meðal flutningsleiðir og birgðageymslur á borð við vöruhús.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: warehouse, stock
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: f5b4e07f128551e978dffb2dedeb3e0257eea1ea
ms.sourcegitcommit: 32bfc2acaaf3693afc9aeb86feea505fd328caa1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/19/2021
ms.locfileid: "5024563"
---
# <a name="setting-up-inventory"></a><span data-ttu-id="c5c93-103">Uppsetning birgða</span><span class="sxs-lookup"><span data-stu-id="c5c93-103">Setting Up Inventory</span></span>
<span data-ttu-id="c5c93-104">Áður en hægt er að hefjast handa við að stýra vöruhúsaaðgerðum og birgðakostnaði þarf að grunnstilla reglur og gildi sem ráða birgðareglum fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="c5c93-104">Before you can manage warehouse activities and inventory costing, you must configure the rules and values that define the company's inventory policies.</span></span>

<span data-ttu-id="c5c93-105">Hægt er að veita betri þjónustu við viðskiptavini og fínstilla aðfangakeðjuna með því að skipulegga birgðirnar á mismunandi stöðum.</span><span class="sxs-lookup"><span data-stu-id="c5c93-105">You can provide better customer service and optimize your supply chain by organizing your inventory at different addresses.</span></span> <span data-ttu-id="c5c93-106">Síðan er hægt að kaupa, geyma eða selja vörur í mismunandi birgðageymslum og flytja birgðir milli þeirra.</span><span class="sxs-lookup"><span data-stu-id="c5c93-106">You can then buy, store, or sell items at different locations and transfer inventory between them.</span></span>

<span data-ttu-id="c5c93-107">Þegar birgðir hafa verið settar upp er hægt að stjórna ýmsum birgðaferlum.</span><span class="sxs-lookup"><span data-stu-id="c5c93-107">When you have set up your inventory, you can manage various processes related to item transactions.</span></span> <span data-ttu-id="c5c93-108">Frekari upplýsingar eru í [Stjórna birgðum](inventory-manage-inventory.md) og [Vöruhúsastjórnun](warehouse-manage-warehouse.md).</span><span class="sxs-lookup"><span data-stu-id="c5c93-108">For more information, see [Manage Inventory](inventory-manage-inventory.md) and [Warehouse Management](warehouse-manage-warehouse.md).</span></span>

| <span data-ttu-id="c5c93-109">Til</span><span class="sxs-lookup"><span data-stu-id="c5c93-109">To</span></span> | <span data-ttu-id="c5c93-110">Sjá</span><span class="sxs-lookup"><span data-stu-id="c5c93-110">See</span></span> |
| --- | --- |
| <span data-ttu-id="c5c93-111">Skilgreina almennar birgðaupplýsingar svo sem númeraraðir og hvernig á að nota birgðageymslur.</span><span class="sxs-lookup"><span data-stu-id="c5c93-111">Define the general inventory setup, such as number series and how to use locations.</span></span> |[<span data-ttu-id="c5c93-112">Setja upp almennar birgðaupplýsingar</span><span class="sxs-lookup"><span data-stu-id="c5c93-112">Set Up General Inventory Information</span></span>](inventory-how-setup-general.md) |
|<span data-ttu-id="c5c93-113">Grunnstilla skilvirkt dreifingarlíkan með mismunandi birgðageymslur og ábyrgðarstöðvum sem hefur verið úthlutað til viðskiptafélaga eða starfsmanna.</span><span class="sxs-lookup"><span data-stu-id="c5c93-113">Configure an efficient distribution model with a combination of different locations and responsibility centers assigned to business partners or employees.</span></span>|[<span data-ttu-id="c5c93-114">Vinna með ábyrgðarstöðvar</span><span class="sxs-lookup"><span data-stu-id="c5c93-114">Work with Responsibility Centers</span></span>](inventory-responsibility-centers.md)|
| <span data-ttu-id="c5c93-115">Skipuleggja birgðir í mörgum birgðageymslum, þar með talið flutningsleiðir.</span><span class="sxs-lookup"><span data-stu-id="c5c93-115">Organize your inventory at multiple locations, including transfer routes.</span></span> |[<span data-ttu-id="c5c93-116">Uppsetning birgðageymsla</span><span class="sxs-lookup"><span data-stu-id="c5c93-116">Set Up Locations</span></span>](inventory-how-register-new-items.md) |
| <span data-ttu-id="c5c93-117">Stofna birgðaspjöld fyrir birgðavörur, vörur sem ekki eru birgðir eða þjónustuvörur sem boðið er upp á.</span><span class="sxs-lookup"><span data-stu-id="c5c93-117">Create item cards for inventory, non-inventory, or service items that you trade in.</span></span> |[<span data-ttu-id="c5c93-118">Skrá nýjar vörur</span><span class="sxs-lookup"><span data-stu-id="c5c93-118">Register New Items</span></span>](inventory-how-register-new-items.md) |
|<span data-ttu-id="c5c93-119">Notaðu virknina **Afrita vöru** til að búa til nýtt birgðaspjald með fljótlegum hætti sem byggt er á fyrirliggjandi birgðaspjaldi.</span><span class="sxs-lookup"><span data-stu-id="c5c93-119">Use the **Copy Item** function to quickly create a new item card based on an existing one.</span></span>|[<span data-ttu-id="c5c93-120">Afrita fyrirliggjandi vörur í Búa til nýjar vörur</span><span class="sxs-lookup"><span data-stu-id="c5c93-120">Copy Existing Items to Create New Items</span></span>](inventory-how-copy-items.md)|
|<span data-ttu-id="c5c93-121">Lærðu hvernig á að fylla inn **Tegund** reitinn á birgðaspjöldum í samræmi við viðskiptatilgang.</span><span class="sxs-lookup"><span data-stu-id="c5c93-121">Learn how to fill in the **Type** field on item cards according to the business purpose.</span></span>|[<span data-ttu-id="c5c93-122">Um vörutegundir</span><span class="sxs-lookup"><span data-stu-id="c5c93-122">About Item Types</span></span>](inventory-about-item-types.md)|
|<span data-ttu-id="c5c93-123">Setja upp margar mælieiningar fyrir vöru sem hægt er að nota sem mælieiningu til vara, til dæmis í sölu, við innkaup eða framleiðslufærslu.</span><span class="sxs-lookup"><span data-stu-id="c5c93-123">Set up multiple units of measure for an item that you can use as alternate UOMs, for example on sales, purchasing, or production transactions.</span></span>|[<span data-ttu-id="c5c93-124">Setja upp mælieiningu vara</span><span class="sxs-lookup"><span data-stu-id="c5c93-124">Set Up Item Units of Measure</span></span>](inventory-how-setup-units-of-measure.md)|
|<span data-ttu-id="c5c93-125">Sem viðbót við birgðaspjöld, skrá upplýsingar um vörur fyrir tiltekna birgðageymslu eða tiltekinn afbrigði.</span><span class="sxs-lookup"><span data-stu-id="c5c93-125">As a supplement to item cards, record information about your items in a specific location or of a specific variant.</span></span>|[<span data-ttu-id="c5c93-126">Setja upp birgðahaldseiningar</span><span class="sxs-lookup"><span data-stu-id="c5c93-126">Set Up Stockkeeping Units</span></span>](inventory-how-to-set-up-stockkeeping-units.md)|
| <span data-ttu-id="c5c93-127">Úthlutaðu vörur í flokka og gefðu þeim eiginleika til að hjálpa þér og viðskiptavinum að finna vörur.</span><span class="sxs-lookup"><span data-stu-id="c5c93-127">Assign items to categories and give them attributes to help you and customers find items.</span></span> |[<span data-ttu-id="c5c93-128">Flokka vörur</span><span class="sxs-lookup"><span data-stu-id="c5c93-128">Categorize Items</span></span>](inventory-how-categorize-items.md) |
|<span data-ttu-id="c5c93-129">Flytja inn margar myndir úr einni zip-skrá þar sem skrár hafa heiti í samræmi við vörunúmer.</span><span class="sxs-lookup"><span data-stu-id="c5c93-129">Import multiple item pictures in one go from a zip file where the files are named according to item numbers.</span></span>|[<span data-ttu-id="c5c93-130">Flytja inn margar vörumyndir</span><span class="sxs-lookup"><span data-stu-id="c5c93-130">Import Multiple Item Pictures</span></span>](inventory-how-import-item-pictures.md)|
|<span data-ttu-id="c5c93-131">Tilgreina sjálfgefnar skýrslur sem á að nota fyrir mismunandi skjalagerðir.</span><span class="sxs-lookup"><span data-stu-id="c5c93-131">Specify default reports to be used for different document types.</span></span>|[<span data-ttu-id="c5c93-132">Skýrsluval í Business Central</span><span class="sxs-lookup"><span data-stu-id="c5c93-132">Report Selection in Business Central</span></span>](across-report-selections.md)|

## <a name="see-related-training-at-microsoft-learn"></a><span data-ttu-id="c5c93-133">Sjá tengda þjálfun á [Microsoft Learn](/learn/paths/trade-get-started-dynamics-365-business-central/)</span><span class="sxs-lookup"><span data-stu-id="c5c93-133">See Related Training at [Microsoft Learn](/learn/paths/trade-get-started-dynamics-365-business-central/)</span></span>

## <a name="see-also"></a><span data-ttu-id="c5c93-134">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="c5c93-134">See Also</span></span>

[<span data-ttu-id="c5c93-135">Stjórnun birgða</span><span class="sxs-lookup"><span data-stu-id="c5c93-135">Managing Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="c5c93-136">Stjórnun innkaupa</span><span class="sxs-lookup"><span data-stu-id="c5c93-136">Managing Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="c5c93-137">[Stjórna sölu](sales-manage-sales.md)  </span><span class="sxs-lookup"><span data-stu-id="c5c93-137">[Managing Sales](sales-manage-sales.md)  </span></span>  
<span data-ttu-id="c5c93-138">[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="c5c93-138">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="c5c93-139">Almenn viðskiptavirkni</span><span class="sxs-lookup"><span data-stu-id="c5c93-139">General Business Functionality</span></span>](ui-across-business-areas.md)
