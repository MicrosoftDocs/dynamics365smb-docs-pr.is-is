---
title: Setja upp bókun millifyrirtækjafærslu
description: 'Stofna lánardrottna og viðskiptamenn millifyrirtækis sem svokallaða millifyrirtækjafélaga, og setja upp bókhaldslykil millifyrirtækis.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'IC, group, consolidation, affiliate, subsidiary'
ms.search.form: '605, 620, 602, 603, 601, 600, 652, 653, 606, 607, 609, 608, 621'
ms.date: 03/09/2022
ms.author: edupont
---
# Setja upp bókun millifyrirtækjafærslu

Bókanir innan samstæðu gerir bókhaldsvinnu fyrir tvö eða fleiri fyrirtæki auðvelt verk fyrir miðstýrða fjármáladeild og bókara í fyrirtækjum millifyrirtækjafélaga. Til að senda viðskipti (til dæmis sölubókarlínu) frá einu fyrirtæki og láta stofna samsvarandi viðskipti (til dæmis innkaupabókarlínu) í fyrirtækisfélaganum þurfa fyrirtækin að koma sér saman um sameiginlegan bókhaldslykil og víddir sem nota í viðskiptum milli fyrirtækjanna. Bókhaldslykillinn milli fyrirtækja gæti til dæmis verið einfölduð útgáfa af bókhaldslykli móðurfyrirtækisins. Hvert fyrirtæki varpar heildarbókhaldslykli sínum á sameiginlega bókhaldslykilinn milli fyrirtækja, og hvert fyrirtæki varpar víddum sínum á víddirnar milli fyrirtækja.  

Einnig þarf að setja upp MF-félagakóða fyrir hvert [!INCLUDE [prod_short](includes/prod_short.md)] fyrirtæki, sem öll fyrirtækin þurfa að samþykkja og síðan úthluta þeim til viðskiptamanna- og lánardrottnaspjalda.  

Ef MF-línur eru stofnaðar eða mótteknar er hægt að nota eigin vörunúmer eða setja upp vörunúmer félagans fyrir hverja vöru, annað hvort í **Lánardr. vörunr.** reitinn eða í **Algengt vörunr.** á vöruspjaldinu. Einnig má nota **Vörutilvísun** aðgerðina: Til að varpa vörunúmerin á skjalinu í lýsingar þínar á vörum millifyrirtækjafélaga, skal opna kortið fyrir hverja vöru, og velja síðan **Tilvísanir** aðgerð til að setja upp tilvísanir á milli þinna vörulýsinga og þess sem tilheyrir millifyrirtækjafélaga. Frekari upplýsingar er að finna í [Nota vörutilvísanir](inventory-how-use-item-cross-refs.md).

Ef gerðar verða sölufærslur milli fyrirtækja sem innihalda forða þarf að fylla út reitinn **Nr. innk.reikn. MF-félaga** á forðaspjaldi fyrir hvern viðkomandi forða. Þetta er númer fjárhagsreikningsins milli fyrirtækja sem magnið fyrir þennan forða verður bókað í fyrirtækisfélaganum. Frekari upplýsingar eru í [Setja upp tilföng](projects-how-setup-resources.md).

> [!NOTE]
> Innkaupafærslur milli fyrirtækja sem innihalda tilföng, eignir og vörugjöld eru ekki studdar að fullu. Í fyrirtæki millifyrirtækjafélaga verður reiturinn **Línugerð** auður í innkaupaskjalslínum sem innihalda þessar einingar. Uppfæra þarf reitinn handvirkt.

## Samþykkja færslur sjálfkrafa frá millifyrirtækjafélögum

2022 útgáfubylgja 1 kynnti nýja síðu **Uppsetning samstæðu** sem getur flýtt fyrir úrvinnslu færslna hjá millifyrirtækjafélögum. Síðan gerir þér kleift að tilgreina hvort þetta fyrirtæki búi sjálfkrafa til færslubókarlínur sem byggja á bókunum millifyrirtækjafélaga af síðunni **MF-færslubók**. Færslubókarlínur eru stofnaðar fyrir þig en ekki bókaðar. Hægt er að nota eftirfarandi reiti á nýju uppsetningarsíðu samstæðufyrirtækja til að tilgreina hvar á að stofna mótteknar færslubókarfærslur innan samstæðu:

* **Sjálfgefið sniðmát MF–færslubókar**
* **Sjálfgefin runumyndun fyrir MF–færslubók**

> [!NOTE]
> Ef fyrirtækið þitt notaði eiginleika innan samstæðu í [!INCLUDE [prod_short](includes/prod_short.md)] á undan 2022 útgáfutímabili 1 til að samþykkja færslur sjálfkrafa þarf stjórnandinn þinn að kveikja á eiginleikanum **Samþykkja almennar færslubókarfærslur innan samstæðu sjálfkrafa** á síðunni **Eiginleikastjórnun**.

## Að setja upp fyrirtæki fyrir samstæðufærslur

Þessir reitir sem á að fylla út eru mismunandi eftir því hvort stjórnandinn hafi kveikt á eiginleikauppfærslunni **Ný upplifun söluverðlagningar**.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Uppsetning samstæðu** og velja síðan viðkomandi tengil.  
2. Á síðunni **Uppsetning samstæðu** skal fylla út reitina. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## Uppsetning millifyrirtækjafélaga

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Millifyrirtækjafélagar** og velja síðan viðkomandi tengil.
2. Valið er **Nýtt** aðgerð.
3. Á síðunni **Millifyrirtækjafélagi** skal fylla út reitina eins og þörf krefur. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Endurtaka skal skref 2 og 3 fyrir öll önnur fyrirtæki sem eru hluti af þessari uppsetningu samstæðu.

> [!NOTE]
> Á [!INCLUDE[prod_short](includes/prod_short.md)] Online er ekki hægt að nota skráarstaðsetningar til að flytja færslur til samstarfsaðila þar sem [!INCLUDE[prod_short](includes/prod_short.md)] hefur ekki aðgang að staðbundna netinu þínu. Ef þú velur **Staðsetning skráar** í reitnum **Flutningsgerð**, er **Möppuslóð** ekki í boði. Þess í stað er skránni hlaðið niður í niðurhalsmöppuna á tölvunni þinni. Þú sendir síðan skrána til einhvers í samstarfsfyrirtækinu, til dæmis í tölvupósti. Við mælum með því að þú notir **Tölvupóstur** í staðinn til að fá beinna samband.

> [!NOTE]
> Fyrir samstæðubókanir, þegar kveikt hefur verið á **Samþykkja færslur sjálfkrafa** á síðunni **Spjald millifyrirtækjafélaga** mun [!INCLUDE[prod_short](includes/prod_short.md)] fela viðvörunarboð um innkaupareikninga sem tvítaka upprunalega innkaupapöntun. Því er mikilvægt að vera með viðskiptaferli til að stjórna tvítekningum. Til dæmis með því að eyða slíkum innkaupapöntunum þegar innkaupareikningurinn berst frá millifyrirtækjafélaga.


## Hvernig á að: Setja upp lánardrottna og viðskiptamenn millifyrirtækis

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Lánardrottnar** og síðan velja viðkomandi tengil.
2. Að öðrum kosti geturðu nálgast lánardrottinn frá reitnum **Lánardrottinn nr.** á síðunni **Millifyrirtækjafélagi**.
3. Opna spjaldið fyrir lánardrottinn sem er millifyrirtækjafélagi. Nánari upplýsingar eru í [Skráning nýrra lánardrottna](purchasing-how-register-new-vendors.md).
4. Í reitnum **Kóði millifyrirtækjafélaga** er valinn viðeigandi kóði fyrir millifyrirtækjafélaga.
5. Endurtaka skref 1 til 4 fyrir viðskiptamenn.

## Bókhaldslykill milli fyrirtækja er settur upp.

