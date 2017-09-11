---
title: "Innkaup á vörum og þjónustu fyrir verk og stjórnun verkbirgða| Microsoft Docs"
description: "Lýsir því hvernig á að hafa umsjón með verkbirgðum og innkaupum á efni og þjónustu í verkum."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project management, material, purchase
ms.date: 06/06/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 46cae53022ba5d65a370694c9818f52a7bf45525
ms.contentlocale: is-is
ms.lasthandoff: 09/11/2017


---
# <a name="how-to-manage-job-supplies"></a><span data-ttu-id="54d06-103">Hvernig á að: Vinna með verkbirgðir</span><span class="sxs-lookup"><span data-stu-id="54d06-103">How to: Manage Job Supplies</span></span>
<span data-ttu-id="54d06-104">Það er mikilvægur og óaðskiljanlegur hluti af framkvæmd allra verka að hafa umsjón með framboði á vöru, þjónustu og útgjöldum.</span><span class="sxs-lookup"><span data-stu-id="54d06-104">Managing project supplies of items, services, and expenses is an integral and critical aspect of the execution of all jobs.</span></span> <span data-ttu-id="54d06-105">Nota má birgðamagn eða gera verktengd innkaup með innkaupapöntunum og/eða innkaupareikningum.</span><span class="sxs-lookup"><span data-stu-id="54d06-105">You can use inventory quantities or make job-specific purchases using purchase orders or purchase invoices.</span></span> <span data-ttu-id="54d06-106">Sem dæmi má nefna þjónustuverk á tölvu sem krefst þess að nýr diskur sé keyptur.</span><span class="sxs-lookup"><span data-stu-id="54d06-106">For example, a service job on a computer requires a new disk.</span></span> <span data-ttu-id="54d06-107">Þá er búinn til innkaupareikningur til kaupa á nýjum diski og verkið, sem nota á diskinn í, er skráð.</span><span class="sxs-lookup"><span data-stu-id="54d06-107">You create a purchase invoice to buy a new disk and record the job that it will be used on.</span></span>

<span data-ttu-id="54d06-108">Ef innkaupavinnslan krefst þess ekki að efnislegu viðskiptin séu skráð sérstaklega er hægt að vinna innkaup í glugganum **Fjárhagsbók verks**.</span><span class="sxs-lookup"><span data-stu-id="54d06-108">If the purchase process does not require that the physical transaction be recorded separately, then a purchase may be processed in the **Job G/L Journal** window.</span></span> <span data-ttu-id="54d06-109">Nánari upplýsingar eru í [Hvernig á að: Skrá notkun vegna verka](projects-how-record-job-usage.md).</span><span class="sxs-lookup"><span data-stu-id="54d06-109">For more information, see [How to: Record Usage for Jobs](projects-how-record-job-usage.md).</span></span>

## <a name="to-purchase-items-or-services-for-a-job"></a><span data-ttu-id="54d06-110">Að kaupa vörur eða þjónustu fyrir verk</span><span class="sxs-lookup"><span data-stu-id="54d06-110">To purchase items or services for a job</span></span>
<span data-ttu-id="54d06-111">Eftirfarandi ferli sýnir hvernig á að nota innkaupareikning til að kaupa vörur fyrir verk.</span><span class="sxs-lookup"><span data-stu-id="54d06-111">The following procedure shows how to use a purchase invoice to purchase products for a job.</span></span> <span data-ttu-id="54d06-112">Sömu skref eiga við þegar innkaupapöntun er notuð.</span><span class="sxs-lookup"><span data-stu-id="54d06-112">The same steps apply when using a purchase order.</span></span>  

1. <span data-ttu-id="54d06-113">Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Innkaupareikningar** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="54d06-113">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Purchase Invoices**, and then choose the related link.</span></span>  
2. <span data-ttu-id="54d06-114">Veljið aðgerðina **Nýtt** og fyllið svo út reitina eins og þörf krefur.</span><span class="sxs-lookup"><span data-stu-id="54d06-114">Choose the **New** action and fill in the fields as necessary.</span></span> <span data-ttu-id="54d06-115">Nánari upplýsingar eru í [Hvernig á að: Skrá innkaup](purchasing-how-record-purchases.md).</span><span class="sxs-lookup"><span data-stu-id="54d06-115">For more information, see [How to: Record Purchases](purchasing-how-record-purchases.md).</span></span>
3. <span data-ttu-id="54d06-116">Í reitina **Verknr.**</span><span class="sxs-lookup"><span data-stu-id="54d06-116">In the **Job No.**</span></span> <span data-ttu-id="54d06-117">og **Verkhlutanr.**</span><span class="sxs-lookup"><span data-stu-id="54d06-117">and **Job Task No.**</span></span> <span data-ttu-id="54d06-118">skal velja þær upplýsingar um verkið sem kaupa skal vörur eða þjónustu vegna.</span><span class="sxs-lookup"><span data-stu-id="54d06-118">fields, select the information of the job that you want to purchase items or services for.</span></span> <span data-ttu-id="54d06-119">Notaðu **Dálkaval** ef svæðið er ekki sýnilegt.</span><span class="sxs-lookup"><span data-stu-id="54d06-119">Use the **Choose Columns** function if the field is not visible.</span></span> <span data-ttu-id="54d06-120">Nánari upplýsingar er að finna í [Sérstillingar notanda](ui-user-personalization.md).</span><span class="sxs-lookup"><span data-stu-id="54d06-120">For more information, see [User Personalization](ui-user-personalization.md).</span></span>

    <span data-ttu-id="54d06-121">Gildið sem valið er í reitnum **Verklínutegund** skilgreinir hvort búin sé til áætlunarlína þegar notkun vörunnar er bókuð.</span><span class="sxs-lookup"><span data-stu-id="54d06-121">The value that you select in the **Job Line Type** field defines whether a planning line is created when you post the usage of the item.</span></span> <span data-ttu-id="54d06-122">Ef reiturinn inniheldur **Reikningshæft** eru stofnaðar áætlunarlínur sem eru tilbúnar til að vera reikningsfærðar til viðskiptavinar.</span><span class="sxs-lookup"><span data-stu-id="54d06-122">If the field contains **Billable**, then job planning lines that are ready to be invoiced to the customer are created.</span></span> <span data-ttu-id="54d06-123">Nánari upplýsingar eru í [Hvernig á að: Reikningsfæra verk](projects-how-invoice-jobs.md).</span><span class="sxs-lookup"><span data-stu-id="54d06-123">For more information, see [How to: Invoice Jobs](projects-how-invoice-jobs.md).</span></span>
