---
title: Setja upp kóða fyrir endurskoðunarslóðir | Microsoft-skjöl
description: Kynntu þér verkin til að setja upp upprunakóða og ástæðukóða sem þú getur notað til að fylgjast með eftirlitsferðum.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accounting, auditing, bookkeeping
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: e39de1d4656b272c5c6cf5c01f54d5d6ebeca05b
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/01/2020
ms.locfileid: "3914215"
---
# <a name="setting-up-source-codes-and-reason-codes-for-audit-trails"></a><span data-ttu-id="9acd1-103">Uppsetning upprunakóða og ástæðukóða fyrir endurskoðunarslóðir</span><span class="sxs-lookup"><span data-stu-id="9acd1-103">Setting Up Source Codes and Reason Codes for Audit Trails</span></span>

<span data-ttu-id="9acd1-104">Öllum bókuðum færslum er sjálfvirkt úthlutað upprunakóða þannig að hægt er að rekja færslur til uppruna þeirra.</span><span class="sxs-lookup"><span data-stu-id="9acd1-104">All posted entries are automatically assigned a source code so that transactions can be traced to their origin.</span></span> <span data-ttu-id="9acd1-105">Ef gefa á færslum upprunakóða til viðbótar má nota ástæðukóða.</span><span class="sxs-lookup"><span data-stu-id="9acd1-105">If you want to give entries a supplementary source code, you can use reason codes.</span></span> <span data-ttu-id="9acd1-106">Ástæðukóðar gefa til kynna hvar færsla var stofnuð.</span><span class="sxs-lookup"><span data-stu-id="9acd1-106">Reason codes are used to indicate why an entry was created.</span></span> <span data-ttu-id="9acd1-107">Þegar ástæðukóðar eru settir upp má úthluta þeim til heilla bókarsniðmáta og bókarkeyrslna, og hægt er að úthluta þeim til einstakra bókarlína og skjala.</span><span class="sxs-lookup"><span data-stu-id="9acd1-107">When you set up reason codes, you can assign them to entire journal templates and journal batches, and you can assign them to individual journal lines and documents.</span></span>  

<span data-ttu-id="9acd1-108">Nota skal kóða sem auðvelt er að muna og eru lýsandi.</span><span class="sxs-lookup"><span data-stu-id="9acd1-108">For both source codes and reason codes, use codes that are easy to remember and descriptive.</span></span> <span data-ttu-id="9acd1-109">Hægt er að setja upp ótakmarkaðan fjölda kóða.</span><span class="sxs-lookup"><span data-stu-id="9acd1-109">The code must be unique, and you can set up as many codes as you like.</span></span>

## <a name="define-source-codes"></a><span data-ttu-id="9acd1-110">Skilgreina upprunakóða</span><span class="sxs-lookup"><span data-stu-id="9acd1-110">Define source codes</span></span>

<span data-ttu-id="9acd1-111">Stundum þarf að skoða hvernig ákveðin færsla varð til, t.d. hvort hún varð til við bókun færslubókar eða innkaupareiknings.</span><span class="sxs-lookup"><span data-stu-id="9acd1-111">Sometimes, you want see how a particular entry arose, such as whether it came from posting a general journal or a purchase invoice.</span></span> <span data-ttu-id="9acd1-112">Upprunakóði gefur til kynna hvar færsla var stofnuð.</span><span class="sxs-lookup"><span data-stu-id="9acd1-112">A source code indicates where an entry was created.</span></span> <span data-ttu-id="9acd1-113">Færslur eru stofnaðar þegar færslubækur og reikningar eru bókuð og við tilteknar keyrslur.</span><span class="sxs-lookup"><span data-stu-id="9acd1-113">Entries are created when journals and invoices are posted and when certain batch jobs are executed.</span></span> <span data-ttu-id="9acd1-114">Hver bókunargerð er með tiltekinn upprunakóða sem er úthlutað þegar einstakar færslur eru stofnaðar.</span><span class="sxs-lookup"><span data-stu-id="9acd1-114">Each posting type has a specific source code that is assigned when individual entries are created.</span></span>  

<span data-ttu-id="9acd1-115">Við bókun færslubóka, pantana, reikninga og kreditreikninga og notkun ýmissa keyrslna eru stofnaðar færslur á ársreikningum.</span><span class="sxs-lookup"><span data-stu-id="9acd1-115">Posting journals, orders, invoices, or credit memos, and running various batch jobs, creates entries in the financial statements.</span></span> <span data-ttu-id="9acd1-116">Nokkrir flýtiflipar eru í glugganum **Uppsetn. upprunakóða** , einn fyrir hvern kerfishluta.</span><span class="sxs-lookup"><span data-stu-id="9acd1-116">The **Source Code Setup** page contains several FastTabs, one for each application area.</span></span> <span data-ttu-id="9acd1-117">Hver flýtiflipi hefur upprunakóðana sem eiga við þann kerfishluta.</span><span class="sxs-lookup"><span data-stu-id="9acd1-117">Each FastTab contains the source codes that are applicable for that application area.</span></span>

