---
title: Bóka lokafærslu ársloka
description: Lýsir því hvernig skal opna færslubókina sem þú tilgreindir í runuvinnslunni Loka rekstrarreikningi, og svo endurskoða og bóka lokafærslu ársloka.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: year closing, close accounting period, close fiscal year, bank account detailed trial balance
ms.date: 02/23/2021
ms.author: edupont
ms.openlocfilehash: 728a3edc1ef2200d4f28130cad6653d6b26a5b3b
ms.sourcegitcommit: a9d48272ce61e5d512a30417412b5363e56abf30
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/04/2021
ms.locfileid: "5493354"
---
# <a name="post-the-year-end-closing-entry"></a><span data-ttu-id="2c7d4-103">Bóka lokafærslu ársloka</span><span class="sxs-lookup"><span data-stu-id="2c7d4-103">Post the Year-End Closing Entry</span></span>

<span data-ttu-id="2c7d4-104">Eftir að runuvinnslan **Loka rekstrarreikningi** hefur verið notuð til að mynda færslu eða færslur fyrir lokun í árslok verður að opna færslubókina sem var tilgreind í runuvinnslunni,  og fara yfir og bóka færslurnar.</span><span class="sxs-lookup"><span data-stu-id="2c7d4-104">After you use the **Close Income Statement** batch job to generate the year-end closing entry or entries, you must open the journal you specified in the batch job, and then review and post the entries.</span></span>  

> [!TIP]
> <span data-ttu-id="2c7d4-105">Hægt er að velja að loka eða ekki loka reikningstímabilum og fjárhagsárum í [!INCLUDE [prod_short](includes/prod_short.md)], allt eftir verkferlum fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="2c7d4-105">Depending on your organizations work processes, you can choose to close or not close accounting periods and fiscal years in [!INCLUDE [prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="2c7d4-106">Eftirfarandi ferli gerir ráð fyrir að fjárhagsárinu hafi verið lokað með valkostinum *Reikningstímabil*, að lokunarfærsla ársloka hafi verið búin til með runuvinnslunni **Loka rekstrarreikningi** og að nú sé hægt að bóka lokunarfærslu í árslok ásamt jöfnun á færslum á lykli eigin fjár.</span><span class="sxs-lookup"><span data-stu-id="2c7d4-106">The following procedure assumes that you have closed the fiscal year using the *Accounting Periods* option, generated a year-end closing entry using the **Close Income Statement** batch job, and are now ready to post the year-end closing entry along with the offsetting equity account entries.</span></span> <span data-ttu-id="2c7d4-107">Fyrirtækið getur valið að vinna á annan hátt, svo sem með því að bóka lokunarfærslu árslokanna sem hluta af lokun fjárhagsársins.</span><span class="sxs-lookup"><span data-stu-id="2c7d4-107">Your organization can choose to work differently, such as post the year-end closing entry as part of closing the fiscal year.</span></span>

## <a name="to-post-the-year-end-closing-entry"></a><span data-ttu-id="2c7d4-108">Til að bóka lokunarfærslu ársloka</span><span class="sxs-lookup"><span data-stu-id="2c7d4-108">To post the year end closing entry</span></span>

1. <span data-ttu-id="2c7d4-109">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Færslubók** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="2c7d4-109">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **General Journal**, and then choose the related link.</span></span>
2. <span data-ttu-id="2c7d4-110">Á síðunni **almenn færslubók** í reitnum **Heiti keyrslu** er keyrslan sem inniheldur lokunarfærslurnar valin.</span><span class="sxs-lookup"><span data-stu-id="2c7d4-110">On the **General Journal** page, in the **Batch Name** field, select the batch that contains the closing entries.</span></span>
3. <span data-ttu-id="2c7d4-111">Farið er yfir færslurnar.</span><span class="sxs-lookup"><span data-stu-id="2c7d4-111">Review the entries.</span></span>
4. <span data-ttu-id="2c7d4-112">Til að bóka færslubókina er valið aðgerðin **bóka**.</span><span class="sxs-lookup"><span data-stu-id="2c7d4-112">To post the journal, choose the **Post** action.</span></span>

> [!NOTE]  
> <span data-ttu-id="2c7d4-113">Greinist villa birtast villuboð.</span><span class="sxs-lookup"><span data-stu-id="2c7d4-113">If an error is detected, an error message is displayed.</span></span> <span data-ttu-id="2c7d4-114">Ef bókunin heppnast eru bókaðar færslur fjarlægðar úr færslubókinni.</span><span class="sxs-lookup"><span data-stu-id="2c7d4-114">If the posting is successful, the posted entries are removed from the journal.</span></span> <span data-ttu-id="2c7d4-115">Þegar færsla hefur verið bókuð er hún bókuð á alla rekstrarreikninga til að staðan verði núll, og útkoma ársins er færð á efnahagsreikning.</span><span class="sxs-lookup"><span data-stu-id="2c7d4-115">After posting is complete, an entry is posted to each income statement account so that its balance becomes zero and the year's result is transferred to the balance sheet.</span></span>

## <a name="see-also"></a><span data-ttu-id="2c7d4-116">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="2c7d4-116">See Also</span></span>

[<span data-ttu-id="2c7d4-117">Loka fjárhagstímabilum</span><span class="sxs-lookup"><span data-stu-id="2c7d4-117">Close Accounting Periods</span></span>](year-close-account-periods.md)  
[<span data-ttu-id="2c7d4-118">Bókum lokað</span><span class="sxs-lookup"><span data-stu-id="2c7d4-118">Closing Books</span></span>](year-close-books.md)  
[<span data-ttu-id="2c7d4-119">Loka rekstrarreikningi</span><span class="sxs-lookup"><span data-stu-id="2c7d4-119">Close Income Statement</span></span>](year-close-income-statement.md)  
<span data-ttu-id="2c7d4-120">[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="2c7d4-120">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]