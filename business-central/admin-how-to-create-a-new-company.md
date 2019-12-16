---
title: Hvernig á að búa til nýtt fyrirtæki | Microsoft Docs
description: Til að nota RapidStart Services eru stofnaðar töflur og síður en engin gögn eru í þeim.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: bbd845f7974ce2d0b6ade27d290e1173fad42f37
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/03/2019
ms.locfileid: "2878890"
---
# <a name="create-a-new-company"></a><span data-ttu-id="129ff-103">Búa til nýtt fyrirtæki</span><span class="sxs-lookup"><span data-stu-id="129ff-103">Create a New Company</span></span>
<span data-ttu-id="129ff-104">Til að nota RapidStart Services fyrir [!INCLUDE[d365fin](includes/d365fin_md.md)] skal fyrst stofna nýtt fyrirtæki þar sem framkvæma skal innleiðingu viðskiptamanns.</span><span class="sxs-lookup"><span data-stu-id="129ff-104">To use RapidStart Services for [!INCLUDE[d365fin](includes/d365fin_md.md)], you first create a new company for which you want to perform a customer implementation.</span></span> <span data-ttu-id="129ff-105">Þegar nýtt fyrirtæki er stofnað eru staðlaðar [!INCLUDE[d365fin](includes/d365fin_md.md)] töflur og síður búnar til, en engin gögn eru í þeim.</span><span class="sxs-lookup"><span data-stu-id="129ff-105">When you create a new company, the standard [!INCLUDE[d365fin](includes/d365fin_md.md)] tables and pages are created, but there is no data in them.</span></span>

<span data-ttu-id="129ff-106">Auk þess er hægt að beita sérstökum uppsetningargögnum fyrir fyrirtækið eftir frumstillingu.</span><span class="sxs-lookup"><span data-stu-id="129ff-106">In addition, you can apply specific setup data to your company after you initialize it.</span></span> <span data-ttu-id="129ff-107">Upplýsingarnar koma úr grunnstillingapakka, sem er .rapidstart skrá, sem afhendir innihald á samþjöppuðu formi.</span><span class="sxs-lookup"><span data-stu-id="129ff-107">The information is provided in a configuration package, a .rapidstart file, which delivers content in a compressed format.</span></span>  

<span data-ttu-id="129ff-108">Grunnstillingarpakkar dæma, þ.á.m. skrár sem miðast við land/svæði eru innifaldar í CRONUS sýnifyrirtækinu.</span><span class="sxs-lookup"><span data-stu-id="129ff-108">Example configuration packages, including country/region-specific files, are included with the CRONUS demonstration company.</span></span> <span data-ttu-id="129ff-109">Notið eftirfarandi aðgerð til að nota pakkann með dæmastillingunum með nýju fyrirtæki.</span><span class="sxs-lookup"><span data-stu-id="129ff-109">Use the following procedures to use the example configuration package with a new company.</span></span>  

## <a name="to-use-the-sample-basicconfig-configuration-package"></a><span data-ttu-id="129ff-110">Til að nota dæmið um BASICCONFIG grunnstillingarpakkann</span><span class="sxs-lookup"><span data-stu-id="129ff-110">To use the sample BASICCONFIG configuration package</span></span>  
1. <span data-ttu-id="129ff-111">Opna fyrirtækið CRONUS International Ltd.</span><span class="sxs-lookup"><span data-stu-id="129ff-111">Open the CRONUS International Ltd. company.</span></span> <span data-ttu-id="129ff-112">Frekari upplýsingar eru í [Breyta grundvallarstillingum](ui-change-basic-settings.md).</span><span class="sxs-lookup"><span data-stu-id="129ff-112">For more information, see [Change Basic Settings](ui-change-basic-settings.md).</span></span>
2. <span data-ttu-id="129ff-113">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Grunnstillingapakkar** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="129ff-113">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Configuration Packages**, and then choose the related link.</span></span>  
3. <span data-ttu-id="129ff-114">Velja skal BASICCONFIG-pakkann af listanum og síðan velja aðgerðina **Flytja út pakka**.</span><span class="sxs-lookup"><span data-stu-id="129ff-114">Choose the BASICCONFIG package from the list, and then choose the **Export Package** action.</span></span>  

