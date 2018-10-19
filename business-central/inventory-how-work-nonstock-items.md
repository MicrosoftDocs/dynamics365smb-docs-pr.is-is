---
title: "Búa til og stjórna vörulistaatriðum| Microsoft Docs"
description: "Lýsir hvernig á að eiga viðskipti með hluti sem eru í lista seljanda yfir vörur en ekki í eigin lista yfir vörur."
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: non-inventoriable
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: feef36443adef82329fe47573dd05cc6941b9d87
ms.contentlocale: is-is
ms.lasthandoff: 09/28/2018

---
# <a name="work-with-catalog-items"></a><span data-ttu-id="5383d-103">Vinna með vörulistaatriði</span><span class="sxs-lookup"><span data-stu-id="5383d-103">Work with Catalog Items</span></span>
<span data-ttu-id="5383d-104">Þú getur boðið ákveðnar vörur til viðskiptamanna þinna til þæginda, sem þú vilt ekki stjórna í kerfinu þínu fyrr en þú byrjar að selja þær.</span><span class="sxs-lookup"><span data-stu-id="5383d-104">You can offer certain items to your customers for their convenience, which you do not want to manage in your system until you start selling them.</span></span> <span data-ttu-id="5383d-105">Þegar þú vilt byrja að stjórna slíkum vörum í kerfinu þínu, getur þú breytt þeim í venjuleg birgðaspjöld á tvo vegu.</span><span class="sxs-lookup"><span data-stu-id="5383d-105">When you want to start managing such items in your system, you can convert them to normal item cards in two ways.</span></span>

* <span data-ttu-id="5383d-106">Búa til nýtt birgðaspjald byggt á sniðmáti úr spjaldi vörulistaatriðis.</span><span class="sxs-lookup"><span data-stu-id="5383d-106">From a catalog item card, create a new item card based on a template.</span></span>
* <span data-ttu-id="5383d-107">Frá sölupöntunarlínu af gerðinni **Vara** með reitinn **Nei** tóman skaltu velja vörulistaatriði.</span><span class="sxs-lookup"><span data-stu-id="5383d-107">From a sales order line of type **Item** with an empty **No** field, select a catalog item.</span></span> <span data-ttu-id="5383d-108">Birgðaspjald er þá sjálfkrafa búið til fyrir vörulistaatriðið.</span><span class="sxs-lookup"><span data-stu-id="5383d-108">An item card is then automatically created for the catalog item.</span></span>

> [!NOTE]  
> <span data-ttu-id="5383d-109">Ekki hægt er að velja vörulistaatriði úr glugganum **Sölureikningur**.</span><span class="sxs-lookup"><span data-stu-id="5383d-109">You cannot select a catalog item from the **Sales Invoice** window.</span></span><br /><br />
> <span data-ttu-id="5383d-110">Hægt er að velja vörulistaatriði úr **Sölutilboð** glugganum, en vörulistaatriði verður ekki umbreytt í venjulega vöru þegar þú notar **Búa til Pöntun** aðgerð.</span><span class="sxs-lookup"><span data-stu-id="5383d-110">You can select a catalog item from the **Sales Quote** window, but the catalog item will not be converted to a normal item when you use the **Make Order** function.</span></span>

<span data-ttu-id="5383d-111">Vörulistaatriði hefur yfirleitt vörunúmer þess lánardrottins sem sér um að veita hana.</span><span class="sxs-lookup"><span data-stu-id="5383d-111">A catalog item typically has the item number of the vendor who supplies it.</span></span> <span data-ttu-id="5383d-112">Til að virkja umbreytingu vörulistaatriðisspjalds í venjulegur birgðaspjald þarftu fyrst að setja það upp hvernig númeraröð lánardrottins er breytt í eigin vörunúmer.</span><span class="sxs-lookup"><span data-stu-id="5383d-112">To enable conversion of a catalog item card to a normal item card, you must first set up how vendor item numbering is converted to your own item numbering.</span></span>   

> [!Important]
> <span data-ttu-id="5383d-113">Vörulistaatriði má ekki rugla saman við vörur sem eru ekki vörur í birgðum sem eru reglulegar vörur sem eru gefnar tegundina **Ekki í birgðum**, til að halda þeim ekki tiltækum og fyrir utan kostnaðarútreikningur, til dæmis vegna þess að þeir eru aðeins notaðir innbyrðis og eru lágir kostnaður.</span><span class="sxs-lookup"><span data-stu-id="5383d-113">Catalog items are not to be mistaken with non-inventory items, which are regular items that are given the type **Non-Inventory** to keep them out of availability and costing calculations, for example, because they are only used internally and have a low cost.</span></span> <span data-ttu-id="5383d-114">Nánari upplýsingar er að finna í [Um vörugerðir](inventory-about-item-types.md).</span><span class="sxs-lookup"><span data-stu-id="5383d-114">For more information, see [About Item Types](inventory-about-item-types.md).</span></span>

