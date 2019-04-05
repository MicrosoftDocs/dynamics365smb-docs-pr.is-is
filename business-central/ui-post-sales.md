---
title: Hvernig skal bóka söluskjöl | Microsoft Docs
description: Kynntu þér mismunandi bókunaraðferðir til að bóka söluskjöl.
services: project-madeira
documentationcenter: ''
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 10/01/2018
ms.author: solsen
ms.openlocfilehash: 7ada688f7946d7f857dc6d4a6518b8bcb4e5c707
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/08/2019
ms.locfileid: "800011"
---
# <a name="posting-sales"></a><span data-ttu-id="35551-103">Sölubókun</span><span class="sxs-lookup"><span data-stu-id="35551-103">Posting Sales</span></span>
<span data-ttu-id="35551-104">Í **bókunarflokki** á söluskjali er hægt að velja milli eftirfarandi bókunaraðgerða:</span><span class="sxs-lookup"><span data-stu-id="35551-104">In the **Posting group** on a sales document, you can choose between the following posting functions:</span></span>

* <span data-ttu-id="35551-105">**Færsla**</span><span class="sxs-lookup"><span data-stu-id="35551-105">**Post**</span></span>
* <span data-ttu-id="35551-106">**Prófunarskýrsla**</span><span class="sxs-lookup"><span data-stu-id="35551-106">**Test Report**</span></span>
* <span data-ttu-id="35551-107">**Bóka og senda**</span><span class="sxs-lookup"><span data-stu-id="35551-107">**Post and Send**</span></span>
* <span data-ttu-id="35551-108">**Bóka og prenta**</span><span class="sxs-lookup"><span data-stu-id="35551-108">**Post and Print**</span></span>
* <span data-ttu-id="35551-109">**Bóka og senda í tölvupósti**</span><span class="sxs-lookup"><span data-stu-id="35551-109">**Post and Email**</span></span>
* <span data-ttu-id="35551-110">**Bóka runu**</span><span class="sxs-lookup"><span data-stu-id="35551-110">**Post Batch**</span></span>
* <span data-ttu-id="35551-111">**Forskoðun bókunar**</span><span class="sxs-lookup"><span data-stu-id="35551-111">**Preview Posting**</span></span>

<span data-ttu-id="35551-112">Þegar lokið hefur verið við allar línurnar og allar upplýsingar færðar á sölupöntunina er hægt að bóka hana.</span><span class="sxs-lookup"><span data-stu-id="35551-112">When you have completed all the lines and entered all the information on the sales order, you can post it.</span></span> <span data-ttu-id="35551-113">Þetta stofnar afhendingu og reikning.</span><span class="sxs-lookup"><span data-stu-id="35551-113">This creates a shipment and an invoice.</span></span>

<span data-ttu-id="35551-114">Þegar sölupöntun er bókuð, eru reikningur viðskiptavinar, fjárhagurinn og birgðahöfuðbókarfærslur uppfærðar.</span><span class="sxs-lookup"><span data-stu-id="35551-114">When a sales order is posted, the customer's account, the general ledger, and the item ledger entries are updated.</span></span>

<span data-ttu-id="35551-115">Sölufærsla er stofnuð í töflunni G/L Entry **fjárhagsfærsla** fyrir hverja sölupöntun.</span><span class="sxs-lookup"><span data-stu-id="35551-115">For each sales order, a sales entry is created in the **G/L Entry** table.</span></span> <span data-ttu-id="35551-116">Færsla er einnig stofnuð í reikningi viðskiptamanns í töflunni **sérsniðin fjárhagsfærsla** og fjárhagsfærsla er stofnuð í viðeigandi safnreikningi viðskiptamanns.</span><span class="sxs-lookup"><span data-stu-id="35551-116">An entry is also created in the customer's account in the **Cust. Ledger Entry** table and a general ledger entry is created in the relevant receivables account.</span></span> <span data-ttu-id="35551-117">Auk þess getur bókun pöntunarinnar leitt til VSK-færslu og fjárhagsfærslu vegna afsláttar.</span><span class="sxs-lookup"><span data-stu-id="35551-117">In addition, posting the order may result in a VAT entry and a general ledger entry for the discount amount.</span></span> <span data-ttu-id="35551-118">Hvort færsla vegna afsláttar er bókuð fer eftir því sem er í reitnum **Afsláttarbókun** á síðunni **Sölugrunnur**.</span><span class="sxs-lookup"><span data-stu-id="35551-118">Whether an entry for the discount is posted depends on the contents of the **Discount Posting** field on the **Sales & Receivables Setup** page.</span></span>

