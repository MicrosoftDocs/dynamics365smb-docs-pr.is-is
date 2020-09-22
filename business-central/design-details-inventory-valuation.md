---
title: Hönnunarupplýsingar - Birgðavirði | Microsoft Docs
description: Birgðaverðmat er ákvörðun kostnaðar sem er úthlutað til birgðavara, eins og lýst með eftirfarandi jöfnu.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: d37ef45bc1232bf0811a14123a814f1bf57ee7c2
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/09/2020
ms.locfileid: "3787697"
---
# <a name="design-details-inventory-valuation"></a><span data-ttu-id="82f84-103">Hönnunarupplýsingar: Birgðavirði</span><span class="sxs-lookup"><span data-stu-id="82f84-103">Design Details: Inventory Valuation</span></span>
<span data-ttu-id="82f84-104">Birgðaverðmat er ákvörðun kostnaðar sem er úthlutað til birgðavara, eins og lýst með eftirfarandi jöfnu.</span><span class="sxs-lookup"><span data-stu-id="82f84-104">Inventory valuation XE "Inventory Valuation"  is the determination of the cost that is assigned to an inventory item, as expressed by the following equation.</span></span>  

<span data-ttu-id="82f84-105">Lokabirgðir = uppahafsbirgðir + nettóinnkaup – kostnaður seldra vara</span><span class="sxs-lookup"><span data-stu-id="82f84-105">Ending inventory = beginning inventory + net purchases – cost of goods sold</span></span>  

<span data-ttu-id="82f84-106">Útreikning á lagerverðmat notar reitinn **Kostnaðarupphæð (raunverul.)** í verðmæti færslum fyrir vöru.</span><span class="sxs-lookup"><span data-stu-id="82f84-106">The calculation of inventory valuation uses the **Cost Amount (Actual)** field of the value entries for the item.</span></span> <span data-ttu-id="82f84-107">Færslurnar eru flokkaðar eftir gerð sem samsvarar kostnaðarþætti, beinum kostnaði, óbeinum kostnaði, dreifni, endurmati og námundun.</span><span class="sxs-lookup"><span data-stu-id="82f84-107">The entries are classified according to the entry type XE "Entry Type"  that corresponds to the cost components, direct cost, indirect cost, variance, revaluation, and rounding.</span></span> <span data-ttu-id="82f84-108">Nánari upplýsingar eru í [Upplýsingar um hönnun: kostnaðarhlutar](design-details-cost-components.md).</span><span class="sxs-lookup"><span data-stu-id="82f84-108">For more information, see [Design Details: Cost Components](design-details-cost-components.md).</span></span>  

<span data-ttu-id="82f84-109">Færslur eru jafnaðar hver við aðra, annaðhvort með fastri jöfnun XE „Jöfnun; Föst“ eða samkvæmt almennri kostnaðarflæðisáætlun sem skilgreind er af kostnaðaraðferðinni XE „Aðferð; Kostnaður“  XE „Kostnaðaraðferð“.</span><span class="sxs-lookup"><span data-stu-id="82f84-109">Entries are applied against each other, either by the fixed application XE "Application; Fixed" , or according to the general cost-flow assumption defined by the costing method XE "Method; Costing"  XE "Costing Method" .</span></span> <span data-ttu-id="82f84-110">Ein færsla birgðaminnkunar getur verið jöfnuð við meira en eina aukningarfærslu með öðrum bókunardagsetningum og mögulega öðru kaupverði.</span><span class="sxs-lookup"><span data-stu-id="82f84-110">One entry of inventory decrease can be applied to more than one increase entry with different posting dates and possibly different acquisition cost XE "Acquisition Cost" s.</span></span> <span data-ttu-id="82f84-111">Nánari upplýsingar eru í [Upplýsingar um hönnun: Vörujöfnun](design-details-item-application.md).</span><span class="sxs-lookup"><span data-stu-id="82f84-111">For more information, see [Design Details: Item Application](design-details-item-application.md).</span></span> <span data-ttu-id="82f84-112">Því byggir útreikningur á birgðavirði fyrir tiltekna dagsetningu á samantekt jákvæðra og neikvæðra virðisfærslna.</span><span class="sxs-lookup"><span data-stu-id="82f84-112">Therefore, calculation of the inventory value XE "Inventory Value"  for a given date is based on summing up positive and negative value entries.</span></span>  

