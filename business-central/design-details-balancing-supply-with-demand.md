---
title: Hönnunarupplýsingar - Jöfnun framboðs og eftirspurnar | Microsoft Docs
description: Kjarni áætlanakerfisins felst í jafnvægi á milli eftirspurn og framboð með því að leggja til notandaaðgerðir til að endurskoða framboðspantanir við ójafnvægi. Þetta á sér stað á blöndu af afbrigði og staðsetningu.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
redirect_url: design-details-balancing-demand-and-supply
ms.openlocfilehash: 1bef0ad2a94e64ecf95614707b6746e6a381fcb0
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/01/2019
ms.locfileid: "2307397"
---
# <a name="design-details-balancing-supply-with-demand"></a><span data-ttu-id="f6470-104">Hönnunarupplýsingar: jöfnun framboðs og eftirspurnar</span><span class="sxs-lookup"><span data-stu-id="f6470-104">Design Details: Balancing Supply with Demand</span></span>
<span data-ttu-id="f6470-105">Kjarni áætlanakerfisins felst í jafnvægi á milli eftirspurn og framboð með því að leggja til notandaaðgerðir til að endurskoða framboðspantanir við ójafnvægi.</span><span class="sxs-lookup"><span data-stu-id="f6470-105">The core of the planning system involves balancing demand and supply by means of suggesting user actions to revise the supply orders in case of imbalance.</span></span> <span data-ttu-id="f6470-106">Þetta á sér stað á blöndu af afbrigði og staðsetningu.</span><span class="sxs-lookup"><span data-stu-id="f6470-106">This takes place per combination of variant and location.</span></span>  

<span data-ttu-id="f6470-107">Ímyndaðu þér að hver birgðaforstilling inniheldur eftirspurnartilvika (raðað eftir dagsetningu og forgangi) og samsvarandi streng á framboðstilvikum.</span><span class="sxs-lookup"><span data-stu-id="f6470-107">Imagine that each inventory profile contains a string of demand events (sorted by date and priority) and a corresponding string of supply events.</span></span> <span data-ttu-id="f6470-108">Hver atburður vísar aftur til upphaflega gerðar þeirra og auðkennis.</span><span class="sxs-lookup"><span data-stu-id="f6470-108">Each event refers back to its source type and identification.</span></span> <span data-ttu-id="f6470-109">Reglur um mótjöfnun vörunnar eru einfaldar.</span><span class="sxs-lookup"><span data-stu-id="f6470-109">The rules for counterbalancing the item are straightforward.</span></span> <span data-ttu-id="f6470-110">Fjögur tilvik af samsvörun framboðs og eftirspurnar getur komið fram hvenær sem er í ferlinu.</span><span class="sxs-lookup"><span data-stu-id="f6470-110">Four instances of matching demand and supply can occur at any point of time in the process:</span></span>  

