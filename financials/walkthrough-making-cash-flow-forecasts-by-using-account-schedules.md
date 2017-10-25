---
title: "Kynning: Gera sjóðstreymisspár með því að nota fjárhagsskemu | Microsoft Docs"
description: "Í þessari kynningu er lýst hvernig hægt er að nota reikningsáætlanir til að búa til sjóðstreymisspár. Fjárhagsskemu framkvæma útreikninga sem ekki er hægt að framkvæma beint í myndriti yfir sjóðstreymisreikninga. í fjárhagsskemum er hægt að setja upp millisummur fyrir sjóðstreymismóttökur og heildarútborganir. Þessar undirsamtölur er hægt að hafa með í nýjum samtölum sem hægt er að nota til að gera sjóðstreymisspár."
services: project-madeira
documentationcenter: 
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
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: c66fc5da322ddb1d217b61da0b563faab27b344e
ms.contentlocale: is-is
ms.lasthandoff: 09/22/2017

---
# <a name="walkthrough-making-cash-flow-forecasts-by-using-account-schedules"></a><span data-ttu-id="f1b1b-106">Kynning: Gera sjóðstreymisspár með því að nota fjárhagsskemu</span><span class="sxs-lookup"><span data-stu-id="f1b1b-106">Walkthrough: Making Cash Flow Forecasts by Using Account Schedules</span></span>
<span data-ttu-id="f1b1b-107">Í þessari kynningu er lýst hvernig hægt er að nota reikningsáætlanir til að búa til sjóðstreymisspár.</span><span class="sxs-lookup"><span data-stu-id="f1b1b-107">This walkthrough describes how you can use account schedules to make cash flow forecasts.</span></span> <span data-ttu-id="f1b1b-108">Fjárhagsskemu framkvæma útreikninga sem ekki er hægt að framkvæma beint í myndriti yfir sjóðstreymisreikninga.</span><span class="sxs-lookup"><span data-stu-id="f1b1b-108">Account schedules perform calculations that cannot be done directly in the chart of cash flow accounts.</span></span> <span data-ttu-id="f1b1b-109">í fjárhagsskemum er hægt að setja upp millisummur fyrir sjóðstreymismóttökur og heildarútborganir.</span><span class="sxs-lookup"><span data-stu-id="f1b1b-109">In the account schedules, you can set up subtotals for cash flow receipts and disbursements.</span></span> <span data-ttu-id="f1b1b-110">Þessar undirsamtölur er hægt að hafa með í nýjum samtölum sem hægt er að nota til að gera sjóðstreymisspár.</span><span class="sxs-lookup"><span data-stu-id="f1b1b-110">These subtotals can be included in new totals that can then be used in making cash flow forecasts.</span></span>  

## <a name="about-this-walkthrough"></a><span data-ttu-id="f1b1b-111">Um kynninguna</span><span class="sxs-lookup"><span data-stu-id="f1b1b-111">About This Walkthrough</span></span>  
<span data-ttu-id="f1b1b-112">Þessi kynning fjallar um eftirfarandi verk:</span><span class="sxs-lookup"><span data-stu-id="f1b1b-112">This walkthrough describes the following tasks:</span></span>  

- <span data-ttu-id="f1b1b-113">Setja upp nýtt heiti fyrir fjárhagsskema</span><span class="sxs-lookup"><span data-stu-id="f1b1b-113">Setting up a new cash flow account schedule name.</span></span>  
- <span data-ttu-id="f1b1b-114">Uppsetning fjárhagsskemalína.</span><span class="sxs-lookup"><span data-stu-id="f1b1b-114">Setting up account schedule lines.</span></span>  
- <span data-ttu-id="f1b1b-115">Setja upp nýtt dálkaútlit.</span><span class="sxs-lookup"><span data-stu-id="f1b1b-115">Setting up a new column layout.</span></span>  
- <span data-ttu-id="f1b1b-116">Úthluta dálkauppsetningu til fjárhagsskema.</span><span class="sxs-lookup"><span data-stu-id="f1b1b-116">Assigning a column layout to an account schedule.</span></span>  
- <span data-ttu-id="f1b1b-117">Sjóðstreymisspá skoðuð og prentuð.</span><span class="sxs-lookup"><span data-stu-id="f1b1b-117">Viewing and printing the cash flow forecast.</span></span>  

