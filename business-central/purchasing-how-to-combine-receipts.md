---
title: Hvernig skal sameina móttökur | Microsoft Docs
description: Ef reikningsfæra á fleiri en eina innkaupamóttöku í einu er hægt að nota aðgerðina sameinaðar móttökur.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 07/02/2020
ms.author: sgroespe
ms.openlocfilehash: f5b3c47ab430b89c2f747f73bc427e045a902992
ms.sourcegitcommit: 506a433298fc3629231cfa98f64a2d1428094fde
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/03/2020
ms.locfileid: "3534672"
---
# <a name="combine-receipts-on-a-single-invoice"></a><span data-ttu-id="dc7af-103">Sameina móttökur í einn reikning</span><span class="sxs-lookup"><span data-stu-id="dc7af-103">Combine Receipts on a Single Invoice</span></span>

<span data-ttu-id="dc7af-104">Ef reikningsfæra á fleiri en eina innkaupamóttöku í einu er hægt að nota aðgerðina **sameinaðar móttökur**.</span><span class="sxs-lookup"><span data-stu-id="dc7af-104">If you want to invoice more than one purchase receipt at a time, you can use the **Combine Receipts** function.</span></span>  

<span data-ttu-id="dc7af-105">Áður en hægt er að búa til sameinaða innkaupamóttöku, þarf að vera búið að bóka fleiri en eina móttöku frá sama lánardrottininn í sama gjaldmiðlinum.</span><span class="sxs-lookup"><span data-stu-id="dc7af-105">Before you can create a combined purchase receipt, more than one receipt from the same vendor in the same currency must be posted.</span></span> <span data-ttu-id="dc7af-106">Það er að segja, það þarf að vera búið að fylla út tvær eða fleiri innkaupapantanir og bóka þær sem mótteknar en ekki reikningsfærðar.</span><span class="sxs-lookup"><span data-stu-id="dc7af-106">In other words, you must have filled in two or more purchase orders and posted them as received, but not invoiced.</span></span>  

<span data-ttu-id="dc7af-107">Þegar innkaupareikningar eru sameinaðir og bókaðir á reikningi, er bókaður innkaupareikningur stofnaður fyrir reikningslínu(r).</span><span class="sxs-lookup"><span data-stu-id="dc7af-107">When purchase receipts are combined on an invoice and posted, then a posted purchase invoice is created for the invoiced lines.</span></span> <span data-ttu-id="dc7af-108">Reiturinn **Reikningsfært magn** á upprunalegri innkaupapöntun eða standandi innkaupapöntun er uppfærður á grundvelli reikningsfærða magnsins.</span><span class="sxs-lookup"><span data-stu-id="dc7af-108">The **Quantity Invoiced** field on the originating purchase order, or blanket purchase order, is updated based on the invoiced quantity.</span></span> <span data-ttu-id="dc7af-109">Hins vegar er upprunalega innkaupaskjalinu ekki eytt jafnvel þó það hafi verið móttekið og reikningsfært að fullu og því verður að eyða innkaupaskjalinu.</span><span class="sxs-lookup"><span data-stu-id="dc7af-109">However, this original purchase document is not deleted, even if it has been fully received and invoiced, and you must therefore delete the purchase document.</span></span>  

> [!NOTE]
> <span data-ttu-id="dc7af-110">Ekki er hægt að leiðrétta eða hætta við innkaupareikninginn síðar.</span><span class="sxs-lookup"><span data-stu-id="dc7af-110">The resulting purchase invoice cannot later be corrected or canceled.</span></span> <span data-ttu-id="dc7af-111">Ef ætlunin er að breyta innkaupareikningi sem er búinn til á þennan hátt verður að nota innkaupakreditreikninga.</span><span class="sxs-lookup"><span data-stu-id="dc7af-111">If you want to modify a purchase invoice that is created in this way, you must use purchase credit memos.</span></span> <span data-ttu-id="dc7af-112">Nánari upplýsingar er að finna [Ógreiddir innkaupareikningar leiðréttir eða afturkallaðir](purchasing-how-correct-cancel-unpaid-purchase-invoices.md).</span><span class="sxs-lookup"><span data-stu-id="dc7af-112">For more information, see [Correct or Cancel Unpaid Purchase Invoices](purchasing-how-correct-cancel-unpaid-purchase-invoices.md).</span></span>

