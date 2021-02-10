---
title: Innsýn og flutningsþjónusta í skýi | Microsoft docs
description: Tengstu með innsýn með Business Central úr innanhússlausnum. Kynntu þér hvernig á flytja í skýið.
author: bmeier94
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.reviewer: edupont
ms. search.keywords: cloud, edge
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: a186166e73d4c6dcda01bbda6ac2c88a18b2babb
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/17/2020
ms.locfileid: "4753718"
---
# <a name="intelligent-insights-with-prod_short-online"></a><span data-ttu-id="0567e-104">Innsýn með [!INCLUDE[prod_short](includes/prod_short.md)] Online</span><span class="sxs-lookup"><span data-stu-id="0567e-104">Intelligent Insights with [!INCLUDE[prod_short](includes/prod_short.md)] Online</span></span>

<span data-ttu-id="0567e-105">Sem notandi [!INCLUDE[prod_short](includes/prod_short.md)] á netinu hefur þú fullan aðgang að atburðarásum á snjallskýi, svo sem að breyta KPI sem byggja á vélnámi, eða þegar þú skoðar gögnin þín í Power BI.</span><span class="sxs-lookup"><span data-stu-id="0567e-105">As a user of [!INCLUDE[prod_short](includes/prod_short.md)] online, you have full access to scenarios that are based on the intelligent cloud, such as KPIs that are based on machine learning, or when you view your data in Power BI.</span></span> <span data-ttu-id="0567e-106">Hins vegar, meðan [!INCLUDE[prod_short](includes/prod_short.md)] er fyrst þjónusta við ský, þá geta þeir viðskiptamenn sem þurfa að keyra vinnuálag sitt að öllu leyti á staðnum eða á eigin snjallkerfi sem tengist skýinu, gert það.</span><span class="sxs-lookup"><span data-stu-id="0567e-106">However, while [!INCLUDE[prod_short](includes/prod_short.md)] is a cloud-first service, also those customers who need to run their workloads fully on-premises or on the intelligent edge connected to the cloud can do so.</span></span>  

<span data-ttu-id="0567e-107">Ef þú hefur áhuga á [!INCLUDE[prod_short](includes/prod_short.md)] getur þú skráð þig fyrir ókeypis prufu á netinu, eða þú getur valið að vinna með samstarfsaðila til að setja upp [!INCLUDE[prod_short](includes/prod_short.md)] á staðnum eftir eigin vali á vélbúnaði.</span><span class="sxs-lookup"><span data-stu-id="0567e-107">If you are interested in [!INCLUDE[prod_short](includes/prod_short.md)], you can sign up for a free trial online, or you can choose to work with a partner to deploy [!INCLUDE[prod_short](includes/prod_short.md)] locally to your own choice of hardware.</span></span> <span data-ttu-id="0567e-108">Þú getur þá ákveðið að fá snjalla innsýn með því að tengjast leigjanda í skýinu.</span><span class="sxs-lookup"><span data-stu-id="0567e-108">You can then decide to get intelligent insights by connecting to a tenant in the cloud.</span></span> <span data-ttu-id="0567e-109">Gögnin frá uppsetningu [!INCLUDE[prod_short](includes/prod_short.md)] á staðnum afritast þar af leiðandi í skýið fyrir aðstæður sem tengjast snjallskýi.</span><span class="sxs-lookup"><span data-stu-id="0567e-109">As a result, the data from your [!INCLUDE[prod_short](includes/prod_short.md)] on-premises deployment replicates to the cloud for intelligent cloud scenarios.</span></span>  

