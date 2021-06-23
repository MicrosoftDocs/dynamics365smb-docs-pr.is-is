---
title: Tínsla og Afhending í einfaldar grunngerðir vöruhúss
description: Í Business Central, er hægt að framkvæma útleiðarferlið til að tína og afhenda á fjóra vegu, með því að nota mismunandi eiginleika, allt eftir flækjustigi vöruhússins.
author: jill-kotel-andersson
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 05/27/2021
ms.author: edupont
ms.openlocfilehash: e1763e6288c8b8218955049ba7ef4c461ee5164e
ms.sourcegitcommit: 0953171d39e1232a7c126142d68cac858234a20e
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/09/2021
ms.locfileid: "6214654"
---
# <a name="walkthrough-picking-and-shipping-in-basic-warehouse-configurations"></a><span data-ttu-id="95166-103">Kynning: Tínsla og Afhending í Einfaldar grunngerð vöruhúss</span><span class="sxs-lookup"><span data-stu-id="95166-103">Walkthrough: Picking and Shipping in Basic Warehouse Configurations</span></span>

<!-- [!INCLUDE[complete_sample_data](includes/complete_sample_data.md)] -->

<span data-ttu-id="95166-104">Í [!INCLUDE[prod_short](includes/prod_short.md)], er hægt að framkvæma útleiðarferlið til að tína og afhenda á fjóra vegu, með því að nota mismunandi eiginleika, allt eftir flækjustigi vöruhússins.</span><span class="sxs-lookup"><span data-stu-id="95166-104">In [!INCLUDE[prod_short](includes/prod_short.md)], the outbound processes for picking and shipping can be performed in four ways using different functionalities depending on the warehouse complexity level.</span></span>  

|<span data-ttu-id="95166-105">Aðferð</span><span class="sxs-lookup"><span data-stu-id="95166-105">Method</span></span>|<span data-ttu-id="95166-106">Ferli á innleið</span><span class="sxs-lookup"><span data-stu-id="95166-106">Inbound process</span></span>|<span data-ttu-id="95166-107">Hólf</span><span class="sxs-lookup"><span data-stu-id="95166-107">Bins</span></span>|<span data-ttu-id="95166-108">Tínsla</span><span class="sxs-lookup"><span data-stu-id="95166-108">Picks</span></span>|<span data-ttu-id="95166-109">Afhendingar</span><span class="sxs-lookup"><span data-stu-id="95166-109">Shipments</span></span>|<span data-ttu-id="95166-110">Flækjustig (Sjá [Hönnunarupplýsingar: uppsetning vöruhúss](design-details-warehouse-setup.md))</span><span class="sxs-lookup"><span data-stu-id="95166-110">Complexity level (See [Design Details: Warehouse Setup](design-details-warehouse-setup.md))</span></span>|  
|------------|---------------------|----------|-----------|---------------|--------------------------------------------------------------------------------------------------------------------|  
|<span data-ttu-id="95166-111">A</span><span class="sxs-lookup"><span data-stu-id="95166-111">A</span></span>|<span data-ttu-id="95166-112">Bóka tínslu og afhendingu frá pöntunarlínunni</span><span class="sxs-lookup"><span data-stu-id="95166-112">Post pick and shipment from the order line</span></span>|<span data-ttu-id="95166-113">X</span><span class="sxs-lookup"><span data-stu-id="95166-113">X</span></span>|||<span data-ttu-id="95166-114">2</span><span class="sxs-lookup"><span data-stu-id="95166-114">2</span></span>|  
|<span data-ttu-id="95166-115">Á</span><span class="sxs-lookup"><span data-stu-id="95166-115">B</span></span>|<span data-ttu-id="95166-116">Bóka tínslu og afhendingu frá birgðatínsluskjali</span><span class="sxs-lookup"><span data-stu-id="95166-116">Post pick and shipment from an inventory pick document</span></span>||<span data-ttu-id="95166-117">X</span><span class="sxs-lookup"><span data-stu-id="95166-117">X</span></span>||<span data-ttu-id="95166-118">3</span><span class="sxs-lookup"><span data-stu-id="95166-118">3</span></span>|  
|<span data-ttu-id="95166-119">C</span><span class="sxs-lookup"><span data-stu-id="95166-119">C</span></span>|<span data-ttu-id="95166-120">Bóka tínslu og afhendingu úr vöruhúsaafhendingarskjali</span><span class="sxs-lookup"><span data-stu-id="95166-120">Post pick and shipment from a warehouse shipment document</span></span>|||<span data-ttu-id="95166-121">X</span><span class="sxs-lookup"><span data-stu-id="95166-121">X</span></span>|<span data-ttu-id="95166-122">4/5/6</span><span class="sxs-lookup"><span data-stu-id="95166-122">4/5/6</span></span>|  
|<span data-ttu-id="95166-123">D</span><span class="sxs-lookup"><span data-stu-id="95166-123">D</span></span>|<span data-ttu-id="95166-124">Bóka tínslu frá vöruhúsatínsluskjali og bóka afhendingu frá vöruhúsaafhendingarskjali</span><span class="sxs-lookup"><span data-stu-id="95166-124">Post pick from a warehouse pick document and post shipment from a warehouse shipment document</span></span>||<span data-ttu-id="95166-125">X</span><span class="sxs-lookup"><span data-stu-id="95166-125">X</span></span>|<span data-ttu-id="95166-126">X</span><span class="sxs-lookup"><span data-stu-id="95166-126">X</span></span>|<span data-ttu-id="95166-127">4/5/6</span><span class="sxs-lookup"><span data-stu-id="95166-127">4/5/6</span></span>|  

