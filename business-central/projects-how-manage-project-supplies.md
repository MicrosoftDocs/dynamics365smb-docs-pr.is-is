---
title: Innkaup á vörum og þjónustu fyrir verk og stjórnun verkbirgða| Microsoft Docs
description: Lýsir því hvernig á að hafa umsjón með verkbirgðum og innkaupum á efni og þjónustu í verkum.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project management, material, purchase
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: acf85015ead55bea4cec5af7577ff58ce3d77af7
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/09/2020
ms.locfileid: "3783883"
---
# <a name="manage-job-supplies"></a><span data-ttu-id="87b26-103">Stjórna verkbirgðum</span><span class="sxs-lookup"><span data-stu-id="87b26-103">Manage Job Supplies</span></span>
<span data-ttu-id="87b26-104">Það er mikilvægur og óaðskiljanlegur hluti af framkvæmd allra verka að hafa umsjón með framboði á vöru, þjónustu og útgjöldum.</span><span class="sxs-lookup"><span data-stu-id="87b26-104">Managing project supplies of items, services, and expenses is an integral and critical aspect of the execution of all jobs.</span></span> <span data-ttu-id="87b26-105">Nota má birgðamagn eða gera verktengd innkaup með innkaupapöntunum og/eða innkaupareikningum.</span><span class="sxs-lookup"><span data-stu-id="87b26-105">You can use inventory quantities or make job-specific purchases using purchase orders or purchase invoices.</span></span> <span data-ttu-id="87b26-106">Sem dæmi má nefna þjónustuverk á tölvu sem krefst þess að nýr diskur sé keyptur.</span><span class="sxs-lookup"><span data-stu-id="87b26-106">For example, a service job on a computer requires a new disk.</span></span> <span data-ttu-id="87b26-107">Þá er búinn til innkaupareikningur til kaupa á nýjum diski og verkið, sem nota á diskinn í, er skráð.</span><span class="sxs-lookup"><span data-stu-id="87b26-107">You create a purchase invoice to buy a new disk and record the job that it will be used on.</span></span>

<span data-ttu-id="87b26-108">Ef innkaupaferlið krefst þess ekki að efnisleg aðgerð sé skráð sérstaklega er hægt að setja innkaup á síðuna **Fjárhagsbók verks**.</span><span class="sxs-lookup"><span data-stu-id="87b26-108">If the purchase process does not require that the physical transaction be recorded separately, then a purchase may be processed on the **Job G/L Journal** page.</span></span> <span data-ttu-id="87b26-109">Frekari upplýsingar eru í [Skrá notkun fyrir verk](projects-how-record-job-usage.md).</span><span class="sxs-lookup"><span data-stu-id="87b26-109">For more information, see [Record Usage for Jobs](projects-how-record-job-usage.md).</span></span>

## <a name="to-purchase-items-or-services-for-a-job"></a><span data-ttu-id="87b26-110">Að kaupa vörur eða þjónustu fyrir verk</span><span class="sxs-lookup"><span data-stu-id="87b26-110">To purchase items or services for a job</span></span>
<span data-ttu-id="87b26-111">Eftirfarandi ferli sýnir hvernig á að nota innkaupareikning til að kaupa vörur fyrir verk.</span><span class="sxs-lookup"><span data-stu-id="87b26-111">The following procedure shows how to use a purchase invoice to purchase products for a job.</span></span> <span data-ttu-id="87b26-112">Sömu skref eiga við þegar innkaupapöntun er notuð.</span><span class="sxs-lookup"><span data-stu-id="87b26-112">The same steps apply when using a purchase order.</span></span>  

1. <span data-ttu-id="87b26-113">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Innkaupareikningar** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="87b26-113">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Purchase Invoices**, and then choose the related link.</span></span>  
2. <span data-ttu-id="87b26-114">Veljið aðgerðina **Nýtt** og fyllið svo út reitina eins og þörf krefur.</span><span class="sxs-lookup"><span data-stu-id="87b26-114">Choose the **New** action and fill in the fields as necessary.</span></span> <span data-ttu-id="87b26-115">Nánari upplýsingar eru í reitnum [Skrá innkaup](purchasing-how-record-purchases.md).</span><span class="sxs-lookup"><span data-stu-id="87b26-115">For more information, see [Record Purchases](purchasing-how-record-purchases.md).</span></span>
3. <span data-ttu-id="87b26-116">Í reitunum **Verk nr.** og **Verkhluti nr.** eru valdar upplýsingarnar um verkið sem þú vilt kaupa vörur eða þjónustu fyrir.</span><span class="sxs-lookup"><span data-stu-id="87b26-116">In the **Job No.** and **Job Task No.** fields, select the information of the job that you want to purchase items or services for.</span></span> <span data-ttu-id="87b26-117">Notaðu **Dálkaval** ef svæðið er ekki sýnilegt.</span><span class="sxs-lookup"><span data-stu-id="87b26-117">Use the **Choose Columns** function if the field is not visible.</span></span> <span data-ttu-id="87b26-118">Frekari upplýsingar eru í [Sérstilling verksvæðis](ui-personalization-user.md).</span><span class="sxs-lookup"><span data-stu-id="87b26-118">For more information, see [Personalize Your Workspace](ui-personalization-user.md).</span></span>

    <span data-ttu-id="87b26-119">Gildið sem valið er í reitnum **Verklínutegund** skilgreinir hvort búin sé til áætlunarlína þegar notkun vörunnar er bókuð.</span><span class="sxs-lookup"><span data-stu-id="87b26-119">The value that you select in the **Job Line Type** field defines whether a planning line is created when you post the usage of the item.</span></span> <span data-ttu-id="87b26-120">Ef reiturinn inniheldur **Reikningshæft** eru stofnaðar áætlunarlínur sem eru tilbúnar til að vera reikningsfærðar til viðskiptavinar.</span><span class="sxs-lookup"><span data-stu-id="87b26-120">If the field contains **Billable**, then job planning lines that are ready to be invoiced to the customer are created.</span></span> <span data-ttu-id="87b26-121">Frekari upplýsingar eru í [Reikningsfærsla verka](projects-how-invoice-jobs.md).</span><span class="sxs-lookup"><span data-stu-id="87b26-121">For more information, see [Invoice Jobs](projects-how-invoice-jobs.md).</span></span>