1. <span data-ttu-id="f6470-111">Ekker framboð eða eftirspurn fyrir vöruna => áætluninni er lokið (eða hún á ekki að hefjast).</span><span class="sxs-lookup"><span data-stu-id="f6470-111">No demand or supply exists for the item => the planning has finished (or should not start).</span></span>  
2. <span data-ttu-id="f6470-112">Eftirspurn er til en ekkert framboð => framboð skal leggja til.</span><span class="sxs-lookup"><span data-stu-id="f6470-112">Demand exists but there is no supply => supply should be suggested.</span></span>  
3. <span data-ttu-id="f6470-113">Framboð er til en engin eftirspurn => hætta skal við framboð.</span><span class="sxs-lookup"><span data-stu-id="f6470-113">Supply exists but there is no demand for it => supply should be canceled.</span></span>  
4. <span data-ttu-id="f6470-114">Hvort tveggja eftirspurn og framboð er til => Spurningar skal spyrja og svara áður en hægt er að tryggja að eftirspurn sé mætt og að framboð sé nægt.</span><span class="sxs-lookup"><span data-stu-id="f6470-114">Both demand and supply exist => questions should be asked and answered before the system can ensure that demand will be met and supply is sufficient.</span></span>  

     <span data-ttu-id="f6470-115">Ef tímasetning framboðs hentar ekki er kannski hægt að enduráætla framboðið eins og hér segir:</span><span class="sxs-lookup"><span data-stu-id="f6470-115">If the timing of the supply is not suitable, perhaps the supply can be rescheduled as follows:</span></span>  

    1.  <span data-ttu-id="f6470-116">Ef framboð er sett á undan eftirspurn er kannski hægt að enduráætla framboðið út svo að birgðirnar séu eins litlar og hægt er.</span><span class="sxs-lookup"><span data-stu-id="f6470-116">If the supply is placed earlier than the demand, perhaps the supply can be rescheduled out so that inventory is as low as possible.</span></span>  
    2.  <span data-ttu-id="f6470-117">Ef framboð er sett á eftir eftirspurn er kannski hægt að enduráætla framboðið inn.</span><span class="sxs-lookup"><span data-stu-id="f6470-117">If the supply is placed later than the demand, perhaps the supply can be rescheduled in.</span></span> <span data-ttu-id="f6470-118">Annars leggur kerfið til nýtt framboð.</span><span class="sxs-lookup"><span data-stu-id="f6470-118">Otherwise, the system will suggest new supply.</span></span>  
    3.  <span data-ttu-id="f6470-119">Ef framboð svarar eftirspurn á þeim degi getur áætlanakerfið haldið áfram að kanna hvort framboðsmagnið svarar eftirspurn.</span><span class="sxs-lookup"><span data-stu-id="f6470-119">If the supply meets the demand on the date, the planning system can proceed to investigate whether the quantity of the supply can cover the demand.</span></span>  

     <span data-ttu-id="f6470-120">Þegar tímasetning er rétt er hægt að reikna viðeigandi magn sem leggja á til sem hér segir:</span><span class="sxs-lookup"><span data-stu-id="f6470-120">Once the timing is in place, the adequate quantity to be supplied can be calculated as follows:</span></span>  

    1.  <span data-ttu-id="f6470-121">Ef framboðsmagnið er minna en eftirspurn er mögulegt að hægt sé að auka framboðsmagnið (eða ekki, ef takmarkað af stefnu um hámarksmagn).</span><span class="sxs-lookup"><span data-stu-id="f6470-121">If the supply quantity is less than the demand, it is possible that the supply quantity could be increased (or not, if limited by a maximum quantity policy).</span></span>  
    2.  <span data-ttu-id="f6470-122">Ef framboðsmagnið er meira en eftirspurn er mögulegt að hægt sé að minnka framboðsmagnið (eða ekki, ef takmarkað af stefnu um lágmarksmagn).</span><span class="sxs-lookup"><span data-stu-id="f6470-122">If the supply quantity is greater than the demand, it is possible that the supply quantity can be decreased (or not, if limited by a minimum quantity policy).</span></span>  

     <span data-ttu-id="f6470-123">Á þessum tímapunkti er annað hvor af þessum tveimur aðstæðum til:</span><span class="sxs-lookup"><span data-stu-id="f6470-123">At this point, either of these two situations exists:</span></span>  

    1.  <span data-ttu-id="f6470-124">Núverandi eftirspurn er hægt að ná yfir, og þar af leiðandi hægt að loka og áætlanagerð fyrir næsta eftirspurn getur byrjað.</span><span class="sxs-lookup"><span data-stu-id="f6470-124">The current demand can be covered, in which case it can be closed and planning for the next demand can start.</span></span>  
    2.  <span data-ttu-id="f6470-125">Birgðir hafa náð hámarksgildi svo eitthvert eftirspurnarmagn er óvarið.</span><span class="sxs-lookup"><span data-stu-id="f6470-125">The supply has reached its maximum, leaving some of the demand quantity uncovered.</span></span> <span data-ttu-id="f6470-126">Í þessu tilviki er áætlanakerfi getur lokað núverandi framboð og halda áfram í næsta.</span><span class="sxs-lookup"><span data-stu-id="f6470-126">In this case, the planning system can close the current supply and proceed to the next one.</span></span>  

 <span data-ttu-id="f6470-127">Ferlið byrjar upp á nýtt með næstu eftirspurn og núverandi framboði, eða öfugt.</span><span class="sxs-lookup"><span data-stu-id="f6470-127">The procedure starts all over with the next demand and the current supply or vice versa.</span></span> <span data-ttu-id="f6470-128">Núverandi framboð gæti náð yfir þessa eftirspurn líka eða núverandi eftirspurn hefur ekki enn verið að fullu tryggðir.</span><span class="sxs-lookup"><span data-stu-id="f6470-128">The current supply might be able to cover this next demand as well, or the current demand has not yet been fully covered.</span></span>  

