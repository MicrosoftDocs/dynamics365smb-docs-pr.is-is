---
title: Stofna sölupöntun viðskiptavinar og selja vörur
description: Lýsir því hvernig skal búa til  sölupöntun, til að skrá samkomulag við viðskiptamann um að selja eða eiga viðskipti með vörur með tilteknum skilmálum.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: trade, partial deliveries, customer sales order
ms.date: 09/24/2021
ms.author: edupont
ms.openlocfilehash: 7156684c2b12af7e5b3e8b51791a702566824009
ms.sourcegitcommit: 6ad0a834fc225cc27dfdbee4a83cf06bbbcbc1c9
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/01/2021
ms.locfileid: "7588502"
---
# <a name="sell-products-with-a-customer-sales-order"></a>Selja vörur með sölupöntun viðskiptavinar  

Þessi grein veitir notendum leiðbeiningar um hvenær á að nota sölupöntun viðskiptavinar frekar en bara reikning. Ef söluferlið krefst þess að aðeins hægt að afhenda hluta pöntunarmagns, til dæmis þar sem allt magnið er ekki tiltæk í einu, og selja svo viðkomandi vörur með því að búa til sölupöntun fyrir viðskiptavin.  

Ef vara er seld með því að afhenda beint frá lánardrottni til viðskiptamanns, sem bein sending þarf að einnig nota sölupantanir. Frekari upplýsingar eru í [Beinar sendingar](sales-how-drop-shipment.md). Frá öllum sjónarhornum séð virka sölupantanir á sama hátt og sölureikningar. Frekari upplýsingar eru í [Reikningsfæra sölur](sales-how-invoice-sales.md).

Þegar þú afhenda vörur, hvort sem er að fullu eða hluta, bókarðu sölupöntunina sem afhenta eða sem senda og reikningsfærða til að stofna viðkomandi vörufærslur og færslur í viðskiptamannabók í kerfinu. Við bókun sölupöntunar, er einnig hægt að senda skjalið í tölvupósti sem PDF viðhengi. Hægt er að láta meginmálslínur tölvupósts vera útfyllt fyrirfram með samantekt á pöntuninni og greiðsluupplýsingum, eins og tengli í PayPal. Frekari upplýsingar eru í [Senda skjöl í tölvupósti](ui-how-send-documents-email.md).

Í viðskiptaumhverfi þar sem viðskiptavinurinn greiðir strax, til dæmis með PayPal eða reiðufé, er greiðsla skráð strax þegar þú bókar sölupöntunina sem reikningsfærða, þ.e.a.s. bókaða sölureikningnum er lokað sem að fullu jöfnuðum. Í reitnum **Kóði greiðslumáta** í sölupöntuninni þarf að velja viðeigandi. Sjá undir skrefi 8. Fyrir rafrænar greiðslur á borð við PayPal þarf einnig að fylla inn í reitinn **Greiðsluþjónusta**. Nánari upplýsingar eru í [Virkja greiðslur viðskiptamanns í gegnum greiðsluþjónustur](sales-how-enable-payment-service-extensions.md).

Þú getur jafnvel búið til beingreiddar pantanir fyrir óskráða viðskiptavini með því að fyrst setja upp „viðskiptamannaspjald fyrir reiðufé" sem þú bendir á í sölupöntuninni. Frekari upplýsingar eru í [Setja upp viðskiptamenn með reiðufé](finance-how-to-set-up-cash-customers.md).

## <a name="to-create-a-sales-order"></a>Sölupöntun stofnuð

> [!NOTE]  
> Eftirfarandi aðferð gerir ráð fyrir því að viðskiptavinurinn sé þegar settur upp. Sjá leiðbeiningar um hvernig þetta er gert í [Skrá nýja viðskiptavini](sales-how-register-new-customers.md).

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, færa inn **Sölupantanir** og velja síðan viðkomandi tengil.
2. Veljið **Nýtt** til að stofna nýja færslu.
3. Í reitnum **Viðskiptamaður** er fært inn nafn núverandi viðskiptamanns.

    Aðrir reitir á síðunni **Sölupöntun** eru nú fylltir út með stöðluðum upplýsingum um viðskiptamanninn sem valinn hefur verið.  

4. Fylltu í eftirstandandi reiti á síðunni **sölupöntun** eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
    > Ef þú leyfir viðskiptavininum að greiða strax, til dæmis með kreditkorti eða PayPal, þá skaltu fylla út reitinn **Kóði greiðslumáta**. Greiðslan er þá skráð um leið og þú bókar sölupöntunina sem reikningsfærða. Ef þú velur REIÐUFÉ, þá er greiðslan skráð á tilteknum mótreikningi.

    Þú ert nú tilbúinn að fylla út í sölupöntunarlínurnar með birgðavöru eða þjónustu sem selja á viðskiptamanninum.

    Ef endurteknar sölulínur hafa verið settar upp fyrir viðskiptamanninn, svo sem mánaðarlegar endurnýjunarpantanir, er hægt að færa línuna inn í pöntunina með því að velja aðgerðina **Endurteknar sölulínur**.
5. Á **Línur** Flýtiflipanum í **Tegund** reitnum, veldu hvaða tegund framleiðsluflokks, kostnaðarauka eða færslu þú munt bókað fyrir viðskiptamanninn með sölulínunni.

