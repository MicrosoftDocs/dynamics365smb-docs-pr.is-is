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
ms.date: 04/16/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 7c346455a9e27d7274b116754f1d594484b95d67
ms.openlocfilehash: f9f5b3a25a24d4d10c80d048153e68030733bf9e
ms.contentlocale: is-is
ms.lasthandoff: 04/18/2018

---
# <a name="work-with-account-schedules"></a><span data-ttu-id="f1aae-103">Vinna með fjárhagsskemu</span><span class="sxs-lookup"><span data-stu-id="f1aae-103">Work with Account Schedules</span></span>
<span data-ttu-id="f1aae-104">Notaðu reikningsáætlanir til að fá innsýn í fjárhagsupplýsingar sem eru geymdar í bókhaldslyklum.</span><span class="sxs-lookup"><span data-stu-id="f1aae-104">Use account schedules to get insight into the financial data stored in your chart of accounts.</span></span> <span data-ttu-id="f1aae-105">Fjárhagsskemu eru notuð til að greina upphæðir í fjárhagsreikningi og bera saman fjárhagsfærslur og færslur í fjárhagsáætlunarskýrslu.</span><span class="sxs-lookup"><span data-stu-id="f1aae-105">Account schedules analyze figures in G/L accounts, and compare general ledger entries with general ledger budget entries.</span></span> <span data-ttu-id="f1aae-106">Niðurstöðurnar birtast í myndritum í Mitt hlutverk, eins og myndrit sjóðstreymis.</span><span class="sxs-lookup"><span data-stu-id="f1aae-106">The results display in charts on your Role Center, such as the Cash Flow chart.</span></span>  

