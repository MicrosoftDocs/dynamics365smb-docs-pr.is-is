---
title: "Bókunardagsetning á virðisfærslum"
description: "Lærðu hvernig runuvinnslan Leiðréttur kostnaður - birgðafærslur ber kennsl á og úthlutar bókunardagsetningu fyrir virðisfærslurnar sem runuvinnslan er að búa til."
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 11/23/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: c95432ec1cf24aaaedf0fad5a2746ace9705e2e3
ms.contentlocale: is-is
ms.lasthandoff: 03/22/2018

---
# <a name="design-details-posting-date-on-adjustment-value-entry"></a><span data-ttu-id="a98a7-103">Hönnunarupplýsingar: Bókunardagsetning á leiðréttingarvirðisfærslu</span><span class="sxs-lookup"><span data-stu-id="a98a7-103">Design Details: Posting Date on Adjustment Value Entry</span></span>
<span data-ttu-id="a98a7-104">Þessi grein veitir leiðbeiningar fyrir notendur birgðakostnaðarvirkni í [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="a98a7-104">This article provides guidance for users of the Inventory Costing functionality in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="a98a7-105">Tilgreind grein veitir leiðbeiningar um hvernig runuvinnslan **Leiðréttur kostnaður - Birgðafærslur** ber kennsl á og úthlutar bókunardagsetningu fyrir virðisfærslurnar sem runuvinnslan er að búa til.</span><span class="sxs-lookup"><span data-stu-id="a98a7-105">The specific article is providing guidance in how the **Adjust Cost - Item Entries** batch job identifies and assigns a posting date to the value entries that the batch job is about to create.</span></span>  

<span data-ttu-id="a98a7-106">Fyrst er hugmynd ferlisins yfirfarin, hvernig runuvinnslan ber kennsl á og úthlutar bókunardagsetningu fyrir virðisfærsluna sem verður búin til.</span><span class="sxs-lookup"><span data-stu-id="a98a7-106">First the concept of the process is reviewed, how the batch job identifies and assigns the Posting Date to the Value Entry to be created.</span></span> <span data-ttu-id="a98a7-107">Eftir það eru nokkrar aðstæður sem við í stuðningshópnum rekumst á af og til og að lokum er samantekt yfir hugtökin sem eru notuð í útgáfu 3.0.</span><span class="sxs-lookup"><span data-stu-id="a98a7-107">Thereafter there are some scenarios shared that we in the support team come across from time to time and finally there is a summary of the concepts used from version 3.0.</span></span>  

## <a name="the-concept"></a><span data-ttu-id="a98a7-108">Hugtakið</span><span class="sxs-lookup"><span data-stu-id="a98a7-108">The Concept</span></span>  
<span data-ttu-id="a98a7-109">Frá útgáfu 5.0, runuvinnslan **Leiðrétta kostnað - Birgðafærslur** úthlutar bókunardagsetningu fyrir virðisfærsluna sem hún kemur til með að búa til í eftirfarandi skrefum:</span><span class="sxs-lookup"><span data-stu-id="a98a7-109">From version 5.0, the **Adjust Cost – Item Entries** batch job assigns a posting date to the value entry it is about to create in the following steps:</span></span>  

1.  <span data-ttu-id="a98a7-110">Upphaflega er bókunardagsetning færslunnar sem á að búa til sú sama og dagsetning færslunnar sem hún leiðréttir.</span><span class="sxs-lookup"><span data-stu-id="a98a7-110">Initially the Posting Date of the entry to be created is the same date as the entry it adjusts.</span></span>  

2.  <span data-ttu-id="a98a7-111">Bókunardagsetningin er sannprófuð gagnvart birgðatímabili og/eða fjárhagsgrunni.</span><span class="sxs-lookup"><span data-stu-id="a98a7-111">The Posting Date is validated against Inventory Periods and/or General Ledger Setup.</span></span>  

3.  <span data-ttu-id="a98a7-112">Úthlutun bókunardagsetningu; Ef upphafleg bókunardagsetning er ekki innan leyfilegs dagsetningabils bókunar, þá mun runuvinnslan úthluta leyfilegri bókunardagsetningu frá annað hvort fjárhagsgrunni eða birgðatímabili.</span><span class="sxs-lookup"><span data-stu-id="a98a7-112">Assignment of Posting Date; If the initial Posting Date is not within allowed posting date range the batch job will assign an allowed Posting Date from either General Ledger Setup or Inventory Period.</span></span> <span data-ttu-id="a98a7-113">Ef bæði birgðatímabil og leyfileg bókunardagsetning í fjárhagsgrunni eru skilgreind, verður síðari dagsetning þessara tveggja úthlutað til leiðréttingarvirðisfærslu.</span><span class="sxs-lookup"><span data-stu-id="a98a7-113">If both Inventory Periods and allowed posting dates in General Ledger Setup are defined, the later date of the two will be assigned to the Adjustment Value Entry.</span></span>  

 <span data-ttu-id="a98a7-114">Við skulum yfirfara þetta ferli betur með dæmi.</span><span class="sxs-lookup"><span data-stu-id="a98a7-114">Let’s review this process more in practice.</span></span> <span data-ttu-id="a98a7-115">Gerum ráð fyrir að við séum með birgðafærslu fyrir sölu.</span><span class="sxs-lookup"><span data-stu-id="a98a7-115">Assume we have an Item Ledger Entry of Sale.</span></span> <span data-ttu-id="a98a7-116">Þessi hlutur var sendur 5. september 2013 og reikningsfærður daginn eftir.</span><span class="sxs-lookup"><span data-stu-id="a98a7-116">The item was shipped on September 5th, 2013 and it was invoiced the day after.</span></span>  

<span data-ttu-id="a98a7-117">![Birgðafærsla: Dagsetningarsnið: ÁÁÁÁ MM DD](media/helene/TechArticleAdjustcost1.png "TechArticleAdjustcost1")</span><span class="sxs-lookup"><span data-stu-id="a98a7-117">![Item Ledger Entry: Date format: YYYY MM DD](media/helene/TechArticleAdjustcost1.png "TechArticleAdjustcost1")</span></span>  

<span data-ttu-id="a98a7-118">Hér að neðan táknar fyrsta virðisfærslan (379) sendinguna og bera þær sömu bókunardagsetningu og yfirbirgðafærslan.</span><span class="sxs-lookup"><span data-stu-id="a98a7-118">Below, the first Value Entry (379) represents the shipment and carry the same Posting Date as the parent Item ledger Entry.</span></span>  

<span data-ttu-id="a98a7-119">Önnur virðisfærslan (381) táknar reikninginn.</span><span class="sxs-lookup"><span data-stu-id="a98a7-119">The second Value Entry (381) represents the invoice.</span></span>  

 <span data-ttu-id="a98a7-120">Þriðja virðisfærslan (391) er leiðrétting á reikningsfærðri virðisfærslu (381)</span><span class="sxs-lookup"><span data-stu-id="a98a7-120">The third Value Entry (391) is an Adjustment of the invoicing Value Entry (381)</span></span>  

 <span data-ttu-id="a98a7-121">![Birgðafærsla: Dagsetningarsnið: ÁÁÁÁ MM DD](media/helene/TechArticleAdjustcost2.png "TechArticleAdjustcost2")</span><span class="sxs-lookup"><span data-stu-id="a98a7-121">![Item Ledger Entry: Date format: YYYY MM DD](media/helene/TechArticleAdjustcost2.png "TechArticleAdjustcost2")</span></span>  

 <span data-ttu-id="a98a7-122">Skref 1: Leiðréttingarvirðisfærsla sem á að búa til er úthlutað sömu bókunardagsetningu og færslan sem hún leiðréttir, sýnt hér að framan með virðisfærslu 391.</span><span class="sxs-lookup"><span data-stu-id="a98a7-122">Step 1: Adjustment Value Entry to be created is assigned same Posting Date as the entry it adjusts, illustrated above by Value entry 391.</span></span>  

 <span data-ttu-id="a98a7-123">Skref 2: Villuleit á upphaflega úthlutaðri bókunardagsetningu.</span><span class="sxs-lookup"><span data-stu-id="a98a7-123">Step 2: Validation of initial assigned Posting Date.</span></span>  

<span data-ttu-id="a98a7-124">Runuvinnslan **Leiðrétta kostnað - Birgðafærslur** ákvarðar hvort upphafleg bókunardagsetning fyrir leiðréttingarvirðisfærslu er innan leyfilegs dagsetningabils bókunar byggt á birgðatímabili og/eða fjárhagsgrunni.</span><span class="sxs-lookup"><span data-stu-id="a98a7-124">The **Adjust Cost – Item Entries** batch job determines if the initial Posting Date of the Adjustment Value Entry is within allowed posting date range based upon Inventory Periods and/or General Ledger Setup.</span></span>  

 <span data-ttu-id="a98a7-125">Við skulum endurskoða ofangreinda sölu með því að bæta við uppsetningu á leyfilegu dagsetningabili bókunar.</span><span class="sxs-lookup"><span data-stu-id="a98a7-125">Let’s review the above mentioned Sale by adding setup of allowed posting date ranges.</span></span>  

 <span data-ttu-id="a98a7-126">Birgðatímabil:</span><span class="sxs-lookup"><span data-stu-id="a98a7-126">Inventory Periods:</span></span>  

<span data-ttu-id="a98a7-127">![Leiðrétta kostnað &#45;Færslugögn vöru](media/helene/TechArticleAdjustcost3.png "TechArticleAdjustcost3")</span><span class="sxs-lookup"><span data-stu-id="a98a7-127">![Adjust cost &#45;Item entries data](media/helene/TechArticleAdjustcost3.png "TechArticleAdjustcost3")</span></span>

 <span data-ttu-id="a98a7-128">Fyrsta leyfilega bókunardagsetning er fyrsta daginn í fyrsta opna tímabilinu.</span><span class="sxs-lookup"><span data-stu-id="a98a7-128">First allowed posting date is the first day in the first open period.</span></span> <span data-ttu-id="a98a7-129">1. september 2013.</span><span class="sxs-lookup"><span data-stu-id="a98a7-129">September 1st, 2013.</span></span>  

 <span data-ttu-id="a98a7-130">Uppsetning fjárhags:</span><span class="sxs-lookup"><span data-stu-id="a98a7-130">General Ledger Setup:</span></span>  

<span data-ttu-id="a98a7-131">![Leiðrétta kostnað &#45;Færslugögn vöru](media/helene/TechArticleAdjustcost4.png "TechArticleAdjustcost4")</span><span class="sxs-lookup"><span data-stu-id="a98a7-131">![Adjust cost &#45;Item entries data](media/helene/TechArticleAdjustcost4.png "TechArticleAdjustcost4")</span></span>

 <span data-ttu-id="a98a7-132">Fyrsta leyfilega bókunardagsetning er dagsetningin sem tilgreind er í reitnum Leyfa bókanir frá: 10. september 2013.</span><span class="sxs-lookup"><span data-stu-id="a98a7-132">First allowed posting date is the date stated in field Allow Posting From: September 10th, 2013.</span></span>  

 <span data-ttu-id="a98a7-133">Ef bæði birgðatímabil og leyfilegar bókunardagsetningar í fjárhagsgrunni eru skilgreind mun síðari dagsetning þessara tveggja skilgreina leyfilegt dagsetningabil bókunar.</span><span class="sxs-lookup"><span data-stu-id="a98a7-133">If both Inventory Periods and allowed posting dates in General Ledger Setup are defined, the later date of the two will define the allowed posting date range.</span></span>  

 <span data-ttu-id="a98a7-134">Skref 3: Úthlutun á leyfilegri bókunardagsetningu;</span><span class="sxs-lookup"><span data-stu-id="a98a7-134">Step 3: Assignment of an allowed posting date;</span></span>  

 <span data-ttu-id="a98a7-135">Upphaflega úthlutaða bókunardagsetningin var 6. september eins og sýnt er í skrefi 1.</span><span class="sxs-lookup"><span data-stu-id="a98a7-135">The initial assigned Posting Date was September 6th as illustrated in step 1.</span></span> <span data-ttu-id="a98a7-136">Í 2. skrefi ber runuvinnslan Leiðrétta kostnað - Birgðafærslur kennsl 10. september sem fyrstu leyfilegu bókunardagsetninguna og úthlutar þess vegna 10. september á leiðréttingarvirðisfærsluna fyrir neðan.</span><span class="sxs-lookup"><span data-stu-id="a98a7-136">However, in the 2nd step the Adjust Cost – Item entries batch job identifies that earliest allowed Posting Date is September 10th and thereby assigns September 10th to the Adjustment Value Entry, below.</span></span>  

 <span data-ttu-id="a98a7-137">![Leiðrétta kostnað &#45;Færslugögn vöru](media/helene/TechArticleAdjustcost5.png "TechArticleAdjustcost5")</span><span class="sxs-lookup"><span data-stu-id="a98a7-137">![Adjust cost &#45;Item entries data](media/helene/TechArticleAdjustcost5.png "TechArticleAdjustcost5")</span></span>

 <span data-ttu-id="a98a7-138">Við höfum nú yfirfarið hugtakið fyrir úthlutun bókunardagsetninga á virðisfærslur sem eru búnar til af runuvinnslu Leiðrétts kostnaðar - Birgðafærslna.</span><span class="sxs-lookup"><span data-stu-id="a98a7-138">We have now reviewed the concept for assigning Posting Dates to Value Entries created by the Adjust Cost - Item entries batch job.</span></span>  

 <span data-ttu-id="a98a7-139">Við skulum halda áfram að yfirfara sumar aðstæður sem við í stuðningshópnum rekumst á af og til í tengslum við úthlutaðar bókunardagsetningar í runuvinnslu Leiðrétts kostnaðar - Birgðafærslna og tengdum uppsetningum.</span><span class="sxs-lookup"><span data-stu-id="a98a7-139">Let’s continue to review some scenarios that we in the support team comes across from time to time in relation to assigned Posting Dates in the Adjust Cost – Item entries batch job and related setups.</span></span>  

## <a name="scenarios"></a><span data-ttu-id="a98a7-140">Dæmi</span><span class="sxs-lookup"><span data-stu-id="a98a7-140">Scenarios</span></span>  

### <a name="scenario-i-posting-date-is-not-within-your-range-of-allowed-posting-dates"></a><span data-ttu-id="a98a7-141">Aðstæður I: „Bókunardagsetning er ekki innan marka leyfilegra bókunardagsetninga...“</span><span class="sxs-lookup"><span data-stu-id="a98a7-141">Scenario I: “Posting Date is not within your range of allowed posting dates…”</span></span>  
 <span data-ttu-id="a98a7-142">Þetta eru aðstæður þar sem notandi fær upp umrædd villuboð þegar runuvinnsla Leiðrétts kostnaðar - Birgðafærsla er keyrð.</span><span class="sxs-lookup"><span data-stu-id="a98a7-142">This is a scenario where a user is experiencing mentioned error message when the Adjust Cost – Item entries batch job is run.</span></span>  

 <span data-ttu-id="a98a7-143">Í fyrri kafla, sem lýsir hugmyndinni um að gefa út bókunardagsetningar, er ætlunin með runuvinnslu Leiðrétts kostnaðar - Birgðafærslna að búa til virðisfærslu með bókunardagsetninguna 10. september.</span><span class="sxs-lookup"><span data-stu-id="a98a7-143">In the previous section, describing the concept of assigning posting dates, the intention of the Adjust Cost – Item entries batch job is to create a Value Entry with Posting Date September 10th.</span></span>  

<span data-ttu-id="a98a7-144">![Leiðrétta kostnað &#45;Færslugögn vöru](media/helene/TechArticleAdjustcost6.png "TechArticleAdjustcost6")</span><span class="sxs-lookup"><span data-stu-id="a98a7-144">![Adjust cost &#45;Item entries data](media/helene/TechArticleAdjustcost6.png "TechArticleAdjustcost6")</span></span>

 <span data-ttu-id="a98a7-145">Við fylgjum eftir notandauppsetningu:</span><span class="sxs-lookup"><span data-stu-id="a98a7-145">We follow up on the User Setup:</span></span>  

<span data-ttu-id="a98a7-146">![Leiðrétta kostnað &#45;Færslugögn vöru](media/helene/TechArticleAdjustcost7.png "TechArticleAdjustcost7")</span><span class="sxs-lookup"><span data-stu-id="a98a7-146">![Adjust cost &#45;Item entries data](media/helene/TechArticleAdjustcost7.png "TechArticleAdjustcost7")</span></span>

 <span data-ttu-id="a98a7-147">Notandinn í þessu tilfelli hefur leyfilegt dagsetningabil bókunar frá 11. september til 30. september og er því ekki heimilt að bóka leiðréttingarvirðisfærsluna með bókunardagsetninguna 10. september.</span><span class="sxs-lookup"><span data-stu-id="a98a7-147">The user in this case has an allowed posting date range from September 11th to September 30th and is thereby not allowed to post the Adjustment Value Entry with Posting Date September 10th.</span></span>  

<span data-ttu-id="a98a7-148">![Leiðrétta kostnað &#45;Færslugögn](media/helene/TechArticleAdjustcost8.png "TechArticleAdjustcost8")</span><span class="sxs-lookup"><span data-stu-id="a98a7-148">![Adjust cost &#45;Item entries data](media/helene/TechArticleAdjustcost8.png "TechArticleAdjustcost8")</span></span>

 <span data-ttu-id="a98a7-149">Grein þekkingargrunns [952996](https://mbs2.microsoft.com/Knowledgebase/kbdisplay.aspx?WTNTZSMNWUKNTMMYXUPYZQPOUXNXSPSYOQQYYMLUQLOYYMWP) fjallar um fleiri aðstæður sem tengjast nefndu villuboði.</span><span class="sxs-lookup"><span data-stu-id="a98a7-149">Knowledge Base article [952996](https://mbs2.microsoft.com/Knowledgebase/kbdisplay.aspx?WTNTZSMNWUKNTMMYXUPYZQPOUXNXSPSYOQQYYMLUQLOYYMWP) discusses additional scenarios related to mentioned error message.</span></span>  

### <a name="scenario-ii-posting-date-on-adjustment-value-entry-versus-posting-date-on-entry-causing-the-adjustment-such-as-revaluation-or-item-charge"></a><span data-ttu-id="a98a7-150">Aðstæður II: Bókunardagsetning á leiðréttingarvirðisfærslum á móti bókunardagsetningu við innfærslu sem veldur leiðréttingu, eins og endurmati eða kostnaðarauka.</span><span class="sxs-lookup"><span data-stu-id="a98a7-150">Scenario II: Posting Date on Adjustment Value Entry versus Posting Date on entry causing the adjustment such as Revaluation or Item charge.</span></span>  

### <a name="revaluation-scenario"></a><span data-ttu-id="a98a7-151">Aðstæður endurmats:</span><span class="sxs-lookup"><span data-stu-id="a98a7-151">Revaluation scenario:</span></span>  
 <span data-ttu-id="a98a7-152">Skilyrði:</span><span class="sxs-lookup"><span data-stu-id="a98a7-152">Prerequisites:</span></span>  

 <span data-ttu-id="a98a7-153">Birgðagrunnur:</span><span class="sxs-lookup"><span data-stu-id="a98a7-153">Inventory setup:</span></span>  

-   <span data-ttu-id="a98a7-154">Sjálfvirk kostnaðarbókun = Já</span><span class="sxs-lookup"><span data-stu-id="a98a7-154">Automatic Cost Posting = Yes</span></span>  

-   <span data-ttu-id="a98a7-155">Sjálfvirk kostnaðarleiðrétting=Alltaf</span><span class="sxs-lookup"><span data-stu-id="a98a7-155">Automatic Cost Adjustment=Always</span></span>  

-   <span data-ttu-id="a98a7-156">Meðalkostnaður Teg. útreikn=vara</span><span class="sxs-lookup"><span data-stu-id="a98a7-156">Average Cost Calc. Type=item</span></span>  

-   <span data-ttu-id="a98a7-157">Meðalkostnaðartímabil=Dagur</span><span class="sxs-lookup"><span data-stu-id="a98a7-157">Average Cost Period=Day</span></span>  

 <span data-ttu-id="a98a7-158">Uppsetning fjárhags:</span><span class="sxs-lookup"><span data-stu-id="a98a7-158">General Ledger Setup:</span></span>  

-   <span data-ttu-id="a98a7-159">Bókun leyfð frá = 1. janúar 2014</span><span class="sxs-lookup"><span data-stu-id="a98a7-159">Allow Posting From = January 1st, 2014</span></span>  

-   <span data-ttu-id="a98a7-160">Bókun leyfð til = tómt</span><span class="sxs-lookup"><span data-stu-id="a98a7-160">Allow Posting To = empty</span></span>  

 <span data-ttu-id="a98a7-161">Notandauppsetning:</span><span class="sxs-lookup"><span data-stu-id="a98a7-161">User Setup:</span></span>  

-   <span data-ttu-id="a98a7-162">Bókun leyfð frá = 1. desember 2013.</span><span class="sxs-lookup"><span data-stu-id="a98a7-162">Allow Posting From = December 1st, 2013.</span></span>  

-   <span data-ttu-id="a98a7-163">Bókun leyfð til = tómt</span><span class="sxs-lookup"><span data-stu-id="a98a7-163">Allow Posting to = empty</span></span>  

##### <a name="to-test-the-scenario"></a><span data-ttu-id="a98a7-164">Að prófa aðstæðurnar</span><span class="sxs-lookup"><span data-stu-id="a98a7-164">To test the scenario</span></span>  

1.  <span data-ttu-id="a98a7-165">Stofna TEST vöru:</span><span class="sxs-lookup"><span data-stu-id="a98a7-165">Create item TEST:</span></span>  

     <span data-ttu-id="a98a7-166">Grunnmælieining = STK</span><span class="sxs-lookup"><span data-stu-id="a98a7-166">Base unit of measure = PCS</span></span>  

     <span data-ttu-id="a98a7-167">Kostnaðarútreikningur = Meðaltal</span><span class="sxs-lookup"><span data-stu-id="a98a7-167">Costing Method = Average</span></span>  

     <span data-ttu-id="a98a7-168">Velja valkvæða bókunarflokka.</span><span class="sxs-lookup"><span data-stu-id="a98a7-168">Select optional posting groups.</span></span>  

2.  <span data-ttu-id="a98a7-169">Opna birgðabók, stofna og bóka línu á eftirfarandi hátt:</span><span class="sxs-lookup"><span data-stu-id="a98a7-169">Open Item Journal, create and post a line as follows:</span></span>  

     <span data-ttu-id="a98a7-170">Bókunardagsetning = 15. desember, 2013</span><span class="sxs-lookup"><span data-stu-id="a98a7-170">Posting Date = December 15th, 2013</span></span>  

     <span data-ttu-id="a98a7-171">Vara = TEST</span><span class="sxs-lookup"><span data-stu-id="a98a7-171">Item = TEST</span></span>  

     <span data-ttu-id="a98a7-172">Tegund færslu = Innkaup</span><span class="sxs-lookup"><span data-stu-id="a98a7-172">Entry Type = Purchase</span></span>  

     <span data-ttu-id="a98a7-173">Magn = 100</span><span class="sxs-lookup"><span data-stu-id="a98a7-173">Quantity = 100</span></span>  

     <span data-ttu-id="a98a7-174">Ein.upphæð = 10</span><span class="sxs-lookup"><span data-stu-id="a98a7-174">Unit Amount = 10</span></span>  

3.  <span data-ttu-id="a98a7-175">Opna birgðabók, stofna og bóka línu á eftirfarandi hátt:</span><span class="sxs-lookup"><span data-stu-id="a98a7-175">Open Item Journal, create and post a line as follows:</span></span>  

     <span data-ttu-id="a98a7-176">Dagsetning = 20. desember 2013</span><span class="sxs-lookup"><span data-stu-id="a98a7-176">Date = December 20th, 2013</span></span>  

     <span data-ttu-id="a98a7-177">Vara = TEST</span><span class="sxs-lookup"><span data-stu-id="a98a7-177">Item = TEST</span></span>  

     <span data-ttu-id="a98a7-178">Tegund færslu = Neikvæð leiðrétting</span><span class="sxs-lookup"><span data-stu-id="a98a7-178">Entry Type = Negative Adjustment</span></span>  

     <span data-ttu-id="a98a7-179">Magn = 2</span><span class="sxs-lookup"><span data-stu-id="a98a7-179">Quantity = 2</span></span>  

4.  <span data-ttu-id="a98a7-180">Opna birgðabók, stofna og bóka línu á eftirfarandi hátt:</span><span class="sxs-lookup"><span data-stu-id="a98a7-180">Open Item Journal, create and post a line as follows:</span></span>  

     <span data-ttu-id="a98a7-181">Dagsetning = 15. janúar 2014</span><span class="sxs-lookup"><span data-stu-id="a98a7-181">Date = January 15th, 2014</span></span>  

     <span data-ttu-id="a98a7-182">Vara = TEST</span><span class="sxs-lookup"><span data-stu-id="a98a7-182">Item = TEST</span></span>  

     <span data-ttu-id="a98a7-183">Tegund færslu = Neikvæð leiðrétting</span><span class="sxs-lookup"><span data-stu-id="a98a7-183">Entry Type = Negative Adjustment</span></span>  

     <span data-ttu-id="a98a7-184">Magn = 3</span><span class="sxs-lookup"><span data-stu-id="a98a7-184">Quantity = 3</span></span>  

5.  <span data-ttu-id="a98a7-185">Opna endurmatsbók, stofna og bóka línu á eftirfarandi hátt:</span><span class="sxs-lookup"><span data-stu-id="a98a7-185">Open Revaluation Journal, create and post a line as follows:</span></span>  

     <span data-ttu-id="a98a7-186">Vara = TEST</span><span class="sxs-lookup"><span data-stu-id="a98a7-186">Item = TEST</span></span>  

     <span data-ttu-id="a98a7-187">Gildir-fyrir færslu = veldu innkaupafærsla bókuð í skrefi 2.</span><span class="sxs-lookup"><span data-stu-id="a98a7-187">Applies-to Entry = select Purchase entry posted at step 2.</span></span> <span data-ttu-id="a98a7-188">Bókunardagsetning endurmats verður sú sama og fyrir færsluna sem hún leiðréttir.</span><span class="sxs-lookup"><span data-stu-id="a98a7-188">The Posting Date of the revaluation will be the same as the entry it adjusts.</span></span>  

     <span data-ttu-id="a98a7-189">Kostnaðarverð endurmetið = 40</span><span class="sxs-lookup"><span data-stu-id="a98a7-189">Unit Cost Revalued = 40</span></span>  

 <span data-ttu-id="a98a7-190">Eftirfarandi birgðahöfuðbók og virðisfærslur hafa verið bókaðar:</span><span class="sxs-lookup"><span data-stu-id="a98a7-190">The following Item Ledger and Value Entries have been posted:</span></span>  

<span data-ttu-id="a98a7-191">![Leiðrétta kostnað &#45;Færslugögn vöru](media/helene/TechArticleAdjustcost9.png "TechArticleAdjustcost9")</span><span class="sxs-lookup"><span data-stu-id="a98a7-191">![Adjust cost &#45;Item entries data](media/helene/TechArticleAdjustcost9.png "TechArticleAdjustcost9")</span></span>

 <span data-ttu-id="a98a7-192">![Leiðrétta kostnað &#45;Færslugögn vöru](media/helene/TechArticleAdjustcost10.png "TechArticleAdjustcost10")</span><span class="sxs-lookup"><span data-stu-id="a98a7-192">![Adjust cost &#45;Item entries data](media/helene/TechArticleAdjustcost10.png "TechArticleAdjustcost10")</span></span>

 <span data-ttu-id="a98a7-193">Runuvinnslan Leiðréttur kostnaður - Birgðafærslur hefur borið kennsl á breytingar á kostnaði og leiðrétti neikvæðu leiðréttingarnar.</span><span class="sxs-lookup"><span data-stu-id="a98a7-193">The Adjust Cost – Item entries batch job has recognized a change in cost and adjusted the Negative Adjustments.</span></span>  

 <span data-ttu-id="a98a7-194">**Endurskoðun bókunardagsetninga á stofnuðum leiðréttingarvirðisfærslum:** Fyrstu leyfilegu bókunardagsetningar sem runuvinnslan Leiðréttur kostnaður - Birgðafærslur verður að tengjast er 1. janúar 2014 eins kemur fram í fjárhagsgrunni.</span><span class="sxs-lookup"><span data-stu-id="a98a7-194">**Review of Posting Dates on created Adjustment Value Entries:** The earliest allowed Posting Date the Adjust Cost - Item Entries batch job has to relate to is January 1st, 2014 as stated in the General Ledger Setup.</span></span>  

 <span data-ttu-id="a98a7-195">**Neikvæð leiðrétting í skrefi 3:** úthlutuð bókunardagsetning er 1. janúar, veitt af fjárhagsgrunni.</span><span class="sxs-lookup"><span data-stu-id="a98a7-195">**Negative Adjustment in step 3:** assigned Posting Date is January 1st, provided by General Ledger Setup.</span></span> <span data-ttu-id="a98a7-196">Bókunardagsetning virðisfærslunnar sem heyrir undir leiðréttingu er 20. desember 2013.</span><span class="sxs-lookup"><span data-stu-id="a98a7-196">The Posting Date of the Value Entry in scope for adjustment is December 20, 2013.</span></span> <span data-ttu-id="a98a7-197">Samkvæmt fjárhagsgrunni er dagsetningin ekki innan leyfilegs dagsetningabils bókunar.</span><span class="sxs-lookup"><span data-stu-id="a98a7-197">According to General Ledger Setup the date is not within allowed posting date range.</span></span> <span data-ttu-id="a98a7-198">Þess vegna er bókunardagsetningunni, sem er nefnd í Bókun leyfð frá reit fjárhagsgrunns, úthlutað á leiðrétttingarvirðisfærsluna.</span><span class="sxs-lookup"><span data-stu-id="a98a7-198">Therefore the Posting Date stated in the Allow Posting From field in the General Ledger Setup is assigned to the Adjustment Value Entry.</span></span>  

 <span data-ttu-id="a98a7-199">**Neikvæð leiðrétting í skrefi 4:** úthlutuð bókunardagsetning er 15. janúar.</span><span class="sxs-lookup"><span data-stu-id="a98a7-199">**Negative Adjustment in step 4:** assigned Posting Date is January 15th.</span></span> <span data-ttu-id="a98a7-200">Virðisfærslan sem heyrir undir leiðréttingu er með bókunardagsetninguna 15. janúar, sem er innan leyfilegs dagsetningabils bókunar samkvæmt fjárhagsgrunni.</span><span class="sxs-lookup"><span data-stu-id="a98a7-200">The Value Entry in scope of adjustment has Posting Date January 15th, which is within the allowed posting date range according to General Ledger Setup.</span></span>  

 <span data-ttu-id="a98a7-201">Leiðréttingin sem gerð var fyrir neikvæðu leiðréttinguna í skrefi 3 veldur umræðu.</span><span class="sxs-lookup"><span data-stu-id="a98a7-201">The adjustment made for the Negative Adjustment in step 3 causes discussion.</span></span> <span data-ttu-id="a98a7-202">Hagstæða bókunardagsetningin fyrir leiðréttingarvirðisfærsluna hefði verið 20. desember eða að minnsta kosti í desember þar sem endurmatið sem olli breytingunni á kostnaði seldrar vöru var bókað í desember.</span><span class="sxs-lookup"><span data-stu-id="a98a7-202">The favorable Posting Date for the Adjustment Value Entry would have been December 20th or at least within December as the revaluation causing the change in COGS was posted in December.</span></span>  

 <span data-ttu-id="a98a7-203">Til að ná leiðréttingu í desember á neikvæðu leiðréttingunni í 3. skrefi þarf fjárhagsgrunnurinn, Bókun leyfð frá reit, að tilgreina dagsetningu í desember.</span><span class="sxs-lookup"><span data-stu-id="a98a7-203">To achieve adjustment in December of the Negative Adjustment in step 3, the General Ledger Setup, Allow Posting From field, need to state a date in December.</span></span>  

 <span data-ttu-id="a98a7-204">**Niðurstaða:**</span><span class="sxs-lookup"><span data-stu-id="a98a7-204">**Conclusion:**</span></span>  

 <span data-ttu-id="a98a7-205">Með reynslu af þessari atburðarás, miðað við hentugastu uppsetningu leyfilegs dagsetningabils bókunar fyrir fyrirtæki, gæti eftirfarandi verið gagnlegt: Svo lengi sem er heimilt að bóka breytingar á birgðaverðmæti á tímabili, desember í þessu tilviki, ætti uppsetningin sem fyrirtækið notar fyrir dagsetningabil sem er leyfilegt að bóka að vera í takt við þessa ákvörðun.</span><span class="sxs-lookup"><span data-stu-id="a98a7-205">With the experiences from this scenario, considering most suitable setup of allowed posting date range for a company, the following might be useful: As long as changes in inventory value is allowed to be posted in a period, December in this case, the setup the company uses for allowed posting date ranges should be aligned with this decision.</span></span> <span data-ttu-id="a98a7-206">Bókun leyfð frá í fjárhagsgrunni, þar sem fram kemur 1. desember, myndi leyfa að áframsenda endurmatið sem gert var í desember á færslur á útleið, sem verða fyrir áhrifum, á sama tímabilinu.</span><span class="sxs-lookup"><span data-stu-id="a98a7-206">The Allow Posting From in the General Ledger Setup, stating December 1st  would allow the revaluation made in December to be forwarded to affected outbound entries in the same period.</span></span>  

 <span data-ttu-id="a98a7-207">Notendahópar sem ekki mega bóka í desember en í janúar, sem fjárhagsgrunnur átti líklega að takmarka í þessum aðstæðum, ætti frekar að staðsetja í notandauppsetningu.</span><span class="sxs-lookup"><span data-stu-id="a98a7-207">User groups not allowed to post in December but in January, which was probably intended to be limited by the General Ledger Setup in this scenario, should instead be addressed via the User setup.</span></span>  

### <a name="item-charge-scenario"></a><span data-ttu-id="a98a7-208">Aðstæður kostnaðarauka:</span><span class="sxs-lookup"><span data-stu-id="a98a7-208">Item charge scenario:</span></span>  
 <span data-ttu-id="a98a7-209">Skilyrði:</span><span class="sxs-lookup"><span data-stu-id="a98a7-209">Prerequisites:</span></span>  

 <span data-ttu-id="a98a7-210">Birgðagrunnur:</span><span class="sxs-lookup"><span data-stu-id="a98a7-210">Inventory setup:</span></span>  

-   <span data-ttu-id="a98a7-211">Sjálfvirk kostnaðarbókun = Já</span><span class="sxs-lookup"><span data-stu-id="a98a7-211">Automatic Cost Posting = Yes</span></span>  

-   <span data-ttu-id="a98a7-212">Sjálfvirk kostnaðarleiðrétting=Alltaf</span><span class="sxs-lookup"><span data-stu-id="a98a7-212">Automatic Cost Adjustment=Always</span></span>  

-   <span data-ttu-id="a98a7-213">Meðalkostnaður Teg. útreikn=vara</span><span class="sxs-lookup"><span data-stu-id="a98a7-213">Average Cost Calc. Type=item</span></span>  

-   <span data-ttu-id="a98a7-214">Meðalkostnaðartímabil=Dagur</span><span class="sxs-lookup"><span data-stu-id="a98a7-214">Average Cost Period=Day</span></span>  

 <span data-ttu-id="a98a7-215">Uppsetning fjárhags:</span><span class="sxs-lookup"><span data-stu-id="a98a7-215">General Ledger Setup:</span></span>  

-   <span data-ttu-id="a98a7-216">Bókun leyfð frá = 1. desember 2013.</span><span class="sxs-lookup"><span data-stu-id="a98a7-216">Allow Posting From = December 1st, 2013.</span></span>  

-   <span data-ttu-id="a98a7-217">Bókun leyfð til = tómt</span><span class="sxs-lookup"><span data-stu-id="a98a7-217">Allow Posting To = empty</span></span>  

 <span data-ttu-id="a98a7-218">Notandauppsetning:</span><span class="sxs-lookup"><span data-stu-id="a98a7-218">User Setup:</span></span>  

-   <span data-ttu-id="a98a7-219">Bókun leyfð frá = 1. desember 2013.</span><span class="sxs-lookup"><span data-stu-id="a98a7-219">Allow Posting From = December 1st, 2013.</span></span>  

-   <span data-ttu-id="a98a7-220">Bókun leyfð til = tómt</span><span class="sxs-lookup"><span data-stu-id="a98a7-220">Allow Posting to = empty</span></span>  

##### <a name="to-test-the-scenario"></a><span data-ttu-id="a98a7-221">Að prófa aðstæðurnar</span><span class="sxs-lookup"><span data-stu-id="a98a7-221">To test the scenario</span></span>  

1.  <span data-ttu-id="a98a7-222">Stofna kostnaðarauka:</span><span class="sxs-lookup"><span data-stu-id="a98a7-222">Create item charge:</span></span>  

     <span data-ttu-id="a98a7-223">Grunnmælieining = STK</span><span class="sxs-lookup"><span data-stu-id="a98a7-223">Base unit of measure = PCS</span></span>  

     <span data-ttu-id="a98a7-224">Kostnaðarútreikningur = Meðaltal</span><span class="sxs-lookup"><span data-stu-id="a98a7-224">Costing Method = Average</span></span>  

     <span data-ttu-id="a98a7-225">Velja valkvæða bókunarflokka.</span><span class="sxs-lookup"><span data-stu-id="a98a7-225">Select optional posting groups.</span></span>  

2.  <span data-ttu-id="a98a7-226">Stofna nýja innkaupapöntun</span><span class="sxs-lookup"><span data-stu-id="a98a7-226">Create new purchase order</span></span>  

     <span data-ttu-id="a98a7-227">Kaupa af lánardrottni nr.: 10000</span><span class="sxs-lookup"><span data-stu-id="a98a7-227">Buy-from Vendor No.: 10000</span></span>  

     <span data-ttu-id="a98a7-228">Bókunardagsetning = 15. desember, 2013</span><span class="sxs-lookup"><span data-stu-id="a98a7-228">Posting Date = December 15th, 2013</span></span>  

     <span data-ttu-id="a98a7-229">Reikningsnr. lánardrottins: 1234</span><span class="sxs-lookup"><span data-stu-id="a98a7-229">Vendor Invoice No.: 1234</span></span>  

     <span data-ttu-id="a98a7-230">Á innkaupapöntunarlínunni:</span><span class="sxs-lookup"><span data-stu-id="a98a7-230">On the purchase order line:</span></span>  

     <span data-ttu-id="a98a7-231">Vara = GJALD</span><span class="sxs-lookup"><span data-stu-id="a98a7-231">Item = CHARGE</span></span>  

     <span data-ttu-id="a98a7-232">Magn = 1</span><span class="sxs-lookup"><span data-stu-id="a98a7-232">Quantity = 1</span></span>  

     <span data-ttu-id="a98a7-233">Innkaupsverð = 100</span><span class="sxs-lookup"><span data-stu-id="a98a7-233">Direct Unit Cost = 100</span></span>  

     <span data-ttu-id="a98a7-234">Bóka móttaka og reikningsfæra.</span><span class="sxs-lookup"><span data-stu-id="a98a7-234">Post Receive and Invoice.</span></span>  

3.  <span data-ttu-id="a98a7-235">Stofna nýja sölupöntun:</span><span class="sxs-lookup"><span data-stu-id="a98a7-235">Create new sales order:</span></span>  

     <span data-ttu-id="a98a7-236">Selt til Viðskiptamaður Nr.: 10000</span><span class="sxs-lookup"><span data-stu-id="a98a7-236">Sell-to Customer No.: 10000</span></span>  

     <span data-ttu-id="a98a7-237">Bókunardagsetning = 16. desember 2013</span><span class="sxs-lookup"><span data-stu-id="a98a7-237">Posting Date = December 16th, 2013</span></span>  

     <span data-ttu-id="a98a7-238">Í sölupöntunarlínu:</span><span class="sxs-lookup"><span data-stu-id="a98a7-238">On the sales order line:</span></span>  

     <span data-ttu-id="a98a7-239">Vara = GJALD</span><span class="sxs-lookup"><span data-stu-id="a98a7-239">Item = CHARGE</span></span>  

     <span data-ttu-id="a98a7-240">Magn = 1</span><span class="sxs-lookup"><span data-stu-id="a98a7-240">Quantity = 1</span></span>  

     <span data-ttu-id="a98a7-241">Einingarverð = 135</span><span class="sxs-lookup"><span data-stu-id="a98a7-241">Unit Price = 135</span></span>  

     <span data-ttu-id="a98a7-242">Bóka afhenda og reikningsfæra.</span><span class="sxs-lookup"><span data-stu-id="a98a7-242">Post Ship and Invoice.</span></span>  

4.  <span data-ttu-id="a98a7-243">Uppsetning fjárhags:</span><span class="sxs-lookup"><span data-stu-id="a98a7-243">General Ledger Setup:</span></span>  

     <span data-ttu-id="a98a7-244">Bókun leyfð frá = 1. janúar 2014</span><span class="sxs-lookup"><span data-stu-id="a98a7-244">Allow Posting From = January 1st, 2014</span></span>  

     <span data-ttu-id="a98a7-245">Bókun leyfð til = autt</span><span class="sxs-lookup"><span data-stu-id="a98a7-245">Allow Posting To = blank</span></span>  

5.  <span data-ttu-id="a98a7-246">Stofna nýja innkaupapöntun:</span><span class="sxs-lookup"><span data-stu-id="a98a7-246">Create new purchase order:</span></span>  

     <span data-ttu-id="a98a7-247">Kaupa af lánardrottni nr.: 10000</span><span class="sxs-lookup"><span data-stu-id="a98a7-247">Buy-from Vendor No.: 10000</span></span>  

     <span data-ttu-id="a98a7-248">Bókunardagsetning = 2. janúar 2014</span><span class="sxs-lookup"><span data-stu-id="a98a7-248">Posting Date = January 2nd, 2014</span></span>  

     <span data-ttu-id="a98a7-249">Reikningsnr. lánardrottins: 2345</span><span class="sxs-lookup"><span data-stu-id="a98a7-249">Vendor Invoice No.: 2345</span></span>  

     <span data-ttu-id="a98a7-250">Á innkaupapöntunarlínunni:</span><span class="sxs-lookup"><span data-stu-id="a98a7-250">On the purchase order line:</span></span>  

     <span data-ttu-id="a98a7-251">Kostnaðarauki = JB-FLUTN</span><span class="sxs-lookup"><span data-stu-id="a98a7-251">Item Charge = JB-FREIGHT</span></span>  

     <span data-ttu-id="a98a7-252">Magn = 1</span><span class="sxs-lookup"><span data-stu-id="a98a7-252">Quantity = 1</span></span>  

     <span data-ttu-id="a98a7-253">Innkaupsverð = 3</span><span class="sxs-lookup"><span data-stu-id="a98a7-253">Direct Unit Cost = 3</span></span>  

     <span data-ttu-id="a98a7-254">Úthluta kostnaðarauka á innkaupamóttöku úr skrefi 2.</span><span class="sxs-lookup"><span data-stu-id="a98a7-254">Assign Item Charge to Purchase Receipt from step 2.</span></span>  

     <span data-ttu-id="a98a7-255">Bóka kvittun og reikningsfæra.</span><span class="sxs-lookup"><span data-stu-id="a98a7-255">Post Receipt and Invoice.</span></span>  

     <span data-ttu-id="a98a7-256">![Leiðrétta kostnað &#45;Færslugögn vöru](media/helene/TechArticleAdjustcost11.png "TechArticleAdjustcost11")</span><span class="sxs-lookup"><span data-stu-id="a98a7-256">![Adjust cost &#45;Item entries data](media/helene/TechArticleAdjustcost11.png "TechArticleAdjustcost11")</span></span>

6.  <span data-ttu-id="a98a7-257">Á vinnudaginn 3. janúar kemur innkaupareikningur sem inniheldur viðbótargjald við kaupin sem voru gerð í skrefi 2.</span><span class="sxs-lookup"><span data-stu-id="a98a7-257">On work date January 3rd a purchase invoice arrives, containing an additional item charge to the purchase made in step 2.</span></span> <span data-ttu-id="a98a7-258">Þessi reikningur hefur dagsetningu skjals 30. desember og er því bókaður með bókunardagsetningunni 30. desember 2013.</span><span class="sxs-lookup"><span data-stu-id="a98a7-258">This invoice has document date December 30th and is therefore posted with Posting Date December 30th, 2013.</span></span>  

     <span data-ttu-id="a98a7-259">Stofna nýja innkaupapöntun:</span><span class="sxs-lookup"><span data-stu-id="a98a7-259">Create new purchase order:</span></span>  

     <span data-ttu-id="a98a7-260">Kaupa af lánardrottni nr.: 10000</span><span class="sxs-lookup"><span data-stu-id="a98a7-260">Buy-from Vendor No.: 10000</span></span>  

     <span data-ttu-id="a98a7-261">Bókunardagsetning = 30. desember 2013</span><span class="sxs-lookup"><span data-stu-id="a98a7-261">Posting Date = December 30th, 2013</span></span>  

     <span data-ttu-id="a98a7-262">Reikningsnr. lánardrottins: 3456</span><span class="sxs-lookup"><span data-stu-id="a98a7-262">Vendor Invoice No.: 3456</span></span>  

     <span data-ttu-id="a98a7-263">Á innkaupapöntunarlínunni:</span><span class="sxs-lookup"><span data-stu-id="a98a7-263">On the purchase order line:</span></span>  

     <span data-ttu-id="a98a7-264">Kostnaðarauki = JB-FLUTN</span><span class="sxs-lookup"><span data-stu-id="a98a7-264">Item Charge = JB-FREIGHT</span></span>  

     <span data-ttu-id="a98a7-265">Magn = 1</span><span class="sxs-lookup"><span data-stu-id="a98a7-265">Quantity = 1</span></span>  

     <span data-ttu-id="a98a7-266">Innkaupsverð = 2</span><span class="sxs-lookup"><span data-stu-id="a98a7-266">Direct Unit Cost = 2</span></span>  

     <span data-ttu-id="a98a7-267">Úthluta kostnaðarauka á innkaupamóttöku úr skrefi 2</span><span class="sxs-lookup"><span data-stu-id="a98a7-267">Assign Item Charge to Purchase Receipt from step 2</span></span>  

     <span data-ttu-id="a98a7-268">Bóka kvittun og reikningsfæra.</span><span class="sxs-lookup"><span data-stu-id="a98a7-268">Post Receipt and Invoice.</span></span>  

   <span data-ttu-id="a98a7-269">![Leiðrétta kostnað &#45;Færslugögn vöru](media/helene/TechArticleAdjustcost12.png "TechArticleAdjustcost12")</span><span class="sxs-lookup"><span data-stu-id="a98a7-269">![Adjust cost &#45;Item entries data](media/helene/TechArticleAdjustcost12.png "TechArticleAdjustcost12")</span></span>

 <span data-ttu-id="a98a7-270">Skýrsla birgðavirðis er prentuð frá og með dagsetningunni 31. desember 2013</span><span class="sxs-lookup"><span data-stu-id="a98a7-270">Inventory Valuation report is printed as of Date December 31st , 2013</span></span>  

<span data-ttu-id="a98a7-271">![Leiðrétta kostnað &#45;Færslugögn vöru](media/helene/TechArticleAdjustcost13.png "TechArticleAdjustcost13")</span><span class="sxs-lookup"><span data-stu-id="a98a7-271">![Adjust cost &#45;Item entries data](media/helene/TechArticleAdjustcost13.png "TechArticleAdjustcost13")</span></span>

 <span data-ttu-id="a98a7-272">**Samantekt á aðstæðum:**</span><span class="sxs-lookup"><span data-stu-id="a98a7-272">**Summary of scenario:**</span></span>  

 <span data-ttu-id="a98a7-273">Útlistaðar aðstæður enda með verðmætamati á birgðum sem sýnir magn = 0 á meðan gildið = 2.</span><span class="sxs-lookup"><span data-stu-id="a98a7-273">The described scenario ends up with an Inventory Valuation report demonstrating Quantity = 0 while the Value = 2.</span></span> <span data-ttu-id="a98a7-274">Bókaður kostnaðarauki í skrefi 11 er hluti af birgðaaukningunni í desember á meðan birgðaminnkun sama tímabils verður ekki fyrir áhrifum.</span><span class="sxs-lookup"><span data-stu-id="a98a7-274">The Item charge posted in step 11 is part of the Inventory Increase value of December while the Inventory Decrease of the same period is not affected.</span></span>  

 <span data-ttu-id="a98a7-275">Að fjárhagsgrunnurinn skyldi gefa upp Leyfa bókun frá og með 1. janúar var gott fyrir fyrsta kostnaðaraukann.</span><span class="sxs-lookup"><span data-stu-id="a98a7-275">Having the General Ledger Setup stating Allow Posting From January 1st was a good thing for the first Item charge.</span></span> <span data-ttu-id="a98a7-276">Kostnaður við birgðaaukningu og -minnkun var skráð á sama tímabilið.</span><span class="sxs-lookup"><span data-stu-id="a98a7-276">The costs of the Inventory Increase and Decrease was recorded in the same period.</span></span> <span data-ttu-id="a98a7-277">Fyrir seinni kostnaðaraukann er það hins vegar fjárhagsgrunnurinn sem veldur því að breytingin á kostnaði seldrar vöru verði samþykktur fyrir næsta tímabil.</span><span class="sxs-lookup"><span data-stu-id="a98a7-277">For the second Item charge however, the General Ledger Setup causes the change in COGS to be recognized in the period after.</span></span>  

 <span data-ttu-id="a98a7-278">**Niðurstaða:**</span><span class="sxs-lookup"><span data-stu-id="a98a7-278">**Conclusion:**</span></span>  

 <span data-ttu-id="a98a7-279">Það er áskorun að hafa skýrslu birgðavirðis til að sýna magn = 0 á meðan gildið <> 0.</span><span class="sxs-lookup"><span data-stu-id="a98a7-279">It’s a challenge to have the Inventory Valuation report to demonstrate Quantity = 0 while the Value <> 0.</span></span> <span data-ttu-id="a98a7-280">Í þessu tilfelli er það líka erfiðara að tjá ákjósanlegustu stillingar með því að hafa innkaupareikninga sem koma á sama degi en taka til mismunandi tímabila eða jafnvel reikningsára.</span><span class="sxs-lookup"><span data-stu-id="a98a7-280">In this case it’s also more difficult to express the optimal settings, having purchase invoices arriving the same day but addressing different periods or even fiscal years.</span></span> <span data-ttu-id="a98a7-281">Að færast yfir á nýtt reikningsár krefst yfirleitt einhverrar skipulagningar og sem hluti af því þarf að íhuga nánar ferli leiðréttingarkostnaðar - birgðafærslna, gera sér grein fyrir kostnaði seldra vara.</span><span class="sxs-lookup"><span data-stu-id="a98a7-281">Crossing to a new fiscal year usually requires some planning and as part of that the insight of Adjust Cost – Item entries process, recognizing COGS, is to be considered.</span></span>  

 <span data-ttu-id="a98a7-282">Í þessari atburðarás getur einn möguleiki verið að hafa fjárhagsgrunninn, reitinn Bókun leyfð frá, gefa upp dagsetningu í desember fyrir nokkra daga í viðbót og fresta bókun á fyrsta kostnaðaraukanum svo allir kostnaðir fyrir fyrra tímabil/fjárhagsár verði viðurkenndir fyrir tímabilið sem þeir tilheyra í fyrstu, keyra síðan runuvinnslu Leiðrétts kostnaðar - Birgðafærslna og í kjölfarið færa leyfða bókunardagsetningu yfir á nýtt tímabil\/fjárhagsársins.</span><span class="sxs-lookup"><span data-stu-id="a98a7-282">In this scenario one option could have been to have the General Ledger Setup, field Allow Posting From, stating a date in December for a couple of more days and the posting of the first item charge postponed to allow all costs for the previous period/fiscal year to be recognized for the period they belong to first, having the Adjust Cost – Item entries batch job run and thereafter move the allowed posting date to the new period\/fiscal year.</span></span> <span data-ttu-id="a98a7-283">Fyrsti kostnaðaraukinn með bókunardagsetninguna 2. janúar getur þá verið bókaður.</span><span class="sxs-lookup"><span data-stu-id="a98a7-283">The first item charge with posting date January 2nd could then be posted.</span></span>  

## <a name="history-of-adjust-cost--item-entries-batch-job"></a><span data-ttu-id="a98a7-284">Ferill runuvinnslu Leiðrétts kostnaðar – birgðafærslna</span><span class="sxs-lookup"><span data-stu-id="a98a7-284">History of Adjust Cost – Item entries batch job</span></span>  
 <span data-ttu-id="a98a7-285">Hér fyrir neðan er samantekt á hugmyndinni um að úthluta bókunardagsetningum á leiðrétttingarvirðisfærslum með runuvinnslu leiðrétts kostnaðar - birgðafærslna síðan í útgáfu 3.0.</span><span class="sxs-lookup"><span data-stu-id="a98a7-285">Below is a summary of the concept assigning Posting Dates to Adjustment Value Entries by the Adjust Cost – Item entries batch job since version 3.0.</span></span>  

### <a name="from-version-30370a"></a><span data-ttu-id="a98a7-286">Frá útgáfu 3.0..3.70.A</span><span class="sxs-lookup"><span data-stu-id="a98a7-286">From version 3.0..3.70.A</span></span>  
 <span data-ttu-id="a98a7-287">Í beiðniglugga fyrir runuvinnslu leiðrétts kostnaðar - birgðafærslna þarf notandi að færa inn bókunardagsetningu.</span><span class="sxs-lookup"><span data-stu-id="a98a7-287">In the request form of the Adjust Cost - Item Entries batch job there is a Posting Date to be entered by the user.</span></span> <span data-ttu-id="a98a7-288">Runuvinnslan fer í gegnum allar nauðsynlegar breytingar og stofnar virðisfærslur með bókunardagsetningunni sem hefur verið færð inn í beiðnigluggann.</span><span class="sxs-lookup"><span data-stu-id="a98a7-288">The batch job runs through all necessary changes and creates value entries with the posting date entered in the request form.</span></span> <span data-ttu-id="a98a7-289">Ráðlögð bókunardagsetning er dagurinn í dag.</span><span class="sxs-lookup"><span data-stu-id="a98a7-289">Suggested posting date to use is today’s date.</span></span>  

### <a name="version-370b40"></a><span data-ttu-id="a98a7-290">Útgáfa 3.70.B..4.0</span><span class="sxs-lookup"><span data-stu-id="a98a7-290">Version 3.70.B..4.0</span></span>  
 <span data-ttu-id="a98a7-291">Í beiðniglugga fyrir runuvinnslu leiðrétts kostnaðar - birgðafærslna þarf notandi að færa inn bókunardagsetningu lokaðrar tímabilsfærslu.</span><span class="sxs-lookup"><span data-stu-id="a98a7-291">In the request form of the Adjust Cost - Item Entries batch job there is a Closed Period Entry Posting Date to be entered by the user.</span></span> <span data-ttu-id="a98a7-292">Runuvinnslan fer í gegnum nauðsynlegar breytingar og stofnar virðisfærslur með bókunardagsetningu á yfirbirgðafærslunni (afhendingardagur sölunnar sem leiðréttingin gefur upp).</span><span class="sxs-lookup"><span data-stu-id="a98a7-292">The batch job runs through all necessary changes and creates value entries with the posting date of the parent item ledger entry (shipment date of the sale that the adjustment address).</span></span> <span data-ttu-id="a98a7-293">Ef bókunardagsetning yfirbirgðafærslunnar er ekki innan leyfilegs dagsetningabils bókunar verður bókunardagsetningu lokaðrar tímabilsfærslu úthlutað leiðréttingarvirðisfærslu.</span><span class="sxs-lookup"><span data-stu-id="a98a7-293">If the posting date of the parent item ledger entry is not within allowed posting date range the posting date stated as Closed Period Entry Posting Date will be assigned the Adjustment Value Entry.</span></span> <span data-ttu-id="a98a7-294">Dagsetning telst vera á lokuðu tímabili þegar hún er eldri en dagsetningin í reitnum Bókun leyfð frá í fjárhagsgrunni.</span><span class="sxs-lookup"><span data-stu-id="a98a7-294">A date is considered to be in a closed period when it is earlier than the date in the Allow Posting From field in the General Ledger Setup.</span></span>  

### <a name="from-version-50"></a><span data-ttu-id="a98a7-295">Frá útgáfu 5,0:</span><span class="sxs-lookup"><span data-stu-id="a98a7-295">From version 5.0:</span></span>  
 <span data-ttu-id="a98a7-296">Ekki þarf lengur að gefa upp bókunardagsetningu í beiðniglugga fyrir runuvinnslu leiðrétts kostnaðar - birgðafærslna.</span><span class="sxs-lookup"><span data-stu-id="a98a7-296">There is no longer a posting date to be stated in the request form of the Adjust Cost - Item entries batch job.</span></span> <span data-ttu-id="a98a7-297">Runuvinnslan fer í gegnum allar nauðsynlegar breytingar og stofnar virðisfærslur með bókunardagsetningu virðisfærslunnar sem hún leiðréttir.</span><span class="sxs-lookup"><span data-stu-id="a98a7-297">The batch job runs through all necessary changes and creates value entries with the posting date of the value entry it adjusts.</span></span> <span data-ttu-id="a98a7-298">Ef bókunardagsetningin er ekki innan leyfilegs dagsetningabils bókunar verður bókunardagsetningin í reitnum Bókun leyfð frá í fjárhagsgrunni notuð, EÐA ef birgðatímabil eru notuð, verður eldri dagsetningin af þessum tveimur notuð.</span><span class="sxs-lookup"><span data-stu-id="a98a7-298">If the posting date is not within allowed posting date range the posting date in the Allow Posting From field in the General Ledger Setup, OR if the Inventory periods are used, the later date of the two will be used.</span></span> <span data-ttu-id="a98a7-299">Sjá útskýrt hugtak hér að ofan.</span><span class="sxs-lookup"><span data-stu-id="a98a7-299">See described concept above.</span></span>  

## <a name="history-of-post-inventory-cost-to-gl-batch-job"></a><span data-ttu-id="a98a7-300">Ferill runuvinnslunnar Bóka birgðabreytingar</span><span class="sxs-lookup"><span data-stu-id="a98a7-300">History of Post Inventory cost to G/L batch job</span></span>  
 <span data-ttu-id="a98a7-301">Runuvinnslan Bóka birgðabreytingar er nátengd runuvinnslunni Leiðrétta kostnað - Birgðafærslur og því er ferill runuvinnslunnar að auki tekin saman og deilt hér.</span><span class="sxs-lookup"><span data-stu-id="a98a7-301">The Post Inventory Cost to G/L batch job is closely related to the Adjust Cost – Item entries batch job why the history of this batch job is summarized and shared here as well.</span></span>  

### <a name="from-version-30370a"></a><span data-ttu-id="a98a7-302">Frá útgáfu 3.0..3.70.A</span><span class="sxs-lookup"><span data-stu-id="a98a7-302">From version 3.0..3.70.A</span></span>  
 <span data-ttu-id="a98a7-303">Í beiðniglugga fyrir birgðabreytingar þarf notandi að færa inn bókunardagsetningu.</span><span class="sxs-lookup"><span data-stu-id="a98a7-303">In the request form of the Post Inventory Cost to G/L there is a Posting Date to be entered by the user.</span></span> <span data-ttu-id="a98a7-304">Runuvinnslan keyrir í gegnum allar virðisfærslur innan síunnar, ef það er einhver, og stofnar fjárhagsfærslur þar sem bókunardagsetning er færð inn í beiðnigluggann.</span><span class="sxs-lookup"><span data-stu-id="a98a7-304">The batch job runs through all value entries within the filter, if any, and creates General Ledger Entries with Posting Date entered in the request form.</span></span>  

### <a name="version-370b40"></a><span data-ttu-id="a98a7-305">Útgáfa 3.70.B..4.0</span><span class="sxs-lookup"><span data-stu-id="a98a7-305">Version 3.70.B..4.0</span></span>  
 <span data-ttu-id="a98a7-306">Í beiðniglugga birgðabreytinga er reiturinn bókunardagsetning lokaðrar tímabilsfærslu tiltækur.</span><span class="sxs-lookup"><span data-stu-id="a98a7-306">In the request form of the Post Inventory Cost to G/L the Closed Period Entry Posting Date field is available.</span></span> <span data-ttu-id="a98a7-307">Forritið notar dagsetninguna sem þú slærð inn í þennan reit sem bókunardagsetningu fyrir fjárhagsfærslurnar sem það stofnar fyrir virðisfærslur, en bókunardagsetningar þeirra eru á lokuðu reikningstímabili.</span><span class="sxs-lookup"><span data-stu-id="a98a7-307">The program uses the date you enter in this field as the posting date for the general ledger entries it creates for value entries whose posting dates are in closed accounting periods.</span></span> <span data-ttu-id="a98a7-308">Að öðrum kosti munu fjárhagsfærslurnar hafa sömu bókunardagsetningu og upprunalegu virðisfærslurnar.</span><span class="sxs-lookup"><span data-stu-id="a98a7-308">Otherwise, the general ledger entries will have the same posting date as the original value entries.</span></span> <span data-ttu-id="a98a7-309">Dagsetning telst vera á lokuðu tímabili þegar hún er eldri en dagsetningin í reitnum Bókun leyfð frá í fjárhagsgrunni.</span><span class="sxs-lookup"><span data-stu-id="a98a7-309">A date is considered to be in a closed period when it is earlier than the date in the Allow Posting From field in the General Ledger Setup.</span></span> <span data-ttu-id="a98a7-310">Ef fjár\/hagur er bókaður fyrir hvern bókunarflokk munu fjárhagsfærslurnar fá bókunardagsetninguna sem er tilgreind í reit bókunardagsetningar í beiðniglugganum.</span><span class="sxs-lookup"><span data-stu-id="a98a7-310">If posting to G\/L Per Posting Group, the general ledger entries will have the posting date that is specified in the Posting Date field in the request form.</span></span>  

 <span data-ttu-id="a98a7-311">Í útgáfum 3 og 4 skannar runuvinnslan allar virðisfærslur til að greina hvort einhverjar virðisfærslur séu til þar sem kostnaðarupphæð (raunveruleg) er frábrugðin kostnaði bókuðum í fjárhag.</span><span class="sxs-lookup"><span data-stu-id="a98a7-311">In version 3 and 4 the batch job scans all value entries to detect if there are any value entries where Cost Amount (Actual) differs from Cost Posted to G/L.</span></span> <span data-ttu-id="a98a7-312">Ef finnst mismunur verður frábrugðna upphæðin bókuð í fjárhagsfærslu.</span><span class="sxs-lookup"><span data-stu-id="a98a7-312">If there is a difference detected the differing amount will be posted in a G/L entry.</span></span> <span data-ttu-id="a98a7-313">Ef bókun áætlaðs kostnaðar er notaður er unnið úr samsvarandi reitum á sama hátt.</span><span class="sxs-lookup"><span data-stu-id="a98a7-313">If expected cost posting is used corresponding fields are processed in the same way.</span></span>  

<span data-ttu-id="a98a7-314">![Leiðrétta kostnað &#45;Færslugögn vöru](media/helene/TechArticleAdjustcost14.png "TechArticleAdjustcost14")</span><span class="sxs-lookup"><span data-stu-id="a98a7-314">![Adjust cost &#45;Item entries data](media/helene/TechArticleAdjustcost14.png "TechArticleAdjustcost14")</span></span>

### <a name="from-version-50"></a><span data-ttu-id="a98a7-315">Frá útgáfu 5,0:</span><span class="sxs-lookup"><span data-stu-id="a98a7-315">From version 5.0:</span></span>  
 <span data-ttu-id="a98a7-316">Ekki þarf lengur að tilgreina bókunardagsetningu í beiðniglugganum fyrir runuvinnslu birgðabreytinga.</span><span class="sxs-lookup"><span data-stu-id="a98a7-316">There is no longer a posting date to be stated in the request form of the Post Inventory Cost to G/L batch job.</span></span> <span data-ttu-id="a98a7-317">Fjárhagsfærslan er búin til með sömu bókunardagsetningu og tengd virðisfærsla.</span><span class="sxs-lookup"><span data-stu-id="a98a7-317">The G/L entry is created with the same Posting Date as the related value entry.</span></span> <span data-ttu-id="a98a7-318">Til þess að ljúka runuvinnslunni verður leyfilegt dagsetningabil bókunar að leyfa bókunardagsetningu stofnuðu fjárhagsfærslunnar.</span><span class="sxs-lookup"><span data-stu-id="a98a7-318">In order to complete the batch job the allowed posting date range must allow the Posting Date of the created G/L entry.</span></span> <span data-ttu-id="a98a7-319">Ef ekki, verður að enduropna tímabundið leyfilegt dagsetningabil bókunar með því að breyta eða fjarlægja dagsetningarnar í reitunum Bókun leyfð frá og til í fjárhagsgrunni.</span><span class="sxs-lookup"><span data-stu-id="a98a7-319">If not, the allowed posting date range must be temporarily re-opened by changing or removing the dates in the Allow Posting From and To fields in the General Ledger Setup.</span></span> <span data-ttu-id="a98a7-320">Til að koma í veg fyrir afstemmingarvandamál er nauðsynlegt að bókunardagsetning fjárhagsfærslu samsvari bókunardagsetningu virðisfærslu.</span><span class="sxs-lookup"><span data-stu-id="a98a7-320">To avoid reconciliation issues it is required that Posting Date of the G/L Entry corresponds to the Posting Date of the Value Entry.</span></span>  

 <span data-ttu-id="a98a7-321">Runuvinnslan skannar tafla 5811 - Bóka virðisfærslu í fjárhag, til að bera kennsl á virðisfærslur sem heyra undir bókun í fjárhag.</span><span class="sxs-lookup"><span data-stu-id="a98a7-321">The batch job scans Table 5811 - Post Value Entry to G/L, to identify the Value Entries in scope for posting to General Ledger.</span></span> <span data-ttu-id="a98a7-322">Taflan var tæmd eftir heppnaða keyrslu.</span><span class="sxs-lookup"><span data-stu-id="a98a7-322">After successful run the table is emptied.</span></span>  

 <span data-ttu-id="a98a7-323">Tekið verður vel á móti öllum athugasemdum um frekari þróun á ferlum og skjalavinnu.</span><span class="sxs-lookup"><span data-stu-id="a98a7-323">Any feedback to how this process and documentation can be further developed is very welcome.</span></span>  

 <span data-ttu-id="a98a7-324">Helena Holmin</span><span class="sxs-lookup"><span data-stu-id="a98a7-324">Helene Holmin</span></span>  

 <span data-ttu-id="a98a7-325">Dynamics NAV Hækkunarhönnuður</span><span class="sxs-lookup"><span data-stu-id="a98a7-325">Dynamics NAV Escalation Engineer</span></span>  

## <a name="see-also"></a><span data-ttu-id="a98a7-326">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="a98a7-326">See Also</span></span>  
[<span data-ttu-id="a98a7-327">Hönnunarupplýsingar: Birgðakostnaður</span><span class="sxs-lookup"><span data-stu-id="a98a7-327">Design Details: Inventory Costing</span></span>](design-details-inventory-costing.md)  
[<span data-ttu-id="a98a7-328">Hönnunarupplýsingar: Umsókn vöru</span><span class="sxs-lookup"><span data-stu-id="a98a7-328">Design Details: Item Application</span></span>](design-details-item-application.md)  

