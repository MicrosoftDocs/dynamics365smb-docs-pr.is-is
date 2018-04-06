---
title: "Hvernig á að: Tengja Power BI Finance and Operations, Business Edition | Microsoft Docs"
description: "Það er auðvelt að fá innsýn, viðskiptagreind og afkastavísi (KPI) í Finance and Operations, Business Edition gögnum með Power BI og Finance and Operations, Business Edition efnispökkunum."
author: SusanneWindfeldPedersen
ms.service: dynamics365-financials
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: account schedule, analysis, reporting, financial report, business intelligence, KPI
ms.date: 02/05/2018
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: b4e2e7bc1c2622d329c73ae5bf47b4accff10aa8
ms.openlocfilehash: aff8d95b13f795fa12d3146e5613712fb3baf9b4
ms.contentlocale: is-is
ms.lasthandoff: 03/22/2018

---
# <a name="connecting-power-bi-to-finance-and-operations-business-edition-content-packs"></a><span data-ttu-id="901e6-103">Tenging Power BI Finance and Operations, Business Edition efnispakka</span><span class="sxs-lookup"><span data-stu-id="901e6-103">Connecting Power BI to Finance and Operations, Business edition Content Packs</span></span>
<span data-ttu-id="901e6-104">Það er auðvelt að fá innsýn í Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] gögnin þín með Power BI og Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] efnispökkunum.</span><span class="sxs-lookup"><span data-stu-id="901e6-104">Getting insights into your Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] data is easy with Power BI and the Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] content packs.</span></span> <span data-ttu-id="901e6-105">Power BI sækir gögn þín og býr svo til út-fyrir-kassann yfirlit og skýrslur sem byggist á þeim gögnum.</span><span class="sxs-lookup"><span data-stu-id="901e6-105">Power BI retrieves your data then builds an out-of-the-box dashboard and reports based on that data.</span></span>

