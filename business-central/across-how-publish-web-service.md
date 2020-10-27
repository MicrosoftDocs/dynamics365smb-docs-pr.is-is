---
title: Sýna hluti sem vefþjónustu
description: Birta hluti sem vefþjónustu til að þeir séu undir eins í boði á Business Central.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.search.keywords: ''
ms.date: 10/08/2020
ms.author: edupont
ms.openlocfilehash: 658816cfb65580404bc8ef10472a5b62c6815c9e
ms.sourcegitcommit: 4bca699d2a5ce182eb5572d72fac4fb478c4f293
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/12/2020
ms.locfileid: "3989489"
---
# <a name="publish-a-web-service"></a><span data-ttu-id="6372f-103">Birta vefþjónustu</span><span class="sxs-lookup"><span data-stu-id="6372f-103">Publish a Web Service</span></span>

<span data-ttu-id="6372f-104">Vefþjónustur eru létt leið til að gera virkni forrita aðgengilega ýmsum utanaðkomandi kerfum og notendum.</span><span class="sxs-lookup"><span data-stu-id="6372f-104">Web services are a lightweight way to make application functionality available to different kinds of external systems and users.</span></span> <span data-ttu-id="6372f-105">Sjálfgefið er að [!INCLUDE[d365fin](includes/d365fin_md.md)] gefi upp nokkra hluti sem vefþjónustur fyrir betri samþættingu við aðra Microsoft-þjónustu.</span><span class="sxs-lookup"><span data-stu-id="6372f-105">By default, [!INCLUDE[d365fin](includes/d365fin_md.md)] exposes a number of objects as web services for better integration with other Microsoft services.</span></span> <span data-ttu-id="6372f-106">Þú getur bætt öðrum vefþjónustum við eftir því hvað reksturinn þarfnast.</span><span class="sxs-lookup"><span data-stu-id="6372f-106">You can add other web services as your business requires.</span></span>  

<span data-ttu-id="6372f-107">Settu upp vefþjónustu í [!INCLUDE[d365fin](includes/d365fin_md.md)] og birtu síðan vefþjónustuna þannig að hún sé aðgengileg sannvottuðu notendum.</span><span class="sxs-lookup"><span data-stu-id="6372f-107">Set up a web service in [!INCLUDE[d365fin](includes/d365fin_md.md)], and then publish the web service so that it is available to authenticated users.</span></span> <span data-ttu-id="6372f-108">Allir heimilaðir notendur geta opnað lýsigögn fyrir vefþjónustu, en aðeins notendur með nægilegar heimildir geta opnað raungögn.</span><span class="sxs-lookup"><span data-stu-id="6372f-108">All authorized users can access metadata for web services, but only users who have sufficient permissions can access actual data.</span></span>  

## <a name="creating-and-publishing-a-web-service"></a><span data-ttu-id="6372f-109">Vefþjónusta stofnuð og gefin út</span><span class="sxs-lookup"><span data-stu-id="6372f-109">Creating and Publishing a Web Service</span></span>

<span data-ttu-id="6372f-110">Eftirfarandi skref skýra hvernig vefþjónusta er búin til og gefin út.</span><span class="sxs-lookup"><span data-stu-id="6372f-110">The following steps explain how to create and publish a web service.</span></span>  

### <a name="to-create-and-publish-a-web-service"></a><span data-ttu-id="6372f-111">Til að stofna og gefa út vefþjónustu</span><span class="sxs-lookup"><span data-stu-id="6372f-111">To create and publish a web service</span></span>  

