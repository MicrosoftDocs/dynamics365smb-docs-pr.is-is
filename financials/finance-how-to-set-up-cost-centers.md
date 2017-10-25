---
title: "Hvernig á að setja upp Kostnaðarstaði | Microsoft Docs"
description: "Kostnaðarstaðir eru deildir og framlegðarstöðvar sem bera ábyrgð á kostnaði og tekjum. Myndrit kostnaðarstaða er svipað og víddarupplýsingar fyrir fjárhag."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 433526fbd2a13f32e64be94cc1936151445c19f5
ms.contentlocale: is-is
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-set-up-cost-centers"></a><span data-ttu-id="12f63-104">Hvernig á að setja upp Kostnaðarstaði</span><span class="sxs-lookup"><span data-stu-id="12f63-104">How to: Set Up Cost Centers</span></span>
<span data-ttu-id="12f63-105">Kostnaðarstaðir eru deildir og framlegðarstöðvar sem bera ábyrgð á kostnaði og tekjum.</span><span class="sxs-lookup"><span data-stu-id="12f63-105">Cost centers are departments that are responsible for costs and income.</span></span> <span data-ttu-id="12f63-106">Myndrit kostnaðarstaða er svipað og víddarupplýsingar fyrir fjárhag.</span><span class="sxs-lookup"><span data-stu-id="12f63-106">The chart of cost centers is similar to the dimension information for the general ledger.</span></span> <span data-ttu-id="12f63-107">Hægt er að setja upp myndritið yfir kostnaðarstaði á eftirfarandi hátt:</span><span class="sxs-lookup"><span data-stu-id="12f63-107">You can set up the chart of cost centers in the following ways:</span></span>  

-   <span data-ttu-id="12f63-108">Flytja víddargildi í fjárhag í myndrit yfir í kostnaðarstaði.</span><span class="sxs-lookup"><span data-stu-id="12f63-108">Transfer dimension values in the general ledger to the chart of cost centers.</span></span> <span data-ttu-id="12f63-109">Hægt er að gera allar nauðsynlegar leiðréttingar eftir flutninginn.</span><span class="sxs-lookup"><span data-stu-id="12f63-109">You can make any necessary adjustments after the transfer.</span></span>  
-   <span data-ttu-id="12f63-110">Stofna nýjan kostnaðarstað sem er óháður fjárhagnum eða bæta nýjum kostnaðarstað við kostnaðarstað sem fyrir er.</span><span class="sxs-lookup"><span data-stu-id="12f63-110">Create a new chart of cost center that is independent of the general ledger or add a new cost center to an existing chart of cost center.</span></span> <span data-ttu-id="12f63-111">Stofna þarf hvern kostnaðarstað sérstaklega.</span><span class="sxs-lookup"><span data-stu-id="12f63-111">You must create each cost center individually.</span></span>  

