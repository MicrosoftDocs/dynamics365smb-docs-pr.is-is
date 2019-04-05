---
title: Hönnunarupplýsingar - Forgangsraða pöntunum | Microsoft Docs
description: Kynntu þér hvernig skal forgangsraða til að mæta kröfum framboðs og eftirspurnar.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, priority, prioritize, order, sku, demand, supply
ms.date: 10/01/2018
ms.author: sgroespe
redirect_url: design-details-balancing-demand-and-supply
ms.openlocfilehash: 1d58a02bdfe4810d1116d20866d3b435bc7341bc
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/08/2019
ms.locfileid: "800829"
---
# <a name="design-details-prioritizing-orders"></a><span data-ttu-id="00a9a-103">Hönnunarupplýsingar: forgangsraða Pantanir</span><span class="sxs-lookup"><span data-stu-id="00a9a-103">Design Details: Prioritizing Orders</span></span>
<span data-ttu-id="00a9a-104">Innan tiltekinnar birgðahaldseiningar, táknar umbeðin eða tiltæk dagsetning hæsta forgang; eftirspurn í dag ætti að mæta áður en eftirspurn næstu viku er mætt.</span><span class="sxs-lookup"><span data-stu-id="00a9a-104">Within a given SKU, the requested or available date represents the highest priority; the demand of today should be dealt with before the demand of next week.</span></span> <span data-ttu-id="00a9a-105">En auk þessarar heildarforgangs, mun áætlanakerfi einnig benda hvaða tegund af eftirspurn ætti að vera uppfyllt áður en önnur er uppfyllt.</span><span class="sxs-lookup"><span data-stu-id="00a9a-105">But in addition to this overall priority, the planning system will also suggest which type of demand should be fulfilled before fulfilling another demand.</span></span> <span data-ttu-id="00a9a-106">Eins mun það stinga upp á hvaða uppruna framboðs ætti að jafna áður en aðrar framboðsuppsprettur eru jafnaðar.</span><span class="sxs-lookup"><span data-stu-id="00a9a-106">Likewise, it will suggest what source of supply should be applied before applying other sources of supply.</span></span> <span data-ttu-id="00a9a-107">Þetta er gert í samræmi við forgang pöntunar.</span><span class="sxs-lookup"><span data-stu-id="00a9a-107">This is done according to order priorities.</span></span>  

<span data-ttu-id="00a9a-108">Hlaðin eftirspurn og framboð hafa áhrif á forstillingu fyrir áætlaðar birgðir samkvæmt eftirfarandi forgangi:</span><span class="sxs-lookup"><span data-stu-id="00a9a-108">Loaded demand and supply contribute to a profile for the projected inventory according to the following priorities:</span></span>  

## <a name="priorities-on-the-demand-side"></a><span data-ttu-id="00a9a-109">Forgangur eftirspurnarmegin</span><span class="sxs-lookup"><span data-stu-id="00a9a-109">Priorities on the Demand Side</span></span>  
1. <span data-ttu-id="00a9a-110">Þegar afhent: birgðafærsla</span><span class="sxs-lookup"><span data-stu-id="00a9a-110">Already shipped: Item Ledger Entry</span></span>  
2. <span data-ttu-id="00a9a-111">Vöruskilapöntun innkaupa</span><span class="sxs-lookup"><span data-stu-id="00a9a-111">Purchase Return Order</span></span>  
3. <span data-ttu-id="00a9a-112">Sölupöntun</span><span class="sxs-lookup"><span data-stu-id="00a9a-112">Sales Order</span></span>  
4. <span data-ttu-id="00a9a-113">Þjónustupöntun</span><span class="sxs-lookup"><span data-stu-id="00a9a-113">Service Order</span></span>  
5. <span data-ttu-id="00a9a-114">Framleiðsluíhlutaþörf</span><span class="sxs-lookup"><span data-stu-id="00a9a-114">Production Component Need</span></span>  
6. <span data-ttu-id="00a9a-115">Samsetningarpöntunarlína</span><span class="sxs-lookup"><span data-stu-id="00a9a-115">Assembly Order Line</span></span>  
7. <span data-ttu-id="00a9a-116">Flutningspantanir á útleið.</span><span class="sxs-lookup"><span data-stu-id="00a9a-116">Outbound Transfer Order</span></span>  
8. <span data-ttu-id="00a9a-117">Standandi pöntun (sem hefur ekki þegar verið notuð í annarri sölupöntun)</span><span class="sxs-lookup"><span data-stu-id="00a9a-117">Blanket Order (that has not already been consumed by related sales orders)</span></span>  
9. <span data-ttu-id="00a9a-118">Spá (sem hefur ekki þegar verið notuð í annarri sölupöntun)</span><span class="sxs-lookup"><span data-stu-id="00a9a-118">Forecast (that has not already been consumed by other sales orders)</span></span>  

> [!NOTE]  
>  <span data-ttu-id="00a9a-119">Innkaupaskil eru yfirleitt ekki notuð í framboðsáætlun. Þau ætti að alltaf að taka úr lotunni sem á að skila.</span><span class="sxs-lookup"><span data-stu-id="00a9a-119">Purchase returns are usually not involved in supply planning; they should always be reserved from the lot that is going to be returned.</span></span> <span data-ttu-id="00a9a-120">Ef ekki er tekið frá gegna innkaupaskil hlutverki í framboðinu og eru fremst í forgangsröðinni til að komast hjá því að áætlanakerfið leggi til birgðapöntun bara til að þjóna innkaupaskilum.</span><span class="sxs-lookup"><span data-stu-id="00a9a-120">If not reserved, purchase returns play a role in the availability and are highly prioritized to avoid that the planning system suggests a supply order just to serve a purchase return.</span></span>  

