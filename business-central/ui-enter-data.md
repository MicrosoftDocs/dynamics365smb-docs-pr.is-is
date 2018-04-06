---
title: "Hvernig á að færa inn gögn í reiti | Microsoft Docs"
description: "Það eru margar grunnaðgerðir sem auðvelda og flýta fyrir gagnainnfærslu. Öllum grunnaðgerðum við gagnainnslátt er lýst í þessu efnisatriði."
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/19/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: e7dcdc0935a8793ae226dfc2f9709b5b8f487a62
ms.openlocfilehash: 4354e28522d359cf9fa6178c4a1919831dcc52db
ms.contentlocale: is-is
ms.lasthandoff: 03/22/2018

---

# <a name="entering-data"></a><span data-ttu-id="9b1bf-104">Gagnainnfærsla</span><span class="sxs-lookup"><span data-stu-id="9b1bf-104">Entering Data</span></span>
<span data-ttu-id="9b1bf-105">Það eru margar grunnaðgerðir sem auðvelda og flýta fyrir gagnainnfærslu.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-105">There are many general functions that help you enter data  in a quick and easy way.</span></span> <span data-ttu-id="9b1bf-106">Öllum grunnaðgerðum við gagnainnslátt er lýst í þessu efnisatriði.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-106">The general functions for entering data are described in this article.</span></span>  

<span data-ttu-id="9b1bf-107">Í dæmunum í þessu efnisatriði er notast við sýnigögn.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-107">The examples in this article use the demonstration data.</span></span>

## <a name="mandatory-fields"></a><span data-ttu-id="9b1bf-108">Áskildir reitir</span><span class="sxs-lookup"><span data-stu-id="9b1bf-108">Mandatory Fields</span></span>
<span data-ttu-id="9b1bf-109">Þegar þú slærð inn gögn á síðum, eru tilteknir reitir merktir með rauðri stjörnu.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-109">When you enter data on pages, certain fields are marked with a red asterisk.</span></span> <span data-ttu-id="9b1bf-110">Rauða stjarnan merkir að fylla verður reitinn út til að ljúka tilteknu ferli sem notar reitinn, eins og að bóka færslu sem notar gildið í reitnum.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-110">The red asterisk means that the field must be filled to complete a certain process that uses the field, such as posting a transaction that uses the value in the field.</span></span>  

<span data-ttu-id="9b1bf-111">Jafnvel þótt reiturinn innihaldi rauða stjörnu er ekki nauðsynlegt að fylla út í reitinn áður en haldið er áfram í aðra reiti eða síðunni lokað.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-111">Even though the field contains a red asterisk, you are not forced to fill the field before you continue to other fields or close the page.</span></span> <span data-ttu-id="9b1bf-112">Rauða stjarnan er eingöngu áminning um að þú verðir útilokaður frá tilteknu ferli.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-112">The red asterisk only serves as a reminder that you will be blocked from completing a certain process.</span></span>  


## <a name="finding-data-as-you-type"></a><span data-ttu-id="9b1bf-113">Finna gögn um leið og ritað er</span><span class="sxs-lookup"><span data-stu-id="9b1bf-113">Finding Data As You Type</span></span>  
 <span data-ttu-id="9b1bf-114">Þegar byrjað er að slá inn stafi í reit birtist fellilisti með mögulegum gildum.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-114">When you start to type characters in a field, a drop-down list is displayed and shows possible field values.</span></span> <span data-ttu-id="9b1bf-115">Listinn breytist eftir því sem fleiri stafir eru slegnir inn og hægt er að velja rétt gildi þegar það birtist.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-115">The list changes as you type more characters, and you can select the correct value when it is displayed.</span></span>  

 <span data-ttu-id="9b1bf-116">Margir af reitunum eru með örvahnapp niður sem hægt er að velja.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-116">Many fields have a down arrow button that you can choose.</span></span> <span data-ttu-id="9b1bf-117">Örin er valin til að fá lista yfir gögn sem tiltæk eru til að færa inn í reitinn.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-117">You choose the arrow to get a list of data that is available to enter in the field.</span></span> <span data-ttu-id="9b1bf-118">Hnappurinn hefur tvær aðgerðir, eftir því hver tegund reitsins er:</span><span class="sxs-lookup"><span data-stu-id="9b1bf-118">The button has two functions depending on the type of field:</span></span>  

-   <span data-ttu-id="9b1bf-119">Uppfletting - Birtir upplýsingar úr annarri töflu sem færa má inn í reitinn.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-119">Lookup - Displays information from another table that you can enter in the field.</span></span> <span data-ttu-id="9b1bf-120">Hægt er að velja eina gagnaeiningu í einu.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-120">You can select one piece of data at a time.</span></span>  

-   <span data-ttu-id="9b1bf-121">Fellival - Birtir safn valkosta sem í boði eru fyrir reitinn.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-121">Drop-down - Displays the set of options that exist for the field.</span></span> <span data-ttu-id="9b1bf-122">Aðeins er hægt að velja einn kost.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-122">You can select only one of the options.</span></span>  

<!--Onprem ## Copy Fields or Lines  
 Depending on the type of writable document, you can copy individual line fields or whole lines to other lines in the document. Read-only data, such as posted entries, cannot be copied.  

 Several database dependencies are used to determine if fields or lines can be copied. One way to determine these dependencies is to view the shortcut menu. The content of the shortcut menu indicates which copy functions are supported by displaying either of these functions:  

-   Copy Cell  

-   Copy Rows  

