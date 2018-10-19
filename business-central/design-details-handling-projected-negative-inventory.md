---
title: "Hönnunarupplýsingar - Meðhöndlun Áætlaðrar Neikvæðra birgða | Microsoft Docs "
description: "Endurpöntunarmarkið endurspeglar ætlaða eftirspurn á afhendingartíma vörunnar. Þegar farið er yfir endurpöntunarmark er kominn tími til að panta meira magn. En áætlaðar birgðir verður að vera nógu stórt til að hylja eftirspurn þar til ný pöntun er móttekin. Á meðan ættu öryggisbirgðir að uppfylla sveiflur í eftirspurn að áætluðu þjónustustigi."
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
ms.openlocfilehash: 25a2017fd91f09a9d7725c68ffaa0df48a041294
ms.contentlocale: is-is
ms.lasthandoff: 09/28/2018

---
# <a name="design-details-handling-projected-negative-inventory"></a><span data-ttu-id="0788c-106">Hönnunarupplýsingar: Meðhöndlun Áætlaðrar Neikvæðra birgða</span><span class="sxs-lookup"><span data-stu-id="0788c-106">Design Details: Handling Projected Negative Inventory</span></span>
<span data-ttu-id="0788c-107">Endurpöntunarmarkið endurspeglar ætlaða eftirspurn á afhendingartíma vörunnar.</span><span class="sxs-lookup"><span data-stu-id="0788c-107">The reorder point expresses the anticipated demand during the lead time of the item.</span></span> <span data-ttu-id="0788c-108">Þegar farið er yfir endurpöntunarmark er kominn tími til að panta meira magn.</span><span class="sxs-lookup"><span data-stu-id="0788c-108">When the reorder point is passed, it is time to order more.</span></span> <span data-ttu-id="0788c-109">En áætlaðar birgðir verður að vera nógu stórt til að hylja eftirspurn þar til ný pöntun er móttekin.</span><span class="sxs-lookup"><span data-stu-id="0788c-109">But the projected inventory must be large enough to cover the demand until the new order is received.</span></span> <span data-ttu-id="0788c-110">Á meðan ættu öryggisbirgðir að uppfylla sveiflur í eftirspurn að áætluðu þjónustustigi.</span><span class="sxs-lookup"><span data-stu-id="0788c-110">Meanwhile, the safety stock should take care of fluctuations in demand up to a targeted service level.</span></span>  

 <span data-ttu-id="0788c-111">Þar af leiðandi lítur áætlanakerfi á það sem neyðarástand ef framtíðareftirspurn er ekki hægt að mæta úr áætlaðar birgðir eða m.ö.o. ef áætlaðar birgðir verða neikvæðar.</span><span class="sxs-lookup"><span data-stu-id="0788c-111">Consequently, the planning system considers it an emergency if a future demand cannot be served from the projected inventory, or expressed in another way, that the projected inventory goes negative.</span></span> <span data-ttu-id="0788c-112">Kerfið meðhöndlar þannig frávik með því að leggja til nýja birgðapöntun til að uppfylla þann hluta eftirspurnarinnar sem birgðir eða önnur eftirspurn getur ekki uppfyllt.</span><span class="sxs-lookup"><span data-stu-id="0788c-112">The system deals with such an exception by suggesting a new supply order to meet the part of the demand that cannot be met by inventory or other supply.</span></span> <span data-ttu-id="0788c-113">Stærð pöntunar í nýju birgðapöntuninni mun ekki taka tillit til hámarksbirgða eða pöntunarmagns, né heldur til pantanabreytinganna Hámarksmagn pöntunar, Lágmarksmagn pöntunar eða Margföld pöntun.</span><span class="sxs-lookup"><span data-stu-id="0788c-113">The order size of the new supply order will not take the maximum inventory or the reorder quantity into consideration, nor will it take into consideration the order modifiers Maximum Order Quantity, Minimum Order Quantity, and Order Multiple.</span></span> <span data-ttu-id="0788c-114">Í Staðinn, mun það endurspegla nákvæmlega skort.</span><span class="sxs-lookup"><span data-stu-id="0788c-114">Instead, it will reflect the exact deficiency.</span></span>  

 <span data-ttu-id="0788c-115">Áætlunarlína fyrir þessa gerð birgðapöntunar birtir viðvörunartákn og viðbótarupplýsingar birtast við uppflettingu, til að upplýsa notandann um stöðu mála.</span><span class="sxs-lookup"><span data-stu-id="0788c-115">The planning line for this type of supply order will display an Emergency warning icon, and additional information will be provided upon lookup to inform the user of the situation.</span></span>  

 <span data-ttu-id="0788c-116">Í eftirfarandi dæmi, framboð D táknar neyðarpöntun til að leiðrétta fyrir neikvæðum birgðum.</span><span class="sxs-lookup"><span data-stu-id="0788c-116">In the following illustration, supply D represents an emergency order to adjust for negative inventory.</span></span>  

 <span data-ttu-id="0788c-117">![Viðbragðsáætlun til að koma í veg fyrir neikvæða birgðastöðu](media/nav_app_supply_planning_2_negative_inventory.png "Viðbragðsáætlun til að koma í veg fyrir neikvæða birgðastöðu")</span><span class="sxs-lookup"><span data-stu-id="0788c-117">![Emergency planning suggestion to avoid negative inventory](media/nav_app_supply_planning_2_negative_inventory.png "Emergency planning suggestion to avoid negative inventory")</span></span>  

