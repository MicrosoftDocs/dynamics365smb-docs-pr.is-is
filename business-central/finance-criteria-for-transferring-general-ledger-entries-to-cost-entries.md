---
title: Skilyrði til að millifærslu fjárhagsfærslna í kostnaðarfærslur | Microsoft Docs
description: Mikilvægt er að átta sig á skilyrðum fyrir því að flytja fjárhagsfærslur til kostnaðarfærslna. Meðan á millifærslu stendur notar runuvinnslan **Millifæra fjárhagsfærslu til kostnaðarbókhalds** eftirfarandi skilyrði til að tilgreina hvort og hvernig fjárhagsfærslur eru fluttar.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 11/13/2018
ms.author: sgroespe
redirect_url: finance-transfer-and-post-cost-entries
ms.openlocfilehash: 6e5fcfedbb899633f61c05b0b8b5ec8125112d65
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/08/2019
ms.locfileid: "799793"
---
# <a name="criteria-for-transferring-general-ledger-entries-to-cost-entries"></a><span data-ttu-id="98455-104">Skilyrði til að millifærslu fjárhagsfærslna í kostnaðarfærslur</span><span class="sxs-lookup"><span data-stu-id="98455-104">Criteria for Transferring General Ledger Entries to Cost Entries</span></span>
<span data-ttu-id="98455-105">Mikilvægt er að átta sig á skilyrðum fyrir því að flytja fjárhagsfærslur til kostnaðarfærslna.</span><span class="sxs-lookup"><span data-stu-id="98455-105">It is important to understand the criteria for transferring general ledger entries to cost entries.</span></span> <span data-ttu-id="98455-106">Meðan á millifærslu stendur notar runuvinnslan **Millifæra fjárhagsfærslu til kostnaðarbókhalds** eftirfarandi skilyrði til að tilgreina hvort og hvernig fjárhagsfærslur eru fluttar.</span><span class="sxs-lookup"><span data-stu-id="98455-106">During the transfer, the **Transfer GL Entries to CA** batch job uses the following criteria to determine if and how the general ledger entries are transferred.</span></span>  

<span data-ttu-id="98455-107">Fjárhagsfærslur eru fluttar ef:</span><span class="sxs-lookup"><span data-stu-id="98455-107">General ledger entries are transferred if:</span></span>  

-   <span data-ttu-id="98455-108">Færslurnar hafa víddargildi sem samsvara annaðhvort kostnaðarstað eða kostnaðarhlut.</span><span class="sxs-lookup"><span data-stu-id="98455-108">The entries have dimension values corresponding to either a cost center or a cost object.</span></span>  
-   <span data-ttu-id="98455-109">Færslurnar hafa víddargildi sem samsvara kostnaðarstað og kostnaðarhlut.</span><span class="sxs-lookup"><span data-stu-id="98455-109">The entries have dimension values that correspond to a cost center and a cost object.</span></span> <span data-ttu-id="98455-110">Kostnaðarstaðurinn hefur forgang í þessum færslum.</span><span class="sxs-lookup"><span data-stu-id="98455-110">For these entries, the cost center takes precedence.</span></span> <span data-ttu-id="98455-111">Þetta hjálpar til við að forðast aðstæður þar sem kostnaðargerð birtist í bæði kostnaðarhlut og kostnaðarstað og er því talin tvisvar í tölfræðigögnum.</span><span class="sxs-lookup"><span data-stu-id="98455-111">This helps avoid a situation where a cost type appears in both a cost object and a cost center and is therefore counted twice in the statistics.</span></span>  
-   <span data-ttu-id="98455-112">Fylgiskjalsnúmerið í færslunum er autt, þannig að það birtist með fylgiskjalsnúmerinu 0000 í kostnaðarfærslunum.</span><span class="sxs-lookup"><span data-stu-id="98455-112">The document number in the entries is empty, so it will appear with a document number of 0000 in the cost entries.</span></span>  
-   <span data-ttu-id="98455-113">Færslurnar eru færðar í kostnaðartegund sem leyfir við blandaðar færslur og þessar færslur eru fluttar sem blönduð færsla, annaðhvort mánaðarlega eða daglega.</span><span class="sxs-lookup"><span data-stu-id="98455-113">The entries are transferred to a cost type that allows for combined entries and these entries are transferred as a combined entry either monthly or daily.</span></span>  

