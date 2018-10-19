---
title: "Hvernig á að flytja fjárhagsfærslur í kostnaðarfærslur | Microsoft Docs"
description: "Hægt er að flytja fjárhagsfærslur í kostnaðarfærslur"
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 62ed00ef7ca278245b9cdd1a28a4ee70cf9a8f11
ms.contentlocale: is-is
ms.lasthandoff: 09/28/2018

---
# <a name="transfer-general-ledger-entries-to-cost-entries"></a><span data-ttu-id="c8166-103">Flytja fjárhagsfærslur í kostnaðarfærslur</span><span class="sxs-lookup"><span data-stu-id="c8166-103">Transfer General Ledger Entries to Cost Entries</span></span>
<span data-ttu-id="c8166-104">Hægt er að flytja fjárhagsfærslur í kostnaðarfærslur</span><span class="sxs-lookup"><span data-stu-id="c8166-104">You can transfer general ledger entries to cost entries.</span></span>  

<span data-ttu-id="c8166-105">Áður en ferlið til að flytja fjárhagsfærslur til kostnaðarfærslna er keyrt, þarf að undirbúa flutninginn til að forðast handvirka leiðréttingarbókun.</span><span class="sxs-lookup"><span data-stu-id="c8166-105">Before you run the process for transferring general ledger entries to cost entries, you must prepare the transfer to avoid manual correction posting.</span></span>  

## <a name="to-prepare-the-transfer"></a><span data-ttu-id="c8166-106">Til að undirbúa færsluna</span><span class="sxs-lookup"><span data-stu-id="c8166-106">To prepare the transfer</span></span>  

1.  <span data-ttu-id="c8166-107">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Uppsetning kostnaðarbókahalds** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="c8166-107">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Cost Accounting Setup**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="c8166-108">Í glugganum **Uppsetning kostnaðarbókhalds** skal ganga úr skugga um að reiturinn **Upphafsdagur fyrir fjárhagsfærslur** sé stilltur á rétt gildi.</span><span class="sxs-lookup"><span data-stu-id="c8166-108">In the **Cost Accounting Setup** window, verify that the **Starting Date for G/L Transfer** field is set to the correct value.</span></span>  
3.  <span data-ttu-id="c8166-109">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Myndrit yfir kostnaðargerðir** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="c8166-109">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Chart of Cost Types**, and then choose the related link.</span></span>  
4.  <span data-ttu-id="c8166-110">Í glugganum **Kostnaðargerðarspjald** skal ganga úr skugga um að reiturinn **Fjárhagsreikningssvið** sé tengdur rétt þannig að hver kostnaðargerð taki færslur úr fjárhag.</span><span class="sxs-lookup"><span data-stu-id="c8166-110">In the **Cost Type Card** window, verify that the **G/L Account Range** field is linked correctly for each cost type to take entries from the general ledger.</span></span>  
5.  <span data-ttu-id="c8166-111">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **bókhaldslykill** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="c8166-111">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Chart of Accounts**, and then choose the related link.</span></span>  
6.  <span data-ttu-id="c8166-112">Fyrir hvern viðeigandi fjárhagsreikning, í glugganum **Fjárhagsreikningsspjald**, skal sannreyna að reiturinn **Kostnaðargerð nr.**</span><span class="sxs-lookup"><span data-stu-id="c8166-112">For each relevant general ledger account, in the **G/L Account Card** window, verify that the **Cost Type No.**</span></span> <span data-ttu-id="c8166-113">sé rétt tengdur í kostnaðartegund.</span><span class="sxs-lookup"><span data-stu-id="c8166-113">field is linked correctly to a cost type.</span></span> <span data-ttu-id="c8166-114">Frekari upplýsingar, sjá [Skilgreining á venslum milli kostnaðargerða og fjárhagsreikninga](finance-defining-the-relationship-between-cost-types-and-general-ledger-accounts.md).</span><span class="sxs-lookup"><span data-stu-id="c8166-114">For more information, see [Defining the Relationship Between Cost Types and General Ledger Accounts](finance-defining-the-relationship-between-cost-types-and-general-ledger-accounts.md).</span></span>  
7.  <span data-ttu-id="c8166-115">Staðfesta að allar viðeigandi fjárhagsfærslur hafa víddargildi sem samsvara kostnaðarstað og kostnaðarhlut.</span><span class="sxs-lookup"><span data-stu-id="c8166-115">Verify that all relevant general ledger entries have dimension values that correspond to a cost center and a cost object.</span></span>  