## <a name="rules-concerning-actions-for-supply-events"></a><span data-ttu-id="f6470-129">Reglur um aðgerðir fyrir framboðstilvik</span><span class="sxs-lookup"><span data-stu-id="f6470-129">Rules Concerning Actions for Supply Events</span></span>  
<span data-ttu-id="f6470-130">Þegar áætlanakerfið framkvæmir ofansækinn útreikninga þar sem birgðir verða að mæta eftirspurn er eftirspurnin tekin sem sjálfgefin, þ.e. er ekki undir stjórn áætlanakerfis.</span><span class="sxs-lookup"><span data-stu-id="f6470-130">When the planning system performs a top-down calculation in which supply must fulfill demand, the demand is taken as a given, that is, it lies outside the control of the planning system.</span></span> <span data-ttu-id="f6470-131">Hins vegar er hægt að stjórna framboðshliðinni.</span><span class="sxs-lookup"><span data-stu-id="f6470-131">However, the supply side can be managed.</span></span> <span data-ttu-id="f6470-132">Því mun áætlanakerfið stinga upp á að búnar séu til nýjar birgðapantanir, þær sem fyrir liggja séu enduráætlaðar og/eða pöntunarmagni sé breytt.</span><span class="sxs-lookup"><span data-stu-id="f6470-132">Therefore, the planning system will suggest creating new supply orders, rescheduling existing ones, and/or changing the order quantity.</span></span> <span data-ttu-id="f6470-133">Ef núverandi birgðapöntun verður óþörf leggur áætlanakerfið til að notandinn hætti við hana.</span><span class="sxs-lookup"><span data-stu-id="f6470-133">If an existing supply order becoming superfluous, the planning system will suggest that the user cancels it.</span></span>  

<span data-ttu-id="f6470-134">Ef notandinn vill útiloka núverandi birgðapöntun frá tillögum áætlanagerðar getur hann tekið fram að hún hafi engan sveigjanleika áætlunar (Sveigjanleiki áætlunar = Enginn).</span><span class="sxs-lookup"><span data-stu-id="f6470-134">If the user wants to exclude an existing supply order from the planning suggestions, he can state that it has no planning flexibility (Planning Flexibility = None).</span></span> <span data-ttu-id="f6470-135">Þá er umframframboð úr þeirri pöntun notað fyrir eftirspurn, án þess að stungið sé upp á neinni aðgerð.</span><span class="sxs-lookup"><span data-stu-id="f6470-135">Then, excess supply from that order will be used to cover demand, but no action will be suggested.</span></span>  

<span data-ttu-id="f6470-136">Almennt gildir að allt framboð hefur áætlunarsveigjanleika sem takmarkast af skilyrðum hverrar af leiðbeinandi aðgerðum.</span><span class="sxs-lookup"><span data-stu-id="f6470-136">In general, all supply has a planning flexibility that is limited by the conditions of each of the suggested actions.</span></span>  

