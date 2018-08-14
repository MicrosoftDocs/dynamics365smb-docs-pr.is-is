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
# <a name="entering-date-ranges"></a><span data-ttu-id="fbaa3-103">Færa inn dagsetningartímabil</span><span class="sxs-lookup"><span data-stu-id="fbaa3-103">Entering Date Ranges</span></span>
<span data-ttu-id="fbaa3-104">Hægt er að stilla afmarkanir með upphafs- og lokadegi til að birta aðeins gögn á tilteknu tímabili.</span><span class="sxs-lookup"><span data-stu-id="fbaa3-104">You can set filters containing a start date and an end date to display only the data contained in that date range or time interval.</span></span> <span data-ttu-id="fbaa3-105">Ákveðnar reglur gilda um hvernig tímabil eru stillt.</span><span class="sxs-lookup"><span data-stu-id="fbaa3-105">Special rules apply to the way you set date ranges.</span></span> <span data-ttu-id="fbaa3-106">Tökum sem dæmi **Topp 10 viðskiptavinir**:</span><span class="sxs-lookup"><span data-stu-id="fbaa3-106">Let's take the **Customer Top 10** as an example:</span></span>

![Stilla dagsetningartímabil á beiðnisíðunni fyrir topp 10 viðskiptavinir](./media/ui-enter-date-ranges/customer-top10-list.png)

<span data-ttu-id="fbaa3-108">Hér geturðu afmarkað skýrsluna við dagsetningartímabil eins og síðustu 2 vikur eða alls 6 vikur, eða hvaða tímabil sem þú vilt.</span><span class="sxs-lookup"><span data-stu-id="fbaa3-108">Here you can limit the report to a date range such as the past 2 weeks, or a total of 6 weeks, or whatever range you want.</span></span> <span data-ttu-id="fbaa3-109">Til að stilla dagsetningartímabil slærðu inn dagsetningar og notar svo annað hvort **..**</span><span class="sxs-lookup"><span data-stu-id="fbaa3-109">To set date ranges, you enter dates and then use either **..**</span></span> <span data-ttu-id="fbaa3-110">eða **|** til að stilla tímabilið.</span><span class="sxs-lookup"><span data-stu-id="fbaa3-110">or **|** to set the range.</span></span> <span data-ttu-id="fbaa3-111">Til að skoða topp 10 viðskiptavinina fyrstu 2 vikurnar í maí, til dæmis, myndirðu setja dagsetingarafmörkunina á *05 01 17..05 14 17*.</span><span class="sxs-lookup"><span data-stu-id="fbaa3-111">In our example, to show the top 10 customers for the first two weeks of May, you would set the date filter to *05 01 17..05 14 17*.</span></span>
<span data-ttu-id="fbaa3-112">Hér eru nokkur fleiri dæmi:</span><span class="sxs-lookup"><span data-stu-id="fbaa3-112">Here are a couple of other examples:</span></span>

