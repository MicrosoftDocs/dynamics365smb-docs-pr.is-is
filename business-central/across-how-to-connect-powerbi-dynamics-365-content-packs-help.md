---
title: "Hvernig á að Tengja Power BI við Business Central | Microsoft Docs"
description: "Það er auðvelt að fá innsýn, viðskiptaupplýsingar og afkastavísi (KPI) í Business Central gögnum með Power BI og  Business Central efnispökkunum."
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: account schedule, analysis, reporting, financial report, business intelligence, KPI
ms.date: 04/03/2018
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: 9cad9c7e2b54506e60af7d38d42f413599a44d01
ms.openlocfilehash: 7b9140611a47b8b823274763731cf000258c681e
ms.contentlocale: is-is
ms.lasthandoff: 04/03/2018

---
# <a name="connecting-power-bi-to-dynamics-365-business-central-content-packs"></a><span data-ttu-id="d25cd-103">Tengja Power BI við efnispakka Dynamics 365 Business Central</span><span class="sxs-lookup"><span data-stu-id="d25cd-103">Connecting Power BI to Dynamics 365 Business Central Content Packs</span></span>
<span data-ttu-id="d25cd-104">Það er auðvelt að fá innsýn í Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] gögnin þín með Power BI og Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] efnispökkunum.</span><span class="sxs-lookup"><span data-stu-id="d25cd-104">Getting insights into your Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] data is easy with Power BI and the Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] content packs.</span></span> <span data-ttu-id="d25cd-105">Power BI sækir gögn þín og býr svo til út-fyrir-kassann yfirlit og skýrslur sem byggist á þeim gögnum.</span><span class="sxs-lookup"><span data-stu-id="d25cd-105">Power BI retrieves your data then builds an out-of-the-box dashboard and reports based on that data.</span></span>

<span data-ttu-id="d25cd-106">Notandi verður að vera með gildan reikning hjá Dynamics 365 og hjá Power BI.</span><span class="sxs-lookup"><span data-stu-id="d25cd-106">You must have a valid account with Dynamics 365 and with Power BI.</span></span> <span data-ttu-id="d25cd-107">Einnig verður að hlaða niður [Power BI Desktop](https://powerbi.microsoft.com/en-us/desktop/) ef þú vilt búa til þínar eigin Power BI skýrslur.</span><span class="sxs-lookup"><span data-stu-id="d25cd-107">Also, you must download [Power BI Desktop](https://powerbi.microsoft.com/en-us/desktop/) if you wish to create your own Power BI reports.</span></span> <span data-ttu-id="d25cd-108">Power BI efnispakki þarfnast heimildar í töflur þaðan sem gögn eru sótt úr.</span><span class="sxs-lookup"><span data-stu-id="d25cd-108">Power BI content packs require permissions to the tables where data is retrieved from.</span></span> <span data-ttu-id="d25cd-109">Frekari upplýsingar um kröfur er að finna hér að neðan.</span><span class="sxs-lookup"><span data-stu-id="d25cd-109">More details on the requirements are described below.</span></span>  

## <a name="how-to-connect"></a><span data-ttu-id="d25cd-110">Hvernig á að tengjast</span><span class="sxs-lookup"><span data-stu-id="d25cd-110">How to Connect</span></span>
1. <span data-ttu-id="d25cd-111">Velja skal **Sækja gögn** neðst til vinstri á yfirlitssvæðinu.</span><span class="sxs-lookup"><span data-stu-id="d25cd-111">Select **Get Data** at the bottom of the left navigation pane.</span></span>  
<span data-ttu-id="d25cd-112">![Flett um til að sækja gögn](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-get-data.png)</span><span class="sxs-lookup"><span data-stu-id="d25cd-112">![Navigating to Get Data](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-get-data.png)</span></span>

<span data-ttu-id="d25cd-113">Þú gætir líka komið þér af stað inn í Dynamics 365 Business Edition.</span><span class="sxs-lookup"><span data-stu-id="d25cd-113">You may also get starting from within Dynamics 365 Business Edition.</span></span> <span data-ttu-id="d25cd-114">Frá hlutverkamiðstöðinni skal fletta að **Skýrsluval** í hluta Power BI hlutverkamiðstöðvar.</span><span class="sxs-lookup"><span data-stu-id="d25cd-114">From the role center, navigate to **Report Selection** in the Power BI Role Center part.</span></span> <span data-ttu-id="d25cd-115">Veldu annað hvort **Þjónusta** eða **Mitt fyrirtæki** frá borðanum.</span><span class="sxs-lookup"><span data-stu-id="d25cd-115">Select either **Service** or **My Organization** from the ribbon.</span></span> <span data-ttu-id="d25cd-116">Þegar önnur hvor þessara aðgerða er valin verður þér vísað annað hvort á fyrirtækisgalleríð í Power BI eða þjónustusafnið í Power BI, sem einnig verður síað til að aðeins birta efnispakka sem tengjast [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)].</span><span class="sxs-lookup"><span data-stu-id="d25cd-116">When either of these actions are selected, you will be taken to either the Organization gallery in Power BI or to the services library in Power BI, which will also be filtered to only display content packs related to [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)].</span></span>

