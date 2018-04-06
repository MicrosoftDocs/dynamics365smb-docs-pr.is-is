---
title: "Kynning: Móttaka og Frágangur í Einfaldar grunngerð vöruhúss | Microsoft Docs"
description: "Í Finance and Operations, Business Edition, er hægt að framkvæma innleiðarferlið til að taka við og ganga frá á fjóra vegu, með því að nota mismunandi eiginleika, allt eftir flækjustigi vöruhússins."
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: b420bc1cc0707824385cda832ac905c016cdd706
ms.contentlocale: is-is
ms.lasthandoff: 03/22/2018

---
# <a name="walkthrough-receiving-and-putting-away-in-basic-warehouse-configurations"></a><span data-ttu-id="4a13e-103">Kynning: Móttaka og Frágangur í Einfaldar grunngerð vöruhúss</span><span class="sxs-lookup"><span data-stu-id="4a13e-103">Walkthrough: Receiving and Putting Away in Basic Warehouse Configurations</span></span>
<span data-ttu-id="4a13e-104">Í [!INCLUDE[d365fin](includes/d365fin_md.md)], er hægt að framkvæma innleiðarferlið til að taka við og ganga frá á fjóra vegu, með því að nota mismunandi eiginleika, allt eftir flækjustigi vöruhússins.</span><span class="sxs-lookup"><span data-stu-id="4a13e-104">In [!INCLUDE[d365fin](includes/d365fin_md.md)], the inbound processes for receiving and putting away can be performed in four ways using different functionalities depending on the warehouse complexity level.</span></span>  

|<span data-ttu-id="4a13e-105">Aðferð</span><span class="sxs-lookup"><span data-stu-id="4a13e-105">Method</span></span>|<span data-ttu-id="4a13e-106">Ferli á innleið</span><span class="sxs-lookup"><span data-stu-id="4a13e-106">Inbound process</span></span>|<span data-ttu-id="4a13e-107">Hólf</span><span class="sxs-lookup"><span data-stu-id="4a13e-107">Bins</span></span>|<span data-ttu-id="4a13e-108">Móttökur</span><span class="sxs-lookup"><span data-stu-id="4a13e-108">Receipts</span></span>|<span data-ttu-id="4a13e-109">Frágangur</span><span class="sxs-lookup"><span data-stu-id="4a13e-109">Put-aways</span></span>|<span data-ttu-id="4a13e-110">Flækjustig (Sjá [Hönnunarupplýsingar: uppsetning vöruhúss](design-details-warehouse-setup.md))</span><span class="sxs-lookup"><span data-stu-id="4a13e-110">Complexity level (See [Design Details: Warehouse Setup](design-details-warehouse-setup.md))</span></span>|  
|------------|---------------------|----------|--------------|----------------|--------------------------------------------------------------------------------------------------------------------|  
|<span data-ttu-id="4a13e-111">A</span><span class="sxs-lookup"><span data-stu-id="4a13e-111">A</span></span>|<span data-ttu-id="4a13e-112">Bóka móttöku og frágang frá pöntunarlínunni</span><span class="sxs-lookup"><span data-stu-id="4a13e-112">Post receipt and put-away from the order line</span></span>|<span data-ttu-id="4a13e-113">X</span><span class="sxs-lookup"><span data-stu-id="4a13e-113">X</span></span>|||<span data-ttu-id="4a13e-114">2</span><span class="sxs-lookup"><span data-stu-id="4a13e-114">2</span></span>|  
|<span data-ttu-id="4a13e-115">Á</span><span class="sxs-lookup"><span data-stu-id="4a13e-115">B</span></span>|<span data-ttu-id="4a13e-116">Bóka móttöku og frágang frá birgðafrágangsskjali</span><span class="sxs-lookup"><span data-stu-id="4a13e-116">Post receipt and put-away from an inventory put-away document</span></span>|||<span data-ttu-id="4a13e-117">X</span><span class="sxs-lookup"><span data-stu-id="4a13e-117">X</span></span>|<span data-ttu-id="4a13e-118">3</span><span class="sxs-lookup"><span data-stu-id="4a13e-118">3</span></span>|  
|<span data-ttu-id="4a13e-119">C</span><span class="sxs-lookup"><span data-stu-id="4a13e-119">C</span></span>|<span data-ttu-id="4a13e-120">Bóka móttöku og frágang frá vöruhúsamóttökuskjali</span><span class="sxs-lookup"><span data-stu-id="4a13e-120">Post receipt and put-away from a warehouse receipt document</span></span>||<span data-ttu-id="4a13e-121">X</span><span class="sxs-lookup"><span data-stu-id="4a13e-121">X</span></span>||<span data-ttu-id="4a13e-122">4/5/6</span><span class="sxs-lookup"><span data-stu-id="4a13e-122">4/5/6</span></span>|  
|<span data-ttu-id="4a13e-123">D</span><span class="sxs-lookup"><span data-stu-id="4a13e-123">D</span></span>|<span data-ttu-id="4a13e-124">Bóka móttöku frá vöruhúsamóttökuskjali og bóka frágang frá vöruhúsafrágangsskjali</span><span class="sxs-lookup"><span data-stu-id="4a13e-124">Post receipt from a warehouse receipt document and post put-away from a warehouse put-away document</span></span>||<span data-ttu-id="4a13e-125">X</span><span class="sxs-lookup"><span data-stu-id="4a13e-125">X</span></span>|<span data-ttu-id="4a13e-126">X</span><span class="sxs-lookup"><span data-stu-id="4a13e-126">X</span></span>|<span data-ttu-id="4a13e-127">4/5/6</span><span class="sxs-lookup"><span data-stu-id="4a13e-127">4/5/6</span></span>|  

