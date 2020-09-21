---
title: Sérsníða síður fyrir hlutverk | Microsoft Docs
description: Kynntu þér hvernig á að sérsníða notandaviðmótið fyrir forstillingu (hlutverk) þannig að allir notendur þess sjái sérsniðið vinnusvæði.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customize, personalize, personalization, hide columns, remove fields, move fields
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: cee71cea69468a45b2e731632fce3827c54794c1
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/09/2020
ms.locfileid: "3781336"
---
# <a name="customize-pages-for-profiles"></a><span data-ttu-id="d754c-103">Sérsníða síður fyrir forstillingar</span><span class="sxs-lookup"><span data-stu-id="d754c-103">Customize Pages for Profiles</span></span>
<span data-ttu-id="d754c-104"> Notendur geta sérstillt síður vinnusvæðisins síns sitt að vild.</span><span class="sxs-lookup"><span data-stu-id="d754c-104">Users can personalize pages that make up their workspace to suit their own preferences.</span></span> <span data-ttu-id="d754c-105">Frekari upplýsingar eru í [Sérstilling verksvæðis](ui-personalization-user.md).</span><span class="sxs-lookup"><span data-stu-id="d754c-105">For more information, see [Personalize Your Workspace](ui-personalization-user.md).</span></span>

<span data-ttu-id="d754c-106">Stjórnendur geta sérstillt síður fyrir forstillingu samkvæmt tengdri viðskiptahlutverki eða deild, til dæmis, þannig að allir notendur sem hafa úthlutað forstillingunni sjái sérstillt síðuútlit.</span><span class="sxs-lookup"><span data-stu-id="d754c-106">Administrators can customize pages for a profile, according to the related business role or department, for example, so that all users that are assigned the profile will see the customized page layout.</span></span> <span data-ttu-id="d754c-107">Stjórnandinn sérstillir síður með því að nota sömu virkni og notendur gera þegar þeir sérstilla síður.</span><span class="sxs-lookup"><span data-stu-id="d754c-107">The administrator customizes pages by using the same functionality as users do when they personalize pages.</span></span>

> [!NOTE]
> <span data-ttu-id="d754c-108">Dæmigerð notkun forstillingar er hlutverk.</span><span class="sxs-lookup"><span data-stu-id="d754c-108">The typical business use of a profile is a role.</span></span> <span data-ttu-id="d754c-109">Forstilling er því heitið *Forstilling (hlutverk)* í notendaviðmóti.</span><span class="sxs-lookup"><span data-stu-id="d754c-109">A profile is therefore named *Profile (Role)* in the UI.</span></span>

<span data-ttu-id="d754c-110">Sérstilling á síðu hefst á síðunni **Forstillingar (hlutverk)**, upphafspunkt stjórnanda til að stjórna notendaforstillingum á einstökum forstillingarspjöldum.</span><span class="sxs-lookup"><span data-stu-id="d754c-110">Page customization starts from the **Profiles (Roles)** page, the administrator's starting point for managing users' profiles on individual profile cards.</span></span> <span data-ttu-id="d754c-111">Auk þess að sérsníða síðuútlitið er hægt að breyta ýmsum öðrum stillingum fyrir forstillingar á síðunni **Sérstilling (hlutverk)** fyrir hverja forstillingu.</span><span class="sxs-lookup"><span data-stu-id="d754c-111">In addition to customizing the page layout, you control various other settings for profiles on the **Profile (Role)** page for each profile.</span></span> <span data-ttu-id="d754c-112">Frekari upplýsingar eru í [Unnið með forstillingar](admin-users-profiles-roles.md).</span><span class="sxs-lookup"><span data-stu-id="d754c-112">For more information, see [Manage Profiles](admin-users-profiles-roles.md).</span></span>

