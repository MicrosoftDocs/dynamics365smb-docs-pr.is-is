---
title: Hvernig á að færa vörur með ítarlegum vöruhúsaaðgerðum | Microsoft Docs
description: Í ítarlegri vöruhúsagrunnstillingu, þ.e. birgðageymslum sem nota beinan frágang og tínslu, sér reyndur starfsmaður um hreyfingar milli hólfa og útbýr hreyfingar í hreyfingavinnublaðinu og stofnar síðan hreyfingar sem starfsmenn vöruhússins framkvæma.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: e843b048c117539d077dc4a8ecba33f265a2e826
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5782635"
---
# <a name="move-items-in-advanced-warehouse-configurations"></a><span data-ttu-id="cf7c9-103">Færa vörur með ítarlegum vöruhúsaaðgerðum</span><span class="sxs-lookup"><span data-stu-id="cf7c9-103">Move Items in Advanced Warehouse Configurations</span></span>
<span data-ttu-id="cf7c9-104">Í ítarlegri vöruhúsagrunnstillingu, þ.e. birgðageymslum sem nota beinan frágang og tínslu, sér reyndur starfsmaður um hreyfingar milli hólfa og útbýr hreyfingar í hreyfingavinnublaðinu og stofnar síðan hreyfingar sem starfsmenn vöruhússins framkvæma.</span><span class="sxs-lookup"><span data-stu-id="cf7c9-104">In advanced warehouse configurations, that is, locations with directed put-away and pick, warehouse movements between bins are performed by a senior employee preparing warehouse movements in the movement worksheet and then creating the warehouse movements for warehouse employees to perform.</span></span>  

## <a name="to-move-items-with-the-warehouse-movement-worksheet"></a><span data-ttu-id="cf7c9-105">Til að færa vörur með vöruhúsahreyfingarvinnublaðinu</span><span class="sxs-lookup"><span data-stu-id="cf7c9-105">To move items with the warehouse movement worksheet</span></span>
<span data-ttu-id="cf7c9-106">Síðan **Vinnublað hreyfingar** hefur tvær aðgerðir sem hjálpa til við að fylla út línurnar sjálfvirkt.</span><span class="sxs-lookup"><span data-stu-id="cf7c9-106">The **Movement Worksheet** page has two functions that can assist in automatically filling in the lines.</span></span> <span data-ttu-id="cf7c9-107">Önnur er aðgerðin **Reikna út áfyllingu hólfs**.</span><span class="sxs-lookup"><span data-stu-id="cf7c9-107">The first is the **Calculate Bin Replenishment** function.</span></span> <span data-ttu-id="cf7c9-108">Aðgerðin notar hólfaflokkun til að leggja til áfyllingu hærra flokkaðra hólfa úr lægra flokkuðum. Hin er aðgerðin **Sækja innihald hólfs** sem fyllir út vinnublaðslínurnar með öllu innihaldi hólfsins eða hólfanna sem eru tilgreind.</span><span class="sxs-lookup"><span data-stu-id="cf7c9-108">This function uses the bin rankings to suggest replenishment for high-ranking bins from low-ranking bins. The second is the **Get Bin Content** function, which fills in the worksheet lines with the entire bin contents of the bin or bins you specify.</span></span>

1.  <span data-ttu-id="cf7c9-109">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Hreyfingavinnublað** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="cf7c9-109">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Movement Worksheet**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="cf7c9-110">Færið inn upplýsingar um vöruhúsahreyfingar í vinnublaðslínurnar eins og við á.</span><span class="sxs-lookup"><span data-stu-id="cf7c9-110">Enter the warehouse movement information on the worksheet lines as appropriate.</span></span>  
3. <span data-ttu-id="cf7c9-111">Veljið aðgerðina **Stofna hreyfingu** til að stofna vöruhúsahreyfingarskjal sem síðan er hægt að skrá þegar vöruhúsahreyfingunni er lokið.</span><span class="sxs-lookup"><span data-stu-id="cf7c9-111">Choose the **Create Movement** action to create a warehouse movement document which can then be registered when the warehouse movement is completed.</span></span>  

### <a name="to-register-the-warehouse-movement"></a><span data-ttu-id="cf7c9-112">Vöruhúsahreyfingin skráð</span><span class="sxs-lookup"><span data-stu-id="cf7c9-112">To register the warehouse movement</span></span>  
1.  <span data-ttu-id="cf7c9-113">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Hreyfingar** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="cf7c9-113">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Movements**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="cf7c9-114">Opnar vöruhúsahreyfingu sem á að vinna með.</span><span class="sxs-lookup"><span data-stu-id="cf7c9-114">Open the warehouse movement that you want to process.</span></span>  
3.  <span data-ttu-id="cf7c9-115">Á línum aðgerðartegundar **Staðsetja** skal tilgreina hvar, sem og, hvenær eigi að færa viðkomandi vöru með því að breyta svæðunum **Svæðiskóti**, **Hólfkóti**, **Magn til afgreiðslu**, eða **Gjalddagi**.</span><span class="sxs-lookup"><span data-stu-id="cf7c9-115">On lines of action type **Place**, specify where, which, and when to move the item in question by editing the **Zone Code**, **Bin Code**, **Qty. to Handle**, or **Due Date** fields.</span></span>  

    <span data-ttu-id="cf7c9-116">Hafi vöruhúsið verið sett þannig upp að hólfakótarnir fylgi eiginlegu skipulagi vöruhússins er hægt að taka ákveðnar vörur úr samfelldum magnhólfum og setja þær síðan í framtíðartínsluhólf sem gætu verið nálægt hvert öðru.</span><span class="sxs-lookup"><span data-stu-id="cf7c9-116">If your warehouse has been set up so the bin codes follow the physical structure of the warehouse, you can take quantities of several items from successive bulk bins and then place them in forward picking bins, which also might be close to one another.</span></span>  
