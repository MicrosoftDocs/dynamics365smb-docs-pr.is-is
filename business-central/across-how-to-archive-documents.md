---
title: Hvernig skal safnvista sölu- og innkaupaskjölum | Microsoft Docs
description: Þú getur safnvistað sölu- og innkaupapöntunum, tilboðum, skilapöntunum og standandi pöntunum og þú getur notað skráða skjalið til að endurskapa skjalið sem það var safnvistað frá.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 02/14/2018
ms.author: sgroespe
ms.openlocfilehash: 2f05313d30aede255e4ef49065f0189d649ce93c
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/08/2019
ms.locfileid: "800622"
---
# <a name="archive-documents"></a><span data-ttu-id="5e6f3-103">Safnvista skjöl</span><span class="sxs-lookup"><span data-stu-id="5e6f3-103">Archive Documents</span></span>
<span data-ttu-id="5e6f3-104">Þú getur safnvistað sölu- og innkaupapöntunum, tilboðum, skilapöntunum og standandi pöntunum, t.d. vegna þess að þú vilt vista afrit af skjali til að nota aftur seinna.</span><span class="sxs-lookup"><span data-stu-id="5e6f3-104">You can archive sales and purchase orders, quotes, return orders, and blanket orders, for example because you want to save a copy of a document for reuse later.</span></span> <span data-ttu-id="5e6f3-105">Þú getur safnvistað sölu- eða innkaupaskjali nokkrum sinnum og vistað aðra safnvistaða útgáfu í hvert skipti.</span><span class="sxs-lookup"><span data-stu-id="5e6f3-105">You can archive a sales or purchase document several times, saving a different archived version each time.</span></span>

<span data-ttu-id="5e6f3-106">Fyrir safnvistuð skjöl þar sem upprunalega skjalið er ennþá til og er ekki bókað, getur þú notað virknina **Endurheimta** til að skrifa yfir upprunalega skjalið með safnvistuðu útgáfu skjalsins.</span><span class="sxs-lookup"><span data-stu-id="5e6f3-106">For archived documents where the original still exists and is not posted, you can use the **Restore** function to overwrite the original with the archived version of the document.</span></span> <span data-ttu-id="5e6f3-107">Þetta er hagnýtt ef þú þarft að endurheimta eldri stöðu á innihaldi skjals.</span><span class="sxs-lookup"><span data-stu-id="5e6f3-107">This is practical if you need to restore the contents of a document to an earlier state.</span></span>

<span data-ttu-id="5e6f3-108">Fyrir safnvistuð skjöl þar sem upprunalega skjalinu er eytt geturðu aðeins notað efnið aftur með því að afrita gögnin, til dæmis með virkninni **Afrita skjal**.</span><span class="sxs-lookup"><span data-stu-id="5e6f3-108">For archived documents where the original is deleted, you can only reuse the content by copying the data, for example with the **Copy Document** function.</span></span>   

## <a name="to-set-up-automatic-document-archiving"></a><span data-ttu-id="5e6f3-109">Setja upp sjálfvirka safnvistun</span><span class="sxs-lookup"><span data-stu-id="5e6f3-109">To set up automatic document archiving</span></span>  
<span data-ttu-id="5e6f3-110">Hægt er að setja upp sjálfvirka safnvistun á sölu- og innkaupapöntnum, tilboðum, standandi pöntunum og vöruskilapöntunum áður en skjölum er eytt.</span><span class="sxs-lookup"><span data-stu-id="5e6f3-110">You can set up automatic archiving of sales and purchase orders, quotes, blanket orders, and return orders, before you delete documents.</span></span>

<span data-ttu-id="5e6f3-111">Eftirfarandi ferli sýnir hvernig skal setja upp sjálfvirka safnvistun á söluskjölum.</span><span class="sxs-lookup"><span data-stu-id="5e6f3-111">The following procedure describes how to set up automatic archiving of sales documents.</span></span> <span data-ttu-id="5e6f3-112">Skrefin eru svipuð fyrir innkaupaskjöl.</span><span class="sxs-lookup"><span data-stu-id="5e6f3-112">The steps are similar for purchase documents.</span></span>
1.  <span data-ttu-id="5e6f3-113">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Uppsetning sölu & útistandandi** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="5e6f3-113">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales & Receivables Setup**, and then choose the related link.</span></span>
2. <span data-ttu-id="5e6f3-114">Á síðunni **Uppsetning sölu & útistandandi** er fyllt út í reitina á eftirfarandi hátt.</span><span class="sxs-lookup"><span data-stu-id="5e6f3-114">On the **Sales & Receivables Setup** page, fill in the fields as follows.</span></span>

