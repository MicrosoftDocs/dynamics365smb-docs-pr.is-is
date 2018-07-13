---
title: "Setja upp Skjöl á innleið| Microsoft Docs"
description: "Nota eiginleikann Skjöl á innleið til að stofna rafræn skjöl, stjórna OCR-verkum, flytja inn reikninga og umbreyta myndaskrám."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 06/08/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: e73c2dd0533aade4aa6225c9d2f385baaea3cfd1
ms.openlocfilehash: ea5673f341954960852de33cb94ee5722c8dbe26
ms.contentlocale: is-is
ms.lasthandoff: 06/11/2018

---
# <a name="set-up-incoming-documents"></a><span data-ttu-id="f0402-103">Setja upp skjöl á innleið</span><span class="sxs-lookup"><span data-stu-id="f0402-103">Set Up Incoming Documents</span></span>
<span data-ttu-id="f0402-104">Ef stofnaðar eru færslubókarlínur úr færslum skjala á innleið verður að tilgreina í í glugganum **Uppsetning fyrir skjöl á innleið** hvaða sniðmát færslubókar og runu á að nota.</span><span class="sxs-lookup"><span data-stu-id="f0402-104">If you create general journal lines from incoming document records, you must specify in the **Incoming Documents Setup** window which journal template and batch to use.</span></span>

<span data-ttu-id="f0402-105">Ef notendur eiga ekki að geta stofnað reikninga eða færslubókarlínur úr færslum skjala á innleið nema skjöl séu fyrst samþykkt verður að setja upp samþykkjendur í glugganum **Samþykkjendur skjala á innleið**.</span><span class="sxs-lookup"><span data-stu-id="f0402-105">If you do not want users to create invoices or general journal lines from incoming document records unless the documents are first approved, you must set up approvers in the **Incoming Document Approvers** window.</span></span>

<span data-ttu-id="f0402-106">Til að breyta PDF og myndaskrám í rafræn skjöl sem er hægt að breyta í til dæmis innkaupareikninga innan [!INCLUDE[d365fin](includes/d365fin_md.md)], verður að fyrst að setja upp eiginleikann OCR og virkja þjónustuna.</span><span class="sxs-lookup"><span data-stu-id="f0402-106">To turn PDF and image files into electronic documents that you can convert to, for example, purchase invoices inside [!INCLUDE[d365fin](includes/d365fin_md.md)], you must first set up the OCR feature and enable the service.</span></span>

<span data-ttu-id="f0402-107">Þegar eiginleikinn Skjöl á innleið er uppsettur, er hægt að nota ólíkar aðgerðir til að yfirfara kostnaðarkvittanir, sýsla með OCR-verk og breyta skjölum á innleið, handvirkt eða sjálfvirkt, yfir í viðkomandi skjöl eða færslubókarlínur.</span><span class="sxs-lookup"><span data-stu-id="f0402-107">When the Incoming Documents feature is set up, you can use different functions to review expense receipts, manage OCR tasks, and convert incoming document files, manually or automatically, to the relevant documents or journal lines.</span></span> <span data-ttu-id="f0402-108">Ytri skrárnar er hægt að hengja við tengd skjöl á öllum stigum úrvinnslunnar, þ.m.t. við bókuð skjöl og við færslur lánardrottins, viðskiptamanns eða fjárhags sem verða til.</span><span class="sxs-lookup"><span data-stu-id="f0402-108">The external files can be attached at any process stage, including to posted documents and to the resulting vendor, customer, and general ledger entries.</span></span> <span data-ttu-id="f0402-109">Nánari upplýsingar er að finna í [Vinna skjöl á innleið](across-process-income-documents.md).</span><span class="sxs-lookup"><span data-stu-id="f0402-109">For more information, see [Processing Incoming Documents](across-process-income-documents.md).</span></span>

