---
title: Af hverju get ég ekki sérsniðið síðu
description: Útskýrir hvers vegna þú getur ekki sérstillt síðu og hvað þú getur gert til að opna hana svo þú getir sérsniðið hana.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customize, personalize, personalization, hide columns, remove fields, move fields
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 8fd90f7bf90209496f67d52ab32a93cfdbaf803f
ms.sourcegitcommit: 652e4b0e1a09bff265014d9f8eb3b038ab0db79e
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/21/2021
ms.locfileid: "6087645"
---
# <a name="why-a-page-is-locked-from-personalization"></a><span data-ttu-id="e1b75-103">Af hverju er síða læst og því ekki hægt að sérsníða hana</span><span class="sxs-lookup"><span data-stu-id="e1b75-103">Why a Page is Locked from Personalization</span></span>

<span data-ttu-id="e1b75-104">Það eru tvö skilyrði sem koma í veg fyrir að þú sérsníðir síðu.</span><span class="sxs-lookup"><span data-stu-id="e1b75-104">There are two conditions that prevent you from personalizing a page.</span></span> <span data-ttu-id="e1b75-105">Annaðhvort er síðan læst (eins og kemur fram í ![Sérstilla lás](media/personalization-lock-icon.png "Sérstilla lás")) tákninu eða hún er útilokuð (eins og kemur fram í ![Sérstilling útilokuð](media/personalization-blocked-icon.png "Sérstilling útilokuð") tákninu).</span><span class="sxs-lookup"><span data-stu-id="e1b75-105">Either the page is locked (as indicated by the ![Personalize Lock](media/personalization-lock-icon.png "Personalize lock")) icon or it is blocked (as indicated by the ![Personalization blocked](media/personalization-blocked-icon.png "Personalization blocked") icon).</span></span>

## <a name="locked-from-personalizing"></a><span data-ttu-id="e1b75-106">Læst fyrir sérstillingar</span><span class="sxs-lookup"><span data-stu-id="e1b75-106">Locked from Personalizing</span></span>

<span data-ttu-id="e1b75-107">Ef táknið ![Sérstilla lás](media/personalization-lock-icon.png "Sérstilla lás") í borðanum **Sérstilling** þegar síða er opnuð merkir það að þú getir ekki gert neinar breytingar á sérstillingu síðunnar.</span><span class="sxs-lookup"><span data-stu-id="e1b75-107">If there is a ![Personalize Lock](media/personalization-lock-icon.png "Personalize lock") icon in the **Personalizing** banner when you open a page, this means that you are currently prevented from making any more personalization changes to the page.</span></span>

<!-- This is because we changed the way personalization works behind the scenes since the last time that you personalized the page. Unfortunately, the old way and new of doing things do not work together.

The page currently includes the last personalization changes that you made. If you want to continue personalizing the page, then you can choose the lock icon and then **Unlock**. Just be aware that if you choose to unlock the page, the current personalization of the page will be cleared, and you will have to start from scratch.
-->

<span data-ttu-id="e1b75-108">Það kunna að vera tvær ástæður fyrir þessu:</span><span class="sxs-lookup"><span data-stu-id="e1b75-108">There can be two reasons for this:</span></span>

1. <span data-ttu-id="e1b75-109">Þú hefur sérstillt síðuna áður, en það var gert með eldri útgáfu af vörunni.</span><span class="sxs-lookup"><span data-stu-id="e1b75-109">You have personalized the page before, but it was done using an earlier version of the product.</span></span> <span data-ttu-id="e1b75-110">Við breyttum því hvernig sérstilling virkar frá því að þú sérstilltir síðuna síðast.</span><span class="sxs-lookup"><span data-stu-id="e1b75-110">We changed the way personalization works behind the scenes since the last time that you personalized the page.</span></span> <span data-ttu-id="e1b75-111">Því miður vinnur gamla og nýja aðferðin ekki saman.</span><span class="sxs-lookup"><span data-stu-id="e1b75-111">Unfortunately, the old way and new way of doing things do not work together.</span></span>

2. <span data-ttu-id="e1b75-112">Hingað til hefur þú aðeins notað [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)] til að sérsníða síðuna.</span><span class="sxs-lookup"><span data-stu-id="e1b75-112">Until now, you have only used the [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)] to personalize the page.</span></span>

### <a name="unlocking-the-page"></a><span data-ttu-id="e1b75-113">Síða aflæst</span><span class="sxs-lookup"><span data-stu-id="e1b75-113">Unlocking the Page</span></span>

<span data-ttu-id="e1b75-114">Ef þú vilt taka síðu úr lás og halda áfram að sérstilla hana skaltu velja táknið ![Sérstilla lás](media/personalization-lock-icon.png "Sérstilla lás") og síðan aðgerðina **Taka úr lás**.</span><span class="sxs-lookup"><span data-stu-id="e1b75-114">If you want to unlock a page and continue personalizing it, choose the ![Personalize Lock](media/personalization-lock-icon.png "Personalize lock") icon, and then choose the **Unlock** action.</span></span>  

