---
title: "Uppsetning staðlaðra lína fyrir ítrekaða sölu og innkaup | Microsoft Docs"
description: "Hægt er að setja upp sölu- og innkaupalínur sem eru ítrekaðar og síðan færa þær inn í sölu- og innkaupaskjöl og fylla þannig á fljótlegan hátt út í línurnar með stöðluðum upplýsingum."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: trade, sell, replenishment
ms.date: 07/02/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: d3ce7b8065837d98b55b6e2dd1644f79b34e534a
ms.contentlocale: is-is
ms.lasthandoff: 03/22/2018

---
# <a name="create-recurring-sales-and-purchase-lines"></a><span data-ttu-id="d463e-103">Stofna ítrekaðar sölu- og innkaupalínur</span><span class="sxs-lookup"><span data-stu-id="d463e-103">Create Recurring Sales and Purchase Lines</span></span>
<span data-ttu-id="d463e-104">Ef þú þarft oft að stofna innkaupa- og sölulínur með svipuðum upplýsingum, geturðu sett upp staðlaðar línur, sem þú getur svo fært inn í ítrekuð sölu- og innkaupaskjöl, til dæmis fyrir endurteknar áfyllingapantanir.</span><span class="sxs-lookup"><span data-stu-id="d463e-104">If you often need to create sales and purchase lines with similar information, you can set up standard lines that you can then insert on recurring sales and purchase documents, for example, for recurring replenishment orders.</span></span>  

<span data-ttu-id="d463e-105">Eftirfarandi ferli sýnir hvernig skal vinna með staðlaðar sölulínur.</span><span class="sxs-lookup"><span data-stu-id="d463e-105">The following procedure shows how to work with standard sales lines.</span></span> <span data-ttu-id="d463e-106">Það virkar á svipaðan hátt fyrir staðlaðar innkaupalínur.</span><span class="sxs-lookup"><span data-stu-id="d463e-106">It works in a similar way for standard purchase lines.</span></span>  

## <a name="to-set-up-standard-sales-lines"></a><span data-ttu-id="d463e-107">Hvernig á að setja upp staðlaðar sölulínur</span><span class="sxs-lookup"><span data-stu-id="d463e-107">To set up standard sales lines</span></span>  
1. <span data-ttu-id="d463e-108">Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **staðlaður sölukóði** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="d463e-108">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Standard Sales Codes**, and then choose the related link.</span></span>  
2. <span data-ttu-id="d463e-109">Í glugganum **Staðlaðar sölulínur** skal velja aðgerðina **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="d463e-109">In the **Standard Sales Lines** window, choose the **New** action.</span></span>  
3. <span data-ttu-id="d463e-110">Fyllt er út í reiti eftir því sem er nauðsynlegt í flýtiflipanum **Almennt**.</span><span class="sxs-lookup"><span data-stu-id="d463e-110">On the **General** FastTab, fill the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
4. <span data-ttu-id="d463e-111">Á flýtiflipanum **Línur** skal færa inn upplýsingar í reitina til að undirbúa sölulínur sem endurspegla hinar stöðluðu línur sem þú býst við að nota sem endurteknar línur í söluskjölum.</span><span class="sxs-lookup"><span data-stu-id="d463e-111">On the **Lines** FastTab, enter information in the fields to prepare sales lines that reflect the standard lines that you expect to use as recurring lines on sales documents.</span></span>  

## <a name="to-insert-standard-sales-lines-on-a-sales-invoice"></a><span data-ttu-id="d463e-112">Staðlaðar sölulínur settar inn í sölureikning</span><span class="sxs-lookup"><span data-stu-id="d463e-112">To insert standard sales lines on a sales invoice</span></span>
1. <span data-ttu-id="d463e-113">Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Reikningar** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="d463e-113">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Invoices**, and then choose the related link.</span></span>
2. <span data-ttu-id="d463e-114">Opnið sölureikningur sem á að setja eina eða fleiri staðlaðar sölulínur inn í.</span><span class="sxs-lookup"><span data-stu-id="d463e-114">Open the sales invoice that you want to insert one or more standard sales lines on.</span></span>
3. <span data-ttu-id="d463e-115">Veljið aðgerðina **Sækja endurteknar sölulínur**.</span><span class="sxs-lookup"><span data-stu-id="d463e-115">Choose the **Get Recurring Sales Lines** action.</span></span>
4. <span data-ttu-id="d463e-116">Í glugganum **Endurteknar sölulínur** skal velja uppflettihnappinn á reitnum **Kóði** og síðan velja síðan safn staðlaðra sölulína.</span><span class="sxs-lookup"><span data-stu-id="d463e-116">In the **Recurring Sales Lines** window, choose the lookup button in the **Code** field, and then select a set of standard sales lines.</span></span>
5. <span data-ttu-id="d463e-117">Velja skal **Í lagi** hnappinn til að setja staðlaðar sölulínur inn á reikninginn, þar sem þú getur endurnotað þær sem fyrir eru eða breytt upplýsingunum.</span><span class="sxs-lookup"><span data-stu-id="d463e-117">Choose the **OK** button to insert the standard sales lines on the invoice, where you can reuse as is or edit the information.</span></span>

