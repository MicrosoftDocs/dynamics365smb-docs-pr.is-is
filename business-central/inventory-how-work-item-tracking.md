---
title: 'Rekja vörur með rað-, lotu- og pakkanúmerum'
description: 'Hægt er að bæta við raðnúmerum, lotunúmerum og pakkanúmerum við hvaða útleiðarskjal eða innleiðarskjal sem er og bókaðar færslur þess er síðan hægt að skoða í viðkomandi birgðafærslum.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: conceptual
ms.search.forms: '6503, 6515, 6513, 6512, 6502, 6506, 6501, 6510, 6507, 6500, 6505, 6508, 9126, 6526, 6516, 6511, 6504, 6509, 163, 6550,'
ms.date: 10/02/2023
ms.custom: bap-template
---
# Rekja vörur með rað-, lotu- og pakkanúmerum

Hægt er að úthluta raðnúmerum, lotunúmerum og pakkanúmerum á öll eða send skjöl á útleið og bókaðar eru Vörurakningarfærslur birtar í tengdum birgðafærslum. Þú heldur utan um vörur á  **síðunni Vörurakningarlínur**  sem er hægt að opna á innleið eða útleið.

Reitirnir Magn efst á  **vörurakningarlínunum**  Sýna magn og samtölur vörurakningarnúmera sem eru skilgreind í línunum. Magnið verður að samsvara þeim í fylgiskjalslínum sem eru tilgreind með 0 í  **óskilgreinda**  reitina.

[!INCLUDE [prod_short](includes/prod_short.md)] Uppfærir ráðstöfunarupplýsingar á  **síðunni Vörurakningarlínur**  þegar þú opnar síðuna. Það uppfærist ekki upplýsingar á meðan þú hefur síðuna opna, jafnvel þótt breytingar eigi sér stað í birgðum eða á öðrum skjölum á þeim tíma.

> [!NOTE]  
> Til þess að aðgerðirnar, sem er lýst í þessari grein, þurfi að setja upp vörurakningu. Til að fá frekari upplýsingar er farið í að  [Setja upp vörurakningu með rað-, lotu-og Pakkningsnúmerum](inventory-how-setup-item-tracking.md).

## Vörurakning til ráðstöfunar

Þegar unnið er með rað-, lotu-og pakkanúmer,  [!INCLUDE[prod_short](includes/prod_short.md)]  reiknar ráðstöfunarupplýsingar út og sýnir það á ýmsum vörurakningarsíðum. Það sýnir hve mikið af lotu, pakkningu eða raðnúmeri er notað á önnur skjöl. Þessar upplýsingar hjálpa til við að draga úr villum og óvissu sem stafar af tvöföldum úthlutunum.

 **VIÐVÖRUNARTEIKN eru birt í**  ráðstöfunarlínum vöru, lotunúmer, á síðunni Vörurakningarlínur  **.** eða  **ráðstöfunar, raðnr.** svæði af eftirfarandi ástæðum:

* Ef eitthvert magnið sem var valið er þegar í notkun í öðrum skjölum.
* Ef lotunúmerið eða raðnúmer eru ekki tiltæk.

 **Lotunr./raðnr.-listi**,  **lotunúmer/raðnr.-til** ráðstöfunar  **og vörurakningar-velja færslur**  Sýna magn vöru sem er í notkun. Í eftirfarandi töflu er listi yfir viðeigandi reiti.

|Svæði|Heimildasamstæða|
|-----|-----------|  
|**Heildarmagn**|Heildartala vöru sem er í birgðum.|
|**Umbeðið magn samtals**|Heildarfjöldi atriða sem beðið er um í þessum og öðrum fylgiskjölum.|
|**Magn í undirbúningi**|Fjöldi vara sem beðið er um í skjalinu en það er ekki bókað.|
|**Umbeðið magn**|Fjöldi þeirra vara sem búið er að biðja um að nota í núverandi skjali.|
|**Heildarmagn tiltækt**|Heildarfjöldi vara í birgðum, mínus magn vörunnar sem beðið er um í þessum og öðrum skjölum (heildarumbeðið magn) og að frádreginni magninu sem er beðið um en hefur enn ekki verið bókað í þessu skjali (núverandi biðmagn).|

Ef unnið er á  **síðunni Vörurakningarlínur**  til langs tíma eða ef mikið er um verkþátt með vörunni sem unnið er með er hægt að  **Velja aðgerðina endurnýja framboð** . Einnig er ráðstöfunarmagn vörunnar sjálfkrafa kannað þegar síðunni er lokað til að staðfesta að það séu ekki ráðstöfunarvandamál.

