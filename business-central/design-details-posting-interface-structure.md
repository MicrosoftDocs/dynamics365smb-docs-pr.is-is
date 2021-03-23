---
title: Hönnunarupplýsingar - Uppbygging bókunarviðmóts | Microsoft Docs
description: Í þessu efnisatriði er að finna yfirlit yfir altæk ferli í uppbyggingu bókunarviðmóts.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: posting, interface, design
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 4815e2d4b69095ff61e92d750963879f93dda875
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5390775"
---
# <a name="design-details-posting-interface-structure"></a><span data-ttu-id="a6b33-103">Hönnunarupplýsingar: Uppbygging bókunarviðmóts</span><span class="sxs-lookup"><span data-stu-id="a6b33-103">Design Details: Posting Interface Structure</span></span>
<span data-ttu-id="a6b33-104">Í [!INCLUDE[prod_short](includes/prod_short.md)] uppbyggingu bókunarviðmóts eru nokkur alþjóðleg ferli sem nota sömu uppbyggingu:</span><span class="sxs-lookup"><span data-stu-id="a6b33-104">In the [!INCLUDE[prod_short](includes/prod_short.md)] posting interface structure, there are several global procedures that use the same structure:</span></span>  
  
* <span data-ttu-id="a6b33-105">RunWithCheck RunWithoutCheck vinnslukóðar – almennt bókunarviðmót fyrir almenna</span><span class="sxs-lookup"><span data-stu-id="a6b33-105">RunWithCheck and RunWithoutCheck call procedure Code – generic posting interface for Gen.</span></span> <span data-ttu-id="a6b33-106">færslubókarlínu.</span><span class="sxs-lookup"><span data-stu-id="a6b33-106">Jnl Line.</span></span>  
* <span data-ttu-id="a6b33-107">CustPostApplyCustLedgEntry – bóka jafnanir viðskiptamanna, úr kóðaeiningu 226 CustEntry-Jafna bókaðar færslur.</span><span class="sxs-lookup"><span data-stu-id="a6b33-107">CustPostApplyCustLedgEntry – post customer application, called from codeunit 226 CustEntry-Apply Posted Entries.</span></span>  
* <span data-ttu-id="a6b33-108">VendPostApplyVendLedgEntry – bóka jafnanir lánardrottins, sóttar úr kóðaeiningu 227 VendEntry-Jafna bókaðar færslur.</span><span class="sxs-lookup"><span data-stu-id="a6b33-108">VendPostApplyVendLedgEntry – post vendor application, called from codeunit 227 VendEntry-Apply Posted Entries.</span></span>  
* <span data-ttu-id="a6b33-109">UnapplyCustLedgEntry – pósta ógildingu jöfnunar viðskiptamanns, sótt úr kóðaeiningu 226 CustEntry-Jafna bókaðar færslur</span><span class="sxs-lookup"><span data-stu-id="a6b33-109">UnapplyCustLedgEntry – post unapply of customer application, called from codeunit 226 CustEntry-Apply Posted Entries</span></span>  
* <span data-ttu-id="a6b33-110">UnapplyVendLedgEntry – pósta ógildingu jöfnunar viðskiptamanns, sótt úr kóðaeiningu 227 VendEntry-Jafna bókaðar færslur</span><span class="sxs-lookup"><span data-stu-id="a6b33-110">UnapplyVendLedgEntry – post unapply of vendor application, called from codeunit 227 VendEntry-Apply Posted Entries</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a6b33-111">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="a6b33-111">See Also</span></span>  
[<span data-ttu-id="a6b33-112">Hönnunarupplýsingar: Uppbygging bókunarvélar</span><span class="sxs-lookup"><span data-stu-id="a6b33-112">Design Details: Posting Engine Structure</span></span>](design-details-posting-engine-structure.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]