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
ms.search.keywords: project management, capacity, staff, resource, time sheet
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 778d9c4308d28be804d7f1572335bd160faad6d8
ms.sourcegitcommit: 1aab52477956bf1aa7376fc7fb984644bc398c61
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/04/2021
ms.locfileid: "6184300"
---
# <a name="set-up-time-sheets"></a><span data-ttu-id="00b4d-103">Setja upp vinnuskýrslur</span><span class="sxs-lookup"><span data-stu-id="00b4d-103">Set Up Time Sheets</span></span>
<span data-ttu-id="00b4d-104">Vinnuskjöl í [!INCLUDE[prod_short](includes/prod_short.md)] meðhöndla tímaskráningu í vikulegum stigum sjö daga.</span><span class="sxs-lookup"><span data-stu-id="00b4d-104">Time sheets in [!INCLUDE[prod_short](includes/prod_short.md)] handle time registration in weekly increments of seven days.</span></span> <span data-ttu-id="00b4d-105">Þær eru notaðar til að fylgjast með þeim tíma sem varið er í verk og hægt er að nota þær fyrir einfalda tímaskráningu forða.</span><span class="sxs-lookup"><span data-stu-id="00b4d-105">You use them to track the time used on jobs, and you can use them to record simple resource time registration.</span></span> <span data-ttu-id="00b4d-106">Áður en hægt er að nota vinnuskýrslur, verður að skilgreina hvernig þær eiga að vera settar upp og grunnstilltar.</span><span class="sxs-lookup"><span data-stu-id="00b4d-106">Before you can use time sheets, you must specify how you want them to be set up and configured.</span></span>

<span data-ttu-id="00b4d-107">Þegar búið er að setja upp hvernig fyrirtækið á að nota vinnuskýrslur er hægt að tilgreina hvort og hvernig tímaskýrslur eru samþykktar.</span><span class="sxs-lookup"><span data-stu-id="00b4d-107">After you have set up how your organization will use time sheets, you can specify if and how time sheets are approved.</span></span> <span data-ttu-id="00b4d-108">Allt eftir þörfum fyrirtækisins er hægt að tilgreina:</span><span class="sxs-lookup"><span data-stu-id="00b4d-108">Depending on the needs of your organization, you can designate:</span></span>

* <span data-ttu-id="00b4d-109">Einn eða fleiri notendur sem vinnuskýrslustjóra og sem samþykkja allar vinnuskýrslur.</span><span class="sxs-lookup"><span data-stu-id="00b4d-109">One or more users as the time sheet administrator and approver for all time sheets.</span></span>
* <span data-ttu-id="00b4d-110">Vinnuskýrslusamþykkjandi fyrir hvern forða.</span><span class="sxs-lookup"><span data-stu-id="00b4d-110">A time sheet approver for each resource.</span></span>

<span data-ttu-id="00b4d-111">Þegar búið er að setja upp vinnuskýrslur er hægt að búa til vinnuskýrslur fyrir forða, úthluta þeim á verkáætlunarlínur og bóka vinnuskýrslulínur.</span><span class="sxs-lookup"><span data-stu-id="00b4d-111">When you have set up time sheets, you can create time sheets for resources, assign them to job planning lines, and post time sheet lines.</span></span> <span data-ttu-id="00b4d-112">Frekari upplýsingar eru í [Nota vinnuskýrslur](projects-how-use-time-sheets.md).</span><span class="sxs-lookup"><span data-stu-id="00b4d-112">For more information, see [Use Time Sheets](projects-how-use-time-sheets.md).</span></span>

## <a name="to-set-up-general-information-for-time-sheets"></a><span data-ttu-id="00b4d-113">Til að setja upp almennar upplýsingar um vinnuskýrslur</span><span class="sxs-lookup"><span data-stu-id="00b4d-113">To set up general information for time sheets</span></span>
1. <span data-ttu-id="00b4d-114">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Uppsetning forða** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="00b4d-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Resources Setup**, and then choose the related link.</span></span>  
2. <span data-ttu-id="00b4d-115">Fyllið inn í svæðin eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="00b4d-115">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="00b4d-116">Í reitnum **Vinnuskýrslur eftir samþykkt verks** skal velja einn af eftirfarandi valkostum.</span><span class="sxs-lookup"><span data-stu-id="00b4d-116">For the **Time Sheet by Job Approval** field, select one of the following options.</span></span>