<span data-ttu-id="4a13e-128">Nánari upplýsingar er að finna í [Hönnunarupplýsingar: vöruhúsaflæði inn](design-details-inbound-warehouse-flow.md).</span><span class="sxs-lookup"><span data-stu-id="4a13e-128">For more information, see [Design Details: Inbound Warehouse Flow](design-details-inbound-warehouse-flow.md).</span></span>  

<span data-ttu-id="4a13e-129">Eftirfarandi kynning sýnir aðferð B í fyrri töflu.</span><span class="sxs-lookup"><span data-stu-id="4a13e-129">The following walkthrough demonstrates method B in the previous table.</span></span>  

## <a name="about-this-walkthrough"></a><span data-ttu-id="4a13e-130">Um kynninguna</span><span class="sxs-lookup"><span data-stu-id="4a13e-130">About This Walkthrough</span></span>  
<span data-ttu-id="4a13e-131">Í grunnstillungum vöruhúss þar sem staðsetning er sett upp þannig að krafist sé frágangs en ekki móttökuvinnslu skal nota gluggan **Birgðafrágangur** til að skrá og bóka frágang og afhendingarupplýsingar fyrir upprunaskjöl á innleið.</span><span class="sxs-lookup"><span data-stu-id="4a13e-131">In basic warehouse configurations where your location is set up to require put-away processing but not receive processing, you use the **Inventory Put-away** window to record and post put-away and receipt information for your inbound source documents.</span></span> <span data-ttu-id="4a13e-132">Upprunaskjalið á innleið getur verið innkaupapöntun, söluvöruskilapöntun, millifærslupöntun á innleið eða framleiðslupöntun þar sem úttakið er tilbúið til frágangs.</span><span class="sxs-lookup"><span data-stu-id="4a13e-132">The inbound source document can be a purchase order, sales return order, inbound transfer order, or production order with output that is ready to be put away.</span></span>

> [!NOTE]
> <span data-ttu-id="4a13e-133">Jafnvel þótt stillingarnar séu kallaðar **Krefjast tínslu** og **Krefjast frágangs**, geturðu samt sem áður bókað móttöku og afhendingu beint frá uppruna viðskiptaskjala í birgðageymslum þar sem þú velur þessa gátreiti.</span><span class="sxs-lookup"><span data-stu-id="4a13e-133">Even though the settings are called **Require Pick** and **Require Put-away**, you can still post receipts and shipments directly from the source business documents at locations where you select these check boxes.</span></span>  

<span data-ttu-id="4a13e-134">Þessi kynning fjallar um eftirfarandi verk.</span><span class="sxs-lookup"><span data-stu-id="4a13e-134">This walkthrough demonstrates the following tasks.</span></span>  

