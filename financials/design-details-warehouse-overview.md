---
title: "Hönnunarupplýsingar - vöruhús yfirlit | Microsoft Docs"
description: "Til að styðja við raunmeðhöndlun vara á svæði og hólfastigi, verða allar upplýsingar að rekja fyrir hverja færslu eða flutning í vöruhús. Þessu er stjórnað í töflunni **Vöruhúsafærsla**. Hver færsla er vistuð í birgðageymsluskrá."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/23/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: f5dc30ab398ae41ab8c36b6c207d2f48036cc98c
ms.contentlocale: is-is
ms.lasthandoff: 03/22/2018

---
# <a name="design-details-warehouse-overview"></a><span data-ttu-id="addde-105">Hönnunarupplýsingar yfirlit vöruhúss</span><span class="sxs-lookup"><span data-stu-id="addde-105">Design Details: Warehouse Overview</span></span>
<span data-ttu-id="addde-106">Til að styðja við raunmeðhöndlun vara á svæði og hólfastigi, verða allar upplýsingar að rekja fyrir hverja færslu eða flutning í vöruhús.</span><span class="sxs-lookup"><span data-stu-id="addde-106">To support the physical handling of items on the zone and bin level, all information must be traced for each transaction or movement in the warehouse.</span></span> <span data-ttu-id="addde-107">Þessu er stjórnað í töflunni **Vöruhúsafærsla**.</span><span class="sxs-lookup"><span data-stu-id="addde-107">This is managed in the **Warehouse Entry** table.</span></span> <span data-ttu-id="addde-108">Hver færsla er vistuð í birgðageymsluskrá.</span><span class="sxs-lookup"><span data-stu-id="addde-108">Each transaction is stored in a warehouse register.</span></span>  

<span data-ttu-id="addde-109">Warehouse skjöl og vörugeymsla dagbók eru notuð til að skrá atriði hreyfingar á lager.</span><span class="sxs-lookup"><span data-stu-id="addde-109">Warehouse documents and a warehouse journal are used to register item movements in the warehouse.</span></span> <span data-ttu-id="addde-110">Í hvert sinn sem vara í vöruhúsinu er færð, móttekin, gengið frá, tekin til, send eða leiðrétt eru vöruhúsafærslur skráðar til að vista raunupplýsingar um svæði, hólf og magn.</span><span class="sxs-lookup"><span data-stu-id="addde-110">Every time that an item in the warehouse is moved, received, put away, picked, shipped, or adjusted, warehouse entries are registered to store the physical information about zone, bin, and quantity.</span></span> <span data-ttu-id="addde-111">Nánari upplýsingar er að finna í [Hönnunarupplýsingar: vöruhúsaflæði inn](design-details-outbound-warehouse-flow.md).</span><span class="sxs-lookup"><span data-stu-id="addde-111">For more information, see [Design Details: Inbound Warehouse Flow](design-details-outbound-warehouse-flow.md).</span></span>  

<span data-ttu-id="addde-112">Taflan **Innihald hólfs** er notuð til að meðhöndla allar mismunandi víddir innihalds í hólfi fyrir hverja vöru, svo sem mælieiningu, hámarksmagn og lágmarksmagn.</span><span class="sxs-lookup"><span data-stu-id="addde-112">The **Bin Content** table is used to handle all the different dimensions of the contents of a bin per item, such as unit of measure, maximum quantity, and minimum quantity.</span></span> <span data-ttu-id="addde-113">Taflan **Innihald hólfs** inniheldur einnig flæðireiti vöruhúsafærslur, vöruhúsaleiðbeiningar og vöruhúsbókarlínur sem tryggja framboð á vöru eftir hólfi og að fljótt sé að reikna hólf fyrir vöru.</span><span class="sxs-lookup"><span data-stu-id="addde-113">The **Bin Content** table also contains flow fields to the warehouse entries, warehouse instructions, and warehouse journal lines, which ensures that the availability of an item per bin and a bin for an item can be calculated quickly.</span></span> <span data-ttu-id="addde-114">Nánari upplýsingar eru í [Upplýsingar um hönnun: Til ráðstöfunar í vöruhúsi](design-details-availability-in-the-warehouse.md).</span><span class="sxs-lookup"><span data-stu-id="addde-114">For more information, see [Design Details: Availability in the Warehouse](design-details-availability-in-the-warehouse.md).</span></span>  

