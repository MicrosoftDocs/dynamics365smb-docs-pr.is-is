---
title: "Hvernig á að: Breyta fyrirliggjandi staðsetningum í vöruhúsastaðsetningar | Microsoft Docs"
description: "Hægt er að láta birgðageymslu sem til er nota svæði og hólf og vinna sem vöruhúsastað."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: e519a1628342f7c4711b3266f53ac857d4865e71
ms.contentlocale: is-is
ms.lasthandoff: 03/22/2018

---
# <a name="convert-existing-locations-to-warehouse-locations"></a><span data-ttu-id="6973e-103">Breyta fyrirliggjandi staðsetningum í vöruhúsastaðsetningar</span><span class="sxs-lookup"><span data-stu-id="6973e-103">Convert Existing Locations to Warehouse Locations</span></span>
<span data-ttu-id="6973e-104">Hægt er að láta birgðageymslu sem til er nota svæði og hólf og vinna sem vöruhúsastað.</span><span class="sxs-lookup"><span data-stu-id="6973e-104">You can enable an existing inventory location to use zones and bins and to operate as a warehouse location.</span></span>  

<span data-ttu-id="6973e-105">Keyrslan til að gera birgðageymslu virka fyrir vöruhúsaðgerðir stofnar upphafsfærslur vöruhúss fyrir leiðréttingarhólf vöruhúss fyrir allar vörur sem geymdar eru í birgðageymslunni.</span><span class="sxs-lookup"><span data-stu-id="6973e-105">The batch job to enable a location for warehouse operation creates initial warehouse entries for the warehouse adjustment bin for all items that have inventory in the location.</span></span> <span data-ttu-id="6973e-106">Þessar upphafsfærslur verða jafnaðar þegar raunbirgðafærslur vöruhúss eru færðar inn eftir keyrslu keyrslunnar.</span><span class="sxs-lookup"><span data-stu-id="6973e-106">These initial entries will be balanced when warehouse physical inventory entries are entered after the batch job is run.</span></span>  

<span data-ttu-id="6973e-107">Hægt er að stofna svæði og hólf fyrir eða eftir umbreytinguna.</span><span class="sxs-lookup"><span data-stu-id="6973e-107">You can create zones and bins either before or after the conversion.</span></span> <span data-ttu-id="6973e-108">Eina hólfið sem þarf að stofna fyrir umbreytinguna er það sem notað verður sem leiðréttingarhólf í framtíðinni.</span><span class="sxs-lookup"><span data-stu-id="6973e-108">The only bin that you must create before the conversion is the one that is to be used as the future adjustment bin.</span></span>  

> [!IMPORTANT]  
>  <span data-ttu-id="6973e-109">Til að hreinsa allar neikvæðar birgðir og öll opin vöruhúsaskjöl áður en birgðageymslu er umbreytt fyrir vöruhúsameðhöndlun skal keyra skýrslu til að finna vörurnar með neikvæðar birgður og opin vöruhúsaskjöl fyrir birgðageymsluna.</span><span class="sxs-lookup"><span data-stu-id="6973e-109">To clear all negative inventory and any open warehouse documents before you convert the location for warehouse handling, run a report to identify the items with negative inventory and open warehouse documents for the location.</span></span> <span data-ttu-id="6973e-110">Frekari upplýsingar eru í Athuga neikvæða birgðastöðu.</span><span class="sxs-lookup"><span data-stu-id="6973e-110">For more information, see Check on Negative Inventory.</span></span>  

## <a name="to-enable-an-existing-location-to-operate-as-a-warehouse-location"></a><span data-ttu-id="6973e-111">Birgðageymsla sett upp sem vöruhúsastaður</span><span class="sxs-lookup"><span data-stu-id="6973e-111">To enable an existing location to operate as a warehouse location</span></span>  
1.  <span data-ttu-id="6973e-112">Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn  **Stofna vöruhúsastað** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="6973e-112">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Create Warehouse Location**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="6973e-113">Í reitnum **Kóti birgðageymslu** skal tilgreina birgðageymslu sem á að virkja fyrir úrvinnslu vöruhúss</span><span class="sxs-lookup"><span data-stu-id="6973e-113">In the **Location Code** field, specify the location that you want to enable for warehouse processing.</span></span>  
3.  <span data-ttu-id="6973e-114">Í reitnum **Kóti leiðréttingarhólfs** skal tilgreina hólfinu í birgðageymslunni þar sem ósamstilltar vöruhúsafærslur eru geymdar.</span><span class="sxs-lookup"><span data-stu-id="6973e-114">In the **Adjustment Bin Code** field, specify the bin at the location where unsynchronized warehouse entries are stored.</span></span> <span data-ttu-id="6973e-115">Nánari upplýsingar má nálgast á „Samstilla leiðréttar vöruhúsafærslur við tengdar birgðabókafærslur“ hlutanum í [Telja, leiðrétta og endurflokka birgðir](inventory-how-count-adjust-reclassify.md).</span><span class="sxs-lookup"><span data-stu-id="6973e-115">For more information, see the "To synchronize the adjusted warehouse entries with the related item ledger entries" section in [Count, Adjust, and Reclassify Inventory](inventory-how-count-adjust-reclassify.md).</span></span>  

    <span data-ttu-id="6973e-116">Opnu birgðafærslurnar fyrir tilgreindu birgðageymsluna eru notaðar í kerfinu til að stofna vöruhúsabókarlínur sem leggja saman allar samsetningar á vörunúmeri, afbrigðiskóta, mælieiningarkóta og, ef nauðsynlegt er, lotunúmeri og raðnúmeri í birgðafærslunum.</span><span class="sxs-lookup"><span data-stu-id="6973e-116">Using the open item ledger entries for the specified location, warehouse journal lines are created that sum up every combination of Item No., Variant Code, Unit of Measure Code, and, if necessary, Lot No. and Serial No. in the item ledger entries.</span></span> <span data-ttu-id="6973e-117">Vöruhúsabókarlínurnar bókast þá.</span><span class="sxs-lookup"><span data-stu-id="6973e-117">The warehouse journal lines are then posted.</span></span> <span data-ttu-id="6973e-118">Þessi bókun stofnar vöruhúsafærslur sem setja birgðirnar í leiðréttingarhólf vöruhúss.</span><span class="sxs-lookup"><span data-stu-id="6973e-118">This posting creates warehouse entries that place the inventory in the warehouse adjustment bin.</span></span> <span data-ttu-id="6973e-119">Kerfið setur einnig **Kóta leiðréttingarhólfs** á Birgðageymsluspjaldið.</span><span class="sxs-lookup"><span data-stu-id="6973e-119">The **Adjustment Bin Code** on the location card is also set.</span></span>  