-   Paste Rows  

 For example, database records, such as lines on a sales order, and master data, such as cards in the **Items** window, cannot be duplicated. For this kind of data, the shortcut menu typically has the **Copy Cell** or **Copy Rows**  functions. If the **Paste** function is not available this indicates that you can only paste the data into external documents. Single fields on a sales line, however, can be copied to the same column in other sales lines.  

 Journal lines are very flexible and can be copied freely in the same journal, indicated by the presence of **Paste** on the shortcut menu.  

> [!NOTE]  
>   If you copy a journal line or document line, the fields that are not in your view are not copied to the new line.

#### To copy previous field  

-   To enter the value of the field immediately above the active field, select **Copy Previous** from the shortcut menu.-->

## <a name="entering-quantities-by-calculation"></a><span data-ttu-id="9b1bf-123">Magn slegið inn eftir útreikningum</span><span class="sxs-lookup"><span data-stu-id="9b1bf-123">Entering Quantities by Calculation</span></span>  
 <span data-ttu-id="9b1bf-124">Þegar tölur eru færðar inn í magnreiti, svo sem reitinn **Magn** í birgðabókarlínu, er hægt að færa inn reikniregluna í stað heiltölumagns.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-124">When entering numbers into quantity fields, such as the **Quantity** field on an item journal line, you can enter the formula instead of the sum quantity.</span></span>  

## <a name="examples"></a><span data-ttu-id="9b1bf-125">Dæmi</span><span class="sxs-lookup"><span data-stu-id="9b1bf-125">Examples</span></span>  

-   <span data-ttu-id="9b1bf-126">Ef tölurnar 19+19 eru slegnar inn er niðurstaðan í reitnum 38.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-126">If you enter 19+19, the field is calculated to 38.</span></span>  

-   <span data-ttu-id="9b1bf-127">Ef tölurnar 41-9 eru slegnar inn er niðurstaðan í reitnum 32.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-127">If you enter 41-9, the field is calculated to 32.</span></span>  

-   <span data-ttu-id="9b1bf-128">Ef tölurnar 12\*4 eru slegnar inn er niðurstaðan í reitnum 48.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-128">If you enter 12\*4, the field is calculated to 48.</span></span>  

-   <span data-ttu-id="9b1bf-129">Ef tölurnar 12/4 eru slegnar inn er niðurstaðan í reitnum 3.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-129">If you enter 12/4, the field is calculated to 3.</span></span>  

## <a name="entering-negative-numbers"></a><span data-ttu-id="9b1bf-130">Neikvæðar tölur er færðar inn</span><span class="sxs-lookup"><span data-stu-id="9b1bf-130">Entering Negative Numbers</span></span>
<span data-ttu-id="9b1bf-131">Hægt er að færa inn neikvæðar tölur eftir tveimur leiðum.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-131">You can enter negative numbers in two ways.</span></span> <span data-ttu-id="9b1bf-132">Númerið -20.5 má færa inn sem:</span><span class="sxs-lookup"><span data-stu-id="9b1bf-132">The number -20.5 can be entered as:</span></span>  

-   <span data-ttu-id="9b1bf-133">-20.5</span><span class="sxs-lookup"><span data-stu-id="9b1bf-133">-20.5</span></span>  

    <span data-ttu-id="9b1bf-134">Eða</span><span class="sxs-lookup"><span data-stu-id="9b1bf-134">or</span></span>
-   <span data-ttu-id="9b1bf-135">20.5-</span><span class="sxs-lookup"><span data-stu-id="9b1bf-135">20.5-</span></span>  

 <span data-ttu-id="9b1bf-136">Í báðum tilfellum verður upphæðin skráð í  sem -20.5.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-136">In both cases, the amount will be recorded in as -20.5.</span></span>  

 <span data-ttu-id="9b1bf-137">Ef síðasti stafur segðarinnar er **+** eða **-**, mun öll segðin verða skráð með því formerki.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-137">If the last character of the expression is a **+** or a **-**, the entire expression will be recorded with that sign.</span></span> <span data-ttu-id="9b1bf-138">Dæmi: **10-20+** mun gefa niðurstöðuna 10 en ekki -10.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-138">An example, **10-20+** will result in 10 and not -10.</span></span>  

## <a name="entering-dates-and-times"></a><span data-ttu-id="9b1bf-139">Dagsetning og tími færð inn</span><span class="sxs-lookup"><span data-stu-id="9b1bf-139">Entering Dates and Times</span></span>
<span data-ttu-id="9b1bf-140">Færa má inn dagsetningar og tíma í alla þá reiti sem ætlaðir eru fyrir dagsetningar (dagsetningarreitir).</span><span class="sxs-lookup"><span data-stu-id="9b1bf-140">You can enter dates and times in all the fields that are specifically assigned to dates (date fields).</span></span> <span data-ttu-id="9b1bf-141">Hægt er að færa inn dagsetningar með eða án skiltákna.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-141">You can enter dates with or without separators.</span></span>

> [!NOTE]  
> <span data-ttu-id="9b1bf-142">Hvernig skal Færa inn dagsetningu og tíma fer eftir **Svæði** stillingunum þínum.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-142">How you enter dates and times depends on your **Region** settings.</span></span> <span data-ttu-id="9b1bf-143">Frekari upplýsingar, sjá [Breyta grunnstillingum](ui-change-basic-settings.md).</span><span class="sxs-lookup"><span data-stu-id="9b1bf-143">For more information, see [Changing Basic Settings](ui-change-basic-settings.md).</span></span>  

