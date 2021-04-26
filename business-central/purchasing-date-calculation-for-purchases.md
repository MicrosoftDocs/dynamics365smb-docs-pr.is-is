---
title: Dagsetning útreiknings fyrir kaup | Microsoft Docs
description: Forritið reiknar sjálfkrafa daginn sem verður að panta vöru svo hún sé til í birgðum á tilteknum degi. Þetta er dagsetningin sem vænta má þess að vara sem pöntuð er á tilteknum degi verði tiltæk til tínslu.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: b65e082355623f422cfb03698f6413fdb04f0daf
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5780258"
---
# <a name="date-calculation-for-purchases"></a><span data-ttu-id="8f864-104">Dagsetning útreiknings fyrir kaup.</span><span class="sxs-lookup"><span data-stu-id="8f864-104">Date Calculation for Purchases</span></span>

[!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="8f864-105">reiknar sjálfkrafa daginn sem verður að panta vöru svo hún sé til í birgðum á tilteknum degi.</span><span class="sxs-lookup"><span data-stu-id="8f864-105">automatically calculates the date on which you must order an item to have it in inventory on a certain date.</span></span> <span data-ttu-id="8f864-106">Þetta er dagsetningin sem vænta má þess að vara sem pöntuð er á tilteknum degi verði tiltæk til tínslu.</span><span class="sxs-lookup"><span data-stu-id="8f864-106">This is the date on which you can expect items ordered on a particular date to be available for picking.</span></span>  

<span data-ttu-id="8f864-107">Ef umbeðin móttökudagsetning er tilgreind í innkaupapöntunarhaus verður reiknuð pöntunardagsetning dagsetningin þegar leggja þarf fram pöntun til að vörurnar berist á þeim degi sem beðið var um.</span><span class="sxs-lookup"><span data-stu-id="8f864-107">If you specify a requested receipt date on a purchase order header, then the calculated order date is the date on which the order must be placed to receive the items on the date that you requested.</span></span> <span data-ttu-id="8f864-108">Svo er dagsetningin þegar vörurnar verða tilbúnar reiknuð og færð inn í reitinn **Væntanleg móttökudagsetning**.</span><span class="sxs-lookup"><span data-stu-id="8f864-108">Then, the date on which the items are available for picking is calculated and entered in the **Expected Receipt Date** field.</span></span>  

<span data-ttu-id="8f864-109">Ef ekki er tilgreind ósk um móttökudag notar forritið pöntunardaginn í línunni sem upphafspunkt þegar það reiknar út hvenær búast má við því að fá vörur sendar og þá dagsetningu þegar varan verður tiltæk til afgreiðslu.</span><span class="sxs-lookup"><span data-stu-id="8f864-109">If you do not specify a requested receipt date, then the order date on the line is used as the starting point for calculating the date on which you can expect to receive the items and the date on which the items are available for picking.</span></span>  

## <a name="calculating-with-a-requested-receipt-date"></a><span data-ttu-id="8f864-110">Reiknað með ósk um móttökudag</span><span class="sxs-lookup"><span data-stu-id="8f864-110">Calculating with a requested receipt date</span></span>

<span data-ttu-id="8f864-111">Ef það er ósk um móttökudag á innkaupapöntunarlínunni notar forritið þessa dagsetningu sem upphafspunkt fyrir eftirfarandi útreikninga.</span><span class="sxs-lookup"><span data-stu-id="8f864-111">If there is a requested receipt date on the purchase order line, then that date is used as the starting point for the following calculations.</span></span>  

- <span data-ttu-id="8f864-112">Ósk um móttökudag - útreikn. afhendingartíma = pöntunardagur</span><span class="sxs-lookup"><span data-stu-id="8f864-112">requested receipt date - lead time calculation = order date</span></span>  
- <span data-ttu-id="8f864-113">Ósk um móttökudag + afgreiðslutími á vörum inn í vöruhús + öryggisforskot = væntanlegur móttökudagur</span><span class="sxs-lookup"><span data-stu-id="8f864-113">requested receipt date + inbound whse. handling time + safety lead time = expected receipt date</span></span>  

<span data-ttu-id="8f864-114">Ef færð hefur verið inn ósk um móttökudag á innkaupapöntunarhausinn er þessi dagsetning afrituð í viðeigandi reit á öllum línunum.</span><span class="sxs-lookup"><span data-stu-id="8f864-114">If you entered a requested receipt date on the purchase order header, then that date is copied to the corresponding field on all the lines.</span></span> <span data-ttu-id="8f864-115">Hægt er að breyta þessari dagsetningu á öllum línunum eða fjarlægja dagsetninguna úr línunni.</span><span class="sxs-lookup"><span data-stu-id="8f864-115">You can change this date on any of the lines, or you can remove the date on the line.</span></span>  

> [!NOTE]
> <span data-ttu-id="8f864-116">Ef ferlið þitt er byggt á útreikningi aftur í tímann, t.d. ef þú notar umbeðna móttökudagsetningu til að fá pöntunardagsetninguna, ráðleggjum við þér að þú notir dagsetningarreiknireglur sem eru með fastri tímalengd á borði við „5D“ fyrir fimm daga eða „1V“ fyrir eina viku.</span><span class="sxs-lookup"><span data-stu-id="8f864-116">If your process is based on backward calculation, for example, if you use the requested receipt date to get the order date, we recommend that you use date formulas that have fixed durations, such as "5D" for five days or "1W" for one week.</span></span> <span data-ttu-id="8f864-117">Dagsetningarreiknireglur án fastra tímalengda, t.d „NV“ fyrir núverandi viku eða „NM“ fyrir núverandi mánuð, getur leitt til rangra útreikninga á dagsetningum.</span><span class="sxs-lookup"><span data-stu-id="8f864-117">Date formulas without fixed durations, such as "CW" for current week or CM for current month, can result in incorrect date calculations.</span></span> <span data-ttu-id="8f864-118">Frekari upplýsingar er að finna í [Vinna með dagsetningar og tíma í dagatali](ui-enter-date-ranges.md).</span><span class="sxs-lookup"><span data-stu-id="8f864-118">For more information about date formulas, see [Working with Calendar Dates and Times](ui-enter-date-ranges.md).</span></span>

## <a name="calculating-without-a-requested-delivery-date"></a><span data-ttu-id="8f864-119">Reiknað án óskar um afhendingardag</span><span class="sxs-lookup"><span data-stu-id="8f864-119">Calculating without a requested delivery date</span></span>

<span data-ttu-id="8f864-120">Ef færð er inn innkaupapöntunarlína án óskar um afhendingardag fyllir forritið út í reitinn **dagsetning pöntunar** á línunni með dagsetningunni í reitnum **dagsetning pöntunar** í innkaupapöntunarhausnum.</span><span class="sxs-lookup"><span data-stu-id="8f864-120">If you enter a purchase order line without a requested delivery date, then the **Order Date** field on the line is filled with the date in the **Order Date** field on the purchase order header.</span></span> <span data-ttu-id="8f864-121">Þetta er annaðhvort dagsetningin sem færð var inn eða vinnudagurinn.</span><span class="sxs-lookup"><span data-stu-id="8f864-121">This is either the date that you entered or the work date.</span></span> <span data-ttu-id="8f864-122">Forritið reiknar þá eftirfarandi dagsetningar fyrir innkaupapöntunarlínuna með pöntunardagsetninguna sem upphafspunkt:</span><span class="sxs-lookup"><span data-stu-id="8f864-122">The following dates are then calculated for the purchase order line, with the order date as the starting point.</span></span>  

- <span data-ttu-id="8f864-123">Pöntunardagur + Útreikningur afgreiðslutíma = Ráðgerð móttökudagsetning.</span><span class="sxs-lookup"><span data-stu-id="8f864-123">order date + lead time calculation = planned receipt date</span></span>  
- <span data-ttu-id="8f864-124">Áætlaður móttökudagur + afgreiðslutími á vörum inn í vöruhús + öryggisforskot = væntanlegur móttökudagur</span><span class="sxs-lookup"><span data-stu-id="8f864-124">planned receipt date + inbound whse. handling time + safety lead time = expected receipt date</span></span>  

<span data-ttu-id="8f864-125">Ef pöntunardeginum er breytt á línunni (til dæmis þegar vörurnar eru ekki til hjá lánardrottninum fyrr en daginn eftir) eru viðeigandi dagsetningar á línunni endurreiknaðar sjálfkrafa.</span><span class="sxs-lookup"><span data-stu-id="8f864-125">If you change the order date on the line, such as when items are not available at your vendor until a later date, then the relevant dates on the line are automatically recalculated.</span></span>  

<span data-ttu-id="8f864-126">Ef pöntunardagsetningunni er breytt í hausnum er dagsetningin afrituð inn í reitinn **Dagsetning pöntunar** á öllum línunum og allir viðeigandi dagsetningareitir eru endurreiknaðir.</span><span class="sxs-lookup"><span data-stu-id="8f864-126">If you change the order date on the header, then that date is copied to the **Order Date** field on all the lines, and all the related date fields are then recalculated.</span></span>  

## <a name="default-values-for-lead-time-calculation"></a><span data-ttu-id="8f864-127">Sjálfgefin gildi fyrir útreikning afhendingartíma</span><span class="sxs-lookup"><span data-stu-id="8f864-127">Default values for lead time calculation</span></span>

[!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="8f864-128">notar gildið úr reitnum **Útreikningur afhendingartíma** í innkaupapöntunarlínunni til að reikna út pöntunina og væntanlegar móttökudagsetningar.</span><span class="sxs-lookup"><span data-stu-id="8f864-128">uses the value from the **Lead Time Calculation** field on the purchase order line to calculate the order and the expected receipt dates.</span></span>  

<span data-ttu-id="8f864-129">Hægt er að tilgreina gildið handvirkt í línunni eða leyfa forritinu að nota gildin sem skilgreind eru í lánardrottnaspjaldi, birgðaspjaldi, birgðahaldseiningu eða vörulista lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="8f864-129">You can manually specify the value on the line or let the program use values that are defined on the vendor card, item card, stockkeeping unit card, or the item vendor catalog.</span></span>
<span data-ttu-id="8f864-130">Gildið fyrir afhendingartíma á lánardrottnaspjaldi er hinsvegar aðeins notað ef afhendingartími er ekki tilgreindur í birgðaspjaldinu, birgðahaldseiningunni eða vörulista lánardrottins fyrir vöruna.</span><span class="sxs-lookup"><span data-stu-id="8f864-130">However, the lead time value on the vendor card is used only if a lead time is not specified on the item card, stockkeeping unit card, or the item vendor catalog for the item.</span></span> <span data-ttu-id="8f864-131">Þetta er einnig hækkandi forgangsröð fyrir þessi gildi.</span><span class="sxs-lookup"><span data-stu-id="8f864-131">This is also the escalating order of priority for these values.</span></span> <span data-ttu-id="8f864-132">Ef þau eru öll gefin upp hefur afhendingartíminn úr lánardrottnaspjaldinu lægsta forgang og afhendingartíminn úr vörulista lánardrottins hæsta forgang.</span><span class="sxs-lookup"><span data-stu-id="8f864-132">If they are all provided, the lead time from the vendor card has the lowest priority, and the lead time from the item vendor catalog has the highest priority.</span></span>  

## <a name="see-also"></a><span data-ttu-id="8f864-133">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="8f864-133">See Also</span></span>

<span data-ttu-id="8f864-134">[Dagsetning útreiknings fyrir sölu](sales-date-calculation-for-sales.md) </span><span class="sxs-lookup"><span data-stu-id="8f864-134">[Date Calculation for Sales](sales-date-calculation-for-sales.md) </span></span>  
[<span data-ttu-id="8f864-135">Reikna dagsetningar pöntunarloforða</span><span class="sxs-lookup"><span data-stu-id="8f864-135">Calculate Order Promising Dates</span></span>](sales-how-to-calculate-order-promising-dates.md)  
<span data-ttu-id="8f864-136">[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="8f864-136">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  


[!INCLUDE[footer-include](includes/footer-banner.md)]