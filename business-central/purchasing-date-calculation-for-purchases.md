---
title: Dagsetning útreiknings fyrir kaup | Microsoft Docs
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
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: 08d2f6498019b8ee0a646cec891ff897a62dc9de
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/08/2019
ms.locfileid: "800276"
---
# <a name="date-calculation-for-purchases"></a><span data-ttu-id="89b1f-104">Dagsetning útreiknings fyrir kaup.</span><span class="sxs-lookup"><span data-stu-id="89b1f-104">Date Calculation for Purchases</span></span>
[!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="89b1f-105">reiknar sjálfkrafa daginn sem verður að panta vöru svo hún sé til í birgðum á tilteknum degi.</span><span class="sxs-lookup"><span data-stu-id="89b1f-105">automatically calculates the date on which you must order an item to have it in inventory on a certain date.</span></span> <span data-ttu-id="89b1f-106">Þetta er dagsetningin sem vænta má þess að vara sem pöntuð er á tilteknum degi verði tiltæk til tínslu.</span><span class="sxs-lookup"><span data-stu-id="89b1f-106">This is the date on which you can expect items ordered on a particular date to be available for picking.</span></span>  

<span data-ttu-id="89b1f-107">Ef umbeðin móttökudagsetning er tilgreind í innkaupapöntunarhaus verður reiknuð pöntunardagsetning dagsetningin þegar leggja þarf fram pöntun til að vörurnar berist á þeim degi sem beðið var um.</span><span class="sxs-lookup"><span data-stu-id="89b1f-107">If you specify a requested receipt date on a purchase order header, then the calculated order date is the date on which the order must be placed to receive the items on the date that you requested.</span></span> <span data-ttu-id="89b1f-108">Svo er dagsetningin þegar vörurnar verða tilbúnar reiknuð og færð inn í reitinn **Væntanleg móttökudagsetning**.</span><span class="sxs-lookup"><span data-stu-id="89b1f-108">Then, the date on which the items are available for picking is calculated and entered in the **Expected Receipt Date** field.</span></span>  

<span data-ttu-id="89b1f-109">Ef ekki er tilgreind ósk um móttökudag notar forritið pöntunardaginn í línunni sem upphafspunkt þegar það reiknar út hvenær búast má við því að fá vörur sendar og þá dagsetningu þegar varan verður tiltæk til afgreiðslu.</span><span class="sxs-lookup"><span data-stu-id="89b1f-109">If you do not specify a requested receipt date, then the order date on the line is used as the starting point for calculating the date on which you can expect to receive the items and the date on which the items are available for picking.</span></span>  

## <a name="calculating-with-a-requested-receipt-date"></a><span data-ttu-id="89b1f-110">Reiknað með ósk um móttökudag</span><span class="sxs-lookup"><span data-stu-id="89b1f-110">Calculating with a Requested Receipt Date</span></span>  
<span data-ttu-id="89b1f-111">Ef það er ósk um móttökudag á innkaupapöntunarlínunni notar forritið þessa dagsetningu sem upphafspunkt fyrir eftirfarandi útreikninga.</span><span class="sxs-lookup"><span data-stu-id="89b1f-111">If there is a requested receipt date on the purchase order line, then that date is used as the starting point for the following calculations.</span></span>  

- <span data-ttu-id="89b1f-112">Ósk um móttökudag - útreikn. afhendingartíma = pöntunardagur</span><span class="sxs-lookup"><span data-stu-id="89b1f-112">requested receipt date - lead time calculation = order date</span></span>  
- <span data-ttu-id="89b1f-113">Ósk um móttökudag + afgreiðslutími á vörum inn í vöruhús + öryggisforskot = væntanlegur móttökudagur</span><span class="sxs-lookup"><span data-stu-id="89b1f-113">requested receipt date + inbound whse. handling time + safety lead time = expected receipt date</span></span>  

<span data-ttu-id="89b1f-114">Ef færð hefur verið inn ósk um móttökudag á innkaupapöntunarhausinn er þessi dagsetning afrituð í viðeigandi reit á öllum línunum.</span><span class="sxs-lookup"><span data-stu-id="89b1f-114">If you entered a requested receipt date on the purchase order header, then that date is copied to the corresponding field on all the lines.</span></span> <span data-ttu-id="89b1f-115">Hægt er að breyta þessari dagsetningu á öllum línunum eða fjarlægja dagsetninguna úr línunni.</span><span class="sxs-lookup"><span data-stu-id="89b1f-115">You can change this date on any of the lines, or you can remove the date on the line.</span></span>  

## <a name="calculating-without-a-requested-delivery-date"></a><span data-ttu-id="89b1f-116">Reiknað án óskar um afhendingardag</span><span class="sxs-lookup"><span data-stu-id="89b1f-116">Calculating without a Requested Delivery Date</span></span>  
<span data-ttu-id="89b1f-117">Ef færð er inn innkaupapöntunarlína án óskar um afhendingardag fyllir forritið út í reitinn **dagsetning pöntunar** á línunni með dagsetningunni í reitnum **dagsetning pöntunar** í innkaupapöntunarhausnum.</span><span class="sxs-lookup"><span data-stu-id="89b1f-117">If you enter a purchase order line without a requested delivery date, then the **Order Date** field on the line is filled with the date in the **Order Date** field on the purchase order header.</span></span> <span data-ttu-id="89b1f-118">Þetta er annaðhvort dagsetningin sem færð var inn eða vinnudagurinn.</span><span class="sxs-lookup"><span data-stu-id="89b1f-118">This is either the date that you entered or the work date.</span></span> <span data-ttu-id="89b1f-119">Forritið reiknar þá eftirfarandi dagsetningar fyrir innkaupapöntunarlínuna með pöntunardagsetninguna sem upphafspunkt:</span><span class="sxs-lookup"><span data-stu-id="89b1f-119">The following dates are then calculated for the purchase order line, with the order date as the starting point.</span></span>  

- <span data-ttu-id="89b1f-120">Pöntunardagur + Útreikningur afgreiðslutíma = Ráðgerð móttökudagsetning.</span><span class="sxs-lookup"><span data-stu-id="89b1f-120">order date + lead time calculation = planned receipt date</span></span>  
- <span data-ttu-id="89b1f-121">Áætlaður móttökudagur + afgreiðslutími á vörum inn í vöruhús + öryggisforskot = væntanlegur móttökudagur</span><span class="sxs-lookup"><span data-stu-id="89b1f-121">planned receipt date + inbound whse. handling time + safety lead time = expected receipt date</span></span>  

<span data-ttu-id="89b1f-122">Ef pöntunardeginum er breytt á línunni (til dæmis þegar vörurnar eru ekki til hjá lánardrottninum fyrr en daginn eftir) eru viðeigandi dagsetningar á línunni endurreiknaðar sjálfkrafa.</span><span class="sxs-lookup"><span data-stu-id="89b1f-122">If you change the order date on the line, such as when items are not available at your vendor until a later date, then the relevant dates on the line are automatically recalculated.</span></span>  

<span data-ttu-id="89b1f-123">Ef pöntunardagsetningunni er breytt í hausnum er dagsetningin afrituð inn í reitinn **Dagsetning pöntunar** á öllum línunum og allir viðeigandi dagsetningareitir eru endurreiknaðir.</span><span class="sxs-lookup"><span data-stu-id="89b1f-123">If you change the order date on the header, then that date is copied to the **Order Date** field on all the lines, and all the related date fields are then recalculated.</span></span>  

## <a name="see-also"></a><span data-ttu-id="89b1f-124">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="89b1f-124">See Also</span></span>  
 <span data-ttu-id="89b1f-125">[Dagsetning útreiknings fyrir sölu](sales-date-calculation-for-sales.md) </span><span class="sxs-lookup"><span data-stu-id="89b1f-125">[Date Calculation for Sales](sales-date-calculation-for-sales.md) </span></span>  
 [<span data-ttu-id="89b1f-126">Reikna dagsetningar pöntunarloforða</span><span class="sxs-lookup"><span data-stu-id="89b1f-126">Calculate Order Promising Dates</span></span>](sales-how-to-calculate-order-promising-dates.md)  
 <span data-ttu-id="89b1f-127">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="89b1f-127">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
