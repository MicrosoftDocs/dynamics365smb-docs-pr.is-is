---
title: "Hvernig á að búa til nýtt fyrirtæki | Microsoft Docs"
description: "Til að nota RapidStart Services eru stofnaðar töflur og síður en engin gögn eru í þeim."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 03/06/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 8c07b7c4e6b1c82004295a187184a6f3ccb4c7c7
ms.contentlocale: is-is
ms.lasthandoff: 03/22/2018

---
# <a name="create-a-new-company"></a><span data-ttu-id="27922-103">Búa til nýtt fyrirtæki</span><span class="sxs-lookup"><span data-stu-id="27922-103">Create a New Company</span></span>
<span data-ttu-id="27922-104">Til að nota RapidStart Services fyrir [!INCLUDE[d365fin](includes/d365fin_md.md)] skal fyrst stofna nýtt fyrirtæki þar sem framkvæma skal innleiðingu viðskiptavinar.</span><span class="sxs-lookup"><span data-stu-id="27922-104">To use RapidStart Services for [!INCLUDE[d365fin](includes/d365fin_md.md)], you first create a new company for which you want to perform a customer implementation.</span></span> <span data-ttu-id="27922-105">Þegar nýtt fyrirtæki er stofnað eru staðlaðar [!INCLUDE[d365fin](includes/d365fin_md.md)] töflur og síður búnar til, en engin gögn eru í þeim.</span><span class="sxs-lookup"><span data-stu-id="27922-105">When you create a new company, the standard [!INCLUDE[d365fin](includes/d365fin_md.md)] tables and pages are created, but there is no data in them.</span></span>

<span data-ttu-id="27922-106">Auk þess er hægt að beita sérstökum uppsetningargögnum fyrir fyrirtækið eftir frumstillingu.</span><span class="sxs-lookup"><span data-stu-id="27922-106">In addition, you can apply specific setup data to your company after you initialize it.</span></span> <span data-ttu-id="27922-107">Upplýsingarnar koma úr grunnstillingapakka, sem er .rapidstart skrá, sem afhendir innihald á samþjöppuðu formi.</span><span class="sxs-lookup"><span data-stu-id="27922-107">The information is provided in a configuration package, a .rapidstart file, which delivers content in a compressed format.</span></span>  

<span data-ttu-id="27922-108">Dæmi um grunnstillingarpakka, þ.m.t. sértækar skrár fyrir land/svæði, eru hluti af sýnifyrirtækinu CRONUS.</span><span class="sxs-lookup"><span data-stu-id="27922-108">Example configuration packages, including country/region-specific files, are included with the CRONUS demonstration company.</span></span> <span data-ttu-id="27922-109">Notið eftirfarandi aðgerð til að nota pakkann með dæmastillingunum með nýju fyrirtæki.</span><span class="sxs-lookup"><span data-stu-id="27922-109">Use the following procedures to use the example configuration package with a new company.</span></span>  

## <a name="to-use-the-sample-basicconfig-configuration-package"></a><span data-ttu-id="27922-110">Til að nota dæmið um BASICCONFIG grunnstillingarpakkann</span><span class="sxs-lookup"><span data-stu-id="27922-110">To use the sample BASICCONFIG configuration package</span></span>  
1. <span data-ttu-id="27922-111">Opna fyrirtækið CRONUS International Ltd.</span><span class="sxs-lookup"><span data-stu-id="27922-111">Open the CRONUS International Ltd. company.</span></span> <span data-ttu-id="27922-112">Frekari upplýsingar, sjá [Breyta grunnstillingum](ui-change-basic-settings.md).</span><span class="sxs-lookup"><span data-stu-id="27922-112">For more information, see [Changing Basic Settings](ui-change-basic-settings.md).</span></span>
2. <span data-ttu-id="27922-113">Velja skal táknið ![Leita að síðu eða skýrslu](media/ui-search/search_small.png "Leita að síðu eða skýrslutákni"), slá inn **Grunnstillingarpakkar** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="27922-113">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Configuration Packages**, and then choose the related link.</span></span>  
3. <span data-ttu-id="27922-114">Velja skal BASICCONFIG-pakkann af listanum og síðan velja aðgerðina **Flytja út pakka**.</span><span class="sxs-lookup"><span data-stu-id="27922-114">Choose the BASICCONFIG package from the list, and then choose the **Export Package** action.</span></span>  

