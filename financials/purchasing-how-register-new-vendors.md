---
title: "Stofna lánardrottnaspjald til að skrá nýjan lánardrottinn | Microsoft Docs"
description: "Kynntu þér hvernig skal stofna lánadrottnaspjald til að skrá nýjan lánardrottinn eða birgja."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: supplier
ms.date: 03/29/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 78710d796ed73d7b4c2505f6cbb8c7d5f41d7320
ms.contentlocale: is-is
ms.lasthandoff: 09/11/2017

---
# <a name="how-to-register-new-vendors"></a><span data-ttu-id="e0298-103">Hvernig á að Skrá nýja lánardrottna</span><span class="sxs-lookup"><span data-stu-id="e0298-103">How to: Register New Vendors</span></span>
<span data-ttu-id="e0298-104">Lánardrottnar veita vörurnar sem selja á.</span><span class="sxs-lookup"><span data-stu-id="e0298-104">Vendors provide the products that you sell.</span></span> <span data-ttu-id="e0298-105">Hver lánardrottinn sem keypt er frá verður að vera skráður sem lánardrottnaspjald.</span><span class="sxs-lookup"><span data-stu-id="e0298-105">Each vendor that you purchase from must be registered as a vendor card.</span></span>

<span data-ttu-id="e0298-106">Áður en hægt er að skrá nýja lánardrottna þarf að setja upp ýmsar innkaupakóða sem hægt er að velja úr þegar fyllt eru út lánardrottnaspjöld.</span><span class="sxs-lookup"><span data-stu-id="e0298-106">Before you can register new vendors, you must set up various purchase codes that you can select from when you fill vendor cards.</span></span> <span data-ttu-id="e0298-107">Þegar búið er að setja inn öll nauðsynleg höfuðgögn er hægt að grunnstilla lánardrottininn frekar, s.s. að forgangsraða lánardrottninum vegna greiðslna og gera lista yfir vörur sem lánardrottinninn og aðrir lánardrottnar geta útvegað.</span><span class="sxs-lookup"><span data-stu-id="e0298-107">When all of the required master data is created, you can perform additional configuration of the vendor, such as prioritize the vendor for payment purposes and list items that the vendor and other vendors can supply.</span></span> <span data-ttu-id="e0298-108">Annar flokkur uppsetningarverkhluta fyrir lánardrottna er að skrá samninga varðandi afslætti, verð og greiðsluaðferðir.</span><span class="sxs-lookup"><span data-stu-id="e0298-108">Another group of setup tasks for vendors is to record your agreements concerning discounts, prices, and payment methods.</span></span> <span data-ttu-id="e0298-109">Nánari upplýsingar er að finna í [Uppsetning innkaupa](purchasing-setup-purchasing.md).</span><span class="sxs-lookup"><span data-stu-id="e0298-109">For more information, see [Setting Up Purchasing](purchasing-setup-purchasing.md).</span></span>

<span data-ttu-id="e0298-110">Lánardrottnaspjöld geyma upplýsingarnar sem þarf til að kaupa vörur frá lánardrottninum.</span><span class="sxs-lookup"><span data-stu-id="e0298-110">Vendor cards hold the information that is required to buy products from the vendor.</span></span> <span data-ttu-id="e0298-111">Nánari upplýsingar er að finna í [Hvernig á að: Skráðu inn kaup](purchasing-how-record-purchases.md) og [Hvernig á að: Skráðu nýja hluti](inventory-how-register-new-items.md).</span><span class="sxs-lookup"><span data-stu-id="e0298-111">For more information, see [How to: Record Purchases](purchasing-how-record-purchases.md) and [How to: Register New Items](inventory-how-register-new-items.md).</span></span>

> [!NOTE]  
>   <span data-ttu-id="e0298-112">Ef lánardrottnasniðmát er til fyrir mismunandi tegundir lánardrottna, þá birtist sjálfkrafa gluggi þegar búið er til nýtt lánardrottnaspjald þar sem hægt er að velja viðeigandi lánardrottnasniðmát.</span><span class="sxs-lookup"><span data-stu-id="e0298-112">If vendor templates exist for different vendor types, then a window appears when you create a new vendor card from where you can select an appropriate template.</span></span> <span data-ttu-id="e0298-113">Ef aðeins eitt lánardrottnasniðmát er fyrir hendi, nota ný lánardrottnaspjöld alltaf það sniðmát.</span><span class="sxs-lookup"><span data-stu-id="e0298-113">If only one vendor template exists, then new vendor cards always use that template.</span></span>

## <a name="to-create-a-new-vendor-card"></a><span data-ttu-id="e0298-114">Að búa til nýtt lánardrottnaspjald.</span><span class="sxs-lookup"><span data-stu-id="e0298-114">To create a new vendor card</span></span>
1. <span data-ttu-id="e0298-115">Á heimasíðunni skal velja **Lánardrottnar** til að opna listann yfir núverandi lánardrottnaspjöld.</span><span class="sxs-lookup"><span data-stu-id="e0298-115">On the Home page, choose **Vendors** to open the list of existing vendors.</span></span>  
2. <span data-ttu-id="e0298-116">Í glugganum **Lánardrottnar** skal velja **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="e0298-116">In the **Vendors** window, Choose **New**.</span></span>

    <span data-ttu-id="e0298-117">Ef fleiri en eitt lánardrottnasniðmát er fyrir hendi, þá birtist sjálfkrafa gluggi með tiltækum lánardrottnasniðmátum.</span><span class="sxs-lookup"><span data-stu-id="e0298-117">If more than one vendor template exists, then a window opens from which you can select a vendor template.</span></span> <span data-ttu-id="e0298-118">Í því tilviki, fylgið næstu tveimur skrefum.</span><span class="sxs-lookup"><span data-stu-id="e0298-118">In that case, follow the next two steps.</span></span>