### <a name="entering-dates"></a><span data-ttu-id="9b1bf-144">Dagsetningar færðar inn</span><span class="sxs-lookup"><span data-stu-id="9b1bf-144">Entering Dates</span></span>  
 <span data-ttu-id="9b1bf-145">Í dagsetningarreit má færa inn tvær, fjórar, sex eða átta tölur:</span><span class="sxs-lookup"><span data-stu-id="9b1bf-145">In a date field you can enter two, four, six, or eight digits:</span></span>  

-   <span data-ttu-id="9b1bf-146">Ef aðeins tvær tölur eru færðar inn þá túlkar kerfið þær sem daginn og bætir við mánuði og ári vinnudagsetningar.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-146">If you enter only two digits, this is interpreted as the day, and it will add the month and the year of the work date.</span></span>  

-   <span data-ttu-id="9b1bf-147">Ef færðar eru inn fjórar tölur þá túlkar kerfið þær sem daginn og mánuðinn og bætir við ári vinnudagsetningar.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-147">If you enter four digits, this is interpreted as the day and the month, and it will add the year of the work date.</span></span>  

-   <span data-ttu-id="9b1bf-148">Ef sú dagsetning sem færa á inn er á bilinu 01/01/1930 til 31/12/2029 má færa árið inn í tveimur tölum; annars skal færa árið inn með fjórum tölum.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-148">If the date you want to enter is in the range 01/01/1930 through 12/31/2029, you can enter the year with two digits; otherwise, enter the year with four digits.</span></span>  

 <span data-ttu-id="9b1bf-149">Einnig er hægt að færa inn dagsetningu sem vikudag ásamt vikunúmeri og hugsanlega ári (til dæmis Mán25 eða mán25 þýðir mánudagur í 25. viku).</span><span class="sxs-lookup"><span data-stu-id="9b1bf-149">You can also enter a date as a weekday followed by a week number and, optionally, a year (for example, Mon25 or mon25 means Monday in week 25).</span></span>  

 <span data-ttu-id="9b1bf-150">Hægt er að færa inn einn af tveimur kóðum í stað sérstakrar dagsetningar.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-150">Instead of entering a specific date, you can enter one of two codes.</span></span>  

|<span data-ttu-id="9b1bf-151">Kóði</span><span class="sxs-lookup"><span data-stu-id="9b1bf-151">Code</span></span>|<span data-ttu-id="9b1bf-152">Niðurstaða</span><span class="sxs-lookup"><span data-stu-id="9b1bf-152">Result</span></span>|  
|--------------|----------------|  
|<span data-ttu-id="9b1bf-153">t</span><span class="sxs-lookup"><span data-stu-id="9b1bf-153">t</span></span>|<span data-ttu-id="9b1bf-154">Þetta er dagurinn í dag (kerfisdagsetning tölvunnar).</span><span class="sxs-lookup"><span data-stu-id="9b1bf-154">This is today's date (the system date for the computer).</span></span>|  
|<span data-ttu-id="9b1bf-155">v</span><span class="sxs-lookup"><span data-stu-id="9b1bf-155">w</span></span>|<span data-ttu-id="9b1bf-156">Þetta er vinnudagurinn sem er settur upp í forritinu.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-156">This is the work date that is setup in the application.</span></span> <span data-ttu-id="9b1bf-157">Vinnudagsetningunni breytt úr valmyndinni [Breyta grunnstillingum](ui-change-basic-settings.md)</span><span class="sxs-lookup"><span data-stu-id="9b1bf-157">To change the work date, see [Changing Basic Settings](ui-change-basic-settings.md).</span></span> <span data-ttu-id="9b1bf-158">Handhægt gæti verið að nota vinnudagsetningar ef verið er að nota margar færslur með aðra dagsetningu en dagsins í dag.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-158">You may want to use a work date if you have many transactions with a date other than today's date.</span></span>|  

<!--Onprem ## Closing Date  
 When you close a fiscal year, you can use closing dates to indicate that an entry is a closing entry. A closing date technically is between two dates, for example between Dec 31 and Jan 1.  

 To specify that a date is a closing date, put C just before the date: C123101. -->

## <a name="entering-times"></a><span data-ttu-id="9b1bf-159">Tími færður inn</span><span class="sxs-lookup"><span data-stu-id="9b1bf-159">Entering Times</span></span>  
 <span data-ttu-id="9b1bf-160">Þegar tímasetningar eru ritaðar er hægt að setja inn hvaða skiltákn sem er milli eininga en það er ekki nauðsynlegt.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-160">When you enter times, you can insert any separator sign that you want between the units, but it is not required.</span></span> <span data-ttu-id="9b1bf-161">Ekki þarf að tilgreina mínútur, sekúndur eða FH/EH.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-161">You do not have to write minutes, seconds, or AM/PM.</span></span>  

 <span data-ttu-id="9b1bf-162">Í eftirfarandi töflu birtast mismunandi leiðir til að færa inn tímasetningar og hvernig þær eru túlkaðar:</span><span class="sxs-lookup"><span data-stu-id="9b1bf-162">The following table lists the various ways in which times can be entered and how they are interpreted.</span></span>  

