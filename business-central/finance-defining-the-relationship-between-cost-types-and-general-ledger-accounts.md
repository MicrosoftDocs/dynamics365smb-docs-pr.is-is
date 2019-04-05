---
title: Skilgreining á venslum milli kostnaðargerða og fjárhagsreikninga | Microsoft Docs
description: Lærðu hvernig á að skilgreina tengsl milli kostnaðartegundarinnar og fjárhagsreikningsins.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: cost types, general ledger
ms.date: 11/13/2018
ms.author: sgroespe
redirect_url: finance-transfer-and-post-cost-entries
ms.openlocfilehash: f80e9b6276d26adffb5e3208ffefbf98d7f7ff96
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/08/2019
ms.locfileid: "799695"
---
# <a name="defining-the-relationship-between-cost-types-and-general-ledger-accounts"></a><span data-ttu-id="59d98-103">Skilgreining á venslum milli kostnaðargerða og fjárhagsreikninga</span><span class="sxs-lookup"><span data-stu-id="59d98-103">Defining the Relationship Between Cost Types and General Ledger Accounts</span></span>
<span data-ttu-id="59d98-104">Tengsl milli kostnaðartegundarinnar og almenna fjárhagslykilsins eru stofnuð í kostnaðartegundinni og í fjárhagsreikningnum.</span><span class="sxs-lookup"><span data-stu-id="59d98-104">The relationship between the cost type and the general ledger account is created in the cost type and in the general ledger account.</span></span>  

* <span data-ttu-id="59d98-105">Reiturinn **Fjárhagsreikningssvið** í töflunni **Kostnaðargerð** mælir fyrir um hvaða fjárhagsreikningur tilheyrir tegund kostnaðar.</span><span class="sxs-lookup"><span data-stu-id="59d98-105">The **G/L Account Range** field in the **Cost Type** table establishes which general ledger accounts belong to a cost type.</span></span>  
* <span data-ttu-id="59d98-106">Reiturinn **Númer kostnaðartegundar**</span><span class="sxs-lookup"><span data-stu-id="59d98-106">The **Cost Type No.**</span></span> <span data-ttu-id="59d98-107">í reikningatöflu mælir fyrir um hvaða tegund kostnaðar fjárhagsreikningur tilheyrir.</span><span class="sxs-lookup"><span data-stu-id="59d98-107">field in the chart of accounts establishes which cost type a general ledger account belongs to.</span></span>  

<span data-ttu-id="59d98-108">Þessir tveir reitir eru fylltir út sjálfkrafa þegar aðgerðin **Sækja kostnaðargerðir úr bókhaldslykli** er notuð.</span><span class="sxs-lookup"><span data-stu-id="59d98-108">These two fields are filled automatically when you use the **Get Cost Types from Chart of Accounts** function.</span></span>  

## <a name="relationship-between-general-ledger-accounts-and-cost-types"></a><span data-ttu-id="59d98-109">Tengsl milli fjárhagsreiknings og kostnaðartegunda</span><span class="sxs-lookup"><span data-stu-id="59d98-109">Relationship Between General Ledger Accounts and Cost Types</span></span>  
<span data-ttu-id="59d98-110">Til eru n:1 vensl milli fjárhagsreikninga og kostnaðargerðar.</span><span class="sxs-lookup"><span data-stu-id="59d98-110">There is an n:1 relationship between general ledger accounts and cost types.</span></span> <span data-ttu-id="59d98-111">Nokkrir fjárhagsreikningar geta tilheyrt einni kostnaðartegund, en hver fjárhagsreikningur tilheyrir aðeins einni kostnaðargerð.</span><span class="sxs-lookup"><span data-stu-id="59d98-111">Several general ledger accounts can belong to one cost type, but each general ledger account belongs to only one cost type.</span></span> <span data-ttu-id="59d98-112">Eftirfarandi tafla lýsir upplýsingunum í tengslunum.</span><span class="sxs-lookup"><span data-stu-id="59d98-112">The following table describes the details in the relationship.</span></span>  

