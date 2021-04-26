---
author: edupont04
ms.service: dynamics365-business-central
ms.topic: include
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 7ead218d289668d893a659f730a4c64e31195f10
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5788555"
---
<span data-ttu-id="8ec13-101">Þegar þú slærð inn dagsetningartíma, sem er dagsetning og tími sameinuð í eitt reit, verður þú að slá inn bil milli dagsetningar og tíma.</span><span class="sxs-lookup"><span data-stu-id="8ec13-101">When you enter datetimes, which are a date and time combined into one field, you must enter a space between the date and the time.</span></span> <span data-ttu-id="8ec13-102">Dagsetningarhlutinn getur aðeins innihaldið bil í formi opinbers dagsetningarskiltákns þinna svæðisstillinga.</span><span class="sxs-lookup"><span data-stu-id="8ec13-102">The date part can only contain spaces in the form of the official date separator of your region settings.</span></span> <span data-ttu-id="8ec13-103">Tíminn getur innihaldið bil í kringum f.h./e.h. vísirinn í tengdum svæðisbundnum stillingum.</span><span class="sxs-lookup"><span data-stu-id="8ec13-103">The time can contain spaces around the AM/PM indicator in relevant regional settings.</span></span>

<!--It is also possible to enter only a date in a datetime field, but it is not possible to enter only a time.-->

<span data-ttu-id="8ec13-104">Í eftirfarandi töflu birtast mismunandi leiðir til að færa inn dagsetningar og tímasetningar og hvernig þær eru túlkaðar:</span><span class="sxs-lookup"><span data-stu-id="8ec13-104">The following table lists the various ways in which you can enter datetimes and how they're interpreted.</span></span>  