|<span data-ttu-id="9b1bf-163">Færsla</span><span class="sxs-lookup"><span data-stu-id="9b1bf-163">Entry</span></span>|<span data-ttu-id="9b1bf-164">Túlkun</span><span class="sxs-lookup"><span data-stu-id="9b1bf-164">Interpretation</span></span>|  
|---------------|------------------------|  
|<span data-ttu-id="9b1bf-165">5</span><span class="sxs-lookup"><span data-stu-id="9b1bf-165">5</span></span>|<span data-ttu-id="9b1bf-166">05:00:00</span><span class="sxs-lookup"><span data-stu-id="9b1bf-166">05:00:00</span></span>|  
|<span data-ttu-id="9b1bf-167">5:30</span><span class="sxs-lookup"><span data-stu-id="9b1bf-167">5:30</span></span>|<span data-ttu-id="9b1bf-168">05:30:00</span><span class="sxs-lookup"><span data-stu-id="9b1bf-168">05:30:00</span></span>|  
|<span data-ttu-id="9b1bf-169">0530</span><span class="sxs-lookup"><span data-stu-id="9b1bf-169">0530</span></span>|<span data-ttu-id="9b1bf-170">05:30:00</span><span class="sxs-lookup"><span data-stu-id="9b1bf-170">05:30:00</span></span>|  
|<span data-ttu-id="9b1bf-171">5:30:5</span><span class="sxs-lookup"><span data-stu-id="9b1bf-171">5:30:5</span></span>|<span data-ttu-id="9b1bf-172">05:30:05</span><span class="sxs-lookup"><span data-stu-id="9b1bf-172">05:30:05</span></span>|  
|<span data-ttu-id="9b1bf-173">053005</span><span class="sxs-lookup"><span data-stu-id="9b1bf-173">053005</span></span>|<span data-ttu-id="9b1bf-174">05:30:05</span><span class="sxs-lookup"><span data-stu-id="9b1bf-174">05:30:05</span></span>|  
|<span data-ttu-id="9b1bf-175">5:30:5,50</span><span class="sxs-lookup"><span data-stu-id="9b1bf-175">5:30:5,50</span></span>|<span data-ttu-id="9b1bf-176">05:30:05,5</span><span class="sxs-lookup"><span data-stu-id="9b1bf-176">05:30:05.5</span></span>|  
|<span data-ttu-id="9b1bf-177">053005050</span><span class="sxs-lookup"><span data-stu-id="9b1bf-177">053005050</span></span>|<span data-ttu-id="9b1bf-178">05:30:05.05</span><span class="sxs-lookup"><span data-stu-id="9b1bf-178">05:30:05.05</span></span>|  

 <span data-ttu-id="9b1bf-179">Rita þarf tvær tölur fyrir hverja tímaeiningu ef skiltákn er ekki notað.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-179">You must enter two digits for each unit of time if you do not enter a separator.</span></span>  

## <a name="entering-datetimes"></a><span data-ttu-id="9b1bf-180">Dagsetning og tímasetning færð inn</span><span class="sxs-lookup"><span data-stu-id="9b1bf-180">Entering Datetimes</span></span>  
 <span data-ttu-id="9b1bf-181">Þegar dagsetning og tími eru færð inn verður að vera bil milli dags og tímasetningar.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-181">When you enter datetimes you must enter a space between the date and the time.</span></span>  

 <span data-ttu-id="9b1bf-182">Í eftirfarandi töflu birtast mismunandi leiðir til að færa inn dagsetningar og tímasetningar og hvernig þær eru túlkaðar:</span><span class="sxs-lookup"><span data-stu-id="9b1bf-182">The following table lists the various ways in which you can enter datetimes and how they are interpreted.</span></span>  