<span data-ttu-id="129ff-115">Notið eftirfarandi aðgerð til að búa til nýtt fyrirtæki og nota BASICCONFIC pakkann sem hluta ferlisins.</span><span class="sxs-lookup"><span data-stu-id="129ff-115">Use the following procedure to create a new company, and use the BASICCONFIG package as part of the process.</span></span>  

## <a name="to-create-a-new-company"></a><span data-ttu-id="129ff-116">Til að búa til nýtt fyrirtæki</span><span class="sxs-lookup"><span data-stu-id="129ff-116">To create a new company</span></span>  
1. <span data-ttu-id="129ff-117">Búa til nýtt fyrirtæki.</span><span class="sxs-lookup"><span data-stu-id="129ff-117">Create a new company.</span></span> <span data-ttu-id="129ff-118">Nánari upplýsingar eru í [Stofna ný fyrirtæki í [!INCLUDE[d365fin](includes/d365fin_md.md)]](about-new-company.md).</span><span class="sxs-lookup"><span data-stu-id="129ff-118">For more information, see [Creating New Companies in [!INCLUDE[d365fin](includes/d365fin_md.md)]](about-new-company.md).</span></span>
2. <span data-ttu-id="129ff-119">Frá Mitt hlutverk RapidStart Services innleiðara er hægt að flytja inn grunnstillingarpakkann sem hefur verið fluttur úr fyrirtækinu CRONUS International Ltd.</span><span class="sxs-lookup"><span data-stu-id="129ff-119">From the RapidStart Services Implementer Role Center, you can now import the configuration package that you exported from the CRONUS International Ltd. company.</span></span>

<span data-ttu-id="129ff-120">Þegar búið er að stofna nýtt fyrirtæki, eru sumar töflur sjálfkrafa fylltar út, jafnvel þótt fyrirtækissniðmát sé ekki notað.</span><span class="sxs-lookup"><span data-stu-id="129ff-120">After you create a new company, some tables are automatically filled in, even if no company template is applied.</span></span> <span data-ttu-id="129ff-121">Til dæmis má sjá stöðluðu kótana fyrir bókun og runufærslur á síðunni **Forðakóði**.</span><span class="sxs-lookup"><span data-stu-id="129ff-121">For example, you can review the standard codes for posting and batch transactions on the **Source Code** page.</span></span> <span data-ttu-id="129ff-122">Ef þú veitir staðbundna útgáfa af [!INCLUDE[d365fin](includes/d365fin_md.md)] ættir þú að fara yfir þessa töflu og íhuga hugsanleg vandamál fyrir viðkomandi tungumál.</span><span class="sxs-lookup"><span data-stu-id="129ff-122">If you provide a local version of [!INCLUDE[d365fin](includes/d365fin_md.md)], you should review this table and consider any local language issues.</span></span>

