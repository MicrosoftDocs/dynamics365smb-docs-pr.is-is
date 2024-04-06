---
title: Setja upp skilmála og stig innheimtubréfa
description: Kynntu þér hvernig á að setja upp Business Central þannig að hægt sé að senda innheimtubréf til viðskiptamanns varðandi gjaldfallinnar greiðslu og bæta kostnaði eða þóknun við greiðsluna vegna tafarinnar.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'payment due, debt, overdue, fee, charge, reminder'
ms.search.form: '431, 432, 436, 478'
ms.date: 03/12/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="set-up-reminder-terms-and-levels"></a>Setja upp skilmála og stig innheimtubréfa

Hægt er að nota áminningar til að minna viðskiptamenn á gjaldfallnar upphæðir og biðja um greiðslu. [!INCLUDE [reminder-terms](includes/reminder-terms.md)]

> [!TIP]
> Þegar áminningarskilmálar og stig hafa verið sett upp er hægt að taka þá með í sjálfvirkum ferlum til að stofna, gefa út og senda áminningar. Nánari upplýsingar um sjálfvirka ferlið eru fara í [Innheimtubréf sjálfvirkt í söfnum](finance-automate-reminders.md).

## <a name="reminder-terms"></a>Skilmálar innheimtubréfa

Ef viðskiptamenn eru í vanskilum verður að ákveða hvenær og hvernig eigi að senda þeim innheimtubréf. Auk þess gæti þurft að skuldfæra reikninga þeirra vegna vaxta eða þóknunar. Hægt er að setja upp eins marga skilmála innheimtubréfa og hver vill.  

> [!NOTE]
> Eigi að reikna vexti á greiðslur sem fallnar eru í gjalddaga er hægt að gera það þegar áminningar eru stofnaðar. Eigi hinsvegar bara að reikna vexti og láta viðskiptamenn vita án þess að senda innheimtubréf er vaxtareikningur [notaður](finance-setup-finance-charges.md). Nánari upplýsingar eru [í Áminning](receivables-collect-outstanding-balances.md#reminders) eða [Vaxtagjöld](receivables-collect-outstanding-balances.md#finance-charges).

### <a name="set-up-attachment-and-email-body-texts-for-communications"></a>Setja upp viðhengi og texta meginmáls tölvupósts fyrir samskipti

Á síðunni **Uppsetning** áminningarskilmála er hægt að setja upp viðhengi og stöðluð tölvupóstskeyti til að nota annaðhvort fyrir öll áminningarstig eða búa til sérstök skilaboð fyrir hvert stig. Til dæmis gætu skilaboðin sem send eru fyrir fyrsta stig innheimtubréfs haft annan tón eða efni en hinn eða þriðji. Til að búa til viðhengi og texta í tölvupósti á öllum stigum skal velja **Samskipti** viðskiptavina efst á síðunni. Til að stofna skilaboð fyrir tilteknar línur skal á flýtiflipanum **Stig** innheimtubréfs velja línu og velja svo aðgerðina **Samskipti** viðskm. á flýtiflipanum.

Sjálfgefið er að viðhengi og texti í tölvupósti noti tungumálastillingarnar þínar. Ef áminningar eru sendar til viðskiptamanna í öðrum löndum gæti hins vegar þurft að hafa samskipti á mismunandi tungumálum. Hægt er að búa til texta fyrir hvert tungumál sem [!INCLUDE [prod_short](includes/prod_short.md)] styður með því að nota **Bæta við texta fyrir aðgerðina Bæta við tungumáli** . Ef það er gert skal tryggja að tungumálin séu eins fyrir viðhengi og texta í tölvupósti. Ef þau stemma ekki og áminningarskilmálarnir eru fleiri en eitt stig getur verið að sjálfvirknin geti ekki sérsniðið skeytið fyrir eitt eða fleiri stig. Til að staðfesta að tungumálin samsvari skal nota aðgerðina **Yfirlitssamskipti** og bera saman samskipti fyrir textann.

Þegar tölvupóstur er sendur er áminningin skýrsla sem hengd er við tölvupóstinn. Skýrslan sem myndar innheimtubréfið er skilgreind á síðunni **Skýrsluval innheimtubréfs/Vaxtareikningur** þar sem einnig er valin skýrsla sem inniheldur meginmálstexta tölvupóstsins í reitnum **Heiti** líkamsuppsetningar tölvupósts. Þegar þú sendir viðskiptamönnum tölvupóst er textinn á flýtiflipanum **Texti** tölvupósts settur inn í skýrsluna sem valin var í reitnum **Heiti** líkamsuppsetningar tölvupósts. Staðlaða skýrslan er með textareit fyrir þennan texta. Hægt er að breyta skýrslunni til dæmis til að bæta við eða fjarlægja efni. Breyta útliti þessara skýrslna á síðunni **Skýrsluútlit** . Nánari upplýsingar um útlit skýrslu fást með því að [fara í Hefja stofnun skýrsluútlits](ui-get-started-layouts.md).

> [!NOTE]
> Samskipti með tölvupósti beint frá [!INCLUDE [prod_short](includes/prod_short.md)] krefst þess að þú sért settur upp til þess. Til að fá nánari upplýsingar um tengingu tölvupóstreikninga við [!INCLUDE [prod_short](includes/prod_short.md)] skaltu fara í [Setja upp tölvupóst](admin-how-setup-email.md).

### <a name="set-up-reminder-terms"></a>Setja upp áminningarskilmála

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Skilmálar innheimtubréfa** og velja síðan viðkomandi tengil.  
2. Fyllið inn í reitina eftir þörfum. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]  
3. Eigi að nota fleiri en eina samsetningu áminninga þarf að setja upp kóta fyrir hverja þeirra.

