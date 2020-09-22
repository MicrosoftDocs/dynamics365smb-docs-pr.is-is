---
title: Hvernig á að bakfæra frálagsbókun | Microsoft Docs
description: Stundum verður að bakfæra frálagsbókun. Dæmi um þetta væri ef gagnafærsluvilla ætti sér stað og rangt magn af frálagi væri bókað í Framleiðslupöntun.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 33be858c687381a50f42d1c59ca735358f113d72
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/09/2020
ms.locfileid: "3788751"
---
# <a name="reverse-output-posting"></a><span data-ttu-id="9c07a-104">Bakfæra frálagsbókun</span><span class="sxs-lookup"><span data-stu-id="9c07a-104">Reverse Output Posting</span></span>
<span data-ttu-id="9c07a-105">Stundum verður að bakfæra frálagsbókun.</span><span class="sxs-lookup"><span data-stu-id="9c07a-105">There are times when output posting must be reversed.</span></span> <span data-ttu-id="9c07a-106">Dæmi um þetta væri ef gagnafærsluvilla ætti sér stað og rangt magn af frálagi væri bókað í Framleiðslupöntun.</span><span class="sxs-lookup"><span data-stu-id="9c07a-106">An example of this would be if a data entry error occurred and an incorrect amount of output is posted to a production order.</span></span>  

## <a name="to-reverse-an-output-posting"></a><span data-ttu-id="9c07a-107">Til að bakfæra frálagsbókun</span><span class="sxs-lookup"><span data-stu-id="9c07a-107">To reverse an output posting</span></span>  
1.  <span data-ttu-id="9c07a-108">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Frálagsbók** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="9c07a-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Output Journal**, and then choose the related link.</span></span> <span data-ttu-id="9c07a-109">Veljið keyrsluna.</span><span class="sxs-lookup"><span data-stu-id="9c07a-109">Select your batch.</span></span>  
2. <span data-ttu-id="9c07a-110">Fyllið inn í reitina eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="9c07a-110">Fill in the fields as necessary.</span></span> <span data-ttu-id="9c07a-111">Frekari upplýsingar, sjá [Fjöldabóka frálag og keyrslutíma](production-how-to-post-output-quantity.md).</span><span class="sxs-lookup"><span data-stu-id="9c07a-111">For more information, see [Batch Post Output and Run Times](production-how-to-post-output-quantity.md).</span></span>
3.  <span data-ttu-id="9c07a-112">Í reitnum **Jafna færslu** veljið tengda birgðafærslu.</span><span class="sxs-lookup"><span data-stu-id="9c07a-112">In the **Applies-To Entry** field, select the associated item ledger entry.</span></span> <span data-ttu-id="9c07a-113">Þá bakfærast birgðafærslurnar og afkastagetufærslurnar.</span><span class="sxs-lookup"><span data-stu-id="9c07a-113">This reverses the capacity and item ledger entries.</span></span>  
4. <span data-ttu-id="9c07a-114">Bóka bakfærsluna með því að bóka færslubókina.</span><span class="sxs-lookup"><span data-stu-id="9c07a-114">Post the reversal by posting the journal.</span></span>  

<span data-ttu-id="9c07a-115">Færslurnar í Frálagsbókinni eru bókaðar í vörubókina sem jákvæð leiðrétting.</span><span class="sxs-lookup"><span data-stu-id="9c07a-115">The output journal entries are posted to the item ledger as a positive adjustment.</span></span>  

## <a name="see-also"></a><span data-ttu-id="9c07a-116">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="9c07a-116">See Also</span></span>  
 <span data-ttu-id="9c07a-117">[Framleiðsla](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="9c07a-117">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
 [<span data-ttu-id="9c07a-118">Uppsetning framleiðslu</span><span class="sxs-lookup"><span data-stu-id="9c07a-118">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
 <span data-ttu-id="9c07a-119">[Áætlun](production-planning.md)    </span><span class="sxs-lookup"><span data-stu-id="9c07a-119">[Planning](production-planning.md)    </span></span>  
 [<span data-ttu-id="9c07a-120">Birgðir</span><span class="sxs-lookup"><span data-stu-id="9c07a-120">Inventory</span></span>](inventory-manage-inventory.md)  
 [<span data-ttu-id="9c07a-121">Innkaup</span><span class="sxs-lookup"><span data-stu-id="9c07a-121">Purchasing</span></span>](purchasing-manage-purchasing.md)  
 <span data-ttu-id="9c07a-122">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="9c07a-122">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
