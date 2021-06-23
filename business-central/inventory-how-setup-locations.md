---
title: Uppsetning staðsetningarspjalds og skilgreining flutningsleiða
description: Þú býrð til staðsetningarspjald fyrir hvern stað sem birgðavara er geymd á, til dæmis vöruhús eða dreifingarmiðstöð, og setur upp leiðir til að flytja vörur á milli staða.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: warehouse, distribution center
ms.date: 06/01/2021
ms.author: edupont
ms.openlocfilehash: 0319f0c64dd46610aa82705257091bd9478ac14f
ms.sourcegitcommit: 1aab52477956bf1aa7376fc7fb984644bc398c61
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/04/2021
ms.locfileid: "6184325"
---
# <a name="set-up-locations"></a><span data-ttu-id="95bda-103">Uppsetning birgðageymsla</span><span class="sxs-lookup"><span data-stu-id="95bda-103">Set Up Locations</span></span>

<span data-ttu-id="95bda-104">Ef vörur eru keyptar, geymdar eða seldar á fleiri en einum stað eða vöruhúsi þarf að setja hverja staðsetningu upp með staðsetningarspjaldi og skilgreina flutningsleiðir.</span><span class="sxs-lookup"><span data-stu-id="95bda-104">If you buy, store, or sell items at more than one place or warehouse, you must set up each location with a location card and define transfer routes.</span></span> <span data-ttu-id="95bda-105">[!INCLUDE [prod_short](includes/prod_short.md)] notar staðsetningar til að hjálpa til við að fylgjast með birgðum í bæði einfaldari tilvikum og flóknari vöruhúsferli.</span><span class="sxs-lookup"><span data-stu-id="95bda-105">[!INCLUDE [prod_short](includes/prod_short.md)] uses locations to help keep track of inventory in both simpler cases and the more complex warehouse processes.</span></span>

<span data-ttu-id="95bda-106">Síðan er hægt að búa til skjalalínur fyrir tilgreinda staðsetningu, skoða tiltækileika eftir staðsetningu og flytja birgðir milli staða.</span><span class="sxs-lookup"><span data-stu-id="95bda-106">You can then create document lines for a specific location, view availability by location, and transfer inventory between locations.</span></span> <span data-ttu-id="95bda-107">Frekari upplýsingar eru í [Stjórna birgðum](inventory-manage-inventory.md).</span><span class="sxs-lookup"><span data-stu-id="95bda-107">For more information, see [Manage Inventory](inventory-manage-inventory.md).</span></span>
<br><br>  
  
