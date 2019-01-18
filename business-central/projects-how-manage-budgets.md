---
title: "Setja upp og stjórna fjárhagsáætlun fyrir verk| Microsoft Docs"
description: "Lýsir því hvernig skal áætla tilföng og spá fyrir um og stjórna kostnaði verks með því að setja upp fjárhagsáætlun fyrir hvert verk."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project budget, forecast
ms.date: 10/17/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: d26a6fd6369d8d10d690246c5d02a04d23bb21ab
ms.contentlocale: is-is
ms.lasthandoff: 11/26/2018

---
# <a name="manage-job-budgets"></a><span data-ttu-id="c66ee-103">Umsjón fjárhagsáætlana fyrir eignir</span><span class="sxs-lookup"><span data-stu-id="c66ee-103">Manage Job Budgets</span></span>
<span data-ttu-id="c66ee-104">Hægt er að setja upp áætlun fyrir hvert verk.</span><span class="sxs-lookup"><span data-stu-id="c66ee-104">You can set up a budget for each job.</span></span> <span data-ttu-id="c66ee-105">Áætlunin er notuð til að áætla forðann sem hægt er að úthluta verki.</span><span class="sxs-lookup"><span data-stu-id="c66ee-105">The budget is used to plan the resources that you allocate to a job.</span></span> <span data-ttu-id="c66ee-106">Áætlunin getur verið almenns eðlis með fáeinum færslum eða með mörgum færslum sem skiptast í aðgerðastig.</span><span class="sxs-lookup"><span data-stu-id="c66ee-106">The budget can be either general with few entries or it can contain more entries that are divided into activity levels.</span></span> <span data-ttu-id="c66ee-107">Svo er hægt að bera áætlaðar upphæðir saman við raunverulega notkun eins og hún birtist í verkbókinni.</span><span class="sxs-lookup"><span data-stu-id="c66ee-107">You can then compare the budgeted amounts with the actual usage as recorded in the job journal.</span></span> <span data-ttu-id="c66ee-108">Með því að fylgjast með mismuni á milli raunnotkun og áætlaðri notkun er hægt að stýra yfirstandandi verkefni og auka gæði síðari verka með því að draga úr hættu á að kostnaður sé vanmetinn.</span><span class="sxs-lookup"><span data-stu-id="c66ee-108">By monitoring differences between actual usage and budgeted usage, you can control an ongoing project and improve the quality of future jobs by reducing the risk of underestimating costs.</span></span>

<span data-ttu-id="c66ee-109">Eftirfarandi aðferð lýsir því hvernig á að meta áætlaðan kostnað við áætlun.</span><span class="sxs-lookup"><span data-stu-id="c66ee-109">The following procedure describes how to estimate budgeted costs during planning.</span></span> <span data-ttu-id="c66ee-110">Upplýsingar um skráningu áætlaðra- og raunverða verka og kostnað er að finna í [Skrá notkun fyrir verk](projects-how-record-job-usage.md).</span><span class="sxs-lookup"><span data-stu-id="c66ee-110">For information about recording budgeted versus actual job prices and costs, see [Record Usage for Jobs](projects-how-record-job-usage.md).</span></span>  

## <a name="JobBudgetCosts"></a> <span data-ttu-id="c66ee-111">Til að áætlað kostnað verks</span><span class="sxs-lookup"><span data-stu-id="c66ee-111">To estimate the budgeted costs for a job</span></span>
<span data-ttu-id="c66ee-112">Þegar viðskiptavinur vill vita verð verks sem verður reikningsfært samkvæmt notkun þarf að ákvarða áætlaðan kostnað verksins.</span><span class="sxs-lookup"><span data-stu-id="c66ee-112">When a customer wants to know the price of a job that will be invoiced based on usage, you must have to determine the budgeted costs for the job.</span></span> <span data-ttu-id="c66ee-113">Síðan **Verð verkvara** er notuð til þess.</span><span class="sxs-lookup"><span data-stu-id="c66ee-113">You use the **Job Task Lines** page to do this.</span></span>

