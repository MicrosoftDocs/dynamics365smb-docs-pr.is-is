---
title: Hönnunarupplýsingar - Færslur víddarsamstæða | Microsoft Docs
description: Þessi fylgiskjöl veita nákvæmar tæknilegar upplýsingar yfir hugtökin og reglurnar sem eru notaðar til að endurhanna víddarfærsluvistun og bókunareiginleika.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, dimensions, codeunit
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: c6b66ecee87e1fd128733f541d46b97f44af0453
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2019
ms.locfileid: "935660"
---
# <a name="design-details-dimension-set-entries"></a><span data-ttu-id="d4c75-103">Hönnunarupplýsingarn: Færslur víddarsamstæða</span><span class="sxs-lookup"><span data-stu-id="d4c75-103">Design Details: Dimension Set Entries</span></span>
<span data-ttu-id="d4c75-104">Þessi fylgiskjöl veita nákvæmar tæknilegar upplýsingar yfir hugtök og reglur víddarfærsluvistun og bókunareiginleika í [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="d4c75-104">This documentation provides detailed technical insight into the concepts and principles of the dimension-entry storing and posting functionality in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="d4c75-105">Skjölin byrja á því að lýsa hugmyndafræðilegum yfirlitum.</span><span class="sxs-lookup"><span data-stu-id="d4c75-105">The documentation starts by describing conceptual overviews.</span></span> <span data-ttu-id="d4c75-106">Þá er tæknistrúktúr útskýrður.</span><span class="sxs-lookup"><span data-stu-id="d4c75-106">Then it explains the technical architecture.</span></span> <span data-ttu-id="d4c75-107">Einnig gefur það dæmi um kóða til undirbúnings fyrir víddarkóðaflutning og -uppfærslu úr útgáfum sem eru eldri en Dynamics NAV 2013R2.</span><span class="sxs-lookup"><span data-stu-id="d4c75-107">Finally, it provides code examples to prepare you for dimension code migration and upgrade from versions earlier than Dynamics NAV 2013R2.</span></span>  

## <a name="in-this-section"></a><span data-ttu-id="d4c75-108">Í þessum hluta</span><span class="sxs-lookup"><span data-stu-id="d4c75-108">In This Section</span></span>  
[<span data-ttu-id="d4c75-109">Yfirlit yfir víddasamstæðufærslur</span><span class="sxs-lookup"><span data-stu-id="d4c75-109">Dimension Set Entries Overview</span></span>](design-details-dimension-set-entries-overview.md)  
[<span data-ttu-id="d4c75-110">Hönnunarupplýsingar Leitað að víddarsamsetningum</span><span class="sxs-lookup"><span data-stu-id="d4c75-110">Design Details: Searching for Dimension Combinations</span></span>](design-details-searching-for-dimension-combinations.md)  
[<span data-ttu-id="d4c75-111">Hönnunarupplýsingar töfluuppbygging</span><span class="sxs-lookup"><span data-stu-id="d4c75-111">Design Details: Table Structure</span></span>](design-details-table-structure.md)  
[<span data-ttu-id="d4c75-112">Hönnunarupplýsingar: Kóðaeining 408 víddarstjórnun</span><span class="sxs-lookup"><span data-stu-id="d4c75-112">Design Details: Codeunit 408 Dimension Management</span></span>](design-details-codeunit-408-dimension-management.md)  
[<span data-ttu-id="d4c75-113">Hönnunarupplýsingar: Kóðadæmi um breytt mynstur í Breytingar</span><span class="sxs-lookup"><span data-stu-id="d4c75-113">Design Details: Code Examples of Changed Patterns in Modifications</span></span>](design-details-code-examples-of-changed-patterns-in-modifications.md)
