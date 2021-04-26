---
title: Setja upp vinnuskýrslur og samþykktarferli þeirra| Microsoft Docs
description: Þú setur upp vinnuskýrslu til að mæla tíma sem er notaður í verk og notkun forða, til að auðvelda þér verkefnastjórnun, mönnun og afkastaveitu.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project management, capacity, staff, resource
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 7134f45ef41400df1e44655d7a7e580da8dcb06b
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5780408"
---
# <a name="set-up-time-sheets"></a><span data-ttu-id="d797a-103">Setja upp vinnuskýrslur</span><span class="sxs-lookup"><span data-stu-id="d797a-103">Set Up Time Sheets</span></span>
<span data-ttu-id="d797a-104">Vinnuskjöl í [!INCLUDE[prod_short](includes/prod_short.md)] meðhöndla tímaskráningu í vikulegum stigum sjö daga.</span><span class="sxs-lookup"><span data-stu-id="d797a-104">Time sheets in [!INCLUDE[prod_short](includes/prod_short.md)] handle time registration in weekly increments of seven days.</span></span> <span data-ttu-id="d797a-105">Þær eru notaðar til að fylgjast með þeim tíma sem varið er í verk og hægt er að nota þær fyrir einfalda tímaskráningu forða.</span><span class="sxs-lookup"><span data-stu-id="d797a-105">You use them to track the time used on jobs, and you can use them to record simple resource time registration.</span></span> <span data-ttu-id="d797a-106">Áður en hægt er að nota vinnuskýrslur, verður að skilgreina hvernig þær eiga að vera settar upp og grunnstilltar.</span><span class="sxs-lookup"><span data-stu-id="d797a-106">Before you can use time sheets, you must specify how you want them to be set up and configured.</span></span>

<span data-ttu-id="d797a-107">Þegar búið er að setja upp hvernig fyrirtækið á að nota vinnuskýrslur er hægt að tilgreina hvort og hvernig tímaskýrslur eru samþykktar.</span><span class="sxs-lookup"><span data-stu-id="d797a-107">After you have set up how your organization will use time sheets, you can specify if and how time sheets are approved.</span></span> <span data-ttu-id="d797a-108">Allt eftir þörfum fyrirtækisins er hægt að tilgreina:</span><span class="sxs-lookup"><span data-stu-id="d797a-108">Depending on the needs of your organization, you can designate:</span></span>

* <span data-ttu-id="d797a-109">Einn eða fleiri notendur sem vinnuskýrslustjóra og sem samþykkja allar vinnuskýrslur.</span><span class="sxs-lookup"><span data-stu-id="d797a-109">One or more users as the time sheet administrator and approver for all time sheets.</span></span>
* <span data-ttu-id="d797a-110">Vinnuskýrslusamþykkjandi fyrir hvern forða.</span><span class="sxs-lookup"><span data-stu-id="d797a-110">A time sheet approver for each resource.</span></span>

<span data-ttu-id="d797a-111">Þegar búið er að setja upp vinnuskýrslur er hægt að búa til vinnuskýrslur fyrir forða, úthluta þeim á verkáætlunarlínur og bóka vinnuskýrslulínur.</span><span class="sxs-lookup"><span data-stu-id="d797a-111">When you have set up time sheets, you can create time sheets for resources, assign them to job planning lines, and post time sheet lines.</span></span> <span data-ttu-id="d797a-112">Frekari upplýsingar eru í [Nota vinnuskýrslur](projects-how-use-time-sheets.md).</span><span class="sxs-lookup"><span data-stu-id="d797a-112">For more information, see [Use Time Sheets](projects-how-use-time-sheets.md).</span></span>

## <a name="to-set-up-general-information-for-time-sheets"></a><span data-ttu-id="d797a-113">Til að setja upp almennar upplýsingar um vinnuskýrslur</span><span class="sxs-lookup"><span data-stu-id="d797a-113">To set up general information for time sheets</span></span>
1. <span data-ttu-id="d797a-114">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Uppsetning forða** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="d797a-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Resources Setup**, and then choose the related link.</span></span>  
2. <span data-ttu-id="d797a-115">Fyllið inn í svæðin eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="d797a-115">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="d797a-116">Í reitnum **Vinnuskýrslur eftir samþykkt verks** skal velja einn af eftirfarandi valkostum.</span><span class="sxs-lookup"><span data-stu-id="d797a-116">For the **Time Sheet by Job Approval** field, select one of the following options.</span></span>

