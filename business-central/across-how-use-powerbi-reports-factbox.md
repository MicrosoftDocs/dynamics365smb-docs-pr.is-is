---
title: Birta sérstillta Power BI-skýrslur fyrir Business Central Data| Microsoft docs
description: Hægt er að nota Power BI skýrslur til að öðlast frekari innsýn í gögnum í listum.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: business intelligence, KPI, Odata, Power App, SOAP, analysis
ms.date: 04/01/2020
ms.author: jswymer
ms.openlocfilehash: 5d3acaf05952a61845eb8bb72b2556f2e54f8208
ms.sourcegitcommit: aeaa0dc64e54432a70c4b0e1faf325cd17d01389
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/17/2020
ms.locfileid: "3697699"
---
# <a name="creating-power-bi-reports-for-displaying-list-data-in-prodshort"></a><span data-ttu-id="b5aa7-103">Býr til Power BI skýrslur til að birta listagögn í [!INCLUDE[prodshort](includes/prodshort.md)]</span><span class="sxs-lookup"><span data-stu-id="b5aa7-103">Creating Power BI Reports for Displaying List Data in [!INCLUDE[prodshort](includes/prodshort.md)]</span></span>

[!INCLUDE[prodlong](includes/prodlong.md)] <span data-ttu-id="b5aa7-104">inniheldur stjórneiningu fyrir upplýsingakassa á mörgum veigamiklum listasíðum sem veita frekari innsýn í gögnin í listanum.</span><span class="sxs-lookup"><span data-stu-id="b5aa7-104">includes a FactBox control element on a number of key list pages that provide additional insight into the data in the list.</span></span> <span data-ttu-id="b5aa7-105">Þegar farið er milli lína í listanum er skýrslan uppfærð og síuð fyrir valda færslu.</span><span class="sxs-lookup"><span data-stu-id="b5aa7-105">As you move between rows in the list, the report is updated and filtered for the selected entry.</span></span> <span data-ttu-id="b5aa7-106">Hægt er að búa til sérsniðnar skýrslur til að birta í þessari stjórnun.</span><span class="sxs-lookup"><span data-stu-id="b5aa7-106">You can create custom reports to display in this control.</span></span> <span data-ttu-id="b5aa7-107">Hins vegar eru fáar reglur til staðar til að tryggja að skýrslur virki eins og til er ætlast.</span><span class="sxs-lookup"><span data-stu-id="b5aa7-107">However, there are a few rules to follow to ensure that reports work as expected.</span></span>  

## <a name="prerequisites"></a><span data-ttu-id="b5aa7-108">Frumskilyrði</span><span class="sxs-lookup"><span data-stu-id="b5aa7-108">Prerequisites</span></span>

- <span data-ttu-id="b5aa7-109">Power BI-Reikningur.</span><span class="sxs-lookup"><span data-stu-id="b5aa7-109">A Power BI account.</span></span>
- <span data-ttu-id="b5aa7-110">Power BI Desktop.</span><span class="sxs-lookup"><span data-stu-id="b5aa7-110">Power BI Desktop.</span></span>

<span data-ttu-id="b5aa7-111">Frekari upplýsingar um það hvernig þú hefst handa má finna í [Nota [!INCLUDE[d365fin](includes/d365fin_md.md)] sem Power BI gagnaveitu](across-how-use-financials-data-source-powerbi.md).</span><span class="sxs-lookup"><span data-stu-id="b5aa7-111">For more information about getting started, see [Using [!INCLUDE[d365fin](includes/d365fin_md.md)] as a Power BI Data Source](across-how-use-financials-data-source-powerbi.md).</span></span>

## <a name="defining-the-report-data-set"></a><span data-ttu-id="b5aa7-112">Skilgreining gagnasamstæðu skýrslu</span><span class="sxs-lookup"><span data-stu-id="b5aa7-112">Defining the report data set</span></span>

<span data-ttu-id="b5aa7-113">Tilgreina gagnagjafann sem inniheldur gögnin sem tengjast listanum.</span><span class="sxs-lookup"><span data-stu-id="b5aa7-113">Specify the data source that contains the data related to the list.</span></span> <span data-ttu-id="b5aa7-114">Ef þú vilt t.d. stofna skýrslu fyrir sölulista skal tryggja að gagnamengið innihaldi upplýsingar sem tengjast sölu.</span><span class="sxs-lookup"><span data-stu-id="b5aa7-114">For example, to create a report for the Sales List, ensure the data set contains information related to sales.</span></span>  

