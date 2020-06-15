---
title: Hvernig á að loka á vörur í sölum eða innkaupum
description: Hægt er að koma í veg fyrir að vara sé notuð, t.d. í sölu- eða innkaupaskjölum.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 467b43b14f1905018c2a26a06c15abc5a0a17e99
ms.sourcegitcommit: 4545bb597dd9dc4c563b30af762977ee1d815497
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/29/2020
ms.locfileid: "3410645"
---
# <a name="block-items-from-sales-or-purchasing"></a><span data-ttu-id="aecfe-103">Loka á vörur í sölum eða innkaupum</span><span class="sxs-lookup"><span data-stu-id="aecfe-103">Block Items from Sales or Purchasing</span></span>
<span data-ttu-id="aecfe-104">Hægt er að loka á vöru svo hún verði ekki slegin inn í línur í innkaupa- eða söluskjölum og hægt er að loka á að hún verði bókuð í færslu.</span><span class="sxs-lookup"><span data-stu-id="aecfe-104">You can block an item from being entered on lines in sales or purchase documents, and you can block it from being posted in any transaction.</span></span> <span data-ttu-id="aecfe-105">Til dæmis er þetta gagnlegt þegar vara er með þekktan galla.</span><span class="sxs-lookup"><span data-stu-id="aecfe-105">For example, this is useful when an item has a known defect.</span></span> <span data-ttu-id="aecfe-106">Ef einhver velur lokaða vöru á sölu- eða innkaupaskjali birtast skilaboð um að varan sé læst.</span><span class="sxs-lookup"><span data-stu-id="aecfe-106">If someone chooses a blocked item on a sales or purchase document a message will inform them that the item is blocked.</span></span>

<span data-ttu-id="aecfe-107">Eftirfarandi tafla sýnir hvað gerist þegar vörum er lokað.</span><span class="sxs-lookup"><span data-stu-id="aecfe-107">The following table describes what occurs when items are blocked.</span></span>  

|<span data-ttu-id="aecfe-108">Valkostur</span><span class="sxs-lookup"><span data-stu-id="aecfe-108">Option</span></span>|<span data-ttu-id="aecfe-109">Description</span><span class="sxs-lookup"><span data-stu-id="aecfe-109">Description</span></span>|  
|--------------------|------------|  
|<span data-ttu-id="aecfe-110">**Lokað fyrir sölu**</span><span class="sxs-lookup"><span data-stu-id="aecfe-110">**Sales Blocked**</span></span>|<span data-ttu-id="aecfe-111">Ekki er hægt að slá vöruna inn í söluskjal eða færslubók söluvöru.</span><span class="sxs-lookup"><span data-stu-id="aecfe-111">You cannot enter the item in a sales document or in a sales item journal.</span></span>|  
|<span data-ttu-id="aecfe-112">**Lokað fyrir innkaup**</span><span class="sxs-lookup"><span data-stu-id="aecfe-112">**Purchasing Blocked**</span></span>|<span data-ttu-id="aecfe-113">Ekki er hægt að slá vöruna inn í innkaupaskjal eða færslubók innkaupavöru, eða í innkaupaáætlunarferli.</span><span class="sxs-lookup"><span data-stu-id="aecfe-113">You cannot enter the item in a purchase document, in a purchase item journal, or in purchase planning processes.</span></span>|  
|<span data-ttu-id="aecfe-114">**Lokað**</span><span class="sxs-lookup"><span data-stu-id="aecfe-114">**Blocked**</span></span>|<span data-ttu-id="aecfe-115">Ekki er hægt að nota vöruna fyrir vörufærslu.</span><span class="sxs-lookup"><span data-stu-id="aecfe-115">You cannot use the item for any item transaction.</span></span>|  

