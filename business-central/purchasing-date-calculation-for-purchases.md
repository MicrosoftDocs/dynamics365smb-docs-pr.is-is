---
title: Reikna dagsetningar fyrir innkaup
description: Í greininni er lýst hvernig hægt er að reikna út dagsetningar innkaupa.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: purchase order, purchase, date, receipt, delivery, lead time
ms.search.forms: ''
ms.date: 02/06/2022
ms.author: bholtorf
ms.openlocfilehash: 6a3d7244beef57a1b5a82b881ec193316fe968fe
ms.sourcegitcommit: 7a6efcbae293c024ca4f6622c82886decf86c176
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/02/2022
ms.locfileid: "8841867"
---
# <a name="calculate-dates-for-purchases"></a>Reikna dagsetningar fyrir innkaup

Ef óskað er eftir að hafa vörur í birgðum á ákveðnum degi, [!INCLUDE[prod_short](includes/prod_short.md)] má reikna dagsetninguna þegar þær eiga að vera pöntunar. 

Útkoman er dagsetningin þegar hægt er að tína vörurnar sem þú pantaðir.  

Ef Umbeðin móttökudagsetning er tilgreind á innkaupapöntunarlínu er reiknaða pöntunardagsetningin dagsetningin þegar pöntunin á að vera gerð. Dagsetningin sem vörurnar verða tiltækar fyrir tiltekt birtar í **reitnum Áætlaður móttökudagur**.  

Ef ekki er tilgreind móttökudagsetning sem búist er við að berist með vörunum er byggt á pöntunardagsetningu í línunni. 

Móttökudagsetning er einnig dagsetningin þegar vörurnar verða tiltækar til tínslu.  

> [!TIP]
> Sjálfgefið er að margir dagsetningarreitir þessa greinis sem eru faldir í innkaupapöntunarlínum. Ef svæði er ekki tiltækt er hægt að bæta því við með því að sérsníða síðuna. Frekari upplýsingar eru í [Sérstilling verksvæðis](ui-personalization-user.md).

## <a name="calculating-with-a-requested-receipt-date"></a>Reiknað með ósk um móttökudag

Ef það er Umbeðin móttökudagsetning á innkaupapöntunarlínunni þá er dagsetningin grunnurinn að eftirfarandi útreikningum:  

- Ósk um móttökudag - útreikn. afhendingartíma = pöntunardagur  
- Ósk um móttökudag + afgreiðslutími á vörum inn í vöruhús + öryggisforskot = væntanlegur móttökudagur  

Ef Umbeðin móttökudagsetning er tilgreind á innkaupapöntunarlínu er dagsetningin tengd við nýjar línur um leið og þær eru stofnaðar. Hægt er að breyta eða fjarlægja dagsetninguna í línunum.  

> [!NOTE]
> Ef ferlið þitt er byggt á útreikningi aftur í tímann, t.d. ef þú notar umbeðna móttökudagsetningu til að fá pöntunardagsetninguna, ráðleggjum við þér að þú notir dagsetningarreiknireglur sem eru með fastri tímalengd á borði við „5D“ fyrir fimm daga eða „1V“ fyrir eina viku. Dagsetningarreiknireglur án fastra tímalengda, t.d „NV“ fyrir núverandi viku eða „NM“ fyrir núverandi mánuð, getur leitt til rangra útreikninga á dagsetningum. Nánari upplýsingar um dagsetningarformúlur [fást með því að vinna með dagsetningar og tíma dagatals](ui-enter-date-ranges.md).

## <a name="calculating-without-a-requested-delivery-date"></a>Reiknað án óskar um afhendingardag

Ef innkaupapöntunarlína er færð inn án umbeðinnar afhendingardagsetningar er reiturinn Pöntunardagsetning **í línunni,** dagsetningin í **reitnum Pöntunardagsetning** í innkaupapöntunarhausnum. Þessi dagsetning er annað hvort dagsetningin sem færð var inn eða vinnudagsetningin. Dagsetningarnar eru reiknaðar út fyrir innkaupapöntunarlínuna með pöntunardagsetninguna sem byrjunarreit, sem hér segir:  

- Pöntunardagur + Útreikningur afgreiðslutíma = Ráðgerð móttökudagsetning.  
- Áætlaður móttökudagur + afgreiðslutími á vörum inn í vöruhús + öryggisforskot = væntanlegur móttökudagur  

Ef pöntunardagsetningunni er breytt í línunni, [!INCLUDE[prod_short](includes/prod_short.md)] endurreiknar aðrar dagsetningar.  

## <a name="default-values-for-lead-time-calculation"></a>Sjálfgefin gildi fyrir útreikning afhendingartíma

[!INCLUDE[prod_short](includes/prod_short.md)] notar dagsetningarreikniregluna í **reitnum Útreikningur** afhendingartíma í innkaupapöntunarlínunni til að reikna út pöntunar-og væntar móttökudagsetningar.  

Hægt er að tilgreina handvirkt dagsetningarreikniregluna á línum. Að öðrum kosti skal [!INCLUDE[prod_short](includes/prod_short.md)] nota reiknireglur sem skilgreindar eru á eftirfarandi síðum í forgangsröð:

1. Birgðalisti lánardrottna
2. Birgðaspjald
3. Birgðahaldseiningarspjald
4. Lánardrottnaspjald

## <a name="see-also"></a>Sjá einnig

[Dagsetning útreiknings fyrir sölu](sales-date-calculation-for-sales.md)   
[Reikna dagsetningar pöntunarloforða](sales-how-to-calculate-order-promising-dates.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]