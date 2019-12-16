---
title: Meðhöndla birgða- og framleiðslukostnað | Microsoft Docs
description: Þótt margar aðgerðir kostnaðarbókhalds felist í innri ferlum sem notandinn kemur ekki nálægt, til dæmis jöfnun færslna og sjálfvirk kostnaðarleiðrétting, eru nokkrir reitir, síður og skýrslur sem ætluð eru notendum sem vinna beint eða óbeint með kostnað vara eða aðgerða.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 8eceae6e325d4b5c1cf5cc4b0ba509c4624dd9f4
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/03/2019
ms.locfileid: "2879777"
---
# <a name="handling-inventory-and-manufacturing-costs"></a><span data-ttu-id="4949b-103">Meðhöndla birgða- og framleiðslukostnað</span><span class="sxs-lookup"><span data-stu-id="4949b-103">Handling Inventory and Manufacturing Costs</span></span>
<span data-ttu-id="4949b-104">Þótt margar aðgerðir kostnaðarbókhalds felist í innri ferlum sem notandinn kemur ekki nálægt, til dæmis jöfnun færslna og sjálfvirk kostnaðarleiðrétting, eru nokkrir reitir, síður og skýrslur sem ætluð eru notendum sem vinna beint eða óbeint með kostnað vara eða aðgerða.</span><span class="sxs-lookup"><span data-stu-id="4949b-104">Although much of the cost accounting functionality is expressed in underlying processes with no user interaction, such as entry application and automatic cost adjustment, a number of fields, pages, and reports are aimed at users who directly or indirectly manage the cost of items or operations.</span></span>  

 <span data-ttu-id="4949b-105">Úthlutun kostnaðarauka til innkaupaskjala er dæmi um óbeinan kostnaðarbókhaldsverkhluta.</span><span class="sxs-lookup"><span data-stu-id="4949b-105">Assigning item charges to purchase documents is an example of an indirect cost accounting task.</span></span> <span data-ttu-id="4949b-106">Uppfærsla einingarkostnaðar samsetningar eða framleiðsluuppskriftarvöru er dæmi um beinni kostnaðarbókhaldsverkhluta.</span><span class="sxs-lookup"><span data-stu-id="4949b-106">Updating the unit cost of assembly or production BOM item is an example of a more direct cost accounting task.</span></span>  

 <span data-ttu-id="4949b-107">Eftirfarandi tafla lýsir röð verkefna með tenglum í efnisatriði þar sem þeim er lýst.</span><span class="sxs-lookup"><span data-stu-id="4949b-107">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>   

