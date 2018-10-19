---
title: "Uppsetning birgðaverðmats og kostnaðar | Microsoft Docs"
description: "Eftirfarandi tafla lýsir röð verkefna með tenglum í efnisatriði þar sem þeim er lýst."
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
ms.openlocfilehash: 296f660f2ca4dfe7a605d2990e18567c5062a482
ms.contentlocale: is-is
ms.lasthandoff: 09/28/2018

---
# <a name="setting-up-inventory-valuation-and-costing"></a><span data-ttu-id="8c60b-103">Uppsetning birgðaverðmats og kostnaðar</span><span class="sxs-lookup"><span data-stu-id="8c60b-103">Setting Up Inventory Valuation and Costing</span></span>
<span data-ttu-id="8c60b-104">Til að ganga úr skugga um að birgðakostnaður sé skráður rétt, er nauðsynlegt að setja upp ýmsa reiti og glugga áður en þú byrjar að framkvæma vörufærslur.</span><span class="sxs-lookup"><span data-stu-id="8c60b-104">To make sure that inventory costs are recorded correctly, you must set up various fields and windows before you begin to make item transactions.</span></span>

<span data-ttu-id="8c60b-105">Eftirfarandi tafla lýsir röð verkefna með tenglum í efnisatriði þar sem þeim er lýst.</span><span class="sxs-lookup"><span data-stu-id="8c60b-105">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>

