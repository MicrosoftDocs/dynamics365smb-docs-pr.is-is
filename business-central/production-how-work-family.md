---
title: "Hvernig á að nota vörusamsafn í framleiðslu | Microsoft Docs"
description: "Þegar grunndagatal er sérsniðið fyrir fyrirtækið eða einhvern viðskiptafélaga eru breytingar á frídögum og virkum dögum færðar inn."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 11/05/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: c3cb9f82688f89f00f934d1468492cfa752742fd
ms.contentlocale: is-is
ms.lasthandoff: 11/26/2018

---
# <a name="work-with-production-families"></a><span data-ttu-id="e4e81-103">Vinna með framleiðslusamsafn</span><span class="sxs-lookup"><span data-stu-id="e4e81-103">Work with Production Families</span></span>
<span data-ttu-id="e4e81-104">Framleiðslusamsafn er hópur einstakra vara sem byggðar eru á líku framleiðsluferli.</span><span class="sxs-lookup"><span data-stu-id="e4e81-104">A production family is a group of individual items whose relationship is based on the similarity of their manufacturing processes.</span></span> <span data-ttu-id="e4e81-105">Með því að mynda framleiðslusamsöfn er hægt að framleiða sumar vörur tvisvar eða oftar í einni vinnslu, en þetta fínstillir efnisnotkun.</span><span class="sxs-lookup"><span data-stu-id="e4e81-105">By forming production families, some items can be manufactured twice or more in one production, which will optimize material consumption.</span></span>

<span data-ttu-id="e4e81-106">Í reit **Magn** á síðunni **Samsafn** er fært inn magnið sem framleitt hefur verið þegar allt samsafnið hefur verið framleitt einu sinni.</span><span class="sxs-lookup"><span data-stu-id="e4e81-106">In the **Quantity** field on the **Family** page, you enter the quantity that will be produced when the whole family has been manufactured once.</span></span>

## <a name="example"></a><span data-ttu-id="e4e81-107">Dæmi</span><span class="sxs-lookup"><span data-stu-id="e4e81-107">Example</span></span>
<span data-ttu-id="e4e81-108">Við stönsun er hægt að framleiða fjögur stykki af sömu vörunni úr einni plötu og 10 stykki af annarri, ólíkri vöru, á sama tíma.</span><span class="sxs-lookup"><span data-stu-id="e4e81-108">In punching processes, four pieces of the same item can be produced from one sheet and 10 pieces of another, different, item at the same time.</span></span> <span data-ttu-id="e4e81-109">Stansvélin mótar öll 14 stykkin í einu þrepi.</span><span class="sxs-lookup"><span data-stu-id="e4e81-109">The punching machine will punch all 14 pieces in one step.</span></span>

<span data-ttu-id="e4e81-110">Stofnun framleiðslusamsafna dregur úr úrkastsmagninu vegna þess að það sem myndi venjulega vera afgangsúrkast, við framleiðslu stærri stykkja, er í staðinn notað til að framleiða minni hluti.</span><span class="sxs-lookup"><span data-stu-id="e4e81-110">Forming production families reduces the scrap quantity because what would normally be leftover scrap, when producing big pieces, will be used instead to produce small items.</span></span>

## <a name="to-set-up-a-production-family"></a><span data-ttu-id="e4e81-111">Uppsetning framleiðslusamsafns</span><span class="sxs-lookup"><span data-stu-id="e4e81-111">To set up a production family</span></span>
1. <span data-ttu-id="e4e81-112">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Fjölskyldur** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="e4e81-112">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Families**, and then choose the related link.</span></span>
2. <span data-ttu-id="e4e81-113">Fyllið inn reitina eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="e4e81-113">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-produce-based-on-a-production-family"></a><span data-ttu-id="e4e81-114">Framleiðsla byggt á framleiðslusamsafni</span><span class="sxs-lookup"><span data-stu-id="e4e81-114">To produce based on a production family</span></span>
1. <span data-ttu-id="e4e81-115">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Fastáætluð framl.pantanir** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="e4e81-115">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Firm Planned Prod. Orders**, and then choose the related link.</span></span>
2. <span data-ttu-id="e4e81-116">Stofna nýja framleiðslupöntun</span><span class="sxs-lookup"><span data-stu-id="e4e81-116">Create a new production order.</span></span> <span data-ttu-id="e4e81-117">Frekari upplýsingar eru í [Stofna framleiðslupantanir](production-how-to-create-production-orders.md).</span><span class="sxs-lookup"><span data-stu-id="e4e81-117">For more information, see [Create Production orders](production-how-to-create-production-orders.md).</span></span>
3. <span data-ttu-id="e4e81-118">Í reitnum **Gerð uppruna**, veljið **Samsafn**.</span><span class="sxs-lookup"><span data-stu-id="e4e81-118">In the **Source Type** field, select **Family**.</span></span>  
4. <span data-ttu-id="e4e81-119">Í reitnum **Forðanr.** er viðeigandi framleiðslusamsafn valið.</span><span class="sxs-lookup"><span data-stu-id="e4e81-119">In the **Source No.** field, select the relevant production family.</span></span>

## <a name="see-also"></a><span data-ttu-id="e4e81-120">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="e4e81-120">See Also</span></span>
[<span data-ttu-id="e4e81-121">Búa til framleiðsluuppskriftir</span><span class="sxs-lookup"><span data-stu-id="e4e81-121">Create Production BOMs</span></span>](production-how-to-create-production-boms.md)  
[<span data-ttu-id="e4e81-122">Uppsetning framleiðslu</span><span class="sxs-lookup"><span data-stu-id="e4e81-122">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="e4e81-123">[Framleiðsla](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="e4e81-123">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
<span data-ttu-id="e4e81-124">[Áætlun](production-planning.md) </span><span class="sxs-lookup"><span data-stu-id="e4e81-124">[Planning](production-planning.md) </span></span>  
[<span data-ttu-id="e4e81-125">Birgðir</span><span class="sxs-lookup"><span data-stu-id="e4e81-125">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="e4e81-126">Innkaup</span><span class="sxs-lookup"><span data-stu-id="e4e81-126">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="e4e81-127">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="e4e81-127">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

