---
title: "Hvernig á að uppfæra staðlað kostnaðarverð | Microsoft Docs"
description: "Reglulega verður að uppfæra staðlað kostnaðarverð íhluta og leggja nýja kostnaðinn saman við yfirvöruna."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/09/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: c59977f847a020fbcda490893dbe15ed88ac1e5a
ms.contentlocale: is-is
ms.lasthandoff: 03/22/2018

---
# <a name="update-standard-costs"></a><span data-ttu-id="614dd-103">Uppfæra staðlaðan kostnað</span><span class="sxs-lookup"><span data-stu-id="614dd-103">Update Standard Costs</span></span>
<span data-ttu-id="614dd-104">Reglulega verður að uppfæra staðlað kostnaðarverð íhluta og leggja nýja kostnaðinn saman við yfirvöruna.</span><span class="sxs-lookup"><span data-stu-id="614dd-104">You must periodically update the standard costs of components and roll the new costs up to the parent item.</span></span> <span data-ttu-id="614dd-105">Ferlið samanstendur yfirleitt af fjórum eftirtöldum skrefum:</span><span class="sxs-lookup"><span data-stu-id="614dd-105">The process typically consists of the following four steps:</span></span>  

1.  <span data-ttu-id="614dd-106">Uppfærslu kostnaðar á íhluta- og afkastagetustigunum.</span><span class="sxs-lookup"><span data-stu-id="614dd-106">Update costs at the component and capacity levels.</span></span> <span data-ttu-id="614dd-107">Frekari upplýsingar, sjá **Leggja til staðlaðan vörukostnað** runuvinnslu.</span><span class="sxs-lookup"><span data-stu-id="614dd-107">For more information, see the **Suggest Item Standard Cost** batch job.</span></span>  
2.  <span data-ttu-id="614dd-108">Samstilling og samantekt íhluta- og afkastakostnaðarins til að reikna út heildarframleiðslu- eða samsetningarkostnað varanna.</span><span class="sxs-lookup"><span data-stu-id="614dd-108">Consolidate and roll up the component and capacity costs to calculate the total manufacturing or assembly cost of the items.</span></span>  
3.  <span data-ttu-id="614dd-109">Innleiða staðlaðan kostnað sem færður var inn þegar fyrri keyrsla var keyrð.</span><span class="sxs-lookup"><span data-stu-id="614dd-109">Implement the standard costs that are entered when you run the previous batch jobs.</span></span> <span data-ttu-id="614dd-110">Staðlaður kostnaður tekur ekki gildi fyrr en hann er innleiddur.</span><span class="sxs-lookup"><span data-stu-id="614dd-110">The standard costs do not take effect until they are implemented.</span></span> <span data-ttu-id="614dd-111">Sjá frekari upplýsingar í Innleiða breytingu á stöðluðu kostnaðarverði.</span><span class="sxs-lookup"><span data-stu-id="614dd-111">For more information, see Implement Standard Cost Changes.</span></span>  
4.  <span data-ttu-id="614dd-112">Innleiða breytingar til að uppfæra reitinn **Kostn.verð** á birgðaspjaldinu og framkvæma endurmat á birgðum.</span><span class="sxs-lookup"><span data-stu-id="614dd-112">Implement the changes to update the **Unit Cost** field on the item card and perform inventory revaluation.</span></span> <span data-ttu-id="614dd-113">Nánari upplýsingar eru í [Endurmat birgða](inventory-how-revalue-inventory.md).</span><span class="sxs-lookup"><span data-stu-id="614dd-113">For more information, see [Revalue Inventory](inventory-how-revalue-inventory.md).</span></span>  

