---
title: "Hvernig á að setja upp vinnustundir og þjónustustundir | Microsoft Docs"
description: "Þú getur tilgreint venjulegan þjónustuvinnustundir í fyrirtækinu. Stuðst er við þessar þjónustustundir við útreikning á svardagsetningu og tíma vegna þjónustupantana og tilboða og til að senda viðvörunarboð vegna svartíma."
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
ms.openlocfilehash: 630875f80f4107522962c79734284569cbc2b6f7
ms.contentlocale: is-is
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-work-hours-and-service-hours"></a><span data-ttu-id="222e0-104">Setja upp vinnustundir og þjónustustundir</span><span class="sxs-lookup"><span data-stu-id="222e0-104">Set Up Work Hours and Service Hours</span></span>
<span data-ttu-id="222e0-105">Þjónustukerfi rekur yfirleitt forðastundir og stöðu þjónustupantana til að spá fyrir um vinnuálag og þjónustuþarfir.</span><span class="sxs-lookup"><span data-stu-id="222e0-105">Typically, a service management system tracks resource hours and service order status in order to forecast workloads and service needs.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="222e0-106"> er með innbyggð verkfæri sem hægt er að sérstilla til að skrá þessa gerð upplýsinga.</span><span class="sxs-lookup"><span data-stu-id="222e0-106"> has built-in tools that you can customize to record this kind of information.</span></span>  
  
<span data-ttu-id="222e0-107">Eftir að sjálfgefinn þjónustutími fyrirtækisins hefur verið stilltur er hægt að reikna út svartíma þjónustupantana eða senda út viðvaranir þegar þjónustusímtöl berast.</span><span class="sxs-lookup"><span data-stu-id="222e0-107">After you set the default service hours of your company, you can calculate response times for service orders or send warnings or alerts when service calls come in.</span></span> <span data-ttu-id="222e0-108">Viðvörunareiginleikinn er notaður samhliða verktímasetningu.</span><span class="sxs-lookup"><span data-stu-id="222e0-108">The alert feature is implemented together with the job scheduler.</span></span>   
  
<span data-ttu-id="222e0-109">Þegar þú vinnur að þjónustupöntun, muntu vilja uppfæra stöðu hennar svo þú getir fylgst með ferlinu.</span><span class="sxs-lookup"><span data-stu-id="222e0-109">As you work on a service order, you will want to update it's status so that you can monitor progress.</span></span> <span data-ttu-id="222e0-110">Þjónustupöntunarstaðan sýnir viðgerðarstöðu allra þjónustuvara í þjónustupöntuninni.</span><span class="sxs-lookup"><span data-stu-id="222e0-110">The service order status reflects the repair status of all the service items in the service order.</span></span> <span data-ttu-id="222e0-111">Frekari upplýsingar eru í [Skilja þjónustupöntun og viðgerðarstöðu](service-order-repair-status.md).</span><span class="sxs-lookup"><span data-stu-id="222e0-111">For more information, see [Understanding Service Order and Repair Status](service-order-repair-status.md).</span></span> 

## <a name="to-set-up-default-service-hours"></a><span data-ttu-id="222e0-112">Uppsetning sjálfgefinna þjónustustunda</span><span class="sxs-lookup"><span data-stu-id="222e0-112">To set up default service hours</span></span>  
<span data-ttu-id="222e0-113">Glugginn **Sjálfgefinn þjónustutími** er notaður til að setja upp venjulegan þjónustutíma í fyrirtækinu.</span><span class="sxs-lookup"><span data-stu-id="222e0-113">You use the **Default Service Hours** window to set up the usual service working hours in your company.</span></span> <span data-ttu-id="222e0-114">Stuðst er við þessar þjónustustundir við útreikning á svardagsetningu og tíma vegna þjónustupantana og tilboða og til að senda viðvörunarboð vegna svartíma.</span><span class="sxs-lookup"><span data-stu-id="222e0-114">These service hours are used to calculate the response date and time for service orders and quotes and to send response time warnings.</span></span> <span data-ttu-id="222e0-115">Kerfið notar sjálfgefinn þjónustutíma í þjónustusamninga nema sérstakar þjónustustundir séu tilgreindar vegna samnings.</span><span class="sxs-lookup"><span data-stu-id="222e0-115">The default service hours are used for service contracts unless you specify special service hours for a contract.</span></span>  
  
1. <span data-ttu-id="222e0-116">Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Sjálfgefnar þjónustustundir** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="222e0-116">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Default Service Hours**, and then choose the related link.</span></span>  
2. <span data-ttu-id="222e0-117">Fyllið inn í reitina eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="222e0-117">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
  
> [!IMPORTANT]  
>  <span data-ttu-id="222e0-118">Ef línurnar í glugganum **Sjálfgefinn þjónustutími** eru auðar eru 24 stundir sem sjálfgefið gildi sem gildir aðeins á virkum dögum.</span><span class="sxs-lookup"><span data-stu-id="222e0-118">If you leave the lines in the **Default Service Hours** window empty, the default value is 24 hours, valid only for calendar working days.</span></span>  
  
## <a name="to-set-up-work-hour-templates"></a><span data-ttu-id="222e0-119">Uppsetning vinnutímasniðmáta</span><span class="sxs-lookup"><span data-stu-id="222e0-119">To set up work-hour templates</span></span>
<span data-ttu-id="222e0-120">Nota má gluggann **Vinnutímasniðmát** til að setja upp sniðmát með dæmigerðum vinnustundum í fyrirtækinu.</span><span class="sxs-lookup"><span data-stu-id="222e0-120">You can use the **Work-Hour Template** window to set up templates that contain the typical working hours in your company.</span></span> <span data-ttu-id="222e0-121">Til dæmis má stofna sniðmát fyrir tæknimenn í fullu starfi og í hlutastarfi.</span><span class="sxs-lookup"><span data-stu-id="222e0-121">For example, you can create templates for full time technicians and part time technicians.</span></span> <span data-ttu-id="222e0-122">Vinnutímasniðmát má nota þegar getu er bætt við forða.</span><span class="sxs-lookup"><span data-stu-id="222e0-122">You can use work-hour templates when you add capacity to resources.</span></span>  
  
