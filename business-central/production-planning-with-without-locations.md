---
title: "Áætlanagerð með eða án birgðageymslna | Microsoft Docs"
description: "Mikilvægt er að skilja áætlanir með eða án birgðageymslukóta í eftirspurnarlínum."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/04/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: a2043b50e9f398839034c87e8f0fb42f68d8c036
ms.contentlocale: is-is
ms.lasthandoff: 03/22/2018

---
# <a name="planning-with-or-without-locations"></a><span data-ttu-id="35c96-103">Áætlanagerð með eða án birgðageymslna</span><span class="sxs-lookup"><span data-stu-id="35c96-103">Planning With or Without Locations</span></span>
<span data-ttu-id="35c96-104">Varðandi áætlanir með eða án birgðageymslukóta í eftirspurnarlínum vinnur áætlanakerfið á einfaldan hátt þegar:</span><span class="sxs-lookup"><span data-stu-id="35c96-104">Concerning planning with or without location codes on demand lines, the planning system operates in a straight forward way when:</span></span>  

-   <span data-ttu-id="35c96-105">eftirspurnarlínur eru alltaf með birgðageymslukóta og kerfið notar birgðahaldseiningar til fulls með viðeigandi birgðageymsluuppsetningu.</span><span class="sxs-lookup"><span data-stu-id="35c96-105">demand lines always carry location codes and the system fully uses stockkeeping units, including the relevant location setup.</span></span>  
-   <span data-ttu-id="35c96-106">eftirspurnarlínur eru aldrei með birgðageymslukóta og kerfið notar ekki birgðahaldseiningar eða neina birgðageymsluuppsetningu (sjá síðasta dæmið hér fyrir neðan).</span><span class="sxs-lookup"><span data-stu-id="35c96-106">demand lines never carry location codes and the system does not use SKUs or any location setup (see last scenario below).</span></span>  

<span data-ttu-id="35c96-107">Ef hins vegar eftirspurnarlínur eru stundum með birgðageymslukóta og stundum ekki fer áætlanakerfið eftir tilteknum reglum í samræmi við uppsetningu.</span><span class="sxs-lookup"><span data-stu-id="35c96-107">However, if demand lines sometimes have location codes and other times do not, the planning system will follow certain rules depending on setup.</span></span>  

## <a name="demand-at-location"></a><span data-ttu-id="35c96-108">Eftirspurn í birgðageymslu</span><span class="sxs-lookup"><span data-stu-id="35c96-108">Demand at Location</span></span>  
<span data-ttu-id="35c96-109">Þegar áætlunarkerfið greinir eftirspurn í birgðageymslu (línu með birgðageymslukóta) vinnar það á mismunandi hátt í samræmi við 3 mikilvæg uppsetningargildi.</span><span class="sxs-lookup"><span data-stu-id="35c96-109">When the planning system detects demand at a location (a line with a location code), it will behave in different ways depending on 3 critical setup values.</span></span>  

<span data-ttu-id="35c96-110">Í áætlunarkeyrslu leitar kerfið að 3 uppsetningargildum í röð og áætlar samkvæmt þeim:</span><span class="sxs-lookup"><span data-stu-id="35c96-110">During a planning run, the system checks for the 3 setup values in sequence and plans accordingly:</span></span>  

1.  <span data-ttu-id="35c96-111">Er gátmerki í reitnum **Birgðageymsla áskilin**?</span><span class="sxs-lookup"><span data-stu-id="35c96-111">Is there a check mark in the **Location Mandatory** field?</span></span>  

    <span data-ttu-id="35c96-112">Ef já:</span><span class="sxs-lookup"><span data-stu-id="35c96-112">If yes, then:</span></span>  

