---
title: "Stofna viðskiptamannaspjald til að skrá nýja viðskiptamenn | Microsoft Docs"
description: "Lýsir því hvernig skal stofna viðskiptamannaspjald til að skrá upplýsingar um alla nýja viðskiptamenn eða biðlara sem selt er til."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: client
ms.date: 03/29/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: a03575bce7d1029e47f2aa1a46d5d0dcf585ab2a
ms.contentlocale: is-is
ms.lasthandoff: 01/30/2018

---
# <a name="register-new-customers"></a><span data-ttu-id="e5273-103">Skrá nýja viðskiptamenn</span><span class="sxs-lookup"><span data-stu-id="e5273-103">Register New Customers</span></span>
<span data-ttu-id="e5273-104">Viðskiptamenn eru uppruni tekna.</span><span class="sxs-lookup"><span data-stu-id="e5273-104">Customers are the source of your income.</span></span> <span data-ttu-id="e5273-105">Þú verður að skrá þig hver viðskiptavinur sem þú selur sem viðskiptavinakort.</span><span class="sxs-lookup"><span data-stu-id="e5273-105">You must register each customer you sell to as a customer card.</span></span> <span data-ttu-id="e5273-106">Viðskiptamannaspjald inniheldur upplýsingarnar sem þarf til að selja vörur til viðskiptamannsins.</span><span class="sxs-lookup"><span data-stu-id="e5273-106">Customer cards hold the information that is required to sell products to the customer.</span></span> <span data-ttu-id="e5273-107">Frekari upplýsingar eru í [Reikningsfæra sölur](sales-how-invoice-sales.md) og [Skrá nýja hluti](inventory-how-register-new-items.md).</span><span class="sxs-lookup"><span data-stu-id="e5273-107">For more information, see [Invoice Sales](sales-how-invoice-sales.md) and [Register New Items](inventory-how-register-new-items.md).</span></span>  

<span data-ttu-id="e5273-108">Áður en hægt er að skrá nýja viðskiptamenn þarf að setja upp ýmsar sölukóða sem hægt er að velja úr þegar fyllt eru út viðskiptamannaspjöld.</span><span class="sxs-lookup"><span data-stu-id="e5273-108">Before you can register new customers, you must set up various sales codes that you can select from when you fill in customer cards.</span></span> <span data-ttu-id="e5273-109">Nánari upplýsingar er að finna í [Uppsetning sölu](sales-setup-sales.md).</span><span class="sxs-lookup"><span data-stu-id="e5273-109">For more information, see [Setting Up Sales](sales-setup-sales.md).</span></span>

> [!NOTE]  
>   <span data-ttu-id="e5273-110">Ef viðskiptamannasniðmát eru til fyrir mismunandi tegundir viðskipamanna, þá birtist sjálfkrafa gluggi þegar búið er til nýtt viðskiptamannaspjald og hægt er að velja viðeigandi sniðmát.</span><span class="sxs-lookup"><span data-stu-id="e5273-110">If customer templates exist for different customer types, then a window appears when you create a new customer card from where you can select an appropriate template.</span></span> <span data-ttu-id="e5273-111">Ef aðeins eitt viðskiptamanna sniðmát er fyrir hendi, nota ný viðskiptamannaspjöld alltaf það sniðmát.</span><span class="sxs-lookup"><span data-stu-id="e5273-111">If only one customer template exists, then new customer cards always use that template.</span></span>

