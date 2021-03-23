---
title: Hvernig skal safnvista sölu- og innkaupaskjölum | Microsoft Docs
description: Þú getur safnvistað sölu- og innkaupapöntunum, tilboðum, skilapöntunum og standandi pöntunum og þú getur notað skráða skjalið til að endurskapa skjalið sem það var safnvistað frá.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 8ec1ab53a2df71d46c671f71673a0b25ea6704bf
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5384575"
---
# <a name="archive-documents"></a><span data-ttu-id="81297-103">Safnvista skjöl</span><span class="sxs-lookup"><span data-stu-id="81297-103">Archive Documents</span></span>
<span data-ttu-id="81297-104">Þú getur safnvistað sölu- og innkaupapöntunum, tilboðum, skilapöntunum og standandi pöntunum, t.d. vegna þess að þú vilt vista afrit af skjali til að nota aftur seinna.</span><span class="sxs-lookup"><span data-stu-id="81297-104">You can archive sales and purchase orders, quotes, return orders, and blanket orders, for example because you want to save a copy of a document for reuse later.</span></span> <span data-ttu-id="81297-105">Þú getur safnvistað sölu- eða innkaupaskjali nokkrum sinnum og vistað aðra safnvistaða útgáfu í hvert skipti.</span><span class="sxs-lookup"><span data-stu-id="81297-105">You can archive a sales or purchase document several times, saving a different archived version each time.</span></span>

<span data-ttu-id="81297-106">Fyrir safnvistuð skjöl þar sem upprunalega skjalið er ennþá til og er ekki bókað, getur þú notað virknina **Endurheimta** til að skrifa yfir upprunalega skjalið með safnvistuðu útgáfu skjalsins.</span><span class="sxs-lookup"><span data-stu-id="81297-106">For archived documents where the original still exists and is not posted, you can use the **Restore** function to overwrite the original with the archived version of the document.</span></span> <span data-ttu-id="81297-107">Þetta er hagnýtt ef þú þarft að endurheimta eldri stöðu á innihaldi skjals.</span><span class="sxs-lookup"><span data-stu-id="81297-107">This is practical if you need to restore the contents of a document to an earlier state.</span></span>

<span data-ttu-id="81297-108">Fyrir safnvistuð skjöl þar sem upprunalega skjalinu er eytt geturðu aðeins notað efnið aftur með því að afrita gögnin, til dæmis með virkninni **Afrita úr skjali**.</span><span class="sxs-lookup"><span data-stu-id="81297-108">For archived documents where the original is deleted, you can only reuse the content by copying the data, for example with the **Copy from Document** function.</span></span>   

## <a name="to-set-up-automatic-document-archiving"></a><span data-ttu-id="81297-109">Setja upp sjálfvirka safnvistun</span><span class="sxs-lookup"><span data-stu-id="81297-109">To set up automatic document archiving</span></span>  
<span data-ttu-id="81297-110">Hægt er að setja upp sjálfvirka safnvistun á sölu- og innkaupapöntnum, tilboðum, standandi pöntunum og vöruskilapöntunum áður en skjölum er eytt.</span><span class="sxs-lookup"><span data-stu-id="81297-110">You can set up automatic archiving of sales and purchase orders, quotes, blanket orders, and return orders, before you delete documents.</span></span>

<span data-ttu-id="81297-111">Eftirfarandi ferli sýnir hvernig skal setja upp sjálfvirka safnvistun á söluskjölum.</span><span class="sxs-lookup"><span data-stu-id="81297-111">The following procedure describes how to set up automatic archiving of sales documents.</span></span> <span data-ttu-id="81297-112">Skrefin eru svipuð fyrir innkaupaskjöl.</span><span class="sxs-lookup"><span data-stu-id="81297-112">The steps are similar for purchase documents.</span></span>
1.  <span data-ttu-id="81297-113">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Sölugrunnur** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="81297-113">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales & Receivables Setup**, and then choose the related link.</span></span>
2. <span data-ttu-id="81297-114">Á síðunni **Uppsetning sölu & útistandandi** er fyllt út í reitina á eftirfarandi hátt.</span><span class="sxs-lookup"><span data-stu-id="81297-114">On the **Sales & Receivables Setup** page, fill in the fields as follows.</span></span>