| <span data-ttu-id="d797a-117">Valkostur</span><span class="sxs-lookup"><span data-stu-id="d797a-117">Option</span></span> | <span data-ttu-id="d797a-118">Lýsing</span><span class="sxs-lookup"><span data-stu-id="d797a-118">Description</span></span> |
| --- | --- |
| <span data-ttu-id="d797a-119">**Aldrei**</span><span class="sxs-lookup"><span data-stu-id="d797a-119">**Never**</span></span> |<span data-ttu-id="d797a-120">Notandinn í reitnum **Notandakenni samþykktaraðila vinnuskýrslu** á forðaspjaldinu samþykkir vinnuskýrsluna.</span><span class="sxs-lookup"><span data-stu-id="d797a-120">The user in the **Time Sheet Approver User ID** field on the resource card approves the time sheet.</span></span> |
| <span data-ttu-id="d797a-121">**Alltaf**</span><span class="sxs-lookup"><span data-stu-id="d797a-121">**Always**</span></span> |<span data-ttu-id="d797a-122">Notandinn í reitnum **Ábyrgðaraðili** á verkspjaldinu samþykkir vinnuskýrsluna.</span><span class="sxs-lookup"><span data-stu-id="d797a-122">The user in the **Person Responsible** field on the job card approves the time sheet.</span></span> |
| <span data-ttu-id="d797a-123">**Aðeins véla**</span><span class="sxs-lookup"><span data-stu-id="d797a-123">**Machine Only**</span></span> |<span data-ttu-id="d797a-124">Ef vinnuskýrsla vélar er tengd við verk er það notandinn í reitnum **Ábyrgðaraðili** á verkspjaldinu sem samþykkir vinnuskýrsluna.</span><span class="sxs-lookup"><span data-stu-id="d797a-124">If the machine time sheet is linked with a job, then the user in the **Person Responsible** field on the job card approves the time sheet.</span></span> <span data-ttu-id="d797a-125">Ef vinnuskýrsla vélar er tengd við forða er það notandinn í reitnum **Notandakenni samþykktaraðila vinnuskýrslu** á forðaspjaldinu sem samþykkir vinnuskýrsluna.</span><span class="sxs-lookup"><span data-stu-id="d797a-125">If the machine time sheet is linked with a resource, then the user in the **Time Sheet Approver User ID** field on the resource card approves the time sheet.</span></span> |

## <a name="to-assign-a-time-sheet-administrator"></a><span data-ttu-id="d797a-126">Til að tilnefna vinnuskýrslustjóra</span><span class="sxs-lookup"><span data-stu-id="d797a-126">To assign a time sheet administrator</span></span>
1. <span data-ttu-id="d797a-127">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Notandauppsetning** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="d797a-127">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **User Setup**, and then choose the related link.</span></span>  
2. <span data-ttu-id="d797a-128">Bæta við nýjum notanda ef notandalistinn inniheldur ekki einstaklinginn sem notandinn vill að sé vinnuskýrslustjórnandi.</span><span class="sxs-lookup"><span data-stu-id="d797a-128">Add a new user if the user list does not include the person who you want to be the time sheet administrator.</span></span> <span data-ttu-id="d797a-129">Frekari upplýsingar eru í [Úthluta leyfum til notenda og hópa](ui-define-granular-permissions.md).</span><span class="sxs-lookup"><span data-stu-id="d797a-129">For more information, see [Assign Permissions to Users and Groups](ui-define-granular-permissions.md).</span></span>
3. <span data-ttu-id="d797a-130">Velja skal notanda sem á að vera vinnuskýrslustjóri og svo skal velja gátreitinn **Stjórnandi vinnuskýrslu**</span><span class="sxs-lookup"><span data-stu-id="d797a-130">Select a user to be a time sheet administrator, and then select the **Time Sheet Admin.** check box.</span></span>  

> [!TIP]  
>   <span data-ttu-id="d797a-131">Mælt er með að aðeins einn notandi sé tilgreindur sem vinnuskýrslustjóri fyrir fyrirtæki.</span><span class="sxs-lookup"><span data-stu-id="d797a-131">It is recommended that you designate only one user to be the time sheet administrator for a company.</span></span> <span data-ttu-id="d797a-132">Í eftirfarandi ferli eru eigandi og samþykkjandi vinnuskýrslu settir upp þar sem samþykkjandi er tilgreindur fyrir hvern forða.</span><span class="sxs-lookup"><span data-stu-id="d797a-132">In the following procedure, you set up a time sheet owner and approver where the time sheet approver is assigned for each resource.</span></span>  

