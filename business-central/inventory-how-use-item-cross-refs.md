---
title: Nota millivísanir vöru
description: Setjið upp tilvísanir á milli lýsinganna sem þú og lánardrottinn notið fyrir vöru þannig að hægt sé að setja inn vörulýsingu lánardrottins í innkaupaskjölum.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: item reference, cross reference, inventory
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 0a9f84522598344435ad9c1263fe8cdea2e2a1e0
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5785649"
---
# <a name="use-item-cross-references"></a><span data-ttu-id="44cfc-103">Nota millivísanir vöru</span><span class="sxs-lookup"><span data-stu-id="44cfc-103">Use Item Cross References</span></span>
<span data-ttu-id="44cfc-104">Ef sett er upp millivísun milli vörulýsingar sem er notuð fyrir vöru og lýsingu sem lánardrottinn þessarar vöru notar, þá er vörulýsing lánardrottins sjálfkrafa færð inn fyrir innkaupaskjöl lánardrottins þegar **Millivísunarnr.** er fyllt út.</span><span class="sxs-lookup"><span data-stu-id="44cfc-104">If you set up a cross reference between the item description that you use for an item and the description that the vendor of that item uses, then the vendor's item description is automatically inserted on purchase documents for the vendor when you fill in the **Cross-Reference No.**</span></span> <span data-ttu-id="44cfc-105">.</span><span class="sxs-lookup"><span data-stu-id="44cfc-105">field.</span></span> <span data-ttu-id="44cfc-106">Sama virknin gildir um númer viðskiptavina í söluskjölum.</span><span class="sxs-lookup"><span data-stu-id="44cfc-106">The same functionality applies for customer item numbers on sales documents.</span></span>

<span data-ttu-id="44cfc-107">Eftirfarandi ferli sýna hvernig á að nota millivísanir vöru innkaupamegin.</span><span class="sxs-lookup"><span data-stu-id="44cfc-107">The following procedures describe how to use item cross references on the purchase side.</span></span> <span data-ttu-id="44cfc-108">Skrefin eru svipuð sölumegin.</span><span class="sxs-lookup"><span data-stu-id="44cfc-108">The steps are similar for the sales side.</span></span>

> [!NOTE]
> <span data-ttu-id="44cfc-109">Það er að verða algengara að vörukenni á borð við GTIN eða GUID innihaldi 30 eða fleiri stafi, sem er meira en núverandi eiginleiki fyrir millivísanir á vörum getur ráðið við.</span><span class="sxs-lookup"><span data-stu-id="44cfc-109">It's becoming more common for item identifiers such as GTINs or GUIDs to contain 30 or more characters, which is more than the current feature for item cross references can handle.</span></span> <span data-ttu-id="44cfc-110">Ef nauðsynlegt er að nota tilvísanir sem innihalda fleiri en 30 stafi getur stjórnandinn kveikt á eiginleikanum **Skrifa lengri vörutilvísun** á síðunni [Eiginleikastjórnun](https://businesscentral.dynamics.com/?page=2610) (tengillinn krefst þess að þú sért með [!INCLUDE[prod_short](includes/prod_short.md)]-leigjanda).</span><span class="sxs-lookup"><span data-stu-id="44cfc-110">If you need to use references that contain more than 30 characters, your administrator can turn on the **Write longer item references** feature on the [Feature Management](https://businesscentral.dynamics.com/?page=2610) page (link requires that you have a [!INCLUDE[prod_short](includes/prod_short.md)] tenant).</span></span> <span data-ttu-id="44cfc-111">Hvernig tilvísanir eru notaðar breytist ekki en heiti hluta eins og síður og hnappar gera það.</span><span class="sxs-lookup"><span data-stu-id="44cfc-111">How you use references doesn't change, but the names of things like pages and buttons will.</span></span> <span data-ttu-id="44cfc-112">Til dæmis verður síðan **Millitilvísanafærslur vöru** að síðunni **Vörutilvísanafærslur**.</span><span class="sxs-lookup"><span data-stu-id="44cfc-112">For example, the **Item Cross-Reference Entries** page will become the **Item Reference Entries** page.</span></span>

