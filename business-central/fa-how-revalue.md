---
title: Endurmeta eignir| Microsoft Docs
description: "Kynntu þér hvernig skal laga virði eigna, skrá nýjar upphæðir sem niðurfærslu eða uppfærslu og bóka viðbótarkaupverð."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: ddd5ac6a8252b066700b8fd0058f7f772e4fd01b
ms.contentlocale: is-is
ms.lasthandoff: 09/28/2018

---
# <a name="revalue-fixed-assets"></a><span data-ttu-id="2dd9d-103">Endurmeta eignir</span><span class="sxs-lookup"><span data-stu-id="2dd9d-103">Revalue Fixed Assets</span></span>
<span data-ttu-id="2dd9d-104">Endurmat eigna getur samanstaðið af uppfærslu, niðurfærslu, og leiðréttingum á almennu virði.</span><span class="sxs-lookup"><span data-stu-id="2dd9d-104">Revaluation of fixed assets can consist of appreciations, write-downs, or general value adjustments.</span></span>

<span data-ttu-id="2dd9d-105">Þegar virði eignar hefur hækkað, er bókuð færslubókarlínu með hærri upphæð, uppfærslu í afskriftabókina.</span><span class="sxs-lookup"><span data-stu-id="2dd9d-105">When the value of a fixed asset has increased, you post a journal line with a higher amount, an appreciation, to the depreciation book.</span></span> <span data-ttu-id="2dd9d-106">Nýtt verð er skráð sem uppfærslu samkvæmt bókunargrunni eigna.</span><span class="sxs-lookup"><span data-stu-id="2dd9d-106">The new amount is recorded as an appreciation according to the fixed asset posting setup.</span></span>

<span data-ttu-id="2dd9d-107">Þegar virði eignar hefur lækkað, bókarðu færslubókarlínu með lægri upphæð, niðurfærslu, í afskriftabók.</span><span class="sxs-lookup"><span data-stu-id="2dd9d-107">When the value of a fixed asset has decreased, you post a journal line with a lower amount, a write-down, to the depreciation book.</span></span> <span data-ttu-id="2dd9d-108">Nýtt verð er skráð sem niðurfærslu samkvæmt bókunargrunni eigna.</span><span class="sxs-lookup"><span data-stu-id="2dd9d-108">The new amount is recorded as a write-down according to the fixed asset posting setup.</span></span>

<span data-ttu-id="2dd9d-109">Endurmat er notað til að laga virði margra eigna, til dæmis, að almennum verðbreytingum.</span><span class="sxs-lookup"><span data-stu-id="2dd9d-109">Indexation is used to adjust multiple fixed asset values, for example per general price changes.</span></span> <span data-ttu-id="2dd9d-110">Hægt er að nota keyrsluna **Endurmat eigna** til að breyta ýmsum upphæðum, svo sem upphæðum niðurfærslna og uppfærslna.</span><span class="sxs-lookup"><span data-stu-id="2dd9d-110">The **Index Fixed Assets** batch job can be used to change various amounts, such as write-down and appreciation amounts.</span></span>

