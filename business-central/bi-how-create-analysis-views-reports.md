---
title: Stofna greiningarskýrslur
description: Lýsir því hvernig stofna skal nýjar greiningarskýrslur fyrir sölu, innkaup og birgðir og búa til greiningarsniðmát.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bi, power BI, analysis, KPI
ms.search.form: 555, 556, 557, 558, 9372, 9370, 9371
ms.date: 09/22/2022
ms.author: edupont
ms.openlocfilehash: 0e49f50f04087a56e119d2f50cc1e9e6a1aedbf0
ms.sourcegitcommit: 8ad79e0ec6e625796af298f756a142624f514cf3
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/30/2022
ms.locfileid: "9606198"
---
# <a name="create-analysis-reports"></a>Stofna greiningarskýrslur

Sölustjórar þurfa að greina veltu, brúttóhagnað og aðrar lykilstærðir varðandi sölu með reglulegu millibili. Innkaupaaðilar hafa meiri áhuga á að greina innkaupamagn, fylgjast með frammistöðu birgja og innkaupaverði. Vöru- og birgðastjórar þurfa hins vegar upplýsingar um birgðaveltu, greiningu á hreyfingu birgða og upplýsingar um birgðavirði. Þannig að það er ekki til nein greiningarskýrsla sem hentar fyrir allt.

Hægt er að sérsníða greiningarskýrslur út frá skrám yfir bókaðar færslur, t.d. sölu, innkaup, millifærslur og birgðaleiðréttingar. Í sérsníðanlegri skýrslu getur notandi sameinað, borið saman og sett fram frumgögnin sem eru upprunnin í birgðafjárhag (með tengdum virðisfærslum) á ýmsan þann hátt sem hann kýs. Greiningarskýrslan er því mjög svipuð veltitöfluskýrslu í Microsoft Excel.  

Þannig getur þú til dæmis búið til sérsniðna skýrslu sem tekur fyrir lykilreikninga þína hvað varðar heildarveltu vöru í upphæðum og seldu magni, brúttóhagnað og brúttóhagnaðarhlutfall á yfirstandandi mánuði. Þá getur þú látið hana bera saman þessar tölur með niðurstöðum síðasta mánaðar eða sama mánaðar í fyrra og reiknað út frávikin. Allt þetta er hægt að gera í sama yfirlitinu, sem gerir þér kleift að komast að orsök þekktra vandamála og jafnvel valið fellilistann til að fókusa á upplýsingar allt niður í stakar færslur.  

Greiningarskýrslan er mynduð úr hlutunum sem á að greina (til dæmis viðskiptamönnum, viðskiptamannaflokkum, sölumönnum o.s.frv. sem sett er fram sem línur) og greiningarfæribreytunum, sem er leiðin sem þú vilt til að greina hlutinn (t.d. hagnaðarútreikningar, samanburður á sölumagni og -upphæðum yfir tímabil eða samanburður á rauntölum og áætlunum, sýnt sem dálkar). 

Í viðbót við greiningarskýrslur, er hægt að stofna og skoða svipaðar upplýsingar í greiningaryfirliti, sem byggir á víddum. Frekari upplýsingar eru á [Greina gögn eftir víddum](bi-how-analyze-data-dimension.md)

## <a name="example"></a>Dæmi

Hægt er að setja upp þessar línur (hluti sem á að greina):  

- Tölvur  
- Skjáir  
- Aukahlutir  

Þá er hægt að setja upp þessa dálka (hvernig á að greina hlutina):  

- Sala gildandi mánaðar  
- Sala síðasta mánaðar  
- Sala síðasta mánaðar í prósentum  

## <a name="setting-up-line-and-column-layouts"></a>Uppsetning á útliti lína og dálka

Á síðunni **Greiningarskýrsla** er hægt að skoða mismunandi línu- og dálkaútlit sem eru sett upp á:

* Síðan **Sniðmát greiningarlínu** þar sem þú skilgreinir heiti skýrslunnar og hlutanna sem á að sýna í línum hennar og
* Síðan **Sniðmát greiningardálks** þar sem þú skilgreinir heiti dálkssniðmáts og greiningarfæribreyta sem birtast í skýrslunni sem dálkar. Hver lína á þessari síðu sýnir dálk í skýrslunni. 

Athuga skal að greiningarlínur og greiningardálkar eru óháð hvort öðru.  

Það fer eftir línunum og dálkunum sem hafa verið sett upp, [!INCLUDE[prod_short](includes/prod_short.md)] dregur saman niðurstöðu skýrslunnar á síðunni **Greiningarskýrsla** eins og sýnt er í eftirfarandi töflu.  

|- |Sala gildandi mánaðar|Sala síðasta mánaðar|Sala síðasta mánaðar í %|  
|-|-|-|-|  
|Tölvur| | | |  
|Skjáir| | | |  
|Varahlutir| | | |  
|Samtals| | | |  

Til dæmis er hægt að setja upp einn flokk af línum og ýmsa flokka af dálkaútlitum til að sýna mánaðarlegar og árlegar skýrslur.

## <a name="set-up-analysis-column-templates"></a>Seta upp greiningardálkssniðmát

Eftirfarandi ferli byggir á greiningaryfirlitum sölu. Skrefin eru svipuð fyrir innkaup og birgðagreiningaryfirlit.

