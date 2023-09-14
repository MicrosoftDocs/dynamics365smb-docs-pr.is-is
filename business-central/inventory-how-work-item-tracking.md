---
title: 'Rekja vörur með rað-, lotu- og pakkanúmerum'
description: 'Hægt er að bæta við raðnúmerum, lotunúmerum og pakkanúmerum við hvaða útleiðarskjal eða innleiðarskjal sem er og bókaðar færslur þess er síðan hægt að skoða í viðkomandi birgðafærslum.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.search.forms: '6503, 6515, 6513, 6512, 6502, 6506, 6501, 6510, 6507, 6500, 6505, 6508, 9126, 6526, 6516, 6511, 6504, 6509, 163, 6550,'
ms.date: 08/31/2021
ms.author: bholtorf
---
# Rekja vörur með rað-, lotu- og pakkanúmerum

Hægt er að úthluta raðnúmerum, lotunúmerum og pakkanúmerum við hvaða útleiðarskjal eða innleiðarskjal sem er og bókaðar færslur þess er síðan hægt að skoða í viðkomandi birgðafærslum. Þú framkvæmir vinnuna á síðunni **Vörurakningarlínur** sem hægt er að opna úr skjali á innleið eða útleið.

Fylki magnreita efst á síðunni **Vörurakningarlínur** birtir magn og summu vörurakningarnúmera sem verið er að skilgreina á línunum. Magnið verður að samsvara því sem er í fylgiskjalslínunni, sem er sýnt með 0 undir **Óskilgreint** reitunum.

Til að mæla afköst safnar forritið ráðstöfunarupplýsingum af síðunni **Vörurakningarlínur** eingöngu einu sinni, þegar hann er opnaður. Þetta þýðir að forritið uppfærir ekki ráðstöfunarupplýsingarnar á meðan síðan er höfð opin, jafnvel þó að breytingar eigi sér stað í birgðum eða í öðrum skjölum á þeim tíma.

> [!NOTE]  
>  Til þess að eiginleikarnir sem lýst er í þessari grein virki þarf fyrst að setja upp vörurakningu. Frekari upplýsingar er að finna í [Setja upp vörurakningu með raðnúmer, lotu og pakkanúmer](inventory-how-setup-item-tracking.md)

## Vörurakning til ráðstöfunar

Þegar unnið er með rað-, lotu- og pakkanúmer reiknar [!INCLUDE[prod_short](includes/prod_short.md)] út upplýsingar um framboð og sýnir það á hinum ýmsu síðum vörurakningar. Þetta gerir það mögulegt að sjá hversu mikið af lotu-, pakka- eða raðnúmerum er nú þegar verið að nota fyrir önnur fylgiskjöl. Þetta minnkar villur og óvissu vegna tvöfaldra úthlutana.

Á síðunni **Vörurakningarlínur** er viðvörunartákn sýnt í reitunum **Lotunr. til ráðstöfunar** eða **Raðnr. til ráðstöfunar** ef eitthvað af magninu sem valið var, eða það allt, er notað í öðrum skjölum eða hvort lotu- eða raðnúmerið er ekki fyrir hendi.

Á síðunum **Lotunr./Raðnr.-listi**, **Lotunr./Raðnr.-ráðstöfunarmagn** og **Vörurakning - Valdar færslur** eru birtar upplýsingar um það hversu mikið magn af vöru er verið að nota. Þetta felur í sér eftirfarandi upplýsingar.

|Svæði|Description|
|-----|-----------|  
|**Heildarmagn**|Heildarmagn þeirra vara sem eru í birgðum.|
|**Umbeðið magn samtals**|Heildarfjöldi þeirra vara sem beðið er um og verða notuð í þessu og öðrum skjölum.|
|**Magn í undirbúningi**|Fjöldi þeirra vara sem búið er að biðja um að nota í núverandi skjali en hefur ekki enn verið bundið við gagnagrunninn.|
|**Umbeðið magn**|Fjöldi þeirra vara sem búið er að biðja um að nota í núverandi skjali.|
|**Heildarmagn tiltækt**|Heildarfjöldi atriða í birgðum, að frádregnu magni varanna sem beðið er um í þessu skjali og öðrum skjölum (umbeðið magn samtals) að frádregnu magninu sem beðið er um en hefur ekki verið fært í skjalið (magn í undirbúningi).|

Ef unnið er á síðunni **Vörurakningarlínur** í langan tíma eða ef mikið er um aðgerðir með þeirri vöru sem verið er að vinna með er hægt að velja **Endurnýjun ráðstöfunar**. Að auki er ráðstöfun vörunnar endurskoðuð sjálfkrafa þegar síðunni er lokað til að fá staðfestingu á því að engin ráðstöfunarvandamál eru fyrir hendi.

