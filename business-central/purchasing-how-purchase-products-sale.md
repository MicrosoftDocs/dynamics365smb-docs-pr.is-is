---
title: Kaupa vörur fyrir sölu með því að stofna innkaupareikninga | Microsoft Docs
description: Úr sölureikningi, til að kaupa vörur, geturðu stofnað innkaupareikning fyrir lánardrottinn eða birgja.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: supply planning, sales demand, replenish
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 32ae014f9d98ceb9c338596d859ec14395ceb6f5
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5377062"
---
# <a name="purchase-items-for-a-sale"></a><span data-ttu-id="dcdb9-103">Kaupa vörur fyrir sölu</span><span class="sxs-lookup"><span data-stu-id="dcdb9-103">Purchase Items for a Sale</span></span>
<span data-ttu-id="dcdb9-104">Frá sölupöntunum og sölureikningum geturðu notað aðgerð til stofna á skjótan hátt innkaupaskjöl fyrir vörumagn sem vantar en er krafist við söluna.</span><span class="sxs-lookup"><span data-stu-id="dcdb9-104">From sales orders and sales invoices, you can use functions to quickly create purchase documents for missing item quantities that are required by the sale.</span></span> <span data-ttu-id="dcdb9-105">Hægt er að nota tvær mismunandi aðgerðir, eftir gerð skjalsins.</span><span class="sxs-lookup"><span data-stu-id="dcdb9-105">You can use two different functions depending on the document type.</span></span>

> [!Note]
> <span data-ttu-id="dcdb9-106">Þessi virkni er til þess að endurnýja söluvöru í eigin birgðum.</span><span class="sxs-lookup"><span data-stu-id="dcdb9-106">This functionality is for replenishing sales items into your own inventory.</span></span> <span data-ttu-id="dcdb9-107">Til að kaupa vörur fyrir beina afhendingu frá lánardrottni þínum til viðskiptamanna þarftu að búa til beina sendingu.</span><span class="sxs-lookup"><span data-stu-id="dcdb9-107">To purchase items for direct delivery from your vendor to your customer, you must create a drop shipment.</span></span> <span data-ttu-id="dcdb9-108">Frekari upplýsingar eru í [Beinar sendingar](sales-how-drop-shipment.md).</span><span class="sxs-lookup"><span data-stu-id="dcdb9-108">For more information, see [Make Drop Shipments](sales-how-drop-shipment.md).</span></span>   

|<span data-ttu-id="dcdb9-109">Virkni</span><span class="sxs-lookup"><span data-stu-id="dcdb9-109">Function</span></span>|<span data-ttu-id="dcdb9-110">Description</span><span class="sxs-lookup"><span data-stu-id="dcdb9-110">Description</span></span>|
|--------|-----------|
|<span data-ttu-id="dcdb9-111">**Stofna innkaupapantanir**</span><span class="sxs-lookup"><span data-stu-id="dcdb9-111">**Create Purchase Orders**</span></span>|<span data-ttu-id="dcdb9-112">Frá sölupöntun, stofnar þessi aðgerð innkaupapöntun fyrir hvern lánardrottinn vöru á sölupöntuninni.</span><span class="sxs-lookup"><span data-stu-id="dcdb9-112">From a sales order, this function creates a purchase order for each vendor of items on the sales order.</span></span> <span data-ttu-id="dcdb9-113">Þú getur breytt innkaupamagninu áður en þú stofnar innkaupapantanirnar.</span><span class="sxs-lookup"><span data-stu-id="dcdb9-113">You can edit the purchase quantity before you create the purchase orders.</span></span> <span data-ttu-id="dcdb9-114">Aðeins er ótiltækt sölumagn lagt til.</span><span class="sxs-lookup"><span data-stu-id="dcdb9-114">Only unavailable sales quantities are suggested.</span></span>
|<span data-ttu-id="dcdb9-115">**Stofna innkaupareikning**</span><span class="sxs-lookup"><span data-stu-id="dcdb9-115">**Create Purchase Invoice**</span></span>|<span data-ttu-id="dcdb9-116">Úr sölupöntun og úr sölureikningi getur þessi aðgerð stofnað innkaupareikning fyrir valinn lánardrottinn fyrir allar línur eða valdar línur í söluskjalinu.</span><span class="sxs-lookup"><span data-stu-id="dcdb9-116">From a sales order and from a sales invoice, this function creates a purchase invoice for a selected vendor for all lines or selected lines on the sales document.</span></span> <span data-ttu-id="dcdb9-117">Lagt er til fullt sölumagn.</span><span class="sxs-lookup"><span data-stu-id="dcdb9-117">The full sales quantity is suggested.</span></span>|

