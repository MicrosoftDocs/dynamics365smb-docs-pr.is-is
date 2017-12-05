---
title: "Hvernig á að takmarka og leyfa notkun á færslu | Microsoft Docs"
description: "Eigi að varna því að færsla sé notuð í tilteknum aðgerðum, til dæmis, ekki fyrr en færslan hefur verið samþykkt, er hægt að virkja tvö verkflæðissvör sem stýrir notkun færslu."
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
ms.sourcegitcommit: ba26b354d235981bd7291f9ac6402779f554ac7a
ms.openlocfilehash: 0dc8b3eeecfbf3f4a96985f4e4adaf0b3a5a21d0
ms.contentlocale: is-is
ms.lasthandoff: 11/10/2017

---
# <a name="how-to-restrict-and-allow-usage-of-a-record"></a><span data-ttu-id="ff0eb-103">Hvernig á að takmarka og heimila notkun á færslu</span><span class="sxs-lookup"><span data-stu-id="ff0eb-103">How to: Restrict and Allow Usage of a Record</span></span>
<span data-ttu-id="ff0eb-104">Eigi að varna því að færsla sé notuð í tilteknum aðgerðum, til dæmis, ekki fyrr en færslan hefur verið samþykkt, er hægt að virkja tvö verkflæðissvör sem stýrir notkun færslu.</span><span class="sxs-lookup"><span data-stu-id="ff0eb-104">If you want to restrict a record from being used in certain activities, for example, until the record has been approved, you can incorporate two workflow responses in a workflow that controls the usage of the record.</span></span> <span data-ttu-id="ff0eb-105">Eitt verkflæðissvar mun takmarka notkun færslunnar eins og tilgreint er í verkflæðistilviki og skilyrðum.</span><span class="sxs-lookup"><span data-stu-id="ff0eb-105">One workflow response will restrict usage of the record as defined by the workflow event and conditions.</span></span> <span data-ttu-id="ff0eb-106">Annað verkflæðissvar mun heimila notkun færslunnar eins og tilgreint er í verkflæðistilviki og skilyrðum.</span><span class="sxs-lookup"><span data-stu-id="ff0eb-106">Another workflow response will allow usage of the record as defined by the workflow event and conditions.</span></span> <span data-ttu-id="ff0eb-107">Tvenns konar svörun er til í almennu útgáfunni af [!INCLUDE[d365fin](includes/d365fin_md.md)] í þessum tilgangi: **Takmarka notkun á færslu**</span><span class="sxs-lookup"><span data-stu-id="ff0eb-107">Two responses exist in the generic version of [!INCLUDE[d365fin](includes/d365fin_md.md)] for this purpose: **Restrict usage of a record.**</span></span> <span data-ttu-id="ff0eb-108">og **heimila notkun á færslu**.</span><span class="sxs-lookup"><span data-stu-id="ff0eb-108">and **Allow usage of a record.**.</span></span>

> [!NOTE]  
>  <span data-ttu-id="ff0eb-109">Í almennu útgáfunni af [!INCLUDE[d365fin](includes/d365fin_md.md)] er að finna stuðnig við það að takmarka bókun færslu, útflutning færslu sem greiðslu og prentun færslu sem ávísun væri.</span><span class="sxs-lookup"><span data-stu-id="ff0eb-109">The generic version of [!INCLUDE[d365fin](includes/d365fin_md.md)] offers support for restricting a record from being posted, from being exported as a payment, and from being printed as a check.</span></span> <span data-ttu-id="ff0eb-110">Til að styðja öðrum takmarkanir, verður samstarfsaðila Microsoft að sérstilla kóða forritsins.</span><span class="sxs-lookup"><span data-stu-id="ff0eb-110">To support other restrictions, a Microsoft partner must customize the application code.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="ff0eb-111">Verkflæðisaðgerð til að takmarka og leyfa að færslur séu notaðar tengist ekki þeirri aðgerð að loka að færslur fyrir vörur, viðskiptavini  og lánardrottna séu bókaðar.</span><span class="sxs-lookup"><span data-stu-id="ff0eb-111">The workflow functionality to restrict and allow records from being used is not related to the functionality to block item, customer, and vendor records from being posted.</span></span>

<span data-ttu-id="ff0eb-112">Eftirfarandi ferli sýnir hvernig á að takmarka að innkaupapantanir séu bókað fyrr en þeir hafa verið samþykktar.</span><span class="sxs-lookup"><span data-stu-id="ff0eb-112">The following procedure describes how to restrict purchase orders from being posted until they have been approved.</span></span> <span data-ttu-id="ff0eb-113">Nýja verkflæði verður byggð á fyrirliggjandi verkflæðissniðmáti samþykktarverkflæðis innkaupareiknings.</span><span class="sxs-lookup"><span data-stu-id="ff0eb-113">The new workflow will be based on the existing Purchase Invoice Approval Workflow workflow template.</span></span>  