### <a name="prerequisites"></a><span data-ttu-id="f1b1b-118">Frumskilyrði</span><span class="sxs-lookup"><span data-stu-id="f1b1b-118">Prerequisites</span></span>  
<span data-ttu-id="f1b1b-119">Til að ljúka þessari kynningu þarf:</span><span class="sxs-lookup"><span data-stu-id="f1b1b-119">To complete this walkthrough, you will need:</span></span>  

- [!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="f1b1b-120"> uppsett.</span><span class="sxs-lookup"><span data-stu-id="f1b1b-120"> installed.</span></span>  
- <span data-ttu-id="f1b1b-121">Vinnublaðslínur sjóðstreymis eru skráðar.</span><span class="sxs-lookup"><span data-stu-id="f1b1b-121">The cash flow worksheet lines are registered.</span></span>  

## <a name="roles"></a><span data-ttu-id="f1b1b-122">Hlutverk</span><span class="sxs-lookup"><span data-stu-id="f1b1b-122">Roles</span></span>  
<span data-ttu-id="f1b1b-123">Þessi kynning sýnir þau verk sem framkvæmd eru með eftirfarandi hlutverkum notenda:</span><span class="sxs-lookup"><span data-stu-id="f1b1b-123">This walkthrough demonstrates tasks that are performed by the following user role:</span></span>  

- <span data-ttu-id="f1b1b-124">Eftirlitsmaður</span><span class="sxs-lookup"><span data-stu-id="f1b1b-124">Controller</span></span>  

## <a name="story"></a><span data-ttu-id="f1b1b-125">Ferill</span><span class="sxs-lookup"><span data-stu-id="f1b1b-125">Story</span></span>  
<span data-ttu-id="f1b1b-126">Ken er fjármálastjóri á CRONUS sem gerir mánaðarlega sjóðstreymisspár.</span><span class="sxs-lookup"><span data-stu-id="f1b1b-126">Ken is a controller at CRONUS who makes monthly cash flow forecasts.</span></span> <span data-ttu-id="f1b1b-127">Hann hefur fjármál, sölu, innkaup og eignir með í spánni og sýnir síðan fjármálastjóranum Söru til að fá greiningu hennar.</span><span class="sxs-lookup"><span data-stu-id="f1b1b-127">He includes finance, sales, purchase, and fixed assets in the forecast, and then he presents it to CFO Sara for business insight.</span></span>  

## <a name="setting-up-a-new-account-schedule-name"></a><span data-ttu-id="f1b1b-128">Setja upp Nýtt heiti fyrir fjárhagsskema</span><span class="sxs-lookup"><span data-stu-id="f1b1b-128">Setting Up a New Account Schedule Name</span></span>  
<span data-ttu-id="f1b1b-129">Fjárhagsskema hefur að geyma heiti fjárhagsskema sjóðstreymis með röð af línum og dálkauppsetningu.</span><span class="sxs-lookup"><span data-stu-id="f1b1b-129">An account schedule consists of a cash flow account schedule name with a series of lines and a column layout.</span></span>  

### <a name="to-set-up-a-new-account-schedule-name"></a><span data-ttu-id="f1b1b-130">Setja upp Nýtt heiti fyrir fjárhagsskema</span><span class="sxs-lookup"><span data-stu-id="f1b1b-130">To set up a new account schedule name</span></span>  

1.  <span data-ttu-id="f1b1b-131">Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Fjárhagsskemu** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="f1b1b-131">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Account Schedules**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="f1b1b-132">Í glugganum **Heiti fjárhagsskema** skal velja aðgerðina **Nýtt** til að búa til nýtt sjóðstreymi á fjárhagsskema.</span><span class="sxs-lookup"><span data-stu-id="f1b1b-132">In the **Account Schedule Names** window, choose the **New** to create a new cash flow account schedule name.</span></span>  
3.  <span data-ttu-id="f1b1b-133">Í reitinn **Heiti** skal færa inn **Spá**.</span><span class="sxs-lookup"><span data-stu-id="f1b1b-133">In the **Name** field, enter **Forecast**.</span></span>  
4.  <span data-ttu-id="f1b1b-134">Í reitnum **Lýsing** færið inn **Lýsing fyrir sjóðstremisspá**.</span><span class="sxs-lookup"><span data-stu-id="f1b1b-134">In the **Description** field, enter **Cash Flow Forecast**.</span></span>  
5.  <span data-ttu-id="f1b1b-135">Reitirnir **Sjálfgefin dálkauppsetning** og **Heiti greiningaryfirlits** eru fylltir út eftir því sem við á.</span><span class="sxs-lookup"><span data-stu-id="f1b1b-135">Leave the **Default Column Layout** and **Analysis View Name** fields blank.</span></span>  

## <a name="setting-up-account-schedule-lines"></a><span data-ttu-id="f1b1b-136">Setja upp fjárhagsskemalínur</span><span class="sxs-lookup"><span data-stu-id="f1b1b-136">Setting Up Account Schedule Lines</span></span>  
<span data-ttu-id="f1b1b-137">Eftir að heiti fjárhagsskema er sett upp, skilgreinir Ken hverja línu sem birtist í fjárhagsskema sjóðsstreymis.</span><span class="sxs-lookup"><span data-stu-id="f1b1b-137">After an account schedule name is set up, Ken defines each line that appears in the cash flow account schedule.</span></span> <span data-ttu-id="f1b1b-138">Ken skilgreinir línur sem hægt er að birta í skýrslum auk lína sem aðeins eru til útreikninga.</span><span class="sxs-lookup"><span data-stu-id="f1b1b-138">Ken defines lines that can be shown in reports in addition to lines that are only for calculation purposes.</span></span>  

### <a name="to-set-up-account-schedule-lines"></a><span data-ttu-id="f1b1b-139">Til að setja upp fjárhagsskemalínur</span><span class="sxs-lookup"><span data-stu-id="f1b1b-139">To set up account schedule lines</span></span>  

1.  <span data-ttu-id="f1b1b-140">Í glugganum **Heiti fjárhagsskema** skal velja nýja heiti fjárhagsskemans fyrir **Spá** sem búið var til.</span><span class="sxs-lookup"><span data-stu-id="f1b1b-140">In the **Account Schedule Names** window, select the new **Forecast** account schedule name that you have created.</span></span> <span data-ttu-id="f1b1b-141">Á flipanum **Heim**, í flokknum **Vinna** skal velja **Breyta fjárhagsskema**.</span><span class="sxs-lookup"><span data-stu-id="f1b1b-141">On the **Home** tab, in the **Process** group, choose **Edit Account Schedule**.</span></span>  
2.  <span data-ttu-id="f1b1b-142">Í glugganum **Fjárhagsskema** skal færa hverja línu inn nákvæmlega eins og sýnt er í eftirfarandi töflu.</span><span class="sxs-lookup"><span data-stu-id="f1b1b-142">In the **Account Schedule** window, enter each line exactly as shown in the following table.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="f1b1b-143">Með aðgerðinni **Setja inn CF reikninga** er hægt að merkja sjóðstreymisreikninga á fljótlegan hátt úr línuriti sjóðstreymisreikninga og afrita þá í reikningsáætlunarlínur.</span><span class="sxs-lookup"><span data-stu-id="f1b1b-143">Using the **Insert CF Accounts** function, you can quickly mark the cash flow accounts from the chart of cash flow accounts and copy them to account schedule lines.</span></span>  

    <span data-ttu-id="f1b1b-144">|Númer raðar|Lýsing|Tegund samantektar|Samantekt|Línugerð|Gerð upphæðar|Sýna|</span><span class="sxs-lookup"><span data-stu-id="f1b1b-144">|Row No.|Description|Totaling Type|Totaling|Row Type|Amount Type|Show|</span></span>  
    <span data-ttu-id="f1b1b-145">|-------|-----------|-------------|--------|--------|---  ------|----| |C10|Upphæða|Nettóbreyting|Færslur|Nettóupphæð|Alltaf|</span><span class="sxs-lookup"><span data-stu-id="f1b1b-145">|-------|-----------|-------------|--------|--------|---  ------|----| |C10|Amount|Net Change|Entries|Net Amount|Always|</span></span>  
    <span data-ttu-id="f1b1b-146">|C20|Upphæð til dags|Staða til dags|Færslru|Nettóupphæð|Alltaf|</span><span class="sxs-lookup"><span data-stu-id="f1b1b-146">|C20|Amount until Date|Balance at Date|Entries|Net Amount|Always|</span></span>  
    <span data-ttu-id="f1b1b-147">|C30|Allt fjárhagsár|Allt fjárhagsár |Færslur|Nettóupphæð|Alltaf|</span><span class="sxs-lookup"><span data-stu-id="f1b1b-147">|C30|Entire Fiscal Year|Entire Fiscal Year|Entries|Net Amount|Always|</span></span>  

4.  <span data-ttu-id="f1b1b-148">Velja hnappinn **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="f1b1b-148">Choose the **OK** button.</span></span>  

## <a name="assigning-the-column-layout-to-the-account-schedule-name"></a><span data-ttu-id="f1b1b-149">Dálkaútlitinu úthlutað til reikningsáætlunarheitis.</span><span class="sxs-lookup"><span data-stu-id="f1b1b-149">Assigning the Column Layout to the Account Schedule Name</span></span>  
<span data-ttu-id="f1b1b-150">Ken er nú tilbúinn að úthluta dálkaútlitinu á reikningsáætlunarheitið.</span><span class="sxs-lookup"><span data-stu-id="f1b1b-150">Ken is now ready to assign the column layout to the account schedule name.</span></span>  

### <a name="to-assign-the-column-layout-to-the-account-schedule-name"></a><span data-ttu-id="f1b1b-151">Til að úthluta dálkaútlitinu á reikningsáætlunarheiti</span><span class="sxs-lookup"><span data-stu-id="f1b1b-151">To assign the column layout to the account schedule name</span></span>  

1.  <span data-ttu-id="f1b1b-152">Í glugganum **Heiti fjárhagsskema** skal velja nýja **heiti** fjárhagsskemans fyrir **Spá** sem búið var til.</span><span class="sxs-lookup"><span data-stu-id="f1b1b-152">In the **Account Schedule Names** window, select **Forecast** in the **Name** field.</span></span>  
2.  <span data-ttu-id="f1b1b-153">Í reitnum **Sjálfgefin dálkauppsetning** er valið dálkauppsetninguna **Sjóðstreymi** sem á að tilnefna sem sjálfgefin dálkauppsetning.</span><span class="sxs-lookup"><span data-stu-id="f1b1b-153">In the **Default Column Layout** field, choose the column layout **Cash Flow** to assign as the default column layout.</span></span>  

### <a name="to-view-and-print-the-cash-flow-forecast"></a><span data-ttu-id="f1b1b-154">Til að skoða og prenta sjóðstreymisspána</span><span class="sxs-lookup"><span data-stu-id="f1b1b-154">To view and print the cash flow forecast</span></span>  
1.  <span data-ttu-id="f1b1b-155">Í glugganum **Heiti fjárhagsskema** skal velja **Yfirlit** aðgerðina til að skoða sjóðstreymisspá.</span><span class="sxs-lookup"><span data-stu-id="f1b1b-155">In the **Account Schedule Names** window, choose the **Overview** action to view the cash flow forecast.</span></span>  
2.  <span data-ttu-id="f1b1b-156">Í glugganum **Fjárhagsskemayfirlit** er hægt að velja upphæð og síðan skoða sjóðstreymisspáfærslur sem mynda upphæðina.</span><span class="sxs-lookup"><span data-stu-id="f1b1b-156">In the **Acc. Schedule Overview** window, you can select an amount and then view the cash flow forecast entries that make up the amount.</span></span> <span data-ttu-id="f1b1b-157">Auk þess er hægt að skoða reikniregluna sem er notuð til að reikna upphæðina.</span><span class="sxs-lookup"><span data-stu-id="f1b1b-157">In addition, you can view the formula that is used to calculate the amount.</span></span> <span data-ttu-id="f1b1b-158">Einnig er hægt að afmarka upphæðir eftir dagsetningu og vídd.</span><span class="sxs-lookup"><span data-stu-id="f1b1b-158">You can also filter the amounts by date and dimension.</span></span>  
3.  <span data-ttu-id="f1b1b-159">Veldu hnappinn **Prenta** til þess að prenta sjóðstreymisspá.</span><span class="sxs-lookup"><span data-stu-id="f1b1b-159">Choose the **Print** action to print the cash flow forecast.</span></span>  

## <a name="see-also"></a><span data-ttu-id="f1b1b-160">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="f1b1b-160">See Also</span></span>  
 <span data-ttu-id="f1b1b-161">[Hvernig skal: Vinna með fjárhagsskemu](bi-how-work-account-schedule.md) </span><span class="sxs-lookup"><span data-stu-id="f1b1b-161">[How to: Work with Account Schedules](bi-how-work-account-schedule.md) </span></span>  
 [<span data-ttu-id="f1b1b-162">Kynningar á viðskiptaferli</span><span class="sxs-lookup"><span data-stu-id="f1b1b-162">Business Process Walkthroughs</span></span>](walkthrough-business-process-walkthroughs.md)  
 <span data-ttu-id="f1b1b-163">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="f1b1b-163">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

