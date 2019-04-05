---
title: Setja upp forðaúthlutun | Microsoft Docs
description: Lærðu hvernig kerfið getur hjálpað til við að tryggja að þú úthlutir þjónustu til einhvers sem hefur nauðsynlega eiginleika til veita hana.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: resource, skill, service, zones
ms.date: 10/01/2018
ms.author: bholtorf
ms.openlocfilehash: 7ce128aa32d650cf756117ab46987167d9a3781a
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/08/2019
ms.locfileid: "799581"
---
# <a name="set-up-resource-allocation"></a><span data-ttu-id="328c2-103">Setja upp forðaúthlutun</span><span class="sxs-lookup"><span data-stu-id="328c2-103">Set Up Resource Allocation</span></span>
<span data-ttu-id="328c2-104">Til að tryggja að þjónustuverkhluti sé framkvæmdur svo vel sé, er mikilvægt að finna tilfang sem er hæft til starfans.</span><span class="sxs-lookup"><span data-stu-id="328c2-104">To ensure that a service task is performed well, it's important to find a resource who is qualified to do the work.</span></span> <span data-ttu-id="328c2-105">Þú getur sett upp [!INCLUDE[d365fin](includes/d365fin_md.md)] svo það sé auðvelt að úthluta verkinu til einhvers sem er hæfur til þess.</span><span class="sxs-lookup"><span data-stu-id="328c2-105">You can set up [!INCLUDE[d365fin](includes/d365fin_md.md)] so that it's easy to allocate someone who has the right skills for the job.</span></span> <span data-ttu-id="328c2-106">Í [!INCLUDE[d365fin](includes/d365fin_md.md)] er þetta nefnt _Forðaúthlutun_.</span><span class="sxs-lookup"><span data-stu-id="328c2-106">In [!INCLUDE[d365fin](includes/d365fin_md.md)], we call this _resource allocation_.</span></span> <span data-ttu-id="328c2-107">Hægt er að úthluta til tilfanga út frá hæfni þeirra, tiltækileika, eða hvort þau eru á sama þjónustusvæði og viðskiptamaðurinn.</span><span class="sxs-lookup"><span data-stu-id="328c2-107">You can allocate resources based on their skill, availability, or whether they are in the same service zone as the customer.</span></span> 

<span data-ttu-id="328c2-108">Til að  nota forðaúthlutun skal setja upp:</span><span class="sxs-lookup"><span data-stu-id="328c2-108">To use resource allocation, you must set up:</span></span>  
  
* <span data-ttu-id="328c2-109">Nauðsynlega hæfni til að gera við og viðhalda þjónustuvörum.</span><span class="sxs-lookup"><span data-stu-id="328c2-109">The skills required to repair and maintain service items.</span></span> <span data-ttu-id="328c2-110">Þú úthlutar þessum til þjónustuvara og tilfanga.</span><span class="sxs-lookup"><span data-stu-id="328c2-110">You assign these to service items and resources.</span></span>  
* <span data-ttu-id="328c2-111">Landfræðileg svæði, kölluð svæði, sem þú getur skilgreint fyrir þinn markað.</span><span class="sxs-lookup"><span data-stu-id="328c2-111">Geographic regions, called zones, that you define for your market.</span></span> <span data-ttu-id="328c2-112">Til dæmis austur, vestur, miðsvæðis og svo framvegis.</span><span class="sxs-lookup"><span data-stu-id="328c2-112">For example, East, West, Central, and so on.</span></span> <span data-ttu-id="328c2-113">Þú úthlutar þessum til viðskiptamanna og tilfanga.</span><span class="sxs-lookup"><span data-stu-id="328c2-113">You assign these to customers and resources.</span></span>  
* <span data-ttu-id="328c2-114">Hvort á að birta tilföng hæfni og svæði, og hvort á að birta viðvörun er einhver velur óhæft tilfang, eða tilfang sem er ekki á þjónustusvæði viðskiptamanns.</span><span class="sxs-lookup"><span data-stu-id="328c2-114">Whether to display resource skills and zones, and whether to display a warning if someone chooses unqualified resource, or a resource that is not in the customer zone.</span></span>  

## <a name="to-set-up-skills"></a><span data-ttu-id="328c2-115">Uppsetning á hæfni</span><span class="sxs-lookup"><span data-stu-id="328c2-115">To set up skills</span></span>
1. <span data-ttu-id="328c2-116">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Hæfni** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="328c2-116">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Skills**, and then choose the related link.</span></span>  
2. <span data-ttu-id="328c2-117">Fyllið inn í reitina eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="328c2-117">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-assign-skills-to-service-items-and-resources"></a><span data-ttu-id="328c2-118">Úthluta hæfni til þjónustuvöru og tilfanga</span><span class="sxs-lookup"><span data-stu-id="328c2-118">To assign skills to service items and resources</span></span>
1. <span data-ttu-id="328c2-119">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Þjónustuvara** eða **Tilföng** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="328c2-119">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Service Items** or **Resources**, and then choose the related link.</span></span>  
2. <span data-ttu-id="328c2-120">Opna spjaldið fyrir þjónustuvöru eða tilfang og síðan velja eitt af eftirfarandi:</span><span class="sxs-lookup"><span data-stu-id="328c2-120">Open the card for the service item or resource, and then choose one of the following:</span></span>  
  
    * <span data-ttu-id="328c2-121">Fyrir þjónustuvöru, velja **Tilföng hæfni**.</span><span class="sxs-lookup"><span data-stu-id="328c2-121">For service items, choose **Resource Skills**.</span></span>  
    * <span data-ttu-id="328c2-122">Fyrir tilföng, velja **Hæfni**.</span><span class="sxs-lookup"><span data-stu-id="328c2-122">For resources, choose **Skills**.</span></span>  