2. <span data-ttu-id="d25cd-117">Í **Þjónusta** reitnum er valið **Sækja**.</span><span class="sxs-lookup"><span data-stu-id="d25cd-117">In the **Services** box, select **Get**.</span></span> <span data-ttu-id="d25cd-118">Þá er gluggi opnaður með **AppSource** og **Forrit fyrir Power BI forrit**.</span><span class="sxs-lookup"><span data-stu-id="d25cd-118">This will open a window with the **AppSource** and **Apps for Power BI apps**.</span></span>  
<span data-ttu-id="d25cd-119">![Velja efnispakka frá netþjónustum](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-online-services-get.png)</span><span class="sxs-lookup"><span data-stu-id="d25cd-119">![Choose content packs from online services](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-online-services-get.png)</span></span>
3. <span data-ttu-id="d25cd-120">Veldu **Forrit** af flipanum **Forrit fyrir Power BI forrit**, veldu efnispakkann **Microsoft Dynamics 365 Business Central** sem þú vilt nota og veldu síðan **Fá hann núna**.</span><span class="sxs-lookup"><span data-stu-id="d25cd-120">Select **Apps** from the **Apps for Power BI apps** tab, choose the **Microsoft Dynamics 365 Business Central** content pack that you want to use, and then select **Get it now**.</span></span>  
<span data-ttu-id="d25cd-121">![Velja Dynamics 365 Business Central og velja Fá núna](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-dynamics365-for-financials-get-it-now.png)</span><span class="sxs-lookup"><span data-stu-id="d25cd-121">![Select Dynamics 365 Business Central and select Get it now](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-dynamics365-for-financials-get-it-now.png)</span></span>
4. <span data-ttu-id="d25cd-122">Þegar kvaðning birtist skal slá inn heiti *fyrirtækisins* í [!INCLUDE[d365fin_md](includes/d365fin_long_md.md)].</span><span class="sxs-lookup"><span data-stu-id="d25cd-122">When prompted, enter the name of *your company* in [!INCLUDE[d365fin_md](includes/d365fin_long_md.md)].</span></span> <span data-ttu-id="d25cd-123">Þetta er ekki birtingarnafnið.</span><span class="sxs-lookup"><span data-stu-id="d25cd-123">This is not the display name.</span></span> <span data-ttu-id="d25cd-124">Heiti fyrirtækis er hægt að finna á síðunni „Fyrirtæki“ innan þíns [!INCLUDE[d365fin_md](includes/d365fin_long_md.md)] tilviks.</span><span class="sxs-lookup"><span data-stu-id="d25cd-124">The company name can be found on the 'Companies' page within your [!INCLUDE[d365fin_md](includes/d365fin_long_md.md)] instance.</span></span> 
<span data-ttu-id="d25cd-125">![Velja Dynamics 365 Business Central og velja Fá núna](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-connect-to-d365-finance-and-operations-crm.png)</span><span class="sxs-lookup"><span data-stu-id="d25cd-125">![Select Dynamics 365 Business Central and select Get it now](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-connect-to-d365-finance-and-operations-crm.png)</span></span>
5. <span data-ttu-id="d25cd-126">Þegar tengingu hefur verið komið á er yfirliti, skýrslu og gagnamengi sjálfkrafa hlaðið í Power BI vinnusvæðið.</span><span class="sxs-lookup"><span data-stu-id="d25cd-126">Once connected, a dashboard, report and dataset will automatically be loaded into your Power BI workspace.</span></span> <span data-ttu-id="d25cd-127">Þegar því lýkur munu reitirnir uppfærast með gögnum úr [!INCLUDE[d365fin_md](includes/d365fin_long_md.md)] fyrirtækinu.</span><span class="sxs-lookup"><span data-stu-id="d25cd-127">When completed, the tiles will update with data from your [!INCLUDE[d365fin_md](includes/d365fin_long_md.md)] company.</span></span>
<span data-ttu-id="d25cd-128">![Velja Dynamics 365 Business Central og velja Fá núna](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-workspace-dashboard-report-dataset.png)</span><span class="sxs-lookup"><span data-stu-id="d25cd-128">![Select Dynamics 365 Business Central  and select Get it now](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-workspace-dashboard-report-dataset.png)</span></span>