<span data-ttu-id="addde-115">Þegar vörubókun verður utan vöruhúsaeiningarinnar ern otuð sjálfgefin jöfnunarhólf á hverja staðsetningu til að samstilla vöruhúsafærslur við birgðafærslur.</span><span class="sxs-lookup"><span data-stu-id="addde-115">When item postings occur outside the warehouse module, a default adjustment bin per location is used to synchronize warehouse entries with inventory entries.</span></span> <span data-ttu-id="addde-116">Við birgðir á lager í vöruhúsi, er munur milli reiknaðrar og talins magns skráð í leiðréttingarhólf og síðan færður sem leiðréttar færslur birgðahöfuðbókar.</span><span class="sxs-lookup"><span data-stu-id="addde-116">During physical inventory of the warehouse, any differences between the calculated and counted quantities are recorded in the adjustment bin and then posted as correcting item ledger entries.</span></span> <span data-ttu-id="addde-117">Nánari upplýsingar eru í [Upplýsingar um hönnun: Samþætting við birgðir](design-details-integration-with-inventory.md).</span><span class="sxs-lookup"><span data-stu-id="addde-117">For more information, see [Design Details: Integration with Inventory](design-details-integration-with-inventory.md).</span></span>  

<span data-ttu-id="addde-118">Eftirfarandi mynd lýsir dæmigerðu vöruhúsaflæði.</span><span class="sxs-lookup"><span data-stu-id="addde-118">The following illustration outlines typical warehouse flows.</span></span>  

<span data-ttu-id="addde-119">![Yfirlit yfir Vöruhúsaferli](media/design_details_warehouse_management_overview.png "hönnunarupplýsingar_yfirlit_vöruhúsastjórnun")</span><span class="sxs-lookup"><span data-stu-id="addde-119">![Overview of warehouse processes](media/design_details_warehouse_management_overview.png "design_details_warehouse_management_overview")</span></span>  

## <a name="basic-or-advanced-warehousing"></a><span data-ttu-id="addde-120">Grunn- eða ítarleg vörugeymsla</span><span class="sxs-lookup"><span data-stu-id="addde-120">Basic or Advanced Warehousing</span></span>  
<span data-ttu-id="addde-121">Vöruhúsavirkni í [!INCLUDE[d365fin](includes/d365fin_md.md)] má framkvæma í mismunandi flækjustigum, allt eftir ferlum fyrirtækisins og pöntunarmagni.</span><span class="sxs-lookup"><span data-stu-id="addde-121">Warehouse functionality in [!INCLUDE[d365fin](includes/d365fin_md.md)] can be implemented in different complexity levels, depending on a company’s processes and order volume.</span></span> <span data-ttu-id="addde-122">Aðalmunurinn er sá aðgerðir eru framkvæmdar pöntun fyrir pöntun í grunnvörugeymslu þegar þeim er steypt saman fyrir margfaldar pantanir í ítarlegu vöruhúsi.</span><span class="sxs-lookup"><span data-stu-id="addde-122">The main difference is that activities are performed order-by-order in basic warehousing when they are consolidated for multiple orders in advanced warehousing.</span></span>  

 <span data-ttu-id="addde-123">Til að greina á milli mismunandi flækjustiga, þessi gögn átt við tvö almenna hluti, grunn og ítarlegt vöruhús.</span><span class="sxs-lookup"><span data-stu-id="addde-123">To differentiate between the different complexity levels, this documentation refers to two general denominations, Basic and Advanced Warehousing.</span></span> <span data-ttu-id="addde-124">Þessi einfalda aðgreining nær yfir mörg mismunandi flækjustig samkvæmt skilgreiningu vörueinda og staðsetningaruppsetniingu, hvert og eitt stutta f mismunandi notandaviðmótsskjölum.</span><span class="sxs-lookup"><span data-stu-id="addde-124">This simple differentiation covers several different complexity levels as defined by product granules and location setup, each supported by different UI documents.</span></span> <span data-ttu-id="addde-125">Nánari upplýsingar eru í [Upplýsingar um hönnun: Uppsetning vöruhúss](design-details-warehouse-setup.md).</span><span class="sxs-lookup"><span data-stu-id="addde-125">For more information, see [Design Details: Warehouse Setup](design-details-warehouse-setup.md).</span></span>  