2.  <span data-ttu-id="35c96-113">Er birgðahaldseining til fyrir vöruna?</span><span class="sxs-lookup"><span data-stu-id="35c96-113">Does SKU exist for the item?</span></span>  

    <span data-ttu-id="35c96-114">Ef já:</span><span class="sxs-lookup"><span data-stu-id="35c96-114">If yes, then:</span></span>  

    <span data-ttu-id="35c96-115">Vörunni er áætlað samkvæmt áætlunarfæribreytum á birgðahaldseiningaspjaldinu.</span><span class="sxs-lookup"><span data-stu-id="35c96-115">The item is planned according to planning parameters on the SKU card.</span></span>  

    <span data-ttu-id="35c96-116">Ef nei:</span><span class="sxs-lookup"><span data-stu-id="35c96-116">If no, then:</span></span>  

3.  <span data-ttu-id="35c96-117">Er reiturinn **Íhlutir á staðnum** með áskildum birgðageymslukóta?</span><span class="sxs-lookup"><span data-stu-id="35c96-117">Does the **Components at Location** field contain the demanded location code?</span></span>  

    <span data-ttu-id="35c96-118">Ef já:</span><span class="sxs-lookup"><span data-stu-id="35c96-118">If yes, then:</span></span>  

    <span data-ttu-id="35c96-119">Vörunni er áætlað samkvæmt áætlunarfæribreytum á birgðaspjaldinu.</span><span class="sxs-lookup"><span data-stu-id="35c96-119">The item is planned according to planning parameters on the item card.</span></span>  

    <span data-ttu-id="35c96-120">Ef nei:</span><span class="sxs-lookup"><span data-stu-id="35c96-120">If no, then:</span></span>  

    <span data-ttu-id="35c96-121">Vörunni er áætlað samkvæmt: Endurpöntunarstefna =  *Lota-fyrir-lotu* , Taka með birgðir =  *Já*, allar aðrar áætlunarfæribreytur = tómar.</span><span class="sxs-lookup"><span data-stu-id="35c96-121">The item is planned according to: Reordering Policy =  *Lot-for-Lot*, Include Inventory =  *Yes*, all other planning parameters = Empty.</span></span> <span data-ttu-id="35c96-122">(Vörur sem nota endurpöntunarstefnuna  *Pöntun* nota  *Pöntun* ásamt öðrum stillingum).</span><span class="sxs-lookup"><span data-stu-id="35c96-122">(Items using reordering policy  *Order* remain using  *Order* as well as the other settings.)</span></span>  

> [!NOTE]  
>  <span data-ttu-id="35c96-123">Þessi lágmarksvalkostur nær aðeins yfir nákvæma eftirspurn.</span><span class="sxs-lookup"><span data-stu-id="35c96-123">This minimal alternative only covers the exact demand.</span></span> <span data-ttu-id="35c96-124">Allar skilgreindar áætlunarfæribreytur eru hunsaðar.</span><span class="sxs-lookup"><span data-stu-id="35c96-124">Any planning parameters defined are ignored.</span></span>  

<span data-ttu-id="35c96-125">Sjá frávik í dæmunum hér fyrir neðan.</span><span class="sxs-lookup"><span data-stu-id="35c96-125">See variations in the scenarios below.</span></span>  