<span data-ttu-id="27922-115">Notið eftirfarandi aðgerð til að búa til nýtt fyrirtæki og nota BASICCONFIC pakkann sem hluta ferlisins.</span><span class="sxs-lookup"><span data-stu-id="27922-115">Use the following procedure to create a new company, and use the BASICCONFIG package as part of the process.</span></span>  

## <a name="to-create-a-new-company"></a><span data-ttu-id="27922-116">Til að búa til nýtt fyrirtæki</span><span class="sxs-lookup"><span data-stu-id="27922-116">To create a new company</span></span>  
1. <span data-ttu-id="27922-117">Búa til nýtt fyrirtæki.</span><span class="sxs-lookup"><span data-stu-id="27922-117">Create a new company.</span></span> <span data-ttu-id="27922-118">Nánari upplýsingar eru í [Stofna ný fyrirtæki í [!INCLUDE[d365fin](includes/d365fin_md.md)]](about-new-company.md).</span><span class="sxs-lookup"><span data-stu-id="27922-118">For more information, see [Creating New Companies in [!INCLUDE[d365fin](includes/d365fin_md.md)]](about-new-company.md).</span></span>
2. <span data-ttu-id="27922-119">Frá Mitt hlutverk RapidStart Services innleiðara er hægt að flytja inn grunnstillingarpakkann sem hefur verið fluttur úr fyrirtækinu CRONUS International Ltd.</span><span class="sxs-lookup"><span data-stu-id="27922-119">From the RapidStart Services Implementer Role Center, you can now import the configuration package that you exported from the CRONUS International Ltd. company.</span></span>

<span data-ttu-id="27922-120">Þegar búið er að stofna nýtt fyrirtæki, eru sumar töflur sjálfkrafa fylltar út, jafnvel þótt fyrirtækissniðmát sé ekki notað.</span><span class="sxs-lookup"><span data-stu-id="27922-120">After you create a new company, some tables are automatically filled in, even if no company template is applied.</span></span> <span data-ttu-id="27922-121">Til dæmis má sjá stöðluðu kótana fyrir bókun og runufærslur í glugganum **Forðakóði**.</span><span class="sxs-lookup"><span data-stu-id="27922-121">For example, you can review the standard codes for posting and batch transactions in the **Source Code** window.</span></span> <span data-ttu-id="27922-122">Ef þú veitir staðbundna útgáfa af [!INCLUDE[d365fin](includes/d365fin_md.md)] ættir þú að fara yfir þessa töflu og íhuga hugsanleg vandamál fyrir viðkomandi tungumál.</span><span class="sxs-lookup"><span data-stu-id="27922-122">If you provide a local version of [!INCLUDE[d365fin](includes/d365fin_md.md)], you should review this table and consider any local language issues.</span></span>

