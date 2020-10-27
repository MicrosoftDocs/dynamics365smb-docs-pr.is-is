---
title: Tínsla og Afhending í Einfaldar grunngerð vöruhúss | Microsoft Docs
description: Í Business Central, er hægt að framkvæma útleiðarferlið til að tína og afhenda á fjóra vegu, með því að nota mismunandi eiginleika, allt eftir flækjustigi vöruhússins.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: c05456ca45b4508be0ba44acedf81997a92b56bb
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/01/2020
ms.locfileid: "3918489"
---
# <a name="walkthrough-picking-and-shipping-in-basic-warehouse-configurations"></a><span data-ttu-id="4ede3-103">Kynning: Tínsla og Afhending í Einfaldar grunngerð vöruhúss</span><span class="sxs-lookup"><span data-stu-id="4ede3-103">Walkthrough: Picking and Shipping in Basic Warehouse Configurations</span></span>

[!INCLUDE[complete_sample_data](includes/complete_sample_data.md)]

<span data-ttu-id="4ede3-104">Í [!INCLUDE[d365fin](includes/d365fin_md.md)], er hægt að framkvæma útleiðarferlið til að tína og afhenda á fjóra vegu, með því að nota mismunandi eiginleika, allt eftir flækjustigi vöruhússins.</span><span class="sxs-lookup"><span data-stu-id="4ede3-104">In [!INCLUDE[d365fin](includes/d365fin_md.md)], the outbound processes for picking and shipping can be performed in four ways using different functionalities depending on the warehouse complexity level.</span></span>  

|<span data-ttu-id="4ede3-105">Aðferð</span><span class="sxs-lookup"><span data-stu-id="4ede3-105">Method</span></span>|<span data-ttu-id="4ede3-106">Ferli á innleið</span><span class="sxs-lookup"><span data-stu-id="4ede3-106">Inbound process</span></span>|<span data-ttu-id="4ede3-107">Hólf</span><span class="sxs-lookup"><span data-stu-id="4ede3-107">Bins</span></span>|<span data-ttu-id="4ede3-108">Tínsla</span><span class="sxs-lookup"><span data-stu-id="4ede3-108">Picks</span></span>|<span data-ttu-id="4ede3-109">Afhendingar</span><span class="sxs-lookup"><span data-stu-id="4ede3-109">Shipments</span></span>|<span data-ttu-id="4ede3-110">Flækjustig (Sjá [Hönnunarupplýsingar: uppsetning vöruhúss](design-details-warehouse-setup.md))</span><span class="sxs-lookup"><span data-stu-id="4ede3-110">Complexity level (See [Design Details: Warehouse Setup](design-details-warehouse-setup.md))</span></span>|  
|------------|---------------------|----------|-----------|---------------|--------------------------------------------------------------------------------------------------------------------|  
|<span data-ttu-id="4ede3-111">A</span><span class="sxs-lookup"><span data-stu-id="4ede3-111">A</span></span>|<span data-ttu-id="4ede3-112">Bóka tínslu og afhendingu frá pöntunarlínunni</span><span class="sxs-lookup"><span data-stu-id="4ede3-112">Post pick and shipment from the order line</span></span>|<span data-ttu-id="4ede3-113">X</span><span class="sxs-lookup"><span data-stu-id="4ede3-113">X</span></span>|||<span data-ttu-id="4ede3-114">2</span><span class="sxs-lookup"><span data-stu-id="4ede3-114">2</span></span>|  
|<span data-ttu-id="4ede3-115">Á</span><span class="sxs-lookup"><span data-stu-id="4ede3-115">B</span></span>|<span data-ttu-id="4ede3-116">Bóka tínslu og afhendingu frá birgðatínsluskjali</span><span class="sxs-lookup"><span data-stu-id="4ede3-116">Post pick and shipment from an inventory pick document</span></span>||<span data-ttu-id="4ede3-117">X</span><span class="sxs-lookup"><span data-stu-id="4ede3-117">X</span></span>||<span data-ttu-id="4ede3-118">3</span><span class="sxs-lookup"><span data-stu-id="4ede3-118">3</span></span>|  
|<span data-ttu-id="4ede3-119">C</span><span class="sxs-lookup"><span data-stu-id="4ede3-119">C</span></span>|<span data-ttu-id="4ede3-120">Bóka tínslu og afhendingu úr vöruhúsaafhendingarskjali</span><span class="sxs-lookup"><span data-stu-id="4ede3-120">Post pick and shipment from a warehouse shipment document</span></span>|||<span data-ttu-id="4ede3-121">X</span><span class="sxs-lookup"><span data-stu-id="4ede3-121">X</span></span>|<span data-ttu-id="4ede3-122">4/5/6</span><span class="sxs-lookup"><span data-stu-id="4ede3-122">4/5/6</span></span>|  
|<span data-ttu-id="4ede3-123">D</span><span class="sxs-lookup"><span data-stu-id="4ede3-123">D</span></span>|<span data-ttu-id="4ede3-124">Bóka tínslu frá vöruhúsatínsluskjali og bóka afhendingu frá vöruhúsaafhendingarskjali</span><span class="sxs-lookup"><span data-stu-id="4ede3-124">Post pick from a warehouse pick document and post shipment from a warehouse shipment document</span></span>||<span data-ttu-id="4ede3-125">X</span><span class="sxs-lookup"><span data-stu-id="4ede3-125">X</span></span>|<span data-ttu-id="4ede3-126">X</span><span class="sxs-lookup"><span data-stu-id="4ede3-126">X</span></span>|<span data-ttu-id="4ede3-127">4/5/6</span><span class="sxs-lookup"><span data-stu-id="4ede3-127">4/5/6</span></span>|  

