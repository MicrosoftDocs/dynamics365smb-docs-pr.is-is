---
title: Hvernig á að bóka mörg skjöl á sama tíma | Microsoft Docs
description: Í stað þess að bóka eitt skjal í einu er hægt að velja mörg óbókuð skjöl í lista fyrir fjöldabókun, annaðhvort fyrir bókun án tafar eða sem til að mynda er áætluð við lok dags.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.reviewer: edupont
ms.date: 08/18/2020
ms.author: edupont
ms.openlocfilehash: 2c04dac37b043995a9b78e2f662f9411c3cf9ae1
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/09/2020
ms.locfileid: "3782519"
---
# <a name="post-multiple-documents-at-the-same-time"></a><span data-ttu-id="2f868-103">Bóka mörg skjöl á sama tíma</span><span class="sxs-lookup"><span data-stu-id="2f868-103">Post Multiple Documents at the Same Time</span></span>

<span data-ttu-id="2f868-104">Í stað þess að bóka eitt skjal í einu er hægt að velja mörg óbókuð skjöl í lista fyrir bókun án tafar eða fyrir fjöldabókun samkvæmt áætlun, svo sem við lok dags.</span><span class="sxs-lookup"><span data-stu-id="2f868-104">Instead of posting individual documents one by one, you can select multiple non-posted documents in a list for immediate posting or for batch posting according to a schedule, such as at the end of the day.</span></span> <span data-ttu-id="2f868-105">Þetta getur komið sér vel ef aðeins yfirmaður getur bókað skjöl sem aðrir notendur hafa búið til eða til að koma í veg fyrir vandamál tengd afköstum þegar bókun er gerð á vinnutíma.</span><span class="sxs-lookup"><span data-stu-id="2f868-105">This may be useful if only a supervisor can post documents created by other users or to avoid system performance issues from posting during work hours.</span></span>

## <a name="to-post-multiple-purchase-orders-immediately"></a><span data-ttu-id="2f868-106">Til að bóka margar innkaupapantanir strax</span><span class="sxs-lookup"><span data-stu-id="2f868-106">To post multiple purchase orders immediately</span></span>

<span data-ttu-id="2f868-107">Eftirfarandi ferli útskýrir hvernig á að bóka margar innkaupapantanir strax.</span><span class="sxs-lookup"><span data-stu-id="2f868-107">The following procedure explains how to post multiple purchase orders immediately.</span></span> <span data-ttu-id="2f868-108">Skrefin eru svipuð fyrir öll innkaupa- og söluskjöl.</span><span class="sxs-lookup"><span data-stu-id="2f868-108">The steps are similar for all purchase and sales documents.</span></span>

1. <span data-ttu-id="2f868-109">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Innkaupapantanir** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="2f868-109">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Purchase Orders**, and then choose the related link.</span></span>
2. <span data-ttu-id="2f868-110">Á síðunni **Innkaupapantanir** skal velja allar pantanir sem á að bóka:</span><span class="sxs-lookup"><span data-stu-id="2f868-110">On the **Purchase Orders** page, proceed to select all orders to be posted:</span></span>
3. <span data-ttu-id="2f868-111">Í reitnum **númer**</span><span class="sxs-lookup"><span data-stu-id="2f868-111">In the **No.**</span></span> <span data-ttu-id="2f868-112">skal velja þrjá lóðrétta punkta til að opna efnisvalmynd og síðan velja aðgerðina **Velja fleira**.</span><span class="sxs-lookup"><span data-stu-id="2f868-112">field, choose the three vertical dots to open the context menu, and then choose the **Select More** action.</span></span>
4. <span data-ttu-id="2f868-113">Veldu gátreitinn fyrir allar línurnar sem tákna pantanir sem á að bóka á sama tíma.</span><span class="sxs-lookup"><span data-stu-id="2f868-113">Select the check box for all the lines representing orders that you want to post at the same time.</span></span>
5. <span data-ttu-id="2f868-114">Veldu **Bókun** aðgerðina og svo aðgerðina **Bóka**.</span><span class="sxs-lookup"><span data-stu-id="2f868-114">Choose the **Posting** action, and then choose the **Post** action.</span></span>
6. <span data-ttu-id="2f868-115">Velja hnappinn **Já** á staðfestingarskilaboðunum.</span><span class="sxs-lookup"><span data-stu-id="2f868-115">Choose the **Yes** button on the confirmation message.</span></span>

## <a name="to-batch-post-multiple-purchase-orders"></a><span data-ttu-id="2f868-116">Til að runubóka marga innkaupapantanir</span><span class="sxs-lookup"><span data-stu-id="2f868-116">To batch post multiple purchase orders</span></span>

<span data-ttu-id="2f868-117">Eftirfarandi ferli útskýrir hvernig á að fjöldabóka innkaupapantanir.</span><span class="sxs-lookup"><span data-stu-id="2f868-117">The following procedure explains how to batch post purchase orders.</span></span> <span data-ttu-id="2f868-118">Skrefin eru svipuð fyrir öll innkaupa- og söluskjöl þar sem aðgerðin **Fjöldabóka** er í boði.</span><span class="sxs-lookup"><span data-stu-id="2f868-118">The steps are similar for all purchase and sales documents where the **Batch Post** action is available.</span></span>

