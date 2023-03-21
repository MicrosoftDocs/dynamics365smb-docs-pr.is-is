---
title: Flytja vörur í vöruhús sem nota beinan frágang og tínslu
description: Í þessari grein er útskýrt hvernig á að flytja vörur í staðsetningum sem nota beinan frágang og tínslu.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: conceptual
ms.date: 02/22/2023
ms.custom: bap-template
ms.search.form: '7351,'
---

# Flytja vörur í ítarlegar Vöruhúsaskilgreiningar sem nota beinan frágang og tínslu

Hægt er að flytja vörur milli hólfa án þess að eftirspurn sé eftir upprunaskjali. Til dæmis væri æskilegt að gera það sem hluta af eftirfarandi verkþáttum:

* Endurskipuleggja vöruhúsið.
* Koma vörum á eftirlitssvæði.
* Taka vörur úr vöruhúsi tínsluhólfa tímabundið, kannski til að þjóna sem sýnilíkön í sölukynningu.
* Færa aukaatriði í framleiðslusvæði fyrir íhluti sem eru skilgreindir með flæðiaðferðum.
* Færa framleiddar eða samsettar vörur úr framleiðslu eða samsetningarsvæði í vöruhús.
* Flytja vörur frá fjöldageymslusvæði í hólf sem notuð eru við tiltekt.

Hvernig vörur eru færðar fer eftir því hvernig vöruhúsið er sett upp sem Birgðageymsla. Frekari upplýsingar um  [uppsetningu vöruhúsastjórnunar](warehouse-setup-warehouse.md).

Í vöruhúsaleiðingum þar sem  **beinn tínsla tínslu-**  og frágangs er kveikt fyrir birgðageymslur er hægt að skrá óáætlaðar hreyfingar á eftirfarandi síðum:  

* Hreyfingavinnublað
* Innanhússtínsla vöruhúss
* Frágangur á innri frágangi vöruhúss
* Endurflokkunarbók vöruhúss

 **Vinnublaðsíðurnar hreyfing**,  **Innanhússtínsla** og   **leirflissíur**  í innanhússfrágangi virka á svipaðan hátt. Notið síðurnar til að undirbúa vöruhúsaaðgerðir fyrir vöruhúsastarfsmenn. Munurinn er í ítarlegri virkni sem tengist hverri síðu og mismunandi gerðum vöruhúsaaðgerða sem eru líklega framkvæmdar af mismunandi starfsmönnum:

* Hreyflaverkstæði leyfir að fyllt sé út hólf háflokkunar með vörum úr öðrum hólfum
* Frágangur nota sniðmát
* Tiltekt notar hólfaflokkun og ráðstöfunarmagn

## Vinnublað vöruhúsahreyfinga

### Til að færa vörur með vöruhúsahreyfingarvinnublaðinu

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Vinnublað hreyfingar** og velja síðan viðkomandi tengil.  
2. Reitirnir í vinnublaðslínunum eru fylltir út eða Notið eina af eftirfarandi aðgerðum til að fylla sjálfvirkt út línurnar:

    * **Sækja hólfainnihald**  fyllir vinnublaðslínurnar með innihaldi hólfsins eða hólfanna sem tilgreind eru.
    * **Reikna** út áfyllingu hólfa notar bin búkings til að stinga upp á áfyllingu fyrir hólf á háu röðum úr hólfum með lág flokkun.

    > [!NOTE]  
    > Ef varan uppfyllir skilyrðin í listanum hér  **á eftir verður reiturinn frá svæði**  og  **úr hólfi**  auður. [!INCLUDE [prod_short](includes/prod_short.md)] reiknar út hvaðan á að flytja vörurnar þegar aðgerðin Stofna hreyfingu  **er notuð** .  
    >  
    > * Varan er fyrningadagsett.  
    > *  **Tínsla í samræmi við FEFO**  víxla er kveikt fyrir birgðageymsluna.  
    > * Aðgerðin Reikna Hólfáfyllingu  **er notuð** .  

3.  **Veldu stofna hreyfingaraðgerð**  til að búa til hreyfinguna. Þegar ferðinni er lokið er hægt að skrá sig í hana.  

