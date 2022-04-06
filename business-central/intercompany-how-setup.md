---
title: Setja upp bókun millifyrirtækjafærslu
description: Stofna lánardrottna og viðskiptamenn millifyrirtækis sem svokallaða millifyrirtækjafélaga, og setja upp bókhaldslykil millifyrirtækis.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: IC, group, consolidation, affiliate, subsidiary
ms.search.form: 605, 620, 602, 603, 601, 600, 652, 653, 606, 607, 609, 608, 621
ms.date: 03/09/2022
ms.author: edupont
ms.openlocfilehash: 398f5bbbe30730057093f8550cef27a514cbc20a
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2022
ms.locfileid: "8515538"
---
# <a name="set-up-intercompany-transaction-posting"></a>Setja upp bókun millifyrirtækjafærslu

Bókhald innan samstæðu gerir bókhaldsfyrirtæki fyrir tvö eða fleiri fyrirtæki auðveldari verkefni fyrir miðlæga Fjármáladeild og glorified bookkeepers hjá félagasamtökum innan samstæðu. Til að senda viðskipti (til dæmis sölubókarlínu) frá einu fyrirtæki og láta stofna samsvarandi viðskipti (til dæmis innkaupabókarlínu) í fyrirtækisfélaganum þurfa fyrirtækin að koma sér saman um sameiginlegan bókhaldslykil og víddir sem nota í viðskiptum milli fyrirtækjanna. Bókhaldslykillinn milli fyrirtækja gæti til dæmis verið einfölduð útgáfa af bókhaldslykli móðurfyrirtækisins. Hvert fyrirtæki varpar heildarbókhaldslykli sínum á sameiginlega bókhaldslykilinn milli fyrirtækja, og hvert fyrirtæki varpar víddum sínum á víddirnar milli fyrirtækja.  

Einnig verður að setja upp MF-félagakóta fyrir hvert [!INCLUDE [prod_short](includes/prod_short.md)] fyrirtæki, sem er samþykktur af öllum fyrirtækjunum, og tengja það við viðskiptamanna-og lánardrottnaspjöld, eftir því sem við á.  

Ef MF-línur eru stofnaðar eða mótteknar er hægt að nota eigin vörunúmer eða setja upp vörunúmer félagans fyrir hverja vöru, annað hvort í **Lánardr. vörunr.** reitinn eða í **Algengt vörunr.** á vöruspjaldinu. Einnig má nota **Vörutilvísun** aðgerðina: Til að varpa vörunúmerin á skjalinu í lýsingar þínar á vörum millifyrirtækjafélaga, skal opna kortið fyrir hverja vöru, og velja síðan **Tilvísanir** aðgerð til að setja upp tilvísanir á milli þinna vörulýsinga og þess sem tilheyrir millifyrirtækjafélaga. Frekari upplýsingar er að finna í [Nota vörutilvísanir](inventory-how-use-item-cross-refs.md). 

Ef gerðar verða sölufærslur milli fyrirtækja sem innihalda forða þarf að fylla út reitinn **Nr. innk.reikn. MF-félaga** á forðaspjaldi fyrir hvern viðkomandi forða. Þetta er númer fjárhagsreikningsins milli fyrirtækja sem magnið fyrir þennan forða verður bókað í fyrirtækisfélaganum. Frekari upplýsingar eru í [Setja upp tilföng](projects-how-setup-resources.md). 

> [!NOTE]
> Innkaupa-og kostnaðarfærslur milli fyrirtækja sem innihalda forða, eignir og kostnaðarauka eru ekki fyllilega studdar. Í fyrirtæki MF-félagins er **reiturinn Tegund** línu auður í innkaupaskjalslínum sem innihalda þessa aðila. Hægt verður að uppfæra svæðið handvirkt. 

