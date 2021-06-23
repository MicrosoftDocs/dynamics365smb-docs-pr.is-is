---
title: Hönnunarupplýsingar - Sameining með birgðum | Microsoft Docs
description: Hlutarnir Vöruhúsakerfi og Birgðir vinna saman í efnislegum birgðum og leiðréttingu birgða eða vöruhúss.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/08/2021
ms.author: edupont
ms.openlocfilehash: 94eb1e0efa5c2a7ab54c46627b9d09ded6fae13f
ms.sourcegitcommit: 0953171d39e1232a7c126142d68cac858234a20e
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/09/2021
ms.locfileid: "6215154"
---
# <a name="design-details-integration-with-inventory"></a><span data-ttu-id="5fd2e-103">Hönnunarupplýsingar: Sameining með birgðum</span><span class="sxs-lookup"><span data-stu-id="5fd2e-103">Design Details: Integration with Inventory</span></span>
<span data-ttu-id="5fd2e-104">Hlutarnir Vöruhúsakerfi og Birgðir vinna saman í efnislegum birgðum og leiðréttingu birgða eða vöruhúss.</span><span class="sxs-lookup"><span data-stu-id="5fd2e-104">The Warehouse Management application area and the Inventory application area interact with one another in physical inventory and in inventory or warehouse adjustment.</span></span>  
  
## <a name="physical-inventory"></a><span data-ttu-id="5fd2e-105">Birgðir</span><span class="sxs-lookup"><span data-stu-id="5fd2e-105">Physical Inventory</span></span>  
 <span data-ttu-id="5fd2e-106">Síðan **Vöruh. - raunbirgðabók** er notaður með glugganum **Raunbirgðabók** fyrir allar ítarlegar staðsetningar vöruhúss.</span><span class="sxs-lookup"><span data-stu-id="5fd2e-106">The **Whse. Phys. Inventory Journal** page is used with the **Phys. Inventory Journal** page for all advanced warehouse locations.</span></span> <span data-ttu-id="5fd2e-107">Birgðir á hólfastigi eru reiknaðar úr og útprentaður listi afhendur starfsmanni vöruhúss.</span><span class="sxs-lookup"><span data-stu-id="5fd2e-107">The inventory on bin level is calculated, and a printed list is provided for the warehouse employee.</span></span> <span data-ttu-id="5fd2e-108">Listinn sýnir hvaða vörur í hvaða hólfum þarf að telja.</span><span class="sxs-lookup"><span data-stu-id="5fd2e-108">The list shows which items in which bins must be counted.</span></span>  
  
 <span data-ttu-id="5fd2e-109">Starfsmaður vöruhússins slær inn reiknað magn síðuna **Vöruh. - raunbirgðabók** og bókar svo færslubókina.</span><span class="sxs-lookup"><span data-stu-id="5fd2e-109">The warehouse employee enters the counted quantity on the **Whse. Phys. Inventory Journal** page and then posts the journal.</span></span>  
  
 <span data-ttu-id="5fd2e-110">Ef talið magn er meira en magn á færslubókarlínu er hreyfing bókuð fyrir þennan mun á milli sjálfgefna leiðréttingarhólfsins og talda hólfsins.</span><span class="sxs-lookup"><span data-stu-id="5fd2e-110">If the counted quantity is greater than the quantity on the journal line, a movement is posted for this difference from the default adjustment bin to the counted bin.</span></span> <span data-ttu-id="5fd2e-111">Þetta eykur magnið í talda hólfinu og minnkar magnið í sjálfgefna leiðréttingarhólfinu.</span><span class="sxs-lookup"><span data-stu-id="5fd2e-111">This increases the quantity in the counted bin and decreases the quantity in the default adjustment bin.</span></span>  
  
 <span data-ttu-id="5fd2e-112">Ef talið magn er minna en magnið á færslubókarlínunni er hreyfing fyrir þennan mun bókuð frá talda hólfinu í sjálfgefna leiðréttingarhólfið.</span><span class="sxs-lookup"><span data-stu-id="5fd2e-112">If the quantity counted is less than the quantity on the journal line, a movement for this difference is posted from the counted bin to the default adjustment bin.</span></span> <span data-ttu-id="5fd2e-113">Þetta lækkar magnið í talda hólfinu og eykur magnið í sjálfgefna leiðréttingarhólfinu.</span><span class="sxs-lookup"><span data-stu-id="5fd2e-113">This decreases the quantity in the counted bin and increases the quantity in the default adjustment bin.</span></span>  
  
 <span data-ttu-id="5fd2e-114">Í háþróaður vörugeymsla, gildi í **Magn reiknað** sviði er sótt frá birgðahöfuðbókarfærslur og gildi í **Magn raunverulegt magn á lager** reitur er sótt frá vöruhúsi færslum, að undanskildum jöfnunarhólfainnihaldi.</span><span class="sxs-lookup"><span data-stu-id="5fd2e-114">In advanced warehouse configurations, the value in the **Quantity (Calculated)** field is retrieved from item ledger entries and the value in the **Quantity (Phys. Inventory)** field is retrieved from warehouse entries, excluding the adjustment bin content.</span></span> <span data-ttu-id="5fd2e-115">Reiturinn **Magn** tilgreininn mismuninn á milli fyrstu reitanna tveggja, sem ætti að vera jafn innihaldinu í leiðréttingarhólfinu.</span><span class="sxs-lookup"><span data-stu-id="5fd2e-115">The **Quantity** field specifies the difference between the first two fields, which should be equal to the contents of the adjustment bin.</span></span>  
  
 <span data-ttu-id="5fd2e-116">Þegar þú bókar efnisbirgðabók eru birgðir og sjálfgefið leiðréttingahólf uppfærð.</span><span class="sxs-lookup"><span data-stu-id="5fd2e-116">When you post the physical inventory journal, the inventory and the default adjustment bin are updated.</span></span>  
  
