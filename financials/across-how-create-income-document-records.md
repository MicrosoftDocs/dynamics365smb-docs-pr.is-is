---
title: "Stofna færslu yfir Skjöl á innleið| Microsoft Docs"
description: "Hægt er að stofna færslur yfir skjöl á innleið, eins og t.d. rafræna reikninga, og stjórna OCR-verkum, netviðskiptum og skjalaskiptum."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 444dabfdcfbf91eb81e281f6f6b4b9f3b184462d
ms.contentlocale: is-is
ms.lasthandoff: 01/30/2018

---
# <a name="create-incoming-document-records"></a><span data-ttu-id="4f0b9-103">Stofna færslur skjala á innleið</span><span class="sxs-lookup"><span data-stu-id="4f0b9-103">Create Incoming Document Records</span></span>
<span data-ttu-id="4f0b9-104">Í glugganum **Skjöl á innleið** er hægt að nota ólíkar aðgerðir til að yfirfara kostnaðarkvittanir, sýsla með OCR-verk og breyta skjölum á innleið, handvirkt eða sjálfvirkt, yfir í viðkomandi skjöl eða færslubókarlínur í.</span><span class="sxs-lookup"><span data-stu-id="4f0b9-104">In the **Incoming Documents** window, you can use different functions to review expense receipts, manage OCR tasks, and convert incoming document files, manually or automatically, to the relevant documents or journal lines.</span></span> <span data-ttu-id="4f0b9-105">Ytri skrárnar er hægt að hengja við tengd skjöl á öllum stigum úrvinnslunnar, þ.m.t. við bókuð skjöl og við færslur lánardrottins, viðskiptamanns eða fjárhags sem verða til.</span><span class="sxs-lookup"><span data-stu-id="4f0b9-105">The external files can be attached at any process stage, including to posted documents and to the resulting vendor, customer, and general ledger entries.</span></span>

<span data-ttu-id="4f0b9-106">Til að skrá ytra skjal í [!INCLUDE[d365fin](includes/d365fin_md.md)] verður fyrst að stofna eða ljúka við færslu fyrir skjal á innleið.</span><span class="sxs-lookup"><span data-stu-id="4f0b9-106">To record an external document in [!INCLUDE[d365fin](includes/d365fin_md.md)], you must first create or complete an incoming document record.</span></span> <span data-ttu-id="4f0b9-107">Þú getur gert þetta með handvirkt, eða þú getur tekið mynd af ytra skjal og síðan að búa til skjal á innleið með myndaskrá í viðhengi.</span><span class="sxs-lookup"><span data-stu-id="4f0b9-107">You can do this manually, or you can take a photo of the external document and then create the incoming document record with the image file attached.</span></span>

<span data-ttu-id="4f0b9-108">Áður en hægt er að nota valkostinn Skjöl á innleið þarf að framkvæma áskilda uppsetningu.</span><span class="sxs-lookup"><span data-stu-id="4f0b9-108">Before you can use the Incoming Documents feature, you must perform the required setup.</span></span> <span data-ttu-id="4f0b9-109">Frekari upplýsingar eru í [Setja upp skjöl á innleið](across-how-setup-income-documents.md).</span><span class="sxs-lookup"><span data-stu-id="4f0b9-109">For more information, see [Set Up Incoming Documents](across-how-setup-income-documents.md).</span></span>

## <a name="to-approve-or-reject-an-incoming-document"></a><span data-ttu-id="4f0b9-110">Til að samþykkja eða hafna fylgiskjali á innleið</span><span class="sxs-lookup"><span data-stu-id="4f0b9-110">To approve or reject an incoming document</span></span>
<span data-ttu-id="4f0b9-111">Ef notendur eiga að geta stofnað reikninga eða færslubókarlínur úr færslum skjala á innleið nema skjöl séu fyrst samþykkt er hægt að setja upp samþykkjendur sem verða að samþykkja færslur áður en þær má vinna.</span><span class="sxs-lookup"><span data-stu-id="4f0b9-111">If you do want to allow users to create invoices or general journal lines from incoming document records unless they are approved, you can set up approvers who must approve the records before they can be processed.</span></span>

1. <span data-ttu-id="4f0b9-112">Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **skjöl á innleið** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="4f0b9-112">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Incoming Documents**, and then choose the related link.</span></span>
2. <span data-ttu-id="4f0b9-113">Valin er línan með skjalinu sem á að samþykkja eða hafna og síðan valið á **Samþykkja** eða **Hafna** aðgerðir.</span><span class="sxs-lookup"><span data-stu-id="4f0b9-113">Select the line with the document that you want to approve or reject, and then choose the **Approve** or **Reject** actions.</span></span>

