---
title: "Hvernig skal búa til fyrirframgreiðslureikning | Microsoft Docs"
description: "Lærið að fást við aðstæður þar sem þú eða lánardrottinn þinn krefjast fyrirframgreiðslu."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/07/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 04d7703df0c1b5e4da8996f00b5f1eed293cbf56
ms.contentlocale: is-is
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-create-prepayment-invoices"></a><span data-ttu-id="bf9e0-103">Hvernig á að stofna reikninga fyrirframgreiðslu</span><span class="sxs-lookup"><span data-stu-id="bf9e0-103">How to: Create Prepayment Invoices</span></span>
<span data-ttu-id="bf9e0-104">Ef viðskiptamenn þurfa að leggja fram greiðslu áður en þeir fá pöntun afhenta eða ef lánardrottin fer fram á greiðslu áður en hann afhendir pöntun er hægt að nota aðgerð fyrirframgreiðslu.</span><span class="sxs-lookup"><span data-stu-id="bf9e0-104">If you require your customers to submit payment before you ship an order to them, or if your vendor requires you to submit payment before they ship an order to you, you can use the prepayment functionality.</span></span>  

<span data-ttu-id="bf9e0-105">Þegar búið er að stofna sölu- eða innkaupapöntun er hægt að stofna fyrirframgreiðslureikning.</span><span class="sxs-lookup"><span data-stu-id="bf9e0-105">After you create a sales or purchase order, you can create a prepayment invoice.</span></span> <span data-ttu-id="bf9e0-106">Hægt er að nota sjálfgefnar prósentur fyrir sölu- og innkauplínur eða leiðrétta upphæðina eins og með þarf.</span><span class="sxs-lookup"><span data-stu-id="bf9e0-106">You can use the default percentages for each sales or purchase line, or you can adjust the amount as necessary.</span></span> <span data-ttu-id="bf9e0-107">Til dæmis er hægt að tilgreina heildarupphæð fyrir alla pöntunina.</span><span class="sxs-lookup"><span data-stu-id="bf9e0-107">For example, you can specify a total amount for the entire order.</span></span>  

<span data-ttu-id="bf9e0-108">Eftirfarandi ferli sýnir hvernig skal gefa út fyrirframgreiðslureikning fyrir sölupantanir.</span><span class="sxs-lookup"><span data-stu-id="bf9e0-108">The following procedure describes how to invoice a prepayment for a sales orders.</span></span> <span data-ttu-id="bf9e0-109">Skrefin eru svipuð fyrir innkaupapöntun.</span><span class="sxs-lookup"><span data-stu-id="bf9e0-109">The steps are similar for purchase orders.</span></span>  

## <a name="to-create-a-prepayment-invoice"></a><span data-ttu-id="bf9e0-110">Stofnun fyrirframgreiðslureiknings</span><span class="sxs-lookup"><span data-stu-id="bf9e0-110">To create a prepayment invoice</span></span>  
1. <span data-ttu-id="bf9e0-111">Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn  **Sölupantanir** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="bf9e0-111">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Sales Orders**, and then choose the related link.</span></span>  
2. <span data-ttu-id="bf9e0-112">Stofna skal nýja sölupöntun.</span><span class="sxs-lookup"><span data-stu-id="bf9e0-112">Create a new sales order.</span></span> <span data-ttu-id="bf9e0-113">Nánari upplýsingar eru í [Hvernig á að: selja vörur.](sales-how-sell-products.md)</span><span class="sxs-lookup"><span data-stu-id="bf9e0-113">For more information, see [How to: sell Products](sales-how-sell-products.md).</span></span>  

    <span data-ttu-id="bf9e0-114">Á flýtiflipanum **Fyrirframgreiðsla**, er reiturinn **Fyrirframgreiðsla %** fylltur út sjálfkrafa ef sjálfgefin fyrirframgreiðsluprósenta er til staðar í viðskiptamannsspjaldinu.</span><span class="sxs-lookup"><span data-stu-id="bf9e0-114">On the **Prepayment** FastTab, the **Prepayment %** field will be filled in automatically if there is a default prepayment percentage on the customer card.</span></span> <span data-ttu-id="bf9e0-115">Hægt er að breyta efni þessa reits.</span><span class="sxs-lookup"><span data-stu-id="bf9e0-115">You can change the contents of the field.</span></span> <span data-ttu-id="bf9e0-116">Fyrirframgreiðslan er eingöngu afrituð úr hausnum í línur sem ekki afrita sjálfgefna fyrirframgreiðsluprósentu úr vörunni.</span><span class="sxs-lookup"><span data-stu-id="bf9e0-116">The prepayment percentage is only copied from the header to lines that do not copy the default prepayment percentage from the item.</span></span>  

    <span data-ttu-id="bf9e0-117">Ef reiturinn **Þjappa fyrirframgreiðslu** er valinn verða línur sameinaðar á reikningnum ef:</span><span class="sxs-lookup"><span data-stu-id="bf9e0-117">If the **Compress Prepayment** field is selected, lines will be combined on the invoice if:</span></span>  
    - <span data-ttu-id="bf9e0-118">Þær eru með sama fjárhagsreikninginn fyrir fyrirframgreiðslur samkvæmt stillingum í almenna bókunargrunninum.</span><span class="sxs-lookup"><span data-stu-id="bf9e0-118">They have the same general ledger account for prepayments as determined by the general posting setup.</span></span>  
    - <span data-ttu-id="bf9e0-119">Þeir hafa sömu víddir.</span><span class="sxs-lookup"><span data-stu-id="bf9e0-119">They have the same dimensions.</span></span>  

    <span data-ttu-id="bf9e0-120">Þessi reitur er hafður auður ef tilgreina á fyrirframgreiðslureikning með einni línu fyrir hverja sölupöntunarlínu sem er með fyrirframgreiðsluprósentu.</span><span class="sxs-lookup"><span data-stu-id="bf9e0-120">Leave the field blank if you want to specify a prepayment invoice with one line for each sales order line that has a prepayment percentage.</span></span>  

