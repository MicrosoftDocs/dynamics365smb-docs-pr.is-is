---
title: Reikningsfæra sölur
description: Lýsir því hvernig skal búa til söluvíxil, eða sölureikning eða sölupöntun, til að skrá samkomulag við viðskiptamann um að selja tilteknar vörur með tilteknum skilmálum.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bill, sale, invoice, order
ms.search.form: 42, 43, 48, 9301, 9305
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 125d28f1621e23f14cda9ce57a935a7da71e43cb
ms.sourcegitcommit: a9e2aaee735870af566db68532cfa697347d68e0
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 11/04/2021
ms.locfileid: "7752469"
---
# <a name="invoice-sales"></a>Reikningsfæra sölur

Búinn er til sölureikningur eða sölupöntun til að skrá samkomulag við viðskiptamann um að selja tilteknar vörur með tilteknum afhendingar- og greiðsluskilmálum.  

Til eru nokkrar aðstæður þar sem verður að nota sölupöntun í stað sölureikningi:  

* Ef þarf að senda aðeins hluti af pöntunarmagni á, til dæmis vegna þess að allt magnið er ekki tiltækt.  
* Ef vörur eru sendar eftir bókun samsvarandi sölureikninga.
* Ef þú selur vörur sem lánardrottni sendir beint til viðskiptamanns, heitir bein afhending. Frekari upplýsingar eru í [Beinar sendingar](sales-how-drop-shipment.md).  

Frá öllum öðrum sjónarhornum séð virka sölupantanir á sama hátt og sölureikningar. Frekari upplýsingar eru í [Selja vörur](sales-how-sell-products.md).

Hægt er að semja við viðskiptamanninn með því að gera fyrst sölutilboð, sem hægt er að breyta í sölureikning þegar samkomulag hefur náðst um söluna. Frekari upplýsingar er að finna í [Búa til sölutilboð](sales-how-make-offers.md).

## <a name="create-sales-invoices"></a>Stofna sölureikninga

