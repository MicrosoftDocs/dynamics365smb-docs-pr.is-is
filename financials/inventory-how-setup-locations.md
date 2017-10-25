---
title: "Uppsetning staðsetningarspjalds og skilgreining flutningsleiða| Microsoft Docs"
description: "Þú býrð til staðsetningarspjald fyrir hvern stað sem birgðavara er geymd á, til dæmis vöruhús eða dreifingarmiðstöð, og setur upp leiðir til að flytja vörur á milli staða."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: warehouse, distribution center
ms.date: 06/02/2017
ms.author: SorenGP
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 7d82b1c63bb1da367736f8dd044640b583493af8
ms.contentlocale: is-is
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-set-up-locations"></a><span data-ttu-id="cf6ca-103">Hvernig á að setja upp birgðageymslur</span><span class="sxs-lookup"><span data-stu-id="cf6ca-103">How to: Set Up Locations</span></span>
<span data-ttu-id="cf6ca-104">Ef vörur eru keyptar, geymdar eða seldar á fleiri en einum stað eða vöruhúsi þarf að setja hverja staðsetningu upp með staðsetningarspjaldi og skilgreina flutningsleiðir.</span><span class="sxs-lookup"><span data-stu-id="cf6ca-104">If you buy, store, or sell items at more than one place or warehouse, you must set each location up with a location card and define transfer routes.</span></span>

<span data-ttu-id="cf6ca-105">Síðan er hægt að búa til skjalalínur fyrir tilgreinda staðsetningu, skoða tiltækileika eftir staðsetningu og flytja birgðir milli staða.</span><span class="sxs-lookup"><span data-stu-id="cf6ca-105">You can then create document lines for a specific location, view availability by location, and transfer inventory between locations.</span></span> <span data-ttu-id="cf6ca-106">Frekari upplýsingar eru í [Stjórna birgðum](inventory-manage-inventory.md).</span><span class="sxs-lookup"><span data-stu-id="cf6ca-106">For more information, see [Manage Inventory](inventory-manage-inventory.md).</span></span>

> [!NOTE]  
>   <span data-ttu-id="cf6ca-107">Þessi virkni krefst þess að upplifun þín sé stillt á **Suite**.</span><span class="sxs-lookup"><span data-stu-id="cf6ca-107">This functionality requires that your experience is set to **Suite**.</span></span> <span data-ttu-id="cf6ca-108">Nánari upplýsingar, sjá [Sérstilla þína [!INCLUDE[d365fin](includes/d365fin_md.md)] upplifun](ui-experiences.md).</span><span class="sxs-lookup"><span data-stu-id="cf6ca-108">For more information, see [Customizing Your [!INCLUDE[d365fin](includes/d365fin_md.md)] Experience](ui-experiences.md).</span></span>

## <a name="to-create-a-location-card"></a><span data-ttu-id="cf6ca-109">Staðsetningarspjald búið til</span><span class="sxs-lookup"><span data-stu-id="cf6ca-109">To create a location card</span></span>
1. <span data-ttu-id="cf6ca-110">Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn  **Staðsetningar** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="cf6ca-110">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Locations**, and then choose the related link.</span></span>
2. <span data-ttu-id="cf6ca-111">Valið er **Nýtt** aðgerð.</span><span class="sxs-lookup"><span data-stu-id="cf6ca-111">Choose the **New** action.</span></span>
3. <span data-ttu-id="cf6ca-112">Í glugganum **Staðsetningarspjald** skal fylla út reitina eins og þörf krefur.</span><span class="sxs-lookup"><span data-stu-id="cf6ca-112">In the **Location Card** window, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. <span data-ttu-id="cf6ca-113">Endurtakið skref 2 og 3 fyrir hverja staðsetningu þar sem á að halda utan um birgðir.</span><span class="sxs-lookup"><span data-stu-id="cf6ca-113">Repeat steps 2 and 3 for every location where you want to keep inventory.</span></span>

