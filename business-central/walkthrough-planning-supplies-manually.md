---
title: Kynning - Handvirk áætlun birgða | Microsoft Docs
description: Þessi kynning sýnir ferli áætlunar birgðapantana til að uppfylla nýja eftirspurn. Hægt er að hefja áætlun birgða með föstu millibili, t.d. á hverjum morgni eða á hverjum mánudegi, eða þegar tilkynning berst frá sölu eða framleiðslu, eftir því um hvers konar eftirspurn er að ræða.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 604a783f292b04c2609b8415d6b2ec6287f5cfcb
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5379803"
---
# <a name="walkthrough-planning-supplies-manually"></a>Kynning: Handvirk áætlun birgða

[!INCLUDE[complete_sample_data](includes/complete_sample_data.md)]  

Þessi kynning sýnir ferli áætlunar birgðapantana til að uppfylla nýja eftirspurn. Hægt er að hefja áætlun birgða með föstu millibili, t.d. á hverjum morgni eða á hverjum mánudegi, eða þegar tilkynning berst frá sölu eða framleiðslu, eftir því um hvers konar eftirspurn er að ræða. Í þessari kynningu verður notuð síðan **Pantanaáætlun**, einfalt birgðaáætlunarverkfæri sem byggir á handvirkri ákvarðanatöku í stað sjálfvirkrar áætlanagerðar sem byggir á færibreytum.  

## <a name="about-this-walkthrough"></a>Um kynninguna  
 Þessi kynning fjallar um eftirfarandi verk:  

-   Áætlun um innkaupapöntun fyrir framleiðslu hluta.  
-   Áætlun um millifærslupöntun til að uppfylla eftirspurn sölu.  
-   Áætlun um framleiðslupöntun fyrir margþrepa atriði.  

## <a name="roles"></a>Hlutverk  
 Þessi kynning sýnir þau verk sem framkvæmd eru með eftirfarandi hlutverkum notenda:  

-   Framleiðslustjóri  
-   Innkaupaaðili  
-   Sölupöntunarvinnsla  

## <a name="prerequisites"></a>Frumskilyrði  
 Áður en kynningin hefst þarf að setja upp [!INCLUDE[prod_short](includes/prod_short.md)]. Eftirtaldar breytingar þarf að gera á grunninum:  

-   Eyða öllum sölupöntunum vegna reiðhjóla.  
-   Stofna eina sölupöntun fyrir 10 reiðhjól hjá staðsetningunni EAST.  
-   Eyða öllum áætluðum og fastáætluðum framleiðsluáætlunum. Ekki eyða pöntunum sem þegar eru í gangi með færslum sem þegar eru skráðar.  

 Regla er að nota gögnin sem lagt er til í þessari kynningu vegna þess að þau gögn hafa nauðsynlegar skrár.  

## <a name="story"></a>Ferill  
 Erla, sem er framleiðslustjóri lítils framleiðslufyrirtækis, er um það bil að fara að áætla framleiðslu og innkaupapantanir til að uppfylla nýja eftirspurn í sölu.  

 Vegna þess að framleiðslan hefur fá stig framleiðsluuppskrifta og flæði pantana er tiltölulega hæggengt notar Erla síðuna **Pantanaáætlun** til að stofna framboðspantanir handvirkt, eitt framleiðsluskref í einu.  

 Í flóknara framleiðsluumhverfi er vinnublaðið fyrir áætlun notað til að gera áætlun um framboð sem byggir á vöruþáttum eins og enduráætlunartímabil, öryggisforskot, endurpöntunarmark og keyrslu útreikninga eftirspurnar allra framleiðslustiga sem steypt hefur verið saman.  

## <a name="setting-up-the-sample-data"></a>Uppsetning sýnigagna  
 Staðlaða CRONUS sýnifyrirtækið er eins og stendur með mikið af óáætlaðri eftirspurn. Í ólíkum verkefnum áætlana sem eru í þessari kynningu verður að víkja frá raunverulegu viðskiptaflæði með því að hundsa kröfur sem hafa gjalddaga sem stutt er í og nota þess í stað kröfur með gjalddaga sem er síðar.  

