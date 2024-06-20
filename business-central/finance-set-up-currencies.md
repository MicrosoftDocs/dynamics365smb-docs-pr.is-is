---
title: Setja upp gjaldmiðla
description: Setja þarf upp hvern gjaldmiðil ef keypt er eða selt í öðrum gjaldmiðlum en staðbundnum gjaldmiðli (SGM) eða ef fjárhagsfærslur eru skráðar í mismunandi gjaldmiðlum.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: multiple currencies
ms.search.form: '5, 118'
ms.date: 06/10/2024
ms.service: dynamics-365-business-central
---
# <a name="set-up-currencies"></a>Setja upp gjaldmiðla

[!INCLUDE [finance-currencies-def](includes/finance-currencies-def.md)]

Notið ytri þjónusta til að fá nýjasta gengi gjaldmiðils í gluggann **Gjaldmiðlar**. Nánari upplýsingar eru [í Til að setja upp gengisþjónustu](finance-how-update-currencies.md#set-up-a-currency-exchange-rate-service) fyrir gjaldmiðla.  

[!INCLUDE [finance-currencies-lcy](includes/finance-currencies-lcy-note.md)]

## <a name="currencies"></a><a name="curr"></a>Gjaldmiðlar

Eftirfarandi tafla lýsir reitunum á listanum **Gjaldmiðlar**.

|Svæði|Lýsing|  
|---------------------------------|---------------------------------------|  
|**Kóði**|Kenni gjaldmiðils.|
|**Lýsing**|Frjáls textalýsing á færslunni.|
|**ISO-kóði**|Alþjóðlegi þriggja bókstafa kóðinn tilheyrir gjaldmiðlinum sem er skilgreindur í ISO 4217.|
|**ISO-talnakóði**|Alþjóðlega tilvísunin í gjaldmiðlinn sem er skilgreindur í ISO 4217.|
|**Dagsetning gengis**|Nýjasta dagsetning gengis.|
|**EMU-gjaldmiðill**|Tilgreinir hvort gjaldmiðillinn er gjaldmiðill EMB (Evrópska efnahags- og myntbandalagsins).|
|**Reikningur innleysts hagnaðar**|Reikningurinn þar sem raunverulegur hagnaður er bókaður þegar tekið er á móti greiðslum fyrir útistandandi skuldir eða skráð raunverulegt gjaldmiðilsgengi á greiðslur í gjaldfallnar skuldir. Dæmi um móttekna gjaldmiðilsfærslu er að finna í dæminu fyrir neðan þessa töflu. |
|**Reikningur innleyst taps**|Reikningurinn þar sem raunverulegt tap er bókað þegar tekið er á móti greiðslum fyrir útistandandi skuldir eða skráð raunverulegt gengi gjaldmiðla á greiðslur í gjaldfallnar skuldir. Dæmi um móttekna gjaldmiðilsfærslu er að finna í dæminu fyrir neðan þessa töflu. |
|**Reikningur óinnleysts hagnaðar**|Reikningurinn þar sem fræðilegur hagnaður er bókaður þegar gjaldmiðilsleiðrétting er framkvæmd.|
|**Reikningur áætlaðs taps**|Reikningurinn þar sem fræðilegt tap er bókað þegar gjaldmiðilsleiðrétting er framkvæmd.|
|**Sléttunarnákvæmni upphæða**|Sumir gjaldmiðlar hafa önnur snið fyrir reikningsupphæðir en þau sem eru tilgreind er á síðunni **Uppsetning fjárhagsgrunns**. Ef sléttunarnákvæmni upphæðar er breytt fyrir gjaldmiðil eru allar reikningsupphæðir í þeim gjaldmiðli sléttaðar með uppfærðri nákvæmni.|
|**Aukastafir upphæðar**|Sumir gjaldmiðlar hafa önnur snið fyrir reikningsupphæðir en þau sem eru tilgreind er á síðunni **Uppsetning fjárhagsgrunns**. Ef upphæðinni er breytt fyrir gjaldmiðil eru allar reikningsupphæðir í gjaldmiðlinum sléttaðar með uppfærðum aukastöfum|
|**Sléttunargerð reikninga**|Tilgreinir aðferðina sem nota skal ef slétta þarf fjárhæðirnar. Valkostirnir eru **Næst**, **Upp** og **Niður**.|
|**Sléttunarnákvæmni einingaupphæða**|Sumir gjaldmiðlar hafa önnur snið fyrir einingaupphæðir en þau sem eru tilgreind er á síðunni **Uppsetning fjárhagsgrunns**. Ef sléttunarnákvæmni einingaupphæðar er breytt fyrir gjaldmiðil eru allar einingaupphæðir í gjaldmiðlinum sléttaðar með uppfærðri nákvæmni.|
|**Aukastafir einingarupphæðar**|Sumir gjaldmiðlar hafa önnur snið fyrir einingaupphæðir en þau sem eru tilgreind er á síðunni **Uppsetning fjárhagsgrunns**. Ef aukastöfum einingarupphæðar er breytt fyrir gjaldmiðil eru allar einingarupphæðir í gjaldmiðlinum sléttaðar með uppfærðum aukastöfum.|
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
|**Hám. VSK-mismunur leyfður**|Leyfileg hámarksupphæð vegna virðisaukaskattsmismunar í þessum gjaldmiðli. Nánari upplýsingar eru [í Leiðrétting VSK-upphæða handvirkt á sölu- og innkaupaskjölum](finance-work-with-vat.md#correcting-vat-amounts-manually-on-sales-and-purchase-documents). Þessi reitur er kannski ekki sýnilegur sjálfkrafa. Hægt er að sækja hana með því að sérstilla síðuna.|
|**Sléttunartegund VSK**|Tilgreinir sléttunaraðferð fyrir handvirka breytingu VSK-upphæða í sölu- og innkaupaskjölum. Þessi reitur er kannski ekki sýnilegur sjálfkrafa. Hægt er að sækja hana með því að sérstilla síðuna.|

### <a name="available-currency-functions"></a>Tiltækar aðgerðir gjaldmiðla

Í eftirfarandi töflu er gerð grein fyrir lykilaðgerðum á síðunni **Gjaldmiðlar**.  

|Valmynd|Aðgerð|Lýsing|
|-------------|--------------|------------------------------|
|**Vinna**|**Stinga upp á reikningum**|Nota reikninga úr öðrum gjaldmiðlum. Algengustu reikningarnir sem oftast eru notaðir eru settir inn.|
||**Breyta greiðsluvikmörkum**|Breyta annaðhvort eða bæði hámarks greiðsluvikmörkum eða prósentutölu greiðsluvikmarka og afmarka eftir gjaldmiðli. Frekari upplýsingar eru í [Greiðsluvikmörk og greiðsluafsláttarvikmörk](finance-payment-tolerance-and-payment-discount-tolerance.md)|
||**Gengi**|Skoða uppfært gengi fyrir gjaldmiðlana sem eru notaðir.|
||**Leiðrétta gengi**|Uppfæra stöðu fyrir fjárhags-, viðskiptamanna-, lánardrottna- og bankareikningsfærslur. Uppfærslan er gagnleg ef gengið breyttist eftir bókun færslnanna.|
||**Gengisleiðréttingarskrá**|Skoða niðurstöður runuvinnslunnar **Leiðrétta gengi**. Ein lína er búin til fyrir hvern gjaldmiðil sem leiðréttur er, eða gjaldmiðil og bókunarflokk.|
|**Gengisþjónusta**|**Gengisþjónustur**|Skoða eða breyta uppsetningunni á þjónustunni sem er sett upp til að sækja uppfært gengi gjaldmiðla þegar þú velur aðgerðina **Uppfæra gengi**.|
||**Uppfæra gengi**|Sækja nýjasta gengi gjaldmiðils frá þjónustuveitu.|
|**Skýrslur**|**Gengisjöfnuður**|Skoða stöðuna hjá öllum viðskiptamönnum og lánardrottnum bæði í erlendum gjaldmiðli og staðbundnum gjaldmiðli (SGM). Skýrslan sýnir tvær stöður í SGM. Einn er staðan í erlendum gjaldmiðli umreiknuð í SGM með því að nota gengi á tíma færslunnar. Hinn er staðan í erlendum gjaldmiðli umreiknuð í SGM með því að nota gengi á vinnudagsetningu.|

## <a name="lcy-and-other-currencies"></a>SGM og aðrir gjaldmiðlar

[!INCLUDE [finance-currencies-lcy-def](includes/finance-currencies-lcy-def.md)]

## <a name="rounding-currencies"></a>Sléttun gjaldmiðla

Til að stjórna gjaldmiðlum sem nota ekki tugastafi og til að koma í veg fyrir óþarfa aukastafi í erlendum gjaldmiðli er hægt að nota tvo mismunandi sléttunareiginleika:

- Sléttun einingaupphæða  

- Sléttun upphæða  

Þessa eiginleika má nota sinn í hvoru lagi eða saman. Auk þess er hægt að nota eiginleikann með sléttun reiknings.

Ólíkt eiginleikanum sléttun reiknings hafa eiginleikarnir sléttun upphæða og sléttun einingaupphæða aðeins áhrif á upphæðir í erlendum gjaldmiðli-ekki samsvarandi upphæðir í SGM. Þessir tveir eiginleikar bóka ekkert í fjárhagsreikninga. Því þarf ekki að tilgreina fjárhagsreikning í bókunarflokkum eða annars staðar.

### <a name="unit-amount-rounding"></a>Sléttun einingaupphæða

Eiginleikinn sléttun einingaupphæða stýrir hvernig söluverð fyrir vörur og forða í erlendum gjaldmiðlum eru sléttaðir í sölu- og innkaupalínum. Tilgreina þarf reglurnar fyrir hvern gjaldmiðil sérstaklega í reitnum **Eining - Sléttunarnákvæmni** í listanum **Gjaldmiðlar**.

Eiginleikinn sléttun einingaupphæða er notaður sjálfkrafa í hvert skipti sem vara eða forðanúmer er færð inn í sölulínu. Ef reikningurinn er fyrir viðskiptamann með gjaldmiðilskóta er verði vörunnar eða forðans breytt í gjaldmiðil viðskiptamannsins. Verðið er sléttað samkvæmt sléttunarnákvæmni einingaupphæða fyrir gjaldmiðilinn.

### <a name="amount-rounding"></a>Sléttun upphæða

Eiginleikinn sléttun upphæða stýrir hvernig upphæðir í erlendum gjaldmiðlum eru sléttaðar í færslubókarlínum, sölulínum og innkaupalínum. Tilgreina þarf reglurnar fyrir hvern gjaldmiðil sérstaklega í reitnum **Upph. sléttunarnákvæmni** í listanum **Gjaldmiðlar** .

Upphæðir í erlendum gjaldmiðlum eru sléttaðar þegar fyllt er út í færslubókarlínur, sölulínur og innkaupalínur og þær bókaðar.

## <a name="exchange-rates"></a>Gengi

Hægt er að skrá gengi fyrir hvern erlendan gjaldmiðil og tilgreina frá hvaða dagsetningu gengin gilda. Til dæmis er hægt að færa inn dag-, mánaðar- eða ársfjórðungsgengi hvers erlends gjaldmiðils.

Hægt er að halda sögulegu gengi á síðunni **Gengi gjaldmiðila** til viðmiðunar. Þegar uppfæra þarf gengi er hægt að nota hnappinn **Uppfæra gengi** til að fá nýjasta gengi frá utanaðkomandi þjónustuaðila.

## <a name="general-ledger-accounts"></a>Fjárhagsreikningar

Ekki er hægt að tengja gjaldmiðilskóta við fjárhagsreikninga vegna þess að upphæðir í fjárhagsreikningum eru í SGM. Ef fyrirtækið er með lán í USD og setur innborgun á bankareikning í SEK er hægt að fylgjast með þessum reikningum með því að setja upp bankareikninga í USD og SEK. Með bókunarflokkum er hægt að tengja reikningana við viðeigandi fjárhagsreikninga. Í fjárhagnum eru upphæðirnar birtar í SGM.

Hægt er að færa gjaldmiðilskóta inn í færslubókarlínu og bóka línuna í fjárhagsreikning. Viðeigandi gengi er notað til að breyta upphæðinni í SGM áður en hún er bókuð í fjárhagsreikninginn.  

## <a name="example-of-a-receivable-currency-transaction"></a>Dæmi um móttekna gjaldmiðilsfærslu

[!INCLUDE [finance-currencies-example](includes/finance-currencies-example.md)]

## <a name="see-also"></a>Sjá einnig .

[Uppfæra gengi](finance-how-update-currencies.md)  
[Setja upp annan skýrslugjaldmiðil](finance-how-setup-additional-currencies.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
