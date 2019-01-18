---
title: "Senda viðskiptamönnum innheimtubréf eða sekt vegna gjaldfallinna greiðslna| Microsoft Docs"
description: "Lýsir því hvernig skal senda innheimtubréf til viðskiptamanns varðandi gjaldfallinnar greiðslu og bæta kostnaði eða þóknun við greiðsluna vegna tafarinnar."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment due, debt, overdue, fee, charge, reminder
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: 3dfc2d9edbb72de196238748ab90ce8dd4990adb
ms.contentlocale: is-is
ms.lasthandoff: 11/26/2018

---
# <a name="collect-outstanding-balances"></a>Innheimta útistandandi skuldir
Í stjórnun útistandandi skulda felst að kanna hvort upphæðir sem falla í gjalddaga eru greiddar tímanlega. Ef viðskiptamenn eru í vanskilum geturðu sent yfirlitsskýrslu Viðskiptamanns sem innheimtubréf. Þú getur einnig gefið út innheimtubréf.

Hægt er að nota áminningar til að minna viðskiptamenn á gjaldfallnar upphæðir. Einnig er hægt að nota áminningar til að reikna út vexti og annan kostnað og hafa þær upplýsingar með í áminningunni. Notaðir eru vaxtareikningar ef krefja á viðskiptamenn um vexti eða gjöld án þess að minna þá á gjaldfallnar upphæðir.

## <a name="reminders"></a>Innheimtubréf
Áður en hægt er að stofna áminningar þarf að setja upp skilmála áminninga og tengja þá við viðskiptamenn. Fyrir hvern áminningarskilmála þarf að skilgreina áminningarstig. Hvert áminningarstig inniheldur reglur um það hvenær áminningin verður send, t.d. hversu mörgum dögum eftir gjalddaga reikningsins eða dagsetningu fyrri áminningar. Innihald síðunnar **Vaxtaskilmálar** ákveður hvort vextir eru reiknaðir í áminningunni.  

Hægt er að keyra reglulega keyrsluna **Stofna innheimtubréf** til að stofna áminningar fyrir alla viðskiptamenn með gjaldfallnar skuldir eða stofna áminningu handvirkt fyrir einstaka viðskiptamenn og láta reikna línurnar og fylla þær út sjálfvirkt.  

Þegar búið er að stofna áminningarnar er hægt að breyta þeim. Textinn sem birtist í upphafi og í lok áminningar ræðst af áminningarstiginu og hægt er að sjá hann í dálknum **Lýsing**. Ef reiknuð upphæð hefur verið sett inn sjálfvirkt í upphafs- eða lokatextann verður textinn ekki leiðréttur ef línunum er eytt. Þá verður að nota aðgerðina **Uppfæra áminningu**.  

Viðskiptamannsfærsla með reitinn **Bið** útfylltan leyfir ekki stofnun áminningar. En ef áminning er stofnuð á grunni annarrar færslu verður gjaldfallin færsla merkt í bið einnig höfð með í áminningunni. Vextir eru ekki reiknaðir á línur með þessum færslum.

Þegar búið er að stofna áminningar, og breyta þeim ef þarf, er hægt að prenta prufuskýrslur eða senda áminningarnar, vanalega sem tölvupóst.

## <a name="finance-charges"></a>Vextir
Þegar viðskiptamaður greiðir ekki á gjalddaga er hægt að láta reikna út vexti sjálfvirkt og bæta þeim við gjaldföllnu upphæðina á reikningi viðskiptamannsins. Hægt er að láta viðskiptamenn vita af viðbótargjöldunum með því að senda vaxtareikninga.  

> [!NOTE]  
> Vaxtareikningar eru notaðir til að reikna út vexti og annan kostnað og til að láta viðskiptamenn vita um þann kostnað án þess að minna þá á gjaldfallnar upphæðir. Einnig er hægt að reikna vexti á gjaldfallnar upphæðir þegar áminningar eru stofnaðar.  

Hægt er að stofna vaxtareikning fyrir einstakan viðskiptamann og fylla línurnar út sjálfvirkt. Einnig er hægt að nota vinnsluna **Stofna vaxtareikninga** til að stofna vaxtareikninga fyrir alla eða valda viðskiptamenn með gjaldfallna stöðu.  

