---
title: "Setja upp vinnuskýrslur og samþykktarferli þeirra| Microsoft Docs"
description: "Þú setur upp vinnuskýrslu til að mæla tíma sem er notaður í verk og notkun forða, til að auðvelda þér verkefnastjórnun, mönnun og afkastaveitu."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project management, capacity, staff, resource
ms.date: 06/06/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 3e85168709eb8e96b2ee2aea516189c2cf88d426
ms.contentlocale: is-is
ms.lasthandoff: 09/11/2017


---
# <a name="how-to-set-up-time-sheets"></a><span data-ttu-id="e6447-103">Hvernig á að setja upp tímablöð</span><span class="sxs-lookup"><span data-stu-id="e6447-103">How to: Set Up Time Sheets</span></span>
<span data-ttu-id="e6447-104">Vinnuskjöl í [!INCLUDE[d365fin](includes/d365fin_md.md)] meðhöndla tímaskráningu í vikulegum stigum sjö daga.</span><span class="sxs-lookup"><span data-stu-id="e6447-104">Time sheets in [!INCLUDE[d365fin](includes/d365fin_md.md)] handle time registration in weekly increments of seven days.</span></span> <span data-ttu-id="e6447-105">Þær eru notaðar til að fylgjast með þeim tíma sem varið er í verk og hægt er að nota þær fyrir einfalda tímaskráningu forða.</span><span class="sxs-lookup"><span data-stu-id="e6447-105">You use them to track the time used on jobs, and you can use them to record simple resource time registration.</span></span> <span data-ttu-id="e6447-106">Áður en hægt er að nota vinnuskýrslur, verður að skilgreina hvernig þær eiga að vera settar upp og grunnstilltar.</span><span class="sxs-lookup"><span data-stu-id="e6447-106">Before you can use time sheets, you must specify how you want them to be set up and configured.</span></span>

<span data-ttu-id="e6447-107">Þegar búið er að setja upp hvernig fyrirtækið á að nota vinnuskýrslur er hægt að tilgreina hvort og hvernig tímaskýrslur eru samþykktar.</span><span class="sxs-lookup"><span data-stu-id="e6447-107">After you have set up how your organization will use time sheets, you can specify if and how time sheets are approved.</span></span> <span data-ttu-id="e6447-108">Allt eftir þörfum fyrirtækisins er hægt að tilgreina:</span><span class="sxs-lookup"><span data-stu-id="e6447-108">Depending on the needs of your organization, you can designate:</span></span>

* <span data-ttu-id="e6447-109">Einn eða fleiri notendur sem vinnuskýrslustjóra og sem samþykkja allar vinnuskýrslur.</span><span class="sxs-lookup"><span data-stu-id="e6447-109">One or more users as the time sheet administrator and approver for all time sheets.</span></span>
* <span data-ttu-id="e6447-110">Vinnuskýrslusamþykkjandi fyrir hvern forða.</span><span class="sxs-lookup"><span data-stu-id="e6447-110">A time sheet approver for each resource.</span></span>

<span data-ttu-id="e6447-111">Þegar búið er að setja upp vinnuskýrslur er hægt að búa til vinnuskýrslur fyrir forða, úthluta þeim á verkáætlunarlínur og bóka vinnuskýrslulínur.</span><span class="sxs-lookup"><span data-stu-id="e6447-111">When you have set up time sheets, you can create time sheets for resources, assign them to job planning lines, and post time sheet lines.</span></span> <span data-ttu-id="e6447-112">Frekari upplýsingar eru í [Hvernig á að: Nota vinnuskýrslur](projects-how-use-time-sheets.md).</span><span class="sxs-lookup"><span data-stu-id="e6447-112">For more information, see [How to: Use Time Sheets](projects-how-use-time-sheets.md).</span></span>

## <a name="to-set-up-general-information-for-time-sheets"></a><span data-ttu-id="e6447-113">Til að setja upp almennar upplýsingar um vinnuskýrslur</span><span class="sxs-lookup"><span data-stu-id="e6447-113">To set up general information for time sheets</span></span>
1. <span data-ttu-id="e6447-114">Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Uppsetning forða** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="e6447-114">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Resources Setup**, and then choose the related link.</span></span>  
2. <span data-ttu-id="e6447-115">Fyllið inn í svæðin eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="e6447-115">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="e6447-116">Í reitnum **Vinnuskýrslur eftir samþykkt verks** skal velja einn af eftirfarandi valkostum.</span><span class="sxs-lookup"><span data-stu-id="e6447-116">For the **Time Sheet by Job Approval** field, select one of the following options.</span></span>

