---
title: Grunnstilling framleiðsluferlis
description: Til að geta umbreytt efni í tilbúna vöru þarf framleiðsluforði, líkt og uppskriftir, leiðir, vélar og starfsmenn á vélum, að vera settur upp í kerfinu.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 99000768, 99000779, 99000780, 99000866
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 0ae567c2ac44c1b8b272b7a7f2ed1e9ba4826b60
ms.sourcegitcommit: 8ad79e0ec6e625796af298f756a142624f514cf3
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/30/2022
ms.locfileid: "9605766"
---
# <a name="setting-up-manufacturing"></a>Uppsetning framleiðslu

Til að geta umbreytt efni í tilbúna vöru þarf framleiðsluforði, líkt og uppskriftir, leiðir, vélar og starfsmenn á vélum, að vera settur upp í kerfinu.

Í kerfinu teljast starfsmenn á vélum og vélar til vélastöðva sem má flokka í vinnustöðvar og vinnustöðvahópa. Þegar þessi forði er þekktur má úthluta á hann aðgerðum samkvæmt skilgreindri uppskrift vörunnar, og leiðarskipulagi, og samkvæmt afkastagetu véla- eða vinnustöðvarinnar. Einnig er hægt að ákvarða afkastagetu hjá hverjum forða. Afkastageta er ákvörðuð út frá tiltækum vinnustundum á hverri véla- og vinnustöð og er stjórnað af dagatölum fyrir hvert stig. Í dagatali vinnustöðvar eru tilgreindir vinnudagar eða -stundir, vaktir, frídagar og fjarvistir sem hafa áhrif á mögulega heildarafkastagetu (oftast mæld í mínútum). Allt er þetta ákvarðað af tilgreindum gildum skilvirkni og getu.  

Þegar framleiðsla hefur verið sett upp, er hægt að skipuleggja og framkvæma framleiðsluskipanir. Frekari upplýsingar eru í [Áætlunargerð](production-planning.md) og [Framleiðsla](production-manage-manufacturing.md).  

Eftirfarandi tafla lýsir röð verkefna með tenglum í efnisatriði þar sem þeim er lýst.

|**Til að**|**Sjá**|  
|------------|-------------|  
|Grunnstilla framleiðslumöguleikana, til dæmis ákvarða vinnustundir í vinnusal og velja áætlunarreglur.|**Framleiðslugrunnur** síðan.|
|PlanningÁ flipanum **Áætlun** á síðunni **Framleiðsluuppsetning** , skaltu stilla altækar færibreytur áætlunar sem hnekkja færibreytum á einstökum birgðaspjöldum.|[Hönnunarupplýsingar: áætlunarfæribreyta](design-details-planning-parameters.md)|
|Skilgreina staðlaða vinnuviku í framleiðsludeildinni út frá upphafi og enda hvers vinnudags og tengdrar vaktar.|[Stofna dagatal verkstæðis](production-how-to-create-work-center-calendars.md)|  
|Skipuleggja föst gildi og skilyrði framleiðsluforða í vinnu- eða vélastöðvum til að stýra frálagi framleiðslu sem fram fer í þeim.|[Setja upp vinnu- og vélastöðvar](production-how-to-set-up-work-and-machine-centers.md)|
|Raða framleiðsluaðgerðir í þá röð sem krafist er og úthluta þeim til vinnu- og vélastöðva með þeim fjölda vinnustunda sem telst nauðsynlegur.|[Stofna leiðir](production-how-to-create-routings.md)|
|Raða framleiðslueiningar eða samsettar einingar undir framleidda yfirvöru og staðfesta uppskriftina fyrir framkvæmd í vinnustöðvum.|[Búa til framleiðsluuppskriftir](production-how-to-create-production-boms.md)|
|Tryggja að rétt einingamagn sé tiltækt þegar framleiddar vörur eru geymdar á lager undir einni mælieiningu en framleiddar í annarri.|[Vinna með mælieiningu framleiðslukeyrslu](production-how-to-use-the-manufacturing-batch-unit-of-measure.md)|  
|Skilgreina samsafn framleiðsluvara með svipað framleiðsluferli til að spara notkun. Til dæmis er hægt að framleiða fjögur stykki af sömu vörunni úr einni plötu og 10 stykki af annarri, ólíkri vöru, á sama tíma.|[Vinna með framleiðslusamsafn](production-how-work-family.md)|
|Nota staðlaða verkhluta til að einfalda stofnun leiða með því að bæta aukaupplýsingum snögglega við ítrekað ferli.|[Setja upp staðlaðar leiðarlínur](production-how-set-up-standard-routing-lines.md)|  
|Undirbúa vinnustöðvar og leiðir til að þær sýni úthýsta framleiðslu.|[Úthýsa framleiðslu til undirverktaka](production-how-to-subcontract-manufacturing.md)|  

## <a name="see-also"></a>Sjá einnig .

[Framleiðsla](production-manage-manufacturing.md)  
[Áætlun](production-planning.md)  
[Birgðir](inventory-manage-inventory.md)  
[Innkaup](purchasing-manage-purchasing.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
