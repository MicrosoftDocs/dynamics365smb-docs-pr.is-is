---
title: Stjórnun Microsoft Teams samþættingar við Business Central | Microsoft docs
description: Stjórna samþættingu Business Central við Microsoft Teams.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Teams, MS Teams, Microsoft Teams, Skype, Link, Microsoft 365, collaborate, collaboration, teamwork
ms.date: 10/08/2020
ms.author: jswymer
ms.openlocfilehash: 3c04dfb2f77eba906b2567ca9438849e1cc20861
ms.sourcegitcommit: 4bca699d2a5ce182eb5572d72fac4fb478c4f293
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/12/2020
ms.locfileid: "3989359"
---
# <a name="managing-microsoft-teams-integration-with-business-central"></a><span data-ttu-id="0be06-103">Stjórnun Microsoft Teams samþættingar við Business Central</span><span class="sxs-lookup"><span data-stu-id="0be06-103">Managing Microsoft Teams Integration with Business Central</span></span>

[!INCLUDE [teams_preview.md](includes/teams_preview.md)]

<span data-ttu-id="0be06-104">Í þessari grein er að finna yfirlit yfir það sem hægt er að gera sem stjórnandi til að stýra Microsoft Teams samþættingu við [!INCLUDE [prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="0be06-104">This article provides an overview of what you can do as an administrator to control Microsoft Teams integration with [!INCLUDE [prodshort](includes/prodshort.md)].</span></span>

## <a name="in-microsoft-teams"></a><span data-ttu-id="0be06-105">Eftir Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="0be06-105">In Microsoft Teams</span></span>

### <a name="minimum-requirements"></a><span data-ttu-id="0be06-106">Lágmarkskröfur</span><span class="sxs-lookup"><span data-stu-id="0be06-106">Minimum requirements</span></span>

<span data-ttu-id="0be06-107">Í þessum hluta er lýst lágmarkskröfum til að eiginleikar [!INCLUDE [prodshort](includes/prodshort.md)]-forritsins virki í Teams.</span><span class="sxs-lookup"><span data-stu-id="0be06-107">This section describes the minimum requirements for the [!INCLUDE [prodshort](includes/prodshort.md)] app features to work in Teams.</span></span>

- <span data-ttu-id="0be06-108">Nauðsynleg leyfi</span><span class="sxs-lookup"><span data-stu-id="0be06-108">Required licenses</span></span>

    <span data-ttu-id="0be06-109">Eftirfarandi tafla gefur yfirlit yfir leyfin sem þarf til að eiginleikar [!INCLUDE [prodshort](includes/prodshort.md)]-forritsins virki í Teams.</span><span class="sxs-lookup"><span data-stu-id="0be06-109">This table gives you an overview of the licenses needed for the [!INCLUDE [prodshort](includes/prodshort.md)] app features to work in Teams.</span></span>

    |<span data-ttu-id="0be06-110">Hvað</span><span class="sxs-lookup"><span data-stu-id="0be06-110">What</span></span>|<span data-ttu-id="0be06-111">Teams-leyfi</span><span class="sxs-lookup"><span data-stu-id="0be06-111">Teams license</span></span>|<span data-ttu-id="0be06-112">Business Central-leyfi</span><span class="sxs-lookup"><span data-stu-id="0be06-112">Business Central license</span></span>|
    |----|---|---|
    |<span data-ttu-id="0be06-113">Límið tengil við [!INCLUDE [prodshort](includes/prodshort.md)]-færslu í samtal og sendið hann sem spjald.</span><span class="sxs-lookup"><span data-stu-id="0be06-113">Paste a link to a [!INCLUDE [prodshort](includes/prodshort.md)] record into a conversation, and send it as a card.</span></span>|<span data-ttu-id="0be06-114">![gátmerki](media/check.png "ávísun")</span><span class="sxs-lookup"><span data-stu-id="0be06-114">![check mark](media/check.png "check")</span></span>|<span data-ttu-id="0be06-115">![gátmerki](media/check.png "ávísun")</span><span class="sxs-lookup"><span data-stu-id="0be06-115">![check mark](media/check.png "check")</span></span>|
    |<span data-ttu-id="0be06-116">Skoðið spjald [!INCLUDE [prodshort](includes/prodshort.md)]-færslu í samtali.</span><span class="sxs-lookup"><span data-stu-id="0be06-116">View a card of a [!INCLUDE [prodshort](includes/prodshort.md)] record in a conversation.</span></span>|<span data-ttu-id="0be06-117">![gátmerki](media/check.png "ávísun")</span><span class="sxs-lookup"><span data-stu-id="0be06-117">![check mark](media/check.png "check")</span></span>||
    |<span data-ttu-id="0be06-118">Skoðið frekari upplýsingar um spjald fyrir [!INCLUDE [prodshort](includes/prodshort.md)]-færslu í samtali.</span><span class="sxs-lookup"><span data-stu-id="0be06-118">View more details of card for a [!INCLUDE [prodshort](includes/prodshort.md)] record in a conversation.</span></span>|<span data-ttu-id="0be06-119">![gátmerki](media/check.png "ávísun")</span><span class="sxs-lookup"><span data-stu-id="0be06-119">![check mark](media/check.png "check")</span></span>|<span data-ttu-id="0be06-120">![gátmerki](media/check.png "ávísun")</span><span class="sxs-lookup"><span data-stu-id="0be06-120">![check mark](media/check.png "check")</span></span>|

- <span data-ttu-id="0be06-121">Leyfa forskoðanir vefslóða</span><span class="sxs-lookup"><span data-stu-id="0be06-121">Allow URL previews</span></span>

    <span data-ttu-id="0be06-122">Það verður að vera kveikt á reglustillingunni **Leyfa forskoðanir vefslóða** .</span><span class="sxs-lookup"><span data-stu-id="0be06-122">**Allow URL previews** policy setting must be turned on.</span></span> <span data-ttu-id="0be06-123">Annars verður ekki hægt að búa til spjald fyrir tengla Business Central sem límdir eru í samtal í Teams.</span><span class="sxs-lookup"><span data-stu-id="0be06-123">Otherwise, a card can't be generated for Business Central links pasted into a Teams conversation.</span></span> <span data-ttu-id="0be06-124">Frekari upplýsingar um þessa stillingur er að finna í [Stjórna skilaboðareglum í Teams](/microsoftteams/messaging-policies-in-teams).</span><span class="sxs-lookup"><span data-stu-id="0be06-124">For more information about this setting, see [Manage messaging policies in Teams](/microsoftteams/messaging-policies-in-teams).</span></span>

### <a name="managing-the-business-central-app-optional"></a><span data-ttu-id="0be06-125">Stjórnun Business Central (valfrjálst)</span><span class="sxs-lookup"><span data-stu-id="0be06-125">Managing the Business Central app (optional)</span></span>

<span data-ttu-id="0be06-126">Sem stjórnandi í Teams er hægt að stjórna öllum forritum fyrir fyrirtækið, þ.m.t. [!INCLUDE [prodshort](includes/prodshort.md)]-forritinu.</span><span class="sxs-lookup"><span data-stu-id="0be06-126">As a Teams administrator, you can manage all apps for your organization, including the [!INCLUDE [prodshort](includes/prodshort.md)] app.</span></span> <span data-ttu-id="0be06-127">Hægt er að samþykkja eða setja upp [!INCLUDE [prodshort](includes/prodshort.md)]-forritið fyrir fyrirtækið þitt, útiloka notanda frá því að setja upp forritið og fleira.</span><span class="sxs-lookup"><span data-stu-id="0be06-127">You can approve or install the [!INCLUDE [prodshort](includes/prodshort.md)] app for your organization, block user's from installing the app, and more.</span></span>

<span data-ttu-id="0be06-128">Frekari upplýsingar er að finna í eftirfarandi greinum í fylgiskjölum Microsoft Teams:</span><span class="sxs-lookup"><span data-stu-id="0be06-128">For more information, see the following articles in the Microsoft Teams documentation:</span></span>

- [<span data-ttu-id="0be06-129">Stjórna forritunum í Microsoft Teams stjórnendamiðstöðinni</span><span class="sxs-lookup"><span data-stu-id="0be06-129">Manage your apps in the Microsoft Teams admin center</span></span>](https://docs.microsoft.com/MicrosoftTeams/manage-apps)
- [<span data-ttu-id="0be06-130">Stjórna uppsetningarreglum forrits í Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="0be06-130">Manage app setup policies in Microsoft Teams</span></span>](https://docs.microsoft.com/microsoftteams/teams-app-setup-policies)

## <a name="in-prodshort"></a><span data-ttu-id="0be06-131">Eftir [!INCLUDE [prodshort](includes/prodshort.md)]</span><span class="sxs-lookup"><span data-stu-id="0be06-131">In [!INCLUDE [prodshort](includes/prodshort.md)]</span></span>

### <a name="minimum-requirements"></a><span data-ttu-id="0be06-132">Lágmarkskröfur</span><span class="sxs-lookup"><span data-stu-id="0be06-132">Minimum requirements</span></span>

- <span data-ttu-id="0be06-133">útgáfa [!INCLUDE [prodshort](includes/prodshort.md)]:</span><span class="sxs-lookup"><span data-stu-id="0be06-133">[!INCLUDE [prodshort](includes/prodshort.md)] version:</span></span>

    <span data-ttu-id="0be06-134">[!INCLUDE [prodshort](includes/prodshort.md)] 2020 útgáfutímabil 2 (útgáfa 17) eða nýrra.</span><span class="sxs-lookup"><span data-stu-id="0be06-134">[!INCLUDE [prodshort](includes/prodshort.md)] 2020 release wave 2 (version 17) or later.</span></span> <span data-ttu-id="0be06-135">Samþætting Teams er aðeins studd fyrir [!INCLUDE [prodshort](includes/prodshort.md)] á netinu; ekki á staðnum.</span><span class="sxs-lookup"><span data-stu-id="0be06-135">Teams integration is only supported for [!INCLUDE [prodshort](includes/prodshort.md)] online; not on-premises.</span></span>

- <span data-ttu-id="0be06-136">Codeunit: **2718 Þjónustuaðili síðusamantektar** er gefin út sem vefþjónusta:</span><span class="sxs-lookup"><span data-stu-id="0be06-136">Codeunit **2718 Page Summary Provider** is published as a web service:</span></span>

    <span data-ttu-id="0be06-137">Þetta codeunit er gefið út sem vefþjónusta að sjálfgefnu.</span><span class="sxs-lookup"><span data-stu-id="0be06-137">This codeunit is published as a web service by default.</span></span> <span data-ttu-id="0be06-138">Codeunit er hluti af kerfisforriti [!INCLUDE [prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="0be06-138">The codeunit is part of the [!INCLUDE [prodshort](includes/prodshort.md)] system application.</span></span> <span data-ttu-id="0be06-139">Það er notað til að sækja reitargögn fyrir [!INCLUDE [prodshort](includes/prodshort.md)]-síðu sem er bætt við samtal í Teams.</span><span class="sxs-lookup"><span data-stu-id="0be06-139">It's used to get the field data for a [!INCLUDE [prodshort](includes/prodshort.md)] page added to a Teams conversation.</span></span> 

- <span data-ttu-id="0be06-140">Aðgangsheimildir notanda:</span><span class="sxs-lookup"><span data-stu-id="0be06-140">User permissions:</span></span>

    <span data-ttu-id="0be06-141">Að mestu leyti eru síður og gögn sem notendur geta skoðað og breytt í samtali í Teams stjórnað af heimildum þeirra í [!INCLUDE [prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="0be06-141">For the most part, the pages and data that users can view and edit in a Teams conversation is controlled by their permissions in [!INCLUDE [prodshort](includes/prodshort.md)].</span></span>
    
    - <span data-ttu-id="0be06-142">Til að líma [!INCLUDE [prodshort](includes/prodshort.md)]-tengil í samtal í Teams og fá hann til að stækka í spjald, verða notendur að minnsta kosti að hafa lesheimild á síðunni og gögnum hennar.</span><span class="sxs-lookup"><span data-stu-id="0be06-142">To paste a [!INCLUDE [prodshort](includes/prodshort.md)] link into a Teams conversation and have it expand into a card, users must have at least read permission on the page and its data.</span></span>
    - <span data-ttu-id="0be06-143">Þegar spjald er sent inn í samtal, getur hvaða notandi sem er í því samtali skoðað spjaldið án leyfis frá Business Central.</span><span class="sxs-lookup"><span data-stu-id="0be06-143">Once a card is submitted into a conversation, any user in that conversation can view that card without permission to Business Central.</span></span>
    - <span data-ttu-id="0be06-144">Til að skoða frekari upplýsingar um spjald eða opna færsluna í [!INCLUDE [prodshort](includes/prodshort.md)], verða notendur að hafa lesheimild á síðunni og gögnum hennar.</span><span class="sxs-lookup"><span data-stu-id="0be06-144">To view more details for a card or open the record in [!INCLUDE [prodshort](includes/prodshort.md)], users must have read permission on the page and its data.</span></span>
    - <span data-ttu-id="0be06-145">Til að breyta gögnum þarf notandi að breyta heimildum.</span><span class="sxs-lookup"><span data-stu-id="0be06-145">To change data, user's need modify permissions.</span></span>
    
    <span data-ttu-id="0be06-146">Frekari upplýsingar um heimildir er að finna í [Úthluta leyfum til notenda og hópa](ui-define-granular-permissions.md).</span><span class="sxs-lookup"><span data-stu-id="0be06-146">For information about permissions, see [Assign Permissions to Users and Groups](ui-define-granular-permissions.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="0be06-147">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="0be06-147">See Also</span></span>
[<span data-ttu-id="0be06-148">Business Central og Microsoft Teams samþættingaryfirlit</span><span class="sxs-lookup"><span data-stu-id="0be06-148">Business Central and Microsoft Teams Integration Overview</span></span>](across-teams-overview.md)  
<span data-ttu-id="0be06-149">[Setja upp [!INCLUDE [prodshort](includes/prodshort.md)]-forritið fyrir Microsoft Teams](across-install-app-for-teams.md)</span><span class="sxs-lookup"><span data-stu-id="0be06-149">[Install the [!INCLUDE [prodshort](includes/prodshort.md)] App for Microsoft Teams](across-install-app-for-teams.md)</span></span>  
[<span data-ttu-id="0be06-150">Þróun fyrir samþættingu Teams</span><span class="sxs-lookup"><span data-stu-id="0be06-150">Developing for Teams Integration</span></span>](/dynamics365/business-central/dev-itpro/developer/devenv-develop-for-teams)  
[<span data-ttu-id="0be06-151">Hafist handa</span><span class="sxs-lookup"><span data-stu-id="0be06-151">Getting Started</span></span>](product-get-started.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
