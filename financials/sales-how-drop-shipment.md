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
ms.date: 03/29/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 977debf7386ad1113ef54147b20fd24c7c285a78
ms.contentlocale: is-is
ms.lasthandoff: 09/11/2017

---
# <a name="how-to-make-drop-shipments"></a><span data-ttu-id="586fa-103">Hvernig á að: Gera beinar afhendingar</span><span class="sxs-lookup"><span data-stu-id="586fa-103">How to: Make Drop Shipments</span></span>
<span data-ttu-id="586fa-104">Bein afhending er afhending frá einum af lánardrottnum fyrirtækisins beint til einhvers af viðskiptamönnum fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="586fa-104">A drop shipment is the shipment of items from one of your vendors directly to one of your customers.</span></span>

<span data-ttu-id="586fa-105">Þegar sölupöntun er merkt fyrir bein sending og þú býrð til innkaupapöntun sem tilgreinir viðskiptamaður í reitnum **Selt-til-Viðskm.nr.**</span><span class="sxs-lookup"><span data-stu-id="586fa-105">When a sales order is marked for drop shipment, and you create a purchase order specifying the customer in the **Sell-to Customer No.**</span></span> <span data-ttu-id="586fa-106">Sviði, getur þú tengt tvö skjöl og þar með leiðbeint seljanda um að senda beint til viðskiptavinarins.</span><span class="sxs-lookup"><span data-stu-id="586fa-106">field, you can link the two documents and thereby instruct the vendor to ship directly to the customer.</span></span>

## <a name="to-create-a-sales-order-for-drop-shipment"></a><span data-ttu-id="586fa-107">Sölupöntun fyrir beina afhendingu búin til</span><span class="sxs-lookup"><span data-stu-id="586fa-107">To create a sales order for drop shipment</span></span>
<span data-ttu-id="586fa-108">Til að Undirbúa bein afhending, er stofnuð sölupöntun fyrir vöru sem venjulega, nema þarf tilgreina í sölulínunni að salan krefst beinnar sendingar.</span><span class="sxs-lookup"><span data-stu-id="586fa-108">To prepare a drop shipment, you create a sales order for an item as normal, except you must indicate on the sales line that the sale requires drop shipment.</span></span>

1. <span data-ttu-id="586fa-109">Stofnið sölupöntun fyrir vöru.</span><span class="sxs-lookup"><span data-stu-id="586fa-109">Create a sales order for an item.</span></span> <span data-ttu-id="586fa-110">Nánari upplýsingar eru í [Hvernig á að: selja vörur.](sales-how-sell-products.md)</span><span class="sxs-lookup"><span data-stu-id="586fa-110">For more information, see [How to: Sell Products](sales-how-sell-products.md).</span></span>
2. <span data-ttu-id="586fa-111">Á velta pöntunarlínunni fyrir dropatilboðið skaltu velja hnappinn **Senda sendingu**.</span><span class="sxs-lookup"><span data-stu-id="586fa-111">On the sales order line for the drop shipment, select the **Drop Shipment** check box.</span></span> <span data-ttu-id="586fa-112">Notaðu **Dálkaval** ef svæðið er ekki sýnilegt.</span><span class="sxs-lookup"><span data-stu-id="586fa-112">Use the **Choose Columns** function if the field is not visible.</span></span> <span data-ttu-id="586fa-113">Nánari upplýsingar er að finna í [Sérstillingar notanda](ui-user-personalization.md).</span><span class="sxs-lookup"><span data-stu-id="586fa-113">For more information, see [User Personalization](ui-user-personalization.md).</span></span>

> [!NOTE]  
>   <span data-ttu-id="586fa-114">Þessi virkni krefst þess að upplifun þín sé stillt á **Pakki**.</span><span class="sxs-lookup"><span data-stu-id="586fa-114">This functionality requires that your experience is set to **Suite**.</span></span> <span data-ttu-id="586fa-115">Nánari upplýsingar, sjá [Sérstilla þína [!INCLUDE[d365fin](includes/d365fin_md.md)] upplifun](ui-experiences.md).</span><span class="sxs-lookup"><span data-stu-id="586fa-115">For more information, see [Customizing Your [!INCLUDE[d365fin](includes/d365fin_md.md)] Experience](ui-experiences.md).</span></span>

