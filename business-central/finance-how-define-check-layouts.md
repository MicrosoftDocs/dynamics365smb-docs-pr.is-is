---
title: Tiltaka útlit ávísunar| Microsoft Docs
description: Þú getur hannað og prentað þínar ávísanir á mismunandi sniði til að vera í samræmi við staðla.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: print check, customize
ms.date: 04/24/2019
ms.author: edupont
ms.openlocfilehash: f2b7fa01cff36e3aab335f7d5921954343c69b74
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/29/2019
ms.locfileid: "1243596"
---
# <a name="define-check-layouts"></a><span data-ttu-id="c19b4-103">Skilgreina útlit ávísana</span><span class="sxs-lookup"><span data-stu-id="c19b4-103">Define Check Layouts</span></span>
<span data-ttu-id="c19b4-104">Hægt er að hanna tékka til þess að uppfylla staðla sem staðaryfirvöld setja.</span><span class="sxs-lookup"><span data-stu-id="c19b4-104">You can design your checks to conform with the standards set by the local authorities.</span></span> <span data-ttu-id="c19b4-105">Hægt er að prenta tékkamyndir á Enska, frönsku eða Spænsku.</span><span class="sxs-lookup"><span data-stu-id="c19b4-105">Check images can be printed in English, French, or Spanish.</span></span>

<span data-ttu-id="c19b4-106">Tékkar eru hannaðir til að vera prentaðir bæði í Bandrískum og kanadískum tékkamyndsniðum annað á sniðinu tékki-svunta-tékki  eða á sniðinu svunta-svunta-tékki.</span><span class="sxs-lookup"><span data-stu-id="c19b4-106">Checks are designed to print in both the United States and Canadian check image formats in either a check-stub-check format or a stub-stub-check format.</span></span>

## <a name="to-define-check-layouts"></a><span data-ttu-id="c19b4-107">Skilgreina útlit ávísana</span><span class="sxs-lookup"><span data-stu-id="c19b4-107">To define check layouts</span></span>
1. <span data-ttu-id="c19b4-108">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **bankareikningar skýrsluvals** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="c19b4-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Report Selections Bank Account**, and then choose the related link.</span></span>
2. <span data-ttu-id="c19b4-109">Á síðunni **Skýrsluval - Bankareikningur** í reitnum **Notkun** skal velja **Reikningur**.</span><span class="sxs-lookup"><span data-stu-id="c19b4-109">On the **Report Selection - Bank Acc.** page, in the **Usage** field, select **Check**.</span></span>
3. <span data-ttu-id="c19b4-110">Eitt af eftirfarandi skýrslukennum er valið:</span><span class="sxs-lookup"><span data-stu-id="c19b4-110">Select one of the following report IDs.</span></span>

  | <span data-ttu-id="c19b4-111">Kenni skýrslu</span><span class="sxs-lookup"><span data-stu-id="c19b4-111">Report ID</span></span> | <span data-ttu-id="c19b4-112">Skýrsluheiti</span><span class="sxs-lookup"><span data-stu-id="c19b4-112">Report Name</span></span> | <span data-ttu-id="c19b4-113">Description</span><span class="sxs-lookup"><span data-stu-id="c19b4-113">Description</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="c19b4-114">1401</span><span class="sxs-lookup"><span data-stu-id="c19b4-114">1401</span></span> |<span data-ttu-id="c19b4-115">Tékki</span><span class="sxs-lookup"><span data-stu-id="c19b4-115">Check</span></span> |<span data-ttu-id="c19b4-116">Þetta er sjálfgefin skýrsla.</span><span class="sxs-lookup"><span data-stu-id="c19b4-116">This is the default report.</span></span> |
  | <span data-ttu-id="c19b4-117">10411</span><span class="sxs-lookup"><span data-stu-id="c19b4-117">10411</span></span> |<span data-ttu-id="c19b4-118">Tékki (Svunta/Svunta/tékki)</span><span class="sxs-lookup"><span data-stu-id="c19b4-118">Check (Stub/Stub/Check)</span></span> |<span data-ttu-id="c19b4-119">þessari skýrslu er hannaðar til að prenta tékka á sniðinu svunta/svunta/tékki.</span><span class="sxs-lookup"><span data-stu-id="c19b4-119">This report is designed to print checks in a stub/stub/check format.</span></span> |
  | <span data-ttu-id="c19b4-120">10412</span><span class="sxs-lookup"><span data-stu-id="c19b4-120">10412</span></span> |<span data-ttu-id="c19b4-121">Tékki (Svunta/tékki/svunta)</span><span class="sxs-lookup"><span data-stu-id="c19b4-121">Check (Stub/Check/Stub)</span></span> |<span data-ttu-id="c19b4-122">Þessari skýrslu er hannaðar til að prenta tékka á sniðinu svunta/tékki/svunta.</span><span class="sxs-lookup"><span data-stu-id="c19b4-122">This report is designed to print checks in a stub/check/stub format.</span></span> |
  | <span data-ttu-id="c19b4-123">10413</span><span class="sxs-lookup"><span data-stu-id="c19b4-123">10413</span></span> |<span data-ttu-id="c19b4-124">Þrjár athuganir á hverri síðu</span><span class="sxs-lookup"><span data-stu-id="c19b4-124">Three Checks per Page</span></span> |<span data-ttu-id="c19b4-125">Þessi skýrsla er hönnuð til að prenta þrjá tékka á hverri síðu.</span><span class="sxs-lookup"><span data-stu-id="c19b4-125">This report is designed to print three checks on each page.</span></span> |

<span data-ttu-id="c19b4-126">Þegar settar hafa verið upp útlit tékka er hægt að prenta tékka af síðunni **greiðslubók** .</span><span class="sxs-lookup"><span data-stu-id="c19b4-126">When you have set up check layouts, you can print checks from the **Payment Journal** page.</span></span> <span data-ttu-id="c19b4-127">Nánari upplýsingar eru í [Vinna með tékka](payables-how-work-checks.md).</span><span class="sxs-lookup"><span data-stu-id="c19b4-127">For more information, see [Work with Checks](payables-how-work-checks.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="c19b4-128">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="c19b4-128">See Also</span></span>
[<span data-ttu-id="c19b4-129">Stjórna skuldum</span><span class="sxs-lookup"><span data-stu-id="c19b4-129">Managing Payables</span></span>](payables-manage-payables.md)  
<span data-ttu-id="c19b4-130">[Stjórnun bankareikninga](bank-manage-bank-accounts.md) </span><span class="sxs-lookup"><span data-stu-id="c19b4-130">[Managing Bank Accounts](bank-manage-bank-accounts.md) </span></span>  
[<span data-ttu-id="c19b4-131">Að klára Ferli í lok tímabila</span><span class="sxs-lookup"><span data-stu-id="c19b4-131">Completing Period-End Processes</span></span>](year-how-complete-period-end-processes.md)  
<span data-ttu-id="c19b4-132">[Unnið með [!INCLUDE[prodshort](includes/prodshort.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="c19b4-132">[Working with [!INCLUDE[prodshort](includes/prodshort.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="c19b4-133">Almenn viðskiptavirkni</span><span class="sxs-lookup"><span data-stu-id="c19b4-133">General Business Functionality</span></span>](ui-across-business-areas.md)
