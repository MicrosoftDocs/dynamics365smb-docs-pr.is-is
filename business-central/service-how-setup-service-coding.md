---
title: "Setja upp Kóta fyrir Staðlaða þjónustu | Microsoft Docs"
description: "Lærðu hvernig á að setja upp Kóta fyrir þjónustuaðgerðir sem þú framkvæmir oft."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: service, service item, service order, repairs, maintenance
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: f73f5b9d74e7b6a75be6320697aa1a4ad84fb4a1
ms.contentlocale: is-is
ms.lasthandoff: 09/28/2018

---

# <a name="set-up-standard-service-codes"></a><span data-ttu-id="4daae-103">Setja upp staðlaða þjónustukóða</span><span class="sxs-lookup"><span data-stu-id="4daae-103">Set Up Standard Service Codes</span></span>
<span data-ttu-id="4daae-104">Þegar dæmigerð þjónusta er framkvæmd er oft nauðsynlegt að stofna þjónustuskjöl sem nota þjónustulínur sem innihalda sams konar upplýsingar.</span><span class="sxs-lookup"><span data-stu-id="4daae-104">When you perform typical service, you often have to create service documents that use service lines that contain similar information.</span></span> <span data-ttu-id="4daae-105">Til að gera það auðvelt að stofna línur, geturðu sett upp staðlaða þjónustukóða sem hafa fyrirframskilgreint safn af þjónustulínum.</span><span class="sxs-lookup"><span data-stu-id="4daae-105">To make it easy to create these lines, you can set up standard service codes that have a predefined set of service lines.</span></span> <span data-ttu-id="4daae-106">Þegar þú velur kóðann fyrir þjónustuskjal, eru línurnar settar inn sjálfvirkt.</span><span class="sxs-lookup"><span data-stu-id="4daae-106">When you choose the code on a service document, the lines are entered automatically.</span></span> <span data-ttu-id="4daae-107">Þú getur sett upp ótakmarkaðan fjölda af stöðluðum þjónustukóðum, hver þjónustukóti getur haft ótakmarkaðan fjölda af þjónustulínum af mismunandi tegundum, þar á meðal vöru, forða, kostnað eða staðlaða textann tengda við þá.</span><span class="sxs-lookup"><span data-stu-id="4daae-107">You can set up any number of standard service codes, and each code can have an unlimited number of service lines of different types, including item, resource, cost, or standrd text linked to it.</span></span> <span data-ttu-id="4daae-108">Þú stofnar þjónustulínur af hverjum stöðluðum þjónustukóða á spjaldinu **Staðlaður þjónustukóði**.</span><span class="sxs-lookup"><span data-stu-id="4daae-108">You create service lines of each standard serice code on the **Standard Service Code** card.</span></span> <span data-ttu-id="4daae-109">Hægt er að úthluta stöðluðum þjónustukóðum til þjónustuvöruflokka í glugganum **Staðlaðir þjónustukóðar**.</span><span class="sxs-lookup"><span data-stu-id="4daae-109">You then assign standard service codes to service item groups in the **Standard Serv. Item Gr. Codes** window.</span></span> <span data-ttu-id="4daae-110">Seinna, þegar þjónustuskjal er búið til, er hægt að keyra virknina **Sækja staðlaða þjónustukóta** til þess að láta færa inn þjónustulínur.</span><span class="sxs-lookup"><span data-stu-id="4daae-110">Later, when you create a service document, you can use the **Get Standard Service Codes** action to add service lines.</span></span>  
  
> [!Tip]
>  <span data-ttu-id="4daae-111">Þú getur notað sama hugmyndagrunn til að stofna línur fyrir sölu og innkaupaskjöl.</span><span class="sxs-lookup"><span data-stu-id="4daae-111">You can use the same concept to create lines on sales and purchase documents.</span></span> <span data-ttu-id="4daae-112">Nánari upplýsingar er að finna í [Stofna ítrekaðar sölu og innkaupalínur](sales-how-work-standard-lines.md).</span><span class="sxs-lookup"><span data-stu-id="4daae-112">For more information, see [Create Recurring Sales and Purchase Lines](sales-how-work-standard-lines.md).</span></span>    
  
## <a name="to-set-up-a-standard-service-code"></a><span data-ttu-id="4daae-113">Uppsetning staðlaðra þjónustukóta</span><span class="sxs-lookup"><span data-stu-id="4daae-113">To set up a standard service code</span></span>    
1. <span data-ttu-id="4daae-114">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **staðlaður þjónustukóði** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="4daae-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Standard Service Codes**, and then choose the related link.</span></span>  
2. <span data-ttu-id="4daae-115">Fyllið inn í reitina eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="4daae-115">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
4. <span data-ttu-id="4daae-116">Fylla út þjónustulínur tengdar þessum þjónustukóta.</span><span class="sxs-lookup"><span data-stu-id="4daae-116">Fill in the service lines linked to this service code.</span></span>  

## <a name="to-assign-a-standard-service-code-to-a-service-item-group"></a><span data-ttu-id="4daae-117">Stöðluðum þjónustukóta úthlutað til þjónustuvöruhóps</span><span class="sxs-lookup"><span data-stu-id="4daae-117">To assign a standard service code to a service item group</span></span>
1. <span data-ttu-id="4daae-118">Veldu ![Ljósaperu sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Þjónustuvöruflokkar** og veldu síðan tengda hlekkinn.</span><span class="sxs-lookup"><span data-stu-id="4daae-118">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Service item Groups**, and then choose the related link.</span></span>  
2. <span data-ttu-id="4daae-119">Fyllið inn í reitina eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="4daae-119">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="4daae-120">Fylla út þjónustulínur tengdar þessum þjónustukóta.</span><span class="sxs-lookup"><span data-stu-id="4daae-120">Fill in the service lines linked to this service code.</span></span>  

## <a name="see-also"></a><span data-ttu-id="4daae-121">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="4daae-121">See Also</span></span>
[<span data-ttu-id="4daae-122">Þjónustukerfi</span><span class="sxs-lookup"><span data-stu-id="4daae-122">Service Management</span></span>](service-service.md)