## Úthlutun rað- eða lotunúmera á færslur á leið inn.

Þú gætir viljað rekja vörur frá því að þær berast. Í því tilfelli er kauppöntunin oft aðalskjal. Hins vegar er hægt að gera vörurakningu úr öllum innsendum skjali og bókaðar færslur birtast í tengdum birgðafærslum.

Rakningarnúmerin flytja sjálfkrafa í allar vöruhúsaaðgerðir á útleið.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Innkaupapantanir** og velja síðan viðkomandi tengil.  
2. Annaðhvort skal opna innkaupapöntun sem þegar er til eða stofna nýja.
3. Fylgiskjalslínan er valin og á  **föstu línunum**  er  **línuaðgerðin**  valin og síðan er  **valin aðgerðin vörurakningaraðgerðir**  til að opna  **síðuna Breyta-Vörurakningarlínur** .  

   Nú er hægt að úthluta rað- eða lotunúmerum á eftirfarandi hátt:  
   - Sjálfvirkt, með því að velja **Vinna** og svo **Úthluta raðnr.** eða **Úthluta lotunr.** og úthlutar kerfið þá rað- eða lotunúmerum úr forskilgreindum númeraröðum.  
   - Sjálfvirkt, með því að velja **Vinna** og svo **Stofna sérsniðin RN**, og úthlutar þá kerfið rað- eða lotunúmerum samkvæmt númeraröðum sem notandi skilgreinir sérstaklega fyrir mótteknar vörur.  
   - Handvirkt með því að færa inn rað- eða lotunúmer beint, t.d. númer birgis.  
   - Handvirkt með því að úthluta hverri vörueiningu sérstöku númeri.  

4. Til að úthluta sjálfvirkt skal velja **Stofna sérstillt raðnúmer** aðgerðina.  
5.  **Í reitinn SÉRSNÍÐA sn**  er fært inn Upphafsnúmer lýsandi raðnúmeraraðar.  **T.d. S/N-Vend0001**.  
6. Í reitinn **Hækka** er færð talan 1 til að tiltaka að hvert raðnúmer hækkar um einn.  

    Reiturinn **Magn sem stofna á** inniheldur sjálfgefið línumagn en því má breyta.  

7.  **Veljið stofna nýtt lotunr.** gátreit til að skipuleggja nýju raðtölurnar í greinilegu lotu.  
7. Velja hnappinn **Í lagi**.  

[!INCLUDE [prod_short](includes/prod_short.md)] stofnar lotunúmer með einstökum raðnúmerum samkvæmt vörumagni í fylgiskjalslínunni. Númerið er forfast með gildinu sem fært var inn í  **svæðið SÉRSNIÐIÐ sn** . T.d. að ræsa frá  **S/N-Vend0001**.  

Magnreitirnir í hausnum Sýna magn og samtölur vörurakningarnúmeranna sem eru skilgreind á síðunni. Magnið verður að samsvara þeim í fylgiskjalslínum sem eru tilgreind með  **0**  í  **svæðinu Óskilgreint** .  

Þegar skjalið er bókað flytja vörurakningarfærslurnar í birgðafærslurnar.

### Meðhöndla rað- og lotunúmer þegar móttökulínur eru sóttar úr innkaupareikningi

Þegar bókaðar voru innhreyfingar eða afhendingarlínur úr tengdum reikningum eða kreditreikningum eru Vörurakningarlínur í vöruhúsaskjölunum sjálfkrafa færðar inn. Þær eru þó unnar á sérstakan hátt.

Aðgerðin styður við eftirfarandi ferli á innleið:  

- **Sækja móttökulínur** - úr innkaupareikningi.  
- **Sækja skilaafhend.línur** - úr innkaupakreditreikningi.  

Aðgerðin styður við eftirfarandi ferli á útleið:  

- **Sækja afhendingarlínur** - úr sölureikningi eða tengdum afhendingum.  
- **Sækja vöruskilamóttökulínur** - úr sölukreditreikningi.  

