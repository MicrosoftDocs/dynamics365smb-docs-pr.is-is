---
title: Stofna færslu yfir Skjöl á innleið| Microsoft Docs
description: Hægt er að stofna færslur yfir skjöl á innleið, eins og t.d. rafræna reikninga, og stjórna OCR-verkum, netviðskiptum og skjalaskiptum.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 722e69389413dc06db4f2b7fd2f8447d9033d030
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/17/2020
ms.locfileid: "4753293"
---
# <a name="create-incoming-document-records"></a><span data-ttu-id="d1ee8-103">Stofna færslur skjala á innleið</span><span class="sxs-lookup"><span data-stu-id="d1ee8-103">Create Incoming Document Records</span></span>
<span data-ttu-id="d1ee8-104">Á síðunni **Skjöl á innleið** er hægt að nota ólíkar aðgerðir til að yfirfara kostnaðarkvittanir, sýsla með OCR-verk og breyta skjölum á innleið, handvirkt eða sjálfvirkt, yfir í viðkomandi skjöl eða færslubókarlínur í.</span><span class="sxs-lookup"><span data-stu-id="d1ee8-104">On the **Incoming Documents** page, you can use different functions to review expense receipts, manage OCR tasks, and convert incoming document files, manually or automatically, to the relevant documents or journal lines.</span></span> <span data-ttu-id="d1ee8-105">Ytri skrárnar er hægt að hengja við tengd skjöl á öllum stigum úrvinnslunnar, þ.m.t. við bókuð skjöl og við færslur lánardrottins, viðskiptamanns eða fjárhags sem verða til.</span><span class="sxs-lookup"><span data-stu-id="d1ee8-105">The external files can be attached at any process stage, including to posted documents and to the resulting vendor, customer, and general ledger entries.</span></span>

<span data-ttu-id="d1ee8-106">Til að skrá ytra skjal í [!INCLUDE[prod_short](includes/prod_short.md)] verður fyrst að stofna eða ljúka við færslu fyrir skjal á innleið.</span><span class="sxs-lookup"><span data-stu-id="d1ee8-106">To record an external document in [!INCLUDE[prod_short](includes/prod_short.md)], you must first create or complete an incoming document record.</span></span> <span data-ttu-id="d1ee8-107">Þú getur gert þetta með handvirkt, eða þú getur tekið mynd af ytra skjal og síðan að búa til skjal á innleið með myndaskrá í viðhengi.</span><span class="sxs-lookup"><span data-stu-id="d1ee8-107">You can do this manually, or you can take a photo of the external document and then create the incoming document record with the image file attached.</span></span>

<span data-ttu-id="d1ee8-108">Áður en hægt er að nota valkostinn Skjöl á innleið þarf að framkvæma áskilda uppsetningu.</span><span class="sxs-lookup"><span data-stu-id="d1ee8-108">Before you can use the Incoming Documents feature, you must perform the required setup.</span></span> <span data-ttu-id="d1ee8-109">Frekari upplýsingar eru í [Setja upp skjöl á innleið](across-how-setup-income-documents.md).</span><span class="sxs-lookup"><span data-stu-id="d1ee8-109">For more information, see [Set Up Incoming Documents](across-how-setup-income-documents.md).</span></span>

## <a name="to-approve-or-reject-an-incoming-document"></a><span data-ttu-id="d1ee8-110">Til að samþykkja eða hafna fylgiskjali á innleið</span><span class="sxs-lookup"><span data-stu-id="d1ee8-110">To approve or reject an incoming document</span></span>
<span data-ttu-id="d1ee8-111">Ef notendur eiga að geta stofnað reikninga eða færslubókarlínur úr færslum skjala á innleið nema skjöl séu fyrst samþykkt er hægt að setja upp samþykkjendur sem verða að samþykkja færslur áður en þær má vinna.</span><span class="sxs-lookup"><span data-stu-id="d1ee8-111">If you do want to allow users to create invoices or general journal lines from incoming document records unless they are approved, you can set up approvers who must approve the records before they can be processed.</span></span>

1. <span data-ttu-id="d1ee8-112">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Skjöl á innleið** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="d1ee8-112">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Incoming Documents**, and then choose the related link.</span></span>
2. <span data-ttu-id="d1ee8-113">Valin er línan með skjalinu sem á að samþykkja eða hafna og síðan valið á **Samþykkja** eða **Hafna** aðgerðir.</span><span class="sxs-lookup"><span data-stu-id="d1ee8-113">Select the line with the document that you want to approve or reject, and then choose the **Approve** or **Reject** actions.</span></span>