## <a name="inventory-valuation-report"></a><span data-ttu-id="82f84-113">Birgðavirðisskýrsla</span><span class="sxs-lookup"><span data-stu-id="82f84-113">Inventory Valuation report</span></span>  
<span data-ttu-id="82f84-114">Til að reikna út birgðavirði í **Birgðavirðisskýrslu** hefst skýrslan með því að reikna verðmæti birgðabreytinga atriðisins á tilteknu upphafsdag.</span><span class="sxs-lookup"><span data-stu-id="82f84-114">To calculate the inventory value in the **Inventory Valuation** report, the report begins by calculating the value of the item’s inventory at a given starting date.</span></span> <span data-ttu-id="82f84-115">Taflan bætir svo virði birgðaaukningar við og dregur frá virði birgðaminnkunar, upp að uppgefinni lokadagsetningu.</span><span class="sxs-lookup"><span data-stu-id="82f84-115">It then adds the value of inventory increases and subtracts the value of inventory decreases up to a given ending date.</span></span> <span data-ttu-id="82f84-116">Lokaniðurstaðan er birgðavirði á lokadag.</span><span class="sxs-lookup"><span data-stu-id="82f84-116">The end result is the inventory value on the ending date.</span></span> <span data-ttu-id="82f84-117">Skýrslan reiknar þessi gildi út með því að reikna út samtölu gildanna í reitnum **Kostnaðarupphæð (raunverul)** í gildafærslunum, með því að nota bókunardagsetningar til að afmarka.</span><span class="sxs-lookup"><span data-stu-id="82f84-117">The report calculates these values by summing the values in the **Cost Amount (Actual)** field in the value entries, using the posting dates as filters.</span></span>  

<span data-ttu-id="82f84-118">Prentaða skýrslan sýnir alltaf raunupphæðir, þ.e. verðgildi færslna sem hafa verið bókaðar sem reikningsfærðar.</span><span class="sxs-lookup"><span data-stu-id="82f84-118">The printed report always shows actual amounts, that is, the cost of entries that have been posted as invoiced.</span></span> <span data-ttu-id="82f84-119">Í skýrslunni er einnig prentaður væntanlegur kostnaður fyrir færslur sem bókaðar eru sem mótteknar eða afhentar ef gátmerki er valið í reitnum Taka með væntanl. kostn. á flýtiflipanum Valkostir.</span><span class="sxs-lookup"><span data-stu-id="82f84-119">The report will also print the expected cost of entries that have posted as received or shipped, if you select the Include Expected Cost field on the Options FastTab.</span></span>  

> [!IMPORTANT]  
>  <span data-ttu-id="82f84-120">Gildi í **Birgðavirði** skýrslu er afstemmt við Birgðareikninginn í fjárhag, sem þýðir að virðisfærslur sem um ræðir hafa verið bókaðar í fjárhag.</span><span class="sxs-lookup"><span data-stu-id="82f84-120">Values in the **Inventory Valuation** report is reconciled with the Inventory account in the general ledger, meaning the value entries in question have been posted to the general ledger.</span></span>  

> [!IMPORTANT]  
>  <span data-ttu-id="82f84-121">Fjárhæðir í dálkunum **Virði** í skýrslunni eru byggðar á bókunardagsetningu færslna fyrir vöru.</span><span class="sxs-lookup"><span data-stu-id="82f84-121">Amounts in the **Value** columns of the report are based on the posting date of transactions for an item.</span></span>  

## <a name="inventory-valuation---wip-report"></a><span data-ttu-id="82f84-122">Birgðavirði - VÍV-skýrsla</span><span class="sxs-lookup"><span data-stu-id="82f84-122">Inventory Valuation - WIP report</span></span>  
<span data-ttu-id="82f84-123">Framleiðslufyrirtæki þarf að velja gildi fyrir þrenns konar birgðir:</span><span class="sxs-lookup"><span data-stu-id="82f84-123">A manufacturing company needs to determine the value of three types of inventory:</span></span>  

* <span data-ttu-id="82f84-124">Hráefnisbirgðir</span><span class="sxs-lookup"><span data-stu-id="82f84-124">Raw Materials inventory</span></span>  
* <span data-ttu-id="82f84-125">VÍV-birgðir</span><span class="sxs-lookup"><span data-stu-id="82f84-125">WIP inventory</span></span>  
* <span data-ttu-id="82f84-126">Fullunnar vörur í birgðum</span><span class="sxs-lookup"><span data-stu-id="82f84-126">Finished Goods inventory</span></span>  