## <a name="to-post-an-appreciation-from-the-fixed-asset-gl-journal"></a><span data-ttu-id="2dd9d-111">Bóka uppfærslu úr fjárhagsbók eigna</span><span class="sxs-lookup"><span data-stu-id="2dd9d-111">To post an appreciation from the fixed asset G/L journal</span></span>
1. <span data-ttu-id="2dd9d-112">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Eignafjárhagsbækur** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="2dd9d-112">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **FA G/L Journals**, and then choose the related link.</span></span>  
2. <span data-ttu-id="2dd9d-113">Stofnaður er upprunaleg Færslubókarlína og reitirnir fylltir út eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="2dd9d-113">Create an initial journal line and fill in the fields as necessary.</span></span>
3. <span data-ttu-id="2dd9d-114">Í reitnum **Eignabókunartegund** er valinn **endurmat**.</span><span class="sxs-lookup"><span data-stu-id="2dd9d-114">In the **FA Posting Type** field, select **Revaluation**.</span></span>
4. <span data-ttu-id="2dd9d-115">Valið er **Setja inn mótreikn. eigna** aðgerð.</span><span class="sxs-lookup"><span data-stu-id="2dd9d-115">Choose the **Insert FA Bal. Account** action.</span></span> <span data-ttu-id="2dd9d-116">Seinni færslubókarlína er búin til fyrir mótreiknings sem er sett upp fyrir bókun uppfærslu.</span><span class="sxs-lookup"><span data-stu-id="2dd9d-116">A second journal line is created for the balancing account that is set up for appreciation posting.</span></span>

    > [!NOTE]  
    >   <span data-ttu-id="2dd9d-117">Skref 4 virkar eingöngu ef búið er að setja upp eftirfarandi: Í **Eignabókunarflokksspjald** glugganum fyrir bókunarflokkur eigna, inniheldur reiturinn **endurmatsreikningur** debetreikning fjárhags og **Mótreikningur endurmats** inniheldur fjárhagsreikninginn sem á að bóka mótfærslur í fyrir endurmat.</span><span class="sxs-lookup"><span data-stu-id="2dd9d-117">Step 4 only works if you have set up the following: In the **FA Posting Group Card** window for the posting group of the fixed asset, the **Appreciation Account** field contains the general ledger debit account and the **Appreciation Bal. Account** field contains the general ledger account to which you want to post balancing entries for appreciation.</span></span> <span data-ttu-id="2dd9d-118">Nánari upplýsingar eru í setja upp bókunarflokka eigna hlutanum í [Setja Upp almennar upplýsingar um eignir](fa-how-setup-general.md).</span><span class="sxs-lookup"><span data-stu-id="2dd9d-118">For more information, see the "To set up fixed asset posting groups" section in [Set Up General Fixed Asset Information](fa-how-setup-general.md).</span></span>  
5. <span data-ttu-id="2dd9d-119">Valið er **Bóka** aðgerðin.</span><span class="sxs-lookup"><span data-stu-id="2dd9d-119">Choose the **Post** action.</span></span>

## <a name="to-post-a-write-down-from-the-fixed-asset-gl-journal"></a><span data-ttu-id="2dd9d-120">Bóka niðurfærsla úr fjárhagsbók eigna</span><span class="sxs-lookup"><span data-stu-id="2dd9d-120">To post a write-down from the fixed asset G/L journal</span></span>
1. <span data-ttu-id="2dd9d-121">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Eignafjárhagsbækur** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="2dd9d-121">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **FA G/L Journals**, and then choose the related link.</span></span>  
2. <span data-ttu-id="2dd9d-122">Stofnaður er upprunaleg Færslubókarlína og reitirnir fylltir út eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="2dd9d-122">Create an initial journal line, and fill in the fields as necessary.</span></span>
3. <span data-ttu-id="2dd9d-123">Í reitnum **Eignabókunartegund** er valinn **niðurfærsla**.</span><span class="sxs-lookup"><span data-stu-id="2dd9d-123">In the **FA Posting Type** field, select **Write-Down**.</span></span>
4. <span data-ttu-id="2dd9d-124">Valið er **Setja inn mótreikn. eigna** aðgerð.</span><span class="sxs-lookup"><span data-stu-id="2dd9d-124">Choose the **Insert FA Bal. Account** action.</span></span> <span data-ttu-id="2dd9d-125">Seinni færslubókarlína er búin til fyrir mótreiknings sem er sett upp fyrir bókun niðurfærslu.</span><span class="sxs-lookup"><span data-stu-id="2dd9d-125">A second journal line is created for the balancing account that is set up for write-down posting.</span></span>

    > [!NOTE]  
    >   <span data-ttu-id="2dd9d-126">Skref 4 virkar eingöngu ef búið er að setja upp eftirfarandi: Í **Eignabókunarflokksspjald** glugganum fyrir bókunarflokkur eigna, inniheldur reiturinn **niðurfærslureikningur** kreditreikning fjárhags og **Útgjaldareikningur niðurfærslu** inniheldur fjárhagsreikninginn sem á að bóka mótfærslur í fyrir niðurfærslur.</span><span class="sxs-lookup"><span data-stu-id="2dd9d-126">Step 4 only works if you have set up the following: In the **FA Posting Group Card** window for the posting group of the fixed asset, the **Write-Down Account** field contains the general ledger credit account and the **Write-Down Expense Account** field contains the general ledger debit account to which you want to post balancing entries for write-downs.</span></span> <span data-ttu-id="2dd9d-127">Nánari upplýsingar eru í setja upp bókunarflokka eigna hlutanum í [Setja Upp almennar upplýsingar um eignir](fa-how-setup-general.md).</span><span class="sxs-lookup"><span data-stu-id="2dd9d-127">For more information, see the "To set up fixed asset posting groups" section in [Set Up General Fixed Asset Information](fa-how-setup-general.md).</span></span>