## Úthlutun rað- eða lotunúmera á færslur á leið inn.

Það getur komið fyrirtækjum vel að hægt sé að rekja vöru frá því hún berst fyrirtækinu. Þegar svo háttar til er innkaupapöntun oft helsta vísbendingin, en vörurakningu má gera út frá hvaða skjali sem er og færslur í því birtar í samsvarandi birgðafærslum.

Þannig flytjast tölurnar sjálfkrafa í gegnum allar útleiðaraðgerðir í vöruhúsi án samskipta við starfsmenn í vöruhúsi.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Innkaupapantanir** og velja síðan viðkomandi tengil.  
2. Annaðhvort skal opna innkaupapöntun sem þegar er til eða stofna nýja.
3. Valin er viðkomandi fylgiskjalslína og á flýtiflipanum **Línur** skal velja aðgerðina **Lína** og loks aðgerðina **Vörurakningarlínur** til að opna síðuna **Breyta – vörurakningarlínur**.  

    Nú er hægt að úthluta rað- eða lotunúmerum á eftirfarandi hátt:  
    -   Sjálfvirkt, með því að velja **Vinna** og svo **Úthluta raðnr.** eða **Úthluta lotunr.** og úthlutar kerfið þá rað- eða lotunúmerum úr forskilgreindum númeraröðum.  
    -   Sjálfvirkt, með því að velja **Vinna** og svo **Stofna sérsniðin RN**, og úthlutar þá kerfið rað- eða lotunúmerum samkvæmt númeraröðum sem notandi skilgreinir sérstaklega fyrir mótteknar vörur.  
    -   Handvirkt með því að færa inn rað- eða lotunúmer beint, t.d. númer birgis.  
    -   Handvirkt með því að úthluta hverri vörueiningu sérstöku númeri.  

4. Til að úthluta sjálfvirkt skal velja **Stofna sérstillt raðnúmer** aðgerðina.  
5. Í reitinn **Sérsniðin raðnr.** er fært inn upphafsnúmer lýsandi númeraraðar, t.d. **r.nr.-Birg0001**.  
6. Í reitinn **Hækka** er færð talan 1 til að tiltaka að hvert raðnúmer hækkar um einn.  

    Reiturinn **Magn sem stofna á** inniheldur sjálfgefið línumagn en því má breyta.  

7. Gátmerki er sett í gátreitinn **Stofna nýtt lotunr.** svo að nýju raðnúmerin flokkist í sérstaka lotu.  
7. Velja hnappinn **Í lagi**.  

Lotunúmer með einstökum raðnúmerum er stofnað eftir vörumagni í skjalslínu og er byrjað á **r.nr.-Birg0001**.  

Magnreitirnir í hausnum sýna magn og samtölur vörurakningarnúmeranna sem eru skilgreind á síðunni. Magnið verður að samsvara því sem er í fylgiskjalslínunni, og er sýnt með í reitunum **Óskilgreint**.  

Þegar fylgiskjalið er bókað eru vörurakningarfærslurnar fluttar í tengdar birgðafærslur.

### Meðhöndla rað- og lotunúmer þegar móttökulínur eru sóttar úr innkaupareikningi

Þegar notuð er aðgerð til að sækja bókaðar kvittanir eða afhendingarlínur frá tengdum reikningum eða kreditreikningum þá eru vörurakningarlínur í vöruhúsaskjölum færðar sjálfkrafa. Hins vegar eru þær unnar á sérstakan hátt.

Aðgerðin styður við eftirfarandi ferli á innleið:  
-   **Sækja móttökulínur** - úr innkaupareikningi.  
-   **Sækja skilaafhend.línur** - úr innkaupakreditreikningi.  

Aðgerðin styður við eftirfarandi ferli á útleið:  
-   **Sækja afhendingarlínur** - úr sölureikningi eða tengdum afhendingum.  
-   **Sækja vöruskilamóttökulínur** - úr sölukreditreikningi.  

