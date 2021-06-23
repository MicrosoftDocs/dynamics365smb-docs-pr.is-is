---
title: Fínstilling Outlook fyrir fyrirtækjainnhólf þitt
description: Kynntu þér hvað hægt er að gera til að bæta upplifun með fyrirtækjainnhólfi í Microsoft Outlook.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Outlook, Microsoft 365, inbox, business inbox, WebView2, Edge, addin, add-in
ms.date: 05/12/2021
ms.author: jswymer
ms.openlocfilehash: 2fee1782057d0f45319e4d12d715c2e1e0d3d4a6
ms.sourcegitcommit: 61e279b253370cdf87b7bc1ee0f927e4f0521344
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/19/2021
ms.locfileid: "6064857"
---
# <a name="optimizing-outlook-for-your-business-inbox"></a><span data-ttu-id="88158-103">Fínstilling Outlook fyrir fyrirtækjainnhólf þitt</span><span class="sxs-lookup"><span data-stu-id="88158-103">Optimizing Outlook for Your Business Inbox</span></span> 

<span data-ttu-id="88158-104">Í þessari grein er fjallað um ýmislegt sem hægt er að gera til að hámarka upplifunina með fyrirtækjainnhólfi í Microsoft Outlook.</span><span class="sxs-lookup"><span data-stu-id="88158-104">This article discusses things you can do to get the best possible experience with the Business Inbox in Microsoft Outlook.</span></span> 

## <a name="update-outlook"></a><span data-ttu-id="88158-105">Uppfæra Outlook</span><span class="sxs-lookup"><span data-stu-id="88158-105">Update Outlook</span></span>

<span data-ttu-id="88158-106">Uppfæra í Outlook útgáfu 2012 eða nýrri.</span><span class="sxs-lookup"><span data-stu-id="88158-106">Update to Outlook version 2012 or newer.</span></span>

> [!NOTE]
> <span data-ttu-id="88158-107">Ef ekki er hægt að uppfæra Outlook í útgáfu 2012 eða nýrri þarf að tryggja að a.m.k. sé uppfært í útgáfu 1905.</span><span class="sxs-lookup"><span data-stu-id="88158-107">If you are unable to update Outlook to version 2012 or later, make sure that you at least update to version 1905.</span></span> <span data-ttu-id="88158-108">Það kemur í veg fyrir að Outlook-viðbótin geti keyrt með eldri Internet Explorer íhlutum</span><span class="sxs-lookup"><span data-stu-id="88158-108">This prevents the Outlook Add-in from running using legacy Internet Explorer components</span></span>

### <a name="how-to-check-your-version-of-outlook"></a><span data-ttu-id="88158-109">Hvernig á að athuga útgáfu þína af Outlook</span><span class="sxs-lookup"><span data-stu-id="88158-109">How to check your version of Outlook</span></span>

<span data-ttu-id="88158-110">Fylgdu þessum leiðbeiningum frá Notendaþjónustu Microsoft Office 2019 eða Microsoft 365 til að sjá hvaða útgáfu af Outlook þú ert með:</span><span class="sxs-lookup"><span data-stu-id="88158-110">Whether you use Office 2019 or Microsoft 365, follow this Microsoft Support guide to check which version of Outlook you have:</span></span>  