<span data-ttu-id="95166-128">Nánari upplýsingar má nálgast á [Hönnunarupplýsingar: vöruhúsaflæði á útleið](design-details-outbound-warehouse-flow.md)</span><span class="sxs-lookup"><span data-stu-id="95166-128">For more information, see [Design Details: Outbound Warehouse Flow](design-details-outbound-warehouse-flow.md).</span></span>  

<span data-ttu-id="95166-129">Eftirfarandi kynning sýnir aðferð B í fyrri töflu.</span><span class="sxs-lookup"><span data-stu-id="95166-129">The following walkthrough demonstrates method B in the previous table.</span></span>  

## <a name="about-this-walkthrough"></a><span data-ttu-id="95166-130">Um kynninguna</span><span class="sxs-lookup"><span data-stu-id="95166-130">About This Walkthrough</span></span>

<span data-ttu-id="95166-131">Í grunnvöruhúsi þar sem staðsetning er sett upp þannig að krafist sé tínsluvinnslu en ekki afhendingarvinnslu skal nota síðuna **Birgðatínsla** til að skrá og bóka tínslu og afhendingarupplýsingar fyrir upprunaskjöl á útleið.</span><span class="sxs-lookup"><span data-stu-id="95166-131">In basic warehouse configurations where your location is set up to require pick processing but not ship processing, you use the **Inventory Pick** page to record and post pick and ship information for your outbound source documents.</span></span> <span data-ttu-id="95166-132">Upprunaskjalið á útleið getur verið sölupöntun, innkaupaskilapöntun, millifærslupöntun á útleið eða framleiðslupöntun með nauðsynlegum íhlutum.</span><span class="sxs-lookup"><span data-stu-id="95166-132">The outbound source document can be a sales order, purchase return order, outbound transfer order, or a production order with component need.</span></span>  

<span data-ttu-id="95166-133">Þessi kynning fjallar um eftirfarandi verk:</span><span class="sxs-lookup"><span data-stu-id="95166-133">This walkthrough demonstrates the following tasks:</span></span>  

- <span data-ttu-id="95166-134">Stilli staðsetningu SUÐUR fyrir birgðatínslu.</span><span class="sxs-lookup"><span data-stu-id="95166-134">Setting up SOUTH location for inventory picks.</span></span>  
- <span data-ttu-id="95166-135">Stofna sölupöntun fyrir viðskiptamann 10000 fyrir 30 Amsterdam Lamps.</span><span class="sxs-lookup"><span data-stu-id="95166-135">Creating a sales order for customer 10000 for 30 Amsterdam Lamps.</span></span>  
- <span data-ttu-id="95166-136">Gefur út sölupöntunina fyrir afgreiðslu vöruhúss.</span><span class="sxs-lookup"><span data-stu-id="95166-136">Releasing the sales order for warehouse handling.</span></span>  
- <span data-ttu-id="95166-137">Stofna birgðatínslu byggða á útgefnu upprunaskjali.</span><span class="sxs-lookup"><span data-stu-id="95166-137">Creating an inventory pick based on a released source document.</span></span>  
- <span data-ttu-id="95166-138">Skráir vöruhúsahreyfinguna frá vöruhúsinu og bókar á sama tíma söluafhendinguna fyrir upprunaskjal sölupöntunarinnar.</span><span class="sxs-lookup"><span data-stu-id="95166-138">Registering the warehouse movement from the warehouse and at the same time posting the sales shipment for the source sales order.</span></span>  

