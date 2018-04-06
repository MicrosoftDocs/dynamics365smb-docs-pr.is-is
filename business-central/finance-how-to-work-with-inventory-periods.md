---
title: "Hvernig á að vinna með birgðatímabil | Microsoft Docs"
description: "Hægt er að stjórna tímarammanum þar sem fólk getur bókað breytingar á birgðum með því að skilgreina birgðatímabil."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: inventory, periods
ms.date: 08/07/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: d302483ca2d66870670aaa0914533472a807d04f
ms.contentlocale: is-is
ms.lasthandoff: 03/22/2018

---
# <a name="work-with-inventory-periods"></a><span data-ttu-id="ac20a-103">Vinna við birgðatímabil</span><span class="sxs-lookup"><span data-stu-id="ac20a-103">Work with Inventory Periods</span></span>
<span data-ttu-id="ac20a-104">Birgðatímabil skilgreina tímabil þar sem hægt er að bóka breytingar á birgðum.</span><span class="sxs-lookup"><span data-stu-id="ac20a-104">Inventory periods define a period of time in which you can post changes to inventory.</span></span> <span data-ttu-id="ac20a-105">Birgðatímabil afmarkast af dagsetningunni sem því lýkur á.</span><span class="sxs-lookup"><span data-stu-id="ac20a-105">An inventory period is defined by the date on which it ends, or the ending date.</span></span> <span data-ttu-id="ac20a-106">Þegar birgðatímabili er lokað er ekki hægt að bóka neinar breytingar á birgðum, hvorki áætluðum né reikningsfærðum fyrir þessa lokadagsetningu.</span><span class="sxs-lookup"><span data-stu-id="ac20a-106">When you close an inventory period, you cannot post any changes to inventory, either expected or invoiced, before this ending date.</span></span> <span data-ttu-id="ac20a-107">Ekki er heldur hægt að bóka nein ný gildi við birgðir fyrir lokadagsetninguna.</span><span class="sxs-lookup"><span data-stu-id="ac20a-107">You cannot post any new values to inventory before the ending date.</span></span> <span data-ttu-id="ac20a-108">Ef birgðafærslur eru hafðar opnar í lokaða tímabilinu, sem þýðir jákvætt magn sem ekki er búið að jafna saman við færslur á útleið, er samt hægt að jafna magn á útleið við þessar færslur, jafnvel þó að tímabilið sé lokað.</span><span class="sxs-lookup"><span data-stu-id="ac20a-108">If you have open item entries in the closed period, meaning positive quantities that have not yet been applied to outbound transactions, you can still apply outbound quantities to these entries, even if the period is closed.</span></span>  

<span data-ttu-id="ac20a-109">Eftirfarandi hlutar útskýra hvernig á að standa að:</span><span class="sxs-lookup"><span data-stu-id="ac20a-109">The following sections describe how to:</span></span>  

* <span data-ttu-id="ac20a-110">Stofna birgðatímabil.</span><span class="sxs-lookup"><span data-stu-id="ac20a-110">Create inventory periods.</span></span>  
* <span data-ttu-id="ac20a-111">Lokun birgðatímabila.</span><span class="sxs-lookup"><span data-stu-id="ac20a-111">Close inventory periods.</span></span>  
* <span data-ttu-id="ac20a-112">Enduropna birgðatímabil.</span><span class="sxs-lookup"><span data-stu-id="ac20a-112">Reopen inventory periods.</span></span>  

## <a name="to-create-an-inventory-period"></a><span data-ttu-id="ac20a-113">Til að stofna birgðatímabil</span><span class="sxs-lookup"><span data-stu-id="ac20a-113">To create an inventory period</span></span>  
1. <span data-ttu-id="ac20a-114">Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Birgðatímabil** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="ac20a-114">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Inventory Periods**, and then choose the related link.</span></span>  
2. <span data-ttu-id="ac20a-115">Stofnið nýja línu.</span><span class="sxs-lookup"><span data-stu-id="ac20a-115">Create a new line.</span></span>  
3. <span data-ttu-id="ac20a-116">Í reitinn **Lokadagsetning** er slegin inn síðasta dagsetningin í birgðatímabilinu sem ætlunin er að skilgreina.</span><span class="sxs-lookup"><span data-stu-id="ac20a-116">In the **Ending Date** field, enter the last date in the inventory period that you want to define.</span></span> <span data-ttu-id="ac20a-117">Þegar tímabilinu er lokað verður ekki hægt að bóka breytingar á birgðum fyrir þessa dagsetningu.</span><span class="sxs-lookup"><span data-stu-id="ac20a-117">When the period is closed, you will not be able to post inventory changes before this date.</span></span>  
4. <span data-ttu-id="ac20a-118">Færa inn lýsandi heiti í reitinn **Heiti**.</span><span class="sxs-lookup"><span data-stu-id="ac20a-118">Enter a descriptive name in the **Name** field.</span></span> <span data-ttu-id="ac20a-119">Velja hnappinn **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="ac20a-119">Choose the **OK** button.</span></span>  

