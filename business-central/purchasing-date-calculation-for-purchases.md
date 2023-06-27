---
title: Reikna dagsetningar fyrir innkaup
description: Þessi grein lýsir því hvernig hægt er að reikna út dagsetningar fyrir innkaup.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'purchase order, purchase, date, receipt, delivery, lead time'
ms.search.forms: null
ms.date: 10/28/2022
ms.author: bholtorf
---
# <a name="calculate-dates-for-purchases" />Reikna dagsetningar fyrir innkaup

Ef ætlunin er að vera með vörur í birgðum á ákveðinni dagsetingu getur [!INCLUDE[prod_short](includes/prod_short.md)] sjálfkrafa reiknað út dagsetninguna þegar á panta þær. 

Niðurstaðan er dagsetningin þegar hægt er að tína vörurnar sem voru pantaðar.  

Ef umbeðin móttökudagsetning er tilgreind í innkaupapöntunarlínu þá er reiknuð pöntunardagsetning dagurinn sem pöntunin er gerð. Dagsetningin þegar vörurnar verða tiltækar fyrir tínslu birtist í reitnum **Væntanleg móttökudagsetning**.  

Ef ekki umbeðin móttökudagsetning er ekki tilgreind byggir dagsetningin sem búist er við að taka á móti vörunum á pöntunardeginum í línunni. 

Móttökudagsetningin er einnig dagsetningin þegar vörurnar verða í boði fyrir tínslu.  

> [!TIP]
> Margir dagsetningarreitirnir sem minnst er á í þessari grein eru sjálfgefið faldir í innkaupapöntunarlínum. Ef reitur er ekki í boði er hægt að bæta honum við með því að sérsníða síðuna. Frekari upplýsingar eru í [Sérstilling verksvæðis](ui-personalization-user.md).

## <a name="calculating-with-a-requested-receipt-date" />Reiknað með ósk um móttökudag

Ef umbeðin móttökudagsetning er til staðar í innkaupapöntunarlínunni er sú dagsetning grunnurinn fyrir eftirfarandi útreikninga:  

- Ósk um móttökudag - útreikn. afhendingartíma = pöntunardagur  
- Ósk um móttökudag + afgreiðslutími á vörum inn í vöruhús + öryggisforskot = væntanlegur móttökudagur  

Ef umbeðin móttökudagsetning er tilgreind í innkaupapöntunarlínu er þeirri dagsetningu úthlutað á nýjar línur þegar þær eru stofnaðar. Hægt er að breyta eða fjarlægja dagsetninguna úr línunum.  

> [!NOTE]
> Ef ferlið þitt er byggt á útreikningi aftur í tímann, t.d. ef þú notar umbeðna móttökudagsetningu til að fá pöntunardagsetninguna, ráðleggjum við þér að þú notir dagsetningarreiknireglur sem eru með fastri tímalengd á borði við „5D“ fyrir fimm daga eða „1V“ fyrir eina viku. Dagsetningarreiknireglur án fastra tímalengda, t.d „NV“ fyrir núverandi viku eða „NM“ fyrir núverandi mánuð, getur leitt til rangra útreikninga á dagsetningum. Frekari upplýsingar um dagsetningarformúlur er að finna í [Vinna með dagsetningar og tíma í dagatali](ui-enter-date-ranges.md).

## <a name="calculating-without-a-requested-receipt-date" />Útreikningur án umbeðinnar móttökudagsetningar

Ef færð er inn innkaupapöntunarlína án umbeðinnar móttökudagsetningar sýnir reiturinn **Dagsetning pöntunar** í línunni dagsetninguna í reitnum **Dagsetning pöntunar** í innkaupapöntunarhausnum. Þetta er annaðhvort dagsetningin sem færð var inn eða vinnudagsetningin. Forritið reiknar þá dagsetningar fyrir innkaupapöntunarlínuna með pöntunardagsetninguna sem upphafspunkt á eftirfarandi hátt:  

- Pöntunardagur + Útreikningur afgreiðslutíma = Ráðgerð móttökudagsetning.  
- Áætlaður móttökudagur + afgreiðslutími á vörum inn í vöruhús + öryggisforskot = væntanlegur móttökudagur  

Ef pöntunardagsetningunni er breytt í línunni endurreiknar [!INCLUDE[prod_short](includes/prod_short.md)] hinar dagsetningarnar.  

## <a name="default-values-for-lead-time-calculation" />Sjálfgefin gildi fyrir útreikning afhendingartíma

[!INCLUDE[prod_short](includes/prod_short.md)] notar dagsetningarformúluna í reitnum **Útreikningur afhendingartíma** í innkaupapöntunarlínunni til að reikna út pöntunina og væntanlegar móttökudagsetningar.  

Hægt er að tilgreina dagsetningarformúlu í línum handvirkt. Annars mun [!INCLUDE[prod_short](includes/prod_short.md)] nota formúlur sem eru skilgreindar á eftirfarandi síðum í þessari forgangsröð:

1. Birgðalisti lánardrottna
2. Birgðaspjald
3. Birgðahaldseiningarspjald
4. Lánardrottnaspjald

## <a name="see-related-microsoft-training" />Sjá tengda [Microsoft þjálfun](/training/modules/estimate-receipt-dates-dynamics-365-business-central/)

## <a name="see-also" />Sjá einnig .

[Dagsetning útreiknings fyrir sölu.](sales-date-calculation-for-sales.md)  
[Reikna dagsetningar pöntunarloforða](sales-how-to-calculate-order-promising-dates.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
