---
title: Bæta við viðhengjum, tenglum og athugasemdum á færslum | Microsoft Docs
description: Setja tengil í skjal eða vefsíðu á tiltekna skrá, s.s. viðskiptavin eða fylgiskjal.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 01/13/2020
ms.author: sgroespe
ms.openlocfilehash: 84d9c0768a457fd13a73b3d70d2b8c329098fe82
ms.sourcegitcommit: ead69ebe5b29927876a4fb23afb6c066f8854591
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/14/2020
ms.locfileid: "2953276"
---
# <a name="manage-attachments-links-and-notes-on-cards-and-documents"></a><span data-ttu-id="4ac60-103">Stjórna viðhengjum, tenglum og athugasemdum á spjöldum og fylgiskjölum</span><span class="sxs-lookup"><span data-stu-id="4ac60-103">Manage Attachments, Links, and Notes on Cards and Documents</span></span>

<span data-ttu-id="4ac60-104">Í upplýsingareitnum á flestum spjöldum og skjölum er hægt að hengja við skrár, bæta við tenglum og skrifa athugasemdir.</span><span class="sxs-lookup"><span data-stu-id="4ac60-104">In the FactBox on most cards and documents, you can attach files, add links, and write notes.</span></span> <span data-ttu-id="4ac60-105">Einnig er hægt að gera þetta á listasíðunni með því að velja tengda línu fyrir tengla og athugasemd.</span><span class="sxs-lookup"><span data-stu-id="4ac60-105">For links and notes, you can also do this on the list page by first selecting the related line.</span></span>

<span data-ttu-id="4ac60-106">Til að skoða eða breyta einhverjum þessara tengdu upplýsingargerða verður fyrst að opna flipann **Viðhengi** í upplýsingareitnum.</span><span class="sxs-lookup"><span data-stu-id="4ac60-106">To view or change any of these attached information types, you must first open the **Attachments** tab in the FactBox.</span></span> <span data-ttu-id="4ac60-107">Talan fyrir aftan dálktitilinn gefur til kynna hversu margar viðhengdar skrár, tenglar eða upplýsingar eru til staðar fyrir kortið eða skjalið.</span><span class="sxs-lookup"><span data-stu-id="4ac60-107">The number behind the tab title indicates how many attached files, links, or notes exist for the card or document.</span></span>

<span data-ttu-id="4ac60-108">Viðhengi, tenglar og athugasemdirnar eru hengd við sem spjaldið eða skjalið er unnið úr í öðrum stöðum, t.d. frá yfirstandandi sölupöntun á bókuðum sölureikningi.</span><span class="sxs-lookup"><span data-stu-id="4ac60-108">Attachments, links, and notes stay attached as the card or document is processed into other states, such as from an ongoing sales order to a posted sales invoice.</span></span> <span data-ttu-id="4ac60-109">Hins vegar eru engar viðhengisgerðirnar úttak úr kerfinu, til dæmis við prentun eða þegar verið er að vista í skrá.</span><span class="sxs-lookup"><span data-stu-id="4ac60-109">However, none of the attachment types are output from the system, for example, when printing or when saving to a file.</span></span>

> [!NOTE]
> <span data-ttu-id="4ac60-110">Þegar verið er að senda og reikningsfæra sölupöntun eða innkaupapöntun verður viðhengið aðeins hengt við endanlegan reikning þeirrar pöntunar.</span><span class="sxs-lookup"><span data-stu-id="4ac60-110">When you partially ship and invoice a sales order or purchase order, the attachment will only be attached to the final invoice of that order.</span></span> <span data-ttu-id="4ac60-111">Sömuleiðis, þegar verið er að reikningsfæra með frestunaraðgerðinni, tengist viðhengið aðeins fjárhagsfærslum skjalsins en ekki fyrir frestunarfærslur.</span><span class="sxs-lookup"><span data-stu-id="4ac60-111">Likewise, when you invoice using the Deferrals feature, the attachment is only attached to the G/L entries for the document but not for the deferral entries.</span></span>

