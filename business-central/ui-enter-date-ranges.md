---
title: Innsláttur dagsetninga og tíma í Business Central | Microsoft Docs
description: Lærðu hvernig á að slá inn dagsetningar og tíma, þar á meðal ýmsar ábendingar um framleiðni, svo sem hraðskrift, segð og afmarkanir. Sía lista eða skýrslur niður í tiltekna dagsetningu eða tímabil.
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: dates, reporting, filter, calendar, shorthand, range
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: ff34a7a8a1086b41d2df2a75955017fc82866fb6
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2020
ms.locfileid: "3194404"
---
# <a name="working-with-calendar-dates-and-times"></a><span data-ttu-id="52ef9-104">Vinna með dagsetningar og tíma í dagatali</span><span class="sxs-lookup"><span data-stu-id="52ef9-104">Working with Calendar Dates and Times</span></span>

[!INCLUDE[d365fin](includes/d365fin_long_md.md)] <span data-ttu-id="52ef9-105">býður upp á margar leiðir til að slá inn dagsetningar og tíma, þar með talin öflugar aðgerðir sem flýta fyrir gagnaskráningu eða hjálpa þér að skrifa flókna dagatalssegðir.</span><span class="sxs-lookup"><span data-stu-id="52ef9-105">offers multiple ways to enter dates and times, including powerful features that accelerate data entry, or help you write complex calendar expressions.</span></span> <span data-ttu-id="52ef9-106">Það eru ýmsar staðir í forritinu þar sem þú getur slegið inn dagsetningar og tíma í reitum.</span><span class="sxs-lookup"><span data-stu-id="52ef9-106">There are various places throughout the application where you can enter dates and times in fields.</span></span> <span data-ttu-id="52ef9-107">Til dæmis, í sölupöntun, getur þú stillt afhendingardagsetningu.</span><span class="sxs-lookup"><span data-stu-id="52ef9-107">For example, on a sales order, you can set the shipment date.</span></span> <span data-ttu-id="52ef9-108">Þegar verið er að afmarka lista eða skýrslugögn er hægt að slá inn dagsetningar og tíma til að staðsetja aðeins þau gögn sem þú hefur áhuga á.</span><span class="sxs-lookup"><span data-stu-id="52ef9-108">When filtering lists or report data, you can enter dates and times to pinpoint only the data that you are interested in.</span></span>

## <a name="check-your-region-and-language-settings"></a><span data-ttu-id="52ef9-109">Athugaðu svæði og tungumálastillingar</span><span class="sxs-lookup"><span data-stu-id="52ef9-109">Check your region and language settings</span></span>
<span data-ttu-id="52ef9-110">**Mínar stillingar** síðan tilgreinir **Svæði** og **Tungumál** sem þú notar í forritinu.</span><span class="sxs-lookup"><span data-stu-id="52ef9-110">The **My Settings** page specifies the **Region** and **Language** that you are using in the application.</span></span> <span data-ttu-id="52ef9-111">Þessar stillingar hafa áhrif á hvernig þú slærð inn dagsetningar og tíma.</span><span class="sxs-lookup"><span data-stu-id="52ef9-111">These settings influence how you enter dates and times.</span></span>

-   <span data-ttu-id="52ef9-112">**Svæði** stillingin ákvarðar hvernig dagsetningar, tímasetningar, númer og gjaldmiðlar eru sýndir eða forsniðnir.</span><span class="sxs-lookup"><span data-stu-id="52ef9-112">The **Region** setting determines how dates, times, numbers, and currencies are shown or formatted.</span></span>

-   <span data-ttu-id="52ef9-113">Fyrir dagsetningamynstur sem fela í sér orð, tungumálið orðanna sem þú notar verða að vera í samræmi við **tungumál** stillinguna.</span><span class="sxs-lookup"><span data-stu-id="52ef9-113">For date patterns that involve words, the language of the words that you use must correspond to the **Language** setting.</span></span>

> [!NOTE]
> [!INCLUDE[d365fin](includes/d365fin_long_md.md)] <span data-ttu-id="52ef9-114">notar gregoríska dagatalskerfið.</span><span class="sxs-lookup"><span data-stu-id="52ef9-114">uses the Gregorian calendar system.</span></span>

<!--
The following sections describe how you can enter dates, times, datetimes, durations, date ranges, and how you use date formulas.
-->

## <a name="entering-dates"></a><span data-ttu-id="52ef9-115">Dagsetningar færðar inn</span><span class="sxs-lookup"><span data-stu-id="52ef9-115">Entering Dates</span></span>

<span data-ttu-id="52ef9-116">Í dagsetningarreitinn getur þú slegið inn dagsetningu með því að nota staðlaða sniðið fyrir svæðisstillingu þína.</span><span class="sxs-lookup"><span data-stu-id="52ef9-116">In a date field, you can enter a date using the standard format for your region setting.</span></span> <span data-ttu-id="52ef9-117">Mismunandi svæði geta notað mismunandi skiltákn milli daga, mánaða og ára.</span><span class="sxs-lookup"><span data-stu-id="52ef9-117">Different regions can use different separators between the days, months and years.</span></span> <span data-ttu-id="52ef9-118">Til dæmis, sum svæði nota bandstrik (mm-dd-áááá) og önnur nota áfram skástrik (mm/dd/áááá).</span><span class="sxs-lookup"><span data-stu-id="52ef9-118">For example, some regions use dashes (mm-dd-yyyy) and others use forward slashes (mm/dd/yyyy).</span></span> <span data-ttu-id="52ef9-119">Hins vegar getur þú notað hvaða skiltákn sem er, jafnvel bil, og dagsetningin verður sjálfkrafa breytt til að nota skiltákn sem passa við svæðið þitt.</span><span class="sxs-lookup"><span data-stu-id="52ef9-119">However, you can use any separators, even a space, and the date will automatically be changed to use separators that match your region.</span></span>

<span data-ttu-id="52ef9-120">Athugaðu að sniðið sem dagsetningar eru birtar á í prentuðum skýrslum eða skjölum sendum í tölvupósti eru ekki undir áhrifum af persónulegu vali þínu á svæðisstillingu.</span><span class="sxs-lookup"><span data-stu-id="52ef9-120">Note that the format in which dates are displayed on printed reports or emailed documents is not influenced by your personal choice of region setting.</span></span>

<span data-ttu-id="52ef9-121">Til að vinna á afkastameiri hátt með dagsetningar og tíma geturðu notað eitthvað af þeim aðferðum eða sniði sem lýst er í eftirfarandi köflum.</span><span class="sxs-lookup"><span data-stu-id="52ef9-121">To work more productively with dates and times, you can use any of the methods or formats that are described in the following sections.</span></span>

### <a name="picking-dates-from-the-calendar"></a><span data-ttu-id="52ef9-122">Velja dagsetningar úr dagatalinu</span><span class="sxs-lookup"><span data-stu-id="52ef9-122">Picking dates from the calendar</span></span>

<span data-ttu-id="52ef9-123">Allir reitir sem sýna dagbókartákn geta verið stilltar með dagsetningarvali dagatals.</span><span class="sxs-lookup"><span data-stu-id="52ef9-123">Any field displaying a calendar icon can be set using the calendar date picker.</span></span> <span data-ttu-id="52ef9-124">Til að birta dagsetningarval dagatals skaltu virkja dagatalstáknið eða ýta á Ctrl + Home flýtilykilinn í reitnum.</span><span class="sxs-lookup"><span data-stu-id="52ef9-124">To display the calendar date picker, activate the calendar icon or press the Ctrl + Home keyboard shortcut in the field.</span></span>

<span data-ttu-id="52ef9-125">![Dagsetningasvæði](media/ui-date-field.png "Dæmi um dagsetningarreit")</span><span class="sxs-lookup"><span data-stu-id="52ef9-125">![Date fields](media/ui-date-field.png "Example of a date field")</span></span>

