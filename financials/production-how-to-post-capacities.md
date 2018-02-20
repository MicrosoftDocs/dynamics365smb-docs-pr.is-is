---
title: "Hvernig á að bóka afkastagetu | Microsoft Docs"
description: "Afkastagetubókin er notuð til að bóka notaða afkastagetu sem ekki er úthlutuð á framleiðslupöntunina. Til dæmis má nefna að nauðsynlegt er að úthluta viðhaldsvinnu á afkastagetu en ekki á framleiðslupöntun."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: a30e62bf2bf62c547398d733fcfe80b0204805cf
ms.contentlocale: is-is
ms.lasthandoff: 01/30/2018

---
# <a name="post-capacities"></a><span data-ttu-id="90e94-104">Bóka afkastagetu</span><span class="sxs-lookup"><span data-stu-id="90e94-104">Post Capacities</span></span>
<span data-ttu-id="90e94-105">Afkastagetubókin er notuð til að bóka notaða afkastagetu sem ekki er úthlutuð á framleiðslupöntunina.</span><span class="sxs-lookup"><span data-stu-id="90e94-105">In the capacity journal, you post consumed capacities that are not assigned to the production order.</span></span> <span data-ttu-id="90e94-106">Til dæmis má nefna að nauðsynlegt er að úthluta viðhaldsvinnu á afkastagetu en ekki á framleiðslupöntun.</span><span class="sxs-lookup"><span data-stu-id="90e94-106">For example, maintenance work must be assigned to capacity, but not to a production order.</span></span>  

## <a name="to-post-capacities"></a><span data-ttu-id="90e94-107">Bókun afkastagetu:</span><span class="sxs-lookup"><span data-stu-id="90e94-107">To post capacities</span></span>  
1.  <span data-ttu-id="90e94-108">Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Afkastagetubók** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="90e94-108">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Capacity Journals**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="90e94-109">Reitirnir **Bókunardags.** og **Fylgiskjal nr.** eru fylltir út .</span><span class="sxs-lookup"><span data-stu-id="90e94-109">Fill in the **Posting Date** and **Document No.** fields.</span></span>  
3.  <span data-ttu-id="90e94-110">Í reitinn **Tegund** er færð inn tegund afkastagetunnar, annaðhvort **Vélastöð** eða **Vinnustöð**, sem verið er að bóka.</span><span class="sxs-lookup"><span data-stu-id="90e94-110">In the **Type** field, enter the type of the capacity, either **Machine Center** or **Work Center**, that you are posting.</span></span>  
4.  <span data-ttu-id="90e94-111">Í reitnum **númer**</span><span class="sxs-lookup"><span data-stu-id="90e94-111">In the **No.**</span></span> <span data-ttu-id="90e94-112">er fært inn númer véla- eða vinnustöðvarinnar.</span><span class="sxs-lookup"><span data-stu-id="90e94-112">field, enter the number of the machine center or work center.</span></span>  
5.  <span data-ttu-id="90e94-113">Viðeigandi gögn eru færð inn í aðra reiti, s.s. **Upphafstími**, **Lokatími**, **Magn** og **Úrkast**.</span><span class="sxs-lookup"><span data-stu-id="90e94-113">Enter the relevant data in the other fields, such as **Starting Time**, **Ending Time**, **Quantity**, and **Scrap**.</span></span>  
6.  <span data-ttu-id="90e94-114">Velja **Bóka** aðgerðina til að bóka afkastagetuna.</span><span class="sxs-lookup"><span data-stu-id="90e94-114">Choose the **Post** action to post the capacities.</span></span>  

## <a name="to-view-work-center-ledger-entries"></a><span data-ttu-id="90e94-115">Skoða fjárhagsfærslur vinnustöðvar</span><span class="sxs-lookup"><span data-stu-id="90e94-115">To view work center ledger entries</span></span>  
<span data-ttu-id="90e94-116">Í gluggunum **Vinnustöðvarspjald** og **Vélastöðvarspjald**, geturðu skoðað bókaða afkastagetu sem afrakstur afgreiddra framleiðslupantana.</span><span class="sxs-lookup"><span data-stu-id="90e94-116">In the **Work Center Card** and **Machine Center Card** windows, you can view the posted capacities as a result of finished production orders.</span></span>    
1.  <span data-ttu-id="90e94-117">Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **vinnustöðvar** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="90e94-117">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Work Centers**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="90e94-118">Viðeigandi **vinnustöðvar** spjald er opnað úr listanum og aðgerðin **Afkastagetufærslur** valin.</span><span class="sxs-lookup"><span data-stu-id="90e94-118">Open the relevant **Work Center** card from the list, and then choose the **Capacity Ledger Entries** action.</span></span>  

<span data-ttu-id="90e94-119">Í glugganum **Afkastagetufærslur** eru birtar bókuðu færslurnar fyrir vinnustöðina í þeirri röð sem þær voru bókaðar.</span><span class="sxs-lookup"><span data-stu-id="90e94-119">The **Capacity Ledger Entries** window displays the posted entries from the work center in the order they were posted.</span></span>   

## <a name="see-also"></a><span data-ttu-id="90e94-120">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="90e94-120">See Also</span></span>  
<span data-ttu-id="90e94-121">[Framleiðsla](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="90e94-121">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
[<span data-ttu-id="90e94-122">Uppsetning framleiðslu</span><span class="sxs-lookup"><span data-stu-id="90e94-122">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="90e94-123">[Áætlun](production-planning.md)    </span><span class="sxs-lookup"><span data-stu-id="90e94-123">[Planning](production-planning.md)    </span></span>  
[<span data-ttu-id="90e94-124">Birgðir</span><span class="sxs-lookup"><span data-stu-id="90e94-124">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="90e94-125">Innkaup</span><span class="sxs-lookup"><span data-stu-id="90e94-125">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="90e94-126">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="90e94-126">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

