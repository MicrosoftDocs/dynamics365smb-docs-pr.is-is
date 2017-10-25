---
title: "Skilgreining fastrar úthlutunar á grundvelli úthlutunarhlutfalls | Microsoft Docs"
description: "Föst úthlutunaraðferð er byggð á tilteknu gildi, s.s. fermetrum í notkun eða skilgreindu úthlutunarhlutfalli, s.s. 5:2:4."
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
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: b48d7f73b640b98d0cdab6e2e7e7486a3bdb39db
ms.contentlocale: is-is
ms.lasthandoff: 09/22/2017

---
# <a name="scenario-example-defining-static-allocations-based-on-allocation-ratio"></a><span data-ttu-id="a0936-103">Dæmi: Skilgreining fastrar úthlutunar á grundvelli úthlutunarhlutfalls</span><span class="sxs-lookup"><span data-stu-id="a0936-103">Scenario Example: Defining Static Allocations Based on Allocation Ratio</span></span>
<span data-ttu-id="a0936-104">Föst úthlutunaraðferð er byggð á tilteknu gildi, s.s. fermetrum í notkun eða skilgreindu úthlutunarhlutfalli, s.s. 5:2:4.</span><span class="sxs-lookup"><span data-stu-id="a0936-104">Static allocation method is based on a definite value, such as square meters used, or an established allocation ratio such as 5:2:4.</span></span>  

