---
title: Margir samningar | Microsoft Docs
description: Það ræðst af þjónustustigssamkomulagi við viðskiptavin hvort afgreiða verður þjónustuvöru í fleiri en einum þjónustusamningi.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: c6410f1b96aa1c1f8251738184db07aba0d94c4b
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/01/2020
ms.locfileid: "3915286"
---
# <a name="multiple-contracts"></a><span data-ttu-id="eab19-103">Margir samningar</span><span class="sxs-lookup"><span data-stu-id="eab19-103">Multiple Contracts</span></span>
<span data-ttu-id="eab19-104">Það ræðst af þjónustustigssamkomulagi við viðskiptavin hvort afgreiða verður þjónustuvöru í fleiri en einum þjónustusamningi.</span><span class="sxs-lookup"><span data-stu-id="eab19-104">Depending on your service level agreements with a customer, you may have to handle a service item under more than one service contract.</span></span>  
  
<span data-ttu-id="eab19-105">Með því að afgreiða þjónustuvöru undir skv. samningum er hægt að gera eftirfarandi:</span><span class="sxs-lookup"><span data-stu-id="eab19-105">By handling a service item under multiple contracts, you can do the following:</span></span>  
  
* <span data-ttu-id="eab19-106">Gefa út mismunandi samninga fyrir sömu þjónustuvöru.</span><span class="sxs-lookup"><span data-stu-id="eab19-106">Issue different contracts for the same service item.</span></span>  
* <span data-ttu-id="eab19-107">Þjónusta varahluti sérstaklega.</span><span class="sxs-lookup"><span data-stu-id="eab19-107">Service parts separately.</span></span>  
* <span data-ttu-id="eab19-108">Taka mið af ólíkri þekkingu sem er nauðsynleg til að þjónusta mismunandi þætti þjónustuvöru, til dæmis vélbúnað og hugbúnað.</span><span class="sxs-lookup"><span data-stu-id="eab19-108">Consider different skills that are required to service different aspects of a service item, such as mechanical components and software.</span></span>  
* <span data-ttu-id="eab19-109">Tilgreinið mismunandi svartíma og tíðni við þjónustu ólíkra hluta þjónustuvöru.</span><span class="sxs-lookup"><span data-stu-id="eab19-109">Specify different response times and frequencies in servicing different parts of a service item.</span></span>  
* <span data-ttu-id="eab19-110">Segja fyrir um ólíka verkþætti sem þarf að vinna í tengslum við þjónustuvöru þegar þjónustuvaran þarfnast mismunandi þjónustu á mismunandi tímabilum.</span><span class="sxs-lookup"><span data-stu-id="eab19-110">Address different kinds of activities to be performed on a service item when the service item requires different types of service in different time periods.</span></span>  
* <span data-ttu-id="eab19-111">Velja og úthluta réttu samningsnúmeri til þjónustuvörulínu þegar þjónustupöntun er stofnuð.</span><span class="sxs-lookup"><span data-stu-id="eab19-111">Select and assign an appropriate contract number to a service item line when you are creating a service order.</span></span>  
* <span data-ttu-id="eab19-112">Afgreiða viðeigandi fjárhagslegar upplýsingar um þjónustuvörur og samkomulag um þjónustustig.</span><span class="sxs-lookup"><span data-stu-id="eab19-112">Handle relevant financial information about service items and service level agreements.</span></span>  
  
<span data-ttu-id="eab19-113">Hægt er að skoða eftirfarandi dæmi um notkun margra samninga.</span><span class="sxs-lookup"><span data-stu-id="eab19-113">You can consider the following examples of using the multiple contracts functionality.</span></span>  
  