## <a name="to-create-a-catalog-item"></a><span data-ttu-id="5383d-115">Til að búa til vörulistaatriði</span><span class="sxs-lookup"><span data-stu-id="5383d-115">To create a catalog item</span></span>
<span data-ttu-id="5383d-116">Vörulistaatriðaspjöld hafa miklu minni upplýsingar en venjulegir birgðaspjald vegna þess að þú notar þær aðeins til að bjóða upp á vitna og á annan hátt.</span><span class="sxs-lookup"><span data-stu-id="5383d-116">Catalog item cards have much less information than normal item cards because you only use them to offer on quotes and in other ways.</span></span> <span data-ttu-id="5383d-117">Af þeirri ástæðu þær þarf að umbreyta þeim í venjulegur birgðaspjöldum áður en hægt bóka sölufærslur fyrir þá.</span><span class="sxs-lookup"><span data-stu-id="5383d-117">For that reason, they must be converted to normal item cards before you can post sales transactions for them.</span></span>

1. <span data-ttu-id="5383d-118">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Vörulistaatriði** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="5383d-118">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Catalog Items**, and then choose the related link.</span></span>
2. <span data-ttu-id="5383d-119">Valið er **Nýtt** aðgerð.</span><span class="sxs-lookup"><span data-stu-id="5383d-119">Choose the **New** action.</span></span>
3. <span data-ttu-id="5383d-120">Fyllið inn í reitina eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="5383d-120">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-set-up-how-catalog-item-numbers-are-converted-to-your-own-numbering"></a><span data-ttu-id="5383d-121">Til að setja upp hvernig vörulistaatriðisnúmer eru breytt í eigin númeraröð</span><span class="sxs-lookup"><span data-stu-id="5383d-121">To set up how catalog item numbers are converted to your own numbering</span></span>
<span data-ttu-id="5383d-122">Til að virkja umbreytingu vörulistaatriðisspjals í venjulegur birgðaspjald þarftu fyrst að setja það upp hvernig númeraröð lánardrottins er breytt í eigin númeraraðasnið.</span><span class="sxs-lookup"><span data-stu-id="5383d-122">To enable conversion of a catalog item card to a normal item card, you must first set up how the vendor's item numbering is converted to your own item number format.</span></span>

1. <span data-ttu-id="5383d-123">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Uppsetning vörulistaatriðis** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="5383d-123">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Catalog Item Setup**, and then choose the related link.</span></span>
2. <span data-ttu-id="5383d-124">Fyllið inn í reitina eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="5383d-124">Fill in the fields as necessary.</span></span>

## <a name="to-convert-a-catalog-item-to-a-normal-item"></a><span data-ttu-id="5383d-125">Til að breyta vörulistaatriði í venjulegt atriði</span><span class="sxs-lookup"><span data-stu-id="5383d-125">To convert a catalog item to a normal item</span></span>
1. <span data-ttu-id="5383d-126">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Vörulistaatriði** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="5383d-126">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Catalog Items**, and then choose the related link.</span></span>
2. <span data-ttu-id="5383d-127">Opnaðu spjaldið fyrir vörulistaatriði sem þú vilt breyta í venjulegt atriði.</span><span class="sxs-lookup"><span data-stu-id="5383d-127">Open the card for a catalog item that you want to convert to a normal item.</span></span>
3. <span data-ttu-id="5383d-128">Í glugganum **Birgðaspjald vörulista** er valin aðgerðin **Stofna atriði**.</span><span class="sxs-lookup"><span data-stu-id="5383d-128">In the **Catalog Item Card** window, choose the **Create Item** action.</span></span>

<span data-ttu-id="5383d-129">Stofnuð eru Nýtt birgðaspjald sem er forútfyllt með upplýsingum úr vörulistaatriði og viðeigandi vörusniðmát.</span><span class="sxs-lookup"><span data-stu-id="5383d-129">A new item card prefilled with information from the catalog item and a relevant item template is created.</span></span> <span data-ttu-id="5383d-130">Hægt er síðan að fylla inn í eða breyta reitum á nýja birgðaspjaldinu eins og þörf krefur.</span><span class="sxs-lookup"><span data-stu-id="5383d-130">You can then fill or edit fields on the new item card as necessary.</span></span> <span data-ttu-id="5383d-131">Nánari upplýsingar eru í [Skrá nýjar vörur](inventory-how-register-new-items.md).</span><span class="sxs-lookup"><span data-stu-id="5383d-131">For more information, see [Register New Items](inventory-how-register-new-items.md).</span></span>

