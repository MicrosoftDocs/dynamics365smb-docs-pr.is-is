---
title: VÍV-aðferðir við útreikning og skráningu verkframvindu
description: 'Lýsir mismunandi verkaðferðum í vinnslu (VÍV) sem hægt er að nota til að bóka, fylgjast með og reikna út fjárhagslegar upplýsingar fyrir verkefni sem eru í vinnslu.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: conceptual
ms.search.keywords: 'work in process, work in progress, calculate project WIP'
ms.search.form: '1010,'
ms.date: 02/22/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# <a name="understanding-wip-methods-in-project-management"></a>Að skilja VÍV-aðferðir í verkefnastjórnun

Þegar verk er unnið er efni, forði og annar kostnaður notaður og það þarf að bóka á verkið. Verk í vinnslu (VÍV) er eiginleiki sem gerir kleift að meta fjárhagslegt virði verka í fjárhag á meðan verkefnin eru í gangi. Oft er hægt að bóka kostnað vegna verks áður en verk er reikningsfært. Þegar aðeins kostnaður hefur verið bókaður verður fjárhagsyfirlitið ónákvæmt.

Til að rekja gildi í fjárhagnum er hægt að reikna út VÍV og bóka gildið í fjárhag. Nánari upplýsingar eru [í Fylgjast með verkframvindu og afköstum](projects-how-monitor-progress-performance.md).

[!INCLUDE[prod_short](includes/prod_short.md)] styður eftirfarandi aðferðir við útreikning og skráningu um virði verka í vinnslu.

| VÍV-aðferð | Tegund útreiknings | Lýsing útreiknings |
| --- | --- | --- |
| Kostnaðargildi |Samþykktar tekjur = Reikningshæft reikningsfært verð <br /><br />Hlutfall kostnaðar áætlana = Heildarkostnaður á fjárhagsáætlun / Heildarverð á fjárhagsáætlun <br /><br />Áætlaður heildarkostnaður = Reikningshæft heildarverð x Kostnaðarhlutfall áætlunar <br /><br />Prósentum lokið = Notkun (heildarkostnaður) / Heildarkostnaður á fjárhagsáætlun <br /><br />Reikningsfærð %= Reikningshæft reikningsfært verð / Reikningshæft heildarverð <br /><br />VÍV-kostnaður = (Prósentum lokið - Reikningsfærð %) x Áætlaður heildarkostnaður <br /><br />Samþykktur kostnaður = Notkun (heildarkostnaður) - VÍV-kostnaður|Útreikningar á kostnaðarvirði hefjast á því að reiknað er virði þess sem hefur verið innt af hendi með því að taka hluta áætlaðs heildarkostnaðar byggt á loknum prósentum. Reikningsfærður kostnaður er dreginn frá með því að taka hluta áætlaðs heildarkostnaðar byggt á reikningsfærðu prósentunni.<br /><br />Þessi útreikningur krefst þess að reikningshæft heildarverð, heildarverð á fjárhagsáætlun og heildarkostnaður á fjárhagsáætlun sé rétt færður inn fyrir allt verkið. |
| Sölukostnaður |Samþykktar tekjur = Reikningshæft reikningsfært verð<br /><br /> Samþykktur kostnaður = Heildarkostnaður á fjárhagsáætlun x Reikningsfærð prósenta<br /><br /> Reikningsfærð %= Reikningshæft reikningsfært verð / Reikningshæft heildarverð<br /> (Reikningsfærð % er dálkur í verkhlutalínum)<br /><br /> VÍV - kostnaður = Notkun (heildarkostnaður) – Samþykktur kostnaður |Útreikningar á sölukostnaði hefjast á því að reiknaður er út samþykktur kostnaður. Kostnaður er samþykktur í hlutfalli byggt á heildarkostnaði á fjárhagsáætlun.<br /><br /> Þessi útreikningur krefst þess að reikningshæft heildarverð og heildarkostnaður á fjárhagsáætlun séu færð inn á réttan hátt fyrir allt verkið. |
| Sölugildi |Samþykktur kostnaður = Notkun (heildarkostnaður)<br /><br /> Samþykktar tekjur = Notkun (heildarverð) x Áætlað hlutfall reikningsfærslu<br /><br /> Endurheimt kostnaðar % = Reikningshæft heildarverð / Heildarverð á fjárhagsáætlun<br /><br /> VÍV-sala = Samþykkt sala - Reikningshæft reikningsfært verð |Útreikningar á söluvirði samþykkja tekjur í hlutfalli byggt á notkun (heildarkostnaði) og áætluðu hlutfalli kostnaðarendurheimtar.<br /><br /> Þessi útreikningur krefst þess að reikningshæft heildarverð og heildarverð á fjárhagsáætlun séu færð inn á réttan hátt fyrir allt verkið. |
| Prósentum lokið |Samþykktur kostnaður = Notkun (heildarkostnaður)<br /><br /> Samþykktar tekjur = Reikningshæft heildarverð x Prósentum lokið<br /><br /> Prósentum lokið = Notkun (heildarkostnaður) / Heildarkostnaður á fjárhagsáætlun<br /> (Tekin upp í **Svæðið Kostnaðar lokið %** í verkhlutalínum)<br /><br /> VÍV-sala = Samþykkt sala - Reikningshæft reikningsfært verð |Útreikningar á loknum prósentum samþykkja tekjur í hlutfalli byggt á loknum prósentum, þ.e. notkun (heildarkostnaði) á móti áætlunarkostnaði.<br /><br /> Þessi útreikningur krefst þess að reikningshæft heildarverð og heildarkostnaður á fjárhagsáætlun séu færð inn á réttan hátt fyrir allt verkið. |
| Samn. sem er lokið |VÍV-upphæð = VÍV-kostnaðarupphæð = Notkun (heildarkostnaður)<br /><br /> VÍV-söluupphæð = Reikningshæft (Reikningsfært verð) |Samningi lokið samþykkir ekki tekjur og kostnað fyrr en verkinu er lokið. Þetta gæti verið æskilegt þegar mikil óvissa ríkir um áætlanir um kostnað og tekjur verkefnisins.<br /><br /> Öll notkun er bókuð á VÍV-kostnaðarreikning (eign) og öll reikningsfærð sala er bókuð á VÍV-reikning reikningsfærðrar sölu (skuld) þar til verkefninu er lokið. |

## <a name="see-also"></a>Sjá einnig .

[Verkefnastjórnun](projects-manage-projects.md)  
[Fjármál](finance.md)  
[Innkaup](purchasing-manage-purchasing.md)  
[Sala](sales-manage-sales.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