Ef viðskiptamaðurinn ákveður að kaupa, bókar þú sölureikninginn til að stofna tengdar magn og virðisfærslur. Við bókun sölureiknings, er einnig hægt að senda skjalið í tölvupósti sem PDF viðhengi. Hægt er að láta meginmálslínur tölvupósts vera útfyllt fyrirfram með samantekt á reikningnum og greiðsluupplýsingum, eins og tengli í PayPal. Frekari upplýsingar eru í [Senda skjöl í tölvupósti](ui-how-send-documents-email.md). Þegar viðskiptamaðurinn greiðir síðan reikninginn getur þú skráð þessi greiðslu á mismunandi vegu, allt eftir stærð og valinn vinnuflæði fyrirtækisins. Fyrir frekari upplýsingar, sjá [Skrá greiðslur](#registering-payments) hlutann.  

Birgðaspjöld geta verið af gerðinni **Birgðir**, **Þjónusta** og **Ekki birgðir** til að tilgreina hvort vara er raunbirgðaeining, launatímaeining eða efnisleg eining sem ekki er geymd í birgðum. Nánari upplýsingar eru í [Skrá nýjar vörur](inventory-how-register-new-items.md). Sölureikningsferlið er það sama fyrir allar þrjár vörutegundirnar.

Hægt er að fylla út viðskiptamannsreitina á sölureikningnum með tveimur leiðum, eftir því hvort viðskiptamaðurinn hefur þegar verið skráður. Sjá skref 2 í eftirfarandi ferli.

### <a name="to-create-a-sales-invoice"></a>Sölureikningar búnir til:

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Sölureikningar** og velja síðan viðkomandi tengil.  
2. Í reitnum **Viðskiptamaður** er fært inn nafn núverandi viðskiptamanns.

   Aðrir reitir á síðunni **Sölureikningur** innihalda nú staðlaðar upplýsingar um valinn viðskiptamann. Ef viðskiptamaðurinn er ekki skráður, fylgið eftirfarandi skrefum:

    1. Í reitnum **Viðskiptamaður** er fært inn nafn nýs viðskiptamanns.
    2. Í svarglugganum um að skrá nýja viðskiptavininn, veljið hnappinn **Já**.
    3. Á síðunni **Velja sniðmát fyrir nýjan viðskiptamann**, skal velja sniðmát til að byggja nýja viðskiptamannaspjaldið á og veljið hnappinn **Í lagi**.
    4. Nýtt viðskiptamannaspjald sýnir upplýsingarnar á valda viðskiptamannasniðmátinu. Eftirstandandi reitir eru fylltir út. Frekari upplýsingar eru í [Skrá nýja viðskiptamenn](sales-how-register-new-customers.md).  
    5. Þegar lokið hefur verið við viðskiptamannaspjaldið skal velja hnappinn **Í lagi** til að fara aftur á síðuna **Sölureikningur**.

   Margir reitir í sölureikningahaus eru ný fullir af upplýsingar sem tilgreindar voru á nýja viðskiptamannaspjaldi.  
3. Fylltu í eftirstandandi reikningana á síðunni **sölureikningur** eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
    > Ef þú leyfir viðskiptavininum að greiða strax, til dæmis með reiðufé eða með PayPal, þá skaltu fylla út reitinn **Kóði greiðslumáta**. Greiðslan er síðan skráð um leið og þú bókar sölureikninginn. Ef þú velur REIÐUFÉ, þá er greiðslan skráð á tilteknum mótreikningi.

    Nú er hægt að fylla út í reikningslínur fyrir vörur sem selt er viðskiptamanni eða einhverri færslu við þann viðskiptamann sem á að skrá í reikning í Fjárhag.  

    Ef endurteknar sölulínur hafa verið settar upp fyrir viðskiptamanninn, svo sem mánaðarlegar endurnýjunarpantanir, er hægt að færa línuna inn í pöntunina með því að velja aðgerðina **Endurteknar sölulínur**.  
4. Á **Línur** Flýtiflipanum í **Tegund** reitnum, veldu hvaða tegund framleiðsluflokks, kostnaðarauka eða færslu þú munt bókað fyrir viðskiptamanninn með sölulínunni.
5. Í reitnum **númer** Reitnum er valin færsla til að bóka samkvæmt gildinu í reitnum **Tegund** reit.

    Þú skilur **nr.** reitur tómur í eftirfarandi tilfellum:

    * Ef línan er ætluð athugasemd. Rita athugasemdina í **Lýsing** reitinn.
    * Ef línan er fyrir vörulistavöru. Velja **Velja vörulistaatriði** aðgerð. Nánari upplýsingar er að finna í [Vinna með vörulistaatriði](inventory-how-work-nonstock-items.md).

6. Í reitnum **Magn** er fært inn hversu margar einingar vöru, kostnaðarauka eða færslu sem línan skráir fyrir viðskiptamanninn.  

    > [!NOTE]  
    > Ef varan er af gerðinni **Þjónusta** eða reiturinn **Gerð** inniheldur **Forðann** þá er magnið tíaeining á borð við klukkustundir, eins og táknað er í **Mælieiningarkóði** reitnum á línunni. Frekari upplýsingar eru í [Setja upp mælieiningu vara](inventory-how-setup-units-of-measure.md)

    Gildið í reitnum **Línuupphæð** er reiknaður sem *Einingarverð* x *Magn*.  

    Verð- og línuupphæðirnar eru sýndar með eða án VSK, en það fer eftir því hvað var valið í reitnum **verð með skatti** á viðskiptamannaspjaldinu.  
7. Í reitnum **Línuafsláttur %**, færið inn prósentutölu ef veita á afslátt af vörunni. Gildið í reitnum **Línuupphæð** er uppfært til samræmis.  

    Ef sérstakt vöruverð hefur verið sett upp á flýtiflipanum **Afslættir söluverðs og sölulínu** á viðskiptamanns- eða vöruspjaldinu, uppfærist verðið og upphæðin á tilboðslínunni sjálfvirkt ef umsamin verðviðmið hafa náðst. Nánari upplýsingar eru í [Skrá söluverð, afslátt og greiðslusamkomulag](sales-how-record-sales-price-discount-payment-agreements.md).  
8. Endurtakið skref 9 til 12 fyrir hverja vöru eða gjald sem á reikningsfæra viðskiptavininn fyrir.  

    Samtölureitirnir undir línunum uppfærast sjálfkrafa eftir því sem þú stofnar eða breytir línum til að sýna upphæðir sem verða bókaðar í fjárhagnum.

    > [!NOTE]
    > Í örfáum tilfellum kunna bókaðar upphæðir að sýna aðra upphæðir en þær sem sýndar eru í samtölureitunum. Venjulega gerist það vegna sléttunarútreiknings í tengslum við virðisaukaskatt.<br /><br />Til að kanna upphæðirnar sem koma til með að vera bókaðar er hægt að nota síðuna **Tölfræðilegar upplýsingar** sem tekur sléttunarútreikninga til greina. Einnig, ef þú velur aðgerðina **Gefa út**, verða samtölureitirnir uppfærðir til að hafa sléttunarútreikninga með.
9. Í reitnum **afsláttarupphæð reiknings** færið inn upphæð sem draga á frá gildinu sem sýnt er í reitnum **Heildarupphæð með skatti**.

    Ef reikningsafslættir hafa verið settir upp fyrir viðskiptamanninn, er tilgreint prósentugildi sjálfvirkt fært inn í reitinn **reikningsafsláttur %** ef viðmiðum hefur verið mætt og upphæðin færð inn í reitinn **afsláttarupphæð án skatts**. Nánari upplýsingar eru í [Skrá söluverð, afslátt og greiðslusamkomulag](sales-how-record-sales-price-discount-payment-agreements.md).  
10. Þegar sölureikningslínunum er lokið, skal velja **bóka og senda** aðgerðina.  

**Bóka og Senda á staðfestingu** svarglugginn birtir þá aðferð sem viðskiptamaðurinn vill nota til að taka á móti fylgiskjölum. Hægt er að breyta sendingaraðferð með því að velja uppflettihnappinn fyrir reitinn **senda skjal** Frekari upplýsingar er að finna á [Setja upp sendisnið skjala](sales-how-setup-document-send-profiles.md).

Tengdar vöru- og viðskiptamannafærslur eru nú búnar til í kerfinu og á sölureikningnum er frálag sem PDF fylgiskjal. Sölureikningurinn er fjarlægður af lista sölureikninga og skipt út fyrir nýtt fylgiskjal á lista bókaðra sölureikninga.  

### <a name="calculating-invoice-discounts-on-sales"></a>Reikna reikningsafslátt á sölu

[!INCLUDE [sales-invoice-discounts](includes/sales-invoice-discounts.md)]

## <a name="posted-invoices"></a>Bókaðir reikningar

[!INCLUDE [posted-invoices](includes/posted-invoices.md)]

Auðvelt er að leiðrétta eða afturkalla bókaðann sölureikning áður en hann er greiddur. Þetta er til dæmis gagnlegt þegar leiðrétta á innsláttarvillu eða þegar viðskiptamaðurinn biður um breytingu snemma í pöntunarferlinu. Frekari upplýsingar eru í [Ógreiddir sölureikningar leiðréttir eða afturkallaðir](sales-how-correct-cancel-sales-invoice.md). Ef bókaður sölureikningur er greiddur, verður að búa til sölukreditreikning til að afturkalla söluna. Fyrir frekar upplýsingar, sjá [Meðhöndlun söluvöruskila eða afturkallana](sales-how-process-sales-returns-cancellations.md).  

[Onpaðu **Bókaðir sölureikningar** listann ](https://businesscentral.dynamics.com/?page=143) í [!INCLUDE [prod_short](includes/prod_short.md)].

## <a name="registering-payments"></a>Skrá greiðslur

Það fer eftir þörfum fyrirtækis þíns, þú getur fengið greitt og skráð þessi greiðslu á mismunandi vegu: handvirkt, sjálfkrafa og með greiðsluþjónustu.  

Hægt er að vinna greiðslur beint frá viðskiptamannaspjaldinu. Nota aðgerðina **Skrá viðskiptamannagreiðslur** til að fá yfirlit yfir ógreidda reikninga fyrir þann viðskiptamann. Merkið síðan reikninginn sem greitt að hluta eða að fullu. Þessi greiðsluafstemming vinnur greiðslur viðskiptamanna þinna með samsvarandi upphæðum sem berast á bankareikningnum þínum með tengdum ógreiddum sölureikningum og sendir síðan greiðslurnar. Nánari upplýsingar er að finna í [Afstemma stakar greiðslur](receivables-how-reconcile-customer-payments-list-unpaid-sales-documents.md#to-register-customer-payments-individually).  

Í viðskiptaumhverfi þar sem viðskiptavinurinn greiðir nokkurn tíma eftir afhendingu, samkvæmt greiðsluskilmálum, er bókaður sölureikningur áfram opinn (ógreiddur) þar til innheimtudeildin staðfestir að greiðsla sé móttekin og jafnar greiðsluna við bókaðan sölureikning. Þetta er hægt að gera handvirkt eða sjálfkrafa. Nánari upplýsingar er að finna í [Afstemma greiðslur viðskiptamanna við inngreiðslubók eða úr færslum viðskiptamannabókar](receivables-how-apply-sales-transactions-manually.md) og [Afstemma greiðslur með sjálfvirkri jöfnun](receivables-how-reconcile-payments-auto-application.md).  

Í viðskiptaumhverfi þar sem viðskiptavinurinn greiðir strax, til dæmis með PayPal eða reiðufé, er greiðsla skráð strax þegar þú bókar sölureikninginn, þ.e.a.s. bókaða sölureikningnum er lokað sem að fullu jöfnuðum. Í reitnum **Kóði greiðslumáta** í sölupöntuninni þarf að velja viðeigandi. Sjá undir skrefi 8. Fyrir rafrænar greiðslur á borð við PayPal þarf einnig að fylla inn í reitinn **Greiðsluþjónusta**. Nánari upplýsingar eru í [Virkja greiðsluur viðskiptamanna um greiðsluþjónustur](sales-how-enable-payment-service-extensions.md).  

Þú getur jafnvel búið til beingreidda reikninga fyrir óskráða viðskiptavini með því að fyrst setja upp „viðskiptamannaspjald fyrir reiðufé“ sem þú bendir á í sölureikningnum. Frekari upplýsingar eru í [Setja upp viðskiptamenn með reiðufé](finance-how-to-set-up-cash-customers.md).  

> [!TIP]
> Ef senda á viðskiptavini áminningar um gjaldfallnar greiðslur þarf að setja upp stig og skilmála innheimtubréfs. Frekari upplýsingar eru í [Setja upp skilmála og stig innheimtubréfa](finance-setup-reminders.md).  

## <a name="external-document-numbers"></a>Númer ytri skjala

[!INCLUDE [ext-doc-no-sales](includes/ext-doc-no-sales.md)]

## <a name="see-related-training-at-microsoft-learn"></a>Sjá tengda þjálfun á [Microsoft Learn](/learn/modules/invoicing-customers-dynamics-365-business-central/index)

## <a name="see-also"></a>Sjá einnig

[Sala](sales-manage-sales.md)  
[Uppsetning sölu](sales-setup-sales.md)  
[Prenta tiltektarlistann](sales-how-print-picking-list.md)  
[Birgðir](inventory-manage-inventory.md)  
[Senda skjöl í tölvupósti](ui-how-send-documents-email.md)  
[Innheimta útistandandi skuldir](receivables-collect-outstanding-balances.md)  
[Magnreikningsfærsla frá Microsoft Bookings í Business Central ](finance-bookings.md)  
[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]