---
title: "Skráning 1099 færslna í Bandaríkjunum | Microsoft Docs"
description: "Skattayfirvöld Bandaríkjanna krefjast 1099 skattaskýrslunnar fyrir greiðslur til lánardrottna og þú getur tilgreint að innkaupaskjal gildi fyrir 1099 og tilgreint 1099 kóðann fyrir lánardrottinn."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: local
ms.date: 03/29/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: c20c52927aa979e56aeef7975fbcee1564ca4dd7
ms.contentlocale: is-is
ms.lasthandoff: 09/11/2017

---
# <a name="reporting-transactions-as-1099-liable-in-the-us"></a><span data-ttu-id="80e49-103">Skráning færslna sem gilda fyrir 1099 í Bandaríkjunum</span><span class="sxs-lookup"><span data-stu-id="80e49-103">Reporting Transactions as 1099 Liable in the US</span></span>

<span data-ttu-id="80e49-104">Skattstofan krefst einnar eða fleiri útgáfa af 1099 skattaskýrslunni fyrir greiðslur til lánardrottna.</span><span class="sxs-lookup"><span data-stu-id="80e49-104">The Internal Revenue Service (IRS) requires one or more versions of the 1099 tax form for payments to vendors.</span></span> <span data-ttu-id="80e49-105">Senda verður afrit af þessum eyðublöðum til lánardrottna árlega á eða fyrir síðasta dag janúar.</span><span class="sxs-lookup"><span data-stu-id="80e49-105">Copies of these forms must be sent to vendors annually on or before the last day of January.</span></span> <span data-ttu-id="80e49-106">Á innkaupaskjölunum er hægt að tilgreina að skjalið gildi fyrir 1099 og hægt er að tilgreina 1099-kóðann fyrir lánardrottinninn.</span><span class="sxs-lookup"><span data-stu-id="80e49-106">On your purchase documents, you can specify that the document is 1099 liable, and you can specify the 1099 code for the vendor.</span></span>  

## <a name="1099-codes"></a><span data-ttu-id="80e49-107">1099-kóðar</span><span class="sxs-lookup"><span data-stu-id="80e49-107">1099 codes</span></span>
<span data-ttu-id="80e49-108">Í [!INCLUDE[d365fin](includes/d365fin_md.md)] eru algengustu 1099 númerin nú þegar sett upp fyrir þig svo þú ert tilbúin til að búa til nauðsynlegar skýrslur.</span><span class="sxs-lookup"><span data-stu-id="80e49-108">In [!INCLUDE[d365fin](includes/d365fin_md.md)], the most common 1099 codes are already set up for you so you are ready to generate the required reports.</span></span> <span data-ttu-id="80e49-109">Kóðarnir eru skilgreindir í glugganum **Eyðublaðsreitur IRS 1099** þar sem einnig er hægt að bæta við nýjum 1099-kóðum.</span><span class="sxs-lookup"><span data-stu-id="80e49-109">The codes are defined in the **IRS 1099 Form Box** window where you can also add new 1099 codes.</span></span> <span data-ttu-id="80e49-110">Fyrir hvern lánardrottin sem standa þarf skil á sköttum er svo hægt að tilgreina viðeigandi 1099-kóða á flýtiflipanum **Greiðslur** á spjaldi lánardrottinsins.</span><span class="sxs-lookup"><span data-stu-id="80e49-110">For each tax liable vendor, you can then specify the relevant 1099 code on the **Payments** FastTab on the Vendor card.</span></span>  

<span data-ttu-id="80e49-111">Með skýrslunni **1099-upplýsingar lánardrottins** er hægt að skoða 1099-færslur sem voru greiddar á tilteknum tíma.</span><span class="sxs-lookup"><span data-stu-id="80e49-111">With the **Vendor 1099 Information** report, you can review 1099 transactions paid during a specified period.</span></span> <span data-ttu-id="80e49-112">Við lok ársins er hægt að prenta 1099-færslur á forprentuðum eyðublöðum.</span><span class="sxs-lookup"><span data-stu-id="80e49-112">At the end of the year, you can print 1099 transactions on preprinted forms.</span></span>  

