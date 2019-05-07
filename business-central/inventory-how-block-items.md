---
title: Hvernig á að loka á vörur í sölum eða innkaupum
description: Í Business Central getur vara verið merkt sem lokuð fyrir sölu, lokuð fyrir innkaupum eða lokuð fyrir allt.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: e13d59e939e71a252e08afc26d2fb1ec76b247c9
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2019
ms.locfileid: "917527"
---
# <a name="block-items-from-sales-or-purchasing"></a><span data-ttu-id="164b6-103">Loka á vörur í sölum eða innkaupum</span><span class="sxs-lookup"><span data-stu-id="164b6-103">Block Items from Sales or Purchasing</span></span>
<span data-ttu-id="164b6-104">Hægt er að loka fyrir vöru svo hún verði ekki slegin inn í sölu- eða innkaupalínur og hægt er að loka á að hún verði bókuð í færslu.</span><span class="sxs-lookup"><span data-stu-id="164b6-104">You can block an item from being entered on sales or purchase lines, and you can block it from being posted in any transaction.</span></span>  

<span data-ttu-id="164b6-105">Eftirfarandi tafla sýnir hvað gerist þegar vörum er lokað.</span><span class="sxs-lookup"><span data-stu-id="164b6-105">The following table illustrates what occurs when items are blocked.</span></span>  

|<span data-ttu-id="164b6-106">Valkostur</span><span class="sxs-lookup"><span data-stu-id="164b6-106">Option</span></span>|<span data-ttu-id="164b6-107">Description</span><span class="sxs-lookup"><span data-stu-id="164b6-107">Description</span></span>|  
|--------------------|------------|  
|<span data-ttu-id="164b6-108">**Lokað fyrir sölu**</span><span class="sxs-lookup"><span data-stu-id="164b6-108">**Sales Blocked**</span></span>|<span data-ttu-id="164b6-109">Ekki er hægt að slá vöruna inn í söluskjal eða færslubók söluvöru.</span><span class="sxs-lookup"><span data-stu-id="164b6-109">You cannot enter the item in a sales document or in a sales item journal.</span></span>|  
|<span data-ttu-id="164b6-110">**Lokað fyrir innkaup**</span><span class="sxs-lookup"><span data-stu-id="164b6-110">**Purchasing Blocked**</span></span>|<span data-ttu-id="164b6-111">Ekki er hægt að slá vöruna inn í innkaupaskjal eða færslubók innkaupavöru, eða í innkaupaáætlunarferli.</span><span class="sxs-lookup"><span data-stu-id="164b6-111">You cannot enter the item in a purchase document, in a purchase item journal, or in purchase planning processes.</span></span>|  
|<span data-ttu-id="164b6-112">**Lokað**</span><span class="sxs-lookup"><span data-stu-id="164b6-112">**Blocked**</span></span>|<span data-ttu-id="164b6-113">Ekki er hægt að nota vöruna fyrir vörufærslu.</span><span class="sxs-lookup"><span data-stu-id="164b6-113">You cannot use the item for any item transaction.</span></span> <span data-ttu-id="164b6-114">Nánari upplýsingar um lokun á vöru í hvaða tilgangi sem er má sjá í vöruspjaldi.</span><span class="sxs-lookup"><span data-stu-id="164b6-114">For more information about blocking an item for all purposes, see Item Card.</span></span>|  

## <a name="to-block-an-item-from-being-entered-on-sales-lines"></a><span data-ttu-id="164b6-115">Til að loka á vöru svo hún verði ekki slegin inn í sölulínur</span><span class="sxs-lookup"><span data-stu-id="164b6-115">To block an item from being entered on sales lines</span></span>  

1.  <span data-ttu-id="164b6-116">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Vörur** og veldu síðan tengda hlekkinn.</span><span class="sxs-lookup"><span data-stu-id="164b6-116">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="164b6-117">Velja skal vöruna sem á að loka á og síðan velja gátreitinn **Sölur lokaðar**.</span><span class="sxs-lookup"><span data-stu-id="164b6-117">Select the item that you want to block, and then select the **Sales Blocked** check box.</span></span>  

<span data-ttu-id="164b6-118">Nú munu villuboð koma upp sem segja að lokað sé fyrir vöruna ef reynt er að slá hana inn í söluskjal eða færslubókarlínu.</span><span class="sxs-lookup"><span data-stu-id="164b6-118">If you try to enter the item on a sales document or journal line, you will now get an error message that the item is blocked.</span></span>

## <a name="to-block-an-item-from-being-entered-on-purchase-lines"></a><span data-ttu-id="164b6-119">Til að loka á vöru svo hún verði ekki slegin inn í innkaupalínur</span><span class="sxs-lookup"><span data-stu-id="164b6-119">To block an item from being entered on purchase lines</span></span>  

1.  <span data-ttu-id="164b6-120">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Vörur** og veldu síðan tengda hlekkinn.</span><span class="sxs-lookup"><span data-stu-id="164b6-120">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="164b6-121">Velja skal vöruna sem á að loka á og síðan velja gátreitinn **innkaup lokuð**.</span><span class="sxs-lookup"><span data-stu-id="164b6-121">Select the item that you want to block, and then select the **Purchasing Blocked** check box.</span></span>  

<span data-ttu-id="164b6-122">Nú munu villuboð koma upp sem segja að lokað sé fyrir vöruna ef reynt er að slá hana inn í innkaupaskjal eða færslubókarlínu.</span><span class="sxs-lookup"><span data-stu-id="164b6-122">If you try to enter the item on a purchase document or journal line, you will now get an error message that the item is blocked.</span></span>

## <a name="to-block-an-item-from-being-posted"></a><span data-ttu-id="164b6-123">Til að loka á vöru svo hún verði ekki bókuð</span><span class="sxs-lookup"><span data-stu-id="164b6-123">To block an item from being posted</span></span>
1. <span data-ttu-id="164b6-124">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Vörur** og veldu síðan tengda hlekkinn.</span><span class="sxs-lookup"><span data-stu-id="164b6-124">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>
2. <span data-ttu-id="164b6-125">Velja skal vöruna sem á að loka á og síðan velja gátreitinn **lokað**.</span><span class="sxs-lookup"><span data-stu-id="164b6-125">Select the item that you want to block, and then select the **Blocked** check box.</span></span>

<span data-ttu-id="164b6-126">Nú munu villuboð koma upp sem segja að lokað sé fyrir vöruna ef reynt er að bóka einhverja færslu fyrir hana.</span><span class="sxs-lookup"><span data-stu-id="164b6-126">If you try to post any type of transaction for the item, you will now get an error message that the item is blocked.</span></span>

## <a name="see-also"></a><span data-ttu-id="164b6-127">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="164b6-127">See Also</span></span>  
[<span data-ttu-id="164b6-128">Skrá nýjar vörur</span><span class="sxs-lookup"><span data-stu-id="164b6-128">Register New Items</span></span>](inventory-how-register-new-items.md)  
[<span data-ttu-id="164b6-129">Birgðir</span><span class="sxs-lookup"><span data-stu-id="164b6-129">Inventory</span></span>](inventory-manage-inventory.md)  
