---
title: "Setja upp forðaúthlutun | Microsoft Docs"
description: "Lærðu hvernig kerfið getur hjálpað til við að tryggja að þú úthlutir þjónustu til einhvers sem hefur nauðsynlega eiginleika til veita hana."
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: resource, skill, service, zones
ms.date: 08/22/2017
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: b16ba9366aefc108f39667678fe8ab70ce421b83
ms.contentlocale: is-is
ms.lasthandoff: 01/30/2018

---

# <a name="set-up-resource-allocation"></a><span data-ttu-id="61703-103">Setja upp forðaúthlutun</span><span class="sxs-lookup"><span data-stu-id="61703-103">Set Up Resource Allocation</span></span>
<span data-ttu-id="61703-104">Til að tryggja að þjónustuverkhluti sé framkvæmdur svo vel sé, er mikilvægt að finna tilfang sem er hæft til starfans.</span><span class="sxs-lookup"><span data-stu-id="61703-104">To ensure that a service task is performed well, it's important to find a resource who is qualified to do the work.</span></span> <span data-ttu-id="61703-105">Þú getur sett upp [!INCLUDE[d365fin](includes/d365fin_md.md)] svo það sé auðvelt að úthluta verkinu til einhvers sem er hæfur til þess.</span><span class="sxs-lookup"><span data-stu-id="61703-105">You can set up [!INCLUDE[d365fin](includes/d365fin_md.md)] so that it's easy to allocate someone who has the right skills for the job.</span></span> <span data-ttu-id="61703-106">Í [!INCLUDE[d365fin](includes/d365fin_md.md)] er þetta nefnt _Forðaúthlutun_.</span><span class="sxs-lookup"><span data-stu-id="61703-106">In [!INCLUDE[d365fin](includes/d365fin_md.md)], we call this _resource allocation_.</span></span> <span data-ttu-id="61703-107">Hægt er að úthluta til tilfanga út frá hæfni þeirra, tiltækileika, eða hvort þau eru á sama þjónustusvæði og viðskiptamaðurinn.</span><span class="sxs-lookup"><span data-stu-id="61703-107">You can allocate resources based on their skill, availability, or whether they are in the same service zone as the customer.</span></span> 

<span data-ttu-id="61703-108">Til að  nota forðaúthlutun skal setja upp:</span><span class="sxs-lookup"><span data-stu-id="61703-108">To use resource allocation, you must set up:</span></span>  
  
* <span data-ttu-id="61703-109">Nauðsynlega hæfni til að gera við og viðhalda þjónustuvörum.</span><span class="sxs-lookup"><span data-stu-id="61703-109">The skills required to repair and maintain service items.</span></span> <span data-ttu-id="61703-110">Þú úthlutar þessum til þjónustuvara og tilfanga.</span><span class="sxs-lookup"><span data-stu-id="61703-110">You assign these to service items and resources.</span></span>  
* <span data-ttu-id="61703-111">Landfræðileg svæði, kölluð svæði, sem þú getur skilgreint fyrir þinn markað.</span><span class="sxs-lookup"><span data-stu-id="61703-111">Geographic regions, called zones, that you define for your market.</span></span> <span data-ttu-id="61703-112">Til dæmis austur, vestur, miðsvæðis og svo framvegis.</span><span class="sxs-lookup"><span data-stu-id="61703-112">For example, East, West, Central, and so on.</span></span> <span data-ttu-id="61703-113">Þú úthlutar þessum til viðskiptamanna og tilfanga.</span><span class="sxs-lookup"><span data-stu-id="61703-113">You assign these to customers and resources.</span></span>  
* <span data-ttu-id="61703-114">Hvort á að birta tilföng hæfni og svæði, og hvort á að birta viðvörun er einhver velur óhæft tilfang, eða tilfang sem er ekki á þjónustusvæði viðskiptamanns.</span><span class="sxs-lookup"><span data-stu-id="61703-114">Whether to display resource skills and zones, and whether to display a warning if someone chooses unqualified resource, or a resource that is not in the customer zone.</span></span>  

## <a name="to-set-up-skills"></a><span data-ttu-id="61703-115">Uppsetning á hæfni</span><span class="sxs-lookup"><span data-stu-id="61703-115">To set up skills</span></span>
1. <span data-ttu-id="61703-116">Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Hæfni** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="61703-116">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Skills**, and then choose the related link.</span></span>  
2. <span data-ttu-id="61703-117">Fyllið inn í reitina eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="61703-117">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-assign-skills-to-service-items-and-resources"></a><span data-ttu-id="61703-118">Úthluta hæfni til þjónustuvöru og tilfanga</span><span class="sxs-lookup"><span data-stu-id="61703-118">To assign skills to service items and resources</span></span>
1. <span data-ttu-id="61703-119">Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Þjónustuvörur** eða **Tilföng** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="61703-119">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Service Items** or **Resources**, and then choose the related link.</span></span>  
2. <span data-ttu-id="61703-120">Opna spjaldið fyrir þjónustuvöru eða tilfang og síðan velja eitt af eftirfarandi:</span><span class="sxs-lookup"><span data-stu-id="61703-120">Open the card for the service item or resource, and then choose one of the following:</span></span>  
  
    * <span data-ttu-id="61703-121">Fyrir þjónustuvöru, velja **Tilföng hæfni**.</span><span class="sxs-lookup"><span data-stu-id="61703-121">For service items, choose **Resource Skills**.</span></span>  
    * <span data-ttu-id="61703-122">Fyrir tilföng, velja **Hæfni**.</span><span class="sxs-lookup"><span data-stu-id="61703-122">For resources, choose **Skills**.</span></span>  

