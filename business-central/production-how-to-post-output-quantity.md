---
title: Hvernig á að fjöldabóka framleiðslufrálag og keyrslutíma | Microsoft Docs
description: Afkastsmagnið sýnir vinnuframvinduna í formi afgreidds magns.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: cb0f01c84cb82765c346e45273bff82fbd1a53af
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/09/2020
ms.locfileid: "3778485"
---
# <a name="batch-post-output-and-run-times"></a><span data-ttu-id="fe287-103">Fjöldabóka frálag og keyrslutíma</span><span class="sxs-lookup"><span data-stu-id="fe287-103">Batch Post Output and Run Times</span></span>
<span data-ttu-id="fe287-104">Afkastsmagnið sýnir vinnuframvinduna í formi afgreidds magns.</span><span class="sxs-lookup"><span data-stu-id="fe287-104">The output quantity represents the work progress in the form of the finished quantity.</span></span>  

> [!NOTE]
> <span data-ttu-id="fe287-105">Aðeins þegar afkastsmagn er bókað í síðustu aðgerðinni eru birgðir sjálfkrafa uppfærðar.</span><span class="sxs-lookup"><span data-stu-id="fe287-105">Only when you post output quantity on the last operation, the inventory is updated automatically.</span></span>  

## <a name="to-post-output-quantities-for-one-or-more-production-order-lines"></a><span data-ttu-id="fe287-106">Bóka frálagsmagn fyrir eina eða fleiri framleiðslupantanalínur</span><span class="sxs-lookup"><span data-stu-id="fe287-106">To post output quantities for one or more production order lines</span></span>
1. <span data-ttu-id="fe287-107">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Frálagsbók** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="fe287-107">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Output Journal**, and then choose the related link.</span></span>  
2. <span data-ttu-id="fe287-108">Reitirnir eru fylltir út með framleiðslupöntunargögnunum og frálagsgögnunum.</span><span class="sxs-lookup"><span data-stu-id="fe287-108">Fill in the fields with the production order data and the output data.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="fe287-109">Ef aðgerðinni er lokið skal velja reitinn **Lokið**.</span><span class="sxs-lookup"><span data-stu-id="fe287-109">If the operation has been completed, select the **Finished** field.</span></span>  

    <span data-ttu-id="fe287-110">Ef vöruhúsið þar sem ganga á frá vörunum notar hólf en krefst ekki frágangsvinnslu skal  tengja kóta hólfs við bókarlínuna til að tilgreina hvar skuli setja vörurnar í vöruhúsinu.</span><span class="sxs-lookup"><span data-stu-id="fe287-110">If the warehouse location where the items should be put away uses bins but does not require put-away processing,  assign a bin code to the journal line to specify where the items should be placed in the warehouse.</span></span> <span data-ttu-id="fe287-111">Frekari upplýsingar eru í [Ganga frá framleiðslu eða samsetningarúttaki](warehouse-how-to-put-away-production-output.md).</span><span class="sxs-lookup"><span data-stu-id="fe287-111">For more information, see [Put Away Production or Assembly Output](warehouse-how-to-put-away-production-output.md).</span></span>  

4. <span data-ttu-id="fe287-112">Veljið **Bókun** til að bóka aðgerðirnar.</span><span class="sxs-lookup"><span data-stu-id="fe287-112">Choose the **Post** acto post the operations.</span></span> <span data-ttu-id="fe287-113">Afkastsmagnið verður bókað.</span><span class="sxs-lookup"><span data-stu-id="fe287-113">The output quantity will be posted.</span></span> <span data-ttu-id="fe287-114">Varan er nú tilbúin til afhendingar.</span><span class="sxs-lookup"><span data-stu-id="fe287-114">The item is now available for shipping.</span></span>  

## <a name="to-post-run-times-for-one-or-more-production-order-lines"></a><span data-ttu-id="fe287-115">Bóka keyrslutími fyrir eina eða fleiri framleiðslupantanalínur</span><span class="sxs-lookup"><span data-stu-id="fe287-115">To post run times for one or more production order lines</span></span>
<span data-ttu-id="fe287-116">Keyrslutíminn sýnir vinnuframvinduna í formi nauðsynlegs vinnutíma.</span><span class="sxs-lookup"><span data-stu-id="fe287-116">The run time represents work progress in the form of the necessary working time.</span></span>    

1.  <span data-ttu-id="fe287-117">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Frálagsbók** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="fe287-117">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Output Journal**, and then choose the related link.</span></span>  
2. <span data-ttu-id="fe287-118">Reitirnir eru fylltir út með framleiðslupöntunargögnunum og frálagsgögnunum.</span><span class="sxs-lookup"><span data-stu-id="fe287-118">Fill in the fields with the production order data and the output data.</span></span>  
3.  <span data-ttu-id="fe287-119">Ef aðgerðinni er lokið skal velja reitinn **Lokið**.</span><span class="sxs-lookup"><span data-stu-id="fe287-119">If the operation is completed, select the **Finished** field.</span></span>  
4. <span data-ttu-id="fe287-120">Velja **bóka** aðgerðina til að bóka tíma eytt á aðgerð.</span><span class="sxs-lookup"><span data-stu-id="fe287-120">Choose the **Post** action to post the time spent per operation.</span></span> <span data-ttu-id="fe287-121">Afkastagetufærslur eru uppfærðar fyrir notaðar vinnu- eða vélastöðvar.</span><span class="sxs-lookup"><span data-stu-id="fe287-121">Capacity ledger entries are updated for the used work or machine centers.</span></span>

## <a name="see-also"></a><span data-ttu-id="fe287-122">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="fe287-122">See Also</span></span>  
<span data-ttu-id="fe287-123">[Framleiðsla](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="fe287-123">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
[<span data-ttu-id="fe287-124">Uppsetning framleiðslu</span><span class="sxs-lookup"><span data-stu-id="fe287-124">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="fe287-125">[Áætlun](production-planning.md)    </span><span class="sxs-lookup"><span data-stu-id="fe287-125">[Planning](production-planning.md)    </span></span>  
[<span data-ttu-id="fe287-126">Birgðir</span><span class="sxs-lookup"><span data-stu-id="fe287-126">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="fe287-127">Innkaup</span><span class="sxs-lookup"><span data-stu-id="fe287-127">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="fe287-128">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="fe287-128">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
