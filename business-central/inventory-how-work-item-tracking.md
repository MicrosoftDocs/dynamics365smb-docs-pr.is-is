---
title: 'Rekja vörur með rað-, lotu- og pakkanúmerum'
description: 'Hægt er að bæta við raðnúmerum, lotunúmerum og pakkanúmerum við hvaða útleiðarskjal eða innleiðarskjal sem er og bókaðar færslur þess er síðan hægt að skoða í viðkomandi birgðafærslum.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.forms: '6503, 6515, 6513, 6512, 6502, 6506, 6501, 6510, 6507, 6500, 6505, 6508, 9126, 6526, 6516, 6511, 6504, 6509, 163, 6550,'
ms.date: 05/16/2024
ms.custom: bap-template
ms.service: dynamics-365-business-central
---
# Rekja vörur með rað-, lotu- og pakkanúmerum

Hægt er að úthluta raðnúmerum, lotunúmerum og pakkanúmerum á hvaða skjal á útleið eða innleið sem er og eru bókaðar vörurakningarfærslur birtar í tengdum birgðafærslum. Hægt er að rekja vörur á síðunni **Vörurakningarlínur** sem hægt er að opna úr skjölum á innleið eða útleið.

Magnreitirnir efst á síðunni **Vörurakningarlínur** sýna magn og samtölur vörurakningarnúmeranna sem skilgreind eru í línunum. Magnið verður að samsvara því sem er í fylgiskjalslínunum, sem er gefið til kynna með *0* í reitunum **Óskilgreint** .

[!INCLUDE [prod_short](includes/prod_short.md)] uppfærir ráðstöfunarupplýsingarnar á síðunni **Vörurakningarlínur** þegar síðan er opnuð. Upplýsingarnar eru ekki uppfærðar meðan síðan er opin, jafnvel þótt breytingar verði á birgðum eða öðrum fylgiskjölum á þeim tíma.

> [!NOTE]  
> Til að aðgerðirnar sem lýst er í þessari grein verði að setja upp vörurakningu. Nánari upplýsingar eru notaðar til að [setja upp vörurakningu með rað-, lotu- og pakkanúmerum](inventory-how-setup-item-tracking.md).

## Vörurakning til ráðstöfunar

Þegar unnið er með rað-, lotu- og pakkanúmer [!INCLUDE[prod_short](includes/prod_short.md)]  reiknar út ráðstöfunarupplýsingar og sýnir upplýsingarnar á ýmsum vörurakningarsíðum. Þar sést hversu mikið af lotu-, pakka- eða raðnúmeri er notað í öðrum skjölum. Þessar upplýsingar hjálpa til við að draga úr villum og óvissu sem tvöföld úthlutun stafar af.

Á síðunni **Vörurakningarlínur** gæti viðvörunartákn sýnt á síðunni **Til ráðstöfunar, Lotunr.** eða **Til ráðstöfunar, Raðnúmer** af eftirfarandi ástæðum:

* Ef eitthvað eða allt magn sem valið hefur verið er þegar notað í öðrum skjölum.
* Ef lotu- eða raðnúmerið er ekki tiltækt.

Síðurnar **Lotunr./Raðnr.-listi**, **Lotunr./Raðnr.-til ráðstöfunar** og **Vörurakning - Velja færslur** sýna magn vöru sem er í notkun. Eftirfarandi tafla sýnir viðeigandi reiti.

|Svæði|Heimildasamstæða|
|-----|-----------|  
|**Heildarmagn**|Heildarfjöldi þeirra vara sem eru í birgðum.|
|**Umbeðið magn samtals**|Heildarfjöldi þeirra vara sem beðið er um í þessu og öðrum skjölum.|
|**Magn í undirbúningi**|Fjöldi þeirra vara sem beðið er um í gildandi skjali en er ekki bókaður.|
|**Umbeðið magn**|Fjöldi þeirra vara sem búið er að biðja um að nota í núverandi skjali.|
|**Heildarmagn tiltækt**|Heildarfjöldi þeirra vara í birgðum, að frádregnum umbeðnum vörum í þessu og öðrum skjölum (allt umbeðið magn) og að frádregnu því magni sem hefur verið beðið um en hefur ekki enn verið bókað í þetta skjal (magn þess sem nú er beðið eftir).|

