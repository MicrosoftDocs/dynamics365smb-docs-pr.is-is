---
title: "Yfirlit yfir uppsetningar fyrir þjónustuvörur og þjónustuvörueiningar | Microsoft Docs"
description: "Lærðu um hluti sem þú verður að setja upp áður en þú getur notað þjónustuvörur, eins og sjálfgefin gildi á borð við svartíma, samningsafslátt í prósentum og þjónustuverðflokk."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 068d141ee8490cc34e8b2092b7dcfda36139660d
ms.contentlocale: is-is
ms.lasthandoff: 01/30/2018

---
# <a name="set-up-service-items-and-service-item-components"></a><span data-ttu-id="d806d-103">Setja upp þjónustuvörur og íhluti þjónustuvara</span><span class="sxs-lookup"><span data-stu-id="d806d-103">Set Up Service Items and Service Item Components</span></span>
<span data-ttu-id="d806d-104">Áður en þú vinnur með þjónustuvörur verður þú að setja upp eftirfarandi:</span><span class="sxs-lookup"><span data-stu-id="d806d-104">To work with service items, you must set up the following</span></span>

* <span data-ttu-id="d806d-105">Þjónustuvöruflokkar</span><span class="sxs-lookup"><span data-stu-id="d806d-105">Service item groups.</span></span> 
* <span data-ttu-id="d806d-106">Valfrjálst</span><span class="sxs-lookup"><span data-stu-id="d806d-106">Optional</span></span>

## <a name="to-set-up-service-item-groups"></a><span data-ttu-id="d806d-107">Setja upp þjónustuvöruflokka</span><span class="sxs-lookup"><span data-stu-id="d806d-107">To set up service item groups</span></span>
<span data-ttu-id="d806d-108">Þú getur setja upp þjónustuvöruflokka sem tengjast hvað varðar viðgerð og viðhaldi.</span><span class="sxs-lookup"><span data-stu-id="d806d-108">You can set up groups of items that are related in terms of repair and maintenance.</span></span> <span data-ttu-id="d806d-109">Skilgreina má sjálfgefin gildi vegna þjónustuvöru í þjónustuvöruflokki, t.d. svartíma, samningsafslátt í prósentum og þjónustuverðflokk.</span><span class="sxs-lookup"><span data-stu-id="d806d-109">You can define default values for service items in a service item group, such as response time, contract discount percent, and service price group.</span></span> <span data-ttu-id="d806d-110">Hægt er að ráða því hvort vara í þjónustuvöruflokki sé sjálfkrafa skráð sem þjónustuvara þegar hún er seld.</span><span class="sxs-lookup"><span data-stu-id="d806d-110">For items in a service item group, you can select whether you want them to be automatically registered as service items when they are sold.</span></span>  
  
<span data-ttu-id="d806d-111">Þjónustuvöruflokkum er úthlutað til vöru á **birgða** spjaldi og þjónustuvöru á **þjónustuvöru** spjaldi.</span><span class="sxs-lookup"><span data-stu-id="d806d-111">You assign service item groups to items on the **Item** card, and to service items on the **Service Item** card.</span></span>  
  
