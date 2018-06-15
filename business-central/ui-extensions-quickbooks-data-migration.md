---
title: "Notkun á QuickBooks Flutningsviðbót | Microsoft Docs"
description: "Lýsir því hvernig skal nota viðbæturnar til að flytja inn viðskiptamenn, lánardrottna, vörur og reikninga frá QuickBooks Desktop til Business Central."
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, import, implement
ms.date: 03/29/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: ad1b888d475c0523c5a905e804a3f89ab4531b28
ms.openlocfilehash: c7348ff75e2f9660611d0d2aed0fa1beacfa259c
ms.contentlocale: is-is
ms.lasthandoff: 05/17/2018

---
# <a name="the-quickbooks-data-migration-extension-for-business-central"></a><span data-ttu-id="24aa7-103">Viðbótin QuickBooks gagnaflutningar í Business Central</span><span class="sxs-lookup"><span data-stu-id="24aa7-103">The QuickBooks Data Migration Extension for Business Central</span></span>
<span data-ttu-id="24aa7-104">Þessi viðbót auðveldar flutning viðskiptamanna, lánardrottna og vara úr QuickBooks í [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="24aa7-104">This extension makes it easy to migrate customers, vendors, items, and accounts from QuickBooks to [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="24aa7-105">Ef fyrirtækið notar QuickBooks er hægt að flytja út viðeigandi upplýsingar og opna síðan leiðarvísi fyrir uppsetningu með hjálp til að hlaða gögnunum upp í [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="24aa7-105">If your business uses QuickBooks today, you can export the relevant information and then open an assisted setup guide to upload the data to [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  
<span data-ttu-id="24aa7-106">Nánari upplýsingar eru í [Innflutningur viðskiptagagna úr öðrum fjárhagskerfum](across-import-data-configuration-packages.md).</span><span class="sxs-lookup"><span data-stu-id="24aa7-106">For more information, see [Importing Business Data from Other Finance Systems](across-import-data-configuration-packages.md).</span></span>

## <a name="exporting-data-from-quickbooks-desktop"></a><span data-ttu-id="24aa7-107">Útflutningur gagna frá QuickBooks Desktop</span><span class="sxs-lookup"><span data-stu-id="24aa7-107">Exporting Data from QuickBooks Desktop</span></span>
<span data-ttu-id="24aa7-108">Það þarf að vera búið að flytja suma eða alla viðskiptamenn, lánardrottna og birgðavörur og reikninga sem fyrir eru yfir í skrá á Intuit Interchange sniði (IIF).</span><span class="sxs-lookup"><span data-stu-id="24aa7-108">You must have exported some or all of your existing customers, vendors, inventory items, and accounts to an Intuit Interchange Format (IIF) file.</span></span> <span data-ttu-id="24aa7-109">Viðbótin QuickBooks gagnaflutningar inniheldur sjálfgefna vörpun gagna QuickBooks þannig að þau gögn má nota til að prófa nýja [!INCLUDE[d365fin](includes/d365fin_md.md)] fyrirtækið.</span><span class="sxs-lookup"><span data-stu-id="24aa7-109">The QuickBooks Data Migration extension includes a default mapping of QuickBooks data so that you can use your existing data to test your new [!INCLUDE[d365fin](includes/d365fin_md.md)] company.</span></span> <span data-ttu-id="24aa7-110">Sjálfgefin vörpun er nægileg í langflestum tilfellum en hægt er að breyta vörpun í leiðarvísi fyrir uppsetningu með hjálp.</span><span class="sxs-lookup"><span data-stu-id="24aa7-110">The default mapping will be sufficient in the vast majority of cases, but you can change the mapping in the assisted setup guide.</span></span>  
<span data-ttu-id="24aa7-111">Í QuickBooks felur skráarvalmyndin í sér þann möguleika að flytja út lista.</span><span class="sxs-lookup"><span data-stu-id="24aa7-111">In QuickBooks, the File menu includes a utility to export lists.</span></span> <span data-ttu-id="24aa7-112">Fyrir [!INCLUDE[d365fin](includes/d365fin_md.md)] er hægt að flytja út eftirfarandi lista:</span><span class="sxs-lookup"><span data-stu-id="24aa7-112">For the purposes of [!INCLUDE[d365fin](includes/d365fin_md.md)], you can export the following lists:</span></span>

* <span data-ttu-id="24aa7-113">Viðskiptamannalisti</span><span class="sxs-lookup"><span data-stu-id="24aa7-113">Customer List</span></span>  
* <span data-ttu-id="24aa7-114">Lánardrottnalisti</span><span class="sxs-lookup"><span data-stu-id="24aa7-114">Vendor List</span></span>  
* <span data-ttu-id="24aa7-115">Birgðalisti</span><span class="sxs-lookup"><span data-stu-id="24aa7-115">Item List</span></span>  
* <span data-ttu-id="24aa7-116">Reikningalisti</span><span class="sxs-lookup"><span data-stu-id="24aa7-116">Account List</span></span>  

<span data-ttu-id="24aa7-117">Útfluttu gögnin eru vistuð sem IIF-skrá sem síðan er hægt að hlaða upp í [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="24aa7-117">The exported data is saved as an IIF file that you can then upload to [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

## <a name="finding-the-quickbooks-data-migration-extension"></a><span data-ttu-id="24aa7-118">Finna viðbótin QuickBooks gagnaflutningar</span><span class="sxs-lookup"><span data-stu-id="24aa7-118">Finding the QuickBooks Data Migration Extension</span></span>
<span data-ttu-id="24aa7-119">Viðbótin QuickBooks gagnaflutningar er sett upp og tilbúin til keyrslu sem samþættur hluti af Gagnaflutningar uppsetningarleiðbeiningar með aðstoð.</span><span class="sxs-lookup"><span data-stu-id="24aa7-119">The QuickBooks Data Migration extension is installed and ready to go as an integrated part of the Data Migration assisted setup guide.</span></span> <span data-ttu-id="24aa7-120">Ef þú ert tilbúin(n) til hefjast handa, og hefur flutt út þín gögn frá QuickBooks, skal velja ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Uppsetning með hjálp** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="24aa7-120">If you are ready to get started now, and have exported your data from QuickBooks, choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Assisted Setup**, and then choose the related link.</span></span> <span data-ttu-id="24aa7-121">Veljið **Flytja viðskiptagögn** og fara síðan eftir skrefunum í leiðbeiningunum.</span><span class="sxs-lookup"><span data-stu-id="24aa7-121">Choose **Migrate business data**, and then follow the steps in the guide.</span></span>  

## <a name="see-also"></a><span data-ttu-id="24aa7-122">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="24aa7-122">See Also</span></span>
[<span data-ttu-id="24aa7-123">Innflutningur viðskiptagagna úr öðrum fjárhagskerfum</span><span class="sxs-lookup"><span data-stu-id="24aa7-123">Importing Business Data from Other Finance Systems</span></span>](across-import-data-configuration-packages.md)  
<span data-ttu-id="24aa7-124">[Sérstilling [!INCLUDE[d365fin](includes/d365fin_md.md)] með viðbótum ](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="24aa7-124">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions ](ui-extensions.md)</span></span>  

