---
title: Röðun, leit og síun í listum | Microsoft Docs
description: Vinna á skilvirkan hátt í listum með því að leita yfir gögnin þín, flokka dálka og hreinsa niðurstöður með öflugum síutáknum og flýtivísum.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: delimit, FlowFilter, totals, limit, advanced
ms.date: 07/24/2020
ms.author: sgroespe
ms.openlocfilehash: 9bdaa604841156763739adf5411469c58a74eb1e
ms.sourcegitcommit: edad0d0b129e916c2cfdfa9c4f8d9d83513f4fd1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/24/2020
ms.locfileid: "3619432"
---
# <a name="sorting-searching-and-filtering"></a><span data-ttu-id="f6d0d-103">Röðun, leit og síun</span><span class="sxs-lookup"><span data-stu-id="f6d0d-103">Sorting, Searching, and Filtering</span></span>

<span data-ttu-id="f6d0d-104">Það eru nokkrir hlutir sem munu hjálpa þér að skanna, finna og takmarka skrár í lista, skýrslu eða XMLport.</span><span class="sxs-lookup"><span data-stu-id="f6d0d-104">There are a few things that you can do that will help you scan, find, and limit records on a list or in a report or XMLport.</span></span> <span data-ttu-id="f6d0d-105">Þar á meðal er röðun, leit og afmörkun.</span><span class="sxs-lookup"><span data-stu-id="f6d0d-105">These include sorting, searching, and filtering.</span></span> <span data-ttu-id="f6d0d-106">Þú getur notað suma eða alla þessa hluti samtímis til að finna eða greina gögnin þín fljótt.</span><span class="sxs-lookup"><span data-stu-id="f6d0d-106">You can apply some or all of these simultaneously to quickly find or analyze your data.</span></span>

<span data-ttu-id="f6d0d-107">Fyrir skýrslur og XMLport, líkt og í listum, er hægt að stilla síur til að afmarka hvaða gögn eigi að taka með í skýrslunni eða XMLport, en ekki er hægt að raða og leita.</span><span class="sxs-lookup"><span data-stu-id="f6d0d-107">For reports and XMLports, as on lists, you can set filters to delimit which data to include in the report or XMLport, but you cannot sort and search.</span></span>

> [!TIP]
> <span data-ttu-id="f6d0d-108">Þegar þú skoðar gögnin þín sem flísar getur þú leitað og notað grunn síun.</span><span class="sxs-lookup"><span data-stu-id="f6d0d-108">When viewing your data as tiles, you can search and use basic filtering.</span></span> <span data-ttu-id="f6d0d-109">Til að nota alla þessa öflugu eiginleika til að raða, leita og sía skaltu velja táknið ![Sýna sem lista](media/ui_show_as_list_icon.png "Sýna sem listaör til vinstri") til að sýna færslurnar sem lista.</span><span class="sxs-lookup"><span data-stu-id="f6d0d-109">To use the full set of powerful features for sorting, searching, and filtering, choose the ![Show as list](media/ui_show_as_list_icon.png "Show as list arrow left") icon to view the records as a list.</span></span>

<!--
When you want to search for data, such as customer names, addresses, or product groups, you enter criteria. In search criteria, you can use all the numbers and letters that you normally use in the specific field. In addition, you can use special symbols to further filter the results. There are two ways to search: using the Quick Filter or column filters.
-->

## <a name="sorting"></a><span data-ttu-id="f6d0d-110">Röðun</span><span class="sxs-lookup"><span data-stu-id="f6d0d-110">Sorting</span></span>

<span data-ttu-id="f6d0d-111">Með Röðun er auðvelt og fljótlegt að fá yfirsýn yfir gögnin.</span><span class="sxs-lookup"><span data-stu-id="f6d0d-111">Sorting makes it easy for you to get a quick overview of your data.</span></span> <span data-ttu-id="f6d0d-112">Ef þú ert með marga viðskiptamenn til dæmis, er hægt að velja að raða þeim eftir **númeri Viðskiptamanns**, **Bókunarflokkum viðskiptavinar**, **Gjaldmiðilskóði**, **LandsSvæðiskóða**, eða **skráningarnúmer Söluskatts** til að fá það yfirlit sem þú þarft.</span><span class="sxs-lookup"><span data-stu-id="f6d0d-112">If you have many customers, for example, you can choose to sort them by **Customer No.**, **Customer Posting Group**, **Currency Code**, **Country Region Code**, or **Sales Tax Registration No.** to get the overview you need.</span></span>

<span data-ttu-id="f6d0d-113">Til að raða á lista, geturðu annað hvort valið fyrirsagnatexta dálka til að skipta á milli hækkandi og lækkandi röðunar, eða valið felliörina í dálkafyrirsögninni, og síðan valið **Hækkandi** eða **Lækkandi**.</span><span class="sxs-lookup"><span data-stu-id="f6d0d-113">To sort a list, you can either choose a column heading text to toggle between ascending and descending order, or choose the drop-down arrow in the column heading, and then choose the **Ascending** or **Descending** action.</span></span>  

> [!NOTE]  
> <span data-ttu-id="f6d0d-114">Myndir, BLOB-reitir, FlowFilters og reitir sem tilheyra ekki töflu styðja ekki röðun.</span><span class="sxs-lookup"><span data-stu-id="f6d0d-114">Sorting is not supported on images, BLOB fields, FlowFilters, and fields that do not belong to a table.</span></span>  

## <a name="searching"></a><span data-ttu-id="f6d0d-115">Leit</span><span class="sxs-lookup"><span data-stu-id="f6d0d-115">Searching</span></span>

<!--## Searching by using the Quick Filter -->
<span data-ttu-id="f6d0d-116">Efst á sérhverri listasíðu er ![Leita í lista](media/ui-search/search-list.png "Tákn fyrir leitarlista")**Leita** aðgerðin sem býður upp á fljótlega og auðvelda leið til að vinna gögnin niður í lista og sýna einungis þær skrár sem innihalda gögnin sem þú vilt sjá.</span><span class="sxs-lookup"><span data-stu-id="f6d0d-116">At the top of each list page, there is a ![Search list](media/ui-search/search-list.png "Search list icon") **Search** action that provides a quick and easy way to reduce the records in a list and display only those records that contain the data that you are interested in seeing.</span></span>

<span data-ttu-id="f6d0d-117">Til að leita skaltu einfaldlega velja aðgerðina **Leita** og síðan skrifa í boxið textann sem þú ert að leita að.</span><span class="sxs-lookup"><span data-stu-id="f6d0d-117">To search, simply choose the **Search** action, and then in the box, type the text that you are looking for.</span></span> <span data-ttu-id="f6d0d-118">Þú getur slegið inn stafi, númer og önnur tákn.</span><span class="sxs-lookup"><span data-stu-id="f6d0d-118">You can enter letters, numbers, and other symbols.</span></span>

### <a name="fine-tuning-the-search"></a><span data-ttu-id="f6d0d-119">Fínstilla leitina</span><span class="sxs-lookup"><span data-stu-id="f6d0d-119">Fine-tuning the Search</span></span>

<span data-ttu-id="f6d0d-120">Almennt mun leit reyna að finna samsvarandi texta í öllum reitum.</span><span class="sxs-lookup"><span data-stu-id="f6d0d-120">In general, search will attempt to match text across all fields.</span></span> <span data-ttu-id="f6d0d-121">Leitin mun ekki gera greinarmun á hástöfum og lágstöfum (óháð há- og lágstöfum) og mun finna textasamsvörun hvar sem er í reitnum (fremst, aftast eða í miðjunni).</span><span class="sxs-lookup"><span data-stu-id="f6d0d-121">It does not distinguish between uppercase and lowercase characters (case insensitive) and will match text placed anywhere in the field, at the beginning, end, or in the middle.</span></span>

