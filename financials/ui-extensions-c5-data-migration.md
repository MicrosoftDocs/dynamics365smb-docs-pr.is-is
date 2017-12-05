---
title: "Notkun C5 gagnaflutningsviðbótar | Microsoft Docs"
description: "Þessi viðbót er notuð til að flytja viðskiptamenn,lánardrottna, vörur og fjárhagsreikninga úr Microsoft Dynamics C5 2012 í Financials."
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: extension, migrate, data, C5, import
ms.date: 09/26/2017
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: ba26b354d235981bd7291f9ac6402779f554ac7a
ms.openlocfilehash: 2d7d533662936116ffa40ded07b68e845fed810b
ms.contentlocale: is-is
ms.lasthandoff: 11/10/2017

---

# <a name="the-c5-data-migration-extension-for-dynamics-365-for-finance-and-operations-business-edition"></a><span data-ttu-id="27a3a-103">C5 gagnaflutningsviðbót fyrir Dynamics 365 for Finance and Operations, Business Edition</span><span class="sxs-lookup"><span data-stu-id="27a3a-103">The C5 Data Migration Extension for Dynamics 365 for Finance and Operations, Business Edition</span></span>
<span data-ttu-id="27a3a-104">Þessi viðbót auðveldar flutning viðskiptamanna, lánardrottna, vara og fjárhagsreikninga úr Microsoft Dynamics C5 2012 í [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="27a3a-104">This extension makes it easy to migrate customers, vendors, items, and your general ledger accounts from Microsoft Dynamcis C5 2012 to [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  
  
> [!Note] 
> <span data-ttu-id="27a3a-105">Fyrirtækið í [!INCLUDE[d365fin](includes/d365fin_md.md)] má ekki innihalda gögn.</span><span class="sxs-lookup"><span data-stu-id="27a3a-105">The company in [!INCLUDE[d365fin](includes/d365fin_md.md)] must not contain any data.</span></span> <span data-ttu-id="27a3a-106">Að auki skaltu ekki búa til viðskiptavini, lánardrottna, vörur eða reikninga fyrr en flutningur lýkur.</span><span class="sxs-lookup"><span data-stu-id="27a3a-106">Additionally, after you start a migration, do not create customers, vendors, items, or accounts until the migration finishes.</span></span>

## <a name="to-migrate-data"></a><span data-ttu-id="27a3a-107">Til að flytja gögn</span><span class="sxs-lookup"><span data-stu-id="27a3a-107">To migrate data</span></span>
<span data-ttu-id="27a3a-108">Það eru aðeins nokkur skref fólgin í því að flytja út gögn úr C5 og flytja þau inn í [!INCLUDE[d365fin](includes/d365fin_md.md)]:</span><span class="sxs-lookup"><span data-stu-id="27a3a-108">There are just a few steps to export data from C5, and import it in [!INCLUDE[d365fin](includes/d365fin_md.md)]:</span></span>  
  
1. <span data-ttu-id="27a3a-109">Í C5 skaltu nota **Flytja út gagnagrunn** eiginleikann til að flytja út gögnin.</span><span class="sxs-lookup"><span data-stu-id="27a3a-109">In C5, use the **Export Database** feature to export the data.</span></span> <span data-ttu-id="27a3a-110">Sendu síðan útflutningsmöppuna í þappaða möppu.</span><span class="sxs-lookup"><span data-stu-id="27a3a-110">Then send the export folder to a compressed (zipped) folder.</span></span>  
2. <span data-ttu-id="27a3a-111">Í [!INCLUDE[d365fin](includes/d365fin_md.md)] skal velja ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Gagnaflutningur** og velja svo **Gagnaflutningur**.</span><span class="sxs-lookup"><span data-stu-id="27a3a-111">In [!INCLUDE[d365fin](includes/d365fin_md.md)], choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Data Migration**, and then choose **Data Migration**.</span></span>  
3. <span data-ttu-id="27a3a-112">Ljúka skal skrefunum í leiðbeiningum um uppsetningu með hjálp.</span><span class="sxs-lookup"><span data-stu-id="27a3a-112">Complete the steps in the assisted setup guide.</span></span> <span data-ttu-id="27a3a-113">Gakktu úr skugga um að velja **Flytja inn úr Microsoft Dynamcis C5 2012** sem gagnagjafa.</span><span class="sxs-lookup"><span data-stu-id="27a3a-113">Make sure to choose **Import from Microsoft Dynamcis C5 2012** as the data source.</span></span>  

> [!Note] 
> <span data-ttu-id="27a3a-114">Fyrirtæki bæta oft við reitum til að sérsníða C5 fyrir tiltekna starfsemi.</span><span class="sxs-lookup"><span data-stu-id="27a3a-114">Companies often add fields to customize C5 for their specific line of business.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="27a3a-115"> flytur ekki gögn úr sérsniðnum reitum.</span><span class="sxs-lookup"><span data-stu-id="27a3a-115"> does not migrate data from custom fields.</span></span> <span data-ttu-id="27a3a-116">Einnig mun flutningur mistakast ef fleiri en 10 sérsniðnir reitir eru til staðar.</span><span class="sxs-lookup"><span data-stu-id="27a3a-116">Also, migration will fail if you have more than 10 custom fields.</span></span> 

## <a name="viewing-the-status-of-the-migration"></a><span data-ttu-id="27a3a-117">Skoðun stöðu á flutningi</span><span class="sxs-lookup"><span data-stu-id="27a3a-117">Viewing the Status of the Migration</span></span>
<span data-ttu-id="27a3a-118">Nota skal síðuna **Gagnaflutningsyfirlit** til að sjá stöðu flutningsins.</span><span class="sxs-lookup"><span data-stu-id="27a3a-118">Use the **Data Migration Overview** page to monitor the success of the migration.</span></span> <span data-ttu-id="27a3a-119">Síðan sýnir upplýsingar, svo sem fjöldi færslna sem flutningurinn mun innihalda, stöðu flutningsins og fjölda vara sem hafa verið fluttar og hvort flutningur þeirra tókst.</span><span class="sxs-lookup"><span data-stu-id="27a3a-119">The page shows information such as the number of entities that the migration will include, the status of the migration, and the number of items that have been migrated and whether they were successfull.</span></span> <span data-ttu-id="27a3a-120">Hún sýnir einnig fjölda villna, gerir þér kleift að rannsaka hvað fór úrskeiðis og, þegar mögulegt er, auðveldar það að fara í færsluna til að laga vandamálin.</span><span class="sxs-lookup"><span data-stu-id="27a3a-120">It also shows the number of errors, lets you investigate what went wrong and, when possible, makes it easy to go to the entity to fix the issues.</span></span> <span data-ttu-id="27a3a-121">Nánari upplýsingar eru í næsta hluta þessa efnisatriðis.</span><span class="sxs-lookup"><span data-stu-id="27a3a-121">For more information, see the next section in this topic.</span></span> 

> [!Note] 
> <span data-ttu-id="27a3a-122">Meðan beðið er eftir stöðu flutningsins þarf að uppfæra síðuna til að birta niðurstöðurnar.</span><span class="sxs-lookup"><span data-stu-id="27a3a-122">While you are waiting for the results of the migration, you must refresh the page to display the results.</span></span>

## <a name="correcting-errors"></a><span data-ttu-id="27a3a-123">Leiðrétting villna</span><span class="sxs-lookup"><span data-stu-id="27a3a-123">Correcting Errors</span></span>
<span data-ttu-id="27a3a-124">Ef eitthvað fer úrskeiðis og villur koma upp sýnir **Staða** reiturinn **Lokið með villum** og **Villutalning** reiturinn mun sýna fjöldann.</span><span class="sxs-lookup"><span data-stu-id="27a3a-124">If something goes wrong and an error occurs, the **Status** field will show **Completed with Errors**, and the **Error Count** field will show how many.</span></span> <span data-ttu-id="27a3a-125">Til að skoða lista yfir villurnar er hægt að opna **Villur í gagnaflutningi** síðuna með því að velja:</span><span class="sxs-lookup"><span data-stu-id="27a3a-125">To view a list of the errors, you can open the **Data Migration Errors** page by choosing:</span></span>

* <span data-ttu-id="27a3a-126">Talan í **Villutalning** reitnum fyrir eininguna.</span><span class="sxs-lookup"><span data-stu-id="27a3a-126">The number in the **Error Count** field for the entity.</span></span> 
* <span data-ttu-id="27a3a-127">Einingin og svo **Sýna villur** aðgerðin.</span><span class="sxs-lookup"><span data-stu-id="27a3a-127">The entity, and then the **Show Errors** action.</span></span> 

<span data-ttu-id="27a3a-128">Á **Villur í gagnaflutningi** síðunni, til að laga villu er hægt að velja villuboð og svo **Breyta færslu** til að opna síðu sem sýnir flutt gögn fyrir eininguna.</span><span class="sxs-lookup"><span data-stu-id="27a3a-128">On the **Data Migration Errors** page, to fix an error you can choose an error message, then choose **Edit Record** to open a page that shows the migrated data for the entity.</span></span> <span data-ttu-id="27a3a-129">Eftir að þú hefur lagað eina eða fleiri villur getur þú valið **Flytja** til að flytja aðeins einingarnar sem þú lagaðir án þess að þurfa að hefja flutninginn aftur.</span><span class="sxs-lookup"><span data-stu-id="27a3a-129">After you fix one or more errors, you can choose **Migrate** to migrate only the entities you fixed, without having to completely restart the migration.</span></span>  

> [!Tip]
> <span data-ttu-id="27a3a-130">Ef þú hefur lagað fleiri en eina villu geturðu notað **Velja fleira** valkostinn til að velja margar línur til að flytja.</span><span class="sxs-lookup"><span data-stu-id="27a3a-130">If you have fixed more than one error, you can use the **Select More** feature to select multiple lines to migrate.</span></span> <span data-ttu-id="27a3a-131">Ef villur eru til staðar sem ekki er mikilvægt að laga geturðu valið þær og svo **Sleppa vali**.</span><span class="sxs-lookup"><span data-stu-id="27a3a-131">Alternatively, if there are errors that are not important to fix, you can choose them and then choose **Skip Selections**.</span></span>

> [!Note]
> <span data-ttu-id="27a3a-132">Ef vörur eru til staðar sem er að finna í uppskrift gætir þú þurft að flytja oftar en einu sinni ef upprunalega varan er ekki stofnuð fyrir afbrigðið sem vísa til hennar.</span><span class="sxs-lookup"><span data-stu-id="27a3a-132">If you have items that are included in a BOM, you might need to migrate more than once if the original item is not created before the variants that reference it.</span></span> <span data-ttu-id="27a3a-133">Ef afbrigðið er búið til fyrst getur tilvísunin í upprunalegu vöruna valdið villuboðum.</span><span class="sxs-lookup"><span data-stu-id="27a3a-133">If an item variant is created first, the reference to the original item can cause an error message.</span></span>  

## <a name="verifying-data-after-migrating"></a><span data-ttu-id="27a3a-134">Staðfesting gagna eftir flutning</span><span class="sxs-lookup"><span data-stu-id="27a3a-134">Verifying Data After Migrating</span></span> 
<span data-ttu-id="27a3a-135">Ef þú vilt sannreyna að gögnin þín voru rétt flutt geturðu skoðað eftirfarandi síður í C5 og [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="27a3a-135">If you want to verify that your data migrated correctly, you can look at the following pages in C5 and [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

|<span data-ttu-id="27a3a-136">Microsoft Dynamcis C5 2012</span><span class="sxs-lookup"><span data-stu-id="27a3a-136">Microsoft Dynamcis C5 2012</span></span> | [!INCLUDE[d365fin](includes/d365fin_md.md)]|
|-----|-----|
|<span data-ttu-id="27a3a-137">Viðskm.færslur</span><span class="sxs-lookup"><span data-stu-id="27a3a-137">Customer Entries</span></span>| <span data-ttu-id="27a3a-138">Almennar færslubækur</span><span class="sxs-lookup"><span data-stu-id="27a3a-138">General Journals</span></span>|
|<span data-ttu-id="27a3a-139">Lánardr.færslur</span><span class="sxs-lookup"><span data-stu-id="27a3a-139">Vendor Entries</span></span>| <span data-ttu-id="27a3a-140">Almennar færslubækur</span><span class="sxs-lookup"><span data-stu-id="27a3a-140">General Journals</span></span>|
|<span data-ttu-id="27a3a-141">Birgðafærslur</span><span class="sxs-lookup"><span data-stu-id="27a3a-141">Item Entries</span></span>| <span data-ttu-id="27a3a-142">Birgðabækur</span><span class="sxs-lookup"><span data-stu-id="27a3a-142">Item Journals</span></span>|

<span data-ttu-id="27a3a-143">Í [!INCLUDE[d365fin](includes/d365fin_md.md)] er lotan fyrir fluttu gögnin kölluð **C5MIGRATE**.</span><span class="sxs-lookup"><span data-stu-id="27a3a-143">In [!INCLUDE[d365fin](includes/d365fin_md.md)], the batch for the migrated data is named **C5MIGRATE**.</span></span> 

## <a name="stopping-data-migration"></a><span data-ttu-id="27a3a-144">Stöðvun gagnaflutnings</span><span class="sxs-lookup"><span data-stu-id="27a3a-144">Stopping Data Migration</span></span>
<span data-ttu-id="27a3a-145">Þú getur hætt að flytja gögn með því að velja **Hætta við allan flutning**.</span><span class="sxs-lookup"><span data-stu-id="27a3a-145">You can stop migrating data by choosing **Stop All Migrations**.</span></span> <span data-ttu-id="27a3a-146">Ef þú gerir það er líka hætt við allan flutning sem bíður.</span><span class="sxs-lookup"><span data-stu-id="27a3a-146">If you do, all pending migrations are also stopped.</span></span>

## <a name="see-also"></a><span data-ttu-id="27a3a-147">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="27a3a-147">See Also</span></span>
<span data-ttu-id="27a3a-148">[Sérstilling [!INCLUDE[d365fin](includes/d365fin_md.md)] með viðbótum](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="27a3a-148">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions](ui-extensions.md)</span></span>  
<span data-ttu-id="27a3a-149">[Velkomin(n) í [!INCLUDE[d365fin](includes/d365fin_md.md)]](index.md)</span><span class="sxs-lookup"><span data-stu-id="27a3a-149">[Welcome to [!INCLUDE[d365fin](includes/d365fin_md.md)]](index.md)</span></span>  

