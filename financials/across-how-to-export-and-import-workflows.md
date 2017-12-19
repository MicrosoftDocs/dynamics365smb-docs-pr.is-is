---
title: "Hvernig á að flytja verkflæði inn og út | Microsoft Docs"
description: "Til að flytja verkflæði í annan Dynamics 365-gagnagrunnur, t.d. til að spara tíma þegar stofnað ný verkflæði, er hægt að flytja út og inn verkflæði."
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
ms.sourcegitcommit: aa56764b5f3210229ad21eae6891fb201462209c
ms.openlocfilehash: 520c81b9c550b4ef29b077685541a2e7ea30d4d7
ms.contentlocale: is-is
ms.lasthandoff: 12/14/2017

---
# <a name="how-to-export-and-import-workflows"></a><span data-ttu-id="47928-103">Hvernig á að: Flytja verkflæði inn og út</span><span class="sxs-lookup"><span data-stu-id="47928-103">How to: Export and Import Workflows</span></span>
<span data-ttu-id="47928-104">Til að flytja verkflæði í annan [!INCLUDE[d365fin](includes/d365fin_md.md)] gagnagrunnur, t.d. til að spara tíma þegar stofnað ný verkflæði, er hægt að flytja út og inn verkflæði.</span><span class="sxs-lookup"><span data-stu-id="47928-104">To transfer workflows to other [!INCLUDE[d365fin](includes/d365fin_md.md)] databases, for example to save time when creating new workflows, you can export and import workflows.</span></span>  

 <span data-ttu-id="47928-105">Önnur leið til að búa til verkflæði er að búa til verkflæði úr verkflæðissniðmátum.</span><span class="sxs-lookup"><span data-stu-id="47928-105">Another way to quickly create workflows is to create workflows from workflow templates.</span></span> <span data-ttu-id="47928-106">Nánari upplýsingar eru í [Hvernig á að: Stofna verkflæði út frá verkflæðissniðmátum](across-how-to-create-workflows-from-workflow-templates.md).</span><span class="sxs-lookup"><span data-stu-id="47928-106">For more information, see [How to: Create Workflows from Workflow Templates](across-how-to-create-workflows-from-workflow-templates.md).</span></span>  

 <span data-ttu-id="47928-107">Í glugganum **Verkflæði** er hægt að stofna verkflæði með því að skrá viðkomandi skref í línurnar.</span><span class="sxs-lookup"><span data-stu-id="47928-107">In the **Workflow** window, you create a workflow by listing the involved steps on the lines.</span></span> <span data-ttu-id="47928-108">Hvert skref samanstendur af atburði verkflæðis, breytt eftir atburður skilyrði, og verkflæðissvar, breytt eftir svarvalkostir.</span><span class="sxs-lookup"><span data-stu-id="47928-108">Each step consists of a workflow event, moderated by event conditions, and a workflow response, moderated by response options.</span></span> <span data-ttu-id="47928-109">Þú skilgreinir skref í verkflæði með því að fylla út í reiti á verkflæðislínum úr föstum listum yfir tilvik og svör gildi sem standa fyrir verkflæðissviðsmyndir sem eru studd af kóða forritsins.</span><span class="sxs-lookup"><span data-stu-id="47928-109">You define workflow steps by filling fields on workflow lines from fixed lists of event and response values representing scenarios that are supported by the application code.</span></span> <span data-ttu-id="47928-110">Nánari upplýsingar eru í [Hvernig á að: Stofna verkflæði](across-how-to-create-workflows.md).</span><span class="sxs-lookup"><span data-stu-id="47928-110">For more information, see [How to: Create Workflows](across-how-to-create-workflows.md).</span></span>  

