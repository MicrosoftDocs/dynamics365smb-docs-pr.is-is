---
title: "Endurskoða og bóka lokafærslu ársloka | Microsoft Docs"
description: "Lýsir því hvernig skal opna færslubókina sem þú tilgreindir í runuvinnslunni Loka rekstrarreikningi, og svo endurskoða og bóka lokafærslu ársloka."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: year closing, close accounting period, close fiscal year, bank account detailed trial balance
ms.date: 03/29/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 78039e9387866ce17ff3be5a2ff509545e8439d2
ms.contentlocale: is-is
ms.lasthandoff: 01/30/2018

---
# <a name="post-the-year-end-closing-entry"></a><span data-ttu-id="6b15c-103">Bóka lokafærslu ársloka</span><span class="sxs-lookup"><span data-stu-id="6b15c-103">Post the Year-End Closing Entry</span></span>
<span data-ttu-id="6b15c-104">Eftir að runuvinnslan **Loka rekstrarreikningi** hefur verið notuð til að mynda færslu eða færslur fyrir lokun í árslok verður að opna færslubókina sem var tilgreind í runuvinnslunni,  og fara yfir og bóka færslurnar.</span><span class="sxs-lookup"><span data-stu-id="6b15c-104">After you use the **Close Income Statement** batch job to generate the year-end closing entry or entries, you must open the journal you specified in the batch job, and then review and post the entries.</span></span>

## <a name="to-post-the-year-end-closing-entry"></a><span data-ttu-id="6b15c-105">Til að bóka lokunarfærslu ársloka</span><span class="sxs-lookup"><span data-stu-id="6b15c-105">To post the year end closing entry</span></span>
1. <span data-ttu-id="6b15c-106">Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **færslubók** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="6b15c-106">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **General Journal**, and then choose the related link.</span></span>
2. <span data-ttu-id="6b15c-107">Í glugganum **almenn færslubók** í reitnum **Heiti keyrslu** er keyrslan sem inniheldur lokunarfærslurnar valin.</span><span class="sxs-lookup"><span data-stu-id="6b15c-107">In the **General Journal** window, in the **Batch Name** field, select the batch that contains the closing entries.</span></span>
3. <span data-ttu-id="6b15c-108">Farið er yfir færslurnar.</span><span class="sxs-lookup"><span data-stu-id="6b15c-108">Review the entries.</span></span>
4. <span data-ttu-id="6b15c-109">Til að bóka færslubókina er valið aðgerðin **bóka**.</span><span class="sxs-lookup"><span data-stu-id="6b15c-109">To post the journal, choose the **Post** action.</span></span>

> [!NOTE]  
>   <span data-ttu-id="6b15c-110">Greinist villa birtast villuboð.</span><span class="sxs-lookup"><span data-stu-id="6b15c-110">If an error is detected, an error message is displayed.</span></span> <span data-ttu-id="6b15c-111">Ef bókunin heppnast eru bókaðar færslur fjarlægðar úr færslubókinni.</span><span class="sxs-lookup"><span data-stu-id="6b15c-111">If the posting is successful, the posted entries are removed from the journal.</span></span> <span data-ttu-id="6b15c-112">Þegar færsla hefur verið bókuð er hún bókuð á alla rekstrarreikninga til að staðan verði núll, og útkoma ársins er færð á efnahagsreikning.</span><span class="sxs-lookup"><span data-stu-id="6b15c-112">After posting is complete, an entry is posted to each income statement account so that its balance becomes zero and the year's result is transferred to the balance sheet.</span></span>

## <a name="see-also"></a><span data-ttu-id="6b15c-113">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="6b15c-113">See Also</span></span>
[<span data-ttu-id="6b15c-114">Loka fjárhagstímabilum</span><span class="sxs-lookup"><span data-stu-id="6b15c-114">Close Accounting Periods</span></span>](year-close-account-periods.md)  
[<span data-ttu-id="6b15c-115">Bókum lokað</span><span class="sxs-lookup"><span data-stu-id="6b15c-115">Closing Books</span></span>](year-close-books.md)  
[<span data-ttu-id="6b15c-116">Loka rekstrarreikningi</span><span class="sxs-lookup"><span data-stu-id="6b15c-116">Close Income Statement</span></span>](year-close-income-statement.md)  
<span data-ttu-id="6b15c-117">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="6b15c-117">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

