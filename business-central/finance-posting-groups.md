---
title: Uppsetning bókunarflokks
description: Yfirlit yfir bókunarflokka sparar tíma og hjálpar við að koma í veg fyrir mistök þegar þú bókar færslur.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: posting setup, initialize
ms.search.form: 312, 313
ms.date: 01/24/2022
ms.author: bholtorf
ms.openlocfilehash: c67b5cf378b959228edb52d4f5331cde5a063b89
ms.sourcegitcommit: 66c78f6f04bfca6c0794b3299241ed65037b1c08
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/26/2022
ms.locfileid: "8029195"
---
# <a name="set-up-posting-groups"></a>Setja upp bókunarflokka

Staða hópar korta aðila eins og viðskiptavini, seljendur, atriði, auðlindir og sölu- og kaupskjöl til almennra reikninga. Þeir spara tíma og hjálpar við að koma í veg fyrir mistök þegar þú bókar færslur. Færslugildin fara á lyklana sem tilgreindir eru í bókunarhópnum fyrir þá tilgreindu einingu. Eina krafan er að þú hafir bókhaldslykla. Nánari upplýsingar er að finna í [Uppsetning bókhaldslykilsins](finance-setup-chart-accounts.md).  

Bókunarflokkar falla undir þrjú atriði:  

* Almennt - Tilgreindu hverjum þú selur og kaupir frá og hvað þú selur og hvað þú kaupir. Þú getur líka sameinað hópa til að tilgreina hluti eins og rekstrarreikninga til að birta eða nota hópa til að sía skýrslur.  
* Sérstakur - Notaðu söluskjöl, til dæmis, í stað þess að senda beint í fjárhag. Þegar þú býrð til færslur í viðskiptamannabókinni, eru samsvarandi færslur gerðar í fjárhagnum.  
* Skattur - Tilgreindu skattprósenturnar og útreikningsgerðir sem eiga við um hverjum þú selur og kaupir frá og hvað þú selur og hvað þú kaupir.

Í eftirfarandi köflum er lýst bókunarflokkum undir hverju Umbrella.  

## <a name="general-posting-groups"></a>Almennir Bókunarflokkar

Eftirfarandi tafla lýsir almennum bókunarflokkum.

| Tegund | Description |
| --- | --- |
| Almennir viðskiptabókunarflokkar |Úthlutaðu þessum hópi á viðskiptavini og lánardrottna til að tilgreina hverjum þú selur og hverjum þú kaupir frá. Settu þetta upp á síðunni fyrir **Alm. viðskiptabókunarflokkar**. Þegar þú gerir það skaltu hugsa um hversu marga hópa þú þarft fyrir niðurbrog á sölu og kaupum. Til dæmis geturðu flokkað viðskiptavini og lánardrottna eftir svæði, eða eftir tegund viðskipta. |
| Almennir vörubókunarflokkar |Úthlutaðu þessum hópi á hluti og tilföng til að tilgreina hvað þú selur og hvað þú kaupir. Setjið þetta upp á síðunni **Alm. vörubókunarflokkar**. Þegar þú gerir það skaltu hugsa um fjölda hópa sem þú þarft til að brjóta niður sölu eftir vöru (atriði og foprði) og kaup eftir vörum. Til dæmis, skaltu skipta þessum hópum eftir hráefnum, smásölu, tilföngum, getu og svo framvegis. |
| Uppsetning almenns bókunargrunns |Sameina viðskipti og vörubókunarflokka, og veldu lyklana til að bóka á. Fyrir hverja samsetningu viðskipta- og vöruskiptahópa er hægt að tengja saman fjölda aðalbókarreikninga. Til dæmis þýðir þetta að hægt er að bóka sölu sömu vöru á marga sölureikninga í fjárhag þegar viðskiptavinir eru tengdir við marga viðskiptabókunarflokka. Settu þetta upp á síðunni **Almennur bókunargrunnur**. |

## <a name="specific-posting-groups"></a>Ákveðnir Bókunarflokkar

Eftirfarandi tafla lýsir bókunarflokkana sem eru sérstaklega gerðir af gögnum.

