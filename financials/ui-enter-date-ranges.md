---
title: "Setja upp dagsetningabil í Finance and Operations, Business Edition | Microsoft Docs"
description: "Kynntu þér hvernig skal sækja skýrslu sem sýnir gögn frá ákveðnu tímabili með því að nota dagsetningartímabil í Finance and Operations, Business Edition."
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: dates, reporting, filter
ms.date: 05/29/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: da2fea4e095c8211f30aaa7c570a84a005e7cbc8
ms.contentlocale: is-is
ms.lasthandoff: 01/30/2018

---
# <a name="entering-date-ranges-in-finance-and-operations-business-edition"></a>Innsláttur dagsetningabils í Finance and Operations, Business Edition 
Hægt er að stilla afmarkanir með upphafs- og lokadegi til að birta aðeins gögn á tilteknu tímabili. Ákveðnar reglur gilda um hvernig tímabil eru stillt. Tökum sem dæmi **Topp 10 viðskiptavinir**:

![Stilla dagsetningartímabil á beiðnisíðunni fyrir topp 10 viðskiptavinir](./media/ui-enter-date-ranges/customer-top10-list.png)

Hér geturðu afmarkað skýrsluna við dagsetningartímabil eins og síðustu 2 vikur eða alls 6 vikur, eða hvaða tímabil sem þú vilt. Til að stilla dagsetningartímabil slærðu inn dagsetningar og notar svo annað hvort **..** eða **|** til að stilla tímabilið. Til að skoða topp 10 viðskiptavinina fyrstu 2 vikurnar í maí, til dæmis, myndirðu setja dagsetingarafmörkunina á *05 01 17..05 14 17*.
Hér eru nokkur fleiri dæmi:

| Merking | Dæmi | Ásamt færslum |
|---|---|---|
|Jafnt og| 12, 15, 16 |Einungis þær sem bókaðar eru 15. desember 2016.|
|Millibil| 12 15 16..01 15 17<br /><br />..12 15 16|Færslur sem eru bókaðar á dagsetningum á milli og með 15. desember 2016 og 15. janúar 2017.<br /><br />Þær sem eru bókaðar eru 15. desember 2016 og fyrr.|
|Annaðhvort eða|12 15 16&#124;12 16 16|Þær sem eru bókaðar annað hvort 15. eða 16. desember 2016. Ef færslur eru bókaðar báða dagana verða þær allar sýndar.|

Einnig má tengja grunnformin saman.

| Dæmi | Ásamt færslum |
|---|---|
|12 15 16&#124;12 01 16..05 31 17 | Færslur sem eru bókaðar annað hvort 15. desember 2016 eða á dagsetningum á milli og með 01. desember 2016 og 31. maí 2017. |
|12 14 16&#124;12 30 16 | Færslur bókaðar til og með 14. desember og færslur bókaðar frá og með 30. desember - það er, allar færslur nema þær sem voru bókaðar á dagsetningum á milli og með 15. og 29. desember. |

Athugið að við notuðum bandarískt dagsetningarsnið hér. Þegar [!INCLUDE[d365fin](includes/d365fin_md.md)] verður tiltækt á öðrum mörkuðum, muntu geta notað þau snið sem þú ert vanur.

## <a name="see-also"></a>Sjá einnig
[Unnið með [!INCLUDE[d365fin](includes/d365fin_long_md.md)]](ui-work-product.md)  
[Skilgreining skilyrða í síum](ui-enter-criteria-filters.md)  
[Almenn viðskiptavirkni](ui-across-business-areas.md)