## <a name="to-transfer-general-ledger-entries-to-cost-entries"></a><span data-ttu-id="c8166-116">Til að færa fjárhagsfærslur yfir í kostnaðarfærslur</span><span class="sxs-lookup"><span data-stu-id="c8166-116">To transfer general ledger entries to cost entries</span></span>  
1.  <span data-ttu-id="c8166-117">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Flytja fjárhagsfærslur til vottorðaútgefanda** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="c8166-117">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Transfer GL Entries to CA**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="c8166-118">Velja hnappinn **Já** til að hefja millifærsluna.</span><span class="sxs-lookup"><span data-stu-id="c8166-118">Choose the **Yes** button to start the transfer.</span></span> <span data-ttu-id="c8166-119">Ferlið færir allar fjárhagsfærslur sem hafa ekki þegar verið færðar.</span><span class="sxs-lookup"><span data-stu-id="c8166-119">The process transfers all general ledger entries that have not already been transferred.</span></span>  

    <span data-ttu-id="c8166-120">Meðan á millifærslu stendur býr ferlið til tengingar í færslurnar í töflunni **Kostnaðarfærsla** og töflunni **Kostnaðarskráning**.</span><span class="sxs-lookup"><span data-stu-id="c8166-120">During the transfer, the process creates connections in the entries in the **Cost Entry** table and the **Cost Register** table.</span></span> <span data-ttu-id="c8166-121">Þannig er hægt að rekja uppruna kostnaðarfærsla.</span><span class="sxs-lookup"><span data-stu-id="c8166-121">This makes it possible to trace the source of cost entries.</span></span>  

## <a name="see-also"></a><span data-ttu-id="c8166-122">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="c8166-122">See Also</span></span>  
 <span data-ttu-id="c8166-123">[Skilyrði til að millifærslu fjárhagsfærslna í kostnaðarfærslur](finance-criteria-for-transferring-general-ledger-entries-to-cost-entries.md) </span><span class="sxs-lookup"><span data-stu-id="c8166-123">[Criteria for Transferring General Ledger Entries to Cost Entries](finance-criteria-for-transferring-general-ledger-entries-to-cost-entries.md) </span></span>  
 <span data-ttu-id="c8166-124">[Sjálfvirkur flutningur og færslur sameinaðar](finance-automatic-transfer-combined-entries.md) </span><span class="sxs-lookup"><span data-stu-id="c8166-124">[Automatic Transfer and Combined Entries](finance-automatic-transfer-combined-entries.md) </span></span>  
 <span data-ttu-id="c8166-125">[Niðurstöður millifærslu](finance-results-of-the-transfer.md) </span><span class="sxs-lookup"><span data-stu-id="c8166-125">[Results of the Transfer](finance-results-of-the-transfer.md) </span></span>  
 <span data-ttu-id="c8166-126">[Flytja og bóka kostnaðarfærslur](finance-transfer-and-post-cost-entries.md) </span><span class="sxs-lookup"><span data-stu-id="c8166-126">[Transferring and Posting Cost Entries](finance-transfer-and-post-cost-entries.md) </span></span>  
 [<span data-ttu-id="c8166-127">Skilgreining á venslum milli kostnaðargerða og fjárhagsreikninga</span><span class="sxs-lookup"><span data-stu-id="c8166-127">Defining the Relationship Between Cost Types and General Ledger Accounts</span></span>](finance-defining-the-relationship-between-cost-types-and-general-ledger-accounts.md)   