> [!NOTE]  
>  <span data-ttu-id="addde-126">Ítarlegasta stig vöruhúss er kallað uppsetningar vöruhúsakerfa í þessu skjali þar sem það stig krefst ítarlegast kornsins, vöruhúsakerfis.</span><span class="sxs-lookup"><span data-stu-id="addde-126">The most advanced level of warehousing is referred to as “WMS installations” in this documentation, since this level requires the most advanced granule, Warehouse Management Systems.</span></span>  

 <span data-ttu-id="addde-127">Eftirfarandi mismunandi notandaviðmótsskjöl eru notuð í grunngerð og ítarlegu vöruhúsi.</span><span class="sxs-lookup"><span data-stu-id="addde-127">The following different UI documents are used in basic and advanced warehousing.</span></span>  

## <a name="basic-ui-documents"></a><span data-ttu-id="addde-128">Grunnviðmótsskjöl</span><span class="sxs-lookup"><span data-stu-id="addde-128">Basic UI Documents</span></span>  

-   <span data-ttu-id="addde-129">**Birgðafrágangur**</span><span class="sxs-lookup"><span data-stu-id="addde-129">**Inventory Put-away**</span></span>  
-   <span data-ttu-id="addde-130">**Birgðatínsla**</span><span class="sxs-lookup"><span data-stu-id="addde-130">**Inventory Pick**</span></span>  
-   <span data-ttu-id="addde-131">**Birgðahreyfing**</span><span class="sxs-lookup"><span data-stu-id="addde-131">**Inventory Movement**</span></span>  
-   <span data-ttu-id="addde-132">**Birgðabók**</span><span class="sxs-lookup"><span data-stu-id="addde-132">**Item Journal**</span></span>  
-   <span data-ttu-id="addde-133">**Endurflokkunarbók vöru**</span><span class="sxs-lookup"><span data-stu-id="addde-133">**Item Reclassification Journal**</span></span>  
-   <span data-ttu-id="addde-134">(Ýmsar skýrslur)</span><span class="sxs-lookup"><span data-stu-id="addde-134">(Various reports)</span></span>  

## <a name="advanced-ui-documents"></a><span data-ttu-id="addde-135">Ítarleg notendaviðmótsskjöl</span><span class="sxs-lookup"><span data-stu-id="addde-135">Advanced UI Documents</span></span>  

-   <span data-ttu-id="addde-136">**Vöruhús -**</span><span class="sxs-lookup"><span data-stu-id="addde-136">**Warehouse Receipt**</span></span>  
-   <span data-ttu-id="addde-137">**Vinnublað frágangs**</span><span class="sxs-lookup"><span data-stu-id="addde-137">**Put-away Worksheet**</span></span>  
-   <span data-ttu-id="addde-138">**Frágangur vöruhúss**</span><span class="sxs-lookup"><span data-stu-id="addde-138">**Warehouse Put-away**</span></span>  
-   <span data-ttu-id="addde-139">**Vinnublað tínslu**</span><span class="sxs-lookup"><span data-stu-id="addde-139">**Pick Worksheet**</span></span>  
-   <span data-ttu-id="addde-140">**Vöruhúsatínsla**</span><span class="sxs-lookup"><span data-stu-id="addde-140">**Warehouse Pick**</span></span>  
-   <span data-ttu-id="addde-141">**Hreyfingavinnublað**</span><span class="sxs-lookup"><span data-stu-id="addde-141">**Movement Worksheet**</span></span>  
-   <span data-ttu-id="addde-142">**Vöruhúsatínsla**</span><span class="sxs-lookup"><span data-stu-id="addde-142">**Warehouse Movement**</span></span>  
-   <span data-ttu-id="addde-143">**Vöruhús - innanhústínsla**</span><span class="sxs-lookup"><span data-stu-id="addde-143">**Internal Whse. Pick**</span></span>  
-   <span data-ttu-id="addde-144">**Vöruhús - innanhúsfrágangur**</span><span class="sxs-lookup"><span data-stu-id="addde-144">**Internal Whse. Put-away**</span></span>  
-   <span data-ttu-id="addde-145">**Vinnublað hólfastofnunar**</span><span class="sxs-lookup"><span data-stu-id="addde-145">**Bin Creation Worksheet**</span></span>  
-   <span data-ttu-id="addde-146">**Vinnublað f. stofnun hólfainnihalds**</span><span class="sxs-lookup"><span data-stu-id="addde-146">**Bin Content Creation Worksheet**</span></span>  
-   <span data-ttu-id="addde-147">**Birgðabók vöruhúss**</span><span class="sxs-lookup"><span data-stu-id="addde-147">**Whse. Item Journal**</span></span>  
-   <span data-ttu-id="addde-148">**Birgðaendurfl.bók vöruhúss**</span><span class="sxs-lookup"><span data-stu-id="addde-148">**Whse. Item Reclass. Journal**</span></span>  
-   <span data-ttu-id="addde-149">(Ýmsar skýrslur)</span><span class="sxs-lookup"><span data-stu-id="addde-149">(Various reports)</span></span>  