|<span data-ttu-id="5e6f3-115">Svæði</span><span class="sxs-lookup"><span data-stu-id="5e6f3-115">Field</span></span>|<span data-ttu-id="5e6f3-116">Description</span><span class="sxs-lookup"><span data-stu-id="5e6f3-116">Description</span></span>|
|-----|-----------|
|<span data-ttu-id="5e6f3-117">**Safnvista sölutilboð**</span><span class="sxs-lookup"><span data-stu-id="5e6f3-117">**Archiving Sales Quotes**</span></span>|<span data-ttu-id="5e6f3-118">**Aldrei** til að aldrei safnvista sölutilboðum þegar þeim er eytt.</span><span class="sxs-lookup"><span data-stu-id="5e6f3-118">**Never** to never archive sales quotes when they are deleted.</span></span> <span data-ttu-id="5e6f3-119">**Spurning** til að biðja notandann um að velja hvort safnvista eigi sölutilboðum þegar þeim er eytt.</span><span class="sxs-lookup"><span data-stu-id="5e6f3-119">**Question** to prompt the user to choose whether to archive sales quotes when they are deleted.</span></span> <span data-ttu-id="5e6f3-120">**Alltaf** til að safnvista sölutilboðum sjálfkrafa þegar þeim er eytt.</span><span class="sxs-lookup"><span data-stu-id="5e6f3-120">**Always** to archive sales quotes automatically when they are deleted.</span></span>|
|<span data-ttu-id="5e6f3-121">**Safnvista standandi sölupöntunum**</span><span class="sxs-lookup"><span data-stu-id="5e6f3-121">**Archiving Blanket Sales Orders**</span></span>|<span data-ttu-id="5e6f3-122">Veldu að safnvista standandi sölupöntunum sjálfkrafa í hvert skipti sem þeim er eytt.</span><span class="sxs-lookup"><span data-stu-id="5e6f3-122">Select to archive blanket sales orders automatically each time they are deleted.</span></span>|
|<span data-ttu-id="5e6f3-123">**Safnvista pöntunum og vöruskilapöntunum**</span><span class="sxs-lookup"><span data-stu-id="5e6f3-123">**Arch. Orders and Ret. Orders**</span></span>|<span data-ttu-id="5e6f3-124">Veldu til að safnvista sölupöntunum sjálfkrafa í hvert skipti sem þeim eru eytt.</span><span class="sxs-lookup"><span data-stu-id="5e6f3-124">Select to automatically archive sales orders each time they are deleted.</span></span>|

## <a name="to-archive-a-sales-order"></a><span data-ttu-id="5e6f3-125">Til að safnvista sölupöntun</span><span class="sxs-lookup"><span data-stu-id="5e6f3-125">To archive a sales order</span></span>
<span data-ttu-id="5e6f3-126">Eftirfarandi ferli sýnir hvernig skal safnvista sölupöntun.</span><span class="sxs-lookup"><span data-stu-id="5e6f3-126">The following procedure describes how to archive a sales order.</span></span> <span data-ttu-id="5e6f3-127">Skrefin eru svipuð fyrir allar pantanir, standandi pantanir, vöruskilapantanir og tilboð.</span><span class="sxs-lookup"><span data-stu-id="5e6f3-127">The steps are similar for all orders, blanket orders, return orders, and quotes.</span></span>

1.  <span data-ttu-id="5e6f3-128">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Sölupantanir** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="5e6f3-128">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Orders**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="5e6f3-129">Opnuð er sölupöntun sem þú vilt kaupa safnvista.</span><span class="sxs-lookup"><span data-stu-id="5e6f3-129">Open a sales order that you want to archive.</span></span>  
3.  <span data-ttu-id="5e6f3-130">Valin er aðgerðin **Safnvista skjal**.</span><span class="sxs-lookup"><span data-stu-id="5e6f3-130">Choose the **Archive Document** action.</span></span>

<span data-ttu-id="5e6f3-131">Sölupöntunin er safnvistuð.</span><span class="sxs-lookup"><span data-stu-id="5e6f3-131">The sales order is archived.</span></span> <span data-ttu-id="5e6f3-132">Hægt er að skoða hana á síðunni **Safnvistaðar sölupantanir**.</span><span class="sxs-lookup"><span data-stu-id="5e6f3-132">You can view it on the **Archived Sales orders** page.</span></span>

