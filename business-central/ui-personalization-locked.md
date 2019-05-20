---
title: Af hverju get ég ekki sérsniðið síðu | Microsoft Docs
description: Útskýrir hvers vegna þú getur ekki sérstillt síðu og hvað þú getur gert til að opna hana svo þú getir sérsniðið hana.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customize, personalize, personalization, hide columns, remove fields, move fields
ms.date: 04/01/2019
ms.author: jswymer
ms.openlocfilehash: 64995372f68ed2804bc165823dacc34ad6a3194d
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/29/2019
ms.locfileid: "1251286"
---
# <a name="why-a-page-is-locked-from-personalization"></a><span data-ttu-id="4c07d-103">Af hverju er síða læst og því ekki hægt að sérsníða hana</span><span class="sxs-lookup"><span data-stu-id="4c07d-103">Why a Page is Locked from Personalization</span></span>

<span data-ttu-id="4c07d-104">Það eru tvö skilyrði sem koma í veg fyrir að þú sérsníðir síðu.</span><span class="sxs-lookup"><span data-stu-id="4c07d-104">There are two conditions that prevent you from personalizing a page.</span></span> <span data-ttu-id="4c07d-105">Annaðhvort er blaðsíðan læst (eins og kemur fram í ![Sérstilla lás](media/personalization-lock-icon.png "Sérstilla lás")) eða hún er útilokuð (eins og kemur fram í ![Sérstilling útilokuð](media/personalization-blocked-icon.png "Sérstilling útilokuð")).</span><span class="sxs-lookup"><span data-stu-id="4c07d-105">Either the page is locked (as indicated by ![Personalize Lock](media/personalization-lock-icon.png "Personalize lock")) or it is blocked (as indicated by ![Personalization blocked](media/personalization-blocked-icon.png "Personalization blocked")).</span></span>

## <a name="locked-from-personalizing"></a><span data-ttu-id="4c07d-106">Læst fyrir sérstillingar</span><span class="sxs-lookup"><span data-stu-id="4c07d-106">Locked from Personalizing</span></span>

<span data-ttu-id="4c07d-107">Ef táknið ![Sérstilla lás](media/personalization-lock-icon.png "Sérstilla lás") í borðanum **Sérstilling** þegar síða er opnuð (eins og sýnt er) merkir það að þú getir ekki gert neinar breytingar á sérstillingu síðunnar.</span><span class="sxs-lookup"><span data-stu-id="4c07d-107">If there is a ![Personalize Lock](media/personalization-lock-icon.png "Personalize lock") icon in the **Personalizing** banner when you open a page (as shown), this means that you are currently prevented from making any more personalization changes to the page.</span></span>

<span data-ttu-id="4c07d-108">![Sérstilla lás](media/personalization-locked.png "Sérstilla lás")</span><span class="sxs-lookup"><span data-stu-id="4c07d-108">![Personalize Lock](media/personalization-locked.png "Personalize lock")</span></span>


<!-- This is because we changed the way personalization works behind the scenes since the last time that you personalized the page. Unfortunately, the old way and new of doing things do not work together.

The page currently includes the last personalization changes that you made. If you want to continue personalizing the page, then you can choose the lock icon and then **Unlock**. Just be aware that if you choose to unlock the page, the current personalization of the page will be cleared, and you will have to start from scratch.
-->

<span data-ttu-id="4c07d-109">Það kunna að vera tvær ástæður fyrir þessu:</span><span class="sxs-lookup"><span data-stu-id="4c07d-109">There can be two reasons for this:</span></span>

1. <span data-ttu-id="4c07d-110">Þú hefur sérstillt síðuna áður, en það var gert með eldri útgáfu af vörunni.</span><span class="sxs-lookup"><span data-stu-id="4c07d-110">You have personalized the page before, but it was done using an earlier version of the product.</span></span> <span data-ttu-id="4c07d-111">Við breyttum því hvernig sérstilling virkar frá því að þú sérstilltir síðuna síðast.</span><span class="sxs-lookup"><span data-stu-id="4c07d-111">We changed the way personalization works behind the scenes since the last time that you personalized the page.</span></span> <span data-ttu-id="4c07d-112">Því miður vinnur gamla og nýja aðferðin ekki saman.</span><span class="sxs-lookup"><span data-stu-id="4c07d-112">Unfortunately, the old way and new way of doing things do not work together.</span></span>

2. <span data-ttu-id="4c07d-113">Hingað til hefur þú aðeins notað [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)] til að sérsníða síðuna.</span><span class="sxs-lookup"><span data-stu-id="4c07d-113">Until now, you have only used the [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)] to personalize the page.</span></span>

### <a name="unlocking-the-page"></a><span data-ttu-id="4c07d-114">Síða aflæst</span><span class="sxs-lookup"><span data-stu-id="4c07d-114">Unlocking the Page</span></span>

