---
title: Yfirlit yfir verkhluta grunnstillingar söluferla | Microsoft Docs
description: Útskýrir verkhluta sem felur í sér uppsetningu á reglum og gildum til skilgreiningar á sölustefnu og söluferlum.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: trade, sell, configure
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 83b27cbc0b1ddfe3114995218bc29c282d3508ca
ms.sourcegitcommit: 32bfc2acaaf3693afc9aeb86feea505fd328caa1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/19/2021
ms.locfileid: "5024363"
---
# <a name="setting-up-sales"></a><span data-ttu-id="138b8-103">Uppsetning sölu</span><span class="sxs-lookup"><span data-stu-id="138b8-103">Setting Up Sales</span></span>
<span data-ttu-id="138b8-104">Áður en hægt er að hefjast handa við að stýra söluferlum þarf að grunnstilla reglur og gildi sem ráða sölureglum fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="138b8-104">Before you can manage sales processes, you must configure the rules and values that define the company's sales policies.</span></span>

<span data-ttu-id="138b8-105">Þú verður að skilgreina almenna uppsetningu, svo sem hvaða söluskrár eru nauðsynlegar og hvernig gildi þeirra eru settar fram.</span><span class="sxs-lookup"><span data-stu-id="138b8-105">You must define the general setup, such as which sales documents are required and how their values are posted.</span></span> <span data-ttu-id="138b8-106">Þessi almenna uppsetning fer yfirleitt fram við innleiðingu í upphafi.</span><span class="sxs-lookup"><span data-stu-id="138b8-106">This general setup is typically performed once during the initial implementation.</span></span>

<span data-ttu-id="138b8-107">Sérstakar raðir verkefna sem tengjast skráningu nýrra viðskiptamanna er að skrá öll sérstök verð eða afsláttarsamninga sem þú hefur með hverjum viðskiptamanni.</span><span class="sxs-lookup"><span data-stu-id="138b8-107">A separate series of tasks related to registering new customers is to record any special price or discount agreements that you have with each customer.</span></span>

<span data-ttu-id="138b8-108">Uppsetning fjármálatendrar sölu, eins og greiðslumáti og gjaldmiðill, er fjallað um í hlutanum uppsetning fjármála.</span><span class="sxs-lookup"><span data-stu-id="138b8-108">Finance-related sales setup, such as payment methods and currencies, are covered in the Finance Setup section.</span></span> <span data-ttu-id="138b8-109">Nánari upplýsingar er að finna í [Uppsetning Fjármála](finance-setup-finance.md).</span><span class="sxs-lookup"><span data-stu-id="138b8-109">For more information, see [Setting Up Finance](finance-setup-finance.md).</span></span>