1. <span data-ttu-id="d806d-112">Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Þjónustuvöruflokkar** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="d806d-112">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Service Item Groups**, and then choose the related link.</span></span>  
2. <span data-ttu-id="d806d-113">Nýr þjónustuvöruflokkur er stofnaður.</span><span class="sxs-lookup"><span data-stu-id="d806d-113">Create a new service item group.</span></span>  
3. <span data-ttu-id="d806d-114">Fyllt er í reitina **Kóti** og **Lýsing**.</span><span class="sxs-lookup"><span data-stu-id="d806d-114">Fill in the **Code** and **Description** fields.</span></span>  
4. <span data-ttu-id="d806d-115">Í reitinn **Sjálfg. samningsafsláttar %** er færð inn sjálfgefin prósenta samningsafsláttar sem á að eiga við þjónustuvöruna í flokknum.</span><span class="sxs-lookup"><span data-stu-id="d806d-115">In the **Default Contract Discount %** field, enter the default contract discount percentage that you want the service items in the group to have.</span></span>  
5. <span data-ttu-id="d806d-116">Í reitinn **Kóti sjálfg. Þjónustuverðfl.** er færður inn kóti sjálfgefins þjónustuverðflokks sem á að eiga við þjónustuvöruna í flokknum.</span><span class="sxs-lookup"><span data-stu-id="d806d-116">In the **Default Serv. Price Group Code** field, enter the default service price group code that you want the service items in the group to have.</span></span>  
6. <span data-ttu-id="d806d-117">Í reitinn **Sjálfgefinn svartími (klst.)** er færður inn sjálfgefinn svartími í klukkustundum sem á að gilda um þjónustuvöruna í flokknum.</span><span class="sxs-lookup"><span data-stu-id="d806d-117">In the **Default Response Time (Hours)** field, enter the default response time in hours that you want the service items in the group to have.</span></span>  
7. <span data-ttu-id="d806d-118">Ef skrá á vöru í flokknum sem þjónustuvöru þegar hún er seld þarf að velja reitinn **Stofna þjónustuvöru**.</span><span class="sxs-lookup"><span data-stu-id="d806d-118">If you want to register the items in the group as service items when they are sold, select the **Create Service Item** field.</span></span>  

## <a name="to-set-up-service-item-components"></a><span data-ttu-id="d806d-119">Uppsetning þjónustuvöruíhluta</span><span class="sxs-lookup"><span data-stu-id="d806d-119">To set up service item components</span></span>
<span data-ttu-id="d806d-120">Í þjónustuvöru geta verið margir íhlutir sem skipta má út með varahlutum þegar varan er í þjónustu.</span><span class="sxs-lookup"><span data-stu-id="d806d-120">A service item can consist of several components, which can be replaced with spare parts when the item is serviced.</span></span> <span data-ttu-id="d806d-121">Þessir íhlutir eru uppsettir í síðunni **Þjónustuvara íhlutalisti**.</span><span class="sxs-lookup"><span data-stu-id="d806d-121">These components are set up on the **Service Item Component List** page.</span></span> <span data-ttu-id="d806d-122">Ef setja á upp íhluta vegna þjónustuvöru sem er uppskrift er hægt að afrita uppskriftarvöruna og stofna hana sem íhluti þjónustuvöru.</span><span class="sxs-lookup"><span data-stu-id="d806d-122">Additionally, if you want to set up components for service items that are BOMs, you can copy the BOM items and create them as service item components.</span></span> 
  
1. <span data-ttu-id="d806d-123">Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Þjónustuvörur** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="d806d-123">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Service Items**, and then choose the related link.</span></span> 
2. <span data-ttu-id="d806d-124">Opna skal þjónustuvöruna sem á að setja upp íhluti fyrir.</span><span class="sxs-lookup"><span data-stu-id="d806d-124">Open the service item for which you want to set up components.</span></span>  
3. <span data-ttu-id="d806d-125">Velja aðgerðina **Íhlutir**.</span><span class="sxs-lookup"><span data-stu-id="d806d-125">Choose the **Components** action.</span></span> <span data-ttu-id="d806d-126">Glugginn **Þjónustuvöruíhlutalisti** opnast.</span><span class="sxs-lookup"><span data-stu-id="d806d-126">The **Service Item Component List** window opens.</span></span>  
4. <span data-ttu-id="d806d-127">Bæta við nýjum íhlut.</span><span class="sxs-lookup"><span data-stu-id="d806d-127">Add a new component.</span></span>  
5. <span data-ttu-id="d806d-128">Í reitnum **Tegund** skal velja **Þjónustuvara** ef íhluturinn sjálfur er skráð þjónustuvara.</span><span class="sxs-lookup"><span data-stu-id="d806d-128">In the **Type** field, choose **Service Item** if the component itself is a registered service item.</span></span> <span data-ttu-id="d806d-129">Að öðrum kosti skal velja **Vara**.</span><span class="sxs-lookup"><span data-stu-id="d806d-129">Otherwise, select **Item**.</span></span>  
6. <span data-ttu-id="d806d-130">Í reitnum **númer**</span><span class="sxs-lookup"><span data-stu-id="d806d-130">In the **No.**</span></span> <span data-ttu-id="d806d-131">skal velja vöruna eða þjónustuvöruna sem er íhlutur þjónustuvörunnar.</span><span class="sxs-lookup"><span data-stu-id="d806d-131">field, choose the item or service item that is a component of the service item.</span></span>  