-   <span data-ttu-id="f6470-137">**Endurtímasetja út**: Dagsetning núverandi framboðspöntunar er hægt að Endurtímasetja út til að mæta skiladegi, nema</span><span class="sxs-lookup"><span data-stu-id="f6470-137">**Reschedule Out**: The date of an existing supply order can be scheduled out to meet the demand due date unless:</span></span>  

    -   <span data-ttu-id="f6470-138">Taflan táknar birgðir (alltaf á degi núll).</span><span class="sxs-lookup"><span data-stu-id="f6470-138">It represents inventory (always on day zero).</span></span>  
    -   <span data-ttu-id="f6470-139">Það er með pöntun fyrir pöntun tengda við aðra eftirspurn.</span><span class="sxs-lookup"><span data-stu-id="f6470-139">It has an order-to-order linked to another demand.</span></span>  
    -   <span data-ttu-id="f6470-140">Hún liggur utan enduráætlunarsíðunnar sem skilgreind er með tímarammanum.</span><span class="sxs-lookup"><span data-stu-id="f6470-140">It lies outside the reschedule page defined by the time bucket.</span></span>  
    -   <span data-ttu-id="f6470-141">Hægt er að nota birgðir sem eru nær.</span><span class="sxs-lookup"><span data-stu-id="f6470-141">There is a closer supply that could be used.</span></span>  
    -   <span data-ttu-id="f6470-142">Á hinn bóginn kann notandinn að ákveða að enduráætla ekki vegna þess að:</span><span class="sxs-lookup"><span data-stu-id="f6470-142">On the other hand, the user may decide not to reschedule because:</span></span>  
    -   <span data-ttu-id="f6470-143">Birgðapöntunin hefur þegar verið tengd við aðra eftirspurn á fyrri dagsetningu</span><span class="sxs-lookup"><span data-stu-id="f6470-143">The supply order has already been tied to another demand on a previous date.</span></span>  
    -   <span data-ttu-id="f6470-144">Nauðsynleg enduráætlunagerð er svo minniháttar að notanda finnst hún óþörf.</span><span class="sxs-lookup"><span data-stu-id="f6470-144">The needed rescheduling is so minimal that the user finds it negligible.</span></span>  

-   <span data-ttu-id="f6470-145">**Endurtímasetja inn**: Dagsetning núverandi framboðspöntunar sem er hægt að gera tímaáætlun á, nema í eftirfarandi skilyrðum:</span><span class="sxs-lookup"><span data-stu-id="f6470-145">**Reschedule In**: The date of an existing supply order can be scheduled in, except in the following conditions:</span></span>  

    -   <span data-ttu-id="f6470-146">Það er beintengt við einhverja aðra eftirspurn.</span><span class="sxs-lookup"><span data-stu-id="f6470-146">It is linked directly to some other demand.</span></span>  
    -   <span data-ttu-id="f6470-147">Hún liggur utan enduráætlunarsíðunnar sem skilgreind er með tímarammanum.</span><span class="sxs-lookup"><span data-stu-id="f6470-147">It lies outside the reschedule page defined by the time bucket.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="f6470-148">Við áætlun vöru með endurpöntunarmarki, er alltaf hægt að áætla birgðapöntunina ef nauðsynlegt er.</span><span class="sxs-lookup"><span data-stu-id="f6470-148">When planning an item using a reorder point, the supply order can always be scheduled in if necessary.</span></span> <span data-ttu-id="f6470-149">Þetta er algengt í birgðapöntun sem er dagsett í framtíðinni sem eru ræstar af endurpöntunarmarki.</span><span class="sxs-lookup"><span data-stu-id="f6470-149">This is common in forward-scheduled supply orders triggered by a reorder point.</span></span>  

-   <span data-ttu-id="f6470-150">**Auka magn**: Magn núverandi framboðspöntunar má auka til að mæta eftirspurn nema framboð þess er tengt beint við eftirspurn með Pöntun fyrir pöntun tengil.</span><span class="sxs-lookup"><span data-stu-id="f6470-150">**Increase Quantity**: The quantity of an existing supply order can be increased to meet the demand unless the supply order is linked directly to a demand by an order-to-order link.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="f6470-151">Jafnvel þótt hægt sé að auka við birgðapöntunina getur það verið takmarkað vegna skilgreinds hámarks pöntunarmagns.</span><span class="sxs-lookup"><span data-stu-id="f6470-151">Even though it is possible to increase the supply order, it may be limited due to a defined maximum order quantity.</span></span>  

-   <span data-ttu-id="f6470-152">**Minnka Magn**: Núverandi birgðapöntun með afgang miðað við núverandi eftirspurn getur lækkað til að mæta eftirspurn.</span><span class="sxs-lookup"><span data-stu-id="f6470-152">**Decrease Quantity**: An existing supply order with a surplus compared to an existing demand can be decreased to meet the demand.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="f6470-153">Jafnvel þótt hægt væri að minnka magnið getur samt verið afgangur miðað við eftirspurnina vegna skilgreinds lágmarks pöntunarmagns við fjöldapantanir.</span><span class="sxs-lookup"><span data-stu-id="f6470-153">Even though the quantity could be decreased, there may still be some surplus compared to the demand due to a defined minimum order quantity or order multiple.</span></span>  

