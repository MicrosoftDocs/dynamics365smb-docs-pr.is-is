---
title: "Hvernig skal bóka innkaupaskjöl | Microsoft Docs"
description: "Kynntu þér mismunandi bókunaraðferðir til að bóka innkaupaskjöl."
services: project-madeira
documentationcenter: 
author: SusanneWindfeldPedersen
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 05/12/2017
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 06c22658518d504c80a5a379d579cf7f7e8a0757
ms.contentlocale: is-is
ms.lasthandoff: 03/22/2018

---
# <a name="posting-purchases"></a><span data-ttu-id="6068c-103">Bókun innkaupa</span><span class="sxs-lookup"><span data-stu-id="6068c-103">Posting Purchases</span></span>
<span data-ttu-id="6068c-104">Í **bókunarflokki** á innkaupaskjali er hægt að velja milli eftirfarandi bókunaraðgerða:</span><span class="sxs-lookup"><span data-stu-id="6068c-104">In the **Posting group** on a purchase document, you can choose between the following posting functions:</span></span>

* <span data-ttu-id="6068c-105">**Færsla**</span><span class="sxs-lookup"><span data-stu-id="6068c-105">**Post**</span></span>
* <span data-ttu-id="6068c-106">**Forskoðun bókunar**</span><span class="sxs-lookup"><span data-stu-id="6068c-106">**Preview Posting**</span></span>
* <span data-ttu-id="6068c-107">**Bóka og prenta**</span><span class="sxs-lookup"><span data-stu-id="6068c-107">**Post and Print**</span></span>
* <span data-ttu-id="6068c-108">**Prófunarskýrsla**</span><span class="sxs-lookup"><span data-stu-id="6068c-108">**Test Report**</span></span>
* <span data-ttu-id="6068c-109">**Bóka runu**</span><span class="sxs-lookup"><span data-stu-id="6068c-109">**Post Batch**</span></span>

<span data-ttu-id="6068c-110">Þegar lokið hefur verið við allar línurnar og allar upplýsingar færðar á innkaupapöntunina er hægt að bóka hana, það er að segja stofna móttöku og reikning.</span><span class="sxs-lookup"><span data-stu-id="6068c-110">When you have completed all the lines and entered all the information on the purchase order, you can post it, that is, create a receipt and an invoice.</span></span>

<span data-ttu-id="6068c-111">Þegar innkaupapöntun er bókuð, eru reikningur lánardrottins, fjárhagurinn og birgðahöfuðbókarfærslur uppfærðar.</span><span class="sxs-lookup"><span data-stu-id="6068c-111">When a purchase order is posted, the vendor's account, the general ledger, and the item ledger entries are updated.</span></span>

<span data-ttu-id="6068c-112">Innkaupafærsla er stofnuð í töflunni  **Fjárhagsfærsla** fyrir hverja innkaupapöntun.</span><span class="sxs-lookup"><span data-stu-id="6068c-112">For each purchase order, a purchase entry is created in the **G/L Entry** table.</span></span> <span data-ttu-id="6068c-113">Færsla er einnig stofnuð í lánardrottnareikningi í töflunni **færsla í lánardrottnabók** og fjárhagsfærsla er stofnuð í viðeigandi safnreikningi lánardrottna.</span><span class="sxs-lookup"><span data-stu-id="6068c-113">An entry is also created in the vendor's account in the **Vendor Ledger Entry** table and a G/L entry is created in the relevant payables account.</span></span> <span data-ttu-id="6068c-114">Auk þess getur bókun pöntunarinnar leitt til VSK-færslu og fjárhagsfærslu vegna afsláttar.</span><span class="sxs-lookup"><span data-stu-id="6068c-114">In addition, posting the order may result in a VAT entry and a G/L entry for the discount amount.</span></span> <span data-ttu-id="6068c-115">Hvort færsla vegna afsláttar er bókuð fer eftir því sem er í reitnum **Afsláttarbókun** í glugganum **Innkaupagrunnur**.</span><span class="sxs-lookup"><span data-stu-id="6068c-115">Whether an entry for the discount is posted depends on the contents of the **Discount Posting** field in the **Purchases & Payables Setup** window.</span></span>

<span data-ttu-id="6068c-116">Birgðafærsla er stofnuð í töflunni  **birgðafærsla** fyrir hverja innkaupapöntunarlínu (ef innkaupalínurnar eru með vörunúmerum) eða þá að fjárhagsfærsla er stofnuð í töflunni **Fjárhagsfærsla** (ef fjárhagsreikningur er í innkaupalínunum).</span><span class="sxs-lookup"><span data-stu-id="6068c-116">For each purchase order line, an item ledger entry will be created in the **Item Ledger Entry** table (if the purchase lines contain item numbers) or a G/L entry will be created in the **G/L Entry** table (if the purchase lines contain a G/L account).</span></span> <span data-ttu-id="6068c-117">Þar að auki eru innkaupapantanir alltaf skráðar í töflunum **Innk.móttökuhaus** og **Innk.reikningshaus** .</span><span class="sxs-lookup"><span data-stu-id="6068c-117">In addition, purchase orders are always recorded in the **Purch. Recpt. Header** and **Purch. Inv. Header** tables.</span></span>

