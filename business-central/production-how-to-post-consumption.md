---
title: Fjöldabóka notkun
description: Ef flæðiaðferðin er stillt á **Handvirk** þarf að bóka íhlutina handvirkt með notkunarbók.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 66a19b624c74ec844806c27c490c300746b46704
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5787903"
---
# <a name="batch-post-production-consumption"></a><span data-ttu-id="1cf32-103">Fjöldabóka framleiðslunotkun</span><span class="sxs-lookup"><span data-stu-id="1cf32-103">Batch Post Production Consumption</span></span>

<span data-ttu-id="1cf32-104">Ef flæðiaðferðin er stillt á **Handvirk** þarf að bóka íhlutina handvirkt með notkunarbók.</span><span class="sxs-lookup"><span data-stu-id="1cf32-104">If the flushing method is **Manual**, you must post the components manually, using a consumption journal.</span></span>  

>[!NOTE]
> <span data-ttu-id="1cf32-105">Ef sett hefur verið gátmerki í reitinn **Krefjast tínslu** á birgðageymsluspjaldinu til að sýna að birgðageymslan krefjist tínsluvinnslu þarf ekki að nota þessa runuvinnslu.</span><span class="sxs-lookup"><span data-stu-id="1cf32-105">If you have placed a check mark in the **Require Pick** field on the location card to indicate that the location requires inventory pick processing, then you do not need to use this batch job.</span></span> [!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="1cf32-106">mun sjá um notkun þegar birgðatínslan er bókuð.</span><span class="sxs-lookup"><span data-stu-id="1cf32-106">will handle consumption when you post the inventory pick.</span></span> <span data-ttu-id="1cf32-107">Frekari upplýsingar eru í [Taka til fyrir framleiðslu eða samsetningu](warehouse-how-to-pick-for-production.md#to-pick-components-in-basic-warehouse-configurations).</span><span class="sxs-lookup"><span data-stu-id="1cf32-107">For more information, see [Pick for Production or Assembly](warehouse-how-to-pick-for-production.md#to-pick-components-in-basic-warehouse-configurations).</span></span> 

<span data-ttu-id="1cf32-108">Einnig er hægt að setja [!INCLUDE[prod_short](includes/prod_short.md)] upp þannig að það bóki sjálfvirkt (*flæða*) íhluti þegar byrjar eða endar framleiðslupantanir.</span><span class="sxs-lookup"><span data-stu-id="1cf32-108">You can also set up [!INCLUDE[prod_short](includes/prod_short.md)] to automatically post (*flush*) components when you start or finish production orders.</span></span> <span data-ttu-id="1cf32-109">Nánari upplýsingar eru í [Leyfa flæði íhluta samkvæmt frálagi aðgerða](production-how-to-flush-components-according-to-operation-output.md).</span><span class="sxs-lookup"><span data-stu-id="1cf32-109">For more information, see [Enable Flushing of Components According to Operation Output](production-how-to-flush-components-according-to-operation-output.md).</span></span>

## <a name="to-post-consumption-for-one-or-more-production-order-lines"></a><span data-ttu-id="1cf32-110">Bóka notkun fyrir eina eða fleiri framleiðslupantanalínur</span><span class="sxs-lookup"><span data-stu-id="1cf32-110">To post consumption for one or more production order lines</span></span>

1.  <span data-ttu-id="1cf32-111">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Notkunarbók** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="1cf32-111">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Consumption Journal**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="1cf32-112">Reitirnir eru fylltir út með framleiðslupöntunargögnunum og notkunargögnunum.</span><span class="sxs-lookup"><span data-stu-id="1cf32-112">Fill in the fields with the production order data and the consumption data.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    <span data-ttu-id="1cf32-113">Notið aðgerðina **Reikna notkun** til að mynda færslubókarlínur úr framleiðslupöntunum sem byggja á raunverulegu frálagi (magni tilbúinnar vöru sem tilkynnt hefur verið um) eða væntanlegu frálagi (magni tilbúinnar vöru sem stefnt er að því að framleiða).</span><span class="sxs-lookup"><span data-stu-id="1cf32-113">Use the **Calc. Consumption** action to generate journal lines from production orders based on the actual output (the quantity of finished goods that you have reported) or on the expected output (the quantity of finished goods that you expect to produce).</span></span>

    > [!NOTE]
    > <span data-ttu-id="1cf32-114">Ef birgðageymsluspjaldið var skilgreint til að krefjast tínsluvinnu vöruhúss, þá má aðeins slá inn magn sem þegar er búið að tína í gegnum vöruhúsaaðgerð í reitinn **Magn** á síðunni **Notkunarbók**, ekki neitt reiknað magn.</span><span class="sxs-lookup"><span data-stu-id="1cf32-114">If you configured the location card to require warehouse pick processing, then only quantities that are already picked through a warehouse activity can be entered in the **Quantity** field in the **Consumption Journal** page, not any calculated quantity.</span></span> <span data-ttu-id="1cf32-115">Frekari upplýsingar eru í [Taka til fyrir framleiðslu eða samsetningu í Grunngerðir vöruhúss](warehouse-how-to-pick-for-internal-operations-in-advanced-warehousing.md)</span><span class="sxs-lookup"><span data-stu-id="1cf32-115">For more information, see [Pick for Production or Assembly in Advanced Warehouse Configurations](warehouse-how-to-pick-for-internal-operations-in-advanced-warehousing.md)</span></span>

3.  <span data-ttu-id="1cf32-116">Velja **Bóka** aðgerðina til að bóka notkunina.</span><span class="sxs-lookup"><span data-stu-id="1cf32-116">Choose the **Post** action to post the consumption.</span></span> <span data-ttu-id="1cf32-117">Tengdar birgðir eru minnkaðar.</span><span class="sxs-lookup"><span data-stu-id="1cf32-117">The related inventories are reduced.</span></span>



## <a name="see-also"></a><span data-ttu-id="1cf32-118">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="1cf32-118">See Also</span></span>

<span data-ttu-id="1cf32-119">[Framleiðsla](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="1cf32-119">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
[<span data-ttu-id="1cf32-120">Uppsetning framleiðslu</span><span class="sxs-lookup"><span data-stu-id="1cf32-120">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="1cf32-121">[Áætlun](production-planning.md)    </span><span class="sxs-lookup"><span data-stu-id="1cf32-121">[Planning](production-planning.md)    </span></span>  
[<span data-ttu-id="1cf32-122">Birgðir</span><span class="sxs-lookup"><span data-stu-id="1cf32-122">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="1cf32-123">Innkaup</span><span class="sxs-lookup"><span data-stu-id="1cf32-123">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="1cf32-124">[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="1cf32-124">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]
