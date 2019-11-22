---
title: 'Kynning: Móttaka og Frágangur í Einfaldar grunngerð vöruhúss | Microsoft Docs'
description: Í Business Central er hægt að framkvæma innleiðarferlið til að taka við og ganga frá á fjóra vegu, með því að nota mismunandi eiginleika, allt eftir flækjustigi vöruhússins.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 31ac21dbba331748c9eef7bce199a5709147016b
ms.sourcegitcommit: 319023e53627dbe8e68643908aacc6fd594a4957
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/04/2019
ms.locfileid: "2554645"
---
# <a name="walkthrough-receiving-and-putting-away-in-basic-warehouse-configurations"></a><span data-ttu-id="6004e-103">Kynning: Móttaka og Frágangur í Einfaldar grunngerð vöruhúss</span><span class="sxs-lookup"><span data-stu-id="6004e-103">Walkthrough: Receiving and Putting Away in Basic Warehouse Configurations</span></span>

<span data-ttu-id="6004e-104">**Athugið**: Framkvæma verður þessa kynningu í sýnifyrirtæki með valkostinum **Fullt mat - öll sýnigögn** sem er í boði í sandkassaumhverfinu.</span><span class="sxs-lookup"><span data-stu-id="6004e-104">**Note**: This walkthrough must be performed on a demonstration company with the **Full Evaluation - Complete Sample Data** option, which is available in the Sandbox environment.</span></span> <span data-ttu-id="6004e-105">Nánari upplýsingar eru í [Sandkassaumhverfi stofnað](across-how-create-sandbox-environment.md).</span><span class="sxs-lookup"><span data-stu-id="6004e-105">For more information, see [Creating a Sandbox Environment](across-how-create-sandbox-environment.md).</span></span>

<span data-ttu-id="6004e-106">Í [!INCLUDE[d365fin](includes/d365fin_md.md)], er hægt að framkvæma innleiðarferlið til að taka við og ganga frá á fjóra vegu, með því að nota mismunandi eiginleika, allt eftir flækjustigi vöruhússins.</span><span class="sxs-lookup"><span data-stu-id="6004e-106">In [!INCLUDE[d365fin](includes/d365fin_md.md)], the inbound processes for receiving and putting away can be performed in four ways using different functionalities depending on the warehouse complexity level.</span></span>  

