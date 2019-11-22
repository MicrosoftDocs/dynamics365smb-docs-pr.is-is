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
ms.date: 10/21/2019
ms.author: sgroespe
ms.openlocfilehash: 88e6a04a8e4a992b6a5df3fee87104eba7b5510e
ms.sourcegitcommit: be1e2c49a8434d3f440d5a201508af9c3c8cc87f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/22/2019
ms.locfileid: "2649789"
---
# <a name="manage-attachments-links-and-notes-on-cards-and-documents"></a><span data-ttu-id="a4d75-103">Stjórna viðhengjum, tenglum og athugasemdum á spjöldum og fylgiskjölum</span><span class="sxs-lookup"><span data-stu-id="a4d75-103">Manage Attachments, Links, and Notes on Cards and Documents</span></span>

<span data-ttu-id="a4d75-104">Í upplýsingareitnum á flestum spjöldum og skjölum er hægt að hengja við skrár, bæta við tenglum og skrifa athugasemdir.</span><span class="sxs-lookup"><span data-stu-id="a4d75-104">In the FactBox on most cards and documents, you can attach files, add links, and write notes.</span></span> <span data-ttu-id="a4d75-105">Einnig er hægt að gera þetta á listasíðunni með því að velja tengda línu fyrir tengla og athugasemd.</span><span class="sxs-lookup"><span data-stu-id="a4d75-105">For links and notes, you can also do this on the list page by first selecting the related line.</span></span>

<span data-ttu-id="a4d75-106">Til að skoða eða breyta einhverjum þessara tengdu upplýsingargerða verður fyrst að opna flipann **Viðhengi** í upplýsingareitnum.</span><span class="sxs-lookup"><span data-stu-id="a4d75-106">To view or change any of these attached information types, you must first open the **Attachments** tab in the FactBox.</span></span> <span data-ttu-id="a4d75-107">Talan fyrir aftan dálktitilinn gefur til kynna hversu margar viðhengdar skrár, tenglar eða upplýsingar eru til staðar fyrir kortið eða skjalið.</span><span class="sxs-lookup"><span data-stu-id="a4d75-107">The number behind the tab title indicates how many attached files, links, or notes exist for the card or document.</span></span>

<span data-ttu-id="a4d75-108">Viðhengi, tenglar og athugasemdirnar eru hengd við sem spjaldið eða skjalið er unnið úr í öðrum stöðum, t.d. frá yfirstandandi sölupöntun á bókuðum sölureikningi.</span><span class="sxs-lookup"><span data-stu-id="a4d75-108">Attachments, links, and notes stay attached as the card or document is processed into other states, such as from an ongoing sales order to a posted sales invoice.</span></span> <span data-ttu-id="a4d75-109">Athugið hins vegar að engin af viðhengisgerðunum er úttak úr kerfinu, til dæmis við prentun eða þegar verið er að vista í skrá.</span><span class="sxs-lookup"><span data-stu-id="a4d75-109">Note, however, that none of the attachment types are output from the system, for example, when printing or when saving to a file.</span></span>