> [!NOTE]  
>  <span data-ttu-id="901e6-106">Notandi verður að vera með gildan reikning hjá Dynamics 365 og hjá Power BI.</span><span class="sxs-lookup"><span data-stu-id="901e6-106">You must have a valid account with Dynamics 365 and with Power BI.</span></span> <span data-ttu-id="901e6-107">Einnig þarf að sækja [Power BI Desktop](https://powerbi.microsoft.com/en-us/desktop/).</span><span class="sxs-lookup"><span data-stu-id="901e6-107">Also, you must download [Power BI Desktop](https://powerbi.microsoft.com/en-us/desktop/).</span></span>  
>  <span data-ttu-id="901e6-108">Power BI efnispakki þarfnast heimildar í töflur þaðan sem gögn eru sótt úr.</span><span class="sxs-lookup"><span data-stu-id="901e6-108">Power BI content packs require permissions to the tables where data is retrieved from.</span></span> <span data-ttu-id="901e6-109">Frekari upplýsingar um kröfur er að finna hér að neðan.</span><span class="sxs-lookup"><span data-stu-id="901e6-109">More details on the requirements are described below.</span></span>  

## <a name="how-to-connect"></a><span data-ttu-id="901e6-110">Hvernig á að tengjast</span><span class="sxs-lookup"><span data-stu-id="901e6-110">How to Connect</span></span>
1. <span data-ttu-id="901e6-111">Velja skal **Sækja gögn** neðst til vinstri á yfirlitssvæðinu.</span><span class="sxs-lookup"><span data-stu-id="901e6-111">Select **Get Data** at the bottom of the left navigation pane.</span></span>  
<span data-ttu-id="901e6-112">![Flett um til að sækja gögn](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-get-data.png)</span><span class="sxs-lookup"><span data-stu-id="901e6-112">![Navigating to Get Data](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-get-data.png)</span></span>
2. <span data-ttu-id="901e6-113">Í **Þjónusta** reitnum er valið **Sækja**.</span><span class="sxs-lookup"><span data-stu-id="901e6-113">In the **Services** box, select **Get**.</span></span> <span data-ttu-id="901e6-114">Þá er gluggi opnaður með **AppSource** og **Forrit fyrir Power BI forrit**.</span><span class="sxs-lookup"><span data-stu-id="901e6-114">This will open a window with the **AppSource** and **Apps for Power BI apps**.</span></span>  
<span data-ttu-id="901e6-115">![Velja efnispakka frá netþjónustum](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-online-services-get.png)</span><span class="sxs-lookup"><span data-stu-id="901e6-115">![Choose content packs from online services](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-online-services-get.png)</span></span>
3. <span data-ttu-id="901e6-116">Velja skal **Forrit** í **Forrit fyrir Power BI forrit** fliöpanum og velja svo **Microsoft Dynamics 365 for Finance and Operations** efnispakkann sem á að nota og svo **Sækja núna**.</span><span class="sxs-lookup"><span data-stu-id="901e6-116">Select **Apps** from the **Apps for Power BI apps** tab, and choose the **Microsoft Dynamics 365 for Finance and Operations** content pack that you want to use, and then select **Get it now**.</span></span>  
<span data-ttu-id="901e6-117">![Velja Dynamics 365 for Finance and Operations, Business Edition og velja Fá núna](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-dynamics365-for-financials-get-it-now.png)</span><span class="sxs-lookup"><span data-stu-id="901e6-117">![Select Dynamics 365 for Finance and Operations, Business edition and select Get it now](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-dynamics365-for-financials-get-it-now.png)</span></span>
4. <span data-ttu-id="901e6-118">Þegar kvaðning birtist skal slá inn heiti *fyrirtækisins* í [!INCLUDE[d365fin_md](includes/d365fin_long_md.md)].</span><span class="sxs-lookup"><span data-stu-id="901e6-118">When prompted, enter the name of *your company* in [!INCLUDE[d365fin_md](includes/d365fin_long_md.md)].</span></span> <span data-ttu-id="901e6-119">Þetta er ekki birtingarnafnið.</span><span class="sxs-lookup"><span data-stu-id="901e6-119">This is not the display name.</span></span>  
<span data-ttu-id="901e6-120">![Velja Dynamics 365 for Finance and Operations, Business Edition og velja Fá núna](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-connect-to-d365-finance-and-operations-crm.png)</span><span class="sxs-lookup"><span data-stu-id="901e6-120">![Select Dynamics 365 for Finance and Operations, Business edition and select Get it now](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-connect-to-d365-finance-and-operations-crm.png)</span></span>
5. <span data-ttu-id="901e6-121">Þegar tengingu hefur verið komið á er yfirliti, skýrslu og gagnamengi sjálfkrafa hlaðið í Power BI vinnusvæðið.</span><span class="sxs-lookup"><span data-stu-id="901e6-121">Once connected, a dashboard, report and dataset will automatically be loaded into your Power BI workspace.</span></span> <span data-ttu-id="901e6-122">Þegar þessu er lokið uppfærast reitirnir með gögnum af reikningnum þínum.</span><span class="sxs-lookup"><span data-stu-id="901e6-122">When completed, the tiles will update with data from your account.</span></span>
<span data-ttu-id="901e6-123">![Velja Dynamics 365 for Finance and Operations, Business Edition og velja Fá núna](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-workspace-dashboard-report-dataset.png)</span><span class="sxs-lookup"><span data-stu-id="901e6-123">![Select Dynamics 365 for Finance and Operations, Business edition  and select Get it now](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-workspace-dashboard-report-dataset.png)</span></span>

## <a name="what-now"></a><span data-ttu-id="901e6-124">Hvað núna?</span><span class="sxs-lookup"><span data-stu-id="901e6-124">What Now?</span></span>

- <span data-ttu-id="901e6-125">Prófaðu [að slá inn spurningu í reitinn Spurningar og svör](https://docs.microsoft.com/en-us/power-bi/service-q-and-a) efst á yfirlitinu.</span><span class="sxs-lookup"><span data-stu-id="901e6-125">Try [asking a question in the Q&A box](https://docs.microsoft.com/en-us/power-bi/service-q-and-a) at the top of the dashboard.</span></span>  
- <span data-ttu-id="901e6-126">[Breyta reitum](https://docs.microsoft.com/en-us/power-bi/service-dashboard-edit-tile) á yfirlitinu.</span><span class="sxs-lookup"><span data-stu-id="901e6-126">[Change the tiles](https://docs.microsoft.com/en-us/power-bi/service-dashboard-edit-tile) in the dashboard.</span></span>  
- <span data-ttu-id="901e6-127">[Velja reit](https://docs.microsoft.com/en-us/power-bi/service-dashboard-tiles) til opna undirliggjandi skýrslu.</span><span class="sxs-lookup"><span data-stu-id="901e6-127">[Select a tile](https://docs.microsoft.com/en-us/power-bi/service-dashboard-tiles) to open the underlying report.</span></span>  
- <span data-ttu-id="901e6-128">Gagnamengið verður stillt á að uppfærast daglega en hægt er að breyta uppfærsluáætluninni eða uppfæra það hvenær sem er í **Uppfæra núna**.</span><span class="sxs-lookup"><span data-stu-id="901e6-128">While your dataset will be scheduled to refreshed daily, you can change the refresh schedule or try refreshing it on demand using **Refresh Now**.</span></span>

## <a name="system-requirements"></a><span data-ttu-id="901e6-129">Kerfiskröfur</span><span class="sxs-lookup"><span data-stu-id="901e6-129">System Requirements</span></span>
<span data-ttu-id="901e6-130">Til að flytja [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] gögn í Power BI þarf notandi að hafa heimidlir á vefþjónustunni til að sækja gögnin.</span><span class="sxs-lookup"><span data-stu-id="901e6-130">To import your [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] data into Power BI, you need to have permissions to the web services used to retrieve data.</span></span> <span data-ttu-id="901e6-131">Vefþjónusta sem er áskilin fyrir hvern efnispakka inniheldur:</span><span class="sxs-lookup"><span data-stu-id="901e6-131">The web services required for each content pack include:</span></span>

<span data-ttu-id="901e6-132">**Microsoft Dynamics 365 for Finance and Operations, Business Edition - CRM**</span><span class="sxs-lookup"><span data-stu-id="901e6-132">**Microsoft Dynamics 365 for Finance and Operations, Business edition – CRM**</span></span>
- <span data-ttu-id="901e6-133">SalesOpportunities</span><span class="sxs-lookup"><span data-stu-id="901e6-133">SalesOpportunities</span></span>
- <span data-ttu-id="901e6-134">ExcelTemplateViewCompany</span><span class="sxs-lookup"><span data-stu-id="901e6-134">ExcelTemplateViewCompany</span></span>

<span data-ttu-id="901e6-135">**Microsoft Dynamics 365 for Finance and Operations, Business Edition - Sales**</span><span class="sxs-lookup"><span data-stu-id="901e6-135">**Microsoft Dynamics 365 for Finance and Operations, Business edition – Sales**</span></span>
- <span data-ttu-id="901e6-136">ItemSalesbyCustomer</span><span class="sxs-lookup"><span data-stu-id="901e6-136">ItemSalesbyCustomer</span></span>
- <span data-ttu-id="901e6-137">SalesDashboard</span><span class="sxs-lookup"><span data-stu-id="901e6-137">SalesDashboard</span></span>
- <span data-ttu-id="901e6-138">ExcelTemplateViewCompany</span><span class="sxs-lookup"><span data-stu-id="901e6-138">ExcelTemplateViewCompany</span></span>

<span data-ttu-id="901e6-139">**Microsoft Dynamics 365 for Finance and Operations, Business Edition - Finance**</span><span class="sxs-lookup"><span data-stu-id="901e6-139">**Microsoft Dynamics 365 for Finance and Operations, Business edition – Finance**</span></span>
- <span data-ttu-id="901e6-140">PowerBIFinance</span><span class="sxs-lookup"><span data-stu-id="901e6-140">PowerBIFinance</span></span>
- <span data-ttu-id="901e6-141">ExcelTemplateViewCompany</span><span class="sxs-lookup"><span data-stu-id="901e6-141">ExcelTemplateViewCompany</span></span>

<span data-ttu-id="901e6-142">**Microsoft Dynamics 365 for Finance and Operations, Business Edition - Jobs**</span><span class="sxs-lookup"><span data-stu-id="901e6-142">**Microsoft Dynamics 365 for Finance and Operations, Business edition – Jobs**</span></span>
- <span data-ttu-id="901e6-143">Verklisti</span><span class="sxs-lookup"><span data-stu-id="901e6-143">Job List</span></span>
- <span data-ttu-id="901e6-144">Áætlunarlínur verks</span><span class="sxs-lookup"><span data-stu-id="901e6-144">Job Planning Lines</span></span>
- <span data-ttu-id="901e6-145">Verkhlutalínur verks</span><span class="sxs-lookup"><span data-stu-id="901e6-145">Job Task Lines</span></span>

<span data-ttu-id="901e6-146">**Microsoft Dynamics 365 for Finance and Operations, Business Edition - Viðskiptamannalisti**</span><span class="sxs-lookup"><span data-stu-id="901e6-146">**Microsoft Dynamics 365 for Finance and Operations, Business edition – Customers List**</span></span>
- <span data-ttu-id="901e6-147">ItemSalesbyCustomer</span><span class="sxs-lookup"><span data-stu-id="901e6-147">ItemSalesbyCustomer</span></span>
- <span data-ttu-id="901e6-148">Power_BI_Item_Purchase_List</span><span class="sxs-lookup"><span data-stu-id="901e6-148">Power_BI_Item_Purchase_List</span></span>
- <span data-ttu-id="901e6-149">Power_BI_Item_Sales_List</span><span class="sxs-lookup"><span data-stu-id="901e6-149">Power_BI_Item_Sales_List</span></span>
- <span data-ttu-id="901e6-150">SalesDashboard</span><span class="sxs-lookup"><span data-stu-id="901e6-150">SalesDashboard</span></span>
- <span data-ttu-id="901e6-151">Power_BI_Customer_List</span><span class="sxs-lookup"><span data-stu-id="901e6-151">Power_BI_Customer_List</span></span>
- <span data-ttu-id="901e6-152">ExcelTemplateViewCompany</span><span class="sxs-lookup"><span data-stu-id="901e6-152">ExcelTemplateViewCompany</span></span>

<span data-ttu-id="901e6-153">**Microsoft Dynamics 365 for Finance and Operations, Business Edition - Vörulisti**</span><span class="sxs-lookup"><span data-stu-id="901e6-153">**Microsoft Dynamics 365 for Finance and Operations, Business edition – Items List**</span></span>
- <span data-ttu-id="901e6-154">ItemSalesbyCustomer</span><span class="sxs-lookup"><span data-stu-id="901e6-154">ItemSalesbyCustomer</span></span>
- <span data-ttu-id="901e6-155">Power_BI_Item_Purchase_List</span><span class="sxs-lookup"><span data-stu-id="901e6-155">Power_BI_Item_Purchase_List</span></span>
- <span data-ttu-id="901e6-156">Power_BI_Item_Sales_List</span><span class="sxs-lookup"><span data-stu-id="901e6-156">Power_BI_Item_Sales_List</span></span>
- <span data-ttu-id="901e6-157">Birgðir</span><span class="sxs-lookup"><span data-stu-id="901e6-157">Items</span></span>
- <span data-ttu-id="901e6-158">SalesDashboard</span><span class="sxs-lookup"><span data-stu-id="901e6-158">SalesDashboard</span></span>
- <span data-ttu-id="901e6-159">ExcelTemplateViewCompany</span><span class="sxs-lookup"><span data-stu-id="901e6-159">ExcelTemplateViewCompany</span></span>

<span data-ttu-id="901e6-160">**Microsoft Dynamics 365 for Finance and Operations, Business Edition - Lánardrottnalisti**</span><span class="sxs-lookup"><span data-stu-id="901e6-160">**Microsoft Dynamics 365 for Finance and Operations, Business edition – Vendors List**</span></span>
- <span data-ttu-id="901e6-161">ItemSalesbyCustomer</span><span class="sxs-lookup"><span data-stu-id="901e6-161">ItemSalesbyCustomer</span></span>
- <span data-ttu-id="901e6-162">Power_BI_Item_Purchase_List</span><span class="sxs-lookup"><span data-stu-id="901e6-162">Power_BI_Item_Purchase_List</span></span>
- <span data-ttu-id="901e6-163">Power_BI_Item_Sales_List</span><span class="sxs-lookup"><span data-stu-id="901e6-163">Power_BI_Item_Sales_List</span></span>
- <span data-ttu-id="901e6-164">Birgðir</span><span class="sxs-lookup"><span data-stu-id="901e6-164">Items</span></span>
- <span data-ttu-id="901e6-165">SalesDashboard</span><span class="sxs-lookup"><span data-stu-id="901e6-165">SalesDashboard</span></span>
- <span data-ttu-id="901e6-166">Power_BI_Customer_List</span><span class="sxs-lookup"><span data-stu-id="901e6-166">Power_BI_Customer_List</span></span>
- <span data-ttu-id="901e6-167">ItemSalesbyCustomer</span><span class="sxs-lookup"><span data-stu-id="901e6-167">ItemSalesbyCustomer</span></span>
- <span data-ttu-id="901e6-168">Power_BI_Vendor_List</span><span class="sxs-lookup"><span data-stu-id="901e6-168">Power_BI_Vendor_List</span></span>
- <span data-ttu-id="901e6-169">ExcelTemplateViewCompany</span><span class="sxs-lookup"><span data-stu-id="901e6-169">ExcelTemplateViewCompany</span></span>

## <a name="web-services"></a><span data-ttu-id="901e6-170">Vefþjónusta</span><span class="sxs-lookup"><span data-stu-id="901e6-170">Web Services</span></span>
<span data-ttu-id="901e6-171">Auðveld leið til að finna vefþjónustu er að leita að vefþjónustu í [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)].</span><span class="sxs-lookup"><span data-stu-id="901e6-171">An easy way to find the web services is to search for web services in [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)].</span></span> <span data-ttu-id="901e6-172">Í listanum skal ganga úr skugga um að reiturinn Birta sé valinn fyrir vefþjónustuna sem finna má að ofan.</span><span class="sxs-lookup"><span data-stu-id="901e6-172">In the list make sure the Publish box is marked for the web services listed above.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="901e6-173">Úrræðaleit</span><span class="sxs-lookup"><span data-stu-id="901e6-173">Troubleshooting</span></span>
<span data-ttu-id="901e6-174">Power BI yfirlitið byggir á birtum vefþjónustum sem eru hér að ofan skráðar, og það mun sýna gögn sýnifyrirtæki eða eigin fyrirtæki þitt ef þú flytja inn gögn úr núverandi fjárhagslausnum þínum.</span><span class="sxs-lookup"><span data-stu-id="901e6-174">The Power BI dashboard relies on the published web services that are listed above, and it will show data from the demonstration company or your own company if you import data from your current finance solution.</span></span> <span data-ttu-id="901e6-175">Hins vegar, ef eitthvað fer úrskeiðis, þessi kafli gefur lausn fyrir dæmigerður vandamál.</span><span class="sxs-lookup"><span data-stu-id="901e6-175">However, if something goes wrong, this section provides a workaround for the most typical issues.</span></span>

### <a name="incorrect-company-name"></a><span data-ttu-id="901e6-176">Rangt fyrirtækjaheiti</span><span class="sxs-lookup"><span data-stu-id="901e6-176">Incorrect Company Name</span></span>  
<span data-ttu-id="901e6-177">Algeng mistök eru að slá inn birtingarnafn fyrirtækis í stað nafn fyrirtækis.</span><span class="sxs-lookup"><span data-stu-id="901e6-177">A common mistake is to enter the company display name instead of the company name.</span></span> <span data-ttu-id="901e6-178">Til að finna nafn fyrirtækisins skal leita að **Fyrirtæki**.</span><span class="sxs-lookup"><span data-stu-id="901e6-178">To find the company name search for **Companies**.</span></span> <span data-ttu-id="901e6-179">Svo skal nota reitinn **Nafn** þegar nafn fyrirtækisins er slegið inn.</span><span class="sxs-lookup"><span data-stu-id="901e6-179">Then use the **Name** field when entering your company name.</span></span>

### <a name="incorrect-user-name-and-password"></a><span data-ttu-id="901e6-180">Rangt notandanafn og aðgangsorð</span><span class="sxs-lookup"><span data-stu-id="901e6-180">Incorrect User Name and Password</span></span>  
<span data-ttu-id="901e6-181">Notandanafn og aðgangsorð sem er notað til að tengjast verður það sama og er notað í Microsoft Office 365 reikningnum.</span><span class="sxs-lookup"><span data-stu-id="901e6-181">The user name and password used to connect will be the same as what is used to connect to your Microsoft Office 365 account.</span></span>  

<span data-ttu-id="901e6-182">Efnispakkinn krefst þess einnig að Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] reikningur sé til staðar.</span><span class="sxs-lookup"><span data-stu-id="901e6-182">The content packs also require that you have a Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] account.</span></span> <span data-ttu-id="901e6-183">Þegar upplýsingarnar hafa verið skráðar inn verða sjálfkrafa borin kennsl á alla Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] leigjendur sem notandinn hefur aðgang að.</span><span class="sxs-lookup"><span data-stu-id="901e6-183">Once you enter your credentials, we will auto discover any Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] tenants you have access to.</span></span> <span data-ttu-id="901e6-184">Ef notandinn hefur ekki leyfi eða prufuútgáfu að Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] reikningi munu villuboð birtast.</span><span class="sxs-lookup"><span data-stu-id="901e6-184">If you do not have a licensed or trial Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] account, you will receive an error message.</span></span>

