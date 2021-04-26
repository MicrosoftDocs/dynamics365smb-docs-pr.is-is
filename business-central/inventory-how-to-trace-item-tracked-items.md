---
title: Rekja vöruraktar vörur
description: Hægt er að sjá hvar vörurakin vara var notuð, þar á meðal hvernig og hvenær hún var fengin eða framleidd, millifærð, seld, notuð eða henni skilað. Einnig er hægt að finna öll núverandi tilvik af tilteknu rað- eða lotunúmeri í gagnagrunninum. Þetta er gert með því að nota vörurakningu og eiginleikann Finna færslur.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: a425b974bf37b440de27f2b469694f9e8eac07de
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5785700"
---
# <a name="trace-item-tracked-items"></a><span data-ttu-id="d0d11-105">Rekja vöruraktar vörur</span><span class="sxs-lookup"><span data-stu-id="d0d11-105">Trace Item-Tracked Items</span></span>
<span data-ttu-id="d0d11-106">Hægt er að sjá hvar vörurakin vara var notuð, þar á meðal hvernig og hvenær hún var fengin eða framleidd, millifærð, seld, notuð eða henni skilað.</span><span class="sxs-lookup"><span data-stu-id="d0d11-106">You can see where an item-tracked item was used, including how and when it was received or produced, transferred, sold, consumed, or returned.</span></span> <span data-ttu-id="d0d11-107">Einnig er hægt að finna öll núverandi tilvik af tilteknu rað- eða lotunúmeri í gagnagrunninum.</span><span class="sxs-lookup"><span data-stu-id="d0d11-107">You can also find all current instances of a specific serial or lot number in the database.</span></span> <span data-ttu-id="d0d11-108">Þetta er gert með því að nota vörurakningu og eiginleikann [Finna færslur](ui-find-entries.md).</span><span class="sxs-lookup"><span data-stu-id="d0d11-108">You do this by using the Item Tracing and the [Find Entries](ui-find-entries.md) features.</span></span>  

<span data-ttu-id="d0d11-109">Þessar aðgerðir geta verið sérstaklega nothæfar við gæðastjórnun þegar komast þarf að því hvaða viðskiptavinir fengu vörur með sérstöku lotunúmeri eða þegar komast þarf að því úr hvaða lotu gallaður íhlutur kom.</span><span class="sxs-lookup"><span data-stu-id="d0d11-109">These features can be particularly useful in quality control when you need to find out which customers received products with a particular lot number or when you need to find out which lot a defective component came from.</span></span>  

 <span data-ttu-id="d0d11-110">Á síðunni **Vörurakning** er hægt að rekja áfram og afturábak í röð bókaðra birgðafærslna fyrir rað- eða lotunúmer.</span><span class="sxs-lookup"><span data-stu-id="d0d11-110">On the **Item Tracing** page, you can trace forwards and backwards in a sequence of posted inventory transactions for the serial or lot number.</span></span>  

 <span data-ttu-id="d0d11-111">Á síðunni **Færsluleit** er ekki hægt að skoða röð færslna en þar sjást allar færslur rað- eða lotunúmers, bæði bókaðar og opnar færslur.</span><span class="sxs-lookup"><span data-stu-id="d0d11-111">On the **Find Entries** page, you cannot see the sequence of transactions, but you can see all records of the serial or lot number, both posted entries and open records.</span></span>  

 <span data-ttu-id="d0d11-112">Aðgerðirnar tvær má nota saman með því að flytja inn rakið rað- eða lotunúmer yfir á síðuna **Finna færslur** til að ljúka ítarlegri rakningaraðgerð.</span><span class="sxs-lookup"><span data-stu-id="d0d11-112">The two features can be used in combination by transferring a traced serial or lot number to the **Find Entries** page to finish a complete trace scenario.</span></span> <span data-ttu-id="d0d11-113">Frekari upplýsingar eru í [Kynning: Rekja rað- og lotunúmer](walkthrough-tracing-serial-lot-numbers.md).</span><span class="sxs-lookup"><span data-stu-id="d0d11-113">For more information, see [Walkthrough: Tracing Serial-Lot Numbers](walkthrough-tracing-serial-lot-numbers.md).</span></span>  

## <a name="to-trace-item-tracked-items"></a><span data-ttu-id="d0d11-114">að rekja vöruraktar vörur</span><span class="sxs-lookup"><span data-stu-id="d0d11-114">To trace item-tracked items</span></span>  