5. <span data-ttu-id="2dd9d-128">Valið er **Bóka** aðgerðin.</span><span class="sxs-lookup"><span data-stu-id="2dd9d-128">Choose the **Post** action.</span></span>

## <a name="to-perform-general-revaluation-of-fixed-assets"></a><span data-ttu-id="2dd9d-129">Framkvæma almennt endurmat eigna</span><span class="sxs-lookup"><span data-stu-id="2dd9d-129">To perform general revaluation of fixed assets</span></span>
<span data-ttu-id="2dd9d-130">Endurmat er notað til að laga virði margra eigna, til dæmis, að almennum verðbreytingum.</span><span class="sxs-lookup"><span data-stu-id="2dd9d-130">Indexation is used to adjust multiple fixed asset values, for example per general price changes.</span></span> <span data-ttu-id="2dd9d-131">Hægt er að nota keyrsluna **Endurmat eigna** til að breyta ýmsum upphæðum, svo sem upphæðum niðurfærslna og uppfærslna.</span><span class="sxs-lookup"><span data-stu-id="2dd9d-131">The **Index Fixed Assets** batch job can be used to change various amounts, such as write-down and appreciation amounts.</span></span> <span data-ttu-id="2dd9d-132">**Leyfa Endurmat** gátreiturinn á **Afskriftabók** glugganum verður að vera valinn.</span><span class="sxs-lookup"><span data-stu-id="2dd9d-132">The **Allow Indexation** check box in the **Depreciation Book** window must be selected.</span></span>

1. <span data-ttu-id="2dd9d-133">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Endurmat Eigna** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="2dd9d-133">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Index Fixed Assets**, and then choose the related link.</span></span>  
2. <span data-ttu-id="2dd9d-134">Fyllið inn í svæðin eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="2dd9d-134">Fill in the fields as necessary.</span></span>
3. <span data-ttu-id="2dd9d-135">Velja hnappinn **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="2dd9d-135">Choose the **OK** button.</span></span>

    <span data-ttu-id="2dd9d-136">Endurmatslínur eru búnar til samkvæmt stillingu í skref 2.</span><span class="sxs-lookup"><span data-stu-id="2dd9d-136">Revaluation lines are created per your settings in step 2.</span></span> <span data-ttu-id="2dd9d-137">Línur eru búnar til annaðhvort í færslubók eigna, allt eftir sniðmáti þínu og uppsetningu keyrslu í glugganum **Eignabókargrunnur**.</span><span class="sxs-lookup"><span data-stu-id="2dd9d-137">The lines are created in either the fixed asset journal or the fixed asset G/L journal, depending on your template and batch setup in the **FA Journal Setup** window.</span></span> <span data-ttu-id="2dd9d-138">Frekari upplýsingar eru í [Uppsetning almennra eignaupplýsinga](fa-how-setup-general.md).</span><span class="sxs-lookup"><span data-stu-id="2dd9d-138">For more information, see [Set Up General Fixed Asset Information](fa-how-setup-general.md).</span></span>
4. <span data-ttu-id="2dd9d-139">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Eignafjárhagsbækur** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="2dd9d-139">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **FA G/L Journals**, and then choose the related link.</span></span>  
5. <span data-ttu-id="2dd9d-140">Velja bókina með eignir sem á að endurmeta og síðan valið aðgerðin **Færslur**.</span><span class="sxs-lookup"><span data-stu-id="2dd9d-140">Select the journal with the fixed assets that you want to revalue, and then choose the **Ledger Entries** action.</span></span>  
6. <span data-ttu-id="2dd9d-141">Athugaðu Stofnaðar færslur, og síðan valið **Bóka** aðgerð til að bóka bókina.</span><span class="sxs-lookup"><span data-stu-id="2dd9d-141">Check the created entries, and then choose the **Post** action to post the journal.</span></span>

    > [!TIP]  
    >   <span data-ttu-id="2dd9d-142">Ef endurmatstölurnar eru aðeins til sýnis er hægt að búa til sérstaka afskriftabók til að geyma þær í.</span><span class="sxs-lookup"><span data-stu-id="2dd9d-142">If the index figures are for simulation purposes only, you can create a special depreciation book to store them in.</span></span> <span data-ttu-id="2dd9d-143">Þá hafa þessar færslur ekki áhrif á aðrar afskriftabækur.</span><span class="sxs-lookup"><span data-stu-id="2dd9d-143">Then these entries will not affect any of the other depreciation books.</span></span>

