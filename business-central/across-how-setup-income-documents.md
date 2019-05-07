---
title: Setja upp Skjöl á innleið| Microsoft Docs
description: Nota eiginleikann Skjöl á innleið til að stofna rafræn skjöl, stjórna OCR-verkum, flytja inn reikninga og umbreyta myndaskrám.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 7e99f4b33767a1bdea7b942d1b183edbacc829ac
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2019
ms.locfileid: "932742"
---
# <a name="set-up-incoming-documents"></a><span data-ttu-id="5495e-103">Setja upp skjöl á innleið</span><span class="sxs-lookup"><span data-stu-id="5495e-103">Set Up Incoming Documents</span></span>
<span data-ttu-id="5495e-104">Ef stofnaðar eru færslubókarlínur úr færslum skjala á innleið verður að tilgreina í á síðunni **Uppsetning fyrir skjöl á innleið** hvaða sniðmát færslubókar og runu á að nota.</span><span class="sxs-lookup"><span data-stu-id="5495e-104">If you create general journal lines from incoming document records, you must specify on the **Incoming Documents Setup** page which journal template and batch to use.</span></span>

<span data-ttu-id="5495e-105">Ef notendur eiga ekki að geta stofnað reikninga eða færslubókarlínur úr færslum skjala á innleið nema skjöl séu fyrst samþykkt verður að setja upp samþykkjendur á síðunni **Samþykkjendur skjala á innleið**.</span><span class="sxs-lookup"><span data-stu-id="5495e-105">If you do not want users to create invoices or general journal lines from incoming document records unless the documents are first approved, you must set up approvers on the **Incoming Document Approvers** page.</span></span>

<span data-ttu-id="5495e-106">Til að breyta PDF og myndaskrám í rafræn skjöl sem er hægt að breyta í til dæmis innkaupareikninga innan [!INCLUDE[d365fin](includes/d365fin_md.md)], verður að fyrst að setja upp eiginleikann OCR og virkja þjónustuna.</span><span class="sxs-lookup"><span data-stu-id="5495e-106">To turn PDF and image files into electronic documents that you can convert to, for example, purchase invoices inside [!INCLUDE[d365fin](includes/d365fin_md.md)], you must first set up the OCR feature and enable the service.</span></span>

<span data-ttu-id="5495e-107">Þegar eiginleikinn Skjöl á innleið er uppsettur, er hægt að nota ólíkar aðgerðir til að yfirfara kostnaðarkvittanir, sýsla með OCR-verk og breyta skjölum á innleið, handvirkt eða sjálfvirkt, yfir í viðkomandi skjöl eða færslubókarlínur.</span><span class="sxs-lookup"><span data-stu-id="5495e-107">When the Incoming Documents feature is set up, you can use different functions to review expense receipts, manage OCR tasks, and convert incoming document files, manually or automatically, to the relevant documents or journal lines.</span></span> <span data-ttu-id="5495e-108">Ytri skrárnar er hægt að hengja við tengd skjöl á öllum stigum úrvinnslunnar, þ.m.t. við bókuð skjöl og við færslur lánardrottins, viðskiptamanns eða fjárhags sem verða til.</span><span class="sxs-lookup"><span data-stu-id="5495e-108">The external files can be attached at any process stage, including to posted documents and to the resulting vendor, customer, and general ledger entries.</span></span> <span data-ttu-id="5495e-109">Nánari upplýsingar er að finna í [Vinna skjöl á innleið](across-process-income-documents.md).</span><span class="sxs-lookup"><span data-stu-id="5495e-109">For more information, see [Processing Incoming Documents](across-process-income-documents.md).</span></span>