-   <span data-ttu-id="4a13e-135">Stilli SILVER staðsetningu fyrir birgðafrágang.</span><span class="sxs-lookup"><span data-stu-id="4a13e-135">Setting up SILVER location for inventory put aways.</span></span>  
-   <span data-ttu-id="4a13e-136">Stilli SILVER staðsetningu fyrir meðhöndlun hólfa.</span><span class="sxs-lookup"><span data-stu-id="4a13e-136">Setting up SILVER location for bin handling.</span></span>  
-   <span data-ttu-id="4a13e-137">Skilgreinir sjálgefið hólf fyrir vöru LS-81.</span><span class="sxs-lookup"><span data-stu-id="4a13e-137">Defining a default bin for item LS-81.</span></span> <span data-ttu-id="4a13e-138">(LS-75 er þegar sett upp í CRONUS.)</span><span class="sxs-lookup"><span data-stu-id="4a13e-138">(LS-75 is already set up in CRONUS.)</span></span>  
-   <span data-ttu-id="4a13e-139">Stofna innkaupapöntun fyrir lánardrottinn 10000 fyrir 40 hátalara.</span><span class="sxs-lookup"><span data-stu-id="4a13e-139">Creating a purchase order for vendor 10000 for 40 loudspeakers.</span></span>  
-   <span data-ttu-id="4a13e-140">Staðfesti að frágangshólfin er forstillt samkvæmt uppsetningu.</span><span class="sxs-lookup"><span data-stu-id="4a13e-140">Verifying that the put-away bins are preset by setup.</span></span>  
-   <span data-ttu-id="4a13e-141">Gefur út innkaupapöntunina fyrir afgreiðslu vöruhúss.</span><span class="sxs-lookup"><span data-stu-id="4a13e-141">Releasing the purchase order for warehouse handling.</span></span>  
-   <span data-ttu-id="4a13e-142">Stofna birgðafrágang byggðan á útgefnu upprunaskjali.</span><span class="sxs-lookup"><span data-stu-id="4a13e-142">Creating an inventory put-away based on a released source document.</span></span>  
-   <span data-ttu-id="4a13e-143">Staðfesti að frágangshólfin erfast úr innkaupapöntuninni.</span><span class="sxs-lookup"><span data-stu-id="4a13e-143">Verifying that the put-away bins are inherited from the purchase order.</span></span>  
-   <span data-ttu-id="4a13e-144">Skráir vöruhúsahreyfinguna í vöruhúsið og bókar á sama tíma innkaupamóttökuna fyrir upprunaskjal innkaupapöntunarinnar.</span><span class="sxs-lookup"><span data-stu-id="4a13e-144">Registering the warehouse movement into the warehouse and at the same time posting the purchase receipt for the source purchase order.</span></span>  

## <a name="roles"></a><span data-ttu-id="4a13e-145">Hlutverk</span><span class="sxs-lookup"><span data-stu-id="4a13e-145">Roles</span></span>  
<span data-ttu-id="4a13e-146">Þessi kynning sýnir þau verk sem framkvæmd eru með eftirfarandi hlutverkum notenda:</span><span class="sxs-lookup"><span data-stu-id="4a13e-146">This walkthrough demonstrates tasks that are performed by the following user roles:</span></span>  

-   <span data-ttu-id="4a13e-147">Yfirmaður vöruhúss</span><span class="sxs-lookup"><span data-stu-id="4a13e-147">Warehouse Manager</span></span>  
-   <span data-ttu-id="4a13e-148">Innkaupaaðili</span><span class="sxs-lookup"><span data-stu-id="4a13e-148">Purchasing Agent</span></span>  
-   <span data-ttu-id="4a13e-149">Starfsmaður í vöruhúsi</span><span class="sxs-lookup"><span data-stu-id="4a13e-149">Warehouse Worker</span></span>  

## <a name="prerequisites"></a><span data-ttu-id="4a13e-150">Frumskilyrði</span><span class="sxs-lookup"><span data-stu-id="4a13e-150">Prerequisites</span></span>  
<span data-ttu-id="4a13e-151">Til að ljúka þessari kynningu þarf:</span><span class="sxs-lookup"><span data-stu-id="4a13e-151">To complete this walkthrough, you will need:</span></span>  

