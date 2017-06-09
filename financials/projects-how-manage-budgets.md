---
title: "Hvernig á að: Stjórna verkáætlunum | Microsoft Docs"
description: "Lýsir hvernig á að stofna fjárhagsáætlun fyrir verk."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project budget, forecast
ms.date: 03/28/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 9a351b581e0312d21b04db43a85243b8a5afb0e3
ms.contentlocale: is-is
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-manage-job-budgets"></a>Hvernig á að: Vinna með verkáætlanir
Hægt er að setja upp áætlun fyrir hvert verk. Áætlunin er notuð til að áætla forðann sem hægt er að úthluta verki. Áætlunin getur verið almenns eðlis með fáeinum færslum eða með mörgum færslum sem skiptast í aðgerðastig. Svo er hægt að bera áætlaðar upphæðir saman við raunverulega notkun eins og hún birtist í verkbókinni. Með því að fylgjast með mismuni á milli raunnotkun og áætlaðri notkun er hægt að stýra yfirstandandi verkefni og auka gæði síðari verka með því að draga úr hættu á að kostnaður sé vanmetinn.

Eftirfarandi aðferð lýsir því hvernig á að meta áætlaðan kostnað við áætlun. Upplýsingar um skráningu áætlunar samanborið við raunverulegt verð og kostnað verks má sjá í [Hvernig á að: Skrá notkun vegna verka](projects-how-record-job-usage.md).  

## <a name="JobBudgetCosts"></a> Til að áætlað kostnað verks
Þegar viðskiptavinur vill vita verð verks sem verður reikningsfært samkvæmt notkun þarf að ákvarða áætlaðan kostnað verksins. Glugginn **Verkhlutalínur** er notaður til þess.

1. Efst í hægra horni skal velja reitinn **Leita að síðu eða skýrslu** táknið ![Leita að síðu eða skýrslu](media/ui-search/search_small.png "Leita að síðu eða skýrslu táknið"), færa **Verk**, og velja síðan viðeigandi tengil.  
2. Opnið viðeigandi verk.
3. Veljið verkhlutalínu af gerðinni Bókun og veljið svo aðgerðina **Verkáætlunarlínur**.
4. Fyllið í reitina eftir þörfum í nýrri línu. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]   

Fyrir reitinn **Línugerð** skal vísa til eftirfarandi upplýsinga.  

| Tegund línu | Lýsing |
| --- | --- |
| **Bæði fjárhagsáætlun og reikningshæft** |Upphæðir kostnaðar og verðs sem færðar eru í áætlunarlínuna eru áætlaður kostnaður þeirrar áætlunarlínu. Verðupphæðin verður reikningsfærð. |
| **Fjárhagsáætlun** |Viðskiptavinurinn er ekki rukkaður um notkun. notkunina er aldrei hægt að flytja á reikning en hún verður samt notuð í útreikningum VÍV. |
| **Reikningshæft** |Viðskiptavinurinn er rukkaður um notkun. Notkun er færð á reikninginn samkvæmt magninu sem tilgreint er í reitnum Magn til flutnings á reikning. |

**Til athugunar**: Reiturinn**Áætlunardagsetning** fyrir áætlunarlínuna inniheldur dagsetninguna þegar búist er við að notkun sem tengist áætlunarlínunni ljúki. Það er líka dagsetningin þegar hægt er að flytja áætlunarlínuna á sölureikning og bóka hana.  

**Til athugunar**: Þegar reiturinn **Magn** er fylltur út eru upplýsingar um heildarverð og heildarkostnað reiknaðar út og fylltar inn fyrir viðeigandi áætlunarlínu. Hægt er að breyta þeim hvenær sem er.

Í glugganum **Verkspjald** er nú hægt að sjá yfirlit yfir samanlagðan áætlaðan kostnað, áætlað verð, reikningshæfan kostnað og reikningshæft verð fyrir hvert verk.

Upplýsingar um skráningu áætlunar samanborið við raunverulegt verð og kostnað verks má sjá í [Hvernig á að: Skrá notkun vegna verka](projects-how-record-job-usage.md).

## <a name="see-also"></a>Sjá einnig
[Verkefnastjórnun](projects-manage-projects.md)  
[Fjármál](finance.md)  
[Innkaup](purchasing-manage-purchasing.md)         
[Sala](sales-manage-sales.md)      
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