|<span data-ttu-id="6004e-107">Aðferð</span><span class="sxs-lookup"><span data-stu-id="6004e-107">Method</span></span>|<span data-ttu-id="6004e-108">Ferli á innleið</span><span class="sxs-lookup"><span data-stu-id="6004e-108">Inbound process</span></span>|<span data-ttu-id="6004e-109">Hólf</span><span class="sxs-lookup"><span data-stu-id="6004e-109">Bins</span></span>|<span data-ttu-id="6004e-110">Móttökur</span><span class="sxs-lookup"><span data-stu-id="6004e-110">Receipts</span></span>|<span data-ttu-id="6004e-111">Frágangur</span><span class="sxs-lookup"><span data-stu-id="6004e-111">Put-aways</span></span>|<span data-ttu-id="6004e-112">Flækjustig (Sjá [Hönnunarupplýsingar: uppsetning vöruhúss](design-details-warehouse-setup.md))</span><span class="sxs-lookup"><span data-stu-id="6004e-112">Complexity level (See [Design Details: Warehouse Setup](design-details-warehouse-setup.md))</span></span>|  
|------------|---------------------|----------|--------------|----------------|--------------------------------------------------------------------------------------------------------------------|  
|<span data-ttu-id="6004e-113">A</span><span class="sxs-lookup"><span data-stu-id="6004e-113">A</span></span>|<span data-ttu-id="6004e-114">Bóka móttöku og frágang frá pöntunarlínunni</span><span class="sxs-lookup"><span data-stu-id="6004e-114">Post receipt and put-away from the order line</span></span>|<span data-ttu-id="6004e-115">X</span><span class="sxs-lookup"><span data-stu-id="6004e-115">X</span></span>|||<span data-ttu-id="6004e-116">2</span><span class="sxs-lookup"><span data-stu-id="6004e-116">2</span></span>|  
|<span data-ttu-id="6004e-117">Á</span><span class="sxs-lookup"><span data-stu-id="6004e-117">B</span></span>|<span data-ttu-id="6004e-118">Bóka móttöku og frágang frá birgðafrágangsskjali</span><span class="sxs-lookup"><span data-stu-id="6004e-118">Post receipt and put-away from an inventory put-away document</span></span>|||<span data-ttu-id="6004e-119">X</span><span class="sxs-lookup"><span data-stu-id="6004e-119">X</span></span>|<span data-ttu-id="6004e-120">3</span><span class="sxs-lookup"><span data-stu-id="6004e-120">3</span></span>|  
|<span data-ttu-id="6004e-121">C</span><span class="sxs-lookup"><span data-stu-id="6004e-121">C</span></span>|<span data-ttu-id="6004e-122">Bóka móttöku og frágang frá vöruhúsamóttökuskjali</span><span class="sxs-lookup"><span data-stu-id="6004e-122">Post receipt and put-away from a warehouse receipt document</span></span>||<span data-ttu-id="6004e-123">X</span><span class="sxs-lookup"><span data-stu-id="6004e-123">X</span></span>||<span data-ttu-id="6004e-124">4/5/6</span><span class="sxs-lookup"><span data-stu-id="6004e-124">4/5/6</span></span>|  
|<span data-ttu-id="6004e-125">D</span><span class="sxs-lookup"><span data-stu-id="6004e-125">D</span></span>|<span data-ttu-id="6004e-126">Bóka móttöku frá vöruhúsamóttökuskjali og bóka frágang frá vöruhúsafrágangsskjali</span><span class="sxs-lookup"><span data-stu-id="6004e-126">Post receipt from a warehouse receipt document and post put-away from a warehouse put-away document</span></span>||<span data-ttu-id="6004e-127">X</span><span class="sxs-lookup"><span data-stu-id="6004e-127">X</span></span>|<span data-ttu-id="6004e-128">X</span><span class="sxs-lookup"><span data-stu-id="6004e-128">X</span></span>|<span data-ttu-id="6004e-129">4/5/6</span><span class="sxs-lookup"><span data-stu-id="6004e-129">4/5/6</span></span>|  

<span data-ttu-id="6004e-130">Nánari upplýsingar er að finna í [Hönnunarupplýsingar: vöruhúsaflæði inn](design-details-inbound-warehouse-flow.md).</span><span class="sxs-lookup"><span data-stu-id="6004e-130">For more information, see [Design Details: Inbound Warehouse Flow](design-details-inbound-warehouse-flow.md).</span></span>  

<span data-ttu-id="6004e-131">Eftirfarandi kynning sýnir aðferð B í fyrri töflu.</span><span class="sxs-lookup"><span data-stu-id="6004e-131">The following walkthrough demonstrates method B in the previous table.</span></span>  

## <a name="about-this-walkthrough"></a><span data-ttu-id="6004e-132">Um kynninguna</span><span class="sxs-lookup"><span data-stu-id="6004e-132">About This Walkthrough</span></span>  
<span data-ttu-id="6004e-133">Í grunnstillungum vöruhúss þar sem staðsetning er sett upp þannig að krafist sé frágangs en ekki móttökuvinnslu skal nota síðuna **Birgðafrágangur** til að skrá og bóka frágang og afhendingarupplýsingar fyrir upprunaskjöl á innleið.</span><span class="sxs-lookup"><span data-stu-id="6004e-133">In basic warehouse configurations where your location is set up to require put-away processing but not receive processing, you use the **Inventory Put-away** page to record and post put-away and receipt information for your inbound source documents.</span></span> <span data-ttu-id="6004e-134">Upprunaskjalið á innleið getur verið innkaupapöntun, söluvöruskilapöntun, millifærslupöntun á innleið eða framleiðslupöntun þar sem úttakið er tilbúið til frágangs.</span><span class="sxs-lookup"><span data-stu-id="6004e-134">The inbound source document can be a purchase order, sales return order, inbound transfer order, or production order with output that is ready to be put away.</span></span>

> [!NOTE]
> <span data-ttu-id="6004e-135">Jafnvel þótt stillingarnar séu kallaðar **Krefjast tínslu** og **Krefjast frágangs**, geturðu samt sem áður bókað móttöku og afhendingu beint frá uppruna viðskiptaskjala í birgðageymslum þar sem þú velur þessa gátreiti.</span><span class="sxs-lookup"><span data-stu-id="6004e-135">Even though the settings are called **Require Pick** and **Require Put-away**, you can still post receipts and shipments directly from the source business documents at locations where you select these check boxes.</span></span>  