<span data-ttu-id="4f0b9-114">Ef færsla skjals á innleið er samþykkt er gátreiturinn **Losað** á línu skjal á innleið valinn.</span><span class="sxs-lookup"><span data-stu-id="4f0b9-114">If you approve the incoming document record, the **Released** check box on the incoming document line is selected.</span></span> <span data-ttu-id="4f0b9-115">Notandi sem stjórnar t.d. stofnun innkaupareikninga getur haldið áfram að vinna úr færslunni.</span><span class="sxs-lookup"><span data-stu-id="4f0b9-115">The user in charge of creating, for example, purchase invoices can proceed to process the record.</span></span>

## <a name="to-create-an-incoming-document-record-by-taking-a-photo"></a><span data-ttu-id="4f0b9-116">Til að stofna færslur skjala á innleið með því að taka mynd</span><span class="sxs-lookup"><span data-stu-id="4f0b9-116">To create an incoming document record by taking a photo</span></span>
> [!NOTE]  
>   <span data-ttu-id="4f0b9-117">Eftirfarandi ferli á aðeins við um [!INCLUDE[d365fin](includes/d365fin_md.md)] biðlara spjaldtölva og síma.</span><span class="sxs-lookup"><span data-stu-id="4f0b9-117">The following procedure only applies to the [!INCLUDE[d365fin](includes/d365fin_md.md)] Tablet and Phone clients.</span></span>

1. <span data-ttu-id="4f0b9-118">Á forritastikunni skal velja **Stofna skjal á innleið úr myndavél** reitinn og fara svo í skref 4..</span><span class="sxs-lookup"><span data-stu-id="4f0b9-118">On the app bar, choose the **Create Incoming Document from Camera** tile, and then go to step 4.</span></span>
2. <span data-ttu-id="4f0b9-119">Að öðrum kosti skal á forritastikunni velja valkostahnappinn, velja **Skjöl á innleið** og velja svo **Öll**.</span><span class="sxs-lookup"><span data-stu-id="4f0b9-119">Alternatively, on the app bar, choose the options button, choose **Incoming Documents**, and then choose **All**.</span></span>
3. <span data-ttu-id="4f0b9-120">Í glugganum **Skjöl á innleið** skal velja úrfellingarmerkishnappinn og svo **Stofna úr myndavél**.</span><span class="sxs-lookup"><span data-stu-id="4f0b9-120">In the **Incoming Documents** window, choose the ellipsis button, and then choose **Create from Camera**.</span></span> <span data-ttu-id="4f0b9-121">Kveikt er á myndavél spjaldtölvu eða síma.</span><span class="sxs-lookup"><span data-stu-id="4f0b9-121">The camera on the tablet or phone is activated.</span></span>
4. <span data-ttu-id="4f0b9-122">Takið mynd af skjali, t.d. innkaupakvittun, sem á að vinna sem skjal á innleið, og veljið svo hnappur **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="4f0b9-122">Take a photo of a document, such as a purchase receipt, that you want to process as an incoming document, and then choose the **OK** button.</span></span>

    <span data-ttu-id="4f0b9-123">Ný færsla skjals á innleið er stofnað með mynd í viðhengi.</span><span class="sxs-lookup"><span data-stu-id="4f0b9-123">A new incoming document record is created, with the image attached.</span></span>

## <a name="to-attach-an-image-to-an-incoming-document-record-by-taking-a-photo"></a><span data-ttu-id="4f0b9-124">Til að hengja mynd við skjal á innleið færsla með því að taka mynd</span><span class="sxs-lookup"><span data-stu-id="4f0b9-124">To attach an image to an incoming document record by taking a photo</span></span>
> [!NOTE]  
>   <span data-ttu-id="4f0b9-125">Eftirfarandi ferli á aðeins við um [!INCLUDE[d365fin](includes/d365fin_md.md)] biðlara spjaldtölva og síma.</span><span class="sxs-lookup"><span data-stu-id="4f0b9-125">The following procedure only applies to the [!INCLUDE[d365fin](includes/d365fin_md.md)] Tablet and Phone clients.</span></span>