## <a name="to-create-one-or-more-purchase-orders-from-a-sales-order"></a><span data-ttu-id="dcdb9-118">Stofna eina eða fleiri innkaupapöntun úr sölupöntun</span><span class="sxs-lookup"><span data-stu-id="dcdb9-118">To create one or more purchase orders from a sales order</span></span>
<span data-ttu-id="dcdb9-119">Til að stofna innkaupapöntun fyrir hvert ótiltækt vörumagn í sölupöntuninni, notarðu **Stofna innkaupapantanir** aðgerðina.</span><span class="sxs-lookup"><span data-stu-id="dcdb9-119">To create a purchase order for each unavailable item quantity on the sales order, you use the **Create Purchase Orders** function.</span></span>

1. <span data-ttu-id="dcdb9-120">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Sölupantanir** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="dcdb9-120">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Orders**, and then choose the related link.</span></span>
2. <span data-ttu-id="dcdb9-121">Opnuð er sölupöntun sem þú vilt kaupa vörur fyrir.</span><span class="sxs-lookup"><span data-stu-id="dcdb9-121">Open a sales order that you want to purchase items for.</span></span>
3. <span data-ttu-id="dcdb9-122">Velja **stofna innkaupapantanir** aðgerð.</span><span class="sxs-lookup"><span data-stu-id="dcdb9-122">Choose the **Create Purchase Orders** action.</span></span>

    <span data-ttu-id="dcdb9-123">Síðan **stofna innkaupapantanir** opnast og birtir eina línu fyrir hverja vöru í sölupöntuninni.</span><span class="sxs-lookup"><span data-stu-id="dcdb9-123">The **Create Purchase Orders** page opens showing a line for each different item on the sales order.</span></span> <span data-ttu-id="dcdb9-124">Línur fyrir bæði fullkomlega tiltækt sölumagn og ótiltækt sölumagn (grámaðar) eru sýndar að sjálfgefnu.</span><span class="sxs-lookup"><span data-stu-id="dcdb9-124">Lines for both fully available sales quantities and unavailable sales quantities (grayed) are shown by default.</span></span> <span data-ttu-id="dcdb9-125">Þú getur valið **sýna ótiltækt** aðgerðina til að sjá aðeins línur fyrir ótiltækt sölumagn.</span><span class="sxs-lookup"><span data-stu-id="dcdb9-125">You can choose the **Show Unavailable** action to only see lines for unavailable sales quantities.</span></span>

    <span data-ttu-id="dcdb9-126">Reiturinn **Magn til innkaupa** inniheldur ótiltækt sölumagn að sjálfgefnu.</span><span class="sxs-lookup"><span data-stu-id="dcdb9-126">The **Quantity to Purchase** field contains the unavailable sales quantity by default.</span></span>
4. <span data-ttu-id="dcdb9-127">Til að kaupa annað magn en ótiltækt sölumagn, skal breyta gildinu í **Magn til innkaupa** reitnum.</span><span class="sxs-lookup"><span data-stu-id="dcdb9-127">To purchase another quantity than the unavailable sales quantity, edit the value in the **Quantity to Purchase** field.</span></span>

    > [!NOTE]  
    >   <span data-ttu-id="dcdb9-128">Þú getur líka breytt **Magn til innkaupa** reitnum á grámuðum línum jafnvel þótt þær sýni fullkomlega tiltækt sölumagn.</span><span class="sxs-lookup"><span data-stu-id="dcdb9-128">You can also change the **Quantity to Purchase** field on grayed lines even though they represent fully available sales quantities.</span></span>
5. <span data-ttu-id="dcdb9-129">Velja hnappinn **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="dcdb9-129">Choose the **OK** button.</span></span>

    <span data-ttu-id="dcdb9-130">Innkaupapöntun er stofnuð fyrir hvern lánardrottinn vöru á sölupöntuninni, og í henni eru allar magnbreytingar sem þú kannt að hafa gert á síðunni **Stofna innkaupapöntun**.</span><span class="sxs-lookup"><span data-stu-id="dcdb9-130">A purchase order is created for each vendor of items on the sales order, including any quantity changes that you made on the **Create Purchase Orders** page.</span></span>
7. <span data-ttu-id="dcdb9-131">Halda áfram að vinna innkaupapöntun eða pantanir, til dæmis með því að breyta eða bæta við innkaupareikningslínum.</span><span class="sxs-lookup"><span data-stu-id="dcdb9-131">Proceed to process the purchase order or orders, for example, by editing or adding purchase order lines.</span></span> <span data-ttu-id="dcdb9-132">Nánari upplýsingar eru í reitnum [Skrá innkaup](purchasing-how-record-purchases.md).</span><span class="sxs-lookup"><span data-stu-id="dcdb9-132">For more information, see [Record Purchases](purchasing-how-record-purchases.md).</span></span>


## <a name="to-create-a-purchase-invoice-from-a-sales-order-or-sales-invoice"></a><span data-ttu-id="dcdb9-133">Stofna innkaupareikning úr sölupöntun eða sölureikningi</span><span class="sxs-lookup"><span data-stu-id="dcdb9-133">To create a purchase invoice from a sales order or sales invoice</span></span>
<span data-ttu-id="dcdb9-134">Til að stofna stakan innkaupareikning fyrir eina eða fleiri línur í söluskjali með því að velja fyrst hvaða lánardrottni skal kaupa af, notarðu **Stofna innkaupareikning** aðgerðina.</span><span class="sxs-lookup"><span data-stu-id="dcdb9-134">To create a single purchase invoice for one or more lines on a sales document by first selecting which vendor to buy from, you use the **Create Purchase Invoice** function.</span></span>

