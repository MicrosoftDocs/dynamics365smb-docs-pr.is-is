---
title: Hönnunarupplýsingar - vöruhús yfirlit | Microsoft Docs
description: Til að styðja við raunmeðhöndlun vara á svæði og hólfastigi, verða allar upplýsingar að rekja fyrir hverja færslu eða flutning í vöruhús. Þessu er stjórnað í töflunni **Vöruhúsafærsla**. Hver færsla er vistuð í birgðageymsluskrá.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 1edf9c9f5b86a618e32820a261f1f9a4597b756a
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/01/2019
ms.locfileid: "2306653"
---
# <a name="design-details-warehouse-overview"></a><span data-ttu-id="99923-105">Hönnunarupplýsingar yfirlit vöruhúss</span><span class="sxs-lookup"><span data-stu-id="99923-105">Design Details: Warehouse Overview</span></span>
<span data-ttu-id="99923-106">Til að styðja við raunmeðhöndlun vara á svæði og hólfastigi, verða allar upplýsingar að rekja fyrir hverja færslu eða flutning í vöruhús.</span><span class="sxs-lookup"><span data-stu-id="99923-106">To support the physical handling of items on the zone and bin level, all information must be traced for each transaction or movement in the warehouse.</span></span> <span data-ttu-id="99923-107">Þessu er stjórnað í töflunni **Vöruhúsafærsla**.</span><span class="sxs-lookup"><span data-stu-id="99923-107">This is managed in the **Warehouse Entry** table.</span></span> <span data-ttu-id="99923-108">Hver færsla er vistuð í birgðageymsluskrá.</span><span class="sxs-lookup"><span data-stu-id="99923-108">Each transaction is stored in a warehouse register.</span></span>  

<span data-ttu-id="99923-109">Warehouse skjöl og vörugeymsla dagbók eru notuð til að skrá atriði hreyfingar á lager.</span><span class="sxs-lookup"><span data-stu-id="99923-109">Warehouse documents and a warehouse journal are used to register item movements in the warehouse.</span></span> <span data-ttu-id="99923-110">Í hvert sinn sem vara í vöruhúsinu er færð, móttekin, gengið frá, tekin til, send eða leiðrétt eru vöruhúsafærslur skráðar til að vista raunupplýsingar um svæði, hólf og magn.</span><span class="sxs-lookup"><span data-stu-id="99923-110">Every time that an item in the warehouse is moved, received, put away, picked, shipped, or adjusted, warehouse entries are registered to store the physical information about zone, bin, and quantity.</span></span>

<span data-ttu-id="99923-111">Taflan **Innihald hólfs** er notuð til að meðhöndla allar mismunandi víddir innihalds í hólfi fyrir hverja vöru, svo sem mælieiningu, hámarksmagn og lágmarksmagn.</span><span class="sxs-lookup"><span data-stu-id="99923-111">The **Bin Content** table is used to handle all the different dimensions of the contents of a bin per item, such as unit of measure, maximum quantity, and minimum quantity.</span></span> <span data-ttu-id="99923-112">Taflan **Innihald hólfs** inniheldur einnig flæðireiti vöruhúsafærslur, vöruhúsaleiðbeiningar og vöruhúsbókarlínur sem tryggja framboð á vöru eftir hólfi og að fljótt sé að reikna hólf fyrir vöru.</span><span class="sxs-lookup"><span data-stu-id="99923-112">The **Bin Content** table also contains flow fields to the warehouse entries, warehouse instructions, and warehouse journal lines, which ensures that the availability of an item per bin and a bin for an item can be calculated quickly.</span></span> <span data-ttu-id="99923-113">Nánari upplýsingar eru í [Upplýsingar um hönnun: Til ráðstöfunar í vöruhúsi](design-details-availability-in-the-warehouse.md).</span><span class="sxs-lookup"><span data-stu-id="99923-113">For more information, see [Design Details: Availability in the Warehouse](design-details-availability-in-the-warehouse.md).</span></span>  

