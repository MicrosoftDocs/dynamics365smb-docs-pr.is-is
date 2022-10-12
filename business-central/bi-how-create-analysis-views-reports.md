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
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/30/2022
ms.locfileid: "9606198"
---
# <a name="create-analysis-reports"></a>Stofna greiningarskýrslur

Sölustjórar þurfa að greina veltu, brúttóhagnað og aðrar vísbendingar um afköst lykla sölu með reglulegu millibili. Kaupendur hafa meiri áhuga á breytilegum innkaupum á bindiverði, afköstum lánardrottna og innkaupsverði. Vöru- og birgðastjórar þurfa hins vegar upplýsingar um birgðaveltu, greiningu á hreyfingu birgða og upplýsingar um birgðavirði. Svo það er engin Ein stærð-passar-öll Greiningarskýrsla.

Hægt er að sérsníða greiningarskýrslur eftir færslum af bókuðum færslum, t.d. sölu, innkaupum, flutningum og birgðaleiðréttingar. Í sérhannaðri skýrslu er hægt að sameina frumgögn, sem fengin eru úr birgðahöfuðbók (með tengdum virðisfærslum), í samanburði og koma fram í lýsandi notendaskilgreindum leiðum. Greiningarskýrslan er því mjög svipuð veltitöfluskýrslu í Microsoft Excel.  

Þannig að til dæmis er hægt að búa til sérsniðna skýrslu sem einblínir á lykillykla að því er varðar heildarafurðaveltu í upphæðum og magni sem selt er, brúttóframlegð og hlutfall af Framlegð í gildandi mánuði. Þá er hægt að hafa það borið saman þær tölur við niðurstöður frá fyrri mánuðum eða sama mánuð í fyrra og reikna frávik. Allt þetta er hægt að gera í einni og sömu skoðunni, sem gerir kleift að sigla til valda auðkenna vandamálasvæða og jafnvel velja fellistiga að núlli í smáatriðum alla leið niður á stig einstakra færslna.  

Greiningarskýrslan samanstendur af hlutum sem á að greina (eins og viðskiptamenn, Viðskiptavinaflokkar, Sölufólk og svo framvegis, táknaðir sem línur) og greiningarfæribreytuna, sem er sú leið sem á að greina hlutinn (s.s. framlegð útreikninga, reglubundið samanburðarmagn af söluupphæðum og bindum eða með reglubundnum samanburði á raunverulegum og áætluðum tölum, sýndar sem dálkar). 

Auk greiningarskýrslna er hægt að stofna og skoða svipaðar upplýsingar í greiningaryfirlitum (Byggt á víddum). Frekari upplýsingar er að greina í [greiningu gagna eftir víddum](bi-how-analyze-data-dimension.md).

## <a name="example"></a>Dæmi

Hægt er að setja upp þessar línur (hluti sem á að greina):  

- Tölvur  
- Skjáir  
- Aukahlutir  

Þá er hægt að setja upp þessa dálka (Hvernig sem hlutirnir eiga að vera greindir):  

- Sala gildandi mánaðar  
- Sala síðasta mánaðar  
- Sala síðasta mánaðar í prósentum  

## <a name="setting-up-line-and-column-layouts"></a>Uppsetning línu-og dálkauppsetningar

**Á síðunni Greiningarskýrsla** er hægt að skoða mismunandi línu-og dálkauppsetningar sem settar eru upp á:

* **Síðan Greiningarlínusniðmát** þar sem notandi skilgreinir heiti skýrslunnar og hlutina sem á að sýna í línunum í skýrslunni og
* **Síðan greiningardálkssniðmát** þar sem heiti dálkssniðmátsins er skilgreint og greiningarfæribreytur sem sýna í skýrslunni sem dálka. Hver lína á þessari síðu táknar dálk í skýrslunni. 

Athuga skal að greiningarlínur og greiningardálkar eru óháð hvort öðru.  

Á grundvelli þeirra lína og dálka sem eru sett upp, [!INCLUDE[prod_short](includes/prod_short.md)] eru niðurstöður skýrslunnar settar saman á **síðunni Greiningarskýrsla** eins og sýnt er í eftirfarandi töflu.  

|- |Sala gildandi mánaðar|Sala síðasta mánaðar|Sala síðasta mánaðar í %|  
|-|-|-|-|  
|Tölvur| | | |  
|Skjáir| | | |  
|Varahlutir| | | |  
|Samtals| | | |  

Til dæmis er hægt að setja upp einn flokk af línum og nokkra flokka dálkauppsetningar til að sýna mánaðarlegar og ársskýrslur, eftir því sem við á.

## <a name="set-up-analysis-column-templates"></a>Setja upp greiningardálkssniðmát

Eftirfarandi ferli er byggt á sölugreiningaryfirlitum. Skrefin eru svipuð fyrir innkaup og birgðagreiningaryfirlit.

