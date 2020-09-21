---
title: Stofna viðskiptamannaspjald til að skrá nýja viðskiptamenn | Microsoft Docs
description: Lýsir því hvernig skal stofna viðskiptamannaspjald til að skrá upplýsingar um alla nýja viðskiptamenn eða biðlara sem selt er til.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: client
ms.date: 06/24/2020
ms.author: edupont
ms.openlocfilehash: 3e25756cff974e0db835f5e3ed3247dff6d7624a
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/09/2020
ms.locfileid: "3780885"
---
# <a name="register-new-customers"></a><span data-ttu-id="4a70e-103">Skrá nýja viðskiptamenn</span><span class="sxs-lookup"><span data-stu-id="4a70e-103">Register New Customers</span></span>

<span data-ttu-id="4a70e-104">Viðskiptamenn eru uppruni tekna.</span><span class="sxs-lookup"><span data-stu-id="4a70e-104">Customers are the source of your income.</span></span> <span data-ttu-id="4a70e-105">Þú verður að skrá þig hver viðskiptavinur sem þú selur sem viðskiptavinakort.</span><span class="sxs-lookup"><span data-stu-id="4a70e-105">You must register each customer you sell to as a customer card.</span></span> <span data-ttu-id="4a70e-106">Viðskiptamannaspjald inniheldur upplýsingarnar sem þarf til að selja vörur til viðskiptamannsins.</span><span class="sxs-lookup"><span data-stu-id="4a70e-106">Customer cards hold the information that is required to sell products to the customer.</span></span> <span data-ttu-id="4a70e-107">Frekari upplýsingar eru í [Reikningsfæra sölur](sales-how-invoice-sales.md) og [Skrá nýja hluti](inventory-how-register-new-items.md).</span><span class="sxs-lookup"><span data-stu-id="4a70e-107">For more information, see [Invoice Sales](sales-how-invoice-sales.md) and [Register New Items](inventory-how-register-new-items.md).</span></span>  

<span data-ttu-id="4a70e-108">Áður en hægt er að skrá nýja viðskiptamenn þarf að setja upp ýmsar sölukóða sem hægt er að velja úr þegar fyllt eru út viðskiptamannaspjöld.</span><span class="sxs-lookup"><span data-stu-id="4a70e-108">Before you can register new customers, you must set up various sales codes that you can select from when you fill in customer cards.</span></span> <span data-ttu-id="4a70e-109">Nánari upplýsingar er að finna í [Uppsetning sölu](sales-setup-sales.md).</span><span class="sxs-lookup"><span data-stu-id="4a70e-109">For more information, see [Setting Up Sales](sales-setup-sales.md).</span></span>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE3PZsM]

## <a name="adding-new-customers"></a><span data-ttu-id="4a70e-110">Bæta við nýjum viðskiptavinum</span><span class="sxs-lookup"><span data-stu-id="4a70e-110">Adding new customers</span></span>

<span data-ttu-id="4a70e-111">Til að skrá nýjan viðskiptavin þarf að fylla út viðskiptamannsspjald.</span><span class="sxs-lookup"><span data-stu-id="4a70e-111">To register a new customer, you must fill in a customer card.</span></span> <span data-ttu-id="4a70e-112">Hægt er að búa til sniðmátum fyrir mismunandi forstillingar viðskiptavina eða hægt er að bæta við viðskiptavinum án sniðmáta.</span><span class="sxs-lookup"><span data-stu-id="4a70e-112">You can establish templates for different customer profiles, or you can add customers without templates.</span></span>  

> [!NOTE]  
> <span data-ttu-id="4a70e-113">Ef viðskiptamannasniðmát eru til fyrir mismunandi tegundir viðskipamanna, þá birtist sjálfkrafa síða þegar búið er til nýtt viðskiptamannaspjald og hægt er að velja viðeigandi sniðmát.</span><span class="sxs-lookup"><span data-stu-id="4a70e-113">If customer templates exist for different customer types, then a page appears when you create a new customer card from where you can select an appropriate template.</span></span> <span data-ttu-id="4a70e-114">Ef aðeins eitt viðskiptamanna sniðmát er fyrir hendi, nota ný viðskiptamannaspjöld alltaf það sniðmát.</span><span class="sxs-lookup"><span data-stu-id="4a70e-114">If only one customer template exists, then new customer cards always use that template.</span></span>  

### <a name="to-create-a-new-customer-card"></a><span data-ttu-id="4a70e-115">Að stofna nýtt viðskiptamannaspjald</span><span class="sxs-lookup"><span data-stu-id="4a70e-115">To create a new customer card</span></span>

