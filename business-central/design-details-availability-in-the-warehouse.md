---
title: Hönnunarupplýsingar - Framboð í vöruhúsi | Microsoft Docs
description: Kerfið þarf að halda sífelldri stjórn á vörum til ráðstöfunar í vöruhúsinu þannig að vörur á útleið gangi vel og sé skilað á sem besta hátt.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/08/2021
ms.author: edupont
ms.openlocfilehash: 184591134706432ed1ea04afa86e1274b748cfe0
ms.sourcegitcommit: 0953171d39e1232a7c126142d68cac858234a20e
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/09/2021
ms.locfileid: "6215504"
---
# <a name="design-details-availability-in-the-warehouse"></a><span data-ttu-id="018d3-103">Hönnunarupplýsingar: Framboð á lager</span><span class="sxs-lookup"><span data-stu-id="018d3-103">Design Details: Availability in the Warehouse</span></span>
<span data-ttu-id="018d3-104">Kerfið þarf að halda sífelldri stjórn á vörum til ráðstöfunar í vöruhúsinu þannig að vörur á útleið gangi vel og sé skilað á sem besta hátt.</span><span class="sxs-lookup"><span data-stu-id="018d3-104">The system must keep a constant control of item availability in the warehouse, so that outbound orders can flow efficiently and provide optimal deliveries.</span></span>  

<span data-ttu-id="018d3-105">Framboð er mismunandi eftir úthlutun á þeim hólfastigum þegar vöruhúsaaðgerðir, t.d. tiltektir og hreyfingar eiga sér stað og þegar frátekningarkerfið setur takmarkanir.</span><span class="sxs-lookup"><span data-stu-id="018d3-105">Availability varies depending on allocations at the bin level when warehouse activities such as picks and movements occur and when the inventory reservation system imposes restrictions to comply with.</span></span> <span data-ttu-id="018d3-106">Frekar flókið reiknirit staðfestir að öllu skilyrði eru uppfyllt áður en magni er úthlutað í tínslu fyrir útleiðarflæði.</span><span class="sxs-lookup"><span data-stu-id="018d3-106">A rather complex algorithm verifies that all conditions are met before allocating quantities to picks for outbound flows.</span></span>

<span data-ttu-id="018d3-107">Ef eitt eða fleiri skilyrði eru ekki uppfyllt geta mismunandi villuboð verið sýndar, þar með talið almennu boðin „Ekkert að afgreiða.“</span><span class="sxs-lookup"><span data-stu-id="018d3-107">If one or more conditions are not met, different error messages can be shown, including the generic "Nothing to handle."</span></span> <span data-ttu-id="018d3-108">skilaboð.</span><span class="sxs-lookup"><span data-stu-id="018d3-108">message.</span></span> <span data-ttu-id="018d3-109">„Ekkert að afgreiða.“</span><span class="sxs-lookup"><span data-stu-id="018d3-109">The "Nothing to handle."</span></span> <span data-ttu-id="018d3-110">skilaboð geta komið upp af mörgum ólíkum ástæðum, bæði í flæði á útleið og innleið, þar sem skjalalína, sem tengist með beinum eða óbeinum hætti, inniheldur reitinn **Magn til afgreiðslu**.</span><span class="sxs-lookup"><span data-stu-id="018d3-110">message can occur for many different reasons, both in outbound and inbound flows, where a directly or indirectly involved document line contains the **Qty. to Handle** field.</span></span>

> [!NOTE]
> <span data-ttu-id="018d3-111">Upplýsingarnar birtast fljótlega hér um hugsanlegar ástæður og lausnir fyrir „Ekkert að afgreiða“.</span><span class="sxs-lookup"><span data-stu-id="018d3-111">Information will soon be published here about possible reasons and solutions for the "Nothing to handle."</span></span> <span data-ttu-id="018d3-112">skilaboð.</span><span class="sxs-lookup"><span data-stu-id="018d3-112">message.</span></span>

