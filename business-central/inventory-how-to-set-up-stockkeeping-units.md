---
title: Hvernig á að setja upp birgðahaldseiningar | Microsoft Docs
description: Hægt er að nota birgðaeiningar til að skrá upplýsingar um vörur fyrir tiltekna birgðageymslu eða tiltekinn afbrigðiskóta.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 50bf3695a135652ec422bb187f1ff2fef06f3a35
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/29/2019
ms.locfileid: "1239384"
---
# <a name="set-up-stockkeeping-units"></a><span data-ttu-id="b92b0-103">Setja upp birgðahaldseiningar</span><span class="sxs-lookup"><span data-stu-id="b92b0-103">Set Up Stockkeeping Units</span></span>
<span data-ttu-id="b92b0-104">Hægt er að nota birgðaeiningar til að skrá upplýsingar um vörur fyrir tiltekna birgðageymslu eða tiltekinn afbrigðiskóta.</span><span class="sxs-lookup"><span data-stu-id="b92b0-104">You can use stockkeeping units to record information about your items for a specific location or a specific variant code.</span></span>  

 <span data-ttu-id="b92b0-105">Birgðahaldseiningar eru viðbót við birgðaspjöldin.</span><span class="sxs-lookup"><span data-stu-id="b92b0-105">Stockkeeping units are a supplement to item cards.</span></span> <span data-ttu-id="b92b0-106">Þær koma ekki í staðinn fyrir þau þótt tengsl séu á milli þeirra.</span><span class="sxs-lookup"><span data-stu-id="b92b0-106">They do not replace them, although they are related to them.</span></span> <span data-ttu-id="b92b0-107">Með notkun birgðaeininga er hægt að aðgreina upplýsingar um vöru fyrir tilteknar birgðageymslur (svo sem vöruhús eða dreifingarmiðstöð) eða tiltekin afbrigði (svo sem mismunandi hillunúmer og mismunandi áfyllingarupplýsingar) fyrir sömu vöruna.</span><span class="sxs-lookup"><span data-stu-id="b92b0-107">Stockkeeping units allow you to differentiate information about an item for a specific location, such as a warehouse or distribution center, or a specific variant, such as different shelf numbers and different replenishment information, for the same item.</span></span>  

## <a name="to-set-up-a-stockkeeping-unit"></a><span data-ttu-id="b92b0-108">Uppsetning birgðaeininga</span><span class="sxs-lookup"><span data-stu-id="b92b0-108">To set up a stockkeeping unit</span></span>  

1.  <span data-ttu-id="b92b0-109">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Birgðahaldseiningar** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="b92b0-109">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Stockkeeping Units**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="b92b0-110">Valið er **Nýtt** aðgerð.</span><span class="sxs-lookup"><span data-stu-id="b92b0-110">Choose the **New** action.</span></span>  
3.  <span data-ttu-id="b92b0-111">Fært er í reitina á spjaldinu.</span><span class="sxs-lookup"><span data-stu-id="b92b0-111">Fill in the fields on the card.</span></span> <span data-ttu-id="b92b0-112">Eftirfarandi reita er krafist: **Vörunr.**, **Kóti birgðageymslu**, og/ eða **Afbrigðiskóti**.</span><span class="sxs-lookup"><span data-stu-id="b92b0-112">The following fields are required: **Item No.**, **Location Code**, and/or **Variant Code**.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

<span data-ttu-id="b92b0-113">Þegar búið að setja upp fyrstu birgðaeininguna fyrir vöru er **Birgðahaldseiningin er til** gátreitur á **Vara** spjaldinu valið.</span><span class="sxs-lookup"><span data-stu-id="b92b0-113">When you have set up the first stockkeeping unit for an item, the **Stockkeeping Unit Exists** check box on the **Item** card is selected.</span></span>  

<span data-ttu-id="b92b0-114">Ef búa á til nokkrar birgðaeiningar fyrir vöru er keyrslan **Stofna birgðahaldseiningu** notuð.</span><span class="sxs-lookup"><span data-stu-id="b92b0-114">To create several stockkeeping units for an item, use the **Create Stockkeeping Unit** batch job.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="b92b0-115">Upplýsingarnar á spjaldinu **Birgðaeining er til** hafa forgang á spjaldið **Vara**.</span><span class="sxs-lookup"><span data-stu-id="b92b0-115">The information on the **Stockkeeping Unit** card has priority over the **Item** card.</span></span>

> [!Warning]
> <span data-ttu-id="b92b0-116">Ef birgðahaldseiningin er afhent með framleiðslu er reiturinn **Staðlaður kostnaður** ekki notaður við reikningagerð og leiðréttingu á raunkostnað framleiddrar vöru.</span><span class="sxs-lookup"><span data-stu-id="b92b0-116">If the SKU is supplied through production, then the **Standard Cost** field is not used when invoicing and adjusting the actual cost of the produced item.</span></span> <span data-ttu-id="b92b0-117">Þess í stað er reiturinn **Staðlaður kostnaður** á undirliggjandi birgðaspjaldinu notaður og öll frávik eru reiknuð út á móti kostnaðarhlut þeirrar vöru.</span><span class="sxs-lookup"><span data-stu-id="b92b0-117">Instead, the **Standard Cost** field on the underlying item card is used, and any variances are calculated against the cost shares of that item.</span></span><br /><br />
> <span data-ttu-id="b92b0-118">Þar sem ekki er hægt að úthluta framleiðsluuppskriftum og leið til birgðahaldseininga, eru samanlagt kostnaðarverð og tengdur útreikningur á kostnaðarhlutum einnig ekki tiltæk á birgðahaldseiningar.</span><span class="sxs-lookup"><span data-stu-id="b92b0-118">Because production BOMs and routing cannot be assigned to SKUs, then the unit cost roll-up and the related calculation of cost shares are also not available on SKUs.</span></span> <span data-ttu-id="b92b0-119">Í [Um útreikning staðlaðs kostnaðar](finance-about-calculating-standard-cost.md) er fjallað nánar um þetta efni</span><span class="sxs-lookup"><span data-stu-id="b92b0-119">For more information, see [About Calculating Standard Cost](finance-about-calculating-standard-cost.md)</span></span>

## <a name="see-also"></a><span data-ttu-id="b92b0-120">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="b92b0-120">See Also</span></span>  
[<span data-ttu-id="b92b0-121">Skrá nýjar vörur</span><span class="sxs-lookup"><span data-stu-id="b92b0-121">Register New Items</span></span>](inventory-how-register-new-items.md)  
[<span data-ttu-id="b92b0-122">Vöruhúsastjórnun sett upp</span><span class="sxs-lookup"><span data-stu-id="b92b0-122">Setting Up Warehouse Management</span></span>](warehouse-setup-warehouse.md)  
[<span data-ttu-id="b92b0-123">Vöruhúsastjórnun</span><span class="sxs-lookup"><span data-stu-id="b92b0-123">Warehouse Management</span></span>](warehouse-manage-warehouse.md)  
[<span data-ttu-id="b92b0-124">Birgðir</span><span class="sxs-lookup"><span data-stu-id="b92b0-124">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="b92b0-125">[Samsetningardeild](assembly-assemble-items.md)  </span><span class="sxs-lookup"><span data-stu-id="b92b0-125">[Assembly Management](assembly-assemble-items.md)  </span></span>  
[<span data-ttu-id="b92b0-126">Hönnunarupplýsingar vöruhúsakerfi</span><span class="sxs-lookup"><span data-stu-id="b92b0-126">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="b92b0-127">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="b92b0-127">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
