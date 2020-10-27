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
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 231148c304c5f2dabba5c69c442dfd0cfdc6397d
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/01/2020
ms.locfileid: "3921943"
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