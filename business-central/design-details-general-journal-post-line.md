---
title: Hönnunarupplýsingar - Bókunarlína færslubókar | Microsoft Docs
description: Þetta efnisatriði veitir upplýsingar um hugtökin og reglurnar sem eru notaðar til að endurhanna bókarlínur færslubókarinnar í Business Central.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, general journal, posting, codeunit 12
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: e7e61b572b2a7a1538d58430cbbcbb19d7cda999
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5390075"
---
# <a name="design-details-general-journal-post-line"></a><span data-ttu-id="9ae7c-103">Hönnunarupplýsingar: Bókunarlína færslubókar</span><span class="sxs-lookup"><span data-stu-id="9ae7c-103">Design Details: General Journal Post Line</span></span>
<span data-ttu-id="9ae7c-104">Þessi fylgiskjöl veita nákvæmar tæknilegar upplýsingar fyrir hugtökin og reglurnar sem eru notaðar til að endurhanna bókarlínur færslubókarinnar í [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="9ae7c-104">This documentation provides detailed technical insight into the concepts and principles that are used to redesign the general journal posting line feature in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="9ae7c-105">Endurhönnunin gerir kóðaeiningu 12 einfaldari og auðveldari að viðhalda.</span><span class="sxs-lookup"><span data-stu-id="9ae7c-105">The redesign makes codeunit 12 simpler and more maintainable.</span></span> <span data-ttu-id="9ae7c-106">Skjölin byrjar með því að lýsa huglæg yfirlit yfir endurhönnun.</span><span class="sxs-lookup"><span data-stu-id="9ae7c-106">The documentation starts by describing conceptual overviews of the redesign.</span></span> <span data-ttu-id="9ae7c-107">Þá er tæknistrúktúr útskýrður til að sýna breytingar eftir endurhönnun.</span><span class="sxs-lookup"><span data-stu-id="9ae7c-107">Then it explains the technical architecture to show the changes that result from the redesign.</span></span>  

## <a name="in-this-section"></a><span data-ttu-id="9ae7c-108">Í þessum hluta</span><span class="sxs-lookup"><span data-stu-id="9ae7c-108">In This Section</span></span>  
[<span data-ttu-id="9ae7c-109">Yfirlit bókunarlínu færslubókar</span><span class="sxs-lookup"><span data-stu-id="9ae7c-109">General Journal Post Line Overview</span></span>](design-details-general-journal-post-line-overview.md)  
[<span data-ttu-id="9ae7c-110">Hönnunarupplýsingar: Uppbygging bókunarviðmóts</span><span class="sxs-lookup"><span data-stu-id="9ae7c-110">Design Details: Posting Interface Structure</span></span>](design-details-posting-interface-structure.md)  
[<span data-ttu-id="9ae7c-111">Hönnunarupplýsingar: Uppbygging bókunarvélar</span><span class="sxs-lookup"><span data-stu-id="9ae7c-111">Design Details: Posting Engine Structure</span></span>](design-details-posting-engine-structure.md)  
[<span data-ttu-id="9ae7c-112">Kóðaeining 12 Breytingar: Vörpun altækra breyta fyrir bókunarlínu færslubókar</span><span class="sxs-lookup"><span data-stu-id="9ae7c-112">Codeunit 12 Changes: Mapping Global Variables for General Journal Post Line</span></span>](design-details-codeunit-12-changes-mapping-global-variables-for-general-journal-post-line.md)  
[<span data-ttu-id="9ae7c-113">Kóðaeining 12 Breytingar: Breytingar á bókunaraðferðum í færslubók</span><span class="sxs-lookup"><span data-stu-id="9ae7c-113">Codeunit 12 Changes: Changes in General Journal Post Procedures</span></span>](design-details-codeunit-12-changes-changes-in-general-journal-post-procedures.md)  

## <a name="see-also"></a><span data-ttu-id="9ae7c-114">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="9ae7c-114">See Also</span></span>  
[<span data-ttu-id="9ae7c-115">Vinna í færslubókum</span><span class="sxs-lookup"><span data-stu-id="9ae7c-115">Working with General Journals</span></span>](ui-work-general-journals.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]