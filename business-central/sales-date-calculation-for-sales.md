---
title: Dagsetning útreiknings fyrir sölu.
description: Forritið reiknar sjálfkrafa daginn sem verður að panta vöru svo hún sé til í birgðum á tilteknum degi og tilbúið fyrir tiltekt.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/23/2021
ms.author: edupont
ms.openlocfilehash: e195e6658bc495b5d06764114d971c9fc4b7b484
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2022
ms.locfileid: "8522617"
---
# <a name="date-calculation-for-sales"></a>Dagsetning útreiknings fyrir sölu.
[!INCLUDE[prod_short](includes/prod_short.md)] reiknar sjálfkrafa út hvenær hægt er að afhenda vöru á sölupöntunarlínu í fyrsta lagi.

Hafi viðskiptamaðurinn farið fram á tiltekna afgreiðsludagsetningu þá er reiknuð út sú dagsetning sem vörurnar þurfa að vera tilbúnar þannig að afgreiðsla geti farið fram á þeim degi.

Hafi viðskiptamaðurinn ekki farið fram á tiltekna afgreiðsludagsetningu þá er dagsetning sem hægt er að afgreiða vörurnar reiknuð út frá deginum sem vörurnar verða tilbúnar.

## <a name="calculating-a-requested-delivery-date"></a>Reiknar ósk um afhendingardag
Ef tilgreind er umbeðin afgreiðsludagsetning á sölupöntunarlínunni verður þessi dagsetning að upphafspunkti fyrir eftirfarandi útreikninga.

- Umbeðin afgreiðsludagsetning – Flutningstími = Áætluð afhendingardagsetning
- sfhendingardagsetning + afgr.tími vara á útl. úr vöruh. = afh.dags.

Ef varan er tiltæk til tínslu á afhendingardagsetningu þá getur söluferlið haldið áfram. Annars birtist viðvörun um að vara sé uppseld.

> [!Note]
> Ef ferlið þitt er byggt á útreikningi aftur í tímann, t.d. ef þú notar umbeðna afhendingardagsetningu til að fá áætlaða sendingardagsetningu ráðleggjum við þér að þú notir dagsetningarreiknireglur sem eru með fastri tímalengd á borði við „5D“ fyrir fimm daga eða „1V“ fyrir eina viku. Dagsetningarreiknireglur án fastra tímalengda, t.d „NV“ fyrir núverandi viku eða „NM“ fyrir núverandi mánuð, getur leitt til rangra útreikninga á dagsetningum. Nánari upplýsingar um dagsetningarformúlur [fást með því að vinna með dagsetningar og tíma dagatals](ui-enter-date-ranges.md).

## <a name="calculating-the-earliest-possible-delivery-date"></a>Reiknar fyrsta mögulega afgreiðsludag
Ef ekki er tilgreind umbeðin afgreiðsludagsetning á sölupöntunarlínunni, eða ef ekki er hægt að verða við umbeðinni afgreiðsludagsetningu, er reiknuð fyrsta dagsetningin sem vörurnar eru tiltækar. Sú dagsetning er færð inn í reitinn Afhendingardagsetning á línuna og eftirtaldar reiknireglur eru síðan notaðar til að reikna út hvenær áætlað er að senda vörurnar ásamt því á hvaða degi viðskiptamaðurinn fær þær afhentar.

- Afhendingardagsetning + afgr.tími vara á útl. úr vöruh. = Áætluð afhendingardagsetning
- áætluð afhendingardagsetning + flutningstími = áætluð afgreiðsludagsetning


## <a name="see-also"></a>Sjá einnig  
 [Dagsetning útreiknings fyrir kaup.](purchasing-date-calculation-for-purchases.md)   
 [Reikna dagsetningar pöntunarloforða](sales-how-to-calculate-order-promising-dates.md)  
 [Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]