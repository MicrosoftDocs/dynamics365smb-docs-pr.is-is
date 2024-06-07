---
title: Sýna hluti sem vefþjónustu
description: Birta hluti sem vefþjónustu til að þeir séu undir eins í boði á Business Central.
author: brentholtorf
ms.topic: conceptual
ms.search.form: 810
ms.date: 04/01/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="publish-a-web-service"></a>Birta vefþjónustu

Vefþjónustur eru létt leið til að gera virkni forrita aðgengilega ýmsum utanaðkomandi kerfum og notendum. Sjálfgefið er að [!INCLUDE[prod_short](includes/prod_short.md)] gefi upp nokkra hluti sem vefþjónustur fyrir betri samþættingu við aðra Microsoft-þjónustu. Þú getur bætt öðrum vefþjónustum við eftir því hvað reksturinn þarfnast.  

Settu upp vefþjónustu í [!INCLUDE[prod_short](includes/prod_short.md)] og birtu síðan vefþjónustuna þannig að hún sé aðgengileg sannvottuðu notendum. Allir heimilaðir notendur geta opnað lýsigögn fyrir vefþjónustu, en aðeins notendur með nægilegar heimildir geta opnað raungögn.  

## <a name="creating-and-publishing-a-web-service"></a>Vefþjónusta stofnuð og gefin út

Eftirfarandi skref skýra hvernig vefþjónusta er búin til og gefin út.  

### <a name="to-create-and-publish-a-web-service"></a>Til að stofna og gefa út vefþjónustu

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, færa inn **Netþjónusta** og velja síðan viðkomandi tengil.  
2. Á síðunni **Vefþjónusta** veljið **Nýtt**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    > [!NOTE]  
    > **Kótaeining** og **Síða** eru gildar tegundir fyrir SOAP-vefþjónustu. **Síða** og **Fyrirspurn** eru gildar gerðir fyrir OData-vefþjónustu. Frá og með útgáfu 16.3, er **Codeunit** einnig gild gerð fyrir OData v4 vefþjónustur, en þá er engin vefslóð sýnd í notandaviðmótinu. Ef gagnagrunnurinn inniheldur mörg fyrirtæki er hægt að velja Kenni hlutar sem á aðeins við eitt af fyrirtækjunum.  
    > Ef heiti þjónustunnar sýnilegt notendum vefþjónustunnar og það gegnir mikilvægu hlutverki í að auðkenna og þekkja vefþjónustuna. Því skaltu gefa henni merkingarbært heiti.

3. Veldu gátreitinn í dálkinum **Útgefið**.  

Þegar vefþjónusta er gefin út sýna reitirnir **OData-vefslóð** og **SOAP-vefslóð** nýju vefslóðirnar. Hins vegar, fyrir codeunit sem gefið er upp sem OData v4 óbundnar aðgerðir, eru reitir vefslóða ekki sýndir.  

Hægt er að prófa vefþjónustuna strax með því að velja tengla í reitunum **OData-vefslóð** og **SOAP-vefslóð**. Einnig er hægt að afrita gildið í reitnum og vista það til síðari nota. Til að prófa codeunit sem gefið er upp sem OData v4 óbundnar aðgerðir, skal fylgja leiðbeiningunum í hlutanum [Sannprófa aðgengileika vefþjónustu](/dynamics365/business-central/dev-itpro/developer/devenv-creating-and-interacting-with-odatav4-unbound-action#verifying-web-service-availability) í efni þróunaraðila.

> [!NOTE]
> Ef hlutirnir sem þú hefur birt sem vefþjónustur eiga ekki að vera aðgengilegir frá [!INCLUDE[prod_short](includes/prod_short.md)] online verður þú að merkja aðferðirnar í kóðanum sem `[Scope('OnPrem')]`. Frekari upplýsingar má sjá í [Umfangseigind](/dynamics365/business-central/dev-itpro/developer/methods/devenv-scope-attribute).

Eftir að þú birtir vefþjónustu, hafa ytri aðilar aðgang að henni. Hægt er að staðfesta að vefþjónustan sé tiltæk með því að nota vafra eða með því að velja tengilinn í reitunum **OData-vefslóð** og **SOAP-vefslóð** á síðunni **Vefþjónusta**. Eftirfarandi ferli sýnir hvernig hægt er að staðfesta aðgengi að vefþjónustunni fyrir notkun síðar.  

### <a name="to-verify-the-availability-of-a-web-service"></a>Til að staðfesta aðgengi að vefþjónustu

1. Viðeigandi vefslóð er slegin inn í vafrann. Eftirfarandi tafla lýsir tegundum vefslóða sem hægt er að færa inn fyrir mismunandi vefþjónustugerðir.  

    > [!div class="mx-tdBreakAll"]
    > |Tegund|Málskipan|Dæmi|
    > |----------------|------|-------|
    > |SOAP|`https://api.businesscentral.dynamics.com/*version*/*tenant*/Production/WS/*CompanyName*/*entity*/` |`https://api.businesscentral.dynamics.com/v2.0/7acc9d3d-d354-4616-8bbd-c4fc9f2b15b3/Production/WS/CRONUS%20USA%2C%20Inc./Page/InvoiceDocument`|
    > |OData V4|`https://api.businesscentral.dynamics.com/*version*/*tenant*/Production/ODataV4/Company('*CompanyName*')/*entity*`|`https://api.businesscentral.dynamics.com/v2.0/7acc9d3d-d354-4616-8bbd-c4fc9f2b15b3/Production/ODataV4/Company('CRONUS%20USA%2C%20Inc.')/InvoiceDocument`<br/>    Í reitnum fyrir heiti fyrirtækis er gerður greinarmunur á há- og lágstöfum.|

2. Fara skal yfir upplýsingarnar sem birtast í vafranum. Staðfesta skal að heiti vefþjónustunnar sem var búin til sjáist.  

Þegar þú ferð inn á vefþjónustu og vilt skrifa gögn aftur til [!INCLUDE[prod_short](includes/prod_short.md)], verður þú að taka fram heiti fyrirtækis. Hægt er að tilgreina fyrirtækið í URI-slóð eins og sýnt er í dæmunum; annars er hægt að tilgreina fyrirtækið sem hluti af færibreytum fyrirspurnarinnar. Eftirfarandi vefslóðir vísa t.d. á sama OData vefþjónustuna og eru báðar gildar vefslóðir.  

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


[!INCLUDE[footer-include](includes/footer-banner.md)]
