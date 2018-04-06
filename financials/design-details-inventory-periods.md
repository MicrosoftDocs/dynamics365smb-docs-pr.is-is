---
title: "Hönnunarupplýsingar - Birgðahaldstími | Microsoft Docs"
description: "Bakfærð færsla eða kostnaðarleiðréttingar hafa oft áhrif á stöðu og birgðaverðmat fyrri reikningstímabil sem teljast lokjuð. Þetta getur haft öfug áhrif á nákvæma skýrslugerð, sérstaklega hjá alþjóðlegum fyrirtækjum. Búnaður birgðahaldstíma má nota til að forðast slíka vandamál, með því að opna eða loka birgðahaldstímum til að takmarka bókanir á tilteknu tímabili."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 742891cc8037696748b7beb459cc877ea482e2a1
ms.contentlocale: is-is
ms.lasthandoff: 03/22/2018

---
# <a name="design-details-inventory-periods"></a><span data-ttu-id="83c93-105">Hönnunarupplýsingar: birgðahaldstími</span><span class="sxs-lookup"><span data-stu-id="83c93-105">Design Details: Inventory Periods</span></span>
<span data-ttu-id="83c93-106">Bakfærð færsla eða kostnaðarleiðréttingar hafa oft áhrif á stöðu og birgðaverðmat fyrri reikningstímabil sem teljast lokjuð.</span><span class="sxs-lookup"><span data-stu-id="83c93-106">Backdated transactions or cost adjustments often affect balances and stock valuations for accounting periods that may be considered closed.</span></span> <span data-ttu-id="83c93-107">Þetta getur haft öfug áhrif á nákvæma skýrslugerð, sérstaklega hjá alþjóðlegum fyrirtækjum.</span><span class="sxs-lookup"><span data-stu-id="83c93-107">This can have adverse effects on accurate reporting, especially within global corporations.</span></span> <span data-ttu-id="83c93-108">Búnaður birgðahaldstíma má nota til að forðast slíka vandamál, með því að opna eða loka birgðahaldstímum til að takmarka bókanir á tilteknu tímabili.</span><span class="sxs-lookup"><span data-stu-id="83c93-108">The Inventory Periods feature can be used to avoid such problems by opening or closing inventory periods to limit posting in a set period of time.</span></span>  

 <span data-ttu-id="83c93-109">Birgðatímabil er tímabil, skilgreint með lokadagsetningu, sem birgðafærslur eru bókaðar innan.</span><span class="sxs-lookup"><span data-stu-id="83c93-109">An inventory period is a period of time, defined by an ending date, in which you post inventory transactions.</span></span> <span data-ttu-id="83c93-110">Þegar þú lokar birgðahaldstíma er ekki hægt að bóka neinar gildisbreytingar á lokaða tímabilinu.</span><span class="sxs-lookup"><span data-stu-id="83c93-110">When you close an inventory period, no value changes can be posted in the closed period.</span></span> <span data-ttu-id="83c93-111">Þetta inniheldur nýjar gildisbókanir, væntanlegar eða reikningsfærðar færslur, breytingar á núverandi gildi og kostnaðarleiðréttingu.</span><span class="sxs-lookup"><span data-stu-id="83c93-111">This includes new value postings, expected or invoiced postings, changes to existing values, and cost adjustments.</span></span> <span data-ttu-id="83c93-112">Hins vegar getur þú samt notað það á opna birgðafærslu sem lendir á lokaða tímabilinu.</span><span class="sxs-lookup"><span data-stu-id="83c93-112">However, you can still apply to an open item ledger entry that falls in the closed period.</span></span> <span data-ttu-id="83c93-113">Nánari upplýsingar eru í [Upplýsingar um hönnun: Vörujöfnun](design-details-item-application.md).</span><span class="sxs-lookup"><span data-stu-id="83c93-113">For more information, see [Design Details: Item Application](design-details-item-application.md).</span></span>  

 <span data-ttu-id="83c93-114">Til að ganga úr skugga um að allar viðskiptifærslur í lokuðu tímabili eru endanlegar, skulu eftirfarandi skilyrði vera uppfyllt áður en birgðahaldstími getur lokað:</span><span class="sxs-lookup"><span data-stu-id="83c93-114">To make sure that all transaction entries in a closed period are final, the following conditions must be met before an inventory period can close:</span></span>  