## <a name="using-the-order-planning-page"></a>Síðan Pantanaáætlun notuð  

Síðuna **Pantanaáætlun** er hægt að opna úr mörgum ólíkum staðsetningum:  

-   Framleiðsla, Áætlun  
-   Sala og markaðssetning, Vinnsla pantana  
-   Innkaup, Áætlun  
-   Að auki geturðu opnað þessa síðu fyrir tiltekna framleiðslupöntun með því að velja aðgerðina **Áætlanagerð** Action.

### <a name="to-use-the-order-planning-page"></a>Að nota síðuna „Pantanaáætlun“  

1.  Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Pantanaáætlun** og veldu síðan tengda tengilinn.  

     Eftir að síðan **Pantanaáætlun** opnast fyrst þarf að reikna áætlun til að sýna nýja eftirspurn frá því hún var reiknuð síðast.  

2.  Velja **Reikna áætlun** aðgerðina.  

     Áætlunarkerfið greinir hverja nýja eftirspurn sem hefur komið fram, svo sem nýja sölu eða framleiðslupantanir.  

     Magnið sem þörf er á fyrir hverja eftirspurnarlínu er reiknað út og byggir á heildarmagni sem til ráðstöfunar er. Útreikningurinn er gerður fyrir hverja pöntun fyrir sig. Það þýðir að pöntunin sem inniheldur eftirspurnarlínuna með fyrstu skila-/afhendingardagsetninguna er tekin fyrir fyrst. Eftir það eru allar aðrar eftirspurnarlínur reiknaðar í sömu röð, óháð skila- eða afhendingardagsetningu.  

3.  Ganga þarf úr skugga um að síðan **Pantanaáætlun** sé stækkuð og að reitir dálka séu af þeirri stærð að þeir sýni öll sjálfgefin heiti reita.  

     Þegar útreikningi er lokið þá sýnir síðan alla óuppfyllta eftirspurn sem línur pöntunarhauss sem hafa verið felldar saman, flokkað eftir nýjustu dagsetningu eftirspurnar.  

     Takið eftir að CRONUS hefur margar pantanir með óuppfyllta eftirspurn. Hver feitletruð áætlunarlína stendur fyrir pöntun, sölupöntun eða framleiðslupöntun; af þeim er að minnsta kosti ein pantanalína með sem uppfyllir ekki ráðstöfunarkröfur.  

4.  Í reitnum **Sýna eftirspurn sem** skal velja afmörkunina **Alla eftirspurn**.  

     Innan reitsins **Tegund eftirspurnar** má velja hvaða tegundir pantana á að birta.  

     Pantanir sem ekki eru vandamál varðandi tiltækt magn eru ekki sýndar. Ef engar pantanir eru til staðar þegar áætlun er reiknuð birtast skilaboð og engar áætlunarlínur birtast.  

## <a name="planning-a-purchase-order-to-fulfill-component-demand"></a>Innkaupapöntun áætluð til að uppfylla eftirspurn íhluta  
 Í þessu ferli er stofnuð innkaupapöntun fyrir íhluti sem þarf til framleiðslunnar.  

### <a name="to-plan-a-purchase-order-to-fulfill-component-need-in-production"></a>Til að áætla innkaupapöntun til að uppfylla þörf á íhlutum fyrir framleiðslu  

1.  Fyrsta línan er stækkuð (veljið táknið +).  
2.  Veljið fyrstu eftirspurnarlínuna, með vöru **LSU-15** og síðan **Sýna fylgiskjal** aðgerðina.  
3.  Opinni framleiðslupöntun er lokað til að fara aftur á síðuna **Pantanaáætlun**.  
4.  Í reitnum **Áfyllingarkerfið** eru **Innkaup** valin.  

     Sjálfgefna gildið er af birgðaspjaldinu eða birgðahaldseiningaspjaldinu, en því er hægt að breyta í einn af eftirtöldum valkostum:  

    -   **Innkaup** – Til að búa til innkaupapöntun.  
    -   **Millifærsla** – til að búa til millifærslupöntun.  
    -   **Framl.pöntun** – Til að búa til framleiðslupöntun.  