### Vöruhúsahreyfingin skráð

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Hreyfingar** og velja síðan viðkomandi tengil.  
2. Opnið hreyfingarskjalið til að skrá.  
3.  **Í línum í stað**  skal tilgreina hvar, sem og af Hvenær á að flytja vöruna með því að velja gildi í  **svæðiskóta**,  **hólfkóta**,  **Magn til afgreiðslu** eða  **skiladags** .  
4.  **Í**  **reitnum Magn til afgreiðslu**  er tilgreint magn hólfainnihaldanna sem á að flytja. Aðeins er hægt að breyta þessu svæði í  **taka**  línur. 

    > [!NOTE]
    > Ef taka þarf vörurnar í eina línu í fleiri en einu hólfi, til dæmis vegna þess að það merkta hólfið er fullt, skal nota  **aðgerðina skipta línu**  á  **fastflipanum línur** . Aðgerðin býr til línu fyrir eftirstandandi magn sem á að afgreiða.
 
5. Til að skrá allar tillögur um magn eins og tilgreint er í  **reitnum Magn**  skal velja  **Magn í <% til að meðhöndla**  aðgerðina.  
6. Velja aðgerðina **Skrá**.  

> [!NOTE]  
> Fyrir staðsetningar sem nota beinan frágang og tínslu er ekki hægt að flytja vörur handvirkt í hólfum af gerðinni  **Móttaka**  vegna þess að þær eru ekki enn hugsaðar sem tiltækar birgðir. Ganga skal frá vörunum í þessum hólfum áður en þær eru tiltækar til hreyfingar.

## Innanhússtínslu  

