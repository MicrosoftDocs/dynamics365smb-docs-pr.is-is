---
title: "Nota Excel til að flytja inn gögn í Financials| Microsoft Docs"
description: "Sjálfgefinn grunnstillingarpakki er notaður til að bæta við viðskiptamenn í Excel og flytja inn gögnin aftur í Business Central."
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: migration, Excel
ms.date: 05/17/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: ad1b888d475c0523c5a905e804a3f89ab4531b28
ms.openlocfilehash: 379cfd2731bba2df6f5e31d2b8de2d72e2064ebb
ms.contentlocale: is-is
ms.lasthandoff: 05/17/2018

---
# <a name="importing-business-data-from-other-finance-systems"></a><span data-ttu-id="63813-103">Innflutningur viðskiptagagna úr öðrum fjárhagskerfum</span><span class="sxs-lookup"><span data-stu-id="63813-103">Importing Business Data from Other Finance Systems</span></span>
<span data-ttu-id="63813-104">Þegar notandi skráir sig í [!INCLUDE[d365fin](includes/d365fin_md.md)], er hægt að ákveða að búa til autt fyrirtæki svo hægt sé að hlaða upp eigin gögnum og prófa áfram nýja [!INCLUDE[d365fin](includes/d365fin_md.md)] fyrirtækið.</span><span class="sxs-lookup"><span data-stu-id="63813-104">When you sign up for [!INCLUDE[d365fin](includes/d365fin_md.md)], you can choose to create an empty company so that you can upload your own data and to test your new [!INCLUDE[d365fin](includes/d365fin_md.md)] company.</span></span> <span data-ttu-id="63813-105">Það fer eftir því fjárhagskerfi sem fyrirtækið notar í dag hvernig og hvort hægt er að millifæra upplýsingar um viðskiptamenn, lánardrottna, birgðir og bankareikninga.</span><span class="sxs-lookup"><span data-stu-id="63813-105">Depending on the finance solution that your business uses today, you can transfer information about customers, vendors, inventory, and bank accounts.</span></span>  

<span data-ttu-id="63813-106">Hægt er að ræsa leiðarvísi um uppsetningu með hjálp frá Mitt hlutverk sem hjálpar til við að flytja viðskiptagögn úr Excel-skrá eða öðrum sniðum.</span><span class="sxs-lookup"><span data-stu-id="63813-106">From the Role Center, you can start an assisted setup guide that helps you transfer the business data from an Excel file or from other formats.</span></span> <span data-ttu-id="63813-107">Þær skráategundir sem hægt er að hlaða upp fer eftir viðbótunum sem í boði eru.</span><span class="sxs-lookup"><span data-stu-id="63813-107">The type of files you can upload depends on the extensions that are available.</span></span> <span data-ttu-id="63813-108">Til dæmis er hægt að yfirfæra gögn úr QuickBooks vegna þess að [!INCLUDE[d365fin](includes/d365fin_md.md)] felur í sér viðbót sem sér um umbreytingu úr QuickBooks.</span><span class="sxs-lookup"><span data-stu-id="63813-108">For example, you can migrate data from QuickBooks because [!INCLUDE[d365fin](includes/d365fin_md.md)] includes an extension that handles the conversion from QuickBooks.</span></span> <span data-ttu-id="63813-109">Ef notandi vill yfirfæra gögn úr öðrum fjárhagskerfum þarf annað hvort að athuga hvort viðbót er í boði fyrir það kerfi eða flytja gögnin inn úr Excel.</span><span class="sxs-lookup"><span data-stu-id="63813-109">If you want to migrate data from other finance solutions, you must either check if an extension is available for that solution or import from Excel.</span></span>  