<span data-ttu-id="4ede3-128">Nánari upplýsingar má nálgast á [Hönnunarupplýsingar: vöruhúsaflæði á útleið](design-details-outbound-warehouse-flow.md)</span><span class="sxs-lookup"><span data-stu-id="4ede3-128">For more information, see [Design Details: Outbound Warehouse Flow](design-details-outbound-warehouse-flow.md).</span></span>  

<span data-ttu-id="4ede3-129">Eftirfarandi kynning sýnir aðferð B í fyrri töflu.</span><span class="sxs-lookup"><span data-stu-id="4ede3-129">The following walkthrough demonstrates method B in the previous table.</span></span>  

## <a name="about-this-walkthrough"></a><span data-ttu-id="4ede3-130">Um kynninguna</span><span class="sxs-lookup"><span data-stu-id="4ede3-130">About This Walkthrough</span></span>

<span data-ttu-id="4ede3-131">Í grunnvöruhúsi þar sem staðsetning er sett upp þannig að krafist sé tínsluvinnslu en ekki afhendingarvinnslu skal nota síðuna **Birgðatínsla** til að skrá og bóka tínslu og afhendingarupplýsingar fyrir upprunaskjöl á útleið.</span><span class="sxs-lookup"><span data-stu-id="4ede3-131">In basic warehouse configurations where your location is set up to require pick processing but not ship processing, you use the **Inventory Pick** page to record and post pick and ship information for your outbound source documents.</span></span> <span data-ttu-id="4ede3-132">Upprunaskjalið á útleið getur verið sölupöntun, innkaupaskilapöntun, millifærslupöntun á útleið eða framleiðslupöntun með nauðsynlegum íhlutum.</span><span class="sxs-lookup"><span data-stu-id="4ede3-132">The outbound source document can be a sales order, purchase return order, outbound transfer order, or a production order with component need.</span></span>  

<span data-ttu-id="4ede3-133">Þessi kynning fjallar um eftirfarandi verk:</span><span class="sxs-lookup"><span data-stu-id="4ede3-133">This walkthrough demonstrates the following tasks:</span></span>  