Ef unnið er á síðunni **Vörurakningarlínur** í langan tíma eða ef mikið er um aðgerðir með vörunni sem verið er að vinna með er hægt að velja aðgerðina **Endurnýja til ráðstöfunar** . Einnig er ráðstafað sjálfkrafa í ráðstöfunarmagn vörunnar þegar síðunni er lokað til að staðfesta að ekki séu tiltæk vandamál.

## Úthlutun rað- eða lotunúmera á færslur á leið inn.

Hugsanlega þarf að rekja vörur frá því þær berast. Í því tilviki er innkaupapöntunin oft aðalskjalið. Hins vegar er hægt að rekja vörurakningu frá hvaða skjali sem er og færslur á innleið birtast í tengdum birgðafærslum.

Rakningarnúmerin flytja sjálfkrafa í allar vöruhúsaaðgerðir á útleið.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Innkaupapantanir** og velja síðan viðkomandi tengil.  
2. Annaðhvort skal opna innkaupapöntun sem þegar er til eða stofna nýja.
3. Velja skal fylgiskjalslínuna og á flýtiflipanum **Línur** skal velja aðgerðina **Lína** og velja svo aðgerðina **Vörurakningarlínur** til að opna **síðuna Breyta - Vörurakningarlínur** .  

   Nú er hægt að úthluta rað- eða lotunúmerum á eftirfarandi hátt:  
   * Sjálfvirkt, með því að velja **Vinna** og svo **Úthluta raðnr.** eða **Úthluta lotunr.** og úthlutar kerfið þá rað- eða lotunúmerum úr forskilgreindum númeraröðum.  
   * Sjálfvirkt, með því að velja **Vinna** og svo **Stofna sérsniðin RN**, og úthlutar þá kerfið rað- eða lotunúmerum samkvæmt númeraröðum sem notandi skilgreinir sérstaklega fyrir mótteknar vörur.  
   * Handvirkt með því að færa inn rað- eða lotunúmer beint, t.d. númer birgis.  
   * Handvirkt með því að úthluta hverri vörueiningu sérstöku númeri.  

4. Til að úthluta sjálfvirkt skal velja **Stofna sérstillt raðnúmer** aðgerðina.  
5. Í reitinn **Sérsniðin raðnr** . er fært inn upphafsnúmer lýsandi raðnúmeraraðar.  **Dæmi S/N-Vend0001**.  
6. Í reitinn **Hækka** er færð talan 1 til að tiltaka að hvert raðnúmer hækkar um einn.  

    Reiturinn **Magn sem stofna á** inniheldur sjálfgefið línumagn en því má breyta.  

7. Velja skal reitinn **Stofna nýtt lotunr.** til að skipuleggja nýju raðnúmerin í sérstakri lotu.  
8. Velja hnappinn **Í lagi**.  

[!INCLUDE [prod_short](includes/prod_short.md)] stofnar lotunúmer með einstökum raðnúmerum samkvæmt vörumagninu í fylgiskjalslínunni. Númerið er forskeytið með gildinu sem fært var inn í reitinn **Sérsniðin raðnr** .. Til dæmis er byrjað á **S/N-Vend0001**.  

Magnreitirnir í hausnum sýna magn og samtölur vörurakningarnúmeranna sem skilgreind eru á síðunni. Magnið verður að samsvara því sem er í fylgiskjalslínunum, sem er tilgreint með **0** í reitnum **Óskilgreint** .  

Þegar fylgiskjalið er bókað eru vörurakningarfærslurnar fluttar í birgðafærslurnar.

### Meðhöndla rað- og lotunúmer þegar móttökulínur eru sóttar úr innkaupareikningi

Þegar bókaðar móttöku- eða afhendingarlínur eru fengnar úr tengdum reikningum eða kreditreikningum eru vörurakningarlínur í vöruhúsaskjölum sjálfkrafa fluttar. Þær eru hins vegar unnar á sérstakan hátt.

Aðgerðin styður við eftirfarandi ferli á innleið:  

* **Sækja móttökulínur** - úr innkaupareikningi.  
* **Sækja skilaafhend.línur** - úr innkaupakreditreikningi.  

Aðgerðin styður við eftirfarandi ferli á útleið:  