## <a name="defining-the-report-filter"></a><span data-ttu-id="b5aa7-115">Skilgreining á afmörkun skýrslu</span><span class="sxs-lookup"><span data-stu-id="b5aa7-115">Defining the report filter</span></span>

<span data-ttu-id="b5aa7-116">Til að gera gagnauppfærslu í valinni færslu á listanum er síu bætt við skýrslu.</span><span class="sxs-lookup"><span data-stu-id="b5aa7-116">To make the data update to the selected record in the list, you add a filter to the report.</span></span> <span data-ttu-id="b5aa7-117">Sían verður að innihalda reit gagnagjafans sem er notaður sem *aðallykill*.</span><span class="sxs-lookup"><span data-stu-id="b5aa7-117">The filter must include a field of the data source that's used as the *primary key*.</span></span> <span data-ttu-id="b5aa7-118">Í flestum tilvikum er aðallykill fyrir lista reiturinn **Nr.**</span><span class="sxs-lookup"><span data-stu-id="b5aa7-118">In most cases, the primary key for a list is the **No.**</span></span> <span data-ttu-id="b5aa7-119">.</span><span class="sxs-lookup"><span data-stu-id="b5aa7-119">field.</span></span>

<span data-ttu-id="b5aa7-120">Til að skilgreina afmörkun í skýrslunni er aðallykill af listanum yfir tiltæki reitir valinn og síðan er sá reitur dregill og sleppt yfir í hlutann **Afmörkun skýrslu**.</span><span class="sxs-lookup"><span data-stu-id="b5aa7-120">To define a filter for the report, select the primary key from the list of available fields, and then drag and drop that field into the **Report Filter** section.</span></span> <span data-ttu-id="b5aa7-121">Sían verður að vera grunnskýrslusía.</span><span class="sxs-lookup"><span data-stu-id="b5aa7-121">The filter must be basic report filter.</span></span> <span data-ttu-id="b5aa7-122">Það getur ekki verið síða, sjónrænt eða ítarleg sía.</span><span class="sxs-lookup"><span data-stu-id="b5aa7-122">It can't be page, visual, or advanced filter.</span></span> 

![Afmörkun skýslu stillt fyrir Aðgerðaskráningu sölureikninga](./media/across-how-use-powerbi-reports-factbox/financials-powerbi-report-filter.png)

## <a name="setting-the-report-size-and-color"></a><span data-ttu-id="b5aa7-124">Stærð og litur skýrslu valin</span><span class="sxs-lookup"><span data-stu-id="b5aa7-124">Setting the report size and color</span></span>

