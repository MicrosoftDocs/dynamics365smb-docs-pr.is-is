---
title: Hvernig á að nota mælieiningu framleiðslukeyrslu | Microsoft Docs
description: Ef vara er sett á lager eftir einni mælieiningu en framleidd eftir annarri, verður framleiðslupöntunin að notar mælieiningu framleiðslukeyrslu til að reikna út rétt magn íhluta. Dæmi um útreikning með mælieiningu framleiðslukeyrslu er þegar framleiddur hlutur er merktur á lager í stykkjum en framleiddur í tonnum.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: c78430de1c45646e54fb8551cd4a8dcfbbfcc4e4
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5383301"
---
# <a name="work-with-manufacturing-batch-units-of-measure"></a><span data-ttu-id="3182e-104">Vinna með mælieiningu framleiðslukeyrslu</span><span class="sxs-lookup"><span data-stu-id="3182e-104">Work with Manufacturing Batch Units of Measure</span></span>
<span data-ttu-id="3182e-105">Ef vara er sett á lager eftir einni mælieiningu en framleidd eftir annarri er framleiðslupöntun stofnuð sem notar mælieiningu framleiðslukeyrslu til að reikna út rétt magn íhluta meðan á keyrslunni **Endurnýjun framleiðslupöntunar** stendur.</span><span class="sxs-lookup"><span data-stu-id="3182e-105">If an item is stocked in one unit of measure but produced in another, a production order is created that uses a manufacturing batch unit of measure to calculate the correct quantity of the components during the **Refresh Production Order** batch job.</span></span> <span data-ttu-id="3182e-106">Dæmi um útreikning með mælieiningu framleiðslukeyrslu er þegar framleiddur hlutur er merktur á lager í stykkjum en framleiddur í tonnum.</span><span class="sxs-lookup"><span data-stu-id="3182e-106">An example of a manufacturing batch unit of measure calculation is when a manufactured item is stocked in pieces but produced in tons.</span></span>  

## <a name="to-create-a-production-bom-using-a-batch-unit-of-measure"></a><span data-ttu-id="3182e-107">Til að stofna framleiðsluuppskrift með því að nota keyrslumælieininguna:</span><span class="sxs-lookup"><span data-stu-id="3182e-107">To create a production BOM using a batch unit of measure</span></span>  
1.  <span data-ttu-id="3182e-108">Mælieining framleiðslukeyrslu er sett upp sem mælieiningarvalkostur á síðunni **Mælieiningar vöru** á vörunni sem á að framleiða.</span><span class="sxs-lookup"><span data-stu-id="3182e-108">The manufacturing batch unit of measure is set up as an alternative unit of measure on the **Item Units of Measure** page on the item to be produced.</span></span> <span data-ttu-id="3182e-109">Keyrslumælieiningin kemur ekki í staðinn fyrir Grunnmælieininguna á vörunni.</span><span class="sxs-lookup"><span data-stu-id="3182e-109">The batch unit of measure will not replace the base unit of measure on the item.</span></span>  
2.  <span data-ttu-id="3182e-110">Stofnuð er framleiðsluuppskrift fyrir vöruna sem er sett upp með mælieiningu framleiðslukeyrslu.</span><span class="sxs-lookup"><span data-stu-id="3182e-110">Create a production BOM for the item set up with the manufacturing batch unit of measure.</span></span> <span data-ttu-id="3182e-111">Frekari upplýsingar eru í [Stofna framleiðsluuppskriftir](production-how-to-create-production-boms.md).</span><span class="sxs-lookup"><span data-stu-id="3182e-111">For more information, see [Create Production BOMs](production-how-to-create-production-boms.md).</span></span>  
3.  <span data-ttu-id="3182e-112">Í reitnum **Mælieiningarkóti** er mælieining framleiðslukeyrslu valin.</span><span class="sxs-lookup"><span data-stu-id="3182e-112">In the **Unit of Measure Code** field, select the manufacturing batch unit of measure.</span></span>  
4.  <span data-ttu-id="3182e-113">Fyrir hverja framleiðsluuppskriftarlínu í reitnum **Magn á** er slegið inn magnið af þessum vöruíhlut sem þarf til að stofna þessa keyrslumælieiningu.</span><span class="sxs-lookup"><span data-stu-id="3182e-113">For each production BOM line, in the **Quantity Per** field, enter the quantity of this component item that is required to create this batch unit of measure.</span></span>  
5.  <span data-ttu-id="3182e-114">Opna **Birgðaspjald** fyrir vöruna sem á í hlut.</span><span class="sxs-lookup"><span data-stu-id="3182e-114">Open the **Item Card** for the related item.</span></span>  

    <span data-ttu-id="3182e-115">Á flýtiflipanum **Áfyllingu**, í reitnum **Framleiðsluuppskriftarnr.**, er framleiðsluuppskriftin valin sem stofnuð var fyrir ofan.</span><span class="sxs-lookup"><span data-stu-id="3182e-115">On the **Replenishment** FastTab, in the **Production BOM No.** field, select the production BOM created above.</span></span>  
6.  <span data-ttu-id="3182e-116">Stofnaður er framleiðslupöntunarhaus með því að nota vöruna sem er sett upp með mælieiningu framleiðslukeyrslu.</span><span class="sxs-lookup"><span data-stu-id="3182e-116">Create a production order header using the item set up with the manufacturing batch unit of measure.</span></span> <span data-ttu-id="3182e-117">Frekari upplýsingar eru í [Stofna framleiðslupantanir](production-how-to-create-production-orders.md).</span><span class="sxs-lookup"><span data-stu-id="3182e-117">For more information, see [Create Production Orders](production-how-to-create-production-orders.md).</span></span>  
7.  <span data-ttu-id="3182e-118">Veldu aðgerðina **Uppfæra** og veldu síðan **Í lagi** hnappinn.</span><span class="sxs-lookup"><span data-stu-id="3182e-118">Choose the **Refresh** action, and then choose  the **OK** button.</span></span>  

