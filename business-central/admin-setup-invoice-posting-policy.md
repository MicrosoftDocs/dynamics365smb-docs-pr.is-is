---
title: Skilgreinið bókunarreglur reiknings fyrir notendur
description: Notaðu reglur reikningabókar til að stjórna því hvort notandi geti bókað sölu-og innkaupareikninga.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.date: 03/09/2023
ms.custom: bap-template
ms.search.forms: '119, 9807,'
---

# Skilgreinið bókunarreglur reiknings fyrir notendur

Fyrirtæki hafa oft einstaka ferla fyrir bókun sölu-og innkaupareikninga og sendinga. Til dæmis geta ferli verið breytileg eftir bókun fólks allt á innkaupapöntun, til margra starfsmanna. Hægt er að takmarka aðgang notenda frá bókun reikninga eða krefjast þess að reikningar séu bókaðir ásamt afhendingum eða innhreyfingum.

## Bókunarregla tilgreind

 **Á síðunni Notandauppsetning**  eru í  **bókunarreglum**  sölureiknings og  **Innk. Reitirnir Bókunarregla**  reikninga, velja einn af eftirfarandi valkostum:

* **Leyfilegt**  (sjálfgefið)-Haltu núverandi hegðun, þar sem notandi getur valið bókunarmöguleika sem nota á, S.s. **Sendist**,  **reikning** og  **Sendist og reikning**. 
* **Bönnuð**  -koma í veg fyrir að notandinn bóki reikninga. Viðskiptamiðað birtist Staðfestingargluggi sem býður aðeins upp á að senda  **eða**  taka  **við**  valkostum.
* **Skylda**  -Leyfa notandanum að bóka reikninga ásamt innhreyfingum eða sendingum. Viðskiptamiðað birtist Staðfestingargluggi með  **skipinu og reikningum**  eða  **móttöku-og reikningakosti** .

## Áhrif á kjör

Eftirfarandi tafla lýsir því hvernig reikningsreglur reikninga hafa áhrif á skjöl.

> [!NOTE]
> Þegar sölu-og innkaupareikningar eru bókaðir og kreditreikningar eru ekki með neina bókunarvalkosti. Skjölin bóka alltaf efnislegar og fjárhagslegar færslur saman. Ekki er hægt að að hluta til að bóka reikninga og kreditreikninga.

|Skjal | Valkostur 1: heimilið <br>Birtir röð valkosta| Valkostur 2: Bannið <br>Svargluggi staðfestingar | Valkostur 3: skyldur <br>Svargluggi staðfestingar|
|--|--|--|--|
|Sölupöntun |-Skip <br>-Reikningur <br>-Senda og reikningsfæra |Á að bóka afhendinguna? |Á að bóka afhendinguna og reikninginn?|
|Sölureikning|Engir Valkostir|Á að bóka reikninginn?|Á að bóka reikninginn?|
|Sölukreditreikningur|Engir Valkostir|Á að bóka kreditreikninginn?|Á að bóka kreditreikninginn?|
|Vöruskilapöntun sölu |-Móttaka <br>-Reikningur <br>-Móttaka og Reikningshald |Á að bóka móttökuna? |Á að bóka móttökuna og reikninginn?|
|Birgðatínslu |-Skip <br>-Senda og reikningsfæra |Á að bóka afhendinguna? |Á að bóka afhendinguna og reikninginn?|
|Innkaupapöntun |-Móttaka <br>-Reikningur <br>-Móttaka og Reikningshald |Á að bóka móttökuna? |Á að bóka móttökuna og reikninginn?|
|Innkaupareikningi|Engir Valkostir|Á að bóka reikninginn?|Á að bóka reikninginn?|
|Innkaupakreditreikningur|Engir Valkostir|Á að bóka kreditreikninginn?|Á að bóka kreditreikninginn?|
|Vöruskilapantanir innkaupa |-Skip <br>-Reikningur <br>-Senda og reikningsfæra |Á að bóka afhendinguna? |Á að bóka afhendinguna og reikninginn?|
|Birgðafrágangur |-Móttaka <br>-Móttaka og Reikningshald |Á að bóka móttökuna? |Á að bóka móttökuna og reikninginn?|
|Vöruhúsaafhending |-Skip <br>-Senda og reikningsfæra | Á að bóka afhendinguna? |Á að bóka afhendinguna og reikninginn?|

   > [!Note]
   > Stillingin hefur ekki áhrif á bókun í færslubókarlínum þar sem hægt er að velja  **reikning**  í  **reitnum Tegund**  fylgiskjals.

## Sjá einnig

[Reikningsfæra sölur](sales-how-invoice-sales.md)  
[Skrá innkaup með innkaupareikningum og pöntunum](purchasing-how-record-purchases.md)  
[Purchase Items for a Sale by Creating Purchase Invoices](purchasing-how-purchase-products-sale.md)
[Getting Ready for Doing Business](ui-get-ready-business.md)  