## <a name="reminder-levels"></a>Stig innheimtubréfa

Fyrir hvert áminningartímabil er hægt að skilgreina ótakmarkaðan fjölda áminningarstiga þó að flest fyrirtæki noti aðeins tvö eða þrjú stig. Í fyrsta sinn sem áminning er stofnuð fyrir viðskiptamann er uppsetning stigs 1 notuð. Þegar áminningin er send er númer stigsins skráð á áminningarfærslurnar sem stofnast og tengt við einstakar viðskiptamannafærslur. Þurfi að minna viðskiptamanninn á aftur eru allar áminningarfærslur tengdar opnum viðskiptamannafærslum kannaðar til að finna hæsta stigsnúmerið. Skilyrði næsta stigsnúmers verða síðan notuð í nýju áminningunni.

Ef stofnaðar eru fleiri áminningar en skilgreind hafa verið stig fyrir verða skilyrði hæsta stigsins notuð. Hægt er að stofna eins margar áminningar og leyft er í reitnum **Hám.fj. innheimtubréfa** í áminningarskilmálunum.

### <a name="to-set-up-reminder-levels"></a>Stig innheimtubréfa sett upp

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Skilmálar innheimtubréfa** og velja síðan viðkomandi tengil.  
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
7. Hægt er að færa inn tengd gildi sjálfkrafa í texta innheimtubréfs með því að færa inn eftirfarandi frátakara í reitinn **Texti** .  

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

    Ef notandi skrifar **skuldir %9 %7 á %2** gjalddaga er eftirfarandi texti í innheimtubréfinu: **Það er skuldað USD 1.200,50 gjalddaga á 02-02-2024.**.

    > [!NOTE]
    > [!INCLUDE [prod_short](includes/prod_short.md)] reiknar gjalddaga samkvæmt dagsetningarreiknireglunni sem færð er inn. Frekari upplýsingar eru í [Nota dagsetningarformúlur](ui-enter-date-ranges.md#use-date-formulas).

8. Til að tilgreina tungumál fyrir tölvupóstskeyti skal velja **Bæta við texta fyrir aðgerð á tungumáli** . Reiturinn **Tungumálskóti** uppfærist þannig að valið sé. Á flýtiflipanum **Texti** tölvupósts er ritað efni skeytisins á völdu tungumáli.

Þegar skilmálar innheimtubréfa hafa verið settir upp er hægt að úthluta þeim til viðskiptamanna á síðum viðskiptamannaspjalda. Frekari upplýsingar eru í [Skrá nýja viðskiptamenn](sales-how-register-new-customers.md).  

## <a name="see-also"></a>Sjá einnig .

[Innheimta útistandandi skuldir](receivables-collect-outstanding-balances.md)  
[Senda innheimtubréf vegna útistandandi stöðu](receivables-send-reminders.md)  
[Setja upp vaxtaskilmála](finance-setup-finance-charges.md)  
[Uppsetning Fjármála](finance-setup-finance.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
