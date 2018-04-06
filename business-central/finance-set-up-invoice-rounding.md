---
title: "Setja upp reikningur sléttun | Microsoft Docs"
description: "Hægt er að slétta upphæðir reikninga þegar reikningar eru stofnaðir. Staðbundnar reglugerðir eða venjur gætu krafist ákveðinnar aðferðar við sléttun reikningsins, til dæmis að upphæð sem deila má í með 0,05."
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/15/2017
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 7e140c8c6d31864f6b27f4993e973b42904b0541
ms.contentlocale: is-is
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-invoice-rounding"></a><span data-ttu-id="19e56-104">Uppsetning sléttunargerðar reikninga</span><span class="sxs-lookup"><span data-stu-id="19e56-104">Set Up Invoice Rounding</span></span>
<span data-ttu-id="19e56-105">Ef þörf er á að slétta upphæðir reikninga þegar reikningar eru stofnaðir, má nota sjálfvirku sléttunaraðferðina.</span><span class="sxs-lookup"><span data-stu-id="19e56-105">If you need to round invoice amounts when you create invoices, you can use the automatic rounding function.</span></span> <span data-ttu-id="19e56-106">Þegar reikningur er sléttaður er bætt við aukalínu með sléttunarupphæðinni og þessi lína er bókuð með hinum reikningslínunum.</span><span class="sxs-lookup"><span data-stu-id="19e56-106">When an invoice is rounded, an extra line is added with the rounding amount and posted with the other invoice lines.</span></span>

> [!NOTE]  
>  <span data-ttu-id="19e56-107">Staðbundnar reglugerðir eða venjur gætu krafist ákveðinnar aðferðar við sléttun reikningsins, til dæmis að upphæð sem deila má í með 0,05.</span><span class="sxs-lookup"><span data-stu-id="19e56-107">Local regulations or local custom may require the invoice to be rounded in a specific way, for example, to an amount divisible by 0.05.</span></span>  
  
<span data-ttu-id="19e56-108">Til að nota sjálvirka sléttun reiknings þarf að:</span><span class="sxs-lookup"><span data-stu-id="19e56-108">To use automatic invoice rounding, you must:</span></span>  
  
* <span data-ttu-id="19e56-109">Tilgreina fjárhagsreikningana sem bóka á sléttunarmun í.</span><span class="sxs-lookup"><span data-stu-id="19e56-109">Specify the general ledger accounts to which rounding differences will be posted.</span></span>  
* <span data-ttu-id="19e56-110">Setja upp reglur fyrir sléttun reikninga í staðbundnum gjaldmiðli og erlendum gjaldmiðli.</span><span class="sxs-lookup"><span data-stu-id="19e56-110">Set up rules for rounding invoices in local currency and in foreign currency.</span></span>  
* <span data-ttu-id="19e56-111">Virkja eiginleikann.</span><span class="sxs-lookup"><span data-stu-id="19e56-111">Activate the function.</span></span>  
  
> [!NOTE]  
>  <span data-ttu-id="19e56-112">Auk jöfnunareiginleika reiknings má slétta upphæðir reikninga með eiginleikunum sléttun einingaupphæða og sléttun upphæða.</span><span class="sxs-lookup"><span data-stu-id="19e56-112">In addition to the invoice rounding features, you can round amounts on invoices by the unit-amount rounding feature and the amount rounding feature.</span></span>  
 
## <a name="set-up-general-ledger-accounts-for-invoice-rounding-differences"></a><span data-ttu-id="19e56-113">Uppsetning fjárhagsreikninga fyrir sléttunarmismun reikninga</span><span class="sxs-lookup"><span data-stu-id="19e56-113">Set up general ledger accounts for invoice rounding differences</span></span>
<span data-ttu-id="19e56-114">Ef nota á sjálfvirka reikningssléttunaraðgerð forritsins þarf að setja upp fjárhagsreikning eða reikninga þar sem sléttunarmismunur verður bókaður.</span><span class="sxs-lookup"><span data-stu-id="19e56-114">To use the automatic invoice rounding function, you must set up the general ledger account or accounts where rounding differences will be posted.</span></span> <span data-ttu-id="19e56-115">Áður en þetta er hægt þarf að setja upp VSK-vörubókunarflokka.</span><span class="sxs-lookup"><span data-stu-id="19e56-115">Before you can do this, you must set up VAT product posting groups.</span></span> <span data-ttu-id="19e56-116">Nánari upplýsingar um það eru í [Setja upp VSK](finance-setup-vat.md).</span><span class="sxs-lookup"><span data-stu-id="19e56-116">For more information, see [Set up VAT](finance-setup-vat.md).</span></span>  
  
