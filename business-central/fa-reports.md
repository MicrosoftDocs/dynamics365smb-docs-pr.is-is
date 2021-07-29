---
title: Skýrslur og greiningar eigna
description: Finnið út hvaða skýrslur og greiningar eru í boði í staðlaðri útgáfu Business Central til að halda utan um eignir.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: reporting
ms.date: 07/13/2021
ms.author: edupont
ms.openlocfilehash: c28e62a2de51323e0a7dcd2f4b5ea26d5896d718
ms.sourcegitcommit: a486aa1760519c380b8cdc8fdf614bed306b65ea
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/13/2021
ms.locfileid: "6543349"
---
# <a name="fixed-assets-reports-and-analytics-in-business-central"></a>Skýrslur og greiningar eigna í Business Central

Til að hjálpa þér að hafa umsjón með eignum í [!INCLUDE [prod_short](includes/prod_short.md)] eru staðlaðar skýrslur og greiningar innbyggðar. Það býður upp á fleiri valkosti en hefðbundið skýrslugerð skorður til að hjálpa að hanna mismunandi gerðir af skýrslum.  

## <a name="reports"></a>Skýrslur

Eftirfarandi tafla lýsir sumum helstu skýrslunum í skýrslugerð vegna eigna.

| Skýrsla | Kenni hlutar | Description |
|--|--|--|
| **Eignalisti** | 5601 | Sýnir lista yfir eignir og upplýsingar um uppsetningu þeirra fyrir tiltekna afskriftabók. |
| **Eignir - Kauplisti** | 5608 | Telja upp allar eignir sem keyptar eru innan tiltekins dagsetningabils. Einnig er hægt að taka með eignir sem hafa verið stofnaðar en hafa ekki verið keyptar. |
| **Upplýsingar eignar** | 5604 | Sýnir fjárhagsfærslur eigna fyrir eignir. |
| **Greining eigna** | 5600 | Greiningarskýrsla þar sem hægt er að tilgreina tvo dagsetningardálka og þrjá gagnadálka til að sjá í skýrslunni. Til dæmis til að búa til skýrslu til að nota til stemma af við fjárhagsbókina skal bæta við dálkum fyrir kaupverð á lokadegi, afskriftum á lokadegi og bókfært virði á lokadegi. Athugunarskýrsla gæti verið með kaupum/nettóbreytingu, niðurfærslu/nettóbreytingu og uppfærslu/nettóbreytingu, þannig að hægt er að athuga llar breytingar á eign ef þörf krefur. Ef reiturinn **Áætlunarskýrsla** er valinn og lokadagsetning er tilgreind fram í tímann mun skýrslan reikna út framtíðarafskriftir og leggja fram mat á afskriftum og bókfærðu virði í framtíðinni ef þessir reitir voru valdir sem skýrsludálkar. |
| **Áætlað virði eignar** | 5607 | Sýnir áætlaðar afskriftarupphæðir og bókað virði fyrir tímabil fram í tímann fyrir eignir. Skýrslan kemur að gagni þegar verið er að nota mismunandi afskriftaraðferðir fyrir eignir og ætlunin er að leggja mat á afskrift næsta árs sem dæmi. Notaðu skýrsluna til að búa til fjárhagsáætlanir fyrir afskriftir með því að velja fjárhagsáætlun og reitinn **Afrita í fjárhagsáætlun**. |
| **Eignir, bókfært virði 01** | 5605 | Hér koma fram sundurliðaðar upplýsingar um kaupverð, virði afskriftar og bókfært virði einstakra eigna og eignaflokka. Fyrir hverja tegund reiknast upphæðir í upphafi og í lok tiltekins tímabils og tímabilið í heild. Ef reiturinn **Fjárhagsáætlunarskýrsla** er valinn mun skýrslan reikna út væntanlegar afskriftir fyrir tímabilið. Færðu inn *tegund flokks* ef þú vilt að skýrslan flokki eignirnar og prenti samtölur flokks. Ef til dæmis hafa verið settir upp sex eignaflokkar er valkosturinn *Eignaflokkur* valinn svo að samtölur flokks verði prentaðar fyrir hvern flokkunarkóðanna sex.|
| **Eignir, bókfært virði 02** | 5606 |Sýnir sundurliðun á bókfærðu virði eignar eftir breytingum á kaupum, afskriftum og hagnaði innan tímabilsins ásamt frekari sundurliðun eftir viðbótum og afföllum innan tímabilsins. Notaðu þessa skýrslu til að lýsa breytingum á eignum á tilteknu tímabili þegar margar mismunandi breytingar eiga sér stað á milli eignaflokka. Ef reiturinn **Fjárhagsáætlunarskýrsla** er valinn mun skýrslan reikna út væntanlegar afskriftir fyrir tímabilið. Færðu inn *tegund flokks* ef þú vilt að skýrslan flokki eignirnar og prenti samtölur flokks. Ef til dæmis hafa verið settir upp sex eignaflokkar er valkosturinn *Eignaflokkur* valinn svo að samtölur flokks verði prentaðar fyrir hvern flokkunarkóðanna sex. |
| **Fjárhagsgreining eignar**| 5610 |Sýnir greiningu á eignum með ýmsum gögnum bæði um einstakar eignir og/eða eignaflokka. Í flýtiflipanum Eignir er hægt að setja afmörkun ef í skýrslunni eiga aðeins að vera tilteknar eignir. Í flýtiflipanum Valkostir skal aðlaga skýrsluna þannig að hún uppfylli þínar kröfur. Skýrslan er svipuð skýrslunni **Eignir - Greining** en sérstaklega til að afstemma við fjárhagsbók og sérstaklega til að staðfesta afskráningarfærslur. Í skýrslunni er gert ráð fyrir að þú þekkir fjárhagsreikningana sem eru tilgreindir í uppsetningu bókunar. |
| **Skráning eignar** |5603  |Hér koma fram bókaðar eignafærslur sem eru flokkaðar og skipt niður eftir dagbókarnúmerum. Hægt er að tilgreina hvaða dagbókarfærslur eiga að koma fram með því að setja afmörkun. Mikilvægt er að setja afmörkun, því annars er hætta á flóði upplýsinga í skýrslunni. |

## <a name="see-also"></a>Sjá einnig .

[Greina fjárhagsskýrslur í Microsoft Excel](finance-analyze-excel.md)  
[Unnið með víddir](finance-dimensions.md)  
[Eignaumsjón](fa-manage.md)  
[Yfirlit yfir staðbundna virkni](about-localization.md)  
[Endurskoðandi upplifun í [!INCLUDE[prod_long](includes/prod_long.md)]](finance-accounting.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
