---
title: Nota Excel til að flytja inn gögn í Business Central
description: Sjálfgefinn grunnstillingarpakki er notaður til að bæta við viðskiptamenn í Excel og flytja inn gögnin aftur í Business Central.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: migration, Excel
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 984186e8bb08cc9e99ab91dbc08f0e85c58e0804
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5777949"
---
# <a name="importing-business-data-from-other-finance-systems"></a><span data-ttu-id="0c99f-103">Innflutningur viðskiptagagna úr öðrum fjárhagskerfum</span><span class="sxs-lookup"><span data-stu-id="0c99f-103">Importing Business Data from Other Finance Systems</span></span>

<span data-ttu-id="0c99f-104">Þegar notandi skráir sig í [!INCLUDE[prod_short](includes/prod_short.md)], er hægt að ákveða að búa til autt fyrirtæki svo hægt sé að hlaða upp eigin gögnum og prófa áfram nýja [!INCLUDE[prod_short](includes/prod_short.md)] fyrirtækið.</span><span class="sxs-lookup"><span data-stu-id="0c99f-104">When you sign up for [!INCLUDE[prod_short](includes/prod_short.md)], you can choose to create an empty company so that you can upload your own data and to test your new [!INCLUDE[prod_short](includes/prod_short.md)] company.</span></span> <span data-ttu-id="0c99f-105">Það fer eftir því fjárhagskerfi sem fyrirtækið notar í dag hvernig og hvort hægt er að millifæra upplýsingar um viðskiptamenn, lánardrottna, birgðir og bankareikninga.</span><span class="sxs-lookup"><span data-stu-id="0c99f-105">Depending on the finance solution that your business uses today, you can transfer information about customers, vendors, inventory, and bank accounts.</span></span>  

<span data-ttu-id="0c99f-106">Hægt er að ræsa leiðarvísi um uppsetningu með hjálp frá Mitt hlutverk sem hjálpar til við að flytja viðskiptagögn úr Excel-skrá eða öðrum sniðum.</span><span class="sxs-lookup"><span data-stu-id="0c99f-106">From the Role Center, you can start an assisted setup guide that helps you transfer the business data from an Excel file or from other formats.</span></span> <span data-ttu-id="0c99f-107">Þær skráategundir sem hægt er að hlaða upp fer eftir viðbótunum sem í boði eru.</span><span class="sxs-lookup"><span data-stu-id="0c99f-107">The type of files you can upload depends on the extensions that are available.</span></span> <span data-ttu-id="0c99f-108">Til dæmis er hægt að yfirfæra gögn úr QuickBooks vegna þess að [!INCLUDE[prod_short](includes/prod_short.md)] felur í sér viðbót sem sér um umbreytingu úr QuickBooks.</span><span class="sxs-lookup"><span data-stu-id="0c99f-108">For example, you can migrate data from QuickBooks because [!INCLUDE[prod_short](includes/prod_short.md)] includes an extension that handles the conversion from QuickBooks.</span></span> <span data-ttu-id="0c99f-109">Ef notandi vill yfirfæra gögn úr öðrum fjárhagskerfum þarf annað hvort að athuga hvort viðbót er í boði fyrir það kerfi eða flytja gögnin inn úr Excel.</span><span class="sxs-lookup"><span data-stu-id="0c99f-109">If you want to migrate data from other finance solutions, you must either check if an extension is available for that solution or import from Excel.</span></span>  

