---
title: "Sjálfvirkur flutningur og sameinaðar færslur | Microsoft Docs"
description: "Í kostnaðarbókhaldi er hægt að flytja fjárhagsfærslur í tegund kostnaðar með því að nota blandaða bókun. Þú getur tilgreint það ef kostnaðargerð fær sameinaðar færslur í reitinn **Sameinaðar færslur** í skilgreiningunni á kostnaðargerð. Eftirfarandi tafla lýsir hinum mismunandi valkostum."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 4f1bcf009b397438bb302a16a23be2f4638cefc4
ms.contentlocale: is-is
ms.lasthandoff: 03/22/2018

---
# <a name="automatic-transfer-and-combined-entries"></a><span data-ttu-id="ed7e1-105">Sjálfvirkur flutningur og færslur sameinaðar</span><span class="sxs-lookup"><span data-stu-id="ed7e1-105">Automatic Transfer and Combined Entries</span></span>
<span data-ttu-id="ed7e1-106">Í kostnaðarbókhaldi er hægt að flytja fjárhagsfærslur í tegund kostnaðar með því að nota blandaða bókun.</span><span class="sxs-lookup"><span data-stu-id="ed7e1-106">In cost accounting, you can transfer general ledger entries to a cost type by using a combined posting.</span></span> <span data-ttu-id="ed7e1-107">Þú getur tilgreint það ef kostnaðargerð fær sameinaðar færslur í reitinn **Sameinaðar færslur** í skilgreiningunni á kostnaðargerð.</span><span class="sxs-lookup"><span data-stu-id="ed7e1-107">You can specify if a cost type receives combined entries in the **Combine Entries** field in the cost type definition.</span></span> <span data-ttu-id="ed7e1-108">Eftirfarandi tafla lýsir hinum mismunandi valkostum.</span><span class="sxs-lookup"><span data-stu-id="ed7e1-108">The following table describes the different options.</span></span>  

|<span data-ttu-id="ed7e1-109">Sameina færslur</span><span class="sxs-lookup"><span data-stu-id="ed7e1-109">Combine entries</span></span>|<span data-ttu-id="ed7e1-110">Lýsing</span><span class="sxs-lookup"><span data-stu-id="ed7e1-110">Description</span></span>|  
|---------------------|-----------------|  
|<span data-ttu-id="ed7e1-111">Ekkert</span><span class="sxs-lookup"><span data-stu-id="ed7e1-111">None</span></span>|<span data-ttu-id="ed7e1-112">Hver fjárhagsfærsla er flutt sérstaklega í samsvarandi kostnaðartegund.</span><span class="sxs-lookup"><span data-stu-id="ed7e1-112">Each general ledger entry is transferred individually to the corresponding cost type.</span></span>|  
|<span data-ttu-id="ed7e1-113">Dagur</span><span class="sxs-lookup"><span data-stu-id="ed7e1-113">Day</span></span>|<span data-ttu-id="ed7e1-114">Fjárhagsfærslur með sömu bókunardagsetningu eru fluttar sem ein færsla í samsvarandi tegund kostnaðar.</span><span class="sxs-lookup"><span data-stu-id="ed7e1-114">General ledger entries with the same posting date are transferred as one entry to the corresponding cost type.</span></span>|  
|<span data-ttu-id="ed7e1-115">Mánuður</span><span class="sxs-lookup"><span data-stu-id="ed7e1-115">Month</span></span>|<span data-ttu-id="ed7e1-116">Allar fjárhagsfærslur í sama almanaksmánuði eru fluttar sem ein færsla í samsvarandi tegund kostnaðar.</span><span class="sxs-lookup"><span data-stu-id="ed7e1-116">All general ledger entries in the same calendar month are transferred as one entry to the corresponding cost type.</span></span>|  

> [!IMPORTANT]  
>  <span data-ttu-id="ed7e1-117">Ef gátreiturinn **Sjálfvirk færsla úr fjárhag** er valinn í glugganum **Uppsetning kostnaðarbókhalds**, uppfærir [!INCLUDE[d365fin](includes/d365fin_md.md)] kostnaðarbókhaldið eftir hverja bókun í fjárhag.</span><span class="sxs-lookup"><span data-stu-id="ed7e1-117">If you have selected the **Auto Transfer from G/L** check box in the **Cost Accounting Setup** window, [!INCLUDE[d365fin](includes/d365fin_md.md)] updates the cost accounting after every posting in the general ledger.</span></span> <span data-ttu-id="ed7e1-118">Sameinaðar færslur eru ekki mögulegar.</span><span class="sxs-lookup"><span data-stu-id="ed7e1-118">Combined entries are not possible.</span></span>  

## <a name="see-also"></a><span data-ttu-id="ed7e1-119">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="ed7e1-119">See Also</span></span>  
 <span data-ttu-id="ed7e1-120">[Flytja fjárhagsfærslur í kostnaðarfærslur](finance-how-to-transfer-general-ledger-entries-to-cost-entries.md) </span><span class="sxs-lookup"><span data-stu-id="ed7e1-120">[Transfer General Ledger Entries to Cost Entries](finance-how-to-transfer-general-ledger-entries-to-cost-entries.md) </span></span>  
 <span data-ttu-id="ed7e1-121">[Skilyrði til að millifærslu fjárhagsfærslna í kostnaðarfærslur](finance-criteria-for-transferring-general-ledger-entries-to-cost-entries.md) </span><span class="sxs-lookup"><span data-stu-id="ed7e1-121">[Criteria for Transferring General Ledger Entries to Cost Entries](finance-criteria-for-transferring-general-ledger-entries-to-cost-entries.md) </span></span>  
 <span data-ttu-id="ed7e1-122">[Niðurstöður millifærslu](finance-results-of-the-transfer.md) </span><span class="sxs-lookup"><span data-stu-id="ed7e1-122">[Results of the Transfer](finance-results-of-the-transfer.md) </span></span>  
 [<span data-ttu-id="ed7e1-123">Flytja og bóka kostnaðarfærslur</span><span class="sxs-lookup"><span data-stu-id="ed7e1-123">Transferring and Posting Cost Entries</span></span>](finance-transfer-and-post-cost-entries.md)  
 <span data-ttu-id="ed7e1-124">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="ed7e1-124">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