<span data-ttu-id="f6d0d-122">Hins vegar geturðu búið til nákvæmari leit með því að nota sértákn.</span><span class="sxs-lookup"><span data-stu-id="f6d0d-122">However, you can make a more exact search by using special characters.</span></span>

- <span data-ttu-id="f6d0d-123">Til að finna aðeins reitargildi sem samsvara öllum textanum og stöfunum, skal staðsetja textann á milli einfaldra gæsalappa `''` (til dæmis, `'man'`).</span><span class="sxs-lookup"><span data-stu-id="f6d0d-123">To find only field values that match the entire text and case exactly, place the search text between single quotes `''` (for example, `'man'`).</span></span>

- <span data-ttu-id="f6d0d-124">Til að finna reitargildi sem byrja á ákveðnum texta og samsvara stöfunum, skal setja `*` á eftir leitartextanum (til dæmis `man*`).</span><span class="sxs-lookup"><span data-stu-id="f6d0d-124">To find field values that start with a certain text and match the case, place `*` after the search text (for example `man*`).</span></span>

- <span data-ttu-id="f6d0d-125">Til að finna reitargildi sem enda á ákveðnum texta og samsvara stöfunum, skal setja `*` á undan leitartextanum (til dæmis `*man`).</span><span class="sxs-lookup"><span data-stu-id="f6d0d-125">To find field values that end with a certain text and match the case, place `*` before the search text (for example `*man`).</span></span>

- <span data-ttu-id="f6d0d-126">Þegar `''` eða `*` er notað er leitin háð há- og lágstöfum.</span><span class="sxs-lookup"><span data-stu-id="f6d0d-126">When using  `''` or `*`, the search is case sensitive.</span></span> <span data-ttu-id="f6d0d-127">Ef þú vilt gera leitina óháða há- og lágstöfum skaltu setja `@` á undan leitartextanum (til dæmis `@man*`).</span><span class="sxs-lookup"><span data-stu-id="f6d0d-127">If you want to make the search case insensitive, place `@` before the search text (for example `@man*`).</span></span>

<span data-ttu-id="f6d0d-128">Eftirfarandi tafla sýnir nokkur dæmi til að útskýra hvernig hægt er að nota leitina.</span><span class="sxs-lookup"><span data-stu-id="f6d0d-128">The following table provides some examples to explain how you can use the search.</span></span>

|<span data-ttu-id="f6d0d-129">Leitarskilyrði</span><span class="sxs-lookup"><span data-stu-id="f6d0d-129">Search Criteria</span></span>|<span data-ttu-id="f6d0d-130">Finnur ...</span><span class="sxs-lookup"><span data-stu-id="f6d0d-130">Finds...</span></span>|
|---------------|----------|
|`man`<br /><span data-ttu-id="f6d0d-131">eða</span><span class="sxs-lookup"><span data-stu-id="f6d0d-131">or</span></span> <br />`Man`|<span data-ttu-id="f6d0d-132">Allar skrár með reitum sem innihalda textann **man**, óháð því hvort notaðir eru há- eða lágstafir.</span><span class="sxs-lookup"><span data-stu-id="f6d0d-132">All records with fields that contain the text **man**, regardless of the case.</span></span> <span data-ttu-id="f6d0d-133">Til dæmis, **Manchester**, **manual**, eða **Sportsman**.</span><span class="sxs-lookup"><span data-stu-id="f6d0d-133">For example, **Manchester**, **manual**, or **Sportsman**.</span></span> |
|`'Man'`|<span data-ttu-id="f6d0d-134">Allar skrár með reitum sem innihalda aðeins **Man**, í samræmi við há- og lágstafi.</span><span class="sxs-lookup"><span data-stu-id="f6d0d-134">All records with fields that contain only **Man**, matching the case.</span></span>|
|`Man*`|<span data-ttu-id="f6d0d-135">Allar skrár með reitum sem byrja á textanum <b>Man</b>, í samræmi við há- og lágstafi.</span><span class="sxs-lookup"><span data-stu-id="f6d0d-135">All records with fields that start with the text <b>Man</b>, matching the case.</span></span> <span data-ttu-id="f6d0d-136">Til dæmis, **Manchester** en ekki **manual** eða **Sportsman** .</span><span class="sxs-lookup"><span data-stu-id="f6d0d-136">For example, **Manchester** but not **manual** or **Sportsman**.</span></span>|
|`@Man*`|<span data-ttu-id="f6d0d-137">Allar skrár með reitum sem byrja með **man**, óháð því hvort notaðir eru há- eða lágstafir.</span><span class="sxs-lookup"><span data-stu-id="f6d0d-137">All records with fields that start with **man**, regardless of the case.</span></span> <span data-ttu-id="f6d0d-138">Til dæmis, **Manchester** og **manual**, en ekki **Sportsman**.</span><span class="sxs-lookup"><span data-stu-id="f6d0d-138">For example, **Manchester** and **manual**, but not **Sportsman**.</span></span>|
|`@*man`|<span data-ttu-id="f6d0d-139">Allar skrár sem endar með **man**, óháð því hvort notaðir eru há- eða lágstafir.</span><span class="sxs-lookup"><span data-stu-id="f6d0d-139">All records that end with **man**, regardless of the case.</span></span> <span data-ttu-id="f6d0d-140">Til dæmis **Sportsman**, en ekki **Manchester** eða **manual**.</span><span class="sxs-lookup"><span data-stu-id="f6d0d-140">For example **Sportsman**, but not **Manchester** or **manual**.</span></span>|