## <a name="to-create-a-new-customer-card"></a><span data-ttu-id="e5273-112">Að stofna nýtt viðskiptamannaspjald</span><span class="sxs-lookup"><span data-stu-id="e5273-112">To create a new customer card</span></span>
1. <span data-ttu-id="e5273-113">Á heimasíðunni skal velja aðgerðina **Viðskiptamenn** til að opna listann yfir núverandi viðskiptamenn.</span><span class="sxs-lookup"><span data-stu-id="e5273-113">On the Home page, choose the **Customers** action to open the list of existing customers.</span></span>  
2. <span data-ttu-id="e5273-114">Í glugganum **Viðskiptamenn** skal velja aðgerðina **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="e5273-114">In the **Customers** window, choose the **New** action.</span></span>

    <span data-ttu-id="e5273-115">Ef aðeins eitt viðskiptamannasniðmát er fyrir hendi, opnast nýtt viðskiptamannaspjald með reiti útfyllta með upplýsingum úr sniðmátinu.</span><span class="sxs-lookup"><span data-stu-id="e5273-115">If only one customer template exists, then a new customer card opens with some fields filled with information from the template.</span></span>

    <span data-ttu-id="e5273-116">Ef fleiri en eitt viðskiptamannasniðmát er fyrir hendi, þá birtist sjálfkrafa gluggi með tiltækum viðskiptamannasniðmátum.</span><span class="sxs-lookup"><span data-stu-id="e5273-116">If more than one customer template exists, then a window opens from which you can select a customer template.</span></span> <span data-ttu-id="e5273-117">Í því tilviki, fylgið næstu tveimur skrefum.</span><span class="sxs-lookup"><span data-stu-id="e5273-117">In that case, follow the next two steps.</span></span>
3. <span data-ttu-id="e5273-118">Í glugganum **Velja sniðmát fyrir nýjan viðskiptamann** skal velja sniðmátið sem á að nota fyrir nýja viðskiptamannaspjaldið.</span><span class="sxs-lookup"><span data-stu-id="e5273-118">In the **Select a template for a new customer** window, choose the template that you want to use for the new customer card.</span></span>
4. <span data-ttu-id="e5273-119">Velja hnappinn **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="e5273-119">Choose the **OK** button.</span></span> <span data-ttu-id="e5273-120">Nýtt viðskiptamannaspjald opnast þar sem búið er að fylla upplýsingar úr sniðmátinu inn í reitina.</span><span class="sxs-lookup"><span data-stu-id="e5273-120">A new customer card opens with some fields filled with information from the template.</span></span>  
5. <span data-ttu-id="e5273-121">Því næst skal færa inn eða breyta reitum á viðskiptamannaspjaldinu eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="e5273-121">Proceed to fill or change fields on the customer card as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

<span data-ttu-id="e5273-122">Á flýtiflipanum **Söluverð** er hægt að sjá sérverð eða afslætti sem veittir eru fyrir viðskiptamanninn ef ákveðin skilyrði eru uppfyllt, svo sem vara, lágmarkspöntunarmagn eða lokadagur.</span><span class="sxs-lookup"><span data-stu-id="e5273-122">On the **Sales Prices** FastTab, you can view special prices or discounts that you grant for the customer if certain criteria are met, such as item, minimum order quantity, or ending date.</span></span> <span data-ttu-id="e5273-123">Hver lína stendur fyrir sértilboðsverð eða línuafslátt.</span><span class="sxs-lookup"><span data-stu-id="e5273-123">Each row represents a special price or line discount.</span></span> <span data-ttu-id="e5273-124">Hver dálkur táknar viðmiðun sem verða að sækja til að réttlæta sérstakt verð sem þú slærð inn í **Einingaverð** sviði, eða línuafslátt sem þú slærð inn í **Línuafsláttur %**.</span><span class="sxs-lookup"><span data-stu-id="e5273-124">Each column represents a criterion that must apply to warrant the special price that you enter in the **Unit Price** field, or the line discount that you enter in the **Line Discount %** field.</span></span> <span data-ttu-id="e5273-125">Nánari upplýsingar eru í [Skrá söluverð, afslátt og greiðslusamkomulag](sales-how-record-sales-price-discount-payment-agreements.md).</span><span class="sxs-lookup"><span data-stu-id="e5273-125">For more information, see [Record Sales Price, Discount, and Payment Agreements](sales-how-record-sales-price-discount-payment-agreements.md).</span></span>

