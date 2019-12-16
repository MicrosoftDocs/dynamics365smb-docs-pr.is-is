---
title: Hvernig á að Reikna út áfyllingu hólfs | Microsoft Docs
description: Þegar birgðageymslan er sett upp þannig að hún noti beinan frágang og tínslu er forgangsröðun frágangssniðmátsins tekið með í reikninginn þegar verið er að ganga frá móttökum.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 7983969df7f07c82b83698442fedbf1bbd20d0f5
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/03/2019
ms.locfileid: "2881823"
---
# <a name="calculate-bin-replenishment"></a><span data-ttu-id="649da-103">Reikna út áfyllingu hólfs</span><span class="sxs-lookup"><span data-stu-id="649da-103">Calculate Bin Replenishment</span></span>
<span data-ttu-id="649da-104">Þegar birgðageymslan er sett upp þannig að hún noti beinan frágang og tínslu er forgangsröðun frágangssniðmátsins tekið með í reikninginn þegar verið er að ganga frá móttökum.</span><span class="sxs-lookup"><span data-stu-id="649da-104">When the location is set up to use directed put-away and pick, priorities of the put-away template for the location are taken into account when putting receipts away.</span></span> <span data-ttu-id="649da-105">Á meðal forgangsatriða eru fast lágmarks- og hámarksmagn tiltekins hólfs og hólfaflokkanir.</span><span class="sxs-lookup"><span data-stu-id="649da-105">Priorities include the minimum and maximum quantities of bin content that have been fixed for a particular bin, and the bin rankings.</span></span> <span data-ttu-id="649da-106">Því fyllist á mest notuðu hólfin eftir því sem þau tæmast ef vörur berast jafnt og þétt.</span><span class="sxs-lookup"><span data-stu-id="649da-106">Therefore, if items are arriving at a steady pace, the most-used pick bins will be filled up as they are emptied.</span></span>  

<span data-ttu-id="649da-107">En birgðir berast ekki alltaf í jöfnum skömmtum.</span><span class="sxs-lookup"><span data-stu-id="649da-107">But inventory does not always arrive in a steady trickle.</span></span> <span data-ttu-id="649da-108">Stundum eru vörur keyptar í miklu magni til að fá afslátt eða þá að framleitt er mikið í einu til að lækka einingarkostnað.</span><span class="sxs-lookup"><span data-stu-id="649da-108">Sometimes, items are purchased in large quantities so that the company can obtain a rebate, or your production unit might produce a lot of one item to achieve a low unit cost.</span></span> <span data-ttu-id="649da-109">Þá berast vörurnar ekki aftur í vöruhúsið í nokkurn tíma og færa þarf vörur með reglulegu millibili í tínsluhólf úr geymslusvæðum.</span><span class="sxs-lookup"><span data-stu-id="649da-109">Then items will not be received in the warehouse again for some time, and the warehouse needs to periodically move items to pick bins from bulk storage areas.</span></span>  

<span data-ttu-id="649da-110">Einnig getur verið að von sé á nýjum birgðum og tæma eigi geymslusvæðið áður en nýju vörurnar koma.</span><span class="sxs-lookup"><span data-stu-id="649da-110">It could also be that the warehouse is expecting new stock to arrive soon and wants to empty the bulk storage area of items before the new merchandise arrives.</span></span>  

<span data-ttu-id="649da-111">Að lokum, hafi geymsluhólfin aðeins verið skilgreind fyrir **frágang** þ.e. tegund hólfanna er ekki með valda aðgerðina **Tína** þarf alltaf að hafa tínsluhólfin full þar sem ekki er ráðlagt að vörur séu tíndar úr hólfum sem eru bara fyrir frágang.</span><span class="sxs-lookup"><span data-stu-id="649da-111">Finally, if you have defined your bulk storage bins with a bin type action **Put Away** only, that is, the bin type does not have the **Pick** action selected, you must always keep your pick bins replenished, since Put Away-type bins are not suggested for a pick of inventory.</span></span>  