<span data-ttu-id="614dd-114">Í [Um útreikning staðlaðs kostnaðar](finance-about-calculating-standard-cost.md) er fjallað nánar um þetta efni.</span><span class="sxs-lookup"><span data-stu-id="614dd-114">For more information, see [About Calculating Standard Cost](finance-about-calculating-standard-cost.md).</span></span>  
## <a name="to-update-standard-costs"></a><span data-ttu-id="614dd-115">að uppfæra staðlað kostnaðarverð</span><span class="sxs-lookup"><span data-stu-id="614dd-115">To update standard costs</span></span>  
1.  <span data-ttu-id="614dd-116">Keyrslan **Leiðr. kostnað - Birgðafærslur** er keyrð</span><span class="sxs-lookup"><span data-stu-id="614dd-116">Run the **Adjust Cost-Item Entries** batch job.</span></span>  
2.  <span data-ttu-id="614dd-117">Keyrslan **Bóka birgðakostnað á fjárhag** er keyrð</span><span class="sxs-lookup"><span data-stu-id="614dd-117">Run the **Post Inventory Cost to G/L** batch job.</span></span>  
3.  <span data-ttu-id="614dd-118">Opnið **Vinnublað fyrir staðlaðan kostnað** og notið eina eða fleiri af eftirfarandi aðgerðum:</span><span class="sxs-lookup"><span data-stu-id="614dd-118">Open the **Standard Cost Worksheet** and use one or more of the following functions:</span></span>  

    1.  <span data-ttu-id="614dd-119">Keyrslan **Leggja til staðlaðan vörukostnað** er keyrð.</span><span class="sxs-lookup"><span data-stu-id="614dd-119">Run the **Suggest Item Standard Cost** batch job.</span></span>  
    2.  <span data-ttu-id="614dd-120">Niðurstöðurnar eru skoðaðar og breytingar eru gerðar eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="614dd-120">Review the results and make changes as necessary.</span></span>  
    3.  <span data-ttu-id="614dd-121">Keyrslan **Leggja til staðlaðan afkastakostnað** er keyrð.</span><span class="sxs-lookup"><span data-stu-id="614dd-121">Run the **Suggest Capacity Standard Cost** batch job.</span></span>  
    4.  <span data-ttu-id="614dd-122">Niðurstöðurnar eru skoðaðar og breytingar eru gerðar eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="614dd-122">Review the results and make changes as necessary.</span></span>
    5. <span data-ttu-id="614dd-123">Keyrslan **Leggja saman staðlað kostnaðarverð** er keyrð.</span><span class="sxs-lookup"><span data-stu-id="614dd-123">Run the **Roll Up Standard Cost** batch job.</span></span>
    6.  <span data-ttu-id="614dd-124">Niðurstöðurnar eru skoðaðar og breytingar eru gerðar eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="614dd-124">Review the results and make changes as necessary.</span></span>
    7.  <span data-ttu-id="614dd-125">Keyrslan **Innleiða breytingu á stöðluðu kostnaðarverði** er keyrð.</span><span class="sxs-lookup"><span data-stu-id="614dd-125">Run the **Implement Standard Cost Changes** batch job.</span></span>  
4.  <span data-ttu-id="614dd-126">Skoða og birta skal gluggann **Endurmatsbók** sem hefur verið fyllt með færslum úr fyrri skrefum í þessu ferli.</span><span class="sxs-lookup"><span data-stu-id="614dd-126">Review and post the **Revaluation Journal** window, which has been populated with entries from the previous steps in this process.</span></span>  

## <a name="see-also"></a><span data-ttu-id="614dd-127">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="614dd-127">See Also</span></span>  
 <span data-ttu-id="614dd-128">[Um umreikning staðalkostnaðar](finance-about-calculating-standard-cost.md) </span><span class="sxs-lookup"><span data-stu-id="614dd-128">[About Calculating Standard Cost](finance-about-calculating-standard-cost.md) </span></span>  
 <span data-ttu-id="614dd-129">[Birgðakostnaði stjórnað](finance-manage-inventory-costs.md) </span><span class="sxs-lookup"><span data-stu-id="614dd-129">[Managing Inventory Costs](finance-manage-inventory-costs.md) </span></span>  
 <span data-ttu-id="614dd-130">[Hönnunarupplýsingar: Aðferð kostn.útreiknings](design-details-costing-methods.md) [[Fjármál](finance.md)</span><span class="sxs-lookup"><span data-stu-id="614dd-130">[Design Details: Costing Methods](design-details-costing-methods.md) [[Finance](finance.md)</span></span>  
 <span data-ttu-id="614dd-131">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="614dd-131">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

