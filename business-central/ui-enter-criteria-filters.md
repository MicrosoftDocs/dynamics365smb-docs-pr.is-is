---
title: Röðun, leit og síun í listum | Microsoft Docs
description: Vinna á skilvirkan hátt í listum með því að leita yfir gögnin þín, flokka dálka og hreinsa niðurstöður með síutáknum og flýtivísum.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: delimit, FlowFilter, totals, limit, advanced
ms.date: 11/16/2020
ms.author: jswymer
ms.openlocfilehash: eda7ab79b326f860816504014d6eefa9fb13a600
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/17/2020
ms.locfileid: "4757593"
---
# <a name="sorting-searching-and-filtering"></a><span data-ttu-id="062b6-103">Röðun, leit og síun</span><span class="sxs-lookup"><span data-stu-id="062b6-103">Sorting, Searching, and Filtering</span></span>

<span data-ttu-id="062b6-104">Það eru nokkrir hlutir sem munu hjálpa þér að skanna, finna og takmarka skrár í lista, skýrslu eða XMLport.</span><span class="sxs-lookup"><span data-stu-id="062b6-104">There are a few things that you can do that will help you scan, find, and limit records on a list or in a report or XMLport.</span></span> <span data-ttu-id="062b6-105">Þar á meðal er röðun, leit og afmörkun.</span><span class="sxs-lookup"><span data-stu-id="062b6-105">These include sorting, searching, and filtering.</span></span> <span data-ttu-id="062b6-106">Þú getur notað suma eða alla þessa hluti samtímis til að finna eða greina gögnin þín fljótt.</span><span class="sxs-lookup"><span data-stu-id="062b6-106">You can apply some or all of these simultaneously to quickly find or analyze your data.</span></span>

<span data-ttu-id="062b6-107">Fyrir skýrslur og XMLport, líkt og í listum, er hægt að stilla síur til að afmarka hvaða gögn eigi að taka með í skýrslunni eða XMLport, en ekki er hægt að raða og leita.</span><span class="sxs-lookup"><span data-stu-id="062b6-107">For reports and XMLports, as on lists, you can set filters to delimit which data to include in the report or XMLport, but you can't sort and search.</span></span>

> [!TIP]
> <span data-ttu-id="062b6-108">Þegar þú skoðar gögnin þín sem flísar getur þú leitað og notað síun.</span><span class="sxs-lookup"><span data-stu-id="062b6-108">When viewing your data as tiles, you can search and use filtering.</span></span> <span data-ttu-id="062b6-109">Til að nota alla þessa öflugu eiginleika til að raða, leita og sía skaltu velja táknið ![Sýna sem lista](media/ui_show_as_list_icon.png "Sýna sem listaör til vinstri") til að sýna færslurnar sem lista.</span><span class="sxs-lookup"><span data-stu-id="062b6-109">To use the full set of powerful features for sorting, searching, and filtering, choose the ![Show as list](media/ui_show_as_list_icon.png "Show as list arrow left") icon to view the records as a list.</span></span>

<!--
When you want to search for data, such as customer names, addresses, or product groups, you enter criteria. In search criteria, you can use all the numbers and letters that you normally use in the specific field. In addition, you can use special symbols to further filter the results. There are two ways to search: using the Quick Filter or column filters.
-->

## <a name="sorting"></a><span data-ttu-id="062b6-110">Röðun</span><span class="sxs-lookup"><span data-stu-id="062b6-110">Sorting</span></span>

<span data-ttu-id="062b6-111">Með Röðun er auðvelt og fljótlegt að fá yfirsýn yfir gögnin.</span><span class="sxs-lookup"><span data-stu-id="062b6-111">Sorting makes it easy for you to get a quick overview of your data.</span></span> <span data-ttu-id="062b6-112">Ef þú ert til dæmis með marga viðskiptamenn, gætirðu raðað þeim eftir **Viðskiptamannanr.**, **Gjaldmiðilskóða** eða **Svæðiskóða lands** til að fá yfirlitið sem þú þarft.</span><span class="sxs-lookup"><span data-stu-id="062b6-112">For example, if you have many customers,  you could sort them by **Customer No.**, **Currency Code**, or **Country Region Code** to get the overview you need.</span></span>

<span data-ttu-id="062b6-113">Til að raða lista geturðu annaðhvort:</span><span class="sxs-lookup"><span data-stu-id="062b6-113">To sort a list, you can either:</span></span>

- <span data-ttu-id="062b6-114">Valið fyrirsagnartexta dálks til að skipta milli hækkandi og lækkandi röð eða</span><span class="sxs-lookup"><span data-stu-id="062b6-114">Choose a column heading text to toggle between ascending and descending order, or</span></span>
- <span data-ttu-id="062b6-115">Valið örina sem vísar niður í dálkhaus, valið síðan aðgerðina **Hækkandi** eða **Lækkandi**.</span><span class="sxs-lookup"><span data-stu-id="062b6-115">Choose the drop-down arrow in the column heading, then choose the **Ascending** or **Descending** action.</span></span>  

> [!NOTE]  
> <span data-ttu-id="062b6-116">Myndir, BLOB-reitir, FlowFilters og reitir sem tilheyra ekki töflu styðja ekki röðun.</span><span class="sxs-lookup"><span data-stu-id="062b6-116">Sorting isn't supported on images, BLOB fields, FlowFilters, and fields that do not belong to a table.</span></span>  

## <a name="searching"></a><span data-ttu-id="062b6-117">Leit</span><span class="sxs-lookup"><span data-stu-id="062b6-117">Searching</span></span>

<!--## Searching by using the Quick Filter -->
<span data-ttu-id="062b6-118">Efst á sérhverri listasíðu er ![Leita í lista](media/ui-search/search-list.png "Tákn fyrir leitarlista") **Leita** aðgerðin sem býður upp á fljótlega og auðvelda leið til að vinna gögnin niður í lista og sýna einungis þær skrár sem innihalda gögnin sem þú vilt sjá.</span><span class="sxs-lookup"><span data-stu-id="062b6-118">At the top of each list page, there's a ![Search list](media/ui-search/search-list.png "Search list icon") **Search** action that provides a quick and easy way to reduce the records in a list and display only those records that contain the data that you're interested in seeing.</span></span>

<span data-ttu-id="062b6-119">Til að leita skaltu einfaldlega velja aðgerðina **Leita** og síðan skrifa í boxið textann sem er verið að leita að.</span><span class="sxs-lookup"><span data-stu-id="062b6-119">To search, just choose the **Search** action, and then in the box, type the text that you're looking for.</span></span> <span data-ttu-id="062b6-120">Þú getur slegið inn stafi, númer og önnur tákn.</span><span class="sxs-lookup"><span data-stu-id="062b6-120">You can enter letters, numbers, and other symbols.</span></span>

<span data-ttu-id="062b6-121">Almennt mun leit reyna að finna samsvarandi texta í öllum reitum.</span><span class="sxs-lookup"><span data-stu-id="062b6-121">In general, search will attempt to match text across all fields.</span></span> <span data-ttu-id="062b6-122">Leitin mun ekki gera greinarmun á hástöfum og lágstöfum (óháð há- og lágstöfum) og mun finna textasamsvörun hvar sem er í reitnum (fremst, aftast eða í miðjunni).</span><span class="sxs-lookup"><span data-stu-id="062b6-122">It doesn't distinguish between uppercase and lowercase characters (case insensitive) and will match text placed anywhere in the field, at the beginning, end, or in the middle.</span></span>

