---
title: Þjónustupöntunarstaða og viðgerðarstaða
description: Reitirnir Staða á síðunni Þjónustupöntun og þjónustuvöruviðgerðarstaðan sem vísað er til í reitnum Viðgerðarstöðukóti á síðunni Þjónustupöntun hafa ákveðið samband í Þjónustukerfi. Þjónustupöntunarstaðan sýnir viðgerðarstöðu allra þjónustuvara í þjónustupöntuninni.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/15/2020
ms.author: edupont
ms.openlocfilehash: 9bbe3a4263250a7d06bfffa2019114eba72a31ca
ms.sourcegitcommit: 2d2dfb6c3eca1322835f0167dc7dab614346972e
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/19/2020
ms.locfileid: "4038619"
---
# <a name="service-order-status-and-repair-status"></a><span data-ttu-id="147d1-104">Þjónustupöntunarstaða og viðgerðarstaða</span><span class="sxs-lookup"><span data-stu-id="147d1-104">Service Order Status and Repair Status</span></span>

<span data-ttu-id="147d1-105">Reitirnir **Staða** á síðunni **Þjónustupöntun** og þjónustuvöruviðgerðarstaðan sem vísað er til í reitnum **Viðgerðarstöðukóti** á síðunni **Þjónustupöntun** hafa ákveðið samband í Þjónustukerfi.</span><span class="sxs-lookup"><span data-stu-id="147d1-105">The **Status** field on the **Service Order** page and the service item repair status, which is represented by the **Repair Status Code** field on the **Service Order** page have a certain relationship in Service Management.</span></span> <span data-ttu-id="147d1-106">Þjónustupöntunarstaðan sýnir viðgerðarstöðu allra þjónustuvara í þjónustupöntuninni.</span><span class="sxs-lookup"><span data-stu-id="147d1-106">The service order status reflects the repair status of all the service items in the service order.</span></span>  

> [!NOTE]  
> <span data-ttu-id="147d1-107">Þessir tveir stöðureitir tengjast ekki reitnum **Losunarstaða** á þjónustupöntunarhausnum, sem ákvarðar hvernig vöruhúsið meðhöndlar þjónustuvörur.</span><span class="sxs-lookup"><span data-stu-id="147d1-107">These two status field are not related to the **Release Status** field on the service order header, which determines how the warehouse handles service items.</span></span>  

<span data-ttu-id="147d1-108">Í hvert sinn sem viðgerðarstöðu þjónustuvöru er breytt í þjónustupöntun er staða pöntunarinnar uppfærð.</span><span class="sxs-lookup"><span data-stu-id="147d1-108">Each time the repair status of a service item is changed in a service order, the status of the order is updated.</span></span> <span data-ttu-id="147d1-109">Til að forritið sýni stöðuna sem sýnir yfirlit yfir viðgerðarstöðuna hjá einstökum þjónustuvörum verður að tilgreina eftirfarandi:</span><span class="sxs-lookup"><span data-stu-id="147d1-109">To display the status that reflects the overall repair status of the individual service items, you must specify the following:</span></span>  

* <span data-ttu-id="147d1-110">Staða þjónustupöntunar sem allar viðgerðarstöður tengjast.</span><span class="sxs-lookup"><span data-stu-id="147d1-110">The service order status that each repair status is linked to.</span></span>  
* <span data-ttu-id="147d1-111">Forgangsröð fyrir hvern valkost þjónustupöntunarstöðu.</span><span class="sxs-lookup"><span data-stu-id="147d1-111">The level of priority of each service order status option.</span></span>  

<span data-ttu-id="147d1-112">Þegar þjónustutilboði er breytt í þjónustupöntun breytir kerfið viðgerðarstöðu hverrar þjónustuvöru í pöntuninni í **Byrjun** og stöðu þjónustupöntunar í **Í undirbúningi**.</span><span class="sxs-lookup"><span data-stu-id="147d1-112">When you convert a service quote to a service order, the repair status of each service item is changed in the order to **Initial** and the service order status is changed to **Pending**.</span></span>  

