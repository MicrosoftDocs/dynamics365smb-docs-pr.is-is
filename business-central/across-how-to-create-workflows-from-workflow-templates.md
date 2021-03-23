---
title: Hvernig á að búa til verkflæði úr verkflæðissniðmátum | Microsoft Docs
description: Hægt er að búa til verkflæði með verkflæðissniðmátum til að spara tíma þegar ný verkflæði eru stofnuð.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 6376c38e2580881a6d3fbb7ffd7661302a448c1a
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5384525"
---
# <a name="create-workflows-from-workflow-templates"></a><span data-ttu-id="66099-103">Búa til verkflæði úr verkflæðissniðmátum</span><span class="sxs-lookup"><span data-stu-id="66099-103">Create Workflows from Workflow Templates</span></span>
<span data-ttu-id="66099-104">Hægt er að búa til verkflæði með verkflæðissniðmátum til að spara tíma þegar ný verkflæði eru stofnuð.</span><span class="sxs-lookup"><span data-stu-id="66099-104">To save time when creating new workflows, you can create workflows from workflow templates.</span></span>  

 <span data-ttu-id="66099-105">Verkflæðissniðmát eru óbreytanleg verkflæði sem eru til staðar í almennu útgáfunni af [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="66099-105">Workflow templates are non-editable workflows that exist in the generic version of [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="66099-106">Kóðar fyrir verkflæðissniðmát sem bætt er við af Microsoft hafa forskeytið „MS-“.</span><span class="sxs-lookup"><span data-stu-id="66099-106">The codes for workflow templates that are added by Microsoft are prefixed with “MS-“.</span></span>  

 <span data-ttu-id="66099-107">Önnur fljótleg leið til að búa til verkflæði er að flytja inn fyrirliggjandi verkflæði sem til er ótengt[!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="66099-107">Another way to quickly create a workflow is to import an existing workflow that you have on a file outside of [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="66099-108">Frekari upplýsingar eru í [Flytja verkflæði inn og út](across-how-to-export-and-import-workflows.md).</span><span class="sxs-lookup"><span data-stu-id="66099-108">For more information, see [Export and Import Workflows](across-how-to-export-and-import-workflows.md).</span></span>  

<span data-ttu-id="66099-109">Á síðunni **Verkflæði** er hægt að stofna verkflæði með því að skrá viðkomandi skref í línurnar.</span><span class="sxs-lookup"><span data-stu-id="66099-109">On the **Workflow** page, you create a workflow by listing the involved steps on the lines.</span></span> <span data-ttu-id="66099-110">Hvert skref samanstendur af atburði verkflæðis, breytt eftir atburður skilyrði, og verkflæðissvar, breytt eftir svarvalkostir.</span><span class="sxs-lookup"><span data-stu-id="66099-110">Each step consists of a workflow event, moderated by event conditions, and a workflow response, moderated by response options.</span></span> <span data-ttu-id="66099-111">Þú skilgreinir skref í verkflæði með því að fylla út í reiti á verkflæðislínum úr föstum listum yfir tilvik og svör gildi sem standa fyrir verkflæðissviðsmyndir sem eru studd af kóða forritsins.</span><span class="sxs-lookup"><span data-stu-id="66099-111">You define workflow steps by filling fields on workflow lines from fixed lists of event and response values representing scenarios that are supported by the application code.</span></span> <span data-ttu-id="66099-112">Frekari upplýsingar eru í [Búa til verkflæði](across-how-to-create-workflows.md).</span><span class="sxs-lookup"><span data-stu-id="66099-112">For more information, see [Create Workflows](across-how-to-create-workflows.md).</span></span>  

## <a name="to-create-a-workflow-from-workflow-template"></a><span data-ttu-id="66099-113">Hvernig á að búa til verkflæði úr verkflæðissniðmátum</span><span class="sxs-lookup"><span data-stu-id="66099-113">To create a workflow from workflow template</span></span>  
1.  <span data-ttu-id="66099-114">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Verkflæði** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="66099-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Workflows**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="66099-115">Velja skal aðgerðina **Stofna verkflæði úr sniðmáti**.</span><span class="sxs-lookup"><span data-stu-id="66099-115">Choose the **Create Workflow from Template** action.</span></span> <span data-ttu-id="66099-116">Síðan **Sniðmát verkflæðis** opnast.</span><span class="sxs-lookup"><span data-stu-id="66099-116">The **Workflow Templates** page opens.</span></span>  
3.  <span data-ttu-id="66099-117">Veljið verkflæðissniðmát og smellið á hnappinn **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="66099-117">Select a workflow template, and then choose the **OK** button.</span></span>  

     <span data-ttu-id="66099-118">Síðan **Verkflæði** opnast fyrir nýtt verkflæði sem inniheldur allar upplýsingarnar úr völdu sniðmáti.</span><span class="sxs-lookup"><span data-stu-id="66099-118">The **Workflow** page opens for a new workflow containing all the information of the selected template.</span></span> <span data-ttu-id="66099-119">Við gildið í reitnum **Kóði** er bætt við t.d. „-01“ til að gefa til kynna að þetta sé fyrsta verkflæðið sem er stofnað úr verkflæðissniðmátinu.</span><span class="sxs-lookup"><span data-stu-id="66099-119">The value in the **Code** field is extended with, for example, “-01” to indicate that this is the first workflow that is created from the workflow template.</span></span>  
4.  <span data-ttu-id="66099-120">Haldið áfram til að stofna verkflæði með því að breyta verkflæðisskrefum eða bæta við nýjum skrefum.</span><span class="sxs-lookup"><span data-stu-id="66099-120">Proceed to create the workflow by editing the workflow steps or add new steps.</span></span> <span data-ttu-id="66099-121">Frekari upplýsingar eru í [Búa til verkflæði](across-how-to-create-workflows.md).</span><span class="sxs-lookup"><span data-stu-id="66099-121">For more information, see [Create Workflows](across-how-to-create-workflows.md).</span></span>  

## <a name="see-also"></a><span data-ttu-id="66099-122">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="66099-122">See Also</span></span>  
 <span data-ttu-id="66099-123">[Búa til verkflæði](across-how-to-create-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="66099-123">[Create Workflows](across-how-to-create-workflows.md) </span></span>  
 <span data-ttu-id="66099-124">[Flytja verkflæði inn og út](across-how-to-export-and-import-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="66099-124">[Export and Import Workflows](across-how-to-export-and-import-workflows.md) </span></span>  
 <span data-ttu-id="66099-125">[Skoða verkflæðisskrefstilvik í skráasafni](across-how-to-view-archived-workflow-step-instances.md) </span><span class="sxs-lookup"><span data-stu-id="66099-125">[View Archived Workflow Step Instances](across-how-to-view-archived-workflow-step-instances.md) </span></span>  
 <span data-ttu-id="66099-126">[Eyða verkflæðum](across-how-to-delete-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="66099-126">[Delete Workflows](across-how-to-delete-workflows.md) </span></span>  
 <span data-ttu-id="66099-127">[Kynning: Uppsetning og notkun verkflæði innkaupasamþykktar](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md) </span><span class="sxs-lookup"><span data-stu-id="66099-127">[Walkthrough: Setting Up and Using a Purchase Approval Workflow](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md) </span></span>  
 <span data-ttu-id="66099-128">[Uppsetning verkflæðis](across-set-up-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="66099-128">[Setting Up Workflows](across-set-up-workflows.md) </span></span>  
 <span data-ttu-id="66099-129">[Nota verkflæði](across-use-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="66099-129">[Using Workflows](across-use-workflows.md) </span></span>  
 [<span data-ttu-id="66099-130">Verkflæði</span><span class="sxs-lookup"><span data-stu-id="66099-130">Workflow</span></span>](across-workflow.md)   


[!INCLUDE[footer-include](includes/footer-banner.md)]