<span data-ttu-id="6004e-136">Þessi kynning fjallar um eftirfarandi verk.</span><span class="sxs-lookup"><span data-stu-id="6004e-136">This walkthrough demonstrates the following tasks.</span></span>  

-   <span data-ttu-id="6004e-137">Stilli SILVER staðsetningu fyrir birgðafrágang.</span><span class="sxs-lookup"><span data-stu-id="6004e-137">Setting up SILVER location for inventory put aways.</span></span>  
-   <span data-ttu-id="6004e-138">Stilli SILVER staðsetningu fyrir meðhöndlun hólfa.</span><span class="sxs-lookup"><span data-stu-id="6004e-138">Setting up SILVER location for bin handling.</span></span>  
-   <span data-ttu-id="6004e-139">Skilgreinir sjálgefið hólf fyrir vöru LS-81.</span><span class="sxs-lookup"><span data-stu-id="6004e-139">Defining a default bin for item LS-81.</span></span> <span data-ttu-id="6004e-140">(LS-75 er þegar uppsett í CRONUS.)</span><span class="sxs-lookup"><span data-stu-id="6004e-140">(LS-75 is already set up in CRONUS.)</span></span>  
-   <span data-ttu-id="6004e-141">Stofna innkaupapöntun fyrir lánardrottinn 10000 fyrir 40 hátalara.</span><span class="sxs-lookup"><span data-stu-id="6004e-141">Creating a purchase order for vendor 10000 for 40 loudspeakers.</span></span>  
-   <span data-ttu-id="6004e-142">Staðfesti að frágangshólfin er forstillt samkvæmt uppsetningu.</span><span class="sxs-lookup"><span data-stu-id="6004e-142">Verifying that the put-away bins are preset by setup.</span></span>  
-   <span data-ttu-id="6004e-143">Gefur út innkaupapöntunina fyrir afgreiðslu vöruhúss.</span><span class="sxs-lookup"><span data-stu-id="6004e-143">Releasing the purchase order for warehouse handling.</span></span>  
-   <span data-ttu-id="6004e-144">Stofna birgðafrágang byggðan á útgefnu upprunaskjali.</span><span class="sxs-lookup"><span data-stu-id="6004e-144">Creating an inventory put-away based on a released source document.</span></span>  
-   <span data-ttu-id="6004e-145">Staðfesti að frágangshólfin erfast úr innkaupapöntuninni.</span><span class="sxs-lookup"><span data-stu-id="6004e-145">Verifying that the put-away bins are inherited from the purchase order.</span></span>  
-   <span data-ttu-id="6004e-146">Skráir vöruhúsahreyfinguna í vöruhúsið og bókar á sama tíma innkaupamóttökuna fyrir upprunaskjal innkaupapöntunarinnar.</span><span class="sxs-lookup"><span data-stu-id="6004e-146">Registering the warehouse movement into the warehouse and at the same time posting the purchase receipt for the source purchase order.</span></span>  

## <a name="roles"></a><span data-ttu-id="6004e-147">Hlutverk</span><span class="sxs-lookup"><span data-stu-id="6004e-147">Roles</span></span>  
<span data-ttu-id="6004e-148">Þessi kynning sýnir þau verk sem framkvæmd eru með eftirfarandi hlutverkum notenda:</span><span class="sxs-lookup"><span data-stu-id="6004e-148">This walkthrough demonstrates tasks that are performed by the following user roles:</span></span>  

-   <span data-ttu-id="6004e-149">Yfirmaður vöruhúss</span><span class="sxs-lookup"><span data-stu-id="6004e-149">Warehouse Manager</span></span>  
-   <span data-ttu-id="6004e-150">Innkaupaaðili</span><span class="sxs-lookup"><span data-stu-id="6004e-150">Purchasing Agent</span></span>  
-   <span data-ttu-id="6004e-151">Starfsmaður í vöruhúsi</span><span class="sxs-lookup"><span data-stu-id="6004e-151">Warehouse Worker</span></span>  

