---
title: Sjálfvirkur flutningur og sameinaðar færslur | Microsoft Docs
description: Í kostnaðarbókhaldi er hægt að flytja fjárhagsfærslur í tegund kostnaðar með því að nota blandaða bókun. Þú getur tilgreint það ef kostnaðargerð fær sameinaðar færslur í reitinn **Sameinaðar færslur** í skilgreiningunni á kostnaðargerð. Eftirfarandi tafla lýsir hinum mismunandi valkostum.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
redirect_url: finance-transfer-and-post-cost-entries
ms.openlocfilehash: 8f6b5328b3a7b8cdcb4582deda363bdd0361ed9a
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/29/2019
ms.locfileid: "1238993"
---
# <a name="automatic-transfer-and-combined-entries"></a><span data-ttu-id="a0588-105">Sjálfvirkur flutningur og færslur sameinaðar</span><span class="sxs-lookup"><span data-stu-id="a0588-105">Automatic Transfer and Combined Entries</span></span>
<span data-ttu-id="a0588-106">Í kostnaðarbókhaldi er hægt að flytja fjárhagsfærslur í tegund kostnaðar með því að nota blandaða bókun.</span><span class="sxs-lookup"><span data-stu-id="a0588-106">In cost accounting, you can transfer general ledger entries to a cost type by using a combined posting.</span></span> <span data-ttu-id="a0588-107">Þú getur tilgreint það ef kostnaðargerð fær sameinaðar færslur í reitinn **Sameinaðar færslur** í skilgreiningunni á kostnaðargerð.</span><span class="sxs-lookup"><span data-stu-id="a0588-107">You can specify if a cost type receives combined entries in the **Combine Entries** field in the cost type definition.</span></span> <span data-ttu-id="a0588-108">Eftirfarandi tafla lýsir hinum mismunandi valkostum.</span><span class="sxs-lookup"><span data-stu-id="a0588-108">The following table describes the different options.</span></span>  

|<span data-ttu-id="a0588-109">Sameina færslur</span><span class="sxs-lookup"><span data-stu-id="a0588-109">Combine entries</span></span>|<span data-ttu-id="a0588-110">Lýsing</span><span class="sxs-lookup"><span data-stu-id="a0588-110">Description</span></span>|  
|---------------------|-----------------|  
|<span data-ttu-id="a0588-111">Ekkert</span><span class="sxs-lookup"><span data-stu-id="a0588-111">None</span></span>|<span data-ttu-id="a0588-112">Hver fjárhagsfærsla er flutt sérstaklega í samsvarandi kostnaðartegund.</span><span class="sxs-lookup"><span data-stu-id="a0588-112">Each general ledger entry is transferred individually to the corresponding cost type.</span></span>|  
|<span data-ttu-id="a0588-113">Dagur</span><span class="sxs-lookup"><span data-stu-id="a0588-113">Day</span></span>|<span data-ttu-id="a0588-114">Fjárhagsfærslur með sömu bókunardagsetningu eru fluttar sem ein færsla í samsvarandi tegund kostnaðar.</span><span class="sxs-lookup"><span data-stu-id="a0588-114">General ledger entries with the same posting date are transferred as one entry to the corresponding cost type.</span></span>|  
|<span data-ttu-id="a0588-115">Mánuður</span><span class="sxs-lookup"><span data-stu-id="a0588-115">Month</span></span>|<span data-ttu-id="a0588-116">Allar fjárhagsfærslur í sama almanaksmánuði eru fluttar sem ein færsla í samsvarandi tegund kostnaðar.</span><span class="sxs-lookup"><span data-stu-id="a0588-116">All general ledger entries in the same calendar month are transferred as one entry to the corresponding cost type.</span></span>|  

> [!IMPORTANT]  
>  <span data-ttu-id="a0588-117">Ef gátreiturinn **Sjálfvirk færsla úr fjárhag** er valinn af síðunni **Uppsetning kostnaðarbókhalds**, uppfærir [!INCLUDE[d365fin](includes/d365fin_md.md)] kostnaðarbókhaldið eftir hverja bókun í fjárhag.</span><span class="sxs-lookup"><span data-stu-id="a0588-117">If you have selected the **Auto Transfer from G/L** check box on the **Cost Accounting Setup** page, [!INCLUDE[d365fin](includes/d365fin_md.md)] updates the cost accounting after every posting in the general ledger.</span></span> <span data-ttu-id="a0588-118">Sameinaðar færslur eru ekki mögulegar.</span><span class="sxs-lookup"><span data-stu-id="a0588-118">Combined entries are not possible.</span></span>  

## <a name="see-also"></a><span data-ttu-id="a0588-119">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="a0588-119">See Also</span></span>  
 <span data-ttu-id="a0588-120">[Flytja og bóka kostnaðarfærslur](finance-transfer-and-post-cost-entries.md) </span><span class="sxs-lookup"><span data-stu-id="a0588-120">[Transferring and Posting Cost Entries](finance-transfer-and-post-cost-entries.md) </span></span>  
 <span data-ttu-id="a0588-121">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="a0588-121">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
