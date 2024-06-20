---
title: Skilgreina bókunarreglu reikninga fyrir notendur
description: Nota bókunarreglur reikninga til að stjórna því hvort notandi getur bókað sölu- og innkaupareikninga.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.date: 06/12/2024
ms.custom: bap-template
ms.search.forms: '119, 9807,'
ms.service: dynamics-365-business-central
---

# <a name="define-an-invoice-posting-policy-for-users"></a>Skilgreina bókunarreglu reikninga fyrir notendur

Fyrirtæki hafa oft einstök ferli við bókun sölu- og innkaupareikninga og afhendingar. Vinnslur geta til dæmis verið breytilegar frá einum einstaklingi sem bókar allt á innkaupapöntun, á marga starfsmenn. Hægt er að takmarka notendur við bókun reikninga eða krefjast þess að reikningar séu bókaðir ásamt afhendingum eða móttökum.

## <a name="to-specify-a-posting-policy"></a>Bókunarregla tilgreind

Á síðunni **Notandauppsetning**, í **bókunarreglu** sölureiknings og **Innk.reikn. Reitirnir Bókunarregla** reikninga, velja einn af eftirfarandi valkostum:

* **Leyfð** (sjálfgefið) - Halda gildandi hegðun þar sem notandi getur valið bókunarvalkostinn sem **á að nota, t.d. Afhenda**, **Reikningsfæra** og **Afhenda og reikningsfæra**. 
* **Bannað** - Komið í veg fyrir að notandi bóki reikninga. [!INCLUDE [prod_short](includes/prod_short.md)] birtir staðfestingarsvarglugga sem veitir aðeins valkostina **Afhenda** eða **Móttaka** .
* **Áskilið** - Leyfa notandanum að bóka reikninga ásamt móttökum eða afhendingum. [!INCLUDE [prod_short](includes/prod_short.md)] birtir staðfestingarsvarglugga með valkostunum **Afhenda og Reikningsfæra** eða **Móttaka og Reikningsfæra** .

## <a name="effect-on-documents"></a>Áhrif á skjöl

Eftirfarandi tafla lýsir því hvernig bókunarreglur reikninga hafa áhrif á fylgiskjöl.

> [!NOTE]
> Þegar sölu- og innkaupareikningar og kreditreikningar eru bókaðir eru engar bókunarvalkostir. Fylgiskjölin bóka alltaf efnisleg og fjárhagsleg viðskipti saman. Ekki er hægt að bóka reikninga og kreditreikninga að hluta.

|Skjal | Valkostur 1: Leyfa <br>Birtir raðir valkosta| Valkostur 2: Bannað <br>Staðfestingarsvargluggi | Valkostur 3: Áskilið <br>Staðfestingarsvargluggi|
|--|--|--|--|
|Sölupöntun |-Skip <br>-Reikningur <br>- Afhenda og reikningsfæra |Á að bóka afhendinguna? |Á að bóka afhendinguna og reikninginn?|
|Sölureikningur|Engir valkostir| Bókun er óheimil eftir notandagrunni|Á að bóka reikninginn?|
|Sölukreditreikningur|Engir valkostir|Bókun er óheimil eftir notandagrunni|Á að bóka kreditreikninginn?|
|Vöruskilapöntun sölu |-Fá <br>-Reikningur <br>- Móttaka og reikningur |Á að bóka móttökuna? |Á að bóka móttökuna og reikninginn?|
|Birgðatínsla |-Skip <br>- Afhenda og reikningsfæra |Á að bóka afhendinguna? |Á að bóka afhendinguna og reikninginn?|
|Innkaupapöntun |-Fá <br>-Reikningur <br>- Móttaka og reikningur |Á að bóka móttökuna? |Á að bóka móttökuna og reikninginn?|
|Innkaupareikningur|Engir valkostir|Bókun er óheimil eftir notandagrunni|Á að bóka reikninginn?|
|Innkaupakreditreikningur|Engir valkostir|Bókun er óheimil eftir notandagrunni|Á að bóka kreditreikninginn?|
|Vöruskilapantanir innkaupa |-Skip <br>-Reikningur <br>- Afhenda og reikningsfæra |Á að bóka afhendinguna? |Á að bóka afhendinguna og reikninginn?|
|Birgðafrágangur |-Fá <br>- Móttaka og reikningur |Á að bóka móttökuna? |Á að bóka móttökuna og reikninginn?|
|Vöruhúsaafhending |-Skip <br>- Afhenda og reikningsfæra | Á að bóka afhendinguna? |Á að bóka afhendinguna og reikninginn?|

   > [!Note]
   > Stillingin hefur ekki áhrif á bókun færslubókarlína þar sem hægt er að velja **Reikningur** í reitnum **Tegund** fylgiskjals.

## <a name="see-also"></a>Sjá einnig

[Reikningsfæra sölur](sales-how-invoice-sales.md)  
[Skrá innkaup með innkaupareikningum og pöntunum](purchasing-how-record-purchases.md)  
[Innkaupavörur til sölu með því að búa til innkaupareikninga](purchasing-how-purchase-products-sale.md)
[til viðskipta](ui-get-ready-business.md)  