## <a name="to-post-additional-acquisition-costs"></a><span data-ttu-id="2dd9d-144">Bókun Viðbótarkaupverðs</span><span class="sxs-lookup"><span data-stu-id="2dd9d-144">To post additional acquisition costs</span></span>
<span data-ttu-id="2dd9d-145">Annar stofnkostnaður eignar er bókaður eins og upphaflegi stofnkostnaðurinn: úr innkaupareikningi eða úr eignabók.</span><span class="sxs-lookup"><span data-stu-id="2dd9d-145">You post additional acquisition cost for a fixed asset in the same way as you post the original acquisition cost: from a purchase invoice or from a fixed asset journal.</span></span> <span data-ttu-id="2dd9d-146">Nánari upplýsingar eru í [Komast yfir eignir](fa-how-acquire.md).</span><span class="sxs-lookup"><span data-stu-id="2dd9d-146">For more information, see [Acquire Fixed Assets](fa-how-acquire.md).</span></span>  

<span data-ttu-id="2dd9d-147">Ef afskriftir hafa þegar verið reiknaðar fyrir eignina er sett gátmerki í reitinn **Afskr. kaupverðs** til að annar stofnkostnaður að frádregnu hrakvirði verði afskrifaður í hlutfalli við upphæðina sem áður keypt eign hefur þegar verið afskrifuð um.</span><span class="sxs-lookup"><span data-stu-id="2dd9d-147">If depreciation has already been calculated for the fixed asset, select the **Depr. Acquisition Cost** check box to have the additional acquisition cost less the salvage value depreciated in proportion to the amount by which the previously acquired fixed asset has already been depreciated.</span></span> <span data-ttu-id="2dd9d-148">Þetta tryggir að afskriftatímabilið breytist ekki.</span><span class="sxs-lookup"><span data-stu-id="2dd9d-148">This ensures that the depreciation period is not changed.</span></span>  

<span data-ttu-id="2dd9d-149">Afskriftaprósentan er reiknuð sem:</span><span class="sxs-lookup"><span data-stu-id="2dd9d-149">The depreciation percentage is calculated as:</span></span>  

<span data-ttu-id="2dd9d-150">*P = (heildarafskriftir x 100) / afskriftagrunnur*</span><span class="sxs-lookup"><span data-stu-id="2dd9d-150">*P = (total depreciation x 100) / depreciable basis*</span></span>

<span data-ttu-id="2dd9d-151">*Afskriftaupphæð = (P/100) x (viðbótarstofnkostnaður - hrakvirði)*</span><span class="sxs-lookup"><span data-stu-id="2dd9d-151">*Depreciation amount = (P/100) x (extra acquisition cost - salvage value)*</span></span>  

<span data-ttu-id="2dd9d-152">Muna þarf að setja gátmerkið í reitinn **Afskr. til eignabókunardags.** í reikningi, eignafjárhagsbókar- eða eignabókarlínurnar til að tryggja að afskrift sé reiknuð frá síðasta eignabókunardegi til bókunardags annars kaupverðs.</span><span class="sxs-lookup"><span data-stu-id="2dd9d-152">Remember to select the **Depr. until FA Posting Date** check box on the invoice, the fixed asset G/L journal, or the fixed asset journal lines to ensure that depreciation is calculated from the last fixed asset posting date to the posting date of the additional acquisition cost.</span></span>

### <a name="example---posting-additional-acquisition-costs"></a><span data-ttu-id="2dd9d-153">Dæmi - bókun viðbótar stofnkostnaðar</span><span class="sxs-lookup"><span data-stu-id="2dd9d-153">Example - Posting Additional Acquisition Costs</span></span>
<span data-ttu-id="2dd9d-154">Vél er keypt 1. ágúst, 2000.</span><span class="sxs-lookup"><span data-stu-id="2dd9d-154">A machine is purchased on August 1, 2000.</span></span> <span data-ttu-id="2dd9d-155">Stofnkostnaðurinn er 4.800.</span><span class="sxs-lookup"><span data-stu-id="2dd9d-155">The acquisition cost is 4,800.</span></span> <span data-ttu-id="2dd9d-156">Afskriftaaðferðin er línuleg til fjögurra ára.</span><span class="sxs-lookup"><span data-stu-id="2dd9d-156">The depreciation method is straight-line over four years.</span></span>

