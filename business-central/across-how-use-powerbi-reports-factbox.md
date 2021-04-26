---
title: Birta sérstillta Power BI-skýrslur fyrir Business Central Data| Microsoft docs
description: Hægt er að nota Power BI skýrslur til að öðlast frekari innsýn í gögn í listum.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: business intelligence, KPI, Odata, Power App, SOAP, analysis
ms.date: 04/01/2021
ms.author: jswymer
ms.openlocfilehash: a600b24e16172134d4f8e78cf47efa4e262cac09
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5777517"
---
# <a name="creating-power-bi-reports-for-displaying-list-data-in-prod_short"></a><span data-ttu-id="c066b-103">Býr til Power BI skýrslur til að birta listagögn í [!INCLUDE[prod_short](includes/prod_short.md)]</span><span class="sxs-lookup"><span data-stu-id="c066b-103">Creating Power BI Reports for Displaying List Data in [!INCLUDE[prod_short](includes/prod_short.md)]</span></span>

[!INCLUDE[prod_long](includes/prod_long.md)] <span data-ttu-id="c066b-104">inniheldur stjórneiningu Power BI upplýsingareits á mörgum mikilvægum listasíðum.</span><span class="sxs-lookup"><span data-stu-id="c066b-104">includes a Power BI FactBox control element on many key list pages.</span></span> <span data-ttu-id="c066b-105">Tilgangurinn með þessum upplýsingareit er að sýna Power BI-skýrslur sem tengjast færslum í listunum sem veita betri innsýn í gögnin.</span><span class="sxs-lookup"><span data-stu-id="c066b-105">The purpose of this FactBox is to display Power BI reports that are related to records in the lists, providing extra insight into the data.</span></span> <span data-ttu-id="c066b-106">Hugmyndin er að þegar farið er milli lína í listanum er skýrslan uppfærð og síuð fyrir valda færslu.</span><span class="sxs-lookup"><span data-stu-id="c066b-106">The idea is that as you move between rows in the list, the report is updated and filtered for the selected entry.</span></span>

[!INCLUDE[prod_long](includes/prod_long.md)] <span data-ttu-id="c066b-107">kemur tilbúið með sumum þessara skýrslna.</span><span class="sxs-lookup"><span data-stu-id="c066b-107">comes ready with some of these reports.</span></span> <span data-ttu-id="c066b-108">Einnig er hægt að búa til eigin sérsniðnar skýrslur sem birtast í þessum upplýsingareit.</span><span class="sxs-lookup"><span data-stu-id="c066b-108">You can also create your own custom reports that display in this FactBox.</span></span> <span data-ttu-id="c066b-109">Þessar skýrslur eru búnar til að svipaðan hátt og aðrar skýrslur.</span><span class="sxs-lookup"><span data-stu-id="c066b-109">Creating these reports is similar to other reports.</span></span> <span data-ttu-id="c066b-110">En fylgja þarf nokkrum hönnunarreglum til að tryggja að skýrslurnar birtist eins og búist er við.</span><span class="sxs-lookup"><span data-stu-id="c066b-110">But there are a few design rules you'll have to follow to make sure the reports display as expected.</span></span> <span data-ttu-id="c066b-111">Þessar reglur eru útskýrðar í þessari grein.</span><span class="sxs-lookup"><span data-stu-id="c066b-111">These rules are explained in this article.</span></span>

> [!NOTE]
> <span data-ttu-id="c066b-112">Fyrir almennar upplýsingar um stofnun og birtingu Power BI-skýrslna fyrir Business Central er að finna í [Myndun Power BI-skýrslna til að birta [!INCLUDE [prod_long](includes/prod_long.md)] gögn](across-how-use-financials-data-source-powerbi.md).</span><span class="sxs-lookup"><span data-stu-id="c066b-112">For general information about creating and publishing Power BI reports for Business Central, see [Building Power BI Reports to Display [!INCLUDE [prod_long](includes/prod_long.md)] Data](across-how-use-financials-data-source-powerbi.md).</span></span> 

## <a name="prerequisites"></a><span data-ttu-id="c066b-113">Frumskilyrði</span><span class="sxs-lookup"><span data-stu-id="c066b-113">Prerequisites</span></span>

- <span data-ttu-id="c066b-114">Power BI-Reikningur.</span><span class="sxs-lookup"><span data-stu-id="c066b-114">A Power BI account.</span></span>
- <span data-ttu-id="c066b-115">Power BI Desktop.</span><span class="sxs-lookup"><span data-stu-id="c066b-115">Power BI Desktop.</span></span>

