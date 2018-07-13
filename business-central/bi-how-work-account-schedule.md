---
title: "Búa til fjárhagsskýrslur með fjárhagsskemum"
description: "Lýsir því hvernig skal nota fjárhagsskemu til að búa til ýmis konar yfirlit og skýrslur fyrir greiningar á afkastagögnum fjárhags."
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bi, power BI, analysis, KPI
ms.date: 05/31/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: e73c2dd0533aade4aa6225c9d2f385baaea3cfd1
ms.openlocfilehash: 69034b0eb97b595d0fbf5795e1fac34ecd775afe
ms.contentlocale: is-is
ms.lasthandoff: 06/11/2018

---
# <a name="prepare-financial-reporting-with-account-schedules-and-account-categories"></a><span data-ttu-id="22596-103">Undirbúa fjárhagsskýrslugerð með fjárhagsskemu og lyklategundum</span><span class="sxs-lookup"><span data-stu-id="22596-103">Prepare Financial Reporting with Account Schedules and Account Categories</span></span>
<span data-ttu-id="22596-104">Notaðu reikningsáætlanir til að fá innsýn í fjárhagsupplýsingar sem eru geymdar í bókhaldslyklum.</span><span class="sxs-lookup"><span data-stu-id="22596-104">Use account schedules to get insight into the financial data stored in your chart of accounts.</span></span> <span data-ttu-id="22596-105">Fjárhagsskemu eru notuð til að greina upphæðir í fjárhagsreikningi og bera saman fjárhagsfærslur og færslur í fjárhagsáætlunarskýrslu.</span><span class="sxs-lookup"><span data-stu-id="22596-105">Account schedules analyze figures in G/L accounts, and compare general ledger entries with general ledger budget entries.</span></span> <span data-ttu-id="22596-106">Niðurstöðurnar birtast í myndritum í Mínu hlutverki, eins og myndrit sjóðstreymis, og í skýrslum á borð við tekjuyfirlit og skýrslum efnahagsreiknings.</span><span class="sxs-lookup"><span data-stu-id="22596-106">The results display in charts on your Role Center, such as the Cash Flow chart, and in reports, such as the Income Statement and the Balance Sheet reports.</span></span>

<span data-ttu-id="22596-107">Þú opnar þessar tvær skýrslur til dæmis með aðgerðinni **Fjárhagsyfirlit** í Mínu hlutverki viðskiptastjórnanda og endurskoðanda.</span><span class="sxs-lookup"><span data-stu-id="22596-107">You access these two reports, for example, with the **Financials Statements** action on the Business Manager and Accountant Role Centers.</span></span>   

