---
title: "Innkaup á vörum og þjónustu fyrir verk og stjórnun verkbirgða| Microsoft Docs"
description: "Lýsir því hvernig á að hafa umsjón með verkbirgðum og innkaupum á efni og þjónustu í verkum."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project management, material, purchase
ms.date: 06/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 958439cc8faa62baa044fcfac160797d609323ad
ms.contentlocale: is-is
ms.lasthandoff: 03/22/2018

---
# <a name="manage-job-supplies"></a><span data-ttu-id="652aa-103">Stjórna verkbirgðum</span><span class="sxs-lookup"><span data-stu-id="652aa-103">Manage Job Supplies</span></span>
<span data-ttu-id="652aa-104">Það er mikilvægur og óaðskiljanlegur hluti af framkvæmd allra verka að hafa umsjón með framboði á vöru, þjónustu og útgjöldum.</span><span class="sxs-lookup"><span data-stu-id="652aa-104">Managing project supplies of items, services, and expenses is an integral and critical aspect of the execution of all jobs.</span></span> <span data-ttu-id="652aa-105">Nota má birgðamagn eða gera verktengd innkaup með innkaupapöntunum og/eða innkaupareikningum.</span><span class="sxs-lookup"><span data-stu-id="652aa-105">You can use inventory quantities or make job-specific purchases using purchase orders or purchase invoices.</span></span> <span data-ttu-id="652aa-106">Sem dæmi má nefna þjónustuverk á tölvu sem krefst þess að nýr diskur sé keyptur.</span><span class="sxs-lookup"><span data-stu-id="652aa-106">For example, a service job on a computer requires a new disk.</span></span> <span data-ttu-id="652aa-107">Þá er búinn til innkaupareikningur til kaupa á nýjum diski og verkið, sem nota á diskinn í, er skráð.</span><span class="sxs-lookup"><span data-stu-id="652aa-107">You create a purchase invoice to buy a new disk and record the job that it will be used on.</span></span>

<span data-ttu-id="652aa-108">Ef innkaupavinnslan krefst þess ekki að efnislegu viðskiptin séu skráð sérstaklega er hægt að vinna innkaup í glugganum **Fjárhagsbók verks**.</span><span class="sxs-lookup"><span data-stu-id="652aa-108">If the purchase process does not require that the physical transaction be recorded separately, then a purchase may be processed in the **Job G/L Journal** window.</span></span> <span data-ttu-id="652aa-109">Frekari upplýsingar eru í [Skrá notkun fyrir verk](projects-how-record-job-usage.md).</span><span class="sxs-lookup"><span data-stu-id="652aa-109">For more information, see [Record Usage for Jobs](projects-how-record-job-usage.md).</span></span>

## <a name="to-purchase-items-or-services-for-a-job"></a><span data-ttu-id="652aa-110">Að kaupa vörur eða þjónustu fyrir verk</span><span class="sxs-lookup"><span data-stu-id="652aa-110">To purchase items or services for a job</span></span>
<span data-ttu-id="652aa-111">Eftirfarandi ferli sýnir hvernig á að nota innkaupareikning til að kaupa vörur fyrir verk.</span><span class="sxs-lookup"><span data-stu-id="652aa-111">The following procedure shows how to use a purchase invoice to purchase products for a job.</span></span> <span data-ttu-id="652aa-112">Sömu skref eiga við þegar innkaupapöntun er notuð.</span><span class="sxs-lookup"><span data-stu-id="652aa-112">The same steps apply when using a purchase order.</span></span>  

1. <span data-ttu-id="652aa-113">Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Innkaupareikningar** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="652aa-113">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Purchase Invoices**, and then choose the related link.</span></span>  
2. <span data-ttu-id="652aa-114">Veljið aðgerðina **Nýtt** og fyllið svo út reitina eins og þörf krefur.</span><span class="sxs-lookup"><span data-stu-id="652aa-114">Choose the **New** action and fill in the fields as necessary.</span></span> <span data-ttu-id="652aa-115">Nánari upplýsingar eru í reitnum [Skrá innkaup](purchasing-how-record-purchases.md).</span><span class="sxs-lookup"><span data-stu-id="652aa-115">For more information, see [Record Purchases](purchasing-how-record-purchases.md).</span></span>
3. <span data-ttu-id="652aa-116">Í reitunum **Verk nr.** og **Verkhluti nr.** eru valdar upplýsingarnar um verkið sem þú vilt kaupa vörur eða þjónustu fyrir.</span><span class="sxs-lookup"><span data-stu-id="652aa-116">In the **Job No.** and **Job Task No.** fields, select the information of the job that you want to purchase items or services for.</span></span> <span data-ttu-id="652aa-117">Notaðu **Dálkaval** ef svæðið er ekki sýnilegt.</span><span class="sxs-lookup"><span data-stu-id="652aa-117">Use the **Choose Columns** function if the field is not visible.</span></span> <span data-ttu-id="652aa-118">Frekari upplýsingar eru í [Sérstilling vinnusvæðisins þíns](ui-personalization-user.md).</span><span class="sxs-lookup"><span data-stu-id="652aa-118">For more information, see [Personalizing Your Workspace](ui-personalization-user.md).</span></span>

    <span data-ttu-id="652aa-119">Gildið sem valið er í reitnum **Verklínutegund** skilgreinir hvort búin sé til áætlunarlína þegar notkun vörunnar er bókuð.</span><span class="sxs-lookup"><span data-stu-id="652aa-119">The value that you select in the **Job Line Type** field defines whether a planning line is created when you post the usage of the item.</span></span> <span data-ttu-id="652aa-120">Ef reiturinn inniheldur **Reikningshæft** eru stofnaðar áætlunarlínur sem eru tilbúnar til að vera reikningsfærðar til viðskiptavinar.</span><span class="sxs-lookup"><span data-stu-id="652aa-120">If the field contains **Billable**, then job planning lines that are ready to be invoiced to the customer are created.</span></span> <span data-ttu-id="652aa-121">Frekari upplýsingar eru í [Reikningsfærsla verka](projects-how-invoice-jobs.md).</span><span class="sxs-lookup"><span data-stu-id="652aa-121">For more information, see [Invoice Jobs](projects-how-invoice-jobs.md).</span></span>
