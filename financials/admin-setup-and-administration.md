---
title: "Verkhlutar framkvæmdir af stjórnendum í Dynamics 365 | Microsoft Docs"
description: "Sumir verkhlutar í [!INCLUDE[d365fin](includes/d365fin_md.md)] krefjast miðlægrar stjórnunar og uppsetningar. Sjáðu hverjir þeir eru og lærðu hvað skal gera."
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/01/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 09c3460a50088098bfe5c2fb633e76dccbac0794
ms.contentlocale: is-is
ms.lasthandoff: 09/22/2017

---
# <a name="setup-and-administration-in-dynamics-365-for-financials"></a><span data-ttu-id="55000-104">Uppsetning og stjórnun í Dynamics 365 for Financials</span><span class="sxs-lookup"><span data-stu-id="55000-104">Setup and Administration in Dynamics 365 for Financials</span></span>
<span data-ttu-id="55000-105">Almenn stjórnunarverk eru yfirleitt framkvæmd af einu hlutverki innan fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="55000-105">Central administration tasks are usually performed by one role in the company.</span></span> <span data-ttu-id="55000-106">Umfang þessara verka getur byggst á stærð fyrirtækisins og starfsábyrgð stjórnandans.</span><span class="sxs-lookup"><span data-stu-id="55000-106">The scope of these tasks can depend on the company's size and the administrator's job responsibilities.</span></span> <span data-ttu-id="55000-107">Til þessara verka geta talist umsjón með gagnagrunnssamstillingu verkraða og póstraða, uppsetning notenda, sérstilling viðmóts og stjórnun dulritunarlykla.</span><span class="sxs-lookup"><span data-stu-id="55000-107">These tasks can include managing database synchronization of job and email queues, setting up users, customizing the user interface, and managing encryption keys.</span></span>  

<span data-ttu-id="55000-108">Mikilvægt er að færa inn rétt uppsetningargildi frá upphafi til að ný viðskiptaforrit nái árangri.</span><span class="sxs-lookup"><span data-stu-id="55000-108">Entering the correct setup values from the start is important to the success of any new business software.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="55000-109"> inniheldur nokkrar uppsetningarleiðbeiningar sem aðstoða þig við að setja upp grunngögn.</span><span class="sxs-lookup"><span data-stu-id="55000-109"> includes a number of setup guides that help you set up core data.</span></span> <span data-ttu-id="55000-110">Nánari upplýsingar er að finna í [Uppsetning Dynamics 365 for Financials](setup.md).</span><span class="sxs-lookup"><span data-stu-id="55000-110">For more information, see [Setting Up Dynamics 365 for Financials](setup.md).</span></span>

<!--Whether you use [!INCLUDE[rim](../../includes/rim_md.md)] to implement setup values or you manually enter them in the new company, you can support your setup decisions with some general recommendations for selected setup fields that are known to potentially cause the solution to be inefficient if defined incorrectly.-->  

<span data-ttu-id="55000-111">Yfirnotandi eða stjórnandi getur sett upp Data Exchange Framework til að gera notendum kleift að flytja út og flytja inn gögn í banka og launaskrár, t.d. fyrir ýmsa stjórnun reiðufés.</span><span class="sxs-lookup"><span data-stu-id="55000-111">A super user or an administrator can set up the Data Exchange Framework to enable users to export and import data in bank and payroll files, for example for various cash management processes.</span></span>  

<span data-ttu-id="55000-112">Eftirfarandi tafla lýsir röð verkefna með tenglum í efnisatriði þar sem þeim er lýst.</span><span class="sxs-lookup"><span data-stu-id="55000-112">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>   

