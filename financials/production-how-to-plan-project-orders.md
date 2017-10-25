---
title: "Hvernig á að áætla verkefnispantanir | Microsoft Docs"
description: "Þessi áætlanagerð byrjar í sölupöntun og nýtir gluggann **Áætlun sölupöntunar**. Þegar framleiðslupöntun verkefnis er stofnuð er hægt að skipuleggja hana frekar með því að nota gluggann **Pantanaáætlun**."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 49e3ce0ef80dd54f66565f62616b3b8f2a4aaeaa
ms.contentlocale: is-is
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-plan-project-orders"></a><span data-ttu-id="6e02f-104">Hvernig á að áætla verkefnispantanir</span><span class="sxs-lookup"><span data-stu-id="6e02f-104">How to: Plan Project Orders</span></span>
<span data-ttu-id="6e02f-105">Þessi áætlanagerð byrjar í sölupöntun og nýtir gluggann  **Áætlun sölupöntunar**.</span><span class="sxs-lookup"><span data-stu-id="6e02f-105">This planning task starts from a sales order and uses the **Sales Order Planning** window.</span></span> <span data-ttu-id="6e02f-106">Þegar framleiðslupöntun verkefnis er stofnuð er hægt að skipuleggja hana frekar með því að nota gluggann **Pantanaáætlun**.</span><span class="sxs-lookup"><span data-stu-id="6e02f-106">Once you have created a project production order, you can plan it further by using the **Order Planning** window.</span></span>  

## <a name="to-create-a-project-production-order"></a><span data-ttu-id="6e02f-107">Framleiðslupöntun verkefnis stofnuð</span><span class="sxs-lookup"><span data-stu-id="6e02f-107">To create a project production order</span></span>  

1.  <span data-ttu-id="6e02f-108">Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn  **Sölupantanir** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="6e02f-108">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Sales Orders**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="6e02f-109">Veljið sölupöntunina sem sýnir framleiðsluverkefnið, og veljið síðan aðgerðina **Áætla**.</span><span class="sxs-lookup"><span data-stu-id="6e02f-109">Select the sales order that represents the production project, and then choose the **Planning** action.</span></span>  
4.  <span data-ttu-id="6e02f-110">Í glugganum **Áætlun sölupöntunar** er smellt á aðgerðina **Stofna framl.pöntun**.</span><span class="sxs-lookup"><span data-stu-id="6e02f-110">In the **Sales Order Planning** window, choose  the **Create Prod. Order** action.</span></span>  
5.  <span data-ttu-id="6e02f-111">Í glugganum **Stofna pöntun úr sölu** í reitnum **Tegund pöntunar** er **Verkefnispöntun** valin.</span><span class="sxs-lookup"><span data-stu-id="6e02f-111">In the **Create Order from Sales** window, in the **Order Type** field, select **Project Order**.</span></span>  
6.  <span data-ttu-id="6e02f-112">Velja hnappinn **Já**.</span><span class="sxs-lookup"><span data-stu-id="6e02f-112">Choose the **Yes** button.</span></span>  
7.  <span data-ttu-id="6e02f-113">Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn  **framleiðslupantanir** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="6e02f-113">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Production Orders**, and then choose the related link.</span></span>
8. <span data-ttu-id="6e02f-114">Opna skal nýstofnaða framleiðslupöntun.</span><span class="sxs-lookup"><span data-stu-id="6e02f-114">Open the production order just created.</span></span>  

    <span data-ttu-id="6e02f-115">Athugið að reiturinn **Tegund uppruna** í framleiðslupöntuninni inniheldur **Söluhaus** og hún hefur margar línur, eina fyrir hverja vöru sölulínu sem þarf að framleiða.</span><span class="sxs-lookup"><span data-stu-id="6e02f-115">Notice that the **Source Type** field of the production order contains **Sales Header** and the order has multiple lines, one for each sales line item that must be produced.</span></span>  
9. <span data-ttu-id="6e02f-116">Veldu aðgerðina **Áætlun**.</span><span class="sxs-lookup"><span data-stu-id="6e02f-116">Choose the **Planning** action.</span></span>
10. <span data-ttu-id="6e02f-117">Í glugganum **Pantanaáætlun** er smellt á **Uppfæra** aðgerðina til reikna nýja eftirspurn.</span><span class="sxs-lookup"><span data-stu-id="6e02f-117">In the **Order Planning** window, choose the **Refresh** action to calculate new demand.</span></span>  