1. <span data-ttu-id="222e0-123">Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **vinnustundasniðmát** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="222e0-123">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Work Hour Templates**, and then choose the related link.</span></span>  
2. <span data-ttu-id="222e0-124">Fyllið inn í reitina eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="222e0-124">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
  
> [!Note]
> <span data-ttu-id="222e0-125">Eftir að þú færir inn vinnustundir fyrir hvern dag, er reiturinn **Heildarstundir á viku** reiknaður út sjálfkrafa.</span><span class="sxs-lookup"><span data-stu-id="222e0-125">After you enter work hours for each day, the value in the **Total per Week** field is calculated automatically.</span></span>  

## <a name="to-set-up-contract-specific-service-hours"></a><span data-ttu-id="222e0-126">Uppsetning samningsbundinna þjónustutíma</span><span class="sxs-lookup"><span data-stu-id="222e0-126">To set up contract specific service hours</span></span>  
<span data-ttu-id="222e0-127">Hægt er að nota gluggann **Þjónustutími** til að setja upp tiltekna þjónustutíma fyrir viðskiptamanninn sem á þjónustusamninginn.</span><span class="sxs-lookup"><span data-stu-id="222e0-127">You can use the **Service Hours** window to set up specific service hours for the customer that owns the service contract.</span></span> <span data-ttu-id="222e0-128">Kerfið styðst við þjónustutíma þegar það reiknar út svardagsetningu og svartíma vegna þjónustupantana og tilboða sem tilheyra þjónustusamningnum.</span><span class="sxs-lookup"><span data-stu-id="222e0-128">Service hours are used to calculate the response date and time for service orders and quotes that belong to the service contract.</span></span>  
  
<span data-ttu-id="222e0-129">Ef ekki eru tilgreindar sérstakar þjónustustundir vegna þjónustusamningsins er notaður sjálfgefinn þjónustutími vegna þjónustusamninga.</span><span class="sxs-lookup"><span data-stu-id="222e0-129">If you do not set up specific service hours for the service contract, the default service hours for service contracts are used.</span></span>  
  
1. <span data-ttu-id="222e0-130">Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Þjónustusamningar** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="222e0-130">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Service Contracts**, and then choose the related link.</span></span>  
2. <span data-ttu-id="222e0-131">Opna skal þjónustusamning sem setja á upp sérststakar þjónustustundir fyrir og veldu **Þjónustustundir**.</span><span class="sxs-lookup"><span data-stu-id="222e0-131">Open the service contract you want to set up specific service hours for, and choose **Service Hours**.</span></span>  
4. <span data-ttu-id="222e0-132">Ef setja á upp þjónustustundir sem byggjast á sjálfgefnum þjónustutíma er smellt á **Afrita sjálfgefinn þjónustutíma** aðgerðina.</span><span class="sxs-lookup"><span data-stu-id="222e0-132">To set up service hours based on default service hours, choose the **Copy Default Service Hours** action.</span></span>  
5. <span data-ttu-id="222e0-133">Breyta reitunum í þjónustutímafærslunum.</span><span class="sxs-lookup"><span data-stu-id="222e0-133">Edit the fields in the service hours entries.</span></span> <span data-ttu-id="222e0-134">Bæta við eða eyða færslum til að setja upp þjónustustundafjölda fyrir samninginn.</span><span class="sxs-lookup"><span data-stu-id="222e0-134">Insert or delete entries to set up the service hours for the contract.</span></span> <span data-ttu-id="222e0-135">Athugið að reitirnir **Dagur**, **Upphafstími** og **Lokatími** eru nauðsynlegir fyrir hverja línu.</span><span class="sxs-lookup"><span data-stu-id="222e0-135">Note that the fields **Day**, **Starting Time** and **Ending Time** are required for each line.</span></span>  
6. <span data-ttu-id="222e0-136">Ef þjónustutíminn á að gilda frá tiltekinni dagsetningu þarf að fylla út reitinn **Upphafsdagsetning**.</span><span class="sxs-lookup"><span data-stu-id="222e0-136">If you want the service hours to be valid from a specific date, fill in the **Starting Date** field.</span></span>  
7. <span data-ttu-id="222e0-137">Ef þjónustutíminn á að gilda á frídögum er merkt í gátreitinn í reitnum **Gildir á frídögum**.</span><span class="sxs-lookup"><span data-stu-id="222e0-137">If you want the service hours to be valid on holidays, select the check box in the **Valid on Holidays** field.</span></span>  

## <a name="see-also"></a><span data-ttu-id="222e0-138">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="222e0-138">See Also</span></span>  
[<span data-ttu-id="222e0-139">Skilja úthlutunarstaða og viðgerðarstaða</span><span class="sxs-lookup"><span data-stu-id="222e0-139">Understanding Allocation Status and Repair Status</span></span>](service-allocation-status-and-repair-status.md)  
[<span data-ttu-id="222e0-140">Þjónustustýring sett upp</span><span class="sxs-lookup"><span data-stu-id="222e0-140">Setting Up Service Management</span></span>](service-setup-service.md)  
<span data-ttu-id="222e0-141">[Skilja þjónustupöntun og viðgerðarstöðu](service-order-repair-status.md).</span><span class="sxs-lookup"><span data-stu-id="222e0-141">[Understanding Service Order and Repair Status](service-order-repair-status.md)</span></span>  

