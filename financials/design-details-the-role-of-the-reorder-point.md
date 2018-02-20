---
title: "Hönnunarupplýsingar - Hlutverk endurpöntunarmarks | Microsoft Docs"
description: "Þetta efnisatriði fjallar um mikilvægi þess að setja upp endurpöntunarmark, svo þú vitir hvenær skal panta frekari birgðir."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: desigh, reorder, demand, supply
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 5b5e3cec4bc5af8188470ea1d711422c0130677e
ms.contentlocale: is-is
ms.lasthandoff: 12/14/2017

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