## <a name="to-create-multiple-sales-invoices-based-on-standard-sales-lines"></a><span data-ttu-id="d463e-118">Stofna marga sölureikninga byggða á stöðluðum sölulínum</span><span class="sxs-lookup"><span data-stu-id="d463e-118">To create multiple sales invoices based on standard sales lines</span></span>
<span data-ttu-id="d463e-119">Hægt er að nota runuvinnsluna **Stofna ítrekaða sölureikninga** til að stofna sölureikninga samkvæmt stöðluðum sölulínum sem eru tengdar við viðskiptamenn og með bókunardögum innan gildir-frá og gildir-til dagsetningum sem hafa verið tilgreindar í stöðluðum sölukóða.</span><span class="sxs-lookup"><span data-stu-id="d463e-119">You can use the **Create Recurring Sales Inv.** batch job to create sales invoices according to standard sales lines that are assigned to the customers and with posting dates within the valid-from and valid-to dates that you specify on the standard sales code.</span></span>

<span data-ttu-id="d463e-120">Í **Endurteknar sölulínur** glugganum er einnig hægt að tilgreina greiðsluaðferð fyrir beingreiðslu og beingreiðsluumboð.</span><span class="sxs-lookup"><span data-stu-id="d463e-120">In the **Recurring Sales Lines** window, you can also specify a direct-debit payment method and a direct-debit mandate.</span></span> <span data-ttu-id="d463e-121">Sölureikningar sem eru stofnaðir með runuvinnslunni **Stofna ítrekaða sölureikninga** munu þá innihalda upplýsingar sem krafist er til að innheimta greiðslu fyrir sölureikninga með SEPA-beingreiðslu.</span><span class="sxs-lookup"><span data-stu-id="d463e-121">The sales invoices that are created with the **Create Recurring Sales Inv.** batch job will then include information required to collect payment for the sales invoices with SEPA direct debit.</span></span> <span data-ttu-id="d463e-122">Nánari upplýsingar má nálgast á [Innheimta greiðslur með SEPA-beingreiðslum](finance-collect-payments-with-sepa-direct-debit.md)</span><span class="sxs-lookup"><span data-stu-id="d463e-122">For more information, see [Collecting Payments with SEPA Direct Debit](finance-collect-payments-with-sepa-direct-debit.md).</span></span>

1. <span data-ttu-id="d463e-123">Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Stofna endurtekna sölureikninga** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="d463e-123">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Create Recurring Sales Invoices**, and then choose the related link.</span></span>
2. <span data-ttu-id="d463e-124">Í glugganum **Búa til endurtekna sölureikninga** þarf að fylla reitina út eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="d463e-124">In the **Create Recurring Sales Inv.** window, fill in the fields as necessary.</span></span>
3. <span data-ttu-id="d463e-125">Í reitnum **Kóði** er færður inn kóðinn fyrir staðlaðar línur sem á að úthluta til viðskiptamanns sem þú vilt stofna sölureikning fyrir.</span><span class="sxs-lookup"><span data-stu-id="d463e-125">In the **Code** field, enter the code for standard sales lines assigned to a customer that you want to create sales invoices for.</span></span>
4. <span data-ttu-id="d463e-126">Velja hnappinn **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="d463e-126">Choose the **OK** button.</span></span>

<span data-ttu-id="d463e-127">Sölureikningar eru stofnaðir fyrir viðskiptamenn með stöðluðum sölukóða viðskiptamanna og öllum tilgreindum upplýsingum um beingreiðslur, fyrir bókun á tilteknum degi.</span><span class="sxs-lookup"><span data-stu-id="d463e-127">Sales invoices are created for the customers with the specified standard customer sales code, and any specified direct-debit information, for posting on the specified date.</span></span>

## <a name="see-also"></a><span data-ttu-id="d463e-128">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="d463e-128">See Also</span></span>  
[<span data-ttu-id="d463e-129">Sala</span><span class="sxs-lookup"><span data-stu-id="d463e-129">Sales</span></span>](sales-manage-sales.md)  
<span data-ttu-id="d463e-130">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="d463e-130">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