## <a name="printing-1099-tax-forms"></a><span data-ttu-id="80e49-113">Prentun 1099-skattaskýrslna</span><span class="sxs-lookup"><span data-stu-id="80e49-113">Printing 1099 tax forms</span></span>
<span data-ttu-id="80e49-114">Í glugganum **Eyðublaðsreitur IRS 1099** fæst aðgangur að eftirfarandi skattaskýrslum:</span><span class="sxs-lookup"><span data-stu-id="80e49-114">From the **IRS 1099 Form Box** window, you can access the following tax forms:</span></span>  

* <span data-ttu-id="80e49-115">Lánardrottinn 1099 Div</span><span class="sxs-lookup"><span data-stu-id="80e49-115">Vendor 1099 Div</span></span>  

  <span data-ttu-id="80e49-116">Prentar landsbundna eyðublaðið 1099-DIV fyrir arðgreiðslur og útgreiðslu.</span><span class="sxs-lookup"><span data-stu-id="80e49-116">Prints the federal form 1099-DIV for dividends and distribution.</span></span> <span data-ttu-id="80e49-117">Hægt er að prenta út öll eða tilgreind 1099-DIV eyðublöð.</span><span class="sxs-lookup"><span data-stu-id="80e49-117">You can print all or specific 1099-DIV forms.</span></span> <span data-ttu-id="80e49-118">Skýrslan notar kóðana sem gilda um upphæðareitina á DIV-eyðublaðinu úr glugganum **Eyðublaðsreitur IRS 1099**.</span><span class="sxs-lookup"><span data-stu-id="80e49-118">The report uses the codes that apply to the DIV form amount boxes from the **IRS 1099 Form-Box** window.</span></span>  
* <span data-ttu-id="80e49-119">Lánardrottinn 1099 Int</span><span class="sxs-lookup"><span data-stu-id="80e49-119">Vendor 1099 Int</span></span>  

  <span data-ttu-id="80e49-120">Prentar landsbundna eyðublaðið 1099-INT fyrir vaxtatekjur.</span><span class="sxs-lookup"><span data-stu-id="80e49-120">Prints the federal form 1099-INT for interest income.</span></span> <span data-ttu-id="80e49-121">Hægt er að prenta út öll eða tilgreind 1099-INT eyðublöð.</span><span class="sxs-lookup"><span data-stu-id="80e49-121">You can print all or specific 1099-INT forms.</span></span> <span data-ttu-id="80e49-122">Skýrslan notar kóðana sem gilda um upphæðareitina á INT-eyðublaðinu úr glugganum **Eyðublaðsreitur IRS 1099**.</span><span class="sxs-lookup"><span data-stu-id="80e49-122">The report uses the codes that apply to the INT form amount boxes from the **IRS 1099 Form-Box** window.</span></span>  
* <span data-ttu-id="80e49-123">Lánardrottinn 1099 Misc – ýmsar tekjur</span><span class="sxs-lookup"><span data-stu-id="80e49-123">Vendor 1099 Misc - Miscellaneous income</span></span>  

  <span data-ttu-id="80e49-124">Prentar landsbundna eyðublaðið 1099-MISC fyrir ýmsar tekjur.</span><span class="sxs-lookup"><span data-stu-id="80e49-124">Prints the federal form 1099-MISC for miscellaneous income.</span></span> <span data-ttu-id="80e49-125">Hægt er að prenta út öll eða tilgreind 1099-MISC eyðublöð.</span><span class="sxs-lookup"><span data-stu-id="80e49-125">You can print all or specific 1099-MISC forms.</span></span> <span data-ttu-id="80e49-126">Skýrslan notar kóðana sem gilda um upphæðareitina á MISC-eyðublaðinu úr glugganum **Eyðublaðsreitur IRS 1099**.</span><span class="sxs-lookup"><span data-stu-id="80e49-126">The report uses the codes that apply to the MISC form amount boxes from the **IRS 1099 Form-Box** window.</span></span>  