6. Í reitnum **númer** sleginn inn fjöldi birgðavöru eða þjónustu.

    Þú skilur **nr.** reitur tómur í eftirfarandi tilfellum:

    * Ef línan er ætluð athugasemd. Rita athugasemdina í **Lýsing** reitinn.
    * Ef línan er fyrir vörulistavöru. Velja **Velja vörulistaatriði** aðgerð. Nánari upplýsingar er að finna í [Vinna með vörulistaatriði](inventory-how-work-nonstock-items.md).
7. Í reitinn **Magn** er fært magn vara sem á að selja.

    > [!NOTE]  
    > Fyrir vörur af tegundinni *Forði* eða *Þjónusta* er magnið tímaeining, t.d. klukkutímar, eins og gefið er til kynna í reitnum **Mælieiningarkóði** í línunni. Frekari upplýsingar eru í [Setja upp mælieiningu vara](inventory-how-setup-units-of-measure.md).

    Reiturinn **línuupphæð** uppfærist til að sýna að gildið í reitnum **einingarverð** margfaldað með gildinu í reitnum **magn**.

    Verð- og línuupphæðirnar eru sýndar með eða án VSK, en það fer eftir því hvað var valið í reitnum **verð með skatti** á viðskiptamannaspjaldinu.
8. Í reitnum **Línuafsláttur %**, færið inn prósentutölu ef veita á viðskiptamanninum afslátt af vörunni. Gildið í reitnum **Línuupphæð** er uppfært til samræmis.

    Ef sérstakt vöruverð hefur verið sett upp á flýtiflipanum **Afslættir söluverðs og sölulínu** á viðskiptamanns- eða birgðaspjaldinu uppfærist verðið og upphæðin á tilboðslínunni sjálfvirkt ef umsamin verðviðmið hafa náðst. Nánari upplýsingar eru í [Skrá söluverð, afslátt og greiðslusamkomulag](sales-how-record-sales-price-discount-payment-agreements.md).
9. Til að bæta við athugasemd um pöntunarlínu sem viðskiptavinurinn getur séð á prentuðu sölupöntuninni, skrifaðu athugasemd í **Lýsingarsvæði** sviði í auða línu.  
10. Endurtakið skref 5 til 9 fyrir hverja birgðavöru sem selja á viðskiptamanninum.

    Samtölureitirnir undir línunum uppfærast sjálfkrafa eftir því sem þú stofnar eða breytir línum til að sýna upphæðir sem verða bókaðar í fjárhagnum.

    > [!NOTE]
    > Í örfáum tilfellum kunna bókaðar upphæðir að sýna aðra upphæðir en þær sem sýndar eru í samtölureitunum. Venjulega gerist það vegna sléttunarútreiknings í tengslum við virðisaukaskatt.
    >
    > Til að kanna upphæðirnar sem koma til með að vera bókaðar skal nota síðuna **Tölfræðilegar upplýsingar** sem tekur sléttunarútreikninga til greina. Einnig, ef þú velur aðgerðina **Gefa út**, verða samtölureitirnir uppfærðir til að hafa sléttunarútreikninga með.  

11. Í reitnum **Afsláttarupphæð reiknings** er hægt að færa inn upphæð sem draga á frá gildinu sem sýnt er í reitnum **Heildarupphæð með skatti**.

    Ef reikningsafslættir hafa verið settir upp fyrir viðskiptamanninn, er tilgreint prósentugildi sjálfvirkt fært inn í reitinn **reikningsafsláttur %** ef viðmiðum hefur verið mætt og upphæðin færð inn í reitinn **afsláttarupphæð án skatts**. Nánari upplýsingar eru í [Skrá söluverð, afslátt og greiðslusamkomulag](sales-how-record-sales-price-discount-payment-agreements.md).
12. Til að afhenda Aðeins hluta pöntunarmagns, skal færa magn í reitinn **magn til Afhendingar** reit. Gildið er afritað í reitinn **magn til Reikningsfærslu**.
13. Til að reikningsfæra Aðeins hluta sends magns, skal færa magn í reitinn **magn til að reikningsfæra** . Magnið verður að vera minna en gildið í reitnum **Magn til að senda**.  
14. Þegar sölupöntunarlínunum er lokið, skal velja **bóka og senda** aðgerðina.

**Bóka og Senda á staðfestingu** svarglugginn birtir þá aðferð sem viðskiptamaðurinn vill nota til að taka á móti fylgiskjölum. Hægt er að breyta sendingaraðferð með því að velja uppflettihnappinn fyrir reitinn **senda skjal** Frekari upplýsingar er að finna á [Setja upp sendisnið skjala](sales-how-setup-document-send-profiles.md).

Tengdar vöru- og viðskiptamannafærslur eru nú búnar til í kerfinu og sölupöntunin er frálag sem PDF fylgiskjal. Þegar sölupantanir eru að fullu bókaðar, er þær fjarlægður af lista sölupantana og skipt út fyrir nýtt fylgiskjal á lista bókaðra sölureikninga og lista yfir bókaðar söluafhendingar.  

## <a name="external-document-number"></a>Númer ytra skjals

[!INCLUDE [ext-doc-no-sales](includes/ext-doc-no-sales.md)]

## <a name="see-also"></a>Sjá einnig

[Sala](sales-manage-sales.md)  
[Uppsetning sölu](sales-setup-sales.md)  
[Prenta tiltektarlistann](sales-how-print-picking-list.md)  
[Birgðir](inventory-manage-inventory.md)  
[Senda skjöl í tölvupósti](ui-how-send-documents-email.md)  
[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]