5.  Í reitnum **Framboð frá** þarf að velja eitt af eftirfarandi valmöguleikum til hliðsjónar við valið áfyllingarkerfi:  

    -   **Lánardrottinn** – Fyrir innkaup  
    -   **Birgðageymsla** – fyrir flutning  

     Ef reiturinn er ekki fylltur út þá koma fram villuboð þegar reynt er að stofna framboðspöntun.  

    > [!NOTE]  
    >  Hafi íhlutirnir uppsett sjálfgefin númer lánadrottna á birgðaspjaldi, þá verða línurnar endurstilltar.  

6.  Velja reitinn **Framboð frá**.  
7.  Á síðunni **Vörulisti lánardrottins** skal velja aðgerðina **Nýtt** og svo er lánadrottinn **30000** valinn.  
8.  Velja hnappinn **Í lagi** til að fara aftur á síðuna **Pantanaáætlun**.  
9. Afrita lánardrottinn **30000** í aðrar línur fyrir hátalaraíhlutina á þessari framleiðslupöntun.  

     Nú er hægt að stofna innkaupapöntun.  

10. Velja **búa til Pantanir** aðgerð. Síðan **Gera framboðspantanir** opnast.  
11. Í  **Pantanaáætlun** á flýtiflipanum **Gera pantanir fyrir** skal velja kostinn **Virk pöntun**.  
12. Á flýtiflipanum **Valkostir** í reitnum **Stofna innkaupapöntun** er kosturinn **Gera innkaupapantanir** valinn.  
13. Veldu hnappinn **Í lagi** til að stofna innkaupapantanir fyrir alla íhluti pöntunarinnar.  

     Innkaupapantanirnar hafa nú verið stofnaðar og vistaðar sem síðustu pantanir í listanum yfir innkaupapantanir.  

## <a name="planning-a-transfer-order-to-fulfill-sales-demand"></a>Millifærslupöntun áætluð til að uppfylla eftirspurn sölu  
 Í þessu ferli er eftirspurn áætluð út frá sölupöntun. Eftirspurnarlínur gefa sölulínur til kynna en ekki íhlutalínur eins og í framleiðslueftirspurn.  

### <a name="to-plan-a-transfer-order-to-fulfill-sales-demand"></a>Áætlun um millifærslupöntun til að uppfylla eftirspurn sölu  

1.  Bendillinn er færður á áætlunarlínu fyrir pöntun **2008**.  
2.  Stækka skal línuna og færa bendilinn á eftirspurnarlínu.  

     Sölupöntun **2008** er fyrir tíu hátalara af vöru **LS-120**, pantað af John Haddock Insurance Co.  

     Þá birtist skilgreint áfyllingarkerfi vörunnar og sjálfgefinn lánadrottinn.  

    > [!NOTE]  
    >  Neðst á síðunni eru fjórir upplýsingareitir. Í reitnum **Fyrsta tiltæka dagsetning** munu þeir tíu hlutir sem þörf er á vera til taks, fyrir framboðspöntun á innleið, níu dögum eftir núverandi lokadag. Ef þetta er of seint fyrir viðskiptamanninn þá sýnir reiturinn **Tiltækt fyrir millifærslu** 13 stykki vörunnar á annarri staðsetningu. Áætla þarf fyrir þessar birgðir.  

3.  Smellt er á **Tiltækt fyrir millifærslu** til að opna síðuna **Sækja annað framboð**.  
4.  Veldu hnappinn **Í lagi** til að bóka þau tíu eintök sem eru tiltæk.  

    > [!NOTE]  
    >  Í eftirspurnarlínuna hefur innkaupatillögu verið skipt út fyrir flutning frá staðsetningunni AÐAL. Aðgerðin **Búa til pantanir** stofnar flutning frá AÐAL til staðar þaðan sem eftirspurnin kemur. Reiturinn **Staðgenglar eru til** virkar á sama hátt.  

