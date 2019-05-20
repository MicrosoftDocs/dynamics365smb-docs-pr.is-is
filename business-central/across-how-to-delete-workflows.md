---
title: Hvernig skal eyða verkflæði | Microsoft Docs
description: Óhætt er að eyða verkflæði ef ljóst er að það sé ekki lengur í notkun. Öll verkflæðistilvik sem eru skilgreind í verkflæði verða að hafa stöðuna **Lokið**.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 31a92e70e044a82313b5329ed2bf007b2b809c11
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/29/2019
ms.locfileid: "1244934"
---
# <a name="delete-workflows"></a><span data-ttu-id="2e833-104">Eyða verkflæðum</span><span class="sxs-lookup"><span data-stu-id="2e833-104">Delete Workflows</span></span>
<span data-ttu-id="2e833-105">Óhætt er að eyða verkflæði ef ljóst er að það sé ekki lengur í notkun.</span><span class="sxs-lookup"><span data-stu-id="2e833-105">If you are certain that a workflow is no longer being used, you can delete it.</span></span> <span data-ttu-id="2e833-106">Öll verkflæðistilvik sem eru skilgreind í verkflæði verða að hafa stöðuna **Lokið**.</span><span class="sxs-lookup"><span data-stu-id="2e833-106">All workflow step instances that are defined in the workflow must have status **Completed**.</span></span>  

> [!CAUTION]  
>  <span data-ttu-id="2e833-107">Þegar verkflæði er eytt munu allar upplýsingar verkflæðisins glatast.</span><span class="sxs-lookup"><span data-stu-id="2e833-107">When you delete a workflow, all information in the workflow will be lost.</span></span>  

 <span data-ttu-id="2e833-108">Á síðunni **Verkflæði** er hægt að stofna verkflæði með því að skrá viðkomandi skref í línurnar.</span><span class="sxs-lookup"><span data-stu-id="2e833-108">On the **Workflow** page, you create a workflow by listing the involved steps on the lines.</span></span> <span data-ttu-id="2e833-109">Hvert skref samanstendur af atburði verkflæðis, breytt eftir atburður skilyrði, og verkflæðissvar, breytt eftir svarvalkostir.</span><span class="sxs-lookup"><span data-stu-id="2e833-109">Each step consists of a workflow event, moderated by event conditions, and a workflow response, moderated by response options.</span></span> <span data-ttu-id="2e833-110">Þú skilgreinir skref í verkflæði með því að fylla út í reiti á verkflæðislínum úr föstum listum yfir tilvik og svör gildi sem standa fyrir verkflæðissviðsmyndir sem eru studd af kóða forritsins.</span><span class="sxs-lookup"><span data-stu-id="2e833-110">You define workflow steps by filling fields on workflow lines from fixed lists of event and response values representing scenarios that are supported by the application code.</span></span> <span data-ttu-id="2e833-111">Frekari upplýsingar eru í [Búa til verkflæði](across-how-to-create-workflows.md).</span><span class="sxs-lookup"><span data-stu-id="2e833-111">For more information, see [Create Workflows](across-how-to-create-workflows.md).</span></span>  

## <a name="to-delete-a-workflow"></a><span data-ttu-id="2e833-112">Að eyða verkflæði</span><span class="sxs-lookup"><span data-stu-id="2e833-112">To delete a workflow</span></span>  
1.  <span data-ttu-id="2e833-113">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **verkflæði** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="2e833-113">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Workflows**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="2e833-114">Veljið verkflæði sem á að eyða.</span><span class="sxs-lookup"><span data-stu-id="2e833-114">Select the workflow that you want to delete.</span></span>  
3.  <span data-ttu-id="2e833-115">Velja skal aðgerðina **Eyða**.</span><span class="sxs-lookup"><span data-stu-id="2e833-115">Choose the **Delete** action.</span></span>  
4.  <span data-ttu-id="2e833-116">Að öðrum kosti er hægt að opna það verkflæði sem á að eyða.</span><span class="sxs-lookup"><span data-stu-id="2e833-116">Alternatively, open the workflow that you want to delete.</span></span>  
5.  <span data-ttu-id="2e833-117">Á síðunni **Verkflæði** skal velja aðgerðina **Eyða**.</span><span class="sxs-lookup"><span data-stu-id="2e833-117">On the **Workflow** page, choose the **Delete** action.</span></span>  

## <a name="see-also"></a><span data-ttu-id="2e833-118">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="2e833-118">See Also</span></span>  
 <span data-ttu-id="2e833-119">[Búa til verkflæði](across-how-to-create-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="2e833-119">[Create Workflows](across-how-to-create-workflows.md) </span></span>  
 <span data-ttu-id="2e833-120">[Virkja verkflæði](across-how-to-enable-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="2e833-120">[Enable Workflows](across-how-to-enable-workflows.md) </span></span>  
 <span data-ttu-id="2e833-121">[Skoða verkflæðisskrefstilvik í skráasafni](across-how-to-view-archived-workflow-step-instances.md) </span><span class="sxs-lookup"><span data-stu-id="2e833-121">[View Archived Workflow Step Instances](across-how-to-view-archived-workflow-step-instances.md) </span></span>  
 <span data-ttu-id="2e833-122">[Kynning: Uppsetning og notkun verkflæði innkaupasamþykktar](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md) </span><span class="sxs-lookup"><span data-stu-id="2e833-122">[Walkthrough: Setting Up and Using a Purchase Approval Workflow](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md) </span></span>  
 <span data-ttu-id="2e833-123">[Uppsetning verkflæðis](across-set-up-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="2e833-123">[Setting Up Workflows](across-set-up-workflows.md) </span></span>  
 <span data-ttu-id="2e833-124">[Nota verkflæði](across-use-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="2e833-124">[Using Workflows](across-use-workflows.md) </span></span>  
 [<span data-ttu-id="2e833-125">Verkflæði</span><span class="sxs-lookup"><span data-stu-id="2e833-125">Workflow</span></span>](across-workflow.md)   
