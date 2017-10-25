---
title: "Leita í gögnum og færa inn afmörkunarviðmið | Microsoft Docs"
description: "Lýsir því hvernig vinna skal með afmarkanir, eins og Flýtiafmörkun, til að sérstilla leitarniðurstöðurnar."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: delimit, FlowFilter
ms.date: 03/29/2017
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 11d7ef56e980ba263dba6328b2f2f08b86410242
ms.contentlocale: is-is
ms.lasthandoff: 09/22/2017

---
# <a name="searching-filtering-and-sorting-data"></a><span data-ttu-id="8f3eb-103">Leita í, afmarka og raða gögnum</span><span class="sxs-lookup"><span data-stu-id="8f3eb-103">Searching, Filtering, and Sorting Data</span></span>
<span data-ttu-id="8f3eb-104">Það eru nokkrir hlutir sem þú getur gert sem mun hjálpa þér að finna, ákvarða nákvæmlega, og skanna skrár í lista.</span><span class="sxs-lookup"><span data-stu-id="8f3eb-104">There are a few things that you can do that will help you find, pinpoint, and scan records in a list.</span></span> <span data-ttu-id="8f3eb-105">Þar á meðal er röðun, leit og afmörkun.</span><span class="sxs-lookup"><span data-stu-id="8f3eb-105">These include sorting, searching and filtering.</span></span>

<span data-ttu-id="8f3eb-106">Til að leita að gögnum, svo sem heiti viðskiptamanna, aðsetrum eða vöruhópum er hægt að setja inn skilyrði.</span><span class="sxs-lookup"><span data-stu-id="8f3eb-106">When you want to search for data, such as customer names, addresses, or product groups, you enter criteria.</span></span> <span data-ttu-id="8f3eb-107">Í leitarskilyrðum er hægt að nota alla sömu tölustafi og bókstafi sem venjulega eru notaðir í reitnum.</span><span class="sxs-lookup"><span data-stu-id="8f3eb-107">In search criteria you can use all the numbers and letters that you normally use in the specific field.</span></span> <span data-ttu-id="8f3eb-108">Ennfremur er hægt að nota sértákn til að afmarka niðurstöðurnar frekar.</span><span class="sxs-lookup"><span data-stu-id="8f3eb-108">In addition, you can use special symbols to further filter the results.</span></span> <span data-ttu-id="8f3eb-109">Tvær leiðir til að leita: nota flýtiafmörkun eða dálkaafmörkun.</span><span class="sxs-lookup"><span data-stu-id="8f3eb-109">There are two ways to search: using the Quick Filter or column filters.</span></span>

## <a name="sorting"></a><span data-ttu-id="8f3eb-110">Röðun</span><span class="sxs-lookup"><span data-stu-id="8f3eb-110">Sorting</span></span>
<span data-ttu-id="8f3eb-111">Með Röðun er auðvelt og fljótlegt að fá yfirsýn yfir gögnin.</span><span class="sxs-lookup"><span data-stu-id="8f3eb-111">Sorting makes it easy for you to get a quick overview of your data.</span></span> <span data-ttu-id="8f3eb-112">Ef þú ert með marga viðskiptamenn til dæmis, er hægt að velja að raða þeim eftir **númeri Viðskiptamanns**, **Bókunarflokkum viðskiptavinar**, **Gjaldmiðilskóði**, **LandsSvæðiskóða**, eða **skráningarnúmer Söluskatts** til að fá það yfirlit sem þú þarft.</span><span class="sxs-lookup"><span data-stu-id="8f3eb-112">If you have many customers, for example, you can choose to sort them by **Customer No.**, **Customer Posting Group**, **Currency Code**, **Country Region Code**, or **Sales Tax Registration No.** to get the overview you need.</span></span>

<span data-ttu-id="8f3eb-113">Til að raða á lista, getur annað hvort valið fyrirsagnatexta dálka til að skipta á milli hækkandi og lækkandi pöntunar, eða valið litlu örina í dálkafyrirsögninni, og síðan valið **Hækkandi** eða **Lækkandi**.</span><span class="sxs-lookup"><span data-stu-id="8f3eb-113">To sort a list, you can either choose a column heading text to toggle between ascending and descending order, or choose the small downs arrow in the column heading, and then choose **Ascending** or **Descending**.</span></span>  

> [!NOTE]  
>   <span data-ttu-id="8f3eb-114">Röðun er ekki studd myndir, BLOB-reitir, FlowFilters og reitir sem tilheyra ekki töflu.</span><span class="sxs-lookup"><span data-stu-id="8f3eb-114">Sorting is not supported images, BLOB fields, FlowFilters, and fields that do not belong to a table.</span></span>  

