---
title: Hvernig á að setja upp Kostnaðarstaði | Microsoft Docs
description: Kostnaðarstaðir eru deildir og framlegðarstöðvar sem bera ábyrgð á kostnaði og tekjum. Myndrit kostnaðarstaða er svipað og víddarupplýsingar fyrir fjárhag.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 11/13/2018
ms.author: sgroespe
redirect_url: finance-set-up-cost-accounting
ms.openlocfilehash: 252ebf514635ada8e07bfb1e950d0cff156d0bfc
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/08/2019
ms.locfileid: "799612"
---
# <a name="set-up-cost-centers"></a><span data-ttu-id="a0f92-104">Uppsetning kostnaðarstaða</span><span class="sxs-lookup"><span data-stu-id="a0f92-104">Set Up Cost Centers</span></span>
<span data-ttu-id="a0f92-105">Kostnaðarstaðir eru deildir og framlegðarstöðvar sem bera ábyrgð á kostnaði og tekjum.</span><span class="sxs-lookup"><span data-stu-id="a0f92-105">Cost centers are departments that are responsible for costs and income.</span></span> <span data-ttu-id="a0f92-106">Myndrit kostnaðarstaða er svipað og víddarupplýsingar fyrir fjárhag.</span><span class="sxs-lookup"><span data-stu-id="a0f92-106">The chart of cost centers is similar to the dimension information for the general ledger.</span></span> <span data-ttu-id="a0f92-107">Hægt er að setja upp myndritið yfir kostnaðarstaði á eftirfarandi hátt:</span><span class="sxs-lookup"><span data-stu-id="a0f92-107">You can set up the chart of cost centers in the following ways:</span></span>  

-   <span data-ttu-id="a0f92-108">Flytja víddargildi í fjárhag í myndrit yfir í kostnaðarstaði.</span><span class="sxs-lookup"><span data-stu-id="a0f92-108">Transfer dimension values in the general ledger to the chart of cost centers.</span></span> <span data-ttu-id="a0f92-109">Hægt er að gera allar nauðsynlegar leiðréttingar eftir flutninginn.</span><span class="sxs-lookup"><span data-stu-id="a0f92-109">You can make any necessary adjustments after the transfer.</span></span>  
-   <span data-ttu-id="a0f92-110">Stofna nýjan kostnaðarstað sem er óháður fjárhagnum eða bæta nýjum kostnaðarstað við kostnaðarstað sem fyrir er.</span><span class="sxs-lookup"><span data-stu-id="a0f92-110">Create a new chart of cost center that is independent of the general ledger or add a new cost center to an existing chart of cost center.</span></span> <span data-ttu-id="a0f92-111">Stofna þarf hvern kostnaðarstað sérstaklega.</span><span class="sxs-lookup"><span data-stu-id="a0f92-111">You must create each cost center individually.</span></span>  

## <a name="to-transfer-dimension-values-in-the-general-ledger-to-the-chart-of-cost-centers"></a><span data-ttu-id="a0f92-112">Til að flytja víddargildi í fjárhag í myndrit yfir í kostnaðarstaði</span><span class="sxs-lookup"><span data-stu-id="a0f92-112">To transfer dimension values in the general ledger to the chart of cost centers</span></span>  
1.  <span data-ttu-id="a0f92-113">Setja upp vídd sem á að vera kostnaðarstaðarvíddin á síðunni **Uppfæra Kostnaðarbókhaldsvíddir**.</span><span class="sxs-lookup"><span data-stu-id="a0f92-113">Set up a dimension to be the cost center dimension on the **Update Cost Acctg. Dimensions** page.</span></span> <span data-ttu-id="a0f92-114">Aðeins gildi úr þessari vídd er flutt.</span><span class="sxs-lookup"><span data-stu-id="a0f92-114">Only the values from this dimension are transferred.</span></span>  
2.  <span data-ttu-id="a0f92-115">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Myndrit yfir kostnaðarstaði** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="a0f92-115">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Chart of Cost Centers**, and then choose the related link.</span></span>  
3.  <span data-ttu-id="a0f92-116">Í flipanum **Aðgerðir** í flokknum **Eiginleikar** veljið **Sækja úr víddinni kostnaðarstaðir** til að flytja víddargildi í myndriti kostnaðarstaðanna.</span><span class="sxs-lookup"><span data-stu-id="a0f92-116">On the **Actions** tab, in the **Functions** group, choose **Get Cost Centers from Dimension** to transfer dimension values to the chart of cost centers.</span></span> <span data-ttu-id="a0f92-117">Aðgerðin flytur víddargildin sem skilgreind voru í skrefi 1.</span><span class="sxs-lookup"><span data-stu-id="a0f92-117">The function transfers the dimension values that you defined in step 1.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="a0f92-118">Hægt er að setja reitinn **Stilla kostnaðarstaðavíddir** upp þannig að hann skilgreini einstefnusamstillingu á víddargildum frá fjárhag yfir í myndrit yfir kostnaðarstaði.</span><span class="sxs-lookup"><span data-stu-id="a0f92-118">You can set up the **Align Cost Center Dimension**  field to define a one-way synchronization of dimension values from the general ledger to the chart of cost centers.</span></span> <span data-ttu-id="a0f92-119">Ekki er hægt að skilreina samstillingu myndrits yfir kostnaðarstaði við víddargildi úr fjárhag.</span><span class="sxs-lookup"><span data-stu-id="a0f92-119">You cannot define a synchronization of the chart of cost centers to dimension values from the general ledger.</span></span>  

