---
title: "Vinna með uppskriftir til að stjórna íhlutum| Microsoft Docs"
description: "Þú stofnar samsetningaruppskrift til að tilgreina íhlutina eða tilföngin sem þarf til að setja saman vöruna sem samsetningaruppskriftin segir til um, og þú getur skoða íhluti samsetningarvöru."
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 05/06/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: e6aef60ee5b206b0ae978f72b92e6f8778290509
ms.contentlocale: is-is
ms.lasthandoff: 09/11/2017

---
# <a name="how-to-work-with-bills-of-material"></a><span data-ttu-id="daa7e-103">Hvernig á að: Vinna með uppskriftir</span><span class="sxs-lookup"><span data-stu-id="daa7e-103">How to: Work with Bills of Material</span></span>
> [!NOTE]  
>   <span data-ttu-id="daa7e-104">Núverandi útgáfa af [!INCLUDE[d365fin](includes/d365fin_md.md)] inniheldur aðeins fyrsta hluta samsetningarstjórnunarbúnaðarins.</span><span class="sxs-lookup"><span data-stu-id="daa7e-104">The current version of [!INCLUDE[d365fin](includes/d365fin_md.md)] only contains the first part of the Assembly Management feature.</span></span> <span data-ttu-id="daa7e-105">Eins og er getur þú aðeins búið til samsetningaruppskrift og síðan séð um tengda yfireiningar sem venjulega birgðavöru.</span><span class="sxs-lookup"><span data-stu-id="daa7e-105">For now, you can only create assembly BOMs and then handle the related parent items as normal inventory items.</span></span> <span data-ttu-id="daa7e-106">Í framtíðar uppfærslu getur þú stjórnað raunverulegu samsetningu hluta úr hlutum, annaðhvort í samanburði til birgðir eða samsetningar til þess að flytja og þú getur selt hluti sem pökkum.</span><span class="sxs-lookup"><span data-stu-id="daa7e-106">In a future update, you can manage the actual assembly of items from components, either in assemble-to-stock or assemble-to-order flows, and you can sell components as kits.</span></span>

<span data-ttu-id="daa7e-107">Þú notar uppskrift til að byggja upp yfireiningu sem þú selur sem undireiningar sem samanstanda af yfiríhlutnum eða sem þú setja saman í pöntun eða í birgðir.</span><span class="sxs-lookup"><span data-stu-id="daa7e-107">You use bills of materials (BOMs) to structure parent items that you sell as kits consisting of the parent's components or that you assemble to order or to stock.</span></span>

<span data-ttu-id="daa7e-108">Í [!INCLUDE[d365fin](includes/d365fin_md.md)] er uppskrift vísað til sem samsetningaruppskrift.</span><span class="sxs-lookup"><span data-stu-id="daa7e-108">In [!INCLUDE[d365fin](includes/d365fin_md.md)], a bill of materials is referred to as an "assembly BOM".</span></span> <span data-ttu-id="daa7e-109">Samsetningaruppskriftir tilgreina hvaða íhlutir eru í yfireiningu.</span><span class="sxs-lookup"><span data-stu-id="daa7e-109">Assembly BOMs specify which components are contained in parent items.</span></span> <span data-ttu-id="daa7e-110">Í þessum gögnum er átt við foreldrahluta sem "samsetningarhlutur".</span><span class="sxs-lookup"><span data-stu-id="daa7e-110">In this documentation, a parent item is referred to as an "assembly item".</span></span>

<span data-ttu-id="daa7e-111">Samsetningaruppskriftir innihalda yfirleitt vörur en geta einnig innihaldið einn eða fleiri forða sem eru nauðsynlegir til að setja samsetningaríhlutinn saman.</span><span class="sxs-lookup"><span data-stu-id="daa7e-111">Assembly BOMs usually contain items but can also contain one or more resources that are required to put the assembly item together.</span></span>

<span data-ttu-id="daa7e-112">Samsetningaruppskriftir geta haft mörg stig, sem þýðir að íhlutur í samsetningaruppskrift getur verið samsetningarvara sömuleiðis.</span><span class="sxs-lookup"><span data-stu-id="daa7e-112">Assembly BOMs can have multiple levels, which means that a component on the assembly BOM can be an assembly item itself.</span></span> <span data-ttu-id="daa7e-113">Í því tilviki inniheldur **samsetningaruppskrift** reiturinn á samsetningaruppskriftinni **Já**.</span><span class="sxs-lookup"><span data-stu-id="daa7e-113">In that case, the **Assembly BOM** field on the assembly BOM line contains **Yes**.</span></span>

