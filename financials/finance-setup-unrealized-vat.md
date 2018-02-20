---
title: "Uppsetning á óinnleystum virðisaukaskatti | Microsoft Docs"
description: "Ef þú ert að nota bókhaldsreikning getur þú tilgreint hvernig á að meðhöndla óinnleyst virðisaukaskatt vegna sölu og kaupa."
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: cash, VAT, unrealized, cash-based
ms.date: 09/08/2017
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: b8bbfac583e1e7ec7eedae9e412b4fd3ac956d0f
ms.contentlocale: is-is
ms.lasthandoff: 01/30/2018

---

# <a name="set-up-unrealized-vat-for-cash-based-accounting"></a><span data-ttu-id="7e70b-103">Uppsetning óinnleyst virðisaukaskatts fyrir reiðufé</span><span class="sxs-lookup"><span data-stu-id="7e70b-103">Set Up Unrealized VAT for Cash-Based Accounting</span></span>
<span data-ttu-id="7e70b-104">Ef þú ert að nota reikningsskilaaðferðir í reiðufé, getur þú sett upp [!INCLUDE[d365fin](includes/d365fin_md.md)] til að takast á við óinnleystan virðisaukaskatt.</span><span class="sxs-lookup"><span data-stu-id="7e70b-104">If you're using cash-based accounting methods, you can set up [!INCLUDE[d365fin](includes/d365fin_md.md)] to handle unrealized VAT.</span></span>

## <a name="to-use-general-ledger-accounts-for-unrealized-vat"></a><span data-ttu-id="7e70b-105">Nota fjárhagsreikninga fyrir óinnleystan virðisaukaskatt</span><span class="sxs-lookup"><span data-stu-id="7e70b-105">To use general ledger accounts for unrealized VAT</span></span>
<span data-ttu-id="7e70b-106">Hægt er að velja að VSK-upphæðir verði reiknaðar og bókaðar á bráðabirgðafjárhagsreikning þegar reikningur er bókaður, og síðan bókaður á rétta fjárhagsreikninginn og settur í VSK-yfirlitin þegar endanlega greiðsluupphæð reikningsins er bókuð.</span><span class="sxs-lookup"><span data-stu-id="7e70b-106">You can choose to have VAT amounts calculated and posted to a temporary general ledger account when an invoice is posted, and then posted to the correct general ledger account and included in VAT statements when the actual payment of the invoice is posted.</span></span> <span data-ttu-id="7e70b-107">Áður en þetta er hægt þarf að ljúka við VSK-bókunargrunninn.</span><span class="sxs-lookup"><span data-stu-id="7e70b-107">Before you can do this, you must complete the VAT posting setup.</span></span>

<span data-ttu-id="7e70b-108">Til að nota reikninga fyrir óinnleyst virðisaukaskatt skaltu fylgja þessum skrefum:</span><span class="sxs-lookup"><span data-stu-id="7e70b-108">To use accounts for unrealized VAT, follow these steps:</span></span>
1. <span data-ttu-id="7e70b-109">Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Uppsetning fjárhags** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="7e70b-109">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, and enter **General Ledger Setup**.</span></span>
2. <span data-ttu-id="7e70b-110">Á **Uppsetning fjárhags** síðunni á flýtiflipanum **Almennt** velurðu **Sýna meira** og svo **Óinnleystur VSK** gátreitinn.</span><span class="sxs-lookup"><span data-stu-id="7e70b-110">On the **General Ledger Setup** page, on the **General** FastTab, choose **Show More**, and then choose the **Unrealized VAT** check box.</span></span>
3. <span data-ttu-id="7e70b-111">Lokaðu síðunni.</span><span class="sxs-lookup"><span data-stu-id="7e70b-111">Close the page.</span></span>
4. <span data-ttu-id="7e70b-112">velja **Leita að síðu eða skýrslu** táknið ![Leita að síðu eða skýrslu](media/ui-search/search_small.png "Leita að síðu eða skýrslu táknið"), færa inn **VSK-bókunargrunnur**.</span><span class="sxs-lookup"><span data-stu-id="7e70b-112">choose the **Search for Page or Report** icon ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon"), and enter **VAT Posting Setup**.</span></span>
5. <span data-ttu-id="7e70b-113">Á **VSK-bókunargrunnur** velurðu VSK-bókunarflokk og síðan **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="7e70b-113">On the **VAT Posting Setup** page, choose the VAT posting group, and then choose **Edit**.</span></span>
6. <span data-ttu-id="7e70b-114">Í reitnum **Tegund áætlaðs VSK**, veldu valkost til að tilgreina hvernig á að úthluta greiðslum til reikningsupphæð (án virðisaukaskatts) og virðisaukaskatts sjálfs og hvernig á að flytja virðisfjárhæðir úr óreynduðu virðisaukaskatti á reikninginn.</span><span class="sxs-lookup"><span data-stu-id="7e70b-114">In the **Unrealized VAT Type** field, choose an option to specify how to allocate payments to the invoice amount (excluding VAT) and the VAT amount itself, and how to transfer VAT amounts from the unrealized VAT account to the realized account.</span></span> <span data-ttu-id="7e70b-115">Eftirfarandi tafla lýsir valkostunum.</span><span class="sxs-lookup"><span data-stu-id="7e70b-115">The following table describes the options.</span></span>

