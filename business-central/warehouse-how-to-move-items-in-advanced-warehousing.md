---
title: Færa vörur í vöruhúsum sem nota beinan frágang og tínslu
description: Í þessari grein er útskýrt hvernig á að færa vörur í birgðageymslum sem nota beinan frágang og tínslu.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.date: 04/23/2024
ms.custom: bap-template
ms.search.form: '7351,'
ms.service: dynamics-365-business-central
---

# <a name="move-items-in-advanced-warehouse-configurations-that-use-directed-put-away-and-pick"></a>Færa vörur í ítarlegri vöruhússkilgreiningu sem nota beinan frágang og tínslu

Hægt er að færa vörur milli hólfa án eftirspurnar úr upprunaskjali. Til dæmis væri hægt að gera það sem hluta af eftirfarandi aðgerðum:

* Endurskipuleggja vöruhúsið.
* Koma vörum á eftirlitssvæði.
* Taka vörur úr tínsluhólfum vöruhússins tímabundið, til dæmis til að þjóna sem sýnilíkön í sölukynningu.
* Flytja aukavörur í framleiðslusvæði fyrir íhluti sem eru grunnstilltir með nokkrum birgðaskráningaraðferðum.
* Flytja framleiddar eða settar saman vörur frá framleiðslu eða samsetningarsvæði í vöruhús.
* Færa vörur úr magngeymslusvæði í hólf sem notuð eru við tínslu.

Hvernig vörur eru færðar veltur á því hvernig vöruhúsið er sett upp sem birgðageymsla. Nánari upplýsingar um [uppsetningu vöruhúsastjórnunar](warehouse-setup-warehouse.md).

Í vöruhúsafbrigðum þar sem vífærslan Bein **tínsla og Frágangur** er virk fyrir birgðageymslur er hægt að skrá óáætlaðar hreyfingar á eftirfarandi síðum:  

* Hreyfingavinnublað
* Innanhússtínsla vöruhúss
* Innanhússfrágangur vöruhúss
* Vöruhúsaendurflokkunarbók

Síðurnar **Vinnublað**  hreyfingar, **Innanhússtínsla** vöruhúss og  **Innanhússfrágangur** vöruhúss virka á sama hátt. Nota síðurnar til að undirbúa vöruhúsaaðgerðir fyrir vöruhúsastarfsmenn. Munurinn er í ítarlegri aðgerð sem tengist hverri síðu og mismunandi tegundum vöruhúsaaðgerða sem líklega eru framkvæmdar af mismunandi starfsmönnum:

* Hreyfingavinnublað gerir kleift að fylla út tínsluhólf með vörum úr öðrum hólfum
* Frágangur notar frágangssniðmát
* Tínsla notar hólfaflokkun og ráðstöfunarmagn

## <a name="warehouse-movement-worksheet"></a>Vinnublað vöruhúsahreyfingar

### <a name="to-move-items-with-the-warehouse-movement-worksheet"></a>Til að færa vörur með vöruhúsahreyfingarvinnublaðinu

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Vinnublað hreyfingar** og velja síðan viðkomandi tengil.  
2. Reitirnir í vinnublaðslínunum eru fylltir út handvirkt eða ein af eftirfarandi aðgerðum notuð til að fylla sjálfkrafa í línurnar:

    * **Sækja innihald** hólfs í vinnublaðslínunum með innihaldi hólfsins eða hólfanna sem eru tilgreind.
    * **Reikna út áfyllingu** hólfa notar hólfaflokkunina til að leggja til áfyllingu á háflokkuðum hólfum úr lægra flokkuðum.

    > [!NOTE]  
    > Ef varan uppfyllir skilyrðin í listanum að neðan eru reitirnir **Frá svæði** og **Frá-hólf** auðir. [!INCLUDE [prod_short](includes/prod_short.md)] reiknar út hvar á að færa vörurnar aðeins þegar aðgerðin **Stofna hreyfingu** er notuð.  
    >  
    > * Varan er fyrningadagsett.  
    > * Kveikt **er á tínslunni Tína eftir FEFO-vísbendingunni** fyrir birgðageymsluna.  
    > * Aðgerðin Reikna út áfyllingu **hólfs** er notuð.  

3. Veljið aðgerðina **Stofna hreyfingu** til að stofna hreyfinguna. Þegar flutningi er lokið er hægt að skrá hana.  

