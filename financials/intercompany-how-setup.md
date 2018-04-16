---
title: "Setja upp Bókun millifyrirtækjafærslu | Microsoft Docs"
description: "Stofna lánardrottna og viðskiptamenn millifyrirtækis sem svokallaða millifyrirtækjafélaga, og setja upp bókhaldslykil millifyrirtækis."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: IC, group, consolidation, affiliate, subsidiary
ms.date: 06/20/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 7a23f0ba28ab4c7bc9e028375246ea2e57d32764
ms.contentlocale: is-is
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-intercompany"></a>Uppsetning milli fyrirtækja
Til að senda viðskipti (til dæmis sölubókarlínu) frá einu fyrirtæki og láta stofna samsvarandi viðskipti (til dæmis innkaupabókarlínu) í fyrirtækisfélaganum þurfa fyrirtækin að koma sér saman um sameiginlegan bókhaldslykil og víddir sem nota á í viðskiptum milli fyrirtækjanna. Bókhaldslykillinn milli fyrirtækja gæti til dæmis verið einfölduð útgáfa af bókhaldslykli móðurfyrirtækisins. Hvert fyrirtæki varpar heildarbókhaldslykli sínum á sameiginlega bókhaldslykilinn milli fyrirtækja, og hvert fyrirtæki varpar víddum sínum á víddirnar milli fyrirtækja.  

Einnig þarf að setja upp MF-félagakóða fyrir hvern fyrirtæki félaga, sem öll fyrirtækin þurfa að samþykkja, og síðan úthluta þeim til viðskiptamanna- og lánardrottnaspjalda með því fylla út í reitinn **MF-félagakóði**.  

Ef MF-línur eru stofnaðar eða mótteknar er hægt að nota eigin vörunúmer eða setja upp vörunúmer félagans fyrir hverja vöru, annað hvort í **Lánardr. vörunr.** reitinn eða í **Algengt vörunr.** á vöruspjaldinu. Einnig má nota **Vörumillivísun** aðgerðina: Til að varpa vörunúmerin á skjalinu í lýsingar þínar á vörum millifyrirtækjafélaga, skal opna kortið fyrir hverja vöru, og velja síðan **millivísanir** aðgerð til að setja upp millivísanir á milli þinna vörulýsinga og þess sem tilheyrir millifyrirtækjafélaga.  

Ef gerðar verða sölufærslur milli fyrirtækja sem innihalda forða þarf að fylla út reitinn **Nr. innk.reikn. MF-félaga** á forðaspjaldi fyrir hvern viðkomandi forða. Þetta er númer fjárhagsreikningsins milli fyrirtækja sem magnið fyrir þennan forða verður bókað í fyrirtækisfélaganum. Nánari upplýsingar eru í  

