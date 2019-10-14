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
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 15b0afcf04ad279000de227523f977fdb695fe01
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/01/2019
ms.locfileid: "2316788"
---
# <a name="post-multiple-documents-at-the-same-time"></a><span data-ttu-id="1a6b8-103">Bóka mörg skjöl á sama tíma</span><span class="sxs-lookup"><span data-stu-id="1a6b8-103">Post Multiple Documents at the Same Time</span></span>
<span data-ttu-id="1a6b8-104">Í stað þess að bóka eitt skjal í einu er hægt að velja mörg óbókuð skjöl í lista fyrir bókun án tafar eða fyrir fjöldabókun samkvæmt áætlun, svo sem við lok dags.</span><span class="sxs-lookup"><span data-stu-id="1a6b8-104">Instead of posting individual documents one by one, you can select multiple non-posted documents in a list for immediate posting or for batch posting according to a schedule, such as at the end of the day.</span></span> <span data-ttu-id="1a6b8-105">Þetta getur komið sér vel ef aðeins yfirmaður getur bókað skjöl sem aðrir notendur hafa búið til eða til að koma í veg fyrir vandamál tengd afköstum þegar bókun er gerð á vinnutíma.</span><span class="sxs-lookup"><span data-stu-id="1a6b8-105">This may be useful if only a supervisor can post documents created by other users or to avoid system performance issues from posting during work hours.</span></span>

## <a name="to-post-multiple-purchase-orders-immediately"></a><span data-ttu-id="1a6b8-106">Til að bóka margar innkaupapantanir strax</span><span class="sxs-lookup"><span data-stu-id="1a6b8-106">To post multiple purchase orders immediately</span></span>
<span data-ttu-id="1a6b8-107">Eftirfarandi ferli útskýrir hvernig á að bóka margar innkaupapantanir strax.</span><span class="sxs-lookup"><span data-stu-id="1a6b8-107">The following procedure explains how to post multiple purchase orders immediately.</span></span> <span data-ttu-id="1a6b8-108">Skrefin eru svipuð fyrir öll innkaupa- og söluskjöl.</span><span class="sxs-lookup"><span data-stu-id="1a6b8-108">The steps are similar for all purchase and sales documents.</span></span>

1. <span data-ttu-id="1a6b8-109">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Innkaupapantanir** og veldu síðan tengda hlekkinn.</span><span class="sxs-lookup"><span data-stu-id="1a6b8-109">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Purchase Orders**, and then choose the related link.</span></span>
2. <span data-ttu-id="1a6b8-110">Á síðunni **Innkaupapantanir** skal velja allar pantanir sem á að bóka:</span><span class="sxs-lookup"><span data-stu-id="1a6b8-110">On the **Purchase Orders** page, proceed to select all orders to be posted:</span></span>
3. <span data-ttu-id="1a6b8-111">Í reitnum **númer**</span><span class="sxs-lookup"><span data-stu-id="1a6b8-111">In the **No.**</span></span> <span data-ttu-id="1a6b8-112">skal velja þrjá lóðrétta punkta til að opna efnisvalmynd og síðan velja aðgerðina **Velja fleira**.</span><span class="sxs-lookup"><span data-stu-id="1a6b8-112">field, choose the three vertical dots to open the context menu, and then choose the **Select More** action.</span></span>
4. <span data-ttu-id="1a6b8-113">Veldu gátreitinn fyrir allar línurnar sem tákna pantanir sem á að bóka á sama tíma.</span><span class="sxs-lookup"><span data-stu-id="1a6b8-113">Select the check box for all the lines representing orders that you want to post at the same time.</span></span>
5. <span data-ttu-id="1a6b8-114">Veldu **Bókun** aðgerðina og svo aðgerðina **Bóka**.</span><span class="sxs-lookup"><span data-stu-id="1a6b8-114">Choose the **Posting** action, and then choose the **Post** action.</span></span>
6. <span data-ttu-id="1a6b8-115">Velja hnappinn **Já** á staðfestingarskilaboðunum.</span><span class="sxs-lookup"><span data-stu-id="1a6b8-115">Choose the **Yes** button on the confirmation message.</span></span>

