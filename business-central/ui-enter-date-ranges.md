---
title: Innsláttur dagsetninga og tíma í Business Central
description: 'Lærðu hvernig á að slá inn dagsetningar og tíma, þar á meðal ýmsar ábendingar um framleiðni, svo sem hraðskrift, segð og afmarkanir.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'dates, reporting, filter, calendar, shorthand, range'
ms.search.form: '9020, 9022, 9026, 9027, 9030, 9000, 9009, 9004, 9005, 9024, 9006, 9007, 9010, 9016, 9017'
ms.date: 10/27/2023
ms.author: bholtorf
---

# <a name="work-with-calendar-dates-and-times"></a>Vinna með dagsetningar og tíma í dagatali

Hægt er að færa inn dagsetningar og tíma á marga vegu. [!INCLUDE[prod_short](includes/prod_long.md)] inniheldur öfluga eiginleika sem hraða gagnaskráningu eða hjálpa þér að skrifa flóknar segðir dagatals. Það eru ýmsar staðir í forritinu þar sem þú getur slegið inn dagsetningar og tíma í reitum. Til dæmis, í sölupöntun, getur þú stillt afhendingardagsetningu. Þegar verið er að afmarka lista eða skýrslugögn er hægt að slá inn dagsetningar og tíma til að staðsetja aðeins þau gögn sem þú hefur áhuga á.

[!INCLUDE [about-ui-learn](includes/about-ui-learn.md)]

## <a name="check-your-region-and-language-settings"></a>Athugaðu svæði og tungumálastillingar

**Mínar stillingar** síðan tilgreinir **Svæði** og **Tungumál** sem þú notar í forritinu. Þessar stillingar hafa áhrif á hvernig þú slærð inn dagsetningar og tíma.

- **Svæði** stillingin ákvarðar hvernig dagsetningar, tímasetningar, númer og gjaldmiðlar eru sýndir eða forsniðnir.

- Fyrir dagsetningamynstur sem fela í sér orð, tungumálið orðanna sem þú notar verða að vera í samræmi við **tungumál** stillinguna.

> [!NOTE]
> [!INCLUDE[prod_short](includes/prod_long.md)] notar gregoríska dagatalskerfið.

<!--
The following sections describe how you can enter dates, times, datetimes, durations, date ranges, and how you use date formulas.
-->

## <a name="entering-dates"></a>Dagsetningar færðar inn

Í dagsetningarreitinn getur þú slegið inn dagsetningu með því að nota staðlaða sniðið fyrir svæðisstillingu þína. Mismunandi svæði geta notað mismunandi skiltákn milli daga, mánaða og ára. Til dæmis, sum svæði nota bandstrik (mm-dd-áááá) og önnur nota áfram skástrik (mm/dd/áááá).  

> [!TIP]
> Þú getur notað hvaða skiltákn sem er, jafnvel bil, og dagsetningin verður sjálfkrafa breytt til að nota skiltákn sem passa við svæðið þitt.

> [!NOTE]
> Sniðið sem dagsetningar eru birtar á í prentuðum skýrslum eða skjölum sendum í tölvupósti eru ekki undir áhrifum af persónulegu vali þínu á svæðisstillingu.

Til að vinna á afkastameiri hátt með dagsetningar og tíma geturðu notað eitthvað af þeim aðferðum eða sniði sem lýst er í eftirfarandi köflum.

### <a name="picking-dates-from-the-calendar"></a>Velja dagsetningar úr dagatalinu

Allir reitir sem sýna dagbókartákn geta verið stilltar með dagsetningarvali dagatals. Til að birta tínslu á dagsetningarvali dagatals skal virkja dagatalstáknið <kbd>eða velja flýtivísunina Ctrl</kbd>+<kbd>Home</kbd> í reitnum.

![Dagsetningasvæði.](media/ui-date-field.png "Dæmi um dagsetningarreit")