5.  Velja **búa til Pantanir** aðgerð. Síðan **Gera framboðspantanir** opnast.  
6.  Í  **Pantanaáætlun** á flýtiflipanum **Gera pantanir fyrir** skal velja kostinn **Virka pöntunin**.  
7.  Á flýtiflipanum **Valkostir** í reitnum **Stofna millifærslupöntun** skal velja kostinn **Gera millif.pantanir**.  
8.  Veldu hnappinn **Í lagi** til að stofna millifærslupöntun til að anna sölupöntunum.  

     Millifærslupöntun hefur nú verið gerð og vistuð í listanum sem síðasta pöntun í listanum yfir opnar millifærslupantanir.  

## <a name="planning-a-multilevel-production-order-to-fulfill-sales-demand"></a>Margþrepa millifærslupöntun áætluð til að uppfylla eftirspurn sölu  
 Í þessu ferli er gerð áætlun til að uppfylla eftirspurn sölu fyrir framleiðslu sem hefur mörg framleiðsluþrep þar sem hvert og eitt myndar háða eftirspurn framleiðslu.  

### <a name="to-plan-multilevel-production-to-fulfill-sales-demand"></a>Að áætla margra þrepa framleiðslu til að uppfylla eftirspurn sölu  

1.  Áætlunarlína með pöntun fyrir eftirspurn sölu **1001** er valin (stofnuð áður sem frumskilyrði).  

     Þessi eftirspurn er sölulína en varan hefur skilgreint áfyllingarkerfi sem er **Framl.pöntun**. Haldið er áfram til að bæta annarri bjöllu við íhlutaþörf hvers hjóls.  

2.  Veldu **Íhlutir** aðgerðina til að opna síðuna **Áætla Íhlutir** .  
3.  Í línunni með bjölluvörunni skal breyta reitnum **Magn á** úr **1** í **2**.  
4.  Á síðunni **Pantanaáætlun** þarf að meta möguleika fyrir pöntunina. Í þessu tilfelli eru engar aðrar leiðir til framboðs, engir staðgenglar, millifærslur, eða síðari afhending. Stofna þarf birgðapöntunina sem lögð er til, framleiðslupöntun.  
5.  Velja **búa til Pantanir** aðgerð til að stofna framleiðslupöntunina.  

     Á síðunni **Pantanaáætlun** sést að áætlunarlínan fyrir sölupöntun **1001** er ekki lengur til staðar og séð hefur verið um upphaflega eftirspurn sölu.  

6.  Glugganum **Pantanaáætlun** er lokað.  

     Nú væri hægt að velja að halda áfram í þessari valmynd og ljúka öllum áætlanagerðum. Þess í stað er nú farið í hlutverk framleiðslustjóra með því að fara í framleiðslupöntunina sem verið var að gera og opna síðuna **Pantanaáætlun**.  

 Framleiðslustjóri þarf að áætla sérstaka röð framleiðslupantana.  

### <a name="to-plan-a-specific-production-order"></a>Til að áætla sérstaka röð framleiðslupöntunar  

1.  Opna skal framleiðslupöntunina **101001**, fyrir tíu reiðhjól, sem var stofnuð með aðgerðinni **Gera pantanir**.  
2.  Opna síðuna **Íhlutir framl.pöntunar** til að athuga hvort staka bjallan endurspeglist í framleiðslupöntuninni.  
3.  Veldu aðgerðina **Áætlun**.  

     Síðan **Pantanaáætlun** opnast í útliti sem er alltaf síað niður á tiltekna framleiðslueftirspurn. Eftirspurn sölu er ekki sýnd. Reikna þarf áætlun áður en hægt er að sjá nokkra viðbótareftirspurn.  

4.  Velja **Reikna áætlun** aðgerðina.  

     Takið eftir að fjórar nýjar framleiðslupantanir koma fram sem óáætluð eftirspurn framleiðslu sem dregin er af pöntun **101001**. Nýju línurnar standa fyrir nýja eftirspurn framleiðslu frá millivörum sem þarf að stofna til að framleiða pöntunina.  

