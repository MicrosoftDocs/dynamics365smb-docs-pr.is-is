---
title: Kynning á Business Central og Power BI| Microsoft Docs
description: Fáðu yfirlit um notkun Power BI til að fá innsýn, viðskiptaupplýsingar og afkastavísi (KPI) úr Business Central gögnum.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: account schedule, analysis, reporting, financial report, business intelligence, KPI
ms.reviewer: edupont
ms.date: 04/01/2021
ms.author: jswymer
ms.openlocfilehash: 3c8ad52667ad8ff0a2cb399ac6354012d7ef9275
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/08/2021
ms.locfileid: "6437913"
---
# <a name="prod_short-and-power-bi"></a>[!INCLUDE[prod_short](includes/prod_short.md)] og Power BI

Það er auðvelt að fá innsýn í [!INCLUDE[prod_short](includes/prod_short.md)] gögnin þín með [Power BI](https://powerbi.microsoft.com) sjónrænu gagnakerfi frá Microsoft. Power BI sækir [!INCLUDE[prod_short](includes/prod_short.md)] gögn sem gera þér kleift að byggja mælaborð og skýrslur út frá þeim gögnum. Power BI býður upp á sveigjanlegt val á skýrslum í [!INCLUDE[prod_short](includes/prod_short.md)], þar sem hægt er að bera saman og sérstilla útlit, og jafnvel sameina gögn úr mismunandi fyrirtækjum í [!INCLUDE[prod_short](includes/prod_short.md)]. Einnig er hægt að taka sumar Power BI skýrslur með í Business Central og skoða þær án þess að fara úr kerfinu. Betra er að skoða flóknari mælaborð á vefsvæðinu Power BI.

![Power BI og Business Central.](media/power-bi-intro.png)

## <a name="what-you-can-do-with-power-bi-and-prod_short"></a>Kynntu þér það sem hægt er að gera með Power BI og [!INCLUDE[prod_short](includes/prod_short.md)]

Það eru ýmsir eiginleikar fyrir vinnu með [!INCLUDE[prod_short](includes/prod_short.md)] og Power BI. Suma hluti er hægt að gera úr Power BI, á meðan aðrir hlutir eru gerðir úr [!INCLUDE[prod_short](includes/prod_short.md)]. Einnig eru sumir eiginleikar í boði með [!INCLUDE[prod_short](includes/prod_short.md)] á netinu, ekki á staðnum. Eftirfarandi tafla sýnir yfirlit.

|Sérkenni|Description|Beinlínutengt|Á staðnum|Meiri upplýsingar|
|-------|-----------|--------------|-----------|----------------|
|Skoða [!INCLUDE[prod_short](includes/prod_short.md)] gögn í Power BI|Hægt er að skoða gögn úr [!INCLUDE[prod_short](includes/prod_short.md)] í skýrslum á Power BI. [!INCLUDE[prod_short](includes/prod_short.md)] á netinu inniheldur nokkrar fyrirframskilgreindar Power BI skýrslur. Eða fyrirtækið kann að hafa gert einhverjar sérsniðnar skýrslur fyrir þig.|![Vinnur á netinu.](media/check.png)|![Vinnur á staðnum](media/check.png)|[Sjá...](across-working-with-business-central-in-powerbi.md)|
|Skoðaðu Power BI-skýrslur í [!INCLUDE[prod_short](includes/prod_short.md)] -biðlaranum.| Power BI skýrslur sem birta [!INCLUDE[prod_short](includes/prod_short.md)] gögn er hægt að fella beint inn í hluta [!INCLUDE[prod_short](includes/prod_short.md)] síðna. Hægt er að skipta hlutanum til að birta allar skýrslur sem þú hefur aðgang að. |![vinnur á netinu.](media/check.png)|![Vinnur á staðnum](media/check.png)<sup>[*](#onprem)</sup>|[Sjá...](across-working-with-powerbi.md).|
|Stofna skýrslur og mælaborð í Power BI sem birta [!INCLUDE[prod_short](includes/prod_short.md)]-gögn.|Notaðu Power BI Desktop til að búa til þínar eigin skýrslur og mælaborð. Hægt er að birta skýrslurnar á eigin Power BI-þjónustu eða deila þeim með öðrum innan fyrirtækisins.|![Vinnur á netinu.](media/check.png)|![vinnur á staðnum](media/check.png)|[Sjá...](across-how-use-financials-data-source-powerbi.md)
|[!INCLUDE[prod_short](includes/prod_short.md)] forrit í Power BI| [!INCLUDE[prod_short](includes/prod_short.md)] gefur út þrjú forrit fyrir Power BI á Microsoft AppSource. Þessi forrit búa til ítarlegar skýrslur og mælaborð í Power BI þjónustunni til að skoða [!INCLUDE[prod_short](includes/prod_short.md)] -gögn. Tiltæk forrit eru meðal annars: <ul><li>[!INCLUDE [prod_long](includes/prod_long.md)] - CRM </li><li>[!INCLUDE [prod_long](includes/prod_long.md)] - Finance </li><li>[!INCLUDE [prod_long](includes/prod_long.md)] - Sales </li></ul>  |![Vinnur á netinu.](media/check.png)||[Sjá...](across-powerbi-business-central-apps.md)

<a name="onprem"><sup>*</sup></a> Þessi eiginleiki krefst skráðs forrits fyrir Business Central í Microsoft Azure. Frekari upplýsingar er að finna á [Skráning Business Central innanhúss í Azure AD fyrir samþættingu við aðrar þjónustur](/dynamics365/business-central/dev-itpro/administration/register-app-azure).

## <a name="getting-ready-to-use-power-bi"></a>Að undirbúa notkun Power BI

Það þarf að gera nokkra hluti áður en hægt er að byrja að nota Power BI með [!INCLUDE[prod_short](includes/prod_short.md)]. <!-- Some of the tasks are typically only done by administrators or super users.--> Verkin fara eftir hlutverki þínu í fyrirtækinu og hvað þú vilt gera við Power BI:

- Sem *viðskiptanotandi* viltu skoða Power BI skýrslur, annaðhvort í Power BI Service eða í Business Central
- Sem *stjórnandi* berðu ábyrgð á stjórnun stillinga sem ná yfir allt fyrirtækið sem stjórna því hvernig Business Central og Power BI vinna.
- Sem *skýrsluhöfundur* viltu búa til sérsniðnar Power BI skýrslur sem þú getur deilt með öðrum notendum.

|Verkefni|Fyrirtækisnotandi|Stjórnandi|Skýrsluhöfundur|Meiri upplýsingar|
|----|-------------|-------------|-----------------------|----------------|
|Fá Power BI reikning.|![enn eitt hakið.](media/check.png)|![þetta er hak](media/check.png)|![aftur hak](media/check.png)|Opnið [https://powerbi.microsoft.com](https://powerbi.microsoft.com). Til að skrá þig fyrir reikningi skaltu nota vinnunetfang og aðgangsorð þitt. <br /><br/>Skráning krefst þess að þú sért með leyfi en í flestum tilvikum ætti þegar að vera til staðar ókeypis leyfi. Frekari upplýsingar er að finna í [Power BI Leyfisveiting](admin-powerbi-setup.md#license).|
|Sækja Power BI Desktop|||![aftur hak.](media/check.png)|Til að fara í niðurhal skal fara í [Power BI Desktop](https://powerbi.microsoft.com/desktop/). Frekari upplýsingar er að finna á [Sækja Power BI Desktop](/power-bi/fundamentals/desktop-get-the-desktop).
|Birta gögn Business Central í Power BI||![þetta er hak.](media/check.png)|![aftur hak](media/check.png)|[Birta gögn í gegnum API-síður eða OData-vefþjónustur](admin-powerbi-setup.md#exposedata)
|Kveikja á samþættingu Power BI<br />(eingöngu á staðnum)||![þetta er hak.](media/check.png)||[Setja upp Business Central á staðnum fyrir Power BI samþættingu](admin-powerbi-setup.md#setup)|


<!--



1. If you're using [!INCLUDE[prod_short](includes/prod_short.md)] on-premises, make sure your deployment meets the requirements outlined in [Set up [!INCLUDE[prod_short](includes/prod_short.md)] on-premises for Power BI integration](admin-powerbi-setup.md#setup). This task is typically an administrative task.

2. Expose Business Central data through API pages or published web services.

    Business Central online automatically included several pages as APIs. For more information, see [Business Central API V2.0](/dynamics365/business-central/dev-itpro/api-reference/v2.0/). Application developers for Business Central online can create custom API pages that you can then consume in reports. For more information, see [Developing a Custom API](/dynamics365/business-central/dev-itpro/developer/devenv-develop-custom-api).

   Codeunit, page, and query objects can be published as OData web services. There are many web services published by default. An easy way to find the web services is to search for *web services* in [!INCLUDE[prod_short](includes/prod_short.md)]. For more information about publishing web services, see [Publish a Web Service](across-how-publish-web-service.md).

3. Get a Power BI account.

   To do anything with Power BI and [!INCLUDE[prod_short](includes/prod_short.md)], whether you're an administrator or just a consumer, you'll need Power BI service account. To get an account, go to [https://powerbi.microsoft.com](https://powerbi.microsoft.com). To sign up for an account, use your work email address and password. Sign-up requires that you have a license, but in most cases you should already have a free license. For more information, see [Power BI Licensing](admin-powerbi-setup.md#license).

4. If you want to create your own Power BI reports, get Power BI Desktop.

   You can download [Power BI Desktop](https://powerbi.microsoft.com/desktop/). For more information, see [Get Power BI Desktop](/power-bi/fundamentals/desktop-get-the-desktop).

-->

## <a name="see-related-training-at-microsoft-learn"></a>Sjá tengda þjálfun á [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)

## <a name="see-also"></a>Sjá einnig

[Power BI fyrir neytendur](/power-bi/consumer/end-user-consumer)  
[„Nýtt útlit“ Power BI þjónustunnar](/power-bi/service-new-look)  
[Stutt leiðbeining: Tengjast við gögn í Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data)  
[Power BI fylgiskjöl](/power-bi/)  
[Viðskiptaupplýsingar](bi.md)  
[Undirbúðu þig fyrir að gera viðskipti](ui-get-ready-business.md)  
[Innflutningur viðskiptagagna úr öðrum fjárhagskerfum](across-import-data-configuration-packages.md)  
[Uppsetning [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Nota [!INCLUDE[prod_short](includes/prod_short.md)] sem Power BI gagnaveitu](across-how-use-financials-data-source-powerbi.md)  
[Nota [!INCLUDE[prod_short](includes/prod_short.md)] sem Power Apps gagnaveitu](across-how-use-financials-data-source-powerapps.md)  
[Nota [!INCLUDE[prod_short](includes/prod_short.md)] í Power Automate](across-how-use-financials-data-source-flow.md)  




[!INCLUDE[footer-include](includes/footer-banner.md)]