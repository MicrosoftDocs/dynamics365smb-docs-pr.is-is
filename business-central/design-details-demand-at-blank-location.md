---
title: Hönnunarupplýsingar - Eftirspurn og framboð | Microsoft Docs
description: Í þessu efnisatriði er fjallað um hugtakið Eftirspurn, sem er algengasta orðið notað yfir hvers konar vergri eftirspurn, svo sem sölupöntun og íhluti þarft frá framleiðslu röð.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, demand, supply, inventory, planning
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 4661104e32e648cc134b3ba0c3d44b5a8c6daca6
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/01/2020
ms.locfileid: "3911206"
---
# <a name="design-details-demand-at-blank-location"></a><span data-ttu-id="19f07-103">Hönnunarupplýsingar: Eftirspurn í birgðageymslunni Tómt</span><span class="sxs-lookup"><span data-stu-id="19f07-103">Design Details: Demand at Blank Location</span></span>
<span data-ttu-id="19f07-104">Þegar notandi býr til eftirspurnartilvik, svo sem sölupöntunarlínu gerir kerfið notandanum kleift að stundum tilgreina staðsetningarkóða og stundum ekki, það er, að nota auða staðsetningu.</span><span class="sxs-lookup"><span data-stu-id="19f07-104">When a user creates a demand event, such as a sales order line, the program allows the user to sometimes specify a location code and other times not, that is, use blank location.</span></span>

<span data-ttu-id="19f07-105">Varðandi áætlanir með eða án birgðageymslukóða vinnur áætlanakerfið á einfaldan hátt þegar:</span><span class="sxs-lookup"><span data-stu-id="19f07-105">For demand with or without location codes, the planning system operates in a straight forward way when:</span></span>

- <span data-ttu-id="19f07-106">Eftirspurnarlínur eru alltaf með staðsetningarkóða og kerfið notar birgðahaldseiningar til fulls með viðeigandi staðsetningaruppsetningu.</span><span class="sxs-lookup"><span data-stu-id="19f07-106">Demand lines always carry location codes and the system fully uses SKUs, including the relevant location setup.</span></span>
- <span data-ttu-id="19f07-107">Eftirspurnarlínur eru aldrei með birgðageymslukóða og kerfið notar ekki birgðahaldseiningar eða neina birgðageymsluuppsetningu (sjá síðasta dæmið hér fyrir neðan).</span><span class="sxs-lookup"><span data-stu-id="19f07-107">Demand lines never carry location codes, and the system does not use SKUs or any location setup (see the last scenario in the following section).</span></span>

<span data-ttu-id="19f07-108">Ef hins vegar eftirspurnaratvik eru stundum með birgðageymslukóða og stundum ekki fer áætlanakerfið eftir tilteknum reglum í samræmi við uppsetningu.</span><span class="sxs-lookup"><span data-stu-id="19f07-108">However, if demand events sometimes have location codes and other times do not, the planning system will follow certain rules depending on setup.</span></span>

## <a name="demand-at-location"></a><span data-ttu-id="19f07-109">Eftirspurn í birgðageymslu</span><span class="sxs-lookup"><span data-stu-id="19f07-109">Demand at Location</span></span>
<span data-ttu-id="19f07-110">Þegar áætlunarkerfið greinir eftirspurn á staðsetningu vinnur það á mismunandi hátt í samræmi við þrjú mikilvæg uppsetningargildi.</span><span class="sxs-lookup"><span data-stu-id="19f07-110">When the planning system detects demand at a location, it will behave in different ways depending on three critical setup values.</span></span> <span data-ttu-id="19f07-111">Í áætlunarkeyrslu leitar kerfið að 3 uppsetningargildum í röð og áætlar samkvæmt þeim:</span><span class="sxs-lookup"><span data-stu-id="19f07-111">During a planning run, the system checks for three setup values in sequence and plans accordingly.</span></span>

