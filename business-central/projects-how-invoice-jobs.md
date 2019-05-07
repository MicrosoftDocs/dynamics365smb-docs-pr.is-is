---
title: Stofna verksölureikning til að reikningsfæra verk| Microsoft Docs
description: Lýsir því hvernig skal reikningsfæra viðskiptamenn fyrir verkútgjöld þegar á verkið líður.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project invoice
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 57a0cb6624e122f52aaa0680fd73df8b67a23d30
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2019
ms.locfileid: "927878"
---
# <a name="invoice-jobs"></a><span data-ttu-id="603d9-103">Reikningsfærsla verka</span><span class="sxs-lookup"><span data-stu-id="603d9-103">Invoice Jobs</span></span>
<span data-ttu-id="603d9-104">Meðan á verkefninu stendur getur kostnaður vegna forðanotkunar, efnis og verktengdra innkaupa safnast upp.</span><span class="sxs-lookup"><span data-stu-id="603d9-104">During the project, job costs from resource usage, materials, and job-related purchases can accumulate.</span></span> <span data-ttu-id="603d9-105">Þessar færslur eru bókaðar í verkbókina á vinnslutíma verksins.</span><span class="sxs-lookup"><span data-stu-id="603d9-105">As the job progresses, these transactions get posted to the job journal.</span></span> <span data-ttu-id="603d9-106">Mikilvægt er að allur kostnaður sé skráður í verkbókina áður en viðskiptavininum er sendur reikningur.</span><span class="sxs-lookup"><span data-stu-id="603d9-106">It is important that all costs get recorded in the job journal before you invoice the customer.</span></span>

<span data-ttu-id="603d9-107">Hægt er að reikningsfæra allt verkið á síðunni **Verkhlutalínur** eða aðeins reikningsfæra ákveðnar reikningshæfar línur á síðunni **Áætlunarlínur**.</span><span class="sxs-lookup"><span data-stu-id="603d9-107">You can invoice the whole job from the **Job Task Lines** page or only invoice selected billable lines from the **Planning Lines** page.</span></span> <span data-ttu-id="603d9-108">Hægt er að reikningsfæra þegar verkinu er lokið eða með vissu millibili á meðan á vinnslu verksins stendur, byggt á reikningsáætlun.</span><span class="sxs-lookup"><span data-stu-id="603d9-108">Invoicing can be done after the job is finished or at certain intervals during the job's progress based on an invoicing schedule.</span></span>

> [!NOTE]  
>   <span data-ttu-id="603d9-109">Ef valið er **Reikningshæft** í reitnum **Verklínutegund** í söluskjölum fyrir verktengd innkaup verða stofnaðar verkáætlunarlínur sem eru tilbúnar til að vera reikningsfærðar á viðskiptamann.</span><span class="sxs-lookup"><span data-stu-id="603d9-109">If you select **Billable** in the **Job Line Type** field on the purchase documents for job-related purchases, then job planning lines that are ready to be invoiced to the customer are created.</span></span> <span data-ttu-id="603d9-110">Frekari upplýsingar eru í [Sjá um birgðir verkefna](projects-how-manage-project-supplies.md).</span><span class="sxs-lookup"><span data-stu-id="603d9-110">For more information, see [Manage Project Supplies](projects-how-manage-project-supplies.md).</span></span>

## <a name="to-create-and-post-a-job-sales-invoice"></a><span data-ttu-id="603d9-111">Til að stofna og bóka sölureikning verks:</span><span class="sxs-lookup"><span data-stu-id="603d9-111">To create and post a job sales invoice</span></span>
<span data-ttu-id="603d9-112">Hægt er að stofna reikning fyrir verk eða einn eða fleiri verkhluta fyrir viðskiptavin þegar verkinu sem á að reikningsfæra er lokið eða komið er að dagsetningu reikningafærslunnar, sem byggist á reikningsfærsluáætlun.</span><span class="sxs-lookup"><span data-stu-id="603d9-112">You can create an invoice for a job or for one or more job tasks for a customer when either the work to be invoiced is complete or the date for invoicing based on an invoicing schedule has been reached.</span></span>

<span data-ttu-id="603d9-113">Á síðunni **Verk** er hægt að reikningsfæra til viðskiptamanns með því að velja verkið og velja svo aðgerðina **Stofna sölureikning verks**.</span><span class="sxs-lookup"><span data-stu-id="603d9-113">From the **Jobs** page, you can invoice a customer by selecting the job, and then choosing the **Create Job Sales Invoice** action.</span></span> <span data-ttu-id="603d9-114">Eftirfarandi ferli sýnir hvernig á að nota keyrslu til að reikningsfæra fleiri verk.</span><span class="sxs-lookup"><span data-stu-id="603d9-114">The following procedure shows how to use a batch job to invoice multiple jobs.</span></span>  

