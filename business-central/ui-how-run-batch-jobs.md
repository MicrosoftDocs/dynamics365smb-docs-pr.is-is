---
title: Stofna og keyra runuvinnslu | Microsoft Docs
description: Þú keyrir runuvinnslu til að vinna gögn og uppfæra upplýsingar, til dæmis að framkvæma tímabundnar bókhaldsaðgerðir eða útreikninga.
services: project-madeira
documentationcenter: ''
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: task, process
ms.date: 04/01/2020
ms.author: solsen
ms.openlocfilehash: c54edd1e907c27aca719898319f69f98c0a0a068
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2020
ms.locfileid: "3195604"
---
# <a name="run-batch-jobs-and-xmlports"></a><span data-ttu-id="aa8f1-103">Keyra runuvinnslur og XMLports</span><span class="sxs-lookup"><span data-stu-id="aa8f1-103">Run Batch Jobs and XMLports</span></span>
<span data-ttu-id="aa8f1-104">Keyrsla er forritabútur sem vinnur úr gögnum í einni keyrslu líkt og keyrslan **Leiðrétta gengi**.</span><span class="sxs-lookup"><span data-stu-id="aa8f1-104">A batch job is a routine that processes data in batches, for example the **Adjust Exchange Rates** batch job.</span></span> <span data-ttu-id="aa8f1-105">Til eru runuvinnslur sem framkvæma reikningstímabilsaðgerðir eins og lokun rekstrarreiknings í lok reikningsárs.</span><span class="sxs-lookup"><span data-stu-id="aa8f1-105">There are batch jobs that perform periodic accounting activities, such as closing the income statement at the end of a fiscal year.</span></span> <span data-ttu-id="aa8f1-106">Margar keyrslur vinna útreikningsvinnu, svo sem útreikning á vöxtum, leiðréttingu á gengi og útreikning á einingaverði.</span><span class="sxs-lookup"><span data-stu-id="aa8f1-106">Many batch jobs do calculation work, such as calculation of finance charges, exchange rate adjustment, and calculation of unit prices.</span></span>

<span data-ttu-id="aa8f1-107">Keyrslu svipar til skýrslu fyrir utan það að keyrslan nýtir útkomuna til að uppfæra upplýsingar beint, án þess að prenta niðurstöðurnar.</span><span class="sxs-lookup"><span data-stu-id="aa8f1-107">A batch job is like a report, except the batch job uses the result of its work to update information directly, instead of printing the results.</span></span>

<span data-ttu-id="aa8f1-108">Hægt er að tímasetja hvenær runuvinnsla er keyrð.</span><span class="sxs-lookup"><span data-stu-id="aa8f1-108">You can schedule when a batch job runs.</span></span> <span data-ttu-id="aa8f1-109">Frekari upplýsingar, sjá [Nota verkraðir til að tímaraða verkhlutum](admin-job-queues-schedule-tasks.md).</span><span class="sxs-lookup"><span data-stu-id="aa8f1-109">For more information, see [Use Job Queues to Schedule Tasks](admin-job-queues-schedule-tasks.md).</span></span>

## <a name="to-run-a-batch-job"></a><span data-ttu-id="aa8f1-110">Til að keyra keyrslu</span><span class="sxs-lookup"><span data-stu-id="aa8f1-110">To run a batch job</span></span>
1. <span data-ttu-id="aa8f1-111">Til að opna beiðnisíðu fyrir viðkomandi runuvinnslu velurðu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, slærð inn heiti runuvinnslunnar og velur síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="aa8f1-111">To open the request page for the relevant batch job, choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter the name of the batch job, and then choose the related link.</span></span>
2. <span data-ttu-id="aa8f1-112">Ef flýtiflipinn **Valkostir** er í boði fyrir runuvinnsluna er fyllt í reitina til að tilgreina hvað runuvinnslan á að gera.</span><span class="sxs-lookup"><span data-stu-id="aa8f1-112">If there is an **Options** FastTab for the batch job, fill in the fields to determine what the batch job will do.</span></span>
3. <span data-ttu-id="aa8f1-113">Á síðunni kann að vera einn eða fleiri flýtiflipar með afmörkunum sem hægt er að nota til að takmarka hvaða gögn eru innifalin í keyrslunni.</span><span class="sxs-lookup"><span data-stu-id="aa8f1-113">The page may contain one or more FastTab with filters, which you can use to limit the data included in the batch job.</span></span> <span data-ttu-id="aa8f1-114">Skilyrði eru sett á ráðlagðar afmarkanir eða fleiri afmörkunum bætt við.</span><span class="sxs-lookup"><span data-stu-id="aa8f1-114">You can enter criteria in the suggested filters or add more filters.</span></span>
4. <span data-ttu-id="aa8f1-115">Veldu hnappinn **Í lagi** til að hefja keyrsluna.</span><span class="sxs-lookup"><span data-stu-id="aa8f1-115">Choose the **OK** button to start the batch job.</span></span>

## <a name="see-also"></a><span data-ttu-id="aa8f1-116">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="aa8f1-116">See Also</span></span>
[<span data-ttu-id="aa8f1-117">Röðun, leit og síun í listum</span><span class="sxs-lookup"><span data-stu-id="aa8f1-117">Sorting, Searching, and Filtering Lists</span></span>](ui-enter-criteria-filters.md)  
[<span data-ttu-id="aa8f1-118">Nota verkraðir til að tímaraða verkhlutum</span><span class="sxs-lookup"><span data-stu-id="aa8f1-118">Use Job Queues to Schedule Tasks</span></span>](admin-job-queues-schedule-tasks.md)  
<span data-ttu-id="aa8f1-119">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="aa8f1-119">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
