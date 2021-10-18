---
title: Uppsetning kostnaðarbókhalds
description: Áður en byrjað er að vinna með kostnaðarbókhald þarf að framkvæma uppsetningu. Hver kostnaðarfærsla verður að hafa úthlutaða kostnaðartegund og kóða kostnaðarstaðar eða kostnaðarhlut úthlutaðan.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/16/2021
ms.author: edupont
ms.openlocfilehash: 7f6f79ba1f8005363204f48c5ea9b91073b517f7
ms.sourcegitcommit: 6ad0a834fc225cc27dfdbee4a83cf06bbbcbc1c9
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/01/2021
ms.locfileid: "7588677"
---
# <a name="setting-up-cost-accounting"></a>Uppsetning kostnaðarbókhalds
Áður en byrjað er að vinna með kostnaðarbókhald þarf að framkvæma uppsetningarverkefni.

## <a name="balances-between-cost-type-cost-center-and-cost-object"></a>Stöður milli kostnaðartegundar , kostnaðarstaðar og kostnaðarliðar
Þegar kostnaðarbókhald er settur upp ætti að ganga úr skugga um að allar færslur séu skráðar á kostnaðartegund sem og kostnaðarstað eða kostnaðarhlut. Það þýðir að hver kostnaðarfærsla verður að hafa úthlutaða kostnaðartegund og kostnaðarstöðvarkóta eða kostnaðarhlut úthlutaðan. Þessi regla tryggir að hver kostnaðarfærsla birtist í annaðhvort kostnaðarstöðunum eða kostnaðarhlutunum, en aldrei á báðum stöðum.  

Með því að gera þetta er hægt að stofna eftirfarandi bókhaldsjöfnu:  

*Tegund kostnaðar* = *Staða kostnaðarstaðar* + *Staða kostnaðarhlutar*  

Þegar prenta á skýrslur yfir tegund kostnaðar, kostnaðarstað og kostnaðarhluta er hægt að gera greiningu á þessum venslum.

## <a name="setting-up-cost-types"></a>Uppsetning kostnaðargerða
Myndrit kostnaðartegunda eru svipuð bókhaldslyklum í fjárhag. Hægt er að setja upp myndritið yfir kostnaðartegundir á eftirfarandi hátt:  

-   Skipulag kostnaðargerða milli fyrirtækja svipað og á reikningum rekstrarreiknings á fjárhagsbókhaldslyklinum. Síðan er hægt að flytja bókhaldslykil fjárhags yfir í kostnaðargerðir. Hægt er að gera allar nauðsynlegar leiðréttingar eftir flutninginn.  
-   Stofna nýja kostnaðartegund eða bæta nýjum kostnaðartegundum við fyrirliggjandi kostnaðartegund. Stofna þarf hverja nýja kostnaðartegund sérstaklega.  

### <a name="to-transfer-the-general-ledger-chart-of-accounts-to-the-chart-of-cost-types"></a>Til að flytja bókhaldslykil fjárhags yfir í kostnaðargerðir.  
1.  Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar 1.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Myndrit kostnaðargerða** og velja síðan viðkomandi tengil.  
2.  Velja skal aðgerðina **Sækja kostnaðargerðir úr bókhaldslykli**. Í svarglugganum er valið hnappinn **Já** til að staðfesta flutninginn. Aðgerðin notar bókhaldslykla til að stofna myndrit af kostnaðartegundum.  

    Myndrit kostnaðargerða inniheldur nú alla rekstrarreikninga í fjárhag og inniheldur fyrirsagnir og samtölur. Hægt er að breyta myndriti yfir kostnaðartegundir, eftir þörfum. Til dæmis er hægt að eyða tvíteknum fyrirliggjandi kostnaðartegundum.  

    > [!IMPORTANT]  
    >  Aðgerðin **Skrá kostnaðargerðir í bókhaldslyklinum** uppfærir samband milli bókhaldslykils og bókhaldslykils fyrir kostnaðartegundir. **númer**  svæðið er fyllt og staðfest til að tryggja að hver almennur fjárhagsreikningur tengist aðeins einni tegund kostnaðar. Aðgerðin keyrir sjálfkrafa áður en fjárhagsfærslur eru færðar í kostnaðarbókhald.  

