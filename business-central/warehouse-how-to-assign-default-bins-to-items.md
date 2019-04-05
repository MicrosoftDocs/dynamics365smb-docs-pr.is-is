---
title: Hvernig á að úthluta vörum sjálfgefnum hólfum | Microsoft Docs
description: Ef hólf eru notuð í birgðageymslu verður öll móttaka, afhending og hreyfing á vörum mun auðveldari ef sjálfgefin hólf eru notuð. Þegar sjálfgefið hólf er tengt vöru leggur kerfið það til í hvert sinn sem færsla fer í gang fyrir vöruna.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: 290c26639234f3379fb4f9b6790fc511e17f683e
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/08/2019
ms.locfileid: "800010"
---
# <a name="assign-default-bins-to-items"></a><span data-ttu-id="94130-104">Sjálfgefin hólf tengd vörum</span><span class="sxs-lookup"><span data-stu-id="94130-104">Assign Default Bins to Items</span></span>
<span data-ttu-id="94130-105">Ef hólf eru notuð í birgðageymslu verður öll móttaka, afhending og hreyfing á vörum mun auðveldari ef sjálfgefin hólf eru notuð.</span><span class="sxs-lookup"><span data-stu-id="94130-105">If you are using bins at a location, assigning default bins to your items can make the process of shipping, receiving, and moving your items much easier.</span></span> <span data-ttu-id="94130-106">Þegar sjálfgefið hólf er tengt vöru leggur kerfið það til í hvert sinn sem færsla fer í gang fyrir vöruna.</span><span class="sxs-lookup"><span data-stu-id="94130-106">When a default bin is assigned to an item, this bin is suggested every time you initiate a transaction for this item.</span></span> <span data-ttu-id="94130-107">Sjálfgefin hólf eru skilgreind á síðunni **Innihald hólfs**.</span><span class="sxs-lookup"><span data-stu-id="94130-107">Default bins are defined on the **Bin Content** page.</span></span>  

## <a name="to-assign-a-default-bin-to-an-item"></a><span data-ttu-id="94130-108">Að úthluta vöru sjálfgefnu hólfi</span><span class="sxs-lookup"><span data-stu-id="94130-108">To assign a default bin to an item</span></span>
1.  <span data-ttu-id="94130-109">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Vinnublað f. stofnun hólfainnihalds** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="94130-109">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Bin Content Creation Worksheet**, and choose the related link.</span></span>  
2.  <span data-ttu-id="94130-110">Tilgreindur er hólfkóti og vöruupplýsingar fyrir hvert hólf sem á að verða sjálfgefið og vöru.</span><span class="sxs-lookup"><span data-stu-id="94130-110">Fill in the bin code and item information for each bin that you would like to set up as a default for an item.</span></span> <span data-ttu-id="94130-111">Gæta skal þess að velja reitinn **Sjálfgefið**.</span><span class="sxs-lookup"><span data-stu-id="94130-111">Make sure to select the **Default** field.</span></span>  
3.  <span data-ttu-id="94130-112">Valið er **Stofna innihald hólfa** aðgerð.</span><span class="sxs-lookup"><span data-stu-id="94130-112">Choose the **Create Bin Content** action.</span></span> <span data-ttu-id="94130-113">Sjálfgefin hólf hafa nú verið tengd vörunum.</span><span class="sxs-lookup"><span data-stu-id="94130-113">Default bins are now assigned for your item.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="94130-114">Þegar gengið er frá vöru og hún er ekki með sjálfgefið hólf gerir kerfið hólfið sem hún er sett í sjálfgefið.</span><span class="sxs-lookup"><span data-stu-id="94130-114">When an item is put away, if the item does not have a default bin assigned, the bin where the item is put away is assigned as the default.</span></span>  

## <a name="to-change-the-default-bin-for-an-item"></a><span data-ttu-id="94130-115">Skipt um sjálfgefið hólf vöru</span><span class="sxs-lookup"><span data-stu-id="94130-115">To change the default bin for an item</span></span>  
<span data-ttu-id="94130-116">Stundum getur þurft að skipta um sjálfgefið hólf vöru eða gefa nýrri vöru sjálfgefið hólf.</span><span class="sxs-lookup"><span data-stu-id="94130-116">You may need to change the default bin assignment for an item or assign a default bin to a new item.</span></span>    
1.  <span data-ttu-id="94130-117">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **innihald hólfs** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="94130-117">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Bin Contents**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="94130-118">Í reitnum **Birgðageymsluafmörkun** er valinn réttur birgðageymslukóti.</span><span class="sxs-lookup"><span data-stu-id="94130-118">In the **Location Filter** field, select the appropriate location code.</span></span>  
3.  <span data-ttu-id="94130-119">Gildandi sjálfgefið hólfafærsla vörunnar er fundið og gátreitur **Sjálfgefið hólf** er hreinsaður.</span><span class="sxs-lookup"><span data-stu-id="94130-119">Find the current default bin content entry for the item and clear the **Default Bin** check box.</span></span>  
4.  <span data-ttu-id="94130-120">Hólfinnihaldslína hólfsins sem á að verða sjálfgefið er fundin.</span><span class="sxs-lookup"><span data-stu-id="94130-120">Find the bin content line for the bin that you would like as the new default bin.</span></span> <span data-ttu-id="94130-121">Veljið gátreitinn **Sjálfgefið hólf**.</span><span class="sxs-lookup"><span data-stu-id="94130-121">Select the **Default Bin** check box.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="94130-122">Þegar gengið er frá vöru í fyrsta skipti og hún er ekki með sjálfgefið hólf gerir kerfið hólfið sem hún er sett í sjálfgefið.</span><span class="sxs-lookup"><span data-stu-id="94130-122">When an item is put away for the first time, and the item does not have a default bin assigned, the system will assign the bin where the item is put away as the default bin for the item.</span></span>  

## <a name="see-also"></a><span data-ttu-id="94130-123">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="94130-123">See Also</span></span>  
[<span data-ttu-id="94130-124">Vöruhúsastjórnun</span><span class="sxs-lookup"><span data-stu-id="94130-124">Warehouse Management</span></span>](warehouse-manage-warehouse.md)  
[<span data-ttu-id="94130-125">Birgðir</span><span class="sxs-lookup"><span data-stu-id="94130-125">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="94130-126">[Vöruhúsastjórnun sett upp](warehouse-setup-warehouse.md)   </span><span class="sxs-lookup"><span data-stu-id="94130-126">[Setting Up Warehouse Management](warehouse-setup-warehouse.md)   </span></span>  
<span data-ttu-id="94130-127">[Samsetningardeild](assembly-assemble-items.md)  </span><span class="sxs-lookup"><span data-stu-id="94130-127">[Assembly Management](assembly-assemble-items.md)  </span></span>  
[<span data-ttu-id="94130-128">Hönnunarupplýsingar vöruhúsakerfi</span><span class="sxs-lookup"><span data-stu-id="94130-128">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="94130-129">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="94130-129">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