## <a name="to-set-up-the-incoming-documents-feature"></a><span data-ttu-id="f0402-110">Setja upp valkostinn fyrir skjal á innleið</span><span class="sxs-lookup"><span data-stu-id="f0402-110">To set up the Incoming Documents feature</span></span>
1. <span data-ttu-id="f0402-111">Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Uppsetning fyrir skjöl á innleið** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="f0402-111">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Incoming Document Setup**, and then choose the related link.</span></span>
2. <span data-ttu-id="f0402-112">Fyllið inn í svæðin eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="f0402-112">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-set-up-approvers-of-incoming-document-records"></a><span data-ttu-id="f0402-113">Að setja upp samþykkjendur fyrir skjöl á innleið</span><span class="sxs-lookup"><span data-stu-id="f0402-113">To set up approvers of incoming document records</span></span>
1. <span data-ttu-id="f0402-114">Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Uppsetning fyrir skjöl á innleið** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="f0402-114">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Incoming Document Setup**, and then choose the related link.</span></span>  
2. <span data-ttu-id="f0402-115">Í glugganum **Skjal á innleið** skal velja aðgerðina **Samþykkjendur**</span><span class="sxs-lookup"><span data-stu-id="f0402-115">In the **Incoming Documents Setup** window, choose the **Approvers** action.</span></span>

    <span data-ttu-id="f0402-116">Glugginn **Samþykkjendur skjala á innleið** sýnir alla notendur sem hafa verið settir upp í [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="f0402-116">The **Incoming Document Approvers** window shows all users that are set up in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  
3. <span data-ttu-id="f0402-117">Veldu einn eða fleiri notendur sem geta samþykkt innsent skjal áður en hægt er að stofna fylgiskjals - eða bókarlínu.</span><span class="sxs-lookup"><span data-stu-id="f0402-117">Select one or more users that can approve an incoming document before a related document or journal line can be created.</span></span>

<span data-ttu-id="f0402-118">Þegar samþykkjendur hafa verið settir upp í glugganum **Samþykkjendur skjala á innleið** geta aðeins þessir notendur samþykkt skjal á innleið ef gátreitur **Krefjast samþykkis fyrir stofnun** í glugganum **uppsetning skjala á innleið** er valinn.</span><span class="sxs-lookup"><span data-stu-id="f0402-118">When approvers have been set up in the **Incoming Document Approvers** window, only those users can approve an incoming document if the **Require Approval To Create** check box in the **Incoming Documents Setup** window is selected.</span></span>

> [!NOTE]  
>   <span data-ttu-id="f0402-119">Þessi uppsetning samþykkis er ekki tengd samþykktarverkflæðum.</span><span class="sxs-lookup"><span data-stu-id="f0402-119">This approval setup is not related to approval workflows.</span></span> <span data-ttu-id="f0402-120">Frekari upplýsingar eru í [Nota verkflæði samþykktar](across-how-use-approval-workflows.md).</span><span class="sxs-lookup"><span data-stu-id="f0402-120">For more information, see [Use Approval Workflows](across-how-use-approval-workflows.md).</span></span>

## <a name="to-set-up-an-ocr-service"></a><span data-ttu-id="f0402-121">Til að setja upp OCR-þjónustu</span><span class="sxs-lookup"><span data-stu-id="f0402-121">To set up an OCR service</span></span>
1. <span data-ttu-id="f0402-122">Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Uppsetning OCR-þjónustu** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="f0402-122">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **OCR Service Setup**, and then choose the related link.</span></span>
2. <span data-ttu-id="f0402-123">Fyllið inn í reitina eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="f0402-123">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
> <span data-ttu-id="f0402-124">Innskráningargögnin þín eru sjálfkrafa dulrituð.</span><span class="sxs-lookup"><span data-stu-id="f0402-124">You login data is automatically encrypted.</span></span>

## <a name="see-also"></a><span data-ttu-id="f0402-125">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="f0402-125">See Also</span></span>
[<span data-ttu-id="f0402-126">Vinnsla skjala á innleið</span><span class="sxs-lookup"><span data-stu-id="f0402-126">Process Incoming Documents</span></span>](across-process-income-documents.md)  
[<span data-ttu-id="f0402-127">Skjöl á innleið</span><span class="sxs-lookup"><span data-stu-id="f0402-127">Incoming Documents</span></span>](across-income-documents.md)  
[<span data-ttu-id="f0402-128">Innkaup</span><span class="sxs-lookup"><span data-stu-id="f0402-128">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="f0402-129">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="f0402-129">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

