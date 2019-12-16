---
title: 'Kynning: Gera sjóðstreymisspár með því að nota fjárhagsskemu | Microsoft Docs'
description: Í þessari kynningu er lýst hvernig hægt er að nota reikningsáætlanir til að búa til sjóðstreymisspár. Fjárhagsskemu framkvæma útreikninga sem ekki er hægt að framkvæma beint í myndriti yfir sjóðstreymisreikninga. í fjárhagsskemum er hægt að setja upp millisummur fyrir sjóðstreymismóttökur og heildarútborganir. Þessar undirsamtölur er hægt að hafa með í nýjum samtölum sem hægt er að nota til að gera sjóðstreymisspár.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 13086d536bb1c2ea3b67c3e11d1327b045a2e744
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/03/2019
ms.locfileid: "2876920"
---
# <a name="walkthrough-making-cash-flow-forecasts-by-using-account-schedules"></a><span data-ttu-id="d42f0-106">Kynning: Gera sjóðstreymisspár með því að nota fjárhagsskemu</span><span class="sxs-lookup"><span data-stu-id="d42f0-106">Walkthrough: Making Cash Flow Forecasts by Using Account Schedules</span></span>
<span data-ttu-id="d42f0-107">Í þessari kynningu er lýst hvernig hægt er að nota reikningsáætlanir til að búa til sjóðstreymisspár.</span><span class="sxs-lookup"><span data-stu-id="d42f0-107">This walkthrough describes how you can use account schedules to make cash flow forecasts.</span></span> <span data-ttu-id="d42f0-108">Fjárhagsskemu framkvæma útreikninga sem ekki er hægt að framkvæma beint í myndriti yfir sjóðstreymisreikninga.</span><span class="sxs-lookup"><span data-stu-id="d42f0-108">Account schedules perform calculations that cannot be done directly in the chart of cash flow accounts.</span></span> <span data-ttu-id="d42f0-109">í fjárhagsskemum er hægt að setja upp millisummur fyrir sjóðstreymismóttökur og heildarútborganir.</span><span class="sxs-lookup"><span data-stu-id="d42f0-109">In the account schedules, you can set up subtotals for cash flow receipts and disbursements.</span></span> <span data-ttu-id="d42f0-110">Þessar undirsamtölur er hægt að hafa með í nýjum samtölum sem hægt er að nota til að gera sjóðstreymisspár.</span><span class="sxs-lookup"><span data-stu-id="d42f0-110">These subtotals can be included in new totals that can then be used in making cash flow forecasts.</span></span>  

## <a name="about-this-walkthrough"></a><span data-ttu-id="d42f0-111">Um kynninguna</span><span class="sxs-lookup"><span data-stu-id="d42f0-111">About This Walkthrough</span></span>  
<span data-ttu-id="d42f0-112">Þessi kynning fjallar um eftirfarandi verk:</span><span class="sxs-lookup"><span data-stu-id="d42f0-112">This walkthrough describes the following tasks:</span></span>  

- <span data-ttu-id="d42f0-113">Setja upp nýtt heiti fyrir fjárhagsskema</span><span class="sxs-lookup"><span data-stu-id="d42f0-113">Setting up a new cash flow account schedule name.</span></span>  
- <span data-ttu-id="d42f0-114">Uppsetning fjárhagsskemalína.</span><span class="sxs-lookup"><span data-stu-id="d42f0-114">Setting up account schedule lines.</span></span>  
- <span data-ttu-id="d42f0-115">Setja upp nýtt dálkaútlit.</span><span class="sxs-lookup"><span data-stu-id="d42f0-115">Setting up a new column layout.</span></span>  
- <span data-ttu-id="d42f0-116">Úthluta dálkauppsetningu til fjárhagsskema.</span><span class="sxs-lookup"><span data-stu-id="d42f0-116">Assigning a column layout to an account schedule.</span></span>  
- <span data-ttu-id="d42f0-117">Sjóðstreymisspá skoðuð og prentuð.</span><span class="sxs-lookup"><span data-stu-id="d42f0-117">Viewing and printing the cash flow forecast.</span></span>  

