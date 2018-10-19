---
title: "Nota runuvinnsluna Greiðslutillögur til lánardrottna| Microsoft Docs"
description: "Hægt er að tilgreina stillingar fyrir greiðslur til lánardrottna og fá þannig greiðslutillögur sem taka mið af gjalddögum og afsláttum."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: vendor payment, creditor, debt, balance due, AP
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 7d2ebaf1efe49c8a66e6d562ab7655d45e181044
ms.contentlocale: is-is
ms.lasthandoff: 09/28/2018

---
# <a name="suggest-vendor-payments"></a><span data-ttu-id="b374b-103">Greiðslutillögur til lánardr.</span><span class="sxs-lookup"><span data-stu-id="b374b-103">Suggest Vendor Payments</span></span>
<span data-ttu-id="b374b-104">Í glugganum **Greiðslubók** geturðu notað **Greiðslutillögur til lánardr.** runuvinnsluna til að stinga upp á greiðslulínur.</span><span class="sxs-lookup"><span data-stu-id="b374b-104">In the **Payment Journal** window, you can use the **Suggest Vendor Payments** batch job to suggest payment lines.</span></span> <span data-ttu-id="b374b-105">Línur fyrir greiðslur sem falla brátt á gjalddaga, eða greiðslur þar sem greiðsluafsláttur er í boði, eru ráðlagðar á grunni stillinganna þinna.</span><span class="sxs-lookup"><span data-stu-id="b374b-105">Lines for payments that are due soon or payments where a payment discount is available are suggested based on your settings.</span></span>

<span data-ttu-id="b374b-106">Til að njóta greiðsluábendinga til fulls verður þú fyrst að forgangsraða lánardrottnum þínum.</span><span class="sxs-lookup"><span data-stu-id="b374b-106">To benefit fully from payment suggestions, you must first prioritize your vendors.</span></span> <span data-ttu-id="b374b-107">Frekari upplýsingar eru í [Lánardrottnum forgangsraðað](purchasing-how-prioritize-vendors.md).</span><span class="sxs-lookup"><span data-stu-id="b374b-107">For more information, see [Prioritize Vendors](purchasing-how-prioritize-vendors.md).</span></span>  

> [!NOTE]  
> <span data-ttu-id="b374b-108">Lánardrottnafærslur sem eru **Í bið** eru ekki teknar með í runukeyrslunni.</span><span class="sxs-lookup"><span data-stu-id="b374b-108">Vendor ledger entries that are **On Hold** are not included in the batch job.</span></span>  

> [!IMPORTANT]  
>   <span data-ttu-id="b374b-109">Ef nýta á greiðsluafslátt og tiltæk upphæð hefur verið færð inn, verður upphæðin notuð fyrir:</span><span class="sxs-lookup"><span data-stu-id="b374b-109">If you want to take advantage of payment discounts, and have entered an available amount, the amount will be used for:</span></span>  
    * <span data-ttu-id="b374b-110">Forgangsatriði fyrirframgreiddar seljenda færslur fyrst í forgangsröð.</span><span class="sxs-lookup"><span data-stu-id="b374b-110">Prioritized overdue vendor entries first in order of priority.</span></span>   
    * <span data-ttu-id="b374b-111">Lánardrottnafærslur sem eru fallnar á tíma sem eru ekki forgangsraðar.</span><span class="sxs-lookup"><span data-stu-id="b374b-111">Overdue vendor entries that are not prioritized.</span></span>  
    * <span data-ttu-id="b374b-112">Opnaðu söluaðili færslur sem eiga rétt á greiðslukortum, raðað eftir seljanda númeri.</span><span class="sxs-lookup"><span data-stu-id="b374b-112">Open vendor entries that qualify for payment discounts, arranged by vendor number.</span></span>  

## <a name="to-use-the-suggest-vendor-payments-function"></a><span data-ttu-id="b374b-113">nota aðgerðina Greiðslutillögur til lánardrottna</span><span class="sxs-lookup"><span data-stu-id="b374b-113">To use the Suggest Vendor Payments function</span></span>
1. <span data-ttu-id="b374b-114">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **greiðslubók** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="b374b-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Payment Journals**, and then choose the related link.</span></span>  
2. <span data-ttu-id="b374b-115">Opna skal viðeigandi færslubók, og síðan velja **Greiðslutillögur til lánardrottna** aðgerðina.</span><span class="sxs-lookup"><span data-stu-id="b374b-115">Open the relevant journal, and then choose the **Suggest Vendor Payments** action.</span></span>  
3. <span data-ttu-id="b374b-116">Fyllið inn í svæðin eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="b374b-116">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
4. <span data-ttu-id="b374b-117">Velja hnappinn **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="b374b-117">Choose the **OK** button.</span></span>  

