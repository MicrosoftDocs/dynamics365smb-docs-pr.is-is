---
title: Jafna og leiðrétta vistaðar stillingar í skýrslum | Microsoft Docs
description: Lýsir því hvernig not skal fyrirfram skilgreinda valmöguleika og afmarkanir til að sérstilla skýrslu, og ná fram réttum upplýsingum.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customization, personalization
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: d61e599b9e86f28de6edcf4ccff5b245503880fe
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/09/2020
ms.locfileid: "3784610"
---
# <a name="manage-saved-settings-for-reports-and-batch-jobs"></a><span data-ttu-id="1829a-103">Stjórna vistuðum stillingum fyrir skýrslur og runuvinnslur</span><span class="sxs-lookup"><span data-stu-id="1829a-103">Manage Saved Settings for Reports and Batch jobs</span></span>
<span data-ttu-id="1829a-104">Þegar skýrslur eru keyrðar er notendum yfirleitt sýnd síða sem gerir þeim kleift að velja valkosti og síur fyrir breytingar á gögnum sem eru í mynduðu skýrslunni.</span><span class="sxs-lookup"><span data-stu-id="1829a-104">When running reports, users are typically presented with a page that lets them select options and set filters to change the data that is included in the generated report.</span></span> <span data-ttu-id="1829a-105">Þessi síða er kölluð beiðnisíða.</span><span class="sxs-lookup"><span data-stu-id="1829a-105">This page is called the request page.</span></span> <span data-ttu-id="1829a-106">Skýrsla getur innihaldið eitt eða fleiri *vistaðar stillingar* sem notendur geta notað á skýrsluna úr beiðnisíðunni.</span><span class="sxs-lookup"><span data-stu-id="1829a-106">A report can include one or more *saved settings* that users can apply to the report from the request page.</span></span> <span data-ttu-id="1829a-107">*Vistuð stillingar* eru skoðaður fyrirfram skilgreind valkosti og afmarkanir.</span><span class="sxs-lookup"><span data-stu-id="1829a-107">*Saved settings* are basically predefined options and filters.</span></span> <span data-ttu-id="1829a-108">Notkun vistaðra stillinga er fljótleg og áreiðanleg leið til að búa til skýrslur sem innihalda rétt gögn.</span><span class="sxs-lookup"><span data-stu-id="1829a-108">Using saved settings is a fast and reliable way to consistently generate reports that contain the correct data.</span></span> <span data-ttu-id="1829a-109">Frekari upplýsingar eru í [Nota vistaðar stillingar](ui-work-report.md#SavedSettings).</span><span class="sxs-lookup"><span data-stu-id="1829a-109">For more information, see [Using Saved Settings](ui-work-report.md#SavedSettings).</span></span>

> [!NOTE]
> <span data-ttu-id="1829a-110">Þetta efnisatriði á að mestu leyti við um „skýrslu“, en svipaðar upplýsingar eiga við um runuvinnslur.</span><span class="sxs-lookup"><span data-stu-id="1829a-110">This topic refers mainly to "report", but similar information applies to batch jobs.</span></span>

<span data-ttu-id="1829a-111">Ef réttar heimildir eru til staðar er hægt að skoða, stofna og breyta vistuðum stillingum fyrir allar skýrslur fyrir alla notendur í fyrirtækinu.</span><span class="sxs-lookup"><span data-stu-id="1829a-111">If you have the proper permissions, you can view, create, and modify the saved settings for all reports for all users in a company.</span></span> <span data-ttu-id="1829a-112">Hægt er að úthluta vistuðum stillingum fyrir skýrslu fyrir einstaka notendur eða alla notendur í fyrirtækinu.</span><span class="sxs-lookup"><span data-stu-id="1829a-112">You can assign saved settings for a report to individual users or to all users in the company.</span></span>

<!--
## Apply saved settings to a report
1. Open the report.

   The request page appears.    
2. In the **Saved Settings** section of the page, set the **Name** field  to the saved settings that you want to use.

   The **Saved Settings** section only appears if the report has been run before or if there are existing saved settings entries. The saved settings entry called **Last used options and filters** is always available. These settings are the option and filter values that were used the last time you ran the report.

-->

## <a name="to-create-and-modify-saved-settings-for-all-users"></a><span data-ttu-id="1829a-113">Til að stofna og breyta vistuðum stillingum fyrir alla notendur</span><span class="sxs-lookup"><span data-stu-id="1829a-113">To create and modify saved settings for all users</span></span>
<span data-ttu-id="1829a-114">Þú hefur umsjón með vistuðum stillingum á síðunni **Stillingar skýrsla**.</span><span class="sxs-lookup"><span data-stu-id="1829a-114">You manage saved settings on the **Reports Settings** page.</span></span> <span data-ttu-id="1829a-115">Tvær aðferðir til að opna þessa síða:</span><span class="sxs-lookup"><span data-stu-id="1829a-115">There are two ways to open this page:</span></span>
-   <span data-ttu-id="1829a-116">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Skýrslustillingar** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="1829a-116">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Report Settings**, and then choose the related link.</span></span>
-   <span data-ttu-id="1829a-117">Opnaðu skýrslu, veldu uppflettingu í **Nota sjálfgildi úr** -svæði og veldu svo aðgerðina **Velja af öllum listanum**.</span><span class="sxs-lookup"><span data-stu-id="1829a-117">Open a report, choose the lookup in the **Use default values from** field, and then choose the **Select from full list** action.</span></span>

<span data-ttu-id="1829a-118">Síðan birtir allar fyrirliggjandi vistaðar stillingafærslur fyrir alla notendur.</span><span class="sxs-lookup"><span data-stu-id="1829a-118">The page displays all the existing saved settings entries for all users.</span></span> <span data-ttu-id="1829a-119">Ef notandanafn er í **Úthlutað til** reitnum getur aðeins sá notandi notað vistuðu stillingarnar fyrir tengda skýrslu.</span><span class="sxs-lookup"><span data-stu-id="1829a-119">If there is a user name in the **Assigned to** field, only that user can use the saved settings for the associated report.</span></span> <span data-ttu-id="1829a-120">Ef gátmerki er í **Deila með öllum notendum** reitnum geta allir notendur notað vistuðu stillingarnar fyrir skýrslu.</span><span class="sxs-lookup"><span data-stu-id="1829a-120">If there is a check mark in the **Share with all users** field, all users can use the saved settings for the report.</span></span>

<span data-ttu-id="1829a-121">Á síðunni **Skýrslustillingar** er hægt að:</span><span class="sxs-lookup"><span data-stu-id="1829a-121">From the **Report Settings** page, you can:</span></span>
-   <span data-ttu-id="1829a-122">Veljið aðgerðina **Nýtt** til að stofna nýja færslu fyrir vistaðar stillingar frá grunni.</span><span class="sxs-lookup"><span data-stu-id="1829a-122">Choose the **New** action to create a new saved settings entry from scratch.</span></span>
-   <span data-ttu-id="1829a-123">Veljið færslu fyrir vistaðar stillingar af listanum og veljið aðgerðina **Afrita** til að búa til afrit.</span><span class="sxs-lookup"><span data-stu-id="1829a-123">Select a saved settings entry from the list, and choose the **Copy** action to create a copy.</span></span>
-   <span data-ttu-id="1829a-124">Veljið færslu fyrir vistaðar stillingar af listanum og veljið aðgerðina **Breyta** til að breyta færslu fyrir vistaðar stillingar.</span><span class="sxs-lookup"><span data-stu-id="1829a-124">Select a saved settings entry from the list, and choose the **Edit** action to modify a saved settings entry.</span></span>

> [!Important]
> <span data-ttu-id="1829a-125">Íhugaðu nafnið sem þú gefur færslu fyrir vistaðar stillingar.</span><span class="sxs-lookup"><span data-stu-id="1829a-125">Consider the name that you give a saved settings entry.</span></span> <span data-ttu-id="1829a-126">Ef þú býrð til færslu fyrir vistaðar stillingar fyrir alla notendur og þú gefur henni sama heiti og fyrirliggjandi færslu fyrir vistaðar stillingar sem er úthlutað á tiltekinn notanda, mun sá notandi ekki geta notað færsluna fyrir vistaðar stillingar sem er úthlutað á alla.</span><span class="sxs-lookup"><span data-stu-id="1829a-126">If you create a saved settings entry for all users, and you give it the same name as an existing saved settings entry that is assigned to a specific user only, then that user will not be able to use the saved settings entry that is assigned to everyone.</span></span>  <span data-ttu-id="1829a-127">Undir **Vistaðar stillingar** á beiðnisíðu skýrslunnar mun notandinn sjá tvær vistaðar stillingar með sama heiti.</span><span class="sxs-lookup"><span data-stu-id="1829a-127">In the **Saved Settings** section on the request page, the user will see two saved settings entries with the same name.</span></span> <span data-ttu-id="1829a-128">Notandaskilgreinda færslan fyrir vistaðar stillingar verður notuð, sama hvor valmöguleikinn er valinn.</span><span class="sxs-lookup"><span data-stu-id="1829a-128">However, no matter which option they choose, the user-specific saved settings entry will be used.</span></span>

> [!NOTE]
> <span data-ttu-id="1829a-129">Aðgerð vistaðra stillinga á skýrslu er aðeins í boði þegar [eiginleikarnir SaveValues](/dynamics365/business-central/dev-itpro/developer/properties/devenv-savevalues-property) á beiðnisíðunni skýrslunnar er stilltur á **Já**.</span><span class="sxs-lookup"><span data-stu-id="1829a-129">The Saved Settings feature is available only on reports where the [SaveValues property](/dynamics365/business-central/dev-itpro/developer/properties/devenv-savevalues-property) of the report's request page is set to **Yes**.</span></span> <span data-ttu-id="1829a-130">**SaveValues** eiginleiki er sett í þróunarumhverfi.</span><span class="sxs-lookup"><span data-stu-id="1829a-130">The **SaveValues** property is set in the development environment.</span></span>  

## <a name="see-also"></a><span data-ttu-id="1829a-131">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="1829a-131">See Also</span></span>
[<span data-ttu-id="1829a-132">Unnið með skýrslur, runuvinnslur og XMLports</span><span class="sxs-lookup"><span data-stu-id="1829a-132">Working with Reports, Batch Jobs, and XMLports</span></span>](ui-work-report.md)  
