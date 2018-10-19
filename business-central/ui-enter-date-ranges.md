---
title: "Innsláttur dagsetninga og tíma í Business Central | Microsoft Docs"
description: "Lærðu hvernig á að slá inn dagsetningar og tíma, þar á meðal ýmsar ábendingar um framleiðni, svo sem hraðskrift, segð og afmarkanir. Sía lista eða skýrslur niður í tiltekna dagsetningu eða tímabil."
documentationcenter: 
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: dates, reporting, filter, calendar, shorthand, range
ms.date: 10/01/2018
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 8717d60a8449ca300eaf9c1a5c4b137ea1a1a247
ms.contentlocale: is-is
ms.lasthandoff: 09/28/2018

---

# <a name="working-with-calendar-dates-and-times"></a><span data-ttu-id="4df69-104">Vinna með dagsetningar og tíma í dagatali</span><span class="sxs-lookup"><span data-stu-id="4df69-104">Working with Calendar Dates and Times</span></span>
[!INCLUDE[d365fin](includes/d365fin_long_md.md)] <span data-ttu-id="4df69-105">býður upp á margar leiðir til að slá inn dagsetningar og tíma, þar með talin öflugar aðgerðir sem flýta fyrir gagnaskráningu eða hjálpa þér að skrifa flókna dagatalssegðir.</span><span class="sxs-lookup"><span data-stu-id="4df69-105">offers multiple ways to enter dates and times, including powerful features that accelerate data entry, or help you write complex calendar expressions.</span></span> <span data-ttu-id="4df69-106">Það eru ýmsar staðir í forritinu þar sem þú getur slegið inn dagsetningar og tíma í reitum.</span><span class="sxs-lookup"><span data-stu-id="4df69-106">There are various places throughout the application where you can enter dates and times in fields.</span></span> <span data-ttu-id="4df69-107">Til dæmis, í sölupöntun, getur þú stillt afhendingardagsetningu.</span><span class="sxs-lookup"><span data-stu-id="4df69-107">For example, on a sales order, you can set the shipment date.</span></span> <span data-ttu-id="4df69-108">Þegar verið er að afmarka lista eða skýrslugögn er hægt að slá inn dagsetningar og tíma til að staðsetja aðeins þau gögn sem þú hefur áhuga á.</span><span class="sxs-lookup"><span data-stu-id="4df69-108">When filtering lists or report data, you can enter dates and times to pinpoint only the data that you are interested in.</span></span>

