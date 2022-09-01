---
title: Setja upp virðisaukaskatt
description: Ganga úr skugga um að rétt reikna, bóka, og tilkynna á VSK vegna sölu eða innkaup. Mælt er með að nota uppsetningarleiðsögn til að setja upp VSK.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: VAT, posting, tax, value-added tax
ms.search.form: 10, 391, 470, 471, 472, 575, 734, 747, 748, 1877,
ms.date: 07/08/2022
ms.author: bholtorf
ms.openlocfilehash: e0703d6dfccc2ec97213c89f42b8d74b3d320e1c
ms.sourcegitcommit: 38b1272947f64a473de910fe81ad97db5213e6c3
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/29/2022
ms.locfileid: "9361583"
---
# <a name="set-up-calculations-and-posting-methods-for-value-added-tax"></a>Uppsetning fyrir útreikning og bókunaraðferðir virðisaukaskatts

Neytendur og fyrirtæki greiða virðisaukaskatt (VSK) þegar þau kaupa vörur eða þjónustu. Upphæð VSK til greiðslu getur verið mismunandi, það fer eftir nokkrum þáttum. Í [!INCLUDE[prod_short](includes/prod_short.md)] er settur upp VSK til að tilgreina gjaldmiðla sem eru notaðir til að reikna skattupphæðir, sem byggðar eru á eftirfarandi færibreytum:

* Hverjum selt er  
* Hverjum keypt er af  
* Það sem er selt  
* Hvað keypt er  

Hægt er að setja upp VSK-útreikninga handvirkt en það getur verið erfiður og tímafrekann. Það er vegna þess að mjög auðvelt er að nota VSK-taxta fyrir mistök og búa til rangar skýrslur um VSK-tengdar. Ef gera á uppsetningu á VSK auðveldari er mælt með því að nota leiðbeiningar um **VSK** sem fylgja í afurðin. 

Ef þú vilt hins vegar setja upp VSK-útreikninga sjálfur eða vilt bara fá upplýsingar um hvert skref er þessi grein að finna lýsingar á hverju þrepi:  

[!INCLUDE [finance-vat](includes/finance-vat.md)]

## <a name="set-up-vat-using-the-assisted-vat-setup-guide-recommended"></a>VSK er settur upp með uppsetningarleiðbeiningum með VSK (ráðlegt > 

> [!NOTE]
> Aðeins er hægt að **nota VSK-Uppsetningarleiðbeiningarnar** ef fyrirtæki *mitt hefur verið stofnað og ekki hafa enn verið bókaðar færslur sem FELA í* sér VSK.

Til að ræsa uppsetningleiðbeiningar með hjálp, fylgið þessum skrefum:

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar 1.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknið og færa inn **aðstoðar uppsetningu**. 
2. Valið **er setja upp virðisauka (VAT)** og ljúka við skrefin.
3. Þegar uppsetningu aðstoðar er lokið er farið á **síðuna VSK-bókunargrunnur** til að kanna hvort fylla þurfi í fleiri reiti samkvæmt staðbundnum kröfum í útgáfunni af [!INCLUDE [prod_short](includes/prod_short.md)]. Frekari upplýsingar á [staðbundinni virkni í Aðalstarfsemi](about-localization.md).  

### <a name="check-the-vat-posting-setup"></a>Athuga skal VSK-bókunaruppsetninguna

Til að styðja ræsingu á byrjun [!INCLUDE [prod_short](includes/prod_short.md)] lætur þú vita um þann sem vantar fjárhag (fjárhags-) reikninga í bókunarflokkum eða bókunaruppsetningar, eins og á **síðunni VSK bókunaruppsetning**. Hægt er að gera þessa gerð tilkynningar óvirkt með því að nota *fjárhagsreikning vantar í bókunarflokk eða tilkynningu í uppsetningu* á **síðunni tilkynningar**. Farðu **bara á síðuna stillingarnar** og veldu *svo breytinguna þegar ég fæ tilkynningar.* .  

Ef slík tilkynning er valin, [!INCLUDE [prod_short](includes/prod_short.md)] stofnar sjálfkrafa þær bókunaruppsetningar sem eru byggðar á bókunarflokkum í skjalinu eða færslubókinni sem verið er að vinna að.  

Á þessum tímapunkti er bara hægt að fylla út reitina sem vantar. En síðar, þegar uppsetningin er ítarlegri, mætti gera grein fyrir því að Upphafleg Uppsetning er röng. Og [!INCLUDE [prod_short](includes/prod_short.md)] leyfir ekki EYÐINGU VSK-bókunaruppsetningar og almennrar bókunaruppsetningar þegar færslur hafa verið stofnaðar á grundvelli slíkra afbrigða. Svo að byrja í 2022 1. gr. er hægt að nota **reitinn lokaður** á **uppsetningarsíðu** VSK-bókunar til að koma í veg fyrir að notendur hafi rangt með uppsetningu sem tengist ekki lengur nýjum bókunum.

