---
title: Hönnunarupplýsingar - Uppbygging bókunarviðmóts
description: Í þessu efnisatriði er að finna yfirlit yfir altæk ferli og hönnunarupplýsingar í uppbyggingu bókunarviðmóts.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: posting, interface, design
ms.date: 06/15/2021
ms.author: edupont
ms.openlocfilehash: 80805675a3ecb1c847f0a55c2dc50008faa3b21f
ms.sourcegitcommit: e562b45fda20ff88230e086caa6587913eddae26
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/30/2021
ms.locfileid: "6318385"
---
# <a name="design-details-posting-interface-structure"></a>Hönnunarupplýsingar: Uppbygging bókunarviðmóts
Í [!INCLUDE[prod_short](includes/prod_short.md)] uppbyggingu bókunarviðmóts eru nokkur alþjóðleg ferli sem nota sömu uppbyggingu:  
  
* RunWithCheck RunWithoutCheck vinnslukóðar – almennt bókunarviðmót fyrir almenna færslubókarlínu.  
* CustPostApplyCustLedgEntry – bóka jafnanir viðskiptamanna, úr kóðaeiningu 226 CustEntry-Jafna bókaðar færslur.  
* VendPostApplyVendLedgEntry – bóka jafnanir lánardrottins, sóttar úr kóðaeiningu 227 VendEntry-Jafna bókaðar færslur.  
* UnapplyCustLedgEntry – pósta ógildingu jöfnunar viðskiptamanns, sótt úr kóðaeiningu 226 CustEntry-Jafna bókaðar færslur  
* UnapplyVendLedgEntry – pósta ógildingu jöfnunar viðskiptamanns, sótt úr kóðaeiningu 227 VendEntry-Jafna bókaðar færslur  
  
## <a name="see-also"></a>Sjá einnig  
[Hönnunarupplýsingar: Uppbygging bókunarvélar](design-details-posting-engine-structure.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]