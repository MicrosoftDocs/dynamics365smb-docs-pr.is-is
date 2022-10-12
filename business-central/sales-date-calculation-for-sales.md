---
title: Útreikningur afhendingardagsetningar fyrir sölu
description: Forritið reiknar sjálfkrafa daginn sem verður að panta vöru svo hún sé til í birgðum á tilteknum degi og tilbúið fyrir tiltekt.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 09/22/2022
ms.author: edupont
ms.openlocfilehash: 8cd8f1594a3d2353343e405d2ab616d2ec931c78
ms.sourcegitcommit: 8ad79e0ec6e625796af298f756a142624f514cf3
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/30/2022
ms.locfileid: "9607851"
---
# <a name="delivery-date-calculation-for-sales"></a>Útreikningur afhendingardagsetningar fyrir sölu

[!INCLUDE[prod_short](includes/prod_short.md)] reiknar sjálfkrafa út hvenær hægt er að afhenda vöru á sölupöntunarlínu í fyrsta lagi.

* Hafi viðskiptamaðurinn farið fram á tiltekna afgreiðsludagsetningu þá er reiknuð út sú dagsetning sem vörurnar þurfa að vera tilbúnar þannig að afgreiðsla geti farið fram á þeim degi.
* Ef viðskiptavinurinn óskar ekki eftir tiltekinni afhendingardagsetningu, þá er dagsetningin sem hægt er að afhenda vörurnar reiknaðar út. Útreikningur hefst frá þeim degi sem vörur eru tiltækar til tínslu.

## <a name="calculating-a-requested-delivery-date"></a>Reiknar út umbeðna afgreiðsludagsetningu

Ef tilgreind er umbeðin afgreiðsludagsetning á sölupöntunarlínunni verður þessi dagsetning að upphafspunkti fyrir eftirfarandi útreikninga.

- *umbeðin afgreiðsludagsetning-sendingartími = áætluð sendingardagsetning*
- *Áætluð afhendingardagsetning-vöruhúsaafhending á útleið Afgreiðslutími = Sendingardagur*

Ef varan er tiltæk til tínslu á afhendingardagsetningu þá getur söluferlið haldið áfram. Annars birtist viðvörun um að vara sé uppseld.

> [!NOTE]
> Ef ferlið er byggt á afturvirkum útreikningi, t.d. ef notaður er Umbeðin afhendingardagsetning til að sækja áætlaða afhendingardagsetningu, er mælt með því að nota dagsetningarformúlur með föstum Lengdum eins og "5D" fyrir fimm daga eða "1W" í eina viku. Dagsetningarreiknireglur án fastra tímalengda, t.d „NV“ fyrir núverandi viku eða „NM“ fyrir núverandi mánuð, getur leitt til rangra útreikninga á dagsetningum. Frekari upplýsingar um dagsetningarformúlur í [vinnunni með Dagatalsdagsetningum og tímum](ui-enter-date-ranges.md).

## <a name="calculating-the-earliest-possible-delivery-date"></a>Útreikningur á fyrsta mögulega afhendingardegi

Ef ekki er tilgreind umbeðin afgreiðsludagsetning á sölupöntunarlínunni eða ef ekki er hægt að uppfylla umbeðna afgreiðsludagsetningu er fyrsta dagsetningin sem vörurnar eru reiknaðar til. Dagsetningin er síðan færð inn í **reitinn sendingardagsetning** í línunni og dagsetningin sem ætlunin er að senda vörurnar til og dagsetningin sem þær verða afhentar viðskiptamanni, reiknaðar með eftirfarandi reiknireglum.

- *sendingardagsetning + afgreiðslutími í vöruhúsi Afgreiðslutími = áætluð sendingardagsetning*
- *áætluð sendingardagsetning + sendingartími = áætluð afhendingardagsetning*

## <a name="see-related-microsoft-training"></a>Sjá tengda [Microsoft-þjálfun](/training/modules/promising-sales-order-delivery-dynamics-365-business-central/).

## <a name="see-also"></a>Sjá einnig .

[Dagsetning útreiknings fyrir kaup](purchasing-date-calculation-for-purchases.md)  
[Reikna dagsetningar pöntunarloforða](sales-how-to-calculate-order-promising-dates.md)  
[Vinna með[!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
