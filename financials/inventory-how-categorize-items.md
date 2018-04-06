---
title: "Skipuleggja hluti í flokkum| Microsoft Docs"
description: "Til að fá hjálp við að leita að og finna vörur, er hægt að úthluta eiginleikum vöru og skipuleggja vörur í flokkum."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: category, search, attribute, facet
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 64511e0979671d13740bd18d95d53e8e37564583
ms.contentlocale: is-is
ms.lasthandoff: 03/22/2018

---
# <a name="categorize-items"></a><span data-ttu-id="af52e-103">Flokka vörur</span><span class="sxs-lookup"><span data-stu-id="af52e-103">Categorize Items</span></span>
<span data-ttu-id="af52e-104">Til að hafa yfirlit yfir vörur og til að hjálpa til við röðun og leit í vörum er gagnlegt að skipuleggja vörur í vöruflokka.</span><span class="sxs-lookup"><span data-stu-id="af52e-104">To maintain an overview of your items and to help you sort and find items, it is useful to organize your items in item categories.</span></span>

<span data-ttu-id="af52e-105">Til að finna vörur eftir eiginleika er hægt að úthluta vörueigindum á vörur og einnig vöruflokka.</span><span class="sxs-lookup"><span data-stu-id="af52e-105">To find items by characteristics, you can assign item attributes to items and also to item categories.</span></span> <span data-ttu-id="af52e-106">Frekari upplýsingar eru í [Vinna með vörueigindir](inventory-how-work-item-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="af52e-106">For more information, see [Work with Item Attributes](inventory-how-work-item-attributes.md).</span></span>

## <a name="to-create-an-item-category"></a><span data-ttu-id="af52e-107">Að búa til vöruflokka</span><span class="sxs-lookup"><span data-stu-id="af52e-107">To create an item category</span></span>
1. <span data-ttu-id="af52e-108">Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Vörurflokkar** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="af52e-108">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Item Categories**, and then choose the related link.</span></span>
2. <span data-ttu-id="af52e-109">Í glugganum **vöruflokkar** skal velja aðgerðina **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="af52e-109">In the **Item Categories** window, choose the **New** action.</span></span>
3. <span data-ttu-id="af52e-110">Í glugganum **vöruflokkaspjald**, á flipanum **Almennt**, eru eftirfarandi reitir fylltir út:</span><span class="sxs-lookup"><span data-stu-id="af52e-110">In the **Item Category Card** window, on the **General** FastTab, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. <span data-ttu-id="af52e-111">Í **eigindir** Flýtiflipanum skal tilgreina hvers kyns vörueigindum fyrir vöruflokk.</span><span class="sxs-lookup"><span data-stu-id="af52e-111">On the **Attributes** FastTab, specify any item attributes for the item category.</span></span> <span data-ttu-id="af52e-112">Nánari upplýsingar eru í „Að úthluta vörueigindum á vöruflokk hlutanum“ í [Vinna með vörueigindir](inventory-how-work-item-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="af52e-112">For more information, see the "To assign item attributes to an item category" section in [Work with Item Attributes](inventory-how-work-item-attributes.md).</span></span>

> [!NOTE]  
>   <span data-ttu-id="af52e-113">Hafi vöruflokkur yfirvöruflokk eins og gefið er til kynna með reitnum **yfirtegund** þá eru allar vörueigindir sem eru úthlutaðar á þann yfirflokk vöru forútfylltar á flýtiflipanum **eigindir**.</span><span class="sxs-lookup"><span data-stu-id="af52e-113">If the item category has a parent item category, as indicated by the **Parent Category** field, then any item attributes that are assigned to that parent item category are prefilled on the **Attributes** FastTab.</span></span>

> [!NOTE]  
>   <span data-ttu-id="af52e-114">Vörueigindir sem á að úthluta á vöruflokk mun sjálfkrafa gilda um vöruna sem vöruflokknum er úthlutað á.</span><span class="sxs-lookup"><span data-stu-id="af52e-114">Item attributes that you assign to an item category will automatically apply to the item that the item category is assigned to.</span></span>

## <a name="to-assign-an-item-category-to-an-item"></a><span data-ttu-id="af52e-115">Að úthluta vöruflokki á vöru.</span><span class="sxs-lookup"><span data-stu-id="af52e-115">To assign an item category to an item</span></span>
1. <span data-ttu-id="af52e-116">Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Vörur** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="af52e-116">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Items**, and then choose the related link.</span></span>
2. <span data-ttu-id="af52e-117">Opna skal birgðaspjaldið fyrir vöruna sem á að úthluta á vöruflokk.</span><span class="sxs-lookup"><span data-stu-id="af52e-117">Open the card for the item that you want to assign to an item category.</span></span>
3. <span data-ttu-id="af52e-118">Veldu leitarhnappinn í reitnum **Vöruflokkskóði** og veldu fyrirliggjandi vöruflokk.</span><span class="sxs-lookup"><span data-stu-id="af52e-118">Choose the lookup button in the **Item Category Code** field and select an existing item category.</span></span> <span data-ttu-id="af52e-119">Einnig má velja á **Nýtt** aðgerð til að stofna fyrst nýjan vöruflokk eins og útskýrt er í "Stofna vöruflokk" hlutanum.</span><span class="sxs-lookup"><span data-stu-id="af52e-119">Alternatively, choose the **New** action to first create a new item category as explained in the "To create an item category" section.</span></span>

## <a name="see-also"></a><span data-ttu-id="af52e-120">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="af52e-120">See Also</span></span>
[<span data-ttu-id="af52e-121">Vinna með vörueigindir</span><span class="sxs-lookup"><span data-stu-id="af52e-121">Work with Item Attributes</span></span>](inventory-how-work-item-attributes.md)  
[<span data-ttu-id="af52e-122">Skrá nýjar vörur</span><span class="sxs-lookup"><span data-stu-id="af52e-122">Register New Items</span></span>](inventory-how-register-new-items.md)  
[<span data-ttu-id="af52e-123">Birgðir</span><span class="sxs-lookup"><span data-stu-id="af52e-123">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="af52e-124">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="af52e-124">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

