---
title: Söluskjöl bókuð
description: Kynntu þér mismunandi bókunaraðferðir til að bóka söluskjöl og hvernig hægt er að uppfæra bókuð skjöl.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.reviewer: edupont
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: e59c48c31e897d235c7920f4231313a2332fdf06
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5783260"
---
# <a name="posting-sales"></a><span data-ttu-id="0e365-103">Sölubókun</span><span class="sxs-lookup"><span data-stu-id="0e365-103">Posting Sales</span></span>

<span data-ttu-id="0e365-104">Undir valmyndinni **Bókun** í söluskjali er hægt að velja milli eftirfarandi bókunaraðgerða:</span><span class="sxs-lookup"><span data-stu-id="0e365-104">Under the **Posting** menu in a sales document, you can choose between the following posting functions:</span></span>

* <span data-ttu-id="0e365-105">**Færsla**</span><span class="sxs-lookup"><span data-stu-id="0e365-105">**Post**</span></span>
* <span data-ttu-id="0e365-106">**Bóka og nýtt**</span><span class="sxs-lookup"><span data-stu-id="0e365-106">**Post and New**</span></span>
* <span data-ttu-id="0e365-107">**Bóka og senda**</span><span class="sxs-lookup"><span data-stu-id="0e365-107">**Post and Send**</span></span>
* <span data-ttu-id="0e365-108">**Forskoðun bókunar**</span><span class="sxs-lookup"><span data-stu-id="0e365-108">**Preview Posting**</span></span>
* <span data-ttu-id="0e365-109">**Bóka runu**</span><span class="sxs-lookup"><span data-stu-id="0e365-109">**Post Batch**</span></span>
* <span data-ttu-id="0e365-110">**Prófunarskýrsla**</span><span class="sxs-lookup"><span data-stu-id="0e365-110">**Test Report**</span></span>

> [!NOTE]
> <span data-ttu-id="0e365-111">Fyrir sölupantanir er hægt að sjá valmöguleika sem tengjast fyrirframgreiðsluvirkni.</span><span class="sxs-lookup"><span data-stu-id="0e365-111">For sales orders, you can also see options related to the prepayments functionality.</span></span> <span data-ttu-id="0e365-112">Frekari upplýsingar er að finna í [Reikningsfærsla fyrirframgreiðslna](finance-invoice-prepayments.md).</span><span class="sxs-lookup"><span data-stu-id="0e365-112">For more information, see [Invoicing Prepayments](finance-invoice-prepayments.md).</span></span>

<span data-ttu-id="0e365-113">Þegar lokið hefur verið við allar línurnar og allar upplýsingar færðar á sölupöntunina er hægt að bóka hana.</span><span class="sxs-lookup"><span data-stu-id="0e365-113">When you have completed all the lines and entered all the information on the sales order, you can post it.</span></span> <span data-ttu-id="0e365-114">Þetta stofnar afhendingu og reikning.</span><span class="sxs-lookup"><span data-stu-id="0e365-114">This creates a shipment and an invoice.</span></span>

<span data-ttu-id="0e365-115">Þegar sölupöntun er bókuð, eru reikningur viðskiptavinar, fjárhagurinn og birgðahöfuðbókarfærslur uppfærðar.</span><span class="sxs-lookup"><span data-stu-id="0e365-115">When a sales order is posted, the customer's account, the general ledger, and the item ledger entries are updated.</span></span>

<span data-ttu-id="0e365-116">Sölufærsla er stofnuð í töflunni G/L Entry **fjárhagsfærsla** fyrir hverja sölupöntun.</span><span class="sxs-lookup"><span data-stu-id="0e365-116">For each sales order, a sales entry is created in the **G/L Entry** table.</span></span> <span data-ttu-id="0e365-117">Færsla er einnig stofnuð í reikningi viðskiptamanns í töflunni **sérsniðin fjárhagsfærsla** og fjárhagsfærsla er stofnuð í viðeigandi safnreikningi viðskiptamanns.</span><span class="sxs-lookup"><span data-stu-id="0e365-117">An entry is also created in the customer's account in the **Cust. Ledger Entry** table and a general ledger entry is created in the relevant receivables account.</span></span> <span data-ttu-id="0e365-118">Auk þess getur bókun pöntunarinnar leitt til VSK-færslu og fjárhagsfærslu vegna afsláttar.</span><span class="sxs-lookup"><span data-stu-id="0e365-118">In addition, posting the order may result in a VAT entry and a general ledger entry for the discount amount.</span></span> <span data-ttu-id="0e365-119">Hvort færsla vegna afsláttar er bókuð fer eftir því sem er í reitnum **Afsláttarbókun** á síðunni **Sölugrunnur**.</span><span class="sxs-lookup"><span data-stu-id="0e365-119">Whether an entry for the discount is posted depends on the contents of the **Discount Posting** field on the **Sales & Receivables Setup** page.</span></span>

