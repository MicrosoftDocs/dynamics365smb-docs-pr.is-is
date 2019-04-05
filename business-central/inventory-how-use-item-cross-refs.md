---
title: Nota millivísanir vöru | Microsoft Docs
description: Ef sett er upp millivísun milli vörulýsingar sem er notuð fyrir vöru og lýsingu sem lánardrottinn þessarar vöru notar, þá er vörulýsing lánardrottins sjálfkrafa færð inn fyrir innkaupaskjöl lánardrottins þegar **Millivísunarnr.** er fyllt út. .
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 03/12/2019
ms.author: sgroespe
ms.openlocfilehash: 09fb7c17e2fccbd3b2ad3195cffa37493ad40f61
ms.sourcegitcommit: d09f5ee0e164c7716f4ccb2ed71e2f9732a1f4f9
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/19/2019
ms.locfileid: "852264"
---
# <a name="use-item-cross-references"></a><span data-ttu-id="6aa7c-104">Nota millivísanir vöru</span><span class="sxs-lookup"><span data-stu-id="6aa7c-104">Use Item Cross References</span></span>
<span data-ttu-id="6aa7c-105">Ef sett er upp millivísun milli vörulýsingar sem er notuð fyrir vöru og lýsingu sem lánardrottinn þessarar vöru notar, þá er vörulýsing lánardrottins sjálfkrafa færð inn fyrir innkaupaskjöl lánardrottins þegar **Millivísunarnr.** er fyllt út.</span><span class="sxs-lookup"><span data-stu-id="6aa7c-105">If you set up a cross reference between the item description that you use for an item and the description that the vendor of that item uses, then the vendor's item description is automatically inserted on purchase documents for the vendor when you fill in the **Cross-Reference No.**</span></span> <span data-ttu-id="6aa7c-106">.</span><span class="sxs-lookup"><span data-stu-id="6aa7c-106">field.</span></span> <span data-ttu-id="6aa7c-107">Sama virknin gildir um númer viðskiptavina í söluskjölum.</span><span class="sxs-lookup"><span data-stu-id="6aa7c-107">The same functionality applies for customer item numbers on sales documents.</span></span>

<span data-ttu-id="6aa7c-108">Eftirfarandi ferli sýna hvernig á að nota millivísanir vöru innkaupamegin.</span><span class="sxs-lookup"><span data-stu-id="6aa7c-108">The following procedures describe how to use item cross references on the purchase side.</span></span> <span data-ttu-id="6aa7c-109">Skrefin eru svipuð sölumegin.</span><span class="sxs-lookup"><span data-stu-id="6aa7c-109">The steps are similar for the sales side.</span></span>

## <a name="to-set-up-an-item-cross-reference-to-a-vendors-item-description"></a><span data-ttu-id="6aa7c-110">Að setja upp millivísun vöru í vörulýsingu lánardrottins</span><span class="sxs-lookup"><span data-stu-id="6aa7c-110">To set up an item cross reference to a vendor's item description</span></span>
1. <span data-ttu-id="6aa7c-111">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Vörur** og veldu síðan tengda hlekkinn.</span><span class="sxs-lookup"><span data-stu-id="6aa7c-111">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>
2. <span data-ttu-id="6aa7c-112">Opnaðu spjaldið fyrir vöru þar sem á að búa til millivísun á vörulýsingu sem lánardrottinn notar fyrir þessa vöru.</span><span class="sxs-lookup"><span data-stu-id="6aa7c-112">Open the card for an item for which you want to create a cross reference to the item description that the vendor uses for that item.</span></span>
3. <span data-ttu-id="6aa7c-113">Veldu aðgerðina **Millivísanir**.</span><span class="sxs-lookup"><span data-stu-id="6aa7c-113">Choose the **Cross References** action.</span></span>
4. <span data-ttu-id="6aa7c-114">Í nýrri línu á síðunni **Færslur fyrir millivísun vöru** skal fylla í reitina eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="6aa7c-114">On a new line on the **Item Cross-Reference Entries** page, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]<span data-ttu-id="6aa7c-115">.</span><span class="sxs-lookup"><span data-stu-id="6aa7c-115">.</span></span>

## <a name="to-enter-a-vendors-item-description-on-a-purchase-order"></a><span data-ttu-id="6aa7c-116">Að færa vörulýsingu lánardrottins inn á innkaupapöntun</span><span class="sxs-lookup"><span data-stu-id="6aa7c-116">To enter a vendor's item description on a purchase order</span></span>
1. <span data-ttu-id="6aa7c-117">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Innkaupapantanir** og veldu síðan tengda hlekkinn.</span><span class="sxs-lookup"><span data-stu-id="6aa7c-117">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Purchase Orders**, and then choose the related link.</span></span>
2. <span data-ttu-id="6aa7c-118">Stofnaðu innkaupapöntun fyrir lánardrottin sem þú setur upp millivísun vöru fyrir í ferlinu hér á undan.</span><span class="sxs-lookup"><span data-stu-id="6aa7c-118">Create a purchase order for the vendor that you set up an item cross reference for in the previous procedure.</span></span>
3. <span data-ttu-id="6aa7c-119">Stofnaðu innkaupalínu fyrir vöruna sem þú setur upp millivísun vöru fyrir í ferlinu hér á undan.</span><span class="sxs-lookup"><span data-stu-id="6aa7c-119">Create a purchase line for the item that you set up an item cross reference for in the previous procedure.</span></span>
4. <span data-ttu-id="6aa7c-120">Í **Millivísunarnr.**</span><span class="sxs-lookup"><span data-stu-id="6aa7c-120">In the **Cross-Reference No.**</span></span> <span data-ttu-id="6aa7c-121">reitnum skal velja millivísun vörunnar sem þú stofnaðir og velja síðan hnappinn **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="6aa7c-121">field, select the item cross reference that you have created, and then choose the **OK** button.</span></span>

<span data-ttu-id="6aa7c-122">Skrifað er yfir reitinn **Lýsing** í línunni með vörulýsingu lánardrottins eins og er uppsett í færslu fyrir millivísun vörunnar.</span><span class="sxs-lookup"><span data-stu-id="6aa7c-122">The **Description** field on the line is overwritten with the vendor's item description, as set up on the item cross-reference entry.</span></span>

## <a name="see-also"></a><span data-ttu-id="6aa7c-123">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="6aa7c-123">See Also</span></span>
[<span data-ttu-id="6aa7c-124">Skrá nýjar vörur</span><span class="sxs-lookup"><span data-stu-id="6aa7c-124">Register New Items</span></span>](inventory-how-register-new-items.md)  
[<span data-ttu-id="6aa7c-125">Birgðir</span><span class="sxs-lookup"><span data-stu-id="6aa7c-125">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="6aa7c-126">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="6aa7c-126">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
