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
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 0d13ffa03e4a123158e2f350ff9eab5e274741b5
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/17/2020
ms.locfileid: "4760568"
---
# <a name="manage-attachments-links-and-notes-on-cards-and-documents"></a><span data-ttu-id="0321f-103">Stjórna viðhengjum, tenglum og athugasemdum á spjöldum og fylgiskjölum</span><span class="sxs-lookup"><span data-stu-id="0321f-103">Manage Attachments, Links, and Notes on Cards and Documents</span></span>

<span data-ttu-id="0321f-104">Í upplýsingareitnum á flestum spjöldum og skjölum er hægt að hengja við skrár, bæta við tenglum og skrifa athugasemdir.</span><span class="sxs-lookup"><span data-stu-id="0321f-104">In the FactBox on most cards and documents, you can attach files, add links, and write notes.</span></span> <span data-ttu-id="0321f-105">Einnig er hægt að gera þetta á listasíðunni með því að velja tengda línu fyrir tengla og athugasemd.</span><span class="sxs-lookup"><span data-stu-id="0321f-105">For links and notes, you can also do this on the list page by first selecting the related line.</span></span>

<span data-ttu-id="0321f-106">Til að skoða eða breyta einhverjum þessara tengdu upplýsingargerða verður fyrst að opna flipann **Viðhengi** í upplýsingareitnum.</span><span class="sxs-lookup"><span data-stu-id="0321f-106">To view or change any of these attached information types, you must first open the **Attachments** tab in the FactBox.</span></span> <span data-ttu-id="0321f-107">Talan fyrir aftan dálktitilinn gefur til kynna hversu margar viðhengdar skrár, tenglar eða upplýsingar eru til staðar fyrir kortið eða skjalið.</span><span class="sxs-lookup"><span data-stu-id="0321f-107">The number behind the tab title indicates how many attached files, links, or notes exist for the card or document.</span></span>

<span data-ttu-id="0321f-108">Viðhengi, tenglar og athugasemdirnar eru hengd við sem spjaldið eða skjalið er unnið úr í öðrum stöðum, t.d. frá yfirstandandi sölupöntun á bókuðum sölureikningi.</span><span class="sxs-lookup"><span data-stu-id="0321f-108">Attachments, links, and notes stay attached as the card or document is processed into other states, such as from an ongoing sales order to a posted sales invoice.</span></span> <span data-ttu-id="0321f-109">Hins vegar eru engar viðhengisgerðirnar úttak úr kerfinu, til dæmis við prentun eða þegar verið er að vista í skrá.</span><span class="sxs-lookup"><span data-stu-id="0321f-109">However, none of the attachment types are output from the system, for example, when printing or when saving to a file.</span></span>

> [!NOTE]
> <span data-ttu-id="0321f-110">Þegar verið er að senda og reikningsfæra sölupöntun eða innkaupapöntun verður viðhengið aðeins hengt við endanlegan reikning þeirrar pöntunar.</span><span class="sxs-lookup"><span data-stu-id="0321f-110">When you partially ship and invoice a sales order or purchase order, the attachment will only be attached to the final invoice of that order.</span></span> <span data-ttu-id="0321f-111">Sömuleiðis, þegar verið er að reikningsfæra með frestunaraðgerðinni, tengist viðhengið aðeins fjárhagsfærslum skjalsins en ekki fyrir frestunarfærslur.</span><span class="sxs-lookup"><span data-stu-id="0321f-111">Likewise, when you invoice using the Deferrals feature, the attachment is only attached to the G/L entries for the document but not for the deferral entries.</span></span>

