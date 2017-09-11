---
title: "Uppsetning og notkun staðlaðra lína fyrir ítrekaða sölu og innkaup | Microsoft Docs"
description: "Hægt er að setja upp sölu- og innkaupalínur sem eru ítrekaðar og síðan færa þær inn í sölu- og innkaupaskjöl og fylla þannig á fljótlegan hátt út í línurnar með stöðluðum upplýsingum."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: trade, sell, replenishment
ms.date: 07/02/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 85d15de13739e944ff8817b402b37ae1c7e1b144
ms.openlocfilehash: 980a0646317c2b5c02c0eadcde9ba984c11580c4
ms.contentlocale: is-is
ms.lasthandoff: 09/11/2017


---
# <a name="how-to-create-recurring-sales-and-purchase-lines"></a><span data-ttu-id="1bc0b-103">Hvernig á að: Stofna ítrekaðar sölu- og innkaupalínur</span><span class="sxs-lookup"><span data-stu-id="1bc0b-103">How to: Create Recurring Sales and Purchase Lines</span></span>
<span data-ttu-id="1bc0b-104">Ef þú þarft oft að stofna innkaupa- og sölulínur með svipuðum upplýsingum, geturðu sett upp staðlaðar línur, sem þú getur svo fært inn í ítrekuð sölu- og innkaupaskjöl, til dæmis fyrir endurteknar áfyllingapantanir.</span><span class="sxs-lookup"><span data-stu-id="1bc0b-104">If you often need to create sales and purchase lines with similar information, you can set up standard lines that you can then insert on recurring sales and purchase documents, for example, for recurring replenishment orders.</span></span>  

<span data-ttu-id="1bc0b-105">Eftirfarandi ferli sýnir hvernig skal vinna með staðlaðar sölulínur.</span><span class="sxs-lookup"><span data-stu-id="1bc0b-105">The following procedure shows how to work with standard sales lines.</span></span> <span data-ttu-id="1bc0b-106">Það virkar á svipaðan hátt fyrir staðlaðar innkaupalínur.</span><span class="sxs-lookup"><span data-stu-id="1bc0b-106">It works in a similar way for standard purchase lines.</span></span>  

## <a name="to-set-up-standard-sales-lines"></a><span data-ttu-id="1bc0b-107">Hvernig á að setja upp staðlaðar sölulínur</span><span class="sxs-lookup"><span data-stu-id="1bc0b-107">To set up standard sales lines</span></span>  
1. <span data-ttu-id="1bc0b-108">Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **staðlaður sölukóði** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="1bc0b-108">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Standard Sales Codes**, and then choose the related link.</span></span>  
2. <span data-ttu-id="1bc0b-109">Í glugganum **Staðlaðar sölulínur** skal velja aðgerðina **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="1bc0b-109">In the **Standard Sales Lines** window, choose the **New** action.</span></span>  
3. <span data-ttu-id="1bc0b-110">Fyllt er út í reiti eftir því sem er nauðsynlegt í flýtiflipanum **Almennt**.</span><span class="sxs-lookup"><span data-stu-id="1bc0b-110">On the **General** FastTab, fill the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
4. <span data-ttu-id="1bc0b-111">Á flýtiflipanum **Línur** skal færa inn upplýsingar í reitina til að undirbúa sölulínur sem endurspegla hinar stöðluðu línur sem þú býst við að nota sem endurteknar línur í söluskjölum.</span><span class="sxs-lookup"><span data-stu-id="1bc0b-111">On the **Lines** FastTab, enter information in the fields to prepare sales lines that reflect the standard lines that you expect to use as recurring lines on sales documents.</span></span>  

## <a name="to-insert-standard-sales-lines-on-a-sales-invoice"></a><span data-ttu-id="1bc0b-112">Staðlaðar sölulínur settar inn í sölureikning</span><span class="sxs-lookup"><span data-stu-id="1bc0b-112">To insert standard sales lines on a sales invoice</span></span>
1. <span data-ttu-id="1bc0b-113">Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Reikningar** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="1bc0b-113">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Invoices**, and then choose the related link.</span></span>
2. <span data-ttu-id="1bc0b-114">Opnið sölureikningur sem á að setja eina eða fleiri staðlaðar sölulínur inn í.</span><span class="sxs-lookup"><span data-stu-id="1bc0b-114">Open the sales invoice that you want to insert one or more standard sales lines on.</span></span>
3. <span data-ttu-id="1bc0b-115">Veljið aðgerðina **Sækja endurteknar sölulínur**.</span><span class="sxs-lookup"><span data-stu-id="1bc0b-115">Choose the **Get Recurring Sales Lines** action.</span></span>
4. <span data-ttu-id="1bc0b-116">Í glugganum **Endurteknar sölulínur** skal velja uppflettihnappinn á reitnum **Kóði** og síðan velja síðan safn staðlaðra sölulína.</span><span class="sxs-lookup"><span data-stu-id="1bc0b-116">In the **Recurring Sales Lines** window, choose the lookup button in the **Code** field, and then select a set of standard sales lines.</span></span>
5. <span data-ttu-id="1bc0b-117">Velja skal **Í lagi** hnappinn til að setja staðlaðar sölulínur inn á reikninginn, þar sem þú getur endurnotað þær sem fyrir eru eða breytt upplýsingunum.</span><span class="sxs-lookup"><span data-stu-id="1bc0b-117">Choose the **OK** button to insert the standard sales lines on the invoice, where you can reuse as is or edit the information.</span></span>