## <a name="to-set-up-an-item-cross-reference-to-a-vendors-item-description"></a><span data-ttu-id="44cfc-113">Að setja upp millivísun vöru í vörulýsingu lánardrottins</span><span class="sxs-lookup"><span data-stu-id="44cfc-113">To set up an item cross reference to a vendor's item description</span></span>

1. <span data-ttu-id="44cfc-114">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Vara** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="44cfc-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>
2. <span data-ttu-id="44cfc-115">Opnaðu spjaldið fyrir vöru þar sem á að búa til millivísun á vörulýsingu sem lánardrottinn notar fyrir þessa vöru.</span><span class="sxs-lookup"><span data-stu-id="44cfc-115">Open the card for an item for which you want to create a cross reference to the item description that the vendor uses for that item.</span></span>
3. <span data-ttu-id="44cfc-116">Veldu aðgerðina **Millivísanir**.</span><span class="sxs-lookup"><span data-stu-id="44cfc-116">Choose the **Cross References** action.</span></span>

     <span data-ttu-id="44cfc-117">Ef ekki er hægt að finna aðgerðina **Millivísanir** skal velja til að skoða fleiri valkosti og finna hana síðan undir **Tengd** > **Vara**.</span><span class="sxs-lookup"><span data-stu-id="44cfc-117">If you cannot find the **Cross References** action, choose to view more options, and then find it under **Related** > **Item**.</span></span>
  
4. <span data-ttu-id="44cfc-118">Í nýrri línu á síðunni **Færslur fyrir millivísun vöru** skal fylla í reitina eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="44cfc-118">On a new line on the **Item Cross-Reference Entries** page, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]<span data-ttu-id="44cfc-119">.</span><span class="sxs-lookup"><span data-stu-id="44cfc-119">.</span></span>

## <a name="to-enter-a-vendors-item-description-on-a-purchase-order"></a><span data-ttu-id="44cfc-120">Að færa vörulýsingu lánardrottins inn á innkaupapöntun</span><span class="sxs-lookup"><span data-stu-id="44cfc-120">To enter a vendor's item description on a purchase order</span></span>

1. <span data-ttu-id="44cfc-121">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Innkaupapantanir** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="44cfc-121">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Purchase Orders**, and then choose the related link.</span></span>
2. <span data-ttu-id="44cfc-122">Stofnaðu innkaupapöntun fyrir lánardrottin sem þú setur upp millivísun vöru fyrir í ferlinu hér á undan.</span><span class="sxs-lookup"><span data-stu-id="44cfc-122">Create a purchase order for the vendor that you set up an item cross reference for in the previous procedure.</span></span>
3. <span data-ttu-id="44cfc-123">Stofnaðu innkaupalínu fyrir vöruna sem þú setur upp millivísun vöru fyrir í ferlinu hér á undan.</span><span class="sxs-lookup"><span data-stu-id="44cfc-123">Create a purchase line for the item that you set up an item cross reference for in the previous procedure.</span></span>
4. <span data-ttu-id="44cfc-124">Í **Millivísunarnr.**</span><span class="sxs-lookup"><span data-stu-id="44cfc-124">In the **Cross-Reference No.**</span></span> <span data-ttu-id="44cfc-125">reitnum skal velja millivísun vörunnar sem þú stofnaðir og velja síðan hnappinn **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="44cfc-125">field, select the item cross reference that you have created, and then choose the **OK** button.</span></span>

<span data-ttu-id="44cfc-126">Skrifað er yfir reitinn **Lýsing** í línunni með vörulýsingu lánardrottins eins og er uppsett í færslu fyrir millivísun vörunnar.</span><span class="sxs-lookup"><span data-stu-id="44cfc-126">The **Description** field on the line is overwritten with the vendor's item description, as set up on the item cross-reference entry.</span></span>

## <a name="see-also"></a><span data-ttu-id="44cfc-127">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="44cfc-127">See Also</span></span>
[<span data-ttu-id="44cfc-128">Skrá nýjar vörur</span><span class="sxs-lookup"><span data-stu-id="44cfc-128">Register New Items</span></span>](inventory-how-register-new-items.md)  
[<span data-ttu-id="44cfc-129">Birgðir</span><span class="sxs-lookup"><span data-stu-id="44cfc-129">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="44cfc-130">[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="44cfc-130">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]