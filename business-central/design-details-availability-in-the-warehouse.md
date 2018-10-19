---
title: "Hönnunarupplýsingar - Framboð í vöruhúsi | Microsoft Docs"
description: "Kerfið þarf að halda sífelldri stjórn á vörum til ráðstöfunar í vöruhúsinu þannig að vörur á útleið gangi vel og sé skilað á sem besta hátt."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 90d25c9c5c5687109387c548a273f4457691e151
ms.contentlocale: is-is
ms.lasthandoff: 09/28/2018

---
# <a name="design-details-availability-in-the-warehouse"></a><span data-ttu-id="cf196-103">Hönnunarupplýsingar: Framboð á lager</span><span class="sxs-lookup"><span data-stu-id="cf196-103">Design Details: Availability in the Warehouse</span></span>
<span data-ttu-id="cf196-104">Kerfið þarf að halda sífelldri stjórn á vörum til ráðstöfunar í vöruhúsinu þannig að vörur á útleið gangi vel og sé skilað á sem besta hátt.</span><span class="sxs-lookup"><span data-stu-id="cf196-104">The system must keep a constant control of item availability in the warehouse, so that outbound orders can flow efficiently and provide optimal deliveries.</span></span>  

 <span data-ttu-id="cf196-105">Framboð er mismunandi eftir úthlutun á þeim hólfastigum þegar vöruhúsaaðgerðir, t.d. tiltektir og hreyfingar eiga sér stað og þegar frátekningarkerfið setur takmarkanir.</span><span class="sxs-lookup"><span data-stu-id="cf196-105">Availability varies depending on allocations at the bin level when warehouse activities such as picks and movements occur and when the inventory reservation system imposes restrictions to comply with.</span></span> <span data-ttu-id="cf196-106">Frekar flókið reiknirit staðfestir að öllu skilyrði eru uppfyllt áður en magni er úthlutað í tínslu fyrir útleiðarflæði.</span><span class="sxs-lookup"><span data-stu-id="cf196-106">A rather complex algorithm verifies that all conditions are met before allocating quantities to picks for outbound flows.</span></span>  

## <a name="bin-content-and-reservations"></a><span data-ttu-id="cf196-107">Innihald hólfs og frátekningar</span><span class="sxs-lookup"><span data-stu-id="cf196-107">Bin Content and Reservations</span></span>  
 <span data-ttu-id="cf196-108">Í hvaða uppsetningu af vöruhúsakerfi sem er, er magn vara bæði til sem vöruhúsafærslur, í vöruhúsanotkunarsvæði, og sem birgðabókarfærslur í birgðanotkunarsvæði.</span><span class="sxs-lookup"><span data-stu-id="cf196-108">In any installation of warehouse management, item quantities exist both as warehouse entries, in the Warehouse application area, and as item ledger entries, in the Inventory application area.</span></span> <span data-ttu-id="cf196-109">Þessar tvær færslugerðir innihalda mismunandi upplýsingar um það hvar vara er til og hvort hún er tiltæk.</span><span class="sxs-lookup"><span data-stu-id="cf196-109">These two entry types contain different information about where items exist and whether they are available.</span></span> <span data-ttu-id="cf196-110">Vöruhúsafærslur skilgreina framboð vöru eftir hólfi og hólfagerð, sem kallast innihald hólfs.</span><span class="sxs-lookup"><span data-stu-id="cf196-110">Warehouse entries define an item’s availability by bin and bin type, which is called bin content.</span></span> <span data-ttu-id="cf196-111">Birgðahöfuðbókarfærslur skilgreina hvort vara er laus með frátekningu hennar samkvæmt fylgiskjölum á útleið.</span><span class="sxs-lookup"><span data-stu-id="cf196-111">Item ledger entries define an item’s availability by its reservation to outbound documents.</span></span>  

 <span data-ttu-id="cf196-112">Sérstök virkni í tiltektaralgrím til að reikna það magn sem er í boði til tínslu þegar innihald innihald hólfs er tengt við frátekningu.</span><span class="sxs-lookup"><span data-stu-id="cf196-112">Special functionality in the picking algorithm exists to calculate the quantity that is available to pick when bin content is coupled with reservations.</span></span>  

