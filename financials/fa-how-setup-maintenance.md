---
title: "Uppsetning eignaviðhalds| Microsoft Docs"
description: "Til að stjórna viðgerðum á og þjónustu við eignir, ertu tilteknar almennar upplýsingar um viðhald, kóðar fyrir tegund verks, og bókunarlykil fyrir kostnað."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: repair, service
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 7ae4abacf22d3610194ea56bbaa997390cb7df0a
ms.contentlocale: is-is
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-fixed-asset-maintenance"></a><span data-ttu-id="7c99f-103">Uppsetning eignarviðhalds</span><span class="sxs-lookup"><span data-stu-id="7c99f-103">Set Up Fixed Asset Maintenance</span></span>
<span data-ttu-id="7c99f-104">Til að halda utan um viðhald eigna, þarf fyrst að setja upp nokkrar almennar viðhaldsupplýsingar, bókunarlykil viðhaldskostnaðar og viðhaldskóta fyrir tegundir vinnu, svo sem Venjubundin Þjónusta eða Viðgerð.</span><span class="sxs-lookup"><span data-stu-id="7c99f-104">To manage fixed asset maintenance, you must first set up some general maintenance information, a posting account for maintenance costs, and maintenance codes for types of work, such as Routine Service or Repair.</span></span>

## <a name="to-set-up-general-maintenance-information"></a><span data-ttu-id="7c99f-105">Uppsetning almennra viðhaldsupplýsinga:</span><span class="sxs-lookup"><span data-stu-id="7c99f-105">To set up general maintenance information</span></span>
<span data-ttu-id="7c99f-106">Ef settir eru upp reitir fyrir viðhald er hægt að bóka viðhaldskostnað úr eignabók.</span><span class="sxs-lookup"><span data-stu-id="7c99f-106">If you set up the fields for maintenance, you can post maintenance expenses from the fixed asset journal.</span></span>

1. <span data-ttu-id="7c99f-107">Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **eignir** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="7c99f-107">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Fixed Assets**, and then choose the related link.</span></span>
2. <span data-ttu-id="7c99f-108">Valin er eignin fyrir hverja skilgreina á vátryggingasvið fyrir, og velja síðan **Breyta** aðgerð.</span><span class="sxs-lookup"><span data-stu-id="7c99f-108">Select the fixed asset that you to define insurance coverage for, and then choose the **Edit** action.</span></span>
3. <span data-ttu-id="7c99f-109">Fyllt er út í reiti eftir því sem við á í flýtiflipanum **Viðhald**.</span><span class="sxs-lookup"><span data-stu-id="7c99f-109">On the **Maintenance** FastTab, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-set-up-maintenance-codes"></a><span data-ttu-id="7c99f-110">Uppsetning viðhaldskóta</span><span class="sxs-lookup"><span data-stu-id="7c99f-110">To set up maintenance codes</span></span>
<span data-ttu-id="7c99f-111">Þegar viðhaldskostnaður er bókaður úr færslubók fyllt í reitinn **viðhaldskóði** til að skrá hvers konar viðhald hefur verið framkvæmt eins og venjubundin þjónusta eða viðgerð.</span><span class="sxs-lookup"><span data-stu-id="7c99f-111">When you post maintenance costs from a general journal, you fill in the **Maintenance Code** field to record what kind of maintenance has been performed, such as routine service or repair.</span></span>

1. <span data-ttu-id="7c99f-112">Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Viðhald** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="7c99f-112">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Maintenance**, and then choose the related link.</span></span>
2. <span data-ttu-id="7c99f-113">Í **Viðhald** glugganum skal setja upp kóta fyrir mismunandi tegundir viðhaldsvinnu.</span><span class="sxs-lookup"><span data-stu-id="7c99f-113">In the **Maintenance** window, set up codes for different types of maintenance work.</span></span>

## <a name="to-set-up-maintenance-expense-accounts"></a><span data-ttu-id="7c99f-114">Uppsetning reikninga viðhaldskostnaðar</span><span class="sxs-lookup"><span data-stu-id="7c99f-114">To set up maintenance expense accounts</span></span>
<span data-ttu-id="7c99f-115">Til að bóka viðhaldskostnað, verður fyrst að Færa inn reikningsnúmer í gluggann **Eignabókunarflokkar**.</span><span class="sxs-lookup"><span data-stu-id="7c99f-115">To post maintenance costs, you must first enter an account number in the **FA Posting Groups** window.</span></span>

1. <span data-ttu-id="7c99f-116">Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn  **FA bókunarflokkar** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="7c99f-116">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **FA Posting Groups**, and then choose the related link.</span></span>
2. <span data-ttu-id="7c99f-117">Reiturinn **Reikningur viðhaldskostnaðar** er fylltur út fyrir hvern bókunarhóp.</span><span class="sxs-lookup"><span data-stu-id="7c99f-117">Fill in the **Maintenance Expense Account** field for each posting group.</span></span>

> [!NOTE]  
>   <span data-ttu-id="7c99f-118">Til að skilgreina að viðhaldskostnaði er úthlutað á deildir eða verkefni, eru settir upp úthlutunarlyklar.</span><span class="sxs-lookup"><span data-stu-id="7c99f-118">To define that maintenance costs are allocated to departments or projects, set up an allocation keys.</span></span> <span data-ttu-id="7c99f-119">Frekari upplýsingar eru í [Setja upp almenna eiginleika eigna](fa-how-setup-general.md).</span><span class="sxs-lookup"><span data-stu-id="7c99f-119">For more information, see [Set Up General Fixed Assets Features](fa-how-setup-general.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="7c99f-120">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="7c99f-120">See Also</span></span>
[<span data-ttu-id="7c99f-121">Uppsetning eigna</span><span class="sxs-lookup"><span data-stu-id="7c99f-121">Setting Up Fixed Assets</span></span>](fa-setup.md)  
[<span data-ttu-id="7c99f-122">Eignir</span><span class="sxs-lookup"><span data-stu-id="7c99f-122">Fixed Assets</span></span>](fa-manage.md)  
[<span data-ttu-id="7c99f-123">Fjármál</span><span class="sxs-lookup"><span data-stu-id="7c99f-123">Finance</span></span>](finance.md)  
<span data-ttu-id="7c99f-124">[Velkomin(n) í [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)</span><span class="sxs-lookup"><span data-stu-id="7c99f-124">[Welcome to [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)</span></span>  
<span data-ttu-id="7c99f-125">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="7c99f-125">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