<span data-ttu-id="99923-114">Þegar vörubókun verður utan vöruhúsaeiningarinnar ern otuð sjálfgefin jöfnunarhólf á hverja staðsetningu til að samstilla vöruhúsafærslur við birgðafærslur.</span><span class="sxs-lookup"><span data-stu-id="99923-114">When item postings occur outside the warehouse module, a default adjustment bin per location is used to synchronize warehouse entries with inventory entries.</span></span> <span data-ttu-id="99923-115">Við birgðir á lager í vöruhúsi, er munur milli reiknaðrar og talins magns skráð í leiðréttingarhólf og síðan færður sem leiðréttar færslur birgðahöfuðbókar.</span><span class="sxs-lookup"><span data-stu-id="99923-115">During physical inventory of the warehouse, any differences between the calculated and counted quantities are recorded in the adjustment bin and then posted as correcting item ledger entries.</span></span> <span data-ttu-id="99923-116">Nánari upplýsingar eru í [Upplýsingar um hönnun: Samþætting við birgðir](design-details-integration-with-inventory.md).</span><span class="sxs-lookup"><span data-stu-id="99923-116">For more information, see [Design Details: Integration with Inventory](design-details-integration-with-inventory.md).</span></span>  

<span data-ttu-id="99923-117">Eftirfarandi mynd lýsir dæmigerðu vöruhúsaflæði.</span><span class="sxs-lookup"><span data-stu-id="99923-117">The following illustration outlines typical warehouse flows.</span></span>  

<span data-ttu-id="99923-118">![Yfirlit yfir Vöruhúsaferli](media/design_details_warehouse_management_overview.png "Yfirlit yfir Vöruhúsaferli")</span><span class="sxs-lookup"><span data-stu-id="99923-118">![Overview of warehouse processes](media/design_details_warehouse_management_overview.png "Overview of warehouse processes")</span></span>  

## <a name="basic-or-advanced-warehousing"></a><span data-ttu-id="99923-119">Grunn- eða ítarleg vörugeymsla</span><span class="sxs-lookup"><span data-stu-id="99923-119">Basic or Advanced Warehousing</span></span>  
<span data-ttu-id="99923-120">Vöruhúsavirkni í [!INCLUDE[d365fin](includes/d365fin_md.md)] má framkvæma í mismunandi flækjustigum, allt eftir ferlum fyrirtækisins og pöntunarmagni.</span><span class="sxs-lookup"><span data-stu-id="99923-120">Warehouse functionality in [!INCLUDE[d365fin](includes/d365fin_md.md)] can be implemented in different complexity levels, depending on a company’s processes and order volume.</span></span> <span data-ttu-id="99923-121">Aðalmunurinn er sá aðgerðir eru framkvæmdar pöntun fyrir pöntun í grunnvörugeymslu þegar þeim er steypt saman fyrir margfaldar pantanir í ítarlegu vöruhúsi.</span><span class="sxs-lookup"><span data-stu-id="99923-121">The main difference is that activities are performed order-by-order in basic warehousing when they are consolidated for multiple orders in advanced warehousing.</span></span>  

 <span data-ttu-id="99923-122">Til að greina á milli mismunandi flækjustiga, þessi gögn átt við tvö almenna hluti, grunn og ítarlegt vöruhús.</span><span class="sxs-lookup"><span data-stu-id="99923-122">To differentiate between the different complexity levels, this documentation refers to two general denominations, Basic and Advanced Warehousing.</span></span> <span data-ttu-id="99923-123">Þessi einfalda aðgreining nær yfir mörg mismunandi flækjustig samkvæmt skilgreiningu vörueinda og staðsetningaruppsetniingu, hvert og eitt stutta f mismunandi notandaviðmótsskjölum.</span><span class="sxs-lookup"><span data-stu-id="99923-123">This simple differentiation covers several different complexity levels as defined by product granules and location setup, each supported by different UI documents.</span></span> <span data-ttu-id="99923-124">Nánari upplýsingar eru í [Upplýsingar um hönnun: Uppsetning vöruhúss](design-details-warehouse-setup.md).</span><span class="sxs-lookup"><span data-stu-id="99923-124">For more information, see [Design Details: Warehouse Setup](design-details-warehouse-setup.md).</span></span>  

