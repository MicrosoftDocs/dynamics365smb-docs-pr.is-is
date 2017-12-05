---
title: "Setja upp dagsetningabil í Dynamics 365 Business edition | Microsoft Docs"
description: "Kynntu þér hvernig skal sækja skýrslu sem sýnir gögn frá ákveðnu tímabili með því að nota dagsetningartímabil í Dynamics 365 Business edition."
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: dates, reporting, filter
ms.date: 05/29/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: ba26b354d235981bd7291f9ac6402779f554ac7a
ms.openlocfilehash: fee6a5d7ce6603829ed98913b7e370a53239ee3e
ms.contentlocale: is-is
ms.lasthandoff: 11/10/2017

---
# <a name="entering-date-ranges-in-dynamics-365-business-edition"></a><span data-ttu-id="35cf3-103">Færa inn dagsetningartímabil í Dynamics 365 Business edition</span><span class="sxs-lookup"><span data-stu-id="35cf3-103">Entering Date Ranges in Dynamics 365 Business edition</span></span> 
<span data-ttu-id="35cf3-104">Hægt er að stilla afmarkanir með upphafs- og lokadegi til að birta aðeins gögn á tilteknu tímabili.</span><span class="sxs-lookup"><span data-stu-id="35cf3-104">You can set filters containing a start date and an end date to display only the data contained in that date range or time interval.</span></span> <span data-ttu-id="35cf3-105">Ákveðnar reglur gilda um hvernig tímabil eru stillt.</span><span class="sxs-lookup"><span data-stu-id="35cf3-105">Special rules apply to the way you set date ranges.</span></span> <span data-ttu-id="35cf3-106">Tökum sem dæmi **Topp 10 viðskiptavinir**:</span><span class="sxs-lookup"><span data-stu-id="35cf3-106">Let's take the **Customer Top 10** as an example:</span></span>

![Stilla dagsetningartímabil á beiðnisíðunni fyrir topp 10 viðskiptavinir](./media/ui-enter-date-ranges/customer-top10-list.png)

<span data-ttu-id="35cf3-108">Hér geturðu afmarkað skýrsluna við dagsetningartímabil eins og síðustu 2 vikur eða alls 6 vikur, eða hvaða tímabil sem þú vilt.</span><span class="sxs-lookup"><span data-stu-id="35cf3-108">Here you can limit the report to a date range such as the past 2 weeks, or a total of 6 weeks, or whatever range you want.</span></span> <span data-ttu-id="35cf3-109">Til að stilla dagsetningartímabil slærðu inn dagsetningar og notar svo annað hvort **..**</span><span class="sxs-lookup"><span data-stu-id="35cf3-109">To set date ranges, you enter dates and then use either **..**</span></span> <span data-ttu-id="35cf3-110">eða **|** til að stilla tímabilið.</span><span class="sxs-lookup"><span data-stu-id="35cf3-110">or **|** to set the range.</span></span> <span data-ttu-id="35cf3-111">Til að skoða topp 10 viðskiptavinina fyrstu 2 vikurnar í maí, til dæmis, myndirðu setja dagsetingarafmörkunina á *05 01 17..05 14 17*.</span><span class="sxs-lookup"><span data-stu-id="35cf3-111">In our example, to show the top 10 customers for the first two weeks of May, you would set the date filter to *05 01 17..05 14 17*.</span></span>
<span data-ttu-id="35cf3-112">Hér eru nokkur fleiri dæmi:</span><span class="sxs-lookup"><span data-stu-id="35cf3-112">Here are a couple of other examples:</span></span>