## <a name="set-up-vat-registration-numbers-for-your-country-or-region"></a>Setja upp VSK-númer fyrir land eða svæði

Til að hjálpa fólki að færa inn gild VSK-númer er hægt að skilgreina snið VSK-númeranna sem eru notuð í þeim löndum eða svæðum sem fyrirtæki á í viðskiptum við. [!INCLUDE[prod_short](includes/prod_short.md)] birtast villuboð ef einhver gerir mistök eða notar snið sem er rangt fyrir landið eða svæðið.

Til að setja upp VSK-númer skal fylgja eftirfarandi skrefum:

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar 2.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Lönd/svæði**.
2. Velja skal landið eða svæðið og svo agðerðina **Snið VSK-númers**.
3. Í reitnum **Snið** skal skilgreina sniðin með því að slá inn einn eða fleiri eftirfarandi stafa:  

* **#** Krefst númers sem er ein tala.  
* **@** Krefst stafs. Þetta snið er ekki Stafrétt.  
* **?** Leyfir hvaða staf sem er.  

    > [!TIP]
    > Hægt er að nota þessa stafi svo framarlega sem þeir eru alltaf til staðar í sniði landsins eða svæðisins. Þannig að ef þú þarft að taka með tímabil eða hyphen á milli stæða er hægt að skilgreina sniðið sem # #. # # # #. # # # eða @ @-# # #-# #.  

## <a name="set-up-vat-business-posting-groups"></a>Uppsetning VSK-viðskiptabókunarflokka

VSK-viðskiptabókunarflokkar á að tákna markaðina þar sem þú stundar viðskiptum við viðskiptamenn og lánardrottna, og tilgreina hvernig á að reikna og bóka VSK á sérhverjum markaði. Dæmi um VSK viðskiptabókunarflokka eru **Innanlands** og **Evrópusambandið (ESB)**.  

Nota skal kóða sem auðvelt er að muna og er auðkennandi fyrir viðskiptaflokkinn, til dæmis **ESB**, **Ekki-ESB**, eða **Innlent**. Hver Kóði verður að vera Einkvæmur, merkir að hægt er að setja upp eins marga kóta og þörf er á en ekki er hægt að hafa sama kótann oftar en einu sinni í töflu.

Til að setja upp VSK-viðskiptabókunarflokk er þessu skrefum fylgt:

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar 3.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknið, færa inn **VSK-viðskiptabókunarflokka** og velja síðan tengda tengilinn.  
2. Fyllið inn reitina eftir þörfum.

Hægt er að setja upp sjálfgefna VSK-viðskiptabókunarflokka með því að tengja þá við almenna viðskiptabókunarflokka. [!INCLUDE[prod_short](includes/prod_short.md)] úthlutar sjálfkrafa VSK-viðskiptabókunarflokkinum þegar þú úthlutar viðskiptabókunarflokki til viðskiptamanns, lánardrottins eða fjárhagsreiknings.

## <a name="set-up-vat-product-posting-groups"></a>Uppsetning VSK-vörubókunarflokka

VSK-vörubókunarflokkar tákna vörurnar og tilfang sem er keypt eða Selt og ákvarða hvernig á að reikna og bóka VSK eftir gerð vörunnar eða forðunarinnar.

Gott ráð er að nota kóta sem auðvelt er að muna og lýsa hlutfallinu, svo sem **Nei-VAT** eða **núll**, **VAT10** eða **lækka** í 10 prósenta VSK og **VAT25** eða **staðalinn** fyrir 25 prósent.

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

VSK-klausa er sett upp til að lýsa upplýsingum um hvaða tegund VSK er notuð. Upplýsingarnar kunna að vera nauðsynlegar samkvæmt reglum stjórnvalda. Þegar búið er að setja upp VSK-ákvæði og tengja það við VSK-bókunaruppsetningu, birtist VSK-ákvæðið á öllum prentuðum söluskjölum sem nota VSK-bókunaruppsetningarflokkinn.

Ef með þarf er einnig hægt að tilgreina hvernig skal þýða VSK ákvæði yfir á öðrum tungumálum. Þegar söluskjal sem inniheldur VSK-kenni er stofnað og prentað, mun skjalið innihalda VSK-ákvæðið sem var þýtt. Tilgreindur tungumálakóðinn á viðskiptamannaspjaldinu ákvarðar tungumálið.

