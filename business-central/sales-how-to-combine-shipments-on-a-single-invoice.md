---
title: "Hvernig á að sameina afhendingar í einn reikning | Microsoft Docs"
description: "Eigi að reikningsfæra fleiri en eina afhendingu saman er hægt að nota eiginleikann sameina afhendingar."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/14/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: d100ec6888fbd2e8fa55ce0facef8645a079dc76
ms.contentlocale: is-is
ms.lasthandoff: 03/22/2018

---
# <a name="combine-shipments-on-a-single-invoice"></a><span data-ttu-id="b215d-103">Sameina afhendingar einn reikning</span><span class="sxs-lookup"><span data-stu-id="b215d-103">Combine Shipments on a Single Invoice</span></span>
<span data-ttu-id="b215d-104">Eigi að reikningsfæra fleiri en eina afhendingu saman er hægt að nota eiginleikann sameina afhendingar.</span><span class="sxs-lookup"><span data-stu-id="b215d-104">If you want to invoice more than one shipment at a time, you can use the combined shipments feature.</span></span>  

 <span data-ttu-id="b215d-105">Áður en hægt er að búa til sameinaða afhendingu þarf að vera búið að bóka fleiri en eina söluafhendingu fyrir sama viðskiptamanninn í sama gjaldmiðlinum.</span><span class="sxs-lookup"><span data-stu-id="b215d-105">Before you can create a combined shipment, more than one sales shipment for the same customer in the same currency must be posted.</span></span> <span data-ttu-id="b215d-106">Það er að segja, það þarf að vera búið að fylla út tvær eða fleiri sölupantanir og bóka þær sem afhentar en ekki reikningsfærðar.</span><span class="sxs-lookup"><span data-stu-id="b215d-106">In other words, you must have filled in two or more sales orders and posted them as shipped, but not invoiced.</span></span> <span data-ttu-id="b215d-107">Til að sameina afhendingar þarf að velja gátreitinn **Sameina afhendingar** á flýtiflipanum **Afhending** í spjaldinu **viðskiptamaður**.</span><span class="sxs-lookup"><span data-stu-id="b215d-107">To combine shipments, the **Combine Shipments** check box must be selected on the **Shipping** FastTab of the **Customer** card.</span></span>  

## <a name="to-manually-combine-shipments-on-a-single-invoice"></a><span data-ttu-id="b215d-108">Að sameina afhendingar handvirkt í einn reikning</span><span class="sxs-lookup"><span data-stu-id="b215d-108">To manually combine shipments on a single invoice</span></span>  
1. <span data-ttu-id="b215d-109">Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Innkaupareikningar** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="b215d-109">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Sales Invoices**, and then choose the related link.</span></span>  
2. <span data-ttu-id="b215d-110">Valið er **Nýtt** aðgerð.</span><span class="sxs-lookup"><span data-stu-id="b215d-110">Choose the **New** action.</span></span> <span data-ttu-id="b215d-111">Frekari upplýsingar eru í [Reikningsfæra sölur](sales-how-invoice-sales.md).</span><span class="sxs-lookup"><span data-stu-id="b215d-111">For more information, see [Invoice Sales](sales-how-invoice-sales.md).</span></span>
3. <span data-ttu-id="b215d-112">Í reitnum **Selt til Viðskm.nr.**.</span><span class="sxs-lookup"><span data-stu-id="b215d-112">In the **Sell-to Customer No.**</span></span> <span data-ttu-id="b215d-113">reitnum er viðskiptamaðurinn sem fær reikninginn fyrir afhentar vörur tilgreindur.</span><span class="sxs-lookup"><span data-stu-id="b215d-113">field, enter the customer who will receive the invoice for the shipped items.</span></span>  
4. <span data-ttu-id="b215d-114">Á flýtiflipanum **Línur** skal velja **Sækja afhendingarlínur** aðgerðina.</span><span class="sxs-lookup"><span data-stu-id="b215d-114">On the **Lines** FastTab, choose the **Get Shipment Lines** action.</span></span>  
5. <span data-ttu-id="b215d-115">Afhendingarlínan sem á að vera á reikningnum er valin:</span><span class="sxs-lookup"><span data-stu-id="b215d-115">Select the shipment line that you want to include in the invoice:</span></span>  

    - <span data-ttu-id="b215d-116">Til að setja allar línur inn eru allar línur valda og svo smellt á **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="b215d-116">To insert all lines, select all lines and choose the **OK** button.</span></span>  
    - <span data-ttu-id="b215d-117">Til að setja sérstakar línur inn eru línurnar valdar og svo smellt á **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="b215d-117">To insert specific lines, select the lines and choose the **OK** button.</span></span> <span data-ttu-id="b215d-118">Hægt er að nota Ctrl-takkanum til að velja margar línur sem ekki eru samliggjandi.</span><span class="sxs-lookup"><span data-stu-id="b215d-118">You can use the Ctrl key to select multiple nonsequential lines.</span></span>  

    <span data-ttu-id="b215d-119">Ef röng afhendingarlína var valin eða byrja á aftur er línunum einfaldlega eytt í reikningnum aðgerðin **Sækja afhendingarlínur** keyrð aftur.</span><span class="sxs-lookup"><span data-stu-id="b215d-119">If an incorrect shipment line was selected or you want to start over, you can simply delete the lines on the invoice and re-run the **Get Shipment Lines** function.</span></span>  
