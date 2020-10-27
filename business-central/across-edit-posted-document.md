---
title: Breyta bókuðum sölu- og innkaupaskjölum | Microsoft Docs
description: Kynntu þér mismunandi bókunaraðferðir til að bóka innkaupaskjöl og hvernig hægt er að uppfæra bókuð skjöl.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.reviewer: edupont
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: eedfa2a0c0f519f5ea22eb51a779f6f2a090d9bf
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/01/2020
ms.locfileid: "3914340"
---
# <a name="edit-posted-documents"></a><span data-ttu-id="ab9e8-103">Breyta bókuðum fylgiskjölum</span><span class="sxs-lookup"><span data-stu-id="ab9e8-103">Edit Posted Documents</span></span>

<span data-ttu-id="ab9e8-104">Stundum þarf að uppfæra bókað skjal vegna þess að upplýsingar sem skipta máli fyrir skjalið hafa breyst.</span><span class="sxs-lookup"><span data-stu-id="ab9e8-104">Sometimes you have to update a posted document because information that is relevant to the document has changed.</span></span> <span data-ttu-id="ab9e8-105">Á bókuðu söluskjali getur þetta til dæmis verið rakningarnúmer pakka frá flutningsaðilanum.</span><span class="sxs-lookup"><span data-stu-id="ab9e8-105">On a posted sales document, this can be the shipping agent's package tracking number, for example.</span></span> <span data-ttu-id="ab9e8-106">Á bókuðu innkaupaskjali getur þetta verið texti greiðslutilvísunar.</span><span class="sxs-lookup"><span data-stu-id="ab9e8-106">On a posted purchase document, this can be a payment reference text.</span></span>

<span data-ttu-id="ab9e8-107">Þú framkvæmir breytinguna í breytanlegri útgáfu af upprunalega skjalinu, sem er merkt með „ **- Uppfæra** “ í titli síðunnar.</span><span class="sxs-lookup"><span data-stu-id="ab9e8-107">You perform the change on an editable version of the original document, indicated by " **- Update** " in the page title.</span></span> <span data-ttu-id="ab9e8-108">Síðan inniheldur undirsafn reitanna úr upprunalega skjalinu, þar sem sumir reitir eru óbreytanlegir og aðeins sýndir til upplýsingar.</span><span class="sxs-lookup"><span data-stu-id="ab9e8-108">The page contains a subset of the fields on the original document, of which some are non-editable fields that are shown for information only.</span></span>

<span data-ttu-id="ab9e8-109">Virknin er í boði fyrir eftirfarandi skjöl á öllum studdum mörkuðum:</span><span class="sxs-lookup"><span data-stu-id="ab9e8-109">The functionality is available for the following documents across all supported markets:</span></span>

- <span data-ttu-id="ab9e8-110">Bókuð söluafhending</span><span class="sxs-lookup"><span data-stu-id="ab9e8-110">Posted Sales Shipment</span></span>
- <span data-ttu-id="ab9e8-111">Bókaður innkaupareikningur</span><span class="sxs-lookup"><span data-stu-id="ab9e8-111">Posted Purchase Invoice</span></span>
- <span data-ttu-id="ab9e8-112">Bókuð skilaafhending</span><span class="sxs-lookup"><span data-stu-id="ab9e8-112">Posted Return Shipment</span></span>
- <span data-ttu-id="ab9e8-113">Bókuð vöruskilamóttaka</span><span class="sxs-lookup"><span data-stu-id="ab9e8-113">Posted Return Receipt</span></span>

<span data-ttu-id="ab9e8-114">Eftirfarandi viðbótarskjölum er hægt að breyta í tilteknum löndum eða svæðum:</span><span class="sxs-lookup"><span data-stu-id="ab9e8-114">The following additional documents can be edited in the specified countries or regions:</span></span>

