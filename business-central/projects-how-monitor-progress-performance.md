---
title: Skilgreina VÍV aðferð og fylgjast með framvindu verks| Microsoft Docs
description: Lýsir því hvernig þú getur búið til verk í vinnslu (VÍV) aðferð og reiknað VÍV til að meta fjárhagslegt gildi verka meðan á þeim stendur.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project management, KPI, work in process, work in progress
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: fac1c041108cacfcabf18b04d128949d05e1d283
ms.sourcegitcommit: 93c8681054b059cec38cb29b86de20be37980676
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938122"
---
# <a name="monitor-job-progress-and-performance"></a><span data-ttu-id="cf055-103">Fylgst með framvindu og afköstum</span><span class="sxs-lookup"><span data-stu-id="cf055-103">Monitor Job Progress and Performance</span></span>
<span data-ttu-id="cf055-104">Þegar verk er unnið er efni, forði og annar kostnaður notuð og þetta þarf að bóka á verkið.</span><span class="sxs-lookup"><span data-stu-id="cf055-104">As a job progresses, materials, resources, and other expenses are consumed and must be posted to the job.</span></span> <span data-ttu-id="cf055-105">Verk í vinnslu (VÍV) er eiginleiki þar sem hægt er að meta fjárhagslegt virði verka í fjárhag eftir því sem verkinu miðar áfram.</span><span class="sxs-lookup"><span data-stu-id="cf055-105">Work in Process (WIP) is a feature that enables you to estimate the financial value of jobs in the general ledger while the jobs are ongoing.</span></span> <span data-ttu-id="cf055-106">Oft er kostnaður bókaður áður en verk er reikningsfært.</span><span class="sxs-lookup"><span data-stu-id="cf055-106">In many cases, you might post expenses for a job before invoicing a job.</span></span> <span data-ttu-id="cf055-107">Þegar aðeins kostnaður hefur verið bókaður verður fjárhagsyfirlitið ónákvæmt.</span><span class="sxs-lookup"><span data-stu-id="cf055-107">When only expenses have been posted, your financial statement will be inaccurate.</span></span> <span data-ttu-id="cf055-108">Frekari upplýsingar eru í [Að skilja VÍV-aðferðir](projects-understanding-wip.md)</span><span class="sxs-lookup"><span data-stu-id="cf055-108">For more information, see [Understanding WIP Methods](projects-understanding-wip.md).</span></span>

<span data-ttu-id="cf055-109">Til að rekja gildi í fjárhagnum er hægt að reikna út VÍV og bóka gildið í fjárhag.</span><span class="sxs-lookup"><span data-stu-id="cf055-109">To track the value in the general ledger, you can calculate WIP and post the value to the general ledger.</span></span>

<span data-ttu-id="cf055-110">VÍV má reikna út byggt á eftirfarandi:</span><span class="sxs-lookup"><span data-stu-id="cf055-110">You can calculate WIP based on the following:</span></span>

* <span data-ttu-id="cf055-111">Kostnaðargildi</span><span class="sxs-lookup"><span data-stu-id="cf055-111">Cost Value</span></span>
* <span data-ttu-id="cf055-112">Sölugildi</span><span class="sxs-lookup"><span data-stu-id="cf055-112">Sales Value</span></span>
* <span data-ttu-id="cf055-113">Auðkennanlegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="cf055-113">Recognizable Cost</span></span>
* <span data-ttu-id="cf055-114">Prósentum lokið</span><span class="sxs-lookup"><span data-stu-id="cf055-114">Percentage of Completion</span></span>
* <span data-ttu-id="cf055-115">Samningi lokið</span><span class="sxs-lookup"><span data-stu-id="cf055-115">Completed Contract</span></span>