<span data-ttu-id="daa7e-114">Sérstakar kröfur eiga við um hluti í samsetningaruppskrift að því er varðar framboð.</span><span class="sxs-lookup"><span data-stu-id="daa7e-114">Special requirements apply to items on assembly BOMs with regards to availability.</span></span> <span data-ttu-id="daa7e-115">Nánari upplýsingar er að finna í "Til að sjá framboð vöru með notkun þess í samsetningaruppskrift“ hlutann í [Hvernig á að: Fá yfirlit yfir framboð](inventory-how-availability-overview.md).</span><span class="sxs-lookup"><span data-stu-id="daa7e-115">For more information, see the "To see the availability of an item by its use in assembly BOMs" section in [How to: View the Availability of Items](inventory-how-availability-overview.md).</span></span>

> [!NOTE]  
>   <span data-ttu-id="daa7e-116">Þessi virkni krefst þess að upplifun þín sé stillt á **Pakki**.</span><span class="sxs-lookup"><span data-stu-id="daa7e-116">This functionality requires that your experience is set to **Suite**.</span></span> <span data-ttu-id="daa7e-117">Nánari upplýsingar er að finna í [aðlaga fjárhagsupplifun þína](ui-experiences.md).</span><span class="sxs-lookup"><span data-stu-id="daa7e-117">For more information, see [Customizing Your Financials Experience](ui-experiences.md).</span></span>

## <a name="to-create-an-assembly-bom"></a><span data-ttu-id="daa7e-118">Til að stofna samsetningaruppskrift</span><span class="sxs-lookup"><span data-stu-id="daa7e-118">To create an assembly BOM</span></span>
<span data-ttu-id="daa7e-119">Til að tilgreina yfireiningu sem samanstendur af öðrum atriðum, og hugsanlega úr tilföngum sem þarf til að setja yfireininguna saman, verður þú að búa til samsetningaruppskrift.</span><span class="sxs-lookup"><span data-stu-id="daa7e-119">To define a parent item that consists of other items, and potentially of resources required to put the parent together, you must create an assembly BOM.</span></span>  

<span data-ttu-id="daa7e-120">Að búa til samsetningaruppskrift er gert í tveimur hltuum:</span><span class="sxs-lookup"><span data-stu-id="daa7e-120">There are two parts to creating an assembly BOM:</span></span>
- <span data-ttu-id="daa7e-121">Uppsetning nýrra vöru</span><span class="sxs-lookup"><span data-stu-id="daa7e-121">Setting up a new item</span></span>
- <span data-ttu-id="daa7e-122">Skilgreining á gerð uppskriftar samsetningaríhlutar.</span><span class="sxs-lookup"><span data-stu-id="daa7e-122">Defining the BOM structure of the assembly item.</span></span>

1. <span data-ttu-id="daa7e-123">Setja upp nýtt atriði.</span><span class="sxs-lookup"><span data-stu-id="daa7e-123">Set up a new item.</span></span> <span data-ttu-id="daa7e-124">Nánari upplýsingar eru í [Hvernig á að: Skrá nýjar vörur](inventory-how-register-new-items.md).</span><span class="sxs-lookup"><span data-stu-id="daa7e-124">For more information, see [How to: Register New Items](inventory-how-register-new-items.md).</span></span>

    <span data-ttu-id="daa7e-125">Haltu áfram að slá inn íhluti eða tilföng á samsetningaruppskrift.</span><span class="sxs-lookup"><span data-stu-id="daa7e-125">Proceed to enter components or resources on the assembly BOM.</span></span>  
