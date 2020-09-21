---
title: Hvernig á að setja upp Dagatöl verkstæðis | Microsoft Docs
description: Dagatal vinnustöðvar tilgreinir vinnudaga og -stundir, vaktir, frídaga og fjarvistir sem hafa áhrif á mögulega heildarafkastagetu, mælda í tíma, með tilliti til tilgreindra gilda skilvirkni og getu. Stofnun og virkjun dagatals vinnustöðvar þarfnast nokkurra undirbúningsskrefa.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 8fe746bcde1bf02c366664c02ea48029777e22ef
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/09/2020
ms.locfileid: "3777937"
---
# <a name="set-up-shop-calendars"></a><span data-ttu-id="5df82-104">Setja upp dagatal verkstæðis</span><span class="sxs-lookup"><span data-stu-id="5df82-104">Set Up Shop Calendars</span></span>
<span data-ttu-id="5df82-105">Dagatal vinnustöðva eða véla tilgreinir vinnudaga og -stundir, vaktir, frídaga og fjarvistir sem hafa áhrif á mögulega heildarafkastagetu, mælda í tíma, með tilliti til tilgreindra gilda skilvirkni og getu.</span><span class="sxs-lookup"><span data-stu-id="5df82-105">A work center or machine calendar specifies the working days and hours, shifts, holidays, and absences that determine the center’s gross available capacity, measured in time, according to its defined efficiency and capacity values.</span></span>

<span data-ttu-id="5df82-106">Fyrst þarf að setja upp eitt eða fleiri almenn dagatöl verkstæðis, sem grunn fyrir útreikningum á tilteknu dagatali vinnu- eða vélastöðvar.</span><span class="sxs-lookup"><span data-stu-id="5df82-106">As a foundation for calculating a specific work or machine center calendar, you must first set up one or more general shop calendars.</span></span> <span data-ttu-id="5df82-107">Dagatal verkstæðis tilgreinir venjulega vinnuviku eftir upphafs- og lokatíma vinnudags og vaktaskipulagi.</span><span class="sxs-lookup"><span data-stu-id="5df82-107">A shop calendar defines a standard work week according to start and end times of each working day and the work shift relation.</span></span> <span data-ttu-id="5df82-108">Auk þess tilgreinir dagatal verkstæðis fasta frídaga árs.</span><span class="sxs-lookup"><span data-stu-id="5df82-108">In addition, the shop calendar defines the fixed holidays during a year.</span></span>  

<span data-ttu-id="5df82-109">Eftirfarandi lýsir því hvernig á að setja upp dagatöl vinnustöðva.</span><span class="sxs-lookup"><span data-stu-id="5df82-109">The following describes how to set up work center calendars.</span></span> <span data-ttu-id="5df82-110">Skrefin eru svipuð þegar sett eru upp dagatöl vélastöðva.</span><span class="sxs-lookup"><span data-stu-id="5df82-110">The steps are similar when setting up machine center calendars.</span></span>  

## <a name="to-create-work-shifts"></a><span data-ttu-id="5df82-111">Vaktir stofnaðar</span><span class="sxs-lookup"><span data-stu-id="5df82-111">To create work shifts</span></span>  
1.  <span data-ttu-id="5df82-112">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Vaktir** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="5df82-112">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Work Shifts**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="5df82-113">Númer er fært inn í reitinn **Kóti** á auðri línu til að auðkenna vaktina t.d. **1**.</span><span class="sxs-lookup"><span data-stu-id="5df82-113">On a blank line, enter a number in the **Code** field to identify the work shift, for example, **1**.</span></span>  
3.  <span data-ttu-id="5df82-114">Vaktinni er lýst í reitnum **Lýsing** t.d. **1. vakt**</span><span class="sxs-lookup"><span data-stu-id="5df82-114">Describe the work shift in the **Description** field, for example, **1st shift**.</span></span>  
4.  <span data-ttu-id="5df82-115">Einnig er hægt að fylla inn í línur fyrir aðra og þriðju vakt.</span><span class="sxs-lookup"><span data-stu-id="5df82-115">Optionally, fill in lines for a second or third work shift.</span></span>  

<span data-ttu-id="5df82-116">Jafnvel þótt vinnustöðvarnar noti ekki vaktaskipulag þarf að færa inn a.m.k. einn vaktakóta.</span><span class="sxs-lookup"><span data-stu-id="5df82-116">Even if your work centers do not work in different work shifts, enter at least one work shift code.</span></span>  

