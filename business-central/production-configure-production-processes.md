---
title: "Grunnstilla framleiðsluferli | Microsoft Docs"
description: "Til að geta umbreytt efni í tilbúna vöru þarf framleiðsluforði, líkt og uppskriftir, leiðir, vélar og starfsmenn á vélum, að vera settur upp í kerfinu."
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
ms.openlocfilehash: 2419755f5788eb7cb8ed464ac97fccd7e63e795c
ms.contentlocale: is-is
ms.lasthandoff: 03/22/2018

---
# <a name="setting-up-manufacturing"></a>Uppsetning framleiðslu
Til að geta umbreytt efni í tilbúna vöru þarf framleiðsluforði, líkt og uppskriftir, leiðir, vélar og starfsmenn á vélum, að vera settur upp í kerfinu.

Í kerfinu teljast starfsmenn á vélum og vélar til vélastöðva sem má flokka í vinnustöðvar og vinnustöðvahópa. Þegar þessi forði er þekktur má úthluta á hann aðgerðum samkvæmt skilgreindri uppskrift vörunnar, og leiðarskipulagi, og samkvæmt afkastagetu véla- eða vinnustöðvarinnar. Einnig er hægt að ákvarða afkastagetu hjá hverjum forða. Afkastageta er ákvörðuð út frá tiltækum vinnustundum á hverri véla- og vinnustöð og er stjórnað af dagatölum fyrir hvert stig. Í dagatali vinnustöðvar eru tilgreindir vinnudagar eða -stundir, vaktir, frídagar og fjarvistir sem hafa áhrif á mögulega heildarafkastagetu (oftast mæld í mínútum). Allt er þetta ákvarðað af tilgreindum gildum skilvirkni og getu.  

Þegar framleiðsla hefur verið sett upp, er hægt að skipuleggja og framkvæma framleiðsluskipanir. Frekari upplýsingar eru í [Áætlunargerð](production-planning.md) og [Framleiðsla](production-manage-manufacturing.md).  

 Eftirfarandi tafla lýsir röð verkefna með tenglum í efnisatriði þar sem þeim er lýst.   

|**Til að**|**Sjá**|  
|------------|-------------|  
|Grunnstilla framleiðslumöguleikana, til dæmis ákvarða vinnustundir í vinnusal og velja áætlunarreglur.|**Framleiðslugrunnur** síðan.|  
|Skilgreina staðlaða vinnuviku í framleiðsludeildinni út frá upphafi og enda hvers vinnudags og tengdrar vaktar.|[Stofna dagatal verkstæðis](production-how-to-create-work-center-calendars.md)|  
|Skipuleggja föst gildi og skilyrði framleiðsluforða í vinnu- eða vélastöðvum til að stýra frálagi framleiðslu sem fram fer í þeim.|[Setja upp vinnu- og vélastöðvar](production-how-to-set-up-work-and-machine-centers.md)|
|Raða framleiðsluaðgerðir í þá röð sem krafist er og úthluta þeim til vinnu- og vélastöðva með þeim fjölda vinnustunda sem telst nauðsynlegur.|[Stofna leiðir](production-how-to-create-routings.md)|
|Raða framleiðslueiningar eða samsettar einingar undir framleidda yfirvöru og staðfesta uppskriftina fyrir framkvæmd í vinnustöðvum.|[Búa til framleiðsluuppskriftir](production-how-to-create-production-boms.md)|
|Tryggja að rétt einingamagn sé tiltækt þegar framleiddar vörur eru geymdar á lager undir einni mælieiningu en framleiddar í annarri.|[Vinna með mælieiningu framleiðslukeyrslu](production-how-to-use-the-manufacturing-batch-unit-of-measure.md)|  
|Skilgreina samsafn framleiðsluvara með svipað framleiðsluferli til að spara notkun. Til dæmis er hægt að framleiða fjögur stykki af sömu vörunni úr einni plötu og 10 stykki af annarri, ólíkri vöru, á sama tíma.|[Vinna með framleiðslusamsafn](production-how-work-family.md)|
|Nota staðlaða verkhluta til að einfalda stofnun leiða með því að bæta aukaupplýsingum snögglega við ítrekað ferli.|[Setja upp staðlaðar leiðarlínur](production-how-set-up-standard-routing-lines.md)|  
|Undirbúa vinnustöðvar og leiðir til að þær sýni úthýsta framleiðslu.|[Úthýsa framleiðslu til undirverktaka](production-how-to-subcontract-manufacturing.md)|  

## <a name="see-also"></a>Sjá einnig
[Framleiðsla](production-manage-manufacturing.md)    
[Áætlun](production-planning.md)   
[Birgðir](inventory-manage-inventory.md)  
[Innkaup](purchasing-manage-purchasing.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