Í þeim tilfellum eru vörurakningarlínurnar sendist á reikninginn eða kreditreikning en á  **síðunni Vörurakningarlínur**  er ekki hægt að breyta rað-eða lotunúmerum. Aðeins er hægt að breyta magninu.  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Innkaupareikningur** og velja síðan viðkomandi tengil.  
2. Opna innkaupareikning fyrir vörur sem eru innkaup með rað- eða lotunúmerum.  
3. Frá línu innkaupareiknings á flýtiflipanum **Línur** skal velja **Sækja móttökulínur** aðgerðina.  
4. Á síðunni **Sækja móttökulínur** veljið móttökulínu sem eru með vörurakningarlínur og veljið svo hnappinn **Í lagi**.  

    Upprunaskjalið er afritað í innkaupareikninginn sem ný lína og vörurakningarlínurnar afritaðar af síðunni **Vörurakningarlínur** sem liggur að baki.  

5. Á innkaupareikningi skal velja innfluttu móttökulínuna.  
6.  **Á vöruflipanum línur**  er línuaðgerðin  **valin**  og síðan er  **aðgerðin vörurakningaraðgerð**  fundin til að finna fluttar vörurakningarlínurnar.  

Ekki er hægt að  **breyta raðnúmeri.** og  **Lotunr.** svæði. Hins vegar er hægt að eyða fullklárnum línum eða breyta magni til að stemma stigu við breytingum á upprunalínunni.  

## Úthlutun rað- eða lotunúmera vegna færslna á leið út.

Útleiðarvinnsla rað- eða lotunúmera er verkhluti sem gerist við mörg mismunandi vöruhúsaferli. Tvær leiðir eru færar til að bæta við rað- og lotunúmerum fyrir færslur á útleið:  

- Veljið úr fyrirliggjandi rað-eða lotunúmerum. Þetta gildir þegar vörurakningarnúmerum er þegar úthlutað í færslum á innleið.
- Úthluta nýjum rað-eða lotunúmerum á hreyfingar á útleið. Þetta á við þegar vörurakningarnúmer eru ekki tengd við vörur fyrr en þær eru seldar og tilbúnar til sendingar.

### Valið úr tiltækum rað- og lotunúmerum  

Þegar unnið er með vörur sem krefjast vörurakningu og verið er að stofna útfærslur, þarf vanalega að velja lotu-eða raðnúmer sem eru þegar til.

1. Af skjali á útleið er valin lína sem á að velja rað- eða lotunúmer í.  
2. Áflýtiflipanum **Línur** skal velja aðgerðina **Lína**, svo **Tengdar upplýsingar** og loks **Vörurakningarlínur**.  
3. Á síðunni **Vörurakningarlínur** er um þrennt að velja þegar kemur að því að tilgreina lotu- eða raðnúmer:  

   -  **Veljið raðnr.** og síðan er valið númer á  **raðnr. Listasíðu** .
   -  **Veljið lotunúmer.** og síðan er númer á  **reitnum lotunúmer valið. Listasíðu** . Síðan skal velja  **Raðnúmer.** og velja númer á  **raðnr. Listasíðu** .
   -  **Velja vinnsluaðgerðina**  og velja síðan  **velja færslur**. Síðan **Velja færslur** sýnir öll lotu- og raðnúmer ásamt upplýsingum um það hvað er til.

4.  **Í reitinn valið magn**  er fært inn magnið af hverri lotu eða raðnúmeri sem á að nota.
5. Velja hnappinn **Í lagi**. Vörurakningarupplýsingarnar eru yfirfærir  **á síðuna Vörurakningarlínur** .  

Magnreitirnir í hausnum Sýna magn og samtölur vörurakningarnúmeranna sem eru skilgreind á síðunni. Magnið verður að samsvara þeim fylgiskjalslínunni sem er tilgreind með  **0**  í  **reitnum Óskilgreint** .  

Þegar fylgiskjalslínan er bókuð flytur vörurakningarupplýsingarnar í viðkomandi birgðabókafærslur.

### Til að úthluta nýjum rað- eða lotunúmerum  

Þetta ferli á við þegar vörur eru ekki með rað-eða lotunúmer meðan þær eru í birgðum. Þess í stað er vörurakningarnúmerum úthlutað þegar vörur eru seldar og tilbúnar til afhendingar. Í þessu tilfelli er vanalega hægt að tengja númer úr fyrirfram ákveðinni númeraröð.

1. Valin er viðkomandi fylgiskjalslína, t.d. sölureikningur eða sölupöntun, og á flýtiflipanum **Línur** skal velja aðgerðina **Lína**, svo **Tengdar upplýsingar** og loks aðgerðina **Vörurakningarlínur**.  

    Hægt er að úthluta vörurakningarnúmerum með eftirtöldum aðferðum:  
    - Sjálfkrafa, úr fyrirfram ákveðinni númeraröð: Velja reitnum  **úthluta raðnr.** eða  **úthluta Lotunr.** aðgerð.  
    - Sjálfvirkt, á grundvelli færibreyta sem notandi skilgreinir sérstaklega fyrir útleiðarvöruna: Velja aðgerðina **Stofna sérsniðið RN**.  
    - Handvirkt með því að færa inn rað-eða lotunúmer án þess að nota númeraröð.  

