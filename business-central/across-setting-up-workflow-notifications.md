---
title: Tilkynningar verkflæðis
description: Mörg Verkflæðissvör snúast um að láta notendur vita að tilvik hafi átt sér stað og þeir þurfi að bregðast við því. Til dæmis getur eitt skref í verkflæði verið að tilvik óski eftir að Notandi 1 samþyki nýja færslu, og að svarið sé að tilkynning sé send til notanda 2, samþykkjanda. Í næsta verkflæðisskrefi getur tilvikið verið að Notandi 2 samþyki færsluna, og svarið að tilkynning sé send til notanda 3 til að hefja tengt ferli samþykktu færslunnar. Í öllum skref verkflæðis sem snúast um samþykki eru tilkynningar tengdar samþykktarfærslu.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: d72c3ba220c98d0c77806466f467ab233b3db65c
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5787047"
---
# <a name="workflow-notifications"></a><span data-ttu-id="a5385-106">Tilkynningar verkflæðis</span><span class="sxs-lookup"><span data-stu-id="a5385-106">Workflow Notifications</span></span>

<span data-ttu-id="a5385-107">Setja upp verkflæðin til að láta notendur vita sjálfkrafa þegar þeir þurfa að skoða skref í því verkflæði.</span><span class="sxs-lookup"><span data-stu-id="a5385-107">Set up your workflows to automatically notify users when their attention is required for a step in that workflow.</span></span> <span data-ttu-id="a5385-108">Mörg Verkflæðissvör snúast um að láta notendur vita að tilvik hafi átt sér stað og þeir þurfi að bregðast við því.</span><span class="sxs-lookup"><span data-stu-id="a5385-108">Many workflow responses are about notifying a user that an event has occurred that they must act on.</span></span> <span data-ttu-id="a5385-109">Til dæmis getur eitt skref í verkflæði verið að tilvik óski eftir að Notandi 1 samþyki nýja færslu, og að svarið sé að tilkynning sé send til notanda 2, samþykkjanda.</span><span class="sxs-lookup"><span data-stu-id="a5385-109">For example, on one workflow step, the event can be that User 1 requests approval of a new record, and the response is that a notification is sent to User 2, the approver.</span></span> <span data-ttu-id="a5385-110">Í næsta verkflæðisskrefi getur tilvikið verið að Notandi 2 samþyki færsluna, og svarið að tilkynning sé send til notanda 3 til að hefja tengt ferli samþykktu færslunnar.</span><span class="sxs-lookup"><span data-stu-id="a5385-110">On the next workflow step, the event can be that User 2 approves the record, and the response is that a notification is sent to User 3 to start a related processing of the approved record.</span></span> <span data-ttu-id="a5385-111">Í öllum skref verkflæðis sem snúast um samþykki eru tilkynningar tengdar samþykktarfærslu.</span><span class="sxs-lookup"><span data-stu-id="a5385-111">For workflow steps that are about approval, each notification is tied to an approval entry.</span></span> <span data-ttu-id="a5385-112">Frekari upplýsingar eru í [Verkflæði](across-workflow.md).</span><span class="sxs-lookup"><span data-stu-id="a5385-112">For more information, see [Workflow](across-workflow.md).</span></span>  

> [!NOTE]  
> <span data-ttu-id="a5385-113">Almenna útgáfan af [!INCLUDE[prod_short](includes/prod_short.md)] styður tilkynningar sem tölvupóst og innri athugasemdir.</span><span class="sxs-lookup"><span data-stu-id="a5385-113">The generic version of [!INCLUDE[prod_short](includes/prod_short.md)] supports notifications as email and as internal notes.</span></span>  

> [!IMPORTANT]  
> <span data-ttu-id="a5385-114">Allar verkflæðistilkynningar eru sendar um verkröð.</span><span class="sxs-lookup"><span data-stu-id="a5385-114">All workflow notifications are sent through a job queue.</span></span> <span data-ttu-id="a5385-115">Ganga skal úr skugga um að verkröð í uppsetningu sé sett upp þannig að hún meðhöndli verkflæðistilkynningar og að gátreiturinn **Byrja sjálfkrafa frá þjóni** sé valinn.</span><span class="sxs-lookup"><span data-stu-id="a5385-115">Make sure that the job queue in your installation is set up to handle workflow notifications, and that the **Start Automatically From Server** check box is selected.</span></span> <span data-ttu-id="a5385-116">Frekari upplýsingar, sjá [Nota verkraðir til að tímaraða verkhlutum](admin-job-queues-schedule-tasks.md).</span><span class="sxs-lookup"><span data-stu-id="a5385-116">For more information, see [Use Job Queues to Schedule Tasks](admin-job-queues-schedule-tasks.md).</span></span>