[!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="22596-108"> veitir nokkrar sýnishornareikninga sem hægt er að nota strax eða þú getur sett upp eigin línur og dálka til að tilgreina tölurnar sem þú vilt bera saman.</span><span class="sxs-lookup"><span data-stu-id="22596-108"> provides a few sample account schedules that you can use right away, or you can set up your own rows and columns to specify the figures to compare.</span></span> <span data-ttu-id="22596-109">Notendur getur þú búið til fjárhagskema til að reikna út framlegð fyrir víddir eins og deildir eða hópa viðskiptamanna.</span><span class="sxs-lookup"><span data-stu-id="22596-109">For example, you can create account schedules to calculate profit margins on dimensions like departments or customer groups.</span></span> <span data-ttu-id="22596-110">Hægt er að búa til eins margar sérsniðnar fjárhagsskýrslur og óskað er.</span><span class="sxs-lookup"><span data-stu-id="22596-110">You can create as many customized financial statements as you want.</span></span>  

<span data-ttu-id="22596-111">Uppsetning fjárhagsskema krefst skilnings á fjárhagsgögnum í bókhaldslyklinum.</span><span class="sxs-lookup"><span data-stu-id="22596-111">Setting up account schedules requires an understanding of the financial data in the chart of accounts.</span></span> <span data-ttu-id="22596-112">Hægt er til dæmis að skoða fjárhagsfærslur sem prósentuhlutfall af áætlunarfærslum.</span><span class="sxs-lookup"><span data-stu-id="22596-112">For example, you can view general ledger entries as percentages of budget entries.</span></span> <span data-ttu-id="22596-113">Þetta krefst þess að fjárhagsáætlanir séu búnar til.</span><span class="sxs-lookup"><span data-stu-id="22596-113">This requires that budgets are created.</span></span> <span data-ttu-id="22596-114">Frekari upplýsingar eru í [Stofna fjárhagsáætlun](finance-how-create-budgets.md).</span><span class="sxs-lookup"><span data-stu-id="22596-114">For more information, see [Create G/L Budgets](finance-how-create-budgets.md).</span></span>

## <a name="account-categories-and-account-schedules"></a><span data-ttu-id="22596-115">Lykiltegundir og fjárhagsskemu</span><span class="sxs-lookup"><span data-stu-id="22596-115">Account Categories and Account Schedules</span></span>
<span data-ttu-id="22596-116">Hægt er að nota lykiltegundir til að breyta sniði fjárhagsskýrslna.</span><span class="sxs-lookup"><span data-stu-id="22596-116">You can use account categories to change the layout of your financial statements.</span></span> <span data-ttu-id="22596-117">Þegar lykiltegundir hafa verið settar upp í glugganum **Flokkar fjárhagsreikninga** og aðgerðin **Mynda fjárhagsskemu** er valin, eru undirliggjandi fjárhagsskemu fyrir kjarnaviðskiptaskýrslur uppfærð.</span><span class="sxs-lookup"><span data-stu-id="22596-117">After you set up your account categories in the **G/L Account Categories** window, and you choose the **Generate Account Schedules** action, the underlying account schedules for the core financial reports are updated.</span></span> <span data-ttu-id="22596-118">Í næsta skipti sem ein af þessum skýrslum er keyrð, t.d. skýrsla stöðuyfirlits, er nýjum samtölum og undirfærslum bætt við sem byggjast á breytingunum.</span><span class="sxs-lookup"><span data-stu-id="22596-118">The next time you run one of these reports, such as the Balance Statement report, new totals and subentries are added, based on your changes.</span></span> <span data-ttu-id="22596-119">Frekari upplýsingar er að finna í kaflanum „Lykilltegundir“ í [Skilja fjárhag og bókhaldslykil](finance-general-ledger.md).</span><span class="sxs-lookup"><span data-stu-id="22596-119">For more information, see The "Account Categories" section in [Understanding the General Ledger and the COA](finance-general-ledger.md).</span></span>  

## <a name="to-create-new-account-schedules"></a><span data-ttu-id="22596-120">Nýtt fjárhagsskema búið til:</span><span class="sxs-lookup"><span data-stu-id="22596-120">To create new account schedules</span></span>  
 <span data-ttu-id="22596-121">Fjárhagsskemu eru notuð til að greina upphæðir í fjárhagsreikningi eða bera saman fjárhagsfærslur og fjárhagsáætlunarfærslur.</span><span class="sxs-lookup"><span data-stu-id="22596-121">You use account schedules to analyze figures in general ledger accounts or to compare general ledger entries with general ledger budget entries.</span></span> <span data-ttu-id="22596-122">Hægt er til dæmis að skoða fjárhagsfærslur sem prósentuhlutfall af áætlunarfærslum.</span><span class="sxs-lookup"><span data-stu-id="22596-122">For example, you can view the general ledger entries as percentages of the budget entries.</span></span>

1. <span data-ttu-id="22596-123">Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Fjárhagsskemu** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="22596-123">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Account Schedules**, and then choose the related link.</span></span>  
2. <span data-ttu-id="22596-124">Í glugganum **Heiti fjárhagsskema** skal velja aðgerðina **Nýtt** til að búa til nýtt heiti á fjárhagsskema.</span><span class="sxs-lookup"><span data-stu-id="22596-124">In the **Account Schedule Names** window, choose the **New** action to create a new account schedule name.</span></span>
3. <span data-ttu-id="22596-125">Fyllið inn í reitina eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="22596-125">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. <span data-ttu-id="22596-126">Veljið aðgerðina **Breyta fjárhagsskema**.</span><span class="sxs-lookup"><span data-stu-id="22596-126">Choose the **Edit Account Schedule** action.</span></span>
5. <span data-ttu-id="22596-127">Í glugganum **Fjárhagsskema** skal fylla reitina út eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="22596-127">In the **Account Schedule** window, fill in the fields as necessary.</span></span>  

    <span data-ttu-id="22596-128">Þegar nýtt fjárhagsskema hefur verið stofnað og línurnar hafa verið settar upp, þarf að setja upp dálka.</span><span class="sxs-lookup"><span data-stu-id="22596-128">When you have created a new account schedule and set up the rows, you must set up columns.</span></span> <span data-ttu-id="22596-129">Annaðhvort er hægt að setja þær upp handvirkt eða úthluta forskilgreindri dálkauppsetningu á viðkomandi fjárhagsskema.</span><span class="sxs-lookup"><span data-stu-id="22596-129">You can either set them up manually or assign a predefined column layout to your account schedule.</span></span>
6. <span data-ttu-id="22596-130">Veljið aðgerðina **Breyta uppsetningu dálkaútlits**.</span><span class="sxs-lookup"><span data-stu-id="22596-130">Choose the **Edit Column Layout Setup** action.</span></span>
7. <span data-ttu-id="22596-131">Í glugganum **Dálkaútlit** skal fylla reitina út eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="22596-131">In the **Column Layout** window, fill in the fields as necessary.</span></span>

> [!NOTE]  
> <span data-ttu-id="22596-132">Ef ekki var tilgreint sjálfgefið dálkaútlit fyrir fjárhagsskemað verður að setja dálkana upp handvirkt.</span><span class="sxs-lookup"><span data-stu-id="22596-132">If you did not assign a default column layout to the account schedule, you must set the columns up manually.</span></span>

### <a name="to-copy-an-existing-account-schedule"></a><span data-ttu-id="22596-133">Til að afrita fyrirliggjandi fjárhagsskema</span><span class="sxs-lookup"><span data-stu-id="22596-133">To copy an existing account schedule</span></span>
<span data-ttu-id="22596-134">Fjárhagsskemu í stöðluðu útgáfunni af [!INCLUDE[d365fin](includes/d365fin_md.md)] eru grunnurinn að stöðluðu fjárhagsskýrslunum sem mögulega passa ekki þörfum reksturs þíns.</span><span class="sxs-lookup"><span data-stu-id="22596-134">The account schedules in the standard version of [!INCLUDE[d365fin](includes/d365fin_md.md)] are the basis of the standard financial reports, which may not suit the needs of your business.</span></span> <span data-ttu-id="22596-135">Til að búa til þínar eigin fjárhagsskýrslur á fljótlegan hátt geturðu byrjað á því að afrita fyrirliggjandi fjárhagsskema.</span><span class="sxs-lookup"><span data-stu-id="22596-135">To quickly create your own financial reports, you can start by copying an existing account schedule.</span></span>
1. <span data-ttu-id="22596-136">Í glugganum **Fjárhagsskema** skal velja fjárhagsskema og síðan velja aðgerðina **Afrita fjárhagsskema**.</span><span class="sxs-lookup"><span data-stu-id="22596-136">In the **Account Schedules** window, select an account schedule, and then choose the **Copy Account Schedule** action.</span></span>
2. <span data-ttu-id="22596-137">Í glugganum **Afrita fjárhagsskema** skal fylla út reitina eftir þörfum og velja síðan hnappinn **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="22596-137">In the **Copy Account Schedule** window, fill in the fields as necessary, and then choose the **OK** button.</span></span>

### <a name="to-create-a-column-that-calculates-percentages"></a><span data-ttu-id="22596-138">Stofnun dálks sem reiknar prósentur:</span><span class="sxs-lookup"><span data-stu-id="22596-138">To create a column that calculates percentages</span></span>  
<span data-ttu-id="22596-139">Stundum getur verið þörf á dálkum í fjárhagsskema til að reikna prósentur heilda.</span><span class="sxs-lookup"><span data-stu-id="22596-139">Sometimes you may want to include a column in an account schedule to calculate percentages of a total.</span></span> <span data-ttu-id="22596-140">Til dæmis, ef nokkrar línur skipta sölu eftir vídd kann að vera þörf á dálki sem birtir prósentu heildarsölu sem hver lína stendur fyrir.</span><span class="sxs-lookup"><span data-stu-id="22596-140">For example, if you have a number of rows that break down sales by dimension, you may want a column to indicate the percentage of total sales that each row represents.</span></span>

1. <span data-ttu-id="22596-141">Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Fjárhagsskemu** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="22596-141">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Account Schedules**, and then choose the related link.</span></span>
2. <span data-ttu-id="22596-142">Í glugganum **Heiti fjárhagsskema** veljið fjárhagsskema.</span><span class="sxs-lookup"><span data-stu-id="22596-142">In the **Account Schedule Names** window, select an account schedule.</span></span>  
3. <span data-ttu-id="22596-143">Veljið aðgerðina **Breyta fjárhagsskema** til að setja upp fjárhagsskemalínu til að reikna heildina sem prósenturnar munu byggjast á.</span><span class="sxs-lookup"><span data-stu-id="22596-143">Choose the **Edit Account Schedule** action to set up an account schedule row to calculate the total on which the percentages will be based.</span></span>  
4. <span data-ttu-id="22596-144">Setjið inn línu beint fyrir ofan fyrstu línuna sem birta á prósentur fyrir.</span><span class="sxs-lookup"><span data-stu-id="22596-144">Insert a line immediately above the first row for which you want to display a percentage.</span></span>  
5. <span data-ttu-id="22596-145">Fyllið inn í reitina í línunni sem hér segir: Í **Tegund samantektar** reitnum er færður inn **Valinn stofn fyrir prósentur**.</span><span class="sxs-lookup"><span data-stu-id="22596-145">Fill in the fields on the line as follows: In the **Totaling Type** field, enter **Set Base for Percent**.</span></span> <span data-ttu-id="22596-146">Í reitnum **Samantekt** er færð inn reikniregla fyrir heildina sem prósentan verður byggð á.</span><span class="sxs-lookup"><span data-stu-id="22596-146">In the **Totaling** field, enter a formula for the total that the percentage will be based on.</span></span> <span data-ttu-id="22596-147">T. d. ef lína 11 inniheldur heildarsölu, skal færa inn **11**.</span><span class="sxs-lookup"><span data-stu-id="22596-147">For example, if row 11 contains the total sales, enter **11**.</span></span>  
6. <span data-ttu-id="22596-148">Veljið aðgerðina **Breyta uppsetningu dálkaútlits** til að setja upp dálk.</span><span class="sxs-lookup"><span data-stu-id="22596-148">Choose the **Edit Column Layout Setup** action to set up a column.</span></span>  
7. <span data-ttu-id="22596-149">Fyllið inn í reitina í línunni sem hér segir: Í **Tegund dálks** reitnum er færður inn **Formúla**.</span><span class="sxs-lookup"><span data-stu-id="22596-149">Fill in the fields on the line as follows: In the **Column Type** field, select **Formula**.</span></span> <span data-ttu-id="22596-150">Í reitnum **Reikniregla** er færð inn reikniregla fyrir upphæðina sem reikna á prósentur fyrir, með % fyrir aftan.</span><span class="sxs-lookup"><span data-stu-id="22596-150">In the **Formula** field, enter a formula for the amount that you want to calculate a percentage for, followed by %.</span></span> <span data-ttu-id="22596-151">Til dæmis ef dálkur N inniheldur hreyfingu, er fært inn **N%**.</span><span class="sxs-lookup"><span data-stu-id="22596-151">For example, if column number N contains the net change, enter **N%**.</span></span>  
8. <span data-ttu-id="22596-152">Skref 4 til 7 eru endurtekin fyrir hvern flokk línu sem skipta á niður eftir prósentum.</span><span class="sxs-lookup"><span data-stu-id="22596-152">Repeat steps 4 through 7 for each group of rows that you want to break down by percentage.</span></span>

## <a name="to-set-up-account-schedules-with-overviews"></a><span data-ttu-id="22596-153">Uppsetning fjárhagsskema með yfirlitum</span><span class="sxs-lookup"><span data-stu-id="22596-153">To set up account schedules with overviews</span></span>  
<span data-ttu-id="22596-154">Hægt er að nota fjárhagsskema til að búa til reikning sem ber saman upphæðir fjárhagsreiknings og fjárhagsáætlunar.</span><span class="sxs-lookup"><span data-stu-id="22596-154">You can use an account schedule to create a statement comparing general ledger figures and general leger budget figures.</span></span>

1. <span data-ttu-id="22596-155">Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Fjárhagsskemu** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="22596-155">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Account Schedules**, and then choose the related link.</span></span>
2. <span data-ttu-id="22596-156">Í glugganum **Heiti fjárhagsskema** veljið fjárhagsskema.</span><span class="sxs-lookup"><span data-stu-id="22596-156">In the **Account Schedule Names** window, select an account schedule.</span></span>  
3. <span data-ttu-id="22596-157">Veljið aðgerðina **Breyta fjárhagsskema**.</span><span class="sxs-lookup"><span data-stu-id="22596-157">Choose the **Edit Account Schedule** action</span></span>  
4. <span data-ttu-id="22596-158">Í glugganum **Fjárhagsskema** skal velja heiti sjálfgefins fjárhagsskema í reitnum **Heiti**.</span><span class="sxs-lookup"><span data-stu-id="22596-158">In the **Account Schedule** window, in the **Name** field, select the default account schedule name.</span></span>
5. <span data-ttu-id="22596-159">Veljið aðgerðina **Setja inn reikning**.</span><span class="sxs-lookup"><span data-stu-id="22596-159">Choose the **Insert Accounts** action.</span></span>  
6. <span data-ttu-id="22596-160">Reikningarnir sem eiga að vera í yfirlitinu eru valdir og smellt á **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="22596-160">Select the accounts that you want to include in your statement, and then choose the **OK** button.</span></span>

    <span data-ttu-id="22596-161">Reikningarnir eru ekki settir inn í fjárhagsskemað.</span><span class="sxs-lookup"><span data-stu-id="22596-161">The accounts are now inserted into your account schedule.</span></span> <span data-ttu-id="22596-162">Einnig er hægt að breyta dálkauppsetningunni.</span><span class="sxs-lookup"><span data-stu-id="22596-162">If you want you can also change the column layout.</span></span>  
7. <span data-ttu-id="22596-163">Veljið aðgerðina **Yfirlit**.</span><span class="sxs-lookup"><span data-stu-id="22596-163">Choose the **Overview** action.</span></span>  
8. <span data-ttu-id="22596-164">Í flýtiflipanum **Víddarafmarkanir** skal stilla afmörkunarheitið sem á að nota á áætlunarafmörkun.</span><span class="sxs-lookup"><span data-stu-id="22596-164">On the **Dimension Filters** FastTab, set the budget filter to the desired filter name.</span></span>  
9. <span data-ttu-id="22596-165">Velja hnappinn **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="22596-165">Choose the **OK** button.</span></span>  

<span data-ttu-id="22596-166">Nú er hægt að afrita áætlunaryfirlitið og líma það inn í töflureikni.</span><span class="sxs-lookup"><span data-stu-id="22596-166">Now you can copy and paste your budget statement into a spreadsheet.</span></span>  

## <a name="comparing-accounting-periods-using-period-formulas"></a><span data-ttu-id="22596-167">Samanburður á reikningstímabilum með reiknireglum tímabils</span><span class="sxs-lookup"><span data-stu-id="22596-167">Comparing Accounting Periods using Period Formulas</span></span>
<span data-ttu-id="22596-168">Fjárhagsskemað þitt getur borið saman niðurstöður mismunandi reikningstímabila, svo sem þessum mánuði miðað við sama mánuð í fyrra.</span><span class="sxs-lookup"><span data-stu-id="22596-168">Your account schedule can compare the results of different accounting periods, such as this month versus same month last year.</span></span> <span data-ttu-id="22596-169">Til að gera það bætir þú við dálki með reitnum **Reikniregla samanburðartímabils** og stillir síðan þennan reit á reiknireglu fyrir tímabil.</span><span class="sxs-lookup"><span data-stu-id="22596-169">To do that, you add a column with the **Comparison Period Formula** field, and then set that field to a period formula.</span></span>  

<span data-ttu-id="22596-170">Reikningstímabil þarf ekki að vera háð almanakinu, en þó verður að vera sami fjöldi reikningstímabila á öllum fjárhagsárum, þótt tímabilin geti verið mislöng.</span><span class="sxs-lookup"><span data-stu-id="22596-170">An accounting period does not have to match the calendar, but each fiscal year must have the same number of accounting periods, even though each period can be different in length.</span></span>   

[!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="22596-171"> nýtir reikniregluna fyrir tímabil til að reikna út upphæð frá samanburðartímabili miðað við tímabilið sem fæst við dagsetningarafmörkun á skýrslubeiðninni.</span><span class="sxs-lookup"><span data-stu-id="22596-171"> uses the period formula to calculate the amount from the comparison period in relation to the period represented by the date filter on the report request.</span></span> <span data-ttu-id="22596-172">Samanburðartímabilið byggir á upphafsdagsetningu dagsetningarsíunnar.</span><span class="sxs-lookup"><span data-stu-id="22596-172">The comparison period is based on the period of the start date of the date filter.</span></span> <span data-ttu-id="22596-173">Skammstafanirnar sem eiga við eru eftirfarandi:</span><span class="sxs-lookup"><span data-stu-id="22596-173">The abbreviations for period specifications are:</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="22596-174">Skammstöfun</span><span class="sxs-lookup"><span data-stu-id="22596-174">Abbreviation</span></span></th>
<th><span data-ttu-id="22596-175">Description</span><span class="sxs-lookup"><span data-stu-id="22596-175">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="22596-176">T</span><span class="sxs-lookup"><span data-stu-id="22596-176">P</span></span></p></td>
<td><p><span data-ttu-id="22596-177">Tímabil</span><span class="sxs-lookup"><span data-stu-id="22596-177">Period</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="22596-178">ST</span><span class="sxs-lookup"><span data-stu-id="22596-178">LP</span></span></p></td>
<td><p><span data-ttu-id="22596-179">Síðasta tímabil reikningsárs, hálfs árs eða ársfjórðungs.</span><span class="sxs-lookup"><span data-stu-id="22596-179">Last period of a fiscal year, half-year or quarter.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="22596-180">CP</span><span class="sxs-lookup"><span data-stu-id="22596-180">CP</span></span></p></td>
<td><p><span data-ttu-id="22596-181">Gildandi tímabil reikningsárs, hálfs árs eða ársfjórðungs.</span><span class="sxs-lookup"><span data-stu-id="22596-181">Current period of a fiscal year, half-year or quarter.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="22596-182">RÁ</span><span class="sxs-lookup"><span data-stu-id="22596-182">FY</span></span></p></td>
<td><p><span data-ttu-id="22596-183">Reikningsár.</span><span class="sxs-lookup"><span data-stu-id="22596-183">Fiscal year.</span></span> <span data-ttu-id="22596-184">Til dæmis á RÁ[1..3] við um fyrsta fjórðung yfirstandandi reikningsárs.</span><span class="sxs-lookup"><span data-stu-id="22596-184">For example, FY[1..3] denotes first quarter of the current fiscal year</span></span></p></td>
</tr>
</tbody>
</table>

<span data-ttu-id="22596-185">Dæmi um reiknireglur:</span><span class="sxs-lookup"><span data-stu-id="22596-185">Examples of formulas:</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="22596-186">Reikniregla</span><span class="sxs-lookup"><span data-stu-id="22596-186">Formula</span></span></th>
<th><span data-ttu-id="22596-187">Description</span><span class="sxs-lookup"><span data-stu-id="22596-187">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="22596-188">&lt;Autt&gt;</span><span class="sxs-lookup"><span data-stu-id="22596-188">&lt;Blank&gt;</span></span></p></td>
<td><p><span data-ttu-id="22596-189">Yfirstandandi tímabil</span><span class="sxs-lookup"><span data-stu-id="22596-189">Current period</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="22596-190">-1T</span><span class="sxs-lookup"><span data-stu-id="22596-190">-1P</span></span></p></td>
<td><p><span data-ttu-id="22596-191">Fyrra tímabil</span><span class="sxs-lookup"><span data-stu-id="22596-191">Previous period</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="22596-192">-1RÁ[..ST]</span><span class="sxs-lookup"><span data-stu-id="22596-192">-1FY[1..LP]</span></span></p></td>
<td><p><span data-ttu-id="22596-193">Allt fyrra reikningsár</span><span class="sxs-lookup"><span data-stu-id="22596-193">Entire previous fiscal year</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="22596-194">-1RÁ</span><span class="sxs-lookup"><span data-stu-id="22596-194">-1FY</span></span></p></td>
<td><p><span data-ttu-id="22596-195">Yfirstandandi tímabil á fyrra reikningsári</span><span class="sxs-lookup"><span data-stu-id="22596-195">Current period in previous fiscal year</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="22596-196">-1RÁ[1..3]</span><span class="sxs-lookup"><span data-stu-id="22596-196">-1FY[1..3]</span></span></p></td>
<td><p><span data-ttu-id="22596-197">Fyrsti fjórðung fyrra reikningsárs</span><span class="sxs-lookup"><span data-stu-id="22596-197">First quarter of previous fiscal year</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="22596-198">-1RÁ[..YT]</span><span class="sxs-lookup"><span data-stu-id="22596-198">-1FY[1..CP]</span></span></p></td>
<td><p><span data-ttu-id="22596-199">Frá upphafi fyrra reikningsárs til yfirstandandi tímabils og með því</span><span class="sxs-lookup"><span data-stu-id="22596-199">From the beginning of previous fiscal year to current period in previous fiscal year, inclusive</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="22596-200">-1RÁ[YT..ST]</span><span class="sxs-lookup"><span data-stu-id="22596-200">-1FY[CP..LP]</span></span></p></td>
<td><p><span data-ttu-id="22596-201">Frá yfirstandandi tímabili á fyrra reikningsári til síðasta tímabils fyrra reikningsárs og með því</span><span class="sxs-lookup"><span data-stu-id="22596-201">From current period in previous fiscal year to last period of previous fiscal year, inclusive</span></span></p></td>
</tr>
</tbody>
</table>

<span data-ttu-id="22596-202">Ef þú vilt reikna eftir venjulegum tímabilum þarf í staðinn að slá inn reiknireglu í reitinn **Reikniregla samanburðartímabils**.</span><span class="sxs-lookup"><span data-stu-id="22596-202">If you want to calculate by regular time periods, you must enter a formula in the **Comparison Date Formula** field instead.</span></span>

> [!NOTE]
> <span data-ttu-id="22596-203">Það er ekki alltaf augljóst hvaða tímabil þú ert að bera saman vegna þess að þú getur stillt afmörkunardagsetningu í skýrslu sem nær yfir aðrar dagsetningar en reikningstímabilin sem endurspeglast í gögnum bókhaldslykilsins.</span><span class="sxs-lookup"><span data-stu-id="22596-203">It is not always transparent which periods you are comparing because you can set a date filter on a report that spans different dates than the accounting periods that are reflected in the data in the chart of accounts.</span></span> <span data-ttu-id="22596-204">Til dæmis stofnar þú fjárhagsskema þar sem þú vilt bera þetta tímabil saman við sama tímabil í fyrra, þannig að þú stillir reitinn **Afmörkunartímabil samanburðardagsetningar** á *-1FY*.</span><span class="sxs-lookup"><span data-stu-id="22596-204">For example, you create an account schedule where you want to compare this period with the same period last year, so you set the **Comparison Date Period Filter** field to *-1FY*.</span></span> <span data-ttu-id="22596-205">Síðan keyrir þú skýrsluna 28. febrúar og setur afmörkunardagsetninguna á janúar og febrúar.</span><span class="sxs-lookup"><span data-stu-id="22596-205">Then, you run the report on February 28th and set the date filter to January and February.</span></span> <span data-ttu-id="22596-206">Fyrir vikið ber fjárhagsskemað saman janúar og febrúar á þessu ári við janúar á síðasta ári, sem er eina reikningstímabilið sem hefur verið lokið á þessum tveimur árum.</span><span class="sxs-lookup"><span data-stu-id="22596-206">As a result, the account schedule compares January and February this year to January last year, which is the only completed accounting period of the two for last year.</span></span>  


## <a name="see-also"></a><span data-ttu-id="22596-207">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="22596-207">See Also</span></span>
[<span data-ttu-id="22596-208">Viðskiptaupplýsingar</span><span class="sxs-lookup"><span data-stu-id="22596-208">Business Intelligence</span></span>](bi.md)  
[<span data-ttu-id="22596-209">Fjármál</span><span class="sxs-lookup"><span data-stu-id="22596-209">Finance</span></span>](finance.md)  
[<span data-ttu-id="22596-210">Uppsetning Fjármála</span><span class="sxs-lookup"><span data-stu-id="22596-210">Setting Up Finance</span></span>](finance-setup-finance.md)  
[<span data-ttu-id="22596-211">Fjárhagur og bókhaldslyklar</span><span class="sxs-lookup"><span data-stu-id="22596-211">The General Ledger and the Chart of Accounts</span></span>](finance-general-ledger.md)  
<span data-ttu-id="22596-212">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="22596-212">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

