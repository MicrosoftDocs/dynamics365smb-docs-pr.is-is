---
title: "Hönnunarupplýsingar - Hugmyndin um Jafnvægi í hnotskurn | Microsoft Docs"
description: "Eftirspurn er gefið af viðskiptavinum fyrirtækisins. Framboð er það sem fyrirtækið getur búið til og fjarlægy til að koma á jafnvægi. Áætlanakerfið byrjar á óháðri eftirspurn og rekur sig svo aftur að framboðinu."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: c6c7adb07337643360baa9cacf4eff659e7557c3
ms.contentlocale: is-is
ms.lasthandoff: 09/28/2018

---
# <a name="design-details-the-concept-of-balancing-in-brief"></a><span data-ttu-id="dd33c-105">Hönnunarupplýsingar: Hugmyndin um Jafnvægi í hnotskurn</span><span class="sxs-lookup"><span data-stu-id="dd33c-105">Design Details: The Concept of Balancing in Brief</span></span>
<span data-ttu-id="dd33c-106">Eftirspurn er gefið af viðskiptavinum fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="dd33c-106">Demand is given by a company’s customers.</span></span> <span data-ttu-id="dd33c-107">Framboð er það sem fyrirtækið getur búið til og fjarlægy til að koma á jafnvægi.</span><span class="sxs-lookup"><span data-stu-id="dd33c-107">Supply is what the company can create and remove to establish balance.</span></span> <span data-ttu-id="dd33c-108">Áætlanakerfið byrjar á óháðri eftirspurn og rekur sig svo aftur að framboðinu.</span><span class="sxs-lookup"><span data-stu-id="dd33c-108">The planning system starts with the independent demand and then tracks backwards to the supply.</span></span>  

 <span data-ttu-id="dd33c-109">Forstillingar birgða eru notaðar til að taka upplýsingar um eftirspurn og búnað, magn og tímastillingu.</span><span class="sxs-lookup"><span data-stu-id="dd33c-109">The inventory profiles are used to contain information about the demands and supplies, quantities, and timing.</span></span> <span data-ttu-id="dd33c-110">Þessar forstillingar mynda tvær hliðar afstemmingarskalans.</span><span class="sxs-lookup"><span data-stu-id="dd33c-110">These profiles essentially make up the two sides of the balancing scale.</span></span>  

 <span data-ttu-id="dd33c-111">Markmiðið með tihögun áætlanagerðarinnar er að mynda andvægi í eftirspurn og framboði vöru til að tryggja að eftirspurnin samsvari framboðinu á gerlegan hátt, eins og skilgreind er með áætlunarfæribreytum og -reglum.</span><span class="sxs-lookup"><span data-stu-id="dd33c-111">The objective of the planning mechanism is to counterbalance the demand and supply of an item to ensure that supply will match demand in a feasible way as defined by the planning parameters and rules.</span></span>  

 <span data-ttu-id="dd33c-112">![Yfirlit yfir framboð og eftirspurn jafnvægi](media/nav_app_supply_planning_2_balancing.png "Yfirlit yfir framboð og eftirspurn jafnvægi")</span><span class="sxs-lookup"><span data-stu-id="dd33c-112">![Overview of supply-demand balancing](media/nav_app_supply_planning_2_balancing.png "Overview of supply-demand balancing")</span></span>  

## <a name="see-also"></a><span data-ttu-id="dd33c-113">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="dd33c-113">See Also</span></span>  
 <span data-ttu-id="dd33c-114">[Hönnunarupplýsingar: Jöfnun eftirspurnar og framboðs](design-details-balancing-demand-and-supply.md) </span><span class="sxs-lookup"><span data-stu-id="dd33c-114">[Design Details: Balancing Demand and Supply](design-details-balancing-demand-and-supply.md) </span></span>  
 <span data-ttu-id="dd33c-115">[Hönnunarupplýsingar: Miðlægar hugmyndir áætlanakerfisins](design-details-central-concepts-of-the-planning-system.md) </span><span class="sxs-lookup"><span data-stu-id="dd33c-115">[Design Details: Central Concepts of the Planning System](design-details-central-concepts-of-the-planning-system.md) </span></span>  
 [<span data-ttu-id="dd33c-116">Hönnunarupplýsingar: framboðsáætlun</span><span class="sxs-lookup"><span data-stu-id="dd33c-116">Design Details: Supply Planning</span></span>](design-details-supply-planning.md)

