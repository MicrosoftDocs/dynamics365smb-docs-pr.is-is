---
title: Að nota C5 gagnaflutningsviðbótina | Microsoft skjöl
description: 'Þessi viðbót er notuð til að flytja viðskiptamenn, lánardrottna, vörur og fjárhagsreikninga úr Microsoft Dynamics C5 2012 í Business Central.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'extension, migrate, data, C5, import'
ms.search.form: '1860, 1861, 1862, 1863, 1864, 1867, 1868, 1869, 1874, 1882, 1883, 1884, 1885, 1886, 1888, 1890, 1891, 1892, 1893, 1894, 1898, 1899, 1900, 1901, 1902, 1903, 1904, 1905, 1906'
ms.date: 12/11/2023
ms.author: bholtorf
---

# <a name="the-c5-data-migration-extension"></a>C5 gagnaflutningsframlengingin

Þessi viðbót auðveldar flutning viðskiptamanna, lánardrottna, vara og fjárhagsreikninga úr Microsoft Dynamics C5 2012 í [!INCLUDE[prod_short](includes/prod_short.md)]. Hægt er að flytja elrdi færslur fyrir fjárhagsreikning.

> [!NOTE]
> Fyrirtækið í [!INCLUDE[prod_short](includes/prod_short.md)] má ekki innihalda gögn. Að auki skaltu ekki búa til viðskiptavini, lánardrottna, vörur eða reikninga fyrr en flutningur lýkur.

## <a name="what-data-is-migrated"></a>Hvaða gögn eru flutt?

Eftirfarandi gögn eru flutt fyrir hverja einingu:

### <a name="customers"></a>Viðskiptavinir

* Tengiliður  
* Birgðageymsla
* Land
* Vídd viðskiptavina (deild, miðstöð, tilgangur)
* Afhendingarmáti
* Sölumaður
* Greiðsluskilmálar
* Greiðslumáti
* Verðflokkur viðskiptamanns
* Reikningsafsláttur viðskiptavinar

Ef reikningar eru fluttir eru eftirfarandi gögn einnig flutt:

* Uppsetning bókunar viðskiptavinar
* Almenn færslubókarkeyrsla
* Opnar færslur (í viðskiptamannabók)

### <a name="vendors"></a>Lánardrottnar

* Tengiliður
* Birgðageymsla
* Land
* Vídd lánardrottins (deild, miðstöð, tilgangur)
* Reikningsafsláttur
* Afhendingarmáti
* Innkaupaaðili
* Greiðsluskilmálar
* Greiðslumáti
* Afsláttur lánardrottnareikninga

Ef reikningar eru fluttir eru eftirfarandi gögn einnig flutt:

* Bókunarflokkur lánardrottins
* Almenn færslubókarkeyrsla
* Opnar færslur (fjárhagsfærslur lánardrottins)

### <a name="items"></a>Birgðir

* Birgðageymsla
* Land
* Vöruvíddir (deild, miðstöð, tilgangur)
* Sölulínuafslættir
* Afsláttarflokkar viðskiptamanna
* Vöruafsláttarflokkar
* Söluverð
* Tollnúmer
* Mælieiningar
* Vörurakningarkóti
* Verðflokkur viðskiptamanns
* Samsetningaruppskrift

Ef reikningar eru fluttir eru eftirfarandi gögn einnig flutt:

* Birgðabókunargrunnur
* Almennur bókunargrunnur
* Birgðabókarkeyrsla
* Opnar færslur (birgðafærslur)

> [!NOTE]
> Ef opnar færslur eru til staðar sem nota erlenda gjaldmiðla er gengi þeirra einnig flutt inn. Önnur gengi eru ekki flutt inn.

### <a name="chart-of-accounts"></a>Bókhaldslykill

* Staðlaðar víddir: Deild, kostnaðarstaður, tilgangur  
* Sögulegar fjárhagsfærslur  

> [!NOTE]
> Sögulegar fjárhagsfærslur eru meðhöndlaðir aðeins öðruvísi. Þegar þú flytur gögn stillirðu færibreytuna **Núverandi tímabil**. Þessi færibreyta tilgreinir hvernig á að vinna úr fjárhagsfærslum. Færslur eftir þessa dagsetningu eru fluttar hver fyrir sig. Færslum fyrir þessa dagsetningu er safnað saman fyrir hvern reikning og fluttar sem ein upphæð. Segjum sem dæmi að það séu færslur á árunum 2015, 2016, 2017, 2018 og þú tilgreinir 1. janúar 2017 í reit núverandi tímabils. Fyrir hvern reikning verður upphæðum fyrir færslur á eða fyrir 31. desember 2016 safnað saman í eina færslubókarlínu fyrir hverja fjárhagsfærslu. Allar færslur eftir þennan dag verða fluttar hver fyrir sig.

## <a name="file-size-requirements"></a>Kröfur um skráarstærð

Stærsta skráin sem þú getur hlaðið upp til [!INCLUDE[prod_short](includes/prod_short.md)] er 150 MB. Ef skráin sem þú ert að flytja út úr C5 er stærri en það, skaltu íhuga að flytja gögn í mörgum skrám. Til dæmis, flytja eina eða tvær gerðir eininga úr C5, svo sem viðskiptavinum og lánardrottnum, í skrá, og síðan flytja út hluti í annarri skrá, og svo framvegis. Hægt er að flytja inn skrár hver í sínu lagi í [!INCLUDE[prod_short](includes/prod_short.md)].

