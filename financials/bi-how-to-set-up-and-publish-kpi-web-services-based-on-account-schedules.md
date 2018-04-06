---
title: "Hvernig á að: Setja upp og gefa út KPI-vefþjónustu sem byggir á fjárhagsskemum | Microsoft Docs"
description: "Í **Uppsetning Fjárhagsskema KPI netþjónustu** glugganum getur þú ákveðið hvernig skal sýna KPI gögn fjárhagsskema og á hvaða einstaka fjárhagsskemum skuli byggja afkastavísa."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/08/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 57f36592105faf0801864e034c3b930ae196ee62
ms.contentlocale: is-is
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-and-publish-kpi-web-services-based-on-account-schedules"></a><span data-ttu-id="b86cf-103">Setja upp og gefa út KPI-vefþjónustu sem byggir á fjárhagsskemum</span><span class="sxs-lookup"><span data-stu-id="b86cf-103">Set Up and Publish KPI Web Services Based on Account Schedules</span></span>
<span data-ttu-id="b86cf-104">Í **Uppsetning Fjárhagsskema KPI netþjónustu** glugganum getur þú ákveðið hvernig skal sýna KPI gögn fjárhagsskema og á hvaða einstaka fjárhagsskemum skuli byggja afkastavísa.</span><span class="sxs-lookup"><span data-stu-id="b86cf-104">In the **Account Schedule KPI Web Service Setup** window, you set up how to show the account-schedule KPI data and which specific account schedules to base the KPIs on.</span></span> <span data-ttu-id="b86cf-105">Þegar þú velur **Birta netþjónustu** hnappinn bætast KPI gögn fjárhagsskema á lista yfir vefþjónustu sem birt hefur verið í glugganum **Vefþjónusta**.</span><span class="sxs-lookup"><span data-stu-id="b86cf-105">When you choose the **Publish Web Service** button, the specified account-schedule KPI data is added to the list of published web services in the **Web Services** window.</span></span>  

## <a name="to-set-up-and-publish-a-kpi-web-service-that-is-based-on-account-schedules"></a><span data-ttu-id="b86cf-106">Til að setja upp og gefa út KPI-vefþjónustu sem byggir á fjárhagsskemum</span><span class="sxs-lookup"><span data-stu-id="b86cf-106">To set up and publish a KPI web service that is based on account schedules</span></span>  