## <a name="to-sell-a-catalog-item-and-convert-it-to-a-normal-item"></a><span data-ttu-id="5383d-132">Til að selja vörulistaatriði og breyta því í venjulegt atriði</span><span class="sxs-lookup"><span data-stu-id="5383d-132">To sell a catalog item, and convert it to a normal item</span></span>
1. <span data-ttu-id="5383d-133">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Sölupantanir** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="5383d-133">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Orders**, and then choose the related link.</span></span>
2. <span data-ttu-id="5383d-134">Valið er **Nýtt** aðgerð.</span><span class="sxs-lookup"><span data-stu-id="5383d-134">Choose the **New** action.</span></span> <span data-ttu-id="5383d-135">Fylltu út reitina á flýtiflipanum **Almennt** eins og fyrir hvaða sölustað sem er.</span><span class="sxs-lookup"><span data-stu-id="5383d-135">Fill in the fields on the **General** FastTab as for any sales order.</span></span> <span data-ttu-id="5383d-136">Frekari upplýsingar eru í [Selja vörur](sales-how-sell-products.md).</span><span class="sxs-lookup"><span data-stu-id="5383d-136">For more information, see [Sell Products](sales-how-sell-products.md).</span></span>
3. <span data-ttu-id="5383d-137">Á nýjum sölulínum, í reitnum **Gerð**, veldu **vöru** en skildu eftir **Nr.**</span><span class="sxs-lookup"><span data-stu-id="5383d-137">On a new sales line, in the **Type** field, select **Item**, but leave the **No.**</span></span> <span data-ttu-id="5383d-138">að vera auður.</span><span class="sxs-lookup"><span data-stu-id="5383d-138">field empty.</span></span>
4. <span data-ttu-id="5383d-139">Veldu aðgerðina **Lína** og veldu síðan **Velja vörulistaatriði** aðgerð.</span><span class="sxs-lookup"><span data-stu-id="5383d-139">Choose the **Line** action, and then choose the **Select Catalog Items** action.</span></span>

    <span data-ttu-id="5383d-140">Vörulistaatriði breytt í venjulegt atriði.</span><span class="sxs-lookup"><span data-stu-id="5383d-140">The catalog item is converted to a normal item.</span></span> <span data-ttu-id="5383d-141">Stofnuð eru Nýtt birgðaspjald sem er forútfyllt með upplýsingum úr vörulistaatriði og viðeigandi vörusniðmát.</span><span class="sxs-lookup"><span data-stu-id="5383d-141">A new item card prefilled with information from the catalog item and a relevant item template is created.</span></span>
5. <span data-ttu-id="5383d-142">Í **Vörulistaatriði** glugganum, veljið vörulistaatriðið sem á að selja og svo hnappinn **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="5383d-142">In the **Catalog Items** window, select the catalog item that you want to sell, and then choose the **OK** button.</span></span>
6. <span data-ttu-id="5383d-143">Þegar sölupöntunarlínunum er lokið, skal velja **bóka** aðgerðina.</span><span class="sxs-lookup"><span data-stu-id="5383d-143">When the sales order is complete, choose the **Post** action.</span></span>

<span data-ttu-id="5383d-144">Hægt er síðan að fylla inn í eða breyta reitum á nýja birgðaspjaldinu eins og þörf krefur.</span><span class="sxs-lookup"><span data-stu-id="5383d-144">You can then fill or edit fields on the new item card as necessary.</span></span> <span data-ttu-id="5383d-145">Nánari upplýsingar eru í [Skrá nýjar vörur](inventory-how-register-new-items.md).</span><span class="sxs-lookup"><span data-stu-id="5383d-145">For more information, see [Register New Items](inventory-how-register-new-items.md).</span></span>

> [!NOTE]  
>   <span data-ttu-id="5383d-146">Tilvísunarskrá yfir vöru er sjálfkrafa búin til fyrir lánardrottinn vörunnar á milli vörunúmers lánardrottins og nýja vörunúmers þíns.</span><span class="sxs-lookup"><span data-stu-id="5383d-146">An Item cross reference record is automatically created for the vendor of the item between the vendor's item number and your new item number.</span></span>

## <a name="see-also"></a><span data-ttu-id="5383d-147">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="5383d-147">See Also</span></span>
[<span data-ttu-id="5383d-148">Skrá nýjar vörur</span><span class="sxs-lookup"><span data-stu-id="5383d-148">Register New Items</span></span>](inventory-how-register-new-items.md)  
<span data-ttu-id="5383d-149">[Sérstakar pantanir stofnaðar](sales-how-to-create-special-orders.md)|</span><span class="sxs-lookup"><span data-stu-id="5383d-149">[Create Special Orders](sales-how-to-create-special-orders.md)|</span></span>  
[<span data-ttu-id="5383d-150">Birgðir</span><span class="sxs-lookup"><span data-stu-id="5383d-150">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="5383d-151">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="5383d-151">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