Í þessum tilvikum eru fyrirliggjandi vörurakningarlínur afritaðar sjálfkrafa í reikninginn eða kreditreikninginn en síðan **Vörurakningarlínur** leyfir ekki breytingar á rað- eða lotunúmerum - aðeins er hægt að breyta magni. Aðeins er hægt að breyta magni.  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Innkaupareikningur** og velja síðan viðkomandi tengil.  
2. Opna innkaupareikning fyrir vörur sem eru innkaup með rað- eða lotunúmerum.  
3. Frá línu innkaupareiknings á flýtiflipanum **Línur** skal velja **Sækja móttökulínur** aðgerðina.  
4. Á síðunni **Sækja móttökulínur** veljið móttökulínu sem eru með vörurakningarlínur og veljið svo hnappinn **Í lagi**.  

    Upprunaskjalið er afritað í innkaupareikninginn sem ný lína og vörurakningarlínurnar afritaðar af síðunni **Vörurakningarlínur** sem liggur að baki.  

5. Í glugganum innk. kr. veljið fluttu móttökulínuna.  
6. Á flýtiflipanum **Línur** skal velja aðgerðina **Lína**, og svo velja aðgerðina **Vörurakningarlínur**  til að sjá vörurakningarlínurnar sem hafa verið færðar.  

Ekki er hægt að breyta efni reitanna  **Raðnr.** og  **Lotunr.** Þó er hægt að eyða heilum línum eða breyta magni til samræmis við breytingarnar í upprunalínunni.  

## Úthlutun rað- eða lotunúmera vegna færslna á leið út.

Útleiðarvinnsla rað- eða lotunúmera er verkhluti sem gerist við mörg mismunandi vöruhúsaferli. Tvær leiðir eru færar til að bæta við rað- og lotunúmerum fyrir færslur á útleið:  

-   Valið úr tiltækum rað- og lotunúmerum Þetta á við þegar vörurakningarnúmerum hefur þegar verið úthlutað við færslu á innleið.
-   Nýjum rað- eða lotunúmerum úthlutað við færslur á útleið. Þetta á við þegar vörurakningarkóðum er ekki úthlutað á vörur fyrr en þær eru seldar og tilbúnar til afhendingar.

### Valið úr tiltækum rað- og lotunúmerum  

Þegar unnið er með vörur sem krefjast vörurakningar og verið er að stofna færslur á útleið (þar sem vörur fara úr birgðum) þarf yfirleitt að velja lotu- eða raðnúmerið frá þeim sem eru til fyrir í birgðum.

1. Af skjali á útleið er valin lína sem á að velja rað- eða lotunúmer í.  
2. Áflýtiflipanum **Línur** skal velja aðgerðina **Lína**, svo **Tengdar upplýsingar** og loks **Vörurakningarlínur**.  
3. Á síðunni **Vörurakningarlínur** er um þrennt að velja þegar kemur að því að tilgreina lotu- eða raðnúmer:  

    - Velja **Raðnr.** reitinn og svo valið númer á síðunni **Raðnúmeralisti**.
    - Velja reitinn **Lotunr.** og velja svo númer á síðunni **Lotunúmeralisti**. Síðan skal velja **Raðnr.** reitinn og svo valið númer á síðunni **Raðnúmeralisti**.
    - Veljið aðgerðina **Vinna** og veljið síðan **Velja færslur**. Síðan **Velja færslur** sýnir öll lotu- og raðnúmer ásamt upplýsingum um það hvað er til.

4. Í reitnum **Valið magn** er slegið inn magn hvers lotu- eða raðnúmers sem á að nota.
5. Veldu hnappinn **Í lagi** og valdar vörurakningarupplýsingar eru færðar á síðuna **Vörurakningarlínur**.  

Magnreitirnir í hausnum sýna magn og samtölur vörurakningarnúmeranna sem skilgreind eru á síðunni. Magnið verður að samsvara því sem er í fylgiskjalslínunni, og er sýnt með **0** undir **Óskilgreint**.  

Þegar fylgiskjalið er bókað eru vörurakningarfærslurnar fluttar í tengdar birgðafærslur.

### Til að úthluta nýjum rað- eða lotunúmerum  

Þessi valkostur á við þegar birgðavörur bera ekki rað- eða lotunúmer og í staðinn er varan með vörurakningarnúmer þegar vörur eru seldar og tilbúnar til afhendingar. Í þessu tilfelli er yfirleitt úthlutað númerum úr fyrirfram skilgreindum númeraröðum.

1. Valin er viðkomandi fylgiskjalslína, t.d. sölureikningur eða sölupöntun, og á flýtiflipanum **Línur** skal velja aðgerðina **Lína**, svo **Tengdar upplýsingar** og loks aðgerðina **Vörurakningarlínur**.  

    Hægt er að úthluta vörurakningarnúmerum með eftirtöldum aðferðum:  
    -   Sjálfvirkt, úr forskilgreindum númeraröðum: Velja aðgerðina **Úthluta raðnúmeri** eða **Úthluta lotunúmeri**.  
    -   Sjálfvirkt, á grundvelli færibreyta sem notandi skilgreinir sérstaklega fyrir útleiðarvöruna: Velja aðgerðina **Stofna sérsniðið RN**.  
    -   Handvirkt með því að færa inn rað- og lotunúmer án þess að nota númeraraðir.  

