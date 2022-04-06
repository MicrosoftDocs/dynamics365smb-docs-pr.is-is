---
title: Setja upp virðisaukaskatt
description: Ganga úr skugga um að rétt reikna, bóka, og tilkynna á VSK vegna sölu eða innkaup. Mælt er með að nota uppsetningarleiðsögn til að setja upp VSK.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: VAT, posting, tax, value-added tax
ms.search.form: 10, 1877, 470, 471, 472
ms.date: 03/04/2022
ms.author: bholtorf
ms.openlocfilehash: 285f0f224853837e2aac6553c34d366afb09f08a
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2022
ms.locfileid: "8519226"
---
# <a name="set-up-calculations-and-posting-methods-for-value-added-tax"></a>Uppsetning fyrir útreikning og bókunaraðferðir virðisaukaskatts

Neytendur og fyrirtæki greiða virðisaukaskatt (VSK) þegar þau kaupa vörur eða þjónustu. Upphæð VSK til greiðslu getur verið mismunandi, það fer eftir nokkrum þáttum. Í [!INCLUDE[prod_short](includes/prod_short.md)] er settur upp VSK til að tilgreina Taxtar sem á að nota við útreikning á skattupphæðum á grundvelli eftirfarandi færibreyta:

* Hverjum selt er  
* Hverjum keypt er af  
* Það sem er selt  
* Hvað keypt er  

Hægt er að setja upp VSK-útreikning handvirkt, en það getur verið bæði snúið og tímafrekt. Til að auðvelda, útveguðum við uppsetningarleiðsögn með hjálp sem nefnist **VSK Uppsetning** sem hjálpar til við verkstig. Mælt er með að nota uppsetningarleiðsögn til að setja upp VSK.

> [!NOTE]  
> Hægt er að nota leiðbeiningarnar, aðeins ef þú hefur stofnað Mitt fyrirtæki, og hefur ekki bókað færslur sem innihalda VSK. Annars er mjög auðvelt að nota mismunandi VSK taxta af misgáning og gera VSK-skýrslum ónákvæmt.  

Ef setja á upp VSK-útreikninga sjálfur eða bara á að fræðast um hvert skref er lýsing á því í þessari grein að finna lýsingar á hverju skrefi.  

[!INCLUDE [finance-vat](includes/finance-vat.md)]

## <a name="use-the-vat-setup-assisted-setup-guide-to-set-up-vat-recommended"></a>Nota leiðbeiningar fyrir uppsetningu VSK-uppsetningar til að setja upp VSK (ráðlegt)

Mælt er með að nota VSK-uppsetningarleiðsögn með hjálp til að setja upp VSK í [!INCLUDE[prod_short](includes/prod_short.md)].

Til að ræsa uppsetningleiðbeiningar með hjálp, fylgið þessum skrefum:

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar 1.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Uppsetning með hjálp**.  
2. Velja **Setja upp VSK** og ljúkið við skrefin.
3. Þegar uppsetningu hjálpar er lokið skal fara á **síðuna VSK-bókunargrunnur** og athuga hvort fylla þurfi í fleiri reiti samkvæmt staðbundnum kröfum í útgáfunni [!INCLUDE [prod_short](includes/prod_short.md)]. Frekari upplýsingar er að finna í [Staðbundin virkni í Business Central](about-localization.md)  

### <a name="check-the-vat-posting-setup"></a>Athuga skal VSK-bókunaruppsetninguna

Til að styðja þig í að byrja hratt [!INCLUDE [prod_short](includes/prod_short.md)] sýnir þú tilkynningar ef Fjárhagur vantar (fjárhagsreikningar) eru í bókunarflokkum eða bókunaruppsetningar eins og **bókunaruppsetning** VSK. Hægt er að skipta þessari gerð tilkynninga á eða úr með því að *nota fjárhagsreikninga sem vantar í bókunarflokk eða tilkynningu í uppsetningu* á **síðunni tilkynningar** mínar. Farðu **bara á síðuna stillingarnar** og veldu *svo breytinguna þegar ég fæ tilkynningar.* .  