> [!NOTE]
> <span data-ttu-id="147d1-113">Áður en hægt er að búa til þjónustupantanir þarf að setja upp viðgerðarstöðu og forgang þjónustustöðu.</span><span class="sxs-lookup"><span data-stu-id="147d1-113">Before you can create service orders, you must set up repair statuses and service status priorities.</span></span> <span data-ttu-id="147d1-114">Frekari upplýsingar eru í [Setja upp stöður fyrir þjónustupantanir og viðgerðir](service-order-repair-status.md).</span><span class="sxs-lookup"><span data-stu-id="147d1-114">For more information, see [Set Up Statuses for Service Orders and Repairs](service-order-repair-status.md).</span></span>

## <a name="specifying-service-order-status-for-repair-status"></a><span data-ttu-id="147d1-115">Þjónustupöntunarstaða tilgreind fyrir viðgerðarstöðu</span><span class="sxs-lookup"><span data-stu-id="147d1-115">Specifying Service Order Status for Repair Status</span></span>

<span data-ttu-id="147d1-116">Hver viðgerðarstaða er tengt tiltekinni þjónustupöntunarstöðu.</span><span class="sxs-lookup"><span data-stu-id="147d1-116">Each repair status is linked to a particular service order status.</span></span> <span data-ttu-id="147d1-117">Valkostirnir fyrir þjónustupöntunarstöðuna eru eftirfarandi:</span><span class="sxs-lookup"><span data-stu-id="147d1-117">The options for the service order status are as follows:</span></span>

* <span data-ttu-id="147d1-118">**Í undirbúningi**</span><span class="sxs-lookup"><span data-stu-id="147d1-118">**Pending**</span></span>
* <span data-ttu-id="147d1-119">**Í vinnslu**</span><span class="sxs-lookup"><span data-stu-id="147d1-119">**In Process**</span></span>
* <span data-ttu-id="147d1-120">**Bið**</span><span class="sxs-lookup"><span data-stu-id="147d1-120">**On Hold**</span></span>
* <span data-ttu-id="147d1-121">**Lokið**</span><span class="sxs-lookup"><span data-stu-id="147d1-121">**Finished**</span></span>

<span data-ttu-id="147d1-122">Valkostirnir fyrir viðgerðarstöðu eru eftirfarandi:</span><span class="sxs-lookup"><span data-stu-id="147d1-122">The repair status options are as follows:</span></span>

* <span data-ttu-id="147d1-123">**Byrjun**</span><span class="sxs-lookup"><span data-stu-id="147d1-123">**Initial**</span></span>
* <span data-ttu-id="147d1-124">**Í vinnslu**</span><span class="sxs-lookup"><span data-stu-id="147d1-124">**In Process**</span></span>
* <span data-ttu-id="147d1-125">**Sent áfram**</span><span class="sxs-lookup"><span data-stu-id="147d1-125">**Referred**</span></span>
* <span data-ttu-id="147d1-126">**Hluta þjónustu lokið**</span><span class="sxs-lookup"><span data-stu-id="147d1-126">**Partly Serviced**</span></span>
* <span data-ttu-id="147d1-127">**Tilboði lokið**</span><span class="sxs-lookup"><span data-stu-id="147d1-127">**Quote Finished**</span></span>
* <span data-ttu-id="147d1-128">**Beðið eftir viðskiptavini**</span><span class="sxs-lookup"><span data-stu-id="147d1-128">**Waiting for Customer**</span></span>
* <span data-ttu-id="147d1-129">**Íhlutur pantaður**</span><span class="sxs-lookup"><span data-stu-id="147d1-129">**Spare Part Ordered**</span></span>
* <span data-ttu-id="147d1-130">**Íhlutur móttekin**</span><span class="sxs-lookup"><span data-stu-id="147d1-130">**Spare Part Received**</span></span>
* <span data-ttu-id="147d1-131">**Lokið**</span><span class="sxs-lookup"><span data-stu-id="147d1-131">**Finished**</span></span>  

### <a name="pending"></a><span data-ttu-id="147d1-132">Í undirbúningi</span><span class="sxs-lookup"><span data-stu-id="147d1-132">Pending</span></span>

