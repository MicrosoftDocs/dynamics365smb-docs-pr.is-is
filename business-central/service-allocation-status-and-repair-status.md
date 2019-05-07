---
title: Úthlutunarstaða og viðgerðarstaða | Microsoft Docs
description: Lærðu um sambandið á milli viðgerðarstaða þjónustuvöru og úthlutunarstaða úthlutunarfærslna fyrir þær.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: resources, allocation, status, repairs
ms.date: 04/01/2019
ms.author: bholtorf
ms.openlocfilehash: ca6edfb33aebedeb70deb17b78abbdb0024f7b2d
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2019
ms.locfileid: "920251"
---
# <a name="allocation-status-and-repair-status-of-service-items"></a><span data-ttu-id="7a9f2-103">Úthlutunarstaða og viðgerðarstaða</span><span class="sxs-lookup"><span data-stu-id="7a9f2-103">Allocation Status and Repair Status of Service Items</span></span>
<span data-ttu-id="7a9f2-104">Viðgerðarstaða þjónustuvöru og úthlutarstaða úthlutunarfærslna vegna þjónustuvöru tengjast á vissan hátt í Þjónustukerfi.</span><span class="sxs-lookup"><span data-stu-id="7a9f2-104">The repair status of service items and the allocation status of the allocation entries for the service items have a certain relationship in Service Management.</span></span> <span data-ttu-id="7a9f2-105">Úthlutunarstaðan breytist þegar viðgerðarstöðu þjónustuvöru er breytt úr  **Lokið** eða  **Hluta þjónustu lokið** og þegar þjónustutilboði er breytt í þjónustupöntun.</span><span class="sxs-lookup"><span data-stu-id="7a9f2-105">The allocation status changes when you change the repair status of the service item to **Finished** or **Partly Serviced** and when you convert a service quote to a service order.</span></span> <span data-ttu-id="7a9f2-106">Viðgerðarstaða þjónustuvöru breytist þegar hætt er við úthlutun þjónustuvöru eða henni er endurúthlutað til annars forða.</span><span class="sxs-lookup"><span data-stu-id="7a9f2-106">The repair status of the service item changes when you cancel the service item allocation or reallocate the service item to another resource.</span></span> <span data-ttu-id="7a9f2-107">Hægt er að skoða viðgerðastöðu þjónustuvöru á síðunni **Þjónustuverk** og hægt er að uppfæra viðgerðarstöðu í **Kóti viðgerðastöðu** á síðunni **Þjónustuvörublað**.</span><span class="sxs-lookup"><span data-stu-id="7a9f2-107">You can view the repair status of service items on the **Service Tasks** page and you can update the repair status in the **Repair Status Code** field on the **Service Item Worksheet** page.</span></span> <span data-ttu-id="7a9f2-108">Hægt er að skoða úthlutunarstöðuna í reitnum **Staða** á síðunni **Úthlutun forða**.</span><span class="sxs-lookup"><span data-stu-id="7a9f2-108">You can view the allocation status in the **Status** field on the **Resource Allocations** page.</span></span>  
  
## <a name="changing-repair-status"></a><span data-ttu-id="7a9f2-109">Viðgerðarstöðu breytt</span><span class="sxs-lookup"><span data-stu-id="7a9f2-109">Changing Repair Status</span></span>  
<span data-ttu-id="7a9f2-110">Þegar viðgerðarstöðu þjónustu vöru er breytt í þjónustuvörulínu leitar forritið að samsvarandi úthlutunarfærslu fyrir þessa þjónustuvöru sem hefur stöðuna **Virk**.</span><span class="sxs-lookup"><span data-stu-id="7a9f2-110">When you change the repair status of a service item on a service item line, there is a search for a corresponding allocation entry for this service item that has the status **Active**.</span></span> <span data-ttu-id="7a9f2-111">Ef úthlutunarfærslan finnst er staðan uppfærð á einn af eftirfarandi háttum:</span><span class="sxs-lookup"><span data-stu-id="7a9f2-111">If such an allocation entry is found, the status is updated in one of the following ways:</span></span>  
  