Þegar búið er að stofna vaxtareikninga er hægt að breyta þeim. Textinn sem birtist í upphafi og í lok vaxtareiknings ræðst af vaxtaskilmálunum og hægt er að sjá hann dálknum **Lýsing** í línunum. Ef reiknuð upphæð hefur verið sett inn sjálfvirkt í upphafs- eða lokatextann verður textinn ekki leiðréttur ef línunum er eytt. Þá verður að nota aðgerðina **Uppfæra vaxtatexta**.  

Þegar búið er að stofna vaxtareikninga, og breyta þeim ef þarf, er hægt að prenta prufuskýrslur eða senda vaxtareikningana, vanalega sem tölvupóst.

## <a name="multiple-interest-rates"></a>Margir vextir
Þegar vaxtaskilmálar og skilmálar innheimtubréfa eru sett upp, fyrir sekt vegna seinkunar á greiðslu, er hægt að tilgreina marga vexti þannig að sektargreiðsla er reiknuð út frá mismunandi vöxtum á mismunandi tímabilum. Ef margir vextir eru ekki settir upp, þá verða vextirnir og tímabilið sem er skilgreint á síðunum **Vaxtaskilmálar** og **Skilmálar innheimtubréfa** notað fyrir allt reikningstímabilið. Frekari upplýsingar eru í [Setja upp marga vexti](finance-how-to-set-up-multiple-interest-rates.md).  

## <a name="to-send-the-customer-statement-report"></a>Til að senda yfirlitsskýrslu viðskiptamanns
1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Yfirlit viðskiptamanns** og veldu síðan tengda tengilinn.
2. Fyllið inn í svæðin eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Undir **úttaksvalkostir**, skal velja hvernig eigi að senda skýrslunnar til viðskiptamanns.

> [!NOTE]  
>   Ef mörgum gjaldmiðlum ef verið að nota, er yfirlitsskýrslu Viðskiptamanns alltaf prentuð í gjaldmiðil viðskiptamannsins. Síðustu dagsetningunni í í yfirlitstímabili er einnig notuð sem yfirlitsdagsetning og dagsetning fyrir aldursgreiningu, ef aldursgreining er höfð með.

## <a name="to-set-up-reminder-terms"></a>Skilmálar innheimtubréfs settir upp
Ef viðskiptamenn eru í vanskilum verður að ákveða hvenær og hvernig eigi að senda þeim innheimtubréf. Auk þess gæti þurft að skuldfæra reikninga þeirra vegna vaxta eða þóknunar. Hægt er að setja upp eins marga skilmála innheimtubréfa og hver vill. Fyrir hvern áminningarskilmálakóta er hægt að skilgreina ótakmarkaðan fjölda áminningarstiga.

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Skilmálar innheimtubréfa** og veldu síðan tengda tengilinn.  
2. Fyllið inn í reitina eftir þörfum.  
3. Eigi að nota fleiri en eina samsetningu áminninga þarf að setja upp kóta fyrir hverja þeirra.

## <a name="to-set-up-reminder-levels"></a>Stig innheimtubréfa sett upp
Í fyrsta sinn sem áminning er stofnuð fyrir viðskiptamann er uppsetning stigs 1 notuð. Þegar áminningin er send er númer stigsins skráð á áminningarfærslurnar sem stofnast og tengt við einstakar viðskiptamannafærslur. Þurfi að minna viðskiptamanninn á aftur eru allar áminningarfærslur tengdar opnum viðskiptamannafærslum kannaðar til að finna hæsta stigsnúmerið. Skilyrði næsta stigsnúmers verða síðan notuð í nýju áminningunni.

