---
title: Flytja inn launafærslur| Microsoft Docs
description: Þegar launum er stjórnað, eru fjárhagsfærslur fluttar inn og bókaðar frá launaveitu til fjárhags, með því að nota launaviðbætur eins og Ceridian eða Quickbooks.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Ceridian, Quickbooks, salary
ms.date: 04/01/2019
ms.author: SorenGP
ms.openlocfilehash: c483b50e7f1456c06ace27d3893c04a3d59e6ab8
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2019
ms.locfileid: "924972"
---
# <a name="import-payroll-transactions"></a><span data-ttu-id="48d34-103">Flytja inn launafærslur</span><span class="sxs-lookup"><span data-stu-id="48d34-103">Import Payroll Transactions</span></span>
<span data-ttu-id="48d34-104">Fyrir launagreiðslur og tengdar færslur verður að flytja inn og birta fjárhagslegar færslur úr launaveitu í fjárhag.</span><span class="sxs-lookup"><span data-stu-id="48d34-104">To account for salary payments and related transactions, you must import and post financial transactions made by your payroll provider to the general ledger.</span></span> <span data-ttu-id="48d34-105">Fyrir þetta þarf fyrst að flytja inn skrá úr launaveitu yfir á síðuna **Færslubók**.</span><span class="sxs-lookup"><span data-stu-id="48d34-105">To do this, you first import a file that you receive from the payroll provider into the **General Journal** page.</span></span> <span data-ttu-id="48d34-106">Síðan varparðu ytri reikningunum í skránni launagreiðslur á viðeigandi fjárhagsreikninga.</span><span class="sxs-lookup"><span data-stu-id="48d34-106">Then you map the external accounts in the payroll file to the relevant G/L accounts.</span></span> <span data-ttu-id="48d34-107">Að lokum bókarðu launafærslur samkvæmt reikningsvörpuninni.</span><span class="sxs-lookup"><span data-stu-id="48d34-107">Lastly, you post the payroll transactions according to the account mapping.</span></span>

> [!NOTE]  
>   <span data-ttu-id="48d34-108">Til að nota þessa aðgerð þarf viðbót fyrir innflutning launa að vera uppsett og virkjuð.</span><span class="sxs-lookup"><span data-stu-id="48d34-108">To use this functionality, an extension for payroll import must be installed and enabled.</span></span> <span data-ttu-id="48d34-109">The Ceridian Payroll og Quickbooks Payroll File Import eftirnafn eru fyrirfram uppsett í [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="48d34-109">The Ceridian Payroll and the Quickbooks Payroll File Import extensions are pre-installed in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="48d34-110">Frekari upplýsingar skoða [Sérstilla [!INCLUDE[d365fin](includes/d365fin_md.md)] Nota viðbætur](ui-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="48d34-110">For more information, see [Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions](ui-extensions.md).</span></span>

## <a name="to-import-a-payroll-file"></a><span data-ttu-id="48d34-111">Til að flytja inn launaskrá</span><span class="sxs-lookup"><span data-stu-id="48d34-111">To import a payroll file</span></span>
1. <span data-ttu-id="48d34-112">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Færslubækur** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="48d34-112">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **General Journals**, and then choose the related link.</span></span>
2. <span data-ttu-id="48d34-113">Í viðkomandi færslubókarkeyrslu skal velja **Flytja inn launafærslur**.</span><span class="sxs-lookup"><span data-stu-id="48d34-113">In the relevant general journal batch, choose the **Import Payroll Transactions** action.</span></span> <span data-ttu-id="48d34-114">Uppsetning með hjálp opnast.</span><span class="sxs-lookup"><span data-stu-id="48d34-114">An assisted setup guide opens.</span></span>
3. <span data-ttu-id="48d34-115">Fylgdu skrefunum á síðunni **Flytja inn launafærslur**.</span><span class="sxs-lookup"><span data-stu-id="48d34-115">Follow the steps on the **Import Payroll Transactions** page.</span></span>

    > [!TIP]  
    >   <span data-ttu-id="48d34-116">Í liðnum þar sem ytri launaskrám er varpað í fjárhagsreikningana þína man kerfið þá vörpun næst þegar sömu skýrslur eru fluttar inn.</span><span class="sxs-lookup"><span data-stu-id="48d34-116">In the step about mapping the external payroll records to your G/L accounts, the mappings that you make will be remembered next time the same records are imported.</span></span> <span data-ttu-id="48d34-117">Þetta sparar tíma því ekki þarf að fylla handvirkt inn svæðið **Reikningnúmer** í færslubókinni í hvert skipti sem þú hefur flutt inn ítrekaða launafærslu.</span><span class="sxs-lookup"><span data-stu-id="48d34-117">This will save you time as you do not have to manually fill in the **Account No.** field in the general journal every time you have imported recurring payroll transactions.</span></span>   

    <span data-ttu-id="48d34-118">Þegar hnappurinn **Í lagi** er valinn í uppsetningu með leiðsögn er síðan **Almenn færslubók** fullur af línum sem tákna færslurnar sem launaskráin innheldur og búið er að fylla út tilheyrandi lykla í reitunum **Fjárhagsreikningur** í samræmi við þá vörpun sem gerð var í leiðsögninni.</span><span class="sxs-lookup"><span data-stu-id="48d34-118">When you choose the **OK** button in the assisted setup guide, the **General Journal** page is filled with lines representing the transactions that the payroll file contains and with the relevant accounts prefilled in the **G/L Account** fields according to mappings you made in the guide.</span></span>
4. <span data-ttu-id="48d34-119">Breyta skal eða bóka færslubókarlínur líkt og fyrir allar aðrar færslur í fjárhag.</span><span class="sxs-lookup"><span data-stu-id="48d34-119">Edit or post the journal lines as for any other general ledger transactions.</span></span> <span data-ttu-id="48d34-120">Frekari upplýsingar, sjá [Bóka færslu beint yfir í Fjárhag](finance-how-post-transactions-directly.md).</span><span class="sxs-lookup"><span data-stu-id="48d34-120">For more information, see [Post Transactions Directly to the General Ledger](finance-how-post-transactions-directly.md).</span></span>   

## <a name="see-also"></a><span data-ttu-id="48d34-121">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="48d34-121">See Also</span></span>
[<span data-ttu-id="48d34-122">Fjármál</span><span class="sxs-lookup"><span data-stu-id="48d34-122">Finance</span></span>](finance.md)  
<span data-ttu-id="48d34-123">[Sérstilling [!INCLUDE[d365fin](includes/d365fin_md.md)] með viðbótum](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="48d34-123">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions](ui-extensions.md)</span></span>  
[<span data-ttu-id="48d34-124">Vinna í færslubókum</span><span class="sxs-lookup"><span data-stu-id="48d34-124">Working with General Journals</span></span>](ui-work-general-journals.md)  
