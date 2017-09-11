---
title: "Notkun á QuickBooks Flutningsviðbót | Microsoft Docs"
description: "Lýsir því hvernig skal nota viðbæturnar til að flytja inn viðskiptamenn, lánardrottna, vörur og reikninga frá Quickbooks Skjáborð til Dynamics 365 for Financials."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, import, implement
ms.date: 03/29/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 37d90316ea0be5489fb5abe33645de3fe0d3cf90
ms.contentlocale: is-is
ms.lasthandoff: 09/11/2017

---
# <a name="the-quickbooks-data-migration-extension-for-dynamics-365-for-financials"></a><span data-ttu-id="3cde5-103">QuickBooks gagnaflutningsviðbótin fyrir Dynamics 365 for Financials</span><span class="sxs-lookup"><span data-stu-id="3cde5-103">The QuickBooks Data Migration Extension for Dynamics 365 for Financials</span></span>
<span data-ttu-id="3cde5-104">Þessi viðbót auðveldar flutning viðskiptamanna, lánardrottna og vara úr QuickBooks í [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="3cde5-104">This extension makes it easy to migrate customers, vendors, items, and accounts from QuickBooks to [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="3cde5-105">Ef fyrirtækið notar QuickBooks er hægt að flytja út viðeigandi upplýsingar og opna síðan leiðarvísi fyrir uppsetningu með hjálp til að hlaða gögnunum upp í [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="3cde5-105">If your business uses QuickBooks today, you can export the relevant information and then open an assisted setup guide to upload the data to [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  
<span data-ttu-id="3cde5-106">Nánari upplýsingar eru í [Innflutningur viðskiptagagna úr öðrum fjárhagskerfum](upload-data.md).</span><span class="sxs-lookup"><span data-stu-id="3cde5-106">For more information, see [Importing Business Data from Other Finance Systems](upload-data.md).</span></span>

## <a name="exporting-data-from-quickbooks"></a><span data-ttu-id="3cde5-107">Útflutningur gagna frá QuickBooks</span><span class="sxs-lookup"><span data-stu-id="3cde5-107">Exporting Data from QuickBooks</span></span>
<span data-ttu-id="3cde5-108">Það þarf að vera búið að flytja suma eða alla viðskiptamenn, lánardrottna og birgðavörur og reikninga sem fyrir eru yfir í skrá á Intuit Interchange sniði (IIF).</span><span class="sxs-lookup"><span data-stu-id="3cde5-108">You must have exported some or all of your existing customers, vendors, inventory items, and accounts to an Intuit Interchange Format (IIF) file.</span></span> <span data-ttu-id="3cde5-109">Viðbótin QuickBooks gagnaflutningar inniheldur sjálfgefna vörpun gagna QuickBooks þannig að þau gögn má nota til að prófa nýja [!INCLUDE[d365fin](includes/d365fin_md.md)] fyrirtækið.</span><span class="sxs-lookup"><span data-stu-id="3cde5-109">The QuickBooks Data Migration extension includes a default mapping of QuickBooks data so that you can use your existing data to test your new [!INCLUDE[d365fin](includes/d365fin_md.md)] company.</span></span> <span data-ttu-id="3cde5-110">Sjálfgefin vörpun er nægileg í langflestum tilfellum en hægt er að breyta vörpun í leiðarvísi fyrir uppsetningu með hjálp.</span><span class="sxs-lookup"><span data-stu-id="3cde5-110">The default mapping will be sufficient in the vast majority of cases, but you can change the mapping in the assisted setup guide.</span></span>  
<span data-ttu-id="3cde5-111">Í QuickBooks felur skráarvalmyndin í sér þann möguleika að flytja út lista.</span><span class="sxs-lookup"><span data-stu-id="3cde5-111">In QuickBooks, the File menu includes a utility to export lists.</span></span> <span data-ttu-id="3cde5-112">Fyrir [!INCLUDE[d365fin](includes/d365fin_md.md)] er hægt að flytja út eftirfarandi lista:</span><span class="sxs-lookup"><span data-stu-id="3cde5-112">For the purposes of [!INCLUDE[d365fin](includes/d365fin_md.md)], you can export the following lists:</span></span>

* <span data-ttu-id="3cde5-113">Viðskiptamannalisti</span><span class="sxs-lookup"><span data-stu-id="3cde5-113">Customer List</span></span>  
* <span data-ttu-id="3cde5-114">Lánardrottnalisti</span><span class="sxs-lookup"><span data-stu-id="3cde5-114">Vendor List</span></span>  
* <span data-ttu-id="3cde5-115">Birgðalisti</span><span class="sxs-lookup"><span data-stu-id="3cde5-115">Item List</span></span>  
* <span data-ttu-id="3cde5-116">Reikningalisti</span><span class="sxs-lookup"><span data-stu-id="3cde5-116">Account List</span></span>  

<span data-ttu-id="3cde5-117">Útfluttu gögnin eru vistuð sem IIF-skrá sem síðan er hægt að hlaða upp í [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="3cde5-117">The exported data is saved as an IIF file that you can then upload to [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

## <a name="see-also"></a><span data-ttu-id="3cde5-118">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="3cde5-118">See Also</span></span>
[<span data-ttu-id="3cde5-119">Innflutningur viðskiptagagna úr öðrum fjárhagskerfum</span><span class="sxs-lookup"><span data-stu-id="3cde5-119">Importing Business Data from Other Finance Systems</span></span>](upload-data.md)  
<span data-ttu-id="3cde5-120">[Sérstilling [!INCLUDE[d365fin](includes/d365fin_md.md)] með viðbótum ](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="3cde5-120">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions ](ui-extensions.md)</span></span>  