## <a name="to-replenish-pick-bins"></a><span data-ttu-id="649da-112">Fyllt á tínsluhólf</span><span class="sxs-lookup"><span data-stu-id="649da-112">To replenish pick bins</span></span>  
1.  <span data-ttu-id="649da-113">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Hreyfingavinnublað** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="649da-113">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Movement Worksheet**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="649da-114">Velja skal aðgerðina **Reikna áfyllingu hólfs** til að opna síður skýrslubeiðna.</span><span class="sxs-lookup"><span data-stu-id="649da-114">Choose the **Calculate Bin Replenishment** action to open the report request page.</span></span>  
3.  <span data-ttu-id="649da-115">Beiðnisíða keyrslunnar er fyllt út til að takmarka umfang áfyllingartillagna sem verða reiknaðar.</span><span class="sxs-lookup"><span data-stu-id="649da-115">Fill in the batch job request page to limit the scope of the replenishment suggestions that will be calculated.</span></span> <span data-ttu-id="649da-116">Til dæmis gæti átt að leggja áherslu á tilteknar vörur, svæði eða hólf.</span><span class="sxs-lookup"><span data-stu-id="649da-116">For example, you might be concerned with particular items, zones, or bins.</span></span>  
4.  <span data-ttu-id="649da-117">Velja hnappinn **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="649da-117">Choose the **OK** button.</span></span> <span data-ttu-id="649da-118">Línur eru stofnaðar fyrir áfyllingarhreyfingar sem þarf að framkvæma reglum sem settar hafa verið upp fyrir hólfin og innihald hólfa, þ.e. vörur í hólfum.</span><span class="sxs-lookup"><span data-stu-id="649da-118">Lines are created for the replenishment movements that need to be performed according to the rules that have been set up for the bins and bin contents, that is, items in bins.</span></span>  
5.  <span data-ttu-id="649da-119">Eigi að framkvæma allar áfyllingar sem lagðar eru til skal velja aðgerðina **Stofna hreyfingu**.</span><span class="sxs-lookup"><span data-stu-id="649da-119">If you want to perform all the suggested replenishments, choose the **Create Movement** action.</span></span> <span data-ttu-id="649da-120">Starfsmenn geta nú fundið leiðbeiningar í valmyndaratriðinu **Hreyfingar**, fylgt þeim og skráð þær.</span><span class="sxs-lookup"><span data-stu-id="649da-120">Employees can now find instructions in the **Movements** menu item, carry them out and register them.</span></span>  
6.  <span data-ttu-id="649da-121">Eigi aðeins að framkvæma sumar af tillögunum skal eyða línunum sem skipta minna máli og stofna síðan hreyfingu.</span><span class="sxs-lookup"><span data-stu-id="649da-121">If you only want some of the suggestions to be performed, delete the lines that are less important and then create a movement.</span></span>  

<span data-ttu-id="649da-122">Næst þegar áfylling hólfa er reiknuð verða tillögurnar sem eytt er stofnaðar aftur ef þær eiga enn við á þeim tíma.</span><span class="sxs-lookup"><span data-stu-id="649da-122">The next time you calculate bin replenishment, the suggestions that you have deleted will be recreated, if they are still valid at that time.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="649da-123">Ef eftirfarandi skilyrðum er fullnægt vegna vöru:</span><span class="sxs-lookup"><span data-stu-id="649da-123">If the following conditions are met for an item:</span></span>  
>   
>  -   <span data-ttu-id="649da-124">Varan er fyrningadagsett, og</span><span class="sxs-lookup"><span data-stu-id="649da-124">The item has an expiration date, and</span></span>  
> -   <span data-ttu-id="649da-125">Reiturinn **Tína eftir FEFO** í birgðageymsluspjaldinu er valinn og</span><span class="sxs-lookup"><span data-stu-id="649da-125">The **Pick According to FEFO** field on the location card is selected, and</span></span>  
> -   <span data-ttu-id="649da-126">Aðgerðin **Reikna út áfyllingu hólfs** er notuð</span><span class="sxs-lookup"><span data-stu-id="649da-126">You use the **Calculate Bin Replenishment** functionality</span></span>  
>   
>  <span data-ttu-id="649da-127">þá verða **Frá-svæði** og **Frá-hólf** reitirnir auðir vegna þess að reiknisögnin sem notuð er til að reikna hvaðan á að færa vörurnar er aðeins virkjuð þegar aðgerðin **Stofna hreyfingu** er ræst.</span><span class="sxs-lookup"><span data-stu-id="649da-127">then the **From Zone** and **From Bin** fields will be blank because the algorithm to calculate from where to move the items is triggered only when you activate the **Create Movement** function.</span></span>  

## <a name="see-also"></a><span data-ttu-id="649da-128">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="649da-128">See Also</span></span>  
[<span data-ttu-id="649da-129">Vöruhúsastjórnun</span><span class="sxs-lookup"><span data-stu-id="649da-129">Warehouse Management</span></span>](warehouse-manage-warehouse.md)  
[<span data-ttu-id="649da-130">Tínsla eftir FEFO</span><span class="sxs-lookup"><span data-stu-id="649da-130">Picking by FEFO</span></span>](warehouse-picking-by-fefo.md)  
[<span data-ttu-id="649da-131">Birgðir</span><span class="sxs-lookup"><span data-stu-id="649da-131">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="649da-132">[Vöruhúsastjórnun sett upp](warehouse-setup-warehouse.md)   </span><span class="sxs-lookup"><span data-stu-id="649da-132">[Setting Up Warehouse Management](warehouse-setup-warehouse.md)   </span></span>  
<span data-ttu-id="649da-133">[Samsetningardeild](assembly-assemble-items.md)  </span><span class="sxs-lookup"><span data-stu-id="649da-133">[Assembly Management](assembly-assemble-items.md)  </span></span>  
[<span data-ttu-id="649da-134">Hönnunarupplýsingar vöruhúsakerfi</span><span class="sxs-lookup"><span data-stu-id="649da-134">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="649da-135">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="649da-135">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
