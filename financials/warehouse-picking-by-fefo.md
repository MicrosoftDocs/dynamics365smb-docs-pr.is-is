---
title: "Hvernig ska virkja tínslu eftir FEFO | Microsoft Docs"
description: "Fyrst-fyrnt-fyrst-út (FEFO) er röðunaraðferð sem tryggir að elstu vörurnar, sem hafa elstu lokadagsetningarnar, eru tíndar fyrst."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: cc45bf06ab5d12cf393d48b7b1c295db28f56b3b
ms.contentlocale: is-is
ms.lasthandoff: 01/30/2018

---
# <a name="enable-picking-items-by-fefo"></a><span data-ttu-id="f9019-103">Virkja Vörutínsla eftir FEFO</span><span class="sxs-lookup"><span data-stu-id="f9019-103">Enable Picking Items by FEFO</span></span>
<span data-ttu-id="f9019-104">Fyrst-fyrnt-fyrst-út (FEFO) er röðunaraðferð sem tryggir að elstu vörurnar, sem hafa elstu lokadagsetningarnar, eru tíndar fyrst.</span><span class="sxs-lookup"><span data-stu-id="f9019-104">First-Expired-First-Out (FEFO) is a sorting method that ensures that the oldest items, those with the earliest expiration dates, are picked first.</span></span>  

 <span data-ttu-id="f9019-105">Þessi aðgerð virkar aðeins ef eftirfarandi skilyrði eru uppfyllt:</span><span class="sxs-lookup"><span data-stu-id="f9019-105">This functionality only works when the following criteria are met:</span></span>  

-   <span data-ttu-id="f9019-106">Varan verður að hafa rað-/lotunúmer.</span><span class="sxs-lookup"><span data-stu-id="f9019-106">The item must have a serial/lot number.</span></span>  
-   <span data-ttu-id="f9019-107">Í vörurakningarkótauppsetningu vörunnar verður að velja reitinn **Vöruhúsarakning bundin við raðnúmer** eða reitinn **Vöruhúsarakning bundin við lotnúmer**.</span><span class="sxs-lookup"><span data-stu-id="f9019-107">On the item’s item tracking code setup, the **SN-Specific Warehouse Tracking** field or the **Lot-Specific Warehouse Tracking** field must be selected.</span></span>  
-   <span data-ttu-id="f9019-108">Vöruna þarf að bóka á birgðir með lokadegi.</span><span class="sxs-lookup"><span data-stu-id="f9019-108">The item must be posted to inventory with an expiration date.</span></span>  
-   <span data-ttu-id="f9019-109">Á birgðageymsluspjaldinu verður reiturinn **Krefjast tínslu** að vera valinn.</span><span class="sxs-lookup"><span data-stu-id="f9019-109">On the location card, the **Require Pick** check box must be selected.</span></span>  
-   <span data-ttu-id="f9019-110">Á birgðageymsluspjaldinu verður gátreiturinn **Tína eftir FEFO** að vera valinn.</span><span class="sxs-lookup"><span data-stu-id="f9019-110">On the location card, the **Pick According to FEFO** check box must be selected.</span></span>  
-   <span data-ttu-id="f9019-111">Á birgðageymsluspjaldinu þarf að velja gátreitinn **Hólf áskilið**.</span><span class="sxs-lookup"><span data-stu-id="f9019-111">On the location card, the **Bin Mandatory** check box must be selected.</span></span>  

 <span data-ttu-id="f9019-112">Þegar öll skilyrðin eru uppfyllt er rað-/lotunúmerum til tínslu raðað með þá elstu fyrst í öllum tínslum og hreyfingum, fyrir utan vörur sem nota raðnúmers- eða lotubundna rakningu.</span><span class="sxs-lookup"><span data-stu-id="f9019-112">When all the criteria are met, then serial/lot-numbered items to be picked are sorted with the oldest first in all picks and movements, except for items that use SN-specific or lot-specific tracking.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="f9019-113">Ef einhverjar vörur með rað-/lotunúmerum nota sértæka rakningu er fyrst tekið tillit til þeirra og undir þeim birtast eftirstandandi ósértak rað-/lotunúmer eftir FEFO.</span><span class="sxs-lookup"><span data-stu-id="f9019-113">If some serial/lot-numbered items use specific tracking, then those are respected first and under them, the remaining, non-specific, serial/lot numbers are listed according to FEFO.</span></span>  

 <span data-ttu-id="f9019-114">Ef tvær vörur með rað-/lotunúmeri hafa sömu fyrningadagsetningu velur kerfið vöruna með lægsta lotu- eða raðnúmerið.</span><span class="sxs-lookup"><span data-stu-id="f9019-114">If two serial/lot-numbered items have the same expiration date, then the program selects the item with the lowest serial or lot number.</span></span> <span data-ttu-id="f9019-115">Ef rað- eða lotunúmerin eru þær sömu þá velur forritið þá vöru sem fyrst var skráð.</span><span class="sxs-lookup"><span data-stu-id="f9019-115">If the serial or lot numbers are the same, then the program selects the item that was registered first.</span></span>  

