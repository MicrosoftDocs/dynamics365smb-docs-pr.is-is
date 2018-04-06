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
ms.date: 03/16/2018
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 315d4b188cdd834e82676a0c5ef77272ad873eb7
ms.contentlocale: is-is
ms.lasthandoff: 03/22/2018

---
# <a name="connecting-power-bi-to-business-central-content-packs"></a><span data-ttu-id="bfbe0-103">Tengir Power BI við efnispakka Business Central</span><span class="sxs-lookup"><span data-stu-id="bfbe0-103">Connecting Power BI to Business Central Content Packs</span></span>
<span data-ttu-id="bfbe0-104">Það er auðvelt að fá innsýn í Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] gögnin þín með Power BI og Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] efnispökkunum.</span><span class="sxs-lookup"><span data-stu-id="bfbe0-104">Getting insights into your Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] data is easy with Power BI and the Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] content packs.</span></span> <span data-ttu-id="bfbe0-105">Power BI sækir gögn þín og býr svo til út-fyrir-kassann yfirlit og skýrslur sem byggist á þeim gögnum.</span><span class="sxs-lookup"><span data-stu-id="bfbe0-105">Power BI retrieves your data then builds an out-of-the-box dashboard and reports based on that data.</span></span>

> [!NOTE]  
>  <span data-ttu-id="bfbe0-106">Notandi verður að vera með gildan reikning hjá [!INCLUDE[d365fin](includes/d365fin_md.md)] og hjá Power BI.</span><span class="sxs-lookup"><span data-stu-id="bfbe0-106">You must have a valid account with [!INCLUDE[d365fin](includes/d365fin_md.md)] and with Power BI.</span></span> <span data-ttu-id="bfbe0-107">Einnig þarf að sækja [Power BI Desktop](https://powerbi.microsoft.com/en-us/desktop/).</span><span class="sxs-lookup"><span data-stu-id="bfbe0-107">Also, you must download [Power BI Desktop](https://powerbi.microsoft.com/en-us/desktop/).</span></span>  
>  <span data-ttu-id="bfbe0-108">Power BI efnispakki þarfnast heimildar í töflur þaðan sem gögn eru sótt úr.</span><span class="sxs-lookup"><span data-stu-id="bfbe0-108">Power BI content packs require permissions to the tables where data is retrieved from.</span></span> <span data-ttu-id="bfbe0-109">Frekari upplýsingar um kröfur er að finna hér að neðan.</span><span class="sxs-lookup"><span data-stu-id="bfbe0-109">More details on the requirements are described below.</span></span>  

## <a name="how-to-connect"></a><span data-ttu-id="bfbe0-110">Hvernig á að tengjast</span><span class="sxs-lookup"><span data-stu-id="bfbe0-110">How to Connect</span></span>
1. <span data-ttu-id="bfbe0-111">Velja skal **Sækja gögn** neðst til vinstri á yfirlitssvæðinu.</span><span class="sxs-lookup"><span data-stu-id="bfbe0-111">Select **Get Data** at the bottom of the left navigation pane.</span></span>  
<span data-ttu-id="bfbe0-112">![Flett um til að sækja gögn](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-get-data.png)</span><span class="sxs-lookup"><span data-stu-id="bfbe0-112">![Navigating to Get Data](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-get-data.png)</span></span>
2. <span data-ttu-id="bfbe0-113">Í **Þjónusta** reitnum er valið **Sækja**.</span><span class="sxs-lookup"><span data-stu-id="bfbe0-113">In the **Services** box, select **Get**.</span></span> <span data-ttu-id="bfbe0-114">Þá er gluggi opnaður með **AppSource** og **Forrit fyrir Power BI forrit**.</span><span class="sxs-lookup"><span data-stu-id="bfbe0-114">This will open a window with the **AppSource** and **Apps for Power BI apps**.</span></span>  
<span data-ttu-id="bfbe0-115">![Velja efnispakka frá netþjónustum](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-online-services-get.png)</span><span class="sxs-lookup"><span data-stu-id="bfbe0-115">![Choose content packs from online services](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-online-services-get.png)</span></span>
3. <span data-ttu-id="bfbe0-116">Velja skal **Forrit** í **Forrit fyrir Power BI forrit** flipanum og velja svo **Microsoft Dynamics 365 Business Central** efnispakkann sem á að nota og svo **Sækja núna**.</span><span class="sxs-lookup"><span data-stu-id="bfbe0-116">Select **Apps** from the **Apps for Power BI apps** tab, and choose the **Microsoft Dynamics 365 Business Central** content pack that you want to use, and then select **Get it now**.</span></span>  
<span data-ttu-id="bfbe0-117">![Velja Dynamics 365 Business Central og velja Fá núna](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-dynamics365-for-financials-get-it-now.png)</span><span class="sxs-lookup"><span data-stu-id="bfbe0-117">![Select Dynamics 365 Business Central and select Get it now](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-dynamics365-for-financials-get-it-now.png)</span></span>
4. <span data-ttu-id="bfbe0-118">Þegar kvaðning birtist skal slá inn heiti *fyrirtækisins* í [!INCLUDE[d365fin_md](includes/d365fin_long_md.md)].</span><span class="sxs-lookup"><span data-stu-id="bfbe0-118">When prompted, enter the name of *your company* in [!INCLUDE[d365fin_md](includes/d365fin_long_md.md)].</span></span> <span data-ttu-id="bfbe0-119">Þetta er ekki birtingarnafnið.</span><span class="sxs-lookup"><span data-stu-id="bfbe0-119">This is not the display name.</span></span>  
<span data-ttu-id="bfbe0-120">![Velja Dynamics 365 Business Central og velja Fá núna](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-connect-to-d365-finance-and-operations-crm.png)</span><span class="sxs-lookup"><span data-stu-id="bfbe0-120">![Select Dynamics 365 Business Central and select Get it now](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-connect-to-d365-finance-and-operations-crm.png)</span></span>
5. <span data-ttu-id="bfbe0-121">Þegar tengingu hefur verið komið á er yfirliti, skýrslu og gagnamengi sjálfkrafa hlaðið í Power BI vinnusvæðið.</span><span class="sxs-lookup"><span data-stu-id="bfbe0-121">Once connected, a dashboard, report and dataset will automatically be loaded into your Power BI workspace.</span></span> <span data-ttu-id="bfbe0-122">Þegar þessu er lokið uppfærast reitirnir með gögnum af reikningnum þínum.</span><span class="sxs-lookup"><span data-stu-id="bfbe0-122">When completed, the tiles will update with data from your account.</span></span>
<span data-ttu-id="bfbe0-123">![Velja Dynamics 365 Business Central og velja Fá núna](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-workspace-dashboard-report-dataset.png)</span><span class="sxs-lookup"><span data-stu-id="bfbe0-123">![Select Dynamics 365 Business Central  and select Get it now](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-workspace-dashboard-report-dataset.png)</span></span>

## <a name="what-now"></a><span data-ttu-id="bfbe0-124">Hvað núna?</span><span class="sxs-lookup"><span data-stu-id="bfbe0-124">What Now?</span></span>

- <span data-ttu-id="bfbe0-125">[Breyta reitum](https://docs.microsoft.com/en-us/power-bi/service-dashboard-edit-tile) á yfirlitinu.</span><span class="sxs-lookup"><span data-stu-id="bfbe0-125">[Change the tiles](https://docs.microsoft.com/en-us/power-bi/service-dashboard-edit-tile) in the dashboard.</span></span>  
- <span data-ttu-id="bfbe0-126">[Velja reit](https://docs.microsoft.com/en-us/power-bi/service-dashboard-tiles) til opna undirliggjandi skýrslu.</span><span class="sxs-lookup"><span data-stu-id="bfbe0-126">[Select a tile](https://docs.microsoft.com/en-us/power-bi/service-dashboard-tiles) to open the underlying report.</span></span>  
- <span data-ttu-id="bfbe0-127">Gagnamengið verður stillt á að uppfærast daglega en hægt er að breyta uppfærsluáætluninni eða uppfæra það hvenær sem er í **Uppfæra núna**.</span><span class="sxs-lookup"><span data-stu-id="bfbe0-127">While your dataset will be scheduled to refreshed daily, you can change the refresh schedule or try refreshing it on demand using **Refresh Now**.</span></span>

## <a name="system-requirements"></a><span data-ttu-id="bfbe0-128">Kerfiskröfur</span><span class="sxs-lookup"><span data-stu-id="bfbe0-128">System Requirements</span></span>
<span data-ttu-id="bfbe0-129">Til að flytja [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] gögn í Power BI þarf notandi að hafa heimidlir á vefþjónustunni til að sækja gögnin.</span><span class="sxs-lookup"><span data-stu-id="bfbe0-129">To import your [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] data into Power BI, you need to have permissions to the web services used to retrieve data.</span></span> <span data-ttu-id="bfbe0-130">Vefþjónusta sem er áskilin fyrir hvern efnispakka inniheldur:</span><span class="sxs-lookup"><span data-stu-id="bfbe0-130">The web services required for each content pack include:</span></span>

<span data-ttu-id="bfbe0-131">**Microsoft Dynamics 365 Business Central – CRM**</span><span class="sxs-lookup"><span data-stu-id="bfbe0-131">**Microsoft Dynamics 365 Business Central – CRM**</span></span>
- <span data-ttu-id="bfbe0-132">SalesOpportunities</span><span class="sxs-lookup"><span data-stu-id="bfbe0-132">SalesOpportunities</span></span>
- <span data-ttu-id="bfbe0-133">ExcelTemplateViewCompany</span><span class="sxs-lookup"><span data-stu-id="bfbe0-133">ExcelTemplateViewCompany</span></span>

<span data-ttu-id="bfbe0-134">**Microsoft Dynamics 365 Business Central – Sales**</span><span class="sxs-lookup"><span data-stu-id="bfbe0-134">**Microsoft Dynamics 365 Business Central – Sales**</span></span>
- <span data-ttu-id="bfbe0-135">ItemSalesbyCustomer</span><span class="sxs-lookup"><span data-stu-id="bfbe0-135">ItemSalesbyCustomer</span></span>
- <span data-ttu-id="bfbe0-136">SalesDashboard</span><span class="sxs-lookup"><span data-stu-id="bfbe0-136">SalesDashboard</span></span>
- <span data-ttu-id="bfbe0-137">ExcelTemplateViewCompany</span><span class="sxs-lookup"><span data-stu-id="bfbe0-137">ExcelTemplateViewCompany</span></span>

<span data-ttu-id="bfbe0-138">**Microsoft Dynamics 365 Business Central – Finance**</span><span class="sxs-lookup"><span data-stu-id="bfbe0-138">**Microsoft Dynamics 365 Business Central – Finance**</span></span>
- <span data-ttu-id="bfbe0-139">PowerBIFinance</span><span class="sxs-lookup"><span data-stu-id="bfbe0-139">PowerBIFinance</span></span>
- <span data-ttu-id="bfbe0-140">ExcelTemplateViewCompany</span><span class="sxs-lookup"><span data-stu-id="bfbe0-140">ExcelTemplateViewCompany</span></span>

<span data-ttu-id="bfbe0-141">**Microsoft Dynamics 365 Business Central – Jobs**</span><span class="sxs-lookup"><span data-stu-id="bfbe0-141">**Microsoft Dynamics 365 Business Central – Jobs**</span></span>
- <span data-ttu-id="bfbe0-142">Verklisti</span><span class="sxs-lookup"><span data-stu-id="bfbe0-142">Job List</span></span>
- <span data-ttu-id="bfbe0-143">Áætlunarlínur verks</span><span class="sxs-lookup"><span data-stu-id="bfbe0-143">Job Planning Lines</span></span>
- <span data-ttu-id="bfbe0-144">Verkhlutalínur verks</span><span class="sxs-lookup"><span data-stu-id="bfbe0-144">Job Task Lines</span></span>

<span data-ttu-id="bfbe0-145">**Microsoft Dynamics 365 Business Central - Viðskiptamannalisti**</span><span class="sxs-lookup"><span data-stu-id="bfbe0-145">**Microsoft Dynamics 365 Business Central – Customers List**</span></span>
- <span data-ttu-id="bfbe0-146">ItemSalesbyCustomer</span><span class="sxs-lookup"><span data-stu-id="bfbe0-146">ItemSalesbyCustomer</span></span>
- <span data-ttu-id="bfbe0-147">Power_BI_Item_Purchase_List</span><span class="sxs-lookup"><span data-stu-id="bfbe0-147">Power_BI_Item_Purchase_List</span></span>
- <span data-ttu-id="bfbe0-148">Power_BI_Item_Sales_List</span><span class="sxs-lookup"><span data-stu-id="bfbe0-148">Power_BI_Item_Sales_List</span></span>
- <span data-ttu-id="bfbe0-149">SalesDashboard</span><span class="sxs-lookup"><span data-stu-id="bfbe0-149">SalesDashboard</span></span>
- <span data-ttu-id="bfbe0-150">Power_BI_Customer_List</span><span class="sxs-lookup"><span data-stu-id="bfbe0-150">Power_BI_Customer_List</span></span>
- <span data-ttu-id="bfbe0-151">ExcelTemplateViewCompany</span><span class="sxs-lookup"><span data-stu-id="bfbe0-151">ExcelTemplateViewCompany</span></span>

<span data-ttu-id="bfbe0-152">**Microsoft Dynamics 365 Business Central - Vörulisti**</span><span class="sxs-lookup"><span data-stu-id="bfbe0-152">**Microsoft Dynamics 365 Business Central – Items List**</span></span>
- <span data-ttu-id="bfbe0-153">ItemSalesbyCustomer</span><span class="sxs-lookup"><span data-stu-id="bfbe0-153">ItemSalesbyCustomer</span></span>
- <span data-ttu-id="bfbe0-154">Power_BI_Item_Purchase_List</span><span class="sxs-lookup"><span data-stu-id="bfbe0-154">Power_BI_Item_Purchase_List</span></span>
- <span data-ttu-id="bfbe0-155">Power_BI_Item_Sales_List</span><span class="sxs-lookup"><span data-stu-id="bfbe0-155">Power_BI_Item_Sales_List</span></span>
- <span data-ttu-id="bfbe0-156">Birgðir</span><span class="sxs-lookup"><span data-stu-id="bfbe0-156">Items</span></span>
- <span data-ttu-id="bfbe0-157">SalesDashboard</span><span class="sxs-lookup"><span data-stu-id="bfbe0-157">SalesDashboard</span></span>
- <span data-ttu-id="bfbe0-158">ExcelTemplateViewCompany</span><span class="sxs-lookup"><span data-stu-id="bfbe0-158">ExcelTemplateViewCompany</span></span>

<span data-ttu-id="bfbe0-159">**Microsoft Dynamics 365 Business Central – lánardrottnar**</span><span class="sxs-lookup"><span data-stu-id="bfbe0-159">**Microsoft Dynamics 365 Business Central – Vendors List**</span></span>
- <span data-ttu-id="bfbe0-160">ItemSalesbyCustomer</span><span class="sxs-lookup"><span data-stu-id="bfbe0-160">ItemSalesbyCustomer</span></span>
- <span data-ttu-id="bfbe0-161">Power_BI_Item_Purchase_List</span><span class="sxs-lookup"><span data-stu-id="bfbe0-161">Power_BI_Item_Purchase_List</span></span>
- <span data-ttu-id="bfbe0-162">Power_BI_Item_Sales_List</span><span class="sxs-lookup"><span data-stu-id="bfbe0-162">Power_BI_Item_Sales_List</span></span>
- <span data-ttu-id="bfbe0-163">Birgðir</span><span class="sxs-lookup"><span data-stu-id="bfbe0-163">Items</span></span>
- <span data-ttu-id="bfbe0-164">SalesDashboard</span><span class="sxs-lookup"><span data-stu-id="bfbe0-164">SalesDashboard</span></span>
- <span data-ttu-id="bfbe0-165">Power_BI_Customer_List</span><span class="sxs-lookup"><span data-stu-id="bfbe0-165">Power_BI_Customer_List</span></span>
- <span data-ttu-id="bfbe0-166">ItemSalesbyCustomer</span><span class="sxs-lookup"><span data-stu-id="bfbe0-166">ItemSalesbyCustomer</span></span>
- <span data-ttu-id="bfbe0-167">Power_BI_Vendor_List</span><span class="sxs-lookup"><span data-stu-id="bfbe0-167">Power_BI_Vendor_List</span></span>
- <span data-ttu-id="bfbe0-168">ExcelTemplateViewCompany</span><span class="sxs-lookup"><span data-stu-id="bfbe0-168">ExcelTemplateViewCompany</span></span>

## <a name="web-services"></a><span data-ttu-id="bfbe0-169">Vefþjónusta</span><span class="sxs-lookup"><span data-stu-id="bfbe0-169">Web Services</span></span>
<span data-ttu-id="bfbe0-170">Auðveld leið til að finna vefþjónustu er að leita að vefþjónustu í [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)].</span><span class="sxs-lookup"><span data-stu-id="bfbe0-170">An easy way to find the web services is to search for web services in [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)].</span></span> <span data-ttu-id="bfbe0-171">Í listanum skal ganga úr skugga um að reiturinn Birta sé valinn fyrir vefþjónustuna sem finna má að ofan.</span><span class="sxs-lookup"><span data-stu-id="bfbe0-171">In the list make sure the Publish box is marked for the web services listed above.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="bfbe0-172">Úrræðaleit</span><span class="sxs-lookup"><span data-stu-id="bfbe0-172">Troubleshooting</span></span>
<span data-ttu-id="bfbe0-173">Power BI yfirlitið byggir á birtum vefþjónustum sem eru hér að ofan skráðar, og það mun sýna gögn sýnifyrirtæki eða eigin fyrirtæki þitt ef þú flytja inn gögn úr núverandi fjárhagslausnum þínum.</span><span class="sxs-lookup"><span data-stu-id="bfbe0-173">The Power BI dashboard relies on the published web services that are listed above, and it will show data from the demonstration company or your own company if you import data from your current finance solution.</span></span> <span data-ttu-id="bfbe0-174">Hins vegar, ef eitthvað fer úrskeiðis, þessi kafli gefur lausn fyrir dæmigerður vandamál.</span><span class="sxs-lookup"><span data-stu-id="bfbe0-174">However, if something goes wrong, this section provides a workaround for the most typical issues.</span></span>

### <a name="incorrect-company-name"></a><span data-ttu-id="bfbe0-175">Rangt fyrirtækjaheiti</span><span class="sxs-lookup"><span data-stu-id="bfbe0-175">Incorrect Company Name</span></span>  
<span data-ttu-id="bfbe0-176">Algeng mistök eru að slá inn birtingarnafn fyrirtækis í stað nafn fyrirtækis.</span><span class="sxs-lookup"><span data-stu-id="bfbe0-176">A common mistake is to enter the company display name instead of the company name.</span></span> <span data-ttu-id="bfbe0-177">Til að finna nafn fyrirtækisins skal leita að **Fyrirtæki**.</span><span class="sxs-lookup"><span data-stu-id="bfbe0-177">To find the company name search for **Companies**.</span></span> <span data-ttu-id="bfbe0-178">Svo skal nota reitinn **Nafn** þegar nafn fyrirtækisins er slegið inn.</span><span class="sxs-lookup"><span data-stu-id="bfbe0-178">Then use the **Name** field when entering your company name.</span></span>

### <a name="incorrect-user-name-and-password"></a><span data-ttu-id="bfbe0-179">Rangt notandanafn og aðgangsorð</span><span class="sxs-lookup"><span data-stu-id="bfbe0-179">Incorrect User Name and Password</span></span>  
<span data-ttu-id="bfbe0-180">Notandanafn og aðgangsorð sem er notað til að tengjast verður það sama og er notað í Microsoft Office 365 reikningnum.</span><span class="sxs-lookup"><span data-stu-id="bfbe0-180">The user name and password used to connect will be the same as what is used to connect to your Microsoft Office 365 account.</span></span>  

<span data-ttu-id="bfbe0-181">Efnispakkinn krefst þess einnig að Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] reikningur sé til staðar.</span><span class="sxs-lookup"><span data-stu-id="bfbe0-181">The content packs also require that you have a Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] account.</span></span> <span data-ttu-id="bfbe0-182">Þegar upplýsingarnar hafa verið skráðar inn verða sjálfkrafa borin kennsl á alla Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] leigjendur sem notandinn hefur aðgang að.</span><span class="sxs-lookup"><span data-stu-id="bfbe0-182">Once you enter your credentials, we will auto discover any Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] tenants you have access to.</span></span> <span data-ttu-id="bfbe0-183">Ef notandinn hefur ekki leyfi eða prufuútgáfu að Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] reikningi munu villuboð birtast.</span><span class="sxs-lookup"><span data-stu-id="bfbe0-183">If you do not have a licensed or trial Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] account, you will receive an error message.</span></span>