## <a name="bin-content-and-reservations"></a><span data-ttu-id="018d3-113">Innihald hólfs og frátekningar</span><span class="sxs-lookup"><span data-stu-id="018d3-113">Bin Content and Reservations</span></span>  
 <span data-ttu-id="018d3-114">Í hvaða uppsetningu af vöruhúsakerfi sem er, er magn vara bæði til sem vöruhúsafærslur, í vöruhúsanotkunarsvæði, og sem birgðabókarfærslur í birgðanotkunarsvæði.</span><span class="sxs-lookup"><span data-stu-id="018d3-114">In any installation of warehouse management, item quantities exist both as warehouse entries, in the Warehouse application area, and as item ledger entries, in the Inventory application area.</span></span> <span data-ttu-id="018d3-115">Þessar tvær færslugerðir innihalda mismunandi upplýsingar um það hvar vara er til og hvort hún er tiltæk.</span><span class="sxs-lookup"><span data-stu-id="018d3-115">These two entry types contain different information about where items exist and whether they are available.</span></span> <span data-ttu-id="018d3-116">Vöruhúsafærslur skilgreina framboð vöru eftir hólfi og hólfagerð, sem kallast innihald hólfs.</span><span class="sxs-lookup"><span data-stu-id="018d3-116">Warehouse entries define an item’s availability by bin and bin type, which is called bin content.</span></span> <span data-ttu-id="018d3-117">Birgðahöfuðbókarfærslur skilgreina hvort vara er laus með frátekningu hennar samkvæmt fylgiskjölum á útleið.</span><span class="sxs-lookup"><span data-stu-id="018d3-117">Item ledger entries define an item’s availability by its reservation to outbound documents.</span></span>  

 <span data-ttu-id="018d3-118">Sérstök virkni í tiltektaralgrím til að reikna það magn sem er í boði til tínslu þegar innihald innihald hólfs er tengt við frátekningu.</span><span class="sxs-lookup"><span data-stu-id="018d3-118">Special functionality in the picking algorithm exists to calculate the quantity that is available to pick when bin content is coupled with reservations.</span></span>  

## <a name="quantity-available-to-pick"></a><span data-ttu-id="018d3-119">Magn tiltækt í tínslu</span><span class="sxs-lookup"><span data-stu-id="018d3-119">Quantity Available to Pick</span></span>  
 <span data-ttu-id="018d3-120">Ef, til dæmis, tínslureiknirit tekur ekki tillit til vörumagns sem eru frátekin fyrir yfirvofandi sölupöntunarsendingu, þá þessir vörur gætu verið tíndar fyrir aðra sölupöntun sem er send fyrr, sem kemur í veg fyrir fyrstu sölu frá því að vera uppfyllt.</span><span class="sxs-lookup"><span data-stu-id="018d3-120">If, for example, the picking algorithm does not consider item quantities that are reserved for a pending sales order shipment, then those items might be picked for another sales order that is shipped earlier, which prevents the first sales from being fulfilled.</span></span> <span data-ttu-id="018d3-121">Til að forðast þetta ástand, dregur tínslureikniritið frá magn sem eru frátekin fyrir aðra útleið skjöl, magni á núverandi tínsluskjalum og magn sem er valinn en ekki enn flutt eða neytt.</span><span class="sxs-lookup"><span data-stu-id="018d3-121">To avoid this situation, the picking algorithm subtracts quantities that are reserved for other outbound documents, quantities on existing pick documents, and quantities that are picked but not yet shipped or consumed.</span></span>  

 <span data-ttu-id="018d3-122">Niðurstöðurnar eru birtar í reitnum **Tiltækt magn** að tína á síðunni **Vinnublað** fyrir tínslu þar sem reiturinn er stöðugt reiknaður.</span><span class="sxs-lookup"><span data-stu-id="018d3-122">The result is displayed in the **Available Qty. to Pick** field on the **Pick Worksheet** page, where the field is calculated dynamically.</span></span> <span data-ttu-id="018d3-123">Gildið er einnig reiknað út þegar notendur stofna tiltektir í vöruhúsi beint fyrir skjöl á útleið.</span><span class="sxs-lookup"><span data-stu-id="018d3-123">The value is also calculated when users create warehouse picks directly for outbound documents.</span></span> <span data-ttu-id="018d3-124">Slík útleiðarskjöl gætu verið sölupantanir, framleiðslunotkun eða útleiðarflutningur, þar sem niðurstaðan endurspeglast í tengdum magnreitum, svo sem **Magn til afgreiðslu**.</span><span class="sxs-lookup"><span data-stu-id="018d3-124">Such outbound documents could be sales orders, production consumption, or outbound transfers, where the result is reflected in the related quantity fields, such as **Qty. to Handle**.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="018d3-125">Varðandi forgang frátekninga er magn frátekningar dregið frá magni sem er laust til tiltektar.</span><span class="sxs-lookup"><span data-stu-id="018d3-125">Concerning the priority of reservations, the quantity to reserve is subtracted from the quantity available to pick.</span></span> <span data-ttu-id="018d3-126">Til dæmis ef magnið sem tiltækt er í tínsluhólfum er 5 einingar en 100 einingar eru í frágangshólfum þá birtast villuboð ef reynt er að taka frá fleiri en 5 einingar fyrir aðra pöntun, vegna þess að viðbótarmagnið verður að vera tiltækt í tínsluhólfum.</span><span class="sxs-lookup"><span data-stu-id="018d3-126">For example, if the quantity available in pick bins is 5 units, but 100 units are in put-away bins, then when you try to reserve more than 5 units for another order, an error message is displayed because the additional quantity must be available in pick bins.</span></span>  