## <a name="to-set-up-a-shop-calendar"></a><span data-ttu-id="5df82-117">Dagatal verkstæðis sett upp</span><span class="sxs-lookup"><span data-stu-id="5df82-117">To set up a shop calendar</span></span>  
1.  <span data-ttu-id="5df82-118">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Dagatal verkstæðis** eða Lánardrottinn og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="5df82-118">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Shop Calendars**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="5df82-119">Númer er fært inn í reitinn **Kóti** á auðri línu til að auðkenna dagatal verkstæðis.</span><span class="sxs-lookup"><span data-stu-id="5df82-119">On a blank line, enter a number in the **Code** field to identify the shop calendar.</span></span>  
3.  <span data-ttu-id="5df82-120">Dagatali verkstæðisins er lýst í reitnum **Lýsing**.</span><span class="sxs-lookup"><span data-stu-id="5df82-120">Describe the shop calendar in the **Description** field.</span></span>  
4.  <span data-ttu-id="5df82-121">Velja aðgerðina **vinnudagar**.</span><span class="sxs-lookup"><span data-stu-id="5df82-121">Choose the **Working Days** action.</span></span>
5.  <span data-ttu-id="5df82-122">Á síðunni **Dagatal verkstæðis vinnudagar**, skal skilgreina heila vinnuviku, með upphafs- og lokatíma fyrir hvern dag.</span><span class="sxs-lookup"><span data-stu-id="5df82-122">On the **Shop Calendar Working Days** page, define a complete work week, with the start and end times for each day.</span></span>  

    <span data-ttu-id="5df82-123">Í reitnum **Vaktakóti** er hægt að velja einn af vöktunum sem áður voru skilgreind.</span><span class="sxs-lookup"><span data-stu-id="5df82-123">In the **Work Shift Code** field, select one of the shifts that you previously defined.</span></span> <span data-ttu-id="5df82-124">Bæta við línu fyrir hvern vinnudag og hverja vakt.</span><span class="sxs-lookup"><span data-stu-id="5df82-124">Add a line for every working day and every shift.</span></span> <span data-ttu-id="5df82-125">Dæmi:</span><span class="sxs-lookup"><span data-stu-id="5df82-125">For example:</span></span>  

    <span data-ttu-id="5df82-126">Mánudagur 07:00 15:00 1</span><span class="sxs-lookup"><span data-stu-id="5df82-126">Monday  07:00 15:00 1</span></span>   
    <span data-ttu-id="5df82-127">Þriðjudagur 07:00 15:00 1</span><span class="sxs-lookup"><span data-stu-id="5df82-127">Tuesday 07:00 15:00 1</span></span>  

    <span data-ttu-id="5df82-128">Ef þörf er á dagatali verkstæðis með tveimur vöktum þarf að fylla inn í hana á þennan hátt:</span><span class="sxs-lookup"><span data-stu-id="5df82-128">If you need a shop calendar with two work shifts, you must fill it in in this manner:</span></span>  

    <span data-ttu-id="5df82-129">Mánudagur 07:00 15:00 1</span><span class="sxs-lookup"><span data-stu-id="5df82-129">Monday 07:00 15:00 1</span></span>   
    <span data-ttu-id="5df82-130">Mánudagur 15:00 23:00 2</span><span class="sxs-lookup"><span data-stu-id="5df82-130">Monday 15:00 23:00 2</span></span>  
    <span data-ttu-id="5df82-131">Þriðjudagur 07:00 15:00 1</span><span class="sxs-lookup"><span data-stu-id="5df82-131">Tuesday 07:00 15:00 1</span></span>  
    <span data-ttu-id="5df82-132">Þriðjudagur 15:00 23:00 2</span><span class="sxs-lookup"><span data-stu-id="5df82-132">Tuesday 15:00 23:00 2</span></span>  

    <span data-ttu-id="5df82-133">Allir vikudagar sem ekki eru tilgreindir í dagatali verkstæðis, t.d. laugardagur og sunnudagur, eru teknir sem frídagar og hafa enga mögulega afkastagetu í dagatali vinnustöðvar.</span><span class="sxs-lookup"><span data-stu-id="5df82-133">Any week days that you do not define in the shop calendar, such as Saturday and Sunday, are considered non-working days and will have zero available capacity in a work center calendar.</span></span>  

    <span data-ttu-id="5df82-134">Þegar allir vinnudagar hafa verið skilgreindir má loka síðunni **Vinnudagar í verkstæðisáætlun** og byrja að færa inn frídaga.</span><span class="sxs-lookup"><span data-stu-id="5df82-134">When all the working days of a week are defined, you can close the **Shop Calendar Working Days** page and proceed to enter holidays.</span></span>  

