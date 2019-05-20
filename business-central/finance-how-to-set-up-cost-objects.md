---
title: Hvernig á að setja upp kostnaðarhluti | Microsoft Docs
description: Lærið hvernig á að setja upp kostnaðarhluti, sem eru svipaðir víddum fyrir fjárhaginn.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
redirect_url: finance-set-up-cost-accounting
ms.openlocfilehash: 725ad9ed12dd32dc1cc3257c266efa274ea964a0
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/29/2019
ms.locfileid: "1239634"
---
# <a name="set-up-cost-objects"></a><span data-ttu-id="c2627-103">Uppsetning kostnaðarhluta</span><span class="sxs-lookup"><span data-stu-id="c2627-103">Set Up Cost Objects</span></span>
<span data-ttu-id="c2627-104">Kostnaðurhlutir eru verkefni, afurðair eða þjónustur fyrirtækis.</span><span class="sxs-lookup"><span data-stu-id="c2627-104">Cost objects are projects, products, or services of a company.</span></span> <span data-ttu-id="c2627-105">Myndrit kostnaðarhluta er svipað og víddarupplýsingar fyrir fjárhag.</span><span class="sxs-lookup"><span data-stu-id="c2627-105">The chart of cost objects is similar to the dimension information for the general ledger.</span></span> <span data-ttu-id="c2627-106">Hægt er að setja upp myndritið yfir kostnaðaríhluti á eftirfarandi hátt:</span><span class="sxs-lookup"><span data-stu-id="c2627-106">You can set up the chart of cost objects in the following ways:</span></span>  

* <span data-ttu-id="c2627-107">Flytja víddargildi í fjárhag í myndrit yfir í kostnaðarhluti.</span><span class="sxs-lookup"><span data-stu-id="c2627-107">Transfer dimension values in the general ledger to the chart of cost objects.</span></span> <span data-ttu-id="c2627-108">Hægt er að gera allar nauðsynlegar leiðréttingar eftir flutninginn.</span><span class="sxs-lookup"><span data-stu-id="c2627-108">You can make any necessary adjustments after the transfer.</span></span>  
* <span data-ttu-id="c2627-109">Stofna nýjan kostnaðarhlut sem er óháður fjárhagnum eða bæta nýjum kostnaðarhlut við kostnaðarhlut sem fyrir er.</span><span class="sxs-lookup"><span data-stu-id="c2627-109">Create a new chart of cost object that is independent of the general ledger or add a new cost object to an existing chart of cost objects.</span></span> <span data-ttu-id="c2627-110">Stofna þarf hvern kostnaðaríhlut sérstaklega.</span><span class="sxs-lookup"><span data-stu-id="c2627-110">You must create each cost object individually.</span></span>  

## <a name="to-transfer-dimension-values-from-the-general-ledger-to-the-chart-of-cost-objects"></a><span data-ttu-id="c2627-111">Til að flytja víddargildi úr fjárhag í kostnaðarhluti</span><span class="sxs-lookup"><span data-stu-id="c2627-111">To transfer dimension values from the general ledger to the chart of cost objects</span></span>  
1.  <span data-ttu-id="c2627-112">Stilla vídd sem á að vera kostnaðarliðarvíddin á síðunni **Uppfæra CA víddir**.</span><span class="sxs-lookup"><span data-stu-id="c2627-112">Set a dimension to be the cost object dimension on the **Update CA Dimensions** page.</span></span> <span data-ttu-id="c2627-113">Aðeins gildi úr þessari vídd er flutt.</span><span class="sxs-lookup"><span data-stu-id="c2627-113">Only the values from this dimension are transferred.</span></span>  
2.  <span data-ttu-id="c2627-114">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Myndrit yfir kostnaðarhluti** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="c2627-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Chart of Cost Objects**, and then choose the related link.</span></span>  
3.  <span data-ttu-id="c2627-115">Veljið aðgerðina **Sækja kostnaðarhluti úr vídd** til að flytja víddargildi í myndriti kostnaðarhlutanna.</span><span class="sxs-lookup"><span data-stu-id="c2627-115">Choose the **Get Cost Objects from Dimension** action to transfer dimension values to the chart of cost objects.</span></span> <span data-ttu-id="c2627-116">Aðgerðin flytur víddargildin sem skilgreind voru í skrefi 1.</span><span class="sxs-lookup"><span data-stu-id="c2627-116">The function transfers the dimension values that you defined in step 1.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="c2627-117">Hægt er að setja reitinn **Stilla kostnaðarhlutavíddir** upp þannig að hann skilgreini einstefnusamstillingu á víddargildum frá fjárhag yfir í myndrit yfir kostnaðarhluti.</span><span class="sxs-lookup"><span data-stu-id="c2627-117">You can set up the **Align Cost Object Dimension**  field to define a one-way synchronization of dimension values from the general ledger to the chart of cost objects.</span></span> <span data-ttu-id="c2627-118">Ekki er hægt að skilreina samstillingu myndrits yfir kostnaðarhluti við víddargildi úr fjárhag.</span><span class="sxs-lookup"><span data-stu-id="c2627-118">You cannot define a synchronization of the chart of cost objects to dimension values from the general ledger.</span></span>  

