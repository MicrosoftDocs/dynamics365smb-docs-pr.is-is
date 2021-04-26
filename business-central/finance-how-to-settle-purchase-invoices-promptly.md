---
title: Greiða innkaupareikninga tímanlega
description: Ef greiða þarf lánardrottni með peningum eða ávísun er hægt að láta gera nauðsynlega bókun um leið og reikningurinn er bókaður.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: bholtorf
ms.openlocfilehash: d7962031aa7dda7dafa96ade8e11339c06ebb305
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5784593"
---
# <a name="settle-purchase-invoices-promptly"></a><span data-ttu-id="299ce-103">Greiða innkaupareikninga tímanlega</span><span class="sxs-lookup"><span data-stu-id="299ce-103">Settle Purchase Invoices Promptly</span></span>

<span data-ttu-id="299ce-104">Ef greiða þarf lánardrottni með peningum eða ávísun er hægt að bóka greiðsluna um leið og reikningurinn er bókaður.</span><span class="sxs-lookup"><span data-stu-id="299ce-104">If you need to pay the vendor by cash or check, you can post the payment when you post the invoice.</span></span>  

> [!NOTE]  
> <span data-ttu-id="299ce-105">Ef oft eru greiddir innkaupareikningar með peningum, ávísun eða bankamillifærslu er gagnlegt að setja upp sérstaka greiðsluaðferð með mótreikningi og færa þessa aðferð í reitinn  **Greiðsluaðferð** á lánardrottnaspjaldinu.</span><span class="sxs-lookup"><span data-stu-id="299ce-105">If you frequently pay purchase invoices in cash, check, or bank transfer, it is a good idea to set up a specific payment method with a balancing account and enter this method in the **Payment Method** field on the vendor card.</span></span> <span data-ttu-id="299ce-106">Mótreikningsnúmerið er sett sjálfkrafa í reikningshausinn í hvert sinn sem búinn er til nýr reikningur.</span><span class="sxs-lookup"><span data-stu-id="299ce-106">The balancing account number is inserted automatically on the invoice header every time you create a new invoice.</span></span> <span data-ttu-id="299ce-107">Frekari upplýsingar er að finna í [Greiðslumátar skilgreindir](finance-payment-methods.md).</span><span class="sxs-lookup"><span data-stu-id="299ce-107">For more information, see [Defining Payment Methods](finance-payment-methods.md).</span></span>  

## <a name="to-settle-purchase-invoices-promptly"></a><span data-ttu-id="299ce-108">Innkaupareikningar gerðir skjótt upp</span><span class="sxs-lookup"><span data-stu-id="299ce-108">To settle purchase invoices promptly</span></span>

1. <span data-ttu-id="299ce-109">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Innkaupareikningar** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="299ce-109">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Purchase Invoices**, and then choose the related link.</span></span>  
2. <span data-ttu-id="299ce-110">Valið er aðgerðin **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="299ce-110">Choose the **New** action.</span></span>  
3. <span data-ttu-id="299ce-111">Ef á að greiða annaðhvort með peningum eða bankamillifærslu skal færa inn númer fjárhagssjóðsreikningsins eða bankareikningsins í reitinn **Númer mótreiknings**.</span><span class="sxs-lookup"><span data-stu-id="299ce-111">To pay either in cash or by bank transfer, enter the number of the general ledger cash account or the bank account in the **Bal. Account No.** field.</span></span>  

> [!IMPORTANT]  
> <span data-ttu-id="299ce-112">Reitirnir **Tegund mótreiknings** og **Mótreikningur nr.** eru ekki í staðalútliti reikningshaussins.</span><span class="sxs-lookup"><span data-stu-id="299ce-112">The **Bal. Account Type** and **Bal. Account No.** fields are not included in the standard layout of the invoice header.</span></span> <span data-ttu-id="299ce-113">Til að bóka greiðslu á reikningi verður fyrst að hafa samband við samstarfsaðila Microsoft sem getur bætt reitunum við með kóða.</span><span class="sxs-lookup"><span data-stu-id="299ce-113">In order to post the payment of an invoice, you must contact a Microsoft partner who can add the fields through code.</span></span>  
>
> <span data-ttu-id="299ce-114">Þessi sérstilling er aðeins nauðsynleg ef ekki eru tilgreindir mótreikningar á greiðslumátunum eins og lýst er að ofan.</span><span class="sxs-lookup"><span data-stu-id="299ce-114">This customization is only required if you do not specify balancing accounts on the payment methods as describe above.</span></span>

## <a name="see-also"></a><span data-ttu-id="299ce-115">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="299ce-115">See Also</span></span>

[<span data-ttu-id="299ce-116">Stjórna skuldum</span><span class="sxs-lookup"><span data-stu-id="299ce-116">Managing Payables</span></span>](payables-manage-payables.md)  
[<span data-ttu-id="299ce-117">Innkaup</span><span class="sxs-lookup"><span data-stu-id="299ce-117">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="299ce-118">[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="299ce-118">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  


[!INCLUDE[footer-include](includes/footer-banner.md)]