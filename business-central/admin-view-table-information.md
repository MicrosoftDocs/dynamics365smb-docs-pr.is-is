---
title: Skoða töfluupplýsingar
description: Kynntu þér hvernig hægt er að skoða upplýsingar um gagnagrunnstöflur beint úr viðmóti biðlara í Business Central.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 10/01/2020
ms.author: jswymer
ms.openlocfilehash: 72e220aa310515c665ce85bd43f4ebd3aac157d0
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/01/2020
ms.locfileid: "3922268"
---
# <a name="viewing-table-information"></a><span data-ttu-id="62753-103">Skoðun töfluupplýsinga</span><span class="sxs-lookup"><span data-stu-id="62753-103">Viewing Table Information</span></span>

<span data-ttu-id="62753-104">Á síðunni **8700 töfluupplýsingar** fást upplýsingar um öll kerfi og fyrirtækjatöflur í Business Central-lausn.</span><span class="sxs-lookup"><span data-stu-id="62753-104">The page **8700 Table Information** provides information about all system and business tables in a Business Central solution.</span></span> <span data-ttu-id="62753-105">Á síðunni birtast upplýsingar um magn gagna sem töflurnar innihalda.</span><span class="sxs-lookup"><span data-stu-id="62753-105">In particular, the page displays information about the amount of data the tables contain.</span></span>

<span data-ttu-id="62753-106">Þessar upplýsingar eru gagnlegar til að leysa úr vandamálum við úrræðaleit, þar sem þær sýna dreifingu á gagnamagni á milli taflna.</span><span class="sxs-lookup"><span data-stu-id="62753-106">This information is useful for troubleshooting performance problems, because let's you see the distribution of data size across tables.</span></span>

## <a name="viewing-table-information"></a><span data-ttu-id="62753-107">Skoða upplýsingar um málatöflu</span><span class="sxs-lookup"><span data-stu-id="62753-107">Viewing table information</span></span>

<span data-ttu-id="62753-108">Til að opna þessa síðu skaltu velja táknið ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu tákn"), slá inn **Töfluupplýsingar** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="62753-108">To open this page, select the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Table Information** , and then choose the related link.</span></span>

<span data-ttu-id="62753-109">Eftirfarandi tafla lýsir upplýsingunum sem eru veittar fyrir hverja töflu:</span><span class="sxs-lookup"><span data-stu-id="62753-109">The following table describes the information provided for each table:</span></span>

|<span data-ttu-id="62753-110">Dálkur</span><span class="sxs-lookup"><span data-stu-id="62753-110">Column</span></span>|<span data-ttu-id="62753-111">Description</span><span class="sxs-lookup"><span data-stu-id="62753-111">Description</span></span>|
|------|-----------|
|<span data-ttu-id="62753-112">Heiti fyrirtækis</span><span class="sxs-lookup"><span data-stu-id="62753-112">Company Name</span></span>|<span data-ttu-id="62753-113">Heiti fyrirtækisins, ef það er til staðar, sem taflan tilheyrir.</span><span class="sxs-lookup"><span data-stu-id="62753-113">The name of the company, if any, that the table belongs to.</span></span>|
|<span data-ttu-id="62753-114">Töfluheiti</span><span class="sxs-lookup"><span data-stu-id="62753-114">Table Name</span></span>|<span data-ttu-id="62753-115">Heiti töflunnar.</span><span class="sxs-lookup"><span data-stu-id="62753-115">The name of the table.</span></span>|
|<span data-ttu-id="62753-116">Nr. töflu.</span><span class="sxs-lookup"><span data-stu-id="62753-116">Table No.</span></span>|<span data-ttu-id="62753-117">Kenni töflunnar</span><span class="sxs-lookup"><span data-stu-id="62753-117">The ID of the table</span></span>|
|<span data-ttu-id="62753-118">Fj.</span><span class="sxs-lookup"><span data-stu-id="62753-118">No.</span></span> <span data-ttu-id="62753-119">fjöldi færslna</span><span class="sxs-lookup"><span data-stu-id="62753-119">of Records</span></span>|<span data-ttu-id="62753-120">Heildarfjöldi færslna sem eru vistaðar í töflunni.</span><span class="sxs-lookup"><span data-stu-id="62753-120">The total number of records stored in the table.</span></span>|
|<span data-ttu-id="62753-121">Stærð færslu</span><span class="sxs-lookup"><span data-stu-id="62753-121">Record Size</span></span>|<span data-ttu-id="62753-122">Meðalstærð færslu í KB/færslu.</span><span class="sxs-lookup"><span data-stu-id="62753-122">The average record size in KB/record.</span></span> <span data-ttu-id="62753-123">Gildið er reiknað með eftirfarandi formúlu: 1024(Size)/(No.</span><span class="sxs-lookup"><span data-stu-id="62753-123">The value is calculated using the following formula: 1024(Size)/(No.</span></span> <span data-ttu-id="62753-124">færslna).</span><span class="sxs-lookup"><span data-stu-id="62753-124">of Records)\`.</span></span> |

## <a name="see-also"></a><span data-ttu-id="62753-125">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="62753-125">See Also</span></span>

[<span data-ttu-id="62753-126">Eftirlit með síðum</span><span class="sxs-lookup"><span data-stu-id="62753-126">Inspecting Pages</span></span>](across-inspect-page.md)  
[<span data-ttu-id="62753-127">Afkastagreinar fyrir þróunaraðila</span><span class="sxs-lookup"><span data-stu-id="62753-127">Performance Articles For Developers</span></span>](/dynamics365/business-central/dev-itpro/performance/performance-developer)  
