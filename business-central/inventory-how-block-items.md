---
title: Hvernig á að loka á vörur í sölum eða innkaupum
description: Í Business Central getur vara verið merkt sem lokuð fyrir sölu, lokuð fyrir innkaupum eða lokuð fyrir allt.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: c453a10f30d2a45f6d4641bda8b24ee3659b1a32
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2020
ms.locfileid: "3182301"
---
# <a name="block-items-from-sales-or-purchasing"></a><span data-ttu-id="2bbd6-103">Loka á vörur í sölum eða innkaupum</span><span class="sxs-lookup"><span data-stu-id="2bbd6-103">Block Items from Sales or Purchasing</span></span>
<span data-ttu-id="2bbd6-104">Hægt er að loka fyrir vöru svo hún verði ekki slegin inn í sölu- eða innkaupalínur og hægt er að loka á að hún verði bókuð í færslu.</span><span class="sxs-lookup"><span data-stu-id="2bbd6-104">You can block an item from being entered on sales or purchase lines, and you can block it from being posted in any transaction.</span></span>  

<span data-ttu-id="2bbd6-105">Eftirfarandi tafla sýnir hvað gerist þegar vörum er lokað.</span><span class="sxs-lookup"><span data-stu-id="2bbd6-105">The following table illustrates what occurs when items are blocked.</span></span>  

|<span data-ttu-id="2bbd6-106">Valkostur</span><span class="sxs-lookup"><span data-stu-id="2bbd6-106">Option</span></span>|<span data-ttu-id="2bbd6-107">Description</span><span class="sxs-lookup"><span data-stu-id="2bbd6-107">Description</span></span>|  
|--------------------|------------|  
|<span data-ttu-id="2bbd6-108">**Lokað fyrir sölu**</span><span class="sxs-lookup"><span data-stu-id="2bbd6-108">**Sales Blocked**</span></span>|<span data-ttu-id="2bbd6-109">Ekki er hægt að slá vöruna inn í söluskjal eða færslubók söluvöru.</span><span class="sxs-lookup"><span data-stu-id="2bbd6-109">You cannot enter the item in a sales document or in a sales item journal.</span></span>|  
|<span data-ttu-id="2bbd6-110">**Lokað fyrir innkaup**</span><span class="sxs-lookup"><span data-stu-id="2bbd6-110">**Purchasing Blocked**</span></span>|<span data-ttu-id="2bbd6-111">Ekki er hægt að slá vöruna inn í innkaupaskjal eða færslubók innkaupavöru, eða í innkaupaáætlunarferli.</span><span class="sxs-lookup"><span data-stu-id="2bbd6-111">You cannot enter the item in a purchase document, in a purchase item journal, or in purchase planning processes.</span></span>|  
|<span data-ttu-id="2bbd6-112">**Lokað**</span><span class="sxs-lookup"><span data-stu-id="2bbd6-112">**Blocked**</span></span>|<span data-ttu-id="2bbd6-113">Ekki er hægt að nota vöruna fyrir vörufærslu.</span><span class="sxs-lookup"><span data-stu-id="2bbd6-113">You cannot use the item for any item transaction.</span></span>|  

> [!NOTE]
> <span data-ttu-id="2bbd6-114">Hægt er að skila útilokuðum vörum.</span><span class="sxs-lookup"><span data-stu-id="2bbd6-114">Blocked items can be returned.</span></span> <span data-ttu-id="2bbd6-115">Þetta þýðir að engar ofangreindra stillinga gilda þegar varan er notuð fyrir skilapantanir og kreditreikninga.</span><span class="sxs-lookup"><span data-stu-id="2bbd6-115">This means that none of the above settings apply when the item is used on return orders and credit memos.</span></span>

<span data-ttu-id="2bbd6-116">Þegar þú notar aðgerðina **Afrita úr fylgiskjali** til að búa til ný skjöl sem byggjast á fyrirliggjandi skjölum færðu tilkynningu ef einhver atriði í upprunaskjalslínum eru lokuð.</span><span class="sxs-lookup"><span data-stu-id="2bbd6-116">When you use the **Copy from Document** function to create new documents based on existing documents, you are notified if any items on the source document lines are blocked.</span></span> <span data-ttu-id="2bbd6-117">Útilokaðar fylgiskjalslínur eru ekki í nýja skjalinu og tilkynning sýnir yfirlit yfir allar fylgiskjalalínur sem eru útilokaðar í upprunaskjalinu.</span><span class="sxs-lookup"><span data-stu-id="2bbd6-117">The blocked document lines are excluded from the new document, and a notification shows an overview of all document lines that are blocked in the source document.</span></span>

