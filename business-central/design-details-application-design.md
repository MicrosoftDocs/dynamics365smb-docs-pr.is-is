---
title: Hönnunarupplýsingar | Microsoft Docs
description: Þetta innihald inniheldur nákvæmar tæknilegar upplýsingar um flókin eiginleikasvæði í Business Central.
author: SorenGP
documentationcenter: ''
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/08/2021
ms.author: edupont
ms.openlocfilehash: df7ea4e62608d64763288b978d4ee48a103e8424
ms.sourcegitcommit: 0953171d39e1232a7c126142d68cac858234a20e
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/09/2021
ms.locfileid: "6215554"
---
# <a name="design-details"></a><span data-ttu-id="ecd5e-103">Hönnunarupplýsingar</span><span class="sxs-lookup"><span data-stu-id="ecd5e-103">Design Details</span></span>
<span data-ttu-id="ecd5e-104">Þetta innihald inniheldur nákvæmar tæknilegar upplýsingar um flókin eiginleikasvæði í [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="ecd5e-104">This content contains detailed technical information about complex application features in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>  

 <span data-ttu-id="ecd5e-105">Hönnunarupplýsingar er ætlað innleiðurum, hönnuðum og yfirnotendum sem þurfa dýpri innsýn til að innleiða, sérsníða, eða setja upp lögun svæði sem um ræðir.</span><span class="sxs-lookup"><span data-stu-id="ecd5e-105">Design details content is aimed at implementers, developers, and super users who need deeper insight to implement, customize, or set up the features in question.</span></span>  

|<span data-ttu-id="ecd5e-106">**Til að**</span><span class="sxs-lookup"><span data-stu-id="ecd5e-106">**To**</span></span>|<span data-ttu-id="ecd5e-107">**Sjá**</span><span class="sxs-lookup"><span data-stu-id="ecd5e-107">**See**</span></span>|  
|------------|-------------|  
|<span data-ttu-id="ecd5e-108">Lesið um hvernig áætlanakerfið virkar og hvernig á að leiðrétta reiknireglurnar til að uppfylla áætlunarþarfir í mismunandi umhverfi.</span><span class="sxs-lookup"><span data-stu-id="ecd5e-108">Learn how the planning system works and how to adjust the algorithms to meet planning requirements in different environments.</span></span>|[<span data-ttu-id="ecd5e-109">Hönnunarupplýsingar: framboðsáætlun</span><span class="sxs-lookup"><span data-stu-id="ecd5e-109">Design Details: Supply Planning</span></span>](design-details-supply-planning.md)|  
|<span data-ttu-id="ecd5e-110">Að skilja virkni kostnaðarforritsins, svo sem kostnaðaraðferð og kostnaðarleiðréttingu, og hvaða reikningsskilareglum sem þeir eru hannaðir fyrir.</span><span class="sxs-lookup"><span data-stu-id="ecd5e-110">Understand mechanisms in the costing engine, such as costing method and cost adjustment, and which accounting principles they are designed for.</span></span>|[<span data-ttu-id="ecd5e-111">Hönnunarupplýsingar: Birgðakostnaður</span><span class="sxs-lookup"><span data-stu-id="ecd5e-111">Design Details: Inventory Costing</span></span>](design-details-inventory-costing.md)|  
|<span data-ttu-id="ecd5e-112">Lesið um hugsunina á bak við ítarlega eiginleika og grunneiginleika vöruhúss og hvernig þeir falla að öðrum eiginleikum birgðakeðju.</span><span class="sxs-lookup"><span data-stu-id="ecd5e-112">Learn about central principles behind advanced and basic warehouse features and how they integrate with other supply chain features.</span></span>|[<span data-ttu-id="ecd5e-113">Hönnunarupplýsingar vöruhúsakerfi</span><span class="sxs-lookup"><span data-stu-id="ecd5e-113">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)|  
|<span data-ttu-id="ecd5e-114">Lesið um sögulega og núgildandi hönnun vörurakningareiginleikans og hvernig hann fellur að frátekningarkerfinu til að taka með rað-/lotunúmer í framboðsútreikninga.</span><span class="sxs-lookup"><span data-stu-id="ecd5e-114">Learn about historic and the current design of item tracking functionality and how it integrates with the reservation system to include serial/lot numbers in availability calculations.</span></span>|[<span data-ttu-id="ecd5e-115">Hönnunarupplýsingar: vörurakning</span><span class="sxs-lookup"><span data-stu-id="ecd5e-115">Design Details: Item Tracking</span></span>](design-details-item-tracking.md)|  
|<span data-ttu-id="ecd5e-116">Kynntu þér valkosti fyrir bókunarlínu færslubókar, þ.m.t. nýlegar breytingar á hönnun kóðaeiningar 12.</span><span class="sxs-lookup"><span data-stu-id="ecd5e-116">Learn about the General Journal Posting Line feature, including recent simplifications to the design of codeunit 12.</span></span>|[<span data-ttu-id="ecd5e-117">Hönnunarupplýsingar: Bókunarlína færslubókar</span><span class="sxs-lookup"><span data-stu-id="ecd5e-117">Design Details: General Journal Post Line</span></span>](design-details-general-journal-post-line.md)|
|<span data-ttu-id="ecd5e-118">Kynntu þér hönnunina fyrir vistun og bókun vídda, þ.m.t. kóðadæmi um hvernig eigi að flytja og uppfæra víddarkóða.</span><span class="sxs-lookup"><span data-stu-id="ecd5e-118">Learn about the design for storing and posting dimensions, including code examples on how to migrate and upgrade dimension code.</span></span>|[<span data-ttu-id="ecd5e-119">Hönnunarupplýsingar: Færslur víddarsamstæða</span><span class="sxs-lookup"><span data-stu-id="ecd5e-119">Design Details: Dimension Set Entries</span></span>](design-details-dimension-set-entries-overview.md)|

## <a name="see-also"></a><span data-ttu-id="ecd5e-120">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="ecd5e-120">See Also</span></span>

[<span data-ttu-id="ecd5e-121">Áætlun</span><span class="sxs-lookup"><span data-stu-id="ecd5e-121">Planning</span></span>](production-planning.md)  
[<span data-ttu-id="ecd5e-122">Birgðakostnaði stjórnað</span><span class="sxs-lookup"><span data-stu-id="ecd5e-122">Managing Inventory Costs</span></span>](finance-manage-inventory-costs.md)  
[<span data-ttu-id="ecd5e-123">Vöruhúsastjórnun</span><span class="sxs-lookup"><span data-stu-id="ecd5e-123">Warehouse Management</span></span>](warehouse-manage-warehouse.md)  
[<span data-ttu-id="ecd5e-124">Setja upp flókin notkunarsviðum með því að nota bestu venjur</span><span class="sxs-lookup"><span data-stu-id="ecd5e-124">Setting Up Complex Application Areas Using Best Practices</span></span>](set-up-complex-application-areas-using-best-practices.md)  
<span data-ttu-id="ecd5e-125">[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="ecd5e-125">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  