<span data-ttu-id="4c07d-115">Ef þú vilt taka síðu úr lás og halda áfram að sérstilla hana skaltu velja ![Sérstilla lás](media/personalization-lock-icon.png "Sérstilla lás") og síðan **Taka úr lás**.</span><span class="sxs-lookup"><span data-stu-id="4c07d-115">If you want to unlock a page and continue personalizing it, choose ![Personalize Lock](media/personalization-lock-icon.png "Personalize lock"), and then **Unlock**.</span></span>  

<span data-ttu-id="4c07d-116">Áður en síða er tekin úr lás skal hafa eftirfarandi í huga:</span><span class="sxs-lookup"><span data-stu-id="4c07d-116">Before you unlock the page, be aware of the following:</span></span>

- <span data-ttu-id="4c07d-117">Núverandi sérstilling á síðunni verður hreinsuð.</span><span class="sxs-lookup"><span data-stu-id="4c07d-117">The current personalization of the page will be cleared.</span></span> <span data-ttu-id="4c07d-118">Síðan mun fara aftur í upprunalegt útlit og þú verður að byrja frá byrjun.</span><span class="sxs-lookup"><span data-stu-id="4c07d-118">The page will go back to its original layout, and you will have to start from scratch.</span></span>

- <span data-ttu-id="4c07d-119">Í [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)], mun síðan vera eins og hún er og verður ekki fyrir áhrifum frá nýjum breytingum sérstillinga sem gerðar eru í biðlara Business Central.</span><span class="sxs-lookup"><span data-stu-id="4c07d-119">In the [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)], the page will remain as-is and will not be affected by the new personalization changes made in the Business Central client.</span></span> <span data-ttu-id="4c07d-120">Í áframhaldinu verður sérstilling í [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)] og Business Central biðlara aðskilin að fullu hvort frá öðru.</span><span class="sxs-lookup"><span data-stu-id="4c07d-120">Going forward, the personalization in the [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)] and Business Central client will be completely separate from each other.</span></span>

## <a name="blocked-from-personalizing"></a><span data-ttu-id="4c07d-121">Lokað fyrir sérstillingar</span><span class="sxs-lookup"><span data-stu-id="4c07d-121">Blocked from Personalizing</span></span>

<span data-ttu-id="4c07d-122">Ef táknið ![Sérstilling útilokuð](media/personalization-blocked-icon.png "Sérstilling útilokuð") er í borðanum fyrir sérstillingu merkir það að þú getir ekki gert neinar sérstillingar á síðunni.</span><span class="sxs-lookup"><span data-stu-id="4c07d-122">If there is a ![Personalization blocked](media/personalization-blocked-icon.png "Personalization blocked") icon in the Personalizing banner, this means that you are blocked from doing any personalization to the page.</span></span>

<span data-ttu-id="4c07d-123">![Sérstilla lás](media/personalization-blocked.png "Sérstilla lás")</span><span class="sxs-lookup"><span data-stu-id="4c07d-123">![Personalize blocked](media/personalization-blocked.png "Personalize lock")</span></span>

<span data-ttu-id="4c07d-124">Ástæðan fyrir þessu er að Mitt hlutverk eða prófíll sem er sem stendur tengdur við notandareikninginn þinn breytir þessari síðu sérstaklega fyrir hlutverkið þitt.</span><span class="sxs-lookup"><span data-stu-id="4c07d-124">The reason for this is that the Role Center or profile that is currently associated with your user account modifies this page specifically for your role.</span></span> <span data-ttu-id="4c07d-125">Vinsamlegast hafðu samband við stjórnandann til að fá aðstoð eða, ef eitthvað vit er í því, reyndu að skipta yfir í hlutverk (frá [**Mínar stillingar**](https://businesscentral.dynamics.com?page=9176 "Fara beint í síðuna fyrir notandastillingarnar þínar í Business Central")) sem felur í sér sérsniðið hlutverk fyrir þessa síðu.</span><span class="sxs-lookup"><span data-stu-id="4c07d-125">Please contact your administrator for assistance or, if it makes sense, try switching to a Role Center (from  [**My Settings**](https://businesscentral.dynamics.com?page=9176 "Go directly to your user settings page in Business Central")) that does include role-tailoring for this page.</span></span>

## <a name="see-also"></a><span data-ttu-id="4c07d-126">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="4c07d-126">See Also</span></span>
[<span data-ttu-id="4c07d-127">Sérstillingar verksvæðis</span><span class="sxs-lookup"><span data-stu-id="4c07d-127">Personalizing Your Workspace</span></span>](ui-personalization-manage.md)  
[<span data-ttu-id="4c07d-128">Sérstillingum stjórnað</span><span class="sxs-lookup"><span data-stu-id="4c07d-128">Managing Personalization</span></span>](ui-personalization-manage.md)  
[<span data-ttu-id="4c07d-129">Breyta grundvallarstillingum</span><span class="sxs-lookup"><span data-stu-id="4c07d-129">Changing Basic Settings</span></span>](ui-change-basic-settings.md)  
[<span data-ttu-id="4c07d-130">Breyta því hvaða eiginleikar eru sýndir</span><span class="sxs-lookup"><span data-stu-id="4c07d-130">Changing Which Features are Displayed</span></span>](ui-experiences.md)  