## <a name="to-assign-a-time-sheets-owner-and-approver"></a><span data-ttu-id="d797a-133">Til að tilgreina eiganda og samþykkjanda vinnuskýrslu</span><span class="sxs-lookup"><span data-stu-id="d797a-133">To assign a time sheets owner and approver</span></span>
1. <span data-ttu-id="d797a-134">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Forði** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="d797a-134">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Resources**, and then choose the related link.</span></span>
2. <span data-ttu-id="d797a-135">Veljið forðann sem á að geta notað vinnuskýrslur og veljið svo gátreitinn **Nota vinnuskýrslu**.</span><span class="sxs-lookup"><span data-stu-id="d797a-135">Select the resource for which you want to set up the ability to use time sheets, and then select the **Use Time Sheet** check box.</span></span>  
3. <span data-ttu-id="d797a-136">Í reitinn **Notandakenni eiganda vinnuskýrslu** skal slá inn notandakenni eiganda vinnuskýrslunnar.</span><span class="sxs-lookup"><span data-stu-id="d797a-136">In the **Time Sheet Owner User ID** field, enter the ID of the owner of the time sheet.</span></span> <span data-ttu-id="d797a-137">Eigandinn getur fært inn tímanotkun á vinnuskýrslu og sent hana til samþykktar.</span><span class="sxs-lookup"><span data-stu-id="d797a-137">The owner can enter time usage on a time sheet and submit it for approval.</span></span> <span data-ttu-id="d797a-138">Þegar forði er einstaklingur er einstaklingurinn yfirleitt einnig eigandi.</span><span class="sxs-lookup"><span data-stu-id="d797a-138">In general, when the resource is a person, that person is also the owner.</span></span>  
4. <span data-ttu-id="d797a-139">Í reitinn **Notandakenni samþykkjanda vinnuskýrslu** skal slá inn notandakenni samþykkjanda vinnuskýrslunnar.</span><span class="sxs-lookup"><span data-stu-id="d797a-139">In the **Time Sheet Approver User ID** field, enter the ID of the approver of the time sheet.</span></span> <span data-ttu-id="d797a-140">Samþykkjandi getur samþykkt, hafnað eða enduropnað vinnuskýrslu.</span><span class="sxs-lookup"><span data-stu-id="d797a-140">The approver can approve, reject, or reopen a time sheet.</span></span>  

> [!NOTE]  
>   <span data-ttu-id="d797a-141">Ekki er hægt að auðkenni samþykkjanda vinnuskýrslu ef tíma fyrir eru tímaskýrslur sem ekki hefur verið unnið með og sem hafa stöðuna **Sent** eða **Opið**.</span><span class="sxs-lookup"><span data-stu-id="d797a-141">You cannot change the ID of the time sheet approver if there are time sheets that have not yet been processed and have the status of **Submitted** or **Open**.</span></span>

## <a name="see-also"></a><span data-ttu-id="d797a-142">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="d797a-142">See Also</span></span>
[<span data-ttu-id="d797a-143">Setja upp verkefnastjórnun</span><span class="sxs-lookup"><span data-stu-id="d797a-143">Setting Up Project Management</span></span>](projects-setup-projects.md)  
[<span data-ttu-id="d797a-144">Verkefnastjórnun</span><span class="sxs-lookup"><span data-stu-id="d797a-144">Project Management</span></span>](projects-manage-projects.md)  
[<span data-ttu-id="d797a-145">Fjármál</span><span class="sxs-lookup"><span data-stu-id="d797a-145">Finance</span></span>](finance.md)  
<span data-ttu-id="d797a-146">[Innkaup](purchasing-manage-purchasing.md)       </span><span class="sxs-lookup"><span data-stu-id="d797a-146">[Purchasing](purchasing-manage-purchasing.md)       </span></span>  
<span data-ttu-id="d797a-147">[Sala](sales-manage-sales.md)    </span><span class="sxs-lookup"><span data-stu-id="d797a-147">[Sales](sales-manage-sales.md)    </span></span>  
<span data-ttu-id="d797a-148">[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="d797a-148">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  


[!INCLUDE[footer-include](includes/footer-banner.md)]