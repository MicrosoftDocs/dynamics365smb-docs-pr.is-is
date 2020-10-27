---
title: Power BI Samþættingaríhlutur og yfirlit yfir arkitektúr fyrir Business Central| Microsoft docs
description: Það er auðvelt að fá innsýn, viðskiptaupplýsingar og afkastavísi (KPI) í Business Central gögnum með Business Central forritunum fyrir Power BI.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: account schedule, analysis, reporting, financial report, business intelligence, KPI
ms.reviewer: edupont
ms.date: 10/01/2020
ms.author: jswymer
ms.openlocfilehash: d02740b0f4c73b96be9268cfdf5e4c3de157d5d5
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/01/2020
ms.locfileid: "3924529"
---
# <a name="power-bi-integration-component-and-architecture-overview-for-prodshort"></a><span data-ttu-id="b18a1-103">Power BI Samþættingaríhlutur og hönnunaryfirlit fyrir [!INCLUDE[prodshort](includes/prodshort.md)]</span><span class="sxs-lookup"><span data-stu-id="b18a1-103">Power BI Integration Component and Architecture Overview for [!INCLUDE[prodshort](includes/prodshort.md)]</span></span>

<span data-ttu-id="b18a1-104">Í þessari grein muntu fá upplýsingar um mismunandi þætti Power BI samþættingar við [!INCLUDE[prodshort](includes/prodshort.md)] til að hjálpa þér að skilja innleiðingu og notkun.</span><span class="sxs-lookup"><span data-stu-id="b18a1-104">In this article, you'll learn about the different aspects of Power BI integration with [!INCLUDE[prodshort](includes/prodshort.md)] to help you understand its implementation and use.</span></span>

## <a name="components"></a><span data-ttu-id="b18a1-105">Íhlutir</span><span class="sxs-lookup"><span data-stu-id="b18a1-105">Components</span></span>

<span data-ttu-id="b18a1-106">Eftirfarandi tafla lýsir helstu íhlutunum sem tengjast Power BI samþættingu.</span><span class="sxs-lookup"><span data-stu-id="b18a1-106">The following table describes the major components involved with Power BI integration.</span></span>

|<span data-ttu-id="b18a1-107">Íhlutur</span><span class="sxs-lookup"><span data-stu-id="b18a1-107">Component</span></span>|<span data-ttu-id="b18a1-108">Description</span><span class="sxs-lookup"><span data-stu-id="b18a1-108">Description</span></span>|
|---------|-----------|
|<span data-ttu-id="b18a1-109">Power BI</span><span class="sxs-lookup"><span data-stu-id="b18a1-109">Power BI</span></span>|<span data-ttu-id="b18a1-110">Skýjahýsing og stjórnunarþjónusta í skýi.</span><span class="sxs-lookup"><span data-stu-id="b18a1-110">A cloud-based report hosting and management service.</span></span>|
|<span data-ttu-id="b18a1-111">Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="b18a1-111">Power BI Desktop</span></span>|<span data-ttu-id="b18a1-112">Höfundarverkfæri til að búa til skýrslur og mælaborð, og gerir þér kleift að keyra skýrslur.</span><span class="sxs-lookup"><span data-stu-id="b18a1-112">An authoring tool for building reports and dashboards, and allows you to run reports.</span></span> <span data-ttu-id="b18a1-113">Það er í boði sem ókeypis niðurhal á Microsoft Store og er uppsett staðbundið.</span><span class="sxs-lookup"><span data-stu-id="b18a1-113">It's available as a free download on Microsoft Store and is installed locally.</span></span>|
|[!INCLUDE[prodshort](includes/prodshort.md)]|<span data-ttu-id="b18a1-114">Lausn á netinu eða staðbundið með tenglum á Power BI og möguleikanum á að innfella Power BI hluta.</span><span class="sxs-lookup"><span data-stu-id="b18a1-114">Online or on-premises solution with connectors exposed to Power BI and the ability to embed a Power BI part.</span></span>|

