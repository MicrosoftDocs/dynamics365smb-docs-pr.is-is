---
title: "Stofna sölupöntun sem er tengd við innkaupapöntun fyrir beina afhendingu | Microsoft Docs"
description: "Lýsir hvernig á að Búa til sölupöntun sem er tengd við innkaupapöntun til að virkja sendingu beint frá lánardrottni til viðskiptamanns."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: direct shipment
ms.date: 01/25/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 087ead3b0a28d09cd687c1fcb60f6fee2c914c4a
ms.contentlocale: is-is
ms.lasthandoff: 01/30/2018

---
# <a name="make-drop-shipments"></a><span data-ttu-id="22957-103">Beinar sendingar</span><span class="sxs-lookup"><span data-stu-id="22957-103">Make Drop Shipments</span></span>
<span data-ttu-id="22957-104">Bein afhending er afhending frá einum af lánardrottnum fyrirtækisins beint til einhvers af viðskiptamönnum fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="22957-104">A drop shipment is the shipment of items from one of your vendors directly to one of your customers.</span></span>

<span data-ttu-id="22957-105">Þegar sölupöntun er merkt fyrir bein sending og þú býrð til innkaupapöntun sem tilgreinir viðskiptamaður í reitnum **Selt-til-Viðskm.nr.**</span><span class="sxs-lookup"><span data-stu-id="22957-105">When a sales order is marked for drop shipment, and you create a purchase order specifying the customer in the **Sell-to Customer No.**</span></span> <span data-ttu-id="22957-106">Sviði, getur þú tengt tvö skjöl og þar með leiðbeint seljanda um að senda beint til viðskiptavinarins.</span><span class="sxs-lookup"><span data-stu-id="22957-106">field, you can link the two documents and thereby instruct the vendor to ship directly to the customer.</span></span>

## <a name="to-create-a-sales-order-for-drop-shipment"></a><span data-ttu-id="22957-107">Sölupöntun fyrir beina afhendingu búin til</span><span class="sxs-lookup"><span data-stu-id="22957-107">To create a sales order for drop shipment</span></span>
<span data-ttu-id="22957-108">Til að Undirbúa bein afhending, er stofnuð sölupöntun fyrir vöru sem venjulega, nema þarf tilgreina í sölulínunni að salan krefst beinnar sendingar.</span><span class="sxs-lookup"><span data-stu-id="22957-108">To prepare a drop shipment, you create a sales order for an item as normal, except you must indicate on the sales line that the sale requires drop shipment.</span></span>

1. <span data-ttu-id="22957-109">Stofnið sölupöntun fyrir vöru.</span><span class="sxs-lookup"><span data-stu-id="22957-109">Create a sales order for an item.</span></span> <span data-ttu-id="22957-110">Frekari upplýsingar eru í [Selja vörur](sales-how-sell-products.md).</span><span class="sxs-lookup"><span data-stu-id="22957-110">For more information, see [Sell Products](sales-how-sell-products.md).</span></span>
2. <span data-ttu-id="22957-111">Á velta pöntunarlínunni fyrir dropatilboðið skaltu velja hnappinn **Senda sendingu**.</span><span class="sxs-lookup"><span data-stu-id="22957-111">On the sales order line for the drop shipment, select the **Drop Shipment** check box.</span></span> <span data-ttu-id="22957-112">Notaðu **Dálkaval** ef svæðið er ekki sýnilegt.</span><span class="sxs-lookup"><span data-stu-id="22957-112">Use the **Choose Columns** function if the field is not visible.</span></span> <span data-ttu-id="22957-113">Frekari upplýsingar eru í [Sérstilling vinnusvæðisins þíns](ui-personalization-user.md).</span><span class="sxs-lookup"><span data-stu-id="22957-113">For more information, see [Personalizing Your Workspace](ui-personalization-user.md).</span></span>

## <a name="to-create-the-purchase-order-for-drop-shipment"></a><span data-ttu-id="22957-114">Innkaupapöntunin stofnuð fyrir beina sendingu</span><span class="sxs-lookup"><span data-stu-id="22957-114">To create the purchase order for drop shipment</span></span>
<span data-ttu-id="22957-115">Til að undirbúa beina sendingu fyrir vöru sem á að selja, stofnarðu innkaupapöntun sem venjulega, nema taka þarf fram í innkaupapöntun að senda verði til viðskiptamannsins, ekki til þíns sjálfs.</span><span class="sxs-lookup"><span data-stu-id="22957-115">To prepare a drop shipment for the item to be sold, you create a purchase order as normal, except you must indicate on the purchase order that it must be shipped to your customer, not to yourself.</span></span>

1. <span data-ttu-id="22957-116">Stofna innkaupapöntun.</span><span class="sxs-lookup"><span data-stu-id="22957-116">Create a purchase order.</span></span> <span data-ttu-id="22957-117">Ekki fylla inn í neina reiti á línunum.</span><span class="sxs-lookup"><span data-stu-id="22957-117">Do not fill any fields on the lines.</span></span> <span data-ttu-id="22957-118">Nánari upplýsingar eru í reitnum [Skrá innkaup](purchasing-how-record-purchases.md).</span><span class="sxs-lookup"><span data-stu-id="22957-118">For more information, see [Record Purchases](purchasing-how-record-purchases.md).</span></span>
2. <span data-ttu-id="22957-119">Í reitnum **Selt til Viðskm.nr.**.</span><span class="sxs-lookup"><span data-stu-id="22957-119">In the **Sell-to Customer No.**</span></span> <span data-ttu-id="22957-120">er valinn viðskiptamaður sem selt er til.</span><span class="sxs-lookup"><span data-stu-id="22957-120">field, select the customer that you are selling to.</span></span>
3. <span data-ttu-id="22957-121">Veljið aðgerðina **beinar sendingar** og veljið síðan aðgerðina **sækja sölupöntun**.</span><span class="sxs-lookup"><span data-stu-id="22957-121">Choose the **Drop Shipments** action, and then choose the **Get Sales Order** action.</span></span>
4. <span data-ttu-id="22957-122">Í **Sölulisti** glugganum er valin sölupöntun sem var útbúin í "stofna sölupöntun fyrir beina sendingu" hlutanum.</span><span class="sxs-lookup"><span data-stu-id="22957-122">In the **Sales List** window, select the sales order that you prepared in the "To create a sales order for drop shipment" section.</span></span>
5. <span data-ttu-id="22957-123">Velja hnappinn **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="22957-123">Choose the **OK** button.</span></span>