* <span data-ttu-id="7a9f2-112">Ef viðgerðarstaðan breytist í **Lokið** breytir forritið úthlutunarstöðunni úr **Virk** í **Lokið**.</span><span class="sxs-lookup"><span data-stu-id="7a9f2-112">If you change the repair status to **Finished**, the allocation status is changed from **Active** to **Finished**.</span></span>  
* <span data-ttu-id="7a9f2-113">Ef viðgerðarstaðan breytist í **Hluta þjónustu lokið** (hluti vinnunnar er búinn) eða **Verki vísað** (engin vinna hafin) breytir forritið úthlutunarstöðunni úr **Virk** í **Þarf að endurúthluta**.</span><span class="sxs-lookup"><span data-stu-id="7a9f2-113">If you change the repair status to **Partly Serviced**, that is, some of the service has been completed, or **Referred**, that is, no service has been done, the allocation status is changed from **Active** to **Reallocation Needed**.</span></span>  
* <span data-ttu-id="7a9f2-114">Ef úthlutunarfærsla þjónustupöntunar er búin til og gefið er til kynna að engum forða hafi verið úthlutað stillir kerfið **Stöðu** reits á síðunni **Úthlutun forða** á **Óvirkt**.</span><span class="sxs-lookup"><span data-stu-id="7a9f2-114">When a service order allocation entry is created that indicates that no resource has been allocated, the **Status** field on the **Resource Allocation** page is set to **Nonactive**.</span></span>  
* <span data-ttu-id="7a9f2-115">Staða úthlutunarfærslu er stillt á **Hætt við** ef þjónustuvöru sem vísað er til í úthlutunarfærslu er endurúthlutað, sem gefur til kynna að úthlutaður forði eða forðaflokkur hafi ekki reynt þjónustuverkhlutann.</span><span class="sxs-lookup"><span data-stu-id="7a9f2-115">The allocation entry status is set to **Canceled** when you reallocate the referred service item in the service order allocation entry, which indicates that the allocated resource or resource group has not attempted the service task.</span></span>  
  
<span data-ttu-id="7a9f2-116">úthlutunarstaðan ber með sér hvort þjónustuverki sé lokið eða hvort annan forða þurfi til þess að ljúka viðkomandi þjónustu.</span><span class="sxs-lookup"><span data-stu-id="7a9f2-116">The allocation status reflects when the service process is finished, or when another resource is necessary in order to finish the service of the service item.</span></span>  
  
## <a name="converting-service-quotes-to-service-orders"></a><span data-ttu-id="7a9f2-117">Þjónustutilboði breytt í þjónustupöntun</span><span class="sxs-lookup"><span data-stu-id="7a9f2-117">Converting Service Quotes to Service Orders</span></span>  
<span data-ttu-id="7a9f2-118">Þegar þjónustutilboði er breytt í þjónustupöntun uppfærir kerfið þjónustupöntunina, þjónustuvöruna í pöntuninni og úthlutunarfærslur með einhverri eftirfarandi aðferða:</span><span class="sxs-lookup"><span data-stu-id="7a9f2-118">When you convert a service quote to a service order, the service order, the service items in the order and their allocation entries are updated in the following ways:</span></span>  
  
* <span data-ttu-id="7a9f2-119">Viðgerðarstöðu þjónustuvörunnar er breytt í **Byrjun**.</span><span class="sxs-lookup"><span data-stu-id="7a9f2-119">The repair status of the service items is changed to **Initial**.</span></span>  
* <span data-ttu-id="7a9f2-120">Staða þjónustupöntunar breytist í **Í undirbúningi**.</span><span class="sxs-lookup"><span data-stu-id="7a9f2-120">The service order status is changed to **Pending**.</span></span>  
* <span data-ttu-id="7a9f2-121">Leitað er að úthlutunarfærslum vegna allrar þjónustuvörunnar í þjónustupöntuninni sem er með stöðuna **Virk**.</span><span class="sxs-lookup"><span data-stu-id="7a9f2-121">There is a search for allocation entries for all the service items in the service order that have the status **Active**.</span></span> <span data-ttu-id="7a9f2-122">Ef slíkar úthlutunarfærsla finnast er stöðu úthlutunar breytt úr **Virk** í **Þarf að endurúthluta**.</span><span class="sxs-lookup"><span data-stu-id="7a9f2-122">If such allocation entries are found, their allocation status is changed from **Active** to **Reallocation Needed**.</span></span>  
  