* **Sækja afhendingarlínur** - úr sölureikningi eða tengdum afhendingum.  
* **Sækja vöruskilamóttökulínur** - úr sölukreditreikningi.  

Í þeim tilvikum flytja vörurakningarlínurnar í reikninginn eða kreditreikninginn **en síðan Vörurakningarlínur** leyfir ekki breytingu á rað- eða lotunúmerum. Aðeins er hægt að breyta magninu.  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Innkaupareikningur** og velja síðan viðkomandi tengil.  
2. Opna innkaupareikning fyrir vörur sem eru innkaup með rað- eða lotunúmerum.  
3. Frá línu innkaupareiknings á flýtiflipanum **Línur** skal velja **Sækja móttökulínur** aðgerðina.  
4. Á síðunni **Sækja móttökulínur** veljið móttökulínu sem eru með vörurakningarlínur og veljið svo hnappinn **Í lagi**.  

    Upprunaskjalið er afritað í innkaupareikninginn sem ný lína og vörurakningarlínurnar afritaðar af síðunni **Vörurakningarlínur** sem liggur að baki.  

5. Á innkaupareikningnum er færð móttökulína valin.  
6. Á flýtiflipanum **Línur** er aðgerðin **Lína** valin og aðgerðin **Vörurakningarlínur** valin til að finna fluttar vörurakningarlínur.  

Ekki er hægt að breyta reitnum Raðnr **.** og **Lotunr.** Svæði. Hins vegar er hægt að eyða heilum línum eða breyta magni til samræmis við breytingarnar í upprunalínunni.  

## Úthlutun rað- eða lotunúmera vegna færslna á leið út.

Útleiðarvinnsla rað- eða lotunúmera er verkhluti sem gerist við mörg mismunandi vöruhúsaferli. Tvær leiðir eru færar til að bæta við rað- og lotunúmerum fyrir færslur á útleið:  

- Velja úr fyrirliggjandi rað- eða lotunúmerum. Þetta á við þegar vörurakningarnúmerum hefur þegar verið úthlutað í færslu á innleið.
- Úthluta nýjum rað- eða lotunúmerum fyrir færslur á útleið. Þetta á við þegar vörurakningarnúmerum er ekki úthlutað á vörur fyrr en þau eru seld og tilbúin til afhendingar.

### Valið úr tiltækum rað- og lotunúmerum  

Þegar unnið er við vörur sem krefjast vörurakningar og verið er að stofna færslur á útleið þarf gjarnan að velja lotu- eða raðnúmer sem þegar eru til.

1. Af skjali á útleið er valin lína sem á að velja rað- eða lotunúmer í.  
2. Áflýtiflipanum **Línur** skal velja aðgerðina **Lína**, svo **Tengdar upplýsingar** og loks **Vörurakningarlínur**.  
3. Á síðunni **Vörurakningarlínur** er um þrennt að velja þegar kemur að því að tilgreina lotu- eða raðnúmer:  

   * Reiturinn Raðnr. er valinn **.** og velja síðan númer í reitnum **Raðnr. Listasíða** .
   * Reiturinn Lotunr. er valinn **.** og velja síðan númer í reitnum **Lotunr. Listasíða** . Síðan er reiturinn Raðnr **. valinn.** og valið númer í reitnum **Raðnr. Listasíða** .
   * Veljið aðgerðina Vinnsla **og veljið** svo Velja færslur **.** Síðan **Velja færslur** sýnir öll lotu- og raðnúmer ásamt upplýsingum um það hvað er til.

4. Í reitinn **Valið magn** er fært inn magn hvers lotu- eða raðnúmers sem á að nota.
5. Velja hnappinn **Í lagi**. Vörurakningarupplýsingarnar flytjast á síðuna **Vörurakningarlínur** .  

Magnreitirnir í hausnum sýna magn og samtölur vörurakningarnúmeranna sem skilgreind eru á síðunni. Magnið verður að samsvara því sem er í fylgiskjalslínunni, sem er gefið til kynna með **0** í reitnum **Óskilgreint** .  

Þegar fylgiskjalslínan er bókuð eru vörurakningarupplýsingarnar fluttar í tengdar birgðafærslur.

### Til að úthluta nýjum rað- eða lotunúmerum  

