---
title: "Hvernig á að rekja vöruraktar vörur | Microsoft Docs"
description: "Hægt er að sjá hvar vörurakin vara var notuð, þar á meðal hvernig og hvenær hún var fengin eða framleidd, millifærð, seld, notuð eða henni skilað. Einnig er hægt að finna öll núverandi tilvik af tilteknu rað- eða lotunúmeri í gagnagrunninum. Það er gert með því að nota Vörurakningu og Færsluleit."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 15676c264736b4547dd32cd7a37b252757f73b2a
ms.contentlocale: is-is
ms.lasthandoff: 03/22/2018

---
# <a name="trace-item-tracked-items"></a><span data-ttu-id="f465f-105">Rekja vöruraktar vörur</span><span class="sxs-lookup"><span data-stu-id="f465f-105">Trace Item-Tracked Items</span></span>
<span data-ttu-id="f465f-106">Hægt er að sjá hvar vörurakin vara var notuð, þar á meðal hvernig og hvenær hún var fengin eða framleidd, millifærð, seld, notuð eða henni skilað.</span><span class="sxs-lookup"><span data-stu-id="f465f-106">You can see where an item-tracked item was used, including how and when it was received or produced, transferred, sold, consumed, or returned.</span></span> <span data-ttu-id="f465f-107">Einnig er hægt að finna öll núverandi tilvik af tilteknu rað- eða lotunúmeri í gagnagrunninum.</span><span class="sxs-lookup"><span data-stu-id="f465f-107">You can also find all current instances of a specific serial or lot number in the database.</span></span> <span data-ttu-id="f465f-108">Það er gert með því að nota Vörurakningu og Færsluleit.</span><span class="sxs-lookup"><span data-stu-id="f465f-108">You do this by using the Item Tracing and the Navigate features.</span></span>  

 <span data-ttu-id="f465f-109">Þessar aðgerðir geta verið sérstaklega nothæfar við gæðastjórnun þegar komast þarf að því hvaða viðskiptavinir fengu vörur með sérstöku lotunúmeri eða þegar komast þarf að því úr hvaða lotu gallaður íhlutur kom.</span><span class="sxs-lookup"><span data-stu-id="f465f-109">These features can be particularly useful in quality control when you need to find out which customers received products with a particular lot number or when you need to find out which lot a defective component came from.</span></span>  

 <span data-ttu-id="f465f-110">Í glugganum **Vörurakning** er hægt að rekja áfram og afturábak í röð bókaðra birgðafærslna fyrir rað- eða lotunúmer.</span><span class="sxs-lookup"><span data-stu-id="f465f-110">In the **Item Tracing** window, you can trace forwards and backwards in a sequence of posted inventory transactions for the serial or lot number.</span></span>  

 <span data-ttu-id="f465f-111">Í glugganum **Færsluleit** er ekki hægt að skoða röð færslna en þar sjást allar færslur rað- eða lotunúmers, bæði bókaðar og opnar.</span><span class="sxs-lookup"><span data-stu-id="f465f-111">In the **Navigate** window, you cannot see the sequence of transactions, but you can see all records of the serial or lot number, both posted entries and open records.</span></span>  

 <span data-ttu-id="f465f-112">Aðgerðirnar tvær má nota í samsetningu með því að flytja inn rakið rað- eða lotunúmer í gluggann **Færsluleit** til að ljúka rakningaraðgerð.</span><span class="sxs-lookup"><span data-stu-id="f465f-112">The two features can be used in combination by transferring a traced serial or lot number to the **Navigate** window to finish a complete trace scenario.</span></span> <span data-ttu-id="f465f-113">Frekari upplýsingar eru í [Kynning: Rekja rað- og lotunúmer](walkthrough-tracing-serial-lot-numbers.md).</span><span class="sxs-lookup"><span data-stu-id="f465f-113">For more information, see [Walkthrough: Tracing Serial-Lot Numbers](walkthrough-tracing-serial-lot-numbers.md).</span></span>  

## <a name="to-trace-item-tracked-items"></a><span data-ttu-id="f465f-114">að rekja vöruraktar vörur</span><span class="sxs-lookup"><span data-stu-id="f465f-114">To trace item-tracked items</span></span>  