## <a name="to-set-up-zones"></a><span data-ttu-id="61703-123">Setja upp svæði</span><span class="sxs-lookup"><span data-stu-id="61703-123">To set up zones</span></span>
1. <span data-ttu-id="61703-124">Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Svæði** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="61703-124">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Zones**, and then choose the related link.</span></span>  
2. <span data-ttu-id="61703-125">Fyllið inn í reitina eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="61703-125">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-assign-zones-to-customers-and-resources"></a><span data-ttu-id="61703-126">Úthluta svæðum til viðskiptamanna og tilfanga</span><span class="sxs-lookup"><span data-stu-id="61703-126">To assign zones to customers and resources</span></span> 
1. <span data-ttu-id="61703-127">Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Viðskiptamenn** eða **Tilföng** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="61703-127">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Customers** or **Resources**, and then choose the related link.</span></span>  
2. <span data-ttu-id="61703-128">Opna spjaldið fyrir þjónustuvöru eða tilfang og síðan velja eitt af eftirfarandi:</span><span class="sxs-lookup"><span data-stu-id="61703-128">Open the card for the service item or resource, and then choose one of the following:</span></span>  
  
    * <span data-ttu-id="61703-129">Fyrir viðskiptamenn, velja svæði í **Þjónustusvæðiskóði** reitnum.</span><span class="sxs-lookup"><span data-stu-id="61703-129">For customers, choose a zone in the **Service Zone Code** field.</span></span>  
    * <span data-ttu-id="61703-130">Fyrir tilföng, velja **Þjónustusvæði** aðgerðina.</span><span class="sxs-lookup"><span data-stu-id="61703-130">For resources, choose the **Service Zones** action.</span></span>  

## <a name="to-specify-what-to-show-when-a-resource-is-chosen"></a><span data-ttu-id="61703-131">Tilgreina hvað á að sýna þegar tilfang er valið</span><span class="sxs-lookup"><span data-stu-id="61703-131">To specify what to show when a resource is chosen</span></span>
1. <span data-ttu-id="61703-132">Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Uppsetning þjónustu** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="61703-132">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Service Setup**, and then choose the related link.</span></span> 
2. <span data-ttu-id="61703-133">Í reitnum **Valkostir Tilföng hæfni** skal velja einn af valkostunum sem lýst er í eftirfarandi töflu.</span><span class="sxs-lookup"><span data-stu-id="61703-133">In the **Resource Skills Option** field, choose one of the options described in the following table.</span></span>  
  
    |<span data-ttu-id="61703-134">**Valkostur**</span><span class="sxs-lookup"><span data-stu-id="61703-134">**Option**</span></span>|<span data-ttu-id="61703-135">**Lýsing**</span><span class="sxs-lookup"><span data-stu-id="61703-135">**Description**</span></span>|  
    |------------|-------------|  
    |<span data-ttu-id="61703-136">Sýndur kóti</span><span class="sxs-lookup"><span data-stu-id="61703-136">Code Shown</span></span> | <span data-ttu-id="61703-137">Birtir eingöngu kóða.</span><span class="sxs-lookup"><span data-stu-id="61703-137">Displays the code only.</span></span>|  
    |<span data-ttu-id="61703-138">Sýnd viðvörun</span><span class="sxs-lookup"><span data-stu-id="61703-138">Warning Displayed</span></span> | <span data-ttu-id="61703-139">Sýnir upplýsingarnar og birtir viðvörun ef þú velur tilfang sem ekki er hæft.</span><span class="sxs-lookup"><span data-stu-id="61703-139">Shows the information and displays a warning if you choose a resource that is not qualified.</span></span>|  
    |<span data-ttu-id="61703-140">Ekki notað</span><span class="sxs-lookup"><span data-stu-id="61703-140">Not Used</span></span> | <span data-ttu-id="61703-141">Sýnir ekki þessar upplýsingar.</span><span class="sxs-lookup"><span data-stu-id="61703-141">Does not show this information.</span></span>|  

## <a name="to-update-resource-capacity"></a><span data-ttu-id="61703-142">Uppfæra Forðageta</span><span class="sxs-lookup"><span data-stu-id="61703-142">To update resource capacity</span></span>  
<span data-ttu-id="61703-143">Ef til vill þarf að breyta forðagetu.</span><span class="sxs-lookup"><span data-stu-id="61703-143">You may need to change the capacity of resources.</span></span>  
  
