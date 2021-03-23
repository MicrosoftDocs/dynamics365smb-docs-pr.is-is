---
title: Setja upp Bókun millifyrirtækjafærslu | Microsoft Docs
description: Stofna lánardrottna og viðskiptamenn millifyrirtækis sem svokallaða millifyrirtækjafélaga, og setja upp bókhaldslykil millifyrirtækis.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: IC, group, consolidation, affiliate, subsidiary
ms.date: 12/15/2020
ms.author: edupont
ms.openlocfilehash: ca8cfec87e0e315562dceca0a48e29b2f1fa577c
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5389025"
---
# <a name="set-up-intercompany"></a>Uppsetning milli fyrirtækja

Til að senda viðskipti (til dæmis sölubókarlínu) frá einu fyrirtæki og láta stofna samsvarandi viðskipti (til dæmis innkaupabókarlínu) í fyrirtækisfélaganum þurfa fyrirtækin að koma sér saman um sameiginlegan bókhaldslykil og víddir sem nota á í viðskiptum milli fyrirtækjanna. Bókhaldslykillinn milli fyrirtækja gæti til dæmis verið einfölduð útgáfa af bókhaldslykli móðurfyrirtækisins. Hvert fyrirtæki varpar heildarbókhaldslykli sínum á sameiginlega bókhaldslykilinn milli fyrirtækja, og hvert fyrirtæki varpar víddum sínum á víddirnar milli fyrirtækja.  

Einnig þarf að setja upp MF-félagakóða fyrir hvern fyrirtæki félaga, sem öll fyrirtækin þurfa að samþykkja, og síðan úthluta þeim til viðskiptamanna- og lánardrottnaspjalda með því fylla út í reitinn **MF-félagakóði**.  

Ef MF-línur eru stofnaðar eða mótteknar er hægt að nota eigin vörunúmer eða setja upp vörunúmer félagans fyrir hverja vöru, annað hvort í **Lánardr. vörunr.** reitinn eða í **Algengt vörunr.** á vöruspjaldinu. Einnig má nota **Vörumillivísun** aðgerðina: Til að varpa vörunúmerin á skjalinu í lýsingar þínar á vörum millifyrirtækjafélaga, skal opna kortið fyrir hverja vöru, og velja síðan **Millivísanir** aðgerð til að setja upp millivísanir á milli þinna vörulýsinga og þess sem tilheyrir millifyrirtækjafélaga. Frekari upplýsingar er að finna í [Nota millivísanir vöru](inventory-how-use-item-cross-refs.md). 

Ef gerðar verða sölufærslur milli fyrirtækja sem innihalda forða þarf að fylla út reitinn **Nr. innk.reikn. MF-félaga** á forðaspjaldi fyrir hvern viðkomandi forða. Þetta er númer fjárhagsreikningsins milli fyrirtækja sem magnið fyrir þennan forða verður bókað í fyrirtækisfélaganum. Frekari upplýsingar eru í [Setja upp tilföng](projects-how-setup-resources.md).

## <a name="to-set-up-companies-for-intercompany-transactions"></a>Setja upp fyrirtæki fyrir millifyrirtækjafærslur
1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Stofngögn** og veldu síðan tengda tengilinn.  
2. Á síðunni **Fyrirtækjaupplýsingar** skal fylla inn í reitina **MF-félagakóði**, **MF-innhólfstegund**. og **MF-innhólfsupplýsingar**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-set-intercompany-partners"></a>Setja millifyrirtækjafélaga
1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Millifyrirtækjafélagar** og veldu síðan tengda tengilinn.
2. Valið er **Nýtt** aðgerð.
3. Á síðunni **Millifyrirtækjafélagi** skal fylla út reitina eins og þörf krefur.

> [!NOTE]
> Á [!INCLUDE[prod_short](includes/prod_short.md)] Online er ekki hægt að nota skráarstaðsetningar til að flytja færslur til samstarfsaðila þar sem [!INCLUDE[prod_short](includes/prod_short.md)] hefur ekki aðgang að staðbundna netinu þínu. Ef þú velur **Staðsetning skráar** í reitnum **Flutningsgerð**, er **Möppuslóð** ekki í boði. Þess í stað er skránni hlaðið niður í niðurhalsmöppuna á tölvunni þinni. Þú sendir síðan skrána til einhvers í samstarfsfyrirtækinu, til dæmis í tölvupósti. Við mælum með því að þú notir **Tölvupóstur** í staðinn til að fá beinna samband.