## <a name="to-set-up-zones"></a><span data-ttu-id="328c2-123">Setja upp svæði</span><span class="sxs-lookup"><span data-stu-id="328c2-123">To set up zones</span></span>
1. <span data-ttu-id="328c2-124">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Svæði** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="328c2-124">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Zones**, and then choose the related link.</span></span>  
2. <span data-ttu-id="328c2-125">Fyllið inn í reitina eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="328c2-125">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-assign-zones-to-customers-and-resources"></a><span data-ttu-id="328c2-126">Úthluta svæðum til viðskiptamanna og tilfanga</span><span class="sxs-lookup"><span data-stu-id="328c2-126">To assign zones to customers and resources</span></span> 
1. <span data-ttu-id="328c2-127">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **viðskiptamenn** eða **Tilföng** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="328c2-127">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Customers** or **Resources**, and then choose the related link.</span></span>  
2. <span data-ttu-id="328c2-128">Opna spjaldið fyrir þjónustuvöru eða tilfang og síðan velja eitt af eftirfarandi:</span><span class="sxs-lookup"><span data-stu-id="328c2-128">Open the card for the service item or resource, and then choose one of the following:</span></span>  
  
    * <span data-ttu-id="328c2-129">Fyrir viðskiptamenn, velja svæði í **Þjónustusvæðiskóði** reitnum.</span><span class="sxs-lookup"><span data-stu-id="328c2-129">For customers, choose a zone in the **Service Zone Code** field.</span></span>  
    * <span data-ttu-id="328c2-130">Fyrir tilföng, velja **Þjónustusvæði** aðgerðina.</span><span class="sxs-lookup"><span data-stu-id="328c2-130">For resources, choose the **Service Zones** action.</span></span>  

## <a name="to-specify-what-to-show-when-a-resource-is-chosen"></a><span data-ttu-id="328c2-131">Tilgreina hvað á að sýna þegar tilfang er valið</span><span class="sxs-lookup"><span data-stu-id="328c2-131">To specify what to show when a resource is chosen</span></span>
1. <span data-ttu-id="328c2-132">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Uppsetning þjónustu** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="328c2-132">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Service Setup**, and then choose the related link.</span></span> 
2. <span data-ttu-id="328c2-133">Í reitnum **Valkostir Tilföng hæfni** skal velja einn af valkostunum sem lýst er í eftirfarandi töflu.</span><span class="sxs-lookup"><span data-stu-id="328c2-133">In the **Resource Skills Option** field, choose one of the options described in the following table.</span></span>  
  
    |<span data-ttu-id="328c2-134">**Valkostur**</span><span class="sxs-lookup"><span data-stu-id="328c2-134">**Option**</span></span>|<span data-ttu-id="328c2-135">**Lýsing**</span><span class="sxs-lookup"><span data-stu-id="328c2-135">**Description**</span></span>|  
    |------------|-------------|  
    |<span data-ttu-id="328c2-136">Sýndur kóti</span><span class="sxs-lookup"><span data-stu-id="328c2-136">Code Shown</span></span> | <span data-ttu-id="328c2-137">Birtir eingöngu kóða.</span><span class="sxs-lookup"><span data-stu-id="328c2-137">Displays the code only.</span></span>|  
    |<span data-ttu-id="328c2-138">Sýnd viðvörun</span><span class="sxs-lookup"><span data-stu-id="328c2-138">Warning Displayed</span></span> | <span data-ttu-id="328c2-139">Sýnir upplýsingarnar og birtir viðvörun ef þú velur tilfang sem ekki er hæft.</span><span class="sxs-lookup"><span data-stu-id="328c2-139">Shows the information and displays a warning if you choose a resource that is not qualified.</span></span>|  
    |<span data-ttu-id="328c2-140">Ekki notað</span><span class="sxs-lookup"><span data-stu-id="328c2-140">Not Used</span></span> | <span data-ttu-id="328c2-141">Sýnir ekki þessar upplýsingar.</span><span class="sxs-lookup"><span data-stu-id="328c2-141">Does not show this information.</span></span>|  

## <a name="to-update-resource-capacity"></a><span data-ttu-id="328c2-142">Uppfæra Forðageta</span><span class="sxs-lookup"><span data-stu-id="328c2-142">To update resource capacity</span></span>  
<span data-ttu-id="328c2-143">Ef til vill þarf að breyta forðagetu.</span><span class="sxs-lookup"><span data-stu-id="328c2-143">You may need to change the capacity of resources.</span></span>  
  
