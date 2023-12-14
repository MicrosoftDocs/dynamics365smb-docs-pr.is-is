---
title: Uppfæra gengi (inniheldur myndskeið)
description: Lærðu hvernig á að nota Business Central til að stilla gengi fyrir upphæðir í mismunandi gjaldmiðlum.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bnielse
ms.topic: conceptual
ms.search.keywords: 'multiple currencies, adjust exchange rates, FX rates'
ms.search.form: '5, 118'
ms.date: 11/13/2023
ms.custom: bap-template
---
# Uppfærðu gengi gjaldmiðla

Ef þú átt viðskipti með mismunandi gjaldmiðla þarftu að fylgjast með breytingum á gengi gjaldmiðla. [!INCLUDE [prod_short](includes/prod_short.md)] hjálpar þér að stjórna og uppfæra gengi handvirkt eða sjálfvirkt og setja upp gjaldeyrisþjónustu.

## Gjaldmiðlar

> [!TIP]  
> Í [!INCLUDE[prod_short](includes/prod_short.md)] er hægt að finna rauntímaupplýsingar um gjaldeyrisgengi (FX) eða söguleg gengi undir hugtakinu gjaldmiðill. Nánari upplýsingar er að finna í [Setja upp annan skýrslugjaldmiðil](finance-how-setup-additional-currencies.md).

[!INCLUDE [finance-currencies-def](includes/finance-currencies-def.md)]

