---
title: Telja og leiðrétta birgðir
description: Lýsir því hvernig á að telja efnislegar birgðir og nota birgðaskjöl til að laga lagerbirgðir.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'adjustment, status, negative, positive, increase, decrease, inventory'
ms.search.forms: '5895, 6561, 6562, 6563, 6564, 6565, 6566, 5892, 5891, 5879, 5880, 5893, 5897, 5882, 5881, 5899, 5875, 5878, 5877, 5876, 5896, 6567, 6568, 6569, 6570, 6571, 6572, 5883, 5886, 884, 5898, 5885, 5890, 5888, 5889, 5887, 5894, 6774, 6775, 6776, 6780, 6781, 6782, 6783'
ms.date: 04/01/2021
ms.author: edupont
---
# <a name="count-and-adjust-inventory-using-documents"></a><a name="count-and-adjust-inventory-using-documents"></a>Telja og leiðrétta birgðir með skjölum

Hægt er að gera efnislega birgðatalningu á vörunum þínum með því að nota skjöl fyrir efnislega birgðapöntun og skráningu efnislegra birgða. Síðan **Pöntun efnislegra birgða** er notuð til að skipuleggja verk ítarlegrar birgðatalningar, t.d. ein á hverja staðsetningu. Síðan **Skráning efnislegra birgða** er notuð til að koma á framfæri og sækja rauntalningu á vörum. Hægt er að búa til margar skráningar fyrir eina pöntun, t.d. til að dreifa flokkum af vörum á mismunandi starfsmenn.

Skýrslan **Skráning efnislegra birgða** er hægt að prenta úr hverri skráningu og inniheldur tóma magnreiti sem taldar birgðir eru færðar inn í. Þegar notandi hefur lokið talningu og magnið hefur verið fært inn á síðuna **Skráning efnislegra birgða**, velur þú aðgerðina **Klára**. Þetta flytur magnið til tengdra lína á síðunni **Pöntun efnislegra birgða**. Virknin tryggir að ekki er hægt að skrá neina vörutalningu tvisvar.  

> [!NOTE]
> Notkun skjala til að framkvæma talningu á efnislegum birgðum veitir meiri stjórn og styður dreifingu á talningu til margra starfsmanna. Einnig er hægt að framkvæma verkið með því að nota færslubækur, t.d. síðurnar **Raunbirgðabækur** og **Raunbirgðabækur vöruhúss**. Nánari upplýsingar er að finna í [Telja, leiðrétta og endurflokka birgðir með færslubókum](inventory-how-count-adjust-reclassify.md). Hvernig á að framkvæma raunbirgðatalningu með skjölum.
>
> Ef verið er að nota svæði, þá er ekki hægt að nota efnislegar birgðapantanir. Í staðinn skal nota síðuna **Raunbirgðabók vöruhúss** til að telja vöruhúsafærslurnar þínar áður en þær eru samstilltar við birgðabókafærslur.

Birgðatalning með því að nota skjöl samanstendur af eftirfarandi skrefum:

1. Stofnaðu pöntun efnislegra birgða með væntanlegu vörumagni fyllt út fyrirfram.
2. Búðu til eina eða fleiri skráningar efnislegra birgða úr pöntuninni.
3. Færðu inn talið vörumagn í skráningarnar, eins og þær eru sóttar í prentuðum eintökum til að mynda og stilltu það á **Lokið**.
4. Ljúktu við og bókaðu pöntun efnislegra birgða.

## <a name="to-create-a-physical-inventory-order"></a><a name="to-create-a-physical-inventory-order"></a>Að stofna pöntun efnislegra birgða

Pöntun efnislegra birgða er ítarlegt skjal sem samanstendur af pöntunarhaus efnislegra birgða og nokkrum pöntunarlínum efnislegra birgða. Upplýsingarnar á haus efnislegra birgða útskýrir hvernig á að gera talningu á efnislegum birgðum. Pöntunarlínur efnislegra birgða innihalda upplýsingarnar um vörurnar og staðsetningar þeirra.

