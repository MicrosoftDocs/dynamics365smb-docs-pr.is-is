---
title: Skoða töfluupplýsingar
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 04/20/2020
ms.author: jswymer
ms.openlocfilehash: de93063a60e6b64405b1491a67489c8bfa4657ad
ms.sourcegitcommit: 99915b493a7e49d12c530f2f9fda1fcedb518b6e
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/21/2020
ms.locfileid: "3275319"
---
# <a name="viewing-table-information"></a><span data-ttu-id="7f55f-102">Skoðun töfluupplýsinga</span><span class="sxs-lookup"><span data-stu-id="7f55f-102">Viewing Table Information</span></span>

<span data-ttu-id="7f55f-103">Á síðunni **8700 töfluupplýsingar** fást upplýsingar um öll kerfi og fyrirtækjatöflur í Business Central-lausn.</span><span class="sxs-lookup"><span data-stu-id="7f55f-103">The page **8700 Table Information** provides information about all system and business tables in a Business Central solution.</span></span> <span data-ttu-id="7f55f-104">Á síðunni birtast upplýsingar um magn gagna sem töflurnar innihalda.</span><span class="sxs-lookup"><span data-stu-id="7f55f-104">In particular, the page displays information about the amount of data the tables contain.</span></span>

<span data-ttu-id="7f55f-105">Þessar upplýsingar eru gagnlegar til að leysa úr vandamálum við úrræðaleit, þar sem þær sýna dreifingu á gagnamagni á milli taflna.</span><span class="sxs-lookup"><span data-stu-id="7f55f-105">This information is useful for troubleshooting performance problems, because let's you see the distribution of data size across tables.</span></span>

## <a name="viewing-table-information"></a><span data-ttu-id="7f55f-106">Skoða upplýsingar um málatöflu</span><span class="sxs-lookup"><span data-stu-id="7f55f-106">Viewing table information</span></span>

<span data-ttu-id="7f55f-107">Til að opna þessa síðu skaltu velja táknið ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu tákn"), slá inn **Töfluupplýsingar** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="7f55f-107">To open this page, select the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Table Information**, and then choose the related link.</span></span>

<span data-ttu-id="7f55f-108">Eftirfarandi tafla lýsir upplýsingunum sem eru veittar fyrir hverja töflu:</span><span class="sxs-lookup"><span data-stu-id="7f55f-108">The following table describes the information provided for each table:</span></span>

|<span data-ttu-id="7f55f-109">Dálkur</span><span class="sxs-lookup"><span data-stu-id="7f55f-109">Column</span></span>|<span data-ttu-id="7f55f-110">Description</span><span class="sxs-lookup"><span data-stu-id="7f55f-110">Description</span></span>|
|------|-----------|
|<span data-ttu-id="7f55f-111">Heiti fyrirtækis</span><span class="sxs-lookup"><span data-stu-id="7f55f-111">Company Name</span></span>|<span data-ttu-id="7f55f-112">Heiti fyrirtækisins, ef það er til staðar, sem taflan tilheyrir.</span><span class="sxs-lookup"><span data-stu-id="7f55f-112">The name of the company, if any, that the table belongs to.</span></span>|
|<span data-ttu-id="7f55f-113">Töfluheiti</span><span class="sxs-lookup"><span data-stu-id="7f55f-113">Table Name</span></span>|<span data-ttu-id="7f55f-114">Heiti töflunnar.</span><span class="sxs-lookup"><span data-stu-id="7f55f-114">The name of the table.</span></span>|
|<span data-ttu-id="7f55f-115">Nr. töflu.</span><span class="sxs-lookup"><span data-stu-id="7f55f-115">Table No.</span></span>|<span data-ttu-id="7f55f-116">Kenni töflunnar</span><span class="sxs-lookup"><span data-stu-id="7f55f-116">The ID of the table</span></span>|
|<span data-ttu-id="7f55f-117">Fj.</span><span class="sxs-lookup"><span data-stu-id="7f55f-117">No.</span></span> <span data-ttu-id="7f55f-118">fjöldi færslna</span><span class="sxs-lookup"><span data-stu-id="7f55f-118">of Records</span></span>|<span data-ttu-id="7f55f-119">Heildarfjöldi færslna sem eru vistaðar í töflunni.</span><span class="sxs-lookup"><span data-stu-id="7f55f-119">The total number of records stored in the table.</span></span>|
|<span data-ttu-id="7f55f-120">Stærð færslu</span><span class="sxs-lookup"><span data-stu-id="7f55f-120">Record Size</span></span>|<span data-ttu-id="7f55f-121">Meðalstærð færslu í KB/færslu.</span><span class="sxs-lookup"><span data-stu-id="7f55f-121">The average record size in KB/record.</span></span> <span data-ttu-id="7f55f-122">Gildið er reiknað með eftirfarandi formúlu: 1024(stærð)/(fjöldi</span><span class="sxs-lookup"><span data-stu-id="7f55f-122">The value is calculated using the following formula: 1024(Size)/(No.</span></span> <span data-ttu-id="7f55f-123">færslna).</span><span class="sxs-lookup"><span data-stu-id="7f55f-123">of Records)\`.</span></span> |

## <a name="see-also"></a><span data-ttu-id="7f55f-124">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="7f55f-124">See Also</span></span>

[<span data-ttu-id="7f55f-125">Eftirlit með síðum</span><span class="sxs-lookup"><span data-stu-id="7f55f-125">Inspecting Pages</span></span>](across-inspect-page.md)  
[<span data-ttu-id="7f55f-126">Afkastagreinar fyrir þróunaraðila</span><span class="sxs-lookup"><span data-stu-id="7f55f-126">Performance Articles For Developers</span></span>](/dynamics365/business-central/dev-itpro/performance/performance-developer)  
