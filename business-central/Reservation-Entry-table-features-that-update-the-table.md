---
title: Taflan Frátekningarfærsla - Aðgerðir sem uppfæra töfluna Frátekningarfærsla | Microsoft-skjöl
description: Þetta veitir leiðbeiningar til að aðstoða við að skilja og leysa úr vandamálum með ósamræmi í gögnum í töflunni Frátekningarfærsla.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 06/26/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

# Taflan Frátekningarfærsla - Kynning

Þessi tæknilega hvítpappír veitir leiðbeiningar til að aðstoða notanda við að skilja og leysa úr vandamálum með ósamræmi í gögnum í *töflunni Frátekningarfærsla* (Tafla 337) í [!INCLUDE[prod_short](includes/prod_short.md)]. Fyrri hlutinn er kynning á aðgerðum sem mynda eða breyta gögnum í þessari töflu. Hún fjallar einnig um nokkra reiti í *töflunni Frátekningarfærsla* sem vert er að benda á í tengslum við þessar aðgerðir. Seinni hlutinn sýnir með dæmum hvernig færslur í *töflunni Frátekningarfærsla* eru myndaðar, þeim eytt eða þeim breytt þegar millifærslupantanir eru unnar eða áætlunaraðgerðir eru framkvæmdar.

Taflan *Frátekningarfærsla* er notuð til að vinna með og geyma upplýsingar um frátekningu, vörurakningu og pöntunarrakningu.

Þegar fengist er við vörurakningu með hlutabókun vinnur taflan ásamt *töflunni Rakningarlýsing* (Tafla 336). Gögn sem notandinn færir inn á síðunni **Vörurakningarlínur** eru stofnuð í bráðabirgðaútgáfu af töflunni 336 og lögð í töflu 337 og rakningarlýsingartöflu þegar síðunni er lokað.

Almennt fer gögnin sem mynduð eru í *töflunni Frátekningarfærsla* eftir því hvaða eiginleikar eru notaðir og hvaða færibreytur voru valdar á birgðaspjaldinu. Þar á meðal eru:

- Rakningarstefna pöntunar
- Frátekningarregla
- Áætlunaraðgerðir framkvæmdar
- Endurpöntunar- og framleiðslustefna
- Áætlunarfæribreytur á birgða- eða birgðaeiningarspjaldinu
- Vörurakningarkóði

## Aðgerðir sem uppfæra töfluna Frátekningarfærsla

### Rakningarstefna pöntunar

Ef reiturinn **Rakningarstefna** pöntunar á vöru er stilltur á Ekkert [!INCLUDE[prod_short](includes/prod_short.md)]  stofnar aldrei frátekningarfærslur í *töflunni Frátekningarfærsla* nema áætlun hreyfingar eða Endurgerðaráætlun, Frátekning eða Vörurakning sé framkvæmd. Þar að auki er hægt að taka frá færslur án pantanarakningar þegar reglur um Framleiðsla og Samsetning eftir pöntun eru notaðar.

Hægt er að íhuga að stilla **rakningarstefnu** pöntunar á Ekkert ef ekki er krafist rakningar á fljúgandi eftirspurn gegn framboði eða öfugt. Rakning framboðs á móti eftirspurn er unnin með pöntunarrakningaraðgerðinni eða áætlunarvélinni. Ekki er mælt með því að pantanarakning sé notuð með áætlunaraðgerðum.

Þegar reiturinn **Rakningaraðferð** pöntunar er stilltur á Aðeins [!INCLUDE[prod_short](includes/prod_short.md)]  rakning, stofnar alltaf færslur í töflu 337 þegar pöntun er stofnuð fyrir vöruna, en **Staða** frátekningar í töflu 337 er ekki alltaf stranglega stillt á Rakning. Íhuga skal eftirfarandi dæmi:

> [!NOTE]  
> Vinnudagsetningin er stillt sem 01/23/2014 (MM/DD/ÁÁÁÁ) fyrir öll dæmi. 
  
1. Stofna vöru með **reitinn Rakningarregla** pöntunar stillta á Aðeins rakningu.  
1. Stofna innkaupapöntun. [!INCLUDE[prod_short](includes/prod_short.md)] stofnar frátekningarfærslu með **Frátekningarstöðu** umfram þar sem innkaupapöntuninni er ekki enn úthlutað eftirspurn.
1. Stofnið sölupöntun. [!INCLUDE[prod_short](includes/prod_short.md)] stofnar nú aðra frátekningarfærslu með **frátekningarstöðu** rakningar.

 **Staða** frátekningar sem stofnuð er í 2. lið verður uppfærð í Rakning, hún er afgreidd sjálfvirkt [!INCLUDE[prod_short](includes/prod_short.md)] . Þetta hugtak heitir Kvik rakning.
Með því að setja reitinn **Rakningarstefna** pöntunar á vöruna aðeins til Rakningar getur notandi notað pöntunarrakningaraðgerðina til að fá yfirlit yfir það hvaða framboð eftirspurnin er úthlutað til og öfugt.

> [!NOTE]  
> Rakningaraðgerð kemur ekki í stað áætlunaraðgerða sem tekur allar vörur, eftirspurn og birgðir saman til að bjóða upp á bestu áætlunartillögurnar til að hámarka þjónustustig viðskiptamanna og jafna birgðastig.

### Frátekningarregla

Frátekning samanstendur af pari færslna í *töflunni Frátekningarfærsla* með **frátekningarstöðu** sem deilir sama færslunúmeri. Ein færsla er með reitinn Jákvæða virka og vísar á framboðið. Hin færslan hefur reitinn **Jákvæða** ekki virkan og vísar á eftirspurnina. Reitirnir **Tegund** uppruna, **Tilv.nr.** uppruna og **Upprunakenni** auðkenna frátekninguna tengja milli eftirspurnar og framboðs.

Upplýsingarnar í reitnum **Tegund** uppruna eru taflan frátekningarfærslunr **.** reiturinn er tengdur. Ef hún er til dæmis eftirspurn (neikvæð) færsla þá gæti hún verið *taflan Sölupöntun* (Tafla 37) eða *Áætlunaríhlutur*  (tafla 99000829).

Reiturinn **Kenni** uppruna inniheldur kenni skjalsins í töflunni sem vísað er til í Tegund uppruna.

Reiturinn **Tilv.nr. uppruna** í reitnum er tilvísunarnúmer línunnar sem frátekningarfærslunr **.** er tengt við. Ef færslan er tengd sölu- eða innkaupalínu, færslubókarlínu eða innkaupatillögulínu eru upplýsingarnar í þessum reit afritaðar úr reitnum **Línunr.** . Ef hún er tengd færslu í *töflunni Birgðafærsla* (tafla 32) eru upplýsingarnar í þessum reit afritaðar úr reitnum **Færslunr.** í töflunni *Birgðafærsla* .