<span data-ttu-id="0567e-110">Tenging við snjallský úr lausnum á staðnum krefst að stjórnandi þinn tilgreini upplýsingar um gagnagrunninn.</span><span class="sxs-lookup"><span data-stu-id="0567e-110">Connecting to the intelligent cloud from an on-premises solution requires your administrator to specify information about your database.</span></span> <span data-ttu-id="0567e-111">Verkfærin sem notuð eru til að tengja uppsetningu innanhúss við [!INCLUDE[prod_short](includes/prod_short.md)] online eru þau sömu sem eru einnig notuð til flutnings frá staðnum á netið.</span><span class="sxs-lookup"><span data-stu-id="0567e-111">The tools used to connect your on-premises deployment to [!INCLUDE[prod_short](includes/prod_short.md)] online are the same that are also used to migration from on-premises to online.</span></span> <span data-ttu-id="0567e-112">Frekari upplýsingar er að finna í [Flytja inn innanhússgögn í Business Central Online](/dynamics365/business-central/dev-itpro/administration/migrate-data) í efnisstjórnunarefninu fyrir [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="0567e-112">For more information, see [Migrating On-Premises Data to Business Central Online](/dynamics365/business-central/dev-itpro/administration/migrate-data) in the administration content for [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>  

## <a name="viewing-intelligent-cloud-insights-in-prod_short-online"></a><span data-ttu-id="0567e-113">Skoða snjallskýjainnsýn í [!INCLUDE[prod_short](includes/prod_short.md)] á netinu</span><span class="sxs-lookup"><span data-stu-id="0567e-113">Viewing Intelligent Cloud Insights in [!INCLUDE[prod_short](includes/prod_short.md)] Online</span></span>

<span data-ttu-id="0567e-114">Í [!INCLUDE[prod_short](includes/prod_short.md)] fyrirtækinu þínu á netinu sýnir **snjallskýjainnsýn** síðan fjögur helstu atriði sem vekja athygli fyrir flest fyrirtæki:</span><span class="sxs-lookup"><span data-stu-id="0567e-114">In your [!INCLUDE[prod_short](includes/prod_short.md)] online company, the **Intelligent Cloud Insights** page shows four key points of interest for most businesses:</span></span>

- <span data-ttu-id="0567e-115">Framboð reiðufé</span><span class="sxs-lookup"><span data-stu-id="0567e-115">Cash availability</span></span>
- <span data-ttu-id="0567e-116">Sala arðsemi</span><span class="sxs-lookup"><span data-stu-id="0567e-116">Sales profitability</span></span>
- <span data-ttu-id="0567e-117">Nettótekjur</span><span class="sxs-lookup"><span data-stu-id="0567e-117">Net income</span></span>
- <span data-ttu-id="0567e-118">Birgðavirði</span><span class="sxs-lookup"><span data-stu-id="0567e-118">Inventory value</span></span>

<span data-ttu-id="0567e-119">Við hliðina á KPI-töflunum færðu innsýn í hugsanlega áhyggjuefni, þ.m.t. gjaldfallnar greiðslur.</span><span class="sxs-lookup"><span data-stu-id="0567e-119">Next to the KPI charts, you get insights into potential areas of concern, including overdue payments.</span></span> <span data-ttu-id="0567e-120">Veldu hvert innsýn til að kafa inn í gögnin.</span><span class="sxs-lookup"><span data-stu-id="0567e-120">Choose each insight to drill into the data.</span></span>  

> [!div class="mx-imgBorder"]
> <span data-ttu-id="0567e-121">![Intelligent Cloud-innsýn](media/across-intelligent-cloud/intelligentcloudApril19.png "Sýnir snjallskýsinnsýn síðu í Business Central")</span><span class="sxs-lookup"><span data-stu-id="0567e-121">![Intelligent cloud insights](media/across-intelligent-cloud/intelligentcloudApril19.png "Shows the Intelligent Cloud Insights page in Business Central")</span></span>

<span data-ttu-id="0567e-122">Síðan tengist einnig Power BI fyrir enn meiri innsýn.</span><span class="sxs-lookup"><span data-stu-id="0567e-122">The page also connects to Power BI for even more insights.</span></span>

## <a name="viewing-intelligent-insights-on-premises"></a><span data-ttu-id="0567e-123">Skoða snjallskýsinnsýn á staðnum</span><span class="sxs-lookup"><span data-stu-id="0567e-123">Viewing Intelligent Insights On-Premises</span></span>

<span data-ttu-id="0567e-124">Þegar Dynamics 365 endursöluaðili þinn hefur öðlast rétt leyfi fyrir lausn þína á staðnum til að tengjast skýinu í gegnum [!INCLUDE[prod_short](includes/prod_short.md)] getur stjórnandi þinn sett upp tenginguna.</span><span class="sxs-lookup"><span data-stu-id="0567e-124">When your Dynamics 365 reselling partner has acquired the right license for your on-premises solution to connect to the cloud through [!INCLUDE[prod_short](includes/prod_short.md)], your administrator can set up the connection.</span></span> <span data-ttu-id="0567e-125">Þegar það er gert geturðu skoðað sömu upplýsingar frá skýinu í forritinu þínu á staðnum.</span><span class="sxs-lookup"><span data-stu-id="0567e-125">Once that is done, you can view the same insights from the cloud in your on-premises application.</span></span> <span data-ttu-id="0567e-126">Í samræmi við lausn á staðnum getur **Snjallskýjannsýn** síðan verið felld inn í heimasíðuna eða verið á sérstakri síðu eins og í [!INCLUDE[prod_short](includes/prod_short.md)] á netinu og innanhúss.</span><span class="sxs-lookup"><span data-stu-id="0567e-126">Depending on the on-premises solution, the **Intelligent Cloud Insights** page can be embedded in the Home page or be a separate page as in [!INCLUDE[prod_short](includes/prod_short.md)] online and on-premises.</span></span>  

## <a name="see-also"></a><span data-ttu-id="0567e-127">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="0567e-127">See Also</span></span>

[<span data-ttu-id="0567e-128">Velkomin(n) í Business Central</span><span class="sxs-lookup"><span data-stu-id="0567e-128">Welcome to Business Central</span></span>](index.md)  
[<span data-ttu-id="0567e-129">Snjallskýsviðbætur fyrir flutningi í skýi</span><span class="sxs-lookup"><span data-stu-id="0567e-129">Intelligent Cloud Extensions for Cloud Migration</span></span>](ui-extensions-data-replication.md)  
[<span data-ttu-id="0567e-130">Flytja inn innanhússgögn í Business Central Online</span><span class="sxs-lookup"><span data-stu-id="0567e-130">Migrating On-Premises Data to Business Central Online</span></span>](/dynamics365/business-central/dev-itpro/administration/migrate-data)  
