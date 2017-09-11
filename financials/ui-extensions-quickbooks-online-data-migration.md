---
title: "Notkun á QuickBooks Flutningsviðbót | Microsoft Docs"
description: "Lýsir því hvernig skal nota viðbæturnar til að yfirfæra viðskiptamenn, lánardrottna, vörur og reikninga frá QuickBooks Online til Financials."
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: extension, migrate, data, QuickBooks, import
ms.date: 05/24/2017
ms.author: bholtorf
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: fe87a108d132ff25f0c93a51df58bb88fb12f421
ms.contentlocale: is-is
ms.lasthandoff: 09/11/2017

---

# <a name="the-quickbooks-online-data-migration-extension-for-dynamics-365-for-financials"></a><span data-ttu-id="e69fd-103">QuickBooks Online gagnaflutningsviðbótin fyrir Dynamics 365 for Financials</span><span class="sxs-lookup"><span data-stu-id="e69fd-103">The QuickBooks Online Data Migration Extension for Dynamics 365 for Financials</span></span>
<span data-ttu-id="e69fd-104">Þessi viðbót er innifalin í **Gagnaflutningur** uppsetningu með aðstoð til að aðstoða þig við að flytja mikilvæg viðskiptagögn frá QuickBooks Online til [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="e69fd-104">This extension is included in the **Data Migration** assisted setup guide to help you migrate important business data from QuickBooks Online to [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="e69fd-105">Þetta er t.d. gagnlegt þegar fyrirtækið þitt er að vaxa, og þú hefur ákveðið að uppfæra stjórnunarforrit fyrirtækisins með því að byrja að nota [!INCLUDE[d365fin](includes/d365fin_md.md)]</span><span class="sxs-lookup"><span data-stu-id="e69fd-105">For example, this is useful when your business is growing, and you've decided to upgrade your business management app by starting to use [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

## <a name="what-data-can-i-import-from-quickbooks-online"></a><span data-ttu-id="e69fd-106">Hvaða gögn get ég flutt inn frá QuickBooks Online?</span><span class="sxs-lookup"><span data-stu-id="e69fd-106">What data can I import from QuickBooks Online?</span></span>
<span data-ttu-id="e69fd-107">Þú getur flutt inn eftirfarandi gögn frá QuickBooks Online til [!INCLUDE[d365fin](includes/d365fin_md.md)]:</span><span class="sxs-lookup"><span data-stu-id="e69fd-107">You can import the following data from QuickBooks Online to [!INCLUDE[d365fin](includes/d365fin_md.md)]:</span></span>  

* <span data-ttu-id="e69fd-108">Viðskiptavinum</span><span class="sxs-lookup"><span data-stu-id="e69fd-108">Customers</span></span>
* <span data-ttu-id="e69fd-109">Lánardrottnar</span><span class="sxs-lookup"><span data-stu-id="e69fd-109">Vendors</span></span>
* <span data-ttu-id="e69fd-110">Birgðir</span><span class="sxs-lookup"><span data-stu-id="e69fd-110">Items</span></span>
* <span data-ttu-id="e69fd-111">Bókhaldslykill</span><span class="sxs-lookup"><span data-stu-id="e69fd-111">Chart of accounts</span></span> 
* <span data-ttu-id="e69fd-112">Upphafsstöðufærsla í fjárhagnum</span><span class="sxs-lookup"><span data-stu-id="e69fd-112">Beginning balance transaction in the general ledger</span></span>
* <span data-ttu-id="e69fd-113">Magn á lager fyrir birgðavörur</span><span class="sxs-lookup"><span data-stu-id="e69fd-113">On-hand quantities for inventory items</span></span>
* <span data-ttu-id="e69fd-114">Opna skjöl fyrir viðskiptamenn og lánardrottna, eins og t.d. reikningar, kreditreikningar og greiðslur.</span><span class="sxs-lookup"><span data-stu-id="e69fd-114">Open documents for customers and vendors, such as invoices, credit memos, and payments</span></span>

<span data-ttu-id="e69fd-115">Við flytjum aðeins fullar upphæðir í sölu- og innkaupaskjöl.</span><span class="sxs-lookup"><span data-stu-id="e69fd-115">We migrate only full amounts on sales and purchase documents.</span></span> <span data-ttu-id="e69fd-116">Við uppfærum ekki upphæðir greiddar að hluta.</span><span class="sxs-lookup"><span data-stu-id="e69fd-116">We do not update partially paid amounts.</span></span> <span data-ttu-id="e69fd-117">Ef viðskiptamaður hefur t.d. borgað 300 af 500 dollurum á sölureikningi, flytjum við fulla upphæð eða 500.</span><span class="sxs-lookup"><span data-stu-id="e69fd-117">For example, if a customer has paid 300 of a total of 500 dollars on a sales invoice, we migrate the full 500.</span></span> <span data-ttu-id="e69fd-118">Ef þú hefur fengið greiddan hluta af greiðslum, þarf að uppfæra þær handvirkt, annað hvort áður eða eftir að þú flytur gögn.</span><span class="sxs-lookup"><span data-stu-id="e69fd-118">If you have received partial payments, you must update these manually, either before or after you migrate data.</span></span> <span data-ttu-id="e69fd-119">Við mælum með því að þú jafnir útistandandi færslur áður en þú flytur gögn, bara til þess að gera eftirleikinn auðveldari.</span><span class="sxs-lookup"><span data-stu-id="e69fd-119">We recommend that you apply outstanding transactions before you migrate, just to make things easier afterward.</span></span>

> [!NOTE]  
>   <span data-ttu-id="e69fd-120">Við flytjum ekki innkaupapantanir eða sölupantanir.</span><span class="sxs-lookup"><span data-stu-id="e69fd-120">We do not migrate purchase orders or sales orders.</span></span>

## <a name="before-you-start"></a><span data-ttu-id="e69fd-121">Verður að byrja fyrir</span><span class="sxs-lookup"><span data-stu-id="e69fd-121">Before you start</span></span>
<span data-ttu-id="e69fd-122">Mikilvægur hluti flutningsferlisins er að tilgreina reikningana sem flytja á færslur til.</span><span class="sxs-lookup"><span data-stu-id="e69fd-122">An important part of the migration process is to specify the accounts to migrate transactions to.</span></span> <span data-ttu-id="e69fd-123">Það er tilvalið að skipuleggja vörpunina áður en þú flytur gögn.</span><span class="sxs-lookup"><span data-stu-id="e69fd-123">It's a good idea to plan this mapping before you migrate data.</span></span> <span data-ttu-id="e69fd-124">Til dæmis, reikningana sem þú bókar færslurnar fyrir:</span><span class="sxs-lookup"><span data-stu-id="e69fd-124">For example, the accounts where you post transactions for:</span></span>  
  
* <span data-ttu-id="e69fd-125">Sala vöru eða þjónustu til viðskiptamanna.</span><span class="sxs-lookup"><span data-stu-id="e69fd-125">The sale of items or services to customers.</span></span>
* <span data-ttu-id="e69fd-126">Innkaup vöru eða þjónustu frá lánardrottnum.</span><span class="sxs-lookup"><span data-stu-id="e69fd-126">The purchase of items or services from vendors.</span></span>  
* <span data-ttu-id="e69fd-127">Leiðréttingar í fjárhagnum.</span><span class="sxs-lookup"><span data-stu-id="e69fd-127">Adjustments in the general ledger.</span></span>  

[!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="e69fd-128"> krefst þess að fjárhagsreikningum hafi verið úthlutað reikningsnúmerum.</span><span class="sxs-lookup"><span data-stu-id="e69fd-128"> requires that general ledger accounts have account numbers assigned to them.</span></span> <span data-ttu-id="e69fd-129">Vertu viss um að reikningsnúmerum hafi verið úthlutað til reikninganna í QuickBooks Online.</span><span class="sxs-lookup"><span data-stu-id="e69fd-129">Make sure that account numbers are assigned to your accounts in QuickBooks Online.</span></span>

<span data-ttu-id="e69fd-130">Ef færslur í QuickBooks Online hafa skattaupphæðir, þarf að setja upp skattareikning fyrir þína skattalögsögu í [!INCLUDE[d365fin](includes/d365fin_md.md)] áður en þú getur bókað færslur.</span><span class="sxs-lookup"><span data-stu-id="e69fd-130">If transactions in QuickBooks Online have tax amounts, you must set up a tax account for your tax jurisdictions in [!INCLUDE[d365fin](includes/d365fin_md.md)] before you can post transactions.</span></span>

## <a name="how-do-i-start-using-the-extension"></a><span data-ttu-id="e69fd-131">Hvernig byrja ég að nota viðbótina?</span><span class="sxs-lookup"><span data-stu-id="e69fd-131">How do I start using the extension?</span></span>
<span data-ttu-id="e69fd-132">Auðvelt er að hefjast handa</span><span class="sxs-lookup"><span data-stu-id="e69fd-132">Getting started is easy.</span></span> <span data-ttu-id="e69fd-133">Það eina sem þú þarft að gera er að keyra **Gagnaflutingur** uppsetningu með aðstoðarleiðbeiningum.</span><span class="sxs-lookup"><span data-stu-id="e69fd-133">All you need to do is run the **Data Migration** assisted setup guide.</span></span> <span data-ttu-id="e69fd-134">Svona er það gert:</span><span class="sxs-lookup"><span data-stu-id="e69fd-134">Here's how:</span></span>

1. <span data-ttu-id="e69fd-135">Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Uppsetning með aðstoð** og velja síðan **Flytja viðskiptagögn**.</span><span class="sxs-lookup"><span data-stu-id="e69fd-135">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Assisted Setup**, and then choose **Migrate business data**.</span></span>
2. <span data-ttu-id="e69fd-136">Fylgdu leiðbeiningunum fyrir hvert skrefi í Uppsetningu með aðstoð.</span><span class="sxs-lookup"><span data-stu-id="e69fd-136">Follow the instructions on each step in the assisted setup guide.</span></span>

## <a name="what-do-i-do-after-i-migrate-data"></a><span data-ttu-id="e69fd-137">Hvað geri ég eftir gagnaflutninginn?</span><span class="sxs-lookup"><span data-stu-id="e69fd-137">What do I do after I migrate data?</span></span>
<span data-ttu-id="e69fd-138">Þegar gagnaflutningi er lokið, hafa færslur stöðuna **Óbókaðar**, svo þú getur endurskoðað þær og gert leiðréttingar.</span><span class="sxs-lookup"><span data-stu-id="e69fd-138">After you migrate data, transactions have the status **Unposted**, so you can review them and make adjustments.</span></span> <span data-ttu-id="e69fd-139">Til að endurskoða færslurnar, skal farið á síðuna þar þú myndir venjulega finna þær.</span><span class="sxs-lookup"><span data-stu-id="e69fd-139">To review the transactions, go to the page where you would normally find them.</span></span> <span data-ttu-id="e69fd-140">Til dæmis, til að endurskoða óbókaða sölureikninga, skal farið á síðuna **Sölureikningar**.</span><span class="sxs-lookup"><span data-stu-id="e69fd-140">For example, to review unposted sales invoices, go to the **Sales Invoices** page.</span></span> <span data-ttu-id="e69fd-141">Til að endurskoða greiðslubækur, skal fara á síðuna **Greiðslubækur**.</span><span class="sxs-lookup"><span data-stu-id="e69fd-141">To review payment journals, go to the **Payment Journals** page.</span></span>   

<span data-ttu-id="e69fd-142">Það eru einkum nokkrir hlutir sem þú þarft að gera:</span><span class="sxs-lookup"><span data-stu-id="e69fd-142">There are a few things in particular that you should do:</span></span>

* <span data-ttu-id="e69fd-143">Ef færslurnar í QuickBooks Online höfðu breytingarmerkingar eða afsláttarupphæð, verður að bæta upphæðunum handvirkt við tengdar færslur í [!INCLUDE[d365fin](includes/d365fin_md.md)] áður en þú bókar þær.</span><span class="sxs-lookup"><span data-stu-id="e69fd-143">If the transactions in QuickBooks Online had markup or discount amounts, you must manually add the amounts to the related transactions in [!INCLUDE[d365fin](includes/d365fin_md.md)] before you post them.</span></span>
* <span data-ttu-id="e69fd-144">Ef þú ert að nota VSK, þarftu kannski að bæta viðskiptabókunarflokki og vörubókunarflokki við uppsetningu bókana svo þú getir bókað VSK upphæðir.</span><span class="sxs-lookup"><span data-stu-id="e69fd-144">If you are using value added tax (VAT), you may need to add a business posting group and a product posting group to the posting setup so that you can post VAT amounts.</span></span>
* <span data-ttu-id="e69fd-145">Staðfesta upphafsstöðu reikninga í fjárhagnum.</span><span class="sxs-lookup"><span data-stu-id="e69fd-145">Verify the beginning balances for accounts in the general ledger.</span></span> <span data-ttu-id="e69fd-146">QuickBooks Online geymir ekki núgildandi stöðu fyrir alla reikninga, og því gætirðu þurft að leiðrétta upphafstöður.</span><span class="sxs-lookup"><span data-stu-id="e69fd-146">QuickBooks Online does not store the current balance for all accounts, so you might need to correct beginning balances.</span></span>

## <a name="see-also"></a><span data-ttu-id="e69fd-147">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="e69fd-147">See Also</span></span>
[<span data-ttu-id="e69fd-148">Innflutningur viðskiptagagna úr öðrum fjárhagskerfum</span><span class="sxs-lookup"><span data-stu-id="e69fd-148">Importing Business Data from Other Finance Systems</span></span>](upload-data.md)  
<span data-ttu-id="e69fd-149">[Sérstilling [!INCLUDE[d365fin](includes/d365fin_md.md)] með viðbótum](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="e69fd-149">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions](ui-extensions.md)</span></span>  