Ef stofnaðar eru fleiri áminningar en skilgreind hafa verið stig fyrir verða skilyrði hæsta stigsins notuð. Hægt er að stofna eins margar áminningar og leyft er í reitnum **Hám.fj. innheimtubréfa** í áminningarskilmálunum.

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Skilmálar innheimtubréfa** og veldu síðan tengda tengilinn.  
2. Á síðunni **Skilmálar innheimtubréfa** er valin lína með skilmálum sem setja á upp stig fyrir og síðan er valin aðgerðin **Stig**.  
3. Fyllið inn í reitina eftir þörfum.  

    Fyrir hvert áminningarstig er hægt að skilgreina sérstök skilyrði sem í geta falist viðbótargjöld, bæði í SGM og erlendum gjaldmiðli. Hægt er að skilgreina mörg viðbótargjöld í erlendum gjaldmiðlum fyrir hvern kóða á síðunni **Stig innheimtubréfa**.
4. Velja aðgerðina **gjaldmiðlar**.
5. Á síðunni **Gjaldmiðlar fyrir stig innheimtubréfa** skal skilgreina gjaldmiðlakóða og viðbótargjald fyrir hvern kóða stigs innheimtubréfa og samsvarandi númer stigs innheimtubréfa.

    > [!NOTE]  
    > Þegar innheimtubréf eru stofnuð í erlendum gjaldmiðli tekur kerfið mið af þeim skilyrðum sem sett eru um erlendan gjaldmiðil hér til að stofna innheimtubréf. Ef engin vaxtaskilyrði innheimtubréfa fyrir erlenda gjaldmiðla eru sett upp notar kerfið SGM-vaxtaskilyrðin sem sett voru upp á síðunni **Stig innheimtubréfs** og breytir þeim í viðeigandi gjaldmiðil.

    Fyrir hvert áminningarstig er hægt að skilgreina texta sem verður prentaður á undan (**Byrjunartexti**) eða eftir (**Lokatexti**) færslunum í áminningunni.

6. Veljið **Byrjunartexti** eða **Lokatexti** aðgerðirnar eftir því sem við á, og fyllið **Áminningartexti** síðuna.
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

Til dæmis, ef þú skrifar**Þú skuldar %9 %7 á gjalddaga %2** mun innheimtubréfið innihalda eftirfarandi texta: **Þú skuldar 1.200,50 USD á gjalddaga 02-02-2014.**.

> [!NOTE]
> Gjalddaginn er reiknaður samkvæmt dagsetningarreiknireglunni sem var slegin inn. Nánari upplýsingar er að finna í kaflanum „Notkun dagsetningarreiknireglna“ í [Færa inn dagsetningabil](ui-enter-date-ranges.md).

Þegar búið er að setja upp áminningarskilmálana með viðbótarstigum og texta þarf að færa einn kóðann á hvert viðskiptamannaspjald. Frekari upplýsingar eru í [Skrá nýja viðskiptamenn](sales-how-register-new-customers.md).

## <a name="to-create-a-reminder-automatically"></a>Innheimtubréf búin til sjálfvirkt:
Innheimtubréf líkist reikningi. Þegar innheimtubréf er búið til þarf að fylla út innheimtuhaus ásamt einni eða fleiri innheimtulínum. Þú getur notað aðgerð til að stofna innheimtubréf fyrir alla viðskiptamenn sjálfvirkt.

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Innheimtubréf** og veldu síðan tengda tengilinn.
2. Á síðunni **Innheimtubréf**, skal velja aðgerðina **Stofna innheimtubréf**.
3. Á síðunni **Stofna innheimtubréf** fyllið út reitina til að skilgreina hvernig og til hvaða aðila innheimtubréfin skulu stofnuð.
4. Velja hnappinn **Í lagi**.

## <a name="to-create-a-reminder-manually"></a>Innheimtubréf búin til handvirkt:
Á síðunni **Innheimtubréf** geturðu fyllt í flýtiflipann **Almennt** handvirkt og svo látið fylla í línurnar sjálfvirkt.

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Innheimtubréf** og veldu síðan tengda tengilinn.
2. Valið er **Nýtt** aðgerð.
3. Fyllt er út í reiti eftir því sem er nauðsynlegt í flýtiflipanum **Almennt**.
4. Veljið aðgerðina **Leggja til innheimtubr.línur**.
5. Í runuvinnslunni **Leggja til innheimtubr.línur** skal fylla út reitina til að skilgreina hvernig og til hvaða aðila innheimtubréfin skulu stofnuð.
6. Veljið gátreiturinn **Taka færslur í bið með** ef á áminningum eiga að birtast opnar færslur gjaldfallnar í bið.

    > [!Important]
    > Opnar færslur sem eru á bið verða settar inn, þrátt fyrir stillingar í gátreitur Aðeins færslur með gjaldföllnum upphæðum.

