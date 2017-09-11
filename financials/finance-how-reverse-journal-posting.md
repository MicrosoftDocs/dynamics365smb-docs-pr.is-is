---
title: "Afturkalla bókun færslubókar með bókun bakfærslu| Microsoft Docs"
description: "Ef þú hefur framkvæmt ranga bókun í færslubók, geturðu notað bakfærsluaðgerðina til að afturkalla bókunina með réttri endurskoðunarslóð."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reimbursement
ms.date: 06/15/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 8126a53d59e72276eb1558fd65fe3c0cd53600cc
ms.contentlocale: is-is
ms.lasthandoff: 09/11/2017

---
# <a name="how-to-reverse-journal-posting"></a><span data-ttu-id="ceac4-103">Hvernig skal: Bakfæra bókun færslubókar</span><span class="sxs-lookup"><span data-stu-id="ceac4-103">How to: Reverse Journal Posting</span></span>
<span data-ttu-id="ceac4-104">Til að afturkalla ranga bókun færslubókar skal velja færsluna og búa til bakfærslu (færsla sem er alveg eins og upphaflega færslan en með andstæðu tákni í reitnum fyrir upphæð) með sama skjalanúmeri og bókunardagsetningu og upphaflega færslan.</span><span class="sxs-lookup"><span data-stu-id="ceac4-104">To undo an erroneous journal posting, you select the entry and create a reverse entry (entries identical to the original entry but with opposite sign in the amount field) with the same document number and posting date as the original entry.</span></span> <span data-ttu-id="ceac4-105">Þegar færsla hefur verið bakfærð þarf að búa til rétta færslu.</span><span class="sxs-lookup"><span data-stu-id="ceac4-105">After reversing an entry, you must make the correct entry.</span></span>

<span data-ttu-id="ceac4-106">Aðeins er hægt að bakfæra færslu sem er bókuð frá færslubókarlínu.</span><span class="sxs-lookup"><span data-stu-id="ceac4-106">You can only reverse entries that are posted from a general journal line.</span></span> <span data-ttu-id="ceac4-107">Færslu er einungis hægt að bakfæra einu sinni.</span><span class="sxs-lookup"><span data-stu-id="ceac4-107">An entry can only be reversed once.</span></span>

<span data-ttu-id="ceac4-108">Frekari upplýsingar um bókun frá færslubók, sjá [Hvernig skal: Bóka færslur beint í fjárhag](finance-how-post-transactions-directly.md)</span><span class="sxs-lookup"><span data-stu-id="ceac4-108">For more information about posting from a general journal, see [How to: Post Transactions Directly to the General Ledger](finance-how-post-transactions-directly.md).</span></span>

<span data-ttu-id="ceac4-109">Hægt er að bakfæra færslur úr öllum **Fjárhagsfærslur** gluggum.</span><span class="sxs-lookup"><span data-stu-id="ceac4-109">You can reverse entries from all **Ledger Entries** windows.</span></span> <span data-ttu-id="ceac4-110">Eftirfarandi ferli byggist á **Fjárhagsfærslur** glugganum.</span><span class="sxs-lookup"><span data-stu-id="ceac4-110">The following procedure is based on the **General Ledger Entries** window.</span></span>

## <a name="to-reverse-the-journal-posting-of-a-general-ledger-entry"></a><span data-ttu-id="ceac4-111">Að bakfæra færslubókarbókun fjárhagsfærslu</span><span class="sxs-lookup"><span data-stu-id="ceac4-111">To reverse the journal posting of a general ledger entry</span></span>
1. <span data-ttu-id="ceac4-112">Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Fjárhagsfærslur** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="ceac4-112">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **General Ledger Entries**, and then choose the related link.</span></span>
2. <span data-ttu-id="ceac4-113">Veljið færsluna sem á að bakfæra og veljið síðna aðgerðina **Bakfæra færslu**.</span><span class="sxs-lookup"><span data-stu-id="ceac4-113">Select the entry that you want to reverse, and then choose the **Reverse Transaction** action.</span></span> <span data-ttu-id="ceac4-114">Athugið að þetta verður að koma úr bókun færslubókar.</span><span class="sxs-lookup"><span data-stu-id="ceac4-114">Note that is must originate from a journal posting.</span></span>
3. <span data-ttu-id="ceac4-115">Í glugganum **Bakfærðar viðskiptafærslur** skal velja viðeigandi línu og svo aðgerðina **Bakfæra**.</span><span class="sxs-lookup"><span data-stu-id="ceac4-115">In the **Reverse Transaction Entries** window, select the relevant entry, and then choose the **Reverse** action.</span></span>
4. <span data-ttu-id="ceac4-116">Velja hnappinn **Já** á staðfestingarskilaboðunum.</span><span class="sxs-lookup"><span data-stu-id="ceac4-116">Choose the **Yes** button on the confirmation message.</span></span>

## <a name="see-also"></a><span data-ttu-id="ceac4-117">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="ceac4-117">See Also</span></span>
[<span data-ttu-id="ceac4-118">Hvernig skal: Bóka færslu beint í Fjárhag</span><span class="sxs-lookup"><span data-stu-id="ceac4-118">How to: Post Transactions Directly to the General Ledger</span></span>](finance-how-post-transactions-directly.md)  
[<span data-ttu-id="ceac4-119">Vinna í færslubókum</span><span class="sxs-lookup"><span data-stu-id="ceac4-119">Working with General Journals</span></span>](ui-work-general-journals.md)  
[<span data-ttu-id="ceac4-120">Fjármál</span><span class="sxs-lookup"><span data-stu-id="ceac4-120">Finance</span></span>](finance.md)  
<span data-ttu-id="ceac4-121">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="ceac4-121">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

