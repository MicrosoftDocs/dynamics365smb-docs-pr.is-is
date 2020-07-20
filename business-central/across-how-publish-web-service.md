---
title: Sýna hluti sem vefþjónustu | Microsoft Docs
description: Birta hluti sem vefþjónustu til að þeir séu undir eins í boði á Business Central.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.search.keywords: ''
ms.date: 05/19/2020
ms.author: edupont
ms.openlocfilehash: 9650539c44a464aab238914ca5d3d65cb8b5c0b8
ms.sourcegitcommit: 3e9c89f90db5eaed599630299353300621fe4007
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/01/2020
ms.locfileid: "3528186"
---
# <a name="publish-a-web-service"></a>Birta vefþjónustu

Vefþjónustur eru létt leið til að gera virkni forrita aðgengilega ýmsum utanaðkomandi kerfum og notendum. [!INCLUDE[d365fin](includes/d365fin_md.md)] inniheldur fjölda hluta sem eru sýndir sem vefþjónusta að sjálfgefnu vegna samþættingu við Microsoft þjónustu, en þú getur einnig bætt við annarri vefþjónustu.  

Þú setur upp vefþjónustu í [!INCLUDE[d365fin](includes/d365fin_md.md)] biðlaranum. Þá verður að gefa vefþjónustuna út til að hún geti tekið við þjónustubeiðnum á netinu. Notendur geta fundið vefþjónustu með því að beina vafra að staðsetningu vefþjóns og biðja um lista yfir þjónustu í boði. Þegar gefa á út vefþjónustu verður hún samstundis virk á netinu fyrir sannvottaða notendur. Allir heimilaðir notendur geta opnað lýsigögn fyrir vefþjónustu, en aðeins notendur með nægilegar heimildir geta opnað raungögn.

## <a name="creating-and-publishing-a-web-service"></a>Vefþjónusta stofnuð og gefin út

Eftirfarandi skref skýra hvernig vefþjónusta er búin til og gefin út.  

### <a name="to-create-and-publish-a-web-service"></a>Til að stofna og gefa út vefþjónustu  

1. Veldu táknið ![ljósapera sem opnar eiginleikan „Viðmótsleit“](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera"), sláðu inn **vefþjónusta** og veldu síðan tengda tengilinn.  
2. Á síðunni **Vefþjónusta** veljið **Nýtt**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    > [!NOTE]  
    > **Kótaeining** og **Síða** eru gildar tegundir fyrir SOAP-vefþjónustu. **Síða** og **Fyrirspurn** eru gildar gerðir fyrir OData-vefþjónustu.  
    > Ef gagnagrunnurinn inniheldur mörg fyrirtæki er hægt að velja Kenni hlutar sem á aðeins við eitt af fyrirtækjunum.  
    > Ef heiti þjónustunnar sýnilegt notendum vefþjónustunnar og það gegnir mikilvægu hlutverki í að auðkenna og þekkja vefþjónustuna. Því skaltu gefa henni merkingarbært heiti.

3. Veldu gátreitinn í dálkinum **Útgefið**.  

Þegar vefþjónusta er gefin út sjást þær vefslóðir sem voru myndaðar fyrir hana í reitunum **OData-vefslóð** og **SOAP-vefslóð**. Hægt er að prófa vefþjónustuna strax með því að velja tengla í reitunum **OData-vefslóð** og **SOAP-vefslóð**. Einnig er hægt að afrita gildið í reitnum og vista það til notkunar síðar.  

> [!NOTE]
> Ef hlutirnir sem þú hefur birt sem vefþjónustur eiga ekki að vera aðgengilegir frá [!INCLUDE[prodshort](includes/prodshort.md)] online verður þú að merkja aðferðirnar í kóðanum sem `[Scope('OnPrem')]`. Frekari upplýsingar má sjá í [Umfangseigind](/dynamics365/business-central/dev-itpro/developer/methods/devenv-scope-attribute).

Eftir að þú birtir vefþjónustu, hafa ytri aðilar aðgang að henni. Hægt er að staðfesta að vefþjónustan sé tiltæk með því að nota vafra eða með því að velja tengilinn í reitunum **OData-vefslóð** og **SOAP-vefslóð** á síðunni **Vefþjónusta**. Eftirfarandi ferli sýnir hvernig hægt er að staðfesta aðgengi að vefþjónustunni fyrir notkun síðar.  

### <a name="to-verify-the-availability-of-a-web-service"></a>Til að staðfesta aðgengi að vefþjónustu  

1. Viðeigandi vefslóð er slegin inn í vafrann. Eftirfarandi tafla lýsir tegundum vefslóða sem hægt er að færa inn fyrir mismunandi vefþjónustugerðir.  

    > [!div class="mx-tdBreakAll"]
    > |Tegund|Málskipan|Dæmi|
    > |----------------|------|-------|
    > |SOAP|`https://api.businesscentral.dynamics.com/*version*/*tenant*/Production/WS/*CompanyName*/*entity*/` |`https://api.businesscentral.dynamics.com/v2.0/7acc9d3d-d354-4616-8bbd-c4fc9f2b15b3/Production/WS/CRONUS%20USA%2C%20Inc./Page/InvoiceDocument`|
    > |OData V4|`https://api.businesscentral.dynamics.com/*version*/*tenant*/Production/ODataV4/Company('*CompanyName*')/*entity*`|`https://api.businesscentral.dynamics.com/v2.0/7acc9d3d-d354-4616-8bbd-c4fc9f2b15b3/Production/ODataV4/Company('CRONUS%20USA%2C%20Inc.')/InvoiceDocument`<br/>    Í reitnum fyrir heiti fyrirtækis er gerður greinarmunur á há- og lágstöfum.|

2. Fara skal yfir upplýsingarnar sem birtast í vafranum. Staðfesta skal að heiti vefþjónustunnar sem var búin til sjáist.  

Þegar þú ferð inn á vefþjónustu og vilt skrifa gögn aftur til [!INCLUDE[d365fin](includes/d365fin_md.md)], verður þú að taka fram heiti fyrirtækis. Hægt er að tilgreina fyrirtækið í URI-slóð eins og sýnt er í dæmunum eða tilgreina það í færibreytum fyrirspurnarinnar. Eftirfarandi vefslóðir vísa t.d. á sama OData vefþjónustuna og eru báðar gildar vefslóðir.  

```
https://api.businesscentral.dynamics.com/v1.0/OData/Company('CRONUS International Ltd.')/Customer  
```

```
https://api.businesscentral.dynamics.com/v1.0/OData/Customer?company='CRONUS International Ltd.'  
```

## <a name="see-also"></a>Sjá einnig

[Stjórnun](admin-setup-and-administration.md)  
[Vefþjónustur Business Central fyrir þróunaraðila](/dynamics365/business-central/dev-itpro/webservices/web-services)  
[OData beiðnitakmörk](/dynamics365/business-central/dev-itpro/administration/operational-limits-online#ODataServices)  