## <a name="to-restore-a-non-posted-sales-order-from-the-archive"></a><span data-ttu-id="5e6f3-133">Að endurheimta óbókaða sölupöntun úr skjalasafninu</span><span class="sxs-lookup"><span data-stu-id="5e6f3-133">To restore a non-posted sales order from the archive</span></span>
<span data-ttu-id="5e6f3-134">Eftirfarandi ferli sýnir hvernig skal ná innihaldi safnvistaðrar sölupöntunar aftur í upprunalega sölupöntun.</span><span class="sxs-lookup"><span data-stu-id="5e6f3-134">The following procedure describes how to bring the contents of an archived sales order back to the original sales order.</span></span> <span data-ttu-id="5e6f3-135">Þetta er aðeins mögulegt þegar upprunalega skjalið hefur ekki verið bókað.</span><span class="sxs-lookup"><span data-stu-id="5e6f3-135">This is only possible when the original document has not been posted.</span></span> <span data-ttu-id="5e6f3-136">Skrefin eru svipuð fyrir allar pantanir, standandi pantanir, vöruskilapantanir og tilboð.</span><span class="sxs-lookup"><span data-stu-id="5e6f3-136">The steps are similar for all orders, blanket orders, return orders, and quotes.</span></span>

1. <span data-ttu-id="5e6f3-137">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Safnvistaðar sölupantanir** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="5e6f3-137">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Archived Sales Orders**, and then choose the related link.</span></span>
2. <span data-ttu-id="5e6f3-138">Valin er safnvistuð sölupöntun, eða útgáfa af henni, sem á að endurheimta og velja síðan aðgerðina **Endurheimta**.</span><span class="sxs-lookup"><span data-stu-id="5e6f3-138">Select the archived sales order, or version of it, that you want to restore, and then choose the **Restore** action.</span></span>  

<span data-ttu-id="5e6f3-139">Innihald upphaflegu sölupöntunar er skipt út fyrir innihald völdu safnvistuðu útgáfunnar.</span><span class="sxs-lookup"><span data-stu-id="5e6f3-139">The contents of the original sales order is replaced with that of the selected archived version.</span></span>

## <a name="to-delete-archived-sales-orders"></a><span data-ttu-id="5e6f3-140">Eyða safnvistuðum sölupöntunum</span><span class="sxs-lookup"><span data-stu-id="5e6f3-140">To delete archived sales orders</span></span>
<span data-ttu-id="5e6f3-141">Eftirfarandi ferli sýnir hvernig skal eyða safnvistuðum sölupöntunum.</span><span class="sxs-lookup"><span data-stu-id="5e6f3-141">The following procedure describes how to delete archived sales orders.</span></span> <span data-ttu-id="5e6f3-142">Skrefin eru svipuð fyrir aðrar safnvistaðar sölur og innkaupaskjöl.</span><span class="sxs-lookup"><span data-stu-id="5e6f3-142">The steps are similar for other archived sales and purchase documents.</span></span>

1.  <span data-ttu-id="5e6f3-143">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Eyða safnvistaðar útgáfur sölupantana** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="5e6f3-143">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Delete Archived Sales Order Versions**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="5e6f3-144">Á síðunni **Eyða útgáfum sölupantana í skjalasafni** skal velja viðeigandi síur.</span><span class="sxs-lookup"><span data-stu-id="5e6f3-144">On the **Delete Archived Sales Order Versions** page, select the appropriate filters.</span></span>  
3.  <span data-ttu-id="5e6f3-145">Velja hnappinn **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="5e6f3-145">Choose the **OK** button.</span></span>

## <a name="see-also"></a><span data-ttu-id="5e6f3-146">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="5e6f3-146">See Also</span></span>
[<span data-ttu-id="5e6f3-147">Rekja skjalalínur</span><span class="sxs-lookup"><span data-stu-id="5e6f3-147">Track Document Lines</span></span>](across-how-to-track-document-lines.md)  
[<span data-ttu-id="5e6f3-148">Sala</span><span class="sxs-lookup"><span data-stu-id="5e6f3-148">Sales</span></span>](sales-manage-sales.md)  
[<span data-ttu-id="5e6f3-149">Almenn viðskiptavirkni</span><span class="sxs-lookup"><span data-stu-id="5e6f3-149">General Business Functionality</span></span>](ui-across-business-areas.md)  
<span data-ttu-id="5e6f3-150">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="5e6f3-150">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
