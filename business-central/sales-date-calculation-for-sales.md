---
title: Útreikningur afhendingardagsetningar fyrir sölu
description: Forritið reiknar sjálfkrafa daginn sem verður að panta vöru svo hún sé til í birgðum á tilteknum degi og tilbúið fyrir tiltekt.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 03/06/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="delivery-date-calculation-for-sales"></a>Útreikningur afhendingardagsetningar fyrir sölu

[!INCLUDE[prod_short](includes/prod_short.md)] reiknar sjálfkrafa út hvenær hægt er að afhenda vöru á sölupöntunarlínu í fyrsta lagi.

* Hafi viðskiptamaðurinn farið fram á tiltekna afgreiðsludagsetningu þá er reiknuð út sú dagsetning sem vörurnar þurfa að vera tilbúnar þannig að afgreiðsla geti farið fram á þeim degi.
* Ef viðskiptamaðurinn biður ekki um tiltekna afgreiðsludagsetningu er dagsetningin þegar hægt er að afhenda vörurnar reiknaðar út. Útreikningurinn hefst frá þeim degi þegar vörurnar eru tilbúnar fyrir tínslu.

## <a name="calculating-a-requested-delivery-date"></a>Reiknar ósk um afhendingardag

Ef tilgreind er umbeðin afgreiðsludagsetning á sölupöntunarlínunni verður þessi dagsetning að upphafspunkti fyrir eftirfarandi útreikninga.

- *Umbeðin afgreiðsludagsetning – Flutningstími = Áætluð afhendingardagsetning*
- *sfhendingardagsetning + afgr.tími vara á útl. úr vöruh. = afh.dags.*

Ef varan er tiltæk til tínslu á afhendingardagsetningu þá getur söluferlið haldið áfram. Annars birtist viðvörun um að vara sé uppseld.

> [!NOTE]
> Ef ferlið þitt er byggt á útreikningi aftur í tímann, t.d. ef þú notar umbeðna afhendingardagsetningu til að fá áætlaða sendingardagsetningu ráðleggjum við þér að þú notir dagsetningarreiknireglur sem eru með fastri tímalengd á borði við „5D“ fyrir fimm daga eða „1V“ fyrir eina viku. Dagsetningarreiknireglur án fastra tímalengda, t.d „NV“ fyrir núverandi viku eða „NM“ fyrir núverandi mánuð, getur leitt til rangra útreikninga á dagsetningum. Frekari upplýsingar eru í [Vinna með dagsetningar og tíma í dagatali](ui-enter-date-ranges.md).

## <a name="calculating-the-earliest-possible-delivery-date"></a>Reiknar fyrsta mögulega afgreiðsludag

Ef ekki er tilgreind umbeðin afgreiðsludagsetning á sölupöntunarlínunni eða ef ekki er hægt að uppfylla umbeðna afgreiðsludagsetningu er fyrsta dagsetningin sem vörurnar eru tiltækar reiknaðar á. Sú dagsetning er síðan færð í reitinn **Afh.dags** í línunni og dagsetningin þegar ætlunin er að senda vörurnar og dagsetninguna þegar afhendar verða viðskiptamanni eru reiknaðar með eftirfarandi reiknireglum.

- *Afhendingardagsetning + afgr.tími vara á útl. úr vöruh. = Áætluð afhendingardagsetning*
- *áætluð afhendingardagsetning + flutningstími = áætluð afgreiðsludagsetning*

## <a name="see-also"></a>Sjá einnig .

[Dagsetning útreiknings fyrir kaup](purchasing-date-calculation-for-purchases.md)  
[Reikna dagsetningar pöntunarloforða](sales-how-to-calculate-order-promising-dates.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
