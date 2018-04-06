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
ms.date: 12/21/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 74460bfcff36d293006229f4a89719f8c05c2631
ms.contentlocale: is-is
ms.lasthandoff: 03/22/2018

---
# <a name="archive-documents"></a><span data-ttu-id="fa4ca-103">Safnvista skjöl</span><span class="sxs-lookup"><span data-stu-id="fa4ca-103">Archive Documents</span></span>
<span data-ttu-id="fa4ca-104">Þú getur safnvistað sölu- og innkaupapöntunum, tilboðum, skilapöntunum og standandi pöntunum og þú getur notað skráða skjalið til að endurskapa skjalið sem það var safnvistað frá.</span><span class="sxs-lookup"><span data-stu-id="fa4ca-104">You can archive sales and purchase orders, quotes, return orders, and blanket orders, and you can use the archived document to recreate the document that it was archived from.</span></span>

## <a name="to-set-up-automatic-document-archiving"></a><span data-ttu-id="fa4ca-105">Setja upp sjálfvirka safnvistun</span><span class="sxs-lookup"><span data-stu-id="fa4ca-105">To set up automatic document archiving</span></span>  
<span data-ttu-id="fa4ca-106">Hægt er að setja upp sjálfvirka safnvistun á sölu- og innkaupapöntnum, tilboðum, standandi pöntunum og vöruskilapöntunum áður en skjölum er eytt.</span><span class="sxs-lookup"><span data-stu-id="fa4ca-106">You can set up automatic archiving of sales and purchase orders, quotes, blanket orders, and return orders, before you delete documents.</span></span>

<span data-ttu-id="fa4ca-107">Eftirfarandi ferli sýnir hvernig skal setja upp sjálfvirka safnvistun á söluskjölum.</span><span class="sxs-lookup"><span data-stu-id="fa4ca-107">The following procedure describes how to set up automatic archiving of sales documents.</span></span> <span data-ttu-id="fa4ca-108">Skrefin eru svipuð fyrir innkaupaskjöl.</span><span class="sxs-lookup"><span data-stu-id="fa4ca-108">The steps are similar for purchase documents.</span></span>
1.  <span data-ttu-id="fa4ca-109">Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Uppsetning Sala & útistandandi** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="fa4ca-109">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Sales & Receivables Setup**, and then choose the related link.</span></span>
2. <span data-ttu-id="fa4ca-110">Í glugganum **Uppsetning sölu & útistandandi** er fyllt út í reitina á eftirfarandi hátt.</span><span class="sxs-lookup"><span data-stu-id="fa4ca-110">In the **Sales & Receivables Setup** window, fill in the fields as follows.</span></span>

|<span data-ttu-id="fa4ca-111">Svæði</span><span class="sxs-lookup"><span data-stu-id="fa4ca-111">Field</span></span>|<span data-ttu-id="fa4ca-112">Description</span><span class="sxs-lookup"><span data-stu-id="fa4ca-112">Description</span></span>|
|-----|-----------|
|<span data-ttu-id="fa4ca-113">**Safnvista sölutilboð**</span><span class="sxs-lookup"><span data-stu-id="fa4ca-113">**Archiving Sales Quotes**</span></span>|<span data-ttu-id="fa4ca-114">**Aldrei** til að aldrei safnvista sölutilboðum þegar þeim er eytt.</span><span class="sxs-lookup"><span data-stu-id="fa4ca-114">**Never** to never archive sales quotes when they are deleted.</span></span> <span data-ttu-id="fa4ca-115">**Spurning** til að biðja notandann um að velja hvort safnvista eigi sölutilboðum þegar þeim er eytt.</span><span class="sxs-lookup"><span data-stu-id="fa4ca-115">**Question** to prompt the user to choose whether to archive sales quotes when they are deleted.</span></span> <span data-ttu-id="fa4ca-116">**Alltaf** til að safnvista sölutilboðum sjálfkrafa þegar þeim er eytt.</span><span class="sxs-lookup"><span data-stu-id="fa4ca-116">**Always** to archive sales quotes automatically when they are deleted.</span></span>|
|<span data-ttu-id="fa4ca-117">**Safnvista standandi sölupöntunum**</span><span class="sxs-lookup"><span data-stu-id="fa4ca-117">**Archiving Blanket Sales Orders**</span></span>|<span data-ttu-id="fa4ca-118">Veldu að safnvista standandi sölupöntunum sjálfkrafa í hvert skipti sem þeim er eytt.</span><span class="sxs-lookup"><span data-stu-id="fa4ca-118">Select to archive blanket sales orders automatically each time they are deleted.</span></span>|
|<span data-ttu-id="fa4ca-119">**Safnvista pöntunum og vöruskilapöntunum**</span><span class="sxs-lookup"><span data-stu-id="fa4ca-119">**Arch. Orders and Ret. Orders**</span></span>|<span data-ttu-id="fa4ca-120">Veldu til að safnvista sölupöntunum sjálfkrafa í hvert skipti sem þeim eru eytt.</span><span class="sxs-lookup"><span data-stu-id="fa4ca-120">Select to automatically archive sales orders each time they are deleted.</span></span>|

## <a name="to-archive-a-sales-order"></a><span data-ttu-id="fa4ca-121">Til að safnvista sölupöntun</span><span class="sxs-lookup"><span data-stu-id="fa4ca-121">To archive a sales order</span></span>
<span data-ttu-id="fa4ca-122">Eftirfarandi ferli sýnir hvernig skal safnvista sölupöntun.</span><span class="sxs-lookup"><span data-stu-id="fa4ca-122">The following procedure describes how to archive a sales order.</span></span> <span data-ttu-id="fa4ca-123">Skrefin eru svipuð fyrir allar pantanir, standandi pantanir, vöruskilapantanir og tilboð.</span><span class="sxs-lookup"><span data-stu-id="fa4ca-123">The steps are similar for all orders, blanket orders, return orders, and quotes.</span></span>

