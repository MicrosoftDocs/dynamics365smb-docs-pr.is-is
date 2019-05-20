---
title: Hvernig á að loka sölu til viðskiptamanna Atriði frá sölu eða kaupum
description: Í Business Central getur vara verið merkt sem lokuð fyrir sölu, lokuð fyrir innkaupum eða lokuð fyrir allt.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: a2dee70270df135bc61ddef38e661758431b02a9
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/29/2019
ms.locfileid: "1251355"
---
# <a name="block-customers"></a><span data-ttu-id="9e448-103">Loka á viðskiptamenn</span><span class="sxs-lookup"><span data-stu-id="9e448-103">Block Customers</span></span>
<span data-ttu-id="9e448-104">Hægt er að loka á viðskiptamann, til dæmis vegna gjaldþrota, svo að ekki sé hægt að bæta viðskiptamanninum við söluskjöl eða svo að ekki sé hægt að bóka færslur fyrir viðskiptamanninn.</span><span class="sxs-lookup"><span data-stu-id="9e448-104">You can block a customer, for example because of insolvency, so that the customer cannot be added to sales documents or so that no transactions can be posted for the customer.</span></span>

<span data-ttu-id="9e448-105">Auk þess að loka á viðskitamenn er hægt að stilla viðskiptakröfur fyrir viðskiptamanninn í bið í tengslum við áminningar.</span><span class="sxs-lookup"><span data-stu-id="9e448-105">In addition to blocking a customer, you can set receivable transactions for the customer to be on hold in connection with reminders.</span></span> <span data-ttu-id="9e448-106">Nánari upplýsingar er að finna í [Innheimta útistandandi skuldir](receivables-collect-outstanding-balances.md).</span><span class="sxs-lookup"><span data-stu-id="9e448-106">For more information, see [Collect Outstanding Balances](receivables-collect-outstanding-balances.md).</span></span>   

<span data-ttu-id="9e448-107">Eftirfarandi tafla lýsir mismunandi valkostum lokunar.</span><span class="sxs-lookup"><span data-stu-id="9e448-107">The following table describes the different blocking options.</span></span>  

|<span data-ttu-id="9e448-108">Valkostur</span><span class="sxs-lookup"><span data-stu-id="9e448-108">Option</span></span>|<span data-ttu-id="9e448-109">Description</span><span class="sxs-lookup"><span data-stu-id="9e448-109">Description</span></span>|  
|--------------------|------------|  
|<span data-ttu-id="9e448-110">**Autt**</span><span class="sxs-lookup"><span data-stu-id="9e448-110">**Blank**</span></span>|<span data-ttu-id="9e448-111">Viðskipti eru leyfð fyrir þennan viðskiptamann.</span><span class="sxs-lookup"><span data-stu-id="9e448-111">Transactions are allowed for this customer.</span></span>|
|<span data-ttu-id="9e448-112">**Afhenda**</span><span class="sxs-lookup"><span data-stu-id="9e448-112">**Ship**</span></span>|<span data-ttu-id="9e448-113">Ekki er hægt að stofna nýjar pantanir og nýjar afhendingar fyrir þennan viðskiptamann.</span><span class="sxs-lookup"><span data-stu-id="9e448-113">New orders and new shipments cannot be created for this customer.</span></span> <span data-ttu-id="9e448-114">Hægt er að reikningsfæra fyrirliggjandi óreikningsfærðar afhendingar.</span><span class="sxs-lookup"><span data-stu-id="9e448-114">Existing shipments not yet invoiced can be invoiced.</span></span>|  
|<span data-ttu-id="9e448-115">**Reikningsfæra**</span><span class="sxs-lookup"><span data-stu-id="9e448-115">**Invoice**</span></span>|<span data-ttu-id="9e448-116">Ekki er hægt að stofna nýjar pantanir, nýjar afhendingar og nýja reikninga fyrir þennan viðskiptamann.</span><span class="sxs-lookup"><span data-stu-id="9e448-116">New orders, new shipments, and new invoices cannot be created for this customer.</span></span> <span data-ttu-id="9e448-117">Ekki er hægt að reikningsfæra fyrirliggjandi óreikningsfærðar afhendingar.</span><span class="sxs-lookup"><span data-stu-id="9e448-117">Existing shipments not yet invoiced cannot be invoiced.</span></span>|  
|<span data-ttu-id="9e448-118">**ALLT**</span><span class="sxs-lookup"><span data-stu-id="9e448-118">**All**</span></span>|<span data-ttu-id="9e448-119">Engar færslur eru leyfðar fyrir þennan viðskiptamann, þ.m.t. greiðslur.</span><span class="sxs-lookup"><span data-stu-id="9e448-119">No transaction is allowed for this customer, including payments.</span></span>|  

## <a name="to-block-a-customer"></a><span data-ttu-id="9e448-120">Til að loka á viðskiptamann</span><span class="sxs-lookup"><span data-stu-id="9e448-120">To block a customer</span></span>  
1. <span data-ttu-id="9e448-121">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Viðskiptamenn** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="9e448-121">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Customers**, and then choose the related link.</span></span>
2. <span data-ttu-id="9e448-122">Veldu viðskiptamann og síðan aðgerðina **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="9e448-122">Select a customer, and then choose the **Edit** action.</span></span>
3. <span data-ttu-id="9e448-123">Fylltu inn **Útiloika** reitinn með einum af valkostunum sem lýst er hér að ofan.</span><span class="sxs-lookup"><span data-stu-id="9e448-123">Fill in the **Blocked** field with one of the options described above.</span></span>

## <a name="see-also"></a><span data-ttu-id="9e448-124">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="9e448-124">See Also</span></span>  
[<span data-ttu-id="9e448-125">Skrá nýja viðskiptamenn</span><span class="sxs-lookup"><span data-stu-id="9e448-125">Register New Customers</span></span>](sales-how-register-new-customers.md)  
[<span data-ttu-id="9e448-126">Innheimta útistandandi skuldir</span><span class="sxs-lookup"><span data-stu-id="9e448-126">Collect Outstanding Balances</span></span>](receivables-collect-outstanding-balances.md)  
[<span data-ttu-id="9e448-127">Stjórnun skulda</span><span class="sxs-lookup"><span data-stu-id="9e448-127">Managing Receivables</span></span>](receivables-manage-receivables.md)  