<span data-ttu-id="addde-150">Nánari upplýsingar um hvert skjal eru í upplýsingum hvers glugga.</span><span class="sxs-lookup"><span data-stu-id="addde-150">For more information about each document, see the respective window topics.</span></span>  

### <a name="terminology"></a><span data-ttu-id="addde-151">Orðalisti</span><span class="sxs-lookup"><span data-stu-id="addde-151">Terminology</span></span>  
<span data-ttu-id="addde-152">Til að jafna við fjárhagshugtökin innkaup og sölu notast [!INCLUDE[d365fin](includes/d365fin_md.md)] vöruhúsaskjöl við eftirfarandi hugtök fyrir vöruflæði í vöruhúsinu.</span><span class="sxs-lookup"><span data-stu-id="addde-152">To align with the financial concepts of purchases and sales, [!INCLUDE[d365fin](includes/d365fin_md.md)] warehouse documentation refers to the following terms for item flow in the warehouse.</span></span>  

|<span data-ttu-id="addde-153">Hugtak</span><span class="sxs-lookup"><span data-stu-id="addde-153">Term</span></span>|<span data-ttu-id="addde-154">Description</span><span class="sxs-lookup"><span data-stu-id="addde-154">Description</span></span>|  
|----------|---------------------------------------|  
|<span data-ttu-id="addde-155">Flæði á innleið</span><span class="sxs-lookup"><span data-stu-id="addde-155">Inbound flow</span></span>|<span data-ttu-id="addde-156">Vörur á ferð innan vöruhúss, svo sem innkaup og millifærslur á innleið.</span><span class="sxs-lookup"><span data-stu-id="addde-156">Items moving into the warehouse location, such as purchases and inbound transfers.</span></span>|  
|<span data-ttu-id="addde-157">Tiltekt innanhúss</span><span class="sxs-lookup"><span data-stu-id="addde-157">Internal flow</span></span>|<span data-ttu-id="addde-158">Vörur á ferð innan vöruhúss, svo sem framleiðsluíhlutir og frálag.</span><span class="sxs-lookup"><span data-stu-id="addde-158">Items moving inside the warehouse location, such as production components and output.</span></span>|  
|<span data-ttu-id="addde-159">Flæði á útleið</span><span class="sxs-lookup"><span data-stu-id="addde-159">Outbound flow</span></span>|<span data-ttu-id="addde-160">Vörur á leið út úr vöruhúsi, svo sem sala eða millifærslur á útleið.</span><span class="sxs-lookup"><span data-stu-id="addde-160">Items moving out of the warehouse location, such as sales and outbound transfers.</span></span>|  

## <a name="see-also"></a><span data-ttu-id="addde-161">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="addde-161">See Also</span></span>  
 [<span data-ttu-id="addde-162">Hönnunarupplýsingar vöruhúsakerfi</span><span class="sxs-lookup"><span data-stu-id="addde-162">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)

