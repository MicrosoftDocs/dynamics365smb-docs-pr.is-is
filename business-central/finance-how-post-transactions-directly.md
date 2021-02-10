---
title: Skrá útgjöld og tekjur beint í fjárhag| Microsoft Docs
description: Fyrir fyrirtækjaaðgerðir sem ekki eru táknaðar með fylgiskjölum í , eins og smærri útgjöld og inngreiðslur, er hægt að búa til færslur sem tengjast aðgerðunum með því að stofna færslubókarlínu á síðunni Fjárhagur.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: direct posting, general ledger
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 72e2851ee60d6cb79f722d12e16ddcb30e95fdbe
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/17/2020
ms.locfileid: "4746942"
---
# <a name="post-transactions-directly-to-the-general-ledger"></a><span data-ttu-id="d9f0b-103">Bóka færslu beint í Fjárhag</span><span class="sxs-lookup"><span data-stu-id="d9f0b-103">Post Transactions Directly to the General Ledger</span></span>

<span data-ttu-id="d9f0b-104">Nota færslubækur til bóka fjárhagsfærslur beint í fjárhagsreikninga og aðra reikninga, svo sem banka-, viðskiptamanna-, lánardrottna- og starfsmannareikninga.</span><span class="sxs-lookup"><span data-stu-id="d9f0b-104">You use general journals to post financial transactions directly to general ledger accounts and other accounts, such as bank, customer, vendor, and employee accounts.</span></span>  

<span data-ttu-id="d9f0b-105">Hefðbundin notkun færslubókarinnar er að bóka starfsmannaútgjöld, þar sem þeir nota eigin peninga í viðskiptaerindum, fyrir seinni tíma endurgreiðslu.</span><span class="sxs-lookup"><span data-stu-id="d9f0b-105">A typical use of the general journal is to post employees' expenditure of own money during business activities, for later reimbursement.</span></span> <span data-ttu-id="d9f0b-106">Nánari upplýsingar eru í [Skrá og endurgreiða starfsmannaútgjöld](finance-how-record-reimburse-employee-expenses.md).</span><span class="sxs-lookup"><span data-stu-id="d9f0b-106">For more information, see [Record and Reimburse Employees' Expenses](finance-how-record-reimburse-employee-expenses.md).</span></span>

<span data-ttu-id="d9f0b-107">Færslubækur bóka fjárhagsfærslur beint í fjárhagsreikninga og aðra reikninga, svo sem banka-, viðskiptamanna-, lánardrottna- og starfsmannareikninga.</span><span class="sxs-lookup"><span data-stu-id="d9f0b-107">General journals post financial transactions directly to general ledger accounts and other accounts, such as bank, customer, vendor, and employee accounts.</span></span> <span data-ttu-id="d9f0b-108">Bókun með almennri færslubók stofnar alltaf færslur á fjárhagsreikningum.</span><span class="sxs-lookup"><span data-stu-id="d9f0b-108">Posting with a general journal always creates entries on general ledger accounts.</span></span> <span data-ttu-id="d9f0b-109">Slíkt á við jafnvel í tilvikum þegar færslubókarlína er bókuð á reikning viðskiptamanns, vegna þess að færsla er bókuð í safnreikning færslubókar með bókunarflokki.</span><span class="sxs-lookup"><span data-stu-id="d9f0b-109">This is true even when, for example, you post a journal line to a customer account, because an entry is posted to a general ledger receivables account through a posting group.</span></span> <span data-ttu-id="d9f0b-110">Hægt er að sérsníða þína útgáfu af færslubók með því að setja upp bókakeyrslu eða sniðmát.</span><span class="sxs-lookup"><span data-stu-id="d9f0b-110">You can personalize your version of a general journal by setting up a journal batch or template.</span></span> <span data-ttu-id="d9f0b-111">Frekari upplýsingar, sjá [Vinna með almennar færslubækur](ui-work-general-journals.md).</span><span class="sxs-lookup"><span data-stu-id="d9f0b-111">For more information, see [Working with General Journals](ui-work-general-journals.md).</span></span>

<span data-ttu-id="d9f0b-112">Ólíkt því sem gerist þegar færslur eru bókaðar með fylgiskjölum, sem krefst kreditreikningsferlis, getur þú réttilega bakfært færslur sem eru bókaðar með fjárhagnum.</span><span class="sxs-lookup"><span data-stu-id="d9f0b-112">Unlike for entries that are posted with documents, which require a credit memo process, you can correctly reverse entries that are posted with the general journal.</span></span> <span data-ttu-id="d9f0b-113">Frekari upplýsingar er að finna í [Bakfæra bókanir í færslubók og afturkalla kvittanir/sendingar](finance-how-reverse-journal-posting.md).</span><span class="sxs-lookup"><span data-stu-id="d9f0b-113">For more information, see [Reverse Journal Postings and Undo Receipts/Shipments](finance-how-reverse-journal-posting.md).</span></span>

