---
title: Tengja sölupöntun við innkaupapöntun fyrir beina afhendingu | Microsoft Docs
description: Lýsir hvernig á að Búa til sölupöntun sem er tengd við innkaupapöntun til að virkja sendingu beint frá lánardrottni til viðskiptamanns.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: direct shipment
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: add7cf9f2f274f50d0e187362b2e0c1bcc2fe8e0
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/01/2020
ms.locfileid: "3926273"
---
# <a name="make-drop-shipments"></a><span data-ttu-id="2841f-103">Beinar sendingar</span><span class="sxs-lookup"><span data-stu-id="2841f-103">Make Drop Shipments</span></span>

<span data-ttu-id="2841f-104">Bein afhending er afhending frá einum af lánardrottnum fyrirtækisins beint til einhvers af viðskiptamönnum fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="2841f-104">A drop shipment is the shipment of items from one of your vendors directly to one of your customers.</span></span>

<span data-ttu-id="2841f-105">Þegar sölupöntun er merkt fyrir beina sendingu og stofnuð er innkaupapöntun sem tilgreinir viðskiptamanninn í reitnum **Sendist til** , **Aðsetur viðskiptamanns** , er hægt að tengja skjölin tvö til að segja lánardrottni að senda beint til viðskiptamannsins.</span><span class="sxs-lookup"><span data-stu-id="2841f-105">When a sales order is marked for drop shipment, and you create a purchase order specifying the customer in the **Ship-to** field, **Customer Address** , you can link the two documents to instruct the vendor to ship directly to the customer.</span></span>
<br><br>  
  
> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4mOyM?rel=0]

## <a name="to-create-a-sales-order-for-drop-shipment"></a><span data-ttu-id="2841f-106">Sölupöntun fyrir beina afhendingu búin til</span><span class="sxs-lookup"><span data-stu-id="2841f-106">To create a sales order for drop shipment</span></span>

<span data-ttu-id="2841f-107">Til að undirbúa beina sendingu, er stofnuð sölupöntun fyrir vöru og tilgreina í sölulínunni að salan krefst beinnar sendingar.</span><span class="sxs-lookup"><span data-stu-id="2841f-107">To prepare a drop shipment, you create a sales order for an item and indicate on the sales line that the sale requires drop shipment.</span></span>

1. <span data-ttu-id="2841f-108">Stofnið sölupöntun fyrir vöru.</span><span class="sxs-lookup"><span data-stu-id="2841f-108">Create a sales order for an item.</span></span> <span data-ttu-id="2841f-109">Frekari upplýsingar eru í [Selja vörur](sales-how-sell-products.md).</span><span class="sxs-lookup"><span data-stu-id="2841f-109">For more information, see [Sell Products](sales-how-sell-products.md).</span></span>
2. <span data-ttu-id="2841f-110">Á velta pöntunarlínunni fyrir dropatilboðið skaltu velja hnappinn **Senda sendingu** .</span><span class="sxs-lookup"><span data-stu-id="2841f-110">On the sales order line for the drop shipment, select the **Drop Shipment** check box.</span></span> <span data-ttu-id="2841f-111">Notaðu **Dálkaval** ef svæðið er ekki sýnilegt.</span><span class="sxs-lookup"><span data-stu-id="2841f-111">Use the **Choose Columns** function if the field is not visible.</span></span> <span data-ttu-id="2841f-112">Frekari upplýsingar eru í [Sérstilling verksvæðis](ui-personalization-user.md).</span><span class="sxs-lookup"><span data-stu-id="2841f-112">For more information, see [Personalize Your Workspace](ui-personalization-user.md).</span></span>

## <a name="to-create-the-purchase-order-for-drop-shipment"></a><span data-ttu-id="2841f-113">Innkaupapöntunin stofnuð fyrir beina sendingu</span><span class="sxs-lookup"><span data-stu-id="2841f-113">To create the purchase order for drop shipment</span></span>

<span data-ttu-id="2841f-114">Til að undirbúa beina sendingu, skal tilgreina í innkaupapöntuninni að senda þarf hana til viðskiptamannsins, ekki til þín.</span><span class="sxs-lookup"><span data-stu-id="2841f-114">To prepare a drop shipment, you indicate on the purchase order that it must be shipped to your customer, not to yourself.</span></span>

