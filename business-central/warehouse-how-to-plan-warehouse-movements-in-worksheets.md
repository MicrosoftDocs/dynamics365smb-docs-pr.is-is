---
title: 'Hvernig á að áætla vöruhúsahreyfingar á vinnublöðum | Microsoft '
description: Hreyfingar eru áætlaðar á vinnublaðinu með hólfaáfyllingu eða með handvirkri áætlun á línum sem á að stofna sem hreyfingaleiðbeiningar.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 1ae0386c4fc2e3ac216d4228c94e7447a808cf50
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/17/2020
ms.locfileid: "4756118"
---
# <a name="plan-warehouse-movements-in-worksheets"></a><span data-ttu-id="60935-103">Áætla vöruhúsahreyfingar á vinnublöðum</span><span class="sxs-lookup"><span data-stu-id="60935-103">Plan Warehouse Movements in Worksheets</span></span>
<span data-ttu-id="60935-104">Hreyfingar eru áætlaðar á vinnublaðinu með hólfaáfyllingu eða með handvirkri áætlun á línum sem á að stofna sem hreyfingaleiðbeiningar.</span><span class="sxs-lookup"><span data-stu-id="60935-104">Plan movements in the worksheet using a bin replenishment function or manually planning the lines that you want to create as movement instructions.</span></span>  

## <a name="to-calculate-a-replenishment-movement"></a><span data-ttu-id="60935-105">Áfyllingarhreyfingar reiknaðar:</span><span class="sxs-lookup"><span data-stu-id="60935-105">To calculate a replenishment movement</span></span>  
<span data-ttu-id="60935-106">Jafnframt því sem vörur eru sendar viðskiptamönnum úr vöruhúsi, fækkar vörunum í hólfunum með hæstu hólfaflokkunina.</span><span class="sxs-lookup"><span data-stu-id="60935-106">As the warehouse ships items out to customers, the bins with the highest bin rankings contain fewer and fewer items.</span></span> <span data-ttu-id="60935-107">Til að fylla á þessi hólf með vörum úr öðrum hólfum er keyrð aðgerðin **Reikna út áfyllingu hólfs** á **Hreyfing Vinnublað** síðunni</span><span class="sxs-lookup"><span data-stu-id="60935-107">To fill up these high-ranking pick bins with items from other bins, run the **Calculate Bin Replenishment** function on the **Movement Worksheet** page</span></span>