<span data-ttu-id="2dd9d-157">31. ágúst, 2000, er keyrslan **Reikna afskrift** keyrð.</span><span class="sxs-lookup"><span data-stu-id="2dd9d-157">On August 31, 2000, the **Calculate Depreciation** batch job is run.</span></span> <span data-ttu-id="2dd9d-158">Afskriftir eru reiknaðar sem:</span><span class="sxs-lookup"><span data-stu-id="2dd9d-158">Depreciation is calculated as:</span></span>

<span data-ttu-id="2dd9d-159">*bókfært virði x fjöldi afskriftadaga / heildarfjöldi afskriftadaga = 4800 x 30 / 1440 = 100*</span><span class="sxs-lookup"><span data-stu-id="2dd9d-159">*book value x number of depreciation days / total number of depreciation days = 4800 x 30 / 1440 = 100*</span></span>  

<span data-ttu-id="2dd9d-160">september, 2000, er sölureikningur bókaður vegna málningar á vélinni.</span><span class="sxs-lookup"><span data-stu-id="2dd9d-160">On September 15, 2000, an invoice is posted for painting the machine.</span></span> <span data-ttu-id="2dd9d-161">Upphæðin á reikningnum er 480.</span><span class="sxs-lookup"><span data-stu-id="2dd9d-161">The invoice amount is 480.</span></span>

<span data-ttu-id="2dd9d-162">Ef valið var **Afskr. til eignabókunardags.** gátreiturinn á reikningnum fyrir bókun, fara fram eftirfarandi útreikningar:</span><span class="sxs-lookup"><span data-stu-id="2dd9d-162">If you selected the **Depr. until FA Posting Date** check box on the invoice before posting, the following calculation is made:</span></span>  

<span data-ttu-id="2dd9d-163">15 daga afskriftir (frá 01/09/00 til 15/09/00) eru reiknaðar sem:</span><span class="sxs-lookup"><span data-stu-id="2dd9d-163">15 days of depreciation (from 09/01/00 to 09/15/00) is calculated as:</span></span>

<span data-ttu-id="2dd9d-164">*bókfært virði x fjöldi afskriftadaga / eftirstandandi fjöldi afskriftadaga = (4800 - 100) x 15 / 1410 = 50*</span><span class="sxs-lookup"><span data-stu-id="2dd9d-164">*book value x number of depreciation days / remaining number of depreciation days = (4800 - 100) x 15 / 1410 = 50*</span></span>

<span data-ttu-id="2dd9d-165">Ef valið var **Afskr. kaupverðs.** gátreiturinn á reikningnum fyrir bókun, fara fram eftirfarandi útreikningar:</span><span class="sxs-lookup"><span data-stu-id="2dd9d-165">If you selected the **Depr. Acquisition Cost** check box on the invoice before posting, the following calculation is made:</span></span>  

<span data-ttu-id="2dd9d-166">*Annar stofnkostnaður er afskrifaður um ((150 x 100) / 4800) / 100 x 480 = 15*</span><span class="sxs-lookup"><span data-stu-id="2dd9d-166">*The additional acquisition cost is depreciated by ((150 x 100) / 4800) / 100 x 480 = 15*</span></span>

<span data-ttu-id="2dd9d-167">Afskriftagrunnurinn er núna *5280 = (4800 + 480)* og uppsafnaðar afskriftir eru *165 = (100 + 50 +15)* sem samsvarar 45 daga afskriftum á heildarkaupverði.</span><span class="sxs-lookup"><span data-stu-id="2dd9d-167">The depreciable basis is now *5280 = (4800 + 480)*, and the accumulated depreciation is *165 = (100 + 50 + 15)*, corresponding to 45 days of depreciation of the total acquisition cost.</span></span> <span data-ttu-id="2dd9d-168">Það merkir að eignin verði að fullu afskrifuð innan áætlaðs fjögurra ára líftíma.</span><span class="sxs-lookup"><span data-stu-id="2dd9d-168">This means that the asset will be totally depreciated within the estimated lifetime of four years.</span></span>  

<span data-ttu-id="2dd9d-169">Þegar keyrslan **Reikna afskriftir** er keyrð 30/09/00 eru útreikningar með eftirfarandi hætti:</span><span class="sxs-lookup"><span data-stu-id="2dd9d-169">When the **Calculate Depreciation** batch job is run on 09/30/00, the following calculation is made:</span></span>  

