---
title: Hönnunarupplýsingar - Lota fyrir lotu | Microsoft Docs
description: Lærið að nota lota fyrir lotu regluna til að gera upp pöntunarmagn á grunni eftispurnar.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
redirect_url: design-details-handling-reordering-policies
ms.openlocfilehash: 5669378383d94b33a25a60a882709885e1463a6d
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/01/2019
ms.locfileid: "2303103"
---
# <a name="design-details-lot-for-lot"></a>Hönnunarupplýsingar: lota fyrir lotu
Lota-fyrir-lotu reglan er sveigjanlegust vegna þess að kerfið bregst bara við raunverulegri eftirspurn og bregst auk þess við væntanlegri eftirspurn samkvæmt spám og standandi pöntunum og ákvarðar svo magn pantanan á grundvelli eftirspurnarinnar. Lota-fyrir-lotu reglan beinist að A- og B-vörum þar sem hægt er að samþykkja birgðir en ætti helst að forðast það.  

Að sumu leyti er lota fyrir lotu stefnan eins og pantanastefnan en er með almenna nálgun á vörur; það getur samþykkt magn í birgðum, og það flokkareftirspurn og samsvarandi framboð í tímarömmum skilgreindum af notanda.  

Tímaramminn er skilgreindum í reitnum **Tímarammi**. Kerfið vinnur með lágmarks tímaramma upp á einn dag, þar sem það er minnsta tímamælieining fyrir birgðir og eftirspurn í kerfin (þó svo að í raun geti tímamælieining á framleiðslupöntunum og íhlutaþörfum verið sekúndur).  

Tímaramminn setur einnig takmörkun á það hvenær birgðapöntun er enduráætluð til að mæta tiltekinni eftirspurn. Ef framboð er innan tímarammans verður það enduráætlað inn eða út til að svara eftirspurninni. Annars, ef það liggur fyrr, mun það valda óþarfa uppsöfnun birgða og ætti að afturkalla. Ef það er síðar verður nýtt framboð stofnað í staðinn.  

Með þessari reglu er einnig mögulegt að skilgreina öryggisbirgðir til að bæta upp hugsanlegar sveiflur á birgðum eða til að mæta skyndilegri eftirspurn.  

Þar sem birgðapöntunarmagn byggir á raunveruleg eftirspurn getur það borgað sig að nota raðabreytur: slétta pöntunarmagn til að það passi við tiltekna pöntunarstuðul (eða innkaupamælieiningu), auka pöntuina upp í tiltekið magn, eða minnka magnið í hámarksmagn (og því búa til tvær eða fleiri birgðir til að uppfylla allt magnið).  

## <a name="see-also"></a>Sjá einnig  
[Hönnunarupplýsingar: Endurpöntunarstefnur](design-details-reordering-policies.md)   
[Hönnunarupplýsingar: Áætlunarfæribreytur](design-details-planning-parameters.md)   
[Hönnunarupplýsingar: Meðhöndlun endurpöntunarstefna](design-details-handling-reordering-policies.md)   
[Hönnunarupplýsingar: framboðsáætlun](design-details-supply-planning.md)