## <a name="whats-available-from-the-start"></a><span data-ttu-id="b18a1-115">Það sem er í boði frá upphafi</span><span class="sxs-lookup"><span data-stu-id="b18a1-115">What's available from the start</span></span>

<span data-ttu-id="b18a1-116">Eftirfarandi tafla lýsir tiltækum eiginleikum.</span><span class="sxs-lookup"><span data-stu-id="b18a1-116">The following table describes available features.</span></span>

|<span data-ttu-id="b18a1-117">Sérkenni</span><span class="sxs-lookup"><span data-stu-id="b18a1-117">Feature</span></span>|[!INCLUDE[prodshort](includes/prodshort.md)] <span data-ttu-id="b18a1-118">á netinu eða aðstoð á staðnum</span><span class="sxs-lookup"><span data-stu-id="b18a1-118">online or on-premises support</span></span>|
|-------|---------------------|
|<span data-ttu-id="b18a1-119">Power BI Ttengi</span><span class="sxs-lookup"><span data-stu-id="b18a1-119">Power BI connectors</span></span>|<span data-ttu-id="b18a1-120">Bæði.</span><span class="sxs-lookup"><span data-stu-id="b18a1-120">Both.</span></span> <span data-ttu-id="b18a1-121">Mismunandi tengi fyrir netið og á staðnum.</span><span class="sxs-lookup"><span data-stu-id="b18a1-121">Different connectors for online and on-premises.</span></span> <span data-ttu-id="b18a1-122">Sama tengi notað fyrir Power BI Desktop og Power BI þjónustuna</span><span class="sxs-lookup"><span data-stu-id="b18a1-122">Same connector used for Power BI Desktop and Power BI Service</span></span> |
|<span data-ttu-id="b18a1-123">Innfelld reynsla fyrir skoðun á tiltekinni skýrslu innan upplýsingareits í [!INCLUDE[prodshort](includes/prodshort.md)]</span><span class="sxs-lookup"><span data-stu-id="b18a1-123">Embedded experience for viewing a given report inside a FactBox in [!INCLUDE[prodshort](includes/prodshort.md)]</span></span>|<span data-ttu-id="b18a1-124">Bæði.</span><span class="sxs-lookup"><span data-stu-id="b18a1-124">Both.</span></span> <span data-ttu-id="b18a1-125">Krefst þess að grunnstilling birti skýrslur á staðnum.</span><span class="sxs-lookup"><span data-stu-id="b18a1-125">Requires configuration to display reports for on-premises.</span></span>|
|<span data-ttu-id="b18a1-126">Power BI-skýrslustjórnun frá [!INCLUDE[prodshort](includes/prodshort.md)]</span><span class="sxs-lookup"><span data-stu-id="b18a1-126">Power BI report management from [!INCLUDE[prodshort](includes/prodshort.md)]</span></span>|<span data-ttu-id="b18a1-127">Beinlínutengt</span><span class="sxs-lookup"><span data-stu-id="b18a1-127">Online</span></span>|
|<span data-ttu-id="b18a1-128">Sjálfgefnar Power BI skýrslur um hlutverkamiðstöðvar virkjaðar á Power BI</span><span class="sxs-lookup"><span data-stu-id="b18a1-128">Default Power BI reports on role centers deployed to Power BI</span></span>|<span data-ttu-id="b18a1-129">Beinlínutengt</span><span class="sxs-lookup"><span data-stu-id="b18a1-129">Online</span></span>|
|<span data-ttu-id="b18a1-130">Power BI-forrit á Microsoft AppSource</span><span class="sxs-lookup"><span data-stu-id="b18a1-130">Power BI Apps on Microsoft AppSource</span></span>|<span data-ttu-id="b18a1-131">Tengt.</span><span class="sxs-lookup"><span data-stu-id="b18a1-131">Online.</span></span>|