### <a name="warehouse-adjustments-to-the-item-ledger"></a><span data-ttu-id="5fd2e-117">Vöruhúsaleiðréttingar í birgðahöfuðbók</span><span class="sxs-lookup"><span data-stu-id="5fd2e-117">Warehouse Adjustments to the Item Ledger</span></span>  
 <span data-ttu-id="5fd2e-118">Síðan **birgðabók** og aðgerðin **Reikna vöruhúsaleiðréttingu** er notuð til að jafna birgðir í birgðabók samkvæmt leiðréttingu sem hefur verið gerð á birgðamagni í vöruhúsahólfi.</span><span class="sxs-lookup"><span data-stu-id="5fd2e-118">You use the **Item Journal** page and the **Calculate Whse. Adjustment** function to adjust inventory on the item ledger in accordance with an adjustment that has been made to the item quantity in a warehouse bin.</span></span> <span data-ttu-id="5fd2e-119">Til að búa til tengil á milli birgða og vöruhúss, verður þú að skilgreina aðlögun sjálfgefið hólf á staðsetningu.</span><span class="sxs-lookup"><span data-stu-id="5fd2e-119">To create a link between the inventory and the warehouse, you must define a default adjustment bin per location.</span></span>  
  
 <span data-ttu-id="5fd2e-120">Sjálfgefið leiðréttingarhólf skráir vörur í vöruhús þegar birgðaaukning er bókuð.</span><span class="sxs-lookup"><span data-stu-id="5fd2e-120">The default adjustment bin registers items in the warehouse when you post an increase for the inventory.</span></span> <span data-ttu-id="5fd2e-121">Hins vegar, ef þú bókar lækkun minnkar einnig magn í sjálfgefnu hólfi.</span><span class="sxs-lookup"><span data-stu-id="5fd2e-121">However, if you post a decrease, the quantity on the default bin is also decreased.</span></span> <span data-ttu-id="5fd2e-122">Í báðum tilvikum, eru birgðahöfuðbókarfærslur og vöruhúsafærslur stofnaðar.</span><span class="sxs-lookup"><span data-stu-id="5fd2e-122">In both cases, item ledger entries and warehouse entries are created.</span></span>  
  
> [!NOTE]  
>  <span data-ttu-id="5fd2e-123">Leiðréttingarhólfið er ekki innifalið í framboðsútreikningi.</span><span class="sxs-lookup"><span data-stu-id="5fd2e-123">The adjustment bin is not included in the availability calculation.</span></span>  
  
 <span data-ttu-id="5fd2e-124">Ef stilla á innihald hólfs er hægt að nota vöruhúsabirgðabókina þar sem hægt er að færa inn vörunúmer, svæðiskóða, hólfkóða og magn sem á að stilla.</span><span class="sxs-lookup"><span data-stu-id="5fd2e-124">If you want to adjust the bin content, you can use the warehouse item journal, from which you can enter the item number, zone code, bin code, and quantity that you want to adjust.</span></span>  
  
 <span data-ttu-id="5fd2e-125">Ef jákvætt magn er slegið inn og línan bókuð aukast birgðir sem geymdar eru í hólfinu og magnið í sjálfgefna leiðréttingarhólfinu minnkar að sama skapi.</span><span class="sxs-lookup"><span data-stu-id="5fd2e-125">If you enter a positive quantity and post the line, then the inventory stored in the bin increases, and the quantity of the default adjustment bin decreases correspondingly.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5fd2e-126">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="5fd2e-126">See Also</span></span>  
 <span data-ttu-id="5fd2e-127">[Hönnunarupplýsingar vöruhúsakerfi](design-details-warehouse-management.md) </span><span class="sxs-lookup"><span data-stu-id="5fd2e-127">[Design Details: Warehouse Management](design-details-warehouse-management.md) </span></span>  
 [<span data-ttu-id="5fd2e-128">Hönnunarupplýsingar: Framboð í vöruhúsi</span><span class="sxs-lookup"><span data-stu-id="5fd2e-128">Design Details: Availability in the Warehouse</span></span>](design-details-availability-in-the-warehouse.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]