1. <span data-ttu-id="4a70e-116">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Viðskiptamenn** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="4a70e-116">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Customers**, and then choose the related link.</span></span>  
2. <span data-ttu-id="4a70e-117">Á síðunni **Viðskiptamenn** skal velja aðgerðina **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="4a70e-117">On the **Customers** page, choose the **New** action.</span></span>

    <span data-ttu-id="4a70e-118">Ef aðeins eitt viðskiptamannasniðmát er fyrir hendi, opnast nýtt viðskiptamannaspjald með reiti útfyllta með upplýsingum úr sniðmátinu.</span><span class="sxs-lookup"><span data-stu-id="4a70e-118">If only one customer template exists, then a new customer card opens with some fields filled with information from the template.</span></span>

    <span data-ttu-id="4a70e-119">Ef fleiri en eitt viðskiptamannasniðmát er fyrir hendi, þá birtist sjálfkrafa síða með tiltækum viðskiptamannasniðmátum.</span><span class="sxs-lookup"><span data-stu-id="4a70e-119">If more than one customer template exists, then a page opens from which you can select a customer template.</span></span> <span data-ttu-id="4a70e-120">Í því tilviki, fylgið næstu tveimur skrefum.</span><span class="sxs-lookup"><span data-stu-id="4a70e-120">In that case, follow the next two steps.</span></span>
3. <span data-ttu-id="4a70e-121">Á síðunni **Velja sniðmát fyrir nýjan viðskiptamann** skal velja sniðmátið sem á að nota fyrir nýja viðskiptamannaspjaldið.</span><span class="sxs-lookup"><span data-stu-id="4a70e-121">On the **Select a template for a new customer** page, choose the template that you want to use for the new customer card.</span></span>
4. <span data-ttu-id="4a70e-122">Velja hnappinn **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="4a70e-122">Choose the **OK** button.</span></span> <span data-ttu-id="4a70e-123">Nýtt viðskiptamannaspjald opnast þar sem búið er að fylla upplýsingar úr sniðmátinu inn í reitina.</span><span class="sxs-lookup"><span data-stu-id="4a70e-123">A new customer card opens with some fields filled with information from the template.</span></span>  
5. <span data-ttu-id="4a70e-124">Því næst skal færa inn eða breyta reitum á viðskiptamannaspjaldinu eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="4a70e-124">Proceed to fill or change fields on the customer card as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

<span data-ttu-id="4a70e-125">Á flýtiflipanum **Söluverð** er hægt að sjá sérverð eða afslætti sem veittir eru fyrir viðskiptamanninn ef ákveðin skilyrði eru uppfyllt, svo sem vara, lágmarkspöntunarmagn eða lokadagur.</span><span class="sxs-lookup"><span data-stu-id="4a70e-125">On the **Sales Prices** FastTab, you can view special prices or discounts that you grant for the customer if certain criteria are met, such as item, minimum order quantity, or ending date.</span></span> <span data-ttu-id="4a70e-126">Hver lína stendur fyrir sértilboðsverð eða línuafslátt.</span><span class="sxs-lookup"><span data-stu-id="4a70e-126">Each row represents a special price or line discount.</span></span> <span data-ttu-id="4a70e-127">Hver dálkur táknar viðmiðun sem verða að sækja til að réttlæta sérstakt verð sem þú slærð inn í **Einingaverð** sviði, eða línuafslátt sem þú slærð inn í **Línuafsláttur %**.</span><span class="sxs-lookup"><span data-stu-id="4a70e-127">Each column represents a criterion that must apply to warrant the special price that you enter in the **Unit Price** field, or the line discount that you enter in the **Line Discount %** field.</span></span> <span data-ttu-id="4a70e-128">Nánari upplýsingar eru í [Skrá söluverð, afslátt og greiðslusamkomulag](sales-how-record-sales-price-discount-payment-agreements.md).</span><span class="sxs-lookup"><span data-stu-id="4a70e-128">For more information, see [Record Sales Price, Discount, and Payment Agreements](sales-how-record-sales-price-discount-payment-agreements.md).</span></span>

<span data-ttu-id="4a70e-129">Viðskiptamaðurinn hefur nú verið skráður og viðskiptamannaspjaldið má nú nota í söluskjölum.</span><span class="sxs-lookup"><span data-stu-id="4a70e-129">The customer is now registered, and the customer card is ready to be used on sales documents.</span></span>

<span data-ttu-id="4a70e-130">Ef nota á þetta viðskiptamannaspjald sem sniðmát þegar ný viðskiptamannaspjöld eru búin til, vistið það sem sniðmát.</span><span class="sxs-lookup"><span data-stu-id="4a70e-130">If you want to use this customer card as a template when you create new customer cards, you can save it as a template.</span></span> <span data-ttu-id="4a70e-131">Nánari upplýsingar eru í eftirfarandi kafla.</span><span class="sxs-lookup"><span data-stu-id="4a70e-131">For more information, see the following section.</span></span>  

