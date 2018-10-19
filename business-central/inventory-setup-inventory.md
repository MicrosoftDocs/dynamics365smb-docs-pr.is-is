---
title: "Uppsetning birgða | Microsoft Docs"
description: "Lýsir því hvernig á að setja upp birgðavinnslur, þar á meðal flutningsleiðir og birgðageymslur á borð við vöruhús."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: warehouse, stock
ms.date: 10/01/2018
ms.author: SorenGP
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 8e4033412560e8dc847397c4399e12985490bf78
ms.contentlocale: is-is
ms.lasthandoff: 09/28/2018

---
# <a name="setting-up-inventory"></a><span data-ttu-id="901e9-103">Uppsetning birgða</span><span class="sxs-lookup"><span data-stu-id="901e9-103">Setting Up Inventory</span></span>
<span data-ttu-id="901e9-104">Áður en hægt er að hefjast handa við að stýra vöruhúsaaðgerðum og birgðakostnaði þarf að grunnstilla reglur og gildi sem ráða birgðareglum fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="901e9-104">Before you can manage warehouse activities and inventory costing, you must configure the rules and values that define the company's inventory policies.</span></span>

<span data-ttu-id="901e9-105">Hægt er að veita betri þjónustu við viðskiptavini og fínstilla aðfangakeðjuna með því að skipulegga birgðirnar á mismunandi stöðum.</span><span class="sxs-lookup"><span data-stu-id="901e9-105">You can provide better customer service and optimize your supply chain by organizing your inventory at different addresses.</span></span> <span data-ttu-id="901e9-106">Síðan er hægt að kaupa, geyma eða selja vörur í mismunandi birgðageymslum og flytja birgðir milli þeirra.</span><span class="sxs-lookup"><span data-stu-id="901e9-106">You can then buy, store, or sell items at different locations and transfer inventory between them.</span></span>

<span data-ttu-id="901e9-107">Þegar birgðir hafa verið settar upp er hægt að stjórna ýmsum birgðaferlum.</span><span class="sxs-lookup"><span data-stu-id="901e9-107">When you have set up your inventory, you can manage various processes related to item transactions.</span></span> <span data-ttu-id="901e9-108">Frekari upplýsingar eru í [Stjórna birgðum](inventory-manage-inventory.md) og [Vöruhúsastjórnun](warehouse-manage-warehouse.md).</span><span class="sxs-lookup"><span data-stu-id="901e9-108">For more information, see [Manage Inventory](inventory-manage-inventory.md) and [Warehouse Management](warehouse-manage-warehouse.md).</span></span>

