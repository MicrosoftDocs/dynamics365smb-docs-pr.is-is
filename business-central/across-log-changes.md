---
title: Endurskoðun breytinga| Microsoft docs
description: Hægt er að virkja breytingaskrá svo að þú hafir yfirlit yfir allar breytingar sem gerðar hafa verið á gögnum í röktum töflum. Þú getur einnig rakið aðgerðir með tilteknum gerðum aðgerðakladda.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: user log, user activity, tracking
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 6db170f8cf0b214a4ec85fc835eb8b98f071f203
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2020
ms.locfileid: "3187714"
---
# <a name="auditing-changes-in-business-central"></a><span data-ttu-id="fca74-104">Endurskoðunarbreytingar í Business Central</span><span class="sxs-lookup"><span data-stu-id="fca74-104">Auditing Changes in Business Central</span></span>

<span data-ttu-id="fca74-105">Hægt er að kveikja á breytingaskrá í [!INCLUDE[d365fin](includes/d365fin_md.md)] til að fá verkþáttarferil.</span><span class="sxs-lookup"><span data-stu-id="fca74-105">You can enable the change log in [!INCLUDE[d365fin](includes/d365fin_md.md)] so you have a history of activities.</span></span> <span data-ttu-id="fca74-106">Skráin byggir á breytingum sem gerðar eru á gögnum í töflunum sem þú rekur. Á síðunni **Breytingaskrárfærslur** er færslum raðað í tímaröð og sýndar eru breytingar sem gerðar eru á reitum á tilgreindum töflum.</span><span class="sxs-lookup"><span data-stu-id="fca74-106">The log is based on changes that are made to data in the tables that you track. On the **Change Log Entries** page, entries are chronologically ordered and show changes that are made to the fields on the specified tables.</span></span> <span data-ttu-id="fca74-107">Breytingaskráin safnar saman öllum breytingum sem gerðar eru á töflunni.</span><span class="sxs-lookup"><span data-stu-id="fca74-107">The change log collects all changes that are made to the table.</span></span>

> [!Important]
> <span data-ttu-id="fca74-108">Breytingar notanda eru ekki sýnilegar í **Breytingaskrárfærslum** fyrr en lota notanda er endurræst á ný, sem gerist í eftirfarandi tilvikum:</span><span class="sxs-lookup"><span data-stu-id="fca74-108">A user's changes are not visible in the **Change Log Entries** until the user's session is restarted, which happens in the following cases:</span></span>
<br />
> * <span data-ttu-id="fca74-109">Lotan rann út og var endurnýjuð.</span><span class="sxs-lookup"><span data-stu-id="fca74-109">The session expired and was refreshed.</span></span>
> * <span data-ttu-id="fca74-110">Notandinn valdi annað fyrirtæki eða hlutverkamiðstöð.</span><span class="sxs-lookup"><span data-stu-id="fca74-110">The user selected another company or Role Center.</span></span>
> * <span data-ttu-id="fca74-111">Notandinn skráði sig út og aftur inn.</span><span class="sxs-lookup"><span data-stu-id="fca74-111">The user signed out and back in.</span></span>

## <a name="working-with-the-change-log"></a><span data-ttu-id="fca74-112">Vinna með breytingaskrá</span><span class="sxs-lookup"><span data-stu-id="fca74-112">Working with the Change Log</span></span>

<span data-ttu-id="fca74-113">Það er alþekkt vandamál í stýrðum tölvukerfum að finna uppruna villna og breytinga á gögnum.</span><span class="sxs-lookup"><span data-stu-id="fca74-113">A common problem in many financial systems is to locate the origin of errors and changes in data.</span></span> <span data-ttu-id="fca74-114">Þetta getur verið allt frá röngu símanúmeri viðskiptamanns til rangrar bókunar í fjárhag.</span><span class="sxs-lookup"><span data-stu-id="fca74-114">It could be anything from an incorrect customer telephone number to an incorrect posting to the general ledger.</span></span> <span data-ttu-id="fca74-115">Með breytingaskránni er hægt að rekja allar beinar breytingar sem notendur gera á gögnum í gagnagrunninum.</span><span class="sxs-lookup"><span data-stu-id="fca74-115">The change log lets you track all direct modifications a user makes to data in the database.</span></span> <span data-ttu-id="fca74-116">Tilgreina verður hverja töflu og reit sem kerfið á að skrá og síðan þarf að virkja breytingaskrána.</span><span class="sxs-lookup"><span data-stu-id="fca74-116">You must specify each table and field that you want the system to log, and then you must activate the change log.</span></span>  

<span data-ttu-id="fca74-117">Síðan **Uppsetning breytingaskrár** er notaður til að gera breytingaskráningu virka eða óvirka.</span><span class="sxs-lookup"><span data-stu-id="fca74-117">You activate and deactivate the change log on the **Change Log Setup** page.</span></span> <span data-ttu-id="fca74-118">Þegar notandi kveikir eða slekkur á breytingaskrá er þessi verkþáttur skráður til að geta ævinlega séð hvaða notandi kveikti eða slökkti á breytingaskránni.</span><span class="sxs-lookup"><span data-stu-id="fca74-118">When a user activates or deactivates the change log, this activity is logged, so you can always see which user deactivated or reactivated the change log.</span></span>

