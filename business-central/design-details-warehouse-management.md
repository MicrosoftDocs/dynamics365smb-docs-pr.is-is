---
title: Hönnunarupplýsingar - vöruhúsakerfi | Microsoft Docs
description: Þetta efnisatriði veitir yfirsýn yfir hönnunina, hugtökin og reglurnar á bak við eiginleika vöruhúsakerfisins í Business Central.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: 37c432a121c8105fbe982a4f8968094105530e3a
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/08/2019
ms.locfileid: "799846"
---
# <a name="design-details-warehouse-management"></a><span data-ttu-id="d8cfd-103">Hönnunarupplýsingar vöruhúsakerfi</span><span class="sxs-lookup"><span data-stu-id="d8cfd-103">Design Details: Warehouse Management</span></span>
<span data-ttu-id="d8cfd-104">Þessi fylgiskjöl veita yfirlit yfir hugtökin og reglurnar sem eru notaðar í valkostum Vöruhúsakerfa í [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="d8cfd-104">This documentation gives an overview of the concepts and principles that are used in the Warehouse Management features in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="d8cfd-105">Það útskýrir hönnun bak við helstu vörugeymsluaðgerðir og hvernig vörugeymslan vinnur með öðrum framboðskeðjuaðgerðum.</span><span class="sxs-lookup"><span data-stu-id="d8cfd-105">It explains the design behind central warehouse features and how warehousing integrates with other supply chain features.</span></span>  

<span data-ttu-id="d8cfd-106">Til að greina á milli mismunandi flækjustiga vörugeymsla, þetta Gögnunum er skipt í tvo almenna hópa, grunn og Ítarleg vöruhús, táknuð með kafla titla.</span><span class="sxs-lookup"><span data-stu-id="d8cfd-106">To differentiate the different complexity levels of the warehousing, this documentation is divided into two general groups, Basic and Advanced warehouse configurations, indicated by section titles.</span></span> <span data-ttu-id="d8cfd-107">Þessi einfalda aðgreining nær yfir mismunandi flækjustig samkvæmt skilgreiningu vörueinda og staðsetningaruppsetniingu.</span><span class="sxs-lookup"><span data-stu-id="d8cfd-107">This simple differentiation covers different complexity levels as defined by product granules and location setup.</span></span> <span data-ttu-id="d8cfd-108">Nánari upplýsingar eru í [Upplýsingar um hönnun: Uppsetning vöruhúss](design-details-warehouse-setup.md).</span><span class="sxs-lookup"><span data-stu-id="d8cfd-108">For more information, see [Design Details: Warehouse Setup](design-details-warehouse-setup.md).</span></span>  

## <a name="in-this-section"></a><span data-ttu-id="d8cfd-109">Í þessum hluta</span><span class="sxs-lookup"><span data-stu-id="d8cfd-109">In This Section</span></span>  
[<span data-ttu-id="d8cfd-110">Hönnunarupplýsingar yfirlit vöruhúss</span><span class="sxs-lookup"><span data-stu-id="d8cfd-110">Design Details: Warehouse Overview</span></span>](design-details-warehouse-overview.md)  
[<span data-ttu-id="d8cfd-111">Hönnunarupplýsingar uppsetningvöruhúss</span><span class="sxs-lookup"><span data-stu-id="d8cfd-111">Design Details: Warehouse Setup</span></span>](design-details-warehouse-setup.md)  
[<span data-ttu-id="d8cfd-112">Hönnunarupplýsingar: vöruhúsaflæði inn</span><span class="sxs-lookup"><span data-stu-id="d8cfd-112">Design Details: Inbound Warehouse Flow</span></span>](design-details-inbound-warehouse-flow.md)  
[<span data-ttu-id="d8cfd-113">Hönnunarupplýsingar: Innra vöruhúsaflæði</span><span class="sxs-lookup"><span data-stu-id="d8cfd-113">Design Details: Internal Warehouse Flows</span></span>](design-details-internal-warehouse-flows.md)  
[<span data-ttu-id="d8cfd-114">Hönnunarupplýsingar: Framboð í vöruhúsi</span><span class="sxs-lookup"><span data-stu-id="d8cfd-114">Design Details: Availability in the Warehouse</span></span>](design-details-availability-in-the-warehouse.md)  
[<span data-ttu-id="d8cfd-115">Hönnunarupplýsingar: vöruhúsaflæði á innleið</span><span class="sxs-lookup"><span data-stu-id="d8cfd-115">Design Details: Outbound Warehouse Flow</span></span>](design-details-outbound-warehouse-flow.md)  
[<span data-ttu-id="d8cfd-116">Hönnunarupplýsingar: Sameining með birgðum</span><span class="sxs-lookup"><span data-stu-id="d8cfd-116">Design Details: Integration with Inventory</span></span>](design-details-integration-with-inventory.md)