|<span data-ttu-id="8c60b-106">**Til að**</span><span class="sxs-lookup"><span data-stu-id="8c60b-106">**To**</span></span>|<span data-ttu-id="8c60b-107">**Sjá**</span><span class="sxs-lookup"><span data-stu-id="8c60b-107">**See**</span></span>|  
|------------|-------------|  
|<span data-ttu-id="8c60b-108">Velja kostnaðaraðferð fyrir hverja vöru til að stýra því hvernig upphaflegur kostnaður hennar er notaður til að meta birgðavirði og kostnað seldra vara.</span><span class="sxs-lookup"><span data-stu-id="8c60b-108">Set a costing method for each item to govern how its incoming cost is used to assess inventory value and the cost of goods sold.</span></span>|[<span data-ttu-id="8c60b-109">Skrá nýjar vörur</span><span class="sxs-lookup"><span data-stu-id="8c60b-109">Register New Items</span></span>](inventory-how-register-new-items.md)|  
|<span data-ttu-id="8c60b-110">Tryggja að kostnaður sé sjálfkrafa bókaður á fjárhag hvenær sem birgðafærsla er bókuð.</span><span class="sxs-lookup"><span data-stu-id="8c60b-110">Ensure that the cost is automatically posted to the general ledger whenever an inventory transaction is posted.</span></span>|<span data-ttu-id="8c60b-111">Reiturinn **Sjálfvirk kostnaðarbókun** í glugganum **Uppsetning birgða**</span><span class="sxs-lookup"><span data-stu-id="8c60b-111">**Automatic Cost Posting** field in the **Inventory Setup** window</span></span>|  
|<span data-ttu-id="8c60b-112">Tryggja að áætlaður kostnaður sé bókaður á fjárhag til að geta séð af bráðabirgðafjárhagsreikningum áætlaðar upphæðir sem eru fallnar í gjalddaga og kostnað seldra vara áður en þær eru reikningsfærðar í raun.</span><span class="sxs-lookup"><span data-stu-id="8c60b-112">Ensure that expected costs are posted to the general ledger to see from the interim G/L accounts an estimate of the amounts due and the cost of the traded items before they are actually invoiced.</span></span>|<span data-ttu-id="8c60b-113">Reiturinn **Áætluð kostnaðarbókun í fjárhag** í glugganum **Uppsetning birgða**</span><span class="sxs-lookup"><span data-stu-id="8c60b-113">**Expected Cost Posting to G/L** field in the **Inventory Setup** window</span></span>|  
|<span data-ttu-id="8c60b-114">Setja kerfið þannig upp að leiðrétt sé sjálfvirkt vegna allra kostnaðarbreytinga í hvert sinn sem birgðafærslur eru bókaðar.</span><span class="sxs-lookup"><span data-stu-id="8c60b-114">Set the system up to adjust for any cost changes automatically every time you post inventory transactions.</span></span>|[<span data-ttu-id="8c60b-115">Leiðr. kostnað vara</span><span class="sxs-lookup"><span data-stu-id="8c60b-115">Adjust Item Costs</span></span>](inventory-how-adjust-item-costs.md)|  
|<span data-ttu-id="8c60b-116">Skilgreina hvort reikna skuli meðalkostnaður aðeins á hverja vöru eða á hverja vöru og hverja birgðahaldseiningu og afbrigði vörunnar.</span><span class="sxs-lookup"><span data-stu-id="8c60b-116">Define if the average cost is to be calculated per item only or per item for each stockkeping unit and for each variant of the item.</span></span>|<span data-ttu-id="8c60b-117">Reiturinn **Útreikningsgerð meðalkostnaðar** í glugganum **Uppsetning birgða**</span><span class="sxs-lookup"><span data-stu-id="8c60b-117">**Average Cost Calc. Type** field in the **Inventory Setup** window</span></span>|  
|<span data-ttu-id="8c60b-118">Velja tímabilið sem forritið á að nota til að reikna út vegið meðalinnkaupsverð vara sem nota meðalverðsaðferðina.</span><span class="sxs-lookup"><span data-stu-id="8c60b-118">Select the period of time you would like the program to use for calculating the weighted average cost of items that use the average costing method.</span></span>|<span data-ttu-id="8c60b-119">Reiturinn **Meðalkostnaðartímabil** í glugganum **Uppsetning birgða**</span><span class="sxs-lookup"><span data-stu-id="8c60b-119">**Average Cost Period** field in the **Inventory Setup** window</span></span>|  
|<span data-ttu-id="8c60b-120">Skilgreina birgðatímabil til að stýra birgðavirði yfir tiltekinn tíma með því að banna bókun færslna á lokuð birgðatímabil.</span><span class="sxs-lookup"><span data-stu-id="8c60b-120">Define inventory periods to control inventory value over time by disallowing transaction posting in closed inventory periods.</span></span>|[<span data-ttu-id="8c60b-121">Vinna við birgðatímabil</span><span class="sxs-lookup"><span data-stu-id="8c60b-121">Work with Inventory Periods</span></span>](finance-how-to-work-with-inventory-periods.md)|  
|<span data-ttu-id="8c60b-122">Tryggja að söluvöruskilum sé jafnað á upphaflegu færsluna á útleið til að varðveita birgðavirð.</span><span class="sxs-lookup"><span data-stu-id="8c60b-122">Ensure that sales returns are applied to the original outbound transaction to preserve inventory value.</span></span>|<span data-ttu-id="8c60b-123">Reiturinn **Nákvæmar kostnaðarbakfærslur áskildar** í glugganum **Sala & útistandandi**</span><span class="sxs-lookup"><span data-stu-id="8c60b-123">**Exact Cost Reversing Mandatory** field in the **Sales & Receivables** window</span></span>|  
|<span data-ttu-id="8c60b-124">Tryggja að innkaupaskil sé jafnað á upphaflegu færsluna á innleið til að varðveita birgðavirði.</span><span class="sxs-lookup"><span data-stu-id="8c60b-124">Ensure that purchase returns are applied to the original inbound transaction to preserve inventory value.</span></span>|<span data-ttu-id="8c60b-125">Reiturinn **Nákvæmar kostnaðarbakfærslur áskildar** í glugganum **Innkaup & viðskiptaskuldir**</span><span class="sxs-lookup"><span data-stu-id="8c60b-125">**Exact Cost Reversing Mandatory** field in the **´Purchases & Payables** window</span></span>|
|<span data-ttu-id="8c60b-126">Setja upp sléttunarreglur sem á að nota þegar vöruverð er leiðrétt eða lagt til eða þegar staðlaður kostnaður er leiðréttur eða lagður til.</span><span class="sxs-lookup"><span data-stu-id="8c60b-126">Set up the rounding rules to apply when adjusting or suggesting item prices and when adjusting or suggesting standard costs.</span></span>|<span data-ttu-id="8c60b-127">Glugginn **Sléttunaraðferð**</span><span class="sxs-lookup"><span data-stu-id="8c60b-127">**Rounding Method** window</span></span>|  

## <a name="see-also"></a><span data-ttu-id="8c60b-128">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="8c60b-128">See Also</span></span>  
[<span data-ttu-id="8c60b-129">Birgðakostnaði stjórnað</span><span class="sxs-lookup"><span data-stu-id="8c60b-129">Managing Inventory Costs</span></span>](finance-manage-inventory-costs.md)  
[<span data-ttu-id="8c60b-130">Unnið með Business Central</span><span class="sxs-lookup"><span data-stu-id="8c60b-130">Working with Business Central</span></span>](ui-work-product.md)  
[<span data-ttu-id="8c60b-131">Fjármál</span><span class="sxs-lookup"><span data-stu-id="8c60b-131">Finance</span></span>](finance.md)  