## <a name="closing-inventory-periods"></a><span data-ttu-id="ac20a-120">Lokun birgðatímabila</span><span class="sxs-lookup"><span data-stu-id="ac20a-120">Closing Inventory Periods</span></span>  
<span data-ttu-id="ac20a-121">Reiturinn **Lokað** gefur til kynna hvort birgðatímabilið er lokað fyrir breytingum á birgðagildum eður ei.</span><span class="sxs-lookup"><span data-stu-id="ac20a-121">The **Closed** field indicates whether or not the inventory period is closed to inventory value changes.</span></span> <span data-ttu-id="ac20a-122">Ekki er hægt að breyta þessum reit.</span><span class="sxs-lookup"><span data-stu-id="ac20a-122">You cannot edit this field.</span></span>  

<span data-ttu-id="ac20a-123">Hægt er að loka hvaða birgðatímabili sem er, að því gefnu að eftirfarandi sé satt:</span><span class="sxs-lookup"><span data-stu-id="ac20a-123">You can close any inventory period, provided that the following is true:</span></span>  

* <span data-ttu-id="ac20a-124">Engar birgðafærslur eru opnar það er að segja ekki neikvætt birgðamagn, á því tímabili.</span><span class="sxs-lookup"><span data-stu-id="ac20a-124">There are no open outbound item ledger entries, meaning negative inventory, in that period.</span></span>  
* <span data-ttu-id="ac20a-125">Kostnaður allra vara hefur verið leiðréttur með keyrslunni **Leiðr. kostnað - Birgðafærslur**.</span><span class="sxs-lookup"><span data-stu-id="ac20a-125">The cost of all items has been adjusted using the **Adjust Cost – Item Entries** batch job.</span></span>  

<span data-ttu-id="ac20a-126">Þetta þýðir að jafna þarf allt færslumagn á útleið, eins og magnið í sölupöntunum, millifærslum á útleið, sölureikningsfærslum, vöruskilum eða innkaupakreditreikningum við magn sem er fyrir í birgðum.</span><span class="sxs-lookup"><span data-stu-id="ac20a-126">This means that all outbound transaction quantities, such as those from sales orders, outbound transfers, sales invoices, purchase returns, or purchase credit memos, must be applied to existing quantity in inventory.</span></span>  

### <a name="to-close-an-inventory-period"></a><span data-ttu-id="ac20a-127">Til að loka birgðatímabili</span><span class="sxs-lookup"><span data-stu-id="ac20a-127">To close an inventory period</span></span>  
1. <span data-ttu-id="ac20a-128">Áður en birgðatímabili er lokað er keyrslan **Leiðr. kostnað - Birgðafærslur** keyrð til að tryggja það að allar kostnaðarleiðréttingar séu bókaðar.</span><span class="sxs-lookup"><span data-stu-id="ac20a-128">Before closing an inventory period, run the **Adjust Cost – Item Entries** batch job to ensure that all cost adjustments are posted.</span></span> <span data-ttu-id="ac20a-129">Í flipanum **Aðgerðir** í flokknum **Eiginleikar** veljið **Leiðrétta kostnað - Birgðafærslur**.</span><span class="sxs-lookup"><span data-stu-id="ac20a-129">On the **Actions** tab, in the **Functions** group, choose **Adjust Cost – Item Entries**.</span></span>  

     <span data-ttu-id="ac20a-130">Keyrð er skýrslan **Loka birgðatímabili - Prófun** til að ákvarða hvort einhverjar opnar birgðafærslur á útleið eru innan birgðatímabilsins eða einhverjar vörur sem ekki hafa fengið kostnað sinn leiðréttan.</span><span class="sxs-lookup"><span data-stu-id="ac20a-130">Run the **Close Inventory Period – Test** report to determine if there are any open outbound item entries within the inventory period or any items whose cost has not yet been adjusted.</span></span>  
2. <span data-ttu-id="ac20a-131">Velja skal **Loka birgðatímabili - Prófun** aðgerðina.</span><span class="sxs-lookup"><span data-stu-id="ac20a-131">Choose the **Close Inventory Period – Test** action.</span></span>  

     <span data-ttu-id="ac20a-132">Keyrð er keyrslan **Bóka birgðabreytingar** til að tryggja það að allur kostnaður sé bókaður í fjárhaginn.</span><span class="sxs-lookup"><span data-stu-id="ac20a-132">Run the **Post Inventory Cost to G/L** batch job to ensure that all costs are posted to the general ledger.</span></span>  
