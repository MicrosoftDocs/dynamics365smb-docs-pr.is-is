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
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 3bcfac75d1d161a4163fda466e320b0efd408655
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/17/2020
ms.locfileid: "4758268"
---
# <a name="enable-customer-payments-through-payment-services"></a><span data-ttu-id="94260-103">Virkja greiðslur viðskiptamanna um greiðsluþjónustur</span><span class="sxs-lookup"><span data-stu-id="94260-103">Enable Customer Payments Through Payment Services</span></span>
<span data-ttu-id="94260-104">Í stað þess að innheimta með millifærslu eða kreditkorti geta viðskiptamenn þínir greitt þér af reikningnum sínum með greiðsluþjónustu, svo sem Microsoft Pay, PayPal eða WorldPay.</span><span class="sxs-lookup"><span data-stu-id="94260-104">As an alternative to collecting payments through bank transfer or credit cards, your customers can pay you through their account with payment services, such as Microsoft Pay, PayPal, or WorldPay.</span></span>  

<span data-ttu-id="94260-105">Eftir að þú hefur virkjað greiðsluþjónustu í [!INCLUDE[prod_short](includes/prod_short.md)] er tengill í þjónustuna í boði á söluskjölum sem þú sendir með tölvupósti til viðskiptavina þinna.</span><span class="sxs-lookup"><span data-stu-id="94260-105">After you enable a payment service in [!INCLUDE[prod_short](includes/prod_short.md)], a link to the service is available on sales documents that you send by email to your customers.</span></span> <span data-ttu-id="94260-106">Viðskiptamenn geta notað tengilinn til að fara í greiðsluþjónustu og greiða reikninginn beint úr söluskjalinu.</span><span class="sxs-lookup"><span data-stu-id="94260-106">Customers can use the link to go to the payment service and pay the bill, directly from the sales document.</span></span> <span data-ttu-id="94260-107">Ef þú vilt ekki hafa tengilinn með, til dæmis ef viðskiptamaður greiðir með peningum, getur þú fjarlægt greiðsluþjónustu af reikningnum áður en þú sendir hann.</span><span class="sxs-lookup"><span data-stu-id="94260-107">If you don't want to include the link, for example, if a customer will pay with cash, you can remove the payment service from the invoice before posting.</span></span>  

<span data-ttu-id="94260-108">Microsoft Pay, PayPal Payments Standard og WorldPay Payments Standard-viðbætur eru settar upp í [!INCLUDE[prod_short](includes/prod_short.md)], og eru tilbúnar fyrir þig til að virkja.</span><span class="sxs-lookup"><span data-stu-id="94260-108">The Microsoft Pay, PayPal Payments Standard, and WorldPay Payments Standard extensions are installed in [!INCLUDE[prod_short](includes/prod_short.md)], and are ready for you to enable.</span></span>  

## <a name="to-enable-a-payment-service-in-prod_short"></a><span data-ttu-id="94260-109">Til að virkja greiðsluþjónustu í [!INCLUDE[prod_short](includes/prod_short.md)]</span><span class="sxs-lookup"><span data-stu-id="94260-109">To enable a payment service in [!INCLUDE[prod_short](includes/prod_short.md)]</span></span>
1. <span data-ttu-id="94260-110">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Greiðsluþjónustur** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="94260-110">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Payment Services**, and then choose the related link.</span></span>  
2. <span data-ttu-id="94260-111">Á síðunni **Greiðsluþjónustur** skal velja aðgerðina **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="94260-111">On the **Payment Services** page, choose the **New** action.</span></span>  
3. <span data-ttu-id="94260-112">Veljið greiðsluþjónustu og lokið svo síðunni.</span><span class="sxs-lookup"><span data-stu-id="94260-112">Select the payment service, and then close the page.</span></span>  
4. <span data-ttu-id="94260-113">Á síðunni **Greiðsluþjónustur** skal velja aðgerðina **uppsetning**.</span><span class="sxs-lookup"><span data-stu-id="94260-113">On the **Payment Services** page, choose the **Setup** action.</span></span>  
5. <span data-ttu-id="94260-114">Fyllið inn reitina eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="94260-114">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
6. <span data-ttu-id="94260-115">Lokaðu síðunni.</span><span class="sxs-lookup"><span data-stu-id="94260-115">Close the page.</span></span>  

## <a name="to-select-a-payment-service-on-a-sales-invoice"></a><span data-ttu-id="94260-116">Til að velja greiðsluþjónustu á sölureikning</span><span class="sxs-lookup"><span data-stu-id="94260-116">To select a payment service on a sales invoice</span></span>
1. <span data-ttu-id="94260-117">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Sölureikningar** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="94260-117">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Invoices**, and then choose the related link.</span></span>  
2. <span data-ttu-id="94260-118">Opnaðu sölureikninginn sem þú vilt greiða með því að nota greiðsluþjónustuna.</span><span class="sxs-lookup"><span data-stu-id="94260-118">Open the sales invoice that you want to pay by using the payment service.</span></span>  
3. <span data-ttu-id="94260-119">Í reitnum **Greiðsluþjónusta** er greiðsluþjónustan valin.</span><span class="sxs-lookup"><span data-stu-id="94260-119">In the **Payment Service** field, choose the payment service.</span></span>  

    > [!NOTE]  
    > <span data-ttu-id="94260-120">**Greiðsluþjónustu** reiturinn er aðeins tiltækur greiðsluþjónustan hefur verið virkjuð.</span><span class="sxs-lookup"><span data-stu-id="94260-120">The **Payment Service** field is available only if you've enabled the payment service.</span></span>  

## <a name="see-also"></a><span data-ttu-id="94260-121">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="94260-121">See Also</span></span>  
[<span data-ttu-id="94260-122">Uppsetning sölu</span><span class="sxs-lookup"><span data-stu-id="94260-122">Setting Up Sales</span></span>](sales-setup-sales.md)  
[<span data-ttu-id="94260-123">Sala</span><span class="sxs-lookup"><span data-stu-id="94260-123">Sales</span></span>](sales-manage-sales.md)  
<span data-ttu-id="94260-124">[Sérstilling [!INCLUDE[prod_short](includes/prod_short.md)] með viðbótum](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="94260-124">[Customizing [!INCLUDE[prod_short](includes/prod_short.md)] Using Extensions](ui-extensions.md)</span></span>  
<span data-ttu-id="94260-125">[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="94260-125">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  