3. <span data-ttu-id="e0298-119">Í glugganum **Velja sniðmát fyrir nýjan lánardrottin** er valið sniðmátið sem á að nota fyrir nýja lánardrottnaspjaldið.</span><span class="sxs-lookup"><span data-stu-id="e0298-119">In the **Select a template for a new vendor** window, choose the template that you want to use for the new vendor card.</span></span>
4. <span data-ttu-id="e0298-120">Velja hnappinn **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="e0298-120">Choose the **OK** button.</span></span> <span data-ttu-id="e0298-121">Nýtt lánardrottnaspjald opnast þar sem búið er að fylla upplýsingar úr sniðmátinu inn í hluta reitanna.</span><span class="sxs-lookup"><span data-stu-id="e0298-121">A new vendor card opens with some fields filled with information from the template.</span></span>
5. <span data-ttu-id="e0298-122">Því næst eru reitir á lánardrottnaspjaldinu færðir inn eða þeim breytt eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="e0298-122">Proceed to fill or change fields on the vendor card as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

<span data-ttu-id="e0298-123">Nú hefur lánardrottinn verið skráður og lánardrottnaspjaldið má nú nota í innkaupaskjölum.</span><span class="sxs-lookup"><span data-stu-id="e0298-123">The vendor is now registered, and the vendor card is ready to be used on purchase documents.</span></span>

<span data-ttu-id="e0298-124">Ef nota á þetta lánardrottnaspjald sem sniðmát þegar ný lánardrottnaspjöld eru búin til, vistið það sem lánardrottnasniðmát.</span><span class="sxs-lookup"><span data-stu-id="e0298-124">If you want to use this vendor card as a template when you create new vendor cards, you can save it as a vendor template.</span></span> <span data-ttu-id="e0298-125">Nánari upplýsingar eru í eftirfarandi kafla.</span><span class="sxs-lookup"><span data-stu-id="e0298-125">For more information, see the following section.</span></span>

## <a name="to-save-the-vendor-card-as-a-template"></a><span data-ttu-id="e0298-126">Að vista lánardrottnaspjaldið sem sniðmát</span><span class="sxs-lookup"><span data-stu-id="e0298-126">To save the vendor card as a template</span></span>
1. <span data-ttu-id="e0298-127">Í glugganum **Lánardrottnaspjald** er valin aðgerðin **Vista sem sniðmát**.</span><span class="sxs-lookup"><span data-stu-id="e0298-127">In the **Vendor Card** window, choose the **Save as Template** action.</span></span> <span data-ttu-id="e0298-128">Glugginn **Lánardrottnasniðmát** opnast og sýnir lánardrottnaspjaldið sem sniðmát.</span><span class="sxs-lookup"><span data-stu-id="e0298-128">The **Vendor Template** window opens showing the vendor card as a template.</span></span>
2. <span data-ttu-id="e0298-129">Fyllið inn í svæðin eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="e0298-129">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="e0298-130">Til að endurnota víddir í sniðmátum, veljið aðgerðina **Víddir**.</span><span class="sxs-lookup"><span data-stu-id="e0298-130">To reuse dimensions in templates, choose the **Dimensions** action.</span></span> <span data-ttu-id="e0298-131">Glugginn **Víddarsniðmát** opnast og sýnir alla víddarkóða sem settir eru upp fyrir lánardrottin.</span><span class="sxs-lookup"><span data-stu-id="e0298-131">The **Dimension Templates** window opens showing any dimension codes that are set up for the vendor.</span></span>
4. <span data-ttu-id="e0298-132">Breyta eða færa inn víddarkóða sem munu gilda fyrir ný lánardrottnaspjöld sem stofnuð eru með sniðmátinu.</span><span class="sxs-lookup"><span data-stu-id="e0298-132">Edit or enter dimension codes that will apply to new vendor cards created by using the template.</span></span>
5. <span data-ttu-id="e0298-133">Þegar lokið hefur verið við nýja lánardrottnasniðmátið skal velja hnappinn **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="e0298-133">When you have completed the new vendor template, choose the **OK** button.</span></span>  
   <span data-ttu-id="e0298-134">Lánardrottnasniðmátinu verður bætt við lista lánardrottnasniðmáta þannig að hægt er að nota það til að búa til ný lánardrottnaspjöld.</span><span class="sxs-lookup"><span data-stu-id="e0298-134">The vendor template is added to the list of vendor templates, so that you can use it to create new vendor cards.</span></span>

## <a name="see-also"></a><span data-ttu-id="e0298-135">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="e0298-135">See Also</span></span>
[<span data-ttu-id="e0298-136">Innkaup</span><span class="sxs-lookup"><span data-stu-id="e0298-136">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="e0298-137">[Hvernig á að skrá kaup](purchasing-how-record-purchases.md) </span><span class="sxs-lookup"><span data-stu-id="e0298-137">[How to: Record Purchases](purchasing-how-record-purchases.md) </span></span>  
<span data-ttu-id="e0298-138">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="e0298-138">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