| <span data-ttu-id="901e9-109">Til</span><span class="sxs-lookup"><span data-stu-id="901e9-109">To</span></span> | <span data-ttu-id="901e9-110">Sjá</span><span class="sxs-lookup"><span data-stu-id="901e9-110">See</span></span> |
| --- | --- |
| <span data-ttu-id="901e9-111">Skilgreina almennar birgðaupplýsingar svo sem númeraraðir og hvernig á að nota birgðageymslur.</span><span class="sxs-lookup"><span data-stu-id="901e9-111">Define the general inventory setup, such as number series and how to use locations.</span></span> |[<span data-ttu-id="901e9-112">Setja upp almennar birgðaupplýsingar</span><span class="sxs-lookup"><span data-stu-id="901e9-112">Set Up General Inventory Information</span></span>](inventory-how-setup-general.md) |
|<span data-ttu-id="901e9-113">Grunnstilla skilvirkt dreifingarlíkan með mismunandi birgðageymslur og ábyrgðarstöðvum sem hefur verið úthlutað til viðskiptafélaga eða starfsmanna.</span><span class="sxs-lookup"><span data-stu-id="901e9-113">Configure an efficient distribution model with a combination of different locations and responsibility centers assigned to business partners or employees.</span></span>|[<span data-ttu-id="901e9-114">Vinna með ábyrgðarstöðvar</span><span class="sxs-lookup"><span data-stu-id="901e9-114">Work with Responsibility Centers</span></span>](inventory-responsibility-centers.md)|
| <span data-ttu-id="901e9-115">Skipuleggja birgðir í mörgum birgðageymslum, þar með talið flutningsleiðir.</span><span class="sxs-lookup"><span data-stu-id="901e9-115">Organize your inventory at multiple locations, including transfer routes.</span></span> |[<span data-ttu-id="901e9-116">Uppsetning birgðageymsla</span><span class="sxs-lookup"><span data-stu-id="901e9-116">Set Up Locations</span></span>](inventory-how-register-new-items.md) |
| <span data-ttu-id="901e9-117">Stofna birgðaspjöld fyrir birgðavörur, vörur sem ekki eru birgðir eða þjónustuvörur sem boðið er upp á.</span><span class="sxs-lookup"><span data-stu-id="901e9-117">Create item cards for inventory, non-inventory, or service items that you trade in.</span></span> |[<span data-ttu-id="901e9-118">Skrá nýjar vörur</span><span class="sxs-lookup"><span data-stu-id="901e9-118">Register New Items</span></span>](inventory-how-register-new-items.md) |
|<span data-ttu-id="901e9-119">Lærðu hvernig á að fylla inn **Tegund** reitinn á birgðaspjöldum í samræmi við viðskiptatilgang.</span><span class="sxs-lookup"><span data-stu-id="901e9-119">Learn how to fill in the **Type** field on item cards according to the business purpose.</span></span>|[<span data-ttu-id="901e9-120">Um vörutegundir</span><span class="sxs-lookup"><span data-stu-id="901e9-120">About Item Types</span></span>](inventory-about-item-types.md)| 
|<span data-ttu-id="901e9-121">Setja upp margar mælieiningar fyrir vöru sem hægt er að nota sem mælieiningu til vara, til dæmis í sölu, við innkaup eða framleiðslufærslu.</span><span class="sxs-lookup"><span data-stu-id="901e9-121">Set up multiple units of measure for an item that you can use as alternate UOMs, for example on sales, purchasing, or production transactions.</span></span>|[<span data-ttu-id="901e9-122">Setja upp mælieiningu vara</span><span class="sxs-lookup"><span data-stu-id="901e9-122">Set Up Item Units of Measure</span></span>](inventory-how-setup-units-of-measure.md)|
|<span data-ttu-id="901e9-123">Sem viðbót við birgðaspjöld, skrá upplýsingar um vörur fyrir tiltekna birgðageymslu eða tiltekinn afbrigði.</span><span class="sxs-lookup"><span data-stu-id="901e9-123">As a supplement to item cards, record information about your items in a specific location or of a specific variant.</span></span>|[<span data-ttu-id="901e9-124">Setja upp birgðahaldseiningar</span><span class="sxs-lookup"><span data-stu-id="901e9-124">Set Up Stockkeeping Units</span></span>](inventory-how-to-set-up-stockkeeping-units.md)|
| <span data-ttu-id="901e9-125">Úthlutaðu vörur í flokka og gefðu þeim eiginleika til að hjálpa þér og viðskiptavinum að finna vörur.</span><span class="sxs-lookup"><span data-stu-id="901e9-125">Assign items to categories and give them attributes to help you and customers find items.</span></span> |[<span data-ttu-id="901e9-126">Flokka vörur</span><span class="sxs-lookup"><span data-stu-id="901e9-126">Categorize Items</span></span>](inventory-how-categorize-items.md) |

## <a name="see-also"></a><span data-ttu-id="901e9-127">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="901e9-127">See Also</span></span>
[<span data-ttu-id="901e9-128">Stjórnun birgða</span><span class="sxs-lookup"><span data-stu-id="901e9-128">Managing Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="901e9-129">Stjórnun innkaupa</span><span class="sxs-lookup"><span data-stu-id="901e9-129">Managing Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="901e9-130">[Stjórna sölu](sales-manage-sales.md)  </span><span class="sxs-lookup"><span data-stu-id="901e9-130">[Managing Sales](sales-manage-sales.md)  </span></span>  
<span data-ttu-id="901e9-131">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="901e9-131">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="901e9-132">Almenn viðskiptavirkni</span><span class="sxs-lookup"><span data-stu-id="901e9-132">General Business Functionality</span></span>](ui-across-business-areas.md)

