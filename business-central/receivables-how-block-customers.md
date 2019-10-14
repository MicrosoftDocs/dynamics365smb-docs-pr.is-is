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
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: c2b0d5b15571b7e8af1ed1dbee22859f4c131aa3
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/01/2019
ms.locfileid: "2316621"
---
# <a name="block-customers"></a><span data-ttu-id="03961-103">Loka á viðskiptamenn</span><span class="sxs-lookup"><span data-stu-id="03961-103">Block Customers</span></span>
<span data-ttu-id="03961-104">Hægt er að loka á viðskiptamann, til dæmis vegna gjaldþrota, svo að ekki sé hægt að bæta viðskiptamanninum við söluskjöl eða svo að ekki sé hægt að bóka færslur fyrir viðskiptamanninn.</span><span class="sxs-lookup"><span data-stu-id="03961-104">You can block a customer, for example because of insolvency, so that the customer cannot be added to sales documents or so that no transactions can be posted for the customer.</span></span>

<span data-ttu-id="03961-105">Auk þess að loka á viðskitamenn er hægt að stilla viðskiptakröfur fyrir viðskiptamanninn í bið í tengslum við áminningar.</span><span class="sxs-lookup"><span data-stu-id="03961-105">In addition to blocking a customer, you can set receivable transactions for the customer to be on hold in connection with reminders.</span></span> <span data-ttu-id="03961-106">Nánari upplýsingar er að finna í [Innheimta útistandandi skuldir](receivables-collect-outstanding-balances.md).</span><span class="sxs-lookup"><span data-stu-id="03961-106">For more information, see [Collect Outstanding Balances](receivables-collect-outstanding-balances.md).</span></span>   

<span data-ttu-id="03961-107">Eftirfarandi tafla lýsir mismunandi valkostum lokunar.</span><span class="sxs-lookup"><span data-stu-id="03961-107">The following table describes the different blocking options.</span></span>  

|<span data-ttu-id="03961-108">Valkostur</span><span class="sxs-lookup"><span data-stu-id="03961-108">Option</span></span>|<span data-ttu-id="03961-109">Description</span><span class="sxs-lookup"><span data-stu-id="03961-109">Description</span></span>|  
|--------------------|------------|  
|<span data-ttu-id="03961-110">**Autt**</span><span class="sxs-lookup"><span data-stu-id="03961-110">**Blank**</span></span>|<span data-ttu-id="03961-111">Viðskipti eru leyfð fyrir þennan viðskiptamann.</span><span class="sxs-lookup"><span data-stu-id="03961-111">Transactions are allowed for this customer.</span></span>|
|<span data-ttu-id="03961-112">**Afhenda**</span><span class="sxs-lookup"><span data-stu-id="03961-112">**Ship**</span></span>|<span data-ttu-id="03961-113">Ekki er hægt að stofna nýjar pantanir og nýjar afhendingar fyrir þennan viðskiptamann.</span><span class="sxs-lookup"><span data-stu-id="03961-113">New orders and new shipments cannot be created for this customer.</span></span> <span data-ttu-id="03961-114">Hægt er að reikningsfæra fyrirliggjandi óreikningsfærðar afhendingar.</span><span class="sxs-lookup"><span data-stu-id="03961-114">Existing shipments not yet invoiced can be invoiced.</span></span>|  
|<span data-ttu-id="03961-115">**Reikningsfæra**</span><span class="sxs-lookup"><span data-stu-id="03961-115">**Invoice**</span></span>|<span data-ttu-id="03961-116">Ekki er hægt að stofna nýjar pantanir, nýjar afhendingar og nýja reikninga fyrir þennan viðskiptamann.</span><span class="sxs-lookup"><span data-stu-id="03961-116">New orders, new shipments, and new invoices cannot be created for this customer.</span></span> <span data-ttu-id="03961-117">Ekki er hægt að reikningsfæra fyrirliggjandi óreikningsfærðar afhendingar.</span><span class="sxs-lookup"><span data-stu-id="03961-117">Existing shipments not yet invoiced cannot be invoiced.</span></span>|  
|<span data-ttu-id="03961-118">**ALLT**</span><span class="sxs-lookup"><span data-stu-id="03961-118">**All**</span></span>|<span data-ttu-id="03961-119">Engar færslur eru leyfðar fyrir þennan viðskiptamann, þ.m.t. greiðslur.</span><span class="sxs-lookup"><span data-stu-id="03961-119">No transaction is allowed for this customer, including payments.</span></span>|  

## <a name="to-block-a-customer"></a><span data-ttu-id="03961-120">Til að loka á viðskiptamann</span><span class="sxs-lookup"><span data-stu-id="03961-120">To block a customer</span></span>  
1. <span data-ttu-id="03961-121">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Viðskiptamenn** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="03961-121">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Customers**, and then choose the related link.</span></span>
2. <span data-ttu-id="03961-122">Veldu viðskiptamann og síðan aðgerðina **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="03961-122">Select a customer, and then choose the **Edit** action.</span></span>
3. <span data-ttu-id="03961-123">Fylltu inn **Útiloika** reitinn með einum af valkostunum sem lýst er hér að ofan.</span><span class="sxs-lookup"><span data-stu-id="03961-123">Fill in the **Blocked** field with one of the options described above.</span></span>

## <a name="see-also"></a><span data-ttu-id="03961-124">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="03961-124">See Also</span></span>  
[<span data-ttu-id="03961-125">Skrá nýja viðskiptamenn</span><span class="sxs-lookup"><span data-stu-id="03961-125">Register New Customers</span></span>](sales-how-register-new-customers.md)  
[<span data-ttu-id="03961-126">Innheimta útistandandi skuldir</span><span class="sxs-lookup"><span data-stu-id="03961-126">Collect Outstanding Balances</span></span>](receivables-collect-outstanding-balances.md)  
[<span data-ttu-id="03961-127">Stjórnun skulda</span><span class="sxs-lookup"><span data-stu-id="03961-127">Managing Receivables</span></span>](receivables-manage-receivables.md)  
