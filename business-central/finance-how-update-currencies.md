---
title: Uppfæra gengi (inniheldur myndskeið)
description: Ef upphæðir í mismunandi gjaldmiðlum eru lagfærðar er hægt að láta Aðalmiðlageringar Leiðrétta gengi þeirra.
author: brentholtorf
ms.topic: conceptual
ms.search.keywords: 'multiple currencies, adjust exchange rates, FX rates'
ms.search.form: '5, 118'
ms.date: 09/07/2023
ms.author: bholtorf
---
# <a name="update-currency-exchange-rates"></a>Uppfæra gengi

Hægt er að skilgreina mismunandi gjaldmiðla í  [!INCLUDE [prod_short](includes/prod_short.md)], til dæmis ef þú átt viðskipti í gjaldmiðlum öðrum en gjaldmiðli landsins. Til að rekja breytingar á gengi gjaldmiðla er hægt að stjórna genginu handvirkt eða setja upp gjaldmiðilsgengisþjónustu.

## <a name="currencies"></a>Gjaldmiðlar

> [!TIP]  
>  [!INCLUDE[prod_short](includes/prod_short.md)] Ef þú ert að leita að rauntímaupplýsingum um gengi í erlendum skiptum (FX) eða sögulegum hlutföllum, finnur þú það nefnt Gjaldmiðill. Auk þessarar greinar geturðu skoðað [Setja upp annan skýrslugjaldmiðil](finance-how-setup-additional-currencies.md).

[!INCLUDE [finance-currencies-def](includes/finance-currencies-def.md)]

