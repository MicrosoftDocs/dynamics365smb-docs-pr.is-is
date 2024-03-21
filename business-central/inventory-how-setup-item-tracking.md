---
title: 'Setja upp vörurakningu með raðnúmer, lotu og pakkanúmer'
description: 'Setjið upp vörurakning með raðnúmerum, lotunúmerum og pakkanúmerum'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 08/31/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Setja upp vörurakningu með raðnúmer, lotu og pakkanúmer

Fylgist með birgðavörum jafnvel í flóknum skilgreiningum vöruhúss með númerum sem eru sértæk fyrir hverja vöru, annaðhvort sem einstakur hlutur, sem lota, eða sem pakkning. Með vörurakningu er hægt að rekja vörur í gegnum færslur innan vöruhúss og skjölum á útleið og innleið.

Vörur með rað- og lotunúmer er hægt að rekja bæði afturábak og áfram í aðfangakeðjunni. Þetta er nytsamlegt fyrir almennt gæðaeftirlit og vöruinnköllun. Frekari upplýsingar er að finna í [Rekja vörurakta vöru](inventory-how-to-trace-item-tracked-items.md).  

> [!TIP]
> Á útgáfutímabili 1 árið 2021  og síðar skal kveikja á eiginleikauppfærslunni *Nota rakningu eftir pakkanúmeri í frátekningu og rakningakerfi* ef vinna á með pakkanúmer ásamt rað- og lotunúmer. Frekari upplýsingar er að finna [Virkjun væntanlegra eiginleika fyrir tíma](admin-feature-management.md). Þegar kveikt er á eiginleikanum er hægt að úthluta pakkanúmerum á skjöl á útleið og innleið svipað og hægt er að vinna með lotunúmer.  

## Númer og vörurakning

Sem hluti af vöruhúsaferlunum til að geta sameinað birgðir í pökkum, kössum, gámum og svo framvegis. En til að halda utan um vörurnar er einkvæmum númerum úthlutað til auðkenningar. Til dæmis gæti verið framleiddur stóll sem er með vörunúmerið *1900-S*. Hver stóll er með raðnúmer, *1001*, en þú sameinar einnig fjóra stóla í lotu, *LOT0001*, og þú sendir stólana í gámi með pakkanúmerinu *CONTAINER010* sem einnig inniheldur aðrar vörur á borð við *LOT0100* með hliðarborðum og *LOT200* með lömpum.  

Það fer eftir skilgreiningunni hvernig þú notar þessi mismunandi númer til að fylgjast með birgðum í [!INCLUDE [prod_short](includes/prod_short.md)] á ýmsum stigum innkaupa, sölu, vöruhúsaaðgerða og svo framvegis.

## Til að setja upp vörurakningarkóða

Vörurakningarkóti endurspeglar ýmis íhugunarefni fyrirtækis varðandi notkun rað- og lotunúmera á vörur sem eru á leið í gegnum birgðirnar.  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Vörurakningarkóðar** og velja síðan viðkomandi tengil.  
2. Valið er aðgerðin **Nýtt**.
3. Fyllið inn reitina eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
4. Í flýtiflipunum **Raðnr.**, **Lotunr.** og **Pakkanr.** skal skilgreina aðferðir í vörurakningu eftir rað-, lotu- og pakkanúmerum.  

> [!NOTE]  
> Ef þú vilt fylgjast með ákveðnum vörum eða ákveðnum lotum í gegnum líftíma þeirra, verður þú að velja reitina **Sértæk SN rakning** og **Sértæk loturakning** í þessari röð. Þar af leiðandi þegar fengist er við einingu á útleið af vöru með þessum vörurakningarkóða verður þú alltaf að tilgreina hvaða fyrirliggjandi raðnúmer skuli notað. Þetta merkir að þegar seld er eining af vörunni verður að tengja hana ákveðnum hópi raðnúmera eða ákveðnu lotunúmeri í birgðum. Með öðrum orðum, raðnúmer eða lotunúmer sem tengt er vöru þegar hún fer í birgðir verður að fylgja þeirri vörutegund út úr birgðunum.