> [!Video https://www.microsoft.com/videoplayer/embed/RE4aQvq?rel=0]

## <a name="location-cards"></a><span data-ttu-id="95bda-108">Staðsetningarspjöld</span><span class="sxs-lookup"><span data-stu-id="95bda-108">Location cards</span></span>

<span data-ttu-id="95bda-109">Staðsetningarkortið tilgreinir upplýsingar um staðsetninguna, t.d. vöruhús eða dreifingarmiðstöð.</span><span class="sxs-lookup"><span data-stu-id="95bda-109">The location card specifies information about a location, such as a warehouse or distribution center.</span></span> <span data-ttu-id="95bda-110">Hver geymsla fær heiti og kóða.</span><span class="sxs-lookup"><span data-stu-id="95bda-110">You give each location a name and a code that represents the location.</span></span> <span data-ttu-id="95bda-111">Hægt er að færa birgðageymslukóðann inn annars staðar í forritinu þegar skrá þarf færslur vegna tiltekinnar birgðageymslu.</span><span class="sxs-lookup"><span data-stu-id="95bda-111">You can then enter the location code in other parts of the program when you want to record transactions for a given location.</span></span>  

<span data-ttu-id="95bda-112">Hægt er að færa inn upplýsingar um hólf og um skipan vöruhússins fyrir hverja staðsetningu.</span><span class="sxs-lookup"><span data-stu-id="95bda-112">You can enter information about bins and warehouse policies for each location.</span></span> <span data-ttu-id="95bda-113">Það fer eftir vöruhúsaskipaninni sem er valin, en hægt er að nota valkostina á flýtiflipanum **Hólf** til að skilgreina hólfin sem verða notuð sem sjálfgefin hólf þegar millifærslur fara fram.</span><span class="sxs-lookup"><span data-stu-id="95bda-113">Based on the warehouse policies you select, you can use the options on the **Bins** FastTab to define the bins that will be used as default bins when you are performing transactions.</span></span> <span data-ttu-id="95bda-114">Ef notaður er beinn frágangur og tínsla er hægt að nota flesta kostina á flýtuflipanum **Hólf** til að tilgreina hvernig eigi að nota mismunandi þróaðar vöruhúsaaðgerðir.</span><span class="sxs-lookup"><span data-stu-id="95bda-114">If you are using directed put-away and pick, you use most of the options on the **Bin Policies** FastTab to define how you would like to use the various advanced warehousing features.</span></span>  

<span data-ttu-id="95bda-115">Sumir valreitir eru gerðir gráir og óvirkir með öðrum stillingum á síðunni **Birgðageymsluspjald** til að takmarka óstuddar uppsetningarsamsetningar.</span><span class="sxs-lookup"><span data-stu-id="95bda-115">Some option fields are grayed and disabled by other settings in the **Location Card** page to restrict unsupported setup combinations.</span></span>  

<span data-ttu-id="95bda-116">Veldu **Svæði** eða **Hólf** aðgerðin til að skoða upplýsingar um svæði og hólf sem gætu verið skilgreint fyrir birgðageymsluna.</span><span class="sxs-lookup"><span data-stu-id="95bda-116">Choose the **Zones** or **Bins** action to view information about zones and bins that may be defined for the location.</span></span>

### <a name="to-create-a-location-card"></a><span data-ttu-id="95bda-117">Staðsetningarspjald búið til</span><span class="sxs-lookup"><span data-stu-id="95bda-117">To create a location card</span></span>

1. <span data-ttu-id="95bda-118">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Staðsetningar** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="95bda-118">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Locations**, and then choose the related link.</span></span>
2. <span data-ttu-id="95bda-119">Valið er **Nýtt** aðgerð.</span><span class="sxs-lookup"><span data-stu-id="95bda-119">Choose the **New** action.</span></span>
3. <span data-ttu-id="95bda-120">Á síðunni **Staðsetningarspjald** skal fylla út reitina eins og þörf krefur.</span><span class="sxs-lookup"><span data-stu-id="95bda-120">On the **Location Card** page, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. <span data-ttu-id="95bda-121">Endurtakið skref 2 og 3 fyrir hverja staðsetningu þar sem á að halda utan um birgðir.</span><span class="sxs-lookup"><span data-stu-id="95bda-121">Repeat steps 2 and 3 for every location where you want to keep inventory.</span></span>

> [!NOTE]  
> <span data-ttu-id="95bda-122">Margir reitir á birgðageymsluspjaldinu vísa til meðhöndlunar vara í vöruhúsaferli á inn- og útleið.</span><span class="sxs-lookup"><span data-stu-id="95bda-122">Many fields on the location card refer to the handling of items in inbound and outbound warehouse processes.</span></span> <span data-ttu-id="95bda-123">Reitirnir skipta ekki máli fyrir fyrirtæki sem þurfa ekki flóknari vöruhúsavirkni.</span><span class="sxs-lookup"><span data-stu-id="95bda-123">The fields are not relevant for companies that do not require the more complex warehouse functionality.</span></span> <span data-ttu-id="95bda-124">Nánari upplýsingar er að finna í [Uppsetning vöruhúsastjórnunar](warehouse-setup-warehouse.md).</span><span class="sxs-lookup"><span data-stu-id="95bda-124">For more information, see [Setting Up Warehouse Management](warehouse-setup-warehouse.md).</span></span>

<span data-ttu-id="95bda-125">Hægt er að breyta uppsetningu staðsetninga síðar en ekki er hægt að breyta uppsetningu staðsetninga sem hafa birgðafærslur.</span><span class="sxs-lookup"><span data-stu-id="95bda-125">You can change the configuration of a location later, but you cannot edit the setup of locations that have item ledger entries.</span></span>  

<span data-ttu-id="95bda-126">Því næst er hægt að skilgreina flutningsleiðir milli staða ef margir staðir eru til staðar.</span><span class="sxs-lookup"><span data-stu-id="95bda-126">Next, if you have multiple locations, you can define transfer routes between locations.</span></span>  

### <a name="to-create-a-transfer-route"></a><span data-ttu-id="95bda-127">Flutningsleið búin til</span><span class="sxs-lookup"><span data-stu-id="95bda-127">To create a transfer route</span></span>

1. <span data-ttu-id="95bda-128">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Flutningsleiðir** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="95bda-128">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Transfer Routes**, and then choose the related link.</span></span>
2. <span data-ttu-id="95bda-129">Að öðrum kosti, frá hvaða síðu **Staðsetningarspjalds** sem er má velja aðgerðina **Flutningsleiðir**.</span><span class="sxs-lookup"><span data-stu-id="95bda-129">Alternatively, from any **Location Card** page, choose the **Transfer Routes** action.</span></span>
3. <span data-ttu-id="95bda-130">Valið er **Nýtt** aðgerð.</span><span class="sxs-lookup"><span data-stu-id="95bda-130">Choose the **New** action.</span></span>
4. <span data-ttu-id="95bda-131">Á síðunni **Staðsetningarspjald** skal fylla út reitina eins og þörf krefur.</span><span class="sxs-lookup"><span data-stu-id="95bda-131">On the **Location Card** page, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

<span data-ttu-id="95bda-132">Nú er hægt að flytja birgðavörur milli tveggja staða.</span><span class="sxs-lookup"><span data-stu-id="95bda-132">You can now transfer inventory items between two locations.</span></span> <span data-ttu-id="95bda-133">Nánari upplýsingar eru í [Flytja birgðir milli staða](inventory-how-transfer-between-locations.md).</span><span class="sxs-lookup"><span data-stu-id="95bda-133">For more information, see [Transfer Inventory Between Locations](inventory-how-transfer-between-locations.md).</span></span>    

## <a name="bins"></a><span data-ttu-id="95bda-134">Hólf</span><span class="sxs-lookup"><span data-stu-id="95bda-134">Bins</span></span>

<span data-ttu-id="95bda-135">Hólf tákna grunnvöruhúsauppbyggingu og eru notuð til að gera tillögur að staðsetningu vöru.</span><span class="sxs-lookup"><span data-stu-id="95bda-135">Bins represent the basic warehouse structure and are used to make suggestions about the placement of items.</span></span> <span data-ttu-id="95bda-136">Þegar hólfin hafa verið stofnuð er hægt að skilgreina nánar hvaða innihald á að setja í hvert hólf eða nota hólfið sem fljótandi hólf án tiltekins innihalds.</span><span class="sxs-lookup"><span data-stu-id="95bda-136">When you have created your bins, you can define precisely the contents that you want to place in each bin, or the bin can function as a floating bin without specified contents.</span></span> <span data-ttu-id="95bda-137">Hólf eru aðallega notuð við grunn- og ítarlegar vöruhúsaðgerðir.</span><span class="sxs-lookup"><span data-stu-id="95bda-137">Bins are predominantly used in basic and advance warehouse operations.</span></span> <span data-ttu-id="95bda-138">Ef þú hefur umsjón með birgðum í einfaldari uppsetningu er líklega ekki þörf á hólfum.</span><span class="sxs-lookup"><span data-stu-id="95bda-138">If you manage inventory in a more simple setup, you probably do not need bins.</span></span>

<span data-ttu-id="95bda-139">Ef nota á hólf í birgðageymslu þarf fyrst að virkja aðgerðina á spjaldinu **Staðsetningin** með því að velja **Hólf áskilin** reitinn á flipanum **Vöruhús**.</span><span class="sxs-lookup"><span data-stu-id="95bda-139">To use the bin functionality at a location, you first activate the functionality on the **Location** card by selecting the **Bins Mandatory** field on the **Warehouse** FastTab.</span></span> <span data-ttu-id="95bda-140">Síðan er vöruflæðið í birgðageymslunni útbúið með því að tilgreina hólfakóða í uppsetningarreitum sem tákna ólík flæði.</span><span class="sxs-lookup"><span data-stu-id="95bda-140">Then you design the item flow at the location by specifying bin codes in setup fields that represent the different flows.</span></span>

> [!NOTE]
> <span data-ttu-id="95bda-141">Áður en hægt er að tilgreina hólfkóta í birgðageymsluspjaldinu þarf að stofna hólfkótana.</span><span class="sxs-lookup"><span data-stu-id="95bda-141">Before you can specify bin codes on the location card, the bin codes must be created.</span></span>

<span data-ttu-id="95bda-142">Nánari upplýsingar er að finna í [Setja upp hólf](warehouse-how-to-create-individual-bins.md) og [Setja upp hólfategundir](warehouse-how-to-set-up-bin-types.md).</span><span class="sxs-lookup"><span data-stu-id="95bda-142">For more information, see [Create Bins](warehouse-how-to-create-individual-bins.md) and [Set Up Bin Types](warehouse-how-to-set-up-bin-types.md).</span></span>  

## <a name="zones"></a><span data-ttu-id="95bda-143">Svæði</span><span class="sxs-lookup"><span data-stu-id="95bda-143">Zones</span></span>

<span data-ttu-id="95bda-144">Ef stofna á hólfin á svæðum má gera það á síðunni **Svæði**.</span><span class="sxs-lookup"><span data-stu-id="95bda-144">If you want to structure your bins under zones, you can do that in the **Zones** page.</span></span>

<span data-ttu-id="95bda-145">[!INCLUDE [prod_short](includes/prod_short.md)] afritar reitina sem stilltir eru fyrir eitthvað tiltekið svæði í hólfin innan þess.</span><span class="sxs-lookup"><span data-stu-id="95bda-145">[!INCLUDE [prod_short](includes/prod_short.md)] copies the fields that you set for any particular zone to the bins within it.</span></span> <span data-ttu-id="95bda-146">Þannig er hægt að úthluta svæði á hólf eða hólfasniðmát (afmörkun hólfa) og nokkrir aðrir reitir fyllast síðan út sjálfkrafa.</span><span class="sxs-lookup"><span data-stu-id="95bda-146">This way, you can assign a zone to a bin or a bin template (bin creation filter), and several other fields are then filled in automatically.</span></span>

<span data-ttu-id="95bda-147">Hins vegar er hægt að velja að setja bara upp eitt svæði og skipuleggja vöruhúsið aðeins eftir hólfum.</span><span class="sxs-lookup"><span data-stu-id="95bda-147">However, you can choose to set up just one zone and to organize your warehouse according to bins alone.</span></span> <span data-ttu-id="95bda-148">Nánari upplýsingar er að finna í [Uppsetning vöruhúsastjórnunar](warehouse-setup-warehouse.md).</span><span class="sxs-lookup"><span data-stu-id="95bda-148">For more information, see [Setting Up Warehouse Management](warehouse-setup-warehouse.md).</span></span>  

## <a name="see-also"></a><span data-ttu-id="95bda-149">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="95bda-149">See Also</span></span>

[<span data-ttu-id="95bda-150">Stjórna birgðum</span><span class="sxs-lookup"><span data-stu-id="95bda-150">Manage Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="95bda-151">Flytja birgðir milli birgðageymslna</span><span class="sxs-lookup"><span data-stu-id="95bda-151">Transfer Inventory Between Locations</span></span>](inventory-how-transfer-between-locations.md)  
[<span data-ttu-id="95bda-152">Stofna hólf</span><span class="sxs-lookup"><span data-stu-id="95bda-152">Create Bins</span></span>](warehouse-how-to-create-individual-bins.md)  
[<span data-ttu-id="95bda-153">Setja upp hólfategundir</span><span class="sxs-lookup"><span data-stu-id="95bda-153">Set Up Bin Types</span></span>](warehouse-how-to-set-up-bin-types.md)  
[<span data-ttu-id="95bda-154">Vöruhúsastjórnun sett upp</span><span class="sxs-lookup"><span data-stu-id="95bda-154">Setting Up Warehouse Management</span></span>](warehouse-setup-warehouse.md)  
<span data-ttu-id="95bda-155">[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="95bda-155">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="95bda-156">Breyta því hvaða eiginleikar eru sýndir</span><span class="sxs-lookup"><span data-stu-id="95bda-156">Change Which Features are Displayed</span></span>](ui-experiences.md)  
[<span data-ttu-id="95bda-157">Almenn viðskiptavirkni</span><span class="sxs-lookup"><span data-stu-id="95bda-157">General Business Functionality</span></span>](ui-across-business-areas.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]