3. <span data-ttu-id="ac20a-133">Velja skal aðgerðina **Bóka birgðir í fjárhag**.</span><span class="sxs-lookup"><span data-stu-id="ac20a-133">Choose the **Post Inventory to G/L** action.</span></span>  
4. <span data-ttu-id="ac20a-134">Í glugganum **Birgðatímabil** skal velja birgðatímabilið sem á að loka.</span><span class="sxs-lookup"><span data-stu-id="ac20a-134">In the **Inventory Periods** window, select the inventory period you want to close.</span></span>  
5. <span data-ttu-id="ac20a-135">Velja aðgerðina **Loka tímabili**.</span><span class="sxs-lookup"><span data-stu-id="ac20a-135">Choose the **Close Period** action.</span></span> <span data-ttu-id="ac20a-136">Þegar birgðatímabilinu hafi verið lokað er ekki hægt að bóka breytingar á birgðum fyrir lokadagsetninguna.</span><span class="sxs-lookup"><span data-stu-id="ac20a-136">After the inventory period has been closed, you cannot post inventory changes before the ending date.</span></span> <span data-ttu-id="ac20a-137">Leiðrétta þarf kostnað allra vara með keyrslunni **Leiðr. kostnað - Birgðafærslur** áður en birgðatímabilinu er lokað.</span><span class="sxs-lookup"><span data-stu-id="ac20a-137">The cost of all items must be adjusted with the **Adjust Cost – Item Entries** batch job before you close the inventory period.</span></span>  
6. <span data-ttu-id="ac20a-138">Veldu hnappinn **Já** til að staðfesta það að ætlunin sé að loka tímabilinu, eða veldu **Nei** til að hætta við lokunina.</span><span class="sxs-lookup"><span data-stu-id="ac20a-138">Choose the **Yes** button to confirm that you want to close the period, or choose **No** to cancel the closing.</span></span>  
7. <span data-ttu-id="ac20a-139">Kerfið lokar birgðatímabilinu og sýnir staðfestingarskilaboð þegar því er lokið.</span><span class="sxs-lookup"><span data-stu-id="ac20a-139">The inventory period is closed and a confirmation message is displayed when it is finished.</span></span>  

## <a name="reopening-inventory-periods"></a><span data-ttu-id="ac20a-140">Enduropnun birgðatímabila</span><span class="sxs-lookup"><span data-stu-id="ac20a-140">Reopening Inventory Periods</span></span>  
<span data-ttu-id="ac20a-141">Þegar birgðatímabili hefur verið lokað er ekki hægt að eyða birgðatímabilinu.</span><span class="sxs-lookup"><span data-stu-id="ac20a-141">After you have closed the inventory period, you cannot delete the inventory period.</span></span> <span data-ttu-id="ac20a-142">Hægt er hins vegar að enduropna það til að leyfa bókun áður en að lokadagsetningu birgðatímabilsins er komið.</span><span class="sxs-lookup"><span data-stu-id="ac20a-142">You can, however, reopen it, if you would like to allow posting before the ending date of the inventory period.</span></span> <span data-ttu-id="ac20a-143">Enduropnun tímabils enduropnar líka öll birgðatímabil með lokadagsetningar seinni en það tímabil sem er enduropnað.</span><span class="sxs-lookup"><span data-stu-id="ac20a-143">Reopening a period also reopens all inventory periods with ending dates later than the period you reopen.</span></span>  

### <a name="to-reopen-an-inventory-period"></a><span data-ttu-id="ac20a-144">Til að enduropna birgðatímabil</span><span class="sxs-lookup"><span data-stu-id="ac20a-144">To reopen an inventory period</span></span>  
1. <span data-ttu-id="ac20a-145">Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Birgðatímabil** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="ac20a-145">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Inventory Periods**, and then choose the related link.</span></span>  
2. <span data-ttu-id="ac20a-146">Velja skal birgðatímabilið sem á að enduropna.</span><span class="sxs-lookup"><span data-stu-id="ac20a-146">Select the inventory period you want to reopen.</span></span>  
3. <span data-ttu-id="ac20a-147">Velja aðgerðina **Enduropna tímabili**.</span><span class="sxs-lookup"><span data-stu-id="ac20a-147">Choose the **Reopen Period** period action.</span></span> <span data-ttu-id="ac20a-148">Staðfesta að það eigi að enduropna tímabilið.</span><span class="sxs-lookup"><span data-stu-id="ac20a-148">Confirm that you want to reopen the period.</span></span>  
4. <span data-ttu-id="ac20a-149">Allir birgðahaldstímar með lokadagsetningu sem kemur síðar en valið tímabilið eru enduropnaðir.</span><span class="sxs-lookup"><span data-stu-id="ac20a-149">All inventory periods with ending dates later than the period you selected are reopened.</span></span>  

## <a name="see-also"></a><span data-ttu-id="ac20a-150">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="ac20a-150">See Also</span></span>  
[<span data-ttu-id="ac20a-151">Hönnunarupplýsingar: birgðahaldstími</span><span class="sxs-lookup"><span data-stu-id="ac20a-151">Design Details: Inventory Periods</span></span>](design-details-inventory-periods.md)  
[<span data-ttu-id="ac20a-152">Fjármál</span><span class="sxs-lookup"><span data-stu-id="ac20a-152">Finance</span></span>](finance.md)  
[<span data-ttu-id="ac20a-153">Birgðir</span><span class="sxs-lookup"><span data-stu-id="ac20a-153">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="ac20a-154">Unnið með Financials</span><span class="sxs-lookup"><span data-stu-id="ac20a-154">Working with Financials</span></span>](ui-work-product.md)