## <a name="to-set-up-intercompany-vendors-and-intercompany-customers"></a>Hvernig á að: Setja upp lánardrottna og viðskiptamenn millifyrirtækis
1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Lánardrottnar** og veldu síðan tengda tengilinn.
2. Að öðrum kosti geturðu nálgast lánardrottinn frá reitnum **Lánardrottinn nr.** á síðunni **Millifyrirtækjafélagi**.
3. Opna spjaldið fyrir lánardrottinn sem er millifyrirtækjafélagi. Nánari upplýsingar eru í [Skráning nýrra lánardrottna](purchasing-how-register-new-vendors.md).
4. Í reitnum **Kóði millifyrirtækjafélaga** er valinn viðeigandi kóði fyrir millifyrirtækjafélaga.
5. Endurtaka skref 1 til 4 fyrir viðskiptamenn.

## <a name="to-set-up-intercompany-charts-of-accounts"></a>Bókhaldslykill milli fyrirtækja er settur upp.
Til að hópur fyrirtækja geti búið til færslur á milli fyrirtækja þarf hann að koma sér saman um bókhaldslykil sem notaður verður sem sameiginleg viðmiðun. Félagarnir þurfa að koma sér saman um reikningsnúmerin sem allir nota þegar færslur milli fyrirtækja eru stofnaðar. Dæmi: móðurfyrirtæki hópsins stofnar einfaldaða útgáfu af bókhaldslykli sínum, flytur bókhaldslykil milli fyrirtækja úr gagnagrunninum í XML-skrá og dreifir henni til einstakra fyrirtækja í hópnum.  

