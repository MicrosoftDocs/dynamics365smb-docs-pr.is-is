---
title: Hvernig á að setja upp vöruhúsastarfsmenn | Microsoft Docs
description: Hver notandi sem framkvæmir vöruhúsaaðgerðir verður að vera settur upp sem starfsmaður sem hefur verið úthlutað einni sjálfgefinni birgðageymslu og hugsanlega fleiri staðsetningum sem ekki eru sjálfgefnar.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 7ebb81abd7e16e0c4aaa3f7cd52ab1b6f1a664c3
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/17/2020
ms.locfileid: "4755926"
---
# <a name="set-up-warehouse-employees"></a><span data-ttu-id="a2f7d-103">Setja upp vöruhúsastarfsmenn</span><span class="sxs-lookup"><span data-stu-id="a2f7d-103">Set Up Warehouse Employees</span></span>
<span data-ttu-id="a2f7d-104">Hver notandi sem framkvæmir vöruhúsaaðgerðir verður að vera settur upp sem starfsmaður sem hefur verið úthlutað einni sjálfgefinni birgðageymslu og hugsanlega fleiri staðsetningum sem ekki eru sjálfgefnar.</span><span class="sxs-lookup"><span data-stu-id="a2f7d-104">Each user who performs warehouse activities must be set up as a warehouse employee assigned to one default location and potentially more non-default locations.</span></span> <span data-ttu-id="a2f7d-105">Þessi notandauppsetning afmarkar allar vöruhúsaaðgerðir í gagnagrunninum við staðsetningu notandans svo hann geti einungis framkvæmt vöruhúsaaðgerðir í sjálfgefnu birgðageymslunni.</span><span class="sxs-lookup"><span data-stu-id="a2f7d-105">This user setup filters all warehouse activities across the database to the employee's location so that the employee can only perform the warehouse activities at the default location.</span></span> <span data-ttu-id="a2f7d-106">Hægt er að úthluta notanda fyrir birgðageymslur sem ekki eru sjálfgefnar sem hann getur skoðað aðgerðalínur fyrir en ekki framkvæmt aðgerðirnar.</span><span class="sxs-lookup"><span data-stu-id="a2f7d-106">A user can be assigned to additional non-default locations for which the employee can view activity lines but not perform the activities.</span></span>

## <a name="to-set-up-warehouse-employees"></a><span data-ttu-id="a2f7d-107">Setja upp vöruhúsastarfsmenn</span><span class="sxs-lookup"><span data-stu-id="a2f7d-107">To set up warehouse employees</span></span>  
1.  <span data-ttu-id="a2f7d-108">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Starfsmenn vöruhúss** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="a2f7d-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Warehouse Employees**, and then choose the related link.</span></span>  
2. <span data-ttu-id="a2f7d-109">Valið er **Nýtt** aðgerð.</span><span class="sxs-lookup"><span data-stu-id="a2f7d-109">Choose the **New** action.</span></span>  
3. <span data-ttu-id="a2f7d-110">Veljið reitinn **Kenni notanda** og veljið síðan notandann sem á að bæta við sem vöruhúsastarfsmanni.</span><span class="sxs-lookup"><span data-stu-id="a2f7d-110">Select the **User ID** field, and then select the user to be added as a warehouse employee.</span></span> <span data-ttu-id="a2f7d-111">Velja hnappinn **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="a2f7d-111">Choose the **OK** button.</span></span>  
6.  <span data-ttu-id="a2f7d-112">Í reitnum **Kóti birgðageymslu** er færður inn kóti birgðageymslunnar þar sem notandinn verður starfandi.</span><span class="sxs-lookup"><span data-stu-id="a2f7d-112">In the **Location Code** field, enter the code of the location where the user will be working.</span></span>  
7.  <span data-ttu-id="a2f7d-113">Gátreiturinn **Sjálfgefið** er valinn til þess að skilgreina birgðageymsluna sem einu staðsetninguna þar sem starfsmaður getur framkvæmt vöruhúsaaðgerðir.</span><span class="sxs-lookup"><span data-stu-id="a2f7d-113">Select the **Default** check box to define the location as the only location where the employee can perform warehouse activities.</span></span>  
8.  <span data-ttu-id="a2f7d-114">Skrefin eru endurtekin til að úthluta öðrum starfsmönnum á birgðageymslur eða úthluta birgðageymslum sem ekki eru sjálfgefnar til vöruhúsastarfsmanna sem þegar eru til.</span><span class="sxs-lookup"><span data-stu-id="a2f7d-114">Repeat these steps to assign other employees to locations or assign non-default locations to existing warehouse employees.</span></span>  

## <a name="see-also"></a><span data-ttu-id="a2f7d-115">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="a2f7d-115">See Also</span></span>  
[<span data-ttu-id="a2f7d-116">Vöruhúsastjórnun</span><span class="sxs-lookup"><span data-stu-id="a2f7d-116">Warehouse Management</span></span>](warehouse-manage-warehouse.md)  
[<span data-ttu-id="a2f7d-117">Birgðir</span><span class="sxs-lookup"><span data-stu-id="a2f7d-117">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="a2f7d-118">[Vöruhúsastjórnun sett upp](warehouse-setup-warehouse.md)   </span><span class="sxs-lookup"><span data-stu-id="a2f7d-118">[Setting Up Warehouse Management](warehouse-setup-warehouse.md)   </span></span>  
<span data-ttu-id="a2f7d-119">[Samsetningardeild](assembly-assemble-items.md)  </span><span class="sxs-lookup"><span data-stu-id="a2f7d-119">[Assembly Management](assembly-assemble-items.md)  </span></span>  
[<span data-ttu-id="a2f7d-120">Hönnunarupplýsingar vöruhúsakerfi</span><span class="sxs-lookup"><span data-stu-id="a2f7d-120">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="a2f7d-121">[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="a2f7d-121">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  