4.  <span data-ttu-id="cf7c9-117">Í línum aðgerðegundir **Taka**, tilgreinið í reitnum **Magn til afgreiðslu** íhlutamagn innihalds hólfs sem á að færa.</span><span class="sxs-lookup"><span data-stu-id="cf7c9-117">On lines of action type **Take**, specify in the **Qty. to Handle** field a part quantity of the bin content that you want to move.</span></span> <span data-ttu-id="cf7c9-118">Allir aðrir reitir á línum af aðgerðtegundinni **Taka** eru skrifvarðir.</span><span class="sxs-lookup"><span data-stu-id="cf7c9-118">All other fields on lines of action type **Take** are read-only.</span></span>  
5.  <span data-ttu-id="cf7c9-119">Til að færa allt ráðlagt magn eins og tilgreint er í reitnum **Magn** skal velja **Fylla sjálfvirkt inn magn til afgr.** aðgerðina.</span><span class="sxs-lookup"><span data-stu-id="cf7c9-119">To move all suggested quantities as specified in the **Quantity** field, choose the **Autofill Qty. to Handle** action.</span></span>  
6. <span data-ttu-id="cf7c9-120">Velja aðgerðina **Skrá**.</span><span class="sxs-lookup"><span data-stu-id="cf7c9-120">Choose the **Register** action.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="cf7c9-121">Þegar birgðageymslan notar beinan frágang og tínslu og hólfategundir þá er ekki hægt að færa vörur handvirkt inn og út úr hólfum því vörur sem eru í hólfi af þeirri gerð verður að skrá sem frágengnar áður en þær verða hluti af tiltækum birgðum.</span><span class="sxs-lookup"><span data-stu-id="cf7c9-121">If the location uses directed put-away and pick, then you cannot manually move items in or out of bins of bin type RECEIVE, because items in such bins must be registered as being put away before they are part of available inventory.</span></span>

## <a name="to-register-the-movement-of-an-item-that-has-already-occurred"></a><span data-ttu-id="cf7c9-122">Flutningur á vörum sem þegar hefur átt sér stað skráður</span><span class="sxs-lookup"><span data-stu-id="cf7c9-122">To register the movement of an item that has already occurred</span></span>  
<span data-ttu-id="cf7c9-123">Ef birgðageymslan notar beinan frágang og tínslu og það þarf að færa vörurnar í önnur hólf án þess að fyrir sé vöruhúsafrágangur, tínsla eða hreyfing er hægt að skrá rétta staðinn fyrir vörurnar í vöruhúsinu með því að nota **vöruhússendurflokkunarbók**.</span><span class="sxs-lookup"><span data-stu-id="cf7c9-123">If your location uses directed put-away and pick, and you need to move items to other bins without a pre-existing warehouse put-away, pick, or movement, you can register the correct placement of the items in the warehouse using the **Whse. Reclassification Journal**.</span></span>

1.  <span data-ttu-id="cf7c9-124">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Endurflokkunarbók vöruhúss** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="cf7c9-124">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Whse. Reclassification Journal**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="cf7c9-125">Reitirnir **Vörunr.**, **, Frá-svæðiskóti**, **Kóti frá-hólfs**, **Til-svæðiskóti**, and **Kóti til-hólfse** eru fylltir út.</span><span class="sxs-lookup"><span data-stu-id="cf7c9-125">Fill in the **Item No.**, **From Zone Code**, **From Bin Code**, **To Zone Code**, and **To Bin Code** fields.</span></span>  
3.  <span data-ttu-id="cf7c9-126">Velja aðgerðina **Skrá**.</span><span class="sxs-lookup"><span data-stu-id="cf7c9-126">Choose the **Register** action.</span></span>  

## <a name="see-also"></a><span data-ttu-id="cf7c9-127">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="cf7c9-127">See Also</span></span>  
[<span data-ttu-id="cf7c9-128">Vöruhúsastjórnun</span><span class="sxs-lookup"><span data-stu-id="cf7c9-128">Warehouse Management</span></span>](warehouse-manage-warehouse.md)  
[<span data-ttu-id="cf7c9-129">Birgðir</span><span class="sxs-lookup"><span data-stu-id="cf7c9-129">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="cf7c9-130">[Vöruhúsastjórnun sett upp](warehouse-setup-warehouse.md)   </span><span class="sxs-lookup"><span data-stu-id="cf7c9-130">[Setting Up Warehouse Management](warehouse-setup-warehouse.md)   </span></span>  
<span data-ttu-id="cf7c9-131">[Samsetningardeild](assembly-assemble-items.md)  </span><span class="sxs-lookup"><span data-stu-id="cf7c9-131">[Assembly Management](assembly-assemble-items.md)  </span></span>  
[<span data-ttu-id="cf7c9-132">Hönnunarupplýsingar vöruhúsakerfi</span><span class="sxs-lookup"><span data-stu-id="cf7c9-132">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="cf7c9-133">[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="cf7c9-133">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]