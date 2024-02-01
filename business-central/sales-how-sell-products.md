---
title: Búðu til sölupöntun viðskiptavinar og seldu vörur
description: 'Lýsir því hvernig skal búa til  sölupöntun, til að skrá samkomulag við viðskiptamann um að selja eða eiga viðskipti með vörur með tilteknum skilmálum.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'trade, partial deliveries, customer sales order, shipping advice, partial shipments,'
ms.search.form: '42, 48, 9305'
ms.date: 11/03/2023
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="sell-products-with-a-customer-sales-order"></a>Selja vörur með sölupöntun viðskiptavina

Þessi grein veitir leiðbeiningar um hvenær eigi að nota sölupöntun viðskiptamanns auk reiknings. Ef söluferlið þitt krefst þess að þú sendir aðeins hluta af pöntun, kannski vegna þess að allt magnið er ekki tiltækt strax, verður þú að vinna úr þeirri sölu með því að gera sölupöntun.

Einnig þarf að nota sölupantanir ef þú selur vörur sem eru sendar beint frá lánardrottni til viðskiptamanns, í því sem kallast bein afhending. Frekari upplýsingar eru í [Beinar sendingar](sales-how-drop-shipment.md). Frá öllum sjónarhornum séð virka sölupantanir á sama hátt og sölureikningar. Frekari upplýsingar eru á [Reikningsfæra sölur](sales-how-invoice-sales.md).

Þegar þú afhenda vörur, hvort sem er að fullu eða hluta, bókarðu sölupöntunina sem afhenta eða sem senda og reikningsfærða til að stofna viðkomandi vörufærslur og færslur í viðskiptamannabók í kerfinu. Við bókun sölupöntunar er einnig hægt að senda hana í tölvupósti sem PDF-viðhengi. Hægt er að fylla út fyrirfram meginmál tölvupósts með samantekt pöntunar og greiðsluupplýsingar, t.d. sem tengil á PayPal. Frekari upplýsingar er að finna í [Senda vörur](warehouse-how-ship-items.md) og [Senda skjöl með tölvupósti](ui-how-send-documents-email.md).

Í viðskiptaumhverfi þar sem viðskiptavinurinn greiðir strax, eins og með PayPal eða reiðufé, er greiðsla skráð strax þegar þú bókar sölureikninginn, sem þýðir að bókaður sölureikningur er lokaður þar sem hann er að fullu notaður. Í reitnum **Kóði greiðslumáta** í sölupöntuninni þarf að velja viðeigandi. Sjá þrep 5 hér að neðan. Fyrir rafrænar greiðslur á borð við PayPal þarf einnig að fylla inn í reitinn **Greiðsluþjónusta**. Frekari upplýsingar eru í [Virkja greiðslur viðskiptamanna um greiðsluþjónustur](sales-how-enable-payment-service-extensions.md).

Þú getur meira að segja búið til beint greiddar pantanir fyrir óskráða viðskiptavini með því að setja fyrst upp „reiðfé viðskiptavina“ kort sem þú bendir á á sölupöntuninni. Frekari upplýsingar má finna í [Uppsetning staðgreiðsluviðskiptamanna](finance-how-to-set-up-cash-customers.md).

## <a name="create-a-sales-order"></a>Stofna sölupöntun

> [!NOTE]  
> Eftirfarandi aðferð gerir ráð fyrir því að viðskiptavinurinn sé þegar settur upp. Sjá leiðbeiningar um hvernig þetta er gert í [Skrá nýja viðskiptavini](sales-how-register-new-customers.md).

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, færa inn **Sölupantanir**, velja síðan viðkomandi tengil.
2. Veljið **Nýtt** til að stofna nýja færslu.
3. Í reitnum **Viðskiptamaður** er fært inn nafn núverandi viðskiptamanns.

    Aðrir reitir á síðunni **Sölupöntun** eru nú fylltir út með stöðluðum upplýsingum um valinn viðskiptamann.  

4. Fylltu í eftirstandandi reiti á síðunni **sölupöntun** eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
    > Ef þú leyfir viðskiptavininum að greiða strax, til dæmis með kreditkorti eða PayPal, þá skaltu fylla út reitinn **Kóði greiðslumáta**. Greiðslan er þá skráð um leið og þú bókar sölupöntunina sem reikningsfærða. Ef þú velur *Reiðufé*, þá er greiðslan skráð á tilteknum mótreikningi.

    Þú ert nú tilbúinn til að fylla út sölupöntunarlínur með birgðavörum eða þjónustu sem þú vilt að viðskiptavinurinn kaupi.

    Ef þú setur upp endurteknar sölulínur fyrir viðskiptavininn, eins og mánaðarlega áfyllingarpöntun, geturðu sett þessar línur inn í pöntunina með því að velja aðgerðina **Fá endurteknar sölulínur** .
5. Á **Línur** Hraðflipanum, í reitnum **Type**, velurðu hvers konar vöru, gjald eða færslu þú sendir inn til viðskiptavinarins á sölulínunni.

6. Í reitnum **númer** sleginn inn fjöldi birgðavöru eða þjónustu.

    Þú skilur **nr.** reitur auður ef línan er fyrir:

    * Athugasemd. Rita athugasemdina í **Lýsing** reitinn.
    * Vara í vörulista. Velja **Velja vörulistaatriði** aðgerð. Frekari upplýsingar eru í [Vinna með vörulistaatriði](inventory-how-work-nonstock-items.md).