<span data-ttu-id="82f84-127">Gildi VÍV-birgða er ákvarðar samkvæmt eftirfarandi jöfnu.</span><span class="sxs-lookup"><span data-stu-id="82f84-127">The value of WIP inventory is determined by the following equation:</span></span>  

* <span data-ttu-id="82f84-128">Lokabirgðir VÍV = Upphafsbirgðir VÍV + framleiðslukostnaður – kostnaður framleiddra vara</span><span class="sxs-lookup"><span data-stu-id="82f84-128">Ending WIP inventory = Beginning WIP inventory + manufacturing costs – cost of goods manufactured</span></span>  

<span data-ttu-id="82f84-129">Eins og fyrir keyptar birgðir eru virðisfærslur grunnur birgðamats.</span><span class="sxs-lookup"><span data-stu-id="82f84-129">As for purchased inventory, the value entries provide the basis of the inventory valuation.</span></span> <span data-ttu-id="82f84-130">Útreikningur er gerður því að nota gildin í reitnum **Kostnaðarupphæð (raunverul.)** fyrir vöruna og afkastagildisfærslurnar sem tengjast framleiðslupöntun.</span><span class="sxs-lookup"><span data-stu-id="82f84-130">The calculation is made using the values in the **Cost Amount (Actual)** field of the item and capacity value entries associated with a production order.</span></span>  

<span data-ttu-id="82f84-131">Tilgangurinn með VÍV-verðmati á birgðum er að ákvarða virði þeirra vara sem ekki eru enn fullunnar á tiltekinni dagsetningu.</span><span class="sxs-lookup"><span data-stu-id="82f84-131">The purpose of WIP inventory valuation is to determine the value of the items whose manufacturing has not yet been completed on a given date.</span></span> <span data-ttu-id="82f84-132">Því byggist VÍV-birgðavirðið á virðisfærslum tengdum notkun og færslum í afkastahöfuðbók.</span><span class="sxs-lookup"><span data-stu-id="82f84-132">Therefore the WIP inventory value is based on the value entries related to the consumption and capacity ledger entries.</span></span> <span data-ttu-id="82f84-133">Fjárhagsfærslur um notkun verða að vera að fullu reikningsfærðar á dagsetningu fullgildingar.</span><span class="sxs-lookup"><span data-stu-id="82f84-133">Consumption ledger entries must be completely invoiced at the date of the valuation.</span></span> <span data-ttu-id="82f84-134">Því sýnir **Verðmæti birgða VÍV** skýrslan kostnaðinn sem endurspeglar VÍV-birgðavirðið í tveimur flokkum: notkun og afkastageta.</span><span class="sxs-lookup"><span data-stu-id="82f84-134">Therefore, the **Inventory Valuation – WIP** report shows the costs representing the WIP inventory value in two categories: consumption and capacity.</span></span>  

## <a name="see-also"></a><span data-ttu-id="82f84-135">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="82f84-135">See Also</span></span>  
<span data-ttu-id="82f84-136">[Hönnunarupplýsingar: afstemming í fjárhag](design-details-reconciliation-with-the-general-ledger.md) </span><span class="sxs-lookup"><span data-stu-id="82f84-136">[Design Details: Reconciliation with the General Ledger](design-details-reconciliation-with-the-general-ledger.md) </span></span>  
<span data-ttu-id="82f84-137">[Hönnunarupplýsingar: Endurmat](design-details-revaluation.md) </span><span class="sxs-lookup"><span data-stu-id="82f84-137">[Design Details: Revaluation](design-details-revaluation.md) </span></span>  
<span data-ttu-id="82f84-138">[Hönnunarupplýsingar: Bókun framleiðslupöntunar](design-details-production-order-posting.md)
[Stjórna birgðakostnaði](finance-manage-inventory-costs.md)</span><span class="sxs-lookup"><span data-stu-id="82f84-138">[Design Details: Production Order Posting](design-details-production-order-posting.md)
[Managing Inventory Costs](finance-manage-inventory-costs.md)</span></span>  
[<span data-ttu-id="82f84-139">Fjármál</span><span class="sxs-lookup"><span data-stu-id="82f84-139">Finance</span></span>](finance.md)  
<span data-ttu-id="82f84-140">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="82f84-140">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
