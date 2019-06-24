---
title: Röðun, leit og síun í listum | Microsoft Docs
description: Vinna á skilvirkan hátt í listum með því að leita yfir gögnin þín, flokka dálka og hreinsa niðurstöður með öflugum síutáknum og flýtivísum.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: delimit, FlowFilter, totals, limit, advanced
ms.date: 06/03/2019
ms.author: sgroespe
ms.openlocfilehash: fc9cefd33f6ca11ee4f2936671a84071e142a1bd
ms.sourcegitcommit: 04581558f6c5488c705a7ac392cf297be10b5f4f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/06/2019
ms.locfileid: "1621184"
---
# <a name="sorting-searching-and-filtering-lists"></a>Röðun, leit og síun í listum
Það eru nokkrir hlutir sem munu hjálpa þér að skanna, finna og takmarka skrár í lista. Þar á meðal er röðun, leit og afmörkun. Þú getur notað suma eða alla þessa hluti samtímis til að finna eða greina gögnin þín fljótt.

> [!TIP]
> Þegar þú skoðar gögnin þín sem flísar getur þú leitað og notað grunn síun. Til að nota alla þessa öflugu eiginleika til að raða, leita og sía skaltu velja ![Sýna sem lista](media/ui_show_as_list_icon.png "Sýna sem lista ör til vinstri") tákn til að sýna sem lista.

<!--
When you want to search for data, such as customer names, addresses, or product groups, you enter criteria. In search criteria you can use all the numbers and letters that you normally use in the specific field. In addition, you can use special symbols to further filter the results. There are two ways to search: using the Quick Filter or column filters.
-->

## <a name="sorting"></a>Röðun
Með Röðun er auðvelt og fljótlegt að fá yfirsýn yfir gögnin. Ef þú ert með marga viðskiptamenn til dæmis, er hægt að velja að raða þeim eftir **númeri Viðskiptamanns**, **Bókunarflokkum viðskiptavinar**, **Gjaldmiðilskóði**, **LandsSvæðiskóða**, eða **skráningarnúmer Söluskatts** til að fá það yfirlit sem þú þarft.

Til að raða á lista, geturðu annað hvort valið fyrirsagnatexta dálka til að skipta á milli hækkandi og lækkandi pöntunar, eða valið litlu niður-örina í dálkafyrirsögninni, og síðan valið **Hækkandi** eða **Lækkandi**.  

> [!NOTE]  
>   Myndir, BLOB-reitir, FlowFilters og reitir sem tilheyra ekki töflu styðja ekki röðun.  

## <a name="searching"></a>Leit
<!--## Searching by using the Quick Filter -->
 Efst á sérhverri listasíðu er ![Leita í lista](media/ui-search/search-list.png "Leita í listatákni") **Leita** tákn sem býður upp á fljótlega og auðvelda leið til að vinna gögnin niður í lista og sýna einungis þær skrár sem innihalda gögnin sem þú vilt sjá.

Til að leita, skaltu einfaldlega velja leitartáknið, og síðan skrifa í boxið textann sem þú ert að leita að. Þú getur slegið inn stafi, númer og önnur tákn.

### <a name="fine-tuning-the-search"></a>Fínstilla leitina
Almennt séð mun leitin reyna að finna samsvörun við textann í öllum reitum; hún gerir ekki greinarmun á hástöfum og lágstöfum (með öðrum orðum, óháð há- og lágstöfum) og mun finna textasamsvörun hvar sem er í reitnum (fremst, aftast eða í miðjunni).

Hins vegar geturðu búið til nákvæmari leit með því að nota eftirfarandi sértákn:

- Til að finna aðeins reitargildi sem samsvara öllum textanum og stöfunum, skal staðsetja textann á milli einfaldra gæsalappa `''` (til dæmis, `'man'`).

- Til að finna reitargildi sem byrja á ákveðnum texta og samsvara stöfunum, skal setja `*` á eftir leitartextanum (til dæmis `man*`).

- Til að finna reitargildi sem enda á ákveðnum texta og samsvara stöfunum, skal setja `*` á undan leitartextanum (til dæmis `*man`).

- Þegar `''` eða `*` er notað er leitin háð há- og lágstöfum. Ef þú vilt gera leitina óháða há- og lágstöfum skaltu setja `@` á undan leitartextanum (til dæmis `@man*`).

