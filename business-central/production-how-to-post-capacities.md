---
title: Hvernig á að bóka afkastagetu | Microsoft Docs
description: Afkastagetubókin er notuð til að bóka notaða afkastagetu sem ekki er úthlutuð á framleiðslupöntunina. Til dæmis má nefna að nauðsynlegt er að úthluta viðhaldsvinnu á afkastagetu en ekki á framleiðslupöntun.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 2fa0038745664c269d6d471c6d9373a9174df201
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/17/2020
ms.locfileid: "4759193"
---
# <a name="post-capacities"></a><span data-ttu-id="096ac-104">Bóka afkastagetu</span><span class="sxs-lookup"><span data-stu-id="096ac-104">Post Capacities</span></span>
<span data-ttu-id="096ac-105">Afkastagetubókin er notuð til að bóka notaða afkastagetu sem ekki er úthlutuð á framleiðslupöntunina.</span><span class="sxs-lookup"><span data-stu-id="096ac-105">In the capacity journal, you post consumed capacities that are not assigned to the production order.</span></span> <span data-ttu-id="096ac-106">Til dæmis má nefna að nauðsynlegt er að úthluta viðhaldsvinnu á afkastagetu en ekki á framleiðslupöntun.</span><span class="sxs-lookup"><span data-stu-id="096ac-106">For example, maintenance work must be assigned to capacity, but not to a production order.</span></span>  

## <a name="to-post-capacities"></a><span data-ttu-id="096ac-107">Bókun afkastagetu:</span><span class="sxs-lookup"><span data-stu-id="096ac-107">To post capacities</span></span>  
1.  <span data-ttu-id="096ac-108">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Afkastagetubækur** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="096ac-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Capacity Journals**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="096ac-109">Reitirnir **Bókunardags.** og **Fylgiskjal nr.** eru fylltir út .</span><span class="sxs-lookup"><span data-stu-id="096ac-109">Fill in the **Posting Date** and **Document No.** fields.</span></span>  
3.  <span data-ttu-id="096ac-110">Í reitinn **Tegund** er færð inn tegund afkastagetunnar, annaðhvort **Vélastöð** eða **Vinnustöð**, sem verið er að bóka.</span><span class="sxs-lookup"><span data-stu-id="096ac-110">In the **Type** field, enter the type of the capacity, either **Machine Center** or **Work Center**, that you are posting.</span></span>  
4.  <span data-ttu-id="096ac-111">Í reitnum **númer**</span><span class="sxs-lookup"><span data-stu-id="096ac-111">In the **No.**</span></span> <span data-ttu-id="096ac-112">er fært inn númer véla- eða vinnustöðvarinnar.</span><span class="sxs-lookup"><span data-stu-id="096ac-112">field, enter the number of the machine center or work center.</span></span>  
5.  <span data-ttu-id="096ac-113">Viðeigandi gögn eru færð inn í aðra reiti, s.s. **Upphafstími**, **Lokatími**, **Magn** og **Úrkast**.</span><span class="sxs-lookup"><span data-stu-id="096ac-113">Enter the relevant data in the other fields, such as **Starting Time**, **Ending Time**, **Quantity**, and **Scrap**.</span></span>  
6.  <span data-ttu-id="096ac-114">Velja **Bóka** aðgerðina til að bóka afkastagetuna.</span><span class="sxs-lookup"><span data-stu-id="096ac-114">Choose the **Post** action to post the capacities.</span></span>  

## <a name="to-view-work-center-ledger-entries"></a><span data-ttu-id="096ac-115">Skoða fjárhagsfærslur vinnustöðvar</span><span class="sxs-lookup"><span data-stu-id="096ac-115">To view work center ledger entries</span></span>  
<span data-ttu-id="096ac-116">Á síðunum **Vinnustöðvarspjald** og **Vélastöðvarspjald**, geturðu skoðað bókaða afkastagetu sem afrakstur afgreiddra framleiðslupantana.</span><span class="sxs-lookup"><span data-stu-id="096ac-116">In the **Work Center Card** and **Machine Center Card** pages, you can view the posted capacities as a result of finished production orders.</span></span>    
1.  <span data-ttu-id="096ac-117">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Vinnustöðvar** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="096ac-117">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Work Centers**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="096ac-118">Viðeigandi **vinnustöðvar** spjald er opnað úr listanum og aðgerðin **Afkastagetufærslur** valin.</span><span class="sxs-lookup"><span data-stu-id="096ac-118">Open the relevant **Work Center** card from the list, and then choose the **Capacity Ledger Entries** action.</span></span>  

<span data-ttu-id="096ac-119">Á síðunni **Afkastagetufærslur** eru birtar bókuðu færslurnar fyrir vinnustöðina í þeirri röð sem þær voru bókaðar.</span><span class="sxs-lookup"><span data-stu-id="096ac-119">The **Capacity Ledger Entries** page displays the posted entries from the work center in the order they were posted.</span></span>   

## <a name="see-also"></a><span data-ttu-id="096ac-120">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="096ac-120">See Also</span></span>  
<span data-ttu-id="096ac-121">[Framleiðsla](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="096ac-121">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
[<span data-ttu-id="096ac-122">Uppsetning framleiðslu</span><span class="sxs-lookup"><span data-stu-id="096ac-122">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="096ac-123">[Áætlun](production-planning.md)    </span><span class="sxs-lookup"><span data-stu-id="096ac-123">[Planning](production-planning.md)    </span></span>  
[<span data-ttu-id="096ac-124">Birgðir</span><span class="sxs-lookup"><span data-stu-id="096ac-124">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="096ac-125">Innkaup</span><span class="sxs-lookup"><span data-stu-id="096ac-125">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="096ac-126">[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="096ac-126">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>
