---
title: "Hvernig á að bakfæra frálagsbókun | Microsoft Docs"
description: "Stundum verður að bakfæra frálagsbókun. Dæmi um þetta væri ef gagnafærsluvilla ætti sér stað og rangt magn af frálagi væri bókað í Framleiðslupöntun."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: fb107d6d165ede233799ab165d735c030c0c8bba
ms.contentlocale: is-is
ms.lasthandoff: 09/28/2018

---
# <a name="reverse-output-posting"></a><span data-ttu-id="6e899-104">Bakfæra frálagsbókun</span><span class="sxs-lookup"><span data-stu-id="6e899-104">Reverse Output Posting</span></span>
<span data-ttu-id="6e899-105">Stundum verður að bakfæra frálagsbókun.</span><span class="sxs-lookup"><span data-stu-id="6e899-105">There are times when output posting must be reversed.</span></span> <span data-ttu-id="6e899-106">Dæmi um þetta væri ef gagnafærsluvilla ætti sér stað og rangt magn af frálagi væri bókað í Framleiðslupöntun.</span><span class="sxs-lookup"><span data-stu-id="6e899-106">An example of this would be if a data entry error occurred and an incorrect amount of output is posted to a production order.</span></span>  

## <a name="to-reverse-an-output-posting"></a><span data-ttu-id="6e899-107">Til að bakfæra frálagsbókun</span><span class="sxs-lookup"><span data-stu-id="6e899-107">To reverse an output posting</span></span>  
1.  <span data-ttu-id="6e899-108">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **frálagsbók** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="6e899-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Output Journal**, and then choose the related link.</span></span> <span data-ttu-id="6e899-109">Veljið keyrsluna.</span><span class="sxs-lookup"><span data-stu-id="6e899-109">Select your batch.</span></span>  
2. <span data-ttu-id="6e899-110">Fyllið inn í reitina eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="6e899-110">Fill in the fields as necessary.</span></span> <span data-ttu-id="6e899-111">Frekari upplýsingar, sjá [Fjöldabóka frálag og keyrslutíma](production-how-to-post-output-quantity.md).</span><span class="sxs-lookup"><span data-stu-id="6e899-111">For more information, see [Batch Post Output and Run Times](production-how-to-post-output-quantity.md).</span></span>
3.  <span data-ttu-id="6e899-112">Í reitnum **Jafna færslu** veljið tengda birgðafærslu.</span><span class="sxs-lookup"><span data-stu-id="6e899-112">In the **Applies-To Entry** field, select the associated item ledger entry.</span></span> <span data-ttu-id="6e899-113">Þá bakfærast birgðafærslurnar og afkastagetufærslurnar.</span><span class="sxs-lookup"><span data-stu-id="6e899-113">This reverses the capacity and item ledger entries.</span></span>  
4. <span data-ttu-id="6e899-114">Bóka bakfærsluna með því að bóka færslubókina.</span><span class="sxs-lookup"><span data-stu-id="6e899-114">Post the reversal by posting the journal.</span></span>  

<span data-ttu-id="6e899-115">Færslurnar í Frálagsbókinni eru bókaðar í vörubókina sem jákvæð leiðrétting.</span><span class="sxs-lookup"><span data-stu-id="6e899-115">The output journal entries are posted to the item ledger as a positive adjustment.</span></span>  

## <a name="see-also"></a><span data-ttu-id="6e899-116">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="6e899-116">See Also</span></span>  
 <span data-ttu-id="6e899-117">[Framleiðsla](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="6e899-117">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
 [<span data-ttu-id="6e899-118">Uppsetning framleiðslu</span><span class="sxs-lookup"><span data-stu-id="6e899-118">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
 <span data-ttu-id="6e899-119">[Áætlun](production-planning.md)    </span><span class="sxs-lookup"><span data-stu-id="6e899-119">[Planning](production-planning.md)    </span></span>  
 [<span data-ttu-id="6e899-120">Birgðir</span><span class="sxs-lookup"><span data-stu-id="6e899-120">Inventory</span></span>](inventory-manage-inventory.md)  
 [<span data-ttu-id="6e899-121">Innkaup</span><span class="sxs-lookup"><span data-stu-id="6e899-121">Purchasing</span></span>](purchasing-manage-purchasing.md)  
 <span data-ttu-id="6e899-122">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="6e899-122">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