1. <span data-ttu-id="19f07-112">Er gátmerki í reitnum **Birgðageymsla áskilin** ?</span><span class="sxs-lookup"><span data-stu-id="19f07-112">Is there a check mark in the **Location Mandatory** field?</span></span>

    <span data-ttu-id="19f07-113">Ef já:</span><span class="sxs-lookup"><span data-stu-id="19f07-113">If yes, then:</span></span>

2. <span data-ttu-id="19f07-114">Er birgðahaldseining til fyrir vöruna?</span><span class="sxs-lookup"><span data-stu-id="19f07-114">Does SKU exist for the item?</span></span>

    <span data-ttu-id="19f07-115">Ef já:</span><span class="sxs-lookup"><span data-stu-id="19f07-115">If yes, then:</span></span>

    <span data-ttu-id="19f07-116">Vörunni er áætlað samkvæmt áætlunarfæribreytum á birgðahaldseiningaspjaldinu.</span><span class="sxs-lookup"><span data-stu-id="19f07-116">The item is planned according to planning parameters on the SKU card.</span></span>

    <span data-ttu-id="19f07-117">Ef nei:</span><span class="sxs-lookup"><span data-stu-id="19f07-117">If no, then:</span></span>

3. <span data-ttu-id="19f07-118">Er reiturinn Íhlutir á staðnum með áskildum birgðageymslukóta?</span><span class="sxs-lookup"><span data-stu-id="19f07-118">Does the Components at Location field contain the demanded location code?</span></span>

  <span data-ttu-id="19f07-119">Ef já:</span><span class="sxs-lookup"><span data-stu-id="19f07-119">If yes, then:</span></span>

  <span data-ttu-id="19f07-120">Vörunni er áætlað samkvæmt áætlunarfæribreytum á birgðaspjaldinu.</span><span class="sxs-lookup"><span data-stu-id="19f07-120">The item is planned according to planning parameters on the item card.</span></span>

  <span data-ttu-id="19f07-121">Ef nei:</span><span class="sxs-lookup"><span data-stu-id="19f07-121">If no, then:</span></span>

  <span data-ttu-id="19f07-122">Vörunni er áætlað samkvæmt: Endurpöntunarstefna = Lota-fyrir-lotu , Taka með birgðir = Já, allar aðrar áætlunarfæribreytur = tómar. Vörur sem nota endurpöntunarstefnuna Pöntun nota Pöntun ásamt öðrum stillingum.</span><span class="sxs-lookup"><span data-stu-id="19f07-122">The item is planned according to: Reordering Policy = Lot-for-Lot, Include Inventory = Yes, all other planning parameters = Empty, items using Reordering Policy = Order will remain using Order along with the other settings.</span></span>

> [!NOTE]
> <span data-ttu-id="19f07-123">Einstök áætlunaruppsetning sem er framleiðsla sem síðasta svörun í skrefi 3 hér að ofan er vitnað til í eftirfarandi sem „lágmarksvalkostur“.</span><span class="sxs-lookup"><span data-stu-id="19f07-123">The exceptional planning setup that is output as the last reaction in step 3 above is referred to in the following as the “minimal alternative”.</span></span> <span data-ttu-id="19f07-124">Þessi áætlunaruppsetning nær aðeins yfir nákvæma eftirspurn. Allar skilgreindar áætlunarfæribreytur eru hunsaðar.</span><span class="sxs-lookup"><span data-stu-id="19f07-124">This planning setup only covers the exact demand, and all other planning parameters are ignored.</span></span>

<span data-ttu-id="19f07-125">Upplýsingar um afbrigði af þessum áætlunarrökum eru í hlutanum Dæmi fyrir neðan.</span><span class="sxs-lookup"><span data-stu-id="19f07-125">For information about variations of this planning logic, see the Scenarios section below.</span></span>