1.  <span data-ttu-id="b86cf-107">Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") táknið slá inn **Uppsetning vefþjónustu fyrir KPI fyrir fjárhagsskema** og velja svo tengdan tengil.</span><span class="sxs-lookup"><span data-stu-id="b86cf-107">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Account Schedule KPI Web Service Setup**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="b86cf-108">Á flýtiflipanum **Almennt** þarf að fylla reitina út eins og lýst er í eftirfarandi töflu.</span><span class="sxs-lookup"><span data-stu-id="b86cf-108">On the **General** FastTab, fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="b86cf-109">Svæði</span><span class="sxs-lookup"><span data-stu-id="b86cf-109">Field</span></span>|<span data-ttu-id="b86cf-110">Lýsing</span><span class="sxs-lookup"><span data-stu-id="b86cf-110">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="b86cf-111">**Forspárgildi hefjast**</span><span class="sxs-lookup"><span data-stu-id="b86cf-111">**Forecasted Values Start**</span></span>|<span data-ttu-id="b86cf-112">Tilgreinið á hvaða tímapunkti áætluðu gildin eru sýnd á mynd KPI fyrir fjárhagsskema.</span><span class="sxs-lookup"><span data-stu-id="b86cf-112">Specify at what point in time forecasted values are shown on the account-schedule KPI graphic.</span></span><br /><br /> <span data-ttu-id="b86cf-113">Spárgildin eru sótt í fjárhagsáætlun sem þú velur reitnum **Heiti fjárhagsáætlunar**.</span><span class="sxs-lookup"><span data-stu-id="b86cf-113">The forecasted values are retrieved from the general ledger budget that you select in the **G/L Budget Name** field.</span></span> <span data-ttu-id="b86cf-114">**Athugið:**  Til að fá afkastavísana sem sýna spárgildin eftir tiltekna dagsetningu og raungildin fyrir dagsetninguna, geturðu breytt reitnum **Leyfa bókun frá** í glugganum **Uppsetning Fjárhags**.</span><span class="sxs-lookup"><span data-stu-id="b86cf-114">**Note:**  To obtain KPIs that show forecasted figures after a certain date and actual figures before the date, you can change the **Allow Posting From** field in the **General Ledger Setup** window.</span></span> <span data-ttu-id="b86cf-115">Frekari upplýsingar, sjá Leyfa bókun frá</span><span class="sxs-lookup"><span data-stu-id="b86cf-115">For more information, see Allow Posting From.</span></span>|  
    |<span data-ttu-id="b86cf-116">**Heiti fjárhagsáætl.**</span><span class="sxs-lookup"><span data-stu-id="b86cf-116">**G/L Budget Name**</span></span>|<span data-ttu-id="b86cf-117">Tilgreinið heiti fjárhagsáætlunarinnar sem veitir áætluð gildi fyrir KPI-vefþjónustu fjárhagsskemans.</span><span class="sxs-lookup"><span data-stu-id="b86cf-117">Specify the name of the general ledger budget that provides forecasted values to the account-schedule KPI web service.</span></span>|  
    |<span data-ttu-id="b86cf-118">**Tímabil**</span><span class="sxs-lookup"><span data-stu-id="b86cf-118">**Period**</span></span>|<span data-ttu-id="b86cf-119">Tilgreinið tímabilið sem KPI-vefþjónusta fjárhagsskemans er byggð á.</span><span class="sxs-lookup"><span data-stu-id="b86cf-119">Specify the period that the account-schedule KPI web service is based on.</span></span>|  
    |<span data-ttu-id="b86cf-120">**Skoða eftir**</span><span class="sxs-lookup"><span data-stu-id="b86cf-120">**View By**</span></span>|<span data-ttu-id="b86cf-121">Tilgreinið hvaða tímabil á að nota til að sýna KPI fyrir fjárhagsskema.</span><span class="sxs-lookup"><span data-stu-id="b86cf-121">Specify which time interval the account-schedule KPI is shown in.</span></span>|  
    |<span data-ttu-id="b86cf-122">**Heiti vefþjónustu**</span><span class="sxs-lookup"><span data-stu-id="b86cf-122">**Web Service Name**</span></span>|<span data-ttu-id="b86cf-123">Tilgreinið heiti KPI-vefþjónustu fyrir fjárhagsskema.</span><span class="sxs-lookup"><span data-stu-id="b86cf-123">Specify the name of the account-schedule KPI web service.</span></span><br /><br /> <span data-ttu-id="b86cf-124">Þetta heiti mun birtast í **Heiti þjónustu** reitnum í **Netþjónusta** glugganum.</span><span class="sxs-lookup"><span data-stu-id="b86cf-124">This name will appear in the **Service Name** field in the **Web Services** window.</span></span>|  

    <span data-ttu-id="b86cf-125">Nú skal tilgreina eitt eða fleiri fjárhagsskemu sem á að birta sem KPI-vefþjónustu samkvæmt uppsetningunni í fyrri töflu.</span><span class="sxs-lookup"><span data-stu-id="b86cf-125">Proceed to specify one or more account schedules that you want to publish as a KPI web service according to the setup that you made in the previous table.</span></span>  

3.  <span data-ttu-id="b86cf-126">Í flýtiflipanum **Fjárhagsskemu** þarf að fylla reitina út eins og lýst er í eftirfarandi töflu.</span><span class="sxs-lookup"><span data-stu-id="b86cf-126">On the **Account Schedules** FastTab, fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="b86cf-127">Svæði</span><span class="sxs-lookup"><span data-stu-id="b86cf-127">Field</span></span>|<span data-ttu-id="b86cf-128">Lýsing</span><span class="sxs-lookup"><span data-stu-id="b86cf-128">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="b86cf-129">**Heiti fjárh.skema**</span><span class="sxs-lookup"><span data-stu-id="b86cf-129">**Acc. Schedule Name**</span></span>|<span data-ttu-id="b86cf-130">Tilgreinið fjárhagsskemað sem KPI-vefþjónustan byggir á.</span><span class="sxs-lookup"><span data-stu-id="b86cf-130">Specify the account schedule that the KPI web service is based on.</span></span>|  
    |<span data-ttu-id="b86cf-131">**Lýsing á fjárhagsskema**</span><span class="sxs-lookup"><span data-stu-id="b86cf-131">**Acc. Schedule Description**</span></span>|<span data-ttu-id="b86cf-132">Tilgreinið lýsingu fjárhagsskemans sem KPI-vefþjónustan byggir á.</span><span class="sxs-lookup"><span data-stu-id="b86cf-132">Specify the description of the account schedule that the KPI web service is based on.</span></span>|  

