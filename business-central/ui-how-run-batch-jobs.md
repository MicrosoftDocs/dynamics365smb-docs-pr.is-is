---
title: Stofna og keyra runuvinnslu | Microsoft Docs
description: "Þú keyrir runuvinnslu til að vinna gögn og uppfæra upplýsingar, til dæmis að framkvæma tímabundnar bókhaldsaðgerðir eða útreikninga."
services: project-madeira
documentationcenter: 
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: task, process
ms.date: 10/01/2018
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 9a6435120d122db894bcd6c953da5ab8ea78420b
ms.contentlocale: is-is
ms.lasthandoff: 09/28/2018

---
# <a name="run-batch-jobs"></a><span data-ttu-id="34ce6-103">Keyra runuvinnslur</span><span class="sxs-lookup"><span data-stu-id="34ce6-103">Run Batch Jobs</span></span>
<span data-ttu-id="34ce6-104">Keyrsla er forritabútur sem vinnur úr gögnum í einni keyrslu líkt og keyrslan **Leiðrétta gengi**.</span><span class="sxs-lookup"><span data-stu-id="34ce6-104">A batch job is a routine that processes data in batches, for example the **Adjust Exchange Rates** batch job.</span></span> <span data-ttu-id="34ce6-105">Til eru runuvinnslur sem framkvæma reikningstímabilsaðgerðir eins og lokun rekstrarreiknings í lok reikningsárs.</span><span class="sxs-lookup"><span data-stu-id="34ce6-105">There are batch jobs that perform periodic accounting activities, such as closing the income statement at the end of a fiscal year.</span></span> <span data-ttu-id="34ce6-106">Margar keyrslur vinna útreikningsvinnu, svo sem útreikning á vöxtum, leiðréttingu á gengi og útreikning á einingaverði.</span><span class="sxs-lookup"><span data-stu-id="34ce6-106">Many batch jobs do calculation work, such as calculation of finance charges, exchange rate adjustment, and calculation of unit prices.</span></span>

<span data-ttu-id="34ce6-107">Keyrslu svipar til skýrslu fyrir utan það að keyrslan nýtir útkomuna til að uppfæra upplýsingar beint, án þess að prenta niðurstöðurnar.</span><span class="sxs-lookup"><span data-stu-id="34ce6-107">A batch job is like a report, except the batch job uses the result of its work to update information directly, instead of printing the results.</span></span>

## <a name="to-run-a-batch-job"></a><span data-ttu-id="34ce6-108">Til að keyra keyrslu</span><span class="sxs-lookup"><span data-stu-id="34ce6-108">To run a batch job</span></span>
1. <span data-ttu-id="34ce6-109">Til að opna beiðniglugga fyrir viðkomandi runuvinnslu velurðu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, slærð inn heiti runuvinnslunnar og velur síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="34ce6-109">To open the request window for the relevant batch job, choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter the name of the batch job, and then choose the related link.</span></span>
2. <span data-ttu-id="34ce6-110">Ef flýtiflipinn **Valkostir** er í boði fyrir runuvinnsluna er fyllt í reitina til að tilgreina hvað runuvinnslan á að gera.</span><span class="sxs-lookup"><span data-stu-id="34ce6-110">If there is an **Options** FastTab for the batch job, fill in the fields to determine what the batch job will do.</span></span>
3. <span data-ttu-id="34ce6-111">Í glugganum kann að vera einn eða fleiri flýtiflipar með afmörkunum sem hægt er að nota til að takmarka hvaða gögn eru innifalin í keyrslunni.</span><span class="sxs-lookup"><span data-stu-id="34ce6-111">The window may contain one or more FastTab with filters, which you can use to limit the data included in the batch job.</span></span> <span data-ttu-id="34ce6-112">Skilyrði eru sett á ráðlagðar afmarkanir eða fleiri afmörkunum bætt við.</span><span class="sxs-lookup"><span data-stu-id="34ce6-112">You can enter criteria in the suggested filters or add more filters.</span></span>
4. <span data-ttu-id="34ce6-113">Veldu hnappinn **Í lagi** til að hefja keyrsluna.</span><span class="sxs-lookup"><span data-stu-id="34ce6-113">Choose the **OK** button to start the batch job.</span></span>

## <a name="see-also"></a><span data-ttu-id="34ce6-114">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="34ce6-114">See Also</span></span>
[<span data-ttu-id="34ce6-115">Leita í, afmarka og raða gögnum</span><span class="sxs-lookup"><span data-stu-id="34ce6-115">Searching, Filtering, and Sorting Data</span></span>](ui-enter-criteria-filters.md)  
<span data-ttu-id="34ce6-116">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="34ce6-116">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