## <a name="to-post-a-transaction-directly-to-a-general-ledger-account"></a><span data-ttu-id="d9f0b-114">Að bóka færslu beint í fjárhagsreikning</span><span class="sxs-lookup"><span data-stu-id="d9f0b-114">To post a transaction directly to a general ledger account</span></span>

1. <span data-ttu-id="d9f0b-115">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Færslubækur** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="d9f0b-115">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **General Journals**, and then choose the related link.</span></span>
2. <span data-ttu-id="d9f0b-116">Viðeigandi færslubók keyrsla er opnaður.</span><span class="sxs-lookup"><span data-stu-id="d9f0b-116">Open the relevant general journal batch.</span></span> <span data-ttu-id="d9f0b-117">Frekari upplýsingar, sjá [Vinna með almennar færslubækur](ui-work-general-journals.md).</span><span class="sxs-lookup"><span data-stu-id="d9f0b-117">For more information, see [Working with General Journals](ui-work-general-journals.md).</span></span>
3. <span data-ttu-id="d9f0b-118">Fyllið í reitina eftir þörfum í nýrri færslubókarlínu.</span><span class="sxs-lookup"><span data-stu-id="d9f0b-118">On a new journal line, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]    

    > [!NOTE]
    > [!INCLUDE[journal-showhide-columns-inline-tip](includes/journal-showhide-columns-inline-tip.md)]
4. <span data-ttu-id="d9f0b-119">Endurtakið skref 3 fyrir allar aðskildar færslur sem þú vilt bóka.</span><span class="sxs-lookup"><span data-stu-id="d9f0b-119">Repeat step 3 for all the separate transactions that you want to post.</span></span>

    > [!TIP]  
    > <span data-ttu-id="d9f0b-120">Ef þú vilt færa inn fleiri færslulínur fyrir ofan eina mótreikningslínu, til dæmis fyrir einn bankareikning, skaltu velja gátreitinn **Leggja til afstemmingarupphæð** á línunni fyrir þína keyrslu á síðunni **færslubókakeyrslur**.</span><span class="sxs-lookup"><span data-stu-id="d9f0b-120">If you want to enter multiple transaction lines above one balance-account line, for example, for one bank account, then select the **Suggest Balancing Amount** check box on the line for your batch on the **General Journal Batches** page.</span></span> <span data-ttu-id="d9f0b-121">Þá verður reiturinn **Upphæð** á mótreikningslínunni sjálfkrafa fylltur út með gildinu sem er nauðsynlegt til að jafna skjalið.</span><span class="sxs-lookup"><span data-stu-id="d9f0b-121">Then the **Amount** field on the balance-account line is automatically prefilled with the value that is required to balance the transactions.</span></span>
5. <span data-ttu-id="d9f0b-122">Veljið **Bóka** aðgerðina til að skrá færslurnar á tilteknu fjárhagsreikningana.</span><span class="sxs-lookup"><span data-stu-id="d9f0b-122">Choose the **Post** action to record the transactions on the specified G/L accounts.</span></span>

## <a name="see-also"></a><span data-ttu-id="d9f0b-123">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="d9f0b-123">See Also</span></span>

[<span data-ttu-id="d9f0b-124">Vinna í færslubókum</span><span class="sxs-lookup"><span data-stu-id="d9f0b-124">Working with General Journals</span></span>](ui-work-general-journals.md)  
[<span data-ttu-id="d9f0b-125">Skrá og endurgreiða starfsmannaútgjöld</span><span class="sxs-lookup"><span data-stu-id="d9f0b-125">Record and Reimburse Employees' Expenses</span></span>](finance-how-record-reimburse-employee-expenses.md)  
[<span data-ttu-id="d9f0b-126">Bakfæra bókanir í færslubók og afturkalla kvittanir/sendingar</span><span class="sxs-lookup"><span data-stu-id="d9f0b-126">Reverse Journal Postings and Undo Receipts/Shipments</span></span>](finance-how-reverse-journal-posting.md)  
[<span data-ttu-id="d9f0b-127">Fjármál</span><span class="sxs-lookup"><span data-stu-id="d9f0b-127">Finance</span></span>](finance.md)  
<span data-ttu-id="d9f0b-128">[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="d9f0b-128">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  