Gjaldmiðilskóðarnir eru tilgreindir í listanum **Gjaldmiðlar**, þ.m.t. viðbótarupplýsingar og stillingar sem eru nauðsynlegar fyrir hvern gjaldmiðilskóða. Sjá [Gjaldmiðlar](finance-set-up-currencies.md#curr) fyrir frekari upplýsingar.

### <a name="example-of-a-receivable-currency-transaction"></a>Dæmi um móttekna gjaldmiðilsfærslu

[!INCLUDE [finance-currencies-example](includes/finance-currencies-example.md)]

## <a name="exchange-rates"></a>Gengi

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

Upphæð leiðréttingargengis eða gengisleiðréttingarfjárhæð, uppfæra allar opnar banka, útistandandi eða gjaldfallnar færslur.  

> [!Note]
> Raunverulegt gjaldmiðilsgengi verður reiknað með þessari formúlu:
>
> `Currency Amount = Amount / Adjustment Exch. Rate Amount * Relational Adjmt Exch. Rate Amt`

## <a name="adjusting-exchange-rates"></a>Leiðrétta gengi

Þar sem gengi sveiflast stöðugt þarf að aðlaga annan gjaldmiðil ígildi með reglubundnum hætti. Ef það er ekki, upphæðir sem umbreytt var úr erlendum (eða öðrum) gjaldmiðlum og bókaðar í fjárhag í staðbundnum gjaldmiðli geta verið rangar. Einnig þarf að uppfæra Daglegar færslur sem bókaðar eru áður en gengi er fært inn.

 **Keyrslan Leiðrétta gengi**  er notuð til að leiðrétta handvirkt gengi fyrir bókaða viðskiptamanna-, lánardrottna-og bankareikningsfærslur. Einnig er hægt að uppfæra aðrar upphæðir skýrslugjaldmiðli í fjárhagsfærslum í keyrslunni.  

> [!TIP]
> Hægt er að nota þjónustu til að uppfæra gengi sjálfkrafa í kerfinu. Frekari upplýsingar er að finna í [Að setja upp þjónustu um gengi gjaldmiðils](finance-how-update-currencies.md#to-set-up-a-currency-exchange-rate-service). Þetta leiðréttir hins vegar ekki gengi í þegar bókuðum færslum. Til að uppfæra gengi á bókuðum færslum skaltu nota runuvinnsluna **Leiðrétta gengi**.

Einnig er hægt að tilgreina hvernig leiðréttingin mun meðhöndla víddir fyrir bókanir áætlaðs hagnaðar og taps með því að velja einn af eftirfarandi valkostum í  **reitnum víddarbókun** :  

* **Færsluvíddir** uppruna: flytja víddargildi fyrir fjárhagsfærslur fyrir áætlaðan hagnað og tap úr færslunni sem verið er að leiðrétta.  
* **Engar víddir** : ekki flytja víddargildi fyrir Óinnleystur hagnað og tap í fjárhagsfærslur. [!INCLUDE [prod_short](includes/prod_short.md)] notar samt sjálfgefna víddarstillingar, til dæmis  **Kóðáskilið**,  **sama kóta** eða  **engan kóða**. Ef upprunafærslurnar eru með víddargildi stofnar leiðréttingin án víddargilda.  
* **Víddir** fjárhagsreiknings: flytja víddargildi úr reitnum Áætlaður hagnaður og tap víddarstillinga fyrir grunnstillingu fjárhagsreikningsins í fjárhagsfærslum áætlaðs hagnaðar.

> [!NOTE]
> Ef nota á forskoðunargetu verður að kveikja á  **eiginleikann uppfæra: virkja notkun á nýju extensible gengisleiðréttingu, þar með talið bókun**  á aðgerðum á  **[Feature Management](https://businesscentral.dynamics.com/?page=2610)** .

> [!IMPORTANT]
> Vegna staðbundinna þarfa í Sviss mælum við ekki með því að virkja  **Uppfærsluuppfærslu: virkja notkun á nýju extensible gengisleiðréttingu, með bókunarendurskoðun**  í landsútgáfunni (CH).

## <a name="preview-the-effect-of-an-adjustment"></a>Forskoða áhrif leiðréttingar

Hægt er að forskoða áhrifin sem gengisleiðrétting verður með við bókun áður en bókað er í raun með því að  **Velja aðgerðina forskoða bókun**  í  **leiðréttingarskýrslu gengisleiðréttingarinnar**  (Report 596). Á beiðssíðu er hægt að tilgreina hvað á að hafa með í forskoðun:

* Fá nákvæma bókun á fjárhag eftir færslu
* Fá samandregna bókun eftir gjaldmiðli. Aðeins skal velja  **reitinn leiðrétta hverja færslu**  í  **leiðréttingarskýrslu gengisleiðréttingar** .

### <a name="effect-on-customers-and-vendors"></a>Áhrif á viðskiptavini og lánardrottna

Keyrslan notar það gengi sem var í gildi á bókunardagsetningunni sem tilgreind er fyrir keyrsluna til að leiðrétta gjaldmiðilinn fyrir viðskiptamanna-og lánardrottnareikninga. Keyrslan reiknar mismuninn fyrir hverja gjaldmiðilsstöðu og bókar upphæðirnar á fjárhagslykilinn sem tilgreindur er í reitnum **Reikningur óinnleysts hagnaðar** eða í reitnum **Reikningur óinnleysts taps** á síðunni **Gjaldmiðlar**. Jöfnunarfærslurnar bókast sjálfkrafa á reikninginn útistandandi - gjaldfallið í fjárhag.

Keyrslan vinnur allar opnar viðskiptamanna- og lánardrottnafærslur. Ef gengismunur er fyrir færslu stofnar keyrslan nýja nákvæma viðskiptamanna-eða lánardrottnafærslu. Nýja færslan endurspeglar Leiðrétta upphæð í viðskiptamanns-eða lánardrottnafærslu.

#### <a name="dimensions-on-customer-and-vendor-ledger-entries"></a>Víddir í viðskiptamanna-og lánardrottnafærslum

[!INCLUDE [prod_short](includes/prod_short.md)] úthlutar víddunum frá viðskiptamanna-eða lánardrottnafærslum til leiðréttingarfærslna og bókar leiðréttingar fyrir hverja samsetningu víddargilda.

### <a name="effect-on-bank-accounts"></a>Áhrif á bankareikninga

Keyrslan leiðréttir gjaldmiðilinn í bankareikningum með því að nota gengið sem gildir fyrir bókunardagsetninguna sem tilgreind er í keyrslunni. Keyrslan reiknar mismuninn fyrir hvern bankareikning sem er með gjaldmiðilskóða og bókar upphæðirnar á fjárhagslykilinn sem er tilgreindur í reitnum **Reikningur innleysts hagnaðar** eða í reitnum **Reikningur innleysts taps** á síðunni **Gjaldmiðlar**. Jöfnunarfærslurnar bókast sjálfkrafa á fjárhag bankareikninga sem eru tilgreindir í bókunarflokki bankareikninga. Keyrslan reiknar eina færslu á hvern gjaldmiðil í hverjum bókunarflokki.

#### <a name="dimensions-on-bank-account-entries"></a>Víddir í bankareikningsfærslur

Leiðréttingarfærslum vegna fjárhagsreiknings bankareikningsins og vegna hagnaðar-/tapreiknings er úthlutað sjálfgefnum víddum bankareikningsins.

### <a name="effect-on-gl-accounts"></a>Áhrif á fjárhagsreikninga

Ef bókað er í öðrum skýrslugjaldmiðli getur keyrslan stofnað nýjar fjárhagsfærslur fyrir gengisleiðréttingar á milli staðbundinna gjaldmiðla og hins skýrslugjaldmiðli. Keyrslan reiknar mismuninn miðað við hverja einstaka fjárhagsfærslu og leiðréttir fjárhagsfærsluna með tilliti til innihaldi reitsins **Gengisleiðrétting** fyrir hvern fjárhagslykil.

#### <a name="dimensions-on-gl-account-entries"></a>Víddir í fjárhagsreikningsfærslum

Leiðréttingarfærslunum er úthlutað sjálfgefnu víddunum í reikningunum sem þær eru bókaðar á.

> [!Important]
> Áður en hægt er að nota keyrsluna verður að færa inn gengið sem á að nota til þess að leiðrétta gengismun gjaldeyrisins. Þetta er gert á síðunni **Gengi gjaldmiðla**.<br><br>  

> [!Video https://www.microsoft.com/videoplayer/embed/RE3Q24s?rel=0]

## <a name="to-set-up-a-currency-exchange-rate-service"></a>Setja upp þjónustu um gengi gjaldmiðils

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

## <a name="to-update-currency-exchange-rates-through-a-service"></a>Til að uppfæra gengi í gegnum þjónustu

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Gjaldmiðlar** og velja síðan viðkomandi tengil.
2. Veldu aðgerðina **Uppfæra gengi**.

Gildið í **Gengi** reitnum á síðunni **Gjaldmiðlar** er uppfært með nýjustu gengi gjaldmiðilsins.

## <a name="correct-mistakes"></a>Leiðrétta mistök

Hvert sem er og þá gæti þurft að leiðrétta mistök í greiðslufærslu sem tengist leiðréttingum á hagnaði og tapi á erlendum gjaldmiðli. Hægt er að nota  **aðgerðina**  Bakfæra færslu  **í bankafærslum**,  **viðskiptamannafærslum** og  **lánardrottnafærslum**  til að ógilda jöfnun og bakfæra greiðslufærsluna.

> [!NOTE]
> Þegar jöfnun er aftengd og bakfæra greiðslu fyrir færslu sem hafði gengisleiðréttingar tengdar gengi er bakfærslan innlegg Bakfærð færsla fyrir leiðréttingarnar. Það gæti þurft að keyra gengisleiðréttinguna aftur til að fá rétta núverandi stöðu.

## <a name="see-also"></a>Sjá einnig

[Gjaldmiðlar í Business Central](finance-currencies.md)  
[Uppsetning gjaldmiðla](finance-set-up-currencies.md)  
[Setja upp annan skýrslugjaldmiðil](finance-how-setup-additional-currencies.md)  
[Lokaár og Tímabil](year-close-years-periods.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