## <a name="to-set-up-companies-for-intercompany-transactions"></a>Setja upp fyrirtæki fyrir millifyrirtækjafærslur
1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Fyrirtækjaupplýsingar** og velja svo viðeigandi tengil.  
2. Í glugganum **Fyrirtækjaupplýsingar** skal fylla inn í reitina **MF-félagakóði**, **MF-innhólfstegund**.  og **MF-innhólfsupplýsingar**. [!INCLUDE [tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-set-intercompany-partners"></a>Setja millifyrirtækjafélaga
1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Millifyrirtækjafélagar** og velja svo viðeigandi tengil.
2. Valið er **Nýtt** aðgerð.
3. Í glugganum **Millifyrirtækjafélagi** skal fylla út reitina eins og þörf krefur.

## <a name="to-set-up-intercompany-vendors-and-intercompany-customers"></a>Hvernig á að: Setja upp lánardrottna og viðskiptamenn millifyrirtækis
1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **lánardrottnar** og velja svo viðeigandi tengil.
2. Að öðrum kosti geturðu nálgast lánardrottinn frá reitnum **Lánardrottinn nr.** í glugganum **Millifyrirtækjafélagi**.
3. Opna spjaldið fyrir lánardrottinn sem er millifyrirtækjafélagi. Nánari upplýsingar eru í [Skráning nýrra lánardrottna](purchasing-how-register-new-vendors.md).
4. Í reitnum **Kóði millifyrirtækjafélaga** er valinn viðeigandi kóði fyrir millifyrirtækjafélaga.
5. Endurtaka skref 1 til 4 fyrir viðskiptamenn.

## <a name="to-set-up-intercompany-charts-of-accounts"></a>Bókhaldslykill milli fyrirtækja er settur upp.
Til að hópur fyrirtækja geti búið til færslur á milli fyrirtækja þarf hann að koma sér saman um bókhaldslykil sem notaður verður sem sameiginleg viðmiðun. Félagarnir þurfa að koma sér saman um reikningsnúmerin sem allir nota þegar færslur milli fyrirtækja eru stofnaðar. Dæmi: móðurfyrirtæki hópsins stofnar einfaldaða útgáfu af bókhaldslykli sínum, flytur bókhaldslykil milli fyrirtækja úr gagnagrunninum í XML-skrá og dreifir henni til einstakra fyrirtækja í hópnum.  

Ef fyrirtækið þitt er móðurfyrirtækið og er með skilgreinandi bókhaldslykil milli fyrirtækja sem hópurinn notar sem sameiginlega viðmiðun, er þessari aðferð fylgt „Skilgreining bókhaldslykils milli fyrirtækja“.  

Ef fyrirtækið þitt er dótturfyrirtæki og hefur fengið XML-skrá með bókhaldslykli sem hópurinn notar sem sameiginlega viðmiðun er þessari aðferð fylgt „Hvernig á að flytja inn Bókhaldslykill milli fyrirtækja“.  

### <a name="to-set-up-the-defining-intercompany-chart-of-accounts"></a>Skilgreinandi bókhaldslykill milli fyrirtækja er settur upp.
1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **MF bókhaldslykill** og velja svo viðeigandi tengil.
2. Í glugganum **MF-bókhaldslykill** færið inn hvern reikining í línu í glugganum.  
3. Ef MF-bókhaldslykillinn verður eins og eða svipaður og venjulegi bókhaldslykillinn er hægt að láta fylla gluggann út sjálfkrafa með því að velja **Afrita frá bókhaldslykli** aðgerðina. Hægt er að breyta nýju línunni eins og þurfa þykir.

### <a name="to-export-an-intercompany-chart-of-accounts"></a>MF-bókhaldslykill er fluttur út
Til að leyfa millifyrirtækjafélögum þínum að flytja inn skilgreinandi bókhaldslykilinn, verður að flytja hann út í skrá.      
1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **MF bókhaldslykill** og velja svo viðeigandi tengil.
2. Í gluggi **MF-bókhaldslykill** veljið aðgerðina **Flytja út** og síðan hnappinn **Vista**.
3. Skrárheitið og staðsetningin þar sem vista á XML-skrána eru valin og síðan smellt á **Vista**.  

### <a name="to-import-the-intercompany-chart-of-accounts"></a>Bókhaldslykill milli fyrirtækja fluttur inn:  
Þegar til er skrá sem inniheldur skilgreinandi MF-bókhaldslykilinn, geta millifyrirtækjafélagar flutt hana inn til að vera vissir um að hafa sama lykilinn.  
1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **MF bókhaldslykill** og velja svo viðeigandi tengil.  
2. Í gluggi **MF-bókhaldslykill** veljið aðgerðina **Flytja inn**.  
3. Skrárheiti og staðsetning XML-skrárinnar eru tilgreind og smellt á **Opna**.  

Glugginn **MF-bókhaldslykill** er fylltur út með nýjum eða breyttum fjárhagsreikningslínum samkvæmt MF-bókhaldslyklinum í skránni. Allar fyrirliggjandi, óskyldar línur í glugganum haldast óbreyttar.

### <a name="to-map-the-intercompany-chart-of-accounts-to-your-companys-chart-of-accounts"></a>Til að varpa MF-bókhaldslykli á bókhaldslykil fyrirtækisins.  
Eftir að MF-bókhaldslykill sem millifyrirtækjafélagar hafa samþykkt að nota hefur verið skilgreindur eða fluttur inn, þarf að tengja hvern fjárhagsreikning millifyrirtækja við einn af fjárhagsreikningum fyrirtækisins. Í glugganum **MF-bókhaldslykill** er skilgreint hvernig fjárhagsreikningar milli fyrirtækja í færslum á innleið verða túlkaðir sem reikningar í bókhaldslykli fyrirtækisins.

Ef reikningar í bókhaldslykli milli fyrirtækja hafa sömu reikningsnúmer og samsvarandi reikningar í bókhaldslyklinum er hægt að varpa reikningunum.

1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **MF bókhaldslykill** og velja svo viðeigandi tengil.  
2. Línurnar sem á að varpa sjálfkrafa eru valdar og svo er valin aðgerðin **Varpa á reikning með sama nr.**.  
3. Fyrir hvern fjárhagsreikning milli fyrirtækja sem ekki var varpað sjálfkrafa, skal fylla í reitinn **Varpa á Fjárhagsreikning nr.**.  

## <a name="to-set-up-default-intercompany-partner-general-ledger-accounts"></a>Hvernig á að setja upp sjálfgefna fjárhagsreikninga samstarfsfyrirtækja  
Þegar sölu- eða innkaupalína milli fyrirtækja er stofnuð til að senda sem færslu á útleið er færður inn reikningur úr MF-bókhaldslykli sem notaður verður sem sjálfgefinn reikningur sem upphæðin ætti að bókast á í fyrirtæki félagans. Í glugganum **Bókhaldslykill** er hægt að tilgreina sjálfgefinn fjárhagsreikning MF-félaga fyrir reikninga sem oft eru notaðir í MF-sölu- eða innkaupalínum á útleið. Til dæmis er hægt að færa inn samsvarandi safnreikning lánardrottna úr MF-bókhaldsreikningi fyrir safnreikninga viðskiptamanna.  

Þegar fjárhagsreikningur er síðan færður inn í reitinn **Nr. Mótreiknings** í línu milli fyrirtækja með **MF-félaga** í reitnum **Tegund reiknings** er sjálfkrafa fyllt í reitinn **MF-félagi fjárhagsreikningur**.  

1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **bókhaldslykill** og velja svo viðeigandi tengil.  
2. Á línuna fyrir fjárhagsreikning sem er notaður fyrir millifyrirtækjafærslur, í reitnum **Sjálfgefinn fjárhagsreikningur MP félaga** skal færa inn MF-fjárhagsreikninginn sem félaginn á að bóka í við bókun í fjárhagsreikninga í línunni.  
3. Skref 3 er endurtekið fyrir hvern reikning sem oft er færður inn í reitinn **Mótreikningur nr.** í línu í færslubók eða fylgiskjali milli fyrirtækja.

## <a name="to-set-up-intercompany-dimensions"></a>Uppsetning vídda millifyrirtækja
Ef milli-fyrirtækjafélagar vilja skiptast á færslum með víddum þurfa þeir allir að samþykkja milli-fyrirtækjavíddirnar sem allir koma til með að nota. Dæmi: móðurfyrirtæki hópsins stofnar einfaldaða útgáfu af víddum sínum, flytur milli-fyrirtækjavíddir í XML-skrá og dreifir henni til einstakra fyrirtækja í hópnum. Hvert dótturfyrirtæki flytur síðan XML-skrána inni í töfluna **MF-vídd** og varpar milli-fyrirtækjavíddum á víddirnar í eigin **vídda** glugga.  

Ef fyrirtækið þitt er móðurfyrirtækið og er með skilgreinandi safn milli-fyrirtækjavídda sem hópurinn notar sem sameiginlega viðmiðun, er þessari aðferð fylgt „Skilgreining vídda millifyrirtækja“.

Ef fyrirtæki þitt er dótturfyrirtæki og þú færð XML-skrá með MF-víddum sem hópurinn notar sem sameiginlega viðmiðun er þessari aðferð fylgt „Hvernig á að flytja inn millifyrirtækjavíddir“.

### <a name="to-define-the-intercompany-dimensions"></a>Skilgreina MF-víddir
1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Millifyrirtækjavíddir** og velja svo viðeigandi tengil.  
2. Í glugganum **MF-víddir** er hver vídd er færð inn í línu í glugganum.

    Ef MF-víddirnar verða eins eða svipaðar og víddir fyrirtækisins er hægt að fylla gluggann sjálfkrafa út með því að nota aðgerðina **Afrita úr víddum** og breyta síðan línunum sem verða til.  
3. Velja skal **Flytja út** aðgerðina til að flytja MF-víddirnar út í XML-skrá til dreifingar til fyrirtækisfélaga.  
4. Skrárheitið og staðsetningin þar sem vista á XML-skrána eru valin og síðan smellt á **Vista**.  

### <a name="to-import-the-intercompany-dimensions"></a>Millifyrirtækjavíddir fluttar inn  
Þegar til er skrá sem inniheldur skilgreinandi MF-víddir, geta millifyrirtækjafélagar flutt hana inn til að vera vissir um að hafa sömu víddirnar.  
1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Millifyrirtækjavíddir** og velja svo viðeigandi tengil.  
2. Í gluggi **MF-víddir** veljið aðgerðina **Flytja inn**.  
3. Skrárheiti og staðsetning XML-skrárinnar eru tilgreind og smellt á **Opna**.  

Línurnar í glugganum **MF-víddir** og glugganum **MF-víddargildi** eru fluttar inn.  

### <a name="to-map-intercompany-dimensions-to-your-companys-dimensions"></a>MF-víddum varpað á víddir fyrirtækisins:
Þegar búið er að skilgreina eða flytja inn víddunum sem þú og milli-fyrirtækjafélagar hafa samþykkt að nota þarf að tengja hverja vídd milli fyrirtækja við eina af víddum fyrirtækisins og öfugt. Í glugganum **MF-víddir** er skilgreint hvernig MF-víddir í færslum á innleið verða túlkaðar sem víddir í víddatöflu fyrirtækisins. Í glugganum **Víddir** er tilgreint hvernig víddirnar verði túlkaðar sem MF-víddir í færslum á útleið.

Ef einhver af víddunum milli fyrirtækja hefur sama kóta og samsvarandi víddir í víddatöflu fyrirtækisins er hægt að láta kerfið varpa víddunum sjálfkrafa, og þá er hægt að varpa reikningunum sjálfkrafa.

1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Millifyrirtækjavíddir** og velja svo viðeigandi tengil.
2. Í glugganum **MF-víddir** eru línurnar sem á að varpa sjálfkrafa eru valdar og svo er **Varpa á víddir með sama kóða** aðgerðin valin.
3. Fyrir hverja vídd milli fyrirtækja sem er ekki varpað sjálfkrafa, skal fylla út í reitinn **Varpa á víddarkóta**.
4. Velja aðgerðina **MF-víddargildi**.
5. Í glugganum **MF-víddargildi** er reiturinn **Varpa á víddargildiskóða** fylltur út.

    Halda áfram að varpa víddum á MF-víddir með því að framkvæma svipuð skref.
6. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Víddir** og velja svo viðeigandi tengil.
7. Í glugganum **Víddir** eru línurnar sem á að varpa sjálfkrafa eru valdar og svo er **Varpa á MF-víddir með sama kóða** aðgerðin valin.
8. Fyrir hverja vídd milli fyrirtækja sem er ekki varpað sjálfkrafa, skal fylla út í reitinn **Varpa á MF víddargildiskóða**.
9. Velja aðgerðina **Víddargildi**.
10. Í glugganum **Víddargildi** er reiturinn **Varpa á MF-víddargildiskóða** fylltur út.

## <a name="see-also"></a>Sjá einnig
[Vinna með millifyrirtækjafærslur](intercompany-manage.md)  
[Fjármál](finance.md)  
[Uppsetning Fjármála](finance-setup-finance.md)  
[Vinna í færslubókum](ui-work-general-journals.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

