---
title: "Stofna nýjar virðisfærslur fyrir vörur í birgðum| Microsoft Docs"
description: "Lýsir því hvernig skal auka eða rýra virðisfærslur einnar eða fleiri vara í birgðum með því að bóka núgildandi og útreiknað virði þeirra."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: costing, inventory cost, value entries
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: d4111c5e1e496b2b47afed2d37533707f1c99a89
ms.contentlocale: is-is
ms.lasthandoff: 09/28/2018

---
# <a name="revalue-inventory"></a><span data-ttu-id="bf25d-103">Endurmat birgða</span><span class="sxs-lookup"><span data-stu-id="bf25d-103">Revalue Inventory</span></span>
<span data-ttu-id="bf25d-104">Ef endurmeta á til hækkunar eða lækkunar birgðavirði vöru eða tiltekinnar færslu vegna vöru verður að nota endurmatsbókina.</span><span class="sxs-lookup"><span data-stu-id="bf25d-104">If you want to appreciate or depreciate an item or a specific item ledger entry, you must use the revaluation journal.</span></span>

## <a name="to-revalue-inventory"></a><span data-ttu-id="bf25d-105">Að endurmeta birgðir</span><span class="sxs-lookup"><span data-stu-id="bf25d-105">To revalue inventory</span></span>
1. <span data-ttu-id="bf25d-106">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Endurmatsbók** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="bf25d-106">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Revaluation Journal**, and then choose the related link.</span></span>
2. <span data-ttu-id="bf25d-107">Veljið aðgerðina **Reikna út birgðavirði**.</span><span class="sxs-lookup"><span data-stu-id="bf25d-107">Choose the **Calculate Inventory Value** action.</span></span>
3. <span data-ttu-id="bf25d-108">Í glugganum **Reikna út birgðavirði** þarf að fylla reitina út eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="bf25d-108">In the **Calculate Inventory Value** window, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. <span data-ttu-id="bf25d-109">Velja hnappinn **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="bf25d-109">Choose the **OK** button.</span></span>
5. <span data-ttu-id="bf25d-110">Í hverri línu í glugganum **Endurmatsbók** skal færa inn nýtt kostnaðarverð í reitinn **Kostnaðarverð (endurmetið)**.</span><span class="sxs-lookup"><span data-stu-id="bf25d-110">On each line in the **Revaluation Journal** window, in the **Unit Cost (Revalued)** field, enter the new unit cost.</span></span> <span data-ttu-id="bf25d-111">Einnig er hægt að færa inn nýja samtölu í reitinn **Birgðavirði (endurmetið)**.</span><span class="sxs-lookup"><span data-stu-id="bf25d-111">Alternatively, enter the new total amount in the **Inventory Value (Revalued)** field.</span></span>

    <span data-ttu-id="bf25d-112">Viðeigandi reitir eru uppfærðir sjálfkrafa.</span><span class="sxs-lookup"><span data-stu-id="bf25d-112">The relevant fields are automatically updated.</span></span> <span data-ttu-id="bf25d-113">Bent er á að í reitnum **Upphæð** er sýnd breytingin í birgðavirði valinnar birgðafærslu.</span><span class="sxs-lookup"><span data-stu-id="bf25d-113">Note that the **Amount** field shows the actual change in inventory value for the selected item ledger entry.</span></span> <span data-ttu-id="bf25d-114">Þar er reiknaður út munurinn á reitunum **Birgðavirði (útreiknað)** og **Birgðavirði (endurmetið)**.</span><span class="sxs-lookup"><span data-stu-id="bf25d-114">It calculates the difference between the **Inventory Value (Calculated)** field and the **Inventory Value (Revalued)** field.</span></span>
6. <span data-ttu-id="bf25d-115">Þegar öllum línunum í endurmatsbókinni er lokið skal velja aðgerðina **Bóka**.</span><span class="sxs-lookup"><span data-stu-id="bf25d-115">When you have completed all lines in the revaluation journal, choose the **Post** action.</span></span>

<span data-ttu-id="bf25d-116">Nýjar færslur eru nú stofnaðar til að endurspegla endurmöt sem bókuð hafa verið.</span><span class="sxs-lookup"><span data-stu-id="bf25d-116">New value entries are now created to reflect the revaluations that you have posted.</span></span> <span data-ttu-id="bf25d-117">Hægt er að skoða ný gildi á viðkomandi birgðaspjaldi.</span><span class="sxs-lookup"><span data-stu-id="bf25d-117">You can see the new values on the respective item cards.</span></span>

## <a name="see-also"></a><span data-ttu-id="bf25d-118">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="bf25d-118">See Also</span></span>
[<span data-ttu-id="bf25d-119">Hönnunarupplýsingar: Endurmat</span><span class="sxs-lookup"><span data-stu-id="bf25d-119">Design Details: Revaluation</span></span>](design-details-revaluation.md)  
[<span data-ttu-id="bf25d-120">Birgðir</span><span class="sxs-lookup"><span data-stu-id="bf25d-120">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="bf25d-121">Sala</span><span class="sxs-lookup"><span data-stu-id="bf25d-121">Sales</span></span>](sales-manage-sales.md)  
[<span data-ttu-id="bf25d-122">Innkaup</span><span class="sxs-lookup"><span data-stu-id="bf25d-122">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="bf25d-123">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="bf25d-123">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

