---
title: Hvernig á að stofna sérpöntun | Microsoft Docs
description: Hægt er að stofna sérpöntun til að tiltekið vörulistaatriði sé sent tilteknum viðskiptamanni. Birgir sendir vöruna í vöruhús og þá má senda hana áfram til viðskiptamanns, annaðhvort sérstaklega eða með annarri pöntun.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: c4549492e118d1b4367e89f2b0169f43ba7f8393
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/17/2020
ms.locfileid: "4748244"
---
# <a name="create-special-orders"></a><span data-ttu-id="56122-104">Sérstakar pantanir stofnaðar</span><span class="sxs-lookup"><span data-stu-id="56122-104">Create Special Orders</span></span>
<span data-ttu-id="56122-105">Hægt er að stofna sérpöntun til að tiltekið vörulistaatriði sé sent tilteknum viðskiptamanni.</span><span class="sxs-lookup"><span data-stu-id="56122-105">You can create a special order for a specific catalog item to be shipped to a specific customer.</span></span> <span data-ttu-id="56122-106">Birgir sendir vöruna í vöruhús og þá má senda hana áfram til viðskiptamanns, annaðhvort sérstaklega eða með annarri pöntun.</span><span class="sxs-lookup"><span data-stu-id="56122-106">Your vendor ships the item to your warehouse and you can then ship the item on to your customer either independently or together with other items on another order.</span></span>  

<span data-ttu-id="56122-107">Sérpantanir gefa til kynna að innkaupa- og sölupöntun séu tengdar til að tryggja að sértækt vörulistaatriði sé tínt og afhent viðskiptamanni.</span><span class="sxs-lookup"><span data-stu-id="56122-107">Special orders imply that the purchase and sales order are linked to ensure that the specific catalog item is picked and delivered to the customer.</span></span>  

<span data-ttu-id="56122-108">Þessa aðgerð er ekki hægt að nota nema búið sé að setja upp spjald fyrir viðskiptamann, lánardrottin og vöru svo hægt sé að vinna pöntunina.</span><span class="sxs-lookup"><span data-stu-id="56122-108">Before you can use this feature, you must first set up the customer, vendor, and item cards necessary for the order.</span></span>  

## <a name="to-create-a-special-order"></a><span data-ttu-id="56122-109">Stofnuð sérpöntun:</span><span class="sxs-lookup"><span data-stu-id="56122-109">To create a special order</span></span>  
1.  <span data-ttu-id="56122-110">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Sölupantanir** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="56122-110">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Order**, and then choose the related link.</span></span>  
2. <span data-ttu-id="56122-111">Valið er aðgerðin **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="56122-111">Choose the **New** action.</span></span> <span data-ttu-id="56122-112">Búin er til ný  sölupöntun fyrir vöruna.</span><span class="sxs-lookup"><span data-stu-id="56122-112">Create and fill in a  sales order for the item.</span></span> <span data-ttu-id="56122-113">Frekari upplýsingar eru í [Selja vörur](sales-how-sell-products.md).</span><span class="sxs-lookup"><span data-stu-id="56122-113">For more information, see [Sell Products](sales-how-sell-products.md).</span></span>
3.  <span data-ttu-id="56122-114">Á flýtiflipanum **Línur** er fyllt út í sölulínuna.</span><span class="sxs-lookup"><span data-stu-id="56122-114">On the **Lines** FastTab, fill in the sales line.</span></span> <span data-ttu-id="56122-115">Í reitnum **Innkaupakóti** veljið innkaupakóta sem er með reitinn **Sérpöntun** valinn.</span><span class="sxs-lookup"><span data-stu-id="56122-115">In the **Purchasing Code** field, select a purchasing code that has the **Special Order** field selected.</span></span>

    <span data-ttu-id="56122-116">Nú þarf að stofna innkaupapöntun út frá innkaupatillögu.</span><span class="sxs-lookup"><span data-stu-id="56122-116">You must now create a purchase order from a requisition worksheet.</span></span>  