Sjá einnig [Flýtilyklar í dagsetningarvali dagatals](keyboard-shortcuts.md#calendarshortcuts).

### <a name="day-week-year-pattern"></a>Dagur\-vika\-ár mynstur

Þú getur slegið inn dagsetningu sem vikudag og síðan vikunúmer og, ef þú vilt, ár. Til dæmis þýðir Mán25 eða mán25 mánudagur í viku 25. Ef þú slærð ekki inn ár er ár vinnudagsetningar notað.

Í stað þess að slá inn allt orðið fyrir vikudaginn getur þú slegið inn hluta af orðinu, með því að byrja á byrjuninni. Ef um er að ræða árekstur (eins og til dæmis f sem gæti verið fimmtudagur eða föstudagur) eru dagarnir metnir í samræmi við svæðisstillingu. Inntakið er fyrst metið með hliðsjón af vinnudegi og í dag líka, sem þú vilt hafa í huga við styttingu. Til dæmis þýðir _t_ „today“ og getur þar af leiðandi ekki þýtt „Tuesday“ eða „Thursday“.

Vikunúmersskemað er alltaf ISO 8601, þar sem vika 1 er vikan sem inniheldur 4. janúar, eða vikan sem inniheldur fyrsta fimmtudag ársins.

### <a name="digit-patterns"></a>Tölustafamynstur

Í dagsetningarreit má færa inn tvær, fjórar, sex eða átta tölur:

- Ef aðeins tvær tölur eru færðar inn þá túlkar kerfið þær sem daginn og bætir við mánuði og ári vinnudagsetningar.

- Ef færðar eru inn fjórar tölur þá túlkar kerfið þær sem daginn og mánuðinn og bætir við ári vinnudagsetningar. Röð dags og mánaðar ræðst af svæðisstillingum þínum. Jafnvel þótt svæðisstillingar þínar séu með árið fyrir daginn og mánuðinn eru fjórir tölustafir túlkaðir sem dagur og mánuður.

- Ef sú dagsetning sem færa á inn er á bilinu 01/01/1950 til 31/12/2049 má færa árið inn í tveimur tölum; annars skal færa árið inn með fjórum tölum.

  > [!NOTE]
  > Ef þú notar [!INCLUDE[prod_short](includes/prod_short.md)] á staðnum getur tveggja stafa árabilið verið mismunandi. Stjórnendur geta breytt bilinu með því að breyta stillingunni **CalendarTwoDigitYearMax** á [!INCLUDE[prod_short](includes/prod_short.md)] þjóninum. Frekari upplýsingar er að finna í [Skilgreining Business Central Server](/dynamics365/business-central/dev-itpro/administration/configure-server-instance#General).
 
### <a name="today"></a>Í dag

Sláðu inn orðið fyrir _í dag_ á tungumálinu sem tilgreint er á síðunni **Mínar stillingar** til að stilla dagsetningu færslu á daginn í dag. Í stað þess að slá inn allt orðið geturðu slegið inn fyrsta hluta orðsins. Á ensku er t.d. hægt að slá inn _t_ eða _tod_ svo lengi sem það er ekki líka byrjunin á öðru orði.

### <a name="period"></a>Tímabili

Til að sía á tilteknu fjárhagstímabili, sláðu inn í dagsetningarreit stafinn t, eða orðið tímabil, og síðan númer sem tilgreinir fjárhagstímabilið, t.d. t2 eða timabil4. Bókhaldstímabilið er miðað við fjárhagsár núverandi vinnudags sem er stillt í hlutverki þínu. Ef vinnudagur er til dæmis **03/21/22**, þá _p1_ eða aðeins _p_, síar á fyrsta fjárhagstímabili fjárhagsársins 2022 (eins og 01/01/22..01/31/22). _p15_ síar á fimmtánda fjárhagstímabilinu frá upphafi fjárhagsársins 2022 (eins og 01/03/23..31/03/23).

Fjárhagstímabilin eru skilgreind á síðunni **Fjárhagstímabil**. Til að skoða eða breyta fjárhagstímabilum skaltu opna síðuna [hér](https://businesscentral.dynamics.com/?page=100).

### <a name="work-date"></a>Vinnudagsetning

Notaðu vinnudagsetningu til að tilgreina dagsetningu sem er ekki dagurinn í dag í færslum. Til dæmis er vinnudagsetning gagnleg þegar þú þarft að setja á ákveðna dagsetningu fyrir margar skrár. Þú tilgreinir vinnudagsetninguna á síðunni **Mínar stillingar**. 

Fljótleg leið til að slá inn vinnudagsetningu í skrár er að slá inn hluta orðsins eða allt orðið _vinnu_ og byrja á fyrsta stafnum á tungumálinu sem þú notar [!INCLUDE[prod_short](includes/prod_long.md)]. Á ensku er t.d. hægt að færa inn _w_ eða _work_. Tungumálið er einnig tilgreint á síðunni **Mínar stillingar**.

Ef engin vinnudagsetning hefur verið tilgreind verður dagurinn í dag notaður. Frekari upplýsingar eru í [Breyta grunnstillingum eins og vinnudagsetningu](ui-change-basic-settings.md#work-date).

### <a name="closing-date"></a>Lokunardagsetning

Þegar reikningsári er lokað er hægt að nota lokunardagsetningu til að sýna að færsla sé lokunarfærsla. Lokunardagsetning er í raun milli tveggja dagsetninga, til dæmis 31. des. og 1. jan.

Til að tilgreina að dagsetning sé lokadagsetning skaltu setja N rétt fyrir dagsetningu, svo sem N123101. Notaðu þetta snið saman með öllum dagsetningarmynstrunum.

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
|v eða vinnudagsetning|vinnudagsetningin|
|m eða mánudagur|Mánudagur vinnudagsetningarvikunnar|
|þr eða þriðjudagur|Þriðjudagur vinnudagsetningarvikunnar|
|la eða laugardagur|Laugardagur vinnudagsetningarvikunnar|
|s eða sunnudagur|Sunnudagur vinnudagsetningarvikunnar|
|þ23|Þriðjudagur 23. viku vinnudagsetningarársins|
|þ 23|Þriðjudagur 23. viku vinnudagsetningarársins|
|þ-1|Þriðjudagur 1. viku vinnudagsetningarársins|

## <a name="setting-ranges"></a><a name="BKMK_SettingDateRanges"></a>Stillingarbil

Á listum, samtölum og skýrslum er hægt að stilla síur á dagsetningar, tímum og tímabilum sem innihalda upphafsgildi og mögulega endanlegt gildi til að birta aðeins gögnin sem eru í því bili. Stöðluðu reglurnar eiga við um það hvernig þú stillir dagsetningarsvið.

|**Merking**|**Dæmi um segð (dagsetning)**|**Gögn sem eru höfð með síunni**|
|-----------|---------------------|--------------------|
|Millibil|12 15 00..01 15 01<br /><br />..12 15 00<br /><br />t1..t4|Skrár með dagsetningar á milli og að meðtöldum 12 15 00 og 01 15 01.<br /><br />Færslur með dagsetningar 12 15 00 eða fyrr.<br /><br />Dagsetningabil sem inniheldur annað, þriðja og fjórða reikningstímabilið, svo sem 01/01/20..30/04/20.|
|Annaðhvort eða|12 15 00\|12 16 00|Skrár með dagsetningar annaðhvort 12 15 00 eða 12 16 00. Ef til eru færslur með dagsetningar á báðum dögum verða þær allar birtar.|
|Samsetning|12 15 00\|12 01 00..12 10 00  <br /><br />..12 14 00\|12 30 00..|Skrár með dagsetningar 12 15 00 eða á dagsetningum á milli og að meðtöldum 12 01 00 og 12 10 00.  <br /><br />Skrár með dagsetningar 12 14 00 eða fyrr, eða 12 30 00 eða síðar, það er, allar skrár nema þær sem eru með dagsetningar á milli og að meðtöldum 12 15 00 og 12 29 00.|

Þú getur notað öll gild snið í síum dagsetningarbils. Til dæmis, mán14 3..t 4t beitt á reitarniðurstöður dagsetningartíma í síu frá kl. 03:00 á mánudag í viku 14 á núgildandi vinnudagsetningarári, innifalið, þar til í dag kl. 16:00, innifalið.

## <a name="use-date-formulas"></a>Nota dagsetningarformúlur

Dagsetningarregla er stutt, skammstöfuð samsetning stafa og tölustafa sem tilgreinir hvernig skal reikna út dagsetningar. Þú getur slegið inn dagsetningarformúlur í ýmsa reiknireiti fyrir dagsetningar eða síur.

> [!NOTE]
> Dagurinn í dag, fyrir upphaf tímabilsins, er með í öllum reitum fyrir reiknireglur dagsetninga. Í samræmi við það, ef til dæmis er fært inn 1V er tímabilið í raun átta dagar þar sem dagurinn í dag er tekinn með. Til að tilgreina sjö daga tímabil \(ein raunvika\) að meðtalinni upphafsdagsetningu tímabilsins þarf að færa inn 6D eða 1V-1D.

Hér eru nokkur dæmi um hvernig nota má dagsetningarreiknireglur:

- Dagsetningarreikniregla í ítrekunartíðnireitnum í ítrekunarbókum ákvarðar hversu oft færsla í færslubókarlínu er bókuð.

- Dagsetningarreikniregla í reitnum **Biðtími** fyrir tiltekið innheimtustig ákvarðar það tímabil sem þarf að líða frá gjalddaga \(eða frá dagsetningu fyrri innheimtubréfs\) áður en innheimtubréf er búið til.

- Dagsetningarreikniregla í reitnum **Gjalddagaútreikningur** ákvarðar hvernig á að reikna gjalddaga í innheimtubréfinu.

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
|LV|Líðandi vika|
|KV|Líðandi mánuður (síðasti dagur mánaðarins)|

Eftirfarandi dæmi sýnir hvernig á að nota tölueiningu og tíma. Tala getur ekki verið hærri en 9999.

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
# <a name="entering-date-ranges"></a>Entering Date Ranges
You can set filters containing a start date and an end date to display only the data contained in that date range or time interval. Special rules apply to the way you set date ranges. Let's take the **Customer Top 10** as an example:

![Setting a date range in the request page for the Customer Top 10 list.](./media/ui-enter-date-ranges/customer-top10-list.png)

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

## <a name="use-date-formulas-1"></a>Use Date Formulas
A date formula is a short, abbreviated combination of letters and numbers that specifies how to calculate dates. You can enter date formulas in various date calculation fields and in recurring frequency fields in recurring journals.

> [!NOTE]
> In all data formula fields, one day is automatically included to cover today as the day when the period starts. Accordingly, for example, if you enter **1W**, then the period is actually eight days because today is included. To specify a period of seven days (one true week) including the period starting date, then you must enter **6D** or **1W\-1D**.

Here are some examples of how date formulas can be used:

- The date formula in the recurring frequency field in recurring journals determines how often the entry on the journal line will be posted.

- The date formula in the **Grace Period** field for a specified reminder level determines the period of time that must pass from the due date (or from the due date of the previous reminder) before a reminder will be created.

- The date formula in the **Due Date Calculation** field determines how to calculate the due date on the reminder.

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
> If the location uses a base calendar, then the date formula that you enter in, for example, the **Shipping Time** field is interpreted according to the calendar working days. For example, **1W**  means seven working days.

-->

## <a name="entering-times"></a>Tími færður inn

Þegar tímasetningar eru slegnar inn er hægt að setja inn hvaða skiltákn án bils sem er milli eininga. Ef notaðir eru tvöfaldir stafir fyrir hverja einingu fram að millisekúndum, þá er það ekki nauðsynlegt.

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
|5:30:5,50|05:30:050,5|
|053005050|05:30:05.05|

> [!NOTE]
> Millisekúndur eru túlkaðar sem tugabrotstákn. Til dæmis þýðir 3, 30 og 300 þýðir allt 300 millisekúndur, á meðan 03 þýðir 30 og 003 þýðir 3 millisekúndur.

> [!IMPORTANT]
> Ekki er hægt að nota 24:00 til að tákna miðnætti eða notað gildi sem er hærra en 24:00.

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

Hægt er að sjá hvaða mælieining er notuð í reitnum tímalengd með því að færa inn tölu. Síðan er hægt að sjá í hvaða mælieiningu hún er umreiknuð í.

Ef mælieiningin er til dæmis klukkustund, er númerinu 5 breytt í 5 klukkustundir.

## <a name="see-also"></a>Sjá einnig .

[Vinna með [!INCLUDE[prod_short](includes/prod_long.md)]](ui-work-product.md)  
[Dagsetning útreiknings fyrir kaup](purchasing-date-calculation-for-purchases.md)  
[Skilgreining skilyrða í síum](ui-enter-criteria-filters.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
