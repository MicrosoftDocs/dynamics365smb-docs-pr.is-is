---
title: Hvernig á að leiðrétta fyrirframgreiðslu | Microsoft Docs
description: Hægt er að gera leiðréttingu á pöntun eftir að búið er að bóka fyrirframgreiðslureikning fyrir pöntunina. Hægt er að bæta nýjum línum við pöntun eftir að búið er að senda fyrirframgreiðslu og bóka síðan annan fyrirframgreiddan reikning en ekki er unnt að eyða línu í pöntun eftir fyrirframgreiðsla hefur verið reikningsfærð fyrir línu.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 3dd124807d3d6ce3a775d18dcd88a8251b0feb30
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/01/2020
ms.locfileid: "3924179"
---
# <a name="correct-prepayments"></a><span data-ttu-id="a984c-104">Leiðrétta fyrirframgreiðslur</span><span class="sxs-lookup"><span data-stu-id="a984c-104">Correct Prepayments</span></span>

<span data-ttu-id="a984c-105">Hægt er að gera leiðréttingu á pöntun eftir að búið er að bóka fyrirframgreiðslureikning fyrir pöntunina.</span><span class="sxs-lookup"><span data-stu-id="a984c-105">You can make a correction to an order after you have posted a prepayment invoice for the order.</span></span> <span data-ttu-id="a984c-106">Hægt er að bæta nýjum línum við pöntun eftir að búið er að senda fyrirframgreiðslu og bóka síðan annan fyrirframgreiddan reikning en ekki er unnt að eyða línu í pöntun eftir fyrirframgreiðsla hefur verið reikningsfærð fyrir línu.</span><span class="sxs-lookup"><span data-stu-id="a984c-106">You can add new lines to an order after issuing a prepayment, and then you can post another prepayment invoice, but you cannot delete a line from an order after a prepayment has been invoiced for the line.</span></span>  

> [!TIP]
> <span data-ttu-id="a984c-107">Ef búið er að bóka fyrirframgreiðslureikning fyrir sölureikning sem þá þú leiðréttir svo eða hættir við verður einnig að leiðrétta eða hætta við fyrirframgreiðsluna.</span><span class="sxs-lookup"><span data-stu-id="a984c-107">If you have posted a prepayment invoice for a sales invoice that you then correct or cancel, you must correct or cancel the prepayment as well.</span></span>

## <a name="to-correct-a-prepayment"></a><span data-ttu-id="a984c-108">Til að leiðrétta fyrirframgreiðslu:</span><span class="sxs-lookup"><span data-stu-id="a984c-108">To correct a prepayment</span></span>

<span data-ttu-id="a984c-109">Eftirfarandi ferli sýnir hvernig gefa skal út kreditreikning fyrirframgreiðslu til að afturkalla allar reikningsfærðar fyrirframgreiðslur fyrir sölupöntun.</span><span class="sxs-lookup"><span data-stu-id="a984c-109">The following procedure shows how to issue a prepayment credit memo to cancel all invoiced prepayments for a sales order.</span></span>  

