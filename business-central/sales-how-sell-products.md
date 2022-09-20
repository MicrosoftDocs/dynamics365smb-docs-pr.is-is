---
title: Stofna sölupöntun viðskiptavinar og selja vörur
description: Lýsir því hvernig skal búa til  sölupöntun, til að skrá samkomulag við viðskiptamann um að selja eða eiga viðskipti með vörur með tilteknum skilmálum.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: trade, partial deliveries, customer sales order, shipping advice, partial shipments,
ms.search.form: 42, 48, 9305
ms.date: 09/02/2022
ms.author: edupont
ms.openlocfilehash: d40adc9e0d21b89f7b648862b08be8456287bd50
ms.sourcegitcommit: 8b95e1700a9d1e5be16cbfe94fdf7b660f1cd5d7
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/09/2022
ms.locfileid: "9460968"
---
# <a name="sell-products-with-a-customer-sales-order"></a>Selja vörur með sölupöntun viðskiptavinar

Í þessari grein er að finna leiðbeiningar um hvenær nota skal sölupöntun viðskiptavinar auk reiknings. Ef söluferlið krefst þess að aðeins sé hægt að senda hluta af pöntun, ef allt magnið er ekki tiltækt strax, verður að vinna úr þeirri sölu með því að gera sölupöntun.

Einnig þarf að nota sölupantanir ef seldar eru vörur sem afhendast beint frá lánardrottni til viðskiptamanns, í það sem kallað er bein afhending. Frekari upplýsingar er að gera í [beinni afhendingu](sales-how-drop-shipment.md). Að öllu öðru leyti þykir sölupantana vinna á sama hátt og sölureikningar. Frekari upplýsingar við [Reikningsölu](sales-how-invoice-sales.md).

Þegar þú afhenda vörur, hvort sem er að fullu eða hluta, bókarðu sölupöntunina sem afhenta eða sem senda og reikningsfærða til að stofna viðkomandi vörufærslur og færslur í viðskiptamannabók í kerfinu. Þegar sölupöntunin er bókuð er einnig hægt að senda hana með tölvupósti sem PDF viðhengi. Hægt er að forfylla netfangið í pósti með samantekt á pöntunar-og greiðsluupplýsingum, t.d. hlekk á PayPal. Frekari upplýsingar sendist á [vörur](warehouse-how-ship-items.md) og [Sendið skjöl með tölvupósti](ui-how-send-documents-email.md).

Í viðskiptaumhverfi þar sem viðskiptavinurinn greiðir strax, til dæmis með PayPal eða reiðufé, er greiðsla skráð strax þegar þú bókar sölupöntunina sem reikningsfærða, þ.e.a.s. bókaða sölureikningnum er lokað sem að fullu jöfnuðum. Í reitnum **Kóði greiðslumáta** í sölupöntuninni þarf að velja viðeigandi. Sjá þrep 5 hér að neðan. Fyrir rafrænar greiðslur á borð við PayPal þarf einnig að fylla inn í reitinn **Greiðsluþjónusta**. [Frekari upplýsingar um virkja viðskiptavinagreiðslur í gegnum greiðsluþjónustu](sales-how-enable-payment-service-extensions.md).

Jafnvel er hægt að stofna beinar greiðrar pantanir fyrir viðskiptavini sem ekki eru skráðir með því að setja fyrst upp "staðgreiðsluviðskiptavinur", sem bent er á í sölupöntuninni. Frekari upplýsingar er að setja upp hjá [viðskiptavinum](finance-how-to-set-up-cash-customers.md).

## <a name="create-a-sales-order"></a>Stofna sölupöntun

> [!NOTE]  
> Eftirfarandi aðferð gerir ráð fyrir því að viðskiptavinurinn sé þegar settur upp. Sjá leiðbeiningar um hvernig þetta er gert í [Skrá nýja viðskiptavini](sales-how-register-new-customers.md).

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Teikn, færa inn **sölupantanir** og velja síðan tengda tengilinn.
2. Veljið **Nýtt** til að stofna nýja færslu.
3. Í reitnum **Viðskiptamaður** er fært inn nafn núverandi viðskiptamanns.

    Önnur svæði á **sölupöntunarsíðunni** eru nú fyllt út með stöðluðum upplýsingum um valinn viðskiptavin.  

