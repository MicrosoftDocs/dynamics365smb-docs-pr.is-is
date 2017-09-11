---
title: "Hvernig skal: Setja upp GetAddress.io UK Postcodes viðbótina | Microsoft Docs"
description: "Lýsir þeirri almennu virkni sem þú notar til að vinna með gögn í Financials, eins og t.d. að færa inn gildi, raða gögnum og breyta yfirliti."
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: getaddress.io, postcodes, extension
ms.date: 06/02/2017
ms.author: bholtorf
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: c5a99f7a90b2f832bba3eb088d0faa7514c14708
ms.contentlocale: is-is
ms.lasthandoff: 09/11/2017

---
# <a name="how-to-set-up-the-getaddressio-uk-postcodes-extension"></a><span data-ttu-id="bc373-103">Hvernig skal: Setja upp GetAddress.io UK Postcodes viðbótina</span><span class="sxs-lookup"><span data-stu-id="bc373-103">How to: Set Up the GetAddress.io UK Postcodes Extension</span></span>
<span data-ttu-id="bc373-104">Þessi viðbót gerir það auðvelt að færa inn heimilisföng í Bretlandi fyrir aðila eins og viðskiptavini, tengiliði, starfsmenn, söluaðila, bankareikninga og svo framvegis.</span><span class="sxs-lookup"><span data-stu-id="bc373-104">This extension makes it easy to enter addresses in the UK for entities like customers, contacts, employees, vendors, bank accounts, and so on.</span></span> 

<span data-ttu-id="bc373-105">The GetAddress.io UK Postcodes viðbótin notar getAddress API til að finna heimilisföng í póstnúmerum í Bretlandi.</span><span class="sxs-lookup"><span data-stu-id="bc373-105">The GetAddress.io UK Postcodes extension uses the getAddress API to find addresses in postcodes in the UK.</span></span> <span data-ttu-id="bc373-106">Til að nota viðbótina þarf að hafa áskrift API-lykil fyrir getAddress API.</span><span class="sxs-lookup"><span data-stu-id="bc373-106">To use the extension, you need to get a plan and an API Key for the getAddress API.</span></span> <span data-ttu-id="bc373-107">Það er auðvelt og við aðstoðum við það þegar þú setur upp GetAddress.io UK Postcodes viðbótina.</span><span class="sxs-lookup"><span data-stu-id="bc373-107">That's easy, and we help you do that when you set up the GetAddress.io UK Postcodes extension.</span></span> <span data-ttu-id="bc373-108">Áætlanir eru byggðar á notkun, eða því sem stundum er kallað köll.</span><span class="sxs-lookup"><span data-stu-id="bc373-108">Plans are based on use, or what's sometimes referred to as calls.</span></span> <span data-ttu-id="bc373-109">Köll í þessu tilviki er þegar [!INCLUDE[d365fin](includes/d365fin_md.md)] birtir lista yfir heimilisföng í póstnúmeri.</span><span class="sxs-lookup"><span data-stu-id="bc373-109">A call, in this case, is when [!INCLUDE[d365fin](includes/d365fin_md.md)] displays a list of addresses in a postcode.</span></span> <span data-ttu-id="bc373-110">Veldu áætlunin sem hentar þér best út frá því hversu oft þú bætir við heimilisföngum.</span><span class="sxs-lookup"><span data-stu-id="bc373-110">Depending on how often you add addresses, choose the plan that is best for you.</span></span> <span data-ttu-id="bc373-111">Ef þú velur eingöngu **Fá API-lykil** á síðunni notarðu áætlunina **Ókeypis**, sem leyfir þér að bæta við 20 heimilisföngum á dag og gildir í 30 daga.</span><span class="sxs-lookup"><span data-stu-id="bc373-111">If you just choose **Get API Key** in the page, you'll use the **Free** plan, which lets you add 20 addresses per day, and is valid for 30 days.</span></span> 