<span data-ttu-id="c2627-119">Myndrit kostnaðarhluta inniheldur nú öll tilgreind víddargildi úr fjárhag og inniheldur titla og samtölur.</span><span class="sxs-lookup"><span data-stu-id="c2627-119">The chart of cost objects now contains all specified dimension values from the general ledger and includes titles and subtotals.</span></span>  

## <a name="to-create-new-cost-objects-in-the-chart-of-cost-objects-page"></a><span data-ttu-id="c2627-120">Til að stofna nýja kostnaðarhluti á síðunni myndrit fyrir kostnaðarliði</span><span class="sxs-lookup"><span data-stu-id="c2627-120">To create new cost objects in the Chart of Cost Objects page</span></span>  
<span data-ttu-id="c2627-121">Hægt er að setja upp og vinna með kostnaðarliði í **Kostnaðarliðaspjald** spjaldinu eða á síðunni **Myndrit fyrir kostnaðarliði**.</span><span class="sxs-lookup"><span data-stu-id="c2627-121">You can set up and maintain cost objects in either the **Cost Object Card** card or on the **Chart of Cost Objects** page.</span></span> <span data-ttu-id="c2627-122">Í þessu ferli eru settir upp kostnaðarliðir á síðunni **Myndrit fyrir kostnaðarliði**.</span><span class="sxs-lookup"><span data-stu-id="c2627-122">In this procedure, you set up cost objects on the **Chart of Cost Objects** page.</span></span>  