## <a name="to-transfer-dimension-values-in-the-general-ledger-to-the-chart-of-cost-centers"></a><span data-ttu-id="12f63-112">Til að flytja víddargildi í fjárhag í myndrit yfir í kostnaðarstaði</span><span class="sxs-lookup"><span data-stu-id="12f63-112">To transfer dimension values in the general ledger to the chart of cost centers</span></span>  
1.  <span data-ttu-id="12f63-113">Setja upp vídd sem á að vera kostnaðarstaðarvíddin í glugganum **Uppfæra Kostnaðarbókhaldsvíddir**.</span><span class="sxs-lookup"><span data-stu-id="12f63-113">Set up a dimension to be the cost center dimension in the **Update Cost Acctg. Dimensions** window.</span></span> <span data-ttu-id="12f63-114">Aðeins gildi úr þessari vídd er flutt.</span><span class="sxs-lookup"><span data-stu-id="12f63-114">Only the values from this dimension are transferred.</span></span>  
2.  <span data-ttu-id="12f63-115">Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Myndrit yfir kostnaðarstaði** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="12f63-115">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Chart of Cost Centers**, and then choose the related link.</span></span>  
3.  <span data-ttu-id="12f63-116">Í flipanum **Aðgerðir** í flokknum **Eiginleikar** veljið **Sækja úr víddinni kostnaðarstaðir** til að flytja víddargildi í myndriti kostnaðarstaðanna.</span><span class="sxs-lookup"><span data-stu-id="12f63-116">On the **Actions** tab, in the **Functions** group, choose **Get Cost Centers from Dimension** to transfer dimension values to the chart of cost centers.</span></span> <span data-ttu-id="12f63-117">Aðgerðin flytur víddargildin sem skilgreind voru í skrefi 1.</span><span class="sxs-lookup"><span data-stu-id="12f63-117">The function transfers the dimension values that you defined in step 1.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="12f63-118">Hægt er að setja reitinn **Stilla kostnaðarstaðavíddir** upp þannig að hann skilgreini einstefnusamstillingu á víddargildum frá fjárhag yfir í myndrit yfir kostnaðarstaði.</span><span class="sxs-lookup"><span data-stu-id="12f63-118">You can set up the **Align Cost Center Dimension**  field to define a one-way synchronization of dimension values from the general ledger to the chart of cost centers.</span></span> <span data-ttu-id="12f63-119">Ekki er hægt að skilreina samstillingu myndrits yfir kostnaðarstaði við víddargildi úr fjárhag.</span><span class="sxs-lookup"><span data-stu-id="12f63-119">You cannot define a synchronization of the chart of cost centers to dimension values from the general ledger.</span></span>  

<span data-ttu-id="12f63-120">Myndrit kostnaðarstaða inniheldur nú öll tilgreind víddargildi úr fjárhag og inniheldur titla og samtölur.</span><span class="sxs-lookup"><span data-stu-id="12f63-120">The chart of cost centers now contains all specified dimension values from the general ledger and includes titles and subtotals.</span></span>  

## <a name="to-create-new-cost-centers-in-the-chart-of-cost-centers-window"></a><span data-ttu-id="12f63-121">Til að stofna nýja kostnaðarstaði í glugganum Myndrit fyrir kostnaðarstaði</span><span class="sxs-lookup"><span data-stu-id="12f63-121">To create new cost centers in the Chart of Cost Centers window</span></span>  
<span data-ttu-id="12f63-122">Hægt er að setja upp og vinna með kostnaðarstaði í **Kostnaðarstaðaspjald** spjaldinu eða í glugganum **Myndrit fyrir kostnaðarstaði**.</span><span class="sxs-lookup"><span data-stu-id="12f63-122">You can set up and maintain cost centers in either the **Cost Center Card** card or in the **Chart of Cost Centers** window.</span></span> <span data-ttu-id="12f63-123">Í þessu ferli eru settir upp kostnaðarstaðir í glugganum **Myndrit fyrir kostnaðarstaði**.</span><span class="sxs-lookup"><span data-stu-id="12f63-123">In this procedure, you set up cost centers in the **Chart of Cost Centers** window.</span></span>  

