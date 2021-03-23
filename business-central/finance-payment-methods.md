---
title: Setja upp greiðsluhætti
description: Greiðsluhættir eru notaðir, til dæmis ávísun, bankamillifærsla, reiðufé eða PayPal, til að tilgreina hvernig sölu- og innkaupareikningar verða greiddir.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: check, bank transfer, cash, PayPal
ms.date: 01/21/2021
ms.author: bholtorf
ms.openlocfilehash: 7132f96327e468c200ebd1f41c0a1e5b767dea6b
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5376838"
---
# <a name="set-up-payment-methods"></a><span data-ttu-id="af070-103">Setja upp greiðsluhætti</span><span class="sxs-lookup"><span data-stu-id="af070-103">Set Up Payment Methods</span></span>

<span data-ttu-id="af070-104">Greiðsluhættir skilgreina hvernig þú vilt að viðskiptavinir greiði þér og hvernig þú vilt greiða lánardrottnum þínum.</span><span class="sxs-lookup"><span data-stu-id="af070-104">Payment methods define the way you prefer for customers to pay you, and how you like to pay your vendors.</span></span> <span data-ttu-id="af070-105">Greiðslumátinn getur verið breytilegur fyrir hvern viðskiptavin eða lánardrottin.</span><span class="sxs-lookup"><span data-stu-id="af070-105">The method can vary for each customer or vendor.</span></span> <span data-ttu-id="af070-106">Dæmi um dæmigerða greiðsluhætti eru **banki**, **reiðufé**, **ávísun** eða **reikningur**.</span><span class="sxs-lookup"><span data-stu-id="af070-106">Examples of typical payment methods are **bank**, **cash**, **check**, or **account**.</span></span>

<span data-ttu-id="af070-107">Þú getur úthlutað greiðslumáta til viðskiptavina og lánardrottna þannig að sama aðferðin sé alltaf notuð á sölu- og innkaupskjölunum sem þú býrð til fyrir þá.</span><span class="sxs-lookup"><span data-stu-id="af070-107">You can assign a payment method to customers and vendors so that the same method is always used on the sales and purchase documents you create for them.</span></span> <span data-ttu-id="af070-108">Hægt er að breyta greiðslumátanum í sölu- og innkaupaskjalinu ef þörf krefur.</span><span class="sxs-lookup"><span data-stu-id="af070-108">If needed, you can change the method on the sales or purchase document.</span></span> <span data-ttu-id="af070-109">Til dæmis, ef þú vilt greiða ákveðinn innkaupareikning í reiðufé frekar en með ávísun.</span><span class="sxs-lookup"><span data-stu-id="af070-109">For example, if you want to pay a particular purchase invoice in cash rather than by check.</span></span> <span data-ttu-id="af070-110">Þetta breytir ekki sjálfgefna greiðslumátanum sem lánardrottninum er úthlutað.</span><span class="sxs-lookup"><span data-stu-id="af070-110">This does not change the default payment method assigned to the vendor.</span></span>

