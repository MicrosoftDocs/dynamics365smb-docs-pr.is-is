---
title: Innheimta útistandandi skuldir
description: Lækar hvernig skal senda innheimtubréf til viðskiptamanns varðandi gjaldfallinnar greiðslu og bæta kostnaði eða þóknun við greiðsluna vegna tafarinnar.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment due, debt, overdue, fee, charge, reminder
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 8de49351f6fa81363f624c39c73d4360be440083
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5392226"
---
# <a name="collect-outstanding-balances"></a>Innheimta útistandandi skuldir

Í stjórnun útistandandi skulda felst að kanna hvort upphæðir sem falla í gjalddaga eru greiddar tímanlega. Ef viðskiptamenn eru í vanskilum geturðu sent **Yfirlit viðskiptamanns** sem innheimtubréf. Þú getur einnig gefið út innheimtubréf.

Hægt er að nota áminningar til að minna viðskiptamenn á gjaldfallnar upphæðir. Einnig er hægt að nota áminningar til að reikna út vexti og annan kostnað og hafa þær upplýsingar með í áminningunni. Notaðir eru vaxtareikningar ef krefja á viðskiptamenn um vexti eða gjöld án þess að minna þá á gjaldfallnar upphæðir.

## <a name="statements"></a>Yfirlit

Á viðskiptamannaspjaldinu er hægt að búa til yfirlit með þessum færslum viðskiptamannsins. Því næst er mynduð PDF-skrá send á viðskiptamanninn. Að öðrum kosti skal nota skýrsluna **Yfirlit viðskiptamanns** til að senda viðskiptamönnunum yfirlit yfir viðskipta ykkar á milli. Hægt er að senda yfirlit viðskiptamanns í Excel til frekari vinnslu.  

### <a name="to-send-the-customer-statement-report"></a>Til að senda yfirlitsskýrslu viðskiptamanns

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Yfirlit viðskiptamanns** og veldu síðan tengda tengilinn.
2. Fyllið inn í svæðin eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Undir **úttaksvalkostir**, skal velja hvernig eigi að senda skýrslunnar til viðskiptamanns.

> [!NOTE]
> Ef mörgum gjaldmiðlum ef verið að nota, er yfirlitsskýrslu Viðskiptamanns alltaf prentuð í gjaldmiðil viðskiptamannsins. Síðustu dagsetningunni í í yfirlitstímabili er einnig notuð sem yfirlitsdagsetning og dagsetning fyrir aldursgreiningu, ef aldursgreining er höfð með.

## <a name="reminders"></a>Innheimtubréf

Áður en hægt er að stofna áminningar þarf að setja upp skilmála áminninga og tengja þá við viðskiptamenn. Frekari upplýsingar eru í [Setja upp skilmála og stig innheimtubréfa](finance-setup-reminders.md). [!INCLUDE [reminder-terms](includes/reminder-terms.md)] Innihald síðunnar **Vaxtaskilmálar** ákveður hvort vextir eru reiknaðir í áminningunni.  

Hægt er að keyra reglulega keyrsluna **Stofna innheimtubréf** til að stofna áminningar fyrir alla viðskiptamenn með gjaldfallnar skuldir eða stofna áminningu handvirkt fyrir einstaka viðskiptamenn og láta reikna línurnar og fylla þær út sjálfvirkt.  

Þegar búið er að stofna áminningarnar er hægt að breyta þeim. Textinn sem birtist í upphafi og í lok áminningar ræðst af áminningarstiginu og hægt er að sjá hann í dálknum **Lýsing**. Ef reiknuð upphæð hefur verið sett inn sjálfvirkt í upphafs- eða lokatextann verður textinn ekki leiðréttur ef línunum er eytt. Þá verður að nota aðgerðina **Uppfæra áminningu**.  

Viðskiptamannsfærsla með reitinn **Bið** útfylltan leyfir ekki stofnun áminningar. En ef áminning er stofnuð á grunni annarrar færslu verður gjaldfallin færsla merkt í bið einnig höfð með í áminningunni. Vextir eru ekki reiknaðir á línur með þessum færslum.

Þegar búið er að stofna áminningar, og breyta þeim ef þarf, er hægt að prenta prufuskýrslur eða senda áminningarnar, vanalega sem tölvupóst.

### <a name="to-create-a-reminder-automatically"></a>Innheimtubréf búin til sjálfvirkt:

Innheimtubréf líkist reikningi. Þegar innheimtubréf er búið til þarf að fylla út innheimtuhaus ásamt einni eða fleiri innheimtulínum. Þú getur notað aðgerð til að stofna innheimtubréf fyrir alla viðskiptamenn sjálfvirkt.

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Innheimtubréf** og veldu síðan tengda tengilinn.
2. Á síðunni **Innheimtubréf**, skal velja aðgerðina **Stofna innheimtubréf**.
3. Á síðunni **Stofna innheimtubréf** fyllið út reitina til að skilgreina hvernig og til hvaða aðila innheimtubréfin skulu stofnuð.
4. Velja hnappinn **Í lagi**.