1. <span data-ttu-id="603d9-115">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Verk - Stofna sölureikning** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="603d9-115">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Job Create Sales Invoice**, and then choose the related link.</span></span>  
2. <span data-ttu-id="603d9-116">Fyllið inn í svæðin eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="603d9-116">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="603d9-117">Ef takmarka á verk sem keyrslan á að vinna skal tilgreina afmarkanir.</span><span class="sxs-lookup"><span data-stu-id="603d9-117">Set filters if you want to limit the jobs that the batch job will process.</span></span>
4. <span data-ttu-id="603d9-118">Velja hnappinn **Í lagi** til að stofna reikningana.</span><span class="sxs-lookup"><span data-stu-id="603d9-118">Choose the **OK** button to create the invoices.</span></span>  

## <a name="to-create-multiple-job-sales-invoices-from-job-planning-lines"></a><span data-ttu-id="603d9-119">Að búa til fleiri sölureikninga úr verkáætlunarlínum</span><span class="sxs-lookup"><span data-stu-id="603d9-119">To create multiple job sales invoices from job planning lines</span></span>
<span data-ttu-id="603d9-120">Hægt er að stofna reikning úr verkáætlunarlínum, og gefa upp á þeim tíma magnið af vörunni, forða eða fjárhagsreikning sem á að reikningsfæra.</span><span class="sxs-lookup"><span data-stu-id="603d9-120">You can create an invoice from a job planning lines, and indicate at that time the quantity of the item, resource, or general ledger account that you want to invoice.</span></span>

1. <span data-ttu-id="603d9-121">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Verk** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="603d9-121">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Jobs**, and then choose the related link.</span></span>
2. <span data-ttu-id="603d9-122">Opnið viðeigandi verk.</span><span class="sxs-lookup"><span data-stu-id="603d9-122">Open a relevant job.</span></span>
3. <span data-ttu-id="603d9-123">Valinn er verkhluti þar sem reiturinn **Verkhlutagerð** inniheldur **Bókuð** og svo er aðgerðin **Verkhlutalínur** valin.</span><span class="sxs-lookup"><span data-stu-id="603d9-123">Select a job task for which the **Job Task Type** field contains **Posting**, and then choose the **Job Planning Lines** action.</span></span>  
4. <span data-ttu-id="603d9-124">Í verkáætlunarlínu í reitnum **Magn Til að reikningsfæra** er slegið inn magn vörunnar, forðann, fjárhagsreikningsgerð sem á að reikningsfæra.</span><span class="sxs-lookup"><span data-stu-id="603d9-124">On a job planning line, in the **Qty. To Transfer to Invoice** field, enter the quantity of the item, resource, general ledger account type that you want to invoice.</span></span>  
5. <span data-ttu-id="603d9-125">Veljið aðgerðina **Stofna sölureikning**.</span><span class="sxs-lookup"><span data-stu-id="603d9-125">Choose the **Create Sales Invoice** action.</span></span>
6. <span data-ttu-id="603d9-126">Á síðunni **Stofna sölureikning verks** færirðu inn bókunardagsetninguna og hvort eigi að stofna nýjan reikning eða skeyta þessum reikningi við fyrirliggjandi reikning.</span><span class="sxs-lookup"><span data-stu-id="603d9-126">On the **Job Create Sales Invoice** page, enter the posting date and whether you want to create a new invoice or append this invoice to an existing one.</span></span>
7. <span data-ttu-id="603d9-127">Velja hnappinn **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="603d9-127">Choose the **OK** button.</span></span>  

    <span data-ttu-id="603d9-128">Í reitnum **Magn flutt á reikning** í verkáætlunarlínunni er hægt að sjá magnið.</span><span class="sxs-lookup"><span data-stu-id="603d9-128">On the job planning line, in the **Qty. Transferred to Invoice** field, you can see the quantity.</span></span>
8. <span data-ttu-id="603d9-129">Á síðunni **Verkáætlunarlínur** skal velja aðgerðina **Sölureikningar/kreditreikningar**.</span><span class="sxs-lookup"><span data-stu-id="603d9-129">On the **Job Planning Lines** page, choose the **Sales Invoices/Credit Memos** action.</span></span>

    <span data-ttu-id="603d9-130">Síðan **Sölureikningur** opnast og sýnir það magn sem hefur verið flutt á reikninginn.</span><span class="sxs-lookup"><span data-stu-id="603d9-130">The **Sales Invoice** page opens, showing the quantity that you have transferred to the invoice.</span></span>  
9. <span data-ttu-id="603d9-131">Gerið frekari breytingar og veljið svo aðgerðina **Bóka**.</span><span class="sxs-lookup"><span data-stu-id="603d9-131">Make any additional changes, and then choose the **Post** action.</span></span>

> [!NOTE]  
>   <span data-ttu-id="603d9-132">Ofangreint ferli er svipað þegar verið er að stofna, yfirfara og bóka verktengdan sölukreditreikning.</span><span class="sxs-lookup"><span data-stu-id="603d9-132">The above procedure is similar for creating, reviewing, and posting a job-related sales credit memo.</span></span>

