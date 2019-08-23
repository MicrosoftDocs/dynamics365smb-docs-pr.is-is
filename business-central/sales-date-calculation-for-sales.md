---
title: Dagsetning útreiknings fyrir sölu | Microsoft Docs
description: Forritið reiknar sjálfkrafa daginn sem verður að panta vöru svo hún sé til í birgðum á tilteknum degi. Þetta er dagsetningin sem vænta má þess að vara sem pöntuð er á tilteknum degi verði tiltæk til tínslu.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 927c16f0fb1d12ff1202e4e675b97078d354375f
ms.sourcegitcommit: 8c0d734c7202fec81da79c7db382243aa49e37f6
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/10/2019
ms.locfileid: "1737121"
---
# <a name="date-calculation-for-sales"></a><span data-ttu-id="ac2ce-104">Dagsetning útreiknings fyrir sölu.</span><span class="sxs-lookup"><span data-stu-id="ac2ce-104">Date Calculation for Sales</span></span>
[!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="ac2ce-105">reiknar sjálfkrafa út hvenær hægt er að afhenda vöru á sölupöntunarlínu í fyrsta lagi.</span><span class="sxs-lookup"><span data-stu-id="ac2ce-105">automatically calculates the earliest possible date that an item on a sales order line can be shipped.</span></span>

<span data-ttu-id="ac2ce-106">Hafi viðskiptamaðurinn farið fram á tiltekna afgreiðsludagsetningu þá er reiknuð út sú dagsetning sem vörurnar þurfa að vera tilbúnar þannig að afgreiðsla geti farið fram á þeim degi.</span><span class="sxs-lookup"><span data-stu-id="ac2ce-106">If the customer has requested a specific delivery date, then the date on which the items must be available to pick to meet that delivery date is calculated.</span></span>

<span data-ttu-id="ac2ce-107">Hafi viðskiptamaðurinn ekki farið fram á tiltekna afgreiðsludagsetningu þá er dagsetning sem hægt er að afgreiða vörurnar reiknuð út frá deginum sem vörurnar verða tilbúnar.</span><span class="sxs-lookup"><span data-stu-id="ac2ce-107">If the customer does not request a specific delivery date, then the date on which the items can be delivered is calculated, starting from the date on which the items are available for picking.</span></span>

## <a name="calculating-a-requested-delivery-date"></a><span data-ttu-id="ac2ce-108">Reiknar ósk um afhendingardag</span><span class="sxs-lookup"><span data-stu-id="ac2ce-108">Calculating a Requested Delivery Date</span></span>
<span data-ttu-id="ac2ce-109">Ef tilgreind er umbeðin afgreiðsludagsetning á sölupöntunarlínunni verður þessi dagsetning að upphafspunkti fyrir eftirfarandi útreikninga.</span><span class="sxs-lookup"><span data-stu-id="ac2ce-109">If you specify a requested delivery date on the sales order line, that date becomes the starting point for the following calculations.</span></span>

- <span data-ttu-id="ac2ce-110">Umbeðin afgreiðsludagsetning – Flutningstími = Áætluð afhendingardagsetning</span><span class="sxs-lookup"><span data-stu-id="ac2ce-110">requested delivery date - shipping time = planned shipment date</span></span>
- <span data-ttu-id="ac2ce-111">sfhendingardagsetning + afgr.tími vara á útl. úr vöruh. = afh.dags.</span><span class="sxs-lookup"><span data-stu-id="ac2ce-111">planned shipment date - outbound whse. handling time = shipment date</span></span>

<span data-ttu-id="ac2ce-112">Ef varan er tiltæk til tínslu á afhendingardagsetningu þá getur söluferlið haldið áfram.</span><span class="sxs-lookup"><span data-stu-id="ac2ce-112">If the items are available to pick on the shipment date, then the sales process can continue.</span></span> <span data-ttu-id="ac2ce-113">Annars birtist viðvörun um að vara sé uppseld.</span><span class="sxs-lookup"><span data-stu-id="ac2ce-113">Otherwise, a stock-out warning is displayed.</span></span>

> [!Note]
> <span data-ttu-id="ac2ce-114">Ef ferlið þitt er byggt á útreikningi aftur í tímann, t.d. ef þú notar umbeðna afhendingardagsetningu til að fá áætlaða sendingardagsetningu ráðleggjum við þér að þú notir dagsetningarreiknireglur sem eru með fastri tímalengd á borði við „5D“ fyrir fimm daga eða „1V“ fyrir eina viku.</span><span class="sxs-lookup"><span data-stu-id="ac2ce-114">If your process is based on backward calculation, for example, if you use the requested delivery date to get the planned shipment date, we recommend that you use date formulas that have fixed durations, such as "5D" for five days or "1W" for one week.</span></span> <span data-ttu-id="ac2ce-115">Dagsetningarreiknireglur án fastra tímalengda, t.d „NV“ fyrir núverandi viku eða „NM“ fyrir núverandi mánuð, getur leitt til rangra útreikninga á dagsetningum.</span><span class="sxs-lookup"><span data-stu-id="ac2ce-115">Date formulas without fixed durations, such as "CW" for current week or CM for current month, can result in incorrect date calculations.</span></span> <span data-ttu-id="ac2ce-116">Frekari upplýsingar er að finna í [Vinna með dagsetningar og tíma í dagatali](ui-enter-date-ranges.md).</span><span class="sxs-lookup"><span data-stu-id="ac2ce-116">For more information about date formulas, see [Working with Calendar Dates and Times](ui-enter-date-ranges.md).</span></span>

## <a name="calculating-the-earliest-possible-delivery-date"></a><span data-ttu-id="ac2ce-117">Reiknar fyrsta mögulega afgreiðsludag</span><span class="sxs-lookup"><span data-stu-id="ac2ce-117">Calculating the Earliest Possible Delivery Date</span></span>
<span data-ttu-id="ac2ce-118">Ef ekki er tilgreind umbeðin afgreiðsludagsetning á sölupöntunarlínunni, eða ef ekki er hægt að verða við umbeðinni afgreiðsludagsetningu, er reiknuð fyrsta dagsetningin sem vörurnar eru tiltækar.</span><span class="sxs-lookup"><span data-stu-id="ac2ce-118">If you do not specify a requested delivery date on the sales order line, or if the requested delivery date cannot be met, then the earliest date on which that the items are available is calculated.</span></span> <span data-ttu-id="ac2ce-119">Sú dagsetning er færð inn í reitinn Afhendingardagsetning á línuna og eftirtaldar reiknireglur eru síðan notaðar til að reikna út hvenær áætlað er að senda vörurnar ásamt því á hvaða degi viðskiptamaðurinn fær þær afhentar.</span><span class="sxs-lookup"><span data-stu-id="ac2ce-119">That date is then entered in the Shipment Date field on the line, and the date on which you plan to ship the items as well as the date on which they will be delivered to the customer are calculated using the following formulas.</span></span>

- <span data-ttu-id="ac2ce-120">Afhendingardagsetning + afgr.tími vara á útl. úr vöruh. = Áætluð afhendingardagsetning</span><span class="sxs-lookup"><span data-stu-id="ac2ce-120">shipment date + outbound whse. handling time = planned shipment date</span></span>
- <span data-ttu-id="ac2ce-121">áætluð afhendingardagsetning + flutningstími = áætluð afgreiðsludagsetning</span><span class="sxs-lookup"><span data-stu-id="ac2ce-121">planned shipment date + shipping time = planned delivery date</span></span>


## <a name="see-also"></a><span data-ttu-id="ac2ce-122">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="ac2ce-122">See Also</span></span>  
 <span data-ttu-id="ac2ce-123">[Dagsetning útreiknings fyrir kaup.](purchasing-date-calculation-for-purchases.md) </span><span class="sxs-lookup"><span data-stu-id="ac2ce-123">[Date Calculation for Purchases](purchasing-date-calculation-for-purchases.md) </span></span>  
 [<span data-ttu-id="ac2ce-124">Reikna dagsetningar pöntunarloforða</span><span class="sxs-lookup"><span data-stu-id="ac2ce-124">Calculate Order Promising Dates</span></span>](sales-how-to-calculate-order-promising-dates.md)  
 <span data-ttu-id="ac2ce-125">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="ac2ce-125">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