## <a name="to-create-the-purchase-order-for-drop-shipment"></a><span data-ttu-id="586fa-116">Innkaupapöntunin stofnuð fyrir beina sendingu</span><span class="sxs-lookup"><span data-stu-id="586fa-116">To create the purchase order for drop shipment</span></span>
<span data-ttu-id="586fa-117">Til að undirbúa beina sendingu fyrir vöru sem á að selja, stofnarðu innkaupapöntun sem venjulega, nema taka þarf fram í innkaupapöntun að senda verði til viðskiptamannsins, ekki til þíns sjálfs.</span><span class="sxs-lookup"><span data-stu-id="586fa-117">To prepare a drop shipment for the item to be sold, you create a purchase order as normal, except you must indicate on the purchase order that it must be shipped to your customer, not to yourself.</span></span>

1. <span data-ttu-id="586fa-118">Stofna innkaupapöntun.</span><span class="sxs-lookup"><span data-stu-id="586fa-118">Create a purchase order.</span></span> <span data-ttu-id="586fa-119">Ekki fylla inn í neina reiti á línunum.</span><span class="sxs-lookup"><span data-stu-id="586fa-119">Do not fill any fields on the lines.</span></span> <span data-ttu-id="586fa-120">Nánari upplýsingar eru í [Hvernig á að: Skrá innkaup](purchasing-how-record-purchases.md).</span><span class="sxs-lookup"><span data-stu-id="586fa-120">For more information, see [How to: Record Purchases](purchasing-how-record-purchases.md).</span></span>
2. <span data-ttu-id="586fa-121">Í reitnum **Selt til Viðskm.nr.**.</span><span class="sxs-lookup"><span data-stu-id="586fa-121">In the **Sell-to Customer No.**</span></span> <span data-ttu-id="586fa-122">er valinn viðskiptamaður sem selt er til.</span><span class="sxs-lookup"><span data-stu-id="586fa-122">field, select the customer that you are selling to.</span></span>
3. <span data-ttu-id="586fa-123">Veljið aðgerðina **beinar sendingar** og veljið síðan aðgerðina **sækja sölupöntun**.</span><span class="sxs-lookup"><span data-stu-id="586fa-123">Choose the **Drop Shipments** action, and then choose the **Get Sales Order** action.</span></span>
4. <span data-ttu-id="586fa-124">Í **Sölulisti** glugganum er valin sölupöntun sem var útbúin í "stofna sölupöntun fyrir beina sendingu" hlutanum.</span><span class="sxs-lookup"><span data-stu-id="586fa-124">In the **Sales List** window, select the sales order that you prepared in the "To create a sales order for drop shipment" section.</span></span>
5. <span data-ttu-id="586fa-125">Velja hnappinn **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="586fa-125">Choose the **OK** button.</span></span>

<span data-ttu-id="586fa-126">Línuupplýsingar úr sölupöntun er sett í sölupöntunarlínu(r).</span><span class="sxs-lookup"><span data-stu-id="586fa-126">The line information from the sales order is inserted on the purchase order line(s).</span></span>

<span data-ttu-id="586fa-127">Nú er hægt að segja lánardrottninum aðsenda vörur til viðskiptamanns, til dæmis, með því að póstleggja innkaupapöntun sem er PDF.</span><span class="sxs-lookup"><span data-stu-id="586fa-127">You can now instruct the vendor to ship the items to your customer, for example, by mailing the purchase order as a PDF.</span></span>     

