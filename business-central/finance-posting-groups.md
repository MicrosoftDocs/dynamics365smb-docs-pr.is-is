---
title: Uppsetning bókunarflokks
description: Yfirlit yfir bókunarflokka sparar tíma og hjálpar við að koma í veg fyrir mistök þegar þú bókar færslur.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'posting setup, initialize'
ms.search.form: '312, 313'
ms.date: 08/26/2022
ms.author: bholtorf
---
# <a name="set-up-posting-groups"></a>Uppsetning bókunarflokka

Bókunarflokkar varpa einingum í fjárhagsreikninga. Dæmi um einingar eru viðskiptamenn, lánardrottnar, vörur, tilföng og sölu- og innkaupaskjöl. Bókunarflokkar spara tíma og hjálpar við að koma í veg fyrir mistök þegar þú bókar færslur. Færslugildin fara á lyklana sem tilgreindir eru í bókunarhópnum fyrir þá tilgreindu einingu. Eina krafan er að þú hafir bókhaldslykla. Nánari upplýsingar er að finna í [Uppsetning bókhaldslykilsins](finance-setup-chart-accounts.md).  

Bókunarflokkar falla undir þrjú atriði:  

* Almennt

  Tilgreindu hverjum þú selur og kaupir frá og hvað þú selur og hvað þú kaupir. Þú getur líka sameinað hópa til að tilgreina hluti eins og rekstrarreikninga til að birta eða nota hópa til að sía skýrslur.  
* Sérstakt

  Notaðu söluskjöl, til dæmis, í stað þess að senda beint í fjárhag. Þegar þú býrð til færslur í viðskiptamannabókinni, eru samsvarandi færslur gerðar í fjárhagnum.  
* Skattur

  Tilgreindu skattprósenturnar og útreikningsgerðir sem eiga við um hverjum þú selur og kaupir frá og hvað þú selur og hvað þú kaupir.

Eftirfarandi hlutar lýsa bókunarflokkunum undir hverju tilfelli.  

## <a name="general-posting-groups"></a>Almennir bókunarflokkar

Eftirfarandi tafla lýsir almennum bókunarflokkum.

| Gerð | Lýsing |
| --- | --- |
| Almennir viðskiptabókunarflokkar |Úthlutaðu þessum hópi á viðskiptavini og lánardrottna til að tilgreina hverjum þú selur og hverjum þú kaupir frá. Settu upp þessa bókunarflokka á síðunni **Alm. viðskiptabókunarflokkar**. Þegar þú gerir það skaltu hugsa um hversu marga hópa þú þarft fyrir niðurbrog á sölu og kaupum. Til dæmis geturðu flokkað viðskiptavini og lánardrottna eftir svæði, eða eftir tegund viðskipta. |
| Almennir vörubókunarflokkar |Úthlutaðu þessum hópi á hluti og tilföng til að tilgreina hvað þú selur og hvað þú kaupir. Settu upp þessa bókunarflokka á síðunni **Alm. vörubókunarflokkar**. Þegar þú gerir það skaltu hugsa um fjölda hópa sem þú þarft til að brjóta niður sölu eftir vöru (atriði og foprði) og kaup eftir vörum. Til dæmis, skaltu skipta þessum hópum eftir hráefnum, smásölu, tilföngum, getu og svo framvegis. |
| Uppsetning almenns bókunargrunns |Sameina viðskipti og vörubókunarflokka, og veldu lyklana til að bóka á. Fyrir hverja samsetningu viðskipta- og vöruskiptahópa er hægt að tengja saman fjölda aðalbókarreikninga. Til dæmis er hægt að bóka sölu á sömu vöru á mismunandi fjárhagsreikninga vegna þess að viðskiptamönnum er úthlutað á mismunandi viðskiptabókunarflokka. Settu þessar grunnstillingar upp á síðunni **Almennur bókunargrunnur**þ |

## <a name="specific-posting-groups"></a>Sértækir bókunarflokkar

Eftirfarandi tafla lýsir bókunarflokkum sem eru sértækir fyrir ákveðnar tegundir gagna.