<span data-ttu-id="6068c-118">Áður en byrjað er að bóka er hægt að prenta prófunarskýrslu sem er með öllum upplýsingum í innkaupapöntuninni og birtir hugsanlegar villur.</span><span class="sxs-lookup"><span data-stu-id="6068c-118">Before you start to post, you can print a test report that contains all the information in the purchase order and indicates any errors there.</span></span> <span data-ttu-id="6068c-119">Til að prenta skýrsluna er farið í flipann **Bókun**valin, og síðan **Prufuskýrsla**.</span><span class="sxs-lookup"><span data-stu-id="6068c-119">To print the report, choose **Posting**, and then choose **Test Report**.</span></span>

> [!IMPORTANT]  
>   <span data-ttu-id="6068c-120">Hægt er að stofna bæði móttöku og reikning þegar pöntun er bókuð.</span><span class="sxs-lookup"><span data-stu-id="6068c-120">When you post an order, you can create both a receipt and an invoice.</span></span> <span data-ttu-id="6068c-121">Það er hægt að gera samhliða eða hvort í sínu lagi.</span><span class="sxs-lookup"><span data-stu-id="6068c-121">These can be done simultaneously or independently.</span></span> <span data-ttu-id="6068c-122">Einnig er hægt að mynda hlutamóttöku og gera hlutareikning með því að fylla út reitina **magnt til móttöku** og **magn til að reikningsfæra** í einstökum innkaupapöntunarlínum áður en bókað er.</span><span class="sxs-lookup"><span data-stu-id="6068c-122">You can also create a partial receipt and a partial invoice by completing the **Qty. to Receive** and **Qty. to Invoice** fields on the individual purchase order lines before you post.</span></span> <span data-ttu-id="6068c-123">Bent er á að ekki er hægt að búa til reikning fyrir einhverju sem hefur ekki verið móttekið.</span><span class="sxs-lookup"><span data-stu-id="6068c-123">Note that you cannot create an invoice for something that has not been received.</span></span> <span data-ttu-id="6068c-124">Það er að segja, áður en hægt er að gera reikning verður móttaka að vera skráð, nema móttaka sé skráð um leið og reikningur er gerður.</span><span class="sxs-lookup"><span data-stu-id="6068c-124">That is, before you can invoice, you must have recorded a receipt, or you must choose to receive and invoice at the same time.</span></span>

<span data-ttu-id="6068c-125">Hægt er annað hvort að bóka, eða bóka og prenta.</span><span class="sxs-lookup"><span data-stu-id="6068c-125">You can either post, or post and print.</span></span> <span data-ttu-id="6068c-126">Ef valið er að bóka og prenta prentast skýrslan við bókun pöntunarinnar.</span><span class="sxs-lookup"><span data-stu-id="6068c-126">If you choose to post and print, a report is printed when the order is posted.</span></span> <span data-ttu-id="6068c-127">Einnig er hægt að velja aðgerðina **Fjöldabóka** sem býður upp á að bóka nokkrar pantanir í einu.</span><span class="sxs-lookup"><span data-stu-id="6068c-127">You can also choose the **Post Batch** function, which lets you post several orders at the same time.</span></span>

<span data-ttu-id="6068c-128">Þegar bókun er lokið hverfa bókuðu innkaupalínurnar úr pöntuninni.</span><span class="sxs-lookup"><span data-stu-id="6068c-128">When the posting is completed, the posted purchase lines are removed from the order.</span></span> <span data-ttu-id="6068c-129">Skilaboð segja til um hvenær bókun er lokið.</span><span class="sxs-lookup"><span data-stu-id="6068c-129">A message tells you when the posting is completed.</span></span> <span data-ttu-id="6068c-130">Að þessu loknu má sjá bókuðu færslurnar í ýmsum af þeim gluggum sem innihalda bókaðar færslur, eins og **Lánardrottinsfærslur**, **Fjárhagsfærslur**, **Birgðafærslur**, **Innkaupaafhendingar** og **bókaðir Innkaupareikninga** glugga.</span><span class="sxs-lookup"><span data-stu-id="6068c-130">After this, you will be able to see the posted entries in the various windows that contain posted entries, such as the **Vendor Ledger Entries**, **G/L Entries**, **Item Ledger Entries**, **Purchase Receipts**, and **Posted Purchase Invoices** windows.</span></span>

## <a name="see-also"></a><span data-ttu-id="6068c-131">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="6068c-131">See Also</span></span>
[<span data-ttu-id="6068c-132">Innkaup</span><span class="sxs-lookup"><span data-stu-id="6068c-132">Purchasing</span></span>](purchasing-manage-purchasing.md)  
[<span data-ttu-id="6068c-133">Bóka skjöl og færslubækur</span><span class="sxs-lookup"><span data-stu-id="6068c-133">Post Documents and Journals</span></span>](ui-post-documents-journals.md)  
<span data-ttu-id="6068c-134">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="6068c-134">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>


