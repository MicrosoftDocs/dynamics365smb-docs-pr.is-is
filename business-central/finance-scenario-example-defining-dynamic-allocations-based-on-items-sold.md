---
title: Dæmi – Skilgreining kvikrar úthlutunar á grundvelli seldra vara | Microsoft Docs
description: Þetta efnisatriði sýnir dæmi um hvernig á að skilgreina úthlutanir með því að nota kvika úthlutunaraðferð.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
redirect_url: finance-define-and-allocate-costs
ms.openlocfilehash: 7219e1d56129da66e802aa0b4ea5df946dc34e04
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/29/2019
ms.locfileid: "1239591"
---
# <a name="scenario-example-defining-dynamic-allocations-based-on-items-sold"></a><span data-ttu-id="bd295-103">Dæmi: Skilgreining kvikrar úthlutunar á grundvelli seldra vara</span><span class="sxs-lookup"><span data-stu-id="bd295-103">Scenario Example: Defining Dynamic Allocations Based on Items Sold</span></span>
<span data-ttu-id="bd295-104">Þetta efnisatriði sýnir dæmi um hvernig á að skilgreina úthlutanir með því að nota kvika úthlutunaraðferð.</span><span class="sxs-lookup"><span data-stu-id="bd295-104">This topic shows an example of how to define allocations by using the dynamic allocation method.</span></span> <span data-ttu-id="bd295-105">Í dæminu er kvika úthlutun af kostnaði fyrir kostnaðarstað breytt til að styðja nýjan kostnaðarhlut IT EQUIPMENT.</span><span class="sxs-lookup"><span data-stu-id="bd295-105">In the example, you change the dynamic allocation of the costs for the SALES cost center to support the new cost object IT EQUIPMENT.</span></span> <span data-ttu-id="bd295-106">IT EQUIPMENT pakkar hafa vörunúmer frá 8904-W til 8924-W.</span><span class="sxs-lookup"><span data-stu-id="bd295-106">IT EQUIPMENT packages have item numbers in the range from 8904-W to 8924-W.</span></span> <span data-ttu-id="bd295-107">Sölutölur fyrra árs eru notaðar til að reikna út hlutdeild.</span><span class="sxs-lookup"><span data-stu-id="bd295-107">You use the previous year’s sales figures to calculate the share.</span></span> <span data-ttu-id="bd295-108">Úthlutunin er bókuð í aukakostnaðartegund 9903.</span><span class="sxs-lookup"><span data-stu-id="bd295-108">The allocation is posted to the helping cost type 9903.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="bd295-109">Í dæminu er notast við sýnigögnin í [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="bd295-109">The example uses the demo data in the [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  

## <a name="to-define-dynamic-allocations-based-on-items-sold-in-the-previous-year"></a><span data-ttu-id="bd295-110">Til að skilgreina kvikar úthlutanir sem byggja á vörum sem seldar voru á síðasta ári</span><span class="sxs-lookup"><span data-stu-id="bd295-110">To define dynamic allocations based on items sold in the previous year</span></span>  

1.  <span data-ttu-id="bd295-111">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Kostnaðarúthlutanir** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="bd295-111">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Cost Allocations**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="bd295-112">Á síðunni **Kostnaðarúthlutun** skal velja aðgerðina **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="bd295-112">On the **Cost Allocation** page, choose the **New** action.</span></span>  
3.  <span data-ttu-id="bd295-113">Í reitnum **Kenni** smellið á færslulykilinn eða sláið inn auðkenni.</span><span class="sxs-lookup"><span data-stu-id="bd295-113">In the **ID** field, press Enter or enter an ID.</span></span>  
4.  <span data-ttu-id="bd295-114">Í reitinn **Stig**, sláið inn **1**.</span><span class="sxs-lookup"><span data-stu-id="bd295-114">In the **Level** field, enter **1**.</span></span>  
5.  <span data-ttu-id="bd295-115">Í reitnum **Gildir frá** og **Gildir til** eru viðeigandi dagsetningar færðar inn.</span><span class="sxs-lookup"><span data-stu-id="bd295-115">In the **Valid From** and **Valid To** fields, enter appropriate dates.</span></span>  
6.  <span data-ttu-id="bd295-116">Í reitinn **Kóði kostnaðarstaðar** er slegið inn **SALA**.</span><span class="sxs-lookup"><span data-stu-id="bd295-116">In the **Cost Center Code** field, enter **SALES**.</span></span>  
7.  <span data-ttu-id="bd295-117">Í **Kreditfært í kostnaðartegund** reitinn er slegin inn kostnaðargerðin **9903**.</span><span class="sxs-lookup"><span data-stu-id="bd295-117">In the **Credit to Cost Type** field, enter the cost type **9903**.</span></span>  
8.  <span data-ttu-id="bd295-118">Í **Markkostnaðartegund** reitinn er slegin inn kostnaðargerðin **9903**.</span><span class="sxs-lookup"><span data-stu-id="bd295-118">In the **Target Cost Type** field, enter the cost type **9903**.</span></span>  
9. <span data-ttu-id="bd295-119">Í reitnum **Markkostnaðarhlutur** veljið **Nýtt** til að stofna nýja kostnaðarhlutinn IT EQUIPMENT og fyllt er í reitina eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="bd295-119">In the **Target Cost Object** field, choose **New** to create a new cost object IT EQUIPMENT and fill in fields as necessary.</span></span> <span data-ttu-id="bd295-120">Veljið **IT EQUIPMENT**.</span><span class="sxs-lookup"><span data-stu-id="bd295-120">Select **IT EQUIPMENT**.</span></span> <span data-ttu-id="bd295-121">Reiturinn **Markkostnaðarstaður** er hafður auður.</span><span class="sxs-lookup"><span data-stu-id="bd295-121">Leave the **Target Cost Center** field blank.</span></span>  
10. <span data-ttu-id="bd295-122">Í reitnum **Gerð úthlutunarmarka**, veljið **Allur kostnaður** til að tilgreina hvernig öllum uppsöfnuðum kostnaði er úthlutað.</span><span class="sxs-lookup"><span data-stu-id="bd295-122">In the **Allocation Target Type** field, select **All Costs** to define how all accumulated costs are allocated.</span></span>  
11. <span data-ttu-id="bd295-123">Í reitnum **Grunnur** veljið úthlutunarstofninn **Seldar vörur (upphæð)**.</span><span class="sxs-lookup"><span data-stu-id="bd295-123">In the **Base** field, select the allocation base **Items Sold (Amount)**.</span></span>  
12. <span data-ttu-id="bd295-124">Í retinn **Númersafmörkun** er fært inn **8904-W..8924-W**.</span><span class="sxs-lookup"><span data-stu-id="bd295-124">In the **No. Filter** field, enter **8904-W..8924-W**.</span></span>  
13. <span data-ttu-id="bd295-125">Í reitinn **Kóði gagnaafmörkunar** er fært inn **Síðasta ár**.</span><span class="sxs-lookup"><span data-stu-id="bd295-125">In the **Date Filter Code** field, enter **Last Year**.</span></span>  
14. <span data-ttu-id="bd295-126">Veljið **Reikna úthlutunarlykil** aðgerðina til að reikna út hlutinn.</span><span class="sxs-lookup"><span data-stu-id="bd295-126">Choose the **Calculate Allocation Key** action to calculate the share.</span></span>  

    > [!IMPORTANT]  
    >  [!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="bd295-127">notar sölutölur fyrri ára til að reikna hlut 1596.50 SGM með 100 prósentum fyrir pakka IT EQUIPMENT.</span><span class="sxs-lookup"><span data-stu-id="bd295-127">uses the previous years’ sales figures to calculate a share of 1596.50 LCY with 100 percent for the IT EQUIPMENT packages.</span></span> <span data-ttu-id="bd295-128">Þetta merkir að öllum seldum vörum síðasta árs verður úthlutað á kostnaðarhlutinn IT EQUIPMENT.</span><span class="sxs-lookup"><span data-stu-id="bd295-128">This means that all of the items sold last year will be allocated to the cost object IT EQUIPMENT.</span></span>  

## <a name="see-also"></a><span data-ttu-id="bd295-129">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="bd295-129">See Also</span></span>  
[<span data-ttu-id="bd295-130">Skilgreina og úthluta kostnaði</span><span class="sxs-lookup"><span data-stu-id="bd295-130">Defining and Allocating Costs</span></span>](finance-define-and-allocate-costs.md)  
<span data-ttu-id="bd295-131">[Orðalisti í kostnaðarbókhaldi](finance-terminology-in-cost-accounting.md) </span><span class="sxs-lookup"><span data-stu-id="bd295-131">[Terminology in Cost Accounting](finance-terminology-in-cost-accounting.md) </span></span>  
[<span data-ttu-id="bd295-132">Um kostnaðarbókhald</span><span class="sxs-lookup"><span data-stu-id="bd295-132">About Cost Accounting</span></span>](finance-about-cost-accounting.md)
