---
title: Setja upp Skjöl á innleið| Microsoft Docs
description: Nota eiginleikann Skjöl á innleið til að stofna rafræn skjöl, stjórna OCR-verkum, flytja inn reikninga og umbreyta myndaskrám.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 08/10/2020
ms.author: sgroespe
ms.openlocfilehash: 7438502e14d1aa0eecdd56db0eb4ae2f2790413a
ms.sourcegitcommit: 007b331b6974983ee614db0406f00777da359ecb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/10/2020
ms.locfileid: "3677117"
---
# <a name="set-up-incoming-documents"></a><span data-ttu-id="1bca0-103">Setja upp skjöl á innleið</span><span class="sxs-lookup"><span data-stu-id="1bca0-103">Set Up Incoming Documents</span></span>

<span data-ttu-id="1bca0-104">Ef stofnaðar eru færslubókarlínur úr færslum skjala á innleið verður að tilgreina í á síðunni **Uppsetning fyrir skjöl á innleið** hvaða sniðmát færslubókar og runu á að nota.</span><span class="sxs-lookup"><span data-stu-id="1bca0-104">If you create general journal lines from incoming document records, you must specify on the **Incoming Documents Setup** page which journal template and batch to use.</span></span>

<span data-ttu-id="1bca0-105">Ef notendur eiga ekki að geta stofnað reikninga eða færslubókarlínur úr færslum skjala á innleið nema skjöl séu fyrst samþykkt verður að setja upp samþykkjendur verkflæðis.</span><span class="sxs-lookup"><span data-stu-id="1bca0-105">If you do not want users to create invoices or general journal lines from incoming document records unless the documents are first approved, you must set up workflow approvers.</span></span>

<span data-ttu-id="1bca0-106">Til að breyta PDF og myndaskrám í rafræn skjöl sem er hægt að breyta í til dæmis innkaupareikninga innan [!INCLUDE[d365fin](includes/d365fin_md.md)], verður að fyrst að setja upp eiginleikann OCR og virkja þjónustuna.</span><span class="sxs-lookup"><span data-stu-id="1bca0-106">To turn PDF and image files into electronic documents that you can convert to, for example, purchase invoices inside [!INCLUDE[d365fin](includes/d365fin_md.md)], you must first set up the OCR feature and enable the service.</span></span> <span data-ttu-id="1bca0-107">Veljið uppfærslupakka sem er viðeigandi fyrir fyrirtækið og/eða landið/svæðið.</span><span class="sxs-lookup"><span data-stu-id="1bca0-107">Choose a service package that is appropriate for your organization and/or country/region.</span></span> <span data-ttu-id="1bca0-108">Að öðrum kosti er hægt að stofna færslur handvirkt til að tákna ytri skjölin.</span><span class="sxs-lookup"><span data-stu-id="1bca0-108">Alternatively, you can create entries manually to represent the external documents.</span></span>  

<span data-ttu-id="1bca0-109">Þegar eiginleikinn Skjöl á innleið er uppsettur, er hægt að nota ólíkar aðgerðir til að yfirfara kostnaðarkvittanir, sýsla með OCR-verk og breyta skjölum á innleið, handvirkt eða sjálfvirkt, yfir í viðkomandi skjöl eða færslubókarlínur.</span><span class="sxs-lookup"><span data-stu-id="1bca0-109">When the Incoming Documents feature is set up, you can use different functions to review expense receipts, manage OCR tasks, and convert incoming document files, manually or automatically, to the relevant documents or journal lines.</span></span> <span data-ttu-id="1bca0-110">Ytri skrárnar er hægt að hengja við tengd skjöl á öllum stigum úrvinnslunnar, þ.m.t. við bókuð skjöl og við færslur lánardrottins, viðskiptamanns eða fjárhags sem verða til.</span><span class="sxs-lookup"><span data-stu-id="1bca0-110">The external files can be attached at any process stage, including to posted documents and to the resulting vendor, customer, and general ledger entries.</span></span> <span data-ttu-id="1bca0-111">Nánari upplýsingar er að finna í [Vinna skjöl á innleið](across-process-income-documents.md).</span><span class="sxs-lookup"><span data-stu-id="1bca0-111">For more information, see [Processing Incoming Documents](across-process-income-documents.md).</span></span>

## <a name="to-set-up-the-incoming-documents-feature"></a><span data-ttu-id="1bca0-112">Setja upp valkostinn fyrir skjal á innleið</span><span class="sxs-lookup"><span data-stu-id="1bca0-112">To set up the Incoming Documents feature</span></span>

1. <span data-ttu-id="1bca0-113">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Uppsetning skjala á innleið** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="1bca0-113">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Incoming Document Setup**, and then choose the related link.</span></span>
2. <span data-ttu-id="1bca0-114">Fyllið inn reitina eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="1bca0-114">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

