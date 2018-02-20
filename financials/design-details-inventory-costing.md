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
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 4f14118e435051c6d63f95a05ebee2e7107ce054
ms.contentlocale: is-is
ms.lasthandoff: 01/30/2018

---
# <a name="design-details-inventory-costing"></a><span data-ttu-id="f2abf-103">Hönnunarupplýsingar: Birgðakostnaður</span><span class="sxs-lookup"><span data-stu-id="f2abf-103">Design Details: Inventory Costing</span></span>
<span data-ttu-id="f2abf-104">Þessi fylgiskjöl veita nákvæmar tæknilegar upplýsingar fyrir hugtökin og reglurnar sem eru notaðar í Birgðarkostnaði [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="f2abf-104">This documentation provides detailed technical insight to the concepts and principles that are used within the Inventory Costing features in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  

<span data-ttu-id="f2abf-105">Birgðakostnaður, einnig kostnaðarstýring, snýst um að skrá og tilkynna kostnað við starfsemi fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="f2abf-105">Inventory costing, also referred to as cost management, is concerned with recording and reporting business operating costs.</span></span>  

## <a name="in-this-section"></a><span data-ttu-id="f2abf-106">Í þessum hluta</span><span class="sxs-lookup"><span data-stu-id="f2abf-106">In This Section</span></span>  
[<span data-ttu-id="f2abf-107">Hönnunarupplýsingar: Aðferð kostnaðarútreiknings</span><span class="sxs-lookup"><span data-stu-id="f2abf-107">Design Details: Costing Methods</span></span>](design-details-costing-methods.md)  
[<span data-ttu-id="f2abf-108">Hönnunarupplýsingar: Umsókn vöru</span><span class="sxs-lookup"><span data-stu-id="f2abf-108">Design Details: Item Application</span></span>](design-details-item-application.md)  
[<span data-ttu-id="f2abf-109">Hönnunarupplýsingar: kostnaðarleiðrétting</span><span class="sxs-lookup"><span data-stu-id="f2abf-109">Design Details: Cost Adjustment</span></span>](design-details-cost-adjustment.md)  
[<span data-ttu-id="f2abf-110">Hönnunarupplýsingar: Væntanleg kostnaðarfærsla</span><span class="sxs-lookup"><span data-stu-id="f2abf-110">Design Details: Expected Cost Posting</span></span>](design-details-expected-cost-posting.md)  
[<span data-ttu-id="f2abf-111">Hönnunarupplýsingar: Meðalkostnaður</span><span class="sxs-lookup"><span data-stu-id="f2abf-111">Design Details: Average Cost</span></span>](design-details-average-cost.md)  
[<span data-ttu-id="f2abf-112">Hönnunarupplýsingar Frávik</span><span class="sxs-lookup"><span data-stu-id="f2abf-112">Design Details: Variance</span></span>](design-details-variance.md)  
[<span data-ttu-id="f2abf-113">Hönnunarupplýsingar: sléttun</span><span class="sxs-lookup"><span data-stu-id="f2abf-113">Design Details: Rounding</span></span>](design-details-rounding.md)  
[<span data-ttu-id="f2abf-114">Hönnunarupplýsingar: kostnaðaríhlutir</span><span class="sxs-lookup"><span data-stu-id="f2abf-114">Design Details: Cost Components</span></span>](design-details-cost-components.md)  
[<span data-ttu-id="f2abf-115">Hönnunarupplýsingar: birgðahaldstími</span><span class="sxs-lookup"><span data-stu-id="f2abf-115">Design Details: Inventory Periods</span></span>](design-details-inventory-periods.md)  
[<span data-ttu-id="f2abf-116">Hönnunarupplýsingar: birgðabókun</span><span class="sxs-lookup"><span data-stu-id="f2abf-116">Design Details: Inventory Posting</span></span>](design-details-inventory-posting.md)  
[<span data-ttu-id="f2abf-117">Hönnunarupplýsingar: staða framleiðslupöntunar</span><span class="sxs-lookup"><span data-stu-id="f2abf-117">Design Details: Production Order Posting</span></span>](design-details-production-order-posting.md)  
[<span data-ttu-id="f2abf-118">Hönnunarupplýsingar: Bókun samsetningarpöntunar</span><span class="sxs-lookup"><span data-stu-id="f2abf-118">Design Details: Assembly Order Posting</span></span>](design-details-assembly-order-posting.md)  
[<span data-ttu-id="f2abf-119">Hönnunarupplýsingar: afstemming í fjárhagur</span><span class="sxs-lookup"><span data-stu-id="f2abf-119">Design Details: Reconciliation with the General Ledger</span></span>](design-details-reconciliation-with-the-general-ledger.md)  
[<span data-ttu-id="f2abf-120">Hönnunarupplýsingar: reikningar í fjárhagur</span><span class="sxs-lookup"><span data-stu-id="f2abf-120">Design Details: Accounts in the General Ledger</span></span>](design-details-accounts-in-the-general-ledger.md)  
[<span data-ttu-id="f2abf-121">Hönnunarupplýsingar: Endurmat</span><span class="sxs-lookup"><span data-stu-id="f2abf-121">Design Details: Revaluation</span></span>](design-details-revaluation.md)

