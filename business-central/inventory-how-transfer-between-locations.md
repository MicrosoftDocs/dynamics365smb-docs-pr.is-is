---
title: Flytja vörur á milli birgðageymslna| Microsoft Docs
description: Lýsir hvernig á að flytja birgðir frá einum stað eða vörugeymslu til annars, annaðhvort með endurflokkunarfærslubók eða með flutningsfyrirmæli.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: move, warehouse
ms.date: 04/01/2020
ms.author: SorenGP
ms.openlocfilehash: c7d383fdaf75857013651944207616bdc7208e6d
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2020
ms.locfileid: "3181965"
---
# <a name="transfer-inventory-between-locations"></a><span data-ttu-id="b3dce-103">Flytja birgðir milli birgðageymslna</span><span class="sxs-lookup"><span data-stu-id="b3dce-103">Transfer Inventory Between Locations</span></span>
<span data-ttu-id="b3dce-104">Það er hægt að flytja birgðavörur milli tveggja staða með því að búa til flutningspantanir.</span><span class="sxs-lookup"><span data-stu-id="b3dce-104">You can transfer inventory items between locations by creating transfer orders.</span></span> <span data-ttu-id="b3dce-105">Einnig er hægt að nota vöruendurflokkunarbók.</span><span class="sxs-lookup"><span data-stu-id="b3dce-105">Alternatively, you can use the item reclassification journal.</span></span>

<span data-ttu-id="b3dce-106">Með flutningspöntun eru flutningar á útleið fluttir frá einum stað og tekið á móti flutningum á innleið á hinum staðnum.</span><span class="sxs-lookup"><span data-stu-id="b3dce-106">With transfer orders, you ship the outbound transfer from one location and receive the inbound transfer at the other location.</span></span> <span data-ttu-id="b3dce-107">Þannig er hægt að stjórna vöruhúsaaðgerðunum og meira öryggi er fyrir því að birgðamagn sé rétt uppfært.</span><span class="sxs-lookup"><span data-stu-id="b3dce-107">This allows you to manage the involved warehouse activities and provides more certainty that inventory quantities are updated correctly.</span></span>

<span data-ttu-id="b3dce-108">Með vöruendurflokkunarbók þarf einfaldlega að fylla inn í reitina **Staðsetningarkóði** og **Nýr staðsetningarkóði**.</span><span class="sxs-lookup"><span data-stu-id="b3dce-108">With the reclassification journal, you simply fill in the **Location Code** and the **New Location Code** fields.</span></span> <span data-ttu-id="b3dce-109">Þegar bókin er bókuð eru færslur birgðahöfuðbókar aðlagaðar þeirri staðsetningu sem um ræðir.</span><span class="sxs-lookup"><span data-stu-id="b3dce-109">When you post the journal, the item ledger entries are adjusted at the locations in question.</span></span> <span data-ttu-id="b3dce-110">Vöruhúsaaðgerðum er ekki stjórnað með þessari aðferð.</span><span class="sxs-lookup"><span data-stu-id="b3dce-110">With this method, warehouse activities are not managed.</span></span>

