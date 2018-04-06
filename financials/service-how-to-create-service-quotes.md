---
title: "Hvernig á að búa til þjónustutilboð | Microsoft Docs"
description: "Hægt er að nota gluggann **Þjónustupöntun** til að stofna skjöl þar sem hægt er að færa inn upplýsingar um þjónustu, s.s. viðgerðir og viðhald, á þjónustuvörum að beiðni viðskiptamanns. Hægt er að nota þjónustutilboð sem drög að þjónustupöntun og svo má breyta tilboðinu í þjónustupöntun."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 9d4f8d21d0c79adbac238b2d26accc4c08656c77
ms.contentlocale: is-is
ms.lasthandoff: 03/22/2018

---
# <a name="create-service-quotes"></a><span data-ttu-id="fa519-104">Stofna þjónustutilboð</span><span class="sxs-lookup"><span data-stu-id="fa519-104">Create Service Quotes</span></span>
<span data-ttu-id="fa519-105">Þú getur hugsað um þjónustutilboð sem grunninn fyrir þjónustupöntunum.</span><span class="sxs-lookup"><span data-stu-id="fa519-105">You can think of service quotes as the basis for service orders.</span></span> <span data-ttu-id="fa519-106">Þetta tvennt er í raun alveg eins.</span><span class="sxs-lookup"><span data-stu-id="fa519-106">In fact, they are almost identical.</span></span> <span data-ttu-id="fa519-107">Bæði innihalda upplýsingar eins og þær hver viðskiptamaðurinn er, tegund pöntunar, varan sem þarf þjónustuna, reiknings- og afhendingarupplýsingar, og upplýsingar um hina raunverulegu þjónustuvinnu.</span><span class="sxs-lookup"><span data-stu-id="fa519-107">They both contain information such as who the customer is, the type of order, the item that needs service, billing and shipping information, and information about the actual service work.</span></span>
 
<span data-ttu-id="fa519-108">Hægt er að nota þjónustutilboð sem drög að þjónustupöntun og svo má breyta tilboðinu í þjónustupöntun.</span><span class="sxs-lookup"><span data-stu-id="fa519-108">You can use a service quote as a preliminary draft for a service order, and then convert the quote to a service order.</span></span>  
  
## <a name="to-create-a-service-quote"></a><span data-ttu-id="fa519-109">Þjónustutilboð búin til:</span><span class="sxs-lookup"><span data-stu-id="fa519-109">To create a service quote</span></span>  
1. <span data-ttu-id="fa519-110">Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Þjónustutilboð** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="fa519-110">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Service Quotes**, and then choose the related link.</span></span>  
2. <span data-ttu-id="fa519-111">Stofna nýtt þjónustutilboð.</span><span class="sxs-lookup"><span data-stu-id="fa519-111">Create a new service quote.</span></span>  
3. <span data-ttu-id="fa519-112">Í reitnum **númer**</span><span class="sxs-lookup"><span data-stu-id="fa519-112">In the **No.**</span></span> <span data-ttu-id="fa519-113">er fært inn númer fyrir þjónustutilboðið.</span><span class="sxs-lookup"><span data-stu-id="fa519-113">field, enter a number for the service quote.</span></span> <span data-ttu-id="fa519-114">Hafi númeraröð fyrir þjónustutilboð verið sett upp í glugganum **Þjónustukerfisgrunnur** er einnig hægt að styðja á færslulykilinn til að velja næsta lausa þjónustutilboðsnúmer.</span><span class="sxs-lookup"><span data-stu-id="fa519-114">Alternatively, if you have set up a number series for service quotes in the **Service Mgt. Setup** window, you can press Enter to select the next available service quote number.</span></span>  
4. <span data-ttu-id="fa519-115">Í **Númer viðskiptamanns**</span><span class="sxs-lookup"><span data-stu-id="fa519-115">In the **Customer No.**</span></span>  <span data-ttu-id="fa519-116">reitnum, veljið viðeigandi viðskiptamann af listanum.</span><span class="sxs-lookup"><span data-stu-id="fa519-116">field, select the relevant customer from the list.</span></span>  

  > [!Note]  
  >  <span data-ttu-id="fa519-117">Fyllt er sjálfkrafa í viðskiptavinareiti með upplýsingum úr spjaldinu **Viðskiptavinur**.</span><span class="sxs-lookup"><span data-stu-id="fa519-117">The customer fields are filled in automatically with information from the **Customer** card.</span></span> <span data-ttu-id="fa519-118">Ef spjaldið **Viðskiptamaður** er ekki til fyrir viðskiptamanninn og sniðmát hefur ekki verið sett upp fyrir hann er hægt að búa viðskiptamanninn til með þjónustutilboðinu.</span><span class="sxs-lookup"><span data-stu-id="fa519-118">If a **Customer** card does not exist for the customer, and you have set up a customer template, you can create the customer from the service quote.</span></span> <span data-ttu-id="fa519-119">Fyllið út viðeigandi reitina og veljið svo aðgerðina **Stofna viðskiptamann**.</span><span class="sxs-lookup"><span data-stu-id="fa519-119">Fill in the relevant fields, and then choose the **Create Customer** action.</span></span>  
  
5. <span data-ttu-id="fa519-120">Vegna stillinga á flýtiflipanum **Áskildir reitir** í glugganum **Þjónustukerfisgrunnur** þarf kannski að fylla út reitinn **Þjónustupöntunartegund** og reitinn **Kóti sölumanns**.</span><span class="sxs-lookup"><span data-stu-id="fa519-120">Depending on the settings on the **Mandatory Fields** FastTab in the **Service Mgt. Setup** window, you may need to fill in the **Service Order Type** field and the **Salesperson Code** field.</span></span>  
6. <span data-ttu-id="fa519-121">Þjónustuvörulínurnar eru fylltar út.</span><span class="sxs-lookup"><span data-stu-id="fa519-121">Fill in the service item lines.</span></span>  
7. <span data-ttu-id="fa519-122">Metinn kostnaður er skráður í þjónustulínurnar.</span><span class="sxs-lookup"><span data-stu-id="fa519-122">Register estimated costs on the service lines.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="fa519-123">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="fa519-123">See Also</span></span>  
[<span data-ttu-id="fa519-124">Stofna þjónustupantanir</span><span class="sxs-lookup"><span data-stu-id="fa519-124">Create Service Orders</span></span>](service-how-to-create-service-orders.md)  
[<span data-ttu-id="fa519-125">Vinna við þjónustuverk</span><span class="sxs-lookup"><span data-stu-id="fa519-125">Work on Service tasks</span></span>](service-how-to-work-on-service-tasks.md)  

 