Eftirfarandi tafla sýnir nokkur dæmi til að útskýra hvernig hægt er að nota leitina.

|Leitarskilyrði|Finnur ...|
|---------------|----------|
|`man`<br />eða <br />`Man`|Allar skrár með reitum sem innihalda textann **man**, óháð því hvort notaðir eru há- eða lágstafir. Til dæmis, **Manchester**, **manual**, eða **Sportsman**. |
|`'Man'`|Allar skrár með reitum sem innihalda aðeins **Man**, í samræmi við há- og lágstafi.|
|`Man*`|Allar skrár með reitum sem byrja á textanum <b>Man</b>, í samræmi við há- og lágstafi. Til dæmis, **Manchester** en ekki **manual** eða **Sportsman** .|
|`@Man*`|Allar skrár með reitum sem byrja með **man**, óháð því hvort notaðir eru há- eða lágstafir. Til dæmis, **Manchester** og **manual**, en ekki **Sportsman**.|
|`@*man`|Allar skrár sem endar með **man**, óháð því hvort notaðir eru há- eða lágstafir. Til dæmis **Sportsman**, en ekki **Manchester** eða **manual**.|

> [!TIP]
> Þú getur ýtt á F3 til að virkja og slökkva á leitarreitnum. Frekari upplýsingar er að finna í [Flýtilyklar](keyboard-shortcuts.md#KeyboardFilter).

## <a name="Filtering"> </a>Afmörkun
Síun veitir háþróaðri og fjölhæfur leið til að stjórna hvaða skrár sem birtast á lista. Það eru tvær helstu munur á leit og síun, eins og lýst er í töflunni hér að neðan.

|| **Leit** | **Afmörkun** |
|--|----------|------------|
| **Reitir sem gilda** | Leitar yfir alla reitum sem eru sýnilegar á síðunni. | Síar einn eða fleiri reiti, hvern fyrir sig, og velur úr öllum reitum í töflunni, þar á meðal reiti sem eru ekki sýnilegar á síðunni. |
| **Samsvörun** | Sýnir skrár með reitum sem passa við leitartexta, óháð notkun há- og lágstafa, eða staðsetningu þess texta. | Sýnir skrár þar sem reiturinn passar nákvæmlega við síuna og gerir greinarmun á há- og lágstöfum, nema sérstakar síu tákn séu slegin inn.

Síun gerir þér kleift að birta skrár fyrir tiltekna reikninga eða viðskiptamenn, dagsetningar, upphæð og aðrar upplýsingar með því að tilgreina síuviðmiðanir. Aðeins eru birtar þær færslur sem uppfylla skilyrðin. Ef þú tilgreinir skilyrði fyrir marga reiti, þá birtast aðeins skrár sem passa við öll skilyrði.

### <a name="working-in-the-filter-pane"></a>Vinna í síusvæðinu

Til að birta afmörkunarsvæðið skal velja ![Tákn fyrir afmörkunarsvæði](media/open-filter-pane-icon.png "Tákn fyrir afmörkunarsvæði") efst í listanum eða ýta á **Shift+F3**. Fyrir lista innan Mitt hlutverk geturðu einnig valið niður-örina nálægt síðutitlinum í yfirlitsstikunni yfir listanum og síðan **Sýna síusvæði** eins og sýnt er hér:

![Sýna síusvæði](media/open-filter-pane.png "Sýna síusvæði")

Síusvæðið sýnir núverandi síur fyrir lista og gerir þér kleift að stilla eigin sérsniðna síur í einu eða fleiri reitum. Eftirfarandi mynd sýnir dæmi um síusvæði fyrir sölutilboðalista.

![Yfirlit yfir síusvæðið ](media/filter-pane-overview.png "Síutákn")

Síusvæði er skipt í þrjá hluta: **Skoðanir**, **Sía listi eftir** og **Sía samtölur eftir**:

- **Yfirlit**

  Sumir listar muna hafa **Skoðanir** hlutann með. Skoðanir eru afbrigði af listanum sem hefur verið forstillt með síum. Til að skipta yfir í annað yfirlit á listanum þínum skaltu einfaldlega velja annan tengil. Þú getur breytt síum tímabundið á yfirliti, en breytingar verða ekki varanlega vistaðar.

- **Sía listi eftir**

  **Sía lista eftir** hlutinn er þar sem þú bætir við síum á tilteknum reitum til að draga úr fjölda birtra skráa. Til að bæta við síu skaltu velja **+ Sía**, veldu reitinn sem þú vilt sía, úr öllum reitum sem er í töflunni, og sláðu síðan inn síuviðmiðanir í glugganum.

- **Sía samtölur eftir**

  Sumar listar sem sýna reiknaðir reitir, svo sem upphæðir og fjölda, munu innihalda **Sía samtölur eftir** hlutann þar sem þú getur breytt ýmsum víddum sem hafa áhrif á útreikninga. Til dæmis getur þú gert skjóta greiningu á bókhaldslyklinum þínum með því að sía upphæðir á tilteknu tímabili eða þú getur skoðað samtölur fyrir sölupantanir aðeins frá tilteknu vörugeymslu.

  Til að bæta við síu, veldu **+ Sía**, veldu eitt af fyrirfram ákveðnum víddum og svo bæta við síuviðmiðunum í reitnum.

  > [!NOTE]
  > Síur í **Sía samtölur eftir** hlutanum eru stjórnað af FlowFilters í síðuhönnuninni. Fyrir tæknilegar upplýsingar, sjá [FlowFilters](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/developer/devenv-flowfilter-overview).


### <a name="entering-filter-criteria-in-the-filter-pane"></a>Slá inn síuviðmiðanir í síusvæðinu
Til að velja reit til að sía skaltu gera eitt af eftirfarandi:
  - Í síusvæðinu, veldu **+ Reitur**. Sláðu inn heiti reitsins sem þú vilt sía eða veldu reit frá valmyndinni sem sýnir alla reiti í töflunni.

  - Í dálkhausi, veldu niður-örina og veldu síðan **Sía ...**. Þetta mun opna síusvæðið og bæta dálknum við síusvæðið.

Þú getur nú skrifað eða valið síuskilyrði í glugganum. Tegund reitsins sem þú síar ákvarðar hvaða skilyrði þú getur slegið inn. Til dæmis, að sía reit sem hefur fasta gildi mun einungis leyfa þér að velja úr þeim gildum. Nánari upplýsingar um sérstaka síu tákn sjá [Sía viðmiðanir](#FilterCriteria) og [Síumerki](#FilterTokens).

Dálkar sem þegar eru með síur eru auðkenndar með ![Síutákn](media/ui-search/filter-icon.png "Síutákn") í dálkhausnum. Til að fjarlægja síu skaltu velja dálkhausinn og svo velja **Hreinsa síu** .


### <a name="entering-filter-criteria-without-using-the-filter-pane"></a>Slá inn síuskilyrði án þess að nota síusvæðið
Þú getur tilgreint einfaldar síur beint á listanum án þess að þurfa að nota síusvæðið.
Með hvaða reit sem er valinn í röð, nota **Alt + F3** flýtilykil til að birta aðeins skrár sem hafa sama gildi. Þú getur síðan valið annan reit og notað sömu flýtileið aftur til að halda áfram að hreinsa síurnar. Ef valinn reitur er nú þegar síað, mun notkun á **Alt + F3** eyða þeirri síu.

> [!TIP]
> Finna og greina gögnin þín fljótar með því að nota samsetningar flýtilykla. Til dæmis, veldu reit, notaðu **Shift + Alt + F3** til að bæta reitnum við síusvæðið, sláðu inn síuviðmiðin, notaðu **Ctrl + Enter** til að fara aftur í raðirnar, veldu annað reit og notaðu **Alt + F3** til að sía í það gildi.
Frekari upplýsingar er að finna í [Flýtilyklar](keyboard-shortcuts.md#KeyboardFilter).


## <a name="FilterCriteria"> </a>Síuskilyrði og tákn
Þegar skilyrði eru sett er hægt að nota alla sömu tölustafi og bókstafi sem venjulega eru notaðir í reitnum. Ennfremur er hægt að nota sértákn til að afmarka niðurstöðurnar frekar. Í eftirfarandi töflum eru táknin sem hægt er að nota í afmarkanir. Fyrir dagsetningar og tíma er einnig hægt að vísa til [Vinna með dagsetningar og tíma í dagatali](ui-enter-date-ranges.md) til að fá nánari upplýsingar.

> [!IMPORTANT]  
>  Það geta verið tilvik þar sem gildi reita innihalda þessi tákn og þú vilt setja afmörkun á þau. Til að gera það, verðurðu að hafa með afmörkunarsegðina sem inniheldur táknið með gæsalöppum („“). Til dæmis, ef þú vilt sía á færslum sem byrja á textanum *S&R*, er síusegðin `'S&R*'`.  

### <a name="-interval"></a>(..) Bil

|Dæmi|Sýndar færslur|  
|-----------------------|-----------------------|  
|`1100..2100`|Tölur 1100 til 2100.|  
|`..2500`|Reikningar til og með 2500|  
|`..12 31 00`|Dagsetningar til og með 31. 12. 00.|  
|`P8..`|Upplýsingar um reikningstímabil 8 og síðar.|  
|`..23`|Frá upphafsdegi til 23. þessa mánaðar – þessa árs 23:59:59|  
|`23..`|Frá 23. þessa mánaðar – þessa árs 00:00:00 til loka tímans|  
|`22..23`|Frá 22. þessa mánaðar – þessa árs 00:00:00 til 23. þessa mánaðar – þessa árs 23:59:59|  

### <a name="124-eitheror"></a>(&#124;) Annaðhvort eða  

|Dæmi|Sýndar færslur|  
|-----------------------|-----------------------|  
|`1200|1300`|Tölur með 1200 eða 1300|  

### <a name="-not-equal-to"></a>(<>) Ekki jafnt og  

|Dæmi|Sýndar færslur|  
|-----------------------|-----------------------|  
|`<>0`|Allar tölur aðrar en 0<br /><br /> Valkosturinn SQL Server býður upp á að sameina þetta tákn algildistákni. Til dæmis merkir <>A* ekki jafnt og neinn texti sem byrjar á stafnum A.|  

### <a name="-greater-than"></a>(>) Meira en  

|Dæmi|Sýndar færslur|  
|-----------------------|-----------------------|  
|`>1200`|Tölur hærri en 1200|  

### <a name="-greater-than-or-equal-to"></a>(>=) Hærra en eða jafnt og  

|Dæmi|Sýndar færslur|  
|-----------------------|-----------------------|  
|`>=1200`|Tölur hærri en eða jafnar 1200|  

### <a name="-less-than"></a>(<) Minna en  

|Dæmi|Sýndar færslur|  
|-----------------------|-----------------------|  
|`<1200`|Tölur lægri en 1200|  

### <a name="-less-than-or-equal-to"></a>(<=) Lægra en eða jafnt og  

|Dæmi|Sýndar færslur|  
|-----------------------|-----------------------|  
|`<=1200`|Tölur lægri en eða jafnar 1200|  

### <a name="-and"></a>(&) Og  

|Dæmi|Sýndar færslur|  
|-----------------------|-----------------------|  
|`>200&<1200`|Tölur hærri en 200 og minni en 1200|  

### <a name="-an-exact-character-match"></a>('') Nákvæm stafasamsvörun  

|Dæmi|Sýndar færslur|  
|-----------------------|-----------------------|  
|`'man'`|Texta sem passar nákvæmlega við Man og er stafréttur.|  

### <a name="-case-insensitive"></a>(@) Stafrétt  

|Dæmi|Sýndar færslur|  
|-----------------------|-----------------------|  
|`@man*`|Texti sem byrjar á Man og er ekki stafréttur.|  

### <a name="-an-indefinite-number-of-unknown-characters"></a>(*) Ótilgreindur fjöldi óþekktra staftákna

|Dæmi|Sýndar færslur|  
|-----------------------|-----------------------|  
|`*Co*`|Texta sem inniheldur „Co“  og er stafréttur.|  
|`*Co`|Texta sem endar á „Co“  og er stafréttur.|  
|`Co*`|Texta sem byrjar á „Co“  og er stafréttur.|  

> [!NOTE]  
>   Þú getur ekki notað `*` þegar þú ert að sía á valkostum (tölusetning) reitum, svo sem **Staða** reitinn á sölupöntunum. Til að færa inn afmörkun fyrir þessa gerð reits, er hægt að færa inn númeragildið sem afmörkunarbreytu. Til dæmis, í **Staða** reitinn á sölupöntun sem hefur gildin **Opna**, **Sleppt**, **Bíður eftir samþykki** og **Bíður eftir fyrirframgreiðslu**, skal nota gildin `0`, `1`, `2` og `3` til að sía fyrir þessar valkostir.

### <a name="-one-unknown-character"></a>(?) eitt óþekkt stafatákn  

|Dæmi|Sýndar færslur|  
|-----------------------|-----------------------|  
|`Hans?n`|Texti eins og Hansen eða Hanson|  

### <a name="combined-format-expressions"></a>Sameinað framsetningarsnið  

|Dæmi|Sýndar færslur|  
|-----------------------|-----------------------|  
|`5999|8100..8490`|Allar færslur með tölunni 5999 eða tölu á bilinu frá 8100 til og með 8490 er teknar með.|  
|`..1299|1400..`|Telja með færslur með tölu sem er lægri eða jöfn 1299 eða tölu sem er jöfn 1400 eða hærri (allar tölur nema 1300 til 1399).|  
|`>50&<100`|Telja með færslur með tölum sem eru hærri en 50 og lægri en 100 (tölurnar 51 til 99).|  


## <a name="FilterTokens"> </a>Síumerki
Þegar þú slærð inn síuviðmiðanir getur þú einnig skrifað orð sem hafa sérstaka þýðingu, sem kallast síumerki. Eftir að hafa slegið inn merkiorðið, er orðinu skipt út fyrir gildin sem það táknar. Þetta gerir síun auðveldara með því að draga úr þörfinni á að fara yfir á aðrar síðum til að fletta upp gildi sem þú vilt bæta við síuna. Taflan hér fyrir neðan lýsir sumum merkjunum sem þú getur slegið inn sem síuviðmiðanir.

> [!TIP]
> Stofnunin þín getur notað sérsniðna merki. Til að læra um öll merkin sem þú hefur aðgang að eða til að bæta við fleiri sérsniðnum merkjum, skaltu tala við stjórnandann þinn. Fyrir tæknilegar upplýsingar, sjá [Bæta við síumerkjum](/dynamics365/business-central/dev-itpro/developer/devenv-adding-filter-tokens).


### <a name="me-or-userid-records-assigned-to-you"></a>(%me eða %userid) Skrám úthlutað til þín

Notaðu `%me` eða `%userid` þegar verið er að sía reiti sem innihalda notandakenni, svo sem **úthlutað til notandakennis** reit, til að birta allar skrár sem eru úthlutað til þín.

|Dæmi|Sýndar færslur|  
|-----------------------|-----------------------|  
|`%me`<br />eða<br />`%userid`|Skrár sem eru úthlutað á notandareikninginn þinn. |  

### <a name="mycustomers-customers-in-my-customers"></a>(%mycustomers) Viðskiptamenn í Mínir viðskiptamenn

Notaðu `%mycustomers` í **Nr** reitnum viðskiptamanns til að birta allar skrár fyrir viðskiptamenn sem eru innifaldir í **Mínir viðskiptamenn** listanum á Mitt hlutverk.

|Dæmi|Sýndar færslur|  
|-----------------------|-----------------------|  
|`%mycustomers`|Viðskiptamenn í **Mínir viðskiptamenn** í Mitt hlutverk. |  

### <a name="myitems-items-in-my-items"></a>(%mytems) Atriði í Mínum atriðum

Notaðu `%myitems` Í atriði **Nr** reitinn til að birta allar skrár fyrir atriði sem eru innifalin í **Mín atriði** listanum í Mitt hlutverk.

|Dæmi|Sýndar færslur|  
|-----------------------|-----------------------|  
|`%myitems`|Atriði í **Mín atriði** í Mitt hlutverk. |  

### <a name="myvendors-vendors-in-my-vendors"></a>(%myvendors) Lánardrottnar í Mínir lánardrottnar

Notaðu `%myvendors` í lánardrottinn **Nr** reitnum, til að birta allar skrá fyrir lánardrottna sem eru innifalin í **Mínir lánardrottnar** listanum í Mitt hlutverk.

|Dæmi|Sýndar færslur|  
|-----------------------|-----------------------|  
|`%myvendors`|Lánardrottnar í **Mínir lánardrottnar** í Mitt hlutverk. |  


## <a name="see-also"></a>Sjá einnig
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Algengar spurningar um leit og síun](ui-search-filter-faq.md)
