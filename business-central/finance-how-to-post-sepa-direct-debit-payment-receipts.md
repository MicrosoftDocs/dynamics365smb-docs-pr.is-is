---
title: "Bóka SEPA-beingreiðslur | Microsoft Docs"
description: "Þegar innheimta beingreiðslu er meðhöndluð af bankanum er hægt að bóka kvittanir greiðslunnar fyrir sölureikninganna."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/21/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 2daa52e1ee4546356ecb7d94b5c01ab9e22bbbd6
ms.contentlocale: is-is
ms.lasthandoff: 03/22/2018

---
# <a name="post-sepa-direct-debit-payment-receipts"></a><span data-ttu-id="41cf4-103">Bóka SEPA-greiðslukvittanir beingreiðslna</span><span class="sxs-lookup"><span data-stu-id="41cf4-103">Post SEPA Direct Debit Payment Receipts</span></span>
<span data-ttu-id="41cf4-104">Þegar innheimta beingreiðslu er meðhöndluð af bankanum er hægt að bóka kvittanir greiðslunnar fyrir sölureikninganna.</span><span class="sxs-lookup"><span data-stu-id="41cf4-104">When a direct debit collection is successfully processed by your bank, you can proceed to post receipt of the payment for the involved sales invoices.</span></span> <span data-ttu-id="41cf4-105">Frekari upplýsingar, sjá [Stofna SEPA-innheimtufærslur fyrir beingreiðslur og flytja út í bankaskrá](finance-how-create-sepa-direct-debit-collection-entries-export-bank-file.md).</span><span class="sxs-lookup"><span data-stu-id="41cf4-105">For more information, see [Create SEPA Direct Debit Collection Entries and Export to a Bank File](finance-how-create-sepa-direct-debit-collection-entries-export-bank-file.md).</span></span>  

<span data-ttu-id="41cf4-106">Hægt að bóka greiðslukvittunina beint úr **Innheimta fyrir beingreiðslur** glugganum, eða **Innheimtufærslur fyrir beingreiðslur** glugganum.</span><span class="sxs-lookup"><span data-stu-id="41cf4-106">You can post the payment receipt directly from the **Direct Debit Collections** window or the **Direct Debit Collect. Entries** window.</span></span> <span data-ttu-id="41cf4-107">Einnig er hægt að færa verkið á annan notanda með því að undirbúa tengdar færslubókarlínur.</span><span class="sxs-lookup"><span data-stu-id="41cf4-107">Alternatively, you can relay the work to another user by preparing the related journal lines.</span></span>  

