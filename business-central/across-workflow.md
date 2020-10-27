---
title: Verkflæði | Microsoft Docs
description: Hægt er að setja upp og nota verkflæði sem tengja viðskiptaferlisverk sem framkvæmd erf af ólíkum notandi. Kerfisverk, s.s. sjálfvirk bókun, er hægt að hafa sem skerf í verkflæði, á undan eða eftir notandaverkum. Að óska eftir samþykki eða samþykkja nýjar færslur eru dæmigerð skref í verkflæði.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 1685ca2ab698cad1b1c7a84f65b5633d1234624b
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/01/2020
ms.locfileid: "3927248"
---
# <a name="workflows-in-dynamics-365-business-central"></a><span data-ttu-id="e2392-105">Verkflæði í Dynamics 365 Business Central</span><span class="sxs-lookup"><span data-stu-id="e2392-105">Workflows in Dynamics 365 Business Central</span></span>

<span data-ttu-id="e2392-106">Hægt er að setja upp og nota verkflæði sem tengja viðskiptaferlisverk sem framkvæmd erf af ólíkum notandi.</span><span class="sxs-lookup"><span data-stu-id="e2392-106">You can set up and use workflows that connect business-process tasks performed by different users.</span></span> <span data-ttu-id="e2392-107">Kerfisverk, s.s. sjálfvirk bókun, er hægt að hafa sem skerf í verkflæði, á undan eða eftir notandaverkum.</span><span class="sxs-lookup"><span data-stu-id="e2392-107">System tasks, such as automatic posting, can be included as steps in workflows, preceded or followed by user tasks.</span></span> <span data-ttu-id="e2392-108">Að óska eftir samþykki eða samþykkja nýjar færslur eru dæmigerð skref í verkflæði.</span><span class="sxs-lookup"><span data-stu-id="e2392-108">Requesting and granting approval to create new records are typical workflow steps.</span></span>  

 <span data-ttu-id="e2392-109">Á síðunni **Verkflæði** er hægt að stofna verkflæði með því að skrá viðkomandi skref í línurnar.</span><span class="sxs-lookup"><span data-stu-id="e2392-109">On the **Workflow** page, you create a workflow by listing the involved steps on the lines.</span></span> <span data-ttu-id="e2392-110">Hvert skref samanstendur af atburði verkflæðis, breytt eftir atburður skilyrði, og verkflæðissvar, breytt eftir svarvalkostir.</span><span class="sxs-lookup"><span data-stu-id="e2392-110">Each step consists of a workflow event, moderated by event conditions, and a workflow response, moderated by response options.</span></span> <span data-ttu-id="e2392-111">Þú skilgreinir skref í verkflæði með því að fylla út í reiti á verkflæðislínum úr föstum listum yfir tilvik og svör gildi sem standa fyrir verkflæðissviðsmyndir sem eru studd af kóða forritsins.</span><span class="sxs-lookup"><span data-stu-id="e2392-111">You define workflow steps by filling fields on workflow lines from fixed lists of event and response values representing scenarios that are supported by the application code.</span></span>  

 <span data-ttu-id="e2392-112">Almenna útgáfan af [!INCLUDE[d365fin](includes/d365fin_md.md)] inniheldur fjölda forstilltra verkflæða sem birtast í sniðmáti verkflæðis og þau er hægt að afrita til að stofna verkflæði.</span><span class="sxs-lookup"><span data-stu-id="e2392-112">The generic version of [!INCLUDE[d365fin](includes/d365fin_md.md)] includes a number of preconfigured workflows represented by workflow templates that you can copy to create workflows.</span></span> <span data-ttu-id="e2392-113">Kóðar fyrir verkflæðissniðmát sem bætt er við af Microsoft hafa forskeytið „MS-“.</span><span class="sxs-lookup"><span data-stu-id="e2392-113">The code for workflow templates that are added by Microsoft are prefixed with “MS-“.</span></span> <span data-ttu-id="e2392-114">Sjá nánari upplýsingar í lista yfir verkflæðissniðmát á síðunni Verkflæðissniðmát.</span><span class="sxs-lookup"><span data-stu-id="e2392-114">For more information, see the list of workflow templates in the Workflow Templates page.</span></span>  

 <span data-ttu-id="e2392-115">Ef viðskiptaaðstæður krefjast verkflæðistilviks eða svars sem ekki er stutt er annað hvort hægt að nota Power Automate eða vinna með Microsoft-samstarfsaðila til að sérsníða forritskóða.</span><span class="sxs-lookup"><span data-stu-id="e2392-115">If a business scenario requires a workflow event or response that is not supported, you can either use Power Automate or work with a Microsoft partner to customize the application code.</span></span> <span data-ttu-id="e2392-116">Frekari upplýsingar eru í [Notkun [!INCLUDE[prodshort](includes/prodshort.md)] í sjálfvirku verkflæði](across-how-use-financials-data-source-flow.md).</span><span class="sxs-lookup"><span data-stu-id="e2392-116">For more information, see [Using [!INCLUDE[prodshort](includes/prodshort.md)] in an Automated Workflow](across-how-use-financials-data-source-flow.md).</span></span>