Sniðmát greiningardálks inniheldur safn af línum, sem hver stendur fyrir greiningardálk sem þú vilt í greiningarskýrslunni. Ef skilgreina á dálk þarf að tengja greiningartegundarkóta við línuna. Þessi greiningartegundarkóði ákveður þá gerð frumgagna í birgðafærslunum sem greiningin verður byggð á. Upprunagögn geta innihalda kostnað, söluupphæð eða magn og tengdar virðisfærslur þeirra. Hægt er að setja upp eins mörg dálk- og línusniðmát og þarf og tengja þau síðan til að stofna nýja greiningarskýrslu.    

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Sniðmát söludálka** og velja síðan viðkomandi tengil.  
2. Velja fyrstu auðu línuna og fylltu út í reitina eftir þörfum.
3. Veljið **Dálkar** aðgerðina.  
4. Á síðunni **Greiningardálkar** eru reitirnir fylltir út til að tilgreina dálkana sem eiga að vera í greiningarskýrslunni.  

    > [!NOTE]  
    > Ef skilgreina á dálk þarf að fylla út reitinn  **Kóti greiningartegundar** (fyrir allar tegundir dálka nema **Reikniregla**). Kóði fyrir greiningartegund er settur upp á síðunni **Greiningartegund**.  
    
    Einnig, í reitnum **Fjárhagsfærslugerð**, ef þú velur **Birgðafærslur**, eru rauntölurnar úr birgðafærslunum afritaðar. Ef valdar eru **Birgðaáætlunarfærslur** eru áætlaðar tölur úr fjárhagsáætluninni afritaðar.  
5. Veldu **Í lagi** til að vista breytingarnar.  

## <a name="set-up-analysis-line-templates"></a>Setja upp greiningarlínusniðmát

Eftirfarandi ferli byggist á greiningarskýrslum fyrir sölu. Skrefin eru svipuð fyrir innkaup og birgðagreiningarskýrslur.

Sniðmát greiningarlínu inniheldur safn af línum, sem hver stendur fyrir greiningarlínu sem þú vilt í greiningarskýrslunni. Lína getur tilgreint eina vöru eða tiltekið svið vara, viðskiptamenn, lánardrottna eða flokka. Einnig er hægt að stofna reiknireglu í línu til að leggja saman allar hinar. Hægt er að setja upp eins mörg dálk- og línusniðmát og þarf og tengja þau síðan til að stofna nýja greiningarskýrslu.   

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Sniðmát sölulína** og velja síðan viðkomandi tengil.  
2. Veldu fyrstu auðu línuna og fylltu svo út í reitina eftir þörfum.
3. Veljið aðgerðina **Línur**.  
4. Á síðunni **Greiningarlínur** eru stofnaðar línur fyrir vörurnar, viðskiptamennina, lánardrottnana eða sölumennina sem tölur óskast um í greiingarskýrslunni. Fylla verður út reitina **Tegund**, **Svið** og **Lýsing**.  

> [!NOTE]  
> Til að stofna margar stakar línur fyrir hverja vöru, viðskiptamann o.s.frv. er einnig hægt að velja viðeigandi innsetningaraðgerð til að fylla út alla viðkomandi reiti í línunni. Hægt er að breyta línunum handvirkt ef þess þarf. Til að setja inn línur skal velja aðgerðina **Setja inn vörur** eða aðgerðina **Setja inn vöruflokka**.  

## <a name="create-a-new-sales-analysis-report"></a>Stofna nýjar sölugreiningarskýrslur

Eftirfarandi ferli byggist á greiningarskýrslum fyrir sölu. Skrefin eru svipuð fyrir innkaup og birgðagreiningarskýrslur.

Með greiningarskýrslum geturðu greint sölu samkvæmt lykilstærðum, svo sem sölutölum í upphæðum og magni, framlegð eða raunsölu í samanburði við áætlun. Einnig er hægt að nota greiningarskýrsluna til að greina meðalsöluverð og meta frammistöðu sölumanna.  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Sölugreiningaskýrslur** og velja síðan viðkomandi tengil.  
2. Á síðunni **Greiningarskýrslusala** skal velja aðgerðina **Nýtt**.
3. Reitirnir eru fylltir út eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Veljið aðgerðina **Breyta greiningarskýrslu**.
5. Á síðunni **Sölugreiningarskýrsla** skal velja aðgerðina **Sýna fylki**  

> [!NOTE]  
> Myndun samsetninga af línu- og dálkssniðmátum til að stofna skýrslu og tenging mismunandi heita við þau er valfrjáls. Ef þetta er gert þarftu ekki að velja sniðmát línu eða dálks á síðunni **Sölugreiningarskýrsla**. Þegar skýrsluheiti hefur verið valið er hægt að breyta línu- og dálkssniðmátum hvoru í sínu lagi og velja síðan skýrsluheitið aftur til að fá upphaflegu samsetninguna aftur.

## <a name="see-also"></a>Sjá einnig .

[Viðskiptagreind fjármála](bi.md)  
[Fjármál](finance.md)  
[Uppsetning Fjármála](finance-setup-finance.md)  
[Fjárhagur og bókhaldslyklar](finance-general-ledger.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