Ef fyrirtækið þitt er móðurfyrirtækið og er með skilgreinandi bókhaldslykil milli fyrirtækja sem hópurinn þinn notar sem sameiginlega viðmiðun, skal fylgja ferlinu [Að setja upp skilgreinandi bókhaldslykla milli fyrirtækja](intercompany-how-setup.md#to-set-up-the-defining-intercompany-chart-of-accounts).  

Ef fyrirtækið þitt er dótturfyrirtæki og hefur fengið XML-skrá með bókhaldslykli sem hópurinn notar sem sameiginlega viðmiðun er þessari aðferð fylgt [Hvernig á að flytja inn Bókhaldslykill milli fyrirtækja](intercompany-how-setup.md#to-import-the-intercompany-chart-of-accounts).  

### <a name="to-set-up-the-defining-intercompany-chart-of-accounts"></a>Skilgreinandi bókhaldslykill milli fyrirtækja er settur upp.
1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **MF-bókhaldslykill** og veldu síðan tengda tengilinn.
2. Á síðunni **MF-bókhaldslyklar** skal færa inn hvern reikning í línu á síðunni.  
3. Ef MF-bókhaldslykillinn verður eins og eða svipaður og venjulegi bókhaldslykillinn er hægt að láta fylla síðuna út sjálfkrafa með því að velja **Afrita frá bókhaldslykli** aðgerðina. Hægt er að breyta nýju línunni eins og þurfa þykir.

### <a name="to-export-an-intercompany-chart-of-accounts"></a>MF-bókhaldslykill er fluttur út
Til að leyfa millifyrirtækjafélögum þínum að flytja inn skilgreinandi bókhaldslykilinn, verður að flytja hann út í skrá.      
1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **MF-bókhaldslykill** og veldu síðan tengda tengilinn.
2. Á síðunni **MF-bókhaldslyklar** skal velja aðgerðina **Flytja út** og síðan velja hnappinn **Vista**.
3. Skrárheitið og staðsetningin þar sem vista á XML-skrána eru valin og síðan smellt á **Vista**.  

### <a name="to-import-the-intercompany-chart-of-accounts"></a>Bókhaldslykill milli fyrirtækja fluttur inn:  
Þegar til er skrá sem inniheldur skilgreinandi MF-bókhaldslykilinn, geta millifyrirtækjafélagar flutt hana inn til að vera vissir um að hafa sama lykilinn.  
1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Bókunarlykill milli fyrirtækja** og veldu síðan tengda tengilinn.  
2. Á síðunni **MF-bókhaldslyklar** skal velja aðgerðina **Flytja inn**.  
3. Skrárheiti og staðsetning XML-skrárinnar eru tilgreind og smellt á **Opna**.  

Síðan **MF-bókhaldslykill** er fylltur út með nýjum eða breyttum fjárhagsreikningslínum samkvæmt MF-bókhaldslyklinum í skránni. Allar fyrirliggjandi, óskyldar línur á síðunni haldast óbreyttar.

### <a name="to-map-the-intercompany-chart-of-accounts-to-your-companys-chart-of-accounts"></a>Til að varpa MF-bókhaldslykli á bókhaldslykil fyrirtækisins.  
Eftir að MF-bókhaldslykill sem millifyrirtækjafélagar hafa samþykkt að nota hefur verið skilgreindur eða fluttur inn, þarf að tengja hvern fjárhagsreikning millifyrirtækja við einn af fjárhagsreikningum fyrirtækisins. Á síðunni **MF-bókhaldslykill** er skilgreint hvernig fjárhagsreikningar milli fyrirtækja í færslum á innleið verða túlkaðir sem reikningar í bókhaldslykli fyrirtækisins.

Ef reikningar í bókhaldslykli milli fyrirtækja hafa sömu reikningsnúmer og samsvarandi reikningar í bókhaldslyklinum er hægt að varpa reikningunum.

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **MF-bókhaldslykill** og veldu síðan tengda tengilinn.  
2. Línurnar sem á að varpa sjálfkrafa eru valdar og svo er valin aðgerðin **Varpa á reikning með sama nr.**.  
3. Fyrir hvern fjárhagsreikning milli fyrirtækja sem ekki var varpað sjálfkrafa, skal fylla í reitinn **Varpa á Fjárhagsreikning nr.**.  

## <a name="to-set-up-default-intercompany-partner-general-ledger-accounts"></a>Hvernig á að setja upp sjálfgefna fjárhagsreikninga samstarfsfyrirtækja  
Þegar sölu- eða innkaupalína milli fyrirtækja er stofnuð til að senda sem færslu á útleið er færður inn reikningur úr MF-bókhaldslykli sem notaður verður sem sjálfgefinn reikningur sem upphæðin ætti að bókast á í fyrirtæki félagans. Á síðunni **Bókhaldslykill** er hægt að tilgreina sjálfgefinn fjárhagsreikning MF-félaga fyrir reikninga sem oft eru notaðir í MF-sölu- eða innkaupalínum á útleið. Til dæmis er hægt að færa inn samsvarandi safnreikning lánardrottna úr MF-bókhaldsreikningi fyrir safnreikninga viðskiptamanna.  

Þegar fjárhagsreikningur er síðan færður inn í reitinn **Nr. Mótreiknings** í línu milli fyrirtækja með **MF-félaga** í reitnum **Tegund reiknings** er sjálfkrafa fyllt í reitinn **MF-félagi fjárhagsreikningur**.  

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Bókhaldslykill** og veldu síðan tengda tengilinn.  
2. Á línuna fyrir fjárhagsreikning sem er notaður fyrir millifyrirtækjafærslur, í reitnum **Sjálfgefinn fjárhagsreikningur MP félaga** skal færa inn MF-fjárhagsreikninginn sem félaginn á að bóka í við bókun í fjárhagsreikninga í línunni.  
3. Skref 2 er endurtekið fyrir hvern reikning sem oft er færður inn í reitinn **Mótreikningur nr.** í línu í færslubók eða fylgiskjali milli fyrirtækja.

## <a name="to-set-up-intercompany-dimensions"></a>Uppsetning vídda millifyrirtækja

Ef milli-fyrirtækjafélagar vilja skiptast á færslum með víddum þurfa þeir allir að samþykkja milli-fyrirtækjavíddirnar sem allir koma til með að nota. Dæmi: móðurfyrirtæki hópsins stofnar einfaldaða útgáfu af víddum sínum, flytur milli-fyrirtækjavíddir í XML-skrá og dreifir henni til einstakra fyrirtækja í hópnum. Hvert dótturfyrirtæki flytur síðan XML-skrána inni í töfluna **MF-vídd** og varpar milli-fyrirtækjavíddum á víddirnar í eigin **vídda** síðu.  

> [!NOTE]
> Hvert fyrirtæki í [!INCLUDE [prod_short](includes/prod_short.md)] verður að varpa víddunum í MF-víddir fyrir skjöl á útleið og varpa MF-víddum á sínar eigin víddir fyrir skjöl á innleið. Þessi vörpun hjálpar til við að tryggja samræmi þvert á fyrirtæki. Frekari upplýsingar eru í hlutanum [MF-víddum varpað á víddir fyrirtækisins](#to-map-intercompany-dimensions-to-your-companys-dimensions).

Ef fyrirtækið þitt er móðurfyrirtækið og er með skilgreinandi safn milli-fyrirtækjavídda sem hópurinn notar sem sameiginlega viðmiðun, er þessari aðferð fylgt [Skilgreining vídda millifyrirtækja](intercompany-how-setup.md#to-define-the-intercompany-dimensions).

Ef fyrirtæki þitt er dótturfyrirtæki og þú færð XML-skrá með MF-víddum sem hópurinn notar sem sameiginlega viðmiðun er þessari aðferð fylgt [Hvernig á að flytja inn millifyrirtækjavíddir](intercompany-how-setup.md#to-import-the-intercompany-dimensions).

### <a name="to-define-the-intercompany-dimensions"></a>Skilgreina MF-víddir
1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **MF-víddir** og veldu síðan tengda tengilinn.  
2. Á síðunni **MF-víddir** er hver vídd er færð inn í línu á síðunni.

    Ef MF-víddirnar verða eins eða svipaðar og víddir fyrirtækisins er hægt að fylla síðuna sjálfkrafa út með því að nota aðgerðina **Afrita úr víddum** og breyta síðan línunum sem verða til.  
3. Velja skal **Flytja út** aðgerðina til að flytja MF-víddirnar út í XML-skrá til dreifingar til fyrirtækisfélaga.  
4. Skrárheitið og staðsetningin þar sem vista á XML-skrána eru valin og síðan smellt á **Vista**.  

### <a name="to-import-the-intercompany-dimensions"></a>Millifyrirtækjavíddir fluttar inn  
Þegar til er skrá sem inniheldur skilgreinandi MF-víddir, geta millifyrirtækjafélagar flutt hana inn til að vera vissir um að hafa sömu víddirnar.  
1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **MF-víddir** og veldu síðan tengda tengilinn.  
2. Á síðunni **MF-víddir** veljið aðgerðina **Flytja inn**.  
3. Skrárheiti og staðsetning XML-skrárinnar eru tilgreind og smellt á **Opna**.  

Línurnar á síðunni **MF-víddir** og síðunni **MF-víddargildi** eru fluttar inn.  

### <a name="to-map-intercompany-dimensions-to-your-companys-dimensions"></a>MF-víddum varpað á víddir fyrirtækisins:
Þegar búið er að skilgreina eða flytja inn víddunum sem þú og milli-fyrirtækjafélagar hafa samþykkt að nota þarf að tengja hverja vídd milli fyrirtækja við eina af víddum fyrirtækisins og öfugt. Á síðunni **MF-víddir** er skilgreint hvernig MF-víddir í *færslum á innleið* verða túlkaðar sem víddir í víddatöflu fyrirtækisins. Á síðunni **Víddir** er tilgreint hvernig víddirnar verði túlkaðar sem MF-víddir í *færslum á útleið*.

Ef einhver af víddunum milli fyrirtækja hefur sama kóta og samsvarandi víddir í víddatöflu fyrirtækisins er hægt að láta forritið varpa víddunum sjálfkrafa, og þá er hægt að varpa reikningunum sjálfkrafa.  

Í eftirfarandi skrefum er MF-víddum fyrst varpað í víddir fyrir skjöl á innleið á síðunni **MF-víddir**. Síðan er víddum varpað í MF-víddir fyrir skjöl á útleið á síðunni **Víddir**.

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **MF-víddir** og veldu síðan tengda tengilinn.
2. Á síðunni **MF-víddir** eru línurnar sem á að varpa sjálfkrafa eru valdar og svo er **Varpa á víddir með sama kóða** aðgerðin valin.
3. Fyrir hverja vídd milli fyrirtækja sem er ekki varpað sjálfkrafa, skal fylla út í reitinn **Varpa á víddarkóta**.

    Hugsanlega þarf að bæta reitnum við yfirlitið. Frekari upplýsingar eru í [Sérstilling verksvæðis](ui-personalization-user.md).
4. Veljið aðgerðina **MF-víddargildi**.
5. Á síðunni **MF-víddargildi** er reiturinn **Varpa á víddargildiskóða** fylltur út.

    Halda áfram að varpa víddum á MF-víddir með því að framkvæma svipuð skref.
6. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Víddir** og veldu síðan tengda tengilinn.
7. Á síðunni **Víddir** eru línurnar sem á að varpa sjálfkrafa eru valdar og svo er **Varpa á MF-víddir með sama kóða** aðgerðin valin.
8. Fyrir hverja vídd milli fyrirtækja sem er ekki varpað sjálfkrafa, skal fylla út í reitinn **Varpa á MF víddargildiskóða**.
9. Velja aðgerðina **Víddargildi**.
10. Á síðunni **Víddargildi** er reiturinn **Varpa á MF-víddargildiskóða** fylltur út.

## <a name="see-also"></a>Sjá einnig

[Vinna með millifyrirtækjafærslur](intercompany-manage.md)  
[Fjármál](finance.md)  
[Uppsetning Fjármála](finance-setup-finance.md)  
[Vinna í færslubókum](ui-work-general-journals.md)  
[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]