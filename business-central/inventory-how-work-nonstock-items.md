---
title: "Stofna og vinna með Utanbirgðavörur| Microsoft Docs"
description: "Lýsir því hvernig viðskipti fara fram með vörur sem ekki hægt að geyma í birgðum eða sem ekki er viðhaldið í birgðum."
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: non-inventoriable
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: cdfca33d0d9ea4b66b8e1c15cd66eaf9fa79b819
ms.contentlocale: is-is
ms.lasthandoff: 03/22/2018

---
# <a name="work-with-nonstock-items"></a><span data-ttu-id="4f8e3-103">Vinna með Utanbirgðavörur</span><span class="sxs-lookup"><span data-stu-id="4f8e3-103">Work with Nonstock Items</span></span>
<span data-ttu-id="4f8e3-104">Þú getur boðið viðskiptamaður þínum tilteknar vörur til þeim til hæginda, vörur sem þú vilt ekki geyma í birgðum fyrr en þú byrjar að selja þær.</span><span class="sxs-lookup"><span data-stu-id="4f8e3-104">You can offer certain items to your customers for their convenience, which you do not want to maintain in inventory until you start selling them.</span></span> <span data-ttu-id="4f8e3-105">Þegar á að byrja að viðhalda slíkum vörum í birgðum, er hægt að breyta þeim í venjulegur birgðaspjöld á tvo vegu.</span><span class="sxs-lookup"><span data-stu-id="4f8e3-105">When you want to start maintaining such items in inventory, you can convert them to normal item cards in two ways.</span></span>

* <span data-ttu-id="4f8e3-106">Úr utanbirgðaspjaldi skal stofna nýtt birgðaspjald á grundvelli sniðmáts.</span><span class="sxs-lookup"><span data-stu-id="4f8e3-106">From a nonstock item card, create a new item card based on a template.</span></span>
* <span data-ttu-id="4f8e3-107">Frá sölustaðarlínu af gerðinni **Vara** með tómum \**Nr.* reit, veldu ekki atriði í vörulista.</span><span class="sxs-lookup"><span data-stu-id="4f8e3-107">From a sales order line of type **Item** with an empty \**No* field, select a nonstock item.</span></span> <span data-ttu-id="4f8e3-108">Birgðaspjald er sjálfkrafa stofnað fyrir þessa utanbirgðavöru.</span><span class="sxs-lookup"><span data-stu-id="4f8e3-108">An item card is automatically created for the nonstock item.</span></span>

> [!NOTE]  
>   <span data-ttu-id="4f8e3-109">Ekki hægt er að velja utanbirgðavöru úr glugganum **Sölureikningur**.</span><span class="sxs-lookup"><span data-stu-id="4f8e3-109">You cannot select a nonstock item from the **Sales Invoice** window.</span></span> <span data-ttu-id="4f8e3-110">Hægt er að velja utanbirgðavöru á úr **Sölutilboð** glugganum, en utanbirgðavöru verður ekki umbreytt í venjulega vöru þegar þú notar **Búa til Pöntun** aðgerð.</span><span class="sxs-lookup"><span data-stu-id="4f8e3-110">You can select a nonstock item from the **Sales Quote** window, but the nonstock item will not be converted to a normal item when you use the **Make Order** function.</span></span>

<span data-ttu-id="4f8e3-111">Utanbirgðavara hefur yfirleitt vörunúmer þess lánardrottins sem sér um að veita hana.</span><span class="sxs-lookup"><span data-stu-id="4f8e3-111">A nonstock item typically has the item number of the vendor who supplies it.</span></span> <span data-ttu-id="4f8e3-112">Til að virkja umbreytingu utanbirgðaspjalds í venjulegur birgðaspjald, þarf fyrst að setja upp hvernig númeraröð lánardrottins er breytt í eigin númeraröð vöru.</span><span class="sxs-lookup"><span data-stu-id="4f8e3-112">To enable conversion of a nonstock item card to a normal item card, you must first set up how vendor item numbering is converted to your own item numbering.</span></span>   

## <a name="to-create-a-nonstock-item"></a><span data-ttu-id="4f8e3-113">Stofna utanbirgðavöru</span><span class="sxs-lookup"><span data-stu-id="4f8e3-113">To create a nonstock item</span></span>
<span data-ttu-id="4f8e3-114">Utanbirgðavöruspjöld hafa mikið minni upplýsingar en venjulegur birgðaspjöldum þar sem þær eru aðeins boðnar gegn tilboðum og með öðrum hætti.</span><span class="sxs-lookup"><span data-stu-id="4f8e3-114">Nonstock item cards have much less information than normal item cards because you only use them to offer on quotes and in other ways.</span></span> <span data-ttu-id="4f8e3-115">Af þeirri ástæðu þær þarf að umbreyta þeim í venjulegur birgðaspjöldum áður en hægt bóka sölufærslur fyrir þá.</span><span class="sxs-lookup"><span data-stu-id="4f8e3-115">For that reason, they must be converted to normal item cards before you can post sales transactions for them.</span></span>