|<span data-ttu-id="81297-115">Svæði</span><span class="sxs-lookup"><span data-stu-id="81297-115">Field</span></span>|<span data-ttu-id="81297-116">Description</span><span class="sxs-lookup"><span data-stu-id="81297-116">Description</span></span>|
|-----|-----------|
|<span data-ttu-id="81297-117">**Safnvista sölutilboð**</span><span class="sxs-lookup"><span data-stu-id="81297-117">**Archiving Sales Quotes**</span></span>|<span data-ttu-id="81297-118">**Aldrei** til að aldrei safnvista sölutilboðum þegar þeim er eytt.</span><span class="sxs-lookup"><span data-stu-id="81297-118">**Never** to never archive sales quotes when they are deleted.</span></span> <span data-ttu-id="81297-119">**Spurning** til að biðja notandann um að velja hvort safnvista eigi sölutilboðum þegar þeim er eytt.</span><span class="sxs-lookup"><span data-stu-id="81297-119">**Question** to prompt the user to choose whether to archive sales quotes when they are deleted.</span></span> <span data-ttu-id="81297-120">**Alltaf** til að safnvista sölutilboðum sjálfkrafa þegar þeim er eytt.</span><span class="sxs-lookup"><span data-stu-id="81297-120">**Always** to archive sales quotes automatically when they are deleted.</span></span>|
|<span data-ttu-id="81297-121">**Safnvista standandi sölupöntunum**</span><span class="sxs-lookup"><span data-stu-id="81297-121">**Archiving Blanket Sales Orders**</span></span>|<span data-ttu-id="81297-122">Veldu að safnvista standandi sölupöntunum sjálfkrafa í hvert skipti sem þeim er eytt.</span><span class="sxs-lookup"><span data-stu-id="81297-122">Select to archive blanket sales orders automatically each time they are deleted.</span></span>|
|<span data-ttu-id="81297-123">**Safnvista pöntunum og vöruskilapöntunum**</span><span class="sxs-lookup"><span data-stu-id="81297-123">**Arch. Orders and Ret. Orders**</span></span>|<span data-ttu-id="81297-124">Veldu til að safnvista sölupöntunum sjálfkrafa í hvert skipti sem þeim eru eytt.</span><span class="sxs-lookup"><span data-stu-id="81297-124">Select to automatically archive sales orders each time they are deleted.</span></span>|

## <a name="to-archive-a-sales-order"></a><span data-ttu-id="81297-125">Til að safnvista sölupöntun</span><span class="sxs-lookup"><span data-stu-id="81297-125">To archive a sales order</span></span>
<span data-ttu-id="81297-126">Eftirfarandi ferli sýnir hvernig skal safnvista sölupöntun.</span><span class="sxs-lookup"><span data-stu-id="81297-126">The following procedure describes how to archive a sales order.</span></span> <span data-ttu-id="81297-127">Skrefin eru svipuð fyrir allar pantanir, standandi pantanir, vöruskilapantanir og tilboð.</span><span class="sxs-lookup"><span data-stu-id="81297-127">The steps are similar for all orders, blanket orders, return orders, and quotes.</span></span>

1.  <span data-ttu-id="81297-128">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Sölupantanir** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="81297-128">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Orders**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="81297-129">Opnuð er sölupöntun sem þú vilt kaupa safnvista.</span><span class="sxs-lookup"><span data-stu-id="81297-129">Open a sales order that you want to archive.</span></span>  
3.  <span data-ttu-id="81297-130">Valin er aðgerðin **Safnvista skjal**.</span><span class="sxs-lookup"><span data-stu-id="81297-130">Choose the **Archive Document** action.</span></span>

<span data-ttu-id="81297-131">Sölupöntunin er safnvistuð.</span><span class="sxs-lookup"><span data-stu-id="81297-131">The sales order is archived.</span></span> <span data-ttu-id="81297-132">Hægt er að skoða hana á síðunni **Safnvistaðar sölupantanir**.</span><span class="sxs-lookup"><span data-stu-id="81297-132">You can view it on the **Archived Sales Orders** page.</span></span>

