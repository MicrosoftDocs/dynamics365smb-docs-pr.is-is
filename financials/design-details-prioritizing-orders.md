---
title: "Hönnunarupplýsingar - Forgangsraða pöntunum | Microsoft Docs"
description: "Kynntu þér hvernig skal forgangsraða til að mæta kröfum framboðs og eftirspurnar."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, priority, prioritize, order, sku, demand, supply
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 7af645f5a9dd7f34619d05cb2d4f0f7f8ad1921d
ms.contentlocale: is-is
ms.lasthandoff: 09/22/2017

---
# <a name="design-details-prioritizing-orders"></a><span data-ttu-id="0b207-103">Hönnunarupplýsingar: forgangsraða Pantanir</span><span class="sxs-lookup"><span data-stu-id="0b207-103">Design Details: Prioritizing Orders</span></span>
<span data-ttu-id="0b207-104">Innan tiltekinnar birgðahaldseiningar, táknar umbeðin eða tiltæk dagsetning hæsta forgang; eftirspurn í dag ætti að mæta áður en eftirspurn næstu viku er mætt.</span><span class="sxs-lookup"><span data-stu-id="0b207-104">Within a given SKU, the requested or available date represents the highest priority; the demand of today should be dealt with before the demand of next week.</span></span> <span data-ttu-id="0b207-105">En auk þessarar heildarforgangs, mun áætlanakerfi einnig benda hvaða tegund af eftirspurn ætti að vera uppfyllt áður en önnur er uppfyllt.</span><span class="sxs-lookup"><span data-stu-id="0b207-105">But in addition to this overall priority, the planning system will also suggest which type of demand should be fulfilled before fulfilling another demand.</span></span> <span data-ttu-id="0b207-106">Eins mun það stinga upp á hvaða uppruna framboðs ætti að jafna áður en aðrar framboðsuppsprettur eru jafnaðar.</span><span class="sxs-lookup"><span data-stu-id="0b207-106">Likewise, it will suggest what source of supply should be applied before applying other sources of supply.</span></span> <span data-ttu-id="0b207-107">Þetta er gert í samræmi við forgang pöntunar.</span><span class="sxs-lookup"><span data-stu-id="0b207-107">This is done according to order priorities.</span></span>  
  
<span data-ttu-id="0b207-108">Hlaðin eftirspurn og framboð hafa áhrif á forstillingu fyrir áætlaðar birgðir samkvæmt eftirfarandi forgangi:</span><span class="sxs-lookup"><span data-stu-id="0b207-108">Loaded demand and supply contribute to a profile for the projected inventory according to the following priorities:</span></span>  
  
## <a name="priorities-on-the-demand-side"></a><span data-ttu-id="0b207-109">Forgangur eftirspurnarmegin</span><span class="sxs-lookup"><span data-stu-id="0b207-109">Priorities on the Demand Side</span></span>  
1. <span data-ttu-id="0b207-110">Þegar afhent: birgðafærsla</span><span class="sxs-lookup"><span data-stu-id="0b207-110">Already shipped: Item Ledger Entry</span></span>  
2. <span data-ttu-id="0b207-111">Vöruskilapöntun innkaupa</span><span class="sxs-lookup"><span data-stu-id="0b207-111">Purchase Return Order</span></span>  
3. <span data-ttu-id="0b207-112">Sölupöntun</span><span class="sxs-lookup"><span data-stu-id="0b207-112">Sales Order</span></span>  
4. <span data-ttu-id="0b207-113">Þjónustupöntun</span><span class="sxs-lookup"><span data-stu-id="0b207-113">Service Order</span></span>  
5. <span data-ttu-id="0b207-114">Framleiðsluíhlutaþörf</span><span class="sxs-lookup"><span data-stu-id="0b207-114">Production Component Need</span></span>  
6. <span data-ttu-id="0b207-115">Samsetningarpöntunarlína</span><span class="sxs-lookup"><span data-stu-id="0b207-115">Assembly Order Line</span></span>  
7. <span data-ttu-id="0b207-116">Flutningspantanir á útleið.</span><span class="sxs-lookup"><span data-stu-id="0b207-116">Outbound Transfer Order</span></span>  
8. <span data-ttu-id="0b207-117">Standandi pöntun (sem hefur ekki þegar verið notuð í annarri sölupöntun)</span><span class="sxs-lookup"><span data-stu-id="0b207-117">Blanket Order (that has not already been consumed by related sales orders)</span></span>  
9. <span data-ttu-id="0b207-118">Spá (sem hefur ekki þegar verið notuð í annarri sölupöntun)</span><span class="sxs-lookup"><span data-stu-id="0b207-118">Forecast (that has not already been consumed by other sales orders)</span></span>  
  
> [!NOTE]  
>  <span data-ttu-id="0b207-119">Innkaupaskil eru yfirleitt ekki notuð í framboðsáætlun. Þau ætti að alltaf að taka úr lotunni sem á að skila.</span><span class="sxs-lookup"><span data-stu-id="0b207-119">Purchase returns are usually not involved in supply planning; they should always be reserved from the lot that is going to be returned.</span></span> <span data-ttu-id="0b207-120">Ef ekki er tekið frá gegna innkaupaskil hlutverki í framboðinu og eru fremst í forgangsröðinni til að komast hjá því að áætlanakerfið leggi til birgðapöntun bara til að þjóna innkaupaskilum.</span><span class="sxs-lookup"><span data-stu-id="0b207-120">If not reserved, purchase returns play a role in the availability and are highly prioritized to avoid that the planning system suggests a supply order just to serve a purchase return.</span></span>  
  
