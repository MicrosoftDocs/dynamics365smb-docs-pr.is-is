---
title: Afskráning eða innköllun eignar| Microsoft Docs
description: Nauðsynlegt er að bóka afskráningarvirði þegar þú rýrir, selur eða innkallar eignir.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: scrap
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 16d052c67a2d9b5513e9dac901dfeddce0527512
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/17/2020
ms.locfileid: "4749419"
---
# <a name="dispose-of-or-retire-fixed-assets"></a><span data-ttu-id="9bf95-103">Afskrá eða innkalla eignir</span><span class="sxs-lookup"><span data-stu-id="9bf95-103">Dispose of or Retire Fixed Assets</span></span>

<span data-ttu-id="9bf95-104">Þegar eign er seld eða afskráð með öðrum hætti verður að bóka afskráningarverðmæti hennar til að reikna út og skrá hagnað eða tap.</span><span class="sxs-lookup"><span data-stu-id="9bf95-104">When you sell or otherwise dispose of a fixed asset, the disposal value must be posted to calculate and record the gain or loss.</span></span> <span data-ttu-id="9bf95-105">Afskráningarfærsla verður að vera síðasta færslan sem bókuð er vegna eignar.</span><span class="sxs-lookup"><span data-stu-id="9bf95-105">A disposal entry must be the last entry posted for a fixed asset.</span></span> <span data-ttu-id="9bf95-106">Vegna eigna sem eru að hluta afskráðar er hægt að bóka eina eða fleiri afskráningarfærslur.</span><span class="sxs-lookup"><span data-stu-id="9bf95-106">For partially disposed fixed assets, you can post more than one disposal entry.</span></span> <span data-ttu-id="9bf95-107">Samtala allra bókaðra afskráningarupphæða verður að vera kreditupphæð.</span><span class="sxs-lookup"><span data-stu-id="9bf95-107">The total of all posted disposal amounts must be a credit amount.</span></span>  

> [!NOTE]  
> <span data-ttu-id="9bf95-108">Ef ný eign kemur í stað annarrar verður að skrá bæði söluna á gömlu eigninni (afskráning) og innkaupin á þeirri nýju (kaup).</span><span class="sxs-lookup"><span data-stu-id="9bf95-108">If you trade-in a fixed asset for another one, you must record both the sale of the old asset (disposal) and the purchase of the new one (acquisition).</span></span> <span data-ttu-id="9bf95-109">Nánari upplýsingar eru í [Komast yfir eignir](fa-how-acquire.md).</span><span class="sxs-lookup"><span data-stu-id="9bf95-109">For more information, see [Acquire Fixed Assets](fa-how-acquire.md).</span></span>  

