---
title: Hvernig á að sameina afhendingar í einn reikning | Microsoft Docs
description: Eigi að reikningsfæra fleiri en eina afhendingu saman er hægt að nota eiginleikann sameina afhendingar.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 802cb7e6d7b7bb56f994eaf2b45df9c9f9cb43d3
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5383076"
---
# <a name="combine-shipments-on-a-single-invoice"></a><span data-ttu-id="d6efd-103">Sameina afhendingar einn reikning</span><span class="sxs-lookup"><span data-stu-id="d6efd-103">Combine Shipments on a Single Invoice</span></span>
<span data-ttu-id="d6efd-104">Eigi að reikningsfæra fleiri en eina afhendingu saman er hægt að nota eiginleikann sameina afhendingar.</span><span class="sxs-lookup"><span data-stu-id="d6efd-104">If you want to invoice more than one shipment at a time, you can use the combined shipments feature.</span></span>  

<span data-ttu-id="d6efd-105">Áður en hægt er að búa til sameinaða afhendingu þarf að vera búið að bóka fleiri en eina söluafhendingu fyrir sama viðskiptamanninn í sama gjaldmiðlinum.</span><span class="sxs-lookup"><span data-stu-id="d6efd-105">Before you can create a combined shipment, more than one sales shipment for the same customer in the same currency must be posted.</span></span> <span data-ttu-id="d6efd-106">Það er að segja, það þarf að vera búið að búa til tvær eða fleiri sölupantanir og bóka þær sem afhentar en ekki reikningsfærðar.</span><span class="sxs-lookup"><span data-stu-id="d6efd-106">In other words, you must have create two or more sales orders and post them as shipped, but not invoiced.</span></span> 

## <a name="to-manually-combine-shipments-on-a-single-invoice"></a><span data-ttu-id="d6efd-107">Að sameina afhendingar handvirkt í einn reikning</span><span class="sxs-lookup"><span data-stu-id="d6efd-107">To manually combine shipments on a single invoice</span></span>  
1. <span data-ttu-id="d6efd-108">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Sölureikningar** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="d6efd-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Invoices**, and then choose the related link.</span></span>  
2. <span data-ttu-id="d6efd-109">Valið er **Nýtt** aðgerð.</span><span class="sxs-lookup"><span data-stu-id="d6efd-109">Choose the **New** action.</span></span> <span data-ttu-id="d6efd-110">Frekari upplýsingar eru í [Reikningsfæra sölur](sales-how-invoice-sales.md).</span><span class="sxs-lookup"><span data-stu-id="d6efd-110">For more information, see [Invoice Sales](sales-how-invoice-sales.md).</span></span>
3. <span data-ttu-id="d6efd-111">Í reitnum **Selt til Viðskm.nr.**.</span><span class="sxs-lookup"><span data-stu-id="d6efd-111">In the **Sell-to Customer No.**</span></span> <span data-ttu-id="d6efd-112">reitnum er viðskiptamaðurinn sem fær reikninginn fyrir afhentar vörur tilgreindur.</span><span class="sxs-lookup"><span data-stu-id="d6efd-112">field, enter the customer who will receive the invoice for the shipped items.</span></span>  
4. <span data-ttu-id="d6efd-113">Á flýtiflipanum **Línur** skal velja **Sækja afhendingarlínur** aðgerðina.</span><span class="sxs-lookup"><span data-stu-id="d6efd-113">On the **Lines** FastTab, choose the **Get Shipment Lines** action.</span></span>  
5. <span data-ttu-id="d6efd-114">Afhendingarlínan sem á að vera á reikningnum er valin:</span><span class="sxs-lookup"><span data-stu-id="d6efd-114">Select the shipment line that you want to include in the invoice:</span></span>  

    - <span data-ttu-id="d6efd-115">Til að setja allar línur inn eru allar línur valda og svo smellt á **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="d6efd-115">To insert all lines, select all lines and choose the **OK** button.</span></span>  
    - <span data-ttu-id="d6efd-116">Til að setja sérstakar línur inn eru línurnar valdar og svo smellt á **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="d6efd-116">To insert specific lines, select the lines and choose the **OK** button.</span></span> <span data-ttu-id="d6efd-117">Hægt er að nota Ctrl-takkanum til að velja margar línur sem ekki eru samliggjandi.</span><span class="sxs-lookup"><span data-stu-id="d6efd-117">You can use the Ctrl key to select multiple nonsequential lines.</span></span>  

    <span data-ttu-id="d6efd-118">Ef röng afhendingarlína var valin eða byrja á aftur er línunum einfaldlega eytt í reikningnum aðgerðin **Sækja afhendingarlínur** keyrð aftur.</span><span class="sxs-lookup"><span data-stu-id="d6efd-118">If an incorrect shipment line was selected or you want to start over, you can simply delete the lines on the invoice and re-run the **Get Shipment Lines** function.</span></span>  
7. <span data-ttu-id="d6efd-119">Til að bóka reikningur er valið aðgerðin **bóka**.</span><span class="sxs-lookup"><span data-stu-id="d6efd-119">To post the invoice, choose the **Post** action.</span></span>  

