---
title: Jafna og leiðrétta vistaðar stillingar í skýrslum | Microsoft Docs
description: Lýsir því hvernig not skal fyrirfram skilgreinda valmöguleika og afmarkanir til að sérstilla skýrslu, og ná fram réttum upplýsingum.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customization, personalization
ms.date: 04/01/2019
ms.author: jswymer
ms.openlocfilehash: 3e7b00d54a9c655a77b7b7f4854e59993866427e
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/29/2019
ms.locfileid: "1251222"
---
# <a name="managing-saved-settings-on-reports"></a><span data-ttu-id="33add-103">Vinna með vistaðar stillingar á skýrslum</span><span class="sxs-lookup"><span data-stu-id="33add-103">Managing Saved Settings on Reports</span></span>
<span data-ttu-id="33add-104">Þegar skýrslur eru keyrðar er notendum yfirleitt sýnd síða sem gerir þeim kleift að velja tiltekna valkosti og afmarkanir fyrir breytingar á gögnum sem eru í mynduðu skýrslunni.</span><span class="sxs-lookup"><span data-stu-id="33add-104">When running a reports, users are typically presented with a page that lets them set certain options and filters for changing the data that is included in the generated report.</span></span> <span data-ttu-id="33add-105">Þessi síða er kölluð beiðnisíða skýrslu.</span><span class="sxs-lookup"><span data-stu-id="33add-105">This page is called the report request page.</span></span> <span data-ttu-id="33add-106">Skýrsla getur innihaldið eitt eða fleiri *vistaðar stillingar* sem notendur geta notað á skýrsluna úr beiðnisíðunni.</span><span class="sxs-lookup"><span data-stu-id="33add-106">A report can include one or more *saved settings* that users can apply to the report from the request page.</span></span> <span data-ttu-id="33add-107">*Vistuð stillingar* eru skoðaður fyrirfram skilgreind valkosti og afmarkanir.</span><span class="sxs-lookup"><span data-stu-id="33add-107">*Saved settings* are basically predefined options and filters.</span></span> <span data-ttu-id="33add-108">Notkun vistaðra stillinga er fljótleg og áreiðanleg leið til að búa til skýrslur sem innihalda rétt gögn.</span><span class="sxs-lookup"><span data-stu-id="33add-108">Using saved settings is a fast and reliable way to consistently generate reports that contain the correct data.</span></span> <span data-ttu-id="33add-109">Nánari upplýsingar um það hvernig vistaðar stillingar eru notaðar eru í [Notkun vistaðra stillinga](ui-work-report.md#SavedSettings).</span><span class="sxs-lookup"><span data-stu-id="33add-109">For more information about how saved settings are used, see [Using Saved Settings](ui-work-report.md#SavedSettings).</span></span>

<span data-ttu-id="33add-110">Ef rétta heimildir, hægt er að skoða, stofna og breyta vistuð stillingar fyrir allar skýrslur fyrir alla notendur í fyrirtækinu.</span><span class="sxs-lookup"><span data-stu-id="33add-110">If you have the proper permissions, you can view, create, and modify the saved settings for all reports for all users in company.</span></span> <span data-ttu-id="33add-111">Hægt er að úthluta vistuð stillingar skýrslu fyrir einstaka notendur eða alla notendur í fyrirtækinu.</span><span class="sxs-lookup"><span data-stu-id="33add-111">You can assign saved settings for a report to individual users or all users in the company.</span></span>

<!--
## Apply saved settings to a report
1. Open the report.

   The report request page appears.    
2. In the **Saved Settings** section of the page, set the **Name** field  to the saved settings that you want to use.

   The **Saved Settings** section only appears if the report has been run before or if there are existing saved settings entries. The saved settings entry called **Last used options and filters** is always available. These settings are the option and filter values that were used the last time you ran the report.

-->

## <a name="create-and-modify-saved-settings-for-all-users"></a><span data-ttu-id="33add-112">Stofna og breyta vistuðum stillingum fyrir alla notendur</span><span class="sxs-lookup"><span data-stu-id="33add-112">Create and modify saved settings for all users</span></span>
<span data-ttu-id="33add-113">Vistuðum stillingum er stjórna af síðu **1560 Stillingar skýrsla**.</span><span class="sxs-lookup"><span data-stu-id="33add-113">You manage saved settings from page **1560 Reports Settings**.</span></span> <span data-ttu-id="33add-114">Tvær aðferðir til að opna þessa síða:</span><span class="sxs-lookup"><span data-stu-id="33add-114">There are two ways to open this page:</span></span>
-   <span data-ttu-id="33add-115">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Skýrslustillingar** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="33add-115">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Report Settings**, and then choose the related link.</span></span>
-   <span data-ttu-id="33add-116">Opnaðu skýrslu, veldu uppflettinguna við hliðina á **Notuð sjálfgildi frá:** reitinn, veldu **Velja af öllum listanum**.</span><span class="sxs-lookup"><span data-stu-id="33add-116">Open a report, choose the lookup next to the **Used default values from:** box, choose **Select from full list**.</span></span>

<span data-ttu-id="33add-117">Síðan birtir allar fyrirliggjandi vistunarstillingafærslur fyrir alla notendur.</span><span class="sxs-lookup"><span data-stu-id="33add-117">The page displays all the existing save settings entries for all users.</span></span> <span data-ttu-id="33add-118">Ef notandanafn er í **Úthlutað til** dálknum getur aðeins sá notandi notað vistuðu stillingarnar fyrir tengda skýrslu.</span><span class="sxs-lookup"><span data-stu-id="33add-118">If there is a user name in the **Assigned to** column, only that user can use the saved settings for the associated report.</span></span> <span data-ttu-id="33add-119">Ef gátmerki er í **Deila með öllum notendum** dálknum geta allir notendur notað vistuðu stillingarnar fyrir skýrslu.</span><span class="sxs-lookup"><span data-stu-id="33add-119">If there is a check mark in the **Share with all users** column, all users can use the saved settings for the report.</span></span>

<span data-ttu-id="33add-120">Á síðunni **Skýrslustillingar** er hægt að:</span><span class="sxs-lookup"><span data-stu-id="33add-120">From the **Report Settings** page, you can:</span></span>
-   <span data-ttu-id="33add-121">Veljið **Nýtt** til að stofna nýja færslu fyrir vistaðar stillingar frá grunni.</span><span class="sxs-lookup"><span data-stu-id="33add-121">Choose **New** to create a new saved settings entry from scratch.</span></span>
-   <span data-ttu-id="33add-122">Veljið færslu fyrir vistaðar stillingar af listanum og veljið **Afrita** til að búa til afrit.</span><span class="sxs-lookup"><span data-stu-id="33add-122">Select a saved settings entry from the list, and choose **Copy** to create a copy.</span></span>
-   <span data-ttu-id="33add-123">Veljið færslu fyrir vistaðar stillingar af listanum og veljið **Breyta** til að breyta færslu fyrir vistaðar stillingar.</span><span class="sxs-lookup"><span data-stu-id="33add-123">Select a saved settings entry from the list, and choose **Edit** to modify a saved settings entry.</span></span>


> [!Important]
> <span data-ttu-id="33add-124">Íhugaðu nafnið sem þú gefur færslu fyrir vistaðar stillingar.</span><span class="sxs-lookup"><span data-stu-id="33add-124">Consider the name that you give a saved settings entry.</span></span> <span data-ttu-id="33add-125">Ef þú býrð til færslu fyrir vistaðar stillingar fyrir alla notendur og þú gefur henni sama heiti og fyrirliggjandi færslu fyrir vistaðar stillingar sem er úthlutað á tiltekinn notanda, mun sá notandi ekki geta notað færsluna fyrir vistaðar stillingar sem er úthlutað á alla.</span><span class="sxs-lookup"><span data-stu-id="33add-125">If you create a saved settings entry for all users, and you give it the same name as an existing saved settings entry that is assigned to a specific user only, then that user will not be able to use the saved settings entry that is assigned to everyone.</span></span>  <span data-ttu-id="33add-126">Undir **Vistaðar stillingar** á beiðnisíðu skýrslunnar mun notandinn sjá tvær vistaðar stillingar með sama heiti.</span><span class="sxs-lookup"><span data-stu-id="33add-126">Under **Saved Settings** on the report request page, the user will see two saved settings entries with the same name.</span></span> <span data-ttu-id="33add-127">Hins vegar, sama hvorn valmöguleikann hann velur, verður notandaskilgreinda færslan fyrir vistaðar stillingar notuð.</span><span class="sxs-lookup"><span data-stu-id="33add-127">However, no matter which option he chooses, the user-specific saved settings entry will be used.</span></span>

> [!NOTE]
> <span data-ttu-id="33add-128">Aðgerð vistaðra stillinga á skýrslu er aðeins í boði þegar [eiginleikarnir SaveValues](https://docs.microsoft.com/en-us/dynamics-nav/savevalues-property) á beiðnisíðunni skýrslunnar er stilltur á `Yes`.</span><span class="sxs-lookup"><span data-stu-id="33add-128">The saved settings feature is available only on reports where the [SaveValues property](https://docs.microsoft.com/en-us/dynamics-nav/savevalues-property) of the report's request page is set to `Yes`.</span></span> <span data-ttu-id="33add-129">**SaveValues** eiginleiki er sett í þróunarumhverfi.</span><span class="sxs-lookup"><span data-stu-id="33add-129">The **SaveValues** property is set in the development environment.</span></span>  

## <a name="see-also"></a><span data-ttu-id="33add-130">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="33add-130">See Also</span></span>
[<span data-ttu-id="33add-131">Unnið með skýrslur og runuvinnslur</span><span class="sxs-lookup"><span data-stu-id="33add-131">Working with Reports and Batch Jobs</span></span>](ui-work-report.md)  
