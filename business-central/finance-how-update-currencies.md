---
title: Uppfæra gengi
description: Fylgstu með upphæðum í mismunandi gjaldmiðlum með gjaldmiðilskóðum og leyfðu Business Central að hjálpa þér að stilla gengi erlendra gjaldmiðla fyrir bókaðar færslur með utanaðkomandi þjónustu.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: multiple currencies, adjust exchange rates, FX rates
ms.date: 07/23/2021
ms.author: edupont
ms.openlocfilehash: c4072e0371499982fc86d6c16b4d614552bc4533
ms.sourcegitcommit: e904da8dc45e41cdd1434111c15e2a9d9edd3fa2
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/23/2021
ms.locfileid: "6660182"
---
# <a name="update-currency-exchange-rates"></a>Uppfæra gengi

Þar sem fyrirtæki starfa í mörgum löndum/svæðum er nauðsynlegt fyrir þau að geta stundað viðskipti og skráð fjárhagslegar upplýsingar í fleiri en einum gjaldmiðli. Gjaldmiðill á staðnum er tilgreindur á síðunni **Fjárhagsgrunnur** eins og lýst er í greininni [Uppsetning fjárhagsgrunns](finance-setup-finance.md). Þegar staðbundinn gjaldmiðill hefur verið skilgreindur verður hann tómur gjaldmiðill. Þegar reiturinn **Gjaldmiðill** er auður merkir það að gjaldmiðillinn er SGM.  

Því næst þarf að setja upp gjaldmiðilskóða fyrir hvern gjaldmiðil sem er notaður ef keypt er eða selt er í öðrum gjaldmiðlum en staðbundnum gjaldmiðli (SGM). Einnig er hægt að stofna bankareikninga með gjaldmiðlum. Hægt er að skrá fjárhagsfærslur í mismunandi gjaldmiðlum, en fjárhagsfærslan verður ávallt færð í staðbundnum gjaldmiðli (SGM).

> [!Important]
> Ekki skal búa til gjaldmiðilskóða bæði í **Fjárhagsáætlun** og á síðunni **Gjaldmiðlar**. Þetta mun skapa villu milli auðs gjaldmiðils og SGM kóðans í gjaldmiðlatöflunni og bankareikningar, viðskiptavinir eða lánardrottnar gætu verið stofnaðir óvart, sumir með auðan gjaldmiðil og aðrir með SGM kóðann.

Fjárhagurinn þinn er settur upp til að nota staðbundna gjaldmiðilinn (SGM), en þú getur sett hann upp til að einnig nota annan gjaldmiðil með gengi stillt. Sé öðrum gjaldmiðli gefin svokölluð skilgreining Viðbótarskýrslugjaldmiðill mun [!INCLUDE[prod_short](includes/prod_short.md)] skrá upphæðirnar sjálfkrafa bæði í SGM og þessum viðbótarskýrslugjaldmiðli í hverri fjárhagsfærslu og í öðrum færslum á borð við færslur fyrir VSK. Nánari upplýsingar er að finna í [Setja upp annan skýrslugjaldmiðil](finance-how-setup-additional-currencies.md). Viðbótarskýrslugjaldmiðillinn er oftast notaður til að auðvelda fjárhagsskýrslugerð til eigenda sem búa í löndum/svæðum sem nota annan gjaldmiðil en staðbundinn gjaldmiðill (SGM).  

> [!IMPORTANT]
> Ef þú vilt nota annan skýrslugjaldmiðil fyrir fjárhagsskýrslur skaltu ganga úr skugga um að þú skiljir takmarkanirnar. Nánari upplýsingar er að finna í [Setja upp annan skýrslugjaldmiðil](finance-how-setup-additional-currencies.md).

## <a name="currencies"></a>Gjaldmiðlar

> [!NOTE]  
> Í [!INCLUDE[prod_short](includes/prod_short.md)], ef þú ert að leita að nýjustu upplýsingum um gengi erlendra gjaldmiðla eða eldri gengi, finnur þú það undir gjaldmiðli. Auk þessarar greinar geturðu skoðað [Setja upp annan skýrslugjaldmiðil](finance-how-setup-additional-currencies.md).

