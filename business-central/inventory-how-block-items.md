---
title: "Hvernig á að loka á vörur í sölum eða innkaupum"
description: "Í Business Central getur vara verið merkt sem lokuð fyrir sölu, lokuð fyrir innkaupum eða lokuð fyrir allt."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/23/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: c6f10f8252c00bf0a599f9fa794ee36c41ce92be
ms.openlocfilehash: 2f8be478dda62fef2cb34397de488f45d4fcfc0c
ms.contentlocale: is-is
ms.lasthandoff: 07/31/2018

---
# <a name="block-items-from-sales-or-purchasing"></a><span data-ttu-id="95ab9-103">Loka á vörur í sölum eða innkaupum</span><span class="sxs-lookup"><span data-stu-id="95ab9-103">Block Items from Sales or Purchasing</span></span>
<span data-ttu-id="95ab9-104">Hægt er að loka fyrir vöru svo hún verði ekki slegin inn í sölu- eða innkaupalínur og hægt er að loka á að hún verði bókuð í færslu.</span><span class="sxs-lookup"><span data-stu-id="95ab9-104">You can block an item from being entered on sales or purchase lines, and you can block it from being posted in any transaction.</span></span>  

<span data-ttu-id="95ab9-105">Eftirfarandi tafla sýnir hvað gerist þegar vörum er lokað.</span><span class="sxs-lookup"><span data-stu-id="95ab9-105">The following table illustrates what occurs when items are blocked.</span></span>  

|<span data-ttu-id="95ab9-106">Valkostur</span><span class="sxs-lookup"><span data-stu-id="95ab9-106">Option</span></span>|<span data-ttu-id="95ab9-107">Description</span><span class="sxs-lookup"><span data-stu-id="95ab9-107">Description</span></span>|  
|--------------------|------------|  
|<span data-ttu-id="95ab9-108">**Lokað fyrir sölu**</span><span class="sxs-lookup"><span data-stu-id="95ab9-108">**Sales Blocked**</span></span>|<span data-ttu-id="95ab9-109">Ekki er hægt að slá vöruna inn í söluskjal eða færslubók söluvöru.</span><span class="sxs-lookup"><span data-stu-id="95ab9-109">You cannot enter the item in a sales document or in a sales item journal.</span></span>|  
|<span data-ttu-id="95ab9-110">**Lokað fyrir innkaup**</span><span class="sxs-lookup"><span data-stu-id="95ab9-110">**Purchasing Blocked**</span></span>|<span data-ttu-id="95ab9-111">Ekki er hægt að slá vöruna inn í innkaupaskjal eða færslubók innkaupavöru, eða í innkaupaáætlunarferli.</span><span class="sxs-lookup"><span data-stu-id="95ab9-111">You cannot enter the item in a purchase document, in a purchase item journal, or in purchase planning processes.</span></span>|  
|<span data-ttu-id="95ab9-112">**Lokað**</span><span class="sxs-lookup"><span data-stu-id="95ab9-112">**Blocked**</span></span>|<span data-ttu-id="95ab9-113">Ekki er hægt að nota vöruna fyrir vörufærslu.</span><span class="sxs-lookup"><span data-stu-id="95ab9-113">You cannot use the item for any item transaction.</span></span> <span data-ttu-id="95ab9-114">Nánari upplýsingar um lokun á vöru í hvaða tilgangi sem er má sjá í vöruspjaldi.</span><span class="sxs-lookup"><span data-stu-id="95ab9-114">For more information about blocking an item for all purposes, see Item Card.</span></span>|  

## <a name="to-block-an-item-from-being-entered-on-sales-lines"></a><span data-ttu-id="95ab9-115">Til að loka á vöru svo hún verði ekki slegin inn í sölulínur</span><span class="sxs-lookup"><span data-stu-id="95ab9-115">To block an item from being entered on sales lines</span></span>  

1.  <span data-ttu-id="95ab9-116">Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Vörur** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="95ab9-116">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Items**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="95ab9-117">Velja skal vöruna sem á að loka á og síðan velja gátreitinn **Sölur lokaðar**.</span><span class="sxs-lookup"><span data-stu-id="95ab9-117">Select the item that you want to block, and then select the **Sales Blocked** check box.</span></span>  

<span data-ttu-id="95ab9-118">Nú munu villuboð koma upp sem segja að lokað sé fyrir vöruna ef reynt er að slá hana inn í söluskjal eða færslubókarlínu.</span><span class="sxs-lookup"><span data-stu-id="95ab9-118">If you try to enter the item on a sales document or journal line, you will now get an error message that the item is blocked.</span></span>

## <a name="to-block-an-item-from-being-entered-on-purchase-lines"></a><span data-ttu-id="95ab9-119">Til að loka á vöru svo hún verði ekki slegin inn í innkaupalínur</span><span class="sxs-lookup"><span data-stu-id="95ab9-119">To block an item from being entered on purchase lines</span></span>  

1.  <span data-ttu-id="95ab9-120">Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Vörur** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="95ab9-120">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Items**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="95ab9-121">Velja skal vöruna sem á að loka á og síðan velja gátreitinn **innkaup lokuð**.</span><span class="sxs-lookup"><span data-stu-id="95ab9-121">Select the item that you want to block, and then select the **Purchasing Blocked** check box.</span></span>  

<span data-ttu-id="95ab9-122">Nú munu villuboð koma upp sem segja að lokað sé fyrir vöruna ef reynt er að slá hana inn í innkaupaskjal eða færslubókarlínu.</span><span class="sxs-lookup"><span data-stu-id="95ab9-122">If you try to enter the item on a purchase document or journal line, you will now get an error message that the item is blocked.</span></span>

## <a name="to-block-an-item-from-being-posted"></a><span data-ttu-id="95ab9-123">Til að loka á vöru svo hún verði ekki bókuð</span><span class="sxs-lookup"><span data-stu-id="95ab9-123">To block an item from being posted</span></span>
1. <span data-ttu-id="95ab9-124">Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Vörur** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="95ab9-124">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Items**, and then choose the related link.</span></span>
2. <span data-ttu-id="95ab9-125">Velja skal vöruna sem á að loka á og síðan velja gátreitinn **lokað**.</span><span class="sxs-lookup"><span data-stu-id="95ab9-125">Select the item that you want to block, and then select the **Blocked** check box.</span></span>

<span data-ttu-id="95ab9-126">Nú munu villuboð koma upp sem segja að lokað sé fyrir vöruna ef reynt er að bóka einhverja færslu fyrir hana.</span><span class="sxs-lookup"><span data-stu-id="95ab9-126">If you try to post any type of transaction for the item, you will now get an error message that the item is blocked.</span></span>

## <a name="see-also"></a><span data-ttu-id="95ab9-127">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="95ab9-127">See Also</span></span>  
[<span data-ttu-id="95ab9-128">Skrá nýjar vörur</span><span class="sxs-lookup"><span data-stu-id="95ab9-128">Register New Items</span></span>](inventory-how-register-new-items.md)  
[<span data-ttu-id="95ab9-129">Birgðir</span><span class="sxs-lookup"><span data-stu-id="95ab9-129">Inventory</span></span>](inventory-manage-inventory.md)  

