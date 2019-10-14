---
title: Hönnunarupplýsingar - Pantanir | Microsoft Docs
description: Þetta efnisatriði veitir upplýsingar um pöntun til pöntunar hlekki í framleiða eftir pöntun umhverfi.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, order
ms.date: 10/01/2019
ms.author: sgroespe
redirect_url: design-details-handling-reordering-policies
ms.openlocfilehash: 09ef0ab320b2f7c19c0484f05efe7b3ae1fa41f7
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/01/2019
ms.locfileid: "2303113"
---
# <a name="design-details-order"></a><span data-ttu-id="a97a3-103">Hönnunarupplýsingar: pantanir</span><span class="sxs-lookup"><span data-stu-id="a97a3-103">Design Details: Order</span></span>
<span data-ttu-id="a97a3-104">Í framleiða eftir pöntun umhverfi, er vara keypt eða framleidd til eingöngu ná ákveðna eftirspurn.</span><span class="sxs-lookup"><span data-stu-id="a97a3-104">In a make-to-order environment, an item is purchased or produced to exclusively cover a specific demand.</span></span> <span data-ttu-id="a97a3-105">Venjulega tekur hún til A-vara og ástæða fyrir að velja Endurpöntunarstefnu pöntunar getur verið að eftirspurn er hverfandi, sem afhendingartími er óveruleg, eða nauðsynlegar eigindir mismunandi.</span><span class="sxs-lookup"><span data-stu-id="a97a3-105">Typically it relates to A-items, and the motivation for choosing the order reordering policy can be that the demand is infrequent, the lead-time is insignificant, or the required attributes vary.</span></span>  

<span data-ttu-id="a97a3-106">Forritið stofnar pöntun-við-pöntun tengsl sem virka sem undirbúningstengsl milli framboðsins, birgðapöntunar eða birgða og eftirspurnarinnar sem henni er ætlað að mæta.</span><span class="sxs-lookup"><span data-stu-id="a97a3-106">The application creates an order-to-order link, which acts as a preliminary connection between the supply, a supply order or inventory, and the demand that it is going to fulfill.</span></span>  

<span data-ttu-id="a97a3-107">Burtséð frá notkun pöntunarstefnu er hægt að nota tengil á milli pantana í áætlun með eftirfarandi hætti:</span><span class="sxs-lookup"><span data-stu-id="a97a3-107">Apart from using the Order policy, the order-to-order link can be applied during planning in the following ways:</span></span>  

* <span data-ttu-id="a97a3-108">Þegar reglan framleiðsla eftir pöntun er notuð til að stofna margþrepa framleiðslupöntun eða framleiðslupöntun af gerðinni verk (nauðsynlegir íhlutir framleiddir samkv. sömu framleiðslupöntun).</span><span class="sxs-lookup"><span data-stu-id="a97a3-108">When using the Make-to-Order manufacturing policy to create multi-level or project type production orders (producing needed components on the same production order).</span></span>  
* <span data-ttu-id="a97a3-109">Þegar búnaðurinn Sölupantanaáætlun er notaður til að stofna framleiðslupöntun úr sölupöntun.</span><span class="sxs-lookup"><span data-stu-id="a97a3-109">When using the Sales Order Planning feature to create a production order from a sales order.</span></span>  

<span data-ttu-id="a97a3-110">Jafnvel þótt framleiðslufyrirtæki álíti sig framleiða eftir pöntun geur verið best að nota endurpöntunarstefnuna lota fyrir lotu ef vörurnar eru staðlaðar án afbrigða í eigindum.</span><span class="sxs-lookup"><span data-stu-id="a97a3-110">Even if a manufacturing company considers itself as a make-to-order environment, it might be best to use a Lot-for-Lot reordering policy if the items are pure standard without variation in attributes.</span></span> <span data-ttu-id="a97a3-111">Niðurstaðan er að kerfið mun nota óáætlaðar birgðir og safna aðeins sölupöntunum með sömu afhendingardagsetningu eða innan tilgreinds tímaramma.</span><span class="sxs-lookup"><span data-stu-id="a97a3-111">As a result, the system will use unplanned inventory and only accumulates sales orders with the same shipment date or within a defined time bucket.</span></span>  

## <a name="order-to-order-links-and-past-due-dates"></a><span data-ttu-id="a97a3-112">Tenglar á milli pantana og liðnir skiladagar</span><span class="sxs-lookup"><span data-stu-id="a97a3-112">Order-to-Order Links and Past Due Dates</span></span>  
<span data-ttu-id="a97a3-113">Ólíkt flestum framboð-eftirspurn settum eru tengdar pantanir með skiladag á undan upphafsdagsetningu áætlunar áætlaðar að fullu af kerfinu.</span><span class="sxs-lookup"><span data-stu-id="a97a3-113">Unlike most supply-demand sets, linked orders with due dates before the planning starting date are fully planned for by the system.</span></span> <span data-ttu-id="a97a3-114">Viðskiptaástæðan fyrir þessa undanþágu er að tiltekin pör eftirspurnar og framboðs þurfa að vera samstillt fram að framkvæmdinni.</span><span class="sxs-lookup"><span data-stu-id="a97a3-114">The business reason for this exception is that specific demand-supply sets must be synchronized through to execution.</span></span> <span data-ttu-id="a97a3-115">Nánari upplýsingar um frosna svæðið sem eiga við um flestar gerðir framboðs og eftirspurnar eru í [Hönnunarupplýsingar: Takast á við pantanir fyrir upphafsdagsetningu áætlunar](design-details-dealing-with-orders-before-the-planning-starting-date.md).</span><span class="sxs-lookup"><span data-stu-id="a97a3-115">For more information about the frozen zone that applies to most demand-supply types, see [Design Details: Dealing with Orders Before the Planning Starting Date](design-details-dealing-with-orders-before-the-planning-starting-date.md).</span></span>  

## <a name="see-also"></a><span data-ttu-id="a97a3-116">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="a97a3-116">See Also</span></span>  
<span data-ttu-id="a97a3-117">[Hönnunarupplýsingar: Endurpöntunarstefnur](design-details-reordering-policies.md) </span><span class="sxs-lookup"><span data-stu-id="a97a3-117">[Design Details: Reordering Policies](design-details-reordering-policies.md) </span></span>  
<span data-ttu-id="a97a3-118">[Hönnunarupplýsingar: áætlunarfæribreyta](design-details-planning-parameters.md) </span><span class="sxs-lookup"><span data-stu-id="a97a3-118">[Design Details: Planning Parameters](design-details-planning-parameters.md) </span></span>  
<span data-ttu-id="a97a3-119">[Hönnunarupplýsingar: Meðhöndlun endurpöntunarstefna](design-details-handling-reordering-policies.md) </span><span class="sxs-lookup"><span data-stu-id="a97a3-119">[Design Details: Handling Reordering Policies](design-details-handling-reordering-policies.md) </span></span>  
[<span data-ttu-id="a97a3-120">Hönnunarupplýsingar: framboðsáætlun</span><span class="sxs-lookup"><span data-stu-id="a97a3-120">Design Details: Supply Planning</span></span>](design-details-supply-planning.md)
