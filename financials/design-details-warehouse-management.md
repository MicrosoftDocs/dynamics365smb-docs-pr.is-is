---
title: "Hönnunarupplýsingar - vöruhúsakerfi | Microsoft Docs"
description: "Þetta efnisatriði veitir yfirsýn yfir hönnunina, hugtökin og reglurnar á bak við eiginleika vöruhúsakerfisins í Finance and Operations, Business Edition."
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/23/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 3145c64e64274cefb19630b639879f09ead8a6f3
ms.contentlocale: is-is
ms.lasthandoff: 03/22/2018

---
# <a name="design-details-warehouse-management"></a><span data-ttu-id="df8c3-103">Hönnunarupplýsingar vöruhúsakerfi</span><span class="sxs-lookup"><span data-stu-id="df8c3-103">Design Details: Warehouse Management</span></span>
<span data-ttu-id="df8c3-104">Þessi fylgiskjöl veita yfirlit yfir hugtökin og reglurnar sem eru notaðar í valkostum Vöruhúsakerfa í [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="df8c3-104">This documentation gives an overview of the concepts and principles that are used in the Warehouse Management features in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="df8c3-105">Það útskýrir hönnun bak við helstu vörugeymsluaðgerðir og hvernig vörugeymslan vinnur með öðrum framboðskeðjuaðgerðum.</span><span class="sxs-lookup"><span data-stu-id="df8c3-105">It explains the design behind central warehouse features and how warehousing integrates with other supply chain features.</span></span>  

<span data-ttu-id="df8c3-106">Til að greina á milli mismunandi flækjustiga vörugeymsla, þetta Gögnunum er skipt í tvo almenna hópa, grunn og Ítarleg vöruhús, táknuð með kafla titla.</span><span class="sxs-lookup"><span data-stu-id="df8c3-106">To differentiate the different complexity levels of the warehousing, this documentation is divided into two general groups, Basic and Advanced warehouse configurations, indicated by section titles.</span></span> <span data-ttu-id="df8c3-107">Þessi einfalda aðgreining nær yfir mismunandi flækjustig samkvæmt skilgreiningu vörueinda og staðsetningaruppsetniingu.</span><span class="sxs-lookup"><span data-stu-id="df8c3-107">This simple differentiation covers different complexity levels as defined by product granules and location setup.</span></span> <span data-ttu-id="df8c3-108">Nánari upplýsingar eru í [Upplýsingar um hönnun: Uppsetning vöruhúss](design-details-warehouse-setup.md).</span><span class="sxs-lookup"><span data-stu-id="df8c3-108">For more information, see [Design Details: Warehouse Setup](design-details-warehouse-setup.md).</span></span>  

## <a name="in-this-section"></a><span data-ttu-id="df8c3-109">Í þessum hluta</span><span class="sxs-lookup"><span data-stu-id="df8c3-109">In This Section</span></span>  
[<span data-ttu-id="df8c3-110">Hönnunarupplýsingar yfirlit vöruhúss</span><span class="sxs-lookup"><span data-stu-id="df8c3-110">Design Details: Warehouse Overview</span></span>](design-details-warehouse-overview.md)  
[<span data-ttu-id="df8c3-111">Hönnunarupplýsingar uppsetningvöruhúss</span><span class="sxs-lookup"><span data-stu-id="df8c3-111">Design Details: Warehouse Setup</span></span>](design-details-warehouse-setup.md)  
[<span data-ttu-id="df8c3-112">Hönnunarupplýsingar: vöruhúsaflæði inn</span><span class="sxs-lookup"><span data-stu-id="df8c3-112">Design Details: Inbound Warehouse Flow</span></span>](design-details-inbound-warehouse-flow.md)  
[<span data-ttu-id="df8c3-113">Hönnunarupplýsingar: Innra vöruhúsaflæði</span><span class="sxs-lookup"><span data-stu-id="df8c3-113">Design Details: Internal Warehouse Flows</span></span>](design-details-internal-warehouse-flows.md)  
[<span data-ttu-id="df8c3-114">Hönnunarupplýsingar: Framboð í vöruhúsi</span><span class="sxs-lookup"><span data-stu-id="df8c3-114">Design Details: Availability in the Warehouse</span></span>](design-details-availability-in-the-warehouse.md)  
[<span data-ttu-id="df8c3-115">Hönnunarupplýsingar: vöruhúsaflæði á innleið</span><span class="sxs-lookup"><span data-stu-id="df8c3-115">Design Details: Outbound Warehouse Flow</span></span>](design-details-outbound-warehouse-flow.md)  
[<span data-ttu-id="df8c3-116">Hönnunarupplýsingar: Sameining með birgðum</span><span class="sxs-lookup"><span data-stu-id="df8c3-116">Design Details: Integration with Inventory</span></span>](design-details-integration-with-inventory.md)