<span data-ttu-id="35551-119">Birgðafærsla er stofnuð í töflunni **birgðafærsla** fyrir hverja sölupöntunarlínu (ef línurnar eru með vörunúmerum) eða þá að fjárhagsfærsla er stofnuð í töflunni **Fjárhagsfærsla** (ef fjárhagsreikningur er í sölulínunum).</span><span class="sxs-lookup"><span data-stu-id="35551-119">For each sales order line, an item ledger entry will be created in the **Item Ledger Entry** table (if the sales lines contain item numbers) or a general ledger entry will be created in the **G/L Entry** table (if the sales lines contain a general ledger account).</span></span> <span data-ttu-id="35551-120">Auk þess eru sölupantanir alltaf skráðar í töflunum **Söluafhendingarhaus** og **Sölureikningshaus**.</span><span class="sxs-lookup"><span data-stu-id="35551-120">In addition to this, sales orders are always recorded in the **Sales Shipment Header** and **Sales Invoice Header** tables.</span></span>

> [!IMPORTANT]  
>   <span data-ttu-id="35551-121">Þegar pöntun er bókuð er hægt að búa til bæði afhendingu og reikning.</span><span class="sxs-lookup"><span data-stu-id="35551-121">When you post an order, you can create both a shipment and an invoice.</span></span> <span data-ttu-id="35551-122">Það er hægt að gera á sama tíma eða hvort í sínu lagi.</span><span class="sxs-lookup"><span data-stu-id="35551-122">These can be done at the same time or independently.</span></span> <span data-ttu-id="35551-123">Einnig er hægt að mynda hlutaafhendingu og gera hlutareikning með því að fylla út reitina **magn til að flytja** og/eða **magn til að reikningsfæra** í einstökum sölupöntunarlínum áður en bókað er.</span><span class="sxs-lookup"><span data-stu-id="35551-123">You can also create a partial shipment and a partial invoice by completing the **Qty. to Ship** and **Qty. to Invoice** fields on the individual sales order lines before you post.</span></span> <span data-ttu-id="35551-124">Bent er á að ekki er hægt að búa til reikning fyrir eitthvað sem ekki er afhent.</span><span class="sxs-lookup"><span data-stu-id="35551-124">Note that you cannot create an invoice for something that is not shipped.</span></span> <span data-ttu-id="35551-125">Það er að segja, áður en hægt er að gera reikning verður afhending að vera skráð, nema afhending sé skráð um leið og reikningur er gerður.</span><span class="sxs-lookup"><span data-stu-id="35551-125">That is, before you can invoice, you must have recorded a shipment, or you must choose to ship and invoice at the same time.</span></span>

<span data-ttu-id="35551-126">Þegar bókun er lokið hverfa bókuðu sölulínurnar úr pöntuninni.</span><span class="sxs-lookup"><span data-stu-id="35551-126">When the posting is completed, the posted sales lines are removed from the order.</span></span> <span data-ttu-id="35551-127">Skilaboð segja til um hvenær bókun er lokið.</span><span class="sxs-lookup"><span data-stu-id="35551-127">A message tells you when the posting is completed.</span></span> <span data-ttu-id="35551-128">Að þessu loknu verður hægt að sjá bókuðu færslurnar í ýmsum af þeim síðum sem innihalda bókaðar færslur, eins og **Viðskiptamannafærslur**, **Fjárhagsfærslur**, **Birgðafærslur,**, **Bókuð söluafhending** og **Bók. sölureikningur**.</span><span class="sxs-lookup"><span data-stu-id="35551-128">After this, you will be able to see the posted entries in the various pages that contain posted entries, such as the **Cust. Ledger Entries**, **G/L Entries**, **Item Ledger Entries**, **Posted Sales Shipments**, and **Posted Sales Invoices** pages.</span></span>

## <a name="see-also"></a><span data-ttu-id="35551-129">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="35551-129">See Also</span></span>
[<span data-ttu-id="35551-130">Sala</span><span class="sxs-lookup"><span data-stu-id="35551-130">Sales</span></span>](sales-manage-sales.md)  
[<span data-ttu-id="35551-131">Senda skjöl í tölvupósti</span><span class="sxs-lookup"><span data-stu-id="35551-131">Send Documents by Email</span></span>](ui-how-send-documents-email.md)  
<span data-ttu-id="35551-132">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="35551-132">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

