---
title: Reikningsfæra sölur
description: Lýsir því hvernig skal búa til söluvíxil, eða sölureikning eða sölupöntun, til að skrá samkomulag við viðskiptamann um að selja tilteknar vörur með tilteknum skilmálum.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bill, sale, invoice, order
ms.search.form: 43, 48, 9301
ms.date: 09/01/2022
ms.author: edupont
ms.openlocfilehash: 1a59356653c01ab9c1493bba0e6be80367f21217
ms.sourcegitcommit: 3acadf94fa34ca57fc137cb2296e644fbabc1a60
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/19/2022
ms.locfileid: "9529624"
---
# <a name="invoice-sales"></a>Reikningsfæra sölur

Yfirleitt er hægt að stofna sölupöntun eða sölureikning til að skrá samning þinn við viðskiptavin sem selur tilteknar vörur tilteknar afhendingar-og greiðsluskilmála.  

Hins vegar verður að nota sölupöntun í stað sölureiknings ef:  

* Þarf að senda aðeins hluta af pöntunarmagni, til dæmis, þar sem fullt magn er ekki í hendi.  
* Senda afurðir eftir að viðkomandi sölureikningar hafa verið bókaðir.
* Selja vörur lánardrottinn sendir beint til viðskiptamanns, sem þekkt er sem bein afhending. Frekari upplýsingar er að gera í [beinni afhendingu](sales-how-drop-shipment.md).  

Í öllum öðrum tilvikum vinna sölupantanir og sölureikningar upp á sama hátt. Frekari upplýsingar um notkun sölupantana í [selja vörur](sales-how-sell-products.md).

Hægt er að semja við viðskiptavininn með því að stofna sölutilboð, sem hægt er að breyta í sölureikning, þegar það er samþykkt við söluna. Frekari upplýsingar er að gera í [sölutilboðum](sales-how-make-offers.md).

## <a name="create-sales-invoices"></a>Stofna sölureikninga