| <span data-ttu-id="35cf3-113">Merking</span><span class="sxs-lookup"><span data-stu-id="35cf3-113">Meaning</span></span> | <span data-ttu-id="35cf3-114">Dæmi</span><span class="sxs-lookup"><span data-stu-id="35cf3-114">Example</span></span> | <span data-ttu-id="35cf3-115">Ásamt færslum</span><span class="sxs-lookup"><span data-stu-id="35cf3-115">Entries included</span></span> |
|---|---|---|
|<span data-ttu-id="35cf3-116">Jafnt og</span><span class="sxs-lookup"><span data-stu-id="35cf3-116">Equal to</span></span>| <span data-ttu-id="35cf3-117">12, 15, 16</span><span class="sxs-lookup"><span data-stu-id="35cf3-117">12 15 16</span></span> |<span data-ttu-id="35cf3-118">Einungis þær sem bókaðar eru 15. desember 2016.</span><span class="sxs-lookup"><span data-stu-id="35cf3-118">Only those posted on December 15 2016.</span></span>|
|<span data-ttu-id="35cf3-119">Millibil</span><span class="sxs-lookup"><span data-stu-id="35cf3-119">Interval</span></span>| <span data-ttu-id="35cf3-120">12 15 16..01 15 17</span><span class="sxs-lookup"><span data-stu-id="35cf3-120">12 15 16..01 15 17</span></span><br /><br /><span data-ttu-id="35cf3-121">..12 15 16</span><span class="sxs-lookup"><span data-stu-id="35cf3-121">..12 15 16</span></span>|<span data-ttu-id="35cf3-122">Færslur sem eru bókaðar á dagsetningum á milli og með 15. desember 2016 og 15. janúar 2017.</span><span class="sxs-lookup"><span data-stu-id="35cf3-122">Those posted on dates between and including December 15 2016 and January 15 2017.</span></span><br /><br /><span data-ttu-id="35cf3-123">Þær sem eru bókaðar eru 15. desember 2016 og fyrr.</span><span class="sxs-lookup"><span data-stu-id="35cf3-123">Those posted on December 15 2016 or earlier.</span></span>|
|<span data-ttu-id="35cf3-124">Annaðhvort eða</span><span class="sxs-lookup"><span data-stu-id="35cf3-124">Either/or</span></span>|<span data-ttu-id="35cf3-125">12 15 16&#124;12 16 16</span><span class="sxs-lookup"><span data-stu-id="35cf3-125">12 15 16&#124;12 16 16</span></span>|<span data-ttu-id="35cf3-126">Þær sem eru bókaðar annað hvort 15. eða 16. desember 2016.</span><span class="sxs-lookup"><span data-stu-id="35cf3-126">Those posted on either December 15 or December 16 2016.</span></span> <span data-ttu-id="35cf3-127">Ef færslur eru bókaðar báða dagana verða þær allar sýndar.</span><span class="sxs-lookup"><span data-stu-id="35cf3-127">If there are entries posted on both days, they will all be displayed.</span></span>|

<span data-ttu-id="35cf3-128">Einnig má tengja grunnformin saman.</span><span class="sxs-lookup"><span data-stu-id="35cf3-128">You can also combine the various format types.</span></span>

| <span data-ttu-id="35cf3-129">Dæmi</span><span class="sxs-lookup"><span data-stu-id="35cf3-129">Example</span></span> | <span data-ttu-id="35cf3-130">Ásamt færslum</span><span class="sxs-lookup"><span data-stu-id="35cf3-130">Entries included</span></span> |
|---|---|
|<span data-ttu-id="35cf3-131">12 15 16&#124;12 01 16..05 31 17</span><span class="sxs-lookup"><span data-stu-id="35cf3-131">12 15 16&#124;12 01 16..05 31 17</span></span> | <span data-ttu-id="35cf3-132">Færslur sem eru bókaðar annað hvort 15. desember 2016 eða á dagsetningum á milli og með 01. desember 2016 og 31. maí 2017.</span><span class="sxs-lookup"><span data-stu-id="35cf3-132">Entries posted either on December 15 2016 or on dates between and including December 01 2016 and May 31 2017.</span></span> |
|<span data-ttu-id="35cf3-133">12 14 16&#124;12 30 16</span><span class="sxs-lookup"><span data-stu-id="35cf3-133">..12 14 16&#124;12 30 16..</span></span> | <span data-ttu-id="35cf3-134">Færslur bókaðar til og með 14. desember og færslur bókaðar frá og með 30. desember - það er, allar færslur nema þær sem voru bókaðar á dagsetningum á milli og með 15. og 29. desember.</span><span class="sxs-lookup"><span data-stu-id="35cf3-134">Entries posted on December 14 or earlier, or entries posted on December 30 or later - that is, all entries except those posted on dates between and including December 15 and 29.</span></span> |

<span data-ttu-id="35cf3-135">Athugið að við notuðum bandarískt dagsetningarsnið hér.</span><span class="sxs-lookup"><span data-stu-id="35cf3-135">Note that we have used the US date format MMDDYY here.</span></span> <span data-ttu-id="35cf3-136">Þegar [!INCLUDE[d365fin](includes/d365fin_md.md)] verður tiltækt á öðrum mörkuðum, muntu geta notað þau snið sem þú ert vanur.</span><span class="sxs-lookup"><span data-stu-id="35cf3-136">As [!INCLUDE[d365fin](includes/d365fin_md.md)] becomes available in other markets, you'll be able to use the formats that you are used to.</span></span>

## <a name="see-also"></a><span data-ttu-id="35cf3-137">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="35cf3-137">See Also</span></span>
<span data-ttu-id="35cf3-138">[Unnið með [!INCLUDE[d365fin](includes/d365fin_long_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="35cf3-138">[Working with [!INCLUDE[d365fin](includes/d365fin_long_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="35cf3-139">Skilgreining skilyrða í síum</span><span class="sxs-lookup"><span data-stu-id="35cf3-139">Entering Criteria in Filters </span></span>](ui-enter-criteria-filters.md)  
[<span data-ttu-id="35cf3-140">Almenn viðskiptavirkni</span><span class="sxs-lookup"><span data-stu-id="35cf3-140">General Business Functionality</span></span>](ui-across-business-areas.md)

