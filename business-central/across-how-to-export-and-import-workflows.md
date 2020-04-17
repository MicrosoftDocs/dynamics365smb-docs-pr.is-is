---
title: Hvernig á að flytja verkflæði inn og út | Microsoft Docs
description: Til að flytja verkflæði í annan Business Central gagnagrunn, t.d. til að spara tíma þegar stofnað ný verkflæði, er hægt að flytja út og inn verkflæði.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 2d309940d177491ce24f49884f388a5c233147fa
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2020
ms.locfileid: "3188277"
---
# <a name="export-and-import-workflows"></a><span data-ttu-id="d164f-103">Flytja verkflæði inn og út</span><span class="sxs-lookup"><span data-stu-id="d164f-103">Export and Import Workflows</span></span>
<span data-ttu-id="d164f-104">Til að flytja verkflæði í annan [!INCLUDE[d365fin](includes/d365fin_md.md)] gagnagrunnur, t.d. til að spara tíma þegar stofnað ný verkflæði, er hægt að flytja út og inn verkflæði.</span><span class="sxs-lookup"><span data-stu-id="d164f-104">To transfer workflows to other [!INCLUDE[d365fin](includes/d365fin_md.md)] databases, for example to save time when creating new workflows, you can export and import workflows.</span></span>  

 <span data-ttu-id="d164f-105">Önnur leið til að búa til verkflæði er að búa til verkflæði úr verkflæðissniðmátum.</span><span class="sxs-lookup"><span data-stu-id="d164f-105">Another way to quickly create workflows is to create workflows from workflow templates.</span></span> <span data-ttu-id="d164f-106">Nánari upplýsingar eru í [Stofna verkflæði út frá verkflæðissniðmátum](across-how-to-create-workflows-from-workflow-templates.md).</span><span class="sxs-lookup"><span data-stu-id="d164f-106">For more information, see [Create Workflows from Workflow Templates](across-how-to-create-workflows-from-workflow-templates.md).</span></span>  

 <span data-ttu-id="d164f-107">Á síðunni **Verkflæði** er hægt að stofna verkflæði með því að skrá viðkomandi skref í línurnar.</span><span class="sxs-lookup"><span data-stu-id="d164f-107">On the **Workflow** page, you create a workflow by listing the involved steps on the lines.</span></span> <span data-ttu-id="d164f-108">Hvert skref samanstendur af atburði verkflæðis, breytt eftir atburður skilyrði, og verkflæðissvar, breytt eftir svarvalkostir.</span><span class="sxs-lookup"><span data-stu-id="d164f-108">Each step consists of a workflow event, moderated by event conditions, and a workflow response, moderated by response options.</span></span> <span data-ttu-id="d164f-109">Þú skilgreinir skref í verkflæði með því að fylla út í reiti á verkflæðislínum úr föstum listum yfir tilvik og svör gildi sem standa fyrir verkflæðissviðsmyndir sem eru studd af kóða forritsins.</span><span class="sxs-lookup"><span data-stu-id="d164f-109">You define workflow steps by filling fields on workflow lines from fixed lists of event and response values representing scenarios that are supported by the application code.</span></span> <span data-ttu-id="d164f-110">Frekari upplýsingar eru í [Búa til verkflæði](across-how-to-create-workflows.md).</span><span class="sxs-lookup"><span data-stu-id="d164f-110">For more information, see [Create Workflows](across-how-to-create-workflows.md).</span></span>  