<span data-ttu-id="d1ee8-114">Ef færsla skjals á innleið er samþykkt er gátreiturinn **Losað** á línu skjal á innleið valinn.</span><span class="sxs-lookup"><span data-stu-id="d1ee8-114">If you approve the incoming document record, the **Released** check box on the incoming document line is selected.</span></span> <span data-ttu-id="d1ee8-115">Notandi sem stjórnar t.d. stofnun innkaupareikninga getur haldið áfram að vinna úr færslunni.</span><span class="sxs-lookup"><span data-stu-id="d1ee8-115">The user in charge of creating, for example, purchase invoices can proceed to process the record.</span></span>

## <a name="to-create-an-incoming-document-record-by-taking-a-photo"></a><span data-ttu-id="d1ee8-116">Til að stofna færslur skjala á innleið með því að taka mynd</span><span class="sxs-lookup"><span data-stu-id="d1ee8-116">To create an incoming document record by taking a photo</span></span>
> [!NOTE]  
>   <span data-ttu-id="d1ee8-117">Eftirfarandi ferli á aðeins við um [!INCLUDE[prod_short](includes/prod_short.md)] biðlara spjaldtölva og síma.</span><span class="sxs-lookup"><span data-stu-id="d1ee8-117">The following procedure only applies to the [!INCLUDE[prod_short](includes/prod_short.md)] Tablet and Phone clients.</span></span>

1. <span data-ttu-id="d1ee8-118">Á forritastikunni skal velja **Stofna skjal á innleið úr myndavél** reitinn og fara svo í skref 4..</span><span class="sxs-lookup"><span data-stu-id="d1ee8-118">On the app bar, choose the **Create Incoming Document from Camera** tile, and then go to step 4.</span></span>
2. <span data-ttu-id="d1ee8-119">Að öðrum kosti skal á forritastikunni velja valkostahnappinn, velja **Skjöl á innleið** og velja svo **Öll**.</span><span class="sxs-lookup"><span data-stu-id="d1ee8-119">Alternatively, on the app bar, choose the options button, choose **Incoming Documents**, and then choose **All**.</span></span>
3. <span data-ttu-id="d1ee8-120">Á síðunni **Skjöl á innleið** skal velja úrfellingarmerkishnappinn og svo **Stofna úr myndavél**.</span><span class="sxs-lookup"><span data-stu-id="d1ee8-120">On the **Incoming Documents** page, choose the ellipsis button, and then choose **Create from Camera**.</span></span> <span data-ttu-id="d1ee8-121">Kveikt er á myndavél spjaldtölvu eða síma.</span><span class="sxs-lookup"><span data-stu-id="d1ee8-121">The camera on the tablet or phone is activated.</span></span>
4. <span data-ttu-id="d1ee8-122">Takið mynd af skjali, t.d. innkaupakvittun, sem á að vinna sem skjal á innleið, og veljið svo hnappur **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="d1ee8-122">Take a photo of a document, such as a purchase receipt, that you want to process as an incoming document, and then choose the **OK** button.</span></span>

    <span data-ttu-id="d1ee8-123">Ný færsla skjals á innleið er stofnað með mynd í viðhengi.</span><span class="sxs-lookup"><span data-stu-id="d1ee8-123">A new incoming document record is created, with the image attached.</span></span>

## <a name="to-attach-an-image-to-an-incoming-document-record-by-taking-a-photo"></a><span data-ttu-id="d1ee8-124">Til að hengja mynd við skjal á innleið færsla með því að taka mynd</span><span class="sxs-lookup"><span data-stu-id="d1ee8-124">To attach an image to an incoming document record by taking a photo</span></span>
> [!NOTE]  
>   <span data-ttu-id="d1ee8-125">Eftirfarandi ferli á aðeins við um [!INCLUDE[prod_short](includes/prod_short.md)] biðlara spjaldtölva og síma.</span><span class="sxs-lookup"><span data-stu-id="d1ee8-125">The following procedure only applies to the [!INCLUDE[prod_short](includes/prod_short.md)] Tablet and Phone clients.</span></span>