<span data-ttu-id="a0f92-120">Myndrit kostnaðarstaða inniheldur nú öll tilgreind víddargildi úr fjárhag og inniheldur titla og samtölur.</span><span class="sxs-lookup"><span data-stu-id="a0f92-120">The chart of cost centers now contains all specified dimension values from the general ledger and includes titles and subtotals.</span></span>  

## <a name="to-create-new-cost-centers-in-the-chart-of-cost-centers-page"></a><span data-ttu-id="a0f92-121">Til að stofna nýja kostnaðarstaði á síðunni Myndrit fyrir kostnaðarstaði</span><span class="sxs-lookup"><span data-stu-id="a0f92-121">To create new cost centers in the Chart of Cost Centers page</span></span>  
<span data-ttu-id="a0f92-122">Hægt er að setja upp og vinna með kostnaðarstaði í **Kostnaðarstaðaspjald** spjaldinu eða á síðunni **Myndrit fyrir kostnaðarstaði**.</span><span class="sxs-lookup"><span data-stu-id="a0f92-122">You can set up and maintain cost centers in either the **Cost Center Card** card or on the **Chart of Cost Centers** page.</span></span> <span data-ttu-id="a0f92-123">Í þessu ferli eru settir upp kostnaðarstaðir á síðunni **Myndrit fyrir kostnaðarstaði**.</span><span class="sxs-lookup"><span data-stu-id="a0f92-123">In this procedure, you set up cost centers on the **Chart of Cost Centers** page.</span></span>  