## <a name="set-up-notifications"></a><span data-ttu-id="a5385-117">Setja upp tilkynningar</span><span class="sxs-lookup"><span data-stu-id="a5385-117">Set up notifications</span></span>

<span data-ttu-id="a5385-118">Sett eru upp mismunandi verkflæðistilkynningar á viðkomandi stöðum:</span><span class="sxs-lookup"><span data-stu-id="a5385-118">You set up different aspects of workflow notifications in the following places:</span></span>  

* <span data-ttu-id="a5385-119">Tilkynning samþykktaraðila</span><span class="sxs-lookup"><span data-stu-id="a5385-119">Approver notification</span></span>

    <span data-ttu-id="a5385-120">Fyrir samþykktarverkflæði eru settir upp viðtakendur verkflæðistilkynninga með því að fylla út línu á síðunni **Notandauppsetning samþykktar** fyrir hvern notanda sem tekur þátt í verkflæðinu.</span><span class="sxs-lookup"><span data-stu-id="a5385-120">For approval workflows, you set up the recipients of workflow notifications by filling a line on the **Approval User Setup** page for each user that takes part in the workflow.</span></span>  

    <span data-ttu-id="a5385-121">Ef notandi 2 er t.d tilgreindur í **Kenni samþykktaraðila** reitnum á línu fyrir notanda 1 þá er tilkynning um samþykktarbeiðni send til notanda 1.</span><span class="sxs-lookup"><span data-stu-id="a5385-121">For example, if User 2 is specified in the **Approver ID** field on the line for User 1, then the approval request notification is sent to User 1.</span></span> <span data-ttu-id="a5385-122">Frekari upplýsingar eru í [Setja upp notendur samþykktar](across-how-to-set-up-approval-users.md).</span><span class="sxs-lookup"><span data-stu-id="a5385-122">For more information, see [Set Up Approval Users](across-how-to-set-up-approval-users.md).</span></span>  