| <span data-ttu-id="138b8-110">Til</span><span class="sxs-lookup"><span data-stu-id="138b8-110">To</span></span> | <span data-ttu-id="138b8-111">Sjá</span><span class="sxs-lookup"><span data-stu-id="138b8-111">See</span></span> |
| --- | --- |
| <span data-ttu-id="138b8-112">Stofna viðskiptamannaspjald fyrir alla viðskiptamenn sem selt er til.</span><span class="sxs-lookup"><span data-stu-id="138b8-112">Create a customer card for each customer that you sell to.</span></span> |[<span data-ttu-id="138b8-113">Skrá nýja viðskiptamenn</span><span class="sxs-lookup"><span data-stu-id="138b8-113">Register New Customers</span></span>](sales-how-register-new-customers.md) |
| <span data-ttu-id="138b8-114">Gera viðskiptavinum kleift að greiða í gegnum paypal með því að velja paypal lógóið á söluskjölum</span><span class="sxs-lookup"><span data-stu-id="138b8-114">Enable customers to pay through PayPal by choosing the PayPal logo on sales documents.</span></span> |[<span data-ttu-id="138b8-115">Virkja greiðslur viðskiptamanna gegnum PayPal</span><span class="sxs-lookup"><span data-stu-id="138b8-115">Enable Customer Payment Through PayPal</span></span>](sales-how-enable-payment-service-extensions.md) |
| <span data-ttu-id="138b8-116">Sláðu inn mismunandi afslætti og sérstakt verð sem þú veitir viðskiptavinum eftir hlut, magni og / eða dagsetningu.</span><span class="sxs-lookup"><span data-stu-id="138b8-116">Enter the different discounts and special prices that you grant to customers depending on item, quantities, and/or date.</span></span> |[<span data-ttu-id="138b8-117">Skrá söluverð, afslátt og greiðslusamkomulag</span><span class="sxs-lookup"><span data-stu-id="138b8-117">Record Sales Price, Discount, and Payment Agreements</span></span>](sales-how-record-sales-price-discount-payment-agreements.md) |
| <span data-ttu-id="138b8-118">Setja upp sölumenn svo að hægt er að úthluta þeim á tengiliði viðskiptamanna eða mæla afköst sölumanna sem grunn til að reikna sölulaun eða bónusa.</span><span class="sxs-lookup"><span data-stu-id="138b8-118">Set up salespeople so that you can assign them to customer contacts or measure salespeople's performance as a basis for calculating the sales commission or bonus.</span></span> |[<span data-ttu-id="138b8-119">Setja upp sölumenn</span><span class="sxs-lookup"><span data-stu-id="138b8-119">Set Up Salespeople</span></span>](sales-how-setup-salespeople.md) |
| <span data-ttu-id="138b8-120">Tilgreint er fyrir tiltekin viðskiptamann eða alla viðskiptamenn hvernig söluskjöl eru send sjálfkrafa þegar **Bóka og senda**</span><span class="sxs-lookup"><span data-stu-id="138b8-120">Specify for individual customers or for all customers how sales documents are sent by default when you choose the **Post and Send** action.</span></span> |[<span data-ttu-id="138b8-121">Setja upp sendisnið skjala</span><span class="sxs-lookup"><span data-stu-id="138b8-121">Set Up Document Sending Profiles</span></span>](sales-how-setup-document-send-profiles.md) |
| <span data-ttu-id="138b8-122">Settu upp tölvupóst til að innihalda samantekt á upplýsingum í söluskjali sem er verið að senda.</span><span class="sxs-lookup"><span data-stu-id="138b8-122">Set your email up to contain a summary of information in the sales document that is being sent.</span></span> |<span data-ttu-id="138b8-123">[Senda skjöl í tölvupósti](ui-how-send-documents-email.md).</span><span class="sxs-lookup"><span data-stu-id="138b8-123">[Send Documents by Email](ui-how-send-documents-email.md).</span></span> |
|<span data-ttu-id="138b8-124">Notaðu EB vefþjónustu til að staðfesta að VSK-númerin viðskiptamanna.</span><span class="sxs-lookup"><span data-stu-id="138b8-124">Use an EU web service to verify a customer's VAT registration number.</span></span>|[<span data-ttu-id="138b8-125">Staðfesta VSK-skráningarnúmer</span><span class="sxs-lookup"><span data-stu-id="138b8-125">Verify VAT Registration Numbers</span></span>](finance-setup-vat.md)|
|<span data-ttu-id="138b8-126">Skilgreindu mismunandi inco-skilmála sem þú býður viðskiptamönnum upp á eða þá sem lánardrottnar þínir bjóða þér.</span><span class="sxs-lookup"><span data-stu-id="138b8-126">Define the different incoterms that you offer to customers or that your vendors offer you.</span></span>|[<span data-ttu-id="138b8-127">Afhendingarmátar settir upp</span><span class="sxs-lookup"><span data-stu-id="138b8-127">Set Up Shipment Methods</span></span>](sales-how-set-up-shipment-methods.md)|
|<span data-ttu-id="138b8-128">Færa inn upplýsingar um mismunandi flutningsseljendur sem skipt er við, ásamt tengli á sendingarleitarþjónustu þeirra.</span><span class="sxs-lookup"><span data-stu-id="138b8-128">Enter information about the different transportation vendors you use, including a link to their package tracking service.</span></span>|[<span data-ttu-id="138b8-129">Uppsetning flutningsaðila</span><span class="sxs-lookup"><span data-stu-id="138b8-129">Set Up Shipping Agents</span></span>](sales-how-to-set-up-shipping-agents.md)|
|<span data-ttu-id="138b8-130">Tilgreina sjálfgefnar skýrslur sem á að nota fyrir mismunandi skjalagerðir.</span><span class="sxs-lookup"><span data-stu-id="138b8-130">Specify default reports to be used for different document types.</span></span>|[<span data-ttu-id="138b8-131">Skýrsluval í Business Central</span><span class="sxs-lookup"><span data-stu-id="138b8-131">Report Selection in Business Central</span></span>](across-report-selections.md)|

## <a name="see-related-training-at-microsoft-learn"></a><span data-ttu-id="138b8-132">Sjá tengda þjálfun á [Microsoft Learn](/learn/paths/trade-get-started-dynamics-365-business-central/)</span><span class="sxs-lookup"><span data-stu-id="138b8-132">See Related Training at [Microsoft Learn](/learn/paths/trade-get-started-dynamics-365-business-central/)</span></span>

## <a name="see-also"></a><span data-ttu-id="138b8-133">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="138b8-133">See Also</span></span>
[<span data-ttu-id="138b8-134">Sala</span><span class="sxs-lookup"><span data-stu-id="138b8-134">Sales</span></span>](sales-manage-sales.md)  
<span data-ttu-id="138b8-135">[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="138b8-135">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>
