---
title: Virkja greiðslur viðskiptamanna gegnum greiðsluþjónustu| Microsoft Docs
description: Gerðu það auðveldara fyrir viðskiptavini að greiða reikninga sína með því að virkja greiðsluþjónustu.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: online payment
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: eac58a651989fff8b1d2cc6b6dbed2a380ae8ef8
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/08/2019
ms.locfileid: "799416"
---
# <a name="enable-customer-payments-through-payment-services"></a><span data-ttu-id="2383b-103">Virkja greiðslur viðskiptamanna um greiðsluþjónustur</span><span class="sxs-lookup"><span data-stu-id="2383b-103">Enable Customer Payments Through Payment Services</span></span>
<span data-ttu-id="2383b-104">Í stað þess að innheimta með millifærslu eða kreditkorti geta viðskiptavinir þínir greitt þér af reikningnum sínum með greiðsluþjónustu, svo sem Microsoft Pay, PayPal eða WorldPay.</span><span class="sxs-lookup"><span data-stu-id="2383b-104">As an alternative to collecting payments through bank transfer or credit cards, your customers can pay you through their account with payment services, such as Microsoft Pay, PayPal, or WorldPay.</span></span>  

<span data-ttu-id="2383b-105">Eftir að þú hefur virkjað greiðsluþjónustu í [!INCLUDE[d365fin](includes/d365fin_md.md)] er tengill í þjónustuna í boði á söluskjölum sem þú sendir með tölvupósti til viðskiptavina þinna.</span><span class="sxs-lookup"><span data-stu-id="2383b-105">After you enable a payment service in [!INCLUDE[d365fin](includes/d365fin_md.md)], a link to the service is available on sales documents that you send by email to your customers.</span></span> <span data-ttu-id="2383b-106">Viðskiptamenn geta notað tengilinn til að fara í greiðsluþjónustu og greiða reikninginn beint úr söluskjalinu.</span><span class="sxs-lookup"><span data-stu-id="2383b-106">Customers can use the link to go to the payment service and pay the bill, directly from the sales document.</span></span> <span data-ttu-id="2383b-107">Ef þú vilt ekki hafa tengilinn með, til dæmis ef viðskiptamaður greiðir með peningum, getur þú fjarlægt greiðsluþjónustu af reikningnum áður en þú sendir hann.</span><span class="sxs-lookup"><span data-stu-id="2383b-107">If you don't want to include the link, for example, if a customer will pay with cash, you can remove the payment service from the invoice before posting.</span></span>  

<span data-ttu-id="2383b-108">Microsoft Pay, PayPal Payments Standard og WorldPay Payments Standard viðbætur eru settar upp í [!INCLUDE[d365fin](includes/d365fin_md.md)], og eru tilbúnar fyrir þig til að virkja.</span><span class="sxs-lookup"><span data-stu-id="2383b-108">The Microsoft Pay, PayPal Payments Standard, and WorldPay Payments Standard extensions are installed in [!INCLUDE[d365fin](includes/d365fin_md.md)], and are ready for you to enable.</span></span>  

## <a name="to-enable-a-payment-service-in-included365finincludesd365finmdmd"></a><span data-ttu-id="2383b-109">Til að virkja greiðsluþjónustu í [!INCLUDE[d365fin](includes/d365fin_md.md)]</span><span class="sxs-lookup"><span data-stu-id="2383b-109">To enable a payment service in [!INCLUDE[d365fin](includes/d365fin_md.md)]</span></span>
1. <span data-ttu-id="2383b-110">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **greiðsluþjónusta** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="2383b-110">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Payment Services**, and then choose the related link.</span></span>  
2. <span data-ttu-id="2383b-111">Á síðunni **Greiðsluþjónustur** skal velja aðgerðina **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="2383b-111">On the **Payment Services** page, choose the **New** action.</span></span>  
3. <span data-ttu-id="2383b-112">Veljið greiðsluþjónustu og lokið svo síðunni.</span><span class="sxs-lookup"><span data-stu-id="2383b-112">Select the payment service, and then close the page.</span></span>  
4. <span data-ttu-id="2383b-113">Á síðunni **Greiðsluþjónustur** skal velja aðgerðina **uppsetning**.</span><span class="sxs-lookup"><span data-stu-id="2383b-113">On the **Payment Services** page, choose the **Setup** action.</span></span>  
5. <span data-ttu-id="2383b-114">Fyllið inn reitina eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="2383b-114">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
6. <span data-ttu-id="2383b-115">Lokaðu síðunni.</span><span class="sxs-lookup"><span data-stu-id="2383b-115">Close the page.</span></span>  

## <a name="to-select-a-payment-service-on-a-sales-invoice"></a><span data-ttu-id="2383b-116">Til að velja greiðsluþjónustu á sölureikning</span><span class="sxs-lookup"><span data-stu-id="2383b-116">To select a payment service on a sales invoice</span></span>
1. <span data-ttu-id="2383b-117">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Sölureikningar** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="2383b-117">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Invoices**, and then choose the related link.</span></span>  
2. <span data-ttu-id="2383b-118">Opnaðu sölureikninginn sem þú vilt greiða með því að nota greiðsluþjónustuna.</span><span class="sxs-lookup"><span data-stu-id="2383b-118">Open the sales invoice that you want to pay by using the payment service.</span></span>  
3. <span data-ttu-id="2383b-119">Í reitnum **Greiðsluþjónusta** er greiðsluþjónustan valin.</span><span class="sxs-lookup"><span data-stu-id="2383b-119">In the **Payment Service** field, choose the payment service.</span></span>  

    > [!NOTE]  
    > <span data-ttu-id="2383b-120">**Greiðsluþjónustu** reiturinn er aðeins tiltækur greiðsluþjónustan hefur verið virkjuð.</span><span class="sxs-lookup"><span data-stu-id="2383b-120">The **Payment Service** field is available only if you've enabled the payment service.</span></span>  

## <a name="see-also"></a><span data-ttu-id="2383b-121">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="2383b-121">See Also</span></span>  
[<span data-ttu-id="2383b-122">Uppsetning sölu</span><span class="sxs-lookup"><span data-stu-id="2383b-122">Setting Up Sales</span></span>](sales-setup-sales.md)  
[<span data-ttu-id="2383b-123">Sala</span><span class="sxs-lookup"><span data-stu-id="2383b-123">Sales</span></span>](sales-manage-sales.md)  
<span data-ttu-id="2383b-124">[Sérstilling [!INCLUDE[d365fin](includes/d365fin_md.md)] með viðbótum](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="2383b-124">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions](ui-extensions.md)</span></span>  
<span data-ttu-id="2383b-125">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="2383b-125">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