## <a name="priorities-on-the-supply-side"></a><span data-ttu-id="00a9a-121">Forgangur framboðsmegin</span><span class="sxs-lookup"><span data-stu-id="00a9a-121">Priorities on the Supply Side</span></span>  
1. <span data-ttu-id="00a9a-122">Þegar í birgðum: birgðafærsla (sveigjanleiki áætlunar = enginn)</span><span class="sxs-lookup"><span data-stu-id="00a9a-122">Already in inventory: Item Ledger Entry (Planning Flexibility = None)</span></span>  
2. <span data-ttu-id="00a9a-123">Söluskilapöntun (sveigjanleiki í áætlun = enginn)</span><span class="sxs-lookup"><span data-stu-id="00a9a-123">Sales Return Order (Planning Flexibility = None)</span></span>  
3. <span data-ttu-id="00a9a-124">Flutningspöntun á innleið</span><span class="sxs-lookup"><span data-stu-id="00a9a-124">Inbound Transfer Order</span></span>  
4. <span data-ttu-id="00a9a-125">Framleiðslupöntun</span><span class="sxs-lookup"><span data-stu-id="00a9a-125">Production Order</span></span>  
5. <span data-ttu-id="00a9a-126">Samsetningarpöntun</span><span class="sxs-lookup"><span data-stu-id="00a9a-126">Assembly Order</span></span>  
6. <span data-ttu-id="00a9a-127">Innkaupapöntun</span><span class="sxs-lookup"><span data-stu-id="00a9a-127">Purchase Order</span></span>  

## <a name="priority-related-to-the-state-of-demand-and-supply"></a><span data-ttu-id="00a9a-128">Forgangur sem tengist stöðu eftirspurnar og framboðs</span><span class="sxs-lookup"><span data-stu-id="00a9a-128">Priority Related to the State of Demand and Supply</span></span>  
<span data-ttu-id="00a9a-129">Burtséð frá forgangi sem fylgir gerð eftirspurnar og framboðs skilgreinir núverandi staða pantana í vinnsluferlinu einnig forgang.</span><span class="sxs-lookup"><span data-stu-id="00a9a-129">Apart from priorities given by the type of demand and supply, the present state of the orders in the execution process also defines a priority.</span></span> <span data-ttu-id="00a9a-130">Til dæmis hafa vöruhúsaaðgerðir áhrif og staða sölu, innkaupa, flutnings, samsetningar og framleiðslupantana er tekin með í reikninginn:</span><span class="sxs-lookup"><span data-stu-id="00a9a-130">For example, warehouse activities have an impact, and the status of sales, purchase, transfer, assembly, and production orders is taken into account:</span></span>  

1. <span data-ttu-id="00a9a-131">Að hluta meðhöndlað (Sveigjanleiki áætlunar = Enginn)</span><span class="sxs-lookup"><span data-stu-id="00a9a-131">Partly handled (Planning Flexibility = None)</span></span>  
2. <span data-ttu-id="00a9a-132">Þegar í vinnslu í vöruhúsi (sveigjanleiki áætlunar = enginn)</span><span class="sxs-lookup"><span data-stu-id="00a9a-132">Already in process in the warehouse (Planning Flexibility = None)</span></span>  
3. <span data-ttu-id="00a9a-133">Útgefið - allar pantanategundir (áætlunarsveigjanleiki = ótakmarkað)</span><span class="sxs-lookup"><span data-stu-id="00a9a-133">Released – all order types (Planning Flexibility = Unlimited)</span></span>  
4. <span data-ttu-id="00a9a-134">Fastáætluð framleiðslupöntun (sveigjanleiki áætlunar = ótakmarkaður)</span><span class="sxs-lookup"><span data-stu-id="00a9a-134">Firm Planned Production Order (Planning Flexibility = Unlimited)</span></span>  
5. <span data-ttu-id="00a9a-135">Áætlað/opið – allar pantanagerðir (Sveigjanleiki áætlunar = Ótakmarkaður)</span><span class="sxs-lookup"><span data-stu-id="00a9a-135">Planned/Open – all order types (Planning Flexibility = Unlimited)</span></span>  

## <a name="see-also"></a><span data-ttu-id="00a9a-136">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="00a9a-136">See Also</span></span>  
<span data-ttu-id="00a9a-137">[Hönnunarupplýsingar: Jöfnun eftirspurnar og framboðs](design-details-balancing-demand-and-supply.md) </span><span class="sxs-lookup"><span data-stu-id="00a9a-137">[Design Details: Balancing Demand and Supply](design-details-balancing-demand-and-supply.md) </span></span>  
<span data-ttu-id="00a9a-138">[Hönnunarupplýsingar: Miðlægar hugmyndir áætlanakerfisins](design-details-central-concepts-of-the-planning-system.md) </span><span class="sxs-lookup"><span data-stu-id="00a9a-138">[Design Details: Central Concepts of the Planning System](design-details-central-concepts-of-the-planning-system.md) </span></span>  
[<span data-ttu-id="00a9a-139">Hönnunarupplýsingar: framboðsáætlun</span><span class="sxs-lookup"><span data-stu-id="00a9a-139">Design Details: Supply Planning</span></span>](design-details-supply-planning.md)
