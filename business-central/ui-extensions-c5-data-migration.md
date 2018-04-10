---
title: "Notkun C5 gagnaflutningsviðbótar | Microsoft Docs"
description: "Þessi viðbót er notuð til að flytja viðskiptamenn,lánardrottna, vörur og fjárhagsreikninga úr Microsoft Dynamics C5 2012 í Financials."
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: extension, migrate, data, C5, import
ms.date: 11/21/2017
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: e7dcdc0935a8793ae226dfc2f9709b5b8f487a62
ms.openlocfilehash: 7fe6393ad43dbad032512b2d6d45cc8ee0392236
ms.contentlocale: is-is
ms.lasthandoff: 03/22/2018

---

# <a name="the-c5-data-migration-extension-for-business-central"></a><span data-ttu-id="c7ba3-103">C5 gagnaflutningsviðbót fyrir Business Central</span><span class="sxs-lookup"><span data-stu-id="c7ba3-103">The C5 Data Migration Extension for Business Central</span></span>
<span data-ttu-id="c7ba3-104">Þessi viðbót auðveldar flutning viðskiptamanna, lánardrottna, vara og fjárhagsreikninga úr Microsoft Dynamics C5 2012 í [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="c7ba3-104">This extension makes it easy to migrate customers, vendors, items, and your general ledger accounts from Microsoft Dynamcis C5 2012 to [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="c7ba3-105">Hægt er að flytja elrdi færslur fyrir fjárhagsreikning.</span><span class="sxs-lookup"><span data-stu-id="c7ba3-105">You can also migrate historical entries for general ledger accounts.</span></span>

> [!Note]
> <span data-ttu-id="c7ba3-106">Fyrirtækið í [!INCLUDE[d365fin](includes/d365fin_md.md)] má ekki innihalda gögn.</span><span class="sxs-lookup"><span data-stu-id="c7ba3-106">The company in [!INCLUDE[d365fin](includes/d365fin_md.md)] must not contain any data.</span></span> <span data-ttu-id="c7ba3-107">Að auki skaltu ekki búa til viðskiptavini, lánardrottna, vörur eða reikninga fyrr en flutningur lýkur.</span><span class="sxs-lookup"><span data-stu-id="c7ba3-107">Additionally, after you start a migration, do not create customers, vendors, items, or accounts until the migration finishes.</span></span>

##<a name="what-data-is-migrated"></a><span data-ttu-id="c7ba3-108">Hvaða gögn eru flutt?</span><span class="sxs-lookup"><span data-stu-id="c7ba3-108">What Data is Migrated?</span></span>
<span data-ttu-id="c7ba3-109">Eftirfarandi gögn eru flutt fyrir hverja einingu:</span><span class="sxs-lookup"><span data-stu-id="c7ba3-109">The following data is migrated for each entity:</span></span>

<span data-ttu-id="c7ba3-110">**Viðskiptavinum**</span><span class="sxs-lookup"><span data-stu-id="c7ba3-110">**Customers**</span></span>
* <span data-ttu-id="c7ba3-111">Birgðageymsla</span><span class="sxs-lookup"><span data-stu-id="c7ba3-111">Location</span></span>
* <span data-ttu-id="c7ba3-112">Land</span><span class="sxs-lookup"><span data-stu-id="c7ba3-112">Country</span></span>
* <span data-ttu-id="c7ba3-113">Vídd viðskiptavina (deild, miðstöð, tilgangur)</span><span class="sxs-lookup"><span data-stu-id="c7ba3-113">Customer dimensions (department, center, purpose)</span></span>
* <span data-ttu-id="c7ba3-114">Afhendingarmáti</span><span class="sxs-lookup"><span data-stu-id="c7ba3-114">Shipment method</span></span>
* <span data-ttu-id="c7ba3-115">Sölumaður</span><span class="sxs-lookup"><span data-stu-id="c7ba3-115">Sales Person</span></span>
* <span data-ttu-id="c7ba3-116">Greiðsluskilmálar</span><span class="sxs-lookup"><span data-stu-id="c7ba3-116">Payment terms</span></span>
* <span data-ttu-id="c7ba3-117">Greiðslumáti</span><span class="sxs-lookup"><span data-stu-id="c7ba3-117">Payment method</span></span>
* <span data-ttu-id="c7ba3-118">Verðflokkur viðskiptamanns</span><span class="sxs-lookup"><span data-stu-id="c7ba3-118">Customer price group</span></span>
* <span data-ttu-id="c7ba3-119">Reikningsafsláttur viðskiptavinar</span><span class="sxs-lookup"><span data-stu-id="c7ba3-119">Customer invoice discount</span></span>

<span data-ttu-id="c7ba3-120">Ef reikningar eru fluttir eru eftirfarandi gögn einnig flutt:</span><span class="sxs-lookup"><span data-stu-id="c7ba3-120">If you migrate accounts, the following data is also migrated:</span></span>

* <span data-ttu-id="c7ba3-121">Uppsetning bókunar viðskiptavinar</span><span class="sxs-lookup"><span data-stu-id="c7ba3-121">Customer posting setup</span></span>
* <span data-ttu-id="c7ba3-122">Almenn færslubókarkeyrsla</span><span class="sxs-lookup"><span data-stu-id="c7ba3-122">General journal batch</span></span>
* <span data-ttu-id="c7ba3-123">Opnar færslur (í viðskiptamannabók)</span><span class="sxs-lookup"><span data-stu-id="c7ba3-123">Open transactions (customer ledger entries)</span></span>

<span data-ttu-id="c7ba3-124">**Lánardrottnar**</span><span class="sxs-lookup"><span data-stu-id="c7ba3-124">**Vendors**</span></span>
* <span data-ttu-id="c7ba3-125">Birgðageymsla</span><span class="sxs-lookup"><span data-stu-id="c7ba3-125">Location</span></span>
* <span data-ttu-id="c7ba3-126">Land</span><span class="sxs-lookup"><span data-stu-id="c7ba3-126">Country</span></span>
* <span data-ttu-id="c7ba3-127">Vídd lánardrottins (deild, miðstöð, tilgangur)</span><span class="sxs-lookup"><span data-stu-id="c7ba3-127">Vendor dimensions (department, center, purpose)</span></span>
* <span data-ttu-id="c7ba3-128">Reikningsafsláttur</span><span class="sxs-lookup"><span data-stu-id="c7ba3-128">Invoice discount</span></span>
* <span data-ttu-id="c7ba3-129">Afhendingarmáti</span><span class="sxs-lookup"><span data-stu-id="c7ba3-129">Shipment method</span></span>
* <span data-ttu-id="c7ba3-130">Innkaupaaðili</span><span class="sxs-lookup"><span data-stu-id="c7ba3-130">Purchaser</span></span>
* <span data-ttu-id="c7ba3-131">Greiðsluskilmálar</span><span class="sxs-lookup"><span data-stu-id="c7ba3-131">Payment terms</span></span>
* <span data-ttu-id="c7ba3-132">Greiðslumáti</span><span class="sxs-lookup"><span data-stu-id="c7ba3-132">Payment method</span></span>
* <span data-ttu-id="c7ba3-133">Afsláttur lánardrottnareikninga</span><span class="sxs-lookup"><span data-stu-id="c7ba3-133">Vendor invoice discount</span></span>

<span data-ttu-id="c7ba3-134">Ef reikningar eru fluttir eru eftirfarandi gögn einnig flutt:</span><span class="sxs-lookup"><span data-stu-id="c7ba3-134">If you migrate accounts, the following data is also migrated:</span></span>

* <span data-ttu-id="c7ba3-135">Bókunarflokkur lánardrottins</span><span class="sxs-lookup"><span data-stu-id="c7ba3-135">Vendor posting setup</span></span>
* <span data-ttu-id="c7ba3-136">Almenn færslubókarkeyrsla</span><span class="sxs-lookup"><span data-stu-id="c7ba3-136">General journal batch</span></span>
* <span data-ttu-id="c7ba3-137">Opnar færslur (fjárhagsfærslur lánardrottins)</span><span class="sxs-lookup"><span data-stu-id="c7ba3-137">Open transactions (vendor ledger entries)</span></span>

<span data-ttu-id="c7ba3-138">**Birgðir**</span><span class="sxs-lookup"><span data-stu-id="c7ba3-138">**Items**</span></span>
* <span data-ttu-id="c7ba3-139">Birgðageymsla</span><span class="sxs-lookup"><span data-stu-id="c7ba3-139">Location</span></span>
* <span data-ttu-id="c7ba3-140">Land</span><span class="sxs-lookup"><span data-stu-id="c7ba3-140">Country</span></span>
* <span data-ttu-id="c7ba3-141">Vöruvíddir (deild, miðstöð, tilgangur)</span><span class="sxs-lookup"><span data-stu-id="c7ba3-141">Item dimensions (department, center, purpose)</span></span>
* <span data-ttu-id="c7ba3-142">Sölulínuafslættir</span><span class="sxs-lookup"><span data-stu-id="c7ba3-142">Sales line discounts</span></span>
* <span data-ttu-id="c7ba3-143">Afsláttarflokkar viðskiptamanna</span><span class="sxs-lookup"><span data-stu-id="c7ba3-143">Customer discount groups</span></span>
* <span data-ttu-id="c7ba3-144">Vöruafsláttarflokkar</span><span class="sxs-lookup"><span data-stu-id="c7ba3-144">Item discount groups</span></span>
* <span data-ttu-id="c7ba3-145">Söluverð</span><span class="sxs-lookup"><span data-stu-id="c7ba3-145">Sales price</span></span>
* <span data-ttu-id="c7ba3-146">Tollnúmer</span><span class="sxs-lookup"><span data-stu-id="c7ba3-146">Tariff number</span></span>
* <span data-ttu-id="c7ba3-147">Mælieiningar</span><span class="sxs-lookup"><span data-stu-id="c7ba3-147">Units of measure</span></span>
* <span data-ttu-id="c7ba3-148">Vörurakningarkóti</span><span class="sxs-lookup"><span data-stu-id="c7ba3-148">Item tracking code</span></span>
* <span data-ttu-id="c7ba3-149">Verðflokkur viðskiptamanns</span><span class="sxs-lookup"><span data-stu-id="c7ba3-149">Customer price group</span></span>

<span data-ttu-id="c7ba3-150">Ef reikningar eru fluttir eru eftirfarandi gögn einnig flutt:</span><span class="sxs-lookup"><span data-stu-id="c7ba3-150">If you migrate accounts, the following data is also migrated:</span></span>

* <span data-ttu-id="c7ba3-151">Birgðabókunargrunnur</span><span class="sxs-lookup"><span data-stu-id="c7ba3-151">Inventory posting setup</span></span>
* <span data-ttu-id="c7ba3-152">Almennur bókunargrunnur</span><span class="sxs-lookup"><span data-stu-id="c7ba3-152">General posting setup</span></span>
* <span data-ttu-id="c7ba3-153">Birgðabókarkeyrsla</span><span class="sxs-lookup"><span data-stu-id="c7ba3-153">Item journal batch</span></span>
* <span data-ttu-id="c7ba3-154">Opnar færslur (birgðafærslur)</span><span class="sxs-lookup"><span data-stu-id="c7ba3-154">Open transactions (item ledger entries)</span></span>

> [!Note]
> <span data-ttu-id="c7ba3-155">Ef opnar færslur eru til staðar sem nota erlenda gjaldmiðla er gengi þeirra einnig flutt inn.</span><span class="sxs-lookup"><span data-stu-id="c7ba3-155">If there are open transactions that use foreign currencies, the exchange rates for those currencies are also migrated.</span></span> <span data-ttu-id="c7ba3-156">Önnur gengi eru ekki flutt inn.</span><span class="sxs-lookup"><span data-stu-id="c7ba3-156">Other exchange rates are not migrated.</span></span>

## <a name="to-migrate-data"></a><span data-ttu-id="c7ba3-157">Til að flytja gögn</span><span class="sxs-lookup"><span data-stu-id="c7ba3-157">To migrate data</span></span>
<span data-ttu-id="c7ba3-158">Það eru aðeins nokkur skref fólgin í því að flytja út gögn úr C5 og flytja þau inn í [!INCLUDE[d365fin](includes/d365fin_md.md)]:</span><span class="sxs-lookup"><span data-stu-id="c7ba3-158">There are just a few steps to export data from C5, and import it in [!INCLUDE[d365fin](includes/d365fin_md.md)]:</span></span>  

1. <span data-ttu-id="c7ba3-159">Í C5 skaltu nota **Flytja út gagnagrunn** eiginleikann til að flytja út gögnin.</span><span class="sxs-lookup"><span data-stu-id="c7ba3-159">In C5, use the **Export Database** feature to export the data.</span></span> <span data-ttu-id="c7ba3-160">Sendu síðan útflutningsmöppuna í þappaða möppu.</span><span class="sxs-lookup"><span data-stu-id="c7ba3-160">Then send the export folder to a compressed (zipped) folder.</span></span>  
2. <span data-ttu-id="c7ba3-161">Í [!INCLUDE[d365fin](includes/d365fin_md.md)] skal velja ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Gagnaflutningur** og velja svo **Gagnaflutningur**.</span><span class="sxs-lookup"><span data-stu-id="c7ba3-161">In [!INCLUDE[d365fin](includes/d365fin_md.md)], choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Data Migration**, and then choose **Data Migration**.</span></span>  
3. <span data-ttu-id="c7ba3-162">Ljúka skal skrefunum í leiðbeiningum um uppsetningu með hjálp.</span><span class="sxs-lookup"><span data-stu-id="c7ba3-162">Complete the steps in the assisted setup guide.</span></span> <span data-ttu-id="c7ba3-163">Gakktu úr skugga um að velja **Flytja inn úr Microsoft Dynamcis C5 2012** sem gagnagjafa.</span><span class="sxs-lookup"><span data-stu-id="c7ba3-163">Make sure to choose **Import from Microsoft Dynamcis C5 2012** as the data source.</span></span>  

> [!Note]
> <span data-ttu-id="c7ba3-164">Fyrirtæki bæta oft við reitum til að sérsníða C5 fyrir tiltekna starfsemi.</span><span class="sxs-lookup"><span data-stu-id="c7ba3-164">Companies often add fields to customize C5 for their specific line of business.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="c7ba3-165"> flytur ekki gögn úr sérsniðnum reitum.</span><span class="sxs-lookup"><span data-stu-id="c7ba3-165"> does not migrate data from custom fields.</span></span> <span data-ttu-id="c7ba3-166">Einnig mun flutningur mistakast ef fleiri en 10 sérsniðnir reitir eru til staðar.</span><span class="sxs-lookup"><span data-stu-id="c7ba3-166">Also, migration will fail if you have more than 10 custom fields.</span></span>

## <a name="viewing-the-status-of-the-migration"></a><span data-ttu-id="c7ba3-167">Skoðun stöðu á flutningi</span><span class="sxs-lookup"><span data-stu-id="c7ba3-167">Viewing the Status of the Migration</span></span>
<span data-ttu-id="c7ba3-168">Nota skal síðuna **Gagnaflutningsyfirlit** til að sjá stöðu flutningsins.</span><span class="sxs-lookup"><span data-stu-id="c7ba3-168">Use the **Data Migration Overview** page to monitor the success of the migration.</span></span> <span data-ttu-id="c7ba3-169">Síðan sýnir upplýsingar, svo sem fjöldi færslna sem flutningurinn mun innihalda, stöðu flutningsins og fjölda vara sem hafa verið fluttar og hvort flutningur þeirra tókst.</span><span class="sxs-lookup"><span data-stu-id="c7ba3-169">The page shows information such as the number of entities that the migration will include, the status of the migration, and the number of items that have been migrated and whether they were successfull.</span></span> <span data-ttu-id="c7ba3-170">Hún sýnir einnig fjölda villna, gerir þér kleift að rannsaka hvað fór úrskeiðis og, þegar mögulegt er, auðveldar það að fara í færsluna til að laga vandamálin.</span><span class="sxs-lookup"><span data-stu-id="c7ba3-170">It also shows the number of errors, lets you investigate what went wrong and, when possible, makes it easy to go to the entity to fix the issues.</span></span> <span data-ttu-id="c7ba3-171">Nánari upplýsingar eru í næsta hluta þessa efnisatriðis.</span><span class="sxs-lookup"><span data-stu-id="c7ba3-171">For more information, see the next section in this topic.</span></span>  

> [!Note]
> <span data-ttu-id="c7ba3-172">Meðan beðið er eftir stöðu flutningsins þarf að uppfæra síðuna til að birta niðurstöðurnar.</span><span class="sxs-lookup"><span data-stu-id="c7ba3-172">While you are waiting for the results of the migration, you must refresh the page to display the results.</span></span>

## <a name="correcting-errors"></a><span data-ttu-id="c7ba3-173">Leiðrétting villna</span><span class="sxs-lookup"><span data-stu-id="c7ba3-173">Correcting Errors</span></span>
<span data-ttu-id="c7ba3-174">Ef eitthvað fer úrskeiðis og villur koma upp sýnir **Staða** reiturinn **Lokið með villum** og **Villutalning** reiturinn mun sýna fjöldann.</span><span class="sxs-lookup"><span data-stu-id="c7ba3-174">If something goes wrong and an error occurs, the **Status** field will show **Completed with Errors**, and the **Error Count** field will show how many.</span></span> <span data-ttu-id="c7ba3-175">Til að skoða lista yfir villurnar er hægt að opna **Villur í gagnaflutningi** síðuna með því að velja:</span><span class="sxs-lookup"><span data-stu-id="c7ba3-175">To view a list of the errors, you can open the **Data Migration Errors** page by choosing:</span></span>  

* <span data-ttu-id="c7ba3-176">Talan í **Villutalning** reitnum fyrir eininguna.</span><span class="sxs-lookup"><span data-stu-id="c7ba3-176">The number in the **Error Count** field for the entity.</span></span>  
* <span data-ttu-id="c7ba3-177">Einingin og svo **Sýna villur** aðgerðin.</span><span class="sxs-lookup"><span data-stu-id="c7ba3-177">The entity, and then the **Show Errors** action.</span></span>  

<span data-ttu-id="c7ba3-178">Á **Villur í gagnaflutningi** síðunni, til að laga villu er hægt að velja villuboð og svo **Breyta færslu** til að opna síðu sem sýnir flutt gögn fyrir eininguna.</span><span class="sxs-lookup"><span data-stu-id="c7ba3-178">On the **Data Migration Errors** page, to fix an error you can choose an error message, then choose **Edit Record** to open a page that shows the migrated data for the entity.</span></span> <span data-ttu-id="c7ba3-179">Eftir að þú hefur lagað eina eða fleiri villur getur þú valið **Flytja** til að flytja aðeins einingarnar sem þú lagaðir án þess að þurfa að hefja flutninginn aftur.</span><span class="sxs-lookup"><span data-stu-id="c7ba3-179">After you fix one or more errors, you can choose **Migrate** to migrate only the entities you fixed, without having to completely restart the migration.</span></span>  

> [!Tip]
> <span data-ttu-id="c7ba3-180">Ef þú hefur lagað fleiri en eina villu geturðu notað **Velja fleira** valkostinn til að velja margar línur til að flytja.</span><span class="sxs-lookup"><span data-stu-id="c7ba3-180">If you have fixed more than one error, you can use the **Select More** feature to select multiple lines to migrate.</span></span> <span data-ttu-id="c7ba3-181">Ef villur eru til staðar sem ekki er mikilvægt að laga geturðu valið þær og svo **Sleppa vali**.</span><span class="sxs-lookup"><span data-stu-id="c7ba3-181">Alternatively, if there are errors that are not important to fix, you can choose them and then choose **Skip Selections**.</span></span>

> [!Note]
> <span data-ttu-id="c7ba3-182">Ef vörur eru til staðar sem er að finna í uppskrift gætir þú þurft að flytja oftar en einu sinni ef upprunalega varan er ekki stofnuð fyrir afbrigðið sem vísa til hennar.</span><span class="sxs-lookup"><span data-stu-id="c7ba3-182">If you have items that are included in a BOM, you might need to migrate more than once if the original item is not created before the variants that reference it.</span></span> <span data-ttu-id="c7ba3-183">Ef afbrigðið er búið til fyrst getur tilvísunin í upprunalegu vöruna valdið villuboðum.</span><span class="sxs-lookup"><span data-stu-id="c7ba3-183">If an item variant is created first, the reference to the original item can cause an error message.</span></span>  

## <a name="verifying-data-after-migrating"></a><span data-ttu-id="c7ba3-184">Staðfesting gagna eftir flutning</span><span class="sxs-lookup"><span data-stu-id="c7ba3-184">Verifying Data After Migrating</span></span>
<span data-ttu-id="c7ba3-185">Ein leið til að sannreyna að gögnin hafi verið rétt flutt inn er með því að skoða eftirfarandi síður í C5 og [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="c7ba3-185">One way to verify that your data migrated correctly is to look at the following pages in C5 and [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

|<span data-ttu-id="c7ba3-186">Microsoft Dynamcis C5 2012</span><span class="sxs-lookup"><span data-stu-id="c7ba3-186">Microsoft Dynamcis C5 2012</span></span> | [!INCLUDE[d365fin](includes/d365fin_md.md)]|
|-----|-----|
|<span data-ttu-id="c7ba3-187">Viðskm.færslur</span><span class="sxs-lookup"><span data-stu-id="c7ba3-187">Customer Entries</span></span>| <span data-ttu-id="c7ba3-188">Almennar færslubækur</span><span class="sxs-lookup"><span data-stu-id="c7ba3-188">General Journals</span></span>|
|<span data-ttu-id="c7ba3-189">Lánardr.færslur</span><span class="sxs-lookup"><span data-stu-id="c7ba3-189">Vendor Entries</span></span>| <span data-ttu-id="c7ba3-190">Almennar færslubækur</span><span class="sxs-lookup"><span data-stu-id="c7ba3-190">General Journals</span></span>|
|<span data-ttu-id="c7ba3-191">Birgðafærslur</span><span class="sxs-lookup"><span data-stu-id="c7ba3-191">Item Entries</span></span>| <span data-ttu-id="c7ba3-192">Birgðabækur</span><span class="sxs-lookup"><span data-stu-id="c7ba3-192">Item Journals</span></span>|

<span data-ttu-id="c7ba3-193">Í [!INCLUDE[d365fin](includes/d365fin_md.md)] er lotan fyrir fluttu gögnin kölluð **C5MIGRATE**.</span><span class="sxs-lookup"><span data-stu-id="c7ba3-193">In [!INCLUDE[d365fin](includes/d365fin_md.md)], the batch for the migrated data is named **C5MIGRATE**.</span></span>

## <a name="stopping-data-migration"></a><span data-ttu-id="c7ba3-194">Stöðvun gagnaflutnings</span><span class="sxs-lookup"><span data-stu-id="c7ba3-194">Stopping Data Migration</span></span>
<span data-ttu-id="c7ba3-195">Þú getur hætt að flytja gögn með því að velja **Hætta við allan flutning**.</span><span class="sxs-lookup"><span data-stu-id="c7ba3-195">You can stop migrating data by choosing **Stop All Migrations**.</span></span> <span data-ttu-id="c7ba3-196">Ef þú gerir það er líka hætt við allan flutning sem bíður.</span><span class="sxs-lookup"><span data-stu-id="c7ba3-196">If you do, all pending migrations are also stopped.</span></span>

## <a name="see-also"></a><span data-ttu-id="c7ba3-197">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="c7ba3-197">See Also</span></span>
<span data-ttu-id="c7ba3-198">[Sérstilling [!INCLUDE[d365fin](includes/d365fin_md.md)] með viðbótum](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="c7ba3-198">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions](ui-extensions.md)</span></span>  
[<span data-ttu-id="c7ba3-199">Hafist handa</span><span class="sxs-lookup"><span data-stu-id="c7ba3-199">Getting Started</span></span>](product-get-started.md) 