## <a name="to-create-a-workflow-step-that-restricts-posting-of-unapproved-purchase-orders"></a><span data-ttu-id="ff0eb-114">Til að stofna verkflæðisskref sem takmarka bókun ósamþykktra innkaupapantanir</span><span class="sxs-lookup"><span data-stu-id="ff0eb-114">To create a workflow step that restricts posting of unapproved purchase orders</span></span>  
1. <span data-ttu-id="ff0eb-115">Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Verkflæði** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="ff0eb-115">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Workflows**, and then choose the related link.</span></span>  
2. <span data-ttu-id="ff0eb-116">Í glugganum **Verkflæði** er stofnuð nýtt verkflæði með heitinu Samþykktarverkflæði innkaupapöntunar.</span><span class="sxs-lookup"><span data-stu-id="ff0eb-116">In the **Workflows** window, create a new workflow named Purchase Order Approval Workflow.</span></span> <span data-ttu-id="ff0eb-117">Nánari upplýsingar eru í [Hvernig á að: Stofna verkflæði](across-how-to-create-workflows.md).</span><span class="sxs-lookup"><span data-stu-id="ff0eb-117">For more information, see [How to: Create Workflows](across-how-to-create-workflows.md).</span></span>  
3. <span data-ttu-id="ff0eb-118">Valin er aðgerðin **Afrita úr verkflæðissniðmáti**.</span><span class="sxs-lookup"><span data-stu-id="ff0eb-118">Choose the **Copy From Workflow Template** action.</span></span>  
4. <span data-ttu-id="ff0eb-119">Veljið reitur **Verkflæðiskóði uppruna** og svo í glugganum **Sniðmát verkflæðis** skal velja verkflæðissniðmátið Samþykktarverkflæði innkaupapöntunar.</span><span class="sxs-lookup"><span data-stu-id="ff0eb-119">Choose the **Source Workflow Code** field, and then, in the **Workflow Templates** window, choose the Purchase Invoice Approval Workflow workflow template.</span></span>  

     <span data-ttu-id="ff0eb-120">Takið eftir að fyrstu tvö þrep verkflæði fjalla um að takmarka fyrst og leyfa svo notkun á innkaupareikninga.</span><span class="sxs-lookup"><span data-stu-id="ff0eb-120">Notice that the first two workflow steps are about restricting and then allowing usage of purchase invoices.</span></span> <span data-ttu-id="ff0eb-121">Því næst skal breyta skilyrðum atburðarins í fyrsta skrefið í nýja verkflæði til að tilgreina að það eigi við innkaupapantanir.</span><span class="sxs-lookup"><span data-stu-id="ff0eb-121">Proceed to change the event condition on the first step of the new workflow to specify that it applies to purchase orders.</span></span>  
5. <span data-ttu-id="ff0eb-122">Á flýtiflipi **verkflæðisskref** skal velja reitur **Skilyrði tiliviks** og svo, fyrir síuna **tegund skjals**, skal velja **pöntun**.</span><span class="sxs-lookup"><span data-stu-id="ff0eb-122">On the **Workflow Steps** FastTab, choose the **Event Conditions** field, and then, for the **Document Type** filter, select **Order**.</span></span>  
6. <span data-ttu-id="ff0eb-123">Haldið áfram til að breyta, eyða eða bæta við öðrum verkflæðisskrefum til að passa við viðskiptaferli sem hefst með því að takmarka ósamþykktar innkaupapantanir frá því að vera bókaðar.</span><span class="sxs-lookup"><span data-stu-id="ff0eb-123">Proceed to edit, delete, or add other workflow steps to fit a business process that begins by restricting unapproved purchase orders from being posted.</span></span>  

## <a name="see-also"></a><span data-ttu-id="ff0eb-124">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="ff0eb-124">See Also</span></span>  
<span data-ttu-id="ff0eb-125">[Hvernig á að: Búa til verkflæði](across-how-to-create-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="ff0eb-125">[How to: Create Workflows](across-how-to-create-workflows.md) </span></span>  
[<span data-ttu-id="ff0eb-126">Verkflæði</span><span class="sxs-lookup"><span data-stu-id="ff0eb-126">Workflow</span></span>](across-workflow.md)   