4.  <span data-ttu-id="b86cf-133">Liður 3 er endurtekinn fyrir öll fjárhagsskemu sem þú vilt nota í KPI-fjárhagsskemavefþjónustunni.</span><span class="sxs-lookup"><span data-stu-id="b86cf-133">Repeat step 3 for all the account schedules that you want to base the account-schedule KPI web service on.</span></span>  
5.  <span data-ttu-id="b86cf-134">Til að skoða eða breyta völdu fjárhagsskema er **Fjárhagsskema** valið á flýtiflipanum **Breyta fjárhagsskema**.</span><span class="sxs-lookup"><span data-stu-id="b86cf-134">To view or edit the selected account schedule, on the **Account Schedule** FastTab, choose the **Edit Account Schedule** action.</span></span>  
6.  <span data-ttu-id="b86cf-135">Til að skoða KPI gögn fyrir afkastavísisvefþjónustu fyrir fjárhagsskema sem þú hefur sett upp, skal velja **Vefþjónusta KPI fyrir fjárhagsskema** aðgerðinni.</span><span class="sxs-lookup"><span data-stu-id="b86cf-135">To view the account-schedule KPI data that you have set up, choose the **Account Schedule KPI Web Service** action.</span></span>  
7.  <span data-ttu-id="b86cf-136">Til að birta afkastavísisvefþjónustu fyrir fjárhagsskema skal velja **Birta vefþjónustu** aðgerðina.</span><span class="sxs-lookup"><span data-stu-id="b86cf-136">To publish the account-schedule KPI web service, choose the **Publish Web Service** action.</span></span> <span data-ttu-id="b86cf-137">Netþjónustunni er bætt á lista yfir vefþjónustu sem birt hefur verið í glugganum **Vefþjónusta**.</span><span class="sxs-lookup"><span data-stu-id="b86cf-137">The web service is added to the list of published web services in the **Web Services** window.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="b86cf-138">Þú getur líka birt KPI netþjónustuna með því að benda á síðuhlutinn **Uppsetning fjárhagsskema KPI netþjónustu** frá **Netþjónusta** glugganum.</span><span class="sxs-lookup"><span data-stu-id="b86cf-138">You can also publish the KPI web service by pointing to the **Account Schedule KPI Web Service Setup** page object from the **Web Services** window.</span></span> <span data-ttu-id="b86cf-139">Frekari upplýsingar er að finna í [Birta vefþjónustu](across-how-publish-web-service.md).</span><span class="sxs-lookup"><span data-stu-id="b86cf-139">For more information, see [Publish a Web Service](across-how-publish-web-service.md).</span></span>  

## <a name="see-also"></a><span data-ttu-id="b86cf-140">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="b86cf-140">See Also</span></span>  
[<span data-ttu-id="b86cf-141">Viðskiptaupplýsingar</span><span class="sxs-lookup"><span data-stu-id="b86cf-141">Business Intelligence</span></span>](bi.md)  
[<span data-ttu-id="b86cf-142">Fjármál</span><span class="sxs-lookup"><span data-stu-id="b86cf-142">Finance</span></span>](finance.md)  
[<span data-ttu-id="b86cf-143">Uppsetning Fjármála</span><span class="sxs-lookup"><span data-stu-id="b86cf-143">Setting Up Finance</span></span>](finance-setup-finance.md)  
[<span data-ttu-id="b86cf-144">Fjárhagur og bókhaldslyklar</span><span class="sxs-lookup"><span data-stu-id="b86cf-144">The General Ledger and the Chart of Accounts</span></span>](finance-general-ledger.md)  
<span data-ttu-id="b86cf-145">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="b86cf-145">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