2. <span data-ttu-id="daa7e-126">Í glugganum **Birgðaspjald** fyrir samsetningaríhluti, veldu **Samsetning** og svo **Samsetningaruppskrift**.</span><span class="sxs-lookup"><span data-stu-id="daa7e-126">In the **Item Card** window for an assembly item, choose the **Assembly** action, and then choose the **Assembly BOM** action.</span></span>
3. <span data-ttu-id="daa7e-127">Í glugganum **Samsetningaruppskrift** þarf að fylla reitina út eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="daa7e-127">In the **Assembly BOM** window, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-view-the-components-of-an-assembly-item-indented-according-to-the-bom-structure"></a><span data-ttu-id="daa7e-128">Til að skoða íhluti samsetningaríhlutar sem ætlaður er samkvæmt uppskriftaruppbyggingunni</span><span class="sxs-lookup"><span data-stu-id="daa7e-128">To view the components of an assembly item indented according to the BOM structure</span></span>
<span data-ttu-id="daa7e-129">Úr **Samsetningaruppskrift** glugganum er hægt að opna annan gluaa sem sýnir íhluti og önnur tilföng samkvæmt uppskriftarstöðu undir samsetningaríhlutnum.</span><span class="sxs-lookup"><span data-stu-id="daa7e-129">From the **Assembly BOM** window, you can open a separate window that shows the components and any resources indented according to their BOM position under the assembly item.</span></span>

1. <span data-ttu-id="daa7e-130">Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Vörur** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="daa7e-130">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Items**, and then choose the related link.</span></span>
2. <span data-ttu-id="daa7e-131">Opnaðu kortið fyrir samsetningarhlut.</span><span class="sxs-lookup"><span data-stu-id="daa7e-131">Open the card for an assembly item.</span></span> <span data-ttu-id="daa7e-132">(**Samsetningaruppskrift** reiturinn í **Vara** glugganum inniheldur **Já**.)</span><span class="sxs-lookup"><span data-stu-id="daa7e-132">(The **Assembly BOM** field in the **Items** window contains **Yes**.)</span></span>
3. <span data-ttu-id="daa7e-133">Í glugganum **Birgðaspjald** fyrir veldu **Samsetning** og svo **Samsetningaruppskrift**.</span><span class="sxs-lookup"><span data-stu-id="daa7e-133">In the **Item Card** window, choose the **Assembly** action, and then choose the **Assembly BOM** action.</span></span>
4. <span data-ttu-id="daa7e-134">Í glugganum **Samsetningaruppskrift** velurðu aðgerðina **Sýna uppskrift**.</span><span class="sxs-lookup"><span data-stu-id="daa7e-134">In the **Assembly BOM** window, choose the **Show BOM** action.</span></span>

## <a name="to-buy-sell-or-transfer-assembly-items"></a><span data-ttu-id="daa7e-135">Til að kaupa, selja eða flytja samsetningaríhluti</span><span class="sxs-lookup"><span data-stu-id="daa7e-135">To buy, sell, or transfer assembly items</span></span>
<span data-ttu-id="daa7e-136">Vegna þess að núverandi útgáfa af [!INCLUDE[d365fin](includes/d365fin_md.md)] inniheldur eingöngu getuna til að skilgreina og úthluta samsettum uppskriftum, geturðu séð um samsetningarhluti á skjalalínum eins og venjulega hluti eingöngu.</span><span class="sxs-lookup"><span data-stu-id="daa7e-136">Because the current version of [!INCLUDE[d365fin](includes/d365fin_md.md)] only contains the ability to define and assign assembly BOMs to items, you can handle assembly items on document lines as normal items only.</span></span>

<span data-ttu-id="daa7e-137">**Athugið**: Birgðamagn uppskriftaríhluta verður ekki aðlagað fyrir þig.</span><span class="sxs-lookup"><span data-stu-id="daa7e-137">**Caution**: The inventory quantity of BOM components will not be adjusted if you do so.</span></span>

## <a name="see-also"></a><span data-ttu-id="daa7e-138">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="daa7e-138">See Also</span></span>
[<span data-ttu-id="daa7e-139">Hvernig á að Skrá nýjar vörur</span><span class="sxs-lookup"><span data-stu-id="daa7e-139">How to: Register New Items</span></span>](inventory-how-register-new-items.md)  
<span data-ttu-id="daa7e-140">[Hvernig skal: Skoða tiltækileika vöru](inventory-how-availability-overview.md)   </span><span class="sxs-lookup"><span data-stu-id="daa7e-140">[How to: View the Availability of Items](inventory-how-availability-overview.md)   </span></span>  
[<span data-ttu-id="daa7e-141">Birgðir</span><span class="sxs-lookup"><span data-stu-id="daa7e-141">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="daa7e-142">[Unnið með [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="daa7e-142">[Working with [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](ui-work-product.md)</span></span>