Þú getur tilgreint gjaldmiðlakóðana í **Gjaldmiðlum** listanum, þar á meðal viðbótarupplýsingar og stillingar sem eru nauðsynlegar fyrir hvern gjaldmiðilskóða. Sjá [Gjaldmiðlar](finance-set-up-currencies.md#curr) fyrir frekari upplýsingar.

### Dæmi um móttekna gjaldmiðilsfærslu

[!INCLUDE [finance-currencies-example](includes/finance-currencies-example.md)]

## Gengi

Gengi eru verkfærin til að reikna gildi staðbundins gjaldmiðils (SGM) fyrir hverja gjaldmiðilsfærslu. Eftirfarandi reitir eru á síðunni **Gengi**:

|Svæði|Heimildasamstæða|  
|---------------------------------|---------------------------------------|  
|**Upphafsdagsetning**|Dagsetningin þegar gjaldmiðillinn tók gildi.|  
|**Gjaldmiðilskóði**|Gjaldmiðilskóðinn sem tengist þessu gengi.|  
|**Kóði viðmiðunargjaldmiðils**|Ef þessi gjaldmiðill er hluti af þríhyrningsútreikningi á gjaldmiðli geturðu sett upp tengdan gjaldmiðilskóða hér.|  
|**Gengisupphæð**|Gengisupphæð er gengi gjaldmiðilskóðans sem valinn er á línunni. Venjulega 1 eða 100.|  
|**Upphæð viðmiðunargengis**|Upphæð venslagengis tengist genginu sem á að nota fyrir tengigjaldmiðilskóðann.|  
|**Leiðrétting gengisupphæðar**|Gengi gjaldmiðilskóðans sem valinn er á línunni fyrir notkun  **Leiðrétta gengisgengi** lotuvinnunni.|  
|**Upph. leiðr. viðmiðunargengis**|Gengi gjaldmiðilskóðans sem valinn er á línunni fyrir notkun  **Leiðrétta gengisgengi** lotuvinnunni.|  
|**Festa gengisupphæð**|Tilgreinir hvort hægt sé að breyta gengi gjaldmiðils á reikningum og í bókarlínum.|  

Almennt eru gildi reitanna **Gengisupphæð** og **Upphæð viðmiðunargengis** notuð sem sjálfgefið gengi gjaldmiðils á öllum nýjum útistandandi kröfum og viðskiptaskuldum sem er stofnað til. Skjalið er úthlutað á gengi samkvæmt gildandi vinnudagsetningu.  

> [!Note]
> Raunverulegur gjaldmiðill er reiknaður út með þessari formúlu:
>
> `Currency Amount = Amount / Exchange Rate Amount * Relational Exch. Rate Amount`

Upphæð leiðréttingargengis, eða venslaleiðréttingargengisupphæð, uppfærir allar opnar banka-, kröfur eða skuldafærslur.  

> [!Note]
> Raunverulegur gjaldmiðill er reiknaður út með þessari formúlu:
>
> `Currency Amount = Amount / Adjustment Exch. Rate Amount * Relational Adjmt Exch. Rate Amt`

## Aðlaga gengi

Vegna þess að gengi breytist stöðugt þarftu að breyta öðrum gjaldmiðilsígildum reglulega. Ef þú gerir það ekki geta upphæðir sem þú umreiknaðir úr erlendum (eða öðrum) gjaldmiðlum og færðar í fjárhag í staðbundinni mynt verið rangar. Einnig þarftu að uppfæra daglegar færslur sem birtar eru áður en þú slærð inn daglegt gengi.

Þú getur notað **Leiðrétta gengisgengi** lotuvinnuna til að stilla gengi handvirkt fyrir bókaða viðskiptavina-, lánardrottins- og bankareikningsfærslur. Runuvinnslan getur einnig uppfært aðrar skýrslugjaldmiðilsupphæðir á bókhaldsfærslum.  

> [!TIP]
> Hægt er að nota þjónustu til að uppfæra gengi sjálfkrafa í kerfinu. Fyrir frekari upplýsingar, sjá [Til að setja upp gjaldeyrisþjónustu](finance-how-update-currencies.md#set-up-a-currency-exchange-rate-service). Hins vegar leiðréttir þetta ekki gengi á þegar bókuðum færslum. Til að uppfæra gengi á bókuðum færslum skaltu nota runuvinnsluna **Leiðrétta gengi**.

Þú getur líka tilgreint hvernig leiðréttingin meðhöndlar víddir fyrir óinnleysta hagnaðar- og tapbókanir með því að velja einn af eftirfarandi valkostum í reitnum **Víddarbókun** :  

* **Víddir upprunafærslu**: Flytja víddargildi fyrir bókhaldsfærslur fyrir óinnleysta hagnað og tap af færslunni sem þú ert að breyta.  
* **Engar víddir**: Ekki flytja víddargildi fyrir óinnleyst hagnað og tap yfir á bókhaldsfærslur. [!INCLUDE [prod_short](includes/prod_short.md)] notar samt sjálfgefna víddarstillingar, til dæmis **Code Obligator**, **Sama kóða** eða **Enginn kóða**. Ef upprunafærslufærslurnar hafa víddargildi, býr leiðréttingin til færslur án víddargilda.  
* **Fjárhagsreikningsvíddir**: Flytja víddargildi frá óinnleystum hagnaði og tapi upprunafærslu víddarstillinga fjárhagsreiknings yfir í bókhaldsfærslur.

> [!NOTE]
> Til að nota forskoðunarhæfileikann þarftu að kveikja á **eiginleikauppfærslu: Virkja notkun nýrrar stækkanlegrar gengisleiðréttingar, þar á meðal að birta endurskoðun** eiginleikann á **[Eiginleikastjórnun](https://businesscentral.dynamics.com/?page=2610)** síða.

> [!IMPORTANT]
> Vegna staðbundinna krafna í Sviss mælum við ekki með því að þú kveikir á **eiginleikauppfærslu: Virkjaðu notkun nýrrar stækkanlegrar gengisleiðréttingar, þar á meðal að birta umsögn** í svissneska (CH) landsútgáfa.

## Forskoðaðu áhrif aðlögunar

Þú getur forskoðað hvaða áhrif gengisleiðrétting hefur á færslu áður en þú birtir í raun með því að velja  **Forskoðunarfærsla** aðgerðina á **Exch. Verðleiðrétting** skýrsla (Skýrsla 596) beiðni síða. Á beiðnisíðunni geturðu tilgreint hvað á að hafa með í forskoðuninni:

* Fáðu nákvæma bókun í aðalbók með færslu.
* Fáðu yfirlitsfærslu eftir gjaldmiðli. Veldu bara reitinn **Aðlaga fyrir hverja færslu** reitinn á **Exch. Verðleiðrétting** skýrsla.

### Áhrif á viðskiptavini og söluaðila

Fyrir viðskiptamanna- og lánardrottinsreikninga notar runuvinnan gengi sem gilti á bókunardagsetningunni sem tilgreind var fyrir runuvinnsluna til að leiðrétta gjaldmiðilinn. Keyrslan reiknar mismuninn fyrir hverja gjaldmiðilsstöðu og bókar upphæðirnar á fjárhagslykilinn sem tilgreindur er í reitnum **Reikningur óinnleysts hagnaðar** eða í reitnum **Reikningur óinnleysts taps** á síðunni **Gjaldmiðlar**. Jöfnunarfærslurnar bókast sjálfkrafa á reikninginn útistandandi - gjaldfallið í fjárhag.

Keyrslan vinnur allar opnar viðskiptamanna- og lánardrottnafærslur. Ef það er gengismunur fyrir færslu, býr runuvinnan til nýja ítarlega viðskiptamanna- eða lánardrottinsfærslu. Nýja færslan endurspeglar leiðrétta upphæð á viðskiptamanna- eða lánardrottinsfærslu.

#### Víddir á viðskiptamanna- og lánardrottinsfærslum

[!INCLUDE [prod_short](includes/prod_short.md)] úthlutar víddum frá viðskiptamanna- eða lánardrottinsfærslum á leiðréttingarfærslurnar og bókar leiðréttingar fyrir hverja samsetningu víddargilda.

### Áhrif á bankareikninga

Keyrslan leiðréttir gjaldmiðilinn í bankareikningum með því að nota gengið sem gildir fyrir bókunardagsetninguna sem tilgreind er í keyrslunni. Keyrslan reiknar mismuninn fyrir hvern bankareikning sem er með gjaldmiðilskóða og bókar upphæðirnar á fjárhagslykilinn sem er tilgreindur í reitnum **Reikningur innleysts hagnaðar** eða í reitnum **Reikningur innleysts taps** á síðunni **Gjaldmiðlar**. Jöfnunarfærslurnar bókast sjálfkrafa á fjárhag bankareikninga sem eru tilgreindir í bókunarflokki bankareikninga. Keyrslan reiknar eina færslu á hvern gjaldmiðil í hverjum bókunarflokki.

#### Mál á bankareikningsfærslum

Leiðréttingarfærslum fyrir fjárhagsreikning bankareiknings og ávinnings-/tapreikningi er úthlutað sjálfgefnum víddum bankareikningsins.

### Áhrif á bókhaldsreikninga

Ef þú bókar í öðrum skýrslugjaldmiðli getur runuvinnan búið til nýjar fjárhagsfærslur fyrir gjaldmiðlaleiðréttingar milli staðbundinnar gjaldmiðils og hins skýrslugjaldmiðilsins. Runuvinnan reiknar út mismuninn fyrir hverja fjárhagsfærslu. Það aðlagar aðalbókarfærsluna eftir innihaldi **Gengisleiðrétting**  reit fyrir hvern fjárhagsreikning.

#### Stærðir á færslum á reikningsfærslum

Leiðréttingarfærslunum er úthlutað sjálfgefnum víddum frá reikningunum sem þær eru bókaðar á.

> [!Important]
> Áður en hægt er að nota runuvinnuna þarf að slá inn leiðréttingargengi sem eru notuð til að leiðrétta gjaldeyrisjöfnuðina. Þetta er gert á síðunni **Gengi gjaldmiðla**.<br><br>  

> [!Video https://www.microsoft.com/videoplayer/embed/RE3Q24s?rel=0]

## Settu upp gjaldeyrisþjónustu

Þú getur notað ytri þjónustu til að halda gjaldeyrisviðskiptum þínum uppfærðum, t.d. FloatRates. 

> [!NOTE]
> Flestar gengisþjónustur veita gögn sem samrýmast innflutningsferlinu í [!INCLUDE[prod_short](includes/prod_short.md)]. Hins vegar eru gögnin stundum öðruvísi sniðin og þú þarft að sérsníða innflutningsferlið. Hægt er að nota gagnaskiptarammann til að gera það með því að bæta við eigin kóðaeiningu. Þú þarft líklega aðstoð frá þróunaraðila til að gera þetta. Frekari upplýsingar er að finna í [Setja upp skilgreiningar gagnaskipta](across-how-to-set-up-data-exchange-definitions.md).

1. Veldu ![peruna sem opnar Segðu mér eiginleikann.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Tákn, slá inn **Gjaldeyrisþjónusta**, og veldu síðan tengda hlekkinn.
2. Veldu **Nýtt**  aðgerð.
3. Fylltu í reitina eftir því sem nauðsyn krefur á síðunni **Þjónusta fyrir gengi gjaldmiðils**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Kveiktu á **Virkjað** víxlhnappinum til að virkja þjónustuna.

> [!NOTE]
> Eftirfarandi myndband sýnir hvernig þú getur tengst gjaldeyrisþjónustu, með Seðlabanka Evrópu sem dæmi. Í hlutanum sem lýsir því hvernig á að setja upp svæðisvörp, er stillingin í **Heimild**  dálk fyrir **Foreldrahnútur fyrir gjaldmiðilskóða**   skilar aðeins fyrsta gjaldmiðlinum sem fannst. Stillingin á að vera `/gesmes:Envelope/Code/Code/Code`.

<br><br>  
  
> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4A1jy?rel=0]

## Uppfærðu gengi gjaldmiðla í gegnum þjónustu

Fylgdu skrefunum sem gefin eru til að uppfæra gengi gjaldmiðla í gegnum þjónustu:

1. Veldu ![peru sem opnar Segðu mér eiginleikann.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Tákn, slá inn **Gjaldmiðlar**, og veldu síðan tengda hlekkinn.
2. Veldu **Uppfærðu gengi**  aðgerð.

## Leiðrétta mistök

Öðru hvoru gæti þurft að leiðrétta mistök í greiðsluviðskiptum sem tengjast leiðréttingum á gjaldeyrishagnaði og -tapi. Þú getur notað aðgerðina **Andstæða færslu**  á **Færslur banka**, **viðskiptabók. Færslur** og **færslur lánardrottna**  til að ógilda og bakfæra greiðslufærsluna.

> [!NOTE]
> Þegar þú afturkallar og bakfærir greiðslu fyrir færslu sem hafði gengisbreytingar tengdar við sig, bókar bakfærslan bakfærslufærslur fyrir leiðréttingarnar. Þú gætir þurft að keyra gengisbreytinguna aftur til að fá rétta núverandi stöðu.

## Sjá einnig

## Sjá einnig .

[Gjaldmiðlar í Business Central](finance-currencies.md)  
[Uppsetning gjaldmiðla](finance-set-up-currencies.md)  
[Setja upp annan skýrslugjaldmiðil](finance-how-setup-additional-currencies.md)  
[Lokaár og Tímabil](year-close-years-periods.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