<span data-ttu-id="e5273-126">Viðskiptamaðurinn hefur nú verið skráður og viðskiptamannaspjaldið má nú nota í söluskjölum.</span><span class="sxs-lookup"><span data-stu-id="e5273-126">The customer is now registered, and the customer card is ready to be used on sales documents.</span></span>

<span data-ttu-id="e5273-127">Ef nota á þetta viðskiptamannaspjald sem sniðmát þegar ný viðskiptamannaspjöld eru búin til, vistið það sem sniðmát.</span><span class="sxs-lookup"><span data-stu-id="e5273-127">If you want to use this customer card as a template when you create new customer cards, you can save it as a template.</span></span> <span data-ttu-id="e5273-128">Nánari upplýsingar eru í eftirfarandi kafla.</span><span class="sxs-lookup"><span data-stu-id="e5273-128">For more information, see the following section.</span></span>

## <a name="to-save-the-customer-card-as-a-template"></a><span data-ttu-id="e5273-129">Til að vista viðskiptamannaspjaldið sem sniðmát</span><span class="sxs-lookup"><span data-stu-id="e5273-129">To save the customer card as a template</span></span>
1. <span data-ttu-id="e5273-130">Í glugganum **Viðskiptamannaspjald** skal velja aðgerðina **Vista sem sniðmát**.</span><span class="sxs-lookup"><span data-stu-id="e5273-130">In the **Customer Card** window, choose the **Save as Template** action.</span></span> <span data-ttu-id="e5273-131">Glugginn **Viðskiptamannasniðmát** opnast og sýnir viðskiptamannaspjaldið sem sniðmát.</span><span class="sxs-lookup"><span data-stu-id="e5273-131">The **Customer Template** window opens showing the customer card as a template.</span></span>
2. <span data-ttu-id="e5273-132">Fyllið inn í svæðin eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="e5273-132">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="e5273-133">Til að endurnota víddir í sniðmátum, veljið aðgerðina **Víddir**.</span><span class="sxs-lookup"><span data-stu-id="e5273-133">To reuse dimensions in templates, choose the **Dimensions** action.</span></span> <span data-ttu-id="e5273-134">Glugginn **Víddarsniðmát** opnast og sýnir alla víddarkóða sem settir eru upp fyrir viðskiptamanninn.</span><span class="sxs-lookup"><span data-stu-id="e5273-134">The **Dimension Templates** window opens showing any dimension codes that are set up for the customer.</span></span>
4. <span data-ttu-id="e5273-135">Breyta eða færa inn víddarkóða sem munu gilda fyrir ný viðskiptamannaspjöld sem stofnuð eru með sniðmátinu.</span><span class="sxs-lookup"><span data-stu-id="e5273-135">Edit or enter dimension codes that will apply to new customer cards created by using the template.</span></span>  
5. <span data-ttu-id="e5273-136">Þegar lokið hefur verið við nýja viðskiptamannasniðmátið skal velja hnappinn **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="e5273-136">When you have completed the new customer template, choose the **OK** button.</span></span>

<span data-ttu-id="e5273-137">Viðskiptamannasniðmátinu verður bætt við lista viðskiptamannasniðmáta þannig að hægt er að nota það til að búa til ný viðskiptamannaspjöld.</span><span class="sxs-lookup"><span data-stu-id="e5273-137">The customer template is added to the list of customer templates, so that you can use it to create new customer cards.</span></span>

## <a name="see-also"></a><span data-ttu-id="e5273-138">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="e5273-138">See Also</span></span>
<span data-ttu-id="e5273-139">[Sala](sales-manage-sales.md)  </span><span class="sxs-lookup"><span data-stu-id="e5273-139">[Sales](sales-manage-sales.md)  </span></span>  
<span data-ttu-id="e5273-140">[Uppsetning sölu](sales-setup-sales.md)  </span><span class="sxs-lookup"><span data-stu-id="e5273-140">[Setting Up Sales](sales-setup-sales.md)  </span></span>  
<span data-ttu-id="e5273-141">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="e5273-141">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