### Að búa til Innahússtínslur  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Innanhússtínsla** og velja síðan viðkomandi tengil.  
2. Valið er aðgerðin **Nýtt**.
3. Fylla þarf út reitinn **Nr.**. reitinn **Staðsetningarkóði**, og reitinn **Kóði til-hólfs** í flýtiflipanum **Almennt**. Reiturinn **Kóði til-hólfs** tilgreinir hólfið sem staðsetja á tíndar vörur. Við framleiðslu væri þetta hólf innhólf framleiðslu eða opið búðarhólf. Annars skal velja hólfakóða með hólfi af tegund sem ekki er notuð við tínslu, oftast nær undirbúnings- eða afhendingarhólf eða hólf fyrir sérstök tilefni.  
4. Vara er valin í reitnum **Vörunr.** og magnið sem á að tína fært inn.  
5. Veldu aðgerðina **Stofna tínslu**. Vöruhúsatínsluleiðbeiningar eru nú tilbúnar fyrir starfsmann vöruhúss. Einnig er hægt að  **Velja úttektaraðgerð**  og stofna vöruhúsaaðgerðir með því að  **nota síðuna tínsluvinnublað** . Frekari upplýsingar um tínsluvinnublöð er að  [Stofna tínsluskjöl í fjöldahjálparblöðum tínslublaðsins](warehouse-how-to-pick-items-for-warehouse-shipment.md#to-create-pick-documents-in-bulk-with-the-pick-worksheet).
6. Þegar tínunni er lokið er hægt að skrá hana.  

### Vöruhúsatínsla skráð

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Tínslur** og velja síðan viðkomandi tengil.  

    Til að vinna að tiltekinni tínslu skaltu velja tínslu úr listanum eða sía listann til að finna tínsluna sem er úthlutað á þig.  
2.  **Ef reiturinn úthlutað notandakenni**  er auður skal FÆRA inn kennið til að auðkenna notandann ef þörf krefur.  
3. Tínsla varanna.  

    Þar sem vöruhúsið er sett upp til að nota beinan frágang og tínslu ákvarðar hólfaflokkun hólfin sem á að velja úr. Hólfin eru lögð til í tínslulínunum. Leiðbeiningarnar innihalda að minnsta kosti tvær aðskildar línur til að taka og setja aðgerðir.  

4. Þegar búið er að velja og setja vörurnar í sendingarsvæði eða afhendingarhólf skal velja  **aðgerðina skrá tínslu** .  

## Frágangur innanhúss  

### Stofna innanhússfrágang  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Teiknið, færa inn  **innanhússfrágang** vöruhúss og velja síðan tengda tengilinn.  
2. Valið er aðgerðin **Nýtt**.
3. Fylla þarf út reitinn **Nr.**. Og  **kóti**  birgðageymslu.
4. Fyllt er út í línu fyrir hverja vöru til að flytja í vöruhúsið.  **Vörunr.**  **og magnsvæðin**  eru nauðsynleg.

    > [!NOTE]  
    > Þegar vara er valin í reitnum  **Vörunr.**  **opnast hólfainnihaldssíðunum**  í stað  **atriða**  síðunnar. Þessi síða opnast vegna þess að verið er að ganga frá vöru sem er tengd tilteknu hólfi-  *hólfi*  -ekki bara vöru, og þú veist nú þegar hólfið sem taka á atriðið af. Ef reiturinn Kóti frá-hólfs  **er fylltur út**  mun innihald hólfsins afmarkast af því gildi.

5. Ef fylla á línurnar með öllu innihaldi hólfsins eða síuðu innihaldi hólfa á staðnum er aðgerðin Sækja innihald  **hólfs valin** .  
6. Veldu aðgerðina **Stofna frágang**. Vöruhúsafrágangsleiðbeiningar eru nú tilbúnar fyrir starfsmann vöruhúss. Einnig er hægt að velja  **úttektaraðgerðina**  til að stofna vöruhúsafrágang með því  **að nota síðuna frágangsvinnublað** . Til að fræðast meira um frágang vinnublaða er farið í að  [Stofna frágang skjala í magni með vinnublaði frágangs](warehouse-how-to-put-items-away-with-warehouse-put-aways.md#to-create-put-away-documents-in-bulk-with-the-put-away-worksheet).
6. Þegar frágangi er lokið er hægt að skrá það.  

### Frágangur vöruhúss skráður

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Frágangur** og velja síðan viðkomandi tengil.
2. Opna vöruhúsafráganginn sem er tilbúinn til afgreiðslu.  
3. Ef þörf er á skal færa inn NOTANDAKENNI þegar unnið er við frágang.  

    Til að hámarka frágangsferlið er hægt að raða frágangslínunum eftir ýmsum skilyrðum. Til dæmis eftir vöru, Hillunúmer eða gjalddaga.

    * Ef taka og setja línur fyrir hverja móttökulínu eiga ekki strax að fylgja annarri annarri og á þeim er hægt að raða línunum með því að velja  **atriði**  í  **reitnum röðunaraðferð** .  
    * Ef bin fremstur endurspeglar efnislegt skipulag vöruhúss skal nota  **röðunaraðferðina hólfaflokkun**  til að skipuleggja hólfastaðsetningar.  

4. Framkvæma frágang.

    Hver innanhússfrágangslína hefur orðið að minnsta kosti tveimur línum í vöruhúsafrágangi.  

    * Fyrsta línan sem hefur **Taka** í reitnum **Aðgerð** sýnir hvar vörurnar eru staðsettar á móttökusvæðinu. Ekki er hægt að breyta svæði og hólfi í þessari línu.  
    * Næsta lína, með  **stað**  í  **reitnum Tegund**  aðgerðar, sýnir hvar á að setja vörurnar í vöruhúsinu. Ef mikið af vörum er fengið í einni móttökulínu gæti þurft að ganga frá vörunum í nokkrum hólfum svo það sé sæti lína fyrir hvert hólf.  

5. Þegar allar vörurnar hafa verið settar í hólf samkvæmt skal velja aðgerðina **Skrá frágang**.  

## Að skrá hreyfingu sem þegar hefur gerst

Ef skrá þarf þá staðreynd að vörur hafa þegar verið færðar í önnur hólf án frágangs, tínslu eða hreyfingar er hægt að  **nota vöruhúsaafhendingin. Endurflokkunarbókar**  síða til að skrá hreyfinguna.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Endurflokkunarbók vöruhúss** og velja síðan viðkomandi tengil.  
2. Reitirnir **Vörunr.**, **, Frá-svæðiskóti**, **Kóti frá-hólfs**, **Til-svæðiskóti**, and **Kóti til-hólfse** eru fylltir út.  
3. Velja aðgerðina **Skrá**.  

## Sjá tengda [Microsoft þjálfun](/training/modules/manage-internal-warehouse-processes/)

## Sjá einnig

[Yfirlit](design-details-warehouse-management.md)
[vöruhúsakerstjórnunar birgðir](inventory-manage-inventory.md)  
[Vöruhúsastjórnun sett upp](warehouse-setup-warehouse.md)  
[Samsetningardeild](assembly-assemble-items.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