## <a name="canceling-allocations"></a><span data-ttu-id="7a9f2-123">Hætt við úthlutanir</span><span class="sxs-lookup"><span data-stu-id="7a9f2-123">Canceling Allocations</span></span>  
<span data-ttu-id="7a9f2-124">Þegar úthlutun vegna þjónustuvöru er afturkölluð uppfærir [!INCLUDE[d365fin](includes/d365fin_md.md)] úthlutunarstöðu samsvarandi úthlutunarfærslu frá **Virk** yfir í **Þörf á endurúthlutun**.</span><span class="sxs-lookup"><span data-stu-id="7a9f2-124">When you cancel an allocation for a service item, [!INCLUDE[d365fin](includes/d365fin_md.md)] updates the allocation status of the corresponding allocation entry from **Active** to **Reallocation Needed**.</span></span>

<span data-ttu-id="7a9f2-125">Viðgerðarstaða þjónustuvörunnar í úthlutunarfærslunni er uppfærð sem hér segir:</span><span class="sxs-lookup"><span data-stu-id="7a9f2-125">The repair status of the service item in the allocation entry is updated in the following ways:</span></span>  
  
* <span data-ttu-id="7a9f2-126">Ef viðgerðarstaðan er **Byrjun** er viðgerðarstöðunni breytt í **Verki vísað** (engin þjónusta hefur verið veitt).</span><span class="sxs-lookup"><span data-stu-id="7a9f2-126">If the repair status is **Initial**, the repair status is changed to **Referred** (no service has been started).</span></span>  
* <span data-ttu-id="7a9f2-127">Ef viðgerðarstaðan er **Í vinnslu** er viðgerðarstöðunni breytt í **Hluta þjónustu lokið** (hluti vinnunnar búinn).</span><span class="sxs-lookup"><span data-stu-id="7a9f2-127">If the repair status is **In Process**, the repair status is changed to **Partly Serviced** (some service has been completed).</span></span>  
  
## <a name="reallocating-an-active-allocation-entry"></a><span data-ttu-id="7a9f2-128">Endurúthluta virkri úthlutnarfærslu</span><span class="sxs-lookup"><span data-stu-id="7a9f2-128">Reallocating an Active Allocation Entry</span></span>  
<span data-ttu-id="7a9f2-129">Þegar þjónustuvöru er endurúthlutað í úthlutunarfærslu sem er **Virk** er úthlutunarfærslan uppfærð sem hér segir:</span><span class="sxs-lookup"><span data-stu-id="7a9f2-129">When you reallocate a service item in an allocation entry that is **Active**, the allocation entry is updated in the following ways:</span></span>  
  
* <span data-ttu-id="7a9f2-130">Hafi þjónustan hafist þegar úthlutun var **Virk** (hafi viðgerðarstaða þjónustuvörunnar í færslunni breyst í **Í vinnslu**) er úthlutunarstöðunni breytt úr **Virk** í **Lokið**.</span><span class="sxs-lookup"><span data-stu-id="7a9f2-130">If service was started when the allocation was **Active** (that is, if the repair status of the service item in the entry was changed to **In Process**), the allocation status is changed from **Active** to **Finished**.</span></span>  
* <span data-ttu-id="7a9f2-131">Hafi þjónusta ekki hafist þegar úthlutun var **Virk** er úthlutunarstöðu breytt úr **Virk** í **Hætt við**.</span><span class="sxs-lookup"><span data-stu-id="7a9f2-131">If service was not started when the allocation was **Active**, the allocation status is changed from **Active** to **Canceled**.</span></span>  
  