| <span data-ttu-id="7e70b-116">Valkostur</span><span class="sxs-lookup"><span data-stu-id="7e70b-116">Option</span></span> | <span data-ttu-id="7e70b-117">Lýsing</span><span class="sxs-lookup"><span data-stu-id="7e70b-117">Description</span></span> |
| --- | --- |
| <span data-ttu-id="7e70b-118">Autt</span><span class="sxs-lookup"><span data-stu-id="7e70b-118">Blank</span></span> | <span data-ttu-id="7e70b-119">Veldu þennan valkost ef þú vilt ekki nota óinnleystur virðisaukaskatt.</span><span class="sxs-lookup"><span data-stu-id="7e70b-119">Choose this option if you don't want to use the unrealized VAT feature.</span></span> |
| <span data-ttu-id="7e70b-120">prósentu</span><span class="sxs-lookup"><span data-stu-id="7e70b-120">Percentage</span></span> | <span data-ttu-id="7e70b-121">Greiðslur nær bæði virðisaukaskatti og reikningsupphæðinni í hlutfalli við hlutfall greiðslunnar af því sem eftir er af reikningnum.</span><span class="sxs-lookup"><span data-stu-id="7e70b-121">Payments covers both VAT and the invoice amount in proportion to the payment's percentage of the remaining invoice amount.</span></span> <span data-ttu-id="7e70b-122">Greiddur virðisaukaskattur er fluttur frá óinnleyst VSK reikningi til áttaðs VSK reikning.</span><span class="sxs-lookup"><span data-stu-id="7e70b-122">The paid VAT amount is transferred from the unrealized VAT account to the realized VAT account.</span></span> |
| <span data-ttu-id="7e70b-123">Fyrsta</span><span class="sxs-lookup"><span data-stu-id="7e70b-123">First</span></span> | <span data-ttu-id="7e70b-124">Greiðslur ná fyrst yfir virðisaukaskatt og síðan reikningsupphæðir.</span><span class="sxs-lookup"><span data-stu-id="7e70b-124">Payments cover VAT first and then invoice amounts.</span></span> <span data-ttu-id="7e70b-125">Þegar svo vill til verður upphæð sem flutt er af reikningi áætlaðs VSK á VSK-reikning jöfn upphæð greiðslu uns VSK er greiddur að fullu.</span><span class="sxs-lookup"><span data-stu-id="7e70b-125">In this case, the amount transferred from the unrealized VAT account to the VAT account will equal the amount of the payment until the total VAT has been paid.</span></span> |
| <span data-ttu-id="7e70b-126">Síðasta</span><span class="sxs-lookup"><span data-stu-id="7e70b-126">Last</span></span> | <span data-ttu-id="7e70b-127">Greiðslur taka fyrst til reikningsupphæðar og síðan VSK.</span><span class="sxs-lookup"><span data-stu-id="7e70b-127">Payments cover the invoice amount first and then VAT.</span></span> <span data-ttu-id="7e70b-128">Í þessu tilviki verður engin upphæð flutt úr óreiknuðu virðisaukaskatti til VSK reiknings þar til heildarfjárhæð reikningsins, án virðisaukaskatts, hefur verið greiddur.</span><span class="sxs-lookup"><span data-stu-id="7e70b-128">In this case, no amount will be transferred from the unrealized VAT account to the VAT account until the total amount of the invoice, excluding VAT, has been paid.</span></span> |
| <span data-ttu-id="7e70b-129">Fyrst (fullgreitt)</span><span class="sxs-lookup"><span data-stu-id="7e70b-129">First (Fully Paid)</span></span> | <span data-ttu-id="7e70b-130">Greiðslur munu ná til virðisaukaskatts fyrstu (eins og valkosturinn _Fyrst_) en engin upphæð verður flutt á VSK reikning fyrr en heildarupphæð virðisaukaskatts hefur verið greidd.</span><span class="sxs-lookup"><span data-stu-id="7e70b-130">Payments will cover VAT first (like the _First_ option), but no amount will be transferred to the VAT account until the full amount of VAT has been paid.</span></span> |
| <span data-ttu-id="7e70b-131">Síðast (fullgreitt)</span><span class="sxs-lookup"><span data-stu-id="7e70b-131">Last (Fully Paid)</span></span> | <span data-ttu-id="7e70b-132">Greiðslur verða fyrst og fremst gjaldfærð (eins og valkosturinn _Síðasti_) en engin upphæð verður flutt á VSK reikning fyrr en heildarupphæð virðisaukaskatts hefur verið greidd.</span><span class="sxs-lookup"><span data-stu-id="7e70b-132">Payments will cover invoice amount first (like the _Last_ option), but no amount will be transferred to the VAT account until the full amount of VAT has been paid.</span></span> |