##<a name="to-set-up-the-getaddressio-uk-postcodes-extension"></a><span data-ttu-id="bc373-112">Til að setja upp GetAddress.io UK Postcodes viðbótina</span><span class="sxs-lookup"><span data-stu-id="bc373-112">To set up the GetAddress.io UK Postcodes extension</span></span> 
1. <span data-ttu-id="bc373-113">Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Þjónustutengingar** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="bc373-113">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Service Connections**, and then choose the related link.</span></span>  
2. <span data-ttu-id="bc373-114">Í reitnum **Þjónustutengingar** er valið **UK Postcode Service**.</span><span class="sxs-lookup"><span data-stu-id="bc373-114">In the **Service Connections** window, choose **UK Postcode Service**.</span></span>
3. <span data-ttu-id="bc373-115">Á síðunni **Grunnstilling póstnúmera** skal velja **Slökkt**.</span><span class="sxs-lookup"><span data-stu-id="bc373-115">In the **Postcode provider configuration** page, choose **Disabled**.</span></span>
4. <span data-ttu-id="bc373-116">Í reitnum **Þjónustuval póstnúmerakóða** er valið **GetAddress.io**.</span><span class="sxs-lookup"><span data-stu-id="bc373-116">In the **Postal code service selection** window, choose **GetAddress.io**.</span></span>
5. <span data-ttu-id="bc373-117">Í **GetAddress.io Config** glugganum er valið **Sækja API-lykilinn** til að opna á **Áætlanir** síðuna á vefsetrinu getAddress API.</span><span class="sxs-lookup"><span data-stu-id="bc373-117">In the **GetAddress.io Config** window, choose **Get API Key** to open the **Plans** page on the website for the getAddress API.</span></span>  

    > [!NOTE]  
>   <span data-ttu-id="bc373-118">Hugsanlega þarf að leyfa sprettiglugga í vafranum.</span><span class="sxs-lookup"><span data-stu-id="bc373-118">You might need to allow pop-ups in your browser.</span></span>
6. <span data-ttu-id="bc373-119">Kauptu áætlun, eða veldu bara **Fá API-lykil** og gefðu síðan upp netfangið þitt.</span><span class="sxs-lookup"><span data-stu-id="bc373-119">Purchase a plan, or just choose **Get API Key**, and then provide your email address.</span></span>
7. <span data-ttu-id="bc373-120">Opnaðu póstinn frá getAddress.io og afritaðu API-lykilinn.</span><span class="sxs-lookup"><span data-stu-id="bc373-120">Open the email from getAddress.io, and copy the API key.</span></span> <span data-ttu-id="bc373-121">Lykilinn er í **API-lykilinn þinn**.</span><span class="sxs-lookup"><span data-stu-id="bc373-121">The key is under the **Your API Key** heading.</span></span>
8. <span data-ttu-id="bc373-122">Í **GetAddress.io Config** glugganum límirðu API-lykilinn inn í **API-lykill** og velur svo **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="bc373-122">In the **GetAddress.io Config** window, paste the API key in the **API Key** field, and then choose **OK**.</span></span>
9. <span data-ttu-id="bc373-123">Í reitnum **Þjónustutengingar** skaltu stafðesta að **Aðsetursveit** reiturinn sýni **GetAddress.io**.</span><span class="sxs-lookup"><span data-stu-id="bc373-123">In the **Service Connections** page, verify that the **Address Provider** field shows **GetAddress.io**.</span></span> <span data-ttu-id="bc373-124">Ef svo er, er þjónustan virkjuð.</span><span class="sxs-lookup"><span data-stu-id="bc373-124">If it does, the service is enabled.</span></span>

## <a name="see-also"></a><span data-ttu-id="bc373-125">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="bc373-125">See Also</span></span>
<span data-ttu-id="bc373-126">[GetAddress.io UK póstnúmer](ui-extensions-getaddressio.md)
[Sérstilling [!INCLUDE[d365fin](includes/d365fin_md.md)] Nota viðbætur](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="bc373-126">[GetAddress.io UK Postcodes](ui-extensions-getaddressio.md)
[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions](ui-extensions.md)</span></span>  
<span data-ttu-id="bc373-127">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="bc373-127">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
