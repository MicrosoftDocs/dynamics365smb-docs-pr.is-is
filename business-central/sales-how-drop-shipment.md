---
title: Tengja sölupöntun við innkaupapöntun fyrir beina afhendingu | Microsoft Docs
description: Lýsir hvernig á að Búa til sölupöntun sem er tengd við innkaupapöntun til að virkja sendingu beint frá lánardrottni til viðskiptamanns.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: direct shipment
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: c61f55701ecb07862f42d3cce242756001529588
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2020
ms.locfileid: "3193684"
---
# <a name="make-drop-shipments"></a><span data-ttu-id="ea967-103">Beinar sendingar</span><span class="sxs-lookup"><span data-stu-id="ea967-103">Make Drop Shipments</span></span>
<span data-ttu-id="ea967-104">Bein afhending er afhending frá einum af lánardrottnum fyrirtækisins beint til einhvers af viðskiptamönnum fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="ea967-104">A drop shipment is the shipment of items from one of your vendors directly to one of your customers.</span></span>

<span data-ttu-id="ea967-105">Þegar sölupöntun er merkt sem bein afhending og þú býrð til innkaupapöntun sem tilgreinir viðskiptamanninn í reitnum **Sendist til**, **Heimilisfang viðskiptavinar**, geturðu tengt skjölin tvö saman og þar með gefið lánardrottninum fyrirmæli um að afhenda beint til viðskiptavinar.</span><span class="sxs-lookup"><span data-stu-id="ea967-105">When a sales order is marked for drop shipment, and you create a purchase order specifying the customer in the **Ship-to** field, **Customer Address**, you can link the two documents and thereby instruct the vendor to ship directly to the customer.</span></span>
<br><br>  
  
> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4mOyM?rel=0]

## <a name="to-create-a-sales-order-for-drop-shipment"></a><span data-ttu-id="ea967-106">Sölupöntun fyrir beina afhendingu búin til</span><span class="sxs-lookup"><span data-stu-id="ea967-106">To create a sales order for drop shipment</span></span>
<span data-ttu-id="ea967-107">Til að Undirbúa bein afhending, er stofnuð sölupöntun fyrir vöru sem venjulega, nema þarf tilgreina í sölulínunni að salan krefst beinnar sendingar.</span><span class="sxs-lookup"><span data-stu-id="ea967-107">To prepare a drop shipment, you create a sales order for an item as normal, except you must indicate on the sales line that the sale requires drop shipment.</span></span>

1. <span data-ttu-id="ea967-108">Stofnið sölupöntun fyrir vöru.</span><span class="sxs-lookup"><span data-stu-id="ea967-108">Create a sales order for an item.</span></span> <span data-ttu-id="ea967-109">Frekari upplýsingar eru í [Selja vörur](sales-how-sell-products.md).</span><span class="sxs-lookup"><span data-stu-id="ea967-109">For more information, see [Sell Products](sales-how-sell-products.md).</span></span>
2. <span data-ttu-id="ea967-110">Á velta pöntunarlínunni fyrir dropatilboðið skaltu velja hnappinn **Senda sendingu**.</span><span class="sxs-lookup"><span data-stu-id="ea967-110">On the sales order line for the drop shipment, select the **Drop Shipment** check box.</span></span> <span data-ttu-id="ea967-111">Notaðu **Dálkaval** ef svæðið er ekki sýnilegt.</span><span class="sxs-lookup"><span data-stu-id="ea967-111">Use the **Choose Columns** function if the field is not visible.</span></span> <span data-ttu-id="ea967-112">Frekari upplýsingar eru í [Sérstilling verksvæðis](ui-personalization-user.md).</span><span class="sxs-lookup"><span data-stu-id="ea967-112">For more information, see [Personalize Your Workspace](ui-personalization-user.md).</span></span>

