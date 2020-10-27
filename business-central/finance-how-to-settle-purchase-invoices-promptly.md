---
title: Greiða innkaupareikninga tímanlega
description: Ef greiða þarf lánardrottni með peningum eða ávísun er hægt að láta gera nauðsynlega bókun um leið og reikningurinn er bókaður.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.search.keywords: ''
ms.date: 10/06/2020
ms.author: bholtorf
ms.openlocfilehash: bac023393d95623a2731ef1b2ada7d30b135063b
ms.sourcegitcommit: 0fb6952376d853a878ed33257e73aadc03b95572
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/07/2020
ms.locfileid: "3968360"
---
# <a name="settle-purchase-invoices-promptly"></a><span data-ttu-id="ef76b-103">Greiða innkaupareikninga tímanlega</span><span class="sxs-lookup"><span data-stu-id="ef76b-103">Settle Purchase Invoices Promptly</span></span>

<span data-ttu-id="ef76b-104">Ef greiða þarf lánardrottni með peningum eða ávísun er hægt að bóka greiðsluna um leið og reikningurinn er bókaður.</span><span class="sxs-lookup"><span data-stu-id="ef76b-104">If you need to pay the vendor by cash or check, you can post the payment when you post the invoice.</span></span>  

> [!NOTE]  
> <span data-ttu-id="ef76b-105">Ef oft eru greiddir innkaupareikningar með peningum, ávísun eða bankamillifærslu er gagnlegt að setja upp sérstaka greiðsluaðferð með mótreikningi og færa þessa aðferð í reitinn  **Greiðsluaðferð** á lánardrottnaspjaldinu.</span><span class="sxs-lookup"><span data-stu-id="ef76b-105">If you frequently pay purchase invoices in cash, check, or bank transfer, it is a good idea to set up a specific payment method with a balancing account and enter this method in the **Payment Method** field on the vendor card.</span></span> <span data-ttu-id="ef76b-106">Mótreikningsnúmerið er sett sjálfkrafa í reikningshausinn í hvert sinn sem búinn er til nýr reikningur.</span><span class="sxs-lookup"><span data-stu-id="ef76b-106">The balancing account number is inserted automatically on the invoice header every time you create a new invoice.</span></span> <span data-ttu-id="ef76b-107">Frekari upplýsingar er að finna í [Greiðslumátar skilgreindir](finance-payment-methods.md).</span><span class="sxs-lookup"><span data-stu-id="ef76b-107">For more information, see [Defining Payment Methods](finance-payment-methods.md).</span></span>  

## <a name="to-settle-purchase-invoices-promptly"></a><span data-ttu-id="ef76b-108">Innkaupareikningar gerðir skjótt upp</span><span class="sxs-lookup"><span data-stu-id="ef76b-108">To settle purchase invoices promptly</span></span>

1. <span data-ttu-id="ef76b-109">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Innkaupareikningar** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="ef76b-109">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Purchase Invoices** , and then choose the related link.</span></span>  
2. <span data-ttu-id="ef76b-110">Valið er aðgerðin **Nýtt** .</span><span class="sxs-lookup"><span data-stu-id="ef76b-110">Choose the **New** action.</span></span>  
3. <span data-ttu-id="ef76b-111">Ef á að greiða annaðhvort með peningum eða bankamillifærslu skal færa inn númer fjárhagssjóðsreikningsins eða bankareikningsins í reitinn **Númer mótreiknings** .</span><span class="sxs-lookup"><span data-stu-id="ef76b-111">To pay either in cash or by bank transfer, enter the number of the general ledger cash account or the bank account in the **Bal. Account No.** field.</span></span>  

> [!IMPORTANT]  
> <span data-ttu-id="ef76b-112">Reitirnir **Tegund mótreiknings** og **Mótreikningur nr.** eru ekki í staðalútliti reikningshaussins.</span><span class="sxs-lookup"><span data-stu-id="ef76b-112">The **Bal. Account Type** and **Bal. Account No.** fields are not included in the standard layout of the invoice header.</span></span> <span data-ttu-id="ef76b-113">Til að bóka greiðslu á reikningi verður fyrst að hafa samband við samstarfsaðila Microsoft sem getur bætt reitunum við með kóða.</span><span class="sxs-lookup"><span data-stu-id="ef76b-113">In order to post the payment of an invoice, you must contact a Microsoft partner who can add the fields through code.</span></span>  
>
> <span data-ttu-id="ef76b-114">Þessi sérstilling er aðeins nauðsynleg ef ekki eru tilgreindir mótreikningar á greiðslumátunum eins og lýst er að ofan.</span><span class="sxs-lookup"><span data-stu-id="ef76b-114">This customization is only required if you do not specify balancing accounts on the payment methods as describe above.</span></span>

## <a name="see-also"></a><span data-ttu-id="ef76b-115">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="ef76b-115">See Also</span></span>

[<span data-ttu-id="ef76b-116">Stjórna skuldum</span><span class="sxs-lookup"><span data-stu-id="ef76b-116">Managing Payables</span></span>](payables-manage-payables.md)  
[<span data-ttu-id="ef76b-117">Innkaup</span><span class="sxs-lookup"><span data-stu-id="ef76b-117">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="ef76b-118">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="ef76b-118">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
