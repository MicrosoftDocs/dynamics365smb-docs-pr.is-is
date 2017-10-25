---
title: "Meðhöndla birgða- og framleiðslukostnað | Microsoft Docs"
description: "Þótt margar aðgerðir kostnaðarbókhalds felist í innri ferlum sem notandinn kemur ekki nálægt, til dæmis jöfnun færslna og sjálfvirk kostnaðarleiðrétting, eru nokkrir reitir, gluggar og skýrslur sem ætluð eru notendum sem vinna beint eða óbeint með kostnað vara eða aðgerða."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/09/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 2745d8b06967549b32c8014a24ab9958c72c1c9d
ms.contentlocale: is-is
ms.lasthandoff: 09/22/2017

---
# <a name="handling-inventory-and-manufacturing-costs"></a><span data-ttu-id="5e279-103">Meðhöndla birgða- og framleiðslukostnað</span><span class="sxs-lookup"><span data-stu-id="5e279-103">Handling Inventory and Manufacturing Costs</span></span>
<span data-ttu-id="5e279-104">Þótt margar aðgerðir kostnaðarbókhalds felist í innri ferlum sem notandinn kemur ekki nálægt, til dæmis jöfnun færslna og sjálfvirk kostnaðarleiðrétting, eru nokkrir reitir, gluggar og skýrslur sem ætluð eru notendum sem vinna beint eða óbeint með kostnað vara eða aðgerða.</span><span class="sxs-lookup"><span data-stu-id="5e279-104">Although much of the cost accounting functionality is expressed in underlying processes with no user interaction, such as entry application and automatic cost adjustment, a number of fields, windows, and reports are aimed at users who directly or indirectly manage the cost of items or operations.</span></span>  

 <span data-ttu-id="5e279-105">Úthlutun kostnaðarauka til innkaupaskjala er dæmi um óbeinan kostnaðarbókhaldsverkhluta.</span><span class="sxs-lookup"><span data-stu-id="5e279-105">Assigning item charges to purchase documents is an example of an indirect cost accounting task.</span></span> <span data-ttu-id="5e279-106">Uppfærsla einingarkostnaðar samsetningar eða framleiðsluuppskriftarvöru er dæmi um beinni kostnaðarbókhaldsverkhluta.</span><span class="sxs-lookup"><span data-stu-id="5e279-106">Updating the unit cost of assembly or production BOM item is an example of a more direct cost accounting task.</span></span>  

 <span data-ttu-id="5e279-107">Eftirfarandi tafla lýsir röð verkefna með tenglum í efnisatriði þar sem þeim er lýst.</span><span class="sxs-lookup"><span data-stu-id="5e279-107">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>   