## <a name="searching-by-using-the-quick-filter"></a><span data-ttu-id="8f3eb-115">Leita með því að nota flýtiafmörkun</span><span class="sxs-lookup"><span data-stu-id="8f3eb-115">Searching by using the Quick Filter</span></span>
<span data-ttu-id="8f3eb-116">Hægt er að bæta afmörkunum við allar síður með því að nota flýtiafmörkun.</span><span class="sxs-lookup"><span data-stu-id="8f3eb-116">You can add filters to all pages by using the Quick Filter.</span></span> <span data-ttu-id="8f3eb-117">Flýtiafmörkun er virkjuð með því að velja stækkunarglerstáknið í efra hægra horni síðu.</span><span class="sxs-lookup"><span data-stu-id="8f3eb-117">The Quick Filter is enabled by choosing the magnifier icon in the top right corner of a page.</span></span> <span data-ttu-id="8f3eb-118">Þessi síugerð er notuð fyrir flýtiinnfærslu viðmiða.</span><span class="sxs-lookup"><span data-stu-id="8f3eb-118">This filtering type is used for a fast entry of criteria.</span></span>

> [!IMPORTANT]  
>   <span data-ttu-id="8f3eb-119">Flýtiafmörkun veitir auðveldan aðgang að afmörkunargögnum með því að færa inn texta án sniðtákna en veitir einnig margs konar valkosti fyrir leitarskilyrði.</span><span class="sxs-lookup"><span data-stu-id="8f3eb-119">The Quick Filter provides an easy access to filter data by entering plain text, but does also provide a lot of search criteria options.</span></span> <span data-ttu-id="8f3eb-120">Það fer eftir því hvort þú slærð texta eða texta með táknum, flýtiafmörkun hagar sér öðruvísi.</span><span class="sxs-lookup"><span data-stu-id="8f3eb-120">Depending on whether you enter plain text or text including symbols, the Quick Filter behaves differently.</span></span>  

* <span data-ttu-id="8f3eb-121">Ef ósniðinn texti er sleginn inn í leitarskilyrðum eru leitarskilyrðin túlkuð sem leit óháð há- og lágstöfum sem inniheldur ákveðinn texta.</span><span class="sxs-lookup"><span data-stu-id="8f3eb-121">If you enter plain text in the search criteria, the search criteria is interpreted as a case insensitive search that contains certain text.</span></span>  
* <span data-ttu-id="8f3eb-122">Ef texti með táknum er sleginn inn í leitarskilyrðum eru leitarskilyrðin túlkuð nákvæmlega eins og þau voru slegin inn og leitin er háð há- og lágstöfum.</span><span class="sxs-lookup"><span data-stu-id="8f3eb-122">If you enter text including symbols in the search criteria, the search criteria is interpreted exactly as you entered it, and the search is case sensitive.</span></span>