### <a name="to-register-the-warehouse-movement"></a>Vöruhúsahreyfingin skráð

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Hreyfingar** og velja síðan viðkomandi tengil.  
2. Opna hreyfingaskjalið sem á að skrá.  
3. Á **staðalínum** er tilgreint hvar, og hvenær færa skuli vöruna með því að velja gildi í reitunum **Svæðiskóti**, **Hólfakóti**, **Magn til afgreiðslu** eða **Gjalddaga** .  
4. Í **Taka-línum** í reitnum **Magn til afgreiðslu** er tilgreint magn hólfainnihaldsins sem á að færa. Aðeins er hægt að breyta þessum reit í **Taka-línum** . 

    > [!NOTE]
    > Ef tína þarf eða setja vörur í einni línu í fleiri en eitt hólf, til dæmis vegna þess að merkta hólfið er fullt, skal nota aðgerðina **Skipta línu** á flýtiflipanum **Línur** . Aðgerðin stofnar línu fyrir eftirstandandi magn sem á að meðhöndla.
 
5. Til að skrá allt magn sem lagt er til eins og tilgreint er í reitnum **Magn** skal velja aðgerðina **Sjálfvirkt magn til afgreiðslu** .  
6. Velja aðgerðina **Skrá**.  

> [!NOTE]  
> Í birgðageymslum sem nota beinan frágang og tínslu er ekki hægt að færa vörur handvirkt í hólf af tegundinni **RECEIVE** vegna þess að þær eru ekki enn taldar tiltækar birgðir. Ganga þarf frá vörunum í þessum hólfum áður en þær eru tiltækar til hreyfinga.

## <a name="internal-pick"></a>Innanhússtínsla

