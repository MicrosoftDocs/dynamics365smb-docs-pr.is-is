---
title: "Tiltaka útlit ávísunar| Microsoft Docs"
description: "Þú getur hannað og prentað þínar ávísanir á mismunandi sniði til að vera í samræmi við staðla."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: print check, customize
ms.date: 10/01/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: d8546cd2f713416e50474848e783d61b4b1dc810
ms.contentlocale: is-is
ms.lasthandoff: 09/28/2018

---
# <a name="define-check-layouts"></a><span data-ttu-id="6a8ca-103">Skilgreina útlit ávísana</span><span class="sxs-lookup"><span data-stu-id="6a8ca-103">Define Check Layouts</span></span>
<span data-ttu-id="6a8ca-104">Hægt er að hanna tékka til þess að uppfylla staðla sem staðaryfirvöld setja.</span><span class="sxs-lookup"><span data-stu-id="6a8ca-104">You can design your checks to conform with the standards set by the local authorities.</span></span> <span data-ttu-id="6a8ca-105">Hægt er að prenta tékkamyndir á Enska, frönsku eða Spænsku.</span><span class="sxs-lookup"><span data-stu-id="6a8ca-105">Check images can be printed in English, French, or Spanish.</span></span>

<span data-ttu-id="6a8ca-106">Tékkar eru hannaðir til að vera prentaðir bæði í Bandrískum og kanadískum tékkamyndsniðum annað á sniðinu tékki-svunta-tékki  eða á sniðinu svunta-svunta-tékki.</span><span class="sxs-lookup"><span data-stu-id="6a8ca-106">Checks are designed to print in both the United States and Canadian check image formats in either a check-stub-check format or a stub-stub-check format.</span></span>

## <a name="to-define-check-layouts"></a><span data-ttu-id="6a8ca-107">Skilgreina útlit ávísana</span><span class="sxs-lookup"><span data-stu-id="6a8ca-107">To define check layouts</span></span>
1. <span data-ttu-id="6a8ca-108">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **bankareikningar skýrsluvals** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="6a8ca-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Report Selections Bank Account**, and then choose the related link.</span></span>
2. <span data-ttu-id="6a8ca-109">Í glugganum **Skýrsluval - Bankareikningur** í reitnum **Notkun** skal velja **Reikningur**.</span><span class="sxs-lookup"><span data-stu-id="6a8ca-109">In the **Report Selection - Bank Acc.** window, in the **Usage** field, select **Check**.</span></span>
3. <span data-ttu-id="6a8ca-110">Eitt af eftirfarandi skýrslukennum er valið:</span><span class="sxs-lookup"><span data-stu-id="6a8ca-110">Select one of the following report IDs.</span></span>

| <span data-ttu-id="6a8ca-111">Kenni skýrslu</span><span class="sxs-lookup"><span data-stu-id="6a8ca-111">Report ID</span></span> | <span data-ttu-id="6a8ca-112">Skýrsluheiti</span><span class="sxs-lookup"><span data-stu-id="6a8ca-112">Report Name</span></span> | <span data-ttu-id="6a8ca-113">Lýsing</span><span class="sxs-lookup"><span data-stu-id="6a8ca-113">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="6a8ca-114">1401</span><span class="sxs-lookup"><span data-stu-id="6a8ca-114">1401</span></span> |<span data-ttu-id="6a8ca-115">Tékki</span><span class="sxs-lookup"><span data-stu-id="6a8ca-115">Check</span></span> |<span data-ttu-id="6a8ca-116">Þetta er sjálfgefin skýrsla.</span><span class="sxs-lookup"><span data-stu-id="6a8ca-116">This is the default report.</span></span> |
| <span data-ttu-id="6a8ca-117">10401</span><span class="sxs-lookup"><span data-stu-id="6a8ca-117">10401</span></span> |<span data-ttu-id="6a8ca-118">Tékki (Svunta/Svunta/tékki)</span><span class="sxs-lookup"><span data-stu-id="6a8ca-118">Check (Stub/Stub/Check)</span></span> |<span data-ttu-id="6a8ca-119">þessari skýrslu er hannaðar til að prenta tékka á sniðinu svunta/svunta/tékki.</span><span class="sxs-lookup"><span data-stu-id="6a8ca-119">This report is designed to print checks in a stub/stub/check format.</span></span> |
| <span data-ttu-id="6a8ca-120">10411</span><span class="sxs-lookup"><span data-stu-id="6a8ca-120">10411</span></span> |<span data-ttu-id="6a8ca-121">Tékki (Svunta/tékki/svunta)</span><span class="sxs-lookup"><span data-stu-id="6a8ca-121">Check (Stub/Check/Stub)</span></span> |<span data-ttu-id="6a8ca-122">Þessari skýrslu er hannaðar til að prenta tékka á sniðinu tékki/svunta/tékki.</span><span class="sxs-lookup"><span data-stu-id="6a8ca-122">This report is designed to print checks in a check/stub/check format.</span></span> |

<span data-ttu-id="6a8ca-123">Þegar settar hafa verið upp útlit tékka er hægt að prenta tékka úr glugganum **greiðslubók** .</span><span class="sxs-lookup"><span data-stu-id="6a8ca-123">When you have set up check layouts, you can print checks from the **Payment Journal** window.</span></span> <span data-ttu-id="6a8ca-124">Nánari upplýsingar eru í [Vinna með tékka](payables-how-work-checks.md).</span><span class="sxs-lookup"><span data-stu-id="6a8ca-124">For more information, see [Work with Checks](payables-how-work-checks.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="6a8ca-125">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="6a8ca-125">See Also</span></span>
[<span data-ttu-id="6a8ca-126">Stjórna skuldum</span><span class="sxs-lookup"><span data-stu-id="6a8ca-126">Managing Payables</span></span>](payables-manage-payables.md)  
<span data-ttu-id="6a8ca-127">[Stjórnun bankareikninga](bank-manage-bank-accounts.md) </span><span class="sxs-lookup"><span data-stu-id="6a8ca-127">[Managing Bank Accounts](bank-manage-bank-accounts.md) </span></span>  
[<span data-ttu-id="6a8ca-128">Að klára Ferli í lok tímabila</span><span class="sxs-lookup"><span data-stu-id="6a8ca-128">Completing Period-End Processes</span></span>](year-how-complete-period-end-processes.md)  
<span data-ttu-id="6a8ca-129">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="6a8ca-129">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="6a8ca-130">Almenn viðskiptavirkni</span><span class="sxs-lookup"><span data-stu-id="6a8ca-130">General Business Functionality</span></span>](ui-across-business-areas.md)