7. Velja hnappinn **Í lagi**.

## <a name="to-replace-reminder-texts"></a>Texta innheimtubréfs skipt út.  
Nokkrar leiðir eru í boði til að ákvarða hvaða texti birtist á prentuðu innheimtubréfi. Í einstaka tilvikum gæti þurft að skipta út byrjunar- og endatexta gildandi stigs með texta af öðru stigi.

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Innheimtubréf** og veldu síðan tengda tengilinn.
2. Opna skal viðeigandi innheimtubréf, og síðan velja **uppfæra innheimtubréf texti** aðgerðina.
3. Á síðunni **uppfæra innheimtubréf texti** er fært inn stigið sem óskað er eftir í reitnum **Stig innheimtubréfs**.
3. Velja hnappinn **Í lagi** til að uppfæra byrjunar- og endatexta.

## <a name="to-issue-a-reminder"></a>Gefa út innheimtubréf
Þegar búið er að stofna áminningar, og breyta þeim ef þarf, er hægt að prenta prufuskýrslur eða senda áminningarnar.

Þegar áminning er send eru gögnin flutt á sérstaka síðu fyrir sendar áminningar. Um leið eru áminningarfærslurnar bókaðar. Ef vextir eða viðbótarkostnaður hefur verið reiknaður eru færslur bókaðar í viðskiptamannabók og á fjárhag.

Þegar innheimtubréf er sent bókar kerfið færslur eftir því sem var tilgreint á síðunni **Skilmálar innheimtubréfa**. Þessi staðall ákvarðar hvort vextir og/eða viðbótargjöld séu bókuð á reikning viðskiptamanns og fjárhag. Uppsetning á síðunni **Bókunarflokkar viðskiptavinar** ákvarðar á hvaða reikninga er bókað.

Fyrir hverja fjárhagsfærslu viðskiptamanns á vaxtareikning, er stofnuð færsla á síðunni **Innheimtubréf/vaxtafærslur**.

Ef gátreitirnir **Bóka vexti** og **Bóka viðbótargjöld** eru valdir á síðunni **Skilmálar innheimtubréfs**, eru eftirfarandi færslur einnig stofnaðar:

- Ein færsla á síðunni **Fjárhagsfærslur viðskiptamanna**
- Ein útistandandi færsla í viðeigandi fjárhagsreikningi
- Ein vaxta- og/eða viðbótargjaldsfærsla í viðeigandi fjárhagsreikningi

Að auki getur sending innheimtubréfs leitt af sér VSK-færslur.

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Innheimtubréf** og veldu síðan tengda tengilinn.
2. Velja skal viðeigandi innheimtubréf, og síðan velja **Senda út** aðgerðina.
3. Á síðunni **Senda út innheimtubréf** þarf að fylla reitina út eftir þörfum.
4. Velja hnappinn **Í lagi**.

Innheimtubréfið er annað hvort prentað út eða sent á tiltekið netfang sem PDF viðhengi.

## <a name="to-set-up-finance-charge-terms"></a>Setja upp vaxtaskilmála
Stofna verður kóta fyrir hvern vaxtaútreikning. Síðan er hægt að færa þennan kóða inn í reitinn **Kóði vaxtaskilmála** á viðskiptamanna- eða lánadrottnaspjöldum.

Hægt er að reikna vexti með því að nota annaðhvort regluna um meðaltal daglegs jafnaðar eða regluna um gjaldfallna stöðu.

* Regla um gjaldfallna stöðu:

    Vaxtareikningurinn er einfaldlega prósentuhluti af gjaldföllnu upphæðinni:  
    *Regla fyrir gjaldfallna stöðu* - *Vaxtareikningur* = *Gjaldfallin upphæð* x *(Vextir / 100)*