## <a name="demand-at-blank-location"></a><span data-ttu-id="19f07-126">Eftirspurn í tómir stöðu</span><span class="sxs-lookup"><span data-stu-id="19f07-126">Demand at Blank Location</span></span>
<span data-ttu-id="19f07-127">Jafnvel þó merkt sé við reitinn **Birgðageymsla áskilin** er heimilt að stofna línur í kerfinu án birgðageymslukóða – einnig kallað tóm birgðageymsla.</span><span class="sxs-lookup"><span data-stu-id="19f07-127">Even if the **Location Mandatory** field is selected, the program will allow demand lines to be created without a location code, also referred to as blank location.</span></span> <span data-ttu-id="19f07-128">Þetta er frávik í kerfinu því það er með mismunandi uppsetningargildi sem stillt eru á að vinna með birgðageymslur (sjá ofangreint) og niðurstaðan verður sú að áætlunarkerfið stofnar ekki áætlunarlínu fyrir svona eftirspurnarlínu.</span><span class="sxs-lookup"><span data-stu-id="19f07-128">This is a deviation for the system because it has various setup values tuned to dealing with locations (see above) and as a result, the planning engine will not create a planning line for such a demand line.</span></span>

<span data-ttu-id="19f07-129">Ef reiturinn **Birgðargeymsla áskilin** áskilin er ekki valinn en einhver af uppsetningargildum birgðageymsla eru til er það einnig talið vera frávik og eftirspurnarkerfið bregst við með því að nota „lágmarksvalkost“: Varan er áætluð samkvæmt: Endurpöntunarstefna = Lota-fyrir-lotu (Pöntun er áfram Pöntun), Taka með birgðir = Já, allar aðrar áætlunarfæribreytur = Auðar.</span><span class="sxs-lookup"><span data-stu-id="19f07-129">If the **Location Mandatory** field is not selected but any of the location setup values exist, it is also considered a deviation, and the planning system will react by using the “minimal alternative”: The item is planned according to: Reordering Policy = Lot-for-Lot (Order remains Order), Include Inventory = Yes, all other planning parameters = Empty.</span></span>

## <a name="scenarios"></a><span data-ttu-id="19f07-130">Dæmi</span><span class="sxs-lookup"><span data-stu-id="19f07-130">Scenarios</span></span>
<span data-ttu-id="19f07-131">Eftirfarandi atburðarás lýsir afbrigðum eftirspurnar á auðum stað og hvernig áætlanakerfi leysir „lágmarksvalkost“.</span><span class="sxs-lookup"><span data-stu-id="19f07-131">The following scenarios describe variations of demand at blank location and how the planning system resolves to the “minimal alternative.”</span></span>

### <a name="setup-1"></a><span data-ttu-id="19f07-132">Uppsetning 1:</span><span class="sxs-lookup"><span data-stu-id="19f07-132">Setup 1:</span></span>
<span data-ttu-id="19f07-133">Birgðageymsla áskilin = Já</span><span class="sxs-lookup"><span data-stu-id="19f07-133">Location Mandatory = Yes</span></span>

<span data-ttu-id="19f07-134">Birgðahaldseining er sett upp fyrir RAUTT</span><span class="sxs-lookup"><span data-stu-id="19f07-134">SKU is set up for RED</span></span>

<span data-ttu-id="19f07-135">Íhlutir á staðnum = BLÁTT</span><span class="sxs-lookup"><span data-stu-id="19f07-135">Components at Location = BLUE</span></span>

#### <a name="case-11-demand-is-at-red-location"></a><span data-ttu-id="19f07-136">Dæmi 1.1: Eftirspurn er í birgðageymslunni  RAUTT</span><span class="sxs-lookup"><span data-stu-id="19f07-136">Case 1.1: Demand is at RED location</span></span>
<span data-ttu-id="19f07-137">Vörunni er áætlað samkvæmt áætlunarfæribreytum á birgðahaldseiningaspjaldinu.</span><span class="sxs-lookup"><span data-stu-id="19f07-137">The item is planned according to planning parameters on the SKU card.</span></span>

