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
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 5905a16341dc487aaf624810d691ac4628ac2e30
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/29/2019
ms.locfileid: "1239522"
---
# <a name="design-details-posting-interface-structure"></a>Hönnunarupplýsingar: Uppbygging bókunarviðmóts
Í [!INCLUDE[d365fin](includes/d365fin_md.md)] uppbyggingu bókunarviðmóts eru nokkur alþjóðleg ferli sem nota sömu uppbyggingu:  
  
* RunWithCheck RunWithoutCheck vinnslukóðar – almennt bókunarviðmót fyrir almenna færslubókarlínu.  
* CustPostApplyCustLedgEntry – bóka jafnanir viðskiptamanna, úr kóðaeiningu 226 CustEntry-Jafna bókaðar færslur.  
* VendPostApplyVendLedgEntry – bóka jafnanir lánardrottins, sóttar úr kóðaeiningu 227 VendEntry-Jafna bókaðar færslur.  
* UnapplyCustLedgEntry – pósta ógildingu jöfnunar viðskiptamanns, sótt úr kóðaeiningu 226 CustEntry-Jafna bókaðar færslur  
* UnapplyVendLedgEntry – pósta ógildingu jöfnunar viðskiptamanns, sótt úr kóðaeiningu 227 VendEntry-Jafna bókaðar færslur  
  
## <a name="see-also"></a>Sjá einnig  
[Hönnunarupplýsingar: Uppbygging bókunarvélar](design-details-posting-engine-structure.md)