> [!NOTE]
> <span data-ttu-id="2f868-119">Fjöldabókun á skjölum fer fram í bakgrunninum.</span><span class="sxs-lookup"><span data-stu-id="2f868-119">Batch posting of documents happens in the background.</span></span> <span data-ttu-id="2f868-120">[!INCLUDE [prodshort](includes/prodshort.md)] á netinu inniheldur sjálfgefin verk fyrir bókun í bakgrunni og fjöldabókun.</span><span class="sxs-lookup"><span data-stu-id="2f868-120">[!INCLUDE [prodshort](includes/prodshort.md)] online includes default jobs for background posting and batch posting.</span></span> <span data-ttu-id="2f868-121">Frekari upplýsingar, sjá [Nota verkraðir til að tímaraða verkhlutum](admin-job-queues-schedule-tasks.md).</span><span class="sxs-lookup"><span data-stu-id="2f868-121">For more information, see [Use Job Queues to Schedule Tasks](admin-job-queues-schedule-tasks.md).</span></span>

1. <span data-ttu-id="2f868-122">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Innkaupapantanir** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="2f868-122">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Purchase Orders**, and then choose the related link.</span></span>  
2. <span data-ttu-id="2f868-123">Á síðunni **Innkaupapantanir** skal velja allar pantanir sem á að bóka:</span><span class="sxs-lookup"><span data-stu-id="2f868-123">On the **Purchase Orders** page, proceed to select all orders to be posted:</span></span>
3. <span data-ttu-id="2f868-124">Í reitnum **númer**</span><span class="sxs-lookup"><span data-stu-id="2f868-124">In the **No.**</span></span> <span data-ttu-id="2f868-125">skal velja þrjá lóðrétta punkta til að opna efnisvalmynd og síðan velja aðgerðina **Velja fleira**.</span><span class="sxs-lookup"><span data-stu-id="2f868-125">field, choose the three vertical dots to open the context menu, and then choose the **Select More** action.</span></span>
4. <span data-ttu-id="2f868-126">Veldu gátreitinn fyrir allar línurnar sem tákna pantanir sem á að bóka á sama tíma.</span><span class="sxs-lookup"><span data-stu-id="2f868-126">Select the check box for all the lines representing orders that you want to post at the same time.</span></span>
5. <span data-ttu-id="2f868-127">Veldu **Bókun** aðgerðina og svo aðgerðina **Fjöldabóka**.</span><span class="sxs-lookup"><span data-stu-id="2f868-127">Choose the **Posting** action, and then choose the **Post Batch** action.</span></span>
6. <span data-ttu-id="2f868-128">Á síðunni **Innkaupapöntun fjöldabókunar** þarf að fylla reitina út eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="2f868-128">On the **Batch Post Purchase Order** page, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
7. <span data-ttu-id="2f868-129">Velja hnappinn **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="2f868-129">Choose the **OK** button.</span></span>
8. <span data-ttu-id="2f868-130">Til að skoða möguleg vandamál sem komu upp við fjöldabókun á skjölum skal opna síðuna **Skráning villuboða**.</span><span class="sxs-lookup"><span data-stu-id="2f868-130">To view potential issues that occurred during batch posting of documents, open the **Error Message Register** page.</span></span>

<span data-ttu-id="2f868-131">Innkaupapöntunum verður nú bætt við valda verkraðarfærslu, sem skilgreinir hvenær skjölin eru bókuð.</span><span class="sxs-lookup"><span data-stu-id="2f868-131">The purchase orders will now be added to a dedicated job queue entry, which defines when the documents are posted.</span></span> <span data-ttu-id="2f868-132">Frekari upplýsingar, sjá [Nota verkraðir til að tímaraða verkhlutum](admin-job-queues-schedule-tasks.md).</span><span class="sxs-lookup"><span data-stu-id="2f868-132">For more information, see [Use Job Queues to Schedule Tasks](admin-job-queues-schedule-tasks.md).</span></span>

<span data-ttu-id="2f868-133">Ef valið er **PDF** í reitnum **Skýrslufrálagsgerð** verða bókaðar innkaupapantanir sem heppnuðust tiltækar í hlutanum **Skýrsluinnhólf** í hlutverkamiðstöðinni.</span><span class="sxs-lookup"><span data-stu-id="2f868-133">If you select **PDF** in the **Report Output Type** field, successfully posted purchase orders will be available in the **Report Inbox** part on your Role Center.</span></span>

## <a name="see-also"></a><span data-ttu-id="2f868-134">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="2f868-134">See Also</span></span>

[<span data-ttu-id="2f868-135">Bókun skjala og færslubóka</span><span class="sxs-lookup"><span data-stu-id="2f868-135">Posting Documents and Journals</span></span>](ui-post-documents-journals.md)  
[<span data-ttu-id="2f868-136">Nota verkraðir til að tímaraða verkhlutum</span><span class="sxs-lookup"><span data-stu-id="2f868-136">Use Job Queues to Schedule Tasks</span></span>](admin-job-queues-schedule-tasks.md)  
[<span data-ttu-id="2f868-137">Breyta bókuðum skjölum</span><span class="sxs-lookup"><span data-stu-id="2f868-137">Edit Posted Documents</span></span>](across-edit-posted-document.md)  
[<span data-ttu-id="2f868-138">Leiðrétta eða afturkalla ógreidda innkaupareikninga</span><span class="sxs-lookup"><span data-stu-id="2f868-138">Correct or Cancel Unpaid Purchase Invoices</span></span>](purchasing-how-correct-cancel-unpaid-purchase-invoices.md)  
[<span data-ttu-id="2f868-139">Finndu síður og upplýsingar með Viðmótsleit</span><span class="sxs-lookup"><span data-stu-id="2f868-139">Finding Pages and Information with Tell Me</span></span>](ui-search.md)  
<span data-ttu-id="2f868-140">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="2f868-140">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
