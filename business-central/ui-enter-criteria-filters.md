---
title: "Röðun, leit og síun í listum | Microsoft Docs"
description: "Vinna á skilvirkan hátt í listum með því að leita yfir gögnin þín, flokka dálka og hreinsa niðurstöður með öflugum síutáknum og flýtivísum."
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: delimit, FlowFilter, totals, limit, advanced
ms.date: 10/01/2018
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: f1ee115c258c25d8b695a0394dbaa11247b9b8ab
ms.contentlocale: is-is
ms.lasthandoff: 09/28/2018

---
# <a name="sorting-searching-and-filtering-lists"></a><span data-ttu-id="80c17-103">Röðun, leit og síun í listum</span><span class="sxs-lookup"><span data-stu-id="80c17-103">Sorting, Searching, and Filtering Lists</span></span>
<span data-ttu-id="80c17-104">Það eru nokkrir hlutir sem munu hjálpa þér að skanna, finna og takmarka skrár í lista.</span><span class="sxs-lookup"><span data-stu-id="80c17-104">There are a few things that you can do that will help you scan, find, and limit records in a list.</span></span> <span data-ttu-id="80c17-105">Þar á meðal er röðun, leit og afmörkun.</span><span class="sxs-lookup"><span data-stu-id="80c17-105">These include sorting, searching and filtering.</span></span> <span data-ttu-id="80c17-106">Þú getur notað suma eða alla þessa hluti samtímis til að finna eða greina gögnin þín fljótt.</span><span class="sxs-lookup"><span data-stu-id="80c17-106">You can apply some or all of these simultaneously to quickly find or analyze your data.</span></span>

> [!TIP]
> <span data-ttu-id="80c17-107">Þegar þú skoðar gögnin þín sem flísar getur þú leitað og notað grunn síun.</span><span class="sxs-lookup"><span data-stu-id="80c17-107">When viewing your data as tiles, you can search and use basic filtering.</span></span> <span data-ttu-id="80c17-108">Til að nota alla þessa öflugu eiginleika til að raða, leita og sía skaltu velja ![Sýna sem lista](media/ui_show_as_list_icon.png "Sýna sem lista ör til vinstri") tákn til að sýna sem lista.</span><span class="sxs-lookup"><span data-stu-id="80c17-108">To use the full set of powerful features for sorting, searching and filtering, choose the ![Show as list](media/ui_show_as_list_icon.png "Show as list arrow left") icon to show as a list.</span></span>

<!--
When you want to search for data, such as customer names, addresses, or product groups, you enter criteria. In search criteria you can use all the numbers and letters that you normally use in the specific field. In addition, you can use special symbols to further filter the results. There are two ways to search: using the Quick Filter or column filters.
-->

## <a name="sorting"></a><span data-ttu-id="80c17-109">Röðun</span><span class="sxs-lookup"><span data-stu-id="80c17-109">Sorting</span></span>
<span data-ttu-id="80c17-110">Með Röðun er auðvelt og fljótlegt að fá yfirsýn yfir gögnin.</span><span class="sxs-lookup"><span data-stu-id="80c17-110">Sorting makes it easy for you to get a quick overview of your data.</span></span> <span data-ttu-id="80c17-111">Ef þú ert með marga viðskiptamenn til dæmis, er hægt að velja að raða þeim eftir **númeri Viðskiptamanns**, **Bókunarflokkum viðskiptavinar**, **Gjaldmiðilskóði**, **LandsSvæðiskóða**, eða **skráningarnúmer Söluskatts** til að fá það yfirlit sem þú þarft.</span><span class="sxs-lookup"><span data-stu-id="80c17-111">If you have many customers, for example, you can choose to sort them by **Customer No.**, **Customer Posting Group**, **Currency Code**, **Country Region Code**, or **Sales Tax Registration No.** to get the overview you need.</span></span>

<span data-ttu-id="80c17-112">Til að raða á lista, geturðu annað hvort valið fyrirsagnatexta dálka til að skipta á milli hækkandi og lækkandi pöntunar, eða valið litlu niður-örina í dálkafyrirsögninni, og síðan valið **Hækkandi** eða **Lækkandi**.</span><span class="sxs-lookup"><span data-stu-id="80c17-112">To sort a list, you can either choose a column heading text to toggle between ascending and descending order, or choose the small down arrow in the column heading, and then choose **Ascending** or **Descending**.</span></span>  

> [!NOTE]  
>   <span data-ttu-id="80c17-113">Myndir, BLOB-reitir, FlowFilters og reitir sem tilheyra ekki töflu styðja ekki röðun.</span><span class="sxs-lookup"><span data-stu-id="80c17-113">Sorting is not supported on images, BLOB fields, FlowFilters, and fields that do not belong to a table.</span></span>  

## <a name="searching"></a><span data-ttu-id="80c17-114">Leit</span><span class="sxs-lookup"><span data-stu-id="80c17-114">Searching</span></span>
<span data-ttu-id="80c17-115"><!--## Searching by using the Quick Filter --> Efst á sérhverri listasíðu er ![Leita í lista](media/ui-search/search-list.png "Leita í listatákni") **Leita** tákn sem býður upp á fljótlega og auðvelda leið til að vinna gögnin niður í lista og sýna einungis þær skrár sem innihalda gögnin sem þú vilt sjá.</span><span class="sxs-lookup"><span data-stu-id="80c17-115"><!--## Searching by using the Quick Filter --> At the top of each list page, there is a ![Search list](media/ui-search/search-list.png "Search list icon") **Search** icon that provides a quick and easy way to reduce the records in a list and display only those records that contain the data that you are interested in seeing.</span></span>

<span data-ttu-id="80c17-116">Til að leita, skaltu einfaldlega velja leitartáknið, og síðan skrifa í boxið textann sem þú ert að leita að.</span><span class="sxs-lookup"><span data-stu-id="80c17-116">To search, simply select the search icon, and then in the box, type the text that you are looking for.</span></span> <span data-ttu-id="80c17-117">Þú getur slegið inn stafi, númer og önnur tákn.</span><span class="sxs-lookup"><span data-stu-id="80c17-117">You can enter letters, numbers, and other symbols.</span></span>

### <a name="fine-tune-the-search"></a><span data-ttu-id="80c17-118">Fínstilla leitina</span><span class="sxs-lookup"><span data-stu-id="80c17-118">Fine-tune the search</span></span>
<span data-ttu-id="80c17-119">Almennt séð mun leitin reyna að finna samsvörun við textann í öllum reitum; hún gerir ekki greinarmun á hástöfum og lágstöfum (með öðrum orðum, óháð há- og lágstöfum) og mun finna textasamsvörun hvar sem er í reitnum (fremst, aftast eða í miðjunni).</span><span class="sxs-lookup"><span data-stu-id="80c17-119">In general, search will attempt to match text across all fields; it does not distinguish between uppercase and lowercase characters (in other words, case insensitive), and will match text placed anwhere in the field (at the beginning, end, or in the middle).</span></span>

<span data-ttu-id="80c17-120">Hins vegar geturðu búið til nákvæmari leit með því að nota eftirfarandi sértákn:</span><span class="sxs-lookup"><span data-stu-id="80c17-120">However, you can make a more exact search by using the following special characters:</span></span>

