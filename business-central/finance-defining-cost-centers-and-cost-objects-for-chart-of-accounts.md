---
title: "Skilgreining kostnaðarstaði og kostnaðarhluti fyrir bókhaldslykil | Microsoft Docs"
description: "Hægt er að flytja útgjalda- og tekjufærslur sjálfkrafa úr fjárhag í kostnaðarbókhald, annað hvort fyrir hverja fjarhagsfærslu eða með keyrslu. Þegar flutningurinn er framkvæmdur flytur kerfið aðeins færslur sem þegar eru tengdar við kostnaðarstað eða kostnaðarhlut. Til að búa til merkingarbæran flutning þarf að tryggja að kostnaðarstaðir og kostnaðarhlutir séu rétt skilgreindir."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
redirect_url: finance-set-up-cost-accounting
ms.translationtype: HT
ms.sourcegitcommit: caf7cf5afe370af0c4294c794c0ff9bc8ff4c31c
ms.openlocfilehash: b3ca863a9f4969046695e0cec16fedf6f5ac7aec
ms.contentlocale: is-is
ms.lasthandoff: 11/22/2018

---
# <a name="defining-cost-centers-and-cost-objects-for-chart-of-accounts"></a><span data-ttu-id="da382-105">Skilgreining kostnaðarstaði og kostnaðarhluti fyrir bókhaldslykil</span><span class="sxs-lookup"><span data-stu-id="da382-105">Defining Cost Centers and Cost Objects for Chart of Accounts</span></span>
<span data-ttu-id="da382-106">Hægt er að flytja útgjalda- og tekjufærslur sjálfkrafa úr fjárhag í kostnaðarbókhald, annað hvort fyrir hverja fjarhagsfærslu eða með keyrslu.</span><span class="sxs-lookup"><span data-stu-id="da382-106">You can automatically transfer the expense and income entries from the general ledger to cost accounting either for each general ledger posting or with a batch job.</span></span> <span data-ttu-id="da382-107">Þegar flutningurinn er framkvæmdur flytur [!INCLUDE[d365fin](includes/d365fin_md.md)] aðeins færslur sem þegar eru tengdar við kostnaðarstað eða kostnaðarhlut.</span><span class="sxs-lookup"><span data-stu-id="da382-107">When you do the transfer, [!INCLUDE[d365fin](includes/d365fin_md.md)] only transfers the entries that are already linked to a cost center or a cost object.</span></span> <span data-ttu-id="da382-108">Til að búa til merkingarbæran flutning þarf að tryggja að kostnaðarstaðir og kostnaðarhlutir séu rétt skilgreindir.</span><span class="sxs-lookup"><span data-stu-id="da382-108">To establish a meaningful transfer, you must ensure that the cost centers and cost objects are correctly defined.</span></span>  

## <a name="defining-default-dimension-values-for-general-ledger-accounts"></a><span data-ttu-id="da382-109">Skilgreining sjálfgefin víddargildi fyrir fjárhagslykla</span><span class="sxs-lookup"><span data-stu-id="da382-109">Defining Default Dimension Values for General Ledger Accounts</span></span>  
<span data-ttu-id="da382-110">Fyrir hvern fjárhagsreikning er hægt að skilgreina sjálfgefið víddargildi í töflunni **Sjálfgefið víddargildi**.</span><span class="sxs-lookup"><span data-stu-id="da382-110">For each general ledger account, you can define default dimension values in the **Default Dimension** table.</span></span> <span data-ttu-id="da382-111">Eftirfarandi dæmi sýnir hvernig eigi að skilgreina að það ætti alltaf að vera kostnaðarstaður DEILDAR, en aldrei kostnaðarhlutur VERKEFNIS þegar bókað er á almennan fjárhagslykil.</span><span class="sxs-lookup"><span data-stu-id="da382-111">The following example shows how to define that there should always be a DEPARTMENT cost center, but never be a PROJECT cost object when posting to a general ledger account.</span></span>  