### <a name="quick-filter-criteria"></a><span data-ttu-id="8f3eb-123">Skilyrði flýtiafmörkunar</span><span class="sxs-lookup"><span data-stu-id="8f3eb-123">Quick filter criteria</span></span>
<!-- html syntax because symbols conflict with MarkDown syntax -->
<TABLE>
  <TR>
    <TH><span data-ttu-id="8f3eb-124">Leitarskilyrði</span><span class="sxs-lookup"><span data-stu-id="8f3eb-124">Search Criteria</span></span></TH>
    <TH><span data-ttu-id="8f3eb-125">Túlkað sem...</span><span class="sxs-lookup"><span data-stu-id="8f3eb-125">Interpreted as...</span></span></TH>
    <TH><span data-ttu-id="8f3eb-126">Vöruskil...</span><span class="sxs-lookup"><span data-stu-id="8f3eb-126">Returns...</span></span></TH>
  </TR>
  <TR>
    <TD><span data-ttu-id="8f3eb-127">man</span><span class="sxs-lookup"><span data-stu-id="8f3eb-127">man</span></span></TD>
    <TD><span data-ttu-id="8f3eb-128">@&#42;man&#42;</span><span class="sxs-lookup"><span data-stu-id="8f3eb-128">@&#42;man&#42;</span></span></TD>
    <TD><span data-ttu-id="8f3eb-129">Allar færslur þurfa að innihalda textann <b>man</b> og rétta há- og lágstafi.</span><span class="sxs-lookup"><span data-stu-id="8f3eb-129">All records that contain the text <b>man</b> and case insensitive.</span></span></TD>
  </TR>
  <TR>
    <TD><span data-ttu-id="8f3eb-130">se</span><span class="sxs-lookup"><span data-stu-id="8f3eb-130">se</span></span></TD>
    <TD><span data-ttu-id="8f3eb-131">@&#42;se&#42;</span><span class="sxs-lookup"><span data-stu-id="8f3eb-131">@&#42;se&#42;</span></span></TD>
    <TD><span data-ttu-id="8f3eb-132">Allar færslur þurfa að innihalda textann <b>se</b> og rétta há- og lágstafi.</span><span class="sxs-lookup"><span data-stu-id="8f3eb-132">All records that contain the text <b>se</b> and case insensitive.</span></span></TD>
  </TR>
  <TR>
    <TD><span data-ttu-id="8f3eb-133">Man&#42;</span><span class="sxs-lookup"><span data-stu-id="8f3eb-133">Man&#42;</span></span></TD>
    <TD><span data-ttu-id="8f3eb-134">Hefst á <b>Man</b> og greinarmunur á litlum og stórum stöfum.</span><span class="sxs-lookup"><span data-stu-id="8f3eb-134">Starts with <b>Man</b> and case sensitive.</span></span></TD>
    <TD><span data-ttu-id="8f3eb-135">Allar færslur sem byrja á textanum <b>Man</b></span><span class="sxs-lookup"><span data-stu-id="8f3eb-135">All records that start with the text <b>Man</b>.</span></span></TD>
  </TR>
  <TR>
    <TD><span data-ttu-id="8f3eb-136">‚man‘</span><span class="sxs-lookup"><span data-stu-id="8f3eb-136">'man'</span></span></TD>
    <TD><span data-ttu-id="8f3eb-137">Nákvæmur texti og greinarmunur á litlum og stórum stöfum.</span><span class="sxs-lookup"><span data-stu-id="8f3eb-137">An exact text and case sensitive.</span></span></TD>
    <TD><span data-ttu-id="8f3eb-138">Allar færslur sem samsvara <b>man</b> nákvæmlega.</span><span class="sxs-lookup"><span data-stu-id="8f3eb-138">All records that match <b>man</b> exactly.</span></span></TD>
  </TR>
  <TR>
    <TD><span data-ttu-id="8f3eb-139">@man*</span><span class="sxs-lookup"><span data-stu-id="8f3eb-139">@man*</span></span> </TD>
    <TD><span data-ttu-id="8f3eb-140">Hefst á og enginn greinarmunur á litlum og stórum stöfum.</span><span class="sxs-lookup"><span data-stu-id="8f3eb-140">Starts with and case insensitive.</span></span></TD>
    <TD><span data-ttu-id="8f3eb-141">Allar færslur sem byrja á <b>man</b>.</span><span class="sxs-lookup"><span data-stu-id="8f3eb-141">All records that start with <b>man</b>.</span></span></TD>
  </TR>
    <TR>
    <TD><span data-ttu-id="8f3eb-142">@&#42;man</span><span class="sxs-lookup"><span data-stu-id="8f3eb-142">@&#42;man</span></span></TD>
    <TD><span data-ttu-id="8f3eb-143">Lýkur á og enginn greinarmunur á litlum og stórum stöfum.</span><span class="sxs-lookup"><span data-stu-id="8f3eb-143">Ends with and case insensitive.</span></span></TD>
    <TD><span data-ttu-id="8f3eb-144">Allar færslur sem enda á <b>man</b>.</span><span class="sxs-lookup"><span data-stu-id="8f3eb-144">All records that end with <b>man</b>.</span></span></TD>
  </TR>
</TABLE>

> [!NOTE]  
>   <span data-ttu-id="8f3eb-145">Ekki er hægt að nota algildisstafi þegar afmarkanir eru á tölusettum reitum, til dæmis reiturinn **Staða** á sölupöntunum.</span><span class="sxs-lookup"><span data-stu-id="8f3eb-145">You cannot use a wildcard when filtering on enumeration fields, such as the **Status** field on sales orders.</span></span> <span data-ttu-id="8f3eb-146">Til að færa inn afmörkun fyrir þessa gerð reits, er hægt að færa inn númeragildið sem afmörkunarbreytu.</span><span class="sxs-lookup"><span data-stu-id="8f3eb-146">To enter a filter for this type of field, you can enter the numeric value as a filtering parameter.</span></span> <span data-ttu-id="8f3eb-147">Til dæmis í reitnum **Sala** á sölupöntun sem hafa gildin **Opin**, **Útgefið**, **Samþykkt í bið** og **Fyrirframgreiðsla í bið** skal nota gildin **0**, **1**, **2** og **3** til þess að afmarka þessa valmöguleika.</span><span class="sxs-lookup"><span data-stu-id="8f3eb-147">For example, in the **Status** field on a sales order that has the values **Open**, **Released**, **Pending Approval**, and **Pending Prepayment**, use the values **0**, **1**, **2**, and **3** to filter for these options.</span></span> 

