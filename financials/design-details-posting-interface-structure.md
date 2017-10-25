---
title: "Hönnunarupplýsingar - Uppbygging bókunarviðmóts | Microsoft Docs"
description: "Í þessu efnisatriði er að finna yfirlit yfir altæk ferli í uppbyggingu bókunarviðmóts."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: posting, interface, design
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 97b1bc02f848d583240a1701e41be4b639422a6c
ms.contentlocale: is-is
ms.lasthandoff: 09/22/2017

---
# <a name="design-details-posting-interface-structure"></a><span data-ttu-id="1676a-103">Hönnunarupplýsingar: Uppbygging bókunarviðmóts</span><span class="sxs-lookup"><span data-stu-id="1676a-103">Design Details: Posting Interface Structure</span></span>
<span data-ttu-id="1676a-104">Í [!INCLUDE[d365fin](includes/d365fin_md.md)] uppbyggingu bókunarviðmóts eru nokkur alþjóðleg ferli sem nota sömu uppbyggingu:</span><span class="sxs-lookup"><span data-stu-id="1676a-104">In the [!INCLUDE[d365fin](includes/d365fin_md.md)] posting interface structure, there are several global procedures that use the same structure:</span></span>  
  
* <span data-ttu-id="1676a-105">RunWithCheck RunWithoutCheck vinnslukóðar – almennt bókunarviðmót fyrir almenna færslubókarlínu.</span><span class="sxs-lookup"><span data-stu-id="1676a-105">RunWithCheck and RunWithoutCheck call procedure Code – generic posting interface for Gen. Jnl Line.</span></span>  
* <span data-ttu-id="1676a-106">CustPostApplyCustLedgEntry – bóka jafnanir viðskiptamanna, úr kóðaeiningu 226 CustEntry-Jafna bókaðar færslur.</span><span class="sxs-lookup"><span data-stu-id="1676a-106">CustPostApplyCustLedgEntry – post customer application, called from codeunit 226 CustEntry-Apply Posted Entries.</span></span>  
* <span data-ttu-id="1676a-107">VendPostApplyVendLedgEntry – bóka jafnanir lánardrottins, sóttar úr kóðaeiningu 227 VendEntry-Jafna bókaðar færslur.</span><span class="sxs-lookup"><span data-stu-id="1676a-107">VendPostApplyVendLedgEntry – post vendor application, called from codeunit 227 VendEntry-Apply Posted Entries.</span></span>  
* <span data-ttu-id="1676a-108">UnapplyCustLedgEntry – pósta ógildingu jöfnunar viðskiptamanns, sótt úr kóðaeiningu 226 CustEntry-Jafna bókaðar færslur</span><span class="sxs-lookup"><span data-stu-id="1676a-108">UnapplyCustLedgEntry – post unapply of customer application, called from codeunit 226 CustEntry-Apply Posted Entries</span></span>  
* <span data-ttu-id="1676a-109">UnapplyVendLedgEntry – pósta ógildingu jöfnunar viðskiptamanns, sótt úr kóðaeiningu 227 VendEntry-Jafna bókaðar færslur</span><span class="sxs-lookup"><span data-stu-id="1676a-109">UnapplyVendLedgEntry – post unapply of vendor application, called from codeunit 227 VendEntry-Apply Posted Entries</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1676a-110">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="1676a-110">See Also</span></span>  
[<span data-ttu-id="1676a-111">Hönnunarupplýsingar: Uppbygging bókunarvélar</span><span class="sxs-lookup"><span data-stu-id="1676a-111">Design Details: Posting Engine Structure</span></span>](design-details-posting-engine-structure.md)