1. <span data-ttu-id="2841f-115">Stofna innkaupapöntun.</span><span class="sxs-lookup"><span data-stu-id="2841f-115">Create a purchase order.</span></span> <span data-ttu-id="2841f-116">Ekki fylla inn í neina reiti á línunum.</span><span class="sxs-lookup"><span data-stu-id="2841f-116">Do not fill any fields on the lines.</span></span> <span data-ttu-id="2841f-117">Nánari upplýsingar eru í reitnum [Skrá innkaup](purchasing-how-record-purchases.md).</span><span class="sxs-lookup"><span data-stu-id="2841f-117">For more information, see [Record Purchases](purchasing-how-record-purchases.md).</span></span>
2. <span data-ttu-id="2841f-118">Í reitnum **Sendist til** skal velja **Heimilisfang viðskiptavinar** .</span><span class="sxs-lookup"><span data-stu-id="2841f-118">In the **Ship-to** field, select **Customer Address** .</span></span>
3. <span data-ttu-id="2841f-119">Í reitnum **Viðskiptavinur** skal velja viðskiptavininn sem þú ert að selja til.</span><span class="sxs-lookup"><span data-stu-id="2841f-119">In the **Customer** field, select the customer that you are selling to.</span></span>
4. <span data-ttu-id="2841f-120">Veljið aðgerðina **beinar sendingar** og veljið síðan aðgerðina **sækja sölupöntun** .</span><span class="sxs-lookup"><span data-stu-id="2841f-120">Choose the **Drop Shipments** action, and then choose the **Get Sales Order** action.</span></span>
5. <span data-ttu-id="2841f-121">Á síðunni **Sölulisti** er valin sölupöntun sem var útbúin í [Að stofna sölupöntun fyrir beina sendingu](sales-how-drop-shipment.md#to-create-a-sales-order-for-drop-shipment).</span><span class="sxs-lookup"><span data-stu-id="2841f-121">On the **Sales List** page, select the sales order that you prepared in [To create a sales order for drop shipment](sales-how-drop-shipment.md#to-create-a-sales-order-for-drop-shipment).</span></span>
6. <span data-ttu-id="2841f-122">Velja hnappinn **Í lagi** .</span><span class="sxs-lookup"><span data-stu-id="2841f-122">Choose the **OK** button.</span></span>

<span data-ttu-id="2841f-123">Línuupplýsingar úr sölupöntun er sett í sölupöntunarlínu(r).</span><span class="sxs-lookup"><span data-stu-id="2841f-123">The line information from the sales order is inserted on the purchase order line(s).</span></span>

<span data-ttu-id="2841f-124">Nú er hægt að segja lánardrottninum aðsenda vörur til viðskiptamanns, til dæmis, með því að póstleggja innkaupapöntun sem er PDF.</span><span class="sxs-lookup"><span data-stu-id="2841f-124">You can now instruct the vendor to ship the items to your customer, for example, by mailing the purchase order as a PDF.</span></span>     

## <a name="to-create-multiple-purchase-orders-for-drop-shipments"></a><span data-ttu-id="2841f-125">Að stofna margar innkaupapantanir fyrir beinar sendingar</span><span class="sxs-lookup"><span data-stu-id="2841f-125">To create multiple purchase orders for drop shipments</span></span>

<span data-ttu-id="2841f-126">Einnig er hægt að nota innkaupatillögublað til að stofna innkaupapöntunina fyrir lánardrottin.</span><span class="sxs-lookup"><span data-stu-id="2841f-126">You can also use the requisition worksheet to create the purchase order for the vendor.</span></span> <span data-ttu-id="2841f-127">Kosturinn við að nota innkaupatillögublaðið er sá að hægt er að stofna innkaupapantanir fyrir allar útistandandi beinar sendingar þannig að ekki þarf að stofna hverja þeirra fyrir sig.</span><span class="sxs-lookup"><span data-stu-id="2841f-127">The advantage of using the requisition worksheet is that it can create purchase orders for all outstanding drop shipments, so you don't have to create each one individually.</span></span>

1. <span data-ttu-id="2841f-128">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Innkaupatillögublöð** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="2841f-128">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Requistion Worksheets** , and then choose the related link.</span></span>
2. <span data-ttu-id="2841f-129">Veljið aðgerðina **beinar sendingar** og veljið síðan aðgerðina **sækja sölupöntun** .</span><span class="sxs-lookup"><span data-stu-id="2841f-129">Choose the **Drop Shipments** action, and then choose the **Get Sales Order** action.</span></span>
3. <span data-ttu-id="2841f-130">Velja hnappinn **Í lagi** .</span><span class="sxs-lookup"><span data-stu-id="2841f-130">Choose the **OK** button.</span></span>
4. <span data-ttu-id="2841f-131">Yfirfara innkaupapöntunarlínur, og í reitnum **Lánardrottnanr.** skal velja lánardrottin sem veitir nauðsynlegar vörur.</span><span class="sxs-lookup"><span data-stu-id="2841f-131">Review the purchase order lines, and in the **Vendor No.** field, select vendor that supplies required goods.</span></span> 
5. <span data-ttu-id="2841f-132">Veljið aðgerðina **Framkvæma aðgerðaboð** til að færa yfirfarnar línur í innkaupapöntun.</span><span class="sxs-lookup"><span data-stu-id="2841f-132">Choose the **Carry Out Action Message** action to convert reviewed lines to a purchase order.</span></span>

## <a name="to-view-the-linked-purchase-order-from-the-sales-order"></a><span data-ttu-id="2841f-133">Til að skoða tengda innkaupapöntunina úr sölupöntuninni</span><span class="sxs-lookup"><span data-stu-id="2841f-133">To view the linked purchase order from the sales order</span></span>

* <span data-ttu-id="2841f-134">Veldu Sölupöntunarlínu beinnar sendingar, veldu **Pöntun** aðgerð og veldu **Bein sending** aðgerð og síðan er valið aðgerðin **Innkaupapöntun** .</span><span class="sxs-lookup"><span data-stu-id="2841f-134">Select the drop-shipment sales order line, choose the **Order** action, choose the **Drop Shipment** action, and then choose the **Purchase Order** action.</span></span>

## <a name="to-post-a-drop-shipment"></a><span data-ttu-id="2841f-135">Til að bóka beina afhendingu</span><span class="sxs-lookup"><span data-stu-id="2841f-135">To post a drop shipment</span></span>

<span data-ttu-id="2841f-136">Þegar lánardrottinn hefur sent vörur, er hægt að bóka sölupöntunina sem senda.</span><span class="sxs-lookup"><span data-stu-id="2841f-136">After the vendor ships the items, you can post the sales order as shipped.</span></span> <span data-ttu-id="2841f-137">Einnig er hægt að bóka innkaupapöntun, en aðeins með **Móttöku** valkostinn fyrr en sölupöntunin hefur verið reikningsfært.</span><span class="sxs-lookup"><span data-stu-id="2841f-137">You can also post the purchase order, but only with the **Receive** option until the sales order has been invoiced.</span></span>

1. <span data-ttu-id="2841f-138">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Sölupantanir** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="2841f-138">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Orders** , and then choose the related link.</span></span>
2. <span data-ttu-id="2841f-139">Opnaðu sölupöntun sem þú stofnaðir í [Að stofna sölupöntun fyrir beina sendingu](#to-create-a-sales-order-for-drop-shipment).</span><span class="sxs-lookup"><span data-stu-id="2841f-139">Open the sales order that you created in [To create a sales order for drop shipment](#to-create-a-sales-order-for-drop-shipment).</span></span>
3. <span data-ttu-id="2841f-140">Í reitnum **magn til Afhendingar** er tilgreint hve mikið af pöntunarmagni skal senda, allt eða hluti pöntunarmagns.</span><span class="sxs-lookup"><span data-stu-id="2841f-140">In the **Qty. to Ship** field, specify how many of the order quantity to ship, the full or a partial order quantity.</span></span>
4. <span data-ttu-id="2841f-141">Veljið aðgerðina **bóka** eða **Bóka og senda** .</span><span class="sxs-lookup"><span data-stu-id="2841f-141">Choose the **Post** or **Post and Send** action.</span></span>
5. <span data-ttu-id="2841f-142">Síðan er annað hvort valið **senda** valkosturinn til að reikningsfæra síðar eða valkostinn **senda og reikningsfæra** eigi að reikningsfæra strax.</span><span class="sxs-lookup"><span data-stu-id="2841f-142">Choose either the **Ship** option to invoice later, or the **Ship and Invoice** option to invoice immediately.</span></span>

## <a name="see-also"></a><span data-ttu-id="2841f-143">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="2841f-143">See Also</span></span>

[<span data-ttu-id="2841f-144">Sérstakar pantanir stofnaðar</span><span class="sxs-lookup"><span data-stu-id="2841f-144">Create Special Orders</span></span>](sales-how-to-create-special-orders.md)  
[<span data-ttu-id="2841f-145">Kaupa vörur fyrir sölu</span><span class="sxs-lookup"><span data-stu-id="2841f-145">Purchase Items for a Sale</span></span>](purchasing-how-purchase-products-sale.md)  
[<span data-ttu-id="2841f-146">Selja vörur</span><span class="sxs-lookup"><span data-stu-id="2841f-146">Sell Products</span></span>](sales-how-sell-products.md)  
[<span data-ttu-id="2841f-147">Skrá innkaup</span><span class="sxs-lookup"><span data-stu-id="2841f-147">Record Purchases</span></span>](purchasing-how-record-purchases.md)  
[<span data-ttu-id="2841f-148">Sala</span><span class="sxs-lookup"><span data-stu-id="2841f-148">Sales</span></span>](sales-manage-sales.md)  
[<span data-ttu-id="2841f-149">Birgðir</span><span class="sxs-lookup"><span data-stu-id="2841f-149">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="2841f-150">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="2841f-150">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
