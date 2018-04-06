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
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: dd745186e4518c2005e34e6b2cbbc8925fd8931e
ms.contentlocale: is-is
ms.lasthandoff: 03/22/2018

---
# <a name="define-check-layouts"></a><span data-ttu-id="e9808-103">Skilgreina útlit ávísana</span><span class="sxs-lookup"><span data-stu-id="e9808-103">Define Check Layouts</span></span>
<span data-ttu-id="e9808-104">Hægt er að hanna tékka til þess að uppfylla staðla sem staðaryfirvöld setja.</span><span class="sxs-lookup"><span data-stu-id="e9808-104">You can design your checks to conform with the standards set by the local authorities.</span></span> <span data-ttu-id="e9808-105">Hægt er að prenta tékkamyndir á Enska, frönsku eða Spænsku.</span><span class="sxs-lookup"><span data-stu-id="e9808-105">Check images can be printed in English, French, or Spanish.</span></span>

<span data-ttu-id="e9808-106">Tékkar eru hannaðir til að vera prentaðir bæði í Bandrískum og kanadískum tékkamyndsniðum annað á sniðinu tékki-svunta-tékki  eða á sniðinu svunta-svunta-tékki.</span><span class="sxs-lookup"><span data-stu-id="e9808-106">Checks are designed to print in both the United States and Canadian check image formats in either a check-stub-check format or a stub-stub-check format.</span></span>

## <a name="to-define-check-layouts"></a><span data-ttu-id="e9808-107">Skilgreina útlit ávísana</span><span class="sxs-lookup"><span data-stu-id="e9808-107">To define check layouts</span></span>
1. <span data-ttu-id="e9808-108">Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Skýrsluval Bankareikningur** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="e9808-108">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Report Selections Bank Account**, and then choose the related link.</span></span>
2. <span data-ttu-id="e9808-109">Í glugganum **Skýrsluval - Bankareikningur** í reitnum **Notkun** skal velja **Reikningur**.</span><span class="sxs-lookup"><span data-stu-id="e9808-109">In the **Report Selection - Bank Acc.** window, in the **Usage** field, select **Check**.</span></span>
3. <span data-ttu-id="e9808-110">Eitt af eftirfarandi skýrslukennum er valið:</span><span class="sxs-lookup"><span data-stu-id="e9808-110">Select one of the following report IDs.</span></span>

| <span data-ttu-id="e9808-111">Kenni skýrslu</span><span class="sxs-lookup"><span data-stu-id="e9808-111">Report ID</span></span> | <span data-ttu-id="e9808-112">Skýrsluheiti</span><span class="sxs-lookup"><span data-stu-id="e9808-112">Report Name</span></span> | <span data-ttu-id="e9808-113">Lýsing</span><span class="sxs-lookup"><span data-stu-id="e9808-113">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="e9808-114">1401</span><span class="sxs-lookup"><span data-stu-id="e9808-114">1401</span></span> |<span data-ttu-id="e9808-115">Tékki</span><span class="sxs-lookup"><span data-stu-id="e9808-115">Check</span></span> |<span data-ttu-id="e9808-116">Þetta er sjálfgefin skýrsla.</span><span class="sxs-lookup"><span data-stu-id="e9808-116">This is the default report.</span></span> |
| <span data-ttu-id="e9808-117">10401</span><span class="sxs-lookup"><span data-stu-id="e9808-117">10401</span></span> |<span data-ttu-id="e9808-118">Tékki (Svunta/Svunta/tékki)</span><span class="sxs-lookup"><span data-stu-id="e9808-118">Check (Stub/Stub/Check)</span></span> |<span data-ttu-id="e9808-119">þessari skýrslu er hannaðar til að prenta tékka á sniðinu svunta/svunta/tékki.</span><span class="sxs-lookup"><span data-stu-id="e9808-119">This report is designed to print checks in a stub/stub/check format.</span></span> |
| <span data-ttu-id="e9808-120">10411</span><span class="sxs-lookup"><span data-stu-id="e9808-120">10411</span></span> |<span data-ttu-id="e9808-121">Tékki (Svunta/tékki/svunta)</span><span class="sxs-lookup"><span data-stu-id="e9808-121">Check (Stub/Check/Stub)</span></span> |<span data-ttu-id="e9808-122">Þessari skýrslu er hannaðar til að prenta tékka á sniðinu tékki/svunta/tékki.</span><span class="sxs-lookup"><span data-stu-id="e9808-122">This report is designed to print checks in a check/stub/check format.</span></span> |

<span data-ttu-id="e9808-123">Þegar settar hafa verið upp útlit tékka er hægt að prenta tékka úr glugganum **greiðslubók** .</span><span class="sxs-lookup"><span data-stu-id="e9808-123">When you have set up check layouts, you can print checks from the **Payment Journal** window.</span></span> <span data-ttu-id="e9808-124">Nánari upplýsingar eru í [Vinna með tékka](payables-how-work-checks.md).</span><span class="sxs-lookup"><span data-stu-id="e9808-124">For more information, see [Work with Checks](payables-how-work-checks.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="e9808-125">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="e9808-125">See Also</span></span>
[<span data-ttu-id="e9808-126">Stjórna skuldum</span><span class="sxs-lookup"><span data-stu-id="e9808-126">Managing Payables</span></span>](payables-manage-payables.md)  
<span data-ttu-id="e9808-127">[Stjórnun bankareikninga](bank-manage-bank-accounts.md) </span><span class="sxs-lookup"><span data-stu-id="e9808-127">[Managing Bank Accounts](bank-manage-bank-accounts.md) </span></span>  
[<span data-ttu-id="e9808-128">Að klára Ferli í lok tímabila</span><span class="sxs-lookup"><span data-stu-id="e9808-128">Completing Period-End Processes</span></span>](year-how-complete-period-end-processes.md)  
<span data-ttu-id="e9808-129">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="e9808-129">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="e9808-130">Almenn viðskiptavirkni</span><span class="sxs-lookup"><span data-stu-id="e9808-130">General Business Functionality</span></span>](ui-across-business-areas.md)

