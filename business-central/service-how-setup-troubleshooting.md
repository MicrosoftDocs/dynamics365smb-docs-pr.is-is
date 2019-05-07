---
title: Setja upp úrræðaleit ferli | Microsoft Docs
description: Lærið hvernig á að setja upp ferli sem hjálpa þjónustuaðilum að koma auga á og leysa úr vandamálum með þjónustuvörum.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: service, service item, troubleshoot, repairs, maintenance
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 2dfa02f0054cab20605281bb1cc580b522b893fd
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2019
ms.locfileid: "937482"
---
# <a name="setting-up-troubleshooting-for-service-items"></a><span data-ttu-id="4d3ee-103">Setja upp úrræðaleit fyrir þjónustuvörur</span><span class="sxs-lookup"><span data-stu-id="4d3ee-103">Setting Up Troubleshooting for Service Items</span></span>
<span data-ttu-id="4d3ee-104">Þú getur sett upp viðmiðunarreglur fyrir úrræðaleit sem hjálpa tæknimönnum að leysa vandamál þegar þeir veita þjónustu.</span><span class="sxs-lookup"><span data-stu-id="4d3ee-104">You can set up troubleshooting guidelines that help technicians solve problems when providing service.</span></span> <span data-ttu-id="4d3ee-105">Viðmiðunarreglur geta t.d. verið listi yfir skref sem framkvæma á við viðgerð, eða röð spurninga til að spyrja um vörurnar.</span><span class="sxs-lookup"><span data-stu-id="4d3ee-105">For example, guidelines might be a list of steps to perform a repair, or a series of questions to ask about the items.</span></span> <span data-ttu-id="4d3ee-106">Þegar leiðbeiningar um úrræðaleit hafa verið settar upp er hægt að úthluta þeim til þjónustuvöruflokka, þjónustuvara og vara.</span><span class="sxs-lookup"><span data-stu-id="4d3ee-106">After you set up troubleshooting guidelines, you can assign them to service item groups, service items, and items.</span></span> <span data-ttu-id="4d3ee-107">Til er afritun stigveldis fyrir viðmiðunarreglur.</span><span class="sxs-lookup"><span data-stu-id="4d3ee-107">There is an inheritance hierarchy for guidelines.</span></span> <span data-ttu-id="4d3ee-108">Ef þú úthlutar þeim til þjónustuvöruflokks, munu vörurnar innan flokksins fá viðmiðunarreglurnar nema þú tiltakir þær fyrir íhlutina.</span><span class="sxs-lookup"><span data-stu-id="4d3ee-108">If you assign them to a service item group, the items included in the group will inherit the guidelines unless you specify them for the items.</span></span> <span data-ttu-id="4d3ee-109">Á sama hátt, munu þjónustuvörur fá viðmiðunarreglurnar frá íhlutunum.</span><span class="sxs-lookup"><span data-stu-id="4d3ee-109">Similarly, service items will inherit guidelines from items.</span></span>  

## <a name="to-set-up-troubleshooting-guidelines"></a><span data-ttu-id="4d3ee-110">Uppsetning leiðbeininga við úrræðaleit</span><span class="sxs-lookup"><span data-stu-id="4d3ee-110">To set up troubleshooting guidelines</span></span>
1. <span data-ttu-id="4d3ee-111">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **úrræðaleit** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="4d3ee-111">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Troubleshooting**, and then choose the related link.</span></span>  
2. <span data-ttu-id="4d3ee-112">Fyllið inn í reitina eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="4d3ee-112">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-assign-troubleshooting-guidelines-to-items-service-items-or-service-item-groups"></a><span data-ttu-id="4d3ee-113">Úthluta leiðbeiningum úrræðaleitar til íhluta, þjónustuvara eða þjónustuvöruflokka</span><span class="sxs-lookup"><span data-stu-id="4d3ee-113">To assign troubleshooting guidelines to items, service items, or service item groups</span></span>
1. <span data-ttu-id="4d3ee-114">Veldu ![Ljósaperu sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Vörur**, **Þjónustuvörur** eða **Þjónustuvöruflokkar** og veldu síðan tengda hlekkinn.</span><span class="sxs-lookup"><span data-stu-id="4d3ee-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, **Service Items**, or **Service Item Groups**, and then choose the related link.</span></span>  
2. <span data-ttu-id="4d3ee-115">Velja skal viðeigandi einingu og velja svo aðgerðina **Úrræðaleit**.</span><span class="sxs-lookup"><span data-stu-id="4d3ee-115">Choose the relevant entity, and then choose the **Troubleshooting** action.</span></span>  

## <a name="see-also"></a><span data-ttu-id="4d3ee-116">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="4d3ee-116">See Also</span></span>
[<span data-ttu-id="4d3ee-117">Þjónustukerfi</span><span class="sxs-lookup"><span data-stu-id="4d3ee-117">Service Management</span></span>](service-service.md)