7. Í reitinn **Magn** er fært magn vara sem á að selja.

    > [!NOTE]  
    > Fyrir vörur af tegundinni *Forði* eða *Þjónusta* er magnið tímaeining, t.d. klukkutímar, eins og gefið er til kynna í reitnum **Mælieiningarkóði** í línunni. Frekari upplýsingar eru í [Setja upp mælieiningu vara](inventory-how-setup-units-of-measure.md).

    Reiturinn **línuupphæð** uppfærist til að sýna að gildið í reitnum **Einingarverð** margfaldað með tölunni í reitnum **magn**.

    Verð- og línuupphæðirnar eru sýndar með eða án VSK, en það fer eftir því hvað var valið í reitnum **verð með skatti** á viðskiptamannaspjaldinu.
8. Í reitnum **Línuafsláttur %**, færið inn prósentutölu ef veita á viðskiptamanninum afslátt af vörunni. Gildið í reitnum **Línuupphæð** er uppfært til samræmis.

    Ef þú setur upp sérstakt vöruverð á **Söluverð og sölulínuafslættir** Flýtiflipanum á viðskiptavina- eða vöruspjaldinu og þegar verðskilyrðin eru uppfyllt, verð og upphæð á sölulína er sjálfkrafa uppfærð. Frekari upplýsingar eru í [Skrá söluverð, afslátt og greiðslusamkomulag](sales-how-record-sales-price-discount-payment-agreements.md).
9. Til að bæta við athugasemd um pöntunarlínu sem viðskiptamaðurinn getur séð á prentuðu sölupöntuninni skal skrifa athugasemd í auða línu í reitinn **Lýsing**.  
10. Endurtaktu skref 5 til 9 fyrir hverja vöru sem þú vilt að viðskiptamaðurinn kaupi.

    Samtölureitirnir undir línunum uppfærast sjálfkrafa eftir því sem þú stofnar eða breytir línum til að sýna upphæðir sem verða bókaðar í fjárhagnum.

    > [!NOTE]
    > Í örfáum tilfellum kunna bókaðar upphæðir að sýna aðra upphæðir en þær sem sýndar eru í samtölureitunum. Þetta er yfirleitt vegna sléttunarútreiknings í tengslum við virðisaukaskatt eða söluskatt.
    >
    > Til að kanna upphæðirnar sem koma til með að vera bókaðar skal nota síðuna **Tölfræðilegar upplýsingar** sem tekur sléttunarútreikninga til greina. Einnig, ef þú velur aðgerðina **Gefa út**, verða samtölureitirnir uppfærðir til að hafa sléttunarútreikninga með.  

11. Í reitnum **Afsláttarupphæð reiknings** er hægt að færa inn upphæð sem draga á frá gildinu sem sýnt er í reitnum **Heildarupphæð með skatti**.

    Ef þú setur upp reikningsafslátt fyrir viðskiptavininn, og eftir að skilyrðin eru uppfyllt, er tilgreint prósentugildi sjálfkrafa sett inn í reitinn **Reikningarafsláttur %** . Og tengd upphæð er sett inn í **Inv. Afsláttarupphæð Excl. Skatt** reitur. Frekari upplýsingar eru í [Skrá söluverð, afslátt og greiðslusamkomulag](sales-how-record-sales-price-discount-payment-agreements.md).
12. Til að afhenda aðeins hluta pöntunarmagns skal færa inn magn í reitinn **Magn til afhendingar**. Gildið er sjálfkrafa afritað í reitinn **Magn til reikningsfærslu**.

    > [!NOTE]
    > Ef reiturinn **Ráðlegging um sendingu** er stilltur á **Ljúka** í flýtiflipanum **Afhending og greiðsla** er ekki hægt að bóka hlutaafhendingar. Frekari upplýsingar er að finna í [Vinna úr hlutaafhendingum](sales-how-send-partial-shipments.md).
13. Til að reikningsfæra aðeins hluta af afhentu magni skal færa inn magnið í reitinn **Magn til reikningsfærslu**. Magnið verður að vera minna en gildið í reitnum **Magn til að senda**.  
14. Þegar sölupöntunarlínunum er lokið, skal velja **bóka og senda** aðgerðina.

[!INCLUDE [order-ship-invoice](includes/order-ship-invoice.md)]

**Bóka og Senda á staðfestingu** svarglugginn birtir þá aðferð sem viðskiptamaðurinn vill nota til að taka á móti fylgiskjölum. Hægt er að breyta sendingaraðferð með því að velja uppflettihnappinn fyrir reitinn **senda skjal** Frekari upplýsingar eru í [Setja upp sendisnið skjala](sales-how-setup-document-send-profiles.md).

Tengdar vöru- og viðskiptamannafærslur eru nú búnar til í kerfinu og sölupöntunin er frálag sem PDF fylgiskjal. Þegar sölupöntunin er að fullu bókuð er hún fjarlægð af sölupöntunarlistanum og skipt út fyrir ný skjöl á sölureikningum og söluafhendingarlista.  

## <a name="external-document-number"></a>Númer ytra skjals

[!INCLUDE [ext-doc-no-sales](includes/ext-doc-no-sales.md)]

## <a name="see-also"></a>Sjá einnig .

[Reikningsfæra sölur](sales-how-invoice-sales.md)  
[Sölubókun](ui-post-sales.md)  
[Senda vörur](warehouse-how-ship-items.md)  
[Beinar sendingar](sales-how-drop-shipment.md)  
[Sala](sales-manage-sales.md)  
[Uppsetning sölu](sales-setup-sales.md)  
[Prenta tiltektarlistann](sales-how-print-picking-list.md)  
[Vinna úr hlutaafhendingum](sales-how-send-partial-shipments.md)  
[Birgðir](inventory-manage-inventory.md)  
[Senda skjöl í tölvupósti](ui-how-send-documents-email.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