## <a name="quantity-available-to-pick"></a><span data-ttu-id="cf196-113">Magn tiltækt í tínslu</span><span class="sxs-lookup"><span data-stu-id="cf196-113">Quantity Available to Pick</span></span>  
 <span data-ttu-id="cf196-114">Ef, til dæmis, tínslureiknirit tekur ekki tillit til vörumagns sem eru frátekin fyrir yfirvofandi sölupöntunarsendingu, þá þessir vörur gætu verið tíndar fyrir aðra sölupöntun sem er send fyrr, sem kemur í veg fyrir fyrstu sölu frá því að vera uppfyllt.</span><span class="sxs-lookup"><span data-stu-id="cf196-114">If, for example, the picking algorithm does not consider item quantities that are reserved for a pending sales order shipment, then those items might be picked for another sales order that is shipped earlier, which prevents the first sales from being fulfilled.</span></span> <span data-ttu-id="cf196-115">Til að forðast þetta ástand, dregur tínslureikniritið frá magn sem eru frátekin fyrir aðra útleið skjöl, magni á núverandi tínsluskjalum og magn sem er valinn en ekki enn flutt eða neytt.</span><span class="sxs-lookup"><span data-stu-id="cf196-115">To avoid this situation, the picking algorithm subtracts quantities that are reserved for other outbound documents, quantities on existing pick documents, and quantities that are picked but not yet shipped or consumed.</span></span>  

 <span data-ttu-id="cf196-116">Niðurstöðurnar eru birtar í reitnum **Tiltækt magn að tína** í glugganum **Vinnublað fyrir tínslu** þar sem reiturinn er stöðugt reiknaður.</span><span class="sxs-lookup"><span data-stu-id="cf196-116">The result is displayed in the **Available Qty. to Pick** field in the **Pick Worksheet** window, where the field is calculated dynamically.</span></span> <span data-ttu-id="cf196-117">Gildið er einnig reiknað út þegar notendur stofna tiltektir í vöruhúsi beint fyrir skjöl á útleið.</span><span class="sxs-lookup"><span data-stu-id="cf196-117">The value is also calculated when users create warehouse picks directly for outbound documents.</span></span> <span data-ttu-id="cf196-118">Slík útleiðarskjöl gætu verið sölupantanir, framleiðslunotkun eða útleiðarflutningur, þar sem niðurstaðan endurspeglast í tengdum magnreitum, svo sem **Magn til afgreiðslu**.</span><span class="sxs-lookup"><span data-stu-id="cf196-118">Such outbound documents could be sales orders, production consumption, or outbound transfers, where the result is reflected in the related quantity fields, such as **Qty. to Handle**.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="cf196-119">Varðandi forgang frátekninga er magn frátekningar dregið frá magni sem er laust til tiltektar.</span><span class="sxs-lookup"><span data-stu-id="cf196-119">Concerning the priority of reservations, the quantity to reserve is subtracted from the quantity available to pick.</span></span> <span data-ttu-id="cf196-120">Til dæmis ef magnið sem tiltækt er í tínsluhólfum er 5 einingar en 100 einingar eru í frágangshólfum þá birtast villuboð ef reynt er að taka frá fleiri en 5 einingar fyrir aðra pöntun, vegna þess að viðbótarmagnið verður að vera tiltækt í tínsluhólfum.</span><span class="sxs-lookup"><span data-stu-id="cf196-120">For example, if the quantity available in pick bins is 5 units, but 100 units are in put-away bins, then when you try to reserve more than 5 units for another order, an error message is displayed because the additional quantity must be available in pick bins.</span></span>  

### <a name="calculating-the-quantity-available-to-pick"></a><span data-ttu-id="cf196-121">Reiknar magn tilbúið í tiltekt</span><span class="sxs-lookup"><span data-stu-id="cf196-121">Calculating the Quantity Available to Pick</span></span>  
 <span data-ttu-id="cf196-122">Magnið sem tiltækt er til tiltektar er reiknað svona:</span><span class="sxs-lookup"><span data-stu-id="cf196-122">The quantity available to pick is calculated as follows:</span></span>  

 <span data-ttu-id="cf196-123">magn tiltækt í tínslu = magn í tínsluhólfum - magn í tínslu og hreyfingar – (frátekið magn í tínsluhólfum + frátekið magn í tínslu og hreyfingu)</span><span class="sxs-lookup"><span data-stu-id="cf196-123">quantity available to pick = quantity in pick bins - quantity on picks and movements – (reserved quantity in pick bins + reserved quantity on picks and movements)</span></span>  

 <span data-ttu-id="cf196-124">Eftirfarandi skýringarmynd sýnir mismunandi þætti í útreikningi.</span><span class="sxs-lookup"><span data-stu-id="cf196-124">The following diagram shows the different elements of the calculation.</span></span>  

 <span data-ttu-id="cf196-125">![Tiltækt í tínslu, með pöntunarskörun](media/design_details_warehouse_management_availability_2.png "Tiltækt í tínslu, með pöntunarskörun")</span><span class="sxs-lookup"><span data-stu-id="cf196-125">![Available to pick with reservation overlap](media/design_details_warehouse_management_availability_2.png "Available to pick with reservation overlap")</span></span>  

