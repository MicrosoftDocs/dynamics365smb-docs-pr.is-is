---
title: "Stofna innkaupareikning úr sölureikningi til að kaupa vörur fyrir sölu | Microsoft Docs"
description: "Úr sölureikningi, til að kaupa vörur, geturðu stofnað innkaupareikning fyrir lánardrottinn eða birgja."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: supply planning, sales demand, replenish
ms.date: 01/25/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 67e76ea76267c001277be3203c28103c3acb3214
ms.contentlocale: is-is
ms.lasthandoff: 01/30/2018

---
# <a name="purchase-items-for-a-sale"></a><span data-ttu-id="85633-103">Kaupa vörur fyrir sölu</span><span class="sxs-lookup"><span data-stu-id="85633-103">Purchase Items for a Sale</span></span>
<span data-ttu-id="85633-104">Frá sölupöntunum og sölureikningum geturðu notað aðgerð til stofna á skjótan hátt innkaupaskjöl fyrir vörumagn sem vantar en er krafist við söluna.</span><span class="sxs-lookup"><span data-stu-id="85633-104">From sales orders and sales invoices, you can use functions to quickly create purchase documents for missing item quantities that are required by the sale.</span></span> <span data-ttu-id="85633-105">Hægt er að nota tvær mismunandi aðgerðir, eftir gerð skjalsins.</span><span class="sxs-lookup"><span data-stu-id="85633-105">You can use two different functions depending on the document type.</span></span>
|<span data-ttu-id="85633-106">Virkni</span><span class="sxs-lookup"><span data-stu-id="85633-106">Function</span></span>|<span data-ttu-id="85633-107">Description</span><span class="sxs-lookup"><span data-stu-id="85633-107">Description</span></span>|
|--------|-----------|
|<span data-ttu-id="85633-108">**Stofna innkaupapantanir**</span><span class="sxs-lookup"><span data-stu-id="85633-108">**Create Purchase Orders**</span></span>|<span data-ttu-id="85633-109">Frá sölupöntun, stofnar þessi aðgerð innkaupapöntun fyrir hvern lánardrottinn vöru á sölupöntuninni.</span><span class="sxs-lookup"><span data-stu-id="85633-109">From a sales order, this function creates a purchase order for each vendor of items on the sales order.</span></span> <span data-ttu-id="85633-110">Þú getur breytt innkaupamagninu áður en þú stofnar innkaupapantanirnar.</span><span class="sxs-lookup"><span data-stu-id="85633-110">You can edit the purchase quantity before you create the purchase orders.</span></span> <span data-ttu-id="85633-111">Aðeins er ótiltækt sölumagn lagt til.</span><span class="sxs-lookup"><span data-stu-id="85633-111">Only unavailable sales quantities are suggested.</span></span>
|<span data-ttu-id="85633-112">**Stofna innkaupareikning**</span><span class="sxs-lookup"><span data-stu-id="85633-112">**Create Purchase Invoice**</span></span>|<span data-ttu-id="85633-113">Úr sölupöntun og úr sölureikningi getur þessi aðgerð stofnað innkaupareikning fyrir valinn lánardrottinn fyrir allar línur eða valdar línur í söluskjalinu.</span><span class="sxs-lookup"><span data-stu-id="85633-113">From a sales order and from a sales invoice, this function creates a purchase invoice for a selected vendor for all lines or selected lines on the sales document.</span></span> <span data-ttu-id="85633-114">Lagt er til fullt sölumagn.</span><span class="sxs-lookup"><span data-stu-id="85633-114">The full sales quantity is suggested.</span></span>|

## <a name="to-create-one-or-more-purchase-orders-from-a-sales-order"></a><span data-ttu-id="85633-115">Stofna eina eða fleiri innkaupapöntun úr sölupöntun</span><span class="sxs-lookup"><span data-stu-id="85633-115">To create one or more purchase orders from a sales order</span></span>
<span data-ttu-id="85633-116">Til að stofna innkaupapöntun fyrir hvert ótiltækt vörumagn í sölupöntuninni, notarðu **Stofna innkaupapantanir** aðgerðina.</span><span class="sxs-lookup"><span data-stu-id="85633-116">To create a purchase order for each unavailable item quantity on the sales order, you use the **Create Purchase Orders** function.</span></span>