## <a name="searching-by-using-column-filters"></a><span data-ttu-id="8f3eb-148">Leita með því að nota dálkaafmörkun</span><span class="sxs-lookup"><span data-stu-id="8f3eb-148">Searching by using column Filters</span></span>
<span data-ttu-id="8f3eb-149">Hægt er að bæta við afmörkunum á einn eða fleiri dálka í lista.</span><span class="sxs-lookup"><span data-stu-id="8f3eb-149">You can add a filter on one or more columns in a list.</span></span> <span data-ttu-id="8f3eb-150">Afmörkun dálka er sveigjanlegri og meiri en flýtiafmörkunin</span><span class="sxs-lookup"><span data-stu-id="8f3eb-150">Filtering on columns is more flexible and enhanced than the Quick Filter.</span></span> 

### <a name="to-add-a-filter-on-a-column"></a><span data-ttu-id="8f3eb-151">Bæta afmörkun á dálk</span><span class="sxs-lookup"><span data-stu-id="8f3eb-151">To add a filter on a column</span></span>
1.  <span data-ttu-id="8f3eb-152">Áður en þú bætir við afmörkun, skal velja ![Sýna sem lista](media/ui_show_as_list_icon.png "Sýna sem lista ör vinstri") tákn til að breyta yfir í skoðun lista.</span><span class="sxs-lookup"><span data-stu-id="8f3eb-152">Before you add a filter, choose ![Show as list](media/ui_show_as_list_icon.png "Show as list arrow left") icon to change to the list view.</span></span>
2. <span data-ttu-id="8f3eb-153">Velja örina sem vísar niður í fyrirsögn dálksins og velja síðan **Afmörkun**.</span><span class="sxs-lookup"><span data-stu-id="8f3eb-153">Choose the downwards arrow in the column heading, and then choose **Filter**.</span></span>
3. <span data-ttu-id="8f3eb-154">Gert er eitt af eftirfarandi:</span><span class="sxs-lookup"><span data-stu-id="8f3eb-154">Do one of the following:</span></span> 
  -  <span data-ttu-id="8f3eb-155">Velja *...* næst boxinu til að velja gildi úr lista.</span><span class="sxs-lookup"><span data-stu-id="8f3eb-155">Choose *...* next to the box to select a value from a list.</span></span>
  -  <span data-ttu-id="8f3eb-156">Færið inn afmörkunarviðmið í boxið.</span><span class="sxs-lookup"><span data-stu-id="8f3eb-156">Enter filter criteria in the box.</span></span> <span data-ttu-id="8f3eb-157">Sjá næsta hluta til að fá upplýsingar.</span><span class="sxs-lookup"><span data-stu-id="8f3eb-157">See the next section for details.</span></span>
4. <span data-ttu-id="8f3eb-158">Velja hnappinn **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="8f3eb-158">Choose the **OK** button.</span></span>

## <a name="filter-criteria-and-symbols"></a><span data-ttu-id="8f3eb-159">Afmörkunarviðmið og tákn</span><span class="sxs-lookup"><span data-stu-id="8f3eb-159">Filter criteria and symbols</span></span>
<span data-ttu-id="8f3eb-160">Þegar skilyrði eru sett er hægt að nota alla sömu tölustafi og bókstafi sem venjulega eru notaðir í reitnum.</span><span class="sxs-lookup"><span data-stu-id="8f3eb-160">When you enter criteria, you can use all the numbers and letters that you can normally use in the field.</span></span> <span data-ttu-id="8f3eb-161">Ennfremur er hægt að nota sértákn til að afmarka niðurstöðurnar frekar.</span><span class="sxs-lookup"><span data-stu-id="8f3eb-161">In addition, you can use special symbols to further filter the results.</span></span> <span data-ttu-id="8f3eb-162">Í eftirfarandi töflum eru táknin sem hægt er að nota í afmarkanir.</span><span class="sxs-lookup"><span data-stu-id="8f3eb-162">The following tables show the symbols which can be used in filters.</span></span>  
  