3. <span data-ttu-id="bf9e0-121">Sölulínurnar eru fylltar út.</span><span class="sxs-lookup"><span data-stu-id="bf9e0-121">Fill in the sales lines.</span></span>  

    <span data-ttu-id="bf9e0-122">Ef sjálfgefnar fyrirframgreiðsluprósentur hafa verið settar upp fyrir vörurnar eru þær afritaðar sjálfvirkt í reitinn **Fyrirframgreiðsla %** í línunni.</span><span class="sxs-lookup"><span data-stu-id="bf9e0-122">If default prepayment percentages have been set up for your items, they are automatically copied to the **Prepayment %** field on the line.</span></span> <span data-ttu-id="bf9e0-123">Annars er prósentan afrituð úr hausnum.</span><span class="sxs-lookup"><span data-stu-id="bf9e0-123">Otherwise, the prepayment percentage is copied from the header.</span></span> <span data-ttu-id="bf9e0-124">Hægt er að breyta innihaldi reitsins **Fyrirframgreiðsla %** í línunni.</span><span class="sxs-lookup"><span data-stu-id="bf9e0-124">You can change the contents of the **Prepayment %** field on the line.</span></span>  
4. <span data-ttu-id="bf9e0-125">Ef þú vilt jafna eina fyriframgreiðsluprósentu við heildarpöntunina, breyttu þá **Fyrirframgreiðsla %** reitnum á hausnum eftir að hafa fyllt inn í þessar línur.</span><span class="sxs-lookup"><span data-stu-id="bf9e0-125">If you want to apply one prepayment percentage to the entire order, change the **Prepayment %** field on the header after filling in the lines.</span></span>  
5. <span data-ttu-id="bf9e0-126">Veldu **Upplýsingar** aðgerðina til að skoða heildarupphæð fyrirframgreiðslu.</span><span class="sxs-lookup"><span data-stu-id="bf9e0-126">To view the total prepayment amount, choose the **Statistics** action.</span></span>

    <span data-ttu-id="bf9e0-127">Ef leiðrétta á heildarupphæð fyrirframgreiðslunnar fyrir pöntunina er hægt að breyta innihaldi reitsins **Upphæð fyrirframgreiðslu** í glugganum **Tölfræði sölupöntunar**.</span><span class="sxs-lookup"><span data-stu-id="bf9e0-127">If you want to adjust the total prepayment amount for the order, you can change the contents of the **Prepayment Amount** field in the **Sales Order Statistics** window.</span></span>  

    <span data-ttu-id="bf9e0-128">Ef reiturinn **Verð ásamt VSK** er valinn er hægt að breyta reitnum **Upphæð fyrirframgreiðslu með VSK**.</span><span class="sxs-lookup"><span data-stu-id="bf9e0-128">If the **Prices Including VAT** field is selected, the **Prepayment Amount Incl. VAT** field is editable.</span></span>  

    <span data-ttu-id="bf9e0-129">Ef þú breytir innihaldi reitsins **Fyrirframgreiðsluupphæð**, mun upphæðinni verða dreift hlutfallslega á milli allra lína, nema þeirra sem hafa **0** í reitnum **Fyrirframgreiðsla %**.</span><span class="sxs-lookup"><span data-stu-id="bf9e0-129">If you change the contents of the **Prepayment Amount** field, the amount will be distributed proportionately between all lines, except those that have **0** in the **Prepayment %** field.</span></span>  
