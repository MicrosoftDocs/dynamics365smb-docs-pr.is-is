---
title: Uppsetning vafrans
description: Lýsir því hvernig á að setja upp vafra til að vinna með Business Central og sasmþættum vörum.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Teams, web client, troubleshooting, errors
ms.date: 04/01/2021
ms.author: jswymer
ms.openlocfilehash: 90625ed6d5664efc9605aeacbc66d8174e55799d
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5776298"
---
# <a name="setting-up-and-troubleshooting-your-browser-to-work-with-business-central-web-client"></a><span data-ttu-id="81b2a-103">Uppsetning og úrræðaleit vafrans til að vinna með Business Central-vefbiðlara</span><span class="sxs-lookup"><span data-stu-id="81b2a-103">Setting Up and Troubleshooting Your Browser to Work With Business Central Web Client</span></span>

<span data-ttu-id="81b2a-104">Þessi grein útskýrir hvernig á að setja upp vafrann þannig að [!INCLUDE[web_client](includes/web_client.md)] og allir eiginleikar þess virki rétt.</span><span class="sxs-lookup"><span data-stu-id="81b2a-104">This article explains how to set up your browser so that the [!INCLUDE[web_client](includes/web_client.md)] and all its features work properly.</span></span> <span data-ttu-id="81b2a-105">Lestu þessa grein ef þú átt í vandræðum með að opna [!INCLUDE[web_client](includes/web_client.md)], vegna þess að stillingar vafrans þíns kunna að valda einhverjum vandamálum.</span><span class="sxs-lookup"><span data-stu-id="81b2a-105">Read this article if you're having problems opening the [!INCLUDE[web_client](includes/web_client.md)], because some problems may be caused by your browser's settings.</span></span>

<span data-ttu-id="81b2a-106">Í greininni er að finna upplýsingar fyrir uppsetningu Microsoft Edge, en kröfur um JavaScript, fótspor og sprettiglugga eru þær sömu fyrir alla studda vafra.</span><span class="sxs-lookup"><span data-stu-id="81b2a-106">The article provides details for setting up Microsoft Edge, but the requirements for JavaScript, cookies, and pop-ups are the same for all supported browsers.</span></span> <span data-ttu-id="81b2a-107">Fyrir aðra vafra skal skoða leiðbeiningarnar sem framleiðandinn gefur upp.</span><span class="sxs-lookup"><span data-stu-id="81b2a-107">For other browsers, refer to the instructions provided by the manufacturer.</span></span>  

## <a name="use-a-supported-browser"></a><span data-ttu-id="81b2a-108">Notaðu studdan vafra</span><span class="sxs-lookup"><span data-stu-id="81b2a-108">Use a supported browser</span></span>