## <a name="to-insert-the-due-date-as-posting-date-on-payment-journal-lines"></a><span data-ttu-id="b374b-118">Setja inn skiladag sem bókunardagsetningu á greiðslubókarlínum</span><span class="sxs-lookup"><span data-stu-id="b374b-118">To insert the due date as posting date on payment journal lines</span></span>
<span data-ttu-id="b374b-119">Þegar þú notar runuvinnsluna **Greiðslutillögur til lánardrottna** til að stofna greiðslulínur fyrir lánardrottna þína getur þú fyllt út tvo sérstaka reiti til að gæta þess að stofnuðu línurnar noti gjalddaga til að reikna út bókunardagsetningu.</span><span class="sxs-lookup"><span data-stu-id="b374b-119">When you use the **Suggest Vendor Payments** batch job to create payment lines for your vendors, you can fill two special fields to make sure that the generated lines use the due date to calculate the posting date.</span></span> <span data-ttu-id="b374b-120">Þessir reitir eru **Reikna Bókunardagsetning úr Gjalddaga jöfnunar** og **frávik gjalddaga jöfnunar**.</span><span class="sxs-lookup"><span data-stu-id="b374b-120">These fields are **Calculate Posting Date from Applies-to-Doc Due Date** and **Applies-to-Doc Due Date Offset**.</span></span>  

> [!IMPORTANT]  
>   <span data-ttu-id="b374b-121">Ekki er hægt að nota reitinn **Reikna út bókunardagsetningu úr gildisdegi** samhliða reitunum **Finna greiðsluafslátt** eða **Samantekt fyrir lánardrottinn**.</span><span class="sxs-lookup"><span data-stu-id="b374b-121">You cannot use the **Calculate Posting Date from Applies-to-Doc Due Date** field together with the **Find Payment Discounts** field or the **Summarize per Vendor** field.</span></span> <span data-ttu-id="b374b-122">Ef staðsetningardagsetningin er byggð á gjalddaga, geta sumir afsláttarmöguleikar ekki reiknað rétt vegna þess að póstsetningardagur er eftir gjalddaga.</span><span class="sxs-lookup"><span data-stu-id="b374b-122">If the posting date is based on the due date, some payment discounts may not calculate correctly because the posting date is after the payment discount date.</span></span>  

<span data-ttu-id="b374b-123">Ef útreiknuð bókunardagsetning er liðin er bókunardagsetningin færð upp að vinnudagsetningunni og viðvörun birtist.</span><span class="sxs-lookup"><span data-stu-id="b374b-123">Also, if the calculated posting date is in the past, then the posting date is moved up to the work date, and a warning is displayed.</span></span>  

<span data-ttu-id="b374b-124">Einnig er hægt að myndað sjálfkrafa greiðslulínur með gjalddaga til að reikna bókunardagsetningu</span><span class="sxs-lookup"><span data-stu-id="b374b-124">Alternatively, you can manually create payment lines using the due date to calculate the posting date.</span></span> <span data-ttu-id="b374b-125">Þegar lánardrottnafærslur hafa verið jafnaðar er hægt að nota **Reikna út bókunardagsetningu** til að uppfæra bókunardagsetningu á færslubókarlínunni með gjalddaga tengds innkaupareiknings.</span><span class="sxs-lookup"><span data-stu-id="b374b-125">After you apply vendor ledger entries, you can use the **Calculate Posting Date** action to update the posting date on the journal line with the due date of the related purchase invoice.</span></span> <span data-ttu-id="b374b-126">Frekari upplýsingar eru í [Jafna innkaupafærslur handvirkt](payables-how-apply-purchase-transactions-manually.md).</span><span class="sxs-lookup"><span data-stu-id="b374b-126">For more information, see [Apply Purchase Transactions Manually](payables-how-apply-purchase-transactions-manually.md).</span></span>  

> [!NOTE]  
>   <span data-ttu-id="b374b-127">Ef innkaupareikningur er gjaldfallinn, er bókunardagsetningin stillt á vinnudag og leturgerð á línunni verður rautt.</span><span class="sxs-lookup"><span data-stu-id="b374b-127">If the purchase invoice is overdue, the posting date is set to the work date, and the font on the line becomes red.</span></span>  

## <a name="see-also"></a><span data-ttu-id="b374b-128">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="b374b-128">See Also</span></span>
[<span data-ttu-id="b374b-129">Stjórna skuldum</span><span class="sxs-lookup"><span data-stu-id="b374b-129">Managing Payables</span></span>](payables-manage-payables.md)  
[<span data-ttu-id="b374b-130">Framkvæma greiðslur</span><span class="sxs-lookup"><span data-stu-id="b374b-130">Making Payments</span></span>](payables-make-payments.md)  
[<span data-ttu-id="b374b-131">Vinna í færslubókum</span><span class="sxs-lookup"><span data-stu-id="b374b-131">Working with General Journals</span></span>](ui-work-general-journals.md)  
<span data-ttu-id="b374b-132">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="b374b-132">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

