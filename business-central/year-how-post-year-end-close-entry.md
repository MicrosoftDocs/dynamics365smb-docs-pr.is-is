---
title: Endurskoða og bóka lokafærslu ársloka | Microsoft Docs
description: Lýsir því hvernig skal opna færslubókina sem þú tilgreindir í runuvinnslunni Loka rekstrarreikningi, og svo endurskoða og bóka lokafærslu ársloka.
services: project-madeira
documentationcenter: ''
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: year closing, close accounting period, close fiscal year, bank account detailed trial balance
ms.date: 04/01/2020
ms.author: jswymer
ms.openlocfilehash: 1fa624ecda5914c0ba4e395025f051bc5d8cc457
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2020
ms.locfileid: "3191737"
---
# <a name="post-the-year-end-closing-entry"></a><span data-ttu-id="9920d-103">Bóka lokafærslu ársloka</span><span class="sxs-lookup"><span data-stu-id="9920d-103">Post the Year-End Closing Entry</span></span>
<span data-ttu-id="9920d-104">Eftir að runuvinnslan **Loka rekstrarreikningi** hefur verið notuð til að mynda færslu eða færslur fyrir lokun í árslok verður að opna færslubókina sem var tilgreind í runuvinnslunni,  og fara yfir og bóka færslurnar.</span><span class="sxs-lookup"><span data-stu-id="9920d-104">After you use the **Close Income Statement** batch job to generate the year-end closing entry or entries, you must open the journal you specified in the batch job, and then review and post the entries.</span></span>

## <a name="to-post-the-year-end-closing-entry"></a><span data-ttu-id="9920d-105">Til að bóka lokunarfærslu ársloka</span><span class="sxs-lookup"><span data-stu-id="9920d-105">To post the year end closing entry</span></span>
1. <span data-ttu-id="9920d-106">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Færslubók** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="9920d-106">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **General Journal**, and then choose the related link.</span></span>
2. <span data-ttu-id="9920d-107">Á síðunni **almenn færslubók** í reitnum **Heiti keyrslu** er keyrslan sem inniheldur lokunarfærslurnar valin.</span><span class="sxs-lookup"><span data-stu-id="9920d-107">On the **General Journal** page, in the **Batch Name** field, select the batch that contains the closing entries.</span></span>
3. <span data-ttu-id="9920d-108">Farið er yfir færslurnar.</span><span class="sxs-lookup"><span data-stu-id="9920d-108">Review the entries.</span></span>
4. <span data-ttu-id="9920d-109">Til að bóka færslubókina er valið aðgerðin **bóka**.</span><span class="sxs-lookup"><span data-stu-id="9920d-109">To post the journal, choose the **Post** action.</span></span>

> [!NOTE]  
>   <span data-ttu-id="9920d-110">Greinist villa birtast villuboð.</span><span class="sxs-lookup"><span data-stu-id="9920d-110">If an error is detected, an error message is displayed.</span></span> <span data-ttu-id="9920d-111">Ef bókunin heppnast eru bókaðar færslur fjarlægðar úr færslubókinni.</span><span class="sxs-lookup"><span data-stu-id="9920d-111">If the posting is successful, the posted entries are removed from the journal.</span></span> <span data-ttu-id="9920d-112">Þegar færsla hefur verið bókuð er hún bókuð á alla rekstrarreikninga til að staðan verði núll, og útkoma ársins er færð á efnahagsreikning.</span><span class="sxs-lookup"><span data-stu-id="9920d-112">After posting is complete, an entry is posted to each income statement account so that its balance becomes zero and the year's result is transferred to the balance sheet.</span></span>

## <a name="see-also"></a><span data-ttu-id="9920d-113">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="9920d-113">See Also</span></span>
[<span data-ttu-id="9920d-114">Loka fjárhagstímabilum</span><span class="sxs-lookup"><span data-stu-id="9920d-114">Close Accounting Periods</span></span>](year-close-account-periods.md)  
[<span data-ttu-id="9920d-115">Bókum lokað</span><span class="sxs-lookup"><span data-stu-id="9920d-115">Closing Books</span></span>](year-close-books.md)  
[<span data-ttu-id="9920d-116">Loka rekstrarreikningi</span><span class="sxs-lookup"><span data-stu-id="9920d-116">Close Income Statement</span></span>](year-close-income-statement.md)  
<span data-ttu-id="9920d-117">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="9920d-117">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