|<span data-ttu-id="da382-112">**Víddarkóti**</span><span class="sxs-lookup"><span data-stu-id="da382-112">**Dimension Code**</span></span>|<span data-ttu-id="da382-113">**Virðisbókun**</span><span class="sxs-lookup"><span data-stu-id="da382-113">**Value Posting**</span></span>|  
|------------------------------------------|-----------------------------------------|  
|<span data-ttu-id="da382-114">Deild</span><span class="sxs-lookup"><span data-stu-id="da382-114">Department</span></span>|<span data-ttu-id="da382-115">Kóti tilskilinn</span><span class="sxs-lookup"><span data-stu-id="da382-115">Code Mandatory</span></span>|  
|<span data-ttu-id="da382-116">Verkefni</span><span class="sxs-lookup"><span data-stu-id="da382-116">Project</span></span>|<span data-ttu-id="da382-117">Enginn kóti</span><span class="sxs-lookup"><span data-stu-id="da382-117">No Code</span></span>|  

## <a name="defining-dimension-values-for-overhead-costs-and-direct-costs"></a><span data-ttu-id="da382-118">Skilgreining á víddargildi fyrir sameiginlegan kostnað og beinan kostnað</span><span class="sxs-lookup"><span data-stu-id="da382-118">Defining Dimension Values for Overhead Costs and Direct Costs</span></span>  
 <span data-ttu-id="da382-119">Hægt er að flytja rekstrarkostnað í kostnaðarstað og beinan kostnað í kostnaðaríhlut.</span><span class="sxs-lookup"><span data-stu-id="da382-119">You can transfer overhead costs to a cost center and direct costs to a cost object.</span></span> <span data-ttu-id="da382-120">Eftirfarandi tafla sýnir bestu samsetningu uppsetningargilda vídda.</span><span class="sxs-lookup"><span data-stu-id="da382-120">The following table shows the optimal combination of the dimension setup values.</span></span>  

|<span data-ttu-id="da382-121">Flytja í</span><span class="sxs-lookup"><span data-stu-id="da382-121">Transfer To</span></span>|<span data-ttu-id="da382-122">Bókun kostnaðarstaðar</span><span class="sxs-lookup"><span data-stu-id="da382-122">Cost Center Posting</span></span>|<span data-ttu-id="da382-123">Bókun kostnaðarhlutar</span><span class="sxs-lookup"><span data-stu-id="da382-123">Cost Object Posting</span></span>|  
|-----------------|-------------------------|-------------------------|  
|<span data-ttu-id="da382-124">Kostnaðarstaður</span><span class="sxs-lookup"><span data-stu-id="da382-124">Cost Center</span></span>|<span data-ttu-id="da382-125">Kóti tilskilinn</span><span class="sxs-lookup"><span data-stu-id="da382-125">Code Mandatory</span></span>|<span data-ttu-id="da382-126">Enginn kóti</span><span class="sxs-lookup"><span data-stu-id="da382-126">No Code</span></span>|  
|<span data-ttu-id="da382-127">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="da382-127">Cost Object</span></span>|<span data-ttu-id="da382-128">Enginn kóti</span><span class="sxs-lookup"><span data-stu-id="da382-128">No Code</span></span>|<span data-ttu-id="da382-129">Kóti tilskilinn</span><span class="sxs-lookup"><span data-stu-id="da382-129">Code Mandatory</span></span>|  

> [!NOTE]  
>  <span data-ttu-id="da382-130">Til að ganga úr skugga um að fyrirfram skilgreindur kostnaðarstaður og kostnaðarhlutur sem eru sett upp í fjárhag séu sjálfkrafa færðar yfir í kostnaðarbókhald skal velja gátreitinn **Athuga fjárhagsbókanir** á síðunni Uppsetning kostnaðarbókhalds</span><span class="sxs-lookup"><span data-stu-id="da382-130">To make sure that the predefined cost center and cost object that you set up in the general ledger are automatically carried over to cost accounting, select the **Check G/L Postings** check box in the Cost Accounting Setup page.</span></span>  

## <a name="see-also"></a><span data-ttu-id="da382-131">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="da382-131">See Also</span></span>  
[<span data-ttu-id="da382-132">Kostnaðarreikningur</span><span class="sxs-lookup"><span data-stu-id="da382-132">Accounting for Costs</span></span>](finance-manage-cost-accounting.md)  
[<span data-ttu-id="da382-133">Uppsetning kostnaðarbókhalds</span><span class="sxs-lookup"><span data-stu-id="da382-133">Setting Up Cost Accounting</span></span>](finance-set-up-cost-accounting.md)  
<span data-ttu-id="da382-134">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="da382-134">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

