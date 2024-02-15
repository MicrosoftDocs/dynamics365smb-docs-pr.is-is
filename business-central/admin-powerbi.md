---
title: Kynning á Business Central og Power BI
description: 'Fáðu yfirlit um notkun Power BI til að fá innsýn, viðskiptaupplýsingar og afkastavísi (KPI) úr Business Central gögnum.'
author: jswymer
ms.topic: overview
ms.search.keywords: 'account schedule, analysis, reporting, financial report, business intelligence, KPI'
ms.search.form: '6316, 6317'
ms.reviewer: jswymer
ms.date: 09/28/2023
ms.author: jswymer
ms.custom: bap-template
ms.service: dynamics-365-business-central
---
# Kynning á [!INCLUDE[prod_short](includes/prod_short.md)] og Power BI

[!INCLUDE[azure-ad-to-microsoft-entra-id](~/../shared-content/shared/azure-ad-to-microsoft-entra-id.md)]

Það er auðvelt að fá innsýn í [!INCLUDE[prod_short](includes/prod_short.md)] gögnin þín með [Power BI](https://powerbi.microsoft.com) - gagnabirtingarkerfi frá Microsoft. Power BI sækir [!INCLUDE[prod_short](includes/prod_short.md)] gögn svo hægt sé að búa til stjórnborð og skýrslur út frá þeim gögnum. Power BI býður upp á sveigjanlegt val á skýrslum í [!INCLUDE[prod_short](includes/prod_short.md)], þar sem hægt er að bera saman og sérstilla útlit, og jafnvel sameina gögn úr mismunandi fyrirtækjum í [!INCLUDE[prod_short](includes/prod_short.md)]. Einnig er hægt að taka sumar Power BI skýrslur með í Business Central og skoða þær án þess að fara úr kerfinu. Betra er að skoða flóknari mælaborð á vefsvæðinu Power BI.

![Power BI og Business Central.](media/power-bi-intro.png)

## Kynntu þér það sem hægt er að gera með Power BI og [!INCLUDE[prod_short](includes/prod_short.md)]

Það eru ýmsir eiginleikar fyrir vinnu með [!INCLUDE[prod_short](includes/prod_short.md)] og Power BI. Suma hluti er hægt að gera úr Power BI, á meðan aðrir hlutir eru gerðir úr [!INCLUDE[prod_short](includes/prod_short.md)]. Einnig eru sumir eiginleikar í boði með [!INCLUDE[prod_short](includes/prod_short.md)] á netinu, ekki á staðnum. Eftirfarandi tafla sýnir yfirlit.

|Eiginleiki|Lýsing|Beinlínutengt|Innanhúss|Frekari upplýsingar|
|-------|-----------|--------------|-----------|----------------|
|Skoða [!INCLUDE[prod_short](includes/prod_short.md)] gögn í Power BI|Hægt er að skoða gögn úr [!INCLUDE[prod_short](includes/prod_short.md)] í skýrslum á Power BI. [!INCLUDE[prod_short](includes/prod_short.md)] á netinu inniheldur nokkrar fyrirframskilgreindar Power BI skýrslur. Eða fyrirtækið kann að hafa gert einhverjar sérsniðnar skýrslur fyrir þig.|![Vinnur á netinu.](media/check.png)|![Vinnur á staðnum](media/check.png)|[Hér...](across-working-with-business-central-in-powerbi.md)|
|Skoðaðu Power BI-skýrslur í [!INCLUDE[prod_short](includes/prod_short.md)] -biðlaranum.| Power BI skýrslur sem birta [!INCLUDE[prod_short](includes/prod_short.md)] gögn er hægt að fella beint inn í hluta [!INCLUDE[prod_short](includes/prod_short.md)] síðna. Hægt er að skipta hlutanum til að birta allar skýrslur sem þú hefur aðgang að. |![vinnur á netinu.](media/check.png)|![Vinnur á staðnum](media/check.png)<sup>[*](#onprem)</sup>|[Hér...](across-working-with-powerbi.md).|
|Stofna skýrslur og mælaborð í Power BI sem birta [!INCLUDE[prod_short](includes/prod_short.md)]-gögn.|Notaðu Power BI Desktop til að búa til þínar eigin skýrslur og mælaborð. Hægt er að birta skýrslurnar á eigin Power BI-þjónustu eða deila þeim með öðrum innan fyrirtækisins.|![Vinnur á netinu.](media/check.png)|![vinnur á staðnum](media/check.png)|[Hér...](across-how-use-financials-data-source-powerbi.md)|
|[!INCLUDE[prod_short](includes/prod_short.md)] forrit í Power BI| [!INCLUDE[prod_short](includes/prod_short.md)] gefur út þrjú forrit fyrir Power BI á Microsoft AppSource. Þessi forrit búa til ítarlegar skýrslur og mælaborð í Power BI þjónustunni til að skoða [!INCLUDE[prod_short](includes/prod_short.md)] -gögn. Tiltæk forrit eru meðal annars: <ul><li>[!INCLUDE [prod_long](includes/prod_long.md)] - CRM </li><li>[!INCLUDE [prod_long](includes/prod_long.md)] - Finance </li><li>[!INCLUDE [prod_long](includes/prod_long.md)] - Sales </li></ul>  |![Vinnur á netinu.](media/check.png)||[Hér...](across-powerbi-business-central-apps.md)|
|Vinna með [!INCLUDE [prod_short](includes/prod_short.md)] gögn í gagnaskemmum og gagnaflæðum|Frá og með júlí 2022 er hægt að nota [!INCLUDE [prod_short](includes/prod_short.md)] tengilinn í Power Query Online á gagnaflæði sem deilt er á milli mismunandi skýrslna og stjórnborða.|![vinnur á netinu.](media/check.png)||[Hér...](across-powerbi-business-central-apps.md)|

<a name="onprem"><sup>*</sup></a> Þessi eiginleiki krefst skráðs forrits fyrir Business Central í Microsoft Azure. Nánari upplýsingar er að finna  [í skráningu fyrirtækja miðsvæðis innanhúss í  Microsoft Entra  Kenni fyrir samþætta við aðra þjónustu](/dynamics365/business-central/dev-itpro/administration/register-app-azure).

## Búðu þig undir að nota Power BI

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

## Rekja fyrirtækið afkastavísa með  Power BI  metrics

Ef þú notar  Power BI  á  [!INCLUDE[prod_short](includes/prod_short.md)]  gögn er auðvelt að rekja afkastavísa eða mælingar sem eru mikilvægar þér. 

Með metrics í  Power BI er hægt að krulli inn í eigin mælikvarða og fylgjast með þeim miðað við Lykilmarkmið fyrirtækja, í einni rúðu. Þessi eiginleiki eykur gögn Menning með því að efla ábyrgðarhæfni, jöfnun og sýnileika fyrir teyma og frumkvæði innan stofnana. 

Fylgdu þessu fjögurra þrepa ferli til að setja upp  Power BI  mælingar:

1. Stofna árangursmat í  Power BI  þjónustunni. Frekari upplýsingar á  [Stofna árangursmat í Power BI](/power-bi/create-reports/service-goals-create).  
2. Bættu við þeim  _mælistika_  sem þú vilt rekja með því að tengjast skýrslunni þinni  Power BI  í Telemetry. Frekari upplýsingar í  [Create tengdir metrics](/power-bi/create-reports/service-goals-create-connected).  
3. Til að bæta við alvilja eru skilgreindar stöðureglur fyrir mælifræði. Frekari upplýsingar í  [stofna reglur um sjálfvirka stöðu fyrir metrics](/power-bi/create-reports/service-metrics-status-rules).  

    Þetta skref gerir stöðuuppfærslur sjálfvirkt á grundvelli reglna sem stjórna þeirri mælingu. Reglur kalla á breytingar sem byggjast á gildi, hlutfall markmet, skilyrði dagsetningar eða sambland af þremur, sem gerir reglurnar eins fjölhalla og mögulegt er. Fyrir tengda mælikvarða eru þessar stöður reglur endurnýjaðar í hvert skipti sem gögn í árangursmati eru endurnýjuð.
4. Að lokum fylgja Mælikvarðar til að fá viðvaranir í teymum eða með tölvupósti. Lærðu meira að  [fylgja mælifræðifræðunum þínum](/power-bi/create-reports/service-metrics-follow).  

Frekari upplýsingar um  Power BI  metrics at  [byrja við metrics í Power BI](/power-bi/create-reports/service-goals-introduction).

> [!NOTE]
> Byrjað er með Business Miðbær 2023 út Wave 2, það er hægt að ívefja árangursmati frá  Power BI  metrics í [!INCLUDE[prod_short](includes/prod_short.md)].

## Næstu skref

- Ef þú ert admin sem þarf að setja upp  Power BI  í  [!INCLUDE[prod_short](includes/prod_short.md)], Farðu þá að  [gera  Power BI  samþættingu](admin-powerbi-setup.md).
- Ef  Power BI  hefur þegar verið sett upp og á að reyna aðgerðirnar er farið í að  [vinna með  Power BI  skýrslur í viðskiptamiðinu](across-working-with-powerbi.md).

## Sjá einnig .

[Viðskiptaupplýsingar](bi.md)  
[Setja upp [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Nota [!INCLUDE[prod_short](includes/prod_short.md)] sem Power BI gagnaveitu](across-how-use-financials-data-source-powerbi.md)  
[Nota [!INCLUDE[prod_short](includes/prod_short.md)] sem Power Apps gagnaveitu](across-how-use-financials-data-source-powerapps.md)  
[Nota [!INCLUDE[prod_short](includes/prod_short.md)] í Power Automate](across-how-use-financials-data-source-flow.md)  
[Power BI fylgiskjöl](/power-bi/)  
[Hvað er Power BI?](/power-bi/fundamentals/power-bi-overview)  
[Stutt leiðbeining: Tengjast við gögn í Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data)  
[Kynning á gagnaskemmum](/power-bi/transform-model/datamarts/datamarts-overview)  
[Kynning á gagnaflæðum og gagnaundirbúningur sjálfsafgreiðslu](/power-bi/transform-model/dataflows/dataflows-introduction-self-service)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