## <a name="prerequisites"></a><span data-ttu-id="6004e-152">Frumskilyrði</span><span class="sxs-lookup"><span data-stu-id="6004e-152">Prerequisites</span></span>  
<span data-ttu-id="6004e-153">Til að ljúka þessari kynningu þarf:</span><span class="sxs-lookup"><span data-stu-id="6004e-153">To complete this walkthrough, you will need:</span></span>  

-   <span data-ttu-id="6004e-154">CRONUS International Ltd. er uppsett.</span><span class="sxs-lookup"><span data-stu-id="6004e-154">CRONUS International Ltd. installed.</span></span>  
-   <span data-ttu-id="6004e-155">Til að gera notanda að starfsmanni vöruhúss í SILVER staðsetningu á eftirfarandi hátt:</span><span class="sxs-lookup"><span data-stu-id="6004e-155">To make yourself a warehouse employee at SILVER location by following these steps:</span></span>  

    1.  <span data-ttu-id="6004e-156">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Starfsfólk vöruhúss** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="6004e-156">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Warehouse Employees**, and then choose the related link.</span></span>  
    2.  <span data-ttu-id="6004e-157">Velja reitinn **Notandakenni** og velja síðan eigin notandareikning notanda á síðunni **Notendur**.</span><span class="sxs-lookup"><span data-stu-id="6004e-157">Choose the **User ID** field, and select your own user account on the **Users** page.</span></span>  
    3.  <span data-ttu-id="6004e-158">Í reitnum **Staðsetningarkóði** er fært inn SILVER.</span><span class="sxs-lookup"><span data-stu-id="6004e-158">In the **Location Code** field, enter SILVER.</span></span>  
    4.  <span data-ttu-id="6004e-159">Veljið reitinn **Sjálfgefið**.</span><span class="sxs-lookup"><span data-stu-id="6004e-159">Select the **Default** field.</span></span>  

## <a name="story"></a><span data-ttu-id="6004e-160">Ferill</span><span class="sxs-lookup"><span data-stu-id="6004e-160">Story</span></span>  
<span data-ttu-id="6004e-161">Ellen, stjórnandi vöruhúss hjá CRONUS International Ltd. stofnar innkaupapöntun fyrir 10 einingar af vöru LS-75 og 30 einingar af vöru LS-81 frá lánardrottni 10000 sem afhenda á til SILVER vöruhúss.</span><span class="sxs-lookup"><span data-stu-id="6004e-161">Ellen, the warehouse manager at CRONUS International Ltd., creates a purchase order for 10 units of item LS-75 and 30 units of item LS-81 from vendor 10000 to be delivered to SILVER Warehouse.</span></span> <span data-ttu-id="6004e-162">Þegar sending berst í vöruhúsið, gengur starfsmaður vöruhússins frá vörunum í sjálfgefin hólf sem eru skilgreind fyrir vörurnar.</span><span class="sxs-lookup"><span data-stu-id="6004e-162">When the delivery arrives at the warehouse, John, the warehouse worker, puts the items away in default bins defined for the items.</span></span> <span data-ttu-id="6004e-163">Frágangurinn er bókaður, vörurnar eru bókaðar sem mótteknar í birgðir og tiltækar til sölu eða aðra eftirspurn.</span><span class="sxs-lookup"><span data-stu-id="6004e-163">When John posts the put-away, the items are posted as received into inventory and available for sale or other demand.</span></span>  

## <a name="setting-up-the-location"></a><span data-ttu-id="6004e-164">Uppsetning staðsetningarinnar</span><span class="sxs-lookup"><span data-stu-id="6004e-164">Setting up the Location</span></span>  
 <span data-ttu-id="6004e-165">Uppsetning síðunnar **Birgðageymsluspjald** skilgreinir vöruhúsaflæði fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="6004e-165">The setup of the **Location Card** page defines the company’s warehouse flows.</span></span>  

### <a name="to-set-up-the-location"></a><span data-ttu-id="6004e-166">Uppsetning staðsetningar</span><span class="sxs-lookup"><span data-stu-id="6004e-166">To set up the location</span></span>  