<span data-ttu-id="e2392-117">Öll verkflæðissniðmát sem eru stofnuð með Power Automate er bætt við listann yfir verkflæðissniðmát innan [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="e2392-117">Any workflow template that you create with Power Automate is added to the list of workflow templates within [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="e2392-118">Frekari upplýsingar eru í [Notkun Business Central í sjálfvirku verkflæði](across-how-use-financials-data-source-flow.md).</span><span class="sxs-lookup"><span data-stu-id="e2392-118">For more information, see [Using Business Central in an Automated Workflow](across-how-use-financials-data-source-flow.md).</span></span>  

 <span data-ttu-id="e2392-119">Eftirfarandi tafla lýsir röð verkefna með tenglum í efnisatriði þar sem þeim er lýst.</span><span class="sxs-lookup"><span data-stu-id="e2392-119">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>  

|<span data-ttu-id="e2392-120">**Til að**</span><span class="sxs-lookup"><span data-stu-id="e2392-120">**To**</span></span>|<span data-ttu-id="e2392-121">**Sjá**</span><span class="sxs-lookup"><span data-stu-id="e2392-121">**See**</span></span>|  
|------------|-------------|  
|<span data-ttu-id="e2392-122">Setja upp notendum verkflæðis, skilgreina hvernig notendur fá tilkynningu, og búa til ný verkflæði.</span><span class="sxs-lookup"><span data-stu-id="e2392-122">Set up workflow users, specify how users get notified, and create new workflows.</span></span> <span data-ttu-id="e2392-123">Til að skapa ný verkflæði fyrir óstuddar sviðsmyndir skal framkvæma umbeðnar verkflæðiseiningar með því að sérsníða kóða forrits.</span><span class="sxs-lookup"><span data-stu-id="e2392-123">For new workflows for unsupported scenarios, implement the required workflow elements by customizing the application code.</span></span>|[<span data-ttu-id="e2392-124">Uppsetning verkflæðis</span><span class="sxs-lookup"><span data-stu-id="e2392-124">Setting Up Workflows</span></span>](across-set-up-workflows.md)|  
|<span data-ttu-id="e2392-125">Virkja verkflæði, bregðast við tilkynningar verkflæðis, þ.m.t samþykktarbeiðnum og samþykkja beiðnir til að framkvæma skref í verkflæði.</span><span class="sxs-lookup"><span data-stu-id="e2392-125">Enable workflows, act on workflow notifications, including request approvals and approve requests to perform a workflow step.</span></span> <span data-ttu-id="e2392-126">Setja verkflæði í skjalasafn eða eyða.</span><span class="sxs-lookup"><span data-stu-id="e2392-126">Archive and delete workflows.</span></span>|[<span data-ttu-id="e2392-127">Nota verkflæði</span><span class="sxs-lookup"><span data-stu-id="e2392-127">Using Workflows</span></span>](across-use-workflows.md)|  

## <a name="see-also"></a><span data-ttu-id="e2392-128">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="e2392-128">See Also</span></span>

[<span data-ttu-id="e2392-129">Sala</span><span class="sxs-lookup"><span data-stu-id="e2392-129">Sales</span></span>](sales-manage-sales.md)  
[<span data-ttu-id="e2392-130">Innkaup</span><span class="sxs-lookup"><span data-stu-id="e2392-130">Purchasing</span></span>](purchasing-manage-purchasing.md)  
[<span data-ttu-id="e2392-131">Stjórna verkum</span><span class="sxs-lookup"><span data-stu-id="e2392-131">Managing Projects</span></span>](projects-manage-projects.md)  
<span data-ttu-id="e2392-132">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="e2392-132">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