2. Í þessu ferli skal úthluta raðnúmeri sjálfkrafa með því að velja **Úthluta raðnúmeri**.  

    Reiturinn **Magn sem stofna á** inniheldur sjálfgefið línumagn en því má breyta.  
3. Gátmerki er sett í reitinn **Stofna nýtt lotunr.** svo að nýju raðnúmerin flokkist í sérstaka lotu.  
4. Veldu hnappinn **Í lagi** og stofnar kerfið þá lotunúmer og ný einstök raðnúmer samkvæmt magninu til afgreiðslu í viðkomandi fylgiskjalslínum.  

Fylki magnreitanna efst sýna á gagnvirkan hátt magn og samtölur vörurakningarnúmeranna sem eru skilgreind á síðunni. Magnið verður að samsvara því sem er í fylgiskjalslínunni, og er sýnt með **0** undir **Óskilgreint**.  

Þegar fylgiskjalið er bókað eru vörurakningarfærslurnar fluttar í tengdar birgðafærslur.

### Úthluta rakningarnúmerum í upprunaskjölum

Í sérstökum tilvikum varðandi rað- og lotunúmeraðar birgðir, eru sérstök rað- og lotunúmer skilgreind í upprunaskjalinu, t.d. sem sölupöntun, sem starfsmaður í vöruhúsi verður að taka tillit til við afgreiðslu úr vöruhúsi. Þetta getur verið vegna þess að viðskiptavinurinn bað um ákveðna lotu í framleiðsluferlinu. Þegar birgðatínslu- eða vöruhúsatínsluskjal er stofnað úr upprunaskjali á útleið þar sem rað- eða lotunúmer eru þegar skilgreind þá eru allir reitir á síðunni **Vörurakningarlínur** undir birgðatínslunni skrifvarðir nema reiturinn **Magn til afgreiðslu**. Í því tilvikum eru vörurakningarnúmer tilgreind í aðskildum frágangs-/tínslulínum í birgðatínslulínunum. Magninu hefur þegar verið skipt í sérstakar samstæður rað- eða lotunúmera því í sölupöntuninni eru vörurakningarnúmerin sem á að afhenda tilgreind.

## Hvernig á að meðhöndla rað- og lotunúmer í millifærslupöntunum

Ferlum við meðferð rað- og lotunúmera sem verið er að flytja milli birgðastöðva svipar til þeirra sem beitt er þegar vara er keypt og seld.  

Millifærslupöntunin er þó sérstök að því leyti að sending og móttaka er framkvæmd úr sömu millifærslulínu og því er notað sama eintak af Uppsetningarspjald fyrir uppfærslu gengis **Vörurakningarlínur**. Þetta merkir að vörurakningarnúmer sem send eru úr einni birgðageymslu verður að móttaka óbreytt í annarri birgðageymslu.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Flutningspantanir** og velja síðan viðkomandi tengil.  
2. Opna skal flutningspöntunina sem á að vinna. Á flýtiflipanum **Línur** skal velja aðgerðina **Lína**, velja aðgerðina **Vörurakningarlínur** og loks aðgerðina **Afhending**.  
3. Á síðunni **Vörurakningarlínur** er rað- eða lotunúmerum úthlutað eða þau valin eins og fyrir hverja aðra útleiðar-birgðafærslu.  

    Þegar unnið er við rað- og lotunúmer vegna millifærsluvöru er yfirleitt búið að úthluta vörunni númerum. Þess vegna felst ferlið yfirleitt í því að velja úr þeim rað- eða lotunúmerum sem fyrir eru.  

4. Millifærslupöntunin, fyrst afhending og síðan móttaka, er bókuð til þess að skráð sé að varan sé flutt með vörurakningarfærslum.  

Meðan á millifærslu stendur er síðan **Vörurakningarlínur** skrifvarin.  

## Skráning viðbótarupplýsinga um rað- og lotunúmer

Ef tengja þarf einhverjar upplýsingar við tiltekið vörurakningarnúmer, t.d. vegna gæðaeftirlits, er hægt að gera það á upplýsingaspjaldinu fyrir rað- eða lotunúmer.

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