1.  <span data-ttu-id="60935-108">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Hreyfingavinnublað** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="60935-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Movement Worksheet**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="60935-109">Velja skal aðgerðina **Reikna áfyllingu hólfs**.</span><span class="sxs-lookup"><span data-stu-id="60935-109">Choose the **Calculate Bin Replenishment** action.</span></span>  

    [!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="60935-110">stofnar línur sem gefa nákvæmlega til kynna hvernig færa á vörur úr lægra flokkuðum hólfum í hærra flokkuð.</span><span class="sxs-lookup"><span data-stu-id="60935-110">creates lines that indicate precisely how you should move items from the low-ranking bins to the higher-ranking bins.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="60935-111">Stungið er upp á hreyfingu í samræmi við FEFO aðgerðin **Stofna hreyfingu** er virkjuð ef eftirfarandi skilyrðum fyrir vöru er fullnægt:</span><span class="sxs-lookup"><span data-stu-id="60935-111">A movement is suggested according to FEFO when you activate the **Create Movement** function if the following conditions are met for an item:</span></span>  
    >   
    >  -   <span data-ttu-id="60935-112">Varan er fyrningadagsett.</span><span class="sxs-lookup"><span data-stu-id="60935-112">The item has an expiration date.</span></span>  
    > -   <span data-ttu-id="60935-113">Gátreiturinn **Tína eftir FEFO** í birgðageymsluspjaldinu er valinn.</span><span class="sxs-lookup"><span data-stu-id="60935-113">The **Pick According to FEFO** check box on the location card is selected.</span></span>  
    > -   <span data-ttu-id="60935-114">Gátreiturinn **Hólf áskilið** á birgðageymsluspjaldinu er valið.</span><span class="sxs-lookup"><span data-stu-id="60935-114">The **Bin Mandatory** check box on the location card is selected.</span></span>  
    > -   <span data-ttu-id="60935-115">Reitirnir **Frá svæði** og **Frá hólf** eru auðir.</span><span class="sxs-lookup"><span data-stu-id="60935-115">The **From Zone** and **From Bin** fields are blank.</span></span>  

    <span data-ttu-id="60935-116">Frekari upplýsingar eru í [Tínsla skv. FEFO](warehouse-picking-by-fefo.md).</span><span class="sxs-lookup"><span data-stu-id="60935-116">For more information, see [Picking by FEFO](warehouse-picking-by-fefo.md).</span></span>  

3.  <span data-ttu-id="60935-117">Farið er yfir línurnar og þeim breitt eftir þörfum eða eytt ef ekki er tími til að framkvæma þær allar.</span><span class="sxs-lookup"><span data-stu-id="60935-117">Look through the lines and change them if necessary, or delete some of them if there is not enough time to perform them all.</span></span>  
4.  <span data-ttu-id="60935-118">Velja aðgerðina **Stofna hreyfingu** til að búa til vöruhúsaleiðbeiningar fyrir aðgerðir starfsmanna vöruhúss.</span><span class="sxs-lookup"><span data-stu-id="60935-118">Choose the **Create Movement** action to make a warehouse instruction for action by warehouse employees.</span></span>  

## <a name="to-move-the-entire-contents-of-one-or-more-bins-by-using-the-get-bin-content-function"></a><span data-ttu-id="60935-119">Með aðgerðinni sækja innihald hólfs er hægt að sækja allt sem er í einu eða fleiri hólfum:</span><span class="sxs-lookup"><span data-stu-id="60935-119">To move the entire contents of one or more bins by using the Get Bin Content function</span></span>  
<span data-ttu-id="60935-120">Einnig er hægt að nota vinnublað hreyfinga til að áætla aðrar hreyfingar á birgðum innan vöruhússins.</span><span class="sxs-lookup"><span data-stu-id="60935-120">You can also use the movement worksheet to plan other movement of inventory within the warehouse.</span></span> <span data-ttu-id="60935-121">Þegar setja á vörur í hólf fyrir gæðaeftirlit, til dæmis, er hægt að nota vinnublað hreyfinga til að áætla aðgerðina og stofna síðan hreyfingu til að útbúa fyrirmæli fyrir starfsmann.</span><span class="sxs-lookup"><span data-stu-id="60935-121">For example, when you want to place items in a bin for quality control, you can use the movement worksheet to plan this action and then create a movement to make instructions for an employee.</span></span>  

1.  <span data-ttu-id="60935-122">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Hreyfingavinnublað** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="60935-122">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Movement Worksheet**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="60935-123">Valið er **Sækja innihald hólfs** aðgerð.</span><span class="sxs-lookup"><span data-stu-id="60935-123">Choose the **Get Bin Content** action.</span></span> <span data-ttu-id="60935-124">Beiðnisíðan er notuð til að afmarka það hvaða hólf og vörur skuli birtast í hreyfingavinnublaðslínunum.</span><span class="sxs-lookup"><span data-stu-id="60935-124">Use the request page to filter which bins and items you want to appear on the movement worksheet lines.</span></span>  
3.  <span data-ttu-id="60935-125">Reitirnir á keyrslusíðunni eru fylltir út.</span><span class="sxs-lookup"><span data-stu-id="60935-125">Fill in the relevant fields in the batch job request page.</span></span> <span data-ttu-id="60935-126">Eigi t.d. að skoða innihald allra hólfa á vissu svæði í birgðageymslunni er reiturinn **Svæðiskóti** .</span><span class="sxs-lookup"><span data-stu-id="60935-126">For example, if you want to see the bin content of all the bins in a certain zone at the location, fill in the **Zone Code** field.</span></span> <span data-ttu-id="60935-127">Eigi að sækja línur fyrir hvert hólf sem tiltekin vara er í er reiturinn **Vörunr.** fylltur út.</span><span class="sxs-lookup"><span data-stu-id="60935-127">If you want to retrieve lines for each bin that contains a particular item, fill in the **Item No.** field.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="60935-128">Ekki er hægt að færa vörur handvirkt inn og út úr hólfi af gerðinni RECEIVE því vörur sem eru í hólfi af þeirri gerð verður að skrá sem frágengnar áður en þær verða hluti af tiltækum birgðum.</span><span class="sxs-lookup"><span data-stu-id="60935-128">You cannot manually move items in or out of a bin of bin type RECEIVE, because items that are in a RECEIVE-type bin must be registered as being put away before they are part of available inventory.</span></span>  

4.  <span data-ttu-id="60935-129">Ef sækja á margar línur skal velja **Raða** til að velja röðunaraðferð til að ákveða í hvaða röð línurnar birtast á vinnublaðinu og síðan skal velja hnappinn **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="60935-129">If you are retrieving many lines, choose **Sort** to select a sorting method to determine the order the lines will appear in the worksheet, and then choose the **OK** button.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="60935-130">Hreyfingalínur eru sóttar í samræmi við FEFO aðgerðin **Sækja hólfaefni** er virkjuð ef eftirfarandi skilyrðum fyrir vöru er fullnægt:</span><span class="sxs-lookup"><span data-stu-id="60935-130">Movement lines are retrieved according to FEFO when you activate the **Get Bin Content** function if the following conditions are met for an item:</span></span>  
    >   
    >  -   <span data-ttu-id="60935-131">Varan er fyrningadagsett.</span><span class="sxs-lookup"><span data-stu-id="60935-131">The item has an expiration date.</span></span>  
    > -   <span data-ttu-id="60935-132">Gátreiturinn **Tína eftir FEFO** í birgðageymsluspjaldinu er valinn.</span><span class="sxs-lookup"><span data-stu-id="60935-132">The **Pick According to FEFO** check box on the location card is selected.</span></span>  
    > -   <span data-ttu-id="60935-133">Gátreiturinn **Hólf áskilið** á birgðageymsluspjaldinu er valið.</span><span class="sxs-lookup"><span data-stu-id="60935-133">The **Bin Mandatory** check box on the location card is selected.</span></span>  
    > -   <span data-ttu-id="60935-134">Reitirnir **Frá svæði** og **Frá hólf** eru auðir.</span><span class="sxs-lookup"><span data-stu-id="60935-134">The **From Zone** and **From Bin** fields are blank.</span></span>  

5.  <span data-ttu-id="60935-135">Reitir í einhverjum línunum sem voru sóttar eru fylltir út til að breyta eins og þarf.</span><span class="sxs-lookup"><span data-stu-id="60935-135">Complete some of the retrieved lines to reflect the changes you want to make.</span></span> <span data-ttu-id="60935-136">Fyrir hverja vöru sem á að færa þarf að fylla út reitina **Vörunr.**, **Kóti frá-hólfs**, **Kóti til-hólfs** og **Magn**.</span><span class="sxs-lookup"><span data-stu-id="60935-136">For each item that you want to move, you must fill in the **Item No.**, **From Bin Code**, **To Bin Code**, and **Quantity** fields.</span></span>  
6.  <span data-ttu-id="60935-137">Línum sem ekkert er fært í skal eytt.</span><span class="sxs-lookup"><span data-stu-id="60935-137">Delete the incomplete lines that you used for information.</span></span>  
7.  <span data-ttu-id="60935-138">Þegar línur hreyfingavinnublaðsins eru orðnar eins og þær eiga að vera skal velja aðgerðina **Stofna hreyfingu** til að útbúa leiðbeiningarnar fyrir starfsmanninn.</span><span class="sxs-lookup"><span data-stu-id="60935-138">Once the movement worksheet lines accurately reflect how the movement action should be carried out by the warehouse employee, choose the **Create Movement** action to create the instructions for the employee.</span></span>  

## <a name="see-also"></a><span data-ttu-id="60935-139">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="60935-139">See Also</span></span>  
[<span data-ttu-id="60935-140">Vöruhúsastjórnun</span><span class="sxs-lookup"><span data-stu-id="60935-140">Warehouse Management</span></span>](warehouse-manage-warehouse.md)  
[<span data-ttu-id="60935-141">Birgðir</span><span class="sxs-lookup"><span data-stu-id="60935-141">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="60935-142">[Vöruhúsastjórnun sett upp](warehouse-setup-warehouse.md)   </span><span class="sxs-lookup"><span data-stu-id="60935-142">[Setting Up Warehouse Management](warehouse-setup-warehouse.md)   </span></span>  
<span data-ttu-id="60935-143">[Samsetningardeild](assembly-assemble-items.md)  </span><span class="sxs-lookup"><span data-stu-id="60935-143">[Assembly Management](assembly-assemble-items.md)  </span></span>  
[<span data-ttu-id="60935-144">Hönnunarupplýsingar vöruhúsakerfi</span><span class="sxs-lookup"><span data-stu-id="60935-144">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="60935-145">[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="60935-145">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>