6. <span data-ttu-id="7e70b-133">Í **Reikn. áætlaðs útskatts**, veldu reikning fyrir óinnleyst söluskatt.</span><span class="sxs-lookup"><span data-stu-id="7e70b-133">In the **Sales VAT Unreal. Account** field, choose the account for unrealized sales VAT.</span></span>

    > [!NOTE]  
>   <span data-ttu-id="7e70b-134">VSK upphæðin verður bókuð á þennan reikning, og verður þar til greiðslu viðskiptavinarins er bókuð.</span><span class="sxs-lookup"><span data-stu-id="7e70b-134">The VAT amount will be posted to this account, and stay there until the customer payment is posted.</span></span> <span data-ttu-id="7e70b-135">Fjárhæðin er síðan flutt á reikninginn vegna söluverðs.</span><span class="sxs-lookup"><span data-stu-id="7e70b-135">The amount is then transferred to the account for sales VAT.</span></span>
7. <span data-ttu-id="7e70b-136">Í reitinn **Reikn. áætlaðs innskatts** er færður áætlaður innskattur á fjárhagsreikninginn.</span><span class="sxs-lookup"><span data-stu-id="7e70b-136">In the **Purch. VAT Unreal. Account** field, enter the general ledger account for unrealized purchase VAT.</span></span>

    > [!NOTE]  
>   <span data-ttu-id="7e70b-137">VSK upphæðin verður bókuð á þennan reikning, og verður þar til greiðslu viðskiptavinarins er bókuð.</span><span class="sxs-lookup"><span data-stu-id="7e70b-137">The VAT amount will be posted to this account, and stay there until the customer payment is posted.</span></span> <span data-ttu-id="7e70b-138">Fjárhæðin er síðan flutt á reikninginn fyrir innskatt.</span><span class="sxs-lookup"><span data-stu-id="7e70b-138">The amount is then transferred to the account for purchase VAT.</span></span>

## <a name="see-also"></a><span data-ttu-id="7e70b-139">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="7e70b-139">See Also</span></span>
[<span data-ttu-id="7e70b-140">Uppsetning á virðisaukaskatti</span><span class="sxs-lookup"><span data-stu-id="7e70b-140">Setting Up Value Added Tax</span></span>](finance-setup-vat.md)