1. <span data-ttu-id="4f8e3-116">Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Utanbirgðavörur** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="4f8e3-116">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Nonstock Items**, and then choose the related link.</span></span>
2. <span data-ttu-id="4f8e3-117">Valið er **Nýtt** aðgerð.</span><span class="sxs-lookup"><span data-stu-id="4f8e3-117">Choose the **New** action.</span></span>
3. <span data-ttu-id="4f8e3-118">Fyllið inn í svæðin eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="4f8e3-118">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-set-up-how-nonstock-item-numbers-are-converted-to-your-own-numbering"></a><span data-ttu-id="4f8e3-119">Setja upp hvernig utanbirgðavörunúmerum er breytt í eigin númeraröð</span><span class="sxs-lookup"><span data-stu-id="4f8e3-119">To set up how nonstock item numbers are converted to your own numbering</span></span>
<span data-ttu-id="4f8e3-120">Til að virkja umbreytingu utanbirgðaspjalds í venjulegt birgðaspjald, þarf fyrst að setja upp hvernig númeraröð lánardrottins er breytt í eigin númeraraðasnið.</span><span class="sxs-lookup"><span data-stu-id="4f8e3-120">To enable conversion of a nonstock item card to a normal item card, you must first set up how the vendor's item numbering is converted to your own item number format.</span></span>

1. <span data-ttu-id="4f8e3-121">Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Utanbirgðavörur Uppsetning** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="4f8e3-121">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Nonstock Item Setup**, and then choose the related link.</span></span>
2. <span data-ttu-id="4f8e3-122">Fyllið inn í reitina eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="4f8e3-122">Fill in the fields as necessary.</span></span>

## <a name="to-convert-a-nonstock-item-to-a-normal-item"></a><span data-ttu-id="4f8e3-123">Breyta utanbirgðavara í venjulega vöru</span><span class="sxs-lookup"><span data-stu-id="4f8e3-123">To convert a nonstock item to a normal item</span></span>
1. <span data-ttu-id="4f8e3-124">Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Utanbirgðavörur** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="4f8e3-124">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Nonstock Items**, and then choose the related link.</span></span>
2. <span data-ttu-id="4f8e3-125">Opna spjald fyrir utanbirgðavara sem þú vilt umbreyta í venjulega vöru.</span><span class="sxs-lookup"><span data-stu-id="4f8e3-125">Open the card for a nonstock item that you want to convert to a normal item.</span></span>
3. <span data-ttu-id="4f8e3-126">Í glugganum **utanbirgðavöruspjald** er valið **Stofna vara** aðgerð.</span><span class="sxs-lookup"><span data-stu-id="4f8e3-126">In the **Nonstock Item Card** window, choose the **Create Item** action.</span></span>

<span data-ttu-id="4f8e3-127">Stofnuð eru Nýtt birgðaspjald með sem er forútfyllt með upplýsingum úr utanbirgðavara og viðeigandi vörusniðmát.</span><span class="sxs-lookup"><span data-stu-id="4f8e3-127">A new item card prefilled with information from the nonstock item and a relevant item template is created.</span></span> <span data-ttu-id="4f8e3-128">Hægt er síðan að fylla inn í eða breyta reitum á nýja birgðaspjaldinu eins og þörf krefur.</span><span class="sxs-lookup"><span data-stu-id="4f8e3-128">You can then fill or edit fields on the new item card as necessary.</span></span> <span data-ttu-id="4f8e3-129">Nánari upplýsingar eru í [Skrá nýjar vörur](inventory-how-register-new-items.md).</span><span class="sxs-lookup"><span data-stu-id="4f8e3-129">For more information, see [Register New Items](inventory-how-register-new-items.md).</span></span>

