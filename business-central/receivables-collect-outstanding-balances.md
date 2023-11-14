---
title: Innheimta útistandandi skuldir
description: 'Kynntu þér hvernig á að minna viðskiptavini á útistandandi greiðslur. Sendu yfirlit viðskiptamanns, gefðu út áminningu eða sendu vaxtareikning.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'payment due, debt, overdue, fee, charge, reminder'
ms.search.form: '6, 25, 440, 443, 448, 452'
ms.date: 02/09/2022
ms.author: bholtorf
---
# Innheimta útistandandi skuldir

Í stjórnun útistandandi skulda felst að kanna hvort upphæðir sem falla í gjalddaga eru greiddar tímanlega. Ef viðskiptamenn eru í vanskilum geturðu sent **Yfirlit viðskiptamanns** sem innheimtubréf. Þú getur einnig gefið út innheimtubréf.

Hægt er að nota áminningar til að minna viðskiptamenn á gjaldfallnar upphæðir. Einnig er hægt að nota áminningar til að reikna út vexti og annan kostnað og hafa þær upplýsingar með í áminningunni. Notaðir eru vaxtareikningar ef krefja á viðskiptamenn um vexti eða gjöld án þess að minna þá á gjaldfallnar upphæðir.

## Yfirlit

Á viðskiptamannaspjaldinu er hægt að búa til yfirlit með þessum færslum viðskiptamannsins. Því næst er mynduð PDF-skrá send á viðskiptamanninn. Að öðrum kosti skal nota skýrsluna **Yfirlit viðskiptamanns** til að senda viðskiptamönnunum yfirlit yfir viðskipta ykkar á milli. Hægt er að senda yfirlit viðskiptamanns í Excel til frekari vinnslu.  

### Til að senda yfirlitsskýrslu viðskiptamanns

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar 10.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Yfirlit viðskiptavinar** og velja síðan viðkomandi tengil.
2. Fyllið inn í svæðin eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Undir **úttaksvalkostir**, skal velja hvernig eigi að senda skýrslunnar til viðskiptamanns.

> [!NOTE]
> Ef mörgum gjaldmiðlum ef verið að nota, er yfirlitsskýrslu Viðskiptamanns alltaf prentuð í gjaldmiðil viðskiptamannsins. Síðustu dagsetningunni í í yfirlitstímabili er einnig notuð sem yfirlitsdagsetning og dagsetning fyrir aldursgreiningu, ef aldursgreining er höfð með.

## Innheimtubréf

[!INCLUDE [receivables-reminders](includes/receivables-reminders.md)]

## Vextir

Þegar viðskiptamaður greiðir ekki á gjalddaga er hægt að láta reikna út vexti sjálfvirkt og bæta þeim við gjaldföllnu upphæðina á reikningi viðskiptamannsins. Hægt er að láta viðskiptamenn vita af viðbótargjöldunum með því að senda vaxtareikninga.  

> [!NOTE]  
> Vaxtareikningar eru notaðir til að reikna út vexti og annan kostnað og til að láta viðskiptamenn vita um þann kostnað án þess að minna þá á gjaldfallnar upphæðir. Einnig er hægt að reikna vexti á gjaldfallnar upphæðir þegar áminningar eru stofnaðar.  

Áður en hægt verður að stofna vaxtareikninga þarf að setja upp skilmála. Nánari upplýsingar um það eru í [Setja upp vaxtaskilmála](finance-setup-finance-charges.md).  

Hægt er að stofna vaxtareikning fyrir einstakan viðskiptamann og fylla línurnar út sjálfvirkt. Einnig er hægt að nota vinnsluna **Stofna vaxtareikninga** til að stofna vaxtareikninga fyrir alla eða valda viðskiptamenn með gjaldfallna stöðu.  

Þegar búið er að stofna vaxtareikninga er hægt að breyta þeim. Textinn sem birtist í upphafi og í lok vaxtareiknings ræðst af vaxtaskilmálunum og hægt er að sjá hann dálknum **Lýsing** í línunum. Ef reiknuð upphæð hefur verið sett inn sjálfvirkt í upphafs- eða lokatextann verður textinn ekki leiðréttur ef línunum er eytt. Þá verður að nota aðgerðina **Uppfæra vaxtatexta**.  

Þegar búið er að stofna vaxtareikninga, og breyta þeim ef þarf, er hægt að prenta prufuskýrslur eða senda vaxtareikningana, vanalega sem tölvupóst.

### Vaxtareikningar stofnaðir handvirkt:

Vaxtareikningur er svipaður reikningi. Hægt er að fylla hausinn út handvirkt og línurnar sjálfvirkt, eða stofna vaxtareikninga sjálfkrafa fyrir alla viðskiptamenn.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar 2.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Vaxtareikningar** og velja síðan viðkomandi tengil.  
2. Veljið aðgerðina **Nýtt** og fyllið svo út reitina eins og þörf krefur.  
3. Velja aðgerðina **Leggja til vaxtareikn.línur**.
4. Á síðunni **Tillaga vaxtareikningur línur**, skal sett afmörkun á flýtiflipanum **Viðskm.færsla** eigi aðeins að búa til vaxtareikninga fyrir tilteknar færslur.

    > [!NOTE]
    > Þó að þau séu skráð hefur það engin áhrif að velja **Greiðsla** og **Kreditreikningur** sem síur **Skjalagerð** vegna þess að **Stinga upp á vaxtareikningslínum** vinnur aðeins með plúsupphæðir.
