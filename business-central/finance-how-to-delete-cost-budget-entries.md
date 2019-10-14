---
title: Hvernig skal eyða kostnaðaráætlunarfærslum | Microsoft Docs
description: Eyða kostnaðaráætlunarfærslum Keyrslan er notuð til að afturkalla kostnaðaráætlunarfærslur í kostnaðaráætlunardagbókinni.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: a20895b02b00c64261e0a318949e2ba83bd15a56
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/01/2019
ms.locfileid: "2302054"
---
# <a name="delete-cost-budget-entries"></a><span data-ttu-id="2f8d5-103">Eyða kostnaðaráætlunarfærslum</span><span class="sxs-lookup"><span data-stu-id="2f8d5-103">Delete Cost Budget Entries</span></span>
<span data-ttu-id="2f8d5-104">**Eyða kostnaðaráætlunarfærslum** Keyrslan er notuð til að afturkalla kostnaðaráætlunarfærslur í kostnaðaráætlunardagbókinni.</span><span class="sxs-lookup"><span data-stu-id="2f8d5-104">You use the **Delete Cost Budget Entries** batch job to cancel cost budget entries from the cost budget register.</span></span>  

<span data-ttu-id="2f8d5-105">Til að koma í veg fyrir gloppur í kostnaðaráætlunarfærslum og kostnaðarskrám ekki er hægt að eyða eina færslu eða runu færslna í miðjum lista yfir færslur í skrá.</span><span class="sxs-lookup"><span data-stu-id="2f8d5-105">To prevent any gaps in the cost budget entries and cost register entries, you cannot delete a single entry or a batch of entries in the middle of the list of register entries.</span></span>  

### <a name="to-delete-a-cost-budget-entry"></a><span data-ttu-id="2f8d5-106">Til að úthluta kostnaðaráætlunarfærslu</span><span class="sxs-lookup"><span data-stu-id="2f8d5-106">To delete a cost budget entry</span></span>  

1.  <span data-ttu-id="2f8d5-107">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Eyða kostnaðaráætlanafærslum** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="2f8d5-107">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Delete Cost Budget Entries**, and then choose the related link.</span></span>  

    <span data-ttu-id="2f8d5-108">**Skráningarnr.**</span><span class="sxs-lookup"><span data-stu-id="2f8d5-108">The **To Register No.**</span></span> <span data-ttu-id="2f8d5-109">reiturinn felur í sér síðasta skráningarfærslunúmerið og því er ekki hægt að breyta.</span><span class="sxs-lookup"><span data-stu-id="2f8d5-109">field contains the last register entry number and cannot be changed.</span></span>  

    <span data-ttu-id="2f8d5-110">Hægt er að nota reitinn **Frá skráningarnr.**</span><span class="sxs-lookup"><span data-stu-id="2f8d5-110">You can use the **From Register No.**</span></span> <span data-ttu-id="2f8d5-111">til að velja skráningarfærslunúmer þar sem eyðing á að hefjast.</span><span class="sxs-lookup"><span data-stu-id="2f8d5-111">field to select a register entry number from which the deletion should begin.</span></span>  
2.  <span data-ttu-id="2f8d5-112">Velja hnappinn **Í lagi** til að eyða völdum færslum kostnaðaráætlana.</span><span class="sxs-lookup"><span data-stu-id="2f8d5-112">Choose the **OK** button to delete the selected cost budget entries.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="2f8d5-113">Til að forðast að eyða kostnaðaráætlunarfærslum fyrir slysni er hægt að loka skráningarfærslum með því að merkja línurnar sem **Lokað** í reitnum **Lokað** á síðunni **Fjárhagsáætlunarskrár**.</span><span class="sxs-lookup"><span data-stu-id="2f8d5-113">To avoid an accidental deletion of cost budget entries, you can close register entries by marking the lines as **Closed** in the **Closed** field on the **Cost Budget Registers** page.</span></span>  

## <a name="see-also"></a><span data-ttu-id="2f8d5-114">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="2f8d5-114">See Also</span></span>  
<span data-ttu-id="2f8d5-115">[Kostnaðarbókhald](finance-manage-cost-accounting.md)
[Stofna kostnaðaráætlun](finance-create-cost-budgets.md)</span><span class="sxs-lookup"><span data-stu-id="2f8d5-115">[Accounting for Costs](finance-manage-cost-accounting.md)
[Creating Cost Budgets](finance-create-cost-budgets.md)</span></span>  
<span data-ttu-id="2f8d5-116">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="2f8d5-116">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
