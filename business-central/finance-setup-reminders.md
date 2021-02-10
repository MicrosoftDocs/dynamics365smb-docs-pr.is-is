---
title: Setja upp skilmála og stig innheimtubréfa
description: Kynntu þér hvernig á að setja upp Business Central þannig að hægt sé að senda innheimtubréf til viðskiptamanns varðandi gjaldfallinnar greiðslu og bæta kostnaði eða þóknun við greiðsluna vegna tafarinnar.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment due, debt, overdue, fee, charge, reminder
ms.date: 01/21/2021
ms.author: edupont
ms.openlocfilehash: 1bef0a7598846f0ea3fe74b03bbef70bb5c940ef
ms.sourcegitcommit: adf1a87a677b8197c68bb28c44b7a58250d6fc51
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/21/2021
ms.locfileid: "5035382"
---
# <a name="set-up-reminder-terms-and-levels"></a>Setja upp skilmála og stig innheimtubréfa

Hægt er að nota áminningar til að minna viðskiptamenn á gjaldfallnar upphæðir. [!INCLUDE [reminder-terms](includes/reminder-terms.md)]

## <a name="reminder-terms"></a>Skilmálar innheimtubréfa

Ef viðskiptamenn eru í vanskilum verður að ákveða hvenær og hvernig eigi að senda þeim innheimtubréf. Auk þess gæti þurft að skuldfæra reikninga þeirra vegna vaxta eða þóknunar. Hægt er að setja upp eins marga skilmála innheimtubréfa og hver vill.  

> [!NOTE]
> Eigi að reikna vexti á greiðslur sem fallnar eru í gjalddaga er hægt að gera það þegar áminningar eru stofnaðar. En ef aðeins á að reikna vexti og láta viðskiptamenn vita án þess að senda áminningar er hægt að nota [vaxtareikninga](finance-setup-finance-charges.md). Frekari upplýsingar eru í [Innheimtubréf](receivables-collect-outstanding-balances.md#reminders) eða [Vextir](receivables-collect-outstanding-balances.md#finance-charges).

### <a name="to-set-up-reminder-terms"></a>Skilmálar innheimtubréfs settir upp

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Skilmálar innheimtubréfa** og veldu síðan tengda tengilinn.  
2. Fyllið inn í reitina eftir þörfum. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]  
3. Eigi að nota fleiri en eina samsetningu áminninga þarf að setja upp kóta fyrir hverja þeirra.

## <a name="reminder-levels"></a>Stig innheimtubréfa

Fyrir hvern áminningarskilmálakóta er hægt að skilgreina ótakmarkaðan fjölda áminningarstiga. Í fyrsta sinn sem áminning er stofnuð fyrir viðskiptamann er uppsetning stigs 1 notuð. Þegar áminningin er send er númer stigsins skráð á áminningarfærslurnar sem stofnast og tengt við einstakar viðskiptamannafærslur. Þurfi að minna viðskiptamanninn á aftur eru allar áminningarfærslur tengdar opnum viðskiptamannafærslum kannaðar til að finna hæsta stigsnúmerið. Skilyrði næsta stigsnúmers verða síðan notuð í nýju áminningunni.

Ef stofnaðar eru fleiri áminningar en skilgreind hafa verið stig fyrir verða skilyrði hæsta stigsins notuð. Hægt er að stofna eins margar áminningar og leyft er í reitnum **Hám.fj. innheimtubréfa** í áminningarskilmálunum.

### <a name="to-set-up-reminder-levels"></a>Stig innheimtubréfa sett upp

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Skilmálar innheimtubréfa** og veldu síðan tengda tengilinn.  
2. Á síðunni **Skilmálar innheimtubréfa** er valin lína með skilmálum sem setja á upp stig fyrir og síðan er valin aðgerðin **Stig**.  
3. Fyllið inn reitina eftir þörfum. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]  

    > [!TIP]
    > Stilling reitsins **Reikna út vexti** ákvarðar hvort vextir verði á innheimtubréfinu þegar það er gefið út. Reiturinn **Bóka vexti** á síðunni **Skilmálar innheimtubréfa** ákvarðar hinsvegar hvort bóka verði reiknaða vexti í fjárhag og viðskiptavinalykla.
    >
    > Til að gefa til kynna að reikna eigi vexti skal velja reitinn **Reikna út vexti**.

    Fyrir hvert stig innheimtubréfa má tilgreina viðbótargjöld í bæði fjárhag og í erlendum gjaldmiðli. Hægt er að skilgreina mörg viðbótargjöld í erlendum gjaldmiðlum fyrir hvern kóða á síðunni **Stig innheimtubréfa**.  

    Hægt er að reikna viðbótargjöldin á þrjár mismunandi vegu sem eru skilgreindar með gildinu í reitnum **Reiknigerð viðbótargjalds**.  

    - **Fast**

        Gjöld eru reiknuð út frá gildunum í reitunum **Viðbótargjald** í línunni fyrir sjálft stig innheimtubréfsins.  
    - **Ein gagnvirkni**

        Gjöld eru reiknuð út frá gildunum í reitunum í viðeigandi línu á síðunni **Uppsetning viðbótargjalds** fyrir það stig innheimtubréfsins.
    - **Uppsöfnuð gagnvirkni**

        Gjöld eru reiknuð út frá gildunum í reitunum í sameinuðum línum á síðunni **Uppsetning viðbótargjalds** fyrir það stig innheimtubréfsins.