|<span data-ttu-id="9b1bf-183">Færsla</span><span class="sxs-lookup"><span data-stu-id="9b1bf-183">Entry</span></span>|<span data-ttu-id="9b1bf-184">Túlkun</span><span class="sxs-lookup"><span data-stu-id="9b1bf-184">Interpretation</span></span>|  
|---------------|------------------------|  
|<span data-ttu-id="9b1bf-185">131202 132455</span><span class="sxs-lookup"><span data-stu-id="9b1bf-185">131202 132455</span></span>|<span data-ttu-id="9b1bf-186">13-12-02 13:24:55</span><span class="sxs-lookup"><span data-stu-id="9b1bf-186">13-12-02 13:24:55</span></span>|  
|<span data-ttu-id="9b1bf-187">1-12-02 10</span><span class="sxs-lookup"><span data-stu-id="9b1bf-187">1-12-02 10</span></span>|<span data-ttu-id="9b1bf-188">01-12-02 10:00:00</span><span class="sxs-lookup"><span data-stu-id="9b1bf-188">01-12-02 10:00:00</span></span>|  
|<span data-ttu-id="9b1bf-189">1.12.02 5</span><span class="sxs-lookup"><span data-stu-id="9b1bf-189">1.12.02 5</span></span>|<span data-ttu-id="9b1bf-190">01-12-02 05:00:00</span><span class="sxs-lookup"><span data-stu-id="9b1bf-190">01-12-02 05:00:00</span></span>|  
|<span data-ttu-id="9b1bf-191">1.12.02</span><span class="sxs-lookup"><span data-stu-id="9b1bf-191">1.12.02</span></span>|<span data-ttu-id="9b1bf-192">01-12-02 00:00:00</span><span class="sxs-lookup"><span data-stu-id="9b1bf-192">01-12-02 00:00:00</span></span>|  
|<span data-ttu-id="9b1bf-193">11 12</span><span class="sxs-lookup"><span data-stu-id="9b1bf-193">11 12</span></span>|<span data-ttu-id="9b1bf-194">11-gildandi mánuður-gildandi ár 12:00:00</span><span class="sxs-lookup"><span data-stu-id="9b1bf-194">11-current month-current year 12:00:00</span></span>|  
|<span data-ttu-id="9b1bf-195">1112 12</span><span class="sxs-lookup"><span data-stu-id="9b1bf-195">1112 12</span></span>|<span data-ttu-id="9b1bf-196">11-12-gildandi ár 12:00:00</span><span class="sxs-lookup"><span data-stu-id="9b1bf-196">11-12-current year 12:00:00</span></span>|  
|<span data-ttu-id="9b1bf-197">d eða dagurinn í dag</span><span class="sxs-lookup"><span data-stu-id="9b1bf-197">t or today</span></span>|<span data-ttu-id="9b1bf-198">dagurinn í dag 00:00:00</span><span class="sxs-lookup"><span data-stu-id="9b1bf-198">today's date 00:00:00</span></span>|  
|<span data-ttu-id="9b1bf-199">t tími</span><span class="sxs-lookup"><span data-stu-id="9b1bf-199">t time</span></span>|<span data-ttu-id="9b1bf-200">gildandi tími dagsins í dag</span><span class="sxs-lookup"><span data-stu-id="9b1bf-200">today's date actual time</span></span>|  
|<span data-ttu-id="9b1bf-201">d 10:30</span><span class="sxs-lookup"><span data-stu-id="9b1bf-201">t 10:30</span></span>|<span data-ttu-id="9b1bf-202">dagurinn í dag 10:30:00</span><span class="sxs-lookup"><span data-stu-id="9b1bf-202">today's date 10:30:00</span></span>|  
|<span data-ttu-id="9b1bf-203">d 03:03:03</span><span class="sxs-lookup"><span data-stu-id="9b1bf-203">t 3:3:3</span></span>|<span data-ttu-id="9b1bf-204">dagurinn í dag 03:03:03</span><span class="sxs-lookup"><span data-stu-id="9b1bf-204">today's date 03:03:03</span></span>|  
|<span data-ttu-id="9b1bf-205">v eða vinnudagsetningin</span><span class="sxs-lookup"><span data-stu-id="9b1bf-205">w or workdate</span></span>|<span data-ttu-id="9b1bf-206">vinnudagsetningin 00:00:00</span><span class="sxs-lookup"><span data-stu-id="9b1bf-206">the working date 00:00:00</span></span>|  
|<span data-ttu-id="9b1bf-207">m eða mánudagur</span><span class="sxs-lookup"><span data-stu-id="9b1bf-207">m or Monday</span></span>|<span data-ttu-id="9b1bf-208">Mánudagur yfirstandandi viku 00:00:00</span><span class="sxs-lookup"><span data-stu-id="9b1bf-208">Monday of the current week 00:00:00</span></span>|  
|<span data-ttu-id="9b1bf-209">þr eða þriðjudagur</span><span class="sxs-lookup"><span data-stu-id="9b1bf-209">tu or Tuesday</span></span>|<span data-ttu-id="9b1bf-210">Þriðjudagur yfirstandandi viku 00:00:00</span><span class="sxs-lookup"><span data-stu-id="9b1bf-210">Tuesday of the current week 00:00:00</span></span>|  
|<span data-ttu-id="9b1bf-211">mi eða miðvikudagur</span><span class="sxs-lookup"><span data-stu-id="9b1bf-211">we or Wednesday</span></span>|<span data-ttu-id="9b1bf-212">Miðvikudagur yfirstandandi viku 00:00:00</span><span class="sxs-lookup"><span data-stu-id="9b1bf-212">Wednesday of the current week 00:00:00</span></span>|  
|<span data-ttu-id="9b1bf-213">fi eða fimmtudagur</span><span class="sxs-lookup"><span data-stu-id="9b1bf-213">th or Thursday</span></span>|<span data-ttu-id="9b1bf-214">Fimmtudagur yfirstandandi viku 00:00:00</span><span class="sxs-lookup"><span data-stu-id="9b1bf-214">Thursday of the current week 00:00:00</span></span>|  
|<span data-ttu-id="9b1bf-215">f eða föstudagur</span><span class="sxs-lookup"><span data-stu-id="9b1bf-215">f or Friday</span></span>|<span data-ttu-id="9b1bf-216">Föstudagur yfirstandandi viku 00:00:00</span><span class="sxs-lookup"><span data-stu-id="9b1bf-216">Friday of the current week 00:00:00</span></span>|  
|<span data-ttu-id="9b1bf-217">l eða laugardagur</span><span class="sxs-lookup"><span data-stu-id="9b1bf-217">s or Saturday</span></span>|<span data-ttu-id="9b1bf-218">Laugardagur yfirstandandi viku 00:00:00</span><span class="sxs-lookup"><span data-stu-id="9b1bf-218">Saturday of the current week 00:00:00</span></span>|  
|<span data-ttu-id="9b1bf-219">s eða sunnudagur</span><span class="sxs-lookup"><span data-stu-id="9b1bf-219">su or Sunday</span></span>|<span data-ttu-id="9b1bf-220">Sunnudagur yfirstandandi viku 00:00:00</span><span class="sxs-lookup"><span data-stu-id="9b1bf-220">Sunday of the current week 00:00:00</span></span>|  
|<span data-ttu-id="9b1bf-221">þr 10:30:00</span><span class="sxs-lookup"><span data-stu-id="9b1bf-221">tu 10:30</span></span>|<span data-ttu-id="9b1bf-222">Þriðjudagur yfirstandandi viku 10:30:00</span><span class="sxs-lookup"><span data-stu-id="9b1bf-222">Tuesday of the current week 10:30:00</span></span>|  
|<span data-ttu-id="9b1bf-223">þr 03:03:03</span><span class="sxs-lookup"><span data-stu-id="9b1bf-223">tu 3:3:3</span></span>|<span data-ttu-id="9b1bf-224">Þriðjudagur yfirstandandi viku 03:03:03</span><span class="sxs-lookup"><span data-stu-id="9b1bf-224">Tuesday of the current week 03:03:03</span></span>|  

