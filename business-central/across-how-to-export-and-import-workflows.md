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
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: a0a67c3b6a706820c8b5fb073c090a6586435ca7
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/08/2019
ms.locfileid: "800619"
---
# <a name="export-and-import-workflows"></a><span data-ttu-id="94263-103">Flytja verkflæði inn og út</span><span class="sxs-lookup"><span data-stu-id="94263-103">Export and Import Workflows</span></span>
<span data-ttu-id="94263-104">Til að flytja verkflæði í annan [!INCLUDE[d365fin](includes/d365fin_md.md)] gagnagrunnur, t.d. til að spara tíma þegar stofnað ný verkflæði, er hægt að flytja út og inn verkflæði.</span><span class="sxs-lookup"><span data-stu-id="94263-104">To transfer workflows to other [!INCLUDE[d365fin](includes/d365fin_md.md)] databases, for example to save time when creating new workflows, you can export and import workflows.</span></span>  

 <span data-ttu-id="94263-105">Önnur leið til að búa til verkflæði er að búa til verkflæði úr verkflæðissniðmátum.</span><span class="sxs-lookup"><span data-stu-id="94263-105">Another way to quickly create workflows is to create workflows from workflow templates.</span></span> <span data-ttu-id="94263-106">Nánari upplýsingar eru í [Stofna verkflæði út frá verkflæðissniðmátum](across-how-to-create-workflows-from-workflow-templates.md).</span><span class="sxs-lookup"><span data-stu-id="94263-106">For more information, see [Create Workflows from Workflow Templates](across-how-to-create-workflows-from-workflow-templates.md).</span></span>  

 <span data-ttu-id="94263-107">Á síðunni **Verkflæði** er hægt að stofna verkflæði með því að skrá viðkomandi skref í línurnar.</span><span class="sxs-lookup"><span data-stu-id="94263-107">On the **Workflow** page, you create a workflow by listing the involved steps on the lines.</span></span> <span data-ttu-id="94263-108">Hvert skref samanstendur af atburði verkflæðis, breytt eftir atburður skilyrði, og verkflæðissvar, breytt eftir svarvalkostir.</span><span class="sxs-lookup"><span data-stu-id="94263-108">Each step consists of a workflow event, moderated by event conditions, and a workflow response, moderated by response options.</span></span> <span data-ttu-id="94263-109">Þú skilgreinir skref í verkflæði með því að fylla út í reiti á verkflæðislínum úr föstum listum yfir tilvik og svör gildi sem standa fyrir verkflæðissviðsmyndir sem eru studd af kóða forritsins.</span><span class="sxs-lookup"><span data-stu-id="94263-109">You define workflow steps by filling fields on workflow lines from fixed lists of event and response values representing scenarios that are supported by the application code.</span></span> <span data-ttu-id="94263-110">Frekari upplýsingar eru í [Búa til verkflæði](across-how-to-create-workflows.md).</span><span class="sxs-lookup"><span data-stu-id="94263-110">For more information, see [Create Workflows](across-how-to-create-workflows.md).</span></span>  

## <a name="to-export-a-workflow"></a><span data-ttu-id="94263-111">Til að flytja út verkflæði</span><span class="sxs-lookup"><span data-stu-id="94263-111">To export a workflow</span></span>  
1.  <span data-ttu-id="94263-112">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **verkflæði** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="94263-112">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Workflows**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="94263-113">Veljið Verkflæði og smellið á hnappinn **Flytja út í skrá**.</span><span class="sxs-lookup"><span data-stu-id="94263-113">Select a workflow, and then choose the **Export to File** action.</span></span>  
3.  <span data-ttu-id="94263-114">Á síðunni **Flytja út skrá** skal velja hnappinn **Vista**.</span><span class="sxs-lookup"><span data-stu-id="94263-114">On the **Export File** page, choose the **Save** button.</span></span>  
4.  <span data-ttu-id="94263-115">Á síðunni **Flytja út** skal velja staðsetningu skrána og svo hnappinn **Vista**.</span><span class="sxs-lookup"><span data-stu-id="94263-115">On the **Export** page, select a file location, and then choose the **Save** button.</span></span>  

## <a name="to-import-a-workflow"></a><span data-ttu-id="94263-116">Til að flytja inn verkflæði</span><span class="sxs-lookup"><span data-stu-id="94263-116">To import a workflow</span></span>  
1.  <span data-ttu-id="94263-117">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **verkflæði** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="94263-117">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Workflows**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="94263-118">Aðgerðin **Flytja inn úr skrá** er valin.</span><span class="sxs-lookup"><span data-stu-id="94263-118">Choose the **Import from File** action.</span></span>  
3.  <span data-ttu-id="94263-119">Á síðunni **Flytja inn** skal velja XML-skrá sem inniheldur verkflæðið og velja svo hnappinn **opna**.</span><span class="sxs-lookup"><span data-stu-id="94263-119">On the **Import** page, choose the XML file that contains the workflow, and then choose the **Open** button.</span></span>  

> [!CAUTION]  
>  <span data-ttu-id="94263-120">Ef verkflæðiskóðinn er þegar til í gagnagrunnur verður skrifað yfir verkflæðisskref með skrefum í innfluttu verkflæði.</span><span class="sxs-lookup"><span data-stu-id="94263-120">If the workflow code already exists in the database, the workflow steps will be overwritten with the steps in the imported workflow.</span></span>  

## <a name="see-also"></a><span data-ttu-id="94263-121">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="94263-121">See Also</span></span>  
 <span data-ttu-id="94263-122">[Búa til verkflæði](across-how-to-create-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="94263-122">[Create Workflows](across-how-to-create-workflows.md) </span></span>  
 <span data-ttu-id="94263-123">[Búa til verkflæði úr verkflæðissniðmátum](across-how-to-create-workflows-from-workflow-templates.md) </span><span class="sxs-lookup"><span data-stu-id="94263-123">[Create Workflows from Workflow Templates](across-how-to-create-workflows-from-workflow-templates.md) </span></span>  
 <span data-ttu-id="94263-124">[Skoða verkflæðisskrefstilvik í skráasafni](across-how-to-view-archived-workflow-step-instances.md) </span><span class="sxs-lookup"><span data-stu-id="94263-124">[View Archived Workflow Step Instances](across-how-to-view-archived-workflow-step-instances.md) </span></span>  
 <span data-ttu-id="94263-125">[Eyða verkflæðum](across-how-to-delete-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="94263-125">[Delete Workflows](across-how-to-delete-workflows.md) </span></span>  
 <span data-ttu-id="94263-126">[Kynning: Uppsetning og notkun verkflæði innkaupasamþykktar](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md) </span><span class="sxs-lookup"><span data-stu-id="94263-126">[Walkthrough: Setting Up and Using a Purchase Approval Workflow](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md) </span></span>  
 <span data-ttu-id="94263-127">[Uppsetning verkflæðis](across-set-up-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="94263-127">[Setting Up Workflows](across-set-up-workflows.md) </span></span>  
 <span data-ttu-id="94263-128">[Nota verkflæði](across-use-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="94263-128">[Using Workflows](across-use-workflows.md) </span></span>  
 [<span data-ttu-id="94263-129">Verkflæði</span><span class="sxs-lookup"><span data-stu-id="94263-129">Workflow</span></span>](across-workflow.md)   
