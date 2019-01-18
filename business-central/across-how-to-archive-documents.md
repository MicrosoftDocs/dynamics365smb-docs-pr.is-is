---
title: "Hvernig skal safnvista sölu- og innkaupaskjölum | Microsoft Docs"
description: "Þú getur safnvistað sölu- og innkaupapöntunum, tilboðum, skilapöntunum og standandi pöntunum og þú getur notað skráða skjalið til að endurskapa skjalið sem það var safnvistað frá."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: 4827e25d97127faf691b96df9868320bb47dee39
ms.contentlocale: is-is
ms.lasthandoff: 11/26/2018

---
# <a name="archive-documents"></a><span data-ttu-id="67365-103">Safnvista skjöl</span><span class="sxs-lookup"><span data-stu-id="67365-103">Archive Documents</span></span>
<span data-ttu-id="67365-104">Þú getur safnvistað sölu- og innkaupapöntunum, tilboðum, skilapöntunum og standandi pöntunum og þú getur notað skráða skjalið til að endurskapa skjalið sem það var safnvistað frá.</span><span class="sxs-lookup"><span data-stu-id="67365-104">You can archive sales and purchase orders, quotes, return orders, and blanket orders, and you can use the archived document to recreate the document that it was archived from.</span></span>

## <a name="to-set-up-automatic-document-archiving"></a><span data-ttu-id="67365-105">Setja upp sjálfvirka safnvistun</span><span class="sxs-lookup"><span data-stu-id="67365-105">To set up automatic document archiving</span></span>  
<span data-ttu-id="67365-106">Hægt er að setja upp sjálfvirka safnvistun á sölu- og innkaupapöntnum, tilboðum, standandi pöntunum og vöruskilapöntunum áður en skjölum er eytt.</span><span class="sxs-lookup"><span data-stu-id="67365-106">You can set up automatic archiving of sales and purchase orders, quotes, blanket orders, and return orders, before you delete documents.</span></span>

<span data-ttu-id="67365-107">Eftirfarandi ferli sýnir hvernig skal setja upp sjálfvirka safnvistun á söluskjölum.</span><span class="sxs-lookup"><span data-stu-id="67365-107">The following procedure describes how to set up automatic archiving of sales documents.</span></span> <span data-ttu-id="67365-108">Skrefin eru svipuð fyrir innkaupaskjöl.</span><span class="sxs-lookup"><span data-stu-id="67365-108">The steps are similar for purchase documents.</span></span>
1.  <span data-ttu-id="67365-109">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Uppsetning sölu & útistandandi** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="67365-109">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales & Receivables Setup**, and then choose the related link.</span></span>
2. <span data-ttu-id="67365-110">Á síðunni **Uppsetning sölu & útistandandi** er fyllt út í reitina á eftirfarandi hátt.</span><span class="sxs-lookup"><span data-stu-id="67365-110">On the **Sales & Receivables Setup** page, fill in the fields as follows.</span></span>

|<span data-ttu-id="67365-111">Svæði</span><span class="sxs-lookup"><span data-stu-id="67365-111">Field</span></span>|<span data-ttu-id="67365-112">Description</span><span class="sxs-lookup"><span data-stu-id="67365-112">Description</span></span>|
|-----|-----------|
|<span data-ttu-id="67365-113">**Safnvista sölutilboð**</span><span class="sxs-lookup"><span data-stu-id="67365-113">**Archiving Sales Quotes**</span></span>|<span data-ttu-id="67365-114">**Aldrei** til að aldrei safnvista sölutilboðum þegar þeim er eytt.</span><span class="sxs-lookup"><span data-stu-id="67365-114">**Never** to never archive sales quotes when they are deleted.</span></span> <span data-ttu-id="67365-115">**Spurning** til að biðja notandann um að velja hvort safnvista eigi sölutilboðum þegar þeim er eytt.</span><span class="sxs-lookup"><span data-stu-id="67365-115">**Question** to prompt the user to choose whether to archive sales quotes when they are deleted.</span></span> <span data-ttu-id="67365-116">**Alltaf** til að safnvista sölutilboðum sjálfkrafa þegar þeim er eytt.</span><span class="sxs-lookup"><span data-stu-id="67365-116">**Always** to archive sales quotes automatically when they are deleted.</span></span>|
|<span data-ttu-id="67365-117">**Safnvista standandi sölupöntunum**</span><span class="sxs-lookup"><span data-stu-id="67365-117">**Archiving Blanket Sales Orders**</span></span>|<span data-ttu-id="67365-118">Veldu að safnvista standandi sölupöntunum sjálfkrafa í hvert skipti sem þeim er eytt.</span><span class="sxs-lookup"><span data-stu-id="67365-118">Select to archive blanket sales orders automatically each time they are deleted.</span></span>|
|<span data-ttu-id="67365-119">**Safnvista pöntunum og vöruskilapöntunum**</span><span class="sxs-lookup"><span data-stu-id="67365-119">**Arch. Orders and Ret. Orders**</span></span>|<span data-ttu-id="67365-120">Veldu til að safnvista sölupöntunum sjálfkrafa í hvert skipti sem þeim eru eytt.</span><span class="sxs-lookup"><span data-stu-id="67365-120">Select to automatically archive sales orders each time they are deleted.</span></span>|