1. <span data-ttu-id="85633-117">Á heimasíðunni skal velja **áframhaldandi Sölupöntun** gluggareit.</span><span class="sxs-lookup"><span data-stu-id="85633-117">On the Home page, choose the **Ongoing Sales Orders** tile.</span></span>
2. <span data-ttu-id="85633-118">Opnuð er sölupöntun sem þú vilt kaupa vörur fyrir.</span><span class="sxs-lookup"><span data-stu-id="85633-118">Open a sales order that you want to purchase items for.</span></span>
3. <span data-ttu-id="85633-119">Velja **stofna innkaupapantanir** aðgerð.</span><span class="sxs-lookup"><span data-stu-id="85633-119">Choose the **Create Purchase Orders** action.</span></span>

    <span data-ttu-id="85633-120">Glugginn **stofna innkaupapantanir** opnast og birtir eina línu fyrir hverja vöru í sölupöntuninni.</span><span class="sxs-lookup"><span data-stu-id="85633-120">The **Create Purchase Orders** window opens showing a line for each different item on the sales order.</span></span> <span data-ttu-id="85633-121">Línur fyrir bæði fullkomlega tiltækt sölumagn og ótiltækt sölumagn (grámaðar) eru sýndar að sjálfgefnu.</span><span class="sxs-lookup"><span data-stu-id="85633-121">Lines for both fully available sales quantities and unavailable sales quantities (grayed) are shown by default.</span></span> <span data-ttu-id="85633-122">Þú getur valið **sýna ótiltækt** aðgerðina til að sjá aðeins línur fyrir ótiltækt sölumagn.</span><span class="sxs-lookup"><span data-stu-id="85633-122">You can choose the **Show Unavailable** action to only see lines for unavailable sales quantities.</span></span>

    <span data-ttu-id="85633-123">Reiturinn **Magn til innkaupa** inniheldur ótiltækt sölumagn að sjálfgefnu.</span><span class="sxs-lookup"><span data-stu-id="85633-123">The **Quantity to Purchase** field contains the unavailable sales quantity by default.</span></span>
4. <span data-ttu-id="85633-124">Til að kaupa annað magn en ótiltækt sölumagn, skal breyta gildinu í **Magn til innkaupa** reitnum.</span><span class="sxs-lookup"><span data-stu-id="85633-124">To purchase another quantity than the unavailable sales quantity, edit the value in the **Quantity to Purchase** field.</span></span>

    > [!NOTE]  
>   <span data-ttu-id="85633-125">Þú getur líka breytt **Magn til innkaupa** reitnum á grámuðum línum jafnvel þótt þær sýni fullkomlega tiltækt sölumagn.</span><span class="sxs-lookup"><span data-stu-id="85633-125">You can also change the **Quantity to Purchase** field on grayed lines even though they represent fully available sales quantities.</span></span>
5. <span data-ttu-id="85633-126">Velja hnappinn **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="85633-126">Choose the **OK** button.</span></span>

    <span data-ttu-id="85633-127">Innkaupapöntun er stofnuð fyrir hvern lánardrottinn vöru á sölupöntuninni, og í henni eru allar magnbreytingar sem þú kannt að hafa gert í **Stofna innkaupapöntun** glugganum.</span><span class="sxs-lookup"><span data-stu-id="85633-127">A purchase order is created for each vendor of items on the sales order, including any quantity changes that you made in the **Create Purchase Orders** window.</span></span>
7. <span data-ttu-id="85633-128">Halda áfram að vinna innkaupapöntun eða pantanir, til dæmis með því að breyta eða bæta við innkaupareikningslínum.</span><span class="sxs-lookup"><span data-stu-id="85633-128">Proceed to process the purchase order or orders, for example, by editing or adding purchase order lines.</span></span> <span data-ttu-id="85633-129">Nánari upplýsingar eru í reitnum [Skrá innkaup](purchasing-how-record-purchases.md).</span><span class="sxs-lookup"><span data-stu-id="85633-129">For more information, see [Record Purchases](purchasing-how-record-purchases.md).</span></span>


## <a name="to-create-a-purchase-invoice-from-a-sales-order-or-sales-invoice"></a><span data-ttu-id="85633-130">Stofna innkaupareikning úr sölupöntun eða sölureikningi</span><span class="sxs-lookup"><span data-stu-id="85633-130">To create a purchase invoice from a sales order or sales invoice</span></span>
<span data-ttu-id="85633-131">Til að stofna stakan innkaupareikning fyrir eina eða fleiri línur í söluskjali með því að velja fyrst hvaða lánardrottni skal kaupa af, notarðu **Stofna innkaupareikning** aðgerðina.</span><span class="sxs-lookup"><span data-stu-id="85633-131">To create a single purchase invoice for one or more lines on a sales document by first selecting which vendor to buy from, you use the **Create Purchase Invoice** function.</span></span>

