---
title: Rekja aðgerðir notanda í breytingaskrá| Microsoft Docs
description: Hægt er að virkja breytingaskrá svo að þú hafir yfirlit yfir allar breytingar sem gerðar hafa verið á gögnum í röktum töflum.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: user log, user activity, tracking
ms.date: 04/01/2019
ms.author: edupont
ms.openlocfilehash: fc14d11bf75ea39553c1ed04986273903874a0e1
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2019
ms.locfileid: "915431"
---
# <a name="auditing-changes-in-business-central"></a><span data-ttu-id="6e00d-103">Endurskoðunarbreytingar í Business Central</span><span class="sxs-lookup"><span data-stu-id="6e00d-103">Auditing Changes in Business Central</span></span>

<span data-ttu-id="6e00d-104">Hægt er að kveikja á breytingaskrá í [!INCLUDE[d365fin](includes/d365fin_md.md)] til að fá verkþáttarferil.</span><span class="sxs-lookup"><span data-stu-id="6e00d-104">You can enable the change log in [!INCLUDE[d365fin](includes/d365fin_md.md)] so you have a history of activities.</span></span> <span data-ttu-id="6e00d-105">Skráin byggir á breytingum sem gerðar eru á gögnum í töflunum sem þú rekur. Á síðunni **Breytingaskrárfærslur** er færslum raðað í tímaröð og sýndar eru breytingar sem gerðar eru á reitum á tilgreindum töflum.</span><span class="sxs-lookup"><span data-stu-id="6e00d-105">The log is based on changes that are made to data in the tables that you track. On the **Change Log Entries** page, entries are chronologically ordered and show changes that are made to the fields on the specified tables.</span></span> <span data-ttu-id="6e00d-106">Breytingaskráin safnar saman öllum breytingum sem gerðar eru á töflunni.</span><span class="sxs-lookup"><span data-stu-id="6e00d-106">The change log collects all changes that are made to the table.</span></span>

> [!Important]
> <span data-ttu-id="6e00d-107">Breytingar notanda eru ekki sýnilegar í **Breytingaskrárfærslum** fyrr en lota notanda er endurræst á ný, sem gerist í eftirfarandi tilvikum:</span><span class="sxs-lookup"><span data-stu-id="6e00d-107">A user's changes are not visible in the **Change Log Entries** until the user's session is restarted, which happens in the following cases:</span></span>
<br />
> * <span data-ttu-id="6e00d-108">Lotan rann út og var endurnýjuð.</span><span class="sxs-lookup"><span data-stu-id="6e00d-108">The session expired and was refreshed.</span></span>
> * <span data-ttu-id="6e00d-109">Notandinn valdi annað fyrirtæki eða hlutverkamiðstöð.</span><span class="sxs-lookup"><span data-stu-id="6e00d-109">The user selected another company or Role Center.</span></span>
> * <span data-ttu-id="6e00d-110">Notandinn skráði sig út og aftur inn.</span><span class="sxs-lookup"><span data-stu-id="6e00d-110">The user signed out and back in.</span></span>

## <a name="working-with-the-change-log"></a><span data-ttu-id="6e00d-111">Vinna með breytingaskrá</span><span class="sxs-lookup"><span data-stu-id="6e00d-111">Working with the Change Log</span></span>

<span data-ttu-id="6e00d-112">Það er alþekkt vandamál í stýrðum tölvukerfum að finna uppruna villna og breytinga á gögnum.</span><span class="sxs-lookup"><span data-stu-id="6e00d-112">A common problem in many financial systems is to locate the origin of errors and changes in data.</span></span> <span data-ttu-id="6e00d-113">Þetta getur verið allt frá röngu símanúmeri viðskiptamanns til rangrar bókunar í fjárhag.</span><span class="sxs-lookup"><span data-stu-id="6e00d-113">It could be anything from an incorrect customer telephone number to an incorrect posting to the general ledger.</span></span> <span data-ttu-id="6e00d-114">Með breytingaskránni er hægt að rekja allar beinar breytingar sem notendur gera á gögnum í gagnagrunninum.</span><span class="sxs-lookup"><span data-stu-id="6e00d-114">The change log lets you track all direct modifications a user makes to data in the database.</span></span> <span data-ttu-id="6e00d-115">Tilgreina verður hverja töflu og reit sem kerfið á að skrá og síðan þarf að virkja breytingaskrána.</span><span class="sxs-lookup"><span data-stu-id="6e00d-115">You must specify each table and field that you want the system to log, and then you must activate the change log.</span></span>  