Gjaldmiðilskóðarnir eru tilgreindir í **Gjaldmiðlar**, þ.m.t. viðbótarupplýsingar og stillingar sem eru nauðsynlegar fyrir hvern gjaldmiðilskóða.

> [!TIP]
> Búðu til gjaldmiðla með alþjóðlegum ISO-kóða þar sem kóðinn einfaldar vinnu við gjaldmiðilinn í framtíðinni.

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

### <a name="example-of-a-receivable-currency-transaction"></a>Dæmi um móttekna gjaldmiðilsfærslu

Þegar þú færð reikning frá fyrirtæki í erlendum gjaldmiðli er nokkuð auðvelt að reikna út staðbundið verðgildi reikningsins miðað við gengi gjaldmiðilsins í dag. Hins vegar fylgir reikningnum oft greiðsluskilmálar svo að þú getur seinkað greiðslunni til síðari tíma, sem gefur til kynna hugsanlega annað gengi gjaldmiðils. Þetta vandamál ásamt því að bankagengi gjaldmiðla er alltaf annað en opinbert gengi gjaldmiðla gerir það að verkum að ekki er hægt að gera ráð fyrir nákvæmri upphæð í staðbundnum gjaldmiðli sem þarf til að ná að dekka reikninginn. Ef gjalddagi reikningsins er til næsta mánaðar gætir þú einnig þurft að endurmeta upphæðina í staðbundnum gjaldmiðli í lok mánaðarins. Leiðrétting gjaldmiðilsins er nauðsynleg vegna þess að nýja LCY-gildið sem krafist er til að standa undir reikningsupphæðinni gæti verið annað og skuldir fyrirtækisins við lánardrottin gætu hafa breyst. Nýja LCY-upphæðin gæti verið hærri eða lægri en fyrri upphæðin og mun því tákna hagnað eða tap. Þar sem reikningurinn hefur ekki enn verið greiddur telst hagnaðurinn eða tapið *óinnleyst*. Seinna er reikningurinn greiddur og bankinn hefur skilað raunverulegu gengi gjaldmiðilsins fyrir greiðsluna. Það er ekki fyrr en nú sem *innleystur* hagnaðurinn eða tapið er reiknað út. Þessi óinnleysti hagnaður eða tap er þá bakfærður og innleystur hagnaður eða tap er birt í staðinn.

Í eftirfarandi dæmi er reikningur móttekinn 1. janúar með gjaldmiðilsupphæðinni 1000. Þá er gjaldmiðillinn 1,123.

|Dagsetning|Aðgerð|Gjaldmiðilsupphæð|Tíðni fylgiskjals|LCY upphæð á skjali|Tíðni leiðréttingar|Reikningur óinnleysts hagnaðar|Greiðslutíðni|Reikningur innleysts taps|  
|-----|----------|------------|-----------|---------|-----------|-------------|---------|---------|
|1/1|**Reikningur**|1000|1,123|1123|||||
|1/31|**Leiðrétting**|1000||1125|1,125|2|||
|2/15|**Bakfærsla leiðréttingar við greiðslu**|1000||||-2|||
|2/15|**Greiðsla**|1000||1120|||1,120|-3|

Í lok mánaðarins er gerð gjaldmiðlaleiðrétting þar sem gjaldmiðilsgengi leiðréttingarinnar hefur verið stillt á 1,125, sem veldur óinnleystum hagnaði upp á 2.

Við greiðslu sýnir raungengi gjaldmiðils sem skráð var í bankaviðskiptunum gengið 1,120.

Hér er um óinnleysta færslu að ræða og því verður hún afturkölluð ásamt greiðslunni.

Að lokum er greiðslan skráð og innleyst tap er bókað á reikning innleyst taps.

## <a name="available-currency-functions"></a>Tiltækar aðgerðir gjaldmiðla

Í eftirfarandi töflu er gerð grein fyrir lykilaðgerðum á síðunni **Gjaldmiðlar**. Sumar aðgerðirnar eru útskýrðar í næstu köflum.  

