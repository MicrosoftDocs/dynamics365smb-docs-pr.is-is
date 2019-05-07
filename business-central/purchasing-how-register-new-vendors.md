---
title: Stofna lánardrottnaspjald til að skrá nýjan lánardrottinn | Microsoft Docs
description: Kynntu þér hvernig skal stofna lánadrottnaspjald til að skrá nýjan lánardrottinn eða birgja.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: supplier
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 9f388b788e8788049ee30567972090984063cad1
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2019
ms.locfileid: "930356"
---
# <a name="register-new-vendors"></a><span data-ttu-id="021b5-103">Skráning nýrra lánardrottna</span><span class="sxs-lookup"><span data-stu-id="021b5-103">Register New Vendors</span></span>
<span data-ttu-id="021b5-104">Lánardrottnar veita vörurnar sem selja á.</span><span class="sxs-lookup"><span data-stu-id="021b5-104">Vendors provide the products that you sell.</span></span> <span data-ttu-id="021b5-105">Hver lánardrottinn sem keypt er frá verður að vera skráður sem lánardrottnaspjald.</span><span class="sxs-lookup"><span data-stu-id="021b5-105">Each vendor that you purchase from must be registered as a vendor card.</span></span>

<span data-ttu-id="021b5-106">Áður en hægt er að skrá nýja lánardrottna þarf að setja upp ýmsar innkaupakóða sem hægt er að velja úr þegar fyllt eru út lánardrottnaspjöld.</span><span class="sxs-lookup"><span data-stu-id="021b5-106">Before you can register new vendors, you must set up various purchase codes that you can select from when you fill vendor cards.</span></span> <span data-ttu-id="021b5-107">Þegar búið er að setja inn öll nauðsynleg höfuðgögn er hægt að grunnstilla lánardrottininn frekar, s.s. að forgangsraða lánardrottninum vegna greiðslna og gera lista yfir vörur sem lánardrottinninn og aðrir lánardrottnar geta útvegað.</span><span class="sxs-lookup"><span data-stu-id="021b5-107">When all of the required master data is created, you can perform additional configuration of the vendor, such as prioritize the vendor for payment purposes and list items that the vendor and other vendors can supply.</span></span> <span data-ttu-id="021b5-108">Annar flokkur uppsetningarverkhluta fyrir lánardrottna er að skrá samninga varðandi afslætti, verð og greiðsluaðferðir.</span><span class="sxs-lookup"><span data-stu-id="021b5-108">Another group of setup tasks for vendors is to record your agreements concerning discounts, prices, and payment methods.</span></span> <span data-ttu-id="021b5-109">Nánari upplýsingar er að finna í [Uppsetning innkaupa](purchasing-setup-purchasing.md).</span><span class="sxs-lookup"><span data-stu-id="021b5-109">For more information, see [Setting Up Purchasing](purchasing-setup-purchasing.md).</span></span>

<span data-ttu-id="021b5-110">Lánardrottnaspjöld geyma upplýsingarnar sem þarf til að kaupa vörur frá lánardrottninum.</span><span class="sxs-lookup"><span data-stu-id="021b5-110">Vendor cards hold the information that is required to buy products from the vendor.</span></span> <span data-ttu-id="021b5-111">Frekari upplýsingar eru í [Skrá innkaup](purchasing-how-record-purchases.md) og [Skrá nýja hluti](inventory-how-register-new-items.md).</span><span class="sxs-lookup"><span data-stu-id="021b5-111">For more information, see [Record Purchases](purchasing-how-record-purchases.md) and [Register New Items](inventory-how-register-new-items.md).</span></span>