[!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="f1aae-107"> veitir nokkrar sýnishornareikninga sem hægt er að nota strax eða þú getur sett upp eigin línur og dálka til að tilgreina tölurnar sem þú vilt bera saman.</span><span class="sxs-lookup"><span data-stu-id="f1aae-107"> provides a few sample account schedules that you can use right away, or you can set up your own rows and columns to specify the figures to compare.</span></span> <span data-ttu-id="f1aae-108">Notendur getur þú búið til fjárhagskema til að reikna út framlegð fyrir víddir eins og deildir eða hópa viðskiptamanna.</span><span class="sxs-lookup"><span data-stu-id="f1aae-108">For example, you can create account schedules to calculate profit margins on dimensions like departments or customer groups.</span></span> <span data-ttu-id="f1aae-109">Hægt er að búa til eins margar sérsniðnar fjárhagsskýrslur og óskað er.</span><span class="sxs-lookup"><span data-stu-id="f1aae-109">You can create as many customized financial statements as you want.</span></span>  

<span data-ttu-id="f1aae-110">Uppsetning fjárhagsskema krefst skilnings á fjárhagsgögnum í bókhaldslyklinum.</span><span class="sxs-lookup"><span data-stu-id="f1aae-110">Setting up account schedules requires an understanding of the financial data in the chart of accounts.</span></span> <span data-ttu-id="f1aae-111">Hægt er til dæmis að skoða fjárhagsfærslur sem prósentuhlutfall af áætlunarfærslum.</span><span class="sxs-lookup"><span data-stu-id="f1aae-111">For example, you can view general ledger entries as percentages of budget entries.</span></span> <span data-ttu-id="f1aae-112">Þetta krefst þess að fjárhagsáætlanir séu búnar til.</span><span class="sxs-lookup"><span data-stu-id="f1aae-112">This requires that budgets are created.</span></span> <span data-ttu-id="f1aae-113">Frekari upplýsingar eru í [Stofna fjárhagsáætlun](finance-how-create-budgets.md).</span><span class="sxs-lookup"><span data-stu-id="f1aae-113">For more information, see [Create G/L Budgets](finance-how-create-budgets.md).</span></span>

## <a name="account-categories-and-account-schedules"></a><span data-ttu-id="f1aae-114">Lykiltegundir og fjárhagsskemu</span><span class="sxs-lookup"><span data-stu-id="f1aae-114">Account Categories and Account Schedules</span></span>
<span data-ttu-id="f1aae-115">Hægt er að nota lykiltegundir til að breyta sniði fjárhagsskýrslna.</span><span class="sxs-lookup"><span data-stu-id="f1aae-115">You can use account categories to change the layout of your financial statements.</span></span> <span data-ttu-id="f1aae-116">Þegar lykiltegundir hafa verið settar upp í glugganum **Flokkar fjárhagsreikninga** og aðgerðin **Mynda fjárhagsskemu** er valin, eru undirliggjandi fjárhagsskemu fyrir kjarnaviðskiptaskýrslur uppfærð.</span><span class="sxs-lookup"><span data-stu-id="f1aae-116">After you set up your account categories in the **G/L Account Categories** window, and you choose the **Generate Account Schedules** action, the underlying account schedules for the core financial reports are updated.</span></span> <span data-ttu-id="f1aae-117">Næst þegar einhver af þessum skýrslum er keyrð, eins og stöðuyfirlit, er nýjum samtölum og undirfærslum bætt við, samkvæmt þeim breytingum sem gerðar voru.</span><span class="sxs-lookup"><span data-stu-id="f1aae-117">The next time you run one of these reports, such as the balance statement, new totals and subentries are added, based on your changes.</span></span> <span data-ttu-id="f1aae-118">Frekari upplýsingar er að finna í [Fjárhagur og bókhaldslyklar](finance-general-ledger.md).</span><span class="sxs-lookup"><span data-stu-id="f1aae-118">For more information, see [The General Ledger and the Chart of Accounts](finance-general-ledger.md).</span></span>  

## <a name="to-create-new-account-schedules"></a><span data-ttu-id="f1aae-119">Nýtt fjárhagsskema búið til:</span><span class="sxs-lookup"><span data-stu-id="f1aae-119">To create new account schedules</span></span>  
 <span data-ttu-id="f1aae-120">Fjárhagsskemu eru notuð til að greina upphæðir í fjárhagsreikningi eða bera saman fjárhagsfærslur og fjárhagsáætlunarfærslur.</span><span class="sxs-lookup"><span data-stu-id="f1aae-120">You use account schedules to analyze figures in general ledger accounts or to compare general ledger entries with general ledger budget entries.</span></span> <span data-ttu-id="f1aae-121">Hægt er til dæmis að skoða fjárhagsfærslur sem prósentuhlutfall af áætlunarfærslum.</span><span class="sxs-lookup"><span data-stu-id="f1aae-121">For example, you can view the general ledger entries as percentages of the budget entries.</span></span>

1. <span data-ttu-id="f1aae-122">Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Fjárhagsskemu** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="f1aae-122">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Account Schedules**, and then choose the related link.</span></span>  
2. <span data-ttu-id="f1aae-123">Í glugganum **Heiti fjárhagsskema** skal velja aðgerðina **Nýtt** til að búa til nýtt heiti á fjárhagsskema.</span><span class="sxs-lookup"><span data-stu-id="f1aae-123">In the **Account Schedule Names** window, choose the **New** action to create a new account schedule name.</span></span>
3. <span data-ttu-id="f1aae-124">Fyllið inn í reitina eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="f1aae-124">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. <span data-ttu-id="f1aae-125">Veljið aðgerðina **Breyta fjárhagsskema**.</span><span class="sxs-lookup"><span data-stu-id="f1aae-125">Choose the **Edit Account Schedule** action.</span></span>
5. <span data-ttu-id="f1aae-126">Í glugganum **Fjárhagsskema** skal fylla reitina út eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="f1aae-126">In the **Account Schedule** window, fill in the fields as necessary.</span></span>  

    <span data-ttu-id="f1aae-127">Þegar nýtt fjárhagsskema hefur verið stofnað og línurnar hafa verið settar upp, þarf að setja upp dálka.</span><span class="sxs-lookup"><span data-stu-id="f1aae-127">When you have created a new account schedule and set up the rows, you must set up columns.</span></span> <span data-ttu-id="f1aae-128">Annaðhvort er hægt að setja þær upp handvirkt eða úthluta forskilgreindri dálkauppsetningu á viðkomandi fjárhagsskema.</span><span class="sxs-lookup"><span data-stu-id="f1aae-128">You can either set them up manually or assign a predefined column layout to your account schedule.</span></span>
6. <span data-ttu-id="f1aae-129">Veljið aðgerðina **Breyta uppsetningu dálkaútlits**.</span><span class="sxs-lookup"><span data-stu-id="f1aae-129">Choose the **Edit Column Layout Setup** action.</span></span>
7. <span data-ttu-id="f1aae-130">Í glugganum **Dálkaútlit** skal fylla reitina út eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="f1aae-130">In the **Column Layout** window, fill in the fields as necessary.</span></span>

> [!NOTE]  
>   <span data-ttu-id="f1aae-131">Ef ekki var tilgreint sjálfgefið dálkaútlit fyrir fjárhagsskemað verður að setja dálkana upp handvirkt.</span><span class="sxs-lookup"><span data-stu-id="f1aae-131">If you did not assign a default column layout to the account schedule, you must set the columns up manually.</span></span>   

### <a name="to-create-a-column-that-calculates-percentages"></a><span data-ttu-id="f1aae-132">Stofnun dálks sem reiknar prósentur:</span><span class="sxs-lookup"><span data-stu-id="f1aae-132">To create a column that calculates percentages</span></span>  
<span data-ttu-id="f1aae-133">Stundum getur verið þörf á dálkum í fjárhagsskema til að reikna prósentur heilda.</span><span class="sxs-lookup"><span data-stu-id="f1aae-133">Sometimes you may want to include a column in an account schedule to calculate percentages of a total.</span></span> <span data-ttu-id="f1aae-134">Til dæmis, ef nokkrar línur skipta sölu eftir vídd kann að vera þörf á dálki sem birtir prósentu heildarsölu sem hver lína stendur fyrir.</span><span class="sxs-lookup"><span data-stu-id="f1aae-134">For example, if you have a number of rows that break down sales by dimension, you may want a column to indicate the percentage of total sales that each row represents.</span></span>

1. <span data-ttu-id="f1aae-135">Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Fjárhagsskemu** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="f1aae-135">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Account Schedules**, and then choose the related link.</span></span>
2. <span data-ttu-id="f1aae-136">Í glugganum **Heiti fjárhagsskema** veljið fjárhagsskema.</span><span class="sxs-lookup"><span data-stu-id="f1aae-136">In the **Account Schedule Names** window, select an account schedule.</span></span>  
3. <span data-ttu-id="f1aae-137">Veljið aðgerðina **Breyta fjárhagsskema** til að setja upp fjárhagsskemalínu til að reikna heildina sem prósenturnar munu byggjast á.</span><span class="sxs-lookup"><span data-stu-id="f1aae-137">Choose the **Edit Account Schedule** action to set up an account schedule row to calculate the total on which the percentages will be based.</span></span>  
4. <span data-ttu-id="f1aae-138">Setjið inn línu beint fyrir ofan fyrstu línuna sem birta á prósentur fyrir.</span><span class="sxs-lookup"><span data-stu-id="f1aae-138">Insert a line immediately above the first row for which you want to display a percentage.</span></span>  
5. <span data-ttu-id="f1aae-139">Fyllið inn í reitina í línunni sem hér segir: Í **Tegund samantektar** reitnum er færður inn **Valinn stofn fyrir prósentur**.</span><span class="sxs-lookup"><span data-stu-id="f1aae-139">Fill in the fields on the line as follows: In the **Totaling Type** field, enter **Set Base for Percent**.</span></span> <span data-ttu-id="f1aae-140">Í reitnum **Samantekt** er færð inn reikniregla fyrir heildina sem prósentan verður byggð á.</span><span class="sxs-lookup"><span data-stu-id="f1aae-140">In the **Totaling** field, enter a formula for the total that the percentage will be based on.</span></span> <span data-ttu-id="f1aae-141">T. d. ef lína 11 inniheldur heildarsölu, skal færa inn **11**.</span><span class="sxs-lookup"><span data-stu-id="f1aae-141">For example, if row 11 contains the total sales, enter **11**.</span></span>  
6. <span data-ttu-id="f1aae-142">Veljið aðgerðina **Breyta uppsetningu dálkaútlits** til að setja upp dálk.</span><span class="sxs-lookup"><span data-stu-id="f1aae-142">Choose the **Edit Column Layout Setup** action to set up a column.</span></span>  
7. <span data-ttu-id="f1aae-143">Fyllið inn í reitina í línunni sem hér segir: Í **Tegund dálks** reitnum er færður inn **Formúla**.</span><span class="sxs-lookup"><span data-stu-id="f1aae-143">Fill in the fields on the line as follows: In the **Column Type** field, select **Formula**.</span></span> <span data-ttu-id="f1aae-144">Í reitnum **Reikniregla** er færð inn reikniregla fyrir upphæðina sem reikna á prósentur fyrir, með % fyrir aftan.</span><span class="sxs-lookup"><span data-stu-id="f1aae-144">In the **Formula** field, enter a formula for the amount that you want to calculate a percentage for, followed by %.</span></span> <span data-ttu-id="f1aae-145">Til dæmis ef dálkur N inniheldur hreyfingu, er fært inn **N%**.</span><span class="sxs-lookup"><span data-stu-id="f1aae-145">For example, if column number N contains the net change, enter **N%**.</span></span>  
8. <span data-ttu-id="f1aae-146">Skref 4 til 7 eru endurtekin fyrir hvern flokk línu sem skipta á niður eftir prósentum.</span><span class="sxs-lookup"><span data-stu-id="f1aae-146">Repeat steps 4 through 7 for each group of rows that you want to break down by percentage.</span></span>

## <a name="to-set-up-account-schedules-with-overviews"></a><span data-ttu-id="f1aae-147">Uppsetning fjárhagsskema með yfirlitum</span><span class="sxs-lookup"><span data-stu-id="f1aae-147">To set up account schedules with overviews</span></span>  
<span data-ttu-id="f1aae-148">Hægt er að nota fjárhagsskema til að búa til reikning sem ber saman upphæðir fjárhagsreiknings og fjárhagsáætlunar.</span><span class="sxs-lookup"><span data-stu-id="f1aae-148">You can use an account schedule to create a statement comparing general ledger figures and general leger budget figures.</span></span>

1. <span data-ttu-id="f1aae-149">Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Fjárhagsskemu** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="f1aae-149">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Account Schedules**, and then choose the related link.</span></span>
2. <span data-ttu-id="f1aae-150">Í glugganum **Heiti fjárhagsskema** veljið fjárhagsskema.</span><span class="sxs-lookup"><span data-stu-id="f1aae-150">In the **Account Schedule Names** window, select an account schedule.</span></span>  
3. <span data-ttu-id="f1aae-151">Veljið aðgerðina **Breyta fjárhagsskema**.</span><span class="sxs-lookup"><span data-stu-id="f1aae-151">Choose the **Edit Account Schedule** action</span></span>  
4. <span data-ttu-id="f1aae-152">Í glugganum **Fjárhagsskema** skal velja heiti sjálfgefins fjárhagsskema í reitnum **Heiti**.</span><span class="sxs-lookup"><span data-stu-id="f1aae-152">In the **Account Schedule** window, in the **Name** field, select the default account schedule name.</span></span>
5. <span data-ttu-id="f1aae-153">Veljið aðgerðina **Setja inn reikning**.</span><span class="sxs-lookup"><span data-stu-id="f1aae-153">Choose the **Insert Accounts** action.</span></span>  
6. <span data-ttu-id="f1aae-154">Reikningarnir sem eiga að vera í yfirlitinu eru valdir og smellt á **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="f1aae-154">Select the accounts that you want to include in your statement, and then choose the **OK** button.</span></span>

    <span data-ttu-id="f1aae-155">Reikningarnir eru ekki settir inn í fjárhagsskemað.</span><span class="sxs-lookup"><span data-stu-id="f1aae-155">The accounts are now inserted into your account schedule.</span></span> <span data-ttu-id="f1aae-156">Einnig er hægt að breyta dálkauppsetningunni.</span><span class="sxs-lookup"><span data-stu-id="f1aae-156">If you want you can also change the column layout.</span></span>  
7. <span data-ttu-id="f1aae-157">Veljið aðgerðina **Yfirlit**.</span><span class="sxs-lookup"><span data-stu-id="f1aae-157">Choose the **Overview** action.</span></span>  
8. <span data-ttu-id="f1aae-158">Í flýtiflipanum **Víddarafmarkanir** skal stilla afmörkunarheitið sem á að nota á áætlunarafmörkun.</span><span class="sxs-lookup"><span data-stu-id="f1aae-158">On the **Dimension Filters** FastTab, set the budget filter to the desired filter name.</span></span>  
9. <span data-ttu-id="f1aae-159">Velja hnappinn **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="f1aae-159">Choose the **OK** button.</span></span>  

<span data-ttu-id="f1aae-160">Nú er hægt að afrita áætlunaryfirlitið og líma það inn í töflureikni.</span><span class="sxs-lookup"><span data-stu-id="f1aae-160">Now you can copy and paste your budget statement into a spreadsheet.</span></span>  

## <a name="comparing-accounting-periods-using-period-formulas"></a><span data-ttu-id="f1aae-161">Samanburður á reikningstímabilum með reiknireglum tímabils</span><span class="sxs-lookup"><span data-stu-id="f1aae-161">Comparing Accounting Periods using Period Formulas</span></span>
<span data-ttu-id="f1aae-162">Fjárhagsskemað þitt getur borið saman niðurstöður mismunandi reikningstímabila, svo sem þessum mánuði miðað við sama mánuð í fyrra.</span><span class="sxs-lookup"><span data-stu-id="f1aae-162">Your account schedule can compare the results of different accounting periods, such as this month versus same month last year.</span></span> <span data-ttu-id="f1aae-163">Til að gera það bætir þú við dálki með reitnum **Reikniregla samanburðartímabils** og stillir síðan þennan reit á reiknireglu fyrir tímabil.</span><span class="sxs-lookup"><span data-stu-id="f1aae-163">To do that, you add a column with the **Comparison Period Formula** field, and then set that field to a period formula.</span></span>  

<span data-ttu-id="f1aae-164">Reikningstímabil þarf ekki að vera háð almanakinu, en þó verður að vera sami fjöldi reikningstímabila á öllum fjárhagsárum, þótt tímabilin geti verið mislöng.</span><span class="sxs-lookup"><span data-stu-id="f1aae-164">An accounting period does not have to match the calendar, but each fiscal year must have the same number of accounting periods, even though each period can be different in length.</span></span>   

[!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="f1aae-165"> nýtir reikniregluna fyrir tímabil til að reikna út upphæð frá samanburðartímabili miðað við tímabilið sem fæst við dagsetningarafmörkun á skýrslubeiðninni.</span><span class="sxs-lookup"><span data-stu-id="f1aae-165"> uses the period formula to calculate the amount from the comparison period in relation to the period represented by the date filter on the report request.</span></span> <span data-ttu-id="f1aae-166">Samanburðartímabilið byggir á upphafsdagsetningu dagsetningarsíunnar.</span><span class="sxs-lookup"><span data-stu-id="f1aae-166">The comparison period is based on the period of the start date of the date filter.</span></span> <span data-ttu-id="f1aae-167">Skammstafanirnar sem eiga við eru eftirfarandi:</span><span class="sxs-lookup"><span data-stu-id="f1aae-167">The abbreviations for period specifications are:</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f1aae-168">Skammstöfun</span><span class="sxs-lookup"><span data-stu-id="f1aae-168">Abbreviation</span></span></th>
<th><span data-ttu-id="f1aae-169">Description</span><span class="sxs-lookup"><span data-stu-id="f1aae-169">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f1aae-170">T</span><span class="sxs-lookup"><span data-stu-id="f1aae-170">P</span></span></p></td>
<td><p><span data-ttu-id="f1aae-171">Tímabil</span><span class="sxs-lookup"><span data-stu-id="f1aae-171">Period</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1aae-172">ST</span><span class="sxs-lookup"><span data-stu-id="f1aae-172">LP</span></span></p></td>
<td><p><span data-ttu-id="f1aae-173">Síðasta tímabil reikningsárs, hálfs árs eða ársfjórðungs.</span><span class="sxs-lookup"><span data-stu-id="f1aae-173">Last period of a fiscal year, half-year or quarter.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1aae-174">CP</span><span class="sxs-lookup"><span data-stu-id="f1aae-174">CP</span></span></p></td>
<td><p><span data-ttu-id="f1aae-175">Gildandi tímabil reikningsárs, hálfs árs eða ársfjórðungs.</span><span class="sxs-lookup"><span data-stu-id="f1aae-175">Current period of a fiscal year, half-year or quarter.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1aae-176">RÁ</span><span class="sxs-lookup"><span data-stu-id="f1aae-176">FY</span></span></p></td>
<td><p><span data-ttu-id="f1aae-177">Reikningsár.</span><span class="sxs-lookup"><span data-stu-id="f1aae-177">Fiscal year.</span></span> <span data-ttu-id="f1aae-178">Til dæmis á RÁ[1..3] við um fyrsta fjórðung yfirstandandi reikningsárs.</span><span class="sxs-lookup"><span data-stu-id="f1aae-178">For example, FY[1..3] denotes first quarter of the current fiscal year</span></span></p></td>
</tr>
</tbody>
</table>

<span data-ttu-id="f1aae-179">Dæmi um reiknireglur:</span><span class="sxs-lookup"><span data-stu-id="f1aae-179">Examples of formulas:</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f1aae-180">Reikniregla</span><span class="sxs-lookup"><span data-stu-id="f1aae-180">Formula</span></span></th>
<th><span data-ttu-id="f1aae-181">Description</span><span class="sxs-lookup"><span data-stu-id="f1aae-181">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f1aae-182">&lt;Autt&gt;</span><span class="sxs-lookup"><span data-stu-id="f1aae-182">&lt;Blank&gt;</span></span></p></td>
<td><p><span data-ttu-id="f1aae-183">Yfirstandandi tímabil</span><span class="sxs-lookup"><span data-stu-id="f1aae-183">Current period</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1aae-184">-1T</span><span class="sxs-lookup"><span data-stu-id="f1aae-184">-1P</span></span></p></td>
<td><p><span data-ttu-id="f1aae-185">Fyrra tímabil</span><span class="sxs-lookup"><span data-stu-id="f1aae-185">Previous period</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1aae-186">-1RÁ[..ST]</span><span class="sxs-lookup"><span data-stu-id="f1aae-186">-1FY[1..LP]</span></span></p></td>
<td><p><span data-ttu-id="f1aae-187">Allt fyrra reikningsár</span><span class="sxs-lookup"><span data-stu-id="f1aae-187">Entire previous fiscal year</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1aae-188">-1RÁ</span><span class="sxs-lookup"><span data-stu-id="f1aae-188">-1FY</span></span></p></td>
<td><p><span data-ttu-id="f1aae-189">Yfirstandandi tímabil á fyrra reikningsári</span><span class="sxs-lookup"><span data-stu-id="f1aae-189">Current period in previous fiscal year</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1aae-190">-1RÁ[1..3]</span><span class="sxs-lookup"><span data-stu-id="f1aae-190">-1FY[1..3]</span></span></p></td>
<td><p><span data-ttu-id="f1aae-191">Fyrsti fjórðung fyrra reikningsárs</span><span class="sxs-lookup"><span data-stu-id="f1aae-191">First quarter of previous fiscal year</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1aae-192">-1RÁ[..YT]</span><span class="sxs-lookup"><span data-stu-id="f1aae-192">-1FY[1..CP]</span></span></p></td>
<td><p><span data-ttu-id="f1aae-193">Frá upphafi fyrra reikningsárs til yfirstandandi tímabils og með því</span><span class="sxs-lookup"><span data-stu-id="f1aae-193">From the beginning of previous fiscal year to current period in previous fiscal year, inclusive</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1aae-194">-1RÁ[YT..ST]</span><span class="sxs-lookup"><span data-stu-id="f1aae-194">-1FY[CP..LP]</span></span></p></td>
<td><p><span data-ttu-id="f1aae-195">Frá yfirstandandi tímabili á fyrra reikningsári til síðasta tímabils fyrra reikningsárs og með því</span><span class="sxs-lookup"><span data-stu-id="f1aae-195">From current period in previous fiscal year to last period of previous fiscal year, inclusive</span></span></p></td>
</tr>
</tbody>
</table>

<span data-ttu-id="f1aae-196">Ef þú vilt reikna eftir venjulegum tímabilum þarf í staðinn að slá inn reiknireglu í reitinn **Reikniregla samanburðartímabils**.</span><span class="sxs-lookup"><span data-stu-id="f1aae-196">If you want to calculate by regular time periods, you must enter a formula in the **Comparison Date Formula** field instead.</span></span>

> [!NOTE]
> <span data-ttu-id="f1aae-197">Það er ekki alltaf augljóst hvaða tímabil þú ert að bera saman vegna þess að þú getur stillt afmörkunardagsetningu í skýrslu sem nær yfir aðrar dagsetningar en reikningstímabilin sem endurspeglast í gögnum bókhaldslykilsins.</span><span class="sxs-lookup"><span data-stu-id="f1aae-197">It is not always transparent which periods you are comparing because you can set a date filter on a report that spans different dates than the accounting periods that are reflected in the data in the chart of accounts.</span></span> <span data-ttu-id="f1aae-198">Til dæmis stofnar þú fjárhagsskema þar sem þú vilt bera þetta tímabil saman við sama tímabil í fyrra, þannig að þú stillir reitinn **Afmörkunartímabil samanburðardagsetningar** á *-1FY*.</span><span class="sxs-lookup"><span data-stu-id="f1aae-198">For example, you create an account schedule where you want to compare this period with the same period last year, so you set the **Comparison Date Period Filter** field to *-1FY*.</span></span> <span data-ttu-id="f1aae-199">Síðan keyrir þú skýrsluna 28. febrúar og setur afmörkunardagsetninguna á janúar og febrúar.</span><span class="sxs-lookup"><span data-stu-id="f1aae-199">Then, you run the report on February 28th and set the date filter to January and February.</span></span> <span data-ttu-id="f1aae-200">Fyrir vikið ber fjárhagsskemað saman janúar og febrúar á þessu ári við janúar á síðasta ári, sem er eina reikningstímabilið sem hefur verið lokið á þessum tveimur árum.</span><span class="sxs-lookup"><span data-stu-id="f1aae-200">As a result, the account schedule compares January and February this year to January last year, which is the only completed accounting period of the two for last year.</span></span>  


## <a name="see-also"></a><span data-ttu-id="f1aae-201">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="f1aae-201">See Also</span></span>
[<span data-ttu-id="f1aae-202">Viðskiptaupplýsingar</span><span class="sxs-lookup"><span data-stu-id="f1aae-202">Business Intelligence</span></span>](bi.md)  
[<span data-ttu-id="f1aae-203">Fjármál</span><span class="sxs-lookup"><span data-stu-id="f1aae-203">Finance</span></span>](finance.md)  
[<span data-ttu-id="f1aae-204">Uppsetning Fjármála</span><span class="sxs-lookup"><span data-stu-id="f1aae-204">Setting Up Finance</span></span>](finance-setup-finance.md)  
[<span data-ttu-id="f1aae-205">Fjárhagur og bókhaldslyklar</span><span class="sxs-lookup"><span data-stu-id="f1aae-205">The General Ledger and the Chart of Accounts</span></span>](finance-general-ledger.md)  
<span data-ttu-id="f1aae-206">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="f1aae-206">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

