---
title: Skipuleggja hluti í flokkum| Microsoft Docs
description: Til að fá hjálp við að leita að og finna vörur, er hægt að úthluta eiginleikum vöru og skipuleggja vörur í flokkum.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: category, search, attribute, facet
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: a5698746fe52ff7ff6ca38e1207f09ded0742c96
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/01/2020
ms.locfileid: "3914105"
---
# <a name="categorize-items"></a><span data-ttu-id="16f6a-103">Flokka vörur</span><span class="sxs-lookup"><span data-stu-id="16f6a-103">Categorize Items</span></span>

<span data-ttu-id="16f6a-104">Til að hafa yfirlit yfir vörur og til að hjálpa til við röðun og leit í vörum er gagnlegt að skipuleggja vörur í vöruflokka.</span><span class="sxs-lookup"><span data-stu-id="16f6a-104">To maintain an overview of your items and to help you sort and find items, it is useful to organize your items in item categories.</span></span>

<span data-ttu-id="16f6a-105">Til að finna vörur eftir eiginleika er hægt að úthluta vörueigindum á vörur og einnig vöruflokka.</span><span class="sxs-lookup"><span data-stu-id="16f6a-105">To find items by characteristics, you can assign item attributes to items and also to item categories.</span></span> <span data-ttu-id="16f6a-106">Frekari upplýsingar eru í [Vinna með vörueigindir](inventory-how-work-item-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="16f6a-106">For more information, see [Work with Item Attributes](inventory-how-work-item-attributes.md).</span></span>
<br><br>  

> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4j4mo?rel=0]

## <a name="to-create-an-item-category"></a><span data-ttu-id="16f6a-107">Að búa til vöruflokka</span><span class="sxs-lookup"><span data-stu-id="16f6a-107">To create an item category</span></span>
1. <span data-ttu-id="16f6a-108">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Vöruflokkar** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="16f6a-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Item Categories** , and then choose the related link.</span></span>
2. <span data-ttu-id="16f6a-109">Á síðunni **vöruflokkar** skal velja aðgerðina **Nýtt** .</span><span class="sxs-lookup"><span data-stu-id="16f6a-109">On the **Item Categories** page, choose the **New** action.</span></span>
3. <span data-ttu-id="16f6a-110">Á síðunni **vöruflokkaspjald** , á flipanum **Almennt** , eru eftirfarandi reitir fylltir út.</span><span class="sxs-lookup"><span data-stu-id="16f6a-110">On the **Item Category Card** page, on the **General** FastTab, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. <span data-ttu-id="16f6a-111">Í **eigindir** Flýtiflipanum skal tilgreina hvers kyns vörueigindum fyrir vöruflokk.</span><span class="sxs-lookup"><span data-stu-id="16f6a-111">On the **Attributes** FastTab, specify any item attributes for the item category.</span></span> <span data-ttu-id="16f6a-112">Frekari upplýsingar er að finna í [Að úthluta vörueigindum á vöruflokka](inventory-how-work-item-attributes.md#to-assign-item-attributes-to-item-categories).</span><span class="sxs-lookup"><span data-stu-id="16f6a-112">For more information, see [To assign item attributes to item categories](inventory-how-work-item-attributes.md#to-assign-item-attributes-to-item-categories).</span></span>

> [!NOTE]  
> <span data-ttu-id="16f6a-113">Hafi vöruflokkur yfirvöruflokk eins og gefið er til kynna með reitnum **yfirtegund** þá eru allar vörueigindir sem eru úthlutaðar á þann yfirflokk vöru forútfylltar á flýtiflipanum **eigindir** .</span><span class="sxs-lookup"><span data-stu-id="16f6a-113">If the item category has a parent item category, as indicated by the **Parent Category** field, then any item attributes that are assigned to that parent item category are prefilled on the **Attributes** FastTab.</span></span>

> [!NOTE]  
> <span data-ttu-id="16f6a-114">Vörueigindir sem á að úthluta á vöruflokk mun sjálfkrafa gilda um vöruna sem vöruflokknum er úthlutað á.</span><span class="sxs-lookup"><span data-stu-id="16f6a-114">Item attributes that you assign to an item category will automatically apply to the item that the item category is assigned to.</span></span>

<span data-ttu-id="16f6a-115">Ef þú skiptir um skoðun varðandi vöruflokk, getur þú eytt honum.</span><span class="sxs-lookup"><span data-stu-id="16f6a-115">If you change your mind about an item category, you can delete it.</span></span> <span data-ttu-id="16f6a-116">Ef honum hefur hinsvegar verið úthlutað á vöru þarf að fjarlægja þá úthlutun áður en vöruflokknum er eytt.</span><span class="sxs-lookup"><span data-stu-id="16f6a-116">However, if it has already been assigned to an item, you must remove that assignment before you can delete the item category.</span></span>

## <a name="to-assign-an-item-category-to-an-item"></a><span data-ttu-id="16f6a-117">Að úthluta vöruflokki á vöru.</span><span class="sxs-lookup"><span data-stu-id="16f6a-117">To assign an item category to an item</span></span>

1. <span data-ttu-id="16f6a-118">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Vara** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="16f6a-118">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items** , and then choose the related link.</span></span>
2. <span data-ttu-id="16f6a-119">Opna skal birgðaspjaldið fyrir vöruna sem á að úthluta á vöruflokk.</span><span class="sxs-lookup"><span data-stu-id="16f6a-119">Open the card for the item that you want to assign to an item category.</span></span>
3. <span data-ttu-id="16f6a-120">Veldu leitarhnappinn í reitnum **Vöruflokkskóði** og veldu fyrirliggjandi vöruflokk.</span><span class="sxs-lookup"><span data-stu-id="16f6a-120">Choose the lookup button in the **Item Category Code** field and select an existing item category.</span></span> <span data-ttu-id="16f6a-121">Einnig má velja á **Nýtt** aðgerð til að stofna fyrst nýjan vöruflokk eins og útskýrt er í [Stofna vöruflokk](inventory-how-categorize-items.md#to-create-an-item-category).</span><span class="sxs-lookup"><span data-stu-id="16f6a-121">Alternatively, choose the **New** action to first create a new item category as explained in [To create an item category](inventory-how-categorize-items.md#to-create-an-item-category).</span></span>

## <a name="categories-attributes-and-variants"></a><span data-ttu-id="16f6a-122">Flokkar, eigindir og afbrigði</span><span class="sxs-lookup"><span data-stu-id="16f6a-122">Categories, attributes, and variants</span></span>

[!INCLUDE[inventory_variant](includes/inventory_variant.md)]

## <a name="see-also"></a><span data-ttu-id="16f6a-123">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="16f6a-123">See Also</span></span>

[<span data-ttu-id="16f6a-124">Vinna með vörueigindir</span><span class="sxs-lookup"><span data-stu-id="16f6a-124">Work with Item Attributes</span></span>](inventory-how-work-item-attributes.md)  
[<span data-ttu-id="16f6a-125">Skrá nýjar vörur</span><span class="sxs-lookup"><span data-stu-id="16f6a-125">Register New Items</span></span>](inventory-how-register-new-items.md)  
[<span data-ttu-id="16f6a-126">Birgðir</span><span class="sxs-lookup"><span data-stu-id="16f6a-126">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="16f6a-127">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="16f6a-127">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