Þegar valkosturinn frátekningarregla er notaður Alltaf ásamt pöntunarrakningu eru báðir yfirleitt í samstillingu. Þegar frátekning er hins vegar fjarlægð eða móttökudagsetning framboðs er færð fram yfir skiladag eftirspurnar verður pöntunarrakningin fjarlægð. Einnig er hægt að finna villuboð þar sem [!INCLUDE[prod_short](includes/prod_short.md)] spyr hvað eigi að gera við fyrirliggjandi frátekningar. Þetta dæmi er útskýrt í eftirfarandi dæmi:

1. Stofna nýja vöru sem kallast COMP. Eftirfarandi reitir eru stilltir:
  - **Áfyllingarkerfið**: Innkaup
  - **Rakningarstefna** pöntunar: Aðeins rakning
  - **Taka frá**: Alltaf
2. Stofna annað atriði sem nefnist FG. Eftirfarandi reitir eru stilltir:
  - **Áfyllingarkerfið**: Framl.pöntun
  - **Rakningarstefna** pöntunar: Aðeins rakning
  - **Taka frá**: Alltaf
3. Stofna annað atriði sem nefnist FG. Eftirfarandi reitir eru stilltir:
  - **Vara**: COMP
  - **Magn á**: 1
4. Nr. framleiðsluuppskriftarinnar vottað UppskriftarFG og úthlutað á vöruFG.
5. Stofna innkaupapöntun. Eftirfarandi reitir eru stilltir:
  - **Vara**: COMP
  - **Magn**: 10
  - **Kóti** birgðageymslu: BLÁTT
  - **Áætluð móttökudagsetning**: 01/24/2014
6. Stofnið sölupöntun. Eftirfarandi reitir eru stilltir:
  - **Afhendingardagur**: 02/14/2014
  - **Kóti** birgðageymslu: BLÁTT
  - **Vara**: COMP
  - **Magn**: 10

> [!NOTE]  
> Sjálfvirk frátekning hefur verið framkvæmd milli innkaupa og sölupöntunar. Þar að auki hefur pöntunarrakning verið stofnuð milli innkaupa og sölupantana.

7. Stofna handvirka útgefna framleiðslupöntun. Eftirfarandi reitir eru stilltir:
  - **Vara**: 02/14/2014
  - **Magn**: 10
  - **Birgðageymsla**: BLÁTT
  - **Gjalddagi**: 02/01/2014
8.  **Á flipanum Heim**, í flokknum Vinnsla, skal velja **Endurnýja framleiðslupöntun**.
9. Íhlutalistinn er opnaður og flett upp VöruBIRGÐ.

> [!NOTE]  
> Engin frátekning eða pöntunarrakning er búin til af [!INCLUDE[prod_short](includes/prod_short.md)]. Ástæðan er sú að frátekning er þegar til á móti sölupöntuninni sem stofnuð var í 6. þrep.

Segjum svo, vegna viðskiptaástæðna, að brýna þurfi vöruna á útgefnu framleiðslupöntuninni sem stofnuð var í 7. þrepi. Svo næst skal í eftirfarandi skrefum hætta við frátekninguna úr sölupöntuninni sem var stofnuð í 6. þrep og takið eftir hvernig rakningu pantana er háttað.

10. Fletta upp á sölupöntuninni fyrir VÖRUSAMBAND frá 6. þrepi og hætta við frátekninguna.
11. Innkaupapöntunin er opnuð úr skrefi 5 og takið eftir að pöntunarrakningin er nú stofnuð á milli innkaupapöntunarinnar og íhlutarins sem þarf úr útgefnu framleiðslupöntuninni.
12. Frátektin er endurtekin milli íhlutarins sem þarf úr útgefnu framleiðslupöntuninni og framboðsins úr innkaupapöntuninni í 5. lið.

> [!NOTE]  
> Frátekningin er ekki endurstofnuð sem þarf að gera handvirkt.

13. Reitnum **Áætluð móttökudagsetningu** er breytt í haus innkaupapöntunar í skrefi 5 frá 01/24/2014 í 02/05/2014.

[!INCLUDE[prod_short](includes/prod_short.md)] birta eftirfarandi viðvörunarboð:

   Frátekningar eru til fyrir þessa pöntun. Hætt verður við þessar frátektir ef gagnaárekstrar stafa af þessari breytingu. Á að halda áfram?

14. Valið er Já. Fletta upp á frátekningar- og pöntunarrakningarfærslum úr innkaupapöntuninni.

> [!NOTE]  
> Hætt er við fyrirliggjandi frátekningu og það þarf að endurstýra handvirkt. Pöntunin er hins vegar kvik og hefur verið endurstofnuð með því [!INCLUDE[prod_short](includes/prod_short.md)] að vera til á milli innkaupapöntunarinnar og sölupöntunarinnar. Ástæðan er eftirspurn útgefnu framleiðslupöntunarinnar (02/01/2014) er á undan áætluðum móttökudagsetningu framboðsins.

Þetta lýkur sýningunni á samskiptunum milli þess að nota sjálfvirkar frátekningar og pöntunarrakningu. Dæmin sýna einnig hvað gerist þegar skiladegi er breytt og villuboðin sem koma af stað þegar misræmi verður í frátekningarárekstri.

### Áætlun reiknuð

Áætlanir sem gerðar eru með pantanaáætlun, innkaupatillögublaðinu eða áætlunarvinnublaðinu mynda færslur í *töflunni Frátekningarfærsla* með **reitinn Staða** frátekningar stillt á Rakning, Frátekning eða Umframbirgðir. Það ætti alltaf að vera par með sama Færslunr. af jákvæðu og neikvæðu gildi í reitnum **Magn (stofn)** þegar staðan er Rakning eða Frátekning. Reiturinn **Tegund** uppruna verður eftirspurnartegundin, þ.e. tafla 37 fyrir neikvætt magn og áætlunartöflu, til dæmis tafla 246, fyrir jákvætt magn. Reiturinn Upprunakenni **verður** ÁÆTLUN.

Ef um er að ræða óúthlutað framboð eða eftirspurn [!INCLUDE[prod_short](includes/prod_short.md)]  er reiturinn Staða **frátekningar stilltur** á Umframbirgðir. Til dæmis er hægt að hafa frátekningarstöðuna Umfram þegar fyrirliggjandi birgðir eru undir magni eða eftirspurn í öryggisbirgðum er tengd við spá.

Taflan *Órakin áætlunareining* (Tafla 99000855) geymir upplýsingar um órakið magn sem birtist þegar notandinn sér um að fletta upp á rakningarsíðu pöntunarinnar til að sjá órakið magn eða velja viðvörunartákn á áætlunarvinnublaðinu. Taflan inniheldur færslur sem standa fyrir órakið umframmagn í pöntunarrakningarkerfinu.