| <span data-ttu-id="fbaa3-113">Merking</span><span class="sxs-lookup"><span data-stu-id="fbaa3-113">Meaning</span></span> | <span data-ttu-id="fbaa3-114">Dæmi</span><span class="sxs-lookup"><span data-stu-id="fbaa3-114">Example</span></span> | <span data-ttu-id="fbaa3-115">Ásamt færslum</span><span class="sxs-lookup"><span data-stu-id="fbaa3-115">Entries included</span></span> |
|---|---|---|
|<span data-ttu-id="fbaa3-116">Jafnt og</span><span class="sxs-lookup"><span data-stu-id="fbaa3-116">Equal to</span></span>| <span data-ttu-id="fbaa3-117">12, 15, 16</span><span class="sxs-lookup"><span data-stu-id="fbaa3-117">12 15 16</span></span> |<span data-ttu-id="fbaa3-118">Einungis þær sem bókaðar eru 15. desember 2016.</span><span class="sxs-lookup"><span data-stu-id="fbaa3-118">Only those posted on December 15 2016.</span></span>|
|<span data-ttu-id="fbaa3-119">Millibil</span><span class="sxs-lookup"><span data-stu-id="fbaa3-119">Interval</span></span>| <span data-ttu-id="fbaa3-120">12 15 16..01 15 17</span><span class="sxs-lookup"><span data-stu-id="fbaa3-120">12 15 16..01 15 17</span></span><br /><br /><span data-ttu-id="fbaa3-121">..12 15 16</span><span class="sxs-lookup"><span data-stu-id="fbaa3-121">..12 15 16</span></span>|<span data-ttu-id="fbaa3-122">Færslur sem eru bókaðar á dagsetningum á milli og með 15. desember 2016 og 15. janúar 2017.</span><span class="sxs-lookup"><span data-stu-id="fbaa3-122">Those posted on dates between and including December 15 2016 and January 15 2017.</span></span><br /><br /><span data-ttu-id="fbaa3-123">Þær sem eru bókaðar eru 15. desember 2016 og fyrr.</span><span class="sxs-lookup"><span data-stu-id="fbaa3-123">Those posted on December 15 2016 or earlier.</span></span>|
|<span data-ttu-id="fbaa3-124">Annaðhvort eða</span><span class="sxs-lookup"><span data-stu-id="fbaa3-124">Either/or</span></span>|<span data-ttu-id="fbaa3-125">12 15 16&#124;12 16 16</span><span class="sxs-lookup"><span data-stu-id="fbaa3-125">12 15 16&#124;12 16 16</span></span>|<span data-ttu-id="fbaa3-126">Þær sem eru bókaðar annað hvort 15. eða 16. desember 2016.</span><span class="sxs-lookup"><span data-stu-id="fbaa3-126">Those posted on either December 15 or December 16 2016.</span></span> <span data-ttu-id="fbaa3-127">Ef færslur eru bókaðar báða dagana verða þær allar sýndar.</span><span class="sxs-lookup"><span data-stu-id="fbaa3-127">If there are entries posted on both days, they will all be displayed.</span></span>|

<span data-ttu-id="fbaa3-128">Einnig má tengja grunnformin saman.</span><span class="sxs-lookup"><span data-stu-id="fbaa3-128">You can also combine the various format types.</span></span>

| <span data-ttu-id="fbaa3-129">Dæmi</span><span class="sxs-lookup"><span data-stu-id="fbaa3-129">Example</span></span> | <span data-ttu-id="fbaa3-130">Ásamt færslum</span><span class="sxs-lookup"><span data-stu-id="fbaa3-130">Entries included</span></span> |
|---|---|
|<span data-ttu-id="fbaa3-131">12 15 16&#124;12 01 16..05 31 17</span><span class="sxs-lookup"><span data-stu-id="fbaa3-131">12 15 16&#124;12 01 16..05 31 17</span></span> | <span data-ttu-id="fbaa3-132">Færslur sem eru bókaðar annað hvort 15. desember 2016 eða á dagsetningum á milli og með 01. desember 2016 og 31. maí 2017.</span><span class="sxs-lookup"><span data-stu-id="fbaa3-132">Entries posted either on December 15 2016 or on dates between and including December 01 2016 and May 31 2017.</span></span> |
|<span data-ttu-id="fbaa3-133">12 14 16&#124;12 30 16</span><span class="sxs-lookup"><span data-stu-id="fbaa3-133">..12 14 16&#124;12 30 16..</span></span> | <span data-ttu-id="fbaa3-134">Færslur bókaðar til og með 14. desember og færslur bókaðar frá og með 30. desember - það er, allar færslur nema þær sem voru bókaðar á dagsetningum á milli og með 15. og 29. desember.</span><span class="sxs-lookup"><span data-stu-id="fbaa3-134">Entries posted on December 14 or earlier, or entries posted on December 30 or later - that is, all entries except those posted on dates between and including December 15 and 29.</span></span> |