|Valmynd|Aðgerð|Description|
|-------------|--------------|------------------------------|
|**Vinna**|**Stinga upp á reikningum**|Nota reikninga úr öðrum gjaldmiðlum. Algengustu reikningarnir verða settir inn.|
||Breyta greiðsluvikmörkum|Breyta annaðhvort eða bæði hámarks greiðsluvikmörkum eða prósentutölu greiðsluvikmarka og afmarka eftir gjaldmiðli. Frekari upplýsingar eru í [Greiðsluvikmörk og greiðsluafsláttarvikmörk](finance-payment-tolerance-and-payment-discount-tolerance.md)|
||**Gengi**|Skoða uppfært gengi fyrir gjaldmiðlana sem eru notaðir.|
||**Leiðrétta gengi**|Leiðrétta fjárhags-, viðskiptamanna-, lánadrottna- og bankareikningsfærslur til að staðan sé uppfærð ef gengið hefur breyst síðan færslurnar voru bókaðar.|
||**Gengisleiðréttingarbók**|Skoða niðurstöður runuvinnslunnar **Leiðrétta gengi**. Ein lína er búin til fyrir hvern gjaldmiðil sem leiðréttur er, eða gjaldmiðil og bókunarflokk.|
|**Gengisþjónusta**|**Gengisþjónustur**|Skoða eða breyta uppsetningunni á þjónustunni sem er sett upp til að sækja uppfært gengi gjaldmiðla þegar þú velur aðgerðina **Uppfæra gengi**.|
||**Uppfæra gengi**|Sækja nýjasta gengi gjaldmiðils frá þjónustuveitu.|
|**Skýrslur**|**Gengisjöfnuður**|Skoða stöðuna hjá öllum viðskiptamönnum og lánardrottnum bæði í erlendum gjaldmiðli og staðbundnum gjaldmiðli (SGM). Skýrslan sýnir tvær stöður í SGM. Einn er staðan í erlendum gjaldmiðli umreiknuð í SGM með því að nota gengi á tíma færslunnar. Hinn er staðan í erlendum gjaldmiðli umreiknuð í SGM með því að nota gengi á vinnudagsetningu.|

## <a name="exchange-rates"></a>Gengi gjaldmiðils

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

## <a name="adjusting-exchange-rates"></a>Gengi leiðrétt

Vegna þess hve tíðar gengisbreytingar eru verður reglubundið að leiðrétta aðra jafngildisgjaldmiðla í kerfinu. Sé það ekki gert verða upphæðir misvísandi sem hafa verið umreiknaðar úr erlendum (eða aukalegum) gjaldmiðlum og bókaðar í fjárhag í SGM. Að auki verður að uppfæra daglegar færslur sem eru bókaðar áður en daglegt gengi er fært inn eftir að upplýsingarnar um daglegt gengi hafa verið færðar inn.

Runuvinnslan **Leiðrétta gengi** er notuð til að lagfæra handvirkt gengi bókaðs viðskiptamanns, lánardrottins og bankareikningsfærslna. Hún getur einnig uppfært upphæðir annars skýrslugjaldmiðils í fjárhagsfærslum.  