> [!NOTE]  
>   <span data-ttu-id="021b5-112">Ef lánardrottnasniðmát er til fyrir mismunandi tegundir lánardrottna, þá birtist síða þegar búið er til nýtt lánardrottnaspjald þar sem hægt er að velja viðeigandi sniðmát.</span><span class="sxs-lookup"><span data-stu-id="021b5-112">If vendor templates exist for different vendor types, then a page appears when you create a new vendor card from where you can select an appropriate template.</span></span> <span data-ttu-id="021b5-113">Ef aðeins eitt lánardrottnasniðmát er fyrir hendi, nota ný lánardrottnaspjöld alltaf það sniðmát.</span><span class="sxs-lookup"><span data-stu-id="021b5-113">If only one vendor template exists, then new vendor cards always use that template.</span></span>

## <a name="to-create-a-new-vendor-card"></a><span data-ttu-id="021b5-114">Að búa til nýtt lánardrottnaspjald.</span><span class="sxs-lookup"><span data-stu-id="021b5-114">To create a new vendor card</span></span>
1. <span data-ttu-id="021b5-115">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **lánardrottnar** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="021b5-115">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Vendors**, and then choose the related link.</span></span>  
2. <span data-ttu-id="021b5-116">Á síðunni **Lánardrottnar** skal velja **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="021b5-116">On the **Vendors** page, Choose **New**.</span></span>

    <span data-ttu-id="021b5-117">Ef fleiri en eitt lánardrottnasniðmát er fyrir hendi, þá birtist sjálfkrafa síða með tiltækum lánardrottnasniðmátum.</span><span class="sxs-lookup"><span data-stu-id="021b5-117">If more than one vendor template exists, then a page opens from which you can select a vendor template.</span></span> <span data-ttu-id="021b5-118">Í því tilviki, fylgið næstu tveimur skrefum.</span><span class="sxs-lookup"><span data-stu-id="021b5-118">In that case, follow the next two steps.</span></span>
3. <span data-ttu-id="021b5-119">Á síðunni **Velja sniðmát fyrir nýjan lánardrottin** er valið sniðmátið sem á að nota fyrir nýja lánardrottnaspjaldið.</span><span class="sxs-lookup"><span data-stu-id="021b5-119">On the **Select a template for a new vendor** page, choose the template that you want to use for the new vendor card.</span></span>
4. <span data-ttu-id="021b5-120">Velja hnappinn **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="021b5-120">Choose the **OK** button.</span></span> <span data-ttu-id="021b5-121">Nýtt lánardrottnaspjald opnast þar sem búið er að fylla upplýsingar úr sniðmátinu inn í hluta reitanna.</span><span class="sxs-lookup"><span data-stu-id="021b5-121">A new vendor card opens with some fields filled with information from the template.</span></span>
5. <span data-ttu-id="021b5-122">Því næst eru reitir á lánardrottnaspjaldinu færðir inn eða þeim breytt eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="021b5-122">Proceed to fill or change fields on the vendor card as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
>   <span data-ttu-id="021b5-123">Ef ekki er vitað reikningsaðsetur sem verður notað fyrir hvern reikning frá lánardrottni skal ekki færa í reitinn **Borga**.</span><span class="sxs-lookup"><span data-stu-id="021b5-123">If you do not know the invoicing address that will be used for every invoice from a vendor, do not fill in the **Pay-to** field.</span></span> <span data-ttu-id="021b5-124">Þess í stað skal velja borga-lánardrottni númer eftir að hafa sett upp innkaupabeiðni, pöntun eða reikningshaus.</span><span class="sxs-lookup"><span data-stu-id="021b5-124">Instead, choose the pay-to vendor number after you have set up a purchase quote, order, or invoice header.</span></span>

<span data-ttu-id="021b5-125">Nú hefur lánardrottinn verið skráður og lánardrottnaspjaldið má nú nota í innkaupaskjölum.</span><span class="sxs-lookup"><span data-stu-id="021b5-125">The vendor is now registered, and the vendor card is ready to be used on purchase documents.</span></span>