Ekki er hægt að breyta rað- eða lotunúmerum eða magni. Til að gera það verður að endurflokka birgðabókarfærsluna í spurningu. Nánari upplýsingar er að finna í [Endurflokkun lotu- eða raðnúmera](inventory-how-work-item-tracking.md#to-reclassify-serial-or-lot-numbers).

## Endurflokka rað- eða lotunúmer

Endurflokkun vörurakningar fyrir vöru þýðir að breyta lotu- eða raðnúmeri í nýtt lotu- eða raðnúmer eða breyta lokadagsetningunni í nýja lokadagsetningu. Ef verið er að vinna með lotur er líka hægt að sameina margar lotur í eina lotu. Þessi verkefni eru framkvæmd með notkun vöruendurflokkunarbókarinnar.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Vöruendurflokkunarbók** og velja síðan viðkomandi tengil.  
2. Línan er fyllt út með viðeigandi upplýsingum. Nánari upplýsingar er að finna í [Telja birgðir með skjölum](inventory-how-count-inventory-with-documents.md) eða [Telja, leiðrétta og endurflokka birgðir með Færslubókum](inventory-how-count-adjust-reclassify.md).
3. Velja aðgerðina **Vörurakningarlínur**  
4. Í reitnum **Raðnr.** eða **Lotunr** skal velja gildandi rað- eða lotunúmer.  
5. Hægt er að slá inn nýtt vörurakningarnúmer með því að slá það inn í reitinn **Nýtt raðnr.** eða **Nýtt lotunr.**. Hægt er að sameina eina eða fleiri lotur við eina nýja lotu eða lotu sem er til fyrir.  

    > [!NOTE]  
    >  Athuga skal að þegar notandi endurflokkar fyrningardagsetningar, eru þær vörur sem hafa elstu lokadagsetningarnar fyrir færslur á útleið lagðar til fyrst. Frekari upplýsingar eru í [Tínsla skv. FEFO](warehouse-picking-by-fefo.md).  

6. Hægt er að slá inn nýja lokadagsetningu fyrir rað- eða lotunúmerið með því að slá það inn í reitinn **Ný lokadagsetning**.  

    > [!IMPORTANT]  
    >  Ef verið er að endurflokka lotu á sama lotunúmer en með aðra lokadagsetningu þá þarf að endurflokka alla lotuna með því að nota línu einnar vöru í endurflokkunarbókinni. Ef verið er að endurflokka meira en eina lotu á fleira en eitt lotunúmer, sem þýðir að verið er að sameina fleiri en eina lotu inn í eina nýja lotu, þá þarf að slá sömu lokadagsetningu inn fyrir allar loturnar. Ef verið er að endurflokka eina lotu sem er í annarri lotu en hefur aðra lokadagsetningu þá þarf að nota lokadagsetningu seinni lotunnar. Ef reiturinn **Ný lokadagsetning** er látinn standa auður þá verður lotu- eða raðnúmerið endurflokkað með auðri lokadagsetningu.  

7. Ef til eru upplýsingar um gamla rað- eða lotunúmerið er hægt að afrita það yfir á nýja rað- eða lotunúmerið.  

    1. Á síðunni **Vörurakningarlínur** skal velja **Nýtt raðnr. upplýsingar** aðgerðina eða **Nýtt lotunr. upplýsingar** aðgerðina.  
    2. Til að afrita upplýsingar frá gamla lotu- eða raðnúmerinu er aðgerðin **Afrita upplýsingar** valin.  
    3. Á upplýsingalistasíðunni er valið það lotu- eða raðnúmer sem ætlunin er að afrita og hnappurinn **Í lagi** valinn.  

8. Hægt er að breyta upplýsingunum sem eru fyrir hendi varðandi lotu- eða raðnúmerið með því að skrá lotu- eða raðupplýsingarnar.  
9. Færslubókin er bókuð til að tengja nýju vörurakningarnúmerin eða lokadagsetningarnar við viðkomandi birgðafærslu.

## Sjá tengda [Microsoft þjálfun](/training/modules/prepare-item-tracking/)

## Sjá einnig .

[Setja upp vörurakningu með raðnúmer, lotu og pakkanúmer](inventory-how-setup-item-tracking.md)  
[Rekja vöruraktar vörur](inventory-how-to-trace-item-tracked-items.md)  
[Birgðir](inventory-manage-inventory.md)  
[Hönnunarupplýsingar: Vörurakning](design-details-item-tracking.md)  
[Hönnunarupplýsingar - vörurakning og frátekningar](design-details-item-tracking-and-reservations.md)  
[Taka frá vörur](inventory-how-to-reserve-items.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
