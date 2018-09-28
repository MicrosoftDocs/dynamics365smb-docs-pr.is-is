---
title: "Niðurstöður millifærslu | Microsoft Docs"
description: "Þetta efnisatriði lýsir því hvað gerist eftir að þú milkliffærir fjárhagsfærslur yfir í kostnaðarfærslur."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: general ledger, transfer, cost entries
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: d171c7764042cd59fe9ca6e0bbce2b4d3d30f050
ms.contentlocale: is-is
ms.lasthandoff: 09/28/2018

---
# <a name="results-of-transferring-general-ledger-entries-to-cost-entries"></a><span data-ttu-id="92e6a-103">Niðurstöður millifærslu fjárhagsfærslna yfir í kostnaðarfærslur</span><span class="sxs-lookup"><span data-stu-id="92e6a-103">Results of Transferring General Ledger Entries to Cost Entries</span></span>
<span data-ttu-id="92e6a-104">Meðan á millifærslu á fjárhagsfærslum í kostnaðarfærslur stendur, stofnar [!INCLUDE[d365fin](includes/d365fin_md.md)] tengingar í færslurnar í töflunni **Fjárhagsfærslur**, töflunni **Kostnaðarfærsla** og töflunni **Kostnaðarskráning** svo hægt sé að rekja tengingar milli kostnaðar- og fjárhagsfærslna.</span><span class="sxs-lookup"><span data-stu-id="92e6a-104">During the transfer of general ledger entries to cost entries, [!INCLUDE[d365fin](includes/d365fin_md.md)] creates connections in the entries in the **G/L Entry** table, the **Cost Entry** table, and the **Cost Register** table to make it possible to trace the connections between cost entries and general ledger entries.</span></span>  

## <a name="general-ledger-entries"></a><span data-ttu-id="92e6a-105">Fjárhagsfærslur</span><span class="sxs-lookup"><span data-stu-id="92e6a-105">General Ledger Entries</span></span>  
<span data-ttu-id="92e6a-106">Fyrir hverja fjárhagsfærslu sem er flutt í kostnaðarbókhald, fyllir [!INCLUDE[d365fin](includes/d365fin_md.md)] út kostnaðinn í reitnum **Færslunr.**</span><span class="sxs-lookup"><span data-stu-id="92e6a-106">For each general ledger entry that is transferred to cost accounting, [!INCLUDE[d365fin](includes/d365fin_md.md)] fills the cost **Entry No.** field.</span></span>  

## <a name="cost-entries"></a><span data-ttu-id="92e6a-107">Kostnaðarfærslur</span><span class="sxs-lookup"><span data-stu-id="92e6a-107">Cost Entries</span></span>  
<span data-ttu-id="92e6a-108">Fyrir sérhverja kostnaðarfærslu, vistar [!INCLUDE[d365fin](includes/d365fin_md.md)] færslunúmer samsvarandi fjárhagsfærslu í reitnum **Fjárhagsfærsla númer** í töflunni **Kostnaðarfærsla**.</span><span class="sxs-lookup"><span data-stu-id="92e6a-108">For each cost entry, [!INCLUDE[d365fin](includes/d365fin_md.md)] saves the entry number of the corresponding general ledger entry in the **G/L Entry No.** field in the **Cost Entry** table.</span></span>  

<span data-ttu-id="92e6a-109">Fyrir sameinaðar kostnaðarfærslur, vistar [!INCLUDE[d365fin](includes/d365fin_md.md)] færslunúmer síðustu fjárhagsfærslu, sem er færslan með hæsta færslunúmerið.</span><span class="sxs-lookup"><span data-stu-id="92e6a-109">For combined cost entries, [!INCLUDE[d365fin](includes/d365fin_md.md)] saves the entry number of the last general ledger entry, which is the entry with the highest entry number.</span></span>  

<span data-ttu-id="92e6a-110">Svæðið **Fjárhagsreikningur** í töflunni **Kostnaðarfærsla** hefur að geyma númer þess almenna fjárhagsreiknings sem kostnaðarfærslan kom frá.</span><span class="sxs-lookup"><span data-stu-id="92e6a-110">The **G/L Account** field in the **Cost Entry** table contains the number of the general ledger account that the cost entry came from.</span></span>  