> [!TIP]
> <span data-ttu-id="062b6-123">Þú getur ýtt á **F3** til að virkja og slökkva á leitarreitnum.</span><span class="sxs-lookup"><span data-stu-id="062b6-123">You can press **F3** to activate and deactivate the search box.</span></span> <span data-ttu-id="062b6-124">Frekari upplýsingar, sjá [Flýtilyklar](keyboard-shortcuts.md#KeyboardFilter).</span><span class="sxs-lookup"><span data-stu-id="062b6-124">For more information, see [Keyboard Shortcuts](keyboard-shortcuts.md#KeyboardFilter).</span></span>

> [!NOTE]  
> <span data-ttu-id="062b6-125">Leit mun ekki passa við gildi í myndum, BLOB-reitum, Flow-síum, FlowFields-reitum og öðrum reitum sem eru ekki hluti af töflu.</span><span class="sxs-lookup"><span data-stu-id="062b6-125">Search won't match values in images, BLOB fields, FlowFilters, FlowFields, and other fields that aren't part of a table.</span></span>


### <a name="fine-tuning-the-search-with-filter-criteria"></a><span data-ttu-id="062b6-126">Fínstilla leitina með síuskilyrði</span><span class="sxs-lookup"><span data-stu-id="062b6-126">Fine-tuning the Search with Filter criteria</span></span>

<span data-ttu-id="062b6-127">Hægt er að gera nákvæmari leit með því að nota virknitákn síu, segðir og síumerki.</span><span class="sxs-lookup"><span data-stu-id="062b6-127">You can make a more exact search by using filter operators, expressions, and filter tokens.</span></span> <span data-ttu-id="062b6-128">Ólíkt síun er þetta notað yfir alla reiti þegar það er notað í leitarglugganum, sem gerir þá ekki eins skilvirka og síun.</span><span class="sxs-lookup"><span data-stu-id="062b6-128">Unlike filtering, these are applied across all fields when used in the search box, making them less efficient than filtering.</span></span>

- <span data-ttu-id="062b6-129">Til að finna aðeins reitargildi sem samsvara öllum textanum og stöfunum, skal staðsetja textann á milli einfaldra gæsalappa `''` (til dæmis, `'man'`).</span><span class="sxs-lookup"><span data-stu-id="062b6-129">To find only field values that match the entire text and case exactly, place the search text between single quotes `''` (for example, `'man'`).</span></span>

- <span data-ttu-id="062b6-130">Til að finna reitargildi sem byrja á ákveðnum texta og samsvara stöfunum, skal setja `*` á eftir leitartextanum (til dæmis `man*`).</span><span class="sxs-lookup"><span data-stu-id="062b6-130">To find field values that start with a certain text and match the case, place `*` after the search text (for example `man*`).</span></span>

- <span data-ttu-id="062b6-131">Til að finna reitargildi sem enda á ákveðnum texta og samsvara stöfunum, skal setja `*` á undan leitartextanum (til dæmis `*man`).</span><span class="sxs-lookup"><span data-stu-id="062b6-131">To find field values that end with a certain text and match the case, place `*` before the search text (for example `*man`).</span></span>

- <span data-ttu-id="062b6-132">Þegar `''` eða `*` er notað er leitin stafrétt.</span><span class="sxs-lookup"><span data-stu-id="062b6-132">When using  `''` or `*`, the search is case-sensitive.</span></span> <span data-ttu-id="062b6-133">Ef þú vilt gera leitina óháða há- og lágstöfum skaltu setja `@` á undan leitartextanum (til dæmis `@man*`).</span><span class="sxs-lookup"><span data-stu-id="062b6-133">If you want to make the search case insensitive, place `@` before the search text (for example `@man*`).</span></span>

<span data-ttu-id="062b6-134">Eftirfarandi tafla sýnir nokkur dæmi til að útskýra hvernig hægt er að nota leitina.</span><span class="sxs-lookup"><span data-stu-id="062b6-134">The following table provides some examples to explain how you can use the search.</span></span>

|<span data-ttu-id="062b6-135">Leitarskilyrði</span><span class="sxs-lookup"><span data-stu-id="062b6-135">Search Criteria</span></span>|<span data-ttu-id="062b6-136">Finnur ...</span><span class="sxs-lookup"><span data-stu-id="062b6-136">Finds...</span></span>|
|---------------|----------|
|`man`<br /><span data-ttu-id="062b6-137">eða</span><span class="sxs-lookup"><span data-stu-id="062b6-137">or</span></span> <br />`Man`|<span data-ttu-id="062b6-138">Allar skrár með reitum sem innihalda textann **man**, óháð því hvort notaðir eru há- eða lágstafir.</span><span class="sxs-lookup"><span data-stu-id="062b6-138">All records with fields that contain the text **man**, regardless of the case.</span></span> <span data-ttu-id="062b6-139">Til dæmis, **Manchester**, **manual**, eða **Sportsman**.</span><span class="sxs-lookup"><span data-stu-id="062b6-139">For example, **Manchester**, **manual**, or **Sportsman**.</span></span> |
|`'Man'`|<span data-ttu-id="062b6-140">Allar skrár með reitum sem innihalda aðeins **Man**, í samræmi við há- og lágstafi.</span><span class="sxs-lookup"><span data-stu-id="062b6-140">All records with fields that contain only **Man**, matching the case.</span></span>|
|`Man*`|<span data-ttu-id="062b6-141">Allar skrár með reitum sem byrja á textanum <b>Man</b>, í samræmi við há- og lágstafi.</span><span class="sxs-lookup"><span data-stu-id="062b6-141">All records with fields that start with the text <b>Man</b>, matching the case.</span></span> <span data-ttu-id="062b6-142">Til dæmis, **Manchester** en ekki **manual** eða **Sportsman** .</span><span class="sxs-lookup"><span data-stu-id="062b6-142">For example, **Manchester** but not **manual** or **Sportsman**.</span></span>|
|`@Man*`|<span data-ttu-id="062b6-143">Allar skrár með reitum sem byrja með **man**, óháð því hvort notaðir eru há- eða lágstafir.</span><span class="sxs-lookup"><span data-stu-id="062b6-143">All records with fields that start with **man**, regardless of the case.</span></span> <span data-ttu-id="062b6-144">Til dæmis, **Manchester** og **manual**, en ekki **Sportsman**.</span><span class="sxs-lookup"><span data-stu-id="062b6-144">For example, **Manchester** and **manual**, but not **Sportsman**.</span></span>|
|`@*man`|<span data-ttu-id="062b6-145">Allar skrár sem endar með **man**, óháð því hvort notaðir eru há- eða lágstafir.</span><span class="sxs-lookup"><span data-stu-id="062b6-145">All records that end with **man**, regardless of the case.</span></span> <span data-ttu-id="062b6-146">Til dæmis **Sportsman**, en ekki **Manchester** eða **manual**.</span><span class="sxs-lookup"><span data-stu-id="062b6-146">For example **Sportsman**, but not **Manchester** or **manual**.</span></span>|


## <a name="filtering"></a><a name="filtering"></a><span data-ttu-id="062b6-147">Afmörkun</span><span class="sxs-lookup"><span data-stu-id="062b6-147">Filtering</span></span>

<span data-ttu-id="062b6-148">Síun veitir háþróaðri og fjölhæfari leið til að stjórna því hvaða færslur birtast á lista, skýrslu eða XMLport.</span><span class="sxs-lookup"><span data-stu-id="062b6-148">Filtering provides a more advanced and versatile way to control which records are included in a list, report, or XMLport.</span></span> <span data-ttu-id="062b6-149">Það eru tvær helstu munur á leit og síun, eins og lýst er í töflunni hér að neðan.</span><span class="sxs-lookup"><span data-stu-id="062b6-149">There are two major differences between searching and filtering, as described in the table below.</span></span>

|| <span data-ttu-id="062b6-150">**Leit**</span><span class="sxs-lookup"><span data-stu-id="062b6-150">**Searching**</span></span> | <span data-ttu-id="062b6-151">**Afmörkun**</span><span class="sxs-lookup"><span data-stu-id="062b6-151">**Filtering**</span></span> |
|--|----------|------------|
| <span data-ttu-id="062b6-152">**Reitir sem gilda**</span><span class="sxs-lookup"><span data-stu-id="062b6-152">**Applicable Fields**</span></span> | <span data-ttu-id="062b6-153">Leitar yfir alla reitum sem eru sýnilegar á síðunni.</span><span class="sxs-lookup"><span data-stu-id="062b6-153">Searches across all fields that are visible on the page.</span></span> | <span data-ttu-id="062b6-154">Síar einn eða fleiri reiti, hvern fyrir sig, og velur úr öllum reitum í töflunni, þar á meðal reiti sem eru ekki sýnilegir á síðunni.</span><span class="sxs-lookup"><span data-stu-id="062b6-154">Filters one or more fields individually, selecting from any field on the table, including fields that aren't visible on the page.</span></span> |
| <span data-ttu-id="062b6-155">**Samsvörun**</span><span class="sxs-lookup"><span data-stu-id="062b6-155">**Matching**</span></span> | <span data-ttu-id="062b6-156">Sýnir skrár með reitum sem samsvara leitartextanum, óháð há- og lágstöfum eða staðsetningu textans í reitnum.</span><span class="sxs-lookup"><span data-stu-id="062b6-156">Displays records with fields that match the search text, no matter the text's case or placement in the field.</span></span> | <span data-ttu-id="062b6-157">Sýnir skrár þar sem reiturinn samsvarar nákvæmlega síunni, þ.m.t. há- og lágstöfum textans, nema ef sérstök síutákn eru færð inn.</span><span class="sxs-lookup"><span data-stu-id="062b6-157">Displays records where the field exactly matches the filter, including the text's case, unless special filter symbols are entered.</span></span>

<span data-ttu-id="062b6-158">Síun gerir þér kleift að birta skrár fyrir tiltekna reikninga eða viðskiptamenn, dagsetningar, upphæð og aðrar upplýsingar með því að tilgreina síuviðmiðanir.</span><span class="sxs-lookup"><span data-stu-id="062b6-158">Filtering enables you to display records for specific accounts or customers, dates, amounts, and other information by specifying filter criteria.</span></span> <span data-ttu-id="062b6-159">Aðeins færslur sem samsvara skilyrðunum eru birtar á listanum eða teknar með í skýrslugerð, runuvinnslu eða XMLport.</span><span class="sxs-lookup"><span data-stu-id="062b6-159">Only records that match the criteria are displayed on the list or included in the report, batch job, or XMLport.</span></span> <span data-ttu-id="062b6-160">Ef þú tilgreinir skilyrði fyrir marga reiti, þá birtast aðeins skrár sem passa við öll skilyrði.</span><span class="sxs-lookup"><span data-stu-id="062b6-160">If you specify criteria for multiple fields, then only records that match all criteria will be displayed.</span></span>

<span data-ttu-id="062b6-161">Fyrir lista eru síurnar sýndar á afmörkunarsvæði sem birtist til vinstri á listanum þegar það er virkjað.</span><span class="sxs-lookup"><span data-stu-id="062b6-161">For lists, the filters are displayed on a filter pane that appears to the left of the list when you activate it.</span></span> <span data-ttu-id="062b6-162">Fyrir skýrslur, runuvinnslur og XMLport eru síurnar sýnilegar beint á beiðnisíðunni.</span><span class="sxs-lookup"><span data-stu-id="062b6-162">For reports, batch jobs, and XMLports, the filters are visible directly on the request page.</span></span>

### <a name="filtering-with-option-fields"></a><span data-ttu-id="062b6-163">Sía með valsvæðum</span><span class="sxs-lookup"><span data-stu-id="062b6-163">Filtering with Option Fields</span></span>

<span data-ttu-id="062b6-164">Fyrir „venjulega“ reiti sem innihalda gögn, uppsetningardagsetningu eða viðskiptagögn er hægt að stilla síur bæði með því að velja gögn og með því að slá inn síugildi og hægt er að nota tákn til að skilgreina ítarleg síuskilyrði.</span><span class="sxs-lookup"><span data-stu-id="062b6-164">For "ordinary" fields that hold data, setup date, or business data, you can set filters both by selecting data and by typing filter values, and you can use symbols to define advanced filter criteria.</span></span> <span data-ttu-id="062b6-165">Nánari upplýsingar eru í [Færa inn síuskilyrði](ui-enter-criteria-filters.md#entering-filter-criteria).</span><span class="sxs-lookup"><span data-stu-id="062b6-165">For more information, see [Entering Filter Criteria](ui-enter-criteria-filters.md#entering-filter-criteria).</span></span>

<span data-ttu-id="062b6-166">Fyrir reiti af gerðinni **Valkostir** er hins vegar aðeins hægt að stilla síu með því að velja einn eða fleiri valkosti úr fellilista með tiltækum valkostum.</span><span class="sxs-lookup"><span data-stu-id="062b6-166">For fields of type **Option**, however, you can only set a filter by selecting one or more options from a drop-down list of the available options.</span></span> <span data-ttu-id="062b6-167">Dæmi um valkostsreit er reiturinn **Staða** á síðunni **Sölupantanir**.</span><span class="sxs-lookup"><span data-stu-id="062b6-167">An example of an option field is the **Status** field on the **Sales Orders** page.</span></span>

> [!NOTE]
> <span data-ttu-id="062b6-168">Þegar margir valkostir eru valdir sem síugildi er venslin á milli valkostanna skilgreind sem *EÐA*.</span><span class="sxs-lookup"><span data-stu-id="062b6-168">When you select multiple options as a filter value, the relationship between the options is defined as *OR*.</span></span> <span data-ttu-id="062b6-169">Til dæmis, ef þú velur báða gátreitina **Opið** og **Losað** á afmörkunarsvæðinu **Staða** á síðunni **Sölupantanir**, þýðir það að sölupantanir sem eru annaðhvort opnar eða losaðar eru birtar.</span><span class="sxs-lookup"><span data-stu-id="062b6-169">For example, if you select both the **Open** and the **Released** check box in the **Status** filter field on the **Sales Orders** page, it means that sales orders that are either open or released are displayed.</span></span>

### <a name="setting-filters-on-lists"></a><span data-ttu-id="062b6-170">Afmarkanir stilltar á lista</span><span class="sxs-lookup"><span data-stu-id="062b6-170">Setting Filters on Lists</span></span>

<span data-ttu-id="062b6-171">Á listum eru síur stilltar með því að nota afmörkunarsvæði.</span><span class="sxs-lookup"><span data-stu-id="062b6-171">On lists, you set filters by using the filter pane.</span></span> <span data-ttu-id="062b6-172">Til að birta afmörkunarsvæðið fyrir lista skal velja felliörina við hliðina á heiti síðunnar og velja síðan **Sýna afmörkunarsvæði**.</span><span class="sxs-lookup"><span data-stu-id="062b6-172">To display the filter pane for a list, choose the drop-down arrow next to the name of the page, and then choose the **Show filter pane** action.</span></span> <span data-ttu-id="062b6-173">Að öðrum kosti er stutt á **Shift+F3**.</span><span class="sxs-lookup"><span data-stu-id="062b6-173">Alternatively, press **Shift+F3**.</span></span>

<span data-ttu-id="062b6-174">Til að birta afmörkunarsvæðið fyrir dálk á lista skal velja felliörina og velja síðan aðgerðina **Afmörkun**.</span><span class="sxs-lookup"><span data-stu-id="062b6-174">To display the filter pane for a column on a list, choose the drop-down arrow, and then choose the **Filter** action.</span></span> <span data-ttu-id="062b6-175">Að öðrum kosti er stutt á **Shift+F3**.</span><span class="sxs-lookup"><span data-stu-id="062b6-175">Alternatively, press **Shift+F3**.</span></span> <span data-ttu-id="062b6-176">Afmörkunarsvæðið opnast með völdum dálki sem sýndur er sem afmörkunarsvæðið í hlutanum **Afmarka lista**.</span><span class="sxs-lookup"><span data-stu-id="062b6-176">The filter pane opens with the selected column shown as a filter field in the **Filter list by** section.</span></span>

<span data-ttu-id="062b6-177">Síusvæðið sýnir núverandi síur fyrir lista og gerir þér kleift að stilla eigin sérsniðna síur í einu eða fleiri reitum með því að velja aðgerðina **+ Sía**.</span><span class="sxs-lookup"><span data-stu-id="062b6-177">The filter pane displays the current filters for a list, and enables you to set your own custom filters on one or more fields by choosing the **+ Filter** action.</span></span>

 <span data-ttu-id="062b6-178">Síusvæði er skipt í þrjá hluta: **Skoðanir**, **Sía listi eftir** og **Sía samtölur eftir**:</span><span class="sxs-lookup"><span data-stu-id="062b6-178">A filter pane is divided in three sections: **Views**, **Filter list by**, and **Filter totals by**:</span></span>

- <span data-ttu-id="062b6-179">**Yfirlit**</span><span class="sxs-lookup"><span data-stu-id="062b6-179">**Views**</span></span>

  <span data-ttu-id="062b6-180">Sumir listar hafa hlutann **Yfirlit** með.</span><span class="sxs-lookup"><span data-stu-id="062b6-180">Some lists include the **Views** section.</span></span> <span data-ttu-id="062b6-181">Skoðanir eru afbrigði af listanum sem hefur verið forstillt með síum.</span><span class="sxs-lookup"><span data-stu-id="062b6-181">Views are variations of the list that have been preconfigured with filters.</span></span> <span data-ttu-id="062b6-182">Þú getur skilgreint og vistað eins mörg yfirlit og þú vilt fyrir hvern lista.</span><span class="sxs-lookup"><span data-stu-id="062b6-182">You can define and save as many views as you want per list.</span></span> <span data-ttu-id="062b6-183">Yfirlitin verða aðgengilegt í öllum tækjum sem þú skráir þig inn á.</span><span class="sxs-lookup"><span data-stu-id="062b6-183">The views will be available to you on any device you sign into.</span></span> <span data-ttu-id="062b6-184">Frekari upplýsingar er að finna á [Vista og sérsníða listayfirlit](ui-views.md).</span><span class="sxs-lookup"><span data-stu-id="062b6-184">For more information, see [Save and Personalize List Views](ui-views.md).</span></span>

- <span data-ttu-id="062b6-185">**Sía listi eftir**</span><span class="sxs-lookup"><span data-stu-id="062b6-185">**Filter list by**</span></span>

  <span data-ttu-id="062b6-186">Þetta er hlutinn er þar sem þú bætir við síum á tilteknum reitum til að draga úr fjölda birtra skráa.</span><span class="sxs-lookup"><span data-stu-id="062b6-186">This section is where you add filters on specific fields to reduce the number of displayed records.</span></span> <span data-ttu-id="062b6-187">Til að bæta við síu skal velja aðgerðina **+ Sía**.</span><span class="sxs-lookup"><span data-stu-id="062b6-187">To add a filter, choose the **+ Filter** action.</span></span> <span data-ttu-id="062b6-188">Til að bæta við síu skal slá inn heiti reitsins sem á að sía listann eftir eða velja reit af fellilistanum.</span><span class="sxs-lookup"><span data-stu-id="062b6-188">Then, type the name of the field that you want to filter the list by or pick a field from the drop-down list.</span></span>

- <span data-ttu-id="062b6-189">**Sía samtölur eftir**</span><span class="sxs-lookup"><span data-stu-id="062b6-189">**Filter totals by**</span></span>

  <span data-ttu-id="062b6-190">Sumar listar sem sýna reiknaðir reitir, svo sem upphæðir og fjölda, munu innihalda **Sía samtölur eftir** hlutann þar sem þú getur breytt ýmsum víddum sem hafa áhrif á útreikninga.</span><span class="sxs-lookup"><span data-stu-id="062b6-190">Some lists that display calculated fields, such as amounts and quantities, will include the **Filter totals by** section where you can adjust various dimensions that influence calculations.</span></span> <span data-ttu-id="062b6-191">Til að bæta við síu skal velja aðgerðina **+ Sía**.</span><span class="sxs-lookup"><span data-stu-id="062b6-191">To add a filter, choose the **+ Filter** action.</span></span> <span data-ttu-id="062b6-192">Til að bæta við síu skal slá inn heiti reitsins sem á að sía listann eftir eða velja reit af fellilistanum.</span><span class="sxs-lookup"><span data-stu-id="062b6-192">Then, type the name of the field that you want to filter the list by or pick a field from the drop-down list.</span></span>

  > [!NOTE]
  > <span data-ttu-id="062b6-193">Síur í **Sía samtölur eftir** hlutanum eru stjórnað af FlowFilters í síðuhönnuninni.</span><span class="sxs-lookup"><span data-stu-id="062b6-193">Filters in the **Filter totals by** section are controlled by FlowFilters on the page design.</span></span> <span data-ttu-id="062b6-194">Fyrir tæknilegar upplýsingar, sjá [FlowFilters](/dynamics365/business-central/dev-itpro/developer/devenv-flowfilter-overview).</span><span class="sxs-lookup"><span data-stu-id="062b6-194">For technical information, see [FlowFilters](/dynamics365/business-central/dev-itpro/developer/devenv-flowfilter-overview).</span></span>

<span data-ttu-id="062b6-195">Hægt er að stilla einfalda síu beint á lista innan með síusvæðinu, þ.e. síu sem sýnir aðeins færslur með sama gildi og í völdum reitum.</span><span class="sxs-lookup"><span data-stu-id="062b6-195">You can set a simple filter directly on a list within using the filter pane, namely a filter that displays only records with the same value as in the selected cell.</span></span> <span data-ttu-id="062b6-196">Velja skal hólf á listanum, velja felliörina og velja síðan aðgerðina **Afmarka í þetta gildi**.</span><span class="sxs-lookup"><span data-stu-id="062b6-196">Select a cell on the list, choose the drop-down arrow, and then choose the **Filter to This Value** action.</span></span> <span data-ttu-id="062b6-197">Að öðrum kosti er stutt á **ALT + F3**.</span><span class="sxs-lookup"><span data-stu-id="062b6-197">Alternatively, press **Alt+F3**.</span></span>

### <a name="setting-filters-in-reports-batch-jobs-and-xmlports"></a><span data-ttu-id="062b6-198">Afmarkanir stilltar í skýrslum, runuvinnslum og XMLports</span><span class="sxs-lookup"><span data-stu-id="062b6-198">Setting Filters in Reports, Batch Jobs, and XMLports</span></span>

<span data-ttu-id="062b6-199">Fyrir skýrslur og XMLports eru síurnar sýnilegar beint á beiðnisíðunni.</span><span class="sxs-lookup"><span data-stu-id="062b6-199">For reports and XMLports, the filters are visible directly on the request page.</span></span> <span data-ttu-id="062b6-200">Beiðnisíðan sýnir síðustu notuðu síur samkvæmt valinu í reitnum **Nota sjálfgildi úr**.</span><span class="sxs-lookup"><span data-stu-id="062b6-200">The request page displays the last used filters according to your selection in the **Use default values from** field.</span></span> <span data-ttu-id="062b6-201">Frekari upplýsingar eru í [Nota vistaðar stillingar](ui-work-report.md#SavedSettings).</span><span class="sxs-lookup"><span data-stu-id="062b6-201">For more information, see [Using Saved Settings](ui-work-report.md#SavedSettings).</span></span>

<span data-ttu-id="062b6-202">Helsti **Sía**-hlutinn sýnir sjálfgefna síureiti sem notaðir eru til að afmarka hvaða færslur á að taka með í skýrslu eða XMLport.</span><span class="sxs-lookup"><span data-stu-id="062b6-202">The main **Filter** section shows the default filter fields that you use to delimit which records to include in the report or XMLport.</span></span> <span data-ttu-id="062b6-203">Til að bæta við síu skal velja aðgerðina **+ Sía**.</span><span class="sxs-lookup"><span data-stu-id="062b6-203">To add a filter, choose the **+ Filter** action.</span></span> <span data-ttu-id="062b6-204">Svo skal færa inn heiti reitsins sem á að sía eftir eða velja reit af fellilistanum.</span><span class="sxs-lookup"><span data-stu-id="062b6-204">Then, type the name of the field that you want to filter by, or pick a field from the drop-down list.</span></span>

<span data-ttu-id="062b6-205">Í hlutanum **Afmarka samtölur eftir** er hægt að breyta ýmsum víddunum sem hafa áhrif á útreikninga í skýrslu eða XMLport.</span><span class="sxs-lookup"><span data-stu-id="062b6-205">In the **Filter totals by** section, you can adjust various dimensions that influence calculations in the report or XMLport.</span></span> <span data-ttu-id="062b6-206">Til að bæta við síu skal velja aðgerðina **+ Sía**.</span><span class="sxs-lookup"><span data-stu-id="062b6-206">To add a filter, choose the **+ Filter** action.</span></span> <span data-ttu-id="062b6-207">Svo skal færa inn heiti reitsins sem á að sía eftir eða velja reit af fellilistanum.</span><span class="sxs-lookup"><span data-stu-id="062b6-207">Then, type the name of the field that you want to filter by, or pick a field from the drop-down list.</span></span>

## <a name="entering-filter-criteria"></a><span data-ttu-id="062b6-208">Færa inn síuskilyrði</span><span class="sxs-lookup"><span data-stu-id="062b6-208">Entering Filter Criteria</span></span>

<span data-ttu-id="062b6-209">Bæði í síuglugganum og á beiðnisíðu er hægt að færa inn síuskilyrðin í reitinn undir síureitnum.</span><span class="sxs-lookup"><span data-stu-id="062b6-209">Both in the filter pane and on a request page, you enter your filter criteria in the box under the filter field.</span></span>

<span data-ttu-id="062b6-210">Gerð síureits ákvarðar hvaða skilyrði er hægt að færa inn.</span><span class="sxs-lookup"><span data-stu-id="062b6-210">The type of the filter field determines which criteria you can enter.</span></span> <span data-ttu-id="062b6-211">Til dæmis, að sía reit sem hefur fasta gildi mun einungis leyfa þér að velja úr þeim gildum.</span><span class="sxs-lookup"><span data-stu-id="062b6-211">For example, filtering a field that has fixed values will only let you choose from those values.</span></span> <span data-ttu-id="062b6-212">Nánari upplýsingar um sérstaka síu tákn sjá [Sía viðmiðanir](#FilterCriteria) og [Síumerki](#FilterTokens).</span><span class="sxs-lookup"><span data-stu-id="062b6-212">For more information about special filter symbols, see [Filter criteria](#FilterCriteria) and [Filter tokens](#FilterTokens).</span></span>

<span data-ttu-id="062b6-213">Dálkar sem þegar eru með síur eru auðkenndar með tákninu ![Síutákn](media/ui-search/filter-icon.png "Síutákn") í dálkhausnum.</span><span class="sxs-lookup"><span data-stu-id="062b6-213">Columns that already have filters are indicated by the ![Filter icon](media/ui-search/filter-icon.png "Filter icon") icon in the column heading.</span></span> <span data-ttu-id="062b6-214">Til að fjarlægja afmörkun skal velja felliörina og velja svo aðgerðina **Hreinsa afmörkun** .</span><span class="sxs-lookup"><span data-stu-id="062b6-214">To remove a filter, choose the drop-down arrow, and then choose the **Clear Filter** action.</span></span>

> [!TIP]
> <span data-ttu-id="062b6-215">Finna og greina gögnin þín fljótar með því að nota samsetningar flýtilykla.</span><span class="sxs-lookup"><span data-stu-id="062b6-215">Accelerate finding and analyzing your data by using combinations of keyboard shortcuts.</span></span> <span data-ttu-id="062b6-216">Til dæmis, veldu reit, notaðu **Shift + Alt + F3** til að bæta reitnum við síusvæðið, sláðu inn síuviðmiðin, notaðu **Ctrl + Enter** til að fara aftur í raðirnar, veldu annað reit og notaðu **Alt + F3** til að sía í það gildi.</span><span class="sxs-lookup"><span data-stu-id="062b6-216">For example, select a field, use **Shift+Alt+F3** to add that field to the filter pane, type the filter criteria, use **Ctrl+Enter** to return to the rows, select another field, and use **Alt+F3** to filter to that value.</span></span> <span data-ttu-id="062b6-217">Frekari upplýsingar, sjá [Flýtilyklar](keyboard-shortcuts.md#KeyboardFilter).</span><span class="sxs-lookup"><span data-stu-id="062b6-217">For more information, see [Keyboard Shortcuts](keyboard-shortcuts.md#KeyboardFilter).</span></span>

### <a name="filter-criteria-and-operators"></a><span data-ttu-id="062b6-218"><a name="FilterCriteria"> </a>Síuskilyrði og virkni</span><span class="sxs-lookup"><span data-stu-id="062b6-218"><a name="FilterCriteria"> </a>Filter Criteria and Operators</span></span>

<span data-ttu-id="062b6-219">Þegar skilyrði eru sett er hægt að nota alla sömu tölustafi og bókstafi sem venjulega eru notaðir í reitnum.</span><span class="sxs-lookup"><span data-stu-id="062b6-219">When you enter criteria, you can use all the numbers and letters that you normally use in the field.</span></span> <span data-ttu-id="062b6-220">En það eru líka til safn sértákna sem hægt er að nota sem virknitákn til að sía niðurstöður enn frekar.</span><span class="sxs-lookup"><span data-stu-id="062b6-220">But there's also a set of special symbols that you can use as operators to further filter the results.</span></span> <span data-ttu-id="062b6-221">Eftirfarandi hlutar útskýra þessi tákn og hvernig á að nota þau sem virknitákn í síum.</span><span class="sxs-lookup"><span data-stu-id="062b6-221">The following sections describe these symbols and how to use them as operators in filters.</span></span>

> [!TIP]
> <span data-ttu-id="062b6-222">Frekari upplýsingar um síun dagsetninga og tímasetninga er að finna í [Vinna með dagsetningar og tíma í dagatali](ui-enter-date-ranges.md).</span><span class="sxs-lookup"><span data-stu-id="062b6-222">For more information about filtering dates and times, see [Working with Calendar Dates and Times](ui-enter-date-ranges.md).</span></span>

> [!IMPORTANT]
> - <span data-ttu-id="062b6-223">Aðstæður kunna að koma upp þar sem gildið sem á að sía inniheldur tákn sem er virknitákn.</span><span class="sxs-lookup"><span data-stu-id="062b6-223">There may be situations where the value that you want to filter on contains a symbol that's an operator.</span></span> <span data-ttu-id="062b6-224">Frekari upplýsingar um hvað skuli gera í slíkum aðstæðum er að finna í [Gildi síuð sem innihalda tákn](#symbols) til að fá frekari leiðbeiningar um hvað skuli til bragðs taka í þessum aðstæðum.</span><span class="sxs-lookup"><span data-stu-id="062b6-224">For more information about handling these situtions, see [Filtering on Values That Contain Symbols](#symbols) for more instructions about handling this situation.</span></span>
>
> - <span data-ttu-id="062b6-225">Ef fleiri en 200 virknitákn eru til staðar í einni síu safnar kerfið sjálfkrafa saman sumum virknitáknum innan sviga `()` fyrir úrvinnsluna.</span><span class="sxs-lookup"><span data-stu-id="062b6-225">If there are more than 200 operators in a single filter, the system will automatically group some expressions in parentheses `()` for the purpose of processing.</span></span> <span data-ttu-id="062b6-226">Þetta hefur engin áhrif á síunina eða niðurstöðurnar.</span><span class="sxs-lookup"><span data-stu-id="062b6-226">This has no effect on the filter or the results.</span></span>  

#### <a name="-interval"></a><span data-ttu-id="062b6-227">(..) Bil</span><span class="sxs-lookup"><span data-stu-id="062b6-227">(..) Interval</span></span>

|<span data-ttu-id="062b6-228">Dæmi</span><span class="sxs-lookup"><span data-stu-id="062b6-228">Sample Expression</span></span>|<span data-ttu-id="062b6-229">Sýndar færslur</span><span class="sxs-lookup"><span data-stu-id="062b6-229">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`1100..2100`|<span data-ttu-id="062b6-230">Tölur 1100 til 2100.</span><span class="sxs-lookup"><span data-stu-id="062b6-230">Numbers 1100 through 2100</span></span>|  
|`..2500`|<span data-ttu-id="062b6-231">Reikningar til og með 2500</span><span class="sxs-lookup"><span data-stu-id="062b6-231">Up to and including 2500</span></span>|  
|`..12 31 00`|<span data-ttu-id="062b6-232">Dagsetningar til og með 31. 12. 00.</span><span class="sxs-lookup"><span data-stu-id="062b6-232">Dates up to and including 12 31 00</span></span>|  
|`P8..`|<span data-ttu-id="062b6-233">Upplýsingar um reikningstímabil 8 og eftir</span><span class="sxs-lookup"><span data-stu-id="062b6-233">Information for accounting period 8 and after</span></span>|  
|`..23`|<span data-ttu-id="062b6-234">Frá upphafsdegi til 23. þessa mánaðar – þessa árs 23:59:59</span><span class="sxs-lookup"><span data-stu-id="062b6-234">From the beginning date until 23-current month-current year 23:59:59</span></span>|  
|`23..`|<span data-ttu-id="062b6-235">Frá 23. þessa mánaðar – þessa árs 00:00:00 til loka tímans</span><span class="sxs-lookup"><span data-stu-id="062b6-235">From 23-current month-current year 0:00:00 until the end of time</span></span>|  
|`22..23`|<span data-ttu-id="062b6-236">Frá 22. þessa mánaðar – þessa árs 00:00:00 til 23. þessa mánaðar – þessa árs 23:59:59</span><span class="sxs-lookup"><span data-stu-id="062b6-236">From 22-current month-current year 0:00:00 until 23-current month-current year 23:59:59</span></span>|  

#### <a name="124-eitheror"></a><span data-ttu-id="062b6-237">(&#124;) Annaðhvort eða</span><span class="sxs-lookup"><span data-stu-id="062b6-237">(&#124;) Either/or</span></span>

|<span data-ttu-id="062b6-238">Dæmi</span><span class="sxs-lookup"><span data-stu-id="062b6-238">Sample Expression</span></span>|<span data-ttu-id="062b6-239">Sýndar færslur</span><span class="sxs-lookup"><span data-stu-id="062b6-239">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`1200|1300`|<span data-ttu-id="062b6-240">Tölur með 1200 eða 1300</span><span class="sxs-lookup"><span data-stu-id="062b6-240">Numbers with 1200 or 1300</span></span>|  

#### <a name="-not-equal-to"></a><span data-ttu-id="062b6-241">(<>) Ekki jafnt og</span><span class="sxs-lookup"><span data-stu-id="062b6-241">(<>) Not equal to</span></span>  

|<span data-ttu-id="062b6-242">Dæmi</span><span class="sxs-lookup"><span data-stu-id="062b6-242">Sample Expression</span></span>|<span data-ttu-id="062b6-243">Sýndar færslur</span><span class="sxs-lookup"><span data-stu-id="062b6-243">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`<>0`|<span data-ttu-id="062b6-244">Allar tölur aðrar en 0</span><span class="sxs-lookup"><span data-stu-id="062b6-244">All numbers except 0</span></span><br /><br /> <span data-ttu-id="062b6-245">Valkosturinn SQL Server býður upp á að sameina þetta tákn algildistákni.</span><span class="sxs-lookup"><span data-stu-id="062b6-245">The SQL Server Option allows you to combine this symbol with a wild-card expression.</span></span> <span data-ttu-id="062b6-246">Til dæmis merkir <>A\* ekki jafnt og neinn texti sem byrjar á stafnum A.</span><span class="sxs-lookup"><span data-stu-id="062b6-246">For example, <>A\* meaning not equal to any text that starts with A.</span></span>|  

#### <a name="-greater-than"></a><span data-ttu-id="062b6-247">(>) Meira en</span><span class="sxs-lookup"><span data-stu-id="062b6-247">(>) Greater than</span></span>  

|<span data-ttu-id="062b6-248">Dæmi</span><span class="sxs-lookup"><span data-stu-id="062b6-248">Sample Expression</span></span>|<span data-ttu-id="062b6-249">Sýndar færslur</span><span class="sxs-lookup"><span data-stu-id="062b6-249">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`>1200`|<span data-ttu-id="062b6-250">Tölur hærri en 1200</span><span class="sxs-lookup"><span data-stu-id="062b6-250">Numbers greater than 1200</span></span>|  

#### <a name="-greater-than-or-equal-to"></a><span data-ttu-id="062b6-251">(>=) Hærra en eða jafnt og</span><span class="sxs-lookup"><span data-stu-id="062b6-251">(>=) Greater than or equal to</span></span>  

|<span data-ttu-id="062b6-252">Dæmi</span><span class="sxs-lookup"><span data-stu-id="062b6-252">Sample Expression</span></span>|<span data-ttu-id="062b6-253">Sýndar færslur</span><span class="sxs-lookup"><span data-stu-id="062b6-253">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`>=1200`|<span data-ttu-id="062b6-254">Tölur hærri en eða jafnar 1200</span><span class="sxs-lookup"><span data-stu-id="062b6-254">Numbers greater than or equal to 1200</span></span>|  

#### <a name="-less-than"></a><span data-ttu-id="062b6-255">(<) Minna en</span><span class="sxs-lookup"><span data-stu-id="062b6-255">(<) Less than</span></span>  

|<span data-ttu-id="062b6-256">Dæmi</span><span class="sxs-lookup"><span data-stu-id="062b6-256">Sample Expression</span></span>|<span data-ttu-id="062b6-257">Sýndar færslur</span><span class="sxs-lookup"><span data-stu-id="062b6-257">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`<1200`|<span data-ttu-id="062b6-258">Tölur lægri en 1200</span><span class="sxs-lookup"><span data-stu-id="062b6-258">Numbers less than 1200</span></span>|  

#### <a name="-less-than-or-equal-to"></a><span data-ttu-id="062b6-259">(<=) Lægra en eða jafnt og</span><span class="sxs-lookup"><span data-stu-id="062b6-259">(<=) Less than or equal to</span></span>  

|<span data-ttu-id="062b6-260">Dæmi</span><span class="sxs-lookup"><span data-stu-id="062b6-260">Sample Expression</span></span>|<span data-ttu-id="062b6-261">Sýndar færslur</span><span class="sxs-lookup"><span data-stu-id="062b6-261">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`<=1200`|<span data-ttu-id="062b6-262">Tölur lægri en eða jafnar 1200</span><span class="sxs-lookup"><span data-stu-id="062b6-262">Numbers less than or equal to 1200</span></span>|  

#### <a name="-and"></a><span data-ttu-id="062b6-263">(&) Og</span><span class="sxs-lookup"><span data-stu-id="062b6-263">(&) And</span></span>  

|<span data-ttu-id="062b6-264">Dæmi</span><span class="sxs-lookup"><span data-stu-id="062b6-264">Sample Expression</span></span>|<span data-ttu-id="062b6-265">Sýndar færslur</span><span class="sxs-lookup"><span data-stu-id="062b6-265">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`>200&<1200`|<span data-ttu-id="062b6-266">Tölur hærri en 200 og minni en 1200</span><span class="sxs-lookup"><span data-stu-id="062b6-266">Numbers greater than 200 and less than 1200</span></span>|  

#### <a name="-an-exact-character-match"></a><span data-ttu-id="062b6-267">('') Nákvæm stafasamsvörun</span><span class="sxs-lookup"><span data-stu-id="062b6-267">('') An exact character match</span></span>  

|<span data-ttu-id="062b6-268">Dæmi</span><span class="sxs-lookup"><span data-stu-id="062b6-268">Sample Expression</span></span>|<span data-ttu-id="062b6-269">Sýndar færslur</span><span class="sxs-lookup"><span data-stu-id="062b6-269">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`'man'`|<span data-ttu-id="062b6-270">Texta sem passar nákvæmlega við **man** og er stafréttur.</span><span class="sxs-lookup"><span data-stu-id="062b6-270">Text that matches **man** exactly and is case-sensitive.</span></span>|  

#### <a name="-case-insensitive"></a><span data-ttu-id="062b6-271">(@) Stafrétt</span><span class="sxs-lookup"><span data-stu-id="062b6-271">(@) Case insensitive</span></span>  

|<span data-ttu-id="062b6-272">Dæmi</span><span class="sxs-lookup"><span data-stu-id="062b6-272">Sample Expression</span></span>|<span data-ttu-id="062b6-273">Sýndar færslur</span><span class="sxs-lookup"><span data-stu-id="062b6-273">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`@man*`|<span data-ttu-id="062b6-274">Texti sem byrjar á **man** og er ekki stafréttur.</span><span class="sxs-lookup"><span data-stu-id="062b6-274">Text that starts with **man** and is case insensitive.</span></span>|  

#### <a name="-an-indefinite-number-of-unknown-characters"></a><span data-ttu-id="062b6-275">(\*) Ótilgreindur fjöldi óþekktra staftákna</span><span class="sxs-lookup"><span data-stu-id="062b6-275">(\*) An indefinite number of unknown characters</span></span>

|<span data-ttu-id="062b6-276">Dæmi</span><span class="sxs-lookup"><span data-stu-id="062b6-276">Sample Expression</span></span>|<span data-ttu-id="062b6-277">Sýndar færslur</span><span class="sxs-lookup"><span data-stu-id="062b6-277">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`*Co*`|<span data-ttu-id="062b6-278">Texta sem inniheldur **Co** og er stafréttur.</span><span class="sxs-lookup"><span data-stu-id="062b6-278">Text that contains **Co** and is case-sensitive.</span></span>|  
|`*Co`|<span data-ttu-id="062b6-279">Texta sem endar á **Co** og er stafréttur.</span><span class="sxs-lookup"><span data-stu-id="062b6-279">Text that ends with **Co"** and is case-sensitive.</span></span>|  
|`Co*`|<span data-ttu-id="062b6-280">Texta sem byrjar á **Co** og er stafréttur.</span><span class="sxs-lookup"><span data-stu-id="062b6-280">Text that begins with **Co** and is case-sensitive.</span></span>|  

#### <a name="-one-unknown-character"></a><span data-ttu-id="062b6-281">(?) eitt óþekkt stafatákn</span><span class="sxs-lookup"><span data-stu-id="062b6-281">(?) One unknown character</span></span>  

|<span data-ttu-id="062b6-282">Dæmi</span><span class="sxs-lookup"><span data-stu-id="062b6-282">Sample Expression</span></span>|<span data-ttu-id="062b6-283">Sýndar færslur</span><span class="sxs-lookup"><span data-stu-id="062b6-283">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`Hans?n`|<span data-ttu-id="062b6-284">Texti eins og **Hansen** eða **Hanson**</span><span class="sxs-lookup"><span data-stu-id="062b6-284">Text such as **Hansen** or **Hanson**</span></span>|  

#### <a name="combined-format-expressions"></a><span data-ttu-id="062b6-285">Sameinað framsetningarsnið</span><span class="sxs-lookup"><span data-stu-id="062b6-285">Combined Format Expressions</span></span>  

|<span data-ttu-id="062b6-286">Dæmi</span><span class="sxs-lookup"><span data-stu-id="062b6-286">Sample Expression</span></span>|<span data-ttu-id="062b6-287">Sýndar færslur</span><span class="sxs-lookup"><span data-stu-id="062b6-287">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`5999|8100..8490`|<span data-ttu-id="062b6-288">Allar færslur með tölunni 5999 eða tölu á bilinu frá 8100 til og með 8490 er teknar með.</span><span class="sxs-lookup"><span data-stu-id="062b6-288">Include any records with the number 5999 or a number from the interval 8100 through 8490.</span></span>|  
|`..1299|1400..`|<span data-ttu-id="062b6-289">Telja með færslur með tölu sem er lægri eða jöfn 1299 eða tölu sem er jöfn 1400 eða hærri (allar tölur nema 1300 til 1399).</span><span class="sxs-lookup"><span data-stu-id="062b6-289">Include records with a number less than or equal to 1299 or a number equal to 1400 or greater (all numbers except 1300 through 1399).</span></span>|  
|`>50&<100`|<span data-ttu-id="062b6-290">Telja með færslur með tölum sem eru hærri en 50 og lægri en 100 (tölurnar 51 til 99).</span><span class="sxs-lookup"><span data-stu-id="062b6-290">Include records with numbers that are greater than 50 and less than 100 (numbers 51 through 99).</span></span>|  

### <a name="filtering-on-values-that-contain-symbols"></a><a name="symbols"></a><span data-ttu-id="062b6-291">Gildi síuð sem innihalda tákn</span><span class="sxs-lookup"><span data-stu-id="062b6-291">Filtering on Values That Contain Symbols</span></span>

<span data-ttu-id="062b6-292">Það gætu komið upp tilfelli þar sem reitargildi innihalda eitt af eftirfarandi táknum:</span><span class="sxs-lookup"><span data-stu-id="062b6-292">There may be cases where field values contain the one of the following symbols:</span></span>

- &
- <span data-ttu-id="062b6-293">(</span><span class="sxs-lookup"><span data-stu-id="062b6-293">(</span></span>
- <span data-ttu-id="062b6-294">)</span><span class="sxs-lookup"><span data-stu-id="062b6-294">)</span></span>
- =
- <span data-ttu-id="062b6-295">&#124;</span><span class="sxs-lookup"><span data-stu-id="062b6-295">&#124;</span></span>

<span data-ttu-id="062b6-296">Ef ætlunin er að sía eitt af þessum táknum skal hafa síusegðina innan gæsalappa.</span><span class="sxs-lookup"><span data-stu-id="062b6-296">If you want to filter on any of these symbols, place the filter expression in quotation marks ('').</span></span> <span data-ttu-id="062b6-297">Ef þú vilt til dæmis sía skrár sem hefjast á textanum *J & V*, þá yrði síusegðin `'J & V*'`.</span><span class="sxs-lookup"><span data-stu-id="062b6-297">For example, if you wanted to filter on records that start with the text *J & V*, the filter expression would be `'J & V*'`.</span></span>

<span data-ttu-id="062b6-298">Þetta skilyrði er ekki nauðsynlegt fyrir önnur tákn.</span><span class="sxs-lookup"><span data-stu-id="062b6-298">This requirement isn't necessary for other symbols.</span></span>

### <a name="filter-tokens"></a><span data-ttu-id="062b6-299"><a name="FilterTokens"> </a>Síumerki</span><span class="sxs-lookup"><span data-stu-id="062b6-299"><a name="FilterTokens"> </a>Filter Tokens</span></span>

<span data-ttu-id="062b6-300">Þegar þú slærð inn síuviðmiðanir getur þú einnig skrifað orð sem hafa sérstaka þýðingu, sem kallast síumerki.</span><span class="sxs-lookup"><span data-stu-id="062b6-300">When entering filter criteria, you can also type words that have special meaning, called filter tokens.</span></span> <span data-ttu-id="062b6-301">Eftir að hafa slegið inn merkiorðið, er orðinu skipt út fyrir gildin sem það táknar.</span><span class="sxs-lookup"><span data-stu-id="062b6-301">After entering the token word, the word is replaced by the value or values that it represents.</span></span> <span data-ttu-id="062b6-302">Síutákn gera síun auðveldari með því að draga úr þörfinni á að fara yfir á aðrar síðum til að fletta upp gildi sem þú vilt bæta við síuna.</span><span class="sxs-lookup"><span data-stu-id="062b6-302">Filter tokens make filtering easier by reducing the need to navigate to other pages to look up values you want to add to your filter.</span></span> <span data-ttu-id="062b6-303">Taflan hér fyrir neðan lýsir sumum merkjunum sem þú getur slegið inn sem síuviðmiðanir.</span><span class="sxs-lookup"><span data-stu-id="062b6-303">The tables below describe some of the tokens you can type as filter criteria.</span></span>

> [!TIP]
> <span data-ttu-id="062b6-304">Stofnunin þín getur notað sérsniðna merki.</span><span class="sxs-lookup"><span data-stu-id="062b6-304">Your organization may use custom tokens.</span></span> <span data-ttu-id="062b6-305">Til að læra um öll merkin sem þú hefur aðgang að eða til að bæta við fleiri sérsniðnum merkjum, skaltu tala við stjórnandann þinn.</span><span class="sxs-lookup"><span data-stu-id="062b6-305">To learn about the complete set of tokens available to you or to add more custom tokens, talk to your administrator.</span></span> <span data-ttu-id="062b6-306">Fyrir tæknilegar upplýsingar, sjá [Bæta við síumerkjum](/dynamics365/business-central/dev-itpro/developer/devenv-adding-filter-tokens).</span><span class="sxs-lookup"><span data-stu-id="062b6-306">For technical information see [Adding Filter Tokens](/dynamics365/business-central/dev-itpro/developer/devenv-adding-filter-tokens).</span></span>

#### <a name="me-or-userid-records-assigned-to-you"></a><span data-ttu-id="062b6-307">(%me eða %userid) Skrám úthlutað til þín</span><span class="sxs-lookup"><span data-stu-id="062b6-307">(%me or %userid) Records Assigned to You</span></span>

<span data-ttu-id="062b6-308">Notaðu `%me` eða `%userid` þegar verið er að sía reiti sem innihalda notandakenni, svo sem **úthlutað til notandakennis** reit, til að birta allar skrár sem eru úthlutað til þín.</span><span class="sxs-lookup"><span data-stu-id="062b6-308">Use `%me` or `%userid` when filtering fields that contain the user ID, such as **Assigned to User ID** field, to display all records that are assigned to you.</span></span>

|<span data-ttu-id="062b6-309">Dæmi</span><span class="sxs-lookup"><span data-stu-id="062b6-309">Sample Expression</span></span>|<span data-ttu-id="062b6-310">Sýndar færslur</span><span class="sxs-lookup"><span data-stu-id="062b6-310">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`%me`<br /><span data-ttu-id="062b6-311">eða</span><span class="sxs-lookup"><span data-stu-id="062b6-311">or</span></span><br />`%userid`|<span data-ttu-id="062b6-312">Skrár sem eru úthlutað á notandareikninginn þinn.</span><span class="sxs-lookup"><span data-stu-id="062b6-312">Records that are assigned to your user account.</span></span> |  

#### <a name="mycustomers-customers-in-my-customers"></a><span data-ttu-id="062b6-313">(%mycustomers) Viðskiptamenn í Mínir viðskiptamenn</span><span class="sxs-lookup"><span data-stu-id="062b6-313">(%mycustomers) Customers in My Customers</span></span>

<span data-ttu-id="062b6-314">Notaðu `%mycustomers` í **Nr** reitnum viðskiptamanns til að birta allar skrár fyrir viðskiptamenn sem eru innifaldir í **Mínir viðskiptamenn** listanum á Mitt hlutverk.</span><span class="sxs-lookup"><span data-stu-id="062b6-314">Use `%mycustomers` in the customer **No** field to display all records for customers that are included in the **My Customers** list on your Role Center.</span></span>

|<span data-ttu-id="062b6-315">Dæmi</span><span class="sxs-lookup"><span data-stu-id="062b6-315">Sample Expression</span></span>|<span data-ttu-id="062b6-316">Sýndar færslur</span><span class="sxs-lookup"><span data-stu-id="062b6-316">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`%mycustomers`|<span data-ttu-id="062b6-317">Viðskiptamenn í **Mínir viðskiptamenn** í Mitt hlutverk.</span><span class="sxs-lookup"><span data-stu-id="062b6-317">Customers in the **My Customers** on your Role Center.</span></span> |  

#### <a name="myitems-items-in-my-items"></a><span data-ttu-id="062b6-318">(%mytems) Atriði í Mínum atriðum</span><span class="sxs-lookup"><span data-stu-id="062b6-318">(%myitems) Items in My Items</span></span>

<span data-ttu-id="062b6-319">Notaðu `%myitems` Í atriði **Nr** reitinn til að birta allar skrár fyrir atriði sem eru innifalin í **Mín atriði** listanum í Mitt hlutverk.</span><span class="sxs-lookup"><span data-stu-id="062b6-319">Use `%myitems` in the item **No** field to display all records for items that are included in the **My Items** list on your Role Center.</span></span>

|<span data-ttu-id="062b6-320">Dæmi</span><span class="sxs-lookup"><span data-stu-id="062b6-320">Sample Expression</span></span>|<span data-ttu-id="062b6-321">Sýndar færslur</span><span class="sxs-lookup"><span data-stu-id="062b6-321">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`%myitems`|<span data-ttu-id="062b6-322">Atriði í **Mín atriði** í Mitt hlutverk.</span><span class="sxs-lookup"><span data-stu-id="062b6-322">Items in the **My Items** on your Role Center.</span></span> |  

#### <a name="myvendors-vendors-in-my-vendors"></a><span data-ttu-id="062b6-323">(%myvendors) Lánardrottnar í Mínir lánardrottnar</span><span class="sxs-lookup"><span data-stu-id="062b6-323">(%myvendors) Vendors in My Vendors</span></span>

<span data-ttu-id="062b6-324">Notaðu `%myvendors` í lánardrottinn **Nr** reitnum, til að birta allar skrá fyrir lánardrottna sem eru innifalin í **Mínir lánardrottnar** listanum í Mitt hlutverk.</span><span class="sxs-lookup"><span data-stu-id="062b6-324">Use `%myvendors` in the vendor **No** field to display all records for vendors that are included in the **My Vendors** list on your Role Center.</span></span>

|<span data-ttu-id="062b6-325">Dæmi</span><span class="sxs-lookup"><span data-stu-id="062b6-325">Sample Expression</span></span>|<span data-ttu-id="062b6-326">Sýndar færslur</span><span class="sxs-lookup"><span data-stu-id="062b6-326">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`%myvendors`|<span data-ttu-id="062b6-327">Lánardrottnar í **Mínir lánardrottnar** í Mitt hlutverk.</span><span class="sxs-lookup"><span data-stu-id="062b6-327">Vendors in the **My Vendors** on your Role Center.</span></span> |  

## <a name="see-also"></a><span data-ttu-id="062b6-328">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="062b6-328">See Also</span></span>

[<span data-ttu-id="062b6-329">Algengar spurningar um leit og síun</span><span class="sxs-lookup"><span data-stu-id="062b6-329">Searching and Filtering FAQ</span></span>](ui-search-filter-faq.md)  
[<span data-ttu-id="062b6-330">Vista og sérsníða listayfirlit</span><span class="sxs-lookup"><span data-stu-id="062b6-330">Save and Personalize List Views</span></span>](ui-views.md)  
<span data-ttu-id="062b6-331">[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="062b6-331">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  