4. <span data-ttu-id="54d06-124">Valið er **bóka** aðgerð.</span><span class="sxs-lookup"><span data-stu-id="54d06-124">Choose the **Post** action.</span></span>

## <a name="to-view-the-value-of-purchases-for-a-job"></a><span data-ttu-id="54d06-125">Til að skoða virði innkaupa fyrir verk</span><span class="sxs-lookup"><span data-stu-id="54d06-125">To view the value of purchases for a job</span></span>
1. <span data-ttu-id="54d06-126">Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Verk** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="54d06-126">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Jobs**, and then choose the related link.</span></span>
2. <span data-ttu-id="54d06-127">Opnið viðeigandi verkspjald.</span><span class="sxs-lookup"><span data-stu-id="54d06-127">Open a relevant job card.</span></span>

    <span data-ttu-id="54d06-128">Á flýtiflipanum **Verkhlutar** sýnir reiturinn **Óafgreiddar pantanir** útistandandi upphæð í staðbundnum gjaldmiðli fyrir vörur í birgðaskrá og þjónustu á innkaupaskjöl fyrir verkhlutalínuna.</span><span class="sxs-lookup"><span data-stu-id="54d06-128">On the **Tasks** FastTab, the **Outstanding Orders** field shows the total outstanding amount, in local currency, of inventory items and services on purchase documents for the job task line.</span></span>  

    <span data-ttu-id="54d06-129">Reiturinn **Afh. upph. óreikn.færð** sýnir virði vara sem afhentra vara í innkaupaskjölum sem ekki hafa verið reikningsfærðar enn.</span><span class="sxs-lookup"><span data-stu-id="54d06-129">The **Amt. Rec. Not Invoiced** field shows the value of items delivered on purchase documents, but not yet invoiced.</span></span>  
3. <span data-ttu-id="54d06-130">Veljið annan hvorn reitinn til að opna í glugganum **Innkaupalínur** þar sem hægt er að fara yfir upplýsingar um línur í tengdum innkaupaskjölum, þ.m.t. hvaða vörum eða þjónustu hefur verið tekið við.</span><span class="sxs-lookup"><span data-stu-id="54d06-130">Choose either of the fields to open the **Purchase Lines** window where you can review information about the related purchase document lines, including which items or services have been received.</span></span>

## <a name="to-post-a-job-related-expense"></a><span data-ttu-id="54d06-131">Til að bóka verktengdan kostnað</span><span class="sxs-lookup"><span data-stu-id="54d06-131">To post a job-related expense</span></span>
<span data-ttu-id="54d06-132">Ef um óeðlileg útgjöld eða einstök útgjöld er að ræða vegna verks er hægt að nota gluggann **Fjárhagsbók verks** til að bóka slíkt beint á reikning viðeigandi verks.</span><span class="sxs-lookup"><span data-stu-id="54d06-132">If you incur extraordinary or one-time job expenses, you can use the **Job G/L Journal** window to post them directly to the relevant job account.</span></span>

1. <span data-ttu-id="54d06-133">Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Fjárhagsbækur verks** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="54d06-133">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Job G/L Journals**, and then choose the related link.</span></span>  
2. <span data-ttu-id="54d06-134">Búa skal til nýja línu og slá inn upplýsingar um útgjöldin, þ.m.t. upplýsingar í reitina **Verknr.**</span><span class="sxs-lookup"><span data-stu-id="54d06-134">Create a new line and enter information about the expense, including information in the **Job No.**</span></span> <span data-ttu-id="54d06-135">og **Verkhlutanr.**</span><span class="sxs-lookup"><span data-stu-id="54d06-135">and **Job Task No** fields.</span></span>  
3. <span data-ttu-id="54d06-136">Þegar færslubókin er tilbúin skal velja aðgerðina **Bóka**.</span><span class="sxs-lookup"><span data-stu-id="54d06-136">When the journal is complete, choose the **Post** action.</span></span>

## <a name="see-also"></a><span data-ttu-id="54d06-137">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="54d06-137">See Also</span></span>
[<span data-ttu-id="54d06-138">Verkefnastjórnun</span><span class="sxs-lookup"><span data-stu-id="54d06-138">Project Management</span></span>](projects-manage-projects.md)  
[<span data-ttu-id="54d06-139">Fjármál</span><span class="sxs-lookup"><span data-stu-id="54d06-139">Finance</span></span>](finance.md)  
<span data-ttu-id="54d06-140">[Innkaup](purchasing-manage-purchasing.md)       </span><span class="sxs-lookup"><span data-stu-id="54d06-140">[Purchasing](purchasing-manage-purchasing.md)       </span></span>  
<span data-ttu-id="54d06-141">[Sala](sales-manage-sales.md)    </span><span class="sxs-lookup"><span data-stu-id="54d06-141">[Sales](sales-manage-sales.md)    </span></span>  
<span data-ttu-id="54d06-142">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="54d06-142">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

