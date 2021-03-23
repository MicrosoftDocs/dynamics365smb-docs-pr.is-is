---
title: Hvernig skal búa til fyrirframgreiðslureikning | Microsoft Docs
description: Lærið að fást við aðstæður þar sem þú eða lánardrottinn þinn krefjast fyrirframgreiðslu.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 3a1f79f089ef8633ca51be35930c5de5c2401b29
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5387400"
---
# <a name="create-prepayment-invoices"></a><span data-ttu-id="6cd9d-103">Stofna fyrirframgreiðslureikninga</span><span class="sxs-lookup"><span data-stu-id="6cd9d-103">Create Prepayment Invoices</span></span>

<span data-ttu-id="6cd9d-104">Ef þú gerir kröfu um að viðskiptavinir inni greiðslu af hendi áður en þú sendir pöntun til þeirra getur þú notað aðgerð fyrirframgreiðslu.</span><span class="sxs-lookup"><span data-stu-id="6cd9d-104">If you require your customers to submit payment before you ship an order to them, you can use the prepayment functionality.</span></span> <span data-ttu-id="6cd9d-105">Sama gildir ef lánardrottinn þinn krefst þess að þú innir greiðslu af hendi áður en hann sendir pöntun til þín.</span><span class="sxs-lookup"><span data-stu-id="6cd9d-105">The same applies if your vendor requires you to submit payment before they ship an order to you.</span></span>  

<span data-ttu-id="6cd9d-106">Hægt er að hefja fyrirframgreiðsluferlið þegar búið er að stofna sölu- eða innkaupapöntun.</span><span class="sxs-lookup"><span data-stu-id="6cd9d-106">You can start the prepayment process when you create a sales or purchase order.</span></span> <span data-ttu-id="6cd9d-107">Ef um er að ræða sjálfgefin fyrirframgreiðsluprósenta fyrir þennan viðskiptavin eða lánardrottinn verður hún sjálfkrafa innifalin á fyrirframgreiðslureikningnum.</span><span class="sxs-lookup"><span data-stu-id="6cd9d-107">If you have a default prepayment percentage for this customer or vendor, that will be included automatically in the resulting prepayment invoice.</span></span> <span data-ttu-id="6cd9d-108">Einnig er hægt að tilgreina fyrirframgreiðsluprósentuna fyrir allt skjalið.</span><span class="sxs-lookup"><span data-stu-id="6cd9d-108">You can also specify a prepayment percentage to the entire document.</span></span>

<span data-ttu-id="6cd9d-109">Þegar búið er að stofna sölu- eða innkaupapöntun er hægt að stofna fyrirframgreiðslureikning.</span><span class="sxs-lookup"><span data-stu-id="6cd9d-109">After you create a sales or purchase order, you can create a prepayment invoice.</span></span> <span data-ttu-id="6cd9d-110">Hægt er að nota sjálfgefnar prósentur fyrir sölu- og innkauplínur eða leiðrétta upphæðina eins og með þarf.</span><span class="sxs-lookup"><span data-stu-id="6cd9d-110">You can use the default percentages for each sales or purchase line, or you can adjust the amount as necessary.</span></span> <span data-ttu-id="6cd9d-111">Til dæmis er hægt að tilgreina heildarupphæð fyrir alla pöntunina.</span><span class="sxs-lookup"><span data-stu-id="6cd9d-111">For example, you can specify a total amount for the entire order.</span></span>  

<span data-ttu-id="6cd9d-112">Eftirfarandi ferli sýnir hvernig skal gefa út fyrirframgreiðslureikning fyrir sölupöntun.</span><span class="sxs-lookup"><span data-stu-id="6cd9d-112">The following procedure describes how to invoice a prepayment for a sales order.</span></span> <span data-ttu-id="6cd9d-113">Skrefin eru svipuð fyrir innkaupapöntun.</span><span class="sxs-lookup"><span data-stu-id="6cd9d-113">The steps are similar for purchase orders.</span></span>  