*   Regla um daglega meðaltalsstöðu

    Fjöldi daga sem greiðslan er komin fram yfir gjalddaga er tekin með í reikninginn:  
    *Regla um daglega meðaltalsstöðu* - *Vaxtareikningur* = *Gjaldfallin upphæð* x *(Fjöldi daga fram yfir gjalddaga / Vaxtatímabil)* x *(Vextir/100)*

Að auki er sérhver kóti í töflunni Vaxtaskilmálar tengdur undirtöflunni Vaxtatexti. Fyrir hvern vaxtagjalddaga er hægt að skilgreina byrjunar- og/eða lokatexta sem verður prentaður á vaxtareikninginn.

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Vaxtaskilmálar** og veldu síðan tengda tengilinn.  
2. Fyllið inn í reitina eftir þörfum.  
3. Eigi að nota fleiri en eina samsetningu vaxtaskilmálar þarf að setja upp kóta fyrir hverja þeirra.

    Fyrir hvern vaxtaskilmála er hægt að skilgreina sérstök skilyrði sem í geta falist viðbótargjöld, bæði í SGM og erlendum gjaldmiðli. Hægt er að skilgreina mörg viðbótargjöld í erlendum gjaldmiðlum fyrir hvern kóða á síðunni **Vaxtaskilmálar**.
4. Velja aðgerðina **gjaldmiðlar**.
5. Á síðunni **Gjaldmiðlar fyrir vaxtaskilmála**, skal skilgreina gjaldmiðilskóða fyrir hvern skilmála og viðbótargjald.

    > [!NOTE]  
    > Þegar vextir eru stofnaðir í erlendum gjaldmiðli tekur kerfið mið af þeim skilyrðum sem sett eru um erlendan gjaldmiðil hér til að stofna vaxtareikningur. Ef engin vaxtaskilyrði fyrir erlenda gjaldmiðla eru sett upp notar kerfið SGM-vaxtaskilyrðin sem sett voru upp á síðunni **Vaxtaskilmálar** og breytir þeim í viðeigandi gjaldmiðil.

    Fyrir hvern kóða vaxtaskilmála er hægt að tilgreina texta sem á að prenta á undan (**Byrjunartexti**) eða á eftir (**Endatexti**) færslunum á vaxtareikningnum.  
6. Veljið **Byrjunartexti** eða **Lokatexti** aðgerðirnar eftir því sem við á, og fyllið út síðuna **Vaxtatexti**.
7. Til að setja viðeigandi gildi sjálfvirkt inn í vaxtatexta, skal fara inn í eftirfarandi staðgengla í reitnum **Texti**.

|Frátaka|Gildi:|  
|-----------------|-----------|  
|%1|Innihald reitsins **Dagsetning skjals** á bréfshaus vaxtareiknings|  
|%2|Innihald reitsins **gjalddagi** á bréfshaus vaxtareiknings|  
|%3|Innihald reitsins **Vextir** í viðeigandi vaxtaskilmálum|  
|%4|Innihald reitsins **eftirstöðvar** á bréfshaus vaxtareiknings|  
|%5|Innihald reitsins **vextir upphæð** á bréfshaus vaxtareiknings|  
|%6|Innihald reitsins **Viðbótargjald** á bréfshaus vaxtareiknings|  
|%7|Heildarupphæð innheimtubréfsins|  
|%8|Innihald reitsins **gjaldmiðilskóði** á bréfshaus vaxtareiknings|  
|%9|Innihald reitsins **bókunardagsetning** á bréfshaus vaxtareiknings|  

## <a name="to-create-a-finance-charge-memo-manually"></a>Vaxtareikningar stofnaðir handvirkt:  
Vaxtareikningur er svipaður reikningi. Hægt er að fylla hausinn út handvirkt og línurnar sjálfvirkt, eða stofna vaxtareikninga sjálfkrafa fyrir alla viðskiptamenn.

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Vaxtareikningar** og veldu síðan tengda tengilinn.  
2. Veljið aðgerðina **Nýtt** og fyllið svo út reitina eins og þörf krefur.  
3. Velja aðgerðina **Leggja til vaxtareikn.línur**.
4. Á síðunni **Tillaga vaxtareikningur línur**, skal sett afmörkun á flýtiflipanum **Viðskm.færsla** eigi aðeins að búa til vaxtareikninga fyrir tilteknar færslur.  
5.  Veldu hnappinn **Í lagi** til að hefja keyrsluna.  

