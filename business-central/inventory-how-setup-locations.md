---
title: "Uppsetning staðsetningarspjalds og skilgreining flutningsleiða| Microsoft Docs"
description: "Þú býrð til staðsetningarspjald fyrir hvern stað sem birgðavara er geymd á, til dæmis vöruhús eða dreifingarmiðstöð, og setur upp leiðir til að flytja vörur á milli staða."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: warehouse, distribution center
ms.date: 10/01/2018
ms.author: SorenGP
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 503655e65b7df83c89e52d76a22396b672b2d28e
ms.contentlocale: is-is
ms.lasthandoff: 09/28/2018

---
# <a name="set-up-locations"></a><span data-ttu-id="e61b5-103">Uppsetning birgðageymsla</span><span class="sxs-lookup"><span data-stu-id="e61b5-103">Set Up Locations</span></span>
<span data-ttu-id="e61b5-104">Ef vörur eru keyptar, geymdar eða seldar á fleiri en einum stað eða vöruhúsi þarf að setja hverja staðsetningu upp með staðsetningarspjaldi og skilgreina flutningsleiðir.</span><span class="sxs-lookup"><span data-stu-id="e61b5-104">If you buy, store, or sell items at more than one place or warehouse, you must set each location up with a location card and define transfer routes.</span></span>

<span data-ttu-id="e61b5-105">Síðan er hægt að búa til skjalalínur fyrir tilgreinda staðsetningu, skoða tiltækileika eftir staðsetningu og flytja birgðir milli staða.</span><span class="sxs-lookup"><span data-stu-id="e61b5-105">You can then create document lines for a specific location, view availability by location, and transfer inventory between locations.</span></span> <span data-ttu-id="e61b5-106">Frekari upplýsingar eru í [Stjórna birgðum](inventory-manage-inventory.md).</span><span class="sxs-lookup"><span data-stu-id="e61b5-106">For more information, see [Manage Inventory](inventory-manage-inventory.md).</span></span>

## <a name="to-create-a-location-card"></a><span data-ttu-id="e61b5-107">Staðsetningarspjald búið til</span><span class="sxs-lookup"><span data-stu-id="e61b5-107">To create a location card</span></span>
1. <span data-ttu-id="e61b5-108">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Staðsetningar** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="e61b5-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Locations**, and then choose the related link.</span></span>
2. <span data-ttu-id="e61b5-109">Valið er **Nýtt** aðgerð.</span><span class="sxs-lookup"><span data-stu-id="e61b5-109">Choose the **New** action.</span></span>
3. <span data-ttu-id="e61b5-110">Í glugganum **Staðsetningarspjald** skal fylla út reitina eins og þörf krefur.</span><span class="sxs-lookup"><span data-stu-id="e61b5-110">In the **Location Card** window, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. <span data-ttu-id="e61b5-111">Endurtakið skref 2 og 3 fyrir hverja staðsetningu þar sem á að halda utan um birgðir.</span><span class="sxs-lookup"><span data-stu-id="e61b5-111">Repeat steps 2 and 3 for every location where you want to keep inventory.</span></span>

> [!NOTE]  
> <span data-ttu-id="e61b5-112">Margir reitir á birgðageymsluspjaldinu vísa til meðhöndlunar vara í vöruhúsaferli á inn- og útleið.</span><span class="sxs-lookup"><span data-stu-id="e61b5-112">Many fields on the location card refer to the handling of items in inbound and outbound warehouse processes.</span></span> <span data-ttu-id="e61b5-113">Nánari upplýsingar er að finna í [Uppsetning vöruhúsastjórnunar](warehouse-setup-warehouse.md).</span><span class="sxs-lookup"><span data-stu-id="e61b5-113">For more information, see [Setting Up Warehouse Management](warehouse-setup-warehouse.md).</span></span>

## <a name="to-create-a-transfer-route"></a><span data-ttu-id="e61b5-114">Flutningsleið búin til</span><span class="sxs-lookup"><span data-stu-id="e61b5-114">To create a transfer route</span></span>
1. <span data-ttu-id="e61b5-115">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **flutningsleið** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="e61b5-115">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Transfer Routes**, and then choose the related link.</span></span>
2. <span data-ttu-id="e61b5-116">Einnig, úr hvaða **Staðsetningarspjaldi** glugga sem er má velja **Flutningsleiðir**.</span><span class="sxs-lookup"><span data-stu-id="e61b5-116">Alternatively, from any **Location Card** window, choose the **Transfer Routes** action.</span></span>
3. <span data-ttu-id="e61b5-117">Valið er **Nýtt** aðgerð.</span><span class="sxs-lookup"><span data-stu-id="e61b5-117">Choose the **New** action.</span></span>
4. <span data-ttu-id="e61b5-118">Í glugganum **Staðsetningarspjald** skal fylla út reitina eins og þörf krefur.</span><span class="sxs-lookup"><span data-stu-id="e61b5-118">In the **Location Card** window, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

<span data-ttu-id="e61b5-119">Nú er hægt að flytja birgðavörur milli tveggja staða.</span><span class="sxs-lookup"><span data-stu-id="e61b5-119">You can now transfer inventory items between two locations.</span></span> <span data-ttu-id="e61b5-120">Nánari upplýsingar eru í [Flytja birgðir milli staða](inventory-how-transfer-between-locations.md).</span><span class="sxs-lookup"><span data-stu-id="e61b5-120">For more information, see [Transfer Inventory Between Locations](inventory-how-transfer-between-locations.md).</span></span>    

## <a name="see-also"></a><span data-ttu-id="e61b5-121">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="e61b5-121">See Also</span></span>
[<span data-ttu-id="e61b5-122">Stjórna birgðum</span><span class="sxs-lookup"><span data-stu-id="e61b5-122">Manage Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="e61b5-123">[Flytja birgðir milli birgðageymslna](inventory-how-transfer-between-locations.md)  </span><span class="sxs-lookup"><span data-stu-id="e61b5-123">[Transfer Inventory Between Locations](inventory-how-transfer-between-locations.md)  </span></span>  
<span data-ttu-id="e61b5-124">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="e61b5-124">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="e61b5-125">Breyting á hvaða eiginleikar eru sýndir</span><span class="sxs-lookup"><span data-stu-id="e61b5-125">Changing Which Features are Displayed</span></span>](ui-experiences.md)  
[<span data-ttu-id="e61b5-126">Almenn viðskiptavirkni</span><span class="sxs-lookup"><span data-stu-id="e61b5-126">General Business Functionality</span></span>](ui-across-business-areas.md)