Til að stofna pöntunarlínur efnislegra birgða er venjulega notuð virknin **Reikna línur** til að endurspegla núverandi birgðir sem línur í pöntuninni. Að öðrum kosti er hægt að nota virknina **Afrita úr skjali** til að fylla út línurnar með innihaldi annarrar opinnar eða bókaðrar pöntunar efnislegra birgða. Eftirfarandi ferli útskýrir eingöngu hvernig á að nota virknina **Reikna línur**.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Efnislegar birgðapantanir** og velja síðan viðkomandi tengil.
2. Valið er **Nýtt** aðgerð.
3. Fylltu út nauðsynlega reiti í flýtiflipanum **Almennt**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Veldu aðgerðina **Reikna línur**.
5. Veldu valkostina eins og þörf er á.
6. Stilltu síur, til dæmis til að aðeins innihalda undirsafn af vörum sem á að telja með fyrstu skráningunni.

    > [!TIP]
    > Til að skipuleggja að margir starfsmenn telji birgðirnar er skynsamlegt að setja á mismunandi síur í hvert skipti sem aðgerðin **Reikna línur** er notuð til að eingöngu fylla út í pöntunina með undirsafni af birgðavörum sem einn notandi kemur til með að skrá. Þannig er hægt að lágmarka hættuna á að vörur séu taldar tvisvar sinnum þegar búnar eru til margar skráningar á efnislegum birgðum fyrir marga starfsmenn. Frekari upplýsingar er að finna í kaflanum [Að stofna skráningu efnislegra birgða](#to-create-a-physical-inventory-recording).

7. Velja hnappinn **Í lagi**.

Lína fyrir hverja vöru sem er til í valdri staðsetningu og samkvæmt stilltum síum og valkostum er færð inn í pöntunina. Fyrir vörur sem eru settar upp fyrir vörurakningu er gátreiturinn **Nota vörurakningu** valinn og upplýsingar um væntanlegt magn á rað- og lotunúmerum er í boði með því að velja aðgerðina **Línur** og síðan **Vörurakningarlínur**. Frekari upplýsingar er að finna í kaflanum [Meðhöndlun vörurakningar þegar birgðir eru taldar](#handling-item-tracking-when-counting-inventory).

Nú er hægt að halda áfram að búa til eina eða fleiri skráningar sem eru leiðbeiningar fyrir starfsfólk sem framkvæmir rauntalninguna.  

## <a name="to-create-a-physical-inventory-recording"></a><a name="to-create-a-physical-inventory-recording"></a>Að stofna skráningu efnislegra birgða

Fyrir hverja pöntun efnislegra birgða er hægt að stofna eitt eða fleiri skjöl fyrir skráningu efnislegra birgða þar sem starfsfólk færir inn talið magn, annaðhvort handvirkt eða í gegnum innleitt skönnunartæki.

Sjálfgefið er að skráning sé stofnuð fyrir allar línurnar í tengdri pöntun efnislegra birgða. Til að forðast að tveir starfsmenn telji sömu vörurnar í tilfelli dreifðrar talningar, er skynsamlegt að fylla smám saman út pöntun efnislegra birgða með því að setja síur á runuvinnsluna **Reikna línur** (sjá kaflann „Að stofna pöntun efnislegra birgða“) og síðan stofna skráningu efnislegra birgða á meðan gátreiturinn **Aðeins línur sem eru ekki í skráningu** er valinn. Þessar stillingar tryggja að allar nýjar skráningar sem eru stofnaðar innihaldi eingöngu vörur sem eru ólíkar þeim sem eru á öðrum skráningum.

Í tilfelli handvirkrar talningar er hægt að prenta lista, skýrsluna **Skráning efnislegra birgða**, sem er með auðan dálk til að skrifa talið magn í. Þegar talningu er lokið skaltu færa skráða magnið inn í viðeigandi línur á síðunni **Skráning efnislegra birgða**. Að lokum skaltu flytja skráð magn á tengda pöntun efnislegra birgða með því að stilla stöðuna á **Lokið**.

1. Á síðu **Pöntun efnislegra birgða** sem inniheldur línur fyrir vörurnar sem á að telja í einni skráningu, skal velja aðgerðina **Búa til nýja skráningu**.
2. Veldu valkostina og stilltu síur eins og þörf er á.
3. Velja hnappinn **Í lagi**.

    Skjal fyrir skráningu efnislegra birgða er búið til.

4. Fyrir hvert safn af vörum sem á að telja skal hlaða þeim í tengda pöntun efnislegra birgða og endurtaka skref 1 til 3 með gátreitinn **Aðeins línur sem eru ekki í skráningu** valinn.

5. Veldu aðgerðina **Skráningar** til að opna síðuna **Listi yfir efnislegar birgðaskráningar**.
6. Opnaðu viðkomandi skráningu.
7. Fyllt er út í reiti eftir því sem er nauðsynlegt í flýtiflipanum **Almennt**.
8. Fyrir vörur sem nota vörurakningu skal búa til viðbótarlínu fyrir hvern kóða lotunúmers eða raðnúmers með því að velja aðgerðina **Virkni** og síðan aðgerðina **Afrita línu**. Frekari upplýsingar er að finna í kaflanum [Meðhöndlun vörurakningar þegar birgðir eru taldar](#handling-item-tracking-when-counting-inventory).  
9. Veldu aðgerðina **Prenta** til að undirbúa efnislegt skjal sem starfsmenn munu nota til að skrifa niður talið magn.

## <a name="to-finish-a-physical-inventory-recording"></a><a name="to-finish-a-physical-inventory-recording"></a>Að ljúka skráningu á efnislegum birgðum

Þegar starfsmenn hafa talið birgðamagnið verður þú að búa þig undir að skrá það í kerfið.

1. Úr síðunni **Listi yfir efnislegar birgðaskráningar** skal velja skráningu efnislegra birgða sem á að klára og síðan velja aðgerðina **Breyta**.
2. Í flýtiflipanum **Línur** skal fylla út raunverulegt talið magn í reitinn **Magn** fyrir hverja línu.
3. Fyrir vörur með rað- eða lotunúmer (gátreiturinn **Nota vörurakningu** er valinn), skal færa inn talið magn í sérstökum línum fyrir rað- og lotunúmer vörunnar. Frekari upplýsingar er að finna í kaflanum [Meðhöndlun vörurakningar þegar birgðir eru taldar](#handling-item-tracking-when-counting-inventory).
4. Veldu gátreitinn **Skráð** í hverri línu.
5. Þegar öll gögn hafa verið færð inn fyrir skráningu efnislegra birgða skal velja aðgerðina **Ljúka**. Athugaðu að allar línur verða að vera með gátreitinn **Skráð** valinn.

    > [!NOTE]
    > Þegar lokið er við skráningu efnislegra birgða er hver lína flutt til línunnar í tengdri pöntun efnislegra birgða sem passar að fullu. Til að passa verða gildin í reitunum **Vörunr.**, **Afbrigðiskóði**, **Staðsetningarkóði** og **Hólfakóði** að vera þau sömu í skráningunni og í pöntunarlínum.<br /><br />
    > Ef engin samsvarandi pöntunarlína efnislegra birgða er til og ef gátreiturinn **Leyfa skráningu án pöntunar** er valinn, þá er ný lína sett inn sjálfkrafa og gátreiturinn **Skráð án pöntunar** í tengdri pöntunarlínu efnislegra birgða er valinn. Annars birtist villuboð og hætt er við ferlið.<br /><br />
    > Ef fleiri en ein skráningarlína efnislegra birgða samsvarar pöntunarlínu efnislegra birgða, birtast skilaboð og hætt er við ferlið. Ef af einhverjum ástæðum tvær eins línur efnislegra birgða enda á pöntun efnislegra birgða er hægt að nota aðgerð til að leysa úr því. Frekari upplýsingar er að finna í kaflanum [Að finna tvíteknar pöntunarlínur efnislegra birgða](#to-find-duplicate-physical-inventory-order-lines).

## <a name="to-complete-a-physical-inventory-order"></a><a name="to-complete-a-physical-inventory-order"></a>Að ljúka pöntun efnislegra birgða

Þegar skráningu efnislegra birgða er lokið er reiturinn **Magnskráning (grunnur)** í tengdri pöntun efnislegra birgða uppfærður með töldum (skráðum) gildum og gátreiturinn **Um skráningar** valinn. Ef talið gildi er frábrugðið því sem búist er við þá er þessi munur sýndur í reitunum **Jákvætt magn (grunnur)** og **Neikvætt magn (grunnur)**.

Til að sjá væntanlegt magn og allan mismun í skráningu fyrir vörur með vörurakningu, skal velja aðgerðina **Línur** og síðan velja aðgerðina **Vörurakningarlínur** til að velja ýmis yfirlit fyrir rað- og lotunúmer sem koma fyrir í efnislegri birgðatalningu.

Einnig er hægt að velja aðgerðina **Mismunur efnislegrar birgðapöntunar** aðgerðina til að skoða mismun milli væntanlegs magns og talins magns.

### <a name="to-find-duplicate-physical-inventory-order-lines"></a><a name="to-find-duplicate-physical-inventory-order-lines"></a>Að finna tvíteknar pöntunarlínur efnislegra birgða

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Efnislegar birgðapantanir** og velja síðan viðkomandi tengil.
2. Opnaðu pöntun efnislegra birgða sem á að skoða tvíteknar línur fyrir.
3. Veldu aðgerðina **Sýna tvíteknar línur**.

Sýndar tvíteknar línur efnislegra birgða svo hægt sé að eyða þeim og halda aðeins einni línu við einstakt gildi í  **reitunum Vörunr.**,  **Afbrigðiskóti** **, kóti** birgðageymslu og  **kóti**  hólfs.

### <a name="to-post-a-physical-inventory-order"></a><a name="to-post-a-physical-inventory-order"></a>Að bóka pöntun efnislegra birgða

Eftir að pöntun efnislegra birgða er lokið og stöðu hennar er breytt í **Lokið** er hægt að bóka hana. Hægt er að setja stöðuna á pöntun efnislegra birgða á **Lokið** ef eftirfarandi er rétt:

- Allar tengdar skráningar efnislegra birgða eru með stöðuna **Lokið**.
- Hver pöntunarlína efnislegra birgða hefur verið talin af að minnsta kosti einni skráningarlínu birgða.
- Gátreitirnir **Í skráningarlínum** og **Væntanlegt magn reiknað** hafa verið valdir fyrir allar pöntunarlínur efnislegra birgða.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Efnislegar birgðapantanir** og velja síðan viðkomandi tengil.
2. Veldu pöntun efnislegra birgða sem á að ljúka við og veldu síðan aðgerðina **Breyta**.

    Á síðunni **Pöntun efnislegra birgða** er skoðað magnið sem er skráð í reitinn **Skráð magn (grunnur)**.
3. Veldu aðgerðina **Ljúka**.

    Gildinu í  **reitnum Staða**  er  **lokið** og nú er aðeins hægt að breyta pöntuninni með því að  **Velja opna enduropna**  aðgerð.
4. Til að bóka pöntunina skal velja aðgerðina **Bóka** og síðan velja hnappinn **Í lagi**.

    Birgðafærslurnar eru uppfærðar ásamt tengdum vörurakningarfærslum.

    [!INCLUDE [preview-posting-inventory](includes/preview-posting-inventory.md)]

### <a name="to-view-posted-physical-inventory-orders"></a><a name="to-view-posted-physical-inventory-orders"></a>Að skoða bókaðar pantanir efnislegra birgða

Eftir bókun verður pöntun efnislegra birgða eytt og hægt er að skoða og meta skjalið sem bókuð pöntun efnislegra birgða ásamt skráningum þess á efnislegum birgðum og öllum athugasemdum sem hafa verið gerðar.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Bókaðar efnislegar birgðapantanir** og velja síðan viðkomandi tengil.
2. Á síðunni **Bókaðar efnislegar birgðapantanir** skal velja bókuð pöntun efnislegra birgða sem á að skoða og síðan velja aðgerðina **Skoða**.
3. Til að skoða lista yfir tengdar skráningar efnislegra birgða skal velja aðgerðina **Skráningar**.

## <a name="handling-item-tracking-when-counting-inventory"></a><a name="handling-item-tracking-when-counting-inventory"></a>Meðhöndlun vörurakningar þegar birgðir eru taldar

Vörurakning á við um rað- eða lotunúmer sem er úthlutað á vörur. Við talningu á vöru sem geymd er í birgðum, t.d. sem 10 mismunandi lotunúmer, verður starfsmaðurinn að geta skráð hvaða og hversu margar einingar af hverju lotunúmeri eru í birgðum. Frekari upplýsingar um virkni vörurakningar er að finna í [Vinna með rað- og lotunúmer](inventory-how-work-item-tracking.md).

Gátreiturinn **Nota vörurakningu** í pöntunarlínum efnislegra birgða er sjálfkrafa valinn ef vörurakningarkóði er settur upp fyrir vöruna, en einnig er hægt að velja eða afvelja hann handvirkt.

### <a name="example---prepare-a-physical-inventory-recording-for-an-item-tracked-item"></a><a name="example---prepare-a-physical-inventory-recording-for-an-item-tracked-item"></a>Dæmi - Undirbúðu skráningu efnislegra birgða fyrir vörurakta vöru

Íhugaðu efnislegar birgðir fyrir vöru A sem er geymd í birgðum sem tíu mismunandi raðnúmer.
1. Á skráningarlínunni fyrir vöruna skal velja gátreitinn **Nota vörurakningu**.
2. Veldu reitinn **Raðnr.**, veldu fyrsta raðnúmerið sem er til í birgðum fyrir vöruna og veldu síðan hnappinn **Í lagi**.

    Afritið línuna fyrir fyrstu vöruna sem rakið er til til að setja inn viðbótarlínur sem samsvara raðnúmerum sem eru geymd í birgðum.

3. Veldu aðgerðina **Virkni** og síðan aðgerðina **Afrita línu**.
4. Á síðunni **Afrita skráningarlínu efnislegra birgða** skal færa inn 9 í reitinn **Fjöldi afrita** og síðan velja hnappinn **Í lagi**.
5. Í fyrstu línu afrituðu línanna skal velja reitinn **Raðnr.** og velja næsta raðnúmer vörunnar.
6. Endurtaktu skref 5 fyrir eftirstandandi átta raðnúmerin, og passa upp á að velja ekki sama númerið tvisvar sinnum.
7. Veldu aðgerðina **Prenta** til að undirbúa prentaða eintakið sem starfsmenn nota til að skrifa niður taldar vörur og rað-/lotunúmer.

Taktu eftir að skýrslan **Skráning efnislegra birgða** inniheldur tíu línur fyrir vöru A, eina fyrir hvert raðnúmer.

### <a name="example---record-and-post-counted-lot-number-differences"></a><a name="example---record-and-post-counted-lot-number-differences"></a>Dæmi - Skrá og bóka mismun á töldu lotunúmeri

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

Á síðunni **Pöntun efnislegra birgða** mun reiturinn **Neikvætt magn (grunnur)** innihalda *8*. Fyrir pöntunarlínunina sem um ræðir mun síðan **Listi yfir vörurakningu efnislegra birgða** innihalda jákvætt og neikvætt magn fyrir hvert lotunúmer.

## <a name="inventory-documents"></a><a name="inventory-documents"></a>Birgðaskjöl

Eftirfarandi gerðir skjala eru gagnlegar til að stjórna vöruhúsinu:

* Notið **Innhreyfingar birgða** til að skrá jákvæðar leiðréttingar á vörum út frá gæðum, magni og kostnaði.
* Notið **Birgðaafhendingar** til að afskrifa týndar eða skemmdar vörur.

Hægt er að prenta þessi skjöl á hvaða stigi sem er, losa þau og opna þau aftur og úthluta almennum gildum, þ.m.t. víddum, í hausnum. Ef ætlunin er að endurprenta skjölin eftir að þau hafa verið bókuð er hægt að gera það á síðunum **Bókuð birgðainnhreyfing** og **Bókuð birgðaafhending**.

> [!NOTE]
> Áður en hægt er að nota þessi skjöl þarf að tilgreina númeraröð til að búa til auðkennin. Nánari upplýsingar er að finna í næsta hluta.

### <a name="to-set-up-numbering-for-inventory-documents"></a><a name="to-set-up-numbering-for-inventory-documents"></a>Að setja upp númeraröð fyrir birgðaskjöl

Þessi verklýsing sýnir hvernig á að búa til númeraröð fyrir birgðaskjöl.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Uppsetning birgða** og velja síðan viðkomandi tengil.
2. Í flýtiflipanum **Tölusetning** skal tilgreina í eftirfarandi reitum númeraraðir fyrir skjöl:

   * **Birgðainnhreyfingarnr.**  
   * **Bókuð birgðamóttökunr.**  
   * **Birgðaafhendingarnr.**  
   * **Bókuð birgðaafhendingarnr.**  

### <a name="to-create-and-post-an-inventory-document"></a><a name="to-create-and-post-an-inventory-document"></a>Að stofna og bóka birgðaskjal

Eftirfarandi ferli sýnir hvernig á að stofna, prenta og bóka birgðamóttöku. Skrefin eru svipuð fyrir birgðaafhendingar.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Birgðamóttaka** og velja síðan viðkomandi tengil.  
2. Í haus síðunnar **Birgðamóttaka** skal velja staðsetninguna í reitnum **Staðsetningarkóði** og síðan fylla út eftirstandandi reiti eftir þörfum.
3. Á flýtiflipanum **Línur** í reitnum **Vara** skal velja birgðavöruna. Í reitinn **Magn** er fært magn vara sem á að bæta við. 
4. Til að prenta skýrslu **Birgðamóttöku** á síðunni **Birgðamóttaka** skal velja aðgerðina **Prenta**.

Eftirfarandi aðgerðir eru í boði á síðunni **Birgðamóttaka**:

* Veljið aðgerðina **Losa** eða **Enduropna** til að stilla stöðuna fyrir næsta úrvinnslustig  
* Veljið aðgerðina **Bóka** til að bóka birgðamóttökuna eða veljið **Bóka og prenta** til að bóka móttökuna og prenta prufuskýrsluna  

    [!INCLUDE [preview-posting-inventory](includes/preview-posting-inventory.md)]

## <a name="printing-inventory-documents"></a><a name="printing-inventory-documents"></a>Prentun birgðaskjala

Hægt er að tilgreina skýrslurnar sem þarf að prenta á mismunandi stigum með því að velja einn af eftirfarandi valkostum í reitnum **Notkun** á síðunni **Skýrsluval - Birgðir**:

* Birgðamóttaka
* Birgðaafhending
* Bókuð birgðamóttaka
* Bókuð birgðaafhending

> [!NOTE]
> Tiltækar skýrslur kunna að vera mismunandi eftir staðfæringu landsins. Grunnforritið inniheldur ekkert útlit.

## <a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a>Sjá tengda [Microsoft þjálfun](/training/modules/adjust-inventory/)

## <a name="see-also"></a><a name="see-also"></a>Sjá einnig .

[Talning, breytingar og endurflokkun birgða með færslubókum](inventory-how-count-adjust-reclassify.md)  
[Vinna með rað- og lotunúmer](inventory-how-work-item-tracking.md)  
[Birgðir](inventory-manage-inventory.md)  
[Yfirlit yfir vöruhúsakerfi](design-details-warehouse-management.md)  
[Sala](sales-manage-sales.md)  
[Innkaup](purchasing-manage-purchasing.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