|Tegund | Description |
| --- | --- |
| Bókunarflokkar viðskm. |Skilgreindu lyklana sem þú vilt nota þegar þú sendir inn færslur viðskiptakrafa. Ef þú notar birgðir með kröfum eru það almenni viðskiptabókunarflokkurinn sem er úthlutaður viðskiptavininum þínum og almenni vörubókunarflokkurinn sem er úthlutaður birgðavöru sem ákvarða lyklana sem sölupöntunarlínur eru bókaðar á. Sjá *almenna viðskiptabókunarflokka* og *almenna vörubókunarflokka* í [kaflanum Almennir Bókunarflokkar](#general-posting-groups). Settu þetta upp á síðunni **Bókunarflokkar viðskiptamanna**. |
| Bókunarflokkar lánardrottna |Tilgreindu hvar á að bóka færslur fyrir viðskiptaskuldir, þjónustureikninga og greiðsluafsláttarreikninga. Þetta er svipað og bókunarflokkur viðskiptamanns. Settu þetta upp á síðunni **Bókunarflokkar lánardrottna**. |
| Birgðabókunarflokkar |Skilgreindu birgðabókunarflokka sem þú úthlutar síðan á viðeigandi vörureikninga á síðunni **Uppsetning birgðabókunar**. Síðan þegar bókaðar eru færslur sem tengjast vöru þá bókar kerfið í fjárhagsreikninginn sem settur var upp fyrir þá samsetningu birgðabókunarflokks og birgðageymslu sem tengist vörunni. Birgðabókunarflokkar bjóða einnig upp á góða leið til að skipuleggja birgðir þínar, þannig að þú getur aðskilið hluti eftir bókunarflokkum þegar þú býrð til skýrslur. Settu þetta upp á síðunni **Birgðabókunarflokkar**. |
| Bókunarflokkar bankareikninga |Skilgreinið fjárhagsreikningana sem bankareikningsfærslurnar eru bókaðar á. Til dæmis getur þetta einfalt ferlið við að rekja færslr og samræma bankareikninga. Settu þetta upp á síðunni **Bókunarflokkar bankareikninga**. Mælt er með að þessir fjárhagsreikningar hafi **reitinn bein bókun** stillt á *Nr*. |
| Bókunarflokkur eigna |Skilgreina reikninga fyrir mismunandi gerðir útgjalda og kostnað, svo sem kaupkostnað, uppsafnaðan afskriftir, kaupkostnað við ráðstöfun, uppsafnað afskriftir við förgun, hagnað af sölu, tapi á förgun, viðhaldskostnaði og afskriftargjöldum. Settu þetta upp á síðunni **Eignabókunarflokkar**. |

## <a name="tax-posting-groups"></a>Skattbókunarflokkar

Eftirfarandi tafla lýsir skatttengdum bókunarflokkum.

| Tegund | Description |
| --- | --- |
| Skattaviðskiptabókunarflokkar |Ákveða hvernig á að reikna og bóka söluskatti fyrir viðskiptavini og lánardrottna. Setjið þetta upp á síðunni **Skattaviðskiptabókunarflokkar**. Þegar þú gerir það skaltu athuga hversu marga hópa þú þarft. Til dæmis getur þetta oltið á þáttum eins og staðbundinni löggjöf og hvort þú stundar viðskipti innanlands og á alþjóðavettvangi. |
| Skattavörubókunarflokkar |Tilgreindu skattaútreikninga sem þarf til að fá þær tegundir af forða sem þú kaupir eða selur. |
| Uppsetning skattbókunar |Sameina viðskiptabókunarflokk skatta og vörubókunarflokk skatta. Þegar þú fyllir inn almenna færslubókarlínu, innkaupalínu, eða sölulínu, munum við líta á samsetninguna til að bera kennsl á lyklana sem nota skal. |

## <a name="example-of-linking-posting-groups"></a>Dæmi um tengingu bókunarflokka

Hér er sviðsmynd.  

Þessar bókunarflokkar eru valdir á viðskiptamannaspjaldinu:  

* Almennur viðskiptabókunarflokkur
* Bókunarflokkur viðskm.  

Þessar bókunarflokkar eru valdir á birgðaspjaldinu:  

* Almennir vörubókunarflokkar  
* Birgðabókunarflokkur  

Þegar þú býrð til söluskjal, notar söluhausinn upplýsingar úr viðskiptamannaspjaldinu og sölulínur nota upplýsingar af birgðaspjaldinu.  

* Tekjubókunin (rekstrarreikningur) er ákvarðaður af samsetningu almennra viðskiptabókunarflokks og almenns vörubókunarflokks.  
* Bókun viðskiptakrafa (efnahagsreikningur) er ákvörðuð af bókunarflokki viðskiptamanni.  
* Birgðabókun (efnahagsreikningur) er ákvörðuð af birgðabókunarlooknum.  
* Kostnaður seldra vara (rekstrarreikningur) er ákvðarðaður af sameiningu almenns viðskiptabókunarflokks og almenns vörubókunarflokk.  

Uppsetningin þín ákvarðar hvenær bókun á sér stað. Til dæmis er tímasetning ákvörðuð af því þegar þú gerir reglubundna starfsemi, svo sem birgðakostnað eða birgðafærslum.

## <a name="copying-posting-setup-lines"></a>Bókunargrunnslínur afritaðar

Því fleiri vörur og viðskiptabókunarflokk sem þú ert með því fleiri línur sérðu á síðunni almennur bókunargrunnur. Vegna þessa gæti þurft að færa inn mikið af gögnum til að setja upp almennan bókunargrunn fyrir fyrirtækið. Þó að samsetningar viðskipta- og vörubókunarflokkanna séu margar er hægt að bóka þær saman í einn fjárhagsreikning. Til að draga úr handvirkum færslum skal afrita fjárhagsreikninga úr línu á síðunni **Alm. bókunargrunnur**.

## <a name="set-up-posting-groups-on-the-go"></a>Setja upp bókunarflokka á ferðinni

Til að fá notendur ræsa hraðar er [!INCLUDE[prod_short](includes/prod_short.md)] boðið upp á aðstoð í gegnum tilkynningar um vantar fjárhagsreikninga í mismunandi bókunarflokka uppsetningar í skjölum. Til að fá þessar tilkynningar þarf að ganga úr skugga um að **fjárhagsreikningurinn vanti í bókunarflokk eða tilkynningu um uppsetningu og að** Tilkynning sé valin á **síðunni tilkynningar sem hægt er að komast í** frá **breytingunni þegar reiturinn tilkynningar er færð** inn á **síðuna mínar stillingar**.  

Þegar unnið er í skjali sem notar bókunarflokk eða-uppsetningu sem nauðsynlegur reikningur vantar kemur upp tilkynning. Veldu hlekkinn í notificationtil að opna síðu þar sem þú getur gert viðeigandi breytingar, gefið þér heimild til þess.  

> [!NOTE]
> Til að taka þig beint út í bókunarflokkinn eða uppsetninguna sem almennur Fjárhagslykill vantar fyrir [!INCLUDE[prod_short](includes/prod_short.md)] verður að stofna frátakaflokk eða-uppsetningu. Bókunarflokkar og uppsetningar eru leið fyrir endurskoðandann til að stýra því hvernig færslur eru bókaðar í fjárhag, þannig að eins er bara stofnun bókunarflokka og uppsetningar ekki leyfðar í fyrirtækinu þínu.  
> 
> Ef svo er þarf að gera **fjárhagsreikninginn óvirkan í bókunarflokki eða** tilkynningu og vinna síðan hjá endurskoðanda til að gera viðkomandi breytingar á bókunarflokknum, uppsetningunni eða skjalinu. Þetta er mikilvægt skref, því þegar skjöl eru bókuð eru ekki hægt að eyða öllum bókunarflokkum sem eru ranglega notaðir vegna þess að fjárhagsfærslur hafa stofnast fyrir þær. 

## <a name="troubleshooting-posting-group-errors"></a>Úrræðaleita villur bókunarflokks

Bókunarflokkar eru með ítarlegustu hlutunum til að setja upp í [!INCLUDE[prod_short](includes/prod_short.md)]. Ef þeir eru ekki settir upp á réttan hátt geta villur komið upp þegar skjöl eða færslubókarlínur eru bókaðar. Til dæmis stafa þessar villur yfirleitt af mistökum í því hvernig almennum fjárhagslyklum er úthlutað eða hvernig bókunarflokkar eru sameinaðir.

Þegar eitthvað er að mun [!INCLUDE[prod_short](includes/prod_short.md)] birtast á síðunni **Villuboð**. Síðan **Villuboð** getur auðveldað það að greina og leysa úr vandanum. Síðan býður upp á lýsingu á villunni sem bendir á uppsetningu bókunarflokksins sem þarfnast skoðunar. Til dæmis geta skilaboðin verið: „Í fyrirframgreiðslureikning sölu vantar bókunargrunn.“ Einnig er tengill til að opna síðuna þar sem rót vandans liggur þannig að hægt sé að leysa úr honum á fljótlegan hátt.  

> [!NOTE]
> Villumeðhöndlunin sem lýst er hér að ofan er ekki í boði fyrir vöru, tilfang, starfsmann og færslubók eigna eða fyrir fjárhagslykla sem bætt er við í staðbundnum útgáfum bókunarflokka.

## <a name="see-also"></a>Sjá einnig .
[Fjárhagur og bókhaldslyklar](finance-general-ledger.md)  
[Uppsetning Fjármála](finance-setup-finance.md)  
[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