<span data-ttu-id="1bca0-115">Sem hluti af uppsetningunni þarf að ákveða hvort krefjast eigi samþykkis á skjölum á innleið.</span><span class="sxs-lookup"><span data-stu-id="1bca0-115">As part of the setup, you must decide if you want to require approval of incoming documents.</span></span> <span data-ttu-id="1bca0-116">Til að krefjast samþykkis þarf að setja upp samþykkjendur og samþykktarverkflæði.</span><span class="sxs-lookup"><span data-stu-id="1bca0-116">To require approval, you must set up approvers and approval workflows.</span></span> <span data-ttu-id="1bca0-117">Ef fyrirtækið ætlar ekki að krefjast samþykkis er hægt að sleppa næsta hluta.</span><span class="sxs-lookup"><span data-stu-id="1bca0-117">If your organization does not intend to require approval, you can skip the next section.</span></span>  

<span data-ttu-id="1bca0-118">Að verður að setja það upp ef þjónusta er notuð til að umbreyta PDF-skrám eða myndskrám sem tákna skjöl á innleið.</span><span class="sxs-lookup"><span data-stu-id="1bca0-118">Finally, you if you use a service to convert PDF or image files representing incoming documents, you must it set up.</span></span> <span data-ttu-id="1bca0-119">Að öðrum kosti er einnig hægt að sleppa þeim hluta.</span><span class="sxs-lookup"><span data-stu-id="1bca0-119">Otherwise, you can also skip that section.</span></span>  

## <a name="to-set-up-approvers-of-incoming-document-records"></a><span data-ttu-id="1bca0-120">Að setja upp samþykkjendur fyrir skjöl á innleið</span><span class="sxs-lookup"><span data-stu-id="1bca0-120">To set up approvers of incoming document records</span></span>

<span data-ttu-id="1bca0-121">Það má setja upp samþykktarferli fyrir skjöl á innleið.</span><span class="sxs-lookup"><span data-stu-id="1bca0-121">Optionally, set up an approval process for the incoming documents.</span></span> <span data-ttu-id="1bca0-122">Samþykkjendur skjala á innleið verða að vera uppsettir sem notendur sem samþykkja verkflæði.</span><span class="sxs-lookup"><span data-stu-id="1bca0-122">Approvers of incoming documents must be set up as approval workflow users.</span></span>

<span data-ttu-id="1bca0-123">Áður en hægt er að stofna verkflæði sem fela í sér samþykktarskref verður að setja upp verkflæðisnotendur sem taka þátt í samþykktarferli.</span><span class="sxs-lookup"><span data-stu-id="1bca0-123">Before you can create workflows that involve approval steps, you must set up the workflow users who are involved in approval processes.</span></span> <span data-ttu-id="1bca0-124">Á síðunni **Uppsetning fyrir samþykki notanda** er einnig hægt að stilla takmörk upphæðar fyrir tilteknar gerðir beiðna og skilgreina staðgengilssamþykkjendur sem samþykktarbeiðnir eru sendar til þegar upphaflegur samþykkjandi er fjarverandi.</span><span class="sxs-lookup"><span data-stu-id="1bca0-124">On the **Approval User Setup** page, you also set amount limits for specific types of requests and define substitute approvers to whom approval requests are delegated when the original approver is absent.</span></span> <span data-ttu-id="1bca0-125">Frekari upplýsingar eru í [Setja upp notendur samþykktar](across-how-to-set-up-approval-users.md).</span><span class="sxs-lookup"><span data-stu-id="1bca0-125">For more information, see [Set Up Approval Users](across-how-to-set-up-approval-users.md).</span></span>

## <a name="to-set-up-an-ocr-service"></a><span data-ttu-id="1bca0-126">Til að setja upp OCR-þjónustu</span><span class="sxs-lookup"><span data-stu-id="1bca0-126">To set up an OCR service</span></span>

1. <span data-ttu-id="1bca0-127">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Uppsetning OCR-þjónustu** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="1bca0-127">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **OCR Service Setup**, and then choose the related link.</span></span>
2. <span data-ttu-id="1bca0-128">Fyllið inn reitina eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="1bca0-128">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
> <span data-ttu-id="1bca0-129">Innskráningargögnin þín eru sjálfkrafa dulrituð.</span><span class="sxs-lookup"><span data-stu-id="1bca0-129">You login data is automatically encrypted.</span></span>

<span data-ttu-id="1bca0-130">Frekari upplýsingar eru í [Hvernig á að nota OCR til að breyta PDF og myndaskrám í rafræn skjöl](across-how-use-ocr-pdf-images-files.md).</span><span class="sxs-lookup"><span data-stu-id="1bca0-130">For more information, see [Use OCR to Turn PDF and Image Files into Electronic Documents](across-how-use-ocr-pdf-images-files.md).</span></span>  

## <a name="see-also"></a><span data-ttu-id="1bca0-131">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="1bca0-131">See Also</span></span>

[<span data-ttu-id="1bca0-132">Vinnsla skjala á innleið</span><span class="sxs-lookup"><span data-stu-id="1bca0-132">Process Incoming Documents</span></span>](across-process-income-documents.md)  
[<span data-ttu-id="1bca0-133">Skjöl á innleið</span><span class="sxs-lookup"><span data-stu-id="1bca0-133">Incoming Documents</span></span>](across-income-documents.md)  
[<span data-ttu-id="1bca0-134">Innkaup</span><span class="sxs-lookup"><span data-stu-id="1bca0-134">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="1bca0-135">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="1bca0-135">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
