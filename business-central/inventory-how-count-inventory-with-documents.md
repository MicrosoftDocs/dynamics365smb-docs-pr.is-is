---
title: Telja og leiðrétta birgðir
description: Lýsir því hvernig á að telja efnislegar birgðir og nota birgðaskjöl til að laga lagerbirgðir.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: how-to
ms.search.keywords: 'adjustment, status, negative, positive, increase, decrease, inventory'
ms.search.forms: '5895, 6561, 6562, 6563, 6564, 6565, 6566, 5892, 5891, 5879, 5880, 5893, 5897, 5882, 5881, 5899, 5875, 5878, 5877, 5876, 5896, 6567, 6568, 6569, 6570, 6571, 6572, 5883, 5886, 884, 5898, 5885, 5890, 5888, 5889, 5887, 5894, 6774, 6775, 6776, 6780, 6781, 6782, 6783'
ms.date: 03/11/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# Telja og leiðrétta birgðir með skjölum

Hægt er að gera efnislega birgðatalningu á vörunum þínum með því að nota skjöl fyrir efnislega birgðapöntun og skráningu efnislegra birgða. Síðan **Pöntun efnislegra birgða** er notuð til að skipuleggja verk ítarlegrar birgðatalningar, t.d. ein á hverja staðsetningu. Nota síðuna **Safn raunbirgðaskráningar** og miðla raunverulegri talningu á vörum. Hægt er að búa til margar skráningar fyrir eina pöntun, til dæmis til að dreifa vöruflokkum til mismunandi starfsmanna.

Hægt er að prenta reitinn **Raunbirgðabók.** Skráning skýrslu úr hverri skráningu og í henni eru auðir magnreitir þar sem hægt er að færa taldar birgðir inn. Þegar talningu er lokið og magnið er fært inn á síðunni **Raunbirgðaskráning** skal velja aðgerðina **Ljúka** . Þessi aðgerð færir magnið yfir í tengdar línur á síðunni **Raunbirgðapöntun** . [!INCLUDE [prod_short](includes/prod_short.md)] tryggir að ekki er hægt að skrá vörutalningu tvisvar.  

> [!NOTE]
> Með því að nota skjöl til að framkvæma raunbirgðatalningu veitir meiri stjórn og styður dreifingu talningar til margra starfsmanna. Einnig er hægt að nota bækur til að framkvæma verkið, eins og síðurnar **Raunbirgðabækur** og **Raunbirgðabækur vöruhúss** . Nánari upplýsingar eru í [Telja, Leiðrétta og Endurflokka birgðir með færslubókum](inventory-how-count-adjust-reclassify.md). Í þessari grein er því lýst hvernig skjöl eru notuð til að telja raunbirgðatalningu.
>
> Ef svæði eru notuð í vöruhúsinu er ekki hægt að nota raunbirgðapantanir. Þess í stað er síðan Vöruh. - Raunbirgðabók **notuð** til að telja vöruhúsafærslurnar áður en þær eru samstilltar við birgðafærslur.

Talning birgða með notkun fylgiskjala samanstendur af eftirfarandi heildarskrefum:

1. Stofnaðu pöntun efnislegra birgða með væntanlegu vörumagni fyllt út fyrirfram.
2. Búðu til eina eða fleiri skráningar efnislegra birgða úr pöntuninni.
3. Færðu inn talið vörumagn í skráningarnar, eins og þær eru sóttar í prentuðum eintökum til að mynda og stilltu það á **Lokið**.
4. Ljúktu við og bókaðu pöntun efnislegra birgða.

## Að stofna pöntun efnislegra birgða

Raunbirgðapöntun er fullbúið skjal sem samanstendur af haus og pöntunarlínum raunbirgðapantana. Upplýsingarnar á haus efnislegra birgða útskýrir hvernig á að gera talningu á efnislegum birgðum. Í pöntunarlínunum eru upplýsingar um vörurnar og birgðageymslurnar.

