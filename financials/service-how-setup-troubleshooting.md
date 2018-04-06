---
title: "Setja upp úrræðaleit ferli | Microsoft Docs"
description: "Lærið hvernig á að setja upp ferli sem hjálpa þjónustuaðilum að koma auga á og leysa úr vandamálum með þjónustuvörum."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: service, service item, troubleshoot, repairs, maintenance
ms.date: 08/22/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 5876bf5d959d106eefb9b0f765e42e74dd13ab07
ms.contentlocale: is-is
ms.lasthandoff: 03/22/2018

---

# <a name="setting-up-troubleshooting-for-service-items"></a><span data-ttu-id="68db8-103">Setja upp úrræðaleit fyrir þjónustuvörur</span><span class="sxs-lookup"><span data-stu-id="68db8-103">Setting Up Troubleshooting for Service Items</span></span>
<span data-ttu-id="68db8-104">Þú getur sett upp viðmiðunarreglur fyrir úrræðaleit sem hjálpa tæknimönnum að leysa vandamál þegar þeir veita þjónustu.</span><span class="sxs-lookup"><span data-stu-id="68db8-104">You can set up troubleshooting guidelines that help technicians solve problems when providing service.</span></span> <span data-ttu-id="68db8-105">Viðmiðunarreglur geta t.d. verið listi yfir skref sem framkvæma á við viðgerð, eða röð spurninga til að spyrja um vörurnar.</span><span class="sxs-lookup"><span data-stu-id="68db8-105">For example, guidelines might be a list of steps to perform a repair, or a series of questions to ask about the items.</span></span> <span data-ttu-id="68db8-106">Þegar leiðbeiningar um úrræðaleit hafa verið settar upp er hægt að úthluta þeim til þjónustuvöruflokka, þjónustuvara og vara.</span><span class="sxs-lookup"><span data-stu-id="68db8-106">After you set up troubleshooting guidelines, you can assign them to service item groups, service items, and items.</span></span> <span data-ttu-id="68db8-107">Til er afritun stigveldis fyrir viðmiðunarreglur.</span><span class="sxs-lookup"><span data-stu-id="68db8-107">There is an inheritance hierarchy for guidelines.</span></span> <span data-ttu-id="68db8-108">Ef þú úthlutar þeim til þjónustuvöruflokks, munu vörurnar innan flokksins fá viðmiðunarreglurnar nema þú tiltakir þær fyrir íhlutina.</span><span class="sxs-lookup"><span data-stu-id="68db8-108">If you assign them to a service item group, the items included in the group will inherit the guidelines unless you specify them for the items.</span></span> <span data-ttu-id="68db8-109">Á sama hátt, munu þjónustuvörur fá viðmiðunarreglurnar frá íhlutunum.</span><span class="sxs-lookup"><span data-stu-id="68db8-109">Similarly, service items will inherit guidelines from items.</span></span>  

## <a name="to-set-up-troubleshooting-guidelines"></a><span data-ttu-id="68db8-110">Uppsetning leiðbeininga við úrræðaleit</span><span class="sxs-lookup"><span data-stu-id="68db8-110">To set up troubleshooting guidelines</span></span>
1. <span data-ttu-id="68db8-111">Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Úrræðaleit** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="68db8-111">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Troubleshooting**, and then choose the related link.</span></span>  
2. <span data-ttu-id="68db8-112">Fyllið inn í reitina eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="68db8-112">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-assign-troubleshooting-guidelines-to-items-service-items-or-service-item-groups"></a><span data-ttu-id="68db8-113">Úthluta leiðbeiningum úrræðaleitar til íhluta, þjónustuvara eða þjónustuvöruflokka</span><span class="sxs-lookup"><span data-stu-id="68db8-113">To assign troubleshooting guidelines to items, service items, or service item groups</span></span>
1. <span data-ttu-id="68db8-114">Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Íhlutir**, **Þjónustuvörur** eða **Þjónustuvöruflokkar** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="68db8-114">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Items**, **Service Items**, or **Service Item Groups**, and then choose the related link.</span></span>  
2. <span data-ttu-id="68db8-115">Velja skal viðeigandi einingu og velja svo aðgerðina **Úrræðaleit**.</span><span class="sxs-lookup"><span data-stu-id="68db8-115">Choose the relevant entity, and then choose the **Troubleshooting** action.</span></span>  

## <a name="see-also"></a><span data-ttu-id="68db8-116">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="68db8-116">See Also</span></span>
[<span data-ttu-id="68db8-117">Þjónustukerfi</span><span class="sxs-lookup"><span data-stu-id="68db8-117">Service Management</span></span>](service-service.md)