<span data-ttu-id="021b5-126">Ef nota á þetta lánardrottnaspjald sem sniðmát þegar ný lánardrottnaspjöld eru búin til, vistið það sem lánardrottnasniðmát.</span><span class="sxs-lookup"><span data-stu-id="021b5-126">If you want to use this vendor card as a template when you create new vendor cards, you can save it as a vendor template.</span></span> <span data-ttu-id="021b5-127">Nánari upplýsingar eru í eftirfarandi kafla.</span><span class="sxs-lookup"><span data-stu-id="021b5-127">For more information, see the following section.</span></span>

## <a name="to-save-the-vendor-card-as-a-template"></a><span data-ttu-id="021b5-128">Að vista lánardrottnaspjaldið sem sniðmát</span><span class="sxs-lookup"><span data-stu-id="021b5-128">To save the vendor card as a template</span></span>
1. <span data-ttu-id="021b5-129">Á síðunni **Lánardrottnaspjald** er valin aðgerðin **Vista sem sniðmát**.</span><span class="sxs-lookup"><span data-stu-id="021b5-129">On the **Vendor Card** page, choose the **Save as Template** action.</span></span> <span data-ttu-id="021b5-130">Síðan **Lánardrottnasniðmát** opnast og sýnir lánardrottnaspjaldið sem sniðmát.</span><span class="sxs-lookup"><span data-stu-id="021b5-130">The **Vendor Template** page opens showing the vendor card as a template.</span></span>
2. <span data-ttu-id="021b5-131">Fyllið inn reitina eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="021b5-131">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="021b5-132">Til að endurnota víddir í sniðmátum, veljið aðgerðina **Víddir**.</span><span class="sxs-lookup"><span data-stu-id="021b5-132">To reuse dimensions in templates, choose the **Dimensions** action.</span></span> <span data-ttu-id="021b5-133">Síðan **Víddarsniðmát** opnast og sýnir alla víddarkóða sem settir eru upp fyrir lánardrottin.</span><span class="sxs-lookup"><span data-stu-id="021b5-133">The **Dimension Templates** page opens showing any dimension codes that are set up for the vendor.</span></span>
4. <span data-ttu-id="021b5-134">Breyta eða færa inn víddarkóða sem munu gilda fyrir ný lánardrottnaspjöld sem stofnuð eru með sniðmátinu.</span><span class="sxs-lookup"><span data-stu-id="021b5-134">Edit or enter dimension codes that will apply to new vendor cards created by using the template.</span></span>
5. <span data-ttu-id="021b5-135">Þegar lokið hefur verið við nýja lánardrottnasniðmátið skal velja hnappinn **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="021b5-135">When you have completed the new vendor template, choose the **OK** button.</span></span>  
   <span data-ttu-id="021b5-136">Lánardrottnasniðmátinu verður bætt við lista lánardrottnasniðmáta þannig að hægt er að nota það til að búa til ný lánardrottnaspjöld.</span><span class="sxs-lookup"><span data-stu-id="021b5-136">The vendor template is added to the list of vendor templates, so that you can use it to create new vendor cards.</span></span>

## <a name="see-also"></a><span data-ttu-id="021b5-137">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="021b5-137">See Also</span></span>
[<span data-ttu-id="021b5-138">Sameina tvítekin atriði</span><span class="sxs-lookup"><span data-stu-id="021b5-138">Merge Duplicate Records</span></span>](sales-how-merge-duplicate-records.md)  
[<span data-ttu-id="021b5-139">Stofnun númeraraða</span><span class="sxs-lookup"><span data-stu-id="021b5-139">Create Number Series</span></span>](ui-create-number-series.md)  
[<span data-ttu-id="021b5-140">Innkaup</span><span class="sxs-lookup"><span data-stu-id="021b5-140">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="021b5-141">[Skrá innkaup](purchasing-how-record-purchases.md) </span><span class="sxs-lookup"><span data-stu-id="021b5-141">[Record Purchases](purchasing-how-record-purchases.md) </span></span>  
<span data-ttu-id="021b5-142">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="021b5-142">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
