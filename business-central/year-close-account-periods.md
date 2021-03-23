---
title: Loka fjárhagstímabilum fyrir fjárhagsár | Microsoft Docs
description: Lýsir því hvernig skal loka fjárhagstímabilum sem mynda fjárhagsárið.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: year closing, close accounting period, close fiscal year, bank account detailed trial balance
ms.date: 10/01/2020
ms.author: jswymer
ms.openlocfilehash: 336c6c8a4596aae26846d6a06091b6f5c4fff970
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5386275"
---
# <a name="close-accounting-periods"></a><span data-ttu-id="9977d-103">Loka fjárhagstímabilum</span><span class="sxs-lookup"><span data-stu-id="9977d-103">Close Accounting Periods</span></span>
<span data-ttu-id="9977d-104">Þegar reikningsári er lokið þarf að loka tímabilunum sem það skiptist í.</span><span class="sxs-lookup"><span data-stu-id="9977d-104">When a fiscal year is over, you must close the periods that comprise it.</span></span>

## <a name="to-close-accounting-periods"></a><span data-ttu-id="9977d-105">Fjárhagstímabilum lokað:</span><span class="sxs-lookup"><span data-stu-id="9977d-105">To close accounting periods</span></span>
1. <span data-ttu-id="9977d-106">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Fjárhagstímabil** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="9977d-106">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Accounting Periods**, and then choose the related link.</span></span>
2. <span data-ttu-id="9977d-107">Á síðunni **Fjárhagstímabil** skal velja aðgerðina **Loka ári**.</span><span class="sxs-lookup"><span data-stu-id="9977d-107">On the **Accounting Periods** page, choose the **Close Year** action.</span></span>

    <span data-ttu-id="9977d-108">Ef fleiri en eitt reikningsár er opið elsta er að elsta sjálfkrafa valið til að vera lokað.</span><span class="sxs-lookup"><span data-stu-id="9977d-108">If more than one fiscal year is open, the earliest one is automatically selected to be closed.</span></span> <span data-ttu-id="9977d-109">Það birtir boð með árinu sem á að loka þar sem er útskýrt hvað gerist ef árinu er lokað.</span><span class="sxs-lookup"><span data-stu-id="9977d-109">A message displays identifying the year that will close and the consequences of closing the year.</span></span>
3. <span data-ttu-id="9977d-110">Til að loka árinu skal velja hnappinn **Já**.</span><span class="sxs-lookup"><span data-stu-id="9977d-110">To close the year, choose the **Yes** button.</span></span>

<span data-ttu-id="9977d-111">Reikningsárið er lokað og reitirnir **Lokað** og **Dags. læst** fyrir öll tímabil á árinu eru valdir.</span><span class="sxs-lookup"><span data-stu-id="9977d-111">The fiscal year is closed, and the **Closed** and **Date Locked** fields for all the periods in the year are selected.</span></span> <span data-ttu-id="9977d-112">Ekki er lengur hægt að opna reikningsárið eða fjarlægja gátmerkið í reitunum **Læst** eða **Dags. læst**.</span><span class="sxs-lookup"><span data-stu-id="9977d-112">The fiscal year cannot be opened again and you cannot remove the check mark from the **Closed** or **Date Locked** fields.</span></span>

> [!NOTE]  
>   <span data-ttu-id="9977d-113">Ekki er hægt að loka reikningsári fyrr en nýtt hefur verið stofnað.</span><span class="sxs-lookup"><span data-stu-id="9977d-113">You cannot close a fiscal year before you create a new one.</span></span> <span data-ttu-id="9977d-114">Bent er á að þegar fjárhagssári hefur verið lokað er ekki hægt að breyta upphafsdagsetningu næsta fjárhagsárs.</span><span class="sxs-lookup"><span data-stu-id="9977d-114">Notice that when a fiscal year has been closed, you cannot change the starting date of the following fiscal year.</span></span>

<span data-ttu-id="9977d-115">Enda þótt reikningsári hafi verið lokað er enn hægt að bóka fjárhagsfærslur á það.</span><span class="sxs-lookup"><span data-stu-id="9977d-115">Even though a fiscal year has been closed, you can still post general ledger entries to it.</span></span> <span data-ttu-id="9977d-116">Þegar það er gert eru færslurnar merktar sem bókaðar á lokað reikningsár og reiturinn **seinfærsla** verður valinn.</span><span class="sxs-lookup"><span data-stu-id="9977d-116">When you do this, the entries will be marked as posted to a closed fiscal year and the **Prior-Year Entry** field will be selected.</span></span>

<span data-ttu-id="9977d-117">Þegar reikningsári hefur verið lokað verður að loka reikningum á rekstrarreikningi og færa ársniðurstöður yfir á reikning á efnahagsreikningi.</span><span class="sxs-lookup"><span data-stu-id="9977d-117">After a fiscal year is closed, you must close the income statement accounts and transfer the year's results to an account in the balance sheet.</span></span> <span data-ttu-id="9977d-118">Hægt er að endurtaka þetta í hvert sinn sem lokaða reikningsárið er bókað.</span><span class="sxs-lookup"><span data-stu-id="9977d-118">You can repeat this every time that you post to the closed fiscal year.</span></span>

## <a name="see-also"></a><span data-ttu-id="9977d-119">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="9977d-119">See Also</span></span>

[<span data-ttu-id="9977d-120">Bókum lokað</span><span class="sxs-lookup"><span data-stu-id="9977d-120">Closing Books</span></span>](year-close-books.md)  
[<span data-ttu-id="9977d-121">Bóka lokafærslu ársloka</span><span class="sxs-lookup"><span data-stu-id="9977d-121">Post the Year-End Closing Entry</span></span>](year-how-post-year-end-close-entry.md)  
[<span data-ttu-id="9977d-122">Unnið með fjárhagstímabil og fjárhagsár</span><span class="sxs-lookup"><span data-stu-id="9977d-122">Work with Accounting Periods and Fiscal Years</span></span>](finance-accounting-periods-and-fiscal-years.md)  
<span data-ttu-id="9977d-123">[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="9977d-123">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]