|<span data-ttu-id="8ec13-105">Færsla</span><span class="sxs-lookup"><span data-stu-id="8ec13-105">Entry</span></span>|<span data-ttu-id="8ec13-106">Túlkun</span><span class="sxs-lookup"><span data-stu-id="8ec13-106">Interpretation</span></span>|
|---------------|------------------------|
|<span data-ttu-id="8ec13-107">08-01-2022 05:48:12 PM</span><span class="sxs-lookup"><span data-stu-id="8ec13-107">08-01-2022 05:48:12 PM</span></span>|<span data-ttu-id="8ec13-108">08\-01\-2022 05:48:12 e.h.</span><span class="sxs-lookup"><span data-stu-id="8ec13-108">08\-01\-2022 05:48:12 PM</span></span>|
|<span data-ttu-id="8ec13-109">131222 132455</span><span class="sxs-lookup"><span data-stu-id="8ec13-109">131222 132455</span></span>|<span data-ttu-id="8ec13-110">13-12-22 13:24:55</span><span class="sxs-lookup"><span data-stu-id="8ec13-110">13-12-22 13:24:55</span></span>|
|<span data-ttu-id="8ec13-111">1-12-22 10</span><span class="sxs-lookup"><span data-stu-id="8ec13-111">1-12-22 10</span></span>|<span data-ttu-id="8ec13-112">01-12-22 10:00:00</span><span class="sxs-lookup"><span data-stu-id="8ec13-112">01-12-22 10:00:00</span></span>|
|<span data-ttu-id="8ec13-113">1.12.22 5</span><span class="sxs-lookup"><span data-stu-id="8ec13-113">1.12.22 5</span></span>|<span data-ttu-id="8ec13-114">01-12-22 05:00:00</span><span class="sxs-lookup"><span data-stu-id="8ec13-114">01-12-22 05:00:00</span></span>|
|<span data-ttu-id="8ec13-115">1.12.22</span><span class="sxs-lookup"><span data-stu-id="8ec13-115">1.12.22</span></span>|<span data-ttu-id="8ec13-116">01-12-22 00:00:00</span><span class="sxs-lookup"><span data-stu-id="8ec13-116">01-12-22 00:00:00</span></span>|
|<span data-ttu-id="8ec13-117">11 12</span><span class="sxs-lookup"><span data-stu-id="8ec13-117">11 12</span></span>|<span data-ttu-id="8ec13-118">11/gildandi mánuður/gildandi ár 12:00:00</span><span class="sxs-lookup"><span data-stu-id="8ec13-118">11-current month-current year 12:00:00</span></span>|
|<span data-ttu-id="8ec13-119">1112 12</span><span class="sxs-lookup"><span data-stu-id="8ec13-119">1112 12</span></span>|<span data-ttu-id="8ec13-120">11/12/gildandi ár 12:00:00</span><span class="sxs-lookup"><span data-stu-id="8ec13-120">11-12-current year 12:00:00</span></span>|
|<span data-ttu-id="8ec13-121">d eða dagurinn í dag</span><span class="sxs-lookup"><span data-stu-id="8ec13-121">t or today</span></span>|<span data-ttu-id="8ec13-122">dagurinn í dag 00:00:00</span><span class="sxs-lookup"><span data-stu-id="8ec13-122">today's date 00:00:00</span></span>|
|<span data-ttu-id="8ec13-123">t tími</span><span class="sxs-lookup"><span data-stu-id="8ec13-123">t time</span></span>|<span data-ttu-id="8ec13-124">gildandi tími dagsins í dag</span><span class="sxs-lookup"><span data-stu-id="8ec13-124">today's date actual time</span></span>|
|<span data-ttu-id="8ec13-125">d 10:30</span><span class="sxs-lookup"><span data-stu-id="8ec13-125">t 10:30</span></span>|<span data-ttu-id="8ec13-126">dagurinn í dag 10:30:00</span><span class="sxs-lookup"><span data-stu-id="8ec13-126">today's date 10:30:00</span></span>|
|<span data-ttu-id="8ec13-127">d 03:03:03</span><span class="sxs-lookup"><span data-stu-id="8ec13-127">t 3:3:3</span></span>|<span data-ttu-id="8ec13-128">dagurinn í dag 03:03:03</span><span class="sxs-lookup"><span data-stu-id="8ec13-128">today's date 03:03:03</span></span>|
|<span data-ttu-id="8ec13-129">v eða vinnudagsetningin</span><span class="sxs-lookup"><span data-stu-id="8ec13-129">w or workdate</span></span>|<span data-ttu-id="8ec13-130">vinnudagsetningin 00:00:00</span><span class="sxs-lookup"><span data-stu-id="8ec13-130">the working date 00:00:00</span></span>|
|<span data-ttu-id="8ec13-131">m eða mánudagur</span><span class="sxs-lookup"><span data-stu-id="8ec13-131">m or Monday</span></span>|<span data-ttu-id="8ec13-132">Mánudagur yfirstandandi viku 00:00:00</span><span class="sxs-lookup"><span data-stu-id="8ec13-132">Monday of the current week 00:00:00</span></span>|
|<span data-ttu-id="8ec13-133">þr eða þriðjudagur</span><span class="sxs-lookup"><span data-stu-id="8ec13-133">tu or Tuesday</span></span>|<span data-ttu-id="8ec13-134">Þriðjudagur yfirstandandi viku 00:00:00</span><span class="sxs-lookup"><span data-stu-id="8ec13-134">Tuesday of the current week 00:00:00</span></span>|
|<span data-ttu-id="8ec13-135">mi eða miðvikudagur</span><span class="sxs-lookup"><span data-stu-id="8ec13-135">we or Wednesday</span></span>|<span data-ttu-id="8ec13-136">Miðvikudagur yfirstandandi viku 00:00:00</span><span class="sxs-lookup"><span data-stu-id="8ec13-136">Wednesday of the current week 00:00:00</span></span>|
|<span data-ttu-id="8ec13-137">fi eða fimmtudagur</span><span class="sxs-lookup"><span data-stu-id="8ec13-137">th or Thursday</span></span>|<span data-ttu-id="8ec13-138">Fimmtudagur yfirstandandi viku 00:00:00</span><span class="sxs-lookup"><span data-stu-id="8ec13-138">Thursday of the current week 00:00:00</span></span>|
|<span data-ttu-id="8ec13-139">f eða föstudagur</span><span class="sxs-lookup"><span data-stu-id="8ec13-139">f or Friday</span></span>|<span data-ttu-id="8ec13-140">Föstudagur yfirstandandi viku 00:00:00</span><span class="sxs-lookup"><span data-stu-id="8ec13-140">Friday of the current week 00:00:00</span></span>|
|<span data-ttu-id="8ec13-141">l eða laugardagur</span><span class="sxs-lookup"><span data-stu-id="8ec13-141">s or Saturday</span></span>|<span data-ttu-id="8ec13-142">Laugardagur yfirstandandi viku 00:00:00</span><span class="sxs-lookup"><span data-stu-id="8ec13-142">Saturday of the current week 00:00:00</span></span>|
|<span data-ttu-id="8ec13-143">s eða sunnudagur</span><span class="sxs-lookup"><span data-stu-id="8ec13-143">su or Sunday</span></span>|<span data-ttu-id="8ec13-144">Sunnudagur yfirstandandi viku 00:00:00</span><span class="sxs-lookup"><span data-stu-id="8ec13-144">Sunday of the current week 00:00:00</span></span>|
|<span data-ttu-id="8ec13-145">þr 10:30:00</span><span class="sxs-lookup"><span data-stu-id="8ec13-145">tu 10:30</span></span>|<span data-ttu-id="8ec13-146">Þriðjudagur yfirstandandi viku 10:30:00</span><span class="sxs-lookup"><span data-stu-id="8ec13-146">Tuesday of the current week 10:30:00</span></span>|
|<span data-ttu-id="8ec13-147">þr 03:03:03</span><span class="sxs-lookup"><span data-stu-id="8ec13-147">tu 3:3:3</span></span>|<span data-ttu-id="8ec13-148">Þriðjudagur yfirstandandi viku 03:03:03</span><span class="sxs-lookup"><span data-stu-id="8ec13-148">Tuesday of the current week 03:03:03</span></span>|
|<span data-ttu-id="8ec13-149">Þ23 Þ</span><span class="sxs-lookup"><span data-stu-id="8ec13-149">t23 t</span></span>|<span data-ttu-id="8ec13-150">Þriðjudagur 23. viku vinnudagsetningarársins, núgildandi tími dagsins</span><span class="sxs-lookup"><span data-stu-id="8ec13-150">Tuesday of week 23 of the work date year, current time of day</span></span>|
|<span data-ttu-id="8ec13-151">þ23</span><span class="sxs-lookup"><span data-stu-id="8ec13-151">t23</span></span>|<span data-ttu-id="8ec13-152">Þriðjudagur 23. viku vinnudagsetningarársins</span><span class="sxs-lookup"><span data-stu-id="8ec13-152">Tuesday of week 23 of the work date year</span></span>|
|<span data-ttu-id="8ec13-153">þ 23</span><span class="sxs-lookup"><span data-stu-id="8ec13-153">t 23</span></span>|<span data-ttu-id="8ec13-154">Í dag 23:00:00</span><span class="sxs-lookup"><span data-stu-id="8ec13-154">Today 23:00:00</span></span>|
|<span data-ttu-id="8ec13-155">þ-1</span><span class="sxs-lookup"><span data-stu-id="8ec13-155">t-1</span></span>|<span data-ttu-id="8ec13-156">Þriðjudagur 1. viku vinnudagsetningarársins</span><span class="sxs-lookup"><span data-stu-id="8ec13-156">Tuesday of week 1 of the work date year</span></span>|


