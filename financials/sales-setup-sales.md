---
title: "Yfirlit yfir verkhluta grunnstillingar söluferla | Microsoft Docs"
description: "Útskýrir verkhluta sem felur í sér uppsetningu á reglum og gildum til skilgreiningar á sölustefnu og söluferlum."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: trade, sell, configure
ms.date: 10/26/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 6407b49cf9b5e844b4e0920ccf1fc299d96ae34f
ms.contentlocale: is-is
ms.lasthandoff: 01/30/2018

---
# <a name="setting-up-sales"></a><span data-ttu-id="50a58-103">Uppsetning sölu</span><span class="sxs-lookup"><span data-stu-id="50a58-103">Setting Up Sales</span></span>
<span data-ttu-id="50a58-104">Áður en hægt er að hefjast handa við að stýra söluferlum þarf að grunnstilla reglur og gildi sem ráða sölureglum fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="50a58-104">Before you can manage sales processes, you must configure the rules and values that define the company's sales policies.</span></span>

<span data-ttu-id="50a58-105">Þú verður að skilgreina almenna uppsetningu, svo sem hvaða söluskrár eru nauðsynlegar og hvernig gildi þeirra eru settar fram.</span><span class="sxs-lookup"><span data-stu-id="50a58-105">You must define the general setup, such as which sales documents are required and how their values are posted.</span></span> <span data-ttu-id="50a58-106">Þessi almenna uppsetning fer yfirleitt fram við innleiðingu í upphafi.</span><span class="sxs-lookup"><span data-stu-id="50a58-106">This general setup is typically performed once during the initial implementation.</span></span>

<span data-ttu-id="50a58-107">Sérstakar raðir verkefna sem tengjast skráningu nýrra viðskiptamanna er að skrá öll sérstök verð eða afsláttarsamninga sem þú hefur með hverjum viðskiptamanni.</span><span class="sxs-lookup"><span data-stu-id="50a58-107">A separate series of tasks related to registering new customers is to record any special price or discount agreements that you have with each customer.</span></span>

<span data-ttu-id="50a58-108">Uppsetning fjármálatendrar sölu, eins og greiðslumáti og gjaldmiðill, er fjallað um í hlutanum uppsetning fjármála.</span><span class="sxs-lookup"><span data-stu-id="50a58-108">Finance-related sales setup, such as payment methods and currencies, are covered in the Finance Setup section.</span></span> <span data-ttu-id="50a58-109">Nánari upplýsingar er að finna í [Uppsetning Fjármála](finance-setup-finance.md).</span><span class="sxs-lookup"><span data-stu-id="50a58-109">For more information, see [Setting Up Finance](finance-setup-finance.md).</span></span>