-   <span data-ttu-id="f6470-154">**Hætta**: Sem sérstök atvik af lækkun magnsaðgerð, er hægt að hætta við birgðapöntun ef það hefur verið lækkað niður í núll.</span><span class="sxs-lookup"><span data-stu-id="f6470-154">**Cancel**: As a special incident of the decrease quantity action, the supply order could be canceled if it has been decreased to zero.</span></span>  
-   <span data-ttu-id="f6470-155">**Nýtt**: Ef engin framboðspöntun er til staðar eða fyrirliggjandi pöntun er ekki hægt að breyta til að uppfylla nauðsynlegt magn á settum skiladegi er stungið upp á nýrri framboðspöntun.</span><span class="sxs-lookup"><span data-stu-id="f6470-155">**New**: If no supply order already exists, or an existing one cannot be changed to meet the necessary quantity on the demanded due date, a new supply order is suggested.</span></span>  

## <a name="determining-the-supply-quantity"></a><span data-ttu-id="f6470-156">Ákvarða framboðsmagn</span><span class="sxs-lookup"><span data-stu-id="f6470-156">Determining the Supply Quantity</span></span>  
<span data-ttu-id="f6470-157">Áætlunarfæribreytur sem tilgreindar voru af notanda stjórna áætluðu magni fyrir hverja framboðspöntun.</span><span class="sxs-lookup"><span data-stu-id="f6470-157">Planning parameters defined by the user control the suggested quantity of each supply order.</span></span>  

<span data-ttu-id="f6470-158">Þegar áætlanakerfið reiknar út magn fyrir nýja birgðapöntun eða breytingu á magni í fyrirliggjandi pöntun getur magn sem lagt er til verið annað en raunverulegt eftirspurn segir til um.</span><span class="sxs-lookup"><span data-stu-id="f6470-158">When the planning system calculates the quantity of a new supply order or the quantity change on an existing one, the suggested quantity may be different from what is actually demanded.</span></span>  

<span data-ttu-id="f6470-159">Ef hámarksbirgðir eða fast pöntunarmagn er valið er hægt að auka magnið sem lagt er til til að ná þessu fasta magni eða hámarksbirgðum.</span><span class="sxs-lookup"><span data-stu-id="f6470-159">If a maximum inventory or fixed order quantity are selected, the suggested quantity may be increased to meet that fixed quantity or the maximum inventory.</span></span> <span data-ttu-id="f6470-160">Ef endurpöntunarstefna notar endurpöntunarmark er hægt að auka magnið að minnsta kosti til að ná endurpöntunarmarkinu.</span><span class="sxs-lookup"><span data-stu-id="f6470-160">If a reordering policy uses a reorder point, the quantity may be increased at least to meet the reorder point.</span></span>  

 <span data-ttu-id="f6470-161">Hægt er að breyta ráðlögðu magni í þessari röð:</span><span class="sxs-lookup"><span data-stu-id="f6470-161">The suggested quantity may be modified in this sequence:</span></span>  

1. <span data-ttu-id="f6470-162">Niður að hámarki pöntunarmagns (ef einhverjar).</span><span class="sxs-lookup"><span data-stu-id="f6470-162">Down to the maximum order quantity (if any).</span></span>  
2. <span data-ttu-id="f6470-163">Upp að lágmarksmagni pöntunar.</span><span class="sxs-lookup"><span data-stu-id="f6470-163">Up to the minimum order quantity.</span></span>  
3. <span data-ttu-id="f6470-164">Upp til að mæta næsta margfeldi pöntunar.</span><span class="sxs-lookup"><span data-stu-id="f6470-164">Up to meet the nearest order multiple.</span></span> <span data-ttu-id="f6470-165">(Ef rangar stillingar eru notaðar er mögulega farið yfir hámarkspöntunarmagn.)</span><span class="sxs-lookup"><span data-stu-id="f6470-165">(In case of erroneous settings, this may violate the maximum order quantity.)</span></span>  

