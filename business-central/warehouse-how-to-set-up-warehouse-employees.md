---
title: "Hvernig á að setja upp vöruhúsastarfsmenn | Microsoft Docs"
description: "Hver notandi sem framkvæmir vöruhúsaaðgerðir verður að vera settur upp sem starfsmaður sem hefur verið úthlutað einni sjálfgefinni birgðageymslu og hugsanlega fleiri staðsetningum sem ekki eru sjálfgefnar."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/23/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: ed9622aae938e4876fc9537702b8f43b84764950
ms.contentlocale: is-is
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-warehouse-employees"></a><span data-ttu-id="040e5-103">Setja upp vöruhúsastarfsmenn</span><span class="sxs-lookup"><span data-stu-id="040e5-103">Set Up Warehouse Employees</span></span>
<span data-ttu-id="040e5-104">Hver notandi sem framkvæmir vöruhúsaaðgerðir verður að vera settur upp sem starfsmaður sem hefur verið úthlutað einni sjálfgefinni birgðageymslu og hugsanlega fleiri staðsetningum sem ekki eru sjálfgefnar.</span><span class="sxs-lookup"><span data-stu-id="040e5-104">Each user who performs warehouse activities must be set up as a warehouse employee assigned to one default location and potentially more non-default locations.</span></span> <span data-ttu-id="040e5-105">Þessi notandauppsetning afmarkar allar vöruhúsaaðgerðir í gagnagrunninum við staðsetningu notandans svo hann geti einungis framkvæmt vöruhúsaaðgerðir í sjálfgefnu birgðageymslunni.</span><span class="sxs-lookup"><span data-stu-id="040e5-105">This user setup filters all warehouse activities across the database to the employee's location so that the employee can only perform the warehouse activities at the default location.</span></span> <span data-ttu-id="040e5-106">Hægt er að úthluta notanda fyrir birgðageymslur sem ekki eru sjálfgefnar sem hann getur skoðað aðgerðalínur fyrir en ekki framkvæmt aðgerðirnar.</span><span class="sxs-lookup"><span data-stu-id="040e5-106">A user can be assigned to additional non-default locations for which the employee can view activity lines but not perform the activities.</span></span>

## <a name="to-set-up-warehouse-employees"></a><span data-ttu-id="040e5-107">Setja upp vöruhúsastarfsmenn</span><span class="sxs-lookup"><span data-stu-id="040e5-107">To set up warehouse employees</span></span>  
1.  <span data-ttu-id="040e5-108">Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **starfsmenn vöruhúss** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="040e5-108">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Warehouse Employees**, and then choose the related link.</span></span>  
2. <span data-ttu-id="040e5-109">Valið er **Nýtt** aðgerð.</span><span class="sxs-lookup"><span data-stu-id="040e5-109">Choose the **New** action.</span></span>  
3. <span data-ttu-id="040e5-110">Veljið reitinn **Kenni notanda** og veljið síðan notandann sem á að bæta við sem vöruhúsastarfsmanni.</span><span class="sxs-lookup"><span data-stu-id="040e5-110">Select the **User ID** field, and then select the user to be added as a warehouse employee.</span></span> <span data-ttu-id="040e5-111">Velja hnappinn **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="040e5-111">Choose the **OK** button.</span></span>  
6.  <span data-ttu-id="040e5-112">Í reitnum **Kóti birgðageymslu** er færður inn kóti birgðageymslunnar þar sem notandinn verður starfandi.</span><span class="sxs-lookup"><span data-stu-id="040e5-112">In the **Location Code** field, enter the code of the location where the user will be working.</span></span>  
7.  <span data-ttu-id="040e5-113">Gátreiturinn **Sjálfgefið** er valinn til þess að skilgreina birgðageymsluna sem einu staðsetninguna þar sem starfsmaður getur framkvæmt vöruhúsaaðgerðir.</span><span class="sxs-lookup"><span data-stu-id="040e5-113">Select the **Default** check box to define the location as the only location where the employee can perform warehouse activities.</span></span>  
8.  <span data-ttu-id="040e5-114">Skrefin eru endurtekin til að úthluta öðrum starfsmönnum á birgðageymslur eða úthluta birgðageymslum sem ekki eru sjálfgefnar til vöruhúsastarfsmanna sem þegar eru til.</span><span class="sxs-lookup"><span data-stu-id="040e5-114">Repeat these steps to assign other employees to locations or assign non-default locations to existing warehouse employees.</span></span>  

## <a name="see-also"></a><span data-ttu-id="040e5-115">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="040e5-115">See Also</span></span>  
[<span data-ttu-id="040e5-116">Vöruhúsastjórnun</span><span class="sxs-lookup"><span data-stu-id="040e5-116">Warehouse Management</span></span>](warehouse-manage-warehouse.md)  
[<span data-ttu-id="040e5-117">Birgðir</span><span class="sxs-lookup"><span data-stu-id="040e5-117">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="040e5-118">[Vöruhúsastjórnun sett upp](warehouse-setup-warehouse.md)   </span><span class="sxs-lookup"><span data-stu-id="040e5-118">[Setting Up Warehouse Management](warehouse-setup-warehouse.md)   </span></span>  
<span data-ttu-id="040e5-119">[Samsetningardeild](assembly-assemble-items.md)  </span><span class="sxs-lookup"><span data-stu-id="040e5-119">[Assembly Management](assembly-assemble-items.md)  </span></span>  
[<span data-ttu-id="040e5-120">Hönnunarupplýsingar vöruhúsakerfi</span><span class="sxs-lookup"><span data-stu-id="040e5-120">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="040e5-121">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="040e5-121">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

