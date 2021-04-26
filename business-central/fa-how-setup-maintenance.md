---
title: Uppsetning eignaviðhalds| Microsoft Docs
description: Til að stjórna viðgerðum á og þjónustu við eignir, ertu tilteknar almennar upplýsingar um viðhald, kóðar fyrir tegund verks, og bókunarlykil fyrir kostnað.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: repair, service
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: b437f7508537ec438bf90c3a1239e2620e9db196
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5775551"
---
# <a name="set-up-fixed-asset-maintenance"></a><span data-ttu-id="cde23-103">Uppsetning eignarviðhalds</span><span class="sxs-lookup"><span data-stu-id="cde23-103">Set Up Fixed Asset Maintenance</span></span>
<span data-ttu-id="cde23-104">Til að halda utan um viðhald eigna, þarf fyrst að setja upp nokkrar almennar viðhaldsupplýsingar, bókunarlykil viðhaldskostnaðar og viðhaldskóta fyrir tegundir vinnu, svo sem Venjubundin Þjónusta eða Viðgerð.</span><span class="sxs-lookup"><span data-stu-id="cde23-104">To manage fixed asset maintenance, you must first set up some general maintenance information, a posting account for maintenance costs, and maintenance codes for types of work, such as Routine Service or Repair.</span></span>

## <a name="to-set-up-general-maintenance-information"></a><span data-ttu-id="cde23-105">Uppsetning almennra viðhaldsupplýsinga:</span><span class="sxs-lookup"><span data-stu-id="cde23-105">To set up general maintenance information</span></span>
<span data-ttu-id="cde23-106">Ef settir eru upp reitir fyrir viðhald er hægt að bóka viðhaldskostnað úr eignabók.</span><span class="sxs-lookup"><span data-stu-id="cde23-106">If you set up the fields for maintenance, you can post maintenance expenses from the fixed asset journal.</span></span>

1. <span data-ttu-id="cde23-107">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Eignir** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="cde23-107">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Fixed Assets**, and then choose the related link.</span></span>
2. <span data-ttu-id="cde23-108">Valin er eignin fyrir hverja skilgreina á vátryggingasvið fyrir, og velja síðan **Breyta** aðgerð.</span><span class="sxs-lookup"><span data-stu-id="cde23-108">Select the fixed asset that you to define insurance coverage for, and then choose the **Edit** action.</span></span>
3. <span data-ttu-id="cde23-109">Fyllt er út í reiti eftir því sem við á í flýtiflipanum **Viðhald**.</span><span class="sxs-lookup"><span data-stu-id="cde23-109">On the **Maintenance** FastTab, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-set-up-maintenance-codes"></a><span data-ttu-id="cde23-110">Uppsetning viðhaldskóta</span><span class="sxs-lookup"><span data-stu-id="cde23-110">To set up maintenance codes</span></span>
<span data-ttu-id="cde23-111">Þegar viðhaldskostnaður er bókaður úr færslubók fyllt í reitinn **viðhaldskóði** til að skrá hvers konar viðhald hefur verið framkvæmt eins og venjubundin þjónusta eða viðgerð.</span><span class="sxs-lookup"><span data-stu-id="cde23-111">When you post maintenance costs from a general journal, you fill in the **Maintenance Code** field to record what kind of maintenance has been performed, such as routine service or repair.</span></span>

1. <span data-ttu-id="cde23-112">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Viðhald** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="cde23-112">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Maintenance**, and then choose the related link.</span></span>
2. <span data-ttu-id="cde23-113">Á síðunni **Viðhald** skal setja upp kóða fyrir mismunandi tegundir viðhaldsvinnu.</span><span class="sxs-lookup"><span data-stu-id="cde23-113">On the **Maintenance** page, set up codes for different types of maintenance work.</span></span>

## <a name="to-set-up-maintenance-expense-accounts"></a><span data-ttu-id="cde23-114">Uppsetning reikninga viðhaldskostnaðar</span><span class="sxs-lookup"><span data-stu-id="cde23-114">To set up maintenance expense accounts</span></span>
<span data-ttu-id="cde23-115">Til að bóka viðhaldskostnað, verður fyrst að Færa inn reikningsnúmer á síðuna **Eignabókunarflokkar**.</span><span class="sxs-lookup"><span data-stu-id="cde23-115">To post maintenance costs, you must first enter an account number on the **FA Posting Groups** page.</span></span>

1. <span data-ttu-id="cde23-116">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Eignarbókunarflokkar** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="cde23-116">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **FA Posting Groups**, and then choose the related link.</span></span>
2. <span data-ttu-id="cde23-117">Reiturinn **Reikningur viðhaldskostnaðar** er fylltur út fyrir hvern bókunarhóp.</span><span class="sxs-lookup"><span data-stu-id="cde23-117">Fill in the **Maintenance Expense Account** field for each posting group.</span></span>

> [!NOTE]  
>   <span data-ttu-id="cde23-118">Til að skilgreina að viðhaldskostnaði er úthlutað á deildir eða verkefni, eru settir upp úthlutunarlyklar.</span><span class="sxs-lookup"><span data-stu-id="cde23-118">To define that maintenance costs are allocated to departments or projects, set up an allocation keys.</span></span> <span data-ttu-id="cde23-119">Frekari upplýsingar eru í [Setja upp almenna eiginleika eigna](fa-how-setup-general.md).</span><span class="sxs-lookup"><span data-stu-id="cde23-119">For more information, see [Set Up General Fixed Assets Features](fa-how-setup-general.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="cde23-120">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="cde23-120">See Also</span></span>
[<span data-ttu-id="cde23-121">Uppsetning eigna</span><span class="sxs-lookup"><span data-stu-id="cde23-121">Setting Up Fixed Assets</span></span>](fa-setup.md)  
[<span data-ttu-id="cde23-122">Eignir</span><span class="sxs-lookup"><span data-stu-id="cde23-122">Fixed Assets</span></span>](fa-manage.md)  
[<span data-ttu-id="cde23-123">Fjármál</span><span class="sxs-lookup"><span data-stu-id="cde23-123">Finance</span></span>](finance.md)  
[<span data-ttu-id="cde23-124">Undirbúðu þig fyrir að gera viðskipti</span><span class="sxs-lookup"><span data-stu-id="cde23-124">Getting Ready for Doing Business</span></span>](ui-get-ready-business.md)  
<span data-ttu-id="cde23-125">[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="cde23-125">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]