## <a name="order-tracking-links-during-planning"></a><span data-ttu-id="f6470-166">Pöntunarrakningatenglar í áætlun</span><span class="sxs-lookup"><span data-stu-id="f6470-166">Order Tracking Links during Planning</span></span>  
<span data-ttu-id="f6470-167">Varðandi pöntunarrakningu við áætlanagerð, það er mikilvægt að nefna að áætlanakerfi endurraðar kvikt stofnuðum pöntunarrakningartenglum fyrir samsetningarnar hlutur/afbrigði / Staðsetningu.</span><span class="sxs-lookup"><span data-stu-id="f6470-167">Concerning order tracking during planning, it is important to mention that the planning system rearranges the dynamically created order tracking links for the item/variant/location combinations.</span></span>  

<span data-ttu-id="f6470-168">Það eru tvær ástæður fyrir þessu:</span><span class="sxs-lookup"><span data-stu-id="f6470-168">There are two reasons for this:</span></span>  

-   <span data-ttu-id="f6470-169">Áætlanakerfið verður að geta réttlætt tillögur sínar, að allri eftirspurn hafi verið svarað og að engar birgðapantanir séu umfram þörf.</span><span class="sxs-lookup"><span data-stu-id="f6470-169">The planning system must be able to justify its suggestions; that all demand has been covered, and that no supply orders are superfluous.</span></span>  
-   <span data-ttu-id="f6470-170">Breytilegir pöntunarrakningartengla þarf að endurjafna reglulega.</span><span class="sxs-lookup"><span data-stu-id="f6470-170">Dynamically created order tracking links need to be rebalanced regularly.</span></span>  

<span data-ttu-id="f6470-171">Með tímanum myndast ójafnvægi í pöntunarrakningartenglum þar sem pöntunarrakningarnetinu er ekki endurraðað fyrr en eftirspurnar- eða framboðstilvikum er lokað í raun og veru.</span><span class="sxs-lookup"><span data-stu-id="f6470-171">Over time, dynamic order tracking links become out of balance since the entire order tracking network is not rearranged until a demand or supply event is actually closed.</span></span>  

<span data-ttu-id="f6470-172">Áður en framboð og eftirspurn er jafnað eyðir forritið öllum pöntunarrakningartenglum.</span><span class="sxs-lookup"><span data-stu-id="f6470-172">Before balancing supply by demand, application deletes all existing order tracking links.</span></span> <span data-ttu-id="f6470-173">Við afstemmingu, þegar eftirspurn eða framboð er lokað, er nýjum pöntunarrakningartenglum komið á milli framboðs og eftirspurnar.</span><span class="sxs-lookup"><span data-stu-id="f6470-173">Then during the balancing procedure, when a demand or supply event is closed, it establishes new order tracking links between the demand and supply.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="f6470-174">Jafnvel þótt vara sé ekki sett upp fyrir kvika pöntunarrakningi býr áætlunarkerfið til jafnaða pöntunarrakningartengla eins og útskýrt er hér að ofan.</span><span class="sxs-lookup"><span data-stu-id="f6470-174">Even if the item is not set up for dynamic order tracking, the planned system will create balanced order tracking links as explained above.</span></span>  

## <a name="see-also"></a><span data-ttu-id="f6470-175">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="f6470-175">See Also</span></span>  
<span data-ttu-id="f6470-176">[Hönnunarupplýsingar: Jöfnun eftirspurnar og framboðs](design-details-balancing-demand-and-supply.md) </span><span class="sxs-lookup"><span data-stu-id="f6470-176">[Design Details: Balancing Demand and Supply](design-details-balancing-demand-and-supply.md) </span></span>  
<span data-ttu-id="f6470-177">[Hönnunarupplýsingar: Miðlægar hugmyndir áætlanakerfis](design-details-central-concepts-of-the-planning-system.md) </span><span class="sxs-lookup"><span data-stu-id="f6470-177">[Design Details: Central Concepts of the Planning System](design-details-central-concepts-of-the-planning-system.md) </span></span>  
[<span data-ttu-id="f6470-178">Hönnunarupplýsingar: framboðsáætlun</span><span class="sxs-lookup"><span data-stu-id="f6470-178">Design Details: Supply Planning</span></span>](design-details-supply-planning.md)
