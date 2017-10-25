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
ms.date: 05/16/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 2d7eb238395a0b1060668996fbbc3e13d9dd8a94
ms.contentlocale: is-is
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-purchase-items-for-a-sale"></a><span data-ttu-id="25854-103">Hvernig á að: Kaupa vörur fyrir sölu.</span><span class="sxs-lookup"><span data-stu-id="25854-103">How to: Purchase Items for a Sale</span></span>
<span data-ttu-id="25854-104">Frá sölupöntunum og sölureikningum geturðu notað aðgerð til stofna á skjótan hátt innkaupaskjöl fyrir vörumagn sem vantar en er krafist við söluna.</span><span class="sxs-lookup"><span data-stu-id="25854-104">From sales orders and sales invoices, you can use functions to quickly create purchase documents for missing item quantities that are required by the sale.</span></span> <span data-ttu-id="25854-105">Hægt er að nota tvær mismunandi aðgerðir, eftir gerð skjalsins.</span><span class="sxs-lookup"><span data-stu-id="25854-105">You can use two different functions depending on the document type.</span></span>
|<span data-ttu-id="25854-106">Virkni</span><span class="sxs-lookup"><span data-stu-id="25854-106">Function</span></span>|<span data-ttu-id="25854-107">Description</span><span class="sxs-lookup"><span data-stu-id="25854-107">Description</span></span>|
|--------|-----------|
|<span data-ttu-id="25854-108">**Stofna innkaupapantanir**</span><span class="sxs-lookup"><span data-stu-id="25854-108">**Create Purchase Orders**</span></span>|<span data-ttu-id="25854-109">Frá sölupöntun, stofnar þessi aðgerð innkaupapöntun fyrir hvern lánardrottinn vöru á sölupöntuninni.</span><span class="sxs-lookup"><span data-stu-id="25854-109">From a sales order, this function creates a purchase order for each vendor of items on the sales order.</span></span> <span data-ttu-id="25854-110">Þú getur breytt innkaupamagninu áður en þú stofnar innkaupapantanirnar.</span><span class="sxs-lookup"><span data-stu-id="25854-110">You can edit the purchase quantity before you create the purchase orders.</span></span> <span data-ttu-id="25854-111">Aðeins er ótiltækt sölumagn lagt til.</span><span class="sxs-lookup"><span data-stu-id="25854-111">Only unavailable sales quantities are suggested.</span></span>
|<span data-ttu-id="25854-112">**Stofna innkaupareikning**</span><span class="sxs-lookup"><span data-stu-id="25854-112">**Create Purchase Invoice**</span></span>|<span data-ttu-id="25854-113">Úr sölupöntun og úr sölureikningi getur þessi aðgerð stofnað innkaupareikning fyrir valinn lánardrottinn fyrir allar línur eða valdar línur í söluskjalinu.</span><span class="sxs-lookup"><span data-stu-id="25854-113">From a sales order and from a sales invoice, this function creates a purchase invoice for a selected vendor for all lines or selected lines on the sales document.</span></span> <span data-ttu-id="25854-114">Lagt er til fullt sölumagn.</span><span class="sxs-lookup"><span data-stu-id="25854-114">The full sales quantity is suggested.</span></span>|

## <a name="to-create-one-or-more-purchase-orders-from-a-sales-order"></a><span data-ttu-id="25854-115">Stofna eina eða fleiri innkaupapöntun úr sölupöntun</span><span class="sxs-lookup"><span data-stu-id="25854-115">To create one or more purchase orders from a sales order</span></span>
<span data-ttu-id="25854-116">Til að stofna innkaupapöntun fyrir hvert ótiltækt vörumagn í sölupöntuninni, notarðu **Stofna innkaupapantanir** aðgerðina.</span><span class="sxs-lookup"><span data-stu-id="25854-116">To create a purchase order for each unavailable item quantity on the sales order, you use the **Create Purchase Orders** function.</span></span> 

> [!NOTE]  
>   <span data-ttu-id="25854-117">Þessi virkni krefst þess að upplifun þín sé stillt á **Suite**.</span><span class="sxs-lookup"><span data-stu-id="25854-117">This functionality requires that your experience is set to **Suite**.</span></span> <span data-ttu-id="25854-118">Nánari upplýsingar, sjá [Sérstilla þína [!INCLUDE[d365fin](includes/d365fin_md.md)] upplifun](ui-experiences.md).</span><span class="sxs-lookup"><span data-stu-id="25854-118">For more information, see [Customizing Your [!INCLUDE[d365fin](includes/d365fin_md.md)] Experience](ui-experiences.md).</span></span>