## <a name="what-now"></a><span data-ttu-id="d25cd-129">Hvað núna?</span><span class="sxs-lookup"><span data-stu-id="d25cd-129">What Now?</span></span>

- <span data-ttu-id="d25cd-130">Prófaðu [að slá inn spurningu í reitinn Spurningar og svör](https://docs.microsoft.com/en-us/power-bi/service-q-and-a) efst á yfirlitinu.</span><span class="sxs-lookup"><span data-stu-id="d25cd-130">Try [asking a question in the Q&A box](https://docs.microsoft.com/en-us/power-bi/service-q-and-a) at the top of the dashboard.</span></span>
- <span data-ttu-id="d25cd-131">[Breyta reitum](https://docs.microsoft.com/en-us/power-bi/service-dashboard-edit-tile) á yfirlitinu.</span><span class="sxs-lookup"><span data-stu-id="d25cd-131">[Change the tiles](https://docs.microsoft.com/en-us/power-bi/service-dashboard-edit-tile) in the dashboard.</span></span>  
- <span data-ttu-id="d25cd-132">[Velja reit](https://docs.microsoft.com/en-us/power-bi/service-dashboard-tiles) til opna undirliggjandi skýrslu.</span><span class="sxs-lookup"><span data-stu-id="d25cd-132">[Select a tile](https://docs.microsoft.com/en-us/power-bi/service-dashboard-tiles) to open the underlying report.</span></span>  
- <span data-ttu-id="d25cd-133">Gagnamengið verður stillt á að uppfærast daglega en hægt er að breyta uppfærsluáætluninni eða uppfæra það hvenær sem er í **Uppfæra núna**.</span><span class="sxs-lookup"><span data-stu-id="d25cd-133">While your dataset will be scheduled to refreshed daily, you can change the refresh schedule or try refreshing it on demand using **Refresh Now**.</span></span>

## <a name="system-requirements"></a><span data-ttu-id="d25cd-134">Kerfiskröfur</span><span class="sxs-lookup"><span data-stu-id="d25cd-134">System Requirements</span></span>
<span data-ttu-id="d25cd-135">Til að flytja [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] gögn í Power BI þarf notandi að hafa heimidlir á vefþjónustunni til að sækja gögnin.</span><span class="sxs-lookup"><span data-stu-id="d25cd-135">To import your [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] data into Power BI, you need to have permissions to the web services used to retrieve data.</span></span> <span data-ttu-id="d25cd-136">Vefþjónusta sem er áskilin fyrir hvern efnispakka inniheldur:</span><span class="sxs-lookup"><span data-stu-id="d25cd-136">The web services required for each content pack include:</span></span>

## <a name="role-center-reports"></a><span data-ttu-id="d25cd-137">Skýrslur hlutverkamiðstöðvar</span><span class="sxs-lookup"><span data-stu-id="d25cd-137">Role Center Reports</span></span>

<span data-ttu-id="d25cd-138">**Microsoft Dynamics 365 Business Central – CRM**</span><span class="sxs-lookup"><span data-stu-id="d25cd-138">**Microsoft Dynamics 365 Business Central – CRM**</span></span>
- <span data-ttu-id="d25cd-139">Sölutækifæri</span><span class="sxs-lookup"><span data-stu-id="d25cd-139">Sales Opportunities</span></span>
- <span data-ttu-id="d25cd-140">Skoða fyrirtæki í Excel-sniðmáti</span><span class="sxs-lookup"><span data-stu-id="d25cd-140">Excel Template View Company</span></span>
- <span data-ttu-id="d25cd-141">Power BI-skýrslumerkimiðar</span><span class="sxs-lookup"><span data-stu-id="d25cd-141">Power BI Report Labels</span></span>

<span data-ttu-id="d25cd-142">**Microsoft Dynamics 365 Business Central – Finance**</span><span class="sxs-lookup"><span data-stu-id="d25cd-142">**Microsoft Dynamics 365 Business Central – Finance**</span></span>
- <span data-ttu-id="d25cd-143">PowerBIFinance</span><span class="sxs-lookup"><span data-stu-id="d25cd-143">PowerBIFinance</span></span>
- <span data-ttu-id="d25cd-144">Skoða fyrirtæki í Excel-sniðmáti</span><span class="sxs-lookup"><span data-stu-id="d25cd-144">Excel Template View Company</span></span>
- <span data-ttu-id="d25cd-145">Power BI-skýrslumerkimiðar</span><span class="sxs-lookup"><span data-stu-id="d25cd-145">Power BI Report Labels</span></span>

<span data-ttu-id="d25cd-146">**Microsoft Dynamics 365 Business Central – Jobs**</span><span class="sxs-lookup"><span data-stu-id="d25cd-146">**Microsoft Dynamics 365 Business Central – Jobs**</span></span>
- <span data-ttu-id="d25cd-147">Verklisti</span><span class="sxs-lookup"><span data-stu-id="d25cd-147">Job List</span></span>
- <span data-ttu-id="d25cd-148">Áætlunarlínur verks</span><span class="sxs-lookup"><span data-stu-id="d25cd-148">Job Planning Lines</span></span>
- <span data-ttu-id="d25cd-149">Verkhlutalínur verks</span><span class="sxs-lookup"><span data-stu-id="d25cd-149">Job Task Lines</span></span>
- <span data-ttu-id="d25cd-150">Power BI-skýrslumerkimiðar</span><span class="sxs-lookup"><span data-stu-id="d25cd-150">Power BI Report Labels</span></span>
- <span data-ttu-id="d25cd-151">Skoða fyrirtæki í Excel-sniðmáti</span><span class="sxs-lookup"><span data-stu-id="d25cd-151">Excel Template View Company</span></span>

<span data-ttu-id="d25cd-152">**Microsoft Dynamics 365 Business Central - Sales**</span><span class="sxs-lookup"><span data-stu-id="d25cd-152">**Microsoft Dynamics 365 Business Central - Sales**</span></span>
- <span data-ttu-id="d25cd-153">Stjórnborð sölu</span><span class="sxs-lookup"><span data-stu-id="d25cd-153">Sales Dashboard</span></span>
- <span data-ttu-id="d25cd-154">Skoða fyrirtæki í Excel-sniðmáti</span><span class="sxs-lookup"><span data-stu-id="d25cd-154">Excel Template View Company</span></span>
- <span data-ttu-id="d25cd-155">Power BI-skýrslumerkimiðar</span><span class="sxs-lookup"><span data-stu-id="d25cd-155">Power BI Report Labels</span></span>

## <a name="list-page-reports"></a><span data-ttu-id="d25cd-156">Listasíða skýrslna</span><span class="sxs-lookup"><span data-stu-id="d25cd-156">List Page Reports</span></span> 

<span data-ttu-id="d25cd-157">**Microsoft Dynamics 365 Business Central – Customers List**</span><span class="sxs-lookup"><span data-stu-id="d25cd-157">**Microsoft Dynamics 365 Business Central – Customers List**</span></span>
- <span data-ttu-id="d25cd-158">Sala vöru eftir viðskiptamönnum</span><span class="sxs-lookup"><span data-stu-id="d25cd-158">Item Sales by Customer</span></span>
- <span data-ttu-id="d25cd-159">Power BI-vöruinnkaupalisti</span><span class="sxs-lookup"><span data-stu-id="d25cd-159">Power BI Item Purchase List</span></span>
- <span data-ttu-id="d25cd-160">Listi yfir vörusölu í Power BI</span><span class="sxs-lookup"><span data-stu-id="d25cd-160">Power BI Item Sales List</span></span>
- <span data-ttu-id="d25cd-161">Stjórnborð sölu</span><span class="sxs-lookup"><span data-stu-id="d25cd-161">Sales Dashboard</span></span>
- <span data-ttu-id="d25cd-162">Power BI-viðskiptamannalisti</span><span class="sxs-lookup"><span data-stu-id="d25cd-162">Power BI Customer List</span></span>
- <span data-ttu-id="d25cd-163">ExcelTemplateViewCompany</span><span class="sxs-lookup"><span data-stu-id="d25cd-163">ExcelTemplateViewCompany</span></span>
- <span data-ttu-id="d25cd-164">Power BI-skýrslumerkimiðar</span><span class="sxs-lookup"><span data-stu-id="d25cd-164">Power BI Report Labels</span></span> 

<span data-ttu-id="d25cd-165">**Microsoft Dynamics 365 Business Central - General Ledger Entries List**</span><span class="sxs-lookup"><span data-stu-id="d25cd-165">**Microsoft Dynamics 365 Business Central - General Ledger Entries List**</span></span>
- <span data-ttu-id="d25cd-166">Listi yfir upphæð fjárhags í Power BI</span><span class="sxs-lookup"><span data-stu-id="d25cd-166">Power BI GL Amount List</span></span>
- <span data-ttu-id="d25cd-167">Upphæð fjárhagsáætlunar í Power BI</span><span class="sxs-lookup"><span data-stu-id="d25cd-167">Power BI GL Budgeted Amount</span></span>
- <span data-ttu-id="d25cd-168">ExcelTemplateViewCompany</span><span class="sxs-lookup"><span data-stu-id="d25cd-168">ExcelTemplateViewCompany</span></span>
- <span data-ttu-id="d25cd-169">Power BI-skýrslumerkimiðar</span><span class="sxs-lookup"><span data-stu-id="d25cd-169">Power BI Report Labels</span></span>

<span data-ttu-id="d25cd-170">**Microsoft Dynamics 365 Business Central – Items List**</span><span class="sxs-lookup"><span data-stu-id="d25cd-170">**Microsoft Dynamics 365 Business Central – Items List**</span></span>
- <span data-ttu-id="d25cd-171">Sala vöru eftir viðskiptamönnum</span><span class="sxs-lookup"><span data-stu-id="d25cd-171">Item Sales by Customer</span></span>
- <span data-ttu-id="d25cd-172">Power BI-vöruinnkaupalisti</span><span class="sxs-lookup"><span data-stu-id="d25cd-172">Power BI Item Purchase List</span></span>
- <span data-ttu-id="d25cd-173">Listi yfir vörusölu í Power BI</span><span class="sxs-lookup"><span data-stu-id="d25cd-173">Power BI Item Sales List</span></span>
- <span data-ttu-id="d25cd-174">Stjórnborð sölu</span><span class="sxs-lookup"><span data-stu-id="d25cd-174">Sales Dashboard</span></span>
- <span data-ttu-id="d25cd-175">ExcelTemplateViewCompany</span><span class="sxs-lookup"><span data-stu-id="d25cd-175">ExcelTemplateViewCompany</span></span>
- <span data-ttu-id="d25cd-176">Power BI-skýrslumerkimiðar</span><span class="sxs-lookup"><span data-stu-id="d25cd-176">Power BI Report Labels</span></span>

<span data-ttu-id="d25cd-177">**Microsoft Dynamics 365 Business Central – Jobs List**</span><span class="sxs-lookup"><span data-stu-id="d25cd-177">**Microsoft Dynamics 365 Business Central – Jobs List**</span></span>
- <span data-ttu-id="d25cd-178">Listi yfir verk í Power BI</span><span class="sxs-lookup"><span data-stu-id="d25cd-178">Power BI Jobs List</span></span>
- <span data-ttu-id="d25cd-179">ExcelTemplateViewCompany</span><span class="sxs-lookup"><span data-stu-id="d25cd-179">ExcelTemplateViewCompany</span></span>
- <span data-ttu-id="d25cd-180">Power BI-skýrslumerkimiðar</span><span class="sxs-lookup"><span data-stu-id="d25cd-180">Power BI Report Labels</span></span>

<span data-ttu-id="d25cd-181">**Microsoft Dynamics 365 Business Central – Purchase Invoices List**</span><span class="sxs-lookup"><span data-stu-id="d25cd-181">**Microsoft Dynamics 365 Business Central – Purchase Invoices List**</span></span>
- <span data-ttu-id="d25cd-182">Listi yfir innkaup í Power BI</span><span class="sxs-lookup"><span data-stu-id="d25cd-182">Power BI Purchase List</span></span>
- <span data-ttu-id="d25cd-183">ExcelTemplateViewCompany</span><span class="sxs-lookup"><span data-stu-id="d25cd-183">ExcelTemplateViewCompany</span></span>
- <span data-ttu-id="d25cd-184">Power BI-skýrslumerkimiðar</span><span class="sxs-lookup"><span data-stu-id="d25cd-184">Power BI Report Labels</span></span>

<span data-ttu-id="d25cd-185">**Microsoft Dynamics 365 Business Central – Sales Orders List**</span><span class="sxs-lookup"><span data-stu-id="d25cd-185">**Microsoft Dynamics 365 Business Central – Sales Orders List**</span></span>
- <span data-ttu-id="d25cd-186">Listi yfir sölu í Power BI</span><span class="sxs-lookup"><span data-stu-id="d25cd-186">Power BI Sales List</span></span>
- <span data-ttu-id="d25cd-187">ExcelTemplateViewCompany</span><span class="sxs-lookup"><span data-stu-id="d25cd-187">ExcelTemplateViewCompany</span></span>
- <span data-ttu-id="d25cd-188">Power BI-skýrslumerkimiðar</span><span class="sxs-lookup"><span data-stu-id="d25cd-188">Power BI Report Labels</span></span>


<span data-ttu-id="d25cd-189">**Microsoft Dynamics 365 Business Central – Vendors List**</span><span class="sxs-lookup"><span data-stu-id="d25cd-189">**Microsoft Dynamics 365 Business Central – Vendors List**</span></span>
- <span data-ttu-id="d25cd-190">Power BI-vöruinnkaupalisti</span><span class="sxs-lookup"><span data-stu-id="d25cd-190">Power BI Item Purchase List</span></span>
- <span data-ttu-id="d25cd-191">Listi yfir vörusölu í Power BI</span><span class="sxs-lookup"><span data-stu-id="d25cd-191">Power BI Item Sales List</span></span>
- <span data-ttu-id="d25cd-192">Power BI-lánardrottnalisti</span><span class="sxs-lookup"><span data-stu-id="d25cd-192">Power BI Vendor List</span></span>
- <span data-ttu-id="d25cd-193">ExcelTemplateViewCompany</span><span class="sxs-lookup"><span data-stu-id="d25cd-193">ExcelTemplateViewCompany</span></span>
- <span data-ttu-id="d25cd-194">Power BI-skýrslumerkimiðar</span><span class="sxs-lookup"><span data-stu-id="d25cd-194">Power BI Report Labels</span></span>

## <a name="web-services"></a><span data-ttu-id="d25cd-195">Vefþjónusta</span><span class="sxs-lookup"><span data-stu-id="d25cd-195">Web Services</span></span>
<span data-ttu-id="d25cd-196">Auðveld leið til að finna vefþjónustu er að leita að vefþjónustu í [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)].</span><span class="sxs-lookup"><span data-stu-id="d25cd-196">An easy way to find the web services is to search for web services in [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)].</span></span> <span data-ttu-id="d25cd-197">Í listanum skal ganga úr skugga um að reiturinn Birta sé valinn fyrir vefþjónustuna sem finna má að ofan.</span><span class="sxs-lookup"><span data-stu-id="d25cd-197">In the list make sure the Publish box is marked for the web services listed above.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="d25cd-198">Úrræðaleit</span><span class="sxs-lookup"><span data-stu-id="d25cd-198">Troubleshooting</span></span>
<span data-ttu-id="d25cd-199">Power BI yfirlitið byggir á birtum vefþjónustum sem eru hér að ofan skráðar, og það mun sýna gögn sýnifyrirtæki eða eigin fyrirtæki þitt ef þú flytja inn gögn úr núverandi fjárhagslausnum þínum.</span><span class="sxs-lookup"><span data-stu-id="d25cd-199">The Power BI dashboard relies on the published web services that are listed above, and it will show data from the demonstration company or your own company if you import data from your current finance solution.</span></span> <span data-ttu-id="d25cd-200">Hins vegar, ef eitthvað fer úrskeiðis, þessi kafli gefur lausn fyrir dæmigerður vandamál.</span><span class="sxs-lookup"><span data-stu-id="d25cd-200">However, if something goes wrong, this section provides a workaround for the most typical issues.</span></span>

### <a name="incorrect-company-name"></a><span data-ttu-id="d25cd-201">Rangt fyrirtækjaheiti</span><span class="sxs-lookup"><span data-stu-id="d25cd-201">Incorrect Company Name</span></span>  
<span data-ttu-id="d25cd-202">Algeng mistök eru að slá inn birtingarnafn fyrirtækis í stað nafn fyrirtækis.</span><span class="sxs-lookup"><span data-stu-id="d25cd-202">A common mistake is to enter the company display name instead of the company name.</span></span> <span data-ttu-id="d25cd-203">Til að finna nafn fyrirtækisins skal leita að **Fyrirtæki**.</span><span class="sxs-lookup"><span data-stu-id="d25cd-203">To find the company name search for **Companies**.</span></span> <span data-ttu-id="d25cd-204">Svo skal nota reitinn **Nafn** þegar nafn fyrirtækisins er slegið inn.</span><span class="sxs-lookup"><span data-stu-id="d25cd-204">Then use the **Name** field when entering your company name.</span></span>

### <a name="incorrect-user-name-and-password"></a><span data-ttu-id="d25cd-205">Rangt notandanafn og aðgangsorð</span><span class="sxs-lookup"><span data-stu-id="d25cd-205">Incorrect User Name and Password</span></span>  
<span data-ttu-id="d25cd-206">Notandanafn og aðgangsorð sem er notað til að tengjast verður það sama og er notað í Microsoft Office 365 reikningnum.</span><span class="sxs-lookup"><span data-stu-id="d25cd-206">The user name and password used to connect will be the same as what is used to connect to your Microsoft Office 365 account.</span></span>  

<span data-ttu-id="d25cd-207">Efnispakkinn krefst þess einnig að Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] reikningur sé til staðar.</span><span class="sxs-lookup"><span data-stu-id="d25cd-207">The content packs also require that you have a Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] account.</span></span> <span data-ttu-id="d25cd-208">Þegar upplýsingarnar hafa verið skráðar inn verða sjálfkrafa borin kennsl á alla Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] leigjendur sem notandinn hefur aðgang að.</span><span class="sxs-lookup"><span data-stu-id="d25cd-208">Once you enter your credentials, we will auto discover any Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] tenants you have access to.</span></span> <span data-ttu-id="d25cd-209">Ef notandinn hefur ekki leyfi eða prufuútgáfu að Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] reikningi munu villuboð birtast.</span><span class="sxs-lookup"><span data-stu-id="d25cd-209">If you do not have a licensed or trial Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] account, you will receive an error message.</span></span>