<span data-ttu-id="fbaa3-135">Athugið að við notuðum bandarískt dagsetningarsnið hér.</span><span class="sxs-lookup"><span data-stu-id="fbaa3-135">Note that we have used the US date format MMDDYY here.</span></span> <span data-ttu-id="fbaa3-136">Þegar [!INCLUDE[d365fin](includes/d365fin_md.md)] verður tiltækt á öðrum mörkuðum, muntu geta notað þau snið sem þú ert vanur.</span><span class="sxs-lookup"><span data-stu-id="fbaa3-136">As [!INCLUDE[d365fin](includes/d365fin_md.md)] becomes available in other markets, you'll be able to use the formats that you are used to.</span></span>

## <a name="using-date-formulas"></a><span data-ttu-id="fbaa3-137">Notkun dagsetningarreiknireglna</span><span class="sxs-lookup"><span data-stu-id="fbaa3-137">Using Date Formulas</span></span>
<span data-ttu-id="fbaa3-138">Dagsetningarregla er stutt, skammstöfuð samsetning stafa og tölustafa sem tilgreinir hvernig skal reikna út dagsetningar.</span><span class="sxs-lookup"><span data-stu-id="fbaa3-138">A date formula is a short, abbreviated combination of letters and numbers that specifies how to calculate dates.</span></span> <span data-ttu-id="fbaa3-139">Hægt er að færa dagsetningarreiknireglur í ólíka dagsetningarreiknireiti og í ítrekunartíðnireiti í ítrekunarbókum.</span><span class="sxs-lookup"><span data-stu-id="fbaa3-139">You can enter date formulas in various date calculation fields and in recurring frequency fields in recurring journals.</span></span>

> [!NOTE]
>  <span data-ttu-id="fbaa3-140">Dagurinn í dag, fyrir upphaf tímabilsins, er með í öllum reitum fyrir reiknireglur dagsetninga.</span><span class="sxs-lookup"><span data-stu-id="fbaa3-140">In all data formula fields, one day is automatically included to cover today as the day when the period starts.</span></span> <span data-ttu-id="fbaa3-141">Samkvæmt því, ef til dæmis fært er inn **1W** er tímabilið í raun átta dagar þar sem dagurinn í dag er tekinn með.</span><span class="sxs-lookup"><span data-stu-id="fbaa3-141">Accordingly, for example, if you enter **1W**, then the period is actually eight days because today is included.</span></span> <span data-ttu-id="fbaa3-142">Til að tilgreina sjö daga tímabil (eina raunviku) að meðtalinni upphafsdagsetningu tímabilsins þarf að færa inn **6D** eða **1W\-1D**.</span><span class="sxs-lookup"><span data-stu-id="fbaa3-142">To specify a period of seven days (one true week) including the period starting date, then you must enter **6D** or **1W\-1D**.</span></span>

<span data-ttu-id="fbaa3-143">Hér eru nokkur dæmi um hvernig nota má dagsetningarreiknireglur:</span><span class="sxs-lookup"><span data-stu-id="fbaa3-143">Here are some examples of how date formulas can be used:</span></span>

-   <span data-ttu-id="fbaa3-144">Dagsetningarreikniregla í ítrekunartíðnireitnum í ítrekunarbókum ákvarðar hversu oft færsla í færslubókarlínu er bókuð.</span><span class="sxs-lookup"><span data-stu-id="fbaa3-144">The date formula in the recurring frequency field in recurring journals determines how often the entry on the journal line will be posted.</span></span>

-   <span data-ttu-id="fbaa3-145">Dagsetningarreikniregla í reitnum **Biðtími** fyrir tiltekið innheimtustig ákvarðar það tímabil sem þarf að líða frá gjalddaga (eða frá gjalddaga fyrra innheimtubréfs) áður en innheimtubréf er búið til.</span><span class="sxs-lookup"><span data-stu-id="fbaa3-145">The date formula in the **Grace Period** field for a specified reminder level determines the period of time that must pass from the due date (or from the due date of the previous reminder) before a reminder will be created.</span></span>

