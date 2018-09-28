---
title: "Hönnunarupplýsingar - Færslur víddarsamstæða | Microsoft Docs"
description: "Þessi fylgiskjöl veita nákvæmar tæknilegar upplýsingar yfir hugtökin og reglurnar sem eru notaðar til að endurhanna víddarfærsluvistun og bókunareiginleika."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, dimensions, codeunit
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 5563241784aaf8bfa1a29f8568411be657647cf7
ms.contentlocale: is-is
ms.lasthandoff: 09/28/2018

---
# <a name="design-details-dimension-set-entries"></a><span data-ttu-id="91b59-103">Hönnunarupplýsingarn: Færslur víddarsamstæða</span><span class="sxs-lookup"><span data-stu-id="91b59-103">Design Details: Dimension Set Entries</span></span>
<span data-ttu-id="91b59-104">Þessi fylgiskjöl veita nákvæmar tæknilegar upplýsingar fyrir hugtökin og reglurnar sem eru notaðar til að endurhanna víddarfærslu fyrir vistun og bókun í [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="91b59-104">This documentation provides detailed technical insight into the concepts and principles that are used to redesign the dimension entry storing and posting feature in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="91b59-105">Skjölin byrjar með því að lýsa huglæg yfirlit yfir endurhönnun.</span><span class="sxs-lookup"><span data-stu-id="91b59-105">The documentation starts by describing conceptual overviews of the redesign.</span></span> <span data-ttu-id="91b59-106">Þá er tæknistrúktúr útskýrður til að sýna hvernig endurhönnun er gerð.</span><span class="sxs-lookup"><span data-stu-id="91b59-106">Then it explains the technical architecture to show how the redesign is made.</span></span> <span data-ttu-id="91b59-107">Einnig gefur það dæmi um kóða til undirbúnings fyrir víddarkóðaflutning og -uppfærslu.</span><span class="sxs-lookup"><span data-stu-id="91b59-107">Finally, it provides code examples to prepare you for dimension code migration and upgrade.</span></span>  

## <a name="in-this-section"></a><span data-ttu-id="91b59-108">Í þessum hluta</span><span class="sxs-lookup"><span data-stu-id="91b59-108">In This Section</span></span>  
[<span data-ttu-id="91b59-109">Yfirlit yfir víddasamstæðufærslur</span><span class="sxs-lookup"><span data-stu-id="91b59-109">Dimension Set Entries Overview</span></span>](design-details-dimension-set-entries-overview.md)  
[<span data-ttu-id="91b59-110">Hönnunarupplýsingar Leitað að víddarsamsetningum</span><span class="sxs-lookup"><span data-stu-id="91b59-110">Design Details: Searching for Dimension Combinations</span></span>](design-details-searching-for-dimension-combinations.md)  
[<span data-ttu-id="91b59-111">Hönnunarupplýsingar töfluuppbygging</span><span class="sxs-lookup"><span data-stu-id="91b59-111">Design Details: Table Structure</span></span>](design-details-table-structure.md)  
[<span data-ttu-id="91b59-112">Hönnunarupplýsingar: Kóðaeining 408 víddarstjórnun</span><span class="sxs-lookup"><span data-stu-id="91b59-112">Design Details: Codeunit 408 Dimension Management</span></span>](design-details-codeunit-408-dimension-management.md)  
[<span data-ttu-id="91b59-113">Hönnunarupplýsingar: Kóðadæmi um breytt mynstur í Breytingar</span><span class="sxs-lookup"><span data-stu-id="91b59-113">Design Details: Code Examples of Changed Patterns in Modifications</span></span>](design-details-code-examples-of-changed-patterns-in-modifications.md)