|<span data-ttu-id="5e279-108">**Til að**</span><span class="sxs-lookup"><span data-stu-id="5e279-108">**To**</span></span>|<span data-ttu-id="5e279-109">**Sjá**</span><span class="sxs-lookup"><span data-stu-id="5e279-109">**See**</span></span>|  
|------------|-------------|  
|<span data-ttu-id="5e279-110">Uppfæra reglulega eða sjálfkrafa kostnaðarverð einnar vöru eða fleiri til að flytja fram kostnaðarbreytingar innhreyfingarfærslna, eins og við kaup eða framleiðslufrálag til viðeigandi útleiðarfærslu, eins og vegna notkunar eða flutninga.</span><span class="sxs-lookup"><span data-stu-id="5e279-110">Periodically or automatically update the unit cost of one or multiple items to forward any cost changes from inbound entries, such as those for purchases or production output, to the related outbound entries, such as consumption or transfers.</span></span>|[<span data-ttu-id="5e279-111">Hvernig á að: Leiðrétta birgðakostnað</span><span class="sxs-lookup"><span data-stu-id="5e279-111">How to: Adjust Item Costs</span></span>](inventory-how-adjust-item-costs.md)|  
|<span data-ttu-id="5e279-112">Fá innsýn í virkni meðalkostnaðar til að taka verðákvarðanir eða rekja verðbreytingar vegna villna við gagnainnslátt.</span><span class="sxs-lookup"><span data-stu-id="5e279-112">Get insight into average cost dynamics to make pricing decisions or to track cost fluctuations caused by data entry errors.</span></span>|[<span data-ttu-id="5e279-113">Hvernig á að Skrá nýjar vörur</span><span class="sxs-lookup"><span data-stu-id="5e279-113">How to: Register New Items</span></span>](inventory-how-register-new-items.md)|  
|<span data-ttu-id="5e279-114">Búa til kostnaðarverð framleiðsluvöru með því að færa inn kostnaðarliðina þrjá: Efniskostnað, afkastakostnað og undirverktakakostnað.</span><span class="sxs-lookup"><span data-stu-id="5e279-114">Create a manufacturing item's standard cost by entering the three cost elements: material cost, capacity cost, and subcontractor cost.</span></span>|[<span data-ttu-id="5e279-115">Um umreikning staðalkostnaðar</span><span class="sxs-lookup"><span data-stu-id="5e279-115">About Calculating Standard Cost</span></span>](finance-about-calculating-standard-cost.md)|  
|<span data-ttu-id="5e279-116">Reikna kostnaðarverð framleiðsluuppskriftar miðað við kostnaðarverð undirliggjandi íhluta.</span><span class="sxs-lookup"><span data-stu-id="5e279-116">Calculate the unit cost of a BOM item based on the unit costs of its underlying components.</span></span>|[<span data-ttu-id="5e279-117">Hvernig á að: Vinna með uppskriftir</span><span class="sxs-lookup"><span data-stu-id="5e279-117">How to: Work with Bills of Material</span></span>](inventory-how-work-BOMs.md)|  
|<span data-ttu-id="5e279-118">Ljúka kostnaðarferli framleiðsluvöru með því að stilla kostnað og afstemma virðisfærslurnar við færslubókina.</span><span class="sxs-lookup"><span data-stu-id="5e279-118">Complete the costing life cycle of a produced item by adjusting the costs and reconciling the value entries with the general ledger.</span></span>|[<span data-ttu-id="5e279-119">Um lokinn framleiðslupantanakostnað</span><span class="sxs-lookup"><span data-stu-id="5e279-119">About Finished Production Order Costs</span></span>](finance-about-finished-production-order-costs.md)|  
|<span data-ttu-id="5e279-120">Breyta gildi vöru í birgðum eða gildi einnar birgðafærslu, t.d. innkaupa.</span><span class="sxs-lookup"><span data-stu-id="5e279-120">Change the value of an item in inventory or the value of one item ledger entry, such as a purchase transaction.</span></span>|[<span data-ttu-id="5e279-121">Hvernig á að: Endurmeta birgðir</span><span class="sxs-lookup"><span data-stu-id="5e279-121">How to: Revalue Inventory</span></span>](inventory-how-revalue-inventory.md)|
|<span data-ttu-id="5e279-122">Afturkalla handvirkt birgðajöfnunarfærslu eða setja aftur upp birgðafærslur sem forritið bjó til.</span><span class="sxs-lookup"><span data-stu-id="5e279-122">Manually undo an item application or reapply item ledger entries created by the program.</span></span>|[<span data-ttu-id="5e279-123">Hvernig á að: fjarlægja og endurjafna birgðabókafærslur</span><span class="sxs-lookup"><span data-stu-id="5e279-123">How to: Remove and Reapply Item Ledger Entries</span></span>](finance-how-to-remove-and-reapply-item-entries.md)|  
|<span data-ttu-id="5e279-124">Nota skal reitinn **Jafnað frá færslu** í birgðabókinni til að stofna handvirkt fasta jöfnun milli færslu á innleið og upphaflegrar færslu á útleið.</span><span class="sxs-lookup"><span data-stu-id="5e279-124">Use the **Applies-from Entry** field in the item journal to manually create a fixed application between an inbound transaction and the original outbound transaction.</span></span>|[<span data-ttu-id="5e279-125">Hvernig á að loka opnum færslum birgðahöfuðbókar vegna fastrar jöfnunar í birgðabók</span><span class="sxs-lookup"><span data-stu-id="5e279-125">How to: Close Open Item Ledger Entries Resulting from Fixed Application in the Item Journal</span></span>](finance-how-to-close-open-item-ledger-entries-resulting-from-fixed-application-in-the-item-journal.md)|  

## <a name="see-also"></a><span data-ttu-id="5e279-126">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="5e279-126">See Also</span></span>  
<span data-ttu-id="5e279-127">[Stjórna Birgðakostnaður](finance-manage-inventory-costs.md)
[Hönnunarupplýsingar: Birgðakostnaður](design-details-inventory-costing.md)</span><span class="sxs-lookup"><span data-stu-id="5e279-127">[Manage Inventory Costs](finance-manage-inventory-costs.md)
[Design Details: Inventory Costing](design-details-inventory-costing.md)</span></span>