> [!NOTE]  
>   <span data-ttu-id="b3dce-111">Ef þú hefur hluti skráð í birgðum þínum án staðsetningar kóða, t.d. frá því að þú átt aðeins eitt vörugeymsla, þá getur þú ekki flutt þau vörur með því að nota flutningsfyrirmæli.</span><span class="sxs-lookup"><span data-stu-id="b3dce-111">If you have items recorded in your inventory without a location code, for example from a time when you only had one warehouse, then you cannot transfer those items using transfer orders.</span></span> <span data-ttu-id="b3dce-112">Þess í stað verður þú að nota endurflokkunarskýrsluna til að endurflokka atriði úr autt staðarnúmeri í raunverulegan staðarnúmer.</span><span class="sxs-lookup"><span data-stu-id="b3dce-112">Instead, you must use the reclassification journal to reclassify the items from a blank location code to an actual location code.</span></span>  <span data-ttu-id="b3dce-113">Nánari upplýsingar er að finna í skrefi 3 í [Að flytja vörur með vöruendurflokkunarbók](inventory-how-transfer-between-locations.md#to-transfer-items-with-the-item-reclassification-journal).</span><span class="sxs-lookup"><span data-stu-id="b3dce-113">For more information, see step 3 in [To transfer items with the item reclassification journal](inventory-how-transfer-between-locations.md#to-transfer-items-with-the-item-reclassification-journal).</span></span>

<span data-ttu-id="b3dce-114">Staðsetning og flutningsleiðir þurfa að vera uppsett til að flytja vörur.</span><span class="sxs-lookup"><span data-stu-id="b3dce-114">To transfer items, locations and transfer routes must be set up.</span></span> <span data-ttu-id="b3dce-115">Nánari upplýsingar er að finna í [Setja upp birgðageymslur](inventory-how-setup-locations.md).</span><span class="sxs-lookup"><span data-stu-id="b3dce-115">For more information, see [Set Up Locations](inventory-how-setup-locations.md).</span></span>

## <a name="to-transfer-items-with-a-transfer-order"></a><span data-ttu-id="b3dce-116">Vörur fluttar með flutningspöntun</span><span class="sxs-lookup"><span data-stu-id="b3dce-116">To transfer items with a transfer order</span></span>
1. <span data-ttu-id="b3dce-117">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Flutningspantanir** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="b3dce-117">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Transfer orders**, and then choose the related link.</span></span>
2. <span data-ttu-id="b3dce-118">Fyllt er út í reiti eftir því sem á við í haus síðunnar **Millifærslupöntun**.</span><span class="sxs-lookup"><span data-stu-id="b3dce-118">On the header of the **Transfer Order** page, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
    >   <span data-ttu-id="b3dce-119">Ef búið er að fylla út reitina **Millifærslukóði**, **Flutningsaðilakóði** og **Flutningsþjónusta** á síðunni **Lýsing millifærsluleiðar** þegar flutningsleið var sett upp, fyllir kerfið sjálfkrafa út samsvarandi reiti á millifærslupöntuninni.</span><span class="sxs-lookup"><span data-stu-id="b3dce-119">If you have filled in the **In-Transit Code**, **Shipping Agent Code**, and **Shipping Agent Service** fields on the **Trans. Route Spec.** page when you set up the transfer route, then the corresponding fields on the transfer order are filled in automatically.</span></span>

    <span data-ttu-id="b3dce-120">Þegar fyllt er út í reitinn **Flutningsþjónusta** reiknar kerfið út móttökudagsetningu fyrir flutt-til birgðageymslu með því að bæta flutningstíma flutningsþjónustunnar við afhendingardagsetninguna.</span><span class="sxs-lookup"><span data-stu-id="b3dce-120">When you fill in the **Shipping Agent Service** field, the receipt date at the transfer-to location is calculated by adding the shipping time of the shipping agent service to the shipment date.</span></span>

3. <span data-ttu-id="b3dce-121">Til að fylla út í línurnar skal annaðhvort færa þær inn handvirkt eða velja einn eftirfarandi valkosta á undir aðgerðinni **Aðgerðir**:</span><span class="sxs-lookup"><span data-stu-id="b3dce-121">To fill in the lines, either enter them manually or choose one of the following options on the under the **Functions** action:</span></span>
    - <span data-ttu-id="b3dce-122">Veldu **Sækja innihald hólfs** aðgerðina til að velja fyrirliggjandi vörur úr tilteknu hólfi á staðsetningunni.</span><span class="sxs-lookup"><span data-stu-id="b3dce-122">Choose the **Get Bin Content** action to select existing items from a specific bin at the location.</span></span>
    - <span data-ttu-id="b3dce-123">Veldu **Sækja móttökulínur** til að velja vörur sem eru nýkomnar á sendist-frá staðsetningu.</span><span class="sxs-lookup"><span data-stu-id="b3dce-123">Choose the **Get Receipt Lines** to select items that have just arrived at the transfer-from location.</span></span>   

    <span data-ttu-id="b3dce-124">Sem starfsmaður vörugeymslu við flutninginn frá staðsetninginni skaltu halda áfram að senda vörurnar.</span><span class="sxs-lookup"><span data-stu-id="b3dce-124">As a warehouse worker at the transfer-from location, proceed to ship the items.</span></span>
4. <span data-ttu-id="b3dce-125">Veldu aðgerðina **Bóka** veldu **Senda** valkostinn og veldu síðan **Í lagi** hnappinn.</span><span class="sxs-lookup"><span data-stu-id="b3dce-125">Choose the **Post** action, choose the **Ship** option, and then choose the **OK** button.</span></span>

    <span data-ttu-id="b3dce-126">Atriðin eru nú í flutningi milli tilgreindra staða, í samræmi við tilgreint flutningsleið.</span><span class="sxs-lookup"><span data-stu-id="b3dce-126">The items are now in transit between the specified locations, according to the specifies transfer route.</span></span>

    <span data-ttu-id="b3dce-127">Sem starfsmaður vörugeymslu við flutninginn frá staðsetninginni skaltu halda áfram að fá vörurnar.</span><span class="sxs-lookup"><span data-stu-id="b3dce-127">As a warehouse worker at the transfer-from location, proceed to receive the items.</span></span> <span data-ttu-id="b3dce-128">Flutningspöntunarlínurnar eru þær sömu og við sendingu og er ekki hægt að breyta þeim.</span><span class="sxs-lookup"><span data-stu-id="b3dce-128">The transfer order lines are the same as when shipped and cannot be edited.</span></span>
5. <span data-ttu-id="b3dce-129">Veldu aðgerðina **Bóka**, veldu **Móttaka** valkostinn og veldu síðan **Í lagi** hnappinn.</span><span class="sxs-lookup"><span data-stu-id="b3dce-129">Choose the **Post** action, choose the **Receive** option, and then choose the **OK** button.</span></span>

## <a name="to-transfer-items-with-the-item-reclassification-journal"></a><span data-ttu-id="b3dce-130">Til að flytja vörur með vöruendurflokkunarbók</span><span class="sxs-lookup"><span data-stu-id="b3dce-130">To transfer items with the item reclassification journal</span></span>
1. <span data-ttu-id="b3dce-131">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Vöruendurflokkunarbók** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="b3dce-131">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Item Reclass. Journals**, and then choose the related link.</span></span>
2. <span data-ttu-id="b3dce-132">Á síðunni **Birgðaendurflokkunarbók** skal fylla út reitina eins og þörf krefur.</span><span class="sxs-lookup"><span data-stu-id="b3dce-132">On the **Item Reclass. Journal** page, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="b3dce-133">Í reitnum **Kóði birgðageymslu** er færð inn birgðageymslan þar sem vörurnar eru nú geymdar.</span><span class="sxs-lookup"><span data-stu-id="b3dce-133">In the **Location Code** field, enter the location where the items are currently stored.</span></span>

    > [!NOTE]  
    >   <span data-ttu-id="b3dce-134">Til að flytja hluti sem ekki hafa staðsetningarkóða skal skilja reitinn **Staðsetningarkóða** eftir auðan.</span><span class="sxs-lookup"><span data-stu-id="b3dce-134">To transfer items that have no location code, leave the **Location Code** field blank.</span></span>
4. <span data-ttu-id="b3dce-135">Í reitnum **Nýr staðsetningarkóði**, sláðu inn staðinn sem þú vilt flytja hlutina í.</span><span class="sxs-lookup"><span data-stu-id="b3dce-135">In the **New Location Code** field, enter the location that you want to transfer the items to.</span></span>
5. <span data-ttu-id="b3dce-136">Valið er **Bóka** aðgerðin.</span><span class="sxs-lookup"><span data-stu-id="b3dce-136">Choose the **Post** action.</span></span>

## <a name="see-also"></a><span data-ttu-id="b3dce-137">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="b3dce-137">See Also</span></span>
[<span data-ttu-id="b3dce-138">Stjórna birgðum</span><span class="sxs-lookup"><span data-stu-id="b3dce-138">Manage Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="b3dce-139">Uppsetning birgðageymsla</span><span class="sxs-lookup"><span data-stu-id="b3dce-139">Set Up Locations</span></span>](inventory-how-setup-locations.md)  
<span data-ttu-id="b3dce-140">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="b3dce-140">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="b3dce-141">Breyta því hvaða eiginleikar eru sýndir</span><span class="sxs-lookup"><span data-stu-id="b3dce-141">Change Which Features are Displayed</span></span>](ui-experiences.md)  
[<span data-ttu-id="b3dce-142">Almenn viðskiptavirkni</span><span class="sxs-lookup"><span data-stu-id="b3dce-142">General Business Functionality</span></span>](ui-across-business-areas.md)