## <a name="to-create-multiple-sales-invoices-based-on-standard-sales-lines"></a><span data-ttu-id="1bc0b-118">Stofna marga sölureikninga byggða á stöðluðum sölulínum</span><span class="sxs-lookup"><span data-stu-id="1bc0b-118">To create multiple sales invoices based on standard sales lines</span></span>
<span data-ttu-id="1bc0b-119">Hægt er að nota **Búa til endurtekna sölureikninga.**</span><span class="sxs-lookup"><span data-stu-id="1bc0b-119">You can use the **Create Recurring Sales Inv.**</span></span> <span data-ttu-id="1bc0b-120">runuvinnsluna til að stofna sölureikninga samkvæmt stöðluðum sölulínum sem eru tengdar við viðskiptamenn og með bókunardögum innan gildir-frá og gildir-til dagsetningum sem hafa verið tilgreindar í stöðluðum sölukóða.</span><span class="sxs-lookup"><span data-stu-id="1bc0b-120">batch job to create sales invoices according to standard sales lines that are assigned to the customers and with posting dates within the valid-from and valid-to dates that you specify on the standard sales code.</span></span>

<span data-ttu-id="1bc0b-121">Í **Endurteknar sölulínur** glugganum er einnig hægt að tilgreina greiðsluaðferð fyrir beingreiðslu og beingreiðsluumboð.</span><span class="sxs-lookup"><span data-stu-id="1bc0b-121">In the **Recurring Sales Lines** window, you can also specify a direct-debit payment method and a direct-debit mandate.</span></span> <span data-ttu-id="1bc0b-122">Sölureikningarnir sem eru stofnaðir með **Búa til endurtekna sölureikninga.**</span><span class="sxs-lookup"><span data-stu-id="1bc0b-122">The sales invoices that are created with the **Create Recurring Sales Inv.**</span></span> <span data-ttu-id="1bc0b-123">runuvinnslunni munu þá innihalda upplýsingar sem eru nauðsynlegar til innheimta greiðslu fyrir sölureikningana með SEPA-beingreiðslum.</span><span class="sxs-lookup"><span data-stu-id="1bc0b-123">batch job will then include information required to collect payment for the sales invoices with SEPA direct debit.</span></span> <span data-ttu-id="1bc0b-124">Nánari upplýsingar má nálgast á Innheimta greiðslur með SEPA-beingreiðslum</span><span class="sxs-lookup"><span data-stu-id="1bc0b-124">For more information, see Collect Payments with SEPA Direct Debit.</span></span>

1. <span data-ttu-id="1bc0b-125">Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Stofna endurtekna sölureikninga** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="1bc0b-125">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Create Recurring Sales Invoices**, and then choose the related link.</span></span>
2. <span data-ttu-id="1bc0b-126">Í glugganum **Stofna endurtekna sölureikninga**</span><span class="sxs-lookup"><span data-stu-id="1bc0b-126">In the **Create Recurring Sales Inv.**</span></span> <span data-ttu-id="1bc0b-127">skal fylla inn í reitina eins og þörf krefur.</span><span class="sxs-lookup"><span data-stu-id="1bc0b-127">window, fill in the fields as necessary.</span></span>
3. <span data-ttu-id="1bc0b-128">Í reitnum **Kóði** er færður inn kóðinn fyrir staðlaðar línur sem á að úthluta til viðskiptamanns sem þú vilt stofna sölureikning fyrir.</span><span class="sxs-lookup"><span data-stu-id="1bc0b-128">In the **Code** field, enter the code for standard sales lines assigned to a customer that you want to create sales invoices for.</span></span>
4. <span data-ttu-id="1bc0b-129">Velja hnappinn **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="1bc0b-129">Choose the **OK** button.</span></span>

<span data-ttu-id="1bc0b-130">Sölureikningar eru stofnaðir fyrir viðskiptamenn með stöðluðum sölukóða viðskiptamanna og öllum tilgreindum upplýsingum um beingreiðslur, fyrir bókun á tilteknum degi.</span><span class="sxs-lookup"><span data-stu-id="1bc0b-130">Sales invoices are created for the customers with the specified standard customer sales code, and any specified direct-debit information, for posting on the specified date.</span></span>

## <a name="see-also"></a><span data-ttu-id="1bc0b-131">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="1bc0b-131">See Also</span></span>  
[<span data-ttu-id="1bc0b-132">Sala</span><span class="sxs-lookup"><span data-stu-id="1bc0b-132">Sales</span></span>](sales-manage-sales.md)  
<span data-ttu-id="1bc0b-133">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="1bc0b-133">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

