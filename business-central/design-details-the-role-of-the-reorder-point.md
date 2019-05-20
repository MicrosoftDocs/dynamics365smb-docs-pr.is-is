---
title: Hönnunarupplýsingar - Hlutverk endurpöntunarmarks | Microsoft Docs
description: Þetta efnisatriði fjallar um mikilvægi þess að setja upp endurpöntunarmark, svo þú vitir hvenær skal panta frekari birgðir.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: desigh, reorder, demand, supply
ms.date: 07/01/2017
ms.author: sgroespe
ms.openlocfilehash: 836da35166d947de8c37128d9ed8807914594c55
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/29/2019
ms.locfileid: "1246083"
---
# <a name="design-details-the-role-of-the-reorder-point"></a>Hönnunarupplýsingar: Hlutverk endurpöntunarmarks
Í viðbót við almenna jafnvægi á framboð og eftirspurn, áætlanagerð kerfi verður einnig fylgjast birgðastigum fyrir viðkomandi vöru að virða skilgreind endurröðun stefnu.  
  
Endurpöntunarmark stendur fyrir eftirspurn á afhendingartíma. Þegar áætlaðar birgðir fara undir birgðastigið sem endurpöntunarmark skilgreinir er kominn tími til að panta meira magn. Á meðan eiga birgðir smám saman að minnka og mögulega ná núlli (eða öryggisbirgðastigi), þar til fyllt er á.  
  
Í samræmi mun áætlunarkerfið stinga upp á framboðspöntun sem er dagsett í framtíðinni á þeim tíma þegar áætlaðar birgðir fara undir endurpöntunarmark.  
  
Endurpöntunarmarkið endurspeglar tiltekið birgðastig. Hins vegar geta birgðastig hreyfst töluvert innan tímarammans og þess vegna verður áætlanakerfið að fylgjast stöðugt með áætluðum tiltækum birgðum.  
  
## <a name="see-also"></a>Sjá einnig  
[Hönnunarupplýsingar: Endurpöntunarstefnur](design-details-reordering-policies.md)   
[Hönnunarupplýsingar: áætlunarfæribreyta](design-details-planning-parameters.md)   
[Hönnunarupplýsingar: Meðhöndlun endurpöntunarstefna](design-details-handling-reordering-policies.md)   
[Hönnunarupplýsingar: framboðsáætlun](design-details-supply-planning.md)