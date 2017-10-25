---
title: "Verkflæði | Microsoft Docs"
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
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: f65c0e577e839928809f7afda3dbdb4c9b7702c8
ms.contentlocale: is-is
ms.lasthandoff: 09/22/2017

---
# <a name="workflow"></a><span data-ttu-id="ebbde-105">Verkflæði</span><span class="sxs-lookup"><span data-stu-id="ebbde-105">Workflow</span></span>
<span data-ttu-id="ebbde-106">Hægt er að setja upp og nota verkflæði sem tengja viðskiptaferlisverk sem framkvæmd erf af ólíkum notandi.</span><span class="sxs-lookup"><span data-stu-id="ebbde-106">You can set up and use workflows that connect business-process tasks performed by different users.</span></span> <span data-ttu-id="ebbde-107">Kerfisverk, s.s. sjálfvirk bókun, er hægt að hafa sem skerf í verkflæði, á undan eða eftir notandaverkum.</span><span class="sxs-lookup"><span data-stu-id="ebbde-107">System tasks, such as automatic posting, can be included as steps in workflows, preceded or followed by user tasks.</span></span> <span data-ttu-id="ebbde-108">Að óska eftir samþykki eða samþykkja nýjar færslur eru dæmigerð skref í verkflæði.</span><span class="sxs-lookup"><span data-stu-id="ebbde-108">Requesting and granting approval to create new records are typical workflow steps.</span></span>  

 <span data-ttu-id="ebbde-109">Í glugganum **Verkflæði** er hægt að stofna verkflæði með því að skrá viðkomandi skref í línurnar.</span><span class="sxs-lookup"><span data-stu-id="ebbde-109">In the **Workflow** window, you create a workflow by listing the involved steps on the lines.</span></span> <span data-ttu-id="ebbde-110">Hvert skref samanstendur af atburði verkflæðis, breytt eftir atburður skilyrði, og verkflæðissvar, breytt eftir svarvalkostir.</span><span class="sxs-lookup"><span data-stu-id="ebbde-110">Each step consists of a workflow event, moderated by event conditions, and a workflow response, moderated by response options.</span></span> <span data-ttu-id="ebbde-111">Þú skilgreinir skref í verkflæði með því að fylla út í reiti á verkflæðislínum úr föstum listum yfir tilvik og svör gildi sem standa fyrir verkflæðissviðsmyndir sem eru studd af kóða forritsins.</span><span class="sxs-lookup"><span data-stu-id="ebbde-111">You define workflow steps by filling fields on workflow lines from fixed lists of event and response values representing scenarios that are supported by the application code.</span></span>  

 <span data-ttu-id="ebbde-112">Almenna útgáfan af [!INCLUDE[d365fin](includes/d365fin_md.md)] inniheldur fjölda forstilltra verkflæða sem birtast í sniðmáti verkflæðis og þau er hægt að afrita til að stofna verkflæði.</span><span class="sxs-lookup"><span data-stu-id="ebbde-112">The generic version of [!INCLUDE[d365fin](includes/d365fin_md.md)] includes a number of preconfigured workflows represented by workflow templates that you can copy to create workflows.</span></span> <span data-ttu-id="ebbde-113">Kóðar fyrir verkflæðissniðmát sem bætt er við af Microsoft hafa forskeytið „MS-“.</span><span class="sxs-lookup"><span data-stu-id="ebbde-113">The code for workflow templates that are added by Microsoft are prefixed with “MS-“.</span></span> <span data-ttu-id="ebbde-114">Sjá nánari upplýsingar í lista yfir verkflæðissniðmát í glugganum Verkflæðissniðmát.</span><span class="sxs-lookup"><span data-stu-id="ebbde-114">For more information, see the list of workflow templates in the Workflow Templates window.</span></span>  

 <span data-ttu-id="ebbde-115">Ef viðskiptasviðsmynd kallar á verkflæðistilvik eða -viðbrögð sem ekki eru studd verður Microsoft-samstarfsaðili að virkja þau með því að sérstilla forritakóðann.</span><span class="sxs-lookup"><span data-stu-id="ebbde-115">If a business scenario requires a workflow event or response that is not supported, a Microsoft partner must implement them by customizing the application code.</span></span> <span data-ttu-id="ebbde-116">Nánari upplýsingar er að finna í [Sýnikennsla: Innleiðing nýrra verkflæðistilvika og svörunar](https://msdn.microsoft.com/en-us/library/mt574349.aspx) á MSDN.</span><span class="sxs-lookup"><span data-stu-id="ebbde-116">For more information, see [Walkthrough: Implementing New Workflow Events and Responses](https://msdn.microsoft.com/en-us/library/mt574349.aspx) on MSDN.</span></span>  

 <span data-ttu-id="ebbde-117">Eftirfarandi tafla lýsir röð verkefna með tenglum í efnisatriði þar sem þeim er lýst.</span><span class="sxs-lookup"><span data-stu-id="ebbde-117">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>  

|<span data-ttu-id="ebbde-118">**Til að**</span><span class="sxs-lookup"><span data-stu-id="ebbde-118">**To**</span></span>|<span data-ttu-id="ebbde-119">**Sjá**</span><span class="sxs-lookup"><span data-stu-id="ebbde-119">**See**</span></span>|  
|------------|-------------|  
|<span data-ttu-id="ebbde-120">Setja upp notendum verkflæðis, skilgreina hvernig notendur fá tilkynningu, og búa til ný verkflæði.</span><span class="sxs-lookup"><span data-stu-id="ebbde-120">Set up workflow users, specify how users get notified, and create new workflows.</span></span> <span data-ttu-id="ebbde-121">Til að skapa ný verkflæði fyrir óstuddar sviðsmyndir skal framkvæma umbeðnar verkflæðiseiningar með því að sérsníða kóða forrits.</span><span class="sxs-lookup"><span data-stu-id="ebbde-121">For new workflows for unsupported scenarios, implement the required workflow elements by customizing the application code.</span></span>|[<span data-ttu-id="ebbde-122">Uppsetning verkflæðis</span><span class="sxs-lookup"><span data-stu-id="ebbde-122">Setting Up Workflows</span></span>](across-set-up-workflows.md)|  
|<span data-ttu-id="ebbde-123">Virkja verkflæði, bregðast við tilkynningar verkflæðis, þ.m.t samþykktarbeiðnum og samþykkja beiðnir til að framkvæma skref í verkflæði.</span><span class="sxs-lookup"><span data-stu-id="ebbde-123">Enable workflows, act on workflow notifications, including request approvals and approve requests to perform a workflow step.</span></span> <span data-ttu-id="ebbde-124">Setja verkflæði í skjalasafn eða eyða.</span><span class="sxs-lookup"><span data-stu-id="ebbde-124">Archive and delete workflows.</span></span>|[<span data-ttu-id="ebbde-125">Nota verkflæði</span><span class="sxs-lookup"><span data-stu-id="ebbde-125">Using Workflows</span></span>](across-use-workflows.md)|  

## <a name="see-also"></a><span data-ttu-id="ebbde-126">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="ebbde-126">See Also</span></span>  
[<span data-ttu-id="ebbde-127">Sala</span><span class="sxs-lookup"><span data-stu-id="ebbde-127">Sales</span></span>](sales-manage-sales.md)  
[<span data-ttu-id="ebbde-128">Innkaup</span><span class="sxs-lookup"><span data-stu-id="ebbde-128">Purchasing</span></span>](purchasing-manage-purchasing.md)  
[<span data-ttu-id="ebbde-129">Stjórna verkum</span><span class="sxs-lookup"><span data-stu-id="ebbde-129">Managing Projects</span></span>](projects-manage-projects.md)  
<span data-ttu-id="ebbde-130">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="ebbde-130">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