6.  <span data-ttu-id="5df82-135">Á síðunni **Dagatöl verkstæðis** veljið dagatal verkstæðisins og veljið síðan **Frídagar** aðgerðina.</span><span class="sxs-lookup"><span data-stu-id="5df82-135">On the **Shop Calendars** page, select the shop calendar, and then choose the **Holidays** action.</span></span>
7. <span data-ttu-id="5df82-136">Á síðunni **Dagatal verkstæðis frídagar** skal skilgreina frídaga ársins með því að slá inn upphafs- og lokadagsetningu/-tíma þeirra og lýsingu á hverjum frídegi í hverja línu fyrir sig.</span><span class="sxs-lookup"><span data-stu-id="5df82-136">On the **Shop Calendar Holidays** page, define the holidays of the year by entering the start date and time, the end time, and description of each holiday on individual lines.</span></span> <span data-ttu-id="5df82-137">Dæmi:</span><span class="sxs-lookup"><span data-stu-id="5df82-137">For example:</span></span>  

    <span data-ttu-id="5df82-138">04/07/14 0:00:00 23:59:00 sumarfrí</span><span class="sxs-lookup"><span data-stu-id="5df82-138">04/07/14 0:00:00 23:59:00 Summer Holiday</span></span>  
    <span data-ttu-id="5df82-139">05/07/14 0:00:00 23:59:00 sumarfrí</span><span class="sxs-lookup"><span data-stu-id="5df82-139">05/07/14 0:00:00 23:59:00 Summer Holiday</span></span>  
    <span data-ttu-id="5df82-140">06/07/14 0:00:00 23:59:00 sumarfrí</span><span class="sxs-lookup"><span data-stu-id="5df82-140">06/07/14 0:00:00 23:59:00 Summer Holiday</span></span>  

<span data-ttu-id="5df82-141">Tilgreindir frídagar hafa enga mögulega afkastagetu í dagatali vinnustöðvar.</span><span class="sxs-lookup"><span data-stu-id="5df82-141">The defined holidays will have zero available capacity in a work center calendar.</span></span>  

<span data-ttu-id="5df82-142">Nú er hægt að úthluta dagatali verkstæðis á vinnustöð til útreiknings á dagatali vinnustöðvar sem mun stjórna tímasetningum aðgerða á þeirri vinnustöð.</span><span class="sxs-lookup"><span data-stu-id="5df82-142">The shop calendar can now be assigned to a work center to calculate the work shop calendar that will govern all operation scheduling at that work center.</span></span>  

## <a name="to-calculate-a-work-center-calendar"></a><span data-ttu-id="5df82-143">Dagatal vinnustöðvar reiknað út</span><span class="sxs-lookup"><span data-stu-id="5df82-143">To calculate a work center calendar</span></span>  