4. <span data-ttu-id="652aa-122">Valið er **Bóka** aðgerðin.</span><span class="sxs-lookup"><span data-stu-id="652aa-122">Choose the **Post** action.</span></span>

## <a name="to-view-the-value-of-purchases-for-a-job"></a><span data-ttu-id="652aa-123">Til að skoða virði innkaupa fyrir verk</span><span class="sxs-lookup"><span data-stu-id="652aa-123">To view the value of purchases for a job</span></span>
1. <span data-ttu-id="652aa-124">Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Verk** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="652aa-124">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Jobs**, and then choose the related link.</span></span>
2. <span data-ttu-id="652aa-125">Opnið viðeigandi verkspjald.</span><span class="sxs-lookup"><span data-stu-id="652aa-125">Open a relevant job card.</span></span>

    <span data-ttu-id="652aa-126">Á flýtiflipanum **Verkhlutar** sýnir reiturinn **Óafgreiddar pantanir** útistandandi upphæð í staðbundnum gjaldmiðli fyrir vörur í birgðaskrá og þjónustu á innkaupaskjöl fyrir verkhlutalínuna.</span><span class="sxs-lookup"><span data-stu-id="652aa-126">On the **Tasks** FastTab, the **Outstanding Orders** field shows the total outstanding amount, in local currency, of inventory items and services on purchase documents for the job task line.</span></span>  

    <span data-ttu-id="652aa-127">Reiturinn **Afh. upph. óreikn.færð** sýnir virði vara sem afhentra vara í innkaupaskjölum sem ekki hafa verið reikningsfærðar enn.</span><span class="sxs-lookup"><span data-stu-id="652aa-127">The **Amt. Rec. Not Invoiced** field shows the value of items delivered on purchase documents, but not yet invoiced.</span></span>  
3. <span data-ttu-id="652aa-128">Veljið annan hvorn reitinn til að opna í glugganum **Innkaupalínur** þar sem hægt er að fara yfir upplýsingar um línur í tengdum innkaupaskjölum, þ.m.t. hvaða vörum eða þjónustu hefur verið tekið við.</span><span class="sxs-lookup"><span data-stu-id="652aa-128">Choose either of the fields to open the **Purchase Lines** window where you can review information about the related purchase document lines, including which items or services have been received.</span></span>

## <a name="to-post-a-job-related-expense"></a><span data-ttu-id="652aa-129">Til að bóka verktengdan kostnað</span><span class="sxs-lookup"><span data-stu-id="652aa-129">To post a job-related expense</span></span>
<span data-ttu-id="652aa-130">Ef um óeðlileg útgjöld eða einstök útgjöld er að ræða vegna verks er hægt að nota gluggann **Fjárhagsbók verks** til að bóka slíkt beint á reikning viðeigandi verks.</span><span class="sxs-lookup"><span data-stu-id="652aa-130">If you incur extraordinary or one-time job expenses, you can use the **Job G/L Journal** window to post them directly to the relevant job account.</span></span>

1. <span data-ttu-id="652aa-131">Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Fjárhagsbækur verks** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="652aa-131">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Job G/L Journals**, and then choose the related link.</span></span>  
2. <span data-ttu-id="652aa-132">Ný lína er stofnuð og kostnaðarupplýsingar, þar á meðal **Verk nr** og **Verkhluti nr.**, færðar inn í reitina.</span><span class="sxs-lookup"><span data-stu-id="652aa-132">Create a new line and enter information about the expense, including information in the **Job No.** and **Job Task No** fields.</span></span>  
3. <span data-ttu-id="652aa-133">Þegar færslubókin er tilbúin skal velja aðgerðina **Bóka**.</span><span class="sxs-lookup"><span data-stu-id="652aa-133">When the journal is complete, choose the **Post** action.</span></span>

## <a name="see-also"></a><span data-ttu-id="652aa-134">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="652aa-134">See Also</span></span>
[<span data-ttu-id="652aa-135">Verkefnastjórnun</span><span class="sxs-lookup"><span data-stu-id="652aa-135">Project Management</span></span>](projects-manage-projects.md)  
[<span data-ttu-id="652aa-136">Fjármál</span><span class="sxs-lookup"><span data-stu-id="652aa-136">Finance</span></span>](finance.md)  
<span data-ttu-id="652aa-137">[Innkaup](purchasing-manage-purchasing.md)       </span><span class="sxs-lookup"><span data-stu-id="652aa-137">[Purchasing](purchasing-manage-purchasing.md)       </span></span>  
<span data-ttu-id="652aa-138">[Sala](sales-manage-sales.md)    </span><span class="sxs-lookup"><span data-stu-id="652aa-138">[Sales](sales-manage-sales.md)    </span></span>  
<span data-ttu-id="652aa-139">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="652aa-139">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

