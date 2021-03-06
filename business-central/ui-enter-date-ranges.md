---
title: Innsláttur dagsetninga og tíma í Business Central | Microsoft Docs
description: Lærðu hvernig á að slá inn dagsetningar og tíma, þar á meðal ýmsar ábendingar um framleiðni, svo sem hraðskrift, segð og afmarkanir. Sía lista eða skýrslur niður í tiltekna dagsetningu eða tímabil.
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: dates, reporting, filter, calendar, shorthand, range
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 404c39cba663cebc4d9ab30126de97bd20cf7e8e
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5773531"
---
# <a name="working-with-calendar-dates-and-times"></a>Vinna með dagsetningar og tíma í dagatali

[!INCLUDE[prod_short](includes/prod_long.md)] býður upp á margar leiðir til að slá inn dagsetningar og tíma, þar með talin öflugar aðgerðir sem flýta fyrir gagnaskráningu eða hjálpa þér að skrifa flókna dagatalssegðir. Það eru ýmsar staðir í forritinu þar sem þú getur slegið inn dagsetningar og tíma í reitum. Til dæmis, í sölupöntun, getur þú stillt afhendingardagsetningu. Þegar verið er að afmarka lista eða skýrslugögn er hægt að slá inn dagsetningar og tíma til að staðsetja aðeins þau gögn sem þú hefur áhuga á.

## <a name="check-your-region-and-language-settings"></a>Athugaðu svæði og tungumálastillingar
**Mínar stillingar** síðan tilgreinir **Svæði** og **Tungumál** sem þú notar í forritinu. Þessar stillingar hafa áhrif á hvernig þú slærð inn dagsetningar og tíma.

-   **Svæði** stillingin ákvarðar hvernig dagsetningar, tímasetningar, númer og gjaldmiðlar eru sýndir eða forsniðnir.

-   Fyrir dagsetningamynstur sem fela í sér orð, tungumálið orðanna sem þú notar verða að vera í samræmi við **tungumál** stillinguna.

> [!NOTE]
> [!INCLUDE[prod_short](includes/prod_long.md)] notar gregoríska dagatalskerfið.

<!--
The following sections describe how you can enter dates, times, datetimes, durations, date ranges, and how you use date formulas.
-->

## <a name="entering-dates"></a>Dagsetningar færðar inn

Í dagsetningarreitinn getur þú slegið inn dagsetningu með því að nota staðlaða sniðið fyrir svæðisstillingu þína. Mismunandi svæði geta notað mismunandi skiltákn milli daga, mánaða og ára. Til dæmis, sum svæði nota bandstrik (mm-dd-áááá) og önnur nota áfram skástrik (mm/dd/áááá). Hins vegar getur þú notað hvaða skiltákn sem er, jafnvel bil, og dagsetningin verður sjálfkrafa breytt til að nota skiltákn sem passa við svæðið þitt.

Athugaðu að sniðið sem dagsetningar eru birtar á í prentuðum skýrslum eða skjölum sendum í tölvupósti eru ekki undir áhrifum af persónulegu vali þínu á svæðisstillingu.

Til að vinna á afkastameiri hátt með dagsetningar og tíma geturðu notað eitthvað af þeim aðferðum eða sniði sem lýst er í eftirfarandi köflum.

### <a name="picking-dates-from-the-calendar"></a>Velja dagsetningar úr dagatalinu

Allir reitir sem sýna dagbókartákn geta verið stilltar með dagsetningarvali dagatals. Til að birta dagsetningarval dagatals skaltu virkja dagatalstáknið eða ýta á Ctrl + Home flýtilykilinn í reitnum.

![Dagsetningasvæði](media/ui-date-field.png "Dæmi um dagsetningarreit")