Greiningardálkssniðmát inniheldur línur sem tákna hverja greiningardálk sem á í greiningarskýrslunni. Ef skilgreina á dálk þarf að tengja greiningartegundarkóta við línuna. Þessi greiningartegundarkóði ákveður þá gerð frumgagna í birgðafærslunum sem greiningin verður byggð á. Í frumgögnum getur verið kostnaður, söluupphæð eða magn og tengdar virðisfærslum þeirra. Hægt er að setja upp eins mörg dálkssniðmát og þarf og nota þau svo til að stofna nýjar greiningarskýrslur.    

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknið, færa inn **Sniðmát** söludálka og velja síðan tengda tengilinn.  
2. Veljið fyrstu auðu línuna og fyllið svæðin í eftir þörfum.
3. Veljið **Dálkar** aðgerðina.  
4. **Á síðunni Greiningardálkar** er fyllt í reitina í til að tilgreina þá dálka sem óskað er eftir í greiningarskýrslunni.  

    > [!NOTE]  
    > Ef skilgreina á dálk þarf að fylla út reitinn  **Kóti greiningartegundar** (fyrir allar tegundir dálka nema **Reikniregla**). Kóði fyrir greiningartegund er settur upp á síðunni **Greiningartegund**.  
    
    Einnig, í reitnum **Fjárhagsfærslugerð**, ef þú velur **Birgðafærslur**, eru rauntölurnar úr birgðafærslunum afritaðar. Ef valdar eru **Birgðaáætlunarfærslur** eru áætlaðar tölur úr fjárhagsáætluninni afritaðar.  
5. Veldu **í lagi** til að vista breytingarnar.  

## <a name="set-up-analysis-line-templates"></a>Setja upp Greiningarlínusniðmát

Eftirfarandi ferli byggist á greiningarskýrslum fyrir sölu. Skrefin eru svipuð fyrir innkaup og birgðagreiningarskýrslur.

Greiningarlínusniðmát inniheldur línur sem tákna hverja greiningarlínu sem á að nota í greiningarskýrslunni. Lína getur tilgreint eina vöru eða tiltekið svið vara, viðskiptamenn, lánardrottna eða flokka. Einnig er hægt að stofna reiknireglu í línu til að leggja saman allar hinar. Hægt er að setja upp eins mörg línusniðmát og þarf og nota þau svo til að stofna nýjar greiningarskýrslur.   

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknið, færa inn **Sölulínusniðmát** og velja síðan tengda tengilinn.  
2. Valin er fyrsta tóma línan og reitirnir fylltir út eftir þörfum.
3. Veljið aðgerðina **Línur**.  
4. Á síðunni **Greiningarlínur** eru stofnaðar línur fyrir vörurnar, viðskiptamennina, lánardrottnana eða sölumennina sem tölur óskast um í greiingarskýrslunni. Fylla verður út reitina **Tegund**, **Svið** og **Lýsing**.  

> [!NOTE]  
> Einnig er hægt að stofna margar einstakar línur fyrir hverja vöru, viðskiptamann o. þ. frv., velja viðeigandi setja inn valkost til að fylla út alla viðeigandi reiti í línunni. Hægt er að breyta línunum handvirkt ef þess þarf. Til að setja inn línur er valið að **Setja inn vörur** eða **Setja inn aðgerðina Vöruflokkar**.  

## <a name="create-a-new-sales-analysis-report"></a>Stofna nýja sölugreiningarskýrslu

Eftirfarandi ferli byggist á greiningarskýrslum fyrir sölu. Skrefin eru svipuð fyrir innkaup og birgðagreiningarskýrslur.

Með greiningarskýrslum er hægt að greina Dynamics sölu þína samkvæmt afkastavísum lykla sölu, svo sem sölu veltu bæði í upphæðum og magni, framlegð eða framvindu raunverulegrar sölu á móti fjárhagsáætlun. Einnig er hægt að nota greiningarskýrslur til að greina meðalsöluverð og meta afköst söluheraflans.  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknið, færa inn **sölugreiningarskýrslur**, velja síðan tengda tengilinn.  
2. Á síðunni **Greiningarskýrslusala** skal velja aðgerðina **Nýtt**.
3. Reitirnir eru fylltir út eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Veljið aðgerðina **Breyta greiningarskýrslu**.
5. Á síðunni **Sölugreiningarskýrsla** skal velja aðgerðina **Sýna fylki**  

> [!NOTE]  
> Myndun samsetninga af línu- og dálkssniðmátum til að stofna skýrslu og tenging mismunandi heita við þau er valfrjáls. Ef þetta er gert þarf ekki að velja línu-og dálkssniðmát á **síðunni Sölugreiningarskýrsla**. Þegar skýrsluheiti hefur verið valið er hægt að breyta línu- og dálkssniðmátum hvoru í sínu lagi og velja síðan skýrsluheitið aftur til að fá upphaflegu samsetninguna aftur.

## <a name="see-also"></a>Sjá einnig .

[Upplýsingarit um Fjármál fyrirtækja](bi.md)  
[Fjármál](finance.md)  
[Uppsetning Fjármála](finance-setup-finance.md)  
[Fjárhagur og bókhaldslyklar](finance-general-ledger.md)  
[Vinna með[!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
