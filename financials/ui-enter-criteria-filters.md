---
title: "Skilgreina leitarskilyrði í afmörkunum | Microsoft Docs"
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
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 86ca45493081d9dbd229548f7c560e1df4e1c7c3
ms.contentlocale: is-is
ms.lasthandoff: 09/11/2017

---
# <a name="entering-criteria-in-filters"></a><span data-ttu-id="d0513-103">Afmörkun skjalanna</span><span class="sxs-lookup"><span data-stu-id="d0513-103">Entering Criteria in Filters</span></span>
<span data-ttu-id="d0513-104">Til að leita að gögnum, svo sem heiti viðskiptamanna, aðsetrum eða vöruhópum er hægt að setja inn skilyrði.</span><span class="sxs-lookup"><span data-stu-id="d0513-104">When you want to search for data, such as customer names, addresses, or product groups, you enter criteria.</span></span> <span data-ttu-id="d0513-105">Í leitarskilyrðum er hægt að nota alla sömu tölustafi og bókstafi sem venjulega eru notaðir í reitnum.</span><span class="sxs-lookup"><span data-stu-id="d0513-105">In search criteria you can use all the numbers and letters that you normally use in the specific field.</span></span> <span data-ttu-id="d0513-106">Ennfremur er hægt að nota sértákn til að afmarka niðurstöðurnar frekar.</span><span class="sxs-lookup"><span data-stu-id="d0513-106">In addition, you can use special symbols to further filter the results.</span></span>

## <a name="searching-using-the-quick-filter"></a><span data-ttu-id="d0513-107">Leita með því að nota flýtiafmörkun</span><span class="sxs-lookup"><span data-stu-id="d0513-107">Searching using the Quick Filter</span></span>
<span data-ttu-id="d0513-108">Hægt er að bæta afmörkunum við allar síður með því að nota flýtiafmörkun.</span><span class="sxs-lookup"><span data-stu-id="d0513-108">You can add filters to all pages by using the Quick Filter.</span></span> <span data-ttu-id="d0513-109">Flýtiafmörkun er virkjuð með því að velja stækkunarglerstáknið í efra hægra horni síðu.</span><span class="sxs-lookup"><span data-stu-id="d0513-109">The Quick Filter is enabled by choosing the magnifier icon in the top right corner of a page.</span></span> <span data-ttu-id="d0513-110">Þessi síugerð er notuð fyrir flýtiinnfærslu viðmiða.</span><span class="sxs-lookup"><span data-stu-id="d0513-110">This filtering type is used for a fast entry of criteria.</span></span>

> [!IMPORTANT]  
>   <span data-ttu-id="d0513-111">Flýtiafmörkun veitir auðveldan aðgang að afmörkunargögnum með því að færa inn texta án sniðtákna en veitir einnig margs konar valkosti fyrir leitarskilyrði.</span><span class="sxs-lookup"><span data-stu-id="d0513-111">The Quick Filter provides an easy access to filter data by entering plain text, but does also provide a lot of search criteria options.</span></span> <span data-ttu-id="d0513-112">Það fer eftir því hvort þú slærð texta eða texta með táknum, flýtiafmörkun hagar sér öðruvísi.</span><span class="sxs-lookup"><span data-stu-id="d0513-112">Depending on whether you enter plain text or text including symbols, the Quick Filter behaves differently.</span></span>  

* <span data-ttu-id="d0513-113">Ef ósniðinn texti er sleginn inn í leitarskilyrðum eru leitarskilyrðin túlkuð sem leit óháð há- og lágstöfum sem inniheldur ákveðinn texta.</span><span class="sxs-lookup"><span data-stu-id="d0513-113">If you enter plain text in the search criteria, the search criteria is interpreted as a case insensitive search that contains certain text.</span></span>  
* <span data-ttu-id="d0513-114">Ef texti með táknum er sleginn inn í leitarskilyrðum eru leitarskilyrðin túlkuð nákvæmlega eins og þau voru slegin inn og leitin er háð há- og lágstöfum.</span><span class="sxs-lookup"><span data-stu-id="d0513-114">If you enter text including symbols in the search criteria, the search criteria is interpreted exactly as you entered it, and the search is case sensitive.</span></span>

