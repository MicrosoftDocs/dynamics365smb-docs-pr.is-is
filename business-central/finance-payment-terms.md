---
title: Setja upp greiðsluskilmála
description: Nota greiðsluskilmála til að stjórna gjalddögum og staðgreiðsluafslætti.
author: brentholtorf
ms.topic: conceptual
ms.search.form: '4,'
ms.date: 09/05/2023
ms.author: bholtorf
---
# <a name="set-up-payment-terms"></a>Setja upp greiðsluskilmála

Greiðsluskilmálar ákvarða hvernig á að stjórna gjalddögum og greiðsluafslætti. Hægt er að setja upp fjöldann allan af greiðsluskilmálakóðum og nota dagsetningareiknireglur til þess að skilgreina greiðsluskilmálana. Þegar notandi skráir sig fyrst inn [!INCLUDE [prod_short](includes/prod_short.md)] býður sýnifyrirtækið upp á nokkra greiðslumáta sem fyrirtæki nota oft. Þó er hægt að bæta við eins mörgum og þörf krefur.  

Ef Greiðsluskilmálar eru úthlutaðir til viðskiptamanna og lánardrottna eru sömu Skilmálar alltaf notaðir á sölu-og innkaupaskjölunum sem stofnuð eru fyrir þau. Dagsetningar fylgiskjals á sölu-og innkaupaskjölum, ekki bókunardagsetningar þeirra, eru notaðar til að reikna út gjalddaga fyrir greiðslur. Hægt er að breyta skilmálunum í sölu- eða innkaupaskjalinu ef þörf krefur, t.d. ef tiltekinn viðskiptavinur á að greiða þér innan 7 daga í stað venjubundinna 14 daga. Ef skilmálum í skjalinu er breytt er ekki breytt sjálfgefna greiðsluhugtakinu sem viðskiptavinurinn úthlutar. Sömu greiðsluskilmálar eru í boði fyrir sölu- og innkaupaskjöl.

Þegar reikningur er bókaður er  [!INCLUDE [prod_short](includes/prod_short.md)]  greiðsluafsláttur reiknaður á grundvelli greiðsluskilmála. Dagsetning staðgreiðsluafsláttar er Síðasta dagsetningin sem viðskiptavinurinn getur fengið afslátt. Dagsetningin er einnig reiknuð þegar bókaður er reikningur.  

Á sama hátt, þegar kreditreikningur er bókaður,  [!INCLUDE [prod_short](includes/prod_short.md)]  reiknar greiðsluafslátt á grundvelli greiðsluskilmála. Hann reiknar út afsláttinn af kreditreikningum á sama hátt og afslætti á reikningum. Þegar kreditreikningur er sótt á reikning er  [!INCLUDE [prod_short](includes/prod_short.md)]  dregið úr afsláttarupphæð fyrir reikninginn með afsláttarupphæð kreditreikningsins.  

Ef senda á viðskiptavini áminningar um gjaldfallnar greiðslur þarf að setja upp stig og skilmála innheimtubréfs. Frekari upplýsingar um áminningar er að fá með því að  [Setja upp skilmála innheimtubréfs](finance-setup-reminders.md).  

## <a name="to-set-up-payment-terms"></a>Greiðsluskilmálar settir upp

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Greiðsluskilmálar** og velja síðan viðkomandi tengil.  
2. Fyllið inn reitina eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

Þegar greiðsluskilmálarnir hafa verið settir upp er þeim úthlutað til viðskiptamanna og lánardrottna. Þú getur einnig úthluta greiðsluskilmálum á greiðslumátana þína.  

> [!TIP]
> Í grunnútgáfu af [!INCLUDE [prod_short](includes/prod_short.md)] , eru greiðsluskilmálar með hlutagreiðslu ekki studdir. Þess í stað verður að nota fyrirframgreiðsluaðgerðina. Til að fræðast meira um fyrirframgreiðslur er farið í  [Setja upp fyrirframgreiðslur](finance-set-up-prepayments.md).
>
> Í sumum löndum/svæðum  *er hægt*  að setja upp greiðsluskilmála með hlutagreiðslum. Til að fræðast um hvort land/svæði þitt styður þennan möguleika er farið í  **kaflann staðbundin virkni**  í efnisyfirlitinu vinstra megin á  [Microsoft Learn](about-localization.md)  grein.

## <a name="see-also"></a>Sjá einnig

[Setja upp greiðsluhætti](finance-payment-methods.md)  
[Uppsetning fyrirframgreiðslu](finance-set-up-prepayments.md)  
[Uppsetning Fjármála](finance-setup-finance.md)  
[Skrá nýja viðskiptamenn](sales-how-register-new-customers.md)  
[Skráning nýrra lánardrottna](purchasing-how-register-new-vendors.md)  
[Sala](sales-manage-sales.md)  
[Innkaup](purchasing-manage-purchasing.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
