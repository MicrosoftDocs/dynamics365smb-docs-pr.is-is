---
title: "Rekja aðgerðir notanda í breytingaskrá| Microsoft Docs"
description: "Hægt er að virkja breytingaskrá svo að þú hafir yfirlit yfir allar breytingar sem gerðar hafa verið á gögnum í röktum töflum."
author: edupont04
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: user log, user activity, tracking
ms.date: 10/01/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: ab9696a3cc14970def764b2741d50dbcd5207460
ms.contentlocale: is-is
ms.lasthandoff: 09/28/2018

---
# <a name="logging-changes-in-business-central"></a><span data-ttu-id="a5a24-103">Skráir breytingar í Business Central</span><span class="sxs-lookup"><span data-stu-id="a5a24-103">Logging Changes in Business Central</span></span>
<span data-ttu-id="a5a24-104">Hægt er að kveikja á breytingaskrá í [!INCLUDE[d365fin](includes/d365fin_md.md)] til að fá verkþáttarferil.</span><span class="sxs-lookup"><span data-stu-id="a5a24-104">You can enable the change log in [!INCLUDE[d365fin](includes/d365fin_md.md)] so you have a history of activities.</span></span> <span data-ttu-id="a5a24-105">Skráin byggir á breytingum sem gerðar eru á gögnum í töflunum sem þú rekur. Í breytingarskránni, er færslum raðað í tímaröð og sýndar eru breytingar sem gerðar eru á reitum á tilgreindri töflu.</span><span class="sxs-lookup"><span data-stu-id="a5a24-105">The log is based on changes that are made to data in the tables that you track. In the change log, entries are chronologically ordered and show changes that are made to the fields on the specified tables.</span></span> <span data-ttu-id="a5a24-106">Breytingaskráin safnar saman öllum breytingum sem gerðar eru á töflunni.</span><span class="sxs-lookup"><span data-stu-id="a5a24-106">The change log collects all changes that are made to the table.</span></span>  

## <a name="working-with-the-change-log"></a><span data-ttu-id="a5a24-107">Vinna með breytingaskrá</span><span class="sxs-lookup"><span data-stu-id="a5a24-107">Working with the Change Log</span></span>
<span data-ttu-id="a5a24-108">Það er alþekkt vandamál í stýrðum tölvukerfum að finna uppruna villna og breytinga á gögnum.</span><span class="sxs-lookup"><span data-stu-id="a5a24-108">A common problem in many financial systems is to locate the origin of errors and changes in data.</span></span> <span data-ttu-id="a5a24-109">Þetta getur verið allt frá röngu símanúmeri viðskiptamanns til rangrar bókunar í fjárhag.</span><span class="sxs-lookup"><span data-stu-id="a5a24-109">It could be anything from an incorrect customer telephone number to an incorrect posting to the general ledger.</span></span> <span data-ttu-id="a5a24-110">Með breytingaskránni er hægt að rekja allar beinar breytingar sem notendur gera á gögnum í gagnagrunninum.</span><span class="sxs-lookup"><span data-stu-id="a5a24-110">The change log lets you track all direct modifications a user makes to data in the database.</span></span> <span data-ttu-id="a5a24-111">Tilgreina verður hverja töflu og reit sem kerfið á að skrá og síðan þarf að virkja breytingaskrána.</span><span class="sxs-lookup"><span data-stu-id="a5a24-111">You must specify each table and field that you want the system to log, and then you must activate the change log.</span></span>  

<span data-ttu-id="a5a24-112">Glugginn **Uppsetning breytingaskrár** er notaður til að gera breytingaskráningu virka eða óvirka.</span><span class="sxs-lookup"><span data-stu-id="a5a24-112">You activate and deactivate the change log in the **Change Log Setup** window.</span></span> <span data-ttu-id="a5a24-113">Þegar kveikt eða slökkt er á breytingaskrá er þessi verkþáttur skráður til að geta ævinlega séð hvaða notandi kveikti eða slökkti á breytingaskránni.</span><span class="sxs-lookup"><span data-stu-id="a5a24-113">When you activate or deactivate the change log, this activity is logged, so you can always see which user deactivated or reactivated the change log.</span></span> <span data-ttu-id="a5a24-114">Ekki er hægt að gera þá skráningu óvirka.</span><span class="sxs-lookup"><span data-stu-id="a5a24-114">This cannot be turned off.</span></span>  

<span data-ttu-id="a5a24-115">Í glugganum **Breytingaskrár Uppsetning** ef aðgerðin **Töflur** er valin, skal tilgreina hvaða töflur á að rekja breytingar fyrir og hvaða breytingar á að rekja. [!INCLUDE[d365fin](includes/d365fin_md.md)] rekur einnig númer kerfistaflna.</span><span class="sxs-lookup"><span data-stu-id="a5a24-115">In the **Change Log Setup** window, if you choose the **Tables** action, you can specify which tables you want to track changes for, and which changes to track. [!INCLUDE[d365fin](includes/d365fin_md.md)] also tracks a number of system tables.</span></span>

<span data-ttu-id="a5a24-116">Þegar breytingaskrá hefur verið sett upp, virkjuð og einhver hefur breytt gögnum skráir forritið breytinguna í breytingaskrárfærslu. Hægt er að skoða og afmarka breytingarnar í glugganum **Breytingaskrárfærslur**.</span><span class="sxs-lookup"><span data-stu-id="a5a24-116">After you have set up the change log, activated it, and made a change to data, you can view and filter the changes in the **Change Log Entries** window.</span></span> <span data-ttu-id="a5a24-117">Ef á að eyða færslum er hægt að gera í glugganum **Eyða Breytingaskrárfærslum** þar sem hægt er að stilla afmarkanir eftir dagsetningar og tíma.</span><span class="sxs-lookup"><span data-stu-id="a5a24-117">If you want to delete entries, you can do that in the **Delete Change Log Entries** window, where you can set filters based on dates and time.</span></span>  

## <a name="see-also"></a><span data-ttu-id="a5a24-118">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="a5a24-118">See Also</span></span>
[<span data-ttu-id="a5a24-119">Breyta grundvallarstillingum</span><span class="sxs-lookup"><span data-stu-id="a5a24-119">Changing Basic Settings</span></span>](ui-change-basic-settings.md)  
[<span data-ttu-id="a5a24-120">Röðun</span><span class="sxs-lookup"><span data-stu-id="a5a24-120">Sorting</span></span>](ui-sorting.md)  
[<span data-ttu-id="a5a24-121">Notkun Leit að síðu eða skýrslu</span><span class="sxs-lookup"><span data-stu-id="a5a24-121">Using Search for Page or Report</span></span>](ui-search.md)  
<span data-ttu-id="a5a24-122">[Vinna með notendur og heimildir](ui-how-users-permissions.md)  </span><span class="sxs-lookup"><span data-stu-id="a5a24-122">[Managing Users and Permissions](ui-how-users-permissions.md)  </span></span>  
<span data-ttu-id="a5a24-123">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="a5a24-123">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