<span data-ttu-id="cf055-116">Til að skoða niðurstöður með annarri aðferð er hægt að breyta aðferðinni og reikna Verk í vinnslu á nýjan leik.</span><span class="sxs-lookup"><span data-stu-id="cf055-116">If you want to view the result using a different method, you can change the method and calculate WIP again.</span></span> <span data-ttu-id="cf055-117">Engin takmörk eru á því hversu oft VÍV er reiknað.</span><span class="sxs-lookup"><span data-stu-id="cf055-117">There is no limit to the number of times that you calculate WIP.</span></span> <span data-ttu-id="cf055-118">VÍV er aðeins reiknað en er ekki bókað í fjárhag.</span><span class="sxs-lookup"><span data-stu-id="cf055-118">WIP is only calculated, it does not get posted to the general ledger.</span></span> <span data-ttu-id="cf055-119">Þegar VÍV hefur verið reiknað út er hægt að bóka það í fjárhag.</span><span class="sxs-lookup"><span data-stu-id="cf055-119">After you have calculated WIP, you can post to the general ledger.</span></span>

## <a name="to-create-a-job-wip-method"></a><span data-ttu-id="cf055-120">Til að búa til VÍV-aðferð fyrir verk</span><span class="sxs-lookup"><span data-stu-id="cf055-120">To create a job WIP method</span></span>
<span data-ttu-id="cf055-121">Hægt er að búa til VÍV-aðferð sem endurspeglar þarfir fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="cf055-121">You can create a job WIP method that reflects the needs of your organization.</span></span> <span data-ttu-id="cf055-122">Þegar búið er að stofna það, er hægt að velja það sem sjálfgefna VÍV-reikningsaðferð fyrir verk sem verða notuð í fyrirtækinu.</span><span class="sxs-lookup"><span data-stu-id="cf055-122">After you have created it, you can set it as the default job WIP calculation method that will be used in your organization.</span></span>  

> [!NOTE]
> <span data-ttu-id="cf055-123">Þegar búið er að nota nýju aðferðina til að stofna VÍV-færslur, er ekki hægt að eyða aðferðinni eða breyta henni.</span><span class="sxs-lookup"><span data-stu-id="cf055-123">After you have used your new method to create WIP entries, you cannot delete the method or modify it.</span></span>  

1. <span data-ttu-id="cf055-124">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **VÍV-aðferðir verks** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="cf055-124">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Job WIP Methods**, and then choose the related link.</span></span>  
2. <span data-ttu-id="cf055-125">Veljið aðgerðina **Nýtt** og fyllið svo út reitina eins og þörf krefur.</span><span class="sxs-lookup"><span data-stu-id="cf055-125">Choose the **New** action, and then fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. <span data-ttu-id="cf055-126">Lokaðu síðunni.</span><span class="sxs-lookup"><span data-stu-id="cf055-126">Close the page.</span></span>   
4. <span data-ttu-id="cf055-127">Til að gera þetta að sjálfgefinni aðferð velurðu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Uppsetning verka** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="cf055-127">To make this new method the default, choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Jobs Setup**, and then choose the related link.</span></span>  
5. <span data-ttu-id="cf055-128">Í reitnum **Sjálfgefin vÍv-aðferð** veljið aðferðina af listanum.</span><span class="sxs-lookup"><span data-stu-id="cf055-128">In the **Default WIP Method** field, choose the method from the list.</span></span>

## <a name="to-define-a-wip-method-for-a-job"></a><span data-ttu-id="cf055-129">Til að skilgreina VÍV aðferð fyrir verk</span><span class="sxs-lookup"><span data-stu-id="cf055-129">To define a WIP method for a job</span></span>
<span data-ttu-id="cf055-130">Þegar nýtt verk er stofnað þarf að tilgreina hvaða VÍV-aðferð skuli eiga við.</span><span class="sxs-lookup"><span data-stu-id="cf055-130">When you create a new job, you must specify which job WIP method that applies.</span></span> <span data-ttu-id="cf055-131">Í sumum tilfellum er þegar búið að stilla sjálfgefna VÍV-aðferð verka.</span><span class="sxs-lookup"><span data-stu-id="cf055-131">In some cases, which Job WIP method that you can use has been set up for you as a default.</span></span>

