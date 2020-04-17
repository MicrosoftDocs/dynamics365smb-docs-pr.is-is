---
title: Stofna sölupöntun og selja vörur | Microsoft Docs
description: Lýsir því hvernig skal búa til  sölupöntun, til að skrá samkomulag við viðskiptamann um að selja eða eiga viðskipti með vörur með tilteknum skilmálum.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: trade
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 5fefafc1ca8ac7f5cd9862ff741a0f0fd9fec7ff
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2020
ms.locfileid: "3194020"
---
# <a name="sell-products"></a>Selja vörur
Búinn er til sölureikningur eða sölupöntun til að skrá samkomulag við viðskiptamann um að selja tilteknar vörur með tilteknum afhendingar- og greiðsluskilmálum.

> [!NOTE]  
>   Þú notar sölupantanir ef söluferlið krefst þess að hægt að afhenda hluta pöntunarmagns , til dæmis þar sem allt magnið er ekki tiltæk í einu. Ef vara er seld með því að afhenda beint frá lánardrottni til viðskiptamanns, sem bein sending þarf að einnig nota sölupantanir. Frekari upplýsingar eru í [Beinar sendingar](sales-how-drop-shipment.md). Frá öllum sjónarhornum séð virka sölupantanir á sama hátt og sölureikningar. Frekari upplýsingar eru í [Reikningsfæra sölur](sales-how-invoice-sales.md).

Hægt er að semja við viðskiptamanninn með því að gera fyrst sölutilboð, sem hægt er að breyta í sölupöntun þegar samkomulag hefur náðst um söluna. Frekari upplýsingar er að finna í [Búa til sölutilboð](sales-how-make-offers.md).

Þegar viðskiptamaðurinn hefur staðfest samninginn, til dæmis eftir tilboðsferli, geturðu sent staðfestingu pöntunar til að skrá afhendindingarskyldu vörunnar, eins og um var samið.

Þegar þú afhenda vörur, hvort sem er að fullu eða hluta, bókarðu sölupöntunina sem afhenta eða sem senda og reikningsfærða til að stofna viðkomandi vörufærslur og færslur í viðskiptamannabók í kerfinu. Við bókun sölupöntunar, er einnig hægt að senda skjalið í tölvupósti sem PDF viðhengi. Hægt er að láta meginmálslínur tölvupósts vera útfyllt fyrirfram með samantekt á pöntuninni og greiðsluupplýsingum, eins og tengli í PayPal. Frekari upplýsingar eru í [Senda skjöl í tölvupósti](ui-how-send-documents-email.md).

Í viðskiptaumhverfi þar sem viðskiptavinurinn greiðir nokkurn tíma eftir afhendingu, samkvæmt greiðsluskilmálum, er bókaður sölureikningur áfram opinn (ógreiddur) þar til innheimtudeildin staðfestir að greiðsla sé móttekin og jafnar greiðsluna við bókaðan sölureikning. Frekari upplýsingar eru í [Afstemma greiðslur með því að nota sjálfvirk jöfnun](receivables-how-reconcile-payments-auto-application.md).

Í viðskiptaumhverfi þar sem viðskiptavinurinn greiðir strax, til dæmis með PayPal eða reiðufé, er greiðsla skráð strax þegar þú bókar sölupöntunina sem reikningsfærða, þ.e.a.s. bókaða sölureikningnum er lokað sem að fullu jöfnuðum. Í reitnum **Kóði greiðslumáta** í sölupöntuninni þarf að velja viðeigandi. Sjá undir skrefi 8. Fyrir rafrænar greiðslur á borð við PayPal þarf einnig að fylla inn í reitinn **Greiðsluþjónusta**. Nánari upplýsingar eru í [Virkja greiðslur viðskiptamanns í gegnum greiðsluþjónustur](sales-how-enable-payment-service-extensions.md).

Þú getur jafnvel búið til beingreiddar pantanir fyrir óskráða viðskiptavini með því að fyrst setja upp „viðskiptamannaspjald fyrir reiðufé" sem þú bendir á í sölupöntuninni. Frekari upplýsingar eru í [Setja upp viðskiptamenn með reiðufé](finance-how-to-set-up-cash-customers.md).