1. <span data-ttu-id="12f63-124">Opna gluggann **myndrit yfir kostnaðarstaði** í breytingarstillingu.</span><span class="sxs-lookup"><span data-stu-id="12f63-124">Open the **Chart of Cost Centers** window in edit mode.</span></span>  
2. <span data-ttu-id="12f63-125">Í reitinn **Kóði** er færður inn kóti kostnaðarstaðarins.</span><span class="sxs-lookup"><span data-stu-id="12f63-125">In the **Code** field, enter the cost center code.</span></span> <span data-ttu-id="12f63-126">Allir kostnaðarstaðir verða að hafa kóta.</span><span class="sxs-lookup"><span data-stu-id="12f63-126">All cost centers must have a code.</span></span>  
3. <span data-ttu-id="12f63-127">Í reitinn **Heiti** er fært inn heiti kostnaðarstaðarins.</span><span class="sxs-lookup"><span data-stu-id="12f63-127">In the **Name** field, enter the cost center name.</span></span>  
4. <span data-ttu-id="12f63-128">Velja fellilistaörina í reitnum **Línugerð** til að tilgreina tilgang kostnaðarstaðarins.</span><span class="sxs-lookup"><span data-stu-id="12f63-128">Choose the drop-down arrow in the **Line Type** field to specify the purpose of the cost center.</span></span>  

    - <span data-ttu-id="12f63-129">Fylla þarf út í reitinn **Samtala** fyrir kostnaðarstaði af gerðinni **Samtals**.</span><span class="sxs-lookup"><span data-stu-id="12f63-129">For cost centers of the **Total** type, you must fill in the **Totaling** field.</span></span> <span data-ttu-id="12f63-130">Nota skal virkinn **eða**, sem er lóðrétt lína (**&#124;**) til að stilla svið kostnaðarstaða.</span><span class="sxs-lookup"><span data-stu-id="12f63-130">Use the **or** operator, which is a vertical line (**&#124;**) to set ranges of cost centers.</span></span>  
    - <span data-ttu-id="12f63-131">Fyrir kostnaðarstaði af línutegundinni **Til-tala** er sjálfkrafa fyllt út í reitinn þegar inndráttarvirknin er notuð.</span><span class="sxs-lookup"><span data-stu-id="12f63-131">For cost centers of the **End-Total** line type, this field is filled in automatically when you use the indent function.</span></span>  
5.  <span data-ttu-id="12f63-132">Fyllið upp í reitina **Röðunarpöntun** og **Undirflokkar kostnaðar**.</span><span class="sxs-lookup"><span data-stu-id="12f63-132">Fill in the **Sorting Order** and **Cost Subtype** fields.</span></span>  
6.  <span data-ttu-id="12f63-133">Velja næstu tómu línu til að stofna nýjan kostnaðarstað og endurtaka síðan þrep 2 til 5.</span><span class="sxs-lookup"><span data-stu-id="12f63-133">Choose the next empty line to create a new cost center, and then repeat steps 2 through 5.</span></span>  
7.  <span data-ttu-id="12f63-134">Þegar búið er að setja upp alla kostnaðarstað skal velja aðgerðina **Draga inn kostnaðarstaði**.</span><span class="sxs-lookup"><span data-stu-id="12f63-134">After you have set up all the cost centers, choose the **Indent Cost Centers** action.</span></span> <span data-ttu-id="12f63-135">Velja hnappinn **Já**.</span><span class="sxs-lookup"><span data-stu-id="12f63-135">Choose the **Yes** button.</span></span>  

> [!IMPORTANT]  
>  <span data-ttu-id="12f63-136">Ef skilgreiningar voru færðar inn í **Samtölur** reitina fyrir **Loka-samtala** kostnaðarstaði áður en inndráttaraðgerðin var keyrð þarf að færa þær inn aftur.</span><span class="sxs-lookup"><span data-stu-id="12f63-136">If you have entered definitions in the **Totaling** fields for **End-Total** cost centers before you run the indent function, then you must enter them again.</span></span> <span data-ttu-id="12f63-137">Aðgerðin skrifar yfir gildin í öllum **Til-tala** reitum.</span><span class="sxs-lookup"><span data-stu-id="12f63-137">The function overwrites the values in all **End-Total** fields.</span></span>  

## <a name="see-also"></a><span data-ttu-id="12f63-138">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="12f63-138">See Also</span></span>  
[<span data-ttu-id="12f63-139">Kostnaðarreikningur</span><span class="sxs-lookup"><span data-stu-id="12f63-139">Accounting for Costs</span></span>](finance-manage-cost-accounting.md)  
<span data-ttu-id="12f63-140">[Uppsetning kostnaðarbókhalds](finance-set-up-cost-accounting.md) </span><span class="sxs-lookup"><span data-stu-id="12f63-140">[Setting Up Cost Accounting](finance-set-up-cost-accounting.md) </span></span>  
<span data-ttu-id="12f63-141">[Orðalisti í kostnaðarbókhaldi](finance-terminology-in-cost-accounting.md) </span><span class="sxs-lookup"><span data-stu-id="12f63-141">[Terminology in Cost Accounting](finance-terminology-in-cost-accounting.md) </span></span>  
[<span data-ttu-id="12f63-142">Um kostnaðarbókhald</span><span class="sxs-lookup"><span data-stu-id="12f63-142">About Cost Accounting</span></span>](finance-about-cost-accounting.md)  
<span data-ttu-id="12f63-143">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="12f63-143">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