<span data-ttu-id="80e49-127">Stjórnsýslubreytingar sem hafa áhrif á þessa skýrslu og töflugögn eru almennt meðhöndluð í árslokauppfærslum.</span><span class="sxs-lookup"><span data-stu-id="80e49-127">Regulatory changes affecting this report and the table data are generally handled in end-of-year updates.</span></span>
<span data-ttu-id="80e49-128">Það getur komið að gagni að keyra skýrsluna **1099-upplýsingar lánardrottins** til að fara yfir gögnin áður en eyðublöðin eru prentuð út.</span><span class="sxs-lookup"><span data-stu-id="80e49-128">It may be helpful to run the **Vendor 1099 Information** report to review the data before printing the forms.</span></span>

## <a name="submitting-1099-tax-forms-electronically"></a><span data-ttu-id="80e49-129">1099-skattaskýrslur lagðar fram rafrænt</span><span class="sxs-lookup"><span data-stu-id="80e49-129">Submitting 1099 tax forms electronically</span></span>
<span data-ttu-id="80e49-130">Til að leggja fram 1099-skattaskýrslurnar rafrænt skal nota skýrsluna **1099-segulmiðlun lánardrottins**.</span><span class="sxs-lookup"><span data-stu-id="80e49-130">To submit the 1099 tax forms electronically, use the **Vendor 1099 Magnetic Media** report.</span></span> <span data-ttu-id="80e49-131">Tilgreinir 1099-eyðublöðin sem hægt er að flytja út.</span><span class="sxs-lookup"><span data-stu-id="80e49-131">Specifies the 1099 forms that can be exported.</span></span> <span data-ttu-id="80e49-132">Eyðublaðaupplýsingarnar sem eru fluttar út í þessari skýrslu eru þær sömu og í skýrslunum sem prenta 1099-eyðublöð sem er lýst í fyrri hluta.</span><span class="sxs-lookup"><span data-stu-id="80e49-132">The form information exported by this report is the same as the reports that print 1099 forms that are described in the previous section.</span></span>  

<span data-ttu-id="80e49-133">Skýrslan notar kóðana sem gilda um upphæðareitina á eyðublaðinu úr glugganum **Eyðublaðsreitur IRS 1099**.</span><span class="sxs-lookup"><span data-stu-id="80e49-133">The report uses the codes that apply to the form amount boxes from the **IRS 1099 Form-Box** window.</span></span> <span data-ttu-id="80e49-134">Kóðunum er varpað í eyðublaðsreitina í skráarútlitum þessarar skýrslu og því verða töflugögnin og skýrsluútgáfan fyrir tiltekið skattaár að passa saman.</span><span class="sxs-lookup"><span data-stu-id="80e49-134">The codes are mapped to the form boxes in the file layouts of this report, therefore the table data and report version for a particular tax year must be in agreement.</span></span> <span data-ttu-id="80e49-135">Ef einhverjum sérsniðnum kóðum er bætt við töfluna verður að varpa þeim í eyðublaðsreitina inni í þessum hlut.</span><span class="sxs-lookup"><span data-stu-id="80e49-135">If any custom codes are added to the table these must be mapped to the form boxes inside this object.</span></span>  

<span data-ttu-id="80e49-136">Stjórnsýslubreytingar sem hafa áhrif á þessa skýrslu og töflugögn eru almennt meðhöndluð í árslokauppfærslum.</span><span class="sxs-lookup"><span data-stu-id="80e49-136">Regulatory changes affecting this report and the table data are generally handled in end-of-year updates.</span></span>
<span data-ttu-id="80e49-137">Það getur komið að gagni að keyra skýrsluna **1099-upplýsingar lánardrottins** til að fara yfir gögnin áður en rafræna skráin er mynduð.</span><span class="sxs-lookup"><span data-stu-id="80e49-137">It may be helpful to run the **Vendor 1099 Information** report to review the data before generating the electronic file.</span></span>  

## <a name="see-also"></a><span data-ttu-id="80e49-138">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="80e49-138">See Also</span></span>
[<span data-ttu-id="80e49-139">Hvernig á að skrá nýja lánardrottna</span><span class="sxs-lookup"><span data-stu-id="80e49-139">How to: Register New Vendors</span></span>](purchasing-how-register-new-vendors.md)  
[<span data-ttu-id="80e49-140">Hvernig á að skrá innkaup</span><span class="sxs-lookup"><span data-stu-id="80e49-140">How to: Record Purchase</span></span>](purchasing-how-record-purchases.md)  
<span data-ttu-id="80e49-141">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="80e49-141">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

