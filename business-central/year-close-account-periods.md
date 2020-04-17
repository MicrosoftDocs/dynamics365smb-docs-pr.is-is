---
title: Loka fjárhagstímabilum fyrir fjárhagsár | Microsoft Docs
description: Lýsir því hvernig skal loka fjárhagstímabilum sem mynda fjárhagsárið.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: year closing, close accounting period, close fiscal year, bank account detailed trial balance
ms.date: 04/01/2020
ms.author: jswymer
ms.openlocfilehash: a696f45446f93dba2dedb0976ff646dd6e4b12b1
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2020
ms.locfileid: "3195876"
---
# <a name="close-accounting-periods"></a><span data-ttu-id="d0e54-103">Loka fjárhagstímabilum</span><span class="sxs-lookup"><span data-stu-id="d0e54-103">Close Accounting Periods</span></span>
<span data-ttu-id="d0e54-104">Þegar reikningsári er lokið þarf að loka tímabilunum sem það skiptist í.</span><span class="sxs-lookup"><span data-stu-id="d0e54-104">When a fiscal year is over, you must close the periods that comprise it.</span></span>

## <a name="to-close-accounting-periods"></a><span data-ttu-id="d0e54-105">Fjárhagstímabilum lokað:</span><span class="sxs-lookup"><span data-stu-id="d0e54-105">To close accounting periods</span></span>
1. <span data-ttu-id="d0e54-106">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Fjárhagstímabil** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="d0e54-106">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Accounting Periods**, and then choose the related link.</span></span>
2. <span data-ttu-id="d0e54-107">Á síðunni **Fjárhagstímabil** skal velja aðgerðina **Loka ári**.</span><span class="sxs-lookup"><span data-stu-id="d0e54-107">On the **Accounting Periods** page, choose the **Close Year** action.</span></span>

    <span data-ttu-id="d0e54-108">Ef fleiri en eitt reikningsár er opið elsta er að elsta sjálfkrafa valið til að vera lokað.</span><span class="sxs-lookup"><span data-stu-id="d0e54-108">If more than one fiscal year is open, the earliest one is automatically selected to be closed.</span></span> <span data-ttu-id="d0e54-109">Það birtir boð með árinu sem á að loka þar sem er útskýrt hvað gerist ef árinu er lokað.</span><span class="sxs-lookup"><span data-stu-id="d0e54-109">A message displays identifying the year that will close and the consequences of closing the year.</span></span>
3. <span data-ttu-id="d0e54-110">Til að loka árinu skal velja hnappinn **Já**.</span><span class="sxs-lookup"><span data-stu-id="d0e54-110">To close the year, choose the **Yes** button.</span></span>

<span data-ttu-id="d0e54-111">Reikningsárið er lokað og reitirnir **Lokað** og **Dags. læst** fyrir öll tímabil á árinu eru valdir.</span><span class="sxs-lookup"><span data-stu-id="d0e54-111">The fiscal year is closed, and the **Closed** and **Date Locked** fields for all the periods in the year are selected.</span></span> <span data-ttu-id="d0e54-112">Ekki er lengur hægt að opna reikningsárið eða fjarlægja gátmerkið í reitunum **Læst** eða **Dags. læst**.</span><span class="sxs-lookup"><span data-stu-id="d0e54-112">The fiscal year cannot be opened again and you cannot remove the check mark from the **Closed** or **Date Locked** fields.</span></span>

> [!NOTE]  
>   <span data-ttu-id="d0e54-113">Ekki er hægt að loka reikningsári fyrr en nýtt hefur verið stofnað.</span><span class="sxs-lookup"><span data-stu-id="d0e54-113">You cannot close a fiscal year before you create a new one.</span></span> <span data-ttu-id="d0e54-114">Bent er á að þegar fjárhagssári hefur verið lokað er ekki hægt að breyta upphafsdagsetningu næsta fjárhagsárs.</span><span class="sxs-lookup"><span data-stu-id="d0e54-114">Notice that when a fiscal year has been closed, you cannot change the starting date of the following fiscal year.</span></span>

<span data-ttu-id="d0e54-115">Enda þótt reikningsári hafi verið lokað er enn hægt að bóka fjárhagsfærslur á það.</span><span class="sxs-lookup"><span data-stu-id="d0e54-115">Even though a fiscal year has been closed, you can still post general ledger entries to it.</span></span> <span data-ttu-id="d0e54-116">Þegar það er gert eru færslurnar merktar sem bókaðar á lokað reikningsár og reiturinn **seinfærsla** verður valinn.</span><span class="sxs-lookup"><span data-stu-id="d0e54-116">When you do this, the entries will be marked as posted to a closed fiscal year and the **Prior-Year Entry** field will be selected.</span></span>

<span data-ttu-id="d0e54-117">Þegar reikningsári hefur verið lokað verður að loka reikningum á rekstrarreikningi og færa ársniðurstöður yfir á reikning á efnahagsreikningi.</span><span class="sxs-lookup"><span data-stu-id="d0e54-117">After a fiscal year is closed, you must close the income statement accounts and transfer the year's results to an account in the balance sheet.</span></span> <span data-ttu-id="d0e54-118">Hægt er að endurtaka þetta í hvert sinn sem lokaða reikningsárið er bókað.</span><span class="sxs-lookup"><span data-stu-id="d0e54-118">You can repeat this every time that you post to the closed fiscal year.</span></span>

## <a name="see-also"></a><span data-ttu-id="d0e54-119">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="d0e54-119">See Also</span></span>

[<span data-ttu-id="d0e54-120">Bókum lokað</span><span class="sxs-lookup"><span data-stu-id="d0e54-120">Closing Books</span></span>](year-close-books.md)  
[<span data-ttu-id="d0e54-121">Bóka lokafærslu ársloka</span><span class="sxs-lookup"><span data-stu-id="d0e54-121">Post the Year-End Closing Entry</span></span>](year-how-post-year-end-close-entry.md)  
[<span data-ttu-id="d0e54-122">Unnið með fjárhagstímabil og fjárhagsár</span><span class="sxs-lookup"><span data-stu-id="d0e54-122">Work with Accounting Periods and Fiscal Years</span></span>](finance-accounting-periods-and-fiscal-years.md)  
<span data-ttu-id="d0e54-123">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="d0e54-123">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
