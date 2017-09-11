---
title: "Jafna og leiðrétta vistaðar stillingar í skýrslum | Microsoft Docs"
description: "Lýsir því hvernig not skal fyrirfram skilgreinda valmöguleika og afmarkanir til að sérstilla skýrslu, og ná fram réttum upplýsingum."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customization, personalization
ms.date: 06/02/2017
ms.author: jswymer
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 9e5f7417579a5ba0629032cf9fa664e0060b9cbf
ms.contentlocale: is-is
ms.lasthandoff: 09/11/2017

---
# <a name="saved-settings-on-reports"></a><span data-ttu-id="0a6f4-103">Vistuð Stillingar á Skýrslur</span><span class="sxs-lookup"><span data-stu-id="0a6f4-103">Saved Settings on Reports</span></span>
<span data-ttu-id="0a6f4-104">Í skýrslunni sem fer eftir að kann að birta með page sem gerir kleift að tilteknum valkosti og afmarkanir fyrir breytingar gögnin sem er tekið með í skýrslunni generated.</span><span class="sxs-lookup"><span data-stu-id="0a6f4-104">Depending on the report that is run, you might be presented with a page that lets you to set certain options and filters for changing the data that is included in the generated report.</span></span> <span data-ttu-id="0a6f4-105">Þessa síðu er heitir síðuna beiðni skýrslu.</span><span class="sxs-lookup"><span data-stu-id="0a6f4-105">This page is known as the report request page.</span></span> <span data-ttu-id="0a6f4-106">Með skýrslunni getur innihaldið eitt eða fleiri *vistuð stillingar* sem hægt er að jafna við skýrsluna úr síðuna beiðni.</span><span class="sxs-lookup"><span data-stu-id="0a6f4-106">A report can include one or more *saved settings* that you can apply to the report from the request page.</span></span> <span data-ttu-id="0a6f4-107">*Vistuð stillingar* eru skoðaður fyrirfram skilgreind valkosti og afmarkanir.</span><span class="sxs-lookup"><span data-stu-id="0a6f4-107">*Saved settings* are basically predefined options and filters.</span></span> <span data-ttu-id="0a6f4-108">Með því að nota vistaðar stillingar er er fljótleg og reliable leið til að haldbærar búa til skýrslur sem eru rétt gögn.</span><span class="sxs-lookup"><span data-stu-id="0a6f4-108">Using saved settings is a fast and reliable way to consistently generate reports that contain the correct data.</span></span>

<span data-ttu-id="0a6f4-109">Hægt er að skoða vistuð stillingar sem völ er á með í skýrslunni í **Vistuð Stillingar** hluta af síðu skýrslunnar beiðni.</span><span class="sxs-lookup"><span data-stu-id="0a6f4-109">You can see the saved settings that are available to you for a report in **Saved Settings** section of the report request page.</span></span>  

## <a name="to-apply-saved-settings-to-a-report"></a><span data-ttu-id="0a6f4-110">Jafna vistuð stillingar í skýrslu</span><span class="sxs-lookup"><span data-stu-id="0a6f4-110">To apply saved settings to a report</span></span>
1. <span data-ttu-id="0a6f4-111">Viðeigandi skýrsla er opnuð.</span><span class="sxs-lookup"><span data-stu-id="0a6f4-111">Open the report.</span></span>

   <span data-ttu-id="0a6f4-112">Skýrslunni beiðni page birtist.</span><span class="sxs-lookup"><span data-stu-id="0a6f4-112">The report request page appears.</span></span>    
2. <span data-ttu-id="0a6f4-113">Í sem **Vistuð Stillingar** hluta af síðu, setja á **Heiti** á vistuðu stillingar sem á að nota.</span><span class="sxs-lookup"><span data-stu-id="0a6f4-113">In the **Saved Settings** section of the page, set the **Name** field  to the saved settings that you want to use.</span></span>

   <span data-ttu-id="0a6f4-114">Hlutinn **Vistaðar stillingar** birtist eingöngu ef skýrslan hefur verið keyrð áður eða ef fyrir eru vistaðar stillingafærslur.</span><span class="sxs-lookup"><span data-stu-id="0a6f4-114">The **Saved Settings** section only appears if the report has been run before or if there are existing saved settings entries.</span></span> <span data-ttu-id="0a6f4-115">Vistaða stillingafærslan sem kallast **Síðast notaðir valkostir og afmarkanir** er alltaf tiltæk.</span><span class="sxs-lookup"><span data-stu-id="0a6f4-115">The saved settings entry called **Last used options and filters** is always available.</span></span> <span data-ttu-id="0a6f4-116">Þessar stillingar eru kostur og afmörkun gildin sem voru notaðar í síðasta sinn sem keyrslan er í skýrslunni.</span><span class="sxs-lookup"><span data-stu-id="0a6f4-116">These settings are the option and filter values that were used the last time you ran the report.</span></span>

