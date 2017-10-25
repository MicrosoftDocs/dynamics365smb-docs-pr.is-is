---
title: "Sýna hluti sem vefþjónustu | Microsoft Docs"
description: "Birtu [!INCLUDE[d365fin](includes/d365fin_md.md)] hluti sem vefþjónustu, þeir undir eins í boði á dreifikerfinu."
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
ms.openlocfilehash: 278515fc479a72957fb52dad71ce2f98d354ee32
ms.contentlocale: is-is
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-publish-a-web-service"></a><span data-ttu-id="15c21-103">Hvernig á að: Birta vefþjónustu</span><span class="sxs-lookup"><span data-stu-id="15c21-103">How to: Publish a Web Service</span></span>
<span data-ttu-id="15c21-104">Vefþjónustur eru létt leið til að gera virkni forrita aðgengilega ýmsum utanaðkomandi kerfum og notendum.</span><span class="sxs-lookup"><span data-stu-id="15c21-104">Web services are a lightweight way to make application functionality available to a variety of external systems and users.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="15c21-105"> inniheldur fjölda hluta sem eru sýndir sem vefþjónusta að sjálfgefnu vegna samþættingu við Microsoft þjónustu, en þú getur einnig bætt við annarri vefþjónustu.</span><span class="sxs-lookup"><span data-stu-id="15c21-105"> includes an number of objects that are exposed as web services by default due to integration with other Microsoft services, but you can also add other web services.</span></span>  

<span data-ttu-id="15c21-106">Hægt er að setja upp vefþjónustu í Windows-biðlaranum eða í vefbiðlaranum.</span><span class="sxs-lookup"><span data-stu-id="15c21-106">You can set up a web service in the Windows client or in the Web client.</span></span> <span data-ttu-id="15c21-107">Þá verður að gefa vefþjónustuna út til að hún geti tekið við þjónustubeiðnum á netinu.</span><span class="sxs-lookup"><span data-stu-id="15c21-107">You must then publish the web service so that it is available to service requests over the network.</span></span> <span data-ttu-id="15c21-108">Notendur geta fundið vefþjónustu með því að beina vafra að staðsetningu vefþjóns og biðja um lista yfir þjónustu í boði.</span><span class="sxs-lookup"><span data-stu-id="15c21-108">Users can discover web services by pointing a browser at the server location and requesting a list of available services.</span></span> <span data-ttu-id="15c21-109">Þegar gefa á út vefþjónustu verður hún samstundis virk á netinu fyrir sannvottaða notendur.</span><span class="sxs-lookup"><span data-stu-id="15c21-109">When you publish a web service, it is immediately available over the network for authenticated users.</span></span> <span data-ttu-id="15c21-110">Allir heimilaðir notendur geta opnað lýsigögn fyrir vefþjónustu, en aðeins notendur með nægilegar heimildir geta opnað raungögn.</span><span class="sxs-lookup"><span data-stu-id="15c21-110">All authorized users can access metadata for web services, but only users who have sufficient permissions can access actual data.</span></span>

## <a name="creating-and-publishing-a-web-service"></a><span data-ttu-id="15c21-111">Vefþjónusta stofnuð og gefin út</span><span class="sxs-lookup"><span data-stu-id="15c21-111">Creating and Publishing a Web Service</span></span>  
 <span data-ttu-id="15c21-112">Eftirfarandi skref skýra hvernig vefþjónusta er búin til og gefin út.</span><span class="sxs-lookup"><span data-stu-id="15c21-112">The following steps explain how to create and publish a web service.</span></span>  

#### <a name="to-create-and-publish-a-web-service"></a><span data-ttu-id="15c21-113">Til að stofna og gefa út vefþjónustu</span><span class="sxs-lookup"><span data-stu-id="15c21-113">To create and publish a web service</span></span>  

1.  <span data-ttu-id="15c21-114">Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Vefþjónusta** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="15c21-114">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Web Services**, and then choose the related link.</span></span>  