Ef slík tilkynning er valin, [!INCLUDE [prod_short](includes/prod_short.md)] stofnar sjálfkrafa þær bókunaruppsetningar sem eru byggðar á bókunarflokkum í skjalinu eða færslubókinni sem verið er að vinna að.  

Á þessu stigi er ef til vill bara hægt að fylla út í þá sem vantar fjárhagsreikninga. Seinna var svo hugsanlega hægt að átta sig á uppsetningunni þegar frekari betrumbæta var bætt. [!INCLUDE [prod_short](includes/prod_short.md)] leyfir ekki eyðingu VSK-bókunaruppsetningar og almennrar bókunaruppsetningar þegar færslur eru stofnaðar á grundvelli slíkra afbrigða. Sem byrjar í 2022 1. er hægt að nota **reitinn lokaður** á **uppsetningarsíðu** VSK-bókunar til að koma í veg fyrir að notendur hafi rangt með uppsetningu sem er ekki lengur viðeigandi fyrir nýjar bókanir.

## <a name="set-up-vat-registration-numbers-for-your-country-or-region"></a>Setja upp VSK-númer fyrir land eða svæði

Til að ganga úr skugga um að rétt VSK-númer séu slegin inn er hægt að skilgreina snið fyrir VSK-númer sem eru notuð í löndum eða svæðum þar sem viðskipti notanda eru stunduð. [!INCLUDE[prod_short](includes/prod_short.md)] mun birta villuboð þegar einhver gerir mistök eða nota snið sem er rangt fyrir landið eða svæðið.

Til að setja upp VSK-númer skal fylgja eftirfarandi skrefum:

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar 2.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Lönd/svæði**.
2. Velja skal landið eða svæðið og svo agðerðina **Snið VSK-númers**.
3. Í reitnum **Snið** skal skilgreina sniðin með því að slá inn einn eða fleiri eftirfarandi stafa:  

* **#** Krefst númers sem er ein tala.  
* **@** Krefst stafs. Þetta snið er ekki Stafrétt.  
* **?** Leyfir hvaða staf sem er.  

    > [!Tip]
    > Hægt er að nota þessa stafi svo framarlega sem þeir eru alltaf til staðar í sniði landsins eða svæðisins. Ef t.d. þarf að hafa með punkt eða bandstrik milli talna skal skilgreina sniðið sem ##.####.### eða @@-###-###.  

## <a name="set-up-vat-business-posting-groups"></a>Uppsetning VSK-viðskiptabókunarflokka

VSK-viðskiptabókunarflokkar á að tákna markaðina þar sem þú stundar viðskiptum við viðskiptamenn og lánardrottna, og tilgreina hvernig á að reikna og bóka VSK á sérhverjum markaði. Dæmi um VSK viðskiptabókunarflokka eru **Innanlands** og **Evrópusambandið (ESB)**.  

Nota skal kóða sem auðvelt er að muna og er auðkennandi fyrir viðskiptaflokkinn, til dæmis **ESB**, **Ekki-ESB**, eða **Innlent**. Kótinn þarf að vera einstakur. Þú getur sett upp eins marga kóða og þörf krefur, en ekki er hægt að nota sama kóðann oftar en einu sinn í einni töflu.

Til að setja upp VSK-viðskiptabókunarflokk er þessu skrefum fylgt:

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar 3.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **VSK-viðskiptabókunarflokk** og velja síðan viðkomandi tengil.  
2. Fyllið inn í svæðin eftir þörfum.

Sjálfgefnir VSK-viðskiptabókunarflokkar eru settir upp með því að tengja þá við almenna viðskiptabókunarflokka. [!INCLUDE[prod_short](includes/prod_short.md)] úthlutar sjálfkrafa VSK-viðskiptabókunarflokkinum þegar þú úthlutar viðskiptabókunarflokki til viðskiptamanns, lánardrottins eða fjárhagsreiknings.

## <a name="set-up-vat-product-posting-groups"></a>Uppsetning VSK-vörubókunarflokka