1.  <span data-ttu-id="6004e-167">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Staðsetningar** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="6004e-167">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Locations**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="6004e-168">SILVER-staðsetningarspjaldið er opnað.</span><span class="sxs-lookup"><span data-stu-id="6004e-168">Open the SILVER location card.</span></span>  
3.  <span data-ttu-id="6004e-169">Veljið gátreitinn **Þarf að ganga frá**.</span><span class="sxs-lookup"><span data-stu-id="6004e-169">Select the **Require Put-away** check box.</span></span>  

    <span data-ttu-id="6004e-170">Setjið svo upp sjálfgefið hólf fyrir vörunúmerin tvö til að stjórna hvar gengið sé frá þeim.</span><span class="sxs-lookup"><span data-stu-id="6004e-170">Proceed to set up a default bin for the two item numbers to control where they are put away.</span></span>  

4.  <span data-ttu-id="6004e-171">Veldu aðgerðina **Hólf**.</span><span class="sxs-lookup"><span data-stu-id="6004e-171">Choose the **Bins** action.</span></span>  
5.  <span data-ttu-id="6004e-172">Veljið fyrstu röð fyrir hólf S-01-0001 og svo aðgerðina **Innihald**.</span><span class="sxs-lookup"><span data-stu-id="6004e-172">Select the first row, for bin S-01-0001, and then choose the **Contents** action.</span></span>  

    <span data-ttu-id="6004e-173">Takið eftir að á síðunni **Innihald hólfs** er vara LS-75 þegar sett upp sem efni í hólfi S-01-0001.</span><span class="sxs-lookup"><span data-stu-id="6004e-173">Notice on the **Bin Content** page that item LS-75 is already set up as content in bin S-01-0001.</span></span>  

6.  <span data-ttu-id="6004e-174">Valið er **Nýtt** aðgerð.</span><span class="sxs-lookup"><span data-stu-id="6004e-174">Choose the **New** action.</span></span>  
7.  <span data-ttu-id="6004e-175">Veljið **Fast** og svo **Sjálfgefið**.</span><span class="sxs-lookup"><span data-stu-id="6004e-175">Select the **Fixed** and the **Default** fields.</span></span>  
8.  <span data-ttu-id="6004e-176">Á **Vörunúmer** reitnum skaltu slá inn LS-81.</span><span class="sxs-lookup"><span data-stu-id="6004e-176">In the **Item No.** field, enter LS-81.</span></span>  

## <a name="creating-the-purchase-order"></a><span data-ttu-id="6004e-177">Stofna innkaupapöntunina</span><span class="sxs-lookup"><span data-stu-id="6004e-177">Creating the Purchase Order</span></span>  
<span data-ttu-id="6004e-178">Innkaupapantanir eru algengustu tegundir af upprunaskjölum á innleið.</span><span class="sxs-lookup"><span data-stu-id="6004e-178">Purchase orders are the most common type of inbound source document.</span></span>  

### <a name="to-create-the-purchase-order"></a><span data-ttu-id="6004e-179">Innkaupapöntunin stofnuð</span><span class="sxs-lookup"><span data-stu-id="6004e-179">To create the purchase order</span></span>  

