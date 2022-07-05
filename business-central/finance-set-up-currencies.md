---
title: Setja upp gjaldmiðla
description: Setja verður upp hvern gjaldmiðil ef hann er keyptur eða seldur í gjaldmiðlum öðrum en gjaldmiðli (ISK) eða ef fjárhagsfærslur eru skráð í mismunandi gjaldmiðlum.
author: edupont04
ms.topic: conceptual
ms.search.keywords: multiple currencies
ms.search.form: 5, 118
ms.date: 03/15/2022
ms.author: edupont
ms.openlocfilehash: e501f61f61aec9d9ffc4acd9607ee6b9cf22e74f
ms.sourcegitcommit: 00a8acc82cdc90e0d0db9d1a4f98a908944fd50a
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/29/2022
ms.locfileid: "9074901"
---
# <a name="set-up-currencies"></a>Setja upp gjaldmiðla

[!INCLUDE [finance-currencies-def](includes/finance-currencies-def.md)]

Notaðu utanaðkomandi þjónustu til að fá nýjustu gengi gjaldmiðla inn á **gjaldeyrislistann**. Frekari upplýsingar er að finna í [Að setja upp þjónustu um gengi gjaldmiðils](finance-how-update-currencies.md#to-set-up-a-currency-exchange-rate-service).  

[!INCLUDE [finance-currencies-lcy](includes/finance-currencies-lcy-note.md)]

## <a name="currencies"></a><a name="curr"></a> Gjaldmiðlum

Eftirfarandi tafla lýsir svæðunum á **listanum Gjaldmiðlar**.

|Svæði|Lýsing|  
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

|Valmynd|Aðgerð|Lýsing|
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

Til að vinna með gjaldmiðla sem nota ekki tugabrot og til að forðast óþörf tugabrot í erlendum gjaldmiðlum er hægt að nota tvo mismunandi sléttunareiginleika:

- Sléttun einingaupphæða  

- Sléttun upphæða  

Þessa eiginleika má nota sinn í hvoru lagi eða saman. Auk þess er hægt að nota þessa eiginleika með sléttun reiknings.

Ólíkt eiginleikanum sléttun reiknings hafa eiginleikarnir sléttun upphæða og sléttun einingaupphæða aðeins áhrif á upphæðir í erlendum gjaldmiðli-ekki samsvarandi upphæðir í SGM. Þessir tveir eiginleikar skila ekki af sér neinum færslum í fjárhagsreikninga. Því þarf ekki að tilgreina fjárhagsreikning í bókunarflokkum eða annarsstaðar.

### <a name="unit-amount-rounding"></a>Sléttun einingaupphæða

Sléttunareiginleiki einingar-upphæðar stýrir því hvernig söluverð vara og forða í erlendum gjaldmiðlum eru sléttuð í sölu-og innkaupalínum. Tilgreina verður reglur fyrir hvern gjaldmiðil fyrir sig, í reitnum Sléttunarnákvæmni **í einingu-upphæð á** listanum Gjaldmiðlar **.**

Eiginleikinn sléttun einingaupphæða er notaður sjálfkrafa í hvert skipti sem vara eða forðanúmer er færð inn í sölulínu. Ef reikningurinn er fyrir viðskiptamann með gjaldmiðilskóta er verði vörunnar eða forðans breytt í gjaldmiðil viðskiptamannsins. Verðið er sléttað samkvæmt sléttunarnákvæmni einingaupphæða fyrir gjaldmiðilinn.

### <a name="amount-rounding"></a>Sléttun upphæða

Sléttunaraðgerðin upphæð stýrir því hvernig upphæðir í erlendum gjaldmiðlum eru sléttaðar í færslubókarlínum, sölulínum og innkaupalínum. Tilgreina verður reglur fyrir hvern gjaldmiðil fyrir sig, í **reitnum Upphæðarsléttunarnákvæmni** á **listanum Gjaldmiðlar**.

Upphæðir í erlendum gjaldmiðlum eru sléttaðar þegar fyllt er út í færslubókarlínur, sölulínur og innkaupalínur og þær bókaðar.

## <a name="exchange-rates"></a>Gengi gjaldmiðla

Hægt er að skrá gengi fyrir hvern erlendan gjaldmiðil og tilgreina frá hvaða dagsetningu gengin gilda. Til dæmis er hægt að færa inn dag-, mánaðar- eða ársfjórðungsgengi hvers erlends gjaldmiðils.

Hægt er að varðveita sögulegt gengi í **síðunni gengi** gjaldmiðla fyrir tilvísanir. Þegar þú þarft að uppfæra gengi, getur þú notað **hnappinn Uppfæra gengi gjaldmiðla** til að fá nýjasta gengi frá utanaðkomandi þjónustuaðila.

## <a name="general-ledger-accounts"></a>Fjárhagsreikninga

Ekki er hægt að tengja gjaldmiðilskóta við fjárhagsreikninga þar sem upphæðir í fjárhag eru í SGM. Ef fyrirtækið er með lán í USD og setur innborgun á bankareikning í SEK er hægt að fylgjast með þessum reikningum með því að setja upp bankareikninga í USD og SEK. Með bókunarflokkum er hægt að tengja reikningana við viðeigandi fjárhagsreikninga. Í fjárhagnum eru upphæðirnar birtar í SGM.

Hægt er að færa gjaldmiðilskóta inn í færslubókarlínu og bóka línuna í fjárhagsreikning. Viðeigandi gengi er notað til að breyta upphæðinni í SGM áður en hún er bókuð í fjárhagsreikninginn.  

## <a name="example-of-a-receivable-currency-transaction"></a>Dæmi um móttekna gjaldmiðilsfærslu

[!INCLUDE [finance-currencies-example](includes/finance-currencies-example.md)]

## <a name="see-related-training-at-microsoft-learn"></a>Sjá tengdar þjálfun hjá [Microsoft Learn](/learn/modules/currencies-exchange-rates-dynamics-365-business-central/)

## <a name="see-also"></a>Sjá einnig .

[Uppfæra gengi](finance-how-update-currencies.md)  
[Setja upp annan skýrslugjaldmiðil](finance-how-setup-additional-currencies.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]