### <a name="quick-filter-criteria"></a><span data-ttu-id="d0513-115">Skilyrði flýtiafmörkunar</span><span class="sxs-lookup"><span data-stu-id="d0513-115">Quick filter criteria</span></span>
<!-- html syntax because symbols conflict with MarkDown syntax -->
<TABLE>
  <TR>
    <TH><span data-ttu-id="d0513-116">Leitarskilyrði</span><span class="sxs-lookup"><span data-stu-id="d0513-116">Search Criteria</span></span></TH>
    <TH><span data-ttu-id="d0513-117">Túlkað sem...</span><span class="sxs-lookup"><span data-stu-id="d0513-117">Interpreted as...</span></span></TH>
    <TH><span data-ttu-id="d0513-118">Vöruskil...</span><span class="sxs-lookup"><span data-stu-id="d0513-118">Returns...</span></span></TH>
  </TR>
  <TR>
    <TD><span data-ttu-id="d0513-119">man</span><span class="sxs-lookup"><span data-stu-id="d0513-119">man</span></span></TD>
    <TD><span data-ttu-id="d0513-120">@&#42;man&#42;</span><span class="sxs-lookup"><span data-stu-id="d0513-120">@&#42;man&#42;</span></span></TD>
    <TD><span data-ttu-id="d0513-121">Allar færslur þurfa að innihalda textann <b>man</b> og rétta há- og lágstafi.</span><span class="sxs-lookup"><span data-stu-id="d0513-121">All records that contain the text <b>man</b> and case insensitive.</span></span></TD>
  </TR>
  <TR>
    <TD><span data-ttu-id="d0513-122">se</span><span class="sxs-lookup"><span data-stu-id="d0513-122">se</span></span></TD>
    <TD><span data-ttu-id="d0513-123">@&#42;se&#42;</span><span class="sxs-lookup"><span data-stu-id="d0513-123">@&#42;se&#42;</span></span></TD>
    <TD><span data-ttu-id="d0513-124">Allar færslur þurfa að innihalda textann <b>se</b> og rétta há- og lágstafi.</span><span class="sxs-lookup"><span data-stu-id="d0513-124">All records that contain the text <b>se</b> and case insensitive.</span></span></TD>
  </TR>
  <TR>
    <TD><span data-ttu-id="d0513-125">Man&#42;</span><span class="sxs-lookup"><span data-stu-id="d0513-125">Man&#42;</span></span></TD>
    <TD><span data-ttu-id="d0513-126">Hefst á <b>Man</b> og greinarmunur á litlum og stórum stöfum.</span><span class="sxs-lookup"><span data-stu-id="d0513-126">Starts with <b>Man</b> and case sensitive.</span></span></TD>
    <TD><span data-ttu-id="d0513-127">Allar færslur sem byrja á textanum <b>Man</b></span><span class="sxs-lookup"><span data-stu-id="d0513-127">All records that start with the text <b>Man</b>.</span></span></TD>
  </TR>
  <TR>
    <TD><span data-ttu-id="d0513-128">‚man‘</span><span class="sxs-lookup"><span data-stu-id="d0513-128">'man'</span></span></TD>
    <TD><span data-ttu-id="d0513-129">Nákvæmur texti og greinarmunur á litlum og stórum stöfum.</span><span class="sxs-lookup"><span data-stu-id="d0513-129">An exact text and case sensitive.</span></span></TD>
    <TD><span data-ttu-id="d0513-130">Allar færslur sem samsvara <b>man</b> nákvæmlega.</span><span class="sxs-lookup"><span data-stu-id="d0513-130">All records that match <b>man</b> exactly.</span></span></TD>
  </TR>
  <TR>
    <TD><span data-ttu-id="d0513-131">@man*</span><span class="sxs-lookup"><span data-stu-id="d0513-131">@man*</span></span> </TD>
    <TD><span data-ttu-id="d0513-132">Hefst á og enginn greinarmunur á litlum og stórum stöfum.</span><span class="sxs-lookup"><span data-stu-id="d0513-132">Starts with and case insensitive.</span></span></TD>
    <TD><span data-ttu-id="d0513-133">Allar færslur sem byrja á <b>man</b>.</span><span class="sxs-lookup"><span data-stu-id="d0513-133">All records that start with <b>man</b>.</span></span></TD>
  </TR>
    <TR>
    <TD><span data-ttu-id="d0513-134">@&#42;man</span><span class="sxs-lookup"><span data-stu-id="d0513-134">@&#42;man</span></span></TD>
    <TD><span data-ttu-id="d0513-135">Lýkur á og enginn greinarmunur á litlum og stórum stöfum.</span><span class="sxs-lookup"><span data-stu-id="d0513-135">Ends with and case insensitive.</span></span></TD>
    <TD><span data-ttu-id="d0513-136">Allar færslur sem enda á <b>man</b>.</span><span class="sxs-lookup"><span data-stu-id="d0513-136">All records that end with <b>man</b>.</span></span></TD>
  </TR>
</TABLE>

> [!NOTE]  
>   <span data-ttu-id="d0513-137">Ekki er hægt að nota algildisstafi þegar afmarkanir eru á tölusettum reitum, til dæmis reiturinn **Staða** á sölupöntunum.</span><span class="sxs-lookup"><span data-stu-id="d0513-137">You cannot use a wildcard when filtering on enumeration fields, such as the **Status** field on sales orders.</span></span> <span data-ttu-id="d0513-138">Til að færa inn afmörkun fyrir þessa gerð reits, er hægt að færa inn númeragildið sem afmörkunarbreytu.</span><span class="sxs-lookup"><span data-stu-id="d0513-138">To enter a filter for this type of field, you can enter the numeric value as a filtering parameter.</span></span> <span data-ttu-id="d0513-139">Til dæmis í reitnum **Sala** á sölupöntun sem hafa gildin **Opin**, **Útgefið**, **Samþykkt í bið** og **Fyrirframgreiðsla í bið** skal nota gildin **0**, **1**, **2** og **3** til þess að afmarka þessa valmöguleika.</span><span class="sxs-lookup"><span data-stu-id="d0513-139">For example, in the **Status** field on a sales order that has the values **Open**, **Released**, **Pending Approval**, and **Pending Prepayment**, use the values **0**, **1**, **2**, and **3** to filter for these options.</span></span>  

## <a name="see-also"></a><span data-ttu-id="d0513-140">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="d0513-140">See Also</span></span>
<span data-ttu-id="d0513-141">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="d0513-141">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

