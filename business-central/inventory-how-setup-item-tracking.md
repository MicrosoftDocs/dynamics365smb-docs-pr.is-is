---
title: 'Setja upp vörurakningu með rað-, lotu- og pakkanúmerum'
description: 'Setjið upp vörurakning með raðnúmerum, lotunúmerum og pakkanúmerum'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 06/06/2024
ms.service: dynamics-365-business-central
---
# <a name="set-up-item-tracking-with-serial-lot-and-package-numbers"></a>Setja upp vörurakningu með rað-, lotu- og pakkanúmerum

Fylgist með birgðavörum jafnvel í flóknum skilgreiningum vöruhúss með númerum sem eru sértæk fyrir hverja vöru, annaðhvort sem einstakur hlutur, sem lota, eða sem pakkning. Með vörurakningu er hægt að rekja vörur í gegnum færslur innan vöruhúss og skjölum á útleið og innleið.

Vörur með rað- og lotunúmer er hægt að rekja bæði afturábak og áfram í aðfangakeðjunni. Þetta er nytsamlegt fyrir almennt gæðaeftirlit og vöruinnköllun. Frekari upplýsingar er að finna í [Rekja vörurakta vöru](inventory-how-to-trace-item-tracked-items.md).  

## <a name="numbers-and-item-tracking"></a>Númer og vörurakning

Sem hluti af vöruhúsaferlunum til að geta sameinað birgðir í pökkum, kössum, gámum og svo framvegis. En til að halda utan um vörurnar er einkvæmum númerum úthlutað til auðkenningar. Til dæmis gæti verið framleiddur stóll sem er með vörunúmerið *1900-S*. Hver stóll er með raðnúmer, *1001*, en þú sameinar einnig fjóra stóla í lotu, *LOT0001*, og þú sendir stólana í gámi með pakkanúmerinu *CONTAINER010* sem einnig inniheldur aðrar vörur á borð við *LOT0100* með hliðarborðum og *LOT200* með lömpum.  

Það fer eftir skilgreiningunni hvernig þú notar þessi mismunandi númer til að fylgjast með birgðum í [!INCLUDE [prod_short](includes/prod_short.md)] á ýmsum stigum innkaupa, sölu, vöruhúsaaðgerða og svo framvegis.

## <a name="to-set-up-item-tracking-codes"></a>Til að setja upp vörurakningarkóða

Vörurakningarkóti endurspeglar ýmis íhugunarefni fyrirtækis varðandi notkun rað- og lotunúmera á vörur sem eru á leið í gegnum birgðirnar.  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Vörurakningarkóðar** og velja síðan viðkomandi tengil.  
2. Valið er aðgerðin **Nýtt**.
3. Fyllið inn reitina eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
4. Á flýtiflipunum **Raðnr.**, **Lotunr.** og **Rakning sendingar** skilgreina reglur vörurakningar eftir rað-, lotu- og pakkanúmerum.  

> [!NOTE]  
> Ef rekja á tilteknar vörur eða tilteknar lotur allan ævi þeirra verður að velja reitina **Rakning bundin við raðnr.raðnr.,** Rakning **·**  lotu og **Rakning tiltekinnar sendingar**, eftir því sem við á. Þegar meðhöndla á útleið af vöru með þennan vörurakningarkóta verður alltaf að tilgreina hvaða fyrirliggjandi raðnúmer eða hvaða fyrirliggjandi lotunúmer skuli meðhöndla. Þetta merkir að þegar seld er eining af vörunni verður að tengja hana ákveðnum hópi raðnúmera eða ákveðnu lotunúmeri í birgðum. Með öðrum orðum, rað-, lotu- eða pakkanúmer sem tengt er vörunni þegar hún fer í birgðir verður að fylgja þeirri vörutegund út úr birgðunum.

Þar sem þessir uppsetningarreitir ná til allra mögulegra færslna vörunnar eru einstakir inn-/útleiðarreitir valdir. Hins vegar koma einstakir inn-/útleiðarreitir jöfnun þvert á birgðir ekkert við. Þeir eru eingöngu til skilgreiningar á vinnuflæði fyrirtækisins varðandi það hvenær á að úthluta vörurakningarnúmerum.  

