---
title: Stofna nýjar virðisfærslur fyrir vörur í birgðum| Microsoft Docs
description: Lýsir því hvernig skal auka eða rýra virðisfærslur einnar eða fleiri vara í birgðum með því að bóka núgildandi og útreiknað virði þeirra.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: costing, inventory cost, value entries
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 2bcd09876f18bb948e060b06199d3d36facaa83f
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/17/2020
ms.locfileid: "4750056"
---
# <a name="revalue-inventory"></a><span data-ttu-id="cfa31-103">Endurmat birgða</span><span class="sxs-lookup"><span data-stu-id="cfa31-103">Revalue Inventory</span></span>
<span data-ttu-id="cfa31-104">Ef endurmeta á til hækkunar eða lækkunar birgðavirði vöru eða tiltekinnar færslu vegna vöru verður að nota endurmatsbókina.</span><span class="sxs-lookup"><span data-stu-id="cfa31-104">If you want to appreciate or depreciate an item or a specific item ledger entry, you must use the revaluation journal.</span></span>

## <a name="to-revalue-inventory"></a><span data-ttu-id="cfa31-105">Að endurmeta birgðir</span><span class="sxs-lookup"><span data-stu-id="cfa31-105">To revalue inventory</span></span>
1. <span data-ttu-id="cfa31-106">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Endurmatsbók** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="cfa31-106">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Revaluation Journal**, and then choose the related link.</span></span>
2. <span data-ttu-id="cfa31-107">Veljið aðgerðina **Reikna út birgðavirði**.</span><span class="sxs-lookup"><span data-stu-id="cfa31-107">Choose the **Calculate Inventory Value** action.</span></span>
3. <span data-ttu-id="cfa31-108">Á síðunni **Reikna út birgðavirði** þarf að fylla reitina út eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="cfa31-108">On the **Calculate Inventory Value** page, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. <span data-ttu-id="cfa31-109">Velja hnappinn **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="cfa31-109">Choose the **OK** button.</span></span>
5. <span data-ttu-id="cfa31-110">Á síðunni **Endurmatsbók** í reitnum **Kostnaðarverð (Endurmetið)** er fært inn nýja kostnaðarverðið.</span><span class="sxs-lookup"><span data-stu-id="cfa31-110">On each line on the **Revaluation Journal** page, in the **Unit Cost (Revalued)** field, enter the new unit cost.</span></span> <span data-ttu-id="cfa31-111">Einnig er hægt að færa inn nýja samtölu í reitinn **Birgðavirði (endurmetið)**.</span><span class="sxs-lookup"><span data-stu-id="cfa31-111">Alternatively, enter the new total amount in the **Inventory Value (Revalued)** field.</span></span>

    <span data-ttu-id="cfa31-112">Viðeigandi reitir eru uppfærðir sjálfkrafa.</span><span class="sxs-lookup"><span data-stu-id="cfa31-112">The relevant fields are automatically updated.</span></span> <span data-ttu-id="cfa31-113">Bent er á að í reitnum **Upphæð** er sýnd breytingin í birgðavirði valinnar birgðafærslu.</span><span class="sxs-lookup"><span data-stu-id="cfa31-113">Note that the **Amount** field shows the actual change in inventory value for the selected item ledger entry.</span></span> <span data-ttu-id="cfa31-114">Þar er reiknaður út munurinn á reitunum **Birgðavirði (útreiknað)** og **Birgðavirði (endurmetið)**.</span><span class="sxs-lookup"><span data-stu-id="cfa31-114">It calculates the difference between the **Inventory Value (Calculated)** field and the **Inventory Value (Revalued)** field.</span></span>
6. <span data-ttu-id="cfa31-115">Þegar öllum línunum í endurmatsbókinni er lokið skal velja aðgerðina **Bóka**.</span><span class="sxs-lookup"><span data-stu-id="cfa31-115">When you have completed all lines in the revaluation journal, choose the **Post** action.</span></span>

<span data-ttu-id="cfa31-116">Nýjar færslur eru nú stofnaðar til að endurspegla endurmöt sem bókuð hafa verið.</span><span class="sxs-lookup"><span data-stu-id="cfa31-116">New value entries are now created to reflect the revaluations that you have posted.</span></span> <span data-ttu-id="cfa31-117">Hægt er að skoða ný gildi á viðkomandi birgðaspjaldi.</span><span class="sxs-lookup"><span data-stu-id="cfa31-117">You can see the new values on the respective item cards.</span></span>

## <a name="see-also"></a><span data-ttu-id="cfa31-118">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="cfa31-118">See Also</span></span>
[<span data-ttu-id="cfa31-119">Hönnunarupplýsingar: Endurmat</span><span class="sxs-lookup"><span data-stu-id="cfa31-119">Design Details: Revaluation</span></span>](design-details-revaluation.md)  
[<span data-ttu-id="cfa31-120">Birgðir</span><span class="sxs-lookup"><span data-stu-id="cfa31-120">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="cfa31-121">Sala</span><span class="sxs-lookup"><span data-stu-id="cfa31-121">Sales</span></span>](sales-manage-sales.md)  
[<span data-ttu-id="cfa31-122">Innkaup</span><span class="sxs-lookup"><span data-stu-id="cfa31-122">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="cfa31-123">[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="cfa31-123">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>