Þar sem þessi ákveðni uppsetningarreitur nær til allra mögulegra færslna varðandi vöruna verða einstakir inn-/útleiðarreitir einnig valdir. Þó hefur sérhver inn- og útleiðarreitur ekkert með jöfnun þvert á birgðir að gera - þeir eru aðeins til skilgreiningar á verkflæði í fyrirtækinu og hafa með það að gera hvenær á að úthluta vörurakningarnúmerum.  

> [!NOTE]  
> Til að úthluta vörurakningarnúmerum í vöruhúsaaðgerðum þarf að velja reitina **RN vöruhúsarakning** og **Lotuvöruhúsarakning** á vörurakningarkóðaspjaldi vörunnar.  

## Uppsetning gildistíma fyrir rað- og lotunúmer

Fyrir sumar vörur þarf ef til vill að setja upp tiltekna gildistíma og reglur með vörurakningaruppsetningunni. Með þessari aðgerð má fylgjast með því hvenær tiltekin rað- og lotunúmer falla úr gildi.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Vörurakningarkóðar** og velja síðan viðkomandi tengil.
2. Veljið fyrirliggjandi vörurakningarkóða og svo aðgerðina **Breyta**.  
3. Á flýtiflipanum **Ýmislegt** skal velja eftirfarandi reiti.  

    |Svæði|Description|  
    |---------------------------------|---------------------------------------|  
    |**Ströng lokasöludagsetning**|Tilgreinir að fyrningardagsetning sem tengd er vörunni þegar hún kemur í birgðir verður að gilda þegar hún fer þaðan.|  
    |**Krefjast lokadagsetningarfærslu**|Tilgreinir að færa þarf dagsetninguna þegar varan rennur út í vörurakningarlínuna.|  
    |**Nota lokadagsetningar**|Tilgreinir að þú viljir reikna út lokadagsetningar. |  

## Uppsetning ábyrgðar fyrir rað- og lotunúmer

Fyrir sumar vörur þarf ef til vill að setja upp tilteknar ábyrgðir í vörurakningarkótanum. Þessi aðgerðareiginleiki gerir kleift að halda utan um það hvenær ábyrgðin á tilteknum rað- eða lotunúmerum í birgðahaldi rennur út.  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Vörurakningarkóðar** og velja síðan viðkomandi tengil.  
2. Veljið fyrirliggjandi vörurakningarkóða og svo aðgerðina **Breyta**.  
3. Á flýtiflipanum **Ýmisl.** skal fylla inn í reitinn **Ábyrgðardagsetning** og velja svo reitina sem hér segir.  

    |Svæði|Description|  
    |---------------------------------|---------------------------------------|  
    |**Ábyrgðardagsetningarregla**|Tilgreinir síðasta dag ábyrgðar á vörunni.|  
    |**Krefjast færslu ábyrgðardagsetningarfærslu**|Tilgreinir að færa þurfi inn ábyrgðardagsetninguna handvirkt í vörurakningarlínuna.|  


## Til að setja upp vörur fyrir rakningu með réttum vörurakningarkóðum

Til að virkja vörurakningu þarftu fyrst að úthluta rakningarkóðum vöru á vöru. Tvær leiðir eru til að bæta við vörurakningarkóðum, með því að velja kóðann úr fyrirfram skilgreindum lista eða með því að úthluta nýjum einstökum kóða. Haltu bendlinum yfir reitunum til að lesa stutta lýsingu.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Vara** og velja síðan viðkomandi tengil.
2. Veljið fyrirliggjandi vöru af listanum og opnið síðuna **Vörukort**.  
3. Á flýtiflipanum **Vörurakning** skal úthluta viðeigandi vörurakningarkóðum og velja **Vörurakningarkóði**, **Raðnúmerin** og **Lotunúmerin**.
    1. Einnig er hægt að búa til nýjan vörurakningarkóða með því að velja aðgerðina **Nýtt**.