## <a name="to-set-up-the-incoming-documents-feature"></a><span data-ttu-id="5495e-110">Setja upp valkostinn fyrir skjal á innleið</span><span class="sxs-lookup"><span data-stu-id="5495e-110">To set up the Incoming Documents feature</span></span>
1. <span data-ttu-id="5495e-111">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **uppsetning skjals á innleið** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="5495e-111">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Incoming Document Setup**, and then choose the related link.</span></span>
2. <span data-ttu-id="5495e-112">Fyllið inn í svæðin eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="5495e-112">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-set-up-approvers-of-incoming-document-records"></a><span data-ttu-id="5495e-113">Að setja upp samþykkjendur fyrir skjöl á innleið</span><span class="sxs-lookup"><span data-stu-id="5495e-113">To set up approvers of incoming document records</span></span>
1. <span data-ttu-id="5495e-114">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **uppsetning skjals á innleið** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="5495e-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Incoming Document Setup**, and then choose the related link.</span></span>  
2. <span data-ttu-id="5495e-115">Á síðunni **Skjal á innleið** skal velja aðgerðina **Samþykkjendur**.</span><span class="sxs-lookup"><span data-stu-id="5495e-115">On the **Incoming Documents Setup** page, choose the **Approvers** action.</span></span>

    <span data-ttu-id="5495e-116">Síðan **Samþykkjendur skjala á innleið** sýnir alla notendur sem hafa verið settir upp í [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="5495e-116">The **Incoming Document Approvers** page shows all users that are set up in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  
3. <span data-ttu-id="5495e-117">Veldu einn eða fleiri notendur sem geta samþykkt innsent skjal áður en hægt er að stofna fylgiskjals - eða bókarlínu.</span><span class="sxs-lookup"><span data-stu-id="5495e-117">Select one or more users that can approve an incoming document before a related document or journal line can be created.</span></span>

<span data-ttu-id="5495e-118">Þegar samþykkjendur hafa verið settir upp á síðunni **Samþykkjendur skjala á innleið** geta aðeins þessir notendur samþykkt skjal á innleið ef gátreitur **Krefjast samþykkis fyrir stofnun** á síðunni **Uppsetning skjala á innleið** er valinn.</span><span class="sxs-lookup"><span data-stu-id="5495e-118">When approvers have been set up on the **Incoming Document Approvers** page, only those users can approve an incoming document if the **Require Approval To Create** check box on the **Incoming Documents Setup** page is selected.</span></span>

> [!NOTE]  
>   <span data-ttu-id="5495e-119">Þessi uppsetning samþykkis er ekki tengd samþykktarverkflæðum.</span><span class="sxs-lookup"><span data-stu-id="5495e-119">This approval setup is not related to approval workflows.</span></span> <span data-ttu-id="5495e-120">Frekari upplýsingar eru í [Nota verkflæði samþykktar](across-how-use-approval-workflows.md).</span><span class="sxs-lookup"><span data-stu-id="5495e-120">For more information, see [Use Approval Workflows](across-how-use-approval-workflows.md).</span></span>

## <a name="to-set-up-an-ocr-service"></a><span data-ttu-id="5495e-121">Til að setja upp OCR-þjónustu</span><span class="sxs-lookup"><span data-stu-id="5495e-121">To set up an OCR service</span></span>
1. <span data-ttu-id="5495e-122">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **uppsetning OCR-þjónustu** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="5495e-122">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **OCR Service Setup**, and then choose the related link.</span></span>
2. <span data-ttu-id="5495e-123">Fyllið inn í reitina eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="5495e-123">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
> <span data-ttu-id="5495e-124">Innskráningargögnin þín eru sjálfkrafa dulrituð.</span><span class="sxs-lookup"><span data-stu-id="5495e-124">You login data is automatically encrypted.</span></span>

## <a name="see-also"></a><span data-ttu-id="5495e-125">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="5495e-125">See Also</span></span>
[<span data-ttu-id="5495e-126">Vinnsla skjala á innleið</span><span class="sxs-lookup"><span data-stu-id="5495e-126">Process Incoming Documents</span></span>](across-process-income-documents.md)  
[<span data-ttu-id="5495e-127">Skjöl á innleið</span><span class="sxs-lookup"><span data-stu-id="5495e-127">Incoming Documents</span></span>](across-income-documents.md)  
[<span data-ttu-id="5495e-128">Innkaup</span><span class="sxs-lookup"><span data-stu-id="5495e-128">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="5495e-129">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="5495e-129">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