2. Í þessu ferli skal úthluta raðnúmeri sjálfkrafa með því að velja **Úthluta raðnúmeri**.  

     **Í reitnum Magn til stofnunar**  er sjálfgefið magn í línunni en hægt er að breyta því.  
3. Gátmerki er sett í reitinn **Stofna nýtt lotunr.** svo að nýju raðnúmerin flokkist í sérstaka lotu.  
4. Veldu hnappinn **Í lagi** og stofnar kerfið þá lotunúmer og ný einstök raðnúmer samkvæmt magninu til afgreiðslu í viðkomandi fylgiskjalslínum.  

Magnreitirnir efst Sýna magn og samtölur vörurakningarnúmeranna sem eru skilgreind á síðunni. Magnið verður að samsvara þeim fylgiskjalslínunni sem er tilgreind með  **0**  í  **reitnum Óskilgreint** .  

Þegar fylgiskjalið er bókað eru vörurakningarfærslurnar færðar í birgðafærslurnar.

### Úthluta rakningarnúmerum í upprunaskjölum

Sum fyrirtæki skilgreina ákveðin rað-eða lotunúmer í upprunaskjali, til dæmis sölupantanir. Ef viðskiptamaður biður til dæmis um ákveðna lotu. Þegar tínsluskjal birgða-eða Vöruhúsatínsla er stofnað úr upprunaskjali á útleið þar sem rað-eða lotunúmer eru þegar skilgreind er ekki hægt að breyta hvaða reitum sem er á  **síðunni Vörurakningarlínur**  undir birgðatínslu. Ein undantekningin er  **reiturinn Magn til afgreiðslu** . Í því tilvikum eru vörurakningarnúmer tilgreind í aðskildum frágangs-/tínslulínum í birgðatínslulínunum. Magninu hefur þegar verið skipt í sérstakar samstæður rað- eða lotunúmera því í sölupöntuninni eru vörurakningarnúmerin sem á að afhenda tilgreind.

## Hvernig á að meðhöndla rað- og lotunúmer í millifærslupöntunum

Ferlum við meðferð rað- og lotunúmera sem verið er að flytja milli birgðastöðva svipar til þeirra sem beitt er þegar vara er keypt og seld.  

Flutningspantanir eru hins vegar einstakar í þeirri sendingu og innhreyfingar eru báðar gerðar úr sömu flutningslínu og nota sama tilvik af  **síðunni Vörurakningarlínur** . Vörurakningarnúmer sem afhent eru frá einum stað þurfa að berast óbreytt á öðrum stað.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Flutningspantanir** og velja síðan viðkomandi tengil.  
2. Opna skal flutningspöntunina sem á að vinna. Á flýtiflipanum **Línur** skal velja aðgerðina **Lína**, velja aðgerðina **Vörurakningarlínur** og loks aðgerðina **Afhending**.  
3. Á síðunni **Vörurakningarlínur** er rað- eða lotunúmerum úthlutað eða þau valin eins og fyrir hverja aðra útleiðar-birgðafærslu.  

    Þegar rað-og lotunúmer er meðhöndlað fyrir flutningsvörur eru tölur yfirleitt þegar úthlutað númerum. Þess vegna velur þú oft úr fyrirliggjandi rað-eða lotunúmerum.  

4. Millifærslapöntunin er bókuð, fyrst skip og síðan Móttaka, til að skrá að vörurnar séu fluttar og bera Vörurakningarfærslur þeirra.  

Við flutninginn er ekki hægt að breyta gildum á  **síðunni Vörurakningarlínur** .  

## Skráning viðbótarupplýsinga um rað- og lotunúmer

Ef tengja þarf sérstakar upplýsingar við vörurakningarnúmer, til dæmis vegna gæðakerfanna, er hægt að gera það á upplýsingakorta fyrir rað-eða lotunúmer.