[!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="0c99f-110">inniheldur sniðmát fyrir viðskiptamenn, lánardrottna og birgðavörur sem hægt er að nota þegar gögnum er hlaðið upp.</span><span class="sxs-lookup"><span data-stu-id="0c99f-110">includes templates for accounts, customers, vendors, and inventory items that you can choose to apply when you import your data.</span></span>

<span data-ttu-id="0c99f-111">Hægt er að flytja aðalgögn og sum færslugögn úr öðrum fjárhagskerfum á grundvelli sjálfgefins grunnstillingarpakka í [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="0c99f-111">You can import master data and some transactional data from other finance systems based on the default configuration package in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="0c99f-112">Á síðunni **Grunnstillingarpakkar** er hægt að vinna með pakka til að flytja inn og staðfesta gögnin áður en pakkinn er notaður.</span><span class="sxs-lookup"><span data-stu-id="0c99f-112">On the **Configuration Packages** page, you can work with the package to import and validate the data before you apply the package.</span></span>  

> [!TIP]  
> <span data-ttu-id="0c99f-113">Mælt er með því að nota leiðsagnarforrit fyrir gagnafærslu til að flytja inn gögn frá Dynamics GP, Dynamics NAV eða QuickBooks.</span><span class="sxs-lookup"><span data-stu-id="0c99f-113">We recommend that you use data migration wizards to import data from Dynamics GP, Dynamics NAV, or QuickBooks.</span></span> <span data-ttu-id="0c99f-114">Frekari upplýsingar er að finna í [Flytja inn innanhússgögn í Business Central Online](/dynamics365/business-central/dev-itpro/administration/migrate-data) í stjórnendaefninu eða [QuickBooks gagnaflutning](ui-extensions-quickbooks-data-migration.md).</span><span class="sxs-lookup"><span data-stu-id="0c99f-114">For more information, see [Migrating On-Premises Data to Business Central Online](/dynamics365/business-central/dev-itpro/administration/migrate-data) in the administration content, or [QuickBooks Data Migration](ui-extensions-quickbooks-data-migration.md).</span></span>

> [!NOTE]  
> <span data-ttu-id="0c99f-115">Fyrir stærri innleiðingarverk getur þú notað RapidStart Services fyrir [!INCLUDE[prod_short](includes/prod_short.md)], sem er víðtækt verkfærasafn til að setja upp nýjar lausnir sem byggjast á viðskiptakröfum viðskiptamanna og uppsetningargögnum.</span><span class="sxs-lookup"><span data-stu-id="0c99f-115">For larger implementation work, you can use RapidStart Services for [!INCLUDE[prod_short](includes/prod_short.md)], which is an extensive toolkit for setting up new solutions based on customers' business requirements and setup data.</span></span> <span data-ttu-id="0c99f-116">RapidStart Services býður einnig upp á virkni til að flytja inn viðskiptagögn.</span><span class="sxs-lookup"><span data-stu-id="0c99f-116">RapidStart Services also offers functionality for import of business data.</span></span> <span data-ttu-id="0c99f-117">Nánari upplýsingar er að finna í [Uppsetning fyrirtækis með RapidStart Services](admin-set-up-a-company-with-rapidstart.md).</span><span class="sxs-lookup"><span data-stu-id="0c99f-117">For more information, see [Setting Up a Company With RapidStart Services](admin-set-up-a-company-with-rapidstart.md).</span></span>

<span data-ttu-id="0c99f-118">Til að flytja inn myndir af vörum er hægt að nota þar til gerða aðgerð á síðunni **Uppsetning birgða**.</span><span class="sxs-lookup"><span data-stu-id="0c99f-118">To import item pictures, you can use a dedicated function on the **Inventory Setup** page.</span></span> <span data-ttu-id="0c99f-119">Frekari upplýsingar er að finna í [Flytja inn margar vörumyndir](inventory-how-import-item-pictures.md).</span><span class="sxs-lookup"><span data-stu-id="0c99f-119">For more information, see [Import Multiple Item Pictures](inventory-how-import-item-pictures.md).</span></span>

## <a name="importing-data-from-configuration-packages"></a><span data-ttu-id="0c99f-120">Innflutningur gagna úr grunnstillingarpakka</span><span class="sxs-lookup"><span data-stu-id="0c99f-120">Importing Data from Configuration Packages</span></span>
[!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="0c99f-121">inniheldur stillingarpakka sem þú getur flutt út í Excel og sett upp gögnin þín þar.</span><span class="sxs-lookup"><span data-stu-id="0c99f-121">includes a configuration package that you can export to Excel and set up your data there.</span></span> <span data-ttu-id="0c99f-122">Síðan er hægt að flytja aftur inn gögnin úr Excel.</span><span class="sxs-lookup"><span data-stu-id="0c99f-122">Then, you can import the data from Excel again.</span></span> <span data-ttu-id="0c99f-123">Pakkinn samanstendur af 27 töflum, þar með talið aðalgögnum, svo sem viðskiptavinum, söluaðilum, hlutum og reikningum, öðrum grunnuppsetningartöflum eins og sendingarkostnaði og viðskiptatöflum eins og söluhaus og línum.</span><span class="sxs-lookup"><span data-stu-id="0c99f-123">The package consists of 27 tables, including master data such as customers, vendors, items, and accounts, other basic setup tables such as shipping methods, and transactions tables such as sales header and lines.</span></span>  

> [!NOTE]  
>   <span data-ttu-id="0c99f-124">Vinna með stillingarpakka er ítarleg virkni og við mælum með að þú hafir samband við kerfisstjórann þinn.</span><span class="sxs-lookup"><span data-stu-id="0c99f-124">Working with configuration packages is advanced functionality, and we recommend that you contact your administrator.</span></span> <span data-ttu-id="0c99f-125">Nánari upplýsingar eru í [Gögn flutt inn úr eldri bókhaldshugbúnaði með því að nota grunnstillingarpakka](across-import-data-configuration-packages.md).</span><span class="sxs-lookup"><span data-stu-id="0c99f-125">For more information, see [Importing Data from Legacy Accounting Software using a Configuration Package](across-import-data-configuration-packages.md).</span></span>

## <a name="working-with-data-in-excel"></a><span data-ttu-id="0c99f-126">Unnið með gögn í Excel</span><span class="sxs-lookup"><span data-stu-id="0c99f-126">Working with Data in Excel</span></span>
<span data-ttu-id="0c99f-127">Þegar sjálfgefinn grunnstillingarpakki er fluttur út í Excel inniheldur vinnubókin sem búin er til vinnublað fyrir hverja töflu í pakkanum.</span><span class="sxs-lookup"><span data-stu-id="0c99f-127">When you export the default configuration package to Excel, the generated workbook contains a worksheet for each table in the package.</span></span> <span data-ttu-id="0c99f-128">Til að einfalda verk er hægt að nýta XML-meðhöndlunarverkfærin sem byggð eru inn í Excel.</span><span class="sxs-lookup"><span data-stu-id="0c99f-128">To simplify your tasks, you can take advantage of the XML manipulation tools that are built into Excel.</span></span> <span data-ttu-id="0c99f-129">Einnig er hægt að nota Excel innbyggðar aðgerðir til aðstoða við gagnsnið og að setja gögn í réttan flokk.</span><span class="sxs-lookup"><span data-stu-id="0c99f-129">You can also use Excel built-in functions to help with data formatting and to put data in the correct cell.</span></span> <span data-ttu-id="0c99f-130">Til dæmis, bætið við auðu vinnublaði og afritið eldri gögnin á það.</span><span class="sxs-lookup"><span data-stu-id="0c99f-130">For example, add a blank worksheet and copy the legacy data to it.</span></span> <span data-ttu-id="0c99f-131">Búið því næst til Excel-formúlu til að varpa gögnum í umbreytingarvinnublaðinu á milli reitanna í útflutta vinnublaðinu og eldri gögnum viðskiptamanns.</span><span class="sxs-lookup"><span data-stu-id="0c99f-131">Then make an Excel formula to map data in the transformation worksheet between the fields in the exported worksheet and customer legacy data.</span></span> <span data-ttu-id="0c99f-132">Þegar búið er að varpa öllum gögnum, skal afrita afmörkun gagnanna á töflu á vinnublaðinu.</span><span class="sxs-lookup"><span data-stu-id="0c99f-132">After you have mapped all of the data, copy the range of data onto the table worksheet.</span></span>  

> [!IMPORTANT]  
>  <span data-ttu-id="0c99f-133">Ekki breyta dálkum í vinnublöðunum.</span><span class="sxs-lookup"><span data-stu-id="0c99f-133">Do not change the columns in the worksheets.</span></span> <span data-ttu-id="0c99f-134">Ef gögnin eru færð, þeim breytt eða þeim eytt er ekki hægt að flytja vinnublaðið inn í [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="0c99f-134">If they are moved, changed, or deleted, the worksheet cannot be imported into [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>

> [!NOTE]
> <span data-ttu-id="0c99f-135">Ekki er hægt að flytja út/flytja inn svæði af gerðinni Blob með Excel.</span><span class="sxs-lookup"><span data-stu-id="0c99f-135">Fields of type Blob cannot be exported/imported using Excel.</span></span>

## <a name="tables-in-the-default-configuration-package"></a><span data-ttu-id="0c99f-136">Töflur í sjálfgefnum grunnstillingarpakka</span><span class="sxs-lookup"><span data-stu-id="0c99f-136">Tables in the Default Configuration Package</span></span>
<span data-ttu-id="0c99f-137">Sjálfgefni grunnstillingarpakkinn styður eftirfarandi töflur:</span><span class="sxs-lookup"><span data-stu-id="0c99f-137">The default configuration package supports the following tables:</span></span>

-   <span data-ttu-id="0c99f-138">Greiðsluskilmálar</span><span class="sxs-lookup"><span data-stu-id="0c99f-138">Payment Terms</span></span>
-   <span data-ttu-id="0c99f-139">Verðflokkur viðskiptamanna</span><span class="sxs-lookup"><span data-stu-id="0c99f-139">Customer Price Group</span></span>
-   <span data-ttu-id="0c99f-140">Afhendingarmáti</span><span class="sxs-lookup"><span data-stu-id="0c99f-140">Shipment Method</span></span>
-   <span data-ttu-id="0c99f-141">Sölumaður/innkaupaaðili</span><span class="sxs-lookup"><span data-stu-id="0c99f-141">Salesperson/Purchaser</span></span>
-   <span data-ttu-id="0c99f-142">Birgðageymsla</span><span class="sxs-lookup"><span data-stu-id="0c99f-142">Location</span></span>
-   <span data-ttu-id="0c99f-143">Fjárhagsreikningur</span><span class="sxs-lookup"><span data-stu-id="0c99f-143">GL Account</span></span>
-   <span data-ttu-id="0c99f-144">Viðskiptavinur</span><span class="sxs-lookup"><span data-stu-id="0c99f-144">Customer</span></span>
-   <span data-ttu-id="0c99f-145">Lánardrottinn</span><span class="sxs-lookup"><span data-stu-id="0c99f-145">Vendor</span></span>
-   <span data-ttu-id="0c99f-146">Atriði</span><span class="sxs-lookup"><span data-stu-id="0c99f-146">Item</span></span>
-   <span data-ttu-id="0c99f-147">Söluhaus</span><span class="sxs-lookup"><span data-stu-id="0c99f-147">Sales Header</span></span>
-   <span data-ttu-id="0c99f-148">Sölulína</span><span class="sxs-lookup"><span data-stu-id="0c99f-148">Sales Line</span></span>
-   <span data-ttu-id="0c99f-149">Innkaupahaus</span><span class="sxs-lookup"><span data-stu-id="0c99f-149">Purchase Header</span></span>
-   <span data-ttu-id="0c99f-150">Innkaupalína</span><span class="sxs-lookup"><span data-stu-id="0c99f-150">Purchase Line</span></span>
-   <span data-ttu-id="0c99f-151">Almenn</span><span class="sxs-lookup"><span data-stu-id="0c99f-151">Gen.</span></span> <span data-ttu-id="0c99f-152">Færslubókarlína</span><span class="sxs-lookup"><span data-stu-id="0c99f-152">Journal Line</span></span>
-   <span data-ttu-id="0c99f-153">Birgðabókarlína</span><span class="sxs-lookup"><span data-stu-id="0c99f-153">Item Journal Line</span></span>
-   <span data-ttu-id="0c99f-154">Bókunarflokkur viðskm.</span><span class="sxs-lookup"><span data-stu-id="0c99f-154">Customer Posting Group</span></span>
-   <span data-ttu-id="0c99f-155">Bókunarflokkur lánardr.</span><span class="sxs-lookup"><span data-stu-id="0c99f-155">Vendor Posting Group</span></span>
-   <span data-ttu-id="0c99f-156">Birgðabókunarflokkur</span><span class="sxs-lookup"><span data-stu-id="0c99f-156">Inventory Posting Group</span></span>
-   <span data-ttu-id="0c99f-157">Mælieining</span><span class="sxs-lookup"><span data-stu-id="0c99f-157">Unit of Measure</span></span>
-   <span data-ttu-id="0c99f-158">Almenn</span><span class="sxs-lookup"><span data-stu-id="0c99f-158">Gen.</span></span> <span data-ttu-id="0c99f-159">Viðskiptabókunarflokkur</span><span class="sxs-lookup"><span data-stu-id="0c99f-159">Business Posting Group</span></span>
-   <span data-ttu-id="0c99f-160">Almenn</span><span class="sxs-lookup"><span data-stu-id="0c99f-160">Gen.</span></span> <span data-ttu-id="0c99f-161">Afurðarbókunarflokkur</span><span class="sxs-lookup"><span data-stu-id="0c99f-161">Product Posting Group</span></span>
-   <span data-ttu-id="0c99f-162">Almennur bókunargrunnur</span><span class="sxs-lookup"><span data-stu-id="0c99f-162">General Posting Setup</span></span>
-   <span data-ttu-id="0c99f-163">Umsjónarsvæði</span><span class="sxs-lookup"><span data-stu-id="0c99f-163">Territory</span></span>
-   <span data-ttu-id="0c99f-164">Vöruflokkur</span><span class="sxs-lookup"><span data-stu-id="0c99f-164">Item Category</span></span>
-   <span data-ttu-id="0c99f-165">Söluverð</span><span class="sxs-lookup"><span data-stu-id="0c99f-165">Sales Price</span></span>
-   <span data-ttu-id="0c99f-166">Innkaupsverð</span><span class="sxs-lookup"><span data-stu-id="0c99f-166">Purchase Price</span></span>

## <a name="see-also"></a><span data-ttu-id="0c99f-167">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="0c99f-167">See Also</span></span>
[<span data-ttu-id="0c99f-168">Uppsetning fyrirtækis með RapidStart Services</span><span class="sxs-lookup"><span data-stu-id="0c99f-168">Setting Up a Company With RapidStart Services</span></span>](admin-set-up-a-company-with-rapidstart.md)  
[<span data-ttu-id="0c99f-169">Flytja inn innanhússgögn í Business Central Online</span><span class="sxs-lookup"><span data-stu-id="0c99f-169">Migrating On-Premises Data to Business Central Online</span></span>](/dynamics365/business-central/dev-itpro/administration/migrate-data)  
[<span data-ttu-id="0c99f-170">QuickBooks gagnaflutningur</span><span class="sxs-lookup"><span data-stu-id="0c99f-170">QuickBooks Data Migration</span></span>](ui-extensions-quickbooks-data-migration.md)  
[<span data-ttu-id="0c99f-171">Flytja inn margar vörumyndir</span><span class="sxs-lookup"><span data-stu-id="0c99f-171">Import Multiple Item Pictures</span></span>](inventory-how-import-item-pictures.md)

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]