---
title: Setja upp Kóta fyrir Staðlaða þjónustu | Microsoft Docs
description: Lærðu hvernig á að setja upp Kóta fyrir þjónustuaðgerðir sem þú framkvæmir oft.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: service, service item, service order, repairs, maintenance
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 2db9480789e90b15e0a9d4e737817d3b8ff3b3c9
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/01/2020
ms.locfileid: "3925829"
---
# <a name="set-up-standard-service-codes"></a><span data-ttu-id="adfbb-103">Setja upp staðlaða þjónustukóða</span><span class="sxs-lookup"><span data-stu-id="adfbb-103">Set Up Standard Service Codes</span></span>

<span data-ttu-id="adfbb-104">Þegar dæmigerð þjónusta er framkvæmd er oft nauðsynlegt að stofna þjónustuskjöl sem nota þjónustulínur sem innihalda sams konar upplýsingar.</span><span class="sxs-lookup"><span data-stu-id="adfbb-104">When you perform typical service, you often have to create service documents that use service lines that contain similar information.</span></span> <span data-ttu-id="adfbb-105">Til að gera það auðvelt að stofna línur, geturðu sett upp staðlaða þjónustukóða sem hafa fyrirframskilgreint safn af þjónustulínum.</span><span class="sxs-lookup"><span data-stu-id="adfbb-105">To make it easy to create these lines, you can set up standard service codes that have a predefined set of service lines.</span></span> <span data-ttu-id="adfbb-106">Þegar þú velur kóðann fyrir þjónustuskjal, eru línurnar settar inn sjálfvirkt.</span><span class="sxs-lookup"><span data-stu-id="adfbb-106">When you choose the code on a service document, the lines are entered automatically.</span></span> <span data-ttu-id="adfbb-107">Þú getur sett upp ótakmarkaðan fjölda af stöðluðum þjónustukóðum, hver þjónustukóti getur haft ótakmarkaðan fjölda af þjónustulínum af mismunandi tegundum, þar á meðal vöru, forða, kostnað eða staðlaða textann tengda við þá.</span><span class="sxs-lookup"><span data-stu-id="adfbb-107">You can set up any number of standard service codes, and each code can have an unlimited number of service lines of different types, including item, resource, cost, or standard text linked to it.</span></span> <span data-ttu-id="adfbb-108">Þú stofnar þjónustulínur af hverjum stöðluðum þjónustukóða á spjaldinu **Staðlaður þjónustukóði** .</span><span class="sxs-lookup"><span data-stu-id="adfbb-108">You create service lines of each standard service code on the **Standard Service Code** card.</span></span> <span data-ttu-id="adfbb-109">Hægt er að úthluta stöðluðum þjónustukóðum til þjónustuvöruflokka á síðunni **Staðlaðir þjónustuvöruflokkakóðar** .</span><span class="sxs-lookup"><span data-stu-id="adfbb-109">You then assign standard service codes to service item groups on the **Standard Serv. Item Gr. Codes** page.</span></span> <span data-ttu-id="adfbb-110">Seinna, þegar þjónustuskjal er búið til, er hægt að keyra virknina **Sækja staðlaða þjónustukóta** til þess að láta færa inn þjónustulínur.</span><span class="sxs-lookup"><span data-stu-id="adfbb-110">Later, when you create a service document, you can use the **Get Standard Service Codes** action to add service lines.</span></span>  
  
> [!Tip]
> <span data-ttu-id="adfbb-111">Þú getur notað sama hugmyndagrunn til að stofna línur fyrir sölu og innkaupaskjöl.</span><span class="sxs-lookup"><span data-stu-id="adfbb-111">You can use the same concept to create lines on sales and purchase documents.</span></span> <span data-ttu-id="adfbb-112">Nánari upplýsingar er að finna í [Stofna ítrekaðar sölu og innkaupalínur](sales-how-work-standard-lines.md).</span><span class="sxs-lookup"><span data-stu-id="adfbb-112">For more information, see [Create Recurring Sales and Purchase Lines](sales-how-work-standard-lines.md).</span></span>  
  
## <a name="to-set-up-a-standard-service-code"></a><span data-ttu-id="adfbb-113">Uppsetning staðlaðra þjónustukóta</span><span class="sxs-lookup"><span data-stu-id="adfbb-113">To set up a standard service code</span></span>

1. <span data-ttu-id="adfbb-114">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Staðlaðir þjónustukóðar** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="adfbb-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Standard Service Codes** , and then choose the related link.</span></span>  
2. <span data-ttu-id="adfbb-115">Fyllið inn í reitina eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="adfbb-115">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. <span data-ttu-id="adfbb-116">Fylla út þjónustulínur tengdar þessum þjónustukóta.</span><span class="sxs-lookup"><span data-stu-id="adfbb-116">Fill in the service lines linked to this service code.</span></span>  

## <a name="to-assign-a-standard-service-code-to-a-service-item-group"></a><span data-ttu-id="adfbb-117">Stöðluðum þjónustukóta úthlutað til þjónustuvöruhóps</span><span class="sxs-lookup"><span data-stu-id="adfbb-117">To assign a standard service code to a service item group</span></span>

1. <span data-ttu-id="adfbb-118">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Þjónustuvöruflokkar** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="adfbb-118">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Service item Groups** , and then choose the related link.</span></span>  
2. <span data-ttu-id="adfbb-119">Fyllið inn í reitina eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="adfbb-119">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="adfbb-120">Fylla út þjónustulínur tengdar þessum þjónustukóta.</span><span class="sxs-lookup"><span data-stu-id="adfbb-120">Fill in the service lines linked to this service code.</span></span>  

## <a name="see-also"></a><span data-ttu-id="adfbb-121">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="adfbb-121">See Also</span></span>

[<span data-ttu-id="adfbb-122">Þjónustukerfi</span><span class="sxs-lookup"><span data-stu-id="adfbb-122">Service Management</span></span>](service-service.md)