- <span data-ttu-id="4ede3-134">Stilli SILVER staðsetningu fyrir birgðatínslu.</span><span class="sxs-lookup"><span data-stu-id="4ede3-134">Setting up SILVER location for inventory picks.</span></span>  
- <span data-ttu-id="4ede3-135">Stofna sölupöntun fyrir viðskiptamann 10000 fyrir 30 hátalara.</span><span class="sxs-lookup"><span data-stu-id="4ede3-135">Creating a sales order for customer 10000 for 30 loudspeakers.</span></span>  
- <span data-ttu-id="4ede3-136">Gefur út sölupöntunina fyrir afgreiðslu vöruhúss.</span><span class="sxs-lookup"><span data-stu-id="4ede3-136">Releasing the sales order for warehouse handling.</span></span>  
- <span data-ttu-id="4ede3-137">Stofna birgðatínslu byggða á útgefnu upprunaskjali.</span><span class="sxs-lookup"><span data-stu-id="4ede3-137">Creating an inventory pick based on a released source document.</span></span>  
- <span data-ttu-id="4ede3-138">Skráir vöruhúsahreyfinguna frá vöruhúsinu og bókar á sama tíma söluafhendinguna fyrir upprunaskjal sölupöntunarinnar.</span><span class="sxs-lookup"><span data-stu-id="4ede3-138">Registering the warehouse movement from the warehouse and at the same time posting the sales shipment for the source sales order.</span></span>  

## <a name="roles"></a><span data-ttu-id="4ede3-139">Hlutverk</span><span class="sxs-lookup"><span data-stu-id="4ede3-139">Roles</span></span>

<span data-ttu-id="4ede3-140">Þessi kynning sýnir þau verk sem framkvæmd eru með eftirfarandi hlutverkum notenda:</span><span class="sxs-lookup"><span data-stu-id="4ede3-140">This walkthrough demonstrates tasks that are performed by the following user roles:</span></span>  

- <span data-ttu-id="4ede3-141">Yfirmaður vöruhúss</span><span class="sxs-lookup"><span data-stu-id="4ede3-141">Warehouse Manager</span></span>  
- <span data-ttu-id="4ede3-142">Pantanavinnsla</span><span class="sxs-lookup"><span data-stu-id="4ede3-142">Order Processor</span></span>  
- <span data-ttu-id="4ede3-143">Starfsmaður í vöruhúsi</span><span class="sxs-lookup"><span data-stu-id="4ede3-143">Warehouse Worker</span></span>  

## <a name="prerequisites"></a><span data-ttu-id="4ede3-144">Frumskilyrði</span><span class="sxs-lookup"><span data-stu-id="4ede3-144">Prerequisites</span></span>

<span data-ttu-id="4ede3-145">Til að ljúka þessari kynningu þarf:</span><span class="sxs-lookup"><span data-stu-id="4ede3-145">To complete this walkthrough, you will need:</span></span>  

- <span data-ttu-id="4ede3-146">Fyrir [!INCLUDE[prodshort](includes/prodshort.md)] á netinu byggir fyrirtæki á **Ítarlegt mat - Heildarsýnigögn** valkostinn í sandkassaumhverfi.</span><span class="sxs-lookup"><span data-stu-id="4ede3-146">For [!INCLUDE[prodshort](includes/prodshort.md)] online, a company based on the **Advanced Evaluation - Complete Sample Data** option in a sandbox environment.</span></span> <span data-ttu-id="4ede3-147">Fyrir [!INCLUDE[prodshort](includes/prodshort.md)] innanhúss premises, CRONUS International Ltd. uppsett.</span><span class="sxs-lookup"><span data-stu-id="4ede3-147">For [!INCLUDE[prodshort](includes/prodshort.md)] on-premises, CRONUS International Ltd. installed.</span></span>  
- <span data-ttu-id="4ede3-148">Til að gera þig að starfsmanni vöruhúss í SILVER staðsetningu skal fylgja eftirfarandi skrefum:</span><span class="sxs-lookup"><span data-stu-id="4ede3-148">To make yourself a warehouse employee at the location SILVER by following these steps:</span></span>  

  1. <span data-ttu-id="4ede3-149">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Starfsmenn vöruhúss** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="4ede3-149">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Warehouse Employees** , and then choose the related link.</span></span>  
  2. <span data-ttu-id="4ede3-150">Velja reitinn **Notandakenni** og velja síðan eigin notandareikning notanda á síðunni **Notendur** .</span><span class="sxs-lookup"><span data-stu-id="4ede3-150">Choose the **User ID** field, and select your own user account on the **Users** page.</span></span>  
  3. <span data-ttu-id="4ede3-151">Í reitnum **Staðsetningarkóði** er fært inn SILVER.</span><span class="sxs-lookup"><span data-stu-id="4ede3-151">In the **Location Code** field, enter SILVER.</span></span>  
  4. <span data-ttu-id="4ede3-152">Veljið reitinn **Sjálfgefið** .</span><span class="sxs-lookup"><span data-stu-id="4ede3-152">Select the **Default** field.</span></span>  

