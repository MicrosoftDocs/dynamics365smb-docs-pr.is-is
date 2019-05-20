---
title: Uppsetning eignaviðhalds| Microsoft Docs
description: Til að stjórna viðgerðum á og þjónustu við eignir, ertu tilteknar almennar upplýsingar um viðhald, kóðar fyrir tegund verks, og bókunarlykil fyrir kostnað.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: repair, service
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: ba01ccb88349a1f1943655949a36e2a21f3ae2de
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/29/2019
ms.locfileid: "1244495"
---
# <a name="set-up-fixed-asset-maintenance"></a><span data-ttu-id="76b4f-103">Uppsetning eignarviðhalds</span><span class="sxs-lookup"><span data-stu-id="76b4f-103">Set Up Fixed Asset Maintenance</span></span>
<span data-ttu-id="76b4f-104">Til að halda utan um viðhald eigna, þarf fyrst að setja upp nokkrar almennar viðhaldsupplýsingar, bókunarlykil viðhaldskostnaðar og viðhaldskóta fyrir tegundir vinnu, svo sem Venjubundin Þjónusta eða Viðgerð.</span><span class="sxs-lookup"><span data-stu-id="76b4f-104">To manage fixed asset maintenance, you must first set up some general maintenance information, a posting account for maintenance costs, and maintenance codes for types of work, such as Routine Service or Repair.</span></span>

## <a name="to-set-up-general-maintenance-information"></a><span data-ttu-id="76b4f-105">Uppsetning almennra viðhaldsupplýsinga:</span><span class="sxs-lookup"><span data-stu-id="76b4f-105">To set up general maintenance information</span></span>
<span data-ttu-id="76b4f-106">Ef settir eru upp reitir fyrir viðhald er hægt að bóka viðhaldskostnað úr eignabók.</span><span class="sxs-lookup"><span data-stu-id="76b4f-106">If you set up the fields for maintenance, you can post maintenance expenses from the fixed asset journal.</span></span>

1. <span data-ttu-id="76b4f-107">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Eignir** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="76b4f-107">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Fixed Assets**, and then choose the related link.</span></span>
2. <span data-ttu-id="76b4f-108">Valin er eignin fyrir hverja skilgreina á vátryggingasvið fyrir, og velja síðan **Breyta** aðgerð.</span><span class="sxs-lookup"><span data-stu-id="76b4f-108">Select the fixed asset that you to define insurance coverage for, and then choose the **Edit** action.</span></span>
3. <span data-ttu-id="76b4f-109">Fyllt er út í reiti eftir því sem við á í flýtiflipanum **Viðhald**.</span><span class="sxs-lookup"><span data-stu-id="76b4f-109">On the **Maintenance** FastTab, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-set-up-maintenance-codes"></a><span data-ttu-id="76b4f-110">Uppsetning viðhaldskóta</span><span class="sxs-lookup"><span data-stu-id="76b4f-110">To set up maintenance codes</span></span>
<span data-ttu-id="76b4f-111">Þegar viðhaldskostnaður er bókaður úr færslubók fyllt í reitinn **viðhaldskóði** til að skrá hvers konar viðhald hefur verið framkvæmt eins og venjubundin þjónusta eða viðgerð.</span><span class="sxs-lookup"><span data-stu-id="76b4f-111">When you post maintenance costs from a general journal, you fill in the **Maintenance Code** field to record what kind of maintenance has been performed, such as routine service or repair.</span></span>

1. <span data-ttu-id="76b4f-112">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **viðhald** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="76b4f-112">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Maintenance**, and then choose the related link.</span></span>
2. <span data-ttu-id="76b4f-113">Á síðunni **Viðhald** skal setja upp kóða fyrir mismunandi tegundir viðhaldsvinnu.</span><span class="sxs-lookup"><span data-stu-id="76b4f-113">On the **Maintenance** page, set up codes for different types of maintenance work.</span></span>

## <a name="to-set-up-maintenance-expense-accounts"></a><span data-ttu-id="76b4f-114">Uppsetning reikninga viðhaldskostnaðar</span><span class="sxs-lookup"><span data-stu-id="76b4f-114">To set up maintenance expense accounts</span></span>
<span data-ttu-id="76b4f-115">Til að bóka viðhaldskostnað, verður fyrst að Færa inn reikningsnúmer á síðuna **Eignabókunarflokkar**.</span><span class="sxs-lookup"><span data-stu-id="76b4f-115">To post maintenance costs, you must first enter an account number on the **FA Posting Groups** page.</span></span>

1. <span data-ttu-id="76b4f-116">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **eignabókunarflokkar** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="76b4f-116">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **FA Posting Groups**, and then choose the related link.</span></span>
2. <span data-ttu-id="76b4f-117">Reiturinn **Reikningur viðhaldskostnaðar** er fylltur út fyrir hvern bókunarhóp.</span><span class="sxs-lookup"><span data-stu-id="76b4f-117">Fill in the **Maintenance Expense Account** field for each posting group.</span></span>

> [!NOTE]  
>   <span data-ttu-id="76b4f-118">Til að skilgreina að viðhaldskostnaði er úthlutað á deildir eða verkefni, eru settir upp úthlutunarlyklar.</span><span class="sxs-lookup"><span data-stu-id="76b4f-118">To define that maintenance costs are allocated to departments or projects, set up an allocation keys.</span></span> <span data-ttu-id="76b4f-119">Frekari upplýsingar eru í [Setja upp almenna eiginleika eigna](fa-how-setup-general.md).</span><span class="sxs-lookup"><span data-stu-id="76b4f-119">For more information, see [Set Up General Fixed Assets Features](fa-how-setup-general.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="76b4f-120">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="76b4f-120">See Also</span></span>
[<span data-ttu-id="76b4f-121">Uppsetning eigna</span><span class="sxs-lookup"><span data-stu-id="76b4f-121">Setting Up Fixed Assets</span></span>](fa-setup.md)  
[<span data-ttu-id="76b4f-122">Eignir</span><span class="sxs-lookup"><span data-stu-id="76b4f-122">Fixed Assets</span></span>](fa-manage.md)  
[<span data-ttu-id="76b4f-123">Fjármál</span><span class="sxs-lookup"><span data-stu-id="76b4f-123">Finance</span></span>](finance.md)  
[<span data-ttu-id="76b4f-124">Hafist handa</span><span class="sxs-lookup"><span data-stu-id="76b4f-124">Getting Started</span></span>](product-get-started.md)  
<span data-ttu-id="76b4f-125">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="76b4f-125">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