## <a name="quantity-available-to-reserve"></a><span data-ttu-id="cf196-126">Magn tiltækt til frátekn.</span><span class="sxs-lookup"><span data-stu-id="cf196-126">Quantity Available to Reserve</span></span>  
 <span data-ttu-id="cf196-127">Þar sem hugmyndir um innihald hólfs og frátekningu og fyrirvara eru til saman, verður magn af vörum fyrir frátekningu með úthlutunum í vöruhúsaskjöl á útleið.</span><span class="sxs-lookup"><span data-stu-id="cf196-127">Because the concepts of bin content and reservation co-exist, the quantity of items that are available to reserve must be aligned with allocations to outbound warehouse documents.</span></span>  

 <span data-ttu-id="cf196-128">Það ætti að vera hægt að taka frá allar vörur í birgðum, nema þær sem eru þegar komnar í útleiðarferli.</span><span class="sxs-lookup"><span data-stu-id="cf196-128">It should be possible to reserve all items in inventory, except those that have started outbound processing.</span></span> <span data-ttu-id="cf196-129">Í samræmi er magnið sem er tiltækt fyrir frátekningu skilgreint sem magn í öllum skjölum og öllum hólfagerðum, nema eftirfarandi magn á útleið:</span><span class="sxs-lookup"><span data-stu-id="cf196-129">Accordingly, the quantity that is available to reserve is defined as the quantity on all documents and all bin types, except the following outbound quantities:</span></span>  

-   <span data-ttu-id="cf196-130">Magn í óskráðum tínsluskjölum</span><span class="sxs-lookup"><span data-stu-id="cf196-130">Quantity on unregistered pick documents</span></span>  
-   <span data-ttu-id="cf196-131">Magn í afhendingarhólfum</span><span class="sxs-lookup"><span data-stu-id="cf196-131">Quantity in shipment bins</span></span>  
-   <span data-ttu-id="cf196-132">Magn í hólfkótum til framleiðslu</span><span class="sxs-lookup"><span data-stu-id="cf196-132">Quantity in to-production bins</span></span>  
-   <span data-ttu-id="cf196-133">Magn í hólfkóta opins vinnslusalar</span><span class="sxs-lookup"><span data-stu-id="cf196-133">Quantity in open shop floor bins</span></span>  
-   <span data-ttu-id="cf196-134">Magn í hólfum til samsetningar</span><span class="sxs-lookup"><span data-stu-id="cf196-134">Quantity in to-assembly bins</span></span>  
-   <span data-ttu-id="cf196-135">Magn í leiðréttingarhólfum</span><span class="sxs-lookup"><span data-stu-id="cf196-135">Quantity in adjustment bins</span></span>  

 <span data-ttu-id="cf196-136">Niðurstöðurnar eru birtar í reitnum **Tiltækt heildarmagn** í glugganum **Frátekning**.</span><span class="sxs-lookup"><span data-stu-id="cf196-136">The result is displayed in the **Total Available Quantity** field in the **Reservation** window.</span></span>  

 <span data-ttu-id="cf196-137">Á frátekningarlínu er magnið sem ekki er hægt að taka frá, vegna þess að því hefur verið úthlutað í vöruhús, birta í reitnum **Magni úthlutað í vöruhúsi** í glugganum **Frátekning**.</span><span class="sxs-lookup"><span data-stu-id="cf196-137">On a reservation line, the quantity that cannot be reserved, because it is allocated in the warehouse, is displayed in the **Qty. Allocated in Warehouse** field in the **Reservation** window.</span></span>  

### <a name="calculating-the-quantity-available-to-reserve"></a><span data-ttu-id="cf196-138">Reikna magnið laust til frátekningar</span><span class="sxs-lookup"><span data-stu-id="cf196-138">Calculating the Quantity Available to Reserve</span></span>  
 <span data-ttu-id="cf196-139">Magnið sem tiltækt er til frátektar er reiknað svona:</span><span class="sxs-lookup"><span data-stu-id="cf196-139">The quantity available to reserve is calculated as follows:</span></span>  

 <span data-ttu-id="cf196-140">magn tiltækt í frátekningu = heildarmagn í birgðum - magn í tínslu og hreyfingu fyrir upprunaskjöl - frátekið magn - magn í hólfum á útleið</span><span class="sxs-lookup"><span data-stu-id="cf196-140">quantity available to reserve = total quantity in inventory - quantity on picks and movements for source documents - reserved quantity - quantity in outbound bins</span></span>  

 <span data-ttu-id="cf196-141">Eftirfarandi skýringarmynd sýnir mismunandi þætti í útreikningi.</span><span class="sxs-lookup"><span data-stu-id="cf196-141">The following diagram shows the different elements of the calculation.</span></span>  

 <span data-ttu-id="cf196-142">![Tiltækt í frátekningu, fyrir úthlutanir í vöruhúsi](media/design_details_warehouse_management_availability_3.png "Tiltækt í frátekningu, fyrir úthlutanir í vöruhúsi")</span><span class="sxs-lookup"><span data-stu-id="cf196-142">![Avaliable to reserve per warehouse allocation](media/design_details_warehouse_management_availability_3.png "Avaliable to reserve per warehouse allocation")</span></span>  

## <a name="see-also"></a><span data-ttu-id="cf196-143">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="cf196-143">See Also</span></span>  
 [<span data-ttu-id="cf196-144">Hönnunarupplýsingar vöruhúsakerfi</span><span class="sxs-lookup"><span data-stu-id="cf196-144">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)