1.  <span data-ttu-id="d0d11-115">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Vörurakning** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="d0d11-115">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Item Tracing**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="d0d11-116">Í afmörkunarreitunum efst á síðunni skal færa inn tiltekið vörunúmer eða afmörkun á vörunúmerum sem á að rekja.</span><span class="sxs-lookup"><span data-stu-id="d0d11-116">In the filter fields at the top of the page, enter the specific item numbers or a filter on the item numbers that you would like to trace.</span></span>  
3.  <span data-ttu-id="d0d11-117">Í reitnum **Sýna íhluti** er valið hvort ætlunin sé einnig að sjá hvaðan íhlutirnir fyrir vörurnar komu.</span><span class="sxs-lookup"><span data-stu-id="d0d11-117">In the **Show Components** field, select whether you would like to also see where the components for the items came from.</span></span> <span data-ttu-id="d0d11-118">Valkostirnir í reitnum eru sem hér segir.</span><span class="sxs-lookup"><span data-stu-id="d0d11-118">Your options in this field are as follows.</span></span>  

    |<span data-ttu-id="d0d11-119">Svæði</span><span class="sxs-lookup"><span data-stu-id="d0d11-119">Field</span></span>|<span data-ttu-id="d0d11-120">Description</span><span class="sxs-lookup"><span data-stu-id="d0d11-120">Description</span></span>|  
    |----------------------------------|---------------------------------------|  
    |<span data-ttu-id="d0d11-121">**Nr**</span><span class="sxs-lookup"><span data-stu-id="d0d11-121">**No**</span></span>|<span data-ttu-id="d0d11-122">Þessi valkostur er valinn ef ætlunin er ekki að sjá neina íhluti.</span><span class="sxs-lookup"><span data-stu-id="d0d11-122">Select this option if you do not want to see any components.</span></span>|  
    |<span data-ttu-id="d0d11-123">**Vara-eingöngu rakin**</span><span class="sxs-lookup"><span data-stu-id="d0d11-123">**Item-tracked Only**</span></span>|<span data-ttu-id="d0d11-124">Þessi valkostur er valinn ef ætlunin er að sjá eingöngu þá íhluti sem hafa lotu- eða raðnúmer.</span><span class="sxs-lookup"><span data-stu-id="d0d11-124">Select this option if you want to see only components that have lot or serial numbers.</span></span>|  
    |<span data-ttu-id="d0d11-125">**ALLT**</span><span class="sxs-lookup"><span data-stu-id="d0d11-125">**All**</span></span>|<span data-ttu-id="d0d11-126">Þessi valkostur er valinn ef ætlunin er að sjá alla íhlutina.</span><span class="sxs-lookup"><span data-stu-id="d0d11-126">Select this option if you want to see all components.</span></span>|  

4.  <span data-ttu-id="d0d11-127">Í reitnum **Rakningaraðferð** er valin sú aðferð sem nota á til að rekja vöruna.</span><span class="sxs-lookup"><span data-stu-id="d0d11-127">In the **Trace Method** field, select the method you would like to use for tracing the item.</span></span> <span data-ttu-id="d0d11-128">Valkostirnir eru eftirfarandi</span><span class="sxs-lookup"><span data-stu-id="d0d11-128">The options are as follows</span></span>  

    |<span data-ttu-id="d0d11-129">Svæði</span><span class="sxs-lookup"><span data-stu-id="d0d11-129">Field</span></span>|<span data-ttu-id="d0d11-130">Description</span><span class="sxs-lookup"><span data-stu-id="d0d11-130">Description</span></span>|  
    |----------------------------------|---------------------------------------|  
    |<span data-ttu-id="d0d11-131">**Notkun->Uppruni**</span><span class="sxs-lookup"><span data-stu-id="d0d11-131">**Usage->Origin**</span></span>|<span data-ttu-id="d0d11-132">Þessi aðferð rekur vöruna frá því hvar hún var notuð til þess hvaðan hún kom.</span><span class="sxs-lookup"><span data-stu-id="d0d11-132">This method traces the item starting from where it was used to where it came from.</span></span> <span data-ttu-id="d0d11-133">Til dæmis, ef framleidd vara var seld til viðskiptavinar, sýnir síðan **Vörurakning** þetta fyrst með söluafhendingarlínunni sem er síðan hægt að stækka til að sjá frá hvaða framleiðslupöntun hún kom.</span><span class="sxs-lookup"><span data-stu-id="d0d11-133">For instance, if a manufactured item was sold to a customer, the **Item Tracing** page shows this with the sales shipment line first, which you can then expand to see from which production order it came.</span></span>|  
    |<span data-ttu-id="d0d11-134">**Uppruni->Notkun**</span><span class="sxs-lookup"><span data-stu-id="d0d11-134">**Origin->Usage**</span></span>|<span data-ttu-id="d0d11-135">Þessi aðferð rekur vöruna frá því hvar hún kom inn í birgðir til þess hvar hún var notuð.</span><span class="sxs-lookup"><span data-stu-id="d0d11-135">This method traces the item starting from where it came into inventory to where it was used.</span></span> <span data-ttu-id="d0d11-136">Til dæmis, ef framleidd vara var seld til viðskiptavinar, sýnir síðan **Vörurakning** þetta fyrst með tilbúinni framleiðslupöntun, sem er síðan hægt að stækka til að sjá söluafhendingarlínur þar sem varan var notuð.</span><span class="sxs-lookup"><span data-stu-id="d0d11-136">For instance, if a manufactured item was sold to a customer, the **Item Tracing** page shows this with the finished production order first, which you can then expand to see sale shipment lines where the item was used.</span></span>|  

