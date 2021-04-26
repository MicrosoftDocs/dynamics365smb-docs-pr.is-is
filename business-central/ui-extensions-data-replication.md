---
title: Viðbætur skýjaflutnings
description: Nota skal flutningsviðbætur í ský til að flytja gögn innanhúss í Business Central á netinu. Þessar viðbætur færa innanhússgögn í skýið svo hægt sé að nota Business Central á netinu með fyrirliggjandi gögnum.
author: jenolson
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, import, implement
ms.reviewer: edupont
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: f02face497affd1fd1467c118e10e69f2be39b85
ms.sourcegitcommit: 951d3c9d541f0b1d26712d37e253c2958dae3321
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/13/2021
ms.locfileid: "5889125"
---
# <a name="cloud-migration-extensions-for-migrating-to-business-central-online"></a><span data-ttu-id="72404-104">Skýjaflutningsviðbætur fyrir flutning á Business Central Online</span><span class="sxs-lookup"><span data-stu-id="72404-104">Cloud Migration Extensions for Migrating to Business Central Online</span></span>

<span data-ttu-id="72404-105">Það fer eftir staðbundinni lausn, en nota þarf aðrar viðbætur til að tengja gögnin við [!INCLUDE[prod_short](includes/prod_short.md)] á netinu í þeim tilgangi að flytja lausnina yfir í skýið.</span><span class="sxs-lookup"><span data-stu-id="72404-105">Depending on your on-premises solution, you must use different extensions to connect your data with [!INCLUDE[prod_short](includes/prod_short.md)] online for purposes of migrating your solution to the cloud.</span></span>  

<span data-ttu-id="72404-106">Ef þú ert að nota eina af studdu vörum á staðnum geturðu stillt skýjaumhverfið sem byggist á vörumiðaðri viðbót.</span><span class="sxs-lookup"><span data-stu-id="72404-106">If you are using one of the supported on-premises products, you can configure your cloud environment based on a product-specific extension.</span></span> <span data-ttu-id="72404-107">Þegar skýjaumhverfið þitt hefur verið grunnstillt geturðu flutt gögn úr þínum lausnum innanhúss í [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="72404-107">Once your cloud environment is configured, you will be able to migrate data from your on-premises solution to [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="72404-108">Þetta gerir þér kleift að nýta hvað skýið býður upp á fyrir fyrirtækið þitt, svo sem aukið innsýn í fyrirtæki þitt, gervigreind, aðgang að mörgum tækjum og aðgang hvenær sem er, hvar sem er.</span><span class="sxs-lookup"><span data-stu-id="72404-108">This will enable you to take full advantage of what the cloud has to offer your business such as, enhanced insights into your business, artificial intelligence, multiple device access, and anytime, anywhere access.</span></span>  

<span data-ttu-id="72404-109">Frekari upplýsingar er að finna í [Flytja inn innanhússgögn í Business Central Online](/dynamics365/business-central/dev-itpro/administration/migrate-data) í efnisstjórnunarefninu fyrir [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="72404-109">For more information, see [Migrating On-Premises Data to Business Central Online](/dynamics365/business-central/dev-itpro/administration/migrate-data) in the administration content for [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>  

## <a name="business-central-on-premises"></a><span data-ttu-id="72404-110">Business Central á staðnum</span><span class="sxs-lookup"><span data-stu-id="72404-110">Business Central on-premises</span></span>

<span data-ttu-id="72404-111">Ef þú ert að nota uppsetningu á staðnum af [!INCLUDE[prod_short](includes/prod_short.md)], náðu þá í viðbæturnar **Snjallskýsgrunnur** og **Business Central-snjallský** og keyrðu **Uppsetningu skýjaflutnings** leiðbeiningar um uppsetningu með hjálp .</span><span class="sxs-lookup"><span data-stu-id="72404-111">If you are using an on-premises deployment of [!INCLUDE[prod_short](includes/prod_short.md)], get the **Intelligent Cloud Base** extension and the **Business Central Intelligent Cloud** extension, and then run the **Cloud Migration Setup** assisted setup guide.</span></span>  

## <a name="dynamics-gp"></a><span data-ttu-id="72404-112">Dynamics GP</span><span class="sxs-lookup"><span data-stu-id="72404-112">Dynamics GP</span></span>

<span data-ttu-id="72404-113">Ef þú ert að nota Dynamics GP skaltu ná í viðbæturnar **Snjallskýsgrunnsviðbót** og **Dynamics GP-snjallský** og keyra **Uppsetningu skýjaflutnings** leiðbeiningar um uppsetningu með hjálp.</span><span class="sxs-lookup"><span data-stu-id="72404-113">If you are using Dynamics GP,  get the **Intelligent Cloud Base Extension** extension and the **Dynamics GP Intelligent Cloud** extension, and then run the **Cloud Migration Setup** assisted setup guide.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="72404-114">Flyt úr Dynamics GP með því að nota leiðbeiningar um uppsetningu með hjálp fyrir **Uppsetning skýjaflutnings** eru aðeins studdar fyrir eftirtalda markaði eins og er: Bandaríkin, Kanada, Bretland.</span><span class="sxs-lookup"><span data-stu-id="72404-114">Migrating from Dynamics GP using the **Cloud Migration Setup** assisted setup guide is currently only supported for the following markets: United States, Canada, United Kingdom.</span></span>

## <a name="dynamics-sl"></a><span data-ttu-id="72404-115">Dynamics SL</span><span class="sxs-lookup"><span data-stu-id="72404-115">Dynamics SL</span></span>

<span data-ttu-id="72404-116">Ef þú ert að nota Dynamics SL skaltu ná í viðbæturnar **Snjallskýsgrunnur**, **Microsoft Dynamics SL-snjallský** og **Microsoft Dynamics SL-ferlissnjalllisti** og keyra svo **Uppsetningu skýjaflutnings** leiðbeiningar um uppsetningu með hjálp.</span><span class="sxs-lookup"><span data-stu-id="72404-116">If you are using Dynamics SL, get the **Intelligent Cloud Base** extension, the **Microsoft Dynamics SL Intelligent Cloud** extension and the **Microsoft Dynamics SL History SmartLists** extension, and then run the **Cloud Migration Setup** assisted setup guide.</span></span>  

## <a name="see-also"></a><span data-ttu-id="72404-117">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="72404-117">See Also</span></span>

[<span data-ttu-id="72404-118">Grunnviðbót skýjaflutnings</span><span class="sxs-lookup"><span data-stu-id="72404-118">Cloud Migration Base Extension</span></span>](ui-extensions-intelligent-cloud.md)  
[<span data-ttu-id="72404-119">Flytja inn innanhússgögn í Business Central Online</span><span class="sxs-lookup"><span data-stu-id="72404-119">Migrating On-Premises Data to Business Central Online</span></span>](/dynamics365/business-central/dev-itpro/administration/migrate-data)  

[!INCLUDE[footer-include](includes/footer-banner.md)]