> [!NOTE]  
> Til að úthluta vörurakningarnúmerum í vöruhúsaaðgerðum þarf að velja reitina **RN vöruhúsarakning** og **Lotuvöruhúsarakning** á vörurakningarkóðaspjaldi vörunnar.  

## <a name="to-set-up-expiration-rules-for-serial-or-lot-numbers"></a>Uppsetning gildistíma fyrir rað- og lotunúmer

Fyrir sumar vörur þarf ef til vill að setja upp tiltekna gildistíma og reglur með vörurakningaruppsetningunni. Með þessari aðgerð má fylgjast með því hvenær tiltekin rað- og lotunúmer falla úr gildi.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Vörurakningarkóðar** og velja síðan viðkomandi tengil.
2. Veljið fyrirliggjandi vörurakningarkóða og svo aðgerðina **Breyta**.  
3. Á flýtiflipanum **Ýmislegt** skal velja eftirfarandi reiti.  

    |Svæði|Description|  
    |---------------------------------|---------------------------------------|  
    |**Ströng lokasöludagsetning**|Tilgreinir að fyrningardagsetning sem tengd er vörunni þegar hún kemur í birgðir verður að gilda þegar hún fer þaðan.|  
    |**Krefjast útrunninnar dagsetningarfærslu**|Tilgreinir að færa þarf dagsetninguna þegar varan rennur út í vörurakningarlínuna.|  
    |**Nota lokadagsetningar**|Tilgreinir að þú viljir reikna út lokadagsetningar. |  

## <a name="to-set-up-warranties-for-serial-or-lot-numbers"></a>Uppsetning ábyrgðar fyrir rað- og lotunúmer

Fyrir sumar vörur þarf ef til vill að setja upp tilteknar ábyrgðir í vörurakningarkótanum. Þessi aðgerðareiginleiki gerir kleift að halda utan um það hvenær ábyrgðin á tilteknum rað- eða lotunúmerum í birgðahaldi rennur út.  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Vörurakningarkóðar** og velja síðan viðkomandi tengil.  
2. Veljið fyrirliggjandi vörurakningarkóða og svo aðgerðina **Breyta**.  
3. Á flýtiflipanum **Ýmisl.** skal fylla inn í reitinn **Ábyrgðardagsetning** og velja svo reitina sem hér segir.  

    |Svæði|Description|  
    |---------------------------------|---------------------------------------|  
    |**Ábyrgðardagsetningarregla**|Tilgreinir síðasta dag ábyrgðar á vörunni.|  
    |**Krefjast færslu ábyrgðardagsetningarfærslu**|Tilgreinir að færa þurfi inn ábyrgðardagsetninguna handvirkt í vörurakningarlínuna.|  

## <a name="to-set-up-items-for-tracking-with-the-correct-item-tracking-codes"></a>Til að setja upp vörur fyrir rakningu með réttum vörurakningarkóðum

Til að gera vörurakningu virka þarf fyrst að úthluta vörurakningarkótum á vöru. Tvær leiðir eru til að bæta við vörurakningarkóðum, með því að velja kóðann úr fyrirfram skilgreindum lista eða með því að úthluta nýjum einstökum kóða. Haltu bendlinum yfir reitunum til að lesa stutta lýsingu.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Vara** og velja síðan viðkomandi tengil.
2. Veljið fyrirliggjandi vöru af listanum og opnið síðuna **Vörukort**.  
3. Á flýtiflipanum **Vörurakning** skal úthluta viðeigandi vörurakningarkóðum og velja **Vörurakningarkóði**, **Raðnúmerin** og **Lotunúmerin**.
    1. Einnig er hægt að búa til nýjan vörurakningarkóða með því að velja aðgerðina **Nýtt**.

## <a name="to-specify-opening-balances-for-the-items-you-track"></a>Til að tilgreina opnunarstöðu fyrir vörurnar er rakið

