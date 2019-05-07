---
title: Hvernig á að birgðaskrá íhluti samkvæmt frálagi aðgerða | Microsoft Docs
description: Fyrir vörur sem hafa verið settar upp með afturvirkri birgðaskráningu er sjálfgefin virkni að reikna út og bóka notkun íhluta þegar stöðu útgefinnar framleiðslupöntunar er breytt í **Lokið**. Frekari upplýsingar eru í Birgðaskráningaraðferð.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 1198cb269e0864a6a8b45380d293c3d05290f269
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2019
ms.locfileid: "921124"
---
# <a name="flush-components-according-to-operation-output"></a>Birgðaskráning íhluta samkvæmt frálagi aðgerðar
Fyrir vörur sem hafa verið settar upp með afturvirkri birgðaskráningu er sjálfgefin virkni að reikna út og bóka notkun íhluta þegar stöðu útgefinnar framleiðslupöntunar er breytt í **Lokið**.  

Ef leiðartengilskótar eru einnig skilgreindir verður reiknað og bókað eftir hverja aðgerð og magnið sem var raunverulega notað í aðgerðinni bókað. Nánari upplýsingar eru í [Stofna leiðir](production-how-to-create-routings.md).  

Til dæmis ef framleiðslupöntun um að framleiða 800 metra krefst 8 kg af íhlut, og ef 200 metrar eru bókaðir sem frálag, bókast 2 kg sjálfkrafa sem notkun.  

Þessi aðgerð er gagnleg af eftirfarandi ástæðum:  

-   **Birgðir - Verðmæti** - Virðisfærslur fyrir frálag og notkun eru stofnaðar samhliða framleiðslupöntun í vinnslu. Án leiðartengilskóða munu birgðagildi hækka þar sem afköst eru bókuð og svo minnka síðar meir þegar gildi íhlutanotkunar er bókuð ásamt lokinni framleiðslupöntun.  
-   **Birgðir til ráðstöfunar** - með stöðugri notkunarbókun er betur uppfært hvort íhlutir eru til ráðstöfunar, sem er mikilvægt til að viðhalda innra jafnvægi á milli eftirspurnar og framboðs. Án leiðartengilskóta kunna aðrar eftirspurnir eftir íhlutnum að líta svo á að hann sé laus, svo framarlega sem hann bíður seinkaðrar notkunarbókunar.  
-   **Tímanleg** – þegar hægt er að sérstilla afurðir eftir beiðni viðskiptamanna er hægt að draga úr rýrnun með því að tryggja að breytingar á verkum og kerfisbreytingar eigi sér aðeins stað þegar þess þarf.  

Eftirfarandi ferli sýnir hvernig eigi að sameina afturvirka birgðaskráningu og kóta leiðartengils þannig að magnið sem er skráð fyrir hverja aðgerð sé í samræmi við raunverulegan frálag lokinna aðgerða.  

## <a name="to-flush-components-according-to-operation-output"></a>Til að birgðaskrá íhluti samkvæmt frálagi aðgerðar  
1.  Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Vörur** og veldu síðan tengda hlekkinn.  
2.  Veldu aðgerðina **Breyta**.  
3.  Á flýtiflipanum **Áfylling**, í reitnum **Birgðaskráningaraðferð**, skal velja **Framsenda**.  

    > [!NOTE]  
    >  Veljið **Tínsla + Áfram** ef íhluturinn er notaður í birgðageymslu sem er sett upp fyrir beinan frágang og tínslu.  

4.  Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **leiðir** og veldu síðan tengda tengilinn.  
5.  Skilgreina leiðartengilskóða fyrir hverja aðgerð sem notar íhlutinn. Nánari upplýsingar eru í [Stofna leiðir ](production-how-to-create-routings.md).  
6.  Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **framleiðsluuppskrift** og veldu síðan tengda tengilinn.  
7.  Skilgreina leiðartengilskóta úr hverju íhlutstilviki við aðgerðina þar sem hann er notaður.

    > [!IMPORTANT]  
    >  Íhluturinn verður að hafa leiðartengil við síðustu aðgerð leiðarinnar.  

## <a name="see-also"></a>Sjá einnig  
[Búa til framleiðsluuppskriftir](production-how-to-create-production-boms.md)  
[Uppsetning framleiðslu](production-configure-production-processes.md)  
[Framleiðsla](production-manage-manufacturing.md)    
[Áætlun](production-planning.md)   
[Birgðir](inventory-manage-inventory.md)  
[Innkaup](purchasing-manage-purchasing.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