## <a name="to-batch-post-multiple-purchase-orders"></a><span data-ttu-id="1a6b8-116">Til að runubóka marga innkaupapantanir</span><span class="sxs-lookup"><span data-stu-id="1a6b8-116">To batch post multiple purchase orders</span></span>
<span data-ttu-id="1a6b8-117">Eftirfarandi ferli útskýrir hvernig á að fjöldabóka innkaupapantanir.</span><span class="sxs-lookup"><span data-stu-id="1a6b8-117">The following procedure explains how to batch post purchase orders.</span></span> <span data-ttu-id="1a6b8-118">Skrefin eru svipuð fyrir öll innkaupa- og söluskjöl þar sem aðgerðin **Fjöldabóka** er í boði.</span><span class="sxs-lookup"><span data-stu-id="1a6b8-118">The steps are similar for all purchase and sales documents where the **Batch Post** action is available.</span></span>

> [!NOTE]
> <span data-ttu-id="1a6b8-119">Fjöldabókun á skjölum gerist í bakgrunninum eins og það er skilgreint af verkraðarfærslu, sem þarf fyrst að setja upp.</span><span class="sxs-lookup"><span data-stu-id="1a6b8-119">Batch posting of documents happens in the background as defined by a job queue entry, which must first be set up.</span></span> <span data-ttu-id="1a6b8-120">Frekari upplýsingar, sjá [Nota verkraðir til að tímaraða verkhlutum](admin-job-queues-schedule-tasks.md).</span><span class="sxs-lookup"><span data-stu-id="1a6b8-120">For more information, see [Use Job Queues to Schedule Tasks](admin-job-queues-schedule-tasks.md).</span></span>

1. <span data-ttu-id="1a6b8-121">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Innkaupapantanir** og veldu síðan tengda hlekkinn.</span><span class="sxs-lookup"><span data-stu-id="1a6b8-121">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Purchase Orders**, and then choose the related link.</span></span>  
2. <span data-ttu-id="1a6b8-122">Á síðunni **Innkaupapantanir** skal velja allar pantanir sem á að bóka:</span><span class="sxs-lookup"><span data-stu-id="1a6b8-122">On the **Purchase Orders** page, proceed to select all orders to be posted:</span></span>
3. <span data-ttu-id="1a6b8-123">Í reitnum **númer**</span><span class="sxs-lookup"><span data-stu-id="1a6b8-123">In the **No.**</span></span> <span data-ttu-id="1a6b8-124">skal velja þrjá lóðrétta punkta til að opna efnisvalmynd og síðan velja aðgerðina **Velja fleira**.</span><span class="sxs-lookup"><span data-stu-id="1a6b8-124">field, choose the three vertical dots to open the context menu, and then choose the **Select More** action.</span></span>
4. <span data-ttu-id="1a6b8-125">Veldu gátreitinn fyrir allar línurnar sem tákna pantanir sem á að bóka á sama tíma.</span><span class="sxs-lookup"><span data-stu-id="1a6b8-125">Select the check box for all the lines representing orders that you want to post at the same time.</span></span>
5. <span data-ttu-id="1a6b8-126">Veldu **Bókun** aðgerðina og svo aðgerðina **Fjöldabóka**.</span><span class="sxs-lookup"><span data-stu-id="1a6b8-126">Choose the **Posting** action, and then choose the **Post Batch** action.</span></span>
6. <span data-ttu-id="1a6b8-127">Á síðunni **Innkaupapöntun fjöldabókunar** þarf að fylla reitina út eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="1a6b8-127">On the **Batch Post Purchase Order** page, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]
    > <span data-ttu-id="1a6b8-128">Til að prenta tengdar skýrslur þegar bókað er, t.d. skýrsluna **Pöntunarstaðfesting** fyrir sölupantanir, skal velja gátreitinn **Prenta**.</span><span class="sxs-lookup"><span data-stu-id="1a6b8-128">To print related reports when posting, such as the **Order Confirmation** report for sales orders, select the **Print** check box.</span></span><br /><br /> <span data-ttu-id="1a6b8-129">Í reitnum **Skýrslufrálagsgerð** á síðunni **Uppsetning sölu og útistandandi** er á síðunni **Uppsetning innkaupa og viðskiptaskulda** er skilgreint hvort prenta eigi skýrsluna eða sýna hana sem PDF.</span><span class="sxs-lookup"><span data-stu-id="1a6b8-129">In the **Report Output Type** field on the **Sales and Receivables Setup** page or **Purchases and Payables Setup** page, you define if the report will be printed or output as a PDF.</span></span><br /><br /> <span data-ttu-id="1a6b8-130">Athugið líka að bein prentun á völdum prentara er aðeins möguleg í uppsetningum innanhúss.</span><span class="sxs-lookup"><span data-stu-id="1a6b8-130">Note also that direct printing to a selected printer is only possible in on-premises installations.</span></span>