<span data-ttu-id="6e02f-118">Pöntunarhausslínan fyrir verkefnispöntunina birtist með allar óuppfylltar eftirspurnarlínur stækkaðar neðan hennar.</span><span class="sxs-lookup"><span data-stu-id="6e02f-118">The order header line for the project order is displayed with all unfulfilled demand lines expanded under it.</span></span> <span data-ttu-id="6e02f-119">Þótt framleiðslupöntunin innihaldi línur fyrir nokkrar framleiddar vörur er heildareftirspurnin fyrir allar framleiðslupöntunarlínur skráð undir einni pöntunarhausslínu í glugganum **Pantanaáætlun**, auk þess sem nafn upprunalega viðskiptamannsins er birt.</span><span class="sxs-lookup"><span data-stu-id="6e02f-119">Although the production order contains lines for several produced items, the total demand for all production order lines is listed under one order header line in the **Order Planning** window, and the original customer name is displayed.</span></span> <span data-ttu-id="6e02f-120">Nú er hægt að áætla eftirspurn eins og lýst er í [Hvernig á að: Áætla nýja eftirspurn pöntun fyrir pöntun](production-how-to-plan-for-new-demand.md).</span><span class="sxs-lookup"><span data-stu-id="6e02f-120">You can now proceed to plan for the demand as described in [How to: Plan for New Demand Order by Order](production-how-to-plan-for-new-demand.md).</span></span>  

> [!NOTE]  
>  <span data-ttu-id="6e02f-121">Eftirspurnarlínur í framleiðslupöntun verkefnisins sem hafa **Framl.pöntun** í reitnum **Áfyllingarkerfi** tákna undirliggjandi framleiðslupantanir.</span><span class="sxs-lookup"><span data-stu-id="6e02f-121">Demand lines in the project production order that have **Prod. Order** in their **Replenishment System** field represent underlying production orders.</span></span> <span data-ttu-id="6e02f-122">Eftir að hafa myndað þessar framleiðslupantanir, þarf að reikna aftur út áætlun í glugganum **Pantanaáætlun** til að auðkenna alla óuppfyllta eftirspurn eftir íhlutum fyrir þær.</span><span class="sxs-lookup"><span data-stu-id="6e02f-122">After you have generated these production orders, you must again calculate a plan in the **Order Planning** window to identify any unfulfilled component demand for them.</span></span> <span data-ttu-id="6e02f-123">Í því tilviki er birtist eftirspurnin í eftirspurnarlínum undir línu í haus venjulegrar framleiðslupöntunar sem þýðir að verkefnistengslin sjást ekki lengur í glugganum.</span><span class="sxs-lookup"><span data-stu-id="6e02f-123">In that case, they are displayed as demand lines under a normal production order header line, meaning, the project relation is no longer visible in the window.</span></span> <span data-ttu-id="6e02f-124">Ef á hinn bóginn notast er við eiginleikann Rekja pöntun er hægt að fara fram og aftur í allar framboðspantanir undir upphaflegu sölupöntuninni.</span><span class="sxs-lookup"><span data-stu-id="6e02f-124">However, if you are using the Order Tracking feature, then you can look back and forth to all supply orders made under the original sales order.</span></span>  

## <a name="see-also"></a><span data-ttu-id="6e02f-125">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="6e02f-125">See Also</span></span>
<span data-ttu-id="6e02f-126">[Áætlun](production-planning.md) </span><span class="sxs-lookup"><span data-stu-id="6e02f-126">[Planning](production-planning.md) </span></span>  
[<span data-ttu-id="6e02f-127">Uppsetning framleiðslu</span><span class="sxs-lookup"><span data-stu-id="6e02f-127">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="6e02f-128">[Framleiðsla](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="6e02f-128">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
[<span data-ttu-id="6e02f-129">Birgðir</span><span class="sxs-lookup"><span data-stu-id="6e02f-129">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="6e02f-130">Innkaup</span><span class="sxs-lookup"><span data-stu-id="6e02f-130">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="6e02f-131">[Hönnunarupplýsingar: framboðsáætlun](design-details-supply-planning.md) </span><span class="sxs-lookup"><span data-stu-id="6e02f-131">[Design Details: Supply Planning](design-details-supply-planning.md) </span></span>  
[<span data-ttu-id="6e02f-132">Uppsetning bestu venja: Framboðsáætlun</span><span class="sxs-lookup"><span data-stu-id="6e02f-132">Setup Best Practices: Supply Planning</span></span>](setup-best-practices-supply-planning.md)  
<span data-ttu-id="6e02f-133">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="6e02f-133">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

