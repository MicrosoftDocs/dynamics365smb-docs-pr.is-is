---
title: "Tiltaka útlit ávísunar| Microsoft Docs"
description: "Þú getur hannað og prentað þínar ávísanir á mismunandi sniði til að vera í samræmi við staðla."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: print check, customize
ms.date: 06/15/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: a2db2860846cd9b8010222faf580f0c9889e39a4
ms.contentlocale: is-is
ms.lasthandoff: 09/11/2017


---
# <a name="how-to-define-check-layouts"></a><span data-ttu-id="ae20f-103">Hvernig á að: Skilgreina útlit ávísana</span><span class="sxs-lookup"><span data-stu-id="ae20f-103">How to: Define Check Layouts</span></span>
<span data-ttu-id="ae20f-104">Hægt er að hanna tékka til þess að uppfylla staðla sem staðaryfirvöld setja.</span><span class="sxs-lookup"><span data-stu-id="ae20f-104">You can design your checks to conform with the standards set by the local authorities.</span></span> <span data-ttu-id="ae20f-105">Hægt er að prenta tékkamyndir á Enska, frönsku eða Spænsku.</span><span class="sxs-lookup"><span data-stu-id="ae20f-105">Check images can be printed in English, French, or Spanish.</span></span>

<span data-ttu-id="ae20f-106">Tékkar eru hannaðir til að vera prentaðir bæði í Bandrískum og kanadískum tékkamyndsniðum annað á sniðinu tékki-svunta-tékki  eða á sniðinu svunta-svunta-tékki.</span><span class="sxs-lookup"><span data-stu-id="ae20f-106">Checks are designed to print in both the United States and Canadian check image formats in either a check-stub-check format or a stub-stub-check format.</span></span>

## <a name="to-define-check-layouts"></a><span data-ttu-id="ae20f-107">Skilgreina útlit ávísana</span><span class="sxs-lookup"><span data-stu-id="ae20f-107">To define check layouts</span></span>
1. <span data-ttu-id="ae20f-108">Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Skýrsluval Bankareikningur** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="ae20f-108">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Report Selections Bank Account**, and then choose the related link.</span></span>
2. <span data-ttu-id="ae20f-109">Í glugganum **Skýrsluval - Bankareikn.**</span><span class="sxs-lookup"><span data-stu-id="ae20f-109">In the **Report Selection - Bank Acc.**</span></span> <span data-ttu-id="ae20f-110">í  **notkun** reitnum, veljið **tékka**.</span><span class="sxs-lookup"><span data-stu-id="ae20f-110">window, in the **Usage** field, select **Check**.</span></span>
3. <span data-ttu-id="ae20f-111">Eitt af eftirfarandi skýrslukennum er valið:</span><span class="sxs-lookup"><span data-stu-id="ae20f-111">Select one of the following report IDs.</span></span>

| <span data-ttu-id="ae20f-112">Kenni skýrslu</span><span class="sxs-lookup"><span data-stu-id="ae20f-112">Report ID</span></span> | <span data-ttu-id="ae20f-113">Skýrsluheiti</span><span class="sxs-lookup"><span data-stu-id="ae20f-113">Report Name</span></span> | <span data-ttu-id="ae20f-114">Lýsing</span><span class="sxs-lookup"><span data-stu-id="ae20f-114">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="ae20f-115">1401</span><span class="sxs-lookup"><span data-stu-id="ae20f-115">1401</span></span> |<span data-ttu-id="ae20f-116">Tékki</span><span class="sxs-lookup"><span data-stu-id="ae20f-116">Check</span></span> |<span data-ttu-id="ae20f-117">Þetta er sjálfgefin skýrsla.</span><span class="sxs-lookup"><span data-stu-id="ae20f-117">This is the default report.</span></span> |
| <span data-ttu-id="ae20f-118">10401</span><span class="sxs-lookup"><span data-stu-id="ae20f-118">10401</span></span> |<span data-ttu-id="ae20f-119">Tékki (Svunta/Svunta/tékki)</span><span class="sxs-lookup"><span data-stu-id="ae20f-119">Check (Stub/Stub/Check)</span></span> |<span data-ttu-id="ae20f-120">þessari skýrslu er hannaðar til að prenta tékka á sniðinu svunta/svunta/tékki.</span><span class="sxs-lookup"><span data-stu-id="ae20f-120">This report is designed to print checks in a stub/stub/check format.</span></span> |
| <span data-ttu-id="ae20f-121">10411</span><span class="sxs-lookup"><span data-stu-id="ae20f-121">10411</span></span> |<span data-ttu-id="ae20f-122">Tékki (Svunta/tékki/svunta)</span><span class="sxs-lookup"><span data-stu-id="ae20f-122">Check (Stub/Check/Stub)</span></span> |<span data-ttu-id="ae20f-123">Þessari skýrslu er hannaðar til að prenta tékka á sniðinu tékki/svunta/tékki.</span><span class="sxs-lookup"><span data-stu-id="ae20f-123">This report is designed to print checks in a check/stub/check format.</span></span> |

<span data-ttu-id="ae20f-124">Þegar settar hafa verið upp útlit tékka er hægt að prenta tékka úr glugganum **greiðslubók** .</span><span class="sxs-lookup"><span data-stu-id="ae20f-124">When you have set up check layouts, you can print checks from the **Payment Journal** window.</span></span> <span data-ttu-id="ae20f-125">Frekari upplýsingar, sjá [Hvernig á að: vinna með ávísanir](payables-how-work-checks.md).</span><span class="sxs-lookup"><span data-stu-id="ae20f-125">For more information, see [How to: Work with Checks](payables-how-work-checks.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="ae20f-126">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="ae20f-126">See Also</span></span>
[<span data-ttu-id="ae20f-127">Stjórna skuldum</span><span class="sxs-lookup"><span data-stu-id="ae20f-127">Managing Payables</span></span>](payables-manage-payables.md)  
<span data-ttu-id="ae20f-128">[Stjórnun bankareikninga](bank-manage-bank-accounts.md) </span><span class="sxs-lookup"><span data-stu-id="ae20f-128">[Managing Bank Accounts](bank-manage-bank-accounts.md) </span></span>  
[<span data-ttu-id="ae20f-129">Að klára Ferli í lok tímabila</span><span class="sxs-lookup"><span data-stu-id="ae20f-129">Completing Period-End Processes</span></span>](year-how-complete-period-end-processes.md)  
<span data-ttu-id="ae20f-130">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="ae20f-130">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="ae20f-131">Almenn viðskiptavirkni</span><span class="sxs-lookup"><span data-stu-id="ae20f-131">General Business Functionality</span></span>](ui-across-business-areas.md)

