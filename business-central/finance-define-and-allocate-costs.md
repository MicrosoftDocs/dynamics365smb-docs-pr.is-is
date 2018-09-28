---
title: "Skilgreina og úthluta kostnaði | Microsoft Docs"
description: "Kostnaðarúthlutun færir kostnað og tekjur milli kostnaðargerða, kostnaðarstaða og kostnaðhluta. Hægt er að tilgreina eins margar línur og þörf krefur."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 7bdddcadf3fb7dceb762354e8fa527158782b676
ms.contentlocale: is-is
ms.lasthandoff: 03/22/2018

---
# <a name="defining-and-allocating-costs"></a>Skilgreina og úthluta kostnaði
Kostnaðarúthlutun færir kostnað og tekjur milli kostnaðargerða, kostnaðarstaða og kostnaðhluta. Hægt er að tilgreina eins margar línur og þörf krefur. Hver úthlutun samanstendur af:  

-   Úthlutunaruppruni.  
-   Eitt eða fleiri úthlutunarmörk.  

Úthlutunaruppruninn kveður á um hvaða kostnaði verður að úthluta, og úthlutunarmörk skilgreina hvert kostnaðinum skuli úthlutað. Til dæmis getur úthlutunaruppruninn verið kostnaðurinn fyrir kostnaðartegundina Rafmagn og hiti. Öllum rafmagns- og hitakostnaði er úthlutað á þrjá kostnaðarstaði: Verkstæði, Framleiðslu og Sölu. Þessir kostnaðarstaðir eru það sem úthluta skal á.  

Fyrir hvern úthlutunaruppruna skilgreinir notandi úthlutunarstig, gildistímabil og afbrigði sem flokkunarkenni. Hægt er að nota keyrslu til að setja afmarkanir til að velja úthlutunarskilgreiningar og keyra síðan kostnaðarúthlutun . sjálfkrafa.  

Fyrir hvert úthlutunarmarki skilgreinir notandi úthlutunarstofninn. Úthlutunarstofn getur annað hvort verið fastur eða kvikur.  

-   Fastir úthlutunargrunnar eru byggðir á tilteknu gildi, s.s. ferfetum eða skilgreindu úthlutunarhlutfalli, s.s. 5:2:4.  
-   Kvik úthlutun fer eftir breytanlegum gildum, eins og fjölda starfsmanna í kostnaðarstöð eða sölutekjum kostnaðarliðar á tilteknu tímabili.  

Eftirfarandi tafla lýsir röð verkefna með tenglum í efnisatriði þar sem þeim er lýst.

|Til|Sjá|  
|--------|---------|  
|Uppsetning úthlutunaruppruna og úthlutunarmarka hans.|[Setja upp uppruna og markhópa úthlutanna](finance-how-to-set-up-allocation-source-and-targets.md)|  
|Setja upp margvíslegar afmarkanir fyrir kvik úthlutunargrunna.|[Uppsetning afmarkanir fyrir Kvik úthlutunargrunnar.](finance-setting-filters-for-dynamic-allocation-bases.md)|  
|Sjá dæmi um hvernig á að skilgreina fasta úthlutun.|[Dæmi: Skilgreining fastrar úthlutunar á grundvelli úthlutunarhlutfalls](finance-scenario-example-defining-static-allocations-based-on-allocation-ratio.md)|  
|Sjá dæmi um hvernig á að skilgreina kvika úthlutun.|[Dæmi: Skilgreining kvikrar úthlutunar á grundvelli seldra vara](finance-scenario-example-defining-dynamic-allocations-based-on-items-sold.md)|  

## <a name="see-also"></a>Sjá einnig  
 [Uppsetning kostnaðarbókhalds](finance-set-up-cost-accounting.md)   
 [Flytja og bóka kostnaðarfærslur](finance-transfer-and-post-cost-entries.md)   
 [Kostnaðarreikningur](finance-manage-cost-accounting.md)   
 [Orðalisti í kostnaðarbókhaldi](finance-terminology-in-cost-accounting.md)   
 [Um kostnaðarbókhald](finance-about-cost-accounting.md)