### <a name="to-save-the-customer-card-as-a-template"></a><span data-ttu-id="4a70e-132">Til að vista viðskiptamannaspjaldið sem sniðmát</span><span class="sxs-lookup"><span data-stu-id="4a70e-132">To save the customer card as a template</span></span>

1. <span data-ttu-id="4a70e-133">Á síðunni **Viðskiptamannaspjald** skal velja aðgerðina **Vista sem sniðmát**.</span><span class="sxs-lookup"><span data-stu-id="4a70e-133">On the **Customer Card** page, choose the **Save as Template** action.</span></span> <span data-ttu-id="4a70e-134">Síðan **Viðskiptamannasniðmát** opnast og sýnir viðskiptamannaspjaldið sem sniðmát.</span><span class="sxs-lookup"><span data-stu-id="4a70e-134">The **Customer Template** page opens showing the customer card as a template.</span></span>
2. <span data-ttu-id="4a70e-135">Fyllið inn reitina eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="4a70e-135">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="4a70e-136">Til að endurnota víddir í sniðmátum, veljið aðgerðina **Víddir**.</span><span class="sxs-lookup"><span data-stu-id="4a70e-136">To reuse dimensions in templates, choose the **Dimensions** action.</span></span> <span data-ttu-id="4a70e-137">Síðan **Víddarsniðmát** opnast og sýnir alla víddarkóða sem settir eru upp fyrir viðskiptamanninn.</span><span class="sxs-lookup"><span data-stu-id="4a70e-137">The **Dimension Templates** page opens showing any dimension codes that are set up for the customer.</span></span>
4. <span data-ttu-id="4a70e-138">Breyta eða færa inn víddarkóða sem munu gilda fyrir ný viðskiptamannaspjöld sem stofnuð eru með sniðmátinu.</span><span class="sxs-lookup"><span data-stu-id="4a70e-138">Edit or enter dimension codes that will apply to new customer cards created by using the template.</span></span>  
5. <span data-ttu-id="4a70e-139">Þegar lokið hefur verið við nýja viðskiptamannasniðmátið skal velja hnappinn **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="4a70e-139">When you have completed the new customer template, choose the **OK** button.</span></span>

<span data-ttu-id="4a70e-140">Viðskiptamannasniðmátinu verður bætt við lista viðskiptamannasniðmáta þannig að hægt er að nota það til að búa til ný viðskiptamannaspjöld.</span><span class="sxs-lookup"><span data-stu-id="4a70e-140">The customer template is added to the list of customer templates, so that you can use it to create new customer cards.</span></span>

## <a name="deleting-customer-cards"></a><span data-ttu-id="4a70e-141">Eyðir viðskiptavinaspjöldum</span><span class="sxs-lookup"><span data-stu-id="4a70e-141">Deleting customer cards</span></span>

<span data-ttu-id="4a70e-142">Ef þú hefur bókað færslu fyrir viðskiptavin er ekki hægt að eyða spjaldinu þar sem hugsanlega þarf að nota fjárhagsfærslurnar í endurskoðun.</span><span class="sxs-lookup"><span data-stu-id="4a70e-142">If you have posted a transaction for a customer, you cannot delete the card because the ledger entries may be needed for auditing.</span></span> <span data-ttu-id="4a70e-143">Til að eyða viðskiptamannaspjöldum með fjárhagsfærslum skaltu hafa samband við samstarfsaðila Microsoft til að gera það með kóða.</span><span class="sxs-lookup"><span data-stu-id="4a70e-143">To delete customer cards with ledger entries, contact to Microsoft partner to do so through code.</span></span>  

## <a name="see-also"></a><span data-ttu-id="4a70e-144">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="4a70e-144">See Also</span></span>

[<span data-ttu-id="4a70e-145">Skilgreina Greiðsluhætti</span><span class="sxs-lookup"><span data-stu-id="4a70e-145">Defining Payment Methods</span></span>](finance-payment-methods.md)  
[<span data-ttu-id="4a70e-146">Sameina tvítekin atriði</span><span class="sxs-lookup"><span data-stu-id="4a70e-146">Merge Duplicate Records</span></span>](sales-how-merge-duplicate-records.md)  
[<span data-ttu-id="4a70e-147">Stofnun númeraraða</span><span class="sxs-lookup"><span data-stu-id="4a70e-147">Create Number Series</span></span>](ui-create-number-series.md)  
[<span data-ttu-id="4a70e-148">Sala</span><span class="sxs-lookup"><span data-stu-id="4a70e-148">Sales</span></span>](sales-manage-sales.md)  
[<span data-ttu-id="4a70e-149">Uppsetning sölu</span><span class="sxs-lookup"><span data-stu-id="4a70e-149">Setting Up Sales</span></span>](sales-setup-sales.md)  
<span data-ttu-id="4a70e-150">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="4a70e-150">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
