---
title: Uppfæra gengi (inniheldur myndskeið)
description: Ef fylgst er með upphæðum í mismunandi gjaldmiðlum er hægt að leyfa Business Central að hjálpa þér að stilla gengi erlendra gjaldmiðla fyrir bókaðar færslur með utanaðkomandi þjónustu.
author: edupont04
ms.topic: conceptual
ms.search.keywords: 'multiple currencies, adjust exchange rates, FX rates'
ms.search.form: '5, 118'
ms.date: 03/15/2022
ms.author: edupont
---
# Uppfæra gengi

Hægt er að skilgreina mismunandi gjaldmiðla í [!INCLUDE [prod_short](includes/prod_short.md)], t.d. ef þú stundar viðskipti í öðrum gjaldmiðlum en staðbundnum gjaldmiðli. Síðan, til að hjálpa þér að fylgjast með breytingum á gengi gjaldmiðla, getur þú stjórnað gjaldmiðlunum handvirkt eða sett upp gjaldmiðlaþjónustu.

## Gjaldmiðlar

> [!TIP]  
> Í [!INCLUDE[prod_short](includes/prod_short.md)], ef þú ert að leita að nýjustu upplýsingum um gengi erlendra gjaldmiðla eða eldri gengi, finnur þú það undir gjaldmiðli. Auk þessarar greinar geturðu skoðað [Setja upp annan skýrslugjaldmiðil](finance-how-setup-additional-currencies.md).

[!INCLUDE [finance-currencies-def](includes/finance-currencies-def.md)]

