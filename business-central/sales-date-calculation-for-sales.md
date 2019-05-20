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
ms.openlocfilehash: a620b7ed9d06cdd8adf7b12bea2b55aecea32bcc
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/29/2019
ms.locfileid: "1251128"
---
# <a name="date-calculation-for-sales"></a><span data-ttu-id="4d2fe-104">Dagsetning útreiknings fyrir sölu.</span><span class="sxs-lookup"><span data-stu-id="4d2fe-104">Date Calculation for Sales</span></span>
[!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="4d2fe-105">reiknar sjálfkrafa út hvenær hægt er að afhenda vöru á sölupöntunarlínu í fyrsta lagi.</span><span class="sxs-lookup"><span data-stu-id="4d2fe-105">automatically calculates the earliest possible date that an item on a sales order line can be shipped.</span></span>

<span data-ttu-id="4d2fe-106">Hafi viðskiptamaðurinn farið fram á tiltekna afgreiðsludagsetningu þá er reiknuð út sú dagsetning sem vörurnar þurfa að vera tilbúnar þannig að afgreiðsla geti farið fram á þeim degi.</span><span class="sxs-lookup"><span data-stu-id="4d2fe-106">If the customer has requested a specific delivery date, then the date on which the items must be available to pick to meet that delivery date is calculated.</span></span>

<span data-ttu-id="4d2fe-107">Hafi viðskiptamaðurinn ekki farið fram á tiltekna afgreiðsludagsetningu þá er dagsetning sem hægt er að afgreiða vörurnar reiknuð út frá deginum sem vörurnar verða tilbúnar.</span><span class="sxs-lookup"><span data-stu-id="4d2fe-107">If the customer does not request a specific delivery date, then the date on which the items can be delivered is calculated, starting from the date on which the items are available for picking.</span></span>

## <a name="calculating-a-requested-delivery-date"></a><span data-ttu-id="4d2fe-108">Reiknar ósk um afhendingardag</span><span class="sxs-lookup"><span data-stu-id="4d2fe-108">Calculating a Requested Delivery Date</span></span>
<span data-ttu-id="4d2fe-109">Ef tilgreindur er afgreiðsludagsetning á sölupöntunarlínunni notar forritið þessa dagsetningu sem upphafspunkt fyrir eftirfarandi útreikninga.</span><span class="sxs-lookup"><span data-stu-id="4d2fe-109">If you specify a requested delivery date on the sales order line, then that date is used as the starting point for the following calculations.</span></span>

- <span data-ttu-id="4d2fe-110">Umbeðin afgreiðsludagsetning – Flutningstími = Áætluð afhendingardagsetning</span><span class="sxs-lookup"><span data-stu-id="4d2fe-110">requested delivery date - shipping time = planned shipment date</span></span>
- <span data-ttu-id="4d2fe-111">sfhendingardagsetning + afgr.tími vara á útl. úr vöruh. = afh.dags.</span><span class="sxs-lookup"><span data-stu-id="4d2fe-111">planned shipment date - outbound whse. handling time = shipment date</span></span>

<span data-ttu-id="4d2fe-112">Ef varan er tiltæk til tínslu á afhendingardagsetningu þá getur söluferlið haldið áfram.</span><span class="sxs-lookup"><span data-stu-id="4d2fe-112">If the items are available to pick on the shipment date, then the sales process can continue.</span></span>

<span data-ttu-id="4d2fe-113">Ef varan er ekki tiltæk til tínslu á afhendingardegi þá birtist viðvörun um að varan sé uppseld.</span><span class="sxs-lookup"><span data-stu-id="4d2fe-113">If the items are not available to be picked on the shipment date, then a stock-out warning is displayed.</span></span>

## <a name="calculating-the-earliest-possible-delivery-date"></a><span data-ttu-id="4d2fe-114">Reiknar fyrsta mögulega afgreiðsludag</span><span class="sxs-lookup"><span data-stu-id="4d2fe-114">Calculating the Earliest Possible Delivery Date</span></span>
<span data-ttu-id="4d2fe-115">Ef ekki er tilgreind umbeðin afgreiðsludagsetning á sölupöntunarlínunni, eða ef ekki er hægt að verða við umbeðinni afgreiðsludagsetningu, er reiknuð fyrsta dagsetningin sem vörurnar eru tiltækar.</span><span class="sxs-lookup"><span data-stu-id="4d2fe-115">If you do not specify a requested delivery date on the sales order line, or if the requested delivery date cannot be met, then the earliest date on which that the items are available is calculated.</span></span> <span data-ttu-id="4d2fe-116">Sú dagsetning er færð inn í reitinn Afhendingardagsetning á línuna og eftirtaldar reiknireglur eru síðan notaðar til að reikna út hvenær áætlað er að senda vörurnar ásamt því á hvaða degi viðskiptamaðurinn fær þær afhentar.</span><span class="sxs-lookup"><span data-stu-id="4d2fe-116">That date is then entered in the Shipment Date field on the line, and the date on which you plan to ship the items as well as the date on which they will be delivered to the customer are calculated using the following formulas.</span></span>

- <span data-ttu-id="4d2fe-117">Afhendingardagsetning + afgr.tími vara á útl. úr vöruh. = Áætluð afhendingardagsetning</span><span class="sxs-lookup"><span data-stu-id="4d2fe-117">shipment date + outbound whse. handling time = planned shipment date</span></span>
- <span data-ttu-id="4d2fe-118">áætluð afhendingardagsetning + flutningstími = áætluð afgreiðsludagsetning</span><span class="sxs-lookup"><span data-stu-id="4d2fe-118">planned shipment date + shipping time = planned delivery date</span></span>


## <a name="see-also"></a><span data-ttu-id="4d2fe-119">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="4d2fe-119">See Also</span></span>  
 <span data-ttu-id="4d2fe-120">[Dagsetning útreiknings fyrir kaup.](purchasing-date-calculation-for-purchases.md) </span><span class="sxs-lookup"><span data-stu-id="4d2fe-120">[Date Calculation for Purchases](purchasing-date-calculation-for-purchases.md) </span></span>  
 [<span data-ttu-id="4d2fe-121">Reikna dagsetningar pöntunarloforða</span><span class="sxs-lookup"><span data-stu-id="4d2fe-121">Calculate Order Promising Dates</span></span>](sales-how-to-calculate-order-promising-dates.md)  
 <span data-ttu-id="4d2fe-122">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="4d2fe-122">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
