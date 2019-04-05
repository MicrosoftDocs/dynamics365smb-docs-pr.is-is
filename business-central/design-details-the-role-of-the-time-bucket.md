---
title: Hönnunarupplýsingar - Hlutverk tímarammi | Microsoft Docs
description: Tilgangurinn með tímarammanum er að safna saman eftirspurnartilvikum innan tímasíðunnar til að útbúa sameiginlega birgðapöntun.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2018
ms.author: sgroespe
redirect_url: design-details-handling-reordering-policies
ms.openlocfilehash: ff748a192d8d1650a708ab70ec33ccc7bfd53c48
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/08/2019
ms.locfileid: "799966"
---
# <a name="design-details-the-role-of-the-time-bucket"></a>Hönnunarupplýsingar: Hlutverk tímaramma
Tilgangurinn með tímarammanum er að safna saman eftirspurnartilvikum innan tímasíðunnar til að útbúa sameiginlega birgðapöntun.  

 Fyrir endurpöntunarstefnur sem nota endurpöntunarmark er hægt að skilgreina tímaramma. Þetta tryggir að eftirspurn innan sama tímabils sé safnað upp áður en áhrifin á áætlaðar birgðir eru könnuð, og hvort endurpöntunarmarki hafi verið náð. Ef farið er yfir endurpöntunarmarkið er ný birgðapöntun áætluð framvirkt frá lokum tímabilsins sem skilgreint er í tímarammanum. Tímaramminn hefst á upphafsdagsetningu áætlunar.  

 Tímaramminn endurspeglar það handvirka ferli að kanna birgðastigið oft fremur en fyrir hverja færslu. Notandinn verður að tilgreina tíðnina (tímarammann). Til dæmis safnar notandinn saman öllum vöruþörfum frá einum lánardrottni til að leggja inn vikulega pöntun.  

 ![Dæmi um tímaramma í skipulagningu](media/nav_app_supply_planning_2_reorder_cycle.png "Dæmi um tímaramma í skipulagningu")  

 Tímaramminn er vanalega notaður til að forðast keðjuverkun. Til dæmis jöfn lína framboðs og eftirspurnar þar sem fyrri eftirspurn er afturkölluð eða ný búin til. Niðurstaðan ætti að vera sú að framboðspöntunin (nema sú síðasta) er enduráætluð.  

## <a name="see-also"></a>Sjá einnig  
 [Hönnunarupplýsingar: Endurpöntunarstefnur](design-details-reordering-policies.md)   
 [Hönnunarupplýsingar: áætlunarfæribreyta](design-details-planning-parameters.md)   
 [Hönnunarupplýsingar: Meðhöndlun endurpöntunarstefna](design-details-handling-reordering-policies.md)   
 [Hönnunarupplýsingar: framboðsáætlun](design-details-supply-planning.md)
