---
title: Stofna greiningarskýrslur| Microsoft Docs
description: Lýsir því hvernig stofna skal nýjar greiningarskýrslur fyrir sölu, innkaup og birgðir og búa til greiningarsniðmát.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bi, power BI, analysis, KPI
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 023511c44e50318555f7e0ce3ce1f20bd0dfa35e
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5382530"
---
#  <a name="create-analysis-reports"></a>Stofna greiningarskýrslur
Sölustjórar þurfa að greina veltu, brúttóhagnað og aðrar lykilstærðir varðandi sölu með reglulegu millibili. Innkaupaaðilar hafa meiri áhuga á að greina innkaupamagn, fylgjast með frammistöðu birgja og innkaupaverði. Vöru- og birgðastjórar þurfa hins vegar upplýsingar um birgðaveltu, greiningu á hreyfingu birgða og upplýsingar um birgðavirði.  

Hægt er að nota greiningarskýrslur til að stofna sérsniðnar skýrslur sem byggðar eru á upplýsingum um bókaðar færslur, t.d. sölu, innkaup, millifærslur og birgðaleiðréttingar. Í sérsníðanlegri skýrslu getur notandi sameinað, borið saman og sett fram frumgögnin sem eru upprunnin í birgðafjárhag (með tengdum virðisfærslum) á ýmsan þann hátt sem hann kýs. Greiningarskýrslan er því mjög svipuð veltitöfluskýrslu í Microsoft Excel.  

Hægt er að stofna sérsniðna skýrslu sem tekur fyrir lykilreikninga og heildarveltu þeirra bæði í magni og upphæðum, brúttóhagnað og brúttóhagnaðarhlutfall í gildandi mánuði, og fá samanburð við niðurstöður fyrri mánaða eða sama mánaðar á síðasta ári, og reikna út frávik. Allt þetta er hægt að gera í sama yfirliti, með möguleika á að komast beint að orsök vandamála með því að smella á hnappinn í fellilistanum til að fá aðgang að upplýsingum um einstakar færslur.  

Greiningarskýrslan er mynduð úr hlutunum sem á að greina, til dæmis viðskiptamönnum, viðskiptamannaflokkum, sölumönnum o.s.frv. sem settir eru fram sem línur, og greiningarfæribreytunum, það er, aðferðinni sem á að beita við að greina hlutina, sem settar eru fram í dálkum, eins og t.d. hagnaðarútreikningar, samanburður á sölumagni og -upphæðum yfir tímabil eða samanburður á rauntölum og áætlunum.

Í viðbót við greiningarskýrslur, er hægt að stofna og skoða svipaðar upplýsingar í greiningaryfirliti, sem byggir á víddum. Nánari upplýsingar er að finna í [Greina gögn eftir víddum](bi-how-analyze-data-dimension.md).

## <a name="example"></a>Dæmi  
Hægt er að setja upp línur eins og þessar:  
- Tölvur  
- Skjáir  
- Varahlutir  

Síðan er hægt að setja upp dálka eins og þessa:  

- Sala gildandi mánaðar  
- Sala síðasta mánaðar  
- Sala síðasta mánaðar í prósentum  

## <a name="setting-up-line-and-column-layouts"></a>Uppsetning á útliti lína og dálka  
 Á siðunni **Greiningarskýrsla** er hægt að skoða mismunandi línu- og dálkaútlit í samræmi við línurnar eða línusniðmátin sem eru sett upp á síðunni **Greiningarlínusniðmát**. Hægt er að skilgreina heiti skýrslunnar og hlutanna sem á að sýna í línum hennar. Dálkarnir eru settir upp á síðunni **Greiningardálkssniðmát**. Hægt er að tilgreina heiti dálkssniðmátsins og greiningarfæribreytanna sem á að sýna í skýrslunni sem dálka. Á síðunni **Greiningardálkssniðmát** sýnir hver lína dálk í skýrslunni. Athuga skal að greiningarlínur og greiningardálkar eru óháð hvort öðru.  

Það fer eftir línunum og dálkunum sem hafa verið sett upp, mun [!INCLUDE[prod_short](includes/prod_short.md)] draga saman niðurstöðu skýrslunnar á síðunni **Greiningarskýrsla** eins og sýnt er í eftirfarandi töflu.  

|- |Sala gildandi mánaðar|Sala síðasta mánaðar|Sala síðasta mánaðar í %|  
|-|-|-|-|  
|Tölvur| | | |  
|Skjáir| | | |  
|Varahlutir| | | |  
|Samtals| | | |  

 Til dæmis er hægt að setja upp eitt safn af línum og mörg af dálkssniðmátum til að sýna annars vegar mánaðarskýrslu og hins vegar skýrslu yfir heilt ár.

 ## <a name="to-set-up-analysis-column-templates"></a>Uppsetning greinignardálkssniðmáta
Eftirfarandi ferli byggist á greiningaryfirliti fyrir sölu. Skrefin eru svipuð fyrir innkaup og birgðagreiningaryfirlit.

Í greiningarskýrslu eru greiningarfæribreyturnar sýndar sem dálkar. Hægt er að tilgreina dálkana sem eiga að vera með í greiningarskýrslunni með því að setja upp greingardálkssniðmát.  