### <a name="calculating-the-quantity-available-to-pick"></a><span data-ttu-id="018d3-127">Reiknar magn tilbúið í tiltekt</span><span class="sxs-lookup"><span data-stu-id="018d3-127">Calculating the Quantity Available to Pick</span></span>  
 <span data-ttu-id="018d3-128">Magnið sem tiltækt er til tiltektar er reiknað svona:</span><span class="sxs-lookup"><span data-stu-id="018d3-128">The quantity available to pick is calculated as follows:</span></span>  

 <span data-ttu-id="018d3-129">magn tiltækt í tínslu = magn í tínsluhólfum - magn í tínslu og hreyfingar – (frátekið magn í tínsluhólfum + frátekið magn í tínslu og hreyfingu)</span><span class="sxs-lookup"><span data-stu-id="018d3-129">quantity available to pick = quantity in pick bins - quantity on picks and movements – (reserved quantity in pick bins + reserved quantity on picks and movements)</span></span>  

 <span data-ttu-id="018d3-130">Eftirfarandi skýringarmynd sýnir mismunandi þætti í útreikningi.</span><span class="sxs-lookup"><span data-stu-id="018d3-130">The following diagram shows the different elements of the calculation.</span></span>  

 <span data-ttu-id="018d3-131">![Tiltækt í tínslu, með pöntunarskörun](media/design_details_warehouse_management_availability_2.png "Tiltækt í tínslu, með pöntunarskörun")</span><span class="sxs-lookup"><span data-stu-id="018d3-131">![Available to pick with reservation overlap](media/design_details_warehouse_management_availability_2.png "Available to pick with reservation overlap")</span></span>  

## <a name="quantity-available-to-reserve"></a><span data-ttu-id="018d3-132">Magn tiltækt til frátekn.</span><span class="sxs-lookup"><span data-stu-id="018d3-132">Quantity Available to Reserve</span></span>  
 <span data-ttu-id="018d3-133">Þar sem hugmyndir um innihald hólfs og frátekningu og fyrirvara eru til saman, verður magn af vörum fyrir frátekningu með úthlutunum í vöruhúsaskjöl á útleið.</span><span class="sxs-lookup"><span data-stu-id="018d3-133">Because the concepts of bin content and reservation co-exist, the quantity of items that are available to reserve must be aligned with allocations to outbound warehouse documents.</span></span>  

 <span data-ttu-id="018d3-134">Það ætti að vera hægt að taka frá allar vörur í birgðum, nema þær sem eru þegar komnar í útleiðarferli.</span><span class="sxs-lookup"><span data-stu-id="018d3-134">It should be possible to reserve all items in inventory, except those that have started outbound processing.</span></span> <span data-ttu-id="018d3-135">Í samræmi er magnið sem er tiltækt fyrir frátekningu skilgreint sem magn í öllum skjölum og öllum hólfagerðum, nema eftirfarandi magn á útleið:</span><span class="sxs-lookup"><span data-stu-id="018d3-135">Accordingly, the quantity that is available to reserve is defined as the quantity on all documents and all bin types, except the following outbound quantities:</span></span>  

