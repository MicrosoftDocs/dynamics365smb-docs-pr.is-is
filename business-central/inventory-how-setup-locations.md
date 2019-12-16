---
title: Uppsetning staðsetningarspjalds og skilgreining flutningsleiða| Microsoft Docs
description: Þú býrð til staðsetningarspjald fyrir hvern stað sem birgðavara er geymd á, til dæmis vöruhús eða dreifingarmiðstöð, og setur upp leiðir til að flytja vörur á milli staða.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: warehouse, distribution center
ms.date: 10/01/2019
ms.author: SorenGP
ms.openlocfilehash: 5554bb1576705cd1f3cbcddc7ef33da7b5db3796
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/03/2019
ms.locfileid: "2878316"
---
# <a name="set-up-locations"></a><span data-ttu-id="5fd37-103">Uppsetning birgðageymsla</span><span class="sxs-lookup"><span data-stu-id="5fd37-103">Set Up Locations</span></span>
<span data-ttu-id="5fd37-104">Ef vörur eru keyptar, geymdar eða seldar á fleiri en einum stað eða vöruhúsi þarf að setja hverja staðsetningu upp með staðsetningarspjaldi og skilgreina flutningsleiðir.</span><span class="sxs-lookup"><span data-stu-id="5fd37-104">If you buy, store, or sell items at more than one place or warehouse, you must set each location up with a location card and define transfer routes.</span></span>

<span data-ttu-id="5fd37-105">Síðan er hægt að búa til skjalalínur fyrir tilgreinda staðsetningu, skoða tiltækileika eftir staðsetningu og flytja birgðir milli staða.</span><span class="sxs-lookup"><span data-stu-id="5fd37-105">You can then create document lines for a specific location, view availability by location, and transfer inventory between locations.</span></span> <span data-ttu-id="5fd37-106">Frekari upplýsingar eru í [Stjórna birgðum](inventory-manage-inventory.md).</span><span class="sxs-lookup"><span data-stu-id="5fd37-106">For more information, see [Manage Inventory](inventory-manage-inventory.md).</span></span>
<br><br>  
  
> [!Video https://www.microsoft.com/videoplayer/embed/RE4aQvq]

## <a name="to-create-a-location-card"></a><span data-ttu-id="5fd37-107">Staðsetningarspjald búið til</span><span class="sxs-lookup"><span data-stu-id="5fd37-107">To create a location card</span></span>
1. <span data-ttu-id="5fd37-108">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Staðsetningar** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="5fd37-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Locations**, and then choose the related link.</span></span>
2. <span data-ttu-id="5fd37-109">Valið er **Nýtt** aðgerð.</span><span class="sxs-lookup"><span data-stu-id="5fd37-109">Choose the **New** action.</span></span>
3. <span data-ttu-id="5fd37-110">Á síðunni **Staðsetningarspjald** skal fylla út reitina eins og þörf krefur.</span><span class="sxs-lookup"><span data-stu-id="5fd37-110">On the **Location Card** page, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. <span data-ttu-id="5fd37-111">Endurtakið skref 2 og 3 fyrir hverja staðsetningu þar sem á að halda utan um birgðir.</span><span class="sxs-lookup"><span data-stu-id="5fd37-111">Repeat steps 2 and 3 for every location where you want to keep inventory.</span></span>

> [!NOTE]  
> <span data-ttu-id="5fd37-112">Margir reitir á birgðageymsluspjaldinu vísa til meðhöndlunar vara í vöruhúsaferli á inn- og útleið.</span><span class="sxs-lookup"><span data-stu-id="5fd37-112">Many fields on the location card refer to the handling of items in inbound and outbound warehouse processes.</span></span> <span data-ttu-id="5fd37-113">Nánari upplýsingar er að finna í [Uppsetning vöruhúsastjórnunar](warehouse-setup-warehouse.md).</span><span class="sxs-lookup"><span data-stu-id="5fd37-113">For more information, see [Setting Up Warehouse Management](warehouse-setup-warehouse.md).</span></span>

## <a name="to-create-a-transfer-route"></a><span data-ttu-id="5fd37-114">Flutningsleið búin til</span><span class="sxs-lookup"><span data-stu-id="5fd37-114">To create a transfer route</span></span>
1. <span data-ttu-id="5fd37-115">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Flutningsleiðir** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="5fd37-115">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Transfer Routes**, and then choose the related link.</span></span>
2. <span data-ttu-id="5fd37-116">Að öðrum kosti, frá hvaða síðu **Staðsetningarspjalds** sem er má velja aðgerðina **Flutningsleiðir**.</span><span class="sxs-lookup"><span data-stu-id="5fd37-116">Alternatively, from any **Location Card** page, choose the **Transfer Routes** action.</span></span>
3. <span data-ttu-id="5fd37-117">Valið er **Nýtt** aðgerð.</span><span class="sxs-lookup"><span data-stu-id="5fd37-117">Choose the **New** action.</span></span>
4. <span data-ttu-id="5fd37-118">Á síðunni **Staðsetningarspjald** skal fylla út reitina eins og þörf krefur.</span><span class="sxs-lookup"><span data-stu-id="5fd37-118">On the **Location Card** page, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

<span data-ttu-id="5fd37-119">Nú er hægt að flytja birgðavörur milli tveggja staða.</span><span class="sxs-lookup"><span data-stu-id="5fd37-119">You can now transfer inventory items between two locations.</span></span> <span data-ttu-id="5fd37-120">Nánari upplýsingar eru í [Flytja birgðir milli staða](inventory-how-transfer-between-locations.md).</span><span class="sxs-lookup"><span data-stu-id="5fd37-120">For more information, see [Transfer Inventory Between Locations](inventory-how-transfer-between-locations.md).</span></span>    

## <a name="see-also"></a><span data-ttu-id="5fd37-121">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="5fd37-121">See Also</span></span>
[<span data-ttu-id="5fd37-122">Stjórna birgðum</span><span class="sxs-lookup"><span data-stu-id="5fd37-122">Manage Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="5fd37-123">[Flytja birgðir milli birgðageymslna](inventory-how-transfer-between-locations.md)  </span><span class="sxs-lookup"><span data-stu-id="5fd37-123">[Transfer Inventory Between Locations](inventory-how-transfer-between-locations.md)  </span></span>  
<span data-ttu-id="5fd37-124">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="5fd37-124">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="5fd37-125">Breyta því hvaða eiginleikar eru sýndir</span><span class="sxs-lookup"><span data-stu-id="5fd37-125">Change Which Features are Displayed</span></span>](ui-experiences.md)  
[<span data-ttu-id="5fd37-126">Almenn viðskiptavirkni</span><span class="sxs-lookup"><span data-stu-id="5fd37-126">General Business Functionality</span></span>](ui-across-business-areas.md)