<span data-ttu-id="22957-124">Línuupplýsingar úr sölupöntun er sett í sölupöntunarlínu(r).</span><span class="sxs-lookup"><span data-stu-id="22957-124">The line information from the sales order is inserted on the purchase order line(s).</span></span>

<span data-ttu-id="22957-125">Nú er hægt að segja lánardrottninum aðsenda vörur til viðskiptamanns, til dæmis, með því að póstleggja innkaupapöntun sem er PDF.</span><span class="sxs-lookup"><span data-stu-id="22957-125">You can now instruct the vendor to ship the items to your customer, for example, by mailing the purchase order as a PDF.</span></span>     

## <a name="to-view-the-linked-purchase-order-from-the-sales-order"></a><span data-ttu-id="22957-126">Til að skoða tengda innkaupapöntunina úr sölupöntuninni</span><span class="sxs-lookup"><span data-stu-id="22957-126">To view the linked purchase order from the sales order</span></span>
* <span data-ttu-id="22957-127">Veldu Sölupöntunarlínu beinnar sendingar, veldu **Pöntun** aðgerð og veldu **Bein sending** aðgerð og síðan er valið aðgerðin **Innkaupapöntun**.</span><span class="sxs-lookup"><span data-stu-id="22957-127">Select the drop-shipment sales order line, choose the **Order** action, choose the **Drop Shipment** action, and then choose the **Purchase Order** action.</span></span>

## <a name="to-post-a-drop-shipment"></a><span data-ttu-id="22957-128">Til að bóka beina afhendingu</span><span class="sxs-lookup"><span data-stu-id="22957-128">To post a drop shipment</span></span>
<span data-ttu-id="22957-129">Þegar lánardrottinn hefur sent vörur, er hægt að bóka sölupöntunina sem senda.</span><span class="sxs-lookup"><span data-stu-id="22957-129">After the vendor ships the items, you can post the sales order as shipped.</span></span> <span data-ttu-id="22957-130">Einnig er hægt að bóka innkaupapöntun, en aðeins með **Móttöku** valkostinn fyrr en sölupöntunin hefur verið reikningsfært.</span><span class="sxs-lookup"><span data-stu-id="22957-130">You can also post the purchase order, but only with the **Receive** option until the sales order has been invoiced.</span></span>

1. <span data-ttu-id="22957-131">Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Sölupantanir** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="22957-131">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Sales orders**, and then choose the related link.</span></span>
2. <span data-ttu-id="22957-132">Opnaðu sölupöntun sem þú stofnaðir í "stofna sölupöntun fyrir beina sendingu" hlutanum.</span><span class="sxs-lookup"><span data-stu-id="22957-132">Open the sales order that you created in the "To create a sales order for a drop shipment" section.</span></span>
3. <span data-ttu-id="22957-133">Í reitnum **magn til Afhendingar** er tilgreint hve mikið af pöntunarmagni skal senda, allt eða hluti pöntunarmagns.</span><span class="sxs-lookup"><span data-stu-id="22957-133">In the **Qty. to Ship** field, specify how many of the order quantity to ship, the full or a partial order quantity.</span></span>
4. <span data-ttu-id="22957-134">Veljið aðgerðina **bóka** eða **Bóka og senda**.</span><span class="sxs-lookup"><span data-stu-id="22957-134">Choose the **Post** or **Post and Send** action.</span></span>
5. <span data-ttu-id="22957-135">Síðan er annað hvort valið **senda** valkosturinn til að reikningsfæra síðar eða valkostinn **senda og reikningsfæra** eigi að reikningsfæra strax.</span><span class="sxs-lookup"><span data-stu-id="22957-135">Choose either the **Ship** option to invoice later, or the **Ship and Invoice** option to invoice immediately.</span></span>

## <a name="see-also"></a><span data-ttu-id="22957-136">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="22957-136">See Also</span></span>
<span data-ttu-id="22957-137">[Sérstakar pantanir stofnaðar](sales-how-to-create-special-orders.md)|</span><span class="sxs-lookup"><span data-stu-id="22957-137">[Create Special Orders](sales-how-to-create-special-orders.md)|</span></span>  
[<span data-ttu-id="22957-138">Selja vörur</span><span class="sxs-lookup"><span data-stu-id="22957-138">Sell Products</span></span>](sales-how-sell-products.md)  
[<span data-ttu-id="22957-139">Skrá innkaup</span><span class="sxs-lookup"><span data-stu-id="22957-139">Record Purchases</span></span>](purchasing-how-record-purchases.md)  
[<span data-ttu-id="22957-140">Sala</span><span class="sxs-lookup"><span data-stu-id="22957-140">Sales</span></span>](sales-manage-sales.md)  
[<span data-ttu-id="22957-141">Birgðir</span><span class="sxs-lookup"><span data-stu-id="22957-141">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="22957-142">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="22957-142">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