1. <span data-ttu-id="25854-119">Á heimasíðunni skal velja **áframhaldandi Sölupöntun** gluggareit.</span><span class="sxs-lookup"><span data-stu-id="25854-119">On the Home page, choose the **Ongoing Sales Orders** tile.</span></span>
2. <span data-ttu-id="25854-120">Opnuð er sölupöntun sem þú vilt kaupa vörur fyrir.</span><span class="sxs-lookup"><span data-stu-id="25854-120">Open a sales order that you want to purchase items for.</span></span>
3. <span data-ttu-id="25854-121">Velja **stofna innkaupapantanir** aðgerð.</span><span class="sxs-lookup"><span data-stu-id="25854-121">Choose the **Create Purchase Orders** action.</span></span>

    <span data-ttu-id="25854-122">Glugginn **stofna innkaupapantanir** opnast og birtir eina línu fyrir hverja vöru í sölupöntuninni.</span><span class="sxs-lookup"><span data-stu-id="25854-122">The **Create Purchase Orders** window opens showing a line for each different item on the sales order.</span></span> <span data-ttu-id="25854-123">Línur fyrir bæði fullkomlega tiltækt sölumagn og ótiltækt sölumagn (grámaðar) eru sýndar að sjálfgefnu.</span><span class="sxs-lookup"><span data-stu-id="25854-123">Lines for both fully available sales quantities and unavailable sales quantities (grayed) are shown by default.</span></span> <span data-ttu-id="25854-124">Þú getur valið **sýna ótiltækt** aðgerðina til að sjá aðeins línur fyrir ótiltækt sölumagn.</span><span class="sxs-lookup"><span data-stu-id="25854-124">You can choose the **Show Unavailable** action to only see lines for unavailable sales quantities.</span></span>

    <span data-ttu-id="25854-125">Reiturinn **Magn til innkaupa** inniheldur ótiltækt sölumagn að sjálfgefnu.</span><span class="sxs-lookup"><span data-stu-id="25854-125">The **Quantity to Purchase** field contains the unavailable sales quantity by default.</span></span>
4. <span data-ttu-id="25854-126">Til að kaupa annað magn en ótiltækt sölumagn, skal breyta gildinu í **Magn til innkaupa** reitnum.</span><span class="sxs-lookup"><span data-stu-id="25854-126">To purchase another quantity than the unavailable sales quantity, edit the value in the **Quantity to Purchase** field.</span></span>

    > [!NOTE]  
>   <span data-ttu-id="25854-127">Þú getur líka breytt **Magn til innkaupa** reitnum á grámuðum línum jafnvel þótt þær sýni fullkomlega tiltækt sölumagn.</span><span class="sxs-lookup"><span data-stu-id="25854-127">You can also change the **Quantity to Purchase** field on grayed lines even though they represent fully available sales quantities.</span></span>
5. <span data-ttu-id="25854-128">Velja hnappinn **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="25854-128">Choose the **OK** button.</span></span> 
    
    <span data-ttu-id="25854-129">Innkaupapöntun er stofnuð fyrir hvern lánardrottinn vöru á sölupöntuninni, og í henni eru allar magnbreytingar sem þú kannt að hafa gert í **Stofna innkaupapöntun** glugganum.</span><span class="sxs-lookup"><span data-stu-id="25854-129">A purchase order is created for each vendor of items on the sales order, including any quantity changes that you made in the **Create Purchase Orders** window.</span></span>
7. <span data-ttu-id="25854-130">Halda áfram að vinna innkaupapöntun eða pantanir, til dæmis með því að breyta eða bæta við innkaupareikningslínum.</span><span class="sxs-lookup"><span data-stu-id="25854-130">Proceed to process the purchase order or orders, for example, by editing or adding purchase order lines.</span></span> <span data-ttu-id="25854-131">Nánari upplýsingar eru í [Hvernig á að: Skrá innkaup](purchasing-how-record-purchases.md).</span><span class="sxs-lookup"><span data-stu-id="25854-131">For more information, see [How to: Record Purchases](purchasing-how-record-purchases.md).</span></span>


## <a name="to-create-a-purchase-invoice-from-a-sales-order-or-sales-invoice"></a><span data-ttu-id="25854-132">Stofna innkaupareikning úr sölupöntun eða sölureikningi</span><span class="sxs-lookup"><span data-stu-id="25854-132">To create a purchase invoice from a sales order or sales invoice</span></span>
<span data-ttu-id="25854-133">Til að stofna stakan innkaupareikning fyrir eina eða fleiri línur í söluskjali með því að velja fyrst hvaða lánardrottni skal kaupa af, notarðu **Stofna innkaupareikning** aðgerðina.</span><span class="sxs-lookup"><span data-stu-id="25854-133">To create a single purchase invoice for one or more lines on a sales document by first selecting which vendor to buy from, you use the **Create Purchase Invoice** function.</span></span> 

