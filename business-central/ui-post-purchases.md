---
title: Hvernig skal bóka innkaupaskjöl | Microsoft Docs
description: Kynntu þér mismunandi bókunaraðferðir til að bóka innkaupaskjöl og hvernig hægt er að uppfæra bókuð skjöl.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.reviewer: edupont
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 78657265e45aa9eb01d56a65aab8366c24b3d39a
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/17/2020
ms.locfileid: "4756743"
---
# <a name="posting-purchases"></a>Bókun innkaupa
Í innkaupaskjali er hægt að velja milli eftirfarandi bókunaraðgerða:

* **Færsla**
* **Forskoðun bókunar**
* **Bóka og prenta**
* **Prófunarskýrsla**
* **Bóka runu**

Þegar innkaupaskjal er bókað eru reikningur lánardrottins, fjárhagurinn, birgðabókarfærslur og forðafærslur uppfærðar.

Fyrir hvert innkaupaskjal er innkaupafærsla stofnuð í töflunni **Fjárhagsfærsla**. Færsla er einnig stofnuð í lánardrottnareikningi í töflunni **færsla í lánardrottnabók** og fjárhagsfærsla er stofnuð í viðeigandi safnreikningi lánardrottna. Auk þess getur bókun pöntunarinnar leitt til VSK-færslu og fjárhagsfærslu fyrir afsláttarupphæðina. Hvort færsla vegna afsláttar er bókuð fer eftir því sem er í reitnum **Afsláttarbókun** á síðunni **Innkaupagrunnur**.

Fyrir hverja innkaupalínu eru eftirfarandi færslur búnar til:
- Færsla í töflunni **Birgðafærsla** ef innkaupalínan er af gerðinni **Vara**.
- Færsla í töflunni **Fjárhagsfærsla** ef innkaupalínurnar eru af gerðinni **Fjárhagsreikningur**
- Færsla í töflunni **Forðafærsla** ef innkaupalínan er af gerðinni **Forði**.

Þar að auki eru innkaupaskjöl alltaf skráð í töflunum **Innk.móttökuhaus** og **Innk.reikningshaus**.

Áður en byrjað er að bóka er hægt að prenta prófunarskýrslu sem er með öllum upplýsingum í innkaupapöntuninni og birtir hugsanlegar villur. Til að prenta skýrsluna er farið í flipann **Bókun** valin, og síðan **Prufuskýrsla**.

> [!IMPORTANT]  
>   Hægt er að stofna bæði móttöku og reikning þegar innkaupapöntun er bókuð. Það er hægt að gera samhliða eða hvort í sínu lagi. Einnig er hægt að mynda hlutamóttöku og gera hlutareikning með því að fylla út reitina **magnt til móttöku** og **magn til að reikningsfæra** í einstökum innkaupapöntunarlínum áður en bókað er. Bent er á að ekki er hægt að búa til reikning fyrir einhverju sem hefur ekki verið móttekið. Það er að segja, áður en hægt er að gera reikning verður móttaka að vera skráð, nema móttaka sé skráð um leið og reikningur er gerður.

Hægt er annað hvort að bóka, eða bóka og prenta. Ef valið er að bóka og prenta prentast skýrslan við bókun pöntunarinnar. Einnig er hægt að velja aðgerðina **Fjöldabóka** sem býður upp á að bóka nokkrar pantanir í einu. Frekari upplýsingar er að finna í [Bóka mörg skjöl á sama tíma](ui-batch-posting.md).

## <a name="viewing-ledger-entries"></a>Fjárhagsfærslur skoðaðar
Þegar bókun er lokið hverfa bókuðu innkaupalínurnar úr pöntuninni. Skilaboð segja til um hvenær bókun er lokið. Að þessu loknu má sjá bókuðu færslurnar í ýmsum af þeim síðum sem innihalda bókaðar færslur, eins og **Lánardrottnafærslur**, **Fjárhagsfærslur**, **Birgðabókafærslur**, **forðafærslur**, **Innkaupakvittanir** og **Bókaðir innkaupareikningar**.

Í flestum tilfellum er hægt að opna fjárhagsfærslur úr viðkomandi spjaldi eða skjali. Á síðunni **Lánardrottnaspjald** skal t.d. velja aðgerðina **Færslur**.

## <a name="editing-ledger-entries"></a>Fjárhagsfærslum breytt
Þú getur breytt ákveðnum reitum í bókuðum innkaupaskjölum, t.d. reitnum **Greiðslutilvísun**. Frekari upplýsingar er að finna í [Breyta bókuðum skjölum](across-edit-posted-document.md). Til að fá fleiri mikilvæg svæði sem hafa áhrif á endurskoðunarslóðina þarf að bakfæra eða afturkalla bókun. Frekari upplýsingar er að finna í [Bakfæra bókanir í færslubók og afturkalla kvittanir/sendingar](finance-how-reverse-journal-posting.md).

## <a name="see-related-training-at-microsoft-learn"></a>Sjá tengda þjálfun á [Microsoft Learn](/learn/modules/receive-invoice-dynamics-d365-business-central/index)

## <a name="see-also"></a>Sjá einnig
[Breyta bókuðum skjölum](across-edit-posted-document.md)  
[Bóka mörg skjöl á sama tíma](ui-batch-posting.md)  
[Innkaup](purchasing-manage-purchasing.md)  
[Bókun skjala og færslubóka](ui-post-documents-journals.md)  
[Leiðrétta eða afturkalla ógreidda innkaupareikninga](purchasing-how-correct-cancel-unpaid-purchase-invoices.md)  
[Finndu síður og upplýsingar með Viðmótsleit](ui-search.md)  
[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]