-   <span data-ttu-id="fbaa3-146">Dagsetningarreikniregla í reitnum **Gjalddagaútreikningur** ákvarðar hvernig á að reikna gjalddaga í innheimtubréfinu.</span><span class="sxs-lookup"><span data-stu-id="fbaa3-146">The date formula in the **Due Date Calculation** field determines how to calculate the due date on the reminder.</span></span>

<span data-ttu-id="fbaa3-147">Dagsetningarreikniregla getur mest haft 20 stafi, bæði tölu- og bókstafi.</span><span class="sxs-lookup"><span data-stu-id="fbaa3-147">The date calculation formula can contain a maximum of 20 characters, both numbers and letters.</span></span> <span data-ttu-id="fbaa3-148">Hægt er að nota eftirfarandi stafi sem skammstafanir fyrir tiltekinn tíma.</span><span class="sxs-lookup"><span data-stu-id="fbaa3-148">You can use the following letters, which are abbreviations for time specifications.</span></span>

|  <span data-ttu-id="fbaa3-149">Stafur</span><span class="sxs-lookup"><span data-stu-id="fbaa3-149">Letter</span></span>  |  <span data-ttu-id="fbaa3-150">Upplýsingar um tíma</span><span class="sxs-lookup"><span data-stu-id="fbaa3-150">Time specification</span></span>  |
|----------|----------------------|
|<span data-ttu-id="fbaa3-151">U</span><span class="sxs-lookup"><span data-stu-id="fbaa3-151">C</span></span>|<span data-ttu-id="fbaa3-152">Opið</span><span class="sxs-lookup"><span data-stu-id="fbaa3-152">Current</span></span>|
|<span data-ttu-id="fbaa3-153">D</span><span class="sxs-lookup"><span data-stu-id="fbaa3-153">D</span></span>|<span data-ttu-id="fbaa3-154">Dagur\(s\)</span><span class="sxs-lookup"><span data-stu-id="fbaa3-154">Day\(s\)</span></span>|
|<span data-ttu-id="fbaa3-155">V</span><span class="sxs-lookup"><span data-stu-id="fbaa3-155">W</span></span>|<span data-ttu-id="fbaa3-156">Vika\(s\)</span><span class="sxs-lookup"><span data-stu-id="fbaa3-156">Week\(s\)</span></span>|
|<span data-ttu-id="fbaa3-157">M</span><span class="sxs-lookup"><span data-stu-id="fbaa3-157">M</span></span>|<span data-ttu-id="fbaa3-158">Mánuður\(s\)</span><span class="sxs-lookup"><span data-stu-id="fbaa3-158">Month\(s\)</span></span>|
|<span data-ttu-id="fbaa3-159">F</span><span class="sxs-lookup"><span data-stu-id="fbaa3-159">Q</span></span>|<span data-ttu-id="fbaa3-160">Fjórðungur\(s\)</span><span class="sxs-lookup"><span data-stu-id="fbaa3-160">Quarter\(s\)</span></span>|
|<span data-ttu-id="fbaa3-161">Á</span><span class="sxs-lookup"><span data-stu-id="fbaa3-161">Y</span></span>|<span data-ttu-id="fbaa3-162">Ár\(s\)</span><span class="sxs-lookup"><span data-stu-id="fbaa3-162">Year\(s\)</span></span>|

<span data-ttu-id="fbaa3-163">Hægt er að rita dagsetningarreiknireglu á þrjá vegu.</span><span class="sxs-lookup"><span data-stu-id="fbaa3-163">You can construct a date formula in three ways.</span></span>