2.  <span data-ttu-id="15c21-115">Á síðunni **Vefþjónusta** skal velja **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="15c21-115">In the **Web Services** page, choose **New**.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    > [!NOTE]  
    >  <span data-ttu-id="15c21-116">**Kótaeining** og **Síða** eru gildar tegundir fyrir SOAP-vefþjónustu.</span><span class="sxs-lookup"><span data-stu-id="15c21-116">**Codeunit** and **Page** are valid types for SOAP web services.</span></span> <span data-ttu-id="15c21-117">**Síða** og **Fyrirspurn** eru gildar gerðir fyrir OData-vefþjónustu.</span><span class="sxs-lookup"><span data-stu-id="15c21-117">**Page** and **Query** are valid types for OData web services.</span></span>  
    <span data-ttu-id="15c21-118">Ef gagnagrunnurinn inniheldur mörg fyrirtæki er hægt að velja Kenni hlutar sem á aðeins við eitt af fyrirtækjunum.</span><span class="sxs-lookup"><span data-stu-id="15c21-118">Also, if the database contains multiple companies, you can choose an object ID that is specific to one of the companies.</span></span>  
    <span data-ttu-id="15c21-119">Ef heiti þjónustunnar sýnilegt notendum vefþjónustunnar og það gegnir mikilvægu hlutverki í að auðkenna og þekkja vefþjónustuna. Því skaltu gefa henni merkingarbært heiti.</span><span class="sxs-lookup"><span data-stu-id="15c21-119">Finally, the service name is visible to consumers of your web service and is the basis for identifying and distinguishing web services, so you should make the name meaningful.</span></span>

3.  <span data-ttu-id="15c21-120">Veldu gátreitinn í dálkinum **Útgefið**.</span><span class="sxs-lookup"><span data-stu-id="15c21-120">Select the check box in the **Published** column.</span></span>  

     <span data-ttu-id="15c21-121">Þegar vefþjónusta er gefin út sjást þær vefslóðir sem voru myndaðar fyrir hana í reitunum **OData-vefslóð** og **SOAP-vefslóð**.</span><span class="sxs-lookup"><span data-stu-id="15c21-121">When you publish the web service, in the **OData URL** and **SOAP URL** fields, you can see the URLs that are generated for the web service.</span></span> <span data-ttu-id="15c21-122">Hægt er að prófa vefþjónustuna strax með því að velja tengla í reitunum **OData-vefslóð** og **SOAP-vefslóð**.</span><span class="sxs-lookup"><span data-stu-id="15c21-122">You can test the web service immediately by choosing the links in the **OData URL** and **SOAP URL** fields.</span></span> <span data-ttu-id="15c21-123">Einnig er hægt að afrita gildið í reitnum og vista það til notkunar síðar.</span><span class="sxs-lookup"><span data-stu-id="15c21-123">Optionally, you can copy the value of the field and save it for later use.</span></span>  

<span data-ttu-id="15c21-124">Eftir að þú birtir vefþjónustu, hafa ytri aðilar aðgang að henni.</span><span class="sxs-lookup"><span data-stu-id="15c21-124">After you publish a web service, it is available to external parties.</span></span> <span data-ttu-id="15c21-125">Hægt er að staðfesta að vefþjónustan sé tiltæk með því að nota vafra eða með því að velja tengilinn í reitunum **OData-vefslóð** og **SOAP-vefslóð** í glugganum **Vefþjónusta**.</span><span class="sxs-lookup"><span data-stu-id="15c21-125">You can verify the availability of that web service by using a browser, or you can choose the link in the **OData URL** and **SOAP URL** fields in the **Web Services** window.</span></span> <span data-ttu-id="15c21-126">Eftirfarandi ferli sýnir hvernig hægt er að staðfesta aðgengi að vefþjónustunni fyrir notkun síðar.</span><span class="sxs-lookup"><span data-stu-id="15c21-126">The following procedure illustrates how you can verify the availability of the web service for later use.</span></span>  

#### <a name="to-verify-the-availability-of-a-web-service"></a><span data-ttu-id="15c21-127">Til að staðfesta aðgengi að vefþjónustu</span><span class="sxs-lookup"><span data-stu-id="15c21-127">To verify the availability of a web service</span></span>  