Auðvelt er að leiðrétta eða afturkalla bókaðann sölureikning sem á uppruna sinn í sölupöntun áður en hann er greiddur. Þetta er gagnlegt þegar leiðrétta á mistök eða þegar viðskiptamaðurinn biður um breytingu snemma í pöntunarferlinu. Frekari upplýsingar eru í [Ógreiddir sölureikningar leiðréttir eða afturkallaðir](sales-how-correct-cancel-sales-invoice.md). Ef bókaður sölureikningur er greiddur, verður að búa til sölukreditreikning til að afturkalla söluna. Fyrir frekar upplýsingar, sjá [Meðhöndlun söluvöruskila eða afturkallana](sales-how-process-sales-returns-cancellations.md).

Birgðaspjaldið getur verið af gerðinni **Birgðir**, **Þjónusta** og **Ekki birgðir** til að tilgreina hvort vara er raunbirgðaeining, launatímaeining eða efnisleg eining sem ekki er geymd í birgðum. Nánari upplýsingar eru í [Skrá nýjar vörur](inventory-how-register-new-items.md). Sölupantanaferlið er það sama fyrir allar þrjár vörutegundir.

Hægt er að fylla út viðskiptamannsreitina á sölupöntunina með tveimur leiðum, eftir því hvort viðskiptamaðurinn hefur þegar verið skráður. Sjá lið 2 og 3 í eftirfarandi ferli.

## <a name="to-create-a-sales-order"></a>Sölupöntun stofnuð
1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Sölupantanir** og veldu síðan tengda tengilinn.
2. Í reitnum **Viðskiptamaður** er fært inn nafn núverandi viðskiptamanns.

    Aðrir reitir á síðunni **Sölupöntun** eru nú fylltir út með stöðluðum upplýsingum um viðskiptamanninn sem valinn hefur verið. Ef viðskiptamaður er ekki skráður, fylgið eftirfarandi skrefum:
3. Í reitnum **Viðskiptamaður** er fært inn nafn nýs viðskiptamanns.
4. Í svarglugganum um að skrá nýja viðskiptavininn, veljið hnappinn **Já**.
5. Á síðunni **Velja sniðmát fyrir nýjan viðskiptamann**, skal velja sniðmát til að byggja nýja viðskiptamannaspjaldið á og veljið hnappinn **Í lagi**.

    Nýtt viðskiptamannaspjald opnast, fyrirfram fyllt út með upplýsingnum á valda viðskiptamannasniðmátinu. Reiturinn **Nafn** er fyrirfram fylltur út með nafni nýja viðskiptamannsins sem fært var inn á sölupöntun.
6. Haltu áfram að fylla út eftirstandandi reiti á spjaldi viðskiptamanns. Frekari upplýsingar eru í [Skrá nýja viðskiptamenn](sales-how-register-new-customers.md).  
7. Þegar lokið hefur verið við viðskiptamannaspjaldið skal velja hnappinn **Í lagi** til að fara aftur á síðuna **sölupöntun**.

    Margir reitir í sölupöntun eru nú fullir af upplýsingar sem tilgreindar voru á nýja viðskiptamannaspjaldi.
8. Fylltu í eftirstandandi reiti á síðunni **sölupöntun** eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
    > Ef þú leyfir viðskiptavininum að greiða strax, til dæmis með kreditkorti eða PayPal, þá skaltu fylla út reitinn **Kóði greiðslumáta**. Greiðslan er þá skráð um leið og þú bókar sölupöntunina sem reikningsfærða. Ef þú velur REIÐUFÉ, þá er greiðslan skráð á tilteknum mótreikningi.

    Þú ert nú tilbúinn að fylla út í sölupöntunarlínurnar með birgðavöru eða þjónustu sem selja á viðskiptamanninum.

    Ef endurteknar sölulínur hafa verið settar upp fyrir viðskiptamanninn, svo sem mánaðarlegar endurnýjunarpantanir, er hægt að færa línuna inn í pöntunina með því að velja aðgerðina **Endurteknar sölulínur**.