## <a name="to-combine-receipts"></a><span data-ttu-id="dc7af-113">Sameining móttakna:</span><span class="sxs-lookup"><span data-stu-id="dc7af-113">To combine receipts</span></span>

1. <span data-ttu-id="dc7af-114">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Innkaupareikningar** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="dc7af-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Purchase Invoices**, and then choose the related link.</span></span>  
2. <span data-ttu-id="dc7af-115">Valið er **Nýtt** aðgerð.</span><span class="sxs-lookup"><span data-stu-id="dc7af-115">Choose the **New** action.</span></span> <span data-ttu-id="dc7af-116">Nánari upplýsingar eru í reitnum [Skrá innkaup](purchasing-how-record-purchases.md).</span><span class="sxs-lookup"><span data-stu-id="dc7af-116">For more information, see [Record Purchases](purchasing-how-record-purchases.md).</span></span>  
3. <span data-ttu-id="dc7af-117">Á flýtiflipanum **Línur** skal velja **Sækja móttökulínur** aðgerðina.</span><span class="sxs-lookup"><span data-stu-id="dc7af-117">On the **Lines** FastTab, choose the **Get Receipt Lines** action.</span></span>  
4. <span data-ttu-id="dc7af-118">Nokkrar móttökulínur eru valdar sem eiga að vera á reikningnum:</span><span class="sxs-lookup"><span data-stu-id="dc7af-118">Select multiple receipt lines that you want to include in the invoice.</span></span>  

    <span data-ttu-id="dc7af-119">Ef röng móttökulína var valin eða byrja á upp á nýtt er einfaldlega hægt að eyða línunum í innkaupareikningum og nota aftur aðgerðina **Sækja móttökulínur**.</span><span class="sxs-lookup"><span data-stu-id="dc7af-119">If an incorrect receipt line was selected or you want to start over, you can just delete the lines on the purchase invoice and then use the **Get Receipt Lines** function again.</span></span>  
5. <span data-ttu-id="dc7af-120">Til að bóka reikningur er valið aðgerðin **bóka**.</span><span class="sxs-lookup"><span data-stu-id="dc7af-120">To post the invoice, choose the **Post** action.</span></span>  

## <a name="to-remove-open-purchase-orders-after-combined-receipt-posting"></a><span data-ttu-id="dc7af-121">Til að fjarlægja opnar innkaupapantanir eftir bókun sameinaðrar móttöku</span><span class="sxs-lookup"><span data-stu-id="dc7af-121">To remove open purchase orders after combined receipt posting</span></span>

1. <span data-ttu-id="dc7af-122">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Eyða** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="dc7af-122">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Delete Invoiced Purchase Orders**, and select the related link.</span></span>  
2. <span data-ttu-id="dc7af-123">Fyllið inn í reitina eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="dc7af-123">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]<span data-ttu-id="dc7af-124">.</span><span class="sxs-lookup"><span data-stu-id="dc7af-124">.</span></span>
3. <span data-ttu-id="dc7af-125">Velja hnappinn **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="dc7af-125">Choose the **OK** button.</span></span>  

<span data-ttu-id="dc7af-126">Að öðrum kosti skal eyða einstökum pöntunum handvirkt.</span><span class="sxs-lookup"><span data-stu-id="dc7af-126">Alternatively, delete the individual orders manually.</span></span>

<span data-ttu-id="dc7af-127">Skref 1 til 3 eru endurtekin fyrir öll skjöl sem urðu fyrir áhrifum, eins og auðar innikaupapantanir.</span><span class="sxs-lookup"><span data-stu-id="dc7af-127">Repeat steps 1 through 3 for any other affected documents, such as blanket purchase orders.</span></span>

## <a name="see-also"></a><span data-ttu-id="dc7af-128">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="dc7af-128">See Also</span></span>

[<span data-ttu-id="dc7af-129">Innkaup</span><span class="sxs-lookup"><span data-stu-id="dc7af-129">Purchasing</span></span>](purchasing-manage-purchasing.md)  
[<span data-ttu-id="dc7af-130">Leiðrétta eða afturkalla ógreidda innkaupareikninga</span><span class="sxs-lookup"><span data-stu-id="dc7af-130">Correct or Cancel Unpaid Purchase Invoices</span></span>](purchasing-how-correct-cancel-unpaid-purchase-invoices.md)  
<span data-ttu-id="dc7af-131">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="dc7af-131">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