Þegar óhefðbundin VSK-hlutföll eru notuð í mismunandi skjalagerðum, t.d. reikningum eða kreditreikningum, er venjulega krafist þess að fyrirtæki láti undanþágutexta (VSK-klausu) fylgja með til að útskýra af hverju minni virðisaukaskattur eða enginn virðisaukaskattur hefur verið reiknaður. Hægt er að skilgreina mismunandi VSK-klausur til að hafa með í viðskiptaskjölum eftir gerð skjals, t.d. reikningur eða kreditreikningur. Það er gert **í VSK-ákvæðum eftir tegund** fylgiskjals.

Hægt er að breyta eða eyða VSK-klausu og þá birtast breytingarnar í myndaðri skýrslu. [!INCLUDE[prod_short](includes/prod_short.md)] geymir hins vegar breytingasöguna. Í skýrslunni eru VSK-klausulýsingar prentaðar og birtar fyrir allar línur í skýrslunni ásamt VSK-upphæðinni og upphæð VSK-stofnsins. Ef VSK-klausa hefur ekki verið skilgreind fyrir neinar línur í söluskjalinu er öllum hlutanum sleppt þegar skýrslan er prentuð.

### <a name="to-set-up-vat-clauses"></a>Að setja upp VSK-ákvæði

1. Veldu þá ![ljósaperu sem opnast Segðu mér lögun 9.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **VSK-ákvæði** og velja síðan viðkomandi tengil.  
2. Á **VSK ákvæði** síðunni, skal búa til nýja línu.  
3. Í reitnum **Kóði** er auðkenni ákvæðisins slegið inn. Þessi kóði er notuð til að úthluta ákvæðinu á VSK-bókunarflokka.  
4. Í reitnum **Lýsing** er færður inn texti VSK-undanþágu sem þú vilt að birtist á fylgiskjölum sem geta innihaldið VSK. **Í reitinn Lýsing 2** er ritaður meiri texti ef þörf krefur. Textinn verður sýndur á nýjum skjalalínum.
5. **Velja lýsinguna eftir aðgerð skjalgerðar**.
6. **Á síðunni VSK-ákvæði eftir tegund** fylgiskjals er fyllt í reitina til að setja upp hvaða VSK-undanþágutexta á að birta sem skjalagerð.  
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

### <a name="to-specify-extended-text-for-vat-clauses"></a>Lengdur texti tilgreindur fyrir VSK-ákvæði

> [!NOTE]  
> Ef land eða svæði þess þarf lengri texta fyrir VSK-ákvæði en sjálfgefnu útgáfuna er hægt að tilgreina lengri texta fyrir VSK-ákvæði sem *lengri texta* svo að hann prenti í sölu-og innkaupaskýrslum.  

1. Veldu þá ![ljósaperu sem opnast Segðu mér lögun 11.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **VSK-ákvæði** og velja síðan viðkomandi tengil.  
2. Velja skal aðgerðina fyrir **lengda texta**.  
3. Valið er aðgerðin **Nýtt**.  
4. Reitirnir Kóti **tungumáls og** Lýsing **eru** fylltir út.  
5. Hægt er að **velja kóta** allra tungumálskóta eða tilgreina viðeigandi tungumál í **reitnum Tungumálskóti** ef tungumálakótar eru notaðir.  
6. Reitirnir **Upphafsdagsetning** og **Lokadagsetning** eru fylltir út ef afmarka á tímabil fyrir lengdan texta.  
7. **Skrifa lengdan texta fyrir VSK-ákvæði í textalínur**.  
8. Veljið viðeigandi reiti fyrir fylgiskjalstegundum þar sem prenta á lengda textann.  
9. Loka síðunni.  

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

Sum fyrirtæki verða að nota bakfærðan VSK þegar þau eiga viðskipti við önnur fyrirtæki. Þessi regla gildir til dæmis um innkaup frá ESB löndum/svæðum og sölu til ESB-landa/-svæða.  

> [!NOTE]  
> Þessi regla á við þegar skipt er við fyrirtæki sem eru skráð VSK-skyld í öðrum ESB-löndum/svæðum. Ef skipt er beint við viðskiptamenn í öðrum ESB-löndum/svæðum ætti að hafa samband við skattayfirvöld til að fá upplýsingar um viðeigandi VSK-reglur.  

> [!TIP]  
> Þú getur staðfest að fyrirtæki sé skráð VSK-skylt í öðru ESB-landi með því að nota ESB staðfestingarþjónustu VSK-númera. Þjónustan er tiltæk án endurgjalds í [!INCLUDE[prod_short](includes/prod_short.md)]. Sjá [SANNREYNA VSK-númer](finance-how-validate-vat-registration-number.md) til að fá frekari upplýsingar.

### <a name="sales-to-eu-countries-or-regions"></a>Sala til ESB-landa eða svæða

VSK er ekki reiknaður á sölu til VSK-skyldra fyrirtækja í öðrum ESB-löndum/svæðum. Tilkynna þarf virði sölu til ESB-landa/svæða sérstaklega á VSK-yfirlitinu.  

Til að reikna VSK rétt fyrir sölu til ESB-landa/ svæða ætti að:  

* Setja upp línu fyrir sölu með sömu upplýsingum fyrir innkaup. Ef línur hafa þegar verið settar upp á **uppsetningarsíðu** VSK vegna INNKAUPA frá ESB löndum/svæðum þá er einnig hægt að nota þessar línur til sölu.  
* Úthluta VSK-viðskiptabókunarflokkunum í reitnum **VSK viðsk.bókunarflokkur** á flýtiflipanum **Reikningar** í viðskiptamannaspjöldum ESB-viðskiptamanna. Einnig ætti að færa inn VSK-númer viðskiptamannsins í reitnum **VSK-númer** á flýtiflipanum **Erlent**.  

Þegar sala til viðskiptamanns í öðru ESB-landi/svæði er bókuð er VSK-upphæðin reiknuð og VSK-færsla með upplýsingum um bakfærðan VSK og VSK-stofn (upphæðina sem notuð er til að reikna VSK-upphæðina) stofnuð. Engar færslur eru bókaðar í VSK-reikningana í fjárhagnum.

## <a name="vat-rounding-for-documents"></a>Sléttun VSK fyrir skjöl

Upphæðir í fylgiskjölum sem ekki hafa verið bókaðar eru sléttaðar og birtar á þann hátt sem samsvarar lokasléttun upphæða sem búið er að bóka. VSK er reiknaður fyrir heilt skjal, sem þýðir að VSK sem er reiknaður í fylgiskjali er byggður á summu allra lína með sama VSK-kenni í skjalinu.  

## <a name="set-up-vat-reporting"></a>Setja upp VSK-skýrslur

Setja þarf upp upplýsingar um hvernig skattyfirvöld í landi eða svæði þurfa að senda VSK-skýrslur. Eftirfarandi skref sýna þær upplýsingar sem oftast eru notaðar. Hins vegar gæti viðkomandi land eða svæði þarfnast annarra skrefa. Nánari upplýsingar er að finna í viðkomandi grein í *kaflanum staðbundnu virknikaflar* í Panel til vinstri.

[!INCLUDE [vat-report-setup](includes/vat-report-setup.md)]

## <a name="see-related-training-at-microsoft-learn"></a>Sjá tengdar þjálfun hjá [Microsoft Learn](/learn/paths/process-vat-dynamics-365-business-central/)

## <a name="see-also"></a>Sjá einnig .

[Setja upp sniðmát VSK-yfirlits og heiti VSK-yfirlits](finance-how-setup-vat-statement.md)  
[Setja upp óinnleystan virðisauka](finance-setup-unrealized-vat.md)  
[Senda VSK skýrslu inn til skattayfirvalda](finance-how-report-vat.md)  
[Unnið með VSK í sölu og innkaupum](finance-work-with-vat.md)  
[Vinna með Breytingarverkfæri VSK-hlutfalls](finance-how-use-vat-rate-change-tool.md)  
[Staðfesta VSK-skráningarnúmer](finance-how-validate-vat-registration-number.md)  
[Staðbundin virkni í Business Central](about-localization.md)  
[VSK-skýrsla í þýsku útgáfunni](LocalFunctionality/Germany/vat-reporting.md)  
[Belgískur VSK](LocalFunctionality/Belgium/belgian-vat.md)  
[Ítalskur VSK](LocalFunctionality/Italy/italian-vat.md)  
[Setja upp rafrænar VSK-og ICP-skýrslur í hollensku útgáfunni](LocalFunctionality/Netherlands/how-to-set-up-electronic-vat-and-icp-declarations.md)  
[VSK-skýrslur í spænsku útgáfunni](LocalFunctionality/Spain/vat-reports.md)  
[Setja upp VSK fyrir vöru og þjónustu í áströlsku útgáfunni](LocalFunctionality/Australia/how-to-set-up-goods-and-service-tax-posting.md)  
[VSK í tékknesku útgáfunni](LocalFunctionality/Czech/finance-vat.md)  
[VSK-skýrsla í norsku útgáfunni](LocalFunctionality/Norway/norwegian-vat-reporting.md)  
[Skrá yfir vöru/þjónustuskatt og Samræmddur Virðisaukaskattur í Kanada](LocalFunctionality/Canada/sales-tax-goods-services.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