<span data-ttu-id="2dd9d-170">*Eftirstöðvar afskriftartíma eru 3 ár, 10 mánuðir og 15 dagar = 1395 dagar*</span><span class="sxs-lookup"><span data-stu-id="2dd9d-170">*Remaining depreciable life is 3 years, 10 months and 15 days = 1395 days*</span></span>  

<span data-ttu-id="2dd9d-171">*Bókfært virði er (5280 -165) = 5115*</span><span class="sxs-lookup"><span data-stu-id="2dd9d-171">*Book value is (5280 - 165) = 5115*</span></span>  

<span data-ttu-id="2dd9d-172">*Afskriftaupphæð fyrir september 2000: 5115 x 15 / 1395 = 55,00*</span><span class="sxs-lookup"><span data-stu-id="2dd9d-172">*Depreciation amount for September 2000: 5115 x 15 / 1395 = 55.00*</span></span>  

<span data-ttu-id="2dd9d-173">*Heildarafskriftir = 165 + 55 = 220*</span><span class="sxs-lookup"><span data-stu-id="2dd9d-173">*Total of depreciation = 165 + 55 = 220*</span></span>  

<span data-ttu-id="2dd9d-174">Ef þú valdir ekki gátreitinn **Afskr. þar til eignabókunardags.** glatar eignin 15 daga afskriftum vegna þess að runuvinnslan **Reikna afskriftir** sem keyrð er á 30/09/00 reiknar afskriftir frá 15/09/00 til 30/09/00.</span><span class="sxs-lookup"><span data-stu-id="2dd9d-174">If you did not select the **Depr. until FA Posting Date** check box, the asset would lose 15 days of depreciation because the **Calculate Depreciation** batch job run on 09/30/00 would calculate depreciation from 09/15/00 to 09/30/00.</span></span> <span data-ttu-id="2dd9d-175">Það merkir að þegar keyrslan **Reikna afskriftir** er keyrð 30/09/00 eru útreikningarnir sem hér segir:</span><span class="sxs-lookup"><span data-stu-id="2dd9d-175">This means that when the **Calculate Depreciation** batch job is run on 09/30/00, the calculation is as follows:</span></span>  

<span data-ttu-id="2dd9d-176">*Eftirstöðvar líftíma eru 3 ár, 10 mánuðir og 15 dagar = 1395 dagar*</span><span class="sxs-lookup"><span data-stu-id="2dd9d-176">*Remaining life time is 3 years, 10 months and 15 days = 1395 days*</span></span>  

<span data-ttu-id="2dd9d-177">*Bókfært virði er (4800 + 480 - 100 - 15) = 5165*</span><span class="sxs-lookup"><span data-stu-id="2dd9d-177">*Book value is (4800 + 480 - 100 - 15) = 5165*</span></span>

<span data-ttu-id="2dd9d-178">*Afskriftaupphæð fyrir september 2000: 5165 x 15 / 1395 = 55,54*</span><span class="sxs-lookup"><span data-stu-id="2dd9d-178">*Depreciation amount for September 2000: 5165 x 15 / 1395 = 55.54*</span></span>  

<span data-ttu-id="2dd9d-179">*Heildarafskriftir = 100 + 15 + 55,54 = 170,54*</span><span class="sxs-lookup"><span data-stu-id="2dd9d-179">*Total of depreciation = 100 + 15 + 55.54 = 170.54*</span></span>

## <a name="see-also"></a><span data-ttu-id="2dd9d-180">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="2dd9d-180">See Also</span></span>
[<span data-ttu-id="2dd9d-181">Eignir</span><span class="sxs-lookup"><span data-stu-id="2dd9d-181">Fixed Assets</span></span>](fa-manage.md)  
[<span data-ttu-id="2dd9d-182">Uppsetning eigna</span><span class="sxs-lookup"><span data-stu-id="2dd9d-182">Setting Up Fixed Assets</span></span>](fa-setup.md)  
[<span data-ttu-id="2dd9d-183">Fjármál</span><span class="sxs-lookup"><span data-stu-id="2dd9d-183">Finance</span></span>](finance.md)  
[<span data-ttu-id="2dd9d-184">Hafist handa</span><span class="sxs-lookup"><span data-stu-id="2dd9d-184">Getting Started</span></span>](product-get-started.md)  
<span data-ttu-id="2dd9d-185">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="2dd9d-185">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