> [!NOTE]  
>   <span data-ttu-id="dcdb9-135">Þessi aðgerð stofnar innkaupareikning fyrir nákvæmlega það vörumagn sem er á valda söluskjalinu.</span><span class="sxs-lookup"><span data-stu-id="dcdb9-135">This function creates a purchase invoice for the exact item quantity on the selected sales document.</span></span> <span data-ttu-id="dcdb9-136">Til að breyta innkaupamagninu, þarftu að breyta innkaupareikningnum eftir að þú stofnar hann.</span><span class="sxs-lookup"><span data-stu-id="dcdb9-136">To change the purchase quantity, you must edit the purchase invoice after it is created.</span></span>  

1. <span data-ttu-id="dcdb9-137">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Sölupantanir** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="dcdb9-137">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Orders**, and then choose the related link.</span></span>
2. <span data-ttu-id="dcdb9-138">Opnuð er sölureikningur sem þú vilt kaupa vörur fyrir.</span><span class="sxs-lookup"><span data-stu-id="dcdb9-138">Open a sales invoice that you want to purchase items for.</span></span>
3. <span data-ttu-id="dcdb9-139">Veldu eitt eða fleiri sölureikningslínur sem þú vilt nota á innkaupareikningur.</span><span class="sxs-lookup"><span data-stu-id="dcdb9-139">Select one or more sales invoice lines that you want to use on the purchase invoice.</span></span> <span data-ttu-id="dcdb9-140">Til að nota alla sölureikningslínur, velja annaðhvort í heild eða ekki velja neinar línur.</span><span class="sxs-lookup"><span data-stu-id="dcdb9-140">To use all the sales invoice lines, select either all of them or do not select any lines.</span></span>
4. <span data-ttu-id="dcdb9-141">Velja **stofna innkaupareikning** aðgerð.</span><span class="sxs-lookup"><span data-stu-id="dcdb9-141">Choose the **Create Purchase Invoice** action.</span></span>
5. <span data-ttu-id="dcdb9-142">Veldu annað hvort **Allar línur** eða  **valdar línur** og velja svo **Í lagi** hnappinn.</span><span class="sxs-lookup"><span data-stu-id="dcdb9-142">Select either **All Lines** or **Selected Lines**, and then choose the **OK** button.</span></span>  
6. <span data-ttu-id="dcdb9-143">Í listanum yfir lánardrottna sem birtist skaltu velja lánardrottin sem þú vilt kaupa allar vörurnar af, og þá velja **Í lagi** hnappinn.</span><span class="sxs-lookup"><span data-stu-id="dcdb9-143">In the list of vendors that appears, select the vendor that you want to buy all the items from, and then choose the **OK** button.</span></span>

    <span data-ttu-id="dcdb9-144">Innkaupareikningur er stofnaður sem inniheldur eina, fleiri en eina eða allar línur sölureikningsins.</span><span class="sxs-lookup"><span data-stu-id="dcdb9-144">A purchase invoice is created that contains one, more than one, or all the lines on the sales invoice.</span></span>
7. <span data-ttu-id="dcdb9-145">Halda áfram að vinna innkaupareikning, til dæmis með því að breyta eða bæta við innkaupareikningslínum.</span><span class="sxs-lookup"><span data-stu-id="dcdb9-145">Proceed to process the purchase invoice, for example, by editing or adding purchase invoice lines.</span></span> <span data-ttu-id="dcdb9-146">Nánari upplýsingar eru í reitnum [Skrá innkaup](purchasing-how-record-purchases.md).</span><span class="sxs-lookup"><span data-stu-id="dcdb9-146">For more information, see [Record Purchases](purchasing-how-record-purchases.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="dcdb9-147">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="dcdb9-147">See Also</span></span>
[<span data-ttu-id="dcdb9-148">Innkaup</span><span class="sxs-lookup"><span data-stu-id="dcdb9-148">Purchasing</span></span>](purchasing-manage-purchasing.md)  
[<span data-ttu-id="dcdb9-149">Skrá innkaup</span><span class="sxs-lookup"><span data-stu-id="dcdb9-149">Record Purchases</span></span>](purchasing-how-record-purchases.md)  
[<span data-ttu-id="dcdb9-150">Reikningsfæra sölur</span><span class="sxs-lookup"><span data-stu-id="dcdb9-150">Invoice Sales</span></span>](sales-how-invoice-sales.md)  
[<span data-ttu-id="dcdb9-151">Skráning nýrra lánardrottna</span><span class="sxs-lookup"><span data-stu-id="dcdb9-151">Register New Vendors</span></span>](purchasing-how-register-new-vendors.md)  
<span data-ttu-id="dcdb9-152">[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="dcdb9-152">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]