## <a name="to-customize-pages-for-a-profile"></a><span data-ttu-id="d754c-113">Til að sérsníða síður fyrir forstillingu</span><span class="sxs-lookup"><span data-stu-id="d754c-113">To customize pages for a profile</span></span>
1. <span data-ttu-id="d754c-114">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Forstillingar (hlutverk)** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="d754c-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Profiles (Roles)**, and then choose the related link.</span></span>
2. <span data-ttu-id="d754c-115">Velja skal línuna fyrir forstillinguna sem á að sérsníða síður fyrir og síðan velja aðgerðina **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="d754c-115">Select the line for the profile that you want to customize pages for, and then choose the **Edit** action.</span></span>
3. <span data-ttu-id="d754c-116">Veldu **Sérsníða síður** aðgerðina.</span><span class="sxs-lookup"><span data-stu-id="d754c-116">Choose the **Customize pages** action.</span></span>

    [!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="d754c-117">opnast í nýjum vafraglugga fyrir valda forstillingu með borðanum **Sérstilla**.</span><span class="sxs-lookup"><span data-stu-id="d754c-117">opens on a new browser tab for the selected profile with the **Customizing** banner activated.</span></span> <span data-ttu-id="d754c-118">Borðinn **Sérsníða** býður upp á sömu virkni og borðinn **Sérstilling** sem er aðgengilegur notendum.</span><span class="sxs-lookup"><span data-stu-id="d754c-118">The **Customizing** banner offers the same functionality as the **Personalizing** banner that is available to users.</span></span>

4. <span data-ttu-id="d754c-119">Sérstilla síður í samræmi við þarfir hlutverks eða deildarinnar sem um ræðir á sama hátt og notandi myndi gera þegar hann sérstillir.</span><span class="sxs-lookup"><span data-stu-id="d754c-119">Customize pages according to the needs of the role or department in question in the same way as a user would do when personalizing.</span></span> <span data-ttu-id="d754c-120">Frekari upplýsingar eru í [Sérstilling verksvæðis](ui-personalization-user.md).</span><span class="sxs-lookup"><span data-stu-id="d754c-120">For more information, see [Personalize Your Workspace](ui-personalization-user.md).</span></span>

    > [!NOTE]
    > <span data-ttu-id="d754c-121">Til að skoða á meðan sérstillingu stendur skal nota Ctrl + Smella á aðgerð þegar hún er auðkennd með bendlinum.</span><span class="sxs-lookup"><span data-stu-id="d754c-121">To navigate during personalization, use Ctrl + Click on an action if it is highlighted by the arrowhead.</span></span>

5. <span data-ttu-id="d754c-122">Þegar lokið er við að breyta útlitinu á einni eða fleiri síðum skal velja hnappinn **Lokið** á borðanum **Sérsníða** .</span><span class="sxs-lookup"><span data-stu-id="d754c-122">When you have finished changing the layout on one or more pages, choose the **Done** button on the **Customizing** banner.</span></span>
6. <span data-ttu-id="d754c-123">Lokið vafraglugganum.</span><span class="sxs-lookup"><span data-stu-id="d754c-123">Close the browser tab.</span></span>

<span data-ttu-id="d754c-124">Sérstillingar fyrir síður er nú skráðar fyrir forstillinguna.</span><span class="sxs-lookup"><span data-stu-id="d754c-124">The customization of pages is now recorded for the profile.</span></span>

## <a name="to-view-all-customized-pages-for-a-profile"></a><span data-ttu-id="d754c-125">Til að skoða allar sérstilltar síður fyrir forstillingu</span><span class="sxs-lookup"><span data-stu-id="d754c-125">To view all customized pages for a profile</span></span>
<span data-ttu-id="d754c-126">Hægt er að fá yfirlit yfir hvaða síður eru sérsniðnar fyrir forstillingu, til dæmis til að áætla hver á að sérsníða eða eyða.</span><span class="sxs-lookup"><span data-stu-id="d754c-126">You can get an overview of which pages are customized for a profile, for example to plan which to customize further or delete.</span></span>

- <span data-ttu-id="d754c-127">Á síðunni **Forstilling (hlutverk)** er hægt að velja aðgerðina **Sérsníða síður**.</span><span class="sxs-lookup"><span data-stu-id="d754c-127">On the **Profile (Role)** page, choose the **Customized Pages** action.</span></span>

## <a name="to-delete-all-customizations-for-a-profile"></a><span data-ttu-id="d754c-128">Til að eyða öllum sérstillingum fyrir forstillingu</span><span class="sxs-lookup"><span data-stu-id="d754c-128">To delete all customizations for a profile</span></span>
<span data-ttu-id="d754c-129">Hægt er að hætta við sérstillingar sem þú hefur gert fyrir forstillingu.</span><span class="sxs-lookup"><span data-stu-id="d754c-129">You can cancel all customizations that you have made for a profile.</span></span> <span data-ttu-id="d754c-130">Sérstillingum sem notandi hefur sett inn með viðbót og sérstillingum sem notanda hefur gert verður ekki eytt.</span><span class="sxs-lookup"><span data-stu-id="d754c-130">Customizations introduced with an extension and personalizations made by a user will not be deleted.</span></span> <span data-ttu-id="d754c-131">Hægt er að eyða öllum sérstillingum með annarri aðgerð.</span><span class="sxs-lookup"><span data-stu-id="d754c-131">You can delete all personalizations with another action.</span></span> <span data-ttu-id="d754c-132">Frekari upplýsingar er að finna á [Eyða öllum sérstillingum sem notandi hefur gert](admin-users-profiles-roles.md#to-delete-all-personalizations-made-by-a-user).</span><span class="sxs-lookup"><span data-stu-id="d754c-132">For more information, see [To delete all personalizations made by a user](admin-users-profiles-roles.md#to-delete-all-personalizations-made-by-a-user).</span></span>

- <span data-ttu-id="d754c-133">Á síðunni **Forstilling (hlutverk)** fyrir sérstillta forstillingu skal velja aðgerðina **Hreinsa sérstilltar síður**.</span><span class="sxs-lookup"><span data-stu-id="d754c-133">On the **Profile (Role)** page for a customized profile, choose the **Clear customized pages** action.</span></span>

<span data-ttu-id="d754c-134">Útlitið á síðum fyrir forstillinguna er endurstillt á sjálfgefið útlit.</span><span class="sxs-lookup"><span data-stu-id="d754c-134">The layout on pages for the profile is reset to the default layout.</span></span>  

## <a name="to-delete-customization-for-specific-pages-for-a-profile"></a><span data-ttu-id="d754c-135">Til að eyða sérstillingum fyrir tilteknar síður forstillingar</span><span class="sxs-lookup"><span data-stu-id="d754c-135">To delete customization for specific pages for a profile</span></span>
<span data-ttu-id="d754c-136">Hægt er að eyða einstökum sérstillingum síðu sem hafa verið gerðar fyrir forstillingu.</span><span class="sxs-lookup"><span data-stu-id="d754c-136">You can delete individual page customizations that you have made for a profile.</span></span> <span data-ttu-id="d754c-137">Sérstillingum sem notandi hefur sett inn með viðbót og sérstillingum sem notanda hefur gert verður ekki eytt.</span><span class="sxs-lookup"><span data-stu-id="d754c-137">Customizations introduced with an extension and personalizations made by a user will not be deleted.</span></span> <span data-ttu-id="d754c-138">Hægt er að eyða tilteknum sérstillingum síðu með annarri aðgerð.</span><span class="sxs-lookup"><span data-stu-id="d754c-138">You can delete specific page personalizations with another action.</span></span> <span data-ttu-id="d754c-139">Frekari upplýsingar er að finna á [Eyða sérstillingum fyrir tilteknar síður](admin-users-profiles-roles.md#to-delete-personalizations-for-specific-pages).</span><span class="sxs-lookup"><span data-stu-id="d754c-139">For more information, see [To delete personalizations for specific pages](admin-users-profiles-roles.md#to-delete-personalizations-for-specific-pages).</span></span>

1. <span data-ttu-id="d754c-140">Á síðunni **Forstilling (hlutverk)** er hægt að velja aðgerðina **Sérsníða síður**.</span><span class="sxs-lookup"><span data-stu-id="d754c-140">On the **Profile (Role)** page, choose the **Customized Pages** action.</span></span>
2. <span data-ttu-id="d754c-141">Á síðunni **Sérstillingar forstillingar** skal velja á eða fleiri línur fyrir sérstillingar síðu sem á að eyða og velja svo aðgerðina **Eyða**.</span><span class="sxs-lookup"><span data-stu-id="d754c-141">On the **Profile Customizations** page, select on or more lines for page customizations that you want to delete, and then choose the **Delete** action.</span></span>

<span data-ttu-id="d754c-142">Útlitinu á völdum síðum er breytt í breytingar sem gerðar voru.</span><span class="sxs-lookup"><span data-stu-id="d754c-142">The layout on the selected pages is adjusted to the changes you made.</span></span>

## <a name="see-also"></a><span data-ttu-id="d754c-143">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="d754c-143">See Also</span></span>
[<span data-ttu-id="d754c-144">Sérstilling verksvæðis</span><span class="sxs-lookup"><span data-stu-id="d754c-144">Personalize Your Workspace</span></span>](ui-personalization-user.md)  
[<span data-ttu-id="d754c-145">Vinna með forstillingar</span><span class="sxs-lookup"><span data-stu-id="d754c-145">Manage Profiles</span></span>](admin-users-profiles-roles.md)  
[<span data-ttu-id="d754c-146">Grunnstillingum breytt</span><span class="sxs-lookup"><span data-stu-id="d754c-146">Change Basic Settings</span></span>](ui-change-basic-settings.md)  
[<span data-ttu-id="d754c-147">Breyta því hvaða eiginleikar eru sýndir</span><span class="sxs-lookup"><span data-stu-id="d754c-147">Change Which Features are Displayed</span></span>](ui-experiences.md)  
<span data-ttu-id="d754c-148">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="d754c-148">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