1. Opna skjal sem hefur verið úthlutað rað- eða lotunúmerum.
2. Opnaðu síðuna **Vörurakningarlínur** fyrir vöruna sem á að slá inn upplýsingar fyrir.
3. Velja aðgerðina **Lína** og svo, til dæmis, aðgerðina **Raðnr. upplýsingaspjalds**  
4. Veljið plúsmerkið **(+)** efst á listanum til að búa til nýja færslu. Reitirnir **Raðnúmer** og **Lotunr.** eru fyllt út fyrirfram úr vörurakningarlínunni.
5. Færa inn stuttan texta í reitinn **Lýsing**, til dæmis um ástand vörunnar.  
6. Velja aðgerðina **Tengt**, veljið aðgerðina **Raðnúmer** og svo aðgerðina **Athugasemd** til að stofna aðra athugasemdaskrá.  
7. Veljið reitinn **Lokaður** til að sleppa rað- eða lotunúmerinu úr færslum.  

<!--If you create serial numbers in bulk by using the **Create Customized SN** or **Assign Serial No.** actions, you can enable **Create SN Information** and an information card will be created for each tracking line.

Alternatively, you can create an information card when you post journals or documents. On the **Item Tracking Code** page, turn on the **Create SN Info. on posting** or **Create SN Info. on posting** toggles. -->

Hægt er að breyta stofnuðum rað- eða lotuupplýsingaspjöldum síðar.

## Breyta fyrirliggjandi upplýsingum um rað- og lotunúmer

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Vörur** og velja síðan viðkomandi tengil.  
2. Velja vöru sem hefur vörurakningarkóða og upplýsingar um rað- eða lotunúmer.
3. Á síðunni **Birgðaspjald** skal velja aðgerðina **Færslur** og velja síðan **Fjárhagsfærslur**.
4. Velja reitinn **Lotunr.** eða **Raðnúmer**. Ef upplýsingar eru til fyrir þetta vörurakningarnúmer þá mun síðan **Lotunr. upplýsingalista** eða **Raðnr. upplýsingalista** opnast.  
5. Velja skal spjald og síðan **Lotunr./raðnúmeraupplýsingaspjald** aðgerðina.  
6. Breyta stuttri lýsingu, athugasemdafærslu eða reitnum **Lokaður**.  