Sjá einnig [Flýtilyklar í dagsetningarvali dagatals](keyboard-shortcuts.md#calendarshortcuts).

### <a name="day-week-year-pattern"></a>Dagur\-vika\-ár mynstur

Þú getur slegið inn dagsetningu sem vikudag og síðan vikunúmer og, ef þú vilt, ár. Til dæmis þýðir Mán25 eða mán25 mánudagur í viku 25. Ef þú slærð ekki inn ár er ár vinnudagsetningar notað.

Í stað þess að slá inn allt orðið fyrir vikudaginn getur þú slegið inn hluta af orðinu, með því að byrja á byrjuninni. Ef um er að ræða árekstur (eins og til dæmis f sem gæti verið fimmtudagur eða föstudagur) eru dagarnir metnir í samræmi við svæðisstillingu. Inntakið er fyrst metið út frá vinnudegi og deginum í dag einnig, svo hafðu þetta í huga þegar skammstafað er. Til dæmis þýðir d nú þegar í dag, svo það getur ekki þýtt þriðjudagur eða fimmtudagur.

Vikunúmersskemað er alltaf ISO 8601, þar sem vika 1 er vikan sem inniheldur 4. janúar, eða vikan sem inniheldur fyrsta fimmtudag ársins.

### <a name="digit-patterns"></a>Tölustafamynstur

Í dagsetningarreit má færa inn tvær, fjórar, sex eða átta tölur:

-   Ef aðeins tvær tölur eru færðar inn þá túlkar kerfið þær sem daginn og bætir við mánuði og ári vinnudagsetningar.

-   Ef færðar eru inn fjórar tölur þá túlkar kerfið þær sem daginn og mánuðinn og bætir við ári vinnudagsetningar. Röð dags og mánaðar ræðst af svæðisstillingum þínum. Jafnvel þótt svæðisstillingar þínar séu með árið fyrir daginn og mánuðinn eru fjórir tölustafir túlkaðir sem dagur og mánuður.

-   Ef sú dagsetning sem færa á inn er á bilinu 01/01/1930 til 31/12/2029 má færa árið inn í tveimur tölum; annars skal færa árið inn með fjórum tölum.

### <a name="today"></a>Í dag

Sláðu inn orðið fyrir daginn í dag, á tungumáli sem er stillt í **Tungumál**, sem stillir daginn á núverandi dagsetningu. Í stað þess að slá inn allt orðið geturðu slegið inn hluta af orðinu, með því að byrja á byrjuninni, eins og t eða ídag, svo lengi sem það er ekki líka byrjun annars orðs.

### <a name="period"></a>Tímabil

Til að sía á tilteknu fjárhagstímabili, sláðu inn í dagsetningarreit stafinn t, eða orðið tímabil, og síðan númer sem tilgreinir fjárhagstímabilið, t.d. t2 eða timabil4. Bókhaldstímabilið er miðað við fjárhagsár núverandi vinnudags sem er stillt í hlutverki þínu. Ef vinnudagur er til dæmis **21/03/22**, þá t1 eða aðeins t, síar á fyrsta fjárhagstímabili fjárhagsársins 2022 (eins og 01/01/22..31/01/22). t15 síar á fimmtánda fjárhagstímabilinu frá upphafi fjárhagsársins 2022 (eins og 01/03/23..31/03/23).

Fjárhagstímabilin eru skilgreind á síðunni **Fjárhagstímabil**. Til að skoða eða breyta fjárhagstímabilum skaltu opna síðuna [hér](https://businesscentral.dynamics.com/?page=100).

### <a name="current-work-date"></a>Núverandi vinnudagsetning

Eiginleiki vinnudagsetningarinnar gerir þér kleift að skrá færslur með því að nota dagsetningu sem er frábrugðið núverandi dagsetningu.

Orðið fyrir „vinnudagsetning“ á tungumálinu sem er stillt með stillingunni **Tungumál** færir dagsetninguna í núverandi vinnudagsetningu, sem er tilgreind á síðunni **Mínar stillingar**. Í stað þess að slá inn allt orðið geturðu slegið inn hluta af orðinu, með því að byrja á byrjuninni, eins og til dæmis „v“ fyrir „vinnu“.

Ef þú hefur ekki skilgreint vinnudagsetningu, verður núverandi dagsetning notuð sem vinnudagsetning. Handhægt gæti verið að nota vinnudagsetningar ef verið er að nota margar færslur með aðra dagsetningu en dagsins í dag.

Sjá einnig [Breyta grunnstillingar, svo sem vinnudagsetning](ui-change-basic-settings.md#work-date).

### <a name="closing-date"></a>Lokunardagsetning

Þegar reikningsári er lokað er hægt að nota lokunardagsetningu til að sýna að færsla sé lokunarfærsla. Lokunardagsetning er í raun milli tveggja dagsetninga, til dæmis 31. des. og 1. jan.

Til að tilgreina að dagsetning sé lokadagsetning skaltu setja N rétt fyrir dagsetningu, svo sem N123101. Þetta er hægt að nota ásamt öllum dagsetningarmynstri.

### <a name="examples"></a>Dæmi

Eftirfarandi tafla inniheldur dæmi um dagsetningar þar sem öll snið eru notuð. Það er gert ráð fyrir svæðisstillingum sem sníðir dagsetningar samkvæmt: **ár.mánuður.dagur.**, viku sem hefst á mánudag og ensku.

|**Færsla**      |**Túlkun**      |
|---------------|------------------------|
|2022.12.31.|2022.12.31.|
|221231|2022.12.31.|
|22.12.31.|2022.12.31.|
|22.12.31.|2022.12.31.|
|20221231|2022.12.31.|
|22/12,31|2022.12.31.|
|11|vinnudagsetning ár/vinnudagsetning mánuður/11.|
|1112|vinnudagsetningarár/11/12.|
|d eða dagurinn í dag|dagurinn í dag|
|t4|dagsetningabil sem felur í sér fjórða reikningstímabilið, svo sem 01/04/20..30/04/20|
|v eða vinnudagsetningin|vinnudagsetningin|
|m eða mánudagur|Mánudagur vinnudagsetningarvikunnar|
|þr eða þriðjudagur|Þriðjudagur vinnudagsetningarvikunnar|
|la eða laugardagur|Laugardagur vinnudagsetningarvikunnar|
|s eða sunnudagur|Sunnudagur vinnudagsetningarvikunnar|
|þ23|Þriðjudagur 23. viku vinnudagsetningarársins|
|þ 23|Þriðjudagur 23. viku vinnudagsetningarársins|
|þ-1|Þriðjudagur 1. viku vinnudagsetningarársins|

##  <a name="setting-ranges"></a><a name="BKMK_SettingDateRanges"></a> Stillingarbil

Á listum, samtölum og skýrslum er hægt að stilla síur á dagsetningar, tímum og tímabilum sem innihalda upphafsgildi og mögulega endanlegt gildi til að birta aðeins gögnin sem eru í því bili. Stöðluðu reglurnar eiga við um það hvernig þú stillir dagsetningarsvið.

|**Merking**|**Dæmi um segð (dagsetning)**|**Gögn sem eru höfð með síunni**|
|-----------|---------------------|--------------------|
|Millibil|12 15 00..01 15 01<br /><br />..12 15 00<br /><br />t1..t4|Skrár með dagsetningar á milli og að meðtöldum 12 15 00 og 01 15 01.<br /><br />Færslur með dagsetningar 12 15 00 eða fyrr.<br /><br />Dagsetningabil sem inniheldur annað, þriðja og fjórða reikningstímabilið, svo sem 01/01/20..30/04/20.|
|Annaðhvort eða|12 15 00\|12 16 00|Skrár með dagsetningar annaðhvort 12 15 00 eða 12 16 00. Ef það eru skrár með dagsetningar á báðum dögum verða þær allar birtar.|
|Samsetning|12 15 00\|12 01 00..12 10 00  <br /><br />..12 14 00\|12 30 00..|Skrár með dagsetningar 12 15 00 eða á dagsetningum á milli og að meðtöldum 12 01 00 og 12 10 00.  <br /><br />Skrár með dagsetningar 12 14 00 eða fyrr, eða 12 30 00 eða síðar, það er, allar skrár nema þær sem eru með dagsetningar á milli og að meðtöldum 12 15 00 og 12 29 00.|

Þú getur notað öll gild snið í síum dagsetningarbils. Til dæmis, mán14 3..t 4t beitt á reitarniðurstöður dagsetningartíma í síu frá kl. 03:00 á mánudag í viku 14 á núgildandi vinnudagsetningarári, innifalið, þar til í dag kl. 16:00, innifalið.

## <a name="using-date-formulas"></a>Notkun dagsetningarreiknireglna
Dagsetningarregla er stutt, skammstöfuð samsetning stafa og tölustafa sem tilgreinir hvernig skal reikna út dagsetningar. Þú getur slegið inn dagsetningarformúlur í ýmsa reiknireiti fyrir dagsetningar eða síur.

> [!NOTE]
>  Dagurinn í dag, fyrir upphaf tímabilsins, er með í öllum reitum fyrir reiknireglur dagsetninga. Í samræmi við það, ef til dæmis er fært inn 1V er tímabilið í raun átta dagar þar sem dagurinn í dag er tekinn með. Til að tilgreina sjö daga tímabil \(ein raunvika\) að meðtalinni upphafsdagsetningu tímabilsins þarf að færa inn 6D eða 1V-1D.

Hér eru nokkur dæmi um hvernig nota má dagsetningarreiknireglur:

-   Dagsetningarreikniregla í ítrekunartíðnireitnum í ítrekunarbókum ákvarðar hversu oft færsla í færslubókarlínu er bókuð.

-   Dagsetningarreikniregla í reitnum **Biðtími** fyrir tiltekið innheimtustig ákvarðar það tímabil sem þarf að líða frá gjalddaga \(eða frá dagsetningu fyrri innheimtubréfs\) áður en innheimtubréf er búið til.

-   Dagsetningarreikniregla í reitnum **Gjalddagaútreikningur** ákvarðar hvernig á að reikna gjalddaga í innheimtubréfinu.

Dagsetningarformúlan getur innihaldið hámark 20 stafir, bæði tölur og bókstafir. Þú getur notað eftirfarandi stafi, sem eru skammstafanir fyrir dagbókareiningar.

|  Stafur  |  Merking  |
|----------|----------------------|
|N|Núverandi|
|D|Dagur\(s\)|
|V|Vika\(s\)|
|M|Mánuður\(s\)|
|F|Fjórðungur\(s\)|
|Á|Ár\(s\)|

Hægt er að rita dagsetningarreiknireglu á þrjá vegu.

Eftirfarandi dæmi sýnir hvernig á að nota N, fyrir núverandi, og tímaeiningu.

|  Segð  |  Merking  |
|--------------|-----------|
|LV|Núverandi vika|
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
|LM+10D|Núverandi mánuður \+ 10 dagar|

Eftirfarandi dæmi sýnir hvernig hægt er að nota mínustákn til að sýna gamla dagsetningu.

|  Segð  |  Merking  |
|--------------|-----------|
|-1Á|1 ári fyrir daginn í dag|

> [!IMPORTANT]
> Ef staðsetningin notar grunndagatal, er dagsetningarreiknireglan sem er til dæmis færð inn í reitinn **Afhendingartími** túlkuð samkvæmt vinnudögum. Til dæmis merkir 1B sjö vinnudaga.
<!--
# Entering Date Ranges
You can set filters containing a start date and an end date to display only the data contained in that date range or time interval. Special rules apply to the way you set date ranges. Let's take the **Customer Top 10** as an example:

![Setting a date range in the request page for the Customer Top 10 list](./media/ui-enter-date-ranges/customer-top10-list.png)

Here you can limit the report to a date range such as the past 2 weeks, or a total of 6 weeks, or whatever range you want. To set date ranges, you enter dates and then use either **..** or **|** to set the range. In our example, to show the top 10 customers for the first two weeks of May, you would set the date filter to *05 01 17..05 14 17*.
Here are a couple of other examples:

| Meaning | Example | Entries included |
|---|---|---|
|Equal to| 12 15 16 |Only those posted on December 15 2016.|
|Interval| 12 15 16..01 15 17<br /><br />..12 15 16|Those posted on dates between and including December 15 2016 and January 15 2017.<br /><br />Those posted on December 15 2016 or earlier.|
|Either/or|12 15 16&#124;12 16 16|Those posted on either December 15 or December 16 2016. If there are entries posted on both days, they will all be displayed.|

You can also combine the various format types.

| Example | Entries included |
|---|---|
|12 15 16&#124;12 01 16..05 31 17 | Entries posted either on December 15 2016 or on dates between and including December 01 2016 and May 31 2017. |
|..12 14 16&#124;12 30 16.. | Entries posted on December 14 or earlier, or entries posted on December 30 or later - that is, all entries except those posted on dates between and including December 15 and 29. |

Note that we have used the US date format MMDDYY here. As [!INCLUDE[prod_short](includes/prod_short.md)] becomes available in other markets, you'll be able to use the formats that you are used to.

## Using Date Formulas
A date formula is a short, abbreviated combination of letters and numbers that specifies how to calculate dates. You can enter date formulas in various date calculation fields and in recurring frequency fields in recurring journals.

> [!NOTE]
>  In all data formula fields, one day is automatically included to cover today as the day when the period starts. Accordingly, for example, if you enter **1W**, then the period is actually eight days because today is included. To specify a period of seven days (one true week) including the period starting date, then you must enter **6D** or **1W\-1D**.

Here are some examples of how date formulas can be used:

-   The date formula in the recurring frequency field in recurring journals determines how often the entry on the journal line will be posted.

-   The date formula in the **Grace Period** field for a specified reminder level determines the period of time that must pass from the due date (or from the due date of the previous reminder) before a reminder will be created.

-   The date formula in the **Due Date Calculation** field determines how to calculate the due date on the reminder.

The date calculation formula can contain a maximum of 20 characters, both numbers and letters. You can use the following letters, which are abbreviations for time specifications.

|  Letter  |  Time specification  |
|----------|----------------------|
|C|Current|
|D|Day\(s\)|
|W|Week\(s\)|
|M|Month\(s\)|
|Q|Quarter\(s\)|
|Y|Year\(s\)|

You can construct a date formula in three ways.

The following example shows how to use **C**, for current, and a time unit.

|  Expression  |  Meaning  |
|--------------|-----------|
|CW|Current week|
|CM|Current month|

The following example shows how to use a number and a time unit. A number cannot be larger than 9999.

|  Expression  |  Meaning  |
|--------------|-----------|
|10D|10 days from today|
|2W|2 weeks from today|

The following example shows how to use a time unit and a number.

|  Expression  |  Meaning  |
|--------------|-----------|
|D10|The next 10th day of a month|
|WD4|The next 4th day of a week \(Thursday\)|

The following example shows how you can combine these three forms as needed.

|  Expression  |  Meaning  |
|--------------|-----------|
|CM\+10D|Current month \+ 10 days|

The following example shows how you can use a minus sign to indicate a date in the past.

|  Expression  |  Meaning  |
|--------------|-----------|
|-1Y|1 year ago from today|

> [!IMPORTANT]
>  If the location uses a base calendar, then the date formula that you enter in, for example, the **Shipping Time** field is interpreted according to the calendar working days. For example, **1W**  means seven working days.

-->

## <a name="entering-times"></a>Tími færður inn
Þegar þú slærð inn tímana getur þú sett inn hvaða skiltákn án bils sem þú vilt milli eininganna, en ef þú notar tvöfalda tölustafi fyrir hverja einingu allt upp að millisekúndum, þá er þess ekki krafist.

Þú þarft aðeins að skrifa stærsta einingar sem þú þarfnast; restin verður stillt á núll. Þú getur einnig sleppt öllum f.h./e.h. vísum.

Í eftirfarandi töflu birtast mismunandi leiðir til að færa inn tímasetningar og hvernig þær eru túlkaðar: Það gerir ráð fyrir svæðisstillingar sem sníða tíma samkvæmt: **Klukkustundir:Mínútur:Sekúndur.Millisekúndur.** og nota f.h. og e.h. vísa um „f.h.“ og „e.h.“, eftir því sem við á.

|**Færsla**      |**Túlkun**      |
|---------------|------------------------|
|05:23:17|05:23:17|
|5|05:00:00|
|5AM|05:00:00|
|5P|17:00:00|
|12|12:00:00|
|12A|00:00:00|
|12P|12:00:00|
|17|17:00:00|
|5:30|05:30:00|
|0530|05:30:00|
|5:30:5|05:30:05|
|053005|05:30:05|
|5:30:5,50|05:30:05.5|
|053005050|05:30:05.05|

Þú ættir að vera meðvitaðir um að millisekúndur séu túlkuð sem tugabrot. Til dæmis þýðir 3, 30 og 300 þýðir allt 300 millisekúndur, á meðan 03 þýðir 30 og 003 þýðir 3 millisekúndur.

Þú getur ekki látið 24:00 tákna miðnætti eða notað gildi sem er hærra en 24:00.

Orðið fyrir „tími“ á tungumálinu sem notað er af [!INCLUDE[prod_short](includes/prod_long.md)] verður metið við núverandi tíma á tölvunni þinni eða fartækinu. Þú getur slegið inn hvaða hluta orðsins sem er, með því að byrja á byrjuninni, eins og til dæmis T eða TÍM.

## <a name="entering-combined-dates-and-times"></a>Slá inn sameinaða dagsetningar og tíma

[!INCLUDE [datetimes](includes/datetimes.md)]

## <a name="entering-duration"></a>Færið inn tímalengd
Sumir reitir í forritinu tákna tímalengd eða magn liðins tíma, í stað tiltekins dagsetningar eða tíma. Hægt er að færa inn tímalengd sem tölu og mælieiningu.

Hér eru nokkur dæmi.

|**Lengd**|**Mælieining**|
|------------|-------------------|
|2t|2 klst|
|6t 30 m|6 klst 30 mín|
|6,5t|6 klst 30 mín|
|90m|1 klst 30 mín|
|2d 6t 30m|2 dagar 6 klst 30 mín|
|2d 6t 30m 56s 600ms|2 dagar 6 klst 30 mín 56 sek 600 millis|

Einnig er hægt að færa inn tölu og þá er henni sjálfkrafa breytt í tímalengd. Tölunni sem færð er inn er breytt samkvæmt sjálfgefnu mælieiningunni sem hefur verið tilgreind fyrir reitinn tímalengd.

Hægt er að sjá hvaða mælieining er notuð í reitnum tímalengd með því að færa inn tölu og sjá í hvaða mælieiningu kerfið færir hana í.

Ef mælieiningin er til dæmis klukkustund, er númerinu 5 breytt í 5 klukkustundir.

## <a name="see-also"></a>Sjá einnig
[Unnið með [!INCLUDE[prod_short](includes/prod_long.md)]](ui-work-product.md)  
[Dagsetning útreiknings fyrir kaup](purchasing-date-calculation-for-purchases.md)  
[Skilgreining skilyrða í síum](ui-enter-criteria-filters.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]