1.  <span data-ttu-id="f465f-115">Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Vörurakning** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="f465f-115">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Item Tracing**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="f465f-116">Í afmörkunarreitina efst í glugganum eru slegin inn tilteknu vörunúmerin eða afmörkun á þau vörunúmer sem ætlunin er að rekja.</span><span class="sxs-lookup"><span data-stu-id="f465f-116">In the filter fields at the top of the window, enter the specific item numbers or a filter on the item numbers that you would like to trace.</span></span>  
3.  <span data-ttu-id="f465f-117">Í reitnum **Sýna íhluti** er valið hvort ætlunin sé einnig að sjá hvaðan íhlutirnir fyrir vörurnar komu.</span><span class="sxs-lookup"><span data-stu-id="f465f-117">In the **Show Components** field, select whether you would like to also see where the components for the items came from.</span></span> <span data-ttu-id="f465f-118">Valkostirnir í reitnum eru sem hér segir.</span><span class="sxs-lookup"><span data-stu-id="f465f-118">Your options in this field are as follows.</span></span>  

    |<span data-ttu-id="f465f-119">Svæði</span><span class="sxs-lookup"><span data-stu-id="f465f-119">Field</span></span>|<span data-ttu-id="f465f-120">Description</span><span class="sxs-lookup"><span data-stu-id="f465f-120">Description</span></span>|  
    |----------------------------------|---------------------------------------|  
    |<span data-ttu-id="f465f-121">**Nr**</span><span class="sxs-lookup"><span data-stu-id="f465f-121">**No**</span></span>|<span data-ttu-id="f465f-122">Þessi valkostur er valinn ef ætlunin er ekki að sjá neina íhluti.</span><span class="sxs-lookup"><span data-stu-id="f465f-122">Select this option if you do not want to see any components.</span></span>|  
    |<span data-ttu-id="f465f-123">**Vara-eingöngu rakin**</span><span class="sxs-lookup"><span data-stu-id="f465f-123">**Item-tracked Only**</span></span>|<span data-ttu-id="f465f-124">Þessi valkostur er valinn ef ætlunin er að sjá eingöngu þá íhluti sem hafa lotu- eða raðnúmer.</span><span class="sxs-lookup"><span data-stu-id="f465f-124">Select this option if you want to see only components that have lot or serial numbers.</span></span>|  
    |<span data-ttu-id="f465f-125">**ALLT**</span><span class="sxs-lookup"><span data-stu-id="f465f-125">**All**</span></span>|<span data-ttu-id="f465f-126">Þessi valkostur er valinn ef ætlunin er að sjá alla íhlutina.</span><span class="sxs-lookup"><span data-stu-id="f465f-126">Select this option if you want to see all components.</span></span>|  

4.  <span data-ttu-id="f465f-127">Í reitnum **Rakningaraðferð** er valin sú aðferð sem nota á til að rekja vöruna.</span><span class="sxs-lookup"><span data-stu-id="f465f-127">In the **Trace Method** field, select the method you would like to use for tracing the item.</span></span> <span data-ttu-id="f465f-128">Valkostirnir eru eftirfarandi</span><span class="sxs-lookup"><span data-stu-id="f465f-128">The options are as follows</span></span>  

    |<span data-ttu-id="f465f-129">Svæði</span><span class="sxs-lookup"><span data-stu-id="f465f-129">Field</span></span>|<span data-ttu-id="f465f-130">Description</span><span class="sxs-lookup"><span data-stu-id="f465f-130">Description</span></span>|  
    |----------------------------------|---------------------------------------|  
    |<span data-ttu-id="f465f-131">**Notkun->Uppruni**</span><span class="sxs-lookup"><span data-stu-id="f465f-131">**Usage->Origin**</span></span>|<span data-ttu-id="f465f-132">Þessi aðferð rekur vöruna frá því hvar hún var notuð til þess hvaðan hún kom.</span><span class="sxs-lookup"><span data-stu-id="f465f-132">This method traces the item starting from where it was used to where it came from.</span></span> <span data-ttu-id="f465f-133">Ef framleidd vara var til dæmis seld viðskiptavini sýnir glugginn **Vörurakning** þetta fyrst með söluafhendingarlínunni og svo er hægt að víkka út til að sjá úr hvaða framleiðslupöntun hún kom.</span><span class="sxs-lookup"><span data-stu-id="f465f-133">For instance, if a manufactured item was sold to a customer, the **Item Tracing** window shows this with the sales shipment line first, which you can then expand to see from which production order it came.</span></span>|  
    |<span data-ttu-id="f465f-134">**Uppruni->Notkun**</span><span class="sxs-lookup"><span data-stu-id="f465f-134">**Origin->Usage**</span></span>|<span data-ttu-id="f465f-135">Þessi aðferð rekur vöruna frá því hvar hún kom inn í birgðir til þess hvar hún var notuð.</span><span class="sxs-lookup"><span data-stu-id="f465f-135">This method traces the item starting from where it came into inventory to where it was used.</span></span> <span data-ttu-id="f465f-136">Ef framleidd vara var til dæmis seld viðskiptavini sýnir glugginn **Vörurakning** þetta fyrst með fullunnu framleiðslupöntuninni, sem svo er hægt að víkka út til að sjá söluafhendingarlínur þar sem varan var notuð.</span><span class="sxs-lookup"><span data-stu-id="f465f-136">For instance, if a manufactured item was sold to a customer, the **Item Tracing** window shows this with the finished production order first, which you can then expand to see sale shipment lines where the item was used.</span></span>|  