## <a name="to-archive-a-sales-order"></a><span data-ttu-id="67365-121">Til að safnvista sölupöntun</span><span class="sxs-lookup"><span data-stu-id="67365-121">To archive a sales order</span></span>
<span data-ttu-id="67365-122">Eftirfarandi ferli sýnir hvernig skal safnvista sölupöntun.</span><span class="sxs-lookup"><span data-stu-id="67365-122">The following procedure describes how to archive a sales order.</span></span> <span data-ttu-id="67365-123">Skrefin eru svipuð fyrir allar pantanir, standandi pantanir, vöruskilapantanir og tilboð.</span><span class="sxs-lookup"><span data-stu-id="67365-123">The steps are similar for all orders, blanket orders, return orders, and quotes.</span></span>

1.  <span data-ttu-id="67365-124">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Sölupantanir** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="67365-124">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Orders**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="67365-125">Opnuð er sölupöntun sem þú vilt kaupa safnvista.</span><span class="sxs-lookup"><span data-stu-id="67365-125">Open a sales order that you want to archive.</span></span>  
3.  <span data-ttu-id="67365-126">Valin er aðgerðin **Safnvista skjal**.</span><span class="sxs-lookup"><span data-stu-id="67365-126">Choose the **Archive Document** action.</span></span>

<span data-ttu-id="67365-127">Sölupöntunin er safnvistuð.</span><span class="sxs-lookup"><span data-stu-id="67365-127">The sales order is archived.</span></span> <span data-ttu-id="67365-128">Hægt er að skoða hana á síðunni **Safnvistaðar sölupantanir**.</span><span class="sxs-lookup"><span data-stu-id="67365-128">You can view it on the **Archived Sales orders** page.</span></span> <span data-ttu-id="67365-129">Héðan er einnig hægt að endurgera sölupöntunina frá staðnum sem hún var safnvistuð frá.</span><span class="sxs-lookup"><span data-stu-id="67365-129">From here, you can also use it to recreate the sales order that it was archived from.</span></span>

## <a name="to-recreate-a-sales-order-from-the-archive"></a><span data-ttu-id="67365-130">Endurgera sölupöntun frá skjalasafninu</span><span class="sxs-lookup"><span data-stu-id="67365-130">To recreate a sales order from the archive</span></span>
<span data-ttu-id="67365-131">Eftirfarandi ferli sýnir hvernig skal endurgera sölupöntun.</span><span class="sxs-lookup"><span data-stu-id="67365-131">The following procedure describes how to recreate a sales order.</span></span> <span data-ttu-id="67365-132">Skrefin eru svipuð fyrir allar pantanir, standandi pantanir, vöruskilapantanir og tilboð.</span><span class="sxs-lookup"><span data-stu-id="67365-132">The steps are similar for all orders, blanket orders, return orders, and quotes.</span></span>

1.  <span data-ttu-id="67365-133">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Safnvistaðar sölupantanir** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="67365-133">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Archived Sales Orders**, and then choose the related link.</span></span>
2.  <span data-ttu-id="67365-134">Valin er safnvistuð sölupöntun sem á að endurgera og velja síðan aðgerðina **Endurstilla**.</span><span class="sxs-lookup"><span data-stu-id="67365-134">Select the archived sales order that you want to recreate, and then choose the **Restore** action.</span></span>  

<span data-ttu-id="67365-135">Sölupöntunin er stofnuð og bætt við síðuna **Sölupantanir**.</span><span class="sxs-lookup"><span data-stu-id="67365-135">The sales order is created and added to the **Sales Orders** page.</span></span>

## <a name="to-delete-archived-sales-orders"></a><span data-ttu-id="67365-136">Eyða safnvistuðum sölupöntunum</span><span class="sxs-lookup"><span data-stu-id="67365-136">To delete archived sales orders</span></span>
<span data-ttu-id="67365-137">Eftirfarandi ferli sýnir hvernig skal eyða safnvistuðum sölupöntunum.</span><span class="sxs-lookup"><span data-stu-id="67365-137">The following procedure describes how to delete archived sales orders.</span></span> <span data-ttu-id="67365-138">Skrefin eru svipuð fyrir aðrar safnvistaðar sölur og innkaupaskjöl.</span><span class="sxs-lookup"><span data-stu-id="67365-138">The steps are similar for other archived sales and purchase documents.</span></span>

1.  <span data-ttu-id="67365-139">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Eyða safnvistaðar útgáfur sölupantana** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="67365-139">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Delete Archived Sales Order Versions**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="67365-140">Á síðunni **Eyða útgáfum sölupantana í skjalasafni** skal velja viðeigandi síur.</span><span class="sxs-lookup"><span data-stu-id="67365-140">On the **Delete Archived Sales Order Versions** page, select the appropriate filters.</span></span>  
3.  <span data-ttu-id="67365-141">Velja hnappinn **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="67365-141">Choose the **OK** button.</span></span>

## <a name="see-also"></a><span data-ttu-id="67365-142">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="67365-142">See Also</span></span>
[<span data-ttu-id="67365-143">Rekja skjalalínur</span><span class="sxs-lookup"><span data-stu-id="67365-143">Track Document Lines</span></span>](across-how-to-track-document-lines.md)  
[<span data-ttu-id="67365-144">Sala</span><span class="sxs-lookup"><span data-stu-id="67365-144">Sales</span></span>](sales-manage-sales.md)  
[<span data-ttu-id="67365-145">Almenn viðskiptavirkni</span><span class="sxs-lookup"><span data-stu-id="67365-145">General Business Functionality</span></span>](ui-across-business-areas.md)  
<span data-ttu-id="67365-146">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="67365-146">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