1.  <span data-ttu-id="fa4ca-124">Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn  **Sölupantanir** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="fa4ca-124">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Sales Orders**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="fa4ca-125">Opnuð er sölupöntun sem þú vilt kaupa safnvista.</span><span class="sxs-lookup"><span data-stu-id="fa4ca-125">Open a sales order that you want to archive.</span></span>  
3.  <span data-ttu-id="fa4ca-126">Valin er aðgerðin **Safnvista skjal**.</span><span class="sxs-lookup"><span data-stu-id="fa4ca-126">Choose the **Archive Document** action.</span></span>

<span data-ttu-id="fa4ca-127">Sölupöntunin er safnvistuð.</span><span class="sxs-lookup"><span data-stu-id="fa4ca-127">The sales order is archived.</span></span> <span data-ttu-id="fa4ca-128">Hægt er að skoða hana í glugganum **Safnvistaðar sölupantanir**.</span><span class="sxs-lookup"><span data-stu-id="fa4ca-128">You can view it in the **Archived Sales orders** window.</span></span> <span data-ttu-id="fa4ca-129">Héðan er einnig hægt að endurgera sölupöntunina frá staðnum sem hún var safnvistuð frá.</span><span class="sxs-lookup"><span data-stu-id="fa4ca-129">From here, you can also use it to recreate the sales order that it was archived from.</span></span>

## <a name="to-recreate-a-sales-order-from-the-archive"></a><span data-ttu-id="fa4ca-130">Endurgera sölupöntun frá skjalasafninu</span><span class="sxs-lookup"><span data-stu-id="fa4ca-130">To recreate a sales order from the archive</span></span>
<span data-ttu-id="fa4ca-131">Eftirfarandi ferli sýnir hvernig skal endurgera sölupöntun.</span><span class="sxs-lookup"><span data-stu-id="fa4ca-131">The following procedure describes how to recreate a sales order.</span></span> <span data-ttu-id="fa4ca-132">Skrefin eru svipuð fyrir allar pantanir, standandi pantanir, vöruskilapantanir og tilboð.</span><span class="sxs-lookup"><span data-stu-id="fa4ca-132">The steps are similar for all orders, blanket orders, return orders, and quotes.</span></span>

1.  <span data-ttu-id="fa4ca-133">Velja skal táknið ![Leita að síðu eða skýrslu](media/ui-search/search_small.png "Leita að síðu eða skýrslutákni"), slá inn **Safnvistaðar sölupantanir** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="fa4ca-133">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Archived Sales Orders**, and then choose the related link.</span></span>
2.  <span data-ttu-id="fa4ca-134">Valin er safnvistuð sölupöntun sem á að endurgera og velja síðan aðgerðina **Endurstilla**.</span><span class="sxs-lookup"><span data-stu-id="fa4ca-134">Select the archived sales order that you want to recreate, and then choose the **Restore** action.</span></span>  

<span data-ttu-id="fa4ca-135">Sölupöntunin er stofnuð og bætt við gluggann **Sölupantanir**.</span><span class="sxs-lookup"><span data-stu-id="fa4ca-135">The sales order is created and added to the **Sales Orders** window.</span></span>

## <a name="to-delete-archived-sales-orders"></a><span data-ttu-id="fa4ca-136">Eyða safnvistuðum sölupöntunum</span><span class="sxs-lookup"><span data-stu-id="fa4ca-136">To delete archived sales orders</span></span>
<span data-ttu-id="fa4ca-137">Eftirfarandi ferli sýnir hvernig skal eyða safnvistuðum sölupöntunum.</span><span class="sxs-lookup"><span data-stu-id="fa4ca-137">The following procedure describes how to delete archived sales orders.</span></span> <span data-ttu-id="fa4ca-138">Skrefin eru svipuð fyrir aðrar safnvistaðar sölur og innkaupaskjöl.</span><span class="sxs-lookup"><span data-stu-id="fa4ca-138">The steps are similar for other archived sales and purchase documents.</span></span>

1.  <span data-ttu-id="fa4ca-139">Velja skal táknið ![Leita að síðu eða skýrslu](media/ui-search/search_small.png "Leita að síðu eða skýrslutákni"), fara í **Eyða útgáfum sölupantana í skjalasafni** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="fa4ca-139">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Delete Archived Sales Order Versions**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="fa4ca-140">Í glugganum **Eyða útgáfum sölupantana í skjalasafni** skal velja viðeigandi síur.</span><span class="sxs-lookup"><span data-stu-id="fa4ca-140">In the **Delete Archived Sales Order Versions** window, select the appropriate filters.</span></span>  
3.  <span data-ttu-id="fa4ca-141">Velja hnappinn **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="fa4ca-141">Choose the **OK** button.</span></span>

## <a name="see-also"></a><span data-ttu-id="fa4ca-142">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="fa4ca-142">See Also</span></span>
[<span data-ttu-id="fa4ca-143">Rekja skjalalínur</span><span class="sxs-lookup"><span data-stu-id="fa4ca-143">Track Document Lines</span></span>](across-how-to-track-document-lines.md)  
[<span data-ttu-id="fa4ca-144">Sala</span><span class="sxs-lookup"><span data-stu-id="fa4ca-144">Sales</span></span>](sales-manage-sales.md)  
[<span data-ttu-id="fa4ca-145">Almenn viðskiptavirkni</span><span class="sxs-lookup"><span data-stu-id="fa4ca-145">General Business Functionality</span></span>](ui-across-business-areas.md)  
<span data-ttu-id="fa4ca-146">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="fa4ca-146">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

