---
title: Setja upp og stjórna áætlun fyrir verk
description: Lýsir því hvernig á að áætla forða og spá og stýra kostnaði verks með því að setja upp áætlun fyrir hvert verk.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: conceptual
ms.search.keywords: 'project budget, forecast'
ms.search.form: '1002, 1007'
ms.date: 02/22/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# Unnið með verkáætlanir

Hægt er að setja upp áætlun fyrir hvert verk. Áætlunin er notuð til að áætla forðann sem úthlutað er til verks. Áætlunin getur verið almenns eðlis með fáeinum færslum eða með mörgum færslum sem skiptast í aðgerðastig. Síðan er hægt að bera áætlaðar upphæðir saman við raunverulega notkun eins og hún er skráð í verkbókina. Með því að fylgjast með mismuni á milli raunverulegrar notkunar og áætlaðrar notkunar er hægt að stýra yfirstandandi verkefni og bæta gæði verkefna í framtíðinni með því að draga úr hættu á að kostnaður sé vanmetinn.

Eftirfarandi aðferð lýsir því hvernig á að meta áætlaðan kostnað við áætlun. Upplýsingar um skráningu áætlaðs samanborið við raunverulegt verð og kostnað verks eru [í Skrá notkun fyrir verkefni](projects-how-record-job-usage.md).  

## <a name="JobBudgetCosts"></a> Áætlaður kostnaður vegna verks áætlaður

Þegar viðskiptavinur vill vita verð verks sem verður reikningsfært samkvæmt notkun verður að ákvarða áætlaðan kostnað fyrir verkið. Nota skal síðuna **Verkhlutalínur** verkefnis til þess.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, slá inn **Verkefni** og velja síðan viðeigandi tengil.  
2. Viðeigandi verkefni er opnað.
3. Veljið verkhlutalínu af gerðinni Bókun og veljið svo aðgerðina Áætlunarlínur **verkefnis** .
4. Fyllið í reitina eftir þörfum í nýrri línu. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

Fyrir reitinn **Línugerð** skal vísa til eftirfarandi upplýsinga.  

| Tegund línu | Lýsing |
| --- | --- |
| **Bæði fjárhagsáætlun og reikningshæft** |Upphæðir kostnaðar og verðs sem færðar eru í áætlunarlínuna eru áætlaður kostnaður þeirrar áætlunarlínu. Verðupphæðin verður reikningsfærð. |
| **Fjárhagsáætlun** |Viðskiptavinurinn er ekki rukkaður um notkun. Notkun flyst ekki á reikning heldur er notuð til að reikna VÍV. |
| **Reikningshæft** |Viðskiptavinurinn er rukkaður um notkun. Notkun flyst á reikninginn samkvæmt magninu sem tilgreint er í reitnum **Magn til flutnings á reikning** . |

> [!NOTE]  
> Reiturinn **Áætluð afhendingardagsetning** fyrir áætlunarlínuna inniheldur dagsetninguna þegar áætlað er að notkun tengd áætlunarlínunni verði lokið. Það er líka dagsetningin þegar hægt er að flytja áætlunarlínuna á sölureikning og bóka hana. <br /><br /> Á undirliggjandi verkhluta á síðunni **Verkspjald** innihalda reitirnir **Upphafsdagsetning** og **Lokadagsetning** gildi reitsins **Áætluð afgreiðsludagsetning** á fyrstu og síðustu áætlunarlínum verksins á tengdu **verkáætlunarlínunum** .

> [!NOTE]  
> Þegar þú fyllir í reitinn **Magn**, verða allar upplýsingar um heildarverð og heildarkostnað reiknaðar út og settar í áætlunarlínuna. Hægt er að breyta þeim hvenær sem er.

Á síðunni **Verkspjald** má nú sjá yfirlit yfir áætlaðan heildarkostnað, áætlað verð, reikningshæfan kostnað og reikningshæft verð fyrir hvert verk.

Upplýsingar um skráningu áætlaðs samanborið við raunverulegt verð og kostnað verks eru [í Skrá notkun fyrir verkefni](projects-how-record-job-usage.md).

## Sjá einnig .

[Verkefnastjórnun](projects-manage-projects.md)  
[Fjármál](finance.md)  
[Innkaup](purchasing-manage-purchasing.md)  
[Sala](sales-manage-sales.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
