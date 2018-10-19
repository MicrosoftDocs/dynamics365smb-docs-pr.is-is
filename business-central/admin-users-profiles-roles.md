---
title: "Meðhöndla notendur og hlutverk | Microsoft Docs"
description: "Lærið að meðhöndla notendur og Mitt hlutverk í Business Central."
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: profiles, users
ms.date: 10/01/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 1a94d023424c6eceb93af6e9ca89a90a3a94e996
ms.contentlocale: is-is
ms.lasthandoff: 09/28/2018

---
# <a name="understanding-users-profiles-and-role-centers"></a><span data-ttu-id="996bd-103">Að skilja notendur, forstillingar og Mitt hlutverk</span><span class="sxs-lookup"><span data-stu-id="996bd-103">Understanding Users, Profiles, and Role Centers</span></span>

<span data-ttu-id="996bd-104">Í [!INCLUDE[d365fin](includes/d365fin_md.md)], eru notendum bætt við af stjórnanda sem gefur einnig notendum aðgang að þeim svæðum [!INCLUDE[d365fin](includes/d365fin_md.md)] sem þeir þurfa í starfi sínu.</span><span class="sxs-lookup"><span data-stu-id="996bd-104">In [!INCLUDE[d365fin](includes/d365fin_md.md)], users are added by an administrator who also gives users access to the areas of [!INCLUDE[d365fin](includes/d365fin_md.md)] that they need in their work.</span></span>  

<span data-ttu-id="996bd-105">Aðgangur að virkni er stjórnað með *notendahópum* og *notandasíðum*.</span><span class="sxs-lookup"><span data-stu-id="996bd-105">Access to functionality is managed through *user groups* and *profiles*.</span></span> <span data-ttu-id="996bd-106">Sem stjórnandi geturðu bætt við og fjarlægt notendur sem hluta af [!INCLUDE[d365fin](includes/d365fin_md.md)] áskrift þinni og þú getur úthlutað leyfum til notenda í gegnum notendaflokka.</span><span class="sxs-lookup"><span data-stu-id="996bd-106">As an administrator, you can add and remove users as part of your [!INCLUDE[d365fin](includes/d365fin_md.md)] subscription, and you can assign users permissions through user groups.</span></span>  

## <a name="adding-users"></a><span data-ttu-id="996bd-107">Bæta við notendum</span><span class="sxs-lookup"><span data-stu-id="996bd-107">Adding Users</span></span>

<span data-ttu-id="996bd-108">Til að bæta við notendum í [!INCLUDE[d365fin](includes/d365fin_md.md)] á netinu, verður stjórnandi Office 365 í fyrirtækinu fyrst að búa til notendur í Office 365 stjórnendamiðstöðinni.</span><span class="sxs-lookup"><span data-stu-id="996bd-108">To add users in [!INCLUDE[d365fin](includes/d365fin_md.md)] online, your company's Office 365 administrator must first create the users in the Office 365 Admin Center.</span></span> <span data-ttu-id="996bd-109">Frekari upplýsingar, sjá [Bæta notendum við Office 365 for business](https://aka.ms/CreateOffice365Users).</span><span class="sxs-lookup"><span data-stu-id="996bd-109">For more information, see [Add Users to Office 365 for business](https://aka.ms/CreateOffice365Users).</span></span>

<span data-ttu-id="996bd-110">Síðan getur kerfisstjórinn úthlutað sérhverjum notanda og flokkum notenda leyfi.</span><span class="sxs-lookup"><span data-stu-id="996bd-110">Then, the administrator can assign permissions to each user and groups of users.</span></span> <span data-ttu-id="996bd-111">Frekari upplýsingar eru í [Stjórna notendum og heimildum](ui-how-users-permissions.md).</span><span class="sxs-lookup"><span data-stu-id="996bd-111">For more information, see [Managing Users and Permissions](ui-how-users-permissions.md).</span></span>  

### <a name="users-of-on-premises-deployments"></a><span data-ttu-id="996bd-112">Notendur uppsetningar á staðnum</span><span class="sxs-lookup"><span data-stu-id="996bd-112">Users of on-premises deployments</span></span>