## <a name="priorities-on-the-supply-side"></a><span data-ttu-id="0b207-121">Forgangur framboðsmegin</span><span class="sxs-lookup"><span data-stu-id="0b207-121">Priorities on the Supply Side</span></span>  
1. <span data-ttu-id="0b207-122">Þegar í birgðum: birgðafærsla (sveigjanleiki áætlunar = enginn)</span><span class="sxs-lookup"><span data-stu-id="0b207-122">Already in inventory: Item Ledger Entry (Planning Flexibility = None)</span></span>  
2. <span data-ttu-id="0b207-123">Söluskilapöntun (sveigjanleiki í áætlun = enginn)</span><span class="sxs-lookup"><span data-stu-id="0b207-123">Sales Return Order (Planning Flexibility = None)</span></span>  
3. <span data-ttu-id="0b207-124">Flutningspöntun á innleið</span><span class="sxs-lookup"><span data-stu-id="0b207-124">Inbound Transfer Order</span></span>  
4. <span data-ttu-id="0b207-125">Framleiðslupöntun</span><span class="sxs-lookup"><span data-stu-id="0b207-125">Production Order</span></span>  
5. <span data-ttu-id="0b207-126">Samsetningarpöntun</span><span class="sxs-lookup"><span data-stu-id="0b207-126">Assembly Order</span></span>  
6. <span data-ttu-id="0b207-127">Innkaupapöntun</span><span class="sxs-lookup"><span data-stu-id="0b207-127">Purchase Order</span></span>  
  
## <a name="priority-related-to-the-state-of-demand-and-supply"></a><span data-ttu-id="0b207-128">Forgangur sem tengist stöðu eftirspurnar og framboðs</span><span class="sxs-lookup"><span data-stu-id="0b207-128">Priority Related to the State of Demand and Supply</span></span>  
<span data-ttu-id="0b207-129">Burtséð frá forgangi sem fylgir gerð eftirspurnar og framboðs skilgreinir núverandi staða pantana í vinnsluferlinu einnig forgang.</span><span class="sxs-lookup"><span data-stu-id="0b207-129">Apart from priorities given by the type of demand and supply, the present state of the orders in the execution process also defines a priority.</span></span> <span data-ttu-id="0b207-130">Til dæmis hafa vöruhúsaaðgerðir áhrif og staða sölu, innkaupa, flutnings, samsetningar og framleiðslupantana er tekin með í reikninginn:</span><span class="sxs-lookup"><span data-stu-id="0b207-130">For example, warehouse activities have an impact, and the status of sales, purchase, transfer, assembly, and production orders is taken into account:</span></span>  
  
1. <span data-ttu-id="0b207-131">Að hluta meðhöndlað (Sveigjanleiki áætlunar = Enginn)</span><span class="sxs-lookup"><span data-stu-id="0b207-131">Partly handled (Planning Flexibility = None)</span></span>  
2. <span data-ttu-id="0b207-132">Þegar í vinnslu í vöruhúsi (sveigjanleiki áætlunar = enginn)</span><span class="sxs-lookup"><span data-stu-id="0b207-132">Already in process in the warehouse (Planning Flexibility = None)</span></span>  
3. <span data-ttu-id="0b207-133">Útgefið - allar pantanategundir (áætlunarsveigjanleiki = ótakmarkað)</span><span class="sxs-lookup"><span data-stu-id="0b207-133">Released – all order types (Planning Flexibility = Unlimited)</span></span>  
4. <span data-ttu-id="0b207-134">Fastáætluð framleiðslupöntun (sveigjanleiki áætlunar = ótakmarkaður)</span><span class="sxs-lookup"><span data-stu-id="0b207-134">Firm Planned Production Order (Planning Flexibility = Unlimited)</span></span>  
5. <span data-ttu-id="0b207-135">Áætlað/opið – allar pantanagerðir (Sveigjanleiki áætlunar = Ótakmarkaður)</span><span class="sxs-lookup"><span data-stu-id="0b207-135">Planned/Open – all order types (Planning Flexibility = Unlimited)</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0b207-136">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="0b207-136">See Also</span></span>  
<span data-ttu-id="0b207-137">[Hönnunarupplýsingar: Jöfnun eftirspurnar og framboðs](design-details-balancing-demand-and-supply.md) </span><span class="sxs-lookup"><span data-stu-id="0b207-137">[Design Details: Balancing Demand and Supply](design-details-balancing-demand-and-supply.md) </span></span>  
<span data-ttu-id="0b207-138">[Hönnunarupplýsingar: Miðlægar hugmyndir áætlanakerfisins](design-details-central-concepts-of-the-planning-system.md) </span><span class="sxs-lookup"><span data-stu-id="0b207-138">[Design Details: Central Concepts of the Planning System](design-details-central-concepts-of-the-planning-system.md) </span></span>  
[<span data-ttu-id="0b207-139">Hönnunarupplýsingar: framboðsáætlun</span><span class="sxs-lookup"><span data-stu-id="0b207-139">Design Details: Supply Planning</span></span>](design-details-supply-planning.md)