## <a name="to-restore-a-non-posted-sales-order-from-the-archive"></a><span data-ttu-id="81297-133">Að endurheimta óbókaða sölupöntun úr skjalasafninu</span><span class="sxs-lookup"><span data-stu-id="81297-133">To restore a non-posted sales order from the archive</span></span>
<span data-ttu-id="81297-134">Eftirfarandi ferli sýnir hvernig skal ná innihaldi safnvistaðrar sölupöntunar aftur í upprunalega sölupöntun.</span><span class="sxs-lookup"><span data-stu-id="81297-134">The following procedure describes how to bring the contents of an archived sales order back to the original sales order.</span></span> <span data-ttu-id="81297-135">Þetta er aðeins mögulegt þegar upprunalega skjalið hefur ekki verið bókað.</span><span class="sxs-lookup"><span data-stu-id="81297-135">This is only possible when the original document has not been posted.</span></span> <span data-ttu-id="81297-136">Skrefin eru svipuð fyrir allar pantanir, standandi pantanir, vöruskilapantanir og tilboð.</span><span class="sxs-lookup"><span data-stu-id="81297-136">The steps are similar for all orders, blanket orders, return orders, and quotes.</span></span>

1. <span data-ttu-id="81297-137">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Safnvistaðar sölupantanir** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="81297-137">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Archived Sales Orders**, and then choose the related link.</span></span>
2. <span data-ttu-id="81297-138">Valin er safnvistuð sölupöntun, eða útgáfa af henni, sem á að endurheimta og velja síðan aðgerðina **Endurheimta**.</span><span class="sxs-lookup"><span data-stu-id="81297-138">Select the archived sales order, or version of it, that you want to restore, and then choose the **Restore** action.</span></span>  

<span data-ttu-id="81297-139">Innihald upphaflegu sölupöntunar er skipt út fyrir innihald völdu safnvistuðu útgáfunnar.</span><span class="sxs-lookup"><span data-stu-id="81297-139">The contents of the original sales order is replaced with that of the selected archived version.</span></span>

## <a name="to-delete-archived-sales-orders"></a><span data-ttu-id="81297-140">Eyða safnvistuðum sölupöntunum</span><span class="sxs-lookup"><span data-stu-id="81297-140">To delete archived sales orders</span></span>
<span data-ttu-id="81297-141">Eftirfarandi ferli sýnir hvernig skal eyða safnvistuðum sölupöntunum.</span><span class="sxs-lookup"><span data-stu-id="81297-141">The following procedure describes how to delete archived sales orders.</span></span> <span data-ttu-id="81297-142">Skrefin eru svipuð fyrir aðrar safnvistaðar sölur og innkaupaskjöl.</span><span class="sxs-lookup"><span data-stu-id="81297-142">The steps are similar for other archived sales and purchase documents.</span></span>

1.  <span data-ttu-id="81297-143">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Eyða útgáfum sölupantana í skjalasafni** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="81297-143">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Delete Archived Sales Order Versions**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="81297-144">Á síðunni **Eyða útgáfum sölupantana í skjalasafni** skal velja viðeigandi síur.</span><span class="sxs-lookup"><span data-stu-id="81297-144">On the **Delete Archived Sales Order Versions** page, select the appropriate filters.</span></span>  
3.  <span data-ttu-id="81297-145">Velja hnappinn **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="81297-145">Choose the **OK** button.</span></span>

## <a name="see-also"></a><span data-ttu-id="81297-146">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="81297-146">See Also</span></span>
[<span data-ttu-id="81297-147">Rekja skjalalínur</span><span class="sxs-lookup"><span data-stu-id="81297-147">Track Document Lines</span></span>](across-how-to-track-document-lines.md)  
[<span data-ttu-id="81297-148">Sala</span><span class="sxs-lookup"><span data-stu-id="81297-148">Sales</span></span>](sales-manage-sales.md)  
[<span data-ttu-id="81297-149">Almenn viðskiptavirkni</span><span class="sxs-lookup"><span data-stu-id="81297-149">General Business Functionality</span></span>](ui-across-business-areas.md)  
<span data-ttu-id="81297-150">[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="81297-150">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]