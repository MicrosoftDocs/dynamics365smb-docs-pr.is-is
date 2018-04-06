---
title: "Skrá útgjöld og tekjur beint í fjárhag| Microsoft Docs"
description: "Fyrir fyrirtækjaaðgerðir sem ekki eru táknaðar með fylgiskjölum í, eins og smærri útgjöld og inngreiðslur, er hægt að búa til færslur sem tengjast aðgerðunum með því að stofna færslubókarlínu í glugganum Fjárhagur."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: direct posting, general ledger
ms.date: 06/28/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: b7e1fc0cda3dadfac73cf0c9a2e599aa78d06bd6
ms.contentlocale: is-is
ms.lasthandoff: 03/22/2018

---
# <a name="post-transactions-directly-to-the-general-ledger"></a><span data-ttu-id="7d7ff-103">Bóka færslu beint í Fjárhag</span><span class="sxs-lookup"><span data-stu-id="7d7ff-103">Post Transactions Directly to the General Ledger</span></span>
<span data-ttu-id="7d7ff-104">Flestar fjárhagsfærslur eru bókaðar í fjárhag gegnum sérstök viðskiptaskjöl, eins og innkaupareikninga og sölupantanir.</span><span class="sxs-lookup"><span data-stu-id="7d7ff-104">Most financial transactions are posted to the general ledger through dedicated business documents, such as purchase invoices and sales orders.</span></span> <span data-ttu-id="7d7ff-105">Fyrir fyrirtækjaaðgerðir sem ekki eru táknaðar með fylgiskjölum í [!INCLUDE[d365fin](includes/d365fin_md.md)], eins og smærri útgjöld og inngreiðslur, er hægt að búa til færslur sem tengjast aðgerðunum með því að stofna færslubókarlínu í glugganum **Fjárhagur**.</span><span class="sxs-lookup"><span data-stu-id="7d7ff-105">For business activities that are not represented by a document in [!INCLUDE[d365fin](includes/d365fin_md.md)], such as smaller expenses or cash receipts, you can create the related transactions by posting journal lines in the **General Journal** window.</span></span>

<span data-ttu-id="7d7ff-106">Hefðbundin notkun færslubókarinnar er að bóka starfsmannaútgjöld, þar sem þeir nota eigin peninga í viðskiptaerindum, fyrir seinni tíma endurgreiðslu.</span><span class="sxs-lookup"><span data-stu-id="7d7ff-106">A typical use of the general journal is to post employees' expenditure of own money during business activities, for later reimbursement.</span></span> <span data-ttu-id="7d7ff-107">Nánari upplýsingar eru í [Skrá og endurgreiða starfsmannaútgjöld](finance-how-record-reimburse-employee-expenses.md).</span><span class="sxs-lookup"><span data-stu-id="7d7ff-107">For more information, see [Record and Reimburse Employees' Expenses](finance-how-record-reimburse-employee-expenses.md).</span></span>

<span data-ttu-id="7d7ff-108">Færslubækur bóka fjárhagsfærslur beint í fjárhagsreikninga og aðra reikninga, svo sem banka-, viðskiptamanna-, lánardrottna- og starfsmannareikninga.</span><span class="sxs-lookup"><span data-stu-id="7d7ff-108">General journals post financial transactions directly to general ledger accounts and other accounts, such as bank, customer, vendor, and employee accounts.</span></span> <span data-ttu-id="7d7ff-109">Bókun með almennri færslubók stofnar alltaf færslur á fjárhagsreikningum.</span><span class="sxs-lookup"><span data-stu-id="7d7ff-109">Posting with a general journal always creates entries on general ledger accounts.</span></span> <span data-ttu-id="7d7ff-110">Slíkt á við jafnvel í tilvikum þegar færslubókarlína er bókuð á reikning viðskiptamanns, vegna þess að færsla er bókuð í safnreikning færslubókar með bókunarflokki.</span><span class="sxs-lookup"><span data-stu-id="7d7ff-110">This is true even when, for example, you post a journal line to a customer account, because an entry is posted to a general ledger receivables account through a posting group.</span></span> <span data-ttu-id="7d7ff-111">Hægt er að sérsníða þína útgáfu af færslubók með því að setja upp bókakeyrslu eða sniðmát.</span><span class="sxs-lookup"><span data-stu-id="7d7ff-111">You can personalize your version of a general journal by setting up a journal batch or template.</span></span> <span data-ttu-id="7d7ff-112">Frekari upplýsingar, sjá [Vinna með almennar færslubækur](ui-work-general-journals.md).</span><span class="sxs-lookup"><span data-stu-id="7d7ff-112">For more information, see [Working with General Journals](ui-work-general-journals.md).</span></span>