9. Í flýtiflipanum **Línur** í reitnum **Vara** er sleginn inn fjöldi birgðavöru eða þjónustu.  
10. Í reitinn **Magn** er fært magn vara sem á að selja.

    > [!NOTE]  
    >   Fyrir vörur af tegundinni Þjónusta er magnið tímaeining, t.d. klukkutímar, eins og gefið er til kynna í reitnum **Mælieiningarkóði** í línunni.

    Reiturinn **línuupphæð** uppfærist til að sýna að gildið í reitnum **einingarverð** margfaldað með gildinu í reitnum **magn**.

    Verð- og línuupphæðirnar eru sýndar með eða án VSK, en það fer eftir því hvað var valið í reitnum **verð með skatti** á viðskiptamannaspjaldinu.
11. Í reitnum **Línuafsláttur %**, færið inn prósentutölu ef veita á viðskiptamanninum afslátt af vörunni. Gildið í reitnum **Línuupphæð** er uppfært til samræmis.

    Ef sérstakt vöruverð hefur verið sett upp á flýtiflipanum **Afslættir söluverðs og sölulínu** á viðskiptamanns- eða birgðaspjaldinu uppfærist verðið og upphæðin á tilboðslínunni sjálfvirkt ef umsamin verðviðmið hafa náðst. Nánari upplýsingar eru í [Skrá söluverð, afslátt og greiðslusamkomulag](sales-how-record-sales-price-discount-payment-agreements.md).
12. Til að bæta við athugasemd um tilboðslínu sem viðskiptavinurinn getur séð á prentuðu sölureikningi, skrifaðu texta í **Lýsingarsvæði** sviði í auða línu.  
13. Endurtakið skref 9 til 12 fyrir hverja birgðavöru sem selja á viðskiptamanninum.

    Samtölur fyrir neðan línurnar eru sjálfkrafa reiknaðar þegar þú stofnar eða breytir línum.
14. Nýtt viðskiptamannaspjald sýnir upplýsingarnar á valda viðskiptamannasniðmátinu. Eftirstandandi reitir eru fylltir út. Frekari upplýsingar eru í [Skrá nýja viðskiptamenn](sales-how-register-new-customers.md).  
15. Þegar lokið hefur verið við viðskiptamannaspjaldið skal velja hnappinn **Í lagi** til að fara aftur á síðuna **sölupöntun**.

    Margir reitir í sölupöntun eru nú fullir af upplýsingar sem tilgreindar voru á nýja viðskiptamannaspjaldi.
16. Fylltu í eftirstandandi reiti á síðunni **sölupöntun** eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    Nú er hægt að fylla út í sölupöntunarlínur fyrir vörur sem selt er viðskiptamanni eða fyrir einhverri færslu við þann viðskiptamann sem á að skrá í reikning í Fjárhag.   

    Ef endurteknar sölulínur hafa verið settar upp fyrir viðskiptamanninn, svo sem mánaðarlegar endurnýjunarpantanir, er hægt að færa línuna inn í pöntunina með því að velja aðgerðina **Endurteknar sölulínur**.  
17. Á **Línur** Flýtiflipanum í **Tegund** reitnum, veldu hvaða tegund framleiðsluflokks, kostnaðarauka eða færslu þú munt bókað fyrir viðskiptamanninn með sölulínunni.

18. Í reitnum **númer** Reitnum er valin færsla til að bóka samkvæmt gildinu í reitnum **Tegund** reit.

    Þú skilur **nr.** reitur tómur í eftirfarandi tilfellum:

    * Ef línan er ætluð athugasemd. Rita athugasemdina í **Lýsing** reitinn.
    * Ef línan er fyrir vörulistavöru. Velja **Velja vörulistaatriði** aðgerð. Nánari upplýsingar er að finna í [Vinna með vörulistaatriði](inventory-how-work-nonstock-items.md).

19. Í reitnum **Magn** er fært inn hversu margar einingar vöru, kostnaðarauka eða færslu sem línan skráir fyrir viðskiptamanninn.  

    > [!NOTE]  
    > Ef varan er af gerðinni **Þjónusta** eða reiturinn **Gerð** innniheldur **Forið** þá er magnið tíaeining á borð við klukkustundir, eins og táknað er í **Mælieiningarkóði** reitnum á línunni. Frekari upplýsingar eru í [Setja upp mælieiningu vara](inventory-how-setup-units-of-measure.md).

    Gildið í reitnum **Línuupphæð** er reiknaður sem *Einingarverð* x *Magn*.  

    Verð- og línuupphæðirnar eru sýndar með eða án VSK, en það fer eftir því hvað var valið í reitnum **verð með skatti** á viðskiptamannaspjaldinu.  