| <span data-ttu-id="50a58-110">Til</span><span class="sxs-lookup"><span data-stu-id="50a58-110">To</span></span> | <span data-ttu-id="50a58-111">Sjá</span><span class="sxs-lookup"><span data-stu-id="50a58-111">See</span></span> |
| --- | --- |
| <span data-ttu-id="50a58-112">Stofna viðskiptamannaspjald fyrir alla viðskiptamenn sem selt er til.</span><span class="sxs-lookup"><span data-stu-id="50a58-112">Create a customer card for each customer that you sell to.</span></span> |[<span data-ttu-id="50a58-113">Skrá nýja viðskiptamenn</span><span class="sxs-lookup"><span data-stu-id="50a58-113">Register New Customers</span></span>](sales-how-register-new-customers.md) |
| <span data-ttu-id="50a58-114">Gera viðskiptavinum kleift að greiða í gegnum paypal með því að velja paypal lógóið á söluskjölum</span><span class="sxs-lookup"><span data-stu-id="50a58-114">Enable customers to pay through PayPal by choosing the PayPal logo on sales documents.</span></span> |[<span data-ttu-id="50a58-115">Virkja greiðslur viðskiptamanna gegnum PayPal</span><span class="sxs-lookup"><span data-stu-id="50a58-115">Enable Customer Payment Through PayPal</span></span>](sales-how-enable-payment-service-extensions.md) |
| <span data-ttu-id="50a58-116">Sláðu inn mismunandi afslætti og sérstakt verð sem þú veitir viðskiptavinum eftir hlut, magni og / eða dagsetningu.</span><span class="sxs-lookup"><span data-stu-id="50a58-116">Enter the different discounts and special prices that you grant to customers depending on item, quantities, and/or date.</span></span> |[<span data-ttu-id="50a58-117">Skrá söluverð, afslátt og greiðslusamkomulag</span><span class="sxs-lookup"><span data-stu-id="50a58-117">Record Sales Price, Discount, and Payment Agreements</span></span>](sales-how-record-sales-price-discount-payment-agreements.md) |
| <span data-ttu-id="50a58-118">Setja upp sölumenn svo að hægt er að úthluta þeim á tengiliði viðskiptamanna eða mæla afköst sölumanna sem grunn til að reikna sölulaun eða bónusa.</span><span class="sxs-lookup"><span data-stu-id="50a58-118">Set up salespeople so that you can assign them to customer contacts or measure salespeople's performance as a basis for calculating the sales commission or bonus.</span></span> |[<span data-ttu-id="50a58-119">Setja upp sölumenn</span><span class="sxs-lookup"><span data-stu-id="50a58-119">Set Up Salespeople</span></span>](sales-how-setup-salespeople.md) |
| <span data-ttu-id="50a58-120">Tilgreint er fyrir tiltekin viðskiptamann eða alla viðskiptamenn hvernig söluskjöl eru send sjálfkrafa þegar **Bóka og senda**</span><span class="sxs-lookup"><span data-stu-id="50a58-120">Specify for individual customers or for all customers how sales documents are sent by default when you choose the **Post and Send** action.</span></span> |[<span data-ttu-id="50a58-121">Setja upp sendisnið skjala</span><span class="sxs-lookup"><span data-stu-id="50a58-121">Set Up Document Sending Profiles</span></span>](sales-how-setup-document-send-profiles.md) |
| <span data-ttu-id="50a58-122">Settu upp tölvupóst til að innihalda samantekt á upplýsingum í söluskjali sem er verið að senda.</span><span class="sxs-lookup"><span data-stu-id="50a58-122">Set your email up to contain a summary of information in the sales document that is being sent.</span></span> |<span data-ttu-id="50a58-123">[Senda skjöl í tölvupósti](ui-how-send-documents-email.md).</span><span class="sxs-lookup"><span data-stu-id="50a58-123">[Send Documents by Email](ui-how-send-documents-email.md).</span></span> |
|<span data-ttu-id="50a58-124">Notaðu EB vefþjónustu til að staðfesta að VSK-númerin viðskiptamanna.</span><span class="sxs-lookup"><span data-stu-id="50a58-124">Use an EU web service to verify a customer's VAT registration number.</span></span>|[<span data-ttu-id="50a58-125">Staðfesta VSK-skráningarnúmer</span><span class="sxs-lookup"><span data-stu-id="50a58-125">Verify VAT Registration Numbers</span></span>](finance-setup-vat.md)|
|<span data-ttu-id="50a58-126">Færa inn upplýsingar um mismunandi flutningsseljendur sem skipt er við, ásamt tengli á sendingarleitarþjónustu þeirra.</span><span class="sxs-lookup"><span data-stu-id="50a58-126">Enter information about the different transportation vendors you use, including a link to their package tracking service.</span></span>|[<span data-ttu-id="50a58-127">Uppsetning flutningsaðila</span><span class="sxs-lookup"><span data-stu-id="50a58-127">Set Up Shipping Agents</span></span>](sales-how-to-set-up-shipping-agents.md)|

## <a name="see-also"></a><span data-ttu-id="50a58-128">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="50a58-128">See Also</span></span>
[<span data-ttu-id="50a58-129">Sala</span><span class="sxs-lookup"><span data-stu-id="50a58-129">Sales</span></span>](sales-manage-sales.md)  
<span data-ttu-id="50a58-130">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="50a58-130">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

