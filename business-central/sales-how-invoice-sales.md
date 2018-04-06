---
title: "Stofna sölureikning eða sölupöntun | Microsoft Docs"
description: "Lýsir því hvernig skal búa til söluvíxil, eða sölureikning eða sölupöntun, til að skrá samkomulag við viðskiptamann um að selja tilteknar vörur með tilteknum skilmálum."
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bill, sale, invoice, order
ms.date: 03/12/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: e4cf02913056fd0b20bb35fd407a82b2ec8b1599
ms.contentlocale: is-is
ms.lasthandoff: 03/22/2018

---
# <a name="invoice-sales"></a>Reikningsfæra sölur
Búinn er til sölureikningur eða sölupöntun til að skrá samkomulag við viðskiptamann um að selja tilteknar vörur með tilteknum afhendingar- og greiðsluskilmálum.  

Til eru nokkrar aðstæður þar sem verður að nota sölupöntun í stað sölureikningi:  

* Ef þarf að senda aðeins hluti af pöntunarmagni á, til dæmis vegna þess að allt magnið er ekki tiltækt.  
* Ef þú selur vörur sem lánardrottni sendir beint til viðskiptamanns, heitir bein afhending. Frekari upplýsingar eru í [Beinar sendingar](sales-how-drop-shipment.md).  

Frá öllum öðrum sjónarhornum séð virka sölupantanir á sama hátt og sölureikningar. Frekari upplýsingar eru í [Selja vörur](sales-how-sell-products.md).

Hægt er að semja við viðskiptamanninn með því að gera fyrst sölutilboð, sem hægt er að breyta í sölureikning þegar samkomulag hefur náðst um söluna. Frekari upplýsingar eru í [Tilboðsgerð](sales-how-make-offers.md).

Ef viðskiptamaðurinn ákveður að kaupa, bókar þú sölureikninginn til að stofna tengdar magn og virðisfærslur. Við bókun sölureiknings, er einnig hægt að senda skjalið í tölvupósti sem PDF viðhengi. Hægt er að láta meginmálslínur tölvupósts vera útfyllt fyrirfram með samantekt á reikningnum og greiðsluupplýsingum, eins og tengli í PayPal. Frekari upplýsingar eru í [Senda skjöl í tölvupósti](ui-how-send-documents-email.md).

Í viðskiptaumhverfi þar sem viðskiptamaðurinn verður að greiða áður en vörur eru afhentar, til dæmis í smásölu, verður að bíða eftir greiðslukvittun fyrir vörunum áður en þær eru afhentar. Í flestum tilfellum er valið að vinna  greiðslur á innleið nokkrum vikum eftir afhendingu með því að jafna greiðslurnar við viðkomandi bókaða, ógreidda sölureikninga. Frekari upplýsingar eru í [afstemma greiðslur með því að nota sjálfvirk jöfnun](receivables-how-reconcile-payments-auto-application.md)

Í viðskiptaumhverfi þar sem viðskiptavinurinn greiðir strax, til dæmis með reiðufé, PayPal eða kreditkorti, er hægt að velja viðeigandi aðferð í reitnum **Kóði greiðslumáta** á sölureikningnum. Greiðsla er síðan skráð strax á bókuðum reikningi. Fyrir greiðsluþjónustur þarf einnig að fylla inn í reitinn **Greiðsluþjónusta**. Nánari upplýsingar eru í [Virkja greiðsluur viðskiptamanna um greiðsluþjónustur](sales-how-enable-payment-service-extensions.md).

Þú getur jafnvel búið til beingreidda reikninga fyrir óskráða viðskiptavini með því að fyrst setja upp „viðskiptamannaspjald fyrir reiðufé" sem þú bendir á í sölureikningnum. Frekari upplýsingar eru í [Setja upp viðskiptamenn með reiðufé](finance-how-to-set-up-cash-customers.md).  

Auðvelt er að leiðrétta eða afturkalla bókaðann sölureikning áður en hann er greiddur. Þetta er til dæmis gagnlegt þegar leiðrétta á innsláttarvillu eða þegar viðskiptamaðurinn biður um breytingu snemma í pöntunarferlinu. Frekari upplýsingar eru í [Ógreiddir sölureikningar leiðréttir eða afturkallaðir](sales-how-correct-cancel-sales-invoice.md). Ef bókaður sölureikningur er greiddur, verður að búa til sölukreditreikning til að afturkalla söluna. Fyrir frekar upplýsingar, sjá [Meðhöndlun söluvöruskila eða afturkallana](sales-how-process-sales-returns-cancellations.md).

Vörurnar geta bæði verið vörur í birgðaskrá og þjónustu, gefið til kynna sem **Birgðir** og **Þjónusta** tegundir á birgðaspjaldinu. Sölureikningaferlið er það sama fyrir báðar vörutegundir. Nánari upplýsingar eru í [Skrá nýjar vörur](inventory-how-register-new-items.md).

Hægt er að fylla út viðskiptamannsreitina á sölureikningnum með tveimur leiðum, eftir því hvort viðskiptamaðurinn hefur þegar verið skráður. Sjá lið 2 og 3 í eftirfarandi ferli.

## <a name="to-create-a-sales-invoice"></a>Sölureikningar búnir til:
1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Innkaupareikningar** og velja svo viðeigandi tengil.  
2. Í reitnum **Viðskiptamaður** er fært inn nafn núverandi viðskiptamanns.

   Aðrir reitir í glugganum **Sölureikningur** eru nú fylltir út með stöðluðum upplýsingum um valinn viðskiptamann. Ef viðskiptamaðurinn er ekki skráður, fylgið eftirfarandi skrefum:
3. Í reitnum **Viðskiptamaður** er fært inn nafn nýs viðskiptamanns.
4. Í svarglugganum um að skrá nýja viðskiptavininn, veljið hnappinn **Já**.
5. Í glugganum **Velja sniðmát fyrir nýjan viðskiptamann**, skal velja sniðmát til að byggja nýja viðskiptamannaspjaldið á og veljið hnappinn **Í lagi**.
6. Nýtt viðskiptamannaspjald sýnir upplýsingarnar á valda viðskiptamannasniðmátinu. Eftirstandandi reitir eru fylltir út. Frekari upplýsingar eru í [Skrá nýja viðskiptamenn](sales-how-register-new-customers.md).  
7. Þegar lokið hefur verið við viðskiptamannaspjaldið skal velja hnappinn **Í lagi** til að fara aftur í gluggann **Sölureikningur**.

   Margir reitir í sölureikningahaus eru ný fullir af upplýsingar sem tilgreindar voru á nýja viðskiptamannaspjaldi.  
8. Fylltu í eftirstandandi reikningana í glugganum **sölureikningur** eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

Nú er hægt að fylla út í reikningslínur fyrir vörur sem selt er viðskiptamanni eða einhverri færslu við þann viðskiptamann sem á að skrá í reikning í Fjárhag.   

Ef endurteknar sölulínur hafa verið settar upp fyrir viðskiptamanninn, svo sem mánaðarlegar endurnýjunarpantanir, er hægt að færa línuna inn í pöntunina með því að velja aðgerðina **Endurteknar sölulínur**.  
9. Á **Línur** Flýtiflipanum í **Tegund** reitnum, veldu hvaða tegund framleiðsluflokks, kostnaðarauka eða færslu þú munt bókað fyrir viðskiptamanninn með sölulínunni.
10. Í reitnum **númer** Reitnum er valin færsla til að bóka samkvæmt gildinu í reitnum **Tegund** reit.

 Þú skilur **nr.** reitinn eftir auðan í eftirfarandi tilvikum: – Ef línan er fyrir athugasemd. Rita athugasemdina í **Lýsing** reitinn.
 – Ef línan er fyrir utanbirgðavöru. Veljið **Velja utanbirgðavörur** aðgerð. Frekari upplýsingar eru í [Vinna með utanbirgðavörur](inventory-how-work-nonstock-items.md).

11. Í reitnum **Magn** er fært inn hversu margar einingar vöru, kostnaðarauka eða færslu sem línan skráir fyrir viðskiptamanninn.  

    > [!NOTE]  
    >   Ef varan er af gerðinni **Þjónusta** eða reiturinn **Gerð** innniheldur **Forið** þá er magnið tíaeining á borð við klukkustundir, eins og táknað er í **Mælieiningarkóði** reitnum á línunni.  

    Gildið í reitnum **Línuupphæð** er reiknaður sem *Einingarverð* x *Magn*.  

    Verð- og línuupphæðirnar eru sýndar með eða án VSK, en það fer eftir því hvað var valið í reitnum **verð með skatti** á viðskiptamannaspjaldinu.  
12. Í reitnum **Línuafsláttur %**, færið inn prósentutölu ef veita á afslátt af vörunni. Gildið í reitnum **Línuupphæð** er uppfært til samræmis.  

    Ef sérstakt vöruverð hefur verið sett upp á flýtiflipanum **Afslættir söluverðs og sölulínu** á viðskiptamanns- eða vöruspjaldinu, uppfærist verðið og upphæðin á tilboðslínunni sjálfvirkt ef umsamin verðviðmið hafa náðst. Nánari upplýsingar eru í [Skrá söluverð, afslátt og greiðslusamkomulag](sales-how-record-sales-price-discount-payment-agreements.md).  
13. Endurtakið skref 9 til 12 fyrir hverja vöru eða gjald sem selja á viðskiptamanninum.  

    Samtölur fyrir neðan línurnar eru sjálfkrafa reiknaðar þegar þú stofna eða breyta línur.  
14. Í reitnum **afsláttarupphæð reiknings** færið inn upphæð sem draga á frá gildinu sem sýnt er í reitnum **Heildarupphæð með skatti**.

    Ef reikningsafslættir hafa verið settir upp fyrir viðskiptamanninn, er tilgreint prósentugildi sjálfvirkt fært inn í reitinn **reikningsafsláttur %** ef viðmiðum hefur verið mætt og upphæðin færð inn í reitinn **afsláttarupphæð án skatts**. Nánari upplýsingar eru í [Skrá söluverð, afslátt og greiðslusamkomulag](sales-how-record-sales-price-discount-payment-agreements.md).  
15. Þegar sölureikningslínunum er lokið, skal velja **bóka og senda** aðgerðina.  

**Bóka og Senda á staðfestingu** svarglugginn birtir þá aðferð sem viðskiptamaðurinn vill nota til að taka á móti fylgiskjölum. Hægt er að breyta sendingaraðferð með því að velja uppflettihnappinn fyrir reitinn **senda skjal** Frekari upplýsingar er að finna á [Setja upp sendisnið skjala](sales-how-setup-document-send-profiles.md).

Tengdar vöru- og viðskiptamannafærslur eru nú búnar til í kerfinu og á sölureikningnum er frálag sem PDF fylgiskjal. Sölureikningurinn er fjarlægður af lista sölureikninga og skipt út fyrir nýtt fylgiskjal á lista bókaðra sölureikninga.

## <a name="see-also"></a>Sjá einnig
[Sala](sales-manage-sales.md)  
[Uppsetning sölu](sales-setup-sales.md)  
[Birgðir](inventory-manage-inventory.md)  
[Senda skjöl í tölvupósti](ui-how-send-documents-email.md)  
[Magnreikningsfærsla frá Microsoft Bookings í Business Central ](finance-bookings.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