- <span data-ttu-id="4ede3-153">Gerið vöru LS-81 tiltæka í SILFUR staðsetningu á eftirfarandi hátt:</span><span class="sxs-lookup"><span data-stu-id="4ede3-153">Make item LS-81 available at SILVER location by following these steps:</span></span>  

  1. <span data-ttu-id="4ede3-154">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Birgðabækur** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="4ede3-154">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Item Journals** , and then choose the related link.</span></span>  
  2. <span data-ttu-id="4ede3-155">Opnið sjálfgefnu færslubókina og stofnið tvær birgðabókarlínur með eftirfarandi upplýsingum um vinnudagsetninguna (Janúar 23).</span><span class="sxs-lookup"><span data-stu-id="4ede3-155">Open the default journal, and then create two item journal lines with the following information about the work date (January 23).</span></span>  

        |<span data-ttu-id="4ede3-156">Tegund færslu</span><span class="sxs-lookup"><span data-stu-id="4ede3-156">Entry Type</span></span>|<span data-ttu-id="4ede3-157">Vörunúmer</span><span class="sxs-lookup"><span data-stu-id="4ede3-157">Item Number</span></span>|<span data-ttu-id="4ede3-158">Kóti birgðageymslu </span><span class="sxs-lookup"><span data-stu-id="4ede3-158">Location Code</span></span>|<span data-ttu-id="4ede3-159">Hólfkóti</span><span class="sxs-lookup"><span data-stu-id="4ede3-159">Bin Code</span></span>|<span data-ttu-id="4ede3-160">Magn</span><span class="sxs-lookup"><span data-stu-id="4ede3-160">Quantity</span></span>|  
        |----------------|-----------------|-------------------|--------------|--------------|  
        |<span data-ttu-id="4ede3-161">Auking</span><span class="sxs-lookup"><span data-stu-id="4ede3-161">Positive Adjmt.</span></span>|<span data-ttu-id="4ede3-162">LS-81</span><span class="sxs-lookup"><span data-stu-id="4ede3-162">LS-81</span></span>|<span data-ttu-id="4ede3-163">SILVER</span><span class="sxs-lookup"><span data-stu-id="4ede3-163">SILVER</span></span>|<span data-ttu-id="4ede3-164">S-01-0001</span><span class="sxs-lookup"><span data-stu-id="4ede3-164">S-01-0001</span></span>|<span data-ttu-id="4ede3-165">20</span><span class="sxs-lookup"><span data-stu-id="4ede3-165">20</span></span>|  
        |<span data-ttu-id="4ede3-166">Auking</span><span class="sxs-lookup"><span data-stu-id="4ede3-166">Positive Adjmt.</span></span>|<span data-ttu-id="4ede3-167">LS-81</span><span class="sxs-lookup"><span data-stu-id="4ede3-167">LS-81</span></span>|<span data-ttu-id="4ede3-168">SILVER</span><span class="sxs-lookup"><span data-stu-id="4ede3-168">SILVER</span></span>|<span data-ttu-id="4ede3-169">S-01-0002</span><span class="sxs-lookup"><span data-stu-id="4ede3-169">S-01-0002</span></span>|<span data-ttu-id="4ede3-170">20</span><span class="sxs-lookup"><span data-stu-id="4ede3-170">20</span></span>|  

  3. <span data-ttu-id="4ede3-171">Valið er **bóka** aðgerð og síðan hnappinn **Já** .</span><span class="sxs-lookup"><span data-stu-id="4ede3-171">Choose the **Post** action, and then select the **Yes** button.</span></span>  

## <a name="story"></a><span data-ttu-id="4ede3-172">Ferill</span><span class="sxs-lookup"><span data-stu-id="4ede3-172">Story</span></span>