| <span data-ttu-id="00b4d-117">Valkostur</span><span class="sxs-lookup"><span data-stu-id="00b4d-117">Option</span></span> | <span data-ttu-id="00b4d-118">Lýsing</span><span class="sxs-lookup"><span data-stu-id="00b4d-118">Description</span></span> |
| --- | --- |
| <span data-ttu-id="00b4d-119">**Aldrei**</span><span class="sxs-lookup"><span data-stu-id="00b4d-119">**Never**</span></span> |<span data-ttu-id="00b4d-120">Notandinn í reitnum **Notandakenni samþykktaraðila vinnuskýrslu** á forðaspjaldinu samþykkir vinnuskýrsluna.</span><span class="sxs-lookup"><span data-stu-id="00b4d-120">The user in the **Time Sheet Approver User ID** field on the resource card approves the time sheet.</span></span> |
| <span data-ttu-id="00b4d-121">**Alltaf**</span><span class="sxs-lookup"><span data-stu-id="00b4d-121">**Always**</span></span> |<span data-ttu-id="00b4d-122">Notandinn í reitnum **Ábyrgðaraðili** á verkspjaldinu samþykkir vinnuskýrsluna.</span><span class="sxs-lookup"><span data-stu-id="00b4d-122">The user in the **Person Responsible** field on the job card approves the time sheet.</span></span> |
| <span data-ttu-id="00b4d-123">**Aðeins véla**</span><span class="sxs-lookup"><span data-stu-id="00b4d-123">**Machine Only**</span></span> |<span data-ttu-id="00b4d-124">Ef vinnuskýrsla vélar er tengd við verk er það notandinn í reitnum **Ábyrgðaraðili** á verkspjaldinu sem samþykkir vinnuskýrsluna.</span><span class="sxs-lookup"><span data-stu-id="00b4d-124">If the machine time sheet is linked with a job, then the user in the **Person Responsible** field on the job card approves the time sheet.</span></span> <span data-ttu-id="00b4d-125">Ef vinnuskýrsla vélar er tengd við forða er það notandinn í reitnum **Notandakenni samþykktaraðila vinnuskýrslu** á forðaspjaldinu sem samþykkir vinnuskýrsluna.</span><span class="sxs-lookup"><span data-stu-id="00b4d-125">If the machine time sheet is linked with a resource, then the user in the **Time Sheet Approver User ID** field on the resource card approves the time sheet.</span></span> |

## <a name="to-assign-a-time-sheet-administrator"></a><span data-ttu-id="00b4d-126">Til að tilnefna vinnuskýrslustjóra</span><span class="sxs-lookup"><span data-stu-id="00b4d-126">To assign a time sheet administrator</span></span>
1. <span data-ttu-id="00b4d-127">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Notandauppsetning** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="00b4d-127">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **User Setup**, and then choose the related link.</span></span>  
2. <span data-ttu-id="00b4d-128">Bæta við nýjum notanda ef notandalistinn inniheldur ekki einstaklinginn sem notandinn vill að sé vinnuskýrslustjórnandi.</span><span class="sxs-lookup"><span data-stu-id="00b4d-128">Add a new user if the user list does not include the person who you want to be the time sheet administrator.</span></span> <span data-ttu-id="00b4d-129">Frekari upplýsingar eru í [Úthluta leyfum til notenda og hópa](ui-define-granular-permissions.md).</span><span class="sxs-lookup"><span data-stu-id="00b4d-129">For more information, see [Assign Permissions to Users and Groups](ui-define-granular-permissions.md).</span></span>
3. <span data-ttu-id="00b4d-130">Velja skal notanda sem á að vera vinnuskýrslustjóri og svo skal velja gátreitinn **Stjórnandi vinnuskýrslu**</span><span class="sxs-lookup"><span data-stu-id="00b4d-130">Select a user to be a time sheet administrator, and then select the **Time Sheet Admin.** check box.</span></span>  

> [!TIP]  
>   <span data-ttu-id="00b4d-131">Mælt er með að aðeins einn notandi sé tilgreindur sem vinnuskýrslustjóri fyrir fyrirtæki.</span><span class="sxs-lookup"><span data-stu-id="00b4d-131">It is recommended that you designate only one user to be the time sheet administrator for a company.</span></span> <span data-ttu-id="00b4d-132">Í eftirfarandi ferli eru eigandi og samþykkjandi vinnuskýrslu settir upp þar sem samþykkjandi er tilgreindur fyrir hvern forða.</span><span class="sxs-lookup"><span data-stu-id="00b4d-132">In the following procedure, you set up a time sheet owner and approver where the time sheet approver is assigned for each resource.</span></span>  

