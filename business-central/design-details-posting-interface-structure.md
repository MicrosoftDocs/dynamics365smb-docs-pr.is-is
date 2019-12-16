---
title: Hönnunarupplýsingar - Uppbygging bókunarviðmóts | Microsoft Docs
description: Í þessu efnisatriði er að finna yfirlit yfir altæk ferli í uppbyggingu bókunarviðmóts.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: posting, interface, design
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 7600e8ebfee6b6eda6f872b0de2f4c8238338340
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/03/2019
ms.locfileid: "2880089"
---
# <a name="design-details-posting-interface-structure"></a><span data-ttu-id="b2a2c-103">Hönnunarupplýsingar: Uppbygging bókunarviðmóts</span><span class="sxs-lookup"><span data-stu-id="b2a2c-103">Design Details: Posting Interface Structure</span></span>
<span data-ttu-id="b2a2c-104">Í [!INCLUDE[d365fin](includes/d365fin_md.md)] uppbyggingu bókunarviðmóts eru nokkur alþjóðleg ferli sem nota sömu uppbyggingu:</span><span class="sxs-lookup"><span data-stu-id="b2a2c-104">In the [!INCLUDE[d365fin](includes/d365fin_md.md)] posting interface structure, there are several global procedures that use the same structure:</span></span>  
  
* <span data-ttu-id="b2a2c-105">RunWithCheck RunWithoutCheck vinnslukóðar – almennt bókunarviðmót fyrir almenna</span><span class="sxs-lookup"><span data-stu-id="b2a2c-105">RunWithCheck and RunWithoutCheck call procedure Code – generic posting interface for Gen.</span></span> <span data-ttu-id="b2a2c-106">færslubókarlínu.</span><span class="sxs-lookup"><span data-stu-id="b2a2c-106">Jnl Line.</span></span>  
* <span data-ttu-id="b2a2c-107">CustPostApplyCustLedgEntry – bóka jafnanir viðskiptamanna, úr kóðaeiningu 226 CustEntry-Jafna bókaðar færslur.</span><span class="sxs-lookup"><span data-stu-id="b2a2c-107">CustPostApplyCustLedgEntry – post customer application, called from codeunit 226 CustEntry-Apply Posted Entries.</span></span>  
* <span data-ttu-id="b2a2c-108">VendPostApplyVendLedgEntry – bóka jafnanir lánardrottins, sóttar úr kóðaeiningu 227 VendEntry-Jafna bókaðar færslur.</span><span class="sxs-lookup"><span data-stu-id="b2a2c-108">VendPostApplyVendLedgEntry – post vendor application, called from codeunit 227 VendEntry-Apply Posted Entries.</span></span>  
* <span data-ttu-id="b2a2c-109">UnapplyCustLedgEntry – pósta ógildingu jöfnunar viðskiptamanns, sótt úr kóðaeiningu 226 CustEntry-Jafna bókaðar færslur</span><span class="sxs-lookup"><span data-stu-id="b2a2c-109">UnapplyCustLedgEntry – post unapply of customer application, called from codeunit 226 CustEntry-Apply Posted Entries</span></span>  
* <span data-ttu-id="b2a2c-110">UnapplyVendLedgEntry – pósta ógildingu jöfnunar viðskiptamanns, sótt úr kóðaeiningu 227 VendEntry-Jafna bókaðar færslur</span><span class="sxs-lookup"><span data-stu-id="b2a2c-110">UnapplyVendLedgEntry – post unapply of vendor application, called from codeunit 227 VendEntry-Apply Posted Entries</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b2a2c-111">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="b2a2c-111">See Also</span></span>  
[<span data-ttu-id="b2a2c-112">Hönnunarupplýsingar: Uppbygging bókunarvélar</span><span class="sxs-lookup"><span data-stu-id="b2a2c-112">Design Details: Posting Engine Structure</span></span>](design-details-posting-engine-structure.md)