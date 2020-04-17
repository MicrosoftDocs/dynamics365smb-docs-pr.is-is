---
title: Notkun C5 gagnaflutningsviðbótar | Microsoft Docs
description: Þessi viðbót er notuð til að flytja viðskiptamenn, lánardrottna, vörur og fjárhagsreikninga úr Microsoft Dynamics C5 2012 í Business Central.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: extension, migrate, data, C5, import
ms.date: 04/01/2020
ms.author: bholtorf
ms.openlocfilehash: cdf14002e28b777441a803fc7804fdac8afe5b77
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2020
ms.locfileid: "3194332"
---
# <a name="the-c5-data-migration-extension"></a><span data-ttu-id="7a65b-103">C5-gagnaflutningsviðbótin</span><span class="sxs-lookup"><span data-stu-id="7a65b-103">The C5 Data Migration Extension</span></span>
<span data-ttu-id="7a65b-104">Þessi viðbót auðveldar flutning viðskiptamanna, lánardrottna, vara og fjárhagsreikninga úr Microsoft Dynamics C5 2012 í [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="7a65b-104">This extension makes it easy to migrate customers, vendors, items, and your general ledger accounts from Microsoft Dynamcis C5 2012 to [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="7a65b-105">Hægt er að flytja elrdi færslur fyrir fjárhagsreikning.</span><span class="sxs-lookup"><span data-stu-id="7a65b-105">You can also migrate historical entries for general ledger accounts.</span></span>

> [!Note]
> <span data-ttu-id="7a65b-106">Fyrirtækið í [!INCLUDE[d365fin](includes/d365fin_md.md)] má ekki innihalda gögn.</span><span class="sxs-lookup"><span data-stu-id="7a65b-106">The company in [!INCLUDE[d365fin](includes/d365fin_md.md)] must not contain any data.</span></span> <span data-ttu-id="7a65b-107">Að auki skaltu ekki búa til viðskiptavini, lánardrottna, vörur eða reikninga fyrr en flutningur lýkur.</span><span class="sxs-lookup"><span data-stu-id="7a65b-107">Additionally, after you start a migration, do not create customers, vendors, items, or accounts until the migration finishes.</span></span>

## <a name="what-data-is-migrated"></a><span data-ttu-id="7a65b-108">Hvaða gögn eru flutt?</span><span class="sxs-lookup"><span data-stu-id="7a65b-108">What Data is Migrated?</span></span>
<span data-ttu-id="7a65b-109">Eftirfarandi gögn eru flutt fyrir hverja einingu:</span><span class="sxs-lookup"><span data-stu-id="7a65b-109">The following data is migrated for each entity:</span></span>

<span data-ttu-id="7a65b-110">**Viðskiptavinum**</span><span class="sxs-lookup"><span data-stu-id="7a65b-110">**Customers**</span></span>
* <span data-ttu-id="7a65b-111">Tengiliður</span><span class="sxs-lookup"><span data-stu-id="7a65b-111">Contacts</span></span>  
* <span data-ttu-id="7a65b-112">Birgðageymsla</span><span class="sxs-lookup"><span data-stu-id="7a65b-112">Location</span></span>
* <span data-ttu-id="7a65b-113">Land</span><span class="sxs-lookup"><span data-stu-id="7a65b-113">Country</span></span>
* <span data-ttu-id="7a65b-114">Vídd viðskiptavina (deild, miðstöð, tilgangur)</span><span class="sxs-lookup"><span data-stu-id="7a65b-114">Customer dimensions (department, center, purpose)</span></span>
* <span data-ttu-id="7a65b-115">Afhendingarmáti</span><span class="sxs-lookup"><span data-stu-id="7a65b-115">Shipment method</span></span>
* <span data-ttu-id="7a65b-116">Sölumaður</span><span class="sxs-lookup"><span data-stu-id="7a65b-116">Sales Person</span></span>
* <span data-ttu-id="7a65b-117">Greiðsluskilmálar</span><span class="sxs-lookup"><span data-stu-id="7a65b-117">Payment terms</span></span>
* <span data-ttu-id="7a65b-118">Greiðslumáti</span><span class="sxs-lookup"><span data-stu-id="7a65b-118">Payment method</span></span>
* <span data-ttu-id="7a65b-119">Verðflokkur viðskiptamanns</span><span class="sxs-lookup"><span data-stu-id="7a65b-119">Customer price group</span></span>
* <span data-ttu-id="7a65b-120">Reikningsafsláttur viðskiptavinar</span><span class="sxs-lookup"><span data-stu-id="7a65b-120">Customer invoice discount</span></span>

<span data-ttu-id="7a65b-121">Ef reikningar eru fluttir eru eftirfarandi gögn einnig flutt:</span><span class="sxs-lookup"><span data-stu-id="7a65b-121">If you migrate accounts, the following data is also migrated:</span></span>

* <span data-ttu-id="7a65b-122">Uppsetning bókunar viðskiptavinar</span><span class="sxs-lookup"><span data-stu-id="7a65b-122">Customer posting setup</span></span>
* <span data-ttu-id="7a65b-123">Almenn færslubókarkeyrsla</span><span class="sxs-lookup"><span data-stu-id="7a65b-123">General journal batch</span></span>
* <span data-ttu-id="7a65b-124">Opnar færslur (í viðskiptamannabók)</span><span class="sxs-lookup"><span data-stu-id="7a65b-124">Open transactions (customer ledger entries)</span></span>

<span data-ttu-id="7a65b-125">**Lánardrottnar**</span><span class="sxs-lookup"><span data-stu-id="7a65b-125">**Vendors**</span></span>
* <span data-ttu-id="7a65b-126">Tengiliður</span><span class="sxs-lookup"><span data-stu-id="7a65b-126">Contacts</span></span>
* <span data-ttu-id="7a65b-127">Birgðageymsla</span><span class="sxs-lookup"><span data-stu-id="7a65b-127">Location</span></span>
* <span data-ttu-id="7a65b-128">Land</span><span class="sxs-lookup"><span data-stu-id="7a65b-128">Country</span></span>
* <span data-ttu-id="7a65b-129">Vídd lánardrottins (deild, miðstöð, tilgangur)</span><span class="sxs-lookup"><span data-stu-id="7a65b-129">Vendor dimensions (department, center, purpose)</span></span>
* <span data-ttu-id="7a65b-130">Reikningsafsláttur</span><span class="sxs-lookup"><span data-stu-id="7a65b-130">Invoice discount</span></span>
* <span data-ttu-id="7a65b-131">Afhendingarmáti</span><span class="sxs-lookup"><span data-stu-id="7a65b-131">Shipment method</span></span>
* <span data-ttu-id="7a65b-132">Innkaupaaðili</span><span class="sxs-lookup"><span data-stu-id="7a65b-132">Purchaser</span></span>
* <span data-ttu-id="7a65b-133">Greiðsluskilmálar</span><span class="sxs-lookup"><span data-stu-id="7a65b-133">Payment terms</span></span>
* <span data-ttu-id="7a65b-134">Greiðslumáti</span><span class="sxs-lookup"><span data-stu-id="7a65b-134">Payment method</span></span>
* <span data-ttu-id="7a65b-135">Afsláttur lánardrottnareikninga</span><span class="sxs-lookup"><span data-stu-id="7a65b-135">Vendor invoice discount</span></span>

<span data-ttu-id="7a65b-136">Ef reikningar eru fluttir eru eftirfarandi gögn einnig flutt:</span><span class="sxs-lookup"><span data-stu-id="7a65b-136">If you migrate accounts, the following data is also migrated:</span></span>

* <span data-ttu-id="7a65b-137">Bókunarflokkur lánardrottins</span><span class="sxs-lookup"><span data-stu-id="7a65b-137">Vendor posting setup</span></span>
* <span data-ttu-id="7a65b-138">Almenn færslubókarkeyrsla</span><span class="sxs-lookup"><span data-stu-id="7a65b-138">General journal batch</span></span>
* <span data-ttu-id="7a65b-139">Opnar færslur (fjárhagsfærslur lánardrottins)</span><span class="sxs-lookup"><span data-stu-id="7a65b-139">Open transactions (vendor ledger entries)</span></span>

<span data-ttu-id="7a65b-140">**Birgðir**</span><span class="sxs-lookup"><span data-stu-id="7a65b-140">**Items**</span></span>
* <span data-ttu-id="7a65b-141">Birgðageymsla</span><span class="sxs-lookup"><span data-stu-id="7a65b-141">Location</span></span>
* <span data-ttu-id="7a65b-142">Land</span><span class="sxs-lookup"><span data-stu-id="7a65b-142">Country</span></span>
* <span data-ttu-id="7a65b-143">Vöruvíddir (deild, miðstöð, tilgangur)</span><span class="sxs-lookup"><span data-stu-id="7a65b-143">Item dimensions (department, center, purpose)</span></span>
* <span data-ttu-id="7a65b-144">Sölulínuafslættir</span><span class="sxs-lookup"><span data-stu-id="7a65b-144">Sales line discounts</span></span>
* <span data-ttu-id="7a65b-145">Afsláttarflokkar viðskiptamanna</span><span class="sxs-lookup"><span data-stu-id="7a65b-145">Customer discount groups</span></span>
* <span data-ttu-id="7a65b-146">Vöruafsláttarflokkar</span><span class="sxs-lookup"><span data-stu-id="7a65b-146">Item discount groups</span></span>
* <span data-ttu-id="7a65b-147">Söluverð</span><span class="sxs-lookup"><span data-stu-id="7a65b-147">Sales price</span></span>
* <span data-ttu-id="7a65b-148">Tollnúmer</span><span class="sxs-lookup"><span data-stu-id="7a65b-148">Tariff number</span></span>
* <span data-ttu-id="7a65b-149">Mælieiningar</span><span class="sxs-lookup"><span data-stu-id="7a65b-149">Units of measure</span></span>
* <span data-ttu-id="7a65b-150">Vörurakningarkóti</span><span class="sxs-lookup"><span data-stu-id="7a65b-150">Item tracking code</span></span>
* <span data-ttu-id="7a65b-151">Verðflokkur viðskiptamanns</span><span class="sxs-lookup"><span data-stu-id="7a65b-151">Customer price group</span></span>
* <span data-ttu-id="7a65b-152">Samsetningaruppskrift</span><span class="sxs-lookup"><span data-stu-id="7a65b-152">Assembly BOMs</span></span>

<span data-ttu-id="7a65b-153">Ef reikningar eru fluttir eru eftirfarandi gögn einnig flutt:</span><span class="sxs-lookup"><span data-stu-id="7a65b-153">If you migrate accounts, the following data is also migrated:</span></span>

* <span data-ttu-id="7a65b-154">Birgðabókunargrunnur</span><span class="sxs-lookup"><span data-stu-id="7a65b-154">Inventory posting setup</span></span>
* <span data-ttu-id="7a65b-155">Almennur bókunargrunnur</span><span class="sxs-lookup"><span data-stu-id="7a65b-155">General posting setup</span></span>
* <span data-ttu-id="7a65b-156">Birgðabókarkeyrsla</span><span class="sxs-lookup"><span data-stu-id="7a65b-156">Item journal batch</span></span>
* <span data-ttu-id="7a65b-157">Opnar færslur (birgðafærslur)</span><span class="sxs-lookup"><span data-stu-id="7a65b-157">Open transactions (item ledger entries)</span></span>

> [!Note]
> <span data-ttu-id="7a65b-158">Ef opnar færslur eru til staðar sem nota erlenda gjaldmiðla er gengi þeirra einnig flutt inn.</span><span class="sxs-lookup"><span data-stu-id="7a65b-158">If there are open transactions that use foreign currencies, the exchange rates for those currencies are also migrated.</span></span> <span data-ttu-id="7a65b-159">Önnur gengi eru ekki flutt inn.</span><span class="sxs-lookup"><span data-stu-id="7a65b-159">Other exchange rates are not migrated.</span></span>

<span data-ttu-id="7a65b-160">**Bókhaldslykill**</span><span class="sxs-lookup"><span data-stu-id="7a65b-160">**Chart of Accounts**</span></span>  
* <span data-ttu-id="7a65b-161">Staðlaðar víddir: Deild, kostnaðarstaður, tilgangur</span><span class="sxs-lookup"><span data-stu-id="7a65b-161">Standard dimensions: Department, Cost Center, Purpose</span></span>  
* <span data-ttu-id="7a65b-162">Sögulegar fjárhagsfærslur</span><span class="sxs-lookup"><span data-stu-id="7a65b-162">Historical G/L transactions</span></span>  

> [!Note]
> <span data-ttu-id="7a65b-163">Sögulegar fjárhagsfærslur eru meðhöndlaðir aðeins öðruvísi.</span><span class="sxs-lookup"><span data-stu-id="7a65b-163">Historical G/L transactions are treated a little differently.</span></span> <span data-ttu-id="7a65b-164">Þegar þú flytur gögn stillirðu færibreytuna **Núverandi tímabil**.</span><span class="sxs-lookup"><span data-stu-id="7a65b-164">When you migrate data you set a **Current Period** parameter.</span></span> <span data-ttu-id="7a65b-165">Þessi færibreyta tilgreinir hvernig á að vinna úr fjárhagsfærslum.</span><span class="sxs-lookup"><span data-stu-id="7a65b-165">This parameter specifies how to process G/L transactions.</span></span> <span data-ttu-id="7a65b-166">Færslur eftir þessa dagsetningu eru fluttar hver fyrir sig.</span><span class="sxs-lookup"><span data-stu-id="7a65b-166">Transactions after this date are migrated individually.</span></span> <span data-ttu-id="7a65b-167">Færslum fyrir þessa dagsetningu er safnað saman fyrir hvern reikning og fluttar sem ein upphæð.</span><span class="sxs-lookup"><span data-stu-id="7a65b-167">Transactions before this date are aggregated per account and migrated as a single amount.</span></span> <span data-ttu-id="7a65b-168">Segjum sem dæmi að það séu færslur á árunum 2015, 2016, 2017, 2018 og þú tilgreinir 1. janúar 2017 í reit núverandi tímabils.</span><span class="sxs-lookup"><span data-stu-id="7a65b-168">For example, let's say there are transactions in 2015, 2016, 2017, 2018, and you specify January 01, 2017 in the Current Period field.</span></span> <span data-ttu-id="7a65b-169">Fyrir hvern reikning verður upphæðum fyrir færslur á eða fyrir 31. desember 2016 safnað saman í eina færslubókarlínu fyrir hverja fjárhagsfærslu.</span><span class="sxs-lookup"><span data-stu-id="7a65b-169">For each account, amounts for transactions on or before December 31, 2106, will be aggregated in a single general journal line for each G/L account.</span></span> <span data-ttu-id="7a65b-170">Allar færslur eftir þennan dag verða fluttar hver fyrir sig.</span><span class="sxs-lookup"><span data-stu-id="7a65b-170">All trascations after this date will be migrated individually.</span></span>

## <a name="file-size-requirements"></a><span data-ttu-id="7a65b-171">Kröfur um skráarstærð</span><span class="sxs-lookup"><span data-stu-id="7a65b-171">File Size Requirements</span></span>
<span data-ttu-id="7a65b-172">Stærsta skráin sem þú getur hlaðið upp til [!INCLUDE[d365fin](includes/d365fin_md.md)] er 150 MB.</span><span class="sxs-lookup"><span data-stu-id="7a65b-172">The largest file size you can upload to [!INCLUDE[d365fin](includes/d365fin_md.md)] is 150 MB.</span></span> <span data-ttu-id="7a65b-173">Ef skráin sem þú ert að flytja út úr C5 er stærri en það, skaltu íhuga að flytja gögn í mörgum skrám.</span><span class="sxs-lookup"><span data-stu-id="7a65b-173">If the file you export from C5 is larger than that, consider migrating data in multiple files.</span></span> <span data-ttu-id="7a65b-174">Til dæmis, flytja eina eða tvær gerðir eininga úr C5, svo sem viðskiptavinum og lánardrottnum, í skrá, og síðan flytja út hluti í annarri skrá, og svo framvegis.</span><span class="sxs-lookup"><span data-stu-id="7a65b-174">For example, export one or two types of entities from C5, such as customers and vendors, to a file, and then export items to another file, and so on.</span></span> <span data-ttu-id="7a65b-175">Hægt er að flytja inn skrár hver í sínu lagi í [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="7a65b-175">You can import files individually in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

## <a name="to-migrate-data"></a><span data-ttu-id="7a65b-176">Til að flytja gögn</span><span class="sxs-lookup"><span data-stu-id="7a65b-176">To migrate data</span></span>
<span data-ttu-id="7a65b-177">Það eru aðeins nokkur skref fólgin í því að flytja út gögn úr C5 og flytja þau inn í [!INCLUDE[d365fin](includes/d365fin_md.md)]:</span><span class="sxs-lookup"><span data-stu-id="7a65b-177">There are just a few steps to export data from C5, and import it in [!INCLUDE[d365fin](includes/d365fin_md.md)]:</span></span>  

1. <span data-ttu-id="7a65b-178">Í C5 skaltu nota **Flytja út gagnagrunn** eiginleikann til að flytja út gögnin.</span><span class="sxs-lookup"><span data-stu-id="7a65b-178">In C5, use the **Export Database** feature to export the data.</span></span> <span data-ttu-id="7a65b-179">Sendu síðan útflutningsmöppuna í þappaða möppu.</span><span class="sxs-lookup"><span data-stu-id="7a65b-179">Then send the export folder to a compressed (zipped) folder.</span></span>  
2. <span data-ttu-id="7a65b-180">Í [!INCLUDE[d365fin](includes/d365fin_md.md)], veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Gagnaflutningur** og veldu síðan **Gagnaflutningur**.</span><span class="sxs-lookup"><span data-stu-id="7a65b-180">In [!INCLUDE[d365fin](includes/d365fin_md.md)], choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Data Migration**, and then choose **Data Migration**.</span></span>  
3. <span data-ttu-id="7a65b-181">Ljúka skal skrefunum í leiðbeiningum um uppsetningu með hjálp.</span><span class="sxs-lookup"><span data-stu-id="7a65b-181">Complete the steps in the assisted setup guide.</span></span> <span data-ttu-id="7a65b-182">Gakktu úr skugga um að velja **Flytja inn úr Microsoft Dynamcis C5 2012** sem gagnagjafa.</span><span class="sxs-lookup"><span data-stu-id="7a65b-182">Make sure to choose **Import from Microsoft Dynamcis C5 2012** as the data source.</span></span>  

## <a name="viewing-the-status-of-the-migration"></a><span data-ttu-id="7a65b-183">Skoðun stöðu á flutningi</span><span class="sxs-lookup"><span data-stu-id="7a65b-183">Viewing the Status of the Migration</span></span>
<span data-ttu-id="7a65b-184">Nota skal síðuna **Gagnaflutningsyfirlit** til að sjá stöðu flutningsins.</span><span class="sxs-lookup"><span data-stu-id="7a65b-184">Use the **Data Migration Overview** page to monitor the success of the migration.</span></span> <span data-ttu-id="7a65b-185">Síðan sýnir upplýsingar, svo sem fjöldi færslna sem flutningurinn mun innihalda, stöðu flutningsins og fjölda vara sem hafa verið fluttar og hvort flutningur þeirra tókst.</span><span class="sxs-lookup"><span data-stu-id="7a65b-185">The page shows information such as the number of entities that the migration will include, the status of the migration, and the number of items that have been migrated and whether they were successfull.</span></span> <span data-ttu-id="7a65b-186">Hún sýnir einnig fjölda villna, gerir þér kleift að rannsaka hvað fór úrskeiðis og, þegar mögulegt er, auðveldar það að fara í færsluna til að laga vandamálin.</span><span class="sxs-lookup"><span data-stu-id="7a65b-186">It also shows the number of errors, lets you investigate what went wrong and, when possible, makes it easy to go to the entity to fix the issues.</span></span> <span data-ttu-id="7a65b-187">Nánari upplýsingar eru í næsta hluta þessa efnisatriðis.</span><span class="sxs-lookup"><span data-stu-id="7a65b-187">For more information, see the next section in this topic.</span></span>  

> [!Note]
> <span data-ttu-id="7a65b-188">Meðan beðið er eftir stöðu flutningsins þarf að uppfæra síðuna til að birta niðurstöðurnar.</span><span class="sxs-lookup"><span data-stu-id="7a65b-188">While you are waiting for the results of the migration, you must refresh the page to display the results.</span></span>

## <a name="how-to-avoid-double-posting"></a><span data-ttu-id="7a65b-189">Hvernig á að koma í veg fyrir tvíbókun</span><span class="sxs-lookup"><span data-stu-id="7a65b-189">How to Avoid Double-Posting</span></span>
<span data-ttu-id="7a65b-190">Til að koma í veg fyrir tvíbókanir í fjárhagnum eru eftirfarandi mótreikningar notaðir fyrir opnar færslur:</span><span class="sxs-lookup"><span data-stu-id="7a65b-190">To help avoid double-posting to the general ledger, the following balance accounts are used for open transactions:</span></span>  

* <span data-ttu-id="7a65b-191">Fyrir lánardrottna notum við viðskiptaskuldareikninginn frá bókunarflokki lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="7a65b-191">For vendors, we use the A/P account from the vendor posting group.</span></span>  
* <span data-ttu-id="7a65b-192">Fyrir viðskiptavini notum við viðskiptakröfureikninginn frá bókunarflokki viðskiptavinar.</span><span class="sxs-lookup"><span data-stu-id="7a65b-192">For customers, we use the A/R account from the customer posting group.</span></span>  
* <span data-ttu-id="7a65b-193">Fyrir vörur búum við til almennan bókunargrunn þar sem leiðréttingarreikningurinn er reikningurinn sem er tilgreindur sem birgðarreikningur í birgðabókunargrunni.</span><span class="sxs-lookup"><span data-stu-id="7a65b-193">For items, we create a general posting setup where the adjustment account is the account specified as the inventory account on the inventory posting setup.</span></span>  

## <a name="correcting-errors"></a><span data-ttu-id="7a65b-194">Leiðrétting villna</span><span class="sxs-lookup"><span data-stu-id="7a65b-194">Correcting Errors</span></span>
<span data-ttu-id="7a65b-195">Ef eitthvað fer úrskeiðis og villur koma upp sýnir **Staða** reiturinn **Lokið með villum** og **Villutalning** reiturinn mun sýna fjöldann.</span><span class="sxs-lookup"><span data-stu-id="7a65b-195">If something goes wrong and an error occurs, the **Status** field will show **Completed with Errors**, and the **Error Count** field will show how many.</span></span> <span data-ttu-id="7a65b-196">Til að skoða lista yfir villurnar er hægt að opna **Villur í gagnaflutningi** síðuna með því að velja:</span><span class="sxs-lookup"><span data-stu-id="7a65b-196">To view a list of the errors, you can open the **Data Migration Errors** page by choosing:</span></span>  

* <span data-ttu-id="7a65b-197">Talan í **Villutalning** reitnum fyrir eininguna.</span><span class="sxs-lookup"><span data-stu-id="7a65b-197">The number in the **Error Count** field for the entity.</span></span>  
* <span data-ttu-id="7a65b-198">Einingin og svo **Sýna villur** aðgerðin.</span><span class="sxs-lookup"><span data-stu-id="7a65b-198">The entity, and then the **Show Errors** action.</span></span>  

<span data-ttu-id="7a65b-199">Á síðunni **Villur í gagnaflutningi**, til að laga villa getur þú valið villuboð, og síðan velja **Breyta skrá** til að skoða gögn sem flutt voru fyrir eininguna.</span><span class="sxs-lookup"><span data-stu-id="7a65b-199">On the **Data Migration Errors** page, to fix an error you can choose an error message, and then choose **Edit Record** to view the migrated data for the entity.</span></span> <span data-ttu-id="7a65b-200">Ef þú hefur nokkrar villur til að laga, getur þú valið **Magnlagfæringar á villum** til að breyta einingum í lista.</span><span class="sxs-lookup"><span data-stu-id="7a65b-200">If you have several errors to fix, you can choose **Bulk-Fix Errors** to edit the entities in a list.</span></span> <span data-ttu-id="7a65b-201">Þú þarft samt að opna stakar skrár ef villan stafaði af tengdum færslu.</span><span class="sxs-lookup"><span data-stu-id="7a65b-201">You still need to open individual records if the error was caused by a related entry though.</span></span> <span data-ttu-id="7a65b-202">Til dæmis verður lánardrottinn ekki fluttur ef netfang eitt af tengiliðum þeirra hefur ógilt snið.</span><span class="sxs-lookup"><span data-stu-id="7a65b-202">For example, a vendor will not be migrated if an email address one of their contacts has an invalid format.</span></span>

<span data-ttu-id="7a65b-203">Eftir að þú hefur lagað eina eða fleiri villur getur þú valið **Flytja** til að flytja aðeins einingarnar sem þú lagaðir án þess að þurfa að hefja flutninginn aftur.</span><span class="sxs-lookup"><span data-stu-id="7a65b-203">After you fix one or more errors, you can choose **Migrate** to migrate only the entities you fixed, without having to completely restart the migration.</span></span>  

> [!Tip]
> <span data-ttu-id="7a65b-204">Ef þú hefur lagað fleiri en eina villu geturðu notað **Velja fleira** valkostinn til að velja margar línur til að flytja.</span><span class="sxs-lookup"><span data-stu-id="7a65b-204">If you have fixed more than one error, you can use the **Select More** feature to select multiple lines to migrate.</span></span> <span data-ttu-id="7a65b-205">Ef villur eru til staðar sem ekki er mikilvægt að laga geturðu valið þær og svo **Sleppa vali**.</span><span class="sxs-lookup"><span data-stu-id="7a65b-205">Alternatively, if there are errors that are not important to fix, you can choose them and then choose **Skip Selections**.</span></span>

> [!Note]
> <span data-ttu-id="7a65b-206">Ef vörur eru til staðar sem er að finna í uppskrift gætir þú þurft að flytja oftar en einu sinni ef upprunalega varan er ekki stofnuð fyrir afbrigðið sem vísa til hennar.</span><span class="sxs-lookup"><span data-stu-id="7a65b-206">If you have items that are included in a BOM, you might need to migrate more than once if the original item is not created before the variants that reference it.</span></span> <span data-ttu-id="7a65b-207">Ef afbrigðið er búið til fyrst getur tilvísunin í upprunalegu vöruna valdið villuboðum.</span><span class="sxs-lookup"><span data-stu-id="7a65b-207">If an item variant is created first, the reference to the original item can cause an error message.</span></span>  

## <a name="verifying-data-after-migrating"></a><span data-ttu-id="7a65b-208">Staðfesting gagna eftir flutning</span><span class="sxs-lookup"><span data-stu-id="7a65b-208">Verifying Data After Migrating</span></span>
<span data-ttu-id="7a65b-209">Ein leið til að sannreyna að gögnin hafi verið rétt flutt inn er með því að skoða eftirfarandi síður í C5 og [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="7a65b-209">One way to verify that your data migrated correctly is to look at the following pages in C5 and [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

|<span data-ttu-id="7a65b-210">Microsoft Dynamcis C5 2012</span><span class="sxs-lookup"><span data-stu-id="7a65b-210">Microsoft Dynamcis C5 2012</span></span> | [!INCLUDE[d365fin](includes/d365fin_md.md)]| <span data-ttu-id="7a65b-211">Runuvinnsla sem á að nota</span><span class="sxs-lookup"><span data-stu-id="7a65b-211">Batch Job to Use</span></span> |
|-----|-----|-----|
|<span data-ttu-id="7a65b-212">Viðskm.færslur</span><span class="sxs-lookup"><span data-stu-id="7a65b-212">Customer Entries</span></span>| <span data-ttu-id="7a65b-213">Almennar færslubækur</span><span class="sxs-lookup"><span data-stu-id="7a65b-213">General Journals</span></span>| <span data-ttu-id="7a65b-214">CUSTMIGR</span><span class="sxs-lookup"><span data-stu-id="7a65b-214">CUSTMIGR</span></span> |
|<span data-ttu-id="7a65b-215">Lánardr.færslur</span><span class="sxs-lookup"><span data-stu-id="7a65b-215">Vendor Entries</span></span>| <span data-ttu-id="7a65b-216">Almennar færslubækur</span><span class="sxs-lookup"><span data-stu-id="7a65b-216">General Journals</span></span>| <span data-ttu-id="7a65b-217">VENDMIGR</span><span class="sxs-lookup"><span data-stu-id="7a65b-217">VENDMIGR</span></span>|
|<span data-ttu-id="7a65b-218">Birgðafærslur</span><span class="sxs-lookup"><span data-stu-id="7a65b-218">Item Entries</span></span>| <span data-ttu-id="7a65b-219">Birgðabækur</span><span class="sxs-lookup"><span data-stu-id="7a65b-219">Item Journals</span></span>| <span data-ttu-id="7a65b-220">ITEMMIGR</span><span class="sxs-lookup"><span data-stu-id="7a65b-220">ITEMMIGR</span></span> |
|<span data-ttu-id="7a65b-221">Fjárhagsfærslur</span><span class="sxs-lookup"><span data-stu-id="7a65b-221">G/L Entries</span></span>| <span data-ttu-id="7a65b-222">Almennar færslubækur</span><span class="sxs-lookup"><span data-stu-id="7a65b-222">General Journals</span></span>| <span data-ttu-id="7a65b-223">GLACMIGR</span><span class="sxs-lookup"><span data-stu-id="7a65b-223">GLACMIGR</span></span> |

## <a name="stopping-data-migration"></a><span data-ttu-id="7a65b-224">Stöðvun gagnaflutnings</span><span class="sxs-lookup"><span data-stu-id="7a65b-224">Stopping Data Migration</span></span>
<span data-ttu-id="7a65b-225">Þú getur hætt að flytja gögn með því að velja **Hætta við allan flutning**.</span><span class="sxs-lookup"><span data-stu-id="7a65b-225">You can stop migrating data by choosing **Stop All Migrations**.</span></span> <span data-ttu-id="7a65b-226">Ef þú gerir það er líka hætt við allan flutning sem bíður.</span><span class="sxs-lookup"><span data-stu-id="7a65b-226">If you do, all pending migrations are also stopped.</span></span>

## <a name="see-also"></a><span data-ttu-id="7a65b-227">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="7a65b-227">See Also</span></span>
<span data-ttu-id="7a65b-228">[Sérstilling [!INCLUDE[d365fin](includes/d365fin_md.md)] með viðbótum](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="7a65b-228">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions](ui-extensions.md)</span></span>  
[<span data-ttu-id="7a65b-229">Hafist handa</span><span class="sxs-lookup"><span data-stu-id="7a65b-229">Getting Started</span></span>](product-get-started.md)