> [!NOTE]  
>   <span data-ttu-id="25854-134">Þessi aðgerð stofnar innkaupareikning fyrir nákvæmlega það vörumagn sem er á valda söluskjalinu.</span><span class="sxs-lookup"><span data-stu-id="25854-134">This function creates a purchase invoice for the exact item quantity on the selected sales document.</span></span> <span data-ttu-id="25854-135">Til að breyta innkaupamagninu, þarftu að breyta innkaupareikningnum eftir að þú stofnar hann.</span><span class="sxs-lookup"><span data-stu-id="25854-135">To change the purchase quantity, you must edit the purchase invoice after it is created.</span></span>  

1. <span data-ttu-id="25854-136">Í reitnum heimasíða , velja **áframhaldandi Sölupöntun** gluggareit.</span><span class="sxs-lookup"><span data-stu-id="25854-136">On the Home page, choose the **Ongoing Sales Invoices** tile.</span></span>
2. <span data-ttu-id="25854-137">Opnuð er sölureikningur sem þú vilt kaupa vörur fyrir.</span><span class="sxs-lookup"><span data-stu-id="25854-137">Open a sales invoice that you want to purchase items for.</span></span>
3. <span data-ttu-id="25854-138">Veldu eitt eða fleiri sölureikningslínur sem þú vilt nota á innkaupareikningur.</span><span class="sxs-lookup"><span data-stu-id="25854-138">Select one or more sales invoice lines that you want to use on the purchase invoice.</span></span> <span data-ttu-id="25854-139">Til að nota alla sölureikningslínur, velja annaðhvort í heild eða ekki velja neinar línur.</span><span class="sxs-lookup"><span data-stu-id="25854-139">To use all the sales invoice lines, select either all of them or do not select any lines.</span></span>
4. <span data-ttu-id="25854-140">Velja **stofna innkaupareikning** aðgerð.</span><span class="sxs-lookup"><span data-stu-id="25854-140">Choose the **Create Purchase Invoice** action.</span></span>
5. <span data-ttu-id="25854-141">Veldu annað hvort **Allar línur** eða  **valdar línur** og velja svo **Í lagi** hnappinn.</span><span class="sxs-lookup"><span data-stu-id="25854-141">Select either **All Lines** or **Selected Lines**, and then choose the **OK** button.</span></span>  
6. <span data-ttu-id="25854-142">Í listanum yfir lánardrottna sem birtist skaltu velja lánardrottin sem þú vilt kaupa allar vörurnar af, og þá velja **Í lagi** hnappinn.</span><span class="sxs-lookup"><span data-stu-id="25854-142">In the list of vendors that appears, select the vendor that you want to buy all the items from, and then choose the **OK** button.</span></span>

    <span data-ttu-id="25854-143">Innkaupareikningur er stofnaður með eina, fleiri eða allar línur sölureikningsins.</span><span class="sxs-lookup"><span data-stu-id="25854-143">A purchase invoice is created that contains one, more, or all the lines on the sales invoice.</span></span>
7. <span data-ttu-id="25854-144">Halda áfram að vinna innkaupareikning, til dæmis með því að breyta eða bæta við innkaupareikningslínum.</span><span class="sxs-lookup"><span data-stu-id="25854-144">Proceed to process the purchase invoice, for example, by editing or adding purchase invoice lines.</span></span> <span data-ttu-id="25854-145">Nánari upplýsingar eru í [Hvernig á að: Skrá innkaup](purchasing-how-record-purchases.md).</span><span class="sxs-lookup"><span data-stu-id="25854-145">For more information, see [How to: Record Purchases](purchasing-how-record-purchases.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="25854-146">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="25854-146">See Also</span></span>
[<span data-ttu-id="25854-147">Innkaup</span><span class="sxs-lookup"><span data-stu-id="25854-147">Purchasing</span></span>](purchasing-manage-purchasing.md)  
[<span data-ttu-id="25854-148">Hvernig á að skrá kaup</span><span class="sxs-lookup"><span data-stu-id="25854-148">How to: Record Purchases</span></span>](purchasing-how-record-purchases.md)  
[<span data-ttu-id="25854-149">Hvernig er reikningsfært</span><span class="sxs-lookup"><span data-stu-id="25854-149">How to: Invoice Sales</span></span>](sales-how-invoice-sales.md)  
[<span data-ttu-id="25854-150">Hvernig á að Skrá nýja lánardrottna</span><span class="sxs-lookup"><span data-stu-id="25854-150">How to: Register New Vendors</span></span>](purchasing-how-register-new-vendors.md)  
<span data-ttu-id="25854-151">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="25854-151">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