1.  <span data-ttu-id="15c21-128">Viðeigandi vefslóð er slegin inn í vafrann.</span><span class="sxs-lookup"><span data-stu-id="15c21-128">In your browser, enter the relevant URL.</span></span> <span data-ttu-id="15c21-129">Eftirfarandi tafla lýsir tegundum vefslóða sem hægt er að færa inn.</span><span class="sxs-lookup"><span data-stu-id="15c21-129">The following table illustrates the types of URLs that you can enter.</span></span> <span data-ttu-id="15c21-130">Fyrir SOAP vefþjónustur skal nota eftirfarandi sniðmát fyrir þína vefslóð.</span><span class="sxs-lookup"><span data-stu-id="15c21-130">For SOAP web services, use the following format for your URI.</span></span>  

    <table>
    <tr>
    <th><span data-ttu-id="15c21-131">Tegund vefþjónustu</span><span class="sxs-lookup"><span data-stu-id="15c21-131">Web service type</span></span></th>
    <th><span data-ttu-id="15c21-132">Málskipan</span><span class="sxs-lookup"><span data-stu-id="15c21-132">Syntax</span></span></th>
    <th><span data-ttu-id="15c21-133">Dæmi</span><span class="sxs-lookup"><span data-stu-id="15c21-133">Example</span></span></th>
    </tr>
    <tr>
    <td><span data-ttu-id="15c21-134">SOAP</span><span class="sxs-lookup"><span data-stu-id="15c21-134">SOAP</span></span></td>
    <td><span data-ttu-id="15c21-135">https://*Server*:*SOAPWebServicePort*/*ServerInstance*/WS/*CompanyName*/salesDocuments/</span><span class="sxs-lookup"><span data-stu-id="15c21-135">https://*Server*:*SOAPWebServicePort*/*ServerInstance*/WS/*CompanyName*/salesDocuments/</span></span></td>
    <td><span data-ttu-id="15c21-136">https://mycompany.financials.dynamics.com:7047/MS/WS/MyCompany/Page/salesDocuments?tenant=mycompany.financials.dynamics.com</span><span class="sxs-lookup"><span data-stu-id="15c21-136">https://mycompany.financials.dynamics.com:7047/MS/WS/MyCompany/Page/salesDocuments?tenant=mycompany.financials.dynamics.com</span></span></td>
    </tr>
    <tr>
    <td><span data-ttu-id="15c21-137">OData</span><span class="sxs-lookup"><span data-stu-id="15c21-137">OData</span></span></td>
    <td><span data-ttu-id="15c21-138">https://*Server*:*ODataWebServicePort*/*ServerInstance*/OData/Company('*CompanyName*')</span><span class="sxs-lookup"><span data-stu-id="15c21-138">https://*Server*:*ODataWebServicePort*/*ServerInstance*/OData/Company('*CompanyName*')</span></span></td>
    <td><span data-ttu-id="15c21-139">https://MyCompany.financials.dynamics.com:7048/MS/OData/Company('MyCompany')/salesDocuments?tenant=MyCompany.financials.dynamics.com</span><span class="sxs-lookup"><span data-stu-id="15c21-139">https://MyCompany.financials.dynamics.com:7048/MS/OData/Company('MyCompany')/salesDocuments?tenant=MyCompany.financials.dynamics.com</span></span>

         The company name is case-sensitive.</td>
    </tr>
    </table>

2.  <span data-ttu-id="15c21-140">Fara skal yfir upplýsingarnar sem birtast í vafranum.</span><span class="sxs-lookup"><span data-stu-id="15c21-140">Review the information that is displayed in the browser.</span></span> <span data-ttu-id="15c21-141">Staðfesta skal að heiti vefþjónustunnar sem var búin til sjáist.</span><span class="sxs-lookup"><span data-stu-id="15c21-141">Verify that you can see the name of the web service that you have created.</span></span>  

 <span data-ttu-id="15c21-142">Þegar þú ferð inn á vefþjónustu og vilt skrifa gögn aftur til [!INCLUDE[d365fin](includes/d365fin_md.md)], verður þú að taka fram heiti fyrirtækis.</span><span class="sxs-lookup"><span data-stu-id="15c21-142">When you access a web service, and you want to write data back to [!INCLUDE[d365fin](includes/d365fin_md.md)], you must specify the company name.</span></span> <span data-ttu-id="15c21-143">Hægt er að tilgreina fyrirtækið í URI-slóð eins og sýnt er í dæmunum eða tilgreina það í færibreytum fyrirspurnarinnar.</span><span class="sxs-lookup"><span data-stu-id="15c21-143">You can specify the company as part of the URI as shown in the examples, or you can specify the company as part of the query parameters.</span></span> <span data-ttu-id="15c21-144">Eftirfarandi vefslóðir vísa t.d. á sama OData vefþjónustuna og eru báðar gildar vefslóðir.</span><span class="sxs-lookup"><span data-stu-id="15c21-144">For example, the following URIs point to the same OData web service and are both valid URIs.</span></span>  

```  
https://localhost:7048/server/OData/Company('CRONUS International Ltd.')/Customer  
```  

```  
https://localhost:7048/server/OData/Customer?company='CRONUS International Ltd.'  
```  

## <a name="see-also"></a><span data-ttu-id="15c21-145">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="15c21-145">See Also</span></span>  
[<span data-ttu-id="15c21-146">Uppsetning og stjórnun í Dynamics 365 for Financials</span><span class="sxs-lookup"><span data-stu-id="15c21-146">Setup and Administration in Dynamics 365 for Financials</span></span>](admin-setup-and-administration.md)  