## <a name="to-assign-a-time-sheets-owner-and-approver"></a><span data-ttu-id="00b4d-133">Til að tilgreina eiganda og samþykkjanda vinnuskýrslu</span><span class="sxs-lookup"><span data-stu-id="00b4d-133">To assign a time sheets owner and approver</span></span>
1. <span data-ttu-id="00b4d-134">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Forði** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="00b4d-134">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Resources**, and then choose the related link.</span></span>
2. <span data-ttu-id="00b4d-135">Veljið forðann sem á að geta notað vinnuskýrslur og veljið svo gátreitinn **Nota vinnuskýrslu**.</span><span class="sxs-lookup"><span data-stu-id="00b4d-135">Select the resource for which you want to set up the ability to use time sheets, and then select the **Use Time Sheet** check box.</span></span>  
3. <span data-ttu-id="00b4d-136">Í reitinn **Notandakenni eiganda vinnuskýrslu** skal slá inn notandakenni eiganda vinnuskýrslunnar.</span><span class="sxs-lookup"><span data-stu-id="00b4d-136">In the **Time Sheet Owner User ID** field, enter the ID of the owner of the time sheet.</span></span> <span data-ttu-id="00b4d-137">Eigandinn getur fært inn tímanotkun á vinnuskýrslu og sent hana til samþykktar.</span><span class="sxs-lookup"><span data-stu-id="00b4d-137">The owner can enter time usage on a time sheet and submit it for approval.</span></span> <span data-ttu-id="00b4d-138">Þegar forði er einstaklingur er einstaklingurinn yfirleitt einnig eigandi.</span><span class="sxs-lookup"><span data-stu-id="00b4d-138">In general, when the resource is a person, that person is also the owner.</span></span>  
4. <span data-ttu-id="00b4d-139">Í reitinn **Notandakenni samþykkjanda vinnuskýrslu** skal slá inn notandakenni samþykkjanda vinnuskýrslunnar.</span><span class="sxs-lookup"><span data-stu-id="00b4d-139">In the **Time Sheet Approver User ID** field, enter the ID of the approver of the time sheet.</span></span> <span data-ttu-id="00b4d-140">Samþykkjandi getur samþykkt, hafnað eða enduropnað vinnuskýrslu.</span><span class="sxs-lookup"><span data-stu-id="00b4d-140">The approver can approve, reject, or reopen a time sheet.</span></span>  

> [!NOTE]  
>   <span data-ttu-id="00b4d-141">Ekki er hægt að auðkenni samþykkjanda vinnuskýrslu ef tíma fyrir eru tímaskýrslur sem ekki hefur verið unnið með og sem hafa stöðuna **Sent** eða **Opið**.</span><span class="sxs-lookup"><span data-stu-id="00b4d-141">You cannot change the ID of the time sheet approver if there are time sheets that have not yet been processed and have the status of **Submitted** or **Open**.</span></span>

## <a name="see-also"></a><span data-ttu-id="00b4d-142">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="00b4d-142">See Also</span></span>
[<span data-ttu-id="00b4d-143">Setja upp verkefnastjórnun</span><span class="sxs-lookup"><span data-stu-id="00b4d-143">Setting Up Project Management</span></span>](projects-setup-projects.md)  
[<span data-ttu-id="00b4d-144">Verkefnastjórnun</span><span class="sxs-lookup"><span data-stu-id="00b4d-144">Project Management</span></span>](projects-manage-projects.md)  
[<span data-ttu-id="00b4d-145">Fjármál</span><span class="sxs-lookup"><span data-stu-id="00b4d-145">Finance</span></span>](finance.md)  
<span data-ttu-id="00b4d-146">[Innkaup](purchasing-manage-purchasing.md)       </span><span class="sxs-lookup"><span data-stu-id="00b4d-146">[Purchasing](purchasing-manage-purchasing.md)       </span></span>  
<span data-ttu-id="00b4d-147">[Sala](sales-manage-sales.md)    </span><span class="sxs-lookup"><span data-stu-id="00b4d-147">[Sales](sales-manage-sales.md)    </span></span>  
<span data-ttu-id="00b4d-148">[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="00b4d-148">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  


[!INCLUDE[footer-include](includes/footer-banner.md)]