5.  <span data-ttu-id="f465f-137">Velja skal **Rekja** aðgerðina til að keyra rakninguna.</span><span class="sxs-lookup"><span data-stu-id="f465f-137">Choose the **Trace** action to run the trace.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="f465f-138">Ef sama lota er móttekin í fleiri en einni færslu sýnir glugginn **Vörurakning** hugsanlega ekki allar færslurnar.</span><span class="sxs-lookup"><span data-stu-id="f465f-138">If you have received the same lot on more transactions, then the **Item Tracing** window may not show all transactions.</span></span> <span data-ttu-id="f465f-139">Aðeins notaðar færslur eru sýndar.</span><span class="sxs-lookup"><span data-stu-id="f465f-139">Only applied transactions are shown.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="f465f-140">Ef lína fyrir ofan vörurakningarlínu hefur þegar rekið færsluferil er gátreiturinn **Þegar verið rakið** valinn.</span><span class="sxs-lookup"><span data-stu-id="f465f-140">If additional transaction history under an item tracing line has already been traced by another line above it, then the **Already Traced** check box is selected.</span></span> <span data-ttu-id="f465f-141">Til að veita einfaldara yfirlit eru slíkar undirliggjandi línur ekki sýndar.</span><span class="sxs-lookup"><span data-stu-id="f465f-141">To provide a simpler view, such underlying lines are not shown.</span></span>  
>   
>  <span data-ttu-id="f465f-142">Til að finna vörurakningarlínur þar sem færsluferill hefur þegar verið rakinn skal velja hnappinn **Fara í það sem hefur verið rakið**.</span><span class="sxs-lookup"><span data-stu-id="f465f-142">To find the item tracing lines where the transaction history has already been traced, choose the **Go to Already Traced** button.</span></span> <span data-ttu-id="f465f-143">Viðkomandi vörurakningarlína er valin og allar undirliggjandi línur eru stækkaðar.</span><span class="sxs-lookup"><span data-stu-id="f465f-143">The item tracing line in question is selected, and all underlying lines are expanded.</span></span>  

## <a name="to-find-item-tracked-items-with-navigate"></a><span data-ttu-id="f465f-144">Til að finna vöruraktar vörur með Færsluleit</span><span class="sxs-lookup"><span data-stu-id="f465f-144">To find item-tracked items with Navigate</span></span>  

1.  <span data-ttu-id="f465f-145">Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Færsluleit** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="f465f-145">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Navigate**, and then select the related link.</span></span>  
2.  <span data-ttu-id="f465f-146">Á flýtiflipanum **Vörurakning**, í reitunum **Raðnúmer** og **Lotunr.**, skal færa inn vörurakningarnúmer sem ætlunin er að rekja.</span><span class="sxs-lookup"><span data-stu-id="f465f-146">On the **Item Tracking** FastTab, in the **Serial No.** and **Lot No.** fields, enter the item tracking numbers that you want to trace.</span></span>  
3.  <span data-ttu-id="f465f-147">Velja skal aðgerðina **Finna** til að finna öll tilvik um rað- eða lotunúmerið í gagnagrunninum.</span><span class="sxs-lookup"><span data-stu-id="f465f-147">Choose the **Find** action to find all instances of the serial or lot number in the database.</span></span>  

## <a name="see-also"></a><span data-ttu-id="f465f-148">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="f465f-148">See Also</span></span>  
[<span data-ttu-id="f465f-149">Birgðir</span><span class="sxs-lookup"><span data-stu-id="f465f-149">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="f465f-150">[Hönnunarupplýsingar: vörurakning](design-details-item-tracking.md)
[Hönnunarupplýsingar - vörurakning og frátekning](design-details-item-tracking-and-reservations.md)</span><span class="sxs-lookup"><span data-stu-id="f465f-150">[Design Details: Item Tracking](design-details-item-tracking.md)
[Design Details - Item Tracking and Reservations](design-details-item-tracking-and-reservations.md)</span></span>  
[<span data-ttu-id="f465f-151">Taka frá vörur</span><span class="sxs-lookup"><span data-stu-id="f465f-151">Reserve Items</span></span>](inventory-how-to-reserve-items.md)  
<span data-ttu-id="f465f-152">[Vinna með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
[Kynning: Rekja rað- og lotunúmer](walkthrough-tracing-serial-lot-numbers.md).</span><span class="sxs-lookup"><span data-stu-id="f465f-152">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
[Walkthrough: Tracing Serial-Lot Numbers](walkthrough-tracing-serial-lot-numbers.md)</span></span>