1. <span data-ttu-id="6372f-112">Veldu táknið ![ljósapera sem opnar eiginleikan „Viðmótsleit“](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera"), sláðu inn **vefþjónusta** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="6372f-112">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Web Services** , and then choose the related link.</span></span>  
2. <span data-ttu-id="6372f-113">Á síðunni **Vefþjónusta** veljið **Nýtt** .</span><span class="sxs-lookup"><span data-stu-id="6372f-113">On the **Web Services** page, choose **New** .</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    > [!NOTE]  
    > <span data-ttu-id="6372f-114">**Kótaeining** og **Síða** eru gildar tegundir fyrir SOAP-vefþjónustu.</span><span class="sxs-lookup"><span data-stu-id="6372f-114">**Codeunit** and **Page** are valid types for SOAP web services.</span></span> <span data-ttu-id="6372f-115">**Síða** og **Fyrirspurn** eru gildar gerðir fyrir OData-vefþjónustu.</span><span class="sxs-lookup"><span data-stu-id="6372f-115">**Page** and **Query** are valid types for OData web services.</span></span> <span data-ttu-id="6372f-116">Frá og með útgáfu 16.3, er **Codeunit** einnig gild gerð fyrir OData v4 vefþjónustur, en þá er engin vefslóð sýnd í notandaviðmótinu.</span><span class="sxs-lookup"><span data-stu-id="6372f-116">Starting with version 16.3, **Codeunit** is also a valid type for OData v4 web services, but then no URL is shown in the user interface.</span></span> <span data-ttu-id="6372f-117">Ef gagnagrunnurinn inniheldur mörg fyrirtæki er hægt að velja Kenni hlutar sem á aðeins við eitt af fyrirtækjunum.</span><span class="sxs-lookup"><span data-stu-id="6372f-117">Also, if the database contains multiple companies, you can choose an object ID that is specific to one of the companies.</span></span>  
    > <span data-ttu-id="6372f-118">Ef heiti þjónustunnar sýnilegt notendum vefþjónustunnar og það gegnir mikilvægu hlutverki í að auðkenna og þekkja vefþjónustuna. Því skaltu gefa henni merkingarbært heiti.</span><span class="sxs-lookup"><span data-stu-id="6372f-118">Finally, the service name is visible to consumers of your web service and is the basis for identifying and distinguishing web services, so you should make the name meaningful.</span></span>

3. <span data-ttu-id="6372f-119">Veldu gátreitinn í dálkinum **Útgefið** .</span><span class="sxs-lookup"><span data-stu-id="6372f-119">Select the check box in the **Published** column.</span></span>  

<span data-ttu-id="6372f-120">Þegar vefþjónusta er gefin út sýna reitirnir **OData-vefslóð** og **SOAP-vefslóð** nýju vefslóðirnar.</span><span class="sxs-lookup"><span data-stu-id="6372f-120">When you publish the web service, the **OData URL** and **SOAP URL** fields show the new URLs.</span></span> <span data-ttu-id="6372f-121">Hins vegar, fyrir codeunit sem gefið er upp sem OData v4 óbundnar aðgerðir, eru reitir vefslóða ekki sýndir.</span><span class="sxs-lookup"><span data-stu-id="6372f-121">However, for codeunits that are exposed as OData v4 unbound actions, the URL fields are not shown.</span></span>  

<span data-ttu-id="6372f-122">Hægt er að prófa vefþjónustuna strax með því að velja tengla í reitunum **OData-vefslóð** og **SOAP-vefslóð** .</span><span class="sxs-lookup"><span data-stu-id="6372f-122">You can test the web service immediately by choosing the links in the **OData URL** and **SOAP URL** fields.</span></span> <span data-ttu-id="6372f-123">Einnig er hægt að afrita gildið í reitnum og vista það til síðari nota.</span><span class="sxs-lookup"><span data-stu-id="6372f-123">Optionally, copy the value of the field and save it for later use.</span></span> <span data-ttu-id="6372f-124">Til að prófa codeunit sem gefið er upp sem OData v4 óbundnar aðgerðir, skal fylgja leiðbeiningunum í hlutanum [Sannprófa aðgengileika vefþjónustu](/dynamics365/business-central/dev-itpro/developer/devenv-creating-and-interacting-with-odatav4-unbound-action#verifying-web-service-availability) í efni þróunaraðila.</span><span class="sxs-lookup"><span data-stu-id="6372f-124">To test codeunits that are exposed as OData v4 unbound actions, follow the instructions in the [Verifying web service availability](/dynamics365/business-central/dev-itpro/developer/devenv-creating-and-interacting-with-odatav4-unbound-action#verifying-web-service-availability) section in the developer content.</span></span>

> [!NOTE]
> <span data-ttu-id="6372f-125">Ef hlutirnir sem þú hefur birt sem vefþjónustur eiga ekki að vera aðgengilegir frá [!INCLUDE[prodshort](includes/prodshort.md)] online verður þú að merkja aðferðirnar í kóðanum sem `[Scope('OnPrem')]`.</span><span class="sxs-lookup"><span data-stu-id="6372f-125">If the objects that you expose as web services must not be accessible from [!INCLUDE[prodshort](includes/prodshort.md)] online, you must mark the methods exposed in the code as `[Scope('OnPrem')]`.</span></span> <span data-ttu-id="6372f-126">Frekari upplýsingar má sjá í [Umfangseigind](/dynamics365/business-central/dev-itpro/developer/methods/devenv-scope-attribute).</span><span class="sxs-lookup"><span data-stu-id="6372f-126">For more information, see [Scope Attribute](/dynamics365/business-central/dev-itpro/developer/methods/devenv-scope-attribute).</span></span>

<span data-ttu-id="6372f-127">Eftir að þú birtir vefþjónustu, hafa ytri aðilar aðgang að henni.</span><span class="sxs-lookup"><span data-stu-id="6372f-127">After you publish a web service, it is available to external parties.</span></span> <span data-ttu-id="6372f-128">Hægt er að staðfesta að vefþjónustan sé tiltæk með því að nota vafra eða með því að velja tengilinn í reitunum **OData-vefslóð** og **SOAP-vefslóð** á síðunni **Vefþjónusta** .</span><span class="sxs-lookup"><span data-stu-id="6372f-128">You can verify the availability of that web service by using a browser, or choose the link in the **OData URL** and **SOAP URL** fields on the **Web Services** page.</span></span> <span data-ttu-id="6372f-129">Eftirfarandi ferli sýnir hvernig hægt er að staðfesta aðgengi að vefþjónustunni fyrir notkun síðar.</span><span class="sxs-lookup"><span data-stu-id="6372f-129">The following procedure illustrates how you can verify the availability of the web service for later use.</span></span>  

### <a name="to-verify-the-availability-of-a-web-service"></a><span data-ttu-id="6372f-130">Til að staðfesta aðgengi að vefþjónustu</span><span class="sxs-lookup"><span data-stu-id="6372f-130">To verify the availability of a web service</span></span>  

1. <span data-ttu-id="6372f-131">Viðeigandi vefslóð er slegin inn í vafrann.</span><span class="sxs-lookup"><span data-stu-id="6372f-131">In your browser, enter the relevant URL.</span></span> <span data-ttu-id="6372f-132">Eftirfarandi tafla lýsir tegundum vefslóða sem hægt er að færa inn fyrir mismunandi vefþjónustugerðir.</span><span class="sxs-lookup"><span data-stu-id="6372f-132">The following table illustrates the types of URLs that you can enter for different web service types.</span></span>  

    > [!div class="mx-tdBreakAll"]
    > |<span data-ttu-id="6372f-133">Tegund</span><span class="sxs-lookup"><span data-stu-id="6372f-133">Type</span></span>|<span data-ttu-id="6372f-134">Málskipan</span><span class="sxs-lookup"><span data-stu-id="6372f-134">Syntax</span></span>|<span data-ttu-id="6372f-135">Dæmi</span><span class="sxs-lookup"><span data-stu-id="6372f-135">Example</span></span>|
    > |----------------|------|-------|
    > |<span data-ttu-id="6372f-136">SOAP</span><span class="sxs-lookup"><span data-stu-id="6372f-136">SOAP</span></span>|`https://api.businesscentral.dynamics.com/*version*/*tenant*/Production/WS/*CompanyName*/*entity*/` |`https://api.businesscentral.dynamics.com/v2.0/7acc9d3d-d354-4616-8bbd-c4fc9f2b15b3/Production/WS/CRONUS%20USA%2C%20Inc./Page/InvoiceDocument`|
    > |<span data-ttu-id="6372f-137">OData V4</span><span class="sxs-lookup"><span data-stu-id="6372f-137">OData V4</span></span>|`https://api.businesscentral.dynamics.com/*version*/*tenant*/Production/ODataV4/Company('*CompanyName*')/*entity*`|`https://api.businesscentral.dynamics.com/v2.0/7acc9d3d-d354-4616-8bbd-c4fc9f2b15b3/Production/ODataV4/Company('CRONUS%20USA%2C%20Inc.')/InvoiceDocument`<br/>    <span data-ttu-id="6372f-138">Í reitnum fyrir heiti fyrirtækis er gerður greinarmunur á há- og lágstöfum.</span><span class="sxs-lookup"><span data-stu-id="6372f-138">The company name is case-sensitive.</span></span>|

2. <span data-ttu-id="6372f-139">Fara skal yfir upplýsingarnar sem birtast í vafranum.</span><span class="sxs-lookup"><span data-stu-id="6372f-139">Review the information that is displayed in the browser.</span></span> <span data-ttu-id="6372f-140">Staðfesta skal að heiti vefþjónustunnar sem var búin til sjáist.</span><span class="sxs-lookup"><span data-stu-id="6372f-140">Verify that you can see the name of the web service that you have created.</span></span>  

<span data-ttu-id="6372f-141">Þegar þú ferð inn á vefþjónustu og vilt skrifa gögn aftur til [!INCLUDE[d365fin](includes/d365fin_md.md)], verður þú að taka fram heiti fyrirtækis.</span><span class="sxs-lookup"><span data-stu-id="6372f-141">When you access a web service, and you want to write data back to [!INCLUDE[d365fin](includes/d365fin_md.md)], you must specify the company name.</span></span> <span data-ttu-id="6372f-142">Hægt er að tilgreina fyrirtækið í URI-slóð eins og sýnt er í dæmunum; annars er hægt að tilgreina fyrirtækið sem hluti af færibreytum fyrirspurnarinnar.</span><span class="sxs-lookup"><span data-stu-id="6372f-142">You can specify the company as part of the URI as shown in the examples; alternatively, specify the company as part of the query parameters.</span></span> <span data-ttu-id="6372f-143">Eftirfarandi vefslóðir vísa t.d. á sama OData vefþjónustuna og eru báðar gildar vefslóðir.</span><span class="sxs-lookup"><span data-stu-id="6372f-143">For example, the following URIs point to the same OData web service and are both valid URIs.</span></span>  

```
https://api.businesscentral.dynamics.com/v1.0/OData/Company('CRONUS International Ltd.')/Customer  
```

```
https://api.businesscentral.dynamics.com/v1.0/OData/Customer?company='CRONUS International Ltd.'  
```

## <a name="see-also"></a><span data-ttu-id="6372f-144">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="6372f-144">See Also</span></span>

[<span data-ttu-id="6372f-145">Stjórnun</span><span class="sxs-lookup"><span data-stu-id="6372f-145">Administration</span></span>](admin-setup-and-administration.md)  
[<span data-ttu-id="6372f-146">Vefþjónustur Business Central fyrir þróunaraðila</span><span class="sxs-lookup"><span data-stu-id="6372f-146">Business Central Web Services for developers</span></span>](/dynamics365/business-central/dev-itpro/webservices/web-services)  
[<span data-ttu-id="6372f-147">OData beiðnitakmörk</span><span class="sxs-lookup"><span data-stu-id="6372f-147">OData request limits</span></span>](/dynamics365/business-central/dev-itpro/administration/operational-limits-online#ODataServices)  
