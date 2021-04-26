---
title: Fjöldabóka framleiðslufrálag og keyrslutíma
description: Frálagsmagnið sýnir framvindu vinnunnar sem lokið magn og notuð afköst vinnu eða vélastöðvar.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 923f68b13619013dd54062438c66192a682868bc
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5787878"
---
# <a name="batch-post-output-and-run-times"></a><span data-ttu-id="e140a-103">Fjöldabóka frálag og keyrslutíma</span><span class="sxs-lookup"><span data-stu-id="e140a-103">Batch Post Output and Run Times</span></span>
<span data-ttu-id="e140a-104">Frálagsmagnið sýnir framvindu vinnunnar sem lokið magn og notuð afköst vinnu eða vélastöðvar.</span><span class="sxs-lookup"><span data-stu-id="e140a-104">The output quantity represents the work progress in the form of the finished quantity and used capacity of work or machine center.</span></span>

<span data-ttu-id="e140a-105">Hægt er að nota frálagsbókina til að:</span><span class="sxs-lookup"><span data-stu-id="e140a-105">You can use the output journal to:</span></span>
*  <span data-ttu-id="e140a-106">Leiðréttir birgðir í tengslum við frálag tilbúinnar vörur frá framleiðslu.</span><span class="sxs-lookup"><span data-stu-id="e140a-106">Adjust inventory in connection with output of finished items from production.</span></span>
*  <span data-ttu-id="e140a-107">Skrá magn og rýrnun hverrar aðgerðar í framleiðsluleið.</span><span class="sxs-lookup"><span data-stu-id="e140a-107">Register quantities and scrap for each operation in production routing.</span></span>
*  <span data-ttu-id="e140a-108">Skrá uppsetningu og keyrslutíma fyrir vinnu og vélastöðvar.</span><span class="sxs-lookup"><span data-stu-id="e140a-108">Register setup and run time for work and machine centers.</span></span>

> [!NOTE]
> <span data-ttu-id="e140a-109">Ef framleiðsluleiðir eru notaðar eru birgðir aðeins uppfærðar þegar frálagsmagn er bókað í síðustu aðgerðinni.</span><span class="sxs-lookup"><span data-stu-id="e140a-109">If production routing are used, the inventory is updated only when you post output quantity on the last operation.</span></span>

<span data-ttu-id="e140a-110">Með glugganum **Framleiðslubók** er hægt að vinna sömu verk og í glugganum **Frálagsbók** og um leið framkvæma tengdar notkunarbókanir.</span><span class="sxs-lookup"><span data-stu-id="e140a-110">With the **Production Journal** window, you can perform the same tasks as in the **Output Journal** window and at the same time perform the related consumption posting tasks.</span></span> <span data-ttu-id="e140a-111">Frekari upplýsingar eru í [Skrá notkun og frálag fyrir eina útgefna framleiðslupöntunarlínu](production-how-to-register-consumption-and-output.md).</span><span class="sxs-lookup"><span data-stu-id="e140a-111">For more information, see [Register Consumption and Output for One Released Production order line](production-how-to-register-consumption-and-output.md).</span></span>

## <a name="to-post-output-quantities-andor-register-run-times-for-one-or-more-production-order-lines"></a><span data-ttu-id="e140a-112">Að bóka frálagsmagn og/eða skrá keyrslutíma fyrir eina eða fleiri framleiðslupantanalínur</span><span class="sxs-lookup"><span data-stu-id="e140a-112">To post output quantities and/or register run times for one or more production order lines</span></span>
1. <span data-ttu-id="e140a-113">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Frálagsbók** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="e140a-113">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Output Journal**, and then choose the related link.</span></span>  
2. <span data-ttu-id="e140a-114">Reitirnir eru fylltir út með framleiðslupöntunargögnunum og frálagsgögnunum og/eða keyrslutímanum.</span><span class="sxs-lookup"><span data-stu-id="e140a-114">Fill in the fields with the production order data and the output data and/or run time.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
  
    <span data-ttu-id="e140a-115">Hægt er að nota aðgerðina **Opna leið** til að mynda færslubókarlínur úr framleiðslupöntunum.</span><span class="sxs-lookup"><span data-stu-id="e140a-115">You can use the **Explode Routing** function to generate journal lines from production orders.</span></span>
  
4. <span data-ttu-id="e140a-116">Ef aðgerðinni er lokið skal velja reitinn **Lokið**.</span><span class="sxs-lookup"><span data-stu-id="e140a-116">If the operation has been completed, select the **Finished** field.</span></span>  
5. <span data-ttu-id="e140a-117">Veldu aðgerðina **Bóka** til að bóka aðgerðina.</span><span class="sxs-lookup"><span data-stu-id="e140a-117">Choose the **Post** action to post the operations.</span></span> 
 
<span data-ttu-id="e140a-118">Fjárhagsfærslur afkasta eru uppfærðar fyrir notaða vinnu eða vélastöðvar með upplýsingum um tíma og magn frálags og rýrnunar.</span><span class="sxs-lookup"><span data-stu-id="e140a-118">Capacity ledger entries are updated for the used work or machine centers with information about time and quantity of output and scrap.</span></span> <span data-ttu-id="e140a-119">Ef síðasta aðgerðin var bókuð verður vörunni bætt við birgðir.</span><span class="sxs-lookup"><span data-stu-id="e140a-119">If you posted the last operation, the item will be added to the inventory.</span></span> 

## <a name="see-also"></a><span data-ttu-id="e140a-120">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="e140a-120">See Also</span></span>  
<span data-ttu-id="e140a-121">[Bóka rýrnun handvirk](production-how-to-post-scrap.md)
[Bakfæra frálagsbókun](production-how-to-reverse-output-posting.md)
[Framleiðsla](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="e140a-121">[Post Scrap Manually](production-how-to-post-scrap.md)
[Reverse Output Posting](production-how-to-reverse-output-posting.md)
[Manufacturing](production-manage-manufacturing.md)  </span></span>  
[<span data-ttu-id="e140a-122">Uppsetning framleiðslu</span><span class="sxs-lookup"><span data-stu-id="e140a-122">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="e140a-123">[Áætlun](production-planning.md)    </span><span class="sxs-lookup"><span data-stu-id="e140a-123">[Planning](production-planning.md)    </span></span>  
[<span data-ttu-id="e140a-124">Birgðir</span><span class="sxs-lookup"><span data-stu-id="e140a-124">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="e140a-125">[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="e140a-125">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]
