---
author: edupont04
ms.service: dynamics365-business-central
ms.topic: include
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 7ead218d289668d893a659f730a4c64e31195f10
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5788555"
---
Þegar þú slærð inn dagsetningartíma, sem er dagsetning og tími sameinuð í eitt reit, verður þú að slá inn bil milli dagsetningar og tíma. Dagsetningarhlutinn getur aðeins innihaldið bil í formi opinbers dagsetningarskiltákns þinna svæðisstillinga. Tíminn getur innihaldið bil í kringum f.h./e.h. vísirinn í tengdum svæðisbundnum stillingum.

<!--It is also possible to enter only a date in a datetime field, but it is not possible to enter only a time.-->

Í eftirfarandi töflu birtast mismunandi leiðir til að færa inn dagsetningar og tímasetningar og hvernig þær eru túlkaðar:  

|Færsla|Túlkun|
|---------------|------------------------|
|08-01-2022 05:48:12 PM|08\-01\-2022 05:48:12 e.h.|
|131222 132455|13-12-22 13:24:55|
|1-12-22 10|01-12-22 10:00:00|
|1.12.22 5|01-12-22 05:00:00|
|1.12.22|01-12-22 00:00:00|
|11 12|11/gildandi mánuður/gildandi ár 12:00:00|
|1112 12|11/12/gildandi ár 12:00:00|
|d eða dagurinn í dag|dagurinn í dag 00:00:00|
|t tími|gildandi tími dagsins í dag|
|d 10:30|dagurinn í dag 10:30:00|
|d 03:03:03|dagurinn í dag 03:03:03|
|v eða vinnudagsetningin|vinnudagsetningin 00:00:00|
|m eða mánudagur|Mánudagur yfirstandandi viku 00:00:00|
|þr eða þriðjudagur|Þriðjudagur yfirstandandi viku 00:00:00|
|mi eða miðvikudagur|Miðvikudagur yfirstandandi viku 00:00:00|
|fi eða fimmtudagur|Fimmtudagur yfirstandandi viku 00:00:00|
|f eða föstudagur|Föstudagur yfirstandandi viku 00:00:00|
|l eða laugardagur|Laugardagur yfirstandandi viku 00:00:00|
|s eða sunnudagur|Sunnudagur yfirstandandi viku 00:00:00|
|þr 10:30:00|Þriðjudagur yfirstandandi viku 10:30:00|
|þr 03:03:03|Þriðjudagur yfirstandandi viku 03:03:03|
|Þ23 Þ|Þriðjudagur 23. viku vinnudagsetningarársins, núgildandi tími dagsins|
|þ23|Þriðjudagur 23. viku vinnudagsetningarársins|
|þ 23|Í dag 23:00:00|
|þ-1|Þriðjudagur 1. viku vinnudagsetningarársins|


