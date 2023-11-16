---
title: 'Röðun, leit og síun í listum'
description: 'Vinna á skilvirkan hátt í listum með því að leita yfir gögnin þín, flokka dálka og hreinsa niðurstöður með síutáknum og flýtivísum.'
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'delimit, FlowFilter, totals, limit, advanced'
ms.search.form: null
ms.date: 10/30/2023
ms.author: jswymer
---
# Röðun, leit og síun

Það eru nokkrir hlutir sem munu hjálpa þér að skanna, finna og takmarka skrár í lista, skýrslu eða XMLport. Þar á meðal er röðun, leit og afmörkun. Þú getur notað suma eða alla þessa hluti samtímis til að finna eða greina gögnin þín fljótt.

[!INCLUDE [about-ui-learn](includes/about-ui-learn.md)]

Fyrir skýrslur og XMLport, líkt og í listum, er hægt að stilla síur til að afmarka hvaða gögn eigi að taka með í skýrslunni eða XMLport, en ekki er hægt að raða og leita.

> [!TIP]
> Þegar þú skoðar gögnin þín sem flísar getur þú leitað og notað síun. Til að nota alla þessa öflugu eiginleika til að raða, leita og sía skaltu velja táknið ![Sýna sem lista.](media/ui_show_as_list_icon.png "Sýna sem listaör til vinstri") táknið til að skoða skrárnar sem lista.

<!--
When you want to search for data, such as customer names, addresses, or product groups, you enter criteria. In search criteria, you can use all the numbers and letters that you normally use in the specific field. In addition, you can use special symbols to further filter the results. There are two ways to search: using the Quick Filter or column filters.
-->

## Röðun

Með Röðun er auðvelt og fljótlegt að fá yfirsýn yfir gögnin. Ef þú ert til dæmis með marga viðskiptamenn, gætirðu raðað þeim eftir **Viðskiptamannanr.**, **Gjaldmiðilskóða** eða **Svæðiskóða lands** til að fá yfirlitið sem þú þarft.

Til að raða lista geturðu annaðhvort:

- Valið fyrirsagnartexta dálks til að skipta milli hækkandi og lækkandi röð eða
- Valið örina sem vísar niður í dálkhaus, valið síðan aðgerðina **Hækkandi** eða **Lækkandi**.  

> [!NOTE]  
> Myndir, BLOB-reitir, FlowFilters og reitir sem tilheyra ekki töflu styðja ekki röðun.  

## Leit

<!--## Searching by using the Quick Filter -->
Efst á öllum listasíðum er ![Leita í lista.](media/ui-search/search-list.png "Tákn fyrir leitarlista") Aðgerðin **Leita** sem býður upp á fljótlega og auðvelda leið til að draga úr magni gagna í lista og sýna einungis þær skrár sem innihalda gögnin sem þú vilt sjá.

Til að leita skaltu einfaldlega velja aðgerðina **Leita** og síðan skrifa í boxið textann sem er verið að leita að. Þú getur slegið inn stafi, númer og önnur tákn.

Almennt mun leit reyna að finna samsvarandi texta í öllum reitum. Leitin mun ekki gera greinarmun á hástöfum og lágstöfum (óháð há- og lágstöfum) og mun finna textasamsvörun hvar sem er í reitnum (fremst, aftast eða í miðjunni).