> [!NOTE]  
> <span data-ttu-id="cf6ca-114">Margir reitir á birgðageymsluspjaldinu vísa til meðhöndlunar vara í vöruhúsaferli á inn- og útleið.</span><span class="sxs-lookup"><span data-stu-id="cf6ca-114">Many fields on the location card refer to the handling of items in inbound and outbound warehouse processes.</span></span> <span data-ttu-id="cf6ca-115">Nánari upplýsingar er að finna í [Uppsetning vöruhúsastjórnunar](warehouse-setup-warehouse.md).</span><span class="sxs-lookup"><span data-stu-id="cf6ca-115">For more information, see [Setting Up Warehouse Management](warehouse-setup-warehouse.md).</span></span> 

## <a name="to-create-a-transfer-route"></a><span data-ttu-id="cf6ca-116">Flutningsleið búin til</span><span class="sxs-lookup"><span data-stu-id="cf6ca-116">To create a transfer route</span></span>
1. <span data-ttu-id="cf6ca-117">Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn  **Flutningsleiðir** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="cf6ca-117">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Transfer Routes**, and then choose the related link.</span></span>
2. <span data-ttu-id="cf6ca-118">Einnig, úr hvaða **Staðsetningarspjaldi** glugga sem er má velja **Flutningsleiðir**.</span><span class="sxs-lookup"><span data-stu-id="cf6ca-118">Alternatively, from any **Location Card** window, choose the **Transfer Routes** action.</span></span>
3. <span data-ttu-id="cf6ca-119">Valið er **Nýtt** aðgerð.</span><span class="sxs-lookup"><span data-stu-id="cf6ca-119">Choose the **New** action.</span></span>
4. <span data-ttu-id="cf6ca-120">Í glugganum **Staðsetningarspjald** skal fylla út reitina eins og þörf krefur.</span><span class="sxs-lookup"><span data-stu-id="cf6ca-120">In the **Location Card** window, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

<span data-ttu-id="cf6ca-121">Nú er hægt að flytja birgðavörur milli tveggja staða.</span><span class="sxs-lookup"><span data-stu-id="cf6ca-121">You can now transfer inventory items between two locations.</span></span> <span data-ttu-id="cf6ca-122">Nánari upplýsingar eru í [Hvernig á að: Flytja birgðir milli staða](inventory-how-transfer-between-locations.md).</span><span class="sxs-lookup"><span data-stu-id="cf6ca-122">For more information, see [How to: Transfer Inventory Between Locations](inventory-how-transfer-between-locations.md).</span></span>    

## <a name="see-also"></a><span data-ttu-id="cf6ca-123">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="cf6ca-123">See Also</span></span>
[<span data-ttu-id="cf6ca-124">Stjórna birgðum</span><span class="sxs-lookup"><span data-stu-id="cf6ca-124">Manage Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="cf6ca-125">[Hvernig á að: Flytja birgðir milli birgðageymslna](inventory-how-transfer-between-locations.md)  </span><span class="sxs-lookup"><span data-stu-id="cf6ca-125">[How to: Transfer Inventory Between Locations](inventory-how-transfer-between-locations.md)  </span></span>  
<span data-ttu-id="cf6ca-126">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="cf6ca-126">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
<span data-ttu-id="cf6ca-127">[Sérstillir þína [!INCLUDE[d365fin](includes/d365fin_md.md)] upplifun](ui-experiences.md).</span><span class="sxs-lookup"><span data-stu-id="cf6ca-127">[Customizing Your [!INCLUDE[d365fin](includes/d365fin_md.md)] Experience](ui-experiences.md)</span></span>  
[<span data-ttu-id="cf6ca-128">Almenn viðskiptavirkni</span><span class="sxs-lookup"><span data-stu-id="cf6ca-128">General Business Functionality</span></span>](ui-across-business-areas.md)