## <a name="creating-multiple-contracts-per-service-item"></a><span data-ttu-id="eab19-114">Margir samningar fyrir hverja þjónustuvöru stofnaðir</span><span class="sxs-lookup"><span data-stu-id="eab19-114">Creating Multiple Contracts per Service Item</span></span>  
<span data-ttu-id="eab19-115">Hægt er að stofna þjónustusamning eða samningstilboð handvirkt fyrir þjónustuvörur sem þegar eru skráðar í samninga sem ekki hefur verið hætt við og eru í eigu sama viðskiptamanns.</span><span class="sxs-lookup"><span data-stu-id="eab19-115">You can manually create a service contract or contract quote for service items already registered in non-canceled contracts owned by the same customer.</span></span> <span data-ttu-id="eab19-116">Þetta er gert með því að fara eins og venjulega í gegnum  ferli til að stofna þjónustusamninga og þjónustusamningstilboð.</span><span class="sxs-lookup"><span data-stu-id="eab19-116">To do this, follow the standard procedure of creating service contracts and service contract quotes.</span></span> <span data-ttu-id="eab19-117">Frekari upplýsingar, sjá [Vinna með þjónustusamninga og þjónustusamningstilboð](service-how-to-create-service-contracts-and-service-contract-quotes.md).</span><span class="sxs-lookup"><span data-stu-id="eab19-117">For more information, see [Work with Service Contracts and Service Contract Quotes](service-how-to-create-service-contracts-and-service-contract-quotes.md).</span></span>  
  
<span data-ttu-id="eab19-118">Þegar valið er að bæta þjónustuvöru í samningslínu sem er skráð í öðrum þjónustusamningum eða samningstilboðum birtir kerfið viðvörun þar sem segir að þjónustuvaran tilheyri þegar einum eða fleirum þjónustusamningum eða samningstilboðum.</span><span class="sxs-lookup"><span data-stu-id="eab19-118">When you add a service item on a contract line that is registered in other service contracts or contract quotes, a warning message is displayed stating that the service item already belongs to one or more service contracts or contract quotes.</span></span> <span data-ttu-id="eab19-119">Ef þessi viðvörun er staðfest eru allar viðeigandi upplýsingar um þjónustuvöru afritaðar í nýstofnaða samningslínu.</span><span class="sxs-lookup"><span data-stu-id="eab19-119">If you confirm this message, all relevant service item information is copied to a newly created contract line.</span></span>  
  
## <a name="copying-documents"></a><span data-ttu-id="eab19-120">Afritun skjala</span><span class="sxs-lookup"><span data-stu-id="eab19-120">Copying Documents</span></span>  
<span data-ttu-id="eab19-121">Hægt er að stofna þjónustusamning eða samningstilboð sjálfkrafa fyrir þjónustuvörur sem þegar eru skráðar í öðrum þjónustusamningum eða samningstilboðum með aðgerðinni **Afrita úr skjali**.</span><span class="sxs-lookup"><span data-stu-id="eab19-121">You can automatically create a service contract or contract quote for service items that are already registered in other service contracts or contract quotes by using the **Copy from Document** action.</span></span>  
  
## <a name="creating-service-orders-for-multiple-contracts"></a><span data-ttu-id="eab19-122">Þjónustupantanir stofnaðar út frá mörgum samningum</span><span class="sxs-lookup"><span data-stu-id="eab19-122">Creating Service Orders for Multiple Contracts</span></span>  
<span data-ttu-id="eab19-123">Hægt er að stofna þjónustupöntun handvirkt fyrir þjónustuvöru sem skráð er í marga virka samninga.</span><span class="sxs-lookup"><span data-stu-id="eab19-123">You can manually create a service order for a service item that is registered in multiple active contracts.</span></span> <span data-ttu-id="eab19-124">Þjónustusamningur er virkur þegar hann er undirritaður og ekki útrunninn.</span><span class="sxs-lookup"><span data-stu-id="eab19-124">A service contract is active when it is signed and not expired.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="eab19-125">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="eab19-125">See Also</span></span>  
[<span data-ttu-id="eab19-126">Uppfylla þjónustusamninga</span><span class="sxs-lookup"><span data-stu-id="eab19-126">Fulfilling Service Contracts</span></span>](service-fulfill-service-contracts.md)  
[<span data-ttu-id="eab19-127">Stofna þjónustupantanir</span><span class="sxs-lookup"><span data-stu-id="eab19-127">Create Service Orders</span></span>](service-how-to-create-service-orders.md)  