<span data-ttu-id="147d1-133">Þjónustupöntunarstaðan **Í undirbúningi** gefur til kynna að þjónustan geti hafist eða haldið áfram hvenær sem er.</span><span class="sxs-lookup"><span data-stu-id="147d1-133">The service order status **Pending** indicates that the service can start or continue at any time.</span></span> <span data-ttu-id="147d1-134">Því er hægt að tengja viðgerðarstöðuvalkostina **Byrjun**, **Verki vísað**, **Hluta þjónustu lokið** og **Varahlutur móttekinn** við þjónustupöntunarstöðuna.</span><span class="sxs-lookup"><span data-stu-id="147d1-134">Therefore, the repair status options of **Initial**, **Referred**, **Partly Serviced**, and **Spare Part Received** can be linked to this service order status.</span></span>  

### <a name="in-process"></a><span data-ttu-id="147d1-135">Í vinnslu</span><span class="sxs-lookup"><span data-stu-id="147d1-135">In Process</span></span>

<span data-ttu-id="147d1-136">Þjónustupöntunarstaðan **Í vinnslu** gefur til kynna að þjónustan sé í vinnslu.</span><span class="sxs-lookup"><span data-stu-id="147d1-136">The service order status **In Process** indicates that the service is in process.</span></span> <span data-ttu-id="147d1-137">Því er hægt að tengja viðgerðarstöðuvalkostina **Í vinnslu** og **Varahlutur pantaður** við þjónustupöntunarstöðuna.</span><span class="sxs-lookup"><span data-stu-id="147d1-137">Therefore, the repair status options **In Process** and **Spare Part Ordered** can both be linked to this service order status.</span></span> <span data-ttu-id="147d1-138">Ef staðan **Varahlutur pantaður** er tengd við þjónustupöntunarstöðuna **Í vinnslu** verður einnig að tengja stöðuna **Varahlutur móttekinn** við þessa þjónustupöntunarstöðu.</span><span class="sxs-lookup"><span data-stu-id="147d1-138">If you link the **Spare Part Ordered** status to an **In Process** service order status, you must also link the **Spare Part Received** status to this service order status.</span></span>  

### <a name="on-hold"></a><span data-ttu-id="147d1-139">Bið</span><span class="sxs-lookup"><span data-stu-id="147d1-139">On Hold</span></span>

<span data-ttu-id="147d1-140">Þjónustupöntunarstaðan **Bið** gefur til kynna að þjónustan sé um stundarsakir í bið þar sem beðið sé eftir viðbrögðum frá viðskiptavini eða varahlutum áður en þjónustan getur hafist.</span><span class="sxs-lookup"><span data-stu-id="147d1-140">The service order status **On Hold** indicates that the service is temporarily on hold because you are waiting for a customer response or spare parts before the service can start.</span></span> <span data-ttu-id="147d1-141">Því er hægt að tengja viðgerðarstöðuvalkostina **Tilboði lokið**, **Varahlutur pantaður** og **Beðið eftir viðskiptavini** við þjónustupöntunarstöðuna.</span><span class="sxs-lookup"><span data-stu-id="147d1-141">Therefore, the repair status options of **Quote Finished**, **Spare Part Ordered**, and **Waiting for Customer** can be linked to this service order status.</span></span>  

### <a name="finished"></a><span data-ttu-id="147d1-142">Lokið</span><span class="sxs-lookup"><span data-stu-id="147d1-142">Finished</span></span>

<span data-ttu-id="147d1-143">Þjónustupöntunarstaðan **Lokið** gefur til kynna að þjónustunni sé lokið.</span><span class="sxs-lookup"><span data-stu-id="147d1-143">The service order status **Finished** indicates that the service has been completed.</span></span> <span data-ttu-id="147d1-144">Því er viðgerðarstaðan **Lokið** tengd við þessa stöðu.</span><span class="sxs-lookup"><span data-stu-id="147d1-144">Therefore, the **Finished** repair status is linked to this status.</span></span>  

## <a name="assigning-priority-to-service-order-status"></a><span data-ttu-id="147d1-145">Þjónustupöntunarstöðu úthlutað forgangi</span><span class="sxs-lookup"><span data-stu-id="147d1-145">Assigning Priority to Service Order Status</span></span>