## <a name="check-your-region-and-language-settings"></a><span data-ttu-id="4df69-109">Athugaðu svæði og tungumálastillingar</span><span class="sxs-lookup"><span data-stu-id="4df69-109">Check your region and language settings</span></span>
<span data-ttu-id="4df69-110">[**Mínar stillingar**](https://businesscentral.dynamics.com?page=9176 "Farðu beint á notendastillingarsíðuna þína í Business Central") síðan tilgreinir **svæði** og **tungumál** sem þú notar í forritinu.</span><span class="sxs-lookup"><span data-stu-id="4df69-110">The [**My Settings**](https://businesscentral.dynamics.com?page=9176 "Go directly to your user settings page in Business Central") page specifies the **Region** and **Language** that you are using in the application.</span></span> <span data-ttu-id="4df69-111">Þessar stillingar hafa áhrif á hvernig þú slærð inn dagsetningar og tíma.</span><span class="sxs-lookup"><span data-stu-id="4df69-111">These settings influence how you enter dates and times.</span></span> 

-   <span data-ttu-id="4df69-112">**Svæði** stillingin ákvarðar hvernig dagsetningar, tímasetningar, númer og gjaldmiðlar eru sýndir eða forsniðnir.</span><span class="sxs-lookup"><span data-stu-id="4df69-112">The **Region** setting determines how dates, times, numbers, and currencies are shown or formatted.</span></span>

-   <span data-ttu-id="4df69-113">Fyrir dagsetningamynstur sem fela í sér orð, tungumálið orðanna sem þú notar verða að vera í samræmi við **tungumál** stillinguna.</span><span class="sxs-lookup"><span data-stu-id="4df69-113">For date patterns that involve words, the language of the words that you use must correspond to the **Language** setting.</span></span>

> [!NOTE]
> [!INCLUDE[d365fin](includes/d365fin_long_md.md)] <span data-ttu-id="4df69-114">notar gregoríska dagatalskerfið.</span><span class="sxs-lookup"><span data-stu-id="4df69-114">uses the Gregorian calendar system.</span></span>

<!-- 
The following sections describe how you can enter dates, times, datetimes, durations, date ranges, and how you use date formulas.
-->
## <a name="entering-dates"></a><span data-ttu-id="4df69-115">Dagsetningar færðar inn</span><span class="sxs-lookup"><span data-stu-id="4df69-115">Entering Dates</span></span>
<span data-ttu-id="4df69-116">Í dagsetningarreitinn getur þú slegið inn dagsetningu með því að nota staðlaða sniðið fyrir svæðisstillingu þína.</span><span class="sxs-lookup"><span data-stu-id="4df69-116">In a date field, you can enter a date using the standard format for your region setting.</span></span> <span data-ttu-id="4df69-117">Mismunandi svæði geta notað mismunandi skiltákn milli daga, mánaða og ára.</span><span class="sxs-lookup"><span data-stu-id="4df69-117">Different regions can use different separators between the days, months and years.</span></span> <span data-ttu-id="4df69-118">Til dæmis, sum svæði nota bandstrik (mm-dd-áááá) og önnur nota áfram skástrik (mm/dd/áááá).</span><span class="sxs-lookup"><span data-stu-id="4df69-118">For example, some regions use dashes (mm-dd-yyyy) and others use forward slashes (mm/dd/yyyy).</span></span> <span data-ttu-id="4df69-119">Hins vegar getur þú notað hvaða skiltákn sem er, jafnvel bil, og dagsetningin verður sjálfkrafa breytt til að nota skiltákn sem passa við svæðið þitt.</span><span class="sxs-lookup"><span data-stu-id="4df69-119">However, you can use any separators, even a space, and the date will automatically be changed to use separators that match your region.</span></span>

<span data-ttu-id="4df69-120">Athugaðu að sniðið sem dagsetningar eru birtar á í prentuðum skýrslum eða skjölum sendum í tölvupósti eru ekki undir áhrifum af persónulegu vali þínu á svæðisstillingu.</span><span class="sxs-lookup"><span data-stu-id="4df69-120">Note that the format in which dates are displayed on printed reports or emailed documents is not influenced by your personal choice of region setting.</span></span>

<span data-ttu-id="4df69-121">Til að vinna á afkastameiri hátt með dagsetningar og tíma geturðu notað eitthvað af þeim aðferðum eða sniði sem lýst er í eftirfarandi köflum.</span><span class="sxs-lookup"><span data-stu-id="4df69-121">To work more productively with dates and times, you can use any of the methods or formats that are described in the following sections.</span></span> 

### <a name="picking-dates-from-the-calendar"></a><span data-ttu-id="4df69-122">Velja dagsetningar úr dagatalinu</span><span class="sxs-lookup"><span data-stu-id="4df69-122">Picking dates from the calendar</span></span>
<span data-ttu-id="4df69-123">Allir reitir sem sýna dagbókartákn geta verið stilltar með dagsetningarvali dagatals.</span><span class="sxs-lookup"><span data-stu-id="4df69-123">Any field displaying a calendar icon can be set using the calendar date picker.</span></span> <span data-ttu-id="4df69-124">Til að birta dagsetningarval dagatals skaltu virkja dagatalstáknið eða ýta á Ctrl + Home flýtilykilinn í reitnum.</span><span class="sxs-lookup"><span data-stu-id="4df69-124">To display the calendar date picker, activate the calendar icon or press the Ctrl + Home keyboard shortcut in the field.</span></span>

<span data-ttu-id="4df69-125">![Dagsetningarreitir](media/ui-date-field.png "Dæmi um dagsetningarreit")</span><span class="sxs-lookup"><span data-stu-id="4df69-125">![Date fields](media/ui-date-field.png "Example of a date field")</span></span>

<span data-ttu-id="4df69-126">Sjá einnig [Flýtilyklar í dagsetningarvali dagatals](keyboard-shortcuts.md#calendarshortcuts)</span><span class="sxs-lookup"><span data-stu-id="4df69-126">See also [Keyboard Shortcuts in the calendar date picker](keyboard-shortcuts.md#calendarshortcuts)</span></span>

### <a name="today"></a><span data-ttu-id="4df69-127">Í dag</span><span class="sxs-lookup"><span data-stu-id="4df69-127">Today</span></span>
<span data-ttu-id="4df69-128">Sláðu inn orðið fyrir `today`, á tungumáli sem er stillt af **Tungumál** stillingu, sem stillir daginn á núverandi dagsetningu.</span><span class="sxs-lookup"><span data-stu-id="4df69-128">Enter the word for `today`, in the language set by **Language** setting, that will set the date to the current date.</span></span> <span data-ttu-id="4df69-129">Í stað þess að slá inn allt orðið geturðu slegið inn hluta af orðinu, með því að byrja á byrjuninni, eins og `t` eða `tod`, svo lengi sem það er ekki líka byrjun annars orðs.</span><span class="sxs-lookup"><span data-stu-id="4df69-129">Instead of entering the entire word, you can enter part of the word, starting from the beginning, such as `t` or `tod`, as long as it is not also the start of another word.</span></span>

### <a name="day-week-year-pattern"></a><span data-ttu-id="4df69-130">Dagur\-vika\-ár mynstur</span><span class="sxs-lookup"><span data-stu-id="4df69-130">Day\-week\-year pattern</span></span>
<span data-ttu-id="4df69-131">Þú getur slegið inn dagsetningu sem vikudag og síðan vikunúmer og, ef þú vilt, ár.</span><span class="sxs-lookup"><span data-stu-id="4df69-131">You can enter a date as a weekday followed by a week number and, optionally, a year.</span></span> <span data-ttu-id="4df69-132">Til dæmis þýðir `Mon25` eða `mon25` mánudagur í viku 25.</span><span class="sxs-lookup"><span data-stu-id="4df69-132">For example, `Mon25` or `mon25` means Monday in week 25.</span></span> <span data-ttu-id="4df69-133">Ef þú slærð ekki inn ár er ár vinnudagsetningar notað.</span><span class="sxs-lookup"><span data-stu-id="4df69-133">If you do not enter a year, the year of the work date is used.</span></span>

<span data-ttu-id="4df69-134">Í stað þess að slá inn allt orðið fyrir vikudaginn getur þú slegið inn hluta af orðinu, með því að byrja á byrjuninni.</span><span class="sxs-lookup"><span data-stu-id="4df69-134">Instead of entering the entire word for the day of the week, you can enter part of the word, starting from the beginning.</span></span> <span data-ttu-id="4df69-135">Ef um er að ræða árekstur (eins og til dæmis `s` sem gæti verið laugardagur eða sunnudagur) eru dagarnir metnir í samræmi við svæðisstillingu.</span><span class="sxs-lookup"><span data-stu-id="4df69-135">In case of conflicts (such as with `s` which could be Saturday or Sunday), the days are evaluated according to the region setting.</span></span> <span data-ttu-id="4df69-136">Inntakið er fyrst metið út frá `workdate` og `today` einnig, svo hafðu þetta í huga þegar skammstafað er.</span><span class="sxs-lookup"><span data-stu-id="4df69-136">The input is first evaluated against `workdate` and `today` as well, so keep this in mind when abbreviating.</span></span> <span data-ttu-id="4df69-137">Til dæmis, `t` þýðir nú þegar í dag, svo það getur ekki þýtt þriðjudagur eða fimmtudagur.</span><span class="sxs-lookup"><span data-stu-id="4df69-137">For example, `t` already means today, so it cannot mean Tuesday or Thursday.</span></span>

<span data-ttu-id="4df69-138">Vikunúmersskemað er alltaf ISO 8601, þar sem vika 1 er vikan sem inniheldur 4. janúar, eða vikan sem inniheldur fyrsta fimmtudag ársins.</span><span class="sxs-lookup"><span data-stu-id="4df69-138">The week number scheme is always ISO 8601, where week 1 is the week with 4 January in it, or the week with the first Thursday of the year.</span></span>

### <a name="digit-patterns"></a><span data-ttu-id="4df69-139">Tölustafamynstur</span><span class="sxs-lookup"><span data-stu-id="4df69-139">Digit patterns</span></span>
<span data-ttu-id="4df69-140">Í dagsetningarreit má færa inn tvær, fjórar, sex eða átta tölur:</span><span class="sxs-lookup"><span data-stu-id="4df69-140">In a date field you can enter two, four, six, or eight digits:</span></span>

-   <span data-ttu-id="4df69-141">Ef aðeins tvær tölur eru færðar inn þá túlkar kerfið þær sem daginn og bætir við mánuði og ári vinnudagsetningar.</span><span class="sxs-lookup"><span data-stu-id="4df69-141">If you enter only two digits, this is interpreted as the day, and it will add the month and the year of the work date.</span></span>

-   <span data-ttu-id="4df69-142">Ef færðar eru inn fjórar tölur þá túlkar kerfið þær sem daginn og mánuðinn og bætir við ári vinnudagsetningar.</span><span class="sxs-lookup"><span data-stu-id="4df69-142">If you enter four digits, this is interpreted as the day and the month, and it will add the year of the work date.</span></span> <span data-ttu-id="4df69-143">Röð dags og mánaðar ræðst af svæðisstillingum þínum.</span><span class="sxs-lookup"><span data-stu-id="4df69-143">The order of the day and month is determined by your region settings.</span></span> <span data-ttu-id="4df69-144">Jafnvel þótt svæðisstillingar þínar séu með árið fyrir daginn og mánuðinn eru fjórir tölustafir túlkaðir sem dagur og mánuður.</span><span class="sxs-lookup"><span data-stu-id="4df69-144">Even if your region settings have the year before the day and month, four digits are interpreted as the day and month.</span></span>

-   <span data-ttu-id="4df69-145">Ef sú dagsetning sem færa á inn er á bilinu 01/01/1930 til 31/12/2029 má færa árið inn í tveimur tölum; annars skal færa árið inn með fjórum tölum.</span><span class="sxs-lookup"><span data-stu-id="4df69-145">If the date you want to enter is in the range 01/01/1930 through 12/31/2029, you can enter the year with two digits; otherwise, enter the year with four digits.</span></span>

### <a name="current-work-date"></a><span data-ttu-id="4df69-146">Núverandi vinnudagsetning</span><span class="sxs-lookup"><span data-stu-id="4df69-146">Current work date</span></span>
<span data-ttu-id="4df69-147">Eiginleiki vinnudagsetningarinnar gerir þér kleift að skrá færslur með því að nota dagsetningu sem er frábrugðið núverandi dagsetningu.</span><span class="sxs-lookup"><span data-stu-id="4df69-147">The work date feature allows you to record transations using a date that is different from the current date.</span></span>

<span data-ttu-id="4df69-148">Orðið fyrir „vinnudagsetning“ á tungumáli, sem stillt er með **Tungumál** stillingu, færir dagsetninguna í núverandi vinnudagsetningu, sem er tilgreindur á [**Mínar stillingar**](https://businesscentral.dynamics.com?page=9176 "Farðu beint á notendastillingarsíðuna þína í Business Central") síðuna.</span><span class="sxs-lookup"><span data-stu-id="4df69-148">The word for 'workdate', in the language set by **Language** setting, will set the date to the currently set work date that is specified on the [**My Settings**](https://businesscentral.dynamics.com?page=9176 "Go directly to your user settings page in Business Central") page.</span></span> <span data-ttu-id="4df69-149">Í stað þess að slá inn allt orðið geturðu slegið inn hluta af orðinu, með því að byrja á byrjuninni, eins og til dæmis „v“ fyrir „vinnu“.</span><span class="sxs-lookup"><span data-stu-id="4df69-149">Instead of entering the entire word, you can enter part of the word, starting from the beginning, such as 'w' or 'work'.</span></span>

<span data-ttu-id="4df69-150">Ef þú hefur ekki skilgreint vinnudagsetningu, verður núverandi dagsetning notuð sem vinnudagsetning.</span><span class="sxs-lookup"><span data-stu-id="4df69-150">If you have not defined a work date, the current date will be used as the work date.</span></span> <span data-ttu-id="4df69-151">Handhægt gæti verið að nota vinnudagsetningar ef verið er að nota margar færslur með aðra dagsetningu en dagsins í dag.</span><span class="sxs-lookup"><span data-stu-id="4df69-151">You may want to use a work date if you have many transactions with a date other than today's date.</span></span>

<span data-ttu-id="4df69-152">Sjá einnig [Breyting grunnstillingar, svo sem vinnudagsetning](ui-change-basic-settings.md#work-date)</span><span class="sxs-lookup"><span data-stu-id="4df69-152">See also [Changing Basic Settings, such as the Work Date](ui-change-basic-settings.md#work-date)</span></span>

### <a name="closing-date"></a><span data-ttu-id="4df69-153">Lokunardagsetning</span><span class="sxs-lookup"><span data-stu-id="4df69-153">Closing Date</span></span>
<span data-ttu-id="4df69-154">Þegar reikningsári er lokað er hægt að nota lokunardagsetningu til að sýna að færsla sé lokunarfærsla.</span><span class="sxs-lookup"><span data-stu-id="4df69-154">When you close a fiscal year, you can use closing dates to indicate that an entry is a closing entry.</span></span> <span data-ttu-id="4df69-155">Lokunardagsetning er í raun milli tveggja dagsetninga, til dæmis 31. des. og 1. jan.</span><span class="sxs-lookup"><span data-stu-id="4df69-155">A closing date technically is between two dates, for example between Dec 31 and Jan 1.</span></span>

<span data-ttu-id="4df69-156">Til að tilgreina að dagsetning sé lokadagsetning skaltu setja `C` rétt fyrir dagsetningu, svo sem `C123101`.</span><span class="sxs-lookup"><span data-stu-id="4df69-156">To specify that a date is a closing date, put `C` just before the date, such as `C123101`.</span></span> <span data-ttu-id="4df69-157">Þetta er hægt að nota ásamt öllum dagsetningarmynstri.</span><span class="sxs-lookup"><span data-stu-id="4df69-157">This can be used in combination with all the date patterns.</span></span>

### <a name="examples"></a><span data-ttu-id="4df69-158">Dæmi</span><span class="sxs-lookup"><span data-stu-id="4df69-158">Examples</span></span>
<span data-ttu-id="4df69-159">Eftirfarandi tafla inniheldur dæmi um dagsetningar þar sem öll snið eru notuð.</span><span class="sxs-lookup"><span data-stu-id="4df69-159">The following table contains examples of dates using all the formats.</span></span> <span data-ttu-id="4df69-160">Það er gert ráð fyrir svæðisstillingum sem sníðir dagsetningar samkvæmt: **ár.mánuður.dagur.**, viku sem hefst á mánudag og ensku.</span><span class="sxs-lookup"><span data-stu-id="4df69-160">It assumes region settings that format dates according to: **year.month.day.**, a week starting on Monday, and the English language.</span></span>

|<span data-ttu-id="4df69-161">**Færsla**</span><span class="sxs-lookup"><span data-stu-id="4df69-161">**Entry**</span></span>      |<span data-ttu-id="4df69-162">**Túlkun**</span><span class="sxs-lookup"><span data-stu-id="4df69-162">**Interpretation**</span></span>      |
|---------------|------------------------|
|`2018.12.31.`|<span data-ttu-id="4df69-163">2018.12.31.</span><span class="sxs-lookup"><span data-stu-id="4df69-163">2018.12.31.</span></span>|
|`181231`|<span data-ttu-id="4df69-164">2018.12.31.</span><span class="sxs-lookup"><span data-stu-id="4df69-164">2018.12.31.</span></span>|
|`18.12.31.`|<span data-ttu-id="4df69-165">2018.12.31.</span><span class="sxs-lookup"><span data-stu-id="4df69-165">2018.12.31.</span></span>|
|`18.12.31.`|<span data-ttu-id="4df69-166">2018.12.31.</span><span class="sxs-lookup"><span data-stu-id="4df69-166">2018.12.31.</span></span>|
|`20181231`|<span data-ttu-id="4df69-167">2018.12.31.</span><span class="sxs-lookup"><span data-stu-id="4df69-167">2018.12.31.</span></span>|
|`18/12,31`|<span data-ttu-id="4df69-168">2018.12.31.</span><span class="sxs-lookup"><span data-stu-id="4df69-168">2018.12.31.</span></span>|
|`11`|<span data-ttu-id="4df69-169">vinnudagsetning ár.vinnudagsetning mánuður.11.</span><span class="sxs-lookup"><span data-stu-id="4df69-169">work date year.work date month.11.</span></span>|
|`1112`|<span data-ttu-id="4df69-170">vinnudagsetningarár.11.12.</span><span class="sxs-lookup"><span data-stu-id="4df69-170">work date year.11.12.</span></span>|
|<span data-ttu-id="4df69-171">`t` eða `today`</span><span class="sxs-lookup"><span data-stu-id="4df69-171">`t` or `today`</span></span>|<span data-ttu-id="4df69-172">dagurinn í dag</span><span class="sxs-lookup"><span data-stu-id="4df69-172">today's date</span></span>|
|<span data-ttu-id="4df69-173">`w` eða `workdate`</span><span class="sxs-lookup"><span data-stu-id="4df69-173">`w` or `workdate`</span></span>|<span data-ttu-id="4df69-174">vinnudagsetningin</span><span class="sxs-lookup"><span data-stu-id="4df69-174">the working date</span></span>|
|<span data-ttu-id="4df69-175">`m` eða `Monday`</span><span class="sxs-lookup"><span data-stu-id="4df69-175">`m` or `Monday`</span></span>|<span data-ttu-id="4df69-176">Mánudagur vinnudagsetningarvikunnar</span><span class="sxs-lookup"><span data-stu-id="4df69-176">Monday of the work date week</span></span>|
|<span data-ttu-id="4df69-177">`tu` eða `Tuesday`</span><span class="sxs-lookup"><span data-stu-id="4df69-177">`tu` or `Tuesday`</span></span>|<span data-ttu-id="4df69-178">Þriðjudagur vinnudagsetningarvikunnar</span><span class="sxs-lookup"><span data-stu-id="4df69-178">Tuesday of the work date week</span></span>|
|<span data-ttu-id="4df69-179">`sa` eða `Saturday`</span><span class="sxs-lookup"><span data-stu-id="4df69-179">`sa` or `Saturday`</span></span>|<span data-ttu-id="4df69-180">Laugardagur vinnudagsetningarvikunnar</span><span class="sxs-lookup"><span data-stu-id="4df69-180">Saturday of the work date week</span></span>|
|<span data-ttu-id="4df69-181">`s` eða `Sunday`</span><span class="sxs-lookup"><span data-stu-id="4df69-181">`s` or `Sunday`</span></span>|<span data-ttu-id="4df69-182">Sunnudagur vinnudagsetningarvikunnar</span><span class="sxs-lookup"><span data-stu-id="4df69-182">Sunday of the work date week</span></span>|
|`t23`|<span data-ttu-id="4df69-183">Þriðjudagur 23. viku vinnudagsetningarársins</span><span class="sxs-lookup"><span data-stu-id="4df69-183">Tuesday of week 23 of the work date year</span></span>|
|`t 23`|<span data-ttu-id="4df69-184">Þriðjudagur 23. viku vinnudagsetningarársins</span><span class="sxs-lookup"><span data-stu-id="4df69-184">Tuesday of week 23 of the work date year</span></span>|
|`t-1`|<span data-ttu-id="4df69-185">Þriðjudagur 1. viku vinnudagsetningarársins</span><span class="sxs-lookup"><span data-stu-id="4df69-185">Tuesday of week 1 of the work date year</span></span>|

##  <a name="BKMK_SettingDateRanges"></a> <span data-ttu-id="4df69-186">Stillingarbil</span><span class="sxs-lookup"><span data-stu-id="4df69-186">Setting Ranges</span></span>
<span data-ttu-id="4df69-187">Á listum, samtölum og skýrslum er hægt að stilla síur á dagsetningar, tímum og tímabilum sem innihalda upphafsgildi og mögulega endanlegt gildi til að birta aðeins gögnin sem eru í því bili.</span><span class="sxs-lookup"><span data-stu-id="4df69-187">On lists, totals and reports, you can set filters on dates, times and datetimes containing a start value and optionally an end value to display only the data contained in that range.</span></span> <span data-ttu-id="4df69-188">Stöðluðu reglurnar eiga við um það hvernig þú stillir dagsetningarsvið.</span><span class="sxs-lookup"><span data-stu-id="4df69-188">The standard rules apply to the way you set date ranges.</span></span>

|<span data-ttu-id="4df69-189">**Merking**</span><span class="sxs-lookup"><span data-stu-id="4df69-189">**Meaning**</span></span>|<span data-ttu-id="4df69-190">**Dæmi um segð (dagsetning)**</span><span class="sxs-lookup"><span data-stu-id="4df69-190">**Sample expression (Date)**</span></span>|<span data-ttu-id="4df69-191">**Gögn sem eru höfð með síunni**</span><span class="sxs-lookup"><span data-stu-id="4df69-191">**Data included in the filter**</span></span>|
|-----------|---------------------|--------------------|
|<span data-ttu-id="4df69-192">Millibil</span><span class="sxs-lookup"><span data-stu-id="4df69-192">Interval</span></span>|<span data-ttu-id="4df69-193">`12 15 00..01 15 01`  \n`..12 15 00`</span><span class="sxs-lookup"><span data-stu-id="4df69-193">`12 15 00..01 15 01`  \n`..12 15 00`</span></span>|<span data-ttu-id="4df69-194">Skrár með dagsetningar á milli og að meðtöldum 12 15 00 og 01 15 01.</span><span class="sxs-lookup"><span data-stu-id="4df69-194">Records with dates between and including 12 15 00 and 01 15 01.</span></span>  <span data-ttu-id="4df69-195">\nSkrár með dagsetningar 12 15 00 eða fyrr.</span><span class="sxs-lookup"><span data-stu-id="4df69-195">\nRecords with dates of 12 15 00 or earlier.</span></span>|
|<span data-ttu-id="4df69-196">Annaðhvort eða</span><span class="sxs-lookup"><span data-stu-id="4df69-196">Either/or</span></span>|<span data-ttu-id="4df69-197">„12 15 00</span><span class="sxs-lookup"><span data-stu-id="4df69-197">\`12 15 00</span></span>|<span data-ttu-id="4df69-198">12 16 00“</span><span class="sxs-lookup"><span data-stu-id="4df69-198">12 16 00\`</span></span>|<span data-ttu-id="4df69-199">Skrár með dagsetningar annaðhvort 12 15 00 eða 12 16 00.</span><span class="sxs-lookup"><span data-stu-id="4df69-199">Records with dates of either 12 15 00 or 12 16 00.</span></span> <span data-ttu-id="4df69-200">Ef það eru skrár með dagsetningar á báðum dögum verða þær allar birtar.</span><span class="sxs-lookup"><span data-stu-id="4df69-200">If there are records with dates on both days, they will all be displayed.</span></span>|
|<span data-ttu-id="4df69-201">Samsetning</span><span class="sxs-lookup"><span data-stu-id="4df69-201">Combination</span></span>|<span data-ttu-id="4df69-202">„12 15 00</span><span class="sxs-lookup"><span data-stu-id="4df69-202">\`12 15 00</span></span>|<span data-ttu-id="4df69-203">12 01 00..12 10 00`  \n`..12 14 00</span><span class="sxs-lookup"><span data-stu-id="4df69-203">12 01 00..12 10 00`  \n`..12 14 00</span></span>|<span data-ttu-id="4df69-204">12 30 00 ..“</span><span class="sxs-lookup"><span data-stu-id="4df69-204">12 30 00..\`</span></span>|<span data-ttu-id="4df69-205">Skrár með dagsetningar 12 15 00 eða á dagsetningum á milli og að meðtöldum 12 01 00 og 12 10 00.</span><span class="sxs-lookup"><span data-stu-id="4df69-205">Records with dates of 12 15 00 or on dates between and including 12 01 00 and 12 10 00.</span></span>  <span data-ttu-id="4df69-206">\nSkrár með dagsetningar 12 14 00 eða fyrr, eða 12 30 00 eða síðar, það er, allar skrár nema þær sem eru með dagsetningar á milli og að meðtöldum 12 15 00 og 12 29 00.</span><span class="sxs-lookup"><span data-stu-id="4df69-206">\nRecords with dates of 12 14 00 or earlier, or dates of 12 30 00 or later, that is, all records except those with dates between and including 12 15 00 and 12 29 00.</span></span>|

<span data-ttu-id="4df69-207">Þú getur notað öll gild snið í síum dagsetningarbils.</span><span class="sxs-lookup"><span data-stu-id="4df69-207">You can use any of the valid formats in date range filters.</span></span> <span data-ttu-id="4df69-208">Til dæmis, `mon14 3..t 4p` beitt á reitarniðurstöður dagsetningartíma í síu frá kl. 03:00 á mánudag í viku 14 á núgildandi vinnudagsetningarári, innifalið, þar til í dag kl. 16:00, innifalið.</span><span class="sxs-lookup"><span data-stu-id="4df69-208">For example, `mon14 3..t 4p` applied on a datetime field results in a filter from 3 AM on Monday in week 14 of the current work date year, inclusive, until today at 4PM, inclusive.</span></span>


## <a name="using-date-formulas"></a><span data-ttu-id="4df69-209">Notkun dagsetningarreiknireglna</span><span class="sxs-lookup"><span data-stu-id="4df69-209">Using Date Formulas</span></span>
<span data-ttu-id="4df69-210">Dagsetningarregla er stutt, skammstöfuð samsetning stafa og tölustafa sem tilgreinir hvernig skal reikna út dagsetningar.</span><span class="sxs-lookup"><span data-stu-id="4df69-210">A date formula is a short, abbreviated combination of letters and numbers that specifies how to calculate dates.</span></span> <span data-ttu-id="4df69-211">Þú getur slegið inn dagsetningarformúlur í ýmsa reiknireiti fyrir dagsetningar eða síur.</span><span class="sxs-lookup"><span data-stu-id="4df69-211">You can enter date formulas in various date calculation fields or filters.</span></span>

> [!NOTE]
>  <span data-ttu-id="4df69-212">Dagurinn í dag, fyrir upphaf tímabilsins, er með í öllum reitum fyrir reiknireglur dagsetninga.</span><span class="sxs-lookup"><span data-stu-id="4df69-212">In all data formula fields, one day is automatically included to cover today as the day when the period starts.</span></span> <span data-ttu-id="4df69-213">Í samræmi við það, ef fært er inn `1W`, til dæmis, er tímabilið í raun átta dagar þar sem dagurinn í dag er tekinn með.</span><span class="sxs-lookup"><span data-stu-id="4df69-213">Accordingly, for example, if you enter `1W`, then the period is actually eight days because today is included.</span></span> <span data-ttu-id="4df69-214">Til að tilgreina sjö daga tímabil \(eina sanna viku\) þ.m.t. upphafsdagsetningu tímabilsins, þá verður þú að slá inn `6D` eða `1W-1D` .</span><span class="sxs-lookup"><span data-stu-id="4df69-214">To specify a period of seven days \(one true week\) including the period starting date, then you must enter `6D` or `1W-1D`.</span></span>

<span data-ttu-id="4df69-215">Hér eru nokkur dæmi um hvernig nota má dagsetningarreiknireglur:</span><span class="sxs-lookup"><span data-stu-id="4df69-215">Here are some examples of how date formulas can be used:</span></span>

-   <span data-ttu-id="4df69-216">Dagsetningarreikniregla í ítrekunartíðnireitnum í ítrekunarbókum ákvarðar hversu oft færsla í færslubókarlínu er bókuð.</span><span class="sxs-lookup"><span data-stu-id="4df69-216">The date formula in the recurring frequency field in recurring journals determines how often the entry on the journal line will be posted.</span></span>

-   <span data-ttu-id="4df69-217">Dagsetningarreikniregla í reitnum **Biðtími** fyrir tiltekið innheimtustig ákvarðar það tímabil sem þarf að líða frá gjalddaga \(eða frá dagsetningu fyrri innheimtubréfs\) áður en innheimtubréf er búið til.</span><span class="sxs-lookup"><span data-stu-id="4df69-217">The date formula in the **Grace Period** field for a specified reminder level determines the period of time that must pass from the due date \(or from the date of the previous reminder\) before a reminder will be created.</span></span>

-   <span data-ttu-id="4df69-218">Dagsetningarreikniregla í reitnum **Gjalddagaútreikningur** ákvarðar hvernig á að reikna gjalddaga í innheimtubréfinu.</span><span class="sxs-lookup"><span data-stu-id="4df69-218">The date formula in the **Due Date Calculation** field determines how to calculate the due date on the reminder.</span></span>

<span data-ttu-id="4df69-219">Dagsetningarformúlan getur innihaldið hámark 20 stafir, bæði tölur og bókstafir.</span><span class="sxs-lookup"><span data-stu-id="4df69-219">The date formula can contain a maximum of 20 characters, both numbers and letters.</span></span> <span data-ttu-id="4df69-220">Þú getur notað eftirfarandi stafi, sem eru skammstafanir fyrir dagbókareiningar.</span><span class="sxs-lookup"><span data-stu-id="4df69-220">You can use the following letters, which are abbreviations for calendar units.</span></span>

|  <span data-ttu-id="4df69-221">Stafur</span><span class="sxs-lookup"><span data-stu-id="4df69-221">Letter</span></span>  |  <span data-ttu-id="4df69-222">Merking</span><span class="sxs-lookup"><span data-stu-id="4df69-222">Meaning</span></span>  |
|----------|----------------------|
|`C`|<span data-ttu-id="4df69-223">Opið</span><span class="sxs-lookup"><span data-stu-id="4df69-223">Current</span></span>|
|`D`|<span data-ttu-id="4df69-224">Dagur\(s\)</span><span class="sxs-lookup"><span data-stu-id="4df69-224">Day\(s\)</span></span>|
|`W`|<span data-ttu-id="4df69-225">Vika\(s\)</span><span class="sxs-lookup"><span data-stu-id="4df69-225">Week\(s\)</span></span>|
|`M`|<span data-ttu-id="4df69-226">Mánuður\(s\)</span><span class="sxs-lookup"><span data-stu-id="4df69-226">Month\(s\)</span></span>|
|`Q`|<span data-ttu-id="4df69-227">Fjórðungur\(s\)</span><span class="sxs-lookup"><span data-stu-id="4df69-227">Quarter\(s\)</span></span>|
|`Y`|<span data-ttu-id="4df69-228">Ár\(s\)</span><span class="sxs-lookup"><span data-stu-id="4df69-228">Year\(s\)</span></span>|

<span data-ttu-id="4df69-229">Hægt er að rita dagsetningarreiknireglu á þrjá vegu.</span><span class="sxs-lookup"><span data-stu-id="4df69-229">You can construct a date formula in three ways.</span></span>

<span data-ttu-id="4df69-230">Eftirfarandi dæmi sýnir hvernig á að nota `C`, fyrir núverandi, og tímaeiningu.</span><span class="sxs-lookup"><span data-stu-id="4df69-230">The following example shows how to use `C`, for current, and a time unit.</span></span>

|  <span data-ttu-id="4df69-231">Segð</span><span class="sxs-lookup"><span data-stu-id="4df69-231">Expression</span></span>  |  <span data-ttu-id="4df69-232">Merking</span><span class="sxs-lookup"><span data-stu-id="4df69-232">Meaning</span></span>  |
|--------------|-----------|
|`CW`|<span data-ttu-id="4df69-233">Líðandi vika</span><span class="sxs-lookup"><span data-stu-id="4df69-233">Current week</span></span>|
|`CM`|<span data-ttu-id="4df69-234">Líðandi mánuður</span><span class="sxs-lookup"><span data-stu-id="4df69-234">Current month</span></span>|

<span data-ttu-id="4df69-235">Eftirfarandi dæmi sýnir hvernig á að nota tölueiningu og tíma.</span><span class="sxs-lookup"><span data-stu-id="4df69-235">The following example shows how to use a number and a time unit.</span></span> <span data-ttu-id="4df69-236">Talan getur ekki verið hærri en 9999.</span><span class="sxs-lookup"><span data-stu-id="4df69-236">A number cannot be larger than 9999.</span></span>

|  <span data-ttu-id="4df69-237">Segð</span><span class="sxs-lookup"><span data-stu-id="4df69-237">Expression</span></span>  |  <span data-ttu-id="4df69-238">Merking</span><span class="sxs-lookup"><span data-stu-id="4df69-238">Meaning</span></span>  |
|--------------|-----------|
|`10D`|<span data-ttu-id="4df69-239">10 dögum eftir daginn í dag</span><span class="sxs-lookup"><span data-stu-id="4df69-239">10 days from today</span></span>|
|`2W`|<span data-ttu-id="4df69-240">2 vikum eftir daginn í dag</span><span class="sxs-lookup"><span data-stu-id="4df69-240">2 weeks from today</span></span>|

<span data-ttu-id="4df69-241">Eftirfarandi dæmi sýnir hvernig á að nota tímaeiningu og tölu.</span><span class="sxs-lookup"><span data-stu-id="4df69-241">The following example shows how to use a time unit and a number.</span></span>

|  <span data-ttu-id="4df69-242">Segð</span><span class="sxs-lookup"><span data-stu-id="4df69-242">Expression</span></span>  |  <span data-ttu-id="4df69-243">Merking</span><span class="sxs-lookup"><span data-stu-id="4df69-243">Meaning</span></span>  |
|--------------|-----------|
|`D10`|<span data-ttu-id="4df69-244">Næsti 10. dagur mánaðar</span><span class="sxs-lookup"><span data-stu-id="4df69-244">The next 10th day of a month</span></span>|
|`WD4`|<span data-ttu-id="4df69-245">Næsti fjórði dagur viku \(fimmtudagur\)</span><span class="sxs-lookup"><span data-stu-id="4df69-245">The next 4th day of a week \(Thursday\)</span></span>|

<span data-ttu-id="4df69-246">Eftirfarandi dæmi sýnir hvernig eigi að samræma þessi þrjú eyðublöð eins og þörf er á.</span><span class="sxs-lookup"><span data-stu-id="4df69-246">The following example shows how you can combine these three forms as needed.</span></span>

|  <span data-ttu-id="4df69-247">Segð</span><span class="sxs-lookup"><span data-stu-id="4df69-247">Expression</span></span>  |  <span data-ttu-id="4df69-248">Merking</span><span class="sxs-lookup"><span data-stu-id="4df69-248">Meaning</span></span>  |
|--------------|-----------|
|`CM+10D`|<span data-ttu-id="4df69-249">Líðandi mánuður \+ 10 dagar</span><span class="sxs-lookup"><span data-stu-id="4df69-249">Current month \+ 10 days</span></span>|

<span data-ttu-id="4df69-250">Eftirfarandi dæmi sýnir hvernig hægt er að nota mínustákn til að sýna gamla dagsetningu.</span><span class="sxs-lookup"><span data-stu-id="4df69-250">The following example shows how you can use a minus sign to indicate a date in the past.</span></span>

|  <span data-ttu-id="4df69-251">Segð</span><span class="sxs-lookup"><span data-stu-id="4df69-251">Expression</span></span>  |  <span data-ttu-id="4df69-252">Merking</span><span class="sxs-lookup"><span data-stu-id="4df69-252">Meaning</span></span>  |
|--------------|-----------|
|`-1Y`|<span data-ttu-id="4df69-253">1 ári fyrir daginn í dag</span><span class="sxs-lookup"><span data-stu-id="4df69-253">1 year ago from today</span></span>|

> [!IMPORTANT]
>  <span data-ttu-id="4df69-254">Ef staðsetningin notar grunndagatal, er dagsetningarreiknireglan sem er til dæmis færð inn í reitinn **Afhendingartími** túlkuð samkvæmt vinnudögum.</span><span class="sxs-lookup"><span data-stu-id="4df69-254">If the location uses a base calendar, then the date formula that you enter in, for example, the **Shipping Time** field is interpreted according to the calendar working days.</span></span> <span data-ttu-id="4df69-255">Til dæmis, `1W` þýðir sjö virkir dagar.</span><span class="sxs-lookup"><span data-stu-id="4df69-255">For example, `1W`  means seven working days.</span></span>
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

## <a name="entering-times"></a><span data-ttu-id="4df69-256">Tími færður inn</span><span class="sxs-lookup"><span data-stu-id="4df69-256">Entering Times</span></span>
<span data-ttu-id="4df69-257">Þegar þú slærð inn tímana getur þú sett inn hvaða skiltákn án bils sem þú vilt milli eininganna, en ef þú notar tvöfalda tölustafi fyrir hverja einingu allt upp að millisekúndum, þá er þess ekki krafist.</span><span class="sxs-lookup"><span data-stu-id="4df69-257">When you enter times, you can insert any non-space separators that you want between the units, but if you use double digits for each unit up to milliseconds, then it is not required.</span></span>

<span data-ttu-id="4df69-258">Þú þarft aðeins að skrifa stærsta einingar sem þú þarfnast; restin verður stillt á núll.</span><span class="sxs-lookup"><span data-stu-id="4df69-258">You only have to write the largest units that you require; the rest will be set to zero.</span></span> <span data-ttu-id="4df69-259">Þú getur einnig sleppt öllum f.h./e.h. vísum.</span><span class="sxs-lookup"><span data-stu-id="4df69-259">You can also leave out any AM/PM indicator.</span></span>

<span data-ttu-id="4df69-260">Í eftirfarandi töflu birtast mismunandi leiðir til að færa inn tímasetningar og hvernig þær eru túlkaðar:</span><span class="sxs-lookup"><span data-stu-id="4df69-260">The following table lists the various ways in which times can be entered and how they are interpreted.</span></span> <span data-ttu-id="4df69-261">Það gerir ráð fyrir svæðisstillingar sem sníða tíma samkvæmt: **Klukkustundir:Mínútur:Sekúndur.Millisekúndur.**</span><span class="sxs-lookup"><span data-stu-id="4df69-261">It assumes region settings that format times according to: **Hours:Minutes:Seconds.Milliseconds.**</span></span> <span data-ttu-id="4df69-262">og nota f.h. og e.h. vísa um „f.h.“ og „e.h.“, eftir því sem við á.</span><span class="sxs-lookup"><span data-stu-id="4df69-262">and use the AM and PM indicators of 'AM' and 'PM', respectively.</span></span>

|<span data-ttu-id="4df69-263">**Færsla**</span><span class="sxs-lookup"><span data-stu-id="4df69-263">**Entry**</span></span>      |<span data-ttu-id="4df69-264">**Túlkun**</span><span class="sxs-lookup"><span data-stu-id="4df69-264">**Interpretation**</span></span>      |
|---------------|------------------------|
|`05:23:17`|<span data-ttu-id="4df69-265">05:23:17</span><span class="sxs-lookup"><span data-stu-id="4df69-265">05:23:17</span></span>|
|`5`|<span data-ttu-id="4df69-266">05:00:00</span><span class="sxs-lookup"><span data-stu-id="4df69-266">05:00:00</span></span>|
|`5AM`|<span data-ttu-id="4df69-267">05:00:00</span><span class="sxs-lookup"><span data-stu-id="4df69-267">05:00:00</span></span>|
|`5P`|<span data-ttu-id="4df69-268">17:00:00</span><span class="sxs-lookup"><span data-stu-id="4df69-268">17:00:00</span></span>|
|`12`|<span data-ttu-id="4df69-269">12:00:00</span><span class="sxs-lookup"><span data-stu-id="4df69-269">12:00:00</span></span>|
|`12A`|<span data-ttu-id="4df69-270">00:00:00</span><span class="sxs-lookup"><span data-stu-id="4df69-270">00:00:00</span></span>|
|`12P`|<span data-ttu-id="4df69-271">12:00:00</span><span class="sxs-lookup"><span data-stu-id="4df69-271">12:00:00</span></span>|
|`17`|<span data-ttu-id="4df69-272">17:00:00</span><span class="sxs-lookup"><span data-stu-id="4df69-272">17:00:00</span></span>|
|`5:30`|<span data-ttu-id="4df69-273">05:30:00</span><span class="sxs-lookup"><span data-stu-id="4df69-273">05:30:00</span></span>|
|`0530`|<span data-ttu-id="4df69-274">05:30:00</span><span class="sxs-lookup"><span data-stu-id="4df69-274">05:30:00</span></span>|
|`5:30:5`|<span data-ttu-id="4df69-275">05:30:05</span><span class="sxs-lookup"><span data-stu-id="4df69-275">05:30:05</span></span>|
|`053005`|<span data-ttu-id="4df69-276">05:30:05</span><span class="sxs-lookup"><span data-stu-id="4df69-276">05:30:05</span></span>|
|`5:30:5,50`|<span data-ttu-id="4df69-277">05:30:050,5</span><span class="sxs-lookup"><span data-stu-id="4df69-277">05:30:05.5</span></span>|
|`053005050`|<span data-ttu-id="4df69-278">05:30:05.05</span><span class="sxs-lookup"><span data-stu-id="4df69-278">05:30:05.05</span></span>|

<span data-ttu-id="4df69-279">Þú ættir að vera meðvitaðir um að millisekúndur séu túlkuð sem tugabrot.</span><span class="sxs-lookup"><span data-stu-id="4df69-279">You should be aware that milliseconds are interpreted as decimal notation.</span></span> <span data-ttu-id="4df69-280">Þannig að, til dæmis, `3`, `30`, og `300` þýðir allt 300 millisekúndur, á meðan `03` þýðir `30` og `003` þýðir 3 millisekúndur.</span><span class="sxs-lookup"><span data-stu-id="4df69-280">So, for example, `3`, `30`, and `300` all mean 300 milliseconds, while `03` means `30` and `003` means 3 milliseconds.</span></span>

<span data-ttu-id="4df69-281">Þú getur ekki látið `24:00` tákna miðnætti eða notað gildi sem er hærra en 24:00.</span><span class="sxs-lookup"><span data-stu-id="4df69-281">You cannot use `24:00` to mean midnight, or use any value greater than 24:00.</span></span>

<span data-ttu-id="4df69-282">Orðið fyrir „tími“ á tungumálinu sem notað er af [!INCLUDE[d365fin](includes/d365fin_long_md.md)] verður metið við núverandi tíma á tölvunni þinni eða fartækinu.</span><span class="sxs-lookup"><span data-stu-id="4df69-282">The word for 'time' in the language used by [!INCLUDE[d365fin](includes/d365fin_long_md.md)] will be evaluated to the current time on your computer or mobile device.</span></span> <span data-ttu-id="4df69-283">Þú getur slegið inn hvaða hluta orðsins sem er, með því að byrja á byrjuninni, eins og til dæmis `t` eða `TIM`.</span><span class="sxs-lookup"><span data-stu-id="4df69-283">You can enter any part of the word, starting from the beginning, such as `t` or `TIM`.</span></span>

## <a name="entering-combined-dates-and-times"></a><span data-ttu-id="4df69-284">Sláðu inn sameinaða dagsetningar og tíma</span><span class="sxs-lookup"><span data-stu-id="4df69-284">Entering combined Dates and Times</span></span>
<span data-ttu-id="4df69-285">Þegar þú slærð inn dagsetningartíma, sem er dagsetning og tími sameinuð í eitt reit, verður þú að slá inn bil milli dagsetningar og tíma.</span><span class="sxs-lookup"><span data-stu-id="4df69-285">When you enter datetimes, which are a date and time combined into one field, you must enter a space between the date and the time.</span></span> <span data-ttu-id="4df69-286">Dagsetningarhlutinn getur aðeins innihaldið bil í formi opinbers dagsetningarskiltákns þinna svæðisstillinga.</span><span class="sxs-lookup"><span data-stu-id="4df69-286">The date part can only contain spaces in the form of the official date separator of your region settings.</span></span> <span data-ttu-id="4df69-287">Tíminn getur innihaldið bil í kringum f.h./e.h. vísirinn.</span><span class="sxs-lookup"><span data-stu-id="4df69-287">The time can contain spaces around the AM/PM indicator.</span></span>

<span data-ttu-id="4df69-288">Einnig er hægt að slá inn aðeins dagsetningu í reit fyrir dagsetningartíma, en ekki er hægt að slá inn aðeins tíma.</span><span class="sxs-lookup"><span data-stu-id="4df69-288">It is also possible to enter only a date in a datetime field, but it is not possible to enter only a time.</span></span>

<span data-ttu-id="4df69-289">Eftirfarandi tafla sýnir nokkur dæmi um samsetningar dagsetninga og tíma.</span><span class="sxs-lookup"><span data-stu-id="4df69-289">The following table lists some examples of date/time combinations.</span></span> <span data-ttu-id="4df69-290">Svæðisstillingarnar í dæmunum birta dagsetningar í sniðinu dagur\-mánuður\-ár, með f.h./e.h. kennimerkjum, ensku og sunnudegi sem byrjun vikunnar.</span><span class="sxs-lookup"><span data-stu-id="4df69-290">The region settings in the examples displays dates in the day\-month\-year format, using AM/PM designators, English language, and Sunday as the start of the week.</span></span>

|<span data-ttu-id="4df69-291">**Færsla**</span><span class="sxs-lookup"><span data-stu-id="4df69-291">**Entry**</span></span>      |<span data-ttu-id="4df69-292">**Túlkun**</span><span class="sxs-lookup"><span data-stu-id="4df69-292">**Interpretation**</span></span>      |
|---------------|------------------------|
|`08-01-2016 05:48:12 PM`|<span data-ttu-id="4df69-293">08\-01\-2016 05:48:12 e.h.</span><span class="sxs-lookup"><span data-stu-id="4df69-293">08\-01\-2016 05:48:12 PM</span></span>|
|`131202 132455`|<span data-ttu-id="4df69-294">13\-12\-2002 13:24:55</span><span class="sxs-lookup"><span data-stu-id="4df69-294">13\-12\-2002 13:24:55</span></span>|
|`1-12-02 10`|<span data-ttu-id="4df69-295">01\-12\-2002 10:00:00</span><span class="sxs-lookup"><span data-stu-id="4df69-295">01\-12\-2002 10:00:00</span></span>|
|`1.12.02 5`|<span data-ttu-id="4df69-296">01\-12\-2002 05:00:00</span><span class="sxs-lookup"><span data-stu-id="4df69-296">01\-12\-2002 05:00:00</span></span>|
|`1.12.02`|<span data-ttu-id="4df69-297">01\-12\-2002 00:00:00</span><span class="sxs-lookup"><span data-stu-id="4df69-297">01\-12\-2002 00:00:00</span></span>|
|`11 12`|<span data-ttu-id="4df69-298">11\-vinnudagsetningarmánuður\-vinnudagsetningarár 12:00:00</span><span class="sxs-lookup"><span data-stu-id="4df69-298">11\-work date month\-work date year 12:00:00</span></span>|
|`1112 12`|<span data-ttu-id="4df69-299">11\-12\-vinnudagsetningarárið 12:00:00</span><span class="sxs-lookup"><span data-stu-id="4df69-299">11\-12\-work date year 12:00:00</span></span>|
|<span data-ttu-id="4df69-300">`t` eða `today`</span><span class="sxs-lookup"><span data-stu-id="4df69-300">`t` or `today`</span></span>|<span data-ttu-id="4df69-301">dagurinn í dag 00:00:00</span><span class="sxs-lookup"><span data-stu-id="4df69-301">today's date 00:00:00</span></span>|
|`t 10:30`|<span data-ttu-id="4df69-302">dagurinn í dag 10:30:00</span><span class="sxs-lookup"><span data-stu-id="4df69-302">today's date 10:30:00</span></span>|
|`t 3:3:3`|<span data-ttu-id="4df69-303">dagurinn í dag 03:03:03</span><span class="sxs-lookup"><span data-stu-id="4df69-303">today's date 03:03:03</span></span>|
|<span data-ttu-id="4df69-304">`w` eða `workdate`</span><span class="sxs-lookup"><span data-stu-id="4df69-304">`w` or `workdate`</span></span>|<span data-ttu-id="4df69-305">vinnudagsetningin 00:00:00</span><span class="sxs-lookup"><span data-stu-id="4df69-305">the working date 00:00:00</span></span>|
|<span data-ttu-id="4df69-306">`m` eða `Monday`</span><span class="sxs-lookup"><span data-stu-id="4df69-306">`m` or `Monday`</span></span>|<span data-ttu-id="4df69-307">Mánudagur vinnudagsetningarvikunnar 00:00:00</span><span class="sxs-lookup"><span data-stu-id="4df69-307">Monday of the work date week 00:00:00</span></span>|
|<span data-ttu-id="4df69-308">`tu` eða `Tuesday`</span><span class="sxs-lookup"><span data-stu-id="4df69-308">`tu` or `Tuesday`</span></span>|<span data-ttu-id="4df69-309">Þriðjudagur vinnudagsetningarvikunnar 00:00:00</span><span class="sxs-lookup"><span data-stu-id="4df69-309">Tuesday of the work date week 00:00:00</span></span>|
|<span data-ttu-id="4df69-310">`sa` eða `Saturday`</span><span class="sxs-lookup"><span data-stu-id="4df69-310">`sa` or `Saturday`</span></span>|<span data-ttu-id="4df69-311">Laugardagur vinnudagsetningarvikunnar 00:00:00</span><span class="sxs-lookup"><span data-stu-id="4df69-311">Saturday of the work date week 00:00:00</span></span>|
|<span data-ttu-id="4df69-312">`s` eða `Sunday`</span><span class="sxs-lookup"><span data-stu-id="4df69-312">`s` or `Sunday`</span></span>|<span data-ttu-id="4df69-313">Sunnudagur vinnudagsetningarvikunnar 00:00:00</span><span class="sxs-lookup"><span data-stu-id="4df69-313">Sunday of the work date week 00:00:00</span></span>|
|`tu 10:30`|<span data-ttu-id="4df69-314">Þriðjudagur vinnudagsetningarvikunnar 10:30:00</span><span class="sxs-lookup"><span data-stu-id="4df69-314">Tuesday of the work date week 10:30:00</span></span>|
|`tu 3:3:3`|<span data-ttu-id="4df69-315">Þriðjudagur vinnudagsetningarvikunnar 03:03:03</span><span class="sxs-lookup"><span data-stu-id="4df69-315">Tuesday of the work date week 03:03:03</span></span>|
|`t23 t`|<span data-ttu-id="4df69-316">Þriðjudagur 23. viku vinnudagsetningarársins, núgildandi tími dagsins</span><span class="sxs-lookup"><span data-stu-id="4df69-316">Tuesday of week 23 of the work date year, current time of day</span></span>|
|`t23`|<span data-ttu-id="4df69-317">Þriðjudagur 23. viku vinnudagsetningarársins</span><span class="sxs-lookup"><span data-stu-id="4df69-317">Tuesday of week 23 of the work date year</span></span>|
|`t 23`|<span data-ttu-id="4df69-318">Í dag 23:00:00</span><span class="sxs-lookup"><span data-stu-id="4df69-318">Today 23:00:00</span></span>|
|`t-1`|<span data-ttu-id="4df69-319">Þriðjudagur 1. viku vinnudagsetningarársins</span><span class="sxs-lookup"><span data-stu-id="4df69-319">Tuesday of week 1 of the work date year</span></span>|

## <a name="entering-duration"></a><span data-ttu-id="4df69-320">Færið inn tímalengd</span><span class="sxs-lookup"><span data-stu-id="4df69-320">Entering Duration</span></span>
<span data-ttu-id="4df69-321">Sumir reitir í forritinu tákna tímalengd eða magn liðins tíma, í stað tiltekins dagsetningar eða tíma.</span><span class="sxs-lookup"><span data-stu-id="4df69-321">Some fields in the application represent a duration, or amount of elapsed time, instead of a specific date or time.</span></span> <span data-ttu-id="4df69-322">Hægt er að færa inn tímalengd sem tölu og mælieiningu.</span><span class="sxs-lookup"><span data-stu-id="4df69-322">You enter a duration as a number followed by its unit of measure.</span></span>

<span data-ttu-id="4df69-323">Hér eru nokkur dæmi.</span><span class="sxs-lookup"><span data-stu-id="4df69-323">Here are some examples.</span></span>

|<span data-ttu-id="4df69-324">**Lengd**</span><span class="sxs-lookup"><span data-stu-id="4df69-324">**Duration**</span></span>|<span data-ttu-id="4df69-325">**Mælieining**</span><span class="sxs-lookup"><span data-stu-id="4df69-325">**Unit of measure**</span></span>|
|------------|-------------------|
|`2h`|<span data-ttu-id="4df69-326">2 klst</span><span class="sxs-lookup"><span data-stu-id="4df69-326">2 hrs</span></span>|
|`6h 30 m`|<span data-ttu-id="4df69-327">6 klst 30 mín</span><span class="sxs-lookup"><span data-stu-id="4df69-327">6 hrs 30 mins</span></span>|
|`6.5h`|<span data-ttu-id="4df69-328">6 klst 30 mín</span><span class="sxs-lookup"><span data-stu-id="4df69-328">6 hrs 30 mins</span></span>|
|`90m`|<span data-ttu-id="4df69-329">1 klst 30 mín</span><span class="sxs-lookup"><span data-stu-id="4df69-329">1 hr 30 mins</span></span>|
|`2d 6h 30m`|<span data-ttu-id="4df69-330">2 dagar 6 klst 30 mín</span><span class="sxs-lookup"><span data-stu-id="4df69-330">2 days 6 hrs 30 mins</span></span>|
|`2d 6h 30m 56s 600ms`|<span data-ttu-id="4df69-331">2 dagar 6 klst 30 mín 56 sek 600 millis</span><span class="sxs-lookup"><span data-stu-id="4df69-331">2 days 6 hrs 30 mins 56 secs 600 msecs</span></span>|

<span data-ttu-id="4df69-332">Einnig er hægt að færa inn tölu og þá er henni sjálfkrafa breytt í tímalengd.</span><span class="sxs-lookup"><span data-stu-id="4df69-332">You can also enter a number, which will be automatically converted to a duration.</span></span> <span data-ttu-id="4df69-333">Tölunni sem færð er inn er breytt samkvæmt sjálfgefnu mælieiningunni sem hefur verið tilgreind fyrir reitinn tímalengd.</span><span class="sxs-lookup"><span data-stu-id="4df69-333">The number you enter is converted according to the default unit of measure that has been specified for the duration field.</span></span>

<span data-ttu-id="4df69-334">Hægt er að sjá hvaða mælieining er notuð í reitnum tímalengd með því að færa inn tölu og sjá í hvaða mælieiningu kerfið færir hana í.</span><span class="sxs-lookup"><span data-stu-id="4df69-334">To see what unit of measure is being used in a duration field, enter a number and see which unit of measure it is converted to.</span></span>

<span data-ttu-id="4df69-335">Til dæmis, ef mælieiningin er klukkustund, er númerinu `5` breytt í 5 klukkustundir.</span><span class="sxs-lookup"><span data-stu-id="4df69-335">For example, if the unit of measure is hours, the number `5` is converted to 5 hrs.</span></span>


## <a name="see-also"></a><span data-ttu-id="4df69-336">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="4df69-336">See Also</span></span>
<span data-ttu-id="4df69-337">[Unnið með [!INCLUDE[d365fin](includes/d365fin_long_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="4df69-337">[Working with [!INCLUDE[d365fin](includes/d365fin_long_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="4df69-338">Dagsetning útreiknings fyrir kaup.</span><span class="sxs-lookup"><span data-stu-id="4df69-338">Date Calculation for Purchases</span></span>](purchasing-date-calculation-for-purchases.md)  
[<span data-ttu-id="4df69-339">Skilgreining skilyrða í síum</span><span class="sxs-lookup"><span data-stu-id="4df69-339">Entering Criteria in Filters </span></span>](ui-enter-criteria-filters.md)  

