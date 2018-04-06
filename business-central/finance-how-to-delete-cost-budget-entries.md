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
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: acd8e0f25a3909ceab3dd63e04509ab48a300bb6
ms.contentlocale: is-is
ms.lasthandoff: 03/22/2018

---
# <a name="delete-cost-budget-entries"></a><span data-ttu-id="ff6af-103">Eyða kostnaðaráætlunarfærslum</span><span class="sxs-lookup"><span data-stu-id="ff6af-103">Delete Cost Budget Entries</span></span>
<span data-ttu-id="ff6af-104">**Eyða kostnaðaráætlunarfærslum** Keyrslan er notuð til að afturkalla kostnaðaráætlunarfærslur í kostnaðaráætlunardagbókinni.</span><span class="sxs-lookup"><span data-stu-id="ff6af-104">You use the **Delete Cost Budget Entries** batch job to cancel cost budget entries from the cost budget register.</span></span>  

<span data-ttu-id="ff6af-105">Til að koma í veg fyrir gloppur í kostnaðaráætlunarfærslum og kostnaðarskrám ekki er hægt að eyða eina færslu eða runu færslna í miðjum lista yfir færslur í skrá.</span><span class="sxs-lookup"><span data-stu-id="ff6af-105">To prevent any gaps in the cost budget entries and cost register entries, you cannot delete a single entry or a batch of entries in the middle of the list of register entries.</span></span>  

### <a name="to-delete-a-cost-budget-entry"></a><span data-ttu-id="ff6af-106">Til að úthluta kostnaðaráætlunarfærslu</span><span class="sxs-lookup"><span data-stu-id="ff6af-106">To delete a cost budget entry</span></span>  

1.  <span data-ttu-id="ff6af-107">Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Eyða kostnaðaráætlunarfærslum** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="ff6af-107">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Delete Cost Budget Entries**, and then choose the related link.</span></span>  

    <span data-ttu-id="ff6af-108">**Skráningarnr.**</span><span class="sxs-lookup"><span data-stu-id="ff6af-108">The **To Register No.**</span></span> <span data-ttu-id="ff6af-109">reiturinn felur í sér síðasta skráningarfærslunúmerið og því er ekki hægt að breyta.</span><span class="sxs-lookup"><span data-stu-id="ff6af-109">field contains the last register entry number and cannot be changed.</span></span>  

    <span data-ttu-id="ff6af-110">Hægt er að nota reitinn **Frá skráningarnr.**</span><span class="sxs-lookup"><span data-stu-id="ff6af-110">You can use the **From Register No.**</span></span> <span data-ttu-id="ff6af-111">til að velja skráningarfærslunúmer þar sem eyðing á að hefjast.</span><span class="sxs-lookup"><span data-stu-id="ff6af-111">field to select a register entry number from which the deletion should begin.</span></span>  
2.  <span data-ttu-id="ff6af-112">Velja hnappinn **Í lagi** til að eyða völdum færslum kostnaðaráætlana.</span><span class="sxs-lookup"><span data-stu-id="ff6af-112">Choose the **OK** button to delete the selected cost budget entries.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="ff6af-113">Til að forðast að eyða kostnaðaráætlunarfærslum fyrir slysni er hægt að loka skráningarfærslum með því að merkja línurnar sem **Lokað** í reitnum **Lokað** í glugganum **Fjárhagsáætlunarskrár**.</span><span class="sxs-lookup"><span data-stu-id="ff6af-113">To avoid an accidental deletion of cost budget entries, you can close register entries by marking the lines as **Closed** in the **Closed** field in the **Cost Budget Registers** window.</span></span>  

## <a name="see-also"></a><span data-ttu-id="ff6af-114">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="ff6af-114">See Also</span></span>  
<span data-ttu-id="ff6af-115">[Kostnaðarbókhald](finance-manage-cost-accounting.md)
[Stofna kostnaðaráætlun](finance-create-cost-budgets.md)</span><span class="sxs-lookup"><span data-stu-id="ff6af-115">[Accounting for Costs](finance-manage-cost-accounting.md)
[Creating Cost Budgets](finance-create-cost-budgets.md)</span></span>  
<span data-ttu-id="ff6af-116">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="ff6af-116">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