### <a name="to-create-a-reminder-manually"></a>Innheimtubréf búin til handvirkt:

Á síðunni **Innheimtubréf** geturðu fyllt í flýtiflipann **Almennt** handvirkt og svo látið fylla í línurnar sjálfvirkt.

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Innheimtubréf** og veldu síðan tengda tengilinn.
2. Valið er aðgerðin **Nýtt**.
3. Fyllt er út í reiti eftir því sem er nauðsynlegt í flýtiflipanum **Almennt**.
4. Veljið aðgerðina **Leggja til innheimtubr.línur**.
5. Í runuvinnslunni **Leggja til innheimtubr.línur** skal fylla út reitina til að skilgreina hvernig og til hvaða aðila innheimtubréfin skulu stofnuð.
6. Veljið gátreiturinn **Taka færslur í bið með** ef á áminningum eiga að birtast opnar færslur gjaldfallnar í bið.
7. Veldu gátreitinn **Aðeins færslur með gjaldföllnum upphæðum** ef þú vilt að áminningarnar innihaldi aðeins opnar færslur sem eru komnar fram yfir á tíma. Aðeins reikningar og greiðslur verða sýndar þar sem þetta eru færslurnar þar sem greiðslur viðskiptamanna kunna að vera gjaldfallnar.

    > [!Important]
    > Opnar færslur sem eru á bið verða settar inn, þrátt fyrir stillingar í gátreitur **Aðeins færslur með gjaldföllnum upphæðum**.

8. Velja hnappinn **Í lagi**.

### <a name="to-replace-reminder-texts"></a>Texta innheimtubréfs skipt út.

Nokkrar leiðir eru í boði til að ákvarða hvaða texti birtist á prentuðu innheimtubréfi. Í einstaka tilvikum gæti þurft að skipta út byrjunar- og endatexta gildandi stigs með texta af öðru stigi.

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Innheimtubréf** og veldu síðan tengda tengilinn.
2. Opna skal viðeigandi innheimtubréf, og síðan velja **uppfæra innheimtubréf texti** aðgerðina.
3. Á síðunni **uppfæra innheimtubréf texti** er fært inn stigið sem óskað er eftir í reitnum **Stig innheimtubréfs**.
4. Velja hnappinn **Í lagi** til að uppfæra byrjunar- og endatexta.

### <a name="to-issue-a-reminder"></a>Gefa út innheimtubréf

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

### <a name="to-cancel-an-issued-reminder"></a>Hætta við útgefið innheimtubréf

Ef innheimtubréf voru gefin út fyrir mistök er hægt að hætta við þau áður en þau eru send út. Þetta er hægt að gera annaðhvort fyrir hvert bréf fyrir sig eða í lotu.

1. Á síðunni **Send innheimtubréf** skal velja eina eða fleiri línu fyrir send innheimtubréf sem á að hætta við og velja svo aðgerðina **Hætta við**.
2. Á síðunni **Hætta við útgefnar áminningar** skal fylla út reitina eftir þörfum og velja síðan hnappinn **Í lagi**.

## <a name="finance-charges"></a>Vextir

Þegar viðskiptamaður greiðir ekki á gjalddaga er hægt að láta reikna út vexti sjálfvirkt og bæta þeim við gjaldföllnu upphæðina á reikningi viðskiptamannsins. Hægt er að láta viðskiptamenn vita af viðbótargjöldunum með því að senda vaxtareikninga.  

> [!NOTE]  
> Vaxtareikningar eru notaðir til að reikna út vexti og annan kostnað og til að láta viðskiptamenn vita um þann kostnað án þess að minna þá á gjaldfallnar upphæðir. Einnig er hægt að reikna vexti á gjaldfallnar upphæðir þegar áminningar eru stofnaðar.  

Áður en hægt verður að stofna vaxtareikninga þarf að setja upp skilmála. Nánari upplýsingar um það eru í [Setja upp vaxtaskilmála](finance-setup-finance-charges.md).  

Hægt er að stofna vaxtareikning fyrir einstakan viðskiptamann og fylla línurnar út sjálfvirkt. Einnig er hægt að nota vinnsluna **Stofna vaxtareikninga** til að stofna vaxtareikninga fyrir alla eða valda viðskiptamenn með gjaldfallna stöðu.  

Þegar búið er að stofna vaxtareikninga er hægt að breyta þeim. Textinn sem birtist í upphafi og í lok vaxtareiknings ræðst af vaxtaskilmálunum og hægt er að sjá hann dálknum **Lýsing** í línunum. Ef reiknuð upphæð hefur verið sett inn sjálfvirkt í upphafs- eða lokatextann verður textinn ekki leiðréttur ef línunum er eytt. Þá verður að nota aðgerðina **Uppfæra vaxtatexta**.  

Þegar búið er að stofna vaxtareikninga, og breyta þeim ef þarf, er hægt að prenta prufuskýrslur eða senda vaxtareikningana, vanalega sem tölvupóst.

