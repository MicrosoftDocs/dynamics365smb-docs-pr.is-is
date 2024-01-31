---
title: Settu upp greiðsluskilmála
description: Notaðu greiðsluskilmála til að stjórna gjalddögum og greiðsluafslætti.
author: brentholtorf
ms.topic: conceptual
ms.search.form: '4,'
ms.date: 09/05/2023
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Settu upp greiðsluskilmála

Greiðsluskilmálar ákvarða hvernig á að stjórna gjalddögum og greiðsluafslætti. Hægt er að setja upp fjöldann allan af greiðsluskilmálakóðum og nota dagsetningareiknireglur til þess að skilgreina greiðsluskilmálana. Þegar notandi skráir sig fyrst inn [!INCLUDE [prod_short](includes/prod_short.md)] býður sýnifyrirtækið upp á nokkra greiðslumáta sem fyrirtæki nota oft. Þó er hægt að bæta við eins mörgum og þörf krefur.  

Ef þú úthlutar greiðsluskilmálum til viðskiptavina og lánardrottna eru sömu skilmálar alltaf notaðir á sölu- og innkaupaskjölunum sem þú býrð til fyrir þá. Dagsetningar skjala á sölu- og innkaupaskjölum, ekki bókunardagsetningar þeirra, eru notaðar til að reikna út gjalddaga fyrir greiðslur. Hægt er að breyta skilmálunum í sölu- eða innkaupaskjalinu ef þörf krefur, t.d. ef tiltekinn viðskiptavinur á að greiða þér innan 7 daga í stað venjubundinna 14 daga. Að breyta skilmálum skjalsins breytir ekki sjálfgefna greiðsluskilmálanum sem viðskiptavinurinn hefur úthlutað. Sömu greiðsluskilmálar eru í boði fyrir sölu- og innkaupaskjöl.

Þegar þú bókar reikning  [!INCLUDE [prod_short](includes/prod_short.md)] reiknar greiðsluafslátturinn út frá greiðsluskilmálum. Dagsetning greiðsluafsláttar er síðasti dagurinn sem viðskiptavinur getur fengið afslátt. Dagsetningin er einnig reiknuð út þegar þú bókar reikning.  

Á sama hátt, þegar þú birtir kreditnótu, [!INCLUDE [prod_short](includes/prod_short.md)] reiknar greiðsluafslátt út frá greiðsluskilmálum. Það reiknar afslátt af kreditnótum á sama hátt og afsláttur af reikningum. Þegar þú notar kreditreikning á reikning [!INCLUDE [prod_short](includes/prod_short.md)] lækkar afsláttarupphæð reikningsins um afsláttarupphæð kreditreikningsins.  

Ef senda á viðskiptavini áminningar um gjaldfallnar greiðslur þarf að setja upp stig og skilmála innheimtubréfs. Til að læra meira um áminningar skaltu fara í [Setja upp áminningarskilmála og stig](finance-setup-reminders.md).  

## Greiðsluskilmálar settir upp

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Greiðsluskilmálar** og velja síðan viðkomandi tengil.  
2. Fyllið inn reitina eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

Þegar greiðsluskilmálarnir hafa verið settir upp er þeim úthlutað til viðskiptamanna og lánardrottna. Þú getur einnig úthluta greiðsluskilmálum á greiðslumátana þína.  

> [!TIP]
> Í grunnútgáfu af [!INCLUDE [prod_short](includes/prod_short.md)] , eru greiðsluskilmálar með hlutagreiðslu ekki studdir. Þess í stað verður að nota fyrirframgreiðsluaðgerðina. Til að læra meira um fyrirframgreiðslur, farðu í [Setja upp fyrirframgreiðslur](finance-set-up-prepayments.md).
>
> Í sumum löndum/svæðum geturðu *þú* sett upp greiðsluskilmála með hlutagreiðslum. Til að læra hvort landið/svæðið þitt styður þessa möguleika skaltu fara í **Staðbundin virkni** hlutann í efnisyfirlitinu vinstra megin í [Microsoft Learn](about-localization.md) grein.

## Sjá einnig

[Setja upp greiðsluhætti](finance-payment-methods.md)  
[Uppsetning fyrirframgreiðslu](finance-set-up-prepayments.md)  
[Uppsetning Fjármála](finance-setup-finance.md)  
[Skrá nýja viðskiptamenn](sales-how-register-new-customers.md)  
[Skráning nýrra lánardrottna](purchasing-how-register-new-vendors.md)  
[Sala](sales-manage-sales.md)  
[Innkaup](purchasing-manage-purchasing.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