1. <span data-ttu-id="a0f92-124">Opnaðu síðuna **Myndrit yfir kostnaðarstaði** í breytingarstillingu.</span><span class="sxs-lookup"><span data-stu-id="a0f92-124">Open the **Chart of Cost Centers** page in edit mode.</span></span>  
2. <span data-ttu-id="a0f92-125">Í reitinn **Kóði** er færður inn kóti kostnaðarstaðarins.</span><span class="sxs-lookup"><span data-stu-id="a0f92-125">In the **Code** field, enter the cost center code.</span></span> <span data-ttu-id="a0f92-126">Allir kostnaðarstaðir verða að hafa kóta.</span><span class="sxs-lookup"><span data-stu-id="a0f92-126">All cost centers must have a code.</span></span>  
3. <span data-ttu-id="a0f92-127">Í reitinn **Heiti** er fært inn heiti kostnaðarstaðarins.</span><span class="sxs-lookup"><span data-stu-id="a0f92-127">In the **Name** field, enter the cost center name.</span></span>  
4. <span data-ttu-id="a0f92-128">Velja fellilistaörina í reitnum **Línugerð** til að tilgreina tilgang kostnaðarstaðarins.</span><span class="sxs-lookup"><span data-stu-id="a0f92-128">Choose the drop-down arrow in the **Line Type** field to specify the purpose of the cost center.</span></span>  

    - <span data-ttu-id="a0f92-129">Fylla þarf út í reitinn **Samtala** fyrir kostnaðarstaði af gerðinni **Samtals**.</span><span class="sxs-lookup"><span data-stu-id="a0f92-129">For cost centers of the **Total** type, you must fill in the **Totaling** field.</span></span> <span data-ttu-id="a0f92-130">Nota skal virkinn **eða**, sem er lóðrétt lína (**&#124;**) til að stilla svið kostnaðarstaða.</span><span class="sxs-lookup"><span data-stu-id="a0f92-130">Use the **or** operator, which is a vertical line (**&#124;**) to set ranges of cost centers.</span></span>  
    - <span data-ttu-id="a0f92-131">Fyrir kostnaðarstaði af línutegundinni **Til-tala** er sjálfkrafa fyllt út í reitinn þegar inndráttarvirknin er notuð.</span><span class="sxs-lookup"><span data-stu-id="a0f92-131">For cost centers of the **End-Total** line type, this field is filled in automatically when you use the indent function.</span></span>  
5.  <span data-ttu-id="a0f92-132">Fyllið upp í reitina **Röðunarpöntun** og **Undirflokkar kostnaðar**.</span><span class="sxs-lookup"><span data-stu-id="a0f92-132">Fill in the **Sorting Order** and **Cost Subtype** fields.</span></span>  
6.  <span data-ttu-id="a0f92-133">Velja næstu tómu línu til að stofna nýjan kostnaðarstað og endurtaka síðan þrep 2 til 5.</span><span class="sxs-lookup"><span data-stu-id="a0f92-133">Choose the next empty line to create a new cost center, and then repeat steps 2 through 5.</span></span>  
7.  <span data-ttu-id="a0f92-134">Þegar búið er að setja upp alla kostnaðarstað skal velja aðgerðina **Draga inn kostnaðarstaði**.</span><span class="sxs-lookup"><span data-stu-id="a0f92-134">After you have set up all the cost centers, choose the **Indent Cost Centers** action.</span></span> <span data-ttu-id="a0f92-135">Velja hnappinn **Já**.</span><span class="sxs-lookup"><span data-stu-id="a0f92-135">Choose the **Yes** button.</span></span>  

> [!IMPORTANT]  
>  <span data-ttu-id="a0f92-136">Ef skilgreiningar voru færðar inn í **Samtölur** reitina fyrir **Loka-samtala** kostnaðarstaði áður en inndráttaraðgerðin var keyrð þarf að færa þær inn aftur.</span><span class="sxs-lookup"><span data-stu-id="a0f92-136">If you have entered definitions in the **Totaling** fields for **End-Total** cost centers before you run the indent function, then you must enter them again.</span></span> <span data-ttu-id="a0f92-137">Aðgerðin skrifar yfir gildin í öllum **Til-tala** reitum.</span><span class="sxs-lookup"><span data-stu-id="a0f92-137">The function overwrites the values in all **End-Total** fields.</span></span>  

## <a name="see-also"></a><span data-ttu-id="a0f92-138">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="a0f92-138">See Also</span></span>  
[<span data-ttu-id="a0f92-139">Kostnaðarreikningur</span><span class="sxs-lookup"><span data-stu-id="a0f92-139">Accounting for Costs</span></span>](finance-manage-cost-accounting.md)  
<span data-ttu-id="a0f92-140">[Uppsetning kostnaðarbókhalds](finance-set-up-cost-accounting.md) </span><span class="sxs-lookup"><span data-stu-id="a0f92-140">[Setting Up Cost Accounting](finance-set-up-cost-accounting.md) </span></span>  
<span data-ttu-id="a0f92-141">[Orðalisti í kostnaðarbókhaldi](finance-terminology-in-cost-accounting.md) </span><span class="sxs-lookup"><span data-stu-id="a0f92-141">[Terminology in Cost Accounting](finance-terminology-in-cost-accounting.md) </span></span>  
[<span data-ttu-id="a0f92-142">Um kostnaðarbókhald</span><span class="sxs-lookup"><span data-stu-id="a0f92-142">About Cost Accounting</span></span>](finance-about-cost-accounting.md)  
<span data-ttu-id="a0f92-143">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="a0f92-143">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