> [!TIP]
> Hægt er að velja  <kbd>F3</kbd>  til að virkja og afvirkja leitargluggann. Frekari upplýsingar, sjá [Flýtilyklar](keyboard-shortcuts.md#KeyboardFilter).

> [!NOTE]  
> Leit mun ekki passa við gildi í myndum, BLOB-reitum, Flow-síum, FlowFields-reitum og öðrum reitum sem eru ekki hluti af töflu.


### Fínstilla leitina með síuskilyrði

Hægt er að gera nákvæmari leit með því að nota virknitákn síu, segðir og síumerki. Ólíkt síun er þetta notað yfir alla reiti þegar það er notað í leitarglugganum, sem gerir þá ekki eins skilvirka og síun.

- Til að finna aðeins reitargildi sem samsvara öllum textanum og stöfunum, skal staðsetja textann á milli einfaldra gæsalappa `''` (til dæmis, `'man'`).

- Til að finna reitargildi sem byrja á ákveðnum texta og samsvara stöfunum, skal setja `*` á eftir leitartextanum (til dæmis `man*`).

- Til að finna reitargildi sem enda á ákveðnum texta og samsvara stöfunum, skal setja `*` á undan leitartextanum (til dæmis `*man`).

- Þegar `''` eða `*` er notað er leitin stafrétt. Ef þú vilt gera leitina óháða há- og lágstöfum skaltu setja `@` á undan leitartextanum (til dæmis `@man*`).

Eftirfarandi tafla sýnir nokkur dæmi til að útskýra hvernig hægt er að nota leitina.

|Leitarskilyrði|Finnur ...|
|---------------|----------|
|`man`<br />eða <br />`Man`|Allar skrár með reitum sem innihalda textann **man**, óháð því hvort notaðir eru há- eða lágstafir. Til dæmis, **Manchester**, **manual**, eða **Sportsman**. |
|`'Man'`|Allar skrár með reitum sem innihalda aðeins **Man**, í samræmi við há- og lágstafi.|
|`Man*`|Allar skrár með reitum sem byrja á textanum <b>Man</b>, í samræmi við há- og lágstafi. Til dæmis, **Manchester** en ekki **manual** eða **Sportsman** .|
|`@Man*`|Allar skrár með reitum sem byrja með **man**, óháð því hvort notaðir eru há- eða lágstafir. Til dæmis, **Manchester** og **manual**, en ekki **Sportsman**.|
|`@*man`|Allar skrár sem endar með **man**, óháð því hvort notaðir eru há- eða lágstafir. Til dæmis **Sportsman**, en ekki **Manchester** eða **manual**.|


## <a name="filtering"></a>Afmörkun

Síun veitir háþróaðri og fjölhæfari leið til að stjórna því hvaða færslur birtast á lista, skýrslu eða XMLport. Það eru tvær helstu munur á leit og síun, eins og lýst er í töflunni hér að neðan.

|| **Leit** | **Afmörkun** |
|--|----------|------------|
| **Reitir sem gilda** | Leitar yfir alla reitum sem eru sýnilegar á síðunni. | Síar einn eða fleiri reiti, hvern fyrir sig, og velur úr öllum reitum í töflunni, þar á meðal reiti sem eru ekki sýnilegir á síðunni. |
| **Samsvörun** | Sýnir skrár með reitum sem samsvara leitartextanum, óháð há- og lágstöfum eða staðsetningu textans í reitnum. | Sýnir skrár þar sem reiturinn samsvarar nákvæmlega síunni, þ.m.t. há- og lágstöfum textans, nema ef sérstök síutákn eru færð inn.

Síun gerir þér kleift að birta skrár fyrir tiltekna reikninga eða viðskiptamenn, dagsetningar, upphæð og aðrar upplýsingar með því að tilgreina síuviðmiðanir. Aðeins færslur sem samsvara skilyrðunum eru birtar á listanum eða teknar með í skýrslugerð, runuvinnslu eða XMLport. Ef þú tilgreinir skilyrði fyrir marga reiti, þá birtast aðeins skrár sem passa við öll skilyrði.

Fyrir lista eru síurnar sýndar á afmörkunarsvæði sem birtist til vinstri á listanum þegar það er virkjað. Fyrir skýrslur, runuvinnslur og XMLport eru síurnar sýnilegar beint á beiðnisíðunni.

### Sía með valsvæðum

Fyrir „venjulega“ reiti sem innihalda gögn, uppsetningardagsetningu eða viðskiptagögn er hægt að stilla síur bæði með því að velja gögn og með því að slá inn síugildi og hægt er að nota tákn til að skilgreina ítarleg síuskilyrði. Nánari upplýsingar eru í [Færa inn síuskilyrði](ui-enter-criteria-filters.md#entering-filter-criteria).

Fyrir reiti af gerðinni **Valkostir** er hins vegar aðeins hægt að stilla síu með því að velja einn eða fleiri valkosti úr fellilista með tiltækum valkostum. Dæmi um valkostsreit er reiturinn **Staða** á síðunni **Sölupantanir**.

> [!NOTE]
> Þegar margir valkostir eru valdir sem síugildi er venslin á milli valkostanna skilgreind sem *EÐA*. Til dæmis, ef þú velur báða gátreitina **Opið** og **Losað** á afmörkunarsvæðinu **Staða** á síðunni **Sölupantanir**, þýðir það að sölupantanir sem eru annaðhvort opnar eða losaðar eru birtar.

### Afmarkanir stilltar á lista

Á listum eru síur stilltar með því að nota afmörkunarsvæði. Til að birta afmörkunarsvæðið fyrir lista skal velja felliörina við hliðina á heiti síðunnar og velja síðan **Sýna afmörkunarsvæði**. Einnig er hægt að velja  <kbd>Shift</kbd>+<kbd>F3</kbd>.

Til að birta afmörkunarsvæðið fyrir dálk á lista skal velja felliörina og velja síðan aðgerðina **Afmörkun**. Einnig er hægt að velja  <kbd>Shift</kbd>+<kbd>F3</kbd>. Afmörkunarsvæðið opnast með völdum dálki sem sýndur er sem afmörkunarsvæðið í hlutanum **Afmarka lista**.

Síusvæðið sýnir núverandi síur fyrir lista og gerir þér kleift að stilla eigin sérsniðna síur í einu eða fleiri reitum með því að velja aðgerðina **+ Sía**.

 Síusvæði er skipt í þrjá hluta: **Skoðanir**, **Sía listi eftir** og **Sía samtölur eftir**:

- **Yfirlit**

  Sumir listar hafa hlutann **Yfirlit** með. Skoðanir eru afbrigði af listanum sem hefur verið forstillt með síum. Þú getur skilgreint og vistað eins mörg yfirlit og þú vilt fyrir hvern lista. Yfirlitin verða aðgengilegt í öllum tækjum sem þú skráir þig inn á. Frekari upplýsingar er að finna á [Vista og sérsníða listayfirlit](ui-views.md).

- **Sía listi eftir**

  Þetta er hlutinn er þar sem þú bætir við síum á tilteknum reitum til að draga úr fjölda birtra skráa. Til að bæta við síu skal velja aðgerðina **+ Sía**. Til að bæta við síu skal slá inn heiti reitsins sem á að sía listann eftir eða velja reit af fellilistanum.

- **Sía samtölur eftir**

  Sumar listar sem sýna reiknaðir reitir, svo sem upphæðir og fjölda, munu innihalda **Sía samtölur eftir** hlutann þar sem þú getur breytt ýmsum víddum sem hafa áhrif á útreikninga. Til að bæta við síu skal velja aðgerðina **+ Sía**. Til að bæta við síu skal slá inn heiti reitsins sem á að sía listann eftir eða velja reit af fellilistanum.

  > [!NOTE]
  > Síur í **Sía samtölur eftir** hlutanum eru stjórnað af FlowFilters í síðuhönnuninni. Fyrir tæknilegar upplýsingar, sjá [FlowFilters](/dynamics365/business-central/dev-itpro/developer/devenv-flowfilter-overview).

Hægt er að stilla einfalda síu beint á lista innan með síusvæðinu, þ.e. síu sem sýnir aðeins færslur með sama gildi og í völdum reitum. Velja skal hólf á listanum, velja felliörina og velja síðan aðgerðina **Afmarka í þetta gildi**. Einnig er hægt að velja  <kbd>Alt</kbd>+<kbd>F3</kbd>.

### Afmarkanir stilltar í skýrslum, runuvinnslum og XMLports

Fyrir skýrslur og XMLports eru síurnar sýnilegar beint á beiðnisíðunni. Beiðnisíðan sýnir síðustu notuðu síur samkvæmt valinu í reitnum **Nota sjálfgildi úr**. Frekari upplýsingar eru í [Nota vistaðar stillingar](ui-work-report.md#SavedSettings).

Helsti **Sía**-hlutinn sýnir sjálfgefna síureiti sem notaðir eru til að afmarka hvaða færslur á að taka með í skýrslu eða XMLport. Til að bæta við síu skal velja aðgerðina **+ Sía**. Svo skal færa inn heiti reitsins sem á að sía eftir eða velja reit af fellilistanum.

Í hlutanum **Afmarka samtölur eftir** er hægt að breyta ýmsum víddunum sem hafa áhrif á útreikninga í skýrslu eða XMLport. Til að bæta við síu skal velja aðgerðina **+ Sía**. Svo skal færa inn heiti reitsins sem á að sía eftir eða velja reit af fellilistanum.

## Færa inn síuskilyrði

Bæði í síuglugganum og á beiðnisíðu er hægt að færa inn síuskilyrðin í reitinn undir síureitnum.

Gerð síureits ákvarðar hvaða skilyrði er hægt að færa inn. Til dæmis, að sía reit sem hefur fasta gildi mun einungis leyfa þér að velja úr þeim gildum. Nánari upplýsingar um sérstaka síu tákn sjá [Sía viðmiðanir](#FilterCriteria) og [Síumerki](#FilterTokens).

Dálkar sem þegar eru með síur eru auðkenndir með ![Síutákninu.](media/ui-search/filter-icon.png "Síutákn") í dálkahausnum. Til að fjarlægja afmörkun skal velja felliörina og velja svo aðgerðina **Hreinsa afmörkun** .

> [!TIP]
> Finna og greina gögnin þín fljótar með því að nota samsetningar flýtilykla. Til dæmis skal velja svæði, nota Shift Alt F3 til að bæta því svæði í afmörkunarrúðuna, færa inn afmörkunarskilyrðin, nota  <kbd>CTRL</kbd>+<kbd>-Enter</kbd>+<kbd>til að fara aftur í línurnar, velja annað svæði og nota</kbd>  Alt  <kbd>F3</kbd>+<kbd>til að sía það gildi.</kbd>  <kbd></kbd>+<kbd></kbd>  Frekari upplýsingar, sjá [Flýtilyklar](keyboard-shortcuts.md#KeyboardFilter).

### <a name="FilterCriteria"> </a>Síuskilyrði og virkni

Þegar skilyrði eru sett er hægt að nota alla sömu tölustafi og bókstafi sem venjulega eru notaðir í reitnum. En það eru líka til safn sértákna sem hægt er að nota sem virknitákn til að sía niðurstöður enn frekar. Eftirfarandi hlutar útskýra þessi tákn og hvernig á að nota þau sem virknitákn í síum.

> [!TIP]
> Frekari upplýsingar um síun dagsetninga og tímasetninga er að finna í [Vinna með dagsetningar og tíma í dagatali](ui-enter-date-ranges.md).

> [!IMPORTANT]
> - Aðstæður kunna að koma upp þar sem gildið sem á að sía inniheldur tákn sem er virknitákn. Frekari upplýsingar um hvað skuli gera í slíkum aðstæðum er að finna í [Gildi síuð sem innihalda tákn](#symbols) til að fá frekari leiðbeiningar um hvað skuli til bragðs taka í þessum aðstæðum.
>
> - Ef fleiri en 200 virknitákn eru til staðar í einni síu safnar kerfið sjálfkrafa saman sumum virknitáknum innan sviga `()` fyrir úrvinnsluna. Þetta hefur engin áhrif á síunina eða niðurstöðurnar.  

#### (..) Bil

|Dæmi|Sýndar færslur|  
|-----------------------|-----------------------|  
|`1100..2100`|Tölur 1100 til 2100.|  
|`..2500`|Reikningar til og með 2500|  
|`..12 31 00`|Dagsetningar til og með 31. 12. 00.|  
|`P8..`|Upplýsingar um reikningstímabil 8 og eftir|  
|`..23`|Frá upphafsdegi til 23. þessa mánaðar – þessa árs 23:59:59|  
|`23..`|Frá 23. þessa mánaðar – þessa árs 00:00:00 til loka tímans|  
|`22..23`|Frá 22. þessa mánaðar – þessa árs 00:00:00 til 23. þessa mánaðar – þessa árs 23:59:59| 

> [!TIP]
> Ef talnaborð er notað getur skiltákn tugabrots komið með staf annan en punkt (.). Ef skipta á um tímabil skal velja  <kbd>Skilríkjalykla</kbd>+<kbd>Alt</kbd>  tugabrotatakkanum á talnaborðinu. Ef þú vilt skipta aftur skaltu velja  <kbd>skilyrt</kbd>+<kbd>aukastaf Alt</kbd> . Frekari upplýsingar eru í [Að stilla skiltákn tugabrots sem á að nota með talnalyklaborðum](ui-enter-data.md#decimal).

#### (&#124;) Annaðhvort eða

|Dæmi|Sýndar færslur|  
|-----------------------|-----------------------|  
|`1200|1300`|Tölur með 1200 eða 1300|  

#### (<>) Ekki jafnt og  

|Dæmi|Sýndar færslur|  
|-----------------------|-----------------------|  
|`<>0`|Allar tölur aðrar en 0<br /><br /> Valkosturinn SQL Server býður upp á að sameina þetta tákn algildistákni. Til dæmis merkir <>A* ekki jafnt og neinn texti sem byrjar á stafnum A.|  

#### (>) Meira en  

|Dæmi|Sýndar færslur|  
|-----------------------|-----------------------|  
|`>1200`|Tölur hærri en 1200|  

#### (>=) Hærra en eða jafnt og  

|Dæmi|Sýndar færslur|  
|-----------------------|-----------------------|  
|`>=1200`|Tölur hærri en eða jafnar 1200|  

#### (<) Minna en  

|Dæmi|Sýndar færslur|  
|-----------------------|-----------------------|  
|`<1200`|Tölur lægri en 1200|  

#### (<=) Lægra en eða jafnt og  

|Dæmi|Sýndar færslur|  
|-----------------------|-----------------------|  
|`<=1200`|Tölur lægri en eða jafnar 1200|  

#### (&) Og  

|Dæmi|Sýndar færslur|  
|-----------------------|-----------------------|  
|`>200&<1200`|Tölur hærri en 200 og minni en 1200|  

#### ('') Nákvæm stafasamsvörun  

|Dæmi|Sýndar færslur|  
|-----------------------|-----------------------|  
|`'man'`|Texta sem passar nákvæmlega við **man** og er stafréttur.|  
|`''`|Auður textareitur.|  

#### (@) Stafrétt  

|Dæmi|Sýndar færslur|  
|-----------------------|-----------------------|  
|`@man*`|Texti sem byrjar á **man** og er ekki stafréttur.|  

#### (*) Ótilgreindur fjöldi óþekktra staftákna

|Dæmi|Sýndar færslur|  
|-----------------------|-----------------------|  
|`*Co*`|Texta sem inniheldur **Co** og er stafréttur.|  
|`*Co`|Texta sem endar á **Co** og er stafréttur.|  
|`Co*`|Texta sem byrjar á **Co** og er stafréttur.|  

#### (?) eitt óþekkt stafatákn  

|Dæmi|Sýndar færslur|  
|-----------------------|-----------------------|  
|`Hans?n`|Texti eins og **Hansen** eða **Hanson**|  

#### Sameinað framsetningarsnið  

|Dæmi|Sýndar færslur|  
|-----------------------|-----------------------|  
|`5999|8100..8490`|Allar færslur með tölunni 5999 eða tölu á bilinu frá 8100 til og með 8490 er teknar með.|  
|`..1299|1400..`|Telja með færslur með tölu sem er lægri eða jöfn 1299 eða tölu sem er jöfn 1400 eða hærri (allar tölur nema 1300 til 1399).|  
|`>50&<100`|Telja með færslur með tölum sem eru hærri en 50 og lægri en 100 (tölurnar 51 til 99).|  

### <a name="symbols"></a>Gildi síuð sem innihalda tákn

Það gætu komið upp tilfelli þar sem reitargildi innihalda eitt af eftirfarandi táknum:

- &
- (
- )
- =
- &#124;

Ef sía á eitthvert þessara tákna skal setja það sem leita á að í einfaldar gæsalappir (`'<expression with symbol>'`). Ef þú vilt til dæmis sía skrár sem hefjast á textanum *J & V*, þá yrði síusegðin `'J & V*'`.

Þetta skilyrði er ekki nauðsynlegt fyrir önnur tákn.

### <a name="FilterTokens"> </a>Síumerki

Þegar þú slærð inn síuviðmiðanir getur þú einnig skrifað orð sem hafa sérstaka þýðingu, sem kallast síumerki. Eftir að hafa slegið inn merkiorðið, er orðinu skipt út fyrir gildin sem það táknar. Síutákn gera síun auðveldari með því að draga úr þörfinni á að fara yfir á aðrar síðum til að fletta upp gildi sem þú vilt bæta við síuna. Taflan hér fyrir neðan lýsir sumum merkjunum sem þú getur slegið inn sem síuviðmiðanir.

> [!TIP]
> Stofnunin þín getur notað sérsniðna merki. Til að læra um öll merkin sem þú hefur aðgang að eða til að bæta við fleiri sérsniðnum merkjum, skaltu tala við stjórnandann þinn. Fyrir tæknilegar upplýsingar, sjá [Bæta við síumerkjum](/dynamics365/business-central/dev-itpro/developer/devenv-adding-filter-tokens).

#### (%me eða %userid) Skrám úthlutað til þín

Notaðu `%me` eða `%userid` þegar verið er að sía reiti sem innihalda notandakenni, svo sem **úthlutað til notandakennis** reit, til að birta allar skrár sem eru úthlutað til þín.

|Dæmi|Sýndar færslur|  
|-----------------------|-----------------------|  
|`%me`<br />eða<br />`%userid`|Skrár sem eru úthlutað á notandareikninginn þinn. |  

#### (%mycustomers) Viðskiptamenn í Mínir viðskiptamenn

Notaðu `%mycustomers` í **Nr** reitnum viðskiptamanns til að birta allar skrár fyrir viðskiptamenn sem eru innifaldir í **Mínir viðskiptamenn** listanum á Mitt hlutverk.

|Dæmi|Sýndar færslur|  
|-----------------------|-----------------------|  
|`%mycustomers`|Viðskiptamenn í **Mínir viðskiptamenn** í Mitt hlutverk. |  

#### (%mytems) Atriði í Mínum atriðum

Notaðu `%myitems` Í atriði **Nr** reitinn til að birta allar skrár fyrir atriði sem eru innifalin í **Mín atriði** listanum í Mitt hlutverk.

|Dæmi|Sýndar færslur|  
|-----------------------|-----------------------|  
|`%myitems`|Atriði í **Mín atriði** í Mitt hlutverk. |  

#### (%myvendors) Lánardrottnar í Mínir lánardrottnar

Notaðu `%myvendors` í lánardrottinn **Nr** reitnum, til að birta allar skrá fyrir lánardrottna sem eru innifalin í **Mínir lánardrottnar** listanum í Mitt hlutverk.

|Dæmi|Sýndar færslur|  
|-----------------------|-----------------------|  
|`%myvendors`|Lánardrottnar í **Mínir lánardrottnar** í Mitt hlutverk. |  

## Sjá einnig .

[Algengar spurningar um leit og síun](ui-search-filter-faq.yml)  
[Vista og sérsníða listayfirlit](ui-views.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
