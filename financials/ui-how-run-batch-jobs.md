---
title: Stofna og keyra runuvinnslu | Microsoft Docs
description: "Þú keyrir runuvinnslu til að vinna gögn og uppfæra upplýsingar, til dæmis að framkvæma tímabundnar bókhaldsaðgerðir eða útreikninga."
services: project-madeira
documentationcenter: 
author: SusanneWindfeldPedersen
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: task, process
ms.date: 03/29/2017
ms.author: solsen
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 6844d5fe3efba5349eef166161c5956116bc7fc0
ms.contentlocale: is-is
ms.lasthandoff: 09/11/2017

---
# <a name="how-to-run-batch-jobs"></a><span data-ttu-id="5ab05-103">Hvernig á að keyra runuvinnslur</span><span class="sxs-lookup"><span data-stu-id="5ab05-103">How to: Run Batch Jobs</span></span>
<span data-ttu-id="5ab05-104">Keyrsla er forritabútur sem vinnur úr gögnum í einni keyrslu líkt og keyrslan **Leiðrétta gengi**.</span><span class="sxs-lookup"><span data-stu-id="5ab05-104">A batch job is a routine that processes data in batches, for example the **Adjust Exchange Rates** batch job.</span></span> <span data-ttu-id="5ab05-105">Til eru runuvinnslur sem framkvæma reikningstímabilsaðgerðir eins og lokun rekstrarreiknings í lok reikningsárs.</span><span class="sxs-lookup"><span data-stu-id="5ab05-105">There are batch jobs that perform periodic accounting activities, such as closing the income statement at the end of a fiscal year.</span></span> <span data-ttu-id="5ab05-106">Margar keyrslur vinna útreikningsvinnu, svo sem útreikning á vöxtum, leiðréttingu á gengi og útreikning á einingaverði.</span><span class="sxs-lookup"><span data-stu-id="5ab05-106">Many batch jobs do calculation work, such as calculation of finance charges, exchange rate adjustment, and calculation of unit prices.</span></span>

<span data-ttu-id="5ab05-107">Keyrslu svipar til skýrslu fyrir utan það að keyrslan nýtir útkomuna til að uppfæra upplýsingar beint, án þess að prenta niðurstöðurnar.</span><span class="sxs-lookup"><span data-stu-id="5ab05-107">A batch job is like a report, except the batch job uses the result of its work to update information directly, instead of printing the results.</span></span>

## <a name="to-run-a-batch-job"></a><span data-ttu-id="5ab05-108">Til að keyra keyrslu</span><span class="sxs-lookup"><span data-stu-id="5ab05-108">To run a batch job</span></span>
1. <span data-ttu-id="5ab05-109">Til að opna beiðnigluggann fyrir viðeigandi runuvinnslu, skal velja ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið ") tákn, slá inn heiti runuvinnslunnar og velja svo tengdan tengil.</span><span class="sxs-lookup"><span data-stu-id="5ab05-109">To open the request window for the relevant batch job, choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter the name of the batch job, and then choose the related link.</span></span>
2. <span data-ttu-id="5ab05-110">Ef flýtiflipinn **Valkostir** er í boði fyrir runuvinnsluna er fyllt í reitina til að tilgreina hvað runuvinnslan á að gera.</span><span class="sxs-lookup"><span data-stu-id="5ab05-110">If there is an **Options** FastTab for the batch job, fill in the fields to determine what the batch job will do.</span></span>
3. <span data-ttu-id="5ab05-111">Í glugganum kann að vera einn eða fleiri flýtiflipar með afmörkunum sem hægt er að nota til að takmarka hvaða gögn eru innifalin í keyrslunni.</span><span class="sxs-lookup"><span data-stu-id="5ab05-111">The window may contain one or more FastTab with filters, which you can use to limit the data included in the batch job.</span></span> <span data-ttu-id="5ab05-112">Skilyrði eru sett á ráðlagðar afmarkanir eða fleiri afmörkunum bætt við.</span><span class="sxs-lookup"><span data-stu-id="5ab05-112">You can enter criteria in the suggested filters or add more filters.</span></span>
4. <span data-ttu-id="5ab05-113">Veldu hnappinn **Í lagi** til að hefja keyrsluna.</span><span class="sxs-lookup"><span data-stu-id="5ab05-113">Choose the **OK** button to start the batch job.</span></span>

## <a name="see-also"></a><span data-ttu-id="5ab05-114">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="5ab05-114">See Also</span></span>
[<span data-ttu-id="5ab05-115">Skilgreining skilyrða í síum</span><span class="sxs-lookup"><span data-stu-id="5ab05-115">Entering Criteria in Filters</span></span>](ui-enter-criteria-filters.md)  
<span data-ttu-id="5ab05-116">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="5ab05-116">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

