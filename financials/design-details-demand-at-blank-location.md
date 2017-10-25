---
title: "Hönnunarupplýsingar - Eftirspurn og framboð | Microsoft Docs"
description: "Í þessu efnisatriði er fjallað um hugtakið Eftirspurn, sem er algengasta orðið notað yfir hvers konar vergri eftirspurn, svo sem sölupöntun og íhluti þarft frá framleiðslu röð."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, demand, supply, inventory, planning
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 69d5e574b390fe50490ff98616983a5e9ea31d94
ms.contentlocale: is-is
ms.lasthandoff: 09/22/2017

---
# <a name="design-details-demand-and-supply"></a><span data-ttu-id="612ee-103">Hönnunarupplýsingar: jöfnun eftirspurn og framboð</span><span class="sxs-lookup"><span data-stu-id="612ee-103">Design Details: Demand and Supply</span></span>
<span data-ttu-id="612ee-104">Eftirspurn er algeng orð notuð fyrir hvers konar vergri eftirspurn, svo sem sölupöntun og íhluti þarft frá framleiðslu röð.</span><span class="sxs-lookup"><span data-stu-id="612ee-104">Demand is the common term used for any kind of gross demand, such as a sales order and component need from a production order.</span></span> <span data-ttu-id="612ee-105">Að auki leyfir forritið meira tæknilega tegundir af eftirspurn, svo sem neikvæðar birgðum og innkaupaskil.</span><span class="sxs-lookup"><span data-stu-id="612ee-105">In addition, the program allows more technical types of demand, such as negative inventory and purchase returns.</span></span>  
  
<span data-ttu-id="612ee-106">Framboð er það orð sem er mest notað fyrir hvaða tegund af jákvæðu eða innleiðarmagni sem er, eins og birgðir, innkaup, samsetning, framleiðsla eða millifærslu á innleið.</span><span class="sxs-lookup"><span data-stu-id="612ee-106">Supply is the common term used for any kind of positive or inbound quantity, such as inventory, purchases, assembly, production, or inbound transfers.</span></span> <span data-ttu-id="612ee-107">Að auki geta söluvöruskil aftur getur einnig táknað framboð.</span><span class="sxs-lookup"><span data-stu-id="612ee-107">In addition, a sales return may also represent supply.</span></span>  
  
<span data-ttu-id="612ee-108">Til að raða út margar uppsprettur eftirspurn og framboð, áætlanakerfi skipuleggur þær á tvær tíma línur sem kallast birgðaforstillingar.</span><span class="sxs-lookup"><span data-stu-id="612ee-108">To sort out the many sources of demand and supply, the planning system organizes them on two time lines called inventory profiles.</span></span> <span data-ttu-id="612ee-109">Ein forstilling inniheldur eftirspurnartilvik og önnur inniheldur samsvarandi framboðstilvik.</span><span class="sxs-lookup"><span data-stu-id="612ee-109">One profile holds demand events, and the other holds the corresponding supply events.</span></span> <span data-ttu-id="612ee-110">Hver atburður táknar eina pöntunarnetsfærslu, t.d. sölulínu, birgðafærslu, eða framleiðslupöntunarlínu.</span><span class="sxs-lookup"><span data-stu-id="612ee-110">Each event represents one order network entity, such as a sales order line, an item ledger entry, or a production order line.</span></span>  
  
<span data-ttu-id="612ee-111">Þegar birgðaforstillingar eru sóttar eru mismunandi eftirspurn-framboð söfn jöfnuð til að skila framboðsáætlun sem uppfyllir listuð markmið.</span><span class="sxs-lookup"><span data-stu-id="612ee-111">When inventory profiles are loaded, the different demand-supply sets are balanced to output a supply plan that fulfills the listed goals.</span></span>  
  
<span data-ttu-id="612ee-112">Áætlunarfæribreytur og birgðastig eru aðrar gerðir eftirspurnar og framboðs, sem fara í gegnum samþætta jöfnun til að fylla á birgðavörur.</span><span class="sxs-lookup"><span data-stu-id="612ee-112">Planning parameters and inventory levels are other types of demand and supply respectively, which undergo integrated balancing to replenish stock items.</span></span> <span data-ttu-id="612ee-113">Nánari upplýsingar eru í [Upplýsingar um hönnun: Afgreiðsla endurpöntunarstefna](design-details-handling-reordering-policies.md).</span><span class="sxs-lookup"><span data-stu-id="612ee-113">For more information, see [Design Details: Handling Reordering Policies](design-details-handling-reordering-policies.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="612ee-114">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="612ee-114">See Also</span></span>  
<span data-ttu-id="612ee-115">[Hönnunarupplýsingar: Jöfnun eftirspurnar og framboðs](design-details-balancing-demand-and-supply.md) </span><span class="sxs-lookup"><span data-stu-id="612ee-115">[Design Details: Balancing Demand and Supply](design-details-balancing-demand-and-supply.md) </span></span>  
<span data-ttu-id="612ee-116">[Hönnunarupplýsingar: Miðlægar hugmyndir áætlanakerfisins](design-details-central-concepts-of-the-planning-system.md) </span><span class="sxs-lookup"><span data-stu-id="612ee-116">[Design Details: Central Concepts of the Planning System](design-details-central-concepts-of-the-planning-system.md) </span></span>  
[<span data-ttu-id="612ee-117">Hönnunarupplýsingar: framboðsáætlun</span><span class="sxs-lookup"><span data-stu-id="612ee-117">Design Details: Supply Planning</span></span>](design-details-supply-planning.md)