5.  <span data-ttu-id="d0d11-137">Velja skal **Rekja** aðgerðina til að keyra rakninguna.</span><span class="sxs-lookup"><span data-stu-id="d0d11-137">Choose the **Trace** action to run the trace.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="d0d11-138">Ef sama lota er móttekin í fleiri en einni færslu sýnir síðan **Vörurakning** hugsanlega ekki allar færslurnar.</span><span class="sxs-lookup"><span data-stu-id="d0d11-138">If you have received the same lot on more transactions, then the **Item Tracing** page may not show all transactions.</span></span> <span data-ttu-id="d0d11-139">Aðeins notaðar færslur eru sýndar.</span><span class="sxs-lookup"><span data-stu-id="d0d11-139">Only applied transactions are shown.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="d0d11-140">Ef lína fyrir ofan vörurakningarlínu hefur þegar rekið færsluferil er gátreiturinn **Þegar verið rakið** valinn.</span><span class="sxs-lookup"><span data-stu-id="d0d11-140">If additional transaction history under an item tracing line has already been traced by another line above it, then the **Already Traced** check box is selected.</span></span> <span data-ttu-id="d0d11-141">Til að veita einfaldara yfirlit eru slíkar undirliggjandi línur ekki sýndar.</span><span class="sxs-lookup"><span data-stu-id="d0d11-141">To provide a simpler view, such underlying lines are not shown.</span></span>  
>   
>  <span data-ttu-id="d0d11-142">Til að finna vörurakningarlínur þar sem færsluferill hefur þegar verið rakinn skal velja hnappinn **Fara í það sem hefur verið rakið**.</span><span class="sxs-lookup"><span data-stu-id="d0d11-142">To find the item tracing lines where the transaction history has already been traced, choose the **Go to Already Traced** button.</span></span> <span data-ttu-id="d0d11-143">Viðkomandi vörurakningarlína er valin og allar undirliggjandi línur eru stækkaðar.</span><span class="sxs-lookup"><span data-stu-id="d0d11-143">The item tracing line in question is selected, and all underlying lines are expanded.</span></span>  

## <a name="to-find-item-tracked-items-with-find-entries"></a><span data-ttu-id="d0d11-144">Til að finna vöruraktar vörur með Finna færslur</span><span class="sxs-lookup"><span data-stu-id="d0d11-144">To find item-tracked items with Find Entries</span></span>  

1. <span data-ttu-id="d0d11-145">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Finna færslur** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="d0d11-145">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Find Entries**, and then select the related link.</span></span>  
2. <span data-ttu-id="d0d11-146">Veljið **Aðgerðir** > **Leita eftir** > **Leita eftir vörutilvísun**.</span><span class="sxs-lookup"><span data-stu-id="d0d11-146">Choose **Actions** > **Find by** > **Find by Item Reference**.</span></span>
3. <span data-ttu-id="d0d11-147">Í reitina **Raðnúmer** og **Lotunúmer** skal færa inn vörurakningarnúmer sem ætlunin er að rekja.</span><span class="sxs-lookup"><span data-stu-id="d0d11-147">In the **Serial No.** and **Lot No.** fields, enter the item tracking numbers that you want to trace.</span></span>  
4. <span data-ttu-id="d0d11-148">Velja skal aðgerðina **Finna** til að finna öll tilvik um rað- eða lotunúmerið í gagnagrunninum.</span><span class="sxs-lookup"><span data-stu-id="d0d11-148">Choose the **Find** action to find all instances of the serial or lot number in the database.</span></span>  

## <a name="see-also"></a><span data-ttu-id="d0d11-149">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="d0d11-149">See Also</span></span>

[<span data-ttu-id="d0d11-150">Birgðir</span><span class="sxs-lookup"><span data-stu-id="d0d11-150">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="d0d11-151">Vinna með raðnúmer, lotu og pakkanúmer</span><span class="sxs-lookup"><span data-stu-id="d0d11-151">Work with Serial, Lot, and Package Numbers</span></span>](inventory-how-work-item-tracking.md)  
[<span data-ttu-id="d0d11-152">Hönnunarupplýsingar: Vörurakning</span><span class="sxs-lookup"><span data-stu-id="d0d11-152">Design Details: Item Tracking</span></span>](design-details-item-tracking.md)  
[<span data-ttu-id="d0d11-153">Hönnunarupplýsingar - vörurakning og frátekningar</span><span class="sxs-lookup"><span data-stu-id="d0d11-153">Design Details - Item Tracking and Reservations</span></span>](design-details-item-tracking-and-reservations.md)  
[<span data-ttu-id="d0d11-154">Taka frá vörur</span><span class="sxs-lookup"><span data-stu-id="d0d11-154">Reserve Items</span></span>](inventory-how-to-reserve-items.md)  
<span data-ttu-id="d0d11-155">[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="d0d11-155">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="d0d11-156">Kynning: Rað-/lotunúmerarakning</span><span class="sxs-lookup"><span data-stu-id="d0d11-156">Walkthrough: Tracing Serial-Lot Numbers</span></span>](walkthrough-tracing-serial-lot-numbers.md)  
[<span data-ttu-id="d0d11-157">Finna færslur</span><span class="sxs-lookup"><span data-stu-id="d0d11-157">Find Entries</span></span>](ui-find-entries.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]