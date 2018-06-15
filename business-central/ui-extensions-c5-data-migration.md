---
title: "Notkun C5 gagnaflutningsviðbótar | Microsoft Docs"
description: "Þessi viðbót er notuð til að flytja viðskiptamenn, lánardrottna, vörur og fjárhagsreikninga úr Microsoft Dynamics C5 2012 í Business Central."
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: extension, migrate, data, C5, import
ms.date: 04/09/208
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: fa6779ee8fb2bbb453014e32cb7f3cf8dcfa18da
ms.openlocfilehash: 698bde6949c6053501881d07135586810fc81bdd
ms.contentlocale: is-is
ms.lasthandoff: 04/11/2018

---

# <a name="the-c5-data-migration-extension-for-business-central"></a><span data-ttu-id="2ac87-103">C5 gagnaflutningsviðbót fyrir Business Central</span><span class="sxs-lookup"><span data-stu-id="2ac87-103">The C5 Data Migration Extension for Business Central</span></span>
<span data-ttu-id="2ac87-104">Þessi viðbót auðveldar flutning viðskiptamanna, lánardrottna, vara og fjárhagsreikninga úr Microsoft Dynamics C5 2012 í [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="2ac87-104">This extension makes it easy to migrate customers, vendors, items, and your general ledger accounts from Microsoft Dynamcis C5 2012 to [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="2ac87-105">Hægt er að flytja elrdi færslur fyrir fjárhagsreikning.</span><span class="sxs-lookup"><span data-stu-id="2ac87-105">You can also migrate historical entries for general ledger accounts.</span></span>

> [!Note]
> <span data-ttu-id="2ac87-106">Fyrirtækið í [!INCLUDE[d365fin](includes/d365fin_md.md)] má ekki innihalda gögn.</span><span class="sxs-lookup"><span data-stu-id="2ac87-106">The company in [!INCLUDE[d365fin](includes/d365fin_md.md)] must not contain any data.</span></span> <span data-ttu-id="2ac87-107">Að auki skaltu ekki búa til viðskiptavini, lánardrottna, vörur eða reikninga fyrr en flutningur lýkur.</span><span class="sxs-lookup"><span data-stu-id="2ac87-107">Additionally, after you start a migration, do not create customers, vendors, items, or accounts until the migration finishes.</span></span>

## <a name="what-data-is-migrated"></a><span data-ttu-id="2ac87-108">Hvaða gögn eru flutt?</span><span class="sxs-lookup"><span data-stu-id="2ac87-108">What Data is Migrated?</span></span>
<span data-ttu-id="2ac87-109">Eftirfarandi gögn eru flutt fyrir hverja einingu:</span><span class="sxs-lookup"><span data-stu-id="2ac87-109">The following data is migrated for each entity:</span></span>

<span data-ttu-id="2ac87-110">**Viðskiptavinum**</span><span class="sxs-lookup"><span data-stu-id="2ac87-110">**Customers**</span></span>
* <span data-ttu-id="2ac87-111">Birgðageymsla</span><span class="sxs-lookup"><span data-stu-id="2ac87-111">Location</span></span>
* <span data-ttu-id="2ac87-112">Land</span><span class="sxs-lookup"><span data-stu-id="2ac87-112">Country</span></span>
* <span data-ttu-id="2ac87-113">Vídd viðskiptavina (deild, miðstöð, tilgangur)</span><span class="sxs-lookup"><span data-stu-id="2ac87-113">Customer dimensions (department, center, purpose)</span></span>
* <span data-ttu-id="2ac87-114">Afhendingarmáti</span><span class="sxs-lookup"><span data-stu-id="2ac87-114">Shipment method</span></span>
* <span data-ttu-id="2ac87-115">Sölumaður</span><span class="sxs-lookup"><span data-stu-id="2ac87-115">Sales Person</span></span>
* <span data-ttu-id="2ac87-116">Greiðsluskilmálar</span><span class="sxs-lookup"><span data-stu-id="2ac87-116">Payment terms</span></span>
* <span data-ttu-id="2ac87-117">Greiðslumáti</span><span class="sxs-lookup"><span data-stu-id="2ac87-117">Payment method</span></span>
* <span data-ttu-id="2ac87-118">Verðflokkur viðskiptamanns</span><span class="sxs-lookup"><span data-stu-id="2ac87-118">Customer price group</span></span>
* <span data-ttu-id="2ac87-119">Reikningsafsláttur viðskiptavinar</span><span class="sxs-lookup"><span data-stu-id="2ac87-119">Customer invoice discount</span></span>

<span data-ttu-id="2ac87-120">Ef reikningar eru fluttir eru eftirfarandi gögn einnig flutt:</span><span class="sxs-lookup"><span data-stu-id="2ac87-120">If you migrate accounts, the following data is also migrated:</span></span>

* <span data-ttu-id="2ac87-121">Uppsetning bókunar viðskiptavinar</span><span class="sxs-lookup"><span data-stu-id="2ac87-121">Customer posting setup</span></span>
* <span data-ttu-id="2ac87-122">Almenn færslubókarkeyrsla</span><span class="sxs-lookup"><span data-stu-id="2ac87-122">General journal batch</span></span>
* <span data-ttu-id="2ac87-123">Opnar færslur (í viðskiptamannabók)</span><span class="sxs-lookup"><span data-stu-id="2ac87-123">Open transactions (customer ledger entries)</span></span>

<span data-ttu-id="2ac87-124">**Lánardrottnar**</span><span class="sxs-lookup"><span data-stu-id="2ac87-124">**Vendors**</span></span>
* <span data-ttu-id="2ac87-125">Birgðageymsla</span><span class="sxs-lookup"><span data-stu-id="2ac87-125">Location</span></span>
* <span data-ttu-id="2ac87-126">Land</span><span class="sxs-lookup"><span data-stu-id="2ac87-126">Country</span></span>
* <span data-ttu-id="2ac87-127">Vídd lánardrottins (deild, miðstöð, tilgangur)</span><span class="sxs-lookup"><span data-stu-id="2ac87-127">Vendor dimensions (department, center, purpose)</span></span>
* <span data-ttu-id="2ac87-128">Reikningsafsláttur</span><span class="sxs-lookup"><span data-stu-id="2ac87-128">Invoice discount</span></span>
* <span data-ttu-id="2ac87-129">Afhendingarmáti</span><span class="sxs-lookup"><span data-stu-id="2ac87-129">Shipment method</span></span>
* <span data-ttu-id="2ac87-130">Innkaupaaðili</span><span class="sxs-lookup"><span data-stu-id="2ac87-130">Purchaser</span></span>
* <span data-ttu-id="2ac87-131">Greiðsluskilmálar</span><span class="sxs-lookup"><span data-stu-id="2ac87-131">Payment terms</span></span>
* <span data-ttu-id="2ac87-132">Greiðslumáti</span><span class="sxs-lookup"><span data-stu-id="2ac87-132">Payment method</span></span>
* <span data-ttu-id="2ac87-133">Afsláttur lánardrottnareikninga</span><span class="sxs-lookup"><span data-stu-id="2ac87-133">Vendor invoice discount</span></span>

<span data-ttu-id="2ac87-134">Ef reikningar eru fluttir eru eftirfarandi gögn einnig flutt:</span><span class="sxs-lookup"><span data-stu-id="2ac87-134">If you migrate accounts, the following data is also migrated:</span></span>

* <span data-ttu-id="2ac87-135">Bókunarflokkur lánardrottins</span><span class="sxs-lookup"><span data-stu-id="2ac87-135">Vendor posting setup</span></span>
* <span data-ttu-id="2ac87-136">Almenn færslubókarkeyrsla</span><span class="sxs-lookup"><span data-stu-id="2ac87-136">General journal batch</span></span>
* <span data-ttu-id="2ac87-137">Opnar færslur (fjárhagsfærslur lánardrottins)</span><span class="sxs-lookup"><span data-stu-id="2ac87-137">Open transactions (vendor ledger entries)</span></span>

<span data-ttu-id="2ac87-138">**Birgðir**</span><span class="sxs-lookup"><span data-stu-id="2ac87-138">**Items**</span></span>
* <span data-ttu-id="2ac87-139">Birgðageymsla</span><span class="sxs-lookup"><span data-stu-id="2ac87-139">Location</span></span>
* <span data-ttu-id="2ac87-140">Land</span><span class="sxs-lookup"><span data-stu-id="2ac87-140">Country</span></span>
* <span data-ttu-id="2ac87-141">Vöruvíddir (deild, miðstöð, tilgangur)</span><span class="sxs-lookup"><span data-stu-id="2ac87-141">Item dimensions (department, center, purpose)</span></span>
* <span data-ttu-id="2ac87-142">Sölulínuafslættir</span><span class="sxs-lookup"><span data-stu-id="2ac87-142">Sales line discounts</span></span>
* <span data-ttu-id="2ac87-143">Afsláttarflokkar viðskiptamanna</span><span class="sxs-lookup"><span data-stu-id="2ac87-143">Customer discount groups</span></span>
* <span data-ttu-id="2ac87-144">Vöruafsláttarflokkar</span><span class="sxs-lookup"><span data-stu-id="2ac87-144">Item discount groups</span></span>
* <span data-ttu-id="2ac87-145">Söluverð</span><span class="sxs-lookup"><span data-stu-id="2ac87-145">Sales price</span></span>
* <span data-ttu-id="2ac87-146">Tollnúmer</span><span class="sxs-lookup"><span data-stu-id="2ac87-146">Tariff number</span></span>
* <span data-ttu-id="2ac87-147">Mælieiningar</span><span class="sxs-lookup"><span data-stu-id="2ac87-147">Units of measure</span></span>
* <span data-ttu-id="2ac87-148">Vörurakningarkóti</span><span class="sxs-lookup"><span data-stu-id="2ac87-148">Item tracking code</span></span>
* <span data-ttu-id="2ac87-149">Verðflokkur viðskiptamanns</span><span class="sxs-lookup"><span data-stu-id="2ac87-149">Customer price group</span></span>

<span data-ttu-id="2ac87-150">Ef reikningar eru fluttir eru eftirfarandi gögn einnig flutt:</span><span class="sxs-lookup"><span data-stu-id="2ac87-150">If you migrate accounts, the following data is also migrated:</span></span>

* <span data-ttu-id="2ac87-151">Birgðabókunargrunnur</span><span class="sxs-lookup"><span data-stu-id="2ac87-151">Inventory posting setup</span></span>
* <span data-ttu-id="2ac87-152">Almennur bókunargrunnur</span><span class="sxs-lookup"><span data-stu-id="2ac87-152">General posting setup</span></span>
* <span data-ttu-id="2ac87-153">Birgðabókarkeyrsla</span><span class="sxs-lookup"><span data-stu-id="2ac87-153">Item journal batch</span></span>
* <span data-ttu-id="2ac87-154">Opnar færslur (birgðafærslur)</span><span class="sxs-lookup"><span data-stu-id="2ac87-154">Open transactions (item ledger entries)</span></span>

> [!Note]
> <span data-ttu-id="2ac87-155">Ef opnar færslur eru til staðar sem nota erlenda gjaldmiðla er gengi þeirra einnig flutt inn.</span><span class="sxs-lookup"><span data-stu-id="2ac87-155">If there are open transactions that use foreign currencies, the exchange rates for those currencies are also migrated.</span></span> <span data-ttu-id="2ac87-156">Önnur gengi eru ekki flutt inn.</span><span class="sxs-lookup"><span data-stu-id="2ac87-156">Other exchange rates are not migrated.</span></span>

<span data-ttu-id="2ac87-157">**Bókhaldslykill**</span><span class="sxs-lookup"><span data-stu-id="2ac87-157">**Chart of Accounts**</span></span>  
* <span data-ttu-id="2ac87-158">Staðlaðar víddir: Deild, kostnaðarstaður, tilgangur</span><span class="sxs-lookup"><span data-stu-id="2ac87-158">Standard dimensions: Department, Cost Center, Purpose</span></span>  
* <span data-ttu-id="2ac87-159">Sögulegar fjárhagsfærslur</span><span class="sxs-lookup"><span data-stu-id="2ac87-159">Historical G/L transactions</span></span>  

> [!Note]
> <span data-ttu-id="2ac87-160">Sögulegar fjárhagsfærslur eru meðhöndlaðir aðeins öðruvísi.</span><span class="sxs-lookup"><span data-stu-id="2ac87-160">Historical G/L transactions are treated a little differently.</span></span> <span data-ttu-id="2ac87-161">Þegar þú flytur gögn stillirðu færibreytuna **Núverandi tímabil**.</span><span class="sxs-lookup"><span data-stu-id="2ac87-161">When you migrate data you set a **Current Period** parameter.</span></span> <span data-ttu-id="2ac87-162">Þessi færibreyta tilgreinir hvernig á að vinna úr fjárhagsfærslum.</span><span class="sxs-lookup"><span data-stu-id="2ac87-162">This parameter specifies how to process G/L transactions.</span></span> <span data-ttu-id="2ac87-163">Færslur eftir þessa dagsetningu eru fluttar hver fyrir sig.</span><span class="sxs-lookup"><span data-stu-id="2ac87-163">Transactions after this date are migrated individually.</span></span> <span data-ttu-id="2ac87-164">Færslum fyrir þessa dagsetningu er safnað saman fyrir hvern reikning og fluttar sem ein upphæð.</span><span class="sxs-lookup"><span data-stu-id="2ac87-164">Transactions before this date are aggregated per account and migrated as a single amount.</span></span> <span data-ttu-id="2ac87-165">Segjum sem dæmi að það séu færslur á árunum 2015, 2016, 2017, 2018 og þú tilgreinir 1. janúar 2017 í reit núverandi tímabils.</span><span class="sxs-lookup"><span data-stu-id="2ac87-165">For example, let's say there are transactions in 2015, 2016, 2017, 2018, and you specify January 01, 2017 in the Current Period field.</span></span> <span data-ttu-id="2ac87-166">Fyrir hvern reikning verður upphæðum fyrir færslur á eða fyrir 31. desember 2016 safnað saman í eina færslubókarlínu fyrir hverja fjárhagsfærslu.</span><span class="sxs-lookup"><span data-stu-id="2ac87-166">For each account, amounts for transactions on or before December 31, 2106, will be aggregated in a single general journal line for each G/L account.</span></span> <span data-ttu-id="2ac87-167">Allar færslur eftir þennan dag verða fluttar hver fyrir sig.</span><span class="sxs-lookup"><span data-stu-id="2ac87-167">All trascations after this date will be migrated individually.</span></span>

## <a name="to-migrate-data"></a><span data-ttu-id="2ac87-168">Til að flytja gögn</span><span class="sxs-lookup"><span data-stu-id="2ac87-168">To migrate data</span></span>
<span data-ttu-id="2ac87-169">Það eru aðeins nokkur skref fólgin í því að flytja út gögn úr C5 og flytja þau inn í [!INCLUDE[d365fin](includes/d365fin_md.md)]:</span><span class="sxs-lookup"><span data-stu-id="2ac87-169">There are just a few steps to export data from C5, and import it in [!INCLUDE[d365fin](includes/d365fin_md.md)]:</span></span>  

1. <span data-ttu-id="2ac87-170">Í C5 skaltu nota **Flytja út gagnagrunn** eiginleikann til að flytja út gögnin.</span><span class="sxs-lookup"><span data-stu-id="2ac87-170">In C5, use the **Export Database** feature to export the data.</span></span> <span data-ttu-id="2ac87-171">Sendu síðan útflutningsmöppuna í þappaða möppu.</span><span class="sxs-lookup"><span data-stu-id="2ac87-171">Then send the export folder to a compressed (zipped) folder.</span></span>  
2. <span data-ttu-id="2ac87-172">Í [!INCLUDE[d365fin](includes/d365fin_md.md)] skal velja ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Gagnaflutningur** og velja svo **Gagnaflutningur**.</span><span class="sxs-lookup"><span data-stu-id="2ac87-172">In [!INCLUDE[d365fin](includes/d365fin_md.md)], choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Data Migration**, and then choose **Data Migration**.</span></span>  
3. <span data-ttu-id="2ac87-173">Ljúka skal skrefunum í leiðbeiningum um uppsetningu með hjálp.</span><span class="sxs-lookup"><span data-stu-id="2ac87-173">Complete the steps in the assisted setup guide.</span></span> <span data-ttu-id="2ac87-174">Gakktu úr skugga um að velja **Flytja inn úr Microsoft Dynamcis C5 2012** sem gagnagjafa.</span><span class="sxs-lookup"><span data-stu-id="2ac87-174">Make sure to choose **Import from Microsoft Dynamcis C5 2012** as the data source.</span></span>  

> [!Note]
> <span data-ttu-id="2ac87-175">Fyrirtæki bæta oft við reitum til að sérsníða C5 fyrir tiltekna starfsemi.</span><span class="sxs-lookup"><span data-stu-id="2ac87-175">Companies often add fields to customize C5 for their specific line of business.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="2ac87-176"> flytur ekki gögn úr sérsniðnum reitum.</span><span class="sxs-lookup"><span data-stu-id="2ac87-176"> does not migrate data from custom fields.</span></span> <span data-ttu-id="2ac87-177">Einnig mun flutningur mistakast ef fleiri en 10 sérsniðnir reitir eru til staðar.</span><span class="sxs-lookup"><span data-stu-id="2ac87-177">Also, migration will fail if you have more than 10 custom fields.</span></span>

## <a name="viewing-the-status-of-the-migration"></a><span data-ttu-id="2ac87-178">Skoðun stöðu á flutningi</span><span class="sxs-lookup"><span data-stu-id="2ac87-178">Viewing the Status of the Migration</span></span>
<span data-ttu-id="2ac87-179">Nota skal síðuna **Gagnaflutningsyfirlit** til að sjá stöðu flutningsins.</span><span class="sxs-lookup"><span data-stu-id="2ac87-179">Use the **Data Migration Overview** page to monitor the success of the migration.</span></span> <span data-ttu-id="2ac87-180">Síðan sýnir upplýsingar, svo sem fjöldi færslna sem flutningurinn mun innihalda, stöðu flutningsins og fjölda vara sem hafa verið fluttar og hvort flutningur þeirra tókst.</span><span class="sxs-lookup"><span data-stu-id="2ac87-180">The page shows information such as the number of entities that the migration will include, the status of the migration, and the number of items that have been migrated and whether they were successfull.</span></span> <span data-ttu-id="2ac87-181">Hún sýnir einnig fjölda villna, gerir þér kleift að rannsaka hvað fór úrskeiðis og, þegar mögulegt er, auðveldar það að fara í færsluna til að laga vandamálin.</span><span class="sxs-lookup"><span data-stu-id="2ac87-181">It also shows the number of errors, lets you investigate what went wrong and, when possible, makes it easy to go to the entity to fix the issues.</span></span> <span data-ttu-id="2ac87-182">Nánari upplýsingar eru í næsta hluta þessa efnisatriðis.</span><span class="sxs-lookup"><span data-stu-id="2ac87-182">For more information, see the next section in this topic.</span></span>  

> [!Note]
> <span data-ttu-id="2ac87-183">Meðan beðið er eftir stöðu flutningsins þarf að uppfæra síðuna til að birta niðurstöðurnar.</span><span class="sxs-lookup"><span data-stu-id="2ac87-183">While you are waiting for the results of the migration, you must refresh the page to display the results.</span></span>

## <a name="how-to-avoid-double-posting"></a><span data-ttu-id="2ac87-184">Hvernig á að koma í veg fyrir tvíbókun</span><span class="sxs-lookup"><span data-stu-id="2ac87-184">How to Avoid Double-Posting</span></span>
<span data-ttu-id="2ac87-185">Til að koma í veg fyrir tvíbókanir í fjárhagnum eru eftirfarandi mótreikningar notaðir fyrir opnar færslur:</span><span class="sxs-lookup"><span data-stu-id="2ac87-185">To help avoid double-posting to the general ledger, the following balance accounts are used for open transactions:</span></span>  
  
* <span data-ttu-id="2ac87-186">Fyrir lánardrottna notum við viðskiptaskuldareikninginn frá bókunarflokki lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="2ac87-186">For vendors, we use the A/P account from the vendor posting group.</span></span>  
* <span data-ttu-id="2ac87-187">Fyrir viðskiptavini notum við viðskiptakröfureikninginn frá bókunarflokki viðskiptavinar.</span><span class="sxs-lookup"><span data-stu-id="2ac87-187">For customers, we use the A/R account from the customer posting group.</span></span>  
* <span data-ttu-id="2ac87-188">Fyrir vörur búum við til almennan bókunargrunn þar sem leiðréttingarreikningurinn er reikningurinn sem er tilgreindur sem birgðarreikningur í birgðabókunargrunni.</span><span class="sxs-lookup"><span data-stu-id="2ac87-188">For items, we create a general posting setup where the adjustment account is the account specified as the inventory account on the inventory posting setup.</span></span>  

## <a name="correcting-errors"></a><span data-ttu-id="2ac87-189">Leiðrétting villna</span><span class="sxs-lookup"><span data-stu-id="2ac87-189">Correcting Errors</span></span>
<span data-ttu-id="2ac87-190">Ef eitthvað fer úrskeiðis og villur koma upp sýnir **Staða** reiturinn **Lokið með villum** og **Villutalning** reiturinn mun sýna fjöldann.</span><span class="sxs-lookup"><span data-stu-id="2ac87-190">If something goes wrong and an error occurs, the **Status** field will show **Completed with Errors**, and the **Error Count** field will show how many.</span></span> <span data-ttu-id="2ac87-191">Til að skoða lista yfir villurnar er hægt að opna **Villur í gagnaflutningi** síðuna með því að velja:</span><span class="sxs-lookup"><span data-stu-id="2ac87-191">To view a list of the errors, you can open the **Data Migration Errors** page by choosing:</span></span>  

* <span data-ttu-id="2ac87-192">Talan í **Villutalning** reitnum fyrir eininguna.</span><span class="sxs-lookup"><span data-stu-id="2ac87-192">The number in the **Error Count** field for the entity.</span></span>  
* <span data-ttu-id="2ac87-193">Einingin og svo **Sýna villur** aðgerðin.</span><span class="sxs-lookup"><span data-stu-id="2ac87-193">The entity, and then the **Show Errors** action.</span></span>  

<span data-ttu-id="2ac87-194">Á **Villur í gagnaflutningi** síðunni, til að laga villu er hægt að velja villuboð og svo **Breyta færslu** til að opna síðu sem sýnir flutt gögn fyrir eininguna.</span><span class="sxs-lookup"><span data-stu-id="2ac87-194">On the **Data Migration Errors** page, to fix an error you can choose an error message, then choose **Edit Record** to open a page that shows the migrated data for the entity.</span></span> <span data-ttu-id="2ac87-195">Eftir að þú hefur lagað eina eða fleiri villur getur þú valið **Flytja** til að flytja aðeins einingarnar sem þú lagaðir án þess að þurfa að hefja flutninginn aftur.</span><span class="sxs-lookup"><span data-stu-id="2ac87-195">After you fix one or more errors, you can choose **Migrate** to migrate only the entities you fixed, without having to completely restart the migration.</span></span>  

> [!Tip]
> <span data-ttu-id="2ac87-196">Ef þú hefur lagað fleiri en eina villu geturðu notað **Velja fleira** valkostinn til að velja margar línur til að flytja.</span><span class="sxs-lookup"><span data-stu-id="2ac87-196">If you have fixed more than one error, you can use the **Select More** feature to select multiple lines to migrate.</span></span> <span data-ttu-id="2ac87-197">Ef villur eru til staðar sem ekki er mikilvægt að laga geturðu valið þær og svo **Sleppa vali**.</span><span class="sxs-lookup"><span data-stu-id="2ac87-197">Alternatively, if there are errors that are not important to fix, you can choose them and then choose **Skip Selections**.</span></span>

> [!Note]
> <span data-ttu-id="2ac87-198">Ef vörur eru til staðar sem er að finna í uppskrift gætir þú þurft að flytja oftar en einu sinni ef upprunalega varan er ekki stofnuð fyrir afbrigðið sem vísa til hennar.</span><span class="sxs-lookup"><span data-stu-id="2ac87-198">If you have items that are included in a BOM, you might need to migrate more than once if the original item is not created before the variants that reference it.</span></span> <span data-ttu-id="2ac87-199">Ef afbrigðið er búið til fyrst getur tilvísunin í upprunalegu vöruna valdið villuboðum.</span><span class="sxs-lookup"><span data-stu-id="2ac87-199">If an item variant is created first, the reference to the original item can cause an error message.</span></span>  

## <a name="verifying-data-after-migrating"></a><span data-ttu-id="2ac87-200">Staðfesting gagna eftir flutning</span><span class="sxs-lookup"><span data-stu-id="2ac87-200">Verifying Data After Migrating</span></span>
<span data-ttu-id="2ac87-201">Ein leið til að sannreyna að gögnin hafi verið rétt flutt inn er með því að skoða eftirfarandi síður í C5 og [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="2ac87-201">One way to verify that your data migrated correctly is to look at the following pages in C5 and [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

|<span data-ttu-id="2ac87-202">Microsoft Dynamcis C5 2012</span><span class="sxs-lookup"><span data-stu-id="2ac87-202">Microsoft Dynamcis C5 2012</span></span> | [!INCLUDE[d365fin](includes/d365fin_md.md)]| <span data-ttu-id="2ac87-203">Runuvinnsla sem á að nota</span><span class="sxs-lookup"><span data-stu-id="2ac87-203">Batch Job to Use</span></span> |
|-----|-----|-----|
|<span data-ttu-id="2ac87-204">Viðskm.færslur</span><span class="sxs-lookup"><span data-stu-id="2ac87-204">Customer Entries</span></span>| <span data-ttu-id="2ac87-205">Almennar færslubækur</span><span class="sxs-lookup"><span data-stu-id="2ac87-205">General Journals</span></span>| <span data-ttu-id="2ac87-206">CUSTMIGR</span><span class="sxs-lookup"><span data-stu-id="2ac87-206">CUSTMIGR</span></span> |
|<span data-ttu-id="2ac87-207">Lánardr.færslur</span><span class="sxs-lookup"><span data-stu-id="2ac87-207">Vendor Entries</span></span>| <span data-ttu-id="2ac87-208">Almennar færslubækur</span><span class="sxs-lookup"><span data-stu-id="2ac87-208">General Journals</span></span>| <span data-ttu-id="2ac87-209">VENDMIGR</span><span class="sxs-lookup"><span data-stu-id="2ac87-209">VENDMIGR</span></span>|
|<span data-ttu-id="2ac87-210">Birgðafærslur</span><span class="sxs-lookup"><span data-stu-id="2ac87-210">Item Entries</span></span>| <span data-ttu-id="2ac87-211">Birgðabækur</span><span class="sxs-lookup"><span data-stu-id="2ac87-211">Item Journals</span></span>| <span data-ttu-id="2ac87-212">ITEMMIGR</span><span class="sxs-lookup"><span data-stu-id="2ac87-212">ITEMMIGR</span></span> |
|<span data-ttu-id="2ac87-213">Fjárhagsfærslur</span><span class="sxs-lookup"><span data-stu-id="2ac87-213">G/L Entries</span></span>| <span data-ttu-id="2ac87-214">Almennar færslubækur</span><span class="sxs-lookup"><span data-stu-id="2ac87-214">General Journals</span></span>| <span data-ttu-id="2ac87-215">GLACMIGR</span><span class="sxs-lookup"><span data-stu-id="2ac87-215">GLACMIGR</span></span> |

## <a name="stopping-data-migration"></a><span data-ttu-id="2ac87-216">Stöðvun gagnaflutnings</span><span class="sxs-lookup"><span data-stu-id="2ac87-216">Stopping Data Migration</span></span>
<span data-ttu-id="2ac87-217">Þú getur hætt að flytja gögn með því að velja **Hætta við allan flutning**.</span><span class="sxs-lookup"><span data-stu-id="2ac87-217">You can stop migrating data by choosing **Stop All Migrations**.</span></span> <span data-ttu-id="2ac87-218">Ef þú gerir það er líka hætt við allan flutning sem bíður.</span><span class="sxs-lookup"><span data-stu-id="2ac87-218">If you do, all pending migrations are also stopped.</span></span>

## <a name="see-also"></a><span data-ttu-id="2ac87-219">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="2ac87-219">See Also</span></span>
<span data-ttu-id="2ac87-220">[Sérstilling [!INCLUDE[d365fin](includes/d365fin_md.md)] með viðbótum](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="2ac87-220">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions](ui-extensions.md)</span></span>  
[<span data-ttu-id="2ac87-221">Hafist handa</span><span class="sxs-lookup"><span data-stu-id="2ac87-221">Getting Started</span></span>](product-get-started.md) 

