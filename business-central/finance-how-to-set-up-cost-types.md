---
title: Hvernig á að setja upp myndrit yfir kostnaðartegundir | Microsoft Docs
description: Myndrit kostnaðartegunda eru svipuð bókhaldslyklum í fjárhag.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: cost types, general ledger, accounts
ms.date: 04/01/2019
ms.author: sgroespe
redirect_url: finance-set-up-cost-accounting
ms.openlocfilehash: e0bf6a8c7595155785949ed51c765fef0524173b
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/29/2019
ms.locfileid: "1240488"
---
# <a name="set-up-cost-types"></a>Uppsetning kostnaðargerða
Myndrit kostnaðartegunda eru svipuð bókhaldslyklum í fjárhag. Hægt er að setja upp myndritið yfir kostnaðartegundir á eftirfarandi hátt:  

-   Skipulag kostnaðargerða milli fyrirtækja svipað og á reikningum rekstrarreiknings á fjárhagsbókhaldslyklinum. Síðan er hægt að flytja bókhaldslykil fjárhags yfir í kostnaðargerðir. Hægt er að gera allar nauðsynlegar leiðréttingar eftir flutninginn.  
-   Stofna nýja kostnaðartegund eða bæta nýjum kostnaðartegundum við fyrirliggjandi kostnaðartegund. Stofna þarf hverja nýja kostnaðartegund sérstaklega.  

## <a name="to-transfer-the-general-ledger-chart-of-accounts-to-the-chart-of-cost-types"></a>Til að flytja bókhaldslykil fjárhags yfir í kostnaðargerðir.  
1.  Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Myndrit yfir kostnaðargerðir** og veldu síðan tengda tengilinn.  
2.  Velja skal aðgerðina **Sækja kostnaðargerðir úr bókhaldslykli**. Í svarglugganum er valið hnappinn **Já** til að staðfesta flutninginn. Aðgerðin notar bókhaldslykla til að stofna myndrit af kostnaðartegundum.  

    Myndrit kostnaðargerða inniheldur nú alla rekstrarreikninga í fjárhag og inniheldur fyrirsagnir og samtölur. Hægt er að breyta myndriti yfir kostnaðartegundir, eftir þörfum. Til dæmis er hægt að eyða tvíteknum fyrirliggjandi kostnaðartegundum.  

    > [!IMPORTANT]  
    >  Aðgerðin **Skrá kostnaðargerðir í bókhaldslyklinum** uppfærir samband milli bókhaldslykils og bókhaldslykils fyrir kostnaðartegundir. **númer**  svæðið er fyllt og staðfest til að tryggja að hver almennur fjárhagsreikningur tengist aðeins einni tegund kostnaðar. Aðgerðin keyrir sjálfkrafa áður en fjárhagsfærslur eru færðar í kostnaðarbókhald.  

## <a name="to-set-up-new-cost-types-in-the-chart-of-cost-types-page"></a>Til að setja upp nýjar kostnaðargerðir á síðunni Myndrit fyrir kostnaðargerðir  
1.  Opnaðu síðuna **Myndrit yfir kostnaðargerðir** í breytingarstillingu.  
2.  Fyllið inn í reitina eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
    >  Hægt er að setja upp og viðhalda kostnaðargerðum á síðunni **Kostnaðargerð spjald** eða á síðunni **Myndrit yfir kostnaðargerðir**. Í þessu ferli eru settar upp kostnaðartegundir á síðunni **Myndrit yfir kostnaðargerðir**.

3.  Þegar búið er að stofna öll kostnaðargerðir, skal velja aðgerðina **Draga inn kostnaðargerðir**. Í svarglugganum, veljið hnappinn **Já**.  
4.  Tengja nýju tegund kostnaðar í samsvarandi almennan fjárhagslykil.  

    > [!IMPORTANT]  
    >  Ef skilgreiningar hafa verið færðar í **Samtala** reitina fyrir línutegundina **Loka-upphæð** áður en aðgerðin **Inndráttur kostnaðargerða** er framkvæmd þarf að færa skilgreiningarnar inn aftur því að aðgerðin skrifar yfir gildin í öllum **Loka-Upphæð**-reitum.  

## <a name="to-update-cost-types"></a>Til að uppfæra kostnaðargerðir  
1.  Á síðunni **Uppsetning kostnaðarbókhalds** skal velja hvort uppfæra eigi myndrit yfir kostnaðartegundir sjálfkrafa þegar bókhaldslykillinn breytist.  
2.  Í reitnum **Stilla fjárhagsreikning** er hægt að velja úr eftirfarandi valkostum.  

- **Engin jöfnun** - Það er engin samsvarandi breyting á kostnaðartegundum þegar bókhaldslyklinum er breytt.  
- **Sjálfvirkt** - Samsvarandi breyting er gerð á kostnaðartegundalyklinum þegar bókhaldslyklinum er breytt.  
- **Kvaðning** - Skilaboð birtast þar sem spurt er hvort gera eigi samsvarandi breytingu á myndriti kostnaðartegunda þegar bókhaldslykli er breytt.  

## <a name="see-also"></a>Sjá einnig  
[Kostnaðarreikningur](finance-manage-cost-accounting.md)  
[Skilgreining kostnaðarstaði og kostnaðarhluti fyrir bókhaldslykil](finance-defining-cost-centers-and-cost-objects-for-chart-of-accounts.md)   
[Stöður milli kostnaðartegundar, kostnaðarstaðar og kostnaðarliðar](finance-balances-between-cost-type-cost-center-and-cost-object.md)   
[Uppsetning kostnaðarbókhalds](finance-set-up-cost-accounting.md)   
[Orðalisti í kostnaðarbókhaldi](finance-terminology-in-cost-accounting.md)   
[Um kostnaðarbókhald](finance-about-cost-accounting.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