## <a name="entering-duration"></a><span data-ttu-id="9b1bf-225">Færið inn tímalengd</span><span class="sxs-lookup"><span data-stu-id="9b1bf-225">Entering Duration</span></span>  
 <span data-ttu-id="9b1bf-226">Hægt er að færa inn tímalengd sem tölu og mælieiningu.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-226">You enter a duration as a number followed by its unit of measure.</span></span>  

 <span data-ttu-id="9b1bf-227">Hér eru nokkur dæmi.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-227">Here are some examples.</span></span>  

|<span data-ttu-id="9b1bf-228">Lengd</span><span class="sxs-lookup"><span data-stu-id="9b1bf-228">Duration</span></span>|<span data-ttu-id="9b1bf-229">Mælieining**</span><span class="sxs-lookup"><span data-stu-id="9b1bf-229">Unit of measure**</span></span>|  
|------------------|-------------------------|  
|<span data-ttu-id="9b1bf-230">2t</span><span class="sxs-lookup"><span data-stu-id="9b1bf-230">2h</span></span>|<span data-ttu-id="9b1bf-231">2 klst</span><span class="sxs-lookup"><span data-stu-id="9b1bf-231">2 hrs</span></span>|  
|<span data-ttu-id="9b1bf-232">6t 30 m</span><span class="sxs-lookup"><span data-stu-id="9b1bf-232">6h 30 m</span></span>|<span data-ttu-id="9b1bf-233">6 klst 30 mín</span><span class="sxs-lookup"><span data-stu-id="9b1bf-233">6 hrs 30 mins</span></span>|  
|<span data-ttu-id="9b1bf-234">6,5t</span><span class="sxs-lookup"><span data-stu-id="9b1bf-234">6.5h</span></span>|<span data-ttu-id="9b1bf-235">6 klst 30 mín</span><span class="sxs-lookup"><span data-stu-id="9b1bf-235">6 hrs 30 mins</span></span>|  
|<span data-ttu-id="9b1bf-236">90m</span><span class="sxs-lookup"><span data-stu-id="9b1bf-236">90m</span></span>|<span data-ttu-id="9b1bf-237">1 klst 30 mín</span><span class="sxs-lookup"><span data-stu-id="9b1bf-237">1 hr 30 mins</span></span>|  
|<span data-ttu-id="9b1bf-238">2d 6t 30m</span><span class="sxs-lookup"><span data-stu-id="9b1bf-238">2d 6h 30m</span></span>|<span data-ttu-id="9b1bf-239">2 dagar 6 klst 30 mín</span><span class="sxs-lookup"><span data-stu-id="9b1bf-239">2 days 6 hrs 30 mins</span></span>|  
|<span data-ttu-id="9b1bf-240">2d 6t 30m 56s 600ms</span><span class="sxs-lookup"><span data-stu-id="9b1bf-240">2d 6h 30m 56s 600ms</span></span>|<span data-ttu-id="9b1bf-241">2 dagar 6 klst 30 mín 56 sek 600 millis</span><span class="sxs-lookup"><span data-stu-id="9b1bf-241">2 days 6 hrs 30 mins 56 secs 600 msecs</span></span>|  

 <span data-ttu-id="9b1bf-242">Einnig er hægt að færa inn tölu og þá er henni sjálfkrafa breytt í tímalengd.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-242">You can also enter a number and it is automatically converted to a duration.</span></span> <span data-ttu-id="9b1bf-243">Tölunni sem færð er inn er breytt samkvæmt sjálfgefnu mælieiningunni sem hefur verið tilgreind fyrir reitinn tímalengd.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-243">The number you enter is converted according to the default unit of measure that has been specified for the duration field.</span></span>  

 <span data-ttu-id="9b1bf-244">Hægt er að sjá hvaða mælieining er notuð í reitnum tímalengd með því að færa inn tölu og sjá í hvaða mælieiningu kerfið færir hana í.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-244">To see what unit of measure is being used in a duration field, enter a number and see which unit of measure it is converted to.</span></span>  

 <span data-ttu-id="9b1bf-245">Tölunni 5 er breytt í 5 klst. ef mælieiningin er klukkustundir.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-245">The number 5 is converted to 5 hrs, if the unit of measure is hours.</span></span>  

<!--OnPrem  ##  <a name="BKMK_SettingDateRanges"></a> Setting Date Ranges  
 You can set filters containing a start date and an end date to display only the data contained in that date range or time interval. Special rules apply to the way you set date ranges.  

|**Meaning**|**Sample expression**|**Entries included**|  
|-----------------|---------------------------|--------------------------|  
|**Equal to**|12 15 00|Only those posted on 12 15 00.|  
|**Interval**|12 15 00..01 15 01<br /><br /> ..12 15 00|Those posted on dates between and including 12 15 00 and 01 15 01.<br /><br /> Those posted on 12 15 00 or earlier.|  
|**Either/or**|12 15 00&#124;12 16 00|Those posted on either 12 15 00 or 12 16 00. If there are entries posted on both days, they will all be displayed.|  

 You can also combine the various format types.  