| <span data-ttu-id="e6447-117">Valkostur</span><span class="sxs-lookup"><span data-stu-id="e6447-117">Option</span></span> | <span data-ttu-id="e6447-118">Lýsing</span><span class="sxs-lookup"><span data-stu-id="e6447-118">Description</span></span> |
| --- | --- |
| <span data-ttu-id="e6447-119">**Aldrei**</span><span class="sxs-lookup"><span data-stu-id="e6447-119">**Never**</span></span> |<span data-ttu-id="e6447-120">Notandinn í reitnum **Notandakenni samþykktaraðila vinnuskýrslu** á forðaspjaldinu samþykkir vinnuskýrsluna.</span><span class="sxs-lookup"><span data-stu-id="e6447-120">The user in the **Time Sheet Approver User ID** field on the resource card approves the time sheet.</span></span> |
| <span data-ttu-id="e6447-121">**Alltaf**</span><span class="sxs-lookup"><span data-stu-id="e6447-121">**Always**</span></span> |<span data-ttu-id="e6447-122">Notandinn í reitnum **Ábyrgðaraðili** á verkspjaldinu samþykkir vinnuskýrsluna.</span><span class="sxs-lookup"><span data-stu-id="e6447-122">The user in the **Person Responsible** field on the job card approves the time sheet.</span></span> |
| <span data-ttu-id="e6447-123">**Aðeins véla**</span><span class="sxs-lookup"><span data-stu-id="e6447-123">**Machine Only**</span></span> |<span data-ttu-id="e6447-124">Ef vinnuskýrsla vélar er tengd við verk er það notandinn í reitnum **Ábyrgðaraðili** á verkspjaldinu sem samþykkir vinnuskýrsluna.</span><span class="sxs-lookup"><span data-stu-id="e6447-124">If the machine time sheet is linked with a job, then the user in the **Person Responsible** field on the job card approves the time sheet.</span></span> <span data-ttu-id="e6447-125">Ef vinnuskýrsla vélar er tengd við forða er það notandinn í reitnum **Notandakenni samþykktaraðila vinnuskýrslu** á forðaspjaldinu sem samþykkir vinnuskýrsluna.</span><span class="sxs-lookup"><span data-stu-id="e6447-125">If the machine time sheet is linked with a resource, then the user in the **Time Sheet Approver User ID** field on the resource card approves the time sheet.</span></span> |

## <a name="to-assign-a-time-sheet-administrator"></a><span data-ttu-id="e6447-126">Til að tilnefna vinnuskýrslustjóra</span><span class="sxs-lookup"><span data-stu-id="e6447-126">To assign a time sheet administrator</span></span>
1. <span data-ttu-id="e6447-127">Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Notandauppsetning** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="e6447-127">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **User Setup**, and then choose the related link.</span></span>  
2. <span data-ttu-id="e6447-128">Bæta við nýjum notanda ef notandalistinn inniheldur ekki einstaklinginn sem notandinn vill að sé vinnuskýrslustjórnandi.</span><span class="sxs-lookup"><span data-stu-id="e6447-128">Add a new user if the user list does not include the person who you want to be the time sheet administrator.</span></span> <span data-ttu-id="e6447-129">Nánari upplýsingar eru í [Hvernig á að: Vinna með notendur og heimildir](ui-how-users-permissions.md).</span><span class="sxs-lookup"><span data-stu-id="e6447-129">For more information, see [How to: Manage Users and Permissions](ui-how-users-permissions.md).</span></span>
3. <span data-ttu-id="e6447-130">Velja skal notanda sem á að vera vinnuskýrslustjóri og svo skal velja gátreitinn**Stjórnandi vinnuskýrslu**</span><span class="sxs-lookup"><span data-stu-id="e6447-130">Select a user to be a time sheet administrator, and then select the **Time Sheet Admin.**</span></span> <span data-ttu-id="e6447-131">.</span><span class="sxs-lookup"><span data-stu-id="e6447-131">check box.</span></span>  

