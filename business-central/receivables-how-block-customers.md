---
title: Hvernig á að loka fyrir sölu til viðskiptamanna
description: Ef þörf er á er hægt að útiloka að viðskiptavinur sé hafður með í söluskjölum og öðrum sölufærslum.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: dc8014cf0896db1ebbc5f0c5ea22e0f160c1b06d
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/01/2020
ms.locfileid: "3926548"
---
# <a name="block-customers"></a><span data-ttu-id="9b368-103">Loka á viðskiptamenn</span><span class="sxs-lookup"><span data-stu-id="9b368-103">Block Customers</span></span>
<span data-ttu-id="9b368-104">Hægt er að loka á viðskiptamann, til dæmis vegna gjaldþrota, svo að ekki sé hægt að bæta viðskiptamanninum við söluskjöl eða svo að ekki sé hægt að bóka færslur fyrir viðskiptamanninn.</span><span class="sxs-lookup"><span data-stu-id="9b368-104">You can block a customer, for example because of insolvency, so that the customer cannot be added to sales documents or so that no transactions can be posted for the customer.</span></span>

<span data-ttu-id="9b368-105">Auk þess að loka á viðskitamenn er hægt að stilla viðskiptakröfur fyrir viðskiptamanninn í bið í tengslum við áminningar.</span><span class="sxs-lookup"><span data-stu-id="9b368-105">In addition to blocking a customer, you can set receivable transactions for the customer to be on hold in connection with reminders.</span></span> <span data-ttu-id="9b368-106">Nánari upplýsingar er að finna í [Innheimta útistandandi skuldir](receivables-collect-outstanding-balances.md).</span><span class="sxs-lookup"><span data-stu-id="9b368-106">For more information, see [Collect Outstanding Balances](receivables-collect-outstanding-balances.md).</span></span>   

<span data-ttu-id="9b368-107">Eftirfarandi tafla lýsir valkostunum fyrir lokun á viðskiptavini.</span><span class="sxs-lookup"><span data-stu-id="9b368-107">The following table describes the options for blocking customers.</span></span>  

|<span data-ttu-id="9b368-108">Valkostur</span><span class="sxs-lookup"><span data-stu-id="9b368-108">Option</span></span>|<span data-ttu-id="9b368-109">Description</span><span class="sxs-lookup"><span data-stu-id="9b368-109">Description</span></span>|  
|--------------------|------------|  
|<span data-ttu-id="9b368-110">**Autt**</span><span class="sxs-lookup"><span data-stu-id="9b368-110">**Blank**</span></span>|<span data-ttu-id="9b368-111">Viðskipti eru leyfð fyrir þennan viðskiptamann.</span><span class="sxs-lookup"><span data-stu-id="9b368-111">Transactions are allowed for this customer.</span></span>|
|<span data-ttu-id="9b368-112">**Afhenda**</span><span class="sxs-lookup"><span data-stu-id="9b368-112">**Ship**</span></span>|<span data-ttu-id="9b368-113">Ekki er hægt að stofna nýjar pantanir og nýjar afhendingar fyrir þennan viðskiptamann.</span><span class="sxs-lookup"><span data-stu-id="9b368-113">New orders and new shipments cannot be created for this customer.</span></span> <span data-ttu-id="9b368-114">Hægt er að reikningsfæra fyrirliggjandi óreikningsfærðar afhendingar.</span><span class="sxs-lookup"><span data-stu-id="9b368-114">Existing shipments not yet invoiced can be invoiced.</span></span>|  
|<span data-ttu-id="9b368-115">**Reikningsfæra**</span><span class="sxs-lookup"><span data-stu-id="9b368-115">**Invoice**</span></span>|<span data-ttu-id="9b368-116">Ekki er hægt að stofna nýjar pantanir, nýjar afhendingar og nýja reikninga fyrir þennan viðskiptamann.</span><span class="sxs-lookup"><span data-stu-id="9b368-116">New orders, new shipments, and new invoices cannot be created for this customer.</span></span> <span data-ttu-id="9b368-117">Ekki er hægt að reikningsfæra fyrirliggjandi óreikningsfærðar afhendingar.</span><span class="sxs-lookup"><span data-stu-id="9b368-117">Existing shipments not yet invoiced cannot be invoiced.</span></span> <span data-ttu-id="9b368-118">Enn er hægt að senda innheimtubréf og vaxtareikninga til viðskiptavinarins.</span><span class="sxs-lookup"><span data-stu-id="9b368-118">You can still send reminders and finance charge memos to the customer.</span></span>|  
|<span data-ttu-id="9b368-119">**Allt**</span><span class="sxs-lookup"><span data-stu-id="9b368-119">**All**</span></span>|<span data-ttu-id="9b368-120">Engar færslur eru leyfðar fyrir þennan viðskiptamann, þ.m.t. greiðslur.</span><span class="sxs-lookup"><span data-stu-id="9b368-120">No transaction is allowed for this customer, including payments.</span></span>|  

## <a name="to-block-a-customer"></a><span data-ttu-id="9b368-121">Til að loka á viðskiptamann</span><span class="sxs-lookup"><span data-stu-id="9b368-121">To block a customer</span></span>  
1. <span data-ttu-id="9b368-122">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Viðskiptamenn** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="9b368-122">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Customers** , and then choose the related link.</span></span>
2. <span data-ttu-id="9b368-123">Veldu viðskiptamann og síðan aðgerðina **Breyta** .</span><span class="sxs-lookup"><span data-stu-id="9b368-123">Select a customer, and then choose the **Edit** action.</span></span>
3. <span data-ttu-id="9b368-124">Í reitnum **Lokað** skal velja hverju á að loka, eins og lýst er í töflunni hér að ofan.</span><span class="sxs-lookup"><span data-stu-id="9b368-124">In the **Blocked** field, choose what to block, as described in the table above.</span></span>

## <a name="see-also"></a><span data-ttu-id="9b368-125">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="9b368-125">See Also</span></span>  
[<span data-ttu-id="9b368-126">Skrá nýja viðskiptamenn</span><span class="sxs-lookup"><span data-stu-id="9b368-126">Register New Customers</span></span>](sales-how-register-new-customers.md)  
[<span data-ttu-id="9b368-127">Innheimta útistandandi skuldir</span><span class="sxs-lookup"><span data-stu-id="9b368-127">Collect Outstanding Balances</span></span>](receivables-collect-outstanding-balances.md)  
[<span data-ttu-id="9b368-128">Stjórnun skulda</span><span class="sxs-lookup"><span data-stu-id="9b368-128">Managing Receivables</span></span>](receivables-manage-receivables.md)  
