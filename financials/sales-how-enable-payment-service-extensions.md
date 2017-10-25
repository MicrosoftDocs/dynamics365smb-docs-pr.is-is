---
title: "Virkja greiðslur viðskiptamanna gegnum greiðsluþjónustu| Microsoft Docs"
description: "Gerðu það auðveldara fyrir viðskiptavini að greiða reikninga sína með því að virkja greiðsluþjónustu."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: online payment
ms.date: 07/07/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: c149949b939a551a14236c84f8ba7538fcb54bbe
ms.contentlocale: is-is
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-enable-customer-payments-through-payment-services"></a><span data-ttu-id="0e9ce-103">Hvernig á að: Virkja greiðslur viðskiptamanna um greiðsluþjónustur</span><span class="sxs-lookup"><span data-stu-id="0e9ce-103">How to: Enable Customer Payments Through Payment Services</span></span>
<span data-ttu-id="0e9ce-104">Í stað þess að innheimta með millifærslu eða kreditkorti geta viðskiptavinir þínir greitt þér af reikningnum sínum með greiðsluþjónustu, svo sem Microsoft Pay, PayPal eða WorldPay.</span><span class="sxs-lookup"><span data-stu-id="0e9ce-104">As an alternative to collecting payments through bank transfer or credit cards, your customers can pay you through their account with payment services, such as Microsoft Pay, PayPal, or WorldPay.</span></span>  

<span data-ttu-id="0e9ce-105">Eftir að þú hefur virkjað greiðsluþjónustu í [!INCLUDE[d365fin](includes/d365fin_md.md)] er tengill í þjónustuna í boði á söluskjölum sem þú sendir með tölvupósti til viðskiptavina þinna.</span><span class="sxs-lookup"><span data-stu-id="0e9ce-105">After you enable a payment service in [!INCLUDE[d365fin](includes/d365fin_md.md)], a link to the service is available on sales documents that you send by email to your customers.</span></span> <span data-ttu-id="0e9ce-106">Viðskiptamenn geta notað tengilinn til að fara í greiðsluþjónustu og greiða reikninginn beint úr söluskjalinu.</span><span class="sxs-lookup"><span data-stu-id="0e9ce-106">Customers can use the link to go to the payment service and pay the bill, directly from the sales document.</span></span> <span data-ttu-id="0e9ce-107">Ef þú vilt ekki hafa tengilinn með, til dæmis ef viðskiptamaður greiðir með peningum, getur þú fjarlægt greiðsluþjónustu af reikningnum áður en þú sendir hann.</span><span class="sxs-lookup"><span data-stu-id="0e9ce-107">If you don't want to include the link, for example, if a customer will pay with cash, you can remove the payment service from the invoice before posting.</span></span>  

<span data-ttu-id="0e9ce-108">Microsoft Pay, PayPal-greiðslustaðals- og WorldPay-greiðslustaðalsviðbætur eru settar upp í [!INCLUDE[d365fin](includes/d365fin_md.md)], og eru tilbúin fyrir þig til að virkja.</span><span class="sxs-lookup"><span data-stu-id="0e9ce-108">The Microsoft Pay, PayPal Payments Standard, and WorldPay Payments Standard extensions are installed in [!INCLUDE[d365fin](includes/d365fin_md.md)], and are ready for you to enable.</span></span>  

## <a name="to-enable-a-payment-service-in-included365finincludesd365finmdmd"></a><span data-ttu-id="0e9ce-109">Til að virkja greiðsluþjónustu í [!INCLUDE[d365fin](includes/d365fin_md.md)]</span><span class="sxs-lookup"><span data-stu-id="0e9ce-109">To enable a payment service in [!INCLUDE[d365fin](includes/d365fin_md.md)]</span></span>
1. <span data-ttu-id="0e9ce-110">Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Greiðsluþjónusta** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="0e9ce-110">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Payment Services**, and then choose the related link.</span></span>  
2. <span data-ttu-id="0e9ce-111">Í glugganum **Greiðsluþjónustur** skal velja aðgerðina **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="0e9ce-111">In the **Payment Services** window, choose the **New** action.</span></span>  
3. <span data-ttu-id="0e9ce-112">Veljið greiðsluþjónustu og lokið glugganum.</span><span class="sxs-lookup"><span data-stu-id="0e9ce-112">Select the payment service, and then close the window.</span></span>  
4. <span data-ttu-id="0e9ce-113">Í glugganum **Greiðsluþjónustur** skal velja aðgerðina **uppsetning**.</span><span class="sxs-lookup"><span data-stu-id="0e9ce-113">In the **Payment Services** window, choose the **Setup** action.</span></span>  
5. <span data-ttu-id="0e9ce-114">Fyllið inn í svæðin eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="0e9ce-114">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
6. <span data-ttu-id="0e9ce-115">Glugganum er lokað.</span><span class="sxs-lookup"><span data-stu-id="0e9ce-115">Close the window.</span></span>  

## <a name="to-select-a-payment-service-on-a-sales-invoice"></a><span data-ttu-id="0e9ce-116">Til að velja greiðsluþjónustu á sölureikning</span><span class="sxs-lookup"><span data-stu-id="0e9ce-116">To select a payment service on a sales invoice</span></span>
1. <span data-ttu-id="0e9ce-117">Í reitnum heimasíða velja **sölureikningar**.</span><span class="sxs-lookup"><span data-stu-id="0e9ce-117">On the Home page, choose **Sales Invoices**.</span></span>  
2. <span data-ttu-id="0e9ce-118">Opnaðu sölureikninginn sem þú vilt greiða með því að nota greiðsluþjónustuna.</span><span class="sxs-lookup"><span data-stu-id="0e9ce-118">Open the sales invoice that you want to pay by using the payment service.</span></span>  
3. <span data-ttu-id="0e9ce-119">Í reitnum **Greiðsluþjónusta** er greiðsluþjónustan valin.</span><span class="sxs-lookup"><span data-stu-id="0e9ce-119">In the **Payment Service** field, choose the payment service.</span></span>  

    > [!NOTE]  
>   <span data-ttu-id="0e9ce-120">**Greiðsluþjónustu** reiturinn er aðeins tiltækur greiðsluþjónustan hefur verið virkjuð.</span><span class="sxs-lookup"><span data-stu-id="0e9ce-120">The **Payment Service** field is available only if you've enabled the payment service.</span></span>  

## <a name="see-also"></a><span data-ttu-id="0e9ce-121">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="0e9ce-121">See Also</span></span>  
[<span data-ttu-id="0e9ce-122">Uppsetning sölu</span><span class="sxs-lookup"><span data-stu-id="0e9ce-122">Setting Up Sales</span></span>](sales-setup-sales.md)  
[<span data-ttu-id="0e9ce-123">Sala</span><span class="sxs-lookup"><span data-stu-id="0e9ce-123">Sales</span></span>](sales-manage-sales.md)  
<span data-ttu-id="0e9ce-124">[Sérstilling [!INCLUDE[d365fin](includes/d365fin_md.md)] með viðbótum](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="0e9ce-124">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions](ui-extensions.md)</span></span>  
<span data-ttu-id="0e9ce-125">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="0e9ce-125">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