## <a name="to-view-the-linked-purchase-order-from-the-sales-order"></a><span data-ttu-id="586fa-128">Til að skoða tengda innkaupapöntunina úr sölupöntuninni</span><span class="sxs-lookup"><span data-stu-id="586fa-128">To view the linked purchase order from the sales order</span></span>
* <span data-ttu-id="586fa-129">Veldu Sölupöntunarlínu beinnar sendingar, veldu **Pöntun** aðgerð og veldu **Bein sending** aðgerð og síðan er valið aðgerðin **Innkaupapöntun**.</span><span class="sxs-lookup"><span data-stu-id="586fa-129">Select the drop-shipment sales order line, choose the **Order** action, choose the **Drop Shipment** action, and then choose the **Purchase Order** action.</span></span>

## <a name="to-post-a-drop-shipment"></a><span data-ttu-id="586fa-130">Til að bóka beina afhendingu</span><span class="sxs-lookup"><span data-stu-id="586fa-130">To post a drop shipment</span></span>
<span data-ttu-id="586fa-131">Þegar lánardrottinn hefur sent vörur, er hægt að bóka sölupöntunina sem senda.</span><span class="sxs-lookup"><span data-stu-id="586fa-131">After the vendor ships the items, you can post the sales order as shipped.</span></span> <span data-ttu-id="586fa-132">Einnig er hægt að bóka innkaupapöntun, en aðeins með **Móttöku** valkostinn fyrr en sölupöntunin hefur verið reikningsfært.</span><span class="sxs-lookup"><span data-stu-id="586fa-132">You can also post the purchase order, but only with the **Receive** option until the sales order has been invoiced.</span></span>

1. <span data-ttu-id="586fa-133">Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Sölupantanir** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="586fa-133">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Sales orders**, and then choose the related link.</span></span>
2. <span data-ttu-id="586fa-134">Opnaðu sölupöntun sem þú stofnaðir í "stofna sölupöntun fyrir beina sendingu" hlutanum.</span><span class="sxs-lookup"><span data-stu-id="586fa-134">Open the sales order that you created in the "To create a sales order for a drop shipment" section.</span></span>
3. <span data-ttu-id="586fa-135">Í reitnum **magn til Afhendingar** er tilgreint hve mikið af pöntunarmagni skal senda, allt eða hluti pöntunarmagns.</span><span class="sxs-lookup"><span data-stu-id="586fa-135">In the **Qty. to Ship** field, specify how many of the order quantity to ship, the full or a partial order quantity.</span></span>
4. <span data-ttu-id="586fa-136">Veljið aðgerðina **bóka** eða **Bóka og senda**.</span><span class="sxs-lookup"><span data-stu-id="586fa-136">Choose the **Post** or **Post and Send** action.</span></span>
5. <span data-ttu-id="586fa-137">Síðan er annað hvort valið **senda** valkosturinn til að reikningsfæra síðar eða valkostinn **senda og reikningsfæra** eigi að reikningsfæra strax.</span><span class="sxs-lookup"><span data-stu-id="586fa-137">Choose either the **Ship** option to invoice later, or the **Ship and Invoice** option to invoice immediately.</span></span>

## <a name="see-also"></a><span data-ttu-id="586fa-138">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="586fa-138">See Also</span></span>
[<span data-ttu-id="586fa-139">Hvernig á að: Selja vörur</span><span class="sxs-lookup"><span data-stu-id="586fa-139">How to: Sell Products</span></span>](sales-how-sell-products.md)  
[<span data-ttu-id="586fa-140">Hvernig á að skrá kaup</span><span class="sxs-lookup"><span data-stu-id="586fa-140">How to: Record Purchases</span></span>](purchasing-how-record-purchases.md)  
[<span data-ttu-id="586fa-141">Sala</span><span class="sxs-lookup"><span data-stu-id="586fa-141">Sales</span></span>](sales-manage-sales.md)  
[<span data-ttu-id="586fa-142">Birgðir</span><span class="sxs-lookup"><span data-stu-id="586fa-142">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="586fa-143">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="586fa-143">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

