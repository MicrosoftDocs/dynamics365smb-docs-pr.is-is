---
author: edupont04
ms.service: dynamics365-business-central
ms.topic: include
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: e75327e1c87af593d8e3f7e4f95e74349fb3a63c
ms.sourcegitcommit: 2c972dfc94d27245eaa99efcf638d030dedafb22
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/09/2022
ms.locfileid: "8104042"
---
Eftirfarandi tafla lýsir sumum helstu skýrslunum í skýrslugerð viðskiptakrafna.

| Skýrsla | Kenni hlutar | Description |
|--|--|--|
| **Aldursgreindar kröfur** | 120 | Sýnir útistandandi upphæð hjá viðskiptavinum skipt niður á tímabil fyrir gjaldfallna tímann. Skýrslan sýnir einnig þann hluta af stöðu viðskiptavinar sem er ekki gjaldfallin og er hægt að sýna með eða án upplýsinga um skjal fyrir hvern viðskiptavin. Þessi skýrsla er aðalskýrslan til að afstemma viðskiptavinabók við fjárhagsbók. Að því gefnu að þú hafir ekki heimilað beina bókun á lyklunum sem notaðir eru viðskiptakröfulyklum viðskiptavinabókunarflokks, er þessi skýrsla lýsing á upphæðunum sem þú finnur í fjárhagsbókinni. |
| **Yfirlit viðskiptavinar** | 1316 | Býr til viðskiptavinayfirlit fyrir tiltekið tímabil. Það er venjulega sent til viðskiptavina til að gefa þeim yfirlit yfir útistandandi upphæðir og einnig til áminningar um að greiða gjaldfallnar upphæðir. Hægt er að velja að birta gjaldfallnar upphæðir í öðrum hluta. Þú getur tekið með aldursgreiningartímabil svipað og það sem er notað í skýrslunni **Aldursgreindar viðskiptakröfur**. Fyrir aldursgreiningartímabil er yfirleitt stillt á *30D* sem þýðir 30 daga tímabil eins og 30, 60, 90 og 90+ daga fram yfir, frá lokadagsetningu, eða *1M+NM* sem verður núverandi mánuður á aðskildu tímabili og síðan mánaðarleg tímabil fyrir næstu mánuði. **Athugaðu**: í lista yfir viðskiptavini hefur þessi skýrsla einnig aðskilda aðgerð: **Tímasett yfirlit**. Þessi valkostur síast ekki á viðskiptavininn sem þú hefur valið. Þetta er sama skýrslan en notuð þegar þú vilt senda yfirlit til allra/fleiri viðskiptavina. |
| **Viðskiptavinur - staða til dags.** | 121 | Sýnir opnar fjárhagsfærslur viðskiptavinar fram að lokadagsetningunni. Þessi skýrsla sýnir svipað efni og yfirlit viðskiptavinar en með engri vísun ef færslan er komin fram yfir. **Athugið**: Dagsetningasían verður notuð á ítarlegar færslur í viðskiptavinabókinni. Þetta þýðir að ef þú ert með greiðslur á eftir lokadagsetningunni sem hafa verið notaðar í reikningum innan dagsetningabilsins munu reikningarnir birtast í skýrslunni því að þeim hefur ekki verið lokað eftir lokadagsetningu. |
| **Viðskiptamaður - Prófjöfnuður** | 129 | Sýnir nettóbreytingar fyrir viðskiptavin fyrir tímabilið sem tilgreint er í dagsetningasíunni ásamt nettóbreytingu það sem af er ári fyrir reikningsárið sem samsvarar völdu tímabili. Skýrslan er flokkuð eftir viðskiptavinabókunarflokkum og mun sýna annað yfirlit yfir viðskiptavinabókina en skýrslan **Aldursgreindar viðskiptakröfur**. **Athugið**: Ef þú hefur ekki sett upp neitt reikningstímabil veit kerfið ekki hvaða reikningsár á að nota og mun annaðhvort sýna það sem af er ári frá nýjasta reikningsárinu sem er skilgreint eða einfaldlega velja tímabilið sem er eða er ekki frá upphafi árs.|
| **Viðskiptavinur – Upplýsingar um prófjöfnuð** | 104 | Sýnir allar færslur í viðskiptavinabókinni innan tilgreindu dagsetningasíunnar. Þessi skýrsla er almennt notuð til að ganga úr skugga um að gerð sé grein fyrir öllum færslum fyrir tiltekinn viðskiptavin eða aðrar innri athuganir á viðskiptavinabókum. |
| **Viðskiptavinur - Greiðslukvittun** | 211 | Býr til greiðslukvittun fyrir hverja færslu í viðskiptavinabók af gerðinni **Greiðsla**. Ef greiðslan hefur verið notuð á reikninga verða reikningarnir tilgreindir; annars verður bara gefið upp að greiðsluupphæðin sé ójöfnuð. Þessi skýrsla er notuð til að senda viðskiptavinum sem vilja gögn um móttöku greiðslu.|
| **Afstemma viðskiptavina- og lánardrottnalykla** | 33 |Sýnir fjárhagsfærslur sem vera til vegna bókunar á viðskiptavina- og lánardrottnafærslum skipt eftir fjárhagslykli og bókunarflokkum. Þessi skýrsla er notuð til að afstemma stöður í viðskiptavina- og lánardrottnabókum við fjárhagsstöðu. |
| **Viðskiptavinur – Einföld samantekt aldursgreiningar**| 109 |Þetta er eldri útgáfa af aldursgreiningarskýrslu viðskiptakrafna. Við mælum með því að þú notir skýrsluna **Aldursgreindar viðskiptaröfur** í staðinn. |
| **Söluupplýsingar** |112  |[!INCLUDE [reports-sales-statistics](reports-sales-statistics.md)]<br>Þessa skýrslu er einnig hægt að nota í viðskiptakröfum þar sem auðveldara er að fletta hratt upp bókuðum greiðslum, afsláttum og sölum fyrir tiltekinn viðskiptavin.|
|**Viðskiptavinalisti**|101| Sýnir ýmsar grunnupplýsingar um viðskiptamenn, svo sem bókunarflokk viðskiptamanna, afsláttarflokk, vexti og greiðsluupplýsingar, sölumann, sjálfgefinn gjaldmiðil viðskiptamanns og hámarksskuld í staðbundnum gjaldmiðli (SGM), ásamt gildandi stöðu viðskiptamanns (í SGM). Skýrsluna má til dæmis nota til að viðhalda upplýsingum í töflunni Lánardrottinn.|