<span data-ttu-id="fbaa3-164">Eftirfarandi dæmi sýnir hvernig á að nota **U**, fyrir líðandi, og tímaeiningu.</span><span class="sxs-lookup"><span data-stu-id="fbaa3-164">The following example shows how to use **C**, for current, and a time unit.</span></span>

|  <span data-ttu-id="fbaa3-165">Segð</span><span class="sxs-lookup"><span data-stu-id="fbaa3-165">Expression</span></span>  |  <span data-ttu-id="fbaa3-166">Merking</span><span class="sxs-lookup"><span data-stu-id="fbaa3-166">Meaning</span></span>  |
|--------------|-----------|
|<span data-ttu-id="fbaa3-167">LV</span><span class="sxs-lookup"><span data-stu-id="fbaa3-167">CW</span></span>|<span data-ttu-id="fbaa3-168">Líðandi vika</span><span class="sxs-lookup"><span data-stu-id="fbaa3-168">Current week</span></span>|
|<span data-ttu-id="fbaa3-169">LM</span><span class="sxs-lookup"><span data-stu-id="fbaa3-169">CM</span></span>|<span data-ttu-id="fbaa3-170">Líðandi mánuður</span><span class="sxs-lookup"><span data-stu-id="fbaa3-170">Current month</span></span>|

<span data-ttu-id="fbaa3-171">Eftirfarandi dæmi sýnir hvernig á að nota tölueiningu og tíma.</span><span class="sxs-lookup"><span data-stu-id="fbaa3-171">The following example shows how to use a number and a time unit.</span></span> <span data-ttu-id="fbaa3-172">Talan getur ekki verið hærri en 9999.</span><span class="sxs-lookup"><span data-stu-id="fbaa3-172">A number cannot be larger than 9999.</span></span>

|  <span data-ttu-id="fbaa3-173">Segð</span><span class="sxs-lookup"><span data-stu-id="fbaa3-173">Expression</span></span>  |  <span data-ttu-id="fbaa3-174">Merking</span><span class="sxs-lookup"><span data-stu-id="fbaa3-174">Meaning</span></span>  |
|--------------|-----------|
|<span data-ttu-id="fbaa3-175">10D</span><span class="sxs-lookup"><span data-stu-id="fbaa3-175">10D</span></span>|<span data-ttu-id="fbaa3-176">10 dögum eftir daginn í dag</span><span class="sxs-lookup"><span data-stu-id="fbaa3-176">10 days from today</span></span>|
|<span data-ttu-id="fbaa3-177">2V</span><span class="sxs-lookup"><span data-stu-id="fbaa3-177">2W</span></span>|<span data-ttu-id="fbaa3-178">2 vikum eftir daginn í dag</span><span class="sxs-lookup"><span data-stu-id="fbaa3-178">2 weeks from today</span></span>|

<span data-ttu-id="fbaa3-179">Eftirfarandi dæmi sýnir hvernig á að nota tímaeiningu og tölu.</span><span class="sxs-lookup"><span data-stu-id="fbaa3-179">The following example shows how to use a time unit and a number.</span></span>

|  <span data-ttu-id="fbaa3-180">Segð</span><span class="sxs-lookup"><span data-stu-id="fbaa3-180">Expression</span></span>  |  <span data-ttu-id="fbaa3-181">Merking</span><span class="sxs-lookup"><span data-stu-id="fbaa3-181">Meaning</span></span>  |
|--------------|-----------|
|<span data-ttu-id="fbaa3-182">D10</span><span class="sxs-lookup"><span data-stu-id="fbaa3-182">D10</span></span>|<span data-ttu-id="fbaa3-183">Næsti 10. dagur mánaðar</span><span class="sxs-lookup"><span data-stu-id="fbaa3-183">The next 10th day of a month</span></span>|
|<span data-ttu-id="fbaa3-184">VD4</span><span class="sxs-lookup"><span data-stu-id="fbaa3-184">WD4</span></span>|<span data-ttu-id="fbaa3-185">Næsti fjórði dagur viku \(fimmtudagur\)</span><span class="sxs-lookup"><span data-stu-id="fbaa3-185">The next 4th day of a week \(Thursday\)</span></span>|