### <a name="to-set-up-new-cost-types-in-the-chart-of-cost-types-page"></a>Til að setja upp nýjar kostnaðargerðir á síðunni Myndrit fyrir kostnaðargerðir  
1.  Opnaðu síðuna **Myndrit yfir kostnaðargerðir** í breytingarstillingu.  
2.  Fyllið inn í reitina eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
    >  Hægt er að setja upp og viðhalda kostnaðargerðum á síðunni **Kostnaðargerð spjald** eða á síðunni **Myndrit yfir kostnaðargerðir**. Í þessu ferli eru settar upp kostnaðartegundir á síðunni **Myndrit yfir kostnaðargerðir**.

3.  Þegar búið er að stofna öll kostnaðargerðir, skal velja aðgerðina **Draga inn kostnaðargerðir**. Í svarglugganum, veljið hnappinn **Já**.  
4.  Tengja nýju tegund kostnaðar í samsvarandi almennan fjárhagslykil.  

    > [!IMPORTANT]  
    >  Ef skilgreiningar hafa verið færðar í **Samtala** reitina fyrir línutegundina **Loka-upphæð** áður en aðgerðin **Inndráttur kostnaðargerða** er framkvæmd þarf að færa skilgreiningarnar inn aftur því að aðgerðin skrifar yfir gildin í öllum **Loka-Upphæð**-reitum.  

### <a name="to-update-cost-types"></a>Til að uppfæra kostnaðargerðir  
1.  Á síðunni **Uppsetning kostnaðarbókhalds** skal velja hvort uppfæra eigi myndrit yfir kostnaðartegundir sjálfkrafa þegar bókhaldslykillinn breytist.  
2.  Í reitnum **Stilla fjárhagsreikning** er hægt að velja úr eftirfarandi valkostum.  

- **Engin jöfnun** - Það er engin samsvarandi breyting á kostnaðartegundum þegar bókhaldslyklinum er breytt.  
- **Sjálfvirkt** - Samsvarandi breyting er gerð á kostnaðartegundalyklinum þegar bókhaldslyklinum er breytt.  
- **Kvaðning** - Skilaboð birtast þar sem spurt er hvort gera eigi samsvarandi breytingu á myndriti kostnaðartegunda þegar bókhaldslykli er breytt.

## <a name="defining-the-relationship-between-cost-types-and-general-ledger-accounts"></a>Skilgreining á venslum milli kostnaðargerða og fjárhagsreikninga
Tengsl milli kostnaðartegundarinnar og almenna fjárhagslykilsins eru stofnuð í kostnaðartegundinni og í fjárhagsreikningnum.  

* Reiturinn **Fjárhagsreikningssvið** í töflunni **Kostnaðargerð** mælir fyrir um hvaða fjárhagsreikningur tilheyrir tegund kostnaðar.  
* Reiturinn **Númer kostnaðartegundar** í reikningatöflu mælir fyrir um hvaða tegund kostnaðar fjárhagsreikningur tilheyrir.  

Þessir tveir reitir eru fylltir út sjálfkrafa þegar aðgerðin **Sækja kostnaðargerðir úr bókhaldslykli** er notuð.  

### <a name="relationship-between-general-ledger-accounts-and-cost-types"></a>Tengsl milli fjárhagsreiknings og kostnaðartegunda  
Til eru n:1 vensl milli fjárhagsreikninga og kostnaðargerðar. Nokkrir fjárhagsreikningar geta tilheyrt einni kostnaðartegund, en hver fjárhagsreikningur tilheyrir aðeins einni kostnaðargerð. Eftirfarandi tafla lýsir upplýsingunum í tengslunum.  

|Tengsl|**Reikningsbil fjárhags**|**Kostnaðartegundarnr.**|  
|------------------|------------------------------------------------|-------------------------------------------|  
|Einn fjárhagsreikningur fyrir hverja kostnaðartegund|Einn fjárhagsreikningur|Ein kostnaðartegund|  
|Nokkrir fjárhagsreikningar fyrir hverja kostnaðartegund|Svið fjárhagsreikninga, til dæmis 7110..7193 fyrir hvern fjárhagsreikning|Fyrir hvern fjárhagsreikning í bilinu, er aðeins ein kostnaðartegund|  
|Kostnaðartegundir án samsvarandi tengsla við fjárhaglykla|\<Empty\>||  
|Fjárhagsreikningar með færslur sem ekki verið fluttar||\<Empty\>|  