- <span data-ttu-id="ab9e8-115">ES: Bókaður sölureikningur, bókaður sölukreditreikningur, bókaður innkaupakreditreikningur</span><span class="sxs-lookup"><span data-stu-id="ab9e8-115">ES: Posted Sales Invoice, Posted Sales Credit Memo, Posted Purchase Credit Memo</span></span>
- <span data-ttu-id="ab9e8-116">APAC: Bókaður sölukreditreikningur, bókaður innkaupakreditreikningur</span><span class="sxs-lookup"><span data-stu-id="ab9e8-116">APAC: Posted Sales Credit Memo, Posted Purchase Credit Memo</span></span>
- <span data-ttu-id="ab9e8-117">RU: Bókaður sölukreditreikningur</span><span class="sxs-lookup"><span data-stu-id="ab9e8-117">RU: Posted Sales Credit Memo</span></span>
- <span data-ttu-id="ab9e8-118">IT: Bókuð millifærsluafhending, bókuð þjónustuafhending</span><span class="sxs-lookup"><span data-stu-id="ab9e8-118">IT: Posted Transfer Shipment, Posted Service Shipment</span></span>

## <a name="to-edit-a-posted-sales-shipment"></a><span data-ttu-id="ab9e8-119">Breyta bókaðri söluafhendingu</span><span class="sxs-lookup"><span data-stu-id="ab9e8-119">To edit a posted sales shipment</span></span>

<span data-ttu-id="ab9e8-120">Eftirfarandi útskýrir hvernig á að breyta bókaðri söluafhendingu.</span><span class="sxs-lookup"><span data-stu-id="ab9e8-120">The following explains how to edit a posted sales shipment.</span></span> <span data-ttu-id="ab9e8-121">Skrefin eru svipuð í hinum studdu skjölunum.</span><span class="sxs-lookup"><span data-stu-id="ab9e8-121">The steps are similar for the other supported documents.</span></span>

1. <span data-ttu-id="ab9e8-122">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Bókaðar söluafhendingar** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="ab9e8-122">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Posted Sales Shipments** , and then choose the related link.</span></span>
2. <span data-ttu-id="ab9e8-123">Veldu skjalið sem á að breyta og síðan aðgerðina **Uppfæra skjal** .</span><span class="sxs-lookup"><span data-stu-id="ab9e8-123">Select the document that you want to edit, and then choose the **Update Document** action.</span></span> <span data-ttu-id="ab9e8-124">Að öðrum kosti skaltu opna skjalið og velja síðan aðgerðina.</span><span class="sxs-lookup"><span data-stu-id="ab9e8-124">Alternatively, open the document and then choose the action.</span></span>
3. <span data-ttu-id="ab9e8-125">Á síðunni **Bókuð söluafhending - uppfæra** skaltu breyta **Rakningarnr. pakka**</span><span class="sxs-lookup"><span data-stu-id="ab9e8-125">On the **Posted Sales Shipment - Update** page, edit the **Package Tracking No.**</span></span> <span data-ttu-id="ab9e8-126">reitnum, sem dæmi.</span><span class="sxs-lookup"><span data-stu-id="ab9e8-126">field, for example.</span></span>
4. <span data-ttu-id="ab9e8-127">Velja hnappinn **Í lagi** .</span><span class="sxs-lookup"><span data-stu-id="ab9e8-127">Choose the **OK** button.</span></span>

<span data-ttu-id="ab9e8-128">Bókuð söluafhending er uppfærð.</span><span class="sxs-lookup"><span data-stu-id="ab9e8-128">The posted sales shipment is updated.</span></span>

## <a name="see-also"></a><span data-ttu-id="ab9e8-129">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="ab9e8-129">See Also</span></span>

[<span data-ttu-id="ab9e8-130">Almenn viðskiptavirkni</span><span class="sxs-lookup"><span data-stu-id="ab9e8-130">General Business Functionality</span></span>](ui-across-business-areas.md)  
[<span data-ttu-id="ab9e8-131">Innkaup</span><span class="sxs-lookup"><span data-stu-id="ab9e8-131">Purchasing</span></span>](purchasing-manage-purchasing.md)  
[<span data-ttu-id="ab9e8-132">Bókun skjala og færslubóka</span><span class="sxs-lookup"><span data-stu-id="ab9e8-132">Posting Documents and Journals</span></span>](ui-post-documents-journals.md)  
<span data-ttu-id="ab9e8-133">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="ab9e8-133">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