<span data-ttu-id="fbaa3-186">Eftirfarandi dæmi sýnir hvernig eigi að samræma þessi þrjú eyðublöð eins og þörf er á.</span><span class="sxs-lookup"><span data-stu-id="fbaa3-186">The following example shows how you can combine these three forms as needed.</span></span>

|  <span data-ttu-id="fbaa3-187">Segð</span><span class="sxs-lookup"><span data-stu-id="fbaa3-187">Expression</span></span>  |  <span data-ttu-id="fbaa3-188">Merking</span><span class="sxs-lookup"><span data-stu-id="fbaa3-188">Meaning</span></span>  |
|--------------|-----------|
|<span data-ttu-id="fbaa3-189">LM\+10D</span><span class="sxs-lookup"><span data-stu-id="fbaa3-189">CM\+10D</span></span>|<span data-ttu-id="fbaa3-190">Líðandi mánuður \+ 10 dagar</span><span class="sxs-lookup"><span data-stu-id="fbaa3-190">Current month \+ 10 days</span></span>|

<span data-ttu-id="fbaa3-191">Eftirfarandi dæmi sýnir hvernig hægt er að nota mínustákn til að sýna gamla dagsetningu.</span><span class="sxs-lookup"><span data-stu-id="fbaa3-191">The following example shows how you can use a minus sign to indicate a date in the past.</span></span>

|  <span data-ttu-id="fbaa3-192">Segð</span><span class="sxs-lookup"><span data-stu-id="fbaa3-192">Expression</span></span>  |  <span data-ttu-id="fbaa3-193">Merking</span><span class="sxs-lookup"><span data-stu-id="fbaa3-193">Meaning</span></span>  |
|--------------|-----------|
|<span data-ttu-id="fbaa3-194">-1Á</span><span class="sxs-lookup"><span data-stu-id="fbaa3-194">-1Y</span></span>|<span data-ttu-id="fbaa3-195">1 ári fyrir daginn í dag</span><span class="sxs-lookup"><span data-stu-id="fbaa3-195">1 year ago from today</span></span>|

> [!IMPORTANT]
>  <span data-ttu-id="fbaa3-196">Ef staðsetningin notar grunndagatal, er dagsetningarreiknireglan sem er til dæmis færð inn í reitinn **Afhendingartími** túlkuð samkvæmt vinnudögum.</span><span class="sxs-lookup"><span data-stu-id="fbaa3-196">If the location uses a base calendar, then the date formula that you enter in, for example, the **Shipping Time** field is interpreted according to the calendar working days.</span></span> <span data-ttu-id="fbaa3-197">Til dæmis þýðir **1V** sjö vinnudagar.</span><span class="sxs-lookup"><span data-stu-id="fbaa3-197">For example, **1W**  means seven working days.</span></span>

## <a name="see-also"></a><span data-ttu-id="fbaa3-198">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="fbaa3-198">See Also</span></span>
<span data-ttu-id="fbaa3-199">[Unnið með [!INCLUDE[d365fin](includes/d365fin_long_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="fbaa3-199">[Working with [!INCLUDE[d365fin](includes/d365fin_long_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="fbaa3-200">Dagsetning útreiknings fyrir kaup.</span><span class="sxs-lookup"><span data-stu-id="fbaa3-200">Date Calculation for Purchases</span></span>](purchasing-date-calculation-for-purchases.md)  
[<span data-ttu-id="fbaa3-201">Skilgreining skilyrða í síum</span><span class="sxs-lookup"><span data-stu-id="fbaa3-201">Entering Criteria in Filters </span></span>](ui-enter-criteria-filters.md)  