Þessar færslur eru stofnaðar við áætlunarkeyrslu og útskýra hvaðan órakta umframmagnið í rakningarlínunum kom. Þetta órakta umframmagn kom frá:

- Framleiðsluspá
- Standandi pantanir
- Magn í öryggisbirgðum
- Endurpöntunarmark
- Hámarksbirgðir
- Pöntunarmagn
- Hámarksmagn pöntunar
- Lágmarksmagn pöntunar
- Fjöldapanta
- Hömlur (% af lotustærð)

 *Í töflunni Frátekningarfærsla*, eins og í innkaupa-, millifærslu- og framleiðslupöntunum, er **reiturinn Sveigjanleiki** áætlunar. Þessi valkostsreitur tilgreinir hvort birgðir sem þessar framboðspantanir tákna eru skoðaðar af áætlunarkerfinu þegar aðgerðarboð eru reiknuð. Ef kosturinn Ótakmarkað er í reitnum tekur áætlunarkerfið línuna með í reikninginn þegar aðgerðaboð eru reiknuð. Ef kosturinn Ekkert er í reitnum er línan föst og óbreytanleg og áætlunarkerfið tekur ekki með línuna þegar aðgerðarboð eru reiknuð. Aðgerðinni *er stýrt í töflunni Frátekningarfærsla* með sama heiti.

### Endurpöntunar- og framleiðslustefna

Ef áætlunaraðgerð er framkvæmd fyrir vöru sem er sett með Endurpöntunarstefnuna sem stillt er á Pöntun [!INCLUDE[prod_short](includes/prod_short.md)]  stofnar færslur í *töflunni Frátekningarfærsla* með frátekningarstöðuna Frátekning í stað Rakningar.

Reitirnir **Tegund** uppruna og **Upprunakenni** hafa jafngilda meðferð á öðrum endurpöntunarstefnum. Í reitnum **Binding** í *töflunni*  Frátekningarfærsla [!INCLUDE[prod_short](includes/prod_short.md)] er hins vegar fært inn Pöntun-eftir pöntun.

Reiturinn **Binding** er fylltur út til að stýra framboðspöntunum sem eru bundnar við tiltekna eftirspurn, til dæmis framleiðslupantanir sem eru stofnaðar beint úr sölupöntun. Reiturinn sýnir Pöntun-í-pöntun þegar færslan er bundin sérstaklega við eftirspurn eða framboð (Sjálfvirk frátekning). Eftirspurnin getur verið tengd sölu- eða íhlutaþörf.

### Vörurakningar- og viðfangsfrátekningarfærsla

Hægt er að stofna [!INCLUDE[prod_short](includes/prod_short.md)] stöðu viðfangsfrátekningar í *töflunni Frátekningarfærsla* þegar engar pöntunarneteiningar eru notaðar, þ.e. Rakning pöntunar. Til dæmis, í notkunarbókarlínu er Vörurakningu úthlutað á íhlutinn. Ef varan er hins vegar þegar rakin [!INCLUDE[prod_short](includes/prod_short.md)]  gæti stofnað fleiri frátekningarfærslur viðfangs. Þetta er sýnt í theEXAMPLE 2 sem tengist millifærslupöntunum í seinni hluta skjalsins.

Þegar síðan Vörurakningarlínur **er skoðaðar eða þeim breytt** er sameiginlegt efni töflunnar *Rakningarlýsing* (Tafla 336) og *Frátekningarfærsla* sett fram í bráðabirgðaútgáfu af töflunni 336. Þetta tryggir heildaraðgang að fyrri og virkum vörurakningargögnum.

Frátekningar falla í tvo flokka: Ótilgreindar frátekningar þar sem lotu- og raðnúmer eru ekki tilgreind á frátekningartíma og Sértækar frátekningar þar sem tiltekin lotu- eða raðnúmer eru tekin frá í birgðum.

 **Lotunr.** eða **Raðnr.** reiturinn er auður í reitnum **Færslunr.** í töflu 337 sem vísar á eftirspurn (til dæmis sölu). Vegna skipulags frátekningargrunnsins í [!INCLUDE[prod_short](includes/prod_short.md)] verður engu að síður að velja tilteknar birgðafærslur til að taka frá [!INCLUDE[prod_short](includes/prod_short.md)]  á móti.

Þar sem birgðafærslurnar hafa vörurakningarupplýsingarnar tekur frátekningin óbeint tiltekin lotu- eða raðnúmer, jafnvel þótt notandinn hafi ekki ætlað þessu. Hins vegar, með Síðbúinni Bindingu, [!INCLUDE[prod_short](includes/prod_short.md)]  tekur samt frá gagnvart tilteknum færslum, en notar síðan endurskipulagningarbúnað í [!INCLUDE[prod_short](includes/prod_short.md)] við bókun.

Frekari upplýsingar er að finna í [!INCLUDE[prod_short](includes/prod_short.md)] Tæknilegu hvítmálunum sem taldir eru upp í viðbótarforðanum í lok skjalsins.

### Undirtegund uppruna, bækluð aðgerðaboð, Leiðrétting aðgerðaboða og Afturköllun heimildar

 **Undirtegund** uppruna, **bækluð aðgerðaboð,Leiðrétting** **aðgerðaboða** og **Afturköllun** uppruna í *töflunni Frátekningarfærsla* er lýst í þessum hluta. Aðstæður gefa kost á að sýna fram á notkun reitanna **Bækluð aðgerðaboð,Aðgerðaboðaleiðrétting** **·**  og **Afplánun afpantaðra** aðgerða. Reiturinn **Leiðrétting aðgerðarboða** er notaður fyrir aðgerðina Rakning pöntunarrakningar og Aðgerðarboð. Reiturinn **Ógilda afturköllun** er notaður fyrir aðgerðina Samsetning til pöntunar árið [!INCLUDE[prod_short](includes/prod_short.md)] 2013.

#### Undirtegund uppruna

Reiturinn **Undirtegund** uppruna gefur til kynna hvaða undirtegund uppruna frátekningarfærslan tengist. Ef færslan er tengd innkaupa- eða sölulínu afritast reiturinn úr reitnum **Tegund** fylgiskjals í línunni. Ef hún er tengd færslubókarlínu afritast reiturinn úr reitnum **Tegund** færslu í færslubókarlínunni.

#### Dempuð aðgerðarboð

Í **bækluðum aðgerðaboðum** Reitur skráir þegar búið er að vinna fyrirliggjandi framboð, til dæmis þegar innkaupapöntun hefur þegar verið móttekin að hluta eða framleiðslupöntun hefur bókað notkun á móti henni.