> [!NOTE]  
>  <span data-ttu-id="99923-125">Ítarlegasta stig vöruhúss er kallað uppsetningar vöruhúsakerfa í þessu skjali þar sem það stig krefst ítarlegast kornsins, vöruhúsakerfis.</span><span class="sxs-lookup"><span data-stu-id="99923-125">The most advanced level of warehousing is referred to as “WMS installations” in this documentation, since this level requires the most advanced granule, Warehouse Management Systems.</span></span>  

 <span data-ttu-id="99923-126">Eftirfarandi mismunandi notandaviðmótsskjöl eru notuð í grunngerð og ítarlegu vöruhúsi.</span><span class="sxs-lookup"><span data-stu-id="99923-126">The following different UI documents are used in basic and advanced warehousing.</span></span>  

## <a name="basic-ui-documents"></a><span data-ttu-id="99923-127">Grunnviðmótsskjöl</span><span class="sxs-lookup"><span data-stu-id="99923-127">Basic UI Documents</span></span>  

-   <span data-ttu-id="99923-128">**Birgðafrágangur**</span><span class="sxs-lookup"><span data-stu-id="99923-128">**Inventory Put-away**</span></span>  
-   <span data-ttu-id="99923-129">**Birgðatínsla**</span><span class="sxs-lookup"><span data-stu-id="99923-129">**Inventory Pick**</span></span>  
-   <span data-ttu-id="99923-130">**Birgðahreyfing**</span><span class="sxs-lookup"><span data-stu-id="99923-130">**Inventory Movement**</span></span>  
-   <span data-ttu-id="99923-131">**Birgðabók**</span><span class="sxs-lookup"><span data-stu-id="99923-131">**Item Journal**</span></span>  
-   <span data-ttu-id="99923-132">**Endurflokkunarbók vöru**</span><span class="sxs-lookup"><span data-stu-id="99923-132">**Item Reclassification Journal**</span></span>  
-   <span data-ttu-id="99923-133">(Ýmsar skýrslur)</span><span class="sxs-lookup"><span data-stu-id="99923-133">(Various reports)</span></span>  

## <a name="advanced-ui-documents"></a><span data-ttu-id="99923-134">Ítarleg notendaviðmótsskjöl</span><span class="sxs-lookup"><span data-stu-id="99923-134">Advanced UI Documents</span></span>  

-   <span data-ttu-id="99923-135">**Vöruhús -**</span><span class="sxs-lookup"><span data-stu-id="99923-135">**Warehouse Receipt**</span></span>  
-   <span data-ttu-id="99923-136">**Vinnublað frágangs**</span><span class="sxs-lookup"><span data-stu-id="99923-136">**Put-away Worksheet**</span></span>  
-   <span data-ttu-id="99923-137">**Frágangur vöruhúss**</span><span class="sxs-lookup"><span data-stu-id="99923-137">**Warehouse Put-away**</span></span>  
-   <span data-ttu-id="99923-138">**Vinnublað tínslu**</span><span class="sxs-lookup"><span data-stu-id="99923-138">**Pick Worksheet**</span></span>  
-   <span data-ttu-id="99923-139">**Vöruhúsatínsla**</span><span class="sxs-lookup"><span data-stu-id="99923-139">**Warehouse Pick**</span></span>  
-   <span data-ttu-id="99923-140">**Hreyfingavinnublað**</span><span class="sxs-lookup"><span data-stu-id="99923-140">**Movement Worksheet**</span></span>  
-   <span data-ttu-id="99923-141">**Vöruhúsatínsla**</span><span class="sxs-lookup"><span data-stu-id="99923-141">**Warehouse Movement**</span></span>  
-   <span data-ttu-id="99923-142">**Vöruhús - innanhústínsla**</span><span class="sxs-lookup"><span data-stu-id="99923-142">**Internal Whse. Pick**</span></span>  
-   <span data-ttu-id="99923-143">**Vöruhús - innanhúsfrágangur**</span><span class="sxs-lookup"><span data-stu-id="99923-143">**Internal Whse. Put-away**</span></span>  
-   <span data-ttu-id="99923-144">**Vinnublað hólfastofnunar**</span><span class="sxs-lookup"><span data-stu-id="99923-144">**Bin Creation Worksheet**</span></span>  
-   <span data-ttu-id="99923-145">**Vinnublað f. stofnun hólfainnihalds**</span><span class="sxs-lookup"><span data-stu-id="99923-145">**Bin Content Creation Worksheet**</span></span>  
-   <span data-ttu-id="99923-146">**Birgðabók vöruhúss**</span><span class="sxs-lookup"><span data-stu-id="99923-146">**Whse. Item Journal**</span></span>  
-   <span data-ttu-id="99923-147">**Birgðaendurfl.bók vöruhúss**</span><span class="sxs-lookup"><span data-stu-id="99923-147">**Whse. Item Reclass. Journal**</span></span>  
-   <span data-ttu-id="99923-148">(Ýmsar skýrslur)</span><span class="sxs-lookup"><span data-stu-id="99923-148">(Various reports)</span></span>  

