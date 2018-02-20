---
title: "Hvernig á að setja upp flutningsaðila | Microsoft Docs"
description: "Hægt er að setja upp kóta fyrir einstaka flutningsaðila og færa inn upplýsingar um þá."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/23/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: b6ab539048f3f802cc4575e023c43632025dccf5
ms.contentlocale: is-is
ms.lasthandoff: 01/30/2018

---
# <a name="set-up-shipping-agents"></a><span data-ttu-id="b3c32-103">Uppsetning flutningsaðila</span><span class="sxs-lookup"><span data-stu-id="b3c32-103">Set Up Shipping Agents</span></span>
<span data-ttu-id="b3c32-104">Hægt er að setja upp kóta fyrir einstaka flutningsaðila og færa inn upplýsingar um þá.</span><span class="sxs-lookup"><span data-stu-id="b3c32-104">You can set up a code for each of your shipping agents and enter information about them.</span></span>  

<span data-ttu-id="b3c32-105">Ef fært er inn veffang flutningsaðila sem býður upp á sendingaleit á Internetinu er hægt að nota sjálfvirku sendingaleitina í kerfinu.</span><span class="sxs-lookup"><span data-stu-id="b3c32-105">If you enter an Internet address for the shipping agent, and the agent provides package tracking services on the Internet, you can use the automatic package tracking feature.</span></span> <span data-ttu-id="b3c32-106">Nánari upplýsingar eru í reitnum [Finna sendingar](sales-how-track-packages.md).</span><span class="sxs-lookup"><span data-stu-id="b3c32-106">For more information, see [Track Packages](sales-how-track-packages.md).</span></span>

<span data-ttu-id="b3c32-107">Þegar flutningsaðilar eru settir upp á sölupöntunum er einnig hægt að tilgreina hvaða þjónustu einstakir flutningsaðilar bjóða.</span><span class="sxs-lookup"><span data-stu-id="b3c32-107">When you set up shipping agents on your sales orders, you can also specify the services that each shipping agent offers.</span></span>  
<span data-ttu-id="b3c32-108">Hægt er að setja upp ótakmarkaðan fjölda af þjónustuatriðum fyrir hvern flutningsaðila og hægt er að tilgreina afhendingartíma fyrir hverja þjónustu.</span><span class="sxs-lookup"><span data-stu-id="b3c32-108">For each shipping agent, you can set up an unlimited number of services, and you can specify a shipping time for each service.</span></span>  

<span data-ttu-id="b3c32-109">Þegar flutningsþjónustu hefur verið úthlutað á sölupöntunarlínu verður afhendingartími þjónustunnar tekin með við útreikning á lofun á pöntun fyrir þá línu.</span><span class="sxs-lookup"><span data-stu-id="b3c32-109">When you have assigned a shipping agent service to a sales order line, the shipping time of the service will be included in the order promising calculation, for that line.</span></span> <span data-ttu-id="b3c32-110">Nánari upplýsingar er að finna í [Reikna dagsetningar pöntunarloforða](sales-how-to-calculate-order-promising-dates.md).</span><span class="sxs-lookup"><span data-stu-id="b3c32-110">For more information, see [Calculate Order Promising Dates](sales-how-to-calculate-order-promising-dates.md).</span></span>

## <a name="to-set-up-a-shipping-agent"></a><span data-ttu-id="b3c32-111">Uppsetning flutningsaðila</span><span class="sxs-lookup"><span data-stu-id="b3c32-111">To set up a shipping agent</span></span>  
1.  <span data-ttu-id="b3c32-112">Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **flutningsaðili** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="b3c32-112">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Shipping Agents**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="b3c32-113">Fyllið inn í reitina eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="b3c32-113">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]<span data-ttu-id="b3c32-114">.</span><span class="sxs-lookup"><span data-stu-id="b3c32-114">.</span></span>  
3.  <span data-ttu-id="b3c32-115">Velja aðgerðina **Flutningsþjónusta**.</span><span class="sxs-lookup"><span data-stu-id="b3c32-115">Choose the **Shipping Agent Services** action.</span></span>
4. <span data-ttu-id="b3c32-116">Í **Flutningsþjónusta**, fyllið inn í reitina eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="b3c32-116">In the **Shipping Agent Services**, fill in the fields as necessary.</span></span>

> [!NOTE]  
>  <span data-ttu-id="b3c32-117">Ef flutningsaðila er eytt úr pantanalínunni eyðir kerfið einnig flutningsþjónustukótanum úr línunni.</span><span class="sxs-lookup"><span data-stu-id="b3c32-117">If you delete the shipping agent on the order line, the shipping agent service code is also deleted.</span></span> <span data-ttu-id="b3c32-118">Efni reita sem byggja að hluta á flutningsþjónustunni er endurreiknað.</span><span class="sxs-lookup"><span data-stu-id="b3c32-118">The contents of fields that were based in part on the shipping agent service are recalculated.</span></span>  

## <a name="see-also"></a><span data-ttu-id="b3c32-119">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="b3c32-119">See Also</span></span>
<span data-ttu-id="b3c32-120">[Finna sendingar](sales-how-track-packages.md)  </span><span class="sxs-lookup"><span data-stu-id="b3c32-120">[Track Packages](sales-how-track-packages.md)  </span></span>  
[<span data-ttu-id="b3c32-121">Vöruhúsastjórnun</span><span class="sxs-lookup"><span data-stu-id="b3c32-121">Warehouse Management</span></span>](warehouse-manage-warehouse.md)  
[<span data-ttu-id="b3c32-122">Birgðir</span><span class="sxs-lookup"><span data-stu-id="b3c32-122">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="b3c32-123">[Vöruhúsastjórnun sett upp](warehouse-setup-warehouse.md)   </span><span class="sxs-lookup"><span data-stu-id="b3c32-123">[Setting Up Warehouse Management](warehouse-setup-warehouse.md)   </span></span>  
<span data-ttu-id="b3c32-124">[Samsetningardeild](assembly-assemble-items.md)  </span><span class="sxs-lookup"><span data-stu-id="b3c32-124">[Assembly Management](assembly-assemble-items.md)  </span></span>  
[<span data-ttu-id="b3c32-125">Hönnunarupplýsingar vöruhúsakerfi</span><span class="sxs-lookup"><span data-stu-id="b3c32-125">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="b3c32-126">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="b3c32-126">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

