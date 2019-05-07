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
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 7a87023445ea10aa19cc0cc4f60d76ce4cf3e365
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2019
ms.locfileid: "929360"
---
# <a name="make-drop-shipments"></a><span data-ttu-id="3d82c-103">Beinar sendingar</span><span class="sxs-lookup"><span data-stu-id="3d82c-103">Make Drop Shipments</span></span>
<span data-ttu-id="3d82c-104">Bein afhending er afhending frá einum af lánardrottnum fyrirtækisins beint til einhvers af viðskiptamönnum fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="3d82c-104">A drop shipment is the shipment of items from one of your vendors directly to one of your customers.</span></span>

<span data-ttu-id="3d82c-105">Þegar sölupöntun er merkt fyrir bein sending og þú býrð til innkaupapöntun sem tilgreinir viðskiptamaður í reitnum **Selt-til-Viðskm.nr.**</span><span class="sxs-lookup"><span data-stu-id="3d82c-105">When a sales order is marked for drop shipment, and you create a purchase order specifying the customer in the **Sell-to Customer No.**</span></span> <span data-ttu-id="3d82c-106">Sviði, getur þú tengt tvö skjöl og þar með leiðbeint seljanda um að senda beint til viðskiptavinarins.</span><span class="sxs-lookup"><span data-stu-id="3d82c-106">field, you can link the two documents and thereby instruct the vendor to ship directly to the customer.</span></span>

## <a name="to-create-a-sales-order-for-drop-shipment"></a><span data-ttu-id="3d82c-107">Sölupöntun fyrir beina afhendingu búin til</span><span class="sxs-lookup"><span data-stu-id="3d82c-107">To create a sales order for drop shipment</span></span>
<span data-ttu-id="3d82c-108">Til að Undirbúa bein afhending, er stofnuð sölupöntun fyrir vöru sem venjulega, nema þarf tilgreina í sölulínunni að salan krefst beinnar sendingar.</span><span class="sxs-lookup"><span data-stu-id="3d82c-108">To prepare a drop shipment, you create a sales order for an item as normal, except you must indicate on the sales line that the sale requires drop shipment.</span></span>

1. <span data-ttu-id="3d82c-109">Stofnið sölupöntun fyrir vöru.</span><span class="sxs-lookup"><span data-stu-id="3d82c-109">Create a sales order for an item.</span></span> <span data-ttu-id="3d82c-110">Frekari upplýsingar eru í [Selja vörur](sales-how-sell-products.md).</span><span class="sxs-lookup"><span data-stu-id="3d82c-110">For more information, see [Sell Products](sales-how-sell-products.md).</span></span>
2. <span data-ttu-id="3d82c-111">Á velta pöntunarlínunni fyrir dropatilboðið skaltu velja hnappinn **Senda sendingu**.</span><span class="sxs-lookup"><span data-stu-id="3d82c-111">On the sales order line for the drop shipment, select the **Drop Shipment** check box.</span></span> <span data-ttu-id="3d82c-112">Notaðu **Dálkaval** ef svæðið er ekki sýnilegt.</span><span class="sxs-lookup"><span data-stu-id="3d82c-112">Use the **Choose Columns** function if the field is not visible.</span></span> <span data-ttu-id="3d82c-113">Frekari upplýsingar eru í [Sérstilling vinnusvæðisins þíns](ui-personalization-user.md).</span><span class="sxs-lookup"><span data-stu-id="3d82c-113">For more information, see [Personalizing Your Workspace](ui-personalization-user.md).</span></span>

