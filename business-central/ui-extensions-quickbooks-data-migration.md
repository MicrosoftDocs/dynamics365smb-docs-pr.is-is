---
title: Flutningsviðbót QuickBooks | Microsoft Docs
description: Lýsir því hvernig skal nota viðbótina til að flytja inn viðskiptamenn, lánardrottna, vörur og reikninga frá QuickBooks Desktop til Business Central.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, import, implement
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: d6b44ccfc11438930450dd86cab53736f00995c5
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5785036"
---
# <a name="the-quickbooks-data-migration-extension"></a><span data-ttu-id="8cd30-103">Viðbótina QuickBooks gagnaflutningur</span><span class="sxs-lookup"><span data-stu-id="8cd30-103">The QuickBooks Data Migration Extension</span></span>

<span data-ttu-id="8cd30-104">Þessi viðbót auðveldar flutning viðskiptamanna, lánardrottna og vara úr QuickBooks í [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="8cd30-104">This extension makes it easy to migrate customers, vendors, items, and accounts from QuickBooks to [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="8cd30-105">Ef fyrirtækið notar QuickBooks er hægt að flytja út viðeigandi upplýsingar og opna síðan leiðarvísi fyrir uppsetningu með hjálp til að hlaða gögnunum upp í [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="8cd30-105">If your business uses QuickBooks today, you can export the relevant information and then open an assisted setup guide to upload the data to [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>  
<span data-ttu-id="8cd30-106">Nánari upplýsingar eru í [Innflutningur viðskiptagagna úr öðrum fjárhagskerfum](across-import-data-configuration-packages.md).</span><span class="sxs-lookup"><span data-stu-id="8cd30-106">For more information, see [Importing Business Data from Other Finance Systems](across-import-data-configuration-packages.md).</span></span>

## <a name="data-from-quickbooks-desktop"></a><span data-ttu-id="8cd30-107">Gögn frá QuickBooks Desktop</span><span class="sxs-lookup"><span data-stu-id="8cd30-107">Data from QuickBooks Desktop</span></span>

<span data-ttu-id="8cd30-108">Þú getur flutt inn eftirfarandi gögn úr QuickBooks Online til Business Central:</span><span class="sxs-lookup"><span data-stu-id="8cd30-108">You can import the following data from QuickBooks Online to Business Central:</span></span>

- <span data-ttu-id="8cd30-109">Viðskiptavinum</span><span class="sxs-lookup"><span data-stu-id="8cd30-109">Customers</span></span>  
- <span data-ttu-id="8cd30-110">Lánardrottnar</span><span class="sxs-lookup"><span data-stu-id="8cd30-110">Vendors</span></span>  
- <span data-ttu-id="8cd30-111">Birgðir</span><span class="sxs-lookup"><span data-stu-id="8cd30-111">Items</span></span>  
- <span data-ttu-id="8cd30-112">Bókhaldslykill</span><span class="sxs-lookup"><span data-stu-id="8cd30-112">Chart of Accounts</span></span>  
- <span data-ttu-id="8cd30-113">Upphafsstöðufærslur í fjárhagnum</span><span class="sxs-lookup"><span data-stu-id="8cd30-113">Beginning Balance transactions in General Ledger</span></span>  
- <span data-ttu-id="8cd30-114">Magn á lager fyrir birgðavörur</span><span class="sxs-lookup"><span data-stu-id="8cd30-114">On-hand Quantities for Inventory Items</span></span>  
- <span data-ttu-id="8cd30-115">Opna skjöl fyrir viðskiptamenn og lánardrottna, eins og t.d. reikningar, kreditreikningar og greiðslur</span><span class="sxs-lookup"><span data-stu-id="8cd30-115">Open documents for customers and vendors, such as invoices, credit memos and payments</span></span>  

<span data-ttu-id="8cd30-116">Við flytjum aðeins fullar upphæðir í sölu- og innkaupaskjöl.</span><span class="sxs-lookup"><span data-stu-id="8cd30-116">We migrate only full amounts on sales and purchase documents.</span></span> <span data-ttu-id="8cd30-117">Við uppfærum ekki upphæðir greiddar að hluta.</span><span class="sxs-lookup"><span data-stu-id="8cd30-117">We do not update partially paid amounts.</span></span> <span data-ttu-id="8cd30-118">Ef viðskiptamaður hefur t.d. borgað 300 af 500 dollurum á sölureikningi, flytjum við fulla upphæð eða 500.</span><span class="sxs-lookup"><span data-stu-id="8cd30-118">For example, if a customer has paid 300 of a total of 500 dollars on a sales invoice, we migrate the full 500.</span></span> <span data-ttu-id="8cd30-119">Ef þú hefur fengið greiddan hluta af greiðslum, þarf að uppfæra þær handvirkt, annað hvort áður eða eftir að þú flytur gögn.</span><span class="sxs-lookup"><span data-stu-id="8cd30-119">If you have received partial payments, you must update these manually, either before or after you migrate data.</span></span> <span data-ttu-id="8cd30-120">Við mælum með því að þú jafnir útistandandi færslur áður en þú flytur gögn, bara til þess að gera eftirleikinn auðveldari.</span><span class="sxs-lookup"><span data-stu-id="8cd30-120">We recommend that you apply outstanding transactions before you migrate, just to make things easier afterward.</span></span>

> [!NOTE]
> <span data-ttu-id="8cd30-121">Við flytjum ekki innkaupapantanir eða sölupantanir.</span><span class="sxs-lookup"><span data-stu-id="8cd30-121">We do not migrate purchase orders or sales orders.</span></span>

## <a name="before-you-start"></a><span data-ttu-id="8cd30-122">Áður en byrjað er</span><span class="sxs-lookup"><span data-stu-id="8cd30-122">Before You Start</span></span>

<span data-ttu-id="8cd30-123">Mikilvægur hluti flutningsferlisins er að tilgreina reikningana sem flytja á færslur til.</span><span class="sxs-lookup"><span data-stu-id="8cd30-123">An important part of the migration process is to specify the accounts to migrate transactions to.</span></span> <span data-ttu-id="8cd30-124">Það er tilvalið að skipuleggja vörpunina áður en þú flytur gögn.</span><span class="sxs-lookup"><span data-stu-id="8cd30-124">It's a good idea to plan this mapping before you migrate data.</span></span> <span data-ttu-id="8cd30-125">Til dæmis, reikningana sem þú bókar færslurnar fyrir:</span><span class="sxs-lookup"><span data-stu-id="8cd30-125">For example, the accounts where you post transactions for:</span></span>

- <span data-ttu-id="8cd30-126">Sala vöru eða þjónustu til viðskiptamanna</span><span class="sxs-lookup"><span data-stu-id="8cd30-126">The sale of items or services to customers</span></span>  
- <span data-ttu-id="8cd30-127">Innkaup vöru eða þjónustu frá lánardrottnum</span><span class="sxs-lookup"><span data-stu-id="8cd30-127">The purchase of items or services from vendors</span></span>  
- <span data-ttu-id="8cd30-128">Leiðréttingar í fjárhagnum</span><span class="sxs-lookup"><span data-stu-id="8cd30-128">Adjustments in the general ledger</span></span>  

<span data-ttu-id="8cd30-129">Business Central krefst þess að fjárhagsreikningum hafi verið úthlutað reikningsnúmerum.</span><span class="sxs-lookup"><span data-stu-id="8cd30-129">Business Central requires that general ledger accounts have account numbers assigned to them.</span></span> <span data-ttu-id="8cd30-130">Vertu viss um að reikningsnúmerum hafi verið úthlutað til reikninganna í QuickBooks.</span><span class="sxs-lookup"><span data-stu-id="8cd30-130">Make sure that account numbers are assigned to your accounts in QuickBooks.</span></span>
<span data-ttu-id="8cd30-131">Ef færslur í QuickBooks hafa skattaupphæðir, þarf að setja upp skattareikning fyrir þína skattalögsögu í Business Central áður en þú getur bókað færslur.</span><span class="sxs-lookup"><span data-stu-id="8cd30-131">If transactions in QuickBooks have tax amounts, you must set up a tax account for your tax jurisdictions in Business Central before you can post transactions.</span></span>

<span data-ttu-id="8cd30-132">Til þess að fá gögnin þín úr QuickBooks Desktop þarftu að hlaða niður Microsoft Data Exporter tólinu.</span><span class="sxs-lookup"><span data-stu-id="8cd30-132">In order to get your data out of the QuickBooks desktop application you will need to download the Microsoft Data Exporter Tool.</span></span>  <span data-ttu-id="8cd30-133">Leiðbeiningar fyrir tólið eru í leiðsagnarforriti fyrir gagnaflutning í [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="8cd30-133">The instructions for the tool are in the Data Migration Wizard in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="8cd30-134">Tólið mun tengjast QuickBooks-forritinu og flytja út viðeigandi gögn í .zip-skrá.</span><span class="sxs-lookup"><span data-stu-id="8cd30-134">The tool will connect to your QuickBooks application and export the applicable data to a .zip file.</span></span>  

> [!NOTE]
> <span data-ttu-id="8cd30-135">Að svo stöddu er gagnaútflutningstólið aðeins með QuickBooks 2017 og 2018.</span><span class="sxs-lookup"><span data-stu-id="8cd30-135">Currently the data exporter tool only works with QuickBooks 2017 and 2018.</span></span>

## <a name="finding-the-quickbooks-data-migration-extension"></a><span data-ttu-id="8cd30-136">Finna viðbótin QuickBooks gagnaflutningar</span><span class="sxs-lookup"><span data-stu-id="8cd30-136">Finding the QuickBooks Data Migration Extension</span></span>

<span data-ttu-id="8cd30-137">Viðbótin QuickBooks gagnaflutningar er sett upp og tilbúin til keyrslu sem samþættur hluti af Gagnaflutningar uppsetningarleiðbeiningar með aðstoð.</span><span class="sxs-lookup"><span data-stu-id="8cd30-137">The QuickBooks Data Migration extension is installed and ready to go as an integrated part of the Data Migration assisted setup guide.</span></span> <span data-ttu-id="8cd30-138">Ef þú ert tilbúinn til að byrja núna og hefur flutt út gögnin þín úr QuickBooks skaltu velja ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Uppsetning með hjálp** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="8cd30-138">If you are ready to get started now, and have exported your data from QuickBooks, choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Assisted Setup**, and then choose the related link.</span></span> <span data-ttu-id="8cd30-139">Veljið **Flytja viðskiptagögn** og fara síðan eftir skrefunum í leiðbeiningunum.</span><span class="sxs-lookup"><span data-stu-id="8cd30-139">Choose **Migrate business data**, and then follow the steps in the guide.</span></span>  

## <a name="what-do-i-do-after-i-migrate-data"></a><span data-ttu-id="8cd30-140">Hvað geri ég eftir gagnaflutninginn?</span><span class="sxs-lookup"><span data-stu-id="8cd30-140">What do I do after I migrate Data?</span></span>

<span data-ttu-id="8cd30-141">Þegar gagnaflutningi er lokið, hafa færslur stöðuna Óbókaðar, svo þú getur endurskoðað þær og gert leiðréttingar.</span><span class="sxs-lookup"><span data-stu-id="8cd30-141">After you migrate data, transactions have the status Unposted, so you can review them and make adjustments.</span></span> <span data-ttu-id="8cd30-142">Til að endurskoða færslurnar, skal farið á síðuna þar þú myndir venjulega finna þær.</span><span class="sxs-lookup"><span data-stu-id="8cd30-142">To review the transactions, go to the page where you would normally find them.</span></span> <span data-ttu-id="8cd30-143">Til dæmis, til að endurskoða óbókaða sölureikninga, skal farið á síðuna Sölureikningar.</span><span class="sxs-lookup"><span data-stu-id="8cd30-143">For example, to review unposted sales invoices, go to the Sales Invoices page.</span></span> <span data-ttu-id="8cd30-144">Til að endurskoða greiðslubækur, skal fara á síðuna Greiðslubækur.</span><span class="sxs-lookup"><span data-stu-id="8cd30-144">To review payment journals, go to the Payment Journals page.</span></span>
<span data-ttu-id="8cd30-145">Það eru einkum nokkrir hlutir sem þú þarft að gera: Ef færslurnar í QuickBooks Online höfðu breytingarmerkingar eða afsláttarupphæð, verður að bæta upphæðunum handvirkt við tengdar færslur í Business Central áður en þú bókar þær.</span><span class="sxs-lookup"><span data-stu-id="8cd30-145">There are a few things in particular that you should do: If the transactions in QuickBooks had markup or discount amounts, you must manually add the amounts to the related transactions in Business Central before you post them.</span></span>
<span data-ttu-id="8cd30-146">Ef þú ert að nota VSK, þarftu kannski að bæta viðskiptabókunarflokki og vörubókunarflokki við uppsetningu bókana svo þú getir bókað VSK upphæðir.</span><span class="sxs-lookup"><span data-stu-id="8cd30-146">If you are using value added tax (VAT), you may need to add a business posting group and a product posting group to the posting setup so that you can post VAT amounts.</span></span>
<span data-ttu-id="8cd30-147">Staðfesta upphafsstöðu reikninga í fjárhagnum.</span><span class="sxs-lookup"><span data-stu-id="8cd30-147">Verify the beginning balances for accounts in the general ledger.</span></span> <span data-ttu-id="8cd30-148">QuickBooks geymir ekki núgildandi stöðu fyrir alla reikninga, og því gætirðu þurft að leiðrétta upphafstöður.</span><span class="sxs-lookup"><span data-stu-id="8cd30-148">QuickBooks does not store the current balance for all accounts, so you might need to correct beginning balances.</span></span>

## <a name="see-also"></a><span data-ttu-id="8cd30-149">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="8cd30-149">See Also</span></span>

[<span data-ttu-id="8cd30-150">Innflutningur viðskiptagagna úr öðrum fjárhagskerfum</span><span class="sxs-lookup"><span data-stu-id="8cd30-150">Importing Business Data from Other Finance Systems</span></span>](across-import-data-configuration-packages.md)  
<span data-ttu-id="8cd30-151">[Sérstilling [!INCLUDE[prod_short](includes/prod_short.md)] með viðbótum ](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="8cd30-151">[Customizing [!INCLUDE[prod_short](includes/prod_short.md)] Using Extensions ](ui-extensions.md)</span></span>  


[!INCLUDE[footer-include](includes/footer-banner.md)]