1. <span data-ttu-id="c66ee-114">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Verk** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="c66ee-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Jobs**, and then choose the related link.</span></span>  
2. <span data-ttu-id="c66ee-115">Opnið viðeigandi verk.</span><span class="sxs-lookup"><span data-stu-id="c66ee-115">Open a relevant job.</span></span>
3. <span data-ttu-id="c66ee-116">Veljið verkhlutalínu af gerðinni Bókun og veljið svo aðgerðina **Verkáætlunarlínur**.</span><span class="sxs-lookup"><span data-stu-id="c66ee-116">Select a task line of type Posting, and then choose the **Job Planning Lines** action.</span></span>
4. <span data-ttu-id="c66ee-117">Fyllið í reitina eftir þörfum í nýrri línu.</span><span class="sxs-lookup"><span data-stu-id="c66ee-117">On a new line, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]   

<span data-ttu-id="c66ee-118">Fyrir reitinn **Línugerð** skal vísa til eftirfarandi upplýsinga.</span><span class="sxs-lookup"><span data-stu-id="c66ee-118">For the **Line Type** field, refer to the following information.</span></span>  

| <span data-ttu-id="c66ee-119">Tegund línu</span><span class="sxs-lookup"><span data-stu-id="c66ee-119">Line Type</span></span> | <span data-ttu-id="c66ee-120">Lýsing</span><span class="sxs-lookup"><span data-stu-id="c66ee-120">Description</span></span> |
| --- | --- |
| <span data-ttu-id="c66ee-121">**Bæði fjárhagsáætlun og reikningshæft**</span><span class="sxs-lookup"><span data-stu-id="c66ee-121">**Both Budget and Billable**</span></span> |<span data-ttu-id="c66ee-122">Upphæðir kostnaðar og verðs sem færðar eru í áætlunarlínuna eru áætlaður kostnaður þeirrar áætlunarlínu.</span><span class="sxs-lookup"><span data-stu-id="c66ee-122">The cost and price amounts entered on the planning line are the budgeted costs for the particular planning line.</span></span> <span data-ttu-id="c66ee-123">Verðupphæðin verður reikningsfærð.</span><span class="sxs-lookup"><span data-stu-id="c66ee-123">The price amount will be invoiced.</span></span> |
| <span data-ttu-id="c66ee-124">**Fjárhagsáætlun**</span><span class="sxs-lookup"><span data-stu-id="c66ee-124">**Budget**</span></span> |<span data-ttu-id="c66ee-125">Viðskiptavinurinn er ekki rukkaður um notkun.</span><span class="sxs-lookup"><span data-stu-id="c66ee-125">The customer is not charged for usage.</span></span> <span data-ttu-id="c66ee-126">notkunina er aldrei hægt að flytja á reikning en hún verður samt notuð í útreikningum VÍV.</span><span class="sxs-lookup"><span data-stu-id="c66ee-126">Usage is not transferred to an invoice, but will still be used in the calculation of WIP.</span></span> |
| <span data-ttu-id="c66ee-127">**Reikningshæft**</span><span class="sxs-lookup"><span data-stu-id="c66ee-127">**Billable**</span></span> |<span data-ttu-id="c66ee-128">Viðskiptavinurinn er rukkaður um notkun.</span><span class="sxs-lookup"><span data-stu-id="c66ee-128">The customer is charged for usage.</span></span> <span data-ttu-id="c66ee-129">Notkun er færð á reikninginn samkvæmt magninu sem tilgreint er í reitnum Magn til flutnings á reikning.</span><span class="sxs-lookup"><span data-stu-id="c66ee-129">Usage is transferred to the invoice, based on the quantity specified in the Qty. to Transfer to Invoice field.</span></span> |