<span data-ttu-id="996bd-113">Fyrir uppsetningu á staðnum fyrir [!INCLUDE[d365fin](includes/d365fin_md.md)] getur stjórnandi valið á milli mismunandi auðkenningarbúnaðs skilríkja fyrir notendur.</span><span class="sxs-lookup"><span data-stu-id="996bd-113">For on-premises deployments of [!INCLUDE[d365fin](includes/d365fin_md.md)], the administrator can choose between different credential authorization mechanisms for users.</span></span> <span data-ttu-id="996bd-114">Þegar þú býrð til notanda gefur þú síðan mismunandi upplýsingar eftir því hvaða skilríki þú notar í tilteknu [!INCLUDE[server](includes/server.md)] tilviki.</span><span class="sxs-lookup"><span data-stu-id="996bd-114">Then, when you create a user, you provide different information depending on the credential type that you are using in the specific [!INCLUDE[server](includes/server.md)] instance.</span></span> <span data-ttu-id="996bd-115">Nánari upplýsingar er að finna í [Gerðir auðkenningar og persónuskilríkja](/dynamics365/business-central/dev-itpro/administration/users-credential-types) í stjórnunarhluta þróunaraðila og ITPro efni fyrir [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="996bd-115">For more information, see the [Authentication and Credential Types](/dynamics365/business-central/dev-itpro/administration/users-credential-types) in the Administration section of the developer and ITPro content for [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  

## <a name="profiles"></a><span data-ttu-id="996bd-116">Forstillingar</span><span class="sxs-lookup"><span data-stu-id="996bd-116">Profiles</span></span>

<span data-ttu-id="996bd-117">Fólkið í þínu fyrirtæki sem hefur aðgang að [!INCLUDE[d365fin](includes/d365fin_md.md)] er öllum úthlutað *Forstilling* sem veitir þeim aðgang að *Hlutverkamiðstöð*.</span><span class="sxs-lookup"><span data-stu-id="996bd-117">The people in your company who have access to [!INCLUDE[d365fin](includes/d365fin_md.md)] are all assigned a *profile* that gives them access to a *Role Center*.</span></span>

<span data-ttu-id="996bd-118">Forstillingar eru söfn [!INCLUDE[d365fin](includes/d365fin_md.md)] notenda sem hafa sömu hlutverkamiðstöð (Mitt hlutverk).</span><span class="sxs-lookup"><span data-stu-id="996bd-118">Profiles are collections of [!INCLUDE[d365fin](includes/d365fin_md.md)] users who share the same Role Center.</span></span> <span data-ttu-id="996bd-119">Hlutverkamiðstöð er aðgangsstaður og heimasíða fyrir [!INCLUDE[d365fin](includes/d365fin_md.md)] sem gefur þér skjótan aðgang að mikilvægustu verkum þínum og birtir ýmsar innsýnir og afkastavísa um vinnu þína.</span><span class="sxs-lookup"><span data-stu-id="996bd-119">A Role Center is the entry point and home page for [!INCLUDE[d365fin](includes/d365fin_md.md)] that gives you quick access to your most important tasks and displays various insights and key performance indicators (KPIs) about your work.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="996bd-120">Í núverandi útgáfu af [!INCLUDE[d365fin](includes/d365fin_md.md)] á netinu, er ekki hægt að bæta við, breyta eða eyða snið.</span><span class="sxs-lookup"><span data-stu-id="996bd-120">In the current version of [!INCLUDE[d365fin](includes/d365fin_md.md)] online, you cannot add, edit, or delete profiles.</span></span>  

## <a name="configuration-and-personalization"></a><span data-ttu-id="996bd-121">Grunnstilling og sérstillingar</span><span class="sxs-lookup"><span data-stu-id="996bd-121">Configuration and Personalization</span></span>
<!--The concept of UI customization in [!INCLUDE[d365fin](includes/d365fin_md.md)] is divided in two:  

-   Configuration, performed by the administrator  

-   Personalization, performed by users  

The administrator configures the user interface for multiple users by customizing the user interface for a profile that the users are assigned to.  -->
<span data-ttu-id="996bd-122">Notendur sérsníða notendaviðmót sinnar útgáfu með því að sérsníða notendaviðmót undir eigin notandinafni.</span><span class="sxs-lookup"><span data-stu-id="996bd-122">Users personalize the user interface of their personal version by customizing the user interface under their own user logon.</span></span> <span data-ttu-id="996bd-123">Stjórnandinn getur eytt þessari aðlögun.</span><span class="sxs-lookup"><span data-stu-id="996bd-123">This personalization can be deleted by the administrator.</span></span> <span data-ttu-id="996bd-124">Frekari upplýsingar eru í [Sérstilling vinnusvæðisins þíns](ui-personalization-user.md).</span><span class="sxs-lookup"><span data-stu-id="996bd-124">For more information, see [Personalizing Your Workspace](ui-personalization-user.md).</span></span>  

## <a name="see-also"></a><span data-ttu-id="996bd-125">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="996bd-125">See Also</span></span>  
[<span data-ttu-id="996bd-126">Vinna með notendur og heimildir</span><span class="sxs-lookup"><span data-stu-id="996bd-126">Managing Users and Permissions</span></span>](ui-how-users-permissions.md)  
[<span data-ttu-id="996bd-127">Stjórnun sérstillinga sem stjórnandi</span><span class="sxs-lookup"><span data-stu-id="996bd-127">Managing Personalization as an Administrator</span></span>](ui-personalization-manage.md)  
[<span data-ttu-id="996bd-128">Sérstillingar verksvæðis</span><span class="sxs-lookup"><span data-stu-id="996bd-128">Personalizing Your Workspace</span></span>](ui-personalization-user.md)  