<span data-ttu-id="99923-149">Nánari upplýsingar um hvert skjal eru á síðum hvers kafla fyrir sig.</span><span class="sxs-lookup"><span data-stu-id="99923-149">For more information about each document, see the respective page topics.</span></span>  

### <a name="terminology"></a><span data-ttu-id="99923-150">Orðalisti</span><span class="sxs-lookup"><span data-stu-id="99923-150">Terminology</span></span>  
<span data-ttu-id="99923-151">Til að jafna við fjárhagshugtökin innkaup og sölu notast [!INCLUDE[d365fin](includes/d365fin_md.md)] vöruhúsaskjöl við eftirfarandi hugtök fyrir vöruflæði í vöruhúsinu.</span><span class="sxs-lookup"><span data-stu-id="99923-151">To align with the financial concepts of purchases and sales, [!INCLUDE[d365fin](includes/d365fin_md.md)] warehouse documentation refers to the following terms for item flow in the warehouse.</span></span>  

|<span data-ttu-id="99923-152">Hugtak</span><span class="sxs-lookup"><span data-stu-id="99923-152">Term</span></span>|<span data-ttu-id="99923-153">Description</span><span class="sxs-lookup"><span data-stu-id="99923-153">Description</span></span>|  
|----------|---------------------------------------|  
|<span data-ttu-id="99923-154">Flæði á innleið</span><span class="sxs-lookup"><span data-stu-id="99923-154">Inbound flow</span></span>|<span data-ttu-id="99923-155">Vörur á ferð innan vöruhúss, svo sem innkaup og millifærslur á innleið.</span><span class="sxs-lookup"><span data-stu-id="99923-155">Items moving into the warehouse location, such as purchases and inbound transfers.</span></span>|  
|<span data-ttu-id="99923-156">Tiltekt innanhúss</span><span class="sxs-lookup"><span data-stu-id="99923-156">Internal flow</span></span>|<span data-ttu-id="99923-157">Vörur á ferð innan vöruhúss, svo sem framleiðsluíhlutir og frálag.</span><span class="sxs-lookup"><span data-stu-id="99923-157">Items moving inside the warehouse location, such as production components and output.</span></span>|  
|<span data-ttu-id="99923-158">Flæði á útleið</span><span class="sxs-lookup"><span data-stu-id="99923-158">Outbound flow</span></span>|<span data-ttu-id="99923-159">Vörur á leið út úr vöruhúsi, svo sem sala eða millifærslur á útleið.</span><span class="sxs-lookup"><span data-stu-id="99923-159">Items moving out of the warehouse location, such as sales and outbound transfers.</span></span>|  

## <a name="see-also"></a><span data-ttu-id="99923-160">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="99923-160">See Also</span></span>  
 [<span data-ttu-id="99923-161">Hönnunarupplýsingar vöruhúsakerfi</span><span class="sxs-lookup"><span data-stu-id="99923-161">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)