## <a name="about-data-tables"></a><span data-ttu-id="129ff-123">Um gagnatöflur</span><span class="sxs-lookup"><span data-stu-id="129ff-123">About Data Tables</span></span>
[!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="129ff-124">gagnatöflur eru til í tveim grunntegundum: Aðaltafla og uppsetning.</span><span class="sxs-lookup"><span data-stu-id="129ff-124">, data tables come in two basic types: Master and Setup.</span></span> <span data-ttu-id="129ff-125">Þegar verið er að setja upp fyrirtækjaskilgreiningu er hægt að nota þessar gerðir til að skerpa á skilgreiningaráætluninni.</span><span class="sxs-lookup"><span data-stu-id="129ff-125">When you are setting up a company configuration, you can use these types to focus your configuration strategy.</span></span>  

### <a name="master-data-tables"></a><span data-ttu-id="129ff-126">Töflur aðalgagna</span><span class="sxs-lookup"><span data-stu-id="129ff-126">Master Data Tables</span></span>  
<span data-ttu-id="129ff-127">Eftirfarandi tafla sýnir sumar aðalgagnatöflurnar.</span><span class="sxs-lookup"><span data-stu-id="129ff-127">The following table lists some of the master data tables.</span></span> <span data-ttu-id="129ff-128">Þegar nýtt fyrirtæki er frumstillt eru þessar töflur auðar.</span><span class="sxs-lookup"><span data-stu-id="129ff-128">When you initialize a new company, these tables are empty.</span></span>  

|<span data-ttu-id="129ff-129">Tafla nr.</span><span class="sxs-lookup"><span data-stu-id="129ff-129">Table No.</span></span>|<span data-ttu-id="129ff-130">Töfluheiti</span><span class="sxs-lookup"><span data-stu-id="129ff-130">Table Name</span></span>|  
|-------------------|--------------------|  
|<span data-ttu-id="129ff-131">15</span><span class="sxs-lookup"><span data-stu-id="129ff-131">15</span></span>|<span data-ttu-id="129ff-132">Fjárhagsreikningur</span><span class="sxs-lookup"><span data-stu-id="129ff-132">G/L Account</span></span>|  
|<span data-ttu-id="129ff-133">18</span><span class="sxs-lookup"><span data-stu-id="129ff-133">18</span></span>|<span data-ttu-id="129ff-134">Viðskiptavinur</span><span class="sxs-lookup"><span data-stu-id="129ff-134">Customer</span></span>|  
|<span data-ttu-id="129ff-135">23</span><span class="sxs-lookup"><span data-stu-id="129ff-135">23</span></span>|<span data-ttu-id="129ff-136">Lánardrottinn</span><span class="sxs-lookup"><span data-stu-id="129ff-136">Vendor</span></span>|  
|<span data-ttu-id="129ff-137">27</span><span class="sxs-lookup"><span data-stu-id="129ff-137">27</span></span>|<span data-ttu-id="129ff-138">Atriði</span><span class="sxs-lookup"><span data-stu-id="129ff-138">Item</span></span>|  
|<span data-ttu-id="129ff-139">5050</span><span class="sxs-lookup"><span data-stu-id="129ff-139">5050</span></span>|<span data-ttu-id="129ff-140">Tengiliður</span><span class="sxs-lookup"><span data-stu-id="129ff-140">Contact</span></span>|  

### <a name="setup-data-tables"></a><span data-ttu-id="129ff-141">Gagnatöflur uppsetningar</span><span class="sxs-lookup"><span data-stu-id="129ff-141">Setup Data Tables</span></span>  
<span data-ttu-id="129ff-142">Í eftirfarandi töflu koma fram sumar uppsetningargagnatöflur þar sem uppsetningarupplýsingar eru fangaðar í grunnstillingarspurningalistanum.</span><span class="sxs-lookup"><span data-stu-id="129ff-142">The following table lists some of the setup data tables, in which you capture setup information in the configuration questionnaire.</span></span> <span data-ttu-id="129ff-143">Þessar töflur innihalda grunnlínuupplýsingar þegar fyrirtækið er stofnað.</span><span class="sxs-lookup"><span data-stu-id="129ff-143">These tables contain baseline information when the company is created.</span></span>  

|<span data-ttu-id="129ff-144">Tafla nr.</span><span class="sxs-lookup"><span data-stu-id="129ff-144">Table No.</span></span>|<span data-ttu-id="129ff-145">Töfluheiti</span><span class="sxs-lookup"><span data-stu-id="129ff-145">Table Name</span></span>|  
|-------------------|--------------------|  
|<span data-ttu-id="129ff-146">98</span><span class="sxs-lookup"><span data-stu-id="129ff-146">98</span></span>|<span data-ttu-id="129ff-147">Uppsetning fjárhags</span><span class="sxs-lookup"><span data-stu-id="129ff-147">General Ledger Setup</span></span>|  
|<span data-ttu-id="129ff-148">311</span><span class="sxs-lookup"><span data-stu-id="129ff-148">311</span></span>|<span data-ttu-id="129ff-149">Sölugrunnur</span><span class="sxs-lookup"><span data-stu-id="129ff-149">Sales & Receivables Setup</span></span>|  
|<span data-ttu-id="129ff-150">312</span><span class="sxs-lookup"><span data-stu-id="129ff-150">312</span></span>|<span data-ttu-id="129ff-151">Innkaupagrunnur</span><span class="sxs-lookup"><span data-stu-id="129ff-151">Purchases & Payables Setup</span></span>|  
|<span data-ttu-id="129ff-152">313</span><span class="sxs-lookup"><span data-stu-id="129ff-152">313</span></span>|<span data-ttu-id="129ff-153">Birgðagrunnur</span><span class="sxs-lookup"><span data-stu-id="129ff-153">Inventory Setup</span></span>|  

<span data-ttu-id="129ff-154">Auk uppsetningargagnataflna inniheldur [!INCLUDE[d365fin](includes/d365fin_md.md)] einnig gögn uppsetningargerðar sem sýna grunnupplýsingar um fyrirtækið og viðskiptaferla þess.</span><span class="sxs-lookup"><span data-stu-id="129ff-154">In addition to setup data tables, [!INCLUDE[d365fin](includes/d365fin_md.md)] also has setup-type data tables that specify core information about the company and its business processes.</span></span> <span data-ttu-id="129ff-155">Eftirfarandi tafla sýnir nokkrar af þeim.</span><span class="sxs-lookup"><span data-stu-id="129ff-155">The following table lists some of them.</span></span>  

|<span data-ttu-id="129ff-156">Tafla nr.</span><span class="sxs-lookup"><span data-stu-id="129ff-156">Table No.</span></span>|<span data-ttu-id="129ff-157">Töfluheiti</span><span class="sxs-lookup"><span data-stu-id="129ff-157">Table Name</span></span>|  
|-------------------|--------------------|  
|<span data-ttu-id="129ff-158">3</span><span class="sxs-lookup"><span data-stu-id="129ff-158">3</span></span>|<span data-ttu-id="129ff-159">Greiðsluskilmálar</span><span class="sxs-lookup"><span data-stu-id="129ff-159">Payment Terms</span></span>|  
|<span data-ttu-id="129ff-160">4</span><span class="sxs-lookup"><span data-stu-id="129ff-160">4</span></span>|<span data-ttu-id="129ff-161">Gjaldmiðill</span><span class="sxs-lookup"><span data-stu-id="129ff-161">Currency</span></span>|  
|<span data-ttu-id="129ff-162">6</span><span class="sxs-lookup"><span data-stu-id="129ff-162">6</span></span>|<span data-ttu-id="129ff-163">Verðflokkar viðskm.</span><span class="sxs-lookup"><span data-stu-id="129ff-163">Customer Price Groups</span></span>|  
|<span data-ttu-id="129ff-164">5700</span><span class="sxs-lookup"><span data-stu-id="129ff-164">5700</span></span>|<span data-ttu-id="129ff-165">Birgðahaldseining</span><span class="sxs-lookup"><span data-stu-id="129ff-165">Stockkeeping Unit</span></span>|

  

## <a name="see-also"></a><span data-ttu-id="129ff-166">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="129ff-166">See Also</span></span>  
[<span data-ttu-id="129ff-167">Nota skilgreiningu á ný fyrirtæki</span><span class="sxs-lookup"><span data-stu-id="129ff-167">Apply Configurations to New Companies</span></span>](admin-apply-configuration-to-new-companies.md)  
[<span data-ttu-id="129ff-168">Uppsetning fyrirtækis með RapidStart Services</span><span class="sxs-lookup"><span data-stu-id="129ff-168">Setting Up a Company With RapidStart Services</span></span>](admin-set-up-a-company-with-rapidstart.md)  
[<span data-ttu-id="129ff-169">Stjórnun</span><span class="sxs-lookup"><span data-stu-id="129ff-169">Administration</span></span>](admin-setup-and-administration.md)