### <a name="cost-types-without-a-relationship-to-the-general-ledger"></a>Kostnaðartegundir án tengsla við fjárhag  
Kostnaðartegund má ekki hafa tengsl við fjárhagsreikninga ef annað af eftirfarandi skilyrðum á við:  

* Reikningar fyrir rekstarbókhald, eins og Reikn. vextir og Afskriftir, taka einungis kostnað frá rekstrarbókhaldi.  
* Aukakostnaðartegundir, t.d. kostnaðargerðir 9901, 9902 og 9903 í [!INCLUDE[prod_short](includes/prod_short.md)]-gagnagrunninum, eru notaðir sem kredit- og debetreikningar fyrir úthlutanir.  
* Hjálparreikningurinn, 9920 í [!INCLUDE[prod_short](includes/prod_short.md)] gagnagrunninn, inniheldur raunverulegar uppsafnanir sem sýna muninn milli kostnaðar og gjalda úr fjárhag.

## <a name="setting-up-cost-centers"></a>Uppsetning kostnaðarstaða
Kostnaðarstaðir eru deildir og framlegðarstöðvar sem bera ábyrgð á kostnaði og tekjum. Myndrit kostnaðarstaða er svipað og víddarupplýsingar fyrir fjárhag. Hægt er að setja upp myndritið yfir kostnaðarstaði á eftirfarandi hátt:  

-   Flytja víddargildi í fjárhag í myndrit yfir í kostnaðarstaði. Hægt er að gera allar nauðsynlegar leiðréttingar eftir flutninginn.  
-   Stofna nýjan kostnaðarstað sem er óháður fjárhagnum eða bæta nýjum kostnaðarstað við kostnaðarstað sem fyrir er. Stofna þarf hvern kostnaðarstað sérstaklega.  

### <a name="to-transfer-dimension-values-in-the-general-ledger-to-the-chart-of-cost-centers"></a>Til að flytja víddargildi í fjárhag í myndrit yfir í kostnaðarstaði  
1.  Setja upp vídd sem á að vera kostnaðarstaðarvíddin á síðunni **Uppfæra Kostnaðarbókhaldsvíddir**. Aðeins gildi úr þessari vídd er flutt.  
2.  Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar 2.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Myndrit kostnaðarstaða** og velja síðan viðkomandi tengil.  
3.  Í flipanum **Aðgerðir** í flokknum **Eiginleikar** veljið **Sækja úr víddinni kostnaðarstaðir** til að flytja víddargildi í myndriti kostnaðarstaðanna. Aðgerðin flytur víddargildin sem skilgreind voru í skrefi 1.  

    > [!NOTE]  
    >  Hægt er að setja reitinn **Stilla kostnaðarstaðavíddir** upp þannig að hann skilgreini einstefnusamstillingu á víddargildum frá fjárhag yfir í myndrit yfir kostnaðarstaði. Ekki er hægt að skilreina samstillingu myndrits yfir kostnaðarstaði við víddargildi úr fjárhag.  

Myndrit kostnaðarstaða inniheldur nú öll tilgreind víddargildi úr fjárhag og inniheldur titla og samtölur.  

### <a name="to-create-new-cost-centers-in-the-chart-of-cost-centers-page"></a>Til að stofna nýja kostnaðarstaði á síðunni Myndrit fyrir kostnaðarstaði  
Hægt er að setja upp og vinna með kostnaðarstaði í **Kostnaðarstaðaspjald** spjaldinu eða á síðunni **Myndrit fyrir kostnaðarstaði**. Í þessu ferli eru settir upp kostnaðarstaðir á síðunni **Myndrit fyrir kostnaðarstaði**.  