VSK-vörubókunarflokkar tákna þær vörur og tilföng sem þú kaupir eða selur, og ákvarða hvernig skal reikna út og bóka VSK eftir tegund vöru eða tilfangs sem eru keypt eða seld.  
Góð regla er að nota kóða sem auðvelt er að muna og lýsa taxtanum, eins og **ÁN-VSK** eða **Núll**, **VSK10** eða **Skertur** fyrir 10% VSK, og **VSK25** eða **Staðlað** fyrir 25%.

Til að setja upp VSK-viðskiptabókunarflokk er þessu skrefum fylgt:

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar 4.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **VSK-vörubókunarflokk** og velja síðan viðkomandi tengil.  
2. Fyllið inn reitina eftir þörfum.

## <a name="combine-vat-posting-groups-in-vat-posting-setups"></a>Sameina VSK-bókunarflokka í VSK bókunaruppsetningar

[!INCLUDE[prod_short](includes/prod_short.md)] reiknar VSK-upphæðir í sölu og innkaup á grundvelli VSK-bókunaruppsetninga, sem eru samsetningar VSK-viðskipta- og vörubókunarflokka. Fyrir hverja samsetningu geturðu valið VSK-prósenta, VSK-útreikningstegund, og fjárhagsreikninga fyrir bókun VSK sem tengist sölu, innkaupum, og bakfærðum gjöldum. Einnig er hægt að tilgreina hvort endurreikna skal VSK þegar greiðsluafsláttur er veittur eða fenginn.  

Hægt er að setja upp ótakmarkaðan fjölda samsetninga. Ef flokka á saman samsetningar VSK-bókunaruppsetninga með svipaða eiginleika, er hægt að tilgreina **Kennimerki VSK** fyrir hvern flokk og úthluta kenninu til flokksmeðlimanna.

Til að sameina VSK-bókunaruppsetningar skal fylgja eftirfarandi skrefum:

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar 5.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **VSK-bókunargrunnur** og velja síðan viðkomandi tengil.
2. Fyllið inn reitina eftir þörfum. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

## <a name="assign-vat-posting-groups-by-default-to-multiple-entities"></a>Úthluta VSK-bókunarflokkum sjálfgefið á margar einingar

Eigi að beita sömu VSK-bókunarflokkum á fjölda eininga, er hægt að setja upp [!INCLUDE[prod_short](includes/prod_short.md)] sem gerir það sjálfvirkt. Hægt er að gera þetta á tvennan hátt:

* Hægt er að úthluta VSK-viðskiptabókunarflokkum til almennra viðskiptabókunarflokka eða sniðmáts viðskiptamanns eða lánardrottins
* Hægt er að úthluta VSK-vörubókunarflokkum til almennum vörubókunarflokkum  

VSK-viðskipta- eða vörubókunarflokki er úthlutað þegar valið er viðskipta- eða vörubókunarflokki fyrir viðskiptamann, lánardrottinn, vöru eða tilföng.

## <a name="assign-vat-posting-groups-to-accounts-customers-vendors-items-and-resources"></a>Tengja VSK-bókunarflokka við lykla, viðskiptamenn, lánardrottna, vörur og forða

Eftirfarandi hlutar útskýra hvernig á að úthluta VSK-bókunarflokkum til einstakra einingar.

### <a name="to-assign-vat-posting-groups-to-individual-general-ledger-accounts"></a>Hvernig á að úthluta VSK-bókunarflokkum til einstakra fjárhagsreikninga

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar 6.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Bókhaldslykill** og velja síðan viðkomandi tengil.  
2. Opna **Fjárhagsreikningur** spjaldið fyrir reikninginn.  
3. Á **Bókun** Flýtiflipanum, í **Alm. bókunartegund** reitnum, er valið annaðhvort **Sölu** eða **Innkaupa**.  
4. Velja skal VSK-bókunarflokkana til að nota fyrir sölureikninginn eða kaupreikninginn.  