<span data-ttu-id="7d7ff-113">Ólíkt því sem gerist þegar færslur eru bókaðar með fylgiskjölum, sem krefst kreditreikningsferlis, getur þú réttilega bakfært færslur sem eru bókaðar með fjárhagnum.</span><span class="sxs-lookup"><span data-stu-id="7d7ff-113">Unlike for entries that are posted with documents, which require a credit memo process, you can correctly reverse entries that are posted with the general journal.</span></span> <span data-ttu-id="7d7ff-114">Frekari upplýsingar eru í [Bakfæra bókanir](finance-how-reverse-journal-posting.md).</span><span class="sxs-lookup"><span data-stu-id="7d7ff-114">For more information, see [Reverse Postings](finance-how-reverse-journal-posting.md).</span></span>

## <a name="to-post-a-transaction-directly-to-a-general-ledger-account"></a><span data-ttu-id="7d7ff-115">Að bóka færslu beint í fjárhagsreikning</span><span class="sxs-lookup"><span data-stu-id="7d7ff-115">To post a transaction directly to a general ledger account</span></span>
1. <span data-ttu-id="7d7ff-116">Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **færslubók** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="7d7ff-116">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **General Journals**, and then choose the related link.</span></span>
2. <span data-ttu-id="7d7ff-117">Viðeigandi færslubók keyrsla er opnaður.</span><span class="sxs-lookup"><span data-stu-id="7d7ff-117">Open the relevant general journal batch.</span></span> <span data-ttu-id="7d7ff-118">Frekari upplýsingar, sjá [Vinna með almennar færslubækur](ui-work-general-journals.md).</span><span class="sxs-lookup"><span data-stu-id="7d7ff-118">For more information, see [Working with General Journals](ui-work-general-journals.md).</span></span>
3. <span data-ttu-id="7d7ff-119">Fyllið í reitina eftir þörfum í nýrri færslubókarlínu.</span><span class="sxs-lookup"><span data-stu-id="7d7ff-119">On a new journal line, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]    
4. <span data-ttu-id="7d7ff-120">Endurtakið skref 3 fyrir allar aðskildar færslur sem þú vilt bóka.</span><span class="sxs-lookup"><span data-stu-id="7d7ff-120">Repeat step 3 for all the separate transactions that you want to post.</span></span>

    > [!TIP]  
    > <span data-ttu-id="7d7ff-121">Ef þú vilt færa inn fleiri færslulínur fyrir ofan eina mótreikningslínu, til dæmis fyrir einn bankareikning, skaltu velja gátreitinn **Leggja til afstemmingarupphæð** á línunni fyrir þína keyrslu í glugganum **færslubókakeyrslur**.</span><span class="sxs-lookup"><span data-stu-id="7d7ff-121">If you want to enter multiple transaction lines above one balance-account line, for example, for one bank account, then select the **Suggest Balancing Amount** check box on the line for your batch in the **General Journal Batches** window.</span></span> <span data-ttu-id="7d7ff-122">Þá verður reiturinn **Upphæð** á mótreikningslínunni sjálfkrafa fylltur út með gildinu sem er nauðsynlegt til að jafna skjalið.</span><span class="sxs-lookup"><span data-stu-id="7d7ff-122">Then the **Amount** field on the balance-account line is automatically prefilled with the value that is required to balance the transactions.</span></span>
5. <span data-ttu-id="7d7ff-123">Veljið **Bóka** aðgerðina til að skrá færslurnar á tilteknu fjárhagsreikningana.</span><span class="sxs-lookup"><span data-stu-id="7d7ff-123">Choose the **Post** action to record the transactions on the specified G/L accounts.</span></span>

## <a name="see-also"></a><span data-ttu-id="7d7ff-124">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="7d7ff-124">See Also</span></span>
[<span data-ttu-id="7d7ff-125">Vinna í færslubókum</span><span class="sxs-lookup"><span data-stu-id="7d7ff-125">Working with General Journals</span></span>](ui-work-general-journals.md)  
[<span data-ttu-id="7d7ff-126">Skrá og endurgreiða starfsmannaútgjöld</span><span class="sxs-lookup"><span data-stu-id="7d7ff-126">Record and Reimburse Employees' Expenses</span></span>](finance-how-record-reimburse-employee-expenses.md)  
[<span data-ttu-id="7d7ff-127">Bakfæra bókanir</span><span class="sxs-lookup"><span data-stu-id="7d7ff-127">Reverse Postings</span></span>](finance-how-reverse-journal-posting.md)  
[<span data-ttu-id="7d7ff-128">Fjármál</span><span class="sxs-lookup"><span data-stu-id="7d7ff-128">Finance</span></span>](finance.md)  
<span data-ttu-id="7d7ff-129">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="7d7ff-129">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