## <a name="to-set-up-a-company-for-intercompany-transactions"></a>Fyrirtæki sett upp fyrir færslur innan samstæðu

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknið, færa inn **Samstæðuuppsetningu** og velja síðan tengda tengilinn.  
2. **Á uppsetningarsíðu** samstæðu er fyllt út í reitina. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

  > [!NOTE]
  > 2022 útgáfubylgja 1 kynnir nýja **Samstæðuuppsetningarsíðu** þannig að einnig er hægt að tilgreina ef fyrirtækið verður að stofna færslubókarlínur sjálfkrafa á grundvelli innleggs frá MF-félaga úr **síðunni MF-færslubók**. Ef fyrirtækið hefur notað áður en þessi losunarbylgja er notuð [!INCLUDE [prod_short](includes/prod_short.md)] þarf að skipta á nýju upplifuninni á **síðu aðgangsstjórnunar**. Fyrir frekari upplýsingar sjá [Auto-Samþykkja færslur fyrir MF-færslubækur](/dynamics365-release-plan/2022wave1/smb/dynamics365-business-central/intercompany-postings-have-auto-accept-transaction-enabled-intercompany-general-journals).

Í útgáfum eldri en 2022 losunarbylgju 1 þarf að fylla út þrjá reiti innan samstæðu á **upplýsingasíðu** fyrirtækisins í staðinn.  

## <a name="to-set-up-intercompany-partners"></a>Uppsetning samstæðufélaga

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Millifyrirtækjafélagar** og velja síðan viðkomandi tengil.
2. Valið er **Nýtt** aðgerð.
3. Á síðunni **Millifyrirtækjafélagi** skal fylla út reitina eins og þörf krefur. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Endurtaka skal þrep 2 til 3 fyrir öll önnur fyrirtæki sem eru hluti af þessari uppsetningu samstæðunnar.

> [!NOTE]
> Á [!INCLUDE[prod_short](includes/prod_short.md)] Online er ekki hægt að nota skráarstaðsetningar til að flytja færslur til samstarfsaðila þar sem [!INCLUDE[prod_short](includes/prod_short.md)] hefur ekki aðgang að staðbundna netinu þínu. Ef þú velur **Staðsetning skráar** í reitnum **Flutningsgerð**, er **Möppuslóð** ekki í boði. Þess í stað er skránni hlaðið niður í niðurhalsmöppuna á tölvunni þinni. Þú sendir síðan skrána til einhvers í samstarfsfyrirtækinu, til dæmis í tölvupósti. Við mælum með því að þú notir **Tölvupóstur** í staðinn til að fá beinna samband.

## <a name="to-set-up-intercompany-vendors-and-intercompany-customers"></a>Hvernig á að: Setja upp lánardrottna og viðskiptamenn millifyrirtækis
1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Lánardrottnar** og síðan velja viðkomandi tengil.
2. Að öðrum kosti geturðu nálgast lánardrottinn frá reitnum **Lánardrottinn nr.** á síðunni **Millifyrirtækjafélagi**.
3. Opna spjaldið fyrir lánardrottinn sem er millifyrirtækjafélagi. Nánari upplýsingar eru í [Skráning nýrra lánardrottna](purchasing-how-register-new-vendors.md).
4. Í reitnum **Kóði millifyrirtækjafélaga** er valinn viðeigandi kóði fyrir millifyrirtækjafélaga.
5. Endurtaka skref 1 til 4 fyrir viðskiptamenn.

## <a name="to-set-up-intercompany-charts-of-accounts"></a>Bókhaldslykill milli fyrirtækja er settur upp.
Til að hópur fyrirtækja geti búið til færslur á milli fyrirtækja þarf hann að koma sér saman um bókhaldslykil sem notaður verður sem sameiginleg viðmiðun. Þú verður að vera sammála samstarfsfyrirtækjunum um reikningsnúmerin sem þú munt öll nota þegar samstæðufærslur eru stofnaðar. Til dæmis stofnar móðurfélag þess flokkinn einfaldaða útgáfu af eigin bókhaldslykli og flytur það síðan yfir í XML-skrá sem það dreifir því til hvers fyrirtækis í flokknum.  

