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
ms.date: 04/01/2019
ms.author: solsen
ms.openlocfilehash: 0b9bf37f9054d767938b851e399a1b2c347f77c3
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/29/2019
ms.locfileid: "1249262"
---
# <a name="run-batch-jobs"></a><span data-ttu-id="0621b-103">Keyra runuvinnslur</span><span class="sxs-lookup"><span data-stu-id="0621b-103">Run Batch Jobs</span></span>
<span data-ttu-id="0621b-104">Keyrsla er forritabútur sem vinnur úr gögnum í einni keyrslu líkt og keyrslan **Leiðrétta gengi**.</span><span class="sxs-lookup"><span data-stu-id="0621b-104">A batch job is a routine that processes data in batches, for example the **Adjust Exchange Rates** batch job.</span></span> <span data-ttu-id="0621b-105">Til eru runuvinnslur sem framkvæma reikningstímabilsaðgerðir eins og lokun rekstrarreiknings í lok reikningsárs.</span><span class="sxs-lookup"><span data-stu-id="0621b-105">There are batch jobs that perform periodic accounting activities, such as closing the income statement at the end of a fiscal year.</span></span> <span data-ttu-id="0621b-106">Margar keyrslur vinna útreikningsvinnu, svo sem útreikning á vöxtum, leiðréttingu á gengi og útreikning á einingaverði.</span><span class="sxs-lookup"><span data-stu-id="0621b-106">Many batch jobs do calculation work, such as calculation of finance charges, exchange rate adjustment, and calculation of unit prices.</span></span>

<span data-ttu-id="0621b-107">Keyrslu svipar til skýrslu fyrir utan það að keyrslan nýtir útkomuna til að uppfæra upplýsingar beint, án þess að prenta niðurstöðurnar.</span><span class="sxs-lookup"><span data-stu-id="0621b-107">A batch job is like a report, except the batch job uses the result of its work to update information directly, instead of printing the results.</span></span>

## <a name="to-run-a-batch-job"></a><span data-ttu-id="0621b-108">Til að keyra keyrslu</span><span class="sxs-lookup"><span data-stu-id="0621b-108">To run a batch job</span></span>
1. <span data-ttu-id="0621b-109">Til að opna beiðnisíðu fyrir viðkomandi runuvinnslu velurðu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, slærð inn heiti runuvinnslunnar og velur síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="0621b-109">To open the request page for the relevant batch job, choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter the name of the batch job, and then choose the related link.</span></span>
2. <span data-ttu-id="0621b-110">Ef flýtiflipinn **Valkostir** er í boði fyrir runuvinnsluna er fyllt í reitina til að tilgreina hvað runuvinnslan á að gera.</span><span class="sxs-lookup"><span data-stu-id="0621b-110">If there is an **Options** FastTab for the batch job, fill in the fields to determine what the batch job will do.</span></span>
3. <span data-ttu-id="0621b-111">Á síðunni kann að vera einn eða fleiri flýtiflipar með afmörkunum sem hægt er að nota til að takmarka hvaða gögn eru innifalin í keyrslunni.</span><span class="sxs-lookup"><span data-stu-id="0621b-111">The page may contain one or more FastTab with filters, which you can use to limit the data included in the batch job.</span></span> <span data-ttu-id="0621b-112">Skilyrði eru sett á ráðlagðar afmarkanir eða fleiri afmörkunum bætt við.</span><span class="sxs-lookup"><span data-stu-id="0621b-112">You can enter criteria in the suggested filters or add more filters.</span></span>
4. <span data-ttu-id="0621b-113">Veldu hnappinn **Í lagi** til að hefja keyrsluna.</span><span class="sxs-lookup"><span data-stu-id="0621b-113">Choose the **OK** button to start the batch job.</span></span>

## <a name="see-also"></a><span data-ttu-id="0621b-114">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="0621b-114">See Also</span></span>
[<span data-ttu-id="0621b-115">Röðun, leit og síun í listum</span><span class="sxs-lookup"><span data-stu-id="0621b-115">Sorting, Searching, and Filtering Lists</span></span>](ui-enter-criteria-filters.md)  
<span data-ttu-id="0621b-116">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="0621b-116">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
