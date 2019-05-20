---
title: Bókunardagsetning á virðisfærslum
description: Lærðu hvernig runuvinnslan Leiðréttur kostnaður - birgðafærslur ber kennsl á og úthlutar bókunardagsetningu fyrir virðisfærslurnar sem runuvinnslan er að búa til.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: edupont
ms.openlocfilehash: b08864a4cf7f7f198d692a6658ae437856860a51
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/29/2019
ms.locfileid: "1247560"
---
# <a name="design-details-posting-date-on-adjustment-value-entry"></a><span data-ttu-id="19d72-103">Hönnunarupplýsingar: Bókunardagsetning á leiðréttingarvirðisfærslu</span><span class="sxs-lookup"><span data-stu-id="19d72-103">Design Details: Posting Date on Adjustment Value Entry</span></span>
<span data-ttu-id="19d72-104">Þessi grein veitir leiðbeiningar fyrir notendur birgðakostnaðarvirkni í [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="19d72-104">This article provides guidance for users of the Inventory Costing functionality in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="19d72-105">Tilgreind grein veitir leiðbeiningar um hvernig runuvinnslan **Leiðréttur kostnaður - Birgðafærslur** ber kennsl á og úthlutar bókunardagsetningu fyrir virðisfærslurnar sem runuvinnslan er að búa til.</span><span class="sxs-lookup"><span data-stu-id="19d72-105">The specific article is providing guidance in how the **Adjust Cost - Item Entries** batch job identifies and assigns a posting date to the value entries that the batch job is about to create.</span></span>  

<span data-ttu-id="19d72-106">Fyrst er hugmynd ferlisins yfirfarin, hvernig runuvinnslan ber kennsl á og úthlutar bókunardagsetningu fyrir virðisfærsluna sem verður búin til.</span><span class="sxs-lookup"><span data-stu-id="19d72-106">First the concept of the process is reviewed, how the batch job identifies and assigns the Posting Date to the Value Entry to be created.</span></span> <span data-ttu-id="19d72-107">Eftir það eru nokkrar aðstæður sem við í stuðningshópnum rekumst á af og til og að lokum er samantekt yfir hugtökin sem eru notuð í útgáfu 3.0.</span><span class="sxs-lookup"><span data-stu-id="19d72-107">Thereafter there are some scenarios shared that we in the support team come across from time to time and finally there is a summary of the concepts used from version 3.0.</span></span>  

## <a name="the-concept"></a><span data-ttu-id="19d72-108">Hugtakið</span><span class="sxs-lookup"><span data-stu-id="19d72-108">The Concept</span></span>  
<span data-ttu-id="19d72-109">Frá útgáfu 5.0, runuvinnslan **Leiðrétta kostnað - Birgðafærslur** úthlutar bókunardagsetningu fyrir virðisfærsluna sem hún kemur til með að búa til í eftirfarandi skrefum:</span><span class="sxs-lookup"><span data-stu-id="19d72-109">From version 5.0, the **Adjust Cost – Item Entries** batch job assigns a posting date to the value entry it is about to create in the following steps:</span></span>  

1.  <span data-ttu-id="19d72-110">Upphaflega er bókunardagsetning færslunnar sem á að búa til sú sama og dagsetning færslunnar sem hún leiðréttir.</span><span class="sxs-lookup"><span data-stu-id="19d72-110">Initially the Posting Date of the entry to be created is the same date as the entry it adjusts.</span></span>  

2.  <span data-ttu-id="19d72-111">Bókunardagsetningin er sannprófuð gagnvart birgðatímabili og/eða fjárhagsgrunni.</span><span class="sxs-lookup"><span data-stu-id="19d72-111">The Posting Date is validated against Inventory Periods and/or General Ledger Setup.</span></span>  

3.  <span data-ttu-id="19d72-112">Úthlutun bókunardagsetningu; Ef upphafleg bókunardagsetning er ekki innan leyfilegs dagsetningabils bókunar, þá mun runuvinnslan úthluta leyfilegri bókunardagsetningu frá annað hvort fjárhagsgrunni eða birgðatímabili.</span><span class="sxs-lookup"><span data-stu-id="19d72-112">Assignment of Posting Date; If the initial Posting Date is not within allowed posting date range the batch job will assign an allowed Posting Date from either General Ledger Setup or Inventory Period.</span></span> <span data-ttu-id="19d72-113">Ef bæði birgðatímabil og leyfileg bókunardagsetning í fjárhagsgrunni eru skilgreind, verður síðari dagsetning þessara tveggja úthlutað til leiðréttingarvirðisfærslu.</span><span class="sxs-lookup"><span data-stu-id="19d72-113">If both Inventory Periods and allowed posting dates in General Ledger Setup are defined, the later date of the two will be assigned to the Adjustment Value Entry.</span></span>  

 <span data-ttu-id="19d72-114">Við skulum yfirfara þetta ferli betur með dæmi.</span><span class="sxs-lookup"><span data-stu-id="19d72-114">Let’s review this process more in practice.</span></span> <span data-ttu-id="19d72-115">Gerum ráð fyrir að við séum með birgðafærslu fyrir sölu.</span><span class="sxs-lookup"><span data-stu-id="19d72-115">Assume we have an Item Ledger Entry of Sale.</span></span> <span data-ttu-id="19d72-116">Þessi hlutur var sendur 5. september 2013 og reikningsfærður daginn eftir.</span><span class="sxs-lookup"><span data-stu-id="19d72-116">The item was shipped on September 5th, 2013 and it was invoiced the day after.</span></span>  

<span data-ttu-id="19d72-117">![Staða birgðahöfuðbókarfærslna í atburðarásinni](media/helene/TechArticleAdjustcost1.png "Staða birgðahöfuðbókarfærslna í atburðarásinni")</span><span class="sxs-lookup"><span data-stu-id="19d72-117">![State of item ledger entries in the scenario](media/helene/TechArticleAdjustcost1.png "State of item ledger entries in the scenario")</span></span>  

<span data-ttu-id="19d72-118">Hér að neðan táknar fyrsta virðisfærslan (379) sendinguna og bera þær sömu bókunardagsetningu og yfirbirgðafærslan.</span><span class="sxs-lookup"><span data-stu-id="19d72-118">Below, the first Value Entry (379) represents the shipment and carry the same Posting Date as the parent Item ledger Entry.</span></span>  

<span data-ttu-id="19d72-119">Önnur virðisfærslan (381) táknar reikninginn.</span><span class="sxs-lookup"><span data-stu-id="19d72-119">The second Value Entry (381) represents the invoice.</span></span>  

 <span data-ttu-id="19d72-120">Þriðja virðisfærslan (391) er leiðrétting á reikningsfærðri virðisfærslu (381)</span><span class="sxs-lookup"><span data-stu-id="19d72-120">The third Value Entry (391) is an Adjustment of the invoicing Value Entry (381)</span></span>  

 <span data-ttu-id="19d72-121">![Staða virðisfærslna í atburðarás](media/helene/TechArticleAdjustcost2.png "Staða virðisfærslna í atburðarás")</span><span class="sxs-lookup"><span data-stu-id="19d72-121">![State of value entries in the scenario](media/helene/TechArticleAdjustcost2.png "State of value entries in the scenario")</span></span>  

 <span data-ttu-id="19d72-122">Skref 1: Leiðréttingarvirðisfærsla sem á að búa til er úthlutað sömu bókunardagsetningu og færslan sem hún leiðréttir, sýnt hér að framan með virðisfærslu 391.</span><span class="sxs-lookup"><span data-stu-id="19d72-122">Step 1: Adjustment Value Entry to be created is assigned same Posting Date as the entry it adjusts, illustrated above by Value entry 391.</span></span>  

 <span data-ttu-id="19d72-123">Skref 2: Villuleit á upphaflega úthlutaðri bókunardagsetningu.</span><span class="sxs-lookup"><span data-stu-id="19d72-123">Step 2: Validation of initial assigned Posting Date.</span></span>  

<span data-ttu-id="19d72-124">Runuvinnslan **Leiðrétta kostnað - Birgðafærslur** ákvarðar hvort upphafleg bókunardagsetning fyrir leiðréttingarvirðisfærslu er innan leyfilegs dagsetningabils bókunar byggt á birgðatímabili og/eða fjárhagsgrunni.</span><span class="sxs-lookup"><span data-stu-id="19d72-124">The **Adjust Cost – Item Entries** batch job determines if the initial Posting Date of the Adjustment Value Entry is within allowed posting date range based upon Inventory Periods and/or General Ledger Setup.</span></span>  

 <span data-ttu-id="19d72-125">Við skulum endurskoða ofangreinda sölu með því að bæta við uppsetningu á leyfilegu dagsetningabili bókunar.</span><span class="sxs-lookup"><span data-stu-id="19d72-125">Let’s review the above mentioned Sale by adding setup of allowed posting date ranges.</span></span>  

 <span data-ttu-id="19d72-126">Birgðatímabil:</span><span class="sxs-lookup"><span data-stu-id="19d72-126">Inventory Periods:</span></span>  

<span data-ttu-id="19d72-127">![Birgðahaldstími í atburðarásinni](media/helene/TechArticleAdjustcost3.png "Birgðahaldstími í atburðarásinni")</span><span class="sxs-lookup"><span data-stu-id="19d72-127">![Inventory periods in the scenario](media/helene/TechArticleAdjustcost3.png "Inventory periods in the scenario")</span></span>

 <span data-ttu-id="19d72-128">Fyrsta leyfilega bókunardagsetning er fyrsta daginn í fyrsta opna tímabilinu.</span><span class="sxs-lookup"><span data-stu-id="19d72-128">First allowed posting date is the first day in the first open period.</span></span> <span data-ttu-id="19d72-129">1. september 2013.</span><span class="sxs-lookup"><span data-stu-id="19d72-129">September 1st, 2013.</span></span>  

 <span data-ttu-id="19d72-130">Uppsetning fjárhags:</span><span class="sxs-lookup"><span data-stu-id="19d72-130">General Ledger Setup:</span></span>  

<span data-ttu-id="19d72-131">![Uppsetning fjárhags í atburðarásinni](media/helene/TechArticleAdjustcost4.png "Uppsetning fjárhags í atburðarásinni")</span><span class="sxs-lookup"><span data-stu-id="19d72-131">![G/L Setup in the scenario](media/helene/TechArticleAdjustcost4.png "G/L Setup in the scenario")</span></span>

 <span data-ttu-id="19d72-132">Fyrsta leyfilega bókunardagsetning er dagsetningin sem tilgreind er í reitnum Leyfa bókanir frá: 10. september 2013.</span><span class="sxs-lookup"><span data-stu-id="19d72-132">First allowed posting date is the date stated in field Allow Posting From: September 10th, 2013.</span></span>  

 <span data-ttu-id="19d72-133">Ef bæði birgðatímabil og leyfilegar bókunardagsetningar í fjárhagsgrunni eru skilgreind mun síðari dagsetning þessara tveggja skilgreina leyfilegt dagsetningabil bókunar.</span><span class="sxs-lookup"><span data-stu-id="19d72-133">If both Inventory Periods and allowed posting dates in General Ledger Setup are defined, the later date of the two will define the allowed posting date range.</span></span>  

 <span data-ttu-id="19d72-134">Skref 3: Úthlutun á leyfilegri bókunardagsetningu;</span><span class="sxs-lookup"><span data-stu-id="19d72-134">Step 3: Assignment of an allowed posting date;</span></span>  

 <span data-ttu-id="19d72-135">Upphaflega úthlutaða bókunardagsetningin var 6. september eins og sýnt er í skrefi 1.</span><span class="sxs-lookup"><span data-stu-id="19d72-135">The initial assigned Posting Date was September 6th as illustrated in step 1.</span></span> <span data-ttu-id="19d72-136">Í 2. skrefi ber runuvinnslan Leiðrétta kostnað - Birgðafærslur kennsl 10. september sem fyrstu leyfilegu bókunardagsetninguna og úthlutar þess vegna 10. september á leiðréttingarvirðisfærsluna fyrir neðan.</span><span class="sxs-lookup"><span data-stu-id="19d72-136">However, in the 2nd step the Adjust Cost – Item entries batch job identifies that earliest allowed Posting Date is September 10th and thereby assigns September 10th to the Adjustment Value Entry, below.</span></span>  

 <span data-ttu-id="19d72-137">![Staða virðisfærslna í atburðarás 2](media/helene/TechArticleAdjustcost5.png "Staða virðisfærslna í atburðarás 2")</span><span class="sxs-lookup"><span data-stu-id="19d72-137">![State of value entries in the scenario 2](media/helene/TechArticleAdjustcost5.png "State of value entries in the scenario 2")</span></span>

 <span data-ttu-id="19d72-138">Við höfum nú yfirfarið hugtakið fyrir úthlutun bókunardagsetninga á virðisfærslur sem eru búnar til af runuvinnslu Leiðrétts kostnaðar - Birgðafærslna.</span><span class="sxs-lookup"><span data-stu-id="19d72-138">We have now reviewed the concept for assigning Posting Dates to Value Entries created by the Adjust Cost - Item entries batch job.</span></span>  

 <span data-ttu-id="19d72-139">Við skulum halda áfram að yfirfara sumar aðstæður sem við í stuðningshópnum rekumst á af og til í tengslum við úthlutaðar bókunardagsetningar í runuvinnslu Leiðrétts kostnaðar - Birgðafærslna og tengdum uppsetningum.</span><span class="sxs-lookup"><span data-stu-id="19d72-139">Let’s continue to review some scenarios that we in the support team comes across from time to time in relation to assigned Posting Dates in the Adjust Cost – Item entries batch job and related setups.</span></span>  

## <a name="scenarios"></a><span data-ttu-id="19d72-140">Dæmi</span><span class="sxs-lookup"><span data-stu-id="19d72-140">Scenarios</span></span>  

### <a name="scenario-i-posting-date-is-not-within-your-range-of-allowed-posting-dates"></a><span data-ttu-id="19d72-141">Aðstæður I: „Bókunardagsetning er ekki innan marka leyfilegra bókunardagsetninga...“</span><span class="sxs-lookup"><span data-stu-id="19d72-141">Scenario I: “Posting Date is not within your range of allowed posting dates…”</span></span>  
 <span data-ttu-id="19d72-142">Þetta eru aðstæður þar sem notandi fær upp umrædd villuboð þegar runuvinnsla Leiðrétts kostnaðar - Birgðafærsla er keyrð.</span><span class="sxs-lookup"><span data-stu-id="19d72-142">This is a scenario where a user is experiencing mentioned error message when the Adjust Cost – Item entries batch job is run.</span></span>  

 <span data-ttu-id="19d72-143">Í fyrri kafla, sem lýsir hugmyndinni um að gefa út bókunardagsetningar, er ætlunin með runuvinnslu Leiðrétts kostnaðar - Birgðafærslna að búa til virðisfærslu með bókunardagsetninguna 10. september.</span><span class="sxs-lookup"><span data-stu-id="19d72-143">In the previous section, describing the concept of assigning posting dates, the intention of the Adjust Cost – Item entries batch job is to create a Value Entry with Posting Date September 10th.</span></span>  

<span data-ttu-id="19d72-144">![Villuboð um bókunardagsetningu](media/helene/TechArticleAdjustcost6.png "Villuboð um bókunardagsetningu")</span><span class="sxs-lookup"><span data-stu-id="19d72-144">![Error message about posting date](media/helene/TechArticleAdjustcost6.png "Error message about posting date")</span></span>

 <span data-ttu-id="19d72-145">Við fylgjum eftir notandauppsetningu:</span><span class="sxs-lookup"><span data-stu-id="19d72-145">We follow up on the User Setup:</span></span>  

<span data-ttu-id="19d72-146">![Uppsetning heimilaðra bókunardagsetninga fyrir notanda](media/helene/TechArticleAdjustcost7.png "Uppsetning heimilaðra bókunardagsetninga fyrir notanda")</span><span class="sxs-lookup"><span data-stu-id="19d72-146">![User's allowed posting dates setup](media/helene/TechArticleAdjustcost7.png "User's allowed posting dates setup")</span></span>

 <span data-ttu-id="19d72-147">Notandinn í þessu tilfelli hefur leyfilegt dagsetningabil bókunar frá 11. september til 30. september og er því ekki heimilt að bóka leiðréttingarvirðisfærsluna með bókunardagsetninguna 10. september.</span><span class="sxs-lookup"><span data-stu-id="19d72-147">The user in this case has an allowed posting date range from September 11th to September 30th and is thereby not allowed to post the Adjustment Value Entry with Posting Date September 10th.</span></span>  

<span data-ttu-id="19d72-148">![Yfirlit yfir virka uppsetningu bókunardagsetningar](media/helene/TechArticleAdjustcost8.png "Yfirlit yfir virka uppsetningu bókunardagsetningar")</span><span class="sxs-lookup"><span data-stu-id="19d72-148">![Overview of involved posting date setup](media/helene/TechArticleAdjustcost8.png "Overview of involved posting date setup")</span></span>

 <span data-ttu-id="19d72-149">Grein þekkingargrunns [952996](https://mbs2.microsoft.com/Knowledgebase/kbdisplay.aspx?WTNTZSMNWUKNTMMYXUPYZQPOUXNXSPSYOQQYYMLUQLOYYMWP) fjallar um fleiri aðstæður sem tengjast nefndu villuboði.</span><span class="sxs-lookup"><span data-stu-id="19d72-149">Knowledge Base article [952996](https://mbs2.microsoft.com/Knowledgebase/kbdisplay.aspx?WTNTZSMNWUKNTMMYXUPYZQPOUXNXSPSYOQQYYMLUQLOYYMWP) discusses additional scenarios related to mentioned error message.</span></span>  

### <a name="scenario-ii-posting-date-on-adjustment-value-entry-versus-posting-date-on-entry-causing-the-adjustment-such-as-revaluation-or-item-charge"></a><span data-ttu-id="19d72-150">Aðstæður II: Bókunardagsetning á leiðréttingarvirðisfærslum á móti bókunardagsetningu við innfærslu sem veldur leiðréttingu, eins og endurmati eða kostnaðarauka.</span><span class="sxs-lookup"><span data-stu-id="19d72-150">Scenario II: Posting Date on Adjustment Value Entry versus Posting Date on entry causing the adjustment such as Revaluation or Item charge.</span></span>  

### <a name="revaluation-scenario"></a><span data-ttu-id="19d72-151">Aðstæður endurmats:</span><span class="sxs-lookup"><span data-stu-id="19d72-151">Revaluation scenario:</span></span>  
 <span data-ttu-id="19d72-152">Skilyrði:</span><span class="sxs-lookup"><span data-stu-id="19d72-152">Prerequisites:</span></span>  

 <span data-ttu-id="19d72-153">Birgðagrunnur:</span><span class="sxs-lookup"><span data-stu-id="19d72-153">Inventory setup:</span></span>  

-   <span data-ttu-id="19d72-154">Sjálfvirk kostnaðarbókun = Já</span><span class="sxs-lookup"><span data-stu-id="19d72-154">Automatic Cost Posting = Yes</span></span>  

-   <span data-ttu-id="19d72-155">Sjálfvirk kostnaðarleiðrétting=Alltaf</span><span class="sxs-lookup"><span data-stu-id="19d72-155">Automatic Cost Adjustment=Always</span></span>  

-   <span data-ttu-id="19d72-156">Meðalkostnaður Teg. útreikn=vara</span><span class="sxs-lookup"><span data-stu-id="19d72-156">Average Cost Calc. Type=item</span></span>  

-   <span data-ttu-id="19d72-157">Meðalkostnaðartímabil=Dagur</span><span class="sxs-lookup"><span data-stu-id="19d72-157">Average Cost Period=Day</span></span>  

 <span data-ttu-id="19d72-158">Uppsetning fjárhags:</span><span class="sxs-lookup"><span data-stu-id="19d72-158">General Ledger Setup:</span></span>  

-   <span data-ttu-id="19d72-159">Bókun leyfð frá = 1. janúar 2014</span><span class="sxs-lookup"><span data-stu-id="19d72-159">Allow Posting From = January 1st, 2014</span></span>  

-   <span data-ttu-id="19d72-160">Bókun leyfð til = tómt</span><span class="sxs-lookup"><span data-stu-id="19d72-160">Allow Posting To = empty</span></span>  

 <span data-ttu-id="19d72-161">Notandauppsetning:</span><span class="sxs-lookup"><span data-stu-id="19d72-161">User Setup:</span></span>  

-   <span data-ttu-id="19d72-162">Bókun leyfð frá = 1. desember 2013.</span><span class="sxs-lookup"><span data-stu-id="19d72-162">Allow Posting From = December 1st, 2013.</span></span>  

-   <span data-ttu-id="19d72-163">Bókun leyfð til = tómt</span><span class="sxs-lookup"><span data-stu-id="19d72-163">Allow Posting to = empty</span></span>  

##### <a name="to-test-the-scenario"></a><span data-ttu-id="19d72-164">Að prófa aðstæðurnar</span><span class="sxs-lookup"><span data-stu-id="19d72-164">To test the scenario</span></span>  

1.  <span data-ttu-id="19d72-165">Stofna TEST vöru:</span><span class="sxs-lookup"><span data-stu-id="19d72-165">Create item TEST:</span></span>  

     <span data-ttu-id="19d72-166">Grunnmælieining = STK</span><span class="sxs-lookup"><span data-stu-id="19d72-166">Base unit of measure = PCS</span></span>  

     <span data-ttu-id="19d72-167">Kostnaðarútreikningur = Meðaltal</span><span class="sxs-lookup"><span data-stu-id="19d72-167">Costing Method = Average</span></span>  

     <span data-ttu-id="19d72-168">Velja valkvæða bókunarflokka.</span><span class="sxs-lookup"><span data-stu-id="19d72-168">Select optional posting groups.</span></span>  

2.  <span data-ttu-id="19d72-169">Opna birgðabók, stofna og bóka línu á eftirfarandi hátt:</span><span class="sxs-lookup"><span data-stu-id="19d72-169">Open Item Journal, create and post a line as follows:</span></span>  

     <span data-ttu-id="19d72-170">Bókunardagsetning = 15. desember, 2013</span><span class="sxs-lookup"><span data-stu-id="19d72-170">Posting Date = December 15th, 2013</span></span>  

     <span data-ttu-id="19d72-171">Vara = TEST</span><span class="sxs-lookup"><span data-stu-id="19d72-171">Item = TEST</span></span>  

     <span data-ttu-id="19d72-172">Tegund færslu = Innkaup</span><span class="sxs-lookup"><span data-stu-id="19d72-172">Entry Type = Purchase</span></span>  

     <span data-ttu-id="19d72-173">Magn = 100</span><span class="sxs-lookup"><span data-stu-id="19d72-173">Quantity = 100</span></span>  

     <span data-ttu-id="19d72-174">Ein.upphæð = 10</span><span class="sxs-lookup"><span data-stu-id="19d72-174">Unit Amount = 10</span></span>  

3.  <span data-ttu-id="19d72-175">Opna birgðabók, stofna og bóka línu á eftirfarandi hátt:</span><span class="sxs-lookup"><span data-stu-id="19d72-175">Open Item Journal, create and post a line as follows:</span></span>  

     <span data-ttu-id="19d72-176">Dagsetning = 20. desember 2013</span><span class="sxs-lookup"><span data-stu-id="19d72-176">Date = December 20th, 2013</span></span>  

     <span data-ttu-id="19d72-177">Vara = TEST</span><span class="sxs-lookup"><span data-stu-id="19d72-177">Item = TEST</span></span>  

     <span data-ttu-id="19d72-178">Tegund færslu = Neikvæð leiðrétting</span><span class="sxs-lookup"><span data-stu-id="19d72-178">Entry Type = Negative Adjustment</span></span>  

     <span data-ttu-id="19d72-179">Magn = 2</span><span class="sxs-lookup"><span data-stu-id="19d72-179">Quantity = 2</span></span>  

4.  <span data-ttu-id="19d72-180">Opna birgðabók, stofna og bóka línu á eftirfarandi hátt:</span><span class="sxs-lookup"><span data-stu-id="19d72-180">Open Item Journal, create and post a line as follows:</span></span>  

     <span data-ttu-id="19d72-181">Dagsetning = 15. janúar 2014</span><span class="sxs-lookup"><span data-stu-id="19d72-181">Date = January 15th, 2014</span></span>  

     <span data-ttu-id="19d72-182">Vara = TEST</span><span class="sxs-lookup"><span data-stu-id="19d72-182">Item = TEST</span></span>  

     <span data-ttu-id="19d72-183">Tegund færslu = Neikvæð leiðrétting</span><span class="sxs-lookup"><span data-stu-id="19d72-183">Entry Type = Negative Adjustment</span></span>  

     <span data-ttu-id="19d72-184">Magn = 3</span><span class="sxs-lookup"><span data-stu-id="19d72-184">Quantity = 3</span></span>  

5.  <span data-ttu-id="19d72-185">Opna endurmatsbók, stofna og bóka línu á eftirfarandi hátt:</span><span class="sxs-lookup"><span data-stu-id="19d72-185">Open Revaluation Journal, create and post a line as follows:</span></span>  

     <span data-ttu-id="19d72-186">Vara = TEST</span><span class="sxs-lookup"><span data-stu-id="19d72-186">Item = TEST</span></span>  

     <span data-ttu-id="19d72-187">Gildir-fyrir færslu = veldu innkaupafærsla bókuð í skrefi 2.</span><span class="sxs-lookup"><span data-stu-id="19d72-187">Applies-to Entry = select Purchase entry posted at step 2.</span></span> <span data-ttu-id="19d72-188">Bókunardagsetning endurmats verður sú sama og fyrir færsluna sem hún leiðréttir.</span><span class="sxs-lookup"><span data-stu-id="19d72-188">The Posting Date of the revaluation will be the same as the entry it adjusts.</span></span>  

     <span data-ttu-id="19d72-189">Kostnaðarverð endurmetið = 40</span><span class="sxs-lookup"><span data-stu-id="19d72-189">Unit Cost Revalued = 40</span></span>  

 <span data-ttu-id="19d72-190">Eftirfarandi birgðahöfuðbók og virðisfærslur hafa verið bókaðar:</span><span class="sxs-lookup"><span data-stu-id="19d72-190">The following Item Ledger and Value Entries have been posted:</span></span>  

<span data-ttu-id="19d72-191">![Yfirlit yfir birgðahöfuðbók og virðisfærslur 1 sem urðu til](media/helene/TechArticleAdjustcost9.png "Yfirlit yfir birgðahöfuðbók og virðisfærslur 1 sem urðu til")</span><span class="sxs-lookup"><span data-stu-id="19d72-191">![Overview of resulting item ledger and value entries 1](media/helene/TechArticleAdjustcost9.png "Overview of resulting item ledger and value entries 1")</span></span>

 <span data-ttu-id="19d72-192">![Yfirlit yfir birgðahöfuðbók og virðisfærslur sem urðu til 2](media/helene/TechArticleAdjustcost10.png "Yfirlit yfir birgðahöfuðbók og virðisfærslur sem urðu til 2")</span><span class="sxs-lookup"><span data-stu-id="19d72-192">![Overview of resulting item ledger and value entries 2](media/helene/TechArticleAdjustcost10.png "Overview of resulting item ledger and value entries 2")</span></span>

 <span data-ttu-id="19d72-193">Runuvinnslan Leiðréttur kostnaður - Birgðafærslur hefur borið kennsl á breytingar á kostnaði og leiðrétti neikvæðu leiðréttingarnar.</span><span class="sxs-lookup"><span data-stu-id="19d72-193">The Adjust Cost – Item entries batch job has recognized a change in cost and adjusted the Negative Adjustments.</span></span>  

 <span data-ttu-id="19d72-194">**Endurskoðun bókunardagsetninga á stofnuðum leiðréttingarvirðisfærslum:** Fyrstu leyfilegu bókunardagsetningar sem runuvinnslan Leiðréttur kostnaður - Birgðafærslur verður að tengjast er 1. janúar 2014 eins kemur fram í fjárhagsgrunni.</span><span class="sxs-lookup"><span data-stu-id="19d72-194">**Review of Posting Dates on created Adjustment Value Entries:** The earliest allowed Posting Date the Adjust Cost - Item Entries batch job has to relate to is January 1st, 2014 as stated in the General Ledger Setup.</span></span>  

 <span data-ttu-id="19d72-195">**Neikvæð leiðrétting í skrefi 3:** úthlutuð bókunardagsetning er 1. janúar, veitt af fjárhagsgrunni.</span><span class="sxs-lookup"><span data-stu-id="19d72-195">**Negative Adjustment in step 3:** assigned Posting Date is January 1st, provided by General Ledger Setup.</span></span> <span data-ttu-id="19d72-196">Bókunardagsetning virðisfærslunnar sem heyrir undir leiðréttingu er 20. desember 2013.</span><span class="sxs-lookup"><span data-stu-id="19d72-196">The Posting Date of the Value Entry in scope for adjustment is December 20, 2013.</span></span> <span data-ttu-id="19d72-197">Samkvæmt fjárhagsgrunni er dagsetningin ekki innan leyfilegs dagsetningabils bókunar.</span><span class="sxs-lookup"><span data-stu-id="19d72-197">According to General Ledger Setup the date is not within allowed posting date range.</span></span> <span data-ttu-id="19d72-198">Þess vegna er bókunardagsetningunni, sem er nefnd í Bókun leyfð frá reit fjárhagsgrunns, úthlutað á leiðrétttingarvirðisfærsluna.</span><span class="sxs-lookup"><span data-stu-id="19d72-198">Therefore the Posting Date stated in the Allow Posting From field in the General Ledger Setup is assigned to the Adjustment Value Entry.</span></span>  

 <span data-ttu-id="19d72-199">**Neikvæð leiðrétting í skrefi 4:** úthlutuð bókunardagsetning er 15. janúar.</span><span class="sxs-lookup"><span data-stu-id="19d72-199">**Negative Adjustment in step 4:** assigned Posting Date is January 15th.</span></span> <span data-ttu-id="19d72-200">Virðisfærslan sem heyrir undir leiðréttingu er með bókunardagsetninguna 15. janúar, sem er innan leyfilegs dagsetningabils bókunar samkvæmt fjárhagsgrunni.</span><span class="sxs-lookup"><span data-stu-id="19d72-200">The Value Entry in scope of adjustment has Posting Date January 15th, which is within the allowed posting date range according to General Ledger Setup.</span></span>  

 <span data-ttu-id="19d72-201">Leiðréttingin sem gerð var fyrir neikvæðu leiðréttinguna í skrefi 3 veldur umræðu.</span><span class="sxs-lookup"><span data-stu-id="19d72-201">The adjustment made for the Negative Adjustment in step 3 causes discussion.</span></span> <span data-ttu-id="19d72-202">Hagstæða bókunardagsetningin fyrir leiðréttingarvirðisfærsluna hefði verið 20. desember eða að minnsta kosti í desember þar sem endurmatið sem olli breytingunni á kostnaði seldrar vöru var bókað í desember.</span><span class="sxs-lookup"><span data-stu-id="19d72-202">The favorable Posting Date for the Adjustment Value Entry would have been December 20th or at least within December as the revaluation causing the change in COGS was posted in December.</span></span>  

 <span data-ttu-id="19d72-203">Til að ná leiðréttingu í desember á neikvæðu leiðréttingunni í 3. skrefi þarf fjárhagsgrunnurinn, Bókun leyfð frá reit, að tilgreina dagsetningu í desember.</span><span class="sxs-lookup"><span data-stu-id="19d72-203">To achieve adjustment in December of the Negative Adjustment in step 3, the General Ledger Setup, Allow Posting From field, need to state a date in December.</span></span>  

 <span data-ttu-id="19d72-204">**Niðurstaða:**</span><span class="sxs-lookup"><span data-stu-id="19d72-204">**Conclusion:**</span></span>  

 <span data-ttu-id="19d72-205">Með reynslu af þessari atburðarás, miðað við hentugastu uppsetningu leyfilegs dagsetningabils bókunar fyrir fyrirtæki, gæti eftirfarandi verið gagnlegt: Svo lengi sem er heimilt að bóka breytingar á birgðaverðmæti á tímabili, desember í þessu tilviki, ætti uppsetningin sem fyrirtækið notar fyrir dagsetningabil sem er leyfilegt að bóka að vera í takt við þessa ákvörðun.</span><span class="sxs-lookup"><span data-stu-id="19d72-205">With the experiences from this scenario, considering most suitable setup of allowed posting date range for a company, the following might be useful: As long as changes in inventory value is allowed to be posted in a period, December in this case, the setup the company uses for allowed posting date ranges should be aligned with this decision.</span></span> <span data-ttu-id="19d72-206">Bókun leyfð frá í fjárhagsgrunni, þar sem fram kemur 1. desember, myndi leyfa að áframsenda endurmatið sem gert var í desember á færslur á útleið, sem verða fyrir áhrifum, á sama tímabilinu.</span><span class="sxs-lookup"><span data-stu-id="19d72-206">The Allow Posting From in the General Ledger Setup, stating December 1st  would allow the revaluation made in December to be forwarded to affected outbound entries in the same period.</span></span>  

 <span data-ttu-id="19d72-207">Notendahópar sem ekki mega bóka í desember en í janúar, sem fjárhagsgrunnur átti líklega að takmarka í þessum aðstæðum, ætti frekar að staðsetja í notandauppsetningu.</span><span class="sxs-lookup"><span data-stu-id="19d72-207">User groups not allowed to post in December but in January, which was probably intended to be limited by the General Ledger Setup in this scenario, should instead be addressed via the User setup.</span></span>  

### <a name="item-charge-scenario"></a><span data-ttu-id="19d72-208">Aðstæður kostnaðarauka:</span><span class="sxs-lookup"><span data-stu-id="19d72-208">Item charge scenario:</span></span>  
 <span data-ttu-id="19d72-209">Skilyrði:</span><span class="sxs-lookup"><span data-stu-id="19d72-209">Prerequisites:</span></span>  

 <span data-ttu-id="19d72-210">Birgðagrunnur:</span><span class="sxs-lookup"><span data-stu-id="19d72-210">Inventory setup:</span></span>  

-   <span data-ttu-id="19d72-211">Sjálfvirk kostnaðarbókun = Já</span><span class="sxs-lookup"><span data-stu-id="19d72-211">Automatic Cost Posting = Yes</span></span>  

-   <span data-ttu-id="19d72-212">Sjálfvirk kostnaðarleiðrétting=Alltaf</span><span class="sxs-lookup"><span data-stu-id="19d72-212">Automatic Cost Adjustment=Always</span></span>  

-   <span data-ttu-id="19d72-213">Meðalkostnaður Teg. útreikn=vara</span><span class="sxs-lookup"><span data-stu-id="19d72-213">Average Cost Calc. Type=item</span></span>  

-   <span data-ttu-id="19d72-214">Meðalkostnaðartímabil=Dagur</span><span class="sxs-lookup"><span data-stu-id="19d72-214">Average Cost Period=Day</span></span>  

 <span data-ttu-id="19d72-215">Uppsetning fjárhags:</span><span class="sxs-lookup"><span data-stu-id="19d72-215">General Ledger Setup:</span></span>  

-   <span data-ttu-id="19d72-216">Bókun leyfð frá = 1. desember 2013.</span><span class="sxs-lookup"><span data-stu-id="19d72-216">Allow Posting From = December 1st, 2013.</span></span>  

-   <span data-ttu-id="19d72-217">Bókun leyfð til = tómt</span><span class="sxs-lookup"><span data-stu-id="19d72-217">Allow Posting To = empty</span></span>  

 <span data-ttu-id="19d72-218">Notandauppsetning:</span><span class="sxs-lookup"><span data-stu-id="19d72-218">User Setup:</span></span>  

-   <span data-ttu-id="19d72-219">Bókun leyfð frá = 1. desember 2013.</span><span class="sxs-lookup"><span data-stu-id="19d72-219">Allow Posting From = December 1st, 2013.</span></span>  

-   <span data-ttu-id="19d72-220">Bókun leyfð til = tómt</span><span class="sxs-lookup"><span data-stu-id="19d72-220">Allow Posting to = empty</span></span>  

##### <a name="to-test-the-scenario"></a><span data-ttu-id="19d72-221">Að prófa aðstæðurnar</span><span class="sxs-lookup"><span data-stu-id="19d72-221">To test the scenario</span></span>  

1.  <span data-ttu-id="19d72-222">Stofna kostnaðarauka:</span><span class="sxs-lookup"><span data-stu-id="19d72-222">Create item charge:</span></span>  

     <span data-ttu-id="19d72-223">Grunnmælieining = STK</span><span class="sxs-lookup"><span data-stu-id="19d72-223">Base unit of measure = PCS</span></span>  

     <span data-ttu-id="19d72-224">Kostnaðarútreikningur = Meðaltal</span><span class="sxs-lookup"><span data-stu-id="19d72-224">Costing Method = Average</span></span>  

     <span data-ttu-id="19d72-225">Velja valkvæða bókunarflokka.</span><span class="sxs-lookup"><span data-stu-id="19d72-225">Select optional posting groups.</span></span>  

2.  <span data-ttu-id="19d72-226">Stofna nýja innkaupapöntun</span><span class="sxs-lookup"><span data-stu-id="19d72-226">Create new purchase order</span></span>  

     <span data-ttu-id="19d72-227">Kaupa af lánardrottni nr.: 10000</span><span class="sxs-lookup"><span data-stu-id="19d72-227">Buy-from Vendor No.: 10000</span></span>  

     <span data-ttu-id="19d72-228">Bókunardagsetning = 15. desember, 2013</span><span class="sxs-lookup"><span data-stu-id="19d72-228">Posting Date = December 15th, 2013</span></span>  

     <span data-ttu-id="19d72-229">Reikningsnr. lánardrottins: 1234</span><span class="sxs-lookup"><span data-stu-id="19d72-229">Vendor Invoice No.: 1234</span></span>  

     <span data-ttu-id="19d72-230">Á innkaupapöntunarlínunni:</span><span class="sxs-lookup"><span data-stu-id="19d72-230">On the purchase order line:</span></span>  

     <span data-ttu-id="19d72-231">Vara = GJALD</span><span class="sxs-lookup"><span data-stu-id="19d72-231">Item = CHARGE</span></span>  

     <span data-ttu-id="19d72-232">Magn = 1</span><span class="sxs-lookup"><span data-stu-id="19d72-232">Quantity = 1</span></span>  

     <span data-ttu-id="19d72-233">Innkaupsverð = 100</span><span class="sxs-lookup"><span data-stu-id="19d72-233">Direct Unit Cost = 100</span></span>  

     <span data-ttu-id="19d72-234">Bóka móttaka og reikningsfæra.</span><span class="sxs-lookup"><span data-stu-id="19d72-234">Post Receive and Invoice.</span></span>  

3.  <span data-ttu-id="19d72-235">Stofna nýja sölupöntun:</span><span class="sxs-lookup"><span data-stu-id="19d72-235">Create new sales order:</span></span>  

     <span data-ttu-id="19d72-236">Selt til Viðskiptamaður Nr.: 10000</span><span class="sxs-lookup"><span data-stu-id="19d72-236">Sell-to Customer No.: 10000</span></span>  

     <span data-ttu-id="19d72-237">Bókunardagsetning = 16. desember 2013</span><span class="sxs-lookup"><span data-stu-id="19d72-237">Posting Date = December 16th, 2013</span></span>  

     <span data-ttu-id="19d72-238">Í sölupöntunarlínu:</span><span class="sxs-lookup"><span data-stu-id="19d72-238">On the sales order line:</span></span>  

     <span data-ttu-id="19d72-239">Vara = GJALD</span><span class="sxs-lookup"><span data-stu-id="19d72-239">Item = CHARGE</span></span>  

     <span data-ttu-id="19d72-240">Magn = 1</span><span class="sxs-lookup"><span data-stu-id="19d72-240">Quantity = 1</span></span>  

     <span data-ttu-id="19d72-241">Einingarverð = 135</span><span class="sxs-lookup"><span data-stu-id="19d72-241">Unit Price = 135</span></span>  

     <span data-ttu-id="19d72-242">Bóka afhenda og reikningsfæra.</span><span class="sxs-lookup"><span data-stu-id="19d72-242">Post Ship and Invoice.</span></span>  

4.  <span data-ttu-id="19d72-243">Uppsetning fjárhags:</span><span class="sxs-lookup"><span data-stu-id="19d72-243">General Ledger Setup:</span></span>  

     <span data-ttu-id="19d72-244">Bókun leyfð frá = 1. janúar 2014</span><span class="sxs-lookup"><span data-stu-id="19d72-244">Allow Posting From = January 1st, 2014</span></span>  

     <span data-ttu-id="19d72-245">Bókun leyfð til = autt</span><span class="sxs-lookup"><span data-stu-id="19d72-245">Allow Posting To = blank</span></span>  

5.  <span data-ttu-id="19d72-246">Stofna nýja innkaupapöntun:</span><span class="sxs-lookup"><span data-stu-id="19d72-246">Create new purchase order:</span></span>  

     <span data-ttu-id="19d72-247">Kaupa af lánardrottni nr.: 10000</span><span class="sxs-lookup"><span data-stu-id="19d72-247">Buy-from Vendor No.: 10000</span></span>  

     <span data-ttu-id="19d72-248">Bókunardagsetning = 2. janúar 2014</span><span class="sxs-lookup"><span data-stu-id="19d72-248">Posting Date = January 2nd, 2014</span></span>  

     <span data-ttu-id="19d72-249">Reikningsnr. lánardrottins: 2345</span><span class="sxs-lookup"><span data-stu-id="19d72-249">Vendor Invoice No.: 2345</span></span>  

     <span data-ttu-id="19d72-250">Á innkaupapöntunarlínunni:</span><span class="sxs-lookup"><span data-stu-id="19d72-250">On the purchase order line:</span></span>  

     <span data-ttu-id="19d72-251">Kostnaðarauki = JB-FLUTN</span><span class="sxs-lookup"><span data-stu-id="19d72-251">Item Charge = JB-FREIGHT</span></span>  

     <span data-ttu-id="19d72-252">Magn = 1</span><span class="sxs-lookup"><span data-stu-id="19d72-252">Quantity = 1</span></span>  

     <span data-ttu-id="19d72-253">Innkaupsverð = 3</span><span class="sxs-lookup"><span data-stu-id="19d72-253">Direct Unit Cost = 3</span></span>  

     <span data-ttu-id="19d72-254">Úthluta kostnaðarauka á innkaupamóttöku úr skrefi 2.</span><span class="sxs-lookup"><span data-stu-id="19d72-254">Assign Item Charge to Purchase Receipt from step 2.</span></span>  

     <span data-ttu-id="19d72-255">Bóka kvittun og reikningsfæra.</span><span class="sxs-lookup"><span data-stu-id="19d72-255">Post Receipt and Invoice.</span></span>  

     <span data-ttu-id="19d72-256">![Yfirlit yfir birgðahöfuðbók og virðisfærslur sem urðu til 3](media/helene/TechArticleAdjustcost11.png "Yfirlit yfir birgðahöfuðbók og virðisfærslur sem urðu til 3")</span><span class="sxs-lookup"><span data-stu-id="19d72-256">![Overview of resulting item ledger and value entries 3](media/helene/TechArticleAdjustcost11.png "Overview of resulting item ledger and value entries 3")</span></span>

6.  <span data-ttu-id="19d72-257">Á vinnudaginn 3. janúar kemur innkaupareikningur sem inniheldur viðbótargjald við kaupin sem voru gerð í skrefi 2.</span><span class="sxs-lookup"><span data-stu-id="19d72-257">On work date January 3rd a purchase invoice arrives, containing an additional item charge to the purchase made in step 2.</span></span> <span data-ttu-id="19d72-258">Þessi reikningur hefur dagsetningu skjals 30. desember og er því bókaður með bókunardagsetningunni 30. desember 2013.</span><span class="sxs-lookup"><span data-stu-id="19d72-258">This invoice has document date December 30th and is therefore posted with Posting Date December 30th, 2013.</span></span>  

     <span data-ttu-id="19d72-259">Stofna nýja innkaupapöntun:</span><span class="sxs-lookup"><span data-stu-id="19d72-259">Create new purchase order:</span></span>  

     <span data-ttu-id="19d72-260">Kaupa af lánardrottni nr.: 10000</span><span class="sxs-lookup"><span data-stu-id="19d72-260">Buy-from Vendor No.: 10000</span></span>  

     <span data-ttu-id="19d72-261">Bókunardagsetning = 30. desember 2013</span><span class="sxs-lookup"><span data-stu-id="19d72-261">Posting Date = December 30th, 2013</span></span>  

     <span data-ttu-id="19d72-262">Reikningsnr. lánardrottins: 3456</span><span class="sxs-lookup"><span data-stu-id="19d72-262">Vendor Invoice No.: 3456</span></span>  

     <span data-ttu-id="19d72-263">Á innkaupapöntunarlínunni:</span><span class="sxs-lookup"><span data-stu-id="19d72-263">On the purchase order line:</span></span>  

     <span data-ttu-id="19d72-264">Kostnaðarauki = JB-FLUTN</span><span class="sxs-lookup"><span data-stu-id="19d72-264">Item Charge = JB-FREIGHT</span></span>  

     <span data-ttu-id="19d72-265">Magn = 1</span><span class="sxs-lookup"><span data-stu-id="19d72-265">Quantity = 1</span></span>  

     <span data-ttu-id="19d72-266">Innkaupsverð = 2</span><span class="sxs-lookup"><span data-stu-id="19d72-266">Direct Unit Cost = 2</span></span>  

     <span data-ttu-id="19d72-267">Úthluta kostnaðarauka á innkaupamóttöku úr skrefi 2</span><span class="sxs-lookup"><span data-stu-id="19d72-267">Assign Item Charge to Purchase Receipt from step 2</span></span>  

     <span data-ttu-id="19d72-268">Bóka kvittun og reikningsfæra.</span><span class="sxs-lookup"><span data-stu-id="19d72-268">Post Receipt and Invoice.</span></span>  

   <span data-ttu-id="19d72-269">![Yfirlit yfir birgðahöfuðbók og virðisfærslur 4 sem urðu til](media/helene/TechArticleAdjustcost12.png "Yfirlit yfir birgðahöfuðbók og virðisfærslur 4 sem urðu til")</span><span class="sxs-lookup"><span data-stu-id="19d72-269">![Overview of resulting item ledger and value entries 4](media/helene/TechArticleAdjustcost12.png "Overview of resulting item ledger and value entries 4")</span></span>

 <span data-ttu-id="19d72-270">Skýrsla birgðavirðis er prentuð frá og með dagsetningunni 31. desember 2013</span><span class="sxs-lookup"><span data-stu-id="19d72-270">Inventory Valuation report is printed as of Date December 31st , 2013</span></span>  

<span data-ttu-id="19d72-271">![Innihald birgðavirðisskýrslu](media/helene/TechArticleAdjustcost13.png "Innihald birgðavirðisskýrslu")</span><span class="sxs-lookup"><span data-stu-id="19d72-271">![Content of the Inventory Valuation report](media/helene/TechArticleAdjustcost13.png "Content of the Inventory Valuation report")</span></span>

 <span data-ttu-id="19d72-272">**Samantekt á aðstæðum:**</span><span class="sxs-lookup"><span data-stu-id="19d72-272">**Summary of scenario:**</span></span>  

 <span data-ttu-id="19d72-273">Útlistaðar aðstæður enda með verðmætamati á birgðum sem sýnir magn = 0 á meðan gildið = 2.</span><span class="sxs-lookup"><span data-stu-id="19d72-273">The described scenario ends up with an Inventory Valuation report demonstrating Quantity = 0 while the Value = 2.</span></span> <span data-ttu-id="19d72-274">Bókaður kostnaðarauki í skrefi 11 er hluti af birgðaaukningunni í desember á meðan birgðaminnkun sama tímabils verður ekki fyrir áhrifum.</span><span class="sxs-lookup"><span data-stu-id="19d72-274">The Item charge posted in step 11 is part of the Inventory Increase value of December while the Inventory Decrease of the same period is not affected.</span></span>  

 <span data-ttu-id="19d72-275">Að fjárhagsgrunnurinn skyldi gefa upp Leyfa bókun frá og með 1. janúar var gott fyrir fyrsta kostnaðaraukann.</span><span class="sxs-lookup"><span data-stu-id="19d72-275">Having the General Ledger Setup stating Allow Posting From January 1st was a good thing for the first Item charge.</span></span> <span data-ttu-id="19d72-276">Kostnaður við birgðaaukningu og -minnkun var skráð á sama tímabilið.</span><span class="sxs-lookup"><span data-stu-id="19d72-276">The costs of the Inventory Increase and Decrease was recorded in the same period.</span></span> <span data-ttu-id="19d72-277">Fyrir seinni kostnaðaraukann er það hins vegar fjárhagsgrunnurinn sem veldur því að breytingin á kostnaði seldrar vöru verði samþykktur fyrir næsta tímabil.</span><span class="sxs-lookup"><span data-stu-id="19d72-277">For the second Item charge however, the General Ledger Setup causes the change in COGS to be recognized in the period after.</span></span>  

 <span data-ttu-id="19d72-278">**Niðurstaða:**</span><span class="sxs-lookup"><span data-stu-id="19d72-278">**Conclusion:**</span></span>  

 <span data-ttu-id="19d72-279">Það er áskorun að hafa skýrslu birgðavirðis til að sýna magn = 0 á meðan gildið <> 0.</span><span class="sxs-lookup"><span data-stu-id="19d72-279">It’s a challenge to have the Inventory Valuation report to demonstrate Quantity = 0 while the Value <> 0.</span></span> <span data-ttu-id="19d72-280">Í þessu tilfelli er það líka erfiðara að tjá ákjósanlegustu stillingar með því að hafa innkaupareikninga sem koma á sama degi en taka til mismunandi tímabila eða jafnvel reikningsára.</span><span class="sxs-lookup"><span data-stu-id="19d72-280">In this case it’s also more difficult to express the optimal settings, having purchase invoices arriving the same day but addressing different periods or even fiscal years.</span></span> <span data-ttu-id="19d72-281">Að færast yfir á nýtt reikningsár krefst yfirleitt einhverrar skipulagningar og sem hluti af því þarf að íhuga nánar ferli leiðréttingarkostnaðar - birgðafærslna, gera sér grein fyrir kostnaði seldra vara.</span><span class="sxs-lookup"><span data-stu-id="19d72-281">Crossing to a new fiscal year usually requires some planning and as part of that the insight of Adjust Cost – Item entries process, recognizing COGS, is to be considered.</span></span>  

 <span data-ttu-id="19d72-282">Í þessari atburðarás getur einn möguleiki verið að hafa fjárhagsgrunninn, reitinn Bókun leyfð frá, gefa upp dagsetningu í desember fyrir nokkra daga í viðbót og fresta bókun á fyrsta kostnaðaraukanum svo allir kostnaðir fyrir fyrra tímabil/fjárhagsár verði viðurkenndir fyrir tímabilið sem þeir tilheyra í fyrstu, keyra síðan runuvinnslu Leiðrétts kostnaðar - Birgðafærslna og í kjölfarið færa leyfða bókunardagsetningu yfir á nýtt tímabil\/fjárhagsársins.</span><span class="sxs-lookup"><span data-stu-id="19d72-282">In this scenario one option could have been to have the General Ledger Setup, field Allow Posting From, stating a date in December for a couple of more days and the posting of the first item charge postponed to allow all costs for the previous period/fiscal year to be recognized for the period they belong to first, having the Adjust Cost – Item entries batch job run and thereafter move the allowed posting date to the new period\/fiscal year.</span></span> <span data-ttu-id="19d72-283">Fyrsti kostnaðaraukinn með bókunardagsetninguna 2. janúar getur þá verið bókaður.</span><span class="sxs-lookup"><span data-stu-id="19d72-283">The first item charge with posting date January 2nd could then be posted.</span></span>  

## <a name="history-of-adjust-cost--item-entries-batch-job"></a><span data-ttu-id="19d72-284">Ferill runuvinnslu Leiðrétts kostnaðar – birgðafærslna</span><span class="sxs-lookup"><span data-stu-id="19d72-284">History of Adjust Cost – Item entries batch job</span></span>  
 <span data-ttu-id="19d72-285">Hér fyrir neðan er samantekt á hugmyndinni um að úthluta bókunardagsetningum á leiðrétttingarvirðisfærslum með runuvinnslu leiðrétts kostnaðar - birgðafærslna síðan í útgáfu 3.0.</span><span class="sxs-lookup"><span data-stu-id="19d72-285">Below is a summary of the concept assigning Posting Dates to Adjustment Value Entries by the Adjust Cost – Item entries batch job since version 3.0.</span></span>  

### <a name="from-version-30370a"></a><span data-ttu-id="19d72-286">Frá útgáfu 3.0..3.70.A</span><span class="sxs-lookup"><span data-stu-id="19d72-286">From version 3.0..3.70.A</span></span>  
 <span data-ttu-id="19d72-287">Í beiðniglugga fyrir runuvinnslu leiðrétts kostnaðar - birgðafærslna þarf notandi að færa inn bókunardagsetningu.</span><span class="sxs-lookup"><span data-stu-id="19d72-287">In the request form of the Adjust Cost - Item Entries batch job there is a Posting Date to be entered by the user.</span></span> <span data-ttu-id="19d72-288">Runuvinnslan fer í gegnum allar nauðsynlegar breytingar og stofnar virðisfærslur með bókunardagsetningunni sem hefur verið færð inn í beiðnigluggann.</span><span class="sxs-lookup"><span data-stu-id="19d72-288">The batch job runs through all necessary changes and creates value entries with the posting date entered in the request form.</span></span> <span data-ttu-id="19d72-289">Ráðlögð bókunardagsetning er dagurinn í dag.</span><span class="sxs-lookup"><span data-stu-id="19d72-289">Suggested posting date to use is today’s date.</span></span>  

### <a name="version-370b40"></a><span data-ttu-id="19d72-290">Útgáfa 3.70.B..4.0</span><span class="sxs-lookup"><span data-stu-id="19d72-290">Version 3.70.B..4.0</span></span>  
 <span data-ttu-id="19d72-291">Í beiðniglugga fyrir runuvinnslu leiðrétts kostnaðar - birgðafærslna þarf notandi að færa inn bókunardagsetningu lokaðrar tímabilsfærslu.</span><span class="sxs-lookup"><span data-stu-id="19d72-291">In the request form of the Adjust Cost - Item Entries batch job there is a Closed Period Entry Posting Date to be entered by the user.</span></span> <span data-ttu-id="19d72-292">Runuvinnslan fer í gegnum nauðsynlegar breytingar og stofnar virðisfærslur með bókunardagsetningu á yfirbirgðafærslunni (afhendingardagur sölunnar sem leiðréttingin gefur upp).</span><span class="sxs-lookup"><span data-stu-id="19d72-292">The batch job runs through all necessary changes and creates value entries with the posting date of the parent item ledger entry (shipment date of the sale that the adjustment address).</span></span> <span data-ttu-id="19d72-293">Ef bókunardagsetning yfirbirgðafærslunnar er ekki innan leyfilegs dagsetningabils bókunar verður bókunardagsetningu lokaðrar tímabilsfærslu úthlutað leiðréttingarvirðisfærslu.</span><span class="sxs-lookup"><span data-stu-id="19d72-293">If the posting date of the parent item ledger entry is not within allowed posting date range the posting date stated as Closed Period Entry Posting Date will be assigned the Adjustment Value Entry.</span></span> <span data-ttu-id="19d72-294">Dagsetning telst vera á lokuðu tímabili þegar hún er eldri en dagsetningin í reitnum Bókun leyfð frá í fjárhagsgrunni.</span><span class="sxs-lookup"><span data-stu-id="19d72-294">A date is considered to be in a closed period when it is earlier than the date in the Allow Posting From field in the General Ledger Setup.</span></span>  

### <a name="from-version-50"></a><span data-ttu-id="19d72-295">Frá útgáfu 5,0:</span><span class="sxs-lookup"><span data-stu-id="19d72-295">From version 5.0:</span></span>  
 <span data-ttu-id="19d72-296">Ekki þarf lengur að gefa upp bókunardagsetningu í beiðniglugga fyrir runuvinnslu leiðrétts kostnaðar - birgðafærslna.</span><span class="sxs-lookup"><span data-stu-id="19d72-296">There is no longer a posting date to be stated in the request form of the Adjust Cost - Item entries batch job.</span></span> <span data-ttu-id="19d72-297">Runuvinnslan fer í gegnum allar nauðsynlegar breytingar og stofnar virðisfærslur með bókunardagsetningu virðisfærslunnar sem hún leiðréttir.</span><span class="sxs-lookup"><span data-stu-id="19d72-297">The batch job runs through all necessary changes and creates value entries with the posting date of the value entry it adjusts.</span></span> <span data-ttu-id="19d72-298">Ef bókunardagsetningin er ekki innan leyfilegs dagsetningabils bókunar verður bókunardagsetningin í reitnum Bókun leyfð frá í fjárhagsgrunni notuð, EÐA ef birgðatímabil eru notuð, verður eldri dagsetningin af þessum tveimur notuð.</span><span class="sxs-lookup"><span data-stu-id="19d72-298">If the posting date is not within allowed posting date range the posting date in the Allow Posting From field in the General Ledger Setup, OR if the Inventory periods are used, the later date of the two will be used.</span></span> <span data-ttu-id="19d72-299">Sjá útskýrt hugtak hér að ofan.</span><span class="sxs-lookup"><span data-stu-id="19d72-299">See described concept above.</span></span>  

## <a name="history-of-post-inventory-cost-to-gl-batch-job"></a><span data-ttu-id="19d72-300">Ferill runuvinnslunnar Bóka birgðabreytingar</span><span class="sxs-lookup"><span data-stu-id="19d72-300">History of Post Inventory cost to G/L batch job</span></span>  
 <span data-ttu-id="19d72-301">Runuvinnslan Bóka birgðabreytingar er nátengd runuvinnslunni Leiðrétta kostnað - Birgðafærslur og því er ferill runuvinnslunnar að auki tekin saman og deilt hér.</span><span class="sxs-lookup"><span data-stu-id="19d72-301">The Post Inventory Cost to G/L batch job is closely related to the Adjust Cost – Item entries batch job why the history of this batch job is summarized and shared here as well.</span></span>  

### <a name="from-version-30370a"></a><span data-ttu-id="19d72-302">Frá útgáfu 3.0..3.70.A</span><span class="sxs-lookup"><span data-stu-id="19d72-302">From version 3.0..3.70.A</span></span>  
 <span data-ttu-id="19d72-303">Í beiðniglugga fyrir birgðabreytingar þarf notandi að færa inn bókunardagsetningu.</span><span class="sxs-lookup"><span data-stu-id="19d72-303">In the request form of the Post Inventory Cost to G/L there is a Posting Date to be entered by the user.</span></span> <span data-ttu-id="19d72-304">Runuvinnslan keyrir í gegnum allar virðisfærslur innan síunnar, ef það er einhver, og stofnar fjárhagsfærslur þar sem bókunardagsetning er færð inn í beiðnigluggann.</span><span class="sxs-lookup"><span data-stu-id="19d72-304">The batch job runs through all value entries within the filter, if any, and creates General Ledger Entries with Posting Date entered in the request form.</span></span>  

### <a name="version-370b40"></a><span data-ttu-id="19d72-305">Útgáfa 3.70.B..4.0</span><span class="sxs-lookup"><span data-stu-id="19d72-305">Version 3.70.B..4.0</span></span>  
 <span data-ttu-id="19d72-306">Í beiðniglugga birgðabreytinga er reiturinn bókunardagsetning lokaðrar tímabilsfærslu tiltækur.</span><span class="sxs-lookup"><span data-stu-id="19d72-306">In the request form of the Post Inventory Cost to G/L the Closed Period Entry Posting Date field is available.</span></span> <span data-ttu-id="19d72-307">Forritið notar dagsetninguna sem þú slærð inn í þennan reit sem bókunardagsetningu fyrir fjárhagsfærslurnar sem það stofnar fyrir virðisfærslur, en bókunardagsetningar þeirra eru á lokuðu reikningstímabili.</span><span class="sxs-lookup"><span data-stu-id="19d72-307">The program uses the date you enter in this field as the posting date for the general ledger entries it creates for value entries whose posting dates are in closed accounting periods.</span></span> <span data-ttu-id="19d72-308">Að öðrum kosti munu fjárhagsfærslurnar hafa sömu bókunardagsetningu og upprunalegu virðisfærslurnar.</span><span class="sxs-lookup"><span data-stu-id="19d72-308">Otherwise, the general ledger entries will have the same posting date as the original value entries.</span></span> <span data-ttu-id="19d72-309">Dagsetning telst vera á lokuðu tímabili þegar hún er eldri en dagsetningin í reitnum Bókun leyfð frá í fjárhagsgrunni.</span><span class="sxs-lookup"><span data-stu-id="19d72-309">A date is considered to be in a closed period when it is earlier than the date in the Allow Posting From field in the General Ledger Setup.</span></span> <span data-ttu-id="19d72-310">Ef fjár\/hagur er bókaður fyrir hvern bókunarflokk munu fjárhagsfærslurnar fá bókunardagsetninguna sem er tilgreind í reit bókunardagsetningar í beiðniglugganum.</span><span class="sxs-lookup"><span data-stu-id="19d72-310">If posting to G\/L Per Posting Group, the general ledger entries will have the posting date that is specified in the Posting Date field in the request form.</span></span>  

 <span data-ttu-id="19d72-311">Í útgáfum 3 og 4 skannar runuvinnslan allar virðisfærslur til að greina hvort einhverjar virðisfærslur séu til þar sem kostnaðarupphæð (raunveruleg) er frábrugðin kostnaði bókuðum í fjárhag.</span><span class="sxs-lookup"><span data-stu-id="19d72-311">In version 3 and 4 the batch job scans all value entries to detect if there are any value entries where Cost Amount (Actual) differs from Cost Posted to G/L.</span></span> <span data-ttu-id="19d72-312">Ef finnst mismunur verður frábrugðna upphæðin bókuð í fjárhagsfærslu.</span><span class="sxs-lookup"><span data-stu-id="19d72-312">If there is a difference detected the differing amount will be posted in a G/L entry.</span></span> <span data-ttu-id="19d72-313">Ef bókun áætlaðs kostnaðar er notaður er unnið úr samsvarandi reitum á sama hátt.</span><span class="sxs-lookup"><span data-stu-id="19d72-313">If expected cost posting is used corresponding fields are processed in the same way.</span></span>  

<span data-ttu-id="19d72-314">![Raunverulegur kostnaður á móti áætluðum kostnaði](media/helene/TechArticleAdjustcost14.png "Raunverulegur kostnaður á móti áætluðum kostnaði")</span><span class="sxs-lookup"><span data-stu-id="19d72-314">![Actual cost versus expected cost](media/helene/TechArticleAdjustcost14.png "Actual cost versus expected cost")</span></span>

### <a name="from-version-50"></a><span data-ttu-id="19d72-315">Frá útgáfu 5,0:</span><span class="sxs-lookup"><span data-stu-id="19d72-315">From version 5.0:</span></span>  
 <span data-ttu-id="19d72-316">Ekki þarf lengur að tilgreina bókunardagsetningu í beiðniglugganum fyrir runuvinnslu birgðabreytinga.</span><span class="sxs-lookup"><span data-stu-id="19d72-316">There is no longer a posting date to be stated in the request form of the Post Inventory Cost to G/L batch job.</span></span> <span data-ttu-id="19d72-317">Fjárhagsfærslan er búin til með sömu bókunardagsetningu og tengd virðisfærsla.</span><span class="sxs-lookup"><span data-stu-id="19d72-317">The G/L entry is created with the same Posting Date as the related value entry.</span></span> <span data-ttu-id="19d72-318">Til þess að ljúka runuvinnslunni verður leyfilegt dagsetningabil bókunar að leyfa bókunardagsetningu stofnuðu fjárhagsfærslunnar.</span><span class="sxs-lookup"><span data-stu-id="19d72-318">In order to complete the batch job the allowed posting date range must allow the Posting Date of the created G/L entry.</span></span> <span data-ttu-id="19d72-319">Ef ekki, verður að enduropna tímabundið leyfilegt dagsetningabil bókunar með því að breyta eða fjarlægja dagsetningarnar í reitunum Bókun leyfð frá og til í fjárhagsgrunni.</span><span class="sxs-lookup"><span data-stu-id="19d72-319">If not, the allowed posting date range must be temporarily re-opened by changing or removing the dates in the Allow Posting From and To fields in the General Ledger Setup.</span></span> <span data-ttu-id="19d72-320">Til að koma í veg fyrir afstemmingarvandamál er nauðsynlegt að bókunardagsetning fjárhagsfærslu samsvari bókunardagsetningu virðisfærslu.</span><span class="sxs-lookup"><span data-stu-id="19d72-320">To avoid reconciliation issues it is required that Posting Date of the G/L Entry corresponds to the Posting Date of the Value Entry.</span></span>  

 <span data-ttu-id="19d72-321">Runuvinnslan skannar tafla 5811 - Bóka virðisfærslu í fjárhag, til að bera kennsl á virðisfærslur sem heyra undir bókun í fjárhag.</span><span class="sxs-lookup"><span data-stu-id="19d72-321">The batch job scans Table 5811 - Post Value Entry to G/L, to identify the Value Entries in scope for posting to General Ledger.</span></span> <span data-ttu-id="19d72-322">Taflan var tæmd eftir heppnaða keyrslu.</span><span class="sxs-lookup"><span data-stu-id="19d72-322">After successful run the table is emptied.</span></span>

## <a name="see-also"></a><span data-ttu-id="19d72-323">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="19d72-323">See Also</span></span>  
[<span data-ttu-id="19d72-324">Hönnunarupplýsingar: Birgðakostnaður</span><span class="sxs-lookup"><span data-stu-id="19d72-324">Design Details: Inventory Costing</span></span>](design-details-inventory-costing.md)  
[<span data-ttu-id="19d72-325">Hönnunarupplýsingar: Birgðajöfnun</span><span class="sxs-lookup"><span data-stu-id="19d72-325">Design Details: Item Application</span></span>](design-details-item-application.md)  
