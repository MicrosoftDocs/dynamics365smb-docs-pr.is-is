---
title: Nota verkflæði
description: Hægt er að setja upp og nota verkflæði sem tengja viðskiptaferlisverk sem framkvæmd erf af ólíkum notandi. Frekari upplýsingar um mismunandi skref sem þú þarft að taka til að nota verkflæði.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 92b32957bb7b20dda304be8a99bb17c5c5947498
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5787008"
---
# <a name="using-workflows"></a><span data-ttu-id="98730-104">Nota verkflæði</span><span class="sxs-lookup"><span data-stu-id="98730-104">Using Workflows</span></span>
<span data-ttu-id="98730-105">Hægt er að setja upp og nota verkflæði sem tengja viðskiptaferlisverk sem framkvæmd erf af ólíkum notandi.</span><span class="sxs-lookup"><span data-stu-id="98730-105">You can set up and use workflows that connect business-process tasks performed by different users.</span></span> <span data-ttu-id="98730-106">Kerfisverk, s.s. sjálfvirk bókun, er hægt að hafa sem skerf í verkflæði, á undan eða eftir notandaverkum.</span><span class="sxs-lookup"><span data-stu-id="98730-106">System tasks, such as automatic posting, can be included as steps in workflows, preceded or followed by user tasks.</span></span> <span data-ttu-id="98730-107">Að óska eftir samþykki eða samþykkja nýjar færslur eru dæmigerð skref í verkflæði.</span><span class="sxs-lookup"><span data-stu-id="98730-107">Requesting and granting approval to create new records are typical workflow steps.</span></span>  

 <span data-ttu-id="98730-108">Áður en hægt er að byrja að nota verkflæði verður að setja upp notendur verkflæðis, stofna verkflæði, hugsanlega eftir að hafa sérsniðið kóða og tilgreina hvernig notendur fá tilkynningar.</span><span class="sxs-lookup"><span data-stu-id="98730-108">Before you can begin to use workflows, you must set up workflow users, create the workflows, potentially preceded by code customization and specify how users receive notifications.</span></span> <span data-ttu-id="98730-109">Nánari upplýsingar er að finna í [Uppsetning Verkflæði](across-set-up-workflows.md).</span><span class="sxs-lookup"><span data-stu-id="98730-109">For more information, see [Setting Up Workflows](across-set-up-workflows.md).</span></span>  

> [!NOTE]  
>  <span data-ttu-id="98730-110">Dæmigerð verkflæðisskref eru um notendur sem biðja um samþykki verka og samþykkjendur sem samþykkja eða hafna samþykktarbeiðnum.</span><span class="sxs-lookup"><span data-stu-id="98730-110">Typical workflow steps are about users who request approval of tasks and approvers accepting or rejecting approval requests.</span></span> <span data-ttu-id="98730-111">Því vísa mörg efni um hvernig nota eigi verkflæði til Samþykktir.</span><span class="sxs-lookup"><span data-stu-id="98730-111">Therefore, many topics about how to use workflows refer to approvals.</span></span>  

 <span data-ttu-id="98730-112">Eftirfarandi tafla lýsir röð verkefna með tenglum í efnisatriði þar sem þeim er lýst.</span><span class="sxs-lookup"><span data-stu-id="98730-112">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>  

|<span data-ttu-id="98730-113">**Til að**</span><span class="sxs-lookup"><span data-stu-id="98730-113">**To**</span></span>|<span data-ttu-id="98730-114">**Sjá**</span><span class="sxs-lookup"><span data-stu-id="98730-114">**See**</span></span>|  
|------------|-------------|  
|<span data-ttu-id="98730-115">Stilla verkflæði á að hefjast þegar fyrsta færslupunktstilvik á sér stað.</span><span class="sxs-lookup"><span data-stu-id="98730-115">Set a workflow to start when the first entry-point event occurs.</span></span>|[<span data-ttu-id="98730-116">Virkja verkflæði</span><span class="sxs-lookup"><span data-stu-id="98730-116">Enable Workflows</span></span>](across-how-to-enable-workflows.md)|  
|<span data-ttu-id="98730-117">Samþykktarbeiðni fyrir verk, sem samþykktaraðili samþykkirðu, hafnarðu eða úthlutar samþykktum, og sendir eða ferð yfir samþykktartilkynningar.</span><span class="sxs-lookup"><span data-stu-id="98730-117">Request approval of a task, as an approver, accept, decline, or delegate approvals, and send or view approval notifications.</span></span>|[<span data-ttu-id="98730-118">Nota Samþykktarverkflæði</span><span class="sxs-lookup"><span data-stu-id="98730-118">Use Approval Workflows</span></span>](across-how-use-approval-workflows.md)|  
|<span data-ttu-id="98730-119">Stofna verkflæðisskreft sem takmarka sérstakri færslugerð sé notuð áður en tiltekið tilvik á sér stað, til dæmis að færsla sé samþykkt.</span><span class="sxs-lookup"><span data-stu-id="98730-119">Create workflow steps that restrict a certain record type from being used before a certain event occurs, for example that the record is approved.</span></span>|[<span data-ttu-id="98730-120">Takmarka og heimila notkun á færslu</span><span class="sxs-lookup"><span data-stu-id="98730-120">Restrict and Allow Usage of a Record</span></span>](across-how-to-restrict-and-allow-usage-of-a-record.md)|  
|<span data-ttu-id="98730-121">Skoða verkflæðisskrefatilvik með stöðuna Lokið.</span><span class="sxs-lookup"><span data-stu-id="98730-121">View workflow step instances of status Completed.</span></span>|[<span data-ttu-id="98730-122">Skoða verkflæðisskrefstilvik í skráasafni</span><span class="sxs-lookup"><span data-stu-id="98730-122">View Archived Workflow Step Instances</span></span>](across-how-to-view-archived-workflow-step-instances.md)|  
|<span data-ttu-id="98730-123">Eyða verkflæði sem á örugglega ekki að nota aftur.</span><span class="sxs-lookup"><span data-stu-id="98730-123">Delete a workflow that you are sure will no longer be used.</span></span>|[<span data-ttu-id="98730-124">Eyða verkflæðum</span><span class="sxs-lookup"><span data-stu-id="98730-124">Delete Workflows</span></span>](across-how-to-delete-workflows.md)|  

## <a name="see-also"></a><span data-ttu-id="98730-125">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="98730-125">See Also</span></span>  
<span data-ttu-id="98730-126">[Uppsetning verkflæðis](across-set-up-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="98730-126">[Setting Up Workflows](across-set-up-workflows.md) </span></span>  
<span data-ttu-id="98730-127">[Verkflæði](across-workflow.md) </span><span class="sxs-lookup"><span data-stu-id="98730-127">[Workflow](across-workflow.md) </span></span>  
<span data-ttu-id="98730-128">[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="98730-128">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]