## <a name="demand-at-blank-location"></a><span data-ttu-id="35c96-126">Eftirspurn í "Tómri birgðageymslu"</span><span class="sxs-lookup"><span data-stu-id="35c96-126">Demand at "Blank Location"</span></span>  
<span data-ttu-id="35c96-127">Jafnvel þó merkt sé við reitinn **Birgðageymsla áskilin** er heimilt að stofna línur í kerfinu án birgðageymslukóta – einnig kallað *TÓM* birgðageymsla.</span><span class="sxs-lookup"><span data-stu-id="35c96-127">Even if the **Location Mandatory** check box is selected, the system will allow demand lines to be created without a location code – also referred to as *BLANK* location.</span></span> <span data-ttu-id="35c96-128">Þetta er frávik í kerfinu því það er með mismunandi uppsetningargildi sem stillt eru á að vinna með birgðageymslur (sjá ofangreint) og niðurstaðan verður sú að áætlunarkerfið stofnar ekki áætlunarlínu fyrir svona eftirspurnarlínu.</span><span class="sxs-lookup"><span data-stu-id="35c96-128">This is a deviation for the system because it has various setup values tuned to dealing with locations (see above) and as a result, the planning engine will not create a planning line for such a demand line.</span></span> <span data-ttu-id="35c96-129">Ef ekki er merkt við reitinn **Birgðageymsla áskilin** en einhver af uppsetningargildum birgðageymsla eru til er það einnig talið vera frávik og eftirspurnarkerfið bregst við með því að leggja til „lágmarksvalkostinn“:</span><span class="sxs-lookup"><span data-stu-id="35c96-129">If the **Location Mandatory** field is not selected but any of the location setup values exist, then that is also considered a deviation and the planning system will react by outputting the "minimal alternative":</span></span>   
<span data-ttu-id="35c96-130">Vörunni er áætlað samkvæmt: Endurpöntunarstefna =  *Lota-fyrir-lotu* ( *Pöntun* er áfram *Pöntun)*, Taka með birgðir =  *Já*, allar aðrar áætlunarfæribreytur = Auðar.</span><span class="sxs-lookup"><span data-stu-id="35c96-130">The item is planned according to: Reordering Policy =  *Lot-for-Lot* ( *Order* remains *Order)*, Include Inventory =  *Yes*, all other planning parameters = Empty.</span></span>  

<span data-ttu-id="35c96-131">Sjá frávik í uppsetningardæmunum hér fyrir neðan.</span><span class="sxs-lookup"><span data-stu-id="35c96-131">See variations in the setup scenarios below.</span></span>  

### <a name="setup-1"></a><span data-ttu-id="35c96-132">Uppsetning 1:</span><span class="sxs-lookup"><span data-stu-id="35c96-132">Setup 1:</span></span>  

-   <span data-ttu-id="35c96-133">Birgðageymsla áskilin = *Já*</span><span class="sxs-lookup"><span data-stu-id="35c96-133">Location Mandatory = *Yes*</span></span>  
-   <span data-ttu-id="35c96-134">Birgðahaldseining er sett upp fyrir  *RAUTT*</span><span class="sxs-lookup"><span data-stu-id="35c96-134">SKU is set up for  *RED*</span></span>  
-   <span data-ttu-id="35c96-135">Íhlutir á staðnum =  *BLÁTT*</span><span class="sxs-lookup"><span data-stu-id="35c96-135">Component at Location =  *BLUE*</span></span>  

#### <a name="case-11-demand-is-at--red-location"></a><span data-ttu-id="35c96-136">Dæmi 1.1: Eftirspurn er í birgðageymslunni  *RAUTT*</span><span class="sxs-lookup"><span data-stu-id="35c96-136">Case 1.1: Demand is at  *RED* location</span></span>  

<span data-ttu-id="35c96-137">Vörunni er áætlað samkvæmt áætlunarfæribreytum á birgðahaldseiningaspjaldinu (að hugsanlegri millifærslu meðtalinni).</span><span class="sxs-lookup"><span data-stu-id="35c96-137">The item is planned according to planning parameters on the SKU card (including possible transfer).</span></span>  

#### <a name="case-12-demand-is-at--blue-location"></a><span data-ttu-id="35c96-138">Dæmi 1.2: Eftirspurn er í birgðageymslunni  *RAUTT*</span><span class="sxs-lookup"><span data-stu-id="35c96-138">Case 1.2: Demand is at  *BLUE* location</span></span>  

<span data-ttu-id="35c96-139">Vörunni er áætlað samkvæmt áætlunarfæribreytum á birgðaspjaldinu.</span><span class="sxs-lookup"><span data-stu-id="35c96-139">The item is planned according to planning parameters on the item card.</span></span>  