<span data-ttu-id="a0936-105">Í þessu efnisatriði er lýst hvernig á að skilgreina þrjá nýja kostnaðarhluti úthlutunarmarks fyrir kostnaðarstað úthlutunarupprunans FRAML með fyrirliggjandi úthlutunarhlutfallinu 5:2:4.</span><span class="sxs-lookup"><span data-stu-id="a0936-105">This topic describes how to define three new allocation target cost objects for the allocation source PROD cost center using the established allocation ratio 5:2:4.</span></span> <span data-ttu-id="a0936-106">Kostnaðarhlutirnir þrír eru ACCESSO, PAINT og FITTINGS.</span><span class="sxs-lookup"><span data-stu-id="a0936-106">The three target cost objects are ACCESSO, PAINT, and FITTINGS.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="a0936-107">Í dæminu er notast við sýnigögnin í [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="a0936-107">The example uses the demo data in the [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  

## <a name="to-define-the-allocation-source-prod-cost-center-on-the-general-fasttab"></a><span data-ttu-id="a0936-108">Til að skilgreina PROD kostnaðarstað úthlutunarveitu á flýtiflipanum Almennt</span><span class="sxs-lookup"><span data-stu-id="a0936-108">To define the allocation source PROD cost center on the General FastTab</span></span>  

1.  <span data-ttu-id="a0936-109">Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn  **Kostnaðarúthlutun** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="a0936-109">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Cost Allocation**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="a0936-110">Í glugganum **Kostnaðarúthlutun** skal velja aðgerðina **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="a0936-110">In the **Cost Allocation** window, choose the **New** action.</span></span>  
3.  <span data-ttu-id="a0936-111">Í reitnum **Kenni** smellið á færslulykilinn eða sláið inn auðkenni.</span><span class="sxs-lookup"><span data-stu-id="a0936-111">In the **ID** field, press Enter or enter an ID.</span></span>  
4.  <span data-ttu-id="a0936-112">Í reitinn **Stig**, sláið inn **1**.</span><span class="sxs-lookup"><span data-stu-id="a0936-112">In the **Level** field, enter **1**.</span></span>  
5.  <span data-ttu-id="a0936-113">Í reitnum **Gildir frá** og **Gildir til** eru viðeigandi dagsetningar færðar inn.</span><span class="sxs-lookup"><span data-stu-id="a0936-113">In the **Valid From** and **Valid To** fields, enter appropriate dates.</span></span>  
6.  <span data-ttu-id="a0936-114">Í reitinn **Kóði kostnaðarstaðar** er slegið inn **SALA**.</span><span class="sxs-lookup"><span data-stu-id="a0936-114">In the **Cost Center Code** field, enter **PROD**.</span></span>  
7.  <span data-ttu-id="a0936-115">Í **Kreditfært í kostnaðartegund** reitinn er slegin inn kostnaðargerðin **9903**.</span><span class="sxs-lookup"><span data-stu-id="a0936-115">In the **Credit to Cost Type** field, enter the cost type **9903**.</span></span>  

## <a name="to-define-the-allocation-target-cost-objects-on-the-lines-fasttab"></a><span data-ttu-id="a0936-116">Til að skilgreina kostnaðarhluti úthlutunarmarks á flýtiflipanum Línur</span><span class="sxs-lookup"><span data-stu-id="a0936-116">To define the allocation target cost objects on the Lines FastTab</span></span>  

1.  <span data-ttu-id="a0936-117">Í fyrstu línunni í reitnum **Markkostnaðartegund** sláið inn **9903**.</span><span class="sxs-lookup"><span data-stu-id="a0936-117">On the first line, in the **Target Cost Type** field, enter **9903**.</span></span>  
2.  <span data-ttu-id="a0936-118">Í fyrstu línunni í reitnum **Markkostnaðarhlutur** veljið **ACCESSO**.</span><span class="sxs-lookup"><span data-stu-id="a0936-118">On the first line, in the **Target Cost Object** field, select **ACCESSO**.</span></span>  
3.  <span data-ttu-id="a0936-119">Í fyrstu línunni í reitnum **„Gerð úthlutunarmarka** veljið **Allur kostnaður** til að tilgreina hvernig öllum uppsöfnuðum kostnaði er úthlutað.</span><span class="sxs-lookup"><span data-stu-id="a0936-119">On the first line, in the **Allocation Target Type** field, select **All Costs** to define how all accrued costs are allocated.</span></span>  
4.  <span data-ttu-id="a0936-120">Í fyrstu línunni í reitnum **Grunnur** veljið **Fast** til að nota fasta úthlutunaraðferð.</span><span class="sxs-lookup"><span data-stu-id="a0936-120">On the first line, in the **Base** field, select **Static** to use the static allocation method.</span></span>  
5.  <span data-ttu-id="a0936-121">Í fyrstu línuna í reitnum **Deila** setjið inn úthlutunarhlutfallið **5**.</span><span class="sxs-lookup"><span data-stu-id="a0936-121">On the first line, in the **Share** field, enter the allocation ratio **5**.</span></span>  
6.  <span data-ttu-id="a0936-122">Í aðra línuna í reitnum **Markkostnaðartegund** sláið inn **9903**.</span><span class="sxs-lookup"><span data-stu-id="a0936-122">On the second line, in the **Target Cost Type** field, enter **9903**.</span></span>  
7.  <span data-ttu-id="a0936-123">Í annarri línunni, í reitnum **Markkostnaðarhlutur** er valið **MÁLNING**.</span><span class="sxs-lookup"><span data-stu-id="a0936-123">On the second line, in the **Target Cost Object** field, select **PAINT**.</span></span>  
8.  <span data-ttu-id="a0936-124">Í annarri línunni í reitnum **„Gerð úthlutunarmarka** veljið **Allur kostnaður** til að tilgreina hvernig öllum uppsöfnuðum kostnaði er úthlutað.</span><span class="sxs-lookup"><span data-stu-id="a0936-124">On the second line, in the **Allocation Target Type** field, select **All Costs** to define how all accrued costs are allocated.</span></span>  
9. <span data-ttu-id="a0936-125">Í annarri línunni, í reitnum **Grunnur**, er valið **Föst** til að nota fasta úthlutunaraðferð.</span><span class="sxs-lookup"><span data-stu-id="a0936-125">On the second line, in the **Base** field, select **Static** to use the static allocation method.</span></span>  
10. <span data-ttu-id="a0936-126">Í annarri línunni, í reitnum **Deila**, er sett inn úthlutunarhlutfallið **2**.</span><span class="sxs-lookup"><span data-stu-id="a0936-126">On the second line, in the **Share** field, enter the allocation ratio **2**.</span></span>  
11. <span data-ttu-id="a0936-127">Í þriðju línuna í reitnum **Markkostnaðartegund** sláið inn **9903**.</span><span class="sxs-lookup"><span data-stu-id="a0936-127">On the third line, in the **Target Cost Type** field, enter **9903**.</span></span>  
12. <span data-ttu-id="a0936-128">Í þriðju línunni í reitnum **Markkostnaðarhlutur**, er slegið inn **TENGIHLUTIR**.</span><span class="sxs-lookup"><span data-stu-id="a0936-128">On the third line, in the **Target Cost Object** field, select **FITTINGS**.</span></span>  
13. <span data-ttu-id="a0936-129">Í þriðju línunni í reitnum **„Gerð úthlutunarmarka** veljið **Allur kostnaður** til að tilgreina hvernig öllum uppsöfnuðum kostnaði er úthlutað.</span><span class="sxs-lookup"><span data-stu-id="a0936-129">On the third line, in the **Allocation Target Type** field, select **All Costs** to define how all accrued costs are allocated.</span></span>  
14. <span data-ttu-id="a0936-130">Í þriðju línunni í reitnum **Grunnur**, er valið **Föst** til að nota fasta úthlutunaraðferð.</span><span class="sxs-lookup"><span data-stu-id="a0936-130">On the third line, in the **Base** field, select **Static** to use the static allocation method.</span></span>  
15. <span data-ttu-id="a0936-131">Í þriðju línunni, í reitnum **Deila**, er sett inn úthlutunarhlutfallið **4**.</span><span class="sxs-lookup"><span data-stu-id="a0936-131">On the third line, in the **Share** field, enter the allocation ratio **4**.</span></span>  

> [!IMPORTANT]  
>  [!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="a0936-132"> reiknar sjálfkrafa reitinn **Prósenta** með því að nota prósentuhlutfall sem er háð öllum þremur úthlutunarhlutföllum sem færð eru inn í reitinn **Deila** í öllum þremur línunum.</span><span class="sxs-lookup"><span data-stu-id="a0936-132"> automatically calculates the **Percent** field using a percentage rate that is dependent on all three allocation ratios that are entered in the **Share** field for all three lines.</span></span>  

## <a name="see-also"></a><span data-ttu-id="a0936-133">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="a0936-133">See Also</span></span>  
<span data-ttu-id="a0936-134">[Hvernig á að setja upp uppruna og markhópa úthlutanna](finance-how-to-set-up-allocation-source-and-targets.md) </span><span class="sxs-lookup"><span data-stu-id="a0936-134">[How to: Set Up Allocation Source and Targets](finance-how-to-set-up-allocation-source-and-targets.md) </span></span>  
<span data-ttu-id="a0936-135">[Skilgreina og úthluta kostnaði](finance-define-and-allocate-costs.md) </span><span class="sxs-lookup"><span data-stu-id="a0936-135">[Defining and Allocating Costs](finance-define-and-allocate-costs.md) </span></span>  
<span data-ttu-id="a0936-136">[Dæmi: Skilgreining kvikrar úthlutunar á grundvelli seldra vara](finance-scenario-example-defining-dynamic-allocations-based-on-items-sold.md) </span><span class="sxs-lookup"><span data-stu-id="a0936-136">[Scenario Example: Defining Dynamic Allocations Based on Items Sold](finance-scenario-example-defining-dynamic-allocations-based-on-items-sold.md) </span></span>  
[<span data-ttu-id="a0936-137">Skilgreina og úthluta kostnaði</span><span class="sxs-lookup"><span data-stu-id="a0936-137">Defining and Allocating Costs</span></span>](finance-define-and-allocate-costs.md)