## <a name="to-attach-a-file-to-a-purchase-invoice"></a><span data-ttu-id="a4d75-110">Til að hengja skrá við innkaupareikning</span><span class="sxs-lookup"><span data-stu-id="a4d75-110">To attach a file to a purchase invoice</span></span>
<span data-ttu-id="a4d75-111">Hægt er að tengja allar gerðir skráa, sem innihalda texta, mynd eða myndskeið við spjald eða skjal.</span><span class="sxs-lookup"><span data-stu-id="a4d75-111">You can attach any type of file, containing text, image, or video, to a card or document.</span></span> <span data-ttu-id="a4d75-112">Þetta er til dæmis gagnlegt þegar óskað er eftir að vista reikning lánardrottins sem PDF-skrá á tengdum innkaupareikningi í [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="a4d75-112">This is useful, for example, when you want to store a vendor's invoice as a PDF file on the related purchase invoice in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

> [!NOTE]
> <span data-ttu-id="a4d75-113">Skrár sem eru hengdar við eiginleikann skjöl á innleið eru ekki teknar með á flipanum **Viðhengi**. Frekari upplýsingar er að finna í [Skjöl á innleið](across-income-documents.md).</span><span class="sxs-lookup"><span data-stu-id="a4d75-113">Files attached with the Incoming Documents feature are not included on the **Attachments** tab. For more information, see [Incoming Documents](across-income-documents.md).</span></span>

<span data-ttu-id="a4d75-114">Eftirfarandi ferli byggist á sölupöntun.</span><span class="sxs-lookup"><span data-stu-id="a4d75-114">The following procedure is based on a sales order.</span></span> <span data-ttu-id="a4d75-115">Skrefin eru svipuð fyrir öll önnur studd skjöl og kort.</span><span class="sxs-lookup"><span data-stu-id="a4d75-115">The steps are similar for all other supported documents and cards.</span></span>

1. <span data-ttu-id="a4d75-116">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Innkaupareikningar** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="a4d75-116">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Purchase Invoices**, and then choose the related link.</span></span>
2. <span data-ttu-id="a4d75-117">Opnaðu sölupöntunina sem á að hengja skrá við.</span><span class="sxs-lookup"><span data-stu-id="a4d75-117">Open the sales order that you want to attach a file to.</span></span>
3. <span data-ttu-id="a4d75-118">Í upplýsingareitnum skal opna flipann **Viðhengi**.</span><span class="sxs-lookup"><span data-stu-id="a4d75-118">In the FactBox, open the **Attachments** tab.</span></span>
4. <span data-ttu-id="a4d75-119">Veljið gildið fyrir aftan reitinn **Skjöl**, eins og „0“.</span><span class="sxs-lookup"><span data-stu-id="a4d75-119">Choose the value behind the **Documents** field, such as "0".</span></span>
5. <span data-ttu-id="a4d75-120">Á síðunni **Skjöl í viðhengi** í reitnum **Viðhengi** skal velja hnappinn **Velja skrá**.</span><span class="sxs-lookup"><span data-stu-id="a4d75-120">On the **Attached Documents** page, in the **Attachment** field, choose the **Select File** button.</span></span>
5. <span data-ttu-id="a4d75-121">Veldu skrá frá hvaða staðsetningu sem er og veldu svo hnappinn **Opna**.</span><span class="sxs-lookup"><span data-stu-id="a4d75-121">Select a file from any location, and then choose the **Open** button.</span></span>

<span data-ttu-id="a4d75-122">Skráin er nú hengd við innkaupareikninginn.</span><span class="sxs-lookup"><span data-stu-id="a4d75-122">The file is now attached to the purchase invoice.</span></span>

## <a name="to-add-a-link-from-an-item-card"></a><span data-ttu-id="a4d75-123">Til að bæta við tengli af birgðaspjaldi</span><span class="sxs-lookup"><span data-stu-id="a4d75-123">To add a link from an item card</span></span>
<span data-ttu-id="a4d75-124">Hægt er að bæta við tengli af korti eða skjali á einhverja vefslóð eða slóð.</span><span class="sxs-lookup"><span data-stu-id="a4d75-124">You can add a link from a card or document to any URL or path.</span></span> <span data-ttu-id="a4d75-125">Þetta er gagnlegt, til dæmis þegar tengja á birgðaspjald við vörulista birgis.</span><span class="sxs-lookup"><span data-stu-id="a4d75-125">This is useful, for example, when you want to link an item card with the supplier's item catalog.</span></span>

<span data-ttu-id="a4d75-126">Eftirfarandi aðferð er byggð á birgðaspjaldi.</span><span class="sxs-lookup"><span data-stu-id="a4d75-126">The following procedure is based on an item card.</span></span> <span data-ttu-id="a4d75-127">Skrefin eru svipuð fyrir öll önnur studd kort og skjöl.</span><span class="sxs-lookup"><span data-stu-id="a4d75-127">The steps are similar for all other supported cards and documents.</span></span>

1. <span data-ttu-id="a4d75-128">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Vara** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="a4d75-128">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>
2. <span data-ttu-id="a4d75-129">Veldu vöruna sem þú vilt bæta við tengli úr og veldu svo flipann **Viðhengi** í upplýsingareitnum.</span><span class="sxs-lookup"><span data-stu-id="a4d75-129">Select the item that you want to add a link from, and then choose the **Attachments** tab in the FactBox.</span></span>
3. <span data-ttu-id="a4d75-130">Í **Tenglar** skal velja **+** táknið.</span><span class="sxs-lookup"><span data-stu-id="a4d75-130">In the **Links**, choose the **+** icon.</span></span>
4. <span data-ttu-id="a4d75-131">Í svæðinu **Veffang tengils** skal slá inn tengilinn.</span><span class="sxs-lookup"><span data-stu-id="a4d75-131">In the **Link Address** field, enter the link.</span></span>

    <span data-ttu-id="a4d75-132">Tengillinn verður að vera gild vefslóð eða slóð innra nets.</span><span class="sxs-lookup"><span data-stu-id="a4d75-132">The link must be a valid internet or intranet URL.</span></span>

5. <span data-ttu-id="a4d75-133">Í reitinn **Lýsing** skal færa inn upplýsingar um tengilinn.</span><span class="sxs-lookup"><span data-stu-id="a4d75-133">In the **Description** field, enter any information about the link.</span></span>  
6. <span data-ttu-id="a4d75-134">Velja hnappinn **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="a4d75-134">Choose the **OK** button.</span></span>

<span data-ttu-id="a4d75-135">Tengillinn er nú tengdur við birgðaspjaldið.</span><span class="sxs-lookup"><span data-stu-id="a4d75-135">The link is now attached to the item card.</span></span>  

## <a name="to-write-a-note-on-a-sales-order"></a><span data-ttu-id="a4d75-136">Til að skrifa athugasemd á sölupöntun</span><span class="sxs-lookup"><span data-stu-id="a4d75-136">To write a note on a sales order</span></span>
<span data-ttu-id="a4d75-137">Hægt er að skrifa athugasemd á skjal eða kort, til dæmis til að skrifa sérstakar leiðbeiningar fyrir aðra notendur skjalsins eða kortsins.</span><span class="sxs-lookup"><span data-stu-id="a4d75-137">You can write a note on a document or card, for example, to communicate special instructions to other users of the document or card.</span></span> <span data-ttu-id="a4d75-138">Hægt er að hafa skráartengla og vefslóðir með í athugasemdum.</span><span class="sxs-lookup"><span data-stu-id="a4d75-138">You can include file links and URLs in notes.</span></span>

> [!NOTE]
> <span data-ttu-id="a4d75-139">Athugasemdirnar á flipanum **Viðhengi** eru ekki tengdar virkni innri athugasemda, sem eru aðallega notaðar til að eiga samskipti á milli notenda verkflæðis.</span><span class="sxs-lookup"><span data-stu-id="a4d75-139">Notes on the **Attachments** tab are not related to internal notes functionality, which is mainly used to communicate between workflow users.</span></span> <span data-ttu-id="a4d75-140">Nánari upplýsingar er að finna í [Uppsetning Verkflæði Tilkynningar](across-setting-up-workflow-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="a4d75-140">For more information, see [Setting Up Workflow Notifications](across-setting-up-workflow-notifications.md).</span></span>

<span data-ttu-id="a4d75-141">Eftirfarandi ferli byggist á sölupöntun.</span><span class="sxs-lookup"><span data-stu-id="a4d75-141">The following procedure is based on a sales order.</span></span> <span data-ttu-id="a4d75-142">Skrefin eru svipuð fyrir öll önnur studd skjöl og kort.</span><span class="sxs-lookup"><span data-stu-id="a4d75-142">The steps are similar for all other supported documents and cards.</span></span>

1. <span data-ttu-id="a4d75-143">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Sölupantanir** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="a4d75-143">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Orders**, and then choose the related link.</span></span>
2. <span data-ttu-id="a4d75-144">Veljið sölupöntunina sem á að afskrifa athugasemd við og veljið svo flipann **Viðhengi** í upplýsingareitnum.</span><span class="sxs-lookup"><span data-stu-id="a4d75-144">Select the sales order that you want to write a note on, and then choose the **Attachments** tab in the FactBox.</span></span>
3. <span data-ttu-id="a4d75-145">Í hlutanum **Athugasemdir** skal velja **+** táknið.</span><span class="sxs-lookup"><span data-stu-id="a4d75-145">In the **Notes** section, choose the **+** icon.</span></span>
4. <span data-ttu-id="a4d75-146">Í reitinn **Athugasemd** skal færa inn hvaða texta sem er, t.d. „Þetta er áríðandi pöntun“.</span><span class="sxs-lookup"><span data-stu-id="a4d75-146">In the **Note** field, write any text, such as "This is an urgent order.".</span></span>
5. <span data-ttu-id="a4d75-147">Velja hnappinn **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="a4d75-147">Choose the **OK** button.</span></span>

<span data-ttu-id="a4d75-148">Athugasemdin er nú hengd við sölupöntunina.</span><span class="sxs-lookup"><span data-stu-id="a4d75-148">The note is now attached to the sales order.</span></span>

## <a name="see-also"></a><span data-ttu-id="a4d75-149">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="a4d75-149">See Also</span></span>  
<span data-ttu-id="a4d75-150">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="a4d75-150">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="a4d75-151">Skjöl á innleið</span><span class="sxs-lookup"><span data-stu-id="a4d75-151">Incoming Documents</span></span>](across-income-documents.md)  
[<span data-ttu-id="a4d75-152">Setja upp tilkynningar verkflæðis</span><span class="sxs-lookup"><span data-stu-id="a4d75-152">Setting Up Workflow Notifications</span></span>](across-setting-up-workflow-notifications.md)  
