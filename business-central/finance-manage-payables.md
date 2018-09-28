---
title: "Stjórnun viðskiptaskulda| Microsoft Docs"
description: "Yfirlit yfir það hvernig á að stjórna viðskiptaskuldum, þar á meðal greiðslum lánardrottna, lánveitendum, skuldum og gjaldfallinni stöðu."
services: project-madeira
documentationcenter: 
author: bholtorf
manager: edupont
editor: 
ms.service: dynamics365-business-central
ms.workload: na
ms.tgt_pltfrm: na
ms.devlang: na
ms.topic: article
ms.search.keywords: vendor payment, creditor, debt, balance due, AP
ms.date: 10/01/2018
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 558d9cc314dec5ec8daaae42adf6b7efd443274b
ms.contentlocale: is-is
ms.lasthandoff: 09/28/2018

---
# <a name="managing-payables"></a><span data-ttu-id="955e2-103">Stjórna skuldum</span><span class="sxs-lookup"><span data-stu-id="955e2-103">Managing Payables</span></span>
[!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="955e2-104">hefur það sem þú þarft til að stjórna viðskiptaskuldum.</span><span class="sxs-lookup"><span data-stu-id="955e2-104"> has what you need to effectively manage accounts payable.</span></span>  

## <a name="payments"></a><span data-ttu-id="955e2-105">Greiðslur</span><span class="sxs-lookup"><span data-stu-id="955e2-105">Payments</span></span>
<span data-ttu-id="955e2-106">Það er auðvelt að forgangsraða greiðslum, reikna með viðurlögum vegna tímabundinna greiðslna og takast á við afslætti fyrir snemma greiðslur.</span><span class="sxs-lookup"><span data-stu-id="955e2-106">It's easy to prioritize payments, account for penalties for overdue payments, and handle discounts for early payments.</span></span>

<span data-ttu-id="955e2-107">Þú getur skráð greiðslur í almennri dagbók og síðan prentað eftir því áður en þú sendir greiðslubókina.</span><span class="sxs-lookup"><span data-stu-id="955e2-107">You can record payments in a general journal, and then print checks before posting the payment journal.</span></span>

<span data-ttu-id="955e2-108">Þú getur sótt greiðslur til loka reikninga þegar þú sendir inn greiðsluna eða eftir að þú hefur sent greiðsluna.</span><span class="sxs-lookup"><span data-stu-id="955e2-108">You can apply payments to close invoices when you post the payment, or after you post the payment.</span></span> <span data-ttu-id="955e2-109">**Jöfnunaraðferðin** sem tilgreind er fyrir lánardrottinn (á **lánardrottnaspjaldinu**) ákvarðar hvort þú sækir greiðsluna handvirkt eða sjálfkrafa.</span><span class="sxs-lookup"><span data-stu-id="955e2-109">The **Application Method** specified for the vendor (on the **Vendor Card**) determines whether you apply the payment manually, or automatically.</span></span> <span data-ttu-id="955e2-110">Þú getur alltaf jafnað færslur handvirkt.</span><span class="sxs-lookup"><span data-stu-id="955e2-110">You can always apply transactions manually.</span></span> <span data-ttu-id="955e2-111">En ef jöfnunaraðferðin fyrir lánardrottin er **Jafna elstu** og þú tilgreinir ekki fylgiskjal fyrir greiðsluna sem jafna á við verður greiðslan jöfnuð við elstu opnu færsluna fyrir þennan lánardrottin.</span><span class="sxs-lookup"><span data-stu-id="955e2-111">However, if the application method for the vendor is **Apply to Oldest**, and you do not specify a document to apply the payment to, the payment is applied to the oldest open entry for the vendor.</span></span>

## <a name="suggest-vendor-payments"></a><span data-ttu-id="955e2-112">Greiðslutillögur til lánardr.</span><span class="sxs-lookup"><span data-stu-id="955e2-112">Suggest Vendor Payments</span></span>
[!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="955e2-113">getur lagt til ýmsar greiðslur til lánardrottna, svo sem greiðslur sem eru bráðum á gjalddaga eða greiðslur sem hægt er að fá afslátt af.</span><span class="sxs-lookup"><span data-stu-id="955e2-113"> can suggest various payments to vendors, such as payments that will be due soon, or payments where a discount is available.</span></span> <span data-ttu-id="955e2-114">Greiðslutillagan getur tekið til greina upphæð sem skilgreind er sem tiltækir fjármunir fyrir greiðslu og hægt er að fá greiðsluafslátt af.</span><span class="sxs-lookup"><span data-stu-id="955e2-114">The payment suggestion can consider an amount that you specify as available funds for payment, and eligibility for payment discounts.</span></span>

## <a name="issue-checks"></a><span data-ttu-id="955e2-115">Útgáfa tékka</span><span class="sxs-lookup"><span data-stu-id="955e2-115">Issue Checks</span></span>
[!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="955e2-116">leyfir þér að gefa út eftirlit með söluaðilum handvirkt og rafrænt.</span><span class="sxs-lookup"><span data-stu-id="955e2-116"> lets you issue checks to vendors manually and electronically.</span></span> <span data-ttu-id="955e2-117">Þú gerir bæði í **Greiðslubækur** glugganum þar sem einnig er hægt að ógilda tékka og skoða fjárhagsfærslur.</span><span class="sxs-lookup"><span data-stu-id="955e2-117">You do both in the **Payment Journals** window, where you can also void checks and view check ledger entries.</span></span>

## <a name="export-payments-to-a-bank-file"></a><span data-ttu-id="955e2-118">Flytja út greiðslur í bankaskrá</span><span class="sxs-lookup"><span data-stu-id="955e2-118">Export Payments to a Bank File</span></span>
<span data-ttu-id="955e2-119">Þegar þú ert tilbúinn til að greiða lánardrottni er hægt úr **Greiðslubók** að flytja út skrá með greiðsluupplýsingum á færslubókarlínur.</span><span class="sxs-lookup"><span data-stu-id="955e2-119">When you are ready to pay a vendor, from the **Payment Journal** window you can export a file with the payment information from the journal lines.</span></span> <span data-ttu-id="955e2-120">Þá er hægt að hlaða upp skránni í netbanka til að meðhöndla peningaflutning.</span><span class="sxs-lookup"><span data-stu-id="955e2-120">You can then upload the file to your electronic bank to process the money transfers.</span></span>

<span data-ttu-id="955e2-121">Ef þú vilt ekki bóka greiðslubókarlínu fyrir útflutta greiðslu, t.d. vegna þess að þú ert að bíða eftir staðfestingu frá banka á færslunni geturðu einfaldlega eytt línunni.</span><span class="sxs-lookup"><span data-stu-id="955e2-121">If you do not want to post a payment journal line for an exported payment, for example because you are waiting for the bank to confirm the transaction, just delete the journal line.</span></span> <span data-ttu-id="955e2-122">Þegar þú síðar stofnar greiðslubókarlínu til að greiða eftirstandandi upphæð á reikningnum sýnir reiturinn **Heildarupphæð flutt út** hversu mikið af greiðsluupphæðinni hefur þegar verið flutt út.</span><span class="sxs-lookup"><span data-stu-id="955e2-122">Later, when you create a payment journal line to pay the remaining amount on the invoice, the **Total Exported Amount** field shows how much of the payment amount has already been exported.</span></span> <span data-ttu-id="955e2-123">Þú getur einnig fundið ítarlegar upplýsingar um heildarupphæðir sem hafa verið fluttar út með því að velja hnappinn **Skráningarfærslur kreditmillifærslna**.</span><span class="sxs-lookup"><span data-stu-id="955e2-123">Also, you can find detailed information about the exported total by choosing the **Credit Transfer Reg. Entries** button.</span></span>

<span data-ttu-id="955e2-124">Ef þú bíður eftir að bóka greiðslur þar til bankinn þinn staðfestir að hann hafi meðhöndlað viðskipti, þá eru tvær leiðir til að koma í veg fyrir að greiðslur sé óvart fluttar út aftur fyrir opin skjöl:</span><span class="sxs-lookup"><span data-stu-id="955e2-124">If you wait to post payments until after your bank confirms that it has processed transactions, there are two ways to avoid accidentally re-exporting payments for open documents:</span></span>  

* <span data-ttu-id="955e2-125">Í greiðslubók með tillögum að greiðslulínum geturðu flokkað með annað hvort dálkinum **Flutt út í greiðsluskrá** eða **Heildarupphæð flutt út** dálkunum og svo eytt greiðslutillögum fyrir opna reikninga þar sem greiðslur hafa þegar átt sér stað og þú vilt ekki greiða.</span><span class="sxs-lookup"><span data-stu-id="955e2-125">In a payment journal with suggested payment lines, sort on either the **Exported to Payment File** or **Total Exported Amount** columns, and then delete payment suggestions for open invoices for which payments have already been made and you do not want to make payments for.</span></span>

    <span data-ttu-id="955e2-126">**Athugaðu** Þú gætir þurft að bæta þessum dálkum við listann.</span><span class="sxs-lookup"><span data-stu-id="955e2-126">**Note** You might have to add these columns to the list.</span></span> <span data-ttu-id="955e2-127">Frekari upplýsingar eru í [Sérstilling vinnusvæðisins þíns](ui-personalization-user.md).</span><span class="sxs-lookup"><span data-stu-id="955e2-127">For more information, see [Personalizing Your Workspace](ui-personalization-user.md).</span></span>  
* <span data-ttu-id="955e2-128">Einnig, á **Greiðslutillögur til lánardrottna** runuvinnslunni þar sem hægt er að tilgreina greiðslur sem á að taka með í greiðslubókinni er hægt að tilgreina að setja ekki inn greiðslulínur fyrir greiðslur sem hafa þegar verið fluttar út með því að velja **Sleppa útfluttum greiðslum** gátreitinn.</span><span class="sxs-lookup"><span data-stu-id="955e2-128">Alternatively, on the **Suggest Vendor Payments** batch job, where you specify the payments to include in the payment journal, you can specify not to insert journal lines for payments that have already been exported by choosing the **Skip Exported Payments** check box.</span></span>

## <a name="see-also"></a><span data-ttu-id="955e2-129">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="955e2-129">See Also</span></span>
[<span data-ttu-id="955e2-130">Greiðsluhættir</span><span class="sxs-lookup"><span data-stu-id="955e2-130">Payment Methods</span></span>](finance-payment-methods.md)  
[<span data-ttu-id="955e2-131">Fjármál</span><span class="sxs-lookup"><span data-stu-id="955e2-131">Finance</span></span>](finance.md)  
<span data-ttu-id="955e2-132">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="955e2-132">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