## <a name="administer-saved-report-settings-for-users"></a><span data-ttu-id="0a6f4-117">Séð um vistuðu skýrslu stillingar fyrir notendur</span><span class="sxs-lookup"><span data-stu-id="0a6f4-117">Administer saved report settings for users</span></span>
<span data-ttu-id="0a6f4-118">Ef rétta heimildir, hægt er að skoða, stofna og breyta vistuð stillingar fyrir allar skýrslur fyrir alla notendur í fyrirtækinu.</span><span class="sxs-lookup"><span data-stu-id="0a6f4-118">If you have the proper permissions, you can view, create, and modify the saved settings for all reports for all users in company.</span></span> <span data-ttu-id="0a6f4-119">Hægt er að úthluta vistuð stillingar skýrslu fyrir einstaka notendur eða alla notendur í fyrirtækinu.</span><span class="sxs-lookup"><span data-stu-id="0a6f4-119">You can assign saved settings for a report to individual users or all users in the company.</span></span>

<span data-ttu-id="0a6f4-120">Stjórna er vistuð stillingar úr page 1506 **Skýrslum Stillingar**.</span><span class="sxs-lookup"><span data-stu-id="0a6f4-120">You manage saved settings from page 1506 **Reports Settings**.</span></span> <span data-ttu-id="0a6f4-121">Til að opna þessa síðu, skal velja ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Skýrslustillingar** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="0a6f4-121">To open this page, choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Report Settings**, and then choose the related link.</span></span>

<span data-ttu-id="0a6f4-122">Úr á **Skýrslu Stillingar** er hægt að búa til nýja stillingar í scratch eða er hægt að afrita og breyta þeim stillingar.</span><span class="sxs-lookup"><span data-stu-id="0a6f4-122">From the **Report Settings** page, you can create a new settings from scratch or you can make a copy and modify existing settings.</span></span> <span data-ttu-id="0a6f4-123">Til að breyta valkostum og síum fyrir stillingar skal velja aðgerðina **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="0a6f4-123">To modify the options and filters for a settings, choose the **Edit** action.</span></span>

<span data-ttu-id="0a6f4-124">**Athugasemdir:**</span><span class="sxs-lookup"><span data-stu-id="0a6f4-124">**Notes:**</span></span>

* <span data-ttu-id="0a6f4-125">Aðgerð vistaðra stillinga á skýrslu er aðeins mikilvæg þegar eiginleikarnir SaveValues á beiðnisíðunni er stilltur á „Já“.</span><span class="sxs-lookup"><span data-stu-id="0a6f4-125">The saved settings feature on reports is only relevant when the SaveValues property of the request page is set to Yes.</span></span> <span data-ttu-id="0a6f4-126">SaveValues eiginleika eiginleika er sett í umhverfi þróun.</span><span class="sxs-lookup"><span data-stu-id="0a6f4-126">The SaveValues property property is set in the development environment.</span></span>
* <span data-ttu-id="0a6f4-127">Ef stofnað er vistað stillingaatriði fyrir alla notendur og það hefur sama heiti og fyrirliggjandi vistaðar stillingar fyrir tiltekinn notanda getur sá notandi ekki notað vistuðu stillingarnar sem er úthlutað til allra.</span><span class="sxs-lookup"><span data-stu-id="0a6f4-127">If you create a saved settings item for all users, and it has the same name as an existing saved settings for a specific user, then that user will not be able to use the saved settings that is assigned to everyone.</span></span>  <span data-ttu-id="0a6f4-128">Í reitnum Vistaðar stillingar á beiðnisíðu skýrslunnar sér notandinn tvo valkosti fyrir vistaðar stillingar með sama heiti.</span><span class="sxs-lookup"><span data-stu-id="0a6f4-128">In the Saved Settings field on the report request page, the user will see two saved settings options with the same name.</span></span> <span data-ttu-id="0a6f4-129">Sama hvorn valkostinn hann velur verða vistuðu stillingarnar sem tilgreindar eru fyrir notandann notaðar.</span><span class="sxs-lookup"><span data-stu-id="0a6f4-129">However, no matter which option he chooses, the user-specific saved settings will be used.</span></span>

## <a name="see-also"></a><span data-ttu-id="0a6f4-130">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="0a6f4-130">See Also</span></span>
[<span data-ttu-id="0a6f4-131">Tímasetja keyrslu skýrslu</span><span class="sxs-lookup"><span data-stu-id="0a6f4-131">Schedule a Rpeort to Run</span></span>](ui-schedule-report.md)  

