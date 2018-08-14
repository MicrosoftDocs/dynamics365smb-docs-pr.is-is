---
title: "Uppsetning dagsetningatímabils í Business Central | Microsoft Docs"
description: "Kynntu þér hvernig skal sækja skýrslu sem sýnir gögn frá ákveðnu tímabili með því að nota dagsetningartímabil í Business Central."
documentationcenter: 
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: dates, reporting, filter
ms.date: 07/05/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: d7664360941313da6ea0b797ef00df2e9810ad62
ms.openlocfilehash: ff63ae71a78f956dddb7b5247ee66f9416cf7cf1
ms.contentlocale: is-is
ms.lasthandoff: 07/09/2018

---
# <a name="entering-date-ranges"></a>Færa inn dagsetningartímabil
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

## <a name="using-date-formulas"></a>Notkun dagsetningarreiknireglna
Dagsetningarregla er stutt, skammstöfuð samsetning stafa og tölustafa sem tilgreinir hvernig skal reikna út dagsetningar. Hægt er að færa dagsetningarreiknireglur í ólíka dagsetningarreiknireiti og í ítrekunartíðnireiti í ítrekunarbókum.

> [!NOTE]
>  Dagurinn í dag, fyrir upphaf tímabilsins, er með í öllum reitum fyrir reiknireglur dagsetninga. Samkvæmt því, ef til dæmis fært er inn **1W** er tímabilið í raun átta dagar þar sem dagurinn í dag er tekinn með. Til að tilgreina sjö daga tímabil (eina raunviku) að meðtalinni upphafsdagsetningu tímabilsins þarf að færa inn **6D** eða **1W\-1D**.

Hér eru nokkur dæmi um hvernig nota má dagsetningarreiknireglur:

-   Dagsetningarreikniregla í ítrekunartíðnireitnum í ítrekunarbókum ákvarðar hversu oft færsla í færslubókarlínu er bókuð.

-   Dagsetningarreikniregla í reitnum **Biðtími** fyrir tiltekið innheimtustig ákvarðar það tímabil sem þarf að líða frá gjalddaga (eða frá gjalddaga fyrra innheimtubréfs) áður en innheimtubréf er búið til.

-   Dagsetningarreikniregla í reitnum **Gjalddagaútreikningur** ákvarðar hvernig á að reikna gjalddaga í innheimtubréfinu.

Dagsetningarreikniregla getur mest haft 20 stafi, bæði tölu- og bókstafi. Hægt er að nota eftirfarandi stafi sem skammstafanir fyrir tiltekinn tíma.

|  Stafur  |  Upplýsingar um tíma  |
|----------|----------------------|
|U|Opið|
|D|Dagur\(s\)|
|V|Vika\(s\)|
|M|Mánuður\(s\)|
|F|Fjórðungur\(s\)|
|Á|Ár\(s\)|

Hægt er að rita dagsetningarreiknireglu á þrjá vegu.

Eftirfarandi dæmi sýnir hvernig á að nota **U**, fyrir líðandi, og tímaeiningu.

|  Segð  |  Merking  |
|--------------|-----------|
|LV|Líðandi vika|
|LM|Líðandi mánuður|

Eftirfarandi dæmi sýnir hvernig á að nota tölueiningu og tíma. Talan getur ekki verið hærri en 9999.

|  Segð  |  Merking  |
|--------------|-----------|
|10D|10 dögum eftir daginn í dag|
|2V|2 vikum eftir daginn í dag|

Eftirfarandi dæmi sýnir hvernig á að nota tímaeiningu og tölu.

|  Segð  |  Merking  |
|--------------|-----------|
|D10|Næsti 10. dagur mánaðar|
|VD4|Næsti fjórði dagur viku \(fimmtudagur\)|

Eftirfarandi dæmi sýnir hvernig eigi að samræma þessi þrjú eyðublöð eins og þörf er á.

|  Segð  |  Merking  |
|--------------|-----------|
|LM\+10D|Líðandi mánuður \+ 10 dagar|

Eftirfarandi dæmi sýnir hvernig hægt er að nota mínustákn til að sýna gamla dagsetningu.

|  Segð  |  Merking  |
|--------------|-----------|
|-1Á|1 ári fyrir daginn í dag|

> [!IMPORTANT]
>  Ef staðsetningin notar grunndagatal, er dagsetningarreiknireglan sem er til dæmis færð inn í reitinn **Afhendingartími** túlkuð samkvæmt vinnudögum. Til dæmis þýðir **1V** sjö vinnudagar.

## <a name="see-also"></a>Sjá einnig
[Unnið með [!INCLUDE[d365fin](includes/d365fin_long_md.md)]](ui-work-product.md)  
[Dagsetning útreiknings fyrir kaup.](purchasing-date-calculation-for-purchases.md)  
[Skilgreining skilyrða í síum](ui-enter-criteria-filters.md)  