1. Opnaðu síðuna **Myndrit yfir kostnaðarstaði** í breytingarstillingu.  
2. Í reitinn **Kóði** er færður inn kóti kostnaðarstaðarins. Allir kostnaðarstaðir verða að hafa kóta.  
3. Í reitinn **Heiti** er fært inn heiti kostnaðarstaðarins.  
4. Velja fellilistaörina í reitnum **Línugerð** til að tilgreina tilgang kostnaðarstaðarins.  

    - Fylla þarf út í reitinn **Samtala** fyrir kostnaðarstaði af gerðinni **Samtals**. Nota skal virkinn **eða**, sem er lóðrétt lína (**&#124;**) til að stilla svið kostnaðarstaða.  
    - Fyrir kostnaðarstaði af línutegundinni **Til-tala** er sjálfkrafa fyllt út í reitinn þegar inndráttarvirknin er notuð.  
5.  Fyllið upp í reitina **Röðunarpöntun** og **Undirflokkar kostnaðar**.  
6.  Velja næstu tómu línu til að stofna nýjan kostnaðarstað og endurtaka síðan þrep 2 til 5.  
7.  Þegar búið er að setja upp alla kostnaðarstað skal velja aðgerðina **Draga inn kostnaðarstaði**. Velja hnappinn **Já**.  

> [!IMPORTANT]  
>  Ef skilgreiningar voru færðar inn í **Samtölur** reitina fyrir **Loka-samtala** kostnaðarstaði áður en inndráttaraðgerðin var keyrð þarf að færa þær inn aftur. Aðgerðin skrifar yfir gildin í öllum **Til - tala** reitum.

## <a name="setting-up-cost-objects"></a>Uppsetning kostnaðarhluta
Kostnaðurhlutir eru verkefni, afurðair eða þjónustur fyrirtækis. Myndrit kostnaðarhluta er svipað og víddarupplýsingar fyrir fjárhag. Hægt er að setja upp myndritið yfir kostnaðaríhluti á eftirfarandi hátt:  

* Flytja víddargildi í fjárhag í myndrit yfir í kostnaðarhluti. Hægt er að gera allar nauðsynlegar leiðréttingar eftir flutninginn.  
* Stofna nýjan kostnaðarhlut sem er óháður fjárhagnum eða bæta nýjum kostnaðarhlut við kostnaðarhlut sem fyrir er. Stofna þarf hvern kostnaðaríhlut sérstaklega.  

### <a name="to-transfer-dimension-values-from-the-general-ledger-to-the-chart-of-cost-objects"></a>Til að flytja víddargildi úr fjárhag í kostnaðarhluti  
1.  Stilla vídd sem á að vera kostnaðarliðarvíddin á síðunni **Uppfæra CA víddir**. Aðeins gildi úr þessari vídd er flutt.  
2.  Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar 3.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Myndrit kostnaðarhluta** og velja síðan viðkomandi tengil.  
3.  Veljið aðgerðina **Sækja kostnaðarhluti úr vídd** til að flytja víddargildi í myndriti kostnaðarhlutanna. Aðgerðin flytur víddargildin sem skilgreind voru í skrefi 1.  

    > [!NOTE]  
    >  Hægt er að setja reitinn **Stilla kostnaðarhlutavíddir** upp þannig að hann skilgreini einstefnusamstillingu á víddargildum frá fjárhag yfir í myndrit yfir kostnaðarhluti. Ekki er hægt að skilreina samstillingu myndrits yfir kostnaðarhluti við víddargildi úr fjárhag.  

Myndrit kostnaðarhluta inniheldur nú öll tilgreind víddargildi úr fjárhag og inniheldur titla og samtölur.  

### <a name="to-create-new-cost-objects-in-the-chart-of-cost-objects-page"></a>Til að stofna nýja kostnaðarhluti á síðunni myndrit fyrir kostnaðarliði  
Hægt er að setja upp og vinna með kostnaðarliði í **Kostnaðarliðaspjald** spjaldinu eða á síðunni **Myndrit fyrir kostnaðarliði**. Í þessu ferli eru settir upp kostnaðarliðir á síðunni **Myndrit fyrir kostnaðarliði**.  

1.  Opnaðu síðuna **Myndrit yfir kostnaðarliði** í breytingarstillingu.  
2.  Í reitinn **Kóði** er færður inn kóti kostnaðarliða. Allir kostnaðarhlutir verða að hafa kóta.  
3.  Í reitinn **Heiti** er færður inn heiti kostnaðarliða.  
4.  Velja fellilistaörina í reitnum **Línugerð** til að tilgreina tilgang kostnaðarhlutarins.  

    * Fyrir kostnaðarhluti af línutegundinni **Samtals** skal fylla út reitinn **Samtals frá/til**. Nota skal virkinn **eða**, sem er lóðrétt lína (**&#124;**) til að stilla svið kostnaðarhluta.  
    * Fyrir kostnaðarhluti af línutegundinni **Til-tala** er sjálfkrafa fyllt út í reitinn þegar inndráttarvirknin er notuð.  
5.  Fyllið upp í reitinn **Röðunarpöntun**.  
6.  Velja næstu tómu línu til að stofna nýjan kostnaðarhlut og endurtaka síðan þrep 2 til 5.  
7.  Þegar búið er að setja upp alla kostnaðarhlutina, skal velja aðgerðina **Draga inn kostnaðarhluti**. Velja hnappinn **Já**.  

> [!IMPORTANT]  
>  Ef skilgreiningar voru færðar inn í reitina **Samtals frá/til** fyrir **Loka-upphæð** kostnaðarhluti áður en inndráttaraðgerðin var keyrð þarf að færa þær inn aftur. Aðgerðin skrifar yfir gildin í öllum **Til - tala** reitum.

## <a name="defining-cost-centers-and-cost-objects-for-chart-of-accounts"></a>Skilgreining kostnaðarstaði og kostnaðarhluti fyrir bókhaldslykil
Hægt er að flytja útgjalda- og tekjufærslur sjálfkrafa úr fjárhag í kostnaðarbókhald, annað hvort fyrir hverja fjarhagsfærslu eða með keyrslu. Þegar flutningurinn er framkvæmdur flytur [!INCLUDE[prod_short](includes/prod_short.md)] aðeins færslur sem þegar eru tengdar við kostnaðarstað eða kostnaðarhlut. Til að búa til merkingarbæran flutning þarf að tryggja að kostnaðarstaðir og kostnaðarhlutir séu rétt skilgreindir.  

### <a name="defining-default-dimension-values-for-general-ledger-accounts"></a>Skilgreining sjálfgefin víddargildi fyrir fjárhagslykla  
Fyrir hvern fjárhagsreikning er hægt að skilgreina sjálfgefið víddargildi í töflunni **Sjálfgefið víddargildi**. Eftirfarandi dæmi sýnir hvernig eigi að skilgreina að það ætti alltaf að vera kostnaðarstaður DEILDAR, en aldrei kostnaðarhlutur VERKEFNIS þegar bókað er á almennan fjárhagslykil.  

|**Víddarkóti**|**Virðisbókun**|  
|------------------------------------------|-----------------------------------------|  
|Deild|Kóti tilskilinn|  
|Verkefni|Enginn kóti|  

### <a name="defining-dimension-values-for-overhead-costs-and-direct-costs"></a>Skilgreining á víddargildi fyrir sameiginlegan kostnað og beinan kostnað  
 Hægt er að flytja rekstrarkostnað í kostnaðarstað og beinan kostnað í kostnaðaríhlut. Eftirfarandi tafla sýnir bestu samsetningu uppsetningargilda vídda.  

|Flytja í|Bókun kostnaðarstaðar|Bókun kostnaðarhlutar|  
|-----------------|-------------------------|-------------------------|  
|Kostnaðarstaður|Kóti tilskilinn|Enginn kóti|  
|Kostnaðarhlutur|Enginn kóti|Kóti tilskilinn|  

> [!NOTE]  
>  Til að ganga úr skugga um að fyrirfram skilgreindur kostnaðarstaður og kostnaðarhlutur sem eru sett upp í fjárhag séu sjálfkrafa færðar yfir í kostnaðarbókhald skal velja gátreitinn **Athuga fjárhagsbókanir** á síðunni Uppsetning kostnaðarbókhalds

## <a name="see-also"></a>Sjá einnig  
[Kostnaðarreikningur](finance-manage-cost-accounting.md)  
[Flytja og bóka kostnaðarfærslur](finance-transfer-and-post-cost-entries.md)   
[Skilgreina og úthluta kostnaði](finance-define-and-allocate-costs.md)  
[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]