## <a name="architecture"></a><span data-ttu-id="b18a1-132">Högun</span><span class="sxs-lookup"><span data-stu-id="b18a1-132">Architecture</span></span>

[!INCLUDE[prodshort](includes/prodshort.md)] <span data-ttu-id="b18a1-133">samþættist við Power BI í gegnum tengil með OData.</span><span class="sxs-lookup"><span data-stu-id="b18a1-133">integrates with Power BI through a connector using OData.</span></span> <span data-ttu-id="b18a1-134">Gagnauppruni fyrir Power BI-skýrslur er óvarinn sem OData vefþjónustur.</span><span class="sxs-lookup"><span data-stu-id="b18a1-134">The data source for Power BI reports is exposed as OData web services.</span></span>

![Power BI högun fyrir samþættingu við Business Central](./media/power-bi-architecture.png)

## <a name="general-flow"></a><span data-ttu-id="b18a1-136">Almennt flæði</span><span class="sxs-lookup"><span data-stu-id="b18a1-136">General Flow</span></span>

<span data-ttu-id="b18a1-137">Eftirfarandi skýringarmynd sýnir grunnverkflæði fyrir notendur þegar verið er að tengja [!INCLUDE[prodshort](includes/prodshort.md)] við Power BI.</span><span class="sxs-lookup"><span data-stu-id="b18a1-137">The following diagram illustrates the basic workflow for users when connecting [!INCLUDE[prodshort](includes/prodshort.md)] to Power BI.</span></span>

![Power BI verkflæði fyrir samþættingu við Business Central](./media/power-bi-flow.png)

