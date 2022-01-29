---
title: Skýrslur og greiningar viðskiptaskulda
description: Finnið út hvaða skýrslur og greiningar eru í boði í staðlaðri útgáfu Business Central til að halda utan um viðskiptaskuldir.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: reporting
ms.search.form: 347
ms.date: 07/13/2021
ms.author: edupont
ms.openlocfilehash: edb3b32f88198d8e21aa2bfddafc1b7f319be9de
ms.sourcegitcommit: e008b3d7003c256475d6c606e5f7c9866a6bbb72
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 01/10/2022
ms.locfileid: "7953385"
---
# <a name="accounts-payable-reports-and-analytics-in-business-central"></a>Skýrslur og greiningar viðskiptaskulda í Business Central

Til að hjálpa þér að hafa umsjón með viðskiptaskuldum í [!INCLUDE [prod_short](includes/prod_short.md)] eru staðlaðar skýrslur og greiningar innbyggðar. Það býður upp á fleiri valkosti en hefðbundið skýrslugerð skorður til að hjálpa að hanna mismunandi gerðir af skýrslum.  

## <a name="reports"></a>Skýrslur

Eftirfarandi tafla lýsir sumum helstu skýrslunum í skýrslugjöf viðskiptaskulda.

| Skýrsla | Kenni hlutar | Description |
|--|--|--|
| **Aldursgreindar skuldir** | 322|Sýnir gjaldfallnar stöður fyrir lánardrottna á gjaldföllnum tímabilum. Hægt er að sýna gjaldfallnar upphæðir eftir gjalddaga, bókunardag eða dagsetningu skjals eftir þörfum. Þú getur valið að sýna upphæðirnar í staðbundnum gjaldmiðli (SGM) og prenta út upplýsingar um gjaldfallin skjöl. Tímabilin geta verið með fyrirsagnir með dagsetningum eða með fjölda dagsetninga sem eru gjaldfallnar miðað við tilgreinda aldursgreiningu eftir gerð.<br>Þessi skýrsla er aðalskýrslan til að afstemma lánardrottnabók við fjárhagsbók. Að því gefnu að þú hafir ekki heimilað beina bókun á lyklunum sem notaðir eru viðskiptaskuldalyklum lánardrottnabókunarflokks, er þessi skýrsla lýsing á upphæðunum sem þú finnur í fjárhagsbókinni.|
| **Lánardr. - Staða til dags.** | 321 | Sýnir stöðu lánardrottins eftir lokadagsetningu á tilteknu dagsetningabili. Hægt er að velja að birta stöðu lánardrottins í staðbundnum gjaldmiðli (SGM). Veljið reitinn **Bæta við ónotaðar færslur** til að sýna færslur sem hafa verið lokaðar fyrir lokadagsetninguna en hafa verið teknar úr notkun (opnaðar) síðar. Veljið **Sýna færslur með núllstöðu** til að sýna lánardrottna með stöðuna núll eftir lokadagsetningunni í dagsetningasíunni. Dagsetningasían gildir um ítarlegar fjárhagsfærslur lánardrottins fyrir færslurnar í skýrslunni. Ef þú ert með greiðslur á eftir lokadagsetningunni sem hafa verið notaðar í reikningum innan dagsetningabilsins munu reikningarnir birtast í skýrslunni því að þeim hefur ekki verið lokað af lokadagsetningunni. |
| **Lánardrottinn – Prófjöfnuður** | 329 | Sýnir nettóbreytingar fyrir lánardrottna fyrir tímabilið sem tilgreint er í dagsetningasíunni ásamt nettóbreytingu það sem af er ári fyrir reikningsárið sem samsvarar völdu tímabili. Skýrslan er flokkuð eftir lánardrottnabókunarflokkum og mun sýna annað yfirlit yfir lánardrottnabókina en skýrslan **Aldursgreindar viðskiptaskuldir**. **Athugið**: Ef þú hefur ekki sett upp neitt reikningstímabil veit kerfið ekki hvaða reikningsár á að nota og mun annaðhvort sýna það sem af er ári frá nýjasta reikningsárinu sem er skilgreint eða einfaldlega velja tímabilið sem er eða er ekki frá upphafi árs.|
| **Lánardrottinn - Upplýsingar um prófjöfnuð** | 304 | Sýnir allar færslur lánardrottnabókar innan tiltekinnar dagsetningasíu. Skýrslan sýnir upphafsstöðu lánardrottins samkvæmt dagsetningasíunni. |
| **Innkaupaupplýsingar** |312 |[!INCLUDE [reports-purchase-statistics](includes/reports-purchase-statistics.md)]<br>Þessa skýrslu er einnig hægt að nota í viðskiptaskuldum þar sem auðveldara er að fletta hratt upp bókuðum greiðslum, afsláttum og öðrum færslum fyrir tiltekinn lánardrottin.|
|**Lánardr. - Samantekt aldursgreiningar**|305| Eldri skýrsla fyrir aldursgreindar viðskiptaskuldir. Mælt er með því að nota skýrsluna **Aldursgreindar viðskiptaskuldir** í staðinn. Hægt er að velja lengd tímabils og dagsetningu til að sem setta dagsetningu fyrir *gjaldfallið eftir*.|
|**Greiðslur í bið**|319|Sýnir færslur lánardrottnabókar þar sem reiturinn **Í bið** er auður.|
|**Fyrirframgreiðslubók lánardrottins**|317|Sýnir greiðslubókina með upplýsingum um greiðsluafslátt og greiðsluþol. Skýrsluna má nota til að athuga greiðslur áður en greiðsluskrár eru búnar til og færslubókin bókuð. **Athugaðu**: Skýrslan sýnir greiðsluafslætti á rangan hátt þegar margir kreditreikningar hafa verið notaðir í forriti. Í þessu tilviki er greiðsluafsláttur fyrir aukalega kreditreikninga sýndur sem afjöfnuð upphæð.|
|**Lánardrottinn - listi**|301|Sýnir ýmsar grunnupplýsingar um lánardrottna, svo sem bókunarflokk lánardrottins, afsláttar- og greiðsluupplýsingar, forgangsstig og sjálfgefinn gjaldmiðil lánardrottins ásamt gildandi stöðu lánardrottins (í SGM). Skýrsluna má til dæmis nota til að viðhalda upplýsingum í töflunni Lánardrottinn.|

## <a name="see-also"></a>Sjá einnig .

[Greina fjárhagsskýrslur í Microsoft Excel](finance-analyze-excel.md)  
[Unnið með víddir](finance-dimensions.md)  
[Eignaumsjón](fa-manage.md)  
[Yfirlit yfir staðbundna virkni](about-localization.md)  
[Endurskoðandi upplifun í [!INCLUDE[prod_long](includes/prod_long.md)]](finance-accounting.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