|<span data-ttu-id="59d98-113">Tengsl</span><span class="sxs-lookup"><span data-stu-id="59d98-113">Relationship</span></span>|<span data-ttu-id="59d98-114">**Reikningsbil fjárhags**</span><span class="sxs-lookup"><span data-stu-id="59d98-114">**G/L Account Range**</span></span>|<span data-ttu-id="59d98-115">**Kostnaðartegundarnr.**</span><span class="sxs-lookup"><span data-stu-id="59d98-115">**Cost Type No.**</span></span>|  
|------------------|------------------------------------------------|-------------------------------------------|  
|<span data-ttu-id="59d98-116">Einn fjárhagsreikningur fyrir hverja kostnaðartegund</span><span class="sxs-lookup"><span data-stu-id="59d98-116">One general ledger account for each cost type</span></span>|<span data-ttu-id="59d98-117">Einn fjárhagsreikningur</span><span class="sxs-lookup"><span data-stu-id="59d98-117">One general ledger account</span></span>|<span data-ttu-id="59d98-118">Ein kostnaðartegund</span><span class="sxs-lookup"><span data-stu-id="59d98-118">One cost type</span></span>|  
|<span data-ttu-id="59d98-119">Nokkrir fjárhagsreikningar fyrir hverja kostnaðartegund</span><span class="sxs-lookup"><span data-stu-id="59d98-119">Several general ledger accounts for one cost type</span></span>|<span data-ttu-id="59d98-120">Svið fjárhagsreikninga, til dæmis 7110..7193 fyrir hvern fjárhagsreikning</span><span class="sxs-lookup"><span data-stu-id="59d98-120">General ledger account range, for example, 7110..7193 for each general ledger account</span></span>|<span data-ttu-id="59d98-121">Fyrir hvern fjárhagsreikning í bilinu, er aðeins ein kostnaðartegund</span><span class="sxs-lookup"><span data-stu-id="59d98-121">For each general ledger account in the range, there is only one cost type</span></span>|  
|<span data-ttu-id="59d98-122">Kostnaðartegundir án samsvarandi tengsla við fjárhaglykla</span><span class="sxs-lookup"><span data-stu-id="59d98-122">Cost types without corresponding general ledger accounts</span></span>|<Empty>||  
|<span data-ttu-id="59d98-123">Fjárhagsreikningar með færslur sem ekki verið fluttar</span><span class="sxs-lookup"><span data-stu-id="59d98-123">General ledger accounts whose entries will not be transferred</span></span>||<Empty>|  

## <a name="cost-types-without-a-relationship-to-the-general-ledger"></a><span data-ttu-id="59d98-124">Kostnaðartegundir án tengsla við fjárhag</span><span class="sxs-lookup"><span data-stu-id="59d98-124">Cost Types Without a Relationship to the General Ledger</span></span>  
<span data-ttu-id="59d98-125">Kostnaðartegund má ekki hafa tengsl við fjárhagsreikninga ef annað af eftirfarandi skilyrðum á við:</span><span class="sxs-lookup"><span data-stu-id="59d98-125">A cost type may not have a relationship to general ledger accounts if one of the following conditions is true:</span></span>  

* <span data-ttu-id="59d98-126">Reikningar fyrir rekstarbókhald, eins og Reikn. vextir og Afskriftir, taka einungis kostnað frá rekstrarbókhaldi.</span><span class="sxs-lookup"><span data-stu-id="59d98-126">Accounts for operational accounting, such as Calc. Interest and Depreciation, only take costs from the operational accounting.</span></span>  
* <span data-ttu-id="59d98-127">Aukakostnaðartegundir, t.d. kostnaðargerðir 9901, 9902 og 9903 í [!INCLUDE[d365fin](includes/d365fin_md.md)]-gagnagrunninum, eru notaðir sem kredit- og debetreikningar fyrir úthlutanir.</span><span class="sxs-lookup"><span data-stu-id="59d98-127">Helping cost types, such as cost types 9901, 9902, and 9903 in the [!INCLUDE[d365fin](includes/d365fin_md.md)] database, are used as credit and debit accounts for allocations.</span></span>  
* <span data-ttu-id="59d98-128">Hjálparreikningurinn, 9920 í [!INCLUDE[d365fin](includes/d365fin_md.md)] gagnagrunninn, inniheldur raunverulegar uppsafnanir sem sýna muninn milli kostnaðar og gjalda úr fjárhag.</span><span class="sxs-lookup"><span data-stu-id="59d98-128">The helping account, 9920 in the [!INCLUDE[d365fin](includes/d365fin_md.md)] database, contains actual accruals that show the difference between costs and the expense from the general ledger.</span></span>  

## <a name="see-also"></a><span data-ttu-id="59d98-129">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="59d98-129">See Also</span></span>  
[<span data-ttu-id="59d98-130">Kostnaðarreikningur</span><span class="sxs-lookup"><span data-stu-id="59d98-130">Accounting for Costs</span></span>](finance-manage-cost-accounting.md)  
<span data-ttu-id="59d98-131">[Uppsetning kostnaðarbókhalds](finance-set-up-cost-accounting.md) </span><span class="sxs-lookup"><span data-stu-id="59d98-131">[Setting Up Cost Accounting](finance-set-up-cost-accounting.md) </span></span>  
[<span data-ttu-id="59d98-132">Um kostnaðarbókhald</span><span class="sxs-lookup"><span data-stu-id="59d98-132">About Cost Accounting</span></span>](finance-about-cost-accounting.md)  
<span data-ttu-id="59d98-133">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="59d98-133">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