-   <span data-ttu-id="4a13e-152">CRONUS  International Ltd. er uppsett.</span><span class="sxs-lookup"><span data-stu-id="4a13e-152">CRONUS International Ltd. installed.</span></span>  
-   <span data-ttu-id="4a13e-153">Til að gera notanda að starfsmanni vöruhúss í SILVER staðsetningu á eftirfarandi hátt:</span><span class="sxs-lookup"><span data-stu-id="4a13e-153">To make yourself a warehouse employee at SILVER location by following these steps:</span></span>  

    1.  <span data-ttu-id="4a13e-154">Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **starfsmenn vöruhúss** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="4a13e-154">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Warehouse Employees**, and then choose the related link.</span></span>  
    2.  <span data-ttu-id="4a13e-155">Velja reitinn **Notandakenni** og velja síðan eigin notandareikning notanda í glugganum **Notendur**.</span><span class="sxs-lookup"><span data-stu-id="4a13e-155">Choose the **User ID** field, and select your own user account in the **Users** window.</span></span>  
    3.  <span data-ttu-id="4a13e-156">Í reitnum **Staðsetningarkóði** er fært inn SILVER.</span><span class="sxs-lookup"><span data-stu-id="4a13e-156">In the **Location Code** field, enter SILVER.</span></span>  
    4.  <span data-ttu-id="4a13e-157">Veljið reitinn **Sjálfgefið**.</span><span class="sxs-lookup"><span data-stu-id="4a13e-157">Select the **Default** field.</span></span>  

## <a name="story"></a><span data-ttu-id="4a13e-158">Ferill</span><span class="sxs-lookup"><span data-stu-id="4a13e-158">Story</span></span>  
<span data-ttu-id="4a13e-159">Ellen, stjórnandi vöruhúss hjá CRONUS International Ltd. stofnar innkaupapöntun fyrir 10 einingar af vöru LS-75 og 30 einingar af vöru LS-81 frá lánardrottni 10000 sem afhenda á til SILVER vöruhúss.</span><span class="sxs-lookup"><span data-stu-id="4a13e-159">Ellen, the warehouse manager at CRONUS International Ltd., creates a purchase order for 10 units of item LS-75 and 30 units of item LS-81 from vendor 10000 to be delivered to SILVER Warehouse.</span></span> <span data-ttu-id="4a13e-160">Þegar sending berst í vöruhúsið, gengur starfsmaður vöruhússins frá vörunum í sjálfgefin hólf sem eru skilgreind fyrir vörurnar.</span><span class="sxs-lookup"><span data-stu-id="4a13e-160">When the delivery arrives at the warehouse, John, the warehouse worker, puts the items away in default bins defined for the items.</span></span> <span data-ttu-id="4a13e-161">Frágangurinn er bókaður, vörurnar eru bókaðar sem mótteknar í birgðir og tiltækar til sölu eða aðra eftirspurn.</span><span class="sxs-lookup"><span data-stu-id="4a13e-161">When John posts the put-away, the items are posted as received into inventory and available for sale or other demand.</span></span>  

## <a name="setting-up-the-location"></a><span data-ttu-id="4a13e-162">Uppsetning staðsetningarinnar</span><span class="sxs-lookup"><span data-stu-id="4a13e-162">Setting up the Location</span></span>  
 <span data-ttu-id="4a13e-163">Uppsetning gluggans **Birgðageymsluspjald** skilgreinir vöruhúsaflæði fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="4a13e-163">The setup of the **Location Card** window defines the company’s warehouse flows.</span></span>  

### <a name="to-set-up-the-location"></a><span data-ttu-id="4a13e-164">Uppsetning staðsetningar</span><span class="sxs-lookup"><span data-stu-id="4a13e-164">To set up the location</span></span>  

1.  <span data-ttu-id="4a13e-165">Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Staðsetningar** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="4a13e-165">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Locations**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="4a13e-166">SILVER-staðsetningarspjaldið er opnað.</span><span class="sxs-lookup"><span data-stu-id="4a13e-166">Open the SILVER location card.</span></span>  
3.  <span data-ttu-id="4a13e-167">Veljið gátreitinn **Þarf að ganga frá**.</span><span class="sxs-lookup"><span data-stu-id="4a13e-167">Select the **Require Put-away** check box.</span></span>  

    <span data-ttu-id="4a13e-168">Setjið svo upp sjálfgefið hólf fyrir vörunúmerin tvö til að stjórna hvar gengið sé frá þeim.</span><span class="sxs-lookup"><span data-stu-id="4a13e-168">Proceed to set up a default bin for the two item numbers to control where they are put away.</span></span>  

