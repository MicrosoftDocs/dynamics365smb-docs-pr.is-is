---
title: "Flytja gögn frá Dynamics GP með Gagnaflutningaviðbótinni | Microsoft Docs"
description: "Nota Dynamics GP Gagnaflutningaviðbótina til að flytja viðskiptamenn, lánardrottna, birgðir og reikninga úr Dynamics GP í Dynamics 365 Business edition."
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
ms.translationtype: HT
ms.sourcegitcommit: ba26b354d235981bd7291f9ac6402779f554ac7a
ms.openlocfilehash: b97c074b1283a981522b7a9651fcc7c552f1f930
ms.contentlocale: is-is
ms.lasthandoff: 11/10/2017

---
# <a name="the-dynamics-gp-data-migration-extension-for-dynamics-365-business-edition"></a><span data-ttu-id="e3ff3-103">Viðbótin Dynamics GP gagnaflutningarviðbót í Dynamics 365 Business edition</span><span class="sxs-lookup"><span data-stu-id="e3ff3-103">The Dynamics GP Data Migration Extension for Dynamics 365 Business edition</span></span> 
<span data-ttu-id="e3ff3-104">Þessi viðbót gerir það auðvelt að flytja viðskiptamenn, lánardrottna, birgðir og reikninga úr Dynamics GP í [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="e3ff3-104">This extension makes it easy to migrate customers, vendors, inventory items, and accounts from Dynamics GP to [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="e3ff3-105">Ef fyrirtækið notar Dynamics GP er hægt að flytja út viðeigandi aðalfærslur og opna síðan leiðarvísi fyrir uppsetningu með hjálp til að bæta gögnunum við [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="e3ff3-105">If your business uses Dynamics GP today, you can export the relevant master records and then open an assisted setup guide to add the data to [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="e3ff3-106">Nánari upplýsingar eru í [Yfirfæra viðskiptagögn úr öðrum fjárhagskerfum](upload-data.md).</span><span class="sxs-lookup"><span data-stu-id="e3ff3-106">For more information, see [Migrate Business Data from Other Finance Systems](upload-data.md).</span></span>

## <a name="exporting-data-from-dynamics-gp"></a><span data-ttu-id="e3ff3-107">Flytja út gögn úr Dynamics GP</span><span class="sxs-lookup"><span data-stu-id="e3ff3-107">Exporting Data from Dynamics GP</span></span>
<span data-ttu-id="e3ff3-108">Þú verður að hafa flutt einhverja eða alla viðskiptamenn þína, söluaðila, birgðavörur og reikninga í skrá með því að nota Dynamics GP virkni fyrir útflutning gagna.</span><span class="sxs-lookup"><span data-stu-id="e3ff3-108">You must have exported some or all of your existing customers, vendors, inventory items, and accounts to a file, using the Dynamics GP functionality for data export.</span></span> <span data-ttu-id="e3ff3-109">Fyrir [!INCLUDE[d365fin](includes/d365fin_md.md)] er hægt að flytja út eftirfarandi gerðir gagna:</span><span class="sxs-lookup"><span data-stu-id="e3ff3-109">For the purposes of [!INCLUDE[d365fin](includes/d365fin_md.md)], you can export the following types of data:</span></span>

* <span data-ttu-id="e3ff3-110">Reikningur</span><span class="sxs-lookup"><span data-stu-id="e3ff3-110">Account</span></span>  
* <span data-ttu-id="e3ff3-111">Viðskiptavinur</span><span class="sxs-lookup"><span data-stu-id="e3ff3-111">Customer</span></span>  
* <span data-ttu-id="e3ff3-112">Atriði</span><span class="sxs-lookup"><span data-stu-id="e3ff3-112">Item</span></span>  
* <span data-ttu-id="e3ff3-113">Lánardrottinn</span><span class="sxs-lookup"><span data-stu-id="e3ff3-113">Vendor</span></span>  

<span data-ttu-id="e3ff3-114">Dynamics GP Data Migration viðbót varpar sjálfkrafa útfluttm gögn þannig að þú hafir skjótan aðgang að gögnunum þínum í nýja [!INCLUDE[d365fin](includes/d365fin_md.md)] fyrirtækinu.</span><span class="sxs-lookup"><span data-stu-id="e3ff3-114">The Dynamics GP Data Migration extension automatically maps the exported data so that your data is quickly available to you in your new [!INCLUDE[d365fin](includes/d365fin_md.md)] company.</span></span> <span data-ttu-id="e3ff3-115">Meðan á ferlinu stendur eru uppsetningarupplýsingar stofnaðar, svo sem bókunarflokkar.</span><span class="sxs-lookup"><span data-stu-id="e3ff3-115">During the process, supporting setup information is created, such as posting groups.</span></span> <span data-ttu-id="e3ff3-116">Birgðavörur verða fluttar inn í kerfið með FIFO sem villuleitaraðferð kostnaðar.</span><span class="sxs-lookup"><span data-stu-id="e3ff3-116">Inventory items will be brought into the system with FIFO as the cost valuation method.</span></span> <span data-ttu-id="e3ff3-117">Lyklar verða settar upp sem aðalreikningslyklar úr Dynamics GP með víddum vegna þess að [!INCLUDE[d365fin](includes/d365fin_long_md.md)] er ekki með lyklahluta.</span><span class="sxs-lookup"><span data-stu-id="e3ff3-117">Accounts will be set up as the main account segment from Dynamics GP with dimensions, because [!INCLUDE[d365fin](includes/d365fin_long_md.md)] does not have account segments.</span></span>

## <a name="see-also"></a><span data-ttu-id="e3ff3-118">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="e3ff3-118">See Also</span></span>
[<span data-ttu-id="e3ff3-119">Innflutningur viðskiptagagna úr öðrum fjárhagskerfum</span><span class="sxs-lookup"><span data-stu-id="e3ff3-119">Importing Business Data from Other Finance Systems</span></span>](upload-data.md)  
<span data-ttu-id="e3ff3-120">[Sérstilling [!INCLUDE[d365fin](includes/d365fin_md.md)] með viðbótum ](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="e3ff3-120">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions ](ui-extensions.md)</span></span>  

