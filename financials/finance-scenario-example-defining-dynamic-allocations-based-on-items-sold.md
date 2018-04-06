---
title: "Dæmi – Skilgreining kvikrar úthlutunar á grundvelli seldra vara | Microsoft Docs"
description: "Þetta efnisatriði sýnir dæmi um hvernig á að skilgreina úthlutanir með því að nota kvika úthlutunaraðferð."
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
ms.openlocfilehash: d8622d11cd23e506d1b85b18dbe5facb740c7753
ms.contentlocale: is-is
ms.lasthandoff: 03/22/2018

---
# <a name="scenario-example-defining-dynamic-allocations-based-on-items-sold"></a><span data-ttu-id="5fe54-103">Dæmi: Skilgreining kvikrar úthlutunar á grundvelli seldra vara</span><span class="sxs-lookup"><span data-stu-id="5fe54-103">Scenario Example: Defining Dynamic Allocations Based on Items Sold</span></span>
<span data-ttu-id="5fe54-104">Þetta efnisatriði sýnir dæmi um hvernig á að skilgreina úthlutanir með því að nota kvika úthlutunaraðferð.</span><span class="sxs-lookup"><span data-stu-id="5fe54-104">This topic shows an example of how to define allocations by using the dynamic allocation method.</span></span> <span data-ttu-id="5fe54-105">Í dæminu er kvika úthlutun af kostnaði fyrir kostnaðarstað breytt til að styðja nýjan kostnaðarhlut IT EQUIPMENT.</span><span class="sxs-lookup"><span data-stu-id="5fe54-105">In the example, you change the dynamic allocation of the costs for the SALES cost center to support the new cost object IT EQUIPMENT.</span></span> <span data-ttu-id="5fe54-106">IT EQUIPMENT pakkar hafa vörunúmer frá 8904-W til 8924-W.</span><span class="sxs-lookup"><span data-stu-id="5fe54-106">IT EQUIPMENT packages have item numbers in the range from 8904-W to 8924-W.</span></span> <span data-ttu-id="5fe54-107">Sölutölur fyrra árs eru notaðar til að reikna út hlutdeild.</span><span class="sxs-lookup"><span data-stu-id="5fe54-107">You use the previous year’s sales figures to calculate the share.</span></span> <span data-ttu-id="5fe54-108">Úthlutunin er bókuð í aukakostnaðartegund 9903.</span><span class="sxs-lookup"><span data-stu-id="5fe54-108">The allocation is posted to the helping cost type 9903.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="5fe54-109">Í dæminu er notast við sýnigögnin í [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="5fe54-109">The example uses the demo data in the [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  

## <a name="to-define-dynamic-allocations-based-on-items-sold-in-the-previous-year"></a><span data-ttu-id="5fe54-110">Til að skilgreina kvikar úthlutanir sem byggja á vörum sem seldar voru á síðasta ári</span><span class="sxs-lookup"><span data-stu-id="5fe54-110">To define dynamic allocations based on items sold in the previous year</span></span>  

1.  <span data-ttu-id="5fe54-111">Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Kostnaðarúthlutanir** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="5fe54-111">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Cost Allocations**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="5fe54-112">Í glugganum **Kostnaðarúthlutun** skal velja aðgerðina **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="5fe54-112">In the **Cost Allocation** window, choose the **New** action.</span></span>  
3.  <span data-ttu-id="5fe54-113">Í reitnum **Kenni** smellið á færslulykilinn eða sláið inn auðkenni.</span><span class="sxs-lookup"><span data-stu-id="5fe54-113">In the **ID** field, press Enter or enter an ID.</span></span>  
4.  <span data-ttu-id="5fe54-114">Í reitinn **Stig**, sláið inn **1**.</span><span class="sxs-lookup"><span data-stu-id="5fe54-114">In the **Level** field, enter **1**.</span></span>  
5.  <span data-ttu-id="5fe54-115">Í reitnum **Gildir frá** og **Gildir til** eru viðeigandi dagsetningar færðar inn.</span><span class="sxs-lookup"><span data-stu-id="5fe54-115">In the **Valid From** and **Valid To** fields, enter appropriate dates.</span></span>  
6.  <span data-ttu-id="5fe54-116">Í reitinn **Kóði kostnaðarstaðar** er slegið inn **SALA**.</span><span class="sxs-lookup"><span data-stu-id="5fe54-116">In the **Cost Center Code** field, enter **SALES**.</span></span>  
7.  <span data-ttu-id="5fe54-117">Í **Kreditfært í kostnaðartegund** reitinn er slegin inn kostnaðargerðin **9903**.</span><span class="sxs-lookup"><span data-stu-id="5fe54-117">In the **Credit to Cost Type** field, enter the cost type **9903**.</span></span>  
8.  <span data-ttu-id="5fe54-118">Í **Markkostnaðartegund** reitinn er slegin inn kostnaðargerðin **9903**.</span><span class="sxs-lookup"><span data-stu-id="5fe54-118">In the **Target Cost Type** field, enter the cost type **9903**.</span></span>  
9. <span data-ttu-id="5fe54-119">Í reitnum **Markkostnaðarhlutur** veljið **Nýtt** til að stofna nýja kostnaðarhlutinn IT EQUIPMENT og fyllt er í reitina eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="5fe54-119">In the **Target Cost Object** field, choose **New** to create a new cost object IT EQUIPMENT and fill in fields as necessary.</span></span> <span data-ttu-id="5fe54-120">Veljið **IT EQUIPMENT**.</span><span class="sxs-lookup"><span data-stu-id="5fe54-120">Select **IT EQUIPMENT**.</span></span> <span data-ttu-id="5fe54-121">Reiturinn **Markkostnaðarstaður** er hafður auður.</span><span class="sxs-lookup"><span data-stu-id="5fe54-121">Leave the **Target Cost Center** field blank.</span></span>  
10. <span data-ttu-id="5fe54-122">Í reitnum **Gerð úthlutunarmarka**, veljið **Allur kostnaður** til að tilgreina hvernig öllum uppsöfnuðum kostnaði er úthlutað.</span><span class="sxs-lookup"><span data-stu-id="5fe54-122">In the **Allocation Target Type** field, select **All Costs** to define how all accumulated costs are allocated.</span></span>  
11. <span data-ttu-id="5fe54-123">Í reitnum **Grunnur** veljið úthlutunarstofninn **Seldar vörur (upphæð)**.</span><span class="sxs-lookup"><span data-stu-id="5fe54-123">In the **Base** field, select the allocation base **Items Sold (Amount)**.</span></span>  
12. <span data-ttu-id="5fe54-124">Í retinn **Númersafmörkun** er fært inn **8904-W..8924-W**.</span><span class="sxs-lookup"><span data-stu-id="5fe54-124">In the **No. Filter** field, enter **8904-W..8924-W**.</span></span>  
13. <span data-ttu-id="5fe54-125">Í reitinn **Kóði gagnaafmörkunar** er fært inn **Síðasta ár**.</span><span class="sxs-lookup"><span data-stu-id="5fe54-125">In the **Date Filter Code** field, enter **Last Year**.</span></span>  
14. <span data-ttu-id="5fe54-126">Veljið **Reikna úthlutunarlykil** aðgerðina til að reikna út hlutinn.</span><span class="sxs-lookup"><span data-stu-id="5fe54-126">Choose the **Calculate Allocation Key** action to calculate the share.</span></span>  

    > [!IMPORTANT]  
    >  [!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="5fe54-127"> notar sölutölur fyrri ára til að reikna hlut 1596.50 SGM með 100 prósentum fyrir pakka IT EQUIPMENT.</span><span class="sxs-lookup"><span data-stu-id="5fe54-127"> uses the previous years’ sales figures to calculate a share of 1596.50 LCY with 100 percent for the IT EQUIPMENT packages.</span></span> <span data-ttu-id="5fe54-128">Þetta merkir að öllum seldum vörum síðasta árs verður úthlutað á kostnaðarhlutinn IT EQUIPMENT.</span><span class="sxs-lookup"><span data-stu-id="5fe54-128">This means that all of the items sold last year will be allocated to the cost object IT EQUIPMENT.</span></span>  

## <a name="see-also"></a><span data-ttu-id="5fe54-129">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="5fe54-129">See Also</span></span>  
 <span data-ttu-id="5fe54-130">[Uppsetning afmarkanir fyrir Kvik úthlutunargrunnar.](finance-setting-filters-for-dynamic-allocation-bases.md) </span><span class="sxs-lookup"><span data-stu-id="5fe54-130">[Setting Filters for Dynamic Allocation Bases](finance-setting-filters-for-dynamic-allocation-bases.md) </span></span>  
 <span data-ttu-id="5fe54-131">[Setja upp uppruna og markhópa úthlutanna](finance-how-to-set-up-allocation-source-and-targets.md) </span><span class="sxs-lookup"><span data-stu-id="5fe54-131">[Set Up Allocation Source and Targets](finance-how-to-set-up-allocation-source-and-targets.md) </span></span>  
 <span data-ttu-id="5fe54-132">[Skilgreina og úthluta kostnaði](finance-define-and-allocate-costs.md) </span><span class="sxs-lookup"><span data-stu-id="5fe54-132">[Defining and Allocating Costs](finance-define-and-allocate-costs.md) </span></span>  
 <span data-ttu-id="5fe54-133">[Orðalisti í kostnaðarbókhaldi](finance-terminology-in-cost-accounting.md) </span><span class="sxs-lookup"><span data-stu-id="5fe54-133">[Terminology in Cost Accounting](finance-terminology-in-cost-accounting.md) </span></span>  
 [<span data-ttu-id="5fe54-134">Um kostnaðarbókhald</span><span class="sxs-lookup"><span data-stu-id="5fe54-134">About Cost Accounting</span></span>](finance-about-cost-accounting.md)

