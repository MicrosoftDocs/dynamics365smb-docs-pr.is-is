---
title: "Afturkalla bókun með bókun bakfærslu| Microsoft Docs"
description: "Ef þú hefur framkvæmt ranga bókun í færslubók, geturðu notað bakfærsluaðgerðina til að afturkalla bókunina með réttri endurskoðunarslóð."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reimbursement
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: beed335b93ef9211e4fc53c25f97b3fed6137348
ms.contentlocale: is-is
ms.lasthandoff: 09/28/2018

---
# <a name="reverse-postings"></a><span data-ttu-id="a897a-103">Bakfæra bókanir</span><span class="sxs-lookup"><span data-stu-id="a897a-103">Reverse Postings</span></span>
<span data-ttu-id="a897a-104">Til að afturkalla ranga bókun færslubókar skal velja færsluna og búa til bakfærslu (færsla sem er alveg eins og upphaflega færslan en með andstæðu tákni í reitnum fyrir upphæð) með sama skjalanúmeri og bókunardagsetningu og upphaflega færslan.</span><span class="sxs-lookup"><span data-stu-id="a897a-104">To undo an erroneous journal posting, you select the entry and create a reverse entry (entries identical to the original entry but with opposite sign in the amount field) with the same document number and posting date as the original entry.</span></span> <span data-ttu-id="a897a-105">Þegar færsla hefur verið bakfærð þarf að búa til rétta færslu.</span><span class="sxs-lookup"><span data-stu-id="a897a-105">After reversing an entry, you must make the correct entry.</span></span>

<span data-ttu-id="a897a-106">Aðeins er hægt að bakfæra færslu sem er bókuð frá færslubókarlínu.</span><span class="sxs-lookup"><span data-stu-id="a897a-106">You can only reverse entries that are posted from a general journal line.</span></span> <span data-ttu-id="a897a-107">Færslu er einungis hægt að bakfæra einu sinni.</span><span class="sxs-lookup"><span data-stu-id="a897a-107">An entry can only be reversed once.</span></span>

<span data-ttu-id="a897a-108">Frekari upplýsingar um bókun frá færslubók, sjá [Bóka færslur beint í fjárhag](finance-how-post-transactions-directly.md).</span><span class="sxs-lookup"><span data-stu-id="a897a-108">For more information about posting from a general journal, see [Post Transactions Directly to the General Ledger](finance-how-post-transactions-directly.md).</span></span>

<span data-ttu-id="a897a-109">Ef magn hefur verið ranglega neikvætt bókað, t.d. ef innkaupapöntun hefur verið gerð með röngum stykkjafjölda og síðan bókað sem móttekið en ekki reikningsfært, er hægt að ógilda bókunina.</span><span class="sxs-lookup"><span data-stu-id="a897a-109">If you have made an incorrect negative quantity posting, such as a purchase order with the wrong number of items and posted it as received but not invoiced, then you can undo the posting.</span></span>

<span data-ttu-id="a897a-110">Ef magn hefur verið ranglega jákvætt bókað, t.d. ef innkaupaskilapöntun hefur verið gerð með röngum stykkjafjölda og síðan bókað sem afgreitt en ekki reikningsfært, er hægt að ógilda bókunina.</span><span class="sxs-lookup"><span data-stu-id="a897a-110">If you have made an incorrect positive quantity posting, such as a purchase return order with the wrong number of items and posted it as shipped but not invoiced, then you can undo the posting.</span></span>   

## <a name="to-reverse-the-journal-posting-of-a-general-ledger-entry"></a><span data-ttu-id="a897a-111">Að bakfæra færslubókarbókun fjárhagsfærslu</span><span class="sxs-lookup"><span data-stu-id="a897a-111">To reverse the journal posting of a general ledger entry</span></span>
<span data-ttu-id="a897a-112">Hægt er að bakfæra færslur úr öllum **Fjárhagsfærslur** gluggum.</span><span class="sxs-lookup"><span data-stu-id="a897a-112">You can reverse entries from all **Ledger Entries** windows.</span></span> <span data-ttu-id="a897a-113">Eftirfarandi ferli er staðsett í **Fjárhagsfærslur** glugganum.</span><span class="sxs-lookup"><span data-stu-id="a897a-113">The following procedure is based in the **General Ledger Entries** window.</span></span>
1. <span data-ttu-id="a897a-114">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **fjárhagsfærslur** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="a897a-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **General Ledger Entries**, and then choose the related link.</span></span>
2. <span data-ttu-id="a897a-115">Veljið færsluna sem á að bakfæra og veljið síðna aðgerðina **Bakfæra færslu**.</span><span class="sxs-lookup"><span data-stu-id="a897a-115">Select the entry that you want to reverse, and then choose the **Reverse Transaction** action.</span></span> <span data-ttu-id="a897a-116">Athugið að þetta verður að koma úr bókun færslubókar.</span><span class="sxs-lookup"><span data-stu-id="a897a-116">Note that is must originate from a journal posting.</span></span>
3. <span data-ttu-id="a897a-117">Í glugganum **Bakfærðar viðskiptafærslur** skal velja viðeigandi línu og svo aðgerðina **Bakfæra**.</span><span class="sxs-lookup"><span data-stu-id="a897a-117">In the **Reverse Transaction Entries** window, select the relevant entry, and then choose the **Reverse** action.</span></span>
4. <span data-ttu-id="a897a-118">Velja hnappinn **Já** á staðfestingarskilaboðunum.</span><span class="sxs-lookup"><span data-stu-id="a897a-118">Choose the **Yes** button on the confirmation message.</span></span>