<span data-ttu-id="98455-114">Fjárhagsfærslur eru ekki fluttar ef:</span><span class="sxs-lookup"><span data-stu-id="98455-114">General ledger entries are not transferred if:</span></span>  

-   <span data-ttu-id="98455-115">Færslurnar hafa víddargildi sem samsvara ekki kostnaðarstað né kostnaðarhlut.</span><span class="sxs-lookup"><span data-stu-id="98455-115">The entries have dimension values that do not correspond to a cost center or a cost object.</span></span>  
-   <span data-ttu-id="98455-116">Færslurnar hafa upphæð núll.</span><span class="sxs-lookup"><span data-stu-id="98455-116">The entries have an amount of zero.</span></span>  
-   <span data-ttu-id="98455-117">Færslurnar hafa fjárhagsreikning sem hefur verið eytt.</span><span class="sxs-lookup"><span data-stu-id="98455-117">The entries have a general ledger account that has been deleted.</span></span>  
-   <span data-ttu-id="98455-118">Færslurnar hafa fjárhagsreikning sem er ekki af tegundinni **Rekstrarreikningur**.</span><span class="sxs-lookup"><span data-stu-id="98455-118">The entries have a general ledger account that is not of the type **Income Statement**.</span></span>  
-   <span data-ttu-id="98455-119">Færslurnar hafa fjárhagsreikning sem er ekki tengdur kostnaðartegund.</span><span class="sxs-lookup"><span data-stu-id="98455-119">The entries have a general ledger account that is not assigned a cost type.</span></span>  
-   <span data-ttu-id="98455-120">Færslurnar hafa bókunardagsetningu fyrir **Upphafsdagsetning fjárhagsmillifærslu**.</span><span class="sxs-lookup"><span data-stu-id="98455-120">The entries have a posting date before the **Starting Date for G/L Transfer**.</span></span>  
-   <span data-ttu-id="98455-121">Færslurnar hafa verið bókaðar með lokadagsetningu.</span><span class="sxs-lookup"><span data-stu-id="98455-121">The entries have been posted with a closing date.</span></span> <span data-ttu-id="98455-122">Þetta eru yfirleitt færslur sem stilla aftur stöðu rekstrarreiknings við lok hvers árs.</span><span class="sxs-lookup"><span data-stu-id="98455-122">These are typically entries that set back the balance of the income statement at the end of the year.</span></span>  

## <a name="see-also"></a><span data-ttu-id="98455-123">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="98455-123">See Also</span></span>  
[<span data-ttu-id="98455-124">Kostnaðarreikningur</span><span class="sxs-lookup"><span data-stu-id="98455-124">Accounting for Costs</span></span>](finance-manage-cost-accounting.md)  
 <span data-ttu-id="98455-125">[Flytja fjárhagsfærslur í kostnaðarfærslur](finance-how-to-transfer-general-ledger-entries-to-cost-entries.md) </span><span class="sxs-lookup"><span data-stu-id="98455-125">[Transfer General Ledger Entries to Cost Entries](finance-how-to-transfer-general-ledger-entries-to-cost-entries.md) </span></span>  
 <span data-ttu-id="98455-126">[Flytja og bóka kostnaðarfærslur](finance-transfer-and-post-cost-entries.md) </span><span class="sxs-lookup"><span data-stu-id="98455-126">[Transferring and Posting Cost Entries](finance-transfer-and-post-cost-entries.md) </span></span>  
 [<span data-ttu-id="98455-127">Um kostnaðarbókhald</span><span class="sxs-lookup"><span data-stu-id="98455-127">About Cost Accounting</span></span>](finance-about-cost-accounting.md)  
 <span data-ttu-id="98455-128">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="98455-128">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