|Gerð | Lýsing |
| --- | --- |
| Bókunarflokkur viðskm. |Skilgreindu lyklana sem þú vilt nota þegar þú sendir inn færslur viðskiptakrafa. Ef þú notar birgðir með kröfum eru það almenni viðskiptabókunarflokkurinn sem er úthlutaður viðskiptavininum þínum og almenni vörubókunarflokkurinn sem er úthlutaður birgðavöru. Sjá *Almennir viðskiptabókunarflokkar* og *Almennir vörubókunarflokkar* í hlutanum [Almennir bókunarflokkar](#general-posting-groups). Settu upp þessa bókunarflokka á síðunni **Bókunarflokkar viðskmanns**. |
| Bókunarflokkur lánardr. |Tilgreindu hvar á að bóka færslur fyrir viðskiptaskuldir, þjónustureikninga og greiðsluafsláttarreikninga. Þetta er svipað og bókunarflokkur viðskiptamanns. Settu upp þessa bókunarflokka á síðunni **Bókunarflokkar lánardrottins**. |
| Birgðabókunarflokkur |Skilgreindu birgðabókunarflokka sem þú úthlutar síðan á viðeigandi vörureikninga á síðunni **Uppsetning birgðabókunar**. Síðan þegar bókaðar eru færslur sem tengjast vöru þá bókar kerfið í fjárhagsreikninginn sem settur var upp fyrir þá samsetningu birgðabókunarflokks og birgðageymslu sem tengist vörunni. Birgðabókunarflokkar bjóða einnig upp á góða leið til að skipuleggja birgðir þínar, þannig að þú getur aðskilið hluti eftir bókunarflokkum þegar þú býrð til skýrslur. Settu upp þessa bókunarflokka á síðunni **Birgðabókunarflokkar**. |
| Bókunarflokkar bankareikninga |Skilgreindu fjárhagsreikningana sem bankareikningsfærslur eru bókaðar í. Til dæmis getur þetta einfalt ferlið við að rekja færslr og samræma bankareikninga. Settu upp þessa bókunarflokka á síðunni **Bókunarflokkar bankareikninga**. Mælt er með að þessir fjárhagsreikningar séu með reitinn **Bein bókun** stilltan á *Nei*. |
| Bókunarflokkur eigna |Skilgreina reikninga fyrir mismunandi gerðir útgjalda og kostnað, svo sem kaupkostnað, uppsafnaðan afskriftir, kaupkostnað við ráðstöfun, uppsafnað afskriftir við förgun, hagnað af sölu, tapi á förgun, viðhaldskostnaði og afskriftargjöldum. Settu upp þessa bókunarflokka á síðunni **Eignarbókunarflokkur**. |

### <a name="allowing-substitute-customer-or-vendor-posting-groups-on-documents"></a>Að leyfa staðgengil fyrir bókunarflokka viðskiptamanns eða lánardrottins í skjöl

[!INCLUDE [preview](includes/preview.md)]

Þú getur leyft fólki að velja annan bókunarflokk viðskiptamanns og lánardrottins en þann sjálfgefna þegar það vinnur með sölu- eða innkaupaskjöl og færslubækur.

Til að leyfa breytingar á bókunarflokkum skaltu velja **Leyfa marga bókunarflokka** á síðunum **Uppsetning sölugrunns** og **Uppsetning þjónustustjórnunar** og síðunni **Uppsetning innkaupagrunns** fyrir breytingar á bókunarflokki lánardrottins.

Á síðunum **Bókunarflokkar viðskiptamanns** eða **Bókunarflokkar lánardrottins** er hægt að tilgreina bókunarflokkana sem á að leyfa sem staðgengla með því að velja **Staðgenglar**. Bókunarflokkar staðgengils geta komið í stað sjálfgefinna bókunarflokka viðskiptamanns eða lánardrottins sem tilgreindir eru fyrir viðskiptamann eða lánardrottin.

Þegar þetta hefur verið sett upp er hægt að velja úr leyfðum bókunarflokkum staðgengils og breyta bókunarflokki viðskiptamanns eða lánardrottins þegar sölu- eða innkaupaskjöl og færslubækur eru bókaðar. Bókunarflokkar fyrir staðgengil viðskiptamanns eða lánardrottins eru afritaðir á bókuð skjöl og færslubækur og fjárhagsfærslur viðskiptakrafna og viðskiptaskulda eru bókaðar á fjárhagsreikninga fyrir staðgenglana.

Þegar notaður er til dæmis reikningur eða greiðsla sem er bókuð með mismunandi bókunarflokkum viðskiptamanns eða lánardrottins (mismunandi fjárhagsreikningar) millifærir [!INCLUDE[prod_short](includes/prod_short.md)] upphæðirnar á milli fjárhagsreikninga til að jafna þá.

## <a name="tax-posting-groups"></a>Skattbókunarflokkar

Eftirfarandi tafla lýsir skatttengdum bókunarflokkum.

| Gerð | Lýsing |
| --- | --- |
| Skattaviðskiptabókunarflokkar |Ákveða hvernig á að reikna og bóka söluskatti fyrir viðskiptavini og lánardrottna. Settu upp þessa bókunarflokka á síðunni **Skattaviðskiptabókunarflokkar**. Þegar þú gerir það skaltu athuga hversu marga hópa þú þarft. Til dæmis getur þetta oltið á þáttum eins og staðbundinni löggjöf og hvort þú stundar viðskipti innanlands og á alþjóðavettvangi. |
| Skattavörubókunarflokkar |Tilgreindu skattaútreikninga sem þarf til að fá þær tegundir af forða sem þú kaupir eða selur. |
| Uppsetning skattbókunar |Sameina viðskiptabókunarflokk skatta og vörubókunarflokk skatta. Þegar þú fyllir inn almenna færslubókarlínu, innkaupalínu, eða sölulínu, munum við líta á samsetninguna til að bera kennsl á lyklana sem nota skal. |

Ef land/svæði þitt notar virðisauka (VSK), sjá  [Setja upp útreikninga og bókunaraðferðir fyrir virðisaukandi skatta](finance-setup-vat.md).  

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

Því fleiri vörur og viðskiptabókunarflokk sem þú ert með því fleiri línur sérðu á síðunni **almennur bókunargrunnur**. Það gæti þurft að að færa inn mikið af gögnum til að setja upp almennan bókunargrunn fyrir fyrirtækið. Þó að samsetningar viðskipta- og vörubókunarflokkanna séu margar er hægt að bóka þær saman í einn fjárhagsreikning. Til að draga úr handvirkum færslum skal afrita fjárhagsreikninga úr línu á síðunni **Alm. bókunargrunnur**.

## <a name="set-up-posting-groups-on-the-go"></a>Setja upp bókunarflokka á ferðinni

Til að koma notendum af stað sem fyrst getur [!INCLUDE[prod_short](includes/prod_short.md)] sýnt tilkynningar um fjárhagsreikninga sem vantar í ýmsum uppsetningum bókunarflokka. Til að fá þessar tilkynningar skaltu ganga úr skugga um að tilkynningin **Fjárhagsreikning vantar í bókunarflokki eða uppsetningu** sé valin á síðunni **Mínar tilkynningar**, sem þú getur opnað úr reitnum **Breyta þegar ég fæ tilkynningar** á síðunni **Mínar stillingar**.  

Þannig færðu tilkynningu þegar þú vinnur í skjali sem notar bókunarflokk eða uppsetningu þar sem vantar nauðsynlegan fjárhagsreikning. Veldu tengilinn í tilkynningunni til að opna síðu þar sem þú getur viðeigandi breytingar svo lengi sem þú hafir heimild til að gera slíkt.  

> [!NOTE]
> Til að geta farið með þig beint í bókunarflokkinn eða uppsetninguna þar sem vantar fjárhagsreikning mun [!INCLUDE[prod_short](includes/prod_short.md)] búa til staðgengil fyrir bókunarflokk eða uppsetningu. Bókunarflokkar og uppsetningar eru leið fyrir endurskoðanda að stjórna því hvernig færslur eru bókaðar í fjárhaginn þannig að tímanlegar stofnanir á bókunarflokkum og uppsetningum eru hugsanlega ekki leyfðar í fyrirtækinu.  
>
> Ef svo er skaltu slökkva á tilkynningunni *Fjárhagsreikning vantar í bókunarflokk eða uppsetningu* og síðan vinna með endurskoðandanum til að gera viðeigandi breytingar á bókunarflokknum, uppsetningunni eða skjalinu. Þetta er mikilvægt skref vegna þess að þegar skjöl eru bókuð verður ekki hægt að eyða neinum rangt notuðum bókunarflokkum eða uppsetningum því að búið er að stofna fjárhagsfærslur fyrir það.

Frá og með útgáfubylgju 1 árið 2022 getur þú notað reitinn **Útilokað** á síðunni **Almennur bókunargrunnur** til að koma í veg fyrir að notendur noti uppsetningu sem á ekki lengur við fyrir nýjar bókanir.  

## <a name="troubleshooting-posting-group-errors"></a>Úrræðaleita villur bókunarflokks

Bókunarflokkar eru með ítarlegustu hlutunum til að setja upp í [!INCLUDE[prod_short](includes/prod_short.md)]. Ef þeir eru ekki settir upp á réttan hátt geta villur komið upp þegar skjöl eða færslubókarlínur eru bókaðar. Til dæmis stafa þessar villur yfirleitt af mistökum í því hvernig almennum fjárhagslyklum er úthlutað eða hvernig bókunarflokkar eru sameinaðir.

Þegar eitthvað er að mun [!INCLUDE[prod_short](includes/prod_short.md)] birtast á síðunni **Villuboð**. Síðan **Villuboð** getur auðveldað það að greina og leysa úr vandanum. Síðan býður upp á lýsingu á villunni sem bendir á uppsetningu bókunarflokksins sem þarfnast skoðunar. Til dæmis geta skilaboðin verið: „Í fyrirframgreiðslureikning sölu vantar bókunargrunn.“ Einnig er tengill til að opna síðuna þar sem rót vandans liggur þannig að hægt sé að leysa úr honum á fljótlegan hátt.  

> [!NOTE]
> Villumeðhöndlunin sem lýst er hér að ofan er ekki í boði fyrir vöru, tilfang, starfsmann og færslubók eigna eða fyrir fjárhagslykla sem bætt er við í staðbundnum útgáfum bókunarflokka.

## <a name="see-related-microsoft-training"></a>Sjá tengda [Microsoft þjálfun](/training/modules/posting-groups-dynamics-365-business-central/)

## <a name="see-also"></a>Sjá einnig .

[Fjárhagur og bókhaldslyklar](finance-general-ledger.md)  
[Uppsetning Fjármála](finance-setup-finance.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