20. Í reitnum **Línuafsláttur %**, færið inn prósentutölu ef veita á afslátt af vörunni. Gildið í reitnum **Línuupphæð** er uppfært til samræmis.  

    Ef sérstakt vöruverð hefur verið sett upp á flýtiflipanum **Afslættir söluverðs og sölulínu** á viðskiptamanns- eða vöruspjaldinu, uppfærist verðið og upphæðin á tilboðslínunni sjálfvirkt ef umsamin verðviðmið hafa náðst. Nánari upplýsingar eru í [Skrá söluverð, afslátt og greiðslusamkomulag](sales-how-record-sales-price-discount-payment-agreements.md).  
21. Endurtakið skref 9 til 12 fyrir hverja vöru eða gjald sem selja á viðskiptamanninum.  

    Samtölureitirnir undir línunum uppfærast sjálfkrafa eftir því sem þú stofnar eða breytir línum til að sýna upphæðir sem verða bókaðar í fjárhagnum.

    > [!NOTE]
    > Í örfáum tilfellum kunna bókaðar upphæðir að sýna aðra upphæðir en þær sem sýndar eru í samtölureitunum. Venjulega gerist það vegna sléttunarútreiknings í tengslum við virðisaukaskatt.<br /><br />Til að kanna upphæðirnar sem koma til með að vera bókaðar er hægt að nota síðuna **Tölfræðilegar upplýsingar** sem tekur sléttunarútreikninga til greina. Einnig, ef þú velur aðgerðina **Gefa út**, verða samtölureitirnir uppfærðir til að hafa sléttunarútreikninga með.  
22. Í reitnum **afsláttarupphæð reiknings** færið inn upphæð sem draga á frá gildinu sem sýnt er í reitnum **Heildarupphæð með skatti**.

    Ef reikningsafslættir hafa verið settir upp fyrir viðskiptamanninn, er tilgreint prósentugildi sjálfvirkt fært inn í reitinn **reikningsafsláttur %** ef viðmiðum hefur verið mætt og upphæðin færð inn í reitinn **afsláttarupphæð án skatts**. Nánari upplýsingar eru í [Skrá söluverð, afslátt og greiðslusamkomulag](sales-how-record-sales-price-discount-payment-agreements.md).
23. Til að afhenda Aðeins hluta pöntunarmagns, skal færa magn í reitinn **magn til Afhendingar** reit. Gildið er afritað í reitinn **magn til Reikningsfærslu**.
24. Til að reikningsfæra Aðeins hluta sends magns, skal færa magn í reitinn **magn til að reikningsfæra** . Magnið verður að vera minna en gildið í reitnum **Magn til að senda**.   
25. Þegar sölupöntunarlínunum er lokið, skal velja **bóka og senda** aðgerðina.

**Bóka og Senda á staðfestingu** svarglugginn birtir þá aðferð sem viðskiptamaðurinn vill nota til að taka á móti fylgiskjölum. Hægt er að breyta sendingaraðferð með því að velja uppflettihnappinn fyrir reitinn **senda skjal** Frekari upplýsingar er að finna á [Setja upp sendisnið skjala](sales-how-setup-document-send-profiles.md).

Tengdar vöru- og viðskiptamannafærslur eru nú búnar til í kerfinu og sölupöntunin er frálag sem PDF fylgiskjal. Þegar sölupantanir eru að fullu bókaðar, er þær fjarlægður af lista sölupantana og skipt út fyrir nýtt fylgiskjal á lista bókaðra sölureikninga og lista yfir bókaðar söluafhendingar.

## <a name="see-also"></a>Sjá einnig
[Sala](sales-manage-sales.md)  
[Uppsetning sölu](sales-setup-sales.md)  
[Birgðir](inventory-manage-inventory.md)  
[Senda skjöl í tölvupósti](ui-how-send-documents-email.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