4. <span data-ttu-id="56122-117">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Innkaupatillaga** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="56122-117">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Requisition Worksheet**, and then choose the related link.</span></span>  
5. <span data-ttu-id="56122-118">Veljið aðgerðina **Sérpöntun** og veljið síðan aðgerðina **sækja sölupöntun**.</span><span class="sxs-lookup"><span data-stu-id="56122-118">Choose the **Special Order** action, and then choose the **Get Sales Orders** action.</span></span>  
6.  <span data-ttu-id="56122-119">Á síðunni **Sækja sölupantanir** sýna niðurstöður þar sem **Númer fylgiskjals** er sölupöntunarnúmeri.</span><span class="sxs-lookup"><span data-stu-id="56122-119">On the **Get Sales Orders** page, show results where the **Document No.** is the sales order number.</span></span> <span data-ttu-id="56122-120">Velja hnappinn **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="56122-120">Choose the **OK** button.</span></span> <span data-ttu-id="56122-121">Kerfið stofnar innkaupatillögulínu vegna vörunnar.</span><span class="sxs-lookup"><span data-stu-id="56122-121">A requisition worksheet line is created for the item.</span></span>  
7.  <span data-ttu-id="56122-122">Í innkaupatillögulínunni skal velja **Nýtt** í reitnum **Aðgerðarboð**.</span><span class="sxs-lookup"><span data-stu-id="56122-122">On the requisition worksheet line, in the **Action Message** field, select **New**.</span></span>  
8.  <span data-ttu-id="56122-123">Á síðunni **Innkaupatillaga** veljið aðgerðina **Framkvæma aðgerðaboð**.</span><span class="sxs-lookup"><span data-stu-id="56122-123">On the **Req. Worksheet** page, choose the **Carry Out Action Message** action.</span></span> <span data-ttu-id="56122-124">Síðan **Framkv. aðgerðaboð - Beiðni** opnast.</span><span class="sxs-lookup"><span data-stu-id="56122-124">The **Carry Out Action Msg. - Req.** page opens.</span></span> <span data-ttu-id="56122-125">Velja hnappinn **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="56122-125">Choose the **OK** button.</span></span>  

    <span data-ttu-id="56122-126">Þá birtast boð þess efnis að innkaupapantanir hafi verið stofnaðar.</span><span class="sxs-lookup"><span data-stu-id="56122-126">A message appears telling you that the purchase orders have been created.</span></span> <span data-ttu-id="56122-127">Velja hnappinn **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="56122-127">Choost the **OK** button.</span></span>  

<span data-ttu-id="56122-128">Tekið er tillit til stofnaðrar innkaupapöntunar fyrir sérpöntun af kerfinu þar sem hún jafnar framboð og eftirspurn.</span><span class="sxs-lookup"><span data-stu-id="56122-128">A purchase order created as a special order for a sales order is respected by the planning system as it balances demand and supply.</span></span> <span data-ttu-id="56122-129">Það er, innkaupapöntun (framboð) helst tengd við sölupöntun (eftirspurn) jafnvel þó innkaupapöntunin gæti lagt til fyrri eftirspurnar.</span><span class="sxs-lookup"><span data-stu-id="56122-129">That is, the purchase order (supply) remains linked to the sales order (demand), even if that purchase order could supply another earlier demand.</span></span> <span data-ttu-id="56122-130">Nánari upplýsingar eru í [Upplýsingar um hönnun: Endurpöntunarstefnur](design-details-reservation-order-tracking-and-action-messaging.md).</span><span class="sxs-lookup"><span data-stu-id="56122-130">For more information, see [Design Details: Reordering Policies](design-details-reservation-order-tracking-and-action-messaging.md).</span></span>  

> [!NOTE]  
>  <span data-ttu-id="56122-131">Ekki er hægt að nota sérpöntunarkostinn ef varan er þegar frátekin.</span><span class="sxs-lookup"><span data-stu-id="56122-131">You cannot use the special order functionality if the item is already reserved.</span></span> <span data-ttu-id="56122-132">Þess vegna, fyrir vörur sem eru seldar með sérpöntunum, gakktu úr skugga um að **Frátekning** reiturinn á birgðaspjaldinu sé ekki stilltur á **Alltaf**.</span><span class="sxs-lookup"><span data-stu-id="56122-132">Therefore, for items that are sold on special orders, make sure the **Reserve** field on the item card is not set to **Always**.</span></span>  

## <a name="see-also"></a><span data-ttu-id="56122-133">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="56122-133">See Also</span></span>  
[<span data-ttu-id="56122-134">Vinna með vörulista</span><span class="sxs-lookup"><span data-stu-id="56122-134">Work with Catalog Items</span></span>](inventory-how-work-nonstock-items.md)  
[<span data-ttu-id="56122-135">Sala</span><span class="sxs-lookup"><span data-stu-id="56122-135">Sales</span></span>](sales-manage-sales.md)  
<span data-ttu-id="56122-136">[Beinar sendingar](sales-how-drop-shipment.md) </span><span class="sxs-lookup"><span data-stu-id="56122-136">[Make Drop Shipments](sales-how-drop-shipment.md) </span></span>  
[<span data-ttu-id="56122-137">Hönnunarupplýsingar: Endurpöntunarstefnur</span><span class="sxs-lookup"><span data-stu-id="56122-137">Design Details: Reordering Policies</span></span>](design-details-reservation-order-tracking-and-action-messaging.md)  
<span data-ttu-id="56122-138">[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="56122-138">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>
