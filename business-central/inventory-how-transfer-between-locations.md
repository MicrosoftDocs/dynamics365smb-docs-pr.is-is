---
title: Flytja vörur á milli birgðageymslna
description: 'Frekari upplýsingar um hvernig á að flytja birgðir frá einum stað eða vöruhúsi til annars, annað hvort með endurflokkunarbók eða flutningspöntunum.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: how-to
ms.date: 02/21/2023
ms.custom: bap-template
ms.search.keywords: 'move, warehouse'
ms.search.forms: '5746, 5745, 5759, 5753, 5743, 5758, 5752, 5744, 5749, 5740, 5741, 5742, 5757, 5748, 5747, 9285, 5756, 5755'
---
# Flytja birgðir milli birgðageymslna

Það er hægt að flytja birgðavörur milli tveggja staða með því að búa til flutningspantanir. Einnig er hægt að nota vöruendurflokkunarbók.

> [!NOTE]
> Til að flytja vörur þarf að setja upp staðsetningar og flutningsleiðir. Til að fræðast meira um uppsetningu staðsetningar er farið í  [Setja upp staðsetningar](inventory-how-setup-locations.md). Ekki er hægt að nota flutningspantanir fyrir  *auða*  staði.

## Flutningspöntunum

Hægt er að senda sendingu út frá einum stað og fá heimflutning á áfangastað. Hægt er að:

* Rekja magn í flutningi
* Skilgreinið dagatöl, leiðir og afgreiðslutíma á innleið og útleið fyrir dagsetningarútreikninga og áætlanagerð. Til að fræðast meira um áætlanagerð er farið í  [um áætlunaraðgerðir](production-about-planning-functionality.md).
* Nota mismunandi vöruhúsaaðgerðir fyrir inn-og útleiðarstaði.
* Með sumum takmörkunum er hægt að nota flutningspantanir fyrir beinan flutning.

## Endurflokkunarbækur vöru

* Einfaldur, Beinn flutningur á vörum milli birgðageymslna.
* Flytja vörur milli hólfa. Frekari upplýsingar um flutning vara milli hólfa er að  [flytja Óáætlaðar vörur í Grunnvöruhúsafbrigðum](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md)
* Breyta lotu eða raðnúmeri á nýja lotu eða raðnúmeri. Til að fræðast meira um raðnúmer og lotunúmer er farið í  [endurflokka rað-eða lotunúmer](inventory-how-work-item-tracking.md#to-reclassify-serial-or-lot-numbers).
* Chang gildistíma til nýju dagsetningarinnar.
* Endurflokka vörur úr  *auða*  birgðageymslu í raunverulega staðsetningu.
* Vöruhúsaaðgerðum er ekki stjórnað. Vöruhúsafærslur verða stofnaðar.

## Vörur fluttar með flutningspöntun

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Flutningspantanir** og velja síðan viðkomandi tengil.
2. Fyllt er út í reiti eftir því sem á við á síðunni **Flutningspöntun**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
    >   Ef Millisendingarkóti, Kóti flutningsfyrirtækisins og  **Flutningsþjónusta** eru fylltir út  **í valnum leiðanna** **.**  **·**  síðu þegar Flutningsleiðin er sett upp eru samsvarandi svæði í millisendingarpöntuninni sjálfkrafa fyllt út.

    Þegar fyllt er út í reitinn **Flutningsþjónusta** reiknar kerfið út móttökudagsetningu fyrir flutt-til birgðageymslu með því að bæta flutningstíma flutningsþjónustunnar við afhendingardagsetninguna.

3. Til að fylla út í línurnar skal annaðhvort færa þær inn handvirkt eða velja einn eftirfarandi valkosta á undir aðgerðinni **Aðgerðir**:

    * Veldu **Sækja innihald hólfs** aðgerðina til að velja fyrirliggjandi vörur úr tilteknu hólfi á staðsetningunni.
    * Veldu **Sækja móttökulínur** til að velja vörur sem eru nýkomnar á sendist-frá staðsetningu.

    Sem starfsmaður vörugeymslu við flutninginn frá staðsetninginni skaltu halda áfram að senda vörurnar.
4. Veldu aðgerðina **Bóka** veldu **Senda** valkostinn og veldu síðan **Í lagi** hnappinn.

    Atriðin eru nú í flutningi milli tilgreindra staða, í samræmi við tilgreint flutningsleið.

    Sem starfsmaður vörugeymslu við flutninginn frá staðsetninginni skaltu halda áfram að fá vörurnar. Flutningspöntunarlínurnar eru þær sömu og við sendingu og er ekki hægt að breyta þeim.
5. Veldu aðgerðina **Bóka**, veldu **Móttaka** valkostinn og veldu síðan **Í lagi** hnappinn.

## Til að flytja vörur með vöruendurflokkunarbók

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Vöruendurflokkunarbók** og velja síðan viðkomandi tengil.
2. Á síðunni **Birgðaendurflokkunarbók** skal fylla út reitina eins og þörf krefur. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Í reitnum **Kóði birgðageymslu** er færð inn birgðageymslan þar sem vörurnar eru nú geymdar.

    > [!NOTE]  
    > Til að flytja hluti sem ekki hafa staðsetningarkóða skal skilja reitinn **Staðsetningarkóða** eftir auðan.
4. Í reitnum **Nýr staðsetningarkóði**, sláðu inn staðinn sem þú vilt flytja hlutina í.
5. Valið er **Bóka** aðgerðin.

## Sjá tengda [Microsoft þjálfun](/training/modules/transfer-items/)

## Sjá einnig .

[Stjórna birgðum](inventory-manage-inventory.md)  
[Uppsetning birgðageymsla](inventory-how-setup-locations.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Breyta því hvaða eiginleikar eru sýndir](ui-experiences.md)  
[Almenn viðskiptavirkni](ui-across-business-areas.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