#### <a name="case-12-demand-is-at-blue-location"></a><span data-ttu-id="19f07-138">Dæmi 1.2: Eftirspurn er í birgðageymslunni  BLÁTT</span><span class="sxs-lookup"><span data-stu-id="19f07-138">Case 1.2: Demand is at BLUE location</span></span>
<span data-ttu-id="19f07-139">Vörunni er áætlað samkvæmt: Endurpöntunarstefna = Lota-fyrir-lotu (Pöntun er áfram Pöntun), Taka með birgðir = Já, allar aðrar áætlunarfæribreytur = tómar.</span><span class="sxs-lookup"><span data-stu-id="19f07-139">The item is planned according to: Reordering Policy = Lot-for-Lot (Order remains Order), Include Inventory = Yes, all other planning parameters = Empty.</span></span>

#### <a name="case-13-demand-is-at-green-location"></a><span data-ttu-id="19f07-140">Dæmi 1.3: Eftirspurn er í birgðageymslunni GRÆNT</span><span class="sxs-lookup"><span data-stu-id="19f07-140">Case 1.3: Demand is at GREEN location</span></span>
<span data-ttu-id="19f07-141">Vörunni er áætlað samkvæmt: Endurpöntunarstefna = Lota-fyrir-lotu (Pöntun er áfram Pöntun), Taka með birgðir = Já, allar aðrar áætlunarfæribreytur = tómar.</span><span class="sxs-lookup"><span data-stu-id="19f07-141">The item is planned according to: Reordering Policy = Lot-for-Lot (Order remains Order), Include Inventory = Yes, all other planning parameters = Empty.</span></span>

#### <a name="case-14-demand-is-at-blank-location"></a><span data-ttu-id="19f07-142">Dæmi 1.4: Eftirspurn er í birgðageymslunni TÓMT</span><span class="sxs-lookup"><span data-stu-id="19f07-142">Case 1.4: Demand is at BLANK location</span></span>
<span data-ttu-id="19f07-143">Vörunni er ekki áætlað þar sem engin birgðageymsla er skilgreind í eftirspurnarlínunni.</span><span class="sxs-lookup"><span data-stu-id="19f07-143">The item is not planned because no location is defined on the demand line.</span></span>

### <a name="setup-2"></a><span data-ttu-id="19f07-144">Uppsetning 2:</span><span class="sxs-lookup"><span data-stu-id="19f07-144">Setup 2:</span></span>
<span data-ttu-id="19f07-145">Birgðageymsla áskilin = Já</span><span class="sxs-lookup"><span data-stu-id="19f07-145">Location Mandatory = Yes</span></span>

<span data-ttu-id="19f07-146">Engin birgðahaldseining er til</span><span class="sxs-lookup"><span data-stu-id="19f07-146">No SKU exists</span></span>

<span data-ttu-id="19f07-147">Íhlutir á staðnum = BLÁTT</span><span class="sxs-lookup"><span data-stu-id="19f07-147">Components at Location = BLUE</span></span>

#### <a name="case-21-demand-is-at-red-location"></a><span data-ttu-id="19f07-148">Dæmi 2.1: Eftirspurn er í birgðageymslunni  RAUTT</span><span class="sxs-lookup"><span data-stu-id="19f07-148">Case 2.1: Demand is at RED location</span></span>
<span data-ttu-id="19f07-149">Vörunni er áætlað samkvæmt: Endurpöntunarstefna = Lota-fyrir-lotu (Pöntun er áfram Pöntun), Taka með birgðir = Já, allar aðrar áætlunarfæribreytur = tómar.</span><span class="sxs-lookup"><span data-stu-id="19f07-149">The item is planned according to: Reordering Policy = Lot-for-Lot (Order remains Order), Include Inventory = Yes, all other planning parameters = Empty.</span></span>