-   <span data-ttu-id="018d3-136">Magn í óskráðum tínsluskjölum</span><span class="sxs-lookup"><span data-stu-id="018d3-136">Quantity on unregistered pick documents</span></span>  
-   <span data-ttu-id="018d3-137">Magn í afhendingarhólfum</span><span class="sxs-lookup"><span data-stu-id="018d3-137">Quantity in shipment bins</span></span>  
-   <span data-ttu-id="018d3-138">Magn í hólfkótum til framleiðslu</span><span class="sxs-lookup"><span data-stu-id="018d3-138">Quantity in to-production bins</span></span>  
-   <span data-ttu-id="018d3-139">Magn í hólfkóta opins vinnslusalar</span><span class="sxs-lookup"><span data-stu-id="018d3-139">Quantity in open shop floor bins</span></span>  
-   <span data-ttu-id="018d3-140">Magn í hólfum til samsetningar</span><span class="sxs-lookup"><span data-stu-id="018d3-140">Quantity in to-assembly bins</span></span>  
-   <span data-ttu-id="018d3-141">Magn í leiðréttingarhólfum</span><span class="sxs-lookup"><span data-stu-id="018d3-141">Quantity in adjustment bins</span></span>  

 <span data-ttu-id="018d3-142">Niðurstöðurnar eru birtar í reitnum **Tiltækt heildarmagn** á síðunni **Frátekning**.</span><span class="sxs-lookup"><span data-stu-id="018d3-142">The result is displayed in the **Total Available Quantity** field on the **Reservation** page.</span></span>  

 <span data-ttu-id="018d3-143">Á frátekningarlínu er magnið sem ekki er hægt að taka frá, vegna þess að því hefur verið úthlutað í vöruhús, birta í reitnum **Magni úthlutað í vöruhúsi** á síðunni **Frátekning**.</span><span class="sxs-lookup"><span data-stu-id="018d3-143">On a reservation line, the quantity that cannot be reserved, because it is allocated in the warehouse, is displayed in the **Qty. Allocated in Warehouse** field on the **Reservation** page.</span></span>  

### <a name="calculating-the-quantity-available-to-reserve"></a><span data-ttu-id="018d3-144">Reikna magnið laust til frátekningar</span><span class="sxs-lookup"><span data-stu-id="018d3-144">Calculating the Quantity Available to Reserve</span></span>  
 <span data-ttu-id="018d3-145">Magnið sem tiltækt er til frátektar er reiknað svona:</span><span class="sxs-lookup"><span data-stu-id="018d3-145">The quantity available to reserve is calculated as follows:</span></span>  

 <span data-ttu-id="018d3-146">magn tiltækt í frátekningu = heildarmagn í birgðum - magn í tínslu og hreyfingu fyrir upprunaskjöl - frátekið magn - magn í hólfum á útleið</span><span class="sxs-lookup"><span data-stu-id="018d3-146">quantity available to reserve = total quantity in inventory - quantity on picks and movements for source documents - reserved quantity - quantity in outbound bins</span></span>  

 <span data-ttu-id="018d3-147">Eftirfarandi skýringarmynd sýnir mismunandi þætti í útreikningi.</span><span class="sxs-lookup"><span data-stu-id="018d3-147">The following diagram shows the different elements of the calculation.</span></span>  

 <span data-ttu-id="018d3-148">![Tiltækt í frátekningu, fyrir úthlutanir í vöruhúsi](media/design_details_warehouse_management_availability_3.png "Tiltækt í frátekningu, fyrir úthlutanir í vöruhúsi")</span><span class="sxs-lookup"><span data-stu-id="018d3-148">![Avaliable to reserve per warehouse allocation](media/design_details_warehouse_management_availability_3.png "Avaliable to reserve per warehouse allocation")</span></span>  

## <a name="see-also"></a><span data-ttu-id="018d3-149">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="018d3-149">See Also</span></span>  
 [<span data-ttu-id="018d3-150">Hönnunarupplýsingar vöruhúsakerfi</span><span class="sxs-lookup"><span data-stu-id="018d3-150">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
 [<span data-ttu-id="018d3-151">Skoða tiltækileika vöru</span><span class="sxs-lookup"><span data-stu-id="018d3-151">View the Availability of Items</span></span>](inventory-how-availability-overview.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]