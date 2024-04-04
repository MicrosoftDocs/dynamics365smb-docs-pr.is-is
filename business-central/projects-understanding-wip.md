---
title: VÍV aðferðir til að reikna út og skrá framvindu verks
description: 'Lýsir mismunandi Verk í vinnslu (VÍV)-aðferðum sem hægt er að nota til að bóka, fylgjast með og reikna út fjárhagsupplýsingar fyrir verk sem eru í vinnslu.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'work in process, work in progress, calculate project WIP'
ms.search.form: 1010
ms.date: 04/01/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="understanding-wip-methods-in-project-management"></a>Að skilja VÍV-aðferðir í verkefnastjórnun

Þegar verk er unnið er efni, forði og annar kostnaður notuð og þetta þarf að bóka á verkið. Verk í vinnslu (VÍV) er eiginleiki þar sem hægt er að meta fjárhagslegt virði verka í fjárhag eftir því sem verkinu miðar áfram. Oft er kostnaður bókaður áður en verk er reikningsfært. Þegar aðeins kostnaður hefur verið bókaður verður fjárhagsyfirlitið ónákvæmt.

Til að rekja gildi í fjárhagnum er hægt að reikna út VÍV og bóka gildið í fjárhag. Frekari upplýsingar eru í [Fylgst með framvindu og afköstum](projects-how-monitor-progress-performance.md).

[!INCLUDE[prod_short](includes/prod_short.md)] styður eftirfarandi aðferðir við útreikning og skráningu um virði verka í vinnslu.

| VÍV-aðferð | Tegund útreiknings | Lýsing útreiknings |
| --- | --- | --- |
| Kostnaðargildi |Samþykktar tekjur = Reikningshæft reikningsfært verð <br /><br />Kostnaðarhlutfall fjárhagsáætlunar = áætluð Heildarkostnaður/áætlun Heildarverð <br /><br />Áætlaður heildarkostnaður = Reikningshæft heildarverð x Kostnaðarhlutfall áætlunar <br /><br />Prósentum lokið = Notkun (heildarkostnaður) / Heildarkostnaður á fjárhagsáætlun <br /><br />Reikningsfærð %= Reikningshæft reikningsfært verð / Reikningshæft heildarverð <br /><br />VÍV-kostnaður = (prósenta lokins reikningsfærðs%) x Áætlaður Heildarkostnaður <br /><br />Viðurkenndur kostnaður = notkun Heildarkostnaður-VÍV-kostnaður|Útreikningar á kostnaðarvirði hefjast á því að reiknað er virði þess sem hefur verið innt af hendi með því að taka hluta áætlaðs heildarkostnaðar byggt á loknum prósentum. Reikningsfærður kostnaður er dreginn frá með því að taka hluta áætlaðs heildarkostnaðar byggt á reikningsfærðu prósentunni.<br /><br />Skilyrði fyrir útreikningnum eru að reikningshæft heildarverð, heildarverð á fjárhagsáætlun og heildarkostnaður á fjárhagsáætlun sé rétt færður inn fyrir verkið í heild. |
| Sölukostnaður |Samþykktar tekjur = Reikningshæft reikningsfært verð<br /><br /> Samþykktur kostnaður = Heildarkostnaður á fjárhagsáætlun x Reikningsfærð prósenta<br /><br /> Reikningsfærð %= Reikningshæft reikningsfært verð / Reikningshæft heildarverð<br /> (Reikningsfærð % er til sem dálkur í verkhlutalínum)<br /><br /> VÍV - kostnaður = Notkun (heildarkostnaður) – Samþykktur kostnaður |Útreikningar á sölukostnaði hefjast á því að reiknaður er út samþykktur kostnaður. Kostnaður er samþykktur í hlutfalli byggt á heildarkostnaði á fjárhagsáætlun.<br /><br /> Skilyrði fyrir útreikningnum eru að reikningshæft heildarverð og heildarkostnaður á fjárhagsáætlun séu færð inn á réttan hátt fyrir allt verkið. |
| Söluvirði |Samþykktur kostnaður = Notkun (heildarkostnaður)<br /><br /> Samþykktar tekjur = Notkun (heildarverð) x Áætlað hlutfall reikningsfærslu<br /><br /> Endurheimt kostnaðar % = Reikningshæft heildarverð / Heildarverð á fjárhagsáætlun<br /><br /> VÍV-sala = Samþykkt sala - Reikningshæft reikningsfært verð |Útreikningar á söluvirði samþykkja tekjur í hlutfalli byggt á notkun (heildarkostnaði) og áætluðu hlutfalli kostnaðarendurheimtar.<br /><br /> Skilyrði fyrir útreikningnum eru að reikningshæft heildarverð og heildarverð á fjárhagsáætlun séu færð inn á réttan hátt fyrir allt verkið. |
| Áfangaaðferð |Samþykktur kostnaður = Notkun (heildarkostnaður)<br /><br /> Samþykktar tekjur = Reikningshæft heildarverð x Prósentum lokið<br /><br /> Prósentum lokið = Notkun (heildarkostnaður) / Heildarkostnaður á fjárhagsáætlun<br /> (Sótt í reitinn **Kostnaði lokið %** í verkhlutalínum)<br /><br /> VÍV-sala = Samþykkt sala - Reikningshæft reikningsfært verð |Útreikningar á loknum prósentum samþykkja tekjur í hlutfalli byggt á loknum prósentum, þ.e. notkun (heildarkostnaði) á móti áætlunarkostnaði.<br /><br /> Skilyrði fyrir útreikningnum eru að reikningshæft heildarverð og heildarkostnaður á fjárhagsáætlun séu færð inn á réttan hátt fyrir allt verkið. |
| Samn. sem er lokið |VÍV-upphæð = VÍV-kostnaðarupphæð = Notkun (heildarkostnaður)<br /><br /> VÍV-söluupphæð = Reikningshæft (Reikningsfært verð) |Með valkostinum Samningi lokið eru tekjur og kostnaður ekki samþykkt fyrr en verkinu er lokið. Þetta getur verið æskilegt þegar mikil óvissa ríkir um áætlun kostnaðar og tekna verksins.<br /><br /> Öll notkun er bókuð í VÍV kostnaðarreikning (eign) og allar reikningsfærðar sölur eru bókaðar í VÍV reikning fyrir reikningsfærðar sölur (skuld) þar til verkinu er lokið. |

## <a name="see-also"></a>Sjá einnig .

[Verkefnastjórnun](projects-manage-projects.md)  
[Fjármál](finance.md)  
[Innkaup](purchasing-manage-purchasing.md)  
[Sala](sales-manage-sales.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