4. Fylltu í eftirstandandi reiti á síðunni **sölupöntun** eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
    > Ef þú leyfir viðskiptavininum að greiða strax, til dæmis með kreditkorti eða PayPal, þá skaltu fylla út reitinn **Kóði greiðslumáta**. Greiðslan er þá skráð um leið og þú bókar sölupöntunina sem reikningsfærða. Ef valið *er reiðufé* er greiðslan skráð í tilgreindan mótreikning.

    Nú er hægt að fylla út sölupöntunarlínurnar með birgðavörum eða þjónustu sem viðskiptamaðurinn á að kaupa.

    Ef settar hafa verið upp endurteknar sölulínur fyrir viðskiptavininn, eins og mánaðarleg áfyllingarpöntun, er hægt að setja þessar línur inn í pöntunina með því að **Velja aðgerðina Sækja endurteknar sölulínur**.
5. **Á vöruflipanum línur** í **reitnum Tegund** er valið hvaða tegund vöru, gjaldi eða færslu verður bókað á viðskiptamanninn í sölulínunni.

6. Í reitnum **númer** sleginn inn fjöldi birgðavöru eða þjónustu.

    Þú skilur **nr.** Reiturinn er auður ef línan er fyrir:

    * Athugasemd. Rita athugasemdina í **Lýsing** reitinn.
    * Vörulistavöru. Velja **Velja vörulistaatriði** aðgerð. Frekari upplýsingar í [vinnu við vörulistavörur](inventory-how-work-nonstock-items.md).
7. Í reitinn **Magn** er fært magn vara sem á að selja.

    > [!NOTE]  
    > Fyrir vörur af *forðanum* eða *þjónustugerðinni* er magnið tímaeining eins og til dæmis klukkustundir, eins og tilgreint er í **reitnum Mælieiningarkóti** í línunni. [Frekari upplýsingar er að setja upp í vörueiningum](inventory-how-setup-units-of-measure.md).

    **Reiturinn Línuupphæð** er uppfærður svo að hún sýni gildið í **reitnum Einingarverð** margfaldað með númerinu í **reitnum Magn**.

    Verð- og línuupphæðirnar eru sýndar með eða án VSK, en það fer eftir því hvað var valið í reitnum **verð með skatti** á viðskiptamannaspjaldinu.
8. Í reitnum **Línuafsláttur %**, færið inn prósentutölu ef veita á viðskiptamanninum afslátt af vörunni. Gildið í reitnum **Línuupphæð** er uppfært til samræmis.

    Ef sett hafa verið upp Sérstök vöruverð á **söluverði og sölulínuafslætti á föstu-Vöruafsláttur** á viðskiptamanna-eða birgðaspjaldinu þá uppfærist verðið og upphæðin í tilboðslínunni sjálfkrafa ef Umsamin verðskilyrði eru uppfyllt. Frekari upplýsingar hjá [Skráning söluverð, afsláttur og Greiðslusamningar](sales-how-record-sales-price-discount-payment-agreements.md).
9. Ef bæta á við athugasemd um pöntunarlínuna sem viðskiptavinurinn getur séð á prentuðu sölupöntuninni, Skrifið þá athugasemd í tóma línu í **reitnum Lýsing**.  
10. Endurtakið skref 5 til 9 fyrir hverja vöru sem viðskiptamaðurinn á að kaupa.

    Samtölur reita undir línunum eru sjálfkrafa uppfærðar þegar línur eru stofnaðar eða þeim breytt til að birta upphæðirnar sem á að bóka í fjárhag.

    > [!NOTE]
    > Í örfáum tilfellum kunna bókaðar upphæðir að sýna aðra upphæðir en þær sem sýndar eru í samtölureitunum. Þetta er vanalega vegna sléttunarútreikninga í tengslum við virðisauka (VAT) eða virðisaukaskatt.
    >
    > Til að kanna upphæðirnar sem verða í raun og veru eftir er notuð **upplýsingasíða** sem tekur mið af sléttunarútreikningum. Einnig, ef þú velur aðgerðina **Gefa út**, verða samtölureitirnir uppfærðir til að hafa sléttunarútreikninga með.  

