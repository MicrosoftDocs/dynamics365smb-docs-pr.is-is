---
title: "Loka fjárhagstímabilum fyrir fjárhagsár | Microsoft Docs"
description: "Lýsir því hvernig skal loka fjárhagstímabilum sem mynda fjárhagsárið."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: year closing, close accounting period, close fiscal year, bank account detailed trial balance
ms.date: 06/02/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 23a9cd7a8a7f579f63937ac4fc28e6d4958f3f9a
ms.contentlocale: is-is
ms.lasthandoff: 03/22/2018

---
# <a name="close-accounting-periods"></a><span data-ttu-id="604de-103">Loka fjárhagstímabilum</span><span class="sxs-lookup"><span data-stu-id="604de-103">Close Accounting Periods</span></span>
<span data-ttu-id="604de-104">Þegar reikningsári er lokið þarf að loka tímabilunum sem það skiptist í.</span><span class="sxs-lookup"><span data-stu-id="604de-104">When a fiscal year is over, you must close the periods that comprise it.</span></span>

## <a name="to-close-accounting-periods"></a><span data-ttu-id="604de-105">Fjárhagstímabilum lokað:</span><span class="sxs-lookup"><span data-stu-id="604de-105">To close accounting periods</span></span>
1. <span data-ttu-id="604de-106">Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Reikningstímabil** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="604de-106">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Accounting Periods**, and then choose the related link.</span></span>
2. <span data-ttu-id="604de-107">Í glugganum **Reikningstímabil** skal velja **loka ári** aðgerðina.</span><span class="sxs-lookup"><span data-stu-id="604de-107">In the **Accounting Periods** window, choose the **Close Year** action.</span></span>

    <span data-ttu-id="604de-108">Ef fleiri en eitt reikningsár er opið elsta er að elsta sjálfkrafa valið til að vera lokað.</span><span class="sxs-lookup"><span data-stu-id="604de-108">If more than one fiscal year is open, the earliest one is automatically selected to be closed.</span></span> <span data-ttu-id="604de-109">Það birtir boð með árinu sem á að loka þar sem er útskýrt hvað gerist ef árinu er lokað.</span><span class="sxs-lookup"><span data-stu-id="604de-109">A message displays identifying the year that will close and the consequences of closing the year.</span></span>
3. <span data-ttu-id="604de-110">Til að loka árinu skal velja hnappinn **Já**.</span><span class="sxs-lookup"><span data-stu-id="604de-110">To close the year, choose the **Yes** button.</span></span>

<span data-ttu-id="604de-111">Reikningsárið er lokað og reitirnir **Lokað** og **Dags. læst** fyrir öll tímabil á árinu eru valdir.</span><span class="sxs-lookup"><span data-stu-id="604de-111">The fiscal year is closed, and the **Closed** and **Date Locked** fields for all the periods in the year are selected.</span></span> <span data-ttu-id="604de-112">Ekki er lengur hægt að opna reikningsárið eða fjarlægja gátmerkið í reitunum **Læst** eða **Dags. læst**.</span><span class="sxs-lookup"><span data-stu-id="604de-112">The fiscal year cannot be opened again and you cannot remove the check mark from the **Closed** or **Date Locked** fields.</span></span>

> [!NOTE]  
>   <span data-ttu-id="604de-113">Ekki er hægt að loka reikningsári fyrr en nýtt hefur verið stofnað.</span><span class="sxs-lookup"><span data-stu-id="604de-113">You cannot close a fiscal year before you create a new one.</span></span> <span data-ttu-id="604de-114">Bent er á að þegar fjárhagssári hefur verið lokað er ekki hægt að breyta upphafsdagsetningu næsta fjárhagsárs.</span><span class="sxs-lookup"><span data-stu-id="604de-114">Notice that when a fiscal year has been closed, you cannot change the starting date of the following fiscal year.</span></span>

<span data-ttu-id="604de-115">Enda þótt reikningsári hafi verið lokað er enn hægt að bóka fjárhagsfærslur á það.</span><span class="sxs-lookup"><span data-stu-id="604de-115">Even though a fiscal year has been closed, you can still post general ledger entries to it.</span></span> <span data-ttu-id="604de-116">Þegar það er gert eru færslurnar merktar sem bókaðar á lokað reikningsár og reiturinn **seinfærsla** verður valinn.</span><span class="sxs-lookup"><span data-stu-id="604de-116">When you do this, the entries will be marked as posted to a closed fiscal year and the **Prior-Year Entry** field will be selected.</span></span>

<span data-ttu-id="604de-117">Þegar reikningsári hefur verið lokað verður að loka reikningum á rekstrarreikningi og færa ársniðurstöður yfir á reikning á efnahagsreikningi.</span><span class="sxs-lookup"><span data-stu-id="604de-117">After a fiscal year is closed, you must close the income statement accounts and transfer the year's results to an account in the balance sheet.</span></span> <span data-ttu-id="604de-118">Hægt er að endurtaka þetta í hvert sinn sem lokaða reikningsárið er bókað.</span><span class="sxs-lookup"><span data-stu-id="604de-118">You can repeat this every time that you post to the closed fiscal year.</span></span>

## <a name="see-also"></a><span data-ttu-id="604de-119">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="604de-119">See Also</span></span>
[<span data-ttu-id="604de-120">Bókum lokað</span><span class="sxs-lookup"><span data-stu-id="604de-120">Closing Books</span></span>](year-close-books.md)  
[<span data-ttu-id="604de-121">Bóka lokafærslu ársloka</span><span class="sxs-lookup"><span data-stu-id="604de-121">Post the Year-End Closing Entry</span></span>](year-how-post-year-end-close-entry.md)  
[<span data-ttu-id="604de-122">Opna nýtt reikningsár</span><span class="sxs-lookup"><span data-stu-id="604de-122">Open a New Fiscal Year</span></span>](finance-how-open-new-fiscal-year.md)  
<span data-ttu-id="604de-123">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="604de-123">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