1. <span data-ttu-id="d1ee8-126">Á forritastikunni velja valkostahnappinn, velja **Skjöl á innleið** og velja svo **Öll**.</span><span class="sxs-lookup"><span data-stu-id="d1ee8-126">On the app bar, choose the options button, choose **Incoming Documents**, and then choose **All**.</span></span>
2. <span data-ttu-id="d1ee8-127">Opnið kort fyrir fyrirliggjandi færsla skjal á innleið.</span><span class="sxs-lookup"><span data-stu-id="d1ee8-127">Open the card for an existing incoming document record.</span></span>
3. <span data-ttu-id="d1ee8-128">Á síðunni **Skjal á innleið** skal velja úrfellingarmerkishnappinn og svo **Hengja við mynd úr myndavél**.</span><span class="sxs-lookup"><span data-stu-id="d1ee8-128">On the **Incoming Document** page, choose the ellipsis button, and then choose **Attach Image from Camera**.</span></span> <span data-ttu-id="d1ee8-129">Kveikt er á myndavél spjaldtölvu eða síma.</span><span class="sxs-lookup"><span data-stu-id="d1ee8-129">The camera on the tablet or phone is activated.</span></span>
4. <span data-ttu-id="d1ee8-130">Takið mynd af skjali, t.d. innkaupakvittun, sem á að vinna sem skjal á innleið, og veljið svo hnappur **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="d1ee8-130">Take a photo of a document, such as a purchase receipt, that you want to process as an incoming document, and then choose the **OK** button.</span></span>

    <span data-ttu-id="d1ee8-131">Myndin er hengja við færsla skjal á innleið.</span><span class="sxs-lookup"><span data-stu-id="d1ee8-131">The image is attached to the incoming document record.</span></span>

## <a name="to-create-an-incoming-document-record-manually"></a><span data-ttu-id="d1ee8-132">Tila ð búa til færslu skjals á innleið handvirkt</span><span class="sxs-lookup"><span data-stu-id="d1ee8-132">To create an incoming document record manually</span></span>
1. <span data-ttu-id="d1ee8-133">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Skjöl á innleið** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="d1ee8-133">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Incoming Documents**, and then choose the related link.</span></span>
2. <span data-ttu-id="d1ee8-134">Aðgerðin **Stofna úr Skrá** er valin.</span><span class="sxs-lookup"><span data-stu-id="d1ee8-134">Choose the **Create from File** action.</span></span>  
3. <span data-ttu-id="d1ee8-135">Á síðunni **Setja inn skrá** skal velja skrá og svo **Opna**.</span><span class="sxs-lookup"><span data-stu-id="d1ee8-135">On the **Insert File** page, select a file, and then choose **Open**.</span></span> <span data-ttu-id="d1ee8-136">Skráin er hengd við sjálfkrafa.</span><span class="sxs-lookup"><span data-stu-id="d1ee8-136">The file is automatically attached.</span></span>
4. <span data-ttu-id="d1ee8-137">Einnig er hægt að velja aðgerðina **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="d1ee8-137">Alternatively, choose the **New** action.</span></span>
5. <span data-ttu-id="d1ee8-138">Ef tengja á skrá, skal velja **Tengja Skrá** aðgerð.</span><span class="sxs-lookup"><span data-stu-id="d1ee8-138">To attach a file, choose the **Attach File** action.</span></span>
6. <span data-ttu-id="d1ee8-139">Á síðunni **Setja inn skrá** skal velja skrána sem táknar skjalið á innleið og svo hnappinn **Opna**.</span><span class="sxs-lookup"><span data-stu-id="d1ee8-139">On the **Insert File** page, select the file that represents the incoming document in question, and then choose the **Open** button.</span></span>
7. <span data-ttu-id="d1ee8-140">Á síðunni **Skjal á innleið** þarf að fylla reitina út eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="d1ee8-140">On the **Incoming Document** page, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="see-also"></a><span data-ttu-id="d1ee8-141">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="d1ee8-141">See Also</span></span>
[<span data-ttu-id="d1ee8-142">Vinnsla skjala á innleið</span><span class="sxs-lookup"><span data-stu-id="d1ee8-142">Process Incoming Documents</span></span>](across-process-income-documents.md)  
[<span data-ttu-id="d1ee8-143">Skjöl á innleið</span><span class="sxs-lookup"><span data-stu-id="d1ee8-143">Incoming Documents</span></span>](across-income-documents.md)  
[<span data-ttu-id="d1ee8-144">Innkaup</span><span class="sxs-lookup"><span data-stu-id="d1ee8-144">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="d1ee8-145">[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="d1ee8-145">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>
