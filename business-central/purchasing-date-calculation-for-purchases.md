---
title: Dagsetning útreiknings fyrir kaup | Microsoft Docs
description: Forritið reiknar sjálfkrafa daginn sem verður að panta vöru svo hún sé til í birgðum á tilteknum degi. Þetta er dagsetningin sem vænta má þess að vara sem pöntuð er á tilteknum degi verði tiltæk til tínslu.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 7b39bcd593489e40d218cf29a3d288dd128cce04
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2020
ms.locfileid: "3192772"
---
# <a name="date-calculation-for-purchases"></a>Dagsetning útreiknings fyrir kaup.
[!INCLUDE[d365fin](includes/d365fin_md.md)] reiknar sjálfkrafa daginn sem verður að panta vöru svo hún sé til í birgðum á tilteknum degi. Þetta er dagsetningin sem vænta má þess að vara sem pöntuð er á tilteknum degi verði tiltæk til tínslu.  

Ef umbeðin móttökudagsetning er tilgreind í innkaupapöntunarhaus verður reiknuð pöntunardagsetning dagsetningin þegar leggja þarf fram pöntun til að vörurnar berist á þeim degi sem beðið var um. Svo er dagsetningin þegar vörurnar verða tilbúnar reiknuð og færð inn í reitinn **Væntanleg móttökudagsetning**.  

Ef ekki er tilgreind ósk um móttökudag notar forritið pöntunardaginn í línunni sem upphafspunkt þegar það reiknar út hvenær búast má við því að fá vörur sendar og þá dagsetningu þegar varan verður tiltæk til afgreiðslu.  

## <a name="calculating-with-a-requested-receipt-date"></a>Reiknað með ósk um móttökudag  
Ef það er ósk um móttökudag á innkaupapöntunarlínunni notar forritið þessa dagsetningu sem upphafspunkt fyrir eftirfarandi útreikninga.  

- Ósk um móttökudag - útreikn. afhendingartíma = pöntunardagur  
- Ósk um móttökudag + afgreiðslutími á vörum inn í vöruhús + öryggisforskot = væntanlegur móttökudagur  

Ef færð hefur verið inn ósk um móttökudag á innkaupapöntunarhausinn er þessi dagsetning afrituð í viðeigandi reit á öllum línunum. Hægt er að breyta þessari dagsetningu á öllum línunum eða fjarlægja dagsetninguna úr línunni.  

> [!Note]
> Ef ferlið þitt er byggt á útreikningi aftur í tímann, t.d. ef þú notar umbeðna móttökudagsetningu til að fá pöntunardagsetninguna, ráðleggjum við þér að þú notir dagsetningarreiknireglur sem eru með fastri tímalengd á borði við „5D“ fyrir fimm daga eða „1V“ fyrir eina viku. Dagsetningarreiknireglur án fastra tímalengda, t.d „NV“ fyrir núverandi viku eða „NM“ fyrir núverandi mánuð, getur leitt til rangra útreikninga á dagsetningum. Frekari upplýsingar er að finna í [Vinna með dagsetningar og tíma í dagatali](ui-enter-date-ranges.md).

## <a name="calculating-without-a-requested-delivery-date"></a>Reiknað án óskar um afhendingardag  
Ef færð er inn innkaupapöntunarlína án óskar um afhendingardag fyllir forritið út í reitinn **dagsetning pöntunar** á línunni með dagsetningunni í reitnum **dagsetning pöntunar** í innkaupapöntunarhausnum. Þetta er annaðhvort dagsetningin sem færð var inn eða vinnudagurinn. Forritið reiknar þá eftirfarandi dagsetningar fyrir innkaupapöntunarlínuna með pöntunardagsetninguna sem upphafspunkt:  

- Pöntunardagur + Útreikningur afgreiðslutíma = Ráðgerð móttökudagsetning.  
- Áætlaður móttökudagur + afgreiðslutími á vörum inn í vöruhús + öryggisforskot = væntanlegur móttökudagur  

Ef pöntunardeginum er breytt á línunni (til dæmis þegar vörurnar eru ekki til hjá lánardrottninum fyrr en daginn eftir) eru viðeigandi dagsetningar á línunni endurreiknaðar sjálfkrafa.  

Ef pöntunardagsetningunni er breytt í hausnum er dagsetningin afrituð inn í reitinn **Dagsetning pöntunar** á öllum línunum og allir viðeigandi dagsetningareitir eru endurreiknaðir.  

## <a name="see-also"></a>Sjá einnig  
 [Dagsetning útreiknings fyrir sölu](sales-date-calculation-for-sales.md)   
 [Reikna dagsetningar pöntunarloforða](sales-how-to-calculate-order-promising-dates.md)  
 [Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