|**Sample expression**|**Entries included**|  
|---------------------------|--------------------------|  
|12 15 00&#124;12 01 00..12 10 00|Entries posted either on 12 15 00 or on dates between and including 12 01 00 and 12 10 00.|  
|..12 14 00&#124;12 30 00..|Entries posted on 12 14 00 or earlier, or entries posted on 12 30 00 or later - that is, all entries except those posted on dates between and including 12 15 00 and 12 29 00.|  -->

## <a name="using-date-formulas"></a><span data-ttu-id="9b1bf-246">Notkun dagsetningarreiknireglna</span><span class="sxs-lookup"><span data-stu-id="9b1bf-246">Using Date Formulas</span></span>  
 <span data-ttu-id="9b1bf-247">Dagsetningarregla er stutt, skammstöfuð samsetning stafa og tölustafa sem tilgreinir hvernig skal reikna út dagsetningar.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-247">A date formula is a short, abbreviated combination of letters and numbers that specifies how to calculate dates.</span></span> <span data-ttu-id="9b1bf-248">Hægt er að færa dagsetningarreiknireglur í ólíka dagsetningarreiknireiti og í ítrekunartíðnireiti í ítrekunarbókum.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-248">You can enter date formulas in various date calculation fields and in recurring frequency fields in recurring journals.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="9b1bf-249">Dagurinn í dag, fyrir upphaf tímabilsins, er með í öllum reitum fyrir reiknireglur dagsetninga.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-249">In all data formula fields, one day is automatically included to cover today as the day when the period starts.</span></span> <span data-ttu-id="9b1bf-250">Í samræmi við það, ef fært er inn 1V, til dæmis, er tímabilið í raun átta dagar þar sem dagurinn í dag er tekinn með.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-250">Accordingly, if you enter 1W, for example, then the period is actually eight days because today is included.</span></span> <span data-ttu-id="9b1bf-251">Til að tilgreina sjö daga tímabil (ein raunvika) að meðtalinni upphafsdagsetningu tímabilsins þarf að færa inn 6D eða 1W-1D.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-251">To specify a period of seven days (one true week) including the period starting date, then you must enter 6D or 1W-1D.</span></span>  

 <span data-ttu-id="9b1bf-252">Hér eru nokkur dæmi um hvernig nota má dagsetningarreiknireglur:</span><span class="sxs-lookup"><span data-stu-id="9b1bf-252">Here are some examples of how date formulas can be used:</span></span>  

-   <span data-ttu-id="9b1bf-253">Dagsetningarreikniregla í ítrekunartíðnireitnum í ítrekunarbókum ákvarðar hversu oft færsla í færslubókarlínu er bókuð.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-253">The date formula in the recurring frequency field in recurring journals determines how often the entry on the journal line will be posted.</span></span>  

-   <span data-ttu-id="9b1bf-254">Dagsetningarreikniregla í reitnum Biðtími fyrir tiltekið innheimtustig ákvarðar það tímabil sem þarf að líða frá gjalddaga (eða frá dagsetningu fyrri innheimtubréfs) áður en innheimtubréf er búið til.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-254">The date formula in the Grace Period field for a specified reminder level determines the period of time that must pass from the due date (or from the date of the previous reminder) before a reminder will be created.</span></span>  

-   <span data-ttu-id="9b1bf-255">Dagsetningarreikniregla í reitnum Gjalddagaútreikningur ákvarðar hvernig kerfið reiknar gjalddaga á innheimtubréfinu.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-255">The date formula in the Due Date Calculation field determines how to calculate the due date on the reminder.</span></span>  

 <span data-ttu-id="9b1bf-256">Dagsetningarreikniregla getur mest haft 20 stafi, bæði tölu- og bókstafi.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-256">The date calculation formula can contain a maximum of 20 characters, both numbers and letters.</span></span> <span data-ttu-id="9b1bf-257">Hægt er að nota eftirfarandi stafi sem skammstafanir fyrir tiltekinn tíma.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-257">You can use the following letters, which are abbreviations for time specifications.</span></span>  

|||  
|-|-|  
|<span data-ttu-id="9b1bf-258">C</span><span class="sxs-lookup"><span data-stu-id="9b1bf-258">C</span></span>|<span data-ttu-id="9b1bf-259">Gildandi</span><span class="sxs-lookup"><span data-stu-id="9b1bf-259">Current</span></span>|  
|<span data-ttu-id="9b1bf-260">D</span><span class="sxs-lookup"><span data-stu-id="9b1bf-260">D</span></span>|<span data-ttu-id="9b1bf-261">Dagar</span><span class="sxs-lookup"><span data-stu-id="9b1bf-261">Day(s)</span></span>|  
|<span data-ttu-id="9b1bf-262">W</span><span class="sxs-lookup"><span data-stu-id="9b1bf-262">W</span></span>|<span data-ttu-id="9b1bf-263">Vikur</span><span class="sxs-lookup"><span data-stu-id="9b1bf-263">Week(s)</span></span>|  
|<span data-ttu-id="9b1bf-264">M</span><span class="sxs-lookup"><span data-stu-id="9b1bf-264">M</span></span>|<span data-ttu-id="9b1bf-265">Mánuðir</span><span class="sxs-lookup"><span data-stu-id="9b1bf-265">Month(s)</span></span>|  
|<span data-ttu-id="9b1bf-266">F</span><span class="sxs-lookup"><span data-stu-id="9b1bf-266">Q</span></span>|<span data-ttu-id="9b1bf-267">Fjórðungar</span><span class="sxs-lookup"><span data-stu-id="9b1bf-267">Quarter(s)</span></span>|  
|<span data-ttu-id="9b1bf-268">Á</span><span class="sxs-lookup"><span data-stu-id="9b1bf-268">Y</span></span>|<span data-ttu-id="9b1bf-269">Ár</span><span class="sxs-lookup"><span data-stu-id="9b1bf-269">Year(s)</span></span>|  

 <span data-ttu-id="9b1bf-270">Hægt er að rita dagsetningarreiknireglu á þrjá vegu.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-270">You can construct a date formula in three ways.</span></span>  

 <span data-ttu-id="9b1bf-271">Eftirfarandi dæmi sýnir hvernig núverandi og tímaeining.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-271">The following example shows how current plus a time unit.</span></span>  