1. <span data-ttu-id="cf055-132">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Verk** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="cf055-132">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Jobs**, and then choose the related link.</span></span>
2. <span data-ttu-id="cf055-133">Valið er aðgerðin **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="cf055-133">Choose the **New** action.</span></span> <span data-ttu-id="cf055-134">Frekari upplýsingar eru í [Stofna verk](projects-how-create-jobs.md).</span><span class="sxs-lookup"><span data-stu-id="cf055-134">For more information, see [Create Jobs](projects-how-create-jobs.md).</span></span>  
3. <span data-ttu-id="cf055-135">Á síðunni **Verkspjald** skal velja VÍV-aðferð úr listanum í reitnum **VÍV-aðferð**.</span><span class="sxs-lookup"><span data-stu-id="cf055-135">On the **Job Card** page, in the **WIP Method** field, select a WIP method from the list.</span></span> <span data-ttu-id="cf055-136">Ef sjálfgefin aðferð hefur verið skilgreind er hægt að velja annan valkost ef þess gerist þörf.</span><span class="sxs-lookup"><span data-stu-id="cf055-136">If a default method has been defined, you can select another option if needed.</span></span>  

## <a name="to-calculate-wip"></a><span data-ttu-id="cf055-137">Útreikningur VÍV</span><span class="sxs-lookup"><span data-stu-id="cf055-137">To calculate WIP</span></span>
<span data-ttu-id="cf055-138">Hægt er að ákvarða VÍV-upphæð sem bóka skal á efnahagsreikning fyrir árslokaskýrslu.</span><span class="sxs-lookup"><span data-stu-id="cf055-138">You can determine the WIP amount that is to be posted to balance sheet accounts for the period end reporting.</span></span> <span data-ttu-id="cf055-139">Þetta má gera með því að nota keyrsluna **Verkreikna VÍV**.</span><span class="sxs-lookup"><span data-stu-id="cf055-139">You use the **Job Calculate WIP** batch job to do this.</span></span>  

1. <span data-ttu-id="cf055-140">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Verkreikna VÍV** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="cf055-140">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Job Calculate WIP**, and then choose the related link.</span></span>  
2. <span data-ttu-id="cf055-141">Veljið aðgerðina **Reikna VÍV**.</span><span class="sxs-lookup"><span data-stu-id="cf055-141">Choose the **Calculate WIP** action.</span></span>
3. <span data-ttu-id="cf055-142">Á síðunni **Verk - Reikna VÍV** þarf að fylla reitina út eins og þörf krefur.</span><span class="sxs-lookup"><span data-stu-id="cf055-142">On the **Job Calculate WIP** page, fill in the fields as necessary.</span></span>
4. <span data-ttu-id="cf055-143">Velja hnappinn **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="cf055-143">Choose the **OK** button.</span></span>  

> [!NOTE]  
>   <span data-ttu-id="cf055-144">Keyrslan reiknar einungis út VÍV.</span><span class="sxs-lookup"><span data-stu-id="cf055-144">The batch job only calculates the WIP.</span></span> <span data-ttu-id="cf055-145">Er ekki bókað í fjárhag.</span><span class="sxs-lookup"><span data-stu-id="cf055-145">It is not posted to the general ledger.</span></span> <span data-ttu-id="cf055-146">Til að gera það verður að keyra keyrsluna **Bóka VÍV á fjárhag** þegar VÍV hefur verið reiknað.</span><span class="sxs-lookup"><span data-stu-id="cf055-146">To do so, you must run the **Post WIP to G/L** batch job when you have calculated the WIP.</span></span> <span data-ttu-id="cf055-147">Nánari upplýsingar má finna hér á eftir.</span><span class="sxs-lookup"><span data-stu-id="cf055-147">For more information, see the following procedure.</span></span>