Við framkvæmd áætlunar er þessi reitur merktur [!INCLUDE[prod_short](includes/prod_short.md)]  og stillir reitinn **Staða** frátekningarfærslu á *Umframfærslur8. Eftirfarandi dæmi er til að myndskreyta:

1. Vara 80001 er opnuð. Eftirfarandi reitir eru stilltir:
  - **Endurpöntunarstefna**: Lota-fyrir-lotu
  - **Frátekning**: Valfrjálst
  - **Rakningarstefna** pöntunar: Engin
2. Stofnið sölupöntun. Eftirfarandi reitir eru stilltir:
  - **Vara**: 80001
  - **Birgðageymsla**: Auður/Ekkert
  - **Magn**: 10
  - **Afhendingardagsetning**: 2/15/2014
3.  **Keyrslan** Reikna áætlun **er opnuð** fyrir Vöru 80001.
  - **Upphafsdagsetning**: 01/23/2014
  - **Lokadagsetning**: 03/01/2014
4. Áætlunartillaga er gefin um að fylla á magnið 10 með nýrri innkaupapöntun og **Skiladagur** 02/15/2014.
5.  **Á flipanum Aðgerðir** í flokknum Aðgerðir skal velja **Framkvæma aðgerðarboð** til að stofna innkaupapöntun með **væntanlega móttökudags** . 02/15/2014.
6. Innkaupapöntunin er opnuð úr skrefi 5 og Magn til móttöku **stillt** á 2 og Móttaka bókuð aðeins.
7. Sölupöntunin er opnuð úr skrefi 2 og afhendingardagsetningu **breytt** í 02/10/2014.
8.  **Opna skal Innkaupatillögublöð** og keyra **Reikna áætlun** fyrir vöru 80001
  - **Upphafsdagsetning**: 01/23/2014
  - **Lokadagsetning**: 03/01/2014
9. Áætlunartillaga er gefin um að fylla á magnið 8 með nýrri innkaupapöntun og **Skiladagur** 02/10/2014.

Upplýsingar um stöðuna í töflu 337 birtast í eftirfarandi mynd.

Færslu nr. 28 í töflu 337 er með frátekningarstöðuna Rakning til samræmis við þær birgðir sem fyrir eru í birgðafærslu 318 fyrir 2 einingar og útistandandi eftirspurn í töflunni Sölupöntun 37. Síðari Færslunr. 29 er einnig með stöðuna Rakning og tengir eftirstöðvar magnsins 8 einingar milli eftirspurnar í töflunni Sölupöntun 37 og tillaga um framboð í töflunni Innkaupatillögulína 246.

Færslunr. 30 er fyrirliggjandi innkaupapöntun sem hefur verið móttekin að hluta með magni 2. Þar af leiðandi **er reiturinn Staða** frátekningar umframmagn og [!INCLUDE[prod_short](includes/prod_short.md)] stillir **reitinn Magn (stofn)** á *8*  (eftirstöðvar) og **bættu aðgerðaboðunum.** reiturinn er virkur.

#### Leiðrétting á aðgerðarboði

Reiturinn **Leiðrétting** aðgerðarboða sýnir breytingu á framboðshlið pöntunarrakningarinnar þegar tengd aðgerðarboð eru samþykkt. Gildi birtist aðeins hér þegar aðgerðirnar fyrir bæði pöntunarrakningu og aðgerðaboð eru virkar (Rakningarstefna pöntunar stillt á Rakning & aðgerðarboð). Gildið er reiknað út frá gögnunum í *töflunni Aðgerðaboðafærsla* (Tafla 99000849). Eftirfarandi dæmi er til að myndskreyta:
1. Opna vöru 80002. Eftirfarandi reitur er stilltur:
 - **Rakningarstefna** pöntunar: Rakning og aðgerðarskilyrði
2. Stofnið sölupöntun. Eftirfarandi reitir eru stilltir:
  - **Vara**: 80002
  - **Birgðageymsla**: BLÁTT
  - **Magn**: 100
3.  **Síðan Pantanaáætlun** er opnuð og keyrslan **Reikna áætlun** keyrð.
4. Sölupöntunin er valin úr skrefi 2 og keyrslan **Gera pantanir** er keyrð.
5. Í sölupöntuninni úr skrefi 2 er reitnum **Magn** breytt úr 100 í 105.
Upplýsingar um stöðuna í töflu 337 birtast í eftirfarandi mynd.
6. Færslunr. 34 er með reitinn **Leiðrétting aðgerðaboða** í töflu 337 virkan fyrir 5 einingar með frátekningarstöðuna Umframbirgðir. Þegar sölupöntunin var aukin í 5 [!INCLUDE[prod_short](includes/prod_short.md)] . lið var þessi frátekning stofnuð þar sem þörf er á meira framboði.
7. Opna skal síðuna Áætlunarvinnublöð **og á** flipanum Heim **í hópnum** Vinnsla **skal velja** Sækja aðgerðarboð **.** [!INCLUDE[prod_short](includes/prod_short.md)] mun leggja til að magn innkaupapöntunarinnar verði aukið úr 100 í 105.

#### Ógilda afturköllun

Reiturinn **Afturköllun án afturköllunar** gefur til kynna að frátekningarfærslan tákni tengja milli sölupöntunarlínu og samsetningarpöntunar. Ekki er hægt að eyða frátekningunni vegna þess að nauðsynlegt er að viðhalda samstillingunni sem á sér stað þegar vara er sett saman í pöntun. Eftirfarandi dæmi er til að myndskreyta:

1. Stofna innkaupapöntun. Eftirfarandi reitir eru stilltir:
  - **Grunnmælieining**: STK
  - Allir sjálfgefnir bókunarflokkar
  - **Áfyllingarkerfið**: Samsetning
  - **Samsetningarstefna**: Samsetning í pöntun
  - **Rakningarstefna** pöntunar: Aðeins rakning
2. Stofna skal nýja vöru sem nefnist Samsetning TVÍV. Eftirfarandi reitir eru stilltir:
  - **Grunnmælieining**: STK
  - Allir sjálfgefnir bókunarflokkar
  - **Áfyllingarkerfið**: Innkaup
  - **Rakningarstefna** pöntunar: Aðeins rakning
3. Opna vörusamsetningarFG og á flipanum Færsluleit **, í flokknum** Samsetning/Framleiðsluflokkur **, skal velja** Samsetning **og velja** síðan Samsetningaruppskrift **.** Í samsetningaruppskriftinni eru eftirfarandi reitir stilltir:
  - **Tegund**: Vara
  - **Nr.**: Sett saman tengt
  - **Magn á**: 1 Velja skal hnappinn **Í lagi** .