<span data-ttu-id="b5aa7-125">Stærð skýrslu verður að stilla á 325 sinnum 310 pixla.</span><span class="sxs-lookup"><span data-stu-id="b5aa7-125">The size of the report must be set to 325 pixels by 310 pixels.</span></span> <span data-ttu-id="b5aa7-126">Þessi stærð býður upp á rétta kvörðun á skýrslu í tiltæku bili í Power BI stjórnun upplýsingareits í [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="b5aa7-126">This size provides the proper scaling of the report in the available space of the Power BI FactBox control in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="b5aa7-127">Til að skilgreina stærð skýrslu skal staðsetja fókus utan svæðis fyrir útlit skýrslu og velja svo tákn fyrir málningarrúllu.</span><span class="sxs-lookup"><span data-stu-id="b5aa7-127">To define the size of the report, place focus outside of the report layout area, and then choose the paint roller icon.</span></span>

![Breidd og hæð skýrslu stillt fyrir Aðgerðaskráningu sölureikninga](./media/across-how-use-powerbi-reports-factbox/financials-powerbi-report-sizing.png)

<span data-ttu-id="b5aa7-129">Hægt er að breyta breidd og hæð skýrslunnar með því að velja **Sérsníða** í reitnum **Tegund**.</span><span class="sxs-lookup"><span data-stu-id="b5aa7-129">You can change the width and height of the report by choosing **Custom** in the **Type** field.</span></span>

<span data-ttu-id="b5aa7-130">Ef bakgrunnur skýringarinnar á að vera með bakgrunnslit Power BI upplýsingareitsins skal stilla bakgrunnslit skýrslu á *#FFFFFF*.</span><span class="sxs-lookup"><span data-stu-id="b5aa7-130">If you want the background of the report to blend with the background color of the Power BI FactBox control, set report background color to *#FFFFFF*.</span></span> 

## <a name="using-reports-with-multiple-pages"></a><span data-ttu-id="b5aa7-131">Notkun á skýrslum með mörgum síðum</span><span class="sxs-lookup"><span data-stu-id="b5aa7-131">Using reports with multiple pages</span></span>

<span data-ttu-id="b5aa7-132">Með Power BI er hægt að stofna eina skýrslu með mörgum síðum.</span><span class="sxs-lookup"><span data-stu-id="b5aa7-132">With Power BI, you can create a single report with multiple pages.</span></span> <span data-ttu-id="b5aa7-133">Fyrir skýrslur sem birtast með listasíðum mælum við hins vegar ekki með því að þær séu með fleiri en eina síðu.</span><span class="sxs-lookup"><span data-stu-id="b5aa7-133">However, for reports that will display with list pages, we don't recommend that they have more than one page.</span></span> <span data-ttu-id="b5aa7-134">Power BI upplýsingareiturinn sýnir aðeins fyrstu síðu skýrslunnar.</span><span class="sxs-lookup"><span data-stu-id="b5aa7-134">The Power BI FactBox will only show the first page of your report.</span></span>

## <a name="naming-the-report"></a><span data-ttu-id="b5aa7-135">Gefa skýrslunni heiti</span><span class="sxs-lookup"><span data-stu-id="b5aa7-135">Naming the report</span></span>

<span data-ttu-id="b5aa7-136">Gefa skal skýrslunni heiti sem inniheldur heiti listasíðunnar sem tengist skýrslunni.</span><span class="sxs-lookup"><span data-stu-id="b5aa7-136">Give the report a name that contains the name of the list page associated with the report.</span></span> <span data-ttu-id="b5aa7-137">Ef skýrsla er t.d. fyrir listasíðuna **Lánardrottinn** skal innihalda orðið *lánardrottinn* einhvers staðar í heitinu.</span><span class="sxs-lookup"><span data-stu-id="b5aa7-137">For example, if the report is for the **Vendor** list page, include the word *vendor* somewhere in the name.</span></span>  

<span data-ttu-id="b5aa7-138">Þessi nafnavenja er ekki skilyrði.</span><span class="sxs-lookup"><span data-stu-id="b5aa7-138">This naming convention isn't a requirement.</span></span> <span data-ttu-id="b5aa7-139">Hins vegar gerir það val á skýrslum í [!INCLUDE[d365fin](includes/d365fin_md.md)] fljótlegri.</span><span class="sxs-lookup"><span data-stu-id="b5aa7-139">However, it makes selecting reports in [!INCLUDE[d365fin](includes/d365fin_md.md)] quicker.</span></span> <span data-ttu-id="b5aa7-140">Þegar skýrsluvalssíða opnast af listasíðu er hún síuð sjálfkrafa út frá síðuheitinu.</span><span class="sxs-lookup"><span data-stu-id="b5aa7-140">When the report selection page opens from a list page, it's automatically filtered based on the page name.</span></span> <span data-ttu-id="b5aa7-141">Þessi sía er búin til að takmarka skýrslurnar sem eru birtar.</span><span class="sxs-lookup"><span data-stu-id="b5aa7-141">This filtering is done to limit the reports that are displayed.</span></span> <span data-ttu-id="b5aa7-142">Einnig er hægt að fjarlægja afmörkunina til að birta heildarlista yfir skýrslur sem eru tiltækar í Power BI.</span><span class="sxs-lookup"><span data-stu-id="b5aa7-142">Users can clear the filter to get a full list of reports available in Power BI.</span></span>  

## <a name="fixing-problems"></a><span data-ttu-id="b5aa7-143">Vandamál lagfærð</span><span class="sxs-lookup"><span data-stu-id="b5aa7-143">Fixing problems</span></span>

<span data-ttu-id="b5aa7-144">Þessi hluti veitir hjáleið fyrir flest dæmigerð vandamál sem komið geta upp þegar Power BI-skýrsla er búin til.</span><span class="sxs-lookup"><span data-stu-id="b5aa7-144">This section provides a workaround for the most typical problems that can occur when you create the Power BI report.</span></span>  

#### <a name="you-cant-see-a-report-on-the-select-report-page"></a><span data-ttu-id="b5aa7-145">Ekki er hægt að sjá skýrslur á síðunni „Velja skýrslur“</span><span class="sxs-lookup"><span data-stu-id="b5aa7-145">You can't see a report on the Select Report page</span></span>

<span data-ttu-id="b5aa7-146">Það er líklega vegna þess að heiti skýrslunnar inniheldur ekki heiti listasíðunnar.</span><span class="sxs-lookup"><span data-stu-id="b5aa7-146">It's probably because the report's name doesn't contain the name of the list page.</span></span> <span data-ttu-id="b5aa7-147">Hreinsaðu síuna til að birta heildarlista yfir skýrslur sem eru tiltækar í Power BI.</span><span class="sxs-lookup"><span data-stu-id="b5aa7-147">Clear the filter to get a full list of Power BI reports available.</span></span>  

#### <a name="report-is-loaded-but-blank-not-filtered-or-filtered-incorrectly"></a><span data-ttu-id="b5aa7-148">Verið er að hlaða skrá en hún er tóm, ekki síuð eða síuð á rangan hátt</span><span class="sxs-lookup"><span data-stu-id="b5aa7-148">Report is loaded but blank, not filtered or filtered incorrectly</span></span>

<span data-ttu-id="b5aa7-149">Sannprófa verður að skýrsluafmörkunin innihaldi réttan aðallykil.</span><span class="sxs-lookup"><span data-stu-id="b5aa7-149">Verify that the report filter contains the right primary key.</span></span> <span data-ttu-id="b5aa7-150">Yfirleitt er þessi reitur **Nr.**</span><span class="sxs-lookup"><span data-stu-id="b5aa7-150">In most cases, this field is the **No.**</span></span> <span data-ttu-id="b5aa7-151">reitur, en í töflunni **Fjárhagsfærsla**, til dæmis, verður að nota **Færslunr.** reitinn.</span><span class="sxs-lookup"><span data-stu-id="b5aa7-151">field, but in the **G/L Entry** table, for example, you must use the **Entry No.** field.</span></span>

#### <a name="report-is-loaded-but-it-shows-a-page-you-didnt-expect"></a><span data-ttu-id="b5aa7-152">Skýrslu er hlaðið inn, en hún sýnir síðu sem þú bjóst ekki við</span><span class="sxs-lookup"><span data-stu-id="b5aa7-152">Report is loaded, but it shows a page you didn't expect</span></span>

<span data-ttu-id="b5aa7-153">Sannprófa verður að skýrslan sem notandi vill að birtist sé fyrsta síðan í skýrslunni.</span><span class="sxs-lookup"><span data-stu-id="b5aa7-153">Verify that the page you want displayed is the first page in your report.</span></span>  

#### <a name="report-appears-with-an-unwanted-gray-boarder-or-its-too-small-or-too-large"></a><span data-ttu-id="b5aa7-154">Skýrsla birtist með óæskilegum gráum ramma eða hún er of lítill eða of stór</span><span class="sxs-lookup"><span data-stu-id="b5aa7-154">Report appears with an unwanted gray boarder, or it's too small or too large</span></span>

<span data-ttu-id="b5aa7-155">Staðfestið að stærð skýrslu sé stillt á 325 x 310 pixla.</span><span class="sxs-lookup"><span data-stu-id="b5aa7-155">Verify that the report size is set to 325 pixels x 310 pixels.</span></span> <span data-ttu-id="b5aa7-156">Vista skal skýrsluna og síðan endurnýja listasíðuna.</span><span class="sxs-lookup"><span data-stu-id="b5aa7-156">Save the report, and then refresh the list page.</span></span>  

## <a name="see-related-training-at-microsoft-learn"></a><span data-ttu-id="b5aa7-157">Sjá tengda þjálfun á [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)</span><span class="sxs-lookup"><span data-stu-id="b5aa7-157">See Related Training at [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)</span></span>

## <a name="see-also"></a><span data-ttu-id="b5aa7-158">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="b5aa7-158">See Also</span></span>

[<span data-ttu-id="b5aa7-159">Gera viðskiptagögn þín virk fyrir Power BI</span><span class="sxs-lookup"><span data-stu-id="b5aa7-159">Enabling Your Business Data for Power BI</span></span>](admin-powerbi.md)  
<span data-ttu-id="b5aa7-160">[Nota [!INCLUDE[d365fin](includes/d365fin_md.md)] sem Power BI gagnaveitu](across-how-use-financials-data-source-powerbi.md)</span><span class="sxs-lookup"><span data-stu-id="b5aa7-160">[Using [!INCLUDE[d365fin](includes/d365fin_md.md)] as a Power BI Data Source](across-how-use-financials-data-source-powerbi.md)</span></span>  
[<span data-ttu-id="b5aa7-161">Hafist handa</span><span class="sxs-lookup"><span data-stu-id="b5aa7-161">Getting Started</span></span>](product-get-started.md)  
<span data-ttu-id="b5aa7-162">[Uppsetning [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span><span class="sxs-lookup"><span data-stu-id="b5aa7-162">[Setting Up [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span></span>  
[<span data-ttu-id="b5aa7-163">Fjármál</span><span class="sxs-lookup"><span data-stu-id="b5aa7-163">Finance</span></span>](finance.md)  
