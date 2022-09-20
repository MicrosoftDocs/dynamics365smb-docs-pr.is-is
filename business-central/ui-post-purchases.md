---
title: Bóka innkaupaskjöl
description: Lærðu um mismunandi leiðir til að bóka innkaupaskjöl og hvernig á að uppfæra bókuð skjöl.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.reviewer: edupont
ms.search.form: ''
ms.date: 08/08/2022
ms.author: edupont
ms.openlocfilehash: 2f306fee236fda2bae4863e0e793239c2168f125
ms.sourcegitcommit: 8b95e1700a9d1e5be16cbfe94fdf7b660f1cd5d7
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/09/2022
ms.locfileid: "9461103"
---
# <a name="posting-purchases"></a>Bókun innkaupa

Í innkaupaskjali er hægt að velja milli eftirfarandi bókunaraðgerða:

* **Færsla**
* **Forskoðun bókunar**
* **Bóka og prenta**
* **Prófunarskýrsla**
* **Bóka runu**

Þegar innkaupaskjal er bókað er reikningur lánardrottins, Fjárhagur (fjárhags), birgðafærslurnar og forðafærslurnar uppfærðar.

Fyrir hvert innkaupaskjal er innkaupafærsla stofnuð í töflunni **Fjárhagsfærsla**. Færsla er einnig stofnuð í lánardrottnareikningi í töflunni **færsla í lánardrottnabók** og fjárhagsfærsla er stofnuð í viðeigandi safnreikningi lánardrottna. Að auki getur bókun innkaupa leitt til virðisaukafærslu (VSK-færsla) og fjárhagsfærslu fyrir afsláttarupphæðina. Hvort færsla vegna afsláttar er bókuð fer eftir því sem er í reitnum **Afsláttarbókun** á síðunni **Innkaupagrunnur**.

Fyrir hverja innkaupalínu þar sem við á eru færslur stofnaðar í:

* **Töflunni Birgðafærsla** ef innkaupalínan er af **vörugerðinni**.
* **Töflunni Fjárhagsfærsla** ef innkaupalínan er af **tegundinni Fjárhagsreikningur**.
* **Töflunni forðafærsla** ef innkaupalínan er af **forðagerð**.

Þar að auki eru innkaupaskjöl alltaf skráð í töflunum **Innk.móttökuhaus** og **Innk.reikningshaus**.

Áður en byrjað er að bóka er hægt að prenta prófunarskýrslu sem er með öllum upplýsingum í innkaupapöntuninni og birtir hugsanlegar villur. Til að prenta skýrsluna er farið í flipann **Bókun** valin, og síðan **Prufuskýrsla**.

> [!IMPORTANT]  
> Hægt er að stofna bæði móttöku og reikning þegar innkaupapöntun er bókuð. Það er hægt að gera samhliða eða hvort í sínu lagi. Einnig er hægt að mynda hlutamóttöku og gera hlutareikning með því að fylla út reitina **magnt til móttöku** og **magn til að reikningsfæra** í einstökum innkaupapöntunarlínum áður en bókað er. Athugið að ekki er hægt að stofna innkaupareikning úr innkaupapöntun fyrir vörur eða þjónustu sem ekki hefur verið móttekið. Það er að segja, áður en hægt er að gera reikning verður móttaka að vera skráð, nema móttaka sé skráð um leið og reikningur er gerður.
>
> Ef bóka á innkaupareikning án þess að taka upp innkaupamóttöku í [!INCLUDE[prod_short](includes/prod_short.md)] skal stofna skjalið á **síðunni innkaupareikningar**. Frekari upplýsingar um [skráningu innkaupa með innkaupareikningum](purchasing-how-record-purchases.md).

Hægt er annað hvort að bóka, eða bóka og prenta. Ef valið er að bóka og prenta prentast skýrslan við bókun pöntunarinnar. Einnig er hægt að velja **aðgerðina Bóka runuvinnslu** til að bóka nokkrar pantanir á sama tíma. Frekari upplýsingar í [Bóka mörg skjöl á sama tíma](ui-batch-posting.md).

## <a name="viewing-ledger-entries"></a>Eignafærslur skoðaðar

Þegar bókun er lokið hverfa bókuðu innkaupalínurnar úr pöntuninni. Skilaboð segja til um hvenær bókun er lokið. Að því loknu er hægt að skoða bókuðu færslurnar á ýmsum síðum, þar á **meðal lánardrottnafærslur**, **·** **fjárhagsfærslur, birgðafærslur** **, forðafærslur** **, innkaupafærslur** og **síður bókaðar innkaupareikninga.**

Í flestum tilfellum er hægt að opna fjárhagsfærslur úr viðkomandi spjaldi eða skjali. Á síðunni **Lánardrottnaspjald** skal t.d. velja aðgerðina **Færslur**.

## <a name="editing-ledger-entries"></a>Ritfærslufærslum breytt

Þú getur breytt ákveðnum reitum í bókuðum innkaupaskjölum, t.d. reitnum **Greiðslutilvísun**. Frekari upplýsingar er að [breyta bókuðum fylgiskjölum](across-edit-posted-document.md). Til að fá fleiri mikilvæg svæði sem hafa áhrif á endurskoðunarslóðina þarf að bakfæra eða afturkalla bókun. Frekari upplýsingar í [Bakfæra færslubók bókanir og afturkalla móttökur/afhendingar](finance-how-reverse-journal-posting.md).

## <a name="see-related-training-at-microsoft-learn"></a>Sjá tengdar þjálfun kl [Microsoft Learn](/learn/modules/receive-invoice-dynamics-d365-business-central/index).

## <a name="see-also"></a>Sjá einnig .

[Breyta bókuðum skjölum](across-edit-posted-document.md)  
[Bóka mörg skjöl á sama tíma](ui-batch-posting.md)  
[Innkaup](purchasing-manage-purchasing.md)  
[Bókun skjala og færslubóka](ui-post-documents-journals.md)  
[Leiðrétta eða afturkalla ógreidda innkaupareikninga](purchasing-how-correct-cancel-unpaid-purchase-invoices.md)  
[Finndu síður og upplýsingar með Viðmótsleit](ui-search.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
