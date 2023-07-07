---
title: Hönnunarupplýsingar - síða vörurakningarlína
description: Lestu um hvernig skal stjórna flæði rað- og lotunúmera í birgðum með síðu vörurakningarlína.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'design, inventory, item, tracking, serial number, lot number'
ms.date: 06/15/2021
ms.author: edupont
---
# <a name="design-details-item-tracking-lines-page"></a>Hönnunarupplýsingar: síða vörurakningarlína
Vörurakningarfærslur og frátekningarfærslur eru stofnaðar í frátekningarkerfi og framboð þeirra er reiknað eftir þörfum. Gögnum sem eru færð á síðuna **Vörurakningarlínur** er stjórnað í tímabundinni útgáfu af töflunni **Rakningarlýsing**. Þegar síðunni er lokað eru virku gögnin skuldbundin töflunni **Frátekningarfærsla** og söguleg gögn skuldbundin töflunni **Rakningarlýsing**. Frekari upplýsingar, sjá: [Hönnunarupplýsingar: Virk móti sögulegum vörurakningarfærslum](design-details-active-versus-historic-item-tracking-entries.md).  
  
Leit úr reitunum **Raðnúmer** og **Lotunúmer** sýna framboð sem byggist á bæði á töflunni **Birgðafærsla** og töflunni **Frátekningarfærsla**, án dagsetningarsíu. Fylki magnreita í haus gluggans **Vörurakningarlínur** birtir með gagnvirkum hætti magn og fjárhæð vörurakningarnúmera sem slegin eru inn í línurnar á síðunni. Magnið verður að samsvara því sem er í fylgiskjalslínunni, og er sýnt með **0** undir **Óskilgreint** reitunum í haus síðunnar.  
  
Til að samræma flæði rað- og lotunúmera gegnum birgðir, eru eftirfarandi reglur til að slá inn gögn á síðuna **Vörurakningarlínur**:  
  
* Fyrir vörurakningarlínur bæði á innleið og útleið er ekki hægt að setja inn raðnúmer með eða án lotunúmers oftar en einu sinni í sama tilviki **Vörurakningarnúmer** síðunnar. Ef reynt er að slá inn einhverja samsetningu af rað- eða lotunúmerum sem eru þegar til staðar á síðunni, þá hindra villuboð gagnaskráninguna.  
* Fyrir vörurakningarlínur á innleið er ekki hægt að bóka tengda skjalið ef vara af sama afbrigði og með sama raðnúmer er þegar í birgðum. Ef reynt er að bóka jákvæða línu fyrir birgðavöru með sama afbrigði og raðnúmeri, þá hindra villuboð bókunina. Hins vegar, fyrir bæði vörurakningarlínur á innleið og á útleið á opnum fylgiskjölum, er hægt að hafa sömu samsetningu rað- eða lotunúmera sem tengjast mismunandi upprunaskjalslínum, það er að segja, eru til í mismunandi tilvikum af **Vörurakningarlínur** síðunni þangað til tengda fylgiskjalið er bókað.  
* Ef varan er sett upp fyrir tilgreinda raðnúmerarakningu eða tilgreinda lotunúmerarakningu er ekki hægt að bóka skjalalínu á útleið nema vara með skilgreinda rað- eða lotunúmerinu sé til í birgðum. Ef reynt er að bóka skjalalínu á útleið fyrir vöru með raðlotunúmeri sem er ekki í birgðum, þá hindra villuboð bókunina.  
  
Reglur innslátt gagna á síðunni **Vörurakningarlínur** styður einnig tengireglur sem stjórna pöntunarrakningu, áætlanagerð og frátekningu. Nánari upplýsingar eru í [Upplýsingar um hönnun: Vörurakning og áætlanir](design-details-item-tracking-and-planning.md).  
  
## <a name="see-also"></a>Sjá einnig
[Hönnunarupplýsingar: vörurakning](design-details-item-tracking.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