[<span data-ttu-id="88158-111">Um Office: Hvaða útgáfu af Office er ég að nota?</span><span class="sxs-lookup"><span data-stu-id="88158-111">About Office: What version of Office am I using?</span></span>](https://support.microsoft.com/office/about-office-what-version-of-office-am-i-using-932788b8-a3ce-44bf-bb09-e334518b8b19)

### <a name="how-to-update-outlook"></a><span data-ttu-id="88158-112">Hvernig á að uppfæra Outlook</span><span class="sxs-lookup"><span data-stu-id="88158-112">How to update Outlook</span></span>

<span data-ttu-id="88158-113">Ef þú vilt uppfæra Outlook í nýjustu útgáfuna skaltu fylgja þessum leiðbeiningum frá Notendaþjónustu Microsoft eða hafa samband við kerfisstjóra:</span><span class="sxs-lookup"><span data-stu-id="88158-113">To update Outlook to the latest version, follow this Microsoft Support guide or contact your administrator:</span></span>

[<span data-ttu-id="88158-114">Setja upp Office-uppfærslur</span><span class="sxs-lookup"><span data-stu-id="88158-114">Install Office updates</span></span>](https://support.microsoft.com/office/install-office-updates-2ab296f3-7f03-43a2-8e50-46de917611c5)

## <a name="install-microsoft-edge-webview2"></a><span data-ttu-id="88158-115">Setja upp Microsoft Edge WebView2</span><span class="sxs-lookup"><span data-stu-id="88158-115">Install Microsoft Edge WebView2</span></span>

<span data-ttu-id="88158-116">Gakktu úr skugga um að Microsoft Edge WebView2 sé uppsett í tækinu.</span><span class="sxs-lookup"><span data-stu-id="88158-116">Ensure that Microsoft Edge WebView2 is installed on your device.</span></span>

### <a name="how-to-check-if-microsoft-edge-webview2-is-installed"></a><span data-ttu-id="88158-117">Hvernig á að athuga hvort Microsoft Edge WebView2 sé uppsett</span><span class="sxs-lookup"><span data-stu-id="88158-117">How to check if Microsoft Edge WebView2 is installed</span></span> 

<span data-ttu-id="88158-118">Gerðu eftirfarandi til að athuga hvort Microsoft Edge WebView2 sé uppsett á tölvu:</span><span class="sxs-lookup"><span data-stu-id="88158-118">To check if you have Microsoft Edge WebView2 installed on a computer, do the following steps:</span></span>

<span data-ttu-id="88158-119">Úr upphafsvalmyndinni:</span><span class="sxs-lookup"><span data-stu-id="88158-119">From Start menu:</span></span>

1. <span data-ttu-id="88158-120">Veldu **Byrja** ![Windows Start](media/windows-start-icon.png "Windows upphafstákn") > **Stillingar** ![Windows stillingar](media/windows-settings-icon.png "Stillingatákn Windows") > **Forrit og eiginleikar**.</span><span class="sxs-lookup"><span data-stu-id="88158-120">Choose **Start** ![Windows Start](media/windows-start-icon.png "Windows Start icon") > **Settings** ![Windows Settings](media/windows-settings-icon.png "Windows Settings icon") > **Apps & Features**.</span></span>
2. <span data-ttu-id="88158-121">Farðu í leitargluggann og sláðu inn **WebView2**.</span><span class="sxs-lookup"><span data-stu-id="88158-121">In the search box, type **WebView2**.</span></span> <span data-ttu-id="88158-122">Ef Microsoft Edge WebView2 er sett upp sérðu færslu sem heitir **Microsoft Edge WebView2 Runtime**.</span><span class="sxs-lookup"><span data-stu-id="88158-122">If Microsoft Edge WebView2 is installed, you'll see an entry called **Microsoft Edge WebView2 Runtime**.</span></span>

<span data-ttu-id="88158-123">Í stjórnborðinu:</span><span class="sxs-lookup"><span data-stu-id="88158-123">From Control Panel:</span></span>

1. <span data-ttu-id="88158-124">Í leitarglugganum við hliðina á **Byrja** ![Windows Start](media/windows-start-icon.png "Windows upphafstákn") skaltu slá inn **Stjórnborð** og velja niðurstöðuna.</span><span class="sxs-lookup"><span data-stu-id="88158-124">In the search box next to **Start** ![Windows Start](media/windows-start-icon.png "Windows Start icon"), type **Control Panel**, and then select the result.</span></span>
2. <span data-ttu-id="88158-125">Veldu **Forrit** > **Forrit og eiginleikar**.</span><span class="sxs-lookup"><span data-stu-id="88158-125">Choose **Programs** > **Programs and Features**.</span></span>
3. <span data-ttu-id="88158-126">Farðu í leitargluggann og sláðu inn **WebView2**.</span><span class="sxs-lookup"><span data-stu-id="88158-126">In the search box, type **WebView2**.</span></span> <span data-ttu-id="88158-127">Ef Microsoft Edge WebView2 er sett upp sérðu færslu sem heitir **Microsoft Edge WebView2 Runtime**.</span><span class="sxs-lookup"><span data-stu-id="88158-127">If Microsoft Edge WebView2 is installed, you'll see an entry called **Microsoft Edge WebView2 Runtime**.</span></span>

### <a name="how-to-install-microsoft-edge-webview2"></a><span data-ttu-id="88158-128">Hvernig á að setja upp Microsoft Edge WebView2</span><span class="sxs-lookup"><span data-stu-id="88158-128">How to install Microsoft Edge WebView2</span></span> 

1. <span data-ttu-id="88158-129">Í vafranum þínum skaltu fara á [https://developer.microsoft.com/microsoft-edge/webview2/](https://developer.microsoft.com/microsoft-edge/webview2/).</span><span class="sxs-lookup"><span data-stu-id="88158-129">Using your browser, go to [https://developer.microsoft.com/microsoft-edge/webview2/](https://developer.microsoft.com/microsoft-edge/webview2/).</span></span>
2. <span data-ttu-id="88158-130">Veldu **Niðurhal**.</span><span class="sxs-lookup"><span data-stu-id="88158-130">Choose **Download**.</span></span>
3. <span data-ttu-id="88158-131">Veldu **Velja uppbyggingu** sem passar við kerfið þitt.</span><span class="sxs-lookup"><span data-stu-id="88158-131">Set **Select Architecture** to match your system.</span></span>
4. <span data-ttu-id="88158-132">Veldu **Niðurhal**.</span><span class="sxs-lookup"><span data-stu-id="88158-132">Choose **Download**.</span></span>

> [!NOTE]
> <span data-ttu-id="88158-133">Fyrirtækið gæti takmarkað hvaða íhluti er hægt að setja upp í tækinu.</span><span class="sxs-lookup"><span data-stu-id="88158-133">Your organization may have restriction on which components can be installed on your device.</span></span> <span data-ttu-id="88158-134">Hafðu samband við stjórnanda til að fá aðstoð.</span><span class="sxs-lookup"><span data-stu-id="88158-134">Contact your administrator for assistance.</span></span>

## <a name="use-a-supported-browser"></a><span data-ttu-id="88158-135">Notaðu studdan vafra</span><span class="sxs-lookup"><span data-stu-id="88158-135">Use a supported browser</span></span>

<span data-ttu-id="88158-136">Íhugaðu að nota Outlook fyrir vefinn í einhverri vafranna sem Business Central styður.</span><span class="sxs-lookup"><span data-stu-id="88158-136">Consider using Outlook for the Web in one of the browsers supported by Business Central.</span></span> <span data-ttu-id="88158-137">Listi yfir studda vafra er í [Lágmarkskröfur fyrir notkun Business Central](product-requirements.md#browsers).</span><span class="sxs-lookup"><span data-stu-id="88158-137">For a list of supported browsers, see [Minimum Requirements for Using Business Central](product-requirements.md#browsers).</span></span>

## <a name="see-also"></a><span data-ttu-id="88158-138">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="88158-138">See Also</span></span>

[<span data-ttu-id="88158-139">Undirbúðu þig fyrir að gera viðskipti</span><span class="sxs-lookup"><span data-stu-id="88158-139">Getting Ready for Doing Business</span></span>](ui-get-ready-business.md)  
[<span data-ttu-id="88158-140">Sækja Business Central í fartækið mitt</span><span class="sxs-lookup"><span data-stu-id="88158-140">Getting Business Central on my Mobile Device</span></span>](install-mobile-app.md)  
[<span data-ttu-id="88158-141">Senda skjöl í tölvupósti</span><span class="sxs-lookup"><span data-stu-id="88158-141">Send Documents by Email</span></span>](ui-how-send-documents-email.md)  
[<span data-ttu-id="88158-142">Fjármál</span><span class="sxs-lookup"><span data-stu-id="88158-142">Finance</span></span>](finance.md)  
[<span data-ttu-id="88158-143">Sala</span><span class="sxs-lookup"><span data-stu-id="88158-143">Sales</span></span>](sales-manage-sales.md)  
[<span data-ttu-id="88158-144">Innkaup</span><span class="sxs-lookup"><span data-stu-id="88158-144">Purchasing</span></span>](purchasing-manage-purchasing.md)  
[<span data-ttu-id="88158-145">Lágmarkskröfur fyrir Outlook</span><span class="sxs-lookup"><span data-stu-id="88158-145">Minimum Requirements for Outlook</span></span>](product-requirements.md#outlook)  
[<span data-ttu-id="88158-146">Notkun innbóta í Outlook á vefnum</span><span class="sxs-lookup"><span data-stu-id="88158-146">Using add-ins in Outlook on the web</span></span>](https://support.office.com/article/Using-Add-ins-in-Outlook-on-the-web-8f2ce816-5df4-44a5-958c-f7f9d6dabdce?appver=OWB150)  


[!INCLUDE[footer-include](includes/footer-banner.md)]