### <a name="to-set-up-general-ledger-accounts-for-invoice-rounding-differences"></a><span data-ttu-id="19e56-117">Uppsetning fjárhagsreikninga fyrir sléttunarmismun reikninga</span><span class="sxs-lookup"><span data-stu-id="19e56-117">To set up general ledger accounts for invoice rounding differences</span></span>  
1. <span data-ttu-id="19e56-118">Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **bókhaldslykill** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="19e56-118">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Chart of Accounts**, and then choose the related link.</span></span>  
2. <span data-ttu-id="19e56-119">Reikningurinn er settur upp á síðunni **Bókhaldslykill** og honum er gefið heitið **Reikningssléttun** eða eitthvað álíka.</span><span class="sxs-lookup"><span data-stu-id="19e56-119">On the **Chart of Accounts** page, set up the account and name it **Invoice Rounding** or something similar.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="19e56-120"> notar reikningsheitið sem texta fyrir reikninga sem eru sléttaðir.</span><span class="sxs-lookup"><span data-stu-id="19e56-120"> will use the account name as text for invoices that are rounded.</span></span>  
3. <span data-ttu-id="19e56-121">Velja skal bókunarflokka fyrir sléttaðar upphæðir í reitunum **Söluskattur vörubókunarflokkur** eða **VSK vörubókunarflokkur**, út frá því hvort notaður er VSK eða söluskattur.</span><span class="sxs-lookup"><span data-stu-id="19e56-121">Depending on whether you use VAT or sales tax, in the **Tax Prod. Posting Group** or **VAT Prod. Posting Group** fields, choose a posting group for rounded amounts.</span></span> <span data-ttu-id="19e56-122">Ráðlegt að setja upp kóta nýja hópsins sem hægt er að nota fyrir reikningssléttun.</span><span class="sxs-lookup"><span data-stu-id="19e56-122">You may want to set up a new group code to use for invoice rounding.</span></span>
4. <span data-ttu-id="19e56-123">Reiturinn **Alm. bókunarflokkur**, og annað hvort **Viðsk.bókunarflokkur söluskatts** eða **Viðsk.bókunarflokkur VSK** reiturinn eru hafðir auðir.</span><span class="sxs-lookup"><span data-stu-id="19e56-123">Leave the **Gen. Posting Type**, and either the **Tax Bus. Posting Group** or **VAT Bus. Posting Group** fields blank.</span></span> <!-- Why do we say to leave these blank, when there are a lot of other fields we also leave blank but don't mention? -->  
  
<span data-ttu-id="19e56-124">Nú getur þú úthlutað sléttunarreikningnum til bókunarflokkanna á síðunni **Bókunarflokkar Lánardrottinn**.</span><span class="sxs-lookup"><span data-stu-id="19e56-124">Now you can assign the invoice rounding account to posting groups on the **Vendor Posting Groups** page.</span></span>  <!-- Why only the vendor posting groups? -->

## <a name="set-up-rounding-for-foreign-and-local-currencies"></a><span data-ttu-id="19e56-125">Uppsetning sléttunar fyrir erlendan og staðbundinn gjaldmiðil</span><span class="sxs-lookup"><span data-stu-id="19e56-125">Set up rounding for foreign and local currencies</span></span>
<span data-ttu-id="19e56-126">Áður en hægt er að nota sjálfvirku reikningssléttunaraðferðina þarf að setja upp sléttunarreglur fyrir erlenda og staðbundna gjaldmiðla.</span><span class="sxs-lookup"><span data-stu-id="19e56-126">Before you can use the automatic invoice rounding function, you must set up rounding rules for foreign and local currencies.</span></span>

