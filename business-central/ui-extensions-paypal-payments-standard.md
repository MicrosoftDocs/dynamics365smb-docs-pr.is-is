---
title: Notkun PayPal Payments Standard-viðbótarinnar
description: Í þessari grein er því lýst hvernig nota á staðlaða viðbót til að gera viðskiptamönnum kleift að greiða með PayPal.
author: brentholtorf
ms.author: bholtorf
ms.topic: conceptual
ms.search.keywords: 'app, add-in, manifest, customize'
ms.search.form: '1070, 1071, 1073, 1074'
ms.date: 07/09/2024
ms.custom: bap-template
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# <a name="the-paypal-payments-standard-extension"></a>Staðlaður viðbót PayPal greiðslna

PayPal Staðalviðbót við greiðslur getur hjálpað til við að auka þjónustustig viðskiptamanna með því að auðvelda viðskiptavinum að greiða reikningana sína.

Í stað þess að innheimta greiðslur með bankamillifærslu eða kreditkortum geta viðskiptavinir greitt með PayPal reikningi sínum. Þegar sölureikningur er sendur með tölvupósti er PayPal tengja í meginmáli tölvupóstsins og í viðhengdu PDF-skjali. Ef viðskiptamaðurinn velur tengja opnast þjónustusíða fyrir PayPal reikning þeirra og sýnir greiðsluupplýsingarnar. Viðskiptamaður getur síðan greiða reikning og sem hverja aðra PayPal greiðslu.

Staðlaða PayPal greiðsluþjónustan býður upp á eftirfarandi kosti:

* Greiðslur viðskiptamanns berast hraðar á bankareikning þinn.
* Viðskiptamenn hafa úr fleiri leiðum að velja til að greiða reikninga.
* PayPal býður upp á trausta greiðsluþjónustu, og viðskiptamenn kjósa hana oft fram yfir að gefa kreditkortaupplýsingar upp á vefsíðum.
* PayPal býður upp á margar leiðir á meðhöndlun greiðslna, þar á meðal vinnslu kreditkorta, PayPal reikninga og aðrar leiðir.
* Hægt er að bæta PayPal tenglinum sjálfkrafa við söluskjöl eða notandinn getur gert það handvirkt.
* PayPal Stöðluð þjónusta greiðslu felur ekki í sér mánaðarleg gjöld eða uppsetningargjöld.
* Þar sem hún er viðbót getur þú auðveldlega virkjað PayPal greiðslustaðalþjónustu þegar og ef fyrirtækið krefst hennar.  

Nánari upplýsingar um hvernig á að setja upp viðbótina er farið í [Virkja greiðslu viðskiptamanns með PayPal](sales-how-enable-payment-service-extensions.md).

## <a name="register-payments-automatically-for-business-accounts"></a>Skrá greiðslur sjálfkrafa fyrir viðskiptareikninga

[!INCLUDE [prod_short](includes/prod_short.md)] getur skráð greiðslur sjálfkrafa ef þú ert með viðskiptareikning fyrir PayPal Commerce Verkvanginn. Þegar viðskiptamennirnir nota PayPal tengja til að greiða reikning, [!INCLUDE [prod_short](includes/prod_short.md)]  bókar færslurnar og lokar skjalinu.

Til að nota þessa getu er á **síðunni**  Uppsetning greiðsluskráningar [!INCLUDE [prod_short](includes/prod_short.md)] kveikt á **því að Skrá greiðslur víkka sjálfkrafa** og staðfesta reikningana sem þú notar fyrir greiðslurnar. Ef ákveðið er að skrá greiðslur ekki sjálfkrafa er hægt að slökkva á þeim aftur.

> [!TIP]
> Forritarar geta notað sandkassareikninga til að prófa uppsetninguna. Til að gera það skal breyta PayPal veffanginu í **sandbox.paypal.com**. [!INCLUDE [prod_short](includes/prod_short.md)] notar PayPals Augnablik greiðslutilkynningu (IPN) til notify_url.

## <a name="see-also"></a>Sjá einnig .

[Sérstilling [!INCLUDE[prod_short](includes/prod_short.md)] með viðbótum](ui-extensions.md)  
[Uppsetning sölu](sales-setup-sales.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