4.  <span data-ttu-id="6973e-120">Til að sjá hvaða vörum var bætt í leiðréttingarhólfið í keyrslunni er hægt að keyra skýrsluna **Leiðréttingarhólf vöruhúss**.</span><span class="sxs-lookup"><span data-stu-id="6973e-120">To see which items were added to the adjustment bin during the batch job, run the **Warehouse Adjustment Bin** report.</span></span>  
5.  <span data-ttu-id="6973e-121">Þegar keyrslunni **Búa til birgðageymslu vöruhúss** er lokið þarf að framkvæma og bóka raunbirgðatalningu vöruhúss.</span><span class="sxs-lookup"><span data-stu-id="6973e-121">When the **Create Warehouse Location** batch job has completed, perform and post a warehouse physical inventory.</span></span> <span data-ttu-id="6973e-122">Nánari upplýsingar er að finna í [Telja, leiðrétta og endurflokka birgðir](inventory-how-count-adjust-reclassify.md).</span><span class="sxs-lookup"><span data-stu-id="6973e-122">For more information, see [Count, Adjust, and Reclassify Inventory](inventory-how-count-adjust-reclassify.md).</span></span>  

> [!NOTE]  
>  <span data-ttu-id="6973e-123">Mælt er með því að **Búa til birgðageymslu vöruhúss** runuvinnslan sé keyrð á tíma sem ekki hefur áhrif á dagleg störf í kerfinu.</span><span class="sxs-lookup"><span data-stu-id="6973e-123">It is recommended that you run the **Create Warehouse Location** batch job at a time when it will not impact the daily work in the system.</span></span> <span data-ttu-id="6973e-124">Keyrslan vinnur með hverja færslu í töflunni **Birgðafærsla** og ef margar birgðafærslur eru til staðar getur keyrslan tekið margar klukkustundir.</span><span class="sxs-lookup"><span data-stu-id="6973e-124">This job processes each entry in the **Item Ledger Entry** table, and if there are a large number of item ledger entries, the job can last several hours.</span></span>  

 <span data-ttu-id="6973e-125">Í þeim birgðageymslum þar sem vöruhúsastjórnunarskjöl voru ekki notuð fyrir umbreytinguna þarf að opna aftur og gefa út öll upprunaskjöl sem voru móttekin eða afhent að hluta fyrir umbreytinguna.</span><span class="sxs-lookup"><span data-stu-id="6973e-125">For those locations that did not use warehouse management documents before the conversion, you must re-open and release any source documents that were partially received or partially shipped before the conversion.</span></span>  

## <a name="see-also"></a><span data-ttu-id="6973e-126">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="6973e-126">See Also</span></span>  
[<span data-ttu-id="6973e-127">Vöruhúsastjórnun</span><span class="sxs-lookup"><span data-stu-id="6973e-127">Warehouse Management</span></span>](warehouse-manage-warehouse.md)  
[<span data-ttu-id="6973e-128">Birgðir</span><span class="sxs-lookup"><span data-stu-id="6973e-128">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="6973e-129">[Vöruhúsastjórnun sett upp](warehouse-setup-warehouse.md)   </span><span class="sxs-lookup"><span data-stu-id="6973e-129">[Setting Up Warehouse Management](warehouse-setup-warehouse.md)   </span></span>  
<span data-ttu-id="6973e-130">[Samsetningardeild](assembly-assemble-items.md)  </span><span class="sxs-lookup"><span data-stu-id="6973e-130">[Assembly Management](assembly-assemble-items.md)  </span></span>  
[<span data-ttu-id="6973e-131">Hönnunarupplýsingar vöruhúsakerfi</span><span class="sxs-lookup"><span data-stu-id="6973e-131">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="6973e-132">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="6973e-132">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

