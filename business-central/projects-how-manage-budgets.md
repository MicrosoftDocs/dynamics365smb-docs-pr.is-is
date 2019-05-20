---
title: Setja upp og stjórna fjárhagsáætlun fyrir verk| Microsoft Docs
description: Lýsir því hvernig skal áætla tilföng og spá fyrir um og stjórna kostnaði verks með því að setja upp fjárhagsáætlun fyrir hvert verk.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project budget, forecast
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: ba7cb69373cb9e311f6ef203edfff0d8e2150ea1
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/29/2019
ms.locfileid: "1253350"
---
# <a name="manage-job-budgets"></a>Umsjón fjárhagsáætlana fyrir eignir
Hægt er að setja upp áætlun fyrir hvert verk. Áætlunin er notuð til að áætla forðann sem hægt er að úthluta verki. Áætlunin getur verið almenns eðlis með fáeinum færslum eða með mörgum færslum sem skiptast í aðgerðastig. Svo er hægt að bera áætlaðar upphæðir saman við raunverulega notkun eins og hún birtist í verkbókinni. Með því að fylgjast með mismuni á milli raunnotkun og áætlaðri notkun er hægt að stýra yfirstandandi verkefni og auka gæði síðari verka með því að draga úr hættu á að kostnaður sé vanmetinn.

Eftirfarandi aðferð lýsir því hvernig á að meta áætlaðan kostnað við áætlun. Upplýsingar um skráningu áætlaðra- og raunverða verka og kostnað er að finna í [Skrá notkun fyrir verk](projects-how-record-job-usage.md).  

## <a name="JobBudgetCosts"></a> Til að áætlað kostnað verks
Þegar viðskiptavinur vill vita verð verks sem verður reikningsfært samkvæmt notkun þarf að ákvarða áætlaðan kostnað verksins. Síðan **Verð verkvara** er notuð til þess.

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Verk** og veldu síðan tengda tengilinn.  
2. Opnið viðeigandi verk.
3. Veljið verkhlutalínu af gerðinni Bókun og veljið svo aðgerðina **Verkáætlunarlínur**.
4. Fyllið í reitina eftir þörfum í nýrri línu. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]   

Fyrir reitinn **Línugerð** skal vísa til eftirfarandi upplýsinga.  

| Tegund línu | Lýsing |
| --- | --- |
| **Bæði fjárhagsáætlun og reikningshæft** |Upphæðir kostnaðar og verðs sem færðar eru í áætlunarlínuna eru áætlaður kostnaður þeirrar áætlunarlínu. Verðupphæðin verður reikningsfærð. |
| **Fjárhagsáætlun** |Viðskiptavinurinn er ekki rukkaður um notkun. notkunina er aldrei hægt að flytja á reikning en hún verður samt notuð í útreikningum VÍV. |
| **Reikningshæft** |Viðskiptavinurinn er rukkaður um notkun. Notkun er færð á reikninginn samkvæmt magninu sem tilgreint er í reitnum Magn til flutnings á reikning. |

> [!NOTE]  
> Reiturinn **Áætluð afhendingardagsetning** fyrir áætlunarlínuna inniheldur dagsetninguna þegar áætlað er að notkun tengd áætlunarlínunni verði lokið. Það er líka dagsetningin þegar hægt er að flytja áætlunarlínuna á sölureikning og bóka hana. <br /><br /> Á undirliggjandi verkhluta á síðunni **Verkspjald** innihalda reitirnir **Upphafsdagur** og **Lokadagur** gildi reitsins **Áætluð afhendingardagsetning** á elstu og nýjustu verkáætlunarlínum á tengdum síðum **Verkáætlunarlínur**.

> [!NOTE]  
>   Þegar þú fyllir í reitinn **Magn**, verða allar upplýsingar um heildarverð og heildarkostnað reiknaðar út og settar í áætlunarlínuna. Hægt er að breyta þeim hvenær sem er.

Á síðunni **Verkspjald** er nú hægt að skoða samantekt yfirlit yfir áætlaðan heildarkostnað, áætlað verð, reikningshæfan kostnað og reikningshæft verð fyrir hvert verk fyrir sig.

Upplýsingar um skráningu áætlaðra- og raunverða verka og kostnað er að finna í [Skrá notkun fyrir verk](projects-how-record-job-usage.md).

## <a name="see-also"></a>Sjá einnig
[Verkefnastjórnun](projects-manage-projects.md)  
[Fjármál](finance.md)  
[Innkaup](purchasing-manage-purchasing.md)         
[Sala](sales-manage-sales.md)      
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