## <a name="to-export-a-workflow"></a><span data-ttu-id="47928-111">Til að flytja út verkflæði</span><span class="sxs-lookup"><span data-stu-id="47928-111">To export a workflow</span></span>  
1.  <span data-ttu-id="47928-112">Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Verkflæði** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="47928-112">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Workflows**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="47928-113">Veljið Verkflæði og smellið á hnappinn **Flytja út í skrá**.</span><span class="sxs-lookup"><span data-stu-id="47928-113">Select a workflow, and then choose the **Export to File** action.</span></span>  
3.  <span data-ttu-id="47928-114">Í gluggi **Flytja út skrá** veljið hnappinn **Vista**.</span><span class="sxs-lookup"><span data-stu-id="47928-114">In the **Export File** window, choose the **Save** button.</span></span>  
4.  <span data-ttu-id="47928-115">Í glugganum **Flytja út** skal velja staðsetningu skrána og svo hnappinn **Vista**.</span><span class="sxs-lookup"><span data-stu-id="47928-115">In the **Export** window, select a file location, and then choose the **Save** button.</span></span>  

## <a name="to-import-a-workflow"></a><span data-ttu-id="47928-116">Til að flytja inn verkflæði</span><span class="sxs-lookup"><span data-stu-id="47928-116">To import a workflow</span></span>  
1.  <span data-ttu-id="47928-117">Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Verkflæði** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="47928-117">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Workflows**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="47928-118">Aðgerðin **Flytja inn úr skrá** er valin.</span><span class="sxs-lookup"><span data-stu-id="47928-118">Choose the **Import from File** action.</span></span>  
3.  <span data-ttu-id="47928-119">Í glugganum **flytja inn** skal velja XML-skrá sem inniheldur verkflæðið og velja svo hnappinn **opna**.</span><span class="sxs-lookup"><span data-stu-id="47928-119">In the **Import** window, choose the XML file that contains the workflow, and then choose the **Open** button.</span></span>  

> [!CAUTION]  
>  <span data-ttu-id="47928-120">Ef verkflæðiskóðinn er þegar til í gagnagrunnur verður skrifað yfir verkflæðisskref með skrefum í innfluttu verkflæði.</span><span class="sxs-lookup"><span data-stu-id="47928-120">If the workflow code already exists in the database, the workflow steps will be overwritten with the steps in the imported workflow.</span></span>  

## <a name="see-also"></a><span data-ttu-id="47928-121">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="47928-121">See Also</span></span>  
 <span data-ttu-id="47928-122">[Hvernig á að: Búa til verkflæði](across-how-to-create-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="47928-122">[How to: Create Workflows](across-how-to-create-workflows.md) </span></span>  
 <span data-ttu-id="47928-123">[Hvernig á að: Búa til verkflæði úr verkflæðissniðmátum](across-how-to-create-workflows-from-workflow-templates.md) </span><span class="sxs-lookup"><span data-stu-id="47928-123">[How to: Create Workflows from Workflow Templates](across-how-to-create-workflows-from-workflow-templates.md) </span></span>  
 <span data-ttu-id="47928-124">[Hvernig á að: Skoða verkflæðisskrefstilvik í skráasafni](across-how-to-view-archived-workflow-step-instances.md) </span><span class="sxs-lookup"><span data-stu-id="47928-124">[How to: View Archived Workflow Step Instances](across-how-to-view-archived-workflow-step-instances.md) </span></span>  
 <span data-ttu-id="47928-125">[Hvernig á að: Eyða verkflæðum](across-how-to-delete-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="47928-125">[How to: Delete Workflows](across-how-to-delete-workflows.md) </span></span>  
 <span data-ttu-id="47928-126">[Kynning: Uppsetning og notkun verkflæði innkaupasamþykktar](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md) </span><span class="sxs-lookup"><span data-stu-id="47928-126">[Walkthrough: Setting Up and Using a Purchase Approval Workflow](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md) </span></span>  
 <span data-ttu-id="47928-127">[Uppsetning verkflæðis](across-set-up-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="47928-127">[Setting Up Workflows](across-set-up-workflows.md) </span></span>  
 <span data-ttu-id="47928-128">[Nota verkflæði](across-use-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="47928-128">[Using Workflows](across-use-workflows.md) </span></span>  
 [<span data-ttu-id="47928-129">Verkflæði</span><span class="sxs-lookup"><span data-stu-id="47928-129">Workflow</span></span>](across-workflow.md)   