## <a name="to-update-finance-charge-memo-texts"></a>Vaxtatexti uppfærður  
Í einhverjum tilfellum gæti þurft að breyta upphafs- og lokatextanum sem settur er upp fyrir vaxtaskilmálana. Ef það er gert eftir að vaxtareikningar hafa verið stofnaðir, en ekki sendir, er hægt að uppfæra reikningana með nýja textanum.

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Vaxtareikningur** og veldu síðan tengda tengilinn.  
2. Opna vaxtareikninginn sem þú vilt breyta textanum í, og velja síðan aðgerðina **Uppfæra vaxtatexta**.
3. Á síðunni **Uppfæra vaxtatexta** er hægt að setja afmörkun eigi að uppfæra marga vaxtareikninga.
4. Velja hnappinn **Í lagi** til að uppfæra byrjunar- og endatexta.  

## <a name="to-issue-finance-charge-memos"></a>Vaxtareikningar sendir út
Þegar búið er að stofna vaxtareikninga, og breyta þeim ef þarf, er hægt að prenta prufuskýrslur eða senda vaxtareikningana.

Þegar innheimtubréf er sent út bókar kerfið færslur eftir því sem var tilgreint á síðunni **Vaxtaskilmálar**. Þessi staðall ákvarðar hvort vextir og/eða viðbótargjöld séu bókuð á reikning viðskiptamanns og fjárhag. Uppsetning á síðunni **Bókunarflokkar viðskiptavinar** ákvarðar á hvaða reikninga er bókað.

Fyrir hverja fjárhagsfærslu viðskiptamanns á vaxtareikning, er stofnuð færsla á síðunni **Innheimtubréf/vaxtafærslur**.

Ef gátreitirnir **Bóka vexti** og **Bóka viðbótargjöld** eru valdir á síðunni **Vaxtaskilmálar**, eru eftirfarandi færslur einnig stofnaðar:

- Ein færsla á síðunni **Fjárhagsfærslur viðskiptamanna**
- Ein útistandandi færsla í viðeigandi fjárhagsreikningi
- Ein vaxta- og/eða viðbótargjaldsfærsla í viðeigandi fjárhagsreikningi

Að auki getur sending vaxtareikningur leitt af sér VSK-færslur.

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Vaxtareikningar** og veldu síðan tengda tengilinn.
2. Velja skal viðeigandi reikning og síðan velja **Senda út** aðgerðina.
3. Á síðunni **Senda út vaxtareikninga** þarf að fylla reitina út eftir þörfum.
4. Velja hnappinn **Í lagi**

Vaxtareikningurinn er annað hvort prentað út eða sent á tiltekið netfang sem PDF viðhengi.

## <a name="to-view-reminder-and-finance-charge-entries"></a>Innheimtubréfa- og vaxtafærslur skoðaðar:  
Þegar innheimtubréf er sent er innheimtubréfafærslu búin til á síðunni **Innheimtubréf/Vaxtafærsla** fyrir hverja innheimtubréfslínu sem inniheldur viðskiptamannafærslu. Hægt er að fá yfirlit yfir færslur innheimtubréfa fyrir ákveðinn viðskiptamann.    
1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Viðskiptamenn** og veldu síðan tengda tengilinn.  
2. Opna skal viðeigandi viðskiptamannaspjald og veljið síðan aðgerðina **fjárhagsfærslur**.
3. Á síðunni **Færslur í viðskiptamannabók** er smellt er á línuna með bókarfærslunni sem á að skoða innheimtubréfafærslur fyrir og síðan er smellt á **Innheimtubréf/Vaxtafærslur**.

## <a name="see-also"></a>Sjá einnig
[Stjórnun skulda](receivables-manage-receivables.md)  
[Sala](sales-manage-sales.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