> [!NOTE]  
>  -   <span data-ttu-id="f9019-116">Þegar vörur með rað-/lotunúmeri eru tíndar í birgðageymslum sem settar eru upp fyrir beinan frágang og tínslu er einungis magn í hólfum af tegundinni *Tínsla* tínt samkvæmt FEFO.</span><span class="sxs-lookup"><span data-stu-id="f9019-116">When picking serial/lot-numbered items in locations set up for directed put-away and pick, only quantities on bins of type *Pick* are picked according to FEFO.</span></span>  
> -   <span data-ttu-id="f9019-117">Til að virkja hreyfingar samkvæmt FEFO, annaðhvort í glugganum **Birgðahreyfing** eða **Vinnublað hreyfingar** verður að skilja reitinn **Frá-hólf** eftir auðan.</span><span class="sxs-lookup"><span data-stu-id="f9019-117">To enable movements according to FEFO, either in the **Inventory Movement** window or the **Movement Worksheet** window, you must leave the **From Bin** field empty.</span></span>  
> -   <span data-ttu-id="f9019-118">Ef reiturinn **Ströng lokasöludagsetning** er valinn. munu aðeins vörur sem ekki eru útrunnar verða teknar með í tínslunni.</span><span class="sxs-lookup"><span data-stu-id="f9019-118">If the **Strict Expiration Posting** field is selected, then only items that are not expired will be included in the pick.</span></span> <span data-ttu-id="f9019-119">Þetta gildir jafnvel þó Tínsla sé ekki notuð samkvæmt FEFO.</span><span class="sxs-lookup"><span data-stu-id="f9019-119">This applies even if you are not using Pick according to FEFO.</span></span>  

## <a name="see-also"></a><span data-ttu-id="f9019-120">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="f9019-120">See Also</span></span>  
<span data-ttu-id="f9019-121">[Vörutínsla](warehouse-pick-items.md) </span><span class="sxs-lookup"><span data-stu-id="f9019-121">[Picking Items](warehouse-pick-items.md) </span></span>  
<span data-ttu-id="f9019-122">[Tína vörur fyrir vöruhúsaafhendingu](warehouse-how-to-pick-items-for-warehouse-shipment.md) </span><span class="sxs-lookup"><span data-stu-id="f9019-122">[Pick Items for Warehouse Shipment](warehouse-how-to-pick-items-for-warehouse-shipment.md) </span></span>  
<span data-ttu-id="f9019-123">[Vörur tíndar með birgðatínslu](warehouse-how-to-pick-items-with-inventory-picks.md) </span><span class="sxs-lookup"><span data-stu-id="f9019-123">[Pick Items with Inventory Picks](warehouse-how-to-pick-items-with-inventory-picks.md) </span></span>  
[<span data-ttu-id="f9019-124">Hönnunarupplýsingar vöruhúsakerfi</span><span class="sxs-lookup"><span data-stu-id="f9019-124">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
[<span data-ttu-id="f9019-125">Birgðir</span><span class="sxs-lookup"><span data-stu-id="f9019-125">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="f9019-126">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="f9019-126">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