### <a name="the-key-didnt-match-any-rows-in-the-table"></a><span data-ttu-id="d25cd-210">Lykillinn passaði ekki við neinar línur í töflunni</span><span class="sxs-lookup"><span data-stu-id="d25cd-210">The Key Didn't Match Any Rows in the Table</span></span>
<span data-ttu-id="d25cd-211">Ef þú slærð inn ógilt heiti fyrirtækis meðan á tengingarferlinu stendur geturðu fengið villuskilaboðin „Lykillinn passaði ekki við neinar línur í töflunni“.</span><span class="sxs-lookup"><span data-stu-id="d25cd-211">If you enter a non-valid company name during the connection process, you may get the error message "The key didn't match any rows in the table".</span></span> <span data-ttu-id="d25cd-212">Gefðu upp rétt nafn fyrirtækis og reyndu að tengjast aftur.</span><span class="sxs-lookup"><span data-stu-id="d25cd-212">Provide the correct company name and try connecting again.</span></span>

## <a name="see-also"></a><span data-ttu-id="d25cd-213">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="d25cd-213">See Also</span></span>
[<span data-ttu-id="d25cd-214">Hafist handa með Power BI</span><span class="sxs-lookup"><span data-stu-id="d25cd-214">Get started with Power BI</span></span>](https://docs.microsoft.com/en-us/power-bi/service-get-started)  
[<span data-ttu-id="d25cd-215">Power BI - Grunnhugtök</span><span class="sxs-lookup"><span data-stu-id="d25cd-215">Power BI - Basic Concepts</span></span>](https://docs.microsoft.com/en-us/power-bi/service-basic-concepts)  
[<span data-ttu-id="d25cd-216">Viðskiptaupplýsingar</span><span class="sxs-lookup"><span data-stu-id="d25cd-216">Business Intelligence</span></span>](bi.md)  
[<span data-ttu-id="d25cd-217">Hafist handa</span><span class="sxs-lookup"><span data-stu-id="d25cd-217">Getting Started</span></span>](product-get-started.md)  
[<span data-ttu-id="d25cd-218">Innflutningur viðskiptagagna úr öðrum fjárhagskerfum</span><span class="sxs-lookup"><span data-stu-id="d25cd-218">Importing Business Data from Other Finance Systems</span></span>](upload-data.md)  
<span data-ttu-id="d25cd-219">[Uppsetning [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span><span class="sxs-lookup"><span data-stu-id="d25cd-219">[Setting Up [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span></span>  
[<span data-ttu-id="d25cd-220">Fjármál</span><span class="sxs-lookup"><span data-stu-id="d25cd-220">Finance</span></span>](finance.md)  
<span data-ttu-id="d25cd-221">[Uppsetning skýrslugerðar fyrir [!INCLUDE[d365fin](includes/d365fin_md.md)] í Power BI](across-how-use-financials-data-source-powerbi.md)</span><span class="sxs-lookup"><span data-stu-id="d25cd-221">[Setup Reporting for [!INCLUDE[d365fin](includes/d365fin_md.md)] in Power BI](across-how-use-financials-data-source-powerbi.md)</span></span>  