Hægt er að stofna opnunarstöðu fyrir vörurnar sem verið er að rekja. Þar sem hægt er að velja mismunandi vöruhúsaskilgreiningar eru tveir valkostir:

* Gera sérstakar keyrslur virkar á síðunni **Birgðabók** svo að fólk færi inn rað-, lotu- og sendingargögn beint í færslubókarlínur.
* Fyrir birgðageymslur þar sem **kveikt er á vísbendingunni Beinn frágangur og tínsla** skal nota **síðuna Raunbirgðabók** vöruhúss til að gera alla vörurakningarreiti tiltæka. Í reitunum sem tiltækir eru eru **ábyrgðardagsetning** og **Lokadags** .

### <a name="item-journals"></a>Birgðabækur

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Birgðabækur** og velja síðan viðkomandi tengil.
2. Velja skal reitinn **Heiti** til að opna lista yfir birgðabókarkeyrslur.
3. Velja skal **Nýtt** til að stofna nýja keyrslu og kveikja svo á vífærslunni **Vörurakning í línum** .
4. Velja skal **Í lagi** til að velja keyrsluna sem var stofnuð.
5. Reitirnir í birgðabókarlínunni eru fylltir út eins og þörf krefur. Bent er á **að Lotunr.**, **Raðnr.**, **Útrunnið,** **Ábyrgðardagsetning** og **Pakkanr.** Reitir eru tiltækir (ef aðgerðin er virk).
6.  **Veljið Bóka** aðgerð til að leiðrétta birgðir.

> [!NOTE] 
> [!INCLUDE [prod_short](includes/prod_short.md)] gerir nokkrar minniháttar prófanir þegar gögn eru færð inn eða flutt inn. Ítarlegri athugun gerist þegar gögn eru bókuð eða flutt úr bókarlínum á **síðuna Vörurakning** . Hið síðarnefnda gerist sjálfkrafa þegar síðan Vörurakning er opnuð **úr** birgðabókarlínunni eða ef aðgerðin **Uppfæra vörurakningarlínur** er valin.

### <a name="warehouse-physical-inventory-journal-for-locations-where-directed-pick-and-put-away-is-turned-on"></a>Raunbirgðabók vöruhúss fyrir birgðageymslur þar sem kveikt er á beinni tínslu og frágangi

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, færa inn **Raunbirgðabók** vöruhúss og velja síðan viðeigandi tengja.
2. Reitirnir í birgðabókarlínunni eru fylltir út eins og þörf krefur. Bent er á **að Lotunr.**, **Raðnr.**, **Útrunnið,** **Ábyrgðardagsetning** og **Pakkanr.** Reitir eru tiltækir (ef aðgerðin er virk).
3. Velja skal aðgerðina **Dagbók** til að gera birgðaleiðréttingar. Muna þarf að samstilla leiðréttu vöruhúsafærslurnar við tengdar birgðafærslur. Nánari upplýsingar eru notaðar til að [samstilla leiðréttu vöruhúsafærslurnar](/dynamics365/business-central/inventory-how-count-adjust-reclassify#to-synchronize-the-adjusted-warehouse-entries-with-the-related-item-ledger-entries).

Fyrir magninnflutning skal nota grunnstillingarpakka til að flytja gögn inn í færslubækurnar.

> [!NOTE]
> Ekki er hægt að nota **Breyta í Excel** til að stofna færslubókarlínur með rakningarupplýsingum.

## <a name="see-also"></a>Sjá einnig .

[Vinna með rað- og lotunúmer](inventory-how-work-item-tracking.md)  
[Rekja vöruraktar vörur](inventory-how-to-trace-item-tracked-items.md)  
[Birgðir](inventory-manage-inventory.md)  
[Hönnunarupplýsingar: Vörurakning](design-details-item-tracking.md)  
[Hönnunarupplýsingar - vörurakning og frátekningar](design-details-item-tracking-and-reservations.md)  
[Taka frá vörur](inventory-how-to-reserve-items.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