> [!TIP]
> <span data-ttu-id="f6d0d-141">Þú getur ýtt á **F3** til að virkja og slökkva á leitarreitnum.</span><span class="sxs-lookup"><span data-stu-id="f6d0d-141">You can press **F3** to activate and deactivate the search box.</span></span> <span data-ttu-id="f6d0d-142">Frekari upplýsingar er að finna í [Flýtilyklar](keyboard-shortcuts.md#KeyboardFilter).</span><span class="sxs-lookup"><span data-stu-id="f6d0d-142">For more information see [Keyboard Shortcuts](keyboard-shortcuts.md#KeyboardFilter).</span></span>

> [!NOTE]  
> <span data-ttu-id="f6d0d-143">Leit mun ekki passa við gildi í myndum, BLOB-reitum, Flow-síum, FlowFields-reitum og öðrum reitum sem eru ekki hluti af töflu.</span><span class="sxs-lookup"><span data-stu-id="f6d0d-143">Search will not match values in images, BLOB fields, FlowFilters, FlowFields, and other fields that are not part of a table.</span></span>

## <a name="filtering"></a><a name="filtering"></a><span data-ttu-id="f6d0d-144">Afmörkun</span><span class="sxs-lookup"><span data-stu-id="f6d0d-144">Filtering</span></span>

<span data-ttu-id="f6d0d-145">Síun veitir háþróaðri og fjölhæfur leið til að stjórna hvaða skrár sem birtast á lista eða eru innifaldar í skýrslu eða XMLport.</span><span class="sxs-lookup"><span data-stu-id="f6d0d-145">Filtering provides a more advanced and versatile way of controlling which records display on a list or include in a report or XMLport.</span></span> <span data-ttu-id="f6d0d-146">Það eru tvær helstu munur á leit og síun, eins og lýst er í töflunni hér að neðan.</span><span class="sxs-lookup"><span data-stu-id="f6d0d-146">There are two major differences between searching and filtering, as described in the table below.</span></span>

|| <span data-ttu-id="f6d0d-147">**Leit**</span><span class="sxs-lookup"><span data-stu-id="f6d0d-147">**Searching**</span></span> | <span data-ttu-id="f6d0d-148">**Afmörkun**</span><span class="sxs-lookup"><span data-stu-id="f6d0d-148">**Filtering**</span></span> |
|--|----------|------------|
| <span data-ttu-id="f6d0d-149">**Reitir sem gilda**</span><span class="sxs-lookup"><span data-stu-id="f6d0d-149">**Applicable Fields**</span></span> | <span data-ttu-id="f6d0d-150">Leitar yfir alla reitum sem eru sýnilegar á síðunni.</span><span class="sxs-lookup"><span data-stu-id="f6d0d-150">Searches across all fields that are visible on the page.</span></span> | <span data-ttu-id="f6d0d-151">Síar einn eða fleiri reiti, hvern fyrir sig, og velur úr öllum reitum í töflunni, þar á meðal reiti sem eru ekki sýnilegar á síðunni.</span><span class="sxs-lookup"><span data-stu-id="f6d0d-151">Filters one or more fields individually, selecting from any field on the table, including fields that are not visible on the page.</span></span> |
| <span data-ttu-id="f6d0d-152">**Samsvörun**</span><span class="sxs-lookup"><span data-stu-id="f6d0d-152">**Matching**</span></span> | <span data-ttu-id="f6d0d-153">Sýnir skrár með reitum sem passa við leitartexta, óháð notkun há- og lágstafa, eða staðsetningu þess texta.</span><span class="sxs-lookup"><span data-stu-id="f6d0d-153">Displays records with fields that match the search text, irrespective of casing or placement of that text.</span></span> | <span data-ttu-id="f6d0d-154">Sýnir skrár þar sem reiturinn passar nákvæmlega við síuna og gerir greinarmun á há- og lágstöfum, nema sérstakar síu tákn séu slegin inn.</span><span class="sxs-lookup"><span data-stu-id="f6d0d-154">Displays records where the field matches the filter exactly and is case sensitive, unless special filter symbols are entered.</span></span>

<span data-ttu-id="f6d0d-155">Síun gerir þér kleift að birta skrár fyrir tiltekna reikninga eða viðskiptamenn, dagsetningar, upphæð og aðrar upplýsingar með því að tilgreina síuviðmiðanir.</span><span class="sxs-lookup"><span data-stu-id="f6d0d-155">Filtering enables you to display records for specific accounts or customers, dates, amounts, and other information by specifying filter criteria.</span></span> <span data-ttu-id="f6d0d-156">Aðeins færslur sem samsvara skilyrðunum eru birtar á listanum eða teknar með í skýrslugerð, runuvinnslu eða XMLport.</span><span class="sxs-lookup"><span data-stu-id="f6d0d-156">Only records that match the criteria are displayed on the list or included in the report, batch job, or XMLport.</span></span> <span data-ttu-id="f6d0d-157">Ef þú tilgreinir skilyrði fyrir marga reiti, þá birtast aðeins skrár sem passa við öll skilyrði.</span><span class="sxs-lookup"><span data-stu-id="f6d0d-157">If you specify criteria for multiple fields, then only records that match all criteria will be displayed.</span></span>

<span data-ttu-id="f6d0d-158">Fyrir lista eru síurnar sýndar á afmörkunarsvæði sem birtist til vinstri á listanum þegar það er virkjað.</span><span class="sxs-lookup"><span data-stu-id="f6d0d-158">For lists, the filters are displayed on a filter pane that appears to the left of the list when you activate it.</span></span> <span data-ttu-id="f6d0d-159">Fyrir skýrslur, runuvinnslur og XMLport eru síurnar sýnilegar beint á beiðnisíðunni.</span><span class="sxs-lookup"><span data-stu-id="f6d0d-159">For reports, batch jobs, and XMLports, the filters are visible directly on the request page.</span></span>

### <a name="filtering-with-option-fields"></a><span data-ttu-id="f6d0d-160">Sía með valsvæðum</span><span class="sxs-lookup"><span data-stu-id="f6d0d-160">Filtering with Option Fields</span></span>

<span data-ttu-id="f6d0d-161">Fyrir „venjulega“ reiti sem innihalda gögn, uppsetningardagsetningu eða viðskiptagögn er hægt að stilla síur bæði með því að velja gögn og með því að slá inn síugildi og hægt er að nota tákn til að skilgreina ítarleg síuskilyrði.</span><span class="sxs-lookup"><span data-stu-id="f6d0d-161">For "ordinary" fields that hold data, setup date or business data, you can set filters both by selecting data and by typing filter values, and you can use symbols to define advanced filter criteria.</span></span> <span data-ttu-id="f6d0d-162">Nánari upplýsingar eru í [Færa inn síuskilyrði](ui-enter-criteria-filters.md#entering-filter-criteria).</span><span class="sxs-lookup"><span data-stu-id="f6d0d-162">For more information, see [Entering Filter Criteria](ui-enter-criteria-filters.md#entering-filter-criteria).</span></span>

<span data-ttu-id="f6d0d-163">Fyrir reiti af gerðinni **Valkostir** er hins vegar aðeins hægt að stilla síu með því að velja einn eða fleiri valkosti úr fellilista með tiltækum valkostum.</span><span class="sxs-lookup"><span data-stu-id="f6d0d-163">For fields of type **Option**, however, you can only set a filter by selecting one or more options from a drop-down list of the available options.</span></span> <span data-ttu-id="f6d0d-164">Dæmi um valkostsreit er reiturinn **Staða** á síðunni **Sölupantanir**.</span><span class="sxs-lookup"><span data-stu-id="f6d0d-164">An example of an option field is the **Status** field on the **Sales Orders** page.</span></span>

> [!NOTE]
> <span data-ttu-id="f6d0d-165">Þegar margir valkostir eru valdir sem síugildi er venslin á milli valkostanna skilgreind sem *EÐA*.</span><span class="sxs-lookup"><span data-stu-id="f6d0d-165">When you select multiple options as a filter value, the relationship between the options is defined as *OR*.</span></span> <span data-ttu-id="f6d0d-166">Til dæmis, ef þú velur báða gátreitina **Opið** og **Losað** á afmörkunarsvæðinu **Staða** á síðunni **Sölupantanir**, þýðir það að sölupantanir sem eru annaðhvort opnar eða losaðar eru birtar.</span><span class="sxs-lookup"><span data-stu-id="f6d0d-166">For example, if you select both the **Open** and the **Released** check box in the **Status** filter field on the **Sales Orders** page, it means that sales orders that are either open or released are displayed.</span></span>

### <a name="setting-filters-on-lists"></a><span data-ttu-id="f6d0d-167">Afmarkanir stilltar á lista</span><span class="sxs-lookup"><span data-stu-id="f6d0d-167">Setting Filters on Lists</span></span>

<span data-ttu-id="f6d0d-168">Á listum eru síur stilltar með því að nota afmörkunarsvæði.</span><span class="sxs-lookup"><span data-stu-id="f6d0d-168">On lists, you set filters by using the filter pane.</span></span> <span data-ttu-id="f6d0d-169">Til að birta afmörkunarsvæðið fyrir lista skal velja felliörina við hliðina á heiti síðunnar og velja síðan **Sýna afmörkunarsvæði**.</span><span class="sxs-lookup"><span data-stu-id="f6d0d-169">To display the filter pane for a list, choose the drop-down arrow next to the name of the page, and then choose the **Show filter pane** action.</span></span> <span data-ttu-id="f6d0d-170">Að öðrum kosti er stutt á **Shift+F3**.</span><span class="sxs-lookup"><span data-stu-id="f6d0d-170">Alternatively, press **Shift+F3**.</span></span>

<span data-ttu-id="f6d0d-171">Til að birta afmörkunarsvæðið fyrir dálk á lista skal velja felliörina og velja síðan aðgerðina **Afmörkun**.</span><span class="sxs-lookup"><span data-stu-id="f6d0d-171">To display the filter pane for a column on a list, choose the drop-down arrow, and then choose the **Filter** action.</span></span> <span data-ttu-id="f6d0d-172">Að öðrum kosti er stutt á **Shift+F3**.</span><span class="sxs-lookup"><span data-stu-id="f6d0d-172">Alternatively, press **Shift+F3**.</span></span> <span data-ttu-id="f6d0d-173">Afmörkunarsvæðið opnast með völdum dálki sem sýndur er sem afmörkunarsvæðið í hlutanum **Afmarka lista**.</span><span class="sxs-lookup"><span data-stu-id="f6d0d-173">The filter pane opens with the selected column shown as a filter field in the **Filter list by** section.</span></span>

<span data-ttu-id="f6d0d-174">Síusvæðið sýnir núverandi síur fyrir lista og gerir þér kleift að stilla eigin sérsniðna síur í einu eða fleiri reitum með því að velja aðgerðina **+ Sía**.</span><span class="sxs-lookup"><span data-stu-id="f6d0d-174">The filter pane displays the current filters for a list, and enables you to set your own custom filters on one or more fields by choosing the **+ Filter** action.</span></span>

 <span data-ttu-id="f6d0d-175">Síusvæði er skipt í þrjá hluta: **Skoðanir**, **Sía listi eftir** og **Sía samtölur eftir**:</span><span class="sxs-lookup"><span data-stu-id="f6d0d-175">A filter pane is divided in three sections: **Views**, **Filter list by**, and **Filter totals by**:</span></span>

- <span data-ttu-id="f6d0d-176">**Yfirlit**</span><span class="sxs-lookup"><span data-stu-id="f6d0d-176">**Views**</span></span>

  <span data-ttu-id="f6d0d-177">Sumir listar hafa hlutann **Yfirlit** með.</span><span class="sxs-lookup"><span data-stu-id="f6d0d-177">Some lists include the **Views** section.</span></span> <span data-ttu-id="f6d0d-178">Skoðanir eru afbrigði af listanum sem hefur verið forstillt með síum.</span><span class="sxs-lookup"><span data-stu-id="f6d0d-178">Views are variations of the list that have been preconfigured with filters.</span></span> <span data-ttu-id="f6d0d-179">Þú getur skilgreint og vistað eins mörg yfirlit og þú vilt fyrir hvern lista, og yfirlitin verða aðgengilegt í öllum tækjum sem þú skráir þig inn á.</span><span class="sxs-lookup"><span data-stu-id="f6d0d-179">You can define and save as many views as you want per list, and the views will be available to you on any device you sign into.</span></span> <span data-ttu-id="f6d0d-180">Frekari upplýsingar er að finna á [Vista og sérsníða listayfirlit](ui-views.md).</span><span class="sxs-lookup"><span data-stu-id="f6d0d-180">For more information, see [Save and Personalize List Views](ui-views.md).</span></span>

- <span data-ttu-id="f6d0d-181">**Sía listi eftir**</span><span class="sxs-lookup"><span data-stu-id="f6d0d-181">**Filter list by**</span></span>

  <span data-ttu-id="f6d0d-182">Þetta er hlutinn er þar sem þú bætir við síum á tilteknum reitum til að draga úr fjölda birtra skráa.</span><span class="sxs-lookup"><span data-stu-id="f6d0d-182">This is where you add filters on specific fields to reduce the number of displayed records.</span></span> <span data-ttu-id="f6d0d-183">Til að bæta við síu skal velja aðgerðina **+ Sía** , færa inn heiti reitsins sem á að sía listann eftir eða velja reit af fellilistanum.</span><span class="sxs-lookup"><span data-stu-id="f6d0d-183">To add a filter, choose the **+ Filter** action, type the name of the field that you want to filter the list by, or pick a field from the drop-down list.</span></span>

- <span data-ttu-id="f6d0d-184">**Sía samtölur eftir**</span><span class="sxs-lookup"><span data-stu-id="f6d0d-184">**Filter totals by**</span></span>

  <span data-ttu-id="f6d0d-185">Sumar listar sem sýna reiknaðir reitir, svo sem upphæðir og fjölda, munu innihalda **Sía samtölur eftir** hlutann þar sem þú getur breytt ýmsum víddum sem hafa áhrif á útreikninga.</span><span class="sxs-lookup"><span data-stu-id="f6d0d-185">Some lists that display calculated fields, such as amounts and quantities, will include the **Filter totals by** section where you can adjust various dimensions that influence calculations.</span></span> <span data-ttu-id="f6d0d-186">Til að bæta við síu skal velja aðgerðina **+ Sía** , færa inn heiti reitsins sem á að sía listann eftir eða velja reit af fellilistanum.</span><span class="sxs-lookup"><span data-stu-id="f6d0d-186">To add a filter, choose the **+ Filter** action, type the name of the field that you want to filter the list by, or pick a field from the drop-down list.</span></span>

  > [!NOTE]
  > <span data-ttu-id="f6d0d-187">Síur í **Sía samtölur eftir** hlutanum eru stjórnað af FlowFilters í síðuhönnuninni.</span><span class="sxs-lookup"><span data-stu-id="f6d0d-187">Filters in the **Filter totals by** section are controlled by FlowFilters on the page design.</span></span> <span data-ttu-id="f6d0d-188">Fyrir tæknilegar upplýsingar, sjá [FlowFilters](/dynamics365/business-central/dev-itpro/developer/devenv-flowfilter-overview).</span><span class="sxs-lookup"><span data-stu-id="f6d0d-188">For technical information, see [FlowFilters](/dynamics365/business-central/dev-itpro/developer/devenv-flowfilter-overview).</span></span>

<span data-ttu-id="f6d0d-189">Hægt er að stilla einfalda síu beint á lista innan með síusvæðinu, þ.e. síu sem sýnir aðeins færslur með sama gildi og í völdum reitum.</span><span class="sxs-lookup"><span data-stu-id="f6d0d-189">You can set a simple filter directly on a list within using the filter pane, namely a filter that displays only records with the same value as in the selected cell.</span></span> <span data-ttu-id="f6d0d-190">Velja skal hólf á listanum, velja felliörina og velja síðan aðgerðina **Afmarka í þetta gildi**.</span><span class="sxs-lookup"><span data-stu-id="f6d0d-190">Select a cell on the list, choose the drop-down arrow, and then choose the **Filter to This Value** action.</span></span> <span data-ttu-id="f6d0d-191">Að öðrum kosti er stutt á **ALT + F3**.</span><span class="sxs-lookup"><span data-stu-id="f6d0d-191">Alternatively, press **Alt+F3**.</span></span>

### <a name="setting-filters-in-reports-batch-jobs-and-xmlports"></a><span data-ttu-id="f6d0d-192">Afmarkanir stilltar í skýrslum, runuvinnslum og XMLports</span><span class="sxs-lookup"><span data-stu-id="f6d0d-192">Setting Filters in Reports, Batch Jobs, and XMLports</span></span>

<span data-ttu-id="f6d0d-193">Fyrir skýrslur og XMLports eru síurnar sýnilegar beint á beiðnisíðunni.</span><span class="sxs-lookup"><span data-stu-id="f6d0d-193">For reports and XMLports, the filters are visible directly on the request page.</span></span> <span data-ttu-id="f6d0d-194">Beiðnisíðan sýnir síðustu notuðu síur samkvæmt valinu í reitnum **Nota sjálfgildi úr**.</span><span class="sxs-lookup"><span data-stu-id="f6d0d-194">The request page displays the last used filters according to your selection in the **Use default values from** field.</span></span> <span data-ttu-id="f6d0d-195">Frekari upplýsingar eru í [Nota vistaðar stillingar](ui-work-report.md#SavedSettings).</span><span class="sxs-lookup"><span data-stu-id="f6d0d-195">For more information, see [Using Saved Settings](ui-work-report.md#SavedSettings).</span></span>

<span data-ttu-id="f6d0d-196">Helsti **Sía**-hlutinn sýnir sjálfgefna síureiti sem notaðir eru til að afmarka hvaða færslur á að taka með í skýrslu eða XMLport.</span><span class="sxs-lookup"><span data-stu-id="f6d0d-196">The main **Filter** section shows the default filter fields that you use to delimit which records to include in the report or XMLport.</span></span> <span data-ttu-id="f6d0d-197">Til að bæta við síu skal velja aðgerðina **+ Sía** , færa inn heiti reitsins sem á að sía eftir eða velja reit af fellilistanum.</span><span class="sxs-lookup"><span data-stu-id="f6d0d-197">To add a filter, choose the **+ Filter** action, type the name of the field that you want to filter by, or pick a field from the drop-down list.</span></span>

<span data-ttu-id="f6d0d-198">Í hlutanum **Afmarka samtölur eftir** er hægt að breyta ýmsum víddunum sem hafa áhrif á útreikninga í skýrslu eða XMLport.</span><span class="sxs-lookup"><span data-stu-id="f6d0d-198">In the **Filter totals by** section, you can adjust various dimensions that influence calculations in the report or XMLport.</span></span> <span data-ttu-id="f6d0d-199">Til að bæta við síu skal velja aðgerðina **+ Sía** , færa inn heiti reitsins sem á að sía eftir eða velja reit af fellilistanum.</span><span class="sxs-lookup"><span data-stu-id="f6d0d-199">To add a filter, choose the **+ Filter** action, type the name of the field that you want to filter by, or pick a field from the drop-down list.</span></span>

## <a name="entering-filter-criteria"></a><span data-ttu-id="f6d0d-200">Færa inn síuskilyrði</span><span class="sxs-lookup"><span data-stu-id="f6d0d-200">Entering Filter Criteria</span></span>

<span data-ttu-id="f6d0d-201">Bæði í síuglugganum og á beiðnisíðu er hægt að færa inn síuskilyrðin í reitinn undir síureitnum.</span><span class="sxs-lookup"><span data-stu-id="f6d0d-201">Both in the filter pane and on a request page, you enter your filter criteria in the box under the filter field.</span></span>

<span data-ttu-id="f6d0d-202">Gerð síureits ákvarðar hvaða skilyrði er hægt að færa inn.</span><span class="sxs-lookup"><span data-stu-id="f6d0d-202">The type of the filter field determines which criteria you can enter.</span></span> <span data-ttu-id="f6d0d-203">Til dæmis, að sía reit sem hefur fasta gildi mun einungis leyfa þér að velja úr þeim gildum.</span><span class="sxs-lookup"><span data-stu-id="f6d0d-203">For example, filtering a field that has fixed values will only let you choose from those values.</span></span> <span data-ttu-id="f6d0d-204">Nánari upplýsingar um sérstaka síu tákn sjá [Sía viðmiðanir](#FilterCriteria) og [Síumerki](#FilterTokens).</span><span class="sxs-lookup"><span data-stu-id="f6d0d-204">For more information about special filter symbols, see [Filter criteria](#FilterCriteria) and [Filter tokens](#FilterTokens).</span></span>

<span data-ttu-id="f6d0d-205">Dálkar sem þegar eru með síur eru auðkenndar með tákninu ![Síutákn](media/ui-search/filter-icon.png "Síutákn") í dálkhausnum.</span><span class="sxs-lookup"><span data-stu-id="f6d0d-205">Columns that already have filters are indicated by the ![Filter icon](media/ui-search/filter-icon.png "Filter icon") icon in the column heading.</span></span> <span data-ttu-id="f6d0d-206">Til að fjarlægja afmörkun skal velja felliörina og velja svo aðgerðina **Hreinsa afmörkun** .</span><span class="sxs-lookup"><span data-stu-id="f6d0d-206">To remove a filter, choose the drop-down arrow, and then choose the **Clear Filter** action.</span></span>

> [!TIP]
> <span data-ttu-id="f6d0d-207">Finna og greina gögnin þín fljótar með því að nota samsetningar flýtilykla.</span><span class="sxs-lookup"><span data-stu-id="f6d0d-207">Accelerate finding and analyzing your data by using combinations of keyboard shortcuts.</span></span> <span data-ttu-id="f6d0d-208">Til dæmis, veldu reit, notaðu **Shift + Alt + F3** til að bæta reitnum við síusvæðið, sláðu inn síuviðmiðin, notaðu **Ctrl + Enter** til að fara aftur í raðirnar, veldu annað reit og notaðu **Alt + F3** til að sía í það gildi.</span><span class="sxs-lookup"><span data-stu-id="f6d0d-208">For example, select a field, use **Shift+Alt+F3** to add that field to the filter pane, type the filter criteria, use **Ctrl+Enter** to return to the rows, select another field, and use **Alt+F3** to filter to that value.</span></span> <span data-ttu-id="f6d0d-209">Frekari upplýsingar er að finna í [Flýtilyklar](keyboard-shortcuts.md#KeyboardFilter).</span><span class="sxs-lookup"><span data-stu-id="f6d0d-209">For more information see [Keyboard Shortcuts](keyboard-shortcuts.md#KeyboardFilter).</span></span>

### <a name="filter-criteria-and-symbols"></a><span data-ttu-id="f6d0d-210"><a name="FilterCriteria"> </a>Síuskilyrði og tákn</span><span class="sxs-lookup"><span data-stu-id="f6d0d-210"><a name="FilterCriteria"> </a>Filter Criteria and Symbols</span></span>

<span data-ttu-id="f6d0d-211">Þegar skilyrði eru sett er hægt að nota alla sömu tölustafi og bókstafi sem venjulega eru notaðir í reitnum.</span><span class="sxs-lookup"><span data-stu-id="f6d0d-211">When you enter criteria, you can use all the numbers and letters that you can normally use in the field.</span></span> <span data-ttu-id="f6d0d-212">Ennfremur er hægt að nota sértákn (eða virknitákn) til að afmarka niðurstöðurnar enn frekar.</span><span class="sxs-lookup"><span data-stu-id="f6d0d-212">In addition, you can use special symbols (or operators) to further filter the results.</span></span> <span data-ttu-id="f6d0d-213">Í eftirfarandi töflum eru táknin sem hægt er að nota í síum.</span><span class="sxs-lookup"><span data-stu-id="f6d0d-213">The following tables show the symbols that can be used in filters.</span></span> <span data-ttu-id="f6d0d-214">Fyrir dagsetningar og tíma er einnig hægt að vísa til [Vinna með dagsetningar og tíma í dagatali](ui-enter-date-ranges.md) til að fá nánari upplýsingar.</span><span class="sxs-lookup"><span data-stu-id="f6d0d-214">For dates and times, you can also refer to [Working with Calendar Dates and Times](ui-enter-date-ranges.md) for more detailed information.</span></span>

> [!IMPORTANT]  
> <span data-ttu-id="f6d0d-215">Það geta verið tilvik þar sem gildi reita innihalda þessi tákn og þú vilt setja afmörkun á þau.</span><span class="sxs-lookup"><span data-stu-id="f6d0d-215">There may be instances where field values contain these symbols and you want to filter on them.</span></span> <span data-ttu-id="f6d0d-216">Til að gera það, verðurðu að hafa með afmörkunarsegðina sem inniheldur táknið með gæsalöppum („“).</span><span class="sxs-lookup"><span data-stu-id="f6d0d-216">To do this, you must include the filter expression that contains the symbol in quotation marks ('').</span></span> <span data-ttu-id="f6d0d-217">Til dæmis, ef þú vilt sía á færslum sem byrja á textanum *S&R*, er síusegðin `'S&R*'`.</span><span class="sxs-lookup"><span data-stu-id="f6d0d-217">For example, if you want to filter on records that start with the text *S&R*, the filter expression is `'S&R*'`.</span></span>

<span data-ttu-id="f6d0d-218">Eftirfarandi hlutar útskýra hvernig á að nota mismunandi virknitákn.</span><span class="sxs-lookup"><span data-stu-id="f6d0d-218">The following sections describe how to use the different operators.</span></span>

> [!NOTE]
> <span data-ttu-id="f6d0d-219">Ef fleiri en 200 virknitákn eru til staðar í einni síu safnar kerfið sjálfkrafa saman sumum virknitáknum innan sviga `()` fyrir úrvinnsluna.</span><span class="sxs-lookup"><span data-stu-id="f6d0d-219">If there are more than 200 operators in a single filter, the system will automatically group some expressions in parentheses `()` for the purpose of processing.</span></span> <span data-ttu-id="f6d0d-220">Þetta hefur engin áhrif á síunina eða niðurstöðurnar.</span><span class="sxs-lookup"><span data-stu-id="f6d0d-220">This has no effect on the filter or the results.</span></span>  

#### <a name="-interval"></a><span data-ttu-id="f6d0d-221">(..) Bil</span><span class="sxs-lookup"><span data-stu-id="f6d0d-221">(..) Interval</span></span>

|<span data-ttu-id="f6d0d-222">Dæmi</span><span class="sxs-lookup"><span data-stu-id="f6d0d-222">Sample Expression</span></span>|<span data-ttu-id="f6d0d-223">Sýndar færslur</span><span class="sxs-lookup"><span data-stu-id="f6d0d-223">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`1100..2100`|<span data-ttu-id="f6d0d-224">Tölur 1100 til 2100.</span><span class="sxs-lookup"><span data-stu-id="f6d0d-224">Numbers 1100 through 2100</span></span>|  
|`..2500`|<span data-ttu-id="f6d0d-225">Reikningar til og með 2500</span><span class="sxs-lookup"><span data-stu-id="f6d0d-225">Up to and including 2500</span></span>|  
|`..12 31 00`|<span data-ttu-id="f6d0d-226">Dagsetningar til og með 31. 12. 00.</span><span class="sxs-lookup"><span data-stu-id="f6d0d-226">Dates up to and including 12 31 00</span></span>|  
|`P8..`|<span data-ttu-id="f6d0d-227">Upplýsingar um reikningstímabil 8 og síðar.</span><span class="sxs-lookup"><span data-stu-id="f6d0d-227">Information for accounting period 8 and thereafter</span></span>|  
|`..23`|<span data-ttu-id="f6d0d-228">Frá upphafsdegi til 23. þessa mánaðar – þessa árs 23:59:59</span><span class="sxs-lookup"><span data-stu-id="f6d0d-228">From the beginning date until 23-current month-current year 23:59:59</span></span>|  
|`23..`|<span data-ttu-id="f6d0d-229">Frá 23. þessa mánaðar – þessa árs 00:00:00 til loka tímans</span><span class="sxs-lookup"><span data-stu-id="f6d0d-229">From 23-current month-current year 0:00:00 until the end of time</span></span>|  
|`22..23`|<span data-ttu-id="f6d0d-230">Frá 22. þessa mánaðar – þessa árs 00:00:00 til 23. þessa mánaðar – þessa árs 23:59:59</span><span class="sxs-lookup"><span data-stu-id="f6d0d-230">From 22-current month-current year 0:00:00 until 23-current month-current year 23:59:59</span></span>|  

#### <a name="124-eitheror"></a><span data-ttu-id="f6d0d-231">(&#124;) Annaðhvort eða</span><span class="sxs-lookup"><span data-stu-id="f6d0d-231">(&#124;) Either/or</span></span>

|<span data-ttu-id="f6d0d-232">Dæmi</span><span class="sxs-lookup"><span data-stu-id="f6d0d-232">Sample Expression</span></span>|<span data-ttu-id="f6d0d-233">Sýndar færslur</span><span class="sxs-lookup"><span data-stu-id="f6d0d-233">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`1200|1300`|<span data-ttu-id="f6d0d-234">Tölur með 1200 eða 1300</span><span class="sxs-lookup"><span data-stu-id="f6d0d-234">Numbers with 1200 or 1300</span></span>|  

#### <a name="-not-equal-to"></a><span data-ttu-id="f6d0d-235">(<>) Ekki jafnt og</span><span class="sxs-lookup"><span data-stu-id="f6d0d-235">(<>) Not equal to</span></span>  

|<span data-ttu-id="f6d0d-236">Dæmi</span><span class="sxs-lookup"><span data-stu-id="f6d0d-236">Sample Expression</span></span>|<span data-ttu-id="f6d0d-237">Sýndar færslur</span><span class="sxs-lookup"><span data-stu-id="f6d0d-237">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`<>0`|<span data-ttu-id="f6d0d-238">Allar tölur aðrar en 0</span><span class="sxs-lookup"><span data-stu-id="f6d0d-238">All numbers except 0</span></span><br /><br /> <span data-ttu-id="f6d0d-239">Valkosturinn SQL Server býður upp á að sameina þetta tákn algildistákni.</span><span class="sxs-lookup"><span data-stu-id="f6d0d-239">The SQL Server Option allows you to combine this symbol with a wild card expression.</span></span> <span data-ttu-id="f6d0d-240">Til dæmis merkir <>A\* ekki jafnt og neinn texti sem byrjar á stafnum A.</span><span class="sxs-lookup"><span data-stu-id="f6d0d-240">For example, <>A\* meaning not equal to any text that starts with A.</span></span>|  

#### <a name="-greater-than"></a><span data-ttu-id="f6d0d-241">(>) Meira en</span><span class="sxs-lookup"><span data-stu-id="f6d0d-241">(>) Greater than</span></span>  

|<span data-ttu-id="f6d0d-242">Dæmi</span><span class="sxs-lookup"><span data-stu-id="f6d0d-242">Sample Expression</span></span>|<span data-ttu-id="f6d0d-243">Sýndar færslur</span><span class="sxs-lookup"><span data-stu-id="f6d0d-243">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`>1200`|<span data-ttu-id="f6d0d-244">Tölur hærri en 1200</span><span class="sxs-lookup"><span data-stu-id="f6d0d-244">Numbers greater than 1200</span></span>|  

#### <a name="-greater-than-or-equal-to"></a><span data-ttu-id="f6d0d-245">(>=) Hærra en eða jafnt og</span><span class="sxs-lookup"><span data-stu-id="f6d0d-245">(>=) Greater than or equal to</span></span>  

|<span data-ttu-id="f6d0d-246">Dæmi</span><span class="sxs-lookup"><span data-stu-id="f6d0d-246">Sample Expression</span></span>|<span data-ttu-id="f6d0d-247">Sýndar færslur</span><span class="sxs-lookup"><span data-stu-id="f6d0d-247">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`>=1200`|<span data-ttu-id="f6d0d-248">Tölur hærri en eða jafnar 1200</span><span class="sxs-lookup"><span data-stu-id="f6d0d-248">Numbers greater than or equal to 1200</span></span>|  

#### <a name="-less-than"></a><span data-ttu-id="f6d0d-249">(<) Minna en</span><span class="sxs-lookup"><span data-stu-id="f6d0d-249">(<) Less than</span></span>  

|<span data-ttu-id="f6d0d-250">Dæmi</span><span class="sxs-lookup"><span data-stu-id="f6d0d-250">Sample Expression</span></span>|<span data-ttu-id="f6d0d-251">Sýndar færslur</span><span class="sxs-lookup"><span data-stu-id="f6d0d-251">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`<1200`|<span data-ttu-id="f6d0d-252">Tölur lægri en 1200</span><span class="sxs-lookup"><span data-stu-id="f6d0d-252">Numbers less than 1200</span></span>|  

#### <a name="-less-than-or-equal-to"></a><span data-ttu-id="f6d0d-253">(<=) Lægra en eða jafnt og</span><span class="sxs-lookup"><span data-stu-id="f6d0d-253">(<=) Less than or equal to</span></span>  

|<span data-ttu-id="f6d0d-254">Dæmi</span><span class="sxs-lookup"><span data-stu-id="f6d0d-254">Sample Expression</span></span>|<span data-ttu-id="f6d0d-255">Sýndar færslur</span><span class="sxs-lookup"><span data-stu-id="f6d0d-255">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`<=1200`|<span data-ttu-id="f6d0d-256">Tölur lægri en eða jafnar 1200</span><span class="sxs-lookup"><span data-stu-id="f6d0d-256">Numbers less than or equal to 1200</span></span>|  

#### <a name="-and"></a><span data-ttu-id="f6d0d-257">(&) Og</span><span class="sxs-lookup"><span data-stu-id="f6d0d-257">(&) And</span></span>  

|<span data-ttu-id="f6d0d-258">Dæmi</span><span class="sxs-lookup"><span data-stu-id="f6d0d-258">Sample Expression</span></span>|<span data-ttu-id="f6d0d-259">Sýndar færslur</span><span class="sxs-lookup"><span data-stu-id="f6d0d-259">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`>200&<1200`|<span data-ttu-id="f6d0d-260">Tölur hærri en 200 og minni en 1200</span><span class="sxs-lookup"><span data-stu-id="f6d0d-260">Numbers greater than 200 and less than 1200</span></span>|  

#### <a name="-an-exact-character-match"></a><span data-ttu-id="f6d0d-261">('') Nákvæm stafasamsvörun</span><span class="sxs-lookup"><span data-stu-id="f6d0d-261">('') An exact character match</span></span>  

|<span data-ttu-id="f6d0d-262">Dæmi</span><span class="sxs-lookup"><span data-stu-id="f6d0d-262">Sample Expression</span></span>|<span data-ttu-id="f6d0d-263">Sýndar færslur</span><span class="sxs-lookup"><span data-stu-id="f6d0d-263">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`'man'`|<span data-ttu-id="f6d0d-264">Texta sem passar nákvæmlega við Man og er stafréttur.</span><span class="sxs-lookup"><span data-stu-id="f6d0d-264">Text that matches man exactly and is case sensitive.</span></span>|  

#### <a name="-case-insensitive"></a><span data-ttu-id="f6d0d-265">(@) Stafrétt</span><span class="sxs-lookup"><span data-stu-id="f6d0d-265">(@) Case insensitive</span></span>  

|<span data-ttu-id="f6d0d-266">Dæmi</span><span class="sxs-lookup"><span data-stu-id="f6d0d-266">Sample Expression</span></span>|<span data-ttu-id="f6d0d-267">Sýndar færslur</span><span class="sxs-lookup"><span data-stu-id="f6d0d-267">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`@man*`|<span data-ttu-id="f6d0d-268">Texti sem byrjar á Man og er ekki stafréttur.</span><span class="sxs-lookup"><span data-stu-id="f6d0d-268">Text that starts with man and is case insensitive.</span></span>|  

#### <a name="-an-indefinite-number-of-unknown-characters"></a><span data-ttu-id="f6d0d-269">(\*) Ótilgreindur fjöldi óþekktra staftákna</span><span class="sxs-lookup"><span data-stu-id="f6d0d-269">(\*) An indefinite number of unknown characters</span></span>

|<span data-ttu-id="f6d0d-270">Dæmi</span><span class="sxs-lookup"><span data-stu-id="f6d0d-270">Sample Expression</span></span>|<span data-ttu-id="f6d0d-271">Sýndar færslur</span><span class="sxs-lookup"><span data-stu-id="f6d0d-271">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`*Co*`|<span data-ttu-id="f6d0d-272">Texta sem inniheldur „Co“  og er stafréttur.</span><span class="sxs-lookup"><span data-stu-id="f6d0d-272">Text that contains "Co" and is case sensitive.</span></span>|  
|`*Co`|<span data-ttu-id="f6d0d-273">Texta sem endar á „Co“  og er stafréttur.</span><span class="sxs-lookup"><span data-stu-id="f6d0d-273">Text that ends with "Co" and is case sensitive.</span></span>|  
|`Co*`|<span data-ttu-id="f6d0d-274">Texta sem byrjar á „Co“  og er stafréttur.</span><span class="sxs-lookup"><span data-stu-id="f6d0d-274">Text that begins with "Co" and is case sensitive.</span></span>|  

#### <a name="-one-unknown-character"></a><span data-ttu-id="f6d0d-275">(?) eitt óþekkt stafatákn</span><span class="sxs-lookup"><span data-stu-id="f6d0d-275">(?) One unknown character</span></span>  

|<span data-ttu-id="f6d0d-276">Dæmi</span><span class="sxs-lookup"><span data-stu-id="f6d0d-276">Sample Expression</span></span>|<span data-ttu-id="f6d0d-277">Sýndar færslur</span><span class="sxs-lookup"><span data-stu-id="f6d0d-277">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`Hans?n`|<span data-ttu-id="f6d0d-278">Texti eins og Hansen eða Hanson</span><span class="sxs-lookup"><span data-stu-id="f6d0d-278">Text such as Hansen or Hanson</span></span>|  

#### <a name="combined-format-expressions"></a><span data-ttu-id="f6d0d-279">Sameinað framsetningarsnið</span><span class="sxs-lookup"><span data-stu-id="f6d0d-279">Combined Format Expressions</span></span>  

|<span data-ttu-id="f6d0d-280">Dæmi</span><span class="sxs-lookup"><span data-stu-id="f6d0d-280">Sample Expression</span></span>|<span data-ttu-id="f6d0d-281">Sýndar færslur</span><span class="sxs-lookup"><span data-stu-id="f6d0d-281">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`5999|8100..8490`|<span data-ttu-id="f6d0d-282">Allar færslur með tölunni 5999 eða tölu á bilinu frá 8100 til og með 8490 er teknar með.</span><span class="sxs-lookup"><span data-stu-id="f6d0d-282">Include any records with the number 5999 or a number from the interval 8100 through 8490.</span></span>|  
|`..1299|1400..`|<span data-ttu-id="f6d0d-283">Telja með færslur með tölu sem er lægri eða jöfn 1299 eða tölu sem er jöfn 1400 eða hærri (allar tölur nema 1300 til 1399).</span><span class="sxs-lookup"><span data-stu-id="f6d0d-283">Include records with a number less than or equal to 1299 or a number equal to 1400 or greater (all numbers except 1300 through 1399).</span></span>|  
|`>50&<100`|<span data-ttu-id="f6d0d-284">Telja með færslur með tölum sem eru hærri en 50 og lægri en 100 (tölurnar 51 til 99).</span><span class="sxs-lookup"><span data-stu-id="f6d0d-284">Include records with numbers that are greater than 50 and less than 100 (numbers 51 through 99).</span></span>|  

### <a name="filter-tokens"></a><span data-ttu-id="f6d0d-285"><a name="FilterTokens"> </a>Síumerki</span><span class="sxs-lookup"><span data-stu-id="f6d0d-285"><a name="FilterTokens"> </a>Filter Tokens</span></span>
<span data-ttu-id="f6d0d-286">Þegar þú slærð inn síuviðmiðanir getur þú einnig skrifað orð sem hafa sérstaka þýðingu, sem kallast síumerki.</span><span class="sxs-lookup"><span data-stu-id="f6d0d-286">When entering filter criteria, you can also type words that have special meaning, called filter tokens.</span></span> <span data-ttu-id="f6d0d-287">Eftir að hafa slegið inn merkiorðið, er orðinu skipt út fyrir gildin sem það táknar.</span><span class="sxs-lookup"><span data-stu-id="f6d0d-287">After entering the token word, the word is replaced by the value or values that it represents.</span></span> <span data-ttu-id="f6d0d-288">Þetta gerir síun auðveldara með því að draga úr þörfinni á að fara yfir á aðrar síðum til að fletta upp gildi sem þú vilt bæta við síuna.</span><span class="sxs-lookup"><span data-stu-id="f6d0d-288">This makes filtering easier by reducing the need to navigate to other pages to look up values you want to add to your filter.</span></span> <span data-ttu-id="f6d0d-289">Taflan hér fyrir neðan lýsir sumum merkjunum sem þú getur slegið inn sem síuviðmiðanir.</span><span class="sxs-lookup"><span data-stu-id="f6d0d-289">The tables below describe some of the tokens you can type as filter criteria.</span></span>

> [!TIP]
> <span data-ttu-id="f6d0d-290">Stofnunin þín getur notað sérsniðna merki.</span><span class="sxs-lookup"><span data-stu-id="f6d0d-290">Your organization may use custom tokens.</span></span> <span data-ttu-id="f6d0d-291">Til að læra um öll merkin sem þú hefur aðgang að eða til að bæta við fleiri sérsniðnum merkjum, skaltu tala við stjórnandann þinn.</span><span class="sxs-lookup"><span data-stu-id="f6d0d-291">To learn about the complete set of tokens available to you or to add more custom tokens, talk to your administrator.</span></span> <span data-ttu-id="f6d0d-292">Fyrir tæknilegar upplýsingar, sjá [Bæta við síumerkjum](/dynamics365/business-central/dev-itpro/developer/devenv-adding-filter-tokens).</span><span class="sxs-lookup"><span data-stu-id="f6d0d-292">For technical information see [Adding Filter Tokens](/dynamics365/business-central/dev-itpro/developer/devenv-adding-filter-tokens).</span></span>

#### <a name="me-or-userid-records-assigned-to-you"></a><span data-ttu-id="f6d0d-293">(%me eða %userid) Skrám úthlutað til þín</span><span class="sxs-lookup"><span data-stu-id="f6d0d-293">(%me or %userid) Records Assigned to You</span></span>

<span data-ttu-id="f6d0d-294">Notaðu `%me` eða `%userid` þegar verið er að sía reiti sem innihalda notandakenni, svo sem **úthlutað til notandakennis** reit, til að birta allar skrár sem eru úthlutað til þín.</span><span class="sxs-lookup"><span data-stu-id="f6d0d-294">Use `%me` or `%userid` when filtering fields that contain the user ID, such as **Assigned to User ID** field, to display all records that are assigned to you.</span></span>

|<span data-ttu-id="f6d0d-295">Dæmi</span><span class="sxs-lookup"><span data-stu-id="f6d0d-295">Sample Expression</span></span>|<span data-ttu-id="f6d0d-296">Sýndar færslur</span><span class="sxs-lookup"><span data-stu-id="f6d0d-296">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`%me`<br /><span data-ttu-id="f6d0d-297">eða</span><span class="sxs-lookup"><span data-stu-id="f6d0d-297">or</span></span><br />`%userid`|<span data-ttu-id="f6d0d-298">Skrár sem eru úthlutað á notandareikninginn þinn.</span><span class="sxs-lookup"><span data-stu-id="f6d0d-298">Records that are assigned to your user account.</span></span> |  

#### <a name="mycustomers-customers-in-my-customers"></a><span data-ttu-id="f6d0d-299">(%mycustomers) Viðskiptamenn í Mínir viðskiptamenn</span><span class="sxs-lookup"><span data-stu-id="f6d0d-299">(%mycustomers) Customers in My Customers</span></span>

<span data-ttu-id="f6d0d-300">Notaðu `%mycustomers` í **Nr** reitnum viðskiptamanns til að birta allar skrár fyrir viðskiptamenn sem eru innifaldir í **Mínir viðskiptamenn** listanum á Mitt hlutverk.</span><span class="sxs-lookup"><span data-stu-id="f6d0d-300">Use `%mycustomers` in the customer **No** field to display all records for customers that are included in the **My Customers** list on your Role Center.</span></span>

|<span data-ttu-id="f6d0d-301">Dæmi</span><span class="sxs-lookup"><span data-stu-id="f6d0d-301">Sample Expression</span></span>|<span data-ttu-id="f6d0d-302">Sýndar færslur</span><span class="sxs-lookup"><span data-stu-id="f6d0d-302">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`%mycustomers`|<span data-ttu-id="f6d0d-303">Viðskiptamenn í **Mínir viðskiptamenn** í Mitt hlutverk.</span><span class="sxs-lookup"><span data-stu-id="f6d0d-303">Customers in the **My Customers** on your Role Center.</span></span> |  

#### <a name="myitems-items-in-my-items"></a><span data-ttu-id="f6d0d-304">(%mytems) Atriði í Mínum atriðum</span><span class="sxs-lookup"><span data-stu-id="f6d0d-304">(%myitems) Items in My Items</span></span>

<span data-ttu-id="f6d0d-305">Notaðu `%myitems` Í atriði **Nr** reitinn til að birta allar skrár fyrir atriði sem eru innifalin í **Mín atriði** listanum í Mitt hlutverk.</span><span class="sxs-lookup"><span data-stu-id="f6d0d-305">Use `%myitems` in the item **No** field to display all records for items that are included in the **My Items** list on your Role Center.</span></span>

|<span data-ttu-id="f6d0d-306">Dæmi</span><span class="sxs-lookup"><span data-stu-id="f6d0d-306">Sample Expression</span></span>|<span data-ttu-id="f6d0d-307">Sýndar færslur</span><span class="sxs-lookup"><span data-stu-id="f6d0d-307">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`%myitems`|<span data-ttu-id="f6d0d-308">Atriði í **Mín atriði** í Mitt hlutverk.</span><span class="sxs-lookup"><span data-stu-id="f6d0d-308">Items in the **My Items** on your Role Center.</span></span> |  

#### <a name="myvendors-vendors-in-my-vendors"></a><span data-ttu-id="f6d0d-309">(%myvendors) Lánardrottnar í Mínir lánardrottnar</span><span class="sxs-lookup"><span data-stu-id="f6d0d-309">(%myvendors) Vendors in My Vendors</span></span>

<span data-ttu-id="f6d0d-310">Notaðu `%myvendors` í lánardrottinn **Nr** reitnum, til að birta allar skrá fyrir lánardrottna sem eru innifalin í **Mínir lánardrottnar** listanum í Mitt hlutverk.</span><span class="sxs-lookup"><span data-stu-id="f6d0d-310">Use `%myvendors` in the vendor **No** field to display all records for vendors that are included in the **My Vendors** list on your Role Center.</span></span>

|<span data-ttu-id="f6d0d-311">Dæmi</span><span class="sxs-lookup"><span data-stu-id="f6d0d-311">Sample Expression</span></span>|<span data-ttu-id="f6d0d-312">Sýndar færslur</span><span class="sxs-lookup"><span data-stu-id="f6d0d-312">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`%myvendors`|<span data-ttu-id="f6d0d-313">Lánardrottnar í **Mínir lánardrottnar** í Mitt hlutverk.</span><span class="sxs-lookup"><span data-stu-id="f6d0d-313">Vendors in the **My Vendors** on your Role Center.</span></span> |  

## <a name="see-also"></a><span data-ttu-id="f6d0d-314">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="f6d0d-314">See Also</span></span>

[<span data-ttu-id="f6d0d-315">Algengar spurningar um leit og síun</span><span class="sxs-lookup"><span data-stu-id="f6d0d-315">Searching and Filtering FAQ</span></span>](ui-search-filter-faq.md)  
[<span data-ttu-id="f6d0d-316">Vista og sérsníða listayfirlit</span><span class="sxs-lookup"><span data-stu-id="f6d0d-316">Save and Personalize List Views</span></span>](ui-views.md)  
<span data-ttu-id="f6d0d-317">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="f6d0d-317">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
