---
title: Hvernig á að stofna framleiðslupantanahausa | Microsoft Docs
description: Hægt er að búa til framl.pöntun handvirkt og fyrsta skrefið er að búa til framleiðslupöntunarhaus.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 683631572b7898ede3b7f1418f68a7ce95743ff8
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5380899"
---
# <a name="create-production-order-headers"></a><span data-ttu-id="feb99-103">Gerð framleiðslupantanahausa</span><span class="sxs-lookup"><span data-stu-id="feb99-103">Create Production Order Headers</span></span>
<span data-ttu-id="feb99-104">Hægt er að búa til framl.pöntun handvirkt og fyrsta skrefið er að búa til framleiðslupöntunarhaus.</span><span class="sxs-lookup"><span data-stu-id="feb99-104">You can create a production order manually, and the first step is to create a production order header.</span></span>

<span data-ttu-id="feb99-105">Framleiðslupantanir eru vanalega stofnaðar sjálfvirkt af áætlanaaðgerð til að uppfylla þekkta eftirspurn.</span><span class="sxs-lookup"><span data-stu-id="feb99-105">Production orders are typically created automatically by a planning function to fulfill a known demand.</span></span> <span data-ttu-id="feb99-106">Nánari upplýsingar er að finna í [áætlanagerð](production-planning.md).</span><span class="sxs-lookup"><span data-stu-id="feb99-106">For more information, see [Planning](production-planning.md).</span></span>   

<span data-ttu-id="feb99-107">Eftirfarandi aðferð sýnir hvernig fastáætluð framl.pöntun er búin til.</span><span class="sxs-lookup"><span data-stu-id="feb99-107">In the following procedure, a firm planned production order is created.</span></span> <span data-ttu-id="feb99-108">Einnig er hægt að búa til framl.pantanir með mismunandi stöðu.</span><span class="sxs-lookup"><span data-stu-id="feb99-108">You can also create production orders with a different status.</span></span>  

## <a name="to-create-a-production-order-header"></a><span data-ttu-id="feb99-109">Gerð framleiðslupantanahausa:</span><span class="sxs-lookup"><span data-stu-id="feb99-109">To create a production order header</span></span>  
1.  <span data-ttu-id="feb99-110">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Fastáætluð framl.pantanir** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="feb99-110">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Firm Planned Prod. Orders**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="feb99-111">Valið er **Nýtt** aðgerð.</span><span class="sxs-lookup"><span data-stu-id="feb99-111">Choose the **New** action.</span></span>  
3.  <span data-ttu-id="feb99-112">Í reitnum **númer**</span><span class="sxs-lookup"><span data-stu-id="feb99-112">In the **No.**</span></span> <span data-ttu-id="feb99-113">er sett næsta númer í röðinni.</span><span class="sxs-lookup"><span data-stu-id="feb99-113">field, insert the next number in the series.</span></span>  
4.  <span data-ttu-id="feb99-114">Uppruni framleiðslupöntunarinnar er valinn í reitnum **Tegund uppruna** .</span><span class="sxs-lookup"><span data-stu-id="feb99-114">In the **Source Type** field, select the source of the production order.</span></span>

    <span data-ttu-id="feb99-115">Hér geturðu valið að framleiða fyrir samsafn af vörum.</span><span class="sxs-lookup"><span data-stu-id="feb99-115">Here you can select to produce for a family of items.</span></span> <span data-ttu-id="feb99-116">Nánari upplýsingar eru í [Vinna með framleiðslusamsafn](production-how-work-family.md).</span><span class="sxs-lookup"><span data-stu-id="feb99-116">For more information, see [Work With Production Families](production-how-work-family.md).</span></span>
5.  <span data-ttu-id="feb99-117">Í reitinn **Nr.** er valið vörunúmer, fjölskylda eða söluhaus sem búa á til þjónustupöntunina fyrir.</span><span class="sxs-lookup"><span data-stu-id="feb99-117">In the **Source No.** field, select the item number, family, or sales header for which the production order is to be generated.</span></span>  
6.  <span data-ttu-id="feb99-118">Reitirnir **Magn** og **Gjalddagi** eru fylltir út í samræmi við óskir notandans.</span><span class="sxs-lookup"><span data-stu-id="feb99-118">Fill in the **Quantity** and **Due Date** fields according to your specifications.</span></span>  

<span data-ttu-id="feb99-119">Þegar framleiðsluskilyrði breytast, eins og t.d. íhlutir eða aðgerðir, geturðu snögglega enduráætlað framleiðslupöntunina.</span><span class="sxs-lookup"><span data-stu-id="feb99-119">When production requirements change, such as components or operations, you can quickly replan the production order.</span></span> <span data-ttu-id="feb99-120">Frekari upplýsingar, sjá [Enduráætla eða uppfæra framleiðslupantanir beint](production-how-to-replan-refresh-production-orders.md).</span><span class="sxs-lookup"><span data-stu-id="feb99-120">For more information, see [Replan or Refresh Production Orders Directly](production-how-to-replan-refresh-production-orders.md).</span></span> 

## <a name="see-also"></a><span data-ttu-id="feb99-121">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="feb99-121">See Also</span></span>  
<span data-ttu-id="feb99-122">[Framleiðsla](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="feb99-122">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
[<span data-ttu-id="feb99-123">Uppsetning framleiðslu</span><span class="sxs-lookup"><span data-stu-id="feb99-123">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="feb99-124">[Áætlun](production-planning.md)    </span><span class="sxs-lookup"><span data-stu-id="feb99-124">[Planning](production-planning.md)    </span></span>  
[<span data-ttu-id="feb99-125">Birgðir</span><span class="sxs-lookup"><span data-stu-id="feb99-125">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="feb99-126">Innkaup</span><span class="sxs-lookup"><span data-stu-id="feb99-126">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="feb99-127">[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="feb99-127">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]