<span data-ttu-id="4ede3-173">Stjórnandi vöruhússins hjá CRONUS setur upp SILVER-vöruhúss fyrir grunntínslur þar sem starfsmenn vöruhússins meðhöndla pantanir á útleið hverja fyrir sig.</span><span class="sxs-lookup"><span data-stu-id="4ede3-173">Ellen, the warehouse manager at CRONUS, sets up SILVER warehouse for basic pick handling where warehouse workers process outbound orders individually.</span></span> <span data-ttu-id="4ede3-174">Sá sem vinnur pantanir, býr til sölupöntun með 30 einingum af vöru LS-81 sem afgreiða á til viðskiptamanns 10000 úr SILVER vöruhúsinu.</span><span class="sxs-lookup"><span data-stu-id="4ede3-174">Susan, the order processor, creates a sales order for 30 units of item LS-81 to be shipped to customer 10000 from the SILVER Warehouse.</span></span> <span data-ttu-id="4ede3-175">Starfsmaður vöruhússins verður að vera fullviss um að afhendingin sé tilbúin og send til viðskiptamannsins.</span><span class="sxs-lookup"><span data-stu-id="4ede3-175">John, the warehouse worker must make sure that the shipment is prepared and delivered to the customer.</span></span> <span data-ttu-id="4ede3-176">Öllum tengdum verkum er stjórnað af John á síðunni **Birgðatínsla** sem sjálfkrafa vísar í hólfin þar sem LS-81 er geymt.</span><span class="sxs-lookup"><span data-stu-id="4ede3-176">John manages all involved tasks on the **Inventory Pick** page, which automatically points to the bins where LS-81 is stored.</span></span>  

## <a name="setting-up-the-location"></a><span data-ttu-id="4ede3-177">Uppsetning staðsetningarinnar</span><span class="sxs-lookup"><span data-stu-id="4ede3-177">Setting Up the Location</span></span>

<span data-ttu-id="4ede3-178">Uppsetning síðunnar **Birgðageymsluspjald** skilgreinir vöruhúsaflæði fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="4ede3-178">The setup of the **Location Card** page defines the company’s warehouse flows.</span></span>  

### <a name="to-set-up-the-location"></a><span data-ttu-id="4ede3-179">Uppsetning staðsetningar</span><span class="sxs-lookup"><span data-stu-id="4ede3-179">To set up the location</span></span>

1. <span data-ttu-id="4ede3-180">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Staðsetningar** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="4ede3-180">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Locations** , and then choose the related link.</span></span>  
2. <span data-ttu-id="4ede3-181">SILVER-staðsetningarspjaldið er opnað.</span><span class="sxs-lookup"><span data-stu-id="4ede3-181">Open the SILVER location card.</span></span>  
3. <span data-ttu-id="4ede3-182">Á flipanum **Vöruhús** skal velja gátreitinn **Krefjast tínslu** .</span><span class="sxs-lookup"><span data-stu-id="4ede3-182">On the **Warehouse** FastTab, choose the **Require Pick** check box.</span></span>  

## <a name="creating-the-sales-order"></a><span data-ttu-id="4ede3-183">Stofna sölupöntunina</span><span class="sxs-lookup"><span data-stu-id="4ede3-183">Creating the Sales Order</span></span>

<span data-ttu-id="4ede3-184">Sölupantanir eru algengasta tegundin af upprunaskjali á útleið.</span><span class="sxs-lookup"><span data-stu-id="4ede3-184">Sales orders are the most common type of outbound source document.</span></span>  

### <a name="to-create-the-sales-order"></a><span data-ttu-id="4ede3-185">Stofna sölupöntun</span><span class="sxs-lookup"><span data-stu-id="4ede3-185">To create the sales order</span></span>