> [!TIP]  
>   <span data-ttu-id="e6447-132">Mælt er með að aðeins einn notandi sé tilgreindur sem vinnuskýrslustjóri fyrir fyrirtæki.</span><span class="sxs-lookup"><span data-stu-id="e6447-132">It is recommended that you designate only one user to be the time sheet administrator for a company.</span></span> <span data-ttu-id="e6447-133">Í eftirfarandi ferli eru eigandi og samþykkjandi vinnuskýrslu settir upp þar sem samþykkjandi er tilgreindur fyrir hvern forða.</span><span class="sxs-lookup"><span data-stu-id="e6447-133">In the following procedure, you set up a time sheet owner and approver where the time sheet approver is assigned for each resource.</span></span>  

## <a name="to-assign-a-time-sheets-owner-and-approver"></a><span data-ttu-id="e6447-134">Til að tilgreina eiganda og samþykkjanda vinnuskýrslu</span><span class="sxs-lookup"><span data-stu-id="e6447-134">To assign a time sheets owner and approver</span></span>
1. <span data-ttu-id="e6447-135">Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Forði** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="e6447-135">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Resources**, and then choose the related link.</span></span>
2. <span data-ttu-id="e6447-136">Veljið forðann sem á að geta notað vinnuskýrslur og veljið svo gátreitinn **Nota vinnuskýrslu**.</span><span class="sxs-lookup"><span data-stu-id="e6447-136">Select the resource for which you want to set up the ability to use time sheets, and then select the **Use Time Sheet** check box.</span></span>  
3. <span data-ttu-id="e6447-137">Í reitinn **Notandakenni eiganda vinnuskýrslu** skal slá inn notandakenni eiganda vinnuskýrslunnar.</span><span class="sxs-lookup"><span data-stu-id="e6447-137">In the **Time Sheet Owner User ID** field, enter the ID of the owner of the time sheet.</span></span> <span data-ttu-id="e6447-138">Eigandinn getur fært inn tímanotkun á vinnuskýrslu og sent hana til samþykktar.</span><span class="sxs-lookup"><span data-stu-id="e6447-138">The owner can enter time usage on a time sheet and submit it for approval.</span></span> <span data-ttu-id="e6447-139">Þegar forði er einstaklingur er einstaklingurinn yfirleitt einnig eigandi.</span><span class="sxs-lookup"><span data-stu-id="e6447-139">In general, when the resource is a person, that person is also the owner.</span></span>  
4. <span data-ttu-id="e6447-140">Í reitinn **Notandakenni samþykkjanda vinnuskýrslu** skal slá inn notandakenni samþykkjanda vinnuskýrslunnar.</span><span class="sxs-lookup"><span data-stu-id="e6447-140">In the **Time Sheet Approver User ID** field, enter the ID of the approver of the time sheet.</span></span> <span data-ttu-id="e6447-141">Samþykkjandi getur samþykkt, hafnað eða enduropnað vinnuskýrslu.</span><span class="sxs-lookup"><span data-stu-id="e6447-141">The approver can approve, reject, or reopen a time sheet.</span></span>  

> [!NOTE]  
>   <span data-ttu-id="e6447-142">Ekki er hægt að auðkenni samþykkjanda vinnuskýrslu ef tíma fyrir eru tímaskýrslur sem ekki hefur verið unnið með og sem hafa stöðuna **Sent** eða **Opið**.</span><span class="sxs-lookup"><span data-stu-id="e6447-142">You cannot change the ID of the time sheet approver if there are time sheets that have not yet been processed and have the status of **Submitted** or **Open**.</span></span>

## <a name="see-also"></a><span data-ttu-id="e6447-143">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="e6447-143">See Also</span></span>
[<span data-ttu-id="e6447-144">Setja upp verkefnastjórnun</span><span class="sxs-lookup"><span data-stu-id="e6447-144">Setting Up Project Management</span></span>](projects-setup-projects.md)  
[<span data-ttu-id="e6447-145">Verkefnastjórnun</span><span class="sxs-lookup"><span data-stu-id="e6447-145">Project Management</span></span>](projects-manage-projects.md)  
[<span data-ttu-id="e6447-146">Fjármál</span><span class="sxs-lookup"><span data-stu-id="e6447-146">Finance</span></span>](finance.md)  
<span data-ttu-id="e6447-147">[Innkaup](purchasing-manage-purchasing.md)       </span><span class="sxs-lookup"><span data-stu-id="e6447-147">[Purchasing](purchasing-manage-purchasing.md)       </span></span>  
<span data-ttu-id="e6447-148">[Sala](sales-manage-sales.md)    </span><span class="sxs-lookup"><span data-stu-id="e6447-148">[Sales](sales-manage-sales.md)    </span></span>  
<span data-ttu-id="e6447-149">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="e6447-149">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

