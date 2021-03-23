---
title: Kynntu þér fjárhag og bókhaldslykla| Microsoft Docs
description: Lýsir fjárhag og bókhaldslyklar, sem og reikningsflokkum.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: analysis, history, track
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 29658ea0c7689ebdcb84384dfb26ec26089685c3
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5376813"
---
# <a name="understanding-the-general-ledger-and-the-coa"></a><span data-ttu-id="dc126-103">Skilja fjárhag og bókhaldslykil</span><span class="sxs-lookup"><span data-stu-id="dc126-103">Understanding the General Ledger and the COA</span></span>

<span data-ttu-id="dc126-104">Fjárhagur geymir fjárhagsgögn,  og bókhaldslykill birtir reikningana sem allar fjárhagsfærslur eru bókaðar í.</span><span class="sxs-lookup"><span data-stu-id="dc126-104">The general ledger stores your financial data, and the chart of accounts shows the accounts that all general ledger entries are posted to.</span></span> [!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="dc126-105">inniheldur staðlaðan bókhaldslykil sem er tilbúin til að styðja þitt fyrirtæki.</span><span class="sxs-lookup"><span data-stu-id="dc126-105">includes a standard chart of accounts that is ready to support your business.</span></span>

## <a name="general-ledger-setup-and-general-posting-setup"></a><span data-ttu-id="dc126-106">Uppsetning Uppsetning fjárhags og uppsetning almenns bókunargrunnur</span><span class="sxs-lookup"><span data-stu-id="dc126-106">General Ledger Setup and General Posting Setup</span></span>

<span data-ttu-id="dc126-107">Uppsetning aðalbókarinnar er kjarninn í fjárhagslegum ferlum vegna þess að það skilgreinir hvernig þú sendir gögn.</span><span class="sxs-lookup"><span data-stu-id="dc126-107">The setup of the general ledger is at the core of financial processes because it defines how you post data.</span></span>  

<span data-ttu-id="dc126-108">Á síðunni **Uppsetning aðalbókarinnar** tilgreinir þú hvernig á að meðhöndla tiltekin reikningsskilaboð í fyrirtækinu þínu, svo sem:</span><span class="sxs-lookup"><span data-stu-id="dc126-108">On the **General Ledger Setup** page, you specify how to handle certain accounting issues in your company, such as:</span></span>  

* <span data-ttu-id="dc126-109">Sléttunarnákvæmni reikninga</span><span class="sxs-lookup"><span data-stu-id="dc126-109">Invoice rounding details</span></span>  
* <span data-ttu-id="dc126-110">Snið aðseturs</span><span class="sxs-lookup"><span data-stu-id="dc126-110">Address formats</span></span>  
* <span data-ttu-id="dc126-111">Fjárhagsskýrslugerð</span><span class="sxs-lookup"><span data-stu-id="dc126-111">Financial reporting</span></span>  

<span data-ttu-id="dc126-112">Á sama hátt er á síðunni **Almennur bókunargrunnur** tilgreint hvernig á að setja upp samsetningar almennra viðskiptabókunarflokka og almenna vörubókunarflokka.</span><span class="sxs-lookup"><span data-stu-id="dc126-112">Similarly, on the **General Posting Setup** page, you specify how you want to set up combinations of general business and general product posting groups.</span></span> <span data-ttu-id="dc126-113">Staða hópar korta aðila eins og viðskiptavini, seljendur, atriði, auðlindir og sölu- og kaupskjöl til almennra reikninga.</span><span class="sxs-lookup"><span data-stu-id="dc126-113">Posting groups map entities like customers, vendors, items, resources, and sales and purchase documents to general ledger accounts.</span></span> <span data-ttu-id="dc126-114">Ein lína er fyllt út fyrir hverja samsetningu viðskiptabókunarflokks og vörubókunarflokks.</span><span class="sxs-lookup"><span data-stu-id="dc126-114">You fill in a line for each combination of business posting group and product posting group.</span></span> <span data-ttu-id="dc126-115">Nánari upplýsingar eru í [Uppsetning bókunarflokka](finance-posting-groups.md).</span><span class="sxs-lookup"><span data-stu-id="dc126-115">For more information, see [Posting Group Setups](finance-posting-groups.md).</span></span>  

> [!TIP]
> <span data-ttu-id="dc126-116">Síðan **Fjárhagsgrunnur** innheldur almenn svæði og svæði sem eiga sérstaklega við um heimaland þitt eða svæði.</span><span class="sxs-lookup"><span data-stu-id="dc126-116">The **General Ledger Setup** page includes generic fields and fields that are particular to your country or region.</span></span> <span data-ttu-id="dc126-117">Ef þú ert ekki viss um merkingu reits mælum við með því að þú hafir samband við endurskoðandann þinn til að ákvarða hvort hann skiptir máli fyrir fyrirtækið þitt.</span><span class="sxs-lookup"><span data-stu-id="dc126-117">If you are not sure of the meaning of a field, we suggest you work with your accountant to determine whether it is of relevance to your organization.</span></span>  

## <a name="the-chart-of-accounts"></a><span data-ttu-id="dc126-118">Bókhaldslykillinn</span><span class="sxs-lookup"><span data-stu-id="dc126-118">The Chart of Accounts</span></span>

<span data-ttu-id="dc126-119">Skýringin á reikningum sýnir allar almennar bókhaldsreikningar.</span><span class="sxs-lookup"><span data-stu-id="dc126-119">The chart of accounts shows all general ledger accounts.</span></span> <span data-ttu-id="dc126-120">Úr bókhaldslyklinum geturðu gert hluti eins og:</span><span class="sxs-lookup"><span data-stu-id="dc126-120">From the chart of accounts, you can do things like:</span></span>  

* <span data-ttu-id="dc126-121">Skoða skýrslur sem sýna aðalbókaratriði og jafnvægi.</span><span class="sxs-lookup"><span data-stu-id="dc126-121">View reports that show general ledger entries and balances.</span></span>  
* <span data-ttu-id="dc126-122">Lokaðu rekstrarreikningi þínum.</span><span class="sxs-lookup"><span data-stu-id="dc126-122">Close your income statement.</span></span>  
* <span data-ttu-id="dc126-123">Opnið fjárhagsreikningskortið til að bæta við eða breyta stillingum.</span><span class="sxs-lookup"><span data-stu-id="dc126-123">Open the G/L account card to add or change settings.</span></span>  
* <span data-ttu-id="dc126-124">Sjá lista yfir pósthópa sem senda á þann reikning.</span><span class="sxs-lookup"><span data-stu-id="dc126-124">See a list of posting groups that post to that account.</span></span>
* <span data-ttu-id="dc126-125">Skoða debet- og kreditstöður fyrir einstakan fjárhagsreikning</span><span class="sxs-lookup"><span data-stu-id="dc126-125">View separate debit and credit balances for a single account</span></span>  

<span data-ttu-id="dc126-126">Þú getur bætt við, breytt eða eytt almennum bókhaldsreikningum.</span><span class="sxs-lookup"><span data-stu-id="dc126-126">You can add, change, or delete general ledger accounts.</span></span> <span data-ttu-id="dc126-127">Til að koma í veg fyrir misræmi geturðu þó ekki eytt almennri aðalbókareikning ef gögnin eru notuð í töflureikningi.</span><span class="sxs-lookup"><span data-stu-id="dc126-127">However, to prevent discrepancies, you can't delete a general ledger account if it's data is used in the chart of accounts.</span></span>  

## <a name="account-categories"></a><span data-ttu-id="dc126-128">tegundir reikninga</span><span class="sxs-lookup"><span data-stu-id="dc126-128">Account Categories</span></span>

<span data-ttu-id="dc126-129">Þú getur sérsniðið uppbyggingu reikningsskila þinnar með því að kortleggja aðalbókarreikninga í reikningsflokkum.</span><span class="sxs-lookup"><span data-stu-id="dc126-129">You can personalize the structure of your financial statements by mapping general ledger accounts to account categories.</span></span>  

<span data-ttu-id="dc126-130">Síðan **Fjárhagsreikningsflokkar** sýnir flokka og undirflokka og fjárhagsreikninga sem eru úthlutað þeim.</span><span class="sxs-lookup"><span data-stu-id="dc126-130">The **G/L Account Categories** page shows your categories and subcategories, and the G/L accounts that are assigned to them.</span></span> <span data-ttu-id="dc126-131">Hægt er að stofna nýja undirflokka og úthluta þeim á fyrirliggjandi reikninga.</span><span class="sxs-lookup"><span data-stu-id="dc126-131">You can create new subcategories and assign those categories to existing accounts.</span></span>  

<span data-ttu-id="dc126-132">Þú stofnar tegundaflokk með því að draga inn aðra undirflokka undir línu á síðunni **flokkar fjárhagsreikninga**.</span><span class="sxs-lookup"><span data-stu-id="dc126-132">You create a category group by indenting other subcategories under a line on the **G/L Account Categories** page.</span></span> <span data-ttu-id="dc126-133">Það gerir það auðveldara fyrir þig að fá yfirlit, því hver flokkur sýnir heildarstöðu.</span><span class="sxs-lookup"><span data-stu-id="dc126-133">This makes it easy for you to get an overview, because each grouping shows a total balance.</span></span> <span data-ttu-id="dc126-134">Til dæmis er hægt að stofna undirflokka fyrir mismunandi tegundir eigna og síðan stofna tegundaflokka fyrir fastafjármunir miðað við veltufjármunir.</span><span class="sxs-lookup"><span data-stu-id="dc126-134">For example, you can create subcategories for different types of assets, and then create category groups for fixed assets versus current assets.</span></span>  

<span data-ttu-id="dc126-135">Þú getur tilgreint hvort reikningarnir í hverjum undirflokki skuli innifalinn í tilteknum tegundum skýrslna.</span><span class="sxs-lookup"><span data-stu-id="dc126-135">You can specify whether the accounts in each subcategory must be included in specific types of reports.</span></span> <span data-ttu-id="dc126-136">Þú getur notað lykiltegundir til hjálpa til við að skilgreina snið fjárhagsskýrslna.</span><span class="sxs-lookup"><span data-stu-id="dc126-136">The account categories help define the layout of your financial statements.</span></span>  

<span data-ttu-id="dc126-137">Til dæmis hin sjálfgefna stöðuyfirlit hefur undirflokk fyrir reiðufé í eignum.</span><span class="sxs-lookup"><span data-stu-id="dc126-137">For example, the default balance statement has a subcategory for Cash under Current Assets.</span></span> <span data-ttu-id="dc126-138">Ef þú vilt jafnvægisyfirlitið skaltu íhuga smápeninga og stöðva getur þú:</span><span class="sxs-lookup"><span data-stu-id="dc126-138">If you want the balance statement consider petty cash and checking, you can:</span></span>  

1. <span data-ttu-id="dc126-139">Bættu við tveimur nýjum undirflokkum.</span><span class="sxs-lookup"><span data-stu-id="dc126-139">Add two new subcategories.</span></span> <span data-ttu-id="dc126-140">Einn fyrir sjóð og einn fyrir reikninginn þinn.</span><span class="sxs-lookup"><span data-stu-id="dc126-140">One for petty cash, and one for your checking account.</span></span>  
2. <span data-ttu-id="dc126-141">Tilgreindu viðbótarskýrslugerðina **Reiðufé** fyrir þessar undirflokka.</span><span class="sxs-lookup"><span data-stu-id="dc126-141">Specify the additional report definition **Cash Accounts** for these subcategories.</span></span>  
3. <span data-ttu-id="dc126-142">Haltu þeim í undirflokknum **Handbært fé**.</span><span class="sxs-lookup"><span data-stu-id="dc126-142">Indent them under the **Cash** subcategory.</span></span>  

<span data-ttu-id="dc126-143">Í næsta skipti sem þú stofnar reikningaskipta birtist efnahagsreikningur þín í heildarjöfnuði fyrir peninga og tvær línur með jafnvægi fyrir smáskatta og eftirlitsreikning.</span><span class="sxs-lookup"><span data-stu-id="dc126-143">The next time you generate account schedules your balance statement will show a total balance for cash and two lines with balances for petty cash and the checking account.</span></span>  

## <a name="see-also"></a><span data-ttu-id="dc126-144">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="dc126-144">See Also</span></span>

[<span data-ttu-id="dc126-145">Fjármál</span><span class="sxs-lookup"><span data-stu-id="dc126-145">Finance</span></span>](finance.md)  
[<span data-ttu-id="dc126-146">Uppsetning eða breyting á bókhaldslykli</span><span class="sxs-lookup"><span data-stu-id="dc126-146">Setting Up or Changing the Chart of Accounts</span></span>](finance-setup-chart-accounts.md)  
[<span data-ttu-id="dc126-147">Viðskiptaupplýsingar</span><span class="sxs-lookup"><span data-stu-id="dc126-147">Business Intelligence</span></span>](bi.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]