4.  <span data-ttu-id="4a13e-169">Veldu aðgerðina **Hólf**.</span><span class="sxs-lookup"><span data-stu-id="4a13e-169">Choose the **Bins** action.</span></span>  
5.  <span data-ttu-id="4a13e-170">Veljið fyrstu röð fyrir hólf S-01-0001 og svo aðgerðina **Innihald**.</span><span class="sxs-lookup"><span data-stu-id="4a13e-170">Select the first row, for bin S-01-0001, and then choose the **Contents** action.</span></span>  

    <span data-ttu-id="4a13e-171">Takið eftir að í glugganum **Innihald hólfs** er vara LS-75 þegar sett upp sem efni í hólfi S-01-0001.</span><span class="sxs-lookup"><span data-stu-id="4a13e-171">Notice in the **Bin Content** window that item LS-75 is already set up as content in bin S-01-0001.</span></span>  

6.  <span data-ttu-id="4a13e-172">Valið er **Nýtt** aðgerð.</span><span class="sxs-lookup"><span data-stu-id="4a13e-172">Choose the **New** action.</span></span>  
7.  <span data-ttu-id="4a13e-173">Veljið **Fast** og svo **Sjálfgefið**.</span><span class="sxs-lookup"><span data-stu-id="4a13e-173">Select the **Fixed** and the **Default** fields.</span></span>  
8.  <span data-ttu-id="4a13e-174">Á **Vörunúmer** reitnum skaltu slá inn LS-81.</span><span class="sxs-lookup"><span data-stu-id="4a13e-174">In the **Item No.** field, enter LS-81.</span></span>  

## <a name="creating-the-purchase-order"></a><span data-ttu-id="4a13e-175">Stofna innkaupapöntunina</span><span class="sxs-lookup"><span data-stu-id="4a13e-175">Creating the Purchase Order</span></span>  
<span data-ttu-id="4a13e-176">Innkaupapantanir eru algengustu tegundir af upprunaskjölum á innleið.</span><span class="sxs-lookup"><span data-stu-id="4a13e-176">Purchase orders are the most common type of inbound source document.</span></span>  

### <a name="to-create-the-purchase-order"></a><span data-ttu-id="4a13e-177">Innkaupapöntunin stofnuð</span><span class="sxs-lookup"><span data-stu-id="4a13e-177">To create the purchase order</span></span>  