1. <span data-ttu-id="61703-144">Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Forðageta** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="61703-144">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Resource Capacity**, and then choose the related link.</span></span>  
2. <span data-ttu-id="61703-145">Veljið tilfang og velja svo aðgerðina **Stilla afkastageta**.</span><span class="sxs-lookup"><span data-stu-id="61703-145">Choose the resource, and then choose the **Set Capacity** action.</span></span>  
3. <span data-ttu-id="61703-146">Gera breytingar og velja svo **Uppfæra afkastagetu**.</span><span class="sxs-lookup"><span data-stu-id="61703-146">Make the changes, and then choose **Update Capacity**.</span></span>  

## <a name="to-update-skills-for-items-service-items-or-service-item-groups"></a><span data-ttu-id="61703-147">Uppfæra hæfni fyrir vörur, þjónustuvörur, eða þjónustuvöruflokka</span><span class="sxs-lookup"><span data-stu-id="61703-147">To update skills for items, service items, or service item groups</span></span>
<span data-ttu-id="61703-148">Ef þú vilt breyta hæfniskóðum sem vörum hefur verið úthlutað, til dæmis úr **PC** í **PCS**, geturðu gert það annað hvort fyrir vörur eða fyrir allar vörur í þjónustuvöruflokknum.</span><span class="sxs-lookup"><span data-stu-id="61703-148">If you want to change the skill codes assigned to items, for example from **PC** to **PCS**, you can do so either for an item, service item, or for all items in a service item group.</span></span>  
  
1. <span data-ttu-id="61703-149">Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Vörur** eða **Þjónustuvara**, eða **Þjónustuvöruflokkur** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="61703-149">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Items** or **Service Item**, or **Service Item Group**, and then choose the related link.</span></span>  
2. <span data-ttu-id="61703-150">Veljið tilfang og velja svo aðgerðina **Forðahæfni**.</span><span class="sxs-lookup"><span data-stu-id="61703-150">Choose the entity to update, and then choose the **Resource Skills** action.</span></span>  
3. <span data-ttu-id="61703-151">Í línunni með kótanum sem á að breyta, í reitnum **Hæfniskóti** skal velja viðeigandi hæfniskóta.</span><span class="sxs-lookup"><span data-stu-id="61703-151">On the line with the code to be changed, in the **Skill Code** field, choose the relevant skill code.</span></span>  
4.  <span data-ttu-id="61703-152">Ef þjónustuvörur tengjast vörunni opnast gluggi með eftirfarandi tveimur valkostum:</span><span class="sxs-lookup"><span data-stu-id="61703-152">If the item has associated service items, a dialog box opens with the following two options:</span></span>  
  
    * <span data-ttu-id="61703-153">Breyta sérþekkingarkótunum í valið gildi: þessi kostur er valinn ef skipta skal á gamla og nýja kótanum í öllum tengdum þjónustuvörum.</span><span class="sxs-lookup"><span data-stu-id="61703-153">Change the skill codes to the selected value: Select this option if you want to replace the old skill code with the new one on all the related service items.</span></span>  
    * <span data-ttu-id="61703-154">Eyða sérþekkingarkótunum eða uppfæra tengsl þeirra: Þessi kostur er valinn ef aðeins á að breyta sérþekkingarkótanum í þessari vöru.</span><span class="sxs-lookup"><span data-stu-id="61703-154">Delete the skill codes or update their relation: Select this option if you want to change the skill code on this item only.</span></span> <span data-ttu-id="61703-155">Sérþekkingarkótanum í tengdum þjónustuvörum verður endurúthlutað, það er, reiturinn **Úthlutað frá** verður uppfærður.</span><span class="sxs-lookup"><span data-stu-id="61703-155">The skill code on the related service items will be reassigned, that is, the **Assigned From** field will be updated.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="61703-156">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="61703-156">See Also</span></span>
[<span data-ttu-id="61703-157">Úthluta forða</span><span class="sxs-lookup"><span data-stu-id="61703-157">Allocate Resources</span></span>](service-how-to-allocate-resources.md)  
[<span data-ttu-id="61703-158">Setja upp vinnustundir og þjónustustundir</span><span class="sxs-lookup"><span data-stu-id="61703-158">Set Up Work Hours and Service Hours</span></span>](service-how-setup-work-service-hours.md)  
[<span data-ttu-id="61703-159">Setja upp bilanatilkynningar</span><span class="sxs-lookup"><span data-stu-id="61703-159">Set Up Fault Reporting</span></span>](service-how-setup-fault-reporting.md)  
[<span data-ttu-id="61703-160">Setja upp Kóta fyrir Staðlaða þjónustu</span><span class="sxs-lookup"><span data-stu-id="61703-160">Set Up Codes for Standard Services</span></span>](service-how-setup-service-coding.md)  
 