#### <a name="case-22-demand-is-at-blue-location"></a><span data-ttu-id="19f07-150">Dæmi 2.2: Eftirspurn er í birgðageymslunni  BLÁTT</span><span class="sxs-lookup"><span data-stu-id="19f07-150">Case 2.2: Demand is at BLUE location</span></span>
<span data-ttu-id="19f07-151">Vörunni er áætlað samkvæmt áætlunarfæribreytum á birgðaspjaldinu.</span><span class="sxs-lookup"><span data-stu-id="19f07-151">The item is planned according to planning parameters on the item card.</span></span>

### <a name="setup-3"></a><span data-ttu-id="19f07-152">Uppsetning 3:</span><span class="sxs-lookup"><span data-stu-id="19f07-152">Setup 3:</span></span>
<span data-ttu-id="19f07-153">Birgðageymsla áskilin = Nei</span><span class="sxs-lookup"><span data-stu-id="19f07-153">Location Mandatory = No</span></span>

<span data-ttu-id="19f07-154">Engin birgðahaldseining er til</span><span class="sxs-lookup"><span data-stu-id="19f07-154">No SKU exists</span></span>

<span data-ttu-id="19f07-155">Íhlutir á staðnum = BLÁTT</span><span class="sxs-lookup"><span data-stu-id="19f07-155">Components at Location = BLUE</span></span>

#### <a name="case-31-demand-is-at-red-location"></a><span data-ttu-id="19f07-156">Dæmi 3.1: Eftirspurn er í birgðageymslunni RAUTT</span><span class="sxs-lookup"><span data-stu-id="19f07-156">Case 3.1: Demand is at RED location</span></span>
<span data-ttu-id="19f07-157">Vörunni er áætlað samkvæmt: Endurpöntunarstefna = Lota-fyrir-lotu (Pöntun er áfram Pöntun), Taka með birgðir = Já, allar aðrar áætlunarfæribreytur = tómar.</span><span class="sxs-lookup"><span data-stu-id="19f07-157">The item is planned according to: Reordering Policy = Lot-for-Lot (Order remains Order), Include Inventory = Yes, all other planning parameters = Empty.</span></span>

#### <a name="case-32-demand-is-at-blue-location"></a><span data-ttu-id="19f07-158">Dæmi 3.2: Eftirspurn er í birgðageymslunni  BLÁTT</span><span class="sxs-lookup"><span data-stu-id="19f07-158">Case 3.2: Demand is at BLUE location</span></span>
<span data-ttu-id="19f07-159">Vörunni er áætlað samkvæmt áætlunarfæribreytum á birgðaspjaldinu.</span><span class="sxs-lookup"><span data-stu-id="19f07-159">The item is planned according to planning parameters on the item card.</span></span>

#### <a name="case-33-demand-is-at-blank-location"></a><span data-ttu-id="19f07-160">Dæmi 3.3: Eftirspurn er í birgðageymslunni TÓMT</span><span class="sxs-lookup"><span data-stu-id="19f07-160">Case 3.3: Demand is at BLANK location</span></span>
<span data-ttu-id="19f07-161">Vörunni er áætlað samkvæmt: Endurpöntunarstefna = Lota-fyrir-lotu (Pöntun er áfram Pöntun), Taka með birgðir = Já, allar aðrar áætlunarfæribreytur = tómar.</span><span class="sxs-lookup"><span data-stu-id="19f07-161">The item is planned according to: Reordering Policy = Lot-for-Lot (Order remains Order), Include Inventory = Yes, all other planning parameters = Empty.</span></span>

### <a name="setup-4"></a><span data-ttu-id="19f07-162">Uppsetning 4:</span><span class="sxs-lookup"><span data-stu-id="19f07-162">Setup 4:</span></span>
<span data-ttu-id="19f07-163">Birgðageymsla áskilin = Nei</span><span class="sxs-lookup"><span data-stu-id="19f07-163">Location Mandatory = No</span></span>

<span data-ttu-id="19f07-164">Engin birgðahaldseining er til</span><span class="sxs-lookup"><span data-stu-id="19f07-164">No SKU exists</span></span>