1. <span data-ttu-id="328c2-144">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Afkastaveita tilfanga** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="328c2-144">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Resource Capacity**, and then choose the related link.</span></span>  
2. <span data-ttu-id="328c2-145">Veljið tilfang og velja svo aðgerðina **Stilla afkastageta**.</span><span class="sxs-lookup"><span data-stu-id="328c2-145">Choose the resource, and then choose the **Set Capacity** action.</span></span>  
3. <span data-ttu-id="328c2-146">Gera breytingar og velja svo **Uppfæra afkastagetu**.</span><span class="sxs-lookup"><span data-stu-id="328c2-146">Make the changes, and then choose **Update Capacity**.</span></span>  

## <a name="to-update-skills-for-items-service-items-or-service-item-groups"></a><span data-ttu-id="328c2-147">Uppfæra hæfni fyrir vörur, þjónustuvörur, eða þjónustuvöruflokka</span><span class="sxs-lookup"><span data-stu-id="328c2-147">To update skills for items, service items, or service item groups</span></span>
<span data-ttu-id="328c2-148">Ef þú vilt breyta hæfniskóðum sem vörum hefur verið úthlutað, til dæmis úr **PC** í **PCS**, geturðu gert það annað hvort fyrir vörur eða fyrir allar vörur í þjónustuvöruflokknum.</span><span class="sxs-lookup"><span data-stu-id="328c2-148">If you want to change the skill codes assigned to items, for example from **PC** to **PCS**, you can do so either for an item, service item, or for all items in a service item group.</span></span>  
  
1. <span data-ttu-id="328c2-149">Veldu ![Ljósaperu sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Vörur** eða **Þjónustuvörur** eða **Þjónustuvöruflokkar** og veldu síðan tengda hlekkinn.</span><span class="sxs-lookup"><span data-stu-id="328c2-149">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items** or **Service Item**, or **Service Item Group**, and then choose the related link.</span></span>  
2. <span data-ttu-id="328c2-150">Veljið tilfang og velja svo aðgerðina **Forðahæfni**.</span><span class="sxs-lookup"><span data-stu-id="328c2-150">Choose the entity to update, and then choose the **Resource Skills** action.</span></span>  
3. <span data-ttu-id="328c2-151">Í línunni með kótanum sem á að breyta, í reitnum **Hæfniskóti** skal velja viðeigandi hæfniskóta.</span><span class="sxs-lookup"><span data-stu-id="328c2-151">On the line with the code to be changed, in the **Skill Code** field, choose the relevant skill code.</span></span>  
4.  <span data-ttu-id="328c2-152">Ef þjónustuvörur tengjast vörunni opnast gluggi með eftirfarandi tveimur valkostum:</span><span class="sxs-lookup"><span data-stu-id="328c2-152">If the item has associated service items, a dialog box opens with the following two options:</span></span>  
  
    * <span data-ttu-id="328c2-153">Breyta sérþekkingarkótunum í valið gildi: þessi kostur er valinn ef skipta skal á gamla og nýja kótanum í öllum tengdum þjónustuvörum.</span><span class="sxs-lookup"><span data-stu-id="328c2-153">Change the skill codes to the selected value: Select this option if you want to replace the old skill code with the new one on all the related service items.</span></span>  
    * <span data-ttu-id="328c2-154">Eyða sérþekkingarkótunum eða uppfæra tengsl þeirra: Þessi kostur er valinn ef aðeins á að breyta sérþekkingarkótanum í þessari vöru.</span><span class="sxs-lookup"><span data-stu-id="328c2-154">Delete the skill codes or update their relation: Select this option if you want to change the skill code on this item only.</span></span> <span data-ttu-id="328c2-155">Sérþekkingarkótanum í tengdum þjónustuvörum verður endurúthlutað, það er, reiturinn **Úthlutað frá** verður uppfærður.</span><span class="sxs-lookup"><span data-stu-id="328c2-155">The skill code on the related service items will be reassigned, that is, the **Assigned From** field will be updated.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="328c2-156">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="328c2-156">See Also</span></span>
[<span data-ttu-id="328c2-157">Úthluta forða</span><span class="sxs-lookup"><span data-stu-id="328c2-157">Allocate Resources</span></span>](service-how-to-allocate-resources.md)  
[<span data-ttu-id="328c2-158">Setja upp vinnustundir og þjónustustundir</span><span class="sxs-lookup"><span data-stu-id="328c2-158">Set Up Work Hours and Service Hours</span></span>](service-how-setup-work-service-hours.md)  
[<span data-ttu-id="328c2-159">Setja upp bilanatilkynningar</span><span class="sxs-lookup"><span data-stu-id="328c2-159">Set Up Fault Reporting</span></span>](service-how-setup-fault-reporting.md)  
[<span data-ttu-id="328c2-160">Setja upp Kóta fyrir Staðlaða þjónustu</span><span class="sxs-lookup"><span data-stu-id="328c2-160">Set Up Codes for Standard Services</span></span>](service-how-setup-service-coding.md)  
 