1. <span data-ttu-id="4ede3-186">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Sölupantanir** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="4ede3-186">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Orders** , and then choose the related link.</span></span>  
2. <span data-ttu-id="4ede3-187">Valið er **Nýtt** aðgerð.</span><span class="sxs-lookup"><span data-stu-id="4ede3-187">Choose the **New** action.</span></span>  
3. <span data-ttu-id="4ede3-188">Stofna sölupöntun fyrir viðskiptamann 10000 á vinnudeginum (23. Janúar) með eftirfarandi sölupöntunarlínu.</span><span class="sxs-lookup"><span data-stu-id="4ede3-188">Create a sales order for customer 10000 on the work date (January 23) with the following sales order line.</span></span>  

    |<span data-ttu-id="4ede3-189">Vara</span><span class="sxs-lookup"><span data-stu-id="4ede3-189">Item</span></span>|<span data-ttu-id="4ede3-190">Kóti birgðageymslu </span><span class="sxs-lookup"><span data-stu-id="4ede3-190">Location Code</span></span>|<span data-ttu-id="4ede3-191">Magn</span><span class="sxs-lookup"><span data-stu-id="4ede3-191">Quantity</span></span>|  
    |----|-------------|--------|  
    |<span data-ttu-id="4ede3-192">LS_81</span><span class="sxs-lookup"><span data-stu-id="4ede3-192">LS_81</span></span>|<span data-ttu-id="4ede3-193">SILVER</span><span class="sxs-lookup"><span data-stu-id="4ede3-193">SILVER</span></span>|<span data-ttu-id="4ede3-194">30</span><span class="sxs-lookup"><span data-stu-id="4ede3-194">30</span></span>|  

     <span data-ttu-id="4ede3-195">Tilkynnið svo vöruhúsinu að sölupöntunin er tilbúin til afgreiðslu í vöruhúsi þegar sendingin berst.</span><span class="sxs-lookup"><span data-stu-id="4ede3-195">Proceed to notify the warehouse that the sales order is ready for warehouse handling.</span></span>  

4. <span data-ttu-id="4ede3-196">Valið er **Losa** aðgerð.</span><span class="sxs-lookup"><span data-stu-id="4ede3-196">Choose the **Release** action.</span></span>  

    <span data-ttu-id="4ede3-197">Haldið er áfram að taka til og senda seldar vörur.</span><span class="sxs-lookup"><span data-stu-id="4ede3-197">John proceeds to pick and ship the sold items.</span></span>  

## <a name="picking-and-shipping-items"></a><span data-ttu-id="4ede3-198">Tínsla og afhending vara</span><span class="sxs-lookup"><span data-stu-id="4ede3-198">Picking and Shipping Items</span></span>