7. <span data-ttu-id="b215d-120">Til að bóka reikningur er valið aðgerðin **bóka**.</span><span class="sxs-lookup"><span data-stu-id="b215d-120">To post the invoice, choose the **Post** action.</span></span>  

## <a name="to-automatically-combine-shipments-on-a-single-invoice"></a><span data-ttu-id="b215d-121">Til að sameina afhendingar sjálfkrafa á einn reikning</span><span class="sxs-lookup"><span data-stu-id="b215d-121">To automatically combine shipments on a single invoice</span></span>  
1. <span data-ttu-id="b215d-122">Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Sameina afhendingu** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="b215d-122">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Combine Shipments**, and then choose the related link.</span></span> <span data-ttu-id="b215d-123">Keyrslubeiðnaglugginn  opnast.</span><span class="sxs-lookup"><span data-stu-id="b215d-123">The batch job request window opens.</span></span>  
2. <span data-ttu-id="b215d-124">Fyllið inn í reitina eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="b215d-124">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="b215d-125">Velja skal gátreitinn **Bóka reikninga**.</span><span class="sxs-lookup"><span data-stu-id="b215d-125">Select the **Post Invoices** check box.</span></span>  
4.  <span data-ttu-id="b215d-126">Velja hnappinn **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="b215d-126">Choose the **OK** button.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="b215d-127">Bóka þarf reikninga handvirkt ef gátreiturinn **Bóka reikninga** var ekki valinn í keyrslunni.</span><span class="sxs-lookup"><span data-stu-id="b215d-127">You will need to manually post the invoices if the **Post Invoices** check box was not selected on the batch job.</span></span>  

## <a name="to-remove-open-sales-orders-after-combined-shipment-posting"></a><span data-ttu-id="b215d-128">Til að fjarlægja opnar sölupantanir eftir sameinaða afhending bókun</span><span class="sxs-lookup"><span data-stu-id="b215d-128">To remove open sales orders after combined shipment posting</span></span> 
<span data-ttu-id="b215d-129">Þegar afhendingar eru sameinaðar í reikningi og bókaðar er bókaður sölureikningur stofnaður fyrir reikningsfærðu línurnar.</span><span class="sxs-lookup"><span data-stu-id="b215d-129">When shipments are combined on an invoice and posted, a posted sales invoice is created for the invoiced lines.</span></span> <span data-ttu-id="b215d-130">Reiturinn **Reikningsfært magn** í upphaflegu standandi sölupöntuninni eða sölupöntuninni er uppfærður samkvæmt reikningsfærða magninu.</span><span class="sxs-lookup"><span data-stu-id="b215d-130">The **Quantity Invoiced** field on the originating blanket sales order or sales order is updated based on the invoiced quantity.</span></span>  

<span data-ttu-id="b215d-131">Þegar afhendingar eru reikningsfærðar á þennan hátt eru pantanir sem afhendingar voru bókaðar úr enn til staðar, jafnvel þótt þær hafi verið afhentar og reikningsfærðar að fullu.</span><span class="sxs-lookup"><span data-stu-id="b215d-131">When you invoice shipments in this way, the orders from which the shipments were posted still exist, even if they have been fully shipped and invoiced.</span></span>   

1. <span data-ttu-id="b215d-132">Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Eyða reikningsfærðum sölupöntunum** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="b215d-132">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Delete Invoiced Sales Orders**, and then select the link.</span></span>  
2. <span data-ttu-id="b215d-133">Tilgreinið í **Nr.**.</span><span class="sxs-lookup"><span data-stu-id="b215d-133">Specify in the **No.**</span></span> <span data-ttu-id="b215d-134">afmörkunarreitnum hvaða sölupantanir á að eyða.</span><span class="sxs-lookup"><span data-stu-id="b215d-134">filter field which sales orders to delete.</span></span>  
3. <span data-ttu-id="b215d-135">Velja hnappinn **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="b215d-135">Choose the **OK** button.</span></span>  

<span data-ttu-id="b215d-136">Að öðrum kosti skal eyða einstökum sölupöntunum handvirkt.</span><span class="sxs-lookup"><span data-stu-id="b215d-136">Alternatively, delete individual sales orders manually.</span></span>  

<span data-ttu-id="b215d-137">Skref 1 til 3 eru endurtekin fyrir öll skjöl sem urðu fyrir áhrifum, eins og auðar sölupantanir.</span><span class="sxs-lookup"><span data-stu-id="b215d-137">Repeat steps 1 through 3 for any other affected documents, such as blanket sales orders.</span></span>

## <a name="see-also"></a><span data-ttu-id="b215d-138">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="b215d-138">See Also</span></span>  
[<span data-ttu-id="b215d-139">Sala</span><span class="sxs-lookup"><span data-stu-id="b215d-139">Sales</span></span>](sales-manage-sales.md)  
<span data-ttu-id="b215d-140">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="b215d-140">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

