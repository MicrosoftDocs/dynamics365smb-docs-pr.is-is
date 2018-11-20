---
title: "Hönnunarupplýsingar: Takast á við pantanir fyrir upphafsdag | Microsoft Docs"
description: "Þetta efni lýsir reglunum sem áætlanagerð gildir um pantanir í frystum svæðum."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: planning, frozen, design serial, lot
ms.date: 10/01/2018
ms.author: sgroespe
redirect_url: design-details-balancing-demand-and-supply
ms.translationtype: HT
ms.sourcegitcommit: 67400e424305cc705db5c1bd52a8e4de17ecc5a9
ms.openlocfilehash: 9fee9eff60b441ef2d4782a77a6fbbbe8b01af03
ms.contentlocale: is-is
ms.lasthandoff: 11/20/2018

---
# <a name="design-details-dealing-with-orders-before-the-planning-starting-date"></a><span data-ttu-id="0903b-103">Hönnunarupplýsingar: Takast á við pantanir fyrir upphafsdag</span><span class="sxs-lookup"><span data-stu-id="0903b-103">Design Details: Dealing with Orders Before the Planning Starting Date</span></span>
<span data-ttu-id="0903b-104">Til að forðast að framboðsáætlun sýnir ómögulegt og því gagnslaus tillögur, vinnur áætlanakerfið tímabilið allt til áætlanagerðarupphafsdags sem fryst svæði þar sem ekkert er áætlað fyrir.</span><span class="sxs-lookup"><span data-stu-id="0903b-104">To avoid that a supply plan shows impossible and therefore useless suggestions, the planning system regards the period up until the planning starting date a frozen zone where nothing is planned for.</span></span> <span data-ttu-id="0903b-105">Eftirfarandi regla gildir um fryst svæði:</span><span class="sxs-lookup"><span data-stu-id="0903b-105">The following rule applies to the frozen zone:</span></span>  

<span data-ttu-id="0903b-106">Allt framboð og eftirspurn fyrir upphafsdagsetningu áætlunartímabilsins verður talin hluti af birgðum eða afhent.</span><span class="sxs-lookup"><span data-stu-id="0903b-106">All supply and demand before the starting date of the planning period will be considered a part of inventory or shipped.</span></span>  

<span data-ttu-id="0903b-107">Í samræmi mun áætlanakerfið ekki, með nokkrum undantekningum, stinga upp á breytingum á framboðspöntunum á frystu svæði og engir pöntunarrakningartenglar eru stofnaðir eða viðhaldið fyrir það tímabil.</span><span class="sxs-lookup"><span data-stu-id="0903b-107">Accordingly, the planning system will not, with a few exceptions, suggest any changes to supply orders in the frozen zone, and no order tracking links are created or maintained for that period.</span></span>  

<span data-ttu-id="0903b-108">Undantekningar frá þessari reglu eru sem hér segir:</span><span class="sxs-lookup"><span data-stu-id="0903b-108">The exceptions to this rule are as follows:</span></span>  

* <span data-ttu-id="0903b-109">Ef áætlaðar tiltækar birgðir, þar með talin summa framboðs og eftirspurnar á frysta svæðinu, eru undir núlli.</span><span class="sxs-lookup"><span data-stu-id="0903b-109">If the projected available inventory, including the sum of supply and demand in the frozen zone, is below zero.</span></span>  
* <span data-ttu-id="0903b-110">Ef raðnúmer/lotunúmer þarf á bakfærða pöntun/pantanir.</span><span class="sxs-lookup"><span data-stu-id="0903b-110">If serial/lot numbers are required on the backdated order(s).</span></span>  
* <span data-ttu-id="0903b-111">Ef samstæðan framboð-eftirspurn er tengd með pöntun-fyrir-pöntun stefnu.</span><span class="sxs-lookup"><span data-stu-id="0903b-111">If the supply-demand set is linked by an order-to-order policy.</span></span>  

<span data-ttu-id="0903b-112">Ef fyrstu tiltæku birgðir eru undir núlli leggur áætlanakerfið til neyðarbirgðapöntun daginn fyrir áætlunartímabilið til að ná yfir magnið sem vantar.</span><span class="sxs-lookup"><span data-stu-id="0903b-112">If the initial available inventory is below zero, the planning system suggests an emergency supply order on the day before the planning period to cover the missing quantity.</span></span> <span data-ttu-id="0903b-113">Þar af leiðandi verða áætlaðar og tiltækar birgðir alltaf minnst núll þegar áætlun fyrir komandi tímabil hefst.</span><span class="sxs-lookup"><span data-stu-id="0903b-113">Consequently, the projected and available inventory will always be at least zero when planning for the future period begins.</span></span> <span data-ttu-id="0903b-114">Áætlunarlína fyrir þessa birgðapöntun birtir viðvörunartákn og viðbótarupplýsingar birtast við uppflettingu.</span><span class="sxs-lookup"><span data-stu-id="0903b-114">The planning line for this supply order will display an Emergency warning icon and additional information is provided upon lookup.</span></span>  

## <a name="seriallot-numbers-and-order-to-order-links-are-exempt-from-the-frozen-zone"></a><span data-ttu-id="0903b-115">Rað/Lotunúmer og pöntun fyrir pöntun tenglar eru undanþegin frosna reiturum</span><span class="sxs-lookup"><span data-stu-id="0903b-115">Serial/Lot Numbers and Order-to-Order Links are Exempt from the Frozen Zone</span></span>  
<span data-ttu-id="0903b-116">Ef raðnúmer/lotunúmer þarf eða pöntun-í-pöntun tengill er til staðar hunsar áætlanakerfið frysta svæðið og skráir magn sem er bakfært frá upphafsdegi og leggur mögulega til aðgerðir til úrbóta ef framboð og eftirspurn eru ekki samstillt.</span><span class="sxs-lookup"><span data-stu-id="0903b-116">If serial/lot numbers are required or an order-to-order link exists, the planning system will disregard the frozen zone and incorporate such quantities that are back-dated from the starting date and potentially suggest corrective actions if demand and supply is not synchronized.</span></span> <span data-ttu-id="0903b-117">Viðskiptaástæðan fyrir þessari stefnu er að slík sérstök pör eftirspurnar og framboðs verða að passa til að tryggja að þessi tiltekna eftirspurn sé uppfyllt.</span><span class="sxs-lookup"><span data-stu-id="0903b-117">The business reason for this principle is that such specific demand-supply sets must match to ensure that this specific demand is fulfilled.</span></span>  

## <a name="see-also"></a><span data-ttu-id="0903b-118">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="0903b-118">See Also</span></span>  
<span data-ttu-id="0903b-119">[Hönnunarupplýsingar: Jöfnun eftirspurnar og framboðs](design-details-balancing-demand-and-supply.md) </span><span class="sxs-lookup"><span data-stu-id="0903b-119">[Design Details: Balancing Demand and Supply](design-details-balancing-demand-and-supply.md) </span></span>  
<span data-ttu-id="0903b-120">[Hönnunarupplýsingar: Miðlægar hugmyndir áætlanakerfisins](design-details-central-concepts-of-the-planning-system.md) </span><span class="sxs-lookup"><span data-stu-id="0903b-120">[Design Details: Central Concepts of the Planning System](design-details-central-concepts-of-the-planning-system.md) </span></span>  
[<span data-ttu-id="0903b-121">Hönnunarupplýsingar: framboðsáætlun</span><span class="sxs-lookup"><span data-stu-id="0903b-121">Design Details: Supply Planning</span></span>](design-details-supply-planning.md)