## <a name="to-post-wip"></a><span data-ttu-id="cf055-148">Til að bóka VÍV</span><span class="sxs-lookup"><span data-stu-id="cf055-148">To post WIP</span></span>
<span data-ttu-id="cf055-149">Þegar VÍV hefur verið reiknað er hægt að bóka það á efnahagsreikning fyrir árslokaskýrslu.</span><span class="sxs-lookup"><span data-stu-id="cf055-149">When you have calculated WIP, you can post it to balance sheet accounts for the period end reporting.</span></span> <span data-ttu-id="cf055-150">Þetta má gera með því að nota keyrsluna **Bóka VÍV á fjárhag**.</span><span class="sxs-lookup"><span data-stu-id="cf055-150">You use the **Job Post WIP to G/L** batch job to do this.</span></span>

1. <span data-ttu-id="cf055-151">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Bóka VÍV í fjárhag** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="cf055-151">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Job Post WIP to G/L**, and then choose the related link.</span></span>  
2. <span data-ttu-id="cf055-152">Á síðunni **Verk - Bóka VÍV í fjárhag** skal fylla reitina út eins og þörf krefur.</span><span class="sxs-lookup"><span data-stu-id="cf055-152">On the **Job Post WIP to G/L** page, fill in the fields as necessary.</span></span>  
3. <span data-ttu-id="cf055-153">Velja hnappinn **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="cf055-153">Choose the **OK** button.</span></span>

## <a name="to-calculate-and-post-job-completion-entries"></a><span data-ttu-id="cf055-154">Að reikna út og bóka verklokafærslur</span><span class="sxs-lookup"><span data-stu-id="cf055-154">To calculate and post job completion entries</span></span>
<span data-ttu-id="cf055-155">Þegar öllum aðgerðum verks hefur verið lokið, þar með talin bókun notkunar og reikningsfærsla, þarf að uppfæra verkið svo að **Staða** þess sé **Lokið**.</span><span class="sxs-lookup"><span data-stu-id="cf055-155">When you have completed all activities for a job, including usage posting and invoicing, you must update the job to have a **Status** of **Completed**.</span></span> <span data-ttu-id="cf055-156">Síðan þarf að bakfæra VÍV sem hefur verið bókað í fjárhag.</span><span class="sxs-lookup"><span data-stu-id="cf055-156">Then, you must reverse any WIP that has been posted to the general ledger.</span></span>

1. <span data-ttu-id="cf055-157">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Verk** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="cf055-157">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Jobs**, and then choose the related link.</span></span>  
2. <span data-ttu-id="cf055-158">Veljið opið verk og veljið svo aðgerðina **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="cf055-158">Select an open job, and then choose the **Edit** action.</span></span>
3. <span data-ttu-id="cf055-159">Í reitnum **Staða** skal velja **Lokið**.</span><span class="sxs-lookup"><span data-stu-id="cf055-159">In the **Status** field, select **Completed**.</span></span>
4. <span data-ttu-id="cf055-160">Fylgið aðstoðarskrefunum til að reikna og bóka VÍV.</span><span class="sxs-lookup"><span data-stu-id="cf055-160">Follow the assistance steps to calculate and post WIP.</span></span> <span data-ttu-id="cf055-161">Einnig er hægt að fylgja skrefum 5 og 6 til að gera það handvirkt.</span><span class="sxs-lookup"><span data-stu-id="cf055-161">Alternatively, follows steps 5 and 6 to do so manually.</span></span>  
5. <span data-ttu-id="cf055-162">Veljið aðgerðina **Reikna VÍV**.</span><span class="sxs-lookup"><span data-stu-id="cf055-162">Choose the **Calculate WIP** action.</span></span>
6. <span data-ttu-id="cf055-163">Á síðunni **Verk - Reikna VÍV** þarf að fylla reitina út eins og þörf krefur.</span><span class="sxs-lookup"><span data-stu-id="cf055-163">On the **Job Calculate WIP** page, fill in the fields as necessary.</span></span>  

     <span data-ttu-id="cf055-164">VÍV færslurnar sem voru stofnaðar með keyrslunni munu nú hafa gátmerki í reitnum **Verki lokið** til að sýna að þær séu lokafærslur.</span><span class="sxs-lookup"><span data-stu-id="cf055-164">The job WIP entries created by running the batch job will have the **Job Complete** check box selected to show that they are completion entries.</span></span>  