4. Birgðabók er opnuð og birgðamagn samsetningarsamsetningar aukið í magn 10 í birgðageymslunni BLÁTT og færslubókarlínan bókuð.
5. Stofnið sölupöntun. Eftirfarandi reitir eru stilltir:
  - **Vara**: Sett saman FG
  - **Birgðageymsla**: BLÁTT
  - **Magn**: 1 Upplýsingar um stöðuna í töflu 337 birtast í eftirfarandi mynd.

Færslunr. 82 er með frátekningarstöðuna Umframbirgðir sem 9 einingar af Samsetningarsamstæðu í birgðum og hefur enga eftirspurn. Færslunr. 84 eru rakningarfrátekningarfærslur milli eftirspurnar í *töflunni Samsetningarlína* 901 og framboðs í birgðafærslu 346.

Færslunr. 86 er með Bindandi pöntun-í-pöntun við frátekningarstöðufrátekningu. Að auki er reiturinn **Ógilda afturköllun** virkur þar sem samsetningarstefnan er stillt sem Samsetning í pöntun fyrir vörusamsetningu FG. Að lokum er reiturinn **Sveigjanleiki** áætlunar stilltur á Ekkert, því [!INCLUDE[prod_short](includes/prod_short.md)] ekki leyfir áætlunargrunninn að eyða frátekningunni.

#### Tiltækt magn til tínslu og frátekningar

Frátekin **tínsla & Afhenda**  magní töflu 337 sem er til í útgáfum áður en [!INCLUDE[prod_short](includes/prod_short.md)] 2013 stýrir tiltækum vörum innan stýrðs vöruhúss. Í hverri uppsetningu vöruhúsakerfis [!INCLUDE[prod_short](includes/prod_short.md)] er magn vöru bæði til sem vöruhúsafærslur og birgðafærslur. Þessar tvær færslutegundir innihalda mismunandi upplýsingar um hvar vörur eru til og hvort þær eru tiltækar. Vöruhúsafærslur skilgreina framboð vöru eftir hólfi og hólfagerð, sem kallast innihald hólfs. Birgðahöfuðbókarfærslur skilgreina hvort vara er laus með frátekningu hennar samkvæmt fylgiskjölum á útleið. Sérstakar aðgerðir eru til í tínslureiknireglurnar til að reikna magnið sem er tiltækt til tínslu þegar innihald hólfs er parað með frátekningu. Tínslureiknireglurnar draga frá magn sem er tekið frá fyrir önnur skjöl á útleið, magn í tínsluskjölum sem fyrir eru og magn sem er tínt en ekki enn afhent eða notað. Útkoman birtist í reitnum **Tiltækt magn til tínslu** á síðunni **Tínsluvinnublað** þar sem reiturinn er reiknaður kviklega. Gildið er einnig reiknað þegar notandi stofnar vöruhúsatínslu beint úr skjölum á útleið, svo sem sölupöntunum, framleiðslunotkun eða millifærslum á útleið.

*Magn tiltækt til tínslu = magn í tínsluhólfum - magn í tínslum og hreyfingum – (frátekið magn í tínsluhólfum + frátekið magn í tínslum og hreyfingum).*

Eftirfarandi dæmi sýnir hvernig gildið í magninu sem tiltækt er til tínslu er reiknað í [!INCLUDE[prod_short](includes/prod_short.md)]:

1. Stofna nýja vöru sem kallast Vöruhúsavara. Eftirfarandi reitir eru stilltir:
  - **Grunnmælieining**: STK
  - Allir sjálfgefnir bókunarflokkar
  - **Áfyllingarkerfið**: Innkaup
  - **Frátektarstefna**: Alltaf
  - **Rakningarstefna** pöntunar: Aðeins rakning
2. Stofna innkaupapöntun á móti lánardrottni 60000. Eftirfarandi reitir eru stilltir:
  - **Vara**: Vöruhúsavara
  - **Staðsetning**: HVÍTT
  - **Magn**: 100
3. Innkaupapöntunin er gefin út og vöruhúsamóttakan stofnuð.
4. Vöruhúsamóttakan er bókuð og vöruhúsafrágangurinn skráður fyrir magnið 100.
5. Stofna aðra innkaupapöntun á móti lánardrottni 60000. Eftirfarandi reitir eru stilltir:
  - **Vara**: Vöruhúsavara
  - **Staðsetning**: HVÍTT
  - **Magn**: 10
6. Innkaupapöntunin er gefin út og vöruhúsamóttakan stofnuð.
7. Aðeins vöruhúsamóttakan er bókuð. Ekki skrá vöruhúsafráganginn.
8. Stofnið sölupöntun. Eftirfarandi reitir eru stilltir:
  - **Vara**: Vöruhúsavara
  - **Staðsetning**: HVÍTT
  - **Magn**: 10 Frátekið magn er sjálfkrafa stillt á 10 vegna þess að frátektarreglan er stillt á Alltaf.
9. Stofnið sölupöntun. Eftirfarandi reitir eru stilltir:
  - **Vara**: Vöruhúsavara
  - **Staðsetning**: HVÍTT
  - **Magn**: 100 Frátekið magn er sjálfkrafa stillt á 100 vegna þess að frátektarstefnan er stillt á Alltaf.
10. Gefa út fyrstu sölupöntunina úr 8. þrepi og stofna vöruhúsaafhendingu.
11. Gefa út vöruhúsaafhendinguna og á **flipanum Aðgerðir** skal velja **Stofna tínslu**.
Eftirfarandi villuboð birtast: *Ekkert í meðhöndlun.*
  Ástæðan er sú að tiltækt magn til tínslu er núll. Þetta er reiknað á eftirfarandi hátt: Magn í birgðum = 110 Tiltækt magn til tínslu = 100

> [!NOTE]  
> Magn í frágangi eða hólfi móttöku er ekki tiltækt fyrir tínslu.
   
   Samtals frátekið á móti sölupöntunum er 110 Magn sem er tiltækt til tínslu = 100 – 110 = núll.

Þegar vöruhúsafrágangurinn er skráður í 7. þrep, sem gerir stofnun vöruhúsatínslunnar mögulega í 11. þrep. Í útgáfum fyrir [!INCLUDE[prod_short](includes/prod_short.md)] árið 2013 skal fylla frátekið **tínslu - Afhenda magn til afhendingar.** í töflu 337 er fylltur út á móti frátekningu á magni 10.

Eftirfarandi mynd er sótt úr [!INCLUDE[prod_short](includes/prod_short.md)] 2009 R2.

## Útskýringar með millifærslupöntunum og áætlunum

### Millifærslupantanir

Þegar millifærslupantanir eru notaðar og varan er afhent en ekki að fullu móttekin fæst frátekningarstaðan Umframmagn í *töflunni Frátekningarfærsla* . Kóti birgðageymslu verður Sendist-til birgðageymsla.