11. Í reitnum Upphæð **reikningsafsláttar er hægt að færa inn upphæðina sem á að draga frá gildinu sem er í reitnum Samtals í** reitnum heildarskattur **.**

    Ef búið er að setja upp reikningsafslátt fyrir viðskiptavininn er gildið sem er sjálfkrafa sett inn í **reitinn reikningsafsláttur** færður inn ef forsendurnar eru uppfylltar og tengd upphæð sett inn í **reitinn Reikningsafsl. afsl. upphæð án skatts**. Frekari upplýsingar hjá [Skráning söluverð, afsláttur og Greiðslusamningar](sales-how-record-sales-price-discount-payment-agreements.md).
12. Ef aðeins á að senda hluta af pöntunarmagninu er magnið fært inn í **reitinn Magn til sendingar**. Gildið afritar sjálfkrafa í **reitinn Magn í reikning**.

    > [!NOTE]
    > **Ef reiturinn flutningsráð** er stilltur sem **heill** í **flipanum Afhending og innheimtur** er ekki hægt að bóka hlutaafhendingar. Frekari upplýsingar á [ferli hlutaafhendingar](sales-how-send-partial-shipments.md).
13. Til að reikningsfæra aðeins hluta afhentra magns er magnið fært inn í **reitinn Magn til reikningsfærslu**. Magnið verður að vera minna en gildið í reitnum **Magn til að senda**.  
14. Þegar sölupöntunarlínunum er lokið, skal velja **bóka og senda** aðgerðina.

[!INCLUDE [order-ship-invoice](includes/order-ship-invoice.md)]

**Bóka og Senda á staðfestingu** svarglugginn birtir þá aðferð sem viðskiptamaðurinn vill nota til að taka á móti fylgiskjölum. Hægt er að breyta sendingaraðferð með því að velja uppflettihnappinn fyrir reitinn **senda skjal** Frekari upplýsingar um uppsetningu á [stillingum](sales-how-setup-document-send-profiles.md) skjalasendingar.

Tengdar vöru- og viðskiptamannafærslur eru nú búnar til í kerfinu og sölupöntunin er frálag sem PDF fylgiskjal. Þegar sölupöntunin er fullbókuð er hún fjarlægð af listanum yfir sölupantanir og henni er skipt út fyrir ný skjöl á listanum yfir bókaða sölureikninga og lista yfir bókaðar söluafhendingar.  

## <a name="external-document-number"></a>Númer ytra skjals

[!INCLUDE [ext-doc-no-sales](includes/ext-doc-no-sales.md)]

## <a name="see-related-training-at-microsoft-learn"></a>Sjá tengdar þjálfun kl [Microsoft Learn](/learn/modules/create-sales-documents-dynamics-365-business-central/).

## <a name="see-also"></a>Sjá einnig .

[Reikningsfæra sölur](sales-how-invoice-sales.md)  
[Sölubókun](ui-post-sales.md)  
[Senda vörur](warehouse-how-ship-items.md)  
[Beinar sendingar](sales-how-drop-shipment.md)  
[Sala](sales-manage-sales.md)  
[Uppsetning sölu](sales-setup-sales.md)  
[Prenta tiltektarlistann](sales-how-print-picking-list.md)  
[Vinna hlutaafhendingar](sales-how-send-partial-shipments.md)  
[Birgðir](inventory-manage-inventory.md)  
[Senda skjöl í tölvupósti](ui-how-send-documents-email.md)  
[Vinna með[!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
