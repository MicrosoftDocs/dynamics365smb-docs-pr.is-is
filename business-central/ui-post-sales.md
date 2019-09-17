---
title: Bókun söluskjala | Microsoft Docs
description: Kynntu þér mismunandi bókunaraðferðir til að bóka söluskjöl og hvernig hægt er að uppfæra bókuð skjöl.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.reviewer: edupont
ms.date: 08/27/2019
ms.author: sgroespe
ms.openlocfilehash: a2eb27a541033b755b9ab9d4ea9156bf7de9cab4
ms.sourcegitcommit: f46793abdb3efd8384c10eb7992e076383251f2c
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/27/2019
ms.locfileid: "1921431"
---
# <a name="posting-sales"></a>Sölubókun
Undir valmyndinni **Bókun** í söluskjali er hægt að velja milli eftirfarandi bókunaraðgerða:

* **Færsla**
* **Bóka og nýtt**
* **Bóka og senda**
* **Forskoðun bókunar**
* **Reikningsdrög**
* **Bráðabirgðareikningur**
* **Prófunarskýrsla**

Þegar lokið hefur verið við allar línurnar og allar upplýsingar færðar á sölupöntunina er hægt að bóka hana. Þetta stofnar afhendingu og reikning.

Þegar sölupöntun er bókuð, eru reikningur viðskiptavinar, fjárhagurinn og birgðahöfuðbókarfærslur uppfærðar.

Sölufærsla er stofnuð í töflunni G/L Entry **fjárhagsfærsla** fyrir hverja sölupöntun. Færsla er einnig stofnuð í reikningi viðskiptamanns í töflunni **sérsniðin fjárhagsfærsla** og fjárhagsfærsla er stofnuð í viðeigandi safnreikningi viðskiptamanns. Auk þess getur bókun pöntunarinnar leitt til VSK-færslu og fjárhagsfærslu vegna afsláttar. Hvort færsla vegna afsláttar er bókuð fer eftir því sem er í reitnum **Afsláttarbókun** á síðunni **Sölugrunnur**.

Birgðafærsla er stofnuð í töflunni **birgðafærsla** fyrir hverja sölupöntunarlínu (ef línurnar eru með vörunúmerum) eða þá að fjárhagsfærsla er stofnuð í töflunni **Fjárhagsfærsla** (ef fjárhagsreikningur er í sölulínunum). Auk þess eru sölupantanir alltaf skráðar í töflunum **Söluafhendingarhaus** og **Sölureikningshaus**.

> [!IMPORTANT]  
>   Þegar pöntun er bókuð er hægt að búa til bæði afhendingu og reikning. Það er hægt að gera á sama tíma eða hvort í sínu lagi. Einnig er hægt að mynda hlutaafhendingu og gera hlutareikning með því að fylla út reitina **magn til að flytja** og/eða **magn til að reikningsfæra** í einstökum sölupöntunarlínum áður en bókað er. Bent er á að ekki er hægt að búa til reikning fyrir eitthvað sem ekki er afhent. Það er að segja, áður en hægt er að gera reikning verður afhending að vera skráð, nema afhending sé skráð um leið og reikningur er gerður.

Þegar bókun er lokið hverfa bókuðu sölulínurnar úr pöntuninni. Skilaboð segja til um hvenær bókun er lokið. Að þessu loknu verður hægt að sjá bókuðu færslurnar í ýmsum af þeim síðum sem innihalda bókaðar færslur, eins og **Viðskiptamannafærslur**, **Fjárhagsfærslur**, **Birgðafærslur,**, **Bókuð söluafhending** og **Bók. sölureikningur**.  

Þú getur breytt tilteknum reitum í bókuðum söluskjölum, t.d. **Rakningarnúmer pakka**. . Frekari upplýsingar er að finna í [Breyta bókuðum skjölum](across-edit-posted-document.md).

## <a name="see-also"></a>Sjá einnig
[Sala](sales-manage-sales.md)  
[Breyta bókuðum skjölum](across-edit-posted-document.md)  
[Senda skjöl í tölvupósti](ui-how-send-documents-email.md)  
[Ógreiddir sölureikningar leiðréttir eða afturkallaðir](sales-how-correct-cancel-sales-invoice.md)  
[Nota Viðmótsleit til að finna eiginleika og upplýsingar](ui-search.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