## <a name="roles"></a><span data-ttu-id="95166-139">Hlutverk</span><span class="sxs-lookup"><span data-stu-id="95166-139">Roles</span></span>

<span data-ttu-id="95166-140">Þessi kynning sýnir þau verk sem framkvæmd eru með eftirfarandi hlutverkum notenda:</span><span class="sxs-lookup"><span data-stu-id="95166-140">This walkthrough demonstrates tasks that are performed by the following user roles:</span></span>  

- <span data-ttu-id="95166-141">Yfirmaður vöruhúss</span><span class="sxs-lookup"><span data-stu-id="95166-141">Warehouse Manager</span></span>  
- <span data-ttu-id="95166-142">Pantanavinnsla</span><span class="sxs-lookup"><span data-stu-id="95166-142">Order Processor</span></span>  
- <span data-ttu-id="95166-143">Starfsmaður í vöruhúsi</span><span class="sxs-lookup"><span data-stu-id="95166-143">Warehouse Worker</span></span>  

<!-- ## Prerequisites

To complete this walkthrough, you will need:  

- For [!INCLUDE[prod_short](includes/prod_short.md)] online, a company based on the **Advanced Evaluation - Complete Sample Data** option in a sandbox environment. For [!INCLUDE[prod_short](includes/prod_short.md)] on-premises, CRONUS installed.
 -->

## <a name="story"></a><span data-ttu-id="95166-144">Ferill</span><span class="sxs-lookup"><span data-stu-id="95166-144">Story</span></span>

<span data-ttu-id="95166-145">Stjórnandi vöruhússins hjá CRONUS setur upp SUÐUR-vöruhús fyrir grunntínslur þar sem starfsmenn vöruhússins meðhöndla pantanir á útleið hverja fyrir sig.</span><span class="sxs-lookup"><span data-stu-id="95166-145">Ellen, the warehouse manager at CRONUS, sets up SOUTH warehouse for basic pick handling where warehouse workers process outbound orders individually.</span></span> <span data-ttu-id="95166-146">Sá sem vinnur pantanir, býr til sölupöntun með 30 einingum af vöru 1928-S sem afgreiða á til viðskiptamanns 10000 úr SUÐUR vöruhúsinu.</span><span class="sxs-lookup"><span data-stu-id="95166-146">Susan, the order processor, creates a sales order for 30 units of item 1928-S to be shipped to customer 10000 from the SOUTH Warehouse.</span></span> <span data-ttu-id="95166-147">Starfsmaður vöruhússins verður að vera fullviss um að afhendingin sé tilbúin og send til viðskiptamannsins.</span><span class="sxs-lookup"><span data-stu-id="95166-147">John, the warehouse worker must make sure that the shipment is prepared and delivered to the customer.</span></span> <span data-ttu-id="95166-148">Öllum tengdum verkum er stjórnað af John á síðunni **Birgðatínsla** sem sjálfkrafa vísar í hólfin þar sem 1928-S er geymt.</span><span class="sxs-lookup"><span data-stu-id="95166-148">John manages all involved tasks on the **Inventory Pick** page, which automatically points to the bins where 1928-S is stored.</span></span>

[!INCLUDE[set_up_location.md](includes/set_up_location.md)]

### <a name="setting-up-the-bin-codes"></a><span data-ttu-id="95166-149">Uppsetning hólfakóða</span><span class="sxs-lookup"><span data-stu-id="95166-149">Setting Up the Bin Codes</span></span>
<span data-ttu-id="95166-150">Þegar staðsetningin hefur verið sett upp verður að bæta tveimur hólfum við.</span><span class="sxs-lookup"><span data-stu-id="95166-150">Once you have the location set up, you must add two bins.</span></span>

