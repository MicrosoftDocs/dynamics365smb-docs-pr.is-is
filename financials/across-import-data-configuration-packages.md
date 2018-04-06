---
title: "Nota Excel til að flytja inn gögn í Financials| Microsoft Docs"
description: "Sjálfgefinn grunnstillingarpakki er notaður til að bæta við viðskiptamenn í Excel og flytja inn gögnin aftur í Finance and Operations, Business Edition."
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: migration, Excel
ms.date: 03/07/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 591d8100100ee717a932d188a87545fe4098a001
ms.contentlocale: is-is
ms.lasthandoff: 03/22/2018

---
# <a name="importing-data-from-legacy-accounting-software-using-a-configuration-package"></a><span data-ttu-id="8f5ec-103">Gögn flutt inn úr eldri bókhaldshugbúnaði með því að nota grunnstillingarpakka</span><span class="sxs-lookup"><span data-stu-id="8f5ec-103">Importing Data from Legacy Accounting Software using a Configuration Package</span></span>
<span data-ttu-id="8f5ec-104">Hægt er að flytja aðalgögn og sum færslugögn úr öðrum fjárhagskerfum á grundvelli sjálfgefins grunnstillingarpakka í [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="8f5ec-104">You can import master data and some transactional data from other finance systems based on the default configuration package in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="8f5ec-105">Í glugganum **Grunnstillingarpakkar** er hægt að vinna með pakka til að flytja inn og staðfesta gögnin áður en pakkinn er notaður.</span><span class="sxs-lookup"><span data-stu-id="8f5ec-105">In the **Configuration Packages** window, you can work with the package to import and validate the data before you apply the package.</span></span>  

> [!NOTE]  
> <span data-ttu-id="8f5ec-106">Grunnstillingarpakkar eru hluti af RapidStart Services fyrir [!INCLUDE[d365fin](includes/d365fin_md.md)], víðtækt verkfærasafn til að setja upp nýjar lausnir sem byggjast á viðskiptakröfum viðskiptavina og uppsetningargögnum.</span><span class="sxs-lookup"><span data-stu-id="8f5ec-106">Configuration packages are part of RapidStart Services for [!INCLUDE[d365fin](includes/d365fin_md.md)], an extensive toolkit for setting up new solutions based on customers' business requirements and setup data.</span></span> <span data-ttu-id="8f5ec-107">RapidStart Services býður einnig upp á virkni til innflutnings á eldri gögnum.</span><span class="sxs-lookup"><span data-stu-id="8f5ec-107">RapidStart Services also offers functionality for import of legacy data.</span></span> <span data-ttu-id="8f5ec-108">Nánari upplýsingar er að finna í [Uppsetning fyrirtækis með RapidStart Services](admin-set-up-a-company-with-rapidstart.md).</span><span class="sxs-lookup"><span data-stu-id="8f5ec-108">For more information, see [Setting Up a Company With RapidStart Services](admin-set-up-a-company-with-rapidstart.md).</span></span>

> [!TIP]  
>   <span data-ttu-id="8f5ec-109">Að öðrum kosti skal nota leiðsagnarforrit fyrir gagnafærslu til að flytja inn gögn frá QuickBooks eða Dynamics GP.</span><span class="sxs-lookup"><span data-stu-id="8f5ec-109">Alternatively, use data migration wizards to import data from QuickBooks or Dynamics GP.</span></span> <span data-ttu-id="8f5ec-110">Nánari upplýsingar, sjá [QuickBooks gagnafærsla](ui-extensions-quickbooks-data-migration.md) eða [Dynamics GP gagnafærsla](ui-extensions-dynamicsgp-data-migration.md).</span><span class="sxs-lookup"><span data-stu-id="8f5ec-110">For more information, see [QuickBooks Data Migration](ui-extensions-quickbooks-data-migration.md) or [Dynamics GP Data Migration](ui-extensions-dynamicsgp-data-migration.md).</span></span>  

## <a name="working-with-data-in-excel"></a><span data-ttu-id="8f5ec-111">Unnið með gögn í Excel</span><span class="sxs-lookup"><span data-stu-id="8f5ec-111">Working with Data in Excel</span></span>
<span data-ttu-id="8f5ec-112">Þegar sjálfgefinn grunnstillingarpakki er fluttur út í Excel inniheldur vinnubókin sem búin er til vinnublað fyrir hverja töflu í pakkanum.</span><span class="sxs-lookup"><span data-stu-id="8f5ec-112">When you export the default configuration package to Excel, the generated workbook contains a worksheet for each table in the package.</span></span> <span data-ttu-id="8f5ec-113">Til að einfalda verk er hægt að nýta XML-meðhöndlunarverkfærin sem byggð eru inn í Excel.</span><span class="sxs-lookup"><span data-stu-id="8f5ec-113">To simplify your tasks, you can take advantage of the XML manipulation tools that are built into Excel.</span></span> <span data-ttu-id="8f5ec-114">Einnig er hægt að nota Excel innbyggðar aðgerðir til aðstoða við gagnsnið og að setja gögn í réttan flokk.</span><span class="sxs-lookup"><span data-stu-id="8f5ec-114">You can also use Excel built-in functions to help with data formatting and to put data in the correct cell.</span></span> <span data-ttu-id="8f5ec-115">Til dæmis, bætið við auðu vinnublaði og afritið eldri gögnin á það.</span><span class="sxs-lookup"><span data-stu-id="8f5ec-115">For example, add a blank worksheet and copy the legacy data to it.</span></span> <span data-ttu-id="8f5ec-116">Búið því næst til Excel-formúlu til að varpa gögnum í umbreytingarvinnublaðinu á milli reitanna í útflutta vinnublaðinu og eldri gögnum viðskiptamanns.</span><span class="sxs-lookup"><span data-stu-id="8f5ec-116">Then make an Excel formula to map data in the transformation worksheet between the fields in the exported worksheet and customer legacy data.</span></span> <span data-ttu-id="8f5ec-117">Þegar búið er að varpa öllum gögnum, skal afrita afmörkun gagnanna á töflu á vinnublaðinu.</span><span class="sxs-lookup"><span data-stu-id="8f5ec-117">After you have mapped all of the data, copy the range of data onto the table worksheet.</span></span>  

> [!IMPORTANT]  
>  <span data-ttu-id="8f5ec-118">Ekki breyta dálkum í vinnublöðunum.</span><span class="sxs-lookup"><span data-stu-id="8f5ec-118">Do not change the columns in the worksheets.</span></span> <span data-ttu-id="8f5ec-119">Ef gögnin eru færð, þeim breytt eða þeim eytt er ekki hægt að flytja vinnublaðið inn í [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="8f5ec-119">If they are moved, changed, or deleted, the worksheet cannot be imported into [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

## <a name="tables-in-the-default-configuration-package"></a><span data-ttu-id="8f5ec-120">Töflur í sjálfgefnum grunnstillingarpakka</span><span class="sxs-lookup"><span data-stu-id="8f5ec-120">Tables in the Default Configuration Package</span></span>
<span data-ttu-id="8f5ec-121">Sjálfgefni grunnstillingarpakkinn styður eftirfarandi töflur:</span><span class="sxs-lookup"><span data-stu-id="8f5ec-121">The default configuration package supports the following tables:</span></span>

-   <span data-ttu-id="8f5ec-122">Greiðsluskilmálar</span><span class="sxs-lookup"><span data-stu-id="8f5ec-122">Payment Terms</span></span>
-   <span data-ttu-id="8f5ec-123">Verðflokkur viðskiptamanna</span><span class="sxs-lookup"><span data-stu-id="8f5ec-123">Customer Price Group</span></span>
-   <span data-ttu-id="8f5ec-124">Afhendingarmáti</span><span class="sxs-lookup"><span data-stu-id="8f5ec-124">Shipment Method</span></span>
-   <span data-ttu-id="8f5ec-125">Sölumaður/innkaupaaðili</span><span class="sxs-lookup"><span data-stu-id="8f5ec-125">Salesperson/Purchaser</span></span>
-   <span data-ttu-id="8f5ec-126">Birgðageymsla</span><span class="sxs-lookup"><span data-stu-id="8f5ec-126">Location</span></span>
-   <span data-ttu-id="8f5ec-127">Fjárhagsreikningur</span><span class="sxs-lookup"><span data-stu-id="8f5ec-127">GL Account</span></span>
-   <span data-ttu-id="8f5ec-128">Viðskiptavinur</span><span class="sxs-lookup"><span data-stu-id="8f5ec-128">Customer</span></span>
-   <span data-ttu-id="8f5ec-129">Lánardrottinn</span><span class="sxs-lookup"><span data-stu-id="8f5ec-129">Vendor</span></span>
-   <span data-ttu-id="8f5ec-130">Atriði</span><span class="sxs-lookup"><span data-stu-id="8f5ec-130">Item</span></span>
-   <span data-ttu-id="8f5ec-131">Söluhaus</span><span class="sxs-lookup"><span data-stu-id="8f5ec-131">Sales Header</span></span>
-   <span data-ttu-id="8f5ec-132">Sölulína</span><span class="sxs-lookup"><span data-stu-id="8f5ec-132">Sales Line</span></span>
-   <span data-ttu-id="8f5ec-133">Innkaupahaus</span><span class="sxs-lookup"><span data-stu-id="8f5ec-133">Purchase Header</span></span>
-   <span data-ttu-id="8f5ec-134">Innkaupalína</span><span class="sxs-lookup"><span data-stu-id="8f5ec-134">Purchase Line</span></span>
-   <span data-ttu-id="8f5ec-135">Fh.færslubókarlína</span><span class="sxs-lookup"><span data-stu-id="8f5ec-135">Gen. Journal Line</span></span>
-   <span data-ttu-id="8f5ec-136">Birgðabókarlína</span><span class="sxs-lookup"><span data-stu-id="8f5ec-136">Item Journal Line</span></span>
-   <span data-ttu-id="8f5ec-137">Bókunarflokkur viðskm.</span><span class="sxs-lookup"><span data-stu-id="8f5ec-137">Customer Posting Group</span></span>
-   <span data-ttu-id="8f5ec-138">Bókunarflokkur lánardr.</span><span class="sxs-lookup"><span data-stu-id="8f5ec-138">Vendor Posting Group</span></span>
-   <span data-ttu-id="8f5ec-139">Birgðabókunarflokkur</span><span class="sxs-lookup"><span data-stu-id="8f5ec-139">Inventory Posting Group</span></span>
-   <span data-ttu-id="8f5ec-140">Mælieining</span><span class="sxs-lookup"><span data-stu-id="8f5ec-140">Unit of Measure</span></span>
-   <span data-ttu-id="8f5ec-141">Alm. viðskiptabókunarflokkur</span><span class="sxs-lookup"><span data-stu-id="8f5ec-141">Gen. Business Posting Group</span></span>
-   <span data-ttu-id="8f5ec-142">Alm. vörubókunarflokkur</span><span class="sxs-lookup"><span data-stu-id="8f5ec-142">Gen. Product Posting Group</span></span>
-   <span data-ttu-id="8f5ec-143">Almennur bókunargrunnur</span><span class="sxs-lookup"><span data-stu-id="8f5ec-143">General Posting Setup</span></span>
-   <span data-ttu-id="8f5ec-144">Umsjónarsvæði</span><span class="sxs-lookup"><span data-stu-id="8f5ec-144">Territory</span></span>
-   <span data-ttu-id="8f5ec-145">Vöruflokkur</span><span class="sxs-lookup"><span data-stu-id="8f5ec-145">Item Category</span></span>
-   <span data-ttu-id="8f5ec-146">Söluverð</span><span class="sxs-lookup"><span data-stu-id="8f5ec-146">Sales Price</span></span>
-   <span data-ttu-id="8f5ec-147">Innkaupsverð</span><span class="sxs-lookup"><span data-stu-id="8f5ec-147">Purchase Price</span></span>

## <a name="importing-customer-data"></a><span data-ttu-id="8f5ec-148">Flytur inn viðskiptamannagögn</span><span class="sxs-lookup"><span data-stu-id="8f5ec-148">Importing Customer Data</span></span>
<span data-ttu-id="8f5ec-149">Eftir að gögn um viðskiptamenn eru færð inn í Excel, eru gögnin flutt inn í [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="8f5ec-149">After the customer data has been entered in Excel, you import the data into [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="8f5ec-150">Í glugganum **Grunnstillingarpakkar** eru gögnin flutt inn úr Excel-skránni og hægt er að sannprófa að gögnin séu í samræmi við [!INCLUDE[d365fin](includes/d365fin_md.md)] áður en pakkinn er notaður.</span><span class="sxs-lookup"><span data-stu-id="8f5ec-150">In the **Configuration Packages** window, you import the data from the Excel file, and you can validate that the data is consistent with [!INCLUDE[d365fin](includes/d365fin_md.md)] before you apply the package.</span></span>

## <a name="see-also"></a><span data-ttu-id="8f5ec-151">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="8f5ec-151">See Also</span></span>
[<span data-ttu-id="8f5ec-152">Innflutningur viðskiptagagna úr öðrum fjárhagskerfum</span><span class="sxs-lookup"><span data-stu-id="8f5ec-152">Importing Business Data from Other Finance Systems</span></span>](upload-data.md)  
[<span data-ttu-id="8f5ec-153">Uppsetning fyrirtækis með RapidStart Services</span><span class="sxs-lookup"><span data-stu-id="8f5ec-153">Setting Up a Company With RapidStart Services</span></span>](admin-set-up-a-company-with-rapidstart.md)  
[<span data-ttu-id="8f5ec-154">QuickBooks gagnaflutningur</span><span class="sxs-lookup"><span data-stu-id="8f5ec-154">QuickBooks Data Migration</span></span>](ui-extensions-quickbooks-data-migration.md)  
[<span data-ttu-id="8f5ec-155">Dynamics GP Gagnafærsla</span><span class="sxs-lookup"><span data-stu-id="8f5ec-155">Dynamics GP Data Migration</span></span>](ui-extensions-dynamicsgp-data-migration.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
## [!INCLUDE[d365fin](includes/training_link_md.md)]