<span data-ttu-id="19f07-165">Íhlutir á staðnum = TÓMT</span><span class="sxs-lookup"><span data-stu-id="19f07-165">Components at Location = BLANK</span></span>

#### <a name="case-41-demand-is-at-blue-location"></a><span data-ttu-id="19f07-166">Dæmi 4.1: Eftirspurn er í birgðageymslunni BLÁTT</span><span class="sxs-lookup"><span data-stu-id="19f07-166">Case 4.1: Demand is at BLUE location</span></span>
<span data-ttu-id="19f07-167">Vörunni er áætlað samkvæmt: Endurpöntunarstefna = Lota-fyrir-lotu (Pöntun er áfram Pöntun), Taka með birgðir = Já, allar aðrar áætlunarfæribreytur = tómar.</span><span class="sxs-lookup"><span data-stu-id="19f07-167">The item is planned according to: Reordering Policy = Lot-for-Lot (Order remains Order), Include Inventory = Yes, all other planning parameters = Empty.</span></span>

#### <a name="case-42-demand-is-at-blank-location"></a><span data-ttu-id="19f07-168">Dæmi 4.2: Eftirspurn er í birgðageymslunni TÓMT</span><span class="sxs-lookup"><span data-stu-id="19f07-168">Case 4.2: Demand is at BLANK location</span></span>
<span data-ttu-id="19f07-169">Varan er áætluð í samræmi við áætlunarfæribreytur á birgðaspjaldinu.</span><span class="sxs-lookup"><span data-stu-id="19f07-169">The item is planned according to planning parameters on the item card.</span></span>

<span data-ttu-id="19f07-170">Eins og sjá má á síðasta dæmi er eina leiðin til að fá réttar niðurstöður fyrir eftirspurnarlínu án birgðageymslukóða sú að gera öll uppsetningargildi sem tengjast birgðageymslum óvirk.</span><span class="sxs-lookup"><span data-stu-id="19f07-170">As illustrated in the last scenario, the only way to get a correct result for a demand line without a location code is to disable all setup values relating to locations.</span></span> <span data-ttu-id="19f07-171">Sömuleiðis er eina leiðin til að fá stöðugar áætlunarniðurstöður fyrir eftirspurn í birgðageymslum sú að nota birgðahaldseiningar.</span><span class="sxs-lookup"><span data-stu-id="19f07-171">Similarly, the only way to get stable planning results for demand at locations is to use SKUs.</span></span> <span data-ttu-id="19f07-172">Af þeim sökum er fyrirtækjum sem þurfa oft að áætla fyrir eftirspurn í birgðageymslum ráðlagt að nota eindina Birgðahaldseiningar.</span><span class="sxs-lookup"><span data-stu-id="19f07-172">Therefore, if companies often plan for demand at locations, they are strongly advised to use the Stockkeeping Units granule.</span></span>

## <a name="see-also"></a><span data-ttu-id="19f07-173">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="19f07-173">See Also</span></span>  
<span data-ttu-id="19f07-174">[Hönnunarupplýsingar: Jöfnun eftirspurnar og framboðs](design-details-balancing-demand-and-supply.md) </span><span class="sxs-lookup"><span data-stu-id="19f07-174">[Design Details: Balancing Demand and Supply](design-details-balancing-demand-and-supply.md) </span></span>  
<span data-ttu-id="19f07-175">[Hönnunarupplýsingar: Miðlægar hugmyndir áætlanakerfisins](design-details-central-concepts-of-the-planning-system.md) </span><span class="sxs-lookup"><span data-stu-id="19f07-175">[Design Details: Central Concepts of the Planning System](design-details-central-concepts-of-the-planning-system.md) </span></span>  
[<span data-ttu-id="19f07-176">Hönnunarupplýsingar: framboðsáætlun</span><span class="sxs-lookup"><span data-stu-id="19f07-176">Design Details: Supply Planning</span></span>](design-details-supply-planning.md)