Reiturinn **Tilv.nr. uppruna** Er reiknað með síðasta línufærslunúmeri + Línufærslunúmer vörunnar í bókuðu millifærsluafhendingunni.

Þegar pöntunarrakning er virk og engin eftirspurn er (sölupöntun eða notkun), [!INCLUDE[prod_short](includes/prod_short.md)] stofnar tvær færslur í töflu 337 með frátekningarstöðuna Umframmagn. Annar er á móti *töflunni Millifærslulína* 5741 og hinn er á móti töflunni Birgðafærsla 32.

Þetta er sýnt í fyrsta dæminu.

#### Dæmi 1

1. Vörur 80003 og 80004 eru opnaðar og reiturinn **Rakningarstefna** stilltur á *Aðeins* rakning. Aðrir reitir eru látnir vera sjálfgildi.
2. Birgðabók er opnuð og birgðum þessara vara aukið í magn 10 hver á móti birgðageymslunni RAUTT og færslubókarlínurnar bókaðar.
3. Stofna millifærslupöntun frá birgðageymslunni RAUTT til BLÁTT fyrir þessar tvær vörur: Vara 80003 á millifærslupöntunarlínu 10000 og Vara 80004 á annarri línu 20000, bæði fyrir 10 einingar.
4. Bóka aðeins afhendingarhluta millifærslupöntunarinnar án vöruhúsaaðgerða.
Bókaða millifærsluafhendingin birtist í eftirfarandi mynd.
Upplýsingar um stöðuna í töflu 337 birtast í eftirfarandi mynd.
5. Bera niðurstöðurnar í bókuðu millifærsluafhendingunni saman við færslurnar í töflu 337.

Eftirfarandi tafla lýsir því sem gerist í tilteknum reitum gegn frátekningarfærslu 40.

|Svæði|Heimildasamstæða|  
|---------------------------------|---------------------------------------|  
|**Staða frátekningar**|Umframmagn sem Vara 80003 er sett upp með pöntunarrakningu en engin eftirspurn er til.|  
|**Staðsetningarkóði**|Flutt-til kóti birgðageymslu BLÁTT.|  
|**Tegund uppruna**|Millifærslulína 5741.|  
|**Upprunakenni**|Númer fylgiskjals millifærslupöntunarinnar 1011.|
|**Tilv.nr. uppruna**|Línunr. heildarlínu 20000 + Línunr. 10000 gegn vöru 80003 = 30000.|

Skýringin á eftirfarandi reitum gegn frátekningarfærslu 43 er sem hér segir.

|Svæði|Heimildasamstæða|  
|---------------------------------|---------------------------------------|  
|**Staða frátekningar**|Umframmagn sem Vara 80003 er sett upp með pöntunarrakningu en engin eftirspurn er til.|  
|**Staðsetningarkóði**|Eigin birgðageymsla millifærslustaðsetningar er sú birgðageymsla sem varan er til á.|  
|**Tegund uppruna**|Taflan Birgðafærsla 32.|  
|**Tilv.nr. uppruna**|Opna birgðafærslan 322.|

#### Dæmi 2

Næsta dæmi sýnir hvað gerist þegar íhlutur er fluttur milli birgðageymslna, en um leið er rakið á milli eftirspurnarþarfar og tiltæks framboðs. Íhlutirnir verða fluttir frá birgðageymslunni RAUTT yfir í BLÁTT sem á að nota í útgefinni framleiðslupöntun. Íhluturinn notar Rakningu pöntunar, Pantanaáætlun og Vörurakningu.

Dæmið vísar í greint flæði í töflu 337 í tengslum **við reitina Frátekningarstaða**, **Kóti** birgðageymslu,Tegund **uppruna**, **Kenni uppruna**, **Tilv.nr.** uppruna og tegund **Bindingar**.

1. Á síðunni Uppsetning **framleiðslu er reiturinn** Íhlutir á staðnum **stilltur** á RAUTT.
2. Nýr vöruíhlutur er stofnaður. Eftirfarandi reitir eru stilltir:
  - **Grunnmælieining**: STK
  - Allir sjálfgefnir bókunarflokkar
  - **Áfyllingarkerfið**: Innkaup
  - **Framleiðslustefna**: Til í birgðum
  - **Rakningarstefna** pöntunar: Aðeins rakning
  - **Vörurakningarkóti**: LOTA
3. Með Birgðabókinni er birgðaaukning fyrir Vöruíhlut aukin á móti birgðageymslunni RAUTT í 100 einingar. Stilla eftirfarandi lotunúmer:
  - Lotunúmer Lota A, Magn 30
  - Lotunúmer B, Magn 70
4. Stofna nýja vöru framleidda. Eftirfarandi reitir eru stilltir:
  - **Grunnmælieining**: STK
  - Allir sjálfgefnir bókunarflokkar
  - **Áfyllingarkerfið**: Framleiðsla
  - **Framleiðslustefna**: Til í birgðum
  - **Rakningarstefna** pöntunar: Aðeins rakning
5. Framleiðsluuppskrift **búin til** með 1 magni á vöruíhlut.
6. Úthluta framleiðsluuppskriftinni á vöru framleidda.
7. Stofnið sölupöntun. Eftirfarandi reitir eru stilltir:
  - **Vara**: Framleidd
  - **Birgðageymsla**: BLÁTT
  - **Magn**: 100
8.  **Á flipanum Aðgerðir** í sölupöntuninni, í flokknum **Áætlun, skal velja** Áætlun **til** að stofna tengda útgefna framleiðslupöntun á móti sölupöntuninni.
9. Útgefna framleiðslupöntunin / íhlutaþörfin er opnuð og takið eftir að birgðageymsan er stillt sem RAUTT.
Ástæðan er sú að Íhlutir á staðnum **eru** RAUÐUR á spjaldinu **Uppsetning framleiðslu** .
Varan framleidd fær frálagið á móti birgðageymslunni BLÁTT.

Upplýsingar um stöðuna í töflu 337 birtast í eftirfarandi mynd.

##### Frátekningarfærslur með tölurnar 55 og 56

Fyrir íhlutaþörfina fyrir Lotu A og Lotu B eru pöntunarrakningartenglar stofnaðir úr eftirspurninni í töflu 5407, Framl.pöntunaríhlutur, til framboðsins í töflu 32, Birgðafærsla.  **Í reitnum Staða** frátekningar er Rakning allra færslnanna fjögurra sem gefa til kynna að þessar kviku pöntunarrakningartengingar milli framboðs og eftirspurnar.

Eftirspurnin í töflu 5407, Framl.pöntunaríhlutur, er tengd upprunakenni útgefnu framleiðslupöntunarinnar 101006. Framboðið í töflu 32, Birgðafærsla, er tengt við tilv.nr. uppruna Verið í birgðafærslunúmerunum 325 og 326 þar sem einingarnar eru til.

