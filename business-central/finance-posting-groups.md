---
title: Uppsetning bókunarflokks
description: Yfirlit yfir bókunarflokka sparar tíma og hjálpar við að koma í veg fyrir mistök þegar þú bókar færslur.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: posting setup, initialize
ms.search.form: 312, 313
ms.date: 03/24/2022
ms.author: bholtorf
ms.openlocfilehash: 4391b73a6e7f26262349abaeff751dd8f0f6c4e1
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2022
ms.locfileid: "8515668"
---
# <a name="set-up-posting-groups"></a>Setja upp bókunarflokka

Bókunarflokkar varpa einingum í fjárhagslykla. Dæmi um einingar eru viðskiptamenn, Lánardrottnar, vörur, tilföng og sölu-og innkaupaskjöl. Bókunarflokkar Sparaðu tíma og Hjálpaðu til við að forðast mistök þegar þú bókar viðskipti. Færslugildin fara á lyklana sem tilgreindir eru í bókunarhópnum fyrir þá tilgreindu einingu. Eina krafan er að þú hafir bókhaldslykla. Nánari upplýsingar er að finna í [Uppsetning bókhaldslykilsins](finance-setup-chart-accounts.md).  

Bókunarflokkar falla undir þrjú atriði:  

* Almennt

  Skilgreindu hver þú selur þér og Kauptu frá, og hvað þú selur og hvað þú kaupir. Þú getur líka sameinað hópa til að tilgreina hluti eins og rekstrarreikninga til að birta eða nota hópa til að sía skýrslur.  
* Sérstakt

  Notið söluskjöl, til dæmis, í stað þess að bóka beint í fjárhag. Þegar þú býrð til færslur í viðskiptamannabókinni, eru samsvarandi færslur gerðar í fjárhagnum.  
* Skattur

  Skilgreinið skattprósentur og reiknigerðir sem gilda um það hver þú selur og kaupir af þér og hvað þú selur og hvað þú kaupir.

Í eftirfarandi köflum er lýst bókunarflokkum undir hverju Umbrella.  

## <a name="general-posting-groups"></a>Almennir Bókunarflokkar

Eftirfarandi tafla lýsir almennum bókunarflokkum.

| Tegund | Description |
| --- | --- |
| Almennir viðskiptabókunarflokkar |Úthlutaðu þessum hópi á viðskiptavini og lánardrottna til að tilgreina hverjum þú selur og hverjum þú kaupir frá. Setjið upp þessa bókunarflokka á **síðunni Alm. viðskiptabókunarflokkar**. Þegar þú gerir það skaltu hugsa um hversu marga hópa þú þarft fyrir niðurbrog á sölu og kaupum. Til dæmis geturðu flokkað viðskiptavini og lánardrottna eftir svæði, eða eftir tegund viðskipta. |
| Almennir vörubókunarflokkar |Úthlutaðu þessum hópi á hluti og tilföng til að tilgreina hvað þú selur og hvað þú kaupir. Setjið upp þessa bókunarflokka á **síðunni Alm. vörubókunarflokkar**. Þegar þú gerir það skaltu hugsa um fjölda hópa sem þú þarft til að brjóta niður sölu eftir vöru (atriði og foprði) og kaup eftir vörum. Til dæmis, skaltu skipta þessum hópum eftir hráefnum, smásölu, tilföngum, getu og svo framvegis. |
| Uppsetning almenns bókunargrunns |Sameina viðskipti og vörubókunarflokka, og veldu lyklana til að bóka á. Fyrir hverja samsetningu viðskipta- og vöruskiptahópa er hægt að tengja saman fjölda aðalbókarreikninga. Til dæmis er hægt að bóka sölu á sömu vöru á mismunandi fjárhagslykla þar sem viðskiptavinum er úthlutað á ólíka viðskiptabókunarflokka. Stillið þessi afbrigði upp á **síðunni Almenn bókunaruppsetning**. |

## <a name="specific-posting-groups"></a>Ákveðnir Bókunarflokkar

Eftirfarandi tafla lýsir bókunarflokkana sem eru sérstaklega gerðir af gögnum.