Ef Bókhaldslykill fyrirtækisins skilgreinir bókhaldslykil samstæðu fyrir félagasamstæðu skal fylgja ferlinu sem er lýst í [til að setja upp bókhaldslykil](intercompany-how-setup.md#to-set-up-the-defining-intercompany-chart-of-accounts) samstæðu.  

Ef fyrirtækið þitt er dótturfyrirtæki og hefur fengið XML-skrá með bókhaldslykli sem hópurinn notar sem sameiginlega viðmiðun er þessari aðferð fylgt [Hvernig á að flytja inn Bókhaldslykill milli fyrirtækja](intercompany-how-setup.md#to-import-the-intercompany-chart-of-accounts).  

### <a name="to-set-up-the-defining-intercompany-chart-of-accounts"></a>Skilgreinandi bókhaldslykill milli fyrirtækja er settur upp.
1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **MF-bókhaldslykill** og velja síðan viðkomandi tengil.
2. Á síðunni **MF-bókhaldslyklar** skal færa inn hvern reikning í línu á síðunni.  
3. Ef MF-bókhaldslykillinn verður eins og eða svipaður og venjulegi bókhaldslykillinn er hægt að láta fylla síðuna út sjálfkrafa með því að velja **Afrita frá bókhaldslykli** aðgerðina. Hægt er að breyta nýju línunni eins og þurfa þykir.

### <a name="to-export-an-intercompany-chart-of-accounts"></a>MF-bókhaldslykill er fluttur út
Til að leyfa millifyrirtækjafélögum þínum að flytja inn skilgreinandi bókhaldslykilinn, verður að flytja hann út í skrá.      
1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **MF-bókhaldslykill** og velja síðan viðkomandi tengil.
2. Á síðunni **MF-bókhaldslyklar** skal velja aðgerðina **Flytja út** og síðan velja hnappinn **Vista**.
3. Skrárheitið og staðsetningin þar sem vista á XML-skrána eru valin og síðan smellt á **Vista**.  

### <a name="to-import-the-intercompany-chart-of-accounts"></a>Bókhaldslykill milli fyrirtækja fluttur inn:  
Þegar til er skrá sem skilgreinir MF-bókhaldslykilinn, geta millifyrirtækjafélagar flutt hana inn til að vera vissir um að hafa sama lykilinn.  
1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **MF-bókhaldslykill** og velja síðan viðkomandi tengil.  
2. Á síðunni **MF-bókhaldslyklar** skal velja aðgerðina **Flytja inn**.  
3. Skrárheiti og staðsetning XML-skrárinnar eru tilgreind og smellt á **Opna**.  

Síðan **MF-bókhaldslykill** er fylltur út með nýjum eða breyttum fjárhagsreikningslínum samkvæmt MF-bókhaldslyklinum í skránni. Allar fyrirliggjandi, óskyldar línur á síðunni haldast óbreyttar.

### <a name="to-map-the-intercompany-chart-of-accounts-to-your-companys-chart-of-accounts"></a>Til að varpa MF-bókhaldslykli á bókhaldslykil fyrirtækisins.  
Þegar bókhaldslykill milli fyrirtækja hefur verið skilgreindur eða fluttur inn sem samstæðufélagarnir hafa samþykkt að nota verður að tengja hvern fjárhagsreikning samstæðunnar við einn af fjárhagsreikningum fyrirtækisins. Á síðunni **MF-bókhaldslykill** er skilgreint hvernig fjárhagsreikningar milli fyrirtækja í færslum á innleið verða túlkaðir sem reikningar í bókhaldslykli fyrirtækisins.

Ef reikningar í bókhaldslykli milli fyrirtækja hafa sömu reikningsnúmer og samsvarandi reikningar í bókhaldslyklinum er hægt að varpa reikningunum.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **MF-bókhaldslykill** og velja síðan viðkomandi tengil.  
2. Línurnar sem á að varpa sjálfkrafa eru valdar og svo er valin aðgerðin **Varpa á reikning með sama nr.**.  
3. Fyrir hvern fjárhagslykil í samstæðu sem ekki var varpað á sjálfkrafa skal fylla inn í **reitinn kort-í Reikn.**  

## <a name="to-set-up-default-intercompany-partner-general-ledger-accounts"></a>Hvernig á að setja upp sjálfgefna fjárhagsreikninga samstarfsfyrirtækja  
Þegar sölu- eða innkaupalína milli fyrirtækja er stofnuð til að senda sem færslu á útleið er færður inn reikningur úr MF-bókhaldslykli sem notaður verður sem sjálfgefinn reikningur sem upphæðin ætti að bókast á í fyrirtæki félagans. Á síðunni **Bókhaldslykill** er hægt að tilgreina sjálfgefinn fjárhagsreikning MF-félaga fyrir reikninga sem reglulega eru notaðir í MF-sölu- eða innkaupalínum á útleið. Til dæmis er hægt að færa inn samsvarandi safnreikning lánardrottna úr MF-bókhaldsreikningi fyrir safnreikninga viðskiptamanna.  

Þegar fjárhagsreikningur er síðan færður inn í reitinn **Nr. Mótreiknings** í línu milli fyrirtækja með **MF-félaga** í reitnum **Tegund reiknings** er sjálfkrafa fyllt í reitinn **MF-félagi fjárhagsreikningur**.  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Bókhaldslykill** og velja síðan viðkomandi tengil.  
2. Á línuna fyrir fjárhagsreikning sem er notaður fyrir millifyrirtækjafærslur, í reitnum **Sjálfgefinn fjárhagsreikningur MP félaga** skal færa inn MF-fjárhagsreikninginn sem félaginn á að bóka í við bókun í fjárhagsreikninga í línunni.  
3. Skref 2 er endurtekið fyrir hvern reikning sem oft er færður inn í reitinn **Mótreikningur nr.** í línu í færslubók eða fylgiskjali milli fyrirtækja.

## <a name="to-set-up-intercompany-dimensions"></a>Uppsetning vídda millifyrirtækja

Ef samstæðufélagarnir eiga að skiptast á færslum með víddum sem tengjast þeim verður að samþykkja víddirnar sem allir munu nota. Til dæmis stofnar móðurfélag flokksins einfaldaða útgáfu af eigin víddum, flytur þær út í XML-skrá sem það dreifir til hvers fyrirtækis í flokknum. Hvert dótturfyrirtæki flytur síðan XML-skrána inni í töfluna **MF-vídd** og varpar milli-fyrirtækjavíddum á víddirnar í eigin **vídda** síðu.  

> [!NOTE]
> Hvert fyrirtæki í [!INCLUDE [prod_short](includes/prod_short.md)] verður að varpa víddunum í MF-víddir fyrir skjöl á útleið og varpa MF-víddum á sínar eigin víddir fyrir skjöl á innleið. Þessi vörpun hjálpar til við að tryggja samræmi þvert á fyrirtæki. Frekari upplýsingar eru í hlutanum [MF-víddum varpað á víddir fyrirtækisins](#to-map-intercompany-dimensions-to-your-companys-dimensions).

Ef fyrirtækið þitt er móðurfyrirtækið og er með skilgreinandi safn milli-fyrirtækjavídda sem hópurinn notar sem sameiginlega viðmiðun, er þessari aðferð fylgt [Skilgreining vídda millifyrirtækja](intercompany-how-setup.md#to-define-the-intercompany-dimensions).

Ef fyrirtæki þitt er dótturfyrirtæki og þú færð XML-skrá með MF-víddum sem hópurinn notar sem sameiginlega viðmiðun er þessari aðferð fylgt [Hvernig á að flytja inn millifyrirtækjavíddir](intercompany-how-setup.md#to-import-the-intercompany-dimensions).

### <a name="to-define-the-intercompany-dimensions"></a>Skilgreina MF-víddir
1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **MF-víddir** og velja síðan viðkomandi tengil.  
2. Á síðunni **MF-víddir** er hver vídd er færð inn í línu á síðunni.

    Ef MF-víddirnar verða eins eða svipaðar og víddir fyrirtækisins er hægt að fylla síðuna sjálfkrafa út með því að nota aðgerðina **Afrita úr víddum** og breyta síðan línunum sem verða til.  
3. Velja skal **Flytja út** aðgerðina til að flytja MF-víddirnar út í XML-skrá til dreifingar til fyrirtækisfélaga.  
4. Skrárheitið og staðsetningin þar sem vista á XML-skrána eru valin og síðan smellt á **Vista**.  

### <a name="to-import-the-intercompany-dimensions"></a>Millifyrirtækjavíddir fluttar inn  
Þegar til er skrá sem inniheldur skilgreinandi MF-víddir, geta millifyrirtækjafélagar flutt hana inn til að vera vissir um að hafa sömu víddirnar.  
1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **MF-víddir** og velja síðan viðkomandi tengil.  
2. Á síðunni **MF-víddir** veljið aðgerðina **Flytja inn**.  
3. Skrárheiti og staðsetning XML-skrárinnar eru tilgreind og smellt á **Opna**.  

Línurnar á síðunni **MF-víddir** og síðunni **MF-víddargildi** eru fluttar inn.  

### <a name="to-map-intercompany-dimensions-to-your-companys-dimensions"></a>MF-víddum varpað á víddir fyrirtækisins:
Þegar víddir hafa verið skilgreindar eða fluttar inn sem samstæðufélagarnir hafa samþykkt að nota verður að tengja hverja samstæðuvíddir við eina af víddum fyrirtækisins og öfugt. Á síðunni **MF-víddir** er skilgreint hvernig MF-víddir í *færslum á innleið* verða túlkaðar sem víddir í víddatöflu fyrirtækisins. Á síðunni **Víddir** er tilgreint hvernig víddirnar verði túlkaðar sem MF-víddir í *færslum á útleið*.

Ef einhver af víddunum milli fyrirtækja hefur sama kóta og samsvarandi víddir í víddatöflu fyrirtækisins er hægt að láta forritið varpa víddunum sjálfkrafa, og þá er hægt að varpa reikningunum sjálfkrafa.  

Í eftirfarandi skrefum er MF-víddum fyrst varpað í víddir fyrir skjöl á innleið á síðunni **MF-víddir**. Síðan er víddum varpað í MF-víddir fyrir skjöl á útleið á síðunni **Víddir**.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **MF-víddir** og velja síðan viðkomandi tengil.
2. Á síðunni **MF-víddir** eru línurnar sem á að varpa sjálfkrafa eru valdar og svo er **Varpa á víddir með sama kóða** aðgerðin valin.
3. Fyrir hverja vídd innan samstæðu sem ekki er varpað sjálfkrafa er fyllt út í **reitinn Varpa á víddarkóta**.

    Hugsanlega þarf að bæta reitnum við yfirlitið. Frekari upplýsingar eru í [Sérstilling verksvæðis](ui-personalization-user.md).
4. Veljið aðgerðina **MF-víddargildi**.
5. Á síðunni **MF-víddargildi** er reiturinn **Varpa á víddargildiskóða** fylltur út.

    Halda áfram að varpa víddum á MF-víddir með því að framkvæma svipuð skref.
6. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Víddir** og velja síðan viðkomandi tengil.
7. Á síðunni **Víddir** eru línurnar sem á að varpa sjálfkrafa eru valdar og svo er **Varpa á MF-víddir með sama kóða** aðgerðin valin.
8. Fyrir hverja vídd innan samstæðu sem ekki er varpað sjálfkrafa skal fylla út **reitinn Varpa á MF-víddargildiskóta**.
9. Velja aðgerðina **Víddargildi**.
10. Á síðunni **Víddargildi** er reiturinn **Varpa á MF-víddargildiskóða** fylltur út.

## <a name="see-also"></a>Sjá einnig

[Vinna með millifyrirtækjafærslur](intercompany-manage.md)  
[Fjármál](finance.md)  
[Uppsetning Fjármála](finance-setup-finance.md)  
[Vinna við Almennar færslubækur](ui-work-general-journals.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]