Í sniðmáti er safn lína sem stendur fyrir greingardálkana sem eru sýndir í greiningarskýrslunni. Ef skilgreina á dálk þarf að tengja greiningartegundarkóta við línuna. Þessi greiningartegundarkóði ákveður þá gerð frumgagna í birgðafærslunum sem greiningin verður byggð á. Upprunagögn innihalda kostnað, söluupphæð eða magn og tengdar virðisfærslur þeirra. Hægt er að setja upp eins mörg dálk- og línusniðmát og þarf og tengja þau síðan til að stofna nýja greiningarskýrslu.    

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Dálkssniðmát Sales** og veldu síðan tengda tengilinn.  
2. Veljið fyrstu auðu línuna og fyllið svo út í reitina eins og þörf krefur.
3. Veljið **Dálkar** aðgerðina.  
4. Á síðunni **Greiningardálkar** eru reitirnir fylltir út til að tilgreina dálkana sem eiga að vera með í greiningarskýrslunni.  

    > [!NOTE]  
    >   Ef skilgreina á dálk þarf að fylla út reitinn  **Kóti greiningartegundar** (fyrir allar tegundir dálka nema **Reikniregla**). Kóði fyrir greiningartegund er settur upp á síðunni **Greiningartegund**.  
    Einnig, í reitnum **Fjárhagsfærslugerð**, ef þú velur **Birgðafærslur**, eru rauntölurnar úr birgðafærslunum afritaðar. Ef valdar eru **Birgðaáætlunarfærslur** eru áætlaðar tölur úr fjárhagsáætluninni afritaðar.  
5.  Velja hnappinn **Í lagi** til að vista breytingarnar.  

## <a name="to-set-up-analysis-line-templates"></a>Uppsetning greingarlínusniðmáta  
Eftirfarandi ferli byggist á greiningarskýrslum fyrir sölu. Skrefin eru svipuð fyrir innkaup og birgðagreiningarskýrslur.

Í greiningarskýrslu eru greiningarhlutirnir sýndir í línunum. Hægt er að tilgreina línurnar sem eiga að vera með í greiningarskýrslunni með því að setja upp greiingarlínusniðmát.  

Í sniðmáti er safn lína sem stendur fyrir greingarlínurnar sem eru sýndar í greiningarskýrslunni. Lína getur tilgreint eina vöru eða tiltekið svið vara, viðskiptamenn, lánardrottna eða flokka. Einnig er hægt að stofna reiknireglu í línu til að leggja saman allar hinar. Hægt er að setja upp eins mörg dálk- og línusniðmát og þarf og tengja þau síðan til að stofna nýja greiningarskýrslu.    

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Línusniðmát Sales** og veldu síðan tengda tengilinn.  
2. Veljið fyrstu auðu línuna og fyllið svo út í reitina eins og þörf krefur.
3. Veljið aðgerðina **Línur**.  
4. Á síðunni **Greiningarlínur** eru stofnaðar línur fyrir vörurnar, viðskiptamennina, lánardrottnana eða sölumennina sem tölur óskast um í greiingarskýrslunni. Fylla verður út reitina **Tegund**, **Svið** og **Lýsing**.  

> [!NOTE]  
>   Þegar stofna á margar stakar línur fyrir hverja vöru, viðskiptamann o.s.frv. er einnig hægt að velja viðeigandi innsetningaraðgerð til að fylla út alla viðkomandi reiti í línunni. Hægt er að breyta línunum handvirkt ef þess þarf. Til að setja inn línur skal velja aðgerðina **Setja inn vörur** eða aðgerðina **Setja inn vöruflokka**.  

## <a name="to-create-a-new-sales-analysis-report"></a>Nýjar sölugreiningarskýrslur stofnaðar
Eftirfarandi ferli byggist á greiningarskýrslum fyrir sölu. Skrefin eru svipuð fyrir innkaup og birgðagreiningarskýrslur.

Greiningarskýrslur eru notaðar til að til að greina sölu samkvæmt lykilstærðum sem notandi velur sjálfur, svo sem sölutölum í upphæðum og magni, framlegð eða raunsölu í samanburði við áætlun. Einnig er hægt að nota skýrsluna til að greina meðalsöluverð og meta frammistöðu sölumanna.  

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Sölugreiningarskýrslur** og veldu síðan tengda tengilinn.  
2. Á síðunni **Greiningarskýrslusala** skal velja aðgerðina **Nýtt**.
3. Fyllið inn reitina eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Veljið aðgerðina **Breyta greiningarskýrslu**.
5. Á síðunni **Sölugreiningarskýrsla** skal velja aðgerðina **Sýna fylki**  

> [!NOTE]  
>   Myndun samsetninga af línu- og dálkssniðmátum til að stofna skýrslu og tenging mismunandi heita við þau er valfrjáls. Ef þetta er gert og skýrsluheiti valið þarf ekki að velja línu- og dálkssniðmát á síðunni **Sölugreiningarskýrsla**. Þegar skýrsluheiti hefur verið valið er hægt að breyta línu- og dálkssniðmátum hvoru í sínu lagi og velja síðan skýrsluheitið aftur til að fá upphaflegu samsetninguna aftur.

## <a name="see-also"></a>Sjá einnig
[Viðskiptaupplýsingar](bi.md)  
[Fjármál](finance.md)  
[Uppsetning Fjármála](finance-setup-finance.md)  
[Fjárhagur og bókhaldslyklar](finance-general-ledger.md)  
[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]