1.  <span data-ttu-id="5df82-144">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Vinnustöðvar** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="5df82-144">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Work Centers**, and then choose the related link.</span></span>
2. <span data-ttu-id="5df82-145">Opna vinnustöðina sem á að uppfæra.</span><span class="sxs-lookup"><span data-stu-id="5df82-145">Open the work center that you want to update.</span></span>  
3. <span data-ttu-id="5df82-146">Í reitnum **Dagatalskóti verkstæðis**, er valið hvaða dagatal verkstæði notar sem grunn fyrir dagatal vinnustöðvar.</span><span class="sxs-lookup"><span data-stu-id="5df82-146">In the **Shop Calendar Code** field, select which shop calendar to use as the foundation for a work center calendar.</span></span>  
4. <span data-ttu-id="5df82-147">Veljið aðgerðina **Dagatal**.</span><span class="sxs-lookup"><span data-stu-id="5df82-147">Choose the **Calendar** action.</span></span>  
5. <span data-ttu-id="5df82-148">Á síðunni **Dagatal vinnustöðvar**, skal velja **Sýna fylki** aðgerðina.</span><span class="sxs-lookup"><span data-stu-id="5df82-148">On the **Work Center Calendar** page, choose the **Show Matrix** action.</span></span>  

    <span data-ttu-id="5df82-149">Vinstra megin á fylkjasíðunni má sjá uppsettar vinnustöðvar.</span><span class="sxs-lookup"><span data-stu-id="5df82-149">The left side of the matrix page lists the work centers that are set up.</span></span> <span data-ttu-id="5df82-150">Hægra megin er dagatal sem birtir tiltæk getugildi fyrir hvern vinnudag í skilgreindri mælieiningu, til dæmis **480** mínútur.</span><span class="sxs-lookup"><span data-stu-id="5df82-150">The right side shows a calendar displaying the available capacity values for each working day in the defined unit of measure, for example, **480** minutes.</span></span> <span data-ttu-id="5df82-151">Hver lína táknar dagatal einnar vinnustöðvar.</span><span class="sxs-lookup"><span data-stu-id="5df82-151">Each line represents the calendar of one work center.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="5df82-152">Einnig er hægt að skoða gildi afkastagetu fyrir hverja viku eða mánuð með því að breyta valinu í reitnum **Skoða eftir** á síðunni **Dagatal vinnustöðvar**.</span><span class="sxs-lookup"><span data-stu-id="5df82-152">You can also select to view the capacity values for each week or month by changing the selection in the **View By** field on the **Work Center Calendar** page.</span></span>  

    <span data-ttu-id="5df82-153">Til að sýna nýtt dagatal verkstæðis sem línu á valdri vinnustöð verður það fyrst að vera reiknað.</span><span class="sxs-lookup"><span data-stu-id="5df82-153">To reflect the new shop calendar as a line on the selected work center, it must first be calculated.</span></span>  

6.  <span data-ttu-id="5df82-154">Velja aðgerðina **Reikna**.</span><span class="sxs-lookup"><span data-stu-id="5df82-154">Choose the **Calculate** action.</span></span>  
7.  <span data-ttu-id="5df82-155">Á flýtiflipanum **Vinnustöð** er hægt að setja afmörkun til að reikna einungis fyrir eina vinnustöð.</span><span class="sxs-lookup"><span data-stu-id="5df82-155">On the **Work Center** FastTab, you can set a filter to only calculate for one work center.</span></span> <span data-ttu-id="5df82-156">Ef engar afmarkanir eru settar verða öll stofnuð dagatöl vinnustöðva reiknuð.</span><span class="sxs-lookup"><span data-stu-id="5df82-156">If you do not set a filter, all existing work center calendars will be calculated.</span></span>  
8.  <span data-ttu-id="5df82-157">Skilgreina upphafs- og lokadagsetningar dagatalstímabilsins sem á að reikna, t.d. eitt ár ; frá 01/01/14 til 31/12/14.</span><span class="sxs-lookup"><span data-stu-id="5df82-157">Define the starting and ending dates of the calendar period that should be calculated, for example, one year from 01/01/14 to 31/12/14.</span></span>
9. <span data-ttu-id="5df82-158">Velja hnappinn **Í lagi** til að reikna út afkastaveitu.</span><span class="sxs-lookup"><span data-stu-id="5df82-158">Choose the **OK** button to calculate capacity.</span></span>  

<span data-ttu-id="5df82-159">Dagatalsfærslur eru nú búnar til (eða þær uppfærðar) og sýna þær mögulega afkastagetu fyrir hvert tímabil með tilliti til eftirfarandi 3 gerða aðalgagna:</span><span class="sxs-lookup"><span data-stu-id="5df82-159">Calendar entries are now created or updated displaying the available capacity for each period according to the following three sets of master data:</span></span>  

- <span data-ttu-id="5df82-160">Vinnudögum og vöktum sem tilgreind eru í úthlutuðu dagatali verkstæðis.</span><span class="sxs-lookup"><span data-stu-id="5df82-160">The working days and shift defined in the assigned shop calendar.</span></span>  
- <span data-ttu-id="5df82-161">Gildinu í reitnum **Geta** á vinnustöðvarspjaldinu.</span><span class="sxs-lookup"><span data-stu-id="5df82-161">The value in the **Capacity** field on the work center card.</span></span>  
- <span data-ttu-id="5df82-162">Gildinu í reitnum **Skilvirkni** á vinnustöðvarspjaldinu.</span><span class="sxs-lookup"><span data-stu-id="5df82-162">The value in the **Efficiency** field on the work center card.</span></span>  