7. <span data-ttu-id="cf055-165">Velja skal aðgerðina **Verk - Bóka VÍV í fjárhag**.</span><span class="sxs-lookup"><span data-stu-id="cf055-165">Choose the **Job Post WIP to G/L** action.</span></span>
8. <span data-ttu-id="cf055-166">Á síðunni **Verk - Bóka VÍV í fjárhag** skal fylla reitina út eins og þörf krefur.</span><span class="sxs-lookup"><span data-stu-id="cf055-166">On the **Job Post WIP to G/L** page, fill in the fields as necessary.</span></span>  

     <span data-ttu-id="cf055-167">VÍV-fjárlagsfærslur verks sem voru stofnaðar með keyrslunni munu nú hafa gátmerki í reitnum **Verki lokið** til að sýna að þær eru lokafærslur.</span><span class="sxs-lookup"><span data-stu-id="cf055-167">The job WIP general ledger entries created by running the batch job will have the **Job Complete** check box selected to show they are completion entries.</span></span>

## <a name="to-view-job-ledger-entries"></a><span data-ttu-id="cf055-168">Verkdagbókarfærslur skoðaðar:</span><span class="sxs-lookup"><span data-stu-id="cf055-168">To view job ledger entries</span></span>
<span data-ttu-id="cf055-169">Allar færslur sem tengjast verki eru skráðar í verkdagbækur og tölusettar í réttri röð, byrjað á 1.</span><span class="sxs-lookup"><span data-stu-id="cf055-169">All job-related entries are recorded in job registers and are numbered sequentially, starting with 1.</span></span> <span data-ttu-id="cf055-170">Í verkdagbókinni er hægt að fá yfirlit um verkfærslurnar.</span><span class="sxs-lookup"><span data-stu-id="cf055-170">From the job register, you can get an overview of all job ledger entries.</span></span>    

1. <span data-ttu-id="cf055-171">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Verkdagbækur** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="cf055-171">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Job Registers**, and then choose the related link.</span></span>
2. <span data-ttu-id="cf055-172">Valin er viðeigandi dagbók og síðan skal velja aðgerðina **Verklínur**.</span><span class="sxs-lookup"><span data-stu-id="cf055-172">Select a relevant register, and then choose **Job Ledger** action.</span></span>

<span data-ttu-id="cf055-173">Á síðunni **Verkfærslur** er hægt að fara yfir færslur sem tengjast verki.</span><span class="sxs-lookup"><span data-stu-id="cf055-173">On the **Job Ledger Entries** page you can review the entries that are associated with any job.</span></span>  

## <a name="see-also"></a><span data-ttu-id="cf055-174">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="cf055-174">See Also</span></span>
<span data-ttu-id="cf055-175">[Verkefnum stjórnað](projects-manage-projects.md)
[Birgðakostnaði stjórnað](finance-manage-inventory-costs.md) </span><span class="sxs-lookup"><span data-stu-id="cf055-175">[Managing Projects](projects-manage-projects.md)
[Managing Inventory Costs](finance-manage-inventory-costs.md) </span></span>  
[<span data-ttu-id="cf055-176">Fjármál</span><span class="sxs-lookup"><span data-stu-id="cf055-176">Finance</span></span>](finance.md)  
<span data-ttu-id="cf055-177">[Innkaup](purchasing-manage-purchasing.md)       </span><span class="sxs-lookup"><span data-stu-id="cf055-177">[Purchasing](purchasing-manage-purchasing.md)       </span></span>  
<span data-ttu-id="cf055-178">[Sala](sales-manage-sales.md)    </span><span class="sxs-lookup"><span data-stu-id="cf055-178">[Sales](sales-manage-sales.md)    </span></span>  
<span data-ttu-id="cf055-179">[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="cf055-179">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  


[!INCLUDE[footer-include](includes/footer-banner.md)]