1.  <span data-ttu-id="0788c-118">Framboð **A**, fyrstu áætlaðar birgðir, er undir pöntunarmark.</span><span class="sxs-lookup"><span data-stu-id="0788c-118">Supply **A**, initial projected inventory, is below reorder point.</span></span>  
2.  <span data-ttu-id="0788c-119">Nýtt framsendingaráætlað framboð er stofnað (**C**).</span><span class="sxs-lookup"><span data-stu-id="0788c-119">A new forward-scheduled supply is created (**C**).</span></span>  

     <span data-ttu-id="0788c-120">(Magn = Hámarksbirgðir – Áætlað birgðastig)</span><span class="sxs-lookup"><span data-stu-id="0788c-120">(Quantity = Maximum Inventory – Projected Inventory Level)</span></span>  
3.  <span data-ttu-id="0788c-121">Framboð **A** er lokað með eftirspurn **B**, sem er ekki að öllu leyti annað.</span><span class="sxs-lookup"><span data-stu-id="0788c-121">Supply **A** is closed by demand **B**, which is not fully covered.</span></span>  

     <span data-ttu-id="0788c-122">(Eftirspurn **B** gæti reynt að áætla framboð C en það gerist ekki samkvæmt tímaramma.)</span><span class="sxs-lookup"><span data-stu-id="0788c-122">(Demand **B** could try to schedule Supply C in but that will not happen according to the time-bucket concept.)</span></span>  
4.  <span data-ttu-id="0788c-123">Nýtt framboð (**D**) er stofnað til að uppfylla eftirstandandi magn eftirspurnar **B**</span><span class="sxs-lookup"><span data-stu-id="0788c-123">New supply (**D**) is created to cover the remaining quantity on Demand **B**.</span></span>  
5.  <span data-ttu-id="0788c-124">Eftirspurn **B** er lokað (búa til áminningu fyrir áætluðum birgðum).</span><span class="sxs-lookup"><span data-stu-id="0788c-124">Demand **B** is closed (creating a reminder to the projected inventory).</span></span>  
6.  <span data-ttu-id="0788c-125">Nýjar birgðir **D** eru lokaðar.</span><span class="sxs-lookup"><span data-stu-id="0788c-125">The new supply **D** is closed.</span></span>  
7.  <span data-ttu-id="0788c-126">Áætlaðar birgðir er athugaðar. Endurpöntunarmarki hefur ekki verið náð.</span><span class="sxs-lookup"><span data-stu-id="0788c-126">Projected Inventory is checked; reorder point has not been crossed.</span></span>  
8.  <span data-ttu-id="0788c-127">Framboð **C** er lokað (ekki meiri eftirspurn til staðar).</span><span class="sxs-lookup"><span data-stu-id="0788c-127">Supply **C** is closed (no more demand exists).</span></span>  
9. <span data-ttu-id="0788c-128">Lokaathugun: Engin útistandandi birgðastigsinnheimtubréf eru eftir.</span><span class="sxs-lookup"><span data-stu-id="0788c-128">Final check: No outstanding inventory level reminders exist.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="0788c-129">Skref 4 endurspeglar hvernig kerfið bregst við í útgáfum fyrr en Microsoft Dynamics NAV 2009 SP1.</span><span class="sxs-lookup"><span data-stu-id="0788c-129">Step 4 reflects how the system reacts in versions earlier than Microsoft Dynamics NAV 2009 SP1.</span></span>  

 <span data-ttu-id="0788c-130">Þetta lýkur lýsingu miðlægra reglna sem tengjast birgðaáætlunargerð sem byggir á reglum um endurpöntun.</span><span class="sxs-lookup"><span data-stu-id="0788c-130">This concludes the description of central principles relating to inventory planning based on reordering policies.</span></span> <span data-ttu-id="0788c-131">Í eftirfarandi kafla er fjallað um einkenni fjögurra studdra endurpöntunarstefna.</span><span class="sxs-lookup"><span data-stu-id="0788c-131">The following section describes the characteristics of the four supported reordering policies.</span></span>  

## <a name="see-also"></a><span data-ttu-id="0788c-132">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="0788c-132">See Also</span></span>  
 <span data-ttu-id="0788c-133">[Hönnunarupplýsingar: Endurpöntunarstefnur](design-details-reordering-policies.md) </span><span class="sxs-lookup"><span data-stu-id="0788c-133">[Design Details: Reordering Policies](design-details-reordering-policies.md) </span></span>  
 <span data-ttu-id="0788c-134">[Hönnunarupplýsingar: áætlunarfæribreyta](design-details-planning-parameters.md) </span><span class="sxs-lookup"><span data-stu-id="0788c-134">[Design Details: Planning Parameters](design-details-planning-parameters.md) </span></span>  
 <span data-ttu-id="0788c-135">[Hönnunarupplýsingar: Meðhöndlun endurpöntunarstefna](design-details-handling-reordering-policies.md) </span><span class="sxs-lookup"><span data-stu-id="0788c-135">[Design Details: Handling Reordering Policies](design-details-handling-reordering-policies.md) </span></span>  
 [<span data-ttu-id="0788c-136">Hönnunarupplýsingar: framboðsáætlun</span><span class="sxs-lookup"><span data-stu-id="0788c-136">Design Details: Supply Planning</span></span>](design-details-supply-planning.md)