<span data-ttu-id="af070-111">Sömu greiðsluaðferðir eru notaðar fyrir sölu- og innkaupaskjöl.</span><span class="sxs-lookup"><span data-stu-id="af070-111">The same payment methods are used for sales and purchase documents.</span></span> <span data-ttu-id="af070-112">Til dæmis er greiðslumátinn _reiðufé_ notaður bæði þegar þú greiðir og þegar þú færð greitt.</span><span class="sxs-lookup"><span data-stu-id="af070-112">For example, a _cash_ payment method is used both when you make payments and when you receive them.</span></span> [!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="af070-113">veit að þegar þú ert að búa til sölureikning þá býstu við að fá greiðslur og hið gagnstæða fyrir innkaupareikninga.</span><span class="sxs-lookup"><span data-stu-id="af070-113">knows that when you are creating a sales invoice you expect to receive payment, and the opposite for purchase invoices.</span></span>

<span data-ttu-id="af070-114">Kreditreikningar vegna skila eru þó undantekningar vegna þess að peningar flæða í gagnstæða átt, frá þér til viðskiptavina og frá lánardrottni til þín.</span><span class="sxs-lookup"><span data-stu-id="af070-114">Credit memos for returns, however, are exceptions because money is flowing in the opposite directions, from you to your customer and from your vendor to you.</span></span> <span data-ttu-id="af070-115">Þess vegna er sjálfgefnum greiðslumáta ekki úthlutað á kreditreikninga.</span><span class="sxs-lookup"><span data-stu-id="af070-115">Therefore, a default payment method is not assigned to credit memos.</span></span> <span data-ttu-id="af070-116">Það er hins vegar til hjáleið ef þú hefur tilgreint greiðsluskilmála fyrir viðskiptavin eða lánardrottin.</span><span class="sxs-lookup"><span data-stu-id="af070-116">There is, however, a workaround if you have specified terms of payment for the customer or vendor.</span></span> <span data-ttu-id="af070-117">Þótt reiturinn **Reikna greiðsluafsl. af kreditreikn.** er ekki ætlaður fyrir þetta, ef þú velur gátreitinn á síðunni **Greiðsluskilmálar**, verður sjálfgefnum greiðslumáta bætt við þegar þú stofnar kreditreikning.</span><span class="sxs-lookup"><span data-stu-id="af070-117">Though the **Calc. Pmt. Disc. on Cr. Memos** field is not intended for this, if you choose the check box on the **Payment Terms** page a default payment method will be added when you create a credit memo.</span></span> <br><br>  

> [!Video https://www.microsoft.com/videoplayer/embed/RE476Ys?rel=0]

## <a name="to-set-up-a-payment-method"></a><span data-ttu-id="af070-118">Greiðsluaðferðir settar upp</span><span class="sxs-lookup"><span data-stu-id="af070-118">To set up a payment method</span></span>

[!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="af070-119">veitir nokkrar greiðsluaðferðir sem fyrirtæki nota oft.</span><span class="sxs-lookup"><span data-stu-id="af070-119">provides a few payment methods that businesses often use.</span></span> <span data-ttu-id="af070-120">Þó er hægt að bæta við eins mörgum og þörf krefur.</span><span class="sxs-lookup"><span data-stu-id="af070-120">You can, however, add as many as you need.</span></span>

1. <span data-ttu-id="af070-121">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Greiðslumáti** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="af070-121">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Payment Methods**, and then choose the related link.</span></span>
2. <span data-ttu-id="af070-122">Fyllið inn reitina eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="af070-122">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

<span data-ttu-id="af070-123">Þú getur einnig bætt við greiðsluskilmálum við greiðslumátann þinn.</span><span class="sxs-lookup"><span data-stu-id="af070-123">Optionally, add payment terms to your payment method.</span></span> <span data-ttu-id="af070-124">Nánari upplýsingar um það eru í [Setja upp greiðsluskilmála](finance-payment-terms.md).</span><span class="sxs-lookup"><span data-stu-id="af070-124">For more information, see [Set Up Payment Terms](finance-payment-terms.md).</span></span>  

## <a name="to-assign-a-payment-method-to-a-customer-or-vendor"></a><span data-ttu-id="af070-125">Viðskiptavinum eða lánardrottnum úthlutaður greiðslumáti</span><span class="sxs-lookup"><span data-stu-id="af070-125">To assign a payment method to a customer or vendor</span></span>

1. <span data-ttu-id="af070-126">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Viðskiptamaður** eða **Lánardrottinn** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="af070-126">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Customer** or **Vendor**, and then choose the related link.</span></span>
2. <span data-ttu-id="af070-127">Í reitnum **Kóði greiðslumáta** skal velja greiðslumátann sem á að nota að sjálfgefnu viðskiptavin eða lánardrottin.</span><span class="sxs-lookup"><span data-stu-id="af070-127">In the **Payment Method Code** field, choose the method to use by default for the customer or vendor.</span></span>

## <a name="see-also"></a><span data-ttu-id="af070-128">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="af070-128">See Also</span></span>

[<span data-ttu-id="af070-129">Skrá nýja viðskiptamenn</span><span class="sxs-lookup"><span data-stu-id="af070-129">Register New Customers</span></span>](sales-how-register-new-customers.md)  
[<span data-ttu-id="af070-130">Setja upp greiðsluskilmála</span><span class="sxs-lookup"><span data-stu-id="af070-130">Set Up Payment Terms</span></span>](finance-payment-terms.md)  
[<span data-ttu-id="af070-131">Fjármál</span><span class="sxs-lookup"><span data-stu-id="af070-131">Finance</span></span>](finance.md)  
<span data-ttu-id="af070-132">[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="af070-132">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  


[!INCLUDE[footer-include](includes/footer-banner.md)]