---
title: Hvernig á að bakfæra frálagsbókun | Microsoft Docs
description: Stundum verður að bakfæra frálagsbókun. Dæmi um þetta væri ef gagnafærsluvilla ætti sér stað og rangt magn af frálagi væri bókað í Framleiðslupöntun.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: cad24d75cacc290ea69f3a4488efd8dc9832a42c
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5787778"
---
# <a name="reverse-output-posting"></a><span data-ttu-id="3e359-104">Bakfæra frálagsbókun</span><span class="sxs-lookup"><span data-stu-id="3e359-104">Reverse Output Posting</span></span>
<span data-ttu-id="3e359-105">Stundum verður að bakfæra frálagsbókun.</span><span class="sxs-lookup"><span data-stu-id="3e359-105">There are times when output posting must be reversed.</span></span> <span data-ttu-id="3e359-106">Dæmi um þetta væri ef gagnafærsluvilla ætti sér stað og rangt magn af frálagi væri bókað í Framleiðslupöntun.</span><span class="sxs-lookup"><span data-stu-id="3e359-106">An example of this would be if a data entry error occurred and an incorrect amount of output is posted to a production order.</span></span>  

## <a name="to-reverse-an-output-posting"></a><span data-ttu-id="3e359-107">Til að bakfæra frálagsbókun</span><span class="sxs-lookup"><span data-stu-id="3e359-107">To reverse an output posting</span></span>  
1.  <span data-ttu-id="3e359-108">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Frálagsbók** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="3e359-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Output Journal**, and then choose the related link.</span></span> <span data-ttu-id="3e359-109">Veljið keyrsluna.</span><span class="sxs-lookup"><span data-stu-id="3e359-109">Select your batch.</span></span>  
2. <span data-ttu-id="3e359-110">Fyllið inn í reitina eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="3e359-110">Fill in the fields as necessary.</span></span> <span data-ttu-id="3e359-111">Frekari upplýsingar, sjá [Fjöldabóka frálag og keyrslutíma](production-how-to-post-output-quantity.md).</span><span class="sxs-lookup"><span data-stu-id="3e359-111">For more information, see [Batch Post Output and Run Times](production-how-to-post-output-quantity.md).</span></span>
3.  <span data-ttu-id="3e359-112">Í reitnum **Jafna færslu** veljið tengda birgðafærslu.</span><span class="sxs-lookup"><span data-stu-id="3e359-112">In the **Applies-To Entry** field, select the associated item ledger entry.</span></span> <span data-ttu-id="3e359-113">Þá bakfærast birgðafærslurnar og afkastagetufærslurnar.</span><span class="sxs-lookup"><span data-stu-id="3e359-113">This reverses the capacity and item ledger entries.</span></span>  
4. <span data-ttu-id="3e359-114">Bóka bakfærsluna með því að bóka færslubókina.</span><span class="sxs-lookup"><span data-stu-id="3e359-114">Post the reversal by posting the journal.</span></span>  

<span data-ttu-id="3e359-115">Færslurnar í Frálagsbókinni eru bókaðar í vörubókina sem jákvæð leiðrétting.</span><span class="sxs-lookup"><span data-stu-id="3e359-115">The output journal entries are posted to the item ledger as a positive adjustment.</span></span>  

## <a name="see-also"></a><span data-ttu-id="3e359-116">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="3e359-116">See Also</span></span>  
 <span data-ttu-id="3e359-117">[Framleiðsla](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="3e359-117">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
 [<span data-ttu-id="3e359-118">Uppsetning framleiðslu</span><span class="sxs-lookup"><span data-stu-id="3e359-118">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
 <span data-ttu-id="3e359-119">[Áætlun](production-planning.md)    </span><span class="sxs-lookup"><span data-stu-id="3e359-119">[Planning](production-planning.md)    </span></span>  
 [<span data-ttu-id="3e359-120">Birgðir</span><span class="sxs-lookup"><span data-stu-id="3e359-120">Inventory</span></span>](inventory-manage-inventory.md)  
 [<span data-ttu-id="3e359-121">Innkaup</span><span class="sxs-lookup"><span data-stu-id="3e359-121">Purchasing</span></span>](purchasing-manage-purchasing.md)  
 <span data-ttu-id="3e359-122">[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="3e359-122">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  


[!INCLUDE[footer-include](includes/footer-banner.md)]