## Tilgreina opnunarstöður fyrir vörurnar sem fylgst er með

Hægt er að stofna opnunarstöður fyrir vörurnar sem fylgst er með. Þar sem hægt er að velja mismunandi vöruhúsafbrigðum eru tveir Valkostir:

* Virkja tilteknar keyrslur á  **síðunni vörubók**  til að leyfa fólki að færa inn rað-, Lot-og pakkagögn beint í færslubókarlínurnar.
* Fyrir staðsetningar þar sem  **beinn frágangur og tínsla**  er kveikt, skal nota  **síðuna raunbirgðabókarsíða**  vöruhúss til að gera allar vörurakningarsvæðin tiltæk. Svæðin sem eru tiltæk  **eru með reitina Ábyrgðardagsetning**  og  **·**  Lokadagsetning.

### Birgðabækur 

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Birgðabækur** og velja síðan viðkomandi tengil.
2. Reiturinn Name  **er**  valinn til að opna lista yfir birgðabókarkeyrslur.
3. Velja  **skal nýtt**  til að stofna nýja runu og kveikja síðan á  **vörurakningu í línum** .
4. Valið  **er í lagi**  til að velja rununnar sem var stofnuð.
5. Reitirnir í birgðabókarlínunni eru fylltir út eftir þörfum. Athugið að  **Lotunr.**,  **raðnr.**,  **Gildistími**,  **Ábyrgðardagsetning** og  **pakki nr.** Svæðin eru tiltæk (ef aðgerðin er gerð virk).
6. Velja skal  **aðgerðina Bóka**  til að leiðrétta birgðir.

> [!NOTE] 
> [!INCLUDE [prod_short](includes/prod_short.md)] tekur nokkrar minni háttar villuleit þegar gögn eru færð inn eða flutt inn. Ítarlegri könnun gerist þegar gögn eru  **bókuð eða flutt í Vörupöntunarglugga í gluggann** Vörurakning. Það síðarnefnda gerist sjálfkrafa þegar glugginn  **Vörurakning er opnaður**  úr birgðabókarlínu eða ef valið  **er aðgerðin uppfæra Vörurakningarlínur** .

### Raunbirgðabók vöruhúss fyrir staðsetningar þar sem beinar tínsla og frágangur er kveikt  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknið, færa inn  **Raunbirgðabók** vöruhúss og velja síðan tengda tengilinn.
2. Reitirnir í birgðabókarlínunni eru fylltir út eftir þörfum. Athugið að  **Lotunr.**,  **raðnr.**,  **Gildistími**,  **Ábyrgðardagsetning** og  **pakki nr.** Svæðin eru tiltæk (ef aðgerðin er gerð virk).
3. Velja skal  **aðgerðina skrá**  til að gera birgðaleiðréttingar. Þú þarft að samstilla leiðréttar vöruhúsafærslur við tengdar birgðafærslur. Til að fá frekari upplýsingar er farið að  [Samstilla leiðréttar vöruhúsafærslur](/dynamics365/business-central/inventory-how-count-adjust-reclassify#to-synchronize-the-adjusted-warehouse-entries-with-the-related-item-ledger-entries).

Fyrir fjöldainnflutning skal nota skilgreiningarpakka til að flytja inn gögn í færslubækur.

> [!NOTE]
> Ekki er hægt að nota  **Edit í Excel**  til að stofna færslubókarlínur með rakningarupplýsingum.

## Sjá einnig .

[Vinna með rað- og lotunúmer](inventory-how-work-item-tracking.md)  
[Rekja vöruraktar vörur](inventory-how-to-trace-item-tracked-items.md)  
[Birgðir](inventory-manage-inventory.md)  
[Hönnunarupplýsingar: Vörurakning](design-details-item-tracking.md)  
[Hönnunarupplýsingar - vörurakning og frátekningar](design-details-item-tracking-and-reservations.md)  
[Taka frá vörur](inventory-how-to-reserve-items.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
