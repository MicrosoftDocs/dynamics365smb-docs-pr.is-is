---
title: "Hönnunarupplýsingar - Birgðakostnaður | Microsoft Docs"
description: "Þessi fylgiskjöl veita nákvæmar tæknilegar upplýsingar fyrir hugtökin og reglurnar sem eru notaðar í Birgðarkostnaði í Finance and Operations, Business Edition."
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, inventory, costing
ms.date: 11/23/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: b34f276a764f0e828fbc1f015429df9852242a4c
ms.openlocfilehash: 2ee8988a89e4bd01683a6945e66e08ab9608af2e
ms.contentlocale: is-is
ms.lasthandoff: 03/22/2018

---
# <a name="design-details-inventory-costing"></a><span data-ttu-id="23941-103">Hönnunarupplýsingar: Birgðakostnaður</span><span class="sxs-lookup"><span data-stu-id="23941-103">Design Details: Inventory Costing</span></span>
<span data-ttu-id="23941-104">Þessi fylgiskjöl veita nákvæmar tæknilegar upplýsingar fyrir hugtökin og reglurnar sem eru notaðar í Birgðarkostnaði [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="23941-104">This documentation provides detailed technical insight to the concepts and principles that are used within the Inventory Costing features in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  

<span data-ttu-id="23941-105">Birgðakostnaður, einnig kostnaðarstýring, snýst um að skrá og tilkynna kostnað við starfsemi fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="23941-105">Inventory costing, also referred to as cost management, is concerned with recording and reporting business operating costs.</span></span>  

## <a name="in-this-section"></a><span data-ttu-id="23941-106">Í þessum hluta</span><span class="sxs-lookup"><span data-stu-id="23941-106">In This Section</span></span>  
[<span data-ttu-id="23941-107">Hönnunarupplýsingar: Aðferð kostnaðarútreiknings</span><span class="sxs-lookup"><span data-stu-id="23941-107">Design Details: Costing Methods</span></span>](design-details-costing-methods.md)  
[<span data-ttu-id="23941-108">Hönnunarupplýsingar: Umsókn vöru</span><span class="sxs-lookup"><span data-stu-id="23941-108">Design Details: Item Application</span></span>](design-details-item-application.md)  
[<span data-ttu-id="23941-109">Hönnunarupplýsingar: Þekkt vandamál birgðajöfnunar</span><span class="sxs-lookup"><span data-stu-id="23941-109">Design Details: Known Item Application Issue</span></span>](design-details-inventory-zero-level-open-item-ledger-entries.md)  
[<span data-ttu-id="23941-110">Hönnunarupplýsingar: kostnaðarleiðrétting</span><span class="sxs-lookup"><span data-stu-id="23941-110">Design Details: Cost Adjustment</span></span>](design-details-cost-adjustment.md)  
[<span data-ttu-id="23941-111">Hönnunarupplýsingar: Bókunardagsetning á leiðréttingarvirðisfærslum</span><span class="sxs-lookup"><span data-stu-id="23941-111">Design Details: Posting Date on Adjustment Value Entry</span></span>](design-details-inventory-adjustment-value-entry-posting-date.md)  
[<span data-ttu-id="23941-112">Hönnunarupplýsingar: Væntanleg kostnaðarfærsla</span><span class="sxs-lookup"><span data-stu-id="23941-112">Design Details: Expected Cost Posting</span></span>](design-details-expected-cost-posting.md)  
[<span data-ttu-id="23941-113">Hönnunarupplýsingar: Meðalkostnaður</span><span class="sxs-lookup"><span data-stu-id="23941-113">Design Details: Average Cost</span></span>](design-details-average-cost.md)  
[<span data-ttu-id="23941-114">Hönnunarupplýsingar Frávik</span><span class="sxs-lookup"><span data-stu-id="23941-114">Design Details: Variance</span></span>](design-details-variance.md)  
[<span data-ttu-id="23941-115">Hönnunarupplýsingar: sléttun</span><span class="sxs-lookup"><span data-stu-id="23941-115">Design Details: Rounding</span></span>](design-details-rounding.md)  
[<span data-ttu-id="23941-116">Hönnunarupplýsingar: kostnaðaríhlutir</span><span class="sxs-lookup"><span data-stu-id="23941-116">Design Details: Cost Components</span></span>](design-details-cost-components.md)  
[<span data-ttu-id="23941-117">Hönnunarupplýsingar: birgðahaldstími</span><span class="sxs-lookup"><span data-stu-id="23941-117">Design Details: Inventory Periods</span></span>](design-details-inventory-periods.md)  
[<span data-ttu-id="23941-118">Hönnunarupplýsingar: birgðabókun</span><span class="sxs-lookup"><span data-stu-id="23941-118">Design Details: Inventory Posting</span></span>](design-details-inventory-posting.md)  
[<span data-ttu-id="23941-119">Hönnunarupplýsingar: staða framleiðslupöntunar</span><span class="sxs-lookup"><span data-stu-id="23941-119">Design Details: Production Order Posting</span></span>](design-details-production-order-posting.md)  
[<span data-ttu-id="23941-120">Hönnunarupplýsingar: Bókun samsetningarpöntunar</span><span class="sxs-lookup"><span data-stu-id="23941-120">Design Details: Assembly Order Posting</span></span>](design-details-assembly-order-posting.md)  
[<span data-ttu-id="23941-121">Hönnunarupplýsingar: afstemming í fjárhagur</span><span class="sxs-lookup"><span data-stu-id="23941-121">Design Details: Reconciliation with the General Ledger</span></span>](design-details-reconciliation-with-the-general-ledger.md)  
[<span data-ttu-id="23941-122">Hönnunarupplýsingar: reikningar í fjárhagur</span><span class="sxs-lookup"><span data-stu-id="23941-122">Design Details: Accounts in the General Ledger</span></span>](design-details-accounts-in-the-general-ledger.md)  
[<span data-ttu-id="23941-123">Hönnunarupplýsingar: Endurmat</span><span class="sxs-lookup"><span data-stu-id="23941-123">Design Details: Revaluation</span></span>](design-details-revaluation.md)