#### <a name="to-setup-the-bin-codes"></a><span data-ttu-id="95166-151">Til að setja upp hólfakóðana</span><span class="sxs-lookup"><span data-stu-id="95166-151">To setup the bin codes</span></span>

1. <span data-ttu-id="95166-152">Veldu aðgerðina **Hólf**.</span><span class="sxs-lookup"><span data-stu-id="95166-152">Select the **Bins** action.</span></span>
2. <span data-ttu-id="95166-153">Búðu til tvö hólf, með kóðunum *S-01-0001* og *S-01-0002*.</span><span class="sxs-lookup"><span data-stu-id="95166-153">Create two bins, with the codes *S-01-0001* and *S-01-0002*.</span></span>

### <a name="making-yourself-a-warehouse-employee-at-location-south"></a><span data-ttu-id="95166-154">Að gera sig að vöruhúsastarfsmanni á staðsetningunni SUÐUR</span><span class="sxs-lookup"><span data-stu-id="95166-154">Making Yourself a Warehouse Employee at Location SOUTH</span></span>

<span data-ttu-id="95166-155">Til að nota þessa aðgerð verður þú að bæta við þig staðsetningu sem starfskraftur í vöruhúsi.</span><span class="sxs-lookup"><span data-stu-id="95166-155">In order to use this functionality, you must add yourself to the location as a warehouse worker.</span></span> 