Ef viðskiptamaðurinn ákveður að kaupa, bókar þú sölureikninginn til að stofna tengdar magn og virðisfærslur. Þegar sölureikningur er bókaður er einnig hægt að senda hann í tölvupósti sem PDF viðhengi. Þú getur forfyllt meginmál tölvupóstins með samantekt á reiknings-og greiðsluupplýsingum, eins og að útvega tengil á PayPal. Frekari upplýsingar í [senda skjöl með tölvupósti](ui-how-send-documents-email.md). Þegar viðskiptamaðurinn greiðir síðan reikninginn getur þú skráð þessi greiðslu á mismunandi vegu, allt eftir stærð og valinn vinnuflæði fyrirtækisins. Frekari upplýsingar er að fá í [hlutanum skráning greiðslna](#registering-payments).  

Birgðaspjöld geta verið af **birgðum**, **þjónustu** eða **Tegund sem ekki eru í birgðum** til að tilgreina ef varan er efnisleg Birgðaeining, Vinnueining eða efnisleg eining sem ekki er geymd í birgðum, eftir því sem við á. Lærðu meira á að [skrá nýjar vörur](inventory-how-register-new-items.md). Sölureikningsferlið er það sama fyrir allar þrjár vörutegundirnar.

Hægt er að fylla út reiti viðskiptavina á sölureikningnum með tvenns konar hætti, eftir því hvort viðskiptavinurinn er þegar skráður. Sjá skref 2 í eftirfarandi ferli.

### <a name="to-create-a-sales-invoice"></a>Sölureikningar búnir til:

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknið, færa inn **sölureikninga** og velja síðan tengda tengilinn.  
2. Í reitnum **Viðskiptamaður** er fært inn nafn núverandi viðskiptamanns. Ef viðskiptamaðurinn er hins vegar nýr og því ekki skráður skal fylgja þessum skrefum til að fylla út staðlaðar upplýsingar um viðskiptavin á **Sölureikningssíðan**:

    1. **Í reitinn Nafn** viðskiptamanns er fært inn heiti nýja viðskiptamannsins.
    2. Í svarglugganum um skráningu á nýjum viðskiptamanni er valið **Já**.
    3. **Á Velja sniðmát fyrir nýja viðskiptavinasíðu**, veljið sniðmát til að byggja nýja viðskiptamannaspjaldið á, veljið svo **í lagi**.
    4. Nýtt viðskiptamannaspjald sýnir upplýsingarnar á valda viðskiptamannasniðmátinu. Eftirstandandi reitir eru fylltir út. Lærðu meira á að [skrá nýja viðskiptamenn](sales-how-register-new-customers.md).  
    5. Þegar viðskiptamannakorta er lokið er hægt að velja **Loka** til að snúa aftur á **sölureikningssísíðuna**.

   Margir reitir í sölureikningahaus eru ný fullir af upplýsingar sem tilgreindar voru á nýja viðskiptamannaspjaldi.  
3. Fylltu í eftirstandandi reikningana á síðunni **sölureikningur** eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
    > Ef viðskiptavinur leyfir að greitt sé strax, til dæmis með reiðufé eða PayPal, þá er reiturinn Greiðsluháttur **fylltur út**. Greiðslan er síðan skráð um leið og þú bókar sölureikninginn. Ef valið *er reiðufé* er greiðslan skráð í tilgreindan mótreikning.

    Nú er hægt að fylla út línur **í** vöruflipa með afurðum sem verið er að selja til viðskiptavinarins eða fyrir færslur sem tengjast viðskiptamanninum sem á að skrá í fjárhag (Fjárhagsreikningur).

4. **Á fastflipanum línur** í **reitnum Tegund** er valin sú tegund afurðar, gjald eða færsla sem er bókuð fyrir viðskiptamanninn í sölulínunni.
   * Ef settar hafa verið upp endurteknar sölulínur fyrir viðskiptavininn, eins og mánaðarleg áfyllingarpöntun, er hægt að endurspegla pöntunina með því að velja **aðgerðina Sækja endurteknar sölulínur**.
5. Í reitnum **númer** Reitnum er valin færsla til að bóka samkvæmt gildinu í reitnum **Tegund** reit.

    Þú skilur **nr.** Reiturinn auður í eftirfarandi tilvikum:

    * Ef línan er ætluð athugasemd. Rita athugasemdina í **Lýsing** reitinn.
    * Ef línan er fyrir vörulistavöru. Velja **Velja vörulistaatriði** aðgerð. Frekari upplýsingar í [vinnu við vörulistavörur](inventory-how-work-nonstock-items.md).

6. **Í reitinn Magn** er fært inn hversu margar einingar af vörunni, gjaldfæra eða færslu línan á að skrá fyrir viðskiptavininn.  

    > [!NOTE]  
    > Ef varan er af **þjónustugerðinni**, eða **reiturinn** Tegund **forða**, er magnið tímaeining eins og t.d. klukkustundir, eins og tilgreint er í **reitnum Mælieiningarkóti** í línunni. [Frekari upplýsingar um uppsetningu vörueininga mæla](inventory-how-setup-units-of-measure.md)

    Gildið í **reitnum Línuupphæð** er reiknað sem *Einingarverð* × *magns*.  

    Verð- og línuupphæðirnar eru sýndar með eða án VSK, en það fer eftir því hvað var valið í reitnum **verð með skatti** á viðskiptamannaspjaldinu.  
7. Í reitnum **Línuafsláttur %**, færið inn prósentutölu ef veita á afslátt af vörunni. Gildið í reitnum **Línuupphæð** er uppfært til samræmis.  

    Ef sérstakt vöruverð hefur verið sett upp á flýtiflipanum **Afslættir söluverðs og sölulínu** á viðskiptamanns- eða vöruspjaldinu, uppfærist verðið og upphæðin á tilboðslínunni sjálfvirkt ef umsamin verðviðmið hafa náðst. Frekari upplýsingar hjá [Skráning söluverð, afsláttur og Greiðslusamningar](sales-how-record-sales-price-discount-payment-agreements.md).  
8. Endurtakið skref 4 til 7 fyrir hverja vöru eða gjald sem á reikningsfæra viðskiptavininn fyrir.

    Samtölur reita undir línunum eru uppfærðar sjálfkrafa, þar sem línur eru stofnaðar eða línum breytt til að sýna upphæðirnar sem bókaðar eru á fjárhag.

    > [!NOTE]
    > Í örfáum tilfellum kunna bókaðar upphæðir að sýna aðra upphæðir en þær sem sýndar eru í samtölureitunum. Venjulega gerist það vegna sléttunarútreiknings í tengslum við virðisaukaskatt.<br /><br />Ef kanna á upphæðir sem á að bóka í raun er hægt að nota **síðuna tölfræði**, sem tekur mið af sléttunarútreikningum. Einnig, ef þú velur aðgerðina **Gefa út**, verða samtölureitirnir uppfærðir til að hafa sléttunarútreikninga með.
9. **Í reitinn Reikn. afsl. upphæð án skatts** er færð inn upphæð sem á að draga frá gildinu sem er í **reitnum Samtala meðskatts** í reitnum Reikningsafsl.

    Ef settur hefur verið upp reikningsafsláttur fyrir viðskiptamanninn þá er tilgreint prósentugildið sjálfkrafa sett í **reitinn reikningsafsláttur** ef afsláttarskilyrðin eru uppfyllt og tengd upphæð sett inn í **reitinn Reikningsafsl. afsl. upphæð án skatts**. Frekari upplýsingar hjá [Skráning söluverð, afsláttur og Greiðslusamningar](sales-how-record-sales-price-discount-payment-agreements.md).

10. Þegar sölureikningslínunum er lokið, skal velja **bóka og senda** aðgerðina.  

**Bóka og Senda á staðfestingu** svarglugginn birtir þá aðferð sem viðskiptamaðurinn vill nota til að taka á móti fylgiskjölum. Hægt er að breyta sendingaraðferð með því að velja uppflettihnappinn fyrir reitinn **senda skjal** Frekari upplýsingar um uppsetningu á [stillingum](sales-how-setup-document-send-profiles.md) skjalasendingar.

Tengdar vöru- og viðskiptamannafærslur eru nú búnar til í kerfinu og á sölureikningnum er frálag sem PDF fylgiskjal. Sölureikningurinn er fjarlægður af lista sölureikninga og skipt út fyrir nýtt fylgiskjal á lista bókaðra sölureikninga.  

### <a name="calculating-invoice-discounts-on-sales"></a>Reikna reikningsafslátt á sölu

[!INCLUDE [sales-invoice-discounts](includes/sales-invoice-discounts.md)]

## <a name="posted-invoices"></a>Bókaðir reikningar

[!INCLUDE [posted-invoices](includes/posted-invoices.md)]

Auðvelt er að leiðrétta eða afturkalla bókaðann sölureikning áður en hann er greiddur. Þetta er gagnlegt þegar leiðrétta á mistök eða þegar viðskiptamaðurinn biður um breytingu snemma í pöntunarferlinu. Lærðu meira við að [leiðrétta eða hætta við ógreidda sölureikninga](sales-how-correct-cancel-sales-invoice.md). Ef bókaður sölureikningur er greiddur, verður að búa til sölukreditreikning til að afturkalla söluna. Frekari upplýsingar í [vinnslu söluskil eða afturkallanir](sales-how-process-sales-returns-cancellations.md).  

[Onpaðu **Bókaðir sölureikningar** listann ](https://businesscentral.dynamics.com/?page=143) í [!INCLUDE [prod_short](includes/prod_short.md)].

## <a name="registering-payments"></a>Skrá greiðslur

Eftir þörfum fyrirtækisins getur þú fengið greitt og skráð greiðslu á mismunandi vegu: handvirkt, sjálfvirkt, og með greiðsluþjónustu.  

Hægt er að vinna greiðslur beint frá viðskiptamannaspjaldinu. Nota aðgerðina **Skrá viðskiptamannagreiðslur** til að fá yfirlit yfir ógreidda reikninga fyrir þann viðskiptamann. Merkið síðan reikninginn sem greitt að hluta eða að fullu. Þessi greiðsluafstemmingar vinnur greiðslur viðskiptavina þinna eftir samsvarandi upphæðum sem mótteknar hafa verið á bankareikningi þínum með tengdum ógreiddum sölureikningum og bókar síðan greiðslurnar. Frekari upplýsingar í [hlutanum til að stemma af greiðslur sérstaklega](receivables-how-reconcile-customer-payments-list-unpaid-sales-documents.md#to-register-customer-payments-individually).  

Í viðskiptaumhverfi þar sem viðskiptavinurinn greiðir nokkurn tíma eftir afhendingu, samkvæmt greiðsluaðlögun, helst bókaði sölureikningur áfram opinn (Ógreidd) þar til Viðskiptavinir ríkisútvarpsins sannreyna að greiðsla sé móttekin og gildir hún á bókuðum sölureikningi. Þetta er hægt að gera handvirkt eða sjálfkrafa. Frekari upplýsingar um [afstemmingu greiðslna viðskiptavina við Inngreiðslubók viðskiptavinar eða viðskiptamannafærslur](receivables-how-apply-sales-transactions-manually.md) og [afstemmingar greiðslna með sjálfvirku forriti](receivables-how-reconcile-payments-auto-application.md).  

Í viðskiptaumhverfi þar sem viðskiptavinurinn greiðir strax, til dæmis með PayPal eða reiðufé, er greiðsla skráð strax þegar þú bókar sölureikninginn, þ.e.a.s. bókaða sölureikningnum er lokað sem að fullu jöfnuðum. Í reitnum **Kóði greiðslumáta** í sölupöntuninni þarf að velja viðeigandi. Fyrir rafrænar greiðslur á borð við PayPal þarf einnig að fylla inn í reitinn **Greiðsluþjónusta**. [Frekari upplýsingar um virkja viðskiptavinagreiðslur í gegnum greiðsluþjónustu](sales-how-enable-payment-service-extensions.md).

Þú getur jafnvel stofnað beint reikninga fyrir viðskiptamenn sem ekki eru skráðir með því að setja upp "staðgreiðsluviðskiptavin" korts fyrir þá, sem þú bendum á á sölureikninginn. Frekari upplýsingar er að setja upp hjá [viðskiptavinum](finance-how-to-set-up-cash-customers.md).  

> [!TIP]
> Ef senda á viðskiptavini áminningar um gjaldfallnar greiðslur þarf að setja upp stig innheimtubréfa og skilmála. Frekari upplýsingar um [uppsetningu Innheimtuskilmála og stiga](finance-setup-reminders.md).  

## <a name="external-document-numbers"></a>Númer ytri skjala

[!INCLUDE [ext-doc-no-sales](includes/ext-doc-no-sales.md)]

## <a name="see-related-microsoft-training"></a>Sjá tengda [Microsoft-þjálfun](/training/modules/invoicing-customers-dynamics-365-business-central/index).

## <a name="see-also"></a>Sjá einnig .

[Sala](sales-manage-sales.md)  
[Uppsetning sölu](sales-setup-sales.md)  
[Prenta tiltektarlistann](sales-how-print-picking-list.md)  
[Birgðir](inventory-manage-inventory.md)  
[Senda skjöl í tölvupósti](ui-how-send-documents-email.md)  
[Innheimta útistandandi skuldir](receivables-collect-outstanding-balances.md)  
[Magnreikningsfærsla frá Microsoft Bookings í Business Central ](finance-bookings.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