> [!IMPORTANT]  
>  <span data-ttu-id="8f3eb-163">Það geta verið tilvik þar sem gildi reita innihalda þessi tákn og þú vilt setja afmörkun á þau.</span><span class="sxs-lookup"><span data-stu-id="8f3eb-163">There may be instances where field values contain these symbols and you want to filter on them.</span></span> <span data-ttu-id="8f3eb-164">Til að gera það, verðurðu að hafa með afmörkunarsegðina sem inniheldur táknið með gæsalöppum („“).</span><span class="sxs-lookup"><span data-stu-id="8f3eb-164">To do this, you must include the filter expression that contains the symbol in quotation marks ('').</span></span> <span data-ttu-id="8f3eb-165">Ef þú vilt t.d. setja afmörkun á skrár sem byrja á textanum *S&R* er afmörkunarsegðin **„S&R*“**.</span><span class="sxs-lookup"><span data-stu-id="8f3eb-165">For example, if you want to filter on records that start with the text *S&R*, the filter expression is **'S&R*'**.</span></span>  
  
### <a name="-interval"></a><span data-ttu-id="8f3eb-166">(..) Bil</span><span class="sxs-lookup"><span data-stu-id="8f3eb-166">(..) Interval</span></span>  
  
|<span data-ttu-id="8f3eb-167">Dæmi</span><span class="sxs-lookup"><span data-stu-id="8f3eb-167">Sample Expression</span></span>|<span data-ttu-id="8f3eb-168">Sýndar færslur</span><span class="sxs-lookup"><span data-stu-id="8f3eb-168">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|<span data-ttu-id="8f3eb-169">1100..2100</span><span class="sxs-lookup"><span data-stu-id="8f3eb-169">1100..2100</span></span>|<span data-ttu-id="8f3eb-170">Tölur 1100 til 2100.</span><span class="sxs-lookup"><span data-stu-id="8f3eb-170">Numbers 1100 through 2100</span></span>|  
|<span data-ttu-id="8f3eb-171">..2500</span><span class="sxs-lookup"><span data-stu-id="8f3eb-171">..2500</span></span>|<span data-ttu-id="8f3eb-172">Reikningar til og með 2500</span><span class="sxs-lookup"><span data-stu-id="8f3eb-172">Up to and including 2500</span></span>|  
|<span data-ttu-id="8f3eb-173">..12 31 00</span><span class="sxs-lookup"><span data-stu-id="8f3eb-173">..12 31 00</span></span>|<span data-ttu-id="8f3eb-174">Dagsetningar til og með 31. 12. 00.</span><span class="sxs-lookup"><span data-stu-id="8f3eb-174">Dates up to and including 12 31 00</span></span>|  
|<span data-ttu-id="8f3eb-175">P8..</span><span class="sxs-lookup"><span data-stu-id="8f3eb-175">P8..</span></span>|<span data-ttu-id="8f3eb-176">Upplýsingar um reikningstímabil 8 og síðar.</span><span class="sxs-lookup"><span data-stu-id="8f3eb-176">Information for accounting period 8 and thereafter</span></span>|  
|<span data-ttu-id="8f3eb-177">..23</span><span class="sxs-lookup"><span data-stu-id="8f3eb-177">..23</span></span>|<span data-ttu-id="8f3eb-178">Frá upphafsdegi til 23. þessa mánaðar – þessa árs 23:59:59</span><span class="sxs-lookup"><span data-stu-id="8f3eb-178">From the beginning date until 23-current month-current year 23:59:59</span></span>|  
|<span data-ttu-id="8f3eb-179">23..</span><span class="sxs-lookup"><span data-stu-id="8f3eb-179">23..</span></span>|<span data-ttu-id="8f3eb-180">Frá 23. þessa mánaðar – þessa árs 00:00:00 til loka tímans</span><span class="sxs-lookup"><span data-stu-id="8f3eb-180">From 23-current month-current year 0:00:00 until the end of time</span></span>|  
|<span data-ttu-id="8f3eb-181">22..23</span><span class="sxs-lookup"><span data-stu-id="8f3eb-181">22..23</span></span>|<span data-ttu-id="8f3eb-182">Frá 22. þessa mánaðar – þessa árs 00:00:00 til 23. þessa mánaðar – þessa árs 23:59:59</span><span class="sxs-lookup"><span data-stu-id="8f3eb-182">From 22-current month-current year 0:00:00 until 23-current month-current year 23:59:59</span></span>|  
  
### <a name="124-eitheror"></a><span data-ttu-id="8f3eb-183">(&#124;) Annaðhvort/eða</span><span class="sxs-lookup"><span data-stu-id="8f3eb-183">(&#124;) Either/or</span></span>  
  