|||  
|-|-|  
|<span data-ttu-id="9b1bf-272">LV</span><span class="sxs-lookup"><span data-stu-id="9b1bf-272">CW</span></span>|<span data-ttu-id="9b1bf-273">Líðandi vika</span><span class="sxs-lookup"><span data-stu-id="9b1bf-273">Current week</span></span>|  
|<span data-ttu-id="9b1bf-274">LM</span><span class="sxs-lookup"><span data-stu-id="9b1bf-274">CM</span></span>|<span data-ttu-id="9b1bf-275">Líðandi mánuður</span><span class="sxs-lookup"><span data-stu-id="9b1bf-275">Current month</span></span>|  

 <span data-ttu-id="9b1bf-276">Eftirfarandi dæmi sýnir hvernig tala og tímaeining.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-276">The following example shows how a number and a time unit.</span></span> <span data-ttu-id="9b1bf-277">Talan getur ekki verið hærri en 9999.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-277">A number cannot be larger than 9999.</span></span>  

|||  
|-|-|  
|<span data-ttu-id="9b1bf-278">10D</span><span class="sxs-lookup"><span data-stu-id="9b1bf-278">10D</span></span>|<span data-ttu-id="9b1bf-279">10 dögum eftir daginn í dag</span><span class="sxs-lookup"><span data-stu-id="9b1bf-279">10 days from today</span></span>|  
|<span data-ttu-id="9b1bf-280">2V</span><span class="sxs-lookup"><span data-stu-id="9b1bf-280">2W</span></span>|<span data-ttu-id="9b1bf-281">2 vikum eftir daginn í dag</span><span class="sxs-lookup"><span data-stu-id="9b1bf-281">2 weeks from today</span></span>|  

 <span data-ttu-id="9b1bf-282">Eftirfarandi dæmi sýnir hvernig tímaeining og tala.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-282">The following example shows how a time unit and a number.</span></span>  

|||  
|-|-|  
|<span data-ttu-id="9b1bf-283">D10</span><span class="sxs-lookup"><span data-stu-id="9b1bf-283">D10</span></span>|<span data-ttu-id="9b1bf-284">Næsti 10. dagur mánaðar</span><span class="sxs-lookup"><span data-stu-id="9b1bf-284">The next 10th day of a month</span></span>|  
|<span data-ttu-id="9b1bf-285">VD4</span><span class="sxs-lookup"><span data-stu-id="9b1bf-285">WD4</span></span>|<span data-ttu-id="9b1bf-286">Næsti 4. dagur viku (fimmtudagur)</span><span class="sxs-lookup"><span data-stu-id="9b1bf-286">The next 4th day of a week (Thursday)</span></span>|  

 <span data-ttu-id="9b1bf-287">Eftirfarandi dæmi sýnir hvernig eigi að samræma þessi þrjú eyðublöð eins og þörf er á.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-287">The following example shows how you can combine these three forms as needed.</span></span>  

|||  
|-|-|  
|<span data-ttu-id="9b1bf-288">LM+10D</span><span class="sxs-lookup"><span data-stu-id="9b1bf-288">CM+10D</span></span>|<span data-ttu-id="9b1bf-289">Líðandi mánuður + 10 dagar</span><span class="sxs-lookup"><span data-stu-id="9b1bf-289">Current month + 10 days</span></span>|  

 <span data-ttu-id="9b1bf-290">Eftirfarandi dæmi sýnir hvernig hægt er að nota mínustákn til að sýna gamla dagsetningu.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-290">The following example shows how you can use a minus sign to indicate a date in the past.</span></span>  

|||  
|-|-|  
|<span data-ttu-id="9b1bf-291">-1Á</span><span class="sxs-lookup"><span data-stu-id="9b1bf-291">-1Y</span></span>|<span data-ttu-id="9b1bf-292">1 ári fyrir daginn í dag</span><span class="sxs-lookup"><span data-stu-id="9b1bf-292">1 year ago from today</span></span>|  

<!--OnPrem > [!CAUTION]  
>  If the location uses a base calendar, then the date formula that you enter in, for example, the **Shipping Time** field is interpreted according to the calendar working days. For example, a 1W means seven working days. For more information, see Base Calendar Card.-->  
## <a name="see-also"></a><span data-ttu-id="9b1bf-293">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="9b1bf-293">See Also</span></span>  
 [<span data-ttu-id="9b1bf-294">Leita í, afmarka og raða gögnum</span><span class="sxs-lookup"><span data-stu-id="9b1bf-294">Searching, Filtering, and Sorting Data</span></span>](ui-enter-criteria-filters.md)  
 <span data-ttu-id="9b1bf-295">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="9b1bf-295">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