### <a name="the-key-didnt-match-any-rows-in-the-table"></a><span data-ttu-id="bfbe0-184">Lykillinn passaði ekki við neinar línur í töflunni</span><span class="sxs-lookup"><span data-stu-id="bfbe0-184">The Key Didn't Match Any Rows in the Table</span></span>
<span data-ttu-id="bfbe0-185">Ef þú slærð inn ógilt nafn fyrirtækis meðan á tengingarferlinu stendur geturðu fengið villuboðið "Lykillinn passaði ekki við neinar raðir í töflunni".</span><span class="sxs-lookup"><span data-stu-id="bfbe0-185">If you enter a non valid company name during the connection process, you may get the error message "The key didn't match any rows in the table".</span></span> <span data-ttu-id="bfbe0-186">Gefðu upp rétt nafn fyrirtækis og reyndu að tengjast aftur.</span><span class="sxs-lookup"><span data-stu-id="bfbe0-186">Provide the correct company name and try connecting again.</span></span>

## <a name="see-also"></a><span data-ttu-id="bfbe0-187">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="bfbe0-187">See Also</span></span>
[<span data-ttu-id="bfbe0-188">Hafist handa með Power BI</span><span class="sxs-lookup"><span data-stu-id="bfbe0-188">Get started with Power BI</span></span>](https://docs.microsoft.com/en-us/power-bi/service-get-started)  
<span data-ttu-id="bfbe0-189">[Power BI - Grunnatriði](https://docs.microsoft.com/en-us/power-bi/service-basic-concepts)
[Viðskiptagreind](bi.md)</span><span class="sxs-lookup"><span data-stu-id="bfbe0-189">[Power BI - Basic Concepts](https://docs.microsoft.com/en-us/power-bi/service-basic-concepts)
[Business Intelligence](bi.md)</span></span>  
<span data-ttu-id="bfbe0-190">[Velkomin(n) í [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)</span><span class="sxs-lookup"><span data-stu-id="bfbe0-190">[Welcome to [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)</span></span>  
[<span data-ttu-id="bfbe0-191">Innflutningur viðskiptagagna úr öðrum fjárhagskerfum</span><span class="sxs-lookup"><span data-stu-id="bfbe0-191">Importing Business Data from Other Finance Systems</span></span>](upload-data.md)  
<span data-ttu-id="bfbe0-192">[Uppsetning [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span><span class="sxs-lookup"><span data-stu-id="bfbe0-192">[Setting Up [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span></span>  
[<span data-ttu-id="bfbe0-193">Fjármál</span><span class="sxs-lookup"><span data-stu-id="bfbe0-193">Finance</span></span>](finance.md)  
<span data-ttu-id="bfbe0-194">[Uppsetning skýrslugerðar fyrir [!INCLUDE[d365fin](includes/d365fin_md.md)] í Power BI](across-how-use-financials-data-source-powerbi.md)</span><span class="sxs-lookup"><span data-stu-id="bfbe0-194">[Setup Reporting for [!INCLUDE[d365fin](includes/d365fin_md.md)] in Power BI](across-how-use-financials-data-source-powerbi.md)</span></span>  