<span data-ttu-id="4ede3-199">Á síðunni **Birgðatínsla** er hægt að meðhöndla alla virkni vöruhúss á útleið fyrir tiltekið upprunaskjal, til dæmis sölupöntun.</span><span class="sxs-lookup"><span data-stu-id="4ede3-199">On the **Inventory Pick** page, you can manage all outbound warehouse activities for a specific source document, such as a sales order.</span></span> [!INCLUDE[tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]  

### <a name="to-pick-and-ship-items"></a><span data-ttu-id="4ede3-200">Til að tína og senda vörur</span><span class="sxs-lookup"><span data-stu-id="4ede3-200">To pick and ship items</span></span>

1. <span data-ttu-id="4ede3-201">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Birgðatínslur** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="4ede3-201">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Inventory Picks** , and then choose the related link.</span></span>  
2. <span data-ttu-id="4ede3-202">Valið er aðgerðin **Nýtt** .</span><span class="sxs-lookup"><span data-stu-id="4ede3-202">Choose the **New** action.</span></span>  

    <span data-ttu-id="4ede3-203">Gakktu úr skugga um að **Nr.**</span><span class="sxs-lookup"><span data-stu-id="4ede3-203">Make sure that the **No.**</span></span> <span data-ttu-id="4ede3-204">reiturinn á flýtiflipanum **Almennt** er fylltur út.</span><span class="sxs-lookup"><span data-stu-id="4ede3-204">field on the **General** FastTab is filled in.</span></span>
3. <span data-ttu-id="4ede3-205">Veljið reitinn **Upprunaskjal** og svo **Sölupöntun** .</span><span class="sxs-lookup"><span data-stu-id="4ede3-205">Select the **Source Document** field, and then select **Sales Order** .</span></span>  
4. <span data-ttu-id="4ede3-206">Veldu reitinn **Upprunanr.** , velja línuna fyrir sölu til viðskiptamanns 10000 og skal velja svo hnappinn **Í lagi** .</span><span class="sxs-lookup"><span data-stu-id="4ede3-206">Select the **Source No.** field, select the line for the sale to customer 10000, and then choose the **OK** button.</span></span>  

    <span data-ttu-id="4ede3-207">Að öðrum kosti, valið er **Sækja upprunaskjal** aðgerð og síðan sölupöntun.</span><span class="sxs-lookup"><span data-stu-id="4ede3-207">Alternatively, choose the **Get Source Document** action, and then select the sales order.</span></span>  
5. <span data-ttu-id="4ede3-208">Velja aðgerðina **Færa sjálfkr. magn til afgr.** .</span><span class="sxs-lookup"><span data-stu-id="4ede3-208">Choose the **Autofill Qty. to Handle** action.</span></span>  

    <span data-ttu-id="4ede3-209">Að öðrum kosti, í reitnum **Magn til afgreiðslu** er fært inn 10 og 20 í birgðatínslulínurnar tvær, í þeirri röð.</span><span class="sxs-lookup"><span data-stu-id="4ede3-209">Alternatively, in the **Qty. to Handle** field, enter 10 and 20 respectively on the two inventory pick lines.</span></span>  
6. <span data-ttu-id="4ede3-210">Veldu aðgerðina **Bóka** , veldu **Afhenda** og veldu síðan **Í lagi** hnappinn.</span><span class="sxs-lookup"><span data-stu-id="4ede3-210">Choose the **Post** action, select **Ship** , and then choose the **OK** button.</span></span>  

    <span data-ttu-id="4ede3-211">Tínsla hátalaranna 30 úr hólfum S-01-0001 og S-01-0002 er nú skráð og neikvæð birgðafærsla er stofnuð sem endurspeglar hina bókuðu söluafhendingu.</span><span class="sxs-lookup"><span data-stu-id="4ede3-211">The 30 loudspeakers are now registered as picked from bins S-01-0001 and S-01-0002, and a negative item ledger entry is created reflecting the posted sales shipment.</span></span>  

## <a name="see-also"></a><span data-ttu-id="4ede3-212">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="4ede3-212">See Also</span></span>

[<span data-ttu-id="4ede3-213">Vörur tíndar með birgðatínslu</span><span class="sxs-lookup"><span data-stu-id="4ede3-213">Pick Items with Inventory Picks</span></span>](warehouse-how-to-pick-items-with-inventory-picks.md)  
[<span data-ttu-id="4ede3-214">Tína vörur fyrir vöruhúsaafhendingu</span><span class="sxs-lookup"><span data-stu-id="4ede3-214">Pick Items for Warehouse Shipment</span></span>](warehouse-how-to-pick-items-for-warehouse-shipment.md)  
[<span data-ttu-id="4ede3-215">Setja upp einfaldar vöruhúsaaðgerðir með aðgerðasvæði</span><span class="sxs-lookup"><span data-stu-id="4ede3-215">Set Up Basic Warehouses with Operations Areas</span></span>](warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md)  
[<span data-ttu-id="4ede3-216">Færa íhluti á aðgerðasvæði í grunnskilgreiningu vöruhúss</span><span class="sxs-lookup"><span data-stu-id="4ede3-216">Move Components to an Operation Area in Basic Warehouse Configurations</span></span>](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md)  
[<span data-ttu-id="4ede3-217">Taka til fyrir framleiðslu eða samsetningu</span><span class="sxs-lookup"><span data-stu-id="4ede3-217">Pick for Production or Assembly</span></span>](warehouse-how-to-pick-for-production.md)  
[<span data-ttu-id="4ede3-218">Færa vörur eftir þörfum í einfaldri grunngerð vöruhúsa</span><span class="sxs-lookup"><span data-stu-id="4ede3-218">Move Items Ad Hoc in Basic Warehouse Configurations</span></span>](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md)  
[<span data-ttu-id="4ede3-219">Hönnunarupplýsingar: vöruhúsaflæði á innleið</span><span class="sxs-lookup"><span data-stu-id="4ede3-219">Design Details: Outbound Warehouse Flow</span></span>](design-details-outbound-warehouse-flow.md)  
[<span data-ttu-id="4ede3-220">Kynningar á viðskiptaferli</span><span class="sxs-lookup"><span data-stu-id="4ede3-220">Business Process Walkthroughs</span></span>](walkthrough-business-process-walkthroughs.md)  
<span data-ttu-id="4ede3-221">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="4ede3-221">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
