---
title: Búa til framleiðslupantanir úr sölupöntunum
description: Hægt er að búa til framleiðslupantanir úr sölupöntunum.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 05/28/2021
ms.author: edupont
ms.openlocfilehash: 438f4d4e1833ba607ceedb9f5d9450c0a4dbb680
ms.sourcegitcommit: f9a190933eadf4608f591e2f1b04c69f1e5c0dc7
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/28/2021
ms.locfileid: "6115237"
---
# <a name="create-production-orders-from-sales-orders"></a><span data-ttu-id="006b8-103">Búa til framleiðslupantanir úr sölupöntunum</span><span class="sxs-lookup"><span data-stu-id="006b8-103">Create Production Orders from Sales Orders</span></span>
<span data-ttu-id="006b8-104">Hægt er að búa til framleiðslupantanir fyrir framleiðsluvörur beint frá sölupöntunum.</span><span class="sxs-lookup"><span data-stu-id="006b8-104">You can create production orders for produced items directly from sales orders.</span></span>  

## <a name="to-create-a-production-order-from-a-sales-order"></a><span data-ttu-id="006b8-105">Framleiðslupantanir búnar til í sölupöntunum:</span><span class="sxs-lookup"><span data-stu-id="006b8-105">To create a production order from a sales order</span></span>  

1.  <span data-ttu-id="006b8-106">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Sölupantanir** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="006b8-106">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Orders**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="006b8-107">Veldu sölupöntun sem þú vilt búa til framleiðslupöntun fyrir.</span><span class="sxs-lookup"><span data-stu-id="006b8-107">Select the sales order you want to create a production order for.</span></span>  
3.  <span data-ttu-id="006b8-108">Veldu aðgerðina **Áætlun**.</span><span class="sxs-lookup"><span data-stu-id="006b8-108">Choose the **Planning** action.</span></span> <span data-ttu-id="006b8-109">Á síðunni **Áætlun sölupöntunar** er hægt að skoða magn vörunnar í sölupöntuninni sem er til ráðstöfunar.</span><span class="sxs-lookup"><span data-stu-id="006b8-109">On the **Sales Order Planning** page, you can view the availability of the sales order item.</span></span>  
4.  <span data-ttu-id="006b8-110">Veldu aðgerðina **Stofna framl.pöntun**.</span><span class="sxs-lookup"><span data-stu-id="006b8-110">Choose the **Create Prod. Order** action.</span></span>  
5.  <span data-ttu-id="006b8-111">Velja skal stöðu og pöntunartegund.</span><span class="sxs-lookup"><span data-stu-id="006b8-111">Select the status and order type.</span></span>  
6.  <span data-ttu-id="006b8-112">Veldu hnappinn **Já** til að búa til eina eða fleiri framleiðslupantanir fyrir línurnar sem eru með **Framl.pöntun** í reitnum **Áfyllingarkerfi**.</span><span class="sxs-lookup"><span data-stu-id="006b8-112">Choose the **Yes** button to create one or more production orders for the lines that have **Prod. Order** in their **Replenishment System** field.</span></span>


> [!NOTE]  
> <span data-ttu-id="006b8-113">Eftirspurnarlínur í tilbúinn framleiðslupöntun sem hafa **Framl.pöntun** í reitnum **Áfyllingarkerfi** tákna undirliggjandi framleiðslupantanir.</span><span class="sxs-lookup"><span data-stu-id="006b8-113">Demand lines in the created production order that have **Prod. Order** in their **Replenishment System** field represent underlying production orders.</span></span> <span data-ttu-id="006b8-114">Eftir að hafa myndað þessar framleiðslupantanir þarf að reikna aftur út áætlun á síðunni **Pantanaáætlun** eða **Enduráætla** til að auðkenna alla óuppfyllta eftirspurn eftir íhlutum fyrir þær.</span><span class="sxs-lookup"><span data-stu-id="006b8-114">After you have generated these production orders, remember to identify any unfulfilled component demand for them using the **Order Planning** page or the **Replan** function from created orders.</span></span> 

## <a name="order-type"></a><span data-ttu-id="006b8-115">Gerð pöntunar</span><span class="sxs-lookup"><span data-stu-id="006b8-115">Order type</span></span>  
<span data-ttu-id="006b8-116">Hægt er að velja um tvær leiðir til að búa til framleiðslupantanir eins og lýst er í eftirfarandi töflu.</span><span class="sxs-lookup"><span data-stu-id="006b8-116">You can choose between two ways to create the production orders as outlined in the following table.</span></span>

|<span data-ttu-id="006b8-117">Valkostur</span><span class="sxs-lookup"><span data-stu-id="006b8-117">Option</span></span>|<span data-ttu-id="006b8-118">Description</span><span class="sxs-lookup"><span data-stu-id="006b8-118">Description</span></span>|
|------|-----------|
|<span data-ttu-id="006b8-119">Vörupöntun</span><span class="sxs-lookup"><span data-stu-id="006b8-119">Item Order</span></span>|<span data-ttu-id="006b8-120">Ein framleiðslupöntun er stofnuð fyrir hverja framleiðslupöntun sem þarf og sem er táknuð með línu í glugganum **Áætlun sölupöntunar**.</span><span class="sxs-lookup"><span data-stu-id="006b8-120">One production order is created for each needed production order that is represented by a line in the **Sales Order Planning** window.</span></span>|
|<span data-ttu-id="006b8-121">Verkefnispöntun</span><span class="sxs-lookup"><span data-stu-id="006b8-121">Project Order</span></span>|<span data-ttu-id="006b8-122">Ein framleiðslupöntun er stofnuð fyrir allar framleiðslupantanir sem þarf og sem eru táknaðar með línum í glugganum **Áætlun sölupöntunar**.</span><span class="sxs-lookup"><span data-stu-id="006b8-122">One production order is created for all needed production orders order that are represented by lines in the **Sales Order Planning** window.</span></span> |

<span data-ttu-id="006b8-123">Þegar verkpantanir eru notaðar inniheldur **Tegund uppruna** í framleiðslupöntuninni **Söluhaus** og hún hefur margar línur, eina fyrir hverja vöru sölulínu sem þarf að framleiða.</span><span class="sxs-lookup"><span data-stu-id="006b8-123">When you use project orders, the **Source Type** field of the production order contains **Sales Header** and the order has multiple lines, one for each sales line item that must be produced.</span></span>  


## <a name="see-also"></a><span data-ttu-id="006b8-124">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="006b8-124">See Also</span></span>  
[<span data-ttu-id="006b8-125">Uppsetning framleiðslu</span><span class="sxs-lookup"><span data-stu-id="006b8-125">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="006b8-126">[Framleiðsla](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="006b8-126">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
[<span data-ttu-id="006b8-127">Birgðir</span><span class="sxs-lookup"><span data-stu-id="006b8-127">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="006b8-128">Innkaup</span><span class="sxs-lookup"><span data-stu-id="006b8-128">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="006b8-129">[Hönnunarupplýsingar: framboðsáætlun](design-details-supply-planning.md) </span><span class="sxs-lookup"><span data-stu-id="006b8-129">[Design Details: Supply Planning](design-details-supply-planning.md) </span></span>  
[<span data-ttu-id="006b8-130">Uppsetning bestu venja: Framboðsáætlun</span><span class="sxs-lookup"><span data-stu-id="006b8-130">Setup Best Practices: Supply Planning</span></span>](setup-best-practices-supply-planning.md)  
<span data-ttu-id="006b8-131">[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="006b8-131">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]