## <a name="about-data-tables"></a><span data-ttu-id="27922-123">Um gagnatöflur</span><span class="sxs-lookup"><span data-stu-id="27922-123">About Data Tables</span></span>
[!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="27922-124"> gagnatöflur eru til í tveim grunntegundum: Aðaltafla og uppsetning.</span><span class="sxs-lookup"><span data-stu-id="27922-124">, data tables come in two basic types: Master and Setup.</span></span> <span data-ttu-id="27922-125">Þegar verið er að setja upp fyrirtækjaskilgreiningu er hægt að nota þessar gerðir til að skerpa á skilgreiningaráætluninni.</span><span class="sxs-lookup"><span data-stu-id="27922-125">When you are setting up a company configuration, you can use these types to focus your configuration strategy.</span></span>  

### <a name="master-data-tables"></a><span data-ttu-id="27922-126">Töflur aðalgagna</span><span class="sxs-lookup"><span data-stu-id="27922-126">Master Data Tables</span></span>  
<span data-ttu-id="27922-127">Eftirfarandi tafla sýnir sumar aðalgagnatöflurnar.</span><span class="sxs-lookup"><span data-stu-id="27922-127">The following table lists some of the master data tables.</span></span> <span data-ttu-id="27922-128">Þegar nýtt fyrirtæki er frumstillt eru þessar töflur auðar.</span><span class="sxs-lookup"><span data-stu-id="27922-128">When you initialize a new company, these tables are empty.</span></span>  

|<span data-ttu-id="27922-129">Tafla nr.</span><span class="sxs-lookup"><span data-stu-id="27922-129">Table No.</span></span>|<span data-ttu-id="27922-130">Töfluheiti</span><span class="sxs-lookup"><span data-stu-id="27922-130">Table Name</span></span>|  
|-------------------|--------------------|  
|<span data-ttu-id="27922-131">15</span><span class="sxs-lookup"><span data-stu-id="27922-131">15</span></span>|<span data-ttu-id="27922-132">Fjárhagsreikningur</span><span class="sxs-lookup"><span data-stu-id="27922-132">G/L Account</span></span>|  
|<span data-ttu-id="27922-133">18</span><span class="sxs-lookup"><span data-stu-id="27922-133">18</span></span>|<span data-ttu-id="27922-134">Viðskiptavinur</span><span class="sxs-lookup"><span data-stu-id="27922-134">Customer</span></span>|  
|<span data-ttu-id="27922-135">23</span><span class="sxs-lookup"><span data-stu-id="27922-135">23</span></span>|<span data-ttu-id="27922-136">Lánardrottinn</span><span class="sxs-lookup"><span data-stu-id="27922-136">Vendor</span></span>|  
|<span data-ttu-id="27922-137">27</span><span class="sxs-lookup"><span data-stu-id="27922-137">27</span></span>|<span data-ttu-id="27922-138">Atriði</span><span class="sxs-lookup"><span data-stu-id="27922-138">Item</span></span>|  
|<span data-ttu-id="27922-139">5050</span><span class="sxs-lookup"><span data-stu-id="27922-139">5050</span></span>|<span data-ttu-id="27922-140">Tengiliður</span><span class="sxs-lookup"><span data-stu-id="27922-140">Contact</span></span>|  

### <a name="setup-data-tables"></a><span data-ttu-id="27922-141">Gagnatöflur uppsetningar</span><span class="sxs-lookup"><span data-stu-id="27922-141">Setup Data Tables</span></span>  
<span data-ttu-id="27922-142">Í eftirfarandi töflu koma fram sumar uppsetningargagnatöflur þar sem uppsetningarupplýsingar eru fangaðar í grunnstillingarspurningalistanum.</span><span class="sxs-lookup"><span data-stu-id="27922-142">The following table lists some of the setup data tables, in which you capture setup information in the configuration questionnaire.</span></span> <span data-ttu-id="27922-143">Þessar töflur innihalda grunnlínuupplýsingar þegar fyrirtækið er stofnað.</span><span class="sxs-lookup"><span data-stu-id="27922-143">These tables contain baseline information when the company is created.</span></span>  

|<span data-ttu-id="27922-144">Tafla nr.</span><span class="sxs-lookup"><span data-stu-id="27922-144">Table No.</span></span>|<span data-ttu-id="27922-145">Töfluheiti</span><span class="sxs-lookup"><span data-stu-id="27922-145">Table Name</span></span>|  
|-------------------|--------------------|  
|<span data-ttu-id="27922-146">98</span><span class="sxs-lookup"><span data-stu-id="27922-146">98</span></span>|<span data-ttu-id="27922-147">Uppsetning fjárhags</span><span class="sxs-lookup"><span data-stu-id="27922-147">General Ledger Setup</span></span>|  
|<span data-ttu-id="27922-148">311</span><span class="sxs-lookup"><span data-stu-id="27922-148">311</span></span>|<span data-ttu-id="27922-149">Sölugrunnur</span><span class="sxs-lookup"><span data-stu-id="27922-149">Sales & Receivables Setup</span></span>|  
|<span data-ttu-id="27922-150">312</span><span class="sxs-lookup"><span data-stu-id="27922-150">312</span></span>|<span data-ttu-id="27922-151">Innkaupagrunnur</span><span class="sxs-lookup"><span data-stu-id="27922-151">Purchases & Payables Setup</span></span>|  
|<span data-ttu-id="27922-152">313</span><span class="sxs-lookup"><span data-stu-id="27922-152">313</span></span>|<span data-ttu-id="27922-153">Birgðagrunnur</span><span class="sxs-lookup"><span data-stu-id="27922-153">Inventory Setup</span></span>|  

<span data-ttu-id="27922-154">Auk uppsetningargagnataflna inniheldur [!INCLUDE[d365fin](includes/d365fin_md.md)] einnig gögn uppsetningargerðar sem sýna grunnupplýsingar um fyrirtækið og viðskiptaferla þess.</span><span class="sxs-lookup"><span data-stu-id="27922-154">In addition to setup data tables, [!INCLUDE[d365fin](includes/d365fin_md.md)] also has setup-type data tables that specify core information about the company and its business processes.</span></span> <span data-ttu-id="27922-155">Eftirfarandi tafla sýnir nokkrar af þeim.</span><span class="sxs-lookup"><span data-stu-id="27922-155">The following table lists some of them.</span></span>  

|<span data-ttu-id="27922-156">Tafla nr.</span><span class="sxs-lookup"><span data-stu-id="27922-156">Table No.</span></span>|<span data-ttu-id="27922-157">Töfluheiti</span><span class="sxs-lookup"><span data-stu-id="27922-157">Table Name</span></span>|  
|-------------------|--------------------|  
|<span data-ttu-id="27922-158">3</span><span class="sxs-lookup"><span data-stu-id="27922-158">3</span></span>|<span data-ttu-id="27922-159">Greiðsluskilmálar</span><span class="sxs-lookup"><span data-stu-id="27922-159">Payment Terms</span></span>|  
|<span data-ttu-id="27922-160">4</span><span class="sxs-lookup"><span data-stu-id="27922-160">4</span></span>|<span data-ttu-id="27922-161">Gjaldmiðill</span><span class="sxs-lookup"><span data-stu-id="27922-161">Currency</span></span>|  
|<span data-ttu-id="27922-162">6</span><span class="sxs-lookup"><span data-stu-id="27922-162">6</span></span>|<span data-ttu-id="27922-163">Verðflokkar viðskm.</span><span class="sxs-lookup"><span data-stu-id="27922-163">Customer Price Groups</span></span>|  
|<span data-ttu-id="27922-164">5700</span><span class="sxs-lookup"><span data-stu-id="27922-164">5700</span></span>|<span data-ttu-id="27922-165">Birgðahaldseining</span><span class="sxs-lookup"><span data-stu-id="27922-165">Stockkeeping Unit</span></span>|

  

## <a name="see-also"></a><span data-ttu-id="27922-166">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="27922-166">See Also</span></span>  
[<span data-ttu-id="27922-167">Nota skilgreiningu á ný fyrirtæki</span><span class="sxs-lookup"><span data-stu-id="27922-167">Apply Configurations to New Companies</span></span>](admin-apply-configuration-to-new-companies.md)  
[<span data-ttu-id="27922-168">Uppsetning fyrirtækis með RapidStart Services</span><span class="sxs-lookup"><span data-stu-id="27922-168">Setting Up a Company With RapidStart Services</span></span>](admin-set-up-a-company-with-rapidstart.md)  
[<span data-ttu-id="27922-169">Stjórnun</span><span class="sxs-lookup"><span data-stu-id="27922-169">Administration</span></span>](admin-setup-and-administration.md)

