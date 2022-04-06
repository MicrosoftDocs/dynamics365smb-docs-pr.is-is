---
title: Setja upp gjaldmiðla
description: Setja verður upp hvern gjaldmiðil ef hann er keyptur eða seldur í gjaldmiðlum öðrum en gjaldmiðli (ISK) eða ef fjárhagsfærslur eru skráð í mismunandi gjaldmiðlum.
author: edupont04
ms.topic: conceptual
ms.search.keywords: multiple currencies
ms.search.form: 5, 118
ms.date: 03/15/2022
ms.author: edupont
ms.openlocfilehash: f36d255c555c9ac83205a675bc7647cb02e0b3c2
ms.sourcegitcommit: 521735f8e27d8bff2d2dfbe94d240c09dcdaec29
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 03/15/2022
ms.locfileid: "8419528"
---
# <a name="set-up-currencies"></a>Setja upp gjaldmiðla

[!INCLUDE [finance-currencies-def](includes/finance-currencies-def.md)]

Notaðu utanaðkomandi þjónustu til að fá nýjustu gengi gjaldmiðla inn á **gjaldeyrislistann**. Frekari upplýsingar er að finna í [Að setja upp þjónustu um gengi gjaldmiðils](finance-how-update-currencies.md#to-set-up-a-currency-exchange-rate-service).  

[!INCLUDE [finance-currencies-lcy](includes/finance-currencies-lcy-note.md)]

## <a name="currencies"></a><a name="curr"></a> Gjaldmiðlum

Eftirfarandi tafla lýsir svæðunum á **listanum Gjaldmiðlar**.

|Svæði|Description|  
|---------------------------------|---------------------------------------|  
|**Kóði**|Kenni gjaldmiðils.|
|**Lýsing**|Frjáls textalýsing á færslunni.|
|**ISO-kóði**|Alþjóðlegi þriggja bókstafa kóðinn tilheyrir gjaldmiðlinum sem er skilgreindur í ISO 4217.|
|**ISO-talnakóði**|Alþjóðlega tilvísunin í gjaldmiðlinn sem er skilgreindur í ISO 4217.|
|**Dagsetning gengis**|Nýjasta dagsetning gengis.|
|**EMU-gjaldmiðill**|Tilgreinir hvort gjaldmiðillinn er gjaldmiðill EMB (Evrópska efnahags- og myntbandalagsins).|
|**Reikningur innleysts hagnaðar**|Reikningurinn þar sem raunverulegur hagnaður verður bókaður þegar þú færð útistandandi greiðslur eða skráir raunverulegt gengi á greiðslur viðskiptaskulda. Dæmi um móttekna gjaldmiðilsfærslu er að finna í dæminu fyrir neðan þessa töflu. |
|**Reikningur innleyst taps**|Reikningurinn þar sem raunverulegt tap verður bókað þegar þú færð útistandandi greiðslur eða skráir raunverulegt gengi á greiðslur viðskiptaskulda. Dæmi um móttekna gjaldmiðilsfærslu er að finna í dæminu fyrir neðan þessa töflu. |
|**Reikningur óinnleysts hagnaðar**|Reikningurinn þar sem fræðilegur hagnaður verður bókaður þegar gjaldmiðlaleiðrétting er framkvæmd.|
|**Reikningur áætlaðs taps**|Reikningurinn þar sem fræðilegt tap verður bókað þegar gjaldmiðlaleiðrétting er framkvæmd.|
|**Sléttunarnákvæmni upphæða**|Sumir gjaldmiðlar hafa önnur snið fyrir reikningsupphæðir en þau sem eru tilgreind er á síðunni **Uppsetning fjárhagsgrunns**. Ef sléttunarnákvæmni er breytt fyrir gjaldmiðil verða allar reikningsupphæðir í gjaldmiðlinum sléttaðar með uppfærðri nákvæmni.|
|**Aukastafir upphæðar**|Sumir gjaldmiðlar hafa önnur snið fyrir reikningsupphæðir en þau sem eru tilgreind er á síðunni **Uppsetning fjárhagsgrunns**. Ef tugasætum upphæðar er breytt fyrir gjaldmiðil verða allar reikningsupphæðir í gjaldmiðlinum sléttaðar með uppfærðum tugabrotum|
|**Sléttunargerð reikninga**|Tilgreinir aðferðina sem nota skal ef slétta þarf fjárhæðirnar. Valkostirnir eru **Næst**, **Upp** og **Niður**.|
|**Sléttunarnákvæmni einingaupphæða**|Sumir gjaldmiðlar hafa önnur snið fyrir einingaupphæðir en þau sem eru tilgreind er á síðunni **Uppsetning fjárhagsgrunns**. Ef sléttunarnákvæmni einingaupphæðar er breytt fyrir gjaldmiðil verða allar einingaupphæðir í gjaldmiðlinum sléttaðar með uppfærðri nákvæmni.|
|**Aukastafir einingarupphæðar**|Sumir gjaldmiðlar hafa önnur snið fyrir einingaupphæðir en þau sem eru tilgreind er á síðunni **Uppsetning fjárhagsgrunns**. Ef tugasætum einingaupphæðar er breytt fyrir gjaldmiðil verða allar einingaupphæðir í gjaldmiðlinum sléttaðar með uppfærðum tugabrotum.|
|**Sléttunarnákvæmni jöfnunar**|Tilgreinir bilið sem er leyft fyrir þennan gjaldmiðil sem sléttunarmismunur þegar færslum er jafnað hverri við aðra.|
|**Umbreyting SGM sléttunar debetreikningur**|Tilgreinir upplýsingar um umreikning sem verða einnig að innihalda debetreikning ef setja á inn leiðréttingarlínur fyrir sléttunarmismun í færslubókum með virkninni **Setja inn sléttun umreiknings í SGM**.|
|**Umbreyting SGM sléttunar kreditreikningur**|Tilgreinir upplýsingar um umreikning sem verða einnig að innihalda kreditreikning ef setja á inn leiðréttingarlínur fyrir sléttunarmismun í færslubókum með virkninni **Setja inn sléttun umreiknings í SGM**.|
|**Síðast leiðrétt, dags.**|Dagsetning síðustu gjaldmiðlaleiðréttingar.|
|**Síðast breytt, dags.**|Dagsetning breytingarinnar á uppsetningu gjaldmiðilsins.|
|**Vikmörk greiðslu %**|Hámark greiðsluvikmarka % sem er stillt fyrir þennan gjaldmiðil. Frekari upplýsingar eru í [Greiðsluvikmörk og greiðsluafsláttarvikmörk](finance-payment-tolerance-and-payment-discount-tolerance.md). |
|**Hám.upph. greiðsluvikmarka**|Hámarksfjárhæð greiðsluvikmarka fyrir þennan gjaldmiðil. Frekari upplýsingar eru í [Greiðsluvikmörk og greiðsluafsláttarvikmörk](finance-payment-tolerance-and-payment-discount-tolerance.md). |
|**Gengisstuðull**|Tilgreinir sambandið milli gjaldmiðilsins og staðbundins gjaldmiðils samkvæmt raunverulegu gengi.|
|**Reikningur orðins fjárh.hagn.**|Tilgreinir fjárhagsreikninginn sem gengishagnaður bókast í vegna leiðréttingar á milli staðbundins gjaldmiðils (SGM) og annars skýrslugjaldmiðils. Gengishagnaðurinn er reiknaður þegar keyrslan Leiðrétta gengi er keyrð til að leiðrétta fjárhagsreikninga. Þessi reitur er kannski ekki sýnilegur sjálfkrafa. Hægt er að sækja hana með því að sérstilla síðuna.|
|**Reikningur orðins fjárh.taps**|Tilgreinir fjárhagsreikninginn sem gengistap bókast í vegna leiðréttingar á milli staðbundins gjaldmiðils (SGM) og annars skýrslugjaldmiðils. Gengishagnaðurinn er reiknaður þegar keyrslan Leiðrétta gengi er keyrð til að leiðrétta fjárhagsreikninga. Þessi reitur er kannski ekki sýnilegur sjálfkrafa. Hægt er að sækja hana með því að sérstilla síðuna.|
|**Afgangsreikningur hagnaðar**|Tilgreinir fjárhagsreikning sem notaður er til að bóka afgangsupphæðir hagnaðar (sléttunarmismun) þegar annar skýrslugjaldmiðill er notaður í kerfishluta fjárhags. Þessi reitur er kannski ekki sýnilegur sjálfkrafa. Hægt er að sækja hana með því að sérstilla síðuna.|
|**Afgangsreikningur taps**|Tilgreinir fjárhagsreikning sem notaður er til að bóka afgangsupphæðir taps (sléttunarmismun) þegar annar skýrslugjaldmiðill er notaður í kerfishluta fjárhags. Þessi reitur er kannski ekki sýnilegur sjálfkrafa. Hægt er að sækja hana með því að sérstilla síðuna.|
|**Hám. VSK-mismunur leyfður**|Leyfileg hámarksupphæð vegna virðisaukaskattsmismunar í þessum gjaldmiðli. Frekari upplýsingar eru í [Handvirk breyting VSK-upphæða í sölu- og innkaupaskjölum](finance-work-with-vat.md#correcting-vat-amounts-manually-in-sales-and-purchase-documents). Þessi reitur er kannski ekki sýnilegur sjálfkrafa. Hægt er að sækja hana með því að sérstilla síðuna.|
|**Sléttunartegund VSK**|Tilgreinir sléttunaraðferð fyrir handvirka breytingu VSK-upphæða í sölu- og innkaupaskjölum. Þessi reitur er kannski ekki sýnilegur sjálfkrafa. Hægt er að sækja hana með því að sérstilla síðuna.|

### <a name="available-currency-functions"></a>Tiltækar gjaldmiðilsaðgerðir

Í eftirfarandi töflu er gerð grein fyrir lykilaðgerðum á síðunni **Gjaldmiðlar**.  

|Valmynd|Aðgerð|Description|
|-------------|--------------|------------------------------|
|**Vinna**|**Stinga upp á reikningum**|Nota reikninga úr öðrum gjaldmiðlum. Algengustu reikningarnir verða settir inn.|
||**Breyta greiðsluvikmörkum**|Breyta annaðhvort eða bæði hámarks greiðsluvikmörkum eða prósentutölu greiðsluvikmarka og afmarka eftir gjaldmiðli. Frekari upplýsingar eru í [Greiðsluvikmörk og greiðsluafsláttarvikmörk](finance-payment-tolerance-and-payment-discount-tolerance.md)|
||**Gengi gjaldmiðla**|Skoða uppfært gengi fyrir gjaldmiðlana sem eru notaðir.|
||**Leiðrétta gengi**|Leiðrétta fjárhags-, viðskiptamanna-, lánadrottna- og bankareikningsfærslur til að staðan sé uppfærð ef gengið hefur breyst síðan færslurnar voru bókaðar.|
||**Skráningu gengisleiðréttingar**|Skoða niðurstöður runuvinnslunnar **Leiðrétta gengi**. Ein lína er búin til fyrir hvern gjaldmiðil sem leiðréttur er, eða gjaldmiðil og bókunarflokk.|
|**Gengisþjónusta**|**Gengisþjónustur**|Skoða eða breyta uppsetningunni á þjónustunni sem er sett upp til að sækja uppfært gengi gjaldmiðla þegar þú velur aðgerðina **Uppfæra gengi**.|
||**Uppfæra gengi**|Sækja nýjasta gengi gjaldmiðils frá þjónustuveitu.|
|**Skýrslur**|**Gengisjöfnuður**|Skoða stöðuna hjá öllum viðskiptamönnum og lánardrottnum bæði í erlendum gjaldmiðli og staðbundnum gjaldmiðli (SGM). Skýrslan sýnir tvær stöður í SGM. Einn er staðan í erlendum gjaldmiðli umreiknuð í SGM með því að nota gengi á tíma færslunnar. Hinn er staðan í erlendum gjaldmiðli umreiknuð í SGM með því að nota gengi á vinnudagsetningu.|

## <a name="lcy-and-other-currencies"></a>ISK og annarra gjaldmiðla

[!INCLUDE [finance-currencies-lcy-def](includes/finance-currencies-lcy-def.md)]

## <a name="rounding-currencies"></a>Sléttun gjaldmiðla

Til að stjórna gjaldmiðlum sem ekki nota aukastafi og til að forðast óþarfa aukastaf í erlendum gjaldmiðli er hægt að nota tvo mismunandi sléttunareiginleika:

- Eining-sléttun upphæðar  

- Sléttun upphæðar  

Þessir eiginleikar geta starfað sjálfstætt eða í samsetningu. Að auki geta aðgerðirnar starfað í tengslum við reikningssléttun.

Öfugt við reikningssléttun, hafa sléttunaraðgerðirnar upphæð og einingaupphæð-sléttun aðeins áhrif á upphæðir í erlendum gjaldmiðli-ekki samsvarandi upphæðir í ISK. Þessar tvær aðgerðir munu ekki leiða til neins í bókunum á fjárhagslykli. Þar af leiðandi þarf ekki að tilgreina almennan fjárhagslykil á bókunarflokkum eða annars staðar.

### <a name="unit-amount-rounding"></a>Eining-sléttun upphæðar

Sléttunareiginleiki einingar-upphæðar stýrir því hvernig söluverð vara og forða í erlendum gjaldmiðlum eru sléttuð í sölu-og innkaupalínum. Tilgreina verður reglur fyrir hvern gjaldmiðil fyrir sig, í reitnum Sléttunarnákvæmni **í einingu-upphæð á** listanum Gjaldmiðlar **.**

Sléttunaraðgerðin eining-upphæð er notuð sjálfkrafa í hvert sinn sem færð er inn vara eða númer forða í sölulínu. Ef reikningurinn er fyrir viðskiptavin með gjaldmiðilskóta er vörunni eða forðaverðinu umbreytt í gjaldmiðil viðskiptavinarins. Verðið er sléttað samkvæmt Sléttunarnákvæmni fyrir gjaldmiðilinn.

### <a name="amount-rounding"></a>Sléttun upphæðar

Sléttunaraðgerðin upphæð stýrir því hvernig upphæðir í erlendum gjaldmiðlum eru sléttaðar í færslubókarlínum, sölulínum og innkaupalínum. Tilgreina verður reglur fyrir hvern gjaldmiðil fyrir sig, í **reitnum Upphæðarsléttunarnákvæmni** á **listanum Gjaldmiðlar**.

Upphæðir í erlendum gjaldmiðlum eru sléttar þegar fyllt er í og bókað í almennar færslubókarlínur, sölulínur og innkaupalínur.

## <a name="exchange-rates"></a>Gengi gjaldmiðla

Hægt er að skrá gengi fyrir hvern erlendan gjaldmiðil og tilgreina frá hvaða dagsetningum gengi gjaldmiðla gildir. Til dæmis er hægt að færa inn daglegt gengi, Mánaðarlegt gengi eða ársfjórðungsleg gengi fyrir hvern erlendan gjaldmiðil.

Hægt er að varðveita sögulegt gengi í **síðunni gengi** gjaldmiðla fyrir tilvísanir. Þegar þú þarft að uppfæra gengi, getur þú notað **hnappinn Uppfæra gengi gjaldmiðla** til að fá nýjasta gengi frá utanaðkomandi þjónustuaðila.

## <a name="general-ledger-accounts"></a>Fjárhagsreikninga

Ekki er hægt að tengja gjaldmiðilskóða við fjárhagslykla þar sem upphæðir í fjárhagsreikningum eru í ISK. Ef þú ert með bankalán í USD og setur innborganir á bankareikning í SEK, geturðu fylgst með þessum reikningum með því að setja upp bankareikninga í USD og SEK. Með bókunarflokkum er hægt að tengja lykla við viðeigandi fjárhagslykla. Í fjárhag er andvirði upphæðanna sýnt í ISK.

Hægt er að færa gjaldmiðilskóða í færslubókarlínu og bóka línuna í fjárhagslykil. Viðeigandi gengi er notað til að umreikna upphæðina í ISK áður en hún er bókuð á fjárhagsreikninginn.  

## <a name="example-of-a-receivable-currency-transaction"></a>Dæmi um móttekna gjaldmiðilsfærslu

[!INCLUDE [finance-currencies-example](includes/finance-currencies-example.md)]

## <a name="see-also"></a>Sjá einnig .

[Uppfæra gengi](finance-how-update-currencies.md)  
[Setja upp annan skýrslugjaldmiðil](finance-how-setup-additional-currencies.md)  