- <span data-ttu-id="80c17-121">Til að finna aðeins reitargildi sem samsvara öllum textanum og stöfunum, skal staðsetja textann á milli einfaldra gæsalappa `''` (til dæmis, `'man'`).</span><span class="sxs-lookup"><span data-stu-id="80c17-121">To find only field values that match the entire text and case exactly, place the search text between single quotes `''` (for example, `'man'`).</span></span>

- <span data-ttu-id="80c17-122">Til að finna reitargildi sem byrja á ákveðnum texta og samsvara stöfunum, skal setja `*` á eftir leitartextanum (til dæmis `man*`).</span><span class="sxs-lookup"><span data-stu-id="80c17-122">To find field values that start with a certain text and match the case, place `*` after the search text (for example `man*`).</span></span>

- <span data-ttu-id="80c17-123">Til að finna reitargildi sem enda á ákveðnum texta og samsvara stöfunum, skal setja `*` á undan leitartextanum (til dæmis `*man`).</span><span class="sxs-lookup"><span data-stu-id="80c17-123">To find field values that end with a certain text and match the case, place `*` before the search text (for example `*man`).</span></span>

- <span data-ttu-id="80c17-124">Þegar `''` eða `*` er notað er leitin háð há- og lágstöfum.</span><span class="sxs-lookup"><span data-stu-id="80c17-124">When using  `''` or `*`, the search is case sensitive.</span></span> <span data-ttu-id="80c17-125">Ef þú vilt gera leitina óháða há- og lágstöfum skaltu setja `@` á undan leitartextanum (til dæmis `@man*`).</span><span class="sxs-lookup"><span data-stu-id="80c17-125">If you want to make the search case insensitive, place `@` before the search text (for example `@man*`).</span></span>

<span data-ttu-id="80c17-126">Eftirfarandi tafla sýnir nokkur dæmi til að útskýra hvernig hægt er að nota leitina.</span><span class="sxs-lookup"><span data-stu-id="80c17-126">The following table provides some examples to explain how you can use the search.</span></span>


<!--
In search criteria you can use all the numbers and letters that you normally use in the specific field. In addition, you can use special symbols to further filter the results. There are two ways to search: using the Quick Filter or column filters.-->

<!--
The Quick Filter provides an easy access to filter data by entering plain text, but does also provide a lot of search criteria options. Depending on whether you enter plain text or text including symbols, the Quick Filter behaves differently.  

* If you enter plain text in the search criteria, the search criteria is interpreted as a case insensitive search that contains certain text.  
* If you enter text including symbols in the search criteria, the search criteria is interpreted exactly as you entered it, and the search is case sensitive.
-->
<!--

|Search Criteria|Interpreted as...|Finds...|
|---------------|----------------|----------|
|`man`<br />or <br />`Man`|Contains the text; case insensitive|All records with fields that contain the text **man**, regardless of the case.|
|`'Man'`|Entire text match; case sensitive.|All records with fields that only contain **Man** exactly.|
|`Man*`|Starts with the text; case sensitive.|All records with fields that start with the text <b>Man</b> exactly.|
|`@Man*`|Starts with the text; case insensitive.|All records with fields that start with **man**, regardless of the case.|
|`@*man`|Ends with the text; case insensitive.|All records that end with **man**, regardless of the case.|
-->

|<span data-ttu-id="80c17-127">Leitarskilyrði</span><span class="sxs-lookup"><span data-stu-id="80c17-127">Search Criteria</span></span>|<span data-ttu-id="80c17-128">Finnur ...</span><span class="sxs-lookup"><span data-stu-id="80c17-128">Finds...</span></span>|
|---------------|----------|
|`man`<br /><span data-ttu-id="80c17-129">eða</span><span class="sxs-lookup"><span data-stu-id="80c17-129">or</span></span> <br />`Man`|<span data-ttu-id="80c17-130">Allar skrár með reitum sem innihalda textann **man**, óháð því hvort notaðir eru há- eða lágstafir.</span><span class="sxs-lookup"><span data-stu-id="80c17-130">All records with fields that contain the text **man**, regardless of the case.</span></span> <span data-ttu-id="80c17-131">Til dæmis, **Manchester**, **manual**, eða **Sportsman**.</span><span class="sxs-lookup"><span data-stu-id="80c17-131">For example, **Manchester**, **manual**, or **Sportsman**.</span></span> |
|`'Man'`|<span data-ttu-id="80c17-132">Allar skrár með reitum sem innihalda aðeins **Man**, í samræmi við há- og lágstafi.</span><span class="sxs-lookup"><span data-stu-id="80c17-132">All records with fields that contain only **Man**, matching the case.</span></span>|
|`Man*`|<span data-ttu-id="80c17-133">Allar skrár með reitum sem byrja á textanum <b>Man</b>, í samræmi við há- og lágstafi.</span><span class="sxs-lookup"><span data-stu-id="80c17-133">All records with fields that start with the text <b>Man</b>, matching the case.</span></span> <span data-ttu-id="80c17-134">Til dæmis, **Manchester** en ekki **manual** eða **Sportsman** .</span><span class="sxs-lookup"><span data-stu-id="80c17-134">For example, **Manchester** but not **manual** or **Sportsman**.</span></span>|
|`@Man*`|<span data-ttu-id="80c17-135">Allar skrár með reitum sem byrja með **man**, óháð því hvort notaðir eru há- eða lágstafir.</span><span class="sxs-lookup"><span data-stu-id="80c17-135">All records with fields that start with **man**, regardless of the case.</span></span> <span data-ttu-id="80c17-136">Til dæmis, **Manchester** og **manual**, en ekki **Sportsman**.</span><span class="sxs-lookup"><span data-stu-id="80c17-136">For example, **Manchester** and **manual**, but not **Sportsman**.</span></span>|
|`@*man`|<span data-ttu-id="80c17-137">Allar skrár sem endar með **man**, óháð því hvort notaðir eru há- eða lágstafir.</span><span class="sxs-lookup"><span data-stu-id="80c17-137">All records that end with **man**, regardless of the case.</span></span> <span data-ttu-id="80c17-138">Til dæmis **Sportsman**, en ekki **Manchester** eða **manual**.</span><span class="sxs-lookup"><span data-stu-id="80c17-138">For example **Sportsman**, but not **Manchester** or **manual**.</span></span>|