<span data-ttu-id="3182e-119">Á flýtiflipanum **Línur** skal velja aðgerðina **Lína**, og velja svo aðgerðina **Íhlutir** til að skoða niðurstöðurnar.</span><span class="sxs-lookup"><span data-stu-id="3182e-119">On the **Lines** FastTab, choose the **Line** action, and then choose the **Components** action to view the result.</span></span> <span data-ttu-id="3182e-120">Forritið reiknar út rétt magn íhluta sem þarf til að fullnægja framleiðsluuppskriftinni á grundvelli mælieiningu framleiðslukeyrslu.</span><span class="sxs-lookup"><span data-stu-id="3182e-120">The application calculates the correct quantity of the components needed to satisfy the production BOM based on the manufacturing batch unit of measure.</span></span>  

## <a name="to-calculate-a-manufacturing-batch-unit-of-measure-on-a-production-order"></a><span data-ttu-id="3182e-121">Til að reikna út Mælieiningu framleiðslukeyrslu á Framleiðslupöntun:</span><span class="sxs-lookup"><span data-stu-id="3182e-121">To calculate a manufacturing batch unit of measure on a production order</span></span>  
1.  <span data-ttu-id="3182e-122">Stofnaður er framleiðslupöntunarhaus með því að nota vöruna sem er sett upp með mælieiningu framleiðslukeyrslu.</span><span class="sxs-lookup"><span data-stu-id="3182e-122">Create a production order header using the item set up with the manufacturing batch unit of measure.</span></span>  
2.  <span data-ttu-id="3182e-123">Í reitnum **Vörunr.** í Framleiðslupöntunarlínunni er slegið inn sama vörunúmer og notað er í hausnum.</span><span class="sxs-lookup"><span data-stu-id="3182e-123">In the **Item No.** field in the Production Order line, type the same item number used in the header.</span></span>  
3.  <span data-ttu-id="3182e-124">Í reitnum **Magn** er slegið inn sama magn og er notað í hausnum.</span><span class="sxs-lookup"><span data-stu-id="3182e-124">In the **Quantity** field, enter the same quantity used in the header.</span></span>  
4.  <span data-ttu-id="3182e-125">Í reitnum **Mælieiningarkóti** er mælieiningarkóti framleiðslukeyrslu valinn.</span><span class="sxs-lookup"><span data-stu-id="3182e-125">In the **Unit of Measure Code** field, select the manufacturing batch unit of measure code.</span></span>  
5.  <span data-ttu-id="3182e-126">Velja aðgerðina **Uppfæra**.</span><span class="sxs-lookup"><span data-stu-id="3182e-126">Choose the **Refresh** action.</span></span>
6.  <span data-ttu-id="3182e-127">Á flýtiflipanum **Reikna** skal hreinsa gátreitinn **Línur**.</span><span class="sxs-lookup"><span data-stu-id="3182e-127">On the **Calculate** FastTab, clear the **Lines** check box.</span></span>  
7.  <span data-ttu-id="3182e-128">Velja hnappinn **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="3182e-128">Choose the **OK** button.</span></span>  
8.  <span data-ttu-id="3182e-129">Á flýtiflipanum **Línur** skal velja aðgerðina **Lína**, og velja svo aðgerðina **Íhlutir** til að skoða niðurstöðurnar.</span><span class="sxs-lookup"><span data-stu-id="3182e-129">On the **Lines** FastTab, choose the **Line** action, and then choose the **Components** action to view the result.</span></span> <span data-ttu-id="3182e-130">Rétt magn íhluta sem þarf til að fullnægja framleiðsluuppskriftinni er reiknað út á grundvelli mælieiningu framleiðslukeyrslu.</span><span class="sxs-lookup"><span data-stu-id="3182e-130">The correct quantity of the components needed to satisfy the production BOM is calculated based on the manufacturing batch unit of measure.</span></span>  

## <a name="see-also"></a><span data-ttu-id="3182e-131">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="3182e-131">See Also</span></span>  
[<span data-ttu-id="3182e-132">Stofna leiðir</span><span class="sxs-lookup"><span data-stu-id="3182e-132">Create Routings</span></span>](production-how-to-create-routings.md)  
<span data-ttu-id="3182e-133">[Búa til framleiðsluuppskriftir](production-how-to-create-production-boms.md)   </span><span class="sxs-lookup"><span data-stu-id="3182e-133">[Create Production BOMs](production-how-to-create-production-boms.md)   </span></span>  
[<span data-ttu-id="3182e-134">Uppsetning framleiðslu</span><span class="sxs-lookup"><span data-stu-id="3182e-134">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="3182e-135">[Framleiðsla](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="3182e-135">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
<span data-ttu-id="3182e-136">[Áætlun](production-planning.md) </span><span class="sxs-lookup"><span data-stu-id="3182e-136">[Planning](production-planning.md) </span></span>  
[<span data-ttu-id="3182e-137">Birgðir</span><span class="sxs-lookup"><span data-stu-id="3182e-137">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="3182e-138">Innkaup</span><span class="sxs-lookup"><span data-stu-id="3182e-138">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="3182e-139">[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="3182e-139">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  


[!INCLUDE[footer-include](includes/footer-banner.md)]