## <a name="to-automatically-combine-shipments-on-a-single-invoice"></a><span data-ttu-id="d6efd-120">Til að sameina afhendingar sjálfkrafa á einn reikning</span><span class="sxs-lookup"><span data-stu-id="d6efd-120">To automatically combine shipments on a single invoice</span></span>  
[!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="d6efd-121">mun aðeins velja sölupantanir þar sem **Sameina afhendingar** er valið.</span><span class="sxs-lookup"><span data-stu-id="d6efd-121">will select only sales orders where **Combine Shipments** is chosen.</span></span> 

1. <span data-ttu-id="d6efd-122">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Sameina afhendingar** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="d6efd-122">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Combine Shipments**, and then choose the related link.</span></span> <span data-ttu-id="d6efd-123">Síðan fyrir keyrslubeiðniglugga opnast.</span><span class="sxs-lookup"><span data-stu-id="d6efd-123">The batch job request page opens.</span></span>  
2. <span data-ttu-id="d6efd-124">Fyllið inn reitina eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="d6efd-124">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="d6efd-125">Velja skal gátreitinn **Bóka reikninga**.</span><span class="sxs-lookup"><span data-stu-id="d6efd-125">Choose the **Post Invoices** check box.</span></span>  
4. <span data-ttu-id="d6efd-126">Velja hnappinn **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="d6efd-126">Choose the **OK** button.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="d6efd-127">Bóka þarf reikninga handvirkt ef gátreiturinn **Bóka reikninga** var ekki valinn í keyrslunni.</span><span class="sxs-lookup"><span data-stu-id="d6efd-127">You will need to manually post the invoices if the **Post Invoices** check box was not selected on the batch job.</span></span>  

## <a name="to-remove-open-sales-orders-after-combined-shipment-posting"></a><span data-ttu-id="d6efd-128">Til að fjarlægja opnar sölupantanir eftir sameinaða afhending bókun</span><span class="sxs-lookup"><span data-stu-id="d6efd-128">To remove open sales orders after combined shipment posting</span></span> 
<span data-ttu-id="d6efd-129">Þegar afhendingar eru sameinaðar í reikningi og bókaðar er bókaður sölureikningur stofnaður fyrir reikningsfærðu línurnar.</span><span class="sxs-lookup"><span data-stu-id="d6efd-129">When shipments are combined on an invoice and posted, a posted sales invoice is created for the invoiced lines.</span></span> <span data-ttu-id="d6efd-130">Reiturinn **Reikningsfært magn** í upphaflegu standandi sölupöntuninni eða sölupöntuninni er uppfærður samkvæmt reikningsfærða magninu.</span><span class="sxs-lookup"><span data-stu-id="d6efd-130">The **Quantity Invoiced** field on the originating blanket sales order or sales order is updated based on the invoiced quantity.</span></span>  

<span data-ttu-id="d6efd-131">Þegar afhendingar eru reikningsfærðar á þennan hátt eru pantanir sem afhendingar voru bókaðar úr enn til staðar, jafnvel þótt þær hafi verið afhentar og reikningsfærðar að fullu.</span><span class="sxs-lookup"><span data-stu-id="d6efd-131">When you invoice shipments in this way, the orders from which the shipments were posted still exist, even if they have been fully shipped and invoiced.</span></span>   

1. <span data-ttu-id="d6efd-132">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Eyða reikningsfærðum sölupöntunum** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="d6efd-132">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Delete Invoiced Sales Orders**, and then select the link.</span></span>  
2. <span data-ttu-id="d6efd-133">Tilgreinið í **Nr.**.</span><span class="sxs-lookup"><span data-stu-id="d6efd-133">Specify in the **No.**</span></span> <span data-ttu-id="d6efd-134">afmörkunarreitnum hvaða sölupantanir á að eyða.</span><span class="sxs-lookup"><span data-stu-id="d6efd-134">filter field which sales orders to delete.</span></span>  
3. <span data-ttu-id="d6efd-135">Velja hnappinn **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="d6efd-135">Choose the **OK** button.</span></span>  

<span data-ttu-id="d6efd-136">Að öðrum kosti skal eyða einstökum sölupöntunum handvirkt.</span><span class="sxs-lookup"><span data-stu-id="d6efd-136">Alternatively, delete individual sales orders manually.</span></span>  

<span data-ttu-id="d6efd-137">Skref 1 til 3 eru endurtekin fyrir öll skjöl sem urðu fyrir áhrifum, eins og auðar sölupantanir.</span><span class="sxs-lookup"><span data-stu-id="d6efd-137">Repeat steps 1 through 3 for any other affected documents, such as blanket sales orders.</span></span>

## <a name="see-also"></a><span data-ttu-id="d6efd-138">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="d6efd-138">See Also</span></span>  
[<span data-ttu-id="d6efd-139">Sala</span><span class="sxs-lookup"><span data-stu-id="d6efd-139">Sales</span></span>](sales-manage-sales.md)  
<span data-ttu-id="d6efd-140">[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="d6efd-140">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]