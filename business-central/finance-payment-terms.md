---
title: Setja upp greiðsluskilmála
description: Í grunnútgáfu Business Central eru greiðsluskilmálar notaðir til að stjórna gjalddögum og greiðsluafslætti.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 10ae5c1932e21b452efd41a1212f1840101a277b
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/08/2021
ms.locfileid: "6437317"
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
> Í sumum löndum *getur* þú sett upp greiðsluskilmála með hlutagreiðslum. Frekari upplýsingar um það hvort þessi valkostur er studdur í þínu landi er að finna í **Staðbundin virkni** hlutanum á yfirlitssvæðinu á vinstri hlið svæðisins [Docs.microsoft.com](about-localization.md).

## <a name="see-also"></a>Sjá einnig

[Setja upp greiðsluhætti](finance-payment-methods.md)  
[Uppsetning fyrirframgreiðslu](finance-set-up-prepayments.md)  
[Uppsetning Fjármála](finance-setup-finance.md)  
[Skrá nýja viðskiptamenn](sales-how-register-new-customers.md)  
[Skráning nýrra lánardrottna](purchasing-how-register-new-vendors.md)  
[Sala](sales-manage-sales.md)  
[Innkaup](purchasing-manage-purchasing.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]