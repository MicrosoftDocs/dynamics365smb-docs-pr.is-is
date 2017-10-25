---
title: "Hvernig á að búa til verkflæði úr verkflæðissniðmátum | Microsoft Docs"
description: "Hægt er að búa til verkflæði með verkflæðissniðmátum til að spara tíma þegar ný verkflæði eru stofnuð."
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
ms.openlocfilehash: dcf6f5f5b0364ebcaefdcbc43fdbd7471cb6079e
ms.contentlocale: is-is
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-create-workflows-from-workflow-templates"></a><span data-ttu-id="ad9bf-103">Hvernig á að: Búa til verkflæði úr verkflæðissniðmátum</span><span class="sxs-lookup"><span data-stu-id="ad9bf-103">How to: Create Workflows from Workflow Templates</span></span>
<span data-ttu-id="ad9bf-104">Hægt er að búa til verkflæði með verkflæðissniðmátum til að spara tíma þegar ný verkflæði eru stofnuð.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-104">To save time when creating new workflows, you can create workflows from workflow templates.</span></span>  

 <span data-ttu-id="ad9bf-105">Verkflæðissniðmát eru óbreytanleg verkflæði sem eru til staðar í almennu útgáfunni af [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="ad9bf-105">Workflow templates are non-editable workflows that exist in the generic version of [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="ad9bf-106">Kóðar fyrir verkflæðissniðmát sem bætt er við af Microsoft hafa forskeytið „MS-“.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-106">The codes for workflow templates that are added by Microsoft are prefixed with “MS-“.</span></span>  

 <span data-ttu-id="ad9bf-107">Önnur fljótleg leið til að búa til verkflæði er að flytja inn fyrirliggjandi verkflæði sem til er ótengt[!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="ad9bf-107">Another way to quickly create a workflow is to import an existing workflow that you have on a file outside of [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="ad9bf-108">Nánari upplýsingar er að finna í [Hvernig að á flytja verkflæði inn og út](across-how-to-export-and-import-workflows.md)</span><span class="sxs-lookup"><span data-stu-id="ad9bf-108">For more information, see [How to: Export and Import Workflows](across-how-to-export-and-import-workflows.md).</span></span>  

<span data-ttu-id="ad9bf-109">Í glugganum **Verkflæði** er hægt að stofna verkflæði með því að skrá viðkomandi skref í línurnar.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-109">In the **Workflow** window, you create a workflow by listing the involved steps on the lines.</span></span> <span data-ttu-id="ad9bf-110">Hvert skref samanstendur af atburði verkflæðis, breytt eftir atburður skilyrði, og verkflæðissvar, breytt eftir svarvalkostir.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-110">Each step consists of a workflow event, moderated by event conditions, and a workflow response, moderated by response options.</span></span> <span data-ttu-id="ad9bf-111">Þú skilgreinir skref í verkflæði með því að fylla út í reiti á verkflæðislínum úr föstum listum yfir tilvik og svör gildi sem standa fyrir verkflæðissviðsmyndir sem eru studd af kóða forritsins.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-111">You define workflow steps by filling fields on workflow lines from fixed lists of event and response values representing scenarios that are supported by the application code.</span></span> <span data-ttu-id="ad9bf-112">Nánari upplýsingar eru í [Hvernig á að: Stofna verkflæði](across-how-to-create-workflows.md).</span><span class="sxs-lookup"><span data-stu-id="ad9bf-112">For more information, see [How to: Create Workflows](across-how-to-create-workflows.md).</span></span>  

## <a name="to-create-a-workflow-from-workflow-template"></a><span data-ttu-id="ad9bf-113">Hvernig á að búa til verkflæði úr verkflæðissniðmátum</span><span class="sxs-lookup"><span data-stu-id="ad9bf-113">To create a workflow from workflow template</span></span>  
1.  <span data-ttu-id="ad9bf-114">Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Verkflæði** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-114">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Workflows**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="ad9bf-115">Velja skal aðgerðina **Stofna verkflæði úr sniðmáti**.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-115">Choose the **Create Workflow from Template** action.</span></span> <span data-ttu-id="ad9bf-116">Glugginn **sniðmát verkflæðis** opnast.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-116">The **Workflow Templates** window opens.</span></span>  
3.  <span data-ttu-id="ad9bf-117">Veljið verkflæðissniðmát og smellið á hnappinn **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-117">Select a workflow template, and then choose the **OK** button.</span></span>  

     <span data-ttu-id="ad9bf-118">Glugginn **Verkflæði** opnast fyrir nýtt verkflæði sem inniheldur allar upplýsingarnar úr völdu sniðmáti.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-118">The **Workflow** window opens for a new workflow containing all the information of the selected template.</span></span> <span data-ttu-id="ad9bf-119">Við gildið í reitnum **Kóði** er bætt við t.d. „-01“ til að gefa til kynna að þetta sé fyrsta verkflæðið sem er stofnað úr verkflæðissniðmátinu.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-119">The value in the **Code** field is extended with, for example, “-01” to indicate that this is the first workflow that is created from the workflow template.</span></span>  
4.  <span data-ttu-id="ad9bf-120">Haldið áfram til að stofna verkflæði með því að breyta verkflæðisskrefum eða bæta við nýjum skrefum.</span><span class="sxs-lookup"><span data-stu-id="ad9bf-120">Proceed to create the workflow by editing the workflow steps or add new steps.</span></span> <span data-ttu-id="ad9bf-121">Nánari upplýsingar eru í [Hvernig á að: Stofna verkflæði](across-how-to-create-workflows.md).</span><span class="sxs-lookup"><span data-stu-id="ad9bf-121">For more information, see [How to: Create Workflows](across-how-to-create-workflows.md).</span></span>  

## <a name="see-also"></a><span data-ttu-id="ad9bf-122">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="ad9bf-122">See Also</span></span>  
 <span data-ttu-id="ad9bf-123">[Hvernig á að: Búa til verkflæði](across-how-to-create-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="ad9bf-123">[How to: Create Workflows](across-how-to-create-workflows.md) </span></span>  
 <span data-ttu-id="ad9bf-124">[Hvernig á að: Flytja verkflæði inn og út](across-how-to-export-and-import-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="ad9bf-124">[How to: Export and Import Workflows](across-how-to-export-and-import-workflows.md) </span></span>  
 <span data-ttu-id="ad9bf-125">[Hvernig á að: Skoða verkflæðisskrefstilvik í skráasafni](across-how-to-view-archived-workflow-step-instances.md) </span><span class="sxs-lookup"><span data-stu-id="ad9bf-125">[How to: View Archived Workflow Step Instances](across-how-to-view-archived-workflow-step-instances.md) </span></span>  
 <span data-ttu-id="ad9bf-126">[Hvernig á að: Eyða verkflæðum](across-how-to-delete-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="ad9bf-126">[How to: Delete Workflows](across-how-to-delete-workflows.md) </span></span>  
 <span data-ttu-id="ad9bf-127">[Kynning: Uppsetning og notkun innkaupasamþykktar](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md) </span><span class="sxs-lookup"><span data-stu-id="ad9bf-127">[Walkthrough: Setting Up and Using a Purchase Approval Workflow](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md) </span></span>  
 <span data-ttu-id="ad9bf-128">[Uppsetning verkflæðis](across-set-up-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="ad9bf-128">[Setting Up Workflows](across-set-up-workflows.md) </span></span>  
 <span data-ttu-id="ad9bf-129">[Nota verkflæði](across-use-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="ad9bf-129">[Using Workflows](across-use-workflows.md) </span></span>  
 [<span data-ttu-id="ad9bf-130">Verkflæði</span><span class="sxs-lookup"><span data-stu-id="ad9bf-130">Workflow</span></span>](across-workflow.md)   