<span data-ttu-id="e1b75-115">Áður en síða er tekin úr lás skal hafa eftirfarandi í huga:</span><span class="sxs-lookup"><span data-stu-id="e1b75-115">Before you unlock the page, be aware of the following:</span></span>

- <span data-ttu-id="e1b75-116">Núverandi sérstilling á síðunni verður hreinsuð.</span><span class="sxs-lookup"><span data-stu-id="e1b75-116">The current personalization of the page will be cleared.</span></span> <span data-ttu-id="e1b75-117">Síðan mun fara aftur í upprunalegt útlit og þú verður að byrja frá byrjun.</span><span class="sxs-lookup"><span data-stu-id="e1b75-117">The page will go back to its original layout, and you will have to start from scratch.</span></span>

- <span data-ttu-id="e1b75-118">Í [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)], mun síðan vera eins og hún er og verður ekki fyrir áhrifum frá nýjum breytingum sérstillinga sem gerðar eru í biðlara Business Central.</span><span class="sxs-lookup"><span data-stu-id="e1b75-118">In the [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)], the page will remain as-is and will not be affected by the new personalization changes made in the Business Central client.</span></span> <span data-ttu-id="e1b75-119">Í áframhaldinu verður sérstilling í [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)] og Business Central biðlara aðskilin að fullu hvort frá öðru.</span><span class="sxs-lookup"><span data-stu-id="e1b75-119">Going forward, the personalization in the [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)] and Business Central client will be completely separate from each other.</span></span>

## <a name="blocked-from-personalizing"></a><span data-ttu-id="e1b75-120">Lokað fyrir sérstillingar</span><span class="sxs-lookup"><span data-stu-id="e1b75-120">Blocked from Personalizing</span></span>

<span data-ttu-id="e1b75-121">Ef táknið ![Sérstilling útilokuð](media/personalization-blocked-icon.png "Sérstilling útilokuð") í borðanum **Sérstilling** merkir það að þú getir ekki gert neinar sérstillingar á síðunni.</span><span class="sxs-lookup"><span data-stu-id="e1b75-121">If there is a ![Personalization blocked](media/personalization-blocked-icon.png "Personalization blocked") icon in the **Personalizing** banner, this means that you are blocked from doing any personalization to the page.</span></span>

<!-- Only text is translated, so removing this image for non-English UX reasons.  ![Personalize blocked](media/personalization-blocked.png "Personalize lock") -->

<span data-ttu-id="e1b75-122">Ástæðan fyrir þessu er að Mitt hlutverk eða hlutverk sem er sem stendur tengt við notandareikninginn þinn breytir þessari síðu sérstaklega fyrir hlutverkið þitt.</span><span class="sxs-lookup"><span data-stu-id="e1b75-122">The reason for this is that the Role Center or role that is currently associated with your user account modifies this page specifically for your role.</span></span> <span data-ttu-id="e1b75-123">Hafðu samband við stjórnanda til að fá aðstoð.</span><span class="sxs-lookup"><span data-stu-id="e1b75-123">Contact your administrator for assistance.</span></span> <span data-ttu-id="e1b75-124">Að öðrum kosti skal reyna að skipta yfir í Mitt hlutverk sem inniheldur hlutverkaleik fyrir þessa síðu.</span><span class="sxs-lookup"><span data-stu-id="e1b75-124">Alternatively, try switching to a Role Center that does include role-tailoring for this page.</span></span> <span data-ttu-id="e1b75-125">Frekari upplýsingar eru í [Breyta grundvallarstillingum](ui-change-basic-settings.md).</span><span class="sxs-lookup"><span data-stu-id="e1b75-125">For more information, see [Change Basic Settings](ui-change-basic-settings.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="e1b75-126">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="e1b75-126">See Also</span></span>
[<span data-ttu-id="e1b75-127">Sérstilling verksvæðis</span><span class="sxs-lookup"><span data-stu-id="e1b75-127">Personalize Your Workspace</span></span>](ui-personalization-user.md)  
[<span data-ttu-id="e1b75-128">Sérsníða síður fyrir forstillingar</span><span class="sxs-lookup"><span data-stu-id="e1b75-128">Customize Pages for Profiles</span></span>](ui-personalization-manage.md)  
[<span data-ttu-id="e1b75-129">Grunnstillingum breytt</span><span class="sxs-lookup"><span data-stu-id="e1b75-129">Change Basic Settings</span></span>](ui-change-basic-settings.md)  
[<span data-ttu-id="e1b75-130">Breyta því hvaða eiginleikar eru sýndir</span><span class="sxs-lookup"><span data-stu-id="e1b75-130">Change Which Features are Displayed</span></span>](ui-experiences.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