Gjaldmiðilskóðarnir eru tilgreindir í listanum **Gjaldmiðlar**, þ.m.t. viðbótarupplýsingar og stillingar sem eru nauðsynlegar fyrir hvern gjaldmiðilskóða. Sjá [Gjaldmiðlar](finance-set-up-currencies.md#curr) fyrir frekari upplýsingar.

### Dæmi um móttekna gjaldmiðilsfærslu

[!INCLUDE [finance-currencies-example](includes/finance-currencies-example.md)]

## Gengi

Gengi eru verkfærin til að reikna gildi staðbundins gjaldmiðils (SGM) fyrir hverja gjaldmiðilsfærslu. Eftirfarandi reitir eru á síðunni **Gengi**:

|Svæði|Description|  
|---------------------------------|---------------------------------------|  
|**Upphafsögn**|Dagsetningin þegar gengið var tekið í notkun|  
|**Gjaldmiðilskóði**|Gjaldmiðilskóðinn sem tengist genginu|  
|**Kóði viðmiðunargjaldmiðils**|Ef þessi gjaldmiðill er hluti af þríhyrndum gjaldmiðlaútreikningi er hægt að setja upp tengdan gjaldmiðilskóða hér|  
|**Gengisupphæð**|Gengisupphæðin er það gengi sem á að nota fyrir gjaldmiðilskóðann sem er valinn á línunni. Venjulega 1 eða 100|  
|**Upphæð viðmiðunargengis**|Upphæð viðmiðunargengis tengist því gengi sem er notað fyrir kóða viðmiðunargjaldmiðilsins|  
|**Leiðrétting gengisupphæðar**|Leiðrétting gengisupphæðar er gengið sem á að nota fyrir gjaldmiðilskóðann sem er valinn á línunni til að nota runuvinnsluna **Gengi leiðrétt**|  
|**Upph. leiðr. viðmiðunargengis**|Hlutfallsleg leiðrétting gengis er gengið sem á að nota fyrir gjaldmiðilskóðann sem er valinn á línunni til að nota runuvinnsluna **Gengi leiðrétt**|  
|**Festa gengisupphæð**|Tilgreinir hvort hægt sé að breyta gengi gjaldmiðils á reikningum og í bókarlínum.|  

Almennt eru gildi reitanna **Gengisupphæð** og **Upphæð viðmiðunargengis** notuð sem sjálfgefið gengi gjaldmiðils á öllum nýjum útistandandi kröfum og viðskiptaskuldum sem er stofnað til. Skjalið er úthlutað á gengi samkvæmt gildandi vinnudagsetningu.  

> [!Note]
> Raunverulegt gjaldmiðilsgengi verður reiknað með þessari formúlu:
>
> `Currency Amount = Amount / Exchange Rate Amount * Relational Exch. Rate Amount`

Upphæð gengisleiðréttingarinnar eða upphæð viðmiðunar gengisleiðréttingari verður notuð til að uppfæra allar opnar færslur í bankanum, kröfur eða greiðslur.  

> [!Note]
> Raunverulegt gjaldmiðilsgengi verður reiknað með þessari formúlu:
>
> `Currency Amount = Amount / Adjustment Exch. Rate Amount * Relational Adjmt Exch. Rate Amt`

## Gengi leiðrétt

Vegna þess hve tíðar gengisbreytingar eru verður reglubundið að leiðrétta aðra jafngildisgjaldmiðla í kerfinu. Sé það ekki gert verða upphæðir misvísandi sem hafa verið umreiknaðar úr erlendum (eða aukalegum) gjaldmiðlum og bókaðar í fjárhag í SGM. Að auki verður að uppfæra daglegar færslur sem eru bókaðar áður en daglegt gengi er fært inn eftir að upplýsingarnar um daglegt gengi hafa verið færðar inn.

Runuvinnslan **Leiðrétta gengi** er notuð til að lagfæra handvirkt gengi bókaðs viðskiptamanns, lánardrottins og bankareikningsfærslna. Hún getur einnig uppfært upphæðir annars skýrslugjaldmiðils í fjárhagsfærslum.  

> [!TIP]
> Hægt er að nota þjónustu til að uppfæra gengi sjálfkrafa í kerfinu. Frekari upplýsingar er að finna í [Að setja upp þjónustu um gengi gjaldmiðils](finance-how-update-currencies.md#to-set-up-a-currency-exchange-rate-service). Þetta leiðréttir hins vegar ekki gengi í þegar bókuðum færslum. Til að uppfæra gengi á bókuðum færslum skaltu nota runuvinnsluna **Leiðrétta gengi**.

Hægt er að forskoða hvaða áhrif leiðrétting hefur á bókun áður en þú bókar í alvöru með því að velja **Forskoða** á síðunni **Leiðrétta gengi**. Auk þess er hægt að velja hvort almennar fjárhagsbókanir verið ítarlegar (á hverja færslu) eða teknar saman (á hvern gjaldmiðil) með því að velja **Taka saman færslur**. Einnig er hægt að tilgreina hvernig á að meðhöndla víddir fyrir bókanir á óinnleystum hagnaði og tapi með því að velja einn af eftirfarandi valkostum í reitnum **Flytja víddargildi**:  

- **Upprunafærsla**: Fjárhagsfærslur fyrir óinnleystan hagnað og tap mun láta flytja víddargildi úr leiðréttu færslunni.
- **Eftir fjárhagsreikningi**: Fjárhagsfærslur fyrir óinnleystan hagnað og tap mun láta flytja gildi úr upprunafærslu víddarstillinga fyrir fjárhagsreikning óinnleysts hagnaðar og taps.
- **Engin millifærsla**: Fjárhagsfærslur fyrir óinnleystan hagnað og tap verða ekki með víddargildi.

### Áhrif á viðskiptamenn og lánardrottna

Keyrslan leiðréttir gjaldmiðilinn í reikningum viðskiptamanna og lánardrottna með því að nota gengið sem gildir fyrir bókunardagsetninguna sem tilgreind er í keyrslunni. Keyrslan reiknar mismuninn fyrir hverja gjaldmiðilsstöðu og bókar upphæðirnar á fjárhagslykilinn sem tilgreindur er í reitnum **Reikningur óinnleysts hagnaðar** eða í reitnum **Reikningur óinnleysts taps** á síðunni **Gjaldmiðlar**. Jöfnunarfærslurnar bókast sjálfkrafa á reikninginn útistandandi - gjaldfallið í fjárhag.

Keyrslan vinnur allar opnar viðskiptamanna- og lánardrottnafærslur. Ef gengismunur er á færslu stofnar runuvinnslan nýja sundurliðaða viðskiptavina- eða lánardrottnafærslu sem endurspeglar leiðréttu upphæðina í viðskiptavina- eða lánardrottnafærslunni.

#### Víddir í fjárhagsfærslum viðskiptavina og lánardrottna

Leiðréttingarfærslum er úthlutað víddum úr viðskiptavina-/lánardrottnafærslum og leiðréttingar eru bókaðar eftir samsetningum á víddagildum.

### Áhrif á bankareikninga

Keyrslan leiðréttir gjaldmiðilinn í bankareikningum með því að nota gengið sem gildir fyrir bókunardagsetninguna sem tilgreind er í keyrslunni. Keyrslan reiknar mismuninn fyrir hvern bankareikning sem er með gjaldmiðilskóða og bókar upphæðirnar á fjárhagslykilinn sem er tilgreindur í reitnum **Reikningur innleysts hagnaðar** eða í reitnum **Reikningur innleysts taps** á síðunni **Gjaldmiðlar**. Jöfnunarfærslurnar bókast sjálfkrafa á fjárhag bankareikninga sem eru tilgreindir í bókunarflokki bankareikninga. Keyrslan reiknar eina færslu á hvern gjaldmiðil í hverjum bókunarflokki.

#### Víddir í bankareikningsfærslum

Leiðréttingarfærslum vegna fjárhagsreiknings bankareikningsins og vegna hagnaðar-/tapreiknings er úthlutað sjálfgefnum víddum bankareikningsins.

### Áhrif á fjárhagsreikninga
Ef bókað er í öðrum skýrslugjaldmiðli er hægt að láta keyrsluna búa til nýjar fjárhagsfærslur fyrir gjaldmiðilsmismun á SGM og öðrum skýrslugjaldmiðli. Keyrslan reiknar mismuninn miðað við hverja einstaka fjárhagsfærslu og leiðréttir fjárhagsfærsluna með tilliti til innihaldi reitsins **Gengisleiðrétting** fyrir hvern fjárhagslykil.

##### Víddir í fjárhagsreikningsfærslum
Leiðréttingarfærslunum er úthlutað sjálfgefnu víddunum í reikningunum sem þær eru bókaðar á.

> [!Important]
> Áður en hægt er að nota keyrsluna verður að færa inn gengið sem á að nota til þess að leiðrétta gengismun gjaldeyrisins. Þetta er gert á síðunni **Gengi gjaldmiðla**.<br><br>  

> [!Video https://www.microsoft.com/videoplayer/embed/RE3Q24s?rel=0]

## Setja upp þjónustu um gengi gjaldmiðils
Þú getur notað ytri þjónustu til að halda gjaldeyrisviðskiptum þínum uppfærðum, t.d. FloatRates. 

> [!NOTE]
> Flestar gengisþjónustur veita gögn sem samrýmast innflutningsferlinu í [!INCLUDE[prod_short](includes/prod_short.md)]. Stundum eru gögnin þó sniðin á annan hátt og þú þarft að sérsníða innflutningsferlið. Hægt er að nota gagnaskiptarammann til að gera það með því að bæta við eigin kóðaeiningu. Þú þarft líklega aðstoð frá þróunaraðila til að gera þetta. Frekari upplýsingar er að finna í [Setja upp skilgreiningar gagnaskipta](across-how-to-set-up-data-exchange-definitions.md).

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Þjónusta um gengi gjaldmiðils** og velja síðan viðkomandi tengil.
2. Valið er **Nýtt** aðgerð.
3. Fylltu í reitina eftir því sem nauðsyn krefur á síðunni **Þjónusta fyrir gengi gjaldmiðils**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Kveiktu á **Virkjað** víxlhnappinum til að virkja þjónustuna.

> [!NOTE]
> Eftirfarandi myndskeið sýnir dæmi um það hvernig á að tengjast við gjaldeyrisþjónustu þar sem evrópski seðlabankinn er notaður sem dæmi. Í hlutanum er því lýst hvernig setja á upp reitaravarpanir. Stillingin í dálknum **Uppruni** fyrir **Yfirhnútur fyrir gjaldmiðilskóða** skilar aðeins fyrsta gjaldmiðlinum sem fannst. Stillingin á að vera `/gesmes:Envelope/Code/Code/Code`.

<br><br>  
  
> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4A1jy?rel=0]

## Til að uppfæra gengi í gegnum þjónustu
1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Gjaldmiðlar** og velja síðan viðkomandi tengil.
2. Veldu aðgerðina **Uppfæra gengi**.

Gildið í **Gengi** reitnum á síðunni **Gjaldmiðlar** er uppfært með nýjustu gengi gjaldmiðilsins.

## Sjá tengda [Microsoft þjálfun](/training/paths/use-multiple-currencies-dynamics-365-business-central/)

## Sjá einnig

[Gjaldmiðlar í Business Central](finance-currencies.md)  
[Uppsetning gjaldmiðla](finance-set-up-currencies.md)  
[Setja upp annan skýrslugjaldmiðil](finance-how-setup-additional-currencies.md)  
[Lokaár og Tímabil](year-close-years-periods.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