## <a name="to-create-a-prepayment-invoice"></a><span data-ttu-id="6cd9d-114">Stofnun fyrirframgreiðslureiknings</span><span class="sxs-lookup"><span data-stu-id="6cd9d-114">To create a prepayment invoice</span></span>

1. <span data-ttu-id="6cd9d-115">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Sölupantanir** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="6cd9d-115">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Orders**, and then choose the related link.</span></span>  
2. <span data-ttu-id="6cd9d-116">Stofna nýja sölupöntun fyrir viðeigandi viðskiptavin.</span><span class="sxs-lookup"><span data-stu-id="6cd9d-116">Create a new sales order for the relevant customer.</span></span> <span data-ttu-id="6cd9d-117">Frekari upplýsingar eru í [Selja vörur](sales-how-sell-products.md).</span><span class="sxs-lookup"><span data-stu-id="6cd9d-117">For more information, see [Sell Products](sales-how-sell-products.md).</span></span>  

    <span data-ttu-id="6cd9d-118">Á flýtiflipanum **Fyrirframgreiðsla** tilgreinir svæðið **Fyrirframgreiðsla %** prósentuna sem á að nota til að reikna út fyrirframgreiðsluupphæðina.</span><span class="sxs-lookup"><span data-stu-id="6cd9d-118">On the **Prepayment** FastTab, the **Prepayment %** field specifies the percentage to use to calculate the prepayment amount.</span></span> <span data-ttu-id="6cd9d-119">Ef sjálfgefin fyrirframgreiðsluprósenta er á spjaldi viðskiptavinar er svæðið sjálfkrafa fylltur út.</span><span class="sxs-lookup"><span data-stu-id="6cd9d-119">If there is a default prepayment percentage on the customer card, the field is filled in automatically.</span></span> <span data-ttu-id="6cd9d-120">Hægt er að breyta prósentunni.</span><span class="sxs-lookup"><span data-stu-id="6cd9d-120">You can change the percentage.</span></span> <!--This percentage is applied to lines where the item on that line does not already specify a prepayment percentage. The prepayment percentage is only copied from the header to lines that do not copy the default prepayment percentage from the item.-->  

    <span data-ttu-id="6cd9d-121">Veldu svæðið **Þjappa fyrirframgreiðslu** ef óskað er eftir að stofna línur á fyrirframgreiðslureikningnum sem sameinar línur úr sölupöntuninni ef:</span><span class="sxs-lookup"><span data-stu-id="6cd9d-121">Choose the **Compress Prepayment** field if you want to create lines on the prepayment invoice that combine lines from the sales order if:</span></span>  

    - <span data-ttu-id="6cd9d-122">Þær eru með sama fjárhagsreikninginn fyrir fyrirframgreiðslur samkvæmt stillingum í almenna bókunargrunninum.</span><span class="sxs-lookup"><span data-stu-id="6cd9d-122">They have the same general ledger account for prepayments as determined by the general posting setup.</span></span>  
    - <span data-ttu-id="6cd9d-123">Þeir hafa sömu víddir.</span><span class="sxs-lookup"><span data-stu-id="6cd9d-123">They have the same dimensions.</span></span>  

    <span data-ttu-id="6cd9d-124">Ekki velja svæðið **Þjappa fyrirframgreiðslu** ef þú vilt tilgreina fyrirframgreiðslureikning með einni línu fyrir hverja sölupöntunarlínu sem hefur fyrirframgreiðsluprósentu.</span><span class="sxs-lookup"><span data-stu-id="6cd9d-124">If you want to specify a prepayment invoice with one line for each sales order line that has a prepayment percentage, then do not choose the **Compress Prepayment** field.</span></span>  

    <span data-ttu-id="6cd9d-125">Gjalddagi fyrirframgreiðslunnar er sjálfkrafa reiknaður út frá gildinu í reitnum **Greiðsluskilmálakóði fyrirframgr.**.</span><span class="sxs-lookup"><span data-stu-id="6cd9d-125">The due date for the prepayment is calculated automatically based on the value of the **Prepmt. Payment Terms Code**.</span></span>