### <a name="prerequisites"></a><span data-ttu-id="d42f0-118">Frumskilyrði</span><span class="sxs-lookup"><span data-stu-id="d42f0-118">Prerequisites</span></span>  
<span data-ttu-id="d42f0-119">Til að ljúka þessari kynningu þarf:</span><span class="sxs-lookup"><span data-stu-id="d42f0-119">To complete this walkthrough, you will need:</span></span>  

- [!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="d42f0-120">uppsett.</span><span class="sxs-lookup"><span data-stu-id="d42f0-120">installed.</span></span>  
- <span data-ttu-id="d42f0-121">Vinnublaðslínur sjóðstreymis eru skráðar.</span><span class="sxs-lookup"><span data-stu-id="d42f0-121">The cash flow worksheet lines are registered.</span></span>  

## <a name="roles"></a><span data-ttu-id="d42f0-122">Hlutverk</span><span class="sxs-lookup"><span data-stu-id="d42f0-122">Roles</span></span>  
<span data-ttu-id="d42f0-123">Þessi kynning sýnir þau verk sem framkvæmd eru með eftirfarandi hlutverkum notenda:</span><span class="sxs-lookup"><span data-stu-id="d42f0-123">This walkthrough demonstrates tasks that are performed by the following user role:</span></span>  

- <span data-ttu-id="d42f0-124">Eftirlitsmaður</span><span class="sxs-lookup"><span data-stu-id="d42f0-124">Controller</span></span>  

## <a name="story"></a><span data-ttu-id="d42f0-125">Ferill</span><span class="sxs-lookup"><span data-stu-id="d42f0-125">Story</span></span>  
<span data-ttu-id="d42f0-126">Ken er fjármálastjóri á CRONUS sem gerir mánaðarlega sjóðstreymisspár.</span><span class="sxs-lookup"><span data-stu-id="d42f0-126">Ken is a controller at CRONUS who makes monthly cash flow forecasts.</span></span> <span data-ttu-id="d42f0-127">Hann hefur fjármál, sölu, innkaup og eignir með í spánni og sýnir síðan fjármálastjóranum Söru til að fá greiningu hennar.</span><span class="sxs-lookup"><span data-stu-id="d42f0-127">He includes finance, sales, purchase, and fixed assets in the forecast, and then he presents it to CFO Sara for business insight.</span></span>  

## <a name="setting-up-a-new-account-schedule-name"></a><span data-ttu-id="d42f0-128">Setja upp Nýtt heiti fyrir fjárhagsskema</span><span class="sxs-lookup"><span data-stu-id="d42f0-128">Setting Up a New Account Schedule Name</span></span>  
<span data-ttu-id="d42f0-129">Fjárhagsskema hefur að geyma heiti fjárhagsskema sjóðstreymis með röð af línum og dálkauppsetningu.</span><span class="sxs-lookup"><span data-stu-id="d42f0-129">An account schedule consists of a cash flow account schedule name with a series of lines and a column layout.</span></span>  

### <a name="to-set-up-a-new-account-schedule-name"></a><span data-ttu-id="d42f0-130">Setja upp Nýtt heiti fyrir fjárhagsskema</span><span class="sxs-lookup"><span data-stu-id="d42f0-130">To set up a new account schedule name</span></span>  

1.  <span data-ttu-id="d42f0-131">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Fjárhagsskema** eða Lánardrottinn og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="d42f0-131">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Account Schedules**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="d42f0-132">Á síðunni **Heiti fjárhagsskema** skal velja aðgerðina **Nýtt** til að búa til nýtt sjóðstreymi á fjárhagsskema.</span><span class="sxs-lookup"><span data-stu-id="d42f0-132">On the **Account Schedule Names** page, choose the **New** to create a new cash flow account schedule name.</span></span>  
3.  <span data-ttu-id="d42f0-133">Í reitinn **Heiti** skal færa inn **Spá**.</span><span class="sxs-lookup"><span data-stu-id="d42f0-133">In the **Name** field, enter **Forecast**.</span></span>  
4.  <span data-ttu-id="d42f0-134">Í reitnum **Lýsing** færið inn **Lýsing fyrir sjóðstremisspá**.</span><span class="sxs-lookup"><span data-stu-id="d42f0-134">In the **Description** field, enter **Cash Flow Forecast**.</span></span>  
5.  <span data-ttu-id="d42f0-135">Reitirnir **Sjálfgefin dálkauppsetning** og **Heiti greiningaryfirlits** eru fylltir út eftir því sem við á.</span><span class="sxs-lookup"><span data-stu-id="d42f0-135">Leave the **Default Column Layout** and **Analysis View Name** fields blank.</span></span>  

## <a name="setting-up-account-schedule-lines"></a><span data-ttu-id="d42f0-136">Setja upp fjárhagsskemalínur</span><span class="sxs-lookup"><span data-stu-id="d42f0-136">Setting Up Account Schedule Lines</span></span>  
<span data-ttu-id="d42f0-137">Eftir að heiti fjárhagsskema er sett upp, skilgreinir Ken hverja línu sem birtist í fjárhagsskema sjóðsstreymis.</span><span class="sxs-lookup"><span data-stu-id="d42f0-137">After an account schedule name is set up, Ken defines each line that appears in the cash flow account schedule.</span></span> <span data-ttu-id="d42f0-138">Ken skilgreinir línur sem hægt er að birta í skýrslum auk lína sem aðeins eru til útreikninga.</span><span class="sxs-lookup"><span data-stu-id="d42f0-138">Ken defines lines that can be shown in reports in addition to lines that are only for calculation purposes.</span></span>  

### <a name="to-set-up-account-schedule-lines"></a><span data-ttu-id="d42f0-139">Til að setja upp fjárhagsskemalínur</span><span class="sxs-lookup"><span data-stu-id="d42f0-139">To set up account schedule lines</span></span>  

1.  <span data-ttu-id="d42f0-140">Á síðunni **Heiti fjárhagsskema** skal velja nýja heiti fjárhagsskemans fyrir **Spá** sem búið var til og svo velja aðgerðina **Breyta fjárhagsskema**.</span><span class="sxs-lookup"><span data-stu-id="d42f0-140">On the **Account Schedule Names** page, select the new **Forecast** account schedule name that you have created, and then choose the **Edit Account Schedule** action.</span></span>  
2.  <span data-ttu-id="d42f0-141">Á síðunni **Fjárhagsskema** skal færa inn hverja línu nákvæmlega eins og sýnt er í eftirfarandi töflu.</span><span class="sxs-lookup"><span data-stu-id="d42f0-141">On the **Account Schedule** page, enter each line exactly as shown in the following table.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="d42f0-142">Með aðgerðinni **Setja inn CF reikninga** er hægt að merkja sjóðstreymisreikninga á fljótlegan hátt úr línuriti sjóðstreymisreikninga og afrita þá í reikningsáætlunarlínur.</span><span class="sxs-lookup"><span data-stu-id="d42f0-142">Using the **Insert CF Accounts** function, you can quickly mark the cash flow accounts from the chart of cash flow accounts and copy them to account schedule lines.</span></span>  

    |<span data-ttu-id="d42f0-143">Línunúmer</span><span class="sxs-lookup"><span data-stu-id="d42f0-143">Row No.</span></span>|<span data-ttu-id="d42f0-144">Description</span><span class="sxs-lookup"><span data-stu-id="d42f0-144">Description</span></span>|<span data-ttu-id="d42f0-145">Tegund samantektar</span><span class="sxs-lookup"><span data-stu-id="d42f0-145">Totaling Type</span></span>|<span data-ttu-id="d42f0-146">Samantekt</span><span class="sxs-lookup"><span data-stu-id="d42f0-146">Totaling</span></span>|<span data-ttu-id="d42f0-147">Tegund línu</span><span class="sxs-lookup"><span data-stu-id="d42f0-147">Row Type</span></span>|<span data-ttu-id="d42f0-148">Tegund upphæðar</span><span class="sxs-lookup"><span data-stu-id="d42f0-148">Amount Type</span></span>|<span data-ttu-id="d42f0-149">Sýna</span><span class="sxs-lookup"><span data-stu-id="d42f0-149">Show</span></span>|  
    |-------|-----------|-------------|--------|--------|-----------|----|
    |<span data-ttu-id="d42f0-150">C10</span><span class="sxs-lookup"><span data-stu-id="d42f0-150">C10</span></span>|<span data-ttu-id="d42f0-151">Upphæð</span><span class="sxs-lookup"><span data-stu-id="d42f0-151">Amount</span></span>|<span data-ttu-id="d42f0-152">Hreyfing</span><span class="sxs-lookup"><span data-stu-id="d42f0-152">Net Change</span></span>|<span data-ttu-id="d42f0-153">Færslur</span><span class="sxs-lookup"><span data-stu-id="d42f0-153">Entries</span></span>|<span data-ttu-id="d42f0-154">Nettóupphæð</span><span class="sxs-lookup"><span data-stu-id="d42f0-154">Net Amount</span></span>|<span data-ttu-id="d42f0-155">Alltaf</span><span class="sxs-lookup"><span data-stu-id="d42f0-155">Always</span></span>|  
    |<span data-ttu-id="d42f0-156">C20</span><span class="sxs-lookup"><span data-stu-id="d42f0-156">C20</span></span>|<span data-ttu-id="d42f0-157">Upphæð til dags</span><span class="sxs-lookup"><span data-stu-id="d42f0-157">Amount until Date</span></span>|<span data-ttu-id="d42f0-158">Staða til dags.</span><span class="sxs-lookup"><span data-stu-id="d42f0-158">Balance at Date</span></span>|<span data-ttu-id="d42f0-159">Færslur</span><span class="sxs-lookup"><span data-stu-id="d42f0-159">Entries</span></span>|<span data-ttu-id="d42f0-160">Nettóupphæð</span><span class="sxs-lookup"><span data-stu-id="d42f0-160">Net Amount</span></span>|<span data-ttu-id="d42f0-161">Alltaf</span><span class="sxs-lookup"><span data-stu-id="d42f0-161">Always</span></span>|  
    |<span data-ttu-id="d42f0-162">C30</span><span class="sxs-lookup"><span data-stu-id="d42f0-162">C30</span></span>|<span data-ttu-id="d42f0-163">Allt reikningsárið</span><span class="sxs-lookup"><span data-stu-id="d42f0-163">Entire Fiscal Year</span></span>|<span data-ttu-id="d42f0-164">Allt reikningsárið</span><span class="sxs-lookup"><span data-stu-id="d42f0-164">Entire Fiscal Year</span></span>|<span data-ttu-id="d42f0-165">Færslur</span><span class="sxs-lookup"><span data-stu-id="d42f0-165">Entries</span></span>|<span data-ttu-id="d42f0-166">Nettóupphæð</span><span class="sxs-lookup"><span data-stu-id="d42f0-166">Net Amount</span></span>|<span data-ttu-id="d42f0-167">Alltaf</span><span class="sxs-lookup"><span data-stu-id="d42f0-167">Always</span></span>|  

4.  <span data-ttu-id="d42f0-168">Velja hnappinn **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="d42f0-168">Choose the **OK** button.</span></span>  

## <a name="assigning-the-column-layout-to-the-account-schedule-name"></a><span data-ttu-id="d42f0-169">Dálkaútlitinu úthlutað til reikningsáætlunarheitis.</span><span class="sxs-lookup"><span data-stu-id="d42f0-169">Assigning the Column Layout to the Account Schedule Name</span></span>  
<span data-ttu-id="d42f0-170">Ken er nú tilbúinn að úthluta dálkaútlitinu á reikningsáætlunarheitið.</span><span class="sxs-lookup"><span data-stu-id="d42f0-170">Ken is now ready to assign the column layout to the account schedule name.</span></span>  

### <a name="to-assign-the-column-layout-to-the-account-schedule-name"></a><span data-ttu-id="d42f0-171">Til að úthluta dálkaútlitinu á reikningsáætlunarheiti</span><span class="sxs-lookup"><span data-stu-id="d42f0-171">To assign the column layout to the account schedule name</span></span>  

1.  <span data-ttu-id="d42f0-172">Á síðunni **Heiti fjárhagsskema** skal velja **Spá** í reitnum **heiti**.</span><span class="sxs-lookup"><span data-stu-id="d42f0-172">On the **Account Schedule Names** page, select **Forecast** in the **Name** field.</span></span>  
2.  <span data-ttu-id="d42f0-173">Í reitnum **Sjálfgefin dálkauppsetning** er valið dálkauppsetninguna **Sjóðstreymi** sem á að tilnefna sem sjálfgefin dálkauppsetning.</span><span class="sxs-lookup"><span data-stu-id="d42f0-173">In the **Default Column Layout** field, choose the column layout **Cash Flow** to assign as the default column layout.</span></span>  

### <a name="to-view-and-print-the-cash-flow-forecast"></a><span data-ttu-id="d42f0-174">Til að skoða og prenta sjóðstreymisspána</span><span class="sxs-lookup"><span data-stu-id="d42f0-174">To view and print the cash flow forecast</span></span>  
1.  <span data-ttu-id="d42f0-175">Á síðunni **Heiti fjárhagsskema** skal velja **Yfirlit** aðgerðina til að skoða sjóðstreymisspá.</span><span class="sxs-lookup"><span data-stu-id="d42f0-175">On the **Account Schedule Names** page, choose the **Overview** action to view the cash flow forecast.</span></span>  
2.  <span data-ttu-id="d42f0-176">Á síðunni **Yfirlit fjárhagsskema** er hægt að velja upphæð og síðan skoða sjóðstreymisspáfærslur sem mynda upphæðina.</span><span class="sxs-lookup"><span data-stu-id="d42f0-176">On the **Acc. Schedule Overview** page, you can select an amount and then view the cash flow forecast entries that make up the amount.</span></span> <span data-ttu-id="d42f0-177">Auk þess er hægt að skoða reikniregluna sem er notuð til að reikna upphæðina.</span><span class="sxs-lookup"><span data-stu-id="d42f0-177">In addition, you can view the formula that is used to calculate the amount.</span></span> <span data-ttu-id="d42f0-178">Einnig er hægt að afmarka upphæðir eftir dagsetningu og vídd.</span><span class="sxs-lookup"><span data-stu-id="d42f0-178">You can also filter the amounts by date and dimension.</span></span>  
3.  <span data-ttu-id="d42f0-179">Veldu hnappinn **Prenta** til þess að prenta sjóðstreymisspá.</span><span class="sxs-lookup"><span data-stu-id="d42f0-179">Choose the **Print** action to print the cash flow forecast.</span></span>  

## <a name="see-also"></a><span data-ttu-id="d42f0-180">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="d42f0-180">See Also</span></span>  
 <span data-ttu-id="d42f0-181">[Vinna með fjárhagsskemu](bi-how-work-account-schedule.md) </span><span class="sxs-lookup"><span data-stu-id="d42f0-181">[Work with Account Schedules](bi-how-work-account-schedule.md) </span></span>  
 [<span data-ttu-id="d42f0-182">Kynningar á viðskiptaferli</span><span class="sxs-lookup"><span data-stu-id="d42f0-182">Business Process Walkthroughs</span></span>](walkthrough-business-process-walkthroughs.md)  
 <span data-ttu-id="d42f0-183">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="d42f0-183">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
