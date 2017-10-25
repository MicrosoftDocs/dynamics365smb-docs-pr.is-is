---
title: "Hönnunarupplýsingar - vörurakningarlínur gluggi | Microsoft Docs"
description: "Lesa um hvernig skal stjórna flæði rað- og lotunúmera í birgðum."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, inventory, item, tracking, serial number, lot number
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 62070ef4e580a3bd665130c9b017bf164bbe2142
ms.contentlocale: is-is
ms.lasthandoff: 09/22/2017

---
# <a name="design-details-item-tracking-lines-window"></a>Hönnunarupplýsingar: vörurakningarlínur gluggi
Vörurakningarfærslur og frátekningarfærslur eru stofnaðar í frátekningarkerfi og framboð þeirra er reiknað eftir þörfum. Gögnum sem er færð í **Vörurakningarlínur** glugga er stjórnað í tímabundinni útgáfu af töflunni **Rakningarlýsing**. Þegar glugganum er lokað eru virku gögnin skuldbundin töflunni **Frátekningarfærsla** og söguleg gögn skuldbundin töflunni **Rakningarlýsing**. Frekari upplýsingar, sjá: [Hönnunarupplýsingar: Virk móti sögulegum vörurakningarfærslum](design-details-active-versus-historic-item-tracking-entries.md).  
  
Leit úr reitunum **Raðnúmer** og **Lotunúmer** sýna framboð sem byggist á bæði á töflunni **Birgðafærsla** og töflunni **Frátekningarfærsla**, án dagsetningarsíu. Fylki magnreita í haus gluggans **Vörurakningarlínur** birtir með gagnvirkum hætti magn og fjárhæð vörurakningarnúmera sem slegin eru inn í línurnar í glugganum. Magnið verður að samsvara því sem er í fylgiskjalslínunni, og er sýnt með **0** undir **Óskilgreint** reitunum í haus gluggans.  
  
Til að samræma flæði rað- og lotunúmeri gegnum birgðum, eru eftirfarandi reglur til að slá inn gögn í **Vörurakningarnúmer** glugga:  
  
* Fyrir vörurakningarlínur bæði á innleið og útleið er ekki hægt að setja inn raðnúmer með eða án lotunúmers oftar en einu sinni í sama tilviki **Vörurakningarnúmer** gluggans. Ef reynt er að slá inn einhverja samsetningu af rað- eða lotunúmerum sem eru þegar til staðar í glugganum, þá hindra villuboð gagnaskráninguna.  
* Fyrir vörurakningarlínur á innleið er ekki hægt að bóka tengda skjalið ef vara af sama afbrigði og með sama raðnúmer er þegar í birgðum. Ef reynt er að bóka jákvæða línu fyrir birgðavöru með sama afbrigði og raðnúmeri, þá hindra villuboð bókunina. Hins vegar, fyrir bæði vörurakningarlínur á innleið og á útleið á opnum fylgiskjölum, er hægt að hafa sömu samsetningu rað- eða lotunúmera sem tengjast mismunandi upprunaskjalslínum, það er að segja, eru til í mismunandi tilvikum af **Vörurakningarlínur** glugganum þangað til tengda fylgiskjalið er bókað.  
* Ef varan er sett upp fyrir tilgreinda raðnúmerarakningu eða tilgreinda lotunúmerarakningu er ekki hægt að bóka skjalalínu á útleið nema vara með skilgreinda rað- eða lotunúmerinu sé til í birgðum. Ef reynt er að bóka skjalalínu á útleið fyrir vöru með raðlotunúmeri sem er ekki í birgðum, þá hindra villuboð bókunina.  
  
Reglur innslátt gagna í glugganum **Vörurakningarlínur** styður einnig tengireglur sem stjórna pöntunarrakningu, áætlanagerð og frátekningu. Nánari upplýsingar eru í [Upplýsingar um hönnun: Vörurakning og áætlanir](design-details-item-tracking-and-planning.md).  
  
## <a name="see-also"></a>Sjá einnig  
[Hönnunarupplýsingar: vörurakning](design-details-item-tracking.md)
