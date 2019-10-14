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
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 0fccda42a69cd1d1d7129380518890fac5b8986c
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/01/2019
ms.locfileid: "2315085"
---
# <a name="posting-purchases"></a>Bókun innkaupa
Í **bókunarflokki** á innkaupaskjali er hægt að velja milli eftirfarandi bókunaraðgerða:

* **Færsla**
* **Forskoðun bókunar**
* **Bóka og prenta**
* **Prófunarskýrsla**
* **Bóka runu**

Þegar lokið hefur verið við allar línurnar og allar upplýsingar færðar á innkaupapöntunina er hægt að bóka hana, það er að segja stofna móttöku og reikning.

Þegar innkaupapöntun er bókuð, eru reikningur lánardrottins, fjárhagurinn og birgðahöfuðbókarfærslur uppfærðar.

Innkaupafærsla er stofnuð í töflunni  **Fjárhagsfærsla** fyrir hverja innkaupapöntun. Færsla er einnig stofnuð í lánardrottnareikningi í töflunni **færsla í lánardrottnabók** og fjárhagsfærsla er stofnuð í viðeigandi safnreikningi lánardrottna. Auk þess getur bókun pöntunarinnar leitt til VSK-færslu og fjárhagsfærslu vegna afsláttar. Hvort færsla vegna afsláttar er bókuð fer eftir því sem er í reitnum **Afsláttarbókun** á síðunni **Innkaupagrunnur**.

Birgðafærsla er stofnuð í töflunni  **birgðafærsla** fyrir hverja innkaupapöntunarlínu (ef innkaupalínurnar eru með vörunúmerum) eða þá að fjárhagsfærsla er stofnuð í töflunni **Fjárhagsfærsla** (ef fjárhagsreikningur er í innkaupalínunum). Þar að auki eru innkaupapantanir alltaf skráðar í töflunum **Innk.móttökuhaus** og **Innk.reikningshaus** .

Áður en byrjað er að bóka er hægt að prenta prófunarskýrslu sem er með öllum upplýsingum í innkaupapöntuninni og birtir hugsanlegar villur. Til að prenta skýrsluna er farið í flipann **Bókun**valin, og síðan **Prufuskýrsla**.

> [!IMPORTANT]  
>   Hægt er að stofna bæði móttöku og reikning þegar pöntun er bókuð. Það er hægt að gera samhliða eða hvort í sínu lagi. Einnig er hægt að mynda hlutamóttöku og gera hlutareikning með því að fylla út reitina **magnt til móttöku** og **magn til að reikningsfæra** í einstökum innkaupapöntunarlínum áður en bókað er. Bent er á að ekki er hægt að búa til reikning fyrir einhverju sem hefur ekki verið móttekið. Það er að segja, áður en hægt er að gera reikning verður móttaka að vera skráð, nema móttaka sé skráð um leið og reikningur er gerður.

Hægt er annað hvort að bóka, eða bóka og prenta. Ef valið er að bóka og prenta prentast skýrslan við bókun pöntunarinnar. Einnig er hægt að velja aðgerðina **Fjöldabóka** sem býður upp á að bóka nokkrar pantanir í einu. Frekari upplýsingar er að finna í [Bóka mörg skjöl á sama tíma](ui-batch-posting.md).

Þegar bókun er lokið hverfa bókuðu innkaupalínurnar úr pöntuninni. Skilaboð segja til um hvenær bókun er lokið. Að þessu loknu má sjá bókuðu færslurnar í ýmsum af þeim síðum sem innihalda bókaðar færslur, eins og **Lánardrottinsfærslur**, **Fjárhagsfærslur**, **Birgðafærslur**, **Innkaupaafhendingar** og **Bókaðir innkaupareikningar** síður.

Þú getur breytt ákveðnum reitum í bókuðum innkaupaskjölum, t.d. reitnum **Greiðslutilvísun**. Frekari upplýsingar er að finna í [Breyta bókuðum skjölum](across-edit-posted-document.md).

## <a name="see-also"></a>Sjá einnig
[Breyta bókuðum skjölum](across-edit-posted-document.md)  
[Bóka mörg skjöl á sama tíma](ui-batch-posting.md)  
[Innkaup](purchasing-manage-purchasing.md)  
[Bókun skjala og færslubóka](ui-post-documents-journals.md)  
[Leiðrétta eða afturkalla ógreidda innkaupareikninga](purchasing-how-correct-cancel-unpaid-purchase-invoices.md)  
[Finndu síður og upplýsingar með Viðmótsleit](ui-search.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