|<span data-ttu-id="4949b-108">**Til að**</span><span class="sxs-lookup"><span data-stu-id="4949b-108">**To**</span></span>|<span data-ttu-id="4949b-109">**Sjá**</span><span class="sxs-lookup"><span data-stu-id="4949b-109">**See**</span></span>|  
|------------|-------------|  
|<span data-ttu-id="4949b-110">Uppfæra reglulega eða sjálfkrafa kostnaðarverð einnar vöru eða fleiri til að flytja fram kostnaðarbreytingar innhreyfingarfærslna, eins og við kaup eða framleiðslufrálag til viðeigandi útleiðarfærslu, eins og vegna notkunar eða flutninga.</span><span class="sxs-lookup"><span data-stu-id="4949b-110">Periodically or automatically update the unit cost of one or multiple items to forward any cost changes from inbound entries, such as those for purchases or production output, to the related outbound entries, such as consumption or transfers.</span></span>|[<span data-ttu-id="4949b-111">Leiðr. kostnað vara</span><span class="sxs-lookup"><span data-stu-id="4949b-111">Adjust Item Costs</span></span>](inventory-how-adjust-item-costs.md)|  
|<span data-ttu-id="4949b-112">Fá innsýn í virkni meðalkostnaðar til að taka verðákvarðanir eða rekja verðbreytingar vegna villna við gagnainnslátt.</span><span class="sxs-lookup"><span data-stu-id="4949b-112">Get insight into average cost dynamics to make pricing decisions or to track cost fluctuations caused by data entry errors.</span></span>|[<span data-ttu-id="4949b-113">Skrá nýjar vörur</span><span class="sxs-lookup"><span data-stu-id="4949b-113">Register New Items</span></span>](inventory-how-register-new-items.md)|  
|<span data-ttu-id="4949b-114">Búa til kostnaðarverð framleiðsluvöru með því að færa inn kostnaðarliðina þrjá: Efniskostnað, afkastakostnað og undirverktakakostnað.</span><span class="sxs-lookup"><span data-stu-id="4949b-114">Create a manufacturing item's standard cost by entering the three cost elements: material cost, capacity cost, and subcontractor cost.</span></span>|[<span data-ttu-id="4949b-115">Um umreikning staðalkostnaðar</span><span class="sxs-lookup"><span data-stu-id="4949b-115">About Calculating Standard Cost</span></span>](finance-about-calculating-standard-cost.md)|  
|<span data-ttu-id="4949b-116">Reikna kostnaðarverð framleiðsluuppskriftar miðað við kostnaðarverð undirliggjandi íhluta.</span><span class="sxs-lookup"><span data-stu-id="4949b-116">Calculate the unit cost of a BOM item based on the unit costs of its underlying components.</span></span>|[<span data-ttu-id="4949b-117">Vinna með uppskriftir</span><span class="sxs-lookup"><span data-stu-id="4949b-117">Work with Bills of Material</span></span>](inventory-how-work-BOMs.md)|  
|<span data-ttu-id="4949b-118">Ljúka kostnaðarferli framleiðsluvöru með því að stilla kostnað og afstemma virðisfærslurnar við færslubókina.</span><span class="sxs-lookup"><span data-stu-id="4949b-118">Complete the costing life cycle of a produced item by adjusting the costs and reconciling the value entries with the general ledger.</span></span>|[<span data-ttu-id="4949b-119">Um lokinn framleiðslupantanakostnað</span><span class="sxs-lookup"><span data-stu-id="4949b-119">About Finished Production Order Costs</span></span>](finance-about-finished-production-order-costs.md)|  
|<span data-ttu-id="4949b-120">Breyta gildi vöru í birgðum eða gildi einnar birgðafærslu, t.d. innkaupa.</span><span class="sxs-lookup"><span data-stu-id="4949b-120">Change the value of an item in inventory or the value of one item ledger entry, such as a purchase transaction.</span></span>|[<span data-ttu-id="4949b-121">Endurmat birgða</span><span class="sxs-lookup"><span data-stu-id="4949b-121">Revalue Inventory</span></span>](inventory-how-revalue-inventory.md)|
|<span data-ttu-id="4949b-122">Afturkalla handvirkt birgðajöfnunarfærslu eða setja aftur upp birgðafærslur sem forritið bjó til.</span><span class="sxs-lookup"><span data-stu-id="4949b-122">Manually undo an item application or reapply item ledger entries created by application.</span></span>|[<span data-ttu-id="4949b-123">Fjarlægja og endurjafna birgðabókafærslur</span><span class="sxs-lookup"><span data-stu-id="4949b-123">Remove and Reapply Item Ledger Entries</span></span>](finance-how-to-remove-and-reapply-item-entries.md)|  
|<span data-ttu-id="4949b-124">Nota skal reitinn **Jafnað frá færslu** í birgðabókinni til að stofna handvirkt fasta jöfnun milli færslu á innleið og upphaflegrar færslu á útleið.</span><span class="sxs-lookup"><span data-stu-id="4949b-124">Use the **Applies-from Entry** field in the item journal to manually create a fixed application between an inbound transaction and the original outbound transaction.</span></span>|[<span data-ttu-id="4949b-125">Loka opnum færslum birgðahöfuðbókar vegna fastrar jöfnunar í birgðabók</span><span class="sxs-lookup"><span data-stu-id="4949b-125">Close Open Item Ledger Entries Resulting from Fixed Application in the Item Journal</span></span>](finance-how-to-close-open-item-ledger-entries-resulting-from-fixed-application-in-the-item-journal.md)|  

## <a name="see-also"></a><span data-ttu-id="4949b-126">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="4949b-126">See Also</span></span>  
<span data-ttu-id="4949b-127">[Stjórna Birgðakostnaður](finance-manage-inventory-costs.md)
[Hönnunarupplýsingar: Birgðakostnaður](design-details-inventory-costing.md)</span><span class="sxs-lookup"><span data-stu-id="4949b-127">[Manage Inventory Costs](finance-manage-inventory-costs.md)
[Design Details: Inventory Costing](design-details-inventory-costing.md)</span></span>