Þetta ferli á við þegar vörur eru ekki með rað- eða lotunúmer meðan þær eru í birgðum. Þess í stað er vörurakningarnúmerum úthlutað þegar vörur eru seldar og tilbúnar til afhendingar. Þá er yfirleitt hægt að úthluta númerum úr forskilgreindum númeraröðum.

1. Valin er viðkomandi fylgiskjalslína, t.d. sölureikningur eða sölupöntun, og á flýtiflipanum **Línur** skal velja aðgerðina **Lína**, svo **Tengdar upplýsingar** og loks aðgerðina **Vörurakningarlínur**.  

    Hægt er að úthluta vörurakningarnúmerum með eftirtöldum aðferðum:  
    * Sjálfvirkt, úr forskilgreindri númeraröð: Velja skal **Úthluta raðnúmeri.** eða **Úthluta lotunr.** Aðgerð.  
    * Sjálfvirkt, á grundvelli færibreyta sem notandi skilgreinir sérstaklega fyrir útleiðarvöruna: Velja aðgerðina **Stofna sérsniðið RN**.  
    * Handvirkt með því að færa inn rað- eða lotunúmer án þess að nota númeraröð.  

2. Í þessu ferli skal úthluta raðnúmeri sjálfkrafa með því að velja **Úthluta raðnúmeri**.  

     **Í reitnum Magn sem á að stofna** er sjálfgefið línumagn en því má breyta.  
3. Gátmerki er sett í reitinn **Stofna nýtt lotunr.** svo að nýju raðnúmerin flokkist í sérstaka lotu.  
4. Veldu hnappinn **Í lagi** og stofnar kerfið þá lotunúmer og ný einstök raðnúmer samkvæmt magninu til afgreiðslu í viðkomandi fylgiskjalslínum.  

Magnreitirnir efst sýna magn og samtölur vörurakningarnúmeranna sem eru skilgreind á síðunni. Magnið verður að samsvara því sem er í fylgiskjalslínunni, sem er gefið til kynna með **0** í reitnum **Óskilgreint** .  

Þegar fylgiskjalið er bókað eru vörurakningarfærslurnar fluttar í birgðafærslurnar.

### Úthluta rakningarnúmerum í upprunaskjölum

Sum fyrirtæki skilgreina tiltekin rað- eða lotunúmer á upprunaskjali, t.d. sölupantanir. Ef viðskiptamaður fer t.d. fram á ákveðna lotu. Þegar birgðatínslu- eða vöruhúsatínsluskjal er stofnað úr upprunaskjali á útleið þar sem rað- eða lotunúmer hafa þegar verið skilgreind er ekki hægt að breyta neinum reitum á síðunni **Vörurakningarlínur** undir birgðatínslunni. Undantekningin er reiturinn **Magn til afgreiðslu** . Í því tilvikum eru vörurakningarnúmer tilgreind í aðskildum frágangs-/tínslulínum í birgðatínslulínunum. Magninu hefur þegar verið skipt í sérstakar samstæður rað- eða lotunúmera því í sölupöntuninni eru vörurakningarnúmerin sem á að afhenda tilgreind.

## Hvernig á að meðhöndla rað- og lotunúmer í millifærslupöntunum

Ferlum við meðferð rað- og lotunúmera sem verið er að flytja milli birgðastöðva svipar til þeirra sem beitt er þegar vara er keypt og seld.  

Millifærslupantanir eru þó einstakar að því leiti að afhending og móttaka fer fram úr sömu millifærslulínu og notar sama tilvik á síðunni **Vörurakningarlínur** . Vörurakningarnúmer sem afhent eru frá einni birgðageymslu verða að vera móttekin óbreytt í annarri birgðageymslu.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Flutningspantanir** og velja síðan viðkomandi tengil.  
2. Opna skal flutningspöntunina sem á að vinna. Á flýtiflipanum **Línur** skal velja aðgerðina **Lína**, velja aðgerðina **Vörurakningarlínur** og loks aðgerðina **Afhending**.  
3. Á síðunni **Vörurakningarlínur** er rað- eða lotunúmerum úthlutað eða þau valin eins og fyrir hverja aðra útleiðar-birgðafærslu.  

    Þegar unnið er með rað- og lotunúmer vegna millifærsluvara er gjarnan búið að úthluta númerum. Þess vegna verður oft valið um fyrirliggjandi rað- eða lotunúmer.  

