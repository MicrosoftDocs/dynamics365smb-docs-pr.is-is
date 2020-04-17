---
title: Hönnunarupplýsingar | Microsoft Docs
description: Þetta innihald inniheldur nákvæmar tæknilegar upplýsingar um flókin eiginleikasvæði í Business Central.
author: SorenGP
documentationcenter: ''
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: b68d9de15af8b0f8943acb3a8a06cf4d3872291e
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2020
ms.locfileid: "3185829"
---
# <a name="design-details"></a><span data-ttu-id="d9c48-103">Hönnunarupplýsingar</span><span class="sxs-lookup"><span data-stu-id="d9c48-103">Design Details</span></span>
<span data-ttu-id="d9c48-104">Þetta innihald inniheldur nákvæmar tæknilegar upplýsingar um flókin eiginleikasvæði í [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="d9c48-104">This content contains detailed technical information about complex application features in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  

 <span data-ttu-id="d9c48-105">Hönnunarupplýsingar er ætlað innleiðurum, hönnuðum og yfirnotendum sem þurfa dýpri innsýn til að innleiða, sérsníða, eða setja upp lögun svæði sem um ræðir.</span><span class="sxs-lookup"><span data-stu-id="d9c48-105">Design details content is aimed at implementers, developers, and super users who need deeper insight to implement, customize, or set up the features in question.</span></span>  

|<span data-ttu-id="d9c48-106">**Til að**</span><span class="sxs-lookup"><span data-stu-id="d9c48-106">**To**</span></span>|<span data-ttu-id="d9c48-107">**Sjá**</span><span class="sxs-lookup"><span data-stu-id="d9c48-107">**See**</span></span>|  
|------------|-------------|  
|<span data-ttu-id="d9c48-108">Lesið um hvernig áætlanakerfið virkar og hvernig á að leiðrétta reiknireglurnar til að uppfylla áætlunarþarfir í mismunandi umhverfi.</span><span class="sxs-lookup"><span data-stu-id="d9c48-108">Learn how the planning system works and how to adjust the algorithms to meet planning requirements in different environments.</span></span>|[<span data-ttu-id="d9c48-109">Hönnunarupplýsingar: framboðsáætlun</span><span class="sxs-lookup"><span data-stu-id="d9c48-109">Design Details: Supply Planning</span></span>](design-details-supply-planning.md)|  
|<span data-ttu-id="d9c48-110">Að skilja virkni kostnaðarforritsins, svo sem kostnaðaraðferð og kostnaðarleiðréttingu, og hvaða reikningsskilareglum sem þeir eru hannaðir fyrir.</span><span class="sxs-lookup"><span data-stu-id="d9c48-110">Understand mechanisms in the costing engine, such as costing method and cost adjustment, and which accounting principles they are designed for.</span></span>|[<span data-ttu-id="d9c48-111">Hönnunarupplýsingar: Birgðakostnaður</span><span class="sxs-lookup"><span data-stu-id="d9c48-111">Design Details: Inventory Costing</span></span>](design-details-inventory-costing.md)|  
|<span data-ttu-id="d9c48-112">Lesið um hugsunina á bak við ítarlega eiginleika og grunneiginleika vöruhúss og hvernig þeir falla að öðrum eiginleikum birgðakeðju.</span><span class="sxs-lookup"><span data-stu-id="d9c48-112">Learn about central principles behind advanced and basic warehouse features and how they integrate with other supply chain features.</span></span>|[<span data-ttu-id="d9c48-113">Hönnunarupplýsingar vöruhúsakerfi</span><span class="sxs-lookup"><span data-stu-id="d9c48-113">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)|  
|<span data-ttu-id="d9c48-114">Lesið um sögulega og núgildandi hönnun vörurakningareiginleikans og hvernig hann fellur að frátekningarkerfinu til að taka með rað-/lotunúmer í framboðsútreikninga.</span><span class="sxs-lookup"><span data-stu-id="d9c48-114">Learn about historic and the current design of item tracking functionality and how it integrates with the reservation system to include serial/lot numbers in availability calculations.</span></span>|[<span data-ttu-id="d9c48-115">Hönnunarupplýsingar: vörurakning</span><span class="sxs-lookup"><span data-stu-id="d9c48-115">Design Details: Item Tracking</span></span>](design-details-item-tracking.md)|  
|<span data-ttu-id="d9c48-116">Kynntu þér valkosti fyrir bókunarlínu færslubókar, þ.m.t. nýlegar breytingar á hönnun kóðaeiningar 12.</span><span class="sxs-lookup"><span data-stu-id="d9c48-116">Learn about the General Journal Posting Line feature, including recent simplifications to the design of codeunit 12.</span></span>|[<span data-ttu-id="d9c48-117">Hönnunarupplýsingar: Bókunarlína færslubókar</span><span class="sxs-lookup"><span data-stu-id="d9c48-117">Design Details: General Journal Post Line</span></span>](design-details-general-journal-post-line.md)|
|<span data-ttu-id="d9c48-118">Kynntu þér hönnunina fyrir vistun og bókun vídda, þ.m.t. kóðadæmi um hvernig eigi að flytja og uppfæra víddarkóða.</span><span class="sxs-lookup"><span data-stu-id="d9c48-118">Learn about the design for storing and posting dimensions, including code examples on how to migrate and upgrade dimension code.</span></span>|[<span data-ttu-id="d9c48-119">Hönnunarupplýsingar: Færslur víddarsamstæða</span><span class="sxs-lookup"><span data-stu-id="d9c48-119">Design Details: Dimension Set Entries</span></span>](design-details-dimension-set-entries.md)| 

## <a name="see-also"></a><span data-ttu-id="d9c48-120">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="d9c48-120">See Also</span></span>  
 <span data-ttu-id="d9c48-121">[Áætlun](production-planning.md) </span><span class="sxs-lookup"><span data-stu-id="d9c48-121">[Planning](production-planning.md) </span></span>  
 <span data-ttu-id="d9c48-122">[Birgðakostnaði stjórnað](finance-manage-inventory-costs.md) </span><span class="sxs-lookup"><span data-stu-id="d9c48-122">[Managing Inventory Costs](finance-manage-inventory-costs.md) </span></span>  
 <span data-ttu-id="d9c48-123">[Vöruhúsastjórnun](warehouse-manage-warehouse.md) </span><span class="sxs-lookup"><span data-stu-id="d9c48-123">[Warehouse Management](warehouse-manage-warehouse.md) </span></span>  
 [<span data-ttu-id="d9c48-124">Setja upp flókin notkunarsviðum með því að nota bestu venjur</span><span class="sxs-lookup"><span data-stu-id="d9c48-124">Setting Up Complex Application Areas Using Best Practices</span></span>](set-up-complex-application-areas-using-best-practices.md)  
 <span data-ttu-id="d9c48-125">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="d9c48-125">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

 ## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