> [!NOTE]
> <span data-ttu-id="aecfe-116">Hægt er að skila útilokuðum vörum.</span><span class="sxs-lookup"><span data-stu-id="aecfe-116">Blocked items can be returned.</span></span> <span data-ttu-id="aecfe-117">Þetta þýðir að engar ofangreindra stillinga gilda þegar varan er notuð fyrir skilapantanir og kreditreikninga.</span><span class="sxs-lookup"><span data-stu-id="aecfe-117">This means that none of the above settings apply when the item is used on return orders and credit memos.</span></span>

<span data-ttu-id="aecfe-118">Þegar þú notar aðgerðina **Afrita úr fylgiskjali** til að búa til ný skjöl sem byggjast á fyrirliggjandi skjölum færðu tilkynningu ef einhver atriði í upprunaskjalslínum eru lokuð.</span><span class="sxs-lookup"><span data-stu-id="aecfe-118">When you use the **Copy from Document** function to create new documents based on existing documents, you are notified if any items on the source document lines are blocked.</span></span> <span data-ttu-id="aecfe-119">Útilokaðar fylgiskjalslínur eru ekki í nýja skjalinu og tilkynning sýnir yfirlit yfir allar fylgiskjalalínur sem eru útilokaðar í upprunaskjalinu.</span><span class="sxs-lookup"><span data-stu-id="aecfe-119">The blocked document lines are excluded from the new document, and a notification shows an overview of all document lines that are blocked in the source document.</span></span>

## <a name="to-block-an-item-from-being-entered-on-sales-lines"></a><span data-ttu-id="aecfe-120">Til að loka á vöru svo hún verði ekki slegin inn í sölulínur</span><span class="sxs-lookup"><span data-stu-id="aecfe-120">To block an item from being entered on sales lines</span></span>  
1.  <span data-ttu-id="aecfe-121">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Vara** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="aecfe-121">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="aecfe-122">Velja skal vöruna sem á að loka á og síðan velja gátreitinn **Sölur lokaðar**.</span><span class="sxs-lookup"><span data-stu-id="aecfe-122">Select the item that you want to block, and then select the **Sales Blocked** check box.</span></span>  

## <a name="to-block-an-item-from-being-entered-on-purchase-lines"></a><span data-ttu-id="aecfe-123">Til að loka á vöru svo hún verði ekki slegin inn í innkaupalínur</span><span class="sxs-lookup"><span data-stu-id="aecfe-123">To block an item from being entered on purchase lines</span></span>  
1.  <span data-ttu-id="aecfe-124">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Vara** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="aecfe-124">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="aecfe-125">Velja skal vöruna sem á að loka á og síðan velja gátreitinn **innkaup lokuð**.</span><span class="sxs-lookup"><span data-stu-id="aecfe-125">Select the item that you want to block, and then select the **Purchasing Blocked** check box.</span></span>  

## <a name="to-block-an-item-from-being-posted"></a><span data-ttu-id="aecfe-126">Til að loka á vöru svo hún verði ekki bókuð</span><span class="sxs-lookup"><span data-stu-id="aecfe-126">To block an item from being posted</span></span>
1. <span data-ttu-id="aecfe-127">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Vara** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="aecfe-127">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>
2. <span data-ttu-id="aecfe-128">Velja skal vöruna sem á að loka á og síðan velja gátreitinn **lokað**.</span><span class="sxs-lookup"><span data-stu-id="aecfe-128">Select the item that you want to block, and then select the **Blocked** check box.</span></span>

## <a name="see-also"></a><span data-ttu-id="aecfe-129">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="aecfe-129">See Also</span></span>  
[<span data-ttu-id="aecfe-130">Skrá nýjar vörur</span><span class="sxs-lookup"><span data-stu-id="aecfe-130">Register New Items</span></span>](inventory-how-register-new-items.md)  
[<span data-ttu-id="aecfe-131">Birgðir</span><span class="sxs-lookup"><span data-stu-id="aecfe-131">Inventory</span></span>](inventory-manage-inventory.md)  