## <a name="to-undo-a-quantity-posting-on-a-posted-purchase-receipt"></a><span data-ttu-id="a897a-119">Að afturkalla magnbókun í bókuðum innkaupamóttökum</span><span class="sxs-lookup"><span data-stu-id="a897a-119">To undo a quantity posting on a posted purchase receipt</span></span>  

1.  <span data-ttu-id="a897a-120">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **bókaðar innkaupakvittanir** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="a897a-120">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Posted Purchase Receipts**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="a897a-121">Opna bókuðu móttökuna sem á að afturkalla.</span><span class="sxs-lookup"><span data-stu-id="a897a-121">Open the posted receipt that you want to undo.</span></span>  
3.  <span data-ttu-id="a897a-122">Velja skal línuna eða línurnar sem þú vilt afturkalla.</span><span class="sxs-lookup"><span data-stu-id="a897a-122">Select the line or lines that you want to undo.</span></span>  
4.  <span data-ttu-id="a897a-123">Veldu **Afturkalla móttöku** aðgerðina.</span><span class="sxs-lookup"><span data-stu-id="a897a-123">Choose **Undo Receipt** action.</span></span>

    <span data-ttu-id="a897a-124">Leiðréttingarlína er sett inn undir völdu móttökulínuna.</span><span class="sxs-lookup"><span data-stu-id="a897a-124">A corrective line is inserted under the selected receipt line.</span></span>  

    <span data-ttu-id="a897a-125">Ef magnið móttekið í vöruhúsamóttöku er leiðréttingarlínan sett inn í bókuðu vöruhúsamóttökuna.</span><span class="sxs-lookup"><span data-stu-id="a897a-125">If the quantity was received in a warehouse receipt, then a corrective line is inserted in the posted warehouse receipt.</span></span>  

    <span data-ttu-id="a897a-126">Reitirnir **Móttekið magn** og **Móttekið magn, óreikningsfært** svæði í tengdri innkaupapöntun eru stilltir á núll.</span><span class="sxs-lookup"><span data-stu-id="a897a-126">The **Quantity Received** and **Qty. Rcd. Not Invoiced** fields on the related purchase order are set to zero.</span></span>

## <a name="to-undo-and-then-redo-a-quantity-posting-on-a-posted-return-shipment"></a><span data-ttu-id="a897a-127">Hvernig skal afturkalla og endurgera magnbókun á bókaða skilaafhendingu.</span><span class="sxs-lookup"><span data-stu-id="a897a-127">To undo and then redo a quantity posting on a posted return shipment</span></span>

1.  <span data-ttu-id="a897a-128">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Bókaðar skilaafhendingar** og veldu síðan tengda hlekkinn.</span><span class="sxs-lookup"><span data-stu-id="a897a-128">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Posted Return Shipments**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="a897a-129">Opna bókuðu skilaafhendinguna sem á að afturkalla.</span><span class="sxs-lookup"><span data-stu-id="a897a-129">Open the posted return shipment that you want to undo.</span></span>
3. <span data-ttu-id="a897a-130">Velja skal línuna eða línurnar sem þú vilt afturkalla.</span><span class="sxs-lookup"><span data-stu-id="a897a-130">Select the line or lines you want to undo.</span></span>  

4.  <span data-ttu-id="a897a-131">Velja skal aðgerðina **Afturkalla vöruskilaafhendingu**.</span><span class="sxs-lookup"><span data-stu-id="a897a-131">Choose the **Undo Return Shipment** action.</span></span>  

    <span data-ttu-id="a897a-132">Leiðréttingarlína er sett í bókaða fylgiskjalið og reitirnir **Skilamagn afhent** og **Skilaupph. afhent óreikningsf.** í innkaupabeiðninni eru settir á núll.</span><span class="sxs-lookup"><span data-stu-id="a897a-132">A corrective line is inserted in the posted document, and the **Return Qty. Shipped** and **Return Shpd. Not Invd.** fields on the return order are set to zero.</span></span>  

    <span data-ttu-id="a897a-133">Farið nú aftur í innkaupaskilapöntunina til að endurtaka bókunina.</span><span class="sxs-lookup"><span data-stu-id="a897a-133">Now go back to the purchase return order to redo the posting.</span></span>  