### <a name="to-assign-vat-business-posting-groups-to-customers-and-vendors"></a>Að úthluta VSK-viðskiptabókunarflokkum til viðskiptamenn og lánardrottna.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar 7.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Viðskiptavinur** eða **Lánardrottinn** og velja síðan viðkomandi tengil.  
2. Á **Viðskiptamaður** eða **Lánardrottinn** spjaldinu, víkið flýtiflipann **Reikningar**.  
3. Veljið VSK-viðskiptabókunarflokkana.  

### <a name="to-assign-vat-product-posting-groups-to-individual-items-and-resources"></a>Til að úthluta VSK-vörubókunarflokkar til einstakra vörur og tilföng.

1. Veldu þá ![ljósaperu sem opnast Segðu mér lögun 8.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Vara** eða **Tilfang** og velja síðan viðkomandi tengil.  
2. Gert er eitt af eftirfarandi:  

    * Á **Vöru** spjaldinu, stækkið **Verð & Bókun** Flýtiflipann, og velja síðan **Sýna fleiri** til að birta **VAT Vörubókunarflokkur** reitinn.  
    * Á **Tilfang** spjaldinu, stækkið **Reikningagerð** flipann.  
3. Veljið VSK-vörubókunarflokk.  

## <a name="set-up-clauses-to-explain-vat-exemption-or-non-standard-vat-rates"></a>Setja upp ákvæði til að útskýra VSK undanþegna eða óstaðlaða VSK-taxta

VSK-klausa er sett upp til að lýsa upplýsingum um hvaða tegund VSK er notuð. Reglur stjórnvalda gætu krafist þessara upplýsinga. Þegar búið er að setja upp VSK-ákvæði og tengja það við VSK-bókunaruppsetningu, birtist VSK-ákvæðið á öllum prentuðum söluskjölum sem nota VSK-bókunaruppsetningarflokkinn.

Ef með þarf er einnig hægt að tilgreina hvernig skal þýða VSK ákvæði yfir á öðrum tungumálum. Þegar söluskjal sem inniheldur VSK-kenni er stofnað og prentað, mun skjalið innihalda VSK-ákvæðið sem var þýtt. Tilgreindur tungumálakóðinn á viðskiptamannaspjaldinu ákvarðar tungumálið.

Þegar óhefðbundin VSK-hlutföll eru notuð í mismunandi skjalagerðum, t.d. reikningum eða kreditreikningum, er venjulega krafist þess að fyrirtæki láti undanþágutexta (VSK-klausu) fylgja með til að útskýra af hverju minni virðisaukaskattur eða enginn virðisaukaskattur hefur verið reiknaður. Hægt er að skilgreina mismunandi VSK-klausur til að hafa með í viðskiptaskjölum eftir gerð skjals, t.d. reikningur eða kreditreikningur. Þetta er gert á síðunni **VSK-klausur eftir skjalagerð**.

Hægt er að breyta eða eyða VSK-klausu og þá birtast breytingarnar í myndaðri skýrslu. [!INCLUDE[prod_short](includes/prod_short.md)] geymir hins vegar breytingasöguna. Í skýrslunni eru VSK-klausulýsingar prentaðar og birtar fyrir allar línur í skýrslunni ásamt VSK-upphæðinni og upphæð VSK-stofnsins. Ef VSK-klausa hefur ekki verið skilgreind fyrir neinar línur í söluskjalinu er öllum hlutanum sleppt þegar skýrslan er prentuð.

### <a name="to-set-up-vat-clauses"></a>Að setja upp VSK-ákvæði

1. Veldu þá ![ljósaperu sem opnast Segðu mér lögun 9.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **VSK-ákvæði** og velja síðan viðkomandi tengil.  
2. Á **VSK ákvæði** síðunni, skal búa til nýja línu.  
3. Í reitnum **Kóði** er auðkenni ákvæðisins slegið inn. Þessi kóði er notuð til að úthluta ákvæðinu á VSK-bókunarflokka.  
4. Í reitnum **Lýsing** er færður inn texti VSK-undanþágu sem þú vilt að birtist á fylgiskjölum sem geta innihaldið VSK. **Í reitinn Lýsing 2** er ritaður meiri texti ef þörf krefur. Textinn verður sýndur á nýjum skjalalínum.
5. Veldu aðgerðina **Lýsing eftir gerð skjals**.
6. Á síðunni **VSK-klausur eftir skjalagerð** skal fylla í reitina til að setja upp hvaða texta VSK-undanþágu á að birta fyrir hvaða skjalagerð.  
7. Valfrjálst: Til að úthluta VSK-ákvæði til VSK-bókunaruppsetningar strax, veljið **Uppsetning**, og velja síðan ákvæðið. Ef þú vilt bíða, er hægt að úthluta ákvæðinu síðar á síðunni **VSK-Bókunaruppsetning**.  
8. Valfrjálst: Til að tilgreina hvernig skal þýða VSK-ákvæðið er **Þýðingar** aðgerðin valin.

### <a name="to-assign-a-vat-clause-to-a-vat-posting-setup"></a>Til að úthluta VSK-ákvæði til VSK-bókunaruppsetningar

1. Veldu þá ![ljósaperu sem opnast Segðu mér lögun 10.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **VSK-bókunargrunnur** og velja síðan viðkomandi tengil.  
2. Í dálkinum **VSK-Ákvæði** skal velja ákvæðið sem nota á fyrir hvert VSK-bókunaruppsetningu sem það á við um.  

### <a name="to-specify-translations-for-vat-clauses"></a>Að tilgreina þýðingar fyrir VSK-ákvæði

1. Veldu þá ![ljósaperu sem opnast Segðu mér lögun 11.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **VSK-ákvæði** og velja síðan viðkomandi tengil.  
2. Veljið aðgerðina **Þýðingar**.  
3. Í reitnum **Tungumálakóði** skal velja tungumál sem þýtt er yfir á.  
4. Í reitunum **Lýsing** og **Lýsing 2** eru færðar inn þýðingar á lýsingunum. Þessi texti er birtur í þýddum VSK-skýrsluskjölum.  

## <a name="create-a-vat-posting-setup-to-handle-import-vat"></a>Stofna VSK-bókunaruppsetningu til að sjá um VSK af innflutningi

Aðgerðin innflutningur VSK *er notuð* þegar bóka þarf skjal þar sem öll UPPHÆÐIN er VSK. Þetta þarf að gera ef reikningur kemur frá skattyfirvöldum fyrir VSK á innfluttar vörur.  

Til að setja upp kóða fyrir VSK vegna innflutnings, skal fylgja þessum skrefum:  

1. Veldu þá ![ljósaperu sem opnast Segðu mér lögun 12.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **VSK-vörubókunarflokk** og velja síðan viðkomandi tengil.  
2. Á síðunni VSK-vörubókunarflokkar, skal setja upp nýja VSK-vörubókunarflokkur fyrir VSK vegna innflutnings.  
3. Veldu þá ![ljósaperu sem opnast Segðu mér lögun 13.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **VSK-bókunargrunnur** og velja síðan viðkomandi tengil.  
4. Á síðunni VSK-bókunaruppsetning skal stofna nýja lína, eða nota VSK-viðskiptabókunarflokk sem fyrir er í samsetningu með nýja VSK-vörubókunarflokknum fyrir VSK vegna innflutnings.  
5. Í reitnum **SK-Útreikningstegund** skal velja **Fullur VSK**.  
6. Í **VSK-sölureikningur** reitinn skal færa inn fjárhagsreikningurinn sem á að nota til að bóka VSK vegna innflutnings. Allir aðrir reikninga eru valfrjáls.  

## <a name="use-reverse-charge-vat-for-trade-between-eu-countries-or-regions"></a>Nota bakfærðan VSK fyrir viðskipti milli ESB-landa eða svæða

Sum fyrirtæki verða að nota bakfærðan VSK þegar þau eiga viðskipti við önnur fyrirtæki. Reglan gildir til dæmis fyrir innkaup frá ESB-löndum/svæðum og sölu til ESB-landa/svæða.  

> [!NOTE]  
> Þessi regla á við þegar skipt er við fyrirtæki sem eru skráð VSK-skyld í öðrum ESB-löndum/svæðum. Ef skipt er beint við viðskiptamenn í öðrum ESB-löndum/svæðum ætti að hafa samband við skattayfirvöld til að fá upplýsingar um viðeigandi VSK-reglur.  

> [!TIP]  
> Þú getur staðfest að fyrirtæki sé skráð VSK-skylt í öðru ESB-landi með því að nota ESB staðfestingarþjónustu VSK-númera. Þjónustan er tiltæk án endurgjalds í [!INCLUDE[prod_short](includes/prod_short.md)]. Sjá [SANNREYNA VSK-númer](finance-how-validate-vat-registration-number.md) til að fá frekari upplýsingar.

### <a name="sales-to-eu-countries-or-regions"></a>Sala til ESB-landa eða svæða

VSK er ekki reiknaður á sölu til VSK-skyldra fyrirtækja í öðrum ESB-löndum/svæðum. Tilkynna þarf virði sölu til ESB-landa/svæða sérstaklega á VSK-yfirlitinu.  

Til að reikna VSK rétt fyrir sölu til ESB-landa/ svæða ætti að:  

* Setja upp línu fyrir sölu með sömu upplýsingum fyrir innkaup. Ef línur eru þegar uppsettar í glugganum VSK-bókunargrunnur fyrir innkaup frá ESB-löndum/-svæðum er einnig hægt að nota línurnar fyrir sölu.  
* Úthluta VSK-viðskiptabókunarflokkunum í reitnum **VSK viðsk.bókunarflokkur** á flýtiflipanum **Reikningar** í viðskiptamannaspjöldum ESB-viðskiptamanna. Einnig ætti að færa inn VSK-númer viðskiptamannsins í reitnum **VSK-númer** á flýtiflipanum **Erlent**.  

Þegar sala til viðskiptamanns í öðru ESB-landi/svæði er bókuð er VSK-upphæðin reiknuð og VSK-færsla með upplýsingum um bakfærðan VSK og VSK-stofn (upphæðina sem notuð er til að reikna VSK-upphæðina) stofnuð. Engar færslur eru bókaðar í VSK-reikningana í fjárhagnum.

## <a name="vat-rounding-for-documents"></a>Sléttun VSK fyrir skjöl

Upphæðir í fylgiskjölum sem ekki hafa verið bókaðar eru sléttaðar og birtar á þann hátt sem samsvarar lokasléttun upphæða sem búið er að bóka. VSK er reiknaður fyrir heilt skjal, sem þýðir að VSK sem er reiknaður í fylgiskjali er byggður á summu allra lína með sama VSK-kenni í skjalinu.  

## <a name="set-up-vat-reporting"></a>Setja upp VSK-skýrslugerð

Setja þarf upp upplýsingar um hvernig skattyfirvöld í landi eða svæði þurfa að senda VSK-skýrslur. Eftirfarandi skref sýna þær upplýsingar sem oftast eru notaðar. Hins vegar gæti landið eða svæðið þurft Viðbótarskref. Nánari upplýsingar er að finna í viðkomandi grein í *kaflanum staðbundnu virknikaflar* í Panel til vinstri.

[!INCLUDE [vat-report-setup](includes/vat-report-setup.md)]

## <a name="see-also"></a>Sjá einnig

[Uppsetning sniðmáta VSK-yfirlits og heiti VSK-yfirlits](finance-how-setup-vat-statement.md)  
[Uppsetning á óinnleystum virðisaukaskatti](finance-setup-unrealized-vat.md)  
[Senda VSK skýrslu inn til skattayfirvalda](finance-how-report-vat.md)  
[Unnið með VSK í sölu og innkaupum](finance-work-with-vat.md)  
[Vinna með Breytingarverkfæri VSK-hlutfalls](finance-how-use-vat-rate-change-tool.md)  
[Staðfesta VSK-skráningarnúmer](finance-how-validate-vat-registration-number.md)  
[Staðbundin virkni í Business Central](about-localization.md)  

## <a name="see-related-training-at-microsoft-learn"></a>Sjá tengda þjálfun á [Microsoft Learn](/learn/paths/process-vat-dynamics-365-business-central/)


[!INCLUDE[footer-include](includes/footer-banner.md)]
