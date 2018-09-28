---
title: "Hönnunarupplýsingar - Uppbygging bókunarviðmóts | Microsoft Docs"
description: "Í þessu efnisatriði er að finna yfirlit yfir altæk ferli í uppbyggingu bókunarviðmóts."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: posting, interface, design
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 236cbcc45ccca23905dcb79a491236c80b2bdebf
ms.contentlocale: is-is
ms.lasthandoff: 09/28/2018

---
# <a name="design-details-posting-interface-structure"></a><span data-ttu-id="b2780-103">Hönnunarupplýsingar: Uppbygging bókunarviðmóts</span><span class="sxs-lookup"><span data-stu-id="b2780-103">Design Details: Posting Interface Structure</span></span>
<span data-ttu-id="b2780-104">Í [!INCLUDE[d365fin](includes/d365fin_md.md)] uppbyggingu bókunarviðmóts eru nokkur alþjóðleg ferli sem nota sömu uppbyggingu:</span><span class="sxs-lookup"><span data-stu-id="b2780-104">In the [!INCLUDE[d365fin](includes/d365fin_md.md)] posting interface structure, there are several global procedures that use the same structure:</span></span>  
  
* <span data-ttu-id="b2780-105">RunWithCheck RunWithoutCheck vinnslukóðar – almennt bókunarviðmót fyrir almenna færslubókarlínu.</span><span class="sxs-lookup"><span data-stu-id="b2780-105">RunWithCheck and RunWithoutCheck call procedure Code – generic posting interface for Gen. Jnl Line.</span></span>  
* <span data-ttu-id="b2780-106">CustPostApplyCustLedgEntry – bóka jafnanir viðskiptamanna, úr kóðaeiningu 226 CustEntry-Jafna bókaðar færslur.</span><span class="sxs-lookup"><span data-stu-id="b2780-106">CustPostApplyCustLedgEntry – post customer application, called from codeunit 226 CustEntry-Apply Posted Entries.</span></span>  
* <span data-ttu-id="b2780-107">VendPostApplyVendLedgEntry – bóka jafnanir lánardrottins, sóttar úr kóðaeiningu 227 VendEntry-Jafna bókaðar færslur.</span><span class="sxs-lookup"><span data-stu-id="b2780-107">VendPostApplyVendLedgEntry – post vendor application, called from codeunit 227 VendEntry-Apply Posted Entries.</span></span>  
* <span data-ttu-id="b2780-108">UnapplyCustLedgEntry – pósta ógildingu jöfnunar viðskiptamanns, sótt úr kóðaeiningu 226 CustEntry-Jafna bókaðar færslur</span><span class="sxs-lookup"><span data-stu-id="b2780-108">UnapplyCustLedgEntry – post unapply of customer application, called from codeunit 226 CustEntry-Apply Posted Entries</span></span>  
* <span data-ttu-id="b2780-109">UnapplyVendLedgEntry – pósta ógildingu jöfnunar viðskiptamanns, sótt úr kóðaeiningu 227 VendEntry-Jafna bókaðar færslur</span><span class="sxs-lookup"><span data-stu-id="b2780-109">UnapplyVendLedgEntry – post unapply of vendor application, called from codeunit 227 VendEntry-Apply Posted Entries</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b2780-110">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="b2780-110">See Also</span></span>  
[<span data-ttu-id="b2780-111">Hönnunarupplýsingar: Uppbygging bókunarvélar</span><span class="sxs-lookup"><span data-stu-id="b2780-111">Design Details: Posting Engine Structure</span></span>](design-details-posting-engine-structure.md)