## <a name="to-attach-a-file-to-a-purchase-invoice"></a><span data-ttu-id="4ac60-112">Til að hengja skrá við innkaupareikning</span><span class="sxs-lookup"><span data-stu-id="4ac60-112">To attach a file to a purchase invoice</span></span>
<span data-ttu-id="4ac60-113">Hægt er að tengja allar gerðir skráa, sem innihalda texta, mynd eða myndskeið við spjald eða skjal.</span><span class="sxs-lookup"><span data-stu-id="4ac60-113">You can attach any type of file, containing text, image, or video, to a card or document.</span></span> <span data-ttu-id="4ac60-114">Þetta er til dæmis gagnlegt þegar óskað er eftir að vista reikning lánardrottins sem PDF-skrá á tengdum innkaupareikningi í [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="4ac60-114">This is useful, for example, when you want to store a vendor's invoice as a PDF file on the related purchase invoice in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

> [!NOTE]
> <span data-ttu-id="4ac60-115">Skrár sem eru hengdar við eiginleikann skjöl á innleið eru ekki teknar með á flipanum **Viðhengi**. Frekari upplýsingar er að finna í [Skjöl á innleið](across-income-documents.md).</span><span class="sxs-lookup"><span data-stu-id="4ac60-115">Files attached with the Incoming Documents feature are not included on the **Attachments** tab. For more information, see [Incoming Documents](across-income-documents.md).</span></span>

<span data-ttu-id="4ac60-116">Eftirfarandi ferli byggist á sölupöntun.</span><span class="sxs-lookup"><span data-stu-id="4ac60-116">The following procedure is based on a sales order.</span></span> <span data-ttu-id="4ac60-117">Skrefin eru svipuð fyrir öll önnur studd skjöl og kort.</span><span class="sxs-lookup"><span data-stu-id="4ac60-117">The steps are similar for all other supported documents and cards.</span></span>

1. <span data-ttu-id="4ac60-118">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Innkaupareikningar** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="4ac60-118">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Purchase Invoices**, and then choose the related link.</span></span>
2. <span data-ttu-id="4ac60-119">Opnaðu sölupöntunina sem á að hengja skrá við.</span><span class="sxs-lookup"><span data-stu-id="4ac60-119">Open the sales order that you want to attach a file to.</span></span>
3. <span data-ttu-id="4ac60-120">Í upplýsingareitnum skal opna flipann **Viðhengi**.</span><span class="sxs-lookup"><span data-stu-id="4ac60-120">In the FactBox, open the **Attachments** tab.</span></span>
4. <span data-ttu-id="4ac60-121">Veljið gildið fyrir aftan reitinn **Skjöl**, eins og „0“.</span><span class="sxs-lookup"><span data-stu-id="4ac60-121">Choose the value behind the **Documents** field, such as "0".</span></span>
5. <span data-ttu-id="4ac60-122">Á síðunni **Skjöl í viðhengi** í reitnum **Viðhengi** skal velja hnappinn **Velja skrá**.</span><span class="sxs-lookup"><span data-stu-id="4ac60-122">On the **Attached Documents** page, in the **Attachment** field, choose the **Select File** button.</span></span>
5. <span data-ttu-id="4ac60-123">Veldu skrá frá hvaða staðsetningu sem er og veldu svo hnappinn **Opna**.</span><span class="sxs-lookup"><span data-stu-id="4ac60-123">Select a file from any location, and then choose the **Open** button.</span></span>

<span data-ttu-id="4ac60-124">Skráin er nú hengd við innkaupareikninginn.</span><span class="sxs-lookup"><span data-stu-id="4ac60-124">The file is now attached to the purchase invoice.</span></span>

## <a name="to-add-a-link-from-an-item-card"></a><span data-ttu-id="4ac60-125">Til að bæta við tengli af birgðaspjaldi</span><span class="sxs-lookup"><span data-stu-id="4ac60-125">To add a link from an item card</span></span>
<span data-ttu-id="4ac60-126">Hægt er að bæta við tengli af korti eða skjali á einhverja vefslóð eða slóð.</span><span class="sxs-lookup"><span data-stu-id="4ac60-126">You can add a link from a card or document to any URL or path.</span></span> <span data-ttu-id="4ac60-127">Þetta er gagnlegt, til dæmis þegar tengja á birgðaspjald við vörulista birgis.</span><span class="sxs-lookup"><span data-stu-id="4ac60-127">This is useful, for example, when you want to link an item card with the supplier's item catalog.</span></span>

<span data-ttu-id="4ac60-128">Eftirfarandi aðferð er byggð á birgðaspjaldi.</span><span class="sxs-lookup"><span data-stu-id="4ac60-128">The following procedure is based on an item card.</span></span> <span data-ttu-id="4ac60-129">Skrefin eru svipuð fyrir öll önnur studd kort og skjöl.</span><span class="sxs-lookup"><span data-stu-id="4ac60-129">The steps are similar for all other supported cards and documents.</span></span>

1. <span data-ttu-id="4ac60-130">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Vara** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="4ac60-130">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>
2. <span data-ttu-id="4ac60-131">Veldu vöruna sem þú vilt bæta við tengli úr og veldu svo flipann **Viðhengi** í upplýsingareitnum.</span><span class="sxs-lookup"><span data-stu-id="4ac60-131">Select the item that you want to add a link from, and then choose the **Attachments** tab in the FactBox.</span></span>
3. <span data-ttu-id="4ac60-132">Í **Tenglar** skal velja **+** táknið.</span><span class="sxs-lookup"><span data-stu-id="4ac60-132">In the **Links**, choose the **+** icon.</span></span>
4. <span data-ttu-id="4ac60-133">Í svæðinu **Veffang tengils** skal slá inn tengilinn.</span><span class="sxs-lookup"><span data-stu-id="4ac60-133">In the **Link Address** field, enter the link.</span></span>

    <span data-ttu-id="4ac60-134">Tengillinn verður að vera gild vefslóð eða slóð innra nets.</span><span class="sxs-lookup"><span data-stu-id="4ac60-134">The link must be a valid internet or intranet URL.</span></span>

5. <span data-ttu-id="4ac60-135">Í reitinn **Lýsing** skal færa inn upplýsingar um tengilinn.</span><span class="sxs-lookup"><span data-stu-id="4ac60-135">In the **Description** field, enter any information about the link.</span></span>  
6. <span data-ttu-id="4ac60-136">Velja hnappinn **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="4ac60-136">Choose the **OK** button.</span></span>

<span data-ttu-id="4ac60-137">Tengillinn er nú tengdur við birgðaspjaldið.</span><span class="sxs-lookup"><span data-stu-id="4ac60-137">The link is now attached to the item card.</span></span>  

## <a name="to-write-a-note-on-a-sales-order"></a><span data-ttu-id="4ac60-138">Til að skrifa athugasemd á sölupöntun</span><span class="sxs-lookup"><span data-stu-id="4ac60-138">To write a note on a sales order</span></span>
<span data-ttu-id="4ac60-139">Hægt er að skrifa athugasemd á skjal eða kort, til dæmis til að skrifa sérstakar leiðbeiningar fyrir aðra notendur skjalsins eða kortsins.</span><span class="sxs-lookup"><span data-stu-id="4ac60-139">You can write a note on a document or card, for example, to communicate special instructions to other users of the document or card.</span></span> <span data-ttu-id="4ac60-140">Hægt er að hafa skráartengla og vefslóðir með í athugasemdum.</span><span class="sxs-lookup"><span data-stu-id="4ac60-140">You can include file links and URLs in notes.</span></span>

> [!NOTE]
> <span data-ttu-id="4ac60-141">Athugasemdirnar á flipanum **Viðhengi** eru ekki tengdar virkni innri athugasemda, sem eru aðallega notaðar til að eiga samskipti á milli notenda verkflæðis.</span><span class="sxs-lookup"><span data-stu-id="4ac60-141">Notes on the **Attachments** tab are not related to internal notes functionality, which is mainly used to communicate between workflow users.</span></span> <span data-ttu-id="4ac60-142">Nánari upplýsingar er að finna í [Uppsetning Verkflæði Tilkynningar](across-setting-up-workflow-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="4ac60-142">For more information, see [Setting Up Workflow Notifications](across-setting-up-workflow-notifications.md).</span></span>

<span data-ttu-id="4ac60-143">Eftirfarandi ferli byggist á sölupöntun.</span><span class="sxs-lookup"><span data-stu-id="4ac60-143">The following procedure is based on a sales order.</span></span> <span data-ttu-id="4ac60-144">Skrefin eru svipuð fyrir öll önnur studd skjöl og kort.</span><span class="sxs-lookup"><span data-stu-id="4ac60-144">The steps are similar for all other supported documents and cards.</span></span>

1. <span data-ttu-id="4ac60-145">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Sölupantanir** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="4ac60-145">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Orders**, and then choose the related link.</span></span>
2. <span data-ttu-id="4ac60-146">Veljið sölupöntunina sem á að afskrifa athugasemd við og veljið svo flipann **Viðhengi** í upplýsingareitnum.</span><span class="sxs-lookup"><span data-stu-id="4ac60-146">Select the sales order that you want to write a note on, and then choose the **Attachments** tab in the FactBox.</span></span>
3. <span data-ttu-id="4ac60-147">Í hlutanum **Athugasemdir** skal velja **+** táknið.</span><span class="sxs-lookup"><span data-stu-id="4ac60-147">In the **Notes** section, choose the **+** icon.</span></span>
4. <span data-ttu-id="4ac60-148">Í reitinn **Athugasemd** skal færa inn hvaða texta sem er, t.d. „Þetta er áríðandi pöntun“.</span><span class="sxs-lookup"><span data-stu-id="4ac60-148">In the **Note** field, write any text, such as "This is an urgent order.".</span></span>
5. <span data-ttu-id="4ac60-149">Velja hnappinn **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="4ac60-149">Choose the **OK** button.</span></span>

<span data-ttu-id="4ac60-150">Athugasemdin er nú hengd við sölupöntunina.</span><span class="sxs-lookup"><span data-stu-id="4ac60-150">The note is now attached to the sales order.</span></span>

## <a name="see-also"></a><span data-ttu-id="4ac60-151">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="4ac60-151">See Also</span></span>  
<span data-ttu-id="4ac60-152">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="4ac60-152">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="4ac60-153">Skjöl á innleið</span><span class="sxs-lookup"><span data-stu-id="4ac60-153">Incoming Documents</span></span>](across-income-documents.md)  
[<span data-ttu-id="4ac60-154">Setja upp tilkynningar verkflæðis</span><span class="sxs-lookup"><span data-stu-id="4ac60-154">Setting Up Workflow Notifications</span></span>](across-setting-up-workflow-notifications.md)  