> [!NOTE]  
> Reiturinn**lotunr.** er auður á eftirspurnarlínum vegna þess að ekki eru tilgreind lotunúmer í íhlutalínum losaðrar framleiðslupöntunar.

##### Frátekningarfærsla með númer 57

Úr sölueftirspurninni í töflu 37, Sölulína, er rakning pöntunar tengja stofnuð fyrir framboðið í töflu 5406, Framl.pöntunarlína.  **Í reitnum Staða** frátekningar er Frátekning og í reitnum **Binding** er Pöntun-eftir pöntun. Það er vegna þess að útgefna framleiðslupöntunin var mynduð sérstaklega fyrir sölupöntunina og verður að vera tengd ólíkt rakningartenglum pöntunar með frátekningarstöðuna Rakning, sem er stofnuð og breytt kviklega.

> [!NOTE]  
> Í **reitnum Binding** getur einnig *verið Pöntun-í-pöntun* þegar eftir pöntun er notuð sem framleiðslustefna og/eða pöntun sem endurpöntunarstefna.

10. Á þessum tímapunkti í dæminu eru 100 einingar íhlutarins fluttar frá birgðageymslunni RAUTT yfir í birgðageymsluna BLÁTT með því að nota millifærslupöntun.

Valið er Lota A og Lota B fyrir afhendinguna.

Bóka heildarmagn útistandandi sem aðeins afhent.

> [!NOTE]  
> Hægt er að nota íhluti í birgðageymslunni RAUTT, en til dæmis til að sýna flæði frátekningarfærslna eru einingarnar fluttar handvirkt í birgðageymsluna BLÁTT.

Upplýsingar um stöðuna í töflunni 337 birtast í eftirfarandi mynd.

##### Frátekningarfærslur með númer 55 og 56

Rakningarfærslur pantana fyrir loturnar tvær íhlutsins sem endurspegla eftirspurn í töflu 5407 er breytt úr frátekningarstöðu Rakningar í Umframmagn. Ástæðan er að birgðirnar sem greiðslan var tengd við áður, í töflu 32, hafa verið notaðar af sendingu á millifærslupöntuninni. Raunverulegur afgangur, eins og í þessu tilfelli, endurspeglar umframframboð eða eftirspurn sem helst órakin. Það er vísbending um ójafnvægi á pöntunarnetinu, sem mun mynda aðgerðarboð af áætlunarkerfinu nema það sé leyst með gagnvirkni.

##### Frátekningarfærslunúmer 59 til 63

Þar sem tvær lotur íhlutarins eru bókaðar í millifærslupöntunina sem afhentar en ekki mótteknar eru allar tengdar jákvæðar rakningarfærslur pöntunar af frátekningartegundinni Umframmagn sem gefur til kynna að þeim sé ekki úthlutað á neina eftirspurn. Ein færsla tengist töflu 5741, Millifærslulínu fyrir hvert lotunúmer og eina færslu sem tengist birgðafærslunni í millifærslustaðnum þar sem vörurnar eru nú til.

Tafla 5741, **millifærslulína** er Tegund uppruna. **Upprunakenni** er Númer millifærslupöntunarskjals 1012 og **Tilv.nr. uppruna** Er 20000 = 10000 + 10000 eins og lýst er í dæmi 1. Birgðageymslan er stillt sem BLÁTT fyrir kóta sendist-til birgðageymslu.

Tvær færslurnar sem eftir eru með **Frátekningarstöðuumframboð** hafa töflu 32,Birgðafærsla **·**, sem Tegund uppruna og **Tilv.nr. uppruna.** 328 og 330, að meðtöldum lotunúmerum þeirra sem eru staðsettar í birgðageymslunni Í millifærslustaðnum OUT LOG.

11. Bóka útistandandi millifærslupöntun sem Móttekin.

Upplýsingar um stöðuna í töflunni 337 birtast í eftirfarandi mynd.

Pöntunarrakningarfærslurnar eru nú svipaðar og fyrsti punkturinn í dæminu, áður en millifærslupöntunin var aðeins bókuð sem afhent, nema færslur fyrir íhlutinn eru nú umframmagn frátekningar í stað Rakningar. Það er vegna þess að íhlutaþörfin er enn í birgðageymslunni RAUTT sem sýnir að í reitnum **Kóti** birgðageymslu í íhlutalínu framleiðslupöntunarinnar er RAUTT eins og sett er upp í reitnum **Íhlutir á staðnum** .

Framboðið sem var úthlutað á þessa eftirspurn áður hafði verið flutt í birgðageymsluna BLÁTT og er ekki hægt að rekja að fullu nema íhlutaþörfinni í framleiðslupöntunarlínunni sé breytt í birgðageymsluna BLÁTT. Þetta er skráð í síðustu tveimur frátekningarfærslunum með lotunúmerin sem eru útfyllt,reiturinn **Tegund** uppruna er Tafla 32 og **Tilv.nr. uppruna** í birgðafærslum 333 og 334.

12. Á íhlutalistanum sem úthlutað er á útgefnu framleiðslupöntunina er birgðageymslunni breytt í BLÁTT fyrir íhlutinn.

12. Notkunarbókin **er** opnuð og keyrslan **Reikna notkun** keyrð.
Úthluta lotumagni 30 og Lotu B magni 70.

Glugganum Vörurakning er lokað.

Upplýsingar um stöðuna í töflunni 337 birtast í eftirfarandi mynd.

##### Frátekningarfærslur með tölurnar 68 og 69

Þar sem íhlutaþörfinni hefur verið breytt í birgðageymsluna BLÁTT og framboðið er tiltækt sem birgðafærslur í birgðageymslunni BLÁTT eru allar pöntunarrakningarfærslur fyrir lotunúmerin tvö nú að fullu raktar, gefið til kynna með frátekningarstöðunni Rakning. Lotunúmerin eru ekki útfyllt í reitnum **Lotunr.** á móti eftirspurninni í töflu 5406, **Framleiðslupöntunarlína**, þar sem við tilgreindum ekki lotunúmer fyrir íhlutinn í útgefnu framleiðslupöntuninni.

##### Frátekningarfærslur með tölurnar 70 og 71

Færslur með frátekningarstöðuna Viðfang eru myndaðar í töflu 337. Ástæðan er sú að báðum lotunúmerum er úthlutað á móti íhlutnum í notkunarbókinni, en færslubókin hefur ekki verið bókuð.

Svona lýkur hlutanum hvernig rakningarfærslur pantana í **töflunni Frátekningarfærsla** eru myndaðar, þeim breytt og þeim eytt þegar margar aðgerðir eru notaðar ásamt millifærslupöntunum.

### Áætlun reiknuð