<span data-ttu-id="92e6a-111">Fyrir stakar kostnaðarfærslur flytur [!INCLUDE[d365fin](includes/d365fin_md.md)] bókunartextann úr fjárhagsfærslunni í textareitinn **Lýsing**.</span><span class="sxs-lookup"><span data-stu-id="92e6a-111">For single cost entries, [!INCLUDE[d365fin](includes/d365fin_md.md)] transfers the posting text from the general ledger entry to the **Description** text field.</span></span> <span data-ttu-id="92e6a-112">Fyrir sameinaðar færslur, sýnir textareiturinn að þessar færslur eru fluttar sem sameinaðar færslur.</span><span class="sxs-lookup"><span data-stu-id="92e6a-112">For combined entries, the text field shows these entries are transferred as combined entries.</span></span> <span data-ttu-id="92e6a-113">Ef til dæmis um er að ræða sameinaða færslu vegna októbermánaðar 2012 gæti textinn verið **Sameinaðar færslur, október 2012**.</span><span class="sxs-lookup"><span data-stu-id="92e6a-113">For example, for a combined entry for the month of October in 2013, the text can be **Combined Entries, October 2013**.</span></span>  

## <a name="cost-register"></a><span data-ttu-id="92e6a-114">Kostnaðarskráning</span><span class="sxs-lookup"><span data-stu-id="92e6a-114">Cost Register</span></span>  
<span data-ttu-id="92e6a-115">Í töflunni **Kostnaðarskráning**, [!INCLUDE[d365fin](includes/d365fin_md.md)] stofnar færslu með upprunaflutningnum frá fjárhag.</span><span class="sxs-lookup"><span data-stu-id="92e6a-115">In the **Cost Register** table, [!INCLUDE[d365fin](includes/d365fin_md.md)] creates an entry with the source transfer from general ledger.</span></span> <span data-ttu-id="92e6a-116">Færslan skráir fyrstu og síðustu færslunúmer fjárhagsfærslna sem eru fluttar, til viðbótar við fyrstu og síðustu færslunúmer kostnaðarfærslnanna sem eru stofnaðar.</span><span class="sxs-lookup"><span data-stu-id="92e6a-116">The entry records the first and last entry numbers of the general ledger entries that are transferred, in addition to the first and last entry numbers of the cost entries that are created.</span></span>  

## <a name="see-also"></a><span data-ttu-id="92e6a-117">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="92e6a-117">See Also</span></span>  
<span data-ttu-id="92e6a-118">[Flytja fjárhagsfærslur í kostnaðarfærslur](finance-how-to-transfer-general-ledger-entries-to-cost-entries.md) </span><span class="sxs-lookup"><span data-stu-id="92e6a-118">[Transfer General Ledger Entries to Cost Entries](finance-how-to-transfer-general-ledger-entries-to-cost-entries.md) </span></span>  
<span data-ttu-id="92e6a-119">[Skilyrði til að millifærslu fjárhagsfærslna í kostnaðarfærslur](finance-criteria-for-transferring-general-ledger-entries-to-cost-entries.md) </span><span class="sxs-lookup"><span data-stu-id="92e6a-119">[Criteria for Transferring General Ledger Entries to Cost Entries](finance-criteria-for-transferring-general-ledger-entries-to-cost-entries.md) </span></span>  
<span data-ttu-id="92e6a-120">[Sjálfvirkur flutningur og færslur sameinaðar](finance-automatic-transfer-combined-entries.md) </span><span class="sxs-lookup"><span data-stu-id="92e6a-120">[Automatic Transfer and Combined Entries](finance-automatic-transfer-combined-entries.md) </span></span>  
[<span data-ttu-id="92e6a-121">Flytja og bóka kostnaðarfærslur</span><span class="sxs-lookup"><span data-stu-id="92e6a-121">Transferring and Posting Cost Entries</span></span>](finance-transfer-and-post-cost-entries.md)  