|Tegund | Description |
| --- | --- |
| Bókunarflokkar viðskm. |Skilgreindu lyklana sem þú vilt nota þegar þú sendir inn færslur viðskiptakrafa. Ef birgðir eru notaðar með útistandandi reikningum sem eru bókaðir á sölupöntunarlínurnar sem eru ákvarðaðar af almennum viðskiptabókunarflokki sem er tengdur viðskiptamanni og almennum vörubókunarflokki sem birgðavara úthlutar vörunni. Sjá *almenna viðskiptabókunarflokka* og *almenna vörubókunarflokka* í [kaflanum Almennir Bókunarflokkar](#general-posting-groups). Setjið upp þessa bókunarflokka á **síðunni viðsk. bókunarflokkar**. |
| Bókunarflokkar lánardrottna |Tilgreindu hvar á að bóka færslur fyrir viðskiptaskuldir, þjónustureikninga og greiðsluafsláttarreikninga. Þetta er svipað og bókunarflokkur viðskiptamanns. Setjið upp þessa bókunarflokka á **síðunni lánardr. bókunarflokkar**. |
| Birgðabókunarflokkar |Skilgreindu birgðabókunarflokka sem þú úthlutar síðan á viðeigandi vörureikninga á síðunni **Uppsetning birgðabókunar**. Síðan þegar bókaðar eru færslur sem tengjast vöru þá bókar kerfið í fjárhagsreikninginn sem settur var upp fyrir þá samsetningu birgðabókunarflokks og birgðageymslu sem tengist vörunni. Birgðabókunarflokkar bjóða einnig upp á góða leið til að skipuleggja birgðir þínar, þannig að þú getur aðskilið hluti eftir bókunarflokkum þegar þú býrð til skýrslur. Setjið upp þessa bókunarflokka á **síðunni Birgðabókunarflokkar**. |
| Bókunarflokkar bankareikninga |Skilgreinið fjárhagsreikningana sem bankareikningsfærslurnar eru bókaðar á. Til dæmis getur þetta einfalt ferlið við að rekja færslr og samræma bankareikninga. Setjið upp þessa bókunarflokka á **síðu bankareiknings bókunarflokka**. Mælt er **með að þessir fjárhagsreikningar hafi reitinn bein bókun** stillt á *Nr*. |
| Bókunarflokkur eigna |Skilgreina reikninga fyrir mismunandi gerðir útgjalda og kostnað, svo sem kaupkostnað, uppsafnaðan afskriftir, kaupkostnað við ráðstöfun, uppsafnað afskriftir við förgun, hagnað af sölu, tapi á förgun, viðhaldskostnaði og afskriftargjöldum. Setjið upp þessa bókunarflokka á **síðunni Eignabókunarflokkar**. |

### <a name="allowing-substitute-customer-or-vendor-posting-groups-on-documents"></a>Staðgengdarflokkum viðskiptamanna-eða lánardrottna skipt í skjöl
Hægt er að láta fólk velja aðra bókunarflokka viðskiptavina en sjálfgildi þegar þeir eru að vinna með sölu-eða innkaupaskjöl og færslubækur.

Ef leyfa á breytingum á bókunarflokkum viðskiptamanna skal velja **Leyfa breytta bókunarflokka** á **uppsetningarsíðum sölu &** og **þjónustukerfisgrunni** og **uppsetningarsíðu innkaupa &** lánardrottna fyrir breytingar á bókunarflokki lánardrottins.

**Á bókunarflokkum viðskiptamanna** -eða **bókunarflokka** lánardrottna er hægt að tilgreina bókunarflokkana til að leyfa sem staðgengilsvörur með því að velja **skipti**. Staðgengilbókunarflokkar geta komið í stað sjálfgefinna bókunarflokka viðskiptamanna eða lánardrottna sem tilgreindir eru fyrir viðskiptavin eða lánardrottinn.

Eftir að þetta hefur verið sett upp er hægt að velja um leyfilega bókunarflokka og breyta viðskiptamanna-eða bókunarflokki lánardrottna við bókun sölu-eða innkaupaskjala og færslubóka. Staðgengilsbókin eða Lánardrottnabókunarflokkar eru afritaðir til bókaðra skjala og tímarita og greiðslujafnaðar eða skiptanlegar fjárhagsfærslur eru bókaðar í fjárhagsreikningana sem tilgreindir eru fyrir staðgengilsbókina.

Þegar sótt er um, til dæmis reikning og greiðslu sem er bókuð með mismunandi fjárhagsreikningum viðskiptamanna eða lánardrottna, skal [!INCLUDE[prod_short](includes/prod_short.md)] flytja upphæðirnar á milli fjárhagsreikningsins til að jafna þær.

## <a name="tax-posting-groups"></a>Skattbókunarflokkar

Eftirfarandi tafla lýsir skatttengdum bókunarflokkum.

| Tegund | Description |
| --- | --- |
| Skattaviðskiptabókunarflokkar |Ákveða hvernig á að reikna og bóka söluskatti fyrir viðskiptavini og lánardrottna. Setjið upp þessa bókunarflokka á **síðunni VSK viðskiptabókunarflokkar**. Þegar þú gerir það skaltu athuga hversu marga hópa þú þarft. Það gæti til dæmis farið eftir þáttum eins og staðbundinni löggjöf og hvort þú átt viðskipti bæði innanlands og alþjóðlega. |
| Skattavörubókunarflokkar |Tilgreindu skattaútreikninga sem þarf til að fá þær tegundir af forða sem þú kaupir eða selur. |
| Uppsetning skattbókunar |Sameina viðskiptabókunarflokk skatta og vörubókunarflokk skatta. Þegar þú fyllir inn almenna færslubókarlínu, innkaupalínu, eða sölulínu, munum við líta á samsetninguna til að bera kennsl á lyklana sem nota skal. |

Ef land þitt notar virðisauka (VSK), sjá [útreikning og bókunaraðferðir fyrir virðisaukandi skatt](finance-setup-vat.md).  

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

Fleiri vöru-og viðskiptabókunarflokkar sem þú hefur þá fleiri línur sem sjást á **síðunni almennar bókunaruppsetningar**. Það gæti tekið upp mikla gagnainnsetningu að setja upp almenna bókunaruppsetningu fyrir fyrirtækið. Þó að samsetningar viðskipta- og vörubókunarflokkanna séu margar er hægt að bóka þær saman í einn fjárhagsreikning. Til að draga úr handvirkum færslum skal afrita fjárhagsreikninga úr línu á síðunni **Alm. bókunargrunnur**.

## <a name="set-up-posting-groups-on-the-go"></a>Setja upp bókunarflokka á ferðinni

Til að fá notendur ræstir hraðar [!INCLUDE[prod_short](includes/prod_short.md)] geta sýnt tilkynningar um vantar fjárhagsreikninga í mismunandi bókunarflokka uppsetningar. Til að fá þessar tilkynningar þarf að ganga úr skugga um að **fjárhagsreikningurinn vanti í bókunarflokk eða tilkynningu um uppsetningu** og að tilkynning sé valin á **síðunni tilkynningar** sem hægt er að komast í frá **breytingunni þegar reiturinn tilkynningar** er færð inn **á síðuna mínar stillingar**.  

Þegar unnið er í skjali sem notar bókunarflokk eða-uppsetningu sem nauðsynlegur reikningur vantar kemur upp tilkynning. Veldu tengilinn í tilkynningunni til að opna síðu þar sem þú getur gert viðeigandi breytingar, gefið þér heimild til þess.  

> [!NOTE]
> Til að taka þig beint út í bókunarflokkinn eða uppsetninguna sem almennur Fjárhagslykill [!INCLUDE[prod_short](includes/prod_short.md)] vantar fyrir verður að stofna frátakaflokk eða-uppsetningu. Bókunarflokkar og uppsetningar eru leið fyrir endurskoðandann til að stýra því hvernig færslur eru bókaðar í fjárhag, þannig að eins er bara stofnun bókunarflokka og uppsetningar ekki leyfðar í fyrirtækinu þínu.  
>
> Ef svo er þarf að gera fjárhagsreikninginn óvirkan *í bókunarflokki eða* tilkynningu og vinna síðan hjá endurskoðanda til að gera viðkomandi breytingar á bókunarflokknum, uppsetningunni eða skjalinu. Þetta er mikilvægt skref, því þegar skjöl eru bókuð eru ekki hægt að eyða öllum bókunarflokkum sem eru ranglega notaðir vegna þess að fjárhagsfærslur hafa stofnast fyrir þær.

Sem byrjar í 2022 1. er hægt að nota **reitinn lokaður** á **síðunni Uppsetning** almennrar bókunar til að koma í veg fyrir að notendur hafi rangt með uppsetningu sem á ekki lengur við um nýjar bókanir.  

## <a name="troubleshooting-posting-group-errors"></a>Úrræðaleita villur bókunarflokks

Bókunarflokkar eru með ítarlegustu hlutunum til að setja upp í [!INCLUDE[prod_short](includes/prod_short.md)]. Ef þeir eru ekki settir upp á réttan hátt geta villur komið upp þegar skjöl eða færslubókarlínur eru bókaðar. Til dæmis stafa þessar villur yfirleitt af mistökum í því hvernig almennum fjárhagslyklum er úthlutað eða hvernig bókunarflokkar eru sameinaðir.

Þegar eitthvað er að mun [!INCLUDE[prod_short](includes/prod_short.md)] birtast á síðunni **Villuboð**. Síðan **Villuboð** getur auðveldað það að greina og leysa úr vandanum. Síðan býður upp á lýsingu á villunni sem bendir á uppsetningu bókunarflokksins sem þarfnast skoðunar. Til dæmis geta skilaboðin verið: „Í fyrirframgreiðslureikning sölu vantar bókunargrunn.“ Einnig er tengill til að opna síðuna þar sem rót vandans liggur þannig að hægt sé að leysa úr honum á fljótlegan hátt.  

> [!NOTE]
> Villumeðhöndlunin sem lýst er hér að ofan er ekki í boði fyrir vöru, tilfang, starfsmann og færslubók eigna eða fyrir fjárhagslykla sem bætt er við í staðbundnum útgáfum bókunarflokka.

## <a name="see-also"></a>Sjá einnig .
[Fjárhagur og bókhaldslyklar](finance-general-ledger.md)  
[Uppsetning Fjármála](finance-setup-finance.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