6. <span data-ttu-id="bf9e0-130">Til að prenta prufuskýrslu áður en fyrirframgreiðslureikningurinn er bókaður skal velja aðgerðina **Fyrirframgreiðsla**, og síðan aðgerðina **Prufuskýrsla fyrirframgreiðslu**.</span><span class="sxs-lookup"><span data-stu-id="bf9e0-130">To print a test report before posting the prepayment invoice, choose the **Prepayment** action, and then choose the **Prepayment Test Report** action.</span></span>  
7. <span data-ttu-id="bf9e0-131">Til að bóka fyrirframgreiðslureikningurinn skal velja aðgerðina **Fyrirframgreiðsla**, og síðan aðgerðina **Bóka fyrirframgreiðslureikning**.</span><span class="sxs-lookup"><span data-stu-id="bf9e0-131">To post the prepayment invoice, choose the **Prepayment** action, and then choose the **Post Prepayment Invoice** action.</span></span>  

    <span data-ttu-id="bf9e0-132">Fyrirframgreiðslureikningur er bókaður og prentaður með því að velja aðgerðina **Bóka og prenta fyrirframgr.reikning**.</span><span class="sxs-lookup"><span data-stu-id="bf9e0-132">To post and print the prepayment invoice, choose the **Post and Print Prepmt. Invoice** action.</span></span>  

<span data-ttu-id="bf9e0-133">Hægt er að gefa út viðbótar fyrirframgreiðslureikninga fyrir pöntunina.</span><span class="sxs-lookup"><span data-stu-id="bf9e0-133">You can issue additional prepayment invoices for the order.</span></span> <span data-ttu-id="bf9e0-134">Þetta er gert með því að hækka upphæð fyrirframgreiðslunnar í einni eða fleiri línum, leiðrétta dagsetningu fylgiskjalsins, ef þess þarf, og bóka fyrirframgreiðslureikninginn.</span><span class="sxs-lookup"><span data-stu-id="bf9e0-134">To do this, increase the prepayment amount on one or more lines, adjust the document date if necessary, and post the prepayment invoice.</span></span> <span data-ttu-id="bf9e0-135">Nýr reikningur er stofnaður fyrir mismuninn á milli reikningsfærðra upphæða fyrirframgreiðslu og nýju fyrirframgreiðsluupphæðarinnar.</span><span class="sxs-lookup"><span data-stu-id="bf9e0-135">A new invoice will be created for the difference between the prepayment amounts invoiced so far and the new prepayment amount.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="bf9e0-136">Ef þú ert í Norður Ameríku, geturðu ekki breytt fyrirframgreiðsluprósentunni eftir að fyrirframgreiðslureikningurinn hefur verið bókaður.</span><span class="sxs-lookup"><span data-stu-id="bf9e0-136">If you are located in North America, you cannot change the prepayment percentage after the prepayment invoice has been posted.</span></span> <span data-ttu-id="bf9e0-137">Í N-amerísku útgáfu [!INCLUDE[d365fin](includes/d365fin_md.md)] er komið í veg fyrir þetta, því útreikningur söluskatts yrði annars rangur.</span><span class="sxs-lookup"><span data-stu-id="bf9e0-137">This is prevented in the North American version of [!INCLUDE[d365fin](includes/d365fin_md.md)] because the calculation of sales tax will otherwise be incorrect.</span></span>  

 <span data-ttu-id="bf9e0-138">Þegar hægt er að bóka restina af reikningnum er hann bókaður eins og hver annar reikningur og fyrirframgreiðsluupphæðin er sjálfvirkt dregin frá þeirri upphæð sem greiða á.</span><span class="sxs-lookup"><span data-stu-id="bf9e0-138">When you are ready to post the rest of the invoice, post it as you would post any invoice, and the prepayment amount will automatically be deducted from the amount due.</span></span>  

## <a name="see-also"></a><span data-ttu-id="bf9e0-139">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="bf9e0-139">See Also</span></span>  
[<span data-ttu-id="bf9e0-140">Reikningsfærsla fyrirframgreiðslna</span><span class="sxs-lookup"><span data-stu-id="bf9e0-140">Invoicing Prepayments</span></span>](finance-invoice-prepayments.md)  
[<span data-ttu-id="bf9e0-141">Kynning: Uppsetning og reikningsfærsla fyrirframgreiðslna fyrir sölu</span><span class="sxs-lookup"><span data-stu-id="bf9e0-141">Walkthrough: Setting Up and Invoicing Sales Prepayments</span></span>](walkthrough-setting-up-and-invoicing-sales-prepayments.md)  
[<span data-ttu-id="bf9e0-142">Fjármál</span><span class="sxs-lookup"><span data-stu-id="bf9e0-142">Finance</span></span>](finance.md)  
<span data-ttu-id="bf9e0-143">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="bf9e0-143">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