Þegar áætlunaraðgerðir eru notaðar, þ.e. Innkaupatillögublað **, Áætlunarvinnublað** eða **Pantanaáætlun**, er hugsanlegt að **frátekningarfærslum** í töflunni Frátekningarfærsla **337 sé breytt eða bætt við eftir áætlunartillögunni sem rökmálið**  gefur [!INCLUDE[prod_short](includes/prod_short.md)] upp. Dæmi 3 mun nota **Endurpöntunarstefnupöntun** með **framleiðslustefnunni** Make-to Order fyrir framleidda vöru. Íhluturinn notar **Endurpöntunarstefnuna** Fast endurpöntunarmagn.

#### Dæmi 3

1. Á **spjaldinu**  Uppsetning framleiðslu **er Íhlutur á staðnum** RAUÐUR frá fyrra dæmi.
2. Stofna nýja yfireining vöru 70061. Eftirfarandi reitir eru stilltir:
  - **Grunnmælieining**: STK
  - Allir sjálfgefnir bókunarflokkar
  - **Áfyllingarkerfið**: Framl.pöntun
  - **Framleiðslustefna**: Eftir pöntun
  - **Endurpöntunarstefna**: Pöntun
  - **Frátekningarstefna**: Valfrjálst
  - **Rakning pöntunar**: Ekkert
3. Stofna nýja vöruíhlut 70062. Eftirfarandi reitir eru stilltir:
  - **Grunnmælieining**: STK
  - Allir sjálfgefnir bókunarflokkar
  - **Áfyllingarkerfið**: Innkaup
  - **Endurpöntunarstefna**: Fast endurpöntunarmagn
  - **Frátekningarstefna**: Valfrjálst
  - **Rakningarstefna** pöntunar: Engin
  - **Magn öryggisbirgða**: 10
  - **Endurpöntunarmark**: 25
  - **Endurpöntunarmagn**: 50
4. Ný framleiðsluuppskrift er búin til og íhlutavara 70062 tilgreind með magni á 1.
Framleiðsluuppskriftinni er úthlutað á yfireining vöru 70061.
5. Stofnið sölupöntun. Eftirfarandi reitir eru stilltir:
  - **Vara**: Fast endurpöntunarmagn
  - **Staðsetning**: RAUTT
  - **Magn**: 40
  - **Afhendingardagsetning**: 2/15/2014
6.  **Síðan Áætlunarvinnublöð** er opnuð **og keyrslan Reikna áætlun endurgerðar keyrð** .
  - **MPS/MRP**: virkt
  - **Upphafsdagsetning**: 01/23/2014
  - **Lokadagsetning**: 03/01/2014
  - Afmörkun á vörum 70061 og 70062
  - Engin spá

Eftirfarandi áætlunartillögur eru gefnar.

Fyrsta áætlunartillagan er að stofna nýja áætlaða framleiðslupöntun til að útvega útistandandi eftirspurn sölupöntunarinnar fyrir magn 40 í yfireining Vöru 70061. Farið yfir rakningu pantana og [!INCLUDE[prod_short](includes/prod_short.md)] birtir útistandandi sölupöntun. Pöntunarrakning er virk þegar áætlunarvélin myndar hana.

Önnur línan er að koma með Birgðir fyrir ofan endurpöntunarmark (25). Að teknu tilliti til Endurpöntunarmagns (50) er magnið 50 einingar lagt til í áætlunargrunninum. Þriðja línan er að færa Birgðir í öryggisbirgðastig (10).

Fjórða línan á að fylla á birgðir þegar sölupöntunin er afhent. Þá eru Birgðir 20 og svo undir endurpöntunarmarki. Þar af leiðandi leggur áætlunarvélin til að kaupa inn 50 viðbótaríhluti sem teknir eru með í reikninginn Endurpöntunarmagn. Þetta er Órakið magn, svo í *töflunni Frátekningarfærsla* 337 verður þetta merkt með frátekningarstöðunni Umframmagn.

Upplýsingar um stöðuna í töflunni 337 birtast í eftirfarandi mynd.

Reiturinn **Staða** frátekningar er Frátekning og Binding eftir pöntun er stofnuð. Ástæðan er sú að Framleiðslustefna vörunnar er eftir pöntun og endurpöntunarstefnan er stillt sem Pöntun. Ef annar af tveimur er stilltur á Pöntun er staða frátekningar frátekning í stað Rakning og Binding stillt á Pöntun eftir pöntun.

Eftirspurnin upp á 40 einingar á móti reitnum **Upprunakenni** er sölupöntunarnúmerið 1005 og tegund uppruna er *taflan Tegund* uppruna 37. Frátekningarfærslan er samstillt áætlunartillögunni, Tilv.nr. upprunatilv. 10000, upprunakenni er ÁÆTLUN og Tegund uppruna er *taflan Innkaupatillögulína* 246. Svo það er staða milli eftirspurnar úr sölupöntuninni og það er birgðir sem áætlunarvélin leggur til.

##### Frátekningarfærslunúmer 73 og 74

Með keyrslunni Reikna áætlun verða til næstu fjórar færslur með frátekningarstöðuna Rakning vegna stillingar endurpöntunarstefnunnar Fast endurpöntunarmagn fyrir íhlutinn. Nauðsynlegt framboð fyrir íhlut vara 70062 er fyllt á samkvæmt áætlunartillögunum sem gefnar eru, Tilv. upprunatilv. nr. 20000 og 30000, með upprunakenni stillt á ÁÆTLUN og Tegund uppruna úr *innkaupatillögulínu* töflu 246. Íhlutaþörfin er stofnuð til að uppfylla eftirspurnina á móti yfireining Vöru 70061 fyrir heildarmagn (stofn) 40. Reiturinn **Upprunaframl.pöntunarlína** er 10000 með tegund uppruna töfluna *Íhlutaþörf* 99000829.

Frátekningarstaðan er ekki Umframmagn þar sem pöntunarrakning er á milli eftirspurnar yfireining vöru 70061 og framboðs á vöruíhlut 70062.

##### Frátekningarfærslunúmer 75 og 76

Síðustu tvær færslurnar hafa frátekningarstöðuna Umframmagn þar sem þær eru Órakið magn sem er myndað á áætlunarvinnublaðinu sem tengist endurpöntunarfæribreytunum Endurpöntunarmark og Endurpöntunarmagn.

## Sjá einnig .  
[Hönnunarupplýsingarn: vörurakning hönnun](design-details-item-tracking-design.md)  
[Hönnunarupplýsingar: Jöfnun eftirspurn og framboð](design-details-balancing-demand-and-supply.md)  
[Hönnunarupplýsingar: Pöntun, pöntunarrakning og stöðuboð](design-details-reservation-order-tracking-and-action-messaging.md)   
[Hönnunarupplýsingar: framboðsáætlun](design-details-supply-planning.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]