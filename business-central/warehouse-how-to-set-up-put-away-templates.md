---
title: Hvernig á að setja upp Frágangssniðmát | Microsoft Docs
description: Ef notaður er beinn frágangur og tínsla er stungið upp á því hólfi sem best hentar vörunum á hverjum tíma samkvæmt frágangssniðmátinu sem sett hefur verið upp fyrir vöruhúsið, hólfaflokkuninni sem hólfin hafa fengið, og hámarks- og lágmarksmagninu sem sett hefur verið upp fyrir föst hólf.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 336a9aa748d997d2cf4c5ae9a93cab6f96495fd6
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5784193"
---
# <a name="set-up-put-away-templates"></a><span data-ttu-id="dd9c7-103">Setja upp frágangssniðmát</span><span class="sxs-lookup"><span data-stu-id="dd9c7-103">Set Up Put-away Templates</span></span>

<span data-ttu-id="dd9c7-104">Ef notaður er beinn frágangur og tínsla er stungið upp á því hólfi sem best hentar vörunum á hverjum tíma samkvæmt frágangssniðmátinu sem sett hefur verið upp fyrir vöruhúsið, hólfaflokkuninni sem hólfin hafa fengið, og hámarks- og lágmarksmagninu sem sett hefur verið upp fyrir föst hólf.</span><span class="sxs-lookup"><span data-stu-id="dd9c7-104">With directed put-away and pick functionality, the most appropriate bin for your items at any given time is suggested, according to the put-away template that you have set up for the warehouse, the bin rankings you have given to the bins, and the minimum and maximum quantities that you have set up for fixed bins.</span></span>  

<span data-ttu-id="dd9c7-105">Hægt er að setja upp fleiri en eitt frágangssniðmát og velja eitt þeirra fyrir almenna stjórnun á frágangi í vöruhúsinu.</span><span class="sxs-lookup"><span data-stu-id="dd9c7-105">You can set up a number of put-away templates and select one of them to govern put-aways in general in your warehouse.</span></span> <span data-ttu-id="dd9c7-106">Einnig er hægt að velja frágangssniðmát fyrir hverja þá vöru eða birgðahaldseiningu sem hefur sérstakar kröfur um frágang.</span><span class="sxs-lookup"><span data-stu-id="dd9c7-106">You can also select a put-away template for any item or stockkeeping unit that might have special put-away requirements.</span></span>  

## <a name="to-set-up-put-away-templates"></a><span data-ttu-id="dd9c7-107">Frágangssniðmát sett upp</span><span class="sxs-lookup"><span data-stu-id="dd9c7-107">To set up put-away templates</span></span>