<span data-ttu-id="5df82-163">Reiknað dagatal vinnustöðvar skilgreinir nú hvenær og hversu mikil afkastageta er til staðar í þessari vinnustöð.</span><span class="sxs-lookup"><span data-stu-id="5df82-163">The calculated work center calendar will now define when and how much capacity is available at this work center.</span></span> <span data-ttu-id="5df82-164">Þetta stýrir ítarlegri röðun aðgerða sem framkvæmdar eru í vinnustöðinni.</span><span class="sxs-lookup"><span data-stu-id="5df82-164">This controls the detailed scheduling of operations performed at the work center.</span></span>  

## <a name="to-record-work-center-absence"></a><span data-ttu-id="5df82-165">Fjarvistir í vinnustöð skráðar</span><span class="sxs-lookup"><span data-stu-id="5df82-165">To record work center absence</span></span>  
1.  <span data-ttu-id="5df82-166">Á síðunni **Dagatal vinnustöðvar**, skal velja **Sýna fylki** aðgerðina.</span><span class="sxs-lookup"><span data-stu-id="5df82-166">On the **Work Center Calendar** page, choose the **Show Matrix** action.</span></span>
2. <span data-ttu-id="5df82-167">Á síðunni **Dagatal vinnustöðvar fylki** er valin vinnustöð sem og sá dagur dagatalsins sem skrá á fjarvistina á og svo er smellt á aðgerðina **Fjarvist**.</span><span class="sxs-lookup"><span data-stu-id="5df82-167">On the **Work Center Calendar Matrix** page, select the work center and calendar day when the absence time should be recorded, and then choose the **Absence** action.</span></span>  
3.  <span data-ttu-id="5df82-168">Á síðunni **Fjarvist** er tilgreindur upphafs- og lokatími fjarvistar þessa dags sem og lýsing á henni.</span><span class="sxs-lookup"><span data-stu-id="5df82-168">On the **Absence** page, define the starting time, ending time, and description of that day’s absence.</span></span> <span data-ttu-id="5df82-169">Dæmi:</span><span class="sxs-lookup"><span data-stu-id="5df82-169">For example:</span></span>  

    <span data-ttu-id="5df82-170">25/01/01 08:00 10:00 viðhald</span><span class="sxs-lookup"><span data-stu-id="5df82-170">25/01/01 08:00 10:00 Maintenance</span></span>  

4.  <span data-ttu-id="5df82-171">Velja **Uppfæra** aðgerðina og síðan loka **Fjarvist** síðunni.</span><span class="sxs-lookup"><span data-stu-id="5df82-171">Choose the **Update** action, and then close the **Absence** page.</span></span>  

<span data-ttu-id="5df82-172">Afkastageta þessa dags hefur nú minnkað í samræmi við skráðan fjarvistartíma.</span><span class="sxs-lookup"><span data-stu-id="5df82-172">The capacity of the selected day has now decreased by the recorded absence time.</span></span>  

## <a name="see-also"></a><span data-ttu-id="5df82-173">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="5df82-173">See Also</span></span>  
[<span data-ttu-id="5df82-174">Setja upp grunndagatöl</span><span class="sxs-lookup"><span data-stu-id="5df82-174">Set Up Base Calendars</span></span>](across-how-to-assign-base-calendars.md)  
[<span data-ttu-id="5df82-175">Setja upp vinnu- og vélastöðvar</span><span class="sxs-lookup"><span data-stu-id="5df82-175">Set Up Work Centers and Machine Centers</span></span>](production-how-to-set-up-work-and-machine-centers.md)  
[<span data-ttu-id="5df82-176">Uppsetning framleiðslu</span><span class="sxs-lookup"><span data-stu-id="5df82-176">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
[<span data-ttu-id="5df82-177">Framleiðsla</span><span class="sxs-lookup"><span data-stu-id="5df82-177">Manufacturing</span></span>](production-manage-manufacturing.md)  
<span data-ttu-id="5df82-178">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="5df82-178">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