<span data-ttu-id="81b2a-109">Gættu þess að nota einn af studdu vöfrunum.</span><span class="sxs-lookup"><span data-stu-id="81b2a-109">Make sure to use a one of the supported browsers.</span></span> <span data-ttu-id="81b2a-110">Sjá [Lágmarkskröfur fyrir notkun Business Central](product-requirements.md#browsers).</span><span class="sxs-lookup"><span data-stu-id="81b2a-110">See [Minimum Requirements for Using Business Central](product-requirements.md#browsers).</span></span>  

## <a name="allow-javascript-from-business-central"></a><span data-ttu-id="81b2a-111">Leyfa JavaScript úr Business Central</span><span class="sxs-lookup"><span data-stu-id="81b2a-111">Allow JavaScript from Business Central</span></span>

<span data-ttu-id="81b2a-112">*Vandamál:*</span><span class="sxs-lookup"><span data-stu-id="81b2a-112">*Problem:*</span></span>

<span data-ttu-id="81b2a-113">Ef vafrinn leyfir ekki JavaScript muntu sjá **NotSupported/DisabledJavaScript** í veffangastikunni og **HTTP Error 404.0 - Not Found** skiaboð birtast þegar reynt er að opna [!INCLUDE[prod_short](includes/prod_short.md)], og</span><span class="sxs-lookup"><span data-stu-id="81b2a-113">If the browser doesn't allow JavaScript, you'll see **NotSupported/DisabledJavaScript** in the address bar and an **HTTP Error 404.0 - Not Found** message when you try to open [!INCLUDE[prod_short](includes/prod_short.md)], and the</span></span> 

<!-- http://localhost:8080/NotSupported/DisabledJavaScript HTTP Error 404.0 - Not Found
The resource you are looking for has been removed, had its name changed, or is temporarily unavailable. -->

<span data-ttu-id="81b2a-114">*Laga:*</span><span class="sxs-lookup"><span data-stu-id="81b2a-114">*Fix:*</span></span>

1. <span data-ttu-id="81b2a-115">Í Microsoft Edge, ferðu í **Stillingar** > **Fótspor og heimildir svæðis** > **JavaScript**.</span><span class="sxs-lookup"><span data-stu-id="81b2a-115">In Microsoft Edge, go to **Settings** > **Cookies and site permissions** > **JavaScript**.</span></span>
2. <span data-ttu-id="81b2a-116">Framkvæmdu eitt af eftirfarandi skrefum.</span><span class="sxs-lookup"><span data-stu-id="81b2a-116">Do one of the following steps.</span></span> <span data-ttu-id="81b2a-117">Veldu skrefið sem fyrirtækið ráðleggur:</span><span class="sxs-lookup"><span data-stu-id="81b2a-117">Choose the step that is recommended by your organization:</span></span>

    - <span data-ttu-id="81b2a-118">Færa **Leyft** til vinstri (slökkt).</span><span class="sxs-lookup"><span data-stu-id="81b2a-118">Move the **Allowed** toggle to the left (Off).</span></span> <span data-ttu-id="81b2a-119">Síðan skal velja **Bæta við** og slá inn vistfang (URL) fyrir [!INCLUDE[prod_short](includes/prod_short.md)] í reitnum **Svæði**.</span><span class="sxs-lookup"><span data-stu-id="81b2a-119">Then, select **Add** and type the address (URL) for [!INCLUDE[prod_short](includes/prod_short.md)] in the **Site** box.</span></span> <span data-ttu-id="81b2a-120">Velja **Bæta við** að þessu loknu.</span><span class="sxs-lookup"><span data-stu-id="81b2a-120">Select **Add** when done.</span></span>
    - <span data-ttu-id="81b2a-121">Færa **Leyft** til hægri (kveikt).</span><span class="sxs-lookup"><span data-stu-id="81b2a-121">Move the **Allowed** toggle to the right (On).</span></span>

## <a name="allow-cookies-from-business-central"></a><span data-ttu-id="81b2a-122">Leyfa kökur úr Business Central</span><span class="sxs-lookup"><span data-stu-id="81b2a-122">Allow cookies from Business Central</span></span>

<span data-ttu-id="81b2a-123">*Vandamál:*</span><span class="sxs-lookup"><span data-stu-id="81b2a-123">*Problem:*</span></span>

<span data-ttu-id="81b2a-124">Ef vafrinn leyfir ekki kökur muntu fá eftirfarandi villu:</span><span class="sxs-lookup"><span data-stu-id="81b2a-124">If the browser doesn't allow cookies, you'll get the following error:</span></span>

<span data-ttu-id="81b2a-125">**Því miður fannst síðan ekki. Athugaðu netfangið og reyndu aftur.**</span><span class="sxs-lookup"><span data-stu-id="81b2a-125">**Sorry, the page could not be found. Please check the address and try again.**</span></span> 

<span data-ttu-id="81b2a-126">*Laga:*</span><span class="sxs-lookup"><span data-stu-id="81b2a-126">*Fix:*</span></span>

1. <span data-ttu-id="81b2a-127">Í Microsoft Edge, ferðu í **Stillingar** > **Fótspor og heimildir svæðis** > **Fótspor og gögn svæðis**.</span><span class="sxs-lookup"><span data-stu-id="81b2a-127">In Microsoft Edge, go to **Settings** > **Cookies and site permissions** > **Cookies and site data**.</span></span>
2. <span data-ttu-id="81b2a-128">Færið **Leyfa vefsvæðum að vista og lesa kökugögn** til hægri (kveikt).</span><span class="sxs-lookup"><span data-stu-id="81b2a-128">Move the **Allow sites to save and read cookie data** toggle to the right (On).</span></span>  

## <a name="allow-pop-ups-from-business-central"></a><a name="popup"></a><span data-ttu-id="81b2a-129">Leyfa sprettiglugga úr Business Central</span><span class="sxs-lookup"><span data-stu-id="81b2a-129">Allow pop-ups from Business Central</span></span>

[!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="81b2a-130">samþættist við nokkrar vörur.</span><span class="sxs-lookup"><span data-stu-id="81b2a-130">integrates with several products.</span></span> <span data-ttu-id="81b2a-131">Í sumum tilvikum, eins og með Microsoft Teams, opnast [!INCLUDE[prod_short](includes/prod_short.md)] eða „Sprettigluggar“ innan vörunnar.</span><span class="sxs-lookup"><span data-stu-id="81b2a-131">In some cases, like with Microsoft Teams, [!INCLUDE[prod_short](includes/prod_short.md)] opens, or "pop-ups", within the product.</span></span> <span data-ttu-id="81b2a-132">Þessi eiginleiki krefst þess að vafrinn þinn leyfi sprettiglugga í [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="81b2a-132">This capability requires that your browser allows pop-ups from [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>

<span data-ttu-id="81b2a-133">*Vandamál:*</span><span class="sxs-lookup"><span data-stu-id="81b2a-133">*Problem:*</span></span>

<span data-ttu-id="81b2a-134">Ef verið er að læsa sprettiglugga fyrir [!INCLUDE[prod_short](includes/prod_short.md)] birtast skilaboð sem svipar til eftirfarandi skilaboða:</span><span class="sxs-lookup"><span data-stu-id="81b2a-134">If pop-ups for [!INCLUDE[prod_short](includes/prod_short.md)] are being blocked, you get a message similar to the following message:</span></span>

<span data-ttu-id="81b2a-135">**Eitthvað fór úrskeiðis. Vafrinn kann að hindra sprettiglugga sem Business Central þarf á að halda.**</span><span class="sxs-lookup"><span data-stu-id="81b2a-135">**Something went wrong. Your browser may be blocking pop-ups needed by Business Central.**</span></span>

<!--
Something went wrong
Your browser may be blocking pop-ups needed by Business Central.

Change your browser settings to allow pop-ups or allow this for trusted domains, then try again.
If these settings are managed for your organization, you should contact your administrator for assistance.

Try again
-->
<span data-ttu-id="81b2a-136">*Laga:*</span><span class="sxs-lookup"><span data-stu-id="81b2a-136">*Fix:*</span></span>

1. <span data-ttu-id="81b2a-137">Í Microsoft Edge, er farið í **Stillingar** > **Fótspor og heimildir svæðis** > **Sprettigluggar og áframsendingar**.</span><span class="sxs-lookup"><span data-stu-id="81b2a-137">In Microsoft Edge, go to **Settings** > **Cookies and site permissions** > **Pop-ups and redirects**.</span></span>
2. <span data-ttu-id="81b2a-138">Færa **Lokað fyrir** til hægri (kveikt).</span><span class="sxs-lookup"><span data-stu-id="81b2a-138">Move the **Blocked** toggle to the right (On).</span></span>
3. <span data-ttu-id="81b2a-139">Veljið **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="81b2a-139">Select **Add**.</span></span> <span data-ttu-id="81b2a-140">Í reitinn **Svæði** skal slá inn `https://businesscentral.dynamics.com` og síðan velja **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="81b2a-140">In the **Site** box, type `https://businesscentral.dynamics.com`, then select **Add**.</span></span>

## <a name="see-also"></a><span data-ttu-id="81b2a-141">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="81b2a-141">See Also</span></span>

[<span data-ttu-id="81b2a-142">Úrræðaleit Teams</span><span class="sxs-lookup"><span data-stu-id="81b2a-142">Troubleshooting Teams</span></span>](admin-teams-troubleshooting.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]