1.  <span data-ttu-id="4a13e-178">Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Innkaupapantanir** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="4a13e-178">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Purchase Orders**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="4a13e-179">Valið er **Nýtt** aðgerð.</span><span class="sxs-lookup"><span data-stu-id="4a13e-179">Choose the **New** action.</span></span>  
3.  <span data-ttu-id="4a13e-180">Stofna innkaupapöntun fyrir lánardrottinn 10000 á vinnudeginum (23. Janúar) með eftirfarandi innkaupapöntunarlínum.</span><span class="sxs-lookup"><span data-stu-id="4a13e-180">Create a purchase order for vendor 10000 on the work date (January 23) with the following purchase order lines.</span></span>  

    |<span data-ttu-id="4a13e-181">Vara</span><span class="sxs-lookup"><span data-stu-id="4a13e-181">Item</span></span>|<span data-ttu-id="4a13e-182">Staðsetningarkóði</span><span class="sxs-lookup"><span data-stu-id="4a13e-182">Location code</span></span>|<span data-ttu-id="4a13e-183">Hólfkóði</span><span class="sxs-lookup"><span data-stu-id="4a13e-183">Bin code</span></span>|<span data-ttu-id="4a13e-184">Magn</span><span class="sxs-lookup"><span data-stu-id="4a13e-184">Quantity</span></span>|  
    |----------|-------------------|--------------|--------------|  
    |<span data-ttu-id="4a13e-185">LS_75</span><span class="sxs-lookup"><span data-stu-id="4a13e-185">LS_75</span></span>|<span data-ttu-id="4a13e-186">SILVER</span><span class="sxs-lookup"><span data-stu-id="4a13e-186">SILVER</span></span>|<span data-ttu-id="4a13e-187">S-01-0001</span><span class="sxs-lookup"><span data-stu-id="4a13e-187">S-01-0001</span></span>|<span data-ttu-id="4a13e-188">10</span><span class="sxs-lookup"><span data-stu-id="4a13e-188">10</span></span>|  
    |<span data-ttu-id="4a13e-189">LS-81</span><span class="sxs-lookup"><span data-stu-id="4a13e-189">LS-81</span></span>|<span data-ttu-id="4a13e-190">SILVER</span><span class="sxs-lookup"><span data-stu-id="4a13e-190">SILVER</span></span>|<span data-ttu-id="4a13e-191">S-01-0001</span><span class="sxs-lookup"><span data-stu-id="4a13e-191">S-01-0001</span></span>|<span data-ttu-id="4a13e-192">30</span><span class="sxs-lookup"><span data-stu-id="4a13e-192">30</span></span>|  

    > [!NOTE]  
    >  <span data-ttu-id="4a13e-193">Hólfkóðinn færist sjálfvirkt inn samkvæmt uppsetningunni sem gerð var í hlutanum „Staðsetning sett upp.“</span><span class="sxs-lookup"><span data-stu-id="4a13e-193">The bin code is entered automatically according to the setup that you performed in the “Setting up the Location” section.</span></span>  

    <span data-ttu-id="4a13e-194">Tilkynnið svo vöruhúsinu að innkaupapöntunin sé tilbúin til afgreiðslu í vöruhúsi þegar sendingin berst.</span><span class="sxs-lookup"><span data-stu-id="4a13e-194">Proceed to notify the warehouse that the purchase order is ready for warehouse handling when the delivery arrives.</span></span>  

4.  <span data-ttu-id="4a13e-195">Valið er **Losa** aðgerð.</span><span class="sxs-lookup"><span data-stu-id="4a13e-195">Choose the **Release** action.</span></span>  

    <span data-ttu-id="4a13e-196">Afhending hátalara frá lánardrottni 10000 hefur borist til SILVER vöruhússins og starfsmaður gengur svo frá þeim.</span><span class="sxs-lookup"><span data-stu-id="4a13e-196">The delivery of loudspeakers from vendor 10000 has arrived at SILVER warehouse, and John proceeds to put them away.</span></span>  

## <a name="receiving-and-putting-the-items-away"></a><span data-ttu-id="4a13e-197">Móttaka og frágangur varanna</span><span class="sxs-lookup"><span data-stu-id="4a13e-197">Receiving and Putting the Items Away</span></span>  
<span data-ttu-id="4a13e-198">Í glugganum **Birgðafrágangur** er hægt að meðhöndla alla virkni vöruhúss á innleið fyrir tiltekið upprunaskjal, til dæmis innkaupapöntun.</span><span class="sxs-lookup"><span data-stu-id="4a13e-198">In the **Inventory Put-away** window, you can manage all inbound warehouse activities for a specific source document, such as a purchase order.</span></span>  

### <a name="to-receive-and-put-the-items-away"></a><span data-ttu-id="4a13e-199">Tekið á móti og gengið frá vörunum</span><span class="sxs-lookup"><span data-stu-id="4a13e-199">To receive and put the items away</span></span>  

1.  <span data-ttu-id="4a13e-200">Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Birgðafrágangur** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="4a13e-200">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Inventory Put-aways**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="4a13e-201">Valið er **Nýtt** aðgerð.</span><span class="sxs-lookup"><span data-stu-id="4a13e-201">Choose the **New** action.</span></span>  
3.  <span data-ttu-id="4a13e-202">Veljið reitinn **Upprunaskjal** og svo **Innkaupapöntun**.</span><span class="sxs-lookup"><span data-stu-id="4a13e-202">Select the **Source Document** field, and then select **Purchase Order**.</span></span>  
4.  <span data-ttu-id="4a13e-203">Veldu reitinn **Upprunanr.**, velja línuna fyrir innkaup frá viðskiptamanni 10000 og skal velja svo hnappinn **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="4a13e-203">Select the **Source No.** field, select the line for the purchase from vendor 10000, and then choose the **OK** button.</span></span>  

    <span data-ttu-id="4a13e-204">Að öðrum kosti, á flipanum **Aðgerðir** í flokknum **Eiginleikar** skal velja **Sækja upprunaskjal**og síðan innkaupapöntunina.</span><span class="sxs-lookup"><span data-stu-id="4a13e-204">Alternatively, on the **Actions** tab, in the **Functions** group, choose **Get Source Document**, and then select the purchase order.</span></span>  