## <a name="to-set-up-service-item-components-from-a-bom"></a><span data-ttu-id="d806d-132">Uppsetning þjónustuvöruíhluta út frá uppskriftum</span><span class="sxs-lookup"><span data-stu-id="d806d-132">To set up service item components from a BOM</span></span>
1.  <span data-ttu-id="d806d-133">Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Þjónustuvörur** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="d806d-133">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Service Items**, and then choose the related link.</span></span>  
2. <span data-ttu-id="d806d-134">Opna skal þjónustuvöruna sem setja á upp íhluti út frá uppskrift fyrir.</span><span class="sxs-lookup"><span data-stu-id="d806d-134">Open the service item for which you want to set up components from a BOM.</span></span>  
3. <span data-ttu-id="d806d-135">Velja aðgerðina **Íhlutir**.</span><span class="sxs-lookup"><span data-stu-id="d806d-135">Choose the **Components** action.</span></span> <span data-ttu-id="d806d-136">Glugginn **Þjónustuvöruíhlutalisti** opnast.</span><span class="sxs-lookup"><span data-stu-id="d806d-136">The **Service Item Component List** window opens.</span></span>  
4. <span data-ttu-id="d806d-137">Valið er **Afrita úr uppskrift** aðgerð.</span><span class="sxs-lookup"><span data-stu-id="d806d-137">Choose the **Copy from BOM** action.</span></span>  
  
    <span data-ttu-id="d806d-138">Ef varan sem þjónustuvaran tengist er uppskrift stofnuð sjálfkrafa fyrir íhluti fyrir alla vöru í uppskriftinni.</span><span class="sxs-lookup"><span data-stu-id="d806d-138">If the item that the service item is linked to is a BOM, the components for all the items in the BOM are created automatically.</span></span>  

## <a name="to-set-up-a-service-shelf"></a><span data-ttu-id="d806d-139">Uppsetning þjónustuhillu</span><span class="sxs-lookup"><span data-stu-id="d806d-139">To set up a service shelf</span></span>
<span data-ttu-id="d806d-140">Þú getur sett upp þjónustuhillur sem tilgreina hvar þú geymir þjónustuvörur þínar.</span><span class="sxs-lookup"><span data-stu-id="d806d-140">You can set up service shelves that identify where you store your service items.</span></span> <span data-ttu-id="d806d-141">Þjónustuhillum er úthlutað til þjónustuvöru í síðunum **Þjónustupöntun** og **Þjónustuvörublað**.</span><span class="sxs-lookup"><span data-stu-id="d806d-141">You assign service shelves to service items on the **Service Order** and **Service Item Worksheet** pages.</span></span>  
  
1. <span data-ttu-id="d806d-142">Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Þjónustuhillur** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="d806d-142">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Service Shelves**, and then choose the related link.</span></span>
2. <span data-ttu-id="d806d-143">Fyllið inn í reitina eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="d806d-143">Fill in the fields as necessary.</span></span>

## <a name="see-also"></a><span data-ttu-id="d806d-144">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="d806d-144">See Also</span></span>
<span data-ttu-id="d806d-145">[Setja upp Kóta fyrir Staðlaða þjónustu](service-how-setup-service-coding.md) </span><span class="sxs-lookup"><span data-stu-id="d806d-145">[Set Up Codes for Standard Services](service-how-setup-service-coding.md) </span></span>  
[<span data-ttu-id="d806d-146">Setja upp úrræðaleit</span><span class="sxs-lookup"><span data-stu-id="d806d-146">Set Up Troubleshooting</span></span>](service-how-setup-troubleshooting.md)