1. <span data-ttu-id="a984c-110">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Sölupantanir** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="a984c-110">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Orders** , and then choose the related link.</span></span>  
2. <span data-ttu-id="a984c-111">Viðeigandi sölupöntun er opnuð.</span><span class="sxs-lookup"><span data-stu-id="a984c-111">Open the relevant sales order.</span></span>
3. <span data-ttu-id="a984c-112">Veljið aðgerðina **Fyrirframgreiðsla** og síðan aðgerðina **Bóka kreditreikning fyrirframgreiðslu** eða **Bóka og prenta kr.reikn. fyrirframgr.** aðgerðina.</span><span class="sxs-lookup"><span data-stu-id="a984c-112">Choose the **Prepayment** action, and then choose the **Post Prepayment Credit Memo** action or the **Post and Print Prepmt. Cr. Memo** action.</span></span>  
4. <span data-ttu-id="a984c-113">Á síðunni **Kreditreikningur sölu** skal farið í leiðréttingu viðeigandi færslna, sem og alla kreditreikninga sölu.</span><span class="sxs-lookup"><span data-stu-id="a984c-113">On the **Sales Credit Memo** page, proceed to correct the relevant entries, as for any sales credit memo.</span></span> <span data-ttu-id="a984c-114">Fyrir frekar upplýsingar, sjá [Meðhöndlun söluvöruskila eða afturkallana](sales-how-process-sales-returns-cancellations.md).</span><span class="sxs-lookup"><span data-stu-id="a984c-114">For more information, see [Process Sales Returns or Cancellations](sales-how-process-sales-returns-cancellations.md).</span></span>  

    > [!NOTE]  
    > <span data-ttu-id="a984c-115">Til að lækka upphæðina í reitnum **Upphæð línu** , verður fyrst að auka fyrirframgreiðsluprósentuna í línunni svo gildið í reitnum **fyrirfrgr. línuupphæð** sé ekki lækkuð niður fyrir gildið í reitnum **fyrirfrg. reikningsupphæð** .</span><span class="sxs-lookup"><span data-stu-id="a984c-115">To reduce the amount in the **Line Amount** field, you must first increase the prepayment percentage on the line so that the value in the **Prepmt. Line Amount** field is not decreased below the value in the **Prepmt. Amt. Inv.** field.</span></span>

5. <span data-ttu-id="a984c-116">Til að gera fyrirframgreiðslureikning fyrir nýjar línur í sölukreditreikningi, veljið aðgerðina **Fyrirframgreiðsla** og síðan aðgerðina **Bóka reikning fyrirframgreiðslu** eða **Bóka og prenta reikn. fyrirframgr.** aðgerðina.</span><span class="sxs-lookup"><span data-stu-id="a984c-116">To make a prepayment invoice for any new lines in the sales credit memo, choose the **Prepayment** action, and then choose the **Post Prepayment Invoice** action or the **Post and Print Prepmt. Invoice** action.</span></span>  
6. <span data-ttu-id="a984c-117">Til að gefa út auka fyrirframgreiðslureikning, skal hækka upphæð fyrirframgreiðslu í einni eða fleiri línum og bóka fyrirframgreiðslureikninginn.</span><span class="sxs-lookup"><span data-stu-id="a984c-117">To issue an additional prepayment invoice, increase the prepayment amount on one or more lines and post the prepayment invoice.</span></span> <span data-ttu-id="a984c-118">Nýr reikningur er stofnaður fyrir mismuninn á milli reikningsfærðra upphæða fyrirframgreiðslu og nýju fyrirframgreiðsluupphæðanna.</span><span class="sxs-lookup"><span data-stu-id="a984c-118">A new invoice will be created for the difference between the prepayment amounts invoiced and the new prepayment amounts.</span></span>  

## <a name="see-also"></a><span data-ttu-id="a984c-119">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="a984c-119">See Also</span></span>

[<span data-ttu-id="a984c-120">Reikningsfærsla fyrirframgreiðslna</span><span class="sxs-lookup"><span data-stu-id="a984c-120">Invoicing Prepayments</span></span>](finance-invoice-prepayments.md)  
[<span data-ttu-id="a984c-121">Kynning: Uppsetning og reikningsfærsla fyrirframgreiðslna fyrir sölu</span><span class="sxs-lookup"><span data-stu-id="a984c-121">Walkthrough: Setting Up and Invoicing Sales Prepayments</span></span>](walkthrough-setting-up-and-invoicing-sales-prepayments.md)  
[<span data-ttu-id="a984c-122">Fjármál</span><span class="sxs-lookup"><span data-stu-id="a984c-122">Finance</span></span>](finance.md)  
<span data-ttu-id="a984c-123">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="a984c-123">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