## <a name="to-attach-a-file-to-a-purchase-invoice"></a><span data-ttu-id="0321f-112">Til að hengja skrá við innkaupareikning</span><span class="sxs-lookup"><span data-stu-id="0321f-112">To attach a file to a purchase invoice</span></span>
<span data-ttu-id="0321f-113">Hægt er að tengja allar gerðir skráa, sem innihalda texta, mynd eða myndskeið við spjald eða skjal.</span><span class="sxs-lookup"><span data-stu-id="0321f-113">You can attach any type of file, containing text, image, or video, to a card or document.</span></span> <span data-ttu-id="0321f-114">Þetta er til dæmis gagnlegt þegar óskað er eftir að vista reikning lánardrottins sem PDF-skrá á tengdum innkaupareikningi í [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="0321f-114">This is useful, for example, when you want to store a vendor's invoice as a PDF file on the related purchase invoice in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>

> [!NOTE]
> <span data-ttu-id="0321f-115">Skrár sem eru hengdar við eiginleikann skjöl á innleið eru ekki teknar með á flipanum **Viðhengi**. Frekari upplýsingar er að finna í [Skjöl á innleið](across-income-documents.md).</span><span class="sxs-lookup"><span data-stu-id="0321f-115">Files attached with the Incoming Documents feature are not included on the **Attachments** tab. For more information, see [Incoming Documents](across-income-documents.md).</span></span>

<span data-ttu-id="0321f-116">Eftirfarandi ferli byggist á innkaupareikningur.</span><span class="sxs-lookup"><span data-stu-id="0321f-116">The following procedure is based on a purchase invoice.</span></span> <span data-ttu-id="0321f-117">Skrefin eru svipuð fyrir öll önnur studd skjöl og kort.</span><span class="sxs-lookup"><span data-stu-id="0321f-117">The steps are similar for all other supported documents and cards.</span></span>

1. <span data-ttu-id="0321f-118">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Innkaupareikningar** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="0321f-118">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Purchase Invoices**, and then choose the related link.</span></span>
2. <span data-ttu-id="0321f-119">Opnaðu sölupöntunina sem á að hengja skrá við.</span><span class="sxs-lookup"><span data-stu-id="0321f-119">Open the sales order that you want to attach a file to.</span></span>
3. <span data-ttu-id="0321f-120">Í upplýsingareitnum skal opna flipann **Viðhengi**.</span><span class="sxs-lookup"><span data-stu-id="0321f-120">In the FactBox, open the **Attachments** tab.</span></span>
4. <span data-ttu-id="0321f-121">Veljið gildið fyrir aftan reitinn **Skjöl**, eins og „0“.</span><span class="sxs-lookup"><span data-stu-id="0321f-121">Choose the value behind the **Documents** field, such as "0".</span></span>
5. <span data-ttu-id="0321f-122">Á síðunni **Skjöl í viðhengi** í reitnum **Viðhengi** skal velja hnappinn **Velja skrá**.</span><span class="sxs-lookup"><span data-stu-id="0321f-122">On the **Attached Documents** page, in the **Attachment** field, choose the **Select File** action.</span></span>
5. <span data-ttu-id="0321f-123">Veldu skrá frá hvaða staðsetningu sem er og veldu svo hnappinn **Opna**.</span><span class="sxs-lookup"><span data-stu-id="0321f-123">Select a file from any location, and then choose the **Open** button.</span></span>

<span data-ttu-id="0321f-124">Skráin er nú hengd við innkaupareikninginn.</span><span class="sxs-lookup"><span data-stu-id="0321f-124">The file is now attached to the purchase invoice.</span></span>

## <a name="to-view-an-attached-file"></a><span data-ttu-id="0321f-125">Til að skoða viðhengda skrá</span><span class="sxs-lookup"><span data-stu-id="0321f-125">To view an attached file</span></span>
1. <span data-ttu-id="0321f-126">Í upplýsingareitnum skal opna flipann **Viðhengi**.</span><span class="sxs-lookup"><span data-stu-id="0321f-126">In the FactBox, open the **Attachments** tab.</span></span>
2. <span data-ttu-id="0321f-127">Veljið gildið fyrir aftan reitinn **Skjöl**, eins og „1“.</span><span class="sxs-lookup"><span data-stu-id="0321f-127">Choose the value behind the **Documents** field, such as "1".</span></span>
3. <span data-ttu-id="0321f-128">Á síðunni **Viðhengd fylgiskjöl** skaltu velja aðgerðina **Forskoðun**.</span><span class="sxs-lookup"><span data-stu-id="0321f-128">On the **Attached Documents** page, choose the **Preview** action.</span></span>
4. <span data-ttu-id="0321f-129">Opnaðu skrána sem var hlaðið niður.</span><span class="sxs-lookup"><span data-stu-id="0321f-129">Open the downloaded file.</span></span>

## <a name="to-save-a-document-as-a-pdf-attachment"></a><span data-ttu-id="0321f-130">Vista skjal sem PDF-viðhengi</span><span class="sxs-lookup"><span data-stu-id="0321f-130">To save a document as a PDF attachment</span></span>
<span data-ttu-id="0321f-131">Í hvert sinn sem vista þarf skjal sem skrá er hægt að nota aðgerðina **Hengja við sem PDF** til að ná í núverandi innihald skjals sem PDF-skrá hengda við FactBox skjalsins.</span><span class="sxs-lookup"><span data-stu-id="0321f-131">Whenever you need to save a document as a file, you can use the **Attach as PDF** action to capture the current document content as a PDF file attached to the FactBox of the document.</span></span> <span data-ttu-id="0321f-132">Þetta er gagnlegt, til dæmis þegar skjöl fylgja mörgum skrefum í ferli, svo sem söluferli eða samþykktarverkflæði og ætlunin er að vísa til útprentunar af fyrra skrefi.</span><span class="sxs-lookup"><span data-stu-id="0321f-132">This is useful, for example, when documents follow multiple steps in a process, such as a sales process or an approval workflow, and you want to refer to a printout of the previous step.</span></span>

<span data-ttu-id="0321f-133">Eftirfarandi ferli byggist á sölupöntun.</span><span class="sxs-lookup"><span data-stu-id="0321f-133">The following procedure is based on a sales order.</span></span> <span data-ttu-id="0321f-134">Skrefin eru svipuð fyrir öll studd skjöl.</span><span class="sxs-lookup"><span data-stu-id="0321f-134">The steps are similar for all supported documents.</span></span>

1. <span data-ttu-id="0321f-135">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Sölupantanir** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="0321f-135">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Orders**, and then choose the related link.</span></span>
2. <span data-ttu-id="0321f-136">Veldu sölupöntun og veldu síðan aðgerðina **Hengja við sem PDF**.</span><span class="sxs-lookup"><span data-stu-id="0321f-136">Select a sales order, and then choose the **Attach as PDF** action.</span></span>

<span data-ttu-id="0321f-137">PDF-skrá með núverandi innihaldi sölupöntunarinnar er bætt við flipann **Viðhengi** í FactBox.</span><span class="sxs-lookup"><span data-stu-id="0321f-137">A PDF file with the current content of the sales order is added to the **Attachments** tab in the FactBox.</span></span>

## <a name="to-add-a-link-from-an-item-card"></a><span data-ttu-id="0321f-138">Til að bæta við tengli af birgðaspjaldi</span><span class="sxs-lookup"><span data-stu-id="0321f-138">To add a link from an item card</span></span>
<span data-ttu-id="0321f-139">Hægt er að bæta við tengli af korti eða skjali á einhverja vefslóð eða slóð.</span><span class="sxs-lookup"><span data-stu-id="0321f-139">You can add a link from a card or document to any URL or path.</span></span> <span data-ttu-id="0321f-140">Þetta er gagnlegt, til dæmis þegar tengja á birgðaspjald við vörulista birgis.</span><span class="sxs-lookup"><span data-stu-id="0321f-140">This is useful, for example, when you want to link an item card with the supplier's item catalog.</span></span>

<span data-ttu-id="0321f-141">Eftirfarandi aðferð er byggð á birgðaspjaldi.</span><span class="sxs-lookup"><span data-stu-id="0321f-141">The following procedure is based on an item card.</span></span> <span data-ttu-id="0321f-142">Skrefin eru svipuð fyrir öll önnur studd kort og skjöl.</span><span class="sxs-lookup"><span data-stu-id="0321f-142">The steps are similar for all other supported cards and documents.</span></span>

1. <span data-ttu-id="0321f-143">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Vara** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="0321f-143">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>
2. <span data-ttu-id="0321f-144">Veldu vöruna sem þú vilt bæta við tengli úr og veldu svo flipann **Viðhengi** í upplýsingareitnum.</span><span class="sxs-lookup"><span data-stu-id="0321f-144">Select the item that you want to add a link from, and then choose the **Attachments** tab in the FactBox.</span></span>
3. <span data-ttu-id="0321f-145">Í **Tenglar** skal velja **+** táknið.</span><span class="sxs-lookup"><span data-stu-id="0321f-145">In the **Links**, choose the **+** icon.</span></span>
4. <span data-ttu-id="0321f-146">Í svæðinu **Veffang tengils** skal slá inn tengilinn.</span><span class="sxs-lookup"><span data-stu-id="0321f-146">In the **Link Address** field, enter the link.</span></span>

    <span data-ttu-id="0321f-147">Tengillinn verður að vera gild vefslóð eða slóð innra nets.</span><span class="sxs-lookup"><span data-stu-id="0321f-147">The link must be a valid internet or intranet URL.</span></span>

5. <span data-ttu-id="0321f-148">Í reitinn **Lýsing** skal færa inn upplýsingar um tengilinn.</span><span class="sxs-lookup"><span data-stu-id="0321f-148">In the **Description** field, enter any information about the link.</span></span>  
6. <span data-ttu-id="0321f-149">Velja hnappinn **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="0321f-149">Choose the **OK** button.</span></span>

<span data-ttu-id="0321f-150">Tengillinn er nú tengdur við birgðaspjaldið.</span><span class="sxs-lookup"><span data-stu-id="0321f-150">The link is now attached to the item card.</span></span>  

## <a name="to-write-a-note-on-a-sales-order"></a><span data-ttu-id="0321f-151">Til að skrifa athugasemd á sölupöntun</span><span class="sxs-lookup"><span data-stu-id="0321f-151">To write a note on a sales order</span></span>
<span data-ttu-id="0321f-152">Hægt er að skrifa athugasemd á skjal eða kort, til dæmis til að skrifa sérstakar leiðbeiningar fyrir aðra notendur skjalsins eða kortsins.</span><span class="sxs-lookup"><span data-stu-id="0321f-152">You can write a note on a document or card, for example, to communicate special instructions to other users of the document or card.</span></span> <span data-ttu-id="0321f-153">Hægt er að hafa skráartengla og vefslóðir með í athugasemdum.</span><span class="sxs-lookup"><span data-stu-id="0321f-153">You can include file links and URLs in notes.</span></span>

> [!NOTE]
> <span data-ttu-id="0321f-154">Athugasemdirnar á flipanum **Viðhengi** eru ekki tengdar virkni innri athugasemda, sem eru aðallega notaðar til að eiga samskipti á milli notenda verkflæðis.</span><span class="sxs-lookup"><span data-stu-id="0321f-154">Notes on the **Attachments** tab are not related to internal notes functionality, which is mainly used to communicate between workflow users.</span></span> <span data-ttu-id="0321f-155">Nánari upplýsingar er að finna í [Uppsetning Verkflæði Tilkynningar](across-setting-up-workflow-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="0321f-155">For more information, see [Setting Up Workflow Notifications](across-setting-up-workflow-notifications.md).</span></span>

<span data-ttu-id="0321f-156">Eftirfarandi ferli byggist á sölupöntun.</span><span class="sxs-lookup"><span data-stu-id="0321f-156">The following procedure is based on a sales order.</span></span> <span data-ttu-id="0321f-157">Skrefin eru svipuð fyrir öll önnur studd skjöl og kort.</span><span class="sxs-lookup"><span data-stu-id="0321f-157">The steps are similar for all other supported documents and cards.</span></span>

1. <span data-ttu-id="0321f-158">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Sölupantanir** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="0321f-158">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Orders**, and then choose the related link.</span></span>
2. <span data-ttu-id="0321f-159">Veljið sölupöntunina sem á að afskrifa athugasemd við og veljið svo flipann **Viðhengi** í upplýsingareitnum.</span><span class="sxs-lookup"><span data-stu-id="0321f-159">Select the sales order that you want to write a note on, and then choose the **Attachments** tab in the FactBox.</span></span>
3. <span data-ttu-id="0321f-160">Í hlutanum **Athugasemdir** skal velja **+** táknið.</span><span class="sxs-lookup"><span data-stu-id="0321f-160">In the **Notes** section, choose the **+** icon.</span></span>
4. <span data-ttu-id="0321f-161">Í reitinn **Athugasemd** skal færa inn hvaða texta sem er, t.d. „Þetta er áríðandi pöntun“.</span><span class="sxs-lookup"><span data-stu-id="0321f-161">In the **Note** field, write any text, such as "This is an urgent order.".</span></span>
5. <span data-ttu-id="0321f-162">Velja hnappinn **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="0321f-162">Choose the **OK** button.</span></span>

<span data-ttu-id="0321f-163">Athugasemdin er nú hengd við sölupöntunina.</span><span class="sxs-lookup"><span data-stu-id="0321f-163">The note is now attached to the sales order.</span></span>

## <a name="see-also"></a><span data-ttu-id="0321f-164">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="0321f-164">See Also</span></span>  
<span data-ttu-id="0321f-165">[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="0321f-165">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="0321f-166">Skjöl á innleið</span><span class="sxs-lookup"><span data-stu-id="0321f-166">Incoming Documents</span></span>](across-income-documents.md)  
[<span data-ttu-id="0321f-167">Setja upp tilkynningar verkflæðis</span><span class="sxs-lookup"><span data-stu-id="0321f-167">Setting Up Workflow Notifications</span></span>](across-setting-up-workflow-notifications.md)  