### <a name="to-create-a-finance-charge-memo-manually"></a>Vaxtareikningar stofnaðir handvirkt:

Vaxtareikningur er svipaður reikningi. Hægt er að fylla hausinn út handvirkt og línurnar sjálfvirkt, eða stofna vaxtareikninga sjálfkrafa fyrir alla viðskiptamenn.

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Vaxtareikningar** og veldu síðan tengda tengilinn.  
2. Veljið aðgerðina **Nýtt** og fyllið svo út reitina eins og þörf krefur.  
3. Velja aðgerðina **Leggja til vaxtareikn.línur**.
4. Á síðunni **Tillaga vaxtareikningur línur**, skal sett afmörkun á flýtiflipanum **Viðskm.færsla** eigi aðeins að búa til vaxtareikninga fyrir tilteknar færslur.

    > [!NOTE]
    > Þó að þau séu skráð hefur það engin áhrif að velja **Greiðsla** og **Kreditreikningur** sem síur **Skjalagerð** vegna þess að **Stinga upp á vaxtareikningslínum** vinnur aðeins með plúsupphæðir.
5.  Veldu hnappinn **Í lagi** til að hefja keyrsluna.  

### <a name="to-update-finance-charge-memo-texts"></a>Vaxtatexti uppfærður  
Í einhverjum tilfellum gæti þurft að breyta upphafs- og lokatextanum sem settur er upp fyrir vaxtaskilmálana. Ef það er gert eftir að vaxtareikningar hafa verið stofnaðir, en ekki sendir, er hægt að uppfæra reikningana með nýja textanum.

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Vaxtareikningur** og veldu síðan tengda tengilinn.  
2. Opna vaxtareikninginn sem þú vilt breyta textanum í, og velja síðan aðgerðina **Uppfæra vaxtatexta**.
3. Á síðunni **Uppfæra vaxtatexta** er hægt að setja afmörkun eigi að uppfæra marga vaxtareikninga.
4. Velja hnappinn **Í lagi** til að uppfæra byrjunar- og endatexta.  

### <a name="to-issue-finance-charge-memos"></a>Vaxtareikningar sendir út
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

### <a name="to-cancel-an-issued-finance-charge-memo"></a>Til að hætta við útgefinn vaxtareikning
Ef vaxtareikningar voru gefnir út fyrir mistök er hægt að hætta við þá áður en þeir eru sendir út. Þetta er hægt að gera annaðhvort fyrir hvern reikning fyrir sig eða í runu.
1. Á síðunni **Útgefnir vaxtareikningar** skal velja eina eða fleiri línur fyrir útgefna vaxtareikninga sem á að hætta við og velja svo aðgerðina **Hætta við**.
2. Á síðunni **Hætta við útgefna vaxtareikninga** skal fylla út reitina eftir þörfum og velja síðan hnappinn **Í lagi**.

### <a name="to-view-reminder-and-finance-charge-entries"></a>Innheimtubréfa- og vaxtafærslur skoðaðar:  
Þegar innheimtubréf er sent er innheimtubréfafærslu búin til á síðunni **Innheimtubréf/Vaxtafærsla** fyrir hverja innheimtubréfslínu sem inniheldur viðskiptamannafærslu. Hægt er að fá yfirlit yfir færslur innheimtubréfa fyrir ákveðinn viðskiptamann.    
1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Viðskiptamenn** og veldu síðan tengda tengilinn.  
2. Opna skal viðeigandi viðskiptamannaspjald og veljið síðan aðgerðina **fjárhagsfærslur**.
3. Á síðunni **Færslur í viðskiptamannabók** er smellt er á línuna með bókarfærslunni sem á að skoða innheimtubréfafærslur fyrir og síðan er smellt á **Innheimtubréf/Vaxtafærslur**.

## <a name="multiple-interest-rates"></a>Margir vextir

Þegar vaxtaskilmálar og skilmálar innheimtubréfa eru sett upp, fyrir sekt vegna seinkunar á greiðslu, er hægt að tilgreina marga vexti þannig að sektargreiðsla er reiknuð út frá mismunandi vöxtum á mismunandi tímabilum. Ef margir vextir eru ekki settir upp, þá verða vextirnir og tímabilið sem er skilgreint á síðunum **Vaxtaskilmálar** og **Skilmálar innheimtubréfa** notað fyrir allt reikningstímabilið. Frekari upplýsingar eru í [Setja upp marga vexti](finance-how-to-set-up-multiple-interest-rates.md).  

## <a name="see-related-training-at-microsoft-learn"></a>Sjá tengda þjálfun á [Microsoft Learn](/learn/paths/process-financial-periodic-activities-dynamics-365-business-central/)

## <a name="see-also"></a>Sjá einnig

[Setja upp skilmála og stig innheimtubréfa](finance-setup-reminders.md)  
[Setja upp vaxtaskilmála](finance-setup-finance-charges.md)  
[Stjórnun skulda](receivables-manage-receivables.md)  
[Sala](sales-manage-sales.md)  
[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]