---
title: Uppfæra gengi gjaldmiðla
description: Læra að nota Business Central til að leiðrétta gengi upphæða í mismunandi gjaldmiðlum.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'multiple currencies, adjust exchange rates, FX rates'
ms.search.form: '5, 118'
ms.date: 05/03/2024
ms.custom: bap-template
ms.service: dynamics-365-business-central
---
# Uppfæra gengi gjaldmiðla

Ef viðskipti eru í mismunandi gjaldmiðlum þarf að fylgjast með breytingum á gengi gjaldmiðla. [!INCLUDE [prod_short](includes/prod_short.md)] hjálpar til við að stjórna og uppfæra gengi handvirkt eða sjálfvirkt og setja upp gengisþjónustu fyrir gjaldmiðil.

## Gjaldmiðlar

> [!TIP]  
> Þar [!INCLUDE[prod_short](includes/prod_short.md)] má finna rauntímaupplýsingar um gengi erlends gengis (FX) eða sögulegt gengi í gjaldmiðli hugtaksins. Nánari upplýsingar er að finna í [Setja upp annan skýrslugjaldmiðil](finance-how-setup-additional-currencies.md).

[!INCLUDE [finance-currencies-def](includes/finance-currencies-def.md)]

Hægt er að tilgreina gjaldmiðilskótana á listanum **Gjaldmiðlar**, þar á meðal viðbótarupplýsingar og stillingar sem eru nauðsynlegar fyrir hvern gjaldmiðilskóta. Sjá [Gjaldmiðlar](finance-set-up-currencies.md#curr) fyrir frekari upplýsingar.

### Dæmi um móttekna gjaldmiðilsfærslu

[!INCLUDE [finance-currencies-example](includes/finance-currencies-example.md)]

## Gengi

Gengi eru verkfærin til að reikna gildi staðbundins gjaldmiðils (SGM) fyrir hverja gjaldmiðilsfærslu. Eftirfarandi reitir eru á síðunni **Gengi**:

|Svæði|Heimildasamstæða|  
|---------------------------------|---------------------------------------|  
|**Upphafsdagsetning**|Dagsetningin þegar gengið var virkt.|  
|**Gjaldmiðilskóði**|Gjaldmiðilskótinn sem tengist þessu gengi.|  
|**Kóði viðmiðunargjaldmiðils**|Ef þessi gjaldmiðill er hluti af útreikningi á þríhyrningsgjaldmiðli er hægt að setja upp viðeigandi gjaldmiðilskóta hér.|  
|**Gengisupphæð**|Gengisupphæðin er gengi gjaldmiðilskóta sem valinn er í línunni. Venjulega 1 eða 100.|  
|**Upphæð viðmiðunargengis**|Viðmiðunargengisupphæðin tengist genginu sem á að nota fyrir kóta viðmiðunargjaldmiðilsins.|  
|**Leiðrétting gengisupphæðar**|Gengi gjaldmiðilskótans sem valinn var á línunni fyrir keyrsluna **Leiðrétta gengi** .|  
|**Upph. leiðr. viðmiðunargengis**|Gengi gjaldmiðilskótans sem valinn var á línunni fyrir keyrsluna **Leiðrétta gengi** .|  
|**Festa gengisupphæð**|Tilgreinir hvort hægt sé að breyta gengi gjaldmiðils á reikningum og í bókarlínum.|  

Almennt eru gildi reitanna **Gengisupphæð** og **Upphæð viðmiðunargengis** notuð sem sjálfgefið gengi gjaldmiðils á öllum nýjum útistandandi kröfum og viðskiptaskuldum sem er stofnað til. Skjalið er úthlutað á gengi samkvæmt gildandi vinnudagsetningu.  

> [!Note]
> Gengi raunverulegs gjaldmiðils er reiknað með þessari reiknireglu:
>
> `Currency Amount = Amount / Exchange Rate Amount * Relational Exch. Rate Amount`

Leiðréttingargengisupphæðin eða upphæð viðmiðunargengis, uppfærir allar færslur í opnum banka, útistandandi eða gjaldföllnu.  

> [!Note]
> Gengi raunverulegs gjaldmiðils er reiknað með þessari reiknireglu:
>
> `Currency Amount = Amount / Adjustment Exch. Rate Amount * Relational Adjmt Exch. Rate Amt`

## Leiðrétta gengi

Vegna þess að gengi sveiflast stöðugt þarf að leiðrétta jafngildi annarra gjaldmiðla reglubundið. Ef það er ekki gert geta upphæðir sem umreiknaðar voru úr erlendum (eða öðrum) gjaldmiðlum og bókaðar í fjárhag í staðbundnum gjaldmiðli verið rangar. Einnig þarf að uppfæra daglegar færslur sem bókaðar eru áður en daglegt gengi er fært inn.

Hægt er að nota keyrsluna **Leiðrétta gengi** til að leiðrétta handvirkt gengi bókaðra viðskiptamanna-, lánardrottna- og bankareikningsfærslna. Keyrslan getur einnig uppfært aðrar upphæðir skýrslugjaldmiðils í fjárhagsfærslum.  

> [!TIP]
> Hægt er að nota þjónustu til að uppfæra gengi sjálfkrafa í kerfinu. Nánari upplýsingar eru [í Til að setja upp gengisþjónustu](finance-how-update-currencies.md#set-up-a-currency-exchange-rate-service) fyrir gjaldmiðla. Þetta leiðréttir hins vegar ekki gengi í færslum sem þegar hafa verið bókaðar. Til að uppfæra gengi á bókuðum færslum skaltu nota runuvinnsluna **Leiðrétta gengi**.

Einnig er hægt að tilgreina hvernig leiðréttingin meðhöndli víddir fyrir bókaðan áætlaðan hagnað og tap með því að velja einn af eftirfarandi valkostum í reitnum **Víddarbókun** :  

* **Upprunafærsluvíddir**: Flytja víddargildi fyrir fjárhagsfærslur fyrir áætlaðan hagnað og tap úr færslunni sem verið er að leiðrétta.  
* **Engar víddir**: Ekki flytja víddargildi fyrir áætlaðan hagnað og tap í fjárhagsfærslur. [!INCLUDE [prod_short](includes/prod_short.md)] notar enn sjálfgefnar víddarstillingar, til dæmis **Kóta áskilinn**, **Sama kóta** eða **Enginn kóti**. Ef upprunaviðskiptafærslurnar hafa víddargildi stofnar leiðréttingin færslur án víddargilda.  
* **Fjárhagsreikningsvíddir**: Flytja víddargildi úr áætluðum hagnaði og tapi á víddarstillingum fjárhagsreiknings í fjárhagsfærslur.

> [!NOTE]
> Til að nota forskoðunarmöguleikann þarf að kveikja á **eiginleikauppfærslunni: Gera notkun á nýrri víðtækri gengisleiðréttingu virka, þ.m.t. bókunarumsagnaaðgerð** á síðunni **[Aðgerðastjórnun](https://businesscentral.dynamics.com/?page=2610)** .

> [!IMPORTANT]
> Vegna staðbundinna krafna í Sviss er ekki mælt með því að þú gerir eiginleikauppfærslu virka **: Virkja notkun á nýrri víðtækri gengisleiðréttingu, þ.m.t. bókun endurskoðunar** í svissneska (CH) landsútgáfunni.

## Skoða áhrif leiðréttingar

Hægt er að forskoða áhrifin sem gengisleiðrétting hefur við bókun áður en bókað er í raun með því að **velja beiðnisíðuna Forskoðunarbókun** á **beiðnisíðunni Gengisleiðrétting** (Skýrsla 596). Á beiðnisíðunni er hægt að tilgreina hvað á að vera með í forskoðuninni:

* Fá nákvæma bókun í fjárhag með færslu.
* Fá samantekna bókun eftir gjaldmiðli. Tínt er í reitinn **Leiðrétta eftir færslu** í skýrslunni **Gengisleiðrétting** .

### Áhrif á viðskiptamenn og lánardrottna

Keyrslan notar gengið sem var í gildi á bókunardagsetningunni sem tilgreind er fyrir keyrsluna til að leiðrétta gjaldmiðilinn fyrir reikninga viðskiptamanna og lánardrottna. Keyrslan reiknar mismuninn fyrir hverja gjaldmiðilsstöðu og bókar upphæðirnar á fjárhagslykilinn sem tilgreindur er í reitnum **Reikningur óinnleysts hagnaðar** eða í reitnum **Reikningur óinnleysts taps** á síðunni **Gjaldmiðlar**. Jöfnunarfærslurnar bókast sjálfkrafa á reikninginn útistandandi - gjaldfallið í fjárhag.

Keyrslan vinnur allar opnar viðskiptamanna- og lánardrottnafærslur. Ef gengismunur er á færslu stofnar keyrslan nýjan sundurliðaða viðskiptamanna- eða lánardrottnafærslu. Nýja færslan sýnir leiðréttu upphæðina í viðskiptamanna- eða lánardrottnafærslunni.

#### Víddir í færslum viðskiptamanna og lánardrottna

[!INCLUDE [prod_short](includes/prod_short.md)] úthlutar víddunum úr viðskiptamanna- eða lánardrottnafærslunum í leiðréttingarfærslurnar og bókar leiðréttingar á hverri samsetningu víddargilda.

### Áhrif á bankareikninga

Keyrslan leiðréttir gjaldmiðilinn í bankareikningum með því að nota gengið sem gildir fyrir bókunardagsetninguna sem tilgreind er í keyrslunni. Keyrslan reiknar mismuninn fyrir hvern bankareikning sem er með gjaldmiðilskóða og bókar upphæðirnar á fjárhagslykilinn sem er tilgreindur í reitnum **Reikningur innleysts hagnaðar** eða í reitnum **Reikningur innleysts taps** á síðunni **Gjaldmiðlar**. Jöfnunarfærslurnar bókast sjálfkrafa á fjárhag bankareikninga sem eru tilgreindir í bókunarflokki bankareikninga. Keyrslan reiknar eina færslu á hvern gjaldmiðil í hverjum bókunarflokki.

#### Víddir í bankareikningsfærslum

Leiðréttingarfærslum vegna fjárhagsreiknings bankareiknings og hagnaðar-/tapreiknings er úthlutað sjálfgefnum víddum bankareikningsins.

### Áhrif á fjárhagsreikninga

Ef bókað er í öðrum skýrslugjaldmiðli getur keyrslan búið til nýjar fjárhagsfærslur fyrir gjaldmiðilsleiðréttingu milli heimagjaldmiðils og annars skýrslugjaldmiðils. Keyrslan reiknar mismuninn fyrir hverja fjárhagsfærslu. Hún leiðréttir fjárhagsfærsluna eftir efni reitsins **Gengisleiðrétting** fyrir hvern fjárhagsreikning.

#### Víddir í fjárhagsreikningsfærslum

Leiðréttingarfærslunum er úthlutað sjálfgefnum víddum úr reikningunum sem þær eru bókaðar á.

> [!Important]
> Áður en hægt er að nota keyrsluna þarf að færa inn gengið sem notað er til að leiðrétta gengisbreytingar á skuldum í erlendum gjaldmiðli. Þetta er gert á síðunni **Gengi gjaldmiðla**.<br><br>  

> [!Video https://www.microsoft.com/videoplayer/embed/RE3Q24s?rel=0]

## Setja upp gengisþjónustu fyrir gengi gjaldmiðla

Hægt er að nota ytri þjónustu til að halda gengi gjaldmiðla uppfært.

> [!NOTE]
> Flestar gengisþjónustur veita gögn sem samrýmast innflutningsferlinu í [!INCLUDE[prod_short](includes/prod_short.md)]. Stundum eru gögnin sniðin á mismunandi hátt og sérsníða þarf innflutningsferlið. Hægt er að nota gagnaskiptarammann til að gera það með því að bæta við eigin kóðaeiningu. Þú þarft líklega aðstoð frá þróunaraðila til að gera þetta. Frekari upplýsingar er að finna í [Setja upp skilgreiningar gagnaskipta](across-how-to-set-up-data-exchange-definitions.md).

1.  ![Veldu Lightbulb sem opnar Tell Me eiginleikann.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, slá inn **Gengisþjónustu gjaldmiðils** og velja síðan viðeigandi tengil.
2. Aðgerðin Ný er **valin** .
3. Fylltu í reitina eftir því sem nauðsyn krefur á síðunni **Þjónusta fyrir gengi gjaldmiðils**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Kveiktu á **Virkjað** víxlhnappinum til að virkja þjónustuna.

> [!NOTE]
> Eftirfarandi myndband sýnir hvernig hægt er að tengjast gengisþjónustu við gengi gjaldmiðla með því að nota Seðlabanka Evrópu sem dæmi. Í hlutanum sem lýsir því hvernig á að setja upp reitavörpun skilar stillingin í dálknum **Uppruni** fyrir **yfirhnút fyrir gjaldmiðilskótann**  aðeins fyrsta gjaldmiðilinn sem fannst. Stillingin á að vera `/gesmes:Envelope/Code/Code/Code`.

<br><br>  
  
> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4A1jy?rel=0]

## Uppfæra gengi gjaldmiðla með þjónustu

Fylgja skal skrefunum sem gefin eru til að uppfæra gengi gjaldmiðla með þjónustu:

1.  ![Veldu Lightbulb sem opnar Tell Me eiginleikann.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, slá inn **Gjaldmiðlar** og velja síðan viðeigandi tengil.
2. Velja skal aðgerðina **Uppfæra gengi** .

## Leiðrétta mistök

Stundum gæti þurft að leiðrétta mistök í greiðslufærslu sem tengist leiðréttingum á hagnaði og tapi á erlendum gjaldmiðli. Hægt er að nota **síðurnar Bakfæra viðskiptafærslur** á síðunum **Bankafærslur**, **Viðskm.færslur** og **Lánardr.færslur** til að ógilda og bakfæra greiðsluviðskiptin.

> [!NOTE]
> Þegar greiðsla er bakfærð og bakfærð fyrir færslu sem var með gengisleiðréttingu á gengi sem tengdist henni bókar bakfærsla bakfærslu vegna leiðréttinganna. Hugsanlega þarf að keyra gengisleiðréttinguna aftur til að fá rétta núverandi stöðu.

## Sjá einnig .

[Gjaldmiðlar í Business Central](finance-currencies.md)  
[Uppsetning gjaldmiðla](finance-set-up-currencies.md)  
[Setja upp annan skýrslugjaldmiðil](finance-how-setup-additional-currencies.md)  
[Lokaár og Tímabil](year-close-years-periods.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