Ekki er hægt að breyta rað-eða lotunúmerum eða magni. Til að gera það verður að endurflokka birgðafærslu færslunnar. Til að fræðast meira um endurflokkun er farið í  [endurflokka lotunúmer eða raðnúmer](inventory-how-work-item-tracking.md#to-reclassify-serial-or-lot-numbers).

## Endurflokka rað- eða lotunúmer

Endurflokkun vörurakningar fyrir vöru þýðir að lotu eða raðnúmeri er breytt í nýja lotu eða raðnúmer eða að breyta lokadagsetningu í nýja lokadagsetningu. Ef notaðar eru lotur er einnig hægt að steypa margar lotur inn í eina. Notið endurflokkunarbók vöru til að gera þessi verk.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Vöruendurflokkunarbók** og velja síðan viðkomandi tengil.  
2. Línan er fyllt út með viðeigandi upplýsingum. Nánari upplýsingar er að finna í [Telja birgðir með skjölum](inventory-how-count-inventory-with-documents.md) eða [Telja, leiðrétta og endurflokka birgðir með Færslubókum](inventory-how-count-adjust-reclassify.md).
3. Velja aðgerðina **Vörurakningarlínur**  
4. Í reitnum **Raðnr.** eða **Lotunr** skal velja gildandi rað- eða lotunúmer.  
5. Hægt er að slá inn nýtt vörurakningarnúmer með því að slá það inn í reitinn **Nýtt raðnr.** eða **Nýtt lotunr.**. Hægt er að sameina eina eða fleiri lotur við eina nýja lotu eða lotu sem er til fyrir.  

    > [!NOTE]  
    > Þegar lokadagsetning er endurlögð eru vörur með elstu lokadagsetningar fyrir færslur á útleið lagðar fyrst. Til að fá frekari upplýsingar er farið í  [Tiltekt með FEFO](warehouse-picking-by-fefo.md).  

6. Ef tilgreina á nýjan gildistíma fyrir rað-eða lotunúmerið er það fært inn í  **reitinn nýtt**  Lokadagsetning.  

    > [!IMPORTANT]  
    > * Ef endurflokkun er mikið í sama lotunúmerið en með annan gildistíma verður að endurflokka allt lotað með því að nota eina vöru endurflokkunarfærslubókarlínu. 
    > * Ef þú endurfærir fleiri en eitt lotu í eitt nýtt lotunúmer, sem þýðir að verið er að sameina fleiri en eitt lotu í eina nýja lotu, verður að færa inn sama lokadagsetningu fyrir allar lotur. 
    > * Ef endurflokkun er ein fyrirliggjandi lota í aðra fyrirliggjandi lotu sem hefur annan gildistíma verður að nota lokadagsetningu úr seinni lotu. 
    > * Ef reiturinn **Ný lokadagsetning** er látinn standa auður þá verður lotu- eða raðnúmerið endurflokkað með auðri lokadagsetningu.  

7. Ef til eru upplýsingar um gamla rað- eða lotunúmerið er hægt að afrita það yfir á nýja rað- eða lotunúmerið.  

    1. Á síðunni **Vörurakningarlínur** skal velja **Nýtt raðnr. upplýsingar** aðgerðina eða **Nýtt lotunr. upplýsingar** aðgerðina.  
    2. Til að afrita upplýsingar frá gamla lotu- eða raðnúmerinu er aðgerðin **Afrita upplýsingar** valin.  
    3. Á upplýsingalistasíðunni er valið það lotu- eða raðnúmer sem ætlunin er að afrita og hnappurinn **Í lagi** valinn.  

8. Hægt er að breyta upplýsingunum sem eru fyrir hendi varðandi lotu- eða raðnúmerið með því að skrá lotu- eða raðupplýsingarnar.  
9. Færslubókin er bókuð til að tengja nýju vörurakningarnúmerin eða lokadagsetningarnar við viðkomandi birgðafærslu.

## Skanna strikamerkjum við Business Seðlaforrit seðlabanka

[!INCLUDE [barcode-mobile-app](includes/barcode-mobile-app.md)]

 **Í síðunni Vörurakningarlínur**  ef óskað er eftir að skanna nokkrar raðfærslur, lotu eða pakka inn er hægt að nota margar  **Aðgerðir til**  að skanna. Þegar búið er að skanna strikamerki er gildi hans fært inn í svæðið á síðunni og næsta flýtifærslusvæði verður tiltækt. Einnig er hægt að nota teiknið strikamerkjaskanni til að fylla út ákveðinn reit.

Eftirfarandi töflur eru á lista yfir síðurnar sem styðja strikamerkóskönnun fyrir vörurakningu  [!INCLUDE [prod_short](includes/prod_short.md)]  í Mobile forritinu.

|Síða  |Gildi svæða er hægt að skanna  |
|---------|---------|
|Vörurakningarlínur     |* Raðnr.<br><br>* Nýtt raðnr.<br><br>* Lotunr.<br><br>* Nýtt lotunr.<br><br>* Pakkning nr.<br><br>* Nýr pakki nr.|
|Vöruh. Vörurakningarlínur     |* Raðnr.<br><br>* Nýtt raðnr.<br><br>* Lotunr.<br><br>* Nýtt lotunr.<br><br>* Pakkning nr.<br><br>* Nýr pakki nr.|
|Vörurakning     |* Raðnr. Afmörkun<br><br>* Lotunr. Afmörkun<br><br>* Pakkning nr. Sía |
|Færslubók atriðis     |* Raðnr.<br><br>* Lotunr.<br><br>* Pakkning nr.     |
|Vöruhúsaaðgerðalína     |* Raðnr.<br><br>* Lotunr.<br><br>* Pakkning nr.<br><br>**Athugið** : eftirfarandi síður nota síðuna Aðgerðalína vöruhúsa:<br><br>* síða 5780 "vöruhúsatínslu Velja Undirmynd "<br><br>* síða 7378 "Ívt. Velja Undirmynd "<br><br>* síða 5771 "vöruhúsatínslu Putaway Undirform "<br><br>* síða 7316 "Vöruhúsakerfi Hreyfill Undirform"<br><br>* síða 7376 "Ívt. Putaway Undirform "<br><br>* síða 7383 "Ívt. Undirform hreyfingar "        |
|Vöruh. Rauná. Innvt. Færslubók     |* Raðnr.<br><br>* Lotunr.<br><br>* Pakkning nr.         |

## Sjá einnig .

[Setja upp vörurakningu með raðnúmer, lotu og pakkanúmer](inventory-how-setup-item-tracking.md)  
[Rekja vöruraktar vörur](inventory-how-to-trace-item-tracked-items.md)  
[Birgðir](inventory-manage-inventory.md)  
[Hönnunarupplýsingar: Vörurakning](design-details-item-tracking.md)  
[Hönnunarupplýsingar - vörurakning og frátekningar](design-details-item-tracking-and-reservations.md)  
[Taka frá vörur](inventory-how-to-reserve-items.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