1. <span data-ttu-id="4f0b9-126">Á forritastikunni velja valkostahnappinn, velja **Skjöl á innleið** og velja svo **Öll**.</span><span class="sxs-lookup"><span data-stu-id="4f0b9-126">On the app bar, choose the options button, choose **Incoming Documents**, and then choose **All**.</span></span>
2. <span data-ttu-id="4f0b9-127">Opnið kort fyrir fyrirliggjandi færsla skjal á innleið.</span><span class="sxs-lookup"><span data-stu-id="4f0b9-127">Open the card for an existing incoming document record.</span></span>
3. <span data-ttu-id="4f0b9-128">Í glugganum **Skjal á innleið** skal velja úrfellingarmerkishnappinn og svo **Hengja við mynd úr myndavél**.</span><span class="sxs-lookup"><span data-stu-id="4f0b9-128">In the **Incoming Document** window, choose the ellipsis button, and then choose **Attach Image from Camera**.</span></span> <span data-ttu-id="4f0b9-129">Kveikt er á myndavél spjaldtölvu eða síma.</span><span class="sxs-lookup"><span data-stu-id="4f0b9-129">The camera on the tablet or phone is activated.</span></span>
4. <span data-ttu-id="4f0b9-130">Takið mynd af skjali, t.d. innkaupakvittun, sem á að vinna sem skjal á innleið, og veljið svo hnappur **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="4f0b9-130">Take a photo of a document, such as a purchase receipt, that you want to process as an incoming document, and then choose the **OK** button.</span></span>

    <span data-ttu-id="4f0b9-131">Myndin er hengja við færsla skjal á innleið.</span><span class="sxs-lookup"><span data-stu-id="4f0b9-131">The image is attached to the incoming document record.</span></span>

## <a name="to-create-an-incoming-document-record-manually"></a><span data-ttu-id="4f0b9-132">Tila ð búa til færslu skjals á innleið handvirkt</span><span class="sxs-lookup"><span data-stu-id="4f0b9-132">To create an incoming document record manually</span></span>
1. <span data-ttu-id="4f0b9-133">Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **skjöl á innleið** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="4f0b9-133">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Incoming Documents**, and then choose the related link.</span></span>
2. <span data-ttu-id="4f0b9-134">Aðgerðin **Stofna úr Skrá** er valin.</span><span class="sxs-lookup"><span data-stu-id="4f0b9-134">Choose the **Create from File** action.</span></span>  
3. <span data-ttu-id="4f0b9-135">Í glugganum **Setja inn skrá** skal velja skrána sem táknar skjalið á innleið og svo hnappinn **Opna**.</span><span class="sxs-lookup"><span data-stu-id="4f0b9-135">In the **Insert File** window, select a file, and then choose **Open**.</span></span> <span data-ttu-id="4f0b9-136">Skráin er hengd við sjálfkrafa.</span><span class="sxs-lookup"><span data-stu-id="4f0b9-136">The file is automatically attached.</span></span>
4. <span data-ttu-id="4f0b9-137">Einnig er hægt að velja aðgerðina **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="4f0b9-137">Alternatively, choose the **New** action.</span></span>
5. <span data-ttu-id="4f0b9-138">Ef tengja á skrá, skal velja **Tengja Skrá** aðgerð.</span><span class="sxs-lookup"><span data-stu-id="4f0b9-138">To attach a file, choose the **Attach File** action.</span></span>
6. <span data-ttu-id="4f0b9-139">Í glugganum **Setja inn skrá** skal velja skrána sem táknar skjalið á innleið og svo hnappinn **Opna**.</span><span class="sxs-lookup"><span data-stu-id="4f0b9-139">In the **Insert File** window, select the file that represents the incoming document in question, and then choose the **Open** button.</span></span>
7. <span data-ttu-id="4f0b9-140">Í glugganum **Skjal á innleið** þarf að fylla reitina út eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="4f0b9-140">In the **Incoming Document** window, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="see-also"></a><span data-ttu-id="4f0b9-141">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="4f0b9-141">See Also</span></span>
[<span data-ttu-id="4f0b9-142">Vinnsla skjala á innleið</span><span class="sxs-lookup"><span data-stu-id="4f0b9-142">Process Incoming Documents</span></span>](across-process-income-documents.md)  
[<span data-ttu-id="4f0b9-143">Skjöl á innleið</span><span class="sxs-lookup"><span data-stu-id="4f0b9-143">Incoming Documents</span></span>](across-income-documents.md)  
[<span data-ttu-id="4f0b9-144">Innkaup</span><span class="sxs-lookup"><span data-stu-id="4f0b9-144">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="4f0b9-145">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="4f0b9-145">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