## <a name="to-post-a-direct-debit-payment-receipt-from-the-direct-debit-collections-window"></a><span data-ttu-id="41cf4-108">Bóka greiðslukvittun beingreiðslu úr glugganum Innheimta beingreiðslur</span><span class="sxs-lookup"><span data-stu-id="41cf4-108">To post a direct-debit payment receipt from the Direct Debit Collections window</span></span>  
1. <span data-ttu-id="41cf4-109">Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Bein skuldfærsla** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="41cf4-109">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Direct Debit Collections**, and then choose the related link.</span></span>  
2. <span data-ttu-id="41cf4-110">Veljið línu fyrir innheimtu beingreiðslu sem hefur verið flutt út í bankaskrá og meðhöndluð af bankanum.</span><span class="sxs-lookup"><span data-stu-id="41cf4-110">Select a line for a direct debit collection that has been exported to a bank file and successfully processed by the bank.</span></span> <span data-ttu-id="41cf4-111">Frekari upplýsingar, sjá [Stofna SEPA-innheimtufærslur fyrir beingreiðslur og flytja út í bankaskrá](finance-how-create-sepa-direct-debit-collection-entries-export-bank-file.md).</span><span class="sxs-lookup"><span data-stu-id="41cf4-111">For more information, see [Create SEPA Direct Debit Collection Entries and Export to a Bank File](finance-how-create-sepa-direct-debit-collection-entries-export-bank-file.md).</span></span>  
3. <span data-ttu-id="41cf4-112">Valið er **bóka greiðslukvittanir** aðgerð.</span><span class="sxs-lookup"><span data-stu-id="41cf4-112">Choose the **Post Payment Receipts** action.</span></span>  
4. <span data-ttu-id="41cf4-113">Í glugganum **bóka innheimtu beingreiðslu** þarf að fylla reitina út eins og lýst er í eftirfarandi töflu.</span><span class="sxs-lookup"><span data-stu-id="41cf4-113">In the **Post Direct Debit Collection** window, fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="41cf4-114">Svæði</span><span class="sxs-lookup"><span data-stu-id="41cf4-114">Field</span></span>|<span data-ttu-id="41cf4-115">Description</span><span class="sxs-lookup"><span data-stu-id="41cf4-115">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="41cf4-116">**Númer innheimtu með beinni skuldfærslu**</span><span class="sxs-lookup"><span data-stu-id="41cf4-116">**Direct Debit Collection No.**</span></span>|<span data-ttu-id="41cf4-117">Tilgreina innheimtu beingreiðslu sem á að bóka greiðslukvittun fyrir.</span><span class="sxs-lookup"><span data-stu-id="41cf4-117">Specify the direct debit collection that you want to post payment receipt for.</span></span>|  
    |<span data-ttu-id="41cf4-118">**Sniðmát almennrar færslubókar**</span><span class="sxs-lookup"><span data-stu-id="41cf4-118">**General Journal Template**</span></span>|<span data-ttu-id="41cf4-119">Tilgreina hvaða sniðmát almennrar færslubókar á að nota til að bóka greiðslukvittun, svo sem sniðmát fyrir inngreiðslur.</span><span class="sxs-lookup"><span data-stu-id="41cf4-119">Specify which general journal template to use for posting the payment receipt, such as the template for cash receipts.</span></span>|  
    |<span data-ttu-id="41cf4-120">**Heiti færslubókarkeyrslu**</span><span class="sxs-lookup"><span data-stu-id="41cf4-120">**General Journal Batch Name**</span></span>|<span data-ttu-id="41cf4-121">Tilgreina hvaða færslubókarkeyrslu á að nota til að bóka greiðslukvittun.</span><span class="sxs-lookup"><span data-stu-id="41cf4-121">Specify which general journal batch to use for posting the payment receipt.</span></span>|  
    |<span data-ttu-id="41cf4-122">**Stofna aðeins færslubók**</span><span class="sxs-lookup"><span data-stu-id="41cf4-122">**Create Journal Only**</span></span>|<span data-ttu-id="41cf4-123">Veljið þennan gátreit ef ekki á að bóka greiðslukvittunina þegar **Í lagi** hnappurinn er valinn.</span><span class="sxs-lookup"><span data-stu-id="41cf4-123">Select this check box if you do not want to post the payment receipt when you choose the **OK** button.</span></span> <span data-ttu-id="41cf4-124">Greiðslukvittunin verður undirbúin í tilgreindri færslubók og mun ekki vera bókuð fyrr en einhver bókar færslubókarlínurnar sem um ræðir.</span><span class="sxs-lookup"><span data-stu-id="41cf4-124">The payment receipt will be prepared in the specified journal and will not be posted until someone posts the journal lines in question.</span></span>|  

5. <span data-ttu-id="41cf4-125">Velja hnappinn **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="41cf4-125">Choose the **OK** button.</span></span>  

## <a name="see-also"></a><span data-ttu-id="41cf4-126">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="41cf4-126">See Also</span></span>  
 <span data-ttu-id="41cf4-127">[Innheimta greiðslur með SEPA-beingreiðslum](finance-collect-payments-with-sepa-direct-debit.md) </span><span class="sxs-lookup"><span data-stu-id="41cf4-127">[Collecting Payments with SEPA Direct Debit](finance-collect-payments-with-sepa-direct-debit.md) </span></span>  
 [<span data-ttu-id="41cf4-128">Sala</span><span class="sxs-lookup"><span data-stu-id="41cf4-128">Sales</span></span>](sales-manage-sales.md)