<span data-ttu-id="9acd1-118">Við bókun eða keyrslu er réttur upprunakóði sjálfkrafa hengdur við færsluna.</span><span class="sxs-lookup"><span data-stu-id="9acd1-118">When you post or run a batch job, the correct source code is automatically attached to the entry.</span></span> <span data-ttu-id="9acd1-119">Til dæmis, við bókun úr færslubók er færslan kóðuð sem *FÆRSLUBK* .</span><span class="sxs-lookup"><span data-stu-id="9acd1-119">For example, when you post from the general journal, the entry is coded as *GENJNL* .</span></span> <span data-ttu-id="9acd1-120">Síðan er hægt að sía síðuna **fjárhagsfærslur** til að sýna hvaða færslur voru bókaðar úr almennu færslubókinni eða úr söluskjölum, til dæmis</span><span class="sxs-lookup"><span data-stu-id="9acd1-120">You can then filter the **General Ledger Entries** page to show which entries were posted from the general journal or from sales documents, for example</span></span>

### <a name="to-define-source-codes"></a><span data-ttu-id="9acd1-121">Upprunakóðar skilgreindir:</span><span class="sxs-lookup"><span data-stu-id="9acd1-121">To define source codes</span></span>

1. <span data-ttu-id="9acd1-122">Veldu ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu tákn") táknið, sláðu inn **Uppsetning upprunakóða** og veldu svo tengdan tengil.</span><span class="sxs-lookup"><span data-stu-id="9acd1-122">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Source Code Setup** , and then choose the related link.</span></span>  

2. <span data-ttu-id="9acd1-123">Í glugganum **Uppsetning upprunakóða** skal tilgreina viðeigandi upprunakóða fyrir hverja bókunargerð og runuvinnslu.</span><span class="sxs-lookup"><span data-stu-id="9acd1-123">In the **Source Code Setup** window, for each each posting type and batch job, specify the relevant source code.</span></span>  

<span data-ttu-id="9acd1-124">Hægt er að breyta innihaldi reits síðar og breytingin mun hafa áhrif á væntanlegar bókanir í framtíðinni.</span><span class="sxs-lookup"><span data-stu-id="9acd1-124">You can change the contents of a field later, and that change will then impact future postings.</span></span>

## <a name="change-source-codes"></a><span data-ttu-id="9acd1-125">Breyta upprunakóðum</span><span class="sxs-lookup"><span data-stu-id="9acd1-125">Change source codes</span></span>

<span data-ttu-id="9acd1-126">Hugsanlega þarf að breyta upprunakóða.</span><span class="sxs-lookup"><span data-stu-id="9acd1-126">You may want to change a source code.</span></span> <span data-ttu-id="9acd1-127">Til dæmis ef notandi vill breyta upprunakóða *FHFBOK* í *FBK* .</span><span class="sxs-lookup"><span data-stu-id="9acd1-127">For example, you want to change the source code *GENJNL* to *GNJ* .</span></span>

### <a name="to-change-source-codes"></a><span data-ttu-id="9acd1-128">Upprunakóðum breytt:</span><span class="sxs-lookup"><span data-stu-id="9acd1-128">To change source codes</span></span>

1. <span data-ttu-id="9acd1-129">Veldu ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu tákn") tákn, sláðu inn **Upprunakóðar** og veldu svo tengdan tengil.</span><span class="sxs-lookup"><span data-stu-id="9acd1-129">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Source Codes** , and then choose the related link.</span></span>

2. <span data-ttu-id="9acd1-130">Kóðinn í reitnum **Kóði** er valinn í línunni með kóðanum sem á að breyta.</span><span class="sxs-lookup"><span data-stu-id="9acd1-130">On the line with the code to be changed, select the code in the **Code** field.</span></span>

3. <span data-ttu-id="9acd1-131">Færa inn nýja kóðann velja síðann hnappinn **Já** .</span><span class="sxs-lookup"><span data-stu-id="9acd1-131">Enter the new code, and then choose the **Yes** button.</span></span> <span data-ttu-id="9acd1-132">Einnig er hægt að breyta efni reitsins **Lýsing** .</span><span class="sxs-lookup"><span data-stu-id="9acd1-132">You can also change the contents of the **Description** field.</span></span>