## <a name="to-create-the-purchase-order-for-drop-shipment"></a><span data-ttu-id="3d82c-114">Innkaupapöntunin stofnuð fyrir beina sendingu</span><span class="sxs-lookup"><span data-stu-id="3d82c-114">To create the purchase order for drop shipment</span></span>
<span data-ttu-id="3d82c-115">Til að undirbúa beina sendingu fyrir vöru sem á að selja, stofnarðu innkaupapöntun sem venjulega, nema taka þarf fram í innkaupapöntun að senda verði til viðskiptamannsins, ekki til þíns sjálfs.</span><span class="sxs-lookup"><span data-stu-id="3d82c-115">To prepare a drop shipment for the item to be sold, you create a purchase order as normal, except you must indicate on the purchase order that it must be shipped to your customer, not to yourself.</span></span>

1. <span data-ttu-id="3d82c-116">Stofna innkaupapöntun.</span><span class="sxs-lookup"><span data-stu-id="3d82c-116">Create a purchase order.</span></span> <span data-ttu-id="3d82c-117">Ekki fylla inn í neina reiti á línunum.</span><span class="sxs-lookup"><span data-stu-id="3d82c-117">Do not fill any fields on the lines.</span></span> <span data-ttu-id="3d82c-118">Nánari upplýsingar eru í reitnum [Skrá innkaup](purchasing-how-record-purchases.md).</span><span class="sxs-lookup"><span data-stu-id="3d82c-118">For more information, see [Record Purchases](purchasing-how-record-purchases.md).</span></span>
2. <span data-ttu-id="3d82c-119">Í reitnum **Selt til Viðskm.nr.**.</span><span class="sxs-lookup"><span data-stu-id="3d82c-119">In the **Sell-to Customer No.**</span></span> <span data-ttu-id="3d82c-120">er valinn viðskiptamaður sem selt er til.</span><span class="sxs-lookup"><span data-stu-id="3d82c-120">field, select the customer that you are selling to.</span></span>
3. <span data-ttu-id="3d82c-121">Veljið aðgerðina **beinar sendingar** og veljið síðan aðgerðina **sækja sölupöntun**.</span><span class="sxs-lookup"><span data-stu-id="3d82c-121">Choose the **Drop Shipments** action, and then choose the **Get Sales Order** action.</span></span>
4. <span data-ttu-id="3d82c-122">Á síðunni **Sölulisti** er valin sölupöntun sem var útbúin í [Að stofna sölupöntun fyrir beina sendingu](sales-how-drop-shipment.md#to-create-a-sales-order-for-drop-shipment).</span><span class="sxs-lookup"><span data-stu-id="3d82c-122">On the **Sales List** page, select the sales order that you prepared in [To create a sales order for drop shipment](sales-how-drop-shipment.md#to-create-a-sales-order-for-drop-shipment).</span></span>
5. <span data-ttu-id="3d82c-123">Velja hnappinn **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="3d82c-123">Choose the **OK** button.</span></span>

<span data-ttu-id="3d82c-124">Línuupplýsingar úr sölupöntun er sett í sölupöntunarlínu(r).</span><span class="sxs-lookup"><span data-stu-id="3d82c-124">The line information from the sales order is inserted on the purchase order line(s).</span></span>

<span data-ttu-id="3d82c-125">Nú er hægt að segja lánardrottninum aðsenda vörur til viðskiptamanns, til dæmis, með því að póstleggja innkaupapöntun sem er PDF.</span><span class="sxs-lookup"><span data-stu-id="3d82c-125">You can now instruct the vendor to ship the items to your customer, for example, by mailing the purchase order as a PDF.</span></span>     

## <a name="to-view-the-linked-purchase-order-from-the-sales-order"></a><span data-ttu-id="3d82c-126">Til að skoða tengda innkaupapöntunina úr sölupöntuninni</span><span class="sxs-lookup"><span data-stu-id="3d82c-126">To view the linked purchase order from the sales order</span></span>
* <span data-ttu-id="3d82c-127">Veldu Sölupöntunarlínu beinnar sendingar, veldu **Pöntun** aðgerð og veldu **Bein sending** aðgerð og síðan er valið aðgerðin **Innkaupapöntun**.</span><span class="sxs-lookup"><span data-stu-id="3d82c-127">Select the drop-shipment sales order line, choose the **Order** action, choose the **Drop Shipment** action, and then choose the **Purchase Order** action.</span></span>

## <a name="to-post-a-drop-shipment"></a><span data-ttu-id="3d82c-128">Til að bóka beina afhendingu</span><span class="sxs-lookup"><span data-stu-id="3d82c-128">To post a drop shipment</span></span>
<span data-ttu-id="3d82c-129">Þegar lánardrottinn hefur sent vörur, er hægt að bóka sölupöntunina sem senda.</span><span class="sxs-lookup"><span data-stu-id="3d82c-129">After the vendor ships the items, you can post the sales order as shipped.</span></span> <span data-ttu-id="3d82c-130">Einnig er hægt að bóka innkaupapöntun, en aðeins með **Móttöku** valkostinn fyrr en sölupöntunin hefur verið reikningsfært.</span><span class="sxs-lookup"><span data-stu-id="3d82c-130">You can also post the purchase order, but only with the **Receive** option until the sales order has been invoiced.</span></span>

1. <span data-ttu-id="3d82c-131">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Sölupantanir** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="3d82c-131">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Orders**, and then choose the related link.</span></span>
2. <span data-ttu-id="3d82c-132">Opnaðu sölupöntun sem þú stofnaðir í [Að stofna sölupöntun fyrir beina sendingu]().</span><span class="sxs-lookup"><span data-stu-id="3d82c-132">Open the sales order that you created in [To create a sales order for drop shipment]().</span></span>
3. <span data-ttu-id="3d82c-133">Í reitnum **magn til Afhendingar** er tilgreint hve mikið af pöntunarmagni skal senda, allt eða hluti pöntunarmagns.</span><span class="sxs-lookup"><span data-stu-id="3d82c-133">In the **Qty. to Ship** field, specify how many of the order quantity to ship, the full or a partial order quantity.</span></span>
4. <span data-ttu-id="3d82c-134">Veljið aðgerðina **bóka** eða **Bóka og senda**.</span><span class="sxs-lookup"><span data-stu-id="3d82c-134">Choose the **Post** or **Post and Send** action.</span></span>
5. <span data-ttu-id="3d82c-135">Síðan er annað hvort valið **senda** valkosturinn til að reikningsfæra síðar eða valkostinn **senda og reikningsfæra** eigi að reikningsfæra strax.</span><span class="sxs-lookup"><span data-stu-id="3d82c-135">Choose either the **Ship** option to invoice later, or the **Ship and Invoice** option to invoice immediately.</span></span>

## <a name="see-also"></a><span data-ttu-id="3d82c-136">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="3d82c-136">See Also</span></span>
[<span data-ttu-id="3d82c-137">Sérstakar pantanir stofnaðar</span><span class="sxs-lookup"><span data-stu-id="3d82c-137">Create Special Orders</span></span>](sales-how-to-create-special-orders.md)  
[<span data-ttu-id="3d82c-138">Kaupa vörur fyrir sölu</span><span class="sxs-lookup"><span data-stu-id="3d82c-138">Purchase Items for a Sale</span></span>](purchasing-how-purchase-products-sale.md)  
[<span data-ttu-id="3d82c-139">Selja vörur</span><span class="sxs-lookup"><span data-stu-id="3d82c-139">Sell Products</span></span>](sales-how-sell-products.md)  
[<span data-ttu-id="3d82c-140">Skrá innkaup</span><span class="sxs-lookup"><span data-stu-id="3d82c-140">Record Purchases</span></span>](purchasing-how-record-purchases.md)  
[<span data-ttu-id="3d82c-141">Sala</span><span class="sxs-lookup"><span data-stu-id="3d82c-141">Sales</span></span>](sales-manage-sales.md)  
[<span data-ttu-id="3d82c-142">Birgðir</span><span class="sxs-lookup"><span data-stu-id="3d82c-142">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="3d82c-143">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="3d82c-143">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
