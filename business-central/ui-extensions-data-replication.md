---
title: Business Central-snjallskýsviðbætur fyrir flutning í ský | Microsoft Docs
description: Nota skal flutningsviðbætur í ský til að flytja gögn innanhúss í Business Central á netinu. Þessar viðbætur færa innanhússgögn í skýið svo hægt sé að nota Business Central á netinu með fyrirliggjandi gögnum.
author: jenolson
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, import, implement
ms.reviewer: edupont
ms.date: 10/01/2020
ms.author: jenolson
ms.openlocfilehash: dde6797139f383948d72c52ca1d05298a280087b
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/01/2020
ms.locfileid: "3915211"
---
# <a name="intelligent-cloud-extensions-for-cloud-migration"></a><span data-ttu-id="ffc04-104">Snjallskýsviðbætur fyrir flutningi í skýi</span><span class="sxs-lookup"><span data-stu-id="ffc04-104">Intelligent Cloud Extensions for Cloud Migration</span></span>

<span data-ttu-id="ffc04-105">Það fer eftir staðbundinni lausn, en nota þarf aðrar viðbætur til að tengja gögnin við [!INCLUDE[prodshort](includes/prodshort.md)] á netinu í þeim tilgangi að flytja lausnina yfir í skýið.</span><span class="sxs-lookup"><span data-stu-id="ffc04-105">Depending on your on-premises solution, you must use different extensions to connect your data with [!INCLUDE[prodshort](includes/prodshort.md)] online for purposes of migrating your solution to the cloud.</span></span>  

<span data-ttu-id="ffc04-106">Ef þú ert að nota eina af studdu vörum á staðnum geturðu stillt skýjaumhverfið sem byggist á vörumiðaðri viðbót.</span><span class="sxs-lookup"><span data-stu-id="ffc04-106">If you are using one of the supported on-premises products, you can configure your cloud environment based on a product-specific extension.</span></span><span data-ttu-id="ffc04-107"> Þegar skýjaumhverfið þitt hefur verið grunnstillt geturðu flutt gögn úr þínum lausnum innanhúss í [!INCLUDE[prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="ffc04-107"> Once your cloud environment is configured, you will be able to migrate data from your on-premises solution to [!INCLUDE[prodshort](includes/prodshort.md)].</span></span> <span data-ttu-id="ffc04-108">Þetta gerir þér kleift að nýta hvað skýið býður upp á fyrir fyrirtækið þitt, svo sem aukið innsýn í fyrirtæki þitt, gervigreind, aðgang að mörgum tækjum og aðgang hvenær sem er, hvar sem er.</span><span class="sxs-lookup"><span data-stu-id="ffc04-108">This will enable you to take full advantage of what the cloud has to offer your business such as, enhanced insights into your business, artificial intelligence, multiple device access, and anytime, anywhere access.</span></span>  

<span data-ttu-id="ffc04-109">Frekari upplýsingar er að finna í [Flytja inn innanhússgögn í Business Central Online](/dynamics365/business-central/dev-itpro/administration/migrate-data) í efnisstjórnunarefninu fyrir [!INCLUDE[prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="ffc04-109">For more information, see [Migrating On-Premises Data to Business Central Online](/dynamics365/business-central/dev-itpro/administration/migrate-data) in the administration content for [!INCLUDE[prodshort](includes/prodshort.md)].</span></span>  

## <a name="business-central-on-premises"></a><span data-ttu-id="ffc04-110">Business Central á staðnum</span><span class="sxs-lookup"><span data-stu-id="ffc04-110">Business Central on-premises</span></span>

<span data-ttu-id="ffc04-111">Ef þú ert að nota uppsetningu á staðnum af [!INCLUDE[prodshort](includes/prodshort.md)], náðu þá í viðbæturnar **Snjallskýsgrunnur** og **Business Central-snjallský** og keyrðu **Uppsetningu skýjaflutnings** leiðbeiningar um uppsetningu með hjálp .</span><span class="sxs-lookup"><span data-stu-id="ffc04-111">If you are using an on-premises deployment of [!INCLUDE[prodshort](includes/prodshort.md)], get the **Intelligent Cloud Base** extension and the **Business Central Intelligent Cloud** extension, and then run the **Cloud Migration Setup** assisted setup guide.</span></span>  

## <a name="dynamics-gp"></a><span data-ttu-id="ffc04-112">Dynamics GP</span><span class="sxs-lookup"><span data-stu-id="ffc04-112">Dynamics GP</span></span>

<span data-ttu-id="ffc04-113">Ef þú ert að nota Dynamics GP skaltu ná í viðbæturnar **Snjallskýsgrunnsviðbót** og **Dynamics GP-snjallský** og keyra **Uppsetningu skýjaflutnings** leiðbeiningar um uppsetningu með hjálp.</span><span class="sxs-lookup"><span data-stu-id="ffc04-113">If you are using Dynamics GP,  get the **Intelligent Cloud Base Extension** extension and the **Dynamics GP Intelligent Cloud** extension, and then run the **Cloud Migration Setup** assisted setup guide.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="ffc04-114">Flyt úr Dynamics GP með því að nota leiðbeiningar um uppsetningu með hjálp fyrir **Uppsetning skýjaflutnings** eru aðeins studdar fyrir eftirtalda markaði eins og er: Bandaríkin, Kanada, Bretland.</span><span class="sxs-lookup"><span data-stu-id="ffc04-114">Migrating from Dynamics GP using the **Cloud Migration Setup** assisted setup guide is currently only supported for the following markets: United States, Canada, United Kingdom.</span></span>

## <a name="dynamics-sl"></a><span data-ttu-id="ffc04-115">Dynamics SL</span><span class="sxs-lookup"><span data-stu-id="ffc04-115">Dynamics SL</span></span>

<span data-ttu-id="ffc04-116">Ef þú ert að nota Dynamics SL skaltu ná í viðbæturnar **Snjallskýsgrunnur** , **Microsoft Dynamics SL-snjallský** og **Microsoft Dynamics SL-ferlissnjalllisti** og keyra svo **Uppsetningu skýjaflutnings** leiðbeiningar um uppsetningu með hjálp.</span><span class="sxs-lookup"><span data-stu-id="ffc04-116">If you are using Dynamics SL, get the **Intelligent Cloud Base** extension, the **Microsoft Dynamics SL Intelligent Cloud** extension and the **Microsoft Dynamics SL History SmartLists** extension, and then run the **Cloud Migration Setup** assisted setup guide.</span></span>  

## <a name="see-also"></a><span data-ttu-id="ffc04-117">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="ffc04-117">See Also</span></span>

[<span data-ttu-id="ffc04-118">Snjöll innsýn</span><span class="sxs-lookup"><span data-stu-id="ffc04-118">Intelligent Insights</span></span>](about-intelligent-cloud.md)  
[<span data-ttu-id="ffc04-119">Snjallskýjaviðbót</span><span class="sxs-lookup"><span data-stu-id="ffc04-119">Intelligent Cloud Base Extension</span></span>](ui-extensions-intelligent-cloud.md)  