<span data-ttu-id="0e365-120">Birgðafærsla er stofnuð í töflunni **birgðafærsla** fyrir hverja sölupöntunarlínu (ef línurnar eru með vörunúmerum) eða þá að fjárhagsfærsla er stofnuð í töflunni **Fjárhagsfærsla** (ef fjárhagsreikningur er í sölulínunum).</span><span class="sxs-lookup"><span data-stu-id="0e365-120">For each sales order line, an item ledger entry will be created in the **Item Ledger Entry** table (if the sales lines contain item numbers) or a general ledger entry will be created in the **G/L Entry** table (if the sales lines contain a general ledger account).</span></span> <span data-ttu-id="0e365-121">Auk þess eru sölupantanir alltaf skráðar í töflunum **Söluafhendingarhaus** og **Sölureikningshaus**.</span><span class="sxs-lookup"><span data-stu-id="0e365-121">In addition to this, sales orders are always recorded in the **Sales Shipment Header** and **Sales Invoice Header** tables.</span></span>

> [!IMPORTANT]  
> <span data-ttu-id="0e365-122">Þegar pöntun er bókuð er hægt að búa til bæði afhendingu og reikning.</span><span class="sxs-lookup"><span data-stu-id="0e365-122">When you post an order, you can create both a shipment and an invoice.</span></span> <span data-ttu-id="0e365-123">Það er hægt að gera á sama tíma eða hvort í sínu lagi.</span><span class="sxs-lookup"><span data-stu-id="0e365-123">These can be done at the same time or independently.</span></span> <span data-ttu-id="0e365-124">Einnig er hægt að mynda hlutaafhendingu og gera hlutareikning með því að fylla út reitina **magn til að flytja** og/eða **magn til að reikningsfæra** í einstökum sölupöntunarlínum áður en bókað er.</span><span class="sxs-lookup"><span data-stu-id="0e365-124">You can also create a partial shipment and a partial invoice by completing the **Qty. to Ship** and **Qty. to Invoice** fields on the individual sales order lines before you post.</span></span> <span data-ttu-id="0e365-125">Bent er á að ekki er hægt að búa til reikning fyrir eitthvað sem ekki er afhent.</span><span class="sxs-lookup"><span data-stu-id="0e365-125">Note that you cannot create an invoice for something that is not shipped.</span></span> <span data-ttu-id="0e365-126">Það er að segja, áður en hægt er að gera reikning verður afhending að vera skráð, nema afhending sé skráð um leið og reikningur er gerður.</span><span class="sxs-lookup"><span data-stu-id="0e365-126">That is, before you can invoice, you must have recorded a shipment, or you must choose to ship and invoice at the same time.</span></span>

<span data-ttu-id="0e365-127">Annaðhvort er hægt að bóka eða bóka og senda.</span><span class="sxs-lookup"><span data-stu-id="0e365-127">You can either post, or post and send.</span></span> <span data-ttu-id="0e365-128">Ef valið er að bóka og senda er PDF-skrá mynduð sem er þá hægt að senda.</span><span class="sxs-lookup"><span data-stu-id="0e365-128">If you choose to post and send, a PDF file is generated that you can then send.</span></span> <span data-ttu-id="0e365-129">Einnig er hægt að velja aðgerðina **Fjöldabóka** sem býður upp á að bóka nokkrar pantanir í einu.</span><span class="sxs-lookup"><span data-stu-id="0e365-129">You can also choose the **Post Batch** function, which lets you post several orders at the same time.</span></span> <span data-ttu-id="0e365-130">Frekari upplýsingar er að finna í [Bóka mörg skjöl á sama tíma](ui-batch-posting.md).</span><span class="sxs-lookup"><span data-stu-id="0e365-130">For more information, see [Post Multiple Documents at the Same Time](ui-batch-posting.md).</span></span>

## <a name="viewing-ledger-entries"></a><span data-ttu-id="0e365-131">Fjárhagsfærslur skoðaðar</span><span class="sxs-lookup"><span data-stu-id="0e365-131">Viewing Ledger Entries</span></span>

<span data-ttu-id="0e365-132">Þegar bókun er lokið hverfa bókuðu sölulínurnar úr pöntuninni.</span><span class="sxs-lookup"><span data-stu-id="0e365-132">When the posting is completed, the posted sales lines are removed from the order.</span></span> <span data-ttu-id="0e365-133">Skilaboð segja til um hvenær bókun er lokið.</span><span class="sxs-lookup"><span data-stu-id="0e365-133">A message tells you when the posting is completed.</span></span> <span data-ttu-id="0e365-134">Að þessu loknu verður hægt að sjá bókuðu færslurnar í ýmsum af þeim síðum sem innihalda bókaðar færslur, eins og **Viðskiptamannafærslur**, **Fjárhagsfærslur**, **Birgðafærslur,**, **Bókuð söluafhending** og **Bók. sölureikningur**.</span><span class="sxs-lookup"><span data-stu-id="0e365-134">After this, you will be able to see the posted entries in the various pages that contain posted entries, such as the **Cust. Ledger Entries**, **G/L Entries**, **Item Ledger Entries**, **Posted Sales Shipments**, and **Posted Sales Invoices** pages.</span></span>  

