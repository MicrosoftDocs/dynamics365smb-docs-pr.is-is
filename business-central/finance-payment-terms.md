---
title: Setja upp greiðsluskilmála
description: Í grunnútgáfu Business Central eru greiðsluskilmálar notaðir til að stjórna gjalddögum og greiðsluafslætti.
author: edupont04
ms.topic: conceptual
ms.search.form: 4
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: e6b242bc3da6a2845c457cfbfcfaf80e6c71d31d
ms.sourcegitcommit: 8ad79e0ec6e625796af298f756a142624f514cf3
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/30/2022
ms.locfileid: "9605111"
---
# <a name="set-up-payment-terms"></a>Setja upp greiðsluskilmála

Greiðsluskilmálar ákvarða hvernig á að stjórna gjalddögum og greiðsluafslætti. Hægt er að setja upp fjöldann allan af greiðsluskilmálakóðum og nota dagsetningareiknireglur til þess að skilgreina greiðsluskilmálana. Þegar notandi skráir sig fyrst inn [!INCLUDE [prod_short](includes/prod_short.md)] býður sýnifyrirtækið upp á nokkra greiðslumáta sem fyrirtæki nota oft. Þó er hægt að bæta við eins mörgum og þörf krefur.  

Þú getur úthlutað greiðsluskilmálum til viðskiptavina og lánardrottna þannig að sömu skilmálar séu alltaf notaðir á sölu- og innkaupskjölunum sem þú býrð til fyrir þá. Hægt er að breyta skilmálunum í sölu- eða innkaupaskjalinu ef þörf krefur, t.d. ef tiltekinn viðskiptavinur á að greiða þér innan 7 daga í stað venjubundinna 14 daga. Þetta breytir ekki sjálfgefnu greiðsluskilmálunum sem er úthlutað á viðskiptavin. Sömu greiðsluskilmálar eru í boði fyrir sölu- og innkaupaskjöl.

Þegar þú bókar svo reikning reiknar [!INCLUDE [prod_short](includes/prod_short.md)] út greiðsluafsláttinn út frá greiðsluskilmálunum. Dagsetning greiðsluafsláttarins, þ.e. síðasta dagsetningin sem viðskiptamaður getur greitt og fengið afslátt af greiðslunni, verður einnig reiknuð út þá.  

Þegar kreditreikningur er bókaður reiknar [!INCLUDE [prod_short](includes/prod_short.md)] út hugsanlegan greiðsluafslátt út frá greiðsluskilmálum á svipaðan hátt. Afslátturinn á kreditreikningum er reiknaður eftir sömu forsendum og staðgreiðsluafslátt á reikningum. Þegar kreditreikningur er jafnaður við reikning er staðgreiðsluafsláttur vegna reikningsins dreginn frá staðgreiðsluafslætti vegna kreditreiknings.  

Ef senda á viðskiptavini áminningar um gjaldfallnar greiðslur þarf að setja upp stig og skilmála innheimtubréfs. Frekari upplýsingar eru í [Setja upp skilmála og stig innheimtubréfa](finance-setup-reminders.md).  

## <a name="to-set-up-payment-terms"></a>Greiðsluskilmálar settir upp

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Greiðsluskilmálar** og velja síðan viðkomandi tengil.  
2. Fyllið inn reitina eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

Þegar greiðsluskilmálarnir hafa verið settir upp er þeim úthlutað til viðskiptamanna og lánardrottna. Þú getur einnig úthluta greiðsluskilmálum á greiðslumátana þína.  

> [!TIP]
> Í grunnútgáfu af [!INCLUDE [prod_short](includes/prod_short.md)] , eru greiðsluskilmálar með hlutagreiðslu ekki studdir. Þess í stað verður að nota fyrirframgreiðsluaðgerðina. Nánari upplýsingar um það eru í [Setja upp fyrirframgreiðslur](finance-set-up-prepayments.md).
>
> Í sumum löndum *getur* þú sett upp greiðsluskilmála með hlutagreiðslum. Frekari upplýsingar um það hvort þessi valkostur er studdur í þínu landi er að finna í **Staðbundin virkni** hlutanum á yfirlitssvæðinu á vinstri hlið svæðisins [Microsoft Learn](about-localization.md) greinarinnar.

## <a name="see-also"></a>Sjá einnig

[Setja upp greiðsluhætti](finance-payment-methods.md)  
[Uppsetning fyrirframgreiðslu](finance-set-up-prepayments.md)  
[Uppsetning Fjármála](finance-setup-finance.md)  
[Skrá nýja viðskiptamenn](sales-how-register-new-customers.md)  
[Skráning nýrra lánardrottna](purchasing-how-register-new-vendors.md)  
[Sala](sales-manage-sales.md)  
[Innkaup](purchasing-manage-purchasing.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]