> [!NOTE]  
> <span data-ttu-id="c66ee-130">Reiturinn **Áætluð afhendingardagsetning** fyrir áætlunarlínuna inniheldur dagsetninguna þegar áætlað er að notkun tengd áætlunarlínunni verði lokið.</span><span class="sxs-lookup"><span data-stu-id="c66ee-130">The **Planned Delivery Date** field for the planning line contains the date when usage related to the planning line is expected to be completed.</span></span> <span data-ttu-id="c66ee-131">Það er líka dagsetningin þegar hægt er að flytja áætlunarlínuna á sölureikning og bóka hana.</span><span class="sxs-lookup"><span data-stu-id="c66ee-131">It is also the date when the planning line may be transferred to a sales invoice and posted.</span></span> <br /><br /> <span data-ttu-id="c66ee-132">Á undirliggjandi verkhluta á síðunni **Verkspjald** innihalda reitirnir **Upphafsdagur** og **Lokadagur** gildi reitsins **Áætluð afhendingardagsetning** á elstu og nýjustu verkáætlunarlínum á tengdum síðum **Verkáætlunarlínur**.</span><span class="sxs-lookup"><span data-stu-id="c66ee-132">On the underlying job task on the **Job Card** page, the **Start Date** and **End Date** fields respectively contain the value of the **Planned Delivery Date** field on the earliest and latest job planning lines in the related **Job Planning Lines** page.</span></span>

> [!NOTE]  
>   <span data-ttu-id="c66ee-133">Þegar þú fyllir í reitinn **Magn**, verða allar upplýsingar um heildarverð og heildarkostnað reiknaðar út og settar í áætlunarlínuna.</span><span class="sxs-lookup"><span data-stu-id="c66ee-133">When you fill in the **Quantity** field, all total price and total cost information will be calculated and filled in for that planning line.</span></span> <span data-ttu-id="c66ee-134">Hægt er að breyta þeim hvenær sem er.</span><span class="sxs-lookup"><span data-stu-id="c66ee-134">You can edit them at any time.</span></span>

<span data-ttu-id="c66ee-135">Á síðunni **Verkspjald** er nú hægt að skoða samantekt yfirlit yfir áætlaðan heildarkostnað, áætlað verð, reikningshæfan kostnað og reikningshæft verð fyrir hvert verk fyrir sig.</span><span class="sxs-lookup"><span data-stu-id="c66ee-135">On the **Job Card** page, you can now see a summary of the total budgeted costs, budgeted price, billable cost and billable price for each task.</span></span>

<span data-ttu-id="c66ee-136">Upplýsingar um skráningu áætlaðra- og raunverða verka og kostnað er að finna í [Skrá notkun fyrir verk](projects-how-record-job-usage.md).</span><span class="sxs-lookup"><span data-stu-id="c66ee-136">For information about recording budgeted versus actual job prices and costs, see [Record Usage for Jobs](projects-how-record-job-usage.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="c66ee-137">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="c66ee-137">See Also</span></span>
[<span data-ttu-id="c66ee-138">Verkefnastjórnun</span><span class="sxs-lookup"><span data-stu-id="c66ee-138">Project Management</span></span>](projects-manage-projects.md)  
[<span data-ttu-id="c66ee-139">Fjármál</span><span class="sxs-lookup"><span data-stu-id="c66ee-139">Finance</span></span>](finance.md)  
<span data-ttu-id="c66ee-140">[Innkaup](purchasing-manage-purchasing.md)       </span><span class="sxs-lookup"><span data-stu-id="c66ee-140">[Purchasing](purchasing-manage-purchasing.md)       </span></span>  
<span data-ttu-id="c66ee-141">[Sala](sales-manage-sales.md)    </span><span class="sxs-lookup"><span data-stu-id="c66ee-141">[Sales](sales-manage-sales.md)    </span></span>  
<span data-ttu-id="c66ee-142">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="c66ee-142">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