<span data-ttu-id="52ef9-126">Sjá einnig [Flýtilyklar í dagsetningarvali dagatals](keyboard-shortcuts.md#calendarshortcuts).</span><span class="sxs-lookup"><span data-stu-id="52ef9-126">See also [Keyboard Shortcuts in the calendar date picker](keyboard-shortcuts.md#calendarshortcuts).</span></span>

### <a name="day-week-year-pattern"></a><span data-ttu-id="52ef9-127">Dagur\-vika\-ár mynstur</span><span class="sxs-lookup"><span data-stu-id="52ef9-127">Day\-week\-year pattern</span></span>

<span data-ttu-id="52ef9-128">Þú getur slegið inn dagsetningu sem vikudag og síðan vikunúmer og, ef þú vilt, ár.</span><span class="sxs-lookup"><span data-stu-id="52ef9-128">You can enter a date as a weekday followed by a week number and, optionally, a year.</span></span> <span data-ttu-id="52ef9-129">Til dæmis þýðir Mán25 eða mán25 mánudagur í viku 25.</span><span class="sxs-lookup"><span data-stu-id="52ef9-129">For example, Mon25 or mon25 means Monday in week 25.</span></span> <span data-ttu-id="52ef9-130">Ef þú slærð ekki inn ár er ár vinnudagsetningar notað.</span><span class="sxs-lookup"><span data-stu-id="52ef9-130">If you do not enter a year, the year of the work date is used.</span></span>

<span data-ttu-id="52ef9-131">Í stað þess að slá inn allt orðið fyrir vikudaginn getur þú slegið inn hluta af orðinu, með því að byrja á byrjuninni.</span><span class="sxs-lookup"><span data-stu-id="52ef9-131">Instead of entering the entire word for the day of the week, you can enter part of the word, starting from the beginning.</span></span> <span data-ttu-id="52ef9-132">Ef um er að ræða árekstur (eins og til dæmis f sem gæti verið fimmtudagur eða föstudagur) eru dagarnir metnir í samræmi við svæðisstillingu.</span><span class="sxs-lookup"><span data-stu-id="52ef9-132">In case of conflicts (such as with s which could be Saturday or Sunday), the days are evaluated according to the region setting.</span></span> <span data-ttu-id="52ef9-133">Inntakið er fyrst metið út frá vinnudegi og deginum í dag einnig, svo hafðu þetta í huga þegar skammstafað er.</span><span class="sxs-lookup"><span data-stu-id="52ef9-133">The input is first evaluated against workdate and today as well, so keep this in mind when abbreviating.</span></span> <span data-ttu-id="52ef9-134">Til dæmis þýðir d nú þegar í dag, svo það getur ekki þýtt þriðjudagur eða fimmtudagur.</span><span class="sxs-lookup"><span data-stu-id="52ef9-134">For example, t already means today, so it cannot mean Tuesday or Thursday.</span></span>

<span data-ttu-id="52ef9-135">Vikunúmersskemað er alltaf ISO 8601, þar sem vika 1 er vikan sem inniheldur 4. janúar, eða vikan sem inniheldur fyrsta fimmtudag ársins.</span><span class="sxs-lookup"><span data-stu-id="52ef9-135">The week number scheme is always ISO 8601, where week 1 is the week with 4 January in it, or the week with the first Thursday of the year.</span></span>

### <a name="digit-patterns"></a><span data-ttu-id="52ef9-136">Tölustafamynstur</span><span class="sxs-lookup"><span data-stu-id="52ef9-136">Digit patterns</span></span>

<span data-ttu-id="52ef9-137">Í dagsetningarreit má færa inn tvær, fjórar, sex eða átta tölur:</span><span class="sxs-lookup"><span data-stu-id="52ef9-137">In a date field you can enter two, four, six, or eight digits:</span></span>

-   <span data-ttu-id="52ef9-138">Ef aðeins tvær tölur eru færðar inn þá túlkar kerfið þær sem daginn og bætir við mánuði og ári vinnudagsetningar.</span><span class="sxs-lookup"><span data-stu-id="52ef9-138">If you enter only two digits, this is interpreted as the day, and it will add the month and the year of the work date.</span></span>

-   <span data-ttu-id="52ef9-139">Ef færðar eru inn fjórar tölur þá túlkar kerfið þær sem daginn og mánuðinn og bætir við ári vinnudagsetningar.</span><span class="sxs-lookup"><span data-stu-id="52ef9-139">If you enter four digits, this is interpreted as the day and the month, and it will add the year of the work date.</span></span> <span data-ttu-id="52ef9-140">Röð dags og mánaðar ræðst af svæðisstillingum þínum.</span><span class="sxs-lookup"><span data-stu-id="52ef9-140">The order of the day and month is determined by your region settings.</span></span> <span data-ttu-id="52ef9-141">Jafnvel þótt svæðisstillingar þínar séu með árið fyrir daginn og mánuðinn eru fjórir tölustafir túlkaðir sem dagur og mánuður.</span><span class="sxs-lookup"><span data-stu-id="52ef9-141">Even if your region settings have the year before the day and month, four digits are interpreted as the day and month.</span></span>

-   <span data-ttu-id="52ef9-142">Ef sú dagsetning sem færa á inn er á bilinu 01/01/1930 til 31/12/2029 má færa árið inn í tveimur tölum; annars skal færa árið inn með fjórum tölum.</span><span class="sxs-lookup"><span data-stu-id="52ef9-142">If the date you want to enter is in the range 01/01/1930 through 12/31/2029, you can enter the year with two digits; otherwise, enter the year with four digits.</span></span>

### <a name="today"></a><span data-ttu-id="52ef9-143">Í dag</span><span class="sxs-lookup"><span data-stu-id="52ef9-143">Today</span></span>

<span data-ttu-id="52ef9-144">Sláðu inn orðið fyrir daginn í dag, á tungumáli sem er stillt í **Tungumál**, sem stillir daginn á núverandi dagsetningu.</span><span class="sxs-lookup"><span data-stu-id="52ef9-144">Enter the word for today, in the language set by **Language** setting, that will set the date to the current date.</span></span> <span data-ttu-id="52ef9-145">Í stað þess að slá inn allt orðið geturðu slegið inn hluta af orðinu, með því að byrja á byrjuninni, eins og t eða ídag, svo lengi sem það er ekki líka byrjun annars orðs.</span><span class="sxs-lookup"><span data-stu-id="52ef9-145">Instead of entering the entire word, you can enter part of the word, starting from the beginning, such as t or tod, as long as it is not also the start of another word.</span></span>

### <a name="period"></a><span data-ttu-id="52ef9-146">Tímabil</span><span class="sxs-lookup"><span data-stu-id="52ef9-146">Period</span></span>

<span data-ttu-id="52ef9-147">Til að sía á tilteknu fjárhagstímabili, sláðu inn í dagsetningarreit stafinn t, eða orðið tímabil, og síðan númer sem tilgreinir fjárhagstímabilið, t.d. t2 eða timabil4.</span><span class="sxs-lookup"><span data-stu-id="52ef9-147">To filter on a specific accounting period, in a date field enter the letter p, or the word period, followed by a number that identifies the accounting period, like p2 or period4.</span></span> <span data-ttu-id="52ef9-148">Bókhaldstímabilið er miðað við fjárhagsár núverandi vinnudags sem er stillt í hlutverki þínu.</span><span class="sxs-lookup"><span data-stu-id="52ef9-148">The accounting period is relative to the fiscal year of the current work date that set in your Role Center.</span></span> <span data-ttu-id="52ef9-149">Ef vinnudagur er til dæmis **21/03/20**, þá t1 eða aðeins t, síar á fyrsta fjárhagstímabili fjárhagsársins 2020 (eins og 01/01/20..31/01/20).</span><span class="sxs-lookup"><span data-stu-id="52ef9-149">For example, if the work date is **03/21/20**, then p1, or just p, filters on the first accounting period of the fiscal year 2020 (such as 01/01/20..01/31/20).</span></span> <span data-ttu-id="52ef9-150">t15 síar á fimmtánda fjárhagstímabilinu frá upphafi fjárhagsársins 2020 (eins og 01/03/21..31/03/21).</span><span class="sxs-lookup"><span data-stu-id="52ef9-150">p15 filters on the fifteenth accounting period from the start of fiscal year 2020 (such as 03/01/21..03/31/21).</span></span>

<span data-ttu-id="52ef9-151">Fjárhagstímabilin eru skilgreind á síðunni **Fjárhagstímabil**.</span><span class="sxs-lookup"><span data-stu-id="52ef9-151">The accounting periods are defined on the **Accounting Periods** page.</span></span> <span data-ttu-id="52ef9-152">Til að skoða eða breyta fjárhagstímabilum skaltu opna síðuna [hér](https://businesscentral.dynamics.com/?page=100).</span><span class="sxs-lookup"><span data-stu-id="52ef9-152">To view or change the accounting periods, open the page [here](https://businesscentral.dynamics.com/?page=100).</span></span>

### <a name="current-work-date"></a><span data-ttu-id="52ef9-153">Núverandi vinnudagsetning</span><span class="sxs-lookup"><span data-stu-id="52ef9-153">Current work date</span></span>

<span data-ttu-id="52ef9-154">Eiginleiki vinnudagsetningarinnar gerir þér kleift að skrá færslur með því að nota dagsetningu sem er frábrugðið núverandi dagsetningu.</span><span class="sxs-lookup"><span data-stu-id="52ef9-154">The work date feature allows you to record transactions using a date that is different from the current date.</span></span>

<span data-ttu-id="52ef9-155">Orðið fyrir „vinnudagsetning“ á tungumálinu sem er stillt með stillingunni **Tungumál** færir dagsetninguna í núverandi vinnudagsetningu, sem er tilgreind á síðunni **Mínar stillingar**.</span><span class="sxs-lookup"><span data-stu-id="52ef9-155">The word for 'workdate', in the language set by **Language** setting, will set the date to the currently set work date that is specified on the **My Settings** page.</span></span> <span data-ttu-id="52ef9-156">Í stað þess að slá inn allt orðið geturðu slegið inn hluta af orðinu, með því að byrja á byrjuninni, eins og til dæmis „v“ fyrir „vinnu“.</span><span class="sxs-lookup"><span data-stu-id="52ef9-156">Instead of entering the entire word, you can enter part of the word, starting from the beginning, such as 'w' or 'work'.</span></span>

<span data-ttu-id="52ef9-157">Ef þú hefur ekki skilgreint vinnudagsetningu, verður núverandi dagsetning notuð sem vinnudagsetning.</span><span class="sxs-lookup"><span data-stu-id="52ef9-157">If you have not defined a work date, the current date will be used as the work date.</span></span> <span data-ttu-id="52ef9-158">Handhægt gæti verið að nota vinnudagsetningar ef verið er að nota margar færslur með aðra dagsetningu en dagsins í dag.</span><span class="sxs-lookup"><span data-stu-id="52ef9-158">You may want to use a work date if you have many transactions with a date other than today's date.</span></span>

<span data-ttu-id="52ef9-159">Sjá einnig [Breyta grunnstillingar, svo sem vinnudagsetning](ui-change-basic-settings.md#work-date).</span><span class="sxs-lookup"><span data-stu-id="52ef9-159">See also [Change Basic Settings, such as the Work Date](ui-change-basic-settings.md#work-date).</span></span>

### <a name="closing-date"></a><span data-ttu-id="52ef9-160">Lokunardagsetning</span><span class="sxs-lookup"><span data-stu-id="52ef9-160">Closing Date</span></span>

<span data-ttu-id="52ef9-161">Þegar reikningsári er lokað er hægt að nota lokunardagsetningu til að sýna að færsla sé lokunarfærsla.</span><span class="sxs-lookup"><span data-stu-id="52ef9-161">When you close a fiscal year, you can use closing dates to indicate that an entry is a closing entry.</span></span> <span data-ttu-id="52ef9-162">Lokunardagsetning er í raun milli tveggja dagsetninga, til dæmis 31. des. og 1. jan.</span><span class="sxs-lookup"><span data-stu-id="52ef9-162">A closing date technically is between two dates, for example between Dec 31 and Jan 1.</span></span>

<span data-ttu-id="52ef9-163">Til að tilgreina að dagsetning sé lokadagsetning skaltu setja N rétt fyrir dagsetningu, svo sem N123101.</span><span class="sxs-lookup"><span data-stu-id="52ef9-163">To specify that a date is a closing date, put C just before the date, such as C123101.</span></span> <span data-ttu-id="52ef9-164">Þetta er hægt að nota ásamt öllum dagsetningarmynstri.</span><span class="sxs-lookup"><span data-stu-id="52ef9-164">This can be used in combination with all the date patterns.</span></span>

### <a name="examples"></a><span data-ttu-id="52ef9-165">Dæmi</span><span class="sxs-lookup"><span data-stu-id="52ef9-165">Examples</span></span>

<span data-ttu-id="52ef9-166">Eftirfarandi tafla inniheldur dæmi um dagsetningar þar sem öll snið eru notuð.</span><span class="sxs-lookup"><span data-stu-id="52ef9-166">The following table contains examples of dates using all the formats.</span></span> <span data-ttu-id="52ef9-167">Það er gert ráð fyrir svæðisstillingum sem sníðir dagsetningar samkvæmt: **ár.mánuður.dagur.**, viku sem hefst á mánudag og ensku.</span><span class="sxs-lookup"><span data-stu-id="52ef9-167">It assumes region settings that format dates according to: **year.month.day.**, a week starting on Monday, and the English language.</span></span>

|<span data-ttu-id="52ef9-168">**Færsla**</span><span class="sxs-lookup"><span data-stu-id="52ef9-168">**Entry**</span></span>      |<span data-ttu-id="52ef9-169">**Túlkun**</span><span class="sxs-lookup"><span data-stu-id="52ef9-169">**Interpretation**</span></span>      |
|---------------|------------------------|
|<span data-ttu-id="52ef9-170">2018.12.31.</span><span class="sxs-lookup"><span data-stu-id="52ef9-170">2018.12.31.</span></span>|<span data-ttu-id="52ef9-171">31/12/2018.</span><span class="sxs-lookup"><span data-stu-id="52ef9-171">2018.12.31.</span></span>|
|<span data-ttu-id="52ef9-172">311218</span><span class="sxs-lookup"><span data-stu-id="52ef9-172">181231</span></span>|<span data-ttu-id="52ef9-173">31/12/2018</span><span class="sxs-lookup"><span data-stu-id="52ef9-173">2018.12.31.</span></span>|
|<span data-ttu-id="52ef9-174">18.12.31.</span><span class="sxs-lookup"><span data-stu-id="52ef9-174">18.12.31.</span></span>|<span data-ttu-id="52ef9-175">31/12/2018</span><span class="sxs-lookup"><span data-stu-id="52ef9-175">2018.12.31.</span></span>|
|<span data-ttu-id="52ef9-176">18.12.31.</span><span class="sxs-lookup"><span data-stu-id="52ef9-176">18.12.31.</span></span>|<span data-ttu-id="52ef9-177">31/12/2018</span><span class="sxs-lookup"><span data-stu-id="52ef9-177">2018.12.31.</span></span>|
|<span data-ttu-id="52ef9-178">31122018</span><span class="sxs-lookup"><span data-stu-id="52ef9-178">20181231</span></span>|<span data-ttu-id="52ef9-179">31/12/2018</span><span class="sxs-lookup"><span data-stu-id="52ef9-179">2018.12.31.</span></span>|
|<span data-ttu-id="52ef9-180">18/12,31</span><span class="sxs-lookup"><span data-stu-id="52ef9-180">18/12,31</span></span>|<span data-ttu-id="52ef9-181">31/12/2018</span><span class="sxs-lookup"><span data-stu-id="52ef9-181">2018.12.31.</span></span>|
|<span data-ttu-id="52ef9-182">11</span><span class="sxs-lookup"><span data-stu-id="52ef9-182">11</span></span>|<span data-ttu-id="52ef9-183">vinnudagsetning ár/vinnudagsetning mánuður/11.</span><span class="sxs-lookup"><span data-stu-id="52ef9-183">work date year.work date month.11.</span></span>|
|<span data-ttu-id="52ef9-184">1112</span><span class="sxs-lookup"><span data-stu-id="52ef9-184">1112</span></span>|<span data-ttu-id="52ef9-185">vinnudagsetningarár/11/12.</span><span class="sxs-lookup"><span data-stu-id="52ef9-185">work date year.11.12.</span></span>|
|<span data-ttu-id="52ef9-186">d eða dagurinn í dag</span><span class="sxs-lookup"><span data-stu-id="52ef9-186">t or today</span></span>|<span data-ttu-id="52ef9-187">dagurinn í dag</span><span class="sxs-lookup"><span data-stu-id="52ef9-187">today's date</span></span>|
|<span data-ttu-id="52ef9-188">t4</span><span class="sxs-lookup"><span data-stu-id="52ef9-188">p4</span></span>|<span data-ttu-id="52ef9-189">dagsetningabil sem felur í sér fjórða reikningstímabilið, svo sem 01/04/20..30/04/20</span><span class="sxs-lookup"><span data-stu-id="52ef9-189">date range that includes the fourth accounting period, such as 04/01/20..04/30/20</span></span>|
|<span data-ttu-id="52ef9-190">v eða vinnudagsetningin</span><span class="sxs-lookup"><span data-stu-id="52ef9-190">w or workdate</span></span>|<span data-ttu-id="52ef9-191">vinnudagsetningin</span><span class="sxs-lookup"><span data-stu-id="52ef9-191">the working date</span></span>|
|<span data-ttu-id="52ef9-192">m eða mánudagur</span><span class="sxs-lookup"><span data-stu-id="52ef9-192">m or Monday</span></span>|<span data-ttu-id="52ef9-193">Mánudagur vinnudagsetningarvikunnar</span><span class="sxs-lookup"><span data-stu-id="52ef9-193">Monday of the work date week</span></span>|
|<span data-ttu-id="52ef9-194">þr eða þriðjudagur</span><span class="sxs-lookup"><span data-stu-id="52ef9-194">tu or Tuesday</span></span>|<span data-ttu-id="52ef9-195">Þriðjudagur vinnudagsetningarvikunnar</span><span class="sxs-lookup"><span data-stu-id="52ef9-195">Tuesday of the work date week</span></span>|
|<span data-ttu-id="52ef9-196">la eða laugardagur</span><span class="sxs-lookup"><span data-stu-id="52ef9-196">sa or Saturday</span></span>|<span data-ttu-id="52ef9-197">Laugardagur vinnudagsetningarvikunnar</span><span class="sxs-lookup"><span data-stu-id="52ef9-197">Saturday of the work date week</span></span>|
|<span data-ttu-id="52ef9-198">s eða sunnudagur</span><span class="sxs-lookup"><span data-stu-id="52ef9-198">s or Sunday</span></span>|<span data-ttu-id="52ef9-199">Sunnudagur vinnudagsetningarvikunnar</span><span class="sxs-lookup"><span data-stu-id="52ef9-199">Sunday of the work date week</span></span>|
|<span data-ttu-id="52ef9-200">þ23</span><span class="sxs-lookup"><span data-stu-id="52ef9-200">t23</span></span>|<span data-ttu-id="52ef9-201">Þriðjudagur 23. viku vinnudagsetningarársins</span><span class="sxs-lookup"><span data-stu-id="52ef9-201">Tuesday of week 23 of the work date year</span></span>|
|<span data-ttu-id="52ef9-202">þ 23</span><span class="sxs-lookup"><span data-stu-id="52ef9-202">t 23</span></span>|<span data-ttu-id="52ef9-203">Þriðjudagur 23. viku vinnudagsetningarársins</span><span class="sxs-lookup"><span data-stu-id="52ef9-203">Tuesday of week 23 of the work date year</span></span>|
|<span data-ttu-id="52ef9-204">þ-1</span><span class="sxs-lookup"><span data-stu-id="52ef9-204">t-1</span></span>|<span data-ttu-id="52ef9-205">Þriðjudagur 1. viku vinnudagsetningarársins</span><span class="sxs-lookup"><span data-stu-id="52ef9-205">Tuesday of week 1 of the work date year</span></span>|

##  <a name="setting-ranges"></a><a name="BKMK_SettingDateRanges"></a> <span data-ttu-id="52ef9-206">Stillingarbil</span><span class="sxs-lookup"><span data-stu-id="52ef9-206">Setting Ranges</span></span>

<span data-ttu-id="52ef9-207">Á listum, samtölum og skýrslum er hægt að stilla síur á dagsetningar, tímum og tímabilum sem innihalda upphafsgildi og mögulega endanlegt gildi til að birta aðeins gögnin sem eru í því bili.</span><span class="sxs-lookup"><span data-stu-id="52ef9-207">On lists, totals and reports, you can set filters on dates, times and datetimes containing a start value and optionally an end value to display only the data contained in that range.</span></span> <span data-ttu-id="52ef9-208">Stöðluðu reglurnar eiga við um það hvernig þú stillir dagsetningarsvið.</span><span class="sxs-lookup"><span data-stu-id="52ef9-208">The standard rules apply to the way you set date ranges.</span></span>

|<span data-ttu-id="52ef9-209">**Merking**</span><span class="sxs-lookup"><span data-stu-id="52ef9-209">**Meaning**</span></span>|<span data-ttu-id="52ef9-210">**Dæmi um segð (dagsetning)**</span><span class="sxs-lookup"><span data-stu-id="52ef9-210">**Sample expression (Date)**</span></span>|<span data-ttu-id="52ef9-211">**Gögn sem eru höfð með síunni**</span><span class="sxs-lookup"><span data-stu-id="52ef9-211">**Data included in the filter**</span></span>|
|-----------|---------------------|--------------------|
|<span data-ttu-id="52ef9-212">Millibil</span><span class="sxs-lookup"><span data-stu-id="52ef9-212">Interval</span></span>|<span data-ttu-id="52ef9-213">12 15 00..01 15 01</span><span class="sxs-lookup"><span data-stu-id="52ef9-213">12 15 00..01 15 01</span></span><br /><br /><span data-ttu-id="52ef9-214">..12 15 00</span><span class="sxs-lookup"><span data-stu-id="52ef9-214">..12 15 00</span></span><br /><br /><span data-ttu-id="52ef9-215">t1..t4</span><span class="sxs-lookup"><span data-stu-id="52ef9-215">p1..p4</span></span>|<span data-ttu-id="52ef9-216">Skrár með dagsetningar á milli og að meðtöldum 12 15 00 og 01 15 01.</span><span class="sxs-lookup"><span data-stu-id="52ef9-216">Records with dates between and including 12 15 00 and 01 15 01.</span></span><br /><br /><span data-ttu-id="52ef9-217">Færslur með dagsetningar 12 15 00 eða fyrr.</span><span class="sxs-lookup"><span data-stu-id="52ef9-217">Records with dates of 12 15 00 or earlier.</span></span><br /><br /><span data-ttu-id="52ef9-218">Dagsetningabil sem inniheldur annað, þriðja og fjórða reikningstímabilið, svo sem 01/01/20..30/04/20.</span><span class="sxs-lookup"><span data-stu-id="52ef9-218">Date range that includes the second, third, and fourth accounting periods, such as 01/01/20..04/30/20.</span></span>|
|<span data-ttu-id="52ef9-219">Annaðhvort eða</span><span class="sxs-lookup"><span data-stu-id="52ef9-219">Either/or</span></span>|<span data-ttu-id="52ef9-220">12 15 00\|12 16 00</span><span class="sxs-lookup"><span data-stu-id="52ef9-220">12 15 00\|12 16 00</span></span>|<span data-ttu-id="52ef9-221">Skrár með dagsetningar annaðhvort 12 15 00 eða 12 16 00.</span><span class="sxs-lookup"><span data-stu-id="52ef9-221">Records with dates of either 12 15 00 or 12 16 00.</span></span> <span data-ttu-id="52ef9-222">Ef það eru skrár með dagsetningar á báðum dögum verða þær allar birtar.</span><span class="sxs-lookup"><span data-stu-id="52ef9-222">If there are records with dates on both days, they will all be displayed.</span></span>|
|<span data-ttu-id="52ef9-223">Samsetning</span><span class="sxs-lookup"><span data-stu-id="52ef9-223">Combination</span></span>|<span data-ttu-id="52ef9-224">12 15 00\|12 01 00..12 10 00</span><span class="sxs-lookup"><span data-stu-id="52ef9-224">12 15 00\|12 01 00..12 10 00</span></span>  <br /><br /><span data-ttu-id="52ef9-225">..12 14 00\|12 30 00..</span><span class="sxs-lookup"><span data-stu-id="52ef9-225">..12 14 00\|12 30 00..</span></span>|<span data-ttu-id="52ef9-226">Skrár með dagsetningar 12 15 00 eða á dagsetningum á milli og að meðtöldum 12 01 00 og 12 10 00.</span><span class="sxs-lookup"><span data-stu-id="52ef9-226">Records with dates of 12 15 00 or on dates between and including 12 01 00 and 12 10 00.</span></span>  <br /><br /><span data-ttu-id="52ef9-227">Skrár með dagsetningar 12 14 00 eða fyrr, eða 12 30 00 eða síðar, það er, allar skrár nema þær sem eru með dagsetningar á milli og að meðtöldum 12 15 00 og 12 29 00.</span><span class="sxs-lookup"><span data-stu-id="52ef9-227">Records with dates of 12 14 00 or earlier, or dates of 12 30 00 or later, that is, all records except those with dates between and including 12 15 00 and 12 29 00.</span></span>|

<span data-ttu-id="52ef9-228">Þú getur notað öll gild snið í síum dagsetningarbils.</span><span class="sxs-lookup"><span data-stu-id="52ef9-228">You can use any of the valid formats in date range filters.</span></span> <span data-ttu-id="52ef9-229">Til dæmis, mán14 3..t 4t beitt á reitarniðurstöður dagsetningartíma í síu frá kl. 03:00 á mánudag í viku 14 á núgildandi vinnudagsetningarári, innifalið, þar til í dag kl. 16:00, innifalið.</span><span class="sxs-lookup"><span data-stu-id="52ef9-229">For example, mon14 3..t 4p applied on a datetime field results in a filter from 3 AM on Monday in week 14 of the current work date year, inclusive, until today at 4PM, inclusive.</span></span>

## <a name="using-date-formulas"></a><span data-ttu-id="52ef9-230">Notkun dagsetningarreiknireglna</span><span class="sxs-lookup"><span data-stu-id="52ef9-230">Using Date Formulas</span></span>
<span data-ttu-id="52ef9-231">Dagsetningarregla er stutt, skammstöfuð samsetning stafa og tölustafa sem tilgreinir hvernig skal reikna út dagsetningar.</span><span class="sxs-lookup"><span data-stu-id="52ef9-231">A date formula is a short, abbreviated combination of letters and numbers that specifies how to calculate dates.</span></span> <span data-ttu-id="52ef9-232">Þú getur slegið inn dagsetningarformúlur í ýmsa reiknireiti fyrir dagsetningar eða síur.</span><span class="sxs-lookup"><span data-stu-id="52ef9-232">You can enter date formulas in various date calculation fields or filters.</span></span>

> [!NOTE]
>  <span data-ttu-id="52ef9-233">Dagurinn í dag, fyrir upphaf tímabilsins, er með í öllum reitum fyrir reiknireglur dagsetninga.</span><span class="sxs-lookup"><span data-stu-id="52ef9-233">In all data formula fields, one day is automatically included to cover today as the day when the period starts.</span></span> <span data-ttu-id="52ef9-234">Í samræmi við það, ef til dæmis er fært inn 1V er tímabilið í raun átta dagar þar sem dagurinn í dag er tekinn með.</span><span class="sxs-lookup"><span data-stu-id="52ef9-234">Accordingly, for example, if you enter 1W, then the period is actually eight days because today is included.</span></span> <span data-ttu-id="52ef9-235">Til að tilgreina sjö daga tímabil \(ein raunvika\) að meðtalinni upphafsdagsetningu tímabilsins þarf að færa inn 6D eða 1V-1D.</span><span class="sxs-lookup"><span data-stu-id="52ef9-235">To specify a period of seven days \(one true week\) including the period starting date, then you must enter 6D or 1W-1D.</span></span>

<span data-ttu-id="52ef9-236">Hér eru nokkur dæmi um hvernig nota má dagsetningarreiknireglur:</span><span class="sxs-lookup"><span data-stu-id="52ef9-236">Here are some examples of how date formulas can be used:</span></span>

-   <span data-ttu-id="52ef9-237">Dagsetningarreikniregla í ítrekunartíðnireitnum í ítrekunarbókum ákvarðar hversu oft færsla í færslubókarlínu er bókuð.</span><span class="sxs-lookup"><span data-stu-id="52ef9-237">The date formula in the recurring frequency field in recurring journals determines how often the entry on the journal line will be posted.</span></span>

-   <span data-ttu-id="52ef9-238">Dagsetningarreikniregla í reitnum **Biðtími** fyrir tiltekið innheimtustig ákvarðar það tímabil sem þarf að líða frá gjalddaga \(eða frá dagsetningu fyrri innheimtubréfs\) áður en innheimtubréf er búið til.</span><span class="sxs-lookup"><span data-stu-id="52ef9-238">The date formula in the **Grace Period** field for a specified reminder level determines the period of time that must pass from the due date \(or from the date of the previous reminder\) before a reminder will be created.</span></span>

-   <span data-ttu-id="52ef9-239">Dagsetningarreikniregla í reitnum **Gjalddagaútreikningur** ákvarðar hvernig á að reikna gjalddaga í innheimtubréfinu.</span><span class="sxs-lookup"><span data-stu-id="52ef9-239">The date formula in the **Due Date Calculation** field determines how to calculate the due date on the reminder.</span></span>

<span data-ttu-id="52ef9-240">Dagsetningarformúlan getur innihaldið hámark 20 stafir, bæði tölur og bókstafir.</span><span class="sxs-lookup"><span data-stu-id="52ef9-240">The date formula can contain a maximum of 20 characters, both numbers and letters.</span></span> <span data-ttu-id="52ef9-241">Þú getur notað eftirfarandi stafi, sem eru skammstafanir fyrir dagbókareiningar.</span><span class="sxs-lookup"><span data-stu-id="52ef9-241">You can use the following letters, which are abbreviations for calendar units.</span></span>

|  <span data-ttu-id="52ef9-242">Stafur</span><span class="sxs-lookup"><span data-stu-id="52ef9-242">Letter</span></span>  |  <span data-ttu-id="52ef9-243">Merking</span><span class="sxs-lookup"><span data-stu-id="52ef9-243">Meaning</span></span>  |
|----------|----------------------|
|<span data-ttu-id="52ef9-244">N</span><span class="sxs-lookup"><span data-stu-id="52ef9-244">C</span></span>|<span data-ttu-id="52ef9-245">Núverandi</span><span class="sxs-lookup"><span data-stu-id="52ef9-245">Current</span></span>|
|<span data-ttu-id="52ef9-246">D</span><span class="sxs-lookup"><span data-stu-id="52ef9-246">D</span></span>|<span data-ttu-id="52ef9-247">Dagur\(s\)</span><span class="sxs-lookup"><span data-stu-id="52ef9-247">Day\(s\)</span></span>|
|<span data-ttu-id="52ef9-248">V</span><span class="sxs-lookup"><span data-stu-id="52ef9-248">W</span></span>|<span data-ttu-id="52ef9-249">Vika\(s\)</span><span class="sxs-lookup"><span data-stu-id="52ef9-249">Week\(s\)</span></span>|
|<span data-ttu-id="52ef9-250">M</span><span class="sxs-lookup"><span data-stu-id="52ef9-250">M</span></span>|<span data-ttu-id="52ef9-251">Mánuður\(s\)</span><span class="sxs-lookup"><span data-stu-id="52ef9-251">Month\(s\)</span></span>|
|<span data-ttu-id="52ef9-252">F</span><span class="sxs-lookup"><span data-stu-id="52ef9-252">Q</span></span>|<span data-ttu-id="52ef9-253">Fjórðungur\(s\)</span><span class="sxs-lookup"><span data-stu-id="52ef9-253">Quarter\(s\)</span></span>|
|<span data-ttu-id="52ef9-254">Á</span><span class="sxs-lookup"><span data-stu-id="52ef9-254">Y</span></span>|<span data-ttu-id="52ef9-255">Ár\(s\)</span><span class="sxs-lookup"><span data-stu-id="52ef9-255">Year\(s\)</span></span>|

<span data-ttu-id="52ef9-256">Hægt er að rita dagsetningarreiknireglu á þrjá vegu.</span><span class="sxs-lookup"><span data-stu-id="52ef9-256">You can construct a date formula in three ways.</span></span>

<span data-ttu-id="52ef9-257">Eftirfarandi dæmi sýnir hvernig á að nota N, fyrir núverandi, og tímaeiningu.</span><span class="sxs-lookup"><span data-stu-id="52ef9-257">The following example shows how to use C, for current, and a time unit.</span></span>

|  <span data-ttu-id="52ef9-258">Segð</span><span class="sxs-lookup"><span data-stu-id="52ef9-258">Expression</span></span>  |  <span data-ttu-id="52ef9-259">Merking</span><span class="sxs-lookup"><span data-stu-id="52ef9-259">Meaning</span></span>  |
|--------------|-----------|
|<span data-ttu-id="52ef9-260">LV</span><span class="sxs-lookup"><span data-stu-id="52ef9-260">CW</span></span>|<span data-ttu-id="52ef9-261">Núverandi vika</span><span class="sxs-lookup"><span data-stu-id="52ef9-261">Current week</span></span>|
|<span data-ttu-id="52ef9-262">LM</span><span class="sxs-lookup"><span data-stu-id="52ef9-262">CM</span></span>|<span data-ttu-id="52ef9-263">Líðandi mánuður</span><span class="sxs-lookup"><span data-stu-id="52ef9-263">Current month</span></span>|

<span data-ttu-id="52ef9-264">Eftirfarandi dæmi sýnir hvernig á að nota tölueiningu og tíma.</span><span class="sxs-lookup"><span data-stu-id="52ef9-264">The following example shows how to use a number and a time unit.</span></span> <span data-ttu-id="52ef9-265">Talan getur ekki verið hærri en 9999.</span><span class="sxs-lookup"><span data-stu-id="52ef9-265">A number cannot be larger than 9999.</span></span>

|  <span data-ttu-id="52ef9-266">Segð</span><span class="sxs-lookup"><span data-stu-id="52ef9-266">Expression</span></span>  |  <span data-ttu-id="52ef9-267">Merking</span><span class="sxs-lookup"><span data-stu-id="52ef9-267">Meaning</span></span>  |
|--------------|-----------|
|<span data-ttu-id="52ef9-268">10D</span><span class="sxs-lookup"><span data-stu-id="52ef9-268">10D</span></span>|<span data-ttu-id="52ef9-269">10 dögum eftir daginn í dag</span><span class="sxs-lookup"><span data-stu-id="52ef9-269">10 days from today</span></span>|
|<span data-ttu-id="52ef9-270">2V</span><span class="sxs-lookup"><span data-stu-id="52ef9-270">2W</span></span>|<span data-ttu-id="52ef9-271">2 vikum eftir daginn í dag</span><span class="sxs-lookup"><span data-stu-id="52ef9-271">2 weeks from today</span></span>|

<span data-ttu-id="52ef9-272">Eftirfarandi dæmi sýnir hvernig á að nota tímaeiningu og tölu.</span><span class="sxs-lookup"><span data-stu-id="52ef9-272">The following example shows how to use a time unit and a number.</span></span>

|  <span data-ttu-id="52ef9-273">Segð</span><span class="sxs-lookup"><span data-stu-id="52ef9-273">Expression</span></span>  |  <span data-ttu-id="52ef9-274">Merking</span><span class="sxs-lookup"><span data-stu-id="52ef9-274">Meaning</span></span>  |
|--------------|-----------|
|<span data-ttu-id="52ef9-275">D10</span><span class="sxs-lookup"><span data-stu-id="52ef9-275">D10</span></span>|<span data-ttu-id="52ef9-276">Næsti 10. dagur mánaðar</span><span class="sxs-lookup"><span data-stu-id="52ef9-276">The next 10th day of a month</span></span>|
|<span data-ttu-id="52ef9-277">VD4</span><span class="sxs-lookup"><span data-stu-id="52ef9-277">WD4</span></span>|<span data-ttu-id="52ef9-278">Næsti fjórði dagur viku \(fimmtudagur\)</span><span class="sxs-lookup"><span data-stu-id="52ef9-278">The next 4th day of a week \(Thursday\)</span></span>|

<span data-ttu-id="52ef9-279">Eftirfarandi dæmi sýnir hvernig eigi að samræma þessi þrjú eyðublöð eins og þörf er á.</span><span class="sxs-lookup"><span data-stu-id="52ef9-279">The following example shows how you can combine these three forms as needed.</span></span>

|  <span data-ttu-id="52ef9-280">Segð</span><span class="sxs-lookup"><span data-stu-id="52ef9-280">Expression</span></span>  |  <span data-ttu-id="52ef9-281">Merking</span><span class="sxs-lookup"><span data-stu-id="52ef9-281">Meaning</span></span>  |
|--------------|-----------|
|<span data-ttu-id="52ef9-282">LM+10D</span><span class="sxs-lookup"><span data-stu-id="52ef9-282">CM+10D</span></span>|<span data-ttu-id="52ef9-283">Núverandi mánuður \+ 10 dagar</span><span class="sxs-lookup"><span data-stu-id="52ef9-283">Current month \+ 10 days</span></span>|

<span data-ttu-id="52ef9-284">Eftirfarandi dæmi sýnir hvernig hægt er að nota mínustákn til að sýna gamla dagsetningu.</span><span class="sxs-lookup"><span data-stu-id="52ef9-284">The following example shows how you can use a minus sign to indicate a date in the past.</span></span>

|  <span data-ttu-id="52ef9-285">Segð</span><span class="sxs-lookup"><span data-stu-id="52ef9-285">Expression</span></span>  |  <span data-ttu-id="52ef9-286">Merking</span><span class="sxs-lookup"><span data-stu-id="52ef9-286">Meaning</span></span>  |
|--------------|-----------|
|<span data-ttu-id="52ef9-287">-1Á</span><span class="sxs-lookup"><span data-stu-id="52ef9-287">-1Y</span></span>|<span data-ttu-id="52ef9-288">1 ári fyrir daginn í dag</span><span class="sxs-lookup"><span data-stu-id="52ef9-288">1 year ago from today</span></span>|

> [!IMPORTANT]
>  <span data-ttu-id="52ef9-289">Ef staðsetningin notar grunndagatal, er dagsetningarreiknireglan sem er til dæmis færð inn í reitinn **Afhendingartími** túlkuð samkvæmt vinnudögum.</span><span class="sxs-lookup"><span data-stu-id="52ef9-289">If the location uses a base calendar, then the date formula that you enter in, for example, the **Shipping Time** field is interpreted according to the calendar working days.</span></span> <span data-ttu-id="52ef9-290">Til dæmis merkir 1B sjö vinnudaga.</span><span class="sxs-lookup"><span data-stu-id="52ef9-290">For example, 1W  means seven working days.</span></span>
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

Note that we have used the US date format MMDDYY here. As [!INCLUDE[d365fin](includes/d365fin_md.md)] becomes available in other markets, you'll be able to use the formats that you are used to.

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

## <a name="entering-times"></a><span data-ttu-id="52ef9-291">Tími færður inn</span><span class="sxs-lookup"><span data-stu-id="52ef9-291">Entering Times</span></span>
<span data-ttu-id="52ef9-292">Þegar þú slærð inn tímana getur þú sett inn hvaða skiltákn án bils sem þú vilt milli eininganna, en ef þú notar tvöfalda tölustafi fyrir hverja einingu allt upp að millisekúndum, þá er þess ekki krafist.</span><span class="sxs-lookup"><span data-stu-id="52ef9-292">When you enter times, you can insert any non-space separators that you want between the units, but if you use double digits for each unit up to milliseconds, then it is not required.</span></span>

<span data-ttu-id="52ef9-293">Þú þarft aðeins að skrifa stærsta einingar sem þú þarfnast; restin verður stillt á núll.</span><span class="sxs-lookup"><span data-stu-id="52ef9-293">You only have to write the largest units that you require; the rest will be set to zero.</span></span> <span data-ttu-id="52ef9-294">Þú getur einnig sleppt öllum f.h./e.h. vísum.</span><span class="sxs-lookup"><span data-stu-id="52ef9-294">You can also leave out any AM/PM indicator.</span></span>

<span data-ttu-id="52ef9-295">Í eftirfarandi töflu birtast mismunandi leiðir til að færa inn tímasetningar og hvernig þær eru túlkaðar:</span><span class="sxs-lookup"><span data-stu-id="52ef9-295">The following table lists the various ways in which times can be entered and how they are interpreted.</span></span> <span data-ttu-id="52ef9-296">Það gerir ráð fyrir svæðisstillingar sem sníða tíma samkvæmt: **Klukkustundir:Mínútur:Sekúndur.Millisekúndur.**</span><span class="sxs-lookup"><span data-stu-id="52ef9-296">It assumes region settings that format times according to: **Hours:Minutes:Seconds.Milliseconds.**</span></span> <span data-ttu-id="52ef9-297">og nota f.h. og e.h. vísa um „f.h.“ og „e.h.“, eftir því sem við á.</span><span class="sxs-lookup"><span data-stu-id="52ef9-297">and use the AM and PM indicators of 'AM' and 'PM', respectively.</span></span>

|<span data-ttu-id="52ef9-298">**Færsla**</span><span class="sxs-lookup"><span data-stu-id="52ef9-298">**Entry**</span></span>      |<span data-ttu-id="52ef9-299">**Túlkun**</span><span class="sxs-lookup"><span data-stu-id="52ef9-299">**Interpretation**</span></span>      |
|---------------|------------------------|
|<span data-ttu-id="52ef9-300">05:23:17</span><span class="sxs-lookup"><span data-stu-id="52ef9-300">05:23:17</span></span>|<span data-ttu-id="52ef9-301">05:23:17</span><span class="sxs-lookup"><span data-stu-id="52ef9-301">05:23:17</span></span>|
|<span data-ttu-id="52ef9-302">5</span><span class="sxs-lookup"><span data-stu-id="52ef9-302">5</span></span>|<span data-ttu-id="52ef9-303">05:00:00</span><span class="sxs-lookup"><span data-stu-id="52ef9-303">05:00:00</span></span>|
|<span data-ttu-id="52ef9-304">5AM</span><span class="sxs-lookup"><span data-stu-id="52ef9-304">5AM</span></span>|<span data-ttu-id="52ef9-305">05:00:00</span><span class="sxs-lookup"><span data-stu-id="52ef9-305">05:00:00</span></span>|
|<span data-ttu-id="52ef9-306">5P</span><span class="sxs-lookup"><span data-stu-id="52ef9-306">5P</span></span>|<span data-ttu-id="52ef9-307">17:00:00</span><span class="sxs-lookup"><span data-stu-id="52ef9-307">17:00:00</span></span>|
|<span data-ttu-id="52ef9-308">12</span><span class="sxs-lookup"><span data-stu-id="52ef9-308">12</span></span>|<span data-ttu-id="52ef9-309">12:00:00</span><span class="sxs-lookup"><span data-stu-id="52ef9-309">12:00:00</span></span>|
|<span data-ttu-id="52ef9-310">12A</span><span class="sxs-lookup"><span data-stu-id="52ef9-310">12A</span></span>|<span data-ttu-id="52ef9-311">00:00:00</span><span class="sxs-lookup"><span data-stu-id="52ef9-311">00:00:00</span></span>|
|<span data-ttu-id="52ef9-312">12P</span><span class="sxs-lookup"><span data-stu-id="52ef9-312">12P</span></span>|<span data-ttu-id="52ef9-313">12:00:00</span><span class="sxs-lookup"><span data-stu-id="52ef9-313">12:00:00</span></span>|
|<span data-ttu-id="52ef9-314">17</span><span class="sxs-lookup"><span data-stu-id="52ef9-314">17</span></span>|<span data-ttu-id="52ef9-315">17:00:00</span><span class="sxs-lookup"><span data-stu-id="52ef9-315">17:00:00</span></span>|
|<span data-ttu-id="52ef9-316">5:30</span><span class="sxs-lookup"><span data-stu-id="52ef9-316">5:30</span></span>|<span data-ttu-id="52ef9-317">05:30:00</span><span class="sxs-lookup"><span data-stu-id="52ef9-317">05:30:00</span></span>|
|<span data-ttu-id="52ef9-318">0530</span><span class="sxs-lookup"><span data-stu-id="52ef9-318">0530</span></span>|<span data-ttu-id="52ef9-319">05:30:00</span><span class="sxs-lookup"><span data-stu-id="52ef9-319">05:30:00</span></span>|
|<span data-ttu-id="52ef9-320">5:30:5</span><span class="sxs-lookup"><span data-stu-id="52ef9-320">5:30:5</span></span>|<span data-ttu-id="52ef9-321">05:30:05</span><span class="sxs-lookup"><span data-stu-id="52ef9-321">05:30:05</span></span>|
|<span data-ttu-id="52ef9-322">053005</span><span class="sxs-lookup"><span data-stu-id="52ef9-322">053005</span></span>|<span data-ttu-id="52ef9-323">05:30:05</span><span class="sxs-lookup"><span data-stu-id="52ef9-323">05:30:05</span></span>|
|<span data-ttu-id="52ef9-324">5:30:5,50</span><span class="sxs-lookup"><span data-stu-id="52ef9-324">5:30:5,50</span></span>|<span data-ttu-id="52ef9-325">05:30:05.5</span><span class="sxs-lookup"><span data-stu-id="52ef9-325">05:30:05.5</span></span>|
|<span data-ttu-id="52ef9-326">053005050</span><span class="sxs-lookup"><span data-stu-id="52ef9-326">053005050</span></span>|<span data-ttu-id="52ef9-327">05:30:05.05</span><span class="sxs-lookup"><span data-stu-id="52ef9-327">05:30:05.05</span></span>|

<span data-ttu-id="52ef9-328">Þú ættir að vera meðvitaðir um að millisekúndur séu túlkuð sem tugabrot.</span><span class="sxs-lookup"><span data-stu-id="52ef9-328">You should be aware that milliseconds are interpreted as decimal notation.</span></span> <span data-ttu-id="52ef9-329">Til dæmis þýðir 3, 30 og 300 þýðir allt 300 millisekúndur, á meðan 03 þýðir 30 og 003 þýðir 3 millisekúndur.</span><span class="sxs-lookup"><span data-stu-id="52ef9-329">So, for example, 3, 30, and 300 all mean 300 milliseconds, while 03 means 30 and 003 means 3 milliseconds.</span></span>

<span data-ttu-id="52ef9-330">Þú getur ekki látið 24:00 tákna miðnætti eða notað gildi sem er hærra en 24:00.</span><span class="sxs-lookup"><span data-stu-id="52ef9-330">You cannot use 24:00 to mean midnight, or use any value greater than 24:00.</span></span>

<span data-ttu-id="52ef9-331">Orðið fyrir „tími“ á tungumálinu sem notað er af [!INCLUDE[d365fin](includes/d365fin_long_md.md)] verður metið við núverandi tíma á tölvunni þinni eða fartækinu.</span><span class="sxs-lookup"><span data-stu-id="52ef9-331">The word for 'time' in the language used by [!INCLUDE[d365fin](includes/d365fin_long_md.md)] will be evaluated to the current time on your computer or mobile device.</span></span> <span data-ttu-id="52ef9-332">Þú getur slegið inn hvaða hluta orðsins sem er, með því að byrja á byrjuninni, eins og til dæmis T eða TÍM.</span><span class="sxs-lookup"><span data-stu-id="52ef9-332">You can enter any part of the word, starting from the beginning, such as t or TIM.</span></span>

## <a name="entering-combined-dates-and-times"></a><span data-ttu-id="52ef9-333">Sláðu inn sameinaða dagsetningar og tíma</span><span class="sxs-lookup"><span data-stu-id="52ef9-333">Entering combined Dates and Times</span></span>
<span data-ttu-id="52ef9-334">Þegar þú slærð inn dagsetningartíma, sem er dagsetning og tími sameinuð í eitt reit, verður þú að slá inn bil milli dagsetningar og tíma.</span><span class="sxs-lookup"><span data-stu-id="52ef9-334">When you enter datetimes, which are a date and time combined into one field, you must enter a space between the date and the time.</span></span> <span data-ttu-id="52ef9-335">Dagsetningarhlutinn getur aðeins innihaldið bil í formi opinbers dagsetningarskiltákns þinna svæðisstillinga.</span><span class="sxs-lookup"><span data-stu-id="52ef9-335">The date part can only contain spaces in the form of the official date separator of your region settings.</span></span> <span data-ttu-id="52ef9-336">Tíminn getur innihaldið bil í kringum f.h./e.h. vísirinn.</span><span class="sxs-lookup"><span data-stu-id="52ef9-336">The time can contain spaces around the AM/PM indicator.</span></span>

<span data-ttu-id="52ef9-337">Einnig er hægt að slá inn aðeins dagsetningu í reit fyrir dagsetningartíma, en ekki er hægt að slá inn aðeins tíma.</span><span class="sxs-lookup"><span data-stu-id="52ef9-337">It is also possible to enter only a date in a datetime field, but it is not possible to enter only a time.</span></span>

<span data-ttu-id="52ef9-338">Eftirfarandi tafla sýnir nokkur dæmi um samsetningar dagsetninga og tíma.</span><span class="sxs-lookup"><span data-stu-id="52ef9-338">The following table lists some examples of date/time combinations.</span></span> <span data-ttu-id="52ef9-339">Svæðisstillingarnar í dæmunum birta dagsetningar í sniðinu dagur\-mánuður\-ár, með f.h./e.h. kennimerkjum, ensku og sunnudegi sem byrjun vikunnar.</span><span class="sxs-lookup"><span data-stu-id="52ef9-339">The region settings in the examples displays dates in the day\-month\-year format, using AM/PM designators, English language, and Sunday as the start of the week.</span></span>

|<span data-ttu-id="52ef9-340">**Færsla**</span><span class="sxs-lookup"><span data-stu-id="52ef9-340">**Entry**</span></span>      |<span data-ttu-id="52ef9-341">**Túlkun**</span><span class="sxs-lookup"><span data-stu-id="52ef9-341">**Interpretation**</span></span>      |
|---------------|------------------------|
|<span data-ttu-id="52ef9-342">08-01-2016 05:48:12 PM</span><span class="sxs-lookup"><span data-stu-id="52ef9-342">08-01-2016 05:48:12 PM</span></span>|<span data-ttu-id="52ef9-343">08\-01\-2016 05:48:12 e.h.</span><span class="sxs-lookup"><span data-stu-id="52ef9-343">08\-01\-2016 05:48:12 PM</span></span>|
|<span data-ttu-id="52ef9-344">131202 132455</span><span class="sxs-lookup"><span data-stu-id="52ef9-344">131202 132455</span></span>|<span data-ttu-id="52ef9-345">13\-12\-2002 13:24:55</span><span class="sxs-lookup"><span data-stu-id="52ef9-345">13\-12\-2002 13:24:55</span></span>|
|<span data-ttu-id="52ef9-346">1-12-02 10</span><span class="sxs-lookup"><span data-stu-id="52ef9-346">1-12-02 10</span></span>|<span data-ttu-id="52ef9-347">01\-12\-2002 10:00:00</span><span class="sxs-lookup"><span data-stu-id="52ef9-347">01\-12\-2002 10:00:00</span></span>|
|<span data-ttu-id="52ef9-348">1.12.02 5</span><span class="sxs-lookup"><span data-stu-id="52ef9-348">1.12.02 5</span></span>|<span data-ttu-id="52ef9-349">01\-12\-2002 05:00:00</span><span class="sxs-lookup"><span data-stu-id="52ef9-349">01\-12\-2002 05:00:00</span></span>|
|<span data-ttu-id="52ef9-350">1.12.02</span><span class="sxs-lookup"><span data-stu-id="52ef9-350">1.12.02</span></span>|<span data-ttu-id="52ef9-351">01\-12\-2002 00:00:00</span><span class="sxs-lookup"><span data-stu-id="52ef9-351">01\-12\-2002 00:00:00</span></span>|
|<span data-ttu-id="52ef9-352">11 12</span><span class="sxs-lookup"><span data-stu-id="52ef9-352">11 12</span></span>|<span data-ttu-id="52ef9-353">11\-vinnudagsetningarmánuður\-vinnudagsetningarár 12:00:00</span><span class="sxs-lookup"><span data-stu-id="52ef9-353">11\-work date month\-work date year 12:00:00</span></span>|
|<span data-ttu-id="52ef9-354">1112 12</span><span class="sxs-lookup"><span data-stu-id="52ef9-354">1112 12</span></span>|<span data-ttu-id="52ef9-355">11\-12\-vinnudagsetningarárið 12:00:00</span><span class="sxs-lookup"><span data-stu-id="52ef9-355">11\-12\-work date year 12:00:00</span></span>|
|<span data-ttu-id="52ef9-356">d eða dagurinn í dag</span><span class="sxs-lookup"><span data-stu-id="52ef9-356">t or today</span></span>|<span data-ttu-id="52ef9-357">dagurinn í dag 00:00:00</span><span class="sxs-lookup"><span data-stu-id="52ef9-357">today's date 00:00:00</span></span>|
|<span data-ttu-id="52ef9-358">d 10:30</span><span class="sxs-lookup"><span data-stu-id="52ef9-358">t 10:30</span></span>|<span data-ttu-id="52ef9-359">dagurinn í dag 10:30:00</span><span class="sxs-lookup"><span data-stu-id="52ef9-359">today's date 10:30:00</span></span>|
|<span data-ttu-id="52ef9-360">d 03:03:03</span><span class="sxs-lookup"><span data-stu-id="52ef9-360">t 3:3:3</span></span>|<span data-ttu-id="52ef9-361">dagurinn í dag 03:03:03</span><span class="sxs-lookup"><span data-stu-id="52ef9-361">today's date 03:03:03</span></span>|
|<span data-ttu-id="52ef9-362">v eða vinnudagsetningin</span><span class="sxs-lookup"><span data-stu-id="52ef9-362">w or workdate</span></span>|<span data-ttu-id="52ef9-363">vinnudagsetningin 00:00:00</span><span class="sxs-lookup"><span data-stu-id="52ef9-363">the working date 00:00:00</span></span>|
|<span data-ttu-id="52ef9-364">m eða mánudagur</span><span class="sxs-lookup"><span data-stu-id="52ef9-364">m or Monday</span></span>|<span data-ttu-id="52ef9-365">Mánudagur vinnudagsetningarvikunnar 00:00:00</span><span class="sxs-lookup"><span data-stu-id="52ef9-365">Monday of the work date week 00:00:00</span></span>|
|<span data-ttu-id="52ef9-366">þr eða þriðjudagur</span><span class="sxs-lookup"><span data-stu-id="52ef9-366">tu or Tuesday</span></span>|<span data-ttu-id="52ef9-367">Þriðjudagur vinnudagsetningarvikunnar 00:00:00</span><span class="sxs-lookup"><span data-stu-id="52ef9-367">Tuesday of the work date week 00:00:00</span></span>|
|<span data-ttu-id="52ef9-368">la eða laugardagur</span><span class="sxs-lookup"><span data-stu-id="52ef9-368">sa or Saturday</span></span>|<span data-ttu-id="52ef9-369">Laugardagur vinnudagsetningarvikunnar 00:00:00</span><span class="sxs-lookup"><span data-stu-id="52ef9-369">Saturday of the work date week 00:00:00</span></span>|
|<span data-ttu-id="52ef9-370">s eða sunnudagur</span><span class="sxs-lookup"><span data-stu-id="52ef9-370">s or Sunday</span></span>|<span data-ttu-id="52ef9-371">Sunnudagur vinnudagsetningarvikunnar 00:00:00</span><span class="sxs-lookup"><span data-stu-id="52ef9-371">Sunday of the work date week 00:00:00</span></span>|
|<span data-ttu-id="52ef9-372">þr 10:30:00</span><span class="sxs-lookup"><span data-stu-id="52ef9-372">tu 10:30</span></span>|<span data-ttu-id="52ef9-373">Þriðjudagur vinnudagsetningarvikunnar 10:30:00</span><span class="sxs-lookup"><span data-stu-id="52ef9-373">Tuesday of the work date week 10:30:00</span></span>|
|<span data-ttu-id="52ef9-374">þr 03:03:03</span><span class="sxs-lookup"><span data-stu-id="52ef9-374">tu 3:3:3</span></span>|<span data-ttu-id="52ef9-375">Þriðjudagur vinnudagsetningarvikunnar 03:03:03</span><span class="sxs-lookup"><span data-stu-id="52ef9-375">Tuesday of the work date week 03:03:03</span></span>|
|<span data-ttu-id="52ef9-376">Þ23 Þ</span><span class="sxs-lookup"><span data-stu-id="52ef9-376">t23 t</span></span>|<span data-ttu-id="52ef9-377">Þriðjudagur 23. viku vinnudagsetningarársins, núgildandi tími dagsins</span><span class="sxs-lookup"><span data-stu-id="52ef9-377">Tuesday of week 23 of the work date year, current time of day</span></span>|
|<span data-ttu-id="52ef9-378">þ23</span><span class="sxs-lookup"><span data-stu-id="52ef9-378">t23</span></span>|<span data-ttu-id="52ef9-379">Þriðjudagur 23. viku vinnudagsetningarársins</span><span class="sxs-lookup"><span data-stu-id="52ef9-379">Tuesday of week 23 of the work date year</span></span>|
|<span data-ttu-id="52ef9-380">þ 23</span><span class="sxs-lookup"><span data-stu-id="52ef9-380">t 23</span></span>|<span data-ttu-id="52ef9-381">Í dag 23:00:00</span><span class="sxs-lookup"><span data-stu-id="52ef9-381">Today 23:00:00</span></span>|
|<span data-ttu-id="52ef9-382">þ-1</span><span class="sxs-lookup"><span data-stu-id="52ef9-382">t-1</span></span>|<span data-ttu-id="52ef9-383">Þriðjudagur 1. viku vinnudagsetningarársins</span><span class="sxs-lookup"><span data-stu-id="52ef9-383">Tuesday of week 1 of the work date year</span></span>|

## <a name="entering-duration"></a><span data-ttu-id="52ef9-384">Færið inn tímalengd</span><span class="sxs-lookup"><span data-stu-id="52ef9-384">Entering Duration</span></span>
<span data-ttu-id="52ef9-385">Sumir reitir í forritinu tákna tímalengd eða magn liðins tíma, í stað tiltekins dagsetningar eða tíma.</span><span class="sxs-lookup"><span data-stu-id="52ef9-385">Some fields in the application represent a duration, or amount of elapsed time, instead of a specific date or time.</span></span> <span data-ttu-id="52ef9-386">Hægt er að færa inn tímalengd sem tölu og mælieiningu.</span><span class="sxs-lookup"><span data-stu-id="52ef9-386">You enter a duration as a number followed by its unit of measure.</span></span>

<span data-ttu-id="52ef9-387">Hér eru nokkur dæmi.</span><span class="sxs-lookup"><span data-stu-id="52ef9-387">Here are some examples.</span></span>

|<span data-ttu-id="52ef9-388">**Lengd**</span><span class="sxs-lookup"><span data-stu-id="52ef9-388">**Duration**</span></span>|<span data-ttu-id="52ef9-389">**Mælieining**</span><span class="sxs-lookup"><span data-stu-id="52ef9-389">**Unit of measure**</span></span>|
|------------|-------------------|
|<span data-ttu-id="52ef9-390">2t</span><span class="sxs-lookup"><span data-stu-id="52ef9-390">2h</span></span>|<span data-ttu-id="52ef9-391">2 klst</span><span class="sxs-lookup"><span data-stu-id="52ef9-391">2 hrs</span></span>|
|<span data-ttu-id="52ef9-392">6t 30 m</span><span class="sxs-lookup"><span data-stu-id="52ef9-392">6h 30 m</span></span>|<span data-ttu-id="52ef9-393">6 klst 30 mín</span><span class="sxs-lookup"><span data-stu-id="52ef9-393">6 hrs 30 mins</span></span>|
|<span data-ttu-id="52ef9-394">6,5t</span><span class="sxs-lookup"><span data-stu-id="52ef9-394">6.5h</span></span>|<span data-ttu-id="52ef9-395">6 klst 30 mín</span><span class="sxs-lookup"><span data-stu-id="52ef9-395">6 hrs 30 mins</span></span>|
|<span data-ttu-id="52ef9-396">90m</span><span class="sxs-lookup"><span data-stu-id="52ef9-396">90m</span></span>|<span data-ttu-id="52ef9-397">1 klst 30 mín</span><span class="sxs-lookup"><span data-stu-id="52ef9-397">1 hr 30 mins</span></span>|
|<span data-ttu-id="52ef9-398">2d 6t 30m</span><span class="sxs-lookup"><span data-stu-id="52ef9-398">2d 6h 30m</span></span>|<span data-ttu-id="52ef9-399">2 dagar 6 klst 30 mín</span><span class="sxs-lookup"><span data-stu-id="52ef9-399">2 days 6 hrs 30 mins</span></span>|
|<span data-ttu-id="52ef9-400">2d 6t 30m 56s 600ms</span><span class="sxs-lookup"><span data-stu-id="52ef9-400">2d 6h 30m 56s 600ms</span></span>|<span data-ttu-id="52ef9-401">2 dagar 6 klst 30 mín 56 sek 600 millis</span><span class="sxs-lookup"><span data-stu-id="52ef9-401">2 days 6 hrs 30 mins 56 secs 600 msecs</span></span>|

<span data-ttu-id="52ef9-402">Einnig er hægt að færa inn tölu og þá er henni sjálfkrafa breytt í tímalengd.</span><span class="sxs-lookup"><span data-stu-id="52ef9-402">You can also enter a number, which will be automatically converted to a duration.</span></span> <span data-ttu-id="52ef9-403">Tölunni sem færð er inn er breytt samkvæmt sjálfgefnu mælieiningunni sem hefur verið tilgreind fyrir reitinn tímalengd.</span><span class="sxs-lookup"><span data-stu-id="52ef9-403">The number you enter is converted according to the default unit of measure that has been specified for the duration field.</span></span>

<span data-ttu-id="52ef9-404">Hægt er að sjá hvaða mælieining er notuð í reitnum tímalengd með því að færa inn tölu og sjá í hvaða mælieiningu kerfið færir hana í.</span><span class="sxs-lookup"><span data-stu-id="52ef9-404">To see what unit of measure is being used in a duration field, enter a number and see which unit of measure it is converted to.</span></span>

<span data-ttu-id="52ef9-405">Ef mælieiningin er til dæmis klukkustund, er númerinu 5 breytt í 5 klukkustundir.</span><span class="sxs-lookup"><span data-stu-id="52ef9-405">For example, if the unit of measure is hours, the number 5 is converted to 5 hrs.</span></span>

## <a name="see-also"></a><span data-ttu-id="52ef9-406">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="52ef9-406">See Also</span></span>
<span data-ttu-id="52ef9-407">[Unnið með [!INCLUDE[d365fin](includes/d365fin_long_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="52ef9-407">[Working with [!INCLUDE[d365fin](includes/d365fin_long_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="52ef9-408">Dagsetning útreiknings fyrir kaup</span><span class="sxs-lookup"><span data-stu-id="52ef9-408">Date Calculation for Purchases</span></span>](purchasing-date-calculation-for-purchases.md)  
[<span data-ttu-id="52ef9-409">Skilgreining skilyrða í síum</span><span class="sxs-lookup"><span data-stu-id="52ef9-409">Entering Criteria in Filters </span></span>](ui-enter-criteria-filters.md)  