## <a name="to-create-the-purchase-order-for-drop-shipment"></a><span data-ttu-id="ea967-113">Innkaupapöntunin stofnuð fyrir beina sendingu</span><span class="sxs-lookup"><span data-stu-id="ea967-113">To create the purchase order for drop shipment</span></span>
<span data-ttu-id="ea967-114">Til að undirbúa beina sendingu fyrir vöru sem á að selja, stofnarðu innkaupapöntun sem venjulega, nema taka þarf fram í innkaupapöntun að senda verði til viðskiptamannsins, ekki til þíns sjálfs.</span><span class="sxs-lookup"><span data-stu-id="ea967-114">To prepare a drop shipment for the item to be sold, you create a purchase order as normal, except you must indicate on the purchase order that it must be shipped to your customer, not to yourself.</span></span>

1. <span data-ttu-id="ea967-115">Stofna innkaupapöntun.</span><span class="sxs-lookup"><span data-stu-id="ea967-115">Create a purchase order.</span></span> <span data-ttu-id="ea967-116">Ekki fylla inn í neina reiti á línunum.</span><span class="sxs-lookup"><span data-stu-id="ea967-116">Do not fill any fields on the lines.</span></span> <span data-ttu-id="ea967-117">Nánari upplýsingar eru í reitnum [Skrá innkaup](purchasing-how-record-purchases.md).</span><span class="sxs-lookup"><span data-stu-id="ea967-117">For more information, see [Record Purchases](purchasing-how-record-purchases.md).</span></span>
2. <span data-ttu-id="ea967-118">Í reitnum **Sendist til** skal velja **Heimilisfang viðskiptavinar**.</span><span class="sxs-lookup"><span data-stu-id="ea967-118">In the **Ship-to** field, select **Customer Address**.</span></span>
3. <span data-ttu-id="ea967-119">Í reitnum **Viðskiptavinur** skal velja viðskiptavininn sem þú ert að selja til.</span><span class="sxs-lookup"><span data-stu-id="ea967-119">In the **Customer** field, select the customer that you are selling to.</span></span>
3. <span data-ttu-id="ea967-120">Veljið aðgerðina **beinar sendingar** og veljið síðan aðgerðina **sækja sölupöntun**.</span><span class="sxs-lookup"><span data-stu-id="ea967-120">Choose the **Drop Shipments** action, and then choose the **Get Sales Order** action.</span></span>
4. <span data-ttu-id="ea967-121">Á síðunni **Sölulisti** er valin sölupöntun sem var útbúin í [Að stofna sölupöntun fyrir beina sendingu](sales-how-drop-shipment.md#to-create-a-sales-order-for-drop-shipment).</span><span class="sxs-lookup"><span data-stu-id="ea967-121">On the **Sales List** page, select the sales order that you prepared in [To create a sales order for drop shipment](sales-how-drop-shipment.md#to-create-a-sales-order-for-drop-shipment).</span></span>
5. <span data-ttu-id="ea967-122">Velja hnappinn **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="ea967-122">Choose the **OK** button.</span></span>

<span data-ttu-id="ea967-123">Línuupplýsingar úr sölupöntun er sett í sölupöntunarlínu(r).</span><span class="sxs-lookup"><span data-stu-id="ea967-123">The line information from the sales order is inserted on the purchase order line(s).</span></span>

<span data-ttu-id="ea967-124">Nú er hægt að segja lánardrottninum aðsenda vörur til viðskiptamanns, til dæmis, með því að póstleggja innkaupapöntun sem er PDF.</span><span class="sxs-lookup"><span data-stu-id="ea967-124">You can now instruct the vendor to ship the items to your customer, for example, by mailing the purchase order as a PDF.</span></span>     

## <a name="to-view-the-linked-purchase-order-from-the-sales-order"></a><span data-ttu-id="ea967-125">Til að skoða tengda innkaupapöntunina úr sölupöntuninni</span><span class="sxs-lookup"><span data-stu-id="ea967-125">To view the linked purchase order from the sales order</span></span>
* <span data-ttu-id="ea967-126">Veldu Sölupöntunarlínu beinnar sendingar, veldu **Pöntun** aðgerð og veldu **Bein sending** aðgerð og síðan er valið aðgerðin **Innkaupapöntun**.</span><span class="sxs-lookup"><span data-stu-id="ea967-126">Select the drop-shipment sales order line, choose the **Order** action, choose the **Drop Shipment** action, and then choose the **Purchase Order** action.</span></span>

## <a name="to-post-a-drop-shipment"></a><span data-ttu-id="ea967-127">Til að bóka beina afhendingu</span><span class="sxs-lookup"><span data-stu-id="ea967-127">To post a drop shipment</span></span>
<span data-ttu-id="ea967-128">Þegar lánardrottinn hefur sent vörur, er hægt að bóka sölupöntunina sem senda.</span><span class="sxs-lookup"><span data-stu-id="ea967-128">After the vendor ships the items, you can post the sales order as shipped.</span></span> <span data-ttu-id="ea967-129">Einnig er hægt að bóka innkaupapöntun, en aðeins með **Móttöku** valkostinn fyrr en sölupöntunin hefur verið reikningsfært.</span><span class="sxs-lookup"><span data-stu-id="ea967-129">You can also post the purchase order, but only with the **Receive** option until the sales order has been invoiced.</span></span>

1. <span data-ttu-id="ea967-130">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Sölupantanir** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="ea967-130">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Orders**, and then choose the related link.</span></span>
2. <span data-ttu-id="ea967-131">Opnaðu sölupöntun sem þú stofnaðir í [Að stofna sölupöntun fyrir beina sendingu]().</span><span class="sxs-lookup"><span data-stu-id="ea967-131">Open the sales order that you created in [To create a sales order for drop shipment]().</span></span>
3. <span data-ttu-id="ea967-132">Í reitnum **magn til Afhendingar** er tilgreint hve mikið af pöntunarmagni skal senda, allt eða hluti pöntunarmagns.</span><span class="sxs-lookup"><span data-stu-id="ea967-132">In the **Qty. to Ship** field, specify how many of the order quantity to ship, the full or a partial order quantity.</span></span>
4. <span data-ttu-id="ea967-133">Veljið aðgerðina **bóka** eða **Bóka og senda**.</span><span class="sxs-lookup"><span data-stu-id="ea967-133">Choose the **Post** or **Post and Send** action.</span></span>
5. <span data-ttu-id="ea967-134">Síðan er annað hvort valið **senda** valkosturinn til að reikningsfæra síðar eða valkostinn **senda og reikningsfæra** eigi að reikningsfæra strax.</span><span class="sxs-lookup"><span data-stu-id="ea967-134">Choose either the **Ship** option to invoice later, or the **Ship and Invoice** option to invoice immediately.</span></span>

## <a name="see-also"></a><span data-ttu-id="ea967-135">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="ea967-135">See Also</span></span>
[<span data-ttu-id="ea967-136">Sérstakar pantanir stofnaðar</span><span class="sxs-lookup"><span data-stu-id="ea967-136">Create Special Orders</span></span>](sales-how-to-create-special-orders.md)  
[<span data-ttu-id="ea967-137">Kaupa vörur fyrir sölu</span><span class="sxs-lookup"><span data-stu-id="ea967-137">Purchase Items for a Sale</span></span>](purchasing-how-purchase-products-sale.md)  
[<span data-ttu-id="ea967-138">Selja vörur</span><span class="sxs-lookup"><span data-stu-id="ea967-138">Sell Products</span></span>](sales-how-sell-products.md)  
[<span data-ttu-id="ea967-139">Skrá innkaup</span><span class="sxs-lookup"><span data-stu-id="ea967-139">Record Purchases</span></span>](purchasing-how-record-purchases.md)  
[<span data-ttu-id="ea967-140">Sala</span><span class="sxs-lookup"><span data-stu-id="ea967-140">Sales</span></span>](sales-manage-sales.md)  
[<span data-ttu-id="ea967-141">Birgðir</span><span class="sxs-lookup"><span data-stu-id="ea967-141">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="ea967-142">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="ea967-142">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