## <a name="to-export-a-workflow"></a><span data-ttu-id="d164f-111">Til að flytja út verkflæði</span><span class="sxs-lookup"><span data-stu-id="d164f-111">To export a workflow</span></span>  
1.  <span data-ttu-id="d164f-112">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Verkflæði** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="d164f-112">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Workflows**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="d164f-113">Veljið Verkflæði og smellið á hnappinn **Flytja út í skrá**.</span><span class="sxs-lookup"><span data-stu-id="d164f-113">Select a workflow, and then choose the **Export to File** action.</span></span>  
3.  <span data-ttu-id="d164f-114">Á síðunni **Flytja út skrá** skal velja hnappinn **Vista**.</span><span class="sxs-lookup"><span data-stu-id="d164f-114">On the **Export File** page, choose the **Save** button.</span></span>  
4.  <span data-ttu-id="d164f-115">Á síðunni **Flytja út** skal velja staðsetningu skrána og svo hnappinn **Vista**.</span><span class="sxs-lookup"><span data-stu-id="d164f-115">On the **Export** page, select a file location, and then choose the **Save** button.</span></span>  

## <a name="to-import-a-workflow"></a><span data-ttu-id="d164f-116">Til að flytja inn verkflæði</span><span class="sxs-lookup"><span data-stu-id="d164f-116">To import a workflow</span></span>  
1.  <span data-ttu-id="d164f-117">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Verkflæði** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="d164f-117">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Workflows**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="d164f-118">Aðgerðin **Flytja inn úr skrá** er valin.</span><span class="sxs-lookup"><span data-stu-id="d164f-118">Choose the **Import from File** action.</span></span>  
3.  <span data-ttu-id="d164f-119">Á síðunni **Flytja inn** skal velja XML-skrá sem inniheldur verkflæðið og velja svo hnappinn **opna**.</span><span class="sxs-lookup"><span data-stu-id="d164f-119">On the **Import** page, choose the XML file that contains the workflow, and then choose the **Open** button.</span></span>  

> [!CAUTION]  
>  <span data-ttu-id="d164f-120">Ef verkflæðiskóðinn er þegar til í gagnagrunnur verður skrifað yfir verkflæðisskref með skrefum í innfluttu verkflæði.</span><span class="sxs-lookup"><span data-stu-id="d164f-120">If the workflow code already exists in the database, the workflow steps will be overwritten with the steps in the imported workflow.</span></span>  

## <a name="see-also"></a><span data-ttu-id="d164f-121">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="d164f-121">See Also</span></span>  
 <span data-ttu-id="d164f-122">[Búa til verkflæði](across-how-to-create-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="d164f-122">[Create Workflows](across-how-to-create-workflows.md) </span></span>  
 <span data-ttu-id="d164f-123">[Búa til verkflæði úr verkflæðissniðmátum](across-how-to-create-workflows-from-workflow-templates.md) </span><span class="sxs-lookup"><span data-stu-id="d164f-123">[Create Workflows from Workflow Templates](across-how-to-create-workflows-from-workflow-templates.md) </span></span>  
 <span data-ttu-id="d164f-124">[Skoða verkflæðisskrefstilvik í skráasafni](across-how-to-view-archived-workflow-step-instances.md) </span><span class="sxs-lookup"><span data-stu-id="d164f-124">[View Archived Workflow Step Instances](across-how-to-view-archived-workflow-step-instances.md) </span></span>  
 <span data-ttu-id="d164f-125">[Eyða verkflæðum](across-how-to-delete-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="d164f-125">[Delete Workflows](across-how-to-delete-workflows.md) </span></span>  
 <span data-ttu-id="d164f-126">[Kynning: Uppsetning og notkun verkflæði innkaupasamþykktar](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md) </span><span class="sxs-lookup"><span data-stu-id="d164f-126">[Walkthrough: Setting Up and Using a Purchase Approval Workflow](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md) </span></span>  
 <span data-ttu-id="d164f-127">[Uppsetning verkflæðis](across-set-up-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="d164f-127">[Setting Up Workflows](across-set-up-workflows.md) </span></span>  
 <span data-ttu-id="d164f-128">[Nota verkflæði](across-use-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="d164f-128">[Using Workflows](across-use-workflows.md) </span></span>  
 [<span data-ttu-id="d164f-129">Verkflæði</span><span class="sxs-lookup"><span data-stu-id="d164f-129">Workflow</span></span>](across-workflow.md)   