5.  <span data-ttu-id="a897a-134">Í glugganum **Bókuð skilaafhending** takið mið af tölunni á svæðinu **Skilapöntun nr**.</span><span class="sxs-lookup"><span data-stu-id="a897a-134">In the **Posted Return Shipment** window, take a note of the number in the **Return Order No.**</span></span> <span data-ttu-id="a897a-135">.</span><span class="sxs-lookup"><span data-stu-id="a897a-135">field.</span></span>  
6.  <span data-ttu-id="a897a-136">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Vöruskilapöntun innkaupa** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="a897a-136">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Purchase Return Orders**, and then select the related link.</span></span>  
7.  <span data-ttu-id="a897a-137">Opna skilapöntunina sem um ræðir og velja síðan **Enduropna** aðgerðina.</span><span class="sxs-lookup"><span data-stu-id="a897a-137">Open the return order in question, and then choose the **Reopen** action.</span></span>  
8.  <span data-ttu-id="a897a-138">Leiðrétta færsluna í **Magn** reitnum og bóka skilapöntun innkaupa aftur.</span><span class="sxs-lookup"><span data-stu-id="a897a-138">Correct the entry in the **Quantity** field and post the purchase return order again.</span></span>  

## <a name="to-post-a-negative-entry"></a><span data-ttu-id="a897a-139">Að bóka neikvæða færslu</span><span class="sxs-lookup"><span data-stu-id="a897a-139">To post a negative entry</span></span>  
<span data-ttu-id="a897a-140">Hægt er að nota reitinn **Leiðrétting** til að bóka neikvæða debetfærslu í stað kreditfærslu, eða til að bóka neikvæða kreditfærslu í stað debetfærslu á reikningi.</span><span class="sxs-lookup"><span data-stu-id="a897a-140">You can use the **Correction** field to post a negative debit instead of a credit, or to post a negative credit instead of a debit on an account.</span></span> <span data-ttu-id="a897a-141">Til að uppfylla lagaskilyrði er þetta svæði sýnilegt að sjálfgefnu í öllum færslubókum.</span><span class="sxs-lookup"><span data-stu-id="a897a-141">To meet legal requirements, this field is visible by default in all journals.</span></span> <span data-ttu-id="a897a-142">Reitirnir **Debetupphæð** og **Kreditupphæð** innihalda bæði upphaflegu færsluna og leiðréttu færsluna.</span><span class="sxs-lookup"><span data-stu-id="a897a-142">The **Debit Amount** and **Credit Amount** fields include both the original entry, and the corrected entry.</span></span> <span data-ttu-id="a897a-143">Þessir reitir hafa engin áhrif á reikningsstöðuna.</span><span class="sxs-lookup"><span data-stu-id="a897a-143">These fields have no effect on the account balance.</span></span>  

1.  <span data-ttu-id="a897a-144">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **færslubækur** og veldu síðan tengda tengilinn</span><span class="sxs-lookup"><span data-stu-id="a897a-144">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **General Journals**, and then choose the related link</span></span>  
2.  <span data-ttu-id="a897a-145">Í reitnum **Heiti keyrslu** skal velja viðeigandi heiti keyrslu.</span><span class="sxs-lookup"><span data-stu-id="a897a-145">In the **Batch Name** field, select the required batch name.</span></span>  
3.  <span data-ttu-id="a897a-146">Færið inn upplýsingar í viðkomandi reiti.</span><span class="sxs-lookup"><span data-stu-id="a897a-146">Enter information into the relevant fields.</span></span>  
4.  <span data-ttu-id="a897a-147">Í færslubókarlínu sem á að virkja fyrir neikvæðar færslur skal velja gátreitinn **Leiðrétting**.</span><span class="sxs-lookup"><span data-stu-id="a897a-147">In the journal line that you want to activate for negative entries, select the **Correction** check box.</span></span>  
5.  <span data-ttu-id="a897a-148">Til að bóka færslubókina skal velja aðgerðina **Bóka** og síðan smella á hnappinn **Já**.</span><span class="sxs-lookup"><span data-stu-id="a897a-148">To post the journal, choose the **Post** action, and then choose the **Yes** button.</span></span>

## <a name="see-also"></a><span data-ttu-id="a897a-149">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="a897a-149">See Also</span></span>
[<span data-ttu-id="a897a-150">Bóka færslu beint í Fjárhag</span><span class="sxs-lookup"><span data-stu-id="a897a-150">Post Transactions Directly to the General Ledger</span></span>](finance-how-post-transactions-directly.md)  
[<span data-ttu-id="a897a-151">Vinna í færslubókum</span><span class="sxs-lookup"><span data-stu-id="a897a-151">Working with General Journals</span></span>](ui-work-general-journals.md)  
[<span data-ttu-id="a897a-152">Fjármál</span><span class="sxs-lookup"><span data-stu-id="a897a-152">Finance</span></span>](finance.md)  
<span data-ttu-id="a897a-153">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="a897a-153">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