> [!TIP]
> <span data-ttu-id="80c17-139">Þú getur ýtt á F3 til að virkja og slökkva á leitarreitnum.</span><span class="sxs-lookup"><span data-stu-id="80c17-139">You can press F3 to activate and deactivate the search box.</span></span> <span data-ttu-id="80c17-140">Frekari upplýsingar er að finna í [Flýtilyklar](keyboard-shortcuts.md#KeyboardFilter).</span><span class="sxs-lookup"><span data-stu-id="80c17-140">For more information see [Keyboard Shortcuts](keyboard-shortcuts.md#KeyboardFilter).</span></span>

## <a name="filtering"></a><span data-ttu-id="80c17-141">Afmörkun</span><span class="sxs-lookup"><span data-stu-id="80c17-141">Filtering</span></span>
<span data-ttu-id="80c17-142">Síun veitir háþróaðri og fjölhæfur leið til að stjórna hvaða skrár sem birtast á lista.</span><span class="sxs-lookup"><span data-stu-id="80c17-142">Filtering provides a more advanced and versatile way of controlling which records display in a list.</span></span> <span data-ttu-id="80c17-143">Það eru tvær helstu munur á leit og síun, eins og lýst er í töflunni hér að neðan.</span><span class="sxs-lookup"><span data-stu-id="80c17-143">There are two major differences between searching and filtering, as described in the table below.</span></span>

|| <span data-ttu-id="80c17-144">**Leit**</span><span class="sxs-lookup"><span data-stu-id="80c17-144">**Searching**</span></span> | <span data-ttu-id="80c17-145">**Afmörkun**</span><span class="sxs-lookup"><span data-stu-id="80c17-145">**Filtering**</span></span> |
|--|----------|------------|
| <span data-ttu-id="80c17-146">**Reitir sem gilda**</span><span class="sxs-lookup"><span data-stu-id="80c17-146">**Applicable fields**</span></span> | <span data-ttu-id="80c17-147">Leitar yfir alla reitum sem eru sýnilegar á síðunni.</span><span class="sxs-lookup"><span data-stu-id="80c17-147">Searches across all fields that are visible on the page.</span></span> | <span data-ttu-id="80c17-148">Síar einn eða fleiri reiti, hvern fyrir sig, og velur úr öllum reitum í töflunni, þar á meðal reiti sem eru ekki sýnilegar á síðunni.</span><span class="sxs-lookup"><span data-stu-id="80c17-148">Filters one or more fields individually, selecting from any field on the table, including fields that are not visible on the page.</span></span> |
| <span data-ttu-id="80c17-149">**Samsvörun**</span><span class="sxs-lookup"><span data-stu-id="80c17-149">**Matching**</span></span> | <span data-ttu-id="80c17-150">Sýnir skrár með reitum sem passa við leitartexta, óháð notkun há- og lágstafa, eða staðsetningu þess texta.</span><span class="sxs-lookup"><span data-stu-id="80c17-150">Displays records with fields that match the search text, irrespective of casing or placement of that text.</span></span> | <span data-ttu-id="80c17-151">Sýnir skrár þar sem reiturinn passar nákvæmlega við síuna og gerir greinarmun á há- og lágstöfum, nema sérstakar síu tákn séu slegin inn.</span><span class="sxs-lookup"><span data-stu-id="80c17-151">Displays records where the field matches the filter exactly and is case sensitive, unless special filter symbols are entered.</span></span>

<span data-ttu-id="80c17-152">Síun gerir þér kleift að birta skrár fyrir tiltekna reikninga eða viðskiptamenn, dagsetningar, upphæð og aðrar upplýsingar með því að tilgreina síuviðmiðanir.</span><span class="sxs-lookup"><span data-stu-id="80c17-152">Filtering enables you to display records for specific accounts or customers, dates, amounts, and other information by specifying filter criteria.</span></span> <span data-ttu-id="80c17-153">Aðeins eru birtar þær færslur sem uppfylla skilyrðin.</span><span class="sxs-lookup"><span data-stu-id="80c17-153">Only records that match the criteria are displayed.</span></span> <span data-ttu-id="80c17-154">Ef þú tilgreinir skilyrði fyrir marga reiti, þá birtast aðeins skrár sem passa við öll skilyrði.</span><span class="sxs-lookup"><span data-stu-id="80c17-154">If you specify criteria for multiple fields, then only records that match all criteria will be displayed.</span></span>

### <a name="working-in-the-filter-pane"></a><span data-ttu-id="80c17-155">Vinna í síusvæðinu</span><span class="sxs-lookup"><span data-stu-id="80c17-155">Working in the filter pane</span></span>
<span data-ttu-id="80c17-156">Síusvæðið sýnir núverandi síur fyrir lista og gerir þér kleift að stilla eigin sérsniðna síur í einu eða fleiri reitum.</span><span class="sxs-lookup"><span data-stu-id="80c17-156">The filter pane displays the current filters for a list, and enables you to set your own custom filters on one or more fields.</span></span> <span data-ttu-id="80c17-157">Eftirfarandi mynd sýnir dæmi um síusvæði fyrir sölutilboðalista.</span><span class="sxs-lookup"><span data-stu-id="80c17-157">The following figure shows an example filter pane for a Sales Quotes list.</span></span>

<span data-ttu-id="80c17-158">![Yfirlit yfir síusvæðið ](media/filter-pane-overview.png "Síutákn")</span><span class="sxs-lookup"><span data-stu-id="80c17-158">![Filter pane overview ](media/filter-pane-overview.png "Filter icon")</span></span>

<span data-ttu-id="80c17-159">Til að sýna síusvæðið skal nota **Shift+F3** flýtilykil.</span><span class="sxs-lookup"><span data-stu-id="80c17-159">To display the filter pane, use the **Shift+F3** keyboard shortcut.</span></span> <span data-ttu-id="80c17-160">Fyrir lista innan Mitt hlutverk geturðu einnig valið niður-örina nálægt síðutitlinum í yfirlitsstikunni yfir listanum og síðan **Sýna síusvæði**.</span><span class="sxs-lookup"><span data-stu-id="80c17-160">For lists within the Role Center, you can also choose the down arrow near the page title in the navigation bar above the list, and then choose **Show filter pane**.</span></span>

<span data-ttu-id="80c17-161">![Sýna síusvæði](media/open-filter-pane.png "Sýna síusvæði")</span><span class="sxs-lookup"><span data-stu-id="80c17-161">![Show filter pane](media/open-filter-pane.png "Show filter pane")</span></span>

<span data-ttu-id="80c17-162">Síusvæði er skipt í þrjá hluta: **Skoðanir**, **Sía listi eftir** og **Sía samtölur eftir**:</span><span class="sxs-lookup"><span data-stu-id="80c17-162">A filter pane is divided in three sections: **Views**, **Filter list by**, and **Filter totals by**:</span></span>

- <span data-ttu-id="80c17-163">**Yfirlit**</span><span class="sxs-lookup"><span data-stu-id="80c17-163">**Views**</span></span>

  <span data-ttu-id="80c17-164">Sumir listar muna hafa **Skoðanir** hlutann með.</span><span class="sxs-lookup"><span data-stu-id="80c17-164">Some lists will include the **Views** section.</span></span> <span data-ttu-id="80c17-165">Skoðanir eru afbrigði af listanum sem hefur verið forstillt með síum.</span><span class="sxs-lookup"><span data-stu-id="80c17-165">Views are variations of the list that have been preconfigured with filters.</span></span> <span data-ttu-id="80c17-166">Til að skipta yfir í annað yfirlit á listanum þínum skaltu einfaldlega velja annan tengil.</span><span class="sxs-lookup"><span data-stu-id="80c17-166">To switch to a different view of your list, simply select another link.</span></span> <span data-ttu-id="80c17-167">Þú getur breytt síum tímabundið á yfirliti, en breytingar verða ekki varanlega vistaðar.</span><span class="sxs-lookup"><span data-stu-id="80c17-167">You can temporarily change the filters on a view, but the changes will not be permanently saved.</span></span>

- <span data-ttu-id="80c17-168">**Sía listi eftir**</span><span class="sxs-lookup"><span data-stu-id="80c17-168">**Filter list by**</span></span>

  <span data-ttu-id="80c17-169">**Sía lista eftir** hlutinn er þar sem þú bætir við síum á tilteknum reitum til að draga úr fjölda birtra skráa.</span><span class="sxs-lookup"><span data-stu-id="80c17-169">The **Filter list by** section is where you add filters on specific fields to reduce the number of displayed records.</span></span> <span data-ttu-id="80c17-170">Til að bæta við síu skaltu velja **+ Sía**, veldu reitinn sem þú vilt sía, úr öllum reitum sem er í töflunni, og sláðu síðan inn síuviðmiðanir í glugganum.</span><span class="sxs-lookup"><span data-stu-id="80c17-170">To add a filter, select **+ Filter**, select the field that you want to filter from any field in the table, and then enter filter criteria in the box.</span></span>

- <span data-ttu-id="80c17-171">**Sía samtölur eftir**</span><span class="sxs-lookup"><span data-stu-id="80c17-171">**Filter totals by**</span></span>

  <span data-ttu-id="80c17-172">Sumar listar sem sýna reiknaðir reitir, svo sem upphæðir og fjölda, munu innihalda **Sía samtölur eftir** hlutann þar sem þú getur breytt ýmsum víddum sem hafa áhrif á útreikninga.</span><span class="sxs-lookup"><span data-stu-id="80c17-172">Some lists that display calculated fields, such as amounts and quantities, will include the **Filter totals by** section where you can adjust various dimensions that influence calculations.</span></span> <span data-ttu-id="80c17-173">Til dæmis getur þú gert skjóta greiningu á bókhaldslyklinum þínum með því að sía upphæðir á tilteknu tímabili eða þú getur skoðað samtölur fyrir sölupantanir aðeins frá tilteknu vörugeymslu.</span><span class="sxs-lookup"><span data-stu-id="80c17-173">For example, you can quickly analyze your chart of accounts by filtering amounts to a specific period, or you can view the totals for sales orders only from a specific warehouse.</span></span>

  <span data-ttu-id="80c17-174">Til að bæta við síu, veldu **+ Sía**, veldu eitt af fyrirfram ákveðnum víddum og svo bæta við síuviðmiðunum í reitnum.</span><span class="sxs-lookup"><span data-stu-id="80c17-174">To add a filter, select **+ Filter**, select one of the predefined dimensions, and then add the filter criteria in the box.</span></span>

  > [!NOTE]
  > <span data-ttu-id="80c17-175">Síur í **Sía samtölur eftir** hlutanum eru stjórnað af FlowFilters í síðuhönnuninni.</span><span class="sxs-lookup"><span data-stu-id="80c17-175">Filters in the **Filter totals by** section are controlled by FlowFilters in the page design.</span></span> <span data-ttu-id="80c17-176">Fyrir tæknilegar upplýsingar, sjá [FlowFilters](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/developer/devenv-flowfilter-overview).</span><span class="sxs-lookup"><span data-stu-id="80c17-176">For technical information, see [FlowFilters](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/developer/devenv-flowfilter-overview).</span></span>


### <a name="entering-filter-criteria-in-the-filter-pane"></a><span data-ttu-id="80c17-177">Slá inn síuviðmiðanir í síusvæðinu</span><span class="sxs-lookup"><span data-stu-id="80c17-177">Entering filter criteria in the filter pane</span></span>
<span data-ttu-id="80c17-178">Til að velja reit til að sía skaltu gera eitt af eftirfarandi:</span><span class="sxs-lookup"><span data-stu-id="80c17-178">To select a field to filter, do one of the following:</span></span>
  - <span data-ttu-id="80c17-179">Í síusvæðinu, veldu **+ Reitur**.</span><span class="sxs-lookup"><span data-stu-id="80c17-179">In the filter pane, choose **+ Field**.</span></span> <span data-ttu-id="80c17-180">Sláðu inn heiti reitsins sem þú vilt sía eða veldu reit frá valmyndinni sem sýnir alla reiti í töflunni.</span><span class="sxs-lookup"><span data-stu-id="80c17-180">Type the name of the field you wish to filter, or pick a field from the menu that displays all fields in the table.</span></span>

  - <span data-ttu-id="80c17-181">Í dálkhausi, veldu niður-örina og veldu síðan **Sía ...**. Þetta mun opna síusvæðið og bæta dálknum við síusvæðið.</span><span class="sxs-lookup"><span data-stu-id="80c17-181">In a column heading, choose the down arrow, and then choose **Filter...**. This will open the filter pane and add the column to the filter pane.</span></span>

<span data-ttu-id="80c17-182">Þú getur nú skrifað eða valið síuskilyrði í glugganum.</span><span class="sxs-lookup"><span data-stu-id="80c17-182">You can now type or select your filter criteria in the box.</span></span> <span data-ttu-id="80c17-183">Tegund reitsins sem þú síar ákvarðar hvaða skilyrði þú getur slegið inn.</span><span class="sxs-lookup"><span data-stu-id="80c17-183">The type of field you filter determines which criteria you can enter.</span></span> <span data-ttu-id="80c17-184">Til dæmis, að sía reit sem hefur fasta gildi mun einungis leyfa þér að velja úr þeim gildum.</span><span class="sxs-lookup"><span data-stu-id="80c17-184">For example, filtering a field that has fixed values will only let you choose from those values.</span></span> <span data-ttu-id="80c17-185">Nánari upplýsingar um sérstaka síu tákn sjá [Sía viðmiðanir](#FilterCriteria) og [Síumerki](#FilterTokens).</span><span class="sxs-lookup"><span data-stu-id="80c17-185">For more information about special filter symbols, see [Filter criteria](#FilterCriteria) and [Filter tokens](#FilterTokens).</span></span>

<span data-ttu-id="80c17-186">Dálkar sem þegar eru með síur eru auðkenndar með ![Síutákn](media/ui-search/filter-icon.png "Síutákn") í dálkhausnum.</span><span class="sxs-lookup"><span data-stu-id="80c17-186">Columns that already have filters are indicated by the ![Filter icon](media/ui-search/filter-icon.png "Filter icon") in the column heading.</span></span> <span data-ttu-id="80c17-187">Til að fjarlægja síu skaltu velja dálkhausinn og svo velja **Hreinsa síu** .</span><span class="sxs-lookup"><span data-stu-id="80c17-187">To remove a filter, select the column heading, then choose **Clear Filter**.</span></span>


### <a name="entering-filter-criteria-without-the-filter-pane"></a><span data-ttu-id="80c17-188">Slá inn síuviðmiðanir án síusvæðisins</span><span class="sxs-lookup"><span data-stu-id="80c17-188">Entering filter criteria without the filter pane</span></span>
<span data-ttu-id="80c17-189">Þú getur tilgreint einfaldar síur beint á listanum án þess að þurfa að nota síusvæðið.</span><span class="sxs-lookup"><span data-stu-id="80c17-189">You can specify simple filters directly within the list without having to use the filter pane.</span></span>
<span data-ttu-id="80c17-190">Með hvaða reit sem er valinn í röð, nota **Alt + F3** flýtilykil til að birta aðeins skrár sem hafa sama gildi.</span><span class="sxs-lookup"><span data-stu-id="80c17-190">With any field selected on a row, use the **Alt+F3** keyboard shortcut to display only the records having that same value.</span></span> <span data-ttu-id="80c17-191">Þú getur síðan valið annan reit og notað sömu flýtileið aftur til að halda áfram að hreinsa síurnar.</span><span class="sxs-lookup"><span data-stu-id="80c17-191">You can then select another field and use the same shortcut again to continue refining your filters.</span></span> <span data-ttu-id="80c17-192">Ef valinn reitur er nú þegar síað, mun notkun á **Alt + F3** eyða þeirri síu.</span><span class="sxs-lookup"><span data-stu-id="80c17-192">If the selected field is already filtered, using **Alt+F3** will clear that filter.</span></span>

> [!TIP]
> <span data-ttu-id="80c17-193">Finna og greina gögnin þín fljótar með því að nota samsetningar flýtilykla.</span><span class="sxs-lookup"><span data-stu-id="80c17-193">Accelerate finding and analyzing your data by using combinations of keyboard shortcuts.</span></span> <span data-ttu-id="80c17-194">Til dæmis, veldu reit, notaðu **Shift + Alt + F3** til að bæta reitnum við síusvæðið, sláðu inn síuviðmiðin, notaðu **Ctrl + Enter** til að fara aftur í raðirnar, veldu annað reit og notaðu **Alt + F3** til að sía í það gildi.</span><span class="sxs-lookup"><span data-stu-id="80c17-194">For example, select a field, use **Shift+Alt+F3** to add that field to the filter pane, type the filter criteria, use **Ctrl+Enter** to return to the rows, select another field, and use **Alt+F3** to filter to that value.</span></span>
<span data-ttu-id="80c17-195">Frekari upplýsingar er að finna í [Flýtilyklar](keyboard-shortcuts.md#KeyboardFilter).</span><span class="sxs-lookup"><span data-stu-id="80c17-195">For more information see [Keyboard Shortcuts](keyboard-shortcuts.md#KeyboardFilter).</span></span>


## <span data-ttu-id="80c17-196"><a name="FilterCriteria"> </a>Afmörkunarviðmið og tákn</span><span class="sxs-lookup"><span data-stu-id="80c17-196"><a name="FilterCriteria"> </a>Filter criteria and symbols</span></span>
<span data-ttu-id="80c17-197">Þegar skilyrði eru sett er hægt að nota alla sömu tölustafi og bókstafi sem venjulega eru notaðir í reitnum.</span><span class="sxs-lookup"><span data-stu-id="80c17-197">When you enter criteria, you can use all the numbers and letters that you can normally use in the field.</span></span> <span data-ttu-id="80c17-198">Ennfremur er hægt að nota sértákn til að afmarka niðurstöðurnar frekar.</span><span class="sxs-lookup"><span data-stu-id="80c17-198">In addition, you can use special symbols to further filter the results.</span></span> <span data-ttu-id="80c17-199">Í eftirfarandi töflum eru táknin sem hægt er að nota í afmarkanir.</span><span class="sxs-lookup"><span data-stu-id="80c17-199">The following tables show the symbols which can be used in filters.</span></span> <span data-ttu-id="80c17-200">Fyrir dagsetningar og tíma er einnig hægt að vísa til [Vinna með dagsetningar og tíma í dagatali](ui-enter-date-ranges.md) til að fá nánari upplýsingar.</span><span class="sxs-lookup"><span data-stu-id="80c17-200">For dates and times, you can also refer to [Working with Calendar Dates and Times](ui-enter-date-ranges.md) for more detailed information.</span></span>

> [!IMPORTANT]  
>  <span data-ttu-id="80c17-201">Það geta verið tilvik þar sem gildi reita innihalda þessi tákn og þú vilt setja afmörkun á þau.</span><span class="sxs-lookup"><span data-stu-id="80c17-201">There may be instances where field values contain these symbols and you want to filter on them.</span></span> <span data-ttu-id="80c17-202">Til að gera það, verðurðu að hafa með afmörkunarsegðina sem inniheldur táknið með gæsalöppum („“).</span><span class="sxs-lookup"><span data-stu-id="80c17-202">To do this, you must include the filter expression that contains the symbol in quotation marks ('').</span></span> <span data-ttu-id="80c17-203">Til dæmis, ef þú vilt sía á færslum sem byrja á textanum *S&R*, er síusegðin `'S&R*'`.</span><span class="sxs-lookup"><span data-stu-id="80c17-203">For example, if you want to filter on records that start with the text *S&R*, the filter expression is `'S&R*'`.</span></span>  

### <a name="-interval"></a><span data-ttu-id="80c17-204">(..) Bil</span><span class="sxs-lookup"><span data-stu-id="80c17-204">(..) Interval</span></span>

|<span data-ttu-id="80c17-205">Dæmi</span><span class="sxs-lookup"><span data-stu-id="80c17-205">Sample Expression</span></span>|<span data-ttu-id="80c17-206">Sýndar færslur</span><span class="sxs-lookup"><span data-stu-id="80c17-206">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`1100..2100`|<span data-ttu-id="80c17-207">Tölur 1100 til 2100.</span><span class="sxs-lookup"><span data-stu-id="80c17-207">Numbers 1100 through 2100</span></span>|  
|`..2500`|<span data-ttu-id="80c17-208">Reikningar til og með 2500</span><span class="sxs-lookup"><span data-stu-id="80c17-208">Up to and including 2500</span></span>|  
|`..12 31 00`|<span data-ttu-id="80c17-209">Dagsetningar til og með 31. 12. 00.</span><span class="sxs-lookup"><span data-stu-id="80c17-209">Dates up to and including 12 31 00</span></span>|  
|`P8..`|<span data-ttu-id="80c17-210">Upplýsingar um reikningstímabil 8 og síðar.</span><span class="sxs-lookup"><span data-stu-id="80c17-210">Information for accounting period 8 and thereafter</span></span>|  
|`..23`|<span data-ttu-id="80c17-211">Frá upphafsdegi til 23. þessa mánaðar – þessa árs 23:59:59</span><span class="sxs-lookup"><span data-stu-id="80c17-211">From the beginning date until 23-current month-current year 23:59:59</span></span>|  
|`23..`|<span data-ttu-id="80c17-212">Frá 23. þessa mánaðar – þessa árs 00:00:00 til loka tímans</span><span class="sxs-lookup"><span data-stu-id="80c17-212">From 23-current month-current year 0:00:00 until the end of time</span></span>|  
|`22..23`|<span data-ttu-id="80c17-213">Frá 22. þessa mánaðar – þessa árs 00:00:00 til 23. þessa mánaðar – þessa árs 23:59:59</span><span class="sxs-lookup"><span data-stu-id="80c17-213">From 22-current month-current year 0:00:00 until 23-current month-current year 23:59:59</span></span>|  

### <a name="124-eitheror"></a><span data-ttu-id="80c17-214">(&#124;) Annaðhvort/eða</span><span class="sxs-lookup"><span data-stu-id="80c17-214">(&#124;) Either/or</span></span>  

|<span data-ttu-id="80c17-215">Dæmi</span><span class="sxs-lookup"><span data-stu-id="80c17-215">Sample Expression</span></span>|<span data-ttu-id="80c17-216">Sýndar færslur</span><span class="sxs-lookup"><span data-stu-id="80c17-216">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|<span data-ttu-id="80c17-217">„1200</span><span class="sxs-lookup"><span data-stu-id="80c17-217">\`1200</span></span>|<span data-ttu-id="80c17-218">1300“</span><span class="sxs-lookup"><span data-stu-id="80c17-218">1300\`</span></span>|<span data-ttu-id="80c17-219">Tölur með 1200 eða 1300</span><span class="sxs-lookup"><span data-stu-id="80c17-219">Numbers with 1200 or 1300</span></span>|  

### <a name="-not-equal-to"></a><span data-ttu-id="80c17-220">(<>) Ekki jafnt og</span><span class="sxs-lookup"><span data-stu-id="80c17-220">(<>) Not equal to</span></span>  

|<span data-ttu-id="80c17-221">Dæmi</span><span class="sxs-lookup"><span data-stu-id="80c17-221">Sample Expression</span></span>|<span data-ttu-id="80c17-222">Sýndar færslur</span><span class="sxs-lookup"><span data-stu-id="80c17-222">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`<>0`|<span data-ttu-id="80c17-223">Allar tölur aðrar en 0</span><span class="sxs-lookup"><span data-stu-id="80c17-223">All numbers except 0</span></span><br /><br /> <span data-ttu-id="80c17-224">Valkosturinn SQL Server býður upp á að sameina þetta tákn algildistákni.</span><span class="sxs-lookup"><span data-stu-id="80c17-224">The SQL Server Option allows you to combine this symbol with a wild card expression.</span></span> <span data-ttu-id="80c17-225">Til dæmis merkir <>A\* ekki jafnt og neinn texti sem byrjar á stafnum A.</span><span class="sxs-lookup"><span data-stu-id="80c17-225">For example, <>A\* meaning not equal to any text that starts with A.</span></span>|  

### <a name="-greater-than"></a><span data-ttu-id="80c17-226">(>) Meira en</span><span class="sxs-lookup"><span data-stu-id="80c17-226">(>) Greater than</span></span>  

|<span data-ttu-id="80c17-227">Dæmi</span><span class="sxs-lookup"><span data-stu-id="80c17-227">Sample Expression</span></span>|<span data-ttu-id="80c17-228">Sýndar færslur</span><span class="sxs-lookup"><span data-stu-id="80c17-228">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`>1200`|<span data-ttu-id="80c17-229">Tölur hærri en 1200</span><span class="sxs-lookup"><span data-stu-id="80c17-229">Numbers greater than 1200</span></span>|  

### <a name="-greater-than-or-equal-to"></a><span data-ttu-id="80c17-230">(>=) Hærra en eða jafnt og</span><span class="sxs-lookup"><span data-stu-id="80c17-230">(>=) Greater than or equal to</span></span>  

|<span data-ttu-id="80c17-231">Dæmi</span><span class="sxs-lookup"><span data-stu-id="80c17-231">Sample Expression</span></span>|<span data-ttu-id="80c17-232">Sýndar færslur</span><span class="sxs-lookup"><span data-stu-id="80c17-232">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`>=1200`|<span data-ttu-id="80c17-233">Tölur hærri en eða jafnar 1200</span><span class="sxs-lookup"><span data-stu-id="80c17-233">Numbers greater than or equal to 1200</span></span>|  

### <a name="-less-than"></a><span data-ttu-id="80c17-234">(<) Minna en</span><span class="sxs-lookup"><span data-stu-id="80c17-234">(<) Less than</span></span>  

|<span data-ttu-id="80c17-235">Dæmi</span><span class="sxs-lookup"><span data-stu-id="80c17-235">Sample Expression</span></span>|<span data-ttu-id="80c17-236">Sýndar færslur</span><span class="sxs-lookup"><span data-stu-id="80c17-236">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`<1200`|<span data-ttu-id="80c17-237">Tölur lægri en 1200</span><span class="sxs-lookup"><span data-stu-id="80c17-237">Numbers less than 1200</span></span>|  

### <a name="-less-than-or-equal-to"></a><span data-ttu-id="80c17-238">(<=) Lægra en eða jafnt og</span><span class="sxs-lookup"><span data-stu-id="80c17-238">(<=) Less than or equal to</span></span>  

|<span data-ttu-id="80c17-239">Dæmi</span><span class="sxs-lookup"><span data-stu-id="80c17-239">Sample Expression</span></span>|<span data-ttu-id="80c17-240">Sýndar færslur</span><span class="sxs-lookup"><span data-stu-id="80c17-240">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`<=1200`|<span data-ttu-id="80c17-241">Tölur lægri en eða jafnar 1200</span><span class="sxs-lookup"><span data-stu-id="80c17-241">Numbers less than or equal to 1200</span></span>|  

### <a name="-and"></a><span data-ttu-id="80c17-242">(&) Og</span><span class="sxs-lookup"><span data-stu-id="80c17-242">(&) And</span></span>  

|<span data-ttu-id="80c17-243">Dæmi</span><span class="sxs-lookup"><span data-stu-id="80c17-243">Sample Expression</span></span>|<span data-ttu-id="80c17-244">Sýndar færslur</span><span class="sxs-lookup"><span data-stu-id="80c17-244">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`>200&<1200`|<span data-ttu-id="80c17-245">Tölur hærri en 200 og minni en 1200</span><span class="sxs-lookup"><span data-stu-id="80c17-245">Numbers greater than 200 and less than 1200</span></span>|  

### <a name="-an-exact-character-match"></a><span data-ttu-id="80c17-246">('') Nákvæm stafasamsvörun</span><span class="sxs-lookup"><span data-stu-id="80c17-246">('') An exact character match</span></span>  

|<span data-ttu-id="80c17-247">Dæmi</span><span class="sxs-lookup"><span data-stu-id="80c17-247">Sample Expression</span></span>|<span data-ttu-id="80c17-248">Sýndar færslur</span><span class="sxs-lookup"><span data-stu-id="80c17-248">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`'man'`|<span data-ttu-id="80c17-249">Texta sem passar nákvæmlega við Man og er stafréttur.</span><span class="sxs-lookup"><span data-stu-id="80c17-249">Text that matches man exactly and is case sensitive.</span></span>|  

### <a name="-case-insensitive"></a><span data-ttu-id="80c17-250">(@) Stafrétt</span><span class="sxs-lookup"><span data-stu-id="80c17-250">(@) Case insensitive</span></span>  

|<span data-ttu-id="80c17-251">Dæmi</span><span class="sxs-lookup"><span data-stu-id="80c17-251">Sample Expression</span></span>|<span data-ttu-id="80c17-252">Sýndar færslur</span><span class="sxs-lookup"><span data-stu-id="80c17-252">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`@man*`|<span data-ttu-id="80c17-253">Texti sem byrjar á Man og er ekki stafréttur.</span><span class="sxs-lookup"><span data-stu-id="80c17-253">Text that starts with man and is case insensitive.</span></span>|  

### <a name="-an-indefinite-number-of-unknown-characters"></a><span data-ttu-id="80c17-254">(\*) Ótilgreindur fjöldi óþekktra staftákna</span><span class="sxs-lookup"><span data-stu-id="80c17-254">(\*) An indefinite number of unknown characters</span></span>

|<span data-ttu-id="80c17-255">Dæmi</span><span class="sxs-lookup"><span data-stu-id="80c17-255">Sample Expression</span></span>|<span data-ttu-id="80c17-256">Sýndar færslur</span><span class="sxs-lookup"><span data-stu-id="80c17-256">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`*Co*`|<span data-ttu-id="80c17-257">Texta sem inniheldur „Co“  og er stafréttur.</span><span class="sxs-lookup"><span data-stu-id="80c17-257">Text that contains "Co" and is case sensitive.</span></span>|  
|`*Co`|<span data-ttu-id="80c17-258">Texta sem endar á „Co“  og er stafréttur.</span><span class="sxs-lookup"><span data-stu-id="80c17-258">Text that ends with "Co" and is case sensitive.</span></span>|  
|`Co*`|<span data-ttu-id="80c17-259">Texta sem byrjar á „Co“  og er stafréttur.</span><span class="sxs-lookup"><span data-stu-id="80c17-259">Text that begins with "Co" and is case sensitive.</span></span>|  

> [!NOTE]  
>   <span data-ttu-id="80c17-260">Þú getur ekki notað `*` þegar þú ert að sía á valkostum (tölusetning) reitum, svo sem **Staða** reitinn á sölupöntunum.</span><span class="sxs-lookup"><span data-stu-id="80c17-260">You cannot use `*` when filtering on option (enumeration) fields, such as the **Status** field on sales orders.</span></span> <span data-ttu-id="80c17-261">Til að færa inn afmörkun fyrir þessa gerð reits, er hægt að færa inn númeragildið sem afmörkunarbreytu.</span><span class="sxs-lookup"><span data-stu-id="80c17-261">To enter a filter for this type of field, you can enter the numeric value as a filtering parameter.</span></span> <span data-ttu-id="80c17-262">Til dæmis, í **Staða** reitinn á sölupöntun sem hefur gildin **Opna**, **Sleppt**, **Bíður eftir samþykki** og **Bíður eftir fyrirframgreiðslu**, skal nota gildin `0`, `1`, `2` og `3` til að sía fyrir þessar valkostir.</span><span class="sxs-lookup"><span data-stu-id="80c17-262">For example, in the **Status** field on a sales order that has the values **Open**, **Released**, **Pending Approval**, and **Pending Prepayment**, use the values `0`, `1`, `2`, and `3` to filter for these options.</span></span>

### <a name="-one-unknown-character"></a><span data-ttu-id="80c17-263">(?) eitt óþekkt stafatákn</span><span class="sxs-lookup"><span data-stu-id="80c17-263">(?) One unknown character</span></span>  

|<span data-ttu-id="80c17-264">Dæmi</span><span class="sxs-lookup"><span data-stu-id="80c17-264">Sample Expression</span></span>|<span data-ttu-id="80c17-265">Sýndar færslur</span><span class="sxs-lookup"><span data-stu-id="80c17-265">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`Hans?n`|<span data-ttu-id="80c17-266">Texti eins og Hansen eða Hanson</span><span class="sxs-lookup"><span data-stu-id="80c17-266">Text such as Hansen or Hanson</span></span>|  

### <a name="combined-format-expressions"></a><span data-ttu-id="80c17-267">Sameinað framsetningarsnið</span><span class="sxs-lookup"><span data-stu-id="80c17-267">Combined format expressions</span></span>  

|<span data-ttu-id="80c17-268">Dæmi</span><span class="sxs-lookup"><span data-stu-id="80c17-268">Sample Expression</span></span>|<span data-ttu-id="80c17-269">Sýndar færslur</span><span class="sxs-lookup"><span data-stu-id="80c17-269">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|<span data-ttu-id="80c17-270">„5999</span><span class="sxs-lookup"><span data-stu-id="80c17-270">\`5999</span></span>|<span data-ttu-id="80c17-271">8100..8490“</span><span class="sxs-lookup"><span data-stu-id="80c17-271">8100..8490\`</span></span>|<span data-ttu-id="80c17-272">Allar færslur með tölunni 5999 eða tölu á bilinu frá 8100 til og með 8490 er teknar með.</span><span class="sxs-lookup"><span data-stu-id="80c17-272">Include any records with the number 5999 or a number from the interval 8100 through 8490.</span></span>|  
|<span data-ttu-id="80c17-273">„.1299</span><span class="sxs-lookup"><span data-stu-id="80c17-273">\`..1299</span></span>|<span data-ttu-id="80c17-274">1400 ..“</span><span class="sxs-lookup"><span data-stu-id="80c17-274">1400..\`</span></span>|<span data-ttu-id="80c17-275">Telja með færslur með tölu sem er lægri eða jöfn 1299 eða tölu sem er jöfn 1400 eða hærri (allar tölur nema 1300 til 1399).</span><span class="sxs-lookup"><span data-stu-id="80c17-275">Include records with a number less than or equal to 1299 or a number equal to 1400 or greater (all numbers except 1300 through 1399).</span></span>|  
|`>50&<100`|<span data-ttu-id="80c17-276">Telja með færslur með tölum sem eru hærri en 50 og lægri en 100 (tölurnar 51 til 99).</span><span class="sxs-lookup"><span data-stu-id="80c17-276">Include records with numbers that are greater than 50 and less than 100 (numbers 51 through 99).</span></span>|  


## <span data-ttu-id="80c17-277"><a name="FilterTokens"> </a>Síumerki</span><span class="sxs-lookup"><span data-stu-id="80c17-277"><a name="FilterTokens"> </a>Filter tokens</span></span>
<span data-ttu-id="80c17-278">Þegar þú slærð inn síuviðmiðanir getur þú einnig skrifað orð sem hafa sérstaka þýðingu, sem kallast síumerki.</span><span class="sxs-lookup"><span data-stu-id="80c17-278">When entering filter criteria, you can also type words that have special meaning, called filter tokens.</span></span> <span data-ttu-id="80c17-279">Eftir að hafa slegið inn merkiorðið, er orðinu skipt út fyrir gildin sem það táknar.</span><span class="sxs-lookup"><span data-stu-id="80c17-279">After entering the token word, the word is replaced by the value or values that it represents.</span></span> <span data-ttu-id="80c17-280">Þetta gerir síun auðveldara með því að draga úr þörfinni á að fara yfir á aðrar síðum til að fletta upp gildi sem þú vilt bæta við síuna.</span><span class="sxs-lookup"><span data-stu-id="80c17-280">This makes filtering easier by reducing the need to navigate to other pages to look up values you want to add to your filter.</span></span> <span data-ttu-id="80c17-281">Taflan hér fyrir neðan lýsir sumum merkjunum sem þú getur slegið inn sem síuviðmiðanir.</span><span class="sxs-lookup"><span data-stu-id="80c17-281">The tables below describe some of the tokens you can type as filter criteria.</span></span>

> [!TIP]
> <span data-ttu-id="80c17-282">Stofnunin þín getur notað sérsniðna merki.</span><span class="sxs-lookup"><span data-stu-id="80c17-282">Your organization may use custom tokens.</span></span> <span data-ttu-id="80c17-283">Til að læra um öll merkin sem þú hefur aðgang að eða til að bæta við fleiri sérsniðnum merkjum, skaltu tala við stjórnandann þinn.</span><span class="sxs-lookup"><span data-stu-id="80c17-283">To learn about the complete set of tokens available to you or to add more custom tokens, talk to your administrator.</span></span> <span data-ttu-id="80c17-284">Fyrir tæknilegar upplýsingar, sjá [Bæta við síumerkjum](/dynamics365/business-central/dev-itpro/developer/devenv-adding-filter-tokens)</span><span class="sxs-lookup"><span data-stu-id="80c17-284">For technical information see [Adding Filter Tokens](/dynamics365/business-central/dev-itpro/developer/devenv-adding-filter-tokens)</span></span>


### <a name="me-or-userid-records-assigned-to-you"></a><span data-ttu-id="80c17-285">(%me eða %userid) Skrám úthlutað til þín</span><span class="sxs-lookup"><span data-stu-id="80c17-285">(%me or %userid) Records assigned to you</span></span>

<span data-ttu-id="80c17-286">Notaðu `%me` eða `%userid` þegar verið er að sía reiti sem innihalda notandakenni, svo sem **úthlutað til notandakennis** reit, til að birta allar skrár sem eru úthlutað til þín.</span><span class="sxs-lookup"><span data-stu-id="80c17-286">Use `%me` or `%userid` when filtering fields that contain the user ID, such as **Assigned to User ID** field, to display all records that are assigned to you.</span></span>

|<span data-ttu-id="80c17-287">Dæmi</span><span class="sxs-lookup"><span data-stu-id="80c17-287">Sample Expression</span></span>|<span data-ttu-id="80c17-288">Sýndar færslur</span><span class="sxs-lookup"><span data-stu-id="80c17-288">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`%me`<br /><span data-ttu-id="80c17-289">eða</span><span class="sxs-lookup"><span data-stu-id="80c17-289">or</span></span><br />`%userid`|<span data-ttu-id="80c17-290">Skrár sem eru úthlutað á notandareikninginn þinn.</span><span class="sxs-lookup"><span data-stu-id="80c17-290">Records the are assigned to your user account.</span></span> |  

### <a name="mycustomers-customers-in-my-customers"></a><span data-ttu-id="80c17-291">(%mycustomers) Viðskiptamenn í Mínir viðskiptamenn</span><span class="sxs-lookup"><span data-stu-id="80c17-291">(%mycustomers) Customers in My Customers</span></span>

<span data-ttu-id="80c17-292">Notaðu `%mycustomers` í **Nr** reitnum viðskiptamanns til að birta allar skrár fyrir viðskiptamenn sem eru innifaldir í **Mínir viðskiptamenn** listanum á Mitt hlutverk.</span><span class="sxs-lookup"><span data-stu-id="80c17-292">Use `%mycustomers` in the customer **No** field to display all records for customers that are included in the **My Customers** list on your Role Center.</span></span>

|<span data-ttu-id="80c17-293">Dæmi</span><span class="sxs-lookup"><span data-stu-id="80c17-293">Sample Expression</span></span>|<span data-ttu-id="80c17-294">Sýndar færslur</span><span class="sxs-lookup"><span data-stu-id="80c17-294">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`%mycustomers`|<span data-ttu-id="80c17-295">Viðskiptamenn í **Mínir viðskiptamenn** í Mitt hlutverk.</span><span class="sxs-lookup"><span data-stu-id="80c17-295">Customers in the **My Customers** on your Role Center.</span></span> |  

### <a name="myitems-items-in-my-items"></a><span data-ttu-id="80c17-296">(%mytems) Atriði í Mínum atriðum</span><span class="sxs-lookup"><span data-stu-id="80c17-296">(%myitems) Items in My Items</span></span>

<span data-ttu-id="80c17-297">Notaðu `%myitems` Í atriði **Nr** reitinn til að birta allar skrár fyrir atriði sem eru innifalin í **Mín atriði** listanum í Mitt hlutverk.</span><span class="sxs-lookup"><span data-stu-id="80c17-297">Use `%myitems` in the item **No** field to display all records for items that are included in the **My Items** list on your Role Center.</span></span>

|<span data-ttu-id="80c17-298">Dæmi</span><span class="sxs-lookup"><span data-stu-id="80c17-298">Sample Expression</span></span>|<span data-ttu-id="80c17-299">Sýndar færslur</span><span class="sxs-lookup"><span data-stu-id="80c17-299">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`%myitems`|<span data-ttu-id="80c17-300">Atriði í **Mín atriði** í Mitt hlutverk.</span><span class="sxs-lookup"><span data-stu-id="80c17-300">Items in the **My Items** on your Role Center.</span></span> |  

### <a name="myvendors-vendors-in-my-vendors"></a><span data-ttu-id="80c17-301">(%myvendors) Lánardrottnar í Mínir lánardrottnar</span><span class="sxs-lookup"><span data-stu-id="80c17-301">(%myvendors) Vendors in My Vendors</span></span>

<span data-ttu-id="80c17-302">Notaðu `%myvendors` í lánardrottinn **Nr** reitnum, til að birta allar skrá fyrir lánardrottna sem eru innifalin í **Mínir lánardrottnar** listanum í Mitt hlutverk.</span><span class="sxs-lookup"><span data-stu-id="80c17-302">Use `%myvendors` in the vendor **No** field to display all records for vendors that are included in the **My Vendors** list on your Role Center.</span></span>

|<span data-ttu-id="80c17-303">Dæmi</span><span class="sxs-lookup"><span data-stu-id="80c17-303">Sample Expression</span></span>|<span data-ttu-id="80c17-304">Sýndar færslur</span><span class="sxs-lookup"><span data-stu-id="80c17-304">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`%myvendors`|<span data-ttu-id="80c17-305">Lánardrottnar í **Mínir lánardrottnar** í Mitt hlutverk.</span><span class="sxs-lookup"><span data-stu-id="80c17-305">Venders in the **My Vendors** on your Role Center.</span></span> |  


## <a name="see-also"></a><span data-ttu-id="80c17-306">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="80c17-306">See Also</span></span>
<span data-ttu-id="80c17-307">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="80c17-307">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="80c17-308">Algengar spurningar um leit og síun</span><span class="sxs-lookup"><span data-stu-id="80c17-308">Common questions about Searching and Filtering</span></span>](ui-search-filter-faq.md)

