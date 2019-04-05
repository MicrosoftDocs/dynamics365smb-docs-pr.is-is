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
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: fb107d6d165ede233799ab165d735c030c0c8bba
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/08/2019
ms.locfileid: "799736"
---
# <a name="reverse-output-posting"></a><span data-ttu-id="ef471-104">Bakfæra frálagsbókun</span><span class="sxs-lookup"><span data-stu-id="ef471-104">Reverse Output Posting</span></span>
<span data-ttu-id="ef471-105">Stundum verður að bakfæra frálagsbókun.</span><span class="sxs-lookup"><span data-stu-id="ef471-105">There are times when output posting must be reversed.</span></span> <span data-ttu-id="ef471-106">Dæmi um þetta væri ef gagnafærsluvilla ætti sér stað og rangt magn af frálagi væri bókað í Framleiðslupöntun.</span><span class="sxs-lookup"><span data-stu-id="ef471-106">An example of this would be if a data entry error occurred and an incorrect amount of output is posted to a production order.</span></span>  

## <a name="to-reverse-an-output-posting"></a><span data-ttu-id="ef471-107">Til að bakfæra frálagsbókun</span><span class="sxs-lookup"><span data-stu-id="ef471-107">To reverse an output posting</span></span>  
1.  <span data-ttu-id="ef471-108">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **frálagsbók** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="ef471-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Output Journal**, and then choose the related link.</span></span> <span data-ttu-id="ef471-109">Veljið keyrsluna.</span><span class="sxs-lookup"><span data-stu-id="ef471-109">Select your batch.</span></span>  
2. <span data-ttu-id="ef471-110">Fyllið inn í reitina eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="ef471-110">Fill in the fields as necessary.</span></span> <span data-ttu-id="ef471-111">Frekari upplýsingar, sjá [Fjöldabóka frálag og keyrslutíma](production-how-to-post-output-quantity.md).</span><span class="sxs-lookup"><span data-stu-id="ef471-111">For more information, see [Batch Post Output and Run Times](production-how-to-post-output-quantity.md).</span></span>
3.  <span data-ttu-id="ef471-112">Í reitnum **Jafna færslu** veljið tengda birgðafærslu.</span><span class="sxs-lookup"><span data-stu-id="ef471-112">In the **Applies-To Entry** field, select the associated item ledger entry.</span></span> <span data-ttu-id="ef471-113">Þá bakfærast birgðafærslurnar og afkastagetufærslurnar.</span><span class="sxs-lookup"><span data-stu-id="ef471-113">This reverses the capacity and item ledger entries.</span></span>  
4. <span data-ttu-id="ef471-114">Bóka bakfærsluna með því að bóka færslubókina.</span><span class="sxs-lookup"><span data-stu-id="ef471-114">Post the reversal by posting the journal.</span></span>  

<span data-ttu-id="ef471-115">Færslurnar í Frálagsbókinni eru bókaðar í vörubókina sem jákvæð leiðrétting.</span><span class="sxs-lookup"><span data-stu-id="ef471-115">The output journal entries are posted to the item ledger as a positive adjustment.</span></span>  

## <a name="see-also"></a><span data-ttu-id="ef471-116">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="ef471-116">See Also</span></span>  
 <span data-ttu-id="ef471-117">[Framleiðsla](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="ef471-117">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
 [<span data-ttu-id="ef471-118">Uppsetning framleiðslu</span><span class="sxs-lookup"><span data-stu-id="ef471-118">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
 <span data-ttu-id="ef471-119">[Áætlun](production-planning.md)    </span><span class="sxs-lookup"><span data-stu-id="ef471-119">[Planning](production-planning.md)    </span></span>  
 [<span data-ttu-id="ef471-120">Birgðir</span><span class="sxs-lookup"><span data-stu-id="ef471-120">Inventory</span></span>](inventory-manage-inventory.md)  
 [<span data-ttu-id="ef471-121">Innkaup</span><span class="sxs-lookup"><span data-stu-id="ef471-121">Purchasing</span></span>](purchasing-manage-purchasing.md)  
 <span data-ttu-id="ef471-122">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="ef471-122">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