### <a name="to-set-up-rounding-for-foreign-currencies"></a><span data-ttu-id="19e56-127">Uppsetning sléttunar fyrir erlendan gjaldmiðil</span><span class="sxs-lookup"><span data-stu-id="19e56-127">To set up rounding for foreign currencies</span></span>  
1. <span data-ttu-id="19e56-128">Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Gjaldmiðlar** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="19e56-128">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Currencies**, and then choose the related link.</span></span>  
2. <span data-ttu-id="19e56-129">Á síðunni **Gjaldmiðlar** skal velja þann erlenda gjaldmiðil sem opna á í **Gjaldmiðilskort** og síðan fylla í reitina **Upphæð sléttunarnákvæmni**, **Eining-Upphæð sléttunarnákvæmni**, **Reikningssléttunarnákvæmni** og **Reikningssléttunartegund**.</span><span class="sxs-lookup"><span data-stu-id="19e56-129">On the **Currencies** page, choose the foreign currency to open the **Currency Card**, and then fill in the **Amount Rounding Precision**, **Unit-Amount Rounding Precision**, **Invoice Rounding Precision** and **Invoice Rounding Type** fields.</span></span>
  
### <a name="to-set-up-rounding-for-your-local-currency"></a><span data-ttu-id="19e56-130">Uppsetning sléttunar fyrir þinn staðbundna gjaldmiðil</span><span class="sxs-lookup"><span data-stu-id="19e56-130">To set up rounding for your local currency</span></span>
1. <span data-ttu-id="19e56-131">Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Uppsetning fjárhags** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="19e56-131">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **General Ledger Setup**, and then choose the related link.</span></span>  
2. <span data-ttu-id="19e56-132">Á **Uppsetning fjárhags** síðunni á flýtiflipanum **Almennt** velurðu **Reikningssléttunarnákvæmni** og svo **Reikningssléttunargerð** reitina.</span><span class="sxs-lookup"><span data-stu-id="19e56-132">On the **General Ledger Setup** page, on the **General** FastTab, fill in the **Inv. Rounding Precision** and **Inv. Rounding Type** fields.</span></span>  

## <a name="activate-the-invoice-rounding-function"></a><span data-ttu-id="19e56-133">Virkja aðgerðina fyrir reikningssléttun</span><span class="sxs-lookup"><span data-stu-id="19e56-133">Activate the invoice rounding function</span></span>  
<span data-ttu-id="19e56-134">Ef forritið á örugglega að slétta sölu- og innkaupareikninga sjálfkrafa þarf að gera reikningssléttunaraðgerðina virka.</span><span class="sxs-lookup"><span data-stu-id="19e56-134">To ensure that sales and purchase invoices are rounded automatically, you must activate the invoice rounding function.</span></span> <span data-ttu-id="19e56-135">Hægt er að gera reikningssléttun virka fyrir sölu- og innkaupareikninga sérstaklega.</span><span class="sxs-lookup"><span data-stu-id="19e56-135">You activate invoice rounding separately for sales and purchase invoices.</span></span>

1. <span data-ttu-id="19e56-136">Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Uppsetning sölu & útistandandi** eða **Uppsetning Innkaup & viðskiptaskuldir** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="19e56-136">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Sales & Receivables Setup** or **Purchases & Payables Setup**, and then choose the related link.</span></span>  
2. <span data-ttu-id="19e56-137">Á flýtiflipanum **Almennt** skal velja gátreitinn **Sléttun reiknings**.</span><span class="sxs-lookup"><span data-stu-id="19e56-137">On the **General** FastTab, choose the **Invoice Rounding** check box.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="19e56-138">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="19e56-138">See Also</span></span>  
[<span data-ttu-id="19e56-139">Reikningsfæra sölur</span><span class="sxs-lookup"><span data-stu-id="19e56-139">Invoice Sales</span></span>](sales-how-invoice-sales.md)  
[<span data-ttu-id="19e56-140">Skrá innkaup</span><span class="sxs-lookup"><span data-stu-id="19e56-140">Record Purchases</span></span>](purchasing-how-record-purchases.md)