7. <span data-ttu-id="1a6b8-131">Velja hnappinn **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="1a6b8-131">Choose the **OK** button.</span></span>
8. <span data-ttu-id="1a6b8-132">Til að skoða möguleg vandamál sem komu upp við fjöldabókun á skjölum skal opna síðuna **Skráning villuboða**.</span><span class="sxs-lookup"><span data-stu-id="1a6b8-132">To view potential issues that occurred during batch posting of documents, open the **Error Message Register** page.</span></span>

<span data-ttu-id="1a6b8-133">Innkaupapöntunum verður nú bætt við valda verkraðarfærslu, sem skilgreinir hvenær skjölin eru bókuð.</span><span class="sxs-lookup"><span data-stu-id="1a6b8-133">The purchase orders will now be added to a dedicated job queue entry, which defines when the documents are posted.</span></span> <span data-ttu-id="1a6b8-134">Frekari upplýsingar, sjá [Nota verkraðir til að tímaraða verkhlutum](admin-job-queues-schedule-tasks.md).</span><span class="sxs-lookup"><span data-stu-id="1a6b8-134">For more information, see [Use Job Queues to Schedule Tasks](admin-job-queues-schedule-tasks.md).</span></span>

<span data-ttu-id="1a6b8-135">Ef valið er **PDF** í reitnum **Skýrslufrálagsgerð** verða bókaðar innkaupapantanir sem heppnuðust tiltækar í hlutanum **Skýrsluinnhólf** í hlutverkamiðstöðinni.</span><span class="sxs-lookup"><span data-stu-id="1a6b8-135">If you select **PDF** in the **Report Output Type** field, successfully posted purchase orders will be available in the **Report Inbox** part on your Role Center.</span></span>

## <a name="see-also"></a><span data-ttu-id="1a6b8-136">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="1a6b8-136">See Also</span></span>
[<span data-ttu-id="1a6b8-137">Bókun skjala og færslubóka</span><span class="sxs-lookup"><span data-stu-id="1a6b8-137">Posting Documents and Journals</span></span>](ui-post-documents-journals.md)  
[<span data-ttu-id="1a6b8-138">Nota verkraðir til að tímaraða verkhlutum</span><span class="sxs-lookup"><span data-stu-id="1a6b8-138">Use Job Queues to Schedule Tasks</span></span>](admin-job-queues-schedule-tasks.md)  
[<span data-ttu-id="1a6b8-139">Breyta bókuðum skjölum</span><span class="sxs-lookup"><span data-stu-id="1a6b8-139">Edit Posted Documents</span></span>](across-edit-posted-document.md)  
[<span data-ttu-id="1a6b8-140">Leiðrétta eða afturkalla ógreidda innkaupareikninga</span><span class="sxs-lookup"><span data-stu-id="1a6b8-140">Correct or Cancel Unpaid Purchase Invoices</span></span>](purchasing-how-correct-cancel-unpaid-purchase-invoices.md)  
[<span data-ttu-id="1a6b8-141">Finndu síður og upplýsingar með Viðmótsleit</span><span class="sxs-lookup"><span data-stu-id="1a6b8-141">Finding Pages and Information with Tell Me</span></span>](ui-search.md)  
<span data-ttu-id="1a6b8-142">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="1a6b8-142">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