4. <span data-ttu-id="87b26-122">Valið er **Bóka** aðgerðin.</span><span class="sxs-lookup"><span data-stu-id="87b26-122">Choose the **Post** action.</span></span>

## <a name="to-view-the-value-of-purchases-for-a-job"></a><span data-ttu-id="87b26-123">Til að skoða virði innkaupa fyrir verk</span><span class="sxs-lookup"><span data-stu-id="87b26-123">To view the value of purchases for a job</span></span>
1. <span data-ttu-id="87b26-124">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Verk** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="87b26-124">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Jobs**, and then choose the related link.</span></span>
2. <span data-ttu-id="87b26-125">Opnið viðeigandi verkspjald.</span><span class="sxs-lookup"><span data-stu-id="87b26-125">Open a relevant job card.</span></span>

    <span data-ttu-id="87b26-126">Á flýtiflipanum **Verkhlutar** sýnir reiturinn **Óafgreiddar pantanir** útistandandi upphæð í staðbundnum gjaldmiðli fyrir vörur í birgðaskrá og þjónustu á innkaupaskjöl fyrir verkhlutalínuna.</span><span class="sxs-lookup"><span data-stu-id="87b26-126">On the **Tasks** FastTab, the **Outstanding Orders** field shows the total outstanding amount, in local currency, of inventory items and services on purchase documents for the job task line.</span></span>  

    <span data-ttu-id="87b26-127">Reiturinn **Afh. upph. óreikn.færð** sýnir virði vara sem afhentra vara í innkaupaskjölum sem ekki hafa verið reikningsfærðar enn.</span><span class="sxs-lookup"><span data-stu-id="87b26-127">The **Amt. Rec. Not Invoiced** field shows the value of items delivered on purchase documents, but not yet invoiced.</span></span>  
3. <span data-ttu-id="87b26-128">Þegar smellt er í reitinn opnast glugginn **Innkaupalínur**. Á síðunni má sjá upplýsingar úr innkaupapöntuninni, þ.á.m. hvaða vörur eða forði hafa verið móttekin.</span><span class="sxs-lookup"><span data-stu-id="87b26-128">Choose either of the fields to open the **Purchase Lines** page where you can review information about the related purchase document lines, including which items or services have been received.</span></span>

## <a name="to-post-a-job-related-expense"></a><span data-ttu-id="87b26-129">Til að bóka verktengdan kostnað</span><span class="sxs-lookup"><span data-stu-id="87b26-129">To post a job-related expense</span></span>
<span data-ttu-id="87b26-130">Ef þú verður fyrir óvenjulegum útgjöldum eða útgöldum sökum eins verks, er hægt að nota síðuna **Verk fjárhagsbókar** til að bóka þau beint í viðeigandi verkreikning.</span><span class="sxs-lookup"><span data-stu-id="87b26-130">If you incur extraordinary or one-time job expenses, you can use the **Job G/L Journal** page to post them directly to the relevant job account.</span></span>

1. <span data-ttu-id="87b26-131">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Fjárhagsbækur verks** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="87b26-131">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Job G/L Journals**, and then choose the related link.</span></span>  
2. <span data-ttu-id="87b26-132">Ný lína er stofnuð og kostnaðarupplýsingar, þar á meðal **Verk nr** og **Verkhluti nr.**, færðar inn í reitina.</span><span class="sxs-lookup"><span data-stu-id="87b26-132">Create a new line and enter information about the expense, including information in the **Job No.** and **Job Task No** fields.</span></span>  
3. <span data-ttu-id="87b26-133">Þegar færslubókin er tilbúin skal velja aðgerðina **Bóka**.</span><span class="sxs-lookup"><span data-stu-id="87b26-133">When the journal is complete, choose the **Post** action.</span></span>

## <a name="see-also"></a><span data-ttu-id="87b26-134">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="87b26-134">See Also</span></span>
[<span data-ttu-id="87b26-135">Verkefnastjórnun</span><span class="sxs-lookup"><span data-stu-id="87b26-135">Project Management</span></span>](projects-manage-projects.md)  
[<span data-ttu-id="87b26-136">Fjármál</span><span class="sxs-lookup"><span data-stu-id="87b26-136">Finance</span></span>](finance.md)  
<span data-ttu-id="87b26-137">[Innkaup](purchasing-manage-purchasing.md)       </span><span class="sxs-lookup"><span data-stu-id="87b26-137">[Purchasing](purchasing-manage-purchasing.md)       </span></span>  
<span data-ttu-id="87b26-138">[Sala](sales-manage-sales.md)    </span><span class="sxs-lookup"><span data-stu-id="87b26-138">[Sales](sales-manage-sales.md)    </span></span>  
<span data-ttu-id="87b26-139">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="87b26-139">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