|<span data-ttu-id="55000-113">**Til að**</span><span class="sxs-lookup"><span data-stu-id="55000-113">**To**</span></span>|<span data-ttu-id="55000-114">**Sjá**</span><span class="sxs-lookup"><span data-stu-id="55000-114">**See**</span></span>|  
|------------|-------------|  
|<span data-ttu-id="55000-115">Bæta við notendum, meðhöndla heimildir og aðgang að gögnum, úthluta hlutverkum.</span><span class="sxs-lookup"><span data-stu-id="55000-115">Add users, manage permissions and access to data, assign roles.</span></span>|[<span data-ttu-id="55000-116">Notendur, forstillingar og hlutverkamiðstöðvar Dynamics 365 for Financials</span><span class="sxs-lookup"><span data-stu-id="55000-116">Users, Profiles, and Role Centers in Dynamics 365 for Financials</span></span>](admin-users-profiles-roles.md)|  
|<span data-ttu-id="55000-117">Rekja allar beinar breytingar sem notendur gera á gögnum í gagnagrunninum til að finna uppruna villna og gagnabreytinga.</span><span class="sxs-lookup"><span data-stu-id="55000-117">Track all direct modifications that users make to data in the database to identify the origin of errors and data changes.</span></span>|[<span data-ttu-id="55000-118">Skráning breytinga í Dynamics 365 for Financials</span><span class="sxs-lookup"><span data-stu-id="55000-118">Logging Changes in Dynamics 365 for Financials</span></span>](across-log-changes.md)|  
|<span data-ttu-id="55000-119">Styðjið uppsetningargildi með tillögum fyrir valda reiti sem vitað er að geta mögulega orðið til óskilvirkni lausnarinnar, ef þeir eru ekki settir rétt upp</span><span class="sxs-lookup"><span data-stu-id="55000-119">Support your setup decisions with recommendations for selected fields that are known to potentially cause the solution to be inefficient if set up incorrectly</span></span>|[<span data-ttu-id="55000-120">Setja upp flókin notkunarsviðum með því að nota bestu venjur</span><span class="sxs-lookup"><span data-stu-id="55000-120">Set Up Complex Application Areas Using Best Practices</span></span>](set-up-complex-application-areas-using-best-practices.md)|  
|<span data-ttu-id="55000-121">Birta síður, kóðaeiningar og beiðnir sem vefþjónustu.</span><span class="sxs-lookup"><span data-stu-id="55000-121">Expose pages, codeunits, and queries as web services.</span></span>|[<span data-ttu-id="55000-122">Hvernig á að: Birta vefþjónustu</span><span class="sxs-lookup"><span data-stu-id="55000-122">How to: Publish a Web Service</span></span>](across-how-publish-web-service.md)|  
|<span data-ttu-id="55000-123">Uppsetning SMTP-netþjóns til að virkja tölvupóstssamskipti inn og út úr Dynamics 365 for Financials.</span><span class="sxs-lookup"><span data-stu-id="55000-123">Set up an SMTP server to enable e-mail communication in and out of Dynamics 365 for Financials</span></span>| [<span data-ttu-id="55000-124">Hvernig á að: Setja upp tölvupóst handvirkt eða með því að nota Uppsetningu með aðstoð</span><span class="sxs-lookup"><span data-stu-id="55000-124">How to: Set Up Email Manually or Using the Assisted Setup</span></span>](madeira-how-setup-email.md)|  
|<span data-ttu-id="55000-125">Færa inn stakar eða endurteknar beiðnir um keyrslu skýrslna eða kótaeininga.</span><span class="sxs-lookup"><span data-stu-id="55000-125">Enter single or recurring requests to run reports or codeunits.</span></span>|[<span data-ttu-id="55000-126">Nota verkraðir til að tímaraða verkhlutum</span><span class="sxs-lookup"><span data-stu-id="55000-126">Use Job Queues to Schedule Tasks</span></span>](admin-job-queues-schedule-tasks.md)|  
|<span data-ttu-id="55000-127">Meðhöndla, eyða eða þjappa skjöl</span><span class="sxs-lookup"><span data-stu-id="55000-127">Manage, delete, or compress documents</span></span>|[<span data-ttu-id="55000-128">Umsjón með skjölum</span><span class="sxs-lookup"><span data-stu-id="55000-128">Manage Documents</span></span>](admin-manage-documents.md)|  
|<span data-ttu-id="55000-129">Nýtt fyrirtækiseining sem notar sniðmát er sett upp.</span><span class="sxs-lookup"><span data-stu-id="55000-129">Set up a new business unit using templates</span></span>|<span data-ttu-id="55000-130">[Stofna ný fyrirtæki í [!INCLUDE[d365fin](includes/d365fin_md.md)]](about-new-company.md)</span><span class="sxs-lookup"><span data-stu-id="55000-130">[Creating New Companies in [!INCLUDE[d365fin](includes/d365fin_md.md)]](about-new-company.md)</span></span>|  

## <a name="see-also"></a><span data-ttu-id="55000-131">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="55000-131">See Also</span></span>
[<span data-ttu-id="55000-132">Yfirlit yfir Viðskiptavirkni</span><span class="sxs-lookup"><span data-stu-id="55000-132">Overview of Business Functionality</span></span>](madeira-business-functionality.md)  
[<span data-ttu-id="55000-133">Almenn viðskiptavirkni</span><span class="sxs-lookup"><span data-stu-id="55000-133">General Business Functionality</span></span>](ui-across-business-areas.md)  
<span data-ttu-id="55000-134">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="55000-134">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
<span data-ttu-id="55000-135">[Velkomin(n) í [!INCLUDE[d365fin](includes/d365fin_md.md)]](index.md)</span><span class="sxs-lookup"><span data-stu-id="55000-135">[Welcome to [!INCLUDE[d365fin](includes/d365fin_md.md)]](index.md)</span></span>  

