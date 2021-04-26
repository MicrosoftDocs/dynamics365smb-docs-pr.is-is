---
title: Hvernig á að setja upp flutningsaðila | Microsoft Docs
description: Hægt er að setja upp kóta fyrir einstaka flutningsaðila og færa inn upplýsingar um þá.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 221578a174c6bd0dd87377340e97cd54a98d177b
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5778398"
---
# <a name="set-up-shipping-agents"></a><span data-ttu-id="ed3dc-103">Uppsetning flutningsaðila</span><span class="sxs-lookup"><span data-stu-id="ed3dc-103">Set Up Shipping Agents</span></span>
<span data-ttu-id="ed3dc-104">Hægt er að setja upp kóta fyrir einstaka flutningsaðila og færa inn upplýsingar um þá.</span><span class="sxs-lookup"><span data-stu-id="ed3dc-104">You can set up a code for each of your shipping agents and enter information about them.</span></span>  

<span data-ttu-id="ed3dc-105">Ef fært er inn veffang flutningsaðila sem býður upp á sendingaleit á Internetinu er hægt að nota sjálfvirku sendingaleitina í kerfinu.</span><span class="sxs-lookup"><span data-stu-id="ed3dc-105">If you enter an Internet address for the shipping agent, and the agent provides package tracking services on the Internet, you can use the automatic package tracking feature.</span></span> <span data-ttu-id="ed3dc-106">Nánari upplýsingar eru í reitnum [Finna sendingar](sales-how-track-packages.md).</span><span class="sxs-lookup"><span data-stu-id="ed3dc-106">For more information, see [Track Packages](sales-how-track-packages.md).</span></span>

<span data-ttu-id="ed3dc-107">Þegar flutningsaðilar eru settir upp á sölupöntunum er einnig hægt að tilgreina hvaða þjónustu einstakir flutningsaðilar bjóða.</span><span class="sxs-lookup"><span data-stu-id="ed3dc-107">When you set up shipping agents on your sales orders, you can also specify the services that each shipping agent offers.</span></span>  
<span data-ttu-id="ed3dc-108">Hægt er að setja upp ótakmarkaðan fjölda af þjónustuatriðum fyrir hvern flutningsaðila og hægt er að tilgreina afhendingartíma fyrir hverja þjónustu.</span><span class="sxs-lookup"><span data-stu-id="ed3dc-108">For each shipping agent, you can set up an unlimited number of services, and you can specify a shipping time for each service.</span></span>  

<span data-ttu-id="ed3dc-109">Þegar flutningsþjónustu hefur verið úthlutað á sölupöntunarlínu verður afhendingartími þjónustunnar tekin með við útreikning á lofun á pöntun fyrir þá línu.</span><span class="sxs-lookup"><span data-stu-id="ed3dc-109">When you have assigned a shipping agent service to a sales order line, the shipping time of the service will be included in the order promising calculation, for that line.</span></span> <span data-ttu-id="ed3dc-110">Nánari upplýsingar er að finna í [Reikna dagsetningar pöntunarloforða](sales-how-to-calculate-order-promising-dates.md).</span><span class="sxs-lookup"><span data-stu-id="ed3dc-110">For more information, see [Calculate Order Promising Dates](sales-how-to-calculate-order-promising-dates.md).</span></span>

## <a name="to-set-up-a-shipping-agent"></a><span data-ttu-id="ed3dc-111">Uppsetning flutningsaðila</span><span class="sxs-lookup"><span data-stu-id="ed3dc-111">To set up a shipping agent</span></span>  
1.  <span data-ttu-id="ed3dc-112">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Flutningsaðilar** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="ed3dc-112">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Shipping Agents**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="ed3dc-113">Fyllið inn í reitina eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="ed3dc-113">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]<span data-ttu-id="ed3dc-114">.</span><span class="sxs-lookup"><span data-stu-id="ed3dc-114">.</span></span>  
3.  <span data-ttu-id="ed3dc-115">Velja aðgerðina **Flutningsþjónusta**.</span><span class="sxs-lookup"><span data-stu-id="ed3dc-115">Choose the **Shipping Agent Services** action.</span></span>
4. <span data-ttu-id="ed3dc-116">Í **Flutningsþjónusta**, fyllið inn í reitina eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="ed3dc-116">In the **Shipping Agent Services**, fill in the fields as necessary.</span></span>

> [!NOTE]  
>  <span data-ttu-id="ed3dc-117">Ef flutningsaðila er eytt úr pantanalínunni eyðir kerfið einnig flutningsþjónustukótanum úr línunni.</span><span class="sxs-lookup"><span data-stu-id="ed3dc-117">If you delete the shipping agent on the order line, the shipping agent service code is also deleted.</span></span> <span data-ttu-id="ed3dc-118">Efni reita sem byggja að hluta á flutningsþjónustunni er endurreiknað.</span><span class="sxs-lookup"><span data-stu-id="ed3dc-118">The contents of fields that were based in part on the shipping agent service are recalculated.</span></span>  

## <a name="see-also"></a><span data-ttu-id="ed3dc-119">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="ed3dc-119">See Also</span></span>
[<span data-ttu-id="ed3dc-120">Afhendingarmátar settir upp</span><span class="sxs-lookup"><span data-stu-id="ed3dc-120">Set Up Shipment Methods</span></span>](sales-how-set-up-shipment-methods.md)  
<span data-ttu-id="ed3dc-121">[Finna sendingar](sales-how-track-packages.md)  </span><span class="sxs-lookup"><span data-stu-id="ed3dc-121">[Track Packages](sales-how-track-packages.md)  </span></span>  
[<span data-ttu-id="ed3dc-122">Vöruhúsastjórnun</span><span class="sxs-lookup"><span data-stu-id="ed3dc-122">Warehouse Management</span></span>](warehouse-manage-warehouse.md)  
[<span data-ttu-id="ed3dc-123">Birgðir</span><span class="sxs-lookup"><span data-stu-id="ed3dc-123">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="ed3dc-124">[Vöruhúsastjórnun sett upp](warehouse-setup-warehouse.md)   </span><span class="sxs-lookup"><span data-stu-id="ed3dc-124">[Setting Up Warehouse Management](warehouse-setup-warehouse.md)   </span></span>  
<span data-ttu-id="ed3dc-125">[Samsetningardeild](assembly-assemble-items.md)  </span><span class="sxs-lookup"><span data-stu-id="ed3dc-125">[Assembly Management](assembly-assemble-items.md)  </span></span>  
[<span data-ttu-id="ed3dc-126">Hönnunarupplýsingar vöruhúsakerfi</span><span class="sxs-lookup"><span data-stu-id="ed3dc-126">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="ed3dc-127">[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="ed3dc-127">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  


[!INCLUDE[footer-include](includes/footer-banner.md)]