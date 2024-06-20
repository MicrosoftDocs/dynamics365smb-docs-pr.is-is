---
title: Setja upp greiðsluskilmála
description: Nota greiðsluskilmála til að stjórna gjalddögum og greiðsluafslætti.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.form: '4,'
ms.date: 06/13/2024
ms.service: dynamics-365-business-central
---
# <a name="set-up-payment-terms"></a>Setja upp greiðsluskilmála

Greiðsluskilmálar ákvarða hvernig á að stjórna gjalddögum og greiðsluafslætti. Hægt er að nota dagsetningarreiknireglur til að skilgreina greiðsluskilmálana. Þegar notandi skráir sig fyrst inn [!INCLUDE [prod_short](includes/prod_short.md)] býður sýnifyrirtækið upp á nokkra greiðslumáta sem fyrirtæki nota oft. Þó er hægt að bæta við eins mörgum og þörf krefur.  

Ef greiðsluskilmálar eru tengdir við viðskiptamenn og lánardrottna eru sömu skilmálar alltaf notaðir í sölu- og innkaupaskjölum sem búin eru til fyrir þá. Dagsetningar fylgiskjala á sölu- og innkaupaskjölum, ekki bókunardagsetningum þeirra, eru notaðar til að reikna gjalddaga fyrir greiðslur. Hægt er að breyta skilmálunum í sölu- eða innkaupaskjalinu ef með þarf. Eigi til dæmis tiltekinn viðskiptamaður að greiða innan sjö daga frekar en sjálfgefna 14 daga. Ef skilmálunum er breytt í skjalinu breytist ekki sjálfgefinn greiðsluskilmálar sem viðskiptamaðurinn hefur sett á. Sömu greiðsluskilmálar eru í boði fyrir sölu- og innkaupaskjöl.

Þegar reikningur er bókaður [!INCLUDE [prod_short](includes/prod_short.md)]  reiknar greiðsluafslátturinn út frá greiðsluskilmálunum. Dagsetning greiðsluafsláttar er síðasti dagurinn sem viðskiptamaðurinn getur fengið afslátt. Dagsetningin er einnig reiknuð við bókun reiknings.  

Á sama hátt reiknar greiðsluafsláttur út frá greiðsluskilmálunum þegar kreditreikningur [!INCLUDE [prod_short](includes/prod_short.md)]  er bókaður. Hann reiknar afsláttinn á kreditreikningum á sama hátt og afsláttur á reikningum. Þegar kreditreikningur er jafnaður við reikning [!INCLUDE [prod_short](includes/prod_short.md)]  minnkar afsláttarupphæð reikningsins um afsláttarupphæð kreditreikningsins.  

Ef senda á viðskiptavini áminningar um gjaldfallnar greiðslur þarf að setja upp stig og skilmála innheimtubréfs. Nánari upplýsingar um áminningar eru í [Setja upp skilmála og stig innheimtubréfa](finance-setup-reminders.md).  

## <a name="to-set-up-payment-terms"></a>Greiðsluskilmálar settir upp

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Greiðsluskilmálar** og velja síðan viðkomandi tengil.  
2. Fyllið inn reitina eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

Þegar greiðsluskilmálarnir hafa verið settir upp er þeim úthlutað til viðskiptamanna og lánardrottna. Þú getur einnig úthluta greiðsluskilmálum á greiðslumátana þína.  

> [!TIP]
> Í grunnútgáfunni af [!INCLUDE [prod_short](includes/prod_short.md)] styðja greiðsluskilmálar ekki hlutagreiðslur. Þess í stað verður að nota fyrirframgreiðsluaðgerðina. Nánari upplýsingar um fyrirframgreiðslur eru í [Setja upp fyrirframgreiðslur](finance-set-up-prepayments.md).
>
> Í sumum löndum/svæðum er hægt *að* setja upp greiðsluskilmála með hlutagreiðslum. Til að komast að **því hvort landið/svæðið styður þennan möguleika er farið í hlutann Staðbundnar aðgerðir** í efnisyfirlitinu vinstra megin [Microsoft Learn](about-localization.md) í greininni.

## <a name="see-also"></a>Sjá einnig .

[Setja upp greiðsluhætti](finance-payment-methods.md)  
[Uppsetning fyrirframgreiðslu](finance-set-up-prepayments.md)  
[Uppsetning Fjármála](finance-setup-finance.md)  
[Skrá nýja viðskiptamenn](sales-how-register-new-customers.md)  
[Skráning nýrra lánardrottna](purchasing-how-register-new-vendors.md)  
[Sala](sales-manage-sales.md)  
[Innkaup](purchasing-manage-purchasing.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