### <a name="the-key-didnt-match-any-rows-in-the-table"></a><span data-ttu-id="901e6-185">Lykillinn passaði ekki við neinar línur í töflunni</span><span class="sxs-lookup"><span data-stu-id="901e6-185">The Key Didn't Match Any Rows in the Table</span></span>
<span data-ttu-id="901e6-186">Ef þú slærð inn ógilt nafn fyrirtækis meðan á tengingarferlinu stendur geturðu fengið villuboðið "Lykillinn passaði ekki við neinar raðir í töflunni".</span><span class="sxs-lookup"><span data-stu-id="901e6-186">If you enter a non valid company name during the connection process, you may get the error message "The key didn't match any rows in the table".</span></span> <span data-ttu-id="901e6-187">Gefðu upp rétt nafn fyrirtækis og reyndu að tengjast aftur.</span><span class="sxs-lookup"><span data-stu-id="901e6-187">Provide the correct company name and try connecting again.</span></span>

## <a name="see-also"></a><span data-ttu-id="901e6-188">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="901e6-188">See Also</span></span>
[<span data-ttu-id="901e6-189">Hafist handa með Power BI</span><span class="sxs-lookup"><span data-stu-id="901e6-189">Get started with Power BI</span></span>](https://docs.microsoft.com/en-us/power-bi/service-get-started)  
<span data-ttu-id="901e6-190">[Power BI - Grunnatriði](https://docs.microsoft.com/en-us/power-bi/service-basic-concepts)
[Viðskiptagreind](bi.md)</span><span class="sxs-lookup"><span data-stu-id="901e6-190">[Power BI - Basic Concepts](https://docs.microsoft.com/en-us/power-bi/service-basic-concepts)
[Business Intelligence](bi.md)</span></span>  
<span data-ttu-id="901e6-191">[Velkomin(n) í [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)</span><span class="sxs-lookup"><span data-stu-id="901e6-191">[Welcome to [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)</span></span>  
[<span data-ttu-id="901e6-192">Innflutningur viðskiptagagna úr öðrum fjárhagskerfum</span><span class="sxs-lookup"><span data-stu-id="901e6-192">Importing Business Data from Other Finance Systems</span></span>](upload-data.md)  
<span data-ttu-id="901e6-193">[Uppsetning [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span><span class="sxs-lookup"><span data-stu-id="901e6-193">[Setting Up [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span></span>  
[<span data-ttu-id="901e6-194">Fjármál</span><span class="sxs-lookup"><span data-stu-id="901e6-194">Finance</span></span>](finance.md)  
<span data-ttu-id="901e6-195">[Uppsetning skýrslugerðar fyrir [!INCLUDE[d365fin](includes/d365fin_md.md)] í Power BI](across-how-use-financials-data-source-powerbi.md)</span><span class="sxs-lookup"><span data-stu-id="901e6-195">[Setup Reporting for [!INCLUDE[d365fin](includes/d365fin_md.md)] in Power BI](across-how-use-financials-data-source-powerbi.md)</span></span>  