<span data-ttu-id="6e00d-116">Síðan **Uppsetning breytingaskrár** er notaður til að gera breytingaskráningu virka eða óvirka.</span><span class="sxs-lookup"><span data-stu-id="6e00d-116">You activate and deactivate the change log on the **Change Log Setup** page.</span></span> <span data-ttu-id="6e00d-117">Þegar notandi kveikir eða slekkur á breytingaskrá er þessi verkþáttur skráður til að geta ævinlega séð hvaða notandi kveikti eða slökkti á breytingaskránni.</span><span class="sxs-lookup"><span data-stu-id="6e00d-117">When a user activates or deactivates the change log, this activity is logged, so you can always see which user deactivated or reactivated the change log.</span></span>

<span data-ttu-id="6e00d-118">Á síðunni **Breytingaskrár Uppsetning** ef aðgerðin **Töflur** er valin, skal tilgreina hvaða töflur á að rekja breytingar fyrir og hvaða breytingar á að rekja. [!INCLUDE[d365fin](includes/d365fin_md.md)] rekur einnig númer kerfistaflna.</span><span class="sxs-lookup"><span data-stu-id="6e00d-118">On the **Change Log Setup** page, if you choose the **Tables** action, you can specify which tables you want to track changes for, and which changes to track. [!INCLUDE[d365fin](includes/d365fin_md.md)] also tracks a number of system tables.</span></span>

<span data-ttu-id="6e00d-119">Þegar breytingaskrá hefur verið sett upp, virkjuð og einhver hefur breytt gögnum skráir forritið breytinguna í breytingaskrárfærslu. Hægt er að skoða og afmarka breytingarnar á síðunni **Breytingaskrárfærslur**.</span><span class="sxs-lookup"><span data-stu-id="6e00d-119">After you have set up the change log, activated it, and made a change to data, you can view and filter the changes on the **Change Log Entries** page.</span></span> <span data-ttu-id="6e00d-120">Ef á að eyða færslum er hægt að gera það á síðunni **Eyða breytingaskrárfærslum** þar sem hægt er að stilla afmarkanir eftir dagsetningu og tíma.</span><span class="sxs-lookup"><span data-stu-id="6e00d-120">If you want to delete entries, you can do that on the **Delete Change Log Entries** page, where you can set filters based on dates and time.</span></span>  

## <a name="see-also"></a><span data-ttu-id="6e00d-121">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="6e00d-121">See Also</span></span>
[<span data-ttu-id="6e00d-122">Breyta grundvallarstillingum</span><span class="sxs-lookup"><span data-stu-id="6e00d-122">Changing Basic Settings</span></span>](ui-change-basic-settings.md)  
[<span data-ttu-id="6e00d-123">Röðun</span><span class="sxs-lookup"><span data-stu-id="6e00d-123">Sorting</span></span>](ui-sorting.md)  
[<span data-ttu-id="6e00d-124">Nota Viðmótsleit til að finna eiginleika og upplýsingar</span><span class="sxs-lookup"><span data-stu-id="6e00d-124">Using Tell Me to Find Features and Information</span></span>](ui-search.md)  
<span data-ttu-id="6e00d-125">[Vinna með notendur og heimildir](ui-how-users-permissions.md)  </span><span class="sxs-lookup"><span data-stu-id="6e00d-125">[Managing Users and Permissions](ui-how-users-permissions.md)  </span></span>  
<span data-ttu-id="6e00d-126">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="6e00d-126">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