|<span data-ttu-id="8f3eb-184">Dæmi</span><span class="sxs-lookup"><span data-stu-id="8f3eb-184">Sample Expression</span></span>|<span data-ttu-id="8f3eb-185">Sýndar færslur</span><span class="sxs-lookup"><span data-stu-id="8f3eb-185">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|<span data-ttu-id="8f3eb-186">1200&#124;1300</span><span class="sxs-lookup"><span data-stu-id="8f3eb-186">1200&#124;1300</span></span>|<span data-ttu-id="8f3eb-187">Tölur með 1200 eða 1300</span><span class="sxs-lookup"><span data-stu-id="8f3eb-187">Numbers with 1200 or 1300</span></span>|  
  
### <a name="-not-equal-to"></a><span data-ttu-id="8f3eb-188">(<>) Ekki jafnt og</span><span class="sxs-lookup"><span data-stu-id="8f3eb-188">(<>) Not equal to</span></span>  
  
|<span data-ttu-id="8f3eb-189">Dæmi</span><span class="sxs-lookup"><span data-stu-id="8f3eb-189">Sample Expression</span></span>|<span data-ttu-id="8f3eb-190">Sýndar færslur</span><span class="sxs-lookup"><span data-stu-id="8f3eb-190">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|<span data-ttu-id="8f3eb-191"><>0</span><span class="sxs-lookup"><span data-stu-id="8f3eb-191"><>0</span></span>|<span data-ttu-id="8f3eb-192">Allar tölur aðrar en 0</span><span class="sxs-lookup"><span data-stu-id="8f3eb-192">All numbers except 0</span></span><br /><br /> <span data-ttu-id="8f3eb-193">Valkosturinn SQL Server býður upp á að sameina þetta tákn algildistákni.</span><span class="sxs-lookup"><span data-stu-id="8f3eb-193">The SQL Server Option allows you to combine this symbol with a wild card expression.</span></span> <span data-ttu-id="8f3eb-194">Til dæmis merkir <>A* ekki jafnt og neinn texti sem byrjar á stafnum A.</span><span class="sxs-lookup"><span data-stu-id="8f3eb-194">For example, <>A* meaning not equal to any text that starts with A.</span></span>|  
  
### <a name="-greater-than"></a><span data-ttu-id="8f3eb-195">(>) Meira en</span><span class="sxs-lookup"><span data-stu-id="8f3eb-195">(>) Greater than</span></span>  
  
|<span data-ttu-id="8f3eb-196">Dæmi</span><span class="sxs-lookup"><span data-stu-id="8f3eb-196">Sample Expression</span></span>|<span data-ttu-id="8f3eb-197">Sýndar færslur</span><span class="sxs-lookup"><span data-stu-id="8f3eb-197">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|<span data-ttu-id="8f3eb-198">>1200</span><span class="sxs-lookup"><span data-stu-id="8f3eb-198">>1200</span></span>|<span data-ttu-id="8f3eb-199">Tölur hærri en 1200</span><span class="sxs-lookup"><span data-stu-id="8f3eb-199">Numbers greater than 1200</span></span>|  
  
### <a name="-greater-than-or-equal-to"></a><span data-ttu-id="8f3eb-200">(>=) Hærra en eða jafnt og</span><span class="sxs-lookup"><span data-stu-id="8f3eb-200">(>=) Greater than or equal to</span></span>  
  
|<span data-ttu-id="8f3eb-201">Dæmi</span><span class="sxs-lookup"><span data-stu-id="8f3eb-201">Sample Expression</span></span>|<span data-ttu-id="8f3eb-202">Sýndar færslur</span><span class="sxs-lookup"><span data-stu-id="8f3eb-202">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|<span data-ttu-id="8f3eb-203">>=1200</span><span class="sxs-lookup"><span data-stu-id="8f3eb-203">>=1200</span></span>|<span data-ttu-id="8f3eb-204">Tölur hærri en eða jafnar 1200</span><span class="sxs-lookup"><span data-stu-id="8f3eb-204">Numbers greater than or equal to 1200</span></span>|  
  
### <a name="-less-than"></a><span data-ttu-id="8f3eb-205">(<) Minna en</span><span class="sxs-lookup"><span data-stu-id="8f3eb-205">(<) Less than</span></span>  
  
|<span data-ttu-id="8f3eb-206">Dæmi</span><span class="sxs-lookup"><span data-stu-id="8f3eb-206">Sample Expression</span></span>|<span data-ttu-id="8f3eb-207">Sýndar færslur</span><span class="sxs-lookup"><span data-stu-id="8f3eb-207">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|<span data-ttu-id="8f3eb-208"><1200</span><span class="sxs-lookup"><span data-stu-id="8f3eb-208"><1200</span></span>|<span data-ttu-id="8f3eb-209">Tölur lægri en 1200</span><span class="sxs-lookup"><span data-stu-id="8f3eb-209">Numbers less than 1200</span></span>|  
  