[!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="63813-110"> inniheldur sniðmát fyrir viðskiptamenn, lánardrottna og birgðavörur sem hægt er að nota þegar gögnum er hlaðið upp.</span><span class="sxs-lookup"><span data-stu-id="63813-110"> includes templates for accounts, customers, vendors, and inventory items that you can choose to apply when you import your data.</span></span>

<span data-ttu-id="63813-111">Hægt er að flytja aðalgögn og sum færslugögn úr öðrum fjárhagskerfum á grundvelli sjálfgefins grunnstillingarpakka í [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="63813-111">You can import master data and some transactional data from other finance systems based on the default configuration package in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="63813-112">Í glugganum **Grunnstillingarpakkar** er hægt að vinna með pakka til að flytja inn og staðfesta gögnin áður en pakkinn er notaður.</span><span class="sxs-lookup"><span data-stu-id="63813-112">In the **Configuration Packages** window, you can work with the package to import and validate the data before you apply the package.</span></span>  

> [!TIP]  
> <span data-ttu-id="63813-113">Að öðrum kosti skal nota leiðsagnarforrit fyrir gagnafærslu til að flytja inn gögn frá QuickBooks eða Dynamics GP.</span><span class="sxs-lookup"><span data-stu-id="63813-113">Alternatively, use data migration wizards to import data from QuickBooks or Dynamics GP.</span></span> <span data-ttu-id="63813-114">Nánari upplýsingar, sjá [QuickBooks gagnafærsla](ui-extensions-quickbooks-data-migration.md) eða [Dynamics GP gagnafærsla](ui-extensions-dynamicsgp-data-migration.md).</span><span class="sxs-lookup"><span data-stu-id="63813-114">For more information, see [QuickBooks Data Migration](ui-extensions-quickbooks-data-migration.md) or [Dynamics GP Data Migration](ui-extensions-dynamicsgp-data-migration.md).</span></span>

> [!NOTE]  
> <span data-ttu-id="63813-115">Fyrir stærri innleiðingarverk getur þú notað RapidStart Services fyrir [!INCLUDE[d365fin](includes/d365fin_md.md)], sem er vítækt verkfærasafn til að setja upp nýjar lausnir sem byggjast á viðskiptakröfum viðskiptavina og uppsetningargögnum.</span><span class="sxs-lookup"><span data-stu-id="63813-115">For larger implementation work, you can use RapidStart Services for [!INCLUDE[d365fin](includes/d365fin_md.md)], which is an extensive toolkit for setting up new solutions based on customers' business requirements and setup data.</span></span> <span data-ttu-id="63813-116">RapidStart Services býður einnig upp á virkni til að flytja inn viðskiptagögn.</span><span class="sxs-lookup"><span data-stu-id="63813-116">RapidStart Services also offers functionality for import of business data.</span></span> <span data-ttu-id="63813-117">Nánari upplýsingar er að finna í [Uppsetning fyrirtækis með RapidStart Services](admin-set-up-a-company-with-rapidstart.md).</span><span class="sxs-lookup"><span data-stu-id="63813-117">For more information, see [Setting Up a Company With RapidStart Services](admin-set-up-a-company-with-rapidstart.md).</span></span>

## <a name="importing-data-from-configuration-packages"></a><span data-ttu-id="63813-118">Innflutningur gagna úr grunnstillingarpakka</span><span class="sxs-lookup"><span data-stu-id="63813-118">Importing Data from Configuration Packages</span></span>
[!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="63813-119"> inniheldur stillingarpakka sem þú getur flutt út í Excel og sett upp gögnin þín þar.</span><span class="sxs-lookup"><span data-stu-id="63813-119"> includes a configuration package that you can export to Excel and set up your data there.</span></span> <span data-ttu-id="63813-120">Síðan er hægt að flytja aftur inn gögnin úr Excel.</span><span class="sxs-lookup"><span data-stu-id="63813-120">Then, you can import the data from Excel again.</span></span> <span data-ttu-id="63813-121">Pakkinn samanstendur af 27 töflum, þar með talið aðalgögnum, svo sem viðskiptavinum, söluaðilum, hlutum og reikningum, öðrum grunnuppsetningartöflum eins og sendingarkostnaði og viðskiptatöflum eins og söluhaus og línum.</span><span class="sxs-lookup"><span data-stu-id="63813-121">The package consists of 27 tables, including master data such as customers, vendors, items, and accounts, other basic setup tables such as shipping methods, and transactions tables such as sales header and lines.</span></span>  

> [!NOTE]  
>   <span data-ttu-id="63813-122">Vinna með stillingarpakka er ítarleg virkni og við mælum með að þú hafir samband við kerfisstjórann þinn.</span><span class="sxs-lookup"><span data-stu-id="63813-122">Working with configuration packages is advanced functionality, and we recommend that you contact your administrator.</span></span> <span data-ttu-id="63813-123">Nánari upplýsingar eru í [Gögn flutt inn úr eldri bókhaldshugbúnaði með því að nota grunnstillingarpakka](across-import-data-configuration-packages.md).</span><span class="sxs-lookup"><span data-stu-id="63813-123">For more information, see [Importing Data from Legacy Accounting Software using a Configuration Package](across-import-data-configuration-packages.md).</span></span>

## <a name="working-with-data-in-excel"></a><span data-ttu-id="63813-124">Unnið með gögn í Excel</span><span class="sxs-lookup"><span data-stu-id="63813-124">Working with Data in Excel</span></span>
<span data-ttu-id="63813-125">Þegar sjálfgefinn grunnstillingarpakki er fluttur út í Excel inniheldur vinnubókin sem búin er til vinnublað fyrir hverja töflu í pakkanum.</span><span class="sxs-lookup"><span data-stu-id="63813-125">When you export the default configuration package to Excel, the generated workbook contains a worksheet for each table in the package.</span></span> <span data-ttu-id="63813-126">Til að einfalda verk er hægt að nýta XML-meðhöndlunarverkfærin sem byggð eru inn í Excel.</span><span class="sxs-lookup"><span data-stu-id="63813-126">To simplify your tasks, you can take advantage of the XML manipulation tools that are built into Excel.</span></span> <span data-ttu-id="63813-127">Einnig er hægt að nota Excel innbyggðar aðgerðir til aðstoða við gagnsnið og að setja gögn í réttan flokk.</span><span class="sxs-lookup"><span data-stu-id="63813-127">You can also use Excel built-in functions to help with data formatting and to put data in the correct cell.</span></span> <span data-ttu-id="63813-128">Til dæmis, bætið við auðu vinnublaði og afritið eldri gögnin á það.</span><span class="sxs-lookup"><span data-stu-id="63813-128">For example, add a blank worksheet and copy the legacy data to it.</span></span> <span data-ttu-id="63813-129">Búið því næst til Excel-formúlu til að varpa gögnum í umbreytingarvinnublaðinu á milli reitanna í útflutta vinnublaðinu og eldri gögnum viðskiptamanns.</span><span class="sxs-lookup"><span data-stu-id="63813-129">Then make an Excel formula to map data in the transformation worksheet between the fields in the exported worksheet and customer legacy data.</span></span> <span data-ttu-id="63813-130">Þegar búið er að varpa öllum gögnum, skal afrita afmörkun gagnanna á töflu á vinnublaðinu.</span><span class="sxs-lookup"><span data-stu-id="63813-130">After you have mapped all of the data, copy the range of data onto the table worksheet.</span></span>  

> [!IMPORTANT]  
>  <span data-ttu-id="63813-131">Ekki breyta dálkum í vinnublöðunum.</span><span class="sxs-lookup"><span data-stu-id="63813-131">Do not change the columns in the worksheets.</span></span> <span data-ttu-id="63813-132">Ef gögnin eru færð, þeim breytt eða þeim eytt er ekki hægt að flytja vinnublaðið inn í [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="63813-132">If they are moved, changed, or deleted, the worksheet cannot be imported into [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

## <a name="tables-in-the-default-configuration-package"></a><span data-ttu-id="63813-133">Töflur í sjálfgefnum grunnstillingarpakka</span><span class="sxs-lookup"><span data-stu-id="63813-133">Tables in the Default Configuration Package</span></span>
<span data-ttu-id="63813-134">Sjálfgefni grunnstillingarpakkinn styður eftirfarandi töflur:</span><span class="sxs-lookup"><span data-stu-id="63813-134">The default configuration package supports the following tables:</span></span>

-   <span data-ttu-id="63813-135">Greiðsluskilmálar</span><span class="sxs-lookup"><span data-stu-id="63813-135">Payment Terms</span></span>
-   <span data-ttu-id="63813-136">Verðflokkur viðskiptamanna</span><span class="sxs-lookup"><span data-stu-id="63813-136">Customer Price Group</span></span>
-   <span data-ttu-id="63813-137">Afhendingarmáti</span><span class="sxs-lookup"><span data-stu-id="63813-137">Shipment Method</span></span>
-   <span data-ttu-id="63813-138">Sölumaður/innkaupaaðili</span><span class="sxs-lookup"><span data-stu-id="63813-138">Salesperson/Purchaser</span></span>
-   <span data-ttu-id="63813-139">Birgðageymsla</span><span class="sxs-lookup"><span data-stu-id="63813-139">Location</span></span>
-   <span data-ttu-id="63813-140">Fjárhagsreikningur</span><span class="sxs-lookup"><span data-stu-id="63813-140">GL Account</span></span>
-   <span data-ttu-id="63813-141">Viðskiptavinur</span><span class="sxs-lookup"><span data-stu-id="63813-141">Customer</span></span>
-   <span data-ttu-id="63813-142">Lánardrottinn</span><span class="sxs-lookup"><span data-stu-id="63813-142">Vendor</span></span>
-   <span data-ttu-id="63813-143">Atriði</span><span class="sxs-lookup"><span data-stu-id="63813-143">Item</span></span>
-   <span data-ttu-id="63813-144">Söluhaus</span><span class="sxs-lookup"><span data-stu-id="63813-144">Sales Header</span></span>
-   <span data-ttu-id="63813-145">Sölulína</span><span class="sxs-lookup"><span data-stu-id="63813-145">Sales Line</span></span>
-   <span data-ttu-id="63813-146">Innkaupahaus</span><span class="sxs-lookup"><span data-stu-id="63813-146">Purchase Header</span></span>
-   <span data-ttu-id="63813-147">Innkaupalína</span><span class="sxs-lookup"><span data-stu-id="63813-147">Purchase Line</span></span>
-   <span data-ttu-id="63813-148">Fh.færslubókarlína</span><span class="sxs-lookup"><span data-stu-id="63813-148">Gen. Journal Line</span></span>
-   <span data-ttu-id="63813-149">Birgðabókarlína</span><span class="sxs-lookup"><span data-stu-id="63813-149">Item Journal Line</span></span>
-   <span data-ttu-id="63813-150">Bókunarflokkur viðskm.</span><span class="sxs-lookup"><span data-stu-id="63813-150">Customer Posting Group</span></span>
-   <span data-ttu-id="63813-151">Bókunarflokkur lánardr.</span><span class="sxs-lookup"><span data-stu-id="63813-151">Vendor Posting Group</span></span>
-   <span data-ttu-id="63813-152">Birgðabókunarflokkur</span><span class="sxs-lookup"><span data-stu-id="63813-152">Inventory Posting Group</span></span>
-   <span data-ttu-id="63813-153">Mælieining</span><span class="sxs-lookup"><span data-stu-id="63813-153">Unit of Measure</span></span>
-   <span data-ttu-id="63813-154">Alm. viðskiptabókunarflokkur</span><span class="sxs-lookup"><span data-stu-id="63813-154">Gen. Business Posting Group</span></span>
-   <span data-ttu-id="63813-155">Alm. vörubókunarflokkur</span><span class="sxs-lookup"><span data-stu-id="63813-155">Gen. Product Posting Group</span></span>
-   <span data-ttu-id="63813-156">Almennur bókunargrunnur</span><span class="sxs-lookup"><span data-stu-id="63813-156">General Posting Setup</span></span>
-   <span data-ttu-id="63813-157">Umsjónarsvæði</span><span class="sxs-lookup"><span data-stu-id="63813-157">Territory</span></span>
-   <span data-ttu-id="63813-158">Vöruflokkur</span><span class="sxs-lookup"><span data-stu-id="63813-158">Item Category</span></span>
-   <span data-ttu-id="63813-159">Söluverð</span><span class="sxs-lookup"><span data-stu-id="63813-159">Sales Price</span></span>
-   <span data-ttu-id="63813-160">Innkaupsverð</span><span class="sxs-lookup"><span data-stu-id="63813-160">Purchase Price</span></span>

## <a name="see-also"></a><span data-ttu-id="63813-161">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="63813-161">See Also</span></span>
[<span data-ttu-id="63813-162">Uppsetning fyrirtækis með RapidStart Services</span><span class="sxs-lookup"><span data-stu-id="63813-162">Setting Up a Company With RapidStart Services</span></span>](admin-set-up-a-company-with-rapidstart.md)  
[<span data-ttu-id="63813-163">QuickBooks gagnaflutningur</span><span class="sxs-lookup"><span data-stu-id="63813-163">QuickBooks Data Migration</span></span>](ui-extensions-quickbooks-data-migration.md)  
[<span data-ttu-id="63813-164">Dynamics GP Gagnafærsla</span><span class="sxs-lookup"><span data-stu-id="63813-164">Dynamics GP Data Migration</span></span>](ui-extensions-dynamicsgp-data-migration.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
## [!INCLUDE[d365fin](includes/training_link_md.md)]