#### <a name="case-13-demand-is-at--green-location"></a><span data-ttu-id="35c96-140">Dæmi 1.3: Eftirspurn er í birgðageymslunni  *GRÆNT*</span><span class="sxs-lookup"><span data-stu-id="35c96-140">Case 1.3: Demand is at  *GREEN* location</span></span>  

<span data-ttu-id="35c96-141">Vörunni er áætlað samkvæmt: Endurpöntunarstefna =  *Lota-fyrir-lotu* ( *Pöntun* er áfram  *Pöntun*), Taka með birgðir =  *Já*, allar aðrar áætlunarfæribreytur = tómar.</span><span class="sxs-lookup"><span data-stu-id="35c96-141">The item is planned according to: Reordering Policy =  *Lot-for-Lot* ( *Order* remains  *Order*), Include Inventory =  *Yes*, all other planning parameters = Empty.</span></span>  

#### <a name="case-14-demand-is-at--blank-location"></a><span data-ttu-id="35c96-142">Dæmi 1.4: Eftirspurn er í birgðageymslunni  *TÓMT*</span><span class="sxs-lookup"><span data-stu-id="35c96-142">Case 1.4: Demand is at  *BLANK* location</span></span>  

<span data-ttu-id="35c96-143">Vörunni er ekki áætlað þar sem engin birgðageymsla er skilgreind í eftirspurnarlínunni.</span><span class="sxs-lookup"><span data-stu-id="35c96-143">The item is not planned because no location is defined on the demand line.</span></span>  

### <a name="setup-2"></a><span data-ttu-id="35c96-144">Uppsetning 2:</span><span class="sxs-lookup"><span data-stu-id="35c96-144">Setup 2:</span></span>  

-   <span data-ttu-id="35c96-145">Birgðageymsla áskilin = *Já*</span><span class="sxs-lookup"><span data-stu-id="35c96-145">Location Mandatory = *Yes*</span></span>  
-   <span data-ttu-id="35c96-146">Engin birgðahaldseining er til</span><span class="sxs-lookup"><span data-stu-id="35c96-146">No SKU exists</span></span>  
-   <span data-ttu-id="35c96-147">Íhlutir á staðnum =  *BLÁTT*</span><span class="sxs-lookup"><span data-stu-id="35c96-147">Component at Location =  *BLUE*</span></span>  

#### <a name="case-21-demand-is-at--red-location"></a><span data-ttu-id="35c96-148">Dæmi 2.1: Eftirspurn er í birgðageymslunni  *RAUTT*</span><span class="sxs-lookup"><span data-stu-id="35c96-148">Case 2.1: Demand is at  *RED* location</span></span>  

<span data-ttu-id="35c96-149">Vörunni er áætlað samkvæmt: Endurpöntunarstefna =  *Lota-fyrir-lotu* ( *Pöntun* er áfram  *Pöntun*), Taka með birgðir =  *Já*, allar aðrar áætlunarfæribreytur = tómar.</span><span class="sxs-lookup"><span data-stu-id="35c96-149">The item is planned according to: Reordering Policy =  *Lot-for-Lot* ( *Order* remains  *Order*), Include Inventory =  *Yes*, all other planning parameters = Empty.</span></span>  

#### <a name="case-22-demand-is-at--blue-location"></a><span data-ttu-id="35c96-150">Dæmi 2.2: Eftirspurn er í birgðageymslunni  *RAUTT*</span><span class="sxs-lookup"><span data-stu-id="35c96-150">Case 2.2: Demand is at  *BLUE* location</span></span>  

<span data-ttu-id="35c96-151">Vörunni er áætlað samkvæmt áætlunarfæribreytum á birgðaspjaldinu.</span><span class="sxs-lookup"><span data-stu-id="35c96-151">The item is planned according to planning parameters on the item card.</span></span>  

### <a name="setup-3"></a><span data-ttu-id="35c96-152">Uppsetning 3:</span><span class="sxs-lookup"><span data-stu-id="35c96-152">Setup 3:</span></span>  