<span data-ttu-id="147d1-146">Þegar viðgerðarstöðu þjónustuvöru er breytt eru þjónustupöntunarstöðurnar tengdar við viðgerðarstöður allra þjónustuvaranna í pöntuninni.</span><span class="sxs-lookup"><span data-stu-id="147d1-146">When a repair status of a service item is changed, the service order status options linked to the different repair status options of all the service items in the order are identified.</span></span> <span data-ttu-id="147d1-147">Ef þjónustuvaran tengist einni eða fleiri þjónustupöntunarstöðuvalkostum er þjónustupöntunarstöðuvalkosturinn valinn sem gefur mesta forgangsröð.</span><span class="sxs-lookup"><span data-stu-id="147d1-147">If the service items are linked to two or more service order status options, the service order status option with the highest priority is selected.</span></span>  

<span data-ttu-id="147d1-148">Ákveða þarf hvaða þjónustupöntunarstöðuvalkostur hefur mikilvægustu upplýsingarnar í stöðunni í þjónustupöntuninni og setja þá stöðu efst í forgangsröðina o.s.frv.</span><span class="sxs-lookup"><span data-stu-id="147d1-148">You must decide which service order status contains the most important information about the status of the service order and assign that status the highest priority, and so on.</span></span>  

<span data-ttu-id="147d1-149">Þegar ný þjónustupöntun er stofnuð og vörum er bætt við hana er reiturinn **Forgangur** í þjónustupöntunarhausnum uppfærður út frá forgangsröðunum á þjónustuvörunum.</span><span class="sxs-lookup"><span data-stu-id="147d1-149">Then, when you create a new service order and you add service items to it, the **Priority** field on the service order header is updated based on the priorities on the service items.</span></span>  

### <a name="example"></a><span data-ttu-id="147d1-150">Dæmi</span><span class="sxs-lookup"><span data-stu-id="147d1-150">Example</span></span>

<span data-ttu-id="147d1-151">Dæmigerð úthlutun forgangsraðar gæti verið sem hér segir:</span><span class="sxs-lookup"><span data-stu-id="147d1-151">A typical priority level assignment could be as follows:</span></span>  

* <span data-ttu-id="147d1-152">Í vinnslu - Mikill</span><span class="sxs-lookup"><span data-stu-id="147d1-152">In Process - High</span></span>  
* <span data-ttu-id="147d1-153">Í undirbúningi - Í meðallagi mikill</span><span class="sxs-lookup"><span data-stu-id="147d1-153">Pending - Medium high</span></span>  
* <span data-ttu-id="147d1-154">Bið - Í meðallagi lítill</span><span class="sxs-lookup"><span data-stu-id="147d1-154">On Hold - Medium low</span></span>  
* <span data-ttu-id="147d1-155">Lokið - Lítill</span><span class="sxs-lookup"><span data-stu-id="147d1-155">Finished - Low</span></span>  

<span data-ttu-id="147d1-156">Ef ein þjónustuvara er til dæmis með viðgerðarstöðuna **Byrjun** tengda við þjónustupöntunarstöðuna **Í undirbúningi**, önnur er með viðgerðarstöðuna **Í vinnslu**, tengda við þjónustupöntunarstöðuna **Í vinnslu** og sú þriðja er með viðgerðarstöðuna **Varahlutur pantaður**, tengda við þjónustupöntunarstöðuna **Bið**, verður útkoman staðan **Í vinnslu** þar sem hún er með mestan forgang.</span><span class="sxs-lookup"><span data-stu-id="147d1-156">For example, if one service item has the repair status **Initial**, linked to the service order status **Pending**, another has the repair status **In Process**, linked to the service order status **In Process**, and a third has the repair status **Spare Part Ordered**, linked to the service order status **On Hold**, the resulting service order status will be **In Process** because this has the highest priority.</span></span>  

## <a name="see-also"></a><span data-ttu-id="147d1-157">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="147d1-157">See Also</span></span>

[<span data-ttu-id="147d1-158">Setja upp stöður fyrir þjónustupantanir og viðgerðir</span><span class="sxs-lookup"><span data-stu-id="147d1-158">Set Up Statuses for Service Orders and Repairs</span></span>](service-order-repair-status.md)  
[<span data-ttu-id="147d1-159">Þjónustustýring sett upp</span><span class="sxs-lookup"><span data-stu-id="147d1-159">Setting Up Service Management</span></span>](service-setup-service.md)  