5.  Veldu aðgerðina **Stækka allt** til að fá yfirlit yfir alla framleiðslueftirspurnina fyrir framleiðslupantanirnar.  

     Til að leggja fram viðbótarupplýsingar um eftirspurnarlínur gæti verið ráðlegt að bæta reitunum **Magn eftirspurnar** og **Tiltækt magn eftirspurnar** í gluggann.  

     Nú þarf að bjóða fram tíu stykki af hverjum íhlut.  

     Athugið að fjórar af eftirspurnarlínunum hafa framleiðslupantanir áfyllingarkerfis. Þessir fjórir samsetningarhlutar eru annað framleiðslustig reiðhjólsins.  

     Sjálfgefnar stillingar áfyllingar eru þegar útfylltar og halda má áfram til að gera pantanir.  

6.  Velja **búa til Pantanir** aðgerð.  

     Áður er hnappurinn **Í lagi** er valinn ætti að lesa textann á flýtiflipanum **Pantanaáætlun**. Þessi texti er mikilvægur vegna þess að vitað er að reiðhjólið hefur nokkra framleidda íhluti—millivörur—í framleiðsluferli sínu sem gæti orðið eftirspurn eftir þegar þessi framleiðslupöntun hefur verið gerð.  

7.  Á síðunni **Gera framboðspantanir** í reitnum **Gera pantanir fyrir** veljið valkostinn **Allar línur** og veljið svo hnappinn **Í lagi** til að stofna framleiðslupöntun fyrir annað framleiðslustig pöntunarinnar.  

     Athugið að eftirspurn framleiðslu á efsta stigi fyrir framleiðslupöntun 101001 er ekki lengur til. Það þýðir að gerð hefur verið áætlun fyrir upphaflega eftirspurn framleiðslu fyrir millivörur.  

     Á síðunni **Pantanaáætlun** má reikna áætlun aftur til að gera áætlun um byggingu reiðhjólsins.  

8.  Velja aðgerðina **Reikna áætlun** til að endurreikna áætlun eins og mælt er fyrir um í meðfylgjandi Hjálpartexta.  

     Nýju línurnar tvær standa fyrir viðbótareftirspurn framleiðslu sem tengist millivörunum sem áætlun var gerð um í fyrri þrepum. Lagt er til að tvær framleiðslupantanir séu gerðar fyrir framboð á hjólnöfunum, ein fyrir 10 framnafir og ein fyrir 10 afturnafir.  

9. Veldu aðgerðina **Stækka allt** til að fá yfirlit yfir alla framleiðslueftirspurnina fyrir þessar tvær framleiðslupantanir.  

     Tillagan um framboðið gefur til kynna að fjórar innkaupapantanir verði gerðar vegna íhlutanna. Ákveðið er að gera pantanirnar sem lagt er til.  

10. Velja **búa til Pantanir** aðgerð.  
11. Í reitnum **Gera pantanir fyrir** veljið valkostinn **Allar línur** og veljið svo hnappinn **Í lagi**. Athuga þarf hvort viðbótareftirspurn er til staðar vegna framleiðslu yfirvörunnar, reiðhjólsins (sem selt er samkvæmt sölupöntun 1001).  
12. Velja **Reikna áætlun** aðgerðina.  

     Skilaboðin segja til um að allir tilskildir hlutir séu nú til staðar (að til sé framboð af þeim). Staðfesta fastáætlaðar framleiðslupantanir sem eru stofnaðar.  

13. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Fastáætluð framl.pantanir** og veldu síðan tengda tengilinn.  

     Á síðunni **Fastáætlað** farið yfir hvernig upphafs- og lokatími einstakra pantana er áætlaður út frá samsetningu framleiðslunnar. Íhlutir á neðsta þrepi eru framleiddir fyrst. Því þarf að áætla pantanir í mörgum þrepum eins og sýnt er í þessu verkflæði fyrir áætlanir.  

## <a name="see-also"></a>Sjá einnig  
 [Kynningar á viðskiptaferlum](walkthrough-business-process-walkthroughs.md)   
 [Kynning: Sjálfvirk áætlun birgða](walkthrough-planning-supplies-automatically.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]