### <a name="to-create-an-internal-pick"></a>Að búa til Innahússtínslur

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Innanhússtínsla** og velja síðan viðkomandi tengil.  
2. Valið er aðgerðin **Nýtt**.
3. Fylla þarf út reitinn **Nr.**. reitinn **Staðsetningarkóði**, og reitinn **Kóði til-hólfs** í flýtiflipanum **Almennt**. Reiturinn **Kóði til-hólfs** tilgreinir hólfið sem staðsetja á tíndar vörur. Við framleiðslu væri þetta hólf innhólf framleiðslu eða opið búðarhólf. Annars skal velja hólfakóða með hólfi af tegund sem ekki er notuð við tínslu, oftast nær undirbúnings- eða afhendingarhólf eða hólf fyrir sérstök tilefni.  
4. Vara er valin í reitnum **Vörunr.** og magnið sem á að tína fært inn.  
5. Veldu aðgerðina **Stofna tínslu**. Vöruhúsatínsluleiðbeiningar eru nú tilbúnar fyrir starfsmann vöruhúss. Einnig er hægt að velja aðgerðina **Gefa út** og stofna vöruhúsatínslur á síðunni **Vinnublað** tínslu. Nánari upplýsingar um tínsluvinnublöð eru í [Stofna tínsluskjöl í magni með tínsluvinnublaðinu](warehouse-how-to-pick-items-for-warehouse-shipment.md#to-create-pick-documents-in-bulk-with-the-pick-worksheet).
6. Þegar tínslunni er lokið er hægt að skrá hana.  

### <a name="to-register-the-warehouse-pick"></a>Vöruhúsatínsla skráð

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Tínslur** og velja síðan viðkomandi tengil.  

    Til að vinna við tiltekna tínslu er tínslan valin af listanum eða listinn afmarkaður til að finna tínslurnar sem úthlutað er á.  
2. Ef reiturinn **Úthlutað notandakenni** er auður er kenni notanda fært inn til að auðkenna sig, ef þörf krefur.  
3. Vörurnar eru tíndar.  

    Þar sem vöruhúsið er sett upp til að nota beinan frágang og tínslu ákvarðar hólfaflokkunin sem á að tína úr. Hólfin eru lögð til í tínslulínunum. Leiðbeiningarnar innihalda að minnsta kosti tvær aðskildar línur fyrir Aðgerðirnar Taka og Setja.  

4. Þegar vörurnar hafa verið tíndar og settar á afhendingarsvæðið eða í afhendingarhólfið skal velja aðgerðina **Skrá tínslu** .  

## <a name="internal-put-away"></a>Innanhússfrágangur

### <a name="to-create-an-internal-put-away"></a>Stofna innanhússfrágang

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, færa inn **Innanhússfrágang í vöruhúsi** og velja síðan viðeigandi tengil.  
2. Valið er aðgerðin **Nýtt**.
3. Fylla þarf út reitinn **Nr.**. og **Birgðageymslukóti** .
4. Fyllt er út í línu fyrir hverja vöru til að flytja í vöruhúsið. Reiturinn Vörunr **.**  **og nauðsynlegt er að fylla** út reitina Magn.

    > [!NOTE]  
    > Þegar vara er valin í reitnum Vörunr **.** opnast **síðan Innihald hólfs** í stað síðunnar **Vörur** . Þessi síða opnast vegna þess að verið er að ganga frá vöru sem er úthlutað tilteknu hólfainnihaldi *-*  ekki bara vöru og þegar er vitað úr hvaða hólfi á að taka vöruna. Ef reiturinn **Kóti frá-hólfs var fylltur** út er hólfainnihaldið afmarkað eftir því gildi.

5. Til að fylla línurnar út með öllu innihaldi hólfsins eða afmarkaða innihaldi hólfa í birgðageymslunni er aðgerðin Sækja innihald **hólfs** valin.  
6. Veldu aðgerðina **Stofna frágang**. Vöruhúsafrágangsleiðbeiningar eru nú tilbúnar fyrir starfsmann vöruhúss. Einnig er hægt að velja aðgerðina **Gefa út** til að stofna vöruhúsafrágang með síðunni **Frágangsvinnublað** . Nánari upplýsingar um vinnublöð frágangs eru í [Stofna frágangsskjöl í magni með frágangsvinnublaðinu](warehouse-how-to-put-items-away-with-warehouse-put-aways.md#to-create-put-away-documents-in-bulk-with-the-put-away-worksheet).
6. Þegar fráganginum er lokið er hægt að skrá hann.  

### <a name="to-register-the-warehouse-put-away"></a>Vöruhúsafrágangur skráður

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Frágangur** og velja síðan viðkomandi tengil.
2. Vöruhúsafrágangurinn sem er tilbúinn til afgreiðslu er opnaður.  
3. Kenni notanda er fært inn þegar vinna hefst við frágang ef með þarf.  

    Til að besta frágangsferlið er hægt að raða frágangslínum eftir ýmsum skilyrðum. Til dæmis eftir vöru, hillunúmeri eða gjalddaga.
   
    * Ef Taka- og Setja-línurnar fyrir hverja móttökulínu fylgja ekki hver annarri á ekki strax að fylgja og þess er óskað skal raða línunum með því að velja **Vara** í reitnum **Röðunaraðferð** .  
    * Ef hólfaflokkunin endurspeglar raunútlit vöruhússins er **röðunaraðferðin Hólfaflokkun** notuð til að skipuleggja vinnubrögð birgðageymslnanna í hólfum.

  > [!NOTE]  
  > Línum er raðað í hækkandi röð eftir völdum skilyrðum. Ef raðað er eftir fylgiskjali fer röðun fyrst eftir tegund fylgiskjals sem byggist á **upprunaskjali** vöruhúsaaðgerða. Ef raðað er eftir sendist-til fer röðun eftir tegund áfangastaðar sem byggð er á reitnum **Tegund** viðtöku vöruhúss.

4. Frágangurinn er framkvæmdur.

    Hver innanhússfrágangslína hefur orðið að minnsta kosti tvær línur í vöruhúsafrágangi.  

    * Fyrsta línan sem hefur **Taka** í reitnum **Aðgerð** sýnir hvar vörurnar eru staðsettar á móttökusvæðinu. Ekki er hægt að breyta svæði og hólfi í línunni.  
    * Næsta lína, með **Setja** í reitnum **Aðgerð**, sýnir hvar setja á vörurnar í vöruhúsinu. Ef tekið er á móti mörgum vörum í einni móttökulínu gæti þurft að ganga frá vörunum í mörg hólf svo að það er Setja-lína fyrir hvert hólf.  

5. Þegar allar vörurnar hafa verið settar í hólf samkvæmt skal velja aðgerðina **Skrá frágang**.  

## <a name="to-register-a-movement-that-has-already-happened"></a>Til að skrá hreyfingu sem þegar hefur gerst

Ef skrá þarf þá staðreynd að vörur hafa þegar verið fluttar í önnur hólf án frágangs, tínslu eða hreyfingar er hægt að nota vöruh **. Síðan Endurflokkunarbók** til að skrá hreyfinguna.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Endurflokkunarbók vöruhúss** og velja síðan viðkomandi tengil.  
2. Reitirnir **Vörunr.**, **, Frá-svæðiskóti**, **Kóti frá-hólfs**, **Til-svæðiskóti**, and **Kóti til-hólfse** eru fylltir út.  
3. Velja aðgerðina **Skrá**.  

## <a name="see-also"></a>Sjá einnig

[Yfirlit yfir vöruhúsakerfi](design-details-warehouse-management.md)
[Birgðir](inventory-manage-inventory.md)  
[Vöruhúsastjórnun sett upp](warehouse-setup-warehouse.md)  
[Samsetningardeild](assembly-assemble-items.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