### <a name="-less-than-or-equal-to"></a><span data-ttu-id="8f3eb-210">(<=) Lægra en eða jafnt og</span><span class="sxs-lookup"><span data-stu-id="8f3eb-210">(<=) Less than or equal to</span></span>  
  
|<span data-ttu-id="8f3eb-211">Dæmi</span><span class="sxs-lookup"><span data-stu-id="8f3eb-211">Sample Expression</span></span>|<span data-ttu-id="8f3eb-212">Sýndar færslur</span><span class="sxs-lookup"><span data-stu-id="8f3eb-212">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|<span data-ttu-id="8f3eb-213"><=1200</span><span class="sxs-lookup"><span data-stu-id="8f3eb-213"><=1200</span></span>|<span data-ttu-id="8f3eb-214">Tölur lægri en eða jafnar 1200</span><span class="sxs-lookup"><span data-stu-id="8f3eb-214">Numbers less than or equal to 1200</span></span>|  
  
### <a name="-and"></a><span data-ttu-id="8f3eb-215">(&) Og</span><span class="sxs-lookup"><span data-stu-id="8f3eb-215">(&) And</span></span>  
  
|<span data-ttu-id="8f3eb-216">Dæmi</span><span class="sxs-lookup"><span data-stu-id="8f3eb-216">Sample Expression</span></span>|<span data-ttu-id="8f3eb-217">Sýndar færslur</span><span class="sxs-lookup"><span data-stu-id="8f3eb-217">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|<span data-ttu-id="8f3eb-218">>200&<1200</span><span class="sxs-lookup"><span data-stu-id="8f3eb-218">>200&<1200</span></span>|<span data-ttu-id="8f3eb-219">Tölur hærri en 200 og minni en 1200</span><span class="sxs-lookup"><span data-stu-id="8f3eb-219">Numbers greater than 200 and less than 1200</span></span>|  
  
### <a name="-an-exact-character-match"></a><span data-ttu-id="8f3eb-220">('') Nákvæm stafasamsvörun</span><span class="sxs-lookup"><span data-stu-id="8f3eb-220">('') An exact character match</span></span>  
  
|<span data-ttu-id="8f3eb-221">Dæmi</span><span class="sxs-lookup"><span data-stu-id="8f3eb-221">Sample Expression</span></span>|<span data-ttu-id="8f3eb-222">Sýndar færslur</span><span class="sxs-lookup"><span data-stu-id="8f3eb-222">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|<span data-ttu-id="8f3eb-223">‚man‘</span><span class="sxs-lookup"><span data-stu-id="8f3eb-223">'man'</span></span>|<span data-ttu-id="8f3eb-224">Texta sem passar nákvæmlega við Man og er stafréttur.</span><span class="sxs-lookup"><span data-stu-id="8f3eb-224">Text that matches man exactly and is case sensitive.</span></span>|  
  
### <a name="-case-insensitive"></a><span data-ttu-id="8f3eb-225">(@) Stafrétt</span><span class="sxs-lookup"><span data-stu-id="8f3eb-225">(@) Case insensitive</span></span>  
  
|<span data-ttu-id="8f3eb-226">Dæmi</span><span class="sxs-lookup"><span data-stu-id="8f3eb-226">Sample Expression</span></span>|<span data-ttu-id="8f3eb-227">Sýndar færslur</span><span class="sxs-lookup"><span data-stu-id="8f3eb-227">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|<span data-ttu-id="8f3eb-228">@man*</span><span class="sxs-lookup"><span data-stu-id="8f3eb-228">@man*</span></span>|<span data-ttu-id="8f3eb-229">Texti sem byrjar á Man og er ekki stafréttur.</span><span class="sxs-lookup"><span data-stu-id="8f3eb-229">Text that starts with man and is case insensitive.</span></span>|  
  
### <a name="-an-indefinite-number-of-unknown-characters"></a><span data-ttu-id="8f3eb-230">(*) Ótilgreindur fjöldi óþekktra staftákna</span><span class="sxs-lookup"><span data-stu-id="8f3eb-230">(*) An indefinite number of unknown characters</span></span>  
  