1.  <span data-ttu-id="6004e-180">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Innkaupapantanir** og veldu síðan tengda hlekkinn.</span><span class="sxs-lookup"><span data-stu-id="6004e-180">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Purchase Orders**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="6004e-181">Valið er **Nýtt** aðgerð.</span><span class="sxs-lookup"><span data-stu-id="6004e-181">Choose the **New** action.</span></span>  
3.  <span data-ttu-id="6004e-182">Stofna innkaupapöntun fyrir lánardrottinn 10000 á vinnudeginum (23. Janúar) með eftirfarandi innkaupapöntunarlínum.</span><span class="sxs-lookup"><span data-stu-id="6004e-182">Create a purchase order for vendor 10000 on the work date (January 23) with the following purchase order lines.</span></span>  

    |<span data-ttu-id="6004e-183">Vara</span><span class="sxs-lookup"><span data-stu-id="6004e-183">Item</span></span>|<span data-ttu-id="6004e-184">Staðsetningarkóði</span><span class="sxs-lookup"><span data-stu-id="6004e-184">Location code</span></span>|<span data-ttu-id="6004e-185">Hólfkóði</span><span class="sxs-lookup"><span data-stu-id="6004e-185">Bin code</span></span>|<span data-ttu-id="6004e-186">Magn</span><span class="sxs-lookup"><span data-stu-id="6004e-186">Quantity</span></span>|  
    |----------|-------------------|--------------|--------------|  
    |<span data-ttu-id="6004e-187">LS_75</span><span class="sxs-lookup"><span data-stu-id="6004e-187">LS_75</span></span>|<span data-ttu-id="6004e-188">SILVER</span><span class="sxs-lookup"><span data-stu-id="6004e-188">SILVER</span></span>|<span data-ttu-id="6004e-189">S-01-0001</span><span class="sxs-lookup"><span data-stu-id="6004e-189">S-01-0001</span></span>|<span data-ttu-id="6004e-190">10</span><span class="sxs-lookup"><span data-stu-id="6004e-190">10</span></span>|  
    |<span data-ttu-id="6004e-191">LS-81</span><span class="sxs-lookup"><span data-stu-id="6004e-191">LS-81</span></span>|<span data-ttu-id="6004e-192">SILVER</span><span class="sxs-lookup"><span data-stu-id="6004e-192">SILVER</span></span>|<span data-ttu-id="6004e-193">S-01-0001</span><span class="sxs-lookup"><span data-stu-id="6004e-193">S-01-0001</span></span>|<span data-ttu-id="6004e-194">30</span><span class="sxs-lookup"><span data-stu-id="6004e-194">30</span></span>|  

    > [!NOTE]  
    >  <span data-ttu-id="6004e-195">Hólfkóðinn færist sjálfvirkt inn samkvæmt uppsetningunni sem gerð var í hlutanum „Staðsetning sett upp.“</span><span class="sxs-lookup"><span data-stu-id="6004e-195">The bin code is entered automatically according to the setup that you performed in the “Setting up the Location” section.</span></span>  

    <span data-ttu-id="6004e-196">Tilkynnið svo vöruhúsinu að innkaupapöntunin sé tilbúin til afgreiðslu í vöruhúsi þegar sendingin berst.</span><span class="sxs-lookup"><span data-stu-id="6004e-196">Proceed to notify the warehouse that the purchase order is ready for warehouse handling when the delivery arrives.</span></span>  

4.  <span data-ttu-id="6004e-197">Valið er **Losa** aðgerð.</span><span class="sxs-lookup"><span data-stu-id="6004e-197">Choose the **Release** action.</span></span>  

    <span data-ttu-id="6004e-198">Afhending hátalara frá lánardrottni 10000 hefur borist til SILVER vöruhússins og starfsmaður gengur svo frá þeim.</span><span class="sxs-lookup"><span data-stu-id="6004e-198">The delivery of loudspeakers from vendor 10000 has arrived at SILVER warehouse, and John proceeds to put them away.</span></span>  

## <a name="receiving-and-putting-the-items-away"></a><span data-ttu-id="6004e-199">Móttaka og frágangur varanna</span><span class="sxs-lookup"><span data-stu-id="6004e-199">Receiving and Putting the Items Away</span></span>  
<span data-ttu-id="6004e-200">Á síðunni **Birgðafrágangur** er hægt að meðhöndla alla virkni vöruhúss á innleið fyrir tiltekið upprunaskjal, til dæmis innkaupapöntun.</span><span class="sxs-lookup"><span data-stu-id="6004e-200">On the **Inventory Put-away** page, you can manage all inbound warehouse activities for a specific source document, such as a purchase order.</span></span>  

### <a name="to-receive-and-put-the-items-away"></a><span data-ttu-id="6004e-201">Tekið á móti og gengið frá vörunum</span><span class="sxs-lookup"><span data-stu-id="6004e-201">To receive and put the items away</span></span>  

1.  <span data-ttu-id="6004e-202">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **birgðafrágangur** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="6004e-202">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Inventory Put-aways**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="6004e-203">Valið er **Nýtt** aðgerð.</span><span class="sxs-lookup"><span data-stu-id="6004e-203">Choose the **New** action.</span></span>  
3.  <span data-ttu-id="6004e-204">Veljið reitinn **Upprunaskjal** og svo **Innkaupapöntun**.</span><span class="sxs-lookup"><span data-stu-id="6004e-204">Select the **Source Document** field, and then select **Purchase Order**.</span></span>  
4.  <span data-ttu-id="6004e-205">Veldu reitinn **Upprunanr.**, velja línuna fyrir innkaup frá viðskiptamanni 10000 og skal velja svo hnappinn **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="6004e-205">Select the **Source No.** field, select the line for the purchase from vendor 10000, and then choose the **OK** button.</span></span>  

    <span data-ttu-id="6004e-206">Að öðrum kosti, valið er **Sækja upprunaskjal** aðgerð og síðan innkaupapöntunina.</span><span class="sxs-lookup"><span data-stu-id="6004e-206">Alternatively, choose the **Get Source Document** action, and then select the purchase order.</span></span>  

