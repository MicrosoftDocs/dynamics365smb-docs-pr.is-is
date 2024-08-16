---
title: Flytja vörur milli vöruhúsastaðsetninga
description: 'Fræðast um hvernig á að færa birgðir frá einum stað eða vöruhúsi til annars, annaðhvort með endurflokkunarbókinni eða millifærslupöntunum.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.date: 08/12/2024
ms.custom: bap-template
ms.search.keywords: 'move, warehouse'
ms.search.forms: '5746, 5745, 5759, 5753, 5743, 5758, 5752, 5744, 5749, 5740, 5741, 5742, 5757, 5748, 5747, 9285, 5756, 5755'
ms.service: dynamics-365-business-central
---

# <a name="transfer-inventory-between-locations"></a>Flytja birgðir milli birgðageymslna

Það er hægt að flytja birgðavörur milli tveggja staða með því að búa til flutningspantanir. Einnig er hægt að nota vöruendurflokkunarbók.

> [!NOTE]
> Til að flytja vörur verður að setja upp birgðageymslur og flutningsleiðir. Nánari upplýsingar um uppsetningu birgðageymslna eru í [Uppsetning birgðageymslna](inventory-how-setup-locations.md). Ekki er hægt að nota millifærslupantanir fyrir *auðar* birgðageymslur.

## <a name="transfer-orders"></a>Millifærslupantanir

Hægt er að afhenda flutning á útleið frá einni birgðageymslu og taka á móti millifærslu á innleið. Hægt er að:

* Rekja magn í flutningi.
* Skilgreina dagatöl, leiðir og afgreiðslutíma á innleið og útleið fyrir útreikning dagsetninga og áætlunar. Nánari upplýsingar um áætlanir eru í [Um áætlunaraðgerðir](production-about-planning-functionality.md).
* Nota mismunandi vöruhúsaaðgerðir fyrir birgðageymslur á innleið og útleið.
* Nota millifærslupantanir fyrir beinar millifærslur, með nokkrum takmörkunum.

## <a name="item-reclassification-journals"></a>Endurflokkunarbækur birgða

Hægt er að nota síðuna **Endurflokkunarbækur** birgða til að:

* Bein flutningur á vörum milli birgðageymslna.
* Vörur færðar milli hólfa. Nánari upplýsingar um flutning á vörum milli hólfa [eru færðar á Vörur óáætlaðar í Grunngrunnstilling vöruhúss](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md).
* Breyta lotu- eða raðnúmeri í nýtt lotu- eða raðnúmer. Nánari upplýsingar um endurflokkun rað- og lotunúmera fást með því að [fara í Endurflokka rað- eða lotunúmer](inventory-how-work-item-tracking.md#to-reclassify-serial-or-lot-numbers).
* Breyta fyrningardagsetningu í nýja dagsetningu.
* Endurflokka vörur frá auðri birgðageymslu í raunverulega birgðageymslu.
* Stofna vöruhúsafærslur ef vöruhúsaaðgerðum er ekki stjórnað.

## <a name="to-transfer-items-with-a-transfer-order"></a>Vörur fluttar með flutningspöntun

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Flutningspantanir** og velja síðan viðkomandi tengil.
2. Fyllt er út í reiti eftir því sem á við á síðunni **Flutningspöntun**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
    > Hafi verið fyllt í reitina **Millifærslukóti**, **Flutningsaðilakóti** og **Flutningsþjónusta** í skilgreiningu flutningsleiðarinnar **.** síðu þegar flutningsleiðin er sett upp eru samsvarandi reitir í millifærslupöntuninni fylltir út sjálfkrafa.

    Þegar fyllt er út í reitinn **Flutningsþjónusta** reiknar kerfið út móttökudagsetningu fyrir flutt-til birgðageymslu með því að bæta flutningstíma flutningsþjónustunnar við afhendingardagsetninguna.

3. Hægt er að fylla út línurnar á marga vegu:

    |Valkostur  |Heimildasamstæða  |
    |---------|---------|
    |Með íhlutun notanda     | Á flýtiflipanum **Línur** er fyllt út í línu fyrir vöru eða aðgerðin **Velja vörur** notuð til að velja margar vörur.        |
    |Sjálfvirk aðferð     | * Veljið aðgerðina **Sækja innihald** hólfs til að velja fyrirliggjandi vörur úr tilteknu hólfi í birgðageymslunni.<br><br>* Velja skal **Sækja móttökulínur** til að velja vörur sem komu í sendist-frá birgðageymsluna.        |

    Nú er hægt að afhenda vörurnar.
4. Veldu aðgerðina **Bóka** veldu **Senda** valkostinn og veldu síðan **Í lagi** hnappinn.

    Vörurnar eru nú í flutningi milli tilgreindra birgðageymslna samkvæmt flutningsleiðinni.

    Sem starfsmaður vörugeymslu við flutninginn frá staðsetninginni skaltu halda áfram að fá vörurnar. Millifærslupöntunarlínurnar eru þær sömu og þegar þær eru afhentar og ekki hægt að breyta þeim.
5. Veldu aðgerðina **Bóka**, veldu **Móttaka** valkostinn og veldu síðan **Í lagi** hnappinn.

### <a name="undo-a-transfer-shipment"></a>Afturkalla millifærsluafhendingu

Ef mistök finnast í magni í bókuðum millifærslupöntunum ef afhendingin berst ekki er auðvelt að leiðrétta magnið. Á síðunni **Bókuð millifærsluafhending** stofnar aðgerðin **Afturkalla afhendingu** leiðréttingarlínur, eins og hér segir:

* Gildið í reitnum **Afhent** magn er minnkað um ógilt magn.
* Gildið í reitnum **Magn til afhendingar** hækkar um ógilt magn.
* Gátreiturinn **Leiðrétting** er valinn fyrir línurnar.

Ef afhent magn í vöruhúsaafhendingu er leiðréttingarlína stofnuð í bókuðu vöruhúsaafhendingunni.

Til að ljúka leiðréttingunni er millifærslupöntunin opnuð aftur, rétt magn fært inn og pöntunin síðan bókuð. Ef vöruhúsaafhending er notuð til að afhenda pöntunina skal stofna og bóka nýja vöruhúsaafhendingu.

### <a name="post-multiple-transfer-orders-in-a-batch"></a>Bóka margar millifærslupantanir í keyrslu

Eftirfarandi ferli útskýrir hvernig á að bóka millifærslupantanir í keyrslu.

1. 1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Flutningspantanir** og velja síðan viðkomandi tengil.  
2. Á síðunni **Millifærslupantanir** eru valdar pantanirnar sem á að bóka.
3. Í reitnum **númer** Skal opna samhengisvalmyndina og velja **Velja meira**.
4. Velja skal gátreitinn fyrir línurnar fyrir hverja pöntun sem á að bóka.
5. Velja skal aðgerðina **Bóka** og velja **svo Fjöldabóka**.
6. Á síðunni **Fjöldabóka millifærslupöntun** skal fylla út reitina eins og þörf krefur.

   > [!TIP]
    > Fyrir millifærslupantanir sem nota millifærslustað er hægt að velja Annaðhvort Afhenda **eða** **Móttaka**. Þetta er endurtekið ef þörf er á að gera bæði. Fyrir pantanir þar sem **kveikt er á bein bókun**  er kveikt á þeim vinna báðir valkostir á sama hátt og bóka pöntunina að fullu.

7. Valið er **Í lagi**.
8. Til að skoða hugsanleg vandamál er síðan Villuboðadagbók **opnuð** .

    > [!NOTE]
    > Bókun á mörgum skjölum gæti tekið nokkurn tíma og lokað á aðra notendur. Íhugaðu að virkja bakgrunnsbókun. Frekari upplýsingar, sjá [Nota verkraðir til að tímaraða verkhlutum](/dynamics365/business-central/admin-job-queues-schedule-tasks).

### <a name="schedule-a-job-queue-entry-to-post-multiple-documents-in-a-batch"></a>Tímasetja verkraðarfærslu til að bóka mörg skjöl í keyrslu

Einnig er hægt að nota verkröðina til að tímasetja bókun á þeim tíma sem hentar fyrirtækinu. Það gæti til dæmis verið vit í því að reka ákveðnar venjur þegar mest af gagnafærslunni fer fram á daginn.

Eftirfarandi ferli sýnir hvernig á að setja upp skýrsluna **Fjöldabóka millifærslupantanir** til að bóka sjálfkrafa beinar millifærslupantanir klukkan 18:00 á virkum dögum. Sá tími er bara dæmi. Skrefin eru eins fyrir önnur skjöl.  

1. Leita að síðunni **Verkraðarfærslur** og velja síðan viðeigandi tengja.  
2. Valið er aðgerðin **Nýtt**.  
3. Í reitnum **Gerð hlutar sem á að keyra** skal velja **Skýrsla**.  
4. Í reitnum **Hlutakenni í keyrslu** skal velja **5707, Fjöldabóka millifærslupantanir**.
5. Gátreiturinn **Skýrslubeiðnisíða** er valinn.
6. Á síðunni Fjöldabóka millifærslupantanir **skal velja valkostinn** Afhenda **, afmarka við** beina millifærslu **og velja** svo Í lagi **.**

   > [!IMPORTANT]
   > Mikilvægt er að setja afmarkanir. Annars bókar [!INCLUDE [prod_short](includes/prod_short.md)]  það öll skjöl, jafnvel þótt þau séu ekki tilbúin. Íhuga skal að setja afmörkun í reitinn **Staða** fyrir gildið **Útgefið** og afmörkun á reitnum **Bókunardags** . fyrir gildið **. Í dag**. Nánari upplýsingar um afmarkanir eru í [Röðun, Leit og Afmörkun](/dynamics365/business-central/ui-enter-criteria-filters).

7. Velja alla gátreiti frá **Keyra á mánudögum** til **Hlaupa á föstudögum**.
8. Í reitinn **Upphafstími** er slegið inn **4**.
9. Velja aðgerðina **Stilla stöðu á Tilbúin**.

### <a name="comparison-of-different-settings-for-transfer-orders"></a>Samanburður á mismunandi stillingum fyrir millifærslupantanir

Hægt er að bóka millifærslupantanir í mismunandi stillingum, með eða án millifærslustaðsetningar. Slökkva á víxl beins **millifærslu** og velja bráðabirgðastaðinn í reitnum **Millifærslukóti** á síðunni **Millifærslupöntun** . Þegar afhending millifærslupöntunar sem notar millifærslustaðinn er bókuð eru vörurnar í línunni ekki lengur tiltækar í einni af birgðageymslunum þar sem þær eru í millifærslu. Bein bókun tryggir að millifærslustaðsetning er ekki notuð og afhendingar- og móttökuferlið samtímis. Nákvæm hegðun bein bókun getur verið mismunandi eftir gildinu sem valið var í reitnum Bókun **beinnar** millifærslu á síðunni **Birgðagrunnur** .

Eftirfarandi tafla lýsir því hvernig samsetningarnar eru mismunandi.

|Möguleiki|Reiturinn Bein **millifærsla** er óvirkur á síðunni **Millifærslupöntun** |**Bein millifærsla** er virk á síðunni **Millifærslupöntun** </br>**Bein millifærslubókun** er stillt **á Bein flutningur** á síðunni **Birgðagrunnur** |**Bein millifærsla** er virk á síðunni **Millifærslupöntun** </br>**Bein millifærslubókun** er stillt á **Móttaka og Afhending** á síðunni **Birgðagrunnur** |
|---|---|---|---|
|Nota birgðageymslu á millifærslu|Já|Nr.|Nr.|
|Getur bókað móttöku án afhendingar.</br>Hægt er að nota **Afturkalla móttöku**.|Já|Nr.|Nr.|
|Hlutabókun|Já|Nr.|Já|
|Birgðabókafærslur|4:</br>Flytja frá birgðageymslu,</br>Flytja í millifærslu,</br>Millifærsla úr millifærslu,</br>Flytja til birgðageymslu.|2:</br>Flytja frá birgðageymslu,</br>Flytja til birgðageymslu.|4:</br>Flytja frá birgðageymslu,</br>Millifæra í *autt*,</br>Millifærsla úr *auðu*,</br>Flytja til birgðageymslu.|
|Bókuð fylgiskjöl|Bókuð millifærsluafhending,</br>Bókuð millifærslumóttaka.|Bókaður beinn flutningur|Bókuð millifærsluafhending,</br>Bókuð millifærslumóttaka.|
|Frátekning: á inn- og útleið|Já|Já|Já|
|Kostnaðarauki - úthlutað á bókaða millifærslumóttöku|Já|Nr.|Já|
|Vöruhúsastjórnun|Fullt|Nr.|Takmarkað, sjá hér að neðan|

Vöruhúsastjórnunarfylki fyrir grunnstillingu: **Bein flutningur** er virkur á síðunni **Millifærslupöntun** og **Bein millifærslubókun** er stillt **á Bein flutningur** á síðunni **Birgðagrunnur** .

|Frá \ til|Til: Engin vöruhúsastjórnun|Til: Vöruhúsamóttaka|Til: Birgðafrágangur|Til: Beinn frágangur og tínsla|
|-|-|-|-|-|
|**Frá: Engin vöruhúsastjórnun**|1|Ekki stutt|1, 4|Ekki stutt|
|**Frá: Vöruhúsaafhending**|1, 2|Ekki stutt|1,2,4|Ekki stutt|
|**Frá: Birgðafrágangur**|1, 3|Ekki stutt|1,3,4|Ekki stutt|
|**Frá: Beinn frágangur og tínsla**|2|Ekki stutt|2|Ekki stutt|

Númerin í reitunum sýna bókunarvalkostina sem eru studdir.

1. Bóka úr millifærslupöntun. Sumar samsetningar þarf ef til vill að fylla út reitinn **Magn til afhendingar** .
2. Stofna og bóka vöruhúsaafhendingu.
3. Stofna og bóka birgðatínslu.
4. Stofna og bóka birgðafrágang. Sumar samsetningar þarf ef til vill að fylla út reitinn **Magn til afhendingar** .

Burtséð frá aðferðinni eru afhendingar- og móttökufærslur framkvæmdar. Til dæmis er hægt að stofna millifærslupöntun úr birgðageymslu sem krefst birgðatínslu til birgðageymslu sem krefst birgðafrágangs. Hægt er að stofna og bóka birgðafráganginn og stofna bæði afhendingar- og móttökufærslur. Einnig er hægt að bóka slík fylgiskjöl úr millifærslupöntun eða úr birgðatínslu.  

Nánari upplýsingar um vöruhúsastjórnun eru [í Yfirlit vöruhúsakerfis](design-details-warehouse-management.md).

## <a name="to-transfer-items-with-the-item-reclassification-journal"></a>Til að flytja vörur með vöruendurflokkunarbók

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Vöruendurflokkunarbók** og velja síðan viðkomandi tengil.
2. Á síðunni **Birgðaendurflokkunarbók** skal fylla út reitina eins og þörf krefur. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Í reitnum **Kóði birgðageymslu** er færð inn birgðageymslan þar sem vörurnar eru nú geymdar.

    > [!NOTE]  
    > Til að flytja hluti sem ekki hafa staðsetningarkóða skal skilja reitinn **Staðsetningarkóða** eftir auðan.
4. Í reitnum **Nýr staðsetningarkóði**, sláðu inn staðinn sem þú vilt flytja hlutina í.
5. Valið er **Bóka** aðgerðin.

    [!INCLUDE [preview-posting-inventory](includes/preview-posting-inventory.md)]


## <a name="see-also"></a>Sjá einnig .

[Stjórna birgðum](inventory-manage-inventory.md)  
[Uppsetning birgðageymsla](inventory-how-setup-locations.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Breyta því hvaða eiginleikar eru sýndir](ui-experiences.md)  
[Almenn viðskiptavirkni](ui-across-business-areas.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