3. <span data-ttu-id="6cd9d-126">Sölulínurnar eru fylltar út.</span><span class="sxs-lookup"><span data-stu-id="6cd9d-126">Fill in the sales lines.</span></span>  

    <span data-ttu-id="6cd9d-127">Ef þú hefur tilgreint sjálfgefna fyrirframgreiðsluprósentuna annað hvort fyrir viðskiptavininn eða á flýtiflipanum **Fyrirframgreiðsla** í þessu skjali, er þetta gildi afritað í hverja línu.</span><span class="sxs-lookup"><span data-stu-id="6cd9d-127">If you have specified a default prepayment percentage either for the customer or on the **Prepayment** FastTab on this document, this value is copied to each line.</span></span> <span data-ttu-id="6cd9d-128">Hægt er að breyta innihaldi reitsins **Fyrirframgreiðsla %** í línunni.</span><span class="sxs-lookup"><span data-stu-id="6cd9d-128">You can change the contents of the **Prepayment %** field on the line.</span></span>  

4. <span data-ttu-id="6cd9d-129">Veldu **Upplýsingar** aðgerðina til að skoða heildarupphæð fyrirframgreiðslu.</span><span class="sxs-lookup"><span data-stu-id="6cd9d-129">To view the total prepayment amount, choose the **Statistics** action.</span></span>

    <span data-ttu-id="6cd9d-130">Ef leiðrétta á heildarupphæð fyrirframgreiðslunnar fyrir pöntunina er hægt að breyta innihaldi reitsins **Upphæð fyrirframgreiðslu** á síðunni **Tölfræði sölupöntunar**.</span><span class="sxs-lookup"><span data-stu-id="6cd9d-130">If you want to adjust the total prepayment amount for the order, you can change the contents of the **Prepayment Amount** field on the **Sales Order Statistics** page.</span></span>  

    <span data-ttu-id="6cd9d-131">Ef reiturinn **Verð ásamt VSK** er valinn er hægt að breyta reitnum **Upphæð fyrirframgreiðslu með VSK**.</span><span class="sxs-lookup"><span data-stu-id="6cd9d-131">If the **Prices Including VAT** field is selected, the **Prepayment Amount Incl. VAT** field is editable.</span></span>  

    <span data-ttu-id="6cd9d-132">Ef þú breytir innihaldi reitsins **Fyrirframgreiðsluupphæð**, mun upphæðinni verða dreift hlutfallslega á milli allra lína, nema þeirra sem hafa **0** í reitnum **Fyrirframgreiðsla %**.</span><span class="sxs-lookup"><span data-stu-id="6cd9d-132">If you change the contents of the **Prepayment Amount** field, the amount will be distributed proportionately between all lines, except those that have **0** in the **Prepayment %** field.</span></span>  

5. <span data-ttu-id="6cd9d-133">Til að prenta prufuskýrslu áður en fyrirframgreiðslureikningurinn er bókaður skal velja aðgerðina **Fyrirframgreiðsla**, og síðan aðgerðina **Prufuskýrsla fyrirframgreiðslu**.</span><span class="sxs-lookup"><span data-stu-id="6cd9d-133">To print a test report before posting the prepayment invoice, choose the **Prepayment** action, and then choose the **Prepayment Test Report** action.</span></span>  
6. <span data-ttu-id="6cd9d-134">Til að bóka fyrirframgreiðslureikningurinn skal velja aðgerðina **Fyrirframgreiðsla**, og síðan aðgerðina **Bóka fyrirframgreiðslureikning**.</span><span class="sxs-lookup"><span data-stu-id="6cd9d-134">To post the prepayment invoice, choose the **Prepayment** action, and then choose the **Post Prepayment Invoice** action.</span></span>  

    <span data-ttu-id="6cd9d-135">Fyrirframgreiðslureikningur er bókaður og prentaður með því að velja aðgerðina **Bóka og prenta fyrirframgr.reikning**.</span><span class="sxs-lookup"><span data-stu-id="6cd9d-135">To post and print the prepayment invoice, choose the **Post and Print Prepmt. Invoice** action.</span></span>  