<!-- 
For more information about getting started, see [Using [!INCLUDE[prod_short](includes/prod_short.md)] as a Power BI Data Source](across-how-use-financials-data-source-powerbi.md).-->

## <a name="create-a-report-for-a-list-page"></a><span data-ttu-id="c066b-116">Búa til skýrslu fyrir listasíðu</span><span class="sxs-lookup"><span data-stu-id="c066b-116">Create a report for a list page</span></span>

1. <span data-ttu-id="c066b-117">Ræsið Power BI Desktop.</span><span class="sxs-lookup"><span data-stu-id="c066b-117">Start Power BI Desktop.</span></span>
2. <span data-ttu-id="c066b-118">Veljið **Sækja gögn** og veljið gagnagjafann fyrir skýrsluna.</span><span class="sxs-lookup"><span data-stu-id="c066b-118">Select **Get Data**, and start choosing the data source for the report.</span></span>

    <span data-ttu-id="c066b-119">Í þessu skrefi skal tilgreina listasíður Business Central sem innihalda gögnin sem eiga að koma fram í skýrslunni.</span><span class="sxs-lookup"><span data-stu-id="c066b-119">In this step, you specify the Business Central list pages that contain the data that you want in the report.</span></span> <span data-ttu-id="c066b-120">Ef þú vilt t.d. stofna skýrslu fyrir sölulista skal tryggja að gagnamengið innihaldi upplýsingar sem tengjast sölu.</span><span class="sxs-lookup"><span data-stu-id="c066b-120">For example, to create a report for the Sales List, ensure the data set contains information related to sales.</span></span>

    <span data-ttu-id="c066b-121">Til að fá frekari upplýsingar skal fylgja leiðbeiningunum [Bæta [!INCLUDE[prod_short](includes/prod_short.md)] við sem gagnagjafa í Power BI Desktop](across-how-use-financials-data-source-powerbi.md#getdata).</span><span class="sxs-lookup"><span data-stu-id="c066b-121">For more information, follow the instructions [Add [!INCLUDE[prod_short](includes/prod_short.md)] as a data source in Power BI Desktop](across-how-use-financials-data-source-powerbi.md#getdata).</span></span>

3. <span data-ttu-id="c066b-122">Stillið afmörkun skýrslunnar.</span><span class="sxs-lookup"><span data-stu-id="c066b-122">Set the report filter.</span></span>

    <span data-ttu-id="c066b-123">Til að gera gagnauppfærslu í valinni færslu á listanum er síu bætt við skýrslu.</span><span class="sxs-lookup"><span data-stu-id="c066b-123">To make the data update to the selected record in the list, you add a filter to the report.</span></span> <span data-ttu-id="c066b-124">Sían verður að innihalda reit gagnagjafans sem er notaður til að auðkenna sérstaklega hverja færslu í listanum.</span><span class="sxs-lookup"><span data-stu-id="c066b-124">The filter must include a field of the data source that's used to uniquely identify each record in the list.</span></span> <span data-ttu-id="c066b-125">Hjá þróunaraðila er þessi reitur *aðallykillinn*.</span><span class="sxs-lookup"><span data-stu-id="c066b-125">In developer terms, this field is the *primary key*.</span></span> <span data-ttu-id="c066b-126">Í flestum tilvikum er aðallykill fyrir lista reiturinn **Nr.**</span><span class="sxs-lookup"><span data-stu-id="c066b-126">In most cases, the primary key for a list is the **No.**</span></span> <span data-ttu-id="c066b-127">.</span><span class="sxs-lookup"><span data-stu-id="c066b-127">field.</span></span>

    <span data-ttu-id="c066b-128">Til að stilla síuna skal gera eftirfarandi:</span><span class="sxs-lookup"><span data-stu-id="c066b-128">To set the filter, do the following steps:</span></span>

    1. <span data-ttu-id="c066b-129">Í **Síunum** skal velja reit aðallykilsins úr listanum yfir tiltæka reiti.</span><span class="sxs-lookup"><span data-stu-id="c066b-129">In the **Filters**, select the primary key field from the list of available fields.</span></span>
    2. <span data-ttu-id="c066b-130">Dragið reitinn yfir á svæðið **Síur** og sleppið honum í reitinn **Síur á öllum síðum**.</span><span class="sxs-lookup"><span data-stu-id="c066b-130">Drag the field to **Filters** pane and drop it in the **Filters on all pages** box.</span></span>
    3. <span data-ttu-id="c066b-131">Stillið **Síugerðina** á **Grunnsíun**.</span><span class="sxs-lookup"><span data-stu-id="c066b-131">Set the **Filter type** to **Basic filtering**.</span></span> <span data-ttu-id="c066b-132">Það getur ekki verið síða, sjónrænt eða ítarleg sía.</span><span class="sxs-lookup"><span data-stu-id="c066b-132">It can't be page, visual, or advanced filter.</span></span>

    ![Afmörkun skýslu stillt fyrir Aðgerðaskráningu sölureikninga](./media/across-how-use-powerbi-reports-factbox/financials-powerbi-report-filter-v3.png)
4. <span data-ttu-id="c066b-134">Hannið útlit skýrslunnar.</span><span class="sxs-lookup"><span data-stu-id="c066b-134">Design the report layout.</span></span>

    <span data-ttu-id="c066b-135">Búið til útlitið með því að draga til reiti og bæta við myndrænum framsetningum.</span><span class="sxs-lookup"><span data-stu-id="c066b-135">Create the layout by dragging fields and adding visualizations.</span></span> <span data-ttu-id="c066b-136">Frekari upplýsingar er að finna í [Vinna með skýrsluyfirlit í Power BI Desktop](/power-bi/create-reports/desktop-report-view) í Power BI-fylgigögnum.</span><span class="sxs-lookup"><span data-stu-id="c066b-136">For more information, see, [Work with Report view in Power BI Desktop](/power-bi/create-reports/desktop-report-view) in the Power BI documentation.</span></span>

5. <span data-ttu-id="c066b-137">Skoðið næstu hluta um hvernig skuli stilla stærð skýrslunnar og nota margar síður.</span><span class="sxs-lookup"><span data-stu-id="c066b-137">See the next sections about sizing the report and using multiple pages.</span></span>

6. <span data-ttu-id="c066b-138">Vistið og gefið skýrslunni heiti.</span><span class="sxs-lookup"><span data-stu-id="c066b-138">Save and name the report.</span></span>

    <span data-ttu-id="c066b-139">Mikilvægt er að gefa skýrslunni heiti sem inniheldur heiti listasíðunnar sem tengist skýrslunni.</span><span class="sxs-lookup"><span data-stu-id="c066b-139">It's important to give the report a name that contains the name of the list page associated with the report.</span></span> <span data-ttu-id="c066b-140">Ef skýrsla er t.d. fyrir listasíðuna **Vörur** skal hafa með orðið *vörur* einhvers staðar í heitinu.</span><span class="sxs-lookup"><span data-stu-id="c066b-140">For example, if the report is for the **Items** list page, include the word *items* somewhere in the name.</span></span>  

    <span data-ttu-id="c066b-141">Þessi nafnavenja er ekki skilyrði.</span><span class="sxs-lookup"><span data-stu-id="c066b-141">This naming convention isn't a requirement.</span></span> <span data-ttu-id="c066b-142">Hins vegar gerir það val á skýrslum í [!INCLUDE[prod_short](includes/prod_short.md)] fljótlegri.</span><span class="sxs-lookup"><span data-stu-id="c066b-142">However, it makes selecting reports in [!INCLUDE[prod_short](includes/prod_short.md)] quicker.</span></span> <span data-ttu-id="c066b-143">Þegar skýrsluvalssíða opnast af listasíðu er hún síuð sjálfkrafa út frá síðuheitinu.</span><span class="sxs-lookup"><span data-stu-id="c066b-143">When the report selection page opens from a list page, it's automatically filtered based on the page name.</span></span> <span data-ttu-id="c066b-144">Þessi sía er búin til að takmarka skýrslurnar sem eru birtar.</span><span class="sxs-lookup"><span data-stu-id="c066b-144">This filtering is done to limit the reports that are displayed.</span></span> <span data-ttu-id="c066b-145">Einnig er hægt að fjarlægja afmörkunina til að birta heildarlista yfir skýrslur sem eru tiltækar í Power BI.</span><span class="sxs-lookup"><span data-stu-id="c066b-145">Users can clear the filter to get a full list of reports available in Power BI.</span></span>

7. <span data-ttu-id="c066b-146">Þegar þessu er lokið skal birta skýrsluna eins og venjulega.</span><span class="sxs-lookup"><span data-stu-id="c066b-146">When you're done, publish the report as usual.</span></span>

    <span data-ttu-id="c066b-147">Frekari upplýsingar er að finna í [Birta skýrslu](across-how-use-financials-data-source-powerbi.md#publish-reports).</span><span class="sxs-lookup"><span data-stu-id="c066b-147">For more information, see [Publishing a Report](across-how-use-financials-data-source-powerbi.md#publish-reports).</span></span>

8. <span data-ttu-id="c066b-148">Prófið skýrsluna.</span><span class="sxs-lookup"><span data-stu-id="c066b-148">Test the report.</span></span>

    <span data-ttu-id="c066b-149">Þegar skýrslurnar hafa verið birtar á vinnusvæðinu ættu þær að vera aðgengilegar í Power BI-upplýsingareitnum á listasíðunni í [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="c066b-149">Once the reports been published to your workspace, it should be available from the Power BI FactBox on the list page in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>

    <span data-ttu-id="c066b-150">Til að prófa hann skal fara í gegnum eftirfarandi skref.</span><span class="sxs-lookup"><span data-stu-id="c066b-150">To test it, do the following steps.</span></span>

    1. <span data-ttu-id="c066b-151">Opnaðu [!INCLUDE[prod_short](includes/prod_short.md)] og farðu á listasíðuna.</span><span class="sxs-lookup"><span data-stu-id="c066b-151">Open [!INCLUDE[prod_short](includes/prod_short.md)] and go to the list page.</span></span>
    2. <span data-ttu-id="c066b-152">Ef Power BI-upplýsingareiturinn sést ekki skal fara á aðgerðarstikuna, síðan velja **Aðgerðir** > **Birta** > **Sýna/fela Power BI skýrslur**.</span><span class="sxs-lookup"><span data-stu-id="c066b-152">If you don't see the Power BI FactBox, go the action bar, then select **Actions** > **Display** > **Show/Hide Power BI Reports**.</span></span>
    3. <span data-ttu-id="c066b-153">Í Power BI-upplýsingareitnum skal velja **Velja skýrslur**, velja reitinn **Virkja** fyrir skýrsluna, síðan velja **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="c066b-153">In the Power BI FactBox, select **Select Reports**, select the **Enable** box for the report, then select **OK**.</span></span>

    <span data-ttu-id="c066b-154">Skýrslan birtist ef þetta er hannað á réttan hátt.</span><span class="sxs-lookup"><span data-stu-id="c066b-154">If designed correctly, the report displays.</span></span>  

## <a name="set-the-report-size-and-color"></a><span data-ttu-id="c066b-155">Stilla stærð og lit skýrslunnar</span><span class="sxs-lookup"><span data-stu-id="c066b-155">Set the report size and color</span></span>

<span data-ttu-id="c066b-156">Stærð skýrslu verður að stilla á 325 sinnum 310 pixla.</span><span class="sxs-lookup"><span data-stu-id="c066b-156">The size of the report must be set to 325 pixels by 310 pixels.</span></span> <span data-ttu-id="c066b-157">Þessi stærð býður upp á rétta kvörðun á skýrslu í tiltæku bili í Power BI stjórnun upplýsingareits í [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="c066b-157">This size provides the proper scaling of the report in the available space of the Power BI FactBox control in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="c066b-158">Til að skilgreina stærð skýrslu skal staðsetja fókus utan svæðis fyrir útlit skýrslu og velja svo tákn fyrir málningarrúllu.</span><span class="sxs-lookup"><span data-stu-id="c066b-158">To define the size of the report, place focus outside of the report layout area, and then choose the paint roller icon.</span></span>

![Breidd og hæð skýrslu stillt fyrir Aðgerðaskráningu sölureikninga](./media/across-how-use-powerbi-reports-factbox/financials-powerbi-report-sizing-v3.png)

<span data-ttu-id="c066b-160">Hægt er að breyta breidd og hæð skýrslunnar með því að velja **Sérsníða** í reitnum **Tegund**.</span><span class="sxs-lookup"><span data-stu-id="c066b-160">You can change the width and height of the report by choosing **Custom** in the **Type** field.</span></span>

<span data-ttu-id="c066b-161">Ef bakgrunnur skýringarinnar á að vera með bakgrunnslit Power BI upplýsingareitsins skal stilla bakgrunnslit skýrslu á *#FFFFFF* (hvítur).</span><span class="sxs-lookup"><span data-stu-id="c066b-161">If you want the background of the report to blend with the background color of the Power BI FactBox control, set report background color to *#FFFFFF* (white).</span></span> 

> [!TIP]
> <span data-ttu-id="c066b-162">Notið [!INCLUDE [prod_short](includes/prod_short.md)]-þemaskrá til að búa til skýrslur með sama litastíl og [!INCLUDE [prod_short](includes/prod_short.md)]-forritin.</span><span class="sxs-lookup"><span data-stu-id="c066b-162">Use the [!INCLUDE [prod_short](includes/prod_short.md)] theme file to build reports with the same color styling as the [!INCLUDE [prod_short](includes/prod_short.md)] apps.</span></span> <span data-ttu-id="c066b-163">Frekari upplýsingar er að finna í [[!INCLUDE [prod_short](includes/prod_short.md)]-skýrsluþema notað](across-how-use-financials-data-source-powerbi.md#theme).</span><span class="sxs-lookup"><span data-stu-id="c066b-163">For more information, see [Using the [!INCLUDE [prod_short](includes/prod_short.md)] report theme](across-how-use-financials-data-source-powerbi.md#theme).</span></span>

## <a name="reports-with-multiple-pages"></a><span data-ttu-id="c066b-164">Skýrslur með mörgum síðum</span><span class="sxs-lookup"><span data-stu-id="c066b-164">Reports with multiple pages</span></span>

<span data-ttu-id="c066b-165">Með Power BI er hægt að stofna eina skýrslu með mörgum síðum.</span><span class="sxs-lookup"><span data-stu-id="c066b-165">With Power BI, you can create a single report with multiple pages.</span></span> <span data-ttu-id="c066b-166">Fyrir skýrslur sem birtast með listasíðum mælum við hins vegar ekki með því að þær séu með fleiri en eina síðu.</span><span class="sxs-lookup"><span data-stu-id="c066b-166">However, for reports that will display with list pages, we don't recommend that they have more than one page.</span></span> <span data-ttu-id="c066b-167">Power BI upplýsingareiturinn sýnir aðeins fyrstu síðu skýrslunnar.</span><span class="sxs-lookup"><span data-stu-id="c066b-167">The Power BI FactBox will only show the first page of your report.</span></span>

## <a name="fixing-problems"></a><span data-ttu-id="c066b-168">Vandamál lagfærð</span><span class="sxs-lookup"><span data-stu-id="c066b-168">Fixing problems</span></span>

<span data-ttu-id="c066b-169">Þessi hluti veitir upplýsingar um hvernig á að laga vandamál sem gætu komið upp þegar reynt er að skoða Power BI-skýrslu fyrir listasíðu í [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="c066b-169">This section provides instructions about how to fix problems that you might run into when trying to view a Power BI report for a list page in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>  

### <a name="you-cant-see-the-power-bi-factbox-on-a-list-page"></a><span data-ttu-id="c066b-170">Ekki er hægt að sjá Power BI-upplýsingareitinn á listasíðu</span><span class="sxs-lookup"><span data-stu-id="c066b-170">You can't see the Power BI FactBox on a list page</span></span>

<span data-ttu-id="c066b-171">Sjálfgefið er að Power BI-upplýsingareiturinn sé falinn.</span><span class="sxs-lookup"><span data-stu-id="c066b-171">By default, the Power BI FactBox is hidden from view.</span></span> <span data-ttu-id="c066b-172">Til að sýna upplýsingareitinn á síðu skal á aðgerðastikunni velja **Aðgerðir** > **Birta** > **Sýna/fela Power BI-skýrslur**.</span><span class="sxs-lookup"><span data-stu-id="c066b-172">To show the FactBox on a page, from the action bar, select **Actions** > **Display** > **Show/Hide Power BI Reports**.</span></span>

### <a name="you-cant-see-the-report-in-the-select-report-pane"></a><span data-ttu-id="c066b-173">Ekki er hægt að sjá skýrsluna á svæðinu Velja skýrslu</span><span class="sxs-lookup"><span data-stu-id="c066b-173">You can't see the report in the Select Report pane</span></span>

<span data-ttu-id="c066b-174">Það er líklega vegna þess að heiti skýrslunnar inniheldur ekki heiti listasíðunnar sem er sýnd.</span><span class="sxs-lookup"><span data-stu-id="c066b-174">It's probably because the report's name doesn't contain the name of the list page that's being shown.</span></span> <span data-ttu-id="c066b-175">Hreinsaðu síuna til að birta heildarlista yfir skýrslur sem eru tiltækar í Power BI.</span><span class="sxs-lookup"><span data-stu-id="c066b-175">Clear the filter to get a full list of Power BI reports available.</span></span>  

### <a name="report-is-loaded-but-blank-not-filtered-or-filtered-incorrectly"></a><span data-ttu-id="c066b-176">Verið er að hlaða skrá en hún er tóm, ekki síuð eða síuð á rangan hátt</span><span class="sxs-lookup"><span data-stu-id="c066b-176">Report is loaded but blank, not filtered, or filtered incorrectly</span></span>

<span data-ttu-id="c066b-177">Sannprófa verður að skýrsluafmörkunin innihaldi réttan aðallykil.</span><span class="sxs-lookup"><span data-stu-id="c066b-177">Verify that the report filter contains the right primary key.</span></span> <span data-ttu-id="c066b-178">Yfirleitt er þessi reitur **Nr.**</span><span class="sxs-lookup"><span data-stu-id="c066b-178">In most cases, this field is the **No.**</span></span> <span data-ttu-id="c066b-179">reitur, en í töflunni **Fjárhagsfærsla**, til dæmis, verður að nota **Færslunr.** reitinn.</span><span class="sxs-lookup"><span data-stu-id="c066b-179">field, but in the **G/L Entry** table, for example, you must use the **Entry No.** field.</span></span>

### <a name="report-is-loaded-but-it-shows-a-page-you-didnt-expect"></a><span data-ttu-id="c066b-180">Skýrslu er hlaðið inn, en hún sýnir síðu sem þú bjóst ekki við</span><span class="sxs-lookup"><span data-stu-id="c066b-180">Report is loaded, but it shows a page you didn't expect</span></span>

<span data-ttu-id="c066b-181">Sannprófa verður að skýrslan sem notandi vill að birtist sé fyrsta síðan í skýrslunni.</span><span class="sxs-lookup"><span data-stu-id="c066b-181">Verify that the page you want displayed is the first page in your report.</span></span>  

### <a name="report-appears-with-an-unwanted-gray-boarder-or-its-too-small-or-too-large"></a><span data-ttu-id="c066b-182">Skýrsla birtist með óæskilegum gráum ramma eða hún er of lítill eða of stór</span><span class="sxs-lookup"><span data-stu-id="c066b-182">Report appears with an unwanted gray boarder, or it's too small or too large</span></span>

<span data-ttu-id="c066b-183">Staðfestið að stærð skýrslu sé stillt á 325 x 310 pixla.</span><span class="sxs-lookup"><span data-stu-id="c066b-183">Verify that the report size is set to 325 pixels x 310 pixels.</span></span> <span data-ttu-id="c066b-184">Vista skal skýrsluna og síðan endurnýja listasíðuna.</span><span class="sxs-lookup"><span data-stu-id="c066b-184">Save the report, and then refresh the list page.</span></span>  

## <a name="see-related-training-at-microsoft-learn"></a><span data-ttu-id="c066b-185">Sjá tengda þjálfun á [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)</span><span class="sxs-lookup"><span data-stu-id="c066b-185">See Related Training at [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)</span></span>

## <a name="see-also"></a><span data-ttu-id="c066b-186">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="c066b-186">See Also</span></span>

[<span data-ttu-id="c066b-187">Gera viðskiptagögn þín virk fyrir Power BI</span><span class="sxs-lookup"><span data-stu-id="c066b-187">Enabling Your Business Data for Power BI</span></span>](admin-powerbi.md)  
<span data-ttu-id="c066b-188">[Nota [!INCLUDE[prod_short](includes/prod_short.md)] sem Power BI gagnaveitu](across-how-use-financials-data-source-powerbi.md)</span><span class="sxs-lookup"><span data-stu-id="c066b-188">[Using [!INCLUDE[prod_short](includes/prod_short.md)] as a Power BI Data Source](across-how-use-financials-data-source-powerbi.md)</span></span>  
[<span data-ttu-id="c066b-189">Undirbúðu þig fyrir að gera viðskipti</span><span class="sxs-lookup"><span data-stu-id="c066b-189">Getting Ready for Doing Business</span></span>](ui-get-ready-business.md)  
<span data-ttu-id="c066b-190">[Uppsetning [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)</span><span class="sxs-lookup"><span data-stu-id="c066b-190">[Setting Up [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)</span></span>  
[<span data-ttu-id="c066b-191">Fjármál</span><span class="sxs-lookup"><span data-stu-id="c066b-191">Finance</span></span>](finance.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]