5.  Veldu hnappinn **Í lagi** til að hefja keyrsluna.  

### Vaxtatexti uppfærður  
Í einhverjum tilfellum gæti þurft að breyta upphafs- og lokatextanum sem settur er upp fyrir vaxtaskilmálana. Ef það er gert eftir að vaxtareikningar hafa verið stofnaðir, en ekki sendir, er hægt að uppfæra reikningana með nýja textanum.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar 3.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Vaxtareikningur** og velja síðan viðkomandi tengil.  
2. Opna vaxtareikninginn sem þú vilt breyta textanum í, og velja síðan aðgerðina **Uppfæra vaxtatexta**.
3. Á síðunni **Uppfæra vaxtatexta** er hægt að setja afmörkun eigi að uppfæra marga vaxtareikninga.
4. Velja hnappinn **Í lagi** til að uppfæra byrjunar- og endatexta.  

### Vaxtareikningar sendir út
Þegar búið er að stofna vaxtareikninga, og breyta þeim ef þarf, er hægt að prenta prufuskýrslur eða senda vaxtareikningana.

Þegar innheimtubréf er sent út bókar kerfið færslur eftir því sem var tilgreint á síðunni **Vaxtaskilmálar**. Þessi staðall ákvarðar hvort vextir og/eða viðbótargjöld séu bókuð á reikning viðskiptamanns og fjárhag. Uppsetning á síðunni **Bókunarflokkar viðskiptavinar** ákvarðar á hvaða reikninga er bókað.

Fyrir hverja fjárhagsfærslu viðskiptamanns á vaxtareikning, er stofnuð færsla á síðunni **Innheimtubréf/vaxtafærslur**.

Ef gátreitirnir **Bóka vexti** og **Bóka viðbótargjöld** eru valdir á síðunni **Vaxtaskilmálar**, eru eftirfarandi færslur einnig stofnaðar:

- Ein færsla á síðunni **Fjárhagsfærslur viðskiptamanna**
- Ein útistandandi færsla í viðeigandi fjárhagsreikningi
- Ein vaxta- og/eða viðbótargjaldsfærsla í viðeigandi fjárhagsreikningi

Að auki getur sending vaxtareikningur leitt af sér VSK-færslur.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar 4.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Vaxtareikningar** og velja síðan viðkomandi tengil.
2. Velja skal viðeigandi reikning og síðan velja **Senda út** aðgerðina.
3. Á síðunni **Senda út vaxtareikninga** þarf að fylla reitina út eftir þörfum.
4. Velja hnappinn **Í lagi**

Vaxtareikningurinn er annað hvort prentað út eða sent á tiltekið netfang sem PDF viðhengi.

### Til að hætta við útgefinn vaxtareikning
Ef vaxtareikningar voru gefnir út fyrir mistök er hægt að hætta við þá áður en þeir eru sendir út. Þetta er hægt að gera annaðhvort fyrir hvern reikning fyrir sig eða í runu.
1. Á síðunni **Útgefnir vaxtareikningar** skal velja eina eða fleiri línur fyrir útgefna vaxtareikninga sem á að hætta við og velja svo aðgerðina **Hætta við**.
2. Á síðunni **Hætta við útgefna vaxtareikninga** skal fylla út reitina eftir þörfum og velja síðan hnappinn **Í lagi**.

### Innheimtubréfa- og vaxtafærslur skoðaðar:  
Þegar innheimtubréf er sent er innheimtubréfafærslu búin til á síðunni **Innheimtubréf/Vaxtafærsla** fyrir hverja innheimtubréfslínu sem inniheldur viðskiptamannafærslu. Hægt er að fá yfirlit yfir færslur innheimtubréfa fyrir ákveðinn viðskiptamann.    
1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar 5.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Viðskiptavinir** og velja síðan viðkomandi tengil.  
2. Opna skal viðeigandi viðskiptamannaspjald og veljið síðan aðgerðina **fjárhagsfærslur**.
3. Á síðunni **Færslur í viðskiptamannabók** er smellt er á línuna með bókarfærslunni sem á að skoða innheimtubréfafærslur fyrir og síðan er smellt á **Innheimtubréf/Vaxtafærslur**.

## Margir vextir

[!INCLUDE [multiple-interest-rates-def](includes/multiple-interest-rates-def.md)]Frekari upplýsingar eru í [Setja upp marga vexti](finance-how-to-set-up-multiple-interest-rates.md).  

## Sjá einnig

[Setja upp skilmála og stig innheimtubréfa](finance-setup-reminders.md)  
[Setja upp vaxtaskilmála](finance-setup-finance-charges.md)  
[Stjórnun skulda](receivables-manage-receivables.md)  
[Sala](sales-manage-sales.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