4. Millifærslupöntunin, fyrst afhending og síðan móttaka, er bókuð til að skrá að vörurnar séu fluttar og bera vörurakningarfærslur þeirra.  

Meðan á millifærslu stendur er ekki hægt að breyta gildum á síðunni **Vörurakningarlínur** .  

## Skráning viðbótarupplýsinga um rað- og lotunúmer

Ef nauðsynlegt er að tengja sérstakar upplýsingar um vörurakningarnúmer, t.d. vegna gæðaeftirlits, er hægt að gera það á upplýsingaspjaldi rað- eða lotunúmers.

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
3. Á síðunni **Birgðaspjald** skal velja aðgerðina **Tengdar**, velja aðgerðina **Tengdar**, velja aðgerðina **Færslur** og velja **svo Færslur**.
4. Velja reitinn **Lotunr.** eða **Raðnúmer**. Ef upplýsingar eru til fyrir þetta vörurakningarnúmer þá mun síðan **Lotunr. upplýsingalista** eða **Raðnr. upplýsingalista** opnast.  
5. Velja skal spjald og síðan **Lotunr./raðnúmeraupplýsingaspjald** aðgerðina.  
6. Breyta stuttri lýsingu, athugasemdafærslu eða reitnum **Lokaður**.  

Ekki er hægt að breyta rað- eða lotunúmerum eða magni. Til að gera það verður að endurflokka birgðafærsluna. Nánari upplýsingar um endurflokkun er farið í Til að [endurflokka lotu- eða raðnúmer](inventory-how-work-item-tracking.md#to-reclassify-serial-or-lot-numbers).

## Endurflokka rað- eða lotunúmer

Endurflokkun vörurakningar fyrir vöru þýðir að breyta lotu- eða raðnúmeri í nýtt lotu- eða raðnúmer eða breyta lokadagsetningunni í nýja lokadagsetningu. Ef lotur eru notaðar er einnig hægt að sameina margar lotur í eina. Nota endurflokkunarbók vöru til að vinna þessa verkhluta.

> [!NOTE]
> [!INCLUDE [prod_short](includes/prod_short.md)] staðfestir að hver lína hafi sérstaka samsetningu rað-, lotu- og/eða pakkanúmera. Ef skipta á lotu, sendingu eða lotu og pakka í margar lotur eða pakka þarf að nota margar færslubókarlínur.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknið, færa inn **birgðaendurflokkunarbækur** og velja síðan viðeigandi tengja.  
2. Línan er fyllt út með viðeigandi upplýsingum. Nánari upplýsingar er að finna í [Telja birgðir með skjölum](inventory-how-count-inventory-with-documents.md) eða [Telja, leiðrétta og endurflokka birgðir með Færslubókum](inventory-how-count-adjust-reclassify.md).
3. Velja aðgerðina **Vörurakningarlínur**  
4. Í reitnum **Raðnr.** eða **Lotunr.** er valið gildandi rað- eða lotunúmer.  
5. Hægt er að slá inn nýtt vörurakningarnúmer með því að slá það inn í reitinn **Nýtt raðnr.** eða **Nýtt lotunr.**. Hægt er að sameina eina eða fleiri lotur við eina nýja lotu eða lotu sem er til fyrir.  

    > [!NOTE]  
    > Þegar fyrningardagsetningar eru endurflokkaðar eru vörur með fyrstu fyrningardagsetningarnar fyrir færslur á útleið lagðar til fyrst. Til að fræðast meira er farið í [Tínsla eftir FEFO](warehouse-picking-by-fefo.md).  

6. Ef tilgreina á nýja fyrningardagsetningu fyrir rað- eða lotunúmerið er hún færð inn í reitinn **Ný lokadagsetning** .  

    > [!IMPORTANT]  
    > * Ef verið er að endurflokka lotu að sama lotunúmeri en með annarri fyrningardagsetningu þarf að endurflokka alla lotuna með einni vöruendurflokkunarbókarlínu.
    > * Ef verið er að endurflokka fleiri en eina lotu við eitt nýtt lotunúmer, þ.e. það að verið er að sameina fleiri en eina lotu í eina nýja lotu, verður að færa inn sömu nýju fyrningardagsetningu fyrir allar loturnar. 
    > * Ef verið er að endurflokka eina lotu sem er til í aðra lotu sem er með aðra lokadagsetningu verður að nota lokadagsetningu seinni lotunnar. 
    > * Ef reiturinn **Ný lokadagsetning** er látinn standa auður þá verður lotu- eða raðnúmerið endurflokkað með auðri lokadagsetningu.  

7. Ef til eru upplýsingar um gamla rað- eða lotunúmerið er hægt að afrita það yfir á nýja rað- eða lotunúmerið.  

    1. Á síðunni **Vörurakningarlínur** skal velja **Nýtt raðnr. upplýsingar** aðgerðina eða **Nýtt lotunr. upplýsingar** aðgerðina.  
    2. Til að afrita upplýsingar frá gamla lotu- eða raðnúmerinu er aðgerðin **Afrita upplýsingar** valin.  
    3. Á upplýsingalistasíðunni er valið það lotu- eða raðnúmer sem ætlunin er að afrita og hnappurinn **Í lagi** valinn.  

8. Hægt er að breyta upplýsingunum sem eru fyrir hendi varðandi lotu- eða raðnúmerið með því að skrá lotu- eða raðupplýsingarnar.  
9. Færslubókin er bókuð til að tengja nýju vörurakningarnúmerin eða lokadagsetningarnar við viðkomandi birgðafærslu.

## Skanna strikamerki með Business Central farsímaforritinu

[!INCLUDE [barcode-mobile-app](includes/barcode-mobile-app.md)]

Á síðunni Vörurakningarlínur **er hægt að nota aðgerðina**  **Skanna margar** . Þegar strikamerki hefur verið skannað út er gildi þess fært inn í reitinn á síðunni og næsti flýtifærslureitur verður tiltækur. Einnig er hægt að nota táknið strikamerkisskannar til að færa í tiltekinn reit.

Eftirfarandi töflur sýna síðurnar sem styðja skönnun strikamerkis fyrir vörurakningu úr farsímaforritinu [!INCLUDE [prod_short](includes/prod_short.md)] .

|Síða  |Gildi svæða sem hægt er að skanna  |
|---------|---------|
|Vörurakningarlínur     |* Raðnr.<br><br>* Nýtt raðnr.<br><br>* Lotunr.<br><br>* Nýtt lotunr.<br><br>* Pakkanr.<br><br>* Ný pakkanr.|
|Vörurakningarlínur vöruhúss     |* Raðnr.<br><br>* Nýtt raðnr.<br><br>* Lotunr.<br><br>* Nýtt lotunr.<br><br>* Pakkanr.<br><br>* Ný pakkanr.|
|Vörurakning     |* Raðnr. Sía<br><br>* Lotunr. Sía<br><br>* Pakkanr. Sía |
|Færslubók atriðis     |* Raðnr.<br><br>* Lotunr.<br><br>* Pakkanr.     |
|Vöruhúsaaðgerðalína     |* Raðnr.<br><br>* Lotunr.<br><br>* Pakkanr.<br><br>**Til athugunar**: Eftirfarandi síður nota síðuna Aðgerðalína vöruhúss:<br><br>* bls. 5780 "Vöruh. Undirgluggi tínslu"<br><br>* bls. 7378 "Birgðag. Undirgluggi tínslu"<br><br>* bls. 5771 "Vöruh. Undirgluggi frágangs"<br><br>* bls. 7316 "Undirgluggi vöruhúsahreyfingar"<br><br>* bls. 7376 "Birgðag. Undirgluggi frágangs"<br><br>* bls. 7383 "Birgðat. Undirgluggi hreyfingar"        |
|Vöruh. Raunbirgðabirgðir Færslubók     |* Raðnr.<br><br>* Lotunr.<br><br>* Pakkanr.         |

## Sjá einnig .

[Setja upp vörurakningu með raðnúmer, lotu og pakkanúmer](inventory-how-setup-item-tracking.md)  
[Rekja vöruraktar vörur](inventory-how-to-trace-item-tracked-items.md)  
[Birgðir](inventory-manage-inventory.md)  
[Hönnunarupplýsingar: Vörurakning](design-details-item-tracking.md)  
[Hönnunarupplýsingar - vörurakning og frátekningar](design-details-item-tracking-and-reservations.md)  
[Taka frá vörur](inventory-how-to-reserve-items.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