|<span data-ttu-id="8f3eb-231">Dæmi</span><span class="sxs-lookup"><span data-stu-id="8f3eb-231">Sample Expression</span></span>|<span data-ttu-id="8f3eb-232">Sýndar færslur</span><span class="sxs-lookup"><span data-stu-id="8f3eb-232">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|<span data-ttu-id="8f3eb-233">*Co*</span><span class="sxs-lookup"><span data-stu-id="8f3eb-233">*Co*</span></span>|<span data-ttu-id="8f3eb-234">Texta sem inniheldur „Co“  og er stafréttur.</span><span class="sxs-lookup"><span data-stu-id="8f3eb-234">Text that contains "Co" and is case sensitive.</span></span>|  
|<span data-ttu-id="8f3eb-235">*Ko</span><span class="sxs-lookup"><span data-stu-id="8f3eb-235">*Co</span></span>|<span data-ttu-id="8f3eb-236">Texta sem endar á „Co“  og er stafréttur.</span><span class="sxs-lookup"><span data-stu-id="8f3eb-236">Text that ends with "Co" and is case sensitive.</span></span>|  
|<span data-ttu-id="8f3eb-237">Ko*</span><span class="sxs-lookup"><span data-stu-id="8f3eb-237">Co*</span></span>|<span data-ttu-id="8f3eb-238">Texta sem byrjar á „Co“  og er stafréttur.</span><span class="sxs-lookup"><span data-stu-id="8f3eb-238">Text that begins with "Co" and is case sensitive.</span></span>|  
  
### <a name="-one-unknown-character"></a><span data-ttu-id="8f3eb-239">(?) eitt óþekkt stafatákn</span><span class="sxs-lookup"><span data-stu-id="8f3eb-239">(?) One unknown character</span></span>  
  
|<span data-ttu-id="8f3eb-240">Dæmi</span><span class="sxs-lookup"><span data-stu-id="8f3eb-240">Sample Expression</span></span>|<span data-ttu-id="8f3eb-241">Sýndar færslur</span><span class="sxs-lookup"><span data-stu-id="8f3eb-241">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|<span data-ttu-id="8f3eb-242">Hans?n</span><span class="sxs-lookup"><span data-stu-id="8f3eb-242">Hans?n</span></span>|<span data-ttu-id="8f3eb-243">Texti eins og Hansen eða Hanson</span><span class="sxs-lookup"><span data-stu-id="8f3eb-243">Text such as Hansen or Hanson</span></span>|  
  
### <a name="combined-format-expressions"></a><span data-ttu-id="8f3eb-244">Sameinað framsetningarsnið</span><span class="sxs-lookup"><span data-stu-id="8f3eb-244">Combined format expressions</span></span>  
  
|<span data-ttu-id="8f3eb-245">Dæmi</span><span class="sxs-lookup"><span data-stu-id="8f3eb-245">Sample Expression</span></span>|<span data-ttu-id="8f3eb-246">Sýndar færslur</span><span class="sxs-lookup"><span data-stu-id="8f3eb-246">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|<span data-ttu-id="8f3eb-247">5999&#124;8100..8490</span><span class="sxs-lookup"><span data-stu-id="8f3eb-247">5999&#124;8100..8490</span></span>|<span data-ttu-id="8f3eb-248">Allar færslur með tölunni 5999 eða tölu á bilinu frá 8100 til og með 8490 er teknar með.</span><span class="sxs-lookup"><span data-stu-id="8f3eb-248">Include any records with the number 5999 or a number from the interval 8100 through 8490.</span></span>|  
|<span data-ttu-id="8f3eb-249">.1299&#124;1400..</span><span class="sxs-lookup"><span data-stu-id="8f3eb-249">..1299&#124;1400..</span></span>|<span data-ttu-id="8f3eb-250">Telja með færslur með tölu sem er lægri eða jöfn 1299 eða tölu sem er jöfn 1400 eða hærri (allar tölur nema 1300 til 1399).</span><span class="sxs-lookup"><span data-stu-id="8f3eb-250">Include records with a number less than or equal to 1299 or a number equal to 1400 or greater (all numbers except 1300 through 1399).</span></span>|  
|<span data-ttu-id="8f3eb-251">>50&<100</span><span class="sxs-lookup"><span data-stu-id="8f3eb-251">>50&<100</span></span>|<span data-ttu-id="8f3eb-252">Telja með færslur með tölum sem eru hærri en 50 og lægri en 100 (tölurnar 51 til 99).</span><span class="sxs-lookup"><span data-stu-id="8f3eb-252">Include records with numbers that are greater than 50 and less than 100 (numbers 51 through 99).</span></span>|  
 
## <a name="see-also"></a><span data-ttu-id="8f3eb-253">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="8f3eb-253">See Also</span></span>
<span data-ttu-id="8f3eb-254">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="8f3eb-254">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