1. <span data-ttu-id="dd9c7-108">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Frágangssniðmát** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="dd9c7-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Put-away Templates**, and then choose the related link.</span></span>  
2. <span data-ttu-id="dd9c7-109">Valið er **Nýtt** aðgerð.</span><span class="sxs-lookup"><span data-stu-id="dd9c7-109">Choose the **New** action.</span></span>  
3. <span data-ttu-id="dd9c7-110">Færður er inn kóti sem er einkvæmt kenni sniðmátsins sem á að stofna.</span><span class="sxs-lookup"><span data-stu-id="dd9c7-110">Enter a code that is the unique identifier of the template you are about to create.</span></span>  
4. <span data-ttu-id="dd9c7-111">Stutt lýsing er færð inn ef vill.</span><span class="sxs-lookup"><span data-stu-id="dd9c7-111">Enter a short description, if you wish.</span></span>  
5. <span data-ttu-id="dd9c7-112">Fyrsta línan er fyllt út með hólfaþörfunum sem á fyrst og fremst að uppfylla þegar tillaga er gerð um frágang.</span><span class="sxs-lookup"><span data-stu-id="dd9c7-112">Fill in the first line with the bin requirements that you want fulfilled first and foremost when suggesting a put-away.</span></span>

    <span data-ttu-id="dd9c7-113">Ef e.d. er óskað eftir sjálfgefinni frágangsaðferð sem á að byggja á föstum hólfum skal velja svæðið **Finna fast hólf**.</span><span class="sxs-lookup"><span data-stu-id="dd9c7-113">For example, if want the default put-away method to be based on fixed bins, then choose the **Find Fixed Bin** field.</span></span> [!INCLUDE[tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]  
6. <span data-ttu-id="dd9c7-114">Önnur línan er fyllt út með hólfaþörfunum sem ættu að vera annar kostur til að uppfylla þegar hólf er fundið fyrir frágang.</span><span class="sxs-lookup"><span data-stu-id="dd9c7-114">Fill in the second line with the bin requirements that would be your second choice to fulfill in finding a bin for put-away.</span></span> <span data-ttu-id="dd9c7-115">Seinni línan er aðeins notuð ef hólf sem uppfyllir skilyrðin í fyrstu línunni finnst ekki.</span><span class="sxs-lookup"><span data-stu-id="dd9c7-115">The second line is used only if a bin that meets the requirements of the first line cannot be found.</span></span>  
7. <span data-ttu-id="dd9c7-116">Haldið er áfram að fylla út línur þar til lýst hefur verið öllum viðunandi hólfastaðsetningum á að nota í frágangi.</span><span class="sxs-lookup"><span data-stu-id="dd9c7-116">Continue to fill in the lines until you have described all the acceptable bin placements that you want to use in the put-away process.</span></span>  
8. <span data-ttu-id="dd9c7-117">Í síðustu línunni í frágangssniðmátinu skal velja gátreitinn **Finna fljótandi hólf**.</span><span class="sxs-lookup"><span data-stu-id="dd9c7-117">On the last line in the put-away template, select the **Find Floating Bin** check box.</span></span>  

<span data-ttu-id="dd9c7-118">Hægt er að stofna mismunandi frágangssniðmát og nota þau eftir hentugleikum.</span><span class="sxs-lookup"><span data-stu-id="dd9c7-118">You can create various put-away templates and then apply them as you see fit.</span></span> <span data-ttu-id="dd9c7-119">Fyrst er notast við frágangssniðmátið sem valið hefur verið fyrir vöruna eða birgðahaldseininguna.</span><span class="sxs-lookup"><span data-stu-id="dd9c7-119">The put-away template that you selected for the item or stockkeeping unit, if any is used first.</span></span> <span data-ttu-id="dd9c7-120">Ef þeir reitir eru ekki fylltir út, er frágangssniðmátið sem valið er fyrir vöruhúsið á flýtiflipanum **Hólfareglur** á birgðageymsluspjaldinu notað.</span><span class="sxs-lookup"><span data-stu-id="dd9c7-120">If these fields are not filled in, then the put-away template that you selected for the warehouse on the **Bin Policies** FastTab on the location card is used.</span></span>  

## <a name="see-also"></a><span data-ttu-id="dd9c7-121">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="dd9c7-121">See Also</span></span>

[<span data-ttu-id="dd9c7-122">Vöruhúsastjórnun</span><span class="sxs-lookup"><span data-stu-id="dd9c7-122">Warehouse Management</span></span>](warehouse-manage-warehouse.md)  
[<span data-ttu-id="dd9c7-123">Birgðir</span><span class="sxs-lookup"><span data-stu-id="dd9c7-123">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="dd9c7-124">Vöruhúsastjórnun sett upp</span><span class="sxs-lookup"><span data-stu-id="dd9c7-124">Setting Up Warehouse Management</span></span>](warehouse-setup-warehouse.md)  
[<span data-ttu-id="dd9c7-125">Samsetningardeild</span><span class="sxs-lookup"><span data-stu-id="dd9c7-125">Assembly Management</span></span>](assembly-assemble-items.md)  
[<span data-ttu-id="dd9c7-126">Hönnunarupplýsingar vöruhúsakerfi</span><span class="sxs-lookup"><span data-stu-id="dd9c7-126">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="dd9c7-127">[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="dd9c7-127">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  


[!INCLUDE[footer-include](includes/footer-banner.md)]