> [!NOTE]  
>   <span data-ttu-id="85633-132">Þessi aðgerð stofnar innkaupareikning fyrir nákvæmlega það vörumagn sem er á valda söluskjalinu.</span><span class="sxs-lookup"><span data-stu-id="85633-132">This function creates a purchase invoice for the exact item quantity on the selected sales document.</span></span> <span data-ttu-id="85633-133">Til að breyta innkaupamagninu, þarftu að breyta innkaupareikningnum eftir að þú stofnar hann.</span><span class="sxs-lookup"><span data-stu-id="85633-133">To change the purchase quantity, you must edit the purchase invoice after it is created.</span></span>  

1. <span data-ttu-id="85633-134">Í reitnum heimasíða , velja **áframhaldandi Sölupöntun** gluggareit.</span><span class="sxs-lookup"><span data-stu-id="85633-134">On the Home page, choose the **Ongoing Sales Invoices** tile.</span></span>
2. <span data-ttu-id="85633-135">Opnuð er sölureikningur sem þú vilt kaupa vörur fyrir.</span><span class="sxs-lookup"><span data-stu-id="85633-135">Open a sales invoice that you want to purchase items for.</span></span>
3. <span data-ttu-id="85633-136">Veldu eitt eða fleiri sölureikningslínur sem þú vilt nota á innkaupareikningur.</span><span class="sxs-lookup"><span data-stu-id="85633-136">Select one or more sales invoice lines that you want to use on the purchase invoice.</span></span> <span data-ttu-id="85633-137">Til að nota alla sölureikningslínur, velja annaðhvort í heild eða ekki velja neinar línur.</span><span class="sxs-lookup"><span data-stu-id="85633-137">To use all the sales invoice lines, select either all of them or do not select any lines.</span></span>
4. <span data-ttu-id="85633-138">Velja **stofna innkaupareikning** aðgerð.</span><span class="sxs-lookup"><span data-stu-id="85633-138">Choose the **Create Purchase Invoice** action.</span></span>
5. <span data-ttu-id="85633-139">Veldu annað hvort **Allar línur** eða  **valdar línur** og velja svo **Í lagi** hnappinn.</span><span class="sxs-lookup"><span data-stu-id="85633-139">Select either **All Lines** or **Selected Lines**, and then choose the **OK** button.</span></span>  
6. <span data-ttu-id="85633-140">Í listanum yfir lánardrottna sem birtist skaltu velja lánardrottin sem þú vilt kaupa allar vörurnar af, og þá velja **Í lagi** hnappinn.</span><span class="sxs-lookup"><span data-stu-id="85633-140">In the list of vendors that appears, select the vendor that you want to buy all the items from, and then choose the **OK** button.</span></span>

    <span data-ttu-id="85633-141">Innkaupareikningur er stofnaður með eina, fleiri eða allar línur sölureikningsins.</span><span class="sxs-lookup"><span data-stu-id="85633-141">A purchase invoice is created that contains one, more, or all the lines on the sales invoice.</span></span>
7. <span data-ttu-id="85633-142">Halda áfram að vinna innkaupareikning, til dæmis með því að breyta eða bæta við innkaupareikningslínum.</span><span class="sxs-lookup"><span data-stu-id="85633-142">Proceed to process the purchase invoice, for example, by editing or adding purchase invoice lines.</span></span> <span data-ttu-id="85633-143">Nánari upplýsingar eru í reitnum [Skrá innkaup](purchasing-how-record-purchases.md).</span><span class="sxs-lookup"><span data-stu-id="85633-143">For more information, see [Record Purchases](purchasing-how-record-purchases.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="85633-144">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="85633-144">See Also</span></span>
[<span data-ttu-id="85633-145">Innkaup</span><span class="sxs-lookup"><span data-stu-id="85633-145">Purchasing</span></span>](purchasing-manage-purchasing.md)  
[<span data-ttu-id="85633-146">Skrá innkaup</span><span class="sxs-lookup"><span data-stu-id="85633-146">Record Purchases</span></span>](purchasing-how-record-purchases.md)  
[<span data-ttu-id="85633-147">Reikningsfæra sölur</span><span class="sxs-lookup"><span data-stu-id="85633-147">Invoice Sales</span></span>](sales-how-invoice-sales.md)  
[<span data-ttu-id="85633-148">Skráning nýrra lánardrottna</span><span class="sxs-lookup"><span data-stu-id="85633-148">Register New Vendors</span></span>](purchasing-how-register-new-vendors.md)  
<span data-ttu-id="85633-149">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="85633-149">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

