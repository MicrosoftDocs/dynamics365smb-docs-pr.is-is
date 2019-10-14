---
title: Hönnunarupplýsingar - Uppbygging bókunarviðmóts | Microsoft Docs
description: Í þessu efnisatriði er að finna yfirlit yfir altæk ferli í uppbyggingu bókunarviðmóts.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: posting, interface, design
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: f484c6474c840b4c2d802494407f8d819256596c
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/01/2019
ms.locfileid: "2306941"
---
# <a name="design-details-posting-interface-structure"></a><span data-ttu-id="87929-103">Hönnunarupplýsingar: Uppbygging bókunarviðmóts</span><span class="sxs-lookup"><span data-stu-id="87929-103">Design Details: Posting Interface Structure</span></span>
<span data-ttu-id="87929-104">Í [!INCLUDE[d365fin](includes/d365fin_md.md)] uppbyggingu bókunarviðmóts eru nokkur alþjóðleg ferli sem nota sömu uppbyggingu:</span><span class="sxs-lookup"><span data-stu-id="87929-104">In the [!INCLUDE[d365fin](includes/d365fin_md.md)] posting interface structure, there are several global procedures that use the same structure:</span></span>  
  
* <span data-ttu-id="87929-105">RunWithCheck RunWithoutCheck vinnslukóðar – almennt bókunarviðmót fyrir almenna</span><span class="sxs-lookup"><span data-stu-id="87929-105">RunWithCheck and RunWithoutCheck call procedure Code – generic posting interface for Gen.</span></span> <span data-ttu-id="87929-106">færslubókarlínu.</span><span class="sxs-lookup"><span data-stu-id="87929-106">Jnl Line.</span></span>  
* <span data-ttu-id="87929-107">CustPostApplyCustLedgEntry – bóka jafnanir viðskiptamanna, úr kóðaeiningu 226 CustEntry-Jafna bókaðar færslur.</span><span class="sxs-lookup"><span data-stu-id="87929-107">CustPostApplyCustLedgEntry – post customer application, called from codeunit 226 CustEntry-Apply Posted Entries.</span></span>  
* <span data-ttu-id="87929-108">VendPostApplyVendLedgEntry – bóka jafnanir lánardrottins, sóttar úr kóðaeiningu 227 VendEntry-Jafna bókaðar færslur.</span><span class="sxs-lookup"><span data-stu-id="87929-108">VendPostApplyVendLedgEntry – post vendor application, called from codeunit 227 VendEntry-Apply Posted Entries.</span></span>  
* <span data-ttu-id="87929-109">UnapplyCustLedgEntry – pósta ógildingu jöfnunar viðskiptamanns, sótt úr kóðaeiningu 226 CustEntry-Jafna bókaðar færslur</span><span class="sxs-lookup"><span data-stu-id="87929-109">UnapplyCustLedgEntry – post unapply of customer application, called from codeunit 226 CustEntry-Apply Posted Entries</span></span>  
* <span data-ttu-id="87929-110">UnapplyVendLedgEntry – pósta ógildingu jöfnunar viðskiptamanns, sótt úr kóðaeiningu 227 VendEntry-Jafna bókaðar færslur</span><span class="sxs-lookup"><span data-stu-id="87929-110">UnapplyVendLedgEntry – post unapply of vendor application, called from codeunit 227 VendEntry-Apply Posted Entries</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="87929-111">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="87929-111">See Also</span></span>  
[<span data-ttu-id="87929-112">Hönnunarupplýsingar: Uppbygging bókunarvélar</span><span class="sxs-lookup"><span data-stu-id="87929-112">Design Details: Posting Engine Structure</span></span>](design-details-posting-engine-structure.md)