-   <span data-ttu-id="35c96-153">Birgðageymsla áskilin = *Nei*</span><span class="sxs-lookup"><span data-stu-id="35c96-153">Location Mandatory = *No*</span></span>  
-   <span data-ttu-id="35c96-154">Engin birgðahaldseining er til</span><span class="sxs-lookup"><span data-stu-id="35c96-154">No SKU exists</span></span>  
-   <span data-ttu-id="35c96-155">Íhlutir á staðnum =  *BLÁTT*</span><span class="sxs-lookup"><span data-stu-id="35c96-155">Component at Location =  *BLUE*</span></span>  

#### <a name="case-31-demand-is-at--red-location"></a><span data-ttu-id="35c96-156">Dæmi 3.1: Eftirspurn er í birgðageymslunni  *RAUTT*</span><span class="sxs-lookup"><span data-stu-id="35c96-156">Case 3.1: Demand is at  *RED* location</span></span>  

<span data-ttu-id="35c96-157">Vörunni er áætlað samkvæmt: Endurpöntunarstefna =  *Lota-fyrir-lotu* ( *Pöntun* er áfram  *Pöntun*), Taka með birgðir =  *Já*, allar aðrar áætlunarfæribreytur = tómar.</span><span class="sxs-lookup"><span data-stu-id="35c96-157">The item is planned according to: Reordering Policy =  *Lot-for-Lot* ( *Order* remains  *Order*), Include Inventory =  *Yes*, all other planning parameters = Empty.</span></span>  

#### <a name="case-32-demand-is-at--blue-location"></a><span data-ttu-id="35c96-158">Dæmi 3.2: Eftirspurn er í birgðageymslunni  *RAUTT*</span><span class="sxs-lookup"><span data-stu-id="35c96-158">Case 3.2: Demand is at  *BLUE* location</span></span>  

<span data-ttu-id="35c96-159">Vörunni er áætlað samkvæmt áætlunarfæribreytum á birgðaspjaldinu.</span><span class="sxs-lookup"><span data-stu-id="35c96-159">The item is planned according to planning parameters on the item card.</span></span>  

#### <a name="case-33-demand-is-at--blank-location"></a><span data-ttu-id="35c96-160">Dæmi 3.3: Eftirspurn er í birgðageymslunni  *TÓMT*</span><span class="sxs-lookup"><span data-stu-id="35c96-160">Case 3.3: Demand is at  *BLANK* location</span></span>  

<span data-ttu-id="35c96-161">Vörunni er áætlað samkvæmt: Endurpöntunarstefna =  *Lota-fyrir-lotu* ( *Pöntun* er áfram  *Pöntun*), Taka með birgðir =  *Já*, allar aðrar áætlunarfæribreytur = tómar.</span><span class="sxs-lookup"><span data-stu-id="35c96-161">The item is planned according to: Reordering Policy =  *Lot-for-Lot* ( *Order* remains  *Order*), Include Inventory =  *Yes*, all other planning parameters = Empty.</span></span>  

### <a name="setup-4"></a><span data-ttu-id="35c96-162">Uppsetning 4:</span><span class="sxs-lookup"><span data-stu-id="35c96-162">Setup 4:</span></span>  

-   <span data-ttu-id="35c96-163">Birgðageymsla áskilin = *Nei*</span><span class="sxs-lookup"><span data-stu-id="35c96-163">Location Mandatory = *No*</span></span>  
-   <span data-ttu-id="35c96-164">Engin birgðahaldseining er til</span><span class="sxs-lookup"><span data-stu-id="35c96-164">No SKU exists</span></span>  
-   <span data-ttu-id="35c96-165">Íhlutir á staðnum =  *TÓMT*</span><span class="sxs-lookup"><span data-stu-id="35c96-165">Component at Location =  *BLANK*</span></span>  