Til að stofna raunbirgðalínur er aðgerðin **Reikna línur** yfirleitt notuð til að bæta gildandi birgðum við sem línur á pöntuninni. Einnig er hægt að nota aðgerðina **Afrita úr fylgiskjali** til að fylla út línurnar með efni annars opinnar eða bókaðrar raunbirgðapöntunar. Eftirfarandi ferli lýsir aðeins notkun aðgerðarinnar **Reikna línur** .

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Efnislegar birgðapantanir** og velja síðan viðkomandi tengil.
2. Valið er **Nýtt** aðgerð.
3. Fylltu út nauðsynlega reiti í flýtiflipanum **Almennt**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Veldu aðgerðina **Reikna línur**.
5. Veldu valkostina eins og þörf er á.
6. Setja afmarkanir, til dæmis, til að taka aðeins með hlutmengi af vörum sem telja á með fyrstu skráningu.

    > [!TIP]
    > Til að áætla fyrir marga starfsmenn að telja birgðirnar skal setja mismunandi afmarkanir í hvert sinn sem aðgerðin **Reikna línur** er notuð til að fylla út pöntunina með hlutmengi birgðavara sem notandi mun skrá. Þegar margar raunbirgðaskráningar eru síðan búnar til fyrir marga starfsmenn er hættan á að talning vara verði talin tvisvar. Nánari upplýsingar eru notaðar með því að fara í Til að [stofna raunbirgðaskráningu](#to-create-a-physical-inventory-recording).

7. Velja hnappinn **Í lagi**.

Lína fyrir hverja vöru sem er til í valinni birgðageymslu og á hverju stilltu afmörkunum og valkostum er bætt við pöntunina. Fyrir vörur sem eru settar upp fyrir vörurakningu er gátreiturinn **Nota vörurakningu** valinn og upplýsingar um áætlað magn rað- og lotunúmera tiltækar með því að **velja Línur** og síðan **Vörurakningarlínur**. Nánari upplýsingar eru notaðar með því að fara í [Meðhöndlun vörurakningar þegar birgðir eru taldar](#handle-item-tracking-when-counting-inventory).

Nú er hægt að búa til eina eða fleiri skráningar sem eru leiðbeiningar til starfsmanna sem nota talninguna.  

> [!NOTE]
> Ef rakning sendinga er notuð er einnig hægt að nota skjöl til að telja og leiðrétta birgðir með sendingarnúmerum. Ef hefja á þessa aðgerð þarf að kveikja á **eiginleikauppfærslu: Gera notkun sendingarleitar virka í raunbirgðapöntunum** á síðunni **Aðgerðastjórnun** . Fyrirliggjandi raunbirgðapantanir eru uppfærðar, hins vegar [!INCLUDE [prod_short](includes/prod_short.md)]  er ekki hægt að ýta á pakkanúmerið **.** . Þessar línur verður að endurstökkva með aðgerðinni **Reikna línur** á síðunni **Raunbirgðapöntun** .
>
> Hægt er að færa inn sendingarnúmer vara þar sem sendingarleitar er þörf á síðunni **Raunbirgðaskráningarlínur** . Velja Skal **Ljúka** til að ljúka skráningu.
>
> Þegar Lokið **hefur verið valið** á **síðunni**  Raunbirgðapöntun [!INCLUDE [prod_short](includes/prod_short.md)] er munur reiknaður út með tilliti til pakkans og annarra vörurakningarupplýsinga og jákvæðar eða neikvæðar leiðréttingar.

## Að stofna skráningu efnislegra birgða

Fyrir hverja raunbirgðapöntun er hægt að stofna eitt eða fleiri raunbirgðaskráningarskjöl þar sem starfsmenn færa inn talda magnið. Starfsmenn geta fært magn inn annaðhvort handvirkt eða með skönnunartæki.

Sjálfgefið er að skráning sé stofnuð fyrir allar línurnar í tengdri pöntun efnislegra birgða. Til að koma í veg fyrir að tveir starfsmenn telji sömu vörurnar ef talningu er dreift þarf smám saman að fylla raunbirgðapöntunina út með því að setja afmarkanir á keyrsluna **Reikna línur** . Síðan er raunbirgðaskráning stofnuð með gátreitnum **Aðeins línur sem ekki eru í færslum valdar** . Þessi stilling tryggir að hver ný skráning innihaldi mismunandi vörur en þær sem eru í öðrum skrám.

Hægt er að prenta reitinn **Raunbirgðir til að fá handvirka talningu.** Skráning skýrslu sem er með tóma dálka þar sem starfsmenn vöruhúss geta skrifað talið magn. Þegar talningu er lokið er skráð magn fært inn í tengdar línur á síðunni **Raunbirgðaskráning** . Að lokum skaltu flytja skráð magn á tengda pöntun efnislegra birgða með því að stilla stöðuna á **Lokið**.

1. Á síðu **Pöntun efnislegra birgða** sem inniheldur línur fyrir vörurnar sem á að telja í einni skráningu, skal velja aðgerðina **Búa til nýja skráningu**.
2. Veldu valkostina og stilltu síur eins og þörf er á.
3. Velja hnappinn **Í lagi**.
4. Ef telja á allar vörur skal hlaða þær á tengda raunbirgðapöntun og endurtaka þrep 1 til 3 með gátreitinn **Aðeins línur ekki í færslum** valinn.
5. Veldu aðgerðina **Skráningar** til að opna síðuna **Listi yfir efnislegar birgðaskráningar**.
6. Opnaðu viðkomandi skráningu.
7. Fyllt er út í reiti eftir því sem er nauðsynlegt í flýtiflipanum **Almennt**.
8. Fyrir vörur sem nota vörurakningu skal búa til viðbótarlínu fyrir hvern kóða lotunúmers eða raðnúmers með því að velja aðgerðina **Virkni** og síðan aðgerðina **Afrita línu**. Nánari upplýsingar eru notaðar með því að fara í [Meðhöndlun vörurakningar þegar birgðir eru taldar](#handle-item-tracking-when-counting-inventory).  
9. Velja skal aðgerðina **Prenta** til að undirbúa efnislegt skjal sem starfsmenn geta notað til að athuga magnið sem þeir telja.

## Að ljúka skráningu á efnislegum birgðum

Eftir að starfsmenn telja magnið skal skrá magnið. [!INCLUDE [prod_short](includes/prod_short.md)]

1. Úr síðunni **Listi yfir efnislegar birgðaskráningar** skal velja skráningu efnislegra birgða sem á að klára og síðan velja aðgerðina **Breyta**.
2. Í flýtiflipanum **Línur** skal fylla út raunverulegt talið magn í reitinn **Magn** fyrir hverja línu.
3. Fyrir vörur með rað- eða lotunúmer (gátreiturinn **Nota vörurakningu** er valinn) er talið magn fært inn í línurnar fyrir rað- og lotunúmer vörunnar. Nánari upplýsingar eru notaðar með því að fara í [Meðhöndlun vörurakningar þegar birgðir eru taldar](#handle-item-tracking-when-counting-inventory).
4. Valinn er gátreiturinn **Skráð í** hverri línu.
5. Þegar öll gögn hafa verið færð inn fyrir skráningu efnislegra birgða skal velja aðgerðina **Ljúka**. Athugaðu að allar línur verða að vera með gátreitinn **Skráð** valinn.

    > [!NOTE]
    > Þegar lokið er við skráningu efnislegra birgða er hver lína flutt til línunnar í tengdri pöntun efnislegra birgða sem passar að fullu. Til að passa verða gildin í reitunum **Vörunr.**, **Afbrigðiskóti**, **Kóti** birgðageymslu og **Hólfkóti** að vera þau sömu í skránni og pöntunarlínunum.>
    > 
    > Ef samsvarandi raunbirgðapöntunarlína er ekki til og ef **gátreiturinn Leyfa skráningu án pöntunar** er valinn er nýrri línu bætt við og gátreiturinn **Skráð án pöntunar** í viðkomandi raunbirgðapöntunarlínu valinn. Annars birtast villuboð og hætt er við vinnsluna.> Ef fleiri en ein raunbirgðaskráningarlína samsvarar raunbirgðapöntunarlínu þá birtast skilaboð og hætt er við vinnsluna. Ef tvær sömu raunbirgðalínur enda á raunbirgðapöntuninni af einhverjum sökum er hægt að nota aðgerð til að leysa hana. Nánari upplýsingar eru notaðar til að [finna tvíteknar línur](#to-find-duplicate-physical-inventory-order-lines) raunbirgðapantana.

## Að ljúka pöntun efnislegra birgða

Þegar skráningu raunbirgða hefur verið lokið er reiturinn **Magn- og stofn)** á tengdri raunbirgðapöntun uppfærður með taldu (skráðu) gildunum og gátreiturinn **Í skráningu** er valinn. Ef talið magn er frábrugðið væntanlegu magni **sýna reitirnir Magn pos (stofn)** og **Neikvætt magn (stofn)** mismuninn.

Til að fá aðgang að væntanlegu magni og einhverjum skráðum mun á vörum með vörurakningu skal velja aðgerðina **Línur** og velja **síðan Vörurakningarlínur** til að velja mismunandi yfirlit fyrir rað- og lotunúmerin í raunbirgðatalningunni.

Einnig er hægt að velja aðgerðina **Mismunur efnislegrar birgðapöntunar** aðgerðina til að skoða mismun milli væntanlegs magns og talins magns.

### Að finna tvíteknar pöntunarlínur efnislegra birgða

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Efnislegar birgðapantanir** og velja síðan viðkomandi tengil.
2. Opna raunbirgðapöntunina til að skoða tvíteknar línur fyrir.
3. Veldu aðgerðina **Sýna tvíteknar línur**.

Tvíteknar raunbirgðalínur sýna svo hægt sé að eyða þeim og aðeins eina línu með einstökum gildum í reitunum **Vörunr.**, **Afbrigðiskóti**, **Kóti** birgðageymslu og **Hólfakóti** .

### Að bóka pöntun efnislegra birgða

Þegar lokið hefur verið við raunbirgðapöntun og stöðu hennar breytt í Lokið **er hægt að** bóka hana. Aðeins er hægt að stilla stöðu raunbirgðapöntunar á **Lokið** við eftirfarandi skilyrði:

- Allar tengdar skráningar efnislegra birgða eru með stöðuna **Lokið**.
- Hver raunbirgðalína er talin með að minnsta kosti einni birgðaskráningarlínu.
- Gátreitirnir **Í skráningarlínum** og **Útreiknað** magn eru valdir fyrir allar raunbirgðapöntunarlínur.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Efnislegar birgðapantanir** og velja síðan viðkomandi tengil.
2. Veldu pöntun efnislegra birgða sem á að ljúka við og veldu síðan aðgerðina **Breyta**.

    Á síðunni **Raunbirgðapöntun** birtist skráð magn í reitnum **Skráð magn (stofn).** .
3. Veldu aðgerðina **Ljúka**.

    Gildinu í reitnum **Staða** er **Lokið**. Nú er aðeins hægt að breyta pöntuninni með því að velja aðgerðina **Enduropna** .
4. Til að bóka pöntunina skal velja aðgerðina **Bóka** og síðan velja hnappinn **Í lagi**.

    Birgðafærslurnar eru uppfærðar ásamt tengdum vörurakningarfærslum.

    [!INCLUDE [preview-posting-inventory](includes/preview-posting-inventory.md)]

### Að skoða bókaðar pantanir efnislegra birgða

Að bókun lokinni er raunbirgðapöntuninni eytt og hægt er að skoða skjalið sem bókaða raunbirgðapöntun. Í bókuðu pöntuninni eru raunbirgðaskráningar hennar og allar athugasemdir gerðar.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Bókaðar efnislegar birgðapantanir** og velja síðan viðkomandi tengil.
2. Í reitnum **Bókaðar raunbirgðir Síðan Pantanir**, valin bókuð birgðapöntun til að skoða og svo er aðgerðin **Skoða** valin.
3. Til að skoða lista yfir tengdar skráningar efnislegra birgða skal velja aðgerðina **Skráningar**.

## Meðhöndla vörurakningu við talningu birgða

Vörurakning tengist rað- eða lotunúmerum sem úthlutað er á vörur. Þegar vara sem geymd er í birgðum er talin, til dæmis, 10 mismunandi lotunúmer, verður starfsmaður að geta skráð hvaða og hversu margar einingar hvers lotunúmers eru í birgðum. Nánari upplýsingar eru notaðar [með því að fara í](inventory-how-work-item-tracking.md) Vinna með rað- og lotunúmer.

Gátreiturinn **Nota vörurakningu** í raunbirgðapöntunarlínum er sjálfkrafa valinn ef vörurakningarkóti er settur upp fyrir vöruna. Hægt er að velja gátreitinn handvirkt eða hreinsa hann.

### Dæmi - Undirbúa skráningu raunbirgða fyrir vörurakta vöru

Íhugaðu efnislegar birgðir fyrir vöru A sem er geymd í birgðum sem tíu mismunandi raðnúmer.

1. Í skráningarlínunni fyrir vöruna er gátreiturinn **Nota vörurakningu** valinn.
2. Veldu reitinn **Raðnr.**, veldu fyrsta raðnúmerið sem er til í birgðum fyrir vöruna og veldu síðan hnappinn **Í lagi**.

    Afrita línuna fyrir fyrstu vöruraknu vöruna til að setja inn viðbótarlínur sem samsvara fjölda raðnúmera sem geymd eru í birgðum.

3. Veljið aðgerðina **Aðgerðir** og veljið **svo Afrita línu**.
4. Á síðunni **Afrita raunbirgðaendurg.línu** er 9 **fært inn** í **reitinn Fjöldi afrita** og síðan er hnappurinn **Í lagi** valinn.
5. Í fyrstu línunni í reitnum **Raðnr.** er valið næsta raðnúmer vörunnar.
6. Skref 5 er endurtekið fyrir eftirstandandi átta raðnúmer. Gæta skal þess að sama númer sé ekki valið tvisvar.
7. Veljið aðgerðina **Prenta** til að undirbúa útprentunina sem starfsmenn nota til að skrifa niður taldar vörur og rað-/lotunúmer.

Taktu eftir að skýrslan **Skráning efnislegra birgða** inniheldur tíu línur fyrir vöru A, eina fyrir hvert raðnúmer.

### Dæmi - Skrá og bóka talinn mismun lotunúmera

Vara rakin eftir lotu er geymd í birgðum með númeraröðunum „LOTA“.

**Væntanlegar birgðir**:

|Lotunr.|Magn|
|-|-|
|LOT1001|80|
|LOT1003|30|
|LOT1006|10|
|Samtals|120|

**Skráð magn**:

|Lotunr.|Magn|
|-|-|
|LOT1001|80|
|LOT0002|12|
|LOT1003|20|
|LOT1006|10|
|Samtals|112|

**Magn sem á að bóka**:

|Lotunr.|Væntanlegt magn|Skráð magn|Magn sem á að bóka|
|-|-|-|-|
|LOT1001|80|80|0|
|LOT1002|0|12|+12|
|LOT1003|30|20|-10|
|LOT1006|10|0|-10|
|Samtals|120|112|-8|

Í reitnum **Raunbirgðamagn** (stofn) **er** 8 í reitnum **Raunbirgðapöntun**. Reiturinn **Raunbirgðir fyrir pöntunarlínuna. Vörurakning. Listasíða** sýnir jákvætt eða neikvætt magn fyrir hvert lotunúmer.

## Birgðaskjöl

Eftirfarandi gerðir skjala eru gagnlegar til að stjórna vöruhúsinu:

* Nota **birgðamóttökur** til að skrá jákvæðar leiðréttingar á vörum samkvæmt gæðum, magni og kostnaði.
* Nota **birgðaafhendingar** til að afskrifa týndar eða skemmdar vörur.

Hægt er að prenta þessi skjöl á hvaða stigi sem er, gefa þau út og enduropna þau og úthluta sameiginlegum gildum eins og víddum í hausnum. Til að endurprenta skjölin eftir að þau hafa verið bókuð skal nota **síðurnar Bókaðar birgðamóttökur** og **Bókaðar birgðaafhendingar** .

> [!NOTE]
> Áður en hægt er að nota þessi fylgiskjöl þarf að tilgreina númeraröð til að stofna kenni þeirra. Nánari upplýsingar eru í Til að [setja upp tölusetningu fyrir birgðaskjöl](#to-set-up-numbering-for-inventory-documents).

### Að setja upp númeraröð fyrir birgðaskjöl

Þessi verklýsing sýnir hvernig á að búa til númeraröð fyrir birgðaskjöl.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Uppsetning birgða** og velja síðan viðkomandi tengil.
2. Í flýtiflipanum **Tölusetning** skal tilgreina í eftirfarandi reitum númeraraðir fyrir skjöl:

   - **Birgðainnhreyfingarnr.**  
   - **Bókuð birgðamóttökunr.**  
   - **Birgðaafhendingarnr.**  
   - **Bókuð birgðaafhendingarnr.**  

### Að stofna og bóka birgðaskjal

Eftirfarandi ferli sýnir hvernig á að stofna, prenta og bóka birgðamóttöku. Skrefin eru svipuð fyrir birgðaafhendingar.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Birgðamóttaka** og velja síðan viðkomandi tengil.  
2. Í haus síðunnar **Birgðamóttaka** skal velja staðsetninguna í reitnum **Staðsetningarkóði** og síðan fylla út eftirstandandi reiti eftir þörfum.
3. Á flýtiflipanum **Línur** í reitnum **Vara** skal velja birgðavöruna. Í reitinn **Magn** er fært magn vara sem á að bæta við.
4. Til að prenta skýrslu **Birgðamóttöku** á síðunni **Birgðamóttaka** skal velja aðgerðina **Prenta**.

Eftirfarandi aðgerðir eru í boði á síðunni **Birgðamóttaka**:

-  **Veljið Útgáfu** eða **Enduropna** aðgerðir til að stilla stöðuna fyrir næsta vinnslustig.  
-  **Veljið Bóka** aðgerð til að bóka birgðamóttökuna eða veljið **Bóka og prenta** til að bóka móttökuna og prenta prófunarskýrsluna.  

    [!INCLUDE [preview-posting-inventory](includes/preview-posting-inventory.md)]

## Prentun birgðaskjala

Hægt er að tilgreina skýrslurnar sem á að prenta á mismunandi þrepum með því að velja einn af eftirfarandi valkostum í **reitnum Notkun** á síðunni **Skýrsluval - Birgðir** :

* Birgðamóttaka
* Birgðaafhending
* Bókuð birgðamóttaka
* Bókuð birgðaafhending

> [!NOTE]
> Tiltækar skýrslur geta verið mismunandi eftir staðfæringu landsins/svæðisins. Grunnforritið inniheldur ekkert útlit.

## Sjá einnig .

[Talning, breytingar og endurflokkun birgða með færslubókum](inventory-how-count-adjust-reclassify.md)  
[Vinna með rað- og lotunúmer](inventory-how-work-item-tracking.md)  
[Birgðir](inventory-manage-inventory.md)  
[Yfirlit yfir vöruhúsakerfi](design-details-warehouse-management.md)  
[Sala](sales-manage-sales.md)  
[Innkaup](purchasing-manage-purchasing.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
