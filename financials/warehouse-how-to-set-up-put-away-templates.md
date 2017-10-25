---
title: "Hvernig á að setja upp Frágangssniðmát | Microsoft Docs"
description: "Ef notaður er beinn frágangur og tínsla er stungið upp á því hólfi sem best hentar vörunum á hverjum tíma samkvæmt frágangssniðmátinu sem sett hefur verið upp fyrir vöruhúsið, hólfaflokkuninni sem hólfin hafa fengið, og hámarks- og lágmarksmagninu sem sett hefur verið upp fyrir föst hólf."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/23/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 5a81b904a9180d7370a00f94a129ec707398e89a
ms.contentlocale: is-is
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-set-up-put-away-templates"></a><span data-ttu-id="1d755-103">Hvernig á að setja upp Frágangssniðmát</span><span class="sxs-lookup"><span data-stu-id="1d755-103">How to: Set Up Put-away Templates</span></span>
<span data-ttu-id="1d755-104">Ef notaður er beinn frágangur og tínsla er stungið upp á því hólfi sem best hentar vörunum á hverjum tíma samkvæmt frágangssniðmátinu sem sett hefur verið upp fyrir vöruhúsið, hólfaflokkuninni sem hólfin hafa fengið, og hámarks- og lágmarksmagninu sem sett hefur verið upp fyrir föst hólf.</span><span class="sxs-lookup"><span data-stu-id="1d755-104">With directed put-away and pick functionality, the most appropriate bin for your items at any given time is suggested, according to the put-away template that you have set up for the warehouse, the bin rankings you have given to the bins, and the minimum and maximum quantities that you have set up for fixed bins.</span></span>  

<span data-ttu-id="1d755-105">Hægt er að setja upp fleiri en eitt frágangssniðmát og velja eitt þeirra fyrir almenna stjórnun á frágangi í vöruhúsinu.</span><span class="sxs-lookup"><span data-stu-id="1d755-105">You can set up a number of put-away templates and select one of them to govern put-aways in general in your warehouse.</span></span> <span data-ttu-id="1d755-106">Einnig er hægt að velja frágangssniðmát fyrir hverja þá vöru eða birgðahaldseiningu sem hefur sérstakar kröfur um frágang.</span><span class="sxs-lookup"><span data-stu-id="1d755-106">You can also select a put-away template for any item or stockkeeping unit that might have special put-away requirements.</span></span>  

## <a name="to-set-up-put-away-templates"></a><span data-ttu-id="1d755-107">Frágangssniðmát sett upp</span><span class="sxs-lookup"><span data-stu-id="1d755-107">To set up put-away templates</span></span>  
1.  <span data-ttu-id="1d755-108">Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Frágangssniðmát** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="1d755-108">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Put-away Templates**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="1d755-109">Valið er **Nýtt** aðgerð.</span><span class="sxs-lookup"><span data-stu-id="1d755-109">Choose the **New** action.</span></span>  
3.  <span data-ttu-id="1d755-110">Færður er inn kóti sem er einkvæmt kenni sniðmátsins sem á að stofna.</span><span class="sxs-lookup"><span data-stu-id="1d755-110">Enter a code that is the unique identifier of the template you are about to create.</span></span>  
4.  <span data-ttu-id="1d755-111">Stutt lýsing er færð inn ef vill.</span><span class="sxs-lookup"><span data-stu-id="1d755-111">Enter a short description, if you wish.</span></span>  
5.  <span data-ttu-id="1d755-112">Fyrsta línan er fyllt út með hólfaþörfunum sem á fyrst og fremst að uppfylla þegar tillaga er gerð um frágang.</span><span class="sxs-lookup"><span data-stu-id="1d755-112">Fill in the first line with the bin requirements that you want fulfilled first and foremost when suggesting a put-away.</span></span>  
6.  <span data-ttu-id="1d755-113">Önnur línan er fyllt út með hólfaþörfunum sem ættu að vera annar kostur til að uppfylla þegar hólf er fundið fyrir frágang.</span><span class="sxs-lookup"><span data-stu-id="1d755-113">Fill in the second line with the bin requirements that would be your second choice to fulfill in finding a bin for put-away.</span></span> <span data-ttu-id="1d755-114">Seinni línan er aðeins notuð ef hólf sem uppfyllir skilyrðin í fyrstu línunni finnst ekki.</span><span class="sxs-lookup"><span data-stu-id="1d755-114">The second line is used only if a bin that meets the requirements of the first line cannot be found.</span></span>  
7.  <span data-ttu-id="1d755-115">Haldið er áfram að fylla út línur þar til lýst hefur verið öllum viðunandi hólfastaðsetningum á að nota í frágangi.</span><span class="sxs-lookup"><span data-stu-id="1d755-115">Continue to fill in the lines until you have described all the acceptable bin placements that you want to use in the put-away process.</span></span>  
8.  <span data-ttu-id="1d755-116">Í síðustu línunni í frágangssniðmátinu skal velja gátreitinn **Finna fljótandi hólf**.</span><span class="sxs-lookup"><span data-stu-id="1d755-116">On the last line in the put-away template, select the **Find Floating Bin** check box.</span></span>  

<span data-ttu-id="1d755-117">Hægt er að stofna mismunandi frágangssniðmát og nota þau eftir hentugleikum.</span><span class="sxs-lookup"><span data-stu-id="1d755-117">You can create various put-away templates and then apply them as you see fit.</span></span> <span data-ttu-id="1d755-118">Fyrst er notast við frágangssniðmátið sem valið hefur verið fyrir vöruna eða birgðahaldseininguna.</span><span class="sxs-lookup"><span data-stu-id="1d755-118">The put-away template that you selected for the item or stockkeeping unit, if any is used first.</span></span> <span data-ttu-id="1d755-119">Ef þeir reitir eru ekki fylltir út, er frágangssniðmátið sem valið er fyrir vöruhúsið á flýtiflipanum **Hólfareglur** á birgðageymsluspjaldinu notað.</span><span class="sxs-lookup"><span data-stu-id="1d755-119">If these fields are not filled in, then the put-away template that you selected for the warehouse on the **Bin Policies** FastTab on the location card is used.</span></span>  

## <a name="see-also"></a><span data-ttu-id="1d755-120">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="1d755-120">See Also</span></span>  
[<span data-ttu-id="1d755-121">Vöruhúsastjórnun</span><span class="sxs-lookup"><span data-stu-id="1d755-121">Warehouse Management</span></span>](warehouse-manage-warehouse.md)  
[<span data-ttu-id="1d755-122">Birgðir</span><span class="sxs-lookup"><span data-stu-id="1d755-122">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="1d755-123">[Vöruhúsastjórnun sett upp](warehouse-setup-warehouse.md)   </span><span class="sxs-lookup"><span data-stu-id="1d755-123">[Setting Up Warehouse Management](warehouse-setup-warehouse.md)   </span></span>  
<span data-ttu-id="1d755-124">[Samsetningardeild](assembly-assemble-items.md)  </span><span class="sxs-lookup"><span data-stu-id="1d755-124">[Assembly Management](assembly-assemble-items.md)  </span></span>  
[<span data-ttu-id="1d755-125">Hönnunarupplýsingar vöruhúsakerfi</span><span class="sxs-lookup"><span data-stu-id="1d755-125">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="1d755-126">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="1d755-126">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

