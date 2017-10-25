---
title: "Notkun verkflæðis | Microsoft Docs"
description: "Hægt er að setja upp og nota verkflæði sem tengja viðskiptaferlisverk sem framkvæmd erf af ólíkum notandi. Kerfisverk, s.s. sjálfvirk bókun, er hægt að hafa sem skerf í verkflæði, á undan eða eftir notandaverkum. Að óska eftir samþykki eða samþykkja nýjar færslur eru dæmigerð skref í verkflæði."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/04/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: a42e336dba385cbf24c19702ad64d76b26c15104
ms.contentlocale: is-is
ms.lasthandoff: 09/22/2017

---
# <a name="using-workflows"></a><span data-ttu-id="41d54-105">Nota verkflæði</span><span class="sxs-lookup"><span data-stu-id="41d54-105">Using Workflows</span></span>
<span data-ttu-id="41d54-106">Hægt er að setja upp og nota verkflæði sem tengja viðskiptaferlisverk sem framkvæmd erf af ólíkum notandi.</span><span class="sxs-lookup"><span data-stu-id="41d54-106">You can set up and use workflows that connect business-process tasks performed by different users.</span></span> <span data-ttu-id="41d54-107">Kerfisverk, s.s. sjálfvirk bókun, er hægt að hafa sem skerf í verkflæði, á undan eða eftir notandaverkum.</span><span class="sxs-lookup"><span data-stu-id="41d54-107">System tasks, such as automatic posting, can be included as steps in workflows, preceded or followed by user tasks.</span></span> <span data-ttu-id="41d54-108">Að óska eftir samþykki eða samþykkja nýjar færslur eru dæmigerð skref í verkflæði.</span><span class="sxs-lookup"><span data-stu-id="41d54-108">Requesting and granting approval to create new records are typical workflow steps.</span></span>  

 <span data-ttu-id="41d54-109">Áður en hægt er að byrja að nota verkflæði verður að setja upp notendur verkflæðis, stofna verkflæði, hugsanlega eftir að hafa sérsniðið kóða og tilgreina hvernig notendur fá tilkynningar.</span><span class="sxs-lookup"><span data-stu-id="41d54-109">Before you can begin to use workflows, you must set up workflow users, create the workflows, potentially preceded by code customization and specify how users receive notifications.</span></span> <span data-ttu-id="41d54-110">Nánari upplýsingar er að finna í [Uppsetning Verkflæði](across-set-up-workflows.md).</span><span class="sxs-lookup"><span data-stu-id="41d54-110">For more information, see [Setting Up Workflows](across-set-up-workflows.md).</span></span>  

> [!NOTE]  
>  <span data-ttu-id="41d54-111">Dæmigerð verkflæðisskref eru um notendur sem biðja um samþykki verka og samþykkjendur sem samþykkja eða hafna samþykktarbeiðnum.</span><span class="sxs-lookup"><span data-stu-id="41d54-111">Typical workflow steps are about users who request approval of tasks and approvers accepting or rejecting approval requests.</span></span> <span data-ttu-id="41d54-112">Því vísa mörg efni um hvernig nota eigi verkflæði til Samþykktir.</span><span class="sxs-lookup"><span data-stu-id="41d54-112">Therefore, many topics about how to use workflows refer to approvals.</span></span>  

 <span data-ttu-id="41d54-113">Eftirfarandi tafla lýsir röð verkefna með tenglum í efnisatriði þar sem þeim er lýst.</span><span class="sxs-lookup"><span data-stu-id="41d54-113">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>  

|<span data-ttu-id="41d54-114">**Til að**</span><span class="sxs-lookup"><span data-stu-id="41d54-114">**To**</span></span>|<span data-ttu-id="41d54-115">**Sjá**</span><span class="sxs-lookup"><span data-stu-id="41d54-115">**See**</span></span>|  
|------------|-------------|  
|<span data-ttu-id="41d54-116">Stilla verkflæði á að hefjast þegar fyrsta færslupunktstilvik á sér stað.</span><span class="sxs-lookup"><span data-stu-id="41d54-116">Set a workflow to start when the first entry-point event occurs.</span></span>|[<span data-ttu-id="41d54-117">Hvernig á að: Virkja verkflæði</span><span class="sxs-lookup"><span data-stu-id="41d54-117">How to: Enable Workflows</span></span>](across-how-to-enable-workflows.md)|  
|<span data-ttu-id="41d54-118">Samþykktarbeiðni fyrir verk, sem samþykktaraðili samþykkirðu, hafnarðu eða úthlutar samþykktum, og sendir eða ferð yfir samþykktartilkynningar.</span><span class="sxs-lookup"><span data-stu-id="41d54-118">Request approval of a task, as an approver, accept, decline, or delegate approvals, and send or view approval notifications.</span></span>|[<span data-ttu-id="41d54-119">Hvernig á að: Nota samþykktarverkflæði</span><span class="sxs-lookup"><span data-stu-id="41d54-119">How to: Use Approval Workflows</span></span>](across-how-use-approval-workflows.md)|  
|<span data-ttu-id="41d54-120">Stofna verkflæðisskreft sem takmarka sérstakri færslugerð sé notuð áður en tiltekið tilvik á sér stað, til dæmis að færsla sé samþykkt.</span><span class="sxs-lookup"><span data-stu-id="41d54-120">Create workflow steps that restrict a certain record type from being used before a certain event occurs, for example that the record is approved.</span></span>|[<span data-ttu-id="41d54-121">Hvernig á að takmarka og heimila notkun á færslu</span><span class="sxs-lookup"><span data-stu-id="41d54-121">How to: Restrict and Allow Usage of a Record</span></span>](across-how-to-restrict-and-allow-usage-of-a-record.md)|  
|<span data-ttu-id="41d54-122">Skoða verkflæðisskrefatilvik með stöðuna Lokið.</span><span class="sxs-lookup"><span data-stu-id="41d54-122">View workflow step instances of status Completed.</span></span>|[<span data-ttu-id="41d54-123">Hvernig á að: Skoða verkflæðisskrefstilvik í skráasafni</span><span class="sxs-lookup"><span data-stu-id="41d54-123">How to: View Archived Workflow Step Instances</span></span>](across-how-to-view-archived-workflow-step-instances.md)|  
|<span data-ttu-id="41d54-124">Eyða verkflæði sem á örugglega ekki að nota aftur.</span><span class="sxs-lookup"><span data-stu-id="41d54-124">Delete a workflow that you are sure will no longer be used.</span></span>|[<span data-ttu-id="41d54-125">Hvernig á að: Eyða verkflæðum</span><span class="sxs-lookup"><span data-stu-id="41d54-125">How to: Delete Workflows</span></span>](across-how-to-delete-workflows.md)|  

## <a name="see-also"></a><span data-ttu-id="41d54-126">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="41d54-126">See Also</span></span>  
<span data-ttu-id="41d54-127">[Uppsetning verkflæðis](across-set-up-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="41d54-127">[Setting Up Workflows](across-set-up-workflows.md) </span></span>  
<span data-ttu-id="41d54-128">[Verkflæði](across-workflow.md) </span><span class="sxs-lookup"><span data-stu-id="41d54-128">[Workflow](across-workflow.md) </span></span>  
<span data-ttu-id="41d54-129">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="41d54-129">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