* <span data-ttu-id="a5385-123">Áætlanir tilkynninga</span><span class="sxs-lookup"><span data-stu-id="a5385-123">Notification schedules</span></span>

    <span data-ttu-id="a5385-124">Hægt er að stilla hvenær og hvernig notendur fá tilkynningar verkflæðis með því að fylla út **Áætlun tilkynninga** síðuna fyrir hvern notanda verkflæðis.</span><span class="sxs-lookup"><span data-stu-id="a5385-124">You set up when and how users receive workflow notifications by filling the **Notification Schedule** page for each workflow user.</span></span> <span data-ttu-id="a5385-125">Frekari upplýsingar eru í [Tilgreina hvenær og hvernig á að fá tilkynningar](across-how-to-specify-when-and-how-to-receive-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="a5385-125">For more information, see [Specify When and How to Receive Notifications](across-how-to-specify-when-and-how-to-receive-notifications.md).</span></span>  
* <span data-ttu-id="a5385-126">Sérsníða tilkynningar í tölvupósti</span><span class="sxs-lookup"><span data-stu-id="a5385-126">Customize the email notifications</span></span>

    <span data-ttu-id="a5385-127">Ef þú vilt geturðu sérsniðið innihald á tilkynningu tölvupósts með því að breyta skýrslu 1320, Tilkynningapóstur.</span><span class="sxs-lookup"><span data-stu-id="a5385-127">If you want, you can customize the content of the email notification by modifying report 1320, Notification Email.</span></span> <span data-ttu-id="a5385-128">Nánari upplýsingar er að finna í [Búa til og breyta sérsniðnum skýrsluútlitum](ui-how-create-custom-report-layout.md).</span><span class="sxs-lookup"><span data-stu-id="a5385-128">For more information, see [Create and Modify Custom Report Layouts](ui-how-create-custom-report-layout.md).</span></span>  
* <span data-ttu-id="a5385-129">Svarmöguleikar</span><span class="sxs-lookup"><span data-stu-id="a5385-129">Response options</span></span>

    <span data-ttu-id="a5385-130">Sett er upp tiltekið efni og reglur um tilkynningar verkflæðis þegar verkflæðið er stofnað.</span><span class="sxs-lookup"><span data-stu-id="a5385-130">You set up specific content and rules of a workflow notification when you create the workflow in question.</span></span> <span data-ttu-id="a5385-131">Þetta er gert með því að velja valkosti á síðunni **Valkostir fyrir verkflæðissvar** fyrir verkflæðissvarið sem táknar tilkynninguna.</span><span class="sxs-lookup"><span data-stu-id="a5385-131">You do this by selecting options on the **Workflow Response Options** page for the workflow response that represents the notification.</span></span> <span data-ttu-id="a5385-132">Frekari upplýsingar eru í skrefi 9 í [Stofna verkflæði](across-how-to-create-workflows.md).</span><span class="sxs-lookup"><span data-stu-id="a5385-132">For more information, see step 9 in [Create Workflows](across-how-to-create-workflows.md).</span></span>  

* <span data-ttu-id="a5385-133">Tilkynna sendanda</span><span class="sxs-lookup"><span data-stu-id="a5385-133">Notify sender</span></span>

    <span data-ttu-id="a5385-134">Fyrir samþykktarverkflæði skal bæta við svarskrefi verkflæðis til að tilkynna sendanda þegar beiðni hefur verið samþykkt eða henni hafnað.</span><span class="sxs-lookup"><span data-stu-id="a5385-134">For approval workflows, add a workflow response step to notify the sender when the request has been approved or rejected.</span></span> <span data-ttu-id="a5385-135">Frekari upplýsingar eru í skrefi 9 í [Stofna verkflæði](across-how-to-create-workflows.md).</span><span class="sxs-lookup"><span data-stu-id="a5385-135">For more information, see step 9 in [Create Workflows](across-how-to-create-workflows.md).</span></span>  

## <a name="see-also"></a><span data-ttu-id="a5385-136">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="a5385-136">See Also</span></span>

[<span data-ttu-id="a5385-137">Setja upp notendur samþykktar</span><span class="sxs-lookup"><span data-stu-id="a5385-137">Set Up Approval Users</span></span>](across-how-to-set-up-approval-users.md)  
[<span data-ttu-id="a5385-138">Setja upp notendur verkflæðis</span><span class="sxs-lookup"><span data-stu-id="a5385-138">Set Up Workflow Users</span></span>](across-how-to-set-up-workflow-users.md)  
[<span data-ttu-id="a5385-139">Tilgreina hvenær og hvernig á að fá tilkynningar</span><span class="sxs-lookup"><span data-stu-id="a5385-139">Specify When and How to Receive Notifications</span></span>](across-how-to-specify-when-and-how-to-receive-notifications.md)  
[<span data-ttu-id="a5385-140">Búa til verkflæði</span><span class="sxs-lookup"><span data-stu-id="a5385-140">Create Workflows</span></span>](across-how-to-create-workflows.md)  
[<span data-ttu-id="a5385-141">Búa til og breyta sérsniðnum skýrsluútlitum</span><span class="sxs-lookup"><span data-stu-id="a5385-141">Create and Modify Custom Report Layouts</span></span>](ui-how-create-custom-report-layout.md)  
[<span data-ttu-id="a5385-142">Nota verkraðir til að tímaraða verkhlutum</span><span class="sxs-lookup"><span data-stu-id="a5385-142">Use Job Queues to Schedule Tasks</span></span>](admin-job-queues-schedule-tasks.md)  
[<span data-ttu-id="a5385-143">Setja upp tölvupóst</span><span class="sxs-lookup"><span data-stu-id="a5385-143">Set up Email</span></span>](admin-how-setup-email.md)  
[<span data-ttu-id="a5385-144">Kynning: Uppsetning og notkun á samþykktarverkflæði innkaupa</span><span class="sxs-lookup"><span data-stu-id="a5385-144">Walkthrough: Setting Up and Using a Purchase Approval Workflow</span></span>](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
[<span data-ttu-id="a5385-145">Verkflæði</span><span class="sxs-lookup"><span data-stu-id="a5385-145">Workflow</span></span>](across-workflow.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]