5.  <span data-ttu-id="4a13e-205">Velja aðgerðina **Færa sjálfkr. magn til afgr.**.</span><span class="sxs-lookup"><span data-stu-id="4a13e-205">Choose the **Autofill Qty. to Handle** action.</span></span>  

    <span data-ttu-id="4a13e-206">Að öðrum kosti, í reitnum **Magn til afgreiðslu** er fært inn 10 og 30 í birgðafrágangslínurnar tvær, í þeirri röð.</span><span class="sxs-lookup"><span data-stu-id="4a13e-206">Alternatively, in the **Qty. to Handle** field, enter 10 and 30 respectively on the two inventory put-away lines.</span></span>  

6.  <span data-ttu-id="4a13e-207">Veldu aðgerðina **Bóka**, veldu **Móttaka** aðgerðina og veldu síðan **Í lagi** hnappinn.</span><span class="sxs-lookup"><span data-stu-id="4a13e-207">Choose the **Post** action, select the **Receive** action, and then choose the **OK** button.</span></span>  

    <span data-ttu-id="4a13e-208">Frágangur hátalaranna 40 í hólf S-01-0001 er nú skráður og jákvæð birgðafærsla er stofnuð sem endurspeglar hina bókuðu innkaupamóttöku.</span><span class="sxs-lookup"><span data-stu-id="4a13e-208">The 40 loudspeakers are now registered as put away in bin S-01-0001, and a positive item ledger entry is created reflecting the posted purchase receipt.</span></span>  

## <a name="see-also"></a><span data-ttu-id="4a13e-209">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="4a13e-209">See Also</span></span>  
 <span data-ttu-id="4a13e-210">[Ganga frá vörum með birgðafrágangi](warehouse-how-to-put-items-away-with-inventory-put-aways.md) </span><span class="sxs-lookup"><span data-stu-id="4a13e-210">[Put Items Away with Inventory Put-aways](warehouse-how-to-put-items-away-with-inventory-put-aways.md) </span></span>  
 <span data-ttu-id="4a13e-211">[Setja upp einfaldar vöruhúsaaðgerðir með aðgerðasvæði](warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md) </span><span class="sxs-lookup"><span data-stu-id="4a13e-211">[Set Up Basic Warehouses with Operations Areas](warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md) </span></span>  
 <span data-ttu-id="4a13e-212">[Færa íhluti á aðgerðasvæði í grunnskilgreiningu vöruhúss](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md) </span><span class="sxs-lookup"><span data-stu-id="4a13e-212">[Move Components to an Operation Area in Basic Warehouse Configurations](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md) </span></span>  
 <span data-ttu-id="4a13e-213">[Taka til fyrir framleiðslu eða samsetningu](warehouse-how-to-pick-for-production.md) </span><span class="sxs-lookup"><span data-stu-id="4a13e-213">[Pick for Production or Assembly](warehouse-how-to-pick-for-production.md) </span></span>  
 <span data-ttu-id="4a13e-214">[Færa vörur eftir þörfum í einfaldri grunngerð vöruhúsa](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md) </span><span class="sxs-lookup"><span data-stu-id="4a13e-214">[Move Items Ad Hoc in Basic Warehouse Configurations](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md) </span></span>  
 <span data-ttu-id="4a13e-215">[Hönnunarupplýsingar: vöruhúsaflæði inn](design-details-inbound-warehouse-flow.md) </span><span class="sxs-lookup"><span data-stu-id="4a13e-215">[Design Details: Inbound Warehouse Flow](design-details-inbound-warehouse-flow.md) </span></span>  
 [<span data-ttu-id="4a13e-216">Kynningar á viðskiptaferli</span><span class="sxs-lookup"><span data-stu-id="4a13e-216">Business Process Walkthroughs</span></span>](walkthrough-business-process-walkthroughs.md)  
 <span data-ttu-id="4a13e-217">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="4a13e-217">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