<span data-ttu-id="6cd9d-136">Hægt er að gefa út viðbótar fyrirframgreiðslureikninga fyrir pöntunina.</span><span class="sxs-lookup"><span data-stu-id="6cd9d-136">You can issue additional prepayment invoices for the order.</span></span> <span data-ttu-id="6cd9d-137">Þetta er gert með því að hækka upphæð fyrirframgreiðslunnar í einni eða fleiri línum, leiðrétta dagsetningu fylgiskjalsins, ef þess þarf, og bóka fyrirframgreiðslureikninginn.</span><span class="sxs-lookup"><span data-stu-id="6cd9d-137">To do this, increase the prepayment amount on one or more lines, adjust the document date if necessary, and post the prepayment invoice.</span></span> <span data-ttu-id="6cd9d-138">Nýr reikningur er stofnaður fyrir mismuninn á milli reikningsfærðra upphæða fyrirframgreiðslu og nýju fyrirframgreiðsluupphæðarinnar.</span><span class="sxs-lookup"><span data-stu-id="6cd9d-138">A new invoice will be created for the difference between the prepayment amounts invoiced so far and the new prepayment amount.</span></span>  

> [!NOTE]  
> <span data-ttu-id="6cd9d-139">Ef þú ert í Norður Ameríku, geturðu ekki breytt fyrirframgreiðsluprósentunni eftir að fyrirframgreiðslureikningurinn hefur verið bókaður.</span><span class="sxs-lookup"><span data-stu-id="6cd9d-139">If you are located in North America, you cannot change the prepayment percentage after the prepayment invoice has been posted.</span></span> <span data-ttu-id="6cd9d-140">Í N-amerísku útgáfu [!INCLUDE[prod_short](includes/prod_short.md)] er komið í veg fyrir þetta, því útreikningur söluskatts yrði annars rangur.</span><span class="sxs-lookup"><span data-stu-id="6cd9d-140">This is prevented in the North American version of [!INCLUDE[prod_short](includes/prod_short.md)] because the calculation of sales tax will otherwise be incorrect.</span></span>  

 <span data-ttu-id="6cd9d-141">Þegar hægt er að bóka restina af reikningnum er hann bókaður eins og hver annar reikningur og fyrirframgreiðsluupphæðin er sjálfvirkt dregin frá þeirri upphæð sem greiða á.</span><span class="sxs-lookup"><span data-stu-id="6cd9d-141">When you are ready to post the rest of the invoice, post it as you would post any invoice, and the prepayment amount will automatically be deducted from the amount due.</span></span>  

## <a name="see-also"></a><span data-ttu-id="6cd9d-142">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="6cd9d-142">See Also</span></span>

[<span data-ttu-id="6cd9d-143">Reikningsfærsla fyrirframgreiðslna</span><span class="sxs-lookup"><span data-stu-id="6cd9d-143">Invoicing Prepayments</span></span>](finance-invoice-prepayments.md)  
[<span data-ttu-id="6cd9d-144">Kynning: Uppsetning og reikningsfærsla fyrirframgreiðslna fyrir sölu</span><span class="sxs-lookup"><span data-stu-id="6cd9d-144">Walkthrough: Setting Up and Invoicing Sales Prepayments</span></span>](walkthrough-setting-up-and-invoicing-sales-prepayments.md)  
[<span data-ttu-id="6cd9d-145">Fjármál</span><span class="sxs-lookup"><span data-stu-id="6cd9d-145">Finance</span></span>](finance.md)  
<span data-ttu-id="6cd9d-146">[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="6cd9d-146">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]