-   <span data-ttu-id="83c93-115">Allar birgðahöfuðbókarfærslur á útleið á tímabilinu þurfa að vera lokaðar (ekki neikvæð birgðastaða).</span><span class="sxs-lookup"><span data-stu-id="83c93-115">All outbound item ledger entries in the period must be closed (no negative inventory).</span></span>  
-   <span data-ttu-id="83c93-116">Leiðrétta þarf allan vörukostnað á tímabilinu.</span><span class="sxs-lookup"><span data-stu-id="83c93-116">All item costs in the period must be adjusted.</span></span>  
-   <span data-ttu-id="83c93-117">Allar losaðar og loknar framleiðslupantanir á tímabilinu þurfa að vera kostnaðarjafnaðar.</span><span class="sxs-lookup"><span data-stu-id="83c93-117">All released and finished production orders in the period must be cost adjusted.</span></span>  

 <span data-ttu-id="83c93-118">Þegar þú lokar birgðahaldstíma er stofnuð birgðahaldstímafærsla með þv´að nota númer síðustu vöruskráningar sem fellur undir birgðahaldstímann.</span><span class="sxs-lookup"><span data-stu-id="83c93-118">When you close an inventory period, an inventory period entry is created by using the number of the last item register that falls in the inventory period.</span></span> <span data-ttu-id="83c93-119">Að auki, er tími, dagsetning, og notandakóði notandans sem lokar tímabilinu eru færðar í birgðahaldstímifærslu.</span><span class="sxs-lookup"><span data-stu-id="83c93-119">In addition, the time, date, and user code of the user closing the period are recorded in the inventory period entry.</span></span> <span data-ttu-id="83c93-120">Með því að nota þessar upplýsingar með síðasta skráðri vöru fyrra tímabili, getur þú séð hvaða birgðafærslur voru bókaðar á birgðahaldstími.</span><span class="sxs-lookup"><span data-stu-id="83c93-120">By using this information with the last item register for the previous period, you can see which inventory transactions were posted in the inventory period.</span></span> <span data-ttu-id="83c93-121">Það er líka hægt að enduropna birgðahaldstíma ef þú þarft að bóka í lokuðum tímabili.</span><span class="sxs-lookup"><span data-stu-id="83c93-121">It is also possible to reopen inventory periods if you need to post in a closed period.</span></span> <span data-ttu-id="83c93-122">Þegar þú enduropnar birgðahaldstíma er stofnuð birgðahaldstímafærsla.</span><span class="sxs-lookup"><span data-stu-id="83c93-122">When you reopen an inventory period, an inventory period entry is created.</span></span>  

## <a name="see-also"></a><span data-ttu-id="83c93-123">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="83c93-123">See Also</span></span>  
 <span data-ttu-id="83c93-124">[Hönnunarupplýsingar: Birgðakostnaður](design-details-inventory-costing.md) [Stjórna birgðakostnaði](finance-manage-inventory-costs.md) [Fjármál](finance.md)</span><span class="sxs-lookup"><span data-stu-id="83c93-124">[Design Details: Inventory Costing](design-details-inventory-costing.md) [Managing Inventory Costs](finance-manage-inventory-costs.md) [Finance](finance.md)</span></span>  
 [<span data-ttu-id="83c93-125">Unnið með Financials</span><span class="sxs-lookup"><span data-stu-id="83c93-125">Working with Financials</span></span>](ui-work-product.md)

