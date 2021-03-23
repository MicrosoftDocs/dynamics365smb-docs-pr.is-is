---
title: Skoða töfluupplýsingar
description: Kynntu þér hvernig hægt er að skoða upplýsingar um gagnagrunnstöflur beint úr viðmóti biðlara í Business Central.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 10/01/2020
ms.author: jswymer
ms.openlocfilehash: a4695594573056ec492bc15c29d1b6fca3100e97
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5388675"
---
# <a name="viewing-table-information"></a><span data-ttu-id="1194e-103">Skoðun töfluupplýsinga</span><span class="sxs-lookup"><span data-stu-id="1194e-103">Viewing Table Information</span></span>

<span data-ttu-id="1194e-104">Á síðunni **8700 töfluupplýsingar** fást upplýsingar um öll kerfi og fyrirtækjatöflur í Business Central-lausn.</span><span class="sxs-lookup"><span data-stu-id="1194e-104">The page **8700 Table Information** provides information about all system and business tables in a Business Central solution.</span></span> <span data-ttu-id="1194e-105">Á síðunni birtast upplýsingar um magn gagna sem töflurnar innihalda.</span><span class="sxs-lookup"><span data-stu-id="1194e-105">In particular, the page displays information about the amount of data the tables contain.</span></span>

<span data-ttu-id="1194e-106">Þessar upplýsingar eru gagnlegar til að leysa úr vandamálum við úrræðaleit, þar sem þær sýna dreifingu á gagnamagni á milli taflna.</span><span class="sxs-lookup"><span data-stu-id="1194e-106">This information is useful for troubleshooting performance problems, because let's you see the distribution of data size across tables.</span></span>

## <a name="viewing-table-information"></a><span data-ttu-id="1194e-107">Skoða upplýsingar um málatöflu</span><span class="sxs-lookup"><span data-stu-id="1194e-107">Viewing table information</span></span>

<span data-ttu-id="1194e-108">Til að opna þessa síðu skaltu velja táknið ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu tákn"), slá inn **Töfluupplýsingar** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="1194e-108">To open this page, select the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Table Information**, and then choose the related link.</span></span>

<span data-ttu-id="1194e-109">Eftirfarandi tafla lýsir upplýsingunum sem eru veittar fyrir hverja töflu:</span><span class="sxs-lookup"><span data-stu-id="1194e-109">The following table describes the information provided for each table:</span></span>

|<span data-ttu-id="1194e-110">Dálkur</span><span class="sxs-lookup"><span data-stu-id="1194e-110">Column</span></span>|<span data-ttu-id="1194e-111">Description</span><span class="sxs-lookup"><span data-stu-id="1194e-111">Description</span></span>|
|------|-----------|
|<span data-ttu-id="1194e-112">Heiti fyrirtækis</span><span class="sxs-lookup"><span data-stu-id="1194e-112">Company Name</span></span>|<span data-ttu-id="1194e-113">Heiti fyrirtækisins, ef það er til staðar, sem taflan tilheyrir.</span><span class="sxs-lookup"><span data-stu-id="1194e-113">The name of the company, if any, that the table belongs to.</span></span>|
|<span data-ttu-id="1194e-114">Töfluheiti</span><span class="sxs-lookup"><span data-stu-id="1194e-114">Table Name</span></span>|<span data-ttu-id="1194e-115">Heiti töflunnar.</span><span class="sxs-lookup"><span data-stu-id="1194e-115">The name of the table.</span></span>|
|<span data-ttu-id="1194e-116">Nr. töflu.</span><span class="sxs-lookup"><span data-stu-id="1194e-116">Table No.</span></span>|<span data-ttu-id="1194e-117">Kenni töflunnar</span><span class="sxs-lookup"><span data-stu-id="1194e-117">The ID of the table</span></span>|
|<span data-ttu-id="1194e-118">Fj.</span><span class="sxs-lookup"><span data-stu-id="1194e-118">No.</span></span> <span data-ttu-id="1194e-119">fjöldi færslna</span><span class="sxs-lookup"><span data-stu-id="1194e-119">of Records</span></span>|<span data-ttu-id="1194e-120">Heildarfjöldi færslna sem eru vistaðar í töflunni.</span><span class="sxs-lookup"><span data-stu-id="1194e-120">The total number of records stored in the table.</span></span>|
|<span data-ttu-id="1194e-121">Stærð færslu</span><span class="sxs-lookup"><span data-stu-id="1194e-121">Record Size</span></span>|<span data-ttu-id="1194e-122">Meðalstærð færslu í KB/færslu.</span><span class="sxs-lookup"><span data-stu-id="1194e-122">The average record size in KB/record.</span></span> <span data-ttu-id="1194e-123">Gildið er reiknað með eftirfarandi formúlu: 1024(Size)/(No.</span><span class="sxs-lookup"><span data-stu-id="1194e-123">The value is calculated using the following formula: 1024(Size)/(No.</span></span> <span data-ttu-id="1194e-124">færslna).</span><span class="sxs-lookup"><span data-stu-id="1194e-124">of Records)\`.</span></span> |

## <a name="see-also"></a><span data-ttu-id="1194e-125">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="1194e-125">See Also</span></span>

[<span data-ttu-id="1194e-126">Eftirlit með síðum</span><span class="sxs-lookup"><span data-stu-id="1194e-126">Inspecting Pages</span></span>](across-inspect-page.md)  
[<span data-ttu-id="1194e-127">Afkastagreinar fyrir þróunaraðila</span><span class="sxs-lookup"><span data-stu-id="1194e-127">Performance Articles For Developers</span></span>](/dynamics365/business-central/dev-itpro/performance/performance-developer)  


[!INCLUDE[footer-include](includes/footer-banner.md)]