#### <a name="case-41-demand-is-at--blue-location"></a><span data-ttu-id="35c96-166">Dæmi 4.1: Eftirspurn er í birgðageymslunni  *BLÁTT*</span><span class="sxs-lookup"><span data-stu-id="35c96-166">Case 4.1: Demand is at  *BLUE* location</span></span>  

<span data-ttu-id="35c96-167">Vörunni er áætlað samkvæmt: Endurpöntunarstefna =  *Lota-fyrir-lotu* ( *Pöntun* er áfram  *Pöntun*), Taka með birgðir =  *Já*, allar aðrar áætlunarfæribreytur = tómar.</span><span class="sxs-lookup"><span data-stu-id="35c96-167">The item is planned according to: Reordering Policy =  *Lot-for-Lot* ( *Order* remains  *Order*), Include Inventory =  *Yes*, all other planning parameters = Empty.</span></span>  

#### <a name="case-42-demand-is-at--blank-location"></a><span data-ttu-id="35c96-168">Dæmi 4.2: Eftirspurn er í birgðageymslunni  *TÓMT*</span><span class="sxs-lookup"><span data-stu-id="35c96-168">Case 4.2: Demand is at  *BLANK* location</span></span>  

<span data-ttu-id="35c96-169">Varan er áætluð í samræmi við áætlunarfæribreytur á birgðaspjaldinu.</span><span class="sxs-lookup"><span data-stu-id="35c96-169">The item is planned according to planning parameters on the item card.</span></span>  

<span data-ttu-id="35c96-170">Eins og sjá má á síðasta dæmi er eina leiðin til að fá réttar niðurstöður fyrir eftirspurnarlínu án birgðageymslukóta sú að gera öll uppsetningargildi sem tengjast birgðageymslum óvirk.</span><span class="sxs-lookup"><span data-stu-id="35c96-170">As you can see from the last scenario, the only way to get a correct result for a demand line without a location code is to disable all setup values relating to locations.</span></span> <span data-ttu-id="35c96-171">Sömuleiðis er eina leiðin til að fá stöðugar áætlunarniðurstöður fyrir eftirspurn í birgðageymslum sú að nota birgðahaldseiningar.</span><span class="sxs-lookup"><span data-stu-id="35c96-171">Similarly, the only way to get stable planning results for demand at locations is to use stockkeeping units.</span></span>  

<span data-ttu-id="35c96-172">Ef þörf í birgðageymslum er áætluð oft er eindregið mælt með að nota birgðahaldseiningaaðgerðina.</span><span class="sxs-lookup"><span data-stu-id="35c96-172">Therefore, if you often plan for demand at locations, it is strongly advised to use the Stockkeeping Units feature.</span></span>  

## <a name="see-also"></a><span data-ttu-id="35c96-173">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="35c96-173">See Also</span></span>
<span data-ttu-id="35c96-174">[Áætlun](production-planning.md)  </span><span class="sxs-lookup"><span data-stu-id="35c96-174">[Planning](production-planning.md)  </span></span>  
[<span data-ttu-id="35c96-175">Uppsetning framleiðslu</span><span class="sxs-lookup"><span data-stu-id="35c96-175">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="35c96-176">[Framleiðsla](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="35c96-176">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
[<span data-ttu-id="35c96-177">Birgðir</span><span class="sxs-lookup"><span data-stu-id="35c96-177">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="35c96-178">Innkaup</span><span class="sxs-lookup"><span data-stu-id="35c96-178">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="35c96-179">[Hönnunarupplýsingar: framboðsáætlun](design-details-supply-planning.md) </span><span class="sxs-lookup"><span data-stu-id="35c96-179">[Design Details: Supply Planning](design-details-supply-planning.md) </span></span>  
[<span data-ttu-id="35c96-180">Uppsetning bestu venja: Framboðsáætlun</span><span class="sxs-lookup"><span data-stu-id="35c96-180">Setup Best Practices: Supply Planning</span></span>](setup-best-practices-supply-planning.md)  
<span data-ttu-id="35c96-181">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="35c96-181">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