Til að hópur fyrirtækja geti búið til færslur á milli fyrirtækja þarf hann að koma sér saman um bókhaldslykil sem notaður verður sem sameiginleg viðmiðun. Félagarnir þurfa að koma sér saman um reikningsnúmerin sem allir nota þegar færslur milli fyrirtækja eru stofnaðar. Dæmi: móðurfyrirtæki hópsins stofnar einfaldaða útgáfu af bókhaldslykli sínum, flytur hann síðan í XML-skrá sem það dreifir á hvert fyrirtæki í hópnum.  

Ef bókhaldslykill fyrir fyrirtækið þitt skilgreinir bókhaldslykil innan samstæðu fyrir fyrirtæki samstarfsaðila skal fylgja ferlinu sem lýst er í [Að setja upp skilgreiningu bókhaldslykils milli fyrirtækja](intercompany-how-setup.md#to-set-up-the-intercompany-chart-of-accounts).  

Ef fyrirtækið þitt er dótturfyrirtæki og hefur fengið XML-skrá með bókhaldslykli sem hópurinn notar sem sameiginlega viðmiðun er þessari aðferð fylgt [Hvernig á að flytja inn Bókhaldslykill milli fyrirtækja](intercompany-how-setup.md#to-import-the-intercompany-chart-of-accounts).  

### Til að setja upp bókhaldslykil milli fyrirtækja

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **MF-bókhaldslykill** og velja síðan viðkomandi tengil.
2. Á síðunni **MF-bókhaldslyklar** skal færa inn hvern reikning í línu á síðunni.  
3. Ef MF-bókhaldslykillinn verður eins og eða svipaður og venjulegi bókhaldslykillinn er hægt að láta fylla síðuna út sjálfkrafa með því að velja **Afrita frá bókhaldslykli** aðgerðina. Hægt er að breyta nýju línunni eins og þurfa þykir.

### MF-bókhaldslykill er fluttur út

Til að leyfa millifyrirtækjafélögum þínum að flytja inn skilgreinandi bókhaldslykilinn, verður að flytja hann út í skrá.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **MF-bókhaldslykill** og velja síðan viðkomandi tengil.
2. Á síðunni **MF-bókhaldslyklar** skal velja aðgerðina **Flytja út** og síðan velja hnappinn **Vista**.
3. Skrárheitið og staðsetningin þar sem vista á XML-skrána eru valin og síðan smellt á **Vista**.  

### Bókhaldslykill milli fyrirtækja fluttur inn:  

Þegar til er skrá sem skilgreinir MF-bókhaldslykilinn, geta millifyrirtækjafélagar flutt hana inn til að vera vissir um að hafa sama lykilinn.  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **MF-bókhaldslykill** og velja síðan viðkomandi tengil.  
2. Á síðunni **MF-bókhaldslyklar** skal velja aðgerðina **Flytja inn**.  
3. Skrárheiti og staðsetning XML-skrárinnar eru tilgreind og smellt á **Opna**.  

Síðan **MF-bókhaldslykill** er fylltur út með nýjum eða breyttum fjárhagsreikningslínum samkvæmt MF-bókhaldslyklinum í skránni. Allar fyrirliggjandi, óskyldar línur á síðunni haldast óbreyttar.

### Til að varpa MF-bókhaldslykli á bókhaldslykil fyrirtækisins.  

Eftir að MF-bókhaldslykill sem millifyrirtækjafélagar hafa samþykkt að nota hefur verið skilgreindur eða fluttur inn, þarf að tengja hvern fjárhagsreikning millifyrirtækja við einn af fjárhagsreikningum fyrirtækisins. Á síðunni **MF-bókhaldslykill** er skilgreint hvernig fjárhagsreikningar milli fyrirtækja í færslum á innleið verða túlkaðir sem reikningar í bókhaldslykli fyrirtækisins.

Ef reikningar í bókhaldslykli milli fyrirtækja hafa sömu reikningsnúmer og samsvarandi reikningar í bókhaldslyklinum er hægt að varpa reikningunum.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **MF-bókhaldslykill** og velja síðan viðkomandi tengil.  
2. Línurnar sem á að varpa sjálfkrafa eru valdar og svo er valin aðgerðin **Varpa á reikning með sama nr.**.  
3. Fyrir hvern fjárhagsreikning milli fyrirtækja sem ekki var varpað sjálfkrafa, skal fylla í reitinn **Varpa á Fjárhagsreikning nr.**.  

## Hvernig á að setja upp sjálfgefna fjárhagsreikninga samstarfsfyrirtækja  

Þegar sölu- eða innkaupalína milli fyrirtækja er stofnuð til að senda sem færslu á útleið er færður inn reikningur úr MF-bókhaldslykli sem notaður verður sem sjálfgefinn reikningur sem upphæðin ætti að bókast á í fyrirtæki félagans. Á síðunni **Bókhaldslykill** er hægt að tilgreina sjálfgefinn fjárhagsreikning MF-félaga fyrir reikninga sem reglulega eru notaðir í MF-sölu- eða innkaupalínum á útleið. Til dæmis er hægt að færa inn samsvarandi safnreikning lánardrottna úr MF-bókhaldsreikningi fyrir safnreikninga viðskiptamanna.  

Þegar fjárhagsreikningur er síðan færður inn í reitinn **Nr. Mótreiknings** í línu milli fyrirtækja með **MF-félaga** í reitnum **Tegund reiknings** er sjálfkrafa fyllt í reitinn **MF-félagi fjárhagsreikningur**.  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Bókhaldslykill** og velja síðan viðkomandi tengil.  
2. Á línuna fyrir fjárhagsreikning sem er notaður fyrir millifyrirtækjafærslur, í reitnum **Sjálfgefinn fjárhagsreikningur MP félaga** skal færa inn MF-fjárhagsreikninginn sem félaginn á að bóka í við bókun í fjárhagsreikninga í línunni.  
3. Skref 2 er endurtekið fyrir hvern reikning sem oft er færður inn í reitinn **Mótreikningur nr.** í línu í færslubók eða fylgiskjali milli fyrirtækja.

## Uppsetning vídda millifyrirtækja

Ef milli-fyrirtækjafélagar vilja geta skiptst á færslum með víddum þurfa þeir allir að samþykkja milli-fyrirtækjavíddirnar sem allir koma til með að nota. Dæmi: móðurfyrirtæki hópsins stofnar einfaldaða útgáfu af eigin safni af víddum, flytur hana síðan í XML-skrá sem það dreifir á hvert fyrirtæki í hópnum. Hvert dótturfyrirtæki flytur síðan XML-skrána inni í töfluna **MF-vídd** og varpar milli-fyrirtækjavíddum á víddirnar í eigin **vídda** síðu.  

> [!NOTE]
> Hvert fyrirtæki í [!INCLUDE [prod_short](includes/prod_short.md)] verður að varpa víddunum í MF-víddir fyrir skjöl á útleið og varpa MF-víddum á sínar eigin víddir fyrir skjöl á innleið. Þessi vörpun hjálpar til við að tryggja samræmi þvert á fyrirtæki. Frekari upplýsingar eru í hlutanum [MF-víddum varpað á víddir fyrirtækisins](#to-map-intercompany-dimensions-to-your-companys-dimensions).

Ef fyrirtækið þitt er móðurfyrirtækið og er með skilgreinandi safn milli-fyrirtækjavídda sem hópurinn notar sem sameiginlega viðmiðun, er þessari aðferð fylgt [Skilgreining vídda millifyrirtækja](intercompany-how-setup.md#to-define-the-intercompany-dimensions).

Ef fyrirtæki þitt er dótturfyrirtæki og þú færð XML-skrá með MF-víddum sem hópurinn notar sem sameiginlega viðmiðun er þessari aðferð fylgt [Hvernig á að flytja inn millifyrirtækjavíddir](intercompany-how-setup.md#to-import-the-intercompany-dimensions).

### Skilgreina MF-víddir

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **MF-víddir** og velja síðan viðkomandi tengil.  
2. Á síðunni **MF-víddir** er hver vídd er færð inn í línu á síðunni.

    Ef MF-víddirnar verða eins eða svipaðar og víddir fyrirtækisins er hægt að fylla síðuna sjálfkrafa út með því að nota aðgerðina **Afrita úr víddum** og breyta síðan línunum sem verða til.  
3. Velja skal **Flytja út** aðgerðina til að flytja MF-víddirnar út í XML-skrá til dreifingar til fyrirtækisfélaga.  
4. Skrárheitið og staðsetningin þar sem vista á XML-skrána eru valin og síðan smellt á **Vista**.  

### Millifyrirtækjavíddir fluttar inn  

Þegar til er skrá sem inniheldur skilgreinandi MF-víddir, geta millifyrirtækjafélagar flutt hana inn til að vera vissir um að hafa sömu víddirnar.  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **MF-víddir** og velja síðan viðkomandi tengil.  
2. Á síðunni **MF-víddir** veljið aðgerðina **Flytja inn**.  
3. Skrárheiti og staðsetning XML-skrárinnar eru tilgreind og smellt á **Opna**.  

Línurnar á síðunni **MF-víddir** og síðunni **MF-víddargildi** eru fluttar inn.  

### MF-víddum varpað á víddir fyrirtækisins:

Þegar búið er að skilgreina eða flytja inn víddunum sem þú og milli-fyrirtækjafélagar hafa samþykkt að nota þarf að tengja hverja vídd milli fyrirtækja við eina af víddum fyrirtækisins og öfugt. Á síðunni **MF-víddir** er skilgreint hvernig MF-víddir í *færslum á innleið* verða túlkaðar sem víddir í víddatöflu fyrirtækisins. Á síðunni **Víddir** er tilgreint hvernig víddirnar verði túlkaðar sem MF-víddir í *færslum á útleið*.

Ef einhver af víddunum milli fyrirtækja hefur sama kóta og samsvarandi víddir í víddatöflu fyrirtækisins er hægt að láta forritið varpa víddunum sjálfkrafa, og þá er hægt að varpa reikningunum sjálfkrafa.  

Í eftirfarandi skrefum er MF-víddum fyrst varpað í víddir fyrir skjöl á innleið á síðunni **MF-víddir**. Síðan er víddum varpað í MF-víddir fyrir skjöl á útleið á síðunni **Víddir**.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **MF-víddir** og velja síðan viðkomandi tengil.
2. Á síðunni **MF-víddir** eru línurnar sem á að varpa sjálfkrafa eru valdar og svo er **Varpa á víddir með sama kóða** aðgerðin valin.
3. Fyrir hverja vídd milli fyrirtækja sem er ekki varpað sjálfkrafa, skal fylla út í reitinn **Varpa á víddarkóða**.

    Hugsanlega þarf að bæta reitnum við yfirlitið. Frekari upplýsingar eru í [Sérstilling verksvæðis](ui-personalization-user.md).
4. Veljið aðgerðina **MF-víddargildi**.
5. Á síðunni **MF-víddargildi** er reiturinn **Varpa á víddargildiskóða** fylltur út.

    Halda áfram að varpa víddum á MF-víddir með því að framkvæma svipuð skref.
6. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Víddir** og velja síðan viðkomandi tengil.
7. Á síðunni **Víddir** eru línurnar sem á að varpa sjálfkrafa eru valdar og svo er **Varpa á MF-víddir með sama kóða** aðgerðin valin.
8. Fyrir hverja vídd milli fyrirtækja sem er ekki varpað sjálfkrafa, skal fylla út í reitinn **Varpa á MF víddargildiskóða**.
9. Velja aðgerðina **Víddargildi**.
10. Á síðunni **Víddargildi** er reiturinn **Varpa á MF-víddargildiskóða** fylltur út.

## Sjá einnig

[Vinna með millifyrirtækjafærslur](intercompany-manage.md)  
[Fjármál](finance.md)  
[Uppsetning Fjármála](finance-setup-finance.md)  
[Vinna í færslubókum](ui-work-general-journals.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]