#### <a name="to-make-yourself-a-warehouse-employee"></a><span data-ttu-id="95166-156">Til að gera þig að starfsmanni vöruhúss</span><span class="sxs-lookup"><span data-stu-id="95166-156">To make yourself a warehouse employee</span></span>

  1. <span data-ttu-id="95166-157">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar fyrsta](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Starfsmenn vöruhúss** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="95166-157">Choose the ![Lightbulb that opens the Tell Me feature first](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Warehouse Employees**, and then choose the related link.</span></span>  
  2. <span data-ttu-id="95166-158">Veldu reitinn **Notandakenni** og síðan eigin notandareikning á síðunni **Starfsmaður vöruhúss**.</span><span class="sxs-lookup"><span data-stu-id="95166-158">Choose the **User ID** field, and select your own user account on the **Warehouse Employees** page.</span></span>
  3. <span data-ttu-id="95166-159">Í reitnum **Staðsetningarkóði** velur þú SUÐUR.</span><span class="sxs-lookup"><span data-stu-id="95166-159">In the **Location Code** field, choose SOUTH.</span></span>  
  4. <span data-ttu-id="95166-160">Veldu reitinn **Sjálfgefið** og síðan hnappinn **Já**.</span><span class="sxs-lookup"><span data-stu-id="95166-160">Select the **Default** field, and then select the **Yes** button.</span></span>  

### <a name="making-item-1928-s-available"></a><span data-ttu-id="95166-161">Gera hlut 1928-S tiltækan</span><span class="sxs-lookup"><span data-stu-id="95166-161">Making Item 1928-S Available</span></span>

<span data-ttu-id="95166-162">Til að gera hlut 1928-S aðgengilegan á SUÐUR staðsetningunni skal fylgja þessum skrefum:</span><span class="sxs-lookup"><span data-stu-id="95166-162">To make item 1928-S available at the SOUTH location follow these steps:</span></span>  

  1. <span data-ttu-id="95166-163">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar annað](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Birgðabækur** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="95166-163">Choose the ![Lightbulb that opens the Tell Me feature second](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Item Journals**, and then choose the related link.</span></span>  
  2. <span data-ttu-id="95166-164">Opnið sjálfgefnu færslubókina og stofnið tvær birgðabókarlínur með eftirfarandi upplýsingum um vinnudagsetninguna (Janúar 23).</span><span class="sxs-lookup"><span data-stu-id="95166-164">Open the default journal, and then create two item journal lines with the following information about the work date (January 23).</span></span>  

        |<span data-ttu-id="95166-165">Tegund færslu</span><span class="sxs-lookup"><span data-stu-id="95166-165">Entry Type</span></span>|<span data-ttu-id="95166-166">Vörunúmer</span><span class="sxs-lookup"><span data-stu-id="95166-166">Item Number</span></span>|<span data-ttu-id="95166-167">Kóti birgðageymslu </span><span class="sxs-lookup"><span data-stu-id="95166-167">Location Code</span></span>|<span data-ttu-id="95166-168">Hólfkóti</span><span class="sxs-lookup"><span data-stu-id="95166-168">Bin Code</span></span>|<span data-ttu-id="95166-169">Magn</span><span class="sxs-lookup"><span data-stu-id="95166-169">Quantity</span></span>|  
        |----------------|-----------------|-------------------|--------------|--------------|  
        |<span data-ttu-id="95166-170">Auking</span><span class="sxs-lookup"><span data-stu-id="95166-170">Positive Adjmt.</span></span>|<span data-ttu-id="95166-171">1928-S</span><span class="sxs-lookup"><span data-stu-id="95166-171">1928-S</span></span>|<span data-ttu-id="95166-172">SUÐUR</span><span class="sxs-lookup"><span data-stu-id="95166-172">SOUTH</span></span>|<span data-ttu-id="95166-173">S-01-0001</span><span class="sxs-lookup"><span data-stu-id="95166-173">S-01-0001</span></span>|<span data-ttu-id="95166-174">20</span><span class="sxs-lookup"><span data-stu-id="95166-174">20</span></span>|  
        |<span data-ttu-id="95166-175">Auking</span><span class="sxs-lookup"><span data-stu-id="95166-175">Positive Adjmt.</span></span>|<span data-ttu-id="95166-176">1928-S</span><span class="sxs-lookup"><span data-stu-id="95166-176">1928-S</span></span>|<span data-ttu-id="95166-177">SUÐUR</span><span class="sxs-lookup"><span data-stu-id="95166-177">SOUTH</span></span>|<span data-ttu-id="95166-178">S-01-0002</span><span class="sxs-lookup"><span data-stu-id="95166-178">S-01-0002</span></span>|<span data-ttu-id="95166-179">20</span><span class="sxs-lookup"><span data-stu-id="95166-179">20</span></span>|  

        <span data-ttu-id="95166-180">Sjálfgefið er að **Hólfakóði** á sölulínunni sé falinn og því þarf að kalla hann fram.</span><span class="sxs-lookup"><span data-stu-id="95166-180">By default, the **Bin Code** field on the sales lines are hidden, so you must display it.</span></span> <span data-ttu-id="95166-181">Til að gera þetta þarftu að sérstilla síðuna.</span><span class="sxs-lookup"><span data-stu-id="95166-181">To do this you need to personalize the page.</span></span> <span data-ttu-id="95166-182">Frekari upplýsingar eru í [Hefja sérstillingu á síðu með borðanum Sérstilla](ui-personalization-user.md#to-start-personalizing-a-page-through-the-personalizing-banner).</span><span class="sxs-lookup"><span data-stu-id="95166-182">For more information, see [To start personalizing a page through the Personalizing banner](ui-personalization-user.md#to-start-personalizing-a-page-through-the-personalizing-banner).</span></span>

  3. <span data-ttu-id="95166-183">Veldu **Aðgerðir**, smelltu síðan á **Bókun** og smella síðan á **Bóka**.</span><span class="sxs-lookup"><span data-stu-id="95166-183">Choose **Actions**, then **Posting**, and then choose **Post**.</span></span>  
  4. <span data-ttu-id="95166-184">Velja hnappinn **Já**.</span><span class="sxs-lookup"><span data-stu-id="95166-184">Select the **Yes** button.</span></span>  

## <a name="creating-the-sales-order"></a><span data-ttu-id="95166-185">Stofna sölupöntunina</span><span class="sxs-lookup"><span data-stu-id="95166-185">Creating the Sales Order</span></span>

<span data-ttu-id="95166-186">Sölupantanir eru algengasta tegundin af upprunaskjali á útleið.</span><span class="sxs-lookup"><span data-stu-id="95166-186">Sales orders are the most common type of outbound source document.</span></span>  

### <a name="to-create-the-sales-order"></a><span data-ttu-id="95166-187">Stofna sölupöntun</span><span class="sxs-lookup"><span data-stu-id="95166-187">To create the sales order</span></span>

1. <span data-ttu-id="95166-188">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar þriðja](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Sölupantanir** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="95166-188">Choose the ![Lightbulb that opens the Tell Me feature third](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Orders**, and then choose the related link.</span></span>  
2. <span data-ttu-id="95166-189">Valið er **Nýtt** aðgerð.</span><span class="sxs-lookup"><span data-stu-id="95166-189">Choose the **New** action.</span></span>  
3. <span data-ttu-id="95166-190">Stofna sölupöntun fyrir viðskiptamann 10000 á vinnudeginum (23. Janúar) með eftirfarandi sölupöntunarlínu.</span><span class="sxs-lookup"><span data-stu-id="95166-190">Create a sales order for customer 10000 on the work date (January 23) with the following sales order line.</span></span>  

    |<span data-ttu-id="95166-191">Vara</span><span class="sxs-lookup"><span data-stu-id="95166-191">Item</span></span>|<span data-ttu-id="95166-192">Kóti birgðageymslu </span><span class="sxs-lookup"><span data-stu-id="95166-192">Location Code</span></span>|<span data-ttu-id="95166-193">Magn</span><span class="sxs-lookup"><span data-stu-id="95166-193">Quantity</span></span>|  
    |----|-------------|--------|  
    |<span data-ttu-id="95166-194">1928-S</span><span class="sxs-lookup"><span data-stu-id="95166-194">1928-S</span></span>|<span data-ttu-id="95166-195">SUÐUR</span><span class="sxs-lookup"><span data-stu-id="95166-195">SOUTH</span></span>|<span data-ttu-id="95166-196">30</span><span class="sxs-lookup"><span data-stu-id="95166-196">30</span></span>|  

     <span data-ttu-id="95166-197">Tilkynnið svo vöruhúsinu að sölupöntunin er tilbúin til afgreiðslu í vöruhúsi þegar sendingin berst.</span><span class="sxs-lookup"><span data-stu-id="95166-197">Proceed to notify the warehouse that the sales order is ready for warehouse handling.</span></span>  

4. <span data-ttu-id="95166-198">Valið er **Losa** aðgerð.</span><span class="sxs-lookup"><span data-stu-id="95166-198">Choose the **Release** action.</span></span>  

    <span data-ttu-id="95166-199">Haldið er áfram að taka til og senda seldar vörur.</span><span class="sxs-lookup"><span data-stu-id="95166-199">John proceeds to pick and ship the sold items.</span></span>  

## <a name="picking-and-shipping-items"></a><span data-ttu-id="95166-200">Tínsla og afhending vara</span><span class="sxs-lookup"><span data-stu-id="95166-200">Picking and Shipping Items</span></span>

<span data-ttu-id="95166-201">Á síðunni **Birgðatínsla** er hægt að meðhöndla alla virkni vöruhúss á útleið fyrir tiltekið upprunaskjal, til dæmis sölupöntun.</span><span class="sxs-lookup"><span data-stu-id="95166-201">On the **Inventory Pick** page, you can manage all outbound warehouse activities for a specific source document, such as a sales order.</span></span> [!INCLUDE[tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]  

### <a name="to-pick-and-ship-items"></a><span data-ttu-id="95166-202">Til að tína og senda vörur</span><span class="sxs-lookup"><span data-stu-id="95166-202">To pick and ship items</span></span>

1. <span data-ttu-id="95166-203">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar fjórða](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Birgðatínslur** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="95166-203">Choose the ![Lightbulb that opens the Tell Me feature fourth](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Inventory Picks**, and then choose the related link.</span></span>  
2. <span data-ttu-id="95166-204">Valið er aðgerðin **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="95166-204">Choose the **New** action.</span></span>  

    <span data-ttu-id="95166-205">Gakktu úr skugga um að **Nr.**</span><span class="sxs-lookup"><span data-stu-id="95166-205">Make sure that the **No.**</span></span> <span data-ttu-id="95166-206">reiturinn á flýtiflipanum **Almennt** er fylltur út.</span><span class="sxs-lookup"><span data-stu-id="95166-206">field on the **General** FastTab is filled in.</span></span>
3. <span data-ttu-id="95166-207">Veljið reitinn **Upprunaskjal** og svo **Sölupöntun**.</span><span class="sxs-lookup"><span data-stu-id="95166-207">Select the **Source Document** field, and then select **Sales Order**.</span></span>  
4. <span data-ttu-id="95166-208">Veldu reitinn **Upprunanr.**, velja línuna fyrir sölu til viðskiptamanns 10000 og skal velja svo hnappinn **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="95166-208">Select the **Source No.** field, select the line for the sale to customer 10000, and then choose the **OK** button.</span></span>  

    <span data-ttu-id="95166-209">Að öðrum kosti, valið er **Sækja upprunaskjal** aðgerð og síðan sölupöntun.</span><span class="sxs-lookup"><span data-stu-id="95166-209">Alternatively, choose the **Get Source Document** action, and then select the sales order.</span></span>  
5. <span data-ttu-id="95166-210">Velja aðgerðina **Færa sjálfkr. magn til afgr.**.</span><span class="sxs-lookup"><span data-stu-id="95166-210">Choose the **Autofill Qty. to Handle** action.</span></span>  

    <span data-ttu-id="95166-211">Að öðrum kosti, í reitnum **Magn til afgreiðslu** er fært inn 10 og 20 í birgðatínslulínurnar tvær, í þeirri röð.</span><span class="sxs-lookup"><span data-stu-id="95166-211">Alternatively, in the **Qty. to Handle** field, enter 10 and 20 respectively on the two inventory pick lines.</span></span>  
6. <span data-ttu-id="95166-212">Veldu aðgerðina **Bóka**, veldu **Afhenda** og veldu síðan **Í lagi** hnappinn.</span><span class="sxs-lookup"><span data-stu-id="95166-212">Choose the **Post** action, select **Ship**, and then choose the **OK** button.</span></span>  

    <span data-ttu-id="95166-213">30 Amsterdam Lamps eru nú skráðir sem teknir til úr hólfum S-01-0001 og S-01-0002 er nú skráð og neikvæð birgðafærsla er stofnuð sem endurspeglar hina bókuðu söluafhendingu.</span><span class="sxs-lookup"><span data-stu-id="95166-213">The 30 Amsterdam Lamps are now registered as picked from bins S-01-0001 and S-01-0002, and a negative item ledger entry is created reflecting the posted sales shipment.</span></span>  

## <a name="see-also"></a><span data-ttu-id="95166-214">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="95166-214">See Also</span></span>

[<span data-ttu-id="95166-215">Vörur tíndar með birgðatínslu</span><span class="sxs-lookup"><span data-stu-id="95166-215">Pick Items with Inventory Picks</span></span>](warehouse-how-to-pick-items-with-inventory-picks.md)  
[<span data-ttu-id="95166-216">Tína vörur fyrir vöruhúsaafhendingu</span><span class="sxs-lookup"><span data-stu-id="95166-216">Pick Items for Warehouse Shipment</span></span>](warehouse-how-to-pick-items-for-warehouse-shipment.md)  
[<span data-ttu-id="95166-217">Setja upp einfaldar vöruhúsaaðgerðir með aðgerðasvæði</span><span class="sxs-lookup"><span data-stu-id="95166-217">Set Up Basic Warehouses with Operations Areas</span></span>](warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md)  
[<span data-ttu-id="95166-218">Færa íhluti á aðgerðasvæði í grunnskilgreiningu vöruhúss</span><span class="sxs-lookup"><span data-stu-id="95166-218">Move Components to an Operation Area in Basic Warehouse Configurations</span></span>](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md)  
[<span data-ttu-id="95166-219">Taka til fyrir framleiðslu eða samsetningu</span><span class="sxs-lookup"><span data-stu-id="95166-219">Pick for Production or Assembly</span></span>](warehouse-how-to-pick-for-production.md)  
[<span data-ttu-id="95166-220">Færa vörur eftir þörfum í einfaldri grunngerð vöruhúsa</span><span class="sxs-lookup"><span data-stu-id="95166-220">Move Items Ad Hoc in Basic Warehouse Configurations</span></span>](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md)  
[<span data-ttu-id="95166-221">Hönnunarupplýsingar: vöruhúsaflæði á innleið</span><span class="sxs-lookup"><span data-stu-id="95166-221">Design Details: Outbound Warehouse Flow</span></span>](design-details-outbound-warehouse-flow.md)  
[<span data-ttu-id="95166-222">Kynningar á viðskiptaferli</span><span class="sxs-lookup"><span data-stu-id="95166-222">Business Process Walkthroughs</span></span>](walkthrough-business-process-walkthroughs.md)  
<span data-ttu-id="95166-223">[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="95166-223">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  


[!INCLUDE[footer-include](includes/footer-banner.md)]