## <a name="to-sell-a-nonstock-item-and-convert-it-to-a-normal-item"></a><span data-ttu-id="4f8e3-130">Selja utanbirgðavara og breyta henni í venjulega vöru</span><span class="sxs-lookup"><span data-stu-id="4f8e3-130">To sell a nonstock item, and convert it to a normal item</span></span>
1. <span data-ttu-id="4f8e3-131">Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn  **Sölupantanir** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="4f8e3-131">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Sales Orders**, and then choose the related link.</span></span>
2. <span data-ttu-id="4f8e3-132">Valið er **Nýtt** aðgerð.</span><span class="sxs-lookup"><span data-stu-id="4f8e3-132">Choose the **New** action.</span></span> <span data-ttu-id="4f8e3-133">Fylltu út reitina á flýtiflipanum **Almennt** eins og fyrir hvaða sölustað sem er.</span><span class="sxs-lookup"><span data-stu-id="4f8e3-133">Fill in the fields on the **General** FastTab as for any sales order.</span></span> <span data-ttu-id="4f8e3-134">Frekari upplýsingar eru í [Selja vörur](sales-how-sell-products.md).</span><span class="sxs-lookup"><span data-stu-id="4f8e3-134">For more information, see [Sell Products](sales-how-sell-products.md).</span></span>
3. <span data-ttu-id="4f8e3-135">Á nýjum sölulínum, í reitnum **Gerð**, veldu **vöru** en skildu eftir **Nr.**</span><span class="sxs-lookup"><span data-stu-id="4f8e3-135">On a new sales line, in the **Type** field, select **Item**, but leave the **No.**</span></span> <span data-ttu-id="4f8e3-136">að vera auður.</span><span class="sxs-lookup"><span data-stu-id="4f8e3-136">field empty.</span></span>
4. <span data-ttu-id="4f8e3-137">Veldu aðgerðina **Lína** og veldu síðan **Velja utanbirgðavörur**.</span><span class="sxs-lookup"><span data-stu-id="4f8e3-137">Choose the **Line** action, and then choose the **Select Nonstock Items** action.</span></span>

    <span data-ttu-id="4f8e3-138">Utanbirgðavara er breytt í venjulega vöru</span><span class="sxs-lookup"><span data-stu-id="4f8e3-138">The nonstock item is converted to a normal item.</span></span> <span data-ttu-id="4f8e3-139">Stofnuð eru Nýtt birgðaspjald með sem er forútfyllt með upplýsingum úr utanbirgðavara og viðeigandi vörusniðmát.</span><span class="sxs-lookup"><span data-stu-id="4f8e3-139">A new item card prefilled with information from the nonstock item and a relevant item template is created.</span></span>
5. <span data-ttu-id="4f8e3-140">Í **utanbirgðavara** glugganum, veljið utanbirgðavöruna sem þú vilt selja og veljið svo hnappinn **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="4f8e3-140">In the **Nonstock Items** window, select the nonstock item that you want to sell, and then choose the **OK** button.</span></span>
6. <span data-ttu-id="4f8e3-141">Þegar sölupöntunarlínunum er lokið, skal velja **bóka** aðgerðina.</span><span class="sxs-lookup"><span data-stu-id="4f8e3-141">When the sales order is complete, choose the **Post** action.</span></span>

<span data-ttu-id="4f8e3-142">Hægt er síðan að fylla inn í eða breyta reitum á nýja birgðaspjaldinu eins og þörf krefur.</span><span class="sxs-lookup"><span data-stu-id="4f8e3-142">You can then fill or edit fields on the new item card as necessary.</span></span> <span data-ttu-id="4f8e3-143">Nánari upplýsingar eru í [Skrá nýjar vörur](inventory-how-register-new-items.md).</span><span class="sxs-lookup"><span data-stu-id="4f8e3-143">For more information, see [Register New Items](inventory-how-register-new-items.md).</span></span>

> [!NOTE]  
>   <span data-ttu-id="4f8e3-144">Tilvísunarskrá yfir vöru er sjálfkrafa búin til fyrir lánardrottinn vörunnar á milli vörunúmers lánardrottins og nýja vörunúmers þíns.</span><span class="sxs-lookup"><span data-stu-id="4f8e3-144">An Item cross reference record is automatically created for the vendor of the item between the vendor's item number and your new item number.</span></span>

## <a name="see-also"></a><span data-ttu-id="4f8e3-145">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="4f8e3-145">See Also</span></span>
[<span data-ttu-id="4f8e3-146">Skrá nýjar vörur</span><span class="sxs-lookup"><span data-stu-id="4f8e3-146">Register New Items</span></span>](inventory-how-register-new-items.md)  
<span data-ttu-id="4f8e3-147">[Sérstakar pantanir stofnaðar](sales-how-to-create-special-orders.md)|</span><span class="sxs-lookup"><span data-stu-id="4f8e3-147">[Create Special Orders](sales-how-to-create-special-orders.md)|</span></span>  
[<span data-ttu-id="4f8e3-148">Birgðir</span><span class="sxs-lookup"><span data-stu-id="4f8e3-148">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="4f8e3-149">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="4f8e3-149">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