1. <span data-ttu-id="b18a1-139">Notandi skráir sig fyrir Power BI -reikningi.</span><span class="sxs-lookup"><span data-stu-id="b18a1-139">User signs up for a Power BI account.</span></span>
2. <span data-ttu-id="b18a1-140">Notandi tengist Power BI frá [!INCLUDE[prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="b18a1-140">User connects to Power BI from [!INCLUDE[prodshort](includes/prodshort.md)].</span></span>
3. [!INCLUDE[prodshort](includes/prodshort.md)] <span data-ttu-id="b18a1-141">staðfestir leyfið.</span><span class="sxs-lookup"><span data-stu-id="b18a1-141">verifies the license.</span></span>
4. [!INCLUDE[prodshort](includes/prodshort.md)] <span data-ttu-id="b18a1-142">virkjar sjálfgefnar skýrslur í Power BI-þjónustunni.</span><span class="sxs-lookup"><span data-stu-id="b18a1-142">deploys default reports to the Power BI service.</span></span> <span data-ttu-id="b18a1-143">Þetta skref gildir aðeins [!INCLUDE[prodshort](includes/prodshort.md)] á netinu.</span><span class="sxs-lookup"><span data-stu-id="b18a1-143">This step only happens for [!INCLUDE[prodshort](includes/prodshort.md)] online.</span></span>
5. [!INCLUDE[prodshort](includes/prodshort.md)] <span data-ttu-id="b18a1-144">gerir skýrslur í Power BI í boði fyrir val í [!INCLUDE[prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="b18a1-144">makes reports in Power BI available for selection in [!INCLUDE[prodshort](includes/prodshort.md)].</span></span> <span data-ttu-id="b18a1-145">Sjálfgefnar skýrslur birtast sjálfkrafa í Power BI-hlutum.</span><span class="sxs-lookup"><span data-stu-id="b18a1-145">Default reports are automatically displayed in Power BI parts.</span></span>
6. <span data-ttu-id="b18a1-146">Notandi stofnar skýrslu í Power BI Desktop.</span><span class="sxs-lookup"><span data-stu-id="b18a1-146">User creates a report in Power BI Desktop.</span></span>
7. <span data-ttu-id="b18a1-147">Notandi gefur út skýrslu á Power BI -þjónustuna.</span><span class="sxs-lookup"><span data-stu-id="b18a1-147">User publishes the report to the Power BI service.</span></span> <span data-ttu-id="b18a1-148">Svo er hægt að velja skýrslurnar í [!INCLUDE[prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="b18a1-148">The reports are then available for selection in [!INCLUDE[prodshort](includes/prodshort.md)].</span></span>

## <a name="see-related-training-at-microsoft-learn"></a><span data-ttu-id="b18a1-149">Sjá tengda þjálfun á [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)</span><span class="sxs-lookup"><span data-stu-id="b18a1-149">See Related Training at [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)</span></span>

## <a name="see-also"></a><span data-ttu-id="b18a1-150">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="b18a1-150">See Also</span></span>

[<span data-ttu-id="b18a1-151">Business Central og Power BI</span><span class="sxs-lookup"><span data-stu-id="b18a1-151">Business Central and Power BI</span></span>](admin-powerbi.md)  
[<span data-ttu-id="b18a1-152">Power BI fyrir neytendur</span><span class="sxs-lookup"><span data-stu-id="b18a1-152">Power BI for consumers</span></span>](/power-bi/consumer/end-user-consumer)  
[<span data-ttu-id="b18a1-153">„Nýtt útlit“ Power BI þjónustunnar</span><span class="sxs-lookup"><span data-stu-id="b18a1-153">The 'new look' of the Power BI service</span></span>](/power-bi/service-new-look)  
[<span data-ttu-id="b18a1-154">Stutt leiðbeining: Tengjast við gögn í Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="b18a1-154">Quickstart: Connect to data in Power BI Desktop</span></span>](/power-bi/desktop-quickstart-connect-to-data)  
[<span data-ttu-id="b18a1-155">Power BI fylgiskjöl</span><span class="sxs-lookup"><span data-stu-id="b18a1-155">Power BI documentation</span></span>](/power-bi/)  
[<span data-ttu-id="b18a1-156">Viðskiptaupplýsingar</span><span class="sxs-lookup"><span data-stu-id="b18a1-156">Business Intelligence</span></span>](bi.md)  
[<span data-ttu-id="b18a1-157">Hafist handa</span><span class="sxs-lookup"><span data-stu-id="b18a1-157">Getting Started</span></span>](product-get-started.md)  
[<span data-ttu-id="b18a1-158">Innflutningur viðskiptagagna úr öðrum fjárhagskerfum</span><span class="sxs-lookup"><span data-stu-id="b18a1-158">Importing Business Data from Other Finance Systems</span></span>](across-import-data-configuration-packages.md)  
<span data-ttu-id="b18a1-159">[Uppsetning [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span><span class="sxs-lookup"><span data-stu-id="b18a1-159">[Setting Up [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span></span>  
<span data-ttu-id="b18a1-160">[Nota [!INCLUDE[d365fin](includes/d365fin_md.md)] sem Power BI gagnaveitu](across-how-use-financials-data-source-powerbi.md)</span><span class="sxs-lookup"><span data-stu-id="b18a1-160">[Using [!INCLUDE[d365fin](includes/d365fin_md.md)] as a Power BI Data Source](across-how-use-financials-data-source-powerbi.md)</span></span>  
<span data-ttu-id="b18a1-161">[Nota [!INCLUDE[d365fin](includes/d365fin_md.md)] sem Power Apps gagnaveitu](across-how-use-financials-data-source-powerapps.md)</span><span class="sxs-lookup"><span data-stu-id="b18a1-161">[Using [!INCLUDE[d365fin](includes/d365fin_md.md)] as a Power Apps Data Source](across-how-use-financials-data-source-powerapps.md)</span></span>  
<span data-ttu-id="b18a1-162">[Nota [!INCLUDE[d365fin](includes/d365fin_md.md)] í Power Automate](across-how-use-financials-data-source-flow.md)</span><span class="sxs-lookup"><span data-stu-id="b18a1-162">[Using [!INCLUDE[d365fin](includes/d365fin_md.md)] in Power Automate](across-how-use-financials-data-source-flow.md)</span></span>  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