## <a name="to-migrate-data"></a>Til að flytja gögn

Það eru aðeins nokkur skref fólgin í því að flytja út gögn úr C5 og flytja þau inn í [!INCLUDE[prod_short](includes/prod_short.md)]:  

1. Í C5 skaltu nota **Flytja út gagnagrunn** eiginleikann til að flytja út gögnin. Sendu síðan útflutningsmöppuna í þappaða möppu.  
2. Í [!INCLUDE[prod_short](includes/prod_short.md)] skal velja ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Gagnaflutningur** og velja síðan **Gagnaflutningur**.  
3. Ljúka skal skrefunum í leiðbeiningum um uppsetningu með hjálp. Gakktu úr skugga um að velja **Flytja inn úr Microsoft Dynamics C5 2012** sem gagnagjafa.  

## <a name="viewing-the-status-of-the-migration"></a>Skoðun stöðu á flutningi

Nota skal síðuna **Gagnaflutningsyfirlit** til að sjá stöðu flutningsins. Síðan sýnir upplýsingar eins og fjölda eininga sem flutningurinn inniheldur, stöðu flutningsins og fjölda hluta sem hafa verið fluttir og hvort þau hafi tekist. Hún sýnir einnig fjölda villna, gerir þér kleift að rannsaka hvað fór úrskeiðis og, þegar mögulegt er, auðveldar það að fara í færsluna til að laga vandamálin. Fyrir frekari upplýsingar, sjá næsta kafla í þessari grein.  

> [!NOTE]
> Meðan beðið er eftir stöðu flutningsins þarf að uppfæra síðuna til að birta niðurstöðurnar.

## <a name="how-to-avoid-double-posting"></a>Hvernig á að koma í veg fyrir tvíbókun

Til að koma í veg fyrir tvíbókanir í fjárhagnum eru eftirfarandi mótreikningar notaðir fyrir opnar færslur:  

* Fyrir lánardrottna notum við viðskiptaskuldareikninginn frá bókunarflokki lánardrottins.  
* Fyrir viðskiptavini notum við viðskiptakröfureikninginn frá bókunarflokki viðskiptavinar.  
* Fyrir vörur búum við til almennan bókunargrunn þar sem leiðréttingarreikningurinn er reikningurinn sem er tilgreindur sem birgðarreikningur í birgðabókunargrunni.  

## <a name="correcting-errors"></a>Leiðrétting villna

Ef eitthvað fer úrskeiðis og villa kemur upp sýnir **Status** reiturinn **Completed with Errors** og **Villatalning** reiturinn mun sýna hversu margar. Til að skoða lista yfir villurnar er hægt að opna **Villur í gagnaflutningi** síðuna með því að velja:  

* Talan í **Villutalning** reitnum fyrir eininguna.  
* Einingin og svo **Sýna villur** aðgerðin.  

Á síðunni **Villur í gagnaflutningi**, til að laga villa getur þú valið villuboð, og síðan velja **Breyta skrá** til að skoða gögn sem flutt voru fyrir eininguna. Ef þú hefur nokkrar villur til að laga, getur þú valið **Magnlagfæringar á villum** til að breyta einingum í lista. Þú þarft samt að opna einstakar færslur ef villan var af völdum tengdrar færslu. Til dæmis verður söluaðili ekki fluttur ef netfang sem einn af tengiliðum þeirra er með ógilt snið.

Eftir að þú hefur lagað eina eða fleiri villur getur þú valið **Flytja** til að flytja aðeins einingarnar sem þú lagaðir án þess að þurfa að hefja flutninginn aftur.  

> [!TIP]
> Ef þú hefur lagað fleiri en eina villu geturðu notað **Velja fleira** valkostinn til að velja margar línur til að flytja. Ef villur eru til staðar sem ekki er mikilvægt að laga geturðu valið þær og svo **Sleppa vali**.

> [!NOTE]
> Ef vörur eru til staðar sem er að finna í uppskrift gætir þú þurft að flytja oftar en einu sinni ef upprunalega varan er ekki stofnuð fyrir afbrigðið sem vísa til hennar. Ef afbrigðið er búið til fyrst getur tilvísunin í upprunalegu vöruna valdið villuboðum.  

## <a name="verifying-data-after-migrating"></a>Staðfesting gagna eftir flutning

Ein leið til að sannreyna að gögnin hafi verið rétt flutt inn er með því að skoða eftirfarandi síður í C5 og [!INCLUDE[prod_short](includes/prod_short.md)].

|Microsoft Dynamics C5 2012 | Dynamics 365 Business Central| Runuvinnsla sem á að nota |
|---------------------------|------------------------------|------------------|
|Viðskm.færslur| Almennar færslubækur| CUSTMIGR |
|Lánardr.færslur| Almennar færslubækur| VENDMIGR|
|Birgðafærslur| Birgðabækur| ITEMMIGR |
|Fjárhagsfærslur| Færslubækur| GLACMIGR |

## <a name="stopping-data-migration"></a>Stöðvun gagnaflutnings

Þú getur hætt að flytja gögn með því að velja **Hætta við allan flutning**. Ef þú gerir það er líka hætt við allan flutning sem bíður.

## <a name="see-also"></a>Sjá einnig .

[Sérstilling [!INCLUDE[prod_short](includes/prod_short.md)] með viðbótum](ui-extensions.md)  
[Undirbúðu þig fyrir að gera viðskipti](ui-get-ready-business.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
