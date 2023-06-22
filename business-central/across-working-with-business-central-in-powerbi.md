---
title: Unnið með Business Central Data í Power BI| Microsoft docs
description: 'Það er auðvelt að fá innsýn, viðskiptaupplýsingar og afkastavísi (KPI) í Business Central með Power BI.'
author: jswymer
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'account schedule, analysis, reporting, financial report, business intelligence, KPI'
ms.date: 09/07/2022
ms.author: jswymer
---
# <a name="work-with-include-prodshortincludesprodshortmd-data-in-power-bi" />Vinna með [!INCLUDE [prod_short](includes/prod_short.md)] gögn í Power BI

Í þessari grein lærir þú undirstöðuatriði varðandi vinnu við skýrslur og mælaborð í Power BI sem nota [!INCLUDE [prod_short](includes/prod_short.md)] sem gagnaveitu. Greinin fjallar um suma þætti sem munu hjálpa til við að hefjast handa sem [!INCLUDE[prod_short](includes/prod_short.md)] notandi. Almennar leiðbeiningar og leiðbeiningar um notkun á Power BI er að finna í [Power BI fylgigögnum fyrir neytendur](/power-bi/consumer).

## <a name="get-ready" />Vertu með allt á tæru

Skráðu þig fyrir nýju Power BI þjónustuna. Ef þú hefur ekki þegar skráð þig skaltu fara á [https://powerbi.microsoft.com](https://powerbi.microsoft.com). Þegar þú skráir skaltu nota vinnunetfang og aðgangsorð.

## <a name="get-started" />Hefjast handa

Þegar þú ert með Power BI-reikning geturðu skráð þig inn á [https://powerbi.microsoft.com/](https://powerbi.microsoft.com/).

Power BI þjónustan hýsir allar skýrslur sem eru í boði. Til að sjá skýrslu skal velja **Vinnusvæðið mitt** > **Skýrslur**. Veljið svo skýrsluna sem á að skoða.

Með [!INCLUDE[prod_short](includes/prod_short.md)] á netinu er sjálfkrafa hægt að hafa sjálfgefnar skýrslur á vinnusvæðinu. Ef stofna á eigin skýrslur er hægt að nota Power BI Desktop til að stofna skýrslur og birta þær síðan á eigin vinnusvæði. Frekari upplýsingar er að finna í [Hafist handa með skýrslur í Power BI Desktop til að birta [!INCLUDE [prod_long](includes/prod_long.md)] gögn](across-how-use-financials-data-source-powerbi.md).

[!INCLUDE[note-multicompany-reports](includes/note-multicompany-reports.md)]

Ef þú ert að nota [!INCLUDE[prod_short](includes/prod_short.md)] á staðnum þarftu að byrja frá grunni með því að nota Power BI Desktop. Hægt er að dreifa Power BI skýrslum sem skrám, sem hægt er að hlaða upp.

## <a name="get-the-latest-data" />Fá nýjustu gögnin

Hver Power BI skýrsla byggir á gagnasafni sem fær gögn frá [!INCLUDE[prod_short](includes/prod_short.md)] uppruna. Þú vilt ganga úr skugga um að gögnin í Power BI-skýrslunum séu uppfærð með gögnunum í [!INCLUDE[prod_short](includes/prod_short.md)]. Þetta hugtak er nefnt *uppfærsla*.  Ekki er víst að endurnýjun gerist sjálfkrafa, allt eftir því hvernig fyrirtækið hefur sett upp Power BI. Það eru tvær leiðir til að uppfæra gögn: handvirkt eða með því að tímasetja uppfærslu. Handvirk endurnýjun fer fram eftir þörfum. Áætluð endurnýjun gerir þér kleift að uppfæra sjálfkrafa á skilgreindum tímabilum.

### <a name="refresh-manually" />Uppfæra handvirkt

Í skoðunarrúðunni, undir **Gagnasafn**, skal velja **Fleiri valkostir (...)** við hliðina á gagnasafni og velja svo **Uppfæra núna**.

### <a name="schedule-a-refresh" />Áætla uppfærslu

Í skoðunarrúðunni, undir Gagnasafn, skal velja Fleiri valkostir (...) við hliðina á gagnasafn og velja svo **Uppfæra núna**. Fylltu út upplýsingarnar í **Tímasetja uppfærslu** og veldu **Not**.

Frekari upplýsingar eru í [Grunnstilla uppfærsluáætlun](/power-bi/connect-data/refresh-scheduled-refresh)

## <a name="a-nameuploadaupload-reports-from-files" /><a name="upload"></a>Hlaða upp skýrslum úr skrám

Hægt er að dreifa Power BI skýrslum á meðal notenda sem. pbix-skrám. Ef þú ert með .pbix-skrá er hægt að hlaða skránni upp á vinnusvæði. Til að hlaða upp skýrslu skal gera eftirfarandi:

1. Á nýja vinnusvæðinu skal velja **Sækja gögn**.

2. Í reitnum Skrár skal velja **Sækja**.

3. Veldu **Staðbundin skrá**, farðu þangað sem hún er vistuð og veldu **Opna**.

Frekari upplýsingar er að finna á [Hlaða upp skýrslu á þjónustu](/power-bi/paginated-reports/paginated-reports-quickstart-aw#upload-the-report-to-the-service).

> [!NOTE]
> Til að hlaða upp skýrslu þarftu að hafa [Premium afkastagetu](/power-bi/service-premium-what-is) vinnusvæði. Nánari upplýsingar er að finna í [Stjórnun Premium eiginleika](/power-bi/admin/service-premium-capacity-manage). 

> [!TIP]
> Ef þú notar [!INCLUDE[prod_short](includes/prod_short.md)] á netinu geturðu einnig hlaðið upp skýrslu úr [!INCLUDE[prod_short](includes/prod_short.md)]. Frekari upplýsingar er að finna í [Vinna með Power BI skýrslur í [!INCLUDE [prod_short](includes/prod_short.md)] - Hlaða upp skýrslum](across-working-with-powerbi.md#upload).

## <a name="a-nameshareashare-reports-with-others" /><a name="share"></a>Deila skýrslum með öðrum

Þegar skýrsla er á vinnusvæðinu er hægt að deila henni með öðrum í fyrirtækinu.

Til að deila skýrslu, í listaskýrslum, eða í opinni skýrslu skal velja **Deila**. Á hlutanum **Deila skýrslu** skal slá inn fullt netfang fyrir einstaklinga eða hóp viðtakenda sem á að deila með. Fylgdu leiðbeiningunum á skjánum til að ljúka deilingunni. Frekari upplýsingar er að finna á [Deila stjórnborði eða skýrslu](/power-bi/collaborate-share/service-share-dashboards#share-a-dashboard-or-report).

> [!NOTE]
> Þú verður að hafa  [Power BI Pro-leyfi](/power-bi/service-features-license-type) og fólkið sem þú deilir með einnig. Efnið verður að vera á vinnusvæði með [Premium réttindi](/power-bi/service-premium-what-is). Nánari upplýsingar eru í [Aðferðir við að deila vinnu þinn í Power BI](/power-bi/service-how-to-collaborate-distribute-dashboards-reports).

## <a name="see-related-microsoft-trainingtrainingmodulesconfigure-powerbi-excel-dynamics--business-centralindex" />Sjá tengda [Microsoft þjálfun](/training/modules/configure-powerbi-excel-dynamics-365-business-central/index)

## <a name="see-also" />Sjá einnig

[Business Central og Power BI](admin-powerbi.md)  
[Búa til Power BI skýrslur til að birta [!INCLUDE [prod_long](includes/prod_long.md)]-gögn](across-how-use-financials-data-source-powerbi.md)  
[Power BI Samþættingaríhlutur og hönnunaryfirlit fyrir [!INCLUDE[prod_short](includes/prod_short.md)]](admin-powerbi-overview.md)  
[Vinna með Power BI Skýrslur í [!INCLUDE [prod_short](includes/prod_short.md)]](across-working-with-powerbi.md)  
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
