---
title: "Hvernig skal eyða kostnaðaráætlunarfærslum | Microsoft Docs"
description: "**Eyða kostnaðaráætlunarfærslum** Keyrslan er notuð til að afturkalla kostnaðaráætlunarfærslur í kostnaðaráætlunardagbókinni."
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
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: cdd7f7cfb2645d780df47bfb75ec7392c1739843
ms.contentlocale: is-is
ms.lasthandoff: 09/28/2018

---
# <a name="delete-cost-budget-entries"></a><span data-ttu-id="fc7ad-103">Eyða kostnaðaráætlunarfærslum</span><span class="sxs-lookup"><span data-stu-id="fc7ad-103">Delete Cost Budget Entries</span></span>
<span data-ttu-id="fc7ad-104">**Eyða kostnaðaráætlunarfærslum** Keyrslan er notuð til að afturkalla kostnaðaráætlunarfærslur í kostnaðaráætlunardagbókinni.</span><span class="sxs-lookup"><span data-stu-id="fc7ad-104">You use the **Delete Cost Budget Entries** batch job to cancel cost budget entries from the cost budget register.</span></span>  

<span data-ttu-id="fc7ad-105">Til að koma í veg fyrir gloppur í kostnaðaráætlunarfærslum og kostnaðarskrám ekki er hægt að eyða eina færslu eða runu færslna í miðjum lista yfir færslur í skrá.</span><span class="sxs-lookup"><span data-stu-id="fc7ad-105">To prevent any gaps in the cost budget entries and cost register entries, you cannot delete a single entry or a batch of entries in the middle of the list of register entries.</span></span>  

### <a name="to-delete-a-cost-budget-entry"></a><span data-ttu-id="fc7ad-106">Til að úthluta kostnaðaráætlunarfærslu</span><span class="sxs-lookup"><span data-stu-id="fc7ad-106">To delete a cost budget entry</span></span>  

1.  <span data-ttu-id="fc7ad-107">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Eyða kostnaðaráætlanafærslum** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="fc7ad-107">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Delete Cost Budget Entries**, and then choose the related link.</span></span>  

    <span data-ttu-id="fc7ad-108">**Skráningarnr.**</span><span class="sxs-lookup"><span data-stu-id="fc7ad-108">The **To Register No.**</span></span> <span data-ttu-id="fc7ad-109">reiturinn felur í sér síðasta skráningarfærslunúmerið og því er ekki hægt að breyta.</span><span class="sxs-lookup"><span data-stu-id="fc7ad-109">field contains the last register entry number and cannot be changed.</span></span>  

    <span data-ttu-id="fc7ad-110">Hægt er að nota reitinn **Frá skráningarnr.**</span><span class="sxs-lookup"><span data-stu-id="fc7ad-110">You can use the **From Register No.**</span></span> <span data-ttu-id="fc7ad-111">til að velja skráningarfærslunúmer þar sem eyðing á að hefjast.</span><span class="sxs-lookup"><span data-stu-id="fc7ad-111">field to select a register entry number from which the deletion should begin.</span></span>  
2.  <span data-ttu-id="fc7ad-112">Velja hnappinn **Í lagi** til að eyða völdum færslum kostnaðaráætlana.</span><span class="sxs-lookup"><span data-stu-id="fc7ad-112">Choose the **OK** button to delete the selected cost budget entries.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="fc7ad-113">Til að forðast að eyða kostnaðaráætlunarfærslum fyrir slysni er hægt að loka skráningarfærslum með því að merkja línurnar sem **Lokað** í reitnum **Lokað** í glugganum **Fjárhagsáætlunarskrár**.</span><span class="sxs-lookup"><span data-stu-id="fc7ad-113">To avoid an accidental deletion of cost budget entries, you can close register entries by marking the lines as **Closed** in the **Closed** field in the **Cost Budget Registers** window.</span></span>  

## <a name="see-also"></a><span data-ttu-id="fc7ad-114">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="fc7ad-114">See Also</span></span>  
<span data-ttu-id="fc7ad-115">[Kostnaðarbókhald](finance-manage-cost-accounting.md)
[Stofna kostnaðaráætlun](finance-create-cost-budgets.md)</span><span class="sxs-lookup"><span data-stu-id="fc7ad-115">[Accounting for Costs](finance-manage-cost-accounting.md)
[Creating Cost Budgets](finance-create-cost-budgets.md)</span></span>  
<span data-ttu-id="fc7ad-116">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="fc7ad-116">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

