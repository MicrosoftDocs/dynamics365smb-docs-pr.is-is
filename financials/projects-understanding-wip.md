---
title: "Skilningur á VÍG-aðferðm | Microsoft Docs"
description: "Lýsir mismunandi WIP-aðferðum sem hægt er að nota til að birta og fylgjast með fjárhagsupplýsingum fyrir störf sem eru í vinnslu."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: work in process, work in progress, calculate project WIP
ms.date: 03/28/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: d6f82b3eb086b53be8a091e7a805c745a74ac10f
ms.contentlocale: is-is
ms.lasthandoff: 05/04/2017


---
# <a name="understanding-wip-methods"></a>Að skila VÍV aðferðir
[!INCLUDE[d365fin](includes/d365fin_md.md)] styður eftirfarandi aðferðir við útreikning og skráningu um virði verka í vinnslu.

| VÍV-aðferð | Tegund útreiknings | Lýsing útreiknings |
| --- | --- | --- |
| Kostnaðarvirði |Samþykktar tekjur = Reikningshæft reikningsfært verð<br /><br /> Áætlaður heildarkostnaður = Reikningshæft heildarverð x Kostnaðarhlutfall áætlunar<br /><br /> VÍV-kostnaður = \(Prósentum lokið - Reikningsfærð %\) x Áætlaður heildarkostnaður<br /><br /> Prósentum lokið = Notkun (heildarkostnaður) / Heildarkostnaður á fjárhagsáætlun<br /> Reikningsfærð % = Reikningshæft reikningsfært verð<br /><br /> Reikningshæft heildarverð (samþykktur kostnaður) = Notkun (heildarkostnaður) VÍV |Útreikningar á kostnaðarvirði hefjast á því að reiknað er virði þess sem hefur verið innt af hendi með því að taka hluta áætlaðs heildarkostnaðar byggt á loknum prósentum. Reikningsfærður kostnaður er dreginn frá með því að taka hluta áætlaðs heildarkostnaðar byggt á reikningsfærðu prósentunni.<br /><br /> Skilyrði fyrir útreikningnum eru að reikningshæft heildarverð, heildarverð á fjárhagsáætlun og heildarkostnaður á fjárhagsáætlun sé rétt færður inn fyrir verkið í heild. |
| Sölukostnaður |Samþykktar tekjur = Reikningshæft reikningsfært verð<br /><br /> Samþykktur kostnaður = Heildarkostnaður á fjárhagsáætlun x Reikningsfærð prósenta<br /><br /> Reikningsfærð %= Reikningshæft reikningsfært verð / Reikningshæft heildarverð<br /><br /> \(Reikningsfærð % er dálkur í verkhlutalínum\)<br /><br /> VÍV - kostnaður = Notkun (heildarkostnaður) – Samþykktur kostnaður |Útreikningar á sölukostnaði hefjast á því að reiknaður er út samþykktur kostnaður. Kostnaður er samþykktur í hlutfalli byggt á heildarkostnaði á fjárhagsáætlun.<br /><br /> Skilyrði fyrir útreikningnum eru að reikningshæft heildarverð og heildarkostnaður á fjárhagsáætlun séu færð inn á réttan hátt fyrir allt verkið. |
| Söluvirði |Samþykktur kostnaður = Notkun (heildarkostnaður)<br /><br /> Samþykktar tekjur = Notkun (heildarverð) x Áætlað hlutfall reikningsfærslu<br /><br /> Endurheimt kostnaðar % = Reikningshæft heildarverð / Heildarverð á fjárhagsáætlun<br /><br /> VÍV-sala = Samþykkt sala - Reikningshæft reikningsfært verð |Útreikningar á söluvirði samþykkja tekjur í hlutfalli byggt á notkun (heildarkostnaði) og áætluðu hlutfalli kostnaðarendurheimtar.<br /><br /> Skilyrði fyrir útreikningnum eru að reikningshæft heildarverð og heildarverð á fjárhagsáætlun séu færð inn á réttan hátt fyrir allt verkið. |
| Áfangaaðferð |Samþykktur kostnaður = Notkun (heildarkostnaður)<br /><br /> Samþykktar tekjur = Reikningshæft heildarverð x Prósentum lokið<br /><br /> Prósentum lokið = Notkun (heildarkostnaður) / Heildarkostnaður á fjárhagsáætlun<br /> \(Kallað „Kostnaður loka %“ í verkhlutalínum\)<br /><br /> VÍV-sala = Samþykkt sala - Reikningshæft reikningsfært verð |Útreikningar á loknum prósentum samþykkja tekjur í hlutfalli byggt á loknum prósentum, þ.e. notkun (heildarkostnaði) á móti áætlunarkostnaði.<br /><br /> Skilyrði fyrir útreikningnum eru að reikningshæft heildarverð og heildarkostnaður á fjárhagsáætlun séu færð inn á réttan hátt fyrir allt verkið. |
| Samn. sem er lokið |WIP Upphæð = WIP Kostnaður upphæð = Notkun \(Heildarkostnaður\)<br /><br /> VÍV-söluupphæð = Reikningshæft \(Reikningsfært verð\) |Með valkostinum Samningi lokið eru tekjur og kostnaður ekki samþykkt fyrr en verkinu er lokið. Þetta getur verið æskilegt þegar mikil óvissa ríkir um áætlun kostnaðar og tekna verksins.<br /><br /> Öll notkun bókast á reikninginn Verk í vinnslu, kostnaður \(eign\) og öll reikningsfærð sala bókast á reikninginn VÍV Reikningsfærð sala \(skuld\) þar til verkinu er lokið. |

## <a name="see-also"></a>Sjá einnig
[Verkefnastjórnun](projects-manage-projects.md)  
[Fjármál](finance.md)  
[Innkaup](purchasing-manage-purchasing.md)         
[Sala](sales-manage-sales.md)      
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