## <a name="to-calculate-and-post-job-completion-entries"></a><span data-ttu-id="603d9-133">Að reikna út og bóka verklokafærslur</span><span class="sxs-lookup"><span data-stu-id="603d9-133">To calculate and post job completion entries</span></span>
<span data-ttu-id="603d9-134">Þegar öllum aðgerðum verks hefur verið lokið, þar með talin bókun notkunar og reikningsfærsla, þarf að uppfæra verkið svo að **Staða** þess sé **Lokið**.</span><span class="sxs-lookup"><span data-stu-id="603d9-134">When you have completed all activities for a job, including usage posting and invoicing, you must update the job to have a **Status** of **Completed**.</span></span> <span data-ttu-id="603d9-135">Síðan þarf að bakfæra VÍV sem hefur verið bókað í fjárhag.</span><span class="sxs-lookup"><span data-stu-id="603d9-135">Then, you must reverse any WIP that has been posted to the general ledger.</span></span>

1. <span data-ttu-id="603d9-136">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Verk** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="603d9-136">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Jobs**, and then choose the related link.</span></span>  
2. <span data-ttu-id="603d9-137">Veljið opið verk og veljið svo aðgerðina **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="603d9-137">Select an open job, and then choose the **Edit** action.</span></span>
3. <span data-ttu-id="603d9-138">Í reitnum **Staða** skal velja **Lokið**.</span><span class="sxs-lookup"><span data-stu-id="603d9-138">In the **Status** field, select **Completed**.</span></span>
4. <span data-ttu-id="603d9-139">Fylgið aðstoðarskrefunum til að reikna og bóka VÍV.</span><span class="sxs-lookup"><span data-stu-id="603d9-139">Follow the assistance steps to calculate and post WIP.</span></span> <span data-ttu-id="603d9-140">Einnig er hægt að fylgja skrefum 5 og 6 til að gera það handvirkt.</span><span class="sxs-lookup"><span data-stu-id="603d9-140">Alternatively, follows steps 5 and 6 to do so manually.</span></span>  
5. <span data-ttu-id="603d9-141">Veljið aðgerðina **Reikna VÍV**.</span><span class="sxs-lookup"><span data-stu-id="603d9-141">Choose the **Calculate WIP** action.</span></span>
6. <span data-ttu-id="603d9-142">Á síðunni **Verk - Reikna VÍV** þarf að fylla reitina út eins og þörf krefur.</span><span class="sxs-lookup"><span data-stu-id="603d9-142">On the **Job Calculate WIP** page, fill in the fields as necessary.</span></span>  

     <span data-ttu-id="603d9-143">VÍV færslurnar sem voru stofnaðar með keyrslunni munu nú hafa gátmerki í reitnum **Verki lokið** til að sýna að þær séu lokafærslur.</span><span class="sxs-lookup"><span data-stu-id="603d9-143">The job WIP entries created by running the batch job will have the **Job Complete** check box selected to show that they are completion entries.</span></span>  
7. <span data-ttu-id="603d9-144">Velja skal aðgerðina **Verk - Bóka VÍV í fjárhag**.</span><span class="sxs-lookup"><span data-stu-id="603d9-144">Choose the **Job Post WIP to G/L** action.</span></span>
8. <span data-ttu-id="603d9-145">Á síðunni **Verk - Bóka VÍV í fjárhag** skal fylla reitina út eins og þörf krefur.</span><span class="sxs-lookup"><span data-stu-id="603d9-145">On the **Job Post WIP to G/L** page, fill in the fields as necessary.</span></span>  

     <span data-ttu-id="603d9-146">VÍV-fjárlagsfærslur verks sem voru stofnaðar með keyrslunni munu nú hafa gátmerki í reitnum **Verki lokið** til að sýna að þær eru lokafærslur.</span><span class="sxs-lookup"><span data-stu-id="603d9-146">The job WIP general ledger entries created by running the batch job will have the **Job Complete** check box selected to show they are completion entries.</span></span>

## <a name="see-also"></a><span data-ttu-id="603d9-147">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="603d9-147">See Also</span></span>
[<span data-ttu-id="603d9-148">Stjórna verkum</span><span class="sxs-lookup"><span data-stu-id="603d9-148">Managing Projects</span></span>](projects-manage-projects.md)  
[<span data-ttu-id="603d9-149">Fjármál</span><span class="sxs-lookup"><span data-stu-id="603d9-149">Finance</span></span>](finance.md)  
<span data-ttu-id="603d9-150">[Innkaup](purchasing-manage-purchasing.md)       </span><span class="sxs-lookup"><span data-stu-id="603d9-150">[Purchasing](purchasing-manage-purchasing.md)       </span></span>  
<span data-ttu-id="603d9-151">[Sala](sales-manage-sales.md)    </span><span class="sxs-lookup"><span data-stu-id="603d9-151">[Sales](sales-manage-sales.md)    </span></span>  
<span data-ttu-id="603d9-152">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="603d9-152">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
