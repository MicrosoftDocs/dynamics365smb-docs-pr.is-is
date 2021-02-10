---
title: Kynning á Business Central og Power BI| Microsoft Docs
description: Það er auðvelt að fá innsýn, viðskiptaupplýsingar og afkastavísi (KPI) í Business Central gögnum með Business Central forritunum fyrir Power BI.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: account schedule, analysis, reporting, financial report, business intelligence, KPI
ms.reviewer: edupont
ms.date: 10/01/2020
ms.author: jswymer
ms.openlocfilehash: 51c9e2cd05deba5fd8ace46382ebeb4eb41d13ba
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/17/2020
ms.locfileid: "4753743"
---
# <a name="prod_short-and-power-bi"></a>[!INCLUDE[prod_short](includes/prod_short.md)] og Power BI

Það er auðvelt að fá innsýn í [!INCLUDE[prod_short](includes/prod_short.md)] gögnin þín með [Power BI](https://powerbi.microsoft.com) sjónrænu gagnakerfi frá Microsoft. Power BI sækir [!INCLUDE[prod_short](includes/prod_short.md)] gögn sem gera þér kleift að byggja mælaborð og skýrslur út frá þeim gögnum. Power BI býður upp á sveigjanlegt val á skýrslum í [!INCLUDE[prod_short](includes/prod_short.md)], þar sem hægt er að bera saman og sérstilla útlit, og jafnvel sameina gögn úr mismunandi fyrirtækjum í [!INCLUDE[prod_short](includes/prod_short.md)]. Einnig er hægt að taka sumar Power BI skýrslur með í Business Central og skoða þær án þess að fara úr kerfinu. Betra er að skoða flóknari mælaborð á vefsvæðinu Power BI.

![Power BI og Business Central](media/power-bi-intro.png)


## <a name="what-you-can-do-with-power-bi-and-prod_short"></a>Kynntu þér það sem hægt er að gera með Power BI og [!INCLUDE[prod_short](includes/prod_short.md)]

Það eru ýmsir eiginleikar fyrir vinnu með [!INCLUDE[prod_short](includes/prod_short.md)] og Power BI. Suma hluti er hægt að gera úr Power BI, á meðan aðrir hlutir eru gerðir úr [!INCLUDE[prod_short](includes/prod_short.md)]. Einnig eru sumir eiginleikar í boði með [!INCLUDE[prod_short](includes/prod_short.md)] á netinu, ekki á staðnum. Eftirfarandi tafla sýnir yfirlit.

|Sérkenni|Description|Beinlínutengt|Á staðnum|Meiri upplýsingar|
|-------|-----------|--------------|-----------|----------------|
|Skoða [!INCLUDE[prod_short](includes/prod_short.md)] gögn í Power BI|Hægt er að skoða gögn úr [!INCLUDE[prod_short](includes/prod_short.md)] í skýrslum á Power BI. [!INCLUDE[prod_short](includes/prod_short.md)] á netinu inniheldur nokkrar fyrirframskilgreindar Power BI skýrslur. Eða fyrirtækið kann að hafa gert einhverjar sérsniðnar skýrslur fyrir þig.|![Vinna á netinu](media/check.png)|![Vinnur á staðnum](media/check.png)|[Sjá...](across-working-with-powerbi.md)|
|Skoðaðu Power BI-skýrslur í [!INCLUDE[prod_short](includes/prod_short.md)] -biðlaranum.| Power BI skýrslur sem birta [!INCLUDE[prod_short](includes/prod_short.md)] gögn er hægt að fella beint inn í hluta [!INCLUDE[prod_short](includes/prod_short.md)] síðna. Hægt er að skipta hlutanum til að birta allar skýrslur sem þú hefur aðgang að. |![vinnur á netinu](media/check.png)|![Vinnur á staðnum](media/check.png)<sup>[*](#onprem)</sup>|[Sjá...](across-working-with-business-central-in-powerbi.md).|
|Stofna skýrslur og mælaborð í Power BI sem birta [!INCLUDE[prod_short](includes/prod_short.md)]-gögn.|Notaðu Power BI Desktop til að búa til þínar eigin skýrslur og mælaborð. Hægt er að birta skýrslurnar á eigin Power BI-þjónustu eða deila þeim með öðrum innan fyrirtækisins.|![Vinna á netinu](media/check.png)|![vinnur á staðnum](media/check.png)|[Sjá...](across-how-use-financials-data-source-powerbi.md)
|[!INCLUDE[prod_short](includes/prod_short.md)] forrit í Power BI| [!INCLUDE[prod_short](includes/prod_short.md)] gefur út þrjú forrit fyrir Power BI á Microsoft AppSource. Þessi forrit búa til ítarlegar skýrslur og mælaborð í Power BI þjónustunni til að skoða [!INCLUDE[prod_short](includes/prod_short.md)] -gögn. Tiltæk forrit eru meðal annars: <ul><li>[!INCLUDE [prod_long](includes/prod_long.md)] - CRM </li><li>[!INCLUDE [prod_long](includes/prod_long.md)] - Finance </li><li>[!INCLUDE [prod_long](includes/prod_long.md)] - Sales </li></ul>  |![Vinna á netinu](media/check.png)||[Sjá...](across-powerbi-business-central-apps.md)

<a name="onprem"><sup>*</sup></a> Þessi eiginleiki krefst skráðs forrits fyrir Business Central í Microsoft Azure. Frekari upplýsingar er að finna á [Skráning Business Central innanhúss í Azure AD fyrir samþættingu við aðrar þjónustur](/dynamics365/business-central/dev-itpro/administration/register-app-azure).

## <a name="getting-ready-to-use-power-bi"></a>Að undirbúa notkun Power BI

Það þarf að gera nokkra hluti áður en hægt er að byrja að nota Power BI með [!INCLUDE[prod_short](includes/prod_short.md)]. Sum verkin eru yfirleitt unnin af stjórnendum eða ofurnotendum.

1. Ef [!INCLUDE[prod_short](includes/prod_short.md)] er notað innanhúss skal ganga úr skugga um að innleiðingin uppfylli þær kröfur sem gerðar eru til [Setja upp [!INCLUDE[prod_short](includes/prod_short.md)] innanhúss fyrir Power BI samþættingu](admin-powerbi-setup.md#setup). Þetta verk er oftast stjórnunarverk.

2. Birting gagna sem vefþjónusta.

    Kóðaeiningar, síður og fyrirspurnir sem ætlunin er að nota sem gagnagjafa í Power BI-skýrslum verða að vera birtar sem vefþjónustur. Margar vefþjónustur birtast sjálfkrafa. Auðveld leið til að finna vefþjónustu er að leita að *vefþjónustu* í [!INCLUDE[prod_short](includes/prod_short.md)].
    
    Frekari upplýsingar um birtingu vefþjónustu er að finna á [Birta vefþjónustu](across-how-publish-web-service.md).

3. Fá Power BI reikning.

    Til að gera allt sem er með Power BI og [!INCLUDE[prod_short](includes/prod_short.md)], hvort sem þú ert kerfisstjóri eða bara neytandi þarftu Power BI þjónustulykil. Til að fá reikning skaltu fara á [https://powerbi.microsoft.com](https://powerbi.microsoft.com). Til að skrá þig fyrir reikningi skaltu nota vinnunetfang og aðgangsorð þitt. Skráning krefst þess að þú sért með leyfi en í flestum tilvikum ætti þegar að vera til staðar ókeypis leyfi. Frekari upplýsingar er að finna á [Power BI Leyfisveiting](admin-powerbi-setup.md#license).

4. Ef ætlunin er að stofna eigin Power BI-skýrslur skal sækja Power BI Desktop.

    Hægt er að hlaða niður [Power BI Desktop](https://powerbi.microsoft.com/desktop/). Frekari upplýsingar er að finna á [Sækja Power BI Desktop](/power-bi/fundamentals/desktop-get-the-desktop).

## <a name="see-related-training-at-microsoft-learn"></a>Sjá tengda þjálfun á [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)

## <a name="see-also"></a>Sjá einnig

[Power BI fyrir neytendur](/power-bi/consumer/end-user-consumer)  
[„Nýtt útlit“ Power BI þjónustunnar](/power-bi/service-new-look)  
[Stutt leiðbeining: Tengjast við gögn í Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data)  
[Power BI fylgiskjöl](/power-bi/)  
[Viðskiptaupplýsingar](bi.md)  
[Hafist handa](product-get-started.md)  
[Innflutningur viðskiptagagna úr öðrum fjárhagskerfum](across-import-data-configuration-packages.md)  
[Uppsetning [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Nota [!INCLUDE[prod_short](includes/prod_short.md)] sem Power BI gagnaveitu](across-how-use-financials-data-source-powerbi.md)  
[Nota [!INCLUDE[prod_short](includes/prod_short.md)] sem Power Apps gagnaveitu](across-how-use-financials-data-source-powerapps.md)  
[Nota [!INCLUDE[prod_short](includes/prod_short.md)] í Power Automate](across-how-use-financials-data-source-flow.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  