<span data-ttu-id="7a9f2-132">Viðgerðarstaða þjónustuvörunnar í úthlutunarfærslunni er uppfærð eins og ef úthlutunin hefði verið afturkölluð.</span><span class="sxs-lookup"><span data-stu-id="7a9f2-132">The repair status of the service item in the allocation entry is updated in the same way as if you had canceled the allocation:</span></span>  
  
* <span data-ttu-id="7a9f2-133">Ef viðgerðarstaðan er **Byrjun** er viðgerðarstöðunni breytt í **Verki vísað** (engin þjónusta hefur verið veitt).</span><span class="sxs-lookup"><span data-stu-id="7a9f2-133">If the repair status is **Initial**, the repair status is changed to **Referred** (no service has been started).</span></span>  
* <span data-ttu-id="7a9f2-134">Ef viðgerðarstaðan er **Í vinnslu** er viðgerðarstöðunni breytt í **Hluta þjónustu lokið** (hluti vinnunnar búinn).</span><span class="sxs-lookup"><span data-stu-id="7a9f2-134">If the repair status is **In Process**, the repair status is changed to **Partly Serviced** (some service has been completed).</span></span>  
  
<span data-ttu-id="7a9f2-135">Ný úthlutunarfærsla sem inniheldur nýja forðann er stofnuð og fær stöðuna **Virk**.</span><span class="sxs-lookup"><span data-stu-id="7a9f2-135">A new allocation entry that contains the new resource is created that has the status **Active**.</span></span>  
  
## <a name="reallocating-a-service-item"></a><span data-ttu-id="7a9f2-136">Endurúthlutun þjónustuvöru</span><span class="sxs-lookup"><span data-stu-id="7a9f2-136">Reallocating a Service Item</span></span>  
<span data-ttu-id="7a9f2-137">Þegar þjónustuvöru er endurúthlutað í úthlutunarfærslu sem er með stöðuna **Þarf að endurúthluta** er úthlutunarfærslan uppfærð sem hér segir:</span><span class="sxs-lookup"><span data-stu-id="7a9f2-137">When you reallocate a service item in an allocation entry that has the status **Reallocation Needed**, the allocation entry is updated in the following ways:</span></span>  
  
* <span data-ttu-id="7a9f2-138">Hafi þjónustan hafist þegar úthlutun var **Virk** (hafi viðgerðarstaða þjónustuvörunnar í færslunni breyst í **Í vinnslu**) er úthlutunarstöðunni breytt úr **Þarf að endurúthluta** í **Lokið**.</span><span class="sxs-lookup"><span data-stu-id="7a9f2-138">If service was started when the allocation was **Active** (that is, if the repair status of the service item in the entry was changed to **In Process**), the allocation status is changed from **Reallocation Needed** to **Finished**.</span></span>  
* <span data-ttu-id="7a9f2-139">Hafi þjónusta ekki hafist þegar úthlutun var **Virk** er úthlutunarstöðu breytt úr **Þarf að endurúthluta** í **Hætt við**.</span><span class="sxs-lookup"><span data-stu-id="7a9f2-139">If service was not started when the allocation was **Active**, the allocation status is changed from **Reallocation Needed** to **Canceled**.</span></span>  
  
<span data-ttu-id="7a9f2-140">Ný úthlutunarfærsla sem inniheldur nýja forðann er stofnuð og fær stöðuna **Virk**.</span><span class="sxs-lookup"><span data-stu-id="7a9f2-140">A new allocation entry that contains the new resource is created that has the status **Active**.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7a9f2-141">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="7a9f2-141">See Also</span></span>  
[<span data-ttu-id="7a9f2-142">Setja upp forðaúthlutanir</span><span class="sxs-lookup"><span data-stu-id="7a9f2-142">Set Up Resource Allocations</span></span>](service-how-setup-resource-allocation.md)  
[<span data-ttu-id="7a9f2-143">Úthluta forða</span><span class="sxs-lookup"><span data-stu-id="7a9f2-143">Allocate Resources</span></span>](service-how-to-allocate-resources.md)  