<span data-ttu-id="9acd1-133">Allar færslur sem á eftir koma og bókaðar eru í færslubók verða með nýja upprunakóðann.</span><span class="sxs-lookup"><span data-stu-id="9acd1-133">All new entries that are posted from the general journal will have the new source code.</span></span>

## <a name="define-reason-codes"></a><span data-ttu-id="9acd1-134">Skilgreina ástæðukóða</span><span class="sxs-lookup"><span data-stu-id="9acd1-134">Define reason codes</span></span>

<span data-ttu-id="9acd1-135">Ástæðukóðar gefa til kynna hvar færsla var stofnuð.</span><span class="sxs-lookup"><span data-stu-id="9acd1-135">Reason codes supplement the source codes and are used to indicate why an entry was created.</span></span> <span data-ttu-id="9acd1-136">Þú getur úthlutað ástæðukóðum í stökum færslum og þú getur úthlutað endanlegum kóðum í tiltekin færslubókarsniðmát og -bókarkeyrslur.</span><span class="sxs-lookup"><span data-stu-id="9acd1-136">You can assign reason codes on individual entries, and you can assign permanent codes to specific journal templates and journal batches.</span></span> <span data-ttu-id="9acd1-137">Þegar kóðar eru tengdir við færslubókarlínu eða sölu- eða innkaupahaus merkir kerfið allar færslur með ástæðukóðanum þegar það bókar þær.</span><span class="sxs-lookup"><span data-stu-id="9acd1-137">When a reason code is linked to a journal line or a sales or purchase header, all entries are marked with the reason code when they are posted.</span></span>  

### <a name="to-set-up-reason-codes"></a><span data-ttu-id="9acd1-138">Uppsetning ástæðukóða</span><span class="sxs-lookup"><span data-stu-id="9acd1-138">To set up reason codes</span></span>

1. <span data-ttu-id="9acd1-139">Veldu ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu tákn") tákn, sláðu inn **Ástæðukóðar** og veldu svo tengdan tengil.</span><span class="sxs-lookup"><span data-stu-id="9acd1-139">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon")  icon, enter **Reason Codes** , and then choose the related link.</span></span>

2. <span data-ttu-id="9acd1-140">Í glugganum **Ástæðukóðar** er skal færa fyrsta kóðann inn í reitinn **Kóði** .</span><span class="sxs-lookup"><span data-stu-id="9acd1-140">In the **Reason Codes** window, enter the first code in the **Code** field.</span></span> <span data-ttu-id="9acd1-141">Texti til útskýringar er færður í reitinn **Lýsing** .</span><span class="sxs-lookup"><span data-stu-id="9acd1-141">In the **Description** field, enter an explanatory text.</span></span>

<span data-ttu-id="9acd1-142">Þetta er endurtekið fyrir alla kóða sem á að nota.</span><span class="sxs-lookup"><span data-stu-id="9acd1-142">Repeat the procedure for each code you want to use.</span></span> <span data-ttu-id="9acd1-143">Hægt er að setja upp kóða að vild.</span><span class="sxs-lookup"><span data-stu-id="9acd1-143">You can set up any number of codes.</span></span>

<span data-ttu-id="9acd1-144">Eftirfarandi ferli sýnir hvernig á að bæta ástæðukóða við færslubókarsniðmát en svipuð skref eiga við um að bæta ástæðukóða við færslubókarlínu eða bókarkeyrslu.</span><span class="sxs-lookup"><span data-stu-id="9acd1-144">The following procedure describes how to add a reason code to a journal template, but similar steps apply to adding a reason code to a journal line or journal batch.</span></span>  

### <a name="to-assign-reason-codes-to-journal-templates"></a><span data-ttu-id="9acd1-145">Ástæðukóðum úthlutað á færslubókarkeyrslur:</span><span class="sxs-lookup"><span data-stu-id="9acd1-145">To assign reason codes to journal templates</span></span>

1. <span data-ttu-id="9acd1-146">Veldu ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu tákn") tákn, sláðu inn **Sniðmát færslubóka** og veldu svo tengdan tengil.</span><span class="sxs-lookup"><span data-stu-id="9acd1-146">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon")  icon, enter **General Journal Templates** , and then choose the related link.</span></span>

2. <span data-ttu-id="9acd1-147">Í línunni með valda færslubókarsniðmátinu, í reitnum **Ástæðukóði** , skal tilgreina viðeigandi kóða.</span><span class="sxs-lookup"><span data-stu-id="9acd1-147">On the line with the selected journal template, in the **Reason Code** field, specify the relevant code.</span></span>