## <a name="to-block-an-item-from-being-entered-on-sales-lines"></a><span data-ttu-id="2bbd6-118">Til að loka á vöru svo hún verði ekki slegin inn í sölulínur</span><span class="sxs-lookup"><span data-stu-id="2bbd6-118">To block an item from being entered on sales lines</span></span>  

1.  <span data-ttu-id="2bbd6-119">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Vara** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="2bbd6-119">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="2bbd6-120">Velja skal vöruna sem á að loka á og síðan velja gátreitinn **Sölur lokaðar**.</span><span class="sxs-lookup"><span data-stu-id="2bbd6-120">Select the item that you want to block, and then select the **Sales Blocked** check box.</span></span>  

<span data-ttu-id="2bbd6-121">Nú munu villuboð koma upp sem segja að lokað sé fyrir vöruna ef reynt er að slá hana inn í söluskjal eða færslubókarlínu.</span><span class="sxs-lookup"><span data-stu-id="2bbd6-121">If you try to enter the item on a sales document or journal line, you will now get an error message that the item is blocked.</span></span>

## <a name="to-block-an-item-from-being-entered-on-purchase-lines"></a><span data-ttu-id="2bbd6-122">Til að loka á vöru svo hún verði ekki slegin inn í innkaupalínur</span><span class="sxs-lookup"><span data-stu-id="2bbd6-122">To block an item from being entered on purchase lines</span></span>  

1.  <span data-ttu-id="2bbd6-123">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Vara** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="2bbd6-123">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="2bbd6-124">Velja skal vöruna sem á að loka á og síðan velja gátreitinn **innkaup lokuð**.</span><span class="sxs-lookup"><span data-stu-id="2bbd6-124">Select the item that you want to block, and then select the **Purchasing Blocked** check box.</span></span>  

<span data-ttu-id="2bbd6-125">Nú munu villuboð koma upp sem segja að lokað sé fyrir vöruna ef reynt er að slá hana inn í innkaupaskjal eða færslubókarlínu.</span><span class="sxs-lookup"><span data-stu-id="2bbd6-125">If you try to enter the item on a purchase document or journal line, you will now get an error message that the item is blocked.</span></span>

## <a name="to-block-an-item-from-being-posted"></a><span data-ttu-id="2bbd6-126">Til að loka á vöru svo hún verði ekki bókuð</span><span class="sxs-lookup"><span data-stu-id="2bbd6-126">To block an item from being posted</span></span>
1. <span data-ttu-id="2bbd6-127">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Vara** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="2bbd6-127">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>
2. <span data-ttu-id="2bbd6-128">Velja skal vöruna sem á að loka á og síðan velja gátreitinn **lokað**.</span><span class="sxs-lookup"><span data-stu-id="2bbd6-128">Select the item that you want to block, and then select the **Blocked** check box.</span></span>

<span data-ttu-id="2bbd6-129">Nú munu villuboð koma upp sem segja að lokað sé fyrir vöruna ef reynt er að bóka einhverja færslu fyrir hana.</span><span class="sxs-lookup"><span data-stu-id="2bbd6-129">If you try to post any type of transaction for the item, you will now get an error message that the item is blocked.</span></span>

## <a name="see-also"></a><span data-ttu-id="2bbd6-130">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="2bbd6-130">See Also</span></span>  
[<span data-ttu-id="2bbd6-131">Skrá nýjar vörur</span><span class="sxs-lookup"><span data-stu-id="2bbd6-131">Register New Items</span></span>](inventory-how-register-new-items.md)  
[<span data-ttu-id="2bbd6-132">Birgðir</span><span class="sxs-lookup"><span data-stu-id="2bbd6-132">Inventory</span></span>](inventory-manage-inventory.md)  