<span data-ttu-id="fca74-119">Á síðunni **Breytingaskrár Uppsetning** ef aðgerðin **Töflur** er valin, skal tilgreina hvaða töflur á að rekja breytingar fyrir og hvaða breytingar á að rekja. [!INCLUDE[d365fin](includes/d365fin_md.md)] rekur einnig númer kerfistaflna.</span><span class="sxs-lookup"><span data-stu-id="fca74-119">On the **Change Log Setup** page, if you choose the **Tables** action, you can specify which tables you want to track changes for, and which changes to track. [!INCLUDE[d365fin](includes/d365fin_md.md)] also tracks a number of system tables.</span></span>

<span data-ttu-id="fca74-120">Þegar breytingaskrá hefur verið sett upp, virkjuð og einhver hefur breytt gögnum skráir forritið breytinguna í breytingaskrárfærslu. Hægt er að skoða og afmarka breytingarnar á síðunni **Breytingaskrárfærslur**.</span><span class="sxs-lookup"><span data-stu-id="fca74-120">After you have set up the change log, activated it, and made a change to data, you can view and filter the changes on the **Change Log Entries** page.</span></span> <span data-ttu-id="fca74-121">Ef á að eyða færslum er hægt að gera það á síðunni **Eyða breytingaskrárfærslum** þar sem hægt er að stilla afmarkanir eftir dagsetningu og tíma.</span><span class="sxs-lookup"><span data-stu-id="fca74-121">If you want to delete entries, you can do that on the **Delete Change Log Entries** page, where you can set filters based on dates and time.</span></span>  

## <a name="working-with-activity-logs"></a><span data-ttu-id="fca74-122">Vinna með aðgerðakladda</span><span class="sxs-lookup"><span data-stu-id="fca74-122">Working with Activity Logs</span></span>

<span data-ttu-id="fca74-123">Á sumum síðum í [!INCLUDE [prodshort](includes/prodshort.md)] er hægt að skoða aðgerðarkladda sem sýnir stöðu og allar villur úr skrám sem þú flytur út úr eða flytur inn í [!INCLUDE [prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="fca74-123">From some pages in [!INCLUDE [prodshort](includes/prodshort.md)], you can view an activity log that shows the status and any errors from files that you export from or import into [!INCLUDE [prodshort](includes/prodshort.md)].</span></span>  

<span data-ttu-id="fca74-124">Upplýsingarnar eru birtar á síðunni **aðgerðarkladdi** í samræmi við samhengið sem þær eru opnaðar úr.</span><span class="sxs-lookup"><span data-stu-id="fca74-124">The information is displayed in the **Activity Log** page, according to the context that it is opened from.</span></span> <span data-ttu-id="fca74-125">Hægt er að opna gluggann **skjalaskiptaþjónusta**, **skjal á innleið**, **bókaðan sölureikning** og **bókaðan sölukreditreikning** síður, til dæmis.</span><span class="sxs-lookup"><span data-stu-id="fca74-125">You can open the window from the **Document Exchange Service Setup**, **Incoming Document**, **Posted Sales Invoice**, and **Posted Sales Credit Memo** pages, for example.</span></span> <span data-ttu-id="fca74-126">Hægt er að tæma listann yfir kladdafærslur eða hreinsa lista yfir færslur sem eru eldri en 7 daga.</span><span class="sxs-lookup"><span data-stu-id="fca74-126">You can empty the list of log entries, or just clear the list of entries older than 7 days.</span></span>  

## <a name="see-also"></a><span data-ttu-id="fca74-127">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="fca74-127">See Also</span></span>
[<span data-ttu-id="fca74-128">Grunnstillingum breytt</span><span class="sxs-lookup"><span data-stu-id="fca74-128">Change Basic Settings</span></span>](ui-change-basic-settings.md)  
[<span data-ttu-id="fca74-129">Röðun, leit, og síun</span><span class="sxs-lookup"><span data-stu-id="fca74-129">Sorting, Searching, and Filtering</span></span>](ui-enter-criteria-filters.md)  
[<span data-ttu-id="fca74-130">Finndu síður og upplýsingar með Viðmótsleit</span><span class="sxs-lookup"><span data-stu-id="fca74-130">Finding Pages and Information with Tell Me</span></span>](ui-search.md)  
<span data-ttu-id="fca74-131">[Úthluta leyfum til notenda og hópa](ui-define-granular-permissions.md)  </span><span class="sxs-lookup"><span data-stu-id="fca74-131">[Assign Permissions to Users and Groups](ui-define-granular-permissions.md)  </span></span>  
<span data-ttu-id="fca74-132">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="fca74-132">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
