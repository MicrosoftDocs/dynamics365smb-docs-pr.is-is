---
title: Hvernig á að bakfæra frálagsbókun | Microsoft Docs
description: Stundum verður að bakfæra frálagsbókun. Dæmi um þetta væri ef gagnafærsluvilla ætti sér stað og rangt magn af frálagi væri bókað í Framleiðslupöntun.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 7ff9557d088bec5fb76e4bf673ad4afd244e08bf
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/01/2019
ms.locfileid: "2313157"
---
# <a name="reverse-output-posting"></a><span data-ttu-id="dafca-104">Bakfæra frálagsbókun</span><span class="sxs-lookup"><span data-stu-id="dafca-104">Reverse Output Posting</span></span>
<span data-ttu-id="dafca-105">Stundum verður að bakfæra frálagsbókun.</span><span class="sxs-lookup"><span data-stu-id="dafca-105">There are times when output posting must be reversed.</span></span> <span data-ttu-id="dafca-106">Dæmi um þetta væri ef gagnafærsluvilla ætti sér stað og rangt magn af frálagi væri bókað í Framleiðslupöntun.</span><span class="sxs-lookup"><span data-stu-id="dafca-106">An example of this would be if a data entry error occurred and an incorrect amount of output is posted to a production order.</span></span>  

## <a name="to-reverse-an-output-posting"></a><span data-ttu-id="dafca-107">Til að bakfæra frálagsbókun</span><span class="sxs-lookup"><span data-stu-id="dafca-107">To reverse an output posting</span></span>  
1.  <span data-ttu-id="dafca-108">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **frálagsbók** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="dafca-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Output Journal**, and then choose the related link.</span></span> <span data-ttu-id="dafca-109">Veljið keyrsluna.</span><span class="sxs-lookup"><span data-stu-id="dafca-109">Select your batch.</span></span>  
2. <span data-ttu-id="dafca-110">Fyllið inn í reitina eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="dafca-110">Fill in the fields as necessary.</span></span> <span data-ttu-id="dafca-111">Frekari upplýsingar, sjá [Fjöldabóka frálag og keyrslutíma](production-how-to-post-output-quantity.md).</span><span class="sxs-lookup"><span data-stu-id="dafca-111">For more information, see [Batch Post Output and Run Times](production-how-to-post-output-quantity.md).</span></span>
3.  <span data-ttu-id="dafca-112">Í reitnum **Jafna færslu** veljið tengda birgðafærslu.</span><span class="sxs-lookup"><span data-stu-id="dafca-112">In the **Applies-To Entry** field, select the associated item ledger entry.</span></span> <span data-ttu-id="dafca-113">Þá bakfærast birgðafærslurnar og afkastagetufærslurnar.</span><span class="sxs-lookup"><span data-stu-id="dafca-113">This reverses the capacity and item ledger entries.</span></span>  
4. <span data-ttu-id="dafca-114">Bóka bakfærsluna með því að bóka færslubókina.</span><span class="sxs-lookup"><span data-stu-id="dafca-114">Post the reversal by posting the journal.</span></span>  

<span data-ttu-id="dafca-115">Færslurnar í Frálagsbókinni eru bókaðar í vörubókina sem jákvæð leiðrétting.</span><span class="sxs-lookup"><span data-stu-id="dafca-115">The output journal entries are posted to the item ledger as a positive adjustment.</span></span>  

## <a name="see-also"></a><span data-ttu-id="dafca-116">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="dafca-116">See Also</span></span>  
 <span data-ttu-id="dafca-117">[Framleiðsla](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="dafca-117">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
 [<span data-ttu-id="dafca-118">Uppsetning framleiðslu</span><span class="sxs-lookup"><span data-stu-id="dafca-118">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
 <span data-ttu-id="dafca-119">[Áætlun](production-planning.md)    </span><span class="sxs-lookup"><span data-stu-id="dafca-119">[Planning](production-planning.md)    </span></span>  
 [<span data-ttu-id="dafca-120">Birgðir</span><span class="sxs-lookup"><span data-stu-id="dafca-120">Inventory</span></span>](inventory-manage-inventory.md)  
 [<span data-ttu-id="dafca-121">Innkaup</span><span class="sxs-lookup"><span data-stu-id="dafca-121">Purchasing</span></span>](purchasing-manage-purchasing.md)  
 <span data-ttu-id="dafca-122">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="dafca-122">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