5.  <span data-ttu-id="6004e-207">Velja aðgerðina **Færa sjálfkr. magn til afgr.**.</span><span class="sxs-lookup"><span data-stu-id="6004e-207">Choose the **Autofill Qty. to Handle** action.</span></span>  

    <span data-ttu-id="6004e-208">Að öðrum kosti, í reitnum **Magn til afgreiðslu** er fært inn 10 og 30 í birgðafrágangslínurnar tvær, í þeirri röð.</span><span class="sxs-lookup"><span data-stu-id="6004e-208">Alternatively, in the **Qty. to Handle** field, enter 10 and 30 respectively on the two inventory put-away lines.</span></span>  

6.  <span data-ttu-id="6004e-209">Veldu aðgerðina **Bóka**, veldu **Móttaka** aðgerðina og veldu síðan **Í lagi** hnappinn.</span><span class="sxs-lookup"><span data-stu-id="6004e-209">Choose the **Post** action, select the **Receive** action, and then choose the **OK** button.</span></span>  

    <span data-ttu-id="6004e-210">Frágangur hátalaranna 40 í hólf S-01-0001 er nú skráður og jákvæð birgðafærsla er stofnuð sem endurspeglar hina bókuðu innkaupamóttöku.</span><span class="sxs-lookup"><span data-stu-id="6004e-210">The 40 loudspeakers are now registered as put away in bin S-01-0001, and a positive item ledger entry is created reflecting the posted purchase receipt.</span></span>  

## <a name="see-also"></a><span data-ttu-id="6004e-211">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="6004e-211">See Also</span></span>  
 <span data-ttu-id="6004e-212">[Ganga frá vörum með birgðafrágangi](warehouse-how-to-put-items-away-with-inventory-put-aways.md) </span><span class="sxs-lookup"><span data-stu-id="6004e-212">[Put Items Away with Inventory Put-aways](warehouse-how-to-put-items-away-with-inventory-put-aways.md) </span></span>  
 <span data-ttu-id="6004e-213">[Setja upp einfaldar vöruhúsaaðgerðir með aðgerðasvæði](warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md) </span><span class="sxs-lookup"><span data-stu-id="6004e-213">[Set Up Basic Warehouses with Operations Areas](warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md) </span></span>  
 <span data-ttu-id="6004e-214">[Færa íhluti á aðgerðasvæði í grunnskilgreiningu vöruhúss](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md) </span><span class="sxs-lookup"><span data-stu-id="6004e-214">[Move Components to an Operation Area in Basic Warehouse Configurations](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md) </span></span>  
 <span data-ttu-id="6004e-215">[Taka til fyrir framleiðslu eða samsetningu](warehouse-how-to-pick-for-production.md) </span><span class="sxs-lookup"><span data-stu-id="6004e-215">[Pick for Production or Assembly](warehouse-how-to-pick-for-production.md) </span></span>  
 <span data-ttu-id="6004e-216">[Færa vörur eftir þörfum í einfaldri grunngerð vöruhúsa](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md) </span><span class="sxs-lookup"><span data-stu-id="6004e-216">[Move Items Ad Hoc in Basic Warehouse Configurations](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md) </span></span>  
 <span data-ttu-id="6004e-217">[Hönnunarupplýsingar: vöruhúsaflæði inn](design-details-inbound-warehouse-flow.md) </span><span class="sxs-lookup"><span data-stu-id="6004e-217">[Design Details: Inbound Warehouse Flow](design-details-inbound-warehouse-flow.md) </span></span>  
 [<span data-ttu-id="6004e-218">Kynningar á viðskiptaferli</span><span class="sxs-lookup"><span data-stu-id="6004e-218">Business Process Walkthroughs</span></span>](walkthrough-business-process-walkthroughs.md)  
 <span data-ttu-id="6004e-219">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="6004e-219">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
