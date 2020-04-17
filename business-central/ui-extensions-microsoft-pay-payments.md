---
title: Microsoft Pay greiðslustaðall | Microsoft Docs
description: Gefur upplýsingar um Microsoft Pay viðbótina
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: df7ce179f14fdaea9a65645d6ccf5d69076212db
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2020
ms.locfileid: "3194116"
---
# <a name="the-microsoft-pay-extension"></a><span data-ttu-id="315d6-103">Microsoft Pay Viðbótin</span><span class="sxs-lookup"><span data-stu-id="315d6-103">The Microsoft Pay Extension</span></span>

> [!IMPORTANT]
> <span data-ttu-id="315d6-104">Tekur gildi 8. febrúar 2020, breytingar á þjónustu Microsoft Pay hafa áhrif á Microsoft Pay-viðbótina í Microsoft [!INCLUDE[d365fin](includes/d365fin_long_md.md)].</span><span class="sxs-lookup"><span data-stu-id="315d6-104">Effective February 8 2020, changes in the Microsoft Pay service will affect the Microsoft Pay extension in Microsoft [!INCLUDE[d365fin](includes/d365fin_long_md.md)].</span></span> <span data-ttu-id="315d6-105">Vegna breytinganna munu greiðslutenglarnir **Greiða núna** sem Microsoft Pay viðbótin býr til fyrir reikninga í [!INCLUDE[d365fin](includes/d365fin_md.md)] ekki opnast í Microsoft Pay eftir 8. febrúar.</span><span class="sxs-lookup"><span data-stu-id="315d6-105">Due to the changes, after February 8, the **Pay now** payment links that the Microsoft Pay extension generates for invoices in [!INCLUDE[d365fin](includes/d365fin_md.md)] will not open Microsoft Pay.</span></span> <span data-ttu-id="315d6-106">Viðskiptavinir sem nota viðbótina ættu að breyta uppsetningu greiðsluþjónustunnar til að byrja að nota PayPal-viðbótina í staðinn.</span><span class="sxs-lookup"><span data-stu-id="315d6-106">Customers who are using the extension should change their Payment Services setup to start using the PayPal extension instead.</span></span><br /></br>
>
> <span data-ttu-id="315d6-107">Frá og með 8. janúar munum við birta tilkynningar í [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="315d6-107">From January 8, we will display a notification in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="315d6-108">Tilkynningin mun innihalda tengil á stillingarnar sem þarf að breyta og í frekari upplýsingar.</span><span class="sxs-lookup"><span data-stu-id="315d6-108">The notification will contain a link to the settings that you need to change and to more information.</span></span> <span data-ttu-id="315d6-109">Eftir 8. febrúar mun Microsoft Pay-viðbótin ekki lengur vera í boði í [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="315d6-109">After February 8, the Microsoft Pay extension will no longer be available in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span><br /></br>
>
> <span data-ttu-id="315d6-110">Breytingarnar hafa áhrif á eftirfarandi útgáfur Business Central:</span><span class="sxs-lookup"><span data-stu-id="315d6-110">The changes impact the following versions of Business Central:</span></span>
> - <span data-ttu-id="315d6-111">Microsoft Dynamics 365 Business Central október 2018</span><span class="sxs-lookup"><span data-stu-id="315d6-111">Microsoft Dynamics 365 Business Central October 2018</span></span>
> - <span data-ttu-id="315d6-112">Microsoft Dynamics 365 Business Central apríl 2019</span><span class="sxs-lookup"><span data-stu-id="315d6-112">Microsoft Dynamics 365 Business Central April 2019</span></span>
> - <span data-ttu-id="315d6-113">Microsoft Dynamics 365 Business Central 2019 útgáfutímabili 2</span><span class="sxs-lookup"><span data-stu-id="315d6-113">Microsoft Dynamics 365 Business Central 2019 Release Wave 2</span></span>

<span data-ttu-id="315d6-114">Viðskiptamenn þurfa stöðugt hærra þjónustustig, bæði hvað varðar gæði vöru en einnig hvað varðar valkosti afhendingar og greiðsluþjónustu.</span><span class="sxs-lookup"><span data-stu-id="315d6-114">Customers continuously require higher customer service, both in terms of the quality of product but also in terms of delivery and payment services.</span></span> <span data-ttu-id="315d6-115">Microsoft Pay þjónustan gerir kleift að veita viðskiptamanninum meiri þjónustu.</span><span class="sxs-lookup"><span data-stu-id="315d6-115">The Microsoft Pay service helps you increase your customer service.</span></span>

<span data-ttu-id="315d6-116">Microsoft Pay viðbótin bætir við Microsoft Pay tengli við söluskjölin þín svo viðskiptamenn geti auðveldlega borgað með því að nota Microsoft Pay.</span><span class="sxs-lookup"><span data-stu-id="315d6-116">The Microsoft Pay extension adds a Microsoft Pay link to your sales documents so customers can easily pay using Microsoft Pay.</span></span> <span data-ttu-id="315d6-117">Síðan geturðu sent skjölin með tölvupósti til að bjóða upp á betri þjónustu við viðskiptavina og stytta tímann sem það tekur greiðslu viðskiptavina að koma inn á bankareikning þinn.</span><span class="sxs-lookup"><span data-stu-id="315d6-117">Then you can send the documents by email to provide higher customer service and shorten the time it takes for customers’ payments to arrive on your bank account.</span></span>

<span data-ttu-id="315d6-118">Microsoft Pay Viðbótin veitir eftirfarandi ávinning:</span><span class="sxs-lookup"><span data-stu-id="315d6-118">The Microsoft Pay extension provides the following benefits:</span></span>
- <span data-ttu-id="315d6-119">Greiðslur viðskiptamanns berast hraðar á bankareikning þinn.</span><span class="sxs-lookup"><span data-stu-id="315d6-119">Customer payments appear faster on your bank account.</span></span>
- <span data-ttu-id="315d6-120">Viðskiptamenn hafa úr fleiri leiðum að velja til að greiða reikninga.</span><span class="sxs-lookup"><span data-stu-id="315d6-120">Customers have more ways to pay invoices.</span></span>
- <span data-ttu-id="315d6-121">Microsoft Pay býður upp á trausta greiðsluþjónustu, og viðskiptamenn kjósa hana oft fram yfir að gefa kreditkortaupplýsingar upp á óþekktum vefsíðum.</span><span class="sxs-lookup"><span data-stu-id="315d6-121">Microsoft Pay offers a trustworthy payment service, which customers prefer to entering credit card information on unknown web sites.</span></span>
- <span data-ttu-id="315d6-122">Microsoft Pay býður upp á margar leiðir á meðhöndlun greiðslna, þar á meðal vinnslu kreditkorta, PayPal reikninga og Stripe.</span><span class="sxs-lookup"><span data-stu-id="315d6-122">Microsoft Pay offers multiple ways of handling payments, including credit card processing, such as PayPal and Stripe.</span></span>
- <span data-ttu-id="315d6-123">Microsoft Pay tengilinn er hægt að innifela sjálfvirkt í hvert reikningsskjal eða innifalið af notanda.</span><span class="sxs-lookup"><span data-stu-id="315d6-123">The Microsoft Pay link can be embedded automatically on every invoice document or by the user.</span></span>
- <span data-ttu-id="315d6-124">Þar sem þessi virkni er uppbyggð sem viðbót, ertu með fulla stjórn á því að virkja hana þegar og ef þín viðskiptaferli þurfa á henni að halda.</span><span class="sxs-lookup"><span data-stu-id="315d6-124">Because this functionality is built as an extension, it gives you full control to enable it when and if your business processes require it.</span></span>

<span data-ttu-id="315d6-125">Það er ókeypis að virkja viðbætur greiðsluþjónustu í [!INCLUDE[d365fin](includes/d365fin_md.md)] en hafa þarf samband við greiðsluþjónustuna til að stofna reikning.</span><span class="sxs-lookup"><span data-stu-id="315d6-125">Enabling payment service extensions is free in [!INCLUDE[d365fin](includes/d365fin_md.md)], however, you will need to contact the payment service to get an account.</span></span> <span data-ttu-id="315d6-126">Nánari upplýsingar eru í [Virkja greiðslur viðskiptamanna um greiðsluþjónustur](sales-how-enable-payment-service-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="315d6-126">For more information, see [Enable Customer Payment Through Payment Services](sales-how-enable-payment-service-extensions.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="315d6-127">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="315d6-127">See Also</span></span>
<span data-ttu-id="315d6-128">[Sérstilling [!INCLUDE[d365fin](includes/d365fin_md.md)] með viðbótum](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="315d6-128">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions](ui-extensions.md)</span></span>  
[<span data-ttu-id="315d6-129">Uppsetning sölu</span><span class="sxs-lookup"><span data-stu-id="315d6-129">Setting Up Sales</span></span>](sales-setup-sales.md)  
<span data-ttu-id="315d6-130">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="315d6-130">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
