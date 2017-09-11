---
title: "Nota Excel til að flytja inn gögn í Financials| Microsoft Docs"
description: "Sjálfgefinn grunnstillingarpakki er notaður til að bæta við viðskiptamenn í Excel og flytja inn gögnin aftur í Dynamics 365 for Financials."
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: migration, Excel
ms.date: 07/05/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: 2a38dc36cb9ff609c5582acd489841b20013d4bc
ms.openlocfilehash: 8cf36afea60b089afac8f1c27d126cd19b88ce94
ms.contentlocale: is-is
ms.lasthandoff: 09/11/2017

---
# <a name="importing-data-from-legacy-accounting-software-using-a-configuration-package"></a><span data-ttu-id="806f5-103">Gögn flutt inn úr eldri bókhaldshugbúnaði með því að nota grunnstillingarpakka</span><span class="sxs-lookup"><span data-stu-id="806f5-103">Importing Data from Legacy Accounting Software using a Configuration Package</span></span>
<span data-ttu-id="806f5-104">Hægt er að flytja aðalgögn og sum færslugögn úr öðrum fjárhagskerfum á grundvelli sjálfgefins grunnstillingarpakka í [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="806f5-104">You can import master data and some transactional data from other finance systems based on the default configuration package in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="806f5-105">Í glugganum **Grunnstillingarpakkar** er hægt að vinna með pakka til að flytja inn og staðfesta gögnin áður en pakkinn er notaður.</span><span class="sxs-lookup"><span data-stu-id="806f5-105">In the **Configuration Packages** window, you can work with the package to import and validate the data before you apply the package.</span></span>  

<span data-ttu-id="806f5-106">Ef notandi þekkir RapidStart Services for Microsoft Dynamics, þekkir hann einnig grunnstillingarpakka.</span><span class="sxs-lookup"><span data-stu-id="806f5-106">If you are familiar with RapidStart Services for Microsoft Dynamics, you are also familiar with configuration packages.</span></span> <span data-ttu-id="806f5-107">Sjálfgefinn grunnstillingarpakki styður algengustu gerðir gagna sem notandi vill flytja inn úr eldra kerfi.</span><span class="sxs-lookup"><span data-stu-id="806f5-107">The default configuration package supports the most common types of data that you want to import from a legacy system.</span></span> <span data-ttu-id="806f5-108">Í Excel er þá hægt að bæta við gögnunum úr eldra kerfinu og setja þau upp í samræmi við viðskiptagrunn [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="806f5-108">In Excel, you can then add the data from the legacy system and set it up according to the business logic of the [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  

> [!TIP]  
>   <span data-ttu-id="806f5-109">Að öðrum kosti skal nota leiðsagnarforrit fyrir gagnafærslu til að flytja inn gögn frá QuickBooks eða Dynamics GP.</span><span class="sxs-lookup"><span data-stu-id="806f5-109">Alternatively, use data migration wizards to import data from QuickBooks or Dynamics GP.</span></span> <span data-ttu-id="806f5-110">Nánari upplýsingar, sjá [QuickBooks gagnafærsla](ui-extensions-quickbooks-data-migration.md) eða [Dynamics GP gagnafærsla](ui-extensions-dynamicsgp-data-migration.md).</span><span class="sxs-lookup"><span data-stu-id="806f5-110">For more information, see [QuickBooks Data Migration](ui-extensions-quickbooks-data-migration.md) or [Dynamics GP Data Migration](ui-extensions-dynamicsgp-data-migration.md).</span></span>  

## <a name="working-with-data-in-excel"></a><span data-ttu-id="806f5-111">Unnið með gögn í Excel</span><span class="sxs-lookup"><span data-stu-id="806f5-111">Working with Data in Excel</span></span>
<span data-ttu-id="806f5-112">Þegar sjálfgefinn grunnstillingarpakki er fluttur út í Excel inniheldur vinnubókin sem búin er til vinnublað fyrir hverja töflu í pakkanum.</span><span class="sxs-lookup"><span data-stu-id="806f5-112">When you export the default configuration package to Excel, the generated workbook contains a worksheet for each table in the package.</span></span> <span data-ttu-id="806f5-113">Til að einfalda verk er hægt að nýta XML-meðhöndlunarverkfærin sem byggð eru inn í Excel.</span><span class="sxs-lookup"><span data-stu-id="806f5-113">To simplify your tasks, you can take advantage of the XML manipulation tools that are built into Excel.</span></span> <span data-ttu-id="806f5-114">Einnig er hægt að nota Excel innbyggðar aðgerðir til aðstoða við gagnsnið og að setja gögn í réttan flokk.</span><span class="sxs-lookup"><span data-stu-id="806f5-114">You can also use Excel built-in functions to help with data formatting and to put data in the correct cell.</span></span> <span data-ttu-id="806f5-115">Til dæmis, bætið við auðu vinnublaði og afritið eldri gögnin á það.</span><span class="sxs-lookup"><span data-stu-id="806f5-115">For example, add a blank worksheet and copy the legacy data to it.</span></span> <span data-ttu-id="806f5-116">Búið því næst til Excel-formúlu til að varpa gögnum í umbreytingarvinnublaðinu á milli reitanna í útflutta vinnublaðinu og eldri gögnum viðskiptamanns.</span><span class="sxs-lookup"><span data-stu-id="806f5-116">Then make an Excel formula to map data in the transformation worksheet between the fields in the exported worksheet and customer legacy data.</span></span> <span data-ttu-id="806f5-117">Þegar búið er að varpa öllum gögnum, skal afrita afmörkun gagnanna á töflu á vinnublaðinu.</span><span class="sxs-lookup"><span data-stu-id="806f5-117">After you have mapped all of the data, copy the range of data onto the table worksheet.</span></span>  

> [!IMPORTANT]  
>  <span data-ttu-id="806f5-118">Ekki breyta dálkum í vinnublöðunum.</span><span class="sxs-lookup"><span data-stu-id="806f5-118">Do not change the columns in the worksheets.</span></span> <span data-ttu-id="806f5-119">Ef gögnin eru færð, þeim breytt eða þeim eytt er ekki hægt að flytja vinnublaðið inn í [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="806f5-119">If they are moved, changed, or deleted, the worksheet cannot be imported into [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

## <a name="tables-in-the-default-configuration-package"></a><span data-ttu-id="806f5-120">Töflur í sjálfgefnum grunnstillingarpakka</span><span class="sxs-lookup"><span data-stu-id="806f5-120">Tables in the Default Configuration Package</span></span>
<span data-ttu-id="806f5-121">Sjálfgefni grunnstillingarpakkinn styður eftirfarandi töflur:</span><span class="sxs-lookup"><span data-stu-id="806f5-121">The default configuration package supports the following tables:</span></span>

-   <span data-ttu-id="806f5-122">Greiðsluskilmálar</span><span class="sxs-lookup"><span data-stu-id="806f5-122">Payment Terms</span></span>
-   <span data-ttu-id="806f5-123">Verðflokkur viðskiptamanna</span><span class="sxs-lookup"><span data-stu-id="806f5-123">Customer Price Group</span></span>
-   <span data-ttu-id="806f5-124">Afhendingarmáti</span><span class="sxs-lookup"><span data-stu-id="806f5-124">Shipment Method</span></span>
-   <span data-ttu-id="806f5-125">Sölumaður/innkaupaaðili</span><span class="sxs-lookup"><span data-stu-id="806f5-125">Salesperson/Purchaser</span></span>
-   <span data-ttu-id="806f5-126">Birgðageymsla</span><span class="sxs-lookup"><span data-stu-id="806f5-126">Location</span></span>
-   <span data-ttu-id="806f5-127">Fjárhagsreikningur</span><span class="sxs-lookup"><span data-stu-id="806f5-127">GL Account</span></span>
-   <span data-ttu-id="806f5-128">Viðskiptavinur</span><span class="sxs-lookup"><span data-stu-id="806f5-128">Customer</span></span>
-   <span data-ttu-id="806f5-129">Lánardrottinn</span><span class="sxs-lookup"><span data-stu-id="806f5-129">Vendor</span></span>
-   <span data-ttu-id="806f5-130">Atriði</span><span class="sxs-lookup"><span data-stu-id="806f5-130">Item</span></span>
-   <span data-ttu-id="806f5-131">Söluhaus</span><span class="sxs-lookup"><span data-stu-id="806f5-131">Sales Header</span></span>
-   <span data-ttu-id="806f5-132">Sölulína</span><span class="sxs-lookup"><span data-stu-id="806f5-132">Sales Line</span></span>
-   <span data-ttu-id="806f5-133">Innkaupahaus</span><span class="sxs-lookup"><span data-stu-id="806f5-133">Purchase Header</span></span>
-   <span data-ttu-id="806f5-134">Innkaupalína</span><span class="sxs-lookup"><span data-stu-id="806f5-134">Purchase Line</span></span>
-   <span data-ttu-id="806f5-135">Fh.færslubókarlína</span><span class="sxs-lookup"><span data-stu-id="806f5-135">Gen. Journal Line</span></span>
-   <span data-ttu-id="806f5-136">Birgðabókarlína</span><span class="sxs-lookup"><span data-stu-id="806f5-136">Item Journal Line</span></span>
-   <span data-ttu-id="806f5-137">Bókunarflokkur viðskm.</span><span class="sxs-lookup"><span data-stu-id="806f5-137">Customer Posting Group</span></span>
-   <span data-ttu-id="806f5-138">Bókunarflokkur lánardr.</span><span class="sxs-lookup"><span data-stu-id="806f5-138">Vendor Posting Group</span></span>
-   <span data-ttu-id="806f5-139">Birgðabókunarflokkur</span><span class="sxs-lookup"><span data-stu-id="806f5-139">Inventory Posting Group</span></span>
-   <span data-ttu-id="806f5-140">Mælieining</span><span class="sxs-lookup"><span data-stu-id="806f5-140">Unit of Measure</span></span>
-   <span data-ttu-id="806f5-141">Alm. viðskiptabókunarflokkur</span><span class="sxs-lookup"><span data-stu-id="806f5-141">Gen. Business Posting Group</span></span>
-   <span data-ttu-id="806f5-142">Alm. vörubókunarflokkur</span><span class="sxs-lookup"><span data-stu-id="806f5-142">Gen. Product Posting Group</span></span>
-   <span data-ttu-id="806f5-143">Almennur bókunargrunnur</span><span class="sxs-lookup"><span data-stu-id="806f5-143">General Posting Setup</span></span>
-   <span data-ttu-id="806f5-144">Umsjónarsvæði</span><span class="sxs-lookup"><span data-stu-id="806f5-144">Territory</span></span>
-   <span data-ttu-id="806f5-145">Vöruflokkur</span><span class="sxs-lookup"><span data-stu-id="806f5-145">Item Category</span></span>
-   <span data-ttu-id="806f5-146">Söluverð</span><span class="sxs-lookup"><span data-stu-id="806f5-146">Sales Price</span></span>
-   <span data-ttu-id="806f5-147">Innkaupsverð</span><span class="sxs-lookup"><span data-stu-id="806f5-147">Purchase Price</span></span>

## <a name="importing-customer-data"></a><span data-ttu-id="806f5-148">Flytur inn viðskiptamannagögn</span><span class="sxs-lookup"><span data-stu-id="806f5-148">Importing Customer Data</span></span>
<span data-ttu-id="806f5-149">Eftir að gögn um viðskiptamenn eru færð inn í Excel, eru gögnin flutt inn í [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="806f5-149">After the customer data has been entered in Excel, you import the data into [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="806f5-150">Í glugganum **Grunnstillingarpakkar** eru gögnin flutt inn úr Excel-skránni og hægt er að sannprófa að gögnin séu í samræmi við [!INCLUDE[d365fin](includes/d365fin_md.md)] áður en pakkinn er notaður.</span><span class="sxs-lookup"><span data-stu-id="806f5-150">In the **Configuration Packages** window, you import the data from the Excel file, and you can validate that the data is consistent with [!INCLUDE[d365fin](includes/d365fin_md.md)] before you apply the package.</span></span>

## <a name="see-also"></a><span data-ttu-id="806f5-151">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="806f5-151">See Also</span></span>
[<span data-ttu-id="806f5-152">Innflutningur viðskiptagagna úr öðrum fjárhagskerfum</span><span class="sxs-lookup"><span data-stu-id="806f5-152">Importing Business Data from Other Finance Systems</span></span>](upload-data.md)  
[<span data-ttu-id="806f5-153">QuickBooks gagnaflutningur</span><span class="sxs-lookup"><span data-stu-id="806f5-153">QuickBooks Data Migration</span></span>](ui-extensions-quickbooks-data-migration.md)  
[<span data-ttu-id="806f5-154">Dynamics GP Gagnafærsla</span><span class="sxs-lookup"><span data-stu-id="806f5-154">Dynamics GP Data Migration</span></span>](ui-extensions-dynamicsgp-data-migration.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]