4. Velja aðgerðina **gjaldmiðlar**.
5. Á síðunni **Gjaldmiðlar fyrir stig innheimtubréfa** skal skilgreina gjaldmiðlakóða og viðbótargjald fyrir hvern kóða stigs innheimtubréfa og samsvarandi númer stigs innheimtubréfa.

    > [!NOTE]  
    > Þegar innheimtubréf eru stofnuð í erlendum gjaldmiðli tekur kerfið mið af þeim skilyrðum sem sett eru um erlendan gjaldmiðil hér til að stofna innheimtubréf. Ef engin vaxtaskilyrði innheimtubréfa fyrir erlenda gjaldmiðla eru sett upp notar kerfið SGM-vaxtaskilyrðin sem sett voru upp á síðunni **Stig innheimtubréfs** og breytir þeim í viðeigandi gjaldmiðil.

    Fyrir hvert áminningarstig er hægt að skilgreina texta sem verður prentaður á undan (**Byrjunartexti**) eða eftir (**Lokatexti**) færslunum í áminningunni.

6. Veljið **Byrjunartexti** eða **Lokatexti** aðgerðirnar eftir því sem við á, og fyllið í **Áminningartexti** síðuna.
7. Til að setja viðeigandi gildi sjálfvirkt inn í innheimtubréfstexta, skal fara inn í eftirfarandi staðgengla í reitnum **Texti**.  

    |Frátaka|Gildi:|  
    |-----------------|-----------|  
    |%1|Innihald reitsins **Dagsetning skjals** á innheimtubréfshausnum|  
    |%2|Innihald reitsins **Gjalddagi** á innheimtubréfshausnum|  
    |%3|Innihald reitsins **Vextir** í viðeigandi vaxtaskilmálum|  
    |%4|Innihald reitsins **Eftirstöðvar** á innheimtubréfshausnum|  
    |%5|Innihald reitsins **Vaxtaupphæð** á innheimtubréfshausnum|  
    |%6|Innihald reitsins **Viðbótargreiðsla** á innheimtubréfshausnum|  
    |%7|Heildarupphæð innheimtubréfsins|  
    |%8|Innihald reitsins **Stig innheimtu** á innheimtubréfshausnum|  
    |%9|Innihald reitsins **Kóði gjaldmiðils** á innheimtubréfshausnum|  
    |%10|Innihald reitsins **Bókunardagsetning** á innheimtubréfshausnum.|  
    |%11|Nafn fyrirtækis|  
    |%12|Innihald reitsins **Viðbótargjald fyrir hverja línu** á innheimtubréfshausnum.|  

    Til dæmis, ef þú skrifar **Þú skuldar %9 %7 á gjalddaga %2.** mun innheimtubréfið innihalda eftirfarandi texta: **Þú skuldar 1.200,50 USD á gjalddaga 02-02-2014.**.

    > [!NOTE]
    > Gjalddaginn er reiknaður samkvæmt dagsetningarreiknireglunni sem var slegin inn. Frekari upplýsingar er að finna í [Að nota dagsetningarreiknireglur](ui-enter-date-ranges.md#using-date-formulas).

Þegar búið er að setja upp áminningarskilmálana með viðbótarstigum og texta þarf að færa einn kóðann á hvert viðskiptamannaspjald. Frekari upplýsingar eru í [Skrá nýja viðskiptamenn](sales-how-register-new-customers.md).  

## <a name="see-also"></a>Sjá einnig .

[Innheimta útistandandi skuldir](receivables-collect-outstanding-balances.md)  
[Setja upp vaxtaskilmála](finance-setup-finance-charges.md)  
[Uppsetning Fjármála](finance-setup-finance.md)  