<span data-ttu-id="0e365-135">Í flestum tilfellum er hægt að opna fjárhagsfærslur úr viðkomandi spjaldi eða skjali.</span><span class="sxs-lookup"><span data-stu-id="0e365-135">In most cases, you can open ledger entries from the affected card or document.</span></span> <span data-ttu-id="0e365-136">Á síðunni **Viðskiptamannaspjald** skal t.d. velja aðgerðina **Fjárhagsfærslur**.</span><span class="sxs-lookup"><span data-stu-id="0e365-136">For example, on the **Customer Card** page, choose the **Ledger Entries** action.</span></span>

## <a name="editing-ledger-entries"></a><span data-ttu-id="0e365-137">Fjárhagsfærslum breytt</span><span class="sxs-lookup"><span data-stu-id="0e365-137">Editing Ledger Entries</span></span>

<span data-ttu-id="0e365-138">Hægt er að breyta tilteknum reitum í bókuðum innkaupaskjölum, svo sem **Rakningarnúmer pakka**</span><span class="sxs-lookup"><span data-stu-id="0e365-138">You can edit certain fields on posted purchase documents, such as the **Package Tracking No.**</span></span> <span data-ttu-id="0e365-139">.</span><span class="sxs-lookup"><span data-stu-id="0e365-139">field.</span></span> <span data-ttu-id="0e365-140">Frekari upplýsingar er að finna í [Breyta bókuðum skjölum](across-edit-posted-document.md).</span><span class="sxs-lookup"><span data-stu-id="0e365-140">For more information, see [Edit Posted Documents](across-edit-posted-document.md).</span></span> <span data-ttu-id="0e365-141">Til að fá fleiri mikilvæg svæði sem hafa áhrif á endurskoðunarslóðina þarf að bakfæra eða afturkalla bókun.</span><span class="sxs-lookup"><span data-stu-id="0e365-141">For more critical fields that affect the auditing trail, you must reverse or undo posting.</span></span> <span data-ttu-id="0e365-142">Frekari upplýsingar er að finna í [Bakfæra bókanir í færslubók og afturkalla kvittanir/sendingar](finance-how-reverse-journal-posting.md).</span><span class="sxs-lookup"><span data-stu-id="0e365-142">For more information, see [Reverse Journal Postings and Undo Receipts/Shipments](finance-how-reverse-journal-posting.md).</span></span>

## <a name="see-related-training-at-microsoft-learn"></a><span data-ttu-id="0e365-143">Sjá tengda þjálfun á [Microsoft Learn](/learn/modules/ship-invoice-items-dynamics-365-business-central/index)</span><span class="sxs-lookup"><span data-stu-id="0e365-143">See Related Training at [Microsoft Learn](/learn/modules/ship-invoice-items-dynamics-365-business-central/index)</span></span>

## <a name="see-also"></a><span data-ttu-id="0e365-144">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="0e365-144">See Also</span></span>

[<span data-ttu-id="0e365-145">Sala</span><span class="sxs-lookup"><span data-stu-id="0e365-145">Sales</span></span>](sales-manage-sales.md)  
[<span data-ttu-id="0e365-146">Bóka mörg skjöl á sama tíma</span><span class="sxs-lookup"><span data-stu-id="0e365-146">Post Multiple Documents at the Same Time</span></span>](ui-batch-posting.md)  
[<span data-ttu-id="0e365-147">Breyta bókuðum skjölum</span><span class="sxs-lookup"><span data-stu-id="0e365-147">Edit Posted Documents</span></span>](across-edit-posted-document.md)  
[<span data-ttu-id="0e365-148">Senda skjöl í tölvupósti</span><span class="sxs-lookup"><span data-stu-id="0e365-148">Send Documents by Email</span></span>](ui-how-send-documents-email.md)  
[<span data-ttu-id="0e365-149">Ógreiddir sölureikningar leiðréttir eða afturkallaðir</span><span class="sxs-lookup"><span data-stu-id="0e365-149">Correct or Cancel Unpaid Sales Invoices</span></span>](sales-how-correct-cancel-sales-invoice.md)  
[<span data-ttu-id="0e365-150">Finndu síður og upplýsingar með Viðmótsleit</span><span class="sxs-lookup"><span data-stu-id="0e365-150">Finding Pages and Information with Tell Me</span></span>](ui-search.md)  
<span data-ttu-id="0e365-151">[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="0e365-151">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>

[!INCLUDE[footer-include](includes/footer-banner.md)]  