3. <span data-ttu-id="9acd1-148">Færslubókarsniðmátinu er lokað.</span><span class="sxs-lookup"><span data-stu-id="9acd1-148">Close the journal template.</span></span>

<span data-ttu-id="9acd1-149">Ástæðukóðinn sem var valinn verður afritaður í nýju færslubókarkeyrsluna sem búin var til með viðkomandi sniðmáti.</span><span class="sxs-lookup"><span data-stu-id="9acd1-149">The selected reason code will be copied to new journal batches created under this journal template.</span></span> <span data-ttu-id="9acd1-150">Ástæðukóðum er úthlutað á færslubókarsniðmát í öðrum kerfishlutum á sama hátt.</span><span class="sxs-lookup"><span data-stu-id="9acd1-150">You assign reason codes to journal templates in the other application areas in the same way.</span></span>

### <a name="to-use-reason-codes-on-sales-and-purchase-documents"></a><span data-ttu-id="9acd1-151">Nota ástæðukóða á sölu- og innkaupaskjöl</span><span class="sxs-lookup"><span data-stu-id="9acd1-151">To use reason codes on sales and purchase documents</span></span>

1. <span data-ttu-id="9acd1-152">Viðeigandi sölu- eða innkaupaskjal er opnað.</span><span class="sxs-lookup"><span data-stu-id="9acd1-152">Open the relevant sales or purchase document.</span></span>

2. <span data-ttu-id="9acd1-153">Kóðinn er færður í reitinn **Ástæðukóði** í sölu- eða innkaupahaus.</span><span class="sxs-lookup"><span data-stu-id="9acd1-153">On the sales or purchase header, enter the code in the **Reason Code** field.</span></span>

<span data-ttu-id="9acd1-154">Þegar reikningurinn er bókaður afritast ástæðukóðinn í allar fjarhags-, viðskiptamanna- og lánardrottnafærslur.</span><span class="sxs-lookup"><span data-stu-id="9acd1-154">When the invoice is posted, the reason code is copied to each general ledger, customer, and vendor entry.</span></span> <span data-ttu-id="9acd1-155">Ekki er hægt að úthluta mismunandi ástæðukóðum í einstakar innkaupa- og sölulínur vegna þess að allar línur bókast sem ein færsla.</span><span class="sxs-lookup"><span data-stu-id="9acd1-155">You cannot assign different reason codes to the individual purchase and sales lines because all lines are posted as one entry.</span></span>

## <a name="see-related-training-at-microsoft-learn"></a><span data-ttu-id="9acd1-156">Sjá tengda þjálfun á [Microsoft Learn](/learn/paths/set-up-financial-management-dynamics-365-business-central/)</span><span class="sxs-lookup"><span data-stu-id="9acd1-156">See Related Training at [Microsoft Learn](/learn/paths/set-up-financial-management-dynamics-365-business-central/)</span></span>

## <a name="see-also"></a><span data-ttu-id="9acd1-157">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="9acd1-157">See Also</span></span>

[<span data-ttu-id="9acd1-158">Fjármál</span><span class="sxs-lookup"><span data-stu-id="9acd1-158">Finance</span></span>](finance.md)  
[<span data-ttu-id="9acd1-159">Afstemming bankareikninga</span><span class="sxs-lookup"><span data-stu-id="9acd1-159">Reconciling Bank Accounts</span></span>](bank-manage-bank-accounts.md)  
[<span data-ttu-id="9acd1-160">Unnið með víddir</span><span class="sxs-lookup"><span data-stu-id="9acd1-160">Working with Dimensions</span></span>](finance-dimensions.md)  
[<span data-ttu-id="9acd1-161">Innflutningur viðskiptagagna úr öðrum fjárhagskerfum</span><span class="sxs-lookup"><span data-stu-id="9acd1-161">Importing Business Data from Other Finance Systems</span></span>](across-import-data-configuration-packages.md)  
[<span data-ttu-id="9acd1-162">Greining á sjóðstreymi í fyrirtækinu þínu</span><span class="sxs-lookup"><span data-stu-id="9acd1-162">Analyzing Cash Flow in Your Company</span></span>](finance-analyze-cash-flow.md)  
<span data-ttu-id="9acd1-163">[Unnið með [!INCLUDE[prodshort](includes/prodshort.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="9acd1-163">[Working with [!INCLUDE[prodshort](includes/prodshort.md)]](ui-work-product.md)</span></span>  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
