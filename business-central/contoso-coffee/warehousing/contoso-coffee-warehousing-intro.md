---
title: Kynning á Contoso-kaffi
description: Yfirlit yfir atburðarásir um hvernig gögn contoso-kaffisins geta hjálpað þér að læra hvernig á að nota vörubúnaðinn í Business Central.
ms.date: 04/01/2022
ms.topic: article
ms.service: dynamics-365-business-central
ms.search.form: 4764
author: brentholtorf
ms.author: bholtorf
---

# <a name="introduction-to-contoso-coffee-warehousing"></a>Kynning á Contoso Coffee Warehousing

Contoso Coffee er skáldað fyrirtæki sem framleiðir kaffivélar fyrir neytendur og fyrirtæki. Contoso-kaffiforritin **fyrir** Business Central bæta við kynningugögnum sem hægt er að nota til að læra hvernig á að nota vöruvörugetu í Business Central. Hægt er að grunnstilla vöruhúsaaðgerðir á ýmsa vegu, sjá [Yfirlit yfir mismunandi valkosti grunnstillingar](../../design-details-warehouse-management.md#overview-of-different-configuration-options).

Forritið veitir þrjár staðsetningar sem eru bjartsýni fyrir mismunandi aðstæður:

- **SILFUR**  

  Þessi birgðageymsla er grunnstillt til að nota hólf. Það er auðvelt að grunnstilla til að styðja grunn- eða háþróaða. 

- **GULUR**  

  Þessi birgðageymsla notar ítarlega vöruhúsaskilgreiningu en notar ekki hólf. Hægt er að endurstilla hana til að styðja grunnstillingar.

- **HVÍTUR**  

  Þessi birgðageymsla notar Ítarlegt vöruhús með beinum frágangi og tínslum sem gerir ítarlegri reglur kleift að færa vörur um vöruhúsið.

## <a name="set-up-contoso-coffee-warehousing-data"></a>Uppsetning Contoso Coffee Warehousing gagna

[!INCLUDE [contoso-coffee-app-install](../../includes/contoso-coffee-app-install.md)]

Þegar viðkomandi forrit hafa verið sett upp er farið á [síðuna Contoso Demo Tool](https://businesscentral.dynamics.com/?page=5194) í [!INCLUDE [prod_short](../../includes/prod_short.md)], línan Vöruhúsaeining *valin* og aðgerðin **Grunnstilla** til að undirbúa einingarnar. Eftirfarandi töflur lýsa stillingunum.  

|Svæði  |Heimildasamstæða  |
|---------|---------|
|**Hólf birgðageymslu**  |Staðsetningin sem nota á fyrir grunnstaðsetningar.|
|**Ítarlegt birgðageymsla**  |Staðsetningin sem nota á fyrir einföld skipulagssvið.|
|**Birgðageymsla beinn frágangur og tínsla**  |Staðsetningin sem nota á fyrir ítarlegar skipulagsaðgerðir.|
|**Millifærslustaður**  |Staðsetningin sem nota á fyrir millifærslustaðinn í millifærsluaðstæðum.|
|**Númer viðskiptamanns**  |Viðskiptavinurinn sem á að nota í grunn- og einföldum aðstæðum í söluaðgerðum.|
|**Nr. lánardrottins**  |Lánardrottinn sem á að nota fyrir öll dæmi í innkaupaaðgerðum.|
|**Vara 1 nr.**  |Aðalatriðið sem á að nota í öllum tilfellum.|
|**Vörunr.**  |Aukaatriðið sem á að nota í öllum tilfellum.|
|**Nr. vöru 3**  |Varan með rakningu.|

Þegar allt er til reiðu skaltu velja aðgerðina **Búa til sýnigögn**. Það tekur nokkrar mínútur að bæta gögnunum við undirliggjandi gagnagrunn en eftir það er allt til reiðu til að keyra ýmsar aðstæður.  

> [!IMPORTANT]
> Ef aðstæður eru keyrðar gæti verið ráðlegt að staðfesta að notandanum hafi verið bætt við fyrir tilteknar birgðageymslur. Nánari upplýsingar eru [í Setja upp vöruhúsastarfsmenn](../../warehouse-how-to-set-up-warehouse-employees.md).

## <a name="scenarios"></a>Dæmi

The Contoso Coffee warehousing kynningargögnin sem nú styðja við eftirfarandi aðstæður til prófunar og þjálfunar:

1.  [Kynning á flæði á inn- og útleið í Grunngrunnstilling vöruhúss](warehouse-basic-flow-putaway-pick.md)
2.  [Kynning á flæði inn og út í blandað vöruhús grunnstillingar](warehouse-mixed-flow-receive-pick-ship.md)
3.  [Kynning á flæði inn og út í Ítarleg vöruhús grunnstilling með beinum frágangi og tínslu](warehouse-directed-flow.md)

Lestu skrefin fyrir hverjar aðstæður í viðkomandi grein.  

## <a name="see-also"></a>Sjá einnig .

[Uppsetning birgða](../../inventory-setup-inventory.md) 
[Hvernig á að setja upp birgðageymslur](../../inventory-how-setup-locations.md) 
[Vörugeymsla](../../warehouse-manage-warehouse.md) 
[Hönnunarupplýsingar](../../design-details-warehouse-overview.md) 