> [!TIP]
> Hægt er að nota þjónustu til að uppfæra gengi sjálfkrafa í kerfinu. Frekari upplýsingar er að finna í [Að setja upp þjónustu um gengi gjaldmiðils](finance-how-update-currencies.md#to-set-up-a-currency-exchange-rate-service). Þetta leiðréttir hins vegar ekki gengi í þegar bókuðum færslum. Til að uppfæra gengi á bókuðum færslum skaltu nota runuvinnsluna **Leiðrétta gengi**.

### <a name="effect-on-customers-and-vendors"></a>Áhrif á viðskiptamenn og lánardrottna

Keyrslan leiðréttir gjaldmiðilinn í reikningum viðskiptamanna og lánardrottna með því að nota gengið sem gildir fyrir bókunardagsetninguna sem tilgreind er í keyrslunni. Keyrslan reiknar mismuninn fyrir hverja gjaldmiðilsstöðu og bókar upphæðirnar á fjárhagslykilinn sem tilgreindur er í reitnum **Reikningur óinnleysts hagnaðar** eða í reitnum **Reikningur óinnleysts taps** á síðunni **Gjaldmiðlar**. Jöfnunarfærslurnar bókast sjálfkrafa á reikninginn útistandandi - gjaldfallið í fjárhag.

Keyrslan vinnur allar opnar viðskiptamanna- og lánardrottnafærslur. Ef gengismunur er á færslu stofnar runuvinnslan nýja sundurliðaða viðskiptavina- eða lánardrottnafærslu sem endurspeglar leiðréttu upphæðina í viðskiptavina- eða lánardrottnafærslunni.

#### <a name="dimensions-on-customer-and-vendor-ledger-entries"></a>Víddir í fjárhagsfærslum viðskiptavina og lánardrottna

Leiðréttingarfærslum er úthlutað víddum úr viðskiptavina-/lánardrottnafærslum og leiðréttingar eru bókaðar eftir samsetningum á víddagildum.

### <a name="effect-on-bank-accounts"></a>Áhrif á bankareikninga

Keyrslan leiðréttir gjaldmiðilinn í bankareikningum með því að nota gengið sem gildir fyrir bókunardagsetninguna sem tilgreind er í keyrslunni. Keyrslan reiknar mismuninn fyrir hvern bankareikning sem er með gjaldmiðilskóða og bókar upphæðirnar á fjárhagslykilinn sem er tilgreindur í reitnum **Reikningur innleysts hagnaðar** eða í reitnum **Reikningur innleysts taps** á síðunni **Gjaldmiðlar**. Jöfnunarfærslurnar bókast sjálfkrafa á fjárhag bankareikninga sem eru tilgreindir í bókunarflokki bankareikninga. Keyrslan reiknar eina færslu á hvern gjaldmiðil í hverjum bókunarflokki.

#### <a name="dimensions-on-bank-account-entries"></a>Víddir í bankareikningsfærslum

Leiðréttingarfærslum vegna fjárhagsreiknings bankareikningsins og vegna hagnaðar-/tapreiknings er úthlutað sjálfgefnum víddum bankareikningsins.

### <a name="effect-on-gl-accounts"></a>Áhrif á fjárhagsreikninga
Ef bókað er í öðrum skýrslugjaldmiðli er hægt að láta keyrsluna búa til nýjar fjárhagsfærslur fyrir gjaldmiðilsmismun á SGM og öðrum skýrslugjaldmiðli. Keyrslan reiknar mismuninn miðað við hverja einstaka fjárhagsfærslu og leiðréttir fjárhagsfærsluna með tilliti til innihaldi reitsins **Gengisleiðrétting** fyrir hvern fjárhagslykil.

##### <a name="dimensions-on-gl-account-entries"></a>Víddir í fjárhagsreikningsfærslum
Leiðréttingarfærslunum er úthlutað sjálfgefnu víddunum í reikningunum sem þær eru bókaðar á.

> [!Important]
> Áður en hægt er að nota keyrsluna verður að færa inn gengið sem á að nota til þess að leiðrétta gengismun gjaldeyrisins. Þetta er gert á síðunni **Gengi gjaldmiðla**.<br><br>  

> [!Video https://www.microsoft.com/videoplayer/embed/RE3Q24s?rel=0]

## <a name="to-set-up-a-currency-exchange-rate-service"></a>Setja upp þjónustu um gengi gjaldmiðils
Þú getur notað ytri þjónustu til að halda gjaldeyrisviðskiptum þínum uppfærðum, t.d. FloatRates.

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

## <a name="see-related-training-at-microsoft-learn"></a>Sjá tengda þjálfun á [Microsoft Learn](/learn/paths/use-multiple-currencies-dynamics-365-business-central/)

## <a name="see-also"></a>Sjá einnig
[Setja upp annan skýrslugjaldmiðil](finance-how-setup-additional-currencies.md)  
[Lokaár og Tímabil](year-close-years-periods.md)  
[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
