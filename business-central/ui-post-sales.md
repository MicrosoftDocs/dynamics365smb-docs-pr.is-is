---
title: Söluskjöl bókuð
description: Kynntu þér mismunandi bókunaraðferðir til að bóka söluskjöl og hvernig hægt er að uppfæra bókuð skjöl.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.reviewer: bholtorf
ms.search.form: '130, 142, 1350'
ms.date: 04/01/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="posting-sales"></a>Sölubókun

Undir valmyndinni **Bókun** í söluskjali er hægt að velja milli eftirfarandi bókunaraðgerða:

* **Færsla**
* **Bóka og nýtt**
* **Bóka og senda**
* **Forskoðun bókunar**
* **Bóka runu**
* **Prófunarskýrsla**

> [!NOTE]
> Fyrir sölupantanir er hægt að sjá valmöguleika sem tengjast fyrirframgreiðsluvirkni. Frekari upplýsingar er að finna í [Reikningsfærsla fyrirframgreiðslna](finance-invoice-prepayments.md).

Þegar lokið hefur verið við allar línurnar og allar upplýsingar færðar á sölupöntunina er hægt að bóka hana. Þetta stofnar afhendingu og reikning.

Þegar sölupöntun er bókuð, eru reikningur viðskiptavinar, fjárhagurinn og birgðahöfuðbókarfærslur uppfærðar.

Sölufærsla er stofnuð í töflunni G/L Entry **fjárhagsfærsla** fyrir hverja sölupöntun. Færsla er einnig stofnuð í reikningi viðskiptamanns í töflunni **sérsniðin fjárhagsfærsla** og fjárhagsfærsla er stofnuð í viðeigandi safnreikningi viðskiptamanns. Auk þess getur bókun pöntunarinnar leitt til VSK-færslu og fjárhagsfærslu vegna afsláttar. Hvort færsla vegna afsláttar er bókuð fer eftir því sem er í reitnum **Afsláttarbókun** á síðunni **Sölugrunnur**.

Birgðafærsla er stofnuð í töflunni **birgðafærsla** fyrir hverja sölupöntunarlínu (ef línurnar eru með vörunúmerum) eða þá að fjárhagsfærsla er stofnuð í töflunni **Fjárhagsfærsla** (ef fjárhagsreikningur er í sölulínunum). Auk þess eru sölupantanir alltaf skráðar í töflunum **Söluafhendingarhaus** og **Sölureikningshaus**.

[!INCLUDE [order-ship-invoice](includes/order-ship-invoice.md)]

Annaðhvort er hægt að bóka eða bóka og senda. Ef valið er að bóka og senda er PDF-skrá mynduð sem er þá hægt að senda. Einnig er hægt að velja aðgerðina **Fjöldabóka** sem býður upp á að bóka nokkrar pantanir í einu. Frekari upplýsingar er að finna í [Bóka mörg skjöl á sama tíma](ui-batch-posting.md).

## <a name="viewing-ledger-entries"></a>Fjárhagsfærslur skoðaðar

Þegar bókun er lokið hverfa bókuðu sölulínurnar úr pöntuninni. Skilaboð segja til um hvenær bókun er lokið. Að þessu loknu verður hægt að sjá bókuðu færslurnar í ýmsum af þeim síðum sem innihalda bókaðar færslur, eins og **Viðskiptamannafærslur**, **Fjárhagsfærslur**, **Birgðafærslur,**, **Bókuð söluafhending** og **Bók. sölureikningur**.  

Í flestum tilfellum er hægt að opna fjárhagsfærslur úr viðkomandi spjaldi eða skjali. Á síðunni **Viðskiptamannaspjald** skal t.d. velja aðgerðina **Fjárhagsfærslur**.

## <a name="editing-ledger-entries"></a>Fjárhagsfærslum breytt

Hægt er að breyta tilteknum reitum í bókuðum innkaupaskjölum, svo sem **Rakningarnúmer pakka** . Frekari upplýsingar er að finna í [Breyta bókuðum skjölum](across-edit-posted-document.md). Til að fá fleiri mikilvæg svæði sem hafa áhrif á endurskoðunarslóðina þarf að bakfæra eða afturkalla bókun. Frekari upplýsingar er að finna í [Bakfæra bókanir í færslubók og afturkalla kvittanir/sendingar](finance-how-reverse-journal-posting.md).

## <a name="see-also"></a>Sjá einnig

[Sala](sales-manage-sales.md)  
[Bóka mörg skjöl á sama tíma](ui-batch-posting.md)  
[Breyta bókuðum skjölum](across-edit-posted-document.md)  
[Senda skjöl í tölvupósti](ui-how-send-documents-email.md)  
[Ógreiddir sölureikningar leiðréttir eða afturkallaðir](sales-how-correct-cancel-sales-invoice.md)  
[Finndu síður og upplýsingar með Viðmótsleit](ui-search.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]  