<span data-ttu-id="9bf95-110">Eftirfarandi skref gera ráð fyrir að þú hafir þegar sett upp viðkomandi bókunarflokka á síðu **Eignabókunarflokkana**.</span><span class="sxs-lookup"><span data-stu-id="9bf95-110">The following steps assume that you have already set up the relevant posting groups in the **FA Posting Groups** page.</span></span> <span data-ttu-id="9bf95-111">Frekari upplýsingar er að finna í [Að setja upp bókunarflokka eigna](fa-how-setup-general.md#to-set-up-fixed-asset-posting-groups).</span><span class="sxs-lookup"><span data-stu-id="9bf95-111">For more information, see [To set up fixed asset posting groups](fa-how-setup-general.md#to-set-up-fixed-asset-posting-groups).</span></span>  

## <a name="to-post-a-disposal-from-the-fixed-asset-gl-journal"></a><span data-ttu-id="9bf95-112">Bóka afskráningu úr fjárhagsbók eigna</span><span class="sxs-lookup"><span data-stu-id="9bf95-112">To post a disposal from the fixed asset G/L journal</span></span>

1. <span data-ttu-id="9bf95-113">Veldu táknið ![ljósapera sem opnar eiginleikann „Viðmótsleit“](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera"), sláið inn **Eignafjárhagsbók** og veljið síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="9bf95-113">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Fixed Asset G/L Journals**, and then choose the related link.</span></span>  
2. <span data-ttu-id="9bf95-114">Stofnaður er upprunaleg Færslubókarlína og reitirnir fylltir út eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="9bf95-114">Create an initial journal line and fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. <span data-ttu-id="9bf95-115">Í reitnum **Eignabókunartegund** er valinn **afskráning**.</span><span class="sxs-lookup"><span data-stu-id="9bf95-115">In the **FA Posting Type** field, select **Disposal**.</span></span>  
4. <span data-ttu-id="9bf95-116">Valið er **Setja inn mótreikn. eigna** aðgerð.</span><span class="sxs-lookup"><span data-stu-id="9bf95-116">Choose the **Insert FA Bal. Account** action.</span></span> <span data-ttu-id="9bf95-117">Seinni færslubókarlína er búin til fyrir mótreiknings sem er sett upp fyrir bókun afskráningar.</span><span class="sxs-lookup"><span data-stu-id="9bf95-117">A second journal line is created for the balancing account that is set up for disposal posting.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="9bf95-118">Skref 4 virkar eingöngu ef búið er að setja upp eftirfarandi: Í **Eignabókunarflokksspjald** síðunni fyrir bókunarflokkur eigna, inniheldur reiturinn **afskráningarreikningur** debetreikning fjárhags og reiturinn **Mótreikningur afskráningar** inniheldur fjárhagsreikninginn sem á að bóka mótfærslur í fyrir styrkingu.</span><span class="sxs-lookup"><span data-stu-id="9bf95-118">Step 4 only works if you have set up the following: On the **FA Posting Group Card** page for the posting group of the fixed asset, the **Disposal Account** field contains the general ledger debit account and the **Disposal Bal. Account** field contains the general ledger account to which you want to post balancing entries for appreciation.</span></span> <span data-ttu-id="9bf95-119">Frekari upplýsingar er að finna í [Að setja upp bókunarflokka eigna](fa-how-setup-general.md#to-set-up-fixed-asset-posting-groups).</span><span class="sxs-lookup"><span data-stu-id="9bf95-119">For more information, see [To set up fixed asset posting groups](fa-how-setup-general.md#to-set-up-fixed-asset-posting-groups).</span></span>  
5. <span data-ttu-id="9bf95-120">Valið er **Bóka** aðgerðin.</span><span class="sxs-lookup"><span data-stu-id="9bf95-120">Choose the **Post** action.</span></span>  

<span data-ttu-id="9bf95-121">Ef hluti eignar er seldur eða afskráður verður að skipta eigninni upp í hluta áður en hægt er að afskrá.</span><span class="sxs-lookup"><span data-stu-id="9bf95-121">If you sell or dispose of part of a fixed asset, you must split up the asset before you can record the disposal transaction.</span></span> <span data-ttu-id="9bf95-122">Nánari upplýsingar eru í [Skipta upp, eða sameina eignir](fa-how-trans-split-combine.md).</span><span class="sxs-lookup"><span data-stu-id="9bf95-122">For more information, see [Transfer, Split, or Combine Fixed Assets](fa-how-trans-split-combine.md).</span></span>  

## <a name="to-view-disposal-ledger-entries"></a><span data-ttu-id="9bf95-123">Skoðun afskráningarfærslna:</span><span class="sxs-lookup"><span data-stu-id="9bf95-123">To view disposal ledger entries</span></span>
<span data-ttu-id="9bf95-124">Þegar eign er seld eða afskráð með öðrum hætti er afskráningarverðmæti hennar bókað í fjárhags þar sem má sjá niðurstöðurnar.</span><span class="sxs-lookup"><span data-stu-id="9bf95-124">When you sell or dispose of a fixed asset, the disposal value is posted to the general ledger where you can view the result.</span></span>  

1. <span data-ttu-id="9bf95-125">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Eignir** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="9bf95-125">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Fixed Assets**, and then choose the related link.</span></span>  
2. <span data-ttu-id="9bf95-126">Valin er eignin sem á að skoða færslur fyrir og veldu síðan aðgerðina **afskriftabækur**.</span><span class="sxs-lookup"><span data-stu-id="9bf95-126">Select the fixed asset that you want to view entries for, and then choose the **Depreciation Books** action.</span></span>  
3. <span data-ttu-id="9bf95-127">Valin er afskriftabók sem á að skoða færslur fyrir og veldu síðan aðgerðina **fjárhagsfærslur**.</span><span class="sxs-lookup"><span data-stu-id="9bf95-127">Select the depreciation book that you want to view entries for, and then choose the **Ledger Entries** action.</span></span>  
4. <span data-ttu-id="9bf95-128">Veljið línu með **Afskráningu** í reitnum **Eignabókunarflokkur** og veljið síðan aðgerðina **Finna færslur**.</span><span class="sxs-lookup"><span data-stu-id="9bf95-128">Select a line with **Disposal** in the **FA Posting Category** field, and then choose the **Find Entries** action.</span></span>  
5. <span data-ttu-id="9bf95-129">Á síðunni **Finna færslur** skal velja línu fjárhagsfærslu og síðan velja aðgerðina **Sýna tengdar færslur**.</span><span class="sxs-lookup"><span data-stu-id="9bf95-129">On the **Find Entries** page, select the general ledger entry line, and then choose the **Show Related Entries** action.</span></span>  

<span data-ttu-id="9bf95-130">Síðan **Fjárhagsfærslur** opnast og sýnir færslurnar sem afskráningarfærslan hefur myndað.</span><span class="sxs-lookup"><span data-stu-id="9bf95-130">The **General Ledger Entries** page opens where you can see the entries that the disposal posting resulted in.</span></span>  

## <a name="see-also"></a><span data-ttu-id="9bf95-131">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="9bf95-131">See Also</span></span>

[<span data-ttu-id="9bf95-132">Eignir</span><span class="sxs-lookup"><span data-stu-id="9bf95-132">Fixed Assets</span></span>](fa-manage.md)  
[<span data-ttu-id="9bf95-133">Uppsetning eigna</span><span class="sxs-lookup"><span data-stu-id="9bf95-133">Setting Up Fixed Assets</span></span>](fa-setup.md)  
<span data-ttu-id="9bf95-134">[Setja upp bókunarflokka eigna](fa-how-setup-general.md#to-set-up-fixed-asset-posting-groups).</span><span class="sxs-lookup"><span data-stu-id="9bf95-134">[To set up fixed asset posting groups](fa-how-setup-general.md#to-set-up-fixed-asset-posting-groups).</span></span>  
[<span data-ttu-id="9bf95-135">Fjármál</span><span class="sxs-lookup"><span data-stu-id="9bf95-135">Finance</span></span>](finance.md)  
[<span data-ttu-id="9bf95-136">Hafist handa</span><span class="sxs-lookup"><span data-stu-id="9bf95-136">Getting Started</span></span>](product-get-started.md)  
<span data-ttu-id="9bf95-137">[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="9bf95-137">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="9bf95-138">Finna færslur</span><span class="sxs-lookup"><span data-stu-id="9bf95-138">Find Entries</span></span>](ui-find-entries.md)  