1.  <span data-ttu-id="c2627-123">Opnaðu síðuna **Myndrit yfir kostnaðarliði** í breytingarstillingu.</span><span class="sxs-lookup"><span data-stu-id="c2627-123">Open the **Chart of Cost Objects** page in edit mode.</span></span>  
2.  <span data-ttu-id="c2627-124">Í reitinn **Kóði** er færður inn kóti kostnaðarliða.</span><span class="sxs-lookup"><span data-stu-id="c2627-124">In the **Code** field, enter the cost object code.</span></span> <span data-ttu-id="c2627-125">Allir kostnaðarhlutir verða að hafa kóta.</span><span class="sxs-lookup"><span data-stu-id="c2627-125">All cost objects must have a code.</span></span>  
3.  <span data-ttu-id="c2627-126">Í reitinn **Heiti** er færður inn heiti kostnaðarliða.</span><span class="sxs-lookup"><span data-stu-id="c2627-126">In the **Name** field, enter the cost object name.</span></span>  
4.  <span data-ttu-id="c2627-127">Velja fellilistaörina í reitnum **Línugerð** til að tilgreina tilgang kostnaðarhlutarins.</span><span class="sxs-lookup"><span data-stu-id="c2627-127">Choose the drop-down arrow in the **Line Type** field to specify the purpose of the cost object.</span></span>  

    * <span data-ttu-id="c2627-128">Fyrir kostnaðarhluti af línutegundinni **Samtals** skal fylla út reitinn **Samtals frá/til**.</span><span class="sxs-lookup"><span data-stu-id="c2627-128">For cost objects of the **Total** line type, fill in the **Total From/To** field.</span></span> <span data-ttu-id="c2627-129">Nota skal virkinn **eða**, sem er lóðrétt lína (**&#124;**) til að stilla svið kostnaðarhluta.</span><span class="sxs-lookup"><span data-stu-id="c2627-129">Use the **or** operator, which is a vertical line (**&#124;**), to set ranges of cost objects.</span></span>  
    * <span data-ttu-id="c2627-130">Fyrir kostnaðarhluti af línutegundinni **Til-tala** er sjálfkrafa fyllt út í reitinn þegar inndráttarvirknin er notuð.</span><span class="sxs-lookup"><span data-stu-id="c2627-130">For cost objects of the **End-Total** line type, this field is filled in automatically when you use  the indent function.</span></span>  
5.  <span data-ttu-id="c2627-131">Fyllið upp í reitinn **Röðunarpöntun**.</span><span class="sxs-lookup"><span data-stu-id="c2627-131">Fill in the **Sorting Order** field.</span></span>  
6.  <span data-ttu-id="c2627-132">Velja næstu tómu línu til að stofna nýjan kostnaðarhlut og endurtaka síðan þrep 2 til 5.</span><span class="sxs-lookup"><span data-stu-id="c2627-132">Chose the next empty line to create a new cost object, and then repeat steps 2 through 5.</span></span>  
7.  <span data-ttu-id="c2627-133">Þegar búið er að setja upp alla kostnaðarhlutina, skal velja aðgerðina **Draga inn kostnaðarhluti**.</span><span class="sxs-lookup"><span data-stu-id="c2627-133">After you have set up all the cost objects, choose the **Indent Cost Objects** action.</span></span> <span data-ttu-id="c2627-134">Velja hnappinn **Já**.</span><span class="sxs-lookup"><span data-stu-id="c2627-134">Choose the **Yes** button.</span></span>  

> [!IMPORTANT]  
>  <span data-ttu-id="c2627-135">Ef skilgreiningar voru færðar inn í reitina **Samtals frá/til** fyrir **Loka-upphæð** kostnaðarhluti áður en inndráttaraðgerðin var keyrð þarf að færa þær inn aftur.</span><span class="sxs-lookup"><span data-stu-id="c2627-135">If you have entered definitions in the **Total From/To** fields for **End-Total** cost objects before you run the indent function, then you must enter them again.</span></span> <span data-ttu-id="c2627-136">Aðgerðin skrifar yfir gildin í öllum **Til - tala** reitum.</span><span class="sxs-lookup"><span data-stu-id="c2627-136">The function overwrites the values in all **End-Total** fields.</span></span>  

## <a name="see-also"></a><span data-ttu-id="c2627-137">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="c2627-137">See Also</span></span>  
[<span data-ttu-id="c2627-138">Kostnaðarreikningur</span><span class="sxs-lookup"><span data-stu-id="c2627-138">Accounting for Costs</span></span>](finance-manage-cost-accounting.md)  
<span data-ttu-id="c2627-139">[Skilgreining kostnaðarstaði og kostnaðarhluti fyrir bókhaldslykil](finance-defining-cost-centers-and-cost-objects-for-chart-of-accounts.md) </span><span class="sxs-lookup"><span data-stu-id="c2627-139">[Defining Cost Centers and Cost Objects for Chart of Accounts](finance-defining-cost-centers-and-cost-objects-for-chart-of-accounts.md) </span></span>  
<span data-ttu-id="c2627-140">[Stöður milli kostnaðartegundar, kostnaðarstaðar og kostnaðarliðar](finance-balances-between-cost-type-cost-center-and-cost-object.md) </span><span class="sxs-lookup"><span data-stu-id="c2627-140">[Balances Between Cost Type, Cost Center, and Cost Object](finance-balances-between-cost-type-cost-center-and-cost-object.md) </span></span>  
<span data-ttu-id="c2627-141">[Uppsetning kostnaðarbókhalds](finance-set-up-cost-accounting.md) </span><span class="sxs-lookup"><span data-stu-id="c2627-141">[Setting Up Cost Accounting](finance-set-up-cost-accounting.md) </span></span>  
<span data-ttu-id="c2627-142">[Orðalisti í kostnaðarbókhaldi](finance-terminology-in-cost-accounting.md) </span><span class="sxs-lookup"><span data-stu-id="c2627-142">[Terminology in Cost Accounting](finance-terminology-in-cost-accounting.md) </span></span>  
[<span data-ttu-id="c2627-143">Um kostnaðarbókhald</span><span class="sxs-lookup"><span data-stu-id="c2627-143">About Cost Accounting</span></span>](finance-about-cost